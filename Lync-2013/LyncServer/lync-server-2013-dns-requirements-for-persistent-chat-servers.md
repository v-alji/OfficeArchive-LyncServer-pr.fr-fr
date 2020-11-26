---
title: 'Lync Server 2013 : configuration requise pour DNS pour les serveurs de chat permanent'
description: 'Lync Server 2013 : configuration requise pour DNS pour les serveurs de chat permanent.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS requirements for Persistent Chat Servers
ms:assetid: f7531374-d7ed-4b63-ae81-02294cb4496a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205391(v=OCS.15)
ms:contentKeyID: 48185857
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 01bfc126ab588542ef5160a0eabe0c839dcf0e44
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429055"
---
# <a name="dns-requirements-for-persistent-chat-servers-in-lync-server-2013"></a><span data-ttu-id="6a388-103">Configuration DNS requise pour les serveurs de chat permanent dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6a388-103">DNS requirements for Persistent Chat Servers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6a388-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6a388-104">

<span> </span></span></span>

<span data-ttu-id="6a388-105">_**Dernière modification de la rubrique :** 2012-06-28_</span><span class="sxs-lookup"><span data-stu-id="6a388-105">_**Topic Last Modified:** 2012-06-28_</span></span>

<span data-ttu-id="6a388-106">Cette section décrit les enregistrements DNS (Domain Name System) requis pour le déploiement de serveurs de chat permanents.</span><span class="sxs-lookup"><span data-stu-id="6a388-106">This section describes the Domain Name System (DNS) records that are required for deployment of Persistent Chat Servers.</span></span>

<div>

## <a name="dns-records-for-persistent-chat-servers"></a><span data-ttu-id="6a388-107">Enregistrements DNS pour les serveurs de chat permanent</span><span class="sxs-lookup"><span data-stu-id="6a388-107">DNS Records for Persistent Chat Servers</span></span>

<span data-ttu-id="6a388-108">Le tableau suivant indique les exigences DNS pour le déploiement d’un serveur de chat permanent.</span><span class="sxs-lookup"><span data-stu-id="6a388-108">The following table specifies DNS requirements for Persistent Chat Server deployment.</span></span>

### <a name="dns-requirements-for-a-persistent-chat-server"></a><span data-ttu-id="6a388-109">Configuration DNS requise pour un serveur de chat permanent</span><span class="sxs-lookup"><span data-stu-id="6a388-109">DNS Requirements for a Persistent Chat Server</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6a388-110">Scénario de déploiement</span><span class="sxs-lookup"><span data-stu-id="6a388-110">Deployment scenario</span></span></th>
<th><span data-ttu-id="6a388-111">Enregistrement DNS requis</span><span class="sxs-lookup"><span data-stu-id="6a388-111">DNS requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6a388-112">Un serveur de chat permanent</span><span class="sxs-lookup"><span data-stu-id="6a388-112">One Persistent Chat Server</span></span></p></td>
<td><p><span data-ttu-id="6a388-113">Un enregistrement interne A qui associe le nom de domaine complet (FQDN) du serveur à son adresse IP.</span><span class="sxs-lookup"><span data-stu-id="6a388-113">An internal A record that resolves the fully qualified domain name (FQDN) of the server to its IP address.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a388-114">Pool de conversation permanente</span><span class="sxs-lookup"><span data-stu-id="6a388-114">Persistent Chat pool</span></span></p></td>
<td><p><span data-ttu-id="6a388-115">Un enregistrement A interne qui résout le nom de domaine complet (FQDN) des serveurs à son adresse IP.</span><span class="sxs-lookup"><span data-stu-id="6a388-115">An internal A record that resolves the fully qualified domain name (FQDN) of the servers to its IP address.</span></span></p>
<p><span data-ttu-id="6a388-116"><strong>Exemple</strong></span><span class="sxs-lookup"><span data-stu-id="6a388-116"><strong>Example</strong></span></span></p>
<p><span data-ttu-id="6a388-117">PersistentChatServer01.contoso.com 10.10.10.1</span><span class="sxs-lookup"><span data-stu-id="6a388-117">PersistentChatServer01.contoso.com     10.10.10.1</span></span></p>
<p><span data-ttu-id="6a388-118">PersistentChatServer02.contoso.com 10.10.10.2</span><span class="sxs-lookup"><span data-stu-id="6a388-118">PersistentChatServer02.contoso.com     10.10.10.2</span></span></p>
<p><span data-ttu-id="6a388-119">Un enregistrement A interne qui résout le nom de domaine complet (FQDN) des serveurs à son adresse IP.</span><span class="sxs-lookup"><span data-stu-id="6a388-119">An internal A record that resolves the fully qualified domain name (FQDN) of the servers to its IP address.</span></span></p>
<p><span data-ttu-id="6a388-120"><strong>Exemple</strong></span><span class="sxs-lookup"><span data-stu-id="6a388-120"><strong>Example</strong></span></span></p>
<p><span data-ttu-id="6a388-121">PersistentChatPool.contoso.com 10.10.10.1</span><span class="sxs-lookup"><span data-stu-id="6a388-121">PersistentChatPool.contoso.com    10.10.10.1</span></span></p>
<p><span data-ttu-id="6a388-122">PersistentChatPool.contoso.com 10.10.10.2</span><span class="sxs-lookup"><span data-stu-id="6a388-122">PersistentChatPool.contoso.com    10.10.10.2</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="6a388-123">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6a388-123">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

