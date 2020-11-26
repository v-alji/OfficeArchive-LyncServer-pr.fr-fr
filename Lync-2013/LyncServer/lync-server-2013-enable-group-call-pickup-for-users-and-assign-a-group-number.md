---
title: 'Lync Server 2013 : activez le prélèvement d’appel de groupe pour les utilisateurs et attribuez un numéro de groupe'
description: 'Lync Server 2013 : activez le prélèvement d’appels de groupe pour les utilisateurs et attribuez un numéro de groupe.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enable Group Call Pickup for users and assign a group number
ms:assetid: c33bb6c2-d43b-4fb6-a0fa-6d82a7b09abe
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945650(v=OCS.15)
ms:contentKeyID: 51541517
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a03fcb20bfd88842dc8b29100b9ece595bf76254
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428922"
---
# <a name="enable-group-call-pickup-for-users-in-lync-server-2013-and-assign-a-group-number"></a><span data-ttu-id="2b70d-103">Activer le prélèvement d’appels de groupe pour les utilisateurs dans Lync Server 2013 et affecter un numéro de groupe</span><span class="sxs-lookup"><span data-stu-id="2b70d-103">Enable Group Call Pickup for users in Lync Server 2013 and assign a group number</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2b70d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2b70d-104">

<span> </span></span></span>

<span data-ttu-id="2b70d-105">_**Dernière modification de la rubrique :** 2013-01-30_</span><span class="sxs-lookup"><span data-stu-id="2b70d-105">_**Topic Last Modified:** 2013-01-30_</span></span>

<span data-ttu-id="2b70d-106">Après avoir ajouté des numéros de groupe de cueillette des appels à la table d’orbite du parc d’appels, vous pouvez attribuer les numéros de groupe aux utilisateurs et activer le prélèvement d’appels de groupe.</span><span class="sxs-lookup"><span data-stu-id="2b70d-106">After you add call pickup group numbers to the call park orbit table, you assign the group numbers to users and enable Group Call Pickup for them.</span></span> <span data-ttu-id="2b70d-107">Utilisez l’outil du kit de ressources de l’extension secondaire (SEFAUtil) pour attribuer des numéros de groupe et activer le choix des appels de groupe.</span><span class="sxs-lookup"><span data-stu-id="2b70d-107">Use the secondary extension feature activation (SEFAUtil) resource kit tool to assign group numbers and enable Group Call Pickup.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="2b70d-108">Dans un déploiement hybride, n’affectez pas de groupe de collecte d’appels de groupe aux utilisateurs hébergés en ligne.</span><span class="sxs-lookup"><span data-stu-id="2b70d-108">In a hybrid deployment, do not assign a Group Call Pickup group to users who are homed online.</span></span> <span data-ttu-id="2b70d-109">Les utilisateurs hébergés en ligne ne peuvent pas participer à la cueillette du groupe.</span><span class="sxs-lookup"><span data-stu-id="2b70d-109">Users who are homed online cannot participate in Group Call Pickup.</span></span> <span data-ttu-id="2b70d-110">Autrement dit, leurs appels ne peuvent pas être pris par d’autres utilisateurs et ils ne peuvent pas répondre aux appels destinés à d’autres utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="2b70d-110">That is, their calls cannot be answered by other users, and they cannot answer calls to other users.</span></span>



</div>

<div>

## <a name="to-assign-a-group-number-and-enable-group-call-pickup-for-a-user"></a><span data-ttu-id="2b70d-111">Pour attribuer un numéro de groupe et activer le prélèvement d’appels de groupe pour un utilisateur</span><span class="sxs-lookup"><span data-stu-id="2b70d-111">To assign a group number and enable Group Call Pickup for a user</span></span>

1.  <span data-ttu-id="2b70d-112">Ouvrez une session sur l’ordinateur où vous avez installé l’outil SEFAUtil avec des droits d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="2b70d-112">Log on to the computer where you installed the SEFAUtil tool with administrator rights.</span></span>

2.  <span data-ttu-id="2b70d-113">À partir de la ligne de commande, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="2b70d-113">At the command line, run:</span></span>
    
        SEFAUtil.exe sip:<sip address of user> /server:<pool FQDN> /enablegrouppickup:<group number>
    
    <span data-ttu-id="2b70d-114">Par exemple, pour assigner le numéro de groupe 199 à un utilisateur, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="2b70d-114">For example, to assign group number 199 to a user:</span></span>
    
        SEFAUtil.exe katarina@contoso.com /server:pool01.contoso.com /enablegrouppickup:199 

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="2b70d-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2b70d-115">See Also</span></span>


[<span data-ttu-id="2b70d-116">Désactiver le prélèvement d’appels de groupe pour les utilisateurs dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2b70d-116">Disable Group Call Pickup for users in Lync Server 2013</span></span>](lync-server-2013-disable-group-call-pickup-for-users.md)  
  

<span data-ttu-id="2b70d-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2b70d-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

