---
title: 'Lync Server 2013 : démarrage de Lync à partir d’une autre application'
description: 'Lync Server 2013 : démarrage de Lync à partir d’une autre application.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Starting Lync from another application
ms:assetid: 573b30b1-6590-4b24-8e96-a41be57cb0ef
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398376(v=OCS.15)
ms:contentKeyID: 48184184
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fd64b8b9f335638b54a0bf6473b5d159c97a0e7f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49393948"
---
# <a name="starting-lync-from-another-application"></a><span data-ttu-id="0c0b6-103">Démarrage de Lync à partir d’une autre application</span><span class="sxs-lookup"><span data-stu-id="0c0b6-103">Starting Lync from another application</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0c0b6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0c0b6-104">

<span> </span></span></span>

<span data-ttu-id="0c0b6-105">_**Dernière modification de la rubrique :** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="0c0b6-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="0c0b6-106">Vous pouvez utiliser des paramètres de ligne de commande pour démarrer rapidement Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="0c0b6-106">You can use command-line parameters to quick-start Lync 2013.</span></span> <span data-ttu-id="0c0b6-107">Par exemple, si un utilisateur clique sur un numéro de téléphone dans une autre application, l’application peut démarrer une instance de Lync 2013 et lancer un appel vers ce numéro.</span><span class="sxs-lookup"><span data-stu-id="0c0b6-107">For example, if a user clicks a phone number in another application, the application can start an instance of Lync 2013 and initiate a call to that number.</span></span>

<span data-ttu-id="0c0b6-108">Lync 2013 peut également reconnaître une liste délimitée par des points-virgules de noms de contacts pour les conférences multipièces.</span><span class="sxs-lookup"><span data-stu-id="0c0b6-108">Lync 2013 can also recognize a semicolon-delimited list of contact names for multiparty conferencing.</span></span>

<span data-ttu-id="0c0b6-109">Si Lync 2013 est configuré de manière à se connecter automatiquement au démarrage, puis en démarrant Lync 2013 avec des paramètres de ligne de commande, vous ouvrez la fenêtre principale de Lync.</span><span class="sxs-lookup"><span data-stu-id="0c0b6-109">If Lync 2013 is configured to automatically sign in when started, then starting Lync 2013 with command-line parameters will open the Lync main window.</span></span> <span data-ttu-id="0c0b6-110">Si Lync n’est pas configuré de manière à se connecter automatiquement au démarrage, la fenêtre de connexion s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="0c0b6-110">If Lync is not configured to automatically sign in when started, the sign-in window opens.</span></span>

<span data-ttu-id="0c0b6-111">Le tableau suivant répertorie les paramètres disponibles.</span><span class="sxs-lookup"><span data-stu-id="0c0b6-111">The following table shows the available parameters.</span></span>

### <a name="lync-2013-command-line-parameters"></a><span data-ttu-id="0c0b6-112">Paramètres Command-Line de Lync 2013</span><span class="sxs-lookup"><span data-stu-id="0c0b6-112">Lync 2013 Command-Line Parameters</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0c0b6-113">Long</span><span class="sxs-lookup"><span data-stu-id="0c0b6-113">Extension</span></span></th>
<th><span data-ttu-id="0c0b6-114">Format des données</span><span class="sxs-lookup"><span data-stu-id="0c0b6-114">Format of Data</span></span></th>
<th><span data-ttu-id="0c0b6-115">Action</span><span class="sxs-lookup"><span data-stu-id="0c0b6-115">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0c0b6-116">tel</span><span class="sxs-lookup"><span data-stu-id="0c0b6-116">tel:</span></span></p></td>
<td><p><span data-ttu-id="0c0b6-117">URI tel</span><span class="sxs-lookup"><span data-stu-id="0c0b6-117">tel URI</span></span></p></td>
<td><p><span data-ttu-id="0c0b6-118">Ouvre la fenêtre de conversation pour un appel audio sans composer le numéro spécifié.</span><span class="sxs-lookup"><span data-stu-id="0c0b6-118">Opens the Conversation window for an audio call but does not dial the specified number.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c0b6-119">callto</span><span class="sxs-lookup"><span data-stu-id="0c0b6-119">callto:</span></span></p></td>
<td><p><span data-ttu-id="0c0b6-120">Tel :, SIP : ou URI tel de type</span><span class="sxs-lookup"><span data-stu-id="0c0b6-120">tel:, sip:, or typeable tel URI</span></span></p></td>
<td><p><span data-ttu-id="0c0b6-121">Ouvre la fenêtre de conversation pour un appel audio sans composer le numéro spécifié.</span><span class="sxs-lookup"><span data-stu-id="0c0b6-121">Opens the Conversation window for an audio call but does not dial the specified number.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c0b6-122">SIP</span><span class="sxs-lookup"><span data-stu-id="0c0b6-122">sip:</span></span></p></td>
<td><p><span data-ttu-id="0c0b6-123">URI SIP</span><span class="sxs-lookup"><span data-stu-id="0c0b6-123">SIP URI</span></span></p></td>
<td><p><span data-ttu-id="0c0b6-124">Ouvre la fenêtre de conversation avec l’URI (Uniform Resource Identifier) SIP spécifié dans la liste des participants.</span><span class="sxs-lookup"><span data-stu-id="0c0b6-124">Opens the Conversation window with the specified SIP Uniform Resource Identifier (URI) in the participant list.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c0b6-125">Quels</span><span class="sxs-lookup"><span data-stu-id="0c0b6-125">Sips:</span></span></p></td>
<td><p><span data-ttu-id="0c0b6-126">URI SIP</span><span class="sxs-lookup"><span data-stu-id="0c0b6-126">SIP URI</span></span></p></td>
<td><p><span data-ttu-id="0c0b6-127">Si Lync 2013 est configuré pour utiliser le protocole TLS (Transport Layer Security), fonctionne exactement comme pour SIP :.</span><span class="sxs-lookup"><span data-stu-id="0c0b6-127">If Lync 2013 is configured to use the Transport Layer Security (TLS) protocol, functions exactly like sip:.</span></span> <span data-ttu-id="0c0b6-128">Si TLS n’est pas utilisé, affiche une boîte de dialogue informant l’utilisateur qu’un niveau de sécurité supérieur est requis.</span><span class="sxs-lookup"><span data-stu-id="0c0b6-128">If TLS is not being used, displays a dialog box informing the user that a higher level of security is required.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c0b6-129">donne</span><span class="sxs-lookup"><span data-stu-id="0c0b6-129">conf:</span></span></p></td>
<td><p><span data-ttu-id="0c0b6-130">URI SIP de la Conférence à rejoindre</span><span class="sxs-lookup"><span data-stu-id="0c0b6-130">SIP URI of conference to join</span></span></p></td>
<td><p><span data-ttu-id="0c0b6-131">Si URI est Self, instancie le focus et affiche le focus uniquement.</span><span class="sxs-lookup"><span data-stu-id="0c0b6-131">If URI is self, instantiates the focus and brings up roster-only view.</span></span> <span data-ttu-id="0c0b6-132">Dans le cas contraire, ouvre l’affichage de la liste, mais n’envoie pas d’invitation.</span><span class="sxs-lookup"><span data-stu-id="0c0b6-132">Otherwise, brings up roster view but does not send INVITE.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c0b6-133">Pseudo</span><span class="sxs-lookup"><span data-stu-id="0c0b6-133">im:</span></span></p></td>
<td><p><span data-ttu-id="0c0b6-134">URI SIP</span><span class="sxs-lookup"><span data-stu-id="0c0b6-134">SIP URI</span></span></p></td>
<td><p><span data-ttu-id="0c0b6-135">Affiche une fenêtre de conversation par messagerie instantanée uniquement avec l’URI SIP.</span><span class="sxs-lookup"><span data-stu-id="0c0b6-135">Displays an instant messaging (IM)-only Conversation window with the SIP URI.</span></span> <span data-ttu-id="0c0b6-136">Accepte plusieurs URI SIP spécifiés entre crochets ( &lt; &gt; ) sans séparateur.</span><span class="sxs-lookup"><span data-stu-id="0c0b6-136">Accepts multiple SIP URIs specified inside angle brackets (&lt;&gt;) without any separator.</span></span></p>
<pre><code>im:&lt;sip:user1@host&gt;&lt;sip:user2@host&gt;</code></pre></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0c0b6-137">Le tableau suivant contient des exemples de ces paramètres de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="0c0b6-137">The following table provides examples of these command-line parameters.</span></span>

### <a name="command-line-parameter-examples"></a><span data-ttu-id="0c0b6-138">Exemples de paramètres de Command-Line</span><span class="sxs-lookup"><span data-stu-id="0c0b6-138">Command-Line Parameter Examples</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0c0b6-139">Instanci</span><span class="sxs-lookup"><span data-stu-id="0c0b6-139">Instance</span></span></th>
<th><span data-ttu-id="0c0b6-140">Conduit</span><span class="sxs-lookup"><span data-stu-id="0c0b6-140">Results</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0c0b6-141">Tel : + 14255550101</span><span class="sxs-lookup"><span data-stu-id="0c0b6-141">Tel:+14255550101</span></span></p></td>
<td><p><span data-ttu-id="0c0b6-142">Ouvre une seule vue de téléphone avec + 14255550101.</span><span class="sxs-lookup"><span data-stu-id="0c0b6-142">Opens a phone-only view with +14255550101.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c0b6-143">Callto : tel : + 14255550101</span><span class="sxs-lookup"><span data-stu-id="0c0b6-143">Callto:tel:+ 14255550101</span></span></p></td>
<td><p><span data-ttu-id="0c0b6-144">Ouvre une seule vue de téléphone avec + 14255550101.</span><span class="sxs-lookup"><span data-stu-id="0c0b6-144">Opens a phone-only view with +14255550101.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c0b6-145">Callto:sip:kazuto@litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="0c0b6-145">Callto:sip:kazuto@litwareinc.com</span></span></p></td>
<td><p><span data-ttu-id="0c0b6-146">Ouvre une seule vue de téléphone avec kazuto@litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="0c0b6-146">Opens a phone-only view with kazuto@litwareinc.com.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c0b6-147">sip:kazuto@litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="0c0b6-147">sip:kazuto@litwareinc.com</span></span></p></td>
<td><p><span data-ttu-id="0c0b6-148">Ouvre une fenêtre de conversation avec kazuto@litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="0c0b6-148">Opens a Conversation window with kazuto@litwareinc.com.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c0b6-149">conf : SIP :https://meet.contoso.com/kazuto/7322994</span><span class="sxs-lookup"><span data-stu-id="0c0b6-149">conf:sip:https://meet.contoso.com/kazuto/7322994</span></span></p></td>
<td><p><span data-ttu-id="0c0b6-150">Ouvre une fenêtre de conversation et affiche les options de participation à une réunion audio.</span><span class="sxs-lookup"><span data-stu-id="0c0b6-150">Opens a Conversation window and displays meeting audio join options.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="0c0b6-151">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0c0b6-151">


</div>

<span> </span>

</div>

</div>

</span></span></div>

