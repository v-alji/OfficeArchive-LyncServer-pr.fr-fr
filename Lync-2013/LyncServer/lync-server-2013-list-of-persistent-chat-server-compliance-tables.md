---
title: 'Lync Server 2013 : Liste des tables de conformité avec le serveur de conversation permanente'
description: 'Lync Server 2013 : liste des tables de compatibilité de serveur Chat permanent.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: List of Persistent Chat Server compliance tables
ms:assetid: 8563446e-90cc-47cc-8a8e-4883decfe195
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ215878(v=OCS.15)
ms:contentKeyID: 48706007
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 47cb28a0ca4180327c2adc48d80e9e41171a7bfc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426577"
---
# <a name="list-of-persistent-chat-server-compliance-tables-in-lync-server-2013"></a><span data-ttu-id="1d981-103">Liste des tables de conformité avec le serveur de conversation permanente dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1d981-103">List of Persistent Chat Server compliance tables in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1d981-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1d981-104">

<span> </span></span></span>

<span data-ttu-id="1d981-105">_**Dernière modification de la rubrique :** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="1d981-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="1d981-106">Le schéma de base de données de conformité des conversations permanentes se compose des tables suivantes.</span><span class="sxs-lookup"><span data-stu-id="1d981-106">The Persistent Chat compliance database schema consists of the following tables.</span></span>

<div>

## <a name="list-of-persistent-chat-server-compliance-tables"></a><span data-ttu-id="1d981-107">Liste des tables de compatibilité de serveur Chat permanent</span><span class="sxs-lookup"><span data-stu-id="1d981-107">List of Persistent Chat Server Compliance Tables</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1d981-108">Table</span><span class="sxs-lookup"><span data-stu-id="1d981-108">Table</span></span></th>
<th><span data-ttu-id="1d981-109">Description</span><span class="sxs-lookup"><span data-stu-id="1d981-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1d981-110"><a href="lync-server-2013-tblcompliancedata.md">tblComplianceData dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="1d981-110"><a href="lync-server-2013-tblcompliancedata.md">tblComplianceData in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="1d981-111">Contient les événements de conformité qui n’ont pas encore été traités par l’adaptateur configuré.</span><span class="sxs-lookup"><span data-stu-id="1d981-111">Contains the compliance events that have not yet been processed by the configured adapter.</span></span></p>
<p><span data-ttu-id="1d981-112">Le tableau suivant contient des événements liés à des discussions permanentes, tels que des messages de discussion et des téléchargements de fichiers.</span><span class="sxs-lookup"><span data-stu-id="1d981-112">This table includes Persistent Chat-related events, such as chat messages and file downloads.</span></span> <span data-ttu-id="1d981-113">(Les événements de participants sont suivis par la table tblComplianceParticipant.)</span><span class="sxs-lookup"><span data-stu-id="1d981-113">(Participant events are tracked by the tblComplianceParticipant table.)</span></span></p>
<p><span data-ttu-id="1d981-114">(Les serveurs qui ont géré les événements dans ce tableau apparaissent dans la table tblComplianceFanout.)</span><span class="sxs-lookup"><span data-stu-id="1d981-114">(The servers that processed the events in this table are listed in the tblComplianceFanout table.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d981-115"><a href="lync-server-2013-tblcompliancefanout.md">tblComplianceFanout dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="1d981-115"><a href="lync-server-2013-tblcompliancefanout.md">tblComplianceFanout in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="1d981-116">Contient les serveurs qui ont traité un événement de conformité.</span><span class="sxs-lookup"><span data-stu-id="1d981-116">Contains the servers that processed a compliance event.</span></span> <span data-ttu-id="1d981-117">Ce tableau est étroitement couplé à la table tblComplianceData.</span><span class="sxs-lookup"><span data-stu-id="1d981-117">This table is tightly coupled with the tblComplianceData table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d981-118"><a href="lync-server-2013-tblcomplianceparticipant.md">tblComplianceParticipant dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="1d981-118"><a href="lync-server-2013-tblcomplianceparticipant.md">tblComplianceParticipant in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="1d981-119">Contient les participants actuels par service de conversation et par serveur.</span><span class="sxs-lookup"><span data-stu-id="1d981-119">Contains current participants per chat service and per server.</span></span> <span data-ttu-id="1d981-120">Elle est conservée en fonction des événements de jointure et de conformité de partie reçus du service de chat permanent.</span><span class="sxs-lookup"><span data-stu-id="1d981-120">It is maintained based on join and part compliance events received from the Persistent Chat service.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d981-121"><a href="lync-server-2013-tblcompliancestate.md">tblComplianceState dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="1d981-121"><a href="lync-server-2013-tblcompliancestate.md">tblComplianceState in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="1d981-122">Contient des informations sur l’état de conformité au pool.</span><span class="sxs-lookup"><span data-stu-id="1d981-122">Contains pool-wide compliance state information.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="1d981-123">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1d981-123">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

