---
title: Configuration des itinéraires de fédération et du trafic multimédia
description: Configurer des itinéraires de Fédération et du trafic multimédia.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Configure federation routes and media traffic
ms:assetid: 8b2f5f81-a955-4ad1-ad74-397322ff9521
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688121(v=OCS.15)
ms:contentKeyID: 49733720
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: de26f472bddc504ff79e427b5243587f27020c3d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394116"
---
# <a name="configure-federation-routes-and-media-traffic"></a><span data-ttu-id="cc8cc-103">Configuration des itinéraires de fédération et du trafic multimédia</span><span class="sxs-lookup"><span data-stu-id="cc8cc-103">Configure federation routes and media traffic</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cc8cc-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cc8cc-104">

<span> </span></span></span>

<span data-ttu-id="cc8cc-105">_**Dernière modification de la rubrique :** 2012-10-15_</span><span class="sxs-lookup"><span data-stu-id="cc8cc-105">_**Topic Last Modified:** 2012-10-15_</span></span>

<span data-ttu-id="cc8cc-106">La Fédération est une relation d’approbation entre au moins deux domaines SIP, qui permet aux utilisateurs d’organisations distinctes de communiquer au sein des frontières du réseau.</span><span class="sxs-lookup"><span data-stu-id="cc8cc-106">Federation is a trust relationship between two or more SIP domains that permits users in separate organizations to communicate across network boundaries.</span></span> <span data-ttu-id="cc8cc-107">Après avoir effectué une migration vers votre pool de pilotes de Lync Server 2013, vous devez effectuer une transition de l’itinéraire de Fédération de vos serveurs Edge Lync Server 2010 vers l’itinéraire de Fédération de votre serveur Edge Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="cc8cc-107">After you migrate to your Lync Server 2013 pilot pool, you need to transition from the federation route of your Lync Server 2010 Edge Servers to the federation route of your Lync Server 2013 Edge Servers.</span></span>

<span data-ttu-id="cc8cc-108">Pour effectuer un déploiement sur un site, procédez comme suit pour migrer l’itinéraire de la Fédération et l’itinéraire de trafic multimédia de votre serveur Edge et de votre directeur 2010 Lync Server 2013 vers votre serveur Edge Lync Server.</span><span class="sxs-lookup"><span data-stu-id="cc8cc-108">Use the following procedures to transition the federation route and the media traffic route from your Lync Server 2010 Edge Server and Director to your Lync Server 2013 Edge Server, for a single-site deployment.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="cc8cc-109">La modification de l’itinéraire et de l’itinéraire de trafic multimédia requis pour la planification de la maintenance pour les serveurs Edge Lync Server 2013 et Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="cc8cc-109">Changing the federation route and media traffic route requires that you schedule maintenance downtime for the Lync Server 2013 and Lync Server 2010 Edge Servers.</span></span> <span data-ttu-id="cc8cc-110">Ce processus de transition complet signifie également que l’accès fédéré ne sera pas disponible pendant la durée de la période d’interruption.</span><span class="sxs-lookup"><span data-stu-id="cc8cc-110">This entire transition process also means that federated access will be unavailable for the duration of the outage.</span></span> <span data-ttu-id="cc8cc-111">Nous vous conseillons de planifier le temps d’arrêt à un moment où vous vous attendez à un minimum d’activités utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cc8cc-111">You should schedule the downtime for a time when you expect minimal user activity.</span></span> <span data-ttu-id="cc8cc-112">Vous devez également fournir une notification suffisante à vos utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="cc8cc-112">You should also provide sufficient notification to your end users.</span></span> <span data-ttu-id="cc8cc-113">Planifiez en conséquence pour cette interruption et définissez les attentes appropriées au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="cc8cc-113">Plan accordingly for this outage and set appropriate expectations within your organization.</span></span>



</div>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="cc8cc-114">Si votre serveur Edge Lync Server 2010 hérité est configuré de manière à utiliser le même nom de domaine complet pour le service Edge d’accès, le service Edge de conférence Web et le service Edge A/V, les procédures de cette section ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="cc8cc-114">If your legacy Lync Server 2010 Edge Server is configured to use the same FQDN for the Access Edge service, Web Conferencing Edge service, and the A/V Edge service, the procedures in this section are not supported.</span></span> <span data-ttu-id="cc8cc-115">Si les services Edge hérités sont configurés pour utiliser le même nom de domaine complet, vous devez tout d’abord migrer tous vos utilisateurs de Lync Server 2010 vers Lync Server 2013, puis désactivez le serveur Edge Lync Server 2010 avant d’activer la Fédération sur le serveur Edge Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="cc8cc-115">If the legacy Edge services are configured to use the same FQDN, you must first migrate all your users from Lync Server 2010 to Lync Server 2013, then decommission the Lync Server 2010 Edge Server before enabling federation on the Lync Server 2013 Edge Server.</span></span>



</div>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="cc8cc-116">Si votre Fédération XMPP est routée par le biais d’un serveur Edge Lync Server 2013, les utilisateurs hérités de Lync Server 2010 ne seront pas en mesure de communiquer avec le partenaire fédéré de XMPP tant que tous les utilisateurs n’ont pas été déplacés vers Lync Server 2013, que les stratégies et les certificats de l’application de ce service ont été 2013 configurés.</span><span class="sxs-lookup"><span data-stu-id="cc8cc-116">If your XMPP federation is routed through a Lync Server 2013 Edge Server, legacy Lync Server 2010 users will not be able to communicate with the XMPP federated partner until all users have been moved to Lync Server 2013, XMPP policies and certificates have been configured, the XMPP federated partner has been configured on Lync Server 2013, and lastly the DNS entries have been updated.</span></span>



</div>

<div>

## <a name="to-remove-the-legacy-federation-association-from-lync-server-2013-sites"></a><span data-ttu-id="cc8cc-117">Pour supprimer l’Association de Fédération héritée des sites Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cc8cc-117">To remove the legacy federation association from Lync Server 2013 sites</span></span>

1.  <span data-ttu-id="cc8cc-118">Sur le serveur frontal Lync Server 2013, ouvrez la topologie existante dans le générateur de topologie.</span><span class="sxs-lookup"><span data-stu-id="cc8cc-118">On the Lync Server 2013 Front End server, open the existing topology in Topology Builder.</span></span>

2.  <span data-ttu-id="cc8cc-119">Dans le volet gauche, accédez au nœud de site qui se trouve juste en dessous de **Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="cc8cc-119">In the left pane, navigate to the site node, which is located directly below **Lync Server**.</span></span>

3.  <span data-ttu-id="cc8cc-120">Cliquez avec le bouton droit sur le site, puis cliquez sur **modifier les propriétés**.</span><span class="sxs-lookup"><span data-stu-id="cc8cc-120">Right-click the site and then click **Edit Properties**.</span></span>

4.  <span data-ttu-id="cc8cc-121">Dans le volet gauche, sélectionnez **gamme de Fédération**.</span><span class="sxs-lookup"><span data-stu-id="cc8cc-121">In the left pane, select **Federation route**.</span></span>

5.  <span data-ttu-id="cc8cc-122">Sous **affectation** de l’itinéraire de Fédération de site, décochez la case **activer la Fédération SIP** pour désactiver le routage de Fédération par le biais de l’environnement 2010 hérité de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="cc8cc-122">Under **Site federation route assignment**, clear the **Enable SIP federation** check box to disable the federation route through the legacy Lync Server 2010 environment.</span></span>
    
    <span data-ttu-id="cc8cc-123">![Boîte de dialogue Modifier les propriétés, page itinéraire de Fédération](images/JJ688121.8d755ae0-fc7d-4253-b0db-0cf31b863c55(OCS.15).jpg "Boîte de dialogue Modifier les propriétés, page itinéraire de Fédération")</span><span class="sxs-lookup"><span data-stu-id="cc8cc-123">![Edit Properties dialog, Federation route page](images/JJ688121.8d755ae0-fc7d-4253-b0db-0cf31b863c55(OCS.15).jpg "Edit Properties dialog, Federation route page")</span></span>

6.  <span data-ttu-id="cc8cc-124">Cliquez sur **OK** pour fermer la page modifier les propriétés.</span><span class="sxs-lookup"><span data-stu-id="cc8cc-124">Click **OK** to close the Edit Properties page.</span></span>

7.  <span data-ttu-id="cc8cc-125">Dans le **Générateur de topologie**, sélectionnez le nœud supérieur **serveur Lync**.</span><span class="sxs-lookup"><span data-stu-id="cc8cc-125">From **Topology Builder**, select the top node **Lync Server**.</span></span>

8.  <span data-ttu-id="cc8cc-126">Dans le menu **action** , cliquez sur **publier la topologie**.</span><span class="sxs-lookup"><span data-stu-id="cc8cc-126">From the **Action** menu, click **Publish Topology**.</span></span>

9.  <span data-ttu-id="cc8cc-127">Cliquez sur **suivant** pour finaliser le processus de publication, puis cliquez sur **Terminer** lorsque le processus de publication est terminé.</span><span class="sxs-lookup"><span data-stu-id="cc8cc-127">Click **Next** to complete the publishing process and then click **Finish** when the publishing process has completed.</span></span>

</div>

<div>

## <a name="to-configure-the-legacy-edge-server-as-a-non-federating-edge-server"></a><span data-ttu-id="cc8cc-128">Pour configurer le serveur de périphérie traditionnel en tant que serveur Edge non fédéré</span><span class="sxs-lookup"><span data-stu-id="cc8cc-128">To configure the legacy Edge Server as a non-federating Edge Server</span></span>

1.  <span data-ttu-id="cc8cc-129">Dans le volet gauche, accédez au nœud **Lync Server 2010** , puis au nœud **pools de bords** .</span><span class="sxs-lookup"><span data-stu-id="cc8cc-129">In the left pane, navigate to the **Lync Server 2010** node and then to the **Edge pools** node.</span></span>

2.  <span data-ttu-id="cc8cc-130">Cliquez avec le bouton droit sur le serveur Edge, puis cliquez sur **modifier les propriétés**.</span><span class="sxs-lookup"><span data-stu-id="cc8cc-130">Right-click the Edge server, and then click **Edit Properties**.</span></span>

3.  <span data-ttu-id="cc8cc-131">Dans le volet gauche, sélectionnez **général** .</span><span class="sxs-lookup"><span data-stu-id="cc8cc-131">Select **General** in the left pane.</span></span>

4.  <span data-ttu-id="cc8cc-132">Décochez la case **activer la Fédération pour ce pool Edge (port 5061)** , puis sélectionnez **OK** pour fermer la page.</span><span class="sxs-lookup"><span data-stu-id="cc8cc-132">Clear the **Enable federation for this Edge pool (port 5061)** check box entry and select **OK** to close the page.</span></span>
    
    <span data-ttu-id="cc8cc-133">![Modifier les propriétés, général, effacer la Fédération d’activation](images/JJ688121.3be2c8c0-9ed9-4544-bafd-b7694271fafc(OCS.15).jpg "Modifier les propriétés, général, effacer la Fédération d’activation")</span><span class="sxs-lookup"><span data-stu-id="cc8cc-133">![Edit Properties, General, clear Enable federation](images/JJ688121.3be2c8c0-9ed9-4544-bafd-b7694271fafc(OCS.15).jpg "Edit Properties, General, clear Enable federation")</span></span>

5.  <span data-ttu-id="cc8cc-134">Dans le menu **action** , cliquez sur **publier la topologie**, puis sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="cc8cc-134">From the **Action** menu, select **Publish Topology**, and then click **Next**.</span></span>

6.  <span data-ttu-id="cc8cc-135">Lorsque l' **Assistant Publication** est terminé, cliquez sur **Terminer** pour fermer l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="cc8cc-135">When the **Publishing wizard** completes, click **Finish** to close the wizard.</span></span>

7.  <span data-ttu-id="cc8cc-136">Vérifiez que la Fédération pour le serveur de périphérie antérieur est désactivée.</span><span class="sxs-lookup"><span data-stu-id="cc8cc-136">Verify federation for the legacy Edge server is disabled.</span></span>
    
    <span data-ttu-id="cc8cc-137">![Générateur de topologie, pool de périphériques, Fédération désactivé](images/JJ688121.a2948438-d51a-4aeb-9eaa-d899ca950758(OCS.15).jpg "Générateur de topologie, pool de périphériques, Fédération désactivé")</span><span class="sxs-lookup"><span data-stu-id="cc8cc-137">![Topology Builder, Edge pool, federation disabled](images/JJ688121.a2948438-d51a-4aeb-9eaa-d899ca950758(OCS.15).jpg "Topology Builder, Edge pool, federation disabled")</span></span>

</div>

<div>

## <a name="to-configure-certificates-on-the-lync-server-2010-edge-server"></a><span data-ttu-id="cc8cc-138">Pour configurer des certificats sur le serveur Edge Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="cc8cc-138">To configure certificates on the Lync Server 2010 Edge Server</span></span>

1.  <span data-ttu-id="cc8cc-139">Exportez le certificat de proxy d’accès externe, avec la clé privée, à partir du serveur Edge Lync Server 2010 hérité.</span><span class="sxs-lookup"><span data-stu-id="cc8cc-139">Export the external Access Proxy certificate, with the private key, from the legacy Lync Server 2010 Edge Server.</span></span>

2.  <span data-ttu-id="cc8cc-140">Sur le serveur Edge Lync Server 2013, importez le certificat externe de proxy d’accès à partir de l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="cc8cc-140">On the Lync Server 2013 Edge Server, import the Access Proxy external certificate from the previous step.</span></span>

3.  <span data-ttu-id="cc8cc-141">Attribuez le certificat externe du proxy d’accès à l’interface externe de Lync Server 2013 du serveur Edge.</span><span class="sxs-lookup"><span data-stu-id="cc8cc-141">Assign the Access Proxy external certificate to the Lync Server 2013 external interface of the Edge Server.</span></span>

4.  <span data-ttu-id="cc8cc-142">Le certificat d’interface interne du serveur Edge Lync Server 2013 doit être demandé auprès d’une autorité de certification approuvée et attribué.</span><span class="sxs-lookup"><span data-stu-id="cc8cc-142">The internal interface certificate of the Lync Server 2013 Edge Server should be requested from a trusted CA and assigned.</span></span>

</div>

<div>

## <a name="to-change-lync-server-2010-federation-route-to-use-lync-server-2013-edge-server"></a><span data-ttu-id="cc8cc-143">Pour modifier l’itinéraire de Fédération de Lync Server 2010 de sorte qu’il utilise Lync Server 2013 Edge Server</span><span class="sxs-lookup"><span data-stu-id="cc8cc-143">To change Lync Server 2010 federation route to use Lync Server 2013 Edge Server</span></span>

1.  <span data-ttu-id="cc8cc-144">Dans le générateur de topologie, dans le volet gauche, accédez au nœud **Lync Server 2013** , puis au nœud **pools de périphérie** .</span><span class="sxs-lookup"><span data-stu-id="cc8cc-144">From Topology Builder, in the left pane, navigate to the **Lync Server 2013** node and then to the **Edge pools** node.</span></span>

2.  <span data-ttu-id="cc8cc-145">Cliquez avec le bouton droit sur le serveur Edge, puis cliquez sur **modifier les propriétés**.</span><span class="sxs-lookup"><span data-stu-id="cc8cc-145">Right-click the Edge server, and then click **Edit Properties**.</span></span>

3.  <span data-ttu-id="cc8cc-146">Dans le volet gauche, sélectionnez **général** .</span><span class="sxs-lookup"><span data-stu-id="cc8cc-146">Select **General** in the left pane.</span></span>

4.  <span data-ttu-id="cc8cc-147">Sélectionnez l’entrée de la case à cocher **activer la Fédération pour ce pool Edge (port 5061)** , puis cliquez sur **OK** pour fermer la page.</span><span class="sxs-lookup"><span data-stu-id="cc8cc-147">Select the check box entry for **Enable federation for this Edge pool (port 5061)** and then click **OK** to close the page.</span></span>
    
    <span data-ttu-id="cc8cc-148">![Boîte de dialogue Modifier les propriétés, page général](images/JJ688121.cc79a88c-cce4-4cab-80ad-4f70325dc7c4(OCS.15).jpg "Boîte de dialogue Modifier les propriétés, page général")</span><span class="sxs-lookup"><span data-stu-id="cc8cc-148">![Edit Properties dialog, General page](images/JJ688121.cc79a88c-cce4-4cab-80ad-4f70325dc7c4(OCS.15).jpg "Edit Properties dialog, General page")</span></span>

5.  <span data-ttu-id="cc8cc-149">Dans le menu **action** , cliquez sur **publier la topologie**, puis sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="cc8cc-149">From the **Action** menu, select **Publish Topology**, and then click **Next**.</span></span>

6.  <span data-ttu-id="cc8cc-150">Lorsque l' **Assistant Publication** est terminé, cliquez sur **Terminer** pour fermer l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="cc8cc-150">When the **Publishing wizard** completes, click **Finish** to close the wizard.</span></span>

7.  <span data-ttu-id="cc8cc-151">Vérifier la **Fédération (le port 5061)** est défini sur **activé**.</span><span class="sxs-lookup"><span data-stu-id="cc8cc-151">Verify **Federation (port 5061)** is set to **Enabled**.</span></span>
    
    <span data-ttu-id="cc8cc-152">![Générateur de topologie, pool de périphériques, Fédération activée](images/JJ688121.e8ccdada-23f4-47e5-a99d-5bf795fefc48(OCS.15).jpg "Générateur de topologie, pool de périphériques, Fédération activée")</span><span class="sxs-lookup"><span data-stu-id="cc8cc-152">![Topology Builder, Edge pool, Federation enabled](images/JJ688121.e8ccdada-23f4-47e5-a99d-5bf795fefc48(OCS.15).jpg "Topology Builder, Edge pool, Federation enabled")</span></span>

</div>

<div>

## <a name="to-update-lync-server-2013-edge-server-federation-next-hop"></a><span data-ttu-id="cc8cc-153">Pour mettre à jour Lync Server 2013 Edge Server Federation Next hop</span><span class="sxs-lookup"><span data-stu-id="cc8cc-153">To update Lync Server 2013 Edge Server federation next hop</span></span>

1.  <span data-ttu-id="cc8cc-154">Dans le générateur de topologie, dans le volet gauche, accédez au nœud **Lync Server 2013** , puis au nœud **pools de périphérie** .</span><span class="sxs-lookup"><span data-stu-id="cc8cc-154">From Topology Builder, in the left pane, navigate to the **Lync Server 2013** node and then to the **Edge pools** node.</span></span>

2.  <span data-ttu-id="cc8cc-155">Développez le nœud, cliquez avec le bouton droit sur le serveur Edge indiqué, puis cliquez sur **modifier les propriétés**.</span><span class="sxs-lookup"><span data-stu-id="cc8cc-155">Expand the node, right-click the Edge Server listed, and then click **Edit Properties**.</span></span>

3.  <span data-ttu-id="cc8cc-156">Dans la page **général** , sous **sélection du tronçon suivant**, sélectionnez dans la liste déroulante le pool Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="cc8cc-156">On the **General** page, under **Next hop selection**, select from the drop-down list the Lync Server 2013  pool.</span></span>
    
    <span data-ttu-id="cc8cc-157">![Boîte de dialogue Modifier les propriétés, page saut suivant](images/JJ688121.5741b9a8-e729-4457-9f62-38f08a2c5b02(OCS.15).jpg "Boîte de dialogue Modifier les propriétés, page saut suivant")</span><span class="sxs-lookup"><span data-stu-id="cc8cc-157">![Edit Properties dialog, Next hop page](images/JJ688121.5741b9a8-e729-4457-9f62-38f08a2c5b02(OCS.15).jpg "Edit Properties dialog, Next hop page")</span></span>

4.  <span data-ttu-id="cc8cc-158">Cliquez sur **OK** pour fermer la page modifier les propriétés.</span><span class="sxs-lookup"><span data-stu-id="cc8cc-158">Click **OK** to close the Edit Properties page.</span></span>

5.  <span data-ttu-id="cc8cc-159">Dans le **Générateur de topologie**, sélectionnez le nœud supérieur **serveur Lync** .</span><span class="sxs-lookup"><span data-stu-id="cc8cc-159">From **Topology Builder**, select the top node **Lync Server** .</span></span>

6.  <span data-ttu-id="cc8cc-160">Dans le menu **action** , cliquez sur **publier la topologie** et terminer l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="cc8cc-160">From the **Action** menu, click **Publish Topology** and complete the wizard.</span></span>

</div>

<div>

## <a name="to-configure-lync-server-2013-edge-server-outbound-media-path"></a><span data-ttu-id="cc8cc-161">Pour configurer le chemin multimédia sortant du serveur Lync Server 2013 Edge</span><span class="sxs-lookup"><span data-stu-id="cc8cc-161">To configure Lync Server 2013 Edge Server outbound media path</span></span>

1.  <span data-ttu-id="cc8cc-162">Dans le concepteur de topologies, dans le volet de gauche, accédez au nœud **Lync Server 2013** , puis au pool sous **Standard Edition serveurs front end** ou **Enterprise Edition**.</span><span class="sxs-lookup"><span data-stu-id="cc8cc-162">From Topology Builder, in the left pane, navigate to the **Lync Server 2013** node and then to the pool below **Standard Edition Front End Servers** or **Enterprise Edition Front End pools**.</span></span>

2.  <span data-ttu-id="cc8cc-163">Cliquez avec le bouton droit sur la liste, puis cliquez sur **modifier les propriétés**.</span><span class="sxs-lookup"><span data-stu-id="cc8cc-163">Right-click the pool, and then click **Edit Properties**.</span></span>

3.  <span data-ttu-id="cc8cc-164">Dans la section **associations** , activez la case à cocher **associer le pool Edge (pour les composants multimédias)** .</span><span class="sxs-lookup"><span data-stu-id="cc8cc-164">In the **Associations** section, select the **Associate Edge pool (for media components)** check box.</span></span>
    
    <span data-ttu-id="cc8cc-165">![Modification des propriétés, général et pool de périphérie](images/JJ688121.fd9b18ca-fda2-4764-9bf0-726bf39f6a12(OCS.15).jpg "Modification des propriétés, général et pool de périphérie")</span><span class="sxs-lookup"><span data-stu-id="cc8cc-165">![Edit Properties, General, Associate Edge pool](images/JJ688121.fd9b18ca-fda2-4764-9bf0-726bf39f6a12(OCS.15).jpg "Edit Properties, General, Associate Edge pool")</span></span>

4.  <span data-ttu-id="cc8cc-166">Dans la zone de liste déroulante, sélectionnez le serveur Edge Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="cc8cc-166">From the drop down box, select the Lync Server 2013 Edge Server.</span></span>

5.  <span data-ttu-id="cc8cc-167">Cliquez sur **OK** pour fermer la page **modifier les propriétés** .</span><span class="sxs-lookup"><span data-stu-id="cc8cc-167">Click **OK** to close the **Edit Properties** page.</span></span>

</div>

<div>

## <a name="to-turn-on-lync-server-2013-edge-server-federation"></a><span data-ttu-id="cc8cc-168">Pour activer la Fédération de serveur Edge Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cc8cc-168">To turn on Lync Server 2013 Edge Server federation</span></span>

1.  <span data-ttu-id="cc8cc-169">Dans le générateur de topologie, dans le volet gauche, accédez au nœud **Lync Server 2013** , puis au nœud **pools de périphérie** .</span><span class="sxs-lookup"><span data-stu-id="cc8cc-169">From Topology Builder, in the left pane, navigate to the **Lync Server 2013** node and then to the **Edge pools** node.</span></span>

2.  <span data-ttu-id="cc8cc-170">Développez le nœud, cliquez avec le bouton droit sur le serveur Edge indiqué, puis cliquez sur **modifier les propriétés**.</span><span class="sxs-lookup"><span data-stu-id="cc8cc-170">Expand the node, right-click the Edge Server listed, and then click **Edit Properties**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="cc8cc-171">La Fédération ne peut être activée que pour un seul pool de bords.</span><span class="sxs-lookup"><span data-stu-id="cc8cc-171">Federation can only be enabled for a single Edge pool.</span></span> <span data-ttu-id="cc8cc-172">Si vous avez plusieurs pools de bords, sélectionnez-en un pour les utiliser comme pools de frontière de Fédération.</span><span class="sxs-lookup"><span data-stu-id="cc8cc-172">If you have multiple Edge pools, select one to use as the federating Edge pool.</span></span>

    
    </div>

3.  <span data-ttu-id="cc8cc-173">Dans la page **général** , assurez-vous que le paramètre **activer la Fédération pour ce pool Edge (port 5061)** est coché.</span><span class="sxs-lookup"><span data-stu-id="cc8cc-173">On the **General** page, verify the **Enable federation for this Edge pool (Port 5061)** setting is checked.</span></span>
    
    <span data-ttu-id="cc8cc-174">![Boîte de dialogue Modifier les propriétés, page général](images/JJ688121.cc79a88c-cce4-4cab-80ad-4f70325dc7c4(OCS.15).jpg "Boîte de dialogue Modifier les propriétés, page général")</span><span class="sxs-lookup"><span data-stu-id="cc8cc-174">![Edit Properties dialog, General page](images/JJ688121.cc79a88c-cce4-4cab-80ad-4f70325dc7c4(OCS.15).jpg "Edit Properties dialog, General page")</span></span>

4.  <span data-ttu-id="cc8cc-175">Cliquez sur **OK** pour fermer la page modifier les propriétés.</span><span class="sxs-lookup"><span data-stu-id="cc8cc-175">Click **OK** to close the Edit Properties page.</span></span>

5.  <span data-ttu-id="cc8cc-176">Ensuite, accédez au nœud site.</span><span class="sxs-lookup"><span data-stu-id="cc8cc-176">Next, navigate to the site node.</span></span>

6.  <span data-ttu-id="cc8cc-177">Cliquez avec le bouton droit sur le site, puis cliquez sur **modifier les propriétés**.</span><span class="sxs-lookup"><span data-stu-id="cc8cc-177">Right-click the site, and then click **Edit Properties**.</span></span>

7.  <span data-ttu-id="cc8cc-178">Dans le volet de gauche, cliquez sur **route de Fédération**.</span><span class="sxs-lookup"><span data-stu-id="cc8cc-178">In the left pane, click **Federation route**.</span></span>

8.  <span data-ttu-id="cc8cc-179">Sous **affectation** de l’itinéraire de la Fédération de sites, sélectionnez **activer la Fédération SIP**, puis dans la liste, sélectionnez le serveur Edge Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="cc8cc-179">Under **Site federation route assignment**, select **Enable SIP federation**, and then from the list select the Lync Server 2013 Edge Server listed.</span></span>
    
    <span data-ttu-id="cc8cc-180">![Modifier les propriétés, page itinéraire de Fédération](images/JJ688121.c50c13b8-0859-4e3e-8793-45c431a5b4b5(OCS.15).jpg "Modifier les propriétés, page itinéraire de Fédération")</span><span class="sxs-lookup"><span data-stu-id="cc8cc-180">![Edit Properties, Federation route page](images/JJ688121.c50c13b8-0859-4e3e-8793-45c431a5b4b5(OCS.15).jpg "Edit Properties, Federation route page")</span></span>

9.  <span data-ttu-id="cc8cc-181">Cliquez sur **OK** pour fermer la page **modifier les propriétés** .</span><span class="sxs-lookup"><span data-stu-id="cc8cc-181">Click **OK** to close the **Edit Properties** page.</span></span>
    
    <span data-ttu-id="cc8cc-182">Pour les déploiements multisites, procédez comme suit sur chaque site.</span><span class="sxs-lookup"><span data-stu-id="cc8cc-182">For multi-site deployments, complete this procedure at each site.</span></span>

</div>

<div>

## <a name="to-publish-edge-server-configuration-changes"></a><span data-ttu-id="cc8cc-183">Pour publier les modifications de configuration de serveur Edge</span><span class="sxs-lookup"><span data-stu-id="cc8cc-183">To publish Edge Server configuration changes</span></span>

1.  <span data-ttu-id="cc8cc-184">Dans le **Générateur de topologie**, sélectionnez le nœud supérieur **serveur Lync** .</span><span class="sxs-lookup"><span data-stu-id="cc8cc-184">From **Topology Builder**, select the top node **Lync Server** .</span></span>

2.  <span data-ttu-id="cc8cc-185">Dans le menu **action** , sélectionnez **publier la topologie** et terminer l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="cc8cc-185">From the **Action** menu, select **Publish Topology** and complete the wizard.</span></span>

3.  <span data-ttu-id="cc8cc-186">Attendez la fin de la réplication Active Directory pour tous les pools du déploiement.</span><span class="sxs-lookup"><span data-stu-id="cc8cc-186">Wait for Active Directory replication to occur to all pools in the deployment.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="cc8cc-187">Le message suivant risque de s’afficher :</span><span class="sxs-lookup"><span data-stu-id="cc8cc-187">You may see the following message:</span></span><BR><span data-ttu-id="cc8cc-188"><STRONG>AVERTISSEMENT : la topologie comporte plus d’un serveur Edge fédéré. Cela peut se produire lors de la migration vers une version plus récente du produit. Dans ce cas, un seul serveur Edge serait utilisé activement pour la Fédération. Vérifiez que l’enregistrement SRV DNS externe pointe vers le serveur Edge approprié. Si vous voulez déployer plusieurs serveurs de périphérie de Fédération de manière à être actifs dans le cadre de la migration (autrement dit, qu’il ne s’agit pas d’un scénario de migration), vérifiez que tous les partenaires fédérés utilisent Lync Server. Vérifiez que l’enregistrement SRV DNS externe recense tous les serveurs Edge compatibles avec la Fédération.</STRONG></span><span class="sxs-lookup"><span data-stu-id="cc8cc-188"><STRONG>Warning: The topology contains more than one Federated Edge Server. This can occur during migration to a more recent version of the product. In that case, only one Edge Server would be actively used for federation. Verify that the external DNS SRV record points to the correct Edge Server. If you want to deploy multiple federation Edge Server to be active concurrently (that is, not a migration scenario), verify that all federated partners are using Lync Server. Verify that the external DNS SRV record lists all federation enabled Edge Servers.</STRONG></span></span><BR><span data-ttu-id="cc8cc-189">Cet avertissement est attendu et peut être ignoré en toute sécurité.</span><span class="sxs-lookup"><span data-stu-id="cc8cc-189">This warning is expected and can be safely ignored.</span></span>

    
    </div>

</div>

<div>

## <a name="to-configure-lync-server-2013-edge-server"></a><span data-ttu-id="cc8cc-190">Pour configurer Lync Server 2013 Edge Server</span><span class="sxs-lookup"><span data-stu-id="cc8cc-190">To configure Lync Server 2013 Edge Server</span></span>

1.  <span data-ttu-id="cc8cc-191">Accédez à tous les serveurs Edge Lync Server 2013 en ligne.</span><span class="sxs-lookup"><span data-stu-id="cc8cc-191">Bring all of the Lync Server 2013 Edge Servers online.</span></span>

2.  <span data-ttu-id="cc8cc-192">Mettez à jour les règles de routage de pare-feu externe ou les paramètres de l’équilibrage de charge matérielle pour envoyer le trafic SIP pour l’accès externe (en général, le port 443) et la Fédération (en général, le port 5061) vers le serveur Edge Lync Server 2013, au lieu du serveur Edge hérité.</span><span class="sxs-lookup"><span data-stu-id="cc8cc-192">Update the external firewall routing rules or the hardware load balancer settings to send SIP traffic for external access (usually port 443) and federation (usually port 5061) to the Lync Server 2013 Edge Server, instead of the legacy Edge Server.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="cc8cc-193">Si vous n’avez pas d’équilibrage de charge matérielle, vous devez mettre à jour l’enregistrement DNS A pour la Fédération pour résoudre le nouveau serveur Lync Server Access Edge.</span><span class="sxs-lookup"><span data-stu-id="cc8cc-193">If you do not have a hardware load balancer, you need to update the DNS A record for federation to resolve to the new Lync Server Access Edge server.</span></span> <span data-ttu-id="cc8cc-194">Pour effectuer cette opération avec un minimum de perturbation, réduisez la valeur TLL du nom de domaine complet (FQDN) du périmètre Lync Server de Lync Server de façon à ce qu’elle pointe vers le nouveau serveur Lync Server d’accès.</span><span class="sxs-lookup"><span data-stu-id="cc8cc-194">To accomplish this with minimum disruption, reduce the TLL value for the external Lync Server Access Edge FQDN so that when DNS is updated to point to the new Lync Server Access Edge, federation and remote access will be updated quickly.</span></span>

    
    </div>

3.  <span data-ttu-id="cc8cc-195">Ensuite, arrêtez le **Edge d’accès de Lync Server** depuis chaque ordinateur du serveur Edge.</span><span class="sxs-lookup"><span data-stu-id="cc8cc-195">Next, stop the **Lync Server Access Edge** from each Edge Server computer.</span></span>

4.  <span data-ttu-id="cc8cc-196">À partir de chaque ordinateur serveur Edge hérité, ouvrez l’application **services** à partir des **Outils d’administration**.</span><span class="sxs-lookup"><span data-stu-id="cc8cc-196">From each legacy Edge Server computer, open the **Services** applet from the **Administrative Tools**.</span></span>

5.  <span data-ttu-id="cc8cc-197">Dans la liste services, recherchez **Edge Access Server**.</span><span class="sxs-lookup"><span data-stu-id="cc8cc-197">In the services list, find **Lync Server Access Edge**.</span></span>

6.  <span data-ttu-id="cc8cc-198">Cliquez avec le bouton droit sur le nom des services, puis sélectionnez **arrêter** pour arrêter le service.</span><span class="sxs-lookup"><span data-stu-id="cc8cc-198">Right-click the services name, and then select **Stop** to stop the service.</span></span>

7.  <span data-ttu-id="cc8cc-199">Définissez le type de démarrage sur **désactivé**.</span><span class="sxs-lookup"><span data-stu-id="cc8cc-199">Set the Startup type to **Disabled**.</span></span>

8.  <span data-ttu-id="cc8cc-200">Cliquez sur **OK** pour fermer la fenêtre **Propriétés** .</span><span class="sxs-lookup"><span data-stu-id="cc8cc-200">Click **OK** to close the **Properties** window.</span></span>

<span data-ttu-id="cc8cc-201"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cc8cc-201"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

