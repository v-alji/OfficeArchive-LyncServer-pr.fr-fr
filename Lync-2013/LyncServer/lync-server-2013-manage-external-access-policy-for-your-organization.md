---
title: 'Lync Server 2013 : Gestion de la stratégie d’accès externe pour l’organisation'
description: 'Lync Server 2013 : gestion de la stratégie d’accès externe pour votre organisation.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Manage external access policy for your organization
ms:assetid: 5571811e-34c8-443a-b94c-1ab5d4275581
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520995(v=OCS.15)
ms:contentKeyID: 48184160
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8f0bb0e6764f67403065187c62debef13c77fcc3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426108"
---
# <a name="manage-external-access-policy-in-lync-server-2013"></a><span data-ttu-id="d3b69-103">Gestion de la stratégie d’accès externe dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d3b69-103">Manage external access policy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d3b69-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d3b69-104">

<span> </span></span></span>

<span data-ttu-id="d3b69-105">_**Dernière modification de la rubrique :** 2013-10-07_</span><span class="sxs-lookup"><span data-stu-id="d3b69-105">_**Topic Last Modified:** 2013-10-07_</span></span>

<span data-ttu-id="d3b69-106">Après le déploiement d’un ou plusieurs serveurs Edge, vous devez activer les types d’accès externe qui seront pris en charge pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="d3b69-106">After deploying one or more Edge Servers, you must enable the types of external access that will be supported for your organization.</span></span>

<span data-ttu-id="d3b69-107">Par défaut, il n’y a pas de stratégies configurées pour prendre en charge l’accès des utilisateurs externes, y compris les accès utilisateurs distants, l’accès des utilisateurs fédérés, même si vous avez déjà activé la prise en charge de l’accès des utilisateurs externes pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="d3b69-107">By default, there are no policies configured to support external user access, including remote user access, federated user access, even if you have already enabled external user access support for your organization.</span></span> <span data-ttu-id="d3b69-108">Pour contrôler l’utilisation de l’accès des utilisateurs externes, vous devez configurer une ou plusieurs stratégies en spécifiant le type d’accès des utilisateurs externes pris en charge pour chaque stratégie.</span><span class="sxs-lookup"><span data-stu-id="d3b69-108">To control the use of external user access, you must configure one or more policies, specifying the type of external user access supported for each policy.</span></span> <span data-ttu-id="d3b69-109">Les étendues de stratégie suivantes sont disponibles pour la création et la configuration.</span><span class="sxs-lookup"><span data-stu-id="d3b69-109">The following policy scopes are available for creation and configuration.</span></span> <span data-ttu-id="d3b69-110">Par défaut, la stratégie globale est créée, mais elle ne peut pas être supprimée.</span><span class="sxs-lookup"><span data-stu-id="d3b69-110">By default, the Global policy is created, but cannot be deleted.</span></span>

  - <span data-ttu-id="d3b69-111">**Politique globale**   La stratégie globale est créée lors du déploiement de votre serveur Edge.</span><span class="sxs-lookup"><span data-stu-id="d3b69-111">**Global policy**   The global policy is created when you deploy your Edge Servers.</span></span> <span data-ttu-id="d3b69-112">Par défaut, aucune option d’accès utilisateur externe n’est activée dans la stratégie globale.</span><span class="sxs-lookup"><span data-stu-id="d3b69-112">By default, no external user access options are enabled in the global policy.</span></span> <span data-ttu-id="d3b69-113">Pour prendre en charge l’accès des utilisateurs externes au niveau global, vous pouvez configurer la stratégie globale pour prendre en charge un ou plusieurs types d’options d’accès utilisateurs externes.</span><span class="sxs-lookup"><span data-stu-id="d3b69-113">To support external user access at the global level, you configure the global policy to support one or more types of external user access options.</span></span> <span data-ttu-id="d3b69-114">La politique globale s’applique à tous les utilisateurs de votre organisation, mais les stratégies de site et les stratégies d’utilisateur remplacent la stratégie globale.</span><span class="sxs-lookup"><span data-stu-id="d3b69-114">The global policy applies to all users in your organization, but site policies and user policies override the global policy.</span></span> <span data-ttu-id="d3b69-115">Si vous supprimez la stratégie globale, vous ne la supprimez pas.</span><span class="sxs-lookup"><span data-stu-id="d3b69-115">If you delete the global policy, you do not remove it.</span></span> <span data-ttu-id="d3b69-116">Au lieu de cela, vous rétablissez la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="d3b69-116">Instead, you reset it to the default setting.</span></span>

  - <span data-ttu-id="d3b69-117">**Stratégie de site**   Vous pouvez créer et configurer une ou plusieurs stratégies de site pour limiter l’accès des utilisateurs externes à des sites spécifiques.</span><span class="sxs-lookup"><span data-stu-id="d3b69-117">**Site policy**   You can create and configure one or more site policies to limit support for external user access to specific sites.</span></span> <span data-ttu-id="d3b69-118">La configuration de la stratégie de site remplace la stratégie globale, uniquement pour le site pour lequel elle est définie.</span><span class="sxs-lookup"><span data-stu-id="d3b69-118">The configuration in the site policy overrides the global policy, but only for the specific site covered by the site policy.</span></span> <span data-ttu-id="d3b69-119">Par exemple, si vous autorisez l’accès des utilisateurs distants dans la stratégie globale, vous pouvez spécifier une stratégie de site qui désactive l’accès des utilisateurs distants pour un site spécifique.</span><span class="sxs-lookup"><span data-stu-id="d3b69-119">For example, if you enable remote user access in the global policy, you might specify a site policy that disables remote user access for a specific site.</span></span> <span data-ttu-id="d3b69-120">Par défaut, une stratégie de site est appliquée à tous les utilisateurs de ce site, mais vous pouvez affecter une stratégie d’utilisateur à un utilisateur pour remplacer le paramètre de stratégie de site.</span><span class="sxs-lookup"><span data-stu-id="d3b69-120">By default, a site policy is applied to all users of that site, but you can assign a user policy to a user to override the site policy setting.</span></span>

  - <span data-ttu-id="d3b69-121">**Stratégie**   de l’utilisateur   Vous pouvez créer et configurer une ou plusieurs stratégies utilisateur pour limiter la prise en charge de l’accès des utilisateurs distants à des utilisateurs spécifiques.</span><span class="sxs-lookup"><span data-stu-id="d3b69-121">**User policy**   You can create and configure one or more user policies to limit support for remote user access to specific users.</span></span> <span data-ttu-id="d3b69-122">La configuration de la stratégie utilisateur remplace la stratégie globale et la stratégie de site, mais uniquement pour les utilisateurs spécifiques auxquels la stratégie utilisateur est affectée.</span><span class="sxs-lookup"><span data-stu-id="d3b69-122">The configuration in the user policy overrides the global and site policy, but only for the specific users to whom the user policy is assigned.</span></span> <span data-ttu-id="d3b69-123">Par exemple, si vous autorisez l’accès des utilisateurs distants dans la stratégie globale et la stratégie de site, vous pouvez spécifier une stratégie d’utilisateur qui désactive l’accès des utilisateurs distants, puis affecter cette stratégie à des utilisateurs spécifiques.</span><span class="sxs-lookup"><span data-stu-id="d3b69-123">For example, if you enable remote user access in the global policy and site policy, you might specify a user policy that disables remote user access and then assign that user policy to specific users.</span></span> <span data-ttu-id="d3b69-124">Si vous créez une stratégie d’utilisateur, vous devez l’appliquer à un ou plusieurs utilisateurs avant qu’elle ne soit appliquée.</span><span class="sxs-lookup"><span data-stu-id="d3b69-124">If you create a user policy, you must apply it to one or more users before it takes effect.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="d3b69-125">Les paramètres de stratégie Lync Server appliqués à un niveau de stratégie peuvent remplacer les paramètres appliqués à un autre niveau de stratégie.</span><span class="sxs-lookup"><span data-stu-id="d3b69-125">Lync Server policy settings that are applied at one policy level can override settings that are applied at another policy level.</span></span> <span data-ttu-id="d3b69-126">Le niveau de priorité de la stratégie de serveur Lync est défini comme suit : la stratégie d’utilisateur (la plus influence) a pour effet de remplacer une stratégie de site, puis une stratégie de site remplace une stratégie globale (moins l’influence).</span><span class="sxs-lookup"><span data-stu-id="d3b69-126">Lync Server policy precedence is: User policy (most influence) overrides a Site policy, and then a Site policy overrides a Global policy (least influence).</span></span> <span data-ttu-id="d3b69-127">Cela signifie que le paramètre de stratégie est plus proche de l’objet affecté par la stratégie, plus l’influence sur l’objet.</span><span class="sxs-lookup"><span data-stu-id="d3b69-127">This means that the closer the policy setting is to the object that the policy is affecting, the more influence it has on the object.</span></span>



</div>

<span data-ttu-id="d3b69-128">Ces options incluent les types d’accès externes suivants :</span><span class="sxs-lookup"><span data-stu-id="d3b69-128">These options include the following types of external access:</span></span>

  - <span data-ttu-id="d3b69-129">**Activer les communications avec les utilisateurs fédérés**   Activez cette opération si vous souhaitez prendre en charge l’accès des utilisateurs aux domaines partenaires fédérés.</span><span class="sxs-lookup"><span data-stu-id="d3b69-129">**Enable communications with federated users**   Enable this if you want to support user access to federated partner domains.</span></span> <span data-ttu-id="d3b69-130">Ce paramètre configure la possibilité pour les utilisateurs de communiquer avec d’autres domaines fédérés SIP, ainsi que des fournisseurs hébergés tels que Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="d3b69-130">This setting configures the ability for users to communicate with other SIP federated domains, as well as Hosted providers like Microsoft 365.</span></span> <span data-ttu-id="d3b69-131">Le choix de ce paramètre vous permet de sélectionner l’option permettant de communiquer avec des domaines fédérés XMPP.</span><span class="sxs-lookup"><span data-stu-id="d3b69-131">Selecting this setting allows you to select the option to allow communication with XMPP federated domains.</span></span>
    
    <span data-ttu-id="d3b69-132">Vous pouvez également sélectionner l’option **activer les communications avec les partenaires fédérés de XMPP** si vous activez **d’abord activer les communications avec les utilisateurs fédérés**.</span><span class="sxs-lookup"><span data-stu-id="d3b69-132">As an option, you can select **Enable communications with XMPP federated partners** if you first select **Enable communications with federated users**.</span></span> <span data-ttu-id="d3b69-133">La Fédération XMPP est une Fédération avec des organisations qui utilisent le protocole XMPP (extensible Messaging and Presence Protocol).</span><span class="sxs-lookup"><span data-stu-id="d3b69-133">XMPP federation is a federation with organizations that use extensible messaging and presence protocol (XMPP).</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="d3b69-134">Si vous activez la Fédération XMPP, vous devez également choisir de déployer la <STRONG>Fédération XMPP</STRONG> dans la section Configuration de pools de périphérie du générateur de topologie.</span><span class="sxs-lookup"><span data-stu-id="d3b69-134">If you enable XMPP federation, you must also select to deploy <STRONG>XMPP federation</STRONG> in the Edge pools configuration section of Topology Builder.</span></span> <span data-ttu-id="d3b69-135">La configuration de la Fédération XMPP déploie un proxy XMPP sur le serveur Edge et une passerelle XMPP sur le serveur frontal.</span><span class="sxs-lookup"><span data-stu-id="d3b69-135">Configuring for XMPP federation deploys an XMPP Proxy on the Edge Server and an XMPP gateway on the Front End Server.</span></span>

    
    </div>

  - <span data-ttu-id="d3b69-136">**Activer les communications avec les utilisateurs distants**   Activez cette option si vous souhaitez que les utilisateurs de votre organisation qui se trouvent en dehors de votre pare-feu (par exemple, des télétravailleurs et des utilisateurs qui voyagent) puissent se connecter à Lync Server via Internet.</span><span class="sxs-lookup"><span data-stu-id="d3b69-136">**Enable communications with remote users**   Enable this option if you want users in your organization who are outside your firewall, such as telecommuters and users who are traveling, to be able to connect to Lync Server over the Internet.</span></span>

  - <span data-ttu-id="d3b69-137">**Activer les communications avec les utilisateurs publics**   Activez cette option si vous souhaitez que les utilisateurs internes puissent communiquer avec des contacts de fournisseurs de messagerie instantanée publics, tels que ceux fournis par Windows Live, Yahoo \! et America Online (AOL).</span><span class="sxs-lookup"><span data-stu-id="d3b69-137">**Enable communications with public users**   Enable this option if you want internal users to be able to communicate with public IM provider contacts, such as those provided by Windows Live, Yahoo\!, and America Online (AOL).</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <UL>
    > <LI>
    > <P><span data-ttu-id="d3b69-138">À compter du 1er septembre, 2012, le contrat de licence de l’utilisateur Microsoft Lync Public IM Connectivity (« PIC USL ») ne sera plus disponible à l’achat pour les contrats de nouveau ou de renouvellement.</span><span class="sxs-lookup"><span data-stu-id="d3b69-138">As of September 1st, 2012, the Microsoft Lync Public IM Connectivity User Subscription License (“PIC USL”) is no longer available for purchase for new or renewing agreements.</span></span> <span data-ttu-id="d3b69-139">Les clients disposant de licences actives seront en mesure de continuer à fédérer avec Yahoo !</span><span class="sxs-lookup"><span data-stu-id="d3b69-139">Customers with active licenses will be able to continue to federate with Yahoo!</span></span> <span data-ttu-id="d3b69-140">Messenger jusqu’à la date d’arrêt du service.</span><span class="sxs-lookup"><span data-stu-id="d3b69-140">Messenger until the service shut down date.</span></span> <span data-ttu-id="d3b69-141">Date de fin de vie du 2014 juin pour AOL et Yahoo !</span><span class="sxs-lookup"><span data-stu-id="d3b69-141">An end of life date of June 2014 for AOL and Yahoo!</span></span> <span data-ttu-id="d3b69-142">a été annoncé.</span><span class="sxs-lookup"><span data-stu-id="d3b69-142">has been announced.</span></span> <span data-ttu-id="d3b69-143">Pour plus d’informations, voir <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">prise en charge de la connectivité de messagerie instantanée publique dans Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="d3b69-143">For details, see <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Support for public instant messenger connectivity in Lync Server 2013</A>.</span></span></P>
    > <LI>
    > <P><span data-ttu-id="d3b69-144">La fonction USL (PIC) est une licence d’abonnement par mois qui est requise pour que Lync Server ou Office Communications Server se fédérer avec Yahoo !</span><span class="sxs-lookup"><span data-stu-id="d3b69-144">The PIC USL is a per-user per-month subscription license that is required for Lync Server or Office Communications Server to federate with Yahoo!</span></span> <span data-ttu-id="d3b69-145">Messenger.</span><span class="sxs-lookup"><span data-stu-id="d3b69-145">Messenger.</span></span> <span data-ttu-id="d3b69-146">La capacité de Microsoft à fournir ce service est subordonné à la prise en charge de Yahoo !, le contrat sous-jacent pour lequel le son est arrêté.</span><span class="sxs-lookup"><span data-stu-id="d3b69-146">Microsoft’s ability to provide this service has been contingent upon support from Yahoo!, the underlying agreement for which is winding down.</span></span></P>
    > <LI>
    > <P><span data-ttu-id="d3b69-147">Plus que jamais, Lync est un outil puissant de connexion entre organisations et de personnes dans le monde entier.</span><span class="sxs-lookup"><span data-stu-id="d3b69-147">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="d3b69-148">La Fédération avec Windows Live Messenger ne nécessite aucune licence d’utilisateur/appareil supplémentaire au-delà de la CAL standard Lync.</span><span class="sxs-lookup"><span data-stu-id="d3b69-148">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard CAL.</span></span> <span data-ttu-id="d3b69-149">Skype Federation sera ajouté à cette liste et permettra aux utilisateurs de Lync de joindre des centaines de millions de personnes à la messagerie instantanée et à la voix.</span><span class="sxs-lookup"><span data-stu-id="d3b69-149">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people with IM and voice.</span></span></P></LI></UL>

    
    </div>

<div>


> [!NOTE]  
> <span data-ttu-id="d3b69-150">Outre l’activation de la prise en charge de l’accès des utilisateurs externes, vous devez également configurer des stratégies pour contrôler l’utilisation de l’accès des utilisateurs externes au sein de votre organisation avant de pouvoir accéder aux utilisateurs externes.</span><span class="sxs-lookup"><span data-stu-id="d3b69-150">In addition to enabling external user access support, you must also configure policies to control the use of external user access in your organization before any type of external user access is available to users.</span></span> <span data-ttu-id="d3b69-151">Pour plus d’informations sur la création, la configuration et l’application de stratégies pour l’accès des utilisateurs externes, voir <A href="lync-server-2013-enable-or-disable-remote-user-access.md">activer ou désactiver l’accès des utilisateurs distants dans Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="d3b69-151">For details about creating, configuring, and applying policies for external user access see <A href="lync-server-2013-enable-or-disable-remote-user-access.md">Enable or disable remote user access in Lync Server 2013</A>.</span></span>



</div>

<span data-ttu-id="d3b69-152">**Pour afficher les stratégies d’accès externe à l’aide des cmdlets Windows PowerShell**</span><span class="sxs-lookup"><span data-stu-id="d3b69-152">**To view external access policies by using Windows PowerShell cmdlets**</span></span>

  - <span data-ttu-id="d3b69-153">Vous pouvez afficher les stratégies d’accès externe à l’aide de Lync Server Management Shell et de l’applet **de passe Get-CsExternalAccessPolicy** .</span><span class="sxs-lookup"><span data-stu-id="d3b69-153">You can view external access policies by using Lync Server Management Shell and the **Get-CsExternalAccessPolicy** cmdlet.</span></span> <span data-ttu-id="d3b69-154">Vous pouvez exécuter cette applet de commande sur Lync Server 2013 Management Shell ou à partir d’une session distante de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d3b69-154">You can run this cmdlet from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="d3b69-155">Pour plus d’informations sur l’utilisation de Windows PowerShell distant pour vous connecter à Lync Server, voir l’article de blog Lync Server Windows PowerShell « démarrage rapide : gestion de Microsoft Lync Server 2010 à l’aide de Remote PowerShell » [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="d3b69-155">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>
    
    <span data-ttu-id="d3b69-156">Pour afficher des informations sur les stratégies d’accès externe, tapez la commande suivante dans Lync Server Management Shell, puis appuyez sur entrée :</span><span class="sxs-lookup"><span data-stu-id="d3b69-156">To view information about all your external access policies, type the following command in the Lync Server Management Shell and then press ENTER:</span></span>
    
        Get-CsExternalAccessPolicy
    
    <span data-ttu-id="d3b69-157">Cette commande renvoie le type d’informations suivant :</span><span class="sxs-lookup"><span data-stu-id="d3b69-157">This command returns information similar to the following:</span></span>
    
        Identity                          : Global
        Description                       :
        EnableFederationAccess            : False
        EnableXmppAccess                  : False
        EnablePublicCloudAccess           : False
        EnablePublicCloudAudioVideoAccess : False
        EnableOutsideAccess               : False

<div>

## <a name="in-this-section"></a><span data-ttu-id="d3b69-158">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="d3b69-158">In This Section</span></span>

  - [<span data-ttu-id="d3b69-159">Configuration des stratégies de contrôle d’accès des utilisateurs fédérés dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d3b69-159">Configure policies to control federated user access in Lync Server 2013</span></span>](lync-server-2013-configure-policies-to-control-federated-user-access.md)

  - [<span data-ttu-id="d3b69-160">Configuration des stratégies de contrôle d’accès des utilisateurs fédérés XMPP dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d3b69-160">Configure policies to control XMPP federated user access in Lync Server 2013</span></span>](lync-server-2013-configure-policies-to-control-xmpp-federated-user-access.md)

  - [<span data-ttu-id="d3b69-161">Configuration des stratégies de contrôle d’accès des utilisateurs distants dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d3b69-161">Configure policies to control remote user access in Lync Server 2013</span></span>](lync-server-2013-configure-policies-to-control-remote-user-access.md)

  - [<span data-ttu-id="d3b69-162">Configuration des stratégies de contrôle d’accès des utilisateurs publics dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d3b69-162">Configure policies to control public user access in Lync Server 2013</span></span>](lync-server-2013-configure-policies-to-control-public-user-access.md)

  - [<span data-ttu-id="d3b69-163">Attribution d’une stratégie d’accès des utilisateurs externes à un utilisateur activé pour Lync dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d3b69-163">Assign an external user access policy to a Lync enabled user in Lync Server 2013</span></span>](lync-server-2013-assign-an-external-user-access-policy-to-a-lync-enabled-user.md)

  - [<span data-ttu-id="d3b69-164">Réinitialisation ou suppression des stratégies d’accès des utilisateurs externes dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d3b69-164">Resetting or deleting external user access policies in Lync Server 2013</span></span>](lync-server-2013-resetting-or-deleting-external-user-access-policies.md)

<span data-ttu-id="d3b69-165"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d3b69-165"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

