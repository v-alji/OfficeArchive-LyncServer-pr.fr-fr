---
title: 'Lync Server 2013 : configuration de scénarios d’exemples vidéo'
description: 'Lync Server 2013 : configuration de scénarios d’exemples vidéo.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring video example scenarios
ms:assetid: da0d61a2-7ac4-4562-bf6a-18473a29acb2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205297(v=OCS.15)
ms:contentKeyID: 48185536
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 625899887926de9afe2e6ff94df70ab725c0190a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432407"
---
# <a name="configuring-video-example-scenarios-for-lync-server-2013"></a><span data-ttu-id="58761-103">Configuration de scénarios d’exemples vidéo pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="58761-103">Configuring video example scenarios for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="58761-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="58761-104">

<span> </span></span></span>

<span data-ttu-id="58761-105">_**Dernière modification de la rubrique :** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="58761-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="58761-106">Lync 2013 ajoute de nouvelles fonctionnalités vidéo pour la prise en charge des vidéos d’affichage de la vidéo HD 1920 x 1080.</span><span class="sxs-lookup"><span data-stu-id="58761-106">Lync 2013 adds new video features to support 1920 x 1080 full high definition (HD) video and Gallery View video.</span></span> <span data-ttu-id="58761-107">Les mesures sur la base des données client indiquent que la bande passante vidéo type n’est plus légèrement comparée à Lync 2010, mais que la bande passante maximale de la bande passante augmente en raison de la prise en charge complète HD (pour plus de détails, voir la section « utilisation du réseau du trafic multimédia » dans les [exigences de bande passante réseau de Lync Server 2013](lync-server-2013-network-bandwidth-requirements-for-media-traffic.md)).</span><span class="sxs-lookup"><span data-stu-id="58761-107">Measurements based on customer data show that the typical video bandwidth increased only slightly compared to Lync 2010, but the maximum video stream bandwidth has increased due to full HD support (for details, see the "Media Traffic Network Usage" section in [Network bandwidth requirements for media traffic in Lync Server 2013](lync-server-2013-network-bandwidth-requirements-for-media-traffic.md)).</span></span> <span data-ttu-id="58761-108">Les administrateurs peuvent donc vouloir limiter la bande passante vidéo pour certains utilisateurs (par exemple, les utilisateurs d’une succursale qui ont moins de capacités réseau) et permettent de garantir la meilleure qualité vidéo possible pour les autres utilisateurs (comme les dirigeants).</span><span class="sxs-lookup"><span data-stu-id="58761-108">Therefore, administrators may want to restrict video bandwidth for certain users (such as users in a branch office that has less network capacity) and help to ensure the best possible video quality for other users (such as executives).</span></span>

<span data-ttu-id="58761-109">Le tableau suivant répertorie les paramètres recommandés pour la configuration de la vidéo pour différentes capacités du réseau.</span><span class="sxs-lookup"><span data-stu-id="58761-109">The following table provides a list of recommended settings for configuring video for different network capacities.</span></span> <span data-ttu-id="58761-110">Ces paramètres restreignent certains scénarios d’utilisation et de réception de vidéos de haute résolution (voir la colonne la plus à droite).</span><span class="sxs-lookup"><span data-stu-id="58761-110">These settings will restrict some user scenarios from sending and receiving higher resolution videos (see rightmost column).</span></span> <span data-ttu-id="58761-111">Le paramètre minimum entraîne l’indisponibilité de la vidéo de la galerie en raison de la bande passante réseau faible de réception.</span><span class="sxs-lookup"><span data-stu-id="58761-111">The minimum setting will result in Gallery Video being unavailable, due to the low maximum receive network bandwidth.</span></span>

### <a name="recommended-video-settings"></a><span data-ttu-id="58761-112">Paramètres vidéo recommandés</span><span class="sxs-lookup"><span data-stu-id="58761-112">Recommended Video Settings</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th>-</th>
<th><span data-ttu-id="58761-113">AllowMultiView</span><span class="sxs-lookup"><span data-stu-id="58761-113">AllowMultiView</span></span></th>
<th><span data-ttu-id="58761-114">EnableMultiViewJoin</span><span class="sxs-lookup"><span data-stu-id="58761-114">EnableMultiViewJoin</span></span></th>
<th><span data-ttu-id="58761-115">VideoBitRateKB</span><span class="sxs-lookup"><span data-stu-id="58761-115">VideoBitRateKB</span></span></th>
<th><span data-ttu-id="58761-116">TotalReceiveVideoBitRateKB</span><span class="sxs-lookup"><span data-stu-id="58761-116">TotalReceiveVideoBitRateKB</span></span></th>
<th><span data-ttu-id="58761-117">Résolution vidéo prévue pour une vidéo de qualité optimale</span><span class="sxs-lookup"><span data-stu-id="58761-117">Expected video resolution for good quality video</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="58761-118">Optimal</span><span class="sxs-lookup"><span data-stu-id="58761-118">Best</span></span></p></td>
<td><p><span data-ttu-id="58761-119">Vrai</span><span class="sxs-lookup"><span data-stu-id="58761-119">True</span></span></p></td>
<td><p><span data-ttu-id="58761-120">Vrai</span><span class="sxs-lookup"><span data-stu-id="58761-120">True</span></span></p></td>
<td><p><span data-ttu-id="58761-121">8000</span><span class="sxs-lookup"><span data-stu-id="58761-121">8000</span></span></p></td>
<td><p><span data-ttu-id="58761-122">8000</span><span class="sxs-lookup"><span data-stu-id="58761-122">8000</span></span></p></td>
<td><p><span data-ttu-id="58761-123">Poste à poste : résolution vidéo de 1920 x 1080</span><span class="sxs-lookup"><span data-stu-id="58761-123">Peer-to-peer: Up to 1920 x 1080 video resolution</span></span></p>
<p><span data-ttu-id="58761-124">Affichage Galerie : jusqu’à 2 1920 x 1080 vidéos ou plusieurs vidéos de résolution réduite</span><span class="sxs-lookup"><span data-stu-id="58761-124">Gallery View: Up to two 1920 x 1080 videos or multiple smaller resolution videos</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58761-125">Good</span><span class="sxs-lookup"><span data-stu-id="58761-125">Good</span></span></p></td>
<td><p><span data-ttu-id="58761-126">Vrai</span><span class="sxs-lookup"><span data-stu-id="58761-126">True</span></span></p></td>
<td><p><span data-ttu-id="58761-127">Vrai</span><span class="sxs-lookup"><span data-stu-id="58761-127">True</span></span></p></td>
<td><p><span data-ttu-id="58761-128">2500</span><span class="sxs-lookup"><span data-stu-id="58761-128">2500</span></span></p></td>
<td><p><span data-ttu-id="58761-129">2500</span><span class="sxs-lookup"><span data-stu-id="58761-129">2500</span></span></p></td>
<td><p><span data-ttu-id="58761-130">Poste à poste : résolution vidéo de 1280 x 720</span><span class="sxs-lookup"><span data-stu-id="58761-130">Peer-to-peer: Up to 1280 x 720 video resolution</span></span></p>
<p><span data-ttu-id="58761-131">Vue Galerie : vidéo de résolution de 5 640 x 360</span><span class="sxs-lookup"><span data-stu-id="58761-131">Gallery View: Up to five 640 x 360 resolution videos</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58761-132">Moyen</span><span class="sxs-lookup"><span data-stu-id="58761-132">Medium</span></span></p></td>
<td><p><span data-ttu-id="58761-133">Vrai</span><span class="sxs-lookup"><span data-stu-id="58761-133">True</span></span></p></td>
<td><p><span data-ttu-id="58761-134">Vrai</span><span class="sxs-lookup"><span data-stu-id="58761-134">True</span></span></p></td>
<td><p><span data-ttu-id="58761-135">1000</span><span class="sxs-lookup"><span data-stu-id="58761-135">1000</span></span></p></td>
<td><p><span data-ttu-id="58761-136">1000</span><span class="sxs-lookup"><span data-stu-id="58761-136">1000</span></span></p></td>
<td><p><span data-ttu-id="58761-137">Poste à poste : résolution vidéo de 960 x 540</span><span class="sxs-lookup"><span data-stu-id="58761-137">Peer-to-peer: Up to 960 x 540 video resolution</span></span></p>
<p><span data-ttu-id="58761-138">Vue Galerie : vidéo de résolution de 5 424 x 240</span><span class="sxs-lookup"><span data-stu-id="58761-138">Gallery View: Up to five 424 x 240 resolution videos</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58761-139">Requise</span><span class="sxs-lookup"><span data-stu-id="58761-139">Minimum</span></span></p></td>
<td><p><span data-ttu-id="58761-140">Vrai</span><span class="sxs-lookup"><span data-stu-id="58761-140">True</span></span></p></td>
<td><p><span data-ttu-id="58761-141">False</span><span class="sxs-lookup"><span data-stu-id="58761-141">False</span></span></p></td>
<td><p><span data-ttu-id="58761-142">350</span><span class="sxs-lookup"><span data-stu-id="58761-142">350</span></span></p></td>
<td><p><span data-ttu-id="58761-143">350</span><span class="sxs-lookup"><span data-stu-id="58761-143">350</span></span></p></td>
<td><p><span data-ttu-id="58761-144">Poste à poste : résolution vidéo de 424 x 240</span><span class="sxs-lookup"><span data-stu-id="58761-144">Peer-to-peer: Up to 424 x 240 video resolution</span></span></p>
<p><span data-ttu-id="58761-145">Affichage Galerie : indisponible</span><span class="sxs-lookup"><span data-stu-id="58761-145">Gallery View: Unavailable</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="58761-146">Vous pouvez utiliser les informations contenues dans le tableau ci-dessus pour déployer les nouvelles fonctionnalités de visioconférence et de vidéoconférence HD pour certains utilisateurs de votre organisation, tout en autorisant des résolutions vidéo différentes pour les autres utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="58761-146">You can use the information in the preceding table to deploy the new HD video and Gallery View video conferencing features for some users in your organization, while allowing different video resolutions for others.</span></span>

<span data-ttu-id="58761-147">Dans l’exemple suivant, l’administrateur déploie les nouvelles fonctions vidéo avec la meilleure qualité vidéo disponible uniquement aux dirigeants.</span><span class="sxs-lookup"><span data-stu-id="58761-147">In the following example, the administrator rolls out the new video features with the highest video quality available only to executives.</span></span> <span data-ttu-id="58761-148">Pour les employés d’une succursale distante disposant d’une faible capacité réseau, le paramètre minimum du tableau précédent est déployé.</span><span class="sxs-lookup"><span data-stu-id="58761-148">For employees in a remote branch office that has low network capacity, only the minimum setting from the preceding table is deployed.</span></span> <span data-ttu-id="58761-149">Pour tous les autres employés, le paramètre « Good » du tableau précédent est déployé.</span><span class="sxs-lookup"><span data-stu-id="58761-149">For all other employees, the "Good" setting from the preceding table is deployed.</span></span>

<span data-ttu-id="58761-150">Pour déployer les nouvelles fonctionnalités aux dirigeants, l’administrateur crée une stratégie de conférence nommée ExecutiveVideo.</span><span class="sxs-lookup"><span data-stu-id="58761-150">To roll out the new features to the executives, the administrator creates a conferencing policy named ExecutiveVideo.</span></span> <span data-ttu-id="58761-151">Cette stratégie de conférence a les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="58761-151">This conferencing policy has the following settings:</span></span>

  - <span data-ttu-id="58761-152">VideoBitRateKB est défini sur 8000 kbps</span><span class="sxs-lookup"><span data-stu-id="58761-152">VideoBitRateKB is set to 8000 Kbps</span></span>

  - <span data-ttu-id="58761-153">TotalReceiveVideoBitRateKB est défini sur 8000 kbps</span><span class="sxs-lookup"><span data-stu-id="58761-153">TotalReceiveVideoBitRateKB is set to 8000 Kbps</span></span>

  - <span data-ttu-id="58761-154">AllowMultiview est défini sur true.</span><span class="sxs-lookup"><span data-stu-id="58761-154">AllowMultiview is set to True</span></span>

  - <span data-ttu-id="58761-155">EnableMultiviewJoin est défini sur true.</span><span class="sxs-lookup"><span data-stu-id="58761-155">EnableMultiviewJoin is set to True</span></span>

<span data-ttu-id="58761-156">Pour les employés de la succursale, l’administrateur crée une stratégie de conférence nommée BranchOfficeVideo.</span><span class="sxs-lookup"><span data-stu-id="58761-156">For employees in the branch office, the administrator creates a conferencing policy named BranchOfficeVideo.</span></span> <span data-ttu-id="58761-157">Cette stratégie de conférence a les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="58761-157">This conferencing policy has the following settings:</span></span>

  - <span data-ttu-id="58761-158">VideoBitRateKB est défini sur 350 kbps</span><span class="sxs-lookup"><span data-stu-id="58761-158">VideoBitRateKB is set to 350 Kbps</span></span>

  - <span data-ttu-id="58761-159">TotalReceiveVideoBitRateKB est défini sur 350 kbps</span><span class="sxs-lookup"><span data-stu-id="58761-159">TotalReceiveVideoBitRateKB is set to 350 Kbps</span></span>

  - <span data-ttu-id="58761-160">AllowMultiview est défini sur true.</span><span class="sxs-lookup"><span data-stu-id="58761-160">AllowMultiview is set to True</span></span>

  - <span data-ttu-id="58761-161">EnableMultiviewJoin est défini sur false.</span><span class="sxs-lookup"><span data-stu-id="58761-161">EnableMultiviewJoin is set to False</span></span>

<span data-ttu-id="58761-162">Pour tous les autres employés, l’administrateur crée une stratégie de conférence nommée StandardVideo.</span><span class="sxs-lookup"><span data-stu-id="58761-162">For all other employees, the administrator creates a conferencing policy named StandardVideo.</span></span> <span data-ttu-id="58761-163">Cette stratégie de conférence a les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="58761-163">This conferencing policy has the following settings:</span></span>

  - <span data-ttu-id="58761-164">VideoBitRateKB est défini sur 2500 kbps</span><span class="sxs-lookup"><span data-stu-id="58761-164">VideoBitRateKB is set to 2500 Kbps</span></span>

  - <span data-ttu-id="58761-165">TotalReceiveVideoBitRateKB est défini sur 2500 kbps</span><span class="sxs-lookup"><span data-stu-id="58761-165">TotalReceiveVideoBitRateKB is set to 2500 Kbps</span></span>

  - <span data-ttu-id="58761-166">AllowMultiview est défini sur true.</span><span class="sxs-lookup"><span data-stu-id="58761-166">AllowMultiview is set to True</span></span>

  - <span data-ttu-id="58761-167">EnableMultiviewJoin est défini sur true.</span><span class="sxs-lookup"><span data-stu-id="58761-167">EnableMultiviewJoin is set to True</span></span>

<span data-ttu-id="58761-168">L’administrateur affecte la stratégie de conférence aux utilisateurs comme suit :</span><span class="sxs-lookup"><span data-stu-id="58761-168">The administrator assigns conferencing policy to users as follows:</span></span>

  - <span data-ttu-id="58761-169">La stratégie de conférence ExecutiveVideo est affectée aux dirigeants.</span><span class="sxs-lookup"><span data-stu-id="58761-169">The ExecutiveVideo conferencing policy is assigned to the executives.</span></span>

  - <span data-ttu-id="58761-170">La stratégie de conférence BranchOfficeVideo est affectée à tous les employés de l’succursale.</span><span class="sxs-lookup"><span data-stu-id="58761-170">The BranchOfficeVideo conferencing policy is assigned to all employees in the branch office.</span></span>

  - <span data-ttu-id="58761-171">La stratégie de conférence StandardVideo est affectée à tous les autres employés.</span><span class="sxs-lookup"><span data-stu-id="58761-171">The StandardVideo conferencing policy is assigned to all other employees.</span></span>

<span data-ttu-id="58761-172">Ces attributions de stratégie de conférence génèrent l’interface utilisateur suivante :</span><span class="sxs-lookup"><span data-stu-id="58761-172">These conferencing policy assignments result in the following user experience:</span></span>

  - <span data-ttu-id="58761-173">Toutes les conférences organisées par tout type d’affichage Galerie de support utilisateur, mais les employés dans la succursale ne peuvent pas accéder à l’affichage Galerie.</span><span class="sxs-lookup"><span data-stu-id="58761-173">All conferences organized by any user support Gallery View, but employees in the branch office cannot experience Gallery View.</span></span>

  - <span data-ttu-id="58761-174">Dans le cadre d’une conférence à deux ou à plusieurs, les dirigeants peuvent envoyer une vidéo HD HD de 1920 x 1080, si leur matériel et leur lien réseau le prennent en charge, et qu’ils peuvent recevoir une vidéo HD de 1920 x 1080, au sein desquels les autres clients participants le prennent en charge.</span><span class="sxs-lookup"><span data-stu-id="58761-174">For any two-party or multiparty conferences, executives can send 1920 x 1080 full HD video, if their hardware and network link supports it, and can receive 1920 x 1080 full HD video where the other participant clients support it.</span></span>

  - <span data-ttu-id="58761-175">Les employés qui ne sont pas des dirigeants disposent de résolutions plus basses que celles des dirigeants dans leurs conférences à deux ou à plusieurs, mais ils continuent à utiliser une bonne résolution.</span><span class="sxs-lookup"><span data-stu-id="58761-175">Employees who are not executives experience lower resolutions than the executives in their two-party or multiparty conferences, but still get good resolution.</span></span>

  - <span data-ttu-id="58761-176">Les employés qui se trouvent dans la succursale disposent d’une bonne qualité vidéo dans les appels à deux participants lorsque Lync affiche la taille de la fenêtre vidéo par défaut ; Toutefois, si la fenêtre Lync est agrandie en plein écran, la résolution vidéo n’augmentera pas.</span><span class="sxs-lookup"><span data-stu-id="58761-176">Employees who are in the branch office will get good video quality in two-party calls when Lync displays the default video window size; however, if the Lync window is maximized to full screen, the video resolution will not increase.</span></span> <span data-ttu-id="58761-177">Dans le cadre de conférences à plusieurs, les employés de la succursale ne verront qu’une vidéo active.</span><span class="sxs-lookup"><span data-stu-id="58761-177">For multiparty conferences, the employees in the branch office will see only one active video.</span></span>

<span data-ttu-id="58761-178"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="58761-178"></div>

<span> </span>

</div>

</div>

</span></span></div>

