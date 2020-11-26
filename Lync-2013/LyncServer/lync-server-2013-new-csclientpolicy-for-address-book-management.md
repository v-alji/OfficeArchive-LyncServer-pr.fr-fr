---
title: 'Lync Server 2013 : New-CsClientPolicy pour la gestion du carnet d’adresses'
description: 'Lync Server 2013 : New-CsClientPolicy pour la gestion du carnet d’adresses.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: New-CsClientPolicy for Address Book management
ms:assetid: ef4415fc-82c4-4dc8-97d1-37a084553343
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429726(v=OCS.15)
ms:contentKeyID: 48185771
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 12c14534c7af447f30a01b1bbbd1679a8375c705
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425109"
---
# <a name="new-csclientpolicy-for-address-book-management-in-lync-server-2013"></a><span data-ttu-id="31caf-103">New-CsClientPolicy la gestion du carnet d’adresses dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="31caf-103">New-CsClientPolicy for Address Book management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="31caf-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="31caf-104">

<span> </span></span></span>

<span data-ttu-id="31caf-105">_**Dernière modification de la rubrique :** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="31caf-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="31caf-106">Qui peut exécuter cette applet de commande : par défaut, les membres des groupes suivants sont autorisés à exécuter l’applet de commande New-CsClientPolicy : RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="31caf-106">Who can run this cmdlet: By default, members of the following groups are authorized to run the New-CsClientPolicy cmdlet: RTCUniversalServerAdmins.</span></span> <span data-ttu-id="31caf-107">Pour renvoyer la liste de tous les rôles de contrôle d’accès basés sur des rôles (RBAC) affectés à cette applet de commande (y compris les rôles RBAC personnalisés que vous avez créés vous-même), exécutez la commande suivante à partir de l’invite Windows PowerShell :</span><span class="sxs-lookup"><span data-stu-id="31caf-107">To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself), run the following command from the Windows PowerShell prompt:</span></span>

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "New-CsClientPolicy"}

<span data-ttu-id="31caf-108">L’applet de New-CsClientPolicy définit un grand nombre de paramètres pour les clients de mise en service pour les fonctionnalités disponibles dans Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="31caf-108">The cmdlet New-CsClientPolicy defines a large number of settings for provisioning clients for features that are available in Lync Server 2013.</span></span> <span data-ttu-id="31caf-109">Pour le service de carnet d’adresses, le paramètre AddressBookAvailability est intéressant.</span><span class="sxs-lookup"><span data-stu-id="31caf-109">For the Address Book Service, the parameter AddressBookAvailability is of interest.</span></span> <span data-ttu-id="31caf-110">Ce paramètre a un impact direct sur les options disponibles pour les clients et propose trois options possibles :</span><span class="sxs-lookup"><span data-stu-id="31caf-110">This parameter, which directly impacts the options available to clients, has three possible options:</span></span>

  - <span data-ttu-id="31caf-111">WebSearchAndFileDownload</span><span class="sxs-lookup"><span data-stu-id="31caf-111">WebSearchAndFileDownload</span></span>

  - <span data-ttu-id="31caf-112">WebSearchOnly</span><span class="sxs-lookup"><span data-stu-id="31caf-112">WebSearchOnly</span></span>

  - <span data-ttu-id="31caf-113">FileDownloadOnly</span><span class="sxs-lookup"><span data-stu-id="31caf-113">FileDownloadOnly</span></span>

<span data-ttu-id="31caf-114">Détermine la manière dont les clients peuvent accéder au carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="31caf-114">When defined, it determines how the Address Book is accessed by clients.</span></span> <span data-ttu-id="31caf-115">Si vous définissez ce paramètre, vous devez définir une des options.</span><span class="sxs-lookup"><span data-stu-id="31caf-115">If you define this parameter, you must define one of the options.</span></span> <span data-ttu-id="31caf-116">Si vous ne modifiez pas ce paramètre, le WebSearchAndFileDownload par défaut reste en vigueur.</span><span class="sxs-lookup"><span data-stu-id="31caf-116">If you do not modify this setting, the default WebSearchAndFileDownload remains in effect.</span></span>

<span data-ttu-id="31caf-117">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="31caf-117">For example:</span></span>

    New-CsClientPolicy -Identity RedmondClientPolicy -DisableCalendarPresence $True -DisablePhonePresence $True -DisplayPhoto "PhotosFromADOnly" -AddressBookAvailability "WebSearchOnly"

<div>

## <a name="see-also"></a><span data-ttu-id="31caf-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="31caf-118">See Also</span></span>


[<span data-ttu-id="31caf-119">Nouveau-CsClientPolicy</span><span class="sxs-lookup"><span data-stu-id="31caf-119">New-CsClientPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsClientPolicy)  
  

<span data-ttu-id="31caf-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="31caf-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

