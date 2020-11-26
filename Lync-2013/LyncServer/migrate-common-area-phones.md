---
title: Migration des téléphones de partie commune
description: Migration des téléphones de surface communs.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migrate Common Area Phones
ms:assetid: 31bd26fc-861b-45c6-8221-18df16e575de
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688015(v=OCS.15)
ms:contentKeyID: 49733604
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1b8df4d94a3db3274df7e4e82ed2185c3626de12
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443824"
---
# <a name="migrate-common-area-phones"></a><span data-ttu-id="e14ef-103">Migration des téléphones de partie commune</span><span class="sxs-lookup"><span data-stu-id="e14ef-103">Migrate Common Area Phones</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e14ef-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e14ef-104">

<span> </span></span></span>

<span data-ttu-id="e14ef-105">_**Dernière modification de la rubrique :** 2012-09-29_</span><span class="sxs-lookup"><span data-stu-id="e14ef-105">_**Topic Last Modified:** 2012-09-29_</span></span>

<span data-ttu-id="e14ef-106">Les téléphones portables courants sont les téléphones IP qui se trouvent le plus souvent dans un espace de travail partagé ou une zone commune (par exemple, salle d’attente, cuisine ou étage d’usine).</span><span class="sxs-lookup"><span data-stu-id="e14ef-106">Common Area Phones are IP phones that most often reside in a shared workspace or common area, like a lobby, kitchen, or factory floor.</span></span> <span data-ttu-id="e14ef-107">Il n’est pas nécessaire de connecter des téléphones communs à un ordinateur pour fournir une fonctionnalité de communications unifiées Lync Server.</span><span class="sxs-lookup"><span data-stu-id="e14ef-107">Common Area Phones do not need to be connected to a computer to provide Lync Server UC functionality.</span></span> <span data-ttu-id="e14ef-108">Après avoir migré un déploiement de Lync Server 2010 vers Lync Server 2013, vous devez également migrer les objets de contact associés au téléphone de zone commune hérité.</span><span class="sxs-lookup"><span data-stu-id="e14ef-108">After migrating an Lync Server 2010 deployment to Lync Server 2013, you must also migrate the contact objects associated with the legacy Common Area Phone.</span></span> <span data-ttu-id="e14ef-109">À l’aide de Lync Server Management Shell, vous devez d’abord récupérer tous les objets de contact associés aux téléphones de zone commune de Lync Server 2010, puis déplacer ces objets vers le pool Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e14ef-109">Using Lync Server Management Shell you will first retrieve all contact objects associated with the Lync Server 2010 Common Area Phones, and then move those objects to the Lync Server 2013 pool.</span></span>

<span data-ttu-id="e14ef-110">**Migration des téléphones de partie commune**</span><span class="sxs-lookup"><span data-stu-id="e14ef-110">**Migrate Common Area Phones**</span></span>

1.  <span data-ttu-id="e14ef-111">À partir du serveur frontal Lync Server 2013, ouvrez Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="e14ef-111">From the Lync Server 2013 Front End server, open Lync Server Management Shell.</span></span>

2.  <span data-ttu-id="e14ef-112">À partir de la ligne de commande, tapez ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="e14ef-112">From the command line, type the following:</span></span>
    
        Get-CsCommonAreaPhone -Filter {RegistrarPool -eq "pool01.contoso.net"} | Move-CsCommonAreaPhone -Target pool02.contoso.net

3.  <span data-ttu-id="e14ef-113">Pour vérifier que tous les objets de contact ont été déplacés vers le pool Lync Server 2013, à partir de Lync Server Management Shell, tapez ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="e14ef-113">To verify all contact objects have been moved to the Lync Server 2013 pool, from the Lync Server Management Shell type the following:</span></span>
    
        Get-CsCommonAreaPhone -Filter {RegistrarPool -eq "pool02.contoso.net"}
    
    <span data-ttu-id="e14ef-114">Vérifiez que tous les objets de contact sont désormais associés au pool Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e14ef-114">Verify all contact objects are now associated with the Lync Server 2013 pool.</span></span>

<span data-ttu-id="e14ef-115"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e14ef-115"></div>

<span> </span>

</div>

</div>

</span></span></div>

