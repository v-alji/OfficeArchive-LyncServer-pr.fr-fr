---
title: 'Lync Server 2013 : Modification des certificats pour la mobilité'
description: 'Lync Server 2013 : modification des certificats pour la mobilité.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Modifying certificates for mobility
ms:assetid: 4e9107af-20f4-4c2a-8c98-ca35b39a4e2d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690015(v=OCS.15)
ms:contentKeyID: 48184120
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 099122b1773c3f15d8ae0034ee5fa404225cdfd2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445693"
---
# <a name="modifying-certificates-for-mobility-in-lync-server-2013"></a><span data-ttu-id="29cbf-103">Modification des certificats pour la mobilité dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="29cbf-103">Modifying certificates for mobility in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="29cbf-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="29cbf-104">

<span> </span></span></span>

<span data-ttu-id="29cbf-105">_**Dernière modification de la rubrique :** 2014-06-20_</span><span class="sxs-lookup"><span data-stu-id="29cbf-105">_**Topic Last Modified:** 2014-06-20_</span></span>

<span data-ttu-id="29cbf-106">Pour prendre en charge les connexions sécurisées entre votre environnement Lync et vos clients mobiles, les certificats SSL (Secure Socket Layer) pour votre pool de directeurs, votre liste frontale et votre proxy inverse doivent être mis à jour avec des entrées de nouveau nom d’objet supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="29cbf-106">To support secure connections between your Lync environment and your mobile clients, the Secure Socket Layer (SSL) certificates for your Director pool, Front End pool, and reverse proxy are going to need to be updated with some additional subject alternative name (SAN) entries.</span></span> <span data-ttu-id="29cbf-107">Pour plus d’informations sur les exigences en matière de certificats pour la mobilité, voir la section exigences relatives aux certificats dans les [exigences techniques de mobilité dans Lync Server 2013](lync-server-2013-technical-requirements-for-mobility.md), mais de manière générale, vous devez obtenir de nouveaux certificats auprès de l’autorité de certification et ajouter ces certificats en suivant les étapes de cet article.</span><span class="sxs-lookup"><span data-stu-id="29cbf-107">If you need to check out more details about the certificate requirements for mobility, see the Certificate Requirements section in [Technical requirements for mobility in Lync Server 2013](lync-server-2013-technical-requirements-for-mobility.md), but basically you’ll need to get new certificates from the Certificate Authority with the additional SAN entries included, and then add those certificates using this article’s steps.</span></span>

<span data-ttu-id="29cbf-108">Bien entendu, avant de commencer, il est généralement judicieux de savoir quel autre nom de l’objet possède déjà vos certificats.</span><span class="sxs-lookup"><span data-stu-id="29cbf-108">Of course before you begin, it’s usually a good idea to know what subject alternative names your certificates already have.</span></span> <span data-ttu-id="29cbf-109">Si vous n’êtes pas sûr de ce que vous avez déjà configuré, il existe de nombreux moyens de le découvrir. Même si l’option est là pour exécuter la commande **Get-CsCertificate** et les autres commandes PowerShell pour afficher ces informations, (ce que nous allons voir ci-dessous) par défaut, les données sont tronquées de façon à ce que vous n’obteniez pas toutes les propriétés dont vous avez besoin.</span><span class="sxs-lookup"><span data-stu-id="29cbf-109">If you’re not sure what’s already been configured, there are a lot of ways to find out. While the option’s there to run the **Get-CsCertificate** and other PowerShell commands to view this information, (which we walk through below) by default that data will be truncated, so you may not get to see all the properties you need.</span></span> <span data-ttu-id="29cbf-110">Pour obtenir une vue d’ensemble du certificat et de toutes ses propriétés, vous pouvez accéder à Microsoft Management Console (MMC) et charger le composant logiciel enfichable Certificats (que nous allons également suivre ci-dessous), ou vous pouvez simplement consulter l’Assistant Déploiement de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="29cbf-110">In order to get a good look at the certificate and all its properties, you can go to the Microsoft Management Console (MMC) and load the Certificates snap-in (which we also walk through below), or you can just check in the Lync Server Deployment Wizard.</span></span>

<span data-ttu-id="29cbf-111">Comme indiqué plus haut, les étapes suivantes vous guident dans la mise à jour des certificats à l’aide de Lync Server Management Shell et de la console MMC.</span><span class="sxs-lookup"><span data-stu-id="29cbf-111">As noted above, the following steps will walk you through updating the certificates using the Lync Server Management Shell and the MMC.</span></span> <span data-ttu-id="29cbf-112">Si vous êtes intéressé par l’utilisation de l’Assistant certificat dans l’Assistant Déploiement de Lync Server pour ce faire, vous pouvez cocher [configurer des certificats pour le directeur de Lync server 2013](lync-server-2013-configure-certificates-for-the-director.md) pour le directeur ou le pool de réalisateur, si vous en avez configuré un (vous ne l’avez peut-être pas).</span><span class="sxs-lookup"><span data-stu-id="29cbf-112">If you’re interested in using the Certificate Wizard in the Lync Server Deployment Wizard for this instead, you can check [Configure certificates for the Director in Lync Server 2013](lync-server-2013-configure-certificates-for-the-director.md) out for the Director or Director pool, if you configured one (you may not have).</span></span> <span data-ttu-id="29cbf-113">Pour le serveur frontal ou le pool frontal, vous pouvez voir [configurer des certificats pour les serveurs dans Lync Server 2013](lync-server-2013-configure-certificates-for-servers.md).</span><span class="sxs-lookup"><span data-stu-id="29cbf-113">For the Front End Server or Front End pool, you’ll want to see [Configure certificates for servers in Lync Server 2013](lync-server-2013-configure-certificates-for-servers.md).</span></span>

<span data-ttu-id="29cbf-114">En dernier lieu, il est possible que vous disposiez d’un seul certificat par défaut dans votre environnement Lync Server 2013 ou que vous ayez des certificats séparés par défaut (tout sauf les services Web), WebServicesExternal et WebServicesInternal.</span><span class="sxs-lookup"><span data-stu-id="29cbf-114">One last thing to keep in mind is that you may have a single Default certificate in your Lync Server 2013 environment, or you may have separate certificates for Default (which is everything but the web services), WebServicesExternal and WebServicesInternal.</span></span> <span data-ttu-id="29cbf-115">Quelle que soit la configuration, suivez les étapes ci-dessous pour vous aider.</span><span class="sxs-lookup"><span data-stu-id="29cbf-115">Whatever your configuration, these steps should help you out.</span></span>

<div>

## <a name="to-update-certificates-with-new-subject-alternative-names-using-the-lync-server-management-shell"></a><span data-ttu-id="29cbf-116">Pour mettre à jour les certificats avec d’autres noms d’objet à l’aide de Lync Server Management Shell</span><span class="sxs-lookup"><span data-stu-id="29cbf-116">To update certificates with new subject alternative names using the Lync Server Management Shell</span></span>

1.  <span data-ttu-id="29cbf-117">Vous devez vous connecter à votre serveur Lync Server 2013 à l’aide d’un compte disposant de droits d’administrateur local et d’autorisations.</span><span class="sxs-lookup"><span data-stu-id="29cbf-117">You need to log on to your Lync Server 2013 server using an account that has local administrator rights and permissions.</span></span> <span data-ttu-id="29cbf-118">Par ailleurs, si vous exécutez la requête PowerShell **-CsCertificate** au cours des étapes 12 et ultérieures, le compte doit disposer de droits d’autorité de certification spécifiée.</span><span class="sxs-lookup"><span data-stu-id="29cbf-118">Additionally, if you’re running the PowerShell **Request-CsCertificate** in Steps 12 and beyond, the account needs to have rights to the specified Certificate Authority (CA).</span></span>

2.  <span data-ttu-id="29cbf-119">Démarrez Lync Server Management Shell : cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="29cbf-119">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="29cbf-120">Pour pouvoir attribuer un certificat mis à jour, vous devez identifier les certificats qui ont été attribués au serveur et le type d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="29cbf-120">Before you can assign an updated certificate, you’ll need to find out what certificates have been assigned to the server and for which type of use.</span></span> <span data-ttu-id="29cbf-121">À partir de la ligne de commande, tapez :</span><span class="sxs-lookup"><span data-stu-id="29cbf-121">At the command line, type:</span></span>
    
        Get-CsCertificate

4.  <span data-ttu-id="29cbf-122">Passez en revue la sortie de l’étape précédente pour voir si un seul certificat a été attribué pour plusieurs usages ou si un certificat différent est attribué à chaque utilisation.</span><span class="sxs-lookup"><span data-stu-id="29cbf-122">Review the output from the previous step to see whether a single certificate has been assigned for multiple uses, or whether a different certificate is assigned for each use.</span></span> <span data-ttu-id="29cbf-123">Dans le paramètre use, recherchez le mode d’utilisation d’un certificat.</span><span class="sxs-lookup"><span data-stu-id="29cbf-123">Look in the Use parameter to find out how a certificate’s being used.</span></span> <span data-ttu-id="29cbf-124">Comparez le paramètre d’empreinte numérique pour les certificats affichés pour déterminer si le même certificat a des usages multiples.</span><span class="sxs-lookup"><span data-stu-id="29cbf-124">Compare the Thumbprint parameter for the displayed certificates to see if the same certificate has multiple uses.</span></span> <span data-ttu-id="29cbf-125">Restez au coeur du paramètre d’empreinte numérique.</span><span class="sxs-lookup"><span data-stu-id="29cbf-125">Keep your eye on the Thumbprint parameter.</span></span>

5.  <span data-ttu-id="29cbf-126">Mettez à jour le certificat.</span><span class="sxs-lookup"><span data-stu-id="29cbf-126">Update the certificate.</span></span> <span data-ttu-id="29cbf-127">À partir de la ligne de commande, tapez :</span><span class="sxs-lookup"><span data-stu-id="29cbf-127">At the command line, type:</span></span>
    
        Set-CsCertificate -Type <type of certificate as displayed in the Use parameter> -Thumbprint <unique identifier>
    
    <span data-ttu-id="29cbf-128">Par exemple, si l’applet de commande **Get-CsCertificate** affichait un certificat utilisant la valeur par défaut, une autre avec une utilisation de WebServicesInternal, et une autre avec une utilisation de WebServicesExternal, et qu’ils ont tous la même valeur d’empreinte numérique, sur la ligne de commande, vous devez taper :</span><span class="sxs-lookup"><span data-stu-id="29cbf-128">For example, if the **Get-CsCertificate** cmdlet displayed a certificate with Use of Default, another with a Use of WebServicesInternal, and another with a Use of WebServicesExternal, and they all had the same Thumbprint value, at the command line, you should type:</span></span>
    
        Set-CsCertificate -Type Default,WebServicesInternal,WebServicesExternal -Thumbprint <Certificate Thumbprint>
    
    <span data-ttu-id="29cbf-129">**Important :**</span><span class="sxs-lookup"><span data-stu-id="29cbf-129">**Important:**</span></span>
    
    <span data-ttu-id="29cbf-130">Si un certificat distinct est attribué à chaque utilisation (de sorte que la valeur de l’empreinte numérique que vous avez examinée ci-dessus est différente pour chaque certificat), il est essentiel que vous n’exécutiez **pas** l’applet de contrôle **Set-CsCertificate** avec plusieurs types, comme dans l’exemple ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="29cbf-130">If a separate certificate is assigned for each use (so the Thumbprint value you checked above is different for each certificate), it’s vital that you **don’t** run the **Set-CsCertificate** cmdlet with multiple types, as in the example above.</span></span> <span data-ttu-id="29cbf-131">Dans ce cas, exécutez l’applet de la cmdlet **Set-CsCertificate** séparément pour chaque utilisation.</span><span class="sxs-lookup"><span data-stu-id="29cbf-131">In this case, run the **Set-CsCertificate** cmdlet separately for each use.</span></span> <span data-ttu-id="29cbf-132">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="29cbf-132">For example:</span></span>
    
        Set-CsCertificate -Type Default -Thumbprint <Certificate Thumbprint>
        Set-CsCertificate -Type WebServicesInternal -Thumbprint <Certificate Thumbprint>
        Set-CsCertificate -Type WebServicesExternal -Thumbprint <Certificate Thumbprint>

6.  <span data-ttu-id="29cbf-133">Pour afficher le certificat (ou les certificats), cliquez sur **Démarrer**, puis sur **exécuter..**..</span><span class="sxs-lookup"><span data-stu-id="29cbf-133">To view the certificate (or certificates), click **Start**, click **Run…**.</span></span> <span data-ttu-id="29cbf-134">Tapez MMC pour ouvrir Microsoft Management Console.</span><span class="sxs-lookup"><span data-stu-id="29cbf-134">Type MMC to open the Microsoft Management Console.</span></span>

7.  <span data-ttu-id="29cbf-135">Dans le menu MMC, sélectionnez **fichier**, choisissez **Ajouter/supprimer un composant logiciel enfichable...**, puis sélectionnez certificats.</span><span class="sxs-lookup"><span data-stu-id="29cbf-135">From the MMC menu, select **File**, select **Add/Remove snap-in…**, select Certificates.</span></span> <span data-ttu-id="29cbf-136">Cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="29cbf-136">Click **Add**.</span></span> <span data-ttu-id="29cbf-137">Lorsque vous y êtes invité, sélectionnez **compte d’ordinateur**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="29cbf-137">When prompted, select **Computer account**, then click **Next**.</span></span>

8.  <span data-ttu-id="29cbf-138">S’il s’agit du serveur sur lequel se trouve le certificat, sélectionnez **ordinateur local**.</span><span class="sxs-lookup"><span data-stu-id="29cbf-138">If this is the server where the certificate’s located, select **Local computer**.</span></span> <span data-ttu-id="29cbf-139">Si le certificat se trouve sur un autre ordinateur, vous devez sélectionner **un autre ordinateur**, puis taper le nom de domaine complet de l’ordinateur ou cliquer sur **Parcourir** dans **entrer le nom de l’objet pour le sélectionner**, puis taper le nom de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="29cbf-139">If the certificate’s located on another computer, you should select **Another computer**, and then you can either type in the fully qualified domain name of the computer, or click **Browse** in **Enter the object name to select**, and type the name of the computer.</span></span> <span data-ttu-id="29cbf-140">Cliquez sur **vérifier les noms**.</span><span class="sxs-lookup"><span data-stu-id="29cbf-140">Click **Check Names**.</span></span> <span data-ttu-id="29cbf-141">Lorsque le nom de l’ordinateur est résolu, il est souligné.</span><span class="sxs-lookup"><span data-stu-id="29cbf-141">When the name of the computer resolves, it’ll be underlined.</span></span> <span data-ttu-id="29cbf-142">Cliquez sur **OK**, puis sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="29cbf-142">Click **OK**, then click **Finish**.</span></span> <span data-ttu-id="29cbf-143">Cliquez sur **OK** pour valider la sélection et fermer la boîte de dialogue **Ajouter ou supprimer des composants additionnels** .</span><span class="sxs-lookup"><span data-stu-id="29cbf-143">Click **OK** to commit the selection and close the **Add or Remove Snap-ins** dialog.</span></span>

9.  <span data-ttu-id="29cbf-144">Pour afficher les propriétés du certificat, développez **certificats**, **personnel**, puis sélectionnez **certificats**.</span><span class="sxs-lookup"><span data-stu-id="29cbf-144">To view the properties of the certificate, expand **Certificates**, expand **Personal**, and select **Certificates**.</span></span> <span data-ttu-id="29cbf-145">Sélectionnez le certificat que vous voulez afficher, cliquez avec le bouton droit sur le certificat, puis sélectionnez **ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="29cbf-145">Select the certificate to view, right-click on the certificate and select **Open**.</span></span>

10. <span data-ttu-id="29cbf-146">Dans l’affichage **certificat** , sélectionnez **Détails**.</span><span class="sxs-lookup"><span data-stu-id="29cbf-146">In the **Certificate** view, select **Details**.</span></span> <span data-ttu-id="29cbf-147">À partir de cet emplacement, vous pouvez sélectionner le nom du sujet du certificat en sélectionnant **objet** et le nom de l’objet affecté ainsi que les propriétés associées apparaissent.</span><span class="sxs-lookup"><span data-stu-id="29cbf-147">From here, you can select the certificate subject name by selecting **Subject** and the assigned subject name and associated properties are displayed.</span></span>

11. <span data-ttu-id="29cbf-148">Pour afficher les noms de remplacement de l’objet affecté, sélectionnez **autre nom** de l’objet.</span><span class="sxs-lookup"><span data-stu-id="29cbf-148">To view the assigned subject alternative names, select **Subject Alternative Name**.</span></span> <span data-ttu-id="29cbf-149">Les noms de remplacement de l’objet affecté apparaissent ici.</span><span class="sxs-lookup"><span data-stu-id="29cbf-149">All assigned subject alternative names are displayed here.</span></span> <span data-ttu-id="29cbf-150">Le nom de remplacement de l’objet indiqué ici est de type **nom DNS** par défaut.</span><span class="sxs-lookup"><span data-stu-id="29cbf-150">The subject alternative names found here are of type **DNS Name** by default.</span></span> <span data-ttu-id="29cbf-151">Les membres suivants doivent s’afficher (qui doivent correspondre à des noms de domaine complets tels qu’ils sont représentées dans l’hôte DNS (A ou, si vous avez des enregistrements IPv6 AAAA) :</span><span class="sxs-lookup"><span data-stu-id="29cbf-151">You should see the following members (all of which should be fully qualified domain names as represented in DNS host (A or, if IPv6 AAAA) records:</span></span>
    
      - <span data-ttu-id="29cbf-152">Nom du pool pour ce pool ou nom de serveur unique s’il ne s’agit pas d’un pool</span><span class="sxs-lookup"><span data-stu-id="29cbf-152">Pool name for this pool, or the single server name if this isn’t a pool</span></span>
    
      - <span data-ttu-id="29cbf-153">Nom du serveur auquel le certificat est affecté</span><span class="sxs-lookup"><span data-stu-id="29cbf-153">Server name that the certificate is assigned to</span></span>
    
      - <span data-ttu-id="29cbf-154">Enregistrements d’URL simples, en règle générale et en ligne</span><span class="sxs-lookup"><span data-stu-id="29cbf-154">Simple URL records, typically meet and dialin</span></span>
    
      - <span data-ttu-id="29cbf-155">Services Web internes et services Web (par exemple, webpool01.contoso.net, webpool01.contoso.com), en fonction des choix effectués dans le générateur de topologie et des sélections de services Web.</span><span class="sxs-lookup"><span data-stu-id="29cbf-155">Web services internal and Web services external names (for example, webpool01.contoso.net, webpool01.contoso.com), based on choices made in Topology Builder and over-ridden web services selections.</span></span>
    
      - <span data-ttu-id="29cbf-156">S’il est déjà attribué, le lyncdiscover.\<sipdomain\></span><span class="sxs-lookup"><span data-stu-id="29cbf-156">If already assigned, the lyncdiscover.\<sipdomain\></span></span> <span data-ttu-id="29cbf-157">et lyncdiscoverinternal.\<sipdomain\></span><span class="sxs-lookup"><span data-stu-id="29cbf-157">and lyncdiscoverinternal.\<sipdomain\></span></span> <span data-ttu-id="29cbf-158">registres.</span><span class="sxs-lookup"><span data-stu-id="29cbf-158">records.</span></span>
    
    <span data-ttu-id="29cbf-159">Le dernier élément correspond à ce que vous êtes le plus intéressé par le biais d’une entrée SAN lyncdiscover et lyncdiscoverinternal.</span><span class="sxs-lookup"><span data-stu-id="29cbf-159">The last item is what you’re most interested in – if there’s a lyncdiscover and lyncdiscoverinternal SAN entry.</span></span>
    
    <span data-ttu-id="29cbf-160">Répétez ces étapes si vous avez plusieurs certificats à vérifier.</span><span class="sxs-lookup"><span data-stu-id="29cbf-160">Repeat these steps if you have multiple certificates to check.</span></span> <span data-ttu-id="29cbf-161">Une fois que vous disposez de ces informations, vous pouvez fermer l’affichage du certificat et la console MMC.</span><span class="sxs-lookup"><span data-stu-id="29cbf-161">Once you have this information, you can close the certificate view and the MMC.</span></span>

12. <span data-ttu-id="29cbf-162">Si un autre nom de l’objet du service de découverte automatique est manquant et que vous utilisez un certificat par défaut unique pour les types WebServicesInternal et WebServiceExternal, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="29cbf-162">If an Autodiscover Service subject alternative name is missing, and you are using a single Default certificate for the Default, WebServicesInternal and WebServiceExternal types, do the following:</span></span>
    
      - <span data-ttu-id="29cbf-163">Dans l’invite de la ligne de commande Lync Server Management Shell, tapez :</span><span class="sxs-lookup"><span data-stu-id="29cbf-163">At the Lync Server Management Shell command line prompt, type:</span></span>
        
            Request-CsCertificate -New -Type Default,WebServicesInternal,WebServicesExternal -Ca dc\myca -AllSipDomain -verbose
        
        <span data-ttu-id="29cbf-164">Si vous avez de nombreux domaines SIP, vous ne pouvez pas utiliser le nouveau paramètre AllSipDomain.</span><span class="sxs-lookup"><span data-stu-id="29cbf-164">If you have many SIP domains, you can’t use the new AllSipDomain parameter.</span></span> <span data-ttu-id="29cbf-165">À la place, vous devez utiliser le paramètre NomDomaine.</span><span class="sxs-lookup"><span data-stu-id="29cbf-165">Instead, you need to use the DomainName parameter.</span></span> <span data-ttu-id="29cbf-166">Lorsque vous utilisez le paramètre nom_domaine, vous devez définir le nom de domaine complet (FQDN) pour les enregistrements lyncdiscoverinternal et lyncdiscover.</span><span class="sxs-lookup"><span data-stu-id="29cbf-166">When you use the DomainName parameter, you’ve got to define the FQDN for the lyncdiscoverinternal and lyncdiscover records.</span></span> <span data-ttu-id="29cbf-167">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="29cbf-167">For example:</span></span>
        
            Request-CsCertificate -New -Type Default,WebServicesInternal,WebServicesExternal -Ca dc\myca -DomainName "LyncdiscoverInternal.contoso.com, LyncdiscoverInternal.contoso.net" -verbose
    
      - <span data-ttu-id="29cbf-168">Pour attribuer le certificat, tapez ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="29cbf-168">To assign the certificate, type the following:</span></span>
        
            Set-CsCertificate -Type Default,WebServicesInternal,WebServicesExternal -Thumbprint <Certificate Thumbprint>
        
        <span data-ttu-id="29cbf-169">Où « empreinte » est l’empreinte digitale affichée pour le certificat nouvellement émis.</span><span class="sxs-lookup"><span data-stu-id="29cbf-169">Where “Thumbprint” is the thumbprint displayed for the newly issued certificate.</span></span>

13. <span data-ttu-id="29cbf-170">Pour un SAN de découverte automatique absent manquant lors de l’utilisation de certificats séparés par défaut, WebServicesInternal et WebServicesExternal, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="29cbf-170">For a missing internal Autodiscover SAN when using separate certificates for Default, WebServicesInternal, and WebServicesExternal, do the following:</span></span>
    
      - <span data-ttu-id="29cbf-171">Dans l’invite de la ligne de commande Lync Server Management Shell, tapez :</span><span class="sxs-lookup"><span data-stu-id="29cbf-171">At the Lync Server Management Shell command line prompt, type:</span></span>
        
            Request-CsCertificate -New -Type WebServicesInternal -Ca dc\myca -AllSipDomain -verbose
        
        <span data-ttu-id="29cbf-172">Si vous avez de nombreux domaines SIP, vous ne pouvez pas utiliser le nouveau paramètre AllSipDomain.</span><span class="sxs-lookup"><span data-stu-id="29cbf-172">If you have many SIP domains, you can’t use the new AllSipDomain parameter.</span></span> <span data-ttu-id="29cbf-173">À la place, vous devez utiliser le paramètre NomDomaine.</span><span class="sxs-lookup"><span data-stu-id="29cbf-173">Instead, you need to use the DomainName parameter.</span></span> <span data-ttu-id="29cbf-174">Lorsque vous utilisez le paramètre nom_domaine, vous devez utiliser un préfixe approprié pour le nom de domaine complet (FQDN) du domaine SIP.</span><span class="sxs-lookup"><span data-stu-id="29cbf-174">When you use the DomainName parameter, you’ve got to use an appropriate prefix for the SIP domain FQDN.</span></span> <span data-ttu-id="29cbf-175">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="29cbf-175">For example:</span></span>
        
            Request-CsCertificate -New -Type WebServicesInternal -Ca dc\myca -DomainName "LyncdiscoverInternal.contoso.com, LyncdiscoverInternal.contoso.net" -verbose
    
      - <span data-ttu-id="29cbf-176">Pour un autre nom d’objet de découverte automatique externe manquant, sur la ligne de commande, tapez :</span><span class="sxs-lookup"><span data-stu-id="29cbf-176">For a missing external Autodiscover subject alternative name, at the command line, type:</span></span>
        
            Request-CsCertificate -New -Type WebServicesExternal -Ca dc\myca -AllSipDomain -verbose
        
        <span data-ttu-id="29cbf-177">Si vous avez de nombreux domaines SIP, vous ne pouvez pas utiliser le nouveau paramètre AllSipDomain.</span><span class="sxs-lookup"><span data-stu-id="29cbf-177">If you have many SIP domains, you can’t use the new AllSipDomain parameter.</span></span> <span data-ttu-id="29cbf-178">À la place, vous devez utiliser le paramètre NomDomaine.</span><span class="sxs-lookup"><span data-stu-id="29cbf-178">Instead, you need to use the DomainName parameter.</span></span> <span data-ttu-id="29cbf-179">Lorsque vous utilisez le paramètre nom_domaine, vous devez utiliser un préfixe approprié pour le nom de domaine complet (FQDN) du domaine SIP.</span><span class="sxs-lookup"><span data-stu-id="29cbf-179">When you use the DomainName parameter, you’ve got to use an appropriate prefix for the SIP domain FQDN.</span></span> <span data-ttu-id="29cbf-180">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="29cbf-180">For example:</span></span>
        
            Request-CsCertificate -New -Type WebServicesExternal -Ca dc\myca -DomainName "Lyncdiscover.contoso.com, Lyncdiscover.contoso.net" -verbose
    
      - <span data-ttu-id="29cbf-181">Pour attribuer les types de certificats individuels, tapez les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="29cbf-181">To assign the individual certificate types, type the following:</span></span>
        
            Set-CsCertificate -Type Default -Thumbprint <Certificate Thumbprint>
            Set-CsCertificate -Type WebServicesInternal -Thumbprint <Certificate Thumbprint>
            Set-CsCertificate -Type WebServicesExternal -Thumbprint <Certificate Thumbprint>
        
        <span data-ttu-id="29cbf-182">Où « empreinte » est l’empreinte digitale affichée pour les certificats individuels émis.</span><span class="sxs-lookup"><span data-stu-id="29cbf-182">Where “Thumbprint” is the thumbprint displayed for the newly issued individual certificates.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="29cbf-183">Remarque : les étapes 12 et 13 doivent être exécutées uniquement si le compte qui les exécute a accès à l’autorité de certification avec les autorisations appropriées.</span><span class="sxs-lookup"><span data-stu-id="29cbf-183">Just to note, Steps 12 and 13 should be run only if the account running them has access to the Certificate Authority with appropriate permissions.</span></span> <span data-ttu-id="29cbf-184">Si vous ne parvenez pas à vous connecter avec un compte qui dispose de ces autorisations, ou si vous utilisez une autorité de certification publique ou distante pour vos certificats, vous devez les demander par le biais de l’Assistant Déploiement de Lync Server, qui a été touché au début de l’article.</span><span class="sxs-lookup"><span data-stu-id="29cbf-184">If you are unable to log in with an account that’s got those permissions, or if you’re using a public or remote Certificate Authority for your certificates, you would need to request them through the Lync Server Deployment Wizard, which was touched on at the top of the article.</span></span>

    
    <span data-ttu-id="29cbf-185"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="29cbf-185"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

