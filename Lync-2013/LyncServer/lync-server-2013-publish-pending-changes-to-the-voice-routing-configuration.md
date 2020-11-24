---
title: 'Lync Server 2013 : publier les modifications en attente apportées à la configuration de l’acheminement vocal'
description: 'Lync Server 2013 : Publiez les modifications en attente apportées à la configuration de l’acheminement vocal.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Publish pending changes to the voice routing configuration
ms:assetid: ff941d0b-fb4b-47d2-b866-6d990ac66b81
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413088(v=OCS.15)
ms:contentKeyID: 48185974
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2a7a56b9a07606932a34dea7149a799dbb60b376
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394565"
---
# <a name="publish-pending-changes-to-the-voice-routing-configuration-in-lync-server-2013"></a><span data-ttu-id="8d322-103">Publier les modifications en attente apportées à la configuration du routage de la voix dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8d322-103">Publish pending changes to the voice routing configuration in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8d322-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8d322-104">

<span> </span></span></span>

<span data-ttu-id="8d322-105">_**Dernière modification de la rubrique :** 2012-08-07_</span><span class="sxs-lookup"><span data-stu-id="8d322-105">_**Topic Last Modified:** 2012-08-07_</span></span>

<span data-ttu-id="8d322-106">Après avoir modifié les paramètres de configuration dans les pages du groupe **Routage des communications vocales**, effectuez cette procédure pour consulter, publier ou annuler les modifications en attente.</span><span class="sxs-lookup"><span data-stu-id="8d322-106">After you make changes to any of the configuration settings in pages in the **Voice Routing** group, perform this procedure to review, publish, or cancel the pending changes.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="8d322-107">Vérifiez qu’un seul utilisateur à la fois modifie les paramètres de configuration du routage des communications vocales.</span><span class="sxs-lookup"><span data-stu-id="8d322-107">Be sure that only one user at a time modifies the Voice Routing configuration settings.</span></span><BR><span data-ttu-id="8d322-p101">Toutes les modifications en attente doivent être publiées en même temps en exécutant la commande <STRONG>Tout valider</STRONG>. Vous ne pouvez pas sélectionner les modifications en attente que vous voulez publier. Avant de publier les modifications en attente, exécutez la commande <STRONG>Vérifier les modifications non validées</STRONG> et annulez les modifications de configuration que vous ne voulez pas publier.</span><span class="sxs-lookup"><span data-stu-id="8d322-p101">All pending changes must be published at the same time by running the <STRONG>Commit all</STRONG> command. You cannot selectively publish pending changes. Before you publish pending changes, run the <STRONG>Review uncommitted changes</STRONG> command and cancel any configuration changes that you do not want to publish.</span></span><BR><span data-ttu-id="8d322-111">Si vous quittez les pages du groupe <STRONG>Routage des communications vocales</STRONG> avant d’avoir validé les modifications en attente, toutes les modifications en attente seront perdues.</span><span class="sxs-lookup"><span data-stu-id="8d322-111">If you navigate away from the pages in the <STRONG>Voice Routing</STRONG> group before committing pending changes, all pending changes will be lost.</span></span> <span data-ttu-id="8d322-112">Cependant, vous pouvez exporter la configuration active (y compris les modifications en attente) vers un fichier de configuration des communications vocales, puis importer et publier la configuration mise à jour.</span><span class="sxs-lookup"><span data-stu-id="8d322-112">However, you can export the current configuration (including any pending changes) to a voice configuration file, and then import and publish the updated configuration.</span></span> <span data-ttu-id="8d322-113">Pour plus d’informations, voir <A href="lync-server-2013-export-a-voice-route-configuration-file.md">exporter un fichier de configuration de l’itinéraire vocal dans Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="8d322-113">For details, see <A href="lync-server-2013-export-a-voice-route-configuration-file.md">Export a voice route configuration file in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="to-review-publish-or-cancel-voice-routing-configuration-changes"></a><span data-ttu-id="8d322-114">Pour consulter, publier ou annuler les modifications de la configuration du routage des communications vocales</span><span class="sxs-lookup"><span data-stu-id="8d322-114">To review, publish, or cancel voice routing configuration changes</span></span>

1.  <span data-ttu-id="8d322-115">Connectez-vous à l’ordinateur en tant que membre du groupe RTCUniversalServerAdmins ou en tant que membre du rôle CsVoiceAdministrator, CsServerAdministrator ou CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="8d322-115">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the CsVoiceAdministrator, CsServerAdministrator, or CsAdministrator role.</span></span> <span data-ttu-id="8d322-116">Pour plus d’informations, reportez-vous à la section [délégation des autorisations de configuration dans Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="8d322-116">For details, see [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="8d322-117">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="8d322-117">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="8d322-118">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="8d322-118">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="8d322-119">Dans la barre de navigation de gauche, cliquez sur **Routage des communications vocales**.</span><span class="sxs-lookup"><span data-stu-id="8d322-119">In the left navigation bar, click **Voice Routing**.</span></span>

4.  <span data-ttu-id="8d322-120">Effectuez les modifications souhaitées au niveau de la configuration dans chacune des pages du groupe **Routage des communications vocales**.</span><span class="sxs-lookup"><span data-stu-id="8d322-120">Make the configuration changes you want to the settings on each page of the **Voice Routing** group.</span></span>

5.  <span data-ttu-id="8d322-121">Pour consulter les modifications en attente sans les publier, sélectionnez **Vérifier les modifications non validées** dans le menu **Valider**.</span><span class="sxs-lookup"><span data-stu-id="8d322-121">To review pending changes without publishing them, select **Review uncommitted changes** from the **Commit** menu.</span></span>

6.  <span data-ttu-id="8d322-122">Si vous souhaitez annuler l’une des modifications en attente, effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="8d322-122">If you want to cancel any of the pending changes, do one of the following:</span></span>
    
      - <span data-ttu-id="8d322-123">Sélectionnez **Annuler toutes les modifications non validées** dans le menu **Valider**.</span><span class="sxs-lookup"><span data-stu-id="8d322-123">Select **Cancel all uncommitted changes** from the **Commit** menu.</span></span>
    
      - <span data-ttu-id="8d322-124">Accédez à l’onglet de la page **Routage des communications vocales** qui contient les modifications en attente que vous souhaitez annuler, cliquez sur **Valider**, puis sur **Annuler les modifications sélectionnées**.</span><span class="sxs-lookup"><span data-stu-id="8d322-124">Navigate to the tab of the **Voice Routing** page that has pending changes you want to cancel, select the item with the pending changes, click **Commit**, and then click **Cancel selected changes**.</span></span>

7.  <span data-ttu-id="8d322-125">Une fois que vous avez vérifié toutes les modifications en attente et annulé celles que vous ne souhaitez pas publier, cliquez sur **Valider**, puis sur **Tout valider**.</span><span class="sxs-lookup"><span data-stu-id="8d322-125">After you have reviewed all pending changes and canceled any that you do not want to publish, click **Commit**, and then click **Commit all**.</span></span>

8.  <span data-ttu-id="8d322-126">Dans la boîte de dialogue **Paramètres de configuration de la voix non validés** qui contient la liste de toutes les modifications en attente, cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="8d322-126">In the **Uncommitted Voice Configuration Settings** dialog box, which displays a list of all of the pending changes, click **OK**.</span></span>
    
    <span data-ttu-id="8d322-127">Lorsque le panneau de configuration de Lync Server a validé les modifications, le message **configuration de routage vocale correctement publié** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="8d322-127">When Lync Server Control Panel has committed the changes, the **Successfully published voice routing configuration** message appears.</span></span>

<span data-ttu-id="8d322-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8d322-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

