---
title: 'Lync Server 2013 : Fonctionnalités de serveurs frontaux, de messagerie instantanée et de présence'
description: 'Lync Server 2013 : fonctionnalités et fonctionnalités des serveurs front-end, de la messagerie instantanée et de la présence.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Features and functionality of Front End Servers, instant messaging, and presence
ms:assetid: 05b29536-dcd7-49b5-934a-2ebf20ddc45c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398109(v=OCS.15)
ms:contentKeyID: 48183294
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b5c8bc3db255228da3366eb5aa142cd5adc233d1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49393977"
---
# <a name="features-and-functionality-of-front-end-servers-instant-messaging-and-presence-in-lync-server-2013"></a><span data-ttu-id="4c01a-103">Fonctionnalités de serveurs frontaux, de messagerie instantanée et de présence dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4c01a-103">Features and functionality of Front End Servers, instant messaging, and presence in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4c01a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4c01a-104">

<span> </span></span></span>

<span data-ttu-id="4c01a-105">_**Dernière modification de la rubrique :** 2013-03-17_</span><span class="sxs-lookup"><span data-stu-id="4c01a-105">_**Topic Last Modified:** 2013-03-17_</span></span>

<span data-ttu-id="4c01a-106">Les serveurs front-end fournissent la plupart des fonctionnalités de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="4c01a-106">Front End Servers provide most Lync Server functionality.</span></span> <span data-ttu-id="4c01a-107">Il existe deux éditions disponibles : Lync Server Enterprise Edition, principalement conçu pour les grandes organisations et Lync Server Standard Edition, conçu essentiellement pour les petites organisations qui ont besoin d’un investissement plus petit sur le matériel et ne nécessitent pas une disponibilité élevée.</span><span class="sxs-lookup"><span data-stu-id="4c01a-107">There are two editions available: Lync Server Enterprise Edition, which is designed primarily for larger organizations, and Lync Server Standard Edition, which is designed primarily for smaller organizations which want a smaller hardware investement and do not require high availability.</span></span> <span data-ttu-id="4c01a-108">Les deux éditions prennent en charge toutes les charges de travail du serveur Lync, notamment la messagerie instantanée, la présence, les conférences et l’voix entreprise.</span><span class="sxs-lookup"><span data-stu-id="4c01a-108">Both editions support all Lync Server workloads including IM, presence, conferencing, and Enterprise Voice.</span></span>

<span data-ttu-id="4c01a-109">La messagerie instantanée permet aux utilisateurs de communiquer en temps réel les uns avec les autres sur leurs ordinateurs à l’aide des messages textuels.</span><span class="sxs-lookup"><span data-stu-id="4c01a-109">Instant messaging (IM) enables your users to communicate with each other in real time on their computers using text-based messages.</span></span> <span data-ttu-id="4c01a-110">Les sessions de messagerie unifiée à deux ou à plusieurs personnes sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="4c01a-110">Both two-party and multiparty IM sessions are supported.</span></span> <span data-ttu-id="4c01a-111">Un participant à une conversation de messagerie instantanée peut ajouter un troisième participant à la conversation à tout moment.</span><span class="sxs-lookup"><span data-stu-id="4c01a-111">A participant in a two-party IM conversation can add a third participant to the conversation at any time.</span></span> <span data-ttu-id="4c01a-112">Lorsque cela arrive, la fenêtre Conversation change pour prendre en charge des fonctionnalités de conférence.</span><span class="sxs-lookup"><span data-stu-id="4c01a-112">When this happens, the Conversation window changes to support conferencing features.</span></span>

<div>


> [!IMPORTANT]
> <span data-ttu-id="4c01a-113">Les clients Lync et Communicator intervenant dans le cadre d’une communication une à une, sont souvent désignés sous le nom d’égal à égal.</span><span class="sxs-lookup"><span data-stu-id="4c01a-113">Lync and Communicator clients when involved in a one to one communication, is often referred to as peer-to-peer.</span></span> <span data-ttu-id="4c01a-114">Techniquement, les deux clients communiquent en une seule conversation avec l’unité de contrôle multipoint (IMMCU) de messagerie instantanée au milieu.</span><span class="sxs-lookup"><span data-stu-id="4c01a-114">Technically, the two clients are communicating in a one to one conversation, with the Instant Messaging multipoint control unit (IMMCU) in the middle.</span></span> <span data-ttu-id="4c01a-115">IMMCU est un composant du serveur frontal.</span><span class="sxs-lookup"><span data-stu-id="4c01a-115">The IMMCU is a component of Front End Server.</span></span> <span data-ttu-id="4c01a-116">Le placement du IMMCU dans le flux de travail de communication requis autorise l’enregistrement des détails des appels et d’autres fonctionnalités que le serveur frontal autorise.</span><span class="sxs-lookup"><span data-stu-id="4c01a-116">Placing the IMMCU in the required communication workflow allows call detail recording and other features that the Front End Server enables.</span></span> <span data-ttu-id="4c01a-117">La communication provient d’un port source dynamique du client vers le port de serveur frontal TLS/TCP/5061 (en partant du principe que l’utilisation de la sécurité de couche de transport recommandée).</span><span class="sxs-lookup"><span data-stu-id="4c01a-117">Communication is from a dynamic source port on the client to the Front End Server port TLS/TCP/5061 (assuming the use of the recommended transport layer security).</span></span> <span data-ttu-id="4c01a-118">Par conception, la communication d’égal à égal (et la messagerie instantanée à plusieurs parties) est possible uniquement lorsque Lync Server et IMMCU est actif et disponible.</span><span class="sxs-lookup"><span data-stu-id="4c01a-118">By design, peer-to-peer communication (as well as multi-party IM) is possible only when Lync Server and the IMMCU is active and available.</span></span>



</div>

<span data-ttu-id="4c01a-119">La *présence* fournit des informations aux utilisateurs sur l’état d’autres personnes sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="4c01a-119">*Presence* provides information to users about the status of other on the network.</span></span> <span data-ttu-id="4c01a-120">Le statut de présence d’un utilisateur fournit des informations pour permettre aux autres utilisateurs de décider s’ils doivent essayer de contacter l’utilisateur et s’ils doivent pour cela utiliser la messagerie instantanée, le téléphone ou la messagerie électronique.</span><span class="sxs-lookup"><span data-stu-id="4c01a-120">A user’s presence status provides information to help others decide whether they should try to contact the user and whether to use instant messaging, phone, or email.</span></span> <span data-ttu-id="4c01a-121">La présence permet une communication instantanée lorsque cela est possible, mais fournit aussi des informations indiquant si un utilisateur est en réunion ou hors du bureau, indiquant que la communication instantanée n’est pas possible.</span><span class="sxs-lookup"><span data-stu-id="4c01a-121">Presence encourages instant communication when possible, but it also provides information about whether a user is in a meeting or out of the office, indicating that instant communication is not possible.</span></span> <span data-ttu-id="4c01a-122">Ce statut de présence est affiché en tant qu’icône de présence dans Lync et d’autres applications prenant en charge la fonctionnalité de présence, dont le client de messagerie et de collaboration Microsoft Outlook, le logiciel Microsoft SharePoint technologies, Microsoft Word et la feuille de calcul Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="4c01a-122">This presence status is displayed as a presence icon in Lync and other presence-aware applications, including the Microsoft Outlook messaging and collaboration client, Microsoft SharePoint technologies, Microsoft Word, and Microsoft Excel spreadsheet software.</span></span> <span data-ttu-id="4c01a-123">L’icône de présence indique la disponibilité actuelle de l’utilisateur et sa volonté à communiquer.</span><span class="sxs-lookup"><span data-stu-id="4c01a-123">The presence icon represents the user’s current availability and willingness to communicate.</span></span>

<span data-ttu-id="4c01a-124"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4c01a-124"></div>

<span> </span>

</div>

</div>

</span></span></div>

