---
title: 'Lync Server 2013 : définir une passerelle dans le générateur de topologie'
description: 'Lync Server 2013 : définissez une passerelle dans le générateur de topologie.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Define a gateway in Topology Builder
ms:assetid: 456e5a96-d9f6-42a6-862c-a69464391628
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425945(v=OCS.15)
ms:contentKeyID: 48184036
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1f8bf09f06f54d8988c8c9a9e385ef251a960bd6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431188"
---
# <a name="define-a-gateway-in-topology-builder-in-lync-server-2013"></a><span data-ttu-id="ecc10-103">Définir une passerelle dans le générateur de topologies de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ecc10-103">Define a gateway in Topology Builder in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ecc10-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ecc10-104">

<span> </span></span></span>

<span data-ttu-id="ecc10-105">_**Dernière modification de la rubrique :** 2012-10-04_</span><span class="sxs-lookup"><span data-stu-id="ecc10-105">_**Topic Last Modified:** 2012-10-04_</span></span>

<span data-ttu-id="ecc10-106">Suivez les étapes ci-dessous pour définir un *homologue* qui vous permet d’associer un serveur de médiation afin de fournir une connectivité au réseau téléphonique commuté (PSTN) pour les utilisateurs autorisés à utiliser voix entreprise.</span><span class="sxs-lookup"><span data-stu-id="ecc10-106">Follow these steps to use Topology Builder to define a *peer* with which you can associate a Mediation Server to provide connectivity to the public switched telephone network (PSTN) for users enabled for Enterprise Voice.</span></span> <span data-ttu-id="ecc10-107">Un hôte du serveur de médiation peut être une passerelle RTC, un PBX IP ou un contrôleur de bordure de session (SBC) pour un fournisseur de services de téléphonie Internet (ITSP) auquel vous vous connectez en configurant un Trunk SIP.</span><span class="sxs-lookup"><span data-stu-id="ecc10-107">A peer to the Mediation Server can be a PSTN gateway, an IP-PBX, or a Session Border Controller (SBC) for an Internet Telephony Service Provider (ITSP) to which you connect by configuring a SIP trunk.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="ecc10-108">Dans cette rubrique, nous partons du principe que vous avez configuré au moins une réserve interne ou un serveur Standard Edition Server dans au moins un site central doté d’un serveur de médiation autonome ou autonome, comme décrit dans <A href="lync-server-2013-define-and-configure-a-front-end-pool-or-standard-edition-server.md">la rubrique définir et configurer un pool frontal ou un serveur Standard Edition Server dans Lync server 2013</A> et <A href="lync-server-2013-publish-the-topology.md">publier la topologie dans Lync Server 2013</A> dans la documentation de déploiement.</span><span class="sxs-lookup"><span data-stu-id="ecc10-108">This topic assumes that you have set up at least one internal Front End pool or Standard Edition server in at least one central site with a collocated or stand-alone Mediation Server, as described in <A href="lync-server-2013-define-and-configure-a-front-end-pool-or-standard-edition-server.md">Define and configure a Front End pool or Standard Edition server in Lync Server 2013</A> and <A href="lync-server-2013-publish-the-topology.md">Publish the topology in Lync Server 2013</A> in the Deployment documentation.</span></span> <span data-ttu-id="ecc10-109">Dans cette rubrique, nous partons également du principe que vous avez vérifié que votre infrastructure répond aux conditions préalables décrites dans la rubrique <A href="lync-server-2013-software-prerequisites-for-enterprise-voice.md">logiciels requis pour Enterprise Voice de Lync server 2013</A> et de <A href="lync-server-2013-security-and-configuration-prerequisites-for-enterprise-voice.md">sécurité et configuration requise pour Enterprise Voice dans Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="ecc10-109">This topic also assumes that you have verified that your infrastructure meets the prerequisites described in <A href="lync-server-2013-software-prerequisites-for-enterprise-voice.md">Software prerequisites for Enterprise Voice in Lync Server 2013</A> and <A href="lync-server-2013-security-and-configuration-prerequisites-for-enterprise-voice.md">Security and configuration prerequisites for Enterprise Voice in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="to-define-a-peer-for-the-mediation-server"></a><span data-ttu-id="ecc10-110">Pour définir un homologue pour le serveur de médiation</span><span class="sxs-lookup"><span data-stu-id="ecc10-110">To Define a Peer for the Mediation Server</span></span>

1.  <span data-ttu-id="ecc10-111">Démarrer le générateur de topologie : cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Générateur de topologie de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="ecc10-111">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>

2.  <span data-ttu-id="ecc10-112">Sous Lync Server 2013, le nom de votre site, composants partagés, cliquez avec le bouton droit sur le nœud **passerelles RTC** , puis cliquez sur **nouvelle passerelle PSTN**.</span><span class="sxs-lookup"><span data-stu-id="ecc10-112">Under Lync Server 2013, your site name, Shared Components, right-click the **PSTN Gateways** node, and then click **New PSTN Gateway**.</span></span>
    
    <span data-ttu-id="ecc10-113">![d898c3c1-8798-4b74-8f02-b994ef3db4c1](images/Gg425945.d898c3c1-8798-4b74-8f02-b994ef3db4c1(OCS.15).png "d898c3c1-8798-4b74-8f02-b994ef3db4c1")</span><span class="sxs-lookup"><span data-stu-id="ecc10-113">![d898c3c1-8798-4b74-8f02-b994ef3db4c1](images/Gg425945.d898c3c1-8798-4b74-8f02-b994ef3db4c1(OCS.15).png "d898c3c1-8798-4b74-8f02-b994ef3db4c1")</span></span>

3.  <span data-ttu-id="ecc10-114">Dans **Définir une nouvelle passerelle IP/RTC**, tapez le nom de domaine complet ou l’adresse IP de l’homologue, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="ecc10-114">In **Define New IP/PSTN Gateway**, type the fully qualified domain name (FQDN) or IP address of the peer, and click **Next**.</span></span>
    
    <span data-ttu-id="ecc10-115">![8017ba5e-41bc-48d4-97d9-fd306cd322b8](images/Gg425945.8017ba5e-41bc-48d4-97d9-fd306cd322b8(OCS.15).png "8017ba5e-41bc-48d4-97d9-fd306cd322b8")</span><span class="sxs-lookup"><span data-stu-id="ecc10-115">![8017ba5e-41bc-48d4-97d9-fd306cd322b8](images/Gg425945.8017ba5e-41bc-48d4-97d9-fd306cd322b8(OCS.15).png "8017ba5e-41bc-48d4-97d9-fd306cd322b8")</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="ecc10-116">Si vous spécifiez TLS (Transport Layer Security) comme type de transport, vous devez spécifier le nom de domaine complet (FQDN) au lieu de l’adresse IP de l’homologue du serveur de médiation.</span><span class="sxs-lookup"><span data-stu-id="ecc10-116">If you specify Transport Layer Security (TLS) as the transport type, you must specify the FQDN instead of the IP address of the peer of the Mediation Server.</span></span>

    
    </div>

4.  <span data-ttu-id="ecc10-117">Définissez le mode d’écoute (IPv4 ou IPv6) de l’adresse IP de votre nouvelle passerelle RTC, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="ecc10-117">Define the listening mode (IPv4 or IPv6) of the IP address of your new PSTN gateway, and click **Next**.</span></span>
    
    <span data-ttu-id="ecc10-118">![c7fc0d12-adc8-45a7-aca1-b376e1d2fcec](images/Gg425945.c7fc0d12-adc8-45a7-aca1-b376e1d2fcec(OCS.15).png "c7fc0d12-adc8-45a7-aca1-b376e1d2fcec")</span><span class="sxs-lookup"><span data-stu-id="ecc10-118">![c7fc0d12-adc8-45a7-aca1-b376e1d2fcec](images/Gg425945.c7fc0d12-adc8-45a7-aca1-b376e1d2fcec(OCS.15).png "c7fc0d12-adc8-45a7-aca1-b376e1d2fcec")</span></span>

5.  <span data-ttu-id="ecc10-119">Définissez une *jonction racine* pour la passerelle RTC.</span><span class="sxs-lookup"><span data-stu-id="ecc10-119">Define a *root trunk* for the PSTN gateway.</span></span> <span data-ttu-id="ecc10-120">Un Trunk est une connexion logique entre un serveur de médiation et une passerelle identifiée de manière unique par le tuple.</span><span class="sxs-lookup"><span data-stu-id="ecc10-120">A trunk is a logical connection between a Mediation Server and a gateway uniquely identified by the tuple.</span></span>
    
    <span data-ttu-id="ecc10-121">Le nom de domaine complet du serveur de médiation, port d’écoute du serveur de médiation (TLS ou TCP) : adresse IP et nom de domaine complet de la passerelle</span><span class="sxs-lookup"><span data-stu-id="ecc10-121">{Mediation Server FQDN, Mediation Server listening port (TLS or TCP) : gateway IP and FQDN, gateway listening port}</span></span>
    
      - <span data-ttu-id="ecc10-122">Lors de la définition d’une passerelle RTC dans le générateur de topologie, vous devez définir une Trunk racine pour ajouter correctement la passerelle RTC à votre topologie.</span><span class="sxs-lookup"><span data-stu-id="ecc10-122">When defining a PSTN gateway in Topology Builder, you must define a root trunk to successfully add the PSTN gateway to your topology.</span></span>
    
      - <span data-ttu-id="ecc10-123">Vous ne pouvez pas supprimer la jonction racine tant que la passerelle RTC associée n’est pas supprimée.</span><span class="sxs-lookup"><span data-stu-id="ecc10-123">The root trunk cannot be removed until the associated PSTN gateway is removed.</span></span>
    
    <span data-ttu-id="ecc10-124">![3b030757-eb35-4616-bb6b-74ee67507e3d](images/Gg425945.3b030757-eb35-4616-bb6b-74ee67507e3d(OCS.15).png "3b030757-eb35-4616-bb6b-74ee67507e3d")</span><span class="sxs-lookup"><span data-stu-id="ecc10-124">![3b030757-eb35-4616-bb6b-74ee67507e3d](images/Gg425945.3b030757-eb35-4616-bb6b-74ee67507e3d(OCS.15).png "3b030757-eb35-4616-bb6b-74ee67507e3d")</span></span>

6.  <span data-ttu-id="ecc10-125">Sous **port d’écoute pour la passerelle RTC/IP**, tapez le port d’écoute que la passerelle, le PBX ou la SBC utilisera pour les messages SIP du serveur de médiation qui sera associé au Trunk racine de la passerelle RTC.</span><span class="sxs-lookup"><span data-stu-id="ecc10-125">Under **Listening Port for IP/PSTN Gateway**, type the listening port that the gateway, PBX, or SBC will use for SIP messages from the Mediation Server that will be associated with the root trunk of the PSTN gateway.</span></span> <span data-ttu-id="ecc10-126">(Par défaut, les ports sont 5066 pour TCP [Transmission Control Protocol] et 5067 pour TLS [Transport Layer Security] sur une passerelle RTC, un autocommutateur privé [PBX] ou un contrôleur SBC.</span><span class="sxs-lookup"><span data-stu-id="ecc10-126">(By default, the ports are 5066 for Transmission Control Protocol (TCP) and 5067 for Transport Layer Security (TLS) on a PSTN gateway, PBX or SBC.</span></span> <span data-ttu-id="ecc10-127">Sur une unité de branchement Survivable sur une succursale, les ports par défaut sont 5081 pour TCP et 5082 pour TLS.)</span><span class="sxs-lookup"><span data-stu-id="ecc10-127">On a Survivable Branch Appliance at a branch site, the default ports are 5081 for TCP and 5082 for TLS.)</span></span>

7.  <span data-ttu-id="ecc10-128">Sous **Protocole de transport SIP**, cliquez sur le type de transport utilisé par l’homologue, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="ecc10-128">Under **SIP Transport Protocol**, click the transport type that the peer uses, and then click **OK**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="ecc10-129">Pour des raisons de sécurité, nous vous recommandons vivement de déployer un homologue sur le serveur de médiation qui peut utiliser le protocole TLS.</span><span class="sxs-lookup"><span data-stu-id="ecc10-129">For security reasons, we strongly recommend that you deploy a peer to the Mediation Server that can use TLS.</span></span>

    
    </div>

8.  <span data-ttu-id="ecc10-130">Sous **serveur de médiation associé**, sélectionnez le pool de serveurs de médiation à associer au Trunk racine de cette passerelle PSTN.</span><span class="sxs-lookup"><span data-stu-id="ecc10-130">Under **Associated Mediation Server**, select the Mediation Server pool to associate with the root trunk of this PSTN Gateway.</span></span>

9.  <span data-ttu-id="ecc10-131">Sous **port du serveur de médiation associé**, tapez le port d’écoute que le serveur de médiation utilisera pour les messages SIP de la passerelle.</span><span class="sxs-lookup"><span data-stu-id="ecc10-131">Under **Associated Mediation Server port**, type the listening port that the Mediation Server will use for SIP messages from the gateway.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="ecc10-132">La prise en charge de l’utilisation de circuits multiples dans Lync Server 2013 permet de définir plusieurs ports de signalisation SIP sur le serveur de médiation pour communiquer avec plusieurs passerelles RTC.</span><span class="sxs-lookup"><span data-stu-id="ecc10-132">With multiple trunk support in Lync Server 2013, multiple SIP signaling ports can be defined on the Mediation Server to be used for communication with multiple PSTN gateways.</span></span> <span data-ttu-id="ecc10-133">Lors de la définition d’un Trunk, le <STRONG>port du serveur de médiation associé</STRONG> doit figurer dans la plage des ports d’écoute pour le protocole correspondant autorisé par le serveur de médiation.</span><span class="sxs-lookup"><span data-stu-id="ecc10-133">When defining a trunk, the <STRONG>Associated Mediation Server port</STRONG> must be within the range of the listening ports for the respective protocol allowed by the Mediation Server.</span></span> <span data-ttu-id="ecc10-134">Cette plage de ports est définie sous Lync Server 2013 et les pools de médiation.</span><span class="sxs-lookup"><span data-stu-id="ecc10-134">This port range is defined under Lync Server 2013 and Mediation Pools.</span></span> <span data-ttu-id="ecc10-135">Cliquez avec le bouton droit sur le pool de serveurs de médiation qui vous intéresse, puis sélectionnez <STRONG>modifier les propriétés</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="ecc10-135">Right-click the Mediation Server pool of interest, and select <STRONG>Edit Properties</STRONG>.</span></span> <span data-ttu-id="ecc10-136">Specify the port range in the <STRONG>Listening ports</STRONG> field.</span><span class="sxs-lookup"><span data-stu-id="ecc10-136">Specify the port range in the <STRONG>Listening ports</STRONG> field.</span></span>

    
    </div>

10. <span data-ttu-id="ecc10-137">Cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="ecc10-137">Click **Finish**.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="ecc10-138">Avant d’achever cette étape, assurez-vous que l’homologue que vous avez défini s’exécute et utilise le nom de domaine complet ou l’adresse IP que vous avez spécifiée.</span><span class="sxs-lookup"><span data-stu-id="ecc10-138">Before you finish this step, be sure that the peer that you defined is running and using the FQDN or IP address that you specified.</span></span>



</div>

<span data-ttu-id="ecc10-139">Ensuite, pour ajouter l’homologue à la topologie, suivez les procédures décrites dans [publier la topologie dans Lync Server 2013](lync-server-2013-publish-the-topology.md) dans la documentation de déploiement.</span><span class="sxs-lookup"><span data-stu-id="ecc10-139">Next, to add the peer to the topology, follow the procedures in [Publish the topology in Lync Server 2013](lync-server-2013-publish-the-topology.md) in the Deployment documentation.</span></span> <span data-ttu-id="ecc10-140">Vous devez publier votre topologie chaque fois que vous utilisez le générateur de topologie pour générer ou modifier votre topologie, de telle sorte que les données puissent être utilisées pour installer les fichiers pour les serveurs exécutant Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ecc10-140">You must publish your topology each time that you use Topology Builder to build or modify your topology, so that the data can be used to install the files for servers that are running Lync Server.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="ecc10-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ecc10-141">See Also</span></span>


[<span data-ttu-id="ecc10-142">Modifier un Trunk dans le générateur de topologies de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ecc10-142">Modify a trunk in Topology Builder in Lync Server 2013</span></span>](lync-server-2013-modify-a-trunk-in-topology-builder.md)  
  

<span data-ttu-id="ecc10-143"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ecc10-143"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

