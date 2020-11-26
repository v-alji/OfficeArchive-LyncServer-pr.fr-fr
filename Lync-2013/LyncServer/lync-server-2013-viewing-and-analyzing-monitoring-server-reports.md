---
title: 'Lync Server 2013 : affichage et analyse des rapports du serveur de surveillance'
description: 'Lync Server 2013 : affichage et analyse des rapports du serveur de surveillance.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Viewing and analyzing monitoring server reports
ms:assetid: 4dd448f1-01d2-49b2-b109-0728f36566b7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720332(v=OCS.15)
ms:contentKeyID: 63969599
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3f2a1812d76a49d487bea35acae3e22ea403f105
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444006"
---
# <a name="viewing-and-analyzing-monitoring-server-reports-in-lync-server-2013"></a><span data-ttu-id="16807-103">Affichage et analyse des rapports du serveur de surveillance dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="16807-103">Viewing and analyzing monitoring server reports in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="16807-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="16807-104">

<span> </span></span></span>

<span data-ttu-id="16807-105">_**Dernière modification de la rubrique :** 2014-05-19_</span><span class="sxs-lookup"><span data-stu-id="16807-105">_**Topic Last Modified:** 2014-05-19_</span></span>

<span data-ttu-id="16807-106">Le rapport analyse du serveur fournit différentes mesures de qualité de la voix pour contrôler le QoE qui est remis aux utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="16807-106">Monitoring Server reports provides several different measures of voice quality to monitor the QoE that is being delivered to end-users.</span></span> <span data-ttu-id="16807-107">Par ailleurs, la surveillance du serveur comporte plusieurs rapports prédéfinis que votre organisation peut utiliser pour surveiller les tendances d’utilisation et de qualité multimédia sur le réseau de votre organisation et résoudre les problèmes de qualité de média.</span><span class="sxs-lookup"><span data-stu-id="16807-107">Additionally, Monitoring Server includes several built-in reports that your organization can use to watch usage and media quality trends on your organization's network and troubleshoot media quality issues that arise.</span></span>

<span data-ttu-id="16807-108">Un élément principal de la conservation des rapports du serveur de surveillance intéressants pour les opérations quotidiennes et hebdomadaires consiste à afficher et à analyser des rapports de qualité multimédia, en particulier :</span><span class="sxs-lookup"><span data-stu-id="16807-108">A primary part of keeping Monitoring Server Reports interesting for daily and weekly operations is viewing and analyzing Media Quality Reports, in particular:</span></span>

  - <span data-ttu-id="16807-109">Rapport de synthèse</span><span class="sxs-lookup"><span data-stu-id="16807-109">QoE Summary/Trend Reports</span></span>

  - <span data-ttu-id="16807-110">Rapports sur les performances QoE</span><span class="sxs-lookup"><span data-stu-id="16807-110">QoE Performance Reports</span></span>

<div>

## <a name="view-reports-from-the-monitoring-server"></a><span data-ttu-id="16807-111">Afficher des rapports du serveur de surveillance</span><span class="sxs-lookup"><span data-stu-id="16807-111">View reports from the monitoring server</span></span>

1.  <span data-ttu-id="16807-112">Dans un navigateur Web, recherchez les serveurs hébergeant SQL Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="16807-112">From a web browser, locate your servers hosting the SQL reporting services.</span></span>

2.  <span data-ttu-id="16807-113">Affichez les rapports nécessaires à partir de l’écran du navigateur.</span><span class="sxs-lookup"><span data-stu-id="16807-113">View the required reports from the browser screen.</span></span>

3.  <span data-ttu-id="16807-114">Facultatif Exportez un rapport en sélectionnant l’option Exporter et le format de sortie requis.</span><span class="sxs-lookup"><span data-stu-id="16807-114">(Optional) Export a report by selecting the export option and the required output format.</span></span>

</div>

<div>

## <a name="configure-call-detail-recording-cdr"></a><span data-ttu-id="16807-115">Configurer l’enregistrement des détails des appels (CDR)</span><span class="sxs-lookup"><span data-stu-id="16807-115">Configure call detail recording (CDR)</span></span>

1.  <span data-ttu-id="16807-116">À partir d’un compte d’utilisateur membre du groupe RTCUniversalServerAdmins (ou doté d’autorisations équivalentes) ou affectées au rôle CsServerAdministrator ou CsAdministrator, connectez-vous à n’importe quel ordinateur se trouve sur le réseau sur lequel vous avez déployé Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="16807-116">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent permissions), or assigned to the CsServerAdministrator or CsAdministrator role, log on to any computer that is in the network in which you deployed Lync Server 2013.</span></span>

2.  <span data-ttu-id="16807-117">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="16807-117">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span>

3.  <span data-ttu-id="16807-118">Dans la barre de navigation de gauche, cliquez sur **Surveillance et archivage**, puis cliquez sur **Enregistrement des détails des appels**.</span><span class="sxs-lookup"><span data-stu-id="16807-118">In the left navigation bar, click **Monitoring and Archiving**, and then click **Call Detail Recording**.</span></span>

4.  <span data-ttu-id="16807-119">Dans la page **Enregistrement des détails des appels**, cliquez sur le site approprié dans le tableau, cliquez sur **Modifier**, puis sur **Afficher les détails**.</span><span class="sxs-lookup"><span data-stu-id="16807-119">On the **Call Detail Recording** page, click the appropriate site in the table, click **Edit**, and then click **Show Details**.</span></span>

5.  <span data-ttu-id="16807-120">Pour activer le vidage, sélectionnez **activer la purge pour la surveillance des serveurs**.</span><span class="sxs-lookup"><span data-stu-id="16807-120">To turn on purging, select **Enable Purging for Monitoring Servers**.</span></span>

6.  <span data-ttu-id="16807-121">Dans **conserver les enregistrements des détails des appels pour une durée maximale (jours) :** sélectionnez le nombre maximal de jours pendant lequel les enregistrements des détails des appels doivent être conservés.</span><span class="sxs-lookup"><span data-stu-id="16807-121">In **Keep call detail recordings for maximum duration (days):** select the maximum number of days that call detail recordings should be retained.</span></span>

7.  <span data-ttu-id="16807-122">Dans **Conserver les données de signalement d’erreurs pendant la durée maximale (jours) :**, sélectionnez le nombre maximum de jours pendant lesquels les rapports d’erreurs sont à conserver.</span><span class="sxs-lookup"><span data-stu-id="16807-122">In **Keep error report data for maximum duration (days):** select the maximum number of days that error reports should be retained.</span></span>

8.  <span data-ttu-id="16807-123">Cliquez sur **Valider**.</span><span class="sxs-lookup"><span data-stu-id="16807-123">Click **Commit**.</span></span>

</div>

<div>

## <a name="configure-qoe"></a><span data-ttu-id="16807-124">Configurer QoE</span><span class="sxs-lookup"><span data-stu-id="16807-124">Configure QoE</span></span>

1.  <span data-ttu-id="16807-125">Connectez-vous à l’ordinateur en tant que membre du groupe RTCUniversalServerAdmins ou en tant que membre du rôle CsVoiceAdministrator, CsServerAdministrator ou CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="16807-125">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the CsVoiceAdministrator, CsServerAdministrator, or CsAdministrator role.</span></span> <span data-ttu-id="16807-126">Pour plus d’informations, consultez autorisations de configuration de délégué.</span><span class="sxs-lookup"><span data-stu-id="16807-126">For details, see Delegate Setup Permissions.</span></span>

2.  <span data-ttu-id="16807-127">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="16807-127">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span>

3.  <span data-ttu-id="16807-128">Dans la barre de navigation de gauche, cliquez sur **Surveillance et archivage**, puis cliquez sur **Données de qualité de l’expérience**.</span><span class="sxs-lookup"><span data-stu-id="16807-128">In the left navigation bar, click **Monitoring and Archiving**, and then click **Quality of Experience Data**.</span></span>

4.  <span data-ttu-id="16807-129">Dans la page **Données de qualité de l’expérience**, cliquez sur le site approprié dans le tableau, sur **Modifier**, puis sur **Afficher les détails**.</span><span class="sxs-lookup"><span data-stu-id="16807-129">On the **Quality of Experience Data** page, click the appropriate site from the table, click **Edit**, and then click **Show Details**.</span></span>

5.  <span data-ttu-id="16807-130">Pour activer le vidage, sélectionnez **activer la purge pour la surveillance des serveurs**.</span><span class="sxs-lookup"><span data-stu-id="16807-130">To turn on purging, select **Enable Purging for Monitoring Servers**.</span></span>

6.  <span data-ttu-id="16807-131">Dans **conserver les enregistrements des détails des appels pour une durée maximale (jours) :** sélectionnez le nombre maximal de jours pendant lequel les données QoE doivent être conservées.</span><span class="sxs-lookup"><span data-stu-id="16807-131">In **Keep call detail recordings for maximum duration (days):** select the maximum number of days that QoE data should be retained.</span></span>

7.  <span data-ttu-id="16807-132">Cliquez sur Valider.</span><span class="sxs-lookup"><span data-stu-id="16807-132">Click Commit.</span></span>

</div>

<div>

## <a name="change-the-archiving-policy"></a><span data-ttu-id="16807-133">Modifier la stratégie d’archivage</span><span class="sxs-lookup"><span data-stu-id="16807-133">Change the archiving policy</span></span>

1.  <span data-ttu-id="16807-134">À partir d’un compte d’utilisateur auquel est affecté un des rôles CsArchivingAdministrator ou CsAdministrator, ouvrez une session sur un ordinateur de votre déploiement interne.</span><span class="sxs-lookup"><span data-stu-id="16807-134">From a user account that is assigned to the CsArchivingAdministrator or CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="16807-135">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="16807-135">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span>

3.  <span data-ttu-id="16807-136">Dans la barre de navigation gauche, cliquez sur **surveillance et archivage**, puis cliquez sur **stratégie d’archivage**.</span><span class="sxs-lookup"><span data-stu-id="16807-136">In the left navigation bar, click **Monitoring and Archiving**, and then click **Archiving Policy**.</span></span>

4.  <span data-ttu-id="16807-137">Cliquez sur **Globale** dans la liste des stratégies, sur **Modifier**, puis sur **Afficher les détails**.</span><span class="sxs-lookup"><span data-stu-id="16807-137">Click **Global** in the list of policies, click **Edit**, and then click **Show details**.</span></span>

5.  <span data-ttu-id="16807-138">Dans **Modifier la stratégie d’archivage - Globale**, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="16807-138">In **Edit Archiving Policy - Global**, do the following:</span></span>

6.  <span data-ttu-id="16807-139">Pour activer ou désactiver l’archivage interne pour le déploiement, cochez ou décochez la case **archiver les communications internes** .</span><span class="sxs-lookup"><span data-stu-id="16807-139">To enable or disable internal archiving for the deployment, select or clear the **Archive internal communications** check box.</span></span>

7.  <span data-ttu-id="16807-140">Pour activer ou désactiver l’archivage externe pour le déploiement, cochez ou décochez la case **archiver les communications externes** .</span><span class="sxs-lookup"><span data-stu-id="16807-140">To enable or disable external archiving for the deployment, select or clear the **Archive external communications** check box.</span></span>

8.  <span data-ttu-id="16807-141">Cliquez sur **Valider**.</span><span class="sxs-lookup"><span data-stu-id="16807-141">Click **Commit**.</span></span>

</div>

<div>

## <a name="apply-an-archiving-policy-to-a-user"></a><span data-ttu-id="16807-142">Appliquer une stratégie d’archivage à un utilisateur</span><span class="sxs-lookup"><span data-stu-id="16807-142">Apply an archiving policy to a user</span></span>

1.  <span data-ttu-id="16807-143">À partir d’un compte d’utilisateur auquel est affecté un des rôles CsArchivingAdministrator ou CsAdministrator, ouvrez une session sur un ordinateur de votre déploiement interne.</span><span class="sxs-lookup"><span data-stu-id="16807-143">From a user account that is assigned to the CsArchivingAdministrator or CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="16807-144">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="16807-144">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span>

3.  <span data-ttu-id="16807-145">Dans la barre de navigation de gauche, cliquez sur **Utilisateurs**, puis recherchez le compte d’utilisateur à configurer.</span><span class="sxs-lookup"><span data-stu-id="16807-145">In the left navigation bar, click **Users**, and then search on the user account that you want to configure.</span></span>

4.  <span data-ttu-id="16807-146">Dans le tableau répertoriant les résultats de la recherche, cliquez sur le compte d’utilisateur, sur **Modifier**, puis sur **Afficher les détails**.</span><span class="sxs-lookup"><span data-stu-id="16807-146">In the table that lists the search results, click the user account, click **Edit**, and then click **Show details**.</span></span>

5.  <span data-ttu-id="16807-147">Dans **modifier l’utilisateur de Lync Server** sous **stratégie d’archivage**, sélectionnez la stratégie d’utilisateur d’archivage que vous voulez appliquer.</span><span class="sxs-lookup"><span data-stu-id="16807-147">In **Edit Lync Server User** under **Archiving policy**, select the archiving user policy that you want to apply.</span></span>

6.  <span data-ttu-id="16807-148">Cliquez sur **Valider**.</span><span class="sxs-lookup"><span data-stu-id="16807-148">Click **Commit**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="16807-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="16807-149">See Also</span></span>


[<span data-ttu-id="16807-150">Utilisation de rapports d’analyse dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="16807-150">Using Monitoring Reports in Lync Server 2013</span></span>](lync-server-2013-using-monitoring-reports.md)  
[<span data-ttu-id="16807-151">Rapport sur les performances du serveur dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="16807-151">Server Performance Report in Lync Server 2013</span></span>](lync-server-2013-server-performance-report.md)  
[<span data-ttu-id="16807-152">Rapport de comparaison de qualité multimédia dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="16807-152">Media Quality Comparison Report in Lync Server 2013</span></span>](lync-server-2013-media-quality-comparison-report.md)  
  

<span data-ttu-id="16807-153"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="16807-153"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

