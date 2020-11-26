---
title: 'Lync Server 2013 : migration des utilisateurs Lync Online vers Lync local'
description: 'Lync Server 2013 : migration des utilisateurs Lync Online vers Lync local.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Migrating Lync Online users to Lync on-premises
ms:assetid: 0e29605b-db2d-4cbf-b6a9-15db6b9fdabc
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn689115(v=OCS.15)
ms:contentKeyID: 62258120
ms.date: 11/13/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 620bc07def8e3c1f6b761c6398b452b4dbcd3b04
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445980"
---
# <a name="migrating-lync-online-users-to-lync-on-premises-in-lync-server-2013"></a><span data-ttu-id="d2437-103">Migration des utilisateurs Lync Online vers Lync local dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d2437-103">Migrating Lync Online users to Lync on-premises in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d2437-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d2437-104">

<span> </span></span></span>

<span data-ttu-id="d2437-105">_**Dernière modification de la rubrique :** 2015-11-13_</span><span class="sxs-lookup"><span data-stu-id="d2437-105">_**Topic Last Modified:** 2015-11-13_</span></span>

<div class="">


> [!IMPORTANT]  
> <span data-ttu-id="d2437-106">Ces étapes sont nécessaires uniquement pour la migration des comptes d’utilisateurs qui ont été activés pour Lync dans Lync Online avant de déployer Lync en local.</span><span class="sxs-lookup"><span data-stu-id="d2437-106">These steps are necessary only for migrating user accounts that were originally enabled for Lync in Lync Online, before you deployed Lync on-premises.</span></span> <span data-ttu-id="d2437-107">Pour déplacer des utilisateurs qui ont été activés pour Lync local, puis transférés plus tard vers Lync Online, voir <A href="lync-server-2013-administering-users-in-a-hybrid-deployment.md">administration des utilisateurs dans un déploiement 2013 Lync Server</A>.</span><span class="sxs-lookup"><span data-stu-id="d2437-107">To move users who were originally enabled for Lync on-premises, then later moved to Lync Online, see <A href="lync-server-2013-administering-users-in-a-hybrid-deployment.md">Administering users in a hybrid Lync Server 2013 deployment</A>.</span></span><BR><span data-ttu-id="d2437-108">De plus, tous les utilisateurs en cours de déplacement doivent disposer de comptes dans l’instance locale d’Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d2437-108">Additionally, all users being moved must have accounts in the on-premises Active Directory.</span></span>



</div>

<div>

## <a name="migrating-user-accounts-originally-enabled-in-lync-online-to-lync-on-premises"></a><span data-ttu-id="d2437-109">Migration des comptes d’utilisateurs activés dans Lync Online vers Lync local</span><span class="sxs-lookup"><span data-stu-id="d2437-109">Migrating User Accounts Originally Enabled in Lync Online to Lync On-Premises</span></span>

1.  <span data-ttu-id="d2437-110">Tout d’abord, assurez-vous que votre organisation est configurée pour l’environnement hybride.</span><span class="sxs-lookup"><span data-stu-id="d2437-110">First, make sure that your organization is configured for hybrid.</span></span>
    
      - <span data-ttu-id="d2437-111">Installez l’outil de synchronisation Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d2437-111">Install the Azure Active Directory Sync Tool.</span></span> <span data-ttu-id="d2437-112">Pour en savoir plus, consultez <https://social.technet.microsoft.com/wiki/contents/articles/19098.howto-install-the-windows-azure-active-directory-sync-tool.aspx>.</span><span class="sxs-lookup"><span data-stu-id="d2437-112">For more information, see <https://social.technet.microsoft.com/wiki/contents/articles/19098.howto-install-the-windows-azure-active-directory-sync-tool.aspx>.</span></span>
    
      - <span data-ttu-id="d2437-113">Pour permettre à vos utilisateurs d’utiliser l’authentification unique pour Lync Online, installez les services ADFS (Active Directory Federation Services) <https://social.technet.microsoft.com/wiki/contents/articles/1011.active-directory-federation-services-ad-fs-overview.aspx> .</span><span class="sxs-lookup"><span data-stu-id="d2437-113">To enable your users to use single sign-on for Lync Online, install Active Directory Federation Services <https://social.technet.microsoft.com/wiki/contents/articles/1011.active-directory-federation-services-ad-fs-overview.aspx>.</span></span>
    
      - <span data-ttu-id="d2437-114">Sur votre déploiement local, dans Lync Server Management Shell, entrez les applets de commande suivantes pour créer le fournisseur d’hébergement pour Lync Online :</span><span class="sxs-lookup"><span data-stu-id="d2437-114">On your on-premises deployment, in Lync Server Management Shell, type the following cmdlets to create the hosting provider for Lync Online:</span></span>
        
           ```PowerShell
           Set-CsAccessEdgeConfiguration -AllowOutsideUsers 1 -AllowFederatedUsers 1 -UseDnsSrvRouting -EnablePartnerDiscovery $true
           ```
        
           ```PowerShell
            New-CsHostingProvider -Identity LyncOnline -ProxyFqdn "sipfed.online.lync.com" -Enabled $true -EnabledSharedAddressSpace $true -HostsOCSUsers $true -VerificationLevel UseSourceVerification -IsLocal $false -AutodiscoverUrl https://webdir.online.lync.com/Autodiscover/AutodiscoverService.svc/root
           ```

2.  <span data-ttu-id="d2437-115">Vérifiez que, sur votre serveur Edge local, vous disposez de la chaîne de certificats qui permet de se connecter à Lync Online, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="d2437-115">Confirm that, on your on-premises Edge Servers, you have the certificate chain that enables connection to Lync Online, as shown in the following table.</span></span> <span data-ttu-id="d2437-116">Vous pouvez télécharger cette chaîne à l’adresse suivante : https://support.office.com/article/office-365-certificate-chains-0c03e6b3-e73f-4316-9e2b-bf4091ae96bb</span><span class="sxs-lookup"><span data-stu-id="d2437-116">You can download this chain here: https://support.office.com/article/office-365-certificate-chains-0c03e6b3-e73f-4316-9e2b-bf4091ae96bb</span></span>


    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="d2437-117">Certificat</span><span class="sxs-lookup"><span data-stu-id="d2437-117">Certificate</span></span></th>
    <th><span data-ttu-id="d2437-118">Magasin de certificats</span><span class="sxs-lookup"><span data-stu-id="d2437-118">Certificate Store</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="d2437-119">Certificat racine de CyberTrust Baltimore</span><span class="sxs-lookup"><span data-stu-id="d2437-119">Baltimore CyberTrust Root</span></span></p></td>
    <td><p><span data-ttu-id="d2437-120">Autorité de certification racine de confiance</span><span class="sxs-lookup"><span data-stu-id="d2437-120">Trusted Root CA</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="d2437-121">Microsoft Internet Authority (Nouveau certificat de l’autorité de certification racine)</span><span class="sxs-lookup"><span data-stu-id="d2437-121">Microsoft Internet Authority (New CA certificate)</span></span></p></td>
    <td><p><span data-ttu-id="d2437-122">Autorité de certification intermédiaire</span><span class="sxs-lookup"><span data-stu-id="d2437-122">Intermediate CA</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="d2437-123">MSIT Machine Auth CA2 (Nouvelle autorité de certification émettrice CA2)</span><span class="sxs-lookup"><span data-stu-id="d2437-123">MSIT Machine Auth CA2 (New Issuing CA2)</span></span></p></td>
    <td><p><span data-ttu-id="d2437-124">Autorité de certification intermédiaire</span><span class="sxs-lookup"><span data-stu-id="d2437-124">Intermediate CA</span></span></p></td>
    </tr>
    </tbody>
    </table>

3.  <span data-ttu-id="d2437-125">Dans votre Active Directory local, activez les comptes d’utilisateurs concernés pour Lync local.</span><span class="sxs-lookup"><span data-stu-id="d2437-125">In your on-premises Active Directory, enable the affected user accounts for Lync on-premises.</span></span> <span data-ttu-id="d2437-126">Pour un utilisateur individuel, tapez l’applet de commande suivante :</span><span class="sxs-lookup"><span data-stu-id="d2437-126">You can do this for an individual user by typing the following cmdlet:</span></span>
    
        Enable-CsUser
        -Identity "username" 
        -SipAddress "sip: username@contoso.com"
        -HostingProviderProxyFqdn "sipfed.online.lync.com"
    
    <span data-ttu-id="d2437-127">Vous pouvez également créer un script qui lit les noms d’utilisateur dans un fichier et les transmet comme informations à l’applet de commande Enable-CsUser :</span><span class="sxs-lookup"><span data-stu-id="d2437-127">Or you can create a script that reads user names from a file and provides them as input to the Enable-CsUser cmdlet:</span></span>
    
        Enable-CsUser
        -Identity $Identity 
        -SipAddress $SipAddress 
        -HostingProviderProxyFqdn "sipfed.online.lync.com"

4.  <span data-ttu-id="d2437-128">Exécutez DirSync pour synchroniser les utilisateurs Lync Online avec les utilisateurs Lync locaux mis à jour.</span><span class="sxs-lookup"><span data-stu-id="d2437-128">Run DirSync to sync the Lync Online users with the updated Lync on-premises users.</span></span>

5.  <span data-ttu-id="d2437-129">Mettez à jour les enregistrements DNS pour acheminer l’ensemble du trafic SIP vers Lync local :</span><span class="sxs-lookup"><span data-stu-id="d2437-129">Update some DNS records to direct all SIP traffic to Lync on-premises:</span></span>
    
      - <span data-ttu-id="d2437-130">Mettez à jour **lyncdiscover.contoso.com**  Un enregistrement pour pointer vers le nom de domaine complet (FQDN) du serveur proxy inverse local.</span><span class="sxs-lookup"><span data-stu-id="d2437-130">Update the **lyncdiscover.contoso.com** A record to point to the FQDN of the on-premises reverse proxy server.</span></span>
    
      - <span data-ttu-id="d2437-131">Mettez à jour le **_\_ SIP_. \_ tls.contoso.com** SRV enregistrement pour la résolution vers l’adresse IP ou VIP publique du service Edge d’accès de Lync local.</span><span class="sxs-lookup"><span data-stu-id="d2437-131">Update the **_\_sip_.\_tls.contoso.com** SRV record to resolve to the public IP or VIP address of the Access Edge service of Lync on-premises.</span></span>
    
      - <span data-ttu-id="d2437-132">Mettez à jour l' **_\_ sipfederationtls_. \_ tcp.contoso.com** SRV enregistrement pour la résolution vers l’adresse IP ou VIP publique du service Edge d’accès de Lync local.</span><span class="sxs-lookup"><span data-stu-id="d2437-132">Update the **_\_sipfederationtls_.\_tcp.contoso.com** SRV record to resolve to the public IP or VIP address of the Access Edge service of Lync on-premises.</span></span>
    
      - <span data-ttu-id="d2437-133">Si votre organisation utilise un « DNS split » (également appelé « DNS split-brain »), vérifiez que les utilisateurs qui résolvent des noms par le biais de la zone DNS interne sont dirigés vers le pool frontal.</span><span class="sxs-lookup"><span data-stu-id="d2437-133">If your organization uses split DNS (sometimes called “split-brain DNS”), make sure that users resolving names through the internal DNS zone are directed to the Front End Pool.</span></span>

6.  <span data-ttu-id="d2437-134">Tapez l' `Get-CsUser` applet de recherche pour vérifier certaines propriétés des utilisateurs que vous allez déplacer.</span><span class="sxs-lookup"><span data-stu-id="d2437-134">Type the `Get-CsUser` cmdlet to check some properties about the users you’ll be moving.</span></span> <span data-ttu-id="d2437-135">Vous voulez vous assurer que HostingProviderProxyFQDN est défini sur `"sipfed.online.lync.com"` et que les adresses SIP sont correctement définies.</span><span class="sxs-lookup"><span data-stu-id="d2437-135">You want to make sure that the HostingProviderProxyFQDN is set to `"sipfed.online.lync.com"` and that the SIP addresses are set correctly.</span></span>

7.  <span data-ttu-id="d2437-136">Déplacez les utilisateurs Lync Online vers Lync local.</span><span class="sxs-lookup"><span data-stu-id="d2437-136">Move Lync Online users to Lync on-premises.</span></span>
    
    <span data-ttu-id="d2437-137">Pour déplacer un seul utilisateur, tapez ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="d2437-137">To move a single user, type this:</span></span>
    
       ```PowerShell
       $cred = Get-Credential
       ```
    
       ```PowerShell
       Move-CsUser -Identity <username>@contoso.com -Target "<fe-pool>.contoso.com" -Credential $cred -HostedMigrationOverrideURL <URL>
       ```
    
    <span data-ttu-id="d2437-138">Vous pouvez déplacer plusieurs utilisateurs à l’aide de l’applet de commande **Get-CsUSer**  avec le paramètre –Filter pour sélectionner les utilisateurs comportant une propriété spécifique.</span><span class="sxs-lookup"><span data-stu-id="d2437-138">You can move multiple users by using the **Get-CsUSer** cmdlet with the –Filter parameter to select the users with a specific property.</span></span> <span data-ttu-id="d2437-139">Par exemple, vous pouvez sélectionner tous les utilisateurs de Lync Online en filtrant pour {Hosting Provider-EQ "sipfed.online.lync.om"}.</span><span class="sxs-lookup"><span data-stu-id="d2437-139">For example, you could select all Lync Online users by filtering for {Hosting Provider –eq “sipfed.online.lync.om”}.</span></span> <span data-ttu-id="d2437-140">Vous pouvez ensuite rediriger les utilisateurs renvoyés vers l’applet de commande **Move-CsUSer**, comme indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="d2437-140">You can then pipe the returned users to the **Move-CsUSer** cmdlet, as shown below.</span></span>
    
        Get-CsUser -Filter {Hosting Provider -eq "sipfed.online.lync.com"} | Move-CsUser -Target "<fe-pool>.contoso.com" -Credential $creds -HostedMigrationOverrideURL <URL>
    
    <span data-ttu-id="d2437-141">Le format de l’URL spécifiée pour le paramètre **hostedmigrationoverrideurl doit correspondre** doit être l’URL du pool sur lequel le service de migration hébergé est en cours d’exécution, au format suivant : *https:// \<Pool FQDN\> /HostedMigration/hostedmigrationService.svc*.</span><span class="sxs-lookup"><span data-stu-id="d2437-141">The format of the URL specified for the **HostedMigrationOverrideUrl** parameter must be the URL to the pool where the Hosted Migration service is running, in the following format: *Https://\<Pool FQDN\>/HostedMigration/hostedmigrationService.svc*.</span></span>
    
    <span data-ttu-id="d2437-142">Vous pouvez déterminer l’URL du service de migration hébergée en affichant l’URL du panneau de configuration Lync Online correspondant à votre compte Microsoft 365 ou de votre organisation Office 365.</span><span class="sxs-lookup"><span data-stu-id="d2437-142">You can determine the URL to the Hosted Migration Service by viewing the URL for the Lync Online Control Panel for your Microsoft 365 or Office 365 organization account.</span></span>
    
    <div>
    
    ## <a name="to-determine-the-hosted-migration-service-url-for-your-organizaton"></a><span data-ttu-id="d2437-143">Pour déterminer l’URL du service de migration hébergée pour votre organisation</span><span class="sxs-lookup"><span data-stu-id="d2437-143">To determine the Hosted Migration Service URL for your organizaton</span></span>
    
    1.  <span data-ttu-id="d2437-144">Connectez-vous à votre organisation Microsoft 365 ou Office 365 en tant qu’administrateur.</span><span class="sxs-lookup"><span data-stu-id="d2437-144">Log in to your Microsoft 365 or Office 365 organization as an administrator.</span></span>
    
    2.  <span data-ttu-id="d2437-145">Ouvrez le **Centre d’administration Lync**.</span><span class="sxs-lookup"><span data-stu-id="d2437-145">Open the **Lync admin center**.</span></span>
    
    3.  <span data-ttu-id="d2437-146">Avec le **Centre d’administration Lync** affiché, sélectionnez et copiez l’URL dans la barre d’adresses jusqu’à **Lync.com**.</span><span class="sxs-lookup"><span data-stu-id="d2437-146">With the **Lync admin center** displayed, select and copy the URL in the address bar up to **lync.com**.</span></span> <span data-ttu-id="d2437-147">L’URL doit se présenter comme dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="d2437-147">An example URL looks similar to the following:</span></span>
        
        `https://webdir0a.online.lync.com/lscp/?language=en-US&tenantID=`
    
    4.  <span data-ttu-id="d2437-148">Dans l’URL, remplacez **webdir** par **admin** pour obtenir le résultat suivant :</span><span class="sxs-lookup"><span data-stu-id="d2437-148">Replace **webdir** in the URL with **admin**, resulting in the following:</span></span>
        
        `https://admin0a.online.lync.com`
    
    5.  <span data-ttu-id="d2437-149">Ajoutez la chaîne ci-dessous à l’URL : **/HostedMigration/hostedmigrationservice.svc**.</span><span class="sxs-lookup"><span data-stu-id="d2437-149">Append the following string to the URL: **/HostedMigration/hostedmigrationservice.svc**.</span></span>
        
        <span data-ttu-id="d2437-150">L’URL obtenue, qui est la valeur de **HostedMigrationOverrideUrl**, doit se présenter comme suit :</span><span class="sxs-lookup"><span data-stu-id="d2437-150">The resulting URL, which is the value of the **HostedMigrationOverrideUrl**, should look like the following:</span></span>
        
        `https://admin0a.online.lync.com/HostedMigration/hostedmigrationservice.svc`
    
    </div>
    
    <div class="">
    

    > [!NOTE]  
    > <span data-ttu-id="d2437-151">La taille maximale par défaut pour les fichiers journaux de transaction de la base de données rtcxds est de 16 Go.</span><span class="sxs-lookup"><span data-stu-id="d2437-151">The default maximum size for transaction log files of the rtcxds database is 16 GB.</span></span> <span data-ttu-id="d2437-152">Cette taille peut être insuffisante si vous déplacez simultanément un grand nombre d’utilisateurs, notamment si la mise en miroir est activée.</span><span class="sxs-lookup"><span data-stu-id="d2437-152">This might not be big enough if you’re moving a large number of users at once, especially if you have mirroring enabled.</span></span> <span data-ttu-id="d2437-153">Pour résoudre ce problème, vous pouvez augmenter la taille du fichier ou sauvegarder régulièrement les fichiers journaux.</span><span class="sxs-lookup"><span data-stu-id="d2437-153">To get around this you can increase the file size or back up the log files regularly.</span></span> <span data-ttu-id="d2437-154">Pour en savoir plus, consultez <A class=uri href="https://support.microsoft.com/kb/2756725">https://support.microsoft.com/kb/2756725</A>.</span><span class="sxs-lookup"><span data-stu-id="d2437-154">For more information, see <A class=uri href="https://support.microsoft.com/kb/2756725">https://support.microsoft.com/kb/2756725</A>.</span></span>

    
    </div>

8.  <span data-ttu-id="d2437-155">Il s’agit d’une étape facultative.</span><span class="sxs-lookup"><span data-stu-id="d2437-155">This is an optional step.</span></span> <span data-ttu-id="d2437-156">Pour une intégration à Exchange 2013 Online, vous devez utiliser un autre fournisseur d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="d2437-156">If you need to integrate with Exchange 2013 Online, you need to use an additional hosting provider.</span></span> <span data-ttu-id="d2437-157">Pour plus d’informations, reportez-vous à la rubrique [configuration d’une intégration de Lync Server 2013 en local avec Exchange Online](lync-server-2013-configuring-on-premises-lync-server-integration-with-exchange-online.md).</span><span class="sxs-lookup"><span data-stu-id="d2437-157">For details, see [Configuring on-premises Lync Server 2013 integration with Exchange Online](lync-server-2013-configuring-on-premises-lync-server-integration-with-exchange-online.md).</span></span>

9.  <span data-ttu-id="d2437-p110">Les utilisateurs sont maintenant déplacés. Pour vérifier qu’un utilisateur possède des valeurs correctes pour les attributs affichés dans le tableau ci-dessous, tapez cette applet de commande :</span><span class="sxs-lookup"><span data-stu-id="d2437-p110">The users are now moved. To check that a user has correct values for the attributes shown in the following table, type this cmdlet:</span></span>
    
        Get-CsUser | fl DisplayName,HostingProvider,SipAddress,Enabled
    
    
    <table>
    <colgroup>
    <col style="width: 25%" />
    <col style="width: 25%" />
    <col style="width: 25%" />
    <col style="width: 25%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="d2437-160">Attribut Active Directory</span><span class="sxs-lookup"><span data-stu-id="d2437-160">Active Directory attribute</span></span></th>
    <th><span data-ttu-id="d2437-161">Nom Attribut</span><span class="sxs-lookup"><span data-stu-id="d2437-161">Attribute name</span></span></th>
    <th><span data-ttu-id="d2437-162">Valeur correcte pour l’utilisateur de Lync Online</span><span class="sxs-lookup"><span data-stu-id="d2437-162">Correct value for Lync Online user</span></span></th>
    <th><span data-ttu-id="d2437-163">Valeur correcte pour les utilisateurs Lync local</span><span class="sxs-lookup"><span data-stu-id="d2437-163">Correct value for Lync on–premises users</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="d2437-164">msRTCSIP-DeploymentLocator</span><span class="sxs-lookup"><span data-stu-id="d2437-164">msRTCSIP-DeploymentLocator</span></span></p></td>
    <td><p><span data-ttu-id="d2437-165">HostingProvider</span><span class="sxs-lookup"><span data-stu-id="d2437-165">HostingProvider</span></span></p></td>
    <td><p><span data-ttu-id="d2437-166">sipfed.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="d2437-166">sipfed.online.lync.com</span></span></p></td>
    <td><p><span data-ttu-id="d2437-167">SRV :</span><span class="sxs-lookup"><span data-stu-id="d2437-167">SRV:</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="d2437-168">msRTCSIP-PrimaryUserAddress</span><span class="sxs-lookup"><span data-stu-id="d2437-168">msRTCSIP-PrimaryUserAddress</span></span></p></td>
    <td><p><span data-ttu-id="d2437-169">SIPAddress</span><span class="sxs-lookup"><span data-stu-id="d2437-169">SIPAddress</span></span></p></td>
    <td><p><span data-ttu-id="d2437-170">sip:userName@contoso.com</span><span class="sxs-lookup"><span data-stu-id="d2437-170">sip:userName@contoso.com</span></span></p></td>
    <td><p><span data-ttu-id="d2437-171">sip:userName@contoso.com</span><span class="sxs-lookup"><span data-stu-id="d2437-171">sip:userName@contoso.com</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="d2437-172">msRTCSIP-UserEnabled</span><span class="sxs-lookup"><span data-stu-id="d2437-172">msRTCSIP-UserEnabled</span></span></p></td>
    <td><p><span data-ttu-id="d2437-173">Activé</span><span class="sxs-lookup"><span data-stu-id="d2437-173">Enabled</span></span></p></td>
    <td><p><span data-ttu-id="d2437-174">True</span><span class="sxs-lookup"><span data-stu-id="d2437-174">True</span></span></p></td>
    <td><p><span data-ttu-id="d2437-175">Vrai</span><span class="sxs-lookup"><span data-stu-id="d2437-175">True</span></span></p></td>
    </tr>
    </tbody>
    </table>


10. <span data-ttu-id="d2437-176">Chaque utilisateur déplacé aura besoin de se déconnecter de Lync, puis de vous reconnecter.</span><span class="sxs-lookup"><span data-stu-id="d2437-176">Each user who has been moved will need to log out of Lync, then log back in.</span></span> <span data-ttu-id="d2437-177">Lorsque l’utilisateur se reconnecte, il doit vérifier ses listes de contacts et ajouter des contacts, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="d2437-177">When they log in they should verify their contact lists, and add contacts if needed.</span></span>
    
    <span data-ttu-id="d2437-178">Notez que les réunions planifiées ne sont pas déplacées de Lync Online vers Lync local.</span><span class="sxs-lookup"><span data-stu-id="d2437-178">Note that scheduled meetings are not migrated from Lync Online to Lync on-premises.</span></span> <span data-ttu-id="d2437-179">Les utilisateurs doivent replanifier ces réunions après les avoir déplacées.</span><span class="sxs-lookup"><span data-stu-id="d2437-179">Users will need to reschedule these meetings after being moved.</span></span>
    
    <span data-ttu-id="d2437-180">Une fois que les enregistrements DNS sont mis à jour et que tous les utilisateurs sont dirigés vers le site, l’attribut HostingProvider indique à l’utilisateur de Lync d’utiliser des enregistrements SRV ou de le diriger vers le fournisseur en ligne « sipfed.online.lync.com ».</span><span class="sxs-lookup"><span data-stu-id="d2437-180">After the DNS records are updated and all users are directed to On premise, the HostingProvider attribute directs the Lync user to either use SRV records or direct them to the Online provider “sipfed.online.lync.com.”</span></span>

<span data-ttu-id="d2437-181"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d2437-181"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

