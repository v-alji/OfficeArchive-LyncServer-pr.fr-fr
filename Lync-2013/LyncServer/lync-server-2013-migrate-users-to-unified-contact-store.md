---
title: 'Lync Server 2013 : Migration des utilisateurs vers le magasin de contacts unifié'
description: 'Lync Server 2013 : migrer des utilisateurs vers un magasin de contacts unifié.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Migrate users to unified contact store
ms:assetid: 215a8ec1-d63e-4fdf-b73d-75aeb9dddb43
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204737(v=OCS.15)
ms:contentKeyID: 48183600
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9e9ee9850cc723ae132f15d7c0c6b3769e1240ba
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425590"
---
# <a name="migrate-users-to-unified-contact-store-in-lync-server-2013"></a><span data-ttu-id="d9f74-103">Migration des utilisateurs vers le magasin de contacts unifié dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d9f74-103">Migrate users to unified contact store in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d9f74-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d9f74-104">

<span> </span></span></span>

<span data-ttu-id="d9f74-105">_**Dernière modification de la rubrique :** 2012-10-15_</span><span class="sxs-lookup"><span data-stu-id="d9f74-105">_**Topic Last Modified:** 2012-10-15_</span></span>

<span data-ttu-id="d9f74-106">Les contacts d’un utilisateur sont automatiquement déplacés vers le serveur Exchange 2013 lorsque l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="d9f74-106">A user's contacts are automatically migrated to the Exchange 2013 server when the user:</span></span>

  - <span data-ttu-id="d9f74-107">une stratégie de services utilisateur dont le paramètre UcsAllowed a la valeur True a été attribuée à l’utilisateur ;</span><span class="sxs-lookup"><span data-stu-id="d9f74-107">Has been assigned a user services policy that has UcsAllowed set to True.</span></span>

  - <span data-ttu-id="d9f74-108">A été configuré avec une boîte aux lettres Exchange 2013 et s’est connecté à la boîte aux lettres au moins une fois.</span><span class="sxs-lookup"><span data-stu-id="d9f74-108">Has been provisioned with an Exchange 2013 mailbox and has signed into the mailbox at least once.</span></span>

  - <span data-ttu-id="d9f74-109">Se connecte à l’aide d’un client enrichi Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="d9f74-109">Logs in by using a Lync 2013 rich client.</span></span>

<span data-ttu-id="d9f74-110">Si l’utilisateur se connecte à l’aide d’un client Lync 2010 ou antérieur, ou si l’utilisateur n’est pas connecté à un serveur Exchange 2013, la stratégie de services des utilisateurs est ignorée et les contacts de l’utilisateur restent dans Lync Server.</span><span class="sxs-lookup"><span data-stu-id="d9f74-110">If the user logs in with a Lync 2010 or earlier client, or if the user is not connected to an Exchange 2013 server, the user services policy is ignored and the user's contacts remain in Lync Server.</span></span>

<span data-ttu-id="d9f74-111">Déterminez si les contacts d’un utilisateur ont été transférés en utilisant l’une des méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="d9f74-111">You can determine whether a user's contacts have been migrated by using either of the following methods:</span></span>

  - <span data-ttu-id="d9f74-112">Vérifiez la clé de Registre suivante sur l’ordinateur client :</span><span class="sxs-lookup"><span data-stu-id="d9f74-112">Check the following registry key on the client computer:</span></span>
    
    <span data-ttu-id="d9f74-113">HKEY \_ \_ logiciel utilisateur \\ actuel \\ Microsoft \\ Office \\ 15,0 \\ Lync \\ \<SIP URL\> \\ UCS</span><span class="sxs-lookup"><span data-stu-id="d9f74-113">HKEY\_CURRENT\_USER\\Software\\Microsoft\\Office\\15.0\\Lync\\\<SIP URL\>\\UCS</span></span>
    
    <span data-ttu-id="d9f74-114">Si les contacts de l’utilisateur sont stockés dans Exchange 2013, cette clé contient une valeur de InUCSMode avec une valeur de 2165.</span><span class="sxs-lookup"><span data-stu-id="d9f74-114">If the user's contacts are stored in Exchange 2013, this key contains a value of InUCSMode with a value of 2165.</span></span>

  - <span data-ttu-id="d9f74-115">Exécutez l’applet de commande **Test-CsUnifiedContactStore**.</span><span class="sxs-lookup"><span data-stu-id="d9f74-115">Run the **Test-CsUnifiedContactStore** cmdlet.</span></span> <span data-ttu-id="d9f74-116">Dans la ligne de commande Lync Server Management Shell, tapez :</span><span class="sxs-lookup"><span data-stu-id="d9f74-116">At the Lync Server Management Shell command line, type:</span></span>
    
        Test-CsUnifiedContactStore -UserSipAddress "sip:kenmyer@litwareinc.com" -TargetFqdn "atl-cs-001.litwareinc.com"
    
    <span data-ttu-id="d9f74-117">Si l’exécution de la commande **Test-CsUnifiedContactStore** s’est déroulée correctement, les contacts de l’utilisateur ont été migrés vers le magasin de contacts unifié.</span><span class="sxs-lookup"><span data-stu-id="d9f74-117">If **Test-CsUnifiedContactStore** succeeds, the user's contacts were migrated to unified contact store.</span></span>

<span data-ttu-id="d9f74-118"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d9f74-118"></div>

<span> </span>

</div>

</div>

</span></span></div>

