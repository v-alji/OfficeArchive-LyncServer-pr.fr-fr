---
title: 'Lync Server 2013 : exigences DNS pour les serveurs Standard Edition'
description: 'Lync Server 2013 : exigences DNS pour les serveurs Standard Edition.'
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
# <a name="dns-requirements-for-standard-edition-servers-in-lync-server-2013"></a><span data-ttu-id="a2a0e-103">Conditions DNS requises pour les serveurs Standard Edition dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a2a0e-103">DNS requirements for Standard Edition servers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a2a0e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a2a0e-104">

<span> </span></span></span>

<span data-ttu-id="a2a0e-105">_**Rubrique dernière modification :** 19/06/2012_</span><span class="sxs-lookup"><span data-stu-id="a2a0e-105">_**Topic Last Modified:** 2012-06-19_</span></span>

<span data-ttu-id="a2a0e-106">Cette section décrit les enregistrements DNS (Domain Name System) requis pour le déploiement de serveurs Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="a2a0e-106">This section describes the Domain Name System (DNS) records that are required for deployment of Standard Edition servers.</span></span>

<div>

## <a name="dns-records-for-standard-edition-servers"></a><span data-ttu-id="a2a0e-107">Enregistrements DNS pour les serveurs Standard Edition</span><span class="sxs-lookup"><span data-stu-id="a2a0e-107">DNS Records for Standard Edition Servers</span></span>

<span data-ttu-id="a2a0e-108">Le tableau suivant spécifie les exigences DNS requises pour le déploiement de serveur Lync Server 2013 Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="a2a0e-108">The following table specifies DNS requirements for Lync Server 2013 Standard Edition server deployment.</span></span>

### <a name="dns-requirements-for-a-standard-edition-server"></a><span data-ttu-id="a2a0e-109">Conditions DNS requises pour un serveur Standard Edition Server</span><span class="sxs-lookup"><span data-stu-id="a2a0e-109">DNS Requirements for a Standard Edition Server</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a2a0e-110">Scénario de déploiement</span><span class="sxs-lookup"><span data-stu-id="a2a0e-110">Deployment scenario</span></span></th>
<th><span data-ttu-id="a2a0e-111">Enregistrement DNS requis</span><span class="sxs-lookup"><span data-stu-id="a2a0e-111">DNS requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a2a0e-112">serveur Standard Edition</span><span class="sxs-lookup"><span data-stu-id="a2a0e-112">Standard Edition server</span></span></p></td>
<td><p><span data-ttu-id="a2a0e-113">Un enregistrement interne A qui associe le nom de domaine complet (FQDN) du serveur à son adresse IP.</span><span class="sxs-lookup"><span data-stu-id="a2a0e-113">An internal A record that resolves the fully qualified domain name (FQDN) of the server to its IP address.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2a0e-114">Connectez-vous automatique au client</span><span class="sxs-lookup"><span data-stu-id="a2a0e-114">Automatic client sign-in</span></span></p></td>
<td><p><span data-ttu-id="a2a0e-115">Pour chaque domaine SIP pris en charge, un enregistrement SRV pour _sipinternaltls._tcp. &lt; domaine sur le port 5061 qui masique le nom de domaine (FQDN) du serveur Standard Edition qui authentifier et redirige les demandes de client pour &gt; la authentification.</span><span class="sxs-lookup"><span data-stu-id="a2a0e-115">For each supported SIP domain, an SRV record for _sipinternaltls._tcp.&lt;domain&gt; over port 5061 that maps to the FQDN of the Standard Edition server that authenticates and redirects client requests for sign-in.</span></span> <span data-ttu-id="a2a0e-116">Pour plus d’informations, consultez la exigences DNS pour la signature automatique du client dans <a href="lync-server-2013-dns-requirements-for-automatic-client-sign-in.md">Lync Server 2013.</a></span><span class="sxs-lookup"><span data-stu-id="a2a0e-116">For details, see <a href="lync-server-2013-dns-requirements-for-automatic-client-sign-in.md">DNS requirements for automatic client sign-in in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a2a0e-117">Découverte du service web de mise à jour des appareils par les appareils de communications unifiées</span><span class="sxs-lookup"><span data-stu-id="a2a0e-117">Device Update Web service discovery by unified communications (UC) devices</span></span></p></td>
<td><p><span data-ttu-id="a2a0e-118">Enregistrement A interne avec le nom ucupdates-r2. &lt; Domaine SIP résolu à l’adresse IP du service web de mise à jour d’appareil du serveur &gt; Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="a2a0e-118">An internal A record with the name ucupdates-r2.&lt;SIP domain&gt; that resolves to the IP address of the Standard Edition server hosting Device Update Web service.</span></span> <span data-ttu-id="a2a0e-119">Dans la situation où un appareil de UC est allumé, mais qu’un utilisateur ne s’est jamais connecté à l’appareil, l’enregistrement A permet à l’appareil de découvrir le service web de mise à jour de l’appareil hébergeant le serveur et d’obtenir des mises à jour.</span><span class="sxs-lookup"><span data-stu-id="a2a0e-119">In the situation where a UC device is turned on, but a user has never logged into the device, the A record allows the device to discover the server hosting Device Update Web service and obtain updates.</span></span> <span data-ttu-id="a2a0e-120">Les périphériques peuvent autrement se procurer ces informations via une mise en service de la bande entrante la première fois qu’un utilisateur se connecte.</span><span class="sxs-lookup"><span data-stu-id="a2a0e-120">Otherwise, devices obtain the server information though in-band provisioning the first time a user logs in.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2a0e-121">Proxy inverse pour prendre en charge le trafic HTTP</span><span class="sxs-lookup"><span data-stu-id="a2a0e-121">A reverse proxy to support HTTP traffic</span></span></p></td>
<td><p><span data-ttu-id="a2a0e-122">Enregistrement A externe qui résout le FQDN de la batterie de serveurs web externe sur l’adresse IP externe du proxy inverse.</span><span class="sxs-lookup"><span data-stu-id="a2a0e-122">An external A record that resolves the external web farm FQDN to the external IP address of the reverse proxy.</span></span> <span data-ttu-id="a2a0e-123">Les clients et appareils de lauc utilisent cet enregistrement pour se connecter au proxy inverse.</span><span class="sxs-lookup"><span data-stu-id="a2a0e-123">Clients and UC devices use this record to connect to the reverse proxy.</span></span> <span data-ttu-id="a2a0e-124">Pour plus d’informations, voir <a href="lync-server-2013-determine-dns-requirements.md">Déterminer les exigences DNS pour Lync Server 2013</a> dans la documentation de planification.</span><span class="sxs-lookup"><span data-stu-id="a2a0e-124">For details, see <a href="lync-server-2013-determine-dns-requirements.md">Determine DNS requirements for Lync Server 2013</a> in the Planning documentation.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="a2a0e-125">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a2a0e-125">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

