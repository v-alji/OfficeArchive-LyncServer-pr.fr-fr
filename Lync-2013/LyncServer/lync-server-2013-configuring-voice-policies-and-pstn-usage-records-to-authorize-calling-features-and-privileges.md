---
title: 'Lync Server 2013 : Configuration des stratégies de voix et des enregistrements d’utilisation RTC pour autoriser les fonctionnalités d’appel et les privilèges dans Lync Server 2013'
description: 'Lync Server 2013 : configuration de stratégies vocales et d’enregistrements d’utilisation RTC pour autoriser les fonctionnalités d’appel et les privilèges.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring voice policies and PSTN usage records to authorize calling features and privileges
ms:assetid: 63f22010-a3d7-4cbd-86e8-6fc0e13c2b84
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398450(v=OCS.15)
ms:contentKeyID: 48184307
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a12c9c64c3f02effba7c7709321eda91350ebb75
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432393"
---
# <a name="configuring-voice-policies-and-pstn-usage-records-to-authorize-calling-features-and-privileges-in-lync-server-2013"></a><span data-ttu-id="3f333-103">Configuration des stratégies de voix et des enregistrements d’utilisation RTC pour autoriser les fonctionnalités d’appel et les privilèges dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3f333-103">Configuring voice policies and PSTN usage records to authorize calling features and privileges in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3f333-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3f333-104">

<span> </span></span></span>

<span data-ttu-id="3f333-105">_**Dernière modification de la rubrique :** 2012-10-10_</span><span class="sxs-lookup"><span data-stu-id="3f333-105">_**Topic Last Modified:** 2012-10-10_</span></span>

<span data-ttu-id="3f333-106">Une *stratégie vocale* active un ensemble de fonctionnalités d’appel et associe un ou plusieurs enregistrements d’utilisation RTC pour définir les fonctionnalités d’appel et les autorisations des utilisateurs auxquels la stratégie est affectée.</span><span class="sxs-lookup"><span data-stu-id="3f333-106">A *voice policy* enables a set of calling features and associates one or more PSTN usage records to define the calling features and permissions of users who are assigned the policy.</span></span>

<span data-ttu-id="3f333-107">L’étendue de la stratégie vocale peut être un *site* (qui définit les fonctionnalités et les autorisations par défaut pour un site réseau) ou un *utilisateur* (qui définit les fonctionnalités et les autorisations à attribuer pour chaque utilisateur ou groupe).</span><span class="sxs-lookup"><span data-stu-id="3f333-107">Voice policy scope can be either *Site* (which defines the default features and permissions for a network site) or *User* (which defines the features and permissions to be assigned on a per-user or group basis).</span></span> <span data-ttu-id="3f333-108">Les utilisateurs non assignés à une stratégie vocale sont automatiquement affectés à la stratégie globale, qui est la stratégie vocale par défaut installée avec le produit.</span><span class="sxs-lookup"><span data-stu-id="3f333-108">Users not assigned to a voice policy will automatically be assigned to the global policy, which is the default voice policy that is installed with the product.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="3f333-109">Pour plus d’informations, reportez-vous à <A href="lync-server-2013-voice-policies.md">stratégies vocales dans Lync Server 2013</A> dans la documentation de planification.</span><span class="sxs-lookup"><span data-stu-id="3f333-109">For details, see <A href="lync-server-2013-voice-policies.md">Voice policies in Lync Server 2013</A> in the Planning documentation.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="3f333-110">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="3f333-110">In This Section</span></span>

  - [<span data-ttu-id="3f333-111">Créer une stratégie de voix et configurer les enregistrements d’utilisation RTC dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3f333-111">Create a voice policy and configure PSTN usage records in Lync Server 2013</span></span>](lync-server-2013-create-a-voice-policy-and-configure-pstn-usage-records.md)

  - [<span data-ttu-id="3f333-112">Modifier une stratégie vocale et configurer les enregistrements d’utilisation RTC dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3f333-112">Modify a voice policy and configure PSTN usage records in Lync Server 2013</span></span>](lync-server-2013-modify-a-voice-policy-and-configure-pstn-usage-records.md)

  - [<span data-ttu-id="3f333-113">Configuration de l’échappement de la messagerie vocale dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3f333-113">Configuring voice mail escape in Lync Server 2013</span></span>](lync-server-2013-configuring-voice-mail-escape.md)

<span data-ttu-id="3f333-114"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3f333-114"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

