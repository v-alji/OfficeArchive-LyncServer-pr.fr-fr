---
title: 'Lync Server 2013 : administration des utilisateurs dans un déploiement hybride'
description: 'Lync Server 2013 : administration des utilisateurs dans un déploiement hybride.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Administering users in a hybrid deployment
ms:assetid: 6924ed7b-30a9-4be7-b952-90655625f2c8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204967(v=OCS.15)
ms:contentKeyID: 48184381
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7f1d7684a9f56eb013574a985ded0313378621c2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49393865"
---
# <a name="administering-users-in-a-hybrid-lync-server-2013-deployment"></a><span data-ttu-id="abc2c-103">Administration des utilisateurs dans un déploiement 2013 Lync Server hybride</span><span class="sxs-lookup"><span data-stu-id="abc2c-103">Administering users in a hybrid Lync Server 2013 deployment</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="abc2c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="abc2c-104">

<span> </span></span></span>

<span data-ttu-id="abc2c-105">_**Dernière modification de la rubrique :** 2014-05-29_</span><span class="sxs-lookup"><span data-stu-id="abc2c-105">_**Topic Last Modified:** 2014-05-29_</span></span>

<span data-ttu-id="abc2c-106">Vous pouvez gérer les paramètres utilisateur et les stratégies pour les utilisateurs migrés vers Lync Online à l’aide des fonctionnalités de gestion des utilisateurs disponibles dans le centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="abc2c-106">You can manage user settings and policies for users migrated to Lync Online by using the User Management features available in the Microsoft 365 admin center.</span></span> <span data-ttu-id="abc2c-107">Vous devez vous connecter à l’aide d’un compte d’administrateur client pour effectuer des tâches d’administration.</span><span class="sxs-lookup"><span data-stu-id="abc2c-107">You must sign in by using your tenant administrator account to perform administration tasks.</span></span>

<div>

## <a name="moving-users-back-to-on-premises"></a><span data-ttu-id="abc2c-108">Replacer les utilisateurs sur le serveur local</span><span class="sxs-lookup"><span data-stu-id="abc2c-108">Moving Users Back to On-premises</span></span>

<div class="">


> [!IMPORTANT]  
> <span data-ttu-id="abc2c-109">Cette section s’applique uniquement aux utilisateurs qui ont été créés et activés pour Lync local, puis transférés d’un déploiement local vers Lync Online.</span><span class="sxs-lookup"><span data-stu-id="abc2c-109">This section applies only to users that were created and enabled for Lync on-premises and then moved from an on-premises deployment to Lync Online.</span></span> <span data-ttu-id="abc2c-110">Pour déplacer des utilisateurs qui ont été créés dans Lync Online (et qui ne sont pas encore activés pour Lync dans un déploiement local), voir <A href="lync-server-2013-moving-users-from-lync-online-to-lync-on-premises.md">déplacement des utilisateurs de Lync Online vers Lync local dans Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="abc2c-110">If you want to move users that were created in Lync Online (and not ever enabled for Lync in an on-premises deployment) see, <A href="lync-server-2013-moving-users-from-lync-online-to-lync-on-premises.md">Moving users from Lync Online to Lync on-premises in Lync Server 2013</A>.</span></span>



</div>

  - <span data-ttu-id="abc2c-111">Pour déplacer un utilisateur de Lync Online vers Lync local, exécutez les applets de commande suivantes :</span><span class="sxs-lookup"><span data-stu-id="abc2c-111">Run the following cmdlets to move a user from Lync Online back to Lync on-premises:</span></span>
    
       ```PowerShell
        $cred=Get-Credential
       ```
    
       ```PowerShell
        Move-CsUser -Identity username@contoso.com -Target localpool.contoso.com -Credential $cred -HostedMigrationOverrideUrl <URL>
       ```

<span data-ttu-id="abc2c-112">L’URL spécifiée pour le paramètre **HostedMigrationOverrideUrl** doit correspondre à celle du pool dans lequel le service de migration hébergée est exécuté, au format suivant :</span><span class="sxs-lookup"><span data-stu-id="abc2c-112">The format of the URL specified for the **HostedMigrationOverrideUrl** parameter must be the URL to the pool where the Hosted Migration service is running, in the following format:</span></span>

<span data-ttu-id="abc2c-113"> Https:// \<Pool FQDN\> /HostedMigration/hostedmigrationService.svc.</span><span class="sxs-lookup"><span data-stu-id="abc2c-113">Https://\<Pool FQDN\>/HostedMigration/hostedmigrationService.svc.</span></span> <span data-ttu-id="abc2c-114">Vous pouvez déterminer l’URL du service de migration hébergée en affichant l’URL du panneau de configuration Lync Online correspondant à votre compte Microsoft 365 ou de votre organisation Office 365.</span><span class="sxs-lookup"><span data-stu-id="abc2c-114">You can determine the URL to the Hosted Migration Service by viewing the URL for the Lync Online Control Panel for your Microsoft 365 or Office 365 organization account.</span></span>

<span data-ttu-id="abc2c-115">**Pour déterminer l’URL du service de migration hébergée pour votre organisation Microsoft 365 ou Office 365**</span><span class="sxs-lookup"><span data-stu-id="abc2c-115">**To determine the Hosted Migration Service URL for your Microsoft 365 or Office 365 organization**</span></span>

1.  <span data-ttu-id="abc2c-116">Connectez-vous à votre organisation en tant qu’administrateur.</span><span class="sxs-lookup"><span data-stu-id="abc2c-116">Log in to your organization as an administrator.</span></span>

2.  <span data-ttu-id="abc2c-117">Ouvrez le **Centre d’administration Lync**.</span><span class="sxs-lookup"><span data-stu-id="abc2c-117">Open the **Lync admin center**.</span></span>

3.  <span data-ttu-id="abc2c-118">Avec le **Centre d’administration Lync** affiché, sélectionnez et copiez l’URL dans la barre d’adresses jusqu’à **Lync.com**.</span><span class="sxs-lookup"><span data-stu-id="abc2c-118">With the **Lync admin center** displayed, select and copy the URL in the address bar up to **lync.com**.</span></span> <span data-ttu-id="abc2c-119">L’URL doit se présenter comme dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="abc2c-119">An example URL looks similar to the following:</span></span>
    
    `https://webdir0a.online.lync.com/lscp/?language=en-US&tenantID=`

4.  <span data-ttu-id="abc2c-120">Dans l’URL, remplacez **webdir** par **admin** pour obtenir le résultat suivant :</span><span class="sxs-lookup"><span data-stu-id="abc2c-120">Replace **webdir** in the URL with **admin**, resulting in the following:</span></span>
    
    `https://admin0a.online.lync.com`

5.  <span data-ttu-id="abc2c-121">Ajoutez la chaîne ci-dessous à l’URL : **/HostedMigration/hostedmigrationservice.svc**.</span><span class="sxs-lookup"><span data-stu-id="abc2c-121">Append the following string to the URL: **/HostedMigration/hostedmigrationservice.svc**.</span></span>
    
    <span data-ttu-id="abc2c-122">L’URL obtenue, qui est la valeur de **HostedMigrationOverrideUrl**, doit se présenter comme suit :</span><span class="sxs-lookup"><span data-stu-id="abc2c-122">The resulting URL, which is the value of the **HostedMigrationOverrideUrl**, should look like the following:</span></span>
    
    `https://admin0a.online.lync.com/HostedMigration/hostedmigrationservice.svc`

<span data-ttu-id="abc2c-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="abc2c-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

