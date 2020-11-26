---
title: 'Lync Server 2013 : restauration d’un serveur membre Enterprise Edition'
description: 'Lync Server 2013 : restauration d’un serveur membre Enterprise Edition.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Restoring an Enterprise Edition member server
ms:assetid: d960b19c-2104-4719-b736-0d940f254d42
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202191(v=OCS.15)
ms:contentKeyID: 51541523
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4f9838f030205d92988e185798d982f835122c9f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436208"
---
# <a name="restoring-an-enterprise-edition-member-server-in-lync-server-2013"></a><span data-ttu-id="19b2e-103">Restauration d’un serveur membre Enterprise Edition dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="19b2e-103">Restoring an Enterprise Edition member server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="19b2e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="19b2e-104">

<span> </span></span></span>

<span data-ttu-id="19b2e-105">_**Dernière modification de la rubrique :** 2013-02-18_</span><span class="sxs-lookup"><span data-stu-id="19b2e-105">_**Topic Last Modified:** 2013-02-18_</span></span>

<span data-ttu-id="19b2e-106">Si un serveur exécutant l’un des rôles serveur suivants ne fonctionne pas, suivez la procédure décrite dans cette rubrique pour restaurer le serveur.</span><span class="sxs-lookup"><span data-stu-id="19b2e-106">If a server running one of the following server roles fails, follow the procedure in this topic to restore the server.</span></span> <span data-ttu-id="19b2e-107">Si plusieurs serveurs échouent indépendamment, suivez la procédure pour chaque serveur.</span><span class="sxs-lookup"><span data-stu-id="19b2e-107">If multiple servers fail independently, follow the procedure for each server.</span></span>

  - <span data-ttu-id="19b2e-108">serveur frontal</span><span class="sxs-lookup"><span data-stu-id="19b2e-108">Front End Server</span></span>

  - <span data-ttu-id="19b2e-109">serveur de médiation</span><span class="sxs-lookup"><span data-stu-id="19b2e-109">Mediation Server</span></span>

  - <span data-ttu-id="19b2e-110">directeur</span><span class="sxs-lookup"><span data-stu-id="19b2e-110">Director</span></span>

  - <span data-ttu-id="19b2e-111">serveur de conversations permanentes</span><span class="sxs-lookup"><span data-stu-id="19b2e-111">Persistent Chat Server</span></span>

  - <span data-ttu-id="19b2e-112">serveur Edge</span><span class="sxs-lookup"><span data-stu-id="19b2e-112">Edge Server</span></span>

<div>


> [!TIP]  
> <span data-ttu-id="19b2e-113">Nous vous recommandons de prendre une copie d’image du système avant de commencer la restauration.</span><span class="sxs-lookup"><span data-stu-id="19b2e-113">We recommend that you take an image copy of the system before you start restoration.</span></span> <span data-ttu-id="19b2e-114">Vous pouvez utiliser cette image comme point de restauration en cas de problème de restauration.</span><span class="sxs-lookup"><span data-stu-id="19b2e-114">You can use this image as a rollback point, in case something goes wrong during restoration.</span></span> <span data-ttu-id="19b2e-115">Vous souhaiterez peut-être prendre la copie d’image après l’installation du système d’exploitation et de SQL Server, puis restaurez ou Réinscrivez les certificats.</span><span class="sxs-lookup"><span data-stu-id="19b2e-115">You might want to take the image copy after you install the operating system and SQL Server, and restore or reenroll the certificates.</span></span>



</div>

<div>

## <a name="to-restore-a-member-server"></a><span data-ttu-id="19b2e-116">Pour restaurer un serveur membre</span><span class="sxs-lookup"><span data-stu-id="19b2e-116">To restore a member server</span></span>

1.  <span data-ttu-id="19b2e-117">Commencez par un serveur propre ou nouveau qui porte le même nom de domaine complet (FQDN) que le serveur en panne, installez le système d’exploitation, puis restaurez ou Réinscrivez les certificats.</span><span class="sxs-lookup"><span data-stu-id="19b2e-117">Start with a clean or new server that has the same fully qualified domain name (FQDN) as the failed server, install the operating system, and then restore or reenroll the certificates.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="19b2e-118">Pour effectuer cette étape, suivez les procédures de déploiement du serveur de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="19b2e-118">Follow your organization's server deployment procedures to perform this step.</span></span>

    
    </div>

2.  <span data-ttu-id="19b2e-119">À partir d’un compte d’utilisateur membre du groupe RTCUniversalServerAdmins, connectez-vous au serveur que vous restaurez.</span><span class="sxs-lookup"><span data-stu-id="19b2e-119">From a user account that is a member of the RTCUniversalServerAdmins group, log on to the server that you are restoring.</span></span>

3.  <span data-ttu-id="19b2e-120">Naviguez jusqu’au dossier d’installation et au média de Lync Server et démarrez l’Assistant Déploiement de Lync Server situé à l' \\ installation de \\ \\Setup.exe.</span><span class="sxs-lookup"><span data-stu-id="19b2e-120">Browse to the Lync Server installation folder or media, and start the Lync Server Deployment Wizard located at \\setup\\amd64\\Setup.exe.</span></span>

4.  <span data-ttu-id="19b2e-121">Suivez l’Assistant déploiement pour effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="19b2e-121">Follow the Deployment Wizard to do the following:</span></span>
    
    1.  <span data-ttu-id="19b2e-122">Exécutez l' **étape 1 : installer le magasin de configuration local** pour installer les fichiers de configuration locaux.</span><span class="sxs-lookup"><span data-stu-id="19b2e-122">Run **Step 1: Install Local Configuration Store** to install the local configuration files.</span></span>
    
    2.  <span data-ttu-id="19b2e-123">Exécutez l' **étape 2 : configurer ou supprimer les composants serveur Lync** pour installer le rôle serveur Lync Server.</span><span class="sxs-lookup"><span data-stu-id="19b2e-123">Run **Step 2: Setup or Remove Lync Server Components** to install the Lync Server server role.</span></span>
    
    3.  <span data-ttu-id="19b2e-124">Exécutez l' **étape 3 : demandez, installez ou attribuez des certificats** pour attribuer les certificats.</span><span class="sxs-lookup"><span data-stu-id="19b2e-124">Run **Step 3: Request, Install or Assign Certificates** to assign the certificates.</span></span>
    
    4.  <span data-ttu-id="19b2e-125">Exécutez l' **étape 4 : démarrer des services** pour démarrer des services sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="19b2e-125">Run **Step 4: Start Services** to start services on the server.</span></span>
    
    <span data-ttu-id="19b2e-126">Pour plus d’informations sur l’exécution de l’Assistant Déploiement, voir la documentation de déploiement pour le rôle de serveur que vous restaurez.</span><span class="sxs-lookup"><span data-stu-id="19b2e-126">For details about running the Deployment Wizard, see the Deployment documentation for the server role that you are restoring.</span></span>

<span data-ttu-id="19b2e-127"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="19b2e-127"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

