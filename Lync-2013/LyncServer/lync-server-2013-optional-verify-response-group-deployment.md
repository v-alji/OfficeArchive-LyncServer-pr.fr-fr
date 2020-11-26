---
title: 'Lync Server 2013 : (facultatif) vérifier le déploiement de Response Group'
description: 'Lync Server 2013 : (facultatif) Vérifiez le déploiement de Response Group.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: (Optional) Verify Response Group deployment
ms:assetid: 202ca4ab-8e6d-44a4-b7c8-071133074feb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687989(v=OCS.15)
ms:contentKeyID: 49733579
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0cfe15026bc1fcfbe10b593987d2717fc0dc8104
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424848"
---
# <a name="optional-verify-response-group-deployment-in-lync-server-2013"></a><span data-ttu-id="a340f-103">Facultatif Vérifier le déploiement de Response Group dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a340f-103">(Optional) Verify Response Group deployment in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a340f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a340f-104">

<span> </span></span></span>

<span data-ttu-id="a340f-105">_**Dernière modification de la rubrique :** 2012-09-11_</span><span class="sxs-lookup"><span data-stu-id="a340f-105">_**Topic Last Modified:** 2012-09-11_</span></span>

<span data-ttu-id="a340f-106">Après avoir configuré Response Group, vous devez vérifier la configuration pour vous assurer que les groupes de réponse fonctionnent comme prévu.</span><span class="sxs-lookup"><span data-stu-id="a340f-106">After you configure Response Group, you need to verify the configuration to make sure your response groups work as expected.</span></span> <span data-ttu-id="a340f-107">Au minimum, vérifiez les scénarios ci-dessous en vous basant sur les types d’utilisateur indiqués ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="a340f-107">At minimum, verify the following scenarios by using the following types of users:</span></span>

<span data-ttu-id="a340f-108">**Utilisateurs**</span><span class="sxs-lookup"><span data-stu-id="a340f-108">**Users**</span></span>

  - <span data-ttu-id="a340f-109">Utilisateur hébergé sur Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a340f-109">A user who is homed on Lync Server 2013</span></span>

  - <span data-ttu-id="a340f-110">Utilisateur externe utilisant le réseau téléphonique commuté (RTC)</span><span class="sxs-lookup"><span data-stu-id="a340f-110">An external user who uses the public switched telephone network (PSTN)</span></span>

  - <span data-ttu-id="a340f-111">Agent hébergé sur Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a340f-111">An agent who is homed on Lync Server 2013</span></span>

<span data-ttu-id="a340f-112">**Scénarios**</span><span class="sxs-lookup"><span data-stu-id="a340f-112">**Scenarios**</span></span>

  - <span data-ttu-id="a340f-113">L’utilisateur de Lync Server 2013 appelle le groupe de réponse.</span><span class="sxs-lookup"><span data-stu-id="a340f-113">The Lync Server 2013 user calls the response group.</span></span>

  - <span data-ttu-id="a340f-114">L’utilisateur externe appelle le service Response Group.</span><span class="sxs-lookup"><span data-stu-id="a340f-114">The external user calls the response group.</span></span>

  - <span data-ttu-id="a340f-115">Un utilisateur appelle le service Response Group pendant que l’agent traite un autre appel. L’appel de l’utilisateur est alors transmis à la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="a340f-115">A user calls the response group while the agent is on another call and goes to the queue.</span></span>

<span data-ttu-id="a340f-116"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a340f-116"></div>

<span> </span>

</div>

</div>

</span></span></div>

