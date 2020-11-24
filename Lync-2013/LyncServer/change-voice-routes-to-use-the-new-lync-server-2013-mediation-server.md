---
title: Changer les itinéraires vocaux pour utiliser le nouveau serveur de médiation Lync Server 2013
description: Changez les itinéraires vocaux pour utiliser le nouveau serveur de médiation Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Change voice routes to use the new Lync Server 2013 Mediation Server
ms:assetid: acd487b3-377c-46bf-9f71-fe6152002664
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205162(v=OCS.15)
ms:contentKeyID: 48185069
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ef58ba61512b5de31a74b79e554dbb3f94b67d99
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394249"
---
# <a name="change-voice-routes-to-use-the-new-lync-server-2013-mediation-server"></a><span data-ttu-id="89e79-103">Changer les itinéraires vocaux pour utiliser le nouveau serveur de médiation Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="89e79-103">Change voice routes to use the new Lync Server 2013 Mediation Server</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="89e79-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="89e79-104">

<span> </span></span></span>

<span data-ttu-id="89e79-105">_**Dernière modification de la rubrique :** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="89e79-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="89e79-106">Cette procédure modifie les itinéraires vocaux pour utiliser le serveur de médiation Lync Server 2013, au lieu du serveur de médiation traditionnel d’Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="89e79-106">This procedure changes the voice routes to use the Lync Server 2013 Mediation Server, instead of the legacy Office Communications Server 2007 R2 Mediation Server.</span></span>

<div>

## <a name="to-change-the-voice-routes-to-use-the-new-mediation-server"></a><span data-ttu-id="89e79-107">Pour modifier les itinéraires vocaux et utiliser le nouveau serveur de médiation</span><span class="sxs-lookup"><span data-stu-id="89e79-107">To change the voice routes to use the new Mediation Server</span></span>

1.  <span data-ttu-id="89e79-108">Panneau de configuration de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="89e79-108">Lync Server 2013 Control Panel</span></span>

2.  <span data-ttu-id="89e79-109">Dans le volet de gauche, sélectionnez routage de la **voix** , puis **route**.</span><span class="sxs-lookup"><span data-stu-id="89e79-109">In the left pane, select **Voice Routing** and then **Route**.</span></span>

3.  <span data-ttu-id="89e79-110">Cliquez sur **nouveau** pour créer un nouvel itinéraire.</span><span class="sxs-lookup"><span data-stu-id="89e79-110">Click **New** to create a New Voice Route.</span></span>

4.  <span data-ttu-id="89e79-111">Renseignez les champs suivants :</span><span class="sxs-lookup"><span data-stu-id="89e79-111">Fill in the following fields:</span></span>
    
      - <span data-ttu-id="89e79-112">**Nom**: tapez un nom descriptif pour l’itinéraire vocal.</span><span class="sxs-lookup"><span data-stu-id="89e79-112">**Name**: Type a descriptive name of the voice route.</span></span> <span data-ttu-id="89e79-113">Pour ce document, nous utiliserons **W15PSTNRoute**.</span><span class="sxs-lookup"><span data-stu-id="89e79-113">For this document we will use **W15PSTNRoute**.</span></span>
    
      - <span data-ttu-id="89e79-114">**Description**: tapez une brève description de l’itinéraire vocal.</span><span class="sxs-lookup"><span data-stu-id="89e79-114">**Description**: Type a short description of the voice route.</span></span>

5.  <span data-ttu-id="89e79-115">Ignorer toutes les sections restantes jusqu’à ce que vous atteigniez les **passerelles associées**.</span><span class="sxs-lookup"><span data-stu-id="89e79-115">Skip all remaining sections until you reach **Associated gateways**.</span></span> <span data-ttu-id="89e79-116">Cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="89e79-116">Click **Add**.</span></span> <span data-ttu-id="89e79-117">Sélectionnez la nouvelle passerelle par défaut, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="89e79-117">Select the new default gateway and click **OK**.</span></span>

6.  <span data-ttu-id="89e79-118">Dans **utilisations RTC associées**, cliquez sur **Sélectionner**.</span><span class="sxs-lookup"><span data-stu-id="89e79-118">Under **Associated PSTN Usages**, click **Select**.</span></span>

7.  <span data-ttu-id="89e79-119">Dans la page **Sélectionner un enregistrement d’utilisation RTC** , sélectionnez un nom d’enregistrement, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="89e79-119">From the **Select PSTN Usage Record** page, select a record name and then click **OK**.</span></span>

8.  <span data-ttu-id="89e79-120">Dans la page **nouvelle gamme vocale** , cliquez sur **OK** pour créer l' **itinéraire vocal**.</span><span class="sxs-lookup"><span data-stu-id="89e79-120">From the **New Voice Route** page, click **OK** to create the **Voice Route**.</span></span>

9.  <span data-ttu-id="89e79-121">Sur la page routage de la **voix** , sélectionnez **gamme**.</span><span class="sxs-lookup"><span data-stu-id="89e79-121">From the **Voice Routing** page, select **Route**.</span></span>

10. <span data-ttu-id="89e79-122">Déplacez l’itinéraire nouvellement créé vers le haut de la liste, puis sélectionnez **valider**.</span><span class="sxs-lookup"><span data-stu-id="89e79-122">Move the newly created route to the top of the list and then select **Commit**.</span></span>

<span data-ttu-id="89e79-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="89e79-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

