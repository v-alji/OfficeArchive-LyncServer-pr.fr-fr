---
title: 'Lync Server 2013 : Test du routage des communications vocales'
description: 'Lync Server 2013 : test de routage de la voix.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test voice routing
ms:assetid: d3aae909-fef6-440f-b144-0b62dc82bf5d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398915(v=OCS.15)
ms:contentKeyID: 48185444
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e641e68ccecfe7d1d0e64dc9eb1b1f5016e68e22
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441150"
---
# <a name="test-voice-routing-in-lync-server-2013"></a><span data-ttu-id="43590-103">Test du routage des communications vocales dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="43590-103">Test voice routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="43590-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="43590-104">

<span> </span></span></span>

<span data-ttu-id="43590-105">_**Dernière modification de la rubrique :** 2013-02-24_</span><span class="sxs-lookup"><span data-stu-id="43590-105">_**Topic Last Modified:** 2013-02-24_</span></span>

<span data-ttu-id="43590-106">Pour configurer des scénarios de cas de test, vous pouvez utiliser l’onglet **test** du panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="43590-106">You can use the Lync Server Control Panel **Test Voice Routing** tab to configure test case scenarios.</span></span> <span data-ttu-id="43590-107">Pour définir un cas de test, vous spécifiez le plan de numérotation, la stratégie vocale, l’utilisation RTC et l’itinéraire vocal sur lequel tester un numéro de téléphone spécifié.</span><span class="sxs-lookup"><span data-stu-id="43590-107">To define a test case, you specify the dial plan, voice policy, PSTN usage, and voice route against which to test a specified phone number.</span></span>

<span data-ttu-id="43590-108">Avant de déployer votre configuration de routage vocale, nous vous recommandons de la tester sur les différents numéros de téléphone pour vérifier que les résultats sont bien attendus.</span><span class="sxs-lookup"><span data-stu-id="43590-108">Before you actually deploy your voice routing configuration, we recommend that you test it on various phone numbers to make sure that the results are what you're expecting.</span></span>

<div>


> [!TIP]  
> <span data-ttu-id="43590-109">Vous pouvez utiliser les commandes d’exportation de cas de <STRONG>test</STRONG> et d' <STRONG>importation de cas de test</STRONG> pour enregistrer les cas de tests de routage de voix et les importer pour les utiliser sur un autre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="43590-109">You can use the <STRONG>Export test cases</STRONG> and <STRONG>Import test cases</STRONG> commands to save voice routing test cases and import them for use on another computer.</span></span>



</div>

<div>


> [!WARNING]  
> <span data-ttu-id="43590-110">Si vous supprimez une partie quelconque de votre configuration de routage, par exemple un plan de numérotation, une stratégie vocale, un itinéraire vocal ou une utilisation du téléphone, vous devez passer en revue et mettre à jour les cas de test de votre gamme vocale.</span><span class="sxs-lookup"><span data-stu-id="43590-110">If you delete any part of your voice routing configuration, such as a dial plan, voice policy, voice route, or phone usage, you should review and update your voice routing test cases.</span></span> <span data-ttu-id="43590-111">Le panneau de configuration de Lync Server ne vous alerte pas pour les cas de tests qui ne sont plus valides en raison de configurations modifiées.</span><span class="sxs-lookup"><span data-stu-id="43590-111">The Lync Server Control Panel will not alert you to test cases that are no longer valid due to changed configurations.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="43590-112">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="43590-112">In This Section</span></span>

  - [<span data-ttu-id="43590-113">Création d’un cas de test de routage des communications vocales dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="43590-113">Create a voice routing test case in Lync Server 2013</span></span>](lync-server-2013-create-a-voice-routing-test-case.md)

  - [<span data-ttu-id="43590-114">Exportation des cas de test de routage des communications vocales dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="43590-114">Export voice routing test cases in Lync Server 2013</span></span>](lync-server-2013-export-voice-routing-test-cases.md)

  - [<span data-ttu-id="43590-115">Importation des cas de test de routage des communications vocales dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="43590-115">Import voice routing test cases in Lync Server 2013</span></span>](lync-server-2013-import-voice-routing-test-cases.md)

  - [<span data-ttu-id="43590-116">Exécution des tests de routage des communications vocales dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="43590-116">Running voice routing tests in Lync Server 2013</span></span>](lync-server-2013-running-voice-routing-tests.md)

<span data-ttu-id="43590-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="43590-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

