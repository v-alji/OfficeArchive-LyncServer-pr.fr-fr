---
title: Déplacer plusieurs utilisateurs vers le pool de pilotes
description: Déplacer plusieurs utilisateurs vers le pool de pilotes.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Move multiple users to the pilot pool
ms:assetid: 90d0590c-922c-4933-b778-9dd850b59310
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205096(v=OCS.15)
ms:contentKeyID: 48184838
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 121509fbad863b0ce2d6cc9c7e9afaef360e2eb6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438495"
---
# <a name="move-multiple-users-to-the-pilot-pool"></a><span data-ttu-id="da847-103">Déplacer plusieurs utilisateurs vers le pool de pilotes</span><span class="sxs-lookup"><span data-stu-id="da847-103">Move multiple users to the pilot pool</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="da847-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="da847-104">

<span> </span></span></span>

<span data-ttu-id="da847-105">_**Dernière modification de la rubrique :** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="da847-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="da847-106">Vous pouvez déplacer plusieurs utilisateurs de votre pool Lync Server 2010 vers votre pool de pilotes Lync Server 2013 à l’aide de Lync Server 2013 panneau de configuration ou de Lync Server 2013 Management Shell.</span><span class="sxs-lookup"><span data-stu-id="da847-106">You can move multiple users from your Lync Server 2010 pool to your Lync Server 2013 pilot pool using Lync Server 2013 Control Panel or Lync Server 2013 Management Shell.</span></span>

<div>

## <a name="to-move-multiple-users-by-using-the-lync-server-2013-control-panel"></a><span data-ttu-id="da847-107">Pour déplacer plusieurs utilisateurs à l’aide du panneau de configuration de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="da847-107">To move multiple users by using the Lync Server 2013 Control Panel</span></span>

1.  <span data-ttu-id="da847-108">Ouvrez le **Paneau de configuration Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="da847-108">Open **Lync Server Control Panel**.</span></span>

2.  <span data-ttu-id="da847-109">Cliquez successivement sur **Utilisateurs**, Rechercher, puis sur **Trouver**.</span><span class="sxs-lookup"><span data-stu-id="da847-109">Click **Users**, click Search, and then click **Find**.</span></span>

3.  <span data-ttu-id="da847-110">Sélectionnez deux utilisateurs que vous voulez déplacer vers le pool Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="da847-110">Select two users that you want to move to the Lync Server 2013 pool.</span></span> <span data-ttu-id="da847-111">Dans cet exemple, nous allons déménager les utilisateurs Chen Yang et Claus Hansen.</span><span class="sxs-lookup"><span data-stu-id="da847-111">In this example, we will move users Chen Yang and Claus Hansen.</span></span>
    
    <span data-ttu-id="da847-112">![Déplacer des utilisateurs vers un pool de Registre spécifique](images/JJ205096.70d510e1-8e6b-40a5-a80b-27cbc63fc337(OCS.15).jpg "Déplacer des utilisateurs vers un pool de Registre spécifique")</span><span class="sxs-lookup"><span data-stu-id="da847-112">![Move users to specific register pool](images/JJ205096.70d510e1-8e6b-40a5-a80b-27cbc63fc337(OCS.15).jpg "Move users to specific register pool")</span></span>  

4.  <span data-ttu-id="da847-113">Dans le menu **action** , sélectionnez **déplacer les utilisateurs sélectionnés vers le pool**.</span><span class="sxs-lookup"><span data-stu-id="da847-113">From the **Action** menu, select **Move selected users to pool**.</span></span>

5.  <span data-ttu-id="da847-114">Dans la liste déroulante, sélectionnez le pool Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="da847-114">From the drop-down list, select the Lync Server 2013 pool.</span></span>

6.  <span data-ttu-id="da847-115">Cliquez sur **Action**, puis sur **Déplacer les utilisateurs sélectionnés vers le pool**.</span><span class="sxs-lookup"><span data-stu-id="da847-115">Click **Action** and then click **Move selected users to pool**.</span></span> <span data-ttu-id="da847-116">Cliquez sur OK.</span><span class="sxs-lookup"><span data-stu-id="da847-116">Click OK.</span></span>
    
    <span data-ttu-id="da847-117">![Déplacer des utilisateurs, boîte de dialogue pool d’inscriptions de destination](images/JJ205401.8a375003-dc00-4541-b578-4d88f2010601(OCS.15).png "Déplacer des utilisateurs, boîte de dialogue pool d’inscriptions de destination")</span><span class="sxs-lookup"><span data-stu-id="da847-117">![Move Users, destination registrar pool dialog box](images/JJ205401.8a375003-dc00-4541-b578-4d88f2010601(OCS.15).png "Move Users, destination registrar pool dialog box")</span></span>  

7.  <span data-ttu-id="da847-118">Vérifiez que la colonne **pool d’inscriptions** pour les utilisateurs contient désormais le pool Lync Server 2013, qui indique que les utilisateurs ont été déplacés correctement.</span><span class="sxs-lookup"><span data-stu-id="da847-118">Verify that the **Registrar pool** column for the users now contains the Lync Server 2013 pool, which indicates that the users have been successfully moved.</span></span>

</div>

<div>

## <a name="to-move-multiple-users-by-using-the-lync-server-2013-management-shell"></a><span data-ttu-id="da847-119">Pour déplacer plusieurs utilisateurs à l’aide de Lync Server 2013 Management Shell</span><span class="sxs-lookup"><span data-stu-id="da847-119">To move multiple users by using the Lync Server 2013 Management Shell</span></span>

1.  <span data-ttu-id="da847-120">Ouvrez Lync Server 2013 Management Shell.</span><span class="sxs-lookup"><span data-stu-id="da847-120">Open the Lync Server 2013 Management Shell.</span></span>

2.  <span data-ttu-id="da847-121">Dans la ligne de commande, tapez les informations suivantes et remplacez **User1** et **utilisateur2** par des noms d’utilisateur spécifiques que vous voulez déplacer, puis remplacez **\_ FQDN du pool** par le nom du pool de destination.</span><span class="sxs-lookup"><span data-stu-id="da847-121">At the command line, type the following and replace **User1** and **User2** with specific user names you want to move and replace **pool\_FQDN** with the name of the destination pool.</span></span> <span data-ttu-id="da847-122">Dans cet exemple, nous allons déplacer les utilisateurs de Hao Chen et Katie Jordanie.</span><span class="sxs-lookup"><span data-stu-id="da847-122">In this example we will move users Hao Chen and Katie Jordan.</span></span>
    
        Get-CsUser -Filter {DisplayName -eq "User1" -or DisplayName - eq "User2"} | Move-CsUser -Target "pool_FQDN"
    
    <span data-ttu-id="da847-123">![Exemple d’applet de Get-CsUser PowerShell](images/JJ205096.767ff9fc-755d-4a80-a710-5b1367aecbe0(OCS.15).jpg "Exemple d’applet de Get-CsUser PowerShell")</span><span class="sxs-lookup"><span data-stu-id="da847-123">![Example of PowerShell Get-CsUser cmdlet](images/JJ205096.767ff9fc-755d-4a80-a710-5b1367aecbe0(OCS.15).jpg "Example of PowerShell Get-CsUser cmdlet")</span></span>  

3.  <span data-ttu-id="da847-124">Dans la ligne de commande, tapez ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="da847-124">At the command line, type the following</span></span>
    
        Get-CsUser -Identity "User1"

4.  <span data-ttu-id="da847-125">L’identité du **pool d’inscriptions** doit maintenant pointer sur le pool que vous avez spécifié comme **nom de \_ domaine complet du pool** à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="da847-125">The **Registrar Pool** identity should now point to the pool you specified as **pool\_FQDN** in the previous step.</span></span> <span data-ttu-id="da847-126">La présence de cette identité confirme que l’utilisateur a bien été déplacé.</span><span class="sxs-lookup"><span data-stu-id="da847-126">The presence of this identity confirms that the user has been successfully moved.</span></span> <span data-ttu-id="da847-127">Répétez l’étape pour vérifier que l' **utilisateur2** a été déplacé.</span><span class="sxs-lookup"><span data-stu-id="da847-127">Repeat step to verify **User2** has been moved.</span></span>
    
    <span data-ttu-id="da847-128">![Sortie de l’applet de cmdlet PowerShell Get-UsUser-Identity](images/JJ205096.8ff04c67-37a0-4156-bfbc-28f9f7b137c8(OCS.15).jpg "Sortie de l’applet de cmdlet PowerShell Get-UsUser-Identity")</span><span class="sxs-lookup"><span data-stu-id="da847-128">![Output of PowerShell Get-UsUser -Identity cmdlet](images/JJ205096.8ff04c67-37a0-4156-bfbc-28f9f7b137c8(OCS.15).jpg "Output of PowerShell Get-UsUser -Identity  cmdlet")</span></span>  

</div>

<div>

## <a name="to-move-all-users-at-the-same-time-by-using-the-lync-server-2013-management-shell"></a><span data-ttu-id="da847-129">Pour déplacer tous les utilisateurs en même temps à l’aide de Lync Server 2013 Management Shell</span><span class="sxs-lookup"><span data-stu-id="da847-129">To move all users at the same time by using the Lync Server 2013 Management Shell</span></span>

<span data-ttu-id="da847-130">Dans cet exemple, tous les utilisateurs ont été retournés au pool Lync Server 2010 (pool01.contoso.net).</span><span class="sxs-lookup"><span data-stu-id="da847-130">In this example, all users have been returned to the Lync Server 2010 pool (pool01.contoso.net).</span></span> <span data-ttu-id="da847-131">À l’aide de Lync Server 2013 Management Shell, tous les utilisateurs sont déplacés en même temps que le pool Lync Server 2013 (pool02.contoso.net).</span><span class="sxs-lookup"><span data-stu-id="da847-131">Using the Lync Server 2013 Management Shell, we will move all users at the same time to the Lync Server 2013 pool (pool02.contoso.net).</span></span>

1.  <span data-ttu-id="da847-132">Ouvrez **Lync Server 2013 Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="da847-132">Open the **Lync Server 2013 Management Shell**.</span></span>

2.  <span data-ttu-id="da847-133">Dans la ligne de commande, tapez ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="da847-133">At the command line, type the following:</span></span>
    
        Get-CsUser -OnLyncServer | Move-CsUser -Target "pool_FQDN"
    
    <span data-ttu-id="da847-134">![Applet de requête PowerShell et résultats dans Management Shell](images/JJ205096.1e57ccb1-9378-4dc7-82b7-dcaa63a285c6(OCS.15).png "Applet de requête PowerShell et résultats dans Management Shell")</span><span class="sxs-lookup"><span data-stu-id="da847-134">![PowerShell cmdlet and results in Management Shell](images/JJ205096.1e57ccb1-9378-4dc7-82b7-dcaa63a285c6(OCS.15).png "PowerShell cmdlet and results in Management Shell")</span></span>  

3.  <span data-ttu-id="da847-135">Exécutez ensuite **Get-Csuser** pour l’un des utilisateurs pilote.</span><span class="sxs-lookup"><span data-stu-id="da847-135">Next, run **Get-CsUser** for one of the pilot users.</span></span>
    
        Get-CsUser -Identity "Hao Chen"

4.  <span data-ttu-id="da847-136">L’identité du **pool d’inscriptions** pour chaque utilisateur pointe désormais sur le pool que vous avez spécifié comme « \_ nom de domaine complet du pool » à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="da847-136">The **Registrar Pool** identity for each user now points to the pool you specified as “pool\_FQDN” in the previous step.</span></span> <span data-ttu-id="da847-137">La présence de cette identité confirme que l’utilisateur a bien été déplacé.</span><span class="sxs-lookup"><span data-stu-id="da847-137">The presence of this identity confirms that the user has been successfully moved.</span></span>

5.  <span data-ttu-id="da847-138">Par ailleurs, nous pouvons afficher la liste des utilisateurs dans le panneau de configuration de Lync Server 2013 et vérifier que la valeur du pool d’inscriptions pointe désormais vers le pool Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="da847-138">Additionally, we can view the list of users in the Lync Server 2013 Control Panel and verify that the Registrar Pool value now points to the Lync Server 2013 pool.</span></span>
    
    <span data-ttu-id="da847-139">![Liste des utilisateurs de Lync Server 2013 Control Panel](images/JJ205096.3f2e87a7-ec59-43c5-82cb-e770108bfb04(OCS.15).jpg "Liste des utilisateurs de Lync Server 2013 Control Panel")</span><span class="sxs-lookup"><span data-stu-id="da847-139">![Lync Server 2013 Control Panel user list](images/JJ205096.3f2e87a7-ec59-43c5-82cb-e770108bfb04(OCS.15).jpg "Lync Server 2013 Control Panel user list")</span></span>  

<span data-ttu-id="da847-140"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="da847-140"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

