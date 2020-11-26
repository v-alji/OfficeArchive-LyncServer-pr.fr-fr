---
title: 'Lync Server 2013 : créer une collection de paramètres de configuration de Trunk'
description: 'Lync Server 2013 : créer un ensemble de paramètres de configuration de Trunk.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create a new collection of trunk configuration settings
ms:assetid: 4ebd710c-38cd-4cff-9a45-df029d424580
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688054(v=OCS.15)
ms:contentKeyID: 49733647
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 16ef4bb6393ec2385eaf7c642734bbc803d4dff6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432183"
---
# <a name="create-a-new-collection-of-trunk-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="15b05-103">Créer une collection de paramètres de configuration de Trunk dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="15b05-103">Create a new collection of trunk configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="15b05-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="15b05-104">

<span> </span></span></span>

<span data-ttu-id="15b05-105">_**Dernière modification de la rubrique :** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="15b05-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="15b05-106">Les paramètres de configuration du Trunk SIP définissent la relation et les fonctionnalités entre un serveur de médiation et la passerelle de réseau téléphonique commuté (PSTN), un échange de succursale public (PBX) ou un contrôleur de bordure de session (SBC) au fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="15b05-106">SIP trunk configuration settings define the relationship and capabilities between a Mediation Server and the public switched telephone network (PSTN) gateway, an IP-public branch exchange (PBX), or a Session Border Controller (SBC) at the service provider.</span></span> <span data-ttu-id="15b05-107">Ces paramètres spécifient, par exemple :</span><span class="sxs-lookup"><span data-stu-id="15b05-107">These settings do such things as specify:</span></span>

  - <span data-ttu-id="15b05-108">si la déviation du trafic multimédia doit être activée sur les jonctions ;</span><span class="sxs-lookup"><span data-stu-id="15b05-108">Whether media bypass should be enabled on the trunks.</span></span>

  - <span data-ttu-id="15b05-109">Les conditions dans lesquelles les paquets de contrôle de transport en temps réel (RTCP) sont envoyés.</span><span class="sxs-lookup"><span data-stu-id="15b05-109">The conditions under which real-time transport control protocol (RTCP) packets are sent.</span></span>

  - <span data-ttu-id="15b05-110">Le chiffrement SRTP (Secure Real-Time Protocol) est requis sur chaque Trunk.</span><span class="sxs-lookup"><span data-stu-id="15b05-110">Whether or not secure real-time protocol (SRTP) encryption is required on each trunk.</span></span>

<span data-ttu-id="15b05-111">Lorsque vous installez Microsoft Lync Server 2013, une collection globale de paramètres de configuration de Trunk SIP est créée pour vous.</span><span class="sxs-lookup"><span data-stu-id="15b05-111">When you install Microsoft Lync Server 2013, a global collection of SIP trunk configuration settings is created for you.</span></span> <span data-ttu-id="15b05-112">En outre, les administrateurs peuvent créer des collections personnalisées sur l’étendue du site ou l’étendue du service (pour le service de passerelle PSTN, uniquement).</span><span class="sxs-lookup"><span data-stu-id="15b05-112">In addition, administrators can create custom setting collections at the site scope or at the service scope (for the PSTN gateway service, only).</span></span>

<span data-ttu-id="15b05-113">Lors de la création des paramètres de configuration de Trunk SIP à l’aide du panneau de configuration de Lync Server, les options suivantes sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="15b05-113">When creating SIP trunk configuration settings using Lync Server Control Panel, the following options are available to you:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="15b05-114">Paramètre de l’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="15b05-114">UI Setting</span></span></th>
<th><span data-ttu-id="15b05-115">Paramètre PowerShell</span><span class="sxs-lookup"><span data-stu-id="15b05-115">PowerShell Parameter</span></span></th>
<th><span data-ttu-id="15b05-116">Description</span><span class="sxs-lookup"><span data-stu-id="15b05-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="15b05-117">Nom</span><span class="sxs-lookup"><span data-stu-id="15b05-117">Name</span></span></p></td>
<td><p><span data-ttu-id="15b05-118">Identity</span><span class="sxs-lookup"><span data-stu-id="15b05-118">Identity</span></span></p></td>
<td><p><span data-ttu-id="15b05-p103">Identificateur unique de la collection. Cette propriété est en lecture seule. Vous ne pouvez pas modifier l’identité d’une collection de paramètres de configuration des jonctions.</span><span class="sxs-lookup"><span data-stu-id="15b05-p103">Unique identifier for the collection. This property is read-only; you cannot change the Identity of a collection of trunk configuration settings.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15b05-121">Description</span><span class="sxs-lookup"><span data-stu-id="15b05-121">Description</span></span></p></td>
<td><p><span data-ttu-id="15b05-122">Description</span><span class="sxs-lookup"><span data-stu-id="15b05-122">Description</span></span></p></td>
<td><p><span data-ttu-id="15b05-123">Permet aux administrateurs de stocker des informations supplémentaires sur les paramètres (par exemple, l’objectif de la configuration des jonctions).</span><span class="sxs-lookup"><span data-stu-id="15b05-123">Provides a way for administrators to store addition information about the settings (for example, the purpose of the trunk configuration).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15b05-124">Nombre maximal de boîtes de dialogue préliminaires prises en charge</span><span class="sxs-lookup"><span data-stu-id="15b05-124">Maximum early dialogs supported</span></span></p></td>
<td><p><span data-ttu-id="15b05-125">MaxEarlyDialogs</span><span class="sxs-lookup"><span data-stu-id="15b05-125">MaxEarlyDialogs</span></span></p></td>
<td><p><span data-ttu-id="15b05-126">Nombre maximal de réponses dirigées qu’une passerelle RTC, un système IP-PBX ou un contrôleur de session en périphérie côté fournisseur de services peut recevoir à une invitation envoyée au serveur de médiation.</span><span class="sxs-lookup"><span data-stu-id="15b05-126">The maximum number of forked responses a PSTN gateway, IP-PBX, or SBC at the service provider can receive to an Invite that it sent to the Mediation Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15b05-127">Niveau de prise en charge du chiffrement</span><span class="sxs-lookup"><span data-stu-id="15b05-127">Encryption support level</span></span></p></td>
<td><p><span data-ttu-id="15b05-128">SRTPMode</span><span class="sxs-lookup"><span data-stu-id="15b05-128">SRTPMode</span></span></p></td>
<td><p><span data-ttu-id="15b05-129">Indique le niveau de prise en charge de la protection du trafic multimédia entre le serveur de médiation et la passerelle RTC, le système IP-PBX ou le contrôleur SBC (Session Border Controller) côté fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="15b05-129">Indicates the level of support for protecting media traffic between the Mediation Server and the PSTN Gateway, IP-PBX, or SBC at the service provider.</span></span> <span data-ttu-id="15b05-130">Dans les cas de déviation du trafic multimédia, cette valeur doit être compatible avec le paramètre EncryptionLevel de la configuration multimédia.</span><span class="sxs-lookup"><span data-stu-id="15b05-130">For media bypass cases, this value must be compatible with the EncryptionLevel setting in the media configuration.</span></span> <span data-ttu-id="15b05-131">La configuration de média est définie à l’aide de la cmdlet <a href="https://docs.microsoft.com/powershell/module/skype/New-CsMediaConfiguration">New-CsMediaConfiguration</a> et de <a href="https://docs.microsoft.com/powershell/module/skype/Set-CsMediaConfiguration">Set-CsMediaConfiguration</a> .</span><span class="sxs-lookup"><span data-stu-id="15b05-131">Media configuration is set by using the <a href="https://docs.microsoft.com/powershell/module/skype/New-CsMediaConfiguration">New-CsMediaConfiguration</a> and <a href="https://docs.microsoft.com/powershell/module/skype/Set-CsMediaConfiguration">Set-CsMediaConfiguration</a> cmdlets.</span></span></p>
<p><span data-ttu-id="15b05-132">Les valeurs autorisées sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="15b05-132">Allowed values are:</span></span></p>
<ul>
<li><p><span data-ttu-id="15b05-133">Obligatoire : le chiffrement SRTP doit être utilisé.</span><span class="sxs-lookup"><span data-stu-id="15b05-133">Required: SRTP encryption must be used.</span></span></p></li>
<li><p><span data-ttu-id="15b05-134">Facultatif : le chiffrement SRTP sera utilisé si la passerelle le prend en charge.</span><span class="sxs-lookup"><span data-stu-id="15b05-134">Optional: SRTP will be used if the gateway supports it.</span></span></p></li>
<li><p><span data-ttu-id="15b05-135">Non pris en charge : le chiffrement SRTP n’est pas pris en charge et ne sera donc pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="15b05-135">Not Supported: SRTP encryption is not supported and therefore will not be used.</span></span></p></li>
</ul>
<p><span data-ttu-id="15b05-p105">SRTPMode n’est utilisé que si la passerelle est configurée de manière à utiliser le protocole de transport TLS (Transport Layer Security). Si la passerelle est configurée avec le protocole de transport TCP, SRTPMode est défini en interne sur NotSupported.</span><span class="sxs-lookup"><span data-stu-id="15b05-p105">SRTPMode is used only if the gateway is configured to use Transport Layer Security (TLS). If the gateway is configured with Transmission Control Protocol (TCP) as the transport, SRTPMode is internally set to Not Supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15b05-138">Prise en charge de la référence</span><span class="sxs-lookup"><span data-stu-id="15b05-138">Refer support</span></span></p></td>
<td><p><span data-ttu-id="15b05-139">Enable3pccRefer</span><span class="sxs-lookup"><span data-stu-id="15b05-139">Enable3pccRefer</span></span></p>
<p><span data-ttu-id="15b05-140">EnableReferSupport</span><span class="sxs-lookup"><span data-stu-id="15b05-140">EnableReferSupport</span></span></p></td>
<td><p><span data-ttu-id="15b05-141">Si ce paramètre défini sur <strong>Activer la référence d’appel vers la passerelle</strong>, cela indique que la jonction prend en charge la réception des demandes REFER à partir du serveur de médiation.</span><span class="sxs-lookup"><span data-stu-id="15b05-141">If set to <strong>Enable sending refer to the gateway</strong>, indicates that the trunk supports receiving Refer requests from the Mediation Server.</span></span></p>
<p><span data-ttu-id="15b05-142">S’il est défini sur <strong>Activer la référence avec un contrôle d’appel tiers</strong>, cela indique que le protocole 3pcc peut être utilisé pour permettre aux appels transférés de contourner le site hébergé.</span><span class="sxs-lookup"><span data-stu-id="15b05-142">If set to <strong>Enable refer using third-party call control</strong>, indicates that the 3pcc protocol can be used to allow transferred calls to bypass the hosted site.</span></span> <span data-ttu-id="15b05-143">3PCC est également connu sous &quot; le nom de contrôle tiers &quot; et se produit lorsqu’un tiers est utilisé pour connecter une paire d’appelants (par exemple, un opérateur passant un appel de la personne a à la personne B).</span><span class="sxs-lookup"><span data-stu-id="15b05-143">3pcc is also known as &quot;third party control,&quot; and occurs when a third-party is used to connect a pair of callers (for example, an operator placing a call from person A to person B).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15b05-144">Activer la déviation du trafic multimédia</span><span class="sxs-lookup"><span data-stu-id="15b05-144">Enable media bypass</span></span></p></td>
<td><p><span data-ttu-id="15b05-145">EnableBypass</span><span class="sxs-lookup"><span data-stu-id="15b05-145">EnableBypass</span></span></p></td>
<td><p><span data-ttu-id="15b05-p107">Indique si la déviation du trafic multimédia est activée pour cette jonction. La déviation du trafic multimédia ne peut être activée que si <strong>Traitement multimédia centralisé</strong> est activé également.</span><span class="sxs-lookup"><span data-stu-id="15b05-p107">Indicates whether media bypass is enabled for this trunk. Media bypass can only be enabled if <strong>Centralized media processing</strong> is also enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15b05-148">Traitement multimédia centralisé</span><span class="sxs-lookup"><span data-stu-id="15b05-148">Centralized media processing</span></span></p></td>
<td><p><span data-ttu-id="15b05-149">ConcentratedTopology</span><span class="sxs-lookup"><span data-stu-id="15b05-149">ConcentratedTopology</span></span></p></td>
<td><p><span data-ttu-id="15b05-p108">Indique s’il existe un point de terminaison multimédia connu (par exemple, une passerelle RTC où le point de terminaison multimédia possède la même adresse IP que le point de terminaison de signalisation).</span><span class="sxs-lookup"><span data-stu-id="15b05-p108">Indicates whether there is a well-known media termination point. (An example of a well-known media termination point would be a PSTN gateway where the media termination has the same IP as the signaling termination.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15b05-152">Activer l’accrochage RTP</span><span class="sxs-lookup"><span data-stu-id="15b05-152">Enable RTP latching</span></span></p></td>
<td><p><span data-ttu-id="15b05-153">EnableRTPLatching</span><span class="sxs-lookup"><span data-stu-id="15b05-153">EnableRTPLatching</span></span></p></td>
<td><p><span data-ttu-id="15b05-p109">Indique si les jonctions SIP (Session Initiation Protocol) prennent en charge l’accrochage RTP. L’accrochage RTP est une technologie qui permet la connectivité RTP/RTCP par le biais d’un appareil ou d’un pare-feu NAT (Network Address Translator).</span><span class="sxs-lookup"><span data-stu-id="15b05-p109">Indicates whether or not the SIP trunks support RTP latching. RTP latching is a technology that enables RTP/RTCP connectivity through a NAT (network address translator) device or firewall.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15b05-156">Activer l’historique du transfert d’appel</span><span class="sxs-lookup"><span data-stu-id="15b05-156">Enable forward call history</span></span></p></td>
<td><p><span data-ttu-id="15b05-157">ForwardCallHistory</span><span class="sxs-lookup"><span data-stu-id="15b05-157">ForwardCallHistory</span></span></p></td>
<td><p><span data-ttu-id="15b05-158">Indique si les informations d’historique d’appel sont transférées par le biais de la jonction.</span><span class="sxs-lookup"><span data-stu-id="15b05-158">Indicates whether call history information will be forwarded through the trunk.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15b05-159">Activer les données de transfert P-Asserted-Identity</span><span class="sxs-lookup"><span data-stu-id="15b05-159">Enable forward P-Asserted-Identity data</span></span></p></td>
<td><p><span data-ttu-id="15b05-160">ForwardPAI</span><span class="sxs-lookup"><span data-stu-id="15b05-160">ForwardPAI</span></span></p></td>
<td><p><span data-ttu-id="15b05-p110">Indique si l’en-tête P-Asserted-Identity (PAI) sera transféré avec l’appel. L’en-tête PAI permet de vérifier l’identité de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="15b05-p110">Indicates whether the P-Asserted-Identity (PAI) header will be forwarded along with the call. The PAI header provides a way to verify the identity of the caller.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15b05-163">Activer le minuteur de basculement de routage de trafic sortant</span><span class="sxs-lookup"><span data-stu-id="15b05-163">Enable outbound routing failover timer</span></span></p></td>
<td><p><span data-ttu-id="15b05-164">EnableFastFailoverTimer</span><span class="sxs-lookup"><span data-stu-id="15b05-164">EnableFastFailoverTimer</span></span></p></td>
<td><p><span data-ttu-id="15b05-p111">Indique si les appels sortants auxquels la passerelle ne répond pas dans les 10 secondes seront routés vers la jonction suivante disponible. En l’absence d’autre jonction, l’appel est abandonné automatiquement. Dans une organisation avec des réponses de passerelle ou réseau lentes, cela peut entraîner l’abandon de nombreux appels.</span><span class="sxs-lookup"><span data-stu-id="15b05-p111">Indicates whether outbound calls that are not answered by the gateway within 10 seconds will be routed to the next available trunk; if there are no additional trunks then the call will automatically be dropped. In an organization with slow networks and gateway responses, that could potentially result in calls being dropped unnecessarily.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15b05-167">Utilisations RTC associées</span><span class="sxs-lookup"><span data-stu-id="15b05-167">Associated PSTN usages</span></span></p></td>
<td><p><span data-ttu-id="15b05-168">PSTNUsages</span><span class="sxs-lookup"><span data-stu-id="15b05-168">PSTNUsages</span></span></p></td>
<td><p><span data-ttu-id="15b05-169">Collection d’utilisations RTC affectées à la jonction.</span><span class="sxs-lookup"><span data-stu-id="15b05-169">Collection of PSTN usages assigned to the trunk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15b05-170">Numéro converti à tester</span><span class="sxs-lookup"><span data-stu-id="15b05-170">Translated number to test</span></span></p></td>
<td><p><span data-ttu-id="15b05-171">S/O</span><span class="sxs-lookup"><span data-stu-id="15b05-171">N/A</span></span></p></td>
<td><p><span data-ttu-id="15b05-172">Numéro de téléphone pouvant être utilisé pour effectuer un test ad hoc des paramètres de configuration des jonctions.</span><span class="sxs-lookup"><span data-stu-id="15b05-172">Phone number that can be used to do an ad hoc test of the trunk configuration settings.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15b05-173">Règles de conversion associées</span><span class="sxs-lookup"><span data-stu-id="15b05-173">Associated translation rules</span></span></p></td>
<td><p><span data-ttu-id="15b05-174">OutboundTranslationRulesList</span><span class="sxs-lookup"><span data-stu-id="15b05-174">OutboundTranslationRulesList</span></span></p></td>
<td><p><span data-ttu-id="15b05-175">Collection de règles de conversion de numéros de téléphone qui s’appliquent aux appels gérés par le routage sortant (appels routés vers les destinations PBX ou RTC).</span><span class="sxs-lookup"><span data-stu-id="15b05-175">Collection of phone number translation rules that apply to calls handled by Outbound Routing (calls routed to PBX or PSTN destinations).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15b05-176">Règles de conversion du numéro appelé</span><span class="sxs-lookup"><span data-stu-id="15b05-176">Called number translation rules</span></span></p></td>
<td><p><span data-ttu-id="15b05-177">OutboundCallingNumberTranslationRulesList</span><span class="sxs-lookup"><span data-stu-id="15b05-177">OutboundCallingNumberTranslationRulesList</span></span></p></td>
<td><p><span data-ttu-id="15b05-178">Collection de règles de conversion de numéro d’appel sortant affectées à la jonction.</span><span class="sxs-lookup"><span data-stu-id="15b05-178">Collection of outbound calling number translation rules assigned to the trunk.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15b05-179">Numéro de téléphone à tester</span><span class="sxs-lookup"><span data-stu-id="15b05-179">Phone number to test</span></span></p></td>
<td><p><span data-ttu-id="15b05-180">S/O</span><span class="sxs-lookup"><span data-stu-id="15b05-180">N/A</span></span></p></td>
<td><p><span data-ttu-id="15b05-181">Numéro de téléphone pouvant être utilisé pour effectuer un test ad hoc des règles de conversion.</span><span class="sxs-lookup"><span data-stu-id="15b05-181">Phone number that can be used to do an ad hoc test of the translation rules.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15b05-182">Numéro appelant</span><span class="sxs-lookup"><span data-stu-id="15b05-182">Calling number</span></span></p></td>
<td><p><span data-ttu-id="15b05-183">S/O</span><span class="sxs-lookup"><span data-stu-id="15b05-183">N/A</span></span></p></td>
<td><p><span data-ttu-id="15b05-184">Indique que le numéro de téléphone à tester est celui de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="15b05-184">Indicates that the phone number to test is the phone number of the caller.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15b05-185">Numéro appelé</span><span class="sxs-lookup"><span data-stu-id="15b05-185">Called number</span></span></p></td>
<td><p><span data-ttu-id="15b05-186">S/O</span><span class="sxs-lookup"><span data-stu-id="15b05-186">N/A</span></span></p></td>
<td><p><span data-ttu-id="15b05-187">Indique que le numéro de téléphone à tester est celui de la personne appelée.</span><span class="sxs-lookup"><span data-stu-id="15b05-187">Indicates that the phone number to test is the phone number of the person being called.</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="15b05-188">Les applets de commande Lync Server CsTrunkConfiguration prennent en charge des propriétés supplémentaires qui ne figurent pas dans le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="15b05-188">The Lync Server CsTrunkConfiguration cmdlets support additional properties not shown in Lync Server Control Panel.</span></span> <span data-ttu-id="15b05-189">Pour plus d’informations, consultez la rubrique d’aide relative à l’applet de <A href="https://docs.microsoft.com/powershell/module/skype/New-CsTrunkConfiguration">nouvelle-CsTrunkConfiguration</A> .</span><span class="sxs-lookup"><span data-stu-id="15b05-189">For more information, see the help topic for the <A href="https://docs.microsoft.com/powershell/module/skype/New-CsTrunkConfiguration">New-CsTrunkConfiguration</A> cmdlet.</span></span>



</div>

<div>

## <a name="to-create-new-trunk-configuration-settings-by-using-lync-server-control-panel"></a><span data-ttu-id="15b05-190">Pour créer des paramètres de configuration de Trunk en utilisant le panneau de configuration de Lync Server</span><span class="sxs-lookup"><span data-stu-id="15b05-190">To create new trunk configuration settings by using Lync Server Control Panel</span></span>

1.  <span data-ttu-id="15b05-191">Dans le panneau de configuration de Lync Server, cliquez sur **routage des communications vocales**, puis cliquez sur **configuration de Trunk**.</span><span class="sxs-lookup"><span data-stu-id="15b05-191">In Lync Server Control Panel, click **Voice Routing**, and then click **Trunk Configuration**.</span></span>

2.  <span data-ttu-id="15b05-192">Sous l’onglet **Configuration de la jonction**, cliquez sur **Nouveau**, puis cliquez sur **Jonction de site** pour créer les paramètres au niveau de l’étendue Site ou cliquez sur **Jonction de pool** pour créer les paramètres au niveau de l’étendue Service.</span><span class="sxs-lookup"><span data-stu-id="15b05-192">On the **Trunk Configuration** tab, click **New**, and then click **Site trunk** to create the new settings at the site scope, or **Pool trunk** to create the new settings at the service scope.</span></span>

3.  <span data-ttu-id="15b05-p113">Dans la boîte de dialogue **Sélectionner un site** ou **Sélectionner un service** (la boîte de dialogue qui s’affiche change selon que vous créez des paramètres au niveau de l’étendue Site ou de l’étendue Service), sélectionnez l’emplacement des nouveaux paramètres de configuration, puis cliquez sur **OK**. Si la boîte de dialogue est vide, vous ne pouvez pas créer de paramètres supplémentaires. Par exemple, si la boîte de dialogue **Sélectionner un site** est vide, une collection de sites de configuration de jonctions a déjà été affectée à l’ensemble de vos sites et chaque site (chaque service) ne peut héberger qu’une seule collection de ce type. Dans ce cas, vous pouvez supprimer la collection existante et créer une autre collection ou modifier simplement la collection existante.</span><span class="sxs-lookup"><span data-stu-id="15b05-p113">In the **Select a Site** or the **Select a Service** dialog box (the dialog box that appears will depend on whether you are creating site-scoped or service-scoped settings) select the location for the new configuration settings and then click **OK**. If the dialog box is blank, that means there is no place to create the new settings; for example, if the **Select a Site** dialog box is blank that means that all of your sites have already been assigned a collection of trunk configuration sites, and each site (and each service) can only host one such collection. In that case, you can either delete the existing collection and create a new collection, or simply modify the existing collection.</span></span>

4.  <span data-ttu-id="15b05-196">Dans la boîte de dialogue **Nouvelle configuration de jonction**, effectuez les sélections appropriées, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="15b05-196">In the **New Trunk Configuration** dialog, make the appropriate selections and then click **OK**.</span></span>

5.  <span data-ttu-id="15b05-p114">La propriété **État** de la collection est définie sur la valeur **Non validé**. Pour valider les modifications et supprimer la collection, cliquez sur **Valider**, puis sur **Tout valider**.</span><span class="sxs-lookup"><span data-stu-id="15b05-p114">The **State** property for the collection will be updated to **Uncommitted**. To commit the changes, and to delete the collection, click **Commit** and then click **Commit All**.</span></span>

6.  <span data-ttu-id="15b05-199">Dans la boîte de dialogue **Paramètres de configuration de la voix non validés**, cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="15b05-199">In the **Uncommitted Voice Configuration Settings** dialog box, click **OK**.</span></span>

7.  <span data-ttu-id="15b05-200">Dans la boîte de dialogue **panneau de configuration Microsoft Lync Server 2013** , cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="15b05-200">In the **Microsoft Lync Server 2013 Control Panel** dialog box click **OK**.</span></span>

<span data-ttu-id="15b05-201"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="15b05-201"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

