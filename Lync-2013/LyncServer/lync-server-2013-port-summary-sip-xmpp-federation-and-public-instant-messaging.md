---
title: Résumé de port-SIP, Fédération de XMPP et messagerie instantanée publique
description: Résumé de port-SIP, Fédération de XMPP et messagerie instantanée publique.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - SIP, XMPP federation, and public instant messaging
ms:assetid: ab05bdd6-e9b0-4b1b-9dd9-29ab88e8befe
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ618373(v=OCS.15)
ms:contentKeyID: 49105660
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7c58dbf7bdd56b4678d56f96a11332219bb40c17
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49393976"
---
# <a name="port-summary---sip-xmpp-federation-and-public-instant-messaging-in-lync-server-2013"></a><span data-ttu-id="4e421-103">Résumé de port-SIP, Fédération de XMPP et messagerie instantanée publique dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4e421-103">Port summary - SIP, XMPP federation, and public instant messaging in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4e421-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4e421-104">

<span> </span></span></span>

<span data-ttu-id="4e421-105">_**Dernière modification de la rubrique :** 2013-03-15_</span><span class="sxs-lookup"><span data-stu-id="4e421-105">_**Topic Last Modified:** 2013-03-15_</span></span>

<span data-ttu-id="4e421-106">Les exigences en matière de port, de protocole et de pare-feu pour la Fédération avec Microsoft Lync Server 2013, Lync Server 2010 et Office Communications Server sont similaires à celles du serveur Edge déployé.</span><span class="sxs-lookup"><span data-stu-id="4e421-106">Port, protocol and firewall requirements for federation with Microsoft Lync Server 2013, Lync Server 2010 and Office Communications Server are similar to those for the deployed Edge Server.</span></span> <span data-ttu-id="4e421-107">Les clients entament une communication avec le service Edge d’accès via TLS/SIP/TCP 443.</span><span class="sxs-lookup"><span data-stu-id="4e421-107">Clients initiate communication with the Access Edge service over TLS/SIP/TCP 443.</span></span> <span data-ttu-id="4e421-108">Les partenaires fédérés peuvent toutefois lancer des communications avec le service Edge d’accès via MTLS/SIP/TCP 5061.</span><span class="sxs-lookup"><span data-stu-id="4e421-108">Federated partners however, will initiate communications to the Access Edge service over MTLS/SIP/TCP 5061.</span></span>

<span data-ttu-id="4e421-109">Pour configurer votre pare-feu pour les ports et les protocoles nécessaires à la prise en charge de la connectivité de messagerie instantanée publique, notez d’abord que le protocole SIP/MTLS/TCP 5061 est bidirectionnel afin de tenir compte de la capacité des contacts du fournisseur de messagerie instantanée publique à contacter les clients Lync ou à communiquer avec des contacts de messagerie instantanée publics.</span><span class="sxs-lookup"><span data-stu-id="4e421-109">To configure your firewall for ports and protocols necessary to support public instant messaging connectivity, first note that SIP/MTLS/TCP 5061 is bidirectional to account for the ability of contacts in the public IM provider to contact Lync clients, or for Lync to contact public IM contacts.</span></span>

<span data-ttu-id="4e421-110">Windows Live Messenger peut participer aux communications audio/vidéo avec les clients Lync.</span><span class="sxs-lookup"><span data-stu-id="4e421-110">Windows Live Messenger can participate in audio/video communications with Lync clients.</span></span> <span data-ttu-id="4e421-111">Il s’agit des comptes pour le pare-feu et la configuration de protocole très similaires dont vous disposez généralement sur le pare-feu pour la prise en charge des clients Lync en tant qu’utilisateurs externes.</span><span class="sxs-lookup"><span data-stu-id="4e421-111">This accounts for the very similar firewall port and protocol configuration that you would typically have on the firewall to support Lync clients as external users.</span></span>

<div>


> [!IMPORTANT]
> <span data-ttu-id="4e421-112">Plus que jamais, Lync est un outil puissant de connexion entre organisations et de personnes dans le monde entier.</span><span class="sxs-lookup"><span data-stu-id="4e421-112">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="4e421-113">La Fédération avec Windows Live Messenger ne nécessite aucune licence d’utilisation/appareil supplémentaire au-delà de la licence d’accès client standard Lync.</span><span class="sxs-lookup"><span data-stu-id="4e421-113">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard Client Access License (CAL).</span></span> <span data-ttu-id="4e421-114">Skype Federation sera ajouté à cette liste et permettra aux utilisateurs de Lync de joindre des centaines de millions de personnes à la messagerie instantanée et à la voix.</span><span class="sxs-lookup"><span data-stu-id="4e421-114">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people with IM and voice.</span></span><BR><span data-ttu-id="4e421-115">Les contacts de la Fédération avec le client Messenger se terminent officiellement le 15 mars 2013, à l’exception de la Chine continentale.</span><span class="sxs-lookup"><span data-stu-id="4e421-115">Federation with Messenger client contacts will officially end on March 15, 2013, except for mainland China.</span></span> <span data-ttu-id="4e421-116">Skype deviendra le client de Fédération pour les utilisateurs fédérés qui utilisaient déjà Messenger.</span><span class="sxs-lookup"><span data-stu-id="4e421-116">Skype will become the federation client for federated users who previously used Messenger.</span></span>



</div>

<span data-ttu-id="4e421-117">Les ports et protocoles définis pour le proxy d’extension de messagerie et de présence (XMPP) déployés sur le serveur Edge autorisent les communications du partenaire fédéré de XMPP au serveur Edge et permettent également la communication entre votre serveur Edge et le partenaire fédéré de XMPP.</span><span class="sxs-lookup"><span data-stu-id="4e421-117">The ports and protocols defined for the extensible messaging and presence protocol (XMPP) proxy deployed on the Edge Server allow communications from the XMPP federated partner to the Edge Server, and also allows communication from your Edge Server to the XMPP federated partner.</span></span> <span data-ttu-id="4e421-118">Une règle est également définie pour le pare-feu à l’intérieur du serveur frontal ou du pool frontal du serveur Edge ou du pool Edge.</span><span class="sxs-lookup"><span data-stu-id="4e421-118">A rule is also defined on the internal-facing firewall from the Front End Server or Front End pool to the Edge Server or Edge pool.</span></span>

<div>

## <a name="firewall-summary---sip-federation"></a><span data-ttu-id="4e421-119">Résumé du pare-feu-Fédération SIP</span><span class="sxs-lookup"><span data-stu-id="4e421-119">Firewall Summary - SIP Federation</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4e421-120">Rôles/protocole/TCP ou UDP/Port</span><span class="sxs-lookup"><span data-stu-id="4e421-120">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="4e421-121">Adresse IP source</span><span class="sxs-lookup"><span data-stu-id="4e421-121">Source IP address</span></span></th>
<th><span data-ttu-id="4e421-122">Adresse IP de destination</span><span class="sxs-lookup"><span data-stu-id="4e421-122">Destination IP address</span></span></th>
<th><span data-ttu-id="4e421-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="4e421-123">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4e421-124">/TCP/5061 d’accès/SIP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="4e421-124">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="4e421-125">Adresse IP publique du service Edge d’accès</span><span class="sxs-lookup"><span data-stu-id="4e421-125">Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="4e421-126">Indifférente</span><span class="sxs-lookup"><span data-stu-id="4e421-126">Any</span></span></p></td>
<td><p><span data-ttu-id="4e421-127">Pour la connectivité de messagerie instantanée fédérée et publique à l’aide du protocole SIP</span><span class="sxs-lookup"><span data-stu-id="4e421-127">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary--public-instant-messaging-connectivity"></a><span data-ttu-id="4e421-128">Résumé du pare-feu-connectivité de messagerie instantanée publique</span><span class="sxs-lookup"><span data-stu-id="4e421-128">Firewall Summary – Public Instant Messaging Connectivity</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4e421-129">Rôles/protocole/TCP ou UDP/Port</span><span class="sxs-lookup"><span data-stu-id="4e421-129">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="4e421-130">Adresse IP source</span><span class="sxs-lookup"><span data-stu-id="4e421-130">Source IP address</span></span></th>
<th><span data-ttu-id="4e421-131">Adresse IP de destination</span><span class="sxs-lookup"><span data-stu-id="4e421-131">Destination IP address</span></span></th>
<th><span data-ttu-id="4e421-132">Remarques</span><span class="sxs-lookup"><span data-stu-id="4e421-132">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4e421-133">/TCP/5061 d’accès/SIP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="4e421-133">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="4e421-134">Partenaires de connectivité de messagerie instantanée publique</span><span class="sxs-lookup"><span data-stu-id="4e421-134">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="4e421-135">Interface d’accès Edge Server</span><span class="sxs-lookup"><span data-stu-id="4e421-135">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="4e421-136">Pour la connectivité de messagerie instantanée fédérée et publique qui utilise SIP.</span><span class="sxs-lookup"><span data-stu-id="4e421-136">For federated and public IM connectivity that use SIP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e421-137">/TCP/5061 d’accès/SIP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="4e421-137">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="4e421-138">Interface d’accès Edge Server</span><span class="sxs-lookup"><span data-stu-id="4e421-138">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="4e421-139">Partenaires de connectivité de messagerie instantanée publique</span><span class="sxs-lookup"><span data-stu-id="4e421-139">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="4e421-140">Pour la connectivité de messagerie instantanée fédérée et publique qui utilise SIP.</span><span class="sxs-lookup"><span data-stu-id="4e421-140">For federated and public IM connectivity that use SIP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e421-141">/TCP/443 d’accès/SIP (TLS)</span><span class="sxs-lookup"><span data-stu-id="4e421-141">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="4e421-142">Clients</span><span class="sxs-lookup"><span data-stu-id="4e421-142">Clients</span></span></p></td>
<td><p><span data-ttu-id="4e421-143">Interface d’accès Edge Server</span><span class="sxs-lookup"><span data-stu-id="4e421-143">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="4e421-144">Trafic SIP client vers serveur pour l’accès des utilisateurs externes.</span><span class="sxs-lookup"><span data-stu-id="4e421-144">Client-to-server SIP traffic for external user access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e421-145">A/V/RTP/TCP/50000-59,999</span><span class="sxs-lookup"><span data-stu-id="4e421-145">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="4e421-146">Interface d’accès Edge Server</span><span class="sxs-lookup"><span data-stu-id="4e421-146">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="4e421-147">Clients Live Messenger</span><span class="sxs-lookup"><span data-stu-id="4e421-147">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="4e421-148">Utilisé pour les sessions A/V avec Windows Live Messenger si la connectivité PIC (Public IM Connectivity) est configurée.</span><span class="sxs-lookup"><span data-stu-id="4e421-148">Used for A/V sessions with Windows Live Messenger if public IM connectivity is configured.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e421-149">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="4e421-149">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="4e421-150">Interface d’accès Edge Server</span><span class="sxs-lookup"><span data-stu-id="4e421-150">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="4e421-151">Clients Live Messenger</span><span class="sxs-lookup"><span data-stu-id="4e421-151">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="4e421-152">Requis pour la connectivité de messagerie instantanée publique avec Windows Live Messenger.</span><span class="sxs-lookup"><span data-stu-id="4e421-152">Required for public IM connectivity with Windows Live Messenger.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e421-153">A/V/STUN, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="4e421-153">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="4e421-154">Clients Live Messenger</span><span class="sxs-lookup"><span data-stu-id="4e421-154">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="4e421-155">Interface d’accès Edge Server</span><span class="sxs-lookup"><span data-stu-id="4e421-155">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="4e421-156">Requis pour la connectivité de messagerie instantanée publique avec Windows Live Messenger.</span><span class="sxs-lookup"><span data-stu-id="4e421-156">Required for public IM connectivity with Windows Live Messenger.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary---extensible-messaging-and-presence-protocol-xmpp"></a><span data-ttu-id="4e421-157">Résumé de pare-feu-protocole de messagerie extensible et de présence</span><span class="sxs-lookup"><span data-stu-id="4e421-157">Firewall Summary - Extensible Messaging and Presence Protocol (XMPP)</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4e421-158">Protocole/TCP ou UDP/Port</span><span class="sxs-lookup"><span data-stu-id="4e421-158">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="4e421-159">Source (adresse IP)</span><span class="sxs-lookup"><span data-stu-id="4e421-159">Source (IP address)</span></span></th>
<th><span data-ttu-id="4e421-160">Destination (adresse IP)</span><span class="sxs-lookup"><span data-stu-id="4e421-160">Destination (IP address)</span></span></th>
<th><span data-ttu-id="4e421-161">Commentaires</span><span class="sxs-lookup"><span data-stu-id="4e421-161">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4e421-162">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="4e421-162">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="4e421-163">Indifférente</span><span class="sxs-lookup"><span data-stu-id="4e421-163">Any</span></span></p></td>
<td><p><span data-ttu-id="4e421-164">Adresse IP de l’interface du service Edge d’accès</span><span class="sxs-lookup"><span data-stu-id="4e421-164">Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="4e421-165">Port de communication serveur à serveur standard pour XMPP.</span><span class="sxs-lookup"><span data-stu-id="4e421-165">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="4e421-166">Autorise la communication au proxy de serveur Edge XMPP auprès des partenaires XMPP fédérés</span><span class="sxs-lookup"><span data-stu-id="4e421-166">Allows communication to the Edge Server XMPP proxy from federated XMPP partners</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e421-167">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="4e421-167">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="4e421-168">Adresse IP de l’interface du service Edge d’accès</span><span class="sxs-lookup"><span data-stu-id="4e421-168">Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="4e421-169">Indifférente</span><span class="sxs-lookup"><span data-stu-id="4e421-169">Any</span></span></p></td>
<td><p><span data-ttu-id="4e421-170">Port de communication serveur à serveur standard pour XMPP.</span><span class="sxs-lookup"><span data-stu-id="4e421-170">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="4e421-171">Autorise la communication du proxy de serveur Edge XMPP aux partenaires XMPP fédérés</span><span class="sxs-lookup"><span data-stu-id="4e421-171">Allows communication from the Edge Server XMPP proxy to federated XMPP partners</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e421-172">XMPP/MTLS/23456</span><span class="sxs-lookup"><span data-stu-id="4e421-172">XMPP/MTLS/23456</span></span></p></td>
<td><p><span data-ttu-id="4e421-173">Indifférente</span><span class="sxs-lookup"><span data-stu-id="4e421-173">Any</span></span></p></td>
<td><p><span data-ttu-id="4e421-174">Adresse IP de l’interface du serveur Edge interne</span><span class="sxs-lookup"><span data-stu-id="4e421-174">Internal Edge Server Interface IP</span></span></p></td>
<td><p><span data-ttu-id="4e421-175">Trafic de XMPP interne provenant de la passerelle XMPP du serveur frontal ou du pool frontal sur le serveur Edge</span><span class="sxs-lookup"><span data-stu-id="4e421-175">Internal XMPP traffic from the XMPP Gateway on the Front End Server or Front End pool to the Edge Server</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="see-also"></a><span data-ttu-id="4e421-176">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4e421-176">See Also</span></span>


[<span data-ttu-id="4e421-177">Scénarios d’accès des utilisateurs externes dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4e421-177">Scenarios for external user access in Lync Server 2013</span></span>](lync-server-2013-scenarios-for-external-user-access.md)  
[<span data-ttu-id="4e421-178">Définition de la configuration requise pour le pare-feu A/V et les ports pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4e421-178">Determine external A/V firewall and port requirements for Lync Server 2013</span></span>](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md)  


[<span data-ttu-id="4e421-179">Gestion des partenaires fédérés XMPP dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4e421-179">Manage XMPP federated partners in Lync Server 2013</span></span>](lync-server-2013-manage-xmpp-federated-partners-for-your-organization.md)  
  

<span data-ttu-id="4e421-180"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4e421-180"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

