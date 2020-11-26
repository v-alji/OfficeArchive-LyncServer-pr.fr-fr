---
title: 'Lync Server 2013 : Gestion des partenaires fédérés XMPP pour l’organisation'
description: 'Lync Server 2013 : gestion des partenaires fédérés de XMPP pour votre organisation.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Manage XMPP federated partners for your organization
ms:assetid: 48681433-725d-457f-926b-f91d95bcf082
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ552450(v=OCS.15)
ms:contentKeyID: 48679561
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 37d6fb4104c35ffc7db9649656f7786568a48b61
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426024"
---
# <a name="manage-xmpp-federated-partners-in-lync-server-2013"></a><span data-ttu-id="0a087-103">Gestion des partenaires fédérés XMPP dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0a087-103">Manage XMPP federated partners in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0a087-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0a087-104">

<span> </span></span></span>

<span data-ttu-id="0a087-105">_**Dernière modification de la rubrique :** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="0a087-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="0a087-106">Il s’agit d’une documentation préliminaire susceptible d’être modifiée.</span><span class="sxs-lookup"><span data-stu-id="0a087-106">This is preliminary documentation and is subject to change.</span></span> <span data-ttu-id="0a087-107">Des rubriques vides sont incluses sous forme d’espaces réservés.</span><span class="sxs-lookup"><span data-stu-id="0a087-107">Blank topics are included as placeholders.</span></span>

<span data-ttu-id="0a087-108">Pour gérer la prise en charge des utilisateurs de domaines fédérés XMPP, vous devez effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="0a087-108">To manage support for users of XMPP federated domains, you need to do the following:</span></span>

  - <span data-ttu-id="0a087-109">Configurez une ou plusieurs stratégies d’accès externe pour la prise en charge des utilisateurs des domaines fédérés XMPP.</span><span class="sxs-lookup"><span data-stu-id="0a087-109">Configure one or more external access policies to support users of XMPP federated domains.</span></span>

  - <span data-ttu-id="0a087-110">Configurer une stratégie de configuration de Microsoft Edge pour prendre en charge la Fédération.</span><span class="sxs-lookup"><span data-stu-id="0a087-110">Configure Access Edge Configuration policy to support federation.</span></span>

  - <span data-ttu-id="0a087-111">Créer des définitions de partenaires fédérés de XMPP.</span><span class="sxs-lookup"><span data-stu-id="0a087-111">Create XMPP Federated Partners definitions.</span></span>

  - <span data-ttu-id="0a087-112">Comprendre les paramètres de négociation disponibles pour la Fédération XMPP.</span><span class="sxs-lookup"><span data-stu-id="0a087-112">Understand negotiation settings available for XMPP federation.</span></span>

<span data-ttu-id="0a087-113">Pour effectuer ces tâches, suivez les procédures décrites dans cette section.</span><span class="sxs-lookup"><span data-stu-id="0a087-113">To perform these tasks, use the procedures in this section.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="0a087-114">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="0a087-114">In This Section</span></span>

  - [<span data-ttu-id="0a087-115">Créer ou modifier une configuration de partenaire XMPP dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0a087-115">Create or edit XMPP partner configuration in Lync Server 2013</span></span>](lync-server-2013-create-or-edit-xmpp-partner-configuration.md)

  - [<span data-ttu-id="0a087-116">Paramètres de négociation pour les partenaires fédérés XMPP dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0a087-116">Negotiation settings for XMPP federated partners in Lync Server 2013</span></span>](lync-server-2013-negotiation-settings-for-xmpp-federated-partners.md)

  - [<span data-ttu-id="0a087-117">Exemple de configuration XMPP dans Lync Server 2013 – Fédération XMPP avec Google Talk</span><span class="sxs-lookup"><span data-stu-id="0a087-117">Example XMPP configuration in Lync Server 2013 – XMPP federation with Google Talk</span></span>](lync-server-2013-example-xmpp-configuration-–-xmpp-federation-with-google-talk.md)

<span data-ttu-id="0a087-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0a087-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

