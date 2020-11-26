---
title: Utiliser le BPA Analyzer pour rechercher des problèmes potentiels dans votre déploiement
description: Utiliser le BPA Analyzer pour analyser votre déploiement à la recherche de problèmes potentiels.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Using Best Practices Analyzer to scan your deployment for potential issues
ms:assetid: 09c84509-dc91-4e7b-882b-3c467b6b026d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg591343(v=OCS.15)
ms:contentKeyID: 48183359
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 032f5b46d8d5a28894e5f746e0cbc2aff6c5eaa2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443481"
---
# <a name="using-best-practices-analyzer-to-scan-your-lync-server-2013-deployment-for-potential-issues"></a><span data-ttu-id="57408-103">Utilisation de l’analyseur de meilleures pratiques pour analyser le déploiement de Lync Server 2013 pour détecter des problèmes potentiels</span><span class="sxs-lookup"><span data-stu-id="57408-103">Using Best Practices Analyzer to scan your Lync Server 2013 deployment for potential issues</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="57408-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="57408-104">

<span> </span></span></span>

<span data-ttu-id="57408-105">_**Dernière modification de la rubrique :** 2012-10-21_</span><span class="sxs-lookup"><span data-stu-id="57408-105">_**Topic Last Modified:** 2012-10-21_</span></span>

<span data-ttu-id="57408-106">Pour exécuter une analyse d’analyse des pratiques recommandées, vous devez spécifier les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="57408-106">To run a Best Practices Analyzer scan, you must specify the following:</span></span>

  - <span data-ttu-id="57408-107">**Informations d’identification**   Pour effectuer une analyse, vous devez vous connecter à un ordinateur sur lequel le système d’analyse des recommandations est installé à l’aide d’un compte membre du groupe Administrateurs local.</span><span class="sxs-lookup"><span data-stu-id="57408-107">**Credentials**   To run a scan, you must log on to a computer on which Best Practices Analyzer is installed by using an account that is a member of the local Administrators group.</span></span> <span data-ttu-id="57408-108">Par ailleurs, vous devez vous connecter à l’aide d’un compte d’utilisateur disposant des droits d’utilisateur et des autorisations nécessaires pour exécuter les analyses appropriées, ou vous devez spécifier des informations d’identification qui disposent des privilèges et autorisations d’utilisateur appropriés lorsque vous exécutez l’analyseur de meilleures pratiques.</span><span class="sxs-lookup"><span data-stu-id="57408-108">Additionally, you need to log on by using a user account that has the user rights and permissions required to run the appropriate scans, or you must specify credentials that have the appropriate user rights and permissions when you run Best Practices Analyzer.</span></span> <span data-ttu-id="57408-109">Pour plus d’informations, consultez la section [appartenances aux groupes et conditions d’utilisation requise pour l’analyseur de meilleures pratiques dans Lync Server 2013](lync-server-2013-group-memberships-and-user-rights-requirements-for-best-practices-analyzer.md).</span><span class="sxs-lookup"><span data-stu-id="57408-109">For details, see [Group memberships and user rights requirements for Best Practices Analyzer in Lync Server 2013](lync-server-2013-group-memberships-and-user-rights-requirements-for-best-practices-analyzer.md).</span></span>

  - <span data-ttu-id="57408-110">**Étendue de la numérisation**   Pour spécifier l’étendue de la numérisation, sélectionnez les catégories et les serveurs que vous souhaitez analyser.</span><span class="sxs-lookup"><span data-stu-id="57408-110">**Scope of scan**   To specify the scope of the scan, select the categories and servers that you want to scan.</span></span> <span data-ttu-id="57408-111">Vous pouvez sélectionner toutes les catégories, une ou plusieurs catégories ou un ou plusieurs serveurs au sein d’une catégorie spécifique dans votre environnement Lync Server.</span><span class="sxs-lookup"><span data-stu-id="57408-111">You can select all categories, one or more categories, or one or more servers within a specific category in your Lync Server environment.</span></span>

  - <span data-ttu-id="57408-112">**Type de numérisation**   Pour l’instant, l’analyse du bilan de santé est le seul type d’analyse disponible (option activée par défaut).</span><span class="sxs-lookup"><span data-stu-id="57408-112">**Type of scan**   Currently, the Health Check scan is the only type of scan available (selected by default).</span></span> <span data-ttu-id="57408-113">L’analyse de vérification de l’intégrité génère un rapport incluant des erreurs, des avertissements et d’autres informations pour tous les serveurs spécifiés dans l’étendue.</span><span class="sxs-lookup"><span data-stu-id="57408-113">The Health Check scan generates a report that includes errors, warnings, and other information for all servers specified in the scope.</span></span>

  - <span data-ttu-id="57408-114">**Débit du réseau**   Les options de vitesse du réseau incluent Fast LAN (100 MB/s), LAN (10 Mbps), WAN rapide (1,5 Mbps) ou WAN (64 kb/s).</span><span class="sxs-lookup"><span data-stu-id="57408-114">**Network speed**   Network speed options include Fast LAN (100 Mbps or more), LAN (10 Mbps), Fast WAN (1.5 Mbps), or WAN (64 kbps).</span></span> <span data-ttu-id="57408-115">Le temps estimé pour terminer la numérisation est basé sur ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="57408-115">The estimated time to complete the scan is based on this setting.</span></span> <span data-ttu-id="57408-116">Ce paramètre est également utilisé pour définir le délai d’expiration.</span><span class="sxs-lookup"><span data-stu-id="57408-116">This setting is also used to set the time-out period.</span></span> <span data-ttu-id="57408-117">Lors de l’analyse, l’analyseur de meilleures pratiques attend la réponse d’un serveur pour une durée spécifiée.</span><span class="sxs-lookup"><span data-stu-id="57408-117">During the scan, the Best Practices Analyzer waits for a response from a server for a specified time.</span></span> <span data-ttu-id="57408-118">S’il ne reçoit pas de réponse dans le délai imparti, il passe au serveur suivant de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="57408-118">If it does not receive a response within the specified time-out period, it moves to the next server in the scan.</span></span> <span data-ttu-id="57408-119">Sur les réseaux plus lents, ce délai d’expiration spécifié est plus long pour tenir compte des latences du réseau plus longues.</span><span class="sxs-lookup"><span data-stu-id="57408-119">On slower networks, this specified time-out period is longer to account for longer network latencies.</span></span> <span data-ttu-id="57408-120">Nous vous recommandons de sélectionner le lien le plus lent dans votre topologie pour ce paramètre afin que l’outil ne soit pas trop rapide.</span><span class="sxs-lookup"><span data-stu-id="57408-120">We recommend that you select the slowest link in your topology for this parameter so that the tool does not time out too quickly.</span></span>

<div>

## <a name="to-scan-your-lync-server-2013-deployment"></a><span data-ttu-id="57408-121">Pour analyser le déploiement de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="57408-121">To scan your Lync Server 2013 deployment</span></span>

1.  <span data-ttu-id="57408-122">Ouvrez une session sur un ordinateur sur lequel le système d’analyse des recommandations est installé à l’aide d’un compte membre du groupe Administrateurs local et ayant d’autres droits et autorisations d’utilisateur requis.</span><span class="sxs-lookup"><span data-stu-id="57408-122">Log on to a computer on which Best Practices Analyzer is installed by using an account that is a member of the local Administrators group, and has other required user rights and permissions.</span></span>

2.  <span data-ttu-id="57408-123">Cliquez sur **Démarrer**, pointez sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis cliquez sur **recommandations Analyzer**.</span><span class="sxs-lookup"><span data-stu-id="57408-123">Click **Start**, point to **All Programs**, click **Microsoft Lync Server 2013**, and then click **Best Practices Analyzer**.</span></span>

3.  <span data-ttu-id="57408-124">Dans l’écran d' **Accueil** , cliquez sur **Sélectionner les options pour une nouvelle analyse**.</span><span class="sxs-lookup"><span data-stu-id="57408-124">On the **Welcome** screen, click **Select options for a new scan**.</span></span>

4.  <span data-ttu-id="57408-125">Dans la page **se connecter à Active Directory** , vérifiez le nom spécifié dans **Active Directory Server**, puis effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="57408-125">On the **Connect to Active Directory** page, verify the name specified in **Active Directory Server**, and then do one of the following:</span></span>
    
      - <span data-ttu-id="57408-126">Pour effectuer une analyse à l’aide des informations d’identification que vous avez utilisées pour vous connecter à l’ordinateur, cliquez sur **se connecter au serveur Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="57408-126">To run a scan using the credentials that you used to log on to the computer, click **Connect to the Active Directory server**.</span></span>
    
      - <span data-ttu-id="57408-127">Pour spécifier d’autres informations d’identification que vous souhaitez utiliser pour les services de domaine Active Directory (AD FS), Edge Server ou Exchange Server, cliquez sur **afficher les options de connexion avancées**, activez chaque case à cocher pour lesquelles des informations d’identification distinctes sont requises, spécifiez les informations d’identification pour chaque case sélectionnée, puis cliquez sur **se connecter au serveur Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="57408-127">To specify different credentials that you want to use for Active Directory Domain Services, Edge Server, or Exchange Server, click **Show advanced logon options**, select each check box for which separate credentials are required, specify the credentials for each selected check box, and then click **Connect to the Active Directory server**.</span></span>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="57408-128">Avant de commencer l’analyse, l’analyseur de meilleures pratiques effectue une vérification du réseau et des autorisations pour vérifier que les informations d’identification du compte spécifiées sont valides et que l’analyseur des meilleures pratiques peut se connecter aux services de domaine Active Directory (AD FS).</span><span class="sxs-lookup"><span data-stu-id="57408-128">Before beginning the scan, Best Practices Analyzer performs a network and permissions check to ensure that the specified account credentials are valid and that Best Practices Analyzer can connect to Active Directory Domain Services.</span></span> <span data-ttu-id="57408-129">Si l’outil s’exécute sur un serveur de groupe de travail, l’outil vérifie également qu’il peut se connecter aux serveurs Edge du réseau de périmètre (autrement dit, s’il est inclus dans l’analyse).</span><span class="sxs-lookup"><span data-stu-id="57408-129">If the tool is running on a workgroup server, the tool also verifies that it can connect to Edge Servers in the perimeter network (that is, if they are included in the scan).</span></span>

    
    </div>

5.  <span data-ttu-id="57408-130">Dans la page **Démarrer une nouvelle analyse des meilleures pratiques** , sélectionnez les options que vous voulez inclure dans l’analyse, spécifiez la vitesse du réseau, puis cliquez sur **Démarrer l’analyse**.</span><span class="sxs-lookup"><span data-stu-id="57408-130">On the **Start a new Best Practices scan** page, select the options that you want to include in the scan, specify the network speed, and then click **Start scanning**.</span></span>

6.  <span data-ttu-id="57408-131">Sur la page **analyse terminée** , cliquez sur **afficher un rapport de cette analyse recommandée**.</span><span class="sxs-lookup"><span data-stu-id="57408-131">On the **Scanning Completed** page, click **View a report of this Best Practices scan**.</span></span>

7.  <span data-ttu-id="57408-132">Dans la page **afficher le rapport** des recommandations, effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="57408-132">On the **View Best Practices Report** page, do one of the following:</span></span>
    
      - <span data-ttu-id="57408-133">Pour afficher les rapports dans une liste organisée par composant serveur, cliquez sur **rapports de liste**, puis sur l’onglet **tous les problèmes** ou **éléments d’information** .</span><span class="sxs-lookup"><span data-stu-id="57408-133">To view reports in a list organized by server component, click **List Reports**, and then click either the **All Issues** tab or the **Informational Items** tab.</span></span>
    
      - <span data-ttu-id="57408-134">Pour afficher les rapports sous forme de liste hiérarchique organisée par type de résultat, cliquez sur **rapports d’arborescence**, puis sur l’onglet **affichage détaillé** ou **affichage de synthèse** .</span><span class="sxs-lookup"><span data-stu-id="57408-134">To view reports as a hierarchical list organized by types of results, click **Tree Reports**, and then click either the **Detailed View** tab or the **Summary View** tab.</span></span>
    
      - <span data-ttu-id="57408-135">Pour afficher d’autres rapports, cliquez sur **autres rapports**.</span><span class="sxs-lookup"><span data-stu-id="57408-135">To view other reports, click **Other Reports**.</span></span>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="57408-136">Pour plus d’informations sur les meilleurs rapports d’analyseurs et les problèmes qu’ils ont identifiés, voir <A href="lync-server-2013-viewing-and-working-with-reports-created-by-best-practices-analyzer.md">afficher et utiliser les rapports créés par meilleurs analyseurs dans Lync server 2013</A> et <A href="lync-server-2013-analyzing-and-resolving-issues-identified-by-best-practices-analyzer.md">analyser et résoudre les problèmes identifiés par l’analyseur de meilleures pratiques dans</A>Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="57408-136">For details about the Best Practices Analyzer reports and the issues they identify, see <A href="lync-server-2013-viewing-and-working-with-reports-created-by-best-practices-analyzer.md">Viewing and working with reports created by Best Practices Analyzer in Lync Server 2013</A> and <A href="lync-server-2013-analyzing-and-resolving-issues-identified-by-best-practices-analyzer.md">Analyzing and resolving issues identified by Best Practices Analyzer in Lync Server 2013</A>.</span></span>

    
    <span data-ttu-id="57408-137"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="57408-137"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

