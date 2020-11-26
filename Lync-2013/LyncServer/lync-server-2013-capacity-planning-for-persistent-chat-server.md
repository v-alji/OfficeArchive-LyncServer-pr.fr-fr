---
title: 'Lync Server 2013 : planification de la capacité pour le serveur de chat permanent'
description: 'Lync Server 2013 : planification de la capacité pour le serveur de chat permanent.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Capacity planning for Persistent Chat Server
ms:assetid: 7a850cd5-c789-4795-a8ff-083be21ae784
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615006(v=OCS.15)
ms:contentKeyID: 48184580
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f78f9f3666fb272b808ef36da2d3010f451d0079
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435557"
---
# <a name="capacity-planning-for-persistent-chat-server-in-lync-server-2013"></a><span data-ttu-id="1d261-103">Planification de la capacité pour le serveur de chat permanent dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1d261-103">Capacity planning for Persistent Chat Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1d261-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1d261-104">

<span> </span></span></span>

<span data-ttu-id="1d261-105">_**Dernière modification de la rubrique :** 2012-10-05_</span><span class="sxs-lookup"><span data-stu-id="1d261-105">_**Topic Last Modified:** 2012-10-05_</span></span>

<span data-ttu-id="1d261-106">Le serveur de chat permanent peut exécuter une discussion en temps réel avec plusieurs utilisateurs, qui peut être persistante lors de la récupération et de la recherche ultérieures.</span><span class="sxs-lookup"><span data-stu-id="1d261-106">Persistent Chat Server can perform multi-user real-time chat that can persist for future retrieval and search.</span></span> <span data-ttu-id="1d261-107">Contrairement à la messagerie instantanée de groupe enregistrée dans la boîte aux lettres d’un utilisateur si l’historique des conversations est configuré, une session serveur Chat permanent reste ouverte plus longtemps, et le contenu est enregistré sur un serveur, ainsi que les messages, les fichiers, les URL et les autres données faisant partie d’une conversation en cours.</span><span class="sxs-lookup"><span data-stu-id="1d261-107">Unlike group instant messaging (IM) that is saved in a user’s mailbox if conversation history is configured, a Persistent Chat Server session stays open longer, and the content is saved on a server, along with the messages, files, URLs, and other data that are part of an ongoing conversation.</span></span>

<span data-ttu-id="1d261-108">La planification de la capacité est une partie importante de la préparation du déploiement d’un serveur de chat permanent.</span><span class="sxs-lookup"><span data-stu-id="1d261-108">Capacity planning is an important part of preparing to deploy Persistent Chat Server.</span></span> <span data-ttu-id="1d261-109">Cette rubrique fournit des détails sur les topologies du serveur de chat permanent prises en charge et les tables de planification de capacité que vous pouvez utiliser pour déterminer la meilleure configuration pour votre déploiement.</span><span class="sxs-lookup"><span data-stu-id="1d261-109">This topic provides details about supported Persistent Chat Server topologies and capacity planning tables that you can use to determine the best configuration for your deployment.</span></span> <span data-ttu-id="1d261-110">Il explique également comment gérer au mieux les déploiements de serveurs de chat permanent qui nécessitent une plus grande capacité aux heures de pointe.</span><span class="sxs-lookup"><span data-stu-id="1d261-110">It also describes how to best manage Persistent Chat Server deployments that require greater capacity at peak times.</span></span>

<span data-ttu-id="1d261-111">Pour télécharger le serveur Chat permanent, voir « Microsoft Lync Server 13 persistent Chat Server » à l’adresse [https://go.microsoft.com/fwlink/p/?linkId=209539](https://go.microsoft.com/fwlink/p/?linkid=209539) .</span><span class="sxs-lookup"><span data-stu-id="1d261-111">To download Persistent Chat Server, see "Microsoft Lync Server 13 Persistent Chat Server" at [https://go.microsoft.com/fwlink/p/?linkId=209539](https://go.microsoft.com/fwlink/p/?linkid=209539).</span></span>

<span data-ttu-id="1d261-112">Pour plus d’informations sur l’installation d’un serveur de chat permanent, voir [installer le serveur Chat permanent dans Lync server 2013](lync-server-2013-installing-persistent-chat-server.md) et [configurer le serveur Chat permanent dans Lync Server 2013](lync-server-2013-configuring-persistent-chat-server.md) dans la documentation de déploiement.</span><span class="sxs-lookup"><span data-stu-id="1d261-112">For details about installing Persistent Chat Server, see [Installing Persistent Chat Server in Lync Server 2013](lync-server-2013-installing-persistent-chat-server.md) and [Configuring Persistent Chat Server in Lync Server 2013](lync-server-2013-configuring-persistent-chat-server.md) in the Deployment documentation.</span></span>

<span data-ttu-id="1d261-113">Les outils d’assistance, tels que l’outil de planification de Lync Server, peuvent vous aider à planifier la capacité.</span><span class="sxs-lookup"><span data-stu-id="1d261-113">Support tools, such as Lync Server Planning Tool, can further assist you with capacity planning.</span></span> <span data-ttu-id="1d261-114">Pour plus d’informations sur l’outil de planification, voir [commencer le processus de planification de Lync Server 2013](lync-server-2013-beginning-the-planning-process.md) dans la documentation de planification.</span><span class="sxs-lookup"><span data-stu-id="1d261-114">For details about the Planning Tool, see [Beginning the planning process for Lync Server 2013](lync-server-2013-beginning-the-planning-process.md) in the Planning documentation.</span></span>

<div>

## <a name="persistent-chat-server-supported-topologies"></a><span data-ttu-id="1d261-115">Topologies prises en charge par le serveur Chat permanent</span><span class="sxs-lookup"><span data-stu-id="1d261-115">Persistent Chat Server Supported Topologies</span></span>

<span data-ttu-id="1d261-116">Vous pouvez déployer le serveur de chat permanent dans les pools serveur unique ou serveur multiples, avec une topologie à pool unique ou à plusieurs pools.</span><span class="sxs-lookup"><span data-stu-id="1d261-116">You can deploy Persistent Chat Server in single-server or multiple-server pools, and with single-pool or multiple-pool topology.</span></span>

<span data-ttu-id="1d261-117">Nous prenons désormais en charge le serveur Chat permanent sur un serveur Standard Edition Server pour les nouveaux déploiements de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1d261-117">We now also support Persistent Chat Server on Standard Edition server for new Lync Server 2013 deployments.</span></span> <span data-ttu-id="1d261-118">Toutefois, les performances et l’évolutivité seront affectées, et comme il n’existe aucune option de haute disponibilité pour ce nouveau déploiement, nous pensons que vous utiliserez principalement cette méthode dans le cadre de la preuve de concept, d’évaluation, etc.</span><span class="sxs-lookup"><span data-stu-id="1d261-118">However, performance and scale will be affected, and because there is no high availability option for this new deployment, we expect you to use this primarily for the purposes of proof of concept, evaluation, and so on.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="1d261-119">Pour plus d’informations sur les deux topologies, reportez-vous à la section <A href="lync-server-2013-planning-for-persistent-chat-server.md">planification du serveur de chat permanent dans Lync server 2013</A> dans cette documentation Set et <A href="lync-server-2013-deploying-persistent-chat-server.md">déploiement du serveur de conversation permanent dans Lync Server 2013</A> dans la documentation de déploiement.</span><span class="sxs-lookup"><span data-stu-id="1d261-119">For additional details about both topologies, see <A href="lync-server-2013-planning-for-persistent-chat-server.md">Planning for Persistent Chat Server in Lync Server 2013</A> in this documentation set and <A href="lync-server-2013-deploying-persistent-chat-server.md">Deploying Persistent Chat Server in Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<div>

## <a name="single-server-topology"></a><span data-ttu-id="1d261-120">Topologie de Single-Server</span><span class="sxs-lookup"><span data-stu-id="1d261-120">Single-Server Topology</span></span>

<span data-ttu-id="1d261-121">La configuration minimum et le déploiement le plus simple pour le serveur de chat permanent est une topologie de serveur frontal de chat permanent unique.</span><span class="sxs-lookup"><span data-stu-id="1d261-121">The minimum configuration and simplest deployment for Persistent Chat Server is a single Persistent Chat Server Front End Server topology.</span></span> <span data-ttu-id="1d261-122">Ce déploiement nécessite un serveur unique exécutant chat permanent (qui exécute éventuellement le service de conformité, si la conformité est activée), un serveur qui héberge la base de données SQL Server et si la conformité est requise, la base de données SQL Server pour stocker les données de conformité.</span><span class="sxs-lookup"><span data-stu-id="1d261-122">This deployment requires a single server that runs Persistent Chat Server (which optionally runs the Compliance service, if compliance is enabled), a server that hosts both the SQL Server database, and if compliance is required, the SQL Server database to store the compliance data.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="1d261-123">Vous ne pouvez pas ajouter de serveurs supplémentaires à un pool de serveurs de chat permanent démarré comme déploiement d’un serveur unique dans le générateur de topologie.</span><span class="sxs-lookup"><span data-stu-id="1d261-123">You cannot add additional servers to a Persistent Chat Server pool that is started as a single-server deployment in Topology Builder.</span></span> <span data-ttu-id="1d261-124">Nous vous recommandons d’utiliser la topologie de pool multiserveur, même si vous utilisez un serveur unique.</span><span class="sxs-lookup"><span data-stu-id="1d261-124">We recommend using the multiple-server pool topology, even if you’re using a single server.</span></span> <span data-ttu-id="1d261-125">C’est pourquoi vous pourrez ajouter d’autres serveurs ultérieurement, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="1d261-125">This is so that you’ll be able to add more servers later, if it's necessary.</span></span> 


</div>

<span data-ttu-id="1d261-126">La figure suivante montre tous les composants obligatoires et facultatifs d’une topologie pour un seul serveur frontal de chat permanent avec conformité.</span><span class="sxs-lookup"><span data-stu-id="1d261-126">The following figure shows all required and optional components of a topology for a single Persistent Chat Server Front End Server with compliance.</span></span>

<span data-ttu-id="1d261-127">**Serveur de chat permanent unique**</span><span class="sxs-lookup"><span data-stu-id="1d261-127">**Single Persistent Chat Server**</span></span>

<span data-ttu-id="1d261-128">![Topologie de serveur unique avec service de conformité](images/Gg398500.9168fa52-61e0-4d17-a14d-45fd32e81456(OCS.15).jpg "Topologie de serveur unique avec service de conformité")</span><span class="sxs-lookup"><span data-stu-id="1d261-128">![Single server topology with Compliance service](images/Gg398500.9168fa52-61e0-4d17-a14d-45fd32e81456(OCS.15).jpg "Single server topology with Compliance service")</span></span>

</div>

<div>

## <a name="multiple-server-topology"></a><span data-ttu-id="1d261-129">Topologie de Multiple-Server</span><span class="sxs-lookup"><span data-stu-id="1d261-129">Multiple-Server Topology</span></span>

<span data-ttu-id="1d261-130">Afin d’offrir une plus grande capacité et une fiabilité accrue, vous pouvez déployer une topologie multiserveur, comme décrit dans [planification pour le serveur de chat permanent dans Lync server 2013](lync-server-2013-planning-for-persistent-chat-server.md).</span><span class="sxs-lookup"><span data-stu-id="1d261-130">To provide greater capacity and reliability, you can deploy a multiple-server topology, as described in [Planning for Persistent Chat Server in Lync Server 2013](lync-server-2013-planning-for-persistent-chat-server.md).</span></span> <span data-ttu-id="1d261-131">La topologie multiserveur peut inclure jusqu’à quatre ordinateurs actifs exécutant chat permanent (les configurations de haute disponibilité et de récupération d’urgence peuvent prendre jusqu’à 8, mais seules quatre peuvent être actives et les quatre autres en veille).</span><span class="sxs-lookup"><span data-stu-id="1d261-131">The multiple-server topology can include as many as four active computers running Persistent Chat Server (high availability and disaster recovery configurations will allow up to eight, but only four can be active and the remaining four on standby).</span></span> <span data-ttu-id="1d261-132">Chaque serveur peut prendre en charge autant d’utilisateurs simultanés qu' 20 000, soit un total d' 80 000 utilisateurs simultanés connectés à un pool de serveurs de chat permanent doté de 4 serveurs.</span><span class="sxs-lookup"><span data-stu-id="1d261-132">Each server can support as many as 20,000 concurrent users, for a total of 80,000 concurrent users connected to a Persistent Chat Server pool with 4 servers.</span></span> <span data-ttu-id="1d261-133">Une topologie multiserveur est la même que celle de la topologie sur un serveur, à l’exception de l’hébergement de plusieurs serveurs et de la possibilité d’augmenter leur taille.</span><span class="sxs-lookup"><span data-stu-id="1d261-133">A multiple-server topology is the same as the single-server topology except that multiple servers host Persistent Chat Server, and can scale higher.</span></span> <span data-ttu-id="1d261-134">Plusieurs ordinateurs exécutant un serveur Chat permanent doivent résider dans le même domaine de services de domaine Active Directory que Lync Server et le service de conformité.</span><span class="sxs-lookup"><span data-stu-id="1d261-134">Multiple computers running Persistent Chat Server should reside in the same Active Directory Domain Services domain as Lync Server and the Compliance service.</span></span>

<span data-ttu-id="1d261-135">La figure suivante montre tous les composants d’une topologie multiserveur avec plusieurs ordinateurs exécutant une conversation permanente serveur, le service de conformité facultatif et une base de données de conformité séparée.</span><span class="sxs-lookup"><span data-stu-id="1d261-135">The following figure shows all the components of a multiple-server topology with multiple computers running Persistent Chat Server, the optional Compliance service, and a separate compliance database.</span></span>

<span data-ttu-id="1d261-136">**Plusieurs serveurs de chat permanent**</span><span class="sxs-lookup"><span data-stu-id="1d261-136">**Multiple Persistent Chat Servers**</span></span>

<span data-ttu-id="1d261-137">![Topologie de plusieurs serveurs](images/Gg398500.19aea898-28df-4d9b-903c-f72ef062d919(OCS.15).jpg "Topologie de plusieurs serveurs")</span><span class="sxs-lookup"><span data-stu-id="1d261-137">![Multiple server topology](images/Gg398500.19aea898-28df-4d9b-903c-f72ef062d919(OCS.15).jpg "Multiple server topology")</span></span>

<span data-ttu-id="1d261-138">Dans le cas d’un déploiement sur un serveur de chat permanent à quatre serveurs, où les utilisateurs de 80 000 peuvent se connecter à un serveur et utiliser une conversation permanente, le chargement est distribué de façon égale auprès des utilisateurs 20 000 par serveur.</span><span class="sxs-lookup"><span data-stu-id="1d261-138">In a four-server Persistent Chat Server deployment, where 80,000 users can be simultaneously signed in to and using Persistent Chat, the load is distributed evenly at 20,000 users per server.</span></span> <span data-ttu-id="1d261-139">Si un serveur devient indisponible, les utilisateurs qui se connectent à ce serveur perdront leur accès au serveur Chat permanent.</span><span class="sxs-lookup"><span data-stu-id="1d261-139">If one server becomes unavailable, the users who are connected to that server will lose their access to Persistent Chat Server.</span></span> <span data-ttu-id="1d261-140">Ces utilisateurs déconnectés sont alors automatiquement transférés vers les serveurs restants jusqu’à ce que le serveur indisponible soit restauré.</span><span class="sxs-lookup"><span data-stu-id="1d261-140">The disconnected users will be automatically transferred to the remaining servers until the unavailable server is restored.</span></span> <span data-ttu-id="1d261-141">En fonction de la quantité de trafic de chat permanent sur le réseau, ce transfert peut prendre quelques minutes ou plus.</span><span class="sxs-lookup"><span data-stu-id="1d261-141">Depending on the amount of Persistent Chat traffic on the network, this transfer can take a few minutes or longer.</span></span> <span data-ttu-id="1d261-142">Étant donné que chacun des serveurs restants peut héberger autant d’utilisateurs qu' 30 000, nous vous recommandons de restaurer le serveur non disponible aussi rapidement que possible pour éviter les problèmes de performances.</span><span class="sxs-lookup"><span data-stu-id="1d261-142">Because each of the remaining servers might be hosting as many as 30,000 users, we recommend that you restore the unavailable server as quickly as possible to avoid performance issues.</span></span> <span data-ttu-id="1d261-143">Dans le cas contraire, vous pouvez rendre un autre serveur de chat permanent disponible via le générateur de topologie ou la cmdlet Windows PowerShell **Set-CsPersistentChatActiveServer**.</span><span class="sxs-lookup"><span data-stu-id="1d261-143">Otherwise, you can make another Persistent Chat Server available by using the Topology Builder or the Windows PowerShell cmdlet, **set-CsPersistentChatActiveServer**.</span></span>

</div>

</div>

<div>

## <a name="persistent-chat-server-capacity-planning"></a><span data-ttu-id="1d261-144">Planification de la capacité du serveur Chat permanent</span><span class="sxs-lookup"><span data-stu-id="1d261-144">Persistent Chat Server Capacity Planning</span></span>

<span data-ttu-id="1d261-145">Les tableaux suivants peuvent vous aider à planifier la capacité du serveur de chat permanent.</span><span class="sxs-lookup"><span data-stu-id="1d261-145">The following tables can help you with capacity planning for Persistent Chat Server.</span></span> <span data-ttu-id="1d261-146">Ils déterminent la manière dont les paramètres du serveur de conversation persistante affectent les capacités de capacité.</span><span class="sxs-lookup"><span data-stu-id="1d261-146">They model how changing various Persistent Chat Server settings affect capacity capabilities.</span></span>

<div>

## <a name="planning-your-maximum-capacity-for-persistent-chat-server"></a><span data-ttu-id="1d261-147">Planification de votre capacité maximale pour le serveur de chat permanent</span><span class="sxs-lookup"><span data-stu-id="1d261-147">Planning Your Maximum Capacity for Persistent Chat Server</span></span>

<span data-ttu-id="1d261-148">Utilisez l’exemple de tableau suivant pour déterminer le nombre d’utilisateurs que vous serez en mesure de prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="1d261-148">Use the following sample table to determine the number of users you will be able to support.</span></span>

### <a name="persistent-chat-server-pool-maximum-capacity-sample"></a><span data-ttu-id="1d261-149">Exemple de capacité maximale du pool de serveurs chat chat</span><span class="sxs-lookup"><span data-stu-id="1d261-149">Persistent Chat Server pool Maximum Capacity Sample</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1d261-150">Instances de service de chat permanent actives</span><span class="sxs-lookup"><span data-stu-id="1d261-150">Active Persistent Chat service instances</span></span></p></td>
<td><p><span data-ttu-id="1d261-151"><em>4</em></span><span class="sxs-lookup"><span data-stu-id="1d261-151"><em>4</em></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d261-152">Instances de service de chat permanent</span><span class="sxs-lookup"><span data-stu-id="1d261-152">Persistent Chat service instances</span></span></p></td>
<td><p><span data-ttu-id="1d261-153"><em>8 (4 doit être inactif ; seul un maximum de 4 peut être actif)</em></span><span class="sxs-lookup"><span data-stu-id="1d261-153"><em>8 (4 must be inactive; only a maximum of 4 can be active)</em></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d261-154">Utilisateurs actifs connectés</span><span class="sxs-lookup"><span data-stu-id="1d261-154">Active users connected</span></span></p></td>
<td><p><span data-ttu-id="1d261-155"><em>80,000</em></span><span class="sxs-lookup"><span data-stu-id="1d261-155"><em>80,000</em></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d261-156">Nombre total d’utilisateurs approvisionnés</span><span class="sxs-lookup"><span data-stu-id="1d261-156">Total provisioned users</span></span></p></td>
<td><p><span data-ttu-id="1d261-157">150,000</span><span class="sxs-lookup"><span data-stu-id="1d261-157">150,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d261-158">Nombre de points de terminaison</span><span class="sxs-lookup"><span data-stu-id="1d261-158">Number of endpoints</span></span></p></td>
<td><p><span data-ttu-id="1d261-159">120,000</span><span class="sxs-lookup"><span data-stu-id="1d261-159">120,000</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1d261-160">Dans l’exemple ci-dessus, le plan doit prendre en charge le nombre maximal d’utilisateurs pouvant être conservés par un serveur de chat permanent : quatre serveurs/instances du service de chat permanent (peuvent comporter 4 serveurs plus passifs pour une disponibilité élevée et une reprise après sinistre) et 20 000 utilisateurs par serveur, pour un total de 80 000 utilisateurs actifs.</span><span class="sxs-lookup"><span data-stu-id="1d261-160">In the preceding sample, the plan is to support the maximum number of users that Persistent Chat Server allows: four servers/instances of the Persistent Chat service (can have four more passive servers running Persistent Chat Server for high availability and disaster recovery) and 20,000 users per server, for a total of 80,000 active users.</span></span>

</div>

<div>

## <a name="capacity-planning-for-managing-persistent-chat-room-access"></a><span data-ttu-id="1d261-161">Planification de la capacité pour gérer l’accès aux salles de conversation permanente</span><span class="sxs-lookup"><span data-stu-id="1d261-161">Capacity Planning for Managing Persistent Chat Room Access</span></span>

<span data-ttu-id="1d261-162">L’exemple de tableau suivant peut vous aider à planifier la gestion de l’accès aux salles de conversation permanentes dans un pool de serveurs de chat permanent.</span><span class="sxs-lookup"><span data-stu-id="1d261-162">The following sample table can help you plan for managing Persistent Chat room access in a Persistent Chat Server pool.</span></span>

### <a name="managing-chat-room-access-sample"></a><span data-ttu-id="1d261-163">Exemple de gestion de l’accès aux salles de conversation</span><span class="sxs-lookup"><span data-stu-id="1d261-163">Managing Chat Room Access Sample</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="1d261-164">Salles de conversation de petite taille</span><span class="sxs-lookup"><span data-stu-id="1d261-164">Small Chat Rooms</span></span></th>
<th><span data-ttu-id="1d261-165">Salles de conversation de taille moyenne</span><span class="sxs-lookup"><span data-stu-id="1d261-165">Medium Chat Rooms</span></span></th>
<th><span data-ttu-id="1d261-166">Salles de conversation de grande taille</span><span class="sxs-lookup"><span data-stu-id="1d261-166">Large Chat Rooms</span></span></th>
<th><span data-ttu-id="1d261-167">Total</span><span class="sxs-lookup"><span data-stu-id="1d261-167">Total</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1d261-168">Taille des salles de conversation (nombre d’utilisateurs connectés)</span><span class="sxs-lookup"><span data-stu-id="1d261-168">Size of chat rooms (number of users connected)</span></span></p></td>
<td><p><span data-ttu-id="1d261-169">30 par salle</span><span class="sxs-lookup"><span data-stu-id="1d261-169">30 per room</span></span></p></td>
<td><p><span data-ttu-id="1d261-170">150 par salle</span><span class="sxs-lookup"><span data-stu-id="1d261-170">150 per room</span></span></p></td>
<td><p><span data-ttu-id="1d261-171">16 000 par salle</span><span class="sxs-lookup"><span data-stu-id="1d261-171">16,000 per room</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d261-172">Salles de conversation</span><span class="sxs-lookup"><span data-stu-id="1d261-172">Chat rooms</span></span></p></td>
<td><p><span data-ttu-id="1d261-173">32,000</span><span class="sxs-lookup"><span data-stu-id="1d261-173">32,000</span></span></p></td>
<td><p><span data-ttu-id="1d261-174">1,067</span><span class="sxs-lookup"><span data-stu-id="1d261-174">1,067</span></span></p></td>
<td><p><span data-ttu-id="1d261-175">0,10</span><span class="sxs-lookup"><span data-stu-id="1d261-175">10</span></span></p></td>
<td><p><span data-ttu-id="1d261-176">33,077</span><span class="sxs-lookup"><span data-stu-id="1d261-176">33,077</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d261-177">% de salles auditorium</span><span class="sxs-lookup"><span data-stu-id="1d261-177">% of rooms that are auditorium</span></span></p></td>
<td><p><span data-ttu-id="1d261-178">1 %</span><span class="sxs-lookup"><span data-stu-id="1d261-178">1%</span></span></p></td>
<td><p><span data-ttu-id="1d261-179">1 %</span><span class="sxs-lookup"><span data-stu-id="1d261-179">1%</span></span></p></td>
<td><p><span data-ttu-id="1d261-180">50%</span><span class="sxs-lookup"><span data-stu-id="1d261-180">50%</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d261-181">% de salles ouvertes</span><span class="sxs-lookup"><span data-stu-id="1d261-181">% of rooms that are open</span></span></p></td>
<td><p><span data-ttu-id="1d261-182">3%</span><span class="sxs-lookup"><span data-stu-id="1d261-182">3%</span></span></p></td>
<td><p><span data-ttu-id="1d261-183">3%</span><span class="sxs-lookup"><span data-stu-id="1d261-183">3%</span></span></p></td>
<td><p><span data-ttu-id="1d261-184">50%</span><span class="sxs-lookup"><span data-stu-id="1d261-184">50%</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d261-185">Salles ouvertes (aucune appartenance explicite)</span><span class="sxs-lookup"><span data-stu-id="1d261-185">Open rooms (no explicit membership)</span></span></p></td>
<td><p><span data-ttu-id="1d261-186">960</span><span class="sxs-lookup"><span data-stu-id="1d261-186">960</span></span></p></td>
<td><p><span data-ttu-id="1d261-187">32</span><span class="sxs-lookup"><span data-stu-id="1d261-187">32</span></span></p></td>
<td><p><span data-ttu-id="1d261-188">5</span><span class="sxs-lookup"><span data-stu-id="1d261-188">5</span></span></p></td>
<td><p><span data-ttu-id="1d261-189">997</span><span class="sxs-lookup"><span data-stu-id="1d261-189">997</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d261-190">Salles non ouvertes (salles standard avec appartenance explicite)</span><span class="sxs-lookup"><span data-stu-id="1d261-190">Non-open rooms (regular rooms with explicit membership)</span></span></p></td>
<td><p><span data-ttu-id="1d261-191">31,040</span><span class="sxs-lookup"><span data-stu-id="1d261-191">31,040</span></span></p></td>
<td><p><span data-ttu-id="1d261-192">1.035</span><span class="sxs-lookup"><span data-stu-id="1d261-192">1.035</span></span></p></td>
<td><p><span data-ttu-id="1d261-193">5</span><span class="sxs-lookup"><span data-stu-id="1d261-193">5</span></span></p></td>
<td><p><span data-ttu-id="1d261-194">32,080</span><span class="sxs-lookup"><span data-stu-id="1d261-194">32,080</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d261-195">Salles auditorium (entrée de présentateurs supplémentaires)</span><span class="sxs-lookup"><span data-stu-id="1d261-195">Auditorium rooms (additional presenters entry)</span></span></p></td>
<td><p><span data-ttu-id="1d261-196">0,4</span><span class="sxs-lookup"><span data-stu-id="1d261-196">0</span></span></p></td>
<td><p><span data-ttu-id="1d261-197">32</span><span class="sxs-lookup"><span data-stu-id="1d261-197">32</span></span></p></td>
<td><p><span data-ttu-id="1d261-198">5</span><span class="sxs-lookup"><span data-stu-id="1d261-198">5</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d261-199">Salles gérées par appartenance directe</span><span class="sxs-lookup"><span data-stu-id="1d261-199">Rooms managed by direct membership</span></span></p></td>
<td><p><span data-ttu-id="1d261-200">50%</span><span class="sxs-lookup"><span data-stu-id="1d261-200">50%</span></span></p></td>
<td><p><span data-ttu-id="1d261-201">10%</span><span class="sxs-lookup"><span data-stu-id="1d261-201">10%</span></span></p></td>
<td><p><span data-ttu-id="1d261-202">0%</span><span class="sxs-lookup"><span data-stu-id="1d261-202">0%</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d261-203">Salles gérées par groupes d’utilisateurs</span><span class="sxs-lookup"><span data-stu-id="1d261-203">Rooms managed by user groups</span></span></p></td>
<td><p><span data-ttu-id="1d261-204">50%</span><span class="sxs-lookup"><span data-stu-id="1d261-204">50%</span></span></p></td>
<td><p><span data-ttu-id="1d261-205">90%</span><span class="sxs-lookup"><span data-stu-id="1d261-205">90%</span></span></p></td>
<td><p><span data-ttu-id="1d261-206">100%</span><span class="sxs-lookup"><span data-stu-id="1d261-206">100%</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d261-207">Groupes d’utilisateurs dans la liste des membres de chaque salle de conversation pour les salles ouvertes (non spécifiés explicitement)</span><span class="sxs-lookup"><span data-stu-id="1d261-207">User groups in each chat room's membership list for open rooms (not specified explicitly)</span></span></p></td>
<td><p><span data-ttu-id="1d261-208">0,4</span><span class="sxs-lookup"><span data-stu-id="1d261-208">0</span></span></p></td>
<td><p><span data-ttu-id="1d261-209">0,4</span><span class="sxs-lookup"><span data-stu-id="1d261-209">0</span></span></p></td>
<td><p><span data-ttu-id="1d261-210">0,4</span><span class="sxs-lookup"><span data-stu-id="1d261-210">0</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d261-211">Utilisateurs dans la liste des membres de chaque salle de conversation pour les salles non ouvertes</span><span class="sxs-lookup"><span data-stu-id="1d261-211">Users in each chat room's membership list for non-open rooms</span></span></p></td>
<td><p><span data-ttu-id="1d261-212">trente</span><span class="sxs-lookup"><span data-stu-id="1d261-212">30</span></span></p></td>
<td><p><span data-ttu-id="1d261-213">150</span><span class="sxs-lookup"><span data-stu-id="1d261-213">150</span></span></p></td>
<td><p><span data-ttu-id="1d261-214">16,000</span><span class="sxs-lookup"><span data-stu-id="1d261-214">16,000</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d261-215">Groupes d’utilisateurs dans la liste des membres de chaque salle de conversation pour les salles non ouvertes</span><span class="sxs-lookup"><span data-stu-id="1d261-215">User groups in each chat room's membership list for non-open rooms</span></span></p></td>
<td><p><span data-ttu-id="1d261-216">3</span><span class="sxs-lookup"><span data-stu-id="1d261-216">3</span></span></p></td>
<td><p><span data-ttu-id="1d261-217">5</span><span class="sxs-lookup"><span data-stu-id="1d261-217">5</span></span></p></td>
<td><p><span data-ttu-id="1d261-218">0,10</span><span class="sxs-lookup"><span data-stu-id="1d261-218">10</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d261-219">Utilisateurs et groupes d’utilisateurs dans la liste des gestionnaires de chaque salle de conversation (pour les salles ouvertes et non ouvertes)</span><span class="sxs-lookup"><span data-stu-id="1d261-219">Users and user groups in each chat room's manager list (for open and non-open rooms)</span></span></p></td>
<td><p><span data-ttu-id="1d261-220">6</span><span class="sxs-lookup"><span data-stu-id="1d261-220">6</span></span></p></td>
<td><p><span data-ttu-id="1d261-221">6</span><span class="sxs-lookup"><span data-stu-id="1d261-221">6</span></span></p></td>
<td><p><span data-ttu-id="1d261-222">6</span><span class="sxs-lookup"><span data-stu-id="1d261-222">6</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d261-223">Utilisateurs et groupes d’utilisateurs dans la liste des présentateurs de chaque salle de conversation auditorium (pour les salles ouvertes et non ouvertes)</span><span class="sxs-lookup"><span data-stu-id="1d261-223">Users and user groups in each auditorium chat room's presenters list (for open and non-open rooms)</span></span></p></td>
<td><p><span data-ttu-id="1d261-224">6</span><span class="sxs-lookup"><span data-stu-id="1d261-224">6</span></span></p></td>
<td><p><span data-ttu-id="1d261-225">6</span><span class="sxs-lookup"><span data-stu-id="1d261-225">6</span></span></p></td>
<td><p><span data-ttu-id="1d261-226">6</span><span class="sxs-lookup"><span data-stu-id="1d261-226">6</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d261-227">Entités d’appartenance basées sur l’utilisateur dans toutes les salles non ouvertes</span><span class="sxs-lookup"><span data-stu-id="1d261-227">User-based membership entities across all non-open rooms</span></span></p></td>
<td><p><span data-ttu-id="1d261-228">465,600</span><span class="sxs-lookup"><span data-stu-id="1d261-228">465,600</span></span></p></td>
<td><p><span data-ttu-id="1d261-229">15,520</span><span class="sxs-lookup"><span data-stu-id="1d261-229">15,520</span></span></p></td>
<td><p>-</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d261-230">Entités d’appartenance basées sur le groupe d’utilisateurs dans toutes les salles non ouvertes</span><span class="sxs-lookup"><span data-stu-id="1d261-230">User-group-based membership entities across all non-open rooms</span></span></p></td>
<td><p><span data-ttu-id="1d261-231">46,560</span><span class="sxs-lookup"><span data-stu-id="1d261-231">46,560</span></span></p></td>
<td><p><span data-ttu-id="1d261-232">4656</span><span class="sxs-lookup"><span data-stu-id="1d261-232">4656</span></span></p></td>
<td><p><span data-ttu-id="1d261-233">50</span><span class="sxs-lookup"><span data-stu-id="1d261-233">50</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d261-234">Entités basées sur les utilisateurs et groupes d’utilisateurs dans toutes les salles de conversation auditorium</span><span class="sxs-lookup"><span data-stu-id="1d261-234">Users and user groups based entities across all auditorium chat rooms</span></span></p></td>
<td><p><span data-ttu-id="1d261-235">0,4</span><span class="sxs-lookup"><span data-stu-id="1d261-235">0</span></span></p></td>
<td><p><span data-ttu-id="1d261-236">192</span><span class="sxs-lookup"><span data-stu-id="1d261-236">192</span></span></p></td>
<td><p><span data-ttu-id="1d261-237">50</span><span class="sxs-lookup"><span data-stu-id="1d261-237">50</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d261-238">Entités de gestionnaires basées sur les utilisateurs et les groupes d’utilisateurs dans toutes les listes de gestionnaires de salles de conversation</span><span class="sxs-lookup"><span data-stu-id="1d261-238">Users and user groups based manager entities across all chat rooms manager lists</span></span></p></td>
<td><p><span data-ttu-id="1d261-239">192,000</span><span class="sxs-lookup"><span data-stu-id="1d261-239">192,000</span></span></p></td>
<td><p><span data-ttu-id="1d261-240">6,400</span><span class="sxs-lookup"><span data-stu-id="1d261-240">6,400</span></span></p></td>
<td><p><span data-ttu-id="1d261-241">60</span><span class="sxs-lookup"><span data-stu-id="1d261-241">60</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d261-242">Utilisateurs actifs par salle de conversation</span><span class="sxs-lookup"><span data-stu-id="1d261-242">Active users per chat room</span></span></p></td>
<td><p><span data-ttu-id="1d261-243"><em>trente</em></span><span class="sxs-lookup"><span data-stu-id="1d261-243"><em>30</em></span></span></p></td>
<td><p><span data-ttu-id="1d261-244"><em>150</em></span><span class="sxs-lookup"><span data-stu-id="1d261-244"><em>150</em></span></span></p></td>
<td><p><span data-ttu-id="1d261-245"><em>16,000</em></span><span class="sxs-lookup"><span data-stu-id="1d261-245"><em>16,000</em></span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d261-246">Salles de conversation par utilisateur</span><span class="sxs-lookup"><span data-stu-id="1d261-246">Chat rooms per user</span></span></p></td>
<td><p><span data-ttu-id="1d261-247"><em>midi</em></span><span class="sxs-lookup"><span data-stu-id="1d261-247"><em>12</em></span></span></p></td>
<td><p><span data-ttu-id="1d261-248"><em>2</em></span><span class="sxs-lookup"><span data-stu-id="1d261-248"><em>2</em></span></span></p></td>
<td><p><span data-ttu-id="1d261-249"><em>2</em></span><span class="sxs-lookup"><span data-stu-id="1d261-249"><em>2</em></span></span></p></td>
<td><p><span data-ttu-id="1d261-250"><em>Seiz</em></span><span class="sxs-lookup"><span data-stu-id="1d261-250"><em>16</em></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d261-251">Groupes d’utilisateurs dans chaque liste d’appartenance à une salle de conversation</span><span class="sxs-lookup"><span data-stu-id="1d261-251">User groups in each chat room’s membership list</span></span></p></td>
<td><p><span data-ttu-id="1d261-252"><em>0,10</em></span><span class="sxs-lookup"><span data-stu-id="1d261-252"><em>10</em></span></span></p></td>
<td><p><span data-ttu-id="1d261-253"><em>0,10</em></span><span class="sxs-lookup"><span data-stu-id="1d261-253"><em>10</em></span></span></p></td>
<td><p><span data-ttu-id="1d261-254"><em>0,15</em></span><span class="sxs-lookup"><span data-stu-id="1d261-254"><em>15</em></span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d261-255">Salles gérées par groupes d’utilisateurs</span><span class="sxs-lookup"><span data-stu-id="1d261-255">Rooms managed by user groups</span></span></p></td>
<td><p><span data-ttu-id="1d261-256"><em>50%</em></span><span class="sxs-lookup"><span data-stu-id="1d261-256"><em>50%</em></span></span></p></td>
<td><p><span data-ttu-id="1d261-257"><em>50%</em></span><span class="sxs-lookup"><span data-stu-id="1d261-257"><em>50%</em></span></span></p></td>
<td><p><span data-ttu-id="1d261-258"><em>50%</em></span><span class="sxs-lookup"><span data-stu-id="1d261-258"><em>50%</em></span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d261-259">Entités d’appartenance basées sur le groupe d’utilisateurs dans toutes les salles de conversation</span><span class="sxs-lookup"><span data-stu-id="1d261-259">User-group-based membership entities across all chat rooms</span></span></p></td>
<td><p><span data-ttu-id="1d261-260">155,200</span><span class="sxs-lookup"><span data-stu-id="1d261-260">155,200</span></span></p></td>
<td><p><span data-ttu-id="1d261-261">5173</span><span class="sxs-lookup"><span data-stu-id="1d261-261">5173</span></span></p></td>
<td><p><span data-ttu-id="1d261-262">68</span><span class="sxs-lookup"><span data-stu-id="1d261-262">68</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d261-263">Entités d’appartenance basées sur l’utilisateur dans toutes les salles de conversation</span><span class="sxs-lookup"><span data-stu-id="1d261-263">User-based membership entities across all chat rooms</span></span></p></td>
<td><p><span data-ttu-id="1d261-264">465,600</span><span class="sxs-lookup"><span data-stu-id="1d261-264">465,600</span></span></p></td>
<td><p><span data-ttu-id="1d261-265">77,600</span><span class="sxs-lookup"><span data-stu-id="1d261-265">77,600</span></span></p></td>
<td><p><span data-ttu-id="1d261-266">72,000</span><span class="sxs-lookup"><span data-stu-id="1d261-266">72,000</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d261-267">Utilisateurs et groupes d’utilisateurs dans chaque liste de gestionnaires, de présentateurs et d’étendue de la salle de conversation</span><span class="sxs-lookup"><span data-stu-id="1d261-267">Users and user groups in each chat room's manager, presenter, and scope lists</span></span></p></td>
<td><p><span data-ttu-id="1d261-268">6</span><span class="sxs-lookup"><span data-stu-id="1d261-268">6</span></span></p></td>
<td><p><span data-ttu-id="1d261-269">6</span><span class="sxs-lookup"><span data-stu-id="1d261-269">6</span></span></p></td>
<td><p><span data-ttu-id="1d261-270">6</span><span class="sxs-lookup"><span data-stu-id="1d261-270">6</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d261-271">Utilisateurs et groupes d’utilisateurs dans toutes les listes de gestionnaires, de présentateurs et d’étendue de salles de conversation</span><span class="sxs-lookup"><span data-stu-id="1d261-271">Users and user groups across all chat rooms' manager, presenter, and scope lists</span></span></p></td>
<td><p><span data-ttu-id="1d261-272">192,000</span><span class="sxs-lookup"><span data-stu-id="1d261-272">192,000</span></span></p></td>
<td><p><span data-ttu-id="1d261-273">6400</span><span class="sxs-lookup"><span data-stu-id="1d261-273">6400</span></span></p></td>
<td><p><span data-ttu-id="1d261-274">60</span><span class="sxs-lookup"><span data-stu-id="1d261-274">60</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d261-275">Entrées de contrôle d’accès</span><span class="sxs-lookup"><span data-stu-id="1d261-275">Access control entries</span></span></p></td>
<td><p><span data-ttu-id="1d261-276">704,160</span><span class="sxs-lookup"><span data-stu-id="1d261-276">704,160</span></span></p></td>
<td><p><span data-ttu-id="1d261-277">26,768</span><span class="sxs-lookup"><span data-stu-id="1d261-277">26,768</span></span></p></td>
<td><p><span data-ttu-id="1d261-278">160</span><span class="sxs-lookup"><span data-stu-id="1d261-278">160</span></span></p></td>
<td><p><span data-ttu-id="1d261-279">731,088</span><span class="sxs-lookup"><span data-stu-id="1d261-279">731,088</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d261-280">Nombre maximum d’entrées de contrôle d’accès</span><span class="sxs-lookup"><span data-stu-id="1d261-280">Maximum access control entries</span></span></p></td>
<td></td>
<td></td>
<td></td>
<td><p><span data-ttu-id="1d261-281">2,000,000</span><span class="sxs-lookup"><span data-stu-id="1d261-281">2,000,000</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1d261-282">Dans l’exemple ci-dessus, lorsque vous déployez les serveurs de chat permanent conformément aux recommandations recommandées, les utilisateurs peuvent gérer jusqu’à 80 000 utilisateurs actifs sur un pool de quatre serveurs avec conformité activée.</span><span class="sxs-lookup"><span data-stu-id="1d261-282">In the preceding sample, when you deploy the Persistent Chat Servers according to the recommended guidelines, they can handle up to 80,000 active users across a four-server pool with compliance enabled.</span></span>

<span data-ttu-id="1d261-283">Cet exemple indique les catégories des salles de conversation : petite (30 utilisateurs actifs à tout moment), moyenne (150 utilisateurs actifs) et grande (16 000 utilisateurs actifs).</span><span class="sxs-lookup"><span data-stu-id="1d261-283">This sample shows chat rooms categorized as small (30 active users at any given time), medium (150 active users), and large (16,000 active users).</span></span> <span data-ttu-id="1d261-284">Le nombre de salles de conversation d’une taille précise est calculé en fonction du nombre total de :</span><span class="sxs-lookup"><span data-stu-id="1d261-284">The number of chat rooms of a certain size is computed based on the total number of:</span></span>

  - <span data-ttu-id="1d261-285">D’utilisateurs actifs dans le système</span><span class="sxs-lookup"><span data-stu-id="1d261-285">Active users in the system</span></span>

  - <span data-ttu-id="1d261-286">D’utilisateurs actifs dans les salles de conversation de la taille donnée</span><span class="sxs-lookup"><span data-stu-id="1d261-286">Active users in chat rooms of the given size</span></span>

  - <span data-ttu-id="1d261-287">Des salles de conversation de la taille donnée auxquelles se joint un seul utilisateur</span><span class="sxs-lookup"><span data-stu-id="1d261-287">Chat rooms of the given size that a single user joins</span></span>

<span data-ttu-id="1d261-p111">Pour chaque salle de conversation, le tableau de planification de capacité précédent spécifie le nombre d’entrées de contrôle d’accès associées à la salle de conversation, dont les entrées affectées directement à la salle de conversation. Vous pouvez contrôler l’accès aux salles de conversation individuelles à l’aide des listes de contrôle d’accès. Vous pouvez également contrôler l’accès au niveau de la catégorie. Dans une liste de contrôle d’accès, une entrée de contrôle d’accès individuelle peut être un groupe d’utilisateurs (par exemple, un groupe de sécurité, une liste de distribution ou un utilisateur unique). Vous pouvez définir des entrées de contrôle d’accès pour les gestionnaires, présentateurs et membres de salles de conversation.</span><span class="sxs-lookup"><span data-stu-id="1d261-p111">For each chat room, the preceding capacity planning table specifies the number of access control entries that are associated with the chat room, including entries that are assigned directly to the chat room. You can control access to individual chat rooms by using access control lists (ACLs). You can also control access at the category level. In an ACL, an individual access control entry can be either a user group—for example, a security group, a distribution list, or a single user. You can define access control entries for chat room managers, presenters, and members.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="1d261-p112">En planifiant votre stratégie de gestion des salles de conversation, gardez à l’esprit que le nombre total d’entrées de contrôle d’accès autorisées est de 2 millions. Si le nombre d’entrées de contrôle d’accès calculé dépasse 2 millions, les performances du serveur pourraient se dégrader de manière significative. Pour éviter ce problème, quand cela s’avère possible, assurez-vous que vos entrées de contrôle d’accès sont des groupes d’utilisateurs au lieu d’utilisateurs individuels.</span><span class="sxs-lookup"><span data-stu-id="1d261-p112">In planning your strategy for managing chat rooms, keep in mind that the total number of allowed access control entries is 2 million. If the calculated access control entries exceed 2 million, server performance could degrade significantly. To avoid this issue, whenever possible, be sure that your access control entries are user groups instead of individual users.</span></span>



</div>

</div>

<div>

## <a name="capacity-planning-for-managing-chat-room-access-by-invitation"></a><span data-ttu-id="1d261-296">Planification de la capacité pour gérer l’accès aux salles de conversation par invitation</span><span class="sxs-lookup"><span data-stu-id="1d261-296">Capacity Planning for Managing Chat Room Access by Invitation</span></span>

<span data-ttu-id="1d261-297">Vous pouvez utiliser le tableau de planification des capacités suivant pour comprendre le nombre d’invitations créées et stockées par le serveur Chat permanent dans la base de données de chat permanent lorsque celui-ci est configuré pour envoyer des invitations.</span><span class="sxs-lookup"><span data-stu-id="1d261-297">You can use the following capacity planning table to understand the number of invitations that Persistent Chat Server creates and stores in the Persistent Chat database when it is configured to send invitations.</span></span> <span data-ttu-id="1d261-298">Pour gérer les invitations à une catégorie, vous devez utiliser la page **paramètres des catégories de salle de conversation** du panneau de configuration de Lync Server, ou à l’aide de l’applet de commande Windows PowerShell **Set-csPersistentChatCategory**.</span><span class="sxs-lookup"><span data-stu-id="1d261-298">You manage invitations on the Category by using the **Chat Room Category settings** page in the Lync Server Control Panel, or by using the Windows PowerShell cmdlet, **set-csPersistentChatCategory**.</span></span> <span data-ttu-id="1d261-299">Vous pouvez gérer les invitations d’une salle de conversation (en fonction de ce que la catégorie autorise) à l’aide de la page de **gestion des salles** lancée par le client Lync, ou à l’aide d’une cmdlet Windows PowerShell, **Set-csPersistentChatRoom**.</span><span class="sxs-lookup"><span data-stu-id="1d261-299">You can manage invitations on a chat room (in line with what the category allows) by using the **Room Management** page launched from the Lync client, or by using a Windows PowerShell cmdlet, **set-csPersistentChatRoom**.</span></span>

<span data-ttu-id="1d261-300">Les exemples de données du tableau ci-après supposent que l’option **Invitations** est définie sur **Oui** dans la page **Paramètres de la salle de conversation** pour 50 % de toutes les salles de conversation.</span><span class="sxs-lookup"><span data-stu-id="1d261-300">The sample data in the following table assumes that, on the **Chat room settings** page for 50 percent of all chat rooms, the **Invitations** option is set to **Yes**.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="1d261-301">Si la valeur calculée du nombre d’invitations générée par le serveur dépasse 1 million, les performances du serveur pourraient se dégrader de manière significative.</span><span class="sxs-lookup"><span data-stu-id="1d261-301">If the calculated value for the number of invitations that is generated by the server exceeds 1 million, server performance could degrade significantly.</span></span> <span data-ttu-id="1d261-302">Pour éviter ce problème, assurez-vous de réduire le nombre de salles de conversation configurées pour envoyer des invitations ou limiter le nombre d’utilisateurs qui peuvent rejoindre des salles de conversation configurées pour envoyer des invitations.</span><span class="sxs-lookup"><span data-stu-id="1d261-302">To avoid this issue, be sure that you minimize the number of chat rooms that are configured to send invitations or restrict the number of users who can join chat rooms that have been configured to send invitations.</span></span>



</div>

### <a name="chat-room-access-by-invitation-sample"></a><span data-ttu-id="1d261-303">Exemple d’accès à une salle de conversation par exemple d’invitation</span><span class="sxs-lookup"><span data-stu-id="1d261-303">Chat Room Access by Invitation Sample</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="1d261-304">Salles de conversation de petite taille</span><span class="sxs-lookup"><span data-stu-id="1d261-304">Small Chat Rooms</span></span></th>
<th><span data-ttu-id="1d261-305">Salles de conversation de taille moyenne</span><span class="sxs-lookup"><span data-stu-id="1d261-305">Medium Chat Rooms</span></span></th>
<th><span data-ttu-id="1d261-306">Salles de conversation de grande taille</span><span class="sxs-lookup"><span data-stu-id="1d261-306">Large Chat Rooms</span></span></th>
<th><span data-ttu-id="1d261-307">Total</span><span class="sxs-lookup"><span data-stu-id="1d261-307">Total</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1d261-308">Utilisateurs pouvant accéder à la salle de conversation</span><span class="sxs-lookup"><span data-stu-id="1d261-308">Users who can access chat room</span></span></p></td>
<td><p><span data-ttu-id="1d261-309">30 par salle</span><span class="sxs-lookup"><span data-stu-id="1d261-309">30 per room</span></span></p></td>
<td><p><span data-ttu-id="1d261-310">150 par salle</span><span class="sxs-lookup"><span data-stu-id="1d261-310">150 per room</span></span></p></td>
<td><p><span data-ttu-id="1d261-311">16 000 par salle</span><span class="sxs-lookup"><span data-stu-id="1d261-311">16,000 per room</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d261-312">Pourcentage de salles qui ont des invitations</span><span class="sxs-lookup"><span data-stu-id="1d261-312">Percentage of rooms that have invitations</span></span></p></td>
<td><p><span data-ttu-id="1d261-313">50%</span><span class="sxs-lookup"><span data-stu-id="1d261-313">50%</span></span></p></td>
<td><p><span data-ttu-id="1d261-314">50%</span><span class="sxs-lookup"><span data-stu-id="1d261-314">50%</span></span></p></td>
<td><p><span data-ttu-id="1d261-315">50%</span><span class="sxs-lookup"><span data-stu-id="1d261-315">50%</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d261-316">Salles de conversation configurées pour envoyer des invitations</span><span class="sxs-lookup"><span data-stu-id="1d261-316">Chat rooms configured to send invitations</span></span></p></td>
<td><p><span data-ttu-id="1d261-317"><em>16,000</em></span><span class="sxs-lookup"><span data-stu-id="1d261-317"><em>16,000</em></span></span></p></td>
<td><p><span data-ttu-id="1d261-318"><em>533</em></span><span class="sxs-lookup"><span data-stu-id="1d261-318"><em>533</em></span></span></p></td>
<td><p><span data-ttu-id="1d261-319"><em>5</em></span><span class="sxs-lookup"><span data-stu-id="1d261-319"><em>5</em></span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d261-320">Utilisateurs pouvant accéder à la salle de conversation</span><span class="sxs-lookup"><span data-stu-id="1d261-320">Users who can access the chat room</span></span></p></td>
<td><p><span data-ttu-id="1d261-321"><em>60</em></span><span class="sxs-lookup"><span data-stu-id="1d261-321"><em>60</em></span></span></p></td>
<td><p><span data-ttu-id="1d261-322"><em>225</em></span><span class="sxs-lookup"><span data-stu-id="1d261-322"><em>225</em></span></span></p></td>
<td><p><span data-ttu-id="1d261-323"><em>16,000</em></span><span class="sxs-lookup"><span data-stu-id="1d261-323"><em>16,000</em></span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d261-324">Invitations générées par un serveur de chat permanent</span><span class="sxs-lookup"><span data-stu-id="1d261-324">Invitations generated by Persistent Chat Server</span></span></p></td>
<td><p><span data-ttu-id="1d261-325">960,000</span><span class="sxs-lookup"><span data-stu-id="1d261-325">960,000</span></span></p></td>
<td><p><span data-ttu-id="1d261-326">120,000</span><span class="sxs-lookup"><span data-stu-id="1d261-326">120,000</span></span></p></td>
<td><p><span data-ttu-id="1d261-327">80,000</span><span class="sxs-lookup"><span data-stu-id="1d261-327">80,000</span></span></p></td>
<td><p><span data-ttu-id="1d261-328">1,160,000</span><span class="sxs-lookup"><span data-stu-id="1d261-328">1,160,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d261-329">Nombre maximal autorisé d’invitations</span><span class="sxs-lookup"><span data-stu-id="1d261-329">Maximum allowable number of invitations</span></span></p></td>
<td></td>
<td></td>
<td></td>
<td><p><span data-ttu-id="1d261-330">2,000,000</span><span class="sxs-lookup"><span data-stu-id="1d261-330">2,000,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d261-331">Modèle 1 - Démarrer avec le nombre attendu de messages par salle par jour</span><span class="sxs-lookup"><span data-stu-id="1d261-331">Model 1 - Start with expected number of messages per room per day</span></span></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d261-332">Taux de conversation par salle (par jour)</span><span class="sxs-lookup"><span data-stu-id="1d261-332">Chat Rate Per Room (per day)</span></span></p></td>
<td><p><span data-ttu-id="1d261-333">50</span><span class="sxs-lookup"><span data-stu-id="1d261-333">50</span></span></p></td>
<td><p><span data-ttu-id="1d261-334">500</span><span class="sxs-lookup"><span data-stu-id="1d261-334">500</span></span></p></td>
<td><p><span data-ttu-id="1d261-335">100</span><span class="sxs-lookup"><span data-stu-id="1d261-335">100</span></span></p></td>
<td><p><span data-ttu-id="1d261-336">650</span><span class="sxs-lookup"><span data-stu-id="1d261-336">650</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d261-337">Taux de conversation (par seconde) de toutes les salles</span><span class="sxs-lookup"><span data-stu-id="1d261-337">Chat rate (per second) across all rooms</span></span></p></td>
<td><p><span data-ttu-id="1d261-338">55.56</span><span class="sxs-lookup"><span data-stu-id="1d261-338">55.56</span></span></p></td>
<td><p><span data-ttu-id="1d261-339">18.52</span><span class="sxs-lookup"><span data-stu-id="1d261-339">18.52</span></span></p></td>
<td><p><span data-ttu-id="1d261-340">0.03</span><span class="sxs-lookup"><span data-stu-id="1d261-340">0.03</span></span></p></td>
<td><p><span data-ttu-id="1d261-341">74</span><span class="sxs-lookup"><span data-stu-id="1d261-341">74</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d261-342">Modèle 2 - Démarrer avec le nombre de messages publiés par utilisateur par jour</span><span class="sxs-lookup"><span data-stu-id="1d261-342">Model 2 - Start with number of messages posted per user per day</span></span></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d261-343">Taux de conversation par utilisateur par jour</span><span class="sxs-lookup"><span data-stu-id="1d261-343">Chat rate per user per day</span></span></p></td>
<td><p><span data-ttu-id="1d261-344">0,15</span><span class="sxs-lookup"><span data-stu-id="1d261-344">15</span></span></p></td>
<td><p><span data-ttu-id="1d261-345">5</span><span class="sxs-lookup"><span data-stu-id="1d261-345">5</span></span></p></td>
<td><p><span data-ttu-id="1d261-346">0.1</span><span class="sxs-lookup"><span data-stu-id="1d261-346">0.1</span></span></p></td>
<td><p><span data-ttu-id="1d261-347">CX3-20</span><span class="sxs-lookup"><span data-stu-id="1d261-347">20</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d261-348">Taux de conversation par salle (par jour)</span><span class="sxs-lookup"><span data-stu-id="1d261-348">Chat rate per room (per day)</span></span></p></td>
<td><p><span data-ttu-id="1d261-349">38</span><span class="sxs-lookup"><span data-stu-id="1d261-349">38</span></span></p></td>
<td><p><span data-ttu-id="1d261-350">375</span><span class="sxs-lookup"><span data-stu-id="1d261-350">375</span></span></p></td>
<td><p><span data-ttu-id="1d261-351">800</span><span class="sxs-lookup"><span data-stu-id="1d261-351">800</span></span></p></td>
<td><p><span data-ttu-id="1d261-352">1,213</span><span class="sxs-lookup"><span data-stu-id="1d261-352">1,213</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d261-353">Taux de conversation (par seconde) de toutes les salles</span><span class="sxs-lookup"><span data-stu-id="1d261-353">Chat rate (per second) across all rooms</span></span></p></td>
<td><p><span data-ttu-id="1d261-354">41.67</span><span class="sxs-lookup"><span data-stu-id="1d261-354">41.67</span></span></p></td>
<td><p><span data-ttu-id="1d261-355">13.89</span><span class="sxs-lookup"><span data-stu-id="1d261-355">13.89</span></span></p></td>
<td><p><span data-ttu-id="1d261-356">0.28</span><span class="sxs-lookup"><span data-stu-id="1d261-356">0.28</span></span></p></td>
<td><p><span data-ttu-id="1d261-357">56</span><span class="sxs-lookup"><span data-stu-id="1d261-357">56</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="persistent-chat-server-performance-user-model"></a><span data-ttu-id="1d261-358">Modèle d’utilisateur de performance serveur Chat permanent</span><span class="sxs-lookup"><span data-stu-id="1d261-358">Persistent Chat Server Performance User Model</span></span>

<span data-ttu-id="1d261-359">Le tableau suivant décrit le modèle utilisateur pour le serveur de chat permanent.</span><span class="sxs-lookup"><span data-stu-id="1d261-359">The following table describes the user model for Persistent Chat Server.</span></span> <span data-ttu-id="1d261-360">Il fournit les bases des conditions de planification de la capacité requises et représente une organisation type avec 80 000 utilisateurs simultanés sur quatre serveurs.</span><span class="sxs-lookup"><span data-stu-id="1d261-360">It provides the basis for the capacity planning requirements and represents a typical organization with 80,000 concurrent users on four servers.</span></span>

### <a name="persistent-chat-server-performance-user-model"></a><span data-ttu-id="1d261-361">Modèle d’utilisateur de performance serveur Chat permanent</span><span class="sxs-lookup"><span data-stu-id="1d261-361">Persistent Chat Server Performance User Model</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1d261-362">Nombre d’utilisateurs actifs connectés</span><span class="sxs-lookup"><span data-stu-id="1d261-362">Number of active users connected</span></span></p></td>
<td><p><span data-ttu-id="1d261-363">80,000</span><span class="sxs-lookup"><span data-stu-id="1d261-363">80,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d261-364">Nombre d’instances de service de chat permanent</span><span class="sxs-lookup"><span data-stu-id="1d261-364">Number of Persistent Chat Server service instances</span></span></p></td>
<td><p><span data-ttu-id="1d261-365">4</span><span class="sxs-lookup"><span data-stu-id="1d261-365">4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d261-366">Taille des petites salles de conversation</span><span class="sxs-lookup"><span data-stu-id="1d261-366">Size of small chat rooms</span></span></p></td>
<td><p><span data-ttu-id="1d261-367">30 utilisateurs</span><span class="sxs-lookup"><span data-stu-id="1d261-367">30 users</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d261-368">Taille des moyennes salles de conversation</span><span class="sxs-lookup"><span data-stu-id="1d261-368">Size of medium chat rooms</span></span></p></td>
<td><p><span data-ttu-id="1d261-369">150 utilisateurs</span><span class="sxs-lookup"><span data-stu-id="1d261-369">150 users</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d261-370">Taille des grandes salles de conversation</span><span class="sxs-lookup"><span data-stu-id="1d261-370">Size of large chat rooms</span></span></p></td>
<td><p><span data-ttu-id="1d261-371">16 000 utilisateurs</span><span class="sxs-lookup"><span data-stu-id="1d261-371">16,000 users</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d261-372">Nombre total de salles de conversation</span><span class="sxs-lookup"><span data-stu-id="1d261-372">Total number of chat rooms</span></span></p></td>
<td><p><span data-ttu-id="1d261-373">33,077</span><span class="sxs-lookup"><span data-stu-id="1d261-373">33,077</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d261-374">Nombre de petites salles de conversation</span><span class="sxs-lookup"><span data-stu-id="1d261-374">Number of small chat rooms</span></span></p></td>
<td><p><span data-ttu-id="1d261-375">32,000</span><span class="sxs-lookup"><span data-stu-id="1d261-375">32,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d261-376">Nombre de moyennes salles de conversation</span><span class="sxs-lookup"><span data-stu-id="1d261-376">Number of medium chat rooms</span></span></p></td>
<td><p><span data-ttu-id="1d261-377">1,067</span><span class="sxs-lookup"><span data-stu-id="1d261-377">1,067</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d261-378">Nombre de grandes salles de conversation</span><span class="sxs-lookup"><span data-stu-id="1d261-378">Number of large chat rooms</span></span></p></td>
<td><p><span data-ttu-id="1d261-379">0,10</span><span class="sxs-lookup"><span data-stu-id="1d261-379">10</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d261-380">Nombre total de salles de conversation par utilisateur</span><span class="sxs-lookup"><span data-stu-id="1d261-380">Total number of chat rooms per user</span></span></p></td>
<td><p><span data-ttu-id="1d261-381">Seiz</span><span class="sxs-lookup"><span data-stu-id="1d261-381">16</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d261-382">Nombre total de petites salles de conversation par utilisateur</span><span class="sxs-lookup"><span data-stu-id="1d261-382">Number of small chat rooms per user</span></span></p></td>
<td><p><span data-ttu-id="1d261-383">midi</span><span class="sxs-lookup"><span data-stu-id="1d261-383">12</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d261-384">Nombre total de moyennes salles de conversation par utilisateur</span><span class="sxs-lookup"><span data-stu-id="1d261-384">Number of medium chat rooms per user</span></span></p></td>
<td><p><span data-ttu-id="1d261-385">2</span><span class="sxs-lookup"><span data-stu-id="1d261-385">2</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d261-386">Nombre total de grandes salles de conversation par utilisateur</span><span class="sxs-lookup"><span data-stu-id="1d261-386">Number of large chat rooms per user</span></span></p></td>
<td><p><span data-ttu-id="1d261-387">2</span><span class="sxs-lookup"><span data-stu-id="1d261-387">2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d261-388">Nombre de salles jointes par utilisateur</span><span class="sxs-lookup"><span data-stu-id="1d261-388">Number of rooms joined per user</span></span></p></td>
<td><p><span data-ttu-id="1d261-389">24</span><span class="sxs-lookup"><span data-stu-id="1d261-389">24</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d261-390">Taux maximal d’utilisateurs joints</span><span class="sxs-lookup"><span data-stu-id="1d261-390">Peak join rate</span></span></p></td>
<td><p><span data-ttu-id="1d261-391">10/seconde</span><span class="sxs-lookup"><span data-stu-id="1d261-391">10/second</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d261-392">Taux de conversation total</span><span class="sxs-lookup"><span data-stu-id="1d261-392">Total chat rate</span></span></p></td>
<td><p><span data-ttu-id="1d261-393">24/seconde</span><span class="sxs-lookup"><span data-stu-id="1d261-393">24/second</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d261-394">Taux de conversation pour les petites salles de conversation</span><span class="sxs-lookup"><span data-stu-id="1d261-394">Chat rate for small chat rooms</span></span></p></td>
<td><p><span data-ttu-id="1d261-395">22.22/second</span><span class="sxs-lookup"><span data-stu-id="1d261-395">22.22/second</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d261-396">Taux de conversation pour les moyennes salles de conversation</span><span class="sxs-lookup"><span data-stu-id="1d261-396">Chat rate for medium chat rooms</span></span></p></td>
<td><p><span data-ttu-id="1d261-397">1.67/second</span><span class="sxs-lookup"><span data-stu-id="1d261-397">1.67/second</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d261-398">Taux de conversation pour les grandes salles de conversation</span><span class="sxs-lookup"><span data-stu-id="1d261-398">Chat rate for large chat rooms</span></span></p></td>
<td><p><span data-ttu-id="1d261-399">~0.15/second</span><span class="sxs-lookup"><span data-stu-id="1d261-399">~0.15/second</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d261-400">Pourcentage des salles de conversation configurées pour les invitations</span><span class="sxs-lookup"><span data-stu-id="1d261-400">Percentage of chat rooms configured for invitations</span></span></p></td>
<td><p><span data-ttu-id="1d261-401">50%</span><span class="sxs-lookup"><span data-stu-id="1d261-401">50%</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d261-402">Pourcentage des appartenances directes</span><span class="sxs-lookup"><span data-stu-id="1d261-402">Percentage of direct memberships</span></span></p></td>
<td><p><span data-ttu-id="1d261-403">50%</span><span class="sxs-lookup"><span data-stu-id="1d261-403">50%</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d261-404">Pourcentage des appartenances aux groupes</span><span class="sxs-lookup"><span data-stu-id="1d261-404">Percentage of group memberships</span></span></p></td>
<td><p><span data-ttu-id="1d261-405">50%</span><span class="sxs-lookup"><span data-stu-id="1d261-405">50%</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d261-406">Nombre moyen d’affiliations d’ancêtre dans les services de domaine Active Directory</span><span class="sxs-lookup"><span data-stu-id="1d261-406">Average number of ancestor affiliations in Active Directory Domain Services</span></span></p></td>
<td><p><span data-ttu-id="1d261-407">100 - 200</span><span class="sxs-lookup"><span data-stu-id="1d261-407">100 - 200</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d261-408">Nombre de contacts abonnés par utilisateur</span><span class="sxs-lookup"><span data-stu-id="1d261-408">Number of subscribed contacts per user</span></span></p></td>
<td><p><span data-ttu-id="1d261-409">80</span><span class="sxs-lookup"><span data-stu-id="1d261-409">80</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d261-410">Nombre moyen de points de terminaison par utilisateur</span><span class="sxs-lookup"><span data-stu-id="1d261-410">Average number of endpoints per user</span></span></p></td>
<td><p><span data-ttu-id="1d261-411">1.5</span><span class="sxs-lookup"><span data-stu-id="1d261-411">1.5</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d261-412">Nombre moyen de salles de conversation visibles par point de terminaison</span><span class="sxs-lookup"><span data-stu-id="1d261-412">Average number of visible chat rooms per endpoint</span></span></p></td>
<td><p><span data-ttu-id="1d261-413">1.5</span><span class="sxs-lookup"><span data-stu-id="1d261-413">1.5</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d261-414">Nombre moyen de salles de conversation visibles par utilisateur</span><span class="sxs-lookup"><span data-stu-id="1d261-414">Average number of visible chat rooms per user</span></span></p></td>
<td><p><span data-ttu-id="1d261-415">2,25 (50 % pour une salle et 50 % pour 2 salles) ; jusqu’à 6 salles ouvertes, une par moniteur</span><span class="sxs-lookup"><span data-stu-id="1d261-415">2.25 (50% for 1 room and 50% for 2 rooms); Up to 6 rooms open, one per monitor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d261-416">Nombre de participants interrogés par intervalle</span><span class="sxs-lookup"><span data-stu-id="1d261-416">Number of participants polled per interval</span></span></p></td>
<td><p><span data-ttu-id="1d261-417">25 par salle de conversation visible</span><span class="sxs-lookup"><span data-stu-id="1d261-417">25 per visible chat room</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d261-418">Durée de la fréquence d’interrogation</span><span class="sxs-lookup"><span data-stu-id="1d261-418">Length of polling interval</span></span></p></td>
<td><p><span data-ttu-id="1d261-419">5 minutes</span><span class="sxs-lookup"><span data-stu-id="1d261-419">5 minutes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d261-420">Nombre de participants interrogés par seconde</span><span class="sxs-lookup"><span data-stu-id="1d261-420">Number of participants polled per second</span></span></p></td>
<td><p><span data-ttu-id="1d261-421">15,000</span><span class="sxs-lookup"><span data-stu-id="1d261-421">15,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d261-422">Nombre de changements du statut de présence par heure et par utilisateur</span><span class="sxs-lookup"><span data-stu-id="1d261-422">Number of presence changes per hour per user</span></span></p></td>
<td><p><span data-ttu-id="1d261-423">6</span><span class="sxs-lookup"><span data-stu-id="1d261-423">6</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d261-424">Nombre de changements du statut de présence par seconde</span><span class="sxs-lookup"><span data-stu-id="1d261-424">Number of presence changes per second</span></span></p></td>
<td><p><span data-ttu-id="1d261-425">133.33</span><span class="sxs-lookup"><span data-stu-id="1d261-425">133.33</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="1d261-426">


</div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1d261-426">


</div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

