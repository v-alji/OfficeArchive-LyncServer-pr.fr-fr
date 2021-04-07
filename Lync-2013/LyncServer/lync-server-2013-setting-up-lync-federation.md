---
title: 'Lync Server 2013 : Configuration de la fédération Lync'
description: 'Lync Server 2013 : configuration de la fédération Lync.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up Lync federation
ms:assetid: 374ddc43-26f9-499d-be68-a5158adfa49c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204800(v=OCS.15)
ms:contentKeyID: 48183822
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 382def41635f05525e5b047e97febffdb069da2a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395068"
---
# <a name="setting-up-lync-federation-in-lync-server-2013"></a><span data-ttu-id="f3271-103">Configuration de la fédération Lync dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f3271-103">Setting up Lync federation in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f3271-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f3271-104">

<span> </span></span></span>

<span data-ttu-id="f3271-105">_**Rubrique dernière modification :** 2014-03-27_</span><span class="sxs-lookup"><span data-stu-id="f3271-105">_**Topic Last Modified:** 2014-03-27_</span></span>

<span data-ttu-id="f3271-106">Si vous avez déjà déployé vos serveurs ou serveurs Edge, l’ajout des fonctionnalités de scénarios fédérés se fait directement.</span><span class="sxs-lookup"><span data-stu-id="f3271-106">If you have already deployed you Edge server or servers, adding the federated scenarios features is straight forward.</span></span> <span data-ttu-id="f3271-107">Si vous n’avez pas encore installé de serveurs Edge, vous devez d’abord le faire.</span><span class="sxs-lookup"><span data-stu-id="f3271-107">If you have not set up Edge Servers, you must do that first.</span></span> <span data-ttu-id="f3271-108">Pour plus d’informations, voir : Planification de l’accès des utilisateurs externes dans [Lync Server 2013](lync-server-2013-planning-for-external-user-access.md) dans la documentation Planification et Déploiement de l’accès des utilisateurs externes dans [Lync Server 2013](lync-server-2013-deploying-external-user-access.md) dans la documentation De déploiement.</span><span class="sxs-lookup"><span data-stu-id="f3271-108">For details, see: [Planning for external user access in Lync Server 2013](lync-server-2013-planning-for-external-user-access.md) in the Planning documentation and [Deploying external user access in Lync Server 2013](lync-server-2013-deploying-external-user-access.md) in the Deployment documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="f3271-109">Si vous envisagez de configurer une combinaison de fédération XMPP, de fédération Lync ou de connectivité de messagerie instantanée publique, vous pouvez les déployer simultanément ou une par une.</span><span class="sxs-lookup"><span data-stu-id="f3271-109">If you intend to setup any combination of XMPP federation, Lync Federation, or public instant messaging connectivity, you can deploy them concurrently or one at a time.</span></span> <span data-ttu-id="f3271-110">Si vous configurez les options via le Générateur de topologie et l’shell de gestion de Lync Server, puis exécutez l’Assistant Déploiement sur le serveur Edge après avoir configuré les options pour un, deux ou les trois types de fédération, vous pouvez réduire le nombre d’étapes requises.</span><span class="sxs-lookup"><span data-stu-id="f3271-110">If you configure the options through the Topology Builder and the Lync Server Management shell, then run the Deployment Wizard at the Edge server after configuring the options for one, two or all three federation types, you can reduce the number of steps required.</span></span>



</div>

<div>

## <a name="setting-up-lync-federation-in-topology-builder-and-the-deployment-wizard"></a><span data-ttu-id="f3271-111">Configuration de la fédération Lync dans le Générateur de topologie et l’Assistant Déploiement</span><span class="sxs-lookup"><span data-stu-id="f3271-111">Setting Up Lync Federation in Topology Builder and the Deployment Wizard</span></span>

1.  <span data-ttu-id="f3271-112">Sur un serveur frontal, ouvrez le Générateur de topologie.</span><span class="sxs-lookup"><span data-stu-id="f3271-112">On a Front End server, open Topology Builder.</span></span> <span data-ttu-id="f3271-113">Développez les pools Edge, puis cliquez avec le bouton droit sur votre serveur Edge ou votre pool de serveurs Edge.</span><span class="sxs-lookup"><span data-stu-id="f3271-113">Expand Edge pools, then right click your Edge server or Edge server pool.</span></span> <span data-ttu-id="f3271-114">Sélectionnez Modifier les propriétés.</span><span class="sxs-lookup"><span data-stu-id="f3271-114">Select Edit properties.</span></span>

2.  <span data-ttu-id="f3271-115">Dans Modifier les propriétés sous Général, sélectionnez Activer la fédération pour ce pool Edge (Port 5061).</span><span class="sxs-lookup"><span data-stu-id="f3271-115">In Edit Properties under General, select Enable federation for this Edge pool (Port 5061).</span></span> <span data-ttu-id="f3271-116">Cliquez sur OK.</span><span class="sxs-lookup"><span data-stu-id="f3271-116">Click OK.</span></span>

3.  <span data-ttu-id="f3271-117">Cliquez sur Action, sélectionnez Topologie, puis Publier.</span><span class="sxs-lookup"><span data-stu-id="f3271-117">Click Action, select Topology, select Publish.</span></span> <span data-ttu-id="f3271-118">Lorsque vous y est invité à publier la topologie, cliquez sur Suivant.</span><span class="sxs-lookup"><span data-stu-id="f3271-118">When prompted on Publish the topology, click Next.</span></span> <span data-ttu-id="f3271-119">Lorsque la publication est terminée, cliquez sur Terminer.</span><span class="sxs-lookup"><span data-stu-id="f3271-119">When the Publish is finished, click Finish.</span></span>

4.  <span data-ttu-id="f3271-120">Sur le serveur Edge, ouvrez l’Assistant Déploiement de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="f3271-120">On the Edge server, open the Lync Server Deployment wizard.</span></span> <span data-ttu-id="f3271-121">Cliquez sur Installer ou mettre à jour Lync Server System, puis sur Installer ou supprimer des composants Lync Server.</span><span class="sxs-lookup"><span data-stu-id="f3271-121">Click Install or Update Lync Server System, then click Setup or Remove Lync Server Components.</span></span> <span data-ttu-id="f3271-122">Cliquez sur Exécuter à nouveau.</span><span class="sxs-lookup"><span data-stu-id="f3271-122">Click Run Again.</span></span>

5.  <span data-ttu-id="f3271-123">Pour configurer les composants de Lync Server, cliquez sur Suivant.</span><span class="sxs-lookup"><span data-stu-id="f3271-123">At Setup Lync Server components, click Next.</span></span> <span data-ttu-id="f3271-124">L’écran de résumé affiche les actions au cours de leur exécution.</span><span class="sxs-lookup"><span data-stu-id="f3271-124">The summary screen will show actions as they are executed.</span></span> <span data-ttu-id="f3271-125">Une fois le déploiement terminé, cliquez sur Afficher le journal pour afficher les fichiers journaux disponibles.</span><span class="sxs-lookup"><span data-stu-id="f3271-125">Once the deployment is done, click View Log to view available log files.</span></span> <span data-ttu-id="f3271-126">Cliquez sur Terminer pour terminer le déploiement.</span><span class="sxs-lookup"><span data-stu-id="f3271-126">Click Finish to complete the deployment.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="f3271-127">Vous pouvez sélectionner cette option, mais un seul groupe Edge ou serveur Edge de votre organisation peut être publié en externe pour la fédération.</span><span class="sxs-lookup"><span data-stu-id="f3271-127">You can select this option, but only one Edge pool or Edge Server in your organization can be published externally for federation.</span></span> <span data-ttu-id="f3271-128">Tout l’accès par les utilisateurs fédérés, y compris les utilisateurs de messagerie instantanée publique, passe par le même pool Edge ou le même serveur Edge.</span><span class="sxs-lookup"><span data-stu-id="f3271-128">All access by federated users, including public instant messaging (IM) users, go through the same Edge pool or single Edge Server.</span></span> <span data-ttu-id="f3271-129">Par exemple, si votre déploiement inclut un pool Edge ou un serveur Edge unique déployé à New York et un serveur déployé à Londres et que vous activez la prise en charge de la fédération sur le pool Edge de New York ou le serveur Edge unique, le trafic de signal des utilisateurs fédérés passe par le pool Edge de New York ou le serveur Edge unique.</span><span class="sxs-lookup"><span data-stu-id="f3271-129">For example, if your deployment includes an Edge pool or single Edge Server deployed in New York and one deployed in London and you enable federation support on the New York Edge pool or single Edge Server, signal traffic for federated users will go through the New York Edge pool or single Edge Server.</span></span> <span data-ttu-id="f3271-130">Cela s’applique également aux communications avec les utilisateurs de Londres, même si un utilisateur interne de Londres qui appelle un utilisateur fédéré de Londres utilise le pool de serveurs ou le serveur Edge de Londres pour le trafic A/V.</span><span class="sxs-lookup"><span data-stu-id="f3271-130">This is true even for communications with London users, although a London internal user calling a London federated user uses the London pool or Edge Server for A/V traffic.</span></span>

    
    </div>

</div>

<div>

## <a name="configuring-federation-with-partners"></a><span data-ttu-id="f3271-131">Configuration de la fédération avec des partenaires</span><span class="sxs-lookup"><span data-stu-id="f3271-131">Configuring Federation with Partners</span></span>

1.  <span data-ttu-id="f3271-132">Pour configurer une fédération réussie avec un autre Microsoft Lync Server 2013, Lync Server 2010, Office Communications Server 2007 R2 ou Office Communicator 2007, sélectionnez le type de fédération dans le tableau suivant et définissez les enregistrements SRV DNS, hôte DNS (A ou AAAA pour IPv6) et configurez les stratégies applicables au type de fédération :</span><span class="sxs-lookup"><span data-stu-id="f3271-132">To setup a successful federation with another Microsoft Lync Server 2013, Lync Server 2010, Office Communications Server 2007 R2, or Office Communicator 2007, select the type of federation from the following table and define DNS SRV records, DNS host (A or AAAA for IPv6) and configure policies applicable to the type of federation:</span></span>
    
    
    <table>
    <colgroup>
    <col style="width: 25%" />
    <col style="width: 25%" />
    <col style="width: 25%" />
    <col style="width: 25%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="f3271-133">Type de fédération</span><span class="sxs-lookup"><span data-stu-id="f3271-133">Federation type</span></span></th>
    <th><span data-ttu-id="f3271-134">Enregistrements DNS</span><span class="sxs-lookup"><span data-stu-id="f3271-134">DNS Records</span></span></th>
    <th><span data-ttu-id="f3271-135">Définition de stratégie</span><span class="sxs-lookup"><span data-stu-id="f3271-135">Policy Definition</span></span></th>
    <th><span data-ttu-id="f3271-136">Remarques</span><span class="sxs-lookup"><span data-stu-id="f3271-136">Notes</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="f3271-137">Domaine partenaire découvert</span><span class="sxs-lookup"><span data-stu-id="f3271-137">Discovered Partner Domain</span></span></p></td>
    <td><p><span data-ttu-id="f3271-138">Configurez l’enregistrement SRV du format _sipfederationtls._tcp. &lt; nom de domaine externe Où la valeur de port de l’enregistrement SRV est &gt; TCP 5061 et où l’hôte offrant ce <strong>service</strong> est défini comme sip.</span><span class="sxs-lookup"><span data-stu-id="f3271-138">Configure SRV record of the format _sipfederationtls._tcp.&lt;external domain name&gt;Where the port value for the SRV record is TCP 5061 and the <strong>Host offering this service</strong> is defined as sip.</span></span> <span data-ttu-id="f3271-139">&lt;nom de domaine &gt; externe (FQDN) de votre service Edge Access.</span><span class="sxs-lookup"><span data-stu-id="f3271-139">&lt;external domain name&gt; – the FQDN of your Access Edge service.</span></span> <span data-ttu-id="f3271-140">Pour plus d’informations sur la création de l’enregistrement SRV, voir Configurer le DNS pour la prise en charge de Edge dans <a href="lync-server-2013-configure-dns-for-edge-support.md">Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="f3271-140">See <a href="lync-server-2013-configure-dns-for-edge-support.md">Configure DNS for edge support in Lync Server 2013</a> for details on creating the SRV record</span></span></p></td>
    <td><ul>
    <li><p><span data-ttu-id="f3271-141"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Activation ou désactivation de la fédération et de la connectivité PIC dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="f3271-141"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Enable or disable federation and public IM connectivity in Lync Server 2013</a></span></span></p></li>
    <li><p><span data-ttu-id="f3271-142"><a href="lync-server-2013-enable-or-disable-discovery-of-federation-partners.md">Activation ou désactivation de la découverte de partenaires de fédération dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="f3271-142"><a href="lync-server-2013-enable-or-disable-discovery-of-federation-partners.md">Enable or disable discovery of federation partners in Lync Server 2013</a></span></span></p></li>
    </ul></td>
    <td><p><span data-ttu-id="f3271-143">Les versions précédentes ont fait référence à ce type de fédération <strong>appelée Open Enhanced Federation.</strong></span><span class="sxs-lookup"><span data-stu-id="f3271-143">Previous versions referred to this type of federation as <strong>Open Enhanced Federation</strong>.</span></span> <span data-ttu-id="f3271-144">La création de l’enregistrement SRV est requise pour ce type de fédération et permet à d’autres partenaires de découvrir votre fédération.</span><span class="sxs-lookup"><span data-stu-id="f3271-144">The creation of the SRV record is required for this type of federation and is to allow other partners to discover your federation.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="f3271-145">Domaine partenaire autorisé</span><span class="sxs-lookup"><span data-stu-id="f3271-145">Allowed Partner Domain</span></span></p></td>
    <td><p><span data-ttu-id="f3271-146">Configurez l’enregistrement SRV du format _sipfederationtls._tcp. &lt; nom de domaine externe Où la valeur de port de l’enregistrement SRV est &gt; TCP 5061 et où l’hôte offrant ce <strong>service</strong> est défini comme sip.</span><span class="sxs-lookup"><span data-stu-id="f3271-146">Configure SRV record of the format _sipfederationtls._tcp.&lt;external domain name&gt;Where the port value for the SRV record is TCP 5061 and the <strong>Host offering this service</strong> is defined as sip.</span></span> <span data-ttu-id="f3271-147">&lt;nom de domaine &gt; externe (FQDN) de votre service Edge Access.</span><span class="sxs-lookup"><span data-stu-id="f3271-147">&lt;external domain name&gt; – the FQDN of your Access Edge service.</span></span> <span data-ttu-id="f3271-148">Pour plus d’informations sur la création de l’enregistrement SRV, voir Configurer le DNS pour la prise en charge de Edge dans <a href="lync-server-2013-configure-dns-for-edge-support.md">Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="f3271-148">See <a href="lync-server-2013-configure-dns-for-edge-support.md">Configure DNS for edge support in Lync Server 2013</a> for details on creating the SRV record</span></span></p></td>
    <td><ul>
    <li><p><span data-ttu-id="f3271-149"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Activation ou désactivation de la fédération et de la connectivité PIC dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="f3271-149"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Enable or disable federation and public IM connectivity in Lync Server 2013</a></span></span></p></li>
    </ul></td>
    <td><p><span data-ttu-id="f3271-150">Les versions précédentes ont fait référence à ce type de fédération appelée <strong>fédération améliorée.</strong></span><span class="sxs-lookup"><span data-stu-id="f3271-150">Previous versions referred to this type of federation as <strong>Enhanced Federation</strong>.</span></span> <span data-ttu-id="f3271-151">La création de l’enregistrement SRV est facultative pour ce type de fédération et permet à d’autres partenaires de découvrir votre fédération.</span><span class="sxs-lookup"><span data-stu-id="f3271-151">The creation of the SRV record is optional for this type of federation and is to allow other partners to discover your federation.</span></span> <span data-ttu-id="f3271-152">Bien entendu, il s’agit alors <strong>d’une fédération</strong>open enhanced ou du domaine partenaire <strong>découvert.</strong></span><span class="sxs-lookup"><span data-stu-id="f3271-152">Of course, this is then an <strong>Open Enhanced Federation</strong>, or <strong>Discovered Partner Domain</strong></span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="f3271-153">Serveur partenaire autorisé</span><span class="sxs-lookup"><span data-stu-id="f3271-153">Allowed Partner Server</span></span></p></td>
    <td><p><span data-ttu-id="f3271-154">Configurer le nom de domaine SIP et le nom de domaine complet du partenaire Edge Server en tant que partenaire de fédération dans Stratégies</span><span class="sxs-lookup"><span data-stu-id="f3271-154">Configure the SIP domain name and the partner Edge Server FQDN as a federation partner in Policies</span></span></p></td>
    <td><ul>
    <li><p><span data-ttu-id="f3271-155"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Activation ou désactivation de la fédération et de la connectivité PIC dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="f3271-155"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Enable or disable federation and public IM connectivity in Lync Server 2013</a></span></span></p></li>
    <li><p><span data-ttu-id="f3271-156"><a href="lync-server-2013-configure-support-for-allowed-external-domains.md">Configuration de la prise en charge des domaines externes autorisés dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="f3271-156"><a href="lync-server-2013-configure-support-for-allowed-external-domains.md">Configure support for allowed external domains in Lync Server 2013</a></span></span></p></li>
    <li><p><span data-ttu-id="f3271-157"><a href="lync-server-2013-configure-support-for-blocked-external-domains.md">Configuration de la prise en charge pour les domaines externes bloqués dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="f3271-157"><a href="lync-server-2013-configure-support-for-blocked-external-domains.md">Configure support for blocked external domains in Lync Server 2013</a></span></span></p></li>
    </ul></td>
    <td><p><span data-ttu-id="f3271-158">Ce type de fédération est la définition d’une relation un à un et ne permet pas de découvrir d’autres partenaires de fédération.</span><span class="sxs-lookup"><span data-stu-id="f3271-158">This federation type is the definition of a one to one relationship and does not allow for discovery of other federation partners.</span></span> <span data-ttu-id="f3271-159">Chaque partenaire de fédération est configuré de manière explicite.</span><span class="sxs-lookup"><span data-stu-id="f3271-159">Each federation partner is configured explicitly.</span></span> <span data-ttu-id="f3271-160">Dans les versions précédentes, il s’agissait de fédération <strong>directe</strong></span><span class="sxs-lookup"><span data-stu-id="f3271-160">In previous versions, this was known as <strong>Direct Federation</strong></span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="f3271-161">Fournisseur d’hébergement et fournisseur de messagerie instantanée publique</span><span class="sxs-lookup"><span data-stu-id="f3271-161">Hosting Provider and Public IM Provider</span></span></p></td>
    <td><p><span data-ttu-id="f3271-162">Aucune exigences DNS spécifique n’est définie pour ce type de fédération</span><span class="sxs-lookup"><span data-stu-id="f3271-162">No specific DNS requirements are defined for this type of federation</span></span></p></td>
    <td><ul>
    <li><p><span data-ttu-id="f3271-163"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Activation ou désactivation de la fédération et de la connectivité PIC dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="f3271-163"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Enable or disable federation and public IM connectivity in Lync Server 2013</a></span></span></p></li>
    <li><p><span data-ttu-id="f3271-164"><a href="lync-server-2013-create-or-edit-public-sip-federated-providers.md">Création ou modification des fournisseurs fédérés SIP publics dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="f3271-164"><a href="lync-server-2013-create-or-edit-public-sip-federated-providers.md">Create or edit public SIP federated providers in Lync Server 2013</a></span></span></p></li>
    <li><p><span data-ttu-id="f3271-165"><a href="lync-server-2013-create-or-edit-hosted-sip-federated-providers.md">Création ou modification des fournisseurs fédérés SIP hébergés dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="f3271-165"><a href="lync-server-2013-create-or-edit-hosted-sip-federated-providers.md">Create or edit hosted SIP federated providers Lync Server 2013</a></span></span></p></li>
    </ul></td>
    <td><p><span data-ttu-id="f3271-166">Ce type de fédération définit les services et fournisseurs d’hébergement que vous voulez configurer pour vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="f3271-166">This federation type defines services and hosting providers that you want to configure for your users.</span></span> <span data-ttu-id="f3271-167">Les utilisations classiques incluent la configuration de fournisseurs de messagerie instantanée publique tels Windows Live Messenger, Yahoo!</span><span class="sxs-lookup"><span data-stu-id="f3271-167">Typical uses include configuration for public IM providers like Windows Live Messenger, Yahoo!</span></span> <span data-ttu-id="f3271-168">et AOL, ainsi que des fournisseurs d’hébergement tels que Lync Online et Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="f3271-168">and AOL, as well as hosting providers such as Lync Online and Microsoft 365</span></span></p>
    <div>

    > [!IMPORTANT]  
    > <UL>
    > <LI>
    > <P><span data-ttu-id="f3271-169">À compter du 1er septembre 2012, la licence d’abonnement utilisateur Microsoft Lync Public IM Connectivity (« PIC USL ») n’est plus disponible à l’achat pour les nouveaux contrats ou le renouvellement.</span><span class="sxs-lookup"><span data-stu-id="f3271-169">As of September 1st, 2012, the Microsoft Lync Public IM Connectivity User Subscription License (“PIC USL”) is no longer available for purchase for new or renewing agreements.</span></span> <span data-ttu-id="f3271-170">Les clients titulaires d’une licence active pourront continuer à se fédérer avec Yahoo!</span><span class="sxs-lookup"><span data-stu-id="f3271-170">Customers with active licenses will be able to continue to federate with Yahoo!</span></span> <span data-ttu-id="f3271-171">Messenger jusqu’à la date d’arrêt du service.</span><span class="sxs-lookup"><span data-stu-id="f3271-171">Messenger until the service shut down date.</span></span> <span data-ttu-id="f3271-172">Date de fin de vie en juin 2014 pour AOL et Yahoo!</span><span class="sxs-lookup"><span data-stu-id="f3271-172">An end of life date of June 2014 for AOL and Yahoo!</span></span> <span data-ttu-id="f3271-173">a été annoncé.</span><span class="sxs-lookup"><span data-stu-id="f3271-173">has been announced.</span></span> <span data-ttu-id="f3271-174">Pour plus d’informations, consultez la prise en charge de la connectivité de messagerie instantanée publique dans <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Lync Server 2013.</A></span><span class="sxs-lookup"><span data-stu-id="f3271-174">For details, see <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Support for public instant messenger connectivity in Lync Server 2013</A>.</span></span></P>
    > <LI>
    > <P><span data-ttu-id="f3271-175">L’outil PIC USL est une licence d’abonnement par utilisateur et par mois requise pour que Lync Server ou Office Communications Server se fédérer avec Yahoo!</span><span class="sxs-lookup"><span data-stu-id="f3271-175">The PIC USL is a per-user per-month subscription license that is required for Lync Server or Office Communications Server to federate with Yahoo!</span></span> <span data-ttu-id="f3271-176">Messenger.</span><span class="sxs-lookup"><span data-stu-id="f3271-176">Messenger.</span></span> <span data-ttu-id="f3271-177">La capacité de Microsoft à fournir ce service a été prise en charge par Yahoo!, le contrat sous-jacent pour lequel il est en cours de liquidation.</span><span class="sxs-lookup"><span data-stu-id="f3271-177">Microsoft’s ability to provide this service has been contingent upon support from Yahoo!, the underlying agreement for which is winding down.</span></span></P>
    > <LI>
    > <P><span data-ttu-id="f3271-178">Plus que jamais, Lync est un outil puissant permettant de communiquer entre les organisations et les individus dans le monde entier.</span><span class="sxs-lookup"><span data-stu-id="f3271-178">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="f3271-179">La fédération avec d Windows Live Messenger ne nécessite aucune licence utilisateur/appareil supplémentaire au-delà de la licence d’accès client standard de Lync.</span><span class="sxs-lookup"><span data-stu-id="f3271-179">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard CAL.</span></span> <span data-ttu-id="f3271-180">La fédération Skype sera ajoutée à cette liste, ce qui permettra aux utilisateurs de Lync d’atteindre des centaines de millions de personnes avec la messagerie instantanée et la voix.</span><span class="sxs-lookup"><span data-stu-id="f3271-180">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people with IM and voice.</span></span></P></LI></UL>


    </div></td>
    </tr>
    </tbody>
    </table>


2.  <span data-ttu-id="f3271-181">Définir et configurer les enregistrements SRV DNS requis (A ou AAAA pour IPv6) et DNS</span><span class="sxs-lookup"><span data-stu-id="f3271-181">Define and configure any required DNS host (A or AAAA for IPv6) and DNS SRV records</span></span>

3.  <span data-ttu-id="f3271-182">Définissez et configurez les stratégies à l’aide du Panneau de configuration de Lync Server ou à l’aide de Lync Server Management Shell et des cmdlets appropriées.</span><span class="sxs-lookup"><span data-stu-id="f3271-182">Define and configure any policies using the Lync Server Control Panel or by using the Lync Server Management Shell and the appropriate cmdlets.</span></span> <span data-ttu-id="f3271-183">Pour plus d’informations sur les cmdlets Lync Server Management Shell, voir les cmdlets de fédération et d’accès externe dans [Lync Server 2013](https://docs.microsoft.com/powershell/module/skype/)</span><span class="sxs-lookup"><span data-stu-id="f3271-183">For details on the Lync Server Management Shell cmdlets, see [Federation and external access cmdlets in Lync Server 2013](https://docs.microsoft.com/powershell/module/skype/)</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="f3271-184">Lync Room System (LRS) n’affiche pas le bouton Rejoindre pour les réunions envoyées par les organisateurs dans des partenaires Lync fédérés.</span><span class="sxs-lookup"><span data-stu-id="f3271-184">Lync Room System (LRS) does not show join button for meetings sent by organizers in federated Lync partners.</span></span> <span data-ttu-id="f3271-185">Pour qu’un lien d’accès à une réunion s’affiche sur LRS, l’organisation d’envoi doit activer le TNEF à l’aide de l’cmdlet suivante :</span><span class="sxs-lookup"><span data-stu-id="f3271-185">For a meeting join link to appear on LRS, the sending organization must enable TNEF by using the following cmdlet:</span></span><BR><BR><CODE>New-RemoteDomain -DomainName Contoso.com -Name Contoso</CODE><BR><CODE>Set-RemoteDomain -Identity Contoso -TNEFEnabled $true</CODE><BR><span data-ttu-id="f3271-186">Notez que ce n’est pas spécifique au LRS.</span><span class="sxs-lookup"><span data-stu-id="f3271-186">Note that this is not LRS specific.</span></span> <span data-ttu-id="f3271-187">Outlook et Lync n’afficheront pas non plus de liens de participer dans ce cas, car les propriétés MAPI ne sont pas transportées, mais dans le cas Outlook, l’utilisateur peut ouvrir l’invitation à la réunion et cliquer sur l’URL de la réunion.</span><span class="sxs-lookup"><span data-stu-id="f3271-187">Outlook and Lync would also not show Join links in this case as MAPI properties are not transported, but in the Outlook case, the user can open up the meeting invite and click on the meeting URL.</span></span> <span data-ttu-id="f3271-188">Lorsque TNEFEnabled est définie sur true Exchange 2013 ne déconnecte pas les propriétés MAPI, y compris OnlineMeetingExternalLink, et le bouton Rejoindre s’affiche dans le rappel.</span><span class="sxs-lookup"><span data-stu-id="f3271-188">When TNEFEnabled is set to true Exchange 2013 does not strip MAPI properties including OnlineMeetingExternalLink and the Join button will be shown on the reminder.</span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="f3271-189">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f3271-189">See Also</span></span>


[<span data-ttu-id="f3271-190">Planification de la fédération SIP, XMPP et de la messagerie instantanée publique dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f3271-190">Planning for SIP, XMPP federation, and public instant messaging in Lync Server 2013</span></span>](lync-server-2013-planning-for-sip-xmpp-federation-and-public-instant-messaging.md)  
[<span data-ttu-id="f3271-191">Gestion de la fédération et de l’accès externe à Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f3271-191">Managing federation and external access to Lync Server 2013</span></span>](lync-server-2013-managing-federation-and-external-access-to-lync-server-2013.md)  
  

<span data-ttu-id="f3271-192"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f3271-192"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

