---
title: 'Lync Server 2013 : Mise à disposition de la messagerie vocale Lync Server aux utilisateurs sur la messagerie unifiée Exchange'
description: 'Lync Server 2013 : fourniture de messages vocaux aux utilisateurs de Lync Server sur la messagerie unifiée Exchange hébergée.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Providing Lync Server 2013 users voice mail on hosted Exchange UM
ms:assetid: 306d3fb5-231b-4f0b-b8d8-0d9083b5ed77
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425807(v=OCS.15)
ms:contentKeyID: 48183752
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: be4048e7fc2bd30a4ab670259a1871bd1b59483a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436831"
---
# <a name="providing-lync-server-2013-users-voice-mail-on-hosted-exchange-um"></a><span data-ttu-id="c8b1d-103">Mise à disposition de la messagerie vocale Lync Server 2013 aux utilisateurs sur la messagerie unifiée Exchange hébergée</span><span class="sxs-lookup"><span data-stu-id="c8b1d-103">Providing Lync Server 2013 users voice mail on hosted Exchange UM</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c8b1d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c8b1d-104">

<span> </span></span></span>

<span data-ttu-id="c8b1d-105">_**Dernière modification de la rubrique :** 2012-09-24_</span><span class="sxs-lookup"><span data-stu-id="c8b1d-105">_**Topic Last Modified:** 2012-09-24_</span></span>

<span data-ttu-id="c8b1d-106">Cette section vous guide tout au long du processus de fourniture d’utilisateurs dans un déploiement Lync Server 2013 local avec la messagerie vocale sur un service de messagerie unifiée Exchange hébergé.</span><span class="sxs-lookup"><span data-stu-id="c8b1d-106">This section guides you through the process of providing users in an on-premises Lync Server 2013 deployment with voice mail on a hosted Exchange Unified Messaging (UM) service.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="c8b1d-107">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="c8b1d-107">In This Section</span></span>

  - [<span data-ttu-id="c8b1d-108">Création d’un enregistrement SRV DNS pour l’intégrer à la messagerie unifiée Exchange hébergée</span><span class="sxs-lookup"><span data-stu-id="c8b1d-108">Create a DNS SRV record for integration with hosted Exchange UM</span></span>](lync-server-2013-create-a-dns-srv-record-for-integration-with-hosted-exchange-um.md)

  - [<span data-ttu-id="c8b1d-109">Configuration du serveur Edge pour l’intégration à la messagerie unifiée Exchange hébergée</span><span class="sxs-lookup"><span data-stu-id="c8b1d-109">Configure the Edge Server for integration with hosted Exchange UM</span></span>](lync-server-2013-configure-the-edge-server-for-integration-with-hosted-exchange-um.md)

  - [<span data-ttu-id="c8b1d-110">Gestion des stratégies de messagerie vocale hébergée dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c8b1d-110">Manage hosted voice mail policies in Lync Server 2013</span></span>](lync-server-2013-manage-hosted-voice-mail-policies.md)

  - [<span data-ttu-id="c8b1d-111">Activation des utilisateurs pour la messagerie vocale hébergée dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c8b1d-111">Enable users for hosted voice mail in Lync Server 2013</span></span>](lync-server-2013-enable-users-for-hosted-voice-mail.md)

  - [<span data-ttu-id="c8b1d-112">Création des objets de contact pour la messagerie unifiée Exchange hébergée dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c8b1d-112">Create contact objects for hosted Exchange UM in Lync Server 2013</span></span>](lync-server-2013-create-contact-objects-for-hosted-exchange-um.md)

<span data-ttu-id="c8b1d-113"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c8b1d-113"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

