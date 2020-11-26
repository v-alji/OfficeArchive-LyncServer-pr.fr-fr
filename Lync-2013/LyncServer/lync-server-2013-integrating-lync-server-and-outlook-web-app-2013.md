---
title: 'Lync Server 2013 : intégration de Lync Server et d’Outlook Web App 2013'
description: 'Lync Server 2013 : intégration de Lync Server et d’Outlook Web App 2013.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Integrating Lync Server 2013 and Outlook Web App 2013
ms:assetid: 513d4cc7-aa87-4f68-b99d-d58b63bdf242
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688055(v=OCS.15)
ms:contentKeyID: 49733649
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0d9c7e91dba22f78325eaddc5b5d7469ccf4cc92
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426892"
---
# <a name="integrating-microsoft-lync-server-2013-and-microsoft-outlook-web-app-2013"></a><span data-ttu-id="fb9e7-103">Intégration de Microsoft Lync Server 2013 et Microsoft Outlook Web App 2013</span><span class="sxs-lookup"><span data-stu-id="fb9e7-103">Integrating Microsoft Lync Server 2013 and Microsoft Outlook Web App 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fb9e7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fb9e7-104">

<span> </span></span></span>

<span data-ttu-id="fb9e7-105">_**Dernière modification de la rubrique :** 2013-02-03_</span><span class="sxs-lookup"><span data-stu-id="fb9e7-105">_**Topic Last Modified:** 2013-02-03_</span></span>

<span data-ttu-id="fb9e7-106">Outre l’intégration avec Microsoft Outlook 2013, Microsoft Lync Server 2013 peut être entièrement intégré à Microsoft Outlook Web App 2013 ; entre autres choses, la messagerie instantanée et la présence dans Outlook Web App sont ajoutées, et votre liste de contacts unifiée doit être partagée entre Outlook Web App et Microsoft Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="fb9e7-106">In addition to integrating with Microsoft Outlook 2013, Microsoft Lync Server 2013 can be fully integrated with Microsoft Outlook Web App 2013; among other things, this adds instant messaging and presence to Outlook Web App, and enables your unified contact list to be shared between Outlook Web App and Microsoft Lync 2013.</span></span> <span data-ttu-id="fb9e7-107">Pour intégrer Lync Server 2013 et Outlook Web App, vous devez commencer par vérifier que le Runtime API managée de l' 4,0 API Exchange a été installé sur votre serveur principal Microsoft Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="fb9e7-107">In order to integrate Lync Server 2013 and Outlook Web App, you must first verify that the Unified Communications Managed API 4.0 Runtime has been installed in your Microsoft Exchange Server 2013 backend server.</span></span> <span data-ttu-id="fb9e7-108">Pour permettre l’intégration de skype16_server et d’Outlook Web App, vous devez d’abord vérifier que le runtime Unified Communications Managed API 4.0 a été installé sur votre serveur principal nm-exch-15-formal Pour ce faire, recherchez la valeur de registre suivante :</span><span class="sxs-lookup"><span data-stu-id="fb9e7-108">You can do this by looking for the existence of the following registry value:</span></span>

<span data-ttu-id="fb9e7-109">HKEY \_ local \_ machine \\ système de \\ CurrentControlSet \\ services CurrentControlSet \\ owa \\ instantmessaging \\ ImplementationDLLPath</span><span class="sxs-lookup"><span data-stu-id="fb9e7-109">HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Services\\MSExchange OWA\\InstantMessaging\\ImplementationDLLPath</span></span>

<span data-ttu-id="fb9e7-110">ImplementationDLLPath doit pointer vers l’emplacement du dossier correspondant au fichier Microsoft.Rtc.Internal.Ucweb.dll.</span><span class="sxs-lookup"><span data-stu-id="fb9e7-110">The ImplementationDLLPath should point to the folder location for the file Microsoft.Rtc.Internal.Ucweb.dll.</span></span> <span data-ttu-id="fb9e7-111">Si ce n’est pas le cas, ou si la valeur de Registre n’existe pas, téléchargez et installez le programme d’installation d’UCMA Runtime à partir du centre de téléchargement Microsoft <https://www.microsoft.com/download/details.aspx?id=34992> .</span><span class="sxs-lookup"><span data-stu-id="fb9e7-111">If it does not, or if the registry value does not exist, then you should download and install the UCMA Runtime setup program from the Microsoft Download Center at <https://www.microsoft.com/download/details.aspx?id=34992>.</span></span> <span data-ttu-id="fb9e7-112">Cette page comporte également des informations sur l’installation du runtime UCMA.</span><span class="sxs-lookup"><span data-stu-id="fb9e7-112">Information on how to install the UCMA Runtime can be found on that same web page.</span></span>

<span data-ttu-id="fb9e7-113">**Compatibilité descendante**</span><span class="sxs-lookup"><span data-stu-id="fb9e7-113">**Backward Compatibility**</span></span>

<span data-ttu-id="fb9e7-114">Lync Server 2013 peut être intégré aux versions de Microsoft Exchange Server 2010 de la messagerie unifiée et d’Outlook Web App.</span><span class="sxs-lookup"><span data-stu-id="fb9e7-114">Lync Server 2013 can be integrated with the Microsoft Exchange Server 2010 versions of both unified messaging and Outlook Web App.</span></span> <span data-ttu-id="fb9e7-115">Pour plus d’informations, reportez-vous à l’article déploiement de la messagerie UNIFIÉe Exchange locale pour fournir la messagerie vocale de Lync Server 2010 à l’adresse [https://technet.microsoft.com/library/gg398768.aspx](lync-server-2013-deploying-on-premises-exchange-um-to-provide-lync-server-2013-voice-mail.md) .</span><span class="sxs-lookup"><span data-stu-id="fb9e7-115">For more information, see the article Deploying On-Premises Exchange UM to Provide Lync Server 2010 Voice Mail at [https://technet.microsoft.com/library/gg398768.aspx](lync-server-2013-deploying-on-premises-exchange-um-to-provide-lync-server-2013-voice-mail.md).</span></span> <span data-ttu-id="fb9e7-116">Si vous intégrationz à Exchange 2010, vous ne disposez pas de fonctionnalités spécifiques de Lync Server telles que le magasin de contacts unifié et l’archivage Lync-to-Exchange.</span><span class="sxs-lookup"><span data-stu-id="fb9e7-116">If you integrate with Exchange 2010 you will not have Lync Server specific features such as the unified contact store and Lync-to-Exchange archiving.</span></span>

<span data-ttu-id="fb9e7-117">Microsoft Lync 2013 peut également être utilisé en association avec Exchange 2010 et Outlook 2010.</span><span class="sxs-lookup"><span data-stu-id="fb9e7-117">Microsoft Lync 2013 can also be used in conjunction with Exchange 2010 and Outlook 2010.</span></span> <span data-ttu-id="fb9e7-118">De nouveau, il est possible que de nouvelles fonctionnalités telles que le magasin de contacts unifié et les photos haute résolution ne soient pas disponibles pour les utilisateurs de Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="fb9e7-118">Once again, however, new functionality such as the unified contact store and high-resolution photos will not be available to Lync 2013 users.</span></span> <span data-ttu-id="fb9e7-119">Ces nouvelles fonctionnalités nécessitent Lync Server 2013 et Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="fb9e7-119">These new capabilities require both Lync Server 2013 and Exchange 2013.</span></span>

<span data-ttu-id="fb9e7-120">**Création d’un pool d’applications approuvées pour Outlook Web App**</span><span class="sxs-lookup"><span data-stu-id="fb9e7-120">**Creating a Trusted Application Pool for Outlook Web App**</span></span>

<span data-ttu-id="fb9e7-121">Si vous avez installé le service routeur de messagerie unifiée Microsoft Exchange et le service de messagerie unifiée Microsoft Exchange sur le même ordinateur, vous n’avez pas besoin de créer un pool d’applications approuvé pour Outlook Web App.</span><span class="sxs-lookup"><span data-stu-id="fb9e7-121">If you have installed the Microsoft Exchange Unified Messaging Call Router service and the Microsoft Exchange Unified Messaging service on the same computer then there is no need to create a trusted application pool for Outlook Web App.</span></span> <span data-ttu-id="fb9e7-122">(Cela suppose que le serveur en question héberge un plan de numérotation de messagerie unifiée SipName.) Si vous utilisez un ordinateur unique pour héberger ces deux services, vous pouvez passer à la section de ce document intitulée **activation de la messagerie instantanée dans Outlook Web App**.</span><span class="sxs-lookup"><span data-stu-id="fb9e7-122">(This assumes that the server in question is hosting a SipName UM dial plan.) If you are using a single computer to host both of these services then you can skip to the section of this document titled **Enabling Instant Messaging on Outlook Web App**.</span></span>

<span data-ttu-id="fb9e7-123">Lync Server 2013 peut détecter automatiquement les serveurs Exchange qui hébergent un plan de numérotation de messagerie unifiée SipName ; ils sont automatiquement ajoutés à la liste des serveurs connus de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="fb9e7-123">Lync Server 2013 can autodiscover any Exchange servers that host a SipName UM dial plan; these servers are automatically added to the Lync Server Known Servers List.</span></span> <span data-ttu-id="fb9e7-124">Il n’est pas nécessaire de créer un pool d’applications digne de confiance et de l’ajouter à la liste de serveurs connus.</span><span class="sxs-lookup"><span data-stu-id="fb9e7-124">There is no need to create a trusted application pool and add these servers to the Known Servers List.</span></span> <span data-ttu-id="fb9e7-125">En fait, cela entraînera l’arrêt de l’intégration d’Outlook Web App.</span><span class="sxs-lookup"><span data-stu-id="fb9e7-125">In fact, doing so will cause Outlook Web App integration to stop working.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="fb9e7-126">C’est la raison pour laquelle la topologie du serveur Lync possède désormais deux entrées pour le même ordinateur : l’entrée découverte automatique et l’entrée ajoutée manuellement.</span><span class="sxs-lookup"><span data-stu-id="fb9e7-126">This is due to the fact that the Lync Server topology will now have two entries for the same computer: the autodiscovered entry, and the manually-added entry.</span></span> <span data-ttu-id="fb9e7-127">Pour résoudre ce problème et permettre à Outlook Web App de fonctionner de nouveau, utilisez Windows PowerShell pour supprimer les entrées du pool approuvé et les applications approuvées associées au serveur.</span><span class="sxs-lookup"><span data-stu-id="fb9e7-127">To fix the problem, and to get Outlook Web App working again, use Windows PowerShell to remove the trusted pool and trusted application entries for the server.</span></span> <span data-ttu-id="fb9e7-128">Pour plus d’informations, reportez-vous aux rubriques d’aide des applets de commande <A href="https://docs.microsoft.com/powershell/module/skype/Remove-CsTrustedApplicationPool">Remove-CsTrustedApplicationPool</A> et <A href="https://docs.microsoft.com/powershell/module/skype/Remove-CsTrustedApplication">Remove-CsTrustedApplication</A>.</span><span class="sxs-lookup"><span data-stu-id="fb9e7-128">See the help topics for the <A href="https://docs.microsoft.com/powershell/module/skype/Remove-CsTrustedApplicationPool">Remove-CsTrustedApplicationPool</A> and <A href="https://docs.microsoft.com/powershell/module/skype/Remove-CsTrustedApplication">Remove-CsTrustedApplication</A> cmdlets for more information.</span></span>



</div>

<span data-ttu-id="fb9e7-129">Si ces deux services s’exécutent sur des ordinateurs distincts, une fois que vous avez vérifié que le runtime de l’API managée de communications unifiées 4,0 est installé, vous devez créer un pool d’applications approuvé Lync Server et une application de confiance associée à Outlook Web App. le serveur sera ajouté à la liste serveurs connus.</span><span class="sxs-lookup"><span data-stu-id="fb9e7-129">If these two services are running on separate computers then, after you have verified that the Unified Communications Managed API 4.0 Runtime has been installed, you must create a Lync Server trusted application pool and a trusted application associated with Outlook Web App; that will add the server to the Known Servers List.</span></span> <span data-ttu-id="fb9e7-130">Pour ce faire, commencez par exécuter une commande similaire à celle-ci à partir de Lync Server Management Shell :</span><span class="sxs-lookup"><span data-stu-id="fb9e7-130">To do that, first run a command similar to this from within the Lync Server Management Shell:</span></span>

    New-CsTrustedApplicationPool -Identity atl-owa-001.litwareinc.com -Registrar atl-cs-001.litwareinc.com -Site Redmond -RequiresReplication $False

<span data-ttu-id="fb9e7-131">Dans la commande précédente, atl-owa-001.litwareinc.com est le nom de domaine complet du pool Outlook Web App. il doit s’agir du nom qui apparaît dans le champ nom de l’objet et le nom de l’objet (SAN) du certificat qui permet d’accéder à Outlook Web App.</span><span class="sxs-lookup"><span data-stu-id="fb9e7-131">In the preceding command, atl-owa-001.litwareinc.com is the fully qualified domain name of the Outlook Web App pool; this must be the same name that appears in the Subject Name and Subject Alternative Name (SAN) fields of the certificate that provides access to Outlook Web App.</span></span> <span data-ttu-id="fb9e7-132">De même, atl-cs-001.litwareinc.com est le nom de domaine complet du pool Lync Server 2013 qui héberge le nouveau pool d’applications approuvées.</span><span class="sxs-lookup"><span data-stu-id="fb9e7-132">Likewise, atl-cs-001.litwareinc.com is the fully qualified domain name of the Lync Server 2013 pool that will host the new trusted application pool.</span></span> <span data-ttu-id="fb9e7-133">Notez également que le site spécifié, Redmond, représente le SiteID du site du serveur Lync.</span><span class="sxs-lookup"><span data-stu-id="fb9e7-133">Note, too that the specified site, Redmond, represents the SiteID of the Lync Server site.</span></span> <span data-ttu-id="fb9e7-134">Le SiteID n’est pas nécessairement le même que le DisplayName du site ; vous pouvez récupérer des SiteIDs pour vos sites Lync Server en exécutant la commande suivante à partir de Lync Server Management Shell :</span><span class="sxs-lookup"><span data-stu-id="fb9e7-134">The SiteID is not necessarily the same as the site's DisplayName; you can retrieve SiteIDs for your Lync Server sites by running the following command from the Lync Server Management Shell:</span></span>

    Get-CsSite | Select-Object DisplayName, SiteID

<span data-ttu-id="fb9e7-135">Après avoir créé le pool d’applications approuvées, utilisez une commande semblable à ce qui suit pour configurer une identité d’application et un port pour Outlook Web App :</span><span class="sxs-lookup"><span data-stu-id="fb9e7-135">After creating the trusted application pool, use a command similar to the following to configure an application Identity and a port for Outlook Web App:</span></span>

    New-CsTrustedApplication -ApplicationId OutlookWebApp -TrustedApplicationPoolFqdn atl-owa-001.litwareinc.com  -Port 5199

<span data-ttu-id="fb9e7-p110">Dans la commande précédente, ApplicationID est simplement un identificateur convivial utilisé pour différencier les applications approuvées. ApplicationID peut être une chaîne de texte qui ne contient pas d’espaces vides ou autres caractères interdits (pour être assuré de créer un identificateur valide, nous vous recommandons d’utiliser uniquement des lettres et des nombres lorsque vous définissez la valeur ApplicationID). La valeur affectée au paramètre Port est également laissée à la discrétion de l’administrateur : il peut s’agir de n’importe quel port réseau disponible.</span><span class="sxs-lookup"><span data-stu-id="fb9e7-p110">In the preceding command, the ApplicationID is simply a friendly identifier used to distinguish trusted applications. The ApplicationID can be any text string that does not include blank spaces or other prohibited characters. (To ensure that you create a valid identifier, it is recommended that you use only letters and numbers when specifying an ApplicationId.) The value assigned to the Port parameter is also left to the administrator's discretion: this can be any available network port.</span></span>

<span data-ttu-id="fb9e7-139">Après la création de l’application fiable, vous devez exécuter la commande suivante pour activer les modifications apportées à la topologie de votre serveur Lync :</span><span class="sxs-lookup"><span data-stu-id="fb9e7-139">After creating the trusted application you must run the following command to enable the changes to your Lync Server topology:</span></span>

    Enable-CsTopology

<span data-ttu-id="fb9e7-140">Notez que vous devez également ajouter votre serveur de boîte aux lettres et votre serveur de messagerie Exchange à l’ensemble de vos plans de numérotation URI SIP.</span><span class="sxs-lookup"><span data-stu-id="fb9e7-140">Note that you must also add your Exchange client access and mailbox server to all of your SIP Uri dial plans.</span></span> <span data-ttu-id="fb9e7-141">Les serveurs seront alors configurés en tant qu’homologues SIP approuvés avec la topologie ExUmRouting pour Lync Server.</span><span class="sxs-lookup"><span data-stu-id="fb9e7-141">In turn, this will configure the servers as trusted SIP peers with the ExUmRouting topology for Lync Server.</span></span>

<span data-ttu-id="fb9e7-142">**Activation de la messagerie instantanée sur Outlook Web App**</span><span class="sxs-lookup"><span data-stu-id="fb9e7-142">**Enabling Instant Messaging on Outlook Web App**</span></span>

<span data-ttu-id="fb9e7-143">Lorsque Lync Server est correctement configuré, vous pouvez alors commencer à configurer Outlook Web App.</span><span class="sxs-lookup"><span data-stu-id="fb9e7-143">With Lync Server correctly configured you can then begin to configure Outlook Web App.</span></span> <span data-ttu-id="fb9e7-144">La première étape de ce processus consiste à activer la messagerie instantanée sur tous vos répertoires virtuels Outlook Web App sur votre serveur principal.</span><span class="sxs-lookup"><span data-stu-id="fb9e7-144">The first step in that process is to enable instant messaging on all your Outlook Web App virtual directories on your front end servers.</span></span> <span data-ttu-id="fb9e7-145">(Il est inutile d’activer la messagerie instantanée pour les répertoires virtuels sur vos serveurs principaux.</span><span class="sxs-lookup"><span data-stu-id="fb9e7-145">(There is no need to enable instant messaging for the virtual directories on your backend servers.</span></span> <span data-ttu-id="fb9e7-146">En fait, nous vous conseillons de ne pas activer la messagerie instantanée sur vos serveurs principaux.) L’activation de la messagerie instantanée sur les serveurs d’accès client peut être activée en exécutant la commande suivante à partir d’Exchange Management Shell :</span><span class="sxs-lookup"><span data-stu-id="fb9e7-146">In fact, it is recommended that you do not enable instant messaging on your backend servers.) Instant messaging can be enabled on the client access servers by running the following command from within the Exchange Management Shell:</span></span>

    Get-OwaVirtualDirectory | Set-OwaVirtualDirectory -InstantMessagingEnabled $True -InstantMessagingType OCS

<div>


> [!NOTE]  
> <span data-ttu-id="fb9e7-p113">Par défaut, la messagerie instantanée est activée quand vous installez Outlook Web App ; en d’autres termes, la propriété InstantMessagingEnabled est définie sur True. Toutefois, vous devez exécuter la commande précédente pour définir le type de messagerie instantanée sur OCS. Par défaut, la propriété InstantMessagingType est définie sur None.</span><span class="sxs-lookup"><span data-stu-id="fb9e7-p113">By default, instant messaging is enabled when you install Outlook Web App; that is, the InstantMessagingEnabled property is set to True. However, you must still run the preceding command in order to set the instant messaging type to OCS. By default, InstantMessagingType is set to None.</span></span>



</div>

<span data-ttu-id="fb9e7-150">Ensuite, vous devez ajouter les deux lignes suivantes à Outlook Web App Web.config fichier (il se trouve généralement dans le dossier C : \\ Program Files \\ Microsoft \\ Exchange Server \\ v15 \\ ClientAccess \\ OWA).</span><span class="sxs-lookup"><span data-stu-id="fb9e7-150">Next you must add the following two lines to Outlook Web App Web.config file (this file is typically located in the folder C:\\Program Files\\Microsoft\\Exchange Server\\V15\\ClientAccess\\Owa).</span></span> <span data-ttu-id="fb9e7-151">Ces deux lignes doivent être ajoutées sous le \<AppSettings\> nœud dans le fichier Web.config, et cette procédure doit être effectuée uniquement sur les serveurs principaux dans lesquels Outlook Web App a été installé :</span><span class="sxs-lookup"><span data-stu-id="fb9e7-151">These two lines should be added under the \<AppSettings\> node in the Web.config file, and this procedure should be carried out only on the backend servers where Outlook Web App has been installed:</span></span>

    <add key="IMCertificateThumbprint" value="EA5A332496CC05DA69B75B66111C0F78A110D22d"/>
    <add key="IMServerName" value="atl-cs-001.litwareinc.com"/>

<span data-ttu-id="fb9e7-152">Dans l’exemple ci-dessus, la valeur de IMCertificateThumbprint doit être l’empreinte numérique du certificat Exchange 2013 installé sur les serveurs principaux.</span><span class="sxs-lookup"><span data-stu-id="fb9e7-152">In the preceding example, the value for IMCertificateThumbprint must be the thumbprint for the Exchange 2013 certificate that is installed on your backend servers.</span></span> <span data-ttu-id="fb9e7-153">Vous pouvez récupérer ces informations en exécutant la commande suivante à partir d’Exchange Management Shell :</span><span class="sxs-lookup"><span data-stu-id="fb9e7-153">You can retrieve that information by running the following command from the Exchange Management Shell:</span></span>

    Get-ExchangeCertificate

<span data-ttu-id="fb9e7-154">Notez également que la valeur affectée à inservername est le nom de domaine complet du pool de serveurs Lync dans lequel vous avez créé le pool d’applications approuvé pour Outlook Web App.</span><span class="sxs-lookup"><span data-stu-id="fb9e7-154">Note, too that the value assigned to IMServerName is the fully qualified domain name of the Lync Server pool where you created the trusted application pool for Outlook Web App.</span></span>

<span data-ttu-id="fb9e7-155">Le certificat que vous utilisez pour Outlook Web App doit être un certificat approuvé par Lync Server.</span><span class="sxs-lookup"><span data-stu-id="fb9e7-155">The certificate that you use for Outlook Web App must be a certificate that is trusted by Lync Server.</span></span> <span data-ttu-id="fb9e7-156">Pour vous assurer que le certificat sera approuvé par Lync Server et qu’Exchange consiste à utiliser votre autorité de certification interne pour créer un certificat sur le serveur de boîte aux lettres, assurez-vous que le nom de domaine complet du serveur est utilisé pour le nom du sujet et que ce nom de domaine complet apparaît dans le champ nom du sujet du certificat.</span><span class="sxs-lookup"><span data-stu-id="fb9e7-156">One way to ensure that the certificate will be trusted by both Lync Server and Exchange is to use your internal certificate authority to create a certificate on the mailbox server, making sure that the server FQDN is used for the subject name and that this FQDN appears in the certificate alternate name field.</span></span> <span data-ttu-id="fb9e7-157">Une fois créé, le certificat peut être importé vers les serveurs principaux.</span><span class="sxs-lookup"><span data-stu-id="fb9e7-157">After the certificate has been created it can then be imported to your backend servers.</span></span> <span data-ttu-id="fb9e7-158">Le résultat net est que le même certificat est utilisé pour deux raisons : 1) communication entre la messagerie unifiée Exchange et Lync Server. et 2) intégration d’Outlook Web App et de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="fb9e7-158">The net result is that the same certificate is used for two purposes: 1) communication between Exchange unified messaging and Lync Server; and, 2) the integration between Outlook Web App and Lync Server.</span></span>

<span data-ttu-id="fb9e7-159">Après avoir mis à jour le fichier Web.config, exécutez la commande suivante sur le serveur principal Exchange pour recycler le pool Outlook Web App :</span><span class="sxs-lookup"><span data-stu-id="fb9e7-159">After you have updated the Web.config file you should then run the following command on the Exchange backend server in order to recycle the Outlook Web App pool:</span></span>

    C:\Windows\System32\Inetsrv\Appcmd.exe recycle apppool /apppool.name:"MSExchangeOWAAppPool"

<span data-ttu-id="fb9e7-160">Le message suivant s’affiche dans Exchange Management Shell lorsque le recyclage réussit :</span><span class="sxs-lookup"><span data-stu-id="fb9e7-160">If the recycle operation succeeds you will see the following message in the Exchange Management Shell:</span></span>

    "MSExchangeOWAAppPool" successfully recycled

<span data-ttu-id="fb9e7-161">**Configuration des stratégies de boîte aux lettres Outlook Web App**</span><span class="sxs-lookup"><span data-stu-id="fb9e7-161">**Configuring Outlook Web App Mailbox Policies**</span></span>

<span data-ttu-id="fb9e7-p117">À ce stade, vous pouvez utiliser la commande suivante afin de configurer la messagerie instantanée pour la ou les stratégies de boîte aux lettres Outlook Web App appropriées. Par exemple, cette commande, exécutée sur l’un de vos serveurs de boîtes aux lettres, active la messagerie instantanée pour la stratégie par défaut :</span><span class="sxs-lookup"><span data-stu-id="fb9e7-p117">At this point you can use the following command to configure instant messaging on the appropriate Outlook Web App mailbox policy (or policies). For example, this command, run on one of your mailbox servers, enables instant messaging on the Default policy:</span></span>

    Set-OwaMailboxPolicy -Identity "Default" -InstantMessagingEnabled $True -InstantMessagingType "OCS"

<span data-ttu-id="fb9e7-164">Quant à cette commande, elle active la messagerie instantanée pour toutes vos stratégies de boîte aux lettres Outlook Web App :</span><span class="sxs-lookup"><span data-stu-id="fb9e7-164">And this command enables instant messaging for all your Outlook Web App mailbox policies:</span></span>

    Get-OwaMailboxPolicy | Set-OwaMailboxPolicy -InstantMessagingEnabled $True -InstantMessagingType "OCS"

<span data-ttu-id="fb9e7-165">Après l’activation de la stratégie de boîte aux lettres, tous les utilisateurs gérés par cette stratégie disposeront d’une intégration complète entre Lync Server et Outlook Web App, à condition que :</span><span class="sxs-lookup"><span data-stu-id="fb9e7-165">After the mailbox policy has been enabled then all users managed by that policy will have full integration between Lync Server and Outlook Web App, provided that:</span></span>

  - <span data-ttu-id="fb9e7-166">L’utilisateur dispose d’une boîte aux lettres sur Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="fb9e7-166">The user has a mailbox on Exchange 2013.</span></span>

  - <span data-ttu-id="fb9e7-167">L’utilisateur a été activé pour Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="fb9e7-167">The user has been enabled for Lync Server 2013.</span></span>

  - <span data-ttu-id="fb9e7-168">l’utilisateur possède une adresse proxy SIP valide.</span><span class="sxs-lookup"><span data-stu-id="fb9e7-168">The user has a valid SIP proxy address.</span></span>

<span data-ttu-id="fb9e7-169">**Désactivation de la messagerie instantanée dans Outlook Web App**</span><span class="sxs-lookup"><span data-stu-id="fb9e7-169">**Disabling Instant Messaging in Outlook Web App**</span></span>

<span data-ttu-id="fb9e7-170">Comme indiqué précédemment, la messagerie instantanée est activée par défaut dans Outlook Web App.</span><span class="sxs-lookup"><span data-stu-id="fb9e7-170">As noted previously, instant messaging is enabled by default in Outlook Web App.</span></span> <span data-ttu-id="fb9e7-171">Cela signifie que si vous n’intégrez pas Outlook Web App à Lync Server, les utilisateurs verront les icônes de présence vides et un message d’erreur chaque fois qu’ils se connecteront à Outlook Web App.</span><span class="sxs-lookup"><span data-stu-id="fb9e7-171">That means that, if you do not integrate Outlook Web App with Lync Server, users will see blank presence icons and an error message each time they log on to Outlook Web App.</span></span> <span data-ttu-id="fb9e7-172">Pour éviter ce problème, utilisez la commande Exchange Management Shell suivante pour désactiver la messagerie instantanée dans Outlook Web App :</span><span class="sxs-lookup"><span data-stu-id="fb9e7-172">To prevent this problem, use the following Exchange Management Shell command to disable instant messaging in Outlook web App:</span></span>

    Get-OwaVirtualDirectory | Set-OwaVirtualDirectory -InstantMessagingEnabled $False

<span data-ttu-id="fb9e7-173">**Vérification de l’intégration à Outlook Web App**</span><span class="sxs-lookup"><span data-stu-id="fb9e7-173">**Verifying Integration With Outlook Web App**</span></span>

<span data-ttu-id="fb9e7-174">Pour vérifier si les fonctionnalités de messagerie instantanée et de présence ont été intégrées dans Outlook Web App, authentifiez-vous dans Outlook Web App 2013.</span><span class="sxs-lookup"><span data-stu-id="fb9e7-174">To verify that instant messaging and presence have been integrated with Outlook Web App, sign on to Outlook Web App 2013.</span></span> <span data-ttu-id="fb9e7-175">Dans le coin supérieur droit de l’écran, vous voyez votre nom d’affichage Exchange.</span><span class="sxs-lookup"><span data-stu-id="fb9e7-175">In the upper right-hand corner of the screen, you will see your Exchange display name.</span></span> <span data-ttu-id="fb9e7-176">S’il existe une icône de présence en regard de votre nom (par exemple, une icône verte indiquant que votre statut actuel est disponible) indiquant que vous avez correctement intégré Lync Server et Outlook Web App.</span><span class="sxs-lookup"><span data-stu-id="fb9e7-176">If there is a presence icon next to your name (for example, a green icon indicating that your current status is Available) that indicates that you have successfully integrated Lync Server and Outlook Web App.</span></span>

<span data-ttu-id="fb9e7-177">Après vous être authentifié dans Outlook Web App, vérifiez si un événement portant l’ID d’événement 112 (et la source MSExchange OWA) a été écrit dans le journal des événements sur le serveur de boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="fb9e7-177">After the initial sign-on to Outlook Web App, check to see if an event with the Event ID 112 (and the source MSExchange OWA) has been written to the event log on the mailbox server.</span></span> <span data-ttu-id="fb9e7-178">Cet événement indique que le gestionnaire de points de terminaison de la messagerie instantanée a été correctement initialisé.</span><span class="sxs-lookup"><span data-stu-id="fb9e7-178">This event indicates that the Instant Messaging Endpoint Manager was successfully initialized.</span></span> <span data-ttu-id="fb9e7-179">Si la messagerie instantanée ne semble pas fonctionner, sur le serveur de boîte aux lettres, recherchez les fichiers journaux dans le dossier C : \\ Program Files \\ Microsoft \\ Exchange Server \\ v15 \\ journalisation d' \\ owa \\ instantmessaging.</span><span class="sxs-lookup"><span data-stu-id="fb9e7-179">If instant messaging does not appear to be working then, on the mailbox server, look for log files in the folder C:\\Program Files\\Microsoft\\Exchange server\\V15\\Logging\\OWA\\InstantMessaging.</span></span> <span data-ttu-id="fb9e7-180">Si le dossier Logging ou InstantMessaging n’existe pas, cela indique que l’intégration a échoué.</span><span class="sxs-lookup"><span data-stu-id="fb9e7-180">If either the Logging or the InstantMessaging folders do not exist that indicates that integration has failed.</span></span> <span data-ttu-id="fb9e7-181">Dans ce cas, vous pouvez utiliser le suivi SIPStack sur Lync Server (tous les niveaux et tous les indicateurs) pour essayer de déterminer l’échec de l’intégration.</span><span class="sxs-lookup"><span data-stu-id="fb9e7-181">In that case, you can use SIPStack tracing on Lync Server (All Levels and All Flags) to try and determine why integration failed.</span></span>

<span data-ttu-id="fb9e7-182"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fb9e7-182"></div>

<span> </span>

</div>

</div>

</span></span></div>

