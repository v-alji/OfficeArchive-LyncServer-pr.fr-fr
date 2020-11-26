---
title: 'Lync Server 2013 : Définition de la configuration requise pour les serveurs frontaux, la messagerie instantanée et la présence'
description: 'Lync Server 2013 : définition de vos exigences pour les serveurs frontaux, la messagerie instantanée et la présence.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Defining your requirements for Front End Servers, instant messaging, and presence
ms:assetid: c21198bc-520c-4d17-8b84-7ff1475b9b0a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412956(v=OCS.15)
ms:contentKeyID: 48185319
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 923132b32d5aef80191b19a7b85c3f17276e5946
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430811"
---
# <a name="defining-your-requirements-for-front-end-servers-instant-messaging-and-presence-in-lync-server-2013"></a><span data-ttu-id="d7fe7-103">Définition de la configuration requise pour les serveurs frontaux, la messagerie instantanée et la présence dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d7fe7-103">Defining your requirements for Front End Servers, instant messaging, and presence in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d7fe7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d7fe7-104">

<span> </span></span></span>

<span data-ttu-id="d7fe7-105">_**Dernière modification de la rubrique :** 2013-10-07_</span><span class="sxs-lookup"><span data-stu-id="d7fe7-105">_**Topic Last Modified:** 2013-10-07_</span></span>

<span data-ttu-id="d7fe7-106">La principale tâche de planification de la messagerie instantanée et de la présence consiste à vérifier que vous disposez de suffisamment de serveurs front-end pour vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="d7fe7-106">The main task of planning for instant messaging (IM) and presence is ensuring that you have enough Front End Servers for your users.</span></span>

<div>

## <a name="enabling-communication-with-external-users"></a><span data-ttu-id="d7fe7-107">Activation de la communication avec des utilisateurs externes</span><span class="sxs-lookup"><span data-stu-id="d7fe7-107">Enabling Communication with External Users</span></span>

<span data-ttu-id="d7fe7-108">Vous pouvez considérablement augmenter les avantages de votre investissement dans Lync Server en permettant aux utilisateurs de communiquer avec des utilisateurs externes.</span><span class="sxs-lookup"><span data-stu-id="d7fe7-108">You can greatly increase the benefits of your investment in Lync Server by enabling your users to communicate with external users.</span></span> <span data-ttu-id="d7fe7-109">Exemples d’utilisateurs externes :</span><span class="sxs-lookup"><span data-stu-id="d7fe7-109">External users can include:</span></span>

  - <span data-ttu-id="d7fe7-110">**Utilisateurs distants**   Les utilisateurs propres de votre organisation, lorsqu’ils travaillent à l’extérieur de votre pare-feu et qu’ils utilisent leur ordinateur portable ou d’autres appareils Lync Server.</span><span class="sxs-lookup"><span data-stu-id="d7fe7-110">**Remote users**   Your organization’s own users, when they are working outside your firewalls and are using their laptops or other Lync Server devices.</span></span>

  - <span data-ttu-id="d7fe7-111">**Utilisateurs fédérés**   Utilisateurs des entreprises avec lesquelles vous travaillez également sur le serveur Lync.</span><span class="sxs-lookup"><span data-stu-id="d7fe7-111">**Federated users**   Users from companies you work with who also run Lync Server.</span></span> <span data-ttu-id="d7fe7-112">Pour autoriser vos utilisateurs à communiquer facilement avec ces utilisateurs externes, créez des relations fédérées avec ces entreprises.</span><span class="sxs-lookup"><span data-stu-id="d7fe7-112">To enable your users to easily contact these users, you create federated relationships with these companies.</span></span>

  - <span data-ttu-id="d7fe7-113">**Utilisateurs publics**   Utilisateurs des services de messagerie instantanée publics, tels que les services de messagerie instantanée fournis par le réseau Windows Live de services Internet, Yahoo \! et AOL, ainsi que les utilisateurs de fournisseurs et de serveurs utilisant le protocole XMPP (extensible Messaging and Presence Protocol), tel que Google Talk.</span><span class="sxs-lookup"><span data-stu-id="d7fe7-113">**Public users**   Users of public IM services, such as IM services provided by the Windows Live network of Internet services, Yahoo\!, and AOL, and users of providers and servers that use Extensible Messaging and Presence Protocol (XMPP), such as Google Talk.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="d7fe7-114">Notez qu’une licence distincte peut être nécessaire pour la connectivité de messagerie instantanée publique avec Windows Live, AOL et Yahoo !</span><span class="sxs-lookup"><span data-stu-id="d7fe7-114">Note that a separate license might be required for public IM connectivity with Windows Live, AOL, and Yahoo!</span></span>

    
    </div>
    
    <div>
    

    > [!IMPORTANT]  
    > <UL>
    > <LI>
    > <P><span data-ttu-id="d7fe7-115">À compter du 1er septembre, 2012, le contrat de licence de l’utilisateur Microsoft Lync Public IM Connectivity (« PIC USL ») ne sera plus disponible à l’achat pour les contrats de nouveau ou de renouvellement.</span><span class="sxs-lookup"><span data-stu-id="d7fe7-115">As of September 1st, 2012, the Microsoft Lync Public IM Connectivity User Subscription License (“PIC USL”) is no longer available for purchase for new or renewing agreements.</span></span> <span data-ttu-id="d7fe7-116">Les clients disposant de licences actives seront en mesure de continuer à fédérer avec Yahoo !</span><span class="sxs-lookup"><span data-stu-id="d7fe7-116">Customers with active licenses will be able to continue to federate with Yahoo!</span></span> <span data-ttu-id="d7fe7-117">Messenger jusqu’à la date d’arrêt du service.</span><span class="sxs-lookup"><span data-stu-id="d7fe7-117">Messenger until the service shut down date.</span></span> <span data-ttu-id="d7fe7-118">Date de fin de vie du 2014 juin pour AOL et Yahoo !</span><span class="sxs-lookup"><span data-stu-id="d7fe7-118">An end of life date of June 2014 for AOL and Yahoo!</span></span> <span data-ttu-id="d7fe7-119">a été annoncé.</span><span class="sxs-lookup"><span data-stu-id="d7fe7-119">has been announced.</span></span> <span data-ttu-id="d7fe7-120">Pour plus d’informations, voir <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">prise en charge de la connectivité de messagerie instantanée publique dans Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="d7fe7-120">For details, see <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Support for public instant messenger connectivity in Lync Server 2013</A>.</span></span></P>
    > <LI>
    > <P><span data-ttu-id="d7fe7-121">La fonction USL (PIC) est une licence d’abonnement par mois qui est requise pour que Lync Server ou Office Communications Server se fédérer avec Yahoo !</span><span class="sxs-lookup"><span data-stu-id="d7fe7-121">The PIC USL is a per-user per-month subscription license that is required for Lync Server or Office Communications Server to federate with Yahoo!</span></span> <span data-ttu-id="d7fe7-122">Messenger.</span><span class="sxs-lookup"><span data-stu-id="d7fe7-122">Messenger.</span></span> <span data-ttu-id="d7fe7-123">La capacité de Microsoft à fournir ce service est subordonné à la prise en charge de Yahoo !, le contrat sous-jacent pour lequel le son est arrêté.</span><span class="sxs-lookup"><span data-stu-id="d7fe7-123">Microsoft’s ability to provide this service has been contingent upon support from Yahoo!, the underlying agreement for which is winding down.</span></span></P>
    > <LI>
    > <P><span data-ttu-id="d7fe7-124">Plus que jamais, Lync est un outil puissant de connexion entre organisations et de personnes dans le monde entier.</span><span class="sxs-lookup"><span data-stu-id="d7fe7-124">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="d7fe7-125">La Fédération avec Windows Live Messenger ne nécessite aucune licence d’utilisateur/appareil supplémentaire au-delà de la CAL standard Lync.</span><span class="sxs-lookup"><span data-stu-id="d7fe7-125">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard CAL.</span></span> <span data-ttu-id="d7fe7-126">Skype Federation sera ajouté à cette liste et permettra aux utilisateurs de Lync de joindre des centaines de millions de personnes à la messagerie instantanée et à la voix.</span><span class="sxs-lookup"><span data-stu-id="d7fe7-126">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people with IM and voice.</span></span></P></LI></UL>

    
    </div>

<span data-ttu-id="d7fe7-127">Pour activer tout ou partie de ces scénarios, vous devez déployer un serveur Edge pour sécuriser les communications entre le déploiement de votre serveur Lync et les utilisateurs externes.</span><span class="sxs-lookup"><span data-stu-id="d7fe7-127">To enable any or all of these scenarios, you need to deploy an Edge Server to help enable secure communications between your Lync Server deployment and external users.</span></span> <span data-ttu-id="d7fe7-128">Les utilisateurs distants de votre organisation et les utilisateurs d’organisations fédérées seront en mesure de détecter leur présence mutuelle et de communiquer via la messagerie instantanée.</span><span class="sxs-lookup"><span data-stu-id="d7fe7-128">Your organization’s remote users and users at federated organizations will be able to see each other’s presence and communicate using IM.</span></span> <span data-ttu-id="d7fe7-129">Pour plus d’informations sur l’activation de la communication avec des utilisateurs externes, voir [planification de l’accès des utilisateurs externes dans Lync Server 2013](lync-server-2013-planning-for-external-user-access.md) dans la documentation de planification.</span><span class="sxs-lookup"><span data-stu-id="d7fe7-129">For details about enabling communication with external users, see [Planning for external user access in Lync Server 2013](lync-server-2013-planning-for-external-user-access.md) in the Planning documentation.</span></span>

</div>

<div>

## <a name="archiving-im-content"></a><span data-ttu-id="d7fe7-130">Archivage de contenu de messagerie instantanée</span><span class="sxs-lookup"><span data-stu-id="d7fe7-130">Archiving IM Content</span></span>

<span data-ttu-id="d7fe7-131">Lync Server fournit des fonctionnalités que vous pouvez utiliser si votre organisation doit respecter les règles de conformité.</span><span class="sxs-lookup"><span data-stu-id="d7fe7-131">Lync Server provides features you can use if your organization must follow compliance regulations.</span></span> <span data-ttu-id="d7fe7-132">Vous pouvez utiliser la fonctionnalité d’archivage pour archiver le contenu des messages instantanés soit pour tous les utilisateurs de votre organisation, soit uniquement pour ceux que vous indiquez.</span><span class="sxs-lookup"><span data-stu-id="d7fe7-132">You can use Archiving to archive the content of IM messages for all users in your organization or for only certain users that you specify.</span></span> <span data-ttu-id="d7fe7-133">Pour plus d’informations, reportez-vous à la rubrique [planification de l’archivage dans Lync Server 2013](lync-server-2013-planning-for-archiving.md) dans la documentation de planification.</span><span class="sxs-lookup"><span data-stu-id="d7fe7-133">For details, see [Planning for Archiving in Lync Server 2013](lync-server-2013-planning-for-archiving.md) in the Planning documentation.</span></span>

<span data-ttu-id="d7fe7-134">Si Microsoft Exchange Server 2013 est également déployé, vous pouvez intégrer l’archivage de données Exchange avec l’archivage des données de Lync Server et utiliser un seul outil pour effectuer une recherche dans les deux types de données archivées.</span><span class="sxs-lookup"><span data-stu-id="d7fe7-134">If you also have Microsoft Exchange Server 2013 deployed, you can integrate the archiving of Exchange data with the archiving of Lync Server data, and use a single tool to search both types of archived data.</span></span> <span data-ttu-id="d7fe7-135">Pour plus d’informations, reportez-vous [à configuration de Microsoft Lync server 2013 pour l’utilisation de l’archivage Microsoft Exchange Server 2013](configuring-lync-server-2013-to-use-microsoft-exchange-server-2013-archiving.md).</span><span class="sxs-lookup"><span data-stu-id="d7fe7-135">For more information, see [Configuring Microsoft Lync Server 2013 to use Microsoft Exchange Server 2013 archiving](configuring-lync-server-2013-to-use-microsoft-exchange-server-2013-archiving.md).</span></span>

<span data-ttu-id="d7fe7-136"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d7fe7-136"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

