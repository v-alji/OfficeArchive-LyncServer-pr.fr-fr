---
title: 'Lync Server 2013 : Hébergement des utilisateurs sur un Survivable Branch Appliance ou un serveur Survivable Branch Server'
description: 'Lync Server 2013 : utilisateurs à domicile sur une unité ou un serveur de succursale Survivable.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Home users on a Survivable Branch Appliance or Server
ms:assetid: faf1ebb9-6d7d-4a58-8ff7-801b7b31d3ba
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413066(v=OCS.15)
ms:contentKeyID: 48185926
ms.date: 12/11/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 124eb7a51a8d5ff672d720fdad8956f682e29090
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427615"
---
# <a name="home-users-on-a-survivable-branch-appliance-or-server-in-lync-server-2013"></a><span data-ttu-id="9cbab-103">Hébergement des utilisateurs sur un Survivable Branch Appliance ou un serveur Survivable Branch Server dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9cbab-103">Home users on a Survivable Branch Appliance or Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9cbab-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9cbab-104">

<span> </span></span></span>

<span data-ttu-id="9cbab-105">_**Dernière modification de la rubrique :** 2014-12-10_</span><span class="sxs-lookup"><span data-stu-id="9cbab-105">_**Topic Last Modified:** 2014-12-10_</span></span>

<span data-ttu-id="9cbab-106">Le processus d’hébergement des utilisateurs sur une unité de branchement survivant ou un serveur de succursale survivant est similaire au processus d’hébergement des utilisateurs sur un pool frontal.</span><span class="sxs-lookup"><span data-stu-id="9cbab-106">The process of homing users on a Survivable Branch Appliance or a Survivable Branch Server is similar to the process of homing users on a Front End pool.</span></span> <span data-ttu-id="9cbab-107">Exécutez l’application branche Survivable ou le serveur de succursales survivant sur le site central.</span><span class="sxs-lookup"><span data-stu-id="9cbab-107">Perform the Survivable Branch Appliance or Survivable Branch Server procedure at the central site.</span></span>

<div>

## <a name="to-home-users-on-survivable-branch-appliance-or-survivable-branch-server"></a><span data-ttu-id="9cbab-108">Pour les particuliers sur un appareil de succursale survivant ou un serveur de succursales survivant</span><span class="sxs-lookup"><span data-stu-id="9cbab-108">To home users on Survivable Branch Appliance or Survivable Branch Server</span></span>

1.  <span data-ttu-id="9cbab-109">Avant de déplacer des utilisateurs vers un serveur de succursales ou un serveur de succursales survivant, ouvrez Lync Server Management Shell, puis effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="9cbab-109">Before moving users to the Survivable Branch Server or Survivable Branch Server, open the Lync Server Management Shell, and then do all of the following:</span></span>
    
      - <span data-ttu-id="9cbab-110">Exécutez l’applet de **contrôle test-CsPstnOutboundCall** pour vérifier que le serveur de succursales survivant est en cours d’exécution et que la connectivité PSTN (réseau téléphonique commuté) est configurée.</span><span class="sxs-lookup"><span data-stu-id="9cbab-110">Run the cmdlet **Test-CsPstnOutboundCall** to verify that the Survivable Branch Server is running and that the public switched telephone network (PSTN) connectivity is configured.</span></span> <span data-ttu-id="9cbab-111">Si vous devez modifier les propriétés de la passerelle RTC, utilisez la cmdlet **Set-CsPstnGateway**.</span><span class="sxs-lookup"><span data-stu-id="9cbab-111">If you need to modify PSTN gateway properties, use the cmdlet **Set-CsPstnGateway**.</span></span>
    
      - <span data-ttu-id="9cbab-112">Exécutez l’applet de contrôle **Get-CsVoicePolicy** pour vérifier que les utilisateurs qui sont hébergés sur le serveur de succursales survivables disposent de la stratégie de routage de VoIP appropriée.</span><span class="sxs-lookup"><span data-stu-id="9cbab-112">Run the cmdlet **Get-CsVoicePolicy** to verify that the users who will be homed on the Survivable Branch Server have the appropriate VoIP routing policy.</span></span> <span data-ttu-id="9cbab-113">Si vous avez besoin de modifier la stratégie VoIP, utilisez la cmdlet **Set-CsVoicePolicy**.</span><span class="sxs-lookup"><span data-stu-id="9cbab-113">If you need to modify the VoIP policy, use the cmdlet **Set-CsVoicePolicy**.</span></span>
    
      - <span data-ttu-id="9cbab-114">Exécutez l’applet de contrôle **Get-CsVoicemailReroutingConfiguration** pour vérifier que les paramètres de reroutage de la messagerie vocale sont configurés.</span><span class="sxs-lookup"><span data-stu-id="9cbab-114">Run the cmdlet **Get-CsVoicemailReroutingConfiguration** to verify that the voice mail rerouting settings are configured.</span></span> <span data-ttu-id="9cbab-115">Si vous devez modifier les paramètres de redirection de la messagerie vocale, utilisez la cmdlet **Set-CsVoicemailReroutingConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="9cbab-115">If you need to modify the voice mail rerouting settings, use the cmdlet **Set-CsVoicemailReroutingConfiguration**.</span></span>

2.  <span data-ttu-id="9cbab-116">Dans Lync Server Management Shell, exécutez l’applet de l’applet de **Csuser** pour déplacer les utilisateurs de l’accueil.</span><span class="sxs-lookup"><span data-stu-id="9cbab-116">In the Lync Server Management Shell, run the cmdlet **Move-CsUser** to move home users.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="9cbab-117">Vous pouvez également utiliser le panneau de configuration de Lync Server pour vérifier les prérequis et les particuliers.</span><span class="sxs-lookup"><span data-stu-id="9cbab-117">You can also use Lync Server Control Panel to verify prerequisites and home users.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="9cbab-118">Les utilisateurs qui sont hébergés sur une unité de branchement Survivable Lync Server ne peuvent pas créer de nouvelles salles de conversation ou afficher la carte de la salle pour les salles existantes.</span><span class="sxs-lookup"><span data-stu-id="9cbab-118">Users who are homed on a Lync Server Survivable Branch Appliance are unable to create new chat rooms or view the room card for existing rooms.</span></span>



</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="9cbab-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9cbab-119">See Also</span></span>


[<span data-ttu-id="9cbab-120">Test-CsPstnOutboundCall</span><span class="sxs-lookup"><span data-stu-id="9cbab-120">Test-CsPstnOutboundCall</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsPstnOutboundCall)  
[<span data-ttu-id="9cbab-121">Get-CsVoicePolicy</span><span class="sxs-lookup"><span data-stu-id="9cbab-121">Get-CsVoicePolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsVoicePolicy)  
[<span data-ttu-id="9cbab-122">Get-CsVoicemailReroutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="9cbab-122">Get-CsVoicemailReroutingConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsVoicemailReroutingConfiguration)  
[<span data-ttu-id="9cbab-123">Move-CsUser</span><span class="sxs-lookup"><span data-stu-id="9cbab-123">Move-CsUser</span></span>](https://docs.microsoft.com/powershell/module/skype/Move-CsUser)  
  

<span data-ttu-id="9cbab-124"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9cbab-124"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

