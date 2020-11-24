---
title: 'Lync Server 2013 : Configuration de la fédération Lync'
description: 'Lync Server 2013 : configuration de la Fédération Lync.'
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
# <a name="setting-up-lync-federation-in-lync-server-2013"></a><span data-ttu-id="21ce2-103">Configuration de la fédération Lync dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="21ce2-103">Setting up Lync federation in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="21ce2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="21ce2-104">

<span> </span></span></span>

<span data-ttu-id="21ce2-105">_**Dernière modification de la rubrique :** 2014-03-27_</span><span class="sxs-lookup"><span data-stu-id="21ce2-105">_**Topic Last Modified:** 2014-03-27_</span></span>

<span data-ttu-id="21ce2-106">Si vous avez déjà déployé votre serveur ou serveur Edge, l’ajout de fonctionnalités de scénarios fédérés est une avancée directe.</span><span class="sxs-lookup"><span data-stu-id="21ce2-106">If you have already deployed you Edge server or servers, adding the federated scenarios features is straight forward.</span></span> <span data-ttu-id="21ce2-107">Si vous n’avez pas configuré Edge Servers, vous devez commencer par cela.</span><span class="sxs-lookup"><span data-stu-id="21ce2-107">If you have not set up Edge Servers, you must do that first.</span></span> <span data-ttu-id="21ce2-108">Pour plus d’informations, reportez-vous à la section [planification de l’accès des utilisateurs externes dans Lync server 2013](lync-server-2013-planning-for-external-user-access.md) dans la documentation de planification et [au déploiement de l’accès des utilisateurs externes dans Lync Server 2013](lync-server-2013-deploying-external-user-access.md) dans la documentation de déploiement.</span><span class="sxs-lookup"><span data-stu-id="21ce2-108">For details, see: [Planning for external user access in Lync Server 2013](lync-server-2013-planning-for-external-user-access.md) in the Planning documentation and [Deploying external user access in Lync Server 2013](lync-server-2013-deploying-external-user-access.md) in the Deployment documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="21ce2-109">Si vous envisagez de configurer n’importe quelle combinaison de la Fédération XMPP, de la Fédération Lync ou de la connectivité de messagerie instantanée publique, vous pouvez les déployer en même temps.</span><span class="sxs-lookup"><span data-stu-id="21ce2-109">If you intend to setup any combination of XMPP federation, Lync Federation, or public instant messaging connectivity, you can deploy them concurrently or one at a time.</span></span> <span data-ttu-id="21ce2-110">Si vous configurez les options à l’aide du générateur de topologie et de Lync Server Management Shell, puis exécutez l’Assistant Déploiement sur le serveur Edge après avoir configuré les options pour un, deux ou trois types de Fédération, vous pouvez réduire le nombre d’étapes requises.</span><span class="sxs-lookup"><span data-stu-id="21ce2-110">If you configure the options through the Topology Builder and the Lync Server Management shell, then run the Deployment Wizard at the Edge server after configuring the options for one, two or all three federation types, you can reduce the number of steps required.</span></span>



</div>

<div>

## <a name="setting-up-lync-federation-in-topology-builder-and-the-deployment-wizard"></a><span data-ttu-id="21ce2-111">Configuration de la Fédération Lync dans le générateur de topologie et de l’Assistant Déploiement</span><span class="sxs-lookup"><span data-stu-id="21ce2-111">Setting Up Lync Federation in Topology Builder and the Deployment Wizard</span></span>

1.  <span data-ttu-id="21ce2-112">Sur un serveur frontal, ouvrez le générateur de topologie.</span><span class="sxs-lookup"><span data-stu-id="21ce2-112">On a Front End server, open Topology Builder.</span></span> <span data-ttu-id="21ce2-113">Développez pools de bords, puis cliquez avec le bouton droit sur votre serveur Edge ou sur le pool de serveurs Edge.</span><span class="sxs-lookup"><span data-stu-id="21ce2-113">Expand Edge pools, then right click your Edge server or Edge server pool.</span></span> <span data-ttu-id="21ce2-114">Sélectionnez modifier les propriétés.</span><span class="sxs-lookup"><span data-stu-id="21ce2-114">Select Edit properties.</span></span>

2.  <span data-ttu-id="21ce2-115">Dans modifier les propriétés sous général, sélectionnez Activer la Fédération pour ce pool Edge (port 5061).</span><span class="sxs-lookup"><span data-stu-id="21ce2-115">In Edit Properties under General, select Enable federation for this Edge pool (Port 5061).</span></span> <span data-ttu-id="21ce2-116">Cliquez sur OK.</span><span class="sxs-lookup"><span data-stu-id="21ce2-116">Click OK.</span></span>

3.  <span data-ttu-id="21ce2-117">Cliquez sur action, sélectionnez topologie, puis publier.</span><span class="sxs-lookup"><span data-stu-id="21ce2-117">Click Action, select Topology, select Publish.</span></span> <span data-ttu-id="21ce2-118">Lorsque le système vous le demande, cliquez sur suivant.</span><span class="sxs-lookup"><span data-stu-id="21ce2-118">When prompted on Publish the topology, click Next.</span></span> <span data-ttu-id="21ce2-119">Lorsque la publication est terminée, cliquez sur Terminer.</span><span class="sxs-lookup"><span data-stu-id="21ce2-119">When the Publish is finished, click Finish.</span></span>

4.  <span data-ttu-id="21ce2-120">Sur le serveur Edge, ouvrez l’Assistant Déploiement de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="21ce2-120">On the Edge server, open the Lync Server Deployment wizard.</span></span> <span data-ttu-id="21ce2-121">Cliquez sur installer ou mettre à jour le système serveur Lync, puis cliquez sur Configurer ou supprimer les composants Lync Server.</span><span class="sxs-lookup"><span data-stu-id="21ce2-121">Click Install or Update Lync Server System, then click Setup or Remove Lync Server Components.</span></span> <span data-ttu-id="21ce2-122">Cliquez de nouveau sur Exécuter.</span><span class="sxs-lookup"><span data-stu-id="21ce2-122">Click Run Again.</span></span>

5.  <span data-ttu-id="21ce2-123">Dans configurer les composants serveur Lync, cliquez sur suivant.</span><span class="sxs-lookup"><span data-stu-id="21ce2-123">At Setup Lync Server components, click Next.</span></span> <span data-ttu-id="21ce2-124">L’écran de synthèse indique les actions à mesure qu’elles sont exécutées.</span><span class="sxs-lookup"><span data-stu-id="21ce2-124">The summary screen will show actions as they are executed.</span></span> <span data-ttu-id="21ce2-125">Lorsque le déploiement est effectué, cliquez sur Afficher le journal pour afficher les fichiers journaux disponibles.</span><span class="sxs-lookup"><span data-stu-id="21ce2-125">Once the deployment is done, click View Log to view available log files.</span></span> <span data-ttu-id="21ce2-126">Cliquez sur Terminer pour terminer le déploiement.</span><span class="sxs-lookup"><span data-stu-id="21ce2-126">Click Finish to complete the deployment.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="21ce2-127">Vous pouvez sélectionner cette option, mais un seul pool de périphériques ou serveur de périphérie de votre organisation peut être publié en externe pour la Fédération.</span><span class="sxs-lookup"><span data-stu-id="21ce2-127">You can select this option, but only one Edge pool or Edge Server in your organization can be published externally for federation.</span></span> <span data-ttu-id="21ce2-128">Tout accès par des utilisateurs fédérés, y compris des utilisateurs de la messagerie instantanée publique, passe par le même pool de périphérie ou serveur à périphérie unique.</span><span class="sxs-lookup"><span data-stu-id="21ce2-128">All access by federated users, including public instant messaging (IM) users, go through the same Edge pool or single Edge Server.</span></span> <span data-ttu-id="21ce2-129">Par exemple, si votre déploiement inclut un pool de périphérie ou un serveur de périphérie unique déployé à New York et un serveur sur lequel il est déployé à Londres et que vous activez la prise en charge de la Fédération sur le pool de périphériques de Nouvelle-York ou un serveur Edge</span><span class="sxs-lookup"><span data-stu-id="21ce2-129">For example, if your deployment includes an Edge pool or single Edge Server deployed in New York and one deployed in London and you enable federation support on the New York Edge pool or single Edge Server, signal traffic for federated users will go through the New York Edge pool or single Edge Server.</span></span> <span data-ttu-id="21ce2-130">Cela s’applique également aux communications avec les utilisateurs de Londres, même si un utilisateur interne de Londres qui appelle un utilisateur fédéré de Londres utilise le pool de serveurs ou le serveur Edge de Londres pour le trafic A/V.</span><span class="sxs-lookup"><span data-stu-id="21ce2-130">This is true even for communications with London users, although a London internal user calling a London federated user uses the London pool or Edge Server for A/V traffic.</span></span>

    
    </div>

</div>

<div>

## <a name="configuring-federation-with-partners"></a><span data-ttu-id="21ce2-131">Configuration de la Fédération avec des partenaires</span><span class="sxs-lookup"><span data-stu-id="21ce2-131">Configuring Federation with Partners</span></span>

1.  <span data-ttu-id="21ce2-132">Pour configurer une Fédération réussie avec un autre Microsoft Lync Server 2013, Lync Server 2010, Office Communications Server 2007 R2 ou Office Communicator 2007, sélectionnez le type de Fédération dans le tableau ci-dessous, puis définissez les enregistrements DNS SRV, l’hôte DNS (A ou AAAA pour IPv6) et configurez les stratégies applicables au type de Fédération :</span><span class="sxs-lookup"><span data-stu-id="21ce2-132">To setup a successful federation with another Microsoft Lync Server 2013, Lync Server 2010, Office Communications Server 2007 R2, or Office Communicator 2007, select the type of federation from the following table and define DNS SRV records, DNS host (A or AAAA for IPv6) and configure policies applicable to the type of federation:</span></span>
    
    
    <table>
    <colgroup>
    <col style="width: 25%" />
    <col style="width: 25%" />
    <col style="width: 25%" />
    <col style="width: 25%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="21ce2-133">Type de Fédération</span><span class="sxs-lookup"><span data-stu-id="21ce2-133">Federation type</span></span></th>
    <th><span data-ttu-id="21ce2-134">Enregistrements DNS</span><span class="sxs-lookup"><span data-stu-id="21ce2-134">DNS Records</span></span></th>
    <th><span data-ttu-id="21ce2-135">Définition de la stratégie</span><span class="sxs-lookup"><span data-stu-id="21ce2-135">Policy Definition</span></span></th>
    <th><span data-ttu-id="21ce2-136">Remarques</span><span class="sxs-lookup"><span data-stu-id="21ce2-136">Notes</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="21ce2-137">Domaine partenaire détecté</span><span class="sxs-lookup"><span data-stu-id="21ce2-137">Discovered Partner Domain</span></span></p></td>
    <td><p><span data-ttu-id="21ce2-138">Configurer l’enregistrement SRV du format _sipfederationtls. _ TCP. nom de domaine externe &gt; où la valeur de port pour l’enregistrement SRV est TCP 5061 et l' <strong>hôte proposant ce service</strong> est défini en tant que SIP.</span><span class="sxs-lookup"><span data-stu-id="21ce2-138">Configure SRV record of the format _sipfederationtls._tcp.&lt;external domain name&gt;Where the port value for the SRV record is TCP 5061 and the <strong>Host offering this service</strong> is defined as sip.</span></span> <span data-ttu-id="21ce2-139">&lt;nom de domaine externe &gt; : nom de domaine complet (FQDN) du service Edge d’accès.</span><span class="sxs-lookup"><span data-stu-id="21ce2-139">&lt;external domain name&gt; – the FQDN of your Access Edge service.</span></span> <span data-ttu-id="21ce2-140">Pour plus d’informations sur la création de l’enregistrement SRV <a href="lync-server-2013-configure-dns-for-edge-support.md">, voir Configurer la prise en charge de DNS pour Edge dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="21ce2-140">See <a href="lync-server-2013-configure-dns-for-edge-support.md">Configure DNS for edge support in Lync Server 2013</a> for details on creating the SRV record</span></span></p></td>
    <td><ul>
    <li><p><span data-ttu-id="21ce2-141"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Activation ou désactivation de la fédération et de la connectivité PIC dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="21ce2-141"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Enable or disable federation and public IM connectivity in Lync Server 2013</a></span></span></p></li>
    <li><p><span data-ttu-id="21ce2-142"><a href="lync-server-2013-enable-or-disable-discovery-of-federation-partners.md">Activation ou désactivation de la découverte de partenaires de fédération dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="21ce2-142"><a href="lync-server-2013-enable-or-disable-discovery-of-federation-partners.md">Enable or disable discovery of federation partners in Lync Server 2013</a></span></span></p></li>
    </ul></td>
    <td><p><span data-ttu-id="21ce2-143">Versions précédentes auxquelles il est fait référence à ce type de Fédération en tant qu’ouverture de la <strong>Fédération avancée</strong>.</span><span class="sxs-lookup"><span data-stu-id="21ce2-143">Previous versions referred to this type of federation as <strong>Open Enhanced Federation</strong>.</span></span> <span data-ttu-id="21ce2-144">La création de l’enregistrement SRV est requise pour ce type de Fédération et permet à d’autres partenaires de détecter votre Fédération.</span><span class="sxs-lookup"><span data-stu-id="21ce2-144">The creation of the SRV record is required for this type of federation and is to allow other partners to discover your federation.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="21ce2-145">Domaine partenaire autorisé</span><span class="sxs-lookup"><span data-stu-id="21ce2-145">Allowed Partner Domain</span></span></p></td>
    <td><p><span data-ttu-id="21ce2-146">Configurer l’enregistrement SRV du format _sipfederationtls. _ TCP. nom de domaine externe &gt; où la valeur de port pour l’enregistrement SRV est TCP 5061 et l' <strong>hôte proposant ce service</strong> est défini en tant que SIP.</span><span class="sxs-lookup"><span data-stu-id="21ce2-146">Configure SRV record of the format _sipfederationtls._tcp.&lt;external domain name&gt;Where the port value for the SRV record is TCP 5061 and the <strong>Host offering this service</strong> is defined as sip.</span></span> <span data-ttu-id="21ce2-147">&lt;nom de domaine externe &gt; : nom de domaine complet (FQDN) du service Edge d’accès.</span><span class="sxs-lookup"><span data-stu-id="21ce2-147">&lt;external domain name&gt; – the FQDN of your Access Edge service.</span></span> <span data-ttu-id="21ce2-148">Pour plus d’informations sur la création de l’enregistrement SRV <a href="lync-server-2013-configure-dns-for-edge-support.md">, voir Configurer la prise en charge de DNS pour Edge dans Lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="21ce2-148">See <a href="lync-server-2013-configure-dns-for-edge-support.md">Configure DNS for edge support in Lync Server 2013</a> for details on creating the SRV record</span></span></p></td>
    <td><ul>
    <li><p><span data-ttu-id="21ce2-149"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Activation ou désactivation de la fédération et de la connectivité PIC dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="21ce2-149"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Enable or disable federation and public IM connectivity in Lync Server 2013</a></span></span></p></li>
    </ul></td>
    <td><p><span data-ttu-id="21ce2-150">Versions précédentes auxquelles il est fait référence à ce type de Fédération comme <strong>Fédération améliorée</strong>.</span><span class="sxs-lookup"><span data-stu-id="21ce2-150">Previous versions referred to this type of federation as <strong>Enhanced Federation</strong>.</span></span> <span data-ttu-id="21ce2-151">La création de l’enregistrement SRV peut être facultative pour ce type de Fédération et permettre à d’autres partenaires de détecter votre Fédération.</span><span class="sxs-lookup"><span data-stu-id="21ce2-151">The creation of the SRV record is optional for this type of federation and is to allow other partners to discover your federation.</span></span> <span data-ttu-id="21ce2-152">Bien entendu, il s’agit d’une <strong>fédération étendue ouverte</strong>ou d’un <strong>domaine partenaire découvert</strong> .</span><span class="sxs-lookup"><span data-stu-id="21ce2-152">Of course, this is then an <strong>Open Enhanced Federation</strong>, or <strong>Discovered Partner Domain</strong></span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="21ce2-153">Serveur partenaire autorisé</span><span class="sxs-lookup"><span data-stu-id="21ce2-153">Allowed Partner Server</span></span></p></td>
    <td><p><span data-ttu-id="21ce2-154">Configurer le nom de domaine SIP et le FQDN du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="21ce2-154">Configure the SIP domain name and the partner Edge Server FQDN as a federation partner in Policies</span></span></p></td>
    <td><ul>
    <li><p><span data-ttu-id="21ce2-155"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Activation ou désactivation de la fédération et de la connectivité PIC dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="21ce2-155"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Enable or disable federation and public IM connectivity in Lync Server 2013</a></span></span></p></li>
    <li><p><span data-ttu-id="21ce2-156"><a href="lync-server-2013-configure-support-for-allowed-external-domains.md">Configuration de la prise en charge des domaines externes autorisés dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="21ce2-156"><a href="lync-server-2013-configure-support-for-allowed-external-domains.md">Configure support for allowed external domains in Lync Server 2013</a></span></span></p></li>
    <li><p><span data-ttu-id="21ce2-157"><a href="lync-server-2013-configure-support-for-blocked-external-domains.md">Configuration de la prise en charge pour les domaines externes bloqués dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="21ce2-157"><a href="lync-server-2013-configure-support-for-blocked-external-domains.md">Configure support for blocked external domains in Lync Server 2013</a></span></span></p></li>
    </ul></td>
    <td><p><span data-ttu-id="21ce2-158">Ce type de Fédération est la définition d’une relation un-à-un qui ne permet pas la découverte d’autres partenaires de la Fédération.</span><span class="sxs-lookup"><span data-stu-id="21ce2-158">This federation type is the definition of a one to one relationship and does not allow for discovery of other federation partners.</span></span> <span data-ttu-id="21ce2-159">Chaque partenaire de Fédération est configuré explicitement.</span><span class="sxs-lookup"><span data-stu-id="21ce2-159">Each federation partner is configured explicitly.</span></span> <span data-ttu-id="21ce2-160">Dans les versions précédentes, il s’agit de la <strong>Fédération directe</strong></span><span class="sxs-lookup"><span data-stu-id="21ce2-160">In previous versions, this was known as <strong>Direct Federation</strong></span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="21ce2-161">Fournisseur d’hébergement et fournisseur de messagerie instantanée publique</span><span class="sxs-lookup"><span data-stu-id="21ce2-161">Hosting Provider and Public IM Provider</span></span></p></td>
    <td><p><span data-ttu-id="21ce2-162">Aucune configuration DNS spécifique n’est définie pour ce type de Fédération</span><span class="sxs-lookup"><span data-stu-id="21ce2-162">No specific DNS requirements are defined for this type of federation</span></span></p></td>
    <td><ul>
    <li><p><span data-ttu-id="21ce2-163"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Activation ou désactivation de la fédération et de la connectivité PIC dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="21ce2-163"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Enable or disable federation and public IM connectivity in Lync Server 2013</a></span></span></p></li>
    <li><p><span data-ttu-id="21ce2-164"><a href="lync-server-2013-create-or-edit-public-sip-federated-providers.md">Création ou modification des fournisseurs fédérés SIP publics dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="21ce2-164"><a href="lync-server-2013-create-or-edit-public-sip-federated-providers.md">Create or edit public SIP federated providers in Lync Server 2013</a></span></span></p></li>
    <li><p><span data-ttu-id="21ce2-165"><a href="lync-server-2013-create-or-edit-hosted-sip-federated-providers.md">Création ou modification des fournisseurs fédérés SIP hébergés dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="21ce2-165"><a href="lync-server-2013-create-or-edit-hosted-sip-federated-providers.md">Create or edit hosted SIP federated providers Lync Server 2013</a></span></span></p></li>
    </ul></td>
    <td><p><span data-ttu-id="21ce2-166">Ce type de Fédération définit les services et fournisseurs d’hébergement que vous voulez configurer pour vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="21ce2-166">This federation type defines services and hosting providers that you want to configure for your users.</span></span> <span data-ttu-id="21ce2-167">Les utilisations typiques incluent la configuration pour les fournisseurs de messagerie instantanée publique tels que Windows Live Messenger, Yahoo !</span><span class="sxs-lookup"><span data-stu-id="21ce2-167">Typical uses include configuration for public IM providers like Windows Live Messenger, Yahoo!</span></span> <span data-ttu-id="21ce2-168">et AOL, ainsi que des fournisseurs d’hébergement tels que Lync Online et Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="21ce2-168">and AOL, as well as hosting providers such as Lync Online and Microsoft 365</span></span></p>
    <div>

    > [!IMPORTANT]  
    > <UL>
    > <LI>
    > <P><span data-ttu-id="21ce2-169">À compter du 1er septembre, 2012, le contrat de licence de l’utilisateur Microsoft Lync Public IM Connectivity (« PIC USL ») ne sera plus disponible à l’achat pour les contrats de nouveau ou de renouvellement.</span><span class="sxs-lookup"><span data-stu-id="21ce2-169">As of September 1st, 2012, the Microsoft Lync Public IM Connectivity User Subscription License (“PIC USL”) is no longer available for purchase for new or renewing agreements.</span></span> <span data-ttu-id="21ce2-170">Les clients disposant de licences actives seront en mesure de continuer à fédérer avec Yahoo !</span><span class="sxs-lookup"><span data-stu-id="21ce2-170">Customers with active licenses will be able to continue to federate with Yahoo!</span></span> <span data-ttu-id="21ce2-171">Messenger jusqu’à la date d’arrêt du service.</span><span class="sxs-lookup"><span data-stu-id="21ce2-171">Messenger until the service shut down date.</span></span> <span data-ttu-id="21ce2-172">Date de fin de vie du 2014 juin pour AOL et Yahoo !</span><span class="sxs-lookup"><span data-stu-id="21ce2-172">An end of life date of June 2014 for AOL and Yahoo!</span></span> <span data-ttu-id="21ce2-173">a été annoncé.</span><span class="sxs-lookup"><span data-stu-id="21ce2-173">has been announced.</span></span> <span data-ttu-id="21ce2-174">Pour plus d’informations, voir <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">prise en charge de la connectivité de messagerie instantanée publique dans Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="21ce2-174">For details, see <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Support for public instant messenger connectivity in Lync Server 2013</A>.</span></span></P>
    > <LI>
    > <P><span data-ttu-id="21ce2-175">La fonction USL (PIC) est une licence d’abonnement par mois qui est requise pour que Lync Server ou Office Communications Server se fédérer avec Yahoo !</span><span class="sxs-lookup"><span data-stu-id="21ce2-175">The PIC USL is a per-user per-month subscription license that is required for Lync Server or Office Communications Server to federate with Yahoo!</span></span> <span data-ttu-id="21ce2-176">Messenger.</span><span class="sxs-lookup"><span data-stu-id="21ce2-176">Messenger.</span></span> <span data-ttu-id="21ce2-177">La capacité de Microsoft à fournir ce service est subordonné à la prise en charge de Yahoo !, le contrat sous-jacent pour lequel le son est arrêté.</span><span class="sxs-lookup"><span data-stu-id="21ce2-177">Microsoft’s ability to provide this service has been contingent upon support from Yahoo!, the underlying agreement for which is winding down.</span></span></P>
    > <LI>
    > <P><span data-ttu-id="21ce2-178">Plus que jamais, Lync est un outil puissant de connexion entre organisations et de personnes dans le monde entier.</span><span class="sxs-lookup"><span data-stu-id="21ce2-178">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="21ce2-179">La Fédération avec Windows Live Messenger ne nécessite aucune licence d’utilisateur/appareil supplémentaire au-delà de la CAL standard Lync.</span><span class="sxs-lookup"><span data-stu-id="21ce2-179">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard CAL.</span></span> <span data-ttu-id="21ce2-180">Skype Federation sera ajouté à cette liste et permettra aux utilisateurs de Lync de joindre des centaines de millions de personnes à la messagerie instantanée et à la voix.</span><span class="sxs-lookup"><span data-stu-id="21ce2-180">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people with IM and voice.</span></span></P></LI></UL>


    </div></td>
    </tr>
    </tbody>
    </table>


2.  <span data-ttu-id="21ce2-181">Définissez et configurez tout hôte DNS requis (A ou AAAA pour IPv6) et enregistrements SRV DNS.</span><span class="sxs-lookup"><span data-stu-id="21ce2-181">Define and configure any required DNS host (A or AAAA for IPv6) and DNS SRV records</span></span>

3.  <span data-ttu-id="21ce2-182">Définissez et configurez toutes les stratégies à l’aide du panneau de configuration de Lync Server ou en utilisant Lync Server Management Shell et les applets de commande appropriées.</span><span class="sxs-lookup"><span data-stu-id="21ce2-182">Define and configure any policies using the Lync Server Control Panel or by using the Lync Server Management Shell and the appropriate cmdlets.</span></span> <span data-ttu-id="21ce2-183">Pour en savoir plus sur les applets de cmdlet Lync Server Management Shell, voir [Fédération et applets de connexion Access externes dans Lync server 2013](https://docs.microsoft.com/powershell/module/skype/)</span><span class="sxs-lookup"><span data-stu-id="21ce2-183">For details on the Lync Server Management Shell cmdlets, see [Federation and external access cmdlets in Lync Server 2013](https://docs.microsoft.com/powershell/module/skype/)</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="21ce2-184">Le système de salle Lync (LRS) ne montre pas le bouton de participation pour les réunions envoyées par des organisateurs dans les partenaires Lync fédérés.</span><span class="sxs-lookup"><span data-stu-id="21ce2-184">Lync Room System (LRS) does not show join button for meetings sent by organizers in federated Lync partners.</span></span> <span data-ttu-id="21ce2-185">Pour qu’un lien de participation à une réunion apparaisse sur LRS, l’organisation d’expédition doit activer TNEF en utilisant l’applet de commande suivante :</span><span class="sxs-lookup"><span data-stu-id="21ce2-185">For a meeting join link to appear on LRS, the sending organization must enable TNEF by using the following cmdlet:</span></span><BR><BR><CODE>New-RemoteDomain -DomainName Contoso.com -Name Contoso</CODE><BR><CODE>Set-RemoteDomain -Identity Contoso -TNEFEnabled $true</CODE><BR><span data-ttu-id="21ce2-186">Notez que cela n’est pas spécifique à LRS.</span><span class="sxs-lookup"><span data-stu-id="21ce2-186">Note that this is not LRS specific.</span></span> <span data-ttu-id="21ce2-187">Dans le cas contraire, Outlook et Lync n’affichent pas de liens de jointure dans le cas où les propriétés MAPI ne sont pas transportées, mais dans le cas d’Outlook, l’utilisateur peut ouvrir l’invitation à la réunion et cliquer sur l’URL de la réunion.</span><span class="sxs-lookup"><span data-stu-id="21ce2-187">Outlook and Lync would also not show Join links in this case as MAPI properties are not transported, but in the Outlook case, the user can open up the meeting invite and click on the meeting URL.</span></span> <span data-ttu-id="21ce2-188">Lorsque TNEFEnabled est défini sur true Exchange 2013 ne Strip pas les propriétés MAPI, y compris OnlineMeetingExternalLink et le bouton Join s’affichera sur le rappel.</span><span class="sxs-lookup"><span data-stu-id="21ce2-188">When TNEFEnabled is set to true Exchange 2013 does not strip MAPI properties including OnlineMeetingExternalLink and the Join button will be shown on the reminder.</span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="21ce2-189">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="21ce2-189">See Also</span></span>


[<span data-ttu-id="21ce2-190">Planification de la Fédération SIP, de XMPP et de la messagerie instantanée publique dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="21ce2-190">Planning for SIP, XMPP federation, and public instant messaging in Lync Server 2013</span></span>](lync-server-2013-planning-for-sip-xmpp-federation-and-public-instant-messaging.md)  
[<span data-ttu-id="21ce2-191">Gestion de la fédération et de l’accès externe à Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="21ce2-191">Managing federation and external access to Lync Server 2013</span></span>](lync-server-2013-managing-federation-and-external-access-to-lync-server-2013.md)  
  

<span data-ttu-id="21ce2-192"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="21ce2-192"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

