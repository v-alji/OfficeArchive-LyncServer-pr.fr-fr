---
title: 'Lync Server 2013 : installation et configuration des nœuds d’observation'
description: 'Lync Server 2013 : installation et configuration des nœuds d’observation.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Installing and configuring watcher nodes
ms:assetid: 61f6deea-e3ef-4468-9be8-a65705815ebb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204943(v=OCS.15)
ms:contentKeyID: 48184284
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 87bf43e1651fabfa0137d09234d663cc905e947b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427057"
---
# <a name="installing-and-configuring-watcher-nodes-in-lync-server-2013"></a><span data-ttu-id="7f2fd-103">Installation et configuration des nœuds d’observation dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7f2fd-103">Installing and configuring watcher nodes in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7f2fd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7f2fd-104">

<span> </span></span></span>

<span data-ttu-id="7f2fd-105">_**Dernière modification de la rubrique :** 2013-11-07_</span><span class="sxs-lookup"><span data-stu-id="7f2fd-105">_**Topic Last Modified:** 2013-11-07_</span></span>

<span data-ttu-id="7f2fd-106">Les *nœuds d’observation* sont des ordinateurs qui exécutent périodiquement les transactions synthétiques de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="7f2fd-106">*Watcher nodes* are computers that periodically run Lync Server synthetic transactions.</span></span> <span data-ttu-id="7f2fd-107">Les *transactions synthétiques* sont des cmdlets Windows PowerShell qui vérifient que les scénarios d’utilisateur final (par exemple, la possibilité de se connecter au système ou la possibilité d’échanger des messages instantanés) fonctionnent comme prévu.</span><span class="sxs-lookup"><span data-stu-id="7f2fd-107">*Synthetic transactions* are Windows PowerShell cmdlets that verify that key end user scenarios—such as the ability to sign in to the system, or the ability to exchange instant messages—are working as expected.</span></span> <span data-ttu-id="7f2fd-108">Pour Lync Server 2013, System Center Operations Manager peut exécuter les transactions synthétiques indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="7f2fd-108">For Lync Server 2013, System Center Operations Manager can run the synthetic transactions shown in the following table.</span></span> <span data-ttu-id="7f2fd-109">Il existe trois types de transactions de synthèse différents indiqués dans le tableau :</span><span class="sxs-lookup"><span data-stu-id="7f2fd-109">There are three different synthetic transaction types shown in the table:</span></span>

  - <span data-ttu-id="7f2fd-110">**Par défaut**.</span><span class="sxs-lookup"><span data-stu-id="7f2fd-110">**Default**.</span></span> <span data-ttu-id="7f2fd-111">Il s’agit des transactions synthétiques qui s’exécutent par défaut sur un nœud d’observateur.</span><span class="sxs-lookup"><span data-stu-id="7f2fd-111">These are the synthetic transactions that a watcher node will run by default.</span></span> <span data-ttu-id="7f2fd-112">Lorsque vous créez un nouveau nœud d’observateur, vous avez la possibilité de spécifier les transactions synthétiques qui seront exécutées sur ce nœud.</span><span class="sxs-lookup"><span data-stu-id="7f2fd-112">When you create a new watcher node, you have the option of specifying which synthetic transactions that node will run.</span></span> <span data-ttu-id="7f2fd-113">(Il s’agit de l’objet du paramètre tests utilisé par l’applet **de nouvelle cmdlet New-CsWatcherNodeConfiguration** .) Si vous n’utilisez pas le paramètre tests lors de la création du nœud d’observateur, toutes les transactions synthétiques par défaut sont exécutées et aucune des transactions synthétiques par défaut ne sera exécutée.</span><span class="sxs-lookup"><span data-stu-id="7f2fd-113">(That's the purpose of the Tests parameter used by the **New-CsWatcherNodeConfiguration** cmdlet.) If you do not use the Tests parameter when the watcher node is created, it will automatically run all the Default synthetic transactions and will not run any of the Non-default synthetic transactions.</span></span> <span data-ttu-id="7f2fd-114">Cela signifie, par exemple, que le nœud d’observateur est configuré pour exécuter le test d' Test-CsAddressBookService, mais qu’il ne sera pas configuré pour exécuter le test Test-CsExumConnectivity.</span><span class="sxs-lookup"><span data-stu-id="7f2fd-114">That means, for example, that the watcher node will be configured to run the Test-CsAddressBookService test, but will not be configured to run the Test-CsExumConnectivity test.</span></span>

  - <span data-ttu-id="7f2fd-115">**Pas par défaut**.</span><span class="sxs-lookup"><span data-stu-id="7f2fd-115">**Non-default**.</span></span> <span data-ttu-id="7f2fd-116">Comme son nom l’indique, les transactions synthétiques non par défaut sont des tests que les nœuds d’observation ne s’exécutent pas par défaut.</span><span class="sxs-lookup"><span data-stu-id="7f2fd-116">As the name implies, Non-default synthetic transactions are tests that watcher nodes do not run by default.</span></span> <span data-ttu-id="7f2fd-117">Toutefois, le nœud Watcher peut être activé pour exécuter une des transactions synthétiques non par défaut.</span><span class="sxs-lookup"><span data-stu-id="7f2fd-117">However, the watcher node can be enabled to run any of the Non-default synthetic transactions.</span></span> <span data-ttu-id="7f2fd-118">Vous pouvez le faire lorsque vous créez le nœud d’observation (à l’aide de l’applet **de connexion New-CsWatcherNodeConfiguration** ), ou à tout moment.</span><span class="sxs-lookup"><span data-stu-id="7f2fd-118">You can do this when you create the watcher node (by using the **New-CsWatcherNodeConfiguration** cmdlet), or at any time after that.</span></span> <span data-ttu-id="7f2fd-119">La plupart des transactions synthétiques non par défaut nécessitent des étapes de configuration supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="7f2fd-119">Many of the Non-default synthetic transactions require extra setup steps.</span></span> <span data-ttu-id="7f2fd-120">Pour plus d’informations, consultez les [instructions de configuration spéciales pour les transactions synthétiques dans Lync Server 2013](lync-server-2013-special-setup-instructions-for-synthetic-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="7f2fd-120">For details, see [Special setup instructions for synthetic transactions in Lync Server 2013](lync-server-2013-special-setup-instructions-for-synthetic-transactions.md).</span></span>

  - <span data-ttu-id="7f2fd-121">**Étendu**.</span><span class="sxs-lookup"><span data-stu-id="7f2fd-121">**Extended**.</span></span> <span data-ttu-id="7f2fd-122">Les tests étendus constituent un type spécial de transaction synthétique autre qu’une valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="7f2fd-122">Extended tests are a special type of Non-default synthetic transaction.</span></span> <span data-ttu-id="7f2fd-123">Contrairement à d’autres transactions synthétiques, les tests étendus peuvent être exécutés plusieurs fois à chaque passage.</span><span class="sxs-lookup"><span data-stu-id="7f2fd-123">Unlike other synthetic transactions, Extended tests can be run multiple times during each pass.</span></span> <span data-ttu-id="7f2fd-124">Cela peut s’avérer utile lors de la vérification du comportement par le biais de plusieurs itinéraires vocaux sur un réseau téléphonique commuté (PSTN) pour un pool.</span><span class="sxs-lookup"><span data-stu-id="7f2fd-124">This can be useful when verifying behavior such as multiple public switched telephone network (PSTN) voice routes for a pool.</span></span> <span data-ttu-id="7f2fd-125">Pour le configurer, il suffit d’ajouter plusieurs instances d’un test étendu à un nœud d’observateur.</span><span class="sxs-lookup"><span data-stu-id="7f2fd-125">This can be configured simply by adding multiple instances of an Extended test to a watcher node.</span></span>

<span data-ttu-id="7f2fd-126">Pour plus d’informations sur la procédure d’ajout d’autres transactions synthétiques à un nœud d’observation, voir [gestion des nœuds d’observation dans Lync Server 2013](lync-server-2013-managing-watcher-nodes.md).</span><span class="sxs-lookup"><span data-stu-id="7f2fd-126">For details about the process of adding other synthetic transactions to a watcher node, see [Managing watcher nodes in Lync Server 2013](lync-server-2013-managing-watcher-nodes.md).</span></span> <span data-ttu-id="7f2fd-127">Vous pouvez utiliser Lync Server Management Shell pour supprimer des transactions synthétiques d’un nœud d’observateur.</span><span class="sxs-lookup"><span data-stu-id="7f2fd-127">You can use the Lync Server Management Shell to remove synthetic transactions from a watcher node.</span></span>

<span data-ttu-id="7f2fd-128">Les transactions synthétiques accessibles aux nœuds observateur sont, par exemple :</span><span class="sxs-lookup"><span data-stu-id="7f2fd-128">The synthetic transactions available to watcher nodes include the following:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7f2fd-129">Nom de l’applet de commande (nom du test)</span><span class="sxs-lookup"><span data-stu-id="7f2fd-129">Cmdlet Name (Test Name)</span></span></th>
<th><span data-ttu-id="7f2fd-130">Description</span><span class="sxs-lookup"><span data-stu-id="7f2fd-130">Description</span></span></th>
<th><span data-ttu-id="7f2fd-131">Type de transaction synthétique</span><span class="sxs-lookup"><span data-stu-id="7f2fd-131">Synthetic Transaction Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7f2fd-132">Test-CsAddressBookService (ABS)</span><span class="sxs-lookup"><span data-stu-id="7f2fd-132">Test-CsAddressBookService (ABS)</span></span></p></td>
<td><p><span data-ttu-id="7f2fd-133">Confirmez que les utilisateurs peuvent chercher des utilisateurs qui ne figurent pas dans leur liste de contacts.</span><span class="sxs-lookup"><span data-stu-id="7f2fd-133">Confirms that users are able to look up users that aren’t in their contact list.</span></span></p></td>
<td><p><span data-ttu-id="7f2fd-134">Par défaut</span><span class="sxs-lookup"><span data-stu-id="7f2fd-134">Default</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f2fd-135">Test-CsAddressBookWebQuery (ABWQ)</span><span class="sxs-lookup"><span data-stu-id="7f2fd-135">Test-CsAddressBookWebQuery (ABWQ)</span></span></p></td>
<td><p><span data-ttu-id="7f2fd-136">Confirmez que les utilisateurs peuvent chercher des utilisateurs qui ne figurent pas dans leur liste de contacts par le biais du protocole HTTP.</span><span class="sxs-lookup"><span data-stu-id="7f2fd-136">Confirms that users are able to look up users that aren’t in their contact list via HTTP.</span></span></p></td>
<td><p><span data-ttu-id="7f2fd-137">Par défaut</span><span class="sxs-lookup"><span data-stu-id="7f2fd-137">Default</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f2fd-138">Test-CsIM (MESSAGERIE INSTANTANÉE)</span><span class="sxs-lookup"><span data-stu-id="7f2fd-138">Test-CsIM (IM)</span></span></p></td>
<td><p><span data-ttu-id="7f2fd-139">Confirme que les utilisateurs peuvent envoyer des messages instantanés P2P.</span><span class="sxs-lookup"><span data-stu-id="7f2fd-139">Confirms that users are able to send peer-to-peer instant messages.</span></span></p></td>
<td><p><span data-ttu-id="7f2fd-140">Par défaut</span><span class="sxs-lookup"><span data-stu-id="7f2fd-140">Default</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f2fd-141">Test-CsP2PAV (AV P2P)</span><span class="sxs-lookup"><span data-stu-id="7f2fd-141">Test-CsP2PAV (P2PAV)</span></span></p></td>
<td><p><span data-ttu-id="7f2fd-142">Confirme que les utilisateurs peuvent passer des appels audio P2P (signalisation uniquement).</span><span class="sxs-lookup"><span data-stu-id="7f2fd-142">Confirms that users are able to place peer-to-peer audio calls (signaling only).</span></span></p></td>
<td><p><span data-ttu-id="7f2fd-143">Par défaut</span><span class="sxs-lookup"><span data-stu-id="7f2fd-143">Default</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f2fd-144">Test-CsPresence (Présence)</span><span class="sxs-lookup"><span data-stu-id="7f2fd-144">Test-CsPresence (Presence)</span></span></p></td>
<td><p><span data-ttu-id="7f2fd-145">Confirme que les utilisateurs peuvent afficher la présence d’autres utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="7f2fd-145">Confirms that users are able to view other users’ presence.</span></span></p></td>
<td><p><span data-ttu-id="7f2fd-146">Par défaut</span><span class="sxs-lookup"><span data-stu-id="7f2fd-146">Default</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f2fd-147">Test-CsRegistration (Enregistrement)</span><span class="sxs-lookup"><span data-stu-id="7f2fd-147">Test-CsRegistration (Registration)</span></span></p></td>
<td><p><span data-ttu-id="7f2fd-148">Confirmez que les utilisateurs sont en mesure de se connecter à Lync.</span><span class="sxs-lookup"><span data-stu-id="7f2fd-148">Confirms that users are able sign in to Lync.</span></span></p></td>
<td><p><span data-ttu-id="7f2fd-149">Par défaut</span><span class="sxs-lookup"><span data-stu-id="7f2fd-149">Default</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f2fd-150">Test-CsAudioConferencingProvider (ACP)</span><span class="sxs-lookup"><span data-stu-id="7f2fd-150">Test-CsAudioConferencingProvider (ACP)</span></span></p></td>
<td><p><span data-ttu-id="7f2fd-151">Non utilisé avec la version locale de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7f2fd-151">Not used with the on-premises version of Lync Server 2013</span></span></p></td>
<td><p><span data-ttu-id="7f2fd-152">Étendu</span><span class="sxs-lookup"><span data-stu-id="7f2fd-152">Extended</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f2fd-153">Test-CsPstnPeerToPeerCall (RTC)</span><span class="sxs-lookup"><span data-stu-id="7f2fd-153">Test-CsPstnPeerToPeerCall (PSTN)</span></span></p></td>
<td><p><span data-ttu-id="7f2fd-154">Confirme que les utilisateurs peuvent passer des appels à des personnes à l’extérieur de l’entreprise et recevoir des appels de celles-ci (numéros RTC).</span><span class="sxs-lookup"><span data-stu-id="7f2fd-154">Confirms that users are able to place and receive calls with people outside of the enterprise (PSTN numbers).</span></span></p></td>
<td><p><span data-ttu-id="7f2fd-155">Non définie par défaut, étendu</span><span class="sxs-lookup"><span data-stu-id="7f2fd-155">Non-default, Extended</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f2fd-156">Test-CsAVConference (AvConference)</span><span class="sxs-lookup"><span data-stu-id="7f2fd-156">Test-CsAVConference (AvConference)</span></span></p></td>
<td><p><span data-ttu-id="7f2fd-157">Confirme que les utilisateurs peuvent créer des conférences audio/vidéo et y participer.</span><span class="sxs-lookup"><span data-stu-id="7f2fd-157">Confirms that users are able to create and participate in an audio/video conference.</span></span></p></td>
<td><p><span data-ttu-id="7f2fd-158">Par défaut</span><span class="sxs-lookup"><span data-stu-id="7f2fd-158">Default</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f2fd-159">Test-CsAVEdgeConnectivity (AVEdgeConnectivity)</span><span class="sxs-lookup"><span data-stu-id="7f2fd-159">Test-CsAVEdgeConnectivity (AVEdgeConnectivity)</span></span></p></td>
<td><p><span data-ttu-id="7f2fd-160">Vérifie que les serveurs Edge A/V peuvent accepter des connexions pour les appels d’égal à égal et les téléconférences.</span><span class="sxs-lookup"><span data-stu-id="7f2fd-160">Confirms that the A/V Edge servers are able to accept connections for peer-to-peer calls and conference calls.</span></span></p></td>
<td><p><span data-ttu-id="7f2fd-161">Non définie par défaut</span><span class="sxs-lookup"><span data-stu-id="7f2fd-161">Non-default</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f2fd-162">Test-CsDataConference (DataConference)</span><span class="sxs-lookup"><span data-stu-id="7f2fd-162">Test-CsDataConference (DataConference)</span></span></p></td>
<td><p><span data-ttu-id="7f2fd-163">Confirme que les utilisateurs peuvent participer à une conférence de collaboration de données, une réunion en ligne incluant des activités telles que des tableaux blancs et des sondages.</span><span class="sxs-lookup"><span data-stu-id="7f2fd-163">Confirms that users can participate in a data collaboration conference, an online meeting that includes activities such as whiteboards and polls.</span></span></p></td>
<td><p><span data-ttu-id="7f2fd-164">Non définie par défaut</span><span class="sxs-lookup"><span data-stu-id="7f2fd-164">Non-default</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f2fd-165">Test-CsExumConnectivity (ExumConnectivity)</span><span class="sxs-lookup"><span data-stu-id="7f2fd-165">Test-CsExumConnectivity (ExumConnectivity)</span></span></p></td>
<td><p><span data-ttu-id="7f2fd-166">Confirmez que l’utilisateur peut se connecter à la messagerie unifiée Exchange.</span><span class="sxs-lookup"><span data-stu-id="7f2fd-166">Confirms that a user can connect to Exchange Unified Messaging (UM).</span></span></p></td>
<td><p><span data-ttu-id="7f2fd-167">Non définie par défaut</span><span class="sxs-lookup"><span data-stu-id="7f2fd-167">Non-default</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f2fd-168">Test-CsGroupIM (GroupIM)</span><span class="sxs-lookup"><span data-stu-id="7f2fd-168">Test-CsGroupIM (GroupIM)</span></span></p></td>
<td><p><span data-ttu-id="7f2fd-169">Confirme que les utilisateurs peuvent envoyer des messages instantanés dans des conférences et participer à des conversations par messagerie instantanée comptant trois personnes ou plus.</span><span class="sxs-lookup"><span data-stu-id="7f2fd-169">Confirms that users are able to send instant messages in conferences and participate in instant message conversations with three or more people.</span></span></p></td>
<td><p><span data-ttu-id="7f2fd-170">Par défaut</span><span class="sxs-lookup"><span data-stu-id="7f2fd-170">Default</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f2fd-171">Test-CsGroupIM –TestJoinLauncher (JoinLauncher)</span><span class="sxs-lookup"><span data-stu-id="7f2fd-171">Test-CsGroupIM –TestJoinLauncher (JoinLauncher)</span></span></p></td>
<td><p><span data-ttu-id="7f2fd-172">Confirme que les utilisateurs peuvent créer et rejoindre des réunions planifiées par le biais d’un lien d’adresse Web.</span><span class="sxs-lookup"><span data-stu-id="7f2fd-172">Confirms that users are able to create and join scheduled meetings via a web address link.</span></span></p></td>
<td><p><span data-ttu-id="7f2fd-173">Non définie par défaut</span><span class="sxs-lookup"><span data-stu-id="7f2fd-173">Non-default</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f2fd-174">Test-CsMCXP2PIM (MCXP2PIM)</span><span class="sxs-lookup"><span data-stu-id="7f2fd-174">Test-CsMCXP2PIM (MCXP2PIM)</span></span></p></td>
<td><p><span data-ttu-id="7f2fd-175">Confirme que les utilisateurs d’appareil mobile peuvent s’enregistrer et envoyer des messages instantanés.</span><span class="sxs-lookup"><span data-stu-id="7f2fd-175">Confirms that mobile device users are able to register and send instant messages.</span></span></p></td>
<td><p><span data-ttu-id="7f2fd-176">Non définie par défaut</span><span class="sxs-lookup"><span data-stu-id="7f2fd-176">Non-default</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f2fd-177">Test-CsPersistentChatMessage (PersistentChatMessage)</span><span class="sxs-lookup"><span data-stu-id="7f2fd-177">Test-CsPersistentChatMessage (PersistentChatMessage)</span></span></p></td>
<td><p><span data-ttu-id="7f2fd-178">Confirme que les utilisateurs peuvent échanger des messages à l’aide du service de conversation permanente.</span><span class="sxs-lookup"><span data-stu-id="7f2fd-178">Confirms that users can exchange messages by using the Persistent Chat service.</span></span></p></td>
<td><p><span data-ttu-id="7f2fd-179">Non définie par défaut</span><span class="sxs-lookup"><span data-stu-id="7f2fd-179">Non-default</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f2fd-180">Test-CsUnifiedContactStore (UnifiedContactStore)</span><span class="sxs-lookup"><span data-stu-id="7f2fd-180">Test-CsUnifiedContactStore (UnifiedContactStore)</span></span></p></td>
<td><p><span data-ttu-id="7f2fd-181">Confirme que les contacts d’un utilisateur sont accessibles par le biais du magasin de contacts unifié.</span><span class="sxs-lookup"><span data-stu-id="7f2fd-181">Confirms that a user's contacts can be accessed through the unified contact store.</span></span> <span data-ttu-id="7f2fd-182">Le magasin de contacts unifié offre aux utilisateurs la possibilité de mettre à jour un ensemble unique de contacts accessibles via Lync 2013, Outlook et/ou Outlook Web Access.</span><span class="sxs-lookup"><span data-stu-id="7f2fd-182">The unified contact store provides a way for users to maintain a single set of contacts that can be accessed by using Lync 2013, Outlook, and/or Outlook Web Access.</span></span></p></td>
<td><p><span data-ttu-id="7f2fd-183">Non définie par défaut</span><span class="sxs-lookup"><span data-stu-id="7f2fd-183">Non-default</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f2fd-184">Test-CsXmppIM (XmppIM)</span><span class="sxs-lookup"><span data-stu-id="7f2fd-184">Test-CsXmppIM (XmppIM)</span></span></p></td>
<td><p><span data-ttu-id="7f2fd-185">Confirme qu’un message instantané peut être envoyé sur la passerelle XMPP (extensible Messaging and Presence Protocol).</span><span class="sxs-lookup"><span data-stu-id="7f2fd-185">Confirms that an instant message can be sent across the XMPP (Extensible Messaging and Presence Protocol) gateway.</span></span></p></td>
<td><p><span data-ttu-id="7f2fd-186">Non définie par défaut</span><span class="sxs-lookup"><span data-stu-id="7f2fd-186">Non-default</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7f2fd-187">Vous n’avez pas besoin d’installer de nœuds FileSystemWatcher pour pouvoir utiliser System Center Operations Manager.</span><span class="sxs-lookup"><span data-stu-id="7f2fd-187">You do not need to install watcher nodes in order to use System Center Operations Manager.</span></span> <span data-ttu-id="7f2fd-188">Si vous n’avez pas installé ces nœuds, vous pouvez toujours obtenir des alertes en temps réel des composants Lync Server 2013 quand un problème survient.</span><span class="sxs-lookup"><span data-stu-id="7f2fd-188">If you do not install these nodes, you can still get real-time alerts from Lync Server 2013 components when an issue occurs.</span></span> <span data-ttu-id="7f2fd-189">(Le composant et le module de gestion des utilisateurs n’utilisent pas de nœuds FileSystemWatcher.) En revanche, les nœuds d’observation sont requis si vous souhaitez surveiller les scénarios de bout en bout à l’aide du pack d’administration actif.</span><span class="sxs-lookup"><span data-stu-id="7f2fd-189">(The Component and User Management Pack does not use watcher nodes.) However, watcher nodes are required if you want to monitor end-to-end scenarios by using the Active Monitoring Management pack.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="7f2fd-190">Les administrateurs peuvent également exécuter des transactions synthétiques manuellement, sans avoir besoin d’utiliser, ou d’installer, Operations Manager.</span><span class="sxs-lookup"><span data-stu-id="7f2fd-190">Administrators can also run synthetic transactions manually, without needing to use, or install, Operations Manager.</span></span> <span data-ttu-id="7f2fd-191">Pour plus d’informations sur les différentes cmdlets Test-Cs, voir l' <A href="https://docs.microsoft.com/powershell/module/skype/?view=skype-ps">index des applets de applet de Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="7f2fd-191">For details about the various Test-Cs cmdlets, see the <A href="https://docs.microsoft.com/powershell/module/skype/?view=skype-ps">Lync Server 2013 cmdlets index</A>.</span></span>



</div>

<span data-ttu-id="7f2fd-192">En fonction de la taille de votre déploiement, les transactions synthétiques pourraient utiliser une grande quantité de mémoire de l’ordinateur et du temps processeur.</span><span class="sxs-lookup"><span data-stu-id="7f2fd-192">Depending on the size of your deployment, synthetic transactions may use a large amount of computer memory and processor time.</span></span> <span data-ttu-id="7f2fd-193">Pour cette raison, nous vous recommandons d’utiliser un ordinateur dédié en tant que nœud d’observation.</span><span class="sxs-lookup"><span data-stu-id="7f2fd-193">For this reason, we recommend that you use a dedicated computer as a watcher node.</span></span> <span data-ttu-id="7f2fd-194">Par exemple, vous ne devez pas configurer un serveur frontal pour qu’il serve de nœud d’observation.</span><span class="sxs-lookup"><span data-stu-id="7f2fd-194">For example, you should not configure a Front End Server to act as a watcher node.</span></span> <span data-ttu-id="7f2fd-195">Les nœuds d’observateur doivent respecter les spécifications matérielles suivantes :</span><span class="sxs-lookup"><span data-stu-id="7f2fd-195">Watcher nodes should meet the following hardware specifications:</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="7f2fd-196">Un nœud Microsoft Lync Server 2010 d’ancienne génération ne peut pas être localisé sur le même ordinateur qu’un nœud de l’observateur Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="7f2fd-196">A legacy Microsoft Lync Server 2010 watcher node cannot be collocated on the same machine with a Lync Server 2013 watcher node.</span></span> <span data-ttu-id="7f2fd-197">En effet, les principaux fichiers système pour Lync Server 2010 et Lync Server 2013 ne peuvent pas être installés sur le même ordinateur.</span><span class="sxs-lookup"><span data-stu-id="7f2fd-197">This is because the core system files for Lync Server 2010 and Lync Server 2013 cannot be installed on the same computer.</span></span><BR><span data-ttu-id="7f2fd-198">Toutefois, les nœuds d’observateur de Lync Server 2013 peuvent contrôler simultanément Lync Server 2013 et Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="7f2fd-198">However, Lync Server 2013 watcher nodes can simultaneously monitor both Lync Server 2013 and Lync Server 2010.</span></span> <span data-ttu-id="7f2fd-199">Les transactions synthétiques par défaut sont prises en charge sur les deux versions de produit.</span><span class="sxs-lookup"><span data-stu-id="7f2fd-199">The Default synthetic transactions are supported on both product versions.</span></span>



</div>

<span data-ttu-id="7f2fd-200">Les nœuds d’observateur Lync Server 2013 pourront être déployés à l’intérieur ou à l’extérieur d’une entreprise pour vous permettre de vérifier les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="7f2fd-200">Lync Server 2013 watcher nodes may be deployed inside or outside of an enterprise to help verify:</span></span>

  - <span></span>  
    <span data-ttu-id="7f2fd-201">Connectivité avec les pools pour les utilisateurs situés dans l’entreprise</span><span class="sxs-lookup"><span data-stu-id="7f2fd-201">Connectivity to pools for users inside the enterprise.</span></span>

  - <span></span>  
    <span data-ttu-id="7f2fd-202">Connectivité via des réseaux de périmètre pour les utilisateurs distants qui travaillent hors de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="7f2fd-202">Connectivity through perimeter networks for remote users who work outside the enterprise.</span></span>

  - <span></span>  
    <span data-ttu-id="7f2fd-203">Connectivité avec les Branch Office Appliances</span><span class="sxs-lookup"><span data-stu-id="7f2fd-203">Connectivity to branch office appliances.</span></span>

  - <span></span>  
    <span data-ttu-id="7f2fd-204">Connectivité à Lync Server 2010 au sein de l’entreprise et via des réseaux de périmètre.</span><span class="sxs-lookup"><span data-stu-id="7f2fd-204">Connectivity to Lync Server 2010 inside the enterprise and through perimeter networks.</span></span>

<span data-ttu-id="7f2fd-205">Différentes options d’authentification sont disponibles à l’intérieur et à l’extérieur de l’entreprise pour simplifier l’administration.</span><span class="sxs-lookup"><span data-stu-id="7f2fd-205">Different authentication options are available for inside and outside of the enterprise to help simplify administration.</span></span> <span data-ttu-id="7f2fd-206">Pour plus d’informations, reportez-vous [à la rubrique Configuration d’un nœud d’observateur pour exécuter des transactions synthétiques dans Lync Server 2013](lync-server-2013-configuring-a-watcher-node-to-run-synthetic-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="7f2fd-206">For details, see [Configuring a watcher node to run synthetic transactions in Lync Server 2013](lync-server-2013-configuring-a-watcher-node-to-run-synthetic-transactions.md).</span></span>

<span data-ttu-id="7f2fd-207">Pour configurer un ordinateur pour qu’il serve de nœud d’observation, vous devez effectuer les étapes suivantes une fois que vous avez installé System Center Operations Manager et importé les packs d’administration de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="7f2fd-207">To configure a computer to act as a watcher node, you must complete the following steps after you have installed System Center Operations Manager and imported the Lync Server 2013 management packs.</span></span>

<span data-ttu-id="7f2fd-208">Avant d’installer les fichiers principaux de Lync Server 2013 et les fichiers de l’agent System Center, assurez-vous que l’ordinateur de nœud d’observation répond à toutes les conditions préalables à l’installation de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="7f2fd-208">Before you install the Lync Server 2013 core files and the System Center agent files, you should also make sure that the watcher node computer meets all the prerequisites for installing Lync Server 2013.</span></span> <span data-ttu-id="7f2fd-209">Par ailleurs, les éléments suivants doivent également être installés sur l’ordinateur du nœud d’observation :</span><span class="sxs-lookup"><span data-stu-id="7f2fd-209">In addition, the watcher node computer should also have the following items installed:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7f2fd-210">Composant matériel</span><span class="sxs-lookup"><span data-stu-id="7f2fd-210">Hardware component</span></span></th>
<th><span data-ttu-id="7f2fd-211">Spécification minimale</span><span class="sxs-lookup"><span data-stu-id="7f2fd-211">Minimum requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7f2fd-212">Processeur</span><span class="sxs-lookup"><span data-stu-id="7f2fd-212">CPU</span></span></p></td>
<td><p><span data-ttu-id="7f2fd-213">L’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="7f2fd-213">One of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="7f2fd-214">Processeur 64 bits, quadruple cœur 2,33 GHz ou supérieur</span><span class="sxs-lookup"><span data-stu-id="7f2fd-214">64-bit processor, quad-core, 2.33 GHz or higher</span></span></p></li>
<li><p><span data-ttu-id="7f2fd-215">Processeur 64 bits à deux voies, double cœur, 2,33 GHz ou supérieur</span><span class="sxs-lookup"><span data-stu-id="7f2fd-215">64-bit 2-way processor, dual-core, 2.33 GHz or higher</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f2fd-216">Mémoire</span><span class="sxs-lookup"><span data-stu-id="7f2fd-216">Memory</span></span></p></td>
<td><p><span data-ttu-id="7f2fd-217">8 Go</span><span class="sxs-lookup"><span data-stu-id="7f2fd-217">8 GB</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f2fd-218">Système d’exploitation réseau</span><span class="sxs-lookup"><span data-stu-id="7f2fd-218">Network operating system</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="7f2fd-219">1 carte réseau 1 Gbps</span><span class="sxs-lookup"><span data-stu-id="7f2fd-219">1 network adapter 1 Gbps</span></span></p></li>
<li><p><span data-ttu-id="7f2fd-220">Windows Server 2008 R2, Windows Server 2012 ou</span><span class="sxs-lookup"><span data-stu-id="7f2fd-220">Windows Server 2008 R2, Windows Server 2012, or</span></span></p>
<p><span data-ttu-id="7f2fd-221">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="7f2fd-221">Windows Server 2012 R2</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


  - <span data-ttu-id="7f2fd-222">Version complète de .NET Framework 4,5.</span><span class="sxs-lookup"><span data-stu-id="7f2fd-222">The full version of .NET Framework 4.5.</span></span>

  - <span data-ttu-id="7f2fd-223">Windows Identity Foundation.</span><span class="sxs-lookup"><span data-stu-id="7f2fd-223">Windows Identity Foundation.</span></span>

  - <span data-ttu-id="7f2fd-224">Windows PowerShell 3,0.</span><span class="sxs-lookup"><span data-stu-id="7f2fd-224">Windows PowerShell 3.0.</span></span>

<span data-ttu-id="7f2fd-225">Dès que toutes les conditions préalables suivantes sont remplies, vous pouvez configurer le nœud de l’observateur en procédant comme suit :</span><span class="sxs-lookup"><span data-stu-id="7f2fd-225">As soon as all these prerequisites have been met, you can configure the watcher node by:</span></span>

  - <span data-ttu-id="7f2fd-226">Installation des fichiers principaux de Lync Server 2013 sur l’ordinateur de nœud d’observation.</span><span class="sxs-lookup"><span data-stu-id="7f2fd-226">Installing the Lync Server 2013 core files on the watcher node computer.</span></span>

  - <span data-ttu-id="7f2fd-227">Installation de l’agent System Center Operations Manager sur l’ordinateur du nœud d’observation.</span><span class="sxs-lookup"><span data-stu-id="7f2fd-227">Installing System Center Operations Manager agent on the watcher node computer.</span></span>

  - <span data-ttu-id="7f2fd-228">Exécution du fichier exécutable Watchernode.msi.</span><span class="sxs-lookup"><span data-stu-id="7f2fd-228">Running the Watchernode.msi executable file.</span></span>

  - <span data-ttu-id="7f2fd-229">Les applets de contrôle **CsWatcherNodeConfiguration** vous permettent de configurer les utilisateurs de test devant être utilisés par le nœud d’observation.</span><span class="sxs-lookup"><span data-stu-id="7f2fd-229">Using the **CsWatcherNodeConfiguration** cmdlets to configure test users to be employed by the watcher node.</span></span>

<span data-ttu-id="7f2fd-230"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7f2fd-230"></div>

<span> </span>

</div>

</div>

</span></span></div>

