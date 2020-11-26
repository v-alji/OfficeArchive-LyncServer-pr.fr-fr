---
title: Migrer les numéros d’accès entrant
description: Migration des numéros d’accès rendez-vous.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migrate dial-in access numbers
ms:assetid: e0dfaed2-64c7-45cb-aaa9-d6117a26625d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721909(v=OCS.15)
ms:contentKeyID: 49733843
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e2c8bd34a30bc4b3f8999144cd84a1eee62e2ab1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446891"
---
# <a name="migrate-dial-in-access-numbers"></a><span data-ttu-id="a3ead-103">Migrer les numéros d’accès entrant</span><span class="sxs-lookup"><span data-stu-id="a3ead-103">Migrate dial-in access numbers</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a3ead-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a3ead-104">

<span> </span></span></span>

<span data-ttu-id="a3ead-105">_**Dernière modification de la rubrique :** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="a3ead-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="a3ead-106">La migration des numéros d’accès rendez-vous de Lync Server 2010 vers Lync Server 2013 nécessite l’exécution de l’applet de connexion **Move-CsApplicationEndpoint** pour migrer les objets de contact.</span><span class="sxs-lookup"><span data-stu-id="a3ead-106">Migrating dial-in access numbers from Lync Server 2010 to Lync Server 2013 requires running the **Move-CsApplicationEndpoint** cmdlet to migrate the contact objects.</span></span> <span data-ttu-id="a3ead-107">Pendant la période de coexistence Lync Server 2010 et Lync Server 2013, les numéros d’accès rendez-vous créés dans Lync Server 2013 se comportent de la même manière que les numéros d’accès rendez-vous créés dans Lync Server 2010, comme décrit dans cette section.</span><span class="sxs-lookup"><span data-stu-id="a3ead-107">During the Lync Server 2010 and Lync Server 2013 coexistence period, dial-in access numbers that you created in Lync Server 2013 behave similarly to the dial-in access numbers that you create in Lync Server 2010, as described in this section.</span></span>

<span data-ttu-id="a3ead-108">Les numéros d’accès rendez-vous que vous avez créés dans Lync Server 2010, mais qui ont été déplacés vers Lync Server 2013 ou que vous avez créés dans Lync Server 2013 auparavant, pendant ou après la migration, présentent les caractéristiques suivantes :</span><span class="sxs-lookup"><span data-stu-id="a3ead-108">Dial-in access numbers that you created in Lync Server 2010 but moved to Lync Server 2013 or that you created in Lync Server 2013 before, during or after migration have the following characteristics:</span></span>

  - <span data-ttu-id="a3ead-109">N’apparaissent pas dans les invitations aux réunions Office Communications Server 2007 R2 et la page numéro d’accès rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="a3ead-109">Do not appear on Office Communications Server 2007 R2 meeting invitations and the dial-in access number page.</span></span>

  - <span data-ttu-id="a3ead-110">S’affichent dans les invitations aux réunions Lync Server 2010 et la page numéro d’accès rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="a3ead-110">Appear on Lync Server 2010 meeting invitations and the dial-in access number page.</span></span>

  - <span data-ttu-id="a3ead-111">S’affichent dans les invitations aux réunions Lync Server 2013 et la page numéro d’accès rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="a3ead-111">Appear on Lync Server 2013 meeting invitations and the dial-in access number page.</span></span>

  - <span data-ttu-id="a3ead-112">Ne peut pas être affiché ou modifié dans l’outil d’administration d’Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="a3ead-112">Cannot be viewed or modified in the Office Communications Server 2007 R2 administrative tool.</span></span>

  - <span data-ttu-id="a3ead-113">Peut être affiché et modifié dans le panneau de configuration de Lync Server 2010 et dans Lync Server 2010 Management Shell.</span><span class="sxs-lookup"><span data-stu-id="a3ead-113">Can be viewed and modified in the Lync Server 2010 Control Panel and in Lync Server 2010 Management Shell.</span></span>

  - <span data-ttu-id="a3ead-114">Peut être affiché et modifié dans le panneau de configuration de Lync Server 2013 et dans Lync Server 2013 Management Shell.</span><span class="sxs-lookup"><span data-stu-id="a3ead-114">Can be viewed and modified in the Lync Server 2013 Control Panel and in Lync Server 2013 Management Shell.</span></span>

  - <span data-ttu-id="a3ead-115">Peuvent être réécrits au sein de la région à l’aide de l’applet de requête Set-CsDialinConferencingAccessNumber avec le paramètre Priority.</span><span class="sxs-lookup"><span data-stu-id="a3ead-115">Can be re-sequenced within the region by using the Set-CsDialinConferencingAccessNumber cmdlet with the Priority parameter.</span></span>

<span data-ttu-id="a3ead-116">Vous devez terminer la migration des numéros d’accès rendez-vous qui pointent vers un pool Lync Server 2010 avant de désactiver le pool Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="a3ead-116">You must finish migrating dial-in access numbers that point to a Lync Server 2010 pool before you decommission the Lync Server 2010 pool.</span></span> <span data-ttu-id="a3ead-117">Si vous n’avez pas terminé la migration des numéros d’accès rendez-vous, comme indiqué dans la procédure suivante, les appels entrants vers les numéros d’accès échoueront.</span><span class="sxs-lookup"><span data-stu-id="a3ead-117">If you do not complete dial-in access number migration as described in the following procedure, incoming calls to the access numbers will fail.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="a3ead-118">Vous devez effectuer cette procédure avant de désaffecter le pool Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="a3ead-118">You must perform this procedure prior to decommissioning the Lync Server 2010 pool.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="a3ead-119">Nous vous recommandons de déplacer les numéros d’accès rendez-vous lorsque le niveau d’utilisation du réseau est faible, en cas de panne de service de courte durée.</span><span class="sxs-lookup"><span data-stu-id="a3ead-119">We recommend that you move dial-in access numbers when network usage is low, in case there is a short period of service outage.</span></span>



</div>

<span data-ttu-id="a3ead-120">**Pour identifier et déplacer les numéros d’accès rendez-vous**</span><span class="sxs-lookup"><span data-stu-id="a3ead-120">**To identify and move dial-in access numbers**</span></span>

1.  <span data-ttu-id="a3ead-121">Démarrez Lync Server Management Shell : cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="a3ead-121">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="a3ead-122">Pour déplacer chaque numéro d’accès entrant vers un pool hébergé sur Lync Server 2013, à partir de la ligne de commande :</span><span class="sxs-lookup"><span data-stu-id="a3ead-122">To move each dial-in access number to a pool hosted on Lync Server 2013, from the command line run:</span></span>
    
        Move-CsApplicationEndpoint -Identity <SIP URI of the access number to be moved> -Target <FQDN of the pool to which the access number is moving>

3.  <span data-ttu-id="a3ead-123">Ouvrez le Paneau de configuration Lync Server.</span><span class="sxs-lookup"><span data-stu-id="a3ead-123">Open Lync Server Control Panel.</span></span>

4.  <span data-ttu-id="a3ead-124">Dans la barre de navigation de gauche, cliquez sur **Conférences**.</span><span class="sxs-lookup"><span data-stu-id="a3ead-124">In the left navigation bar, click **Conferencing**.</span></span>

5.  <span data-ttu-id="a3ead-125">Cliquez sur l’onglet **numéro d’accès** rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="a3ead-125">Click the **Dial-in Access Number** tab.</span></span>

6.  <span data-ttu-id="a3ead-126">Vérifiez qu’aucun numéro d’accès par connexion n’est conservé pour le pool Lync Server 2010 à partir duquel vous effectuez la migration.</span><span class="sxs-lookup"><span data-stu-id="a3ead-126">Verify that no dial-in access numbers remain for the Lync Server 2010 pool from which you are migrating.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="a3ead-127">Lorsque tous les numéros d’accès par connexion pointent vers le pool Lync Server 2013, vous pouvez désactiver le pool Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="a3ead-127">When all dial-in access numbers point to the Lync Server 2013 pool, you can then decommission the Lync Server 2010 pool.</span></span>

    
    </div>

<span data-ttu-id="a3ead-128">**Vérifier la migration des numéros d’accès rendez-vous à l’aide du panneau de configuration de Lync Server**</span><span class="sxs-lookup"><span data-stu-id="a3ead-128">**Verify the dial-in access number migration using Lync Server Control Panel**</span></span>

1.  <span data-ttu-id="a3ead-129">À partir d’un compte d’utilisateur affecté au rôle **CsUserAdministrator** ou au rôle **CsAdministrator** , connectez-vous à n’importe quel ordinateur dans votre déploiement interne.</span><span class="sxs-lookup"><span data-stu-id="a3ead-129">From a user account that is assigned to the **CsUserAdministrator** role or the **CsAdministrator** role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="a3ead-130">Ouvrez le Paneau de configuration Lync Server.</span><span class="sxs-lookup"><span data-stu-id="a3ead-130">Open Lync Server Control Panel.</span></span>

3.  <span data-ttu-id="a3ead-131">Dans la barre de navigation de gauche, cliquez sur **Conférences**.</span><span class="sxs-lookup"><span data-stu-id="a3ead-131">In the left navigation bar, click **Conferencing**.</span></span>

4.  <span data-ttu-id="a3ead-132">Cliquez sur l’onglet **numéro d’accès** rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="a3ead-132">Click the **Dial-in Access Number** tab.</span></span>

5.  <span data-ttu-id="a3ead-133">Vérifiez que tous les numéros d’accès rendez-vous sont déplacés vers le pool hébergé sur Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a3ead-133">Verify all the dial-in access number are migrated to the pool hosted on Lync Server 2013.</span></span>

<span data-ttu-id="a3ead-134">**Vérifier la migration des numéros d’accès entrants à l’aide de Lync Server Management Shell**</span><span class="sxs-lookup"><span data-stu-id="a3ead-134">**Verify the dial-in access number migration using Lync Server Management Shell**</span></span>

1.  <span data-ttu-id="a3ead-135">Ouvrez Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="a3ead-135">Open Lync Server Management Shell.</span></span>

2.  <span data-ttu-id="a3ead-136">Pour rétablir tous les numéros d’accès pour les conférences rendez-vous transférés, à partir de la ligne de commande :</span><span class="sxs-lookup"><span data-stu-id="a3ead-136">To return all the dial-in conferencing access numbers migrated, from the command line run:</span></span>
    
        Get-CsDialInConferencingAccessNumber -Filter {Pool -eq "<FQDN of the pool to which the access number is moved>"}

3.  <span data-ttu-id="a3ead-137">Vérifiez que tous les numéros d’accès rendez-vous sont déplacés vers le pool hébergé sur Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a3ead-137">Verify all the dial-in access numbers are migrated to the pool hosted on Lync Server 2013.</span></span>

<span data-ttu-id="a3ead-138"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a3ead-138"></div>

<span> </span>

</div>

</div>

</span></span></div>

