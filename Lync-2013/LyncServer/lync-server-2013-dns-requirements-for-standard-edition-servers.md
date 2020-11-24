---
title: 'Lync Server 2013 : configuration requise pour DNS pour les serveurs Standard Edition Server'
description: 'Lync Server 2013 : configuration DNS requise pour les serveurs Standard Edition Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS requirements for Standard Edition servers
ms:assetid: 3d6bbe65-e7ce-491b-a0bd-d2f7197f240d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425900(v=OCS.15)
ms:contentKeyID: 48183920
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: cc93549e07fb82304ad76b051730eab972530764
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49393984"
---
# <a name="dns-requirements-for-standard-edition-servers-in-lync-server-2013"></a><span data-ttu-id="e3820-103">Configuration DNS requise pour les serveurs Standard Edition Server dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e3820-103">DNS requirements for Standard Edition servers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e3820-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e3820-104">

<span> </span></span></span>

<span data-ttu-id="e3820-105">_**Dernière modification de la rubrique :** 2012-06-19_</span><span class="sxs-lookup"><span data-stu-id="e3820-105">_**Topic Last Modified:** 2012-06-19_</span></span>

<span data-ttu-id="e3820-106">Cette section décrit les enregistrements DNS (Domain Name System) requis pour le déploiement de serveurs Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="e3820-106">This section describes the Domain Name System (DNS) records that are required for deployment of Standard Edition servers.</span></span>

<div>

## <a name="dns-records-for-standard-edition-servers"></a><span data-ttu-id="e3820-107">Enregistrements DNS pour les serveurs Standard Edition Server</span><span class="sxs-lookup"><span data-stu-id="e3820-107">DNS Records for Standard Edition Servers</span></span>

<span data-ttu-id="e3820-108">Le tableau suivant indique les exigences DNS pour le déploiement de Lync Server 2013 Standard Edition Server.</span><span class="sxs-lookup"><span data-stu-id="e3820-108">The following table specifies DNS requirements for Lync Server 2013 Standard Edition server deployment.</span></span>

### <a name="dns-requirements-for-a-standard-edition-server"></a><span data-ttu-id="e3820-109">Configuration DNS requise pour un serveur Standard Edition Server</span><span class="sxs-lookup"><span data-stu-id="e3820-109">DNS Requirements for a Standard Edition Server</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e3820-110">Scénario de déploiement</span><span class="sxs-lookup"><span data-stu-id="e3820-110">Deployment scenario</span></span></th>
<th><span data-ttu-id="e3820-111">Enregistrement DNS requis</span><span class="sxs-lookup"><span data-stu-id="e3820-111">DNS requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e3820-112">serveur Standard Edition</span><span class="sxs-lookup"><span data-stu-id="e3820-112">Standard Edition server</span></span></p></td>
<td><p><span data-ttu-id="e3820-113">Un enregistrement interne A qui associe le nom de domaine complet (FQDN) du serveur à son adresse IP.</span><span class="sxs-lookup"><span data-stu-id="e3820-113">An internal A record that resolves the fully qualified domain name (FQDN) of the server to its IP address.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3820-114">Connexion automatique au client</span><span class="sxs-lookup"><span data-stu-id="e3820-114">Automatic client sign-in</span></span></p></td>
<td><p><span data-ttu-id="e3820-115">Pour chaque domaine SIP pris en charge, un enregistrement SRV pour _sipinternaltls. _ TCP. domaine &gt; sur le port 5061 qui correspond au nom de domaine complet du serveur Standard Edition qui authentifie et redirige les demandes de connexion du client.</span><span class="sxs-lookup"><span data-stu-id="e3820-115">For each supported SIP domain, an SRV record for _sipinternaltls._tcp.&lt;domain&gt; over port 5061 that maps to the FQDN of the Standard Edition server that authenticates and redirects client requests for sign-in.</span></span> <span data-ttu-id="e3820-116">Pour plus d’informations, voir <a href="lync-server-2013-dns-requirements-for-automatic-client-sign-in.md">configuration DNS requise pour la connexion automatique au client dans Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="e3820-116">For details, see <a href="lync-server-2013-dns-requirements-for-automatic-client-sign-in.md">DNS requirements for automatic client sign-in in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3820-117">Découverte du service Web de mise à jour d’appareil par des appareils de communications unifiées (UC)</span><span class="sxs-lookup"><span data-stu-id="e3820-117">Device Update Web service discovery by unified communications (UC) devices</span></span></p></td>
<td><p><span data-ttu-id="e3820-118">Un enregistrement A interne du nom ucupdates-r2. &lt; Domaine SIP résolu &gt; sur l’adresse IP du service Web de mise à jour des appareils d’hébergement Standard Edition Server.</span><span class="sxs-lookup"><span data-stu-id="e3820-118">An internal A record with the name ucupdates-r2.&lt;SIP domain&gt; that resolves to the IP address of the Standard Edition server hosting Device Update Web service.</span></span> <span data-ttu-id="e3820-119">Dans le cas où un périphérique UC est activé, mais qu’aucun utilisateur ne s’est connecté à l’appareil, l’enregistrement A permet à l’appareil de détecter le service Web de mise à jour de l’appareil d’hébergement du serveur et d’obtenir les mises à jour.</span><span class="sxs-lookup"><span data-stu-id="e3820-119">In the situation where a UC device is turned on, but a user has never logged into the device, the A record allows the device to discover the server hosting Device Update Web service and obtain updates.</span></span> <span data-ttu-id="e3820-120">Les périphériques peuvent autrement se procurer ces informations via une mise en service de la bande entrante la première fois qu’un utilisateur se connecte.</span><span class="sxs-lookup"><span data-stu-id="e3820-120">Otherwise, devices obtain the server information though in-band provisioning the first time a user logs in.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3820-121">Proxy inverse pour la prise en charge du trafic HTTP</span><span class="sxs-lookup"><span data-stu-id="e3820-121">A reverse proxy to support HTTP traffic</span></span></p></td>
<td><p><span data-ttu-id="e3820-122">Un enregistrement A externe qui résout le nom de domaine complet de la batterie de serveurs Web externe à l’adresse IP externe du proxy inverse.</span><span class="sxs-lookup"><span data-stu-id="e3820-122">An external A record that resolves the external web farm FQDN to the external IP address of the reverse proxy.</span></span> <span data-ttu-id="e3820-123">Les clients et les appareils UC utilisent cet enregistrement pour se connecter au proxy inverse.</span><span class="sxs-lookup"><span data-stu-id="e3820-123">Clients and UC devices use this record to connect to the reverse proxy.</span></span> <span data-ttu-id="e3820-124">Pour plus d’informations, reportez-vous à la rubrique <a href="lync-server-2013-determine-dns-requirements.md">déterminer les exigences DNS pour Lync Server 2013</a> dans la documentation de planification.</span><span class="sxs-lookup"><span data-stu-id="e3820-124">For details, see <a href="lync-server-2013-determine-dns-requirements.md">Determine DNS requirements for Lync Server 2013</a> in the Planning documentation.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="e3820-125">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e3820-125">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

