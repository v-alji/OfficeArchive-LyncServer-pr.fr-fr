---
title: 'Lync Server 2013 : Vérification ou configuration de l’authentification et de la certification dans les répertoires virtuels des services Internet (IIS)'
description: 'Lync Server 2013 : Vérifiez ou configurez l’authentification et la certification sur les répertoires virtuels IIS.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Verify or configure authentication and certification on IIS virtual directories
ms:assetid: 3ca90be0-1d64-447c-807a-3a2ee3bf625e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429702(v=OCS.15)
ms:contentKeyID: 48183883
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5e4d583eda7f0c7fb32b51dd5df6eb48af9b20d9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438935"
---
# <a name="verify-or-configure-authentication-and-certification-on-iis-virtual-directories-in-lync-server-2013"></a><span data-ttu-id="c8cb6-103">Connexion d’un Survivable Branch Appliance à un pool de serveurs frontaux</span><span class="sxs-lookup"><span data-stu-id="c8cb6-103">Verify or configure authentication and certification on IIS virtual directories in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c8cb6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c8cb6-104">

<span> </span></span></span>

<span data-ttu-id="c8cb6-105">_**Dernière modification de la rubrique :** 2012-05-25_</span><span class="sxs-lookup"><span data-stu-id="c8cb6-105">_**Topic Last Modified:** 2012-05-25_</span></span>

<span data-ttu-id="c8cb6-106">Suivez la procédure ci-dessous pour configurer le certificat sur les répertoires virtuels d’Internet Information Services (IIS) ou vérifier que le certificat est correctement configuré.</span><span class="sxs-lookup"><span data-stu-id="c8cb6-106">Use the following procedure to configure the certificate on your Internet Information Services (IIS) virtual directories or verify that the certificate is configured correctly.</span></span> <span data-ttu-id="c8cb6-107">Appliquez la procédure suivante à chaque serveur exécutant IIS dans votre pool de serveurs Lync interne et au directeur facultatif.</span><span class="sxs-lookup"><span data-stu-id="c8cb6-107">Perform the following procedure on each server running IIS in your internal Lync Server pool and the optional Director.or Director pool servers.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="c8cb6-108">La procédure suivante définit une procédure permettant de demander un certificat combiné qui est utilisé pour tous les rôles Lync Server, site Web interne et site Web externe dans IIS.</span><span class="sxs-lookup"><span data-stu-id="c8cb6-108">The following procedure defines a procedure to request a combined certificate that is used for all purposes Lync Server, Internal Web Site and External Web Site in IIS.</span></span> <span data-ttu-id="c8cb6-109">Lync Server 2010 a présenté un ensemble d' &nbsp; applets de certification Windows PowerShell Lync Server Management Shell pour une vue rapide de la gestion de la demande de certificat, de l’importation et de l’affectation.</span><span class="sxs-lookup"><span data-stu-id="c8cb6-109">Lync Server 2010 introduced a set of Lync Server Management Shell&nbsp;Windows PowerShell cmdlets for the express purpose of managing certificate request, import, and assignment.</span></span> <span data-ttu-id="c8cb6-110">La procédure suppose qu’il existe une autorité de certification déployée en interne (CA) qui peut traiter la demande.</span><span class="sxs-lookup"><span data-stu-id="c8cb6-110">The procedure assumes that there is an internally deployed certification authority (CA) that can process the request.</span></span> <span data-ttu-id="c8cb6-111">Si vous utilisez des certificats publics pour votre serveur Lync, ou si votre autorité de certification nécessite une demande hors connexion, voir la syntaxe détaillée de cette rubrique pour plus d’informations sur le paramètre – OUTPUT.</span><span class="sxs-lookup"><span data-stu-id="c8cb6-111">If you use public certificates for your Lync Server purposes, or your CA requires an offline request, see the detailed syntax in this topic for information on the –Output parameter.</span></span> <span data-ttu-id="c8cb6-112"><A href="https://docs.microsoft.com/powershell/module/skype/Request-CsCertificate">Requête-CsCertificate</A></span><span class="sxs-lookup"><span data-stu-id="c8cb6-112"><A href="https://docs.microsoft.com/powershell/module/skype/Request-CsCertificate">Request-CsCertificate</A></span></span>



</div>

<div>

## <a name="to-configure-authentication-and-certificates-on-iis-virtual-directories"></a><span data-ttu-id="c8cb6-113">Pour configurer l’authentification et les certificats sur les répertoires virtuels IIS</span><span class="sxs-lookup"><span data-stu-id="c8cb6-113">To configure authentication and certificates on IIS virtual directories</span></span>

1.  <span data-ttu-id="c8cb6-114">Pour pouvoir effectuer les opérations suivantes, vous devez être connecté à l’ordinateur (serveur frontal ou directeur) sur lequel les services Web sont installés et être un administrateur local.</span><span class="sxs-lookup"><span data-stu-id="c8cb6-114">To successfully complete the following, you must be logged on to the computer (Front End Server or Director) where the web services are installed and be a local administrator.</span></span> <span data-ttu-id="c8cb6-115">Vous devez disposer des autorisations de **lecture** et d' **inscription** sur l’autorité de certification auprès desquelles vous demandez des certificats, si celle-ci est l’autorité de certification de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="c8cb6-115">You must have the **read** and **enroll** permissions on the certification authority that you will be requesting certificates from, if the certification authority is your organization’s certification authority.</span></span> <span data-ttu-id="c8cb6-116">Vous n’avez pas besoin d’autorisations sur l’autorité de certification si vous allez configurer et envoyer une demande de certificat hors connexion.</span><span class="sxs-lookup"><span data-stu-id="c8cb6-116">You do not need permissions to the certification authority if you will configure and send an offline certificate request.</span></span>

2.  <span data-ttu-id="c8cb6-117">Cliquez sur **Démarrer**, sur **tous les programmes**, sélectionnez **Outils d’administration**, puis cliquez sur **Gestionnaire des services Internet (IIS)**.</span><span class="sxs-lookup"><span data-stu-id="c8cb6-117">Click **Start**, select **All Programs**, select **Administrative Tools**, and then click **Internet Information Services (IIS) Manager**.</span></span>

3.  <span data-ttu-id="c8cb6-118">Dans le **Gestionnaire des services Internet (IIS)**, sélectionnez **ServerName**.</span><span class="sxs-lookup"><span data-stu-id="c8cb6-118">In **Internet Information Services (IIS) Manager**, select **ServerName**.</span></span> <span data-ttu-id="c8cb6-119">Dans l' **affichage fonctionnalités**, sélectionnez **certificats de serveur**, cliquez avec le bouton droit, puis sélectionnez Ouvrir la **fonctionnalité**.</span><span class="sxs-lookup"><span data-stu-id="c8cb6-119">In **Features View**, select **Server Certificates**, right-click and select **Open Feature**.</span></span>
    
    <div>
    

    > [!TIP]  
    > <span data-ttu-id="c8cb6-120">Dans l’affichage fonctionnalités des certificats de serveur, si des certificats sont attribués au serveur, ils s’affichent ici.</span><span class="sxs-lookup"><span data-stu-id="c8cb6-120">In the Server Certificates Feature View, if there are certificates assigned to the server, they will appear here.</span></span> <span data-ttu-id="c8cb6-121">Si un certificat répond à la configuration requise pour le site Web externe dans IIS, vous pouvez le réutiliser.</span><span class="sxs-lookup"><span data-stu-id="c8cb6-121">If there is a certificate that matches the requirements for the External Web Site in IIS, you can re-use that certificate.</span></span> <span data-ttu-id="c8cb6-122">Pour afficher un certificat, cliquez avec le bouton droit sur le certificat, puis sélectionnez <STRONG>afficher.</STRONG></span><span class="sxs-lookup"><span data-stu-id="c8cb6-122">To view a certificate, right-click the certificate and select <STRONG>View…</STRONG></span></span>

    
    </div>

4.  <span data-ttu-id="c8cb6-123">Sur le serveur frontal ou le directeur pour lequel vous demandez le certificat, cliquez sur **Démarrer**, sélectionnez **tous les programmes**, **Microsoft Lync Server 2013**, puis cliquez sur **Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="c8cb6-123">On the Front End Server or Director that you are requesting the certificate for, click **Start**, select **All Programs**, select **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

5.  <span data-ttu-id="c8cb6-124">Dans Lync Server Management Shell, tapez les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="c8cb6-124">In the Lync Server Management Shell, type the following:</span></span>
    
        Get-CsCertificate
    
    <span data-ttu-id="c8cb6-125">La sortie est une liste des certificats actuellement sur le serveur dans le magasin de certificats personnels de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c8cb6-125">The output is a list of the certificates that are currently on the server in the Computer Personal certificate store.</span></span> <span data-ttu-id="c8cb6-126">Notez que dans le certificat combiné (autrement dit, les services Web internes et externes par défaut utilisent le même certificat) vous constaterez que la propriété Use sera remplie avec la valeur par défaut, WebServicesInternal et WebServicesExternal.</span><span class="sxs-lookup"><span data-stu-id="c8cb6-126">Note that in the combined certificate (that is, where the default, web services internal and web services external are using the same certificate) you will see that the Use property will be populated with Default, WebServicesInternal and WebServicesExternal.</span></span> <span data-ttu-id="c8cb6-127">Par ailleurs, la propriété d’empreinte est identique pour chaque type d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="c8cb6-127">Also, the Thumbprint property will be the same for each of the Use types.</span></span> <span data-ttu-id="c8cb6-128">Un exemple de sortie de Get-CsCertificate est illustré dans cet exemple :</span><span class="sxs-lookup"><span data-stu-id="c8cb6-128">An example output of Get-CsCertificate is shown in this example:</span></span>
    
    <span data-ttu-id="c8cb6-129">![Get-CsCertificate informations sur l’état actuel de scert](images/Gg429702.664f6326-6cd5-48e2-8235-fc3950ea43b4(OCS.15).jpg "Get-CsCertificate des informations sur l’état actuel de scert")</span><span class="sxs-lookup"><span data-stu-id="c8cb6-129">![Get-CsCertificate info on current scert status](images/Gg429702.664f6326-6cd5-48e2-8235-fc3950ea43b4(OCS.15).jpg "Get-CsCertificate info on current scert status")</span></span>

6.  <span data-ttu-id="c8cb6-130">Dans Lync Server Management Shell, tapez les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="c8cb6-130">In the Lync Server Management Shell, type the following:</span></span>
    
        Request-CsCertificate -New -Type Default,WebServicesInternal,WebServicesExternal -CA <CA Server FQDN\CA Instance> -Verbose -DomainName "<FQDN entries to be added to the Subject Alternative Name>"
    
    <span data-ttu-id="c8cb6-131">Où la commande complète s’afficherait comme suit :</span><span class="sxs-lookup"><span data-stu-id="c8cb6-131">Where the full command would appear like following example:</span></span>
    
        Request-CsCertificate -New -Type Default,WebServicesInternal,WebServicesExternal -CA dc01.contoso.net\contoso-DC01-CA -Verbose -DomainName "LyncdiscoverInternal.Contoso.com,Lyncdiscover.Contoso.com"
    
    <div>
    

    > [!TIP]  
    > <span data-ttu-id="c8cb6-132">Par défaut, Request-CsCertificate remplit le nom du sujet avec le nom du serveur ou du pool et les entrées du nom alternatif de l’objet, ainsi que le nom de domaine complet (FQDN) du serveur, nom de domaine complet (FQDN) du serveur et noms de domaine complets de services Web internes et externes.</span><span class="sxs-lookup"><span data-stu-id="c8cb6-132">By default, Request-CsCertificate will populate the subject name with the server or pool name and populate entries in the subject alternative name with the server FQDN, pool FQDN, Simple URL FQDNs, and internal and external web services FQDNs.</span></span> <span data-ttu-id="c8cb6-133">Pour ce faire, elle fait référence au document topologique dans votre déploiement.</span><span class="sxs-lookup"><span data-stu-id="c8cb6-133">It does this by referencing to the topology document in your deployment.</span></span> <span data-ttu-id="c8cb6-134">S’il existe une valeur manquante et que vous avez spécifié le paramètre – Verbose, vous serez averti que les valeurs calculées et réelles d’autres noms sont différentes, mais qu’elle ne vous indique pas quelles valeurs sont manquantes.</span><span class="sxs-lookup"><span data-stu-id="c8cb6-134">If there is a missing value and you have specified the –Verbose parameter, you will be notified that the computed and actual values for alternative names are different, but it does not inform you which values are missing.</span></span> <span data-ttu-id="c8cb6-135">Elle vous fournit la valeur calculée entière que l’applet de la cmdlet référence.</span><span class="sxs-lookup"><span data-stu-id="c8cb6-135">It does supply you with the entire computed value that the cmdlet references.</span></span> <span data-ttu-id="c8cb6-136">Utilisez la chaîne de noms alternatifs calculés dans la sortie pour demander à nouveau le certificat qui inclura toutes les valeurs.</span><span class="sxs-lookup"><span data-stu-id="c8cb6-136">Use the computed alternative names string in the output to re-request a new certificate that will include all values.</span></span>

    
    </div>
    
    <span data-ttu-id="c8cb6-137">![Sortie d’une demande de certificat à l’aide d’une requête-CsCertifica](images/Gg429702.9e59a657-fa75-4454-8fd3-57c81e829f7b(OCS.15).jpg "Sortie d’une demande de certificat à l’aide d' Request-CsCertifica")</span><span class="sxs-lookup"><span data-stu-id="c8cb6-137">![Output from cert request using Request-CsCertifica](images/Gg429702.9e59a657-fa75-4454-8fd3-57c81e829f7b(OCS.15).jpg "Output from cert request using Request-CsCertifica")</span></span>

7.  <span data-ttu-id="c8cb6-138">Dans Lync Server Management Shell, tapez les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="c8cb6-138">In the Lync Server Management Shell, type the following:</span></span>
    
        Set-CsCertificate -Type Default,WebServicesInternal,WebServicesExternal -Thumbprint <Thumbprint of certificate to use>
    
    <span data-ttu-id="c8cb6-139">Où la commande complète s’afficherait comme suit :</span><span class="sxs-lookup"><span data-stu-id="c8cb6-139">Where the full command would appear like following example:</span></span>
    
        Set-CsCertificate -Type Default,WebServicesInternal,WebServicesExternal -Thumbprint 466D9BB0E8B928B65AF38FA2D9F41E1B301ECE9D
    
    <span data-ttu-id="c8cb6-140">La sortie de l’applet de commande Set-CsCertificate montre que le certificat (identifié par l’empreinte numérique du certificat) est attribué à l’utilisation par défaut WebServicesExternal et WebServicesInternal.</span><span class="sxs-lookup"><span data-stu-id="c8cb6-140">The output from the Set-CsCertificate cmdlet will show that the same certificate (identified by the thumbprint of the certificate) is assigned for the Default, WebServicesExternal and WebServicesInternal usage.</span></span>
    
    <span data-ttu-id="c8cb6-141">![Sortie à partir de Set-CsCertificate sur IIS WebEx](images/Gg429702.dd451c9d-7b49-4408-8071-c868cb1e678c(OCS.15).jpg "Sortie à partir de Set-CsCertificate sur IIS WebEx")</span><span class="sxs-lookup"><span data-stu-id="c8cb6-141">![Output from Set-CsCertificate on IIS WebExt](images/Gg429702.dd451c9d-7b49-4408-8071-c868cb1e678c(OCS.15).jpg "Output from Set-CsCertificate on IIS WebExt")</span></span>

</div>

<div>

## <a name="to-verify-or-configure-authentication-and-certificates-on-iis-virtual-directories"></a><span data-ttu-id="c8cb6-142">Pour vérifier ou configurer l’authentification et les certificats dans les répertoires virtuels d’IIS</span><span class="sxs-lookup"><span data-stu-id="c8cb6-142">To verify or configure authentication and certificates on IIS virtual directories</span></span>

1.  <span data-ttu-id="c8cb6-143">Cliquez sur **Démarrer**, sur **tous les programmes**, sélectionnez **Outils d’administration**, puis cliquez sur **Gestionnaire des services Internet (IIS)**.</span><span class="sxs-lookup"><span data-stu-id="c8cb6-143">Click **Start**, select **All Programs**, select **Administrative Tools**, and then click **Internet Information Services (IIS) Manager**.</span></span>

2.  <span data-ttu-id="c8cb6-144">Dans le **Gestionnaire des services Internet (IIS)**, développez **NomServeur**, puis **sites**.</span><span class="sxs-lookup"><span data-stu-id="c8cb6-144">In **Internet Information Services (IIS) Manager**, expand **ServerName**, and then expand **Sites**.</span></span>

3.  <span data-ttu-id="c8cb6-145">Cliquez avec le bouton droit sur **site Web externe de Lync Server**, puis cliquez sur **modifier les liaisons** .</span><span class="sxs-lookup"><span data-stu-id="c8cb6-145">Right-click **Lync Server External Web Site**, and then click **Edit Bindings**</span></span>

4.  <span data-ttu-id="c8cb6-146">Vérifiez que https est associé au port 4443, puis cliquez sur **https**.</span><span class="sxs-lookup"><span data-stu-id="c8cb6-146">Verify that https is associated with port 4443, and then click **https**.</span></span>

5.  <span data-ttu-id="c8cb6-147">Sélectionnez l’entrée HTTPs, cliquez sur **modifier**, puis vérifiez que Lync Server WebServicesExternalCertificate est lié à ce protocole.</span><span class="sxs-lookup"><span data-stu-id="c8cb6-147">Select the HTTPS entry, click **Edit**, and then verify that Lync Server WebServicesExternalCertificate is bound to this protocol.</span></span> <span data-ttu-id="c8cb6-148">Comparez l’empreinte digitale de l’applet de certification Set-CsCertificate pour vous assurer que le certificat attendu est associé correctement à la liaison HTTPs.</span><span class="sxs-lookup"><span data-stu-id="c8cb6-148">Compare the thumbprint from the Set-CsCertificate cmdlet to ensure that the expected certificate is correctly associated with the HTTPS binding.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="c8cb6-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c8cb6-149">See Also</span></span>


[<span data-ttu-id="c8cb6-150">Get-CsCertificate</span><span class="sxs-lookup"><span data-stu-id="c8cb6-150">Get-CsCertificate</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsCertificate)  
[<span data-ttu-id="c8cb6-151">Set-CsCertificate</span><span class="sxs-lookup"><span data-stu-id="c8cb6-151">Set-CsCertificate</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsCertificate)  
  

<span data-ttu-id="c8cb6-152"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c8cb6-152"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

