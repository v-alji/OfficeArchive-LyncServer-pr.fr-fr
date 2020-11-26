---
title: 'Lync Server 2013 : déploiement de Lync Web App'
description: 'Lync Server 2013 : déploiement de Lync Web App.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying Lync Web App
ms:assetid: b6301e98-051c-4e4b-8e10-ec922a8f508a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205190(v=OCS.15)
ms:contentKeyID: 48185189
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ce6fef02781afbd5bc5f315ce24bfb3bdb16df1c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429901"
---
# <a name="deploying-lync-web-app-in-lync-server-2013"></a><span data-ttu-id="39efd-103">Déploiement de Lync Web App dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="39efd-103">Deploying Lync Web App in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="39efd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="39efd-104">

<span> </span></span></span>

<span data-ttu-id="39efd-105">_**Dernière modification de la rubrique :** 2013-07-18_</span><span class="sxs-lookup"><span data-stu-id="39efd-105">_**Topic Last Modified:** 2013-07-18_</span></span>

<span data-ttu-id="39efd-106">Lync Web App est un client Web Internet Information Services (IIS) qui s’installe avec Lync Server 2013 et est activé par défaut.</span><span class="sxs-lookup"><span data-stu-id="39efd-106">Lync Web App is an Internet Information Services (IIS) web client that installs with Lync Server 2013 and is enabled by default.</span></span> <span data-ttu-id="39efd-107">Aucune étape supplémentaire n’est nécessaire pour activer Lync Web App sur le serveur ou déployer le client Web auprès des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="39efd-107">No additional steps are necessary to either enable Lync Web App on the server or deploy the web client to users.</span></span> <span data-ttu-id="39efd-108">Dès qu’un utilisateur clique sur l’URL d’une réunion, mais que le client 2013 Lync n’est pas installé, l’utilisateur est invité à rejoindre la réunion à l’aide de la version la plus récente de Lync Web App.</span><span class="sxs-lookup"><span data-stu-id="39efd-108">Whenever a user clicks a meeting URL but does not have the Lync 2013 client installed, the user is presented with the option to join the meeting by using the latest version of Lync Web App.</span></span>

<span data-ttu-id="39efd-109">Les fonctionnalités de voix, de vidéo et de partage dans Lync Web App requièrent un contrôle Microsoft ActiveX.</span><span class="sxs-lookup"><span data-stu-id="39efd-109">The voice, video, and sharing features in Lync Web App require a Microsoft ActiveX control.</span></span> <span data-ttu-id="39efd-110">Lorsque vous y êtes invité, vous pouvez installer le contrôle ActiveX à l’avance ou permettre aux utilisateurs de l’installer lorsque la première fois qu’ils utilisent Lync Web App ou la première fois qu’ils ont accès à une fonctionnalité qui nécessite le contrôle ActiveX.</span><span class="sxs-lookup"><span data-stu-id="39efd-110">You can either install the ActiveX control in advance or allow users to install it when prompted, which happens the first time they use Lync Web App or the first time they access a feature that requires the ActiveX control.</span></span>

<div class=" ">


> [!NOTE]  
> <span data-ttu-id="39efd-111">Dans les déploiements de serveur Edge Lync Server 2013, un proxy HTTPs inverse dans le réseau de périmètre est requis pour l’accès au client Lync Web App.</span><span class="sxs-lookup"><span data-stu-id="39efd-111">In Lync Server 2013 Edge Server deployments, an HTTPS reverse proxy in the perimeter network is required for Lync Web App client access.</span></span> <span data-ttu-id="39efd-112">Vous devez également publier des URL simples.</span><span class="sxs-lookup"><span data-stu-id="39efd-112">You must also publish simple URLs.</span></span> <span data-ttu-id="39efd-113">Pour plus d’informations, reportez-vous à la rubrique <A href="lync-server-2013-setting-up-reverse-proxy-servers.md">configuration de serveurs proxy inverse pour Lync server 2013</A> et <A href="lync-server-2013-planning-for-simple-urls.md">planification d’URL simples dans Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="39efd-113">For details, see <A href="lync-server-2013-setting-up-reverse-proxy-servers.md">Setting up reverse proxy servers for Lync Server 2013</A> and <A href="lync-server-2013-planning-for-simple-urls.md">Planning for simple URLs in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="enabling-multi-factor-authentication-for-lync-web-app"></a><span data-ttu-id="39efd-114">Activation de l’authentification multifacteur pour Lync Web App</span><span class="sxs-lookup"><span data-stu-id="39efd-114">Enabling Multi-Factor Authentication for Lync Web App</span></span>

<span data-ttu-id="39efd-115">La version 2013 de Lync Server de Lync Web App prend en charge l’authentification multifacteur.</span><span class="sxs-lookup"><span data-stu-id="39efd-115">The Lync Server 2013 version of Lync Web App supports multi-factor authentication.</span></span> <span data-ttu-id="39efd-116">Outre le nom d’utilisateur et le mot de passe, vous pouvez demander des méthodes d’authentification supplémentaires, telles que des cartes à puce ou des épingles, afin d’authentifier les utilisateurs qui se connectent à partir de réseaux externes lors de leur connexion aux réunions Lync.</span><span class="sxs-lookup"><span data-stu-id="39efd-116">In addition to user name and password, you can require additional authentication methods, such as smart cards or PINs, to authenticate users who are joining from external networks when they sign in to Lync meetings.</span></span> <span data-ttu-id="39efd-117">Vous pouvez activer l’authentification multifacteur via le déploiement du serveur de fédération AD FS (Active Directory Federation Services) et l’activation de l’authentification passive dans Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="39efd-117">You can enable multi-factor authentication by deploying Active Directory Federation Service (AD FS) federation server and enabling passive authentication in Lync Server 2013.</span></span> <span data-ttu-id="39efd-118">Après la configuration d’AD FS, les utilisateurs externes qui essaient de participer à des réunions Lync sont dotés d’une page Web d’authentification multifacteur AD FS contenant le nom d’utilisateur et le mot de passe, ainsi que d’autres méthodes d’authentification que vous avez configurées.</span><span class="sxs-lookup"><span data-stu-id="39efd-118">After AD FS is configured, external users who attempt to join Lync meetings are presented with an AD FS multi-factor authentication webpage that contains the user name and password challenge along with any additional authentication methods that you have configured.</span></span>

<div class=" ">


> [!IMPORTANT]  
> <span data-ttu-id="39efd-119">Vous trouverez ci-dessous des considérations importantes si vous envisagez de configurer les services AD FS pour l’authentification multifacteur :</span><span class="sxs-lookup"><span data-stu-id="39efd-119">The following are important considerations if you plan to configure AD FS for multi-factor authentication:</span></span> 
> <UL>
> <LI>
> <P><span data-ttu-id="39efd-p105">L'authentification ADFS multifacteur fonctionne si le participant à la réunion et l'organisateur appartiennent à la même organisation ou à une organisation fédérée AD FS. Elle ne fonctionne pas pour les utilisateurs fédérés Lync, car l’infrastructure web du serveur Lync ne la prend pas en charge pour le moment.</span><span class="sxs-lookup"><span data-stu-id="39efd-p105">Multi-factor ADFS authentication works if the meeting participant and organizer are both in the same organization or are both from an AD FS federated organization. Multi-factor ADFS authentication does not work for Lync federated users because the Lync server web infrastructure does not currently support it.</span></span></P>
> <LI>
> <P><span data-ttu-id="39efd-122">Si vous utilisez des équilibreurs de charge matérielle, activez la persistance des cookies sur les équilibreurs de charge de sorte que toutes les requêtes du client Lync Web App soient gérées par le même serveur principal.</span><span class="sxs-lookup"><span data-stu-id="39efd-122">If you use hardware load balancers, enable cookie persistence on the load balancers so that all requests from the Lync Web App client are handled by the same Front End Server.</span></span></P>
> <LI>
> <P><span data-ttu-id="39efd-123">Lorsque vous établissez une relation d’approbation de la partie de confiance entre les serveurs Lync Server et AD FS, attribuez une durée de vie du jeton suffisamment longue pour couvrir la longueur maximale de vos réunions Lync.</span><span class="sxs-lookup"><span data-stu-id="39efd-123">When you establish a relying party trust between Lync Server and AD FS servers, assign a token life that is long enough to span the maximum length of your Lync meetings.</span></span> <span data-ttu-id="39efd-124">Une durée de vie de jeton de 240 minutes est généralement suffisante.</span><span class="sxs-lookup"><span data-stu-id="39efd-124">Typically, a token life of 240 minutes is sufficient.</span></span></P>
> <LI>
> <P><span data-ttu-id="39efd-125">Cette configuration ne s’applique pas aux clients mobiles Lync.</span><span class="sxs-lookup"><span data-stu-id="39efd-125">This configuration does not apply to Lync mobile clients.</span></span></P></LI></UL>



</div>

<span data-ttu-id="39efd-126">**Pour configurer l’authentification multifacteur**</span><span class="sxs-lookup"><span data-stu-id="39efd-126">**To Configure Multi-Factor Authentication**</span></span>

1.  <span data-ttu-id="39efd-127">Installez un rôle de serveur de fédération AD FS.</span><span class="sxs-lookup"><span data-stu-id="39efd-127">Install an AD FS federation server role.</span></span> <span data-ttu-id="39efd-128">Pour plus d’informations, consultez le Guide de déploiement de services ADFS (Active Directory Federation Services) 2,0 à l’adresse <https://go.microsoft.com/fwlink/p/?linkid=267511></span><span class="sxs-lookup"><span data-stu-id="39efd-128">For details, see the Active Directory Federation Services 2.0 Deployment Guide at <https://go.microsoft.com/fwlink/p/?linkid=267511></span></span>

2.  <span data-ttu-id="39efd-129">Créez des certificats pour AD FS.</span><span class="sxs-lookup"><span data-stu-id="39efd-129">Create certificates for AD FS.</span></span> <span data-ttu-id="39efd-130">Pour plus d’informations, reportez-vous à la section « certificats de serveur de Fédération » de la rubrique plan pour et déployer AD FS pour une utilisation avec une connexion unique à l’adresse [https://go.microsoft.com/fwlink/p/?LinkId=285376](https://go.microsoft.com/fwlink/p/?linkid=285376) .</span><span class="sxs-lookup"><span data-stu-id="39efd-130">For more information, see the "Federation server certificates" section of the Plan for and deploy AD FS for use with single sign-on topic at [https://go.microsoft.com/fwlink/p/?LinkId=285376](https://go.microsoft.com/fwlink/p/?linkid=285376).</span></span>

3.  <span data-ttu-id="39efd-131">À partir de l’interface de ligne de commande Windows PowerShell, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="39efd-131">From the Windows PowerShell command-line interface, run the following command:</span></span>
    ```powershell
    add-pssnapin Microsoft.Adfs.powershell
    ```
4.  <span data-ttu-id="39efd-132">Établissez un partenariat en exécutant la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="39efd-132">Establish a partnership by running the following command:</span></span>
    ```powershell
    Add-ADFSRelyingPartyTrust -Name ContosoApp -MetadataURL https://lyncpool.contoso.com/passiveauth/federationmetadata/2007-06/federationmetadata.xml
     ```
5.  <span data-ttu-id="39efd-133">Définissez les règles de partie de confiance suivantes :</span><span class="sxs-lookup"><span data-stu-id="39efd-133">Set the following relying party rules:</span></span>
    
       ```powershell
        $IssuanceAuthorizationRules = '@RuleTemplate = "AllowAllAuthzRule" => issue(Type = "http://schemas.contoso.com/authorization/claims/permit", Value = "true");'
        $IssuanceTransformRules = '@RuleTemplate = "PassThroughClaims" @RuleName = "Sid" c:[Type == "http://schemas.contoso.com/ws/2008/06/identity/claims/primarysid"]=> issue(claim = c);'
       ```
    
       ```powershell
        Set-ADFSRelyingPartyTrust -TargetName ContosoApp -IssuanceAuthorizationRules $IssuanceAuthorizationRules -IssuanceTransformRules $IssuanceTransformRules
       ```
    
       ```powershell
        Set-CsWebServiceConfiguration -UseWsFedPassiveAuth $true -WsFedPassiveMetadataUri https://dc.contoso.com/federationmetadata/2007-06/federationmetadata.xml
       ```

</div>

<div>

## <a name="branchcache-configuration"></a><span data-ttu-id="39efd-134">Configuration de BranchCache</span><span class="sxs-lookup"><span data-stu-id="39efd-134">BranchCache Configuration</span></span>

<span data-ttu-id="39efd-135">La fonctionnalité BranchCache dans Windows 7 et Windows Server 2008 R2 peut interférer avec les composants Web de Lync Web App.</span><span class="sxs-lookup"><span data-stu-id="39efd-135">The BranchCache feature in Windows 7 and Windows Server 2008 R2 can interfere with Lync Web App web components.</span></span> <span data-ttu-id="39efd-136">Pour éviter les problèmes liés aux utilisateurs Lync Web App, assurez-vous que BranchCache n’est pas activé.</span><span class="sxs-lookup"><span data-stu-id="39efd-136">To prevent issues for Lync Web App users, make sure that BranchCache is not enabled.</span></span>

<span data-ttu-id="39efd-137">Pour plus d’informations sur la désactivation de BranchCache, voir le Guide de déploiement de BranchCache, qui est disponible au format Word au centre de téléchargement Microsoft au [https://go.microsoft.com/fwlink/p/?LinkId=268788](https://go.microsoft.com/fwlink/p/?linkid=268788) format HTML, dans la bibliothèque technique de Windows Server 2008 R2 [https://go.microsoft.com/fwlink/p/?LinkId=268789](https://go.microsoft.com/fwlink/p/?linkid=268789) .</span><span class="sxs-lookup"><span data-stu-id="39efd-137">For details about disabling BranchCache, see the BranchCache Deployment Guide, which is available in Word format at the Microsoft Download Center at [https://go.microsoft.com/fwlink/p/?LinkId=268788](https://go.microsoft.com/fwlink/p/?linkid=268788) and in HTML format in the Windows Server 2008 R2 Technical Library at [https://go.microsoft.com/fwlink/p/?LinkId=268789](https://go.microsoft.com/fwlink/p/?linkid=268789).</span></span>

</div>

<div>

## <a name="verifying-lync-web-app-deployment"></a><span data-ttu-id="39efd-138">Vérification du déploiement de Lync Web App</span><span class="sxs-lookup"><span data-stu-id="39efd-138">Verifying Lync Web App Deployment</span></span>

<span data-ttu-id="39efd-139">Vous pouvez utiliser l'applet de commande Test-CsUcwaConference pour vérifier que deux utilisateurs de test peuvent participer à une conférence à l'aide de l'API UCWA (Unified Communications Web API).</span><span class="sxs-lookup"><span data-stu-id="39efd-139">You can use the Test-CsUcwaConference cmdlet to verify that a pair of test users can participate in a conference using the Unified Communications Web API (UCWA).</span></span> <span data-ttu-id="39efd-140">Pour plus d’informations sur cette cmdlet, voir [test-CsUcwaConference](https://docs.microsoft.com/powershell/module/skype/Test-CsUcwaConference) dans la documentation Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="39efd-140">For details about this cmdlet, see [Test-CsUcwaConference](https://docs.microsoft.com/powershell/module/skype/Test-CsUcwaConference) in the Lync Server Management Shell documentation.</span></span>

</div>

<div>

## <a name="troubleshooting-plug-in-installation-on-windows-server-2008-r2"></a><span data-ttu-id="39efd-141">Résoudre les problèmes d’installation du plug-in sur Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="39efd-141">Troubleshooting Plug-in Installation on Windows Server 2008 R2</span></span>

<span data-ttu-id="39efd-142">Si l’installation du plug-in échoue sur un ordinateur exécutant Windows Server 2008 R2, vous devrez peut-être modifier le paramètre de sécurité Internet Explorer ou le paramètre de clé de Registre DisableMSI.</span><span class="sxs-lookup"><span data-stu-id="39efd-142">If installation of the plug-in fails on a computer running Windows Server 2008 R2, you may need to modify the Internet Explorer security setting or the DisableMSI registry key setting.</span></span>

<span data-ttu-id="39efd-143">**Pour modifier le paramètre de sécurité dans Internet Explorer**</span><span class="sxs-lookup"><span data-stu-id="39efd-143">**To modify the security setting in Internet Explorer**</span></span>

1.  <span data-ttu-id="39efd-144">Ouvrez Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="39efd-144">Open Internet Explorer.</span></span>

2.  <span data-ttu-id="39efd-145">Cliquez sur **Outils**, sur **Options Internet**, puis sur **Avancé**.</span><span class="sxs-lookup"><span data-stu-id="39efd-145">Click **Tools**, click **Internet Options**, and then click **Advanced**.</span></span>

3.  <span data-ttu-id="39efd-146">Faites défiler la page vers le bas jusqu'à la section **Sécurité**.</span><span class="sxs-lookup"><span data-stu-id="39efd-146">Scroll down to the **Security** section.</span></span>

4.  <span data-ttu-id="39efd-147">Désactivez la case à cocher **Ne pas enregistrer les pages chiffrées sur le disque**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="39efd-147">Clear **Do not save encrypted pages to disk**, and then click **OK**.</span></span>
    
    <div class=" ">
    

    > [!NOTE]  
    > <span data-ttu-id="39efd-148">Si cette option est sélectionnée, ce paramètre entraîne également une erreur lors de la tentative de téléchargement d’une pièce jointe à partir de Lync Web App.</span><span class="sxs-lookup"><span data-stu-id="39efd-148">If selected, this setting will also cause an error when trying to download an attachment from Lync Web App.</span></span>

    
    </div>

5.  <span data-ttu-id="39efd-149">Rejoignez la réunion.</span><span class="sxs-lookup"><span data-stu-id="39efd-149">Rejoin the meeting.</span></span> <span data-ttu-id="39efd-150">Le plug-in doit se télécharger sans erreurs.</span><span class="sxs-lookup"><span data-stu-id="39efd-150">The plug-in should download without errors.</span></span>

<span data-ttu-id="39efd-151">**Pour modifier le paramètre de Registre DisableMSI**</span><span class="sxs-lookup"><span data-stu-id="39efd-151">**To modify the DisableMSI Registry setting**</span></span>

1.  <span data-ttu-id="39efd-152">Cliquez sur **Démarrer**, puis sur **Exécuter**.</span><span class="sxs-lookup"><span data-stu-id="39efd-152">Click **Start**, and then click **Run**.</span></span>

2.  <span data-ttu-id="39efd-153">Pour accéder à l'Éditeur du registre, tapez **regedit**.</span><span class="sxs-lookup"><span data-stu-id="39efd-153">To access the Registry Editor, type **regedit**.</span></span>

3.  <span data-ttu-id="39efd-154">Naviguez jusqu’à HKEY stratégies de logiciels de l' \_ \_ ordinateur local \\ \\ \\ Microsoft \\ Windows \\ installer.</span><span class="sxs-lookup"><span data-stu-id="39efd-154">Navigate to HKEY\_LOCAL\_MACHINE\\Software\\Policies\\Microsoft\\Windows\\Installer.</span></span>

4.  <span data-ttu-id="39efd-155">Modifiez ou ajoutez la clé de Registre DisableMSI de type REG \_ DWORD et attribuez-lui la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="39efd-155">Edit or add the DisableMSI registry key of type REG\_DWORD and set it to 0.</span></span>

5.  <span data-ttu-id="39efd-156">Rejoignez la réunion.</span><span class="sxs-lookup"><span data-stu-id="39efd-156">Rejoin the meeting.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="39efd-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="39efd-157">See Also</span></span>


[<span data-ttu-id="39efd-158">Configuration de la page de participation à une réunion dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="39efd-158">Configuring the meeting join page in Lync Server 2013</span></span>](lync-server-2013-configuring-the-meeting-join-page.md)  
[<span data-ttu-id="39efd-159">Plates-formes prises en charge par Lync Web App pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="39efd-159">Lync Web App supported platforms for Lync Server 2013</span></span>](lync-server-2013-lync-web-app-supported-platforms.md)  
  

<span data-ttu-id="39efd-160"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="39efd-160"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

