---
title: 'Lync Server 2013 : Restauration des utilisateurs migrés'
description: 'Lync Server 2013 : restaurez les utilisateurs migrés.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Roll back migrated users
ms:assetid: bfabaf0b-9a42-4057-b729-a7ab9eee8c72
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205224(v=OCS.15)
ms:contentKeyID: 48185286
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c5993bfd530c84307d3ee5be627b3ed33814be73
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442342"
---
# <a name="roll-back-migrated-users-in-lync-server-2013"></a><span data-ttu-id="9dced-103">Restauration des utilisateurs migrés dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9dced-103">Roll back migrated users in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9dced-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9dced-104">

<span> </span></span></span>

<span data-ttu-id="9dced-105">_**Dernière modification de la rubrique :** 2012-10-07_</span><span class="sxs-lookup"><span data-stu-id="9dced-105">_**Topic Last Modified:** 2012-10-07_</span></span>

<span data-ttu-id="9dced-106">Si vous avez besoin de restaurer la fonctionnalité de magasin de contacts unifiée, restaurez les contacts uniquement si vous revenez à l’utilisateur dans Exchange 2010 ou Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="9dced-106">If you need to roll back the unified contact store feature, roll back the contacts only if you move the user back to Exchange 2010 or Lync Server 2010.</span></span> <span data-ttu-id="9dced-107">Pour effectuer la restauration, désactivez la stratégie définie pour l’utilisateur, puis exécutez l’applet de commande **Invoke-CsUcsRollback**.</span><span class="sxs-lookup"><span data-stu-id="9dced-107">To roll back, disable the policy for the user, and then run the **Invoke-CsUcsRollback** cmdlet.</span></span> <span data-ttu-id="9dced-108">La simple exécution de **Invoke-CsUcsRollback** ne suffit pas à garantir une restauration permanente ; en effet, si la stratégie n’est pas désactivée, le magasin de contacts unifié continue d’être transféré.</span><span class="sxs-lookup"><span data-stu-id="9dced-108">Just running **Invoke-CsUcsRollback** alone is not enough to ensure permanent rollback, because unified contact store migration will be initiated again if the policy is not disabled.</span></span> <span data-ttu-id="9dced-109">Par exemple, si un utilisateur est restauré, car Exchange 2013 est restauré dans Exchange 2010, puis la boîte aux lettres de l’utilisateur est déplacée vers Exchange 2013, la migration de magasin de contacts unifiée est lancée à l’issue de la période d’annulation, tant que le magasin de contacts unifié est toujours activé pour l’utilisateur dans la stratégie de services des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="9dced-109">For example, if a user is rolled back because Exchange 2013 is rolled back to Exchange 2010, and then the user’s mailbox is moved to Exchange 2013, the unified contact store migration will be initiated again seven days after the rollback, as long as unified contact store is still enabled for the user in the user services policy.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="9dced-110">L’applet de commande <STRONG>Move-Csuser</STRONG> restaure automatiquement le magasin de contacts de l’utilisateur à partir d’Exchange 2013 vers Lync Server 2013 dans les situations suivantes :</span><span class="sxs-lookup"><span data-stu-id="9dced-110">The <STRONG>Move-CsUser</STRONG> cmdlet automatically rolls back the user's contact store from Exchange 2013 to Lync Server 2013 in the following situations:</span></span> 
> <UL>
> <LI>
> <P><span data-ttu-id="9dced-111">Lorsque les utilisateurs sont déplacés de Lync Server 2013 vers Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="9dced-111">When users are moved from Lync Server 2013 to Lync Server 2010.</span></span></P>
> <LI>
> <P><span data-ttu-id="9dced-112">Lorsque les utilisateurs migrent l’environnement croisé, par exemple lorsqu’un utilisateur est déplacé de Lync Online vers Lync Server 2013 local, ou vice-versa.</span><span class="sxs-lookup"><span data-stu-id="9dced-112">When users are migrated cross premises, such as when a user is moved from Lync Online to Lync Server 2013 on-premises, or vice versa.</span></span></P></LI></UL>



</div>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="9dced-p102">L’importation des données d’un magasin de contacts unifié à partir d’une base de données de sauvegarde peut endommager les données du magasin de contacts unifié et les données utilisateur si le mode de magasin de contacts unifié a été modifié entre l’exportation et l’importation. Par exemple :</span><span class="sxs-lookup"><span data-stu-id="9dced-p102">Importing unified contact store data from a backup database can cause unified contact store data and user data to become corrupted if the unified contact store mode changed between the export and the import. For example:</span></span> 
> <UL>
> <LI>
> <P><span data-ttu-id="9dced-115">Si vous exportez des listes de contacts avant la migration des contacts de l’utilisateur vers Exchange 2013, puis après la migration, vous importez les mêmes données, les données et les listes de contacts du magasin de contacts unifié seront corrompues.</span><span class="sxs-lookup"><span data-stu-id="9dced-115">If you export contact lists before the users' contacts are migrated to Exchange 2013 and then, after the migration, import the same data, the unified contact store data and contact lists will be corrupted.</span></span></P>
> <LI>
> <P><span data-ttu-id="9dced-116">Si vous exportez des éléments UserData après avoir migré des utilisateurs vers Exchange 2013, restaurez la migration, et pour une raison quelconque, vous importez les données à partir d’après la migration, les données et les listes de contacts du magasin de contacts unifié seront endommagées.</span><span class="sxs-lookup"><span data-stu-id="9dced-116">If you export userdata after you migrate users to Exchange 2013, roll back the migration, and then for some reason you import the data from after the migration, the unified contact store data and contact lists will be corrupted.</span></span></P></LI></UL>



</div>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="9dced-117">Avant de déplacer une boîte aux lettres Exchange à partir d’Exchange 2013 vers Exchange 2010, l’administrateur Exchange doit s’assurer que l’administrateur de Lync Server a restauré le premier contact de l’utilisateur du serveur Lync à partir d’Exchange 2013 sur Lync Server.</span><span class="sxs-lookup"><span data-stu-id="9dced-117">Before you move an Exchange mailbox from Exchange 2013 to Exchange 2010, the Exchange administrator must make sure that the Lync Server administrator has first rolled back the Lync Server user contacts from Exchange 2013 to Lync Server.</span></span> <span data-ttu-id="9dced-118">Pour restaurer des contacts de magasin de contacts unifiés vers Lync Server, reportez-vous à la procédure « pour restaurer des contacts de magasin de contacts unifiés à partir d’Exchange 2013 vers Lync Server 2013 », plus loin dans cette section.</span><span class="sxs-lookup"><span data-stu-id="9dced-118">To roll back unified contact store contacts to Lync Server, see procedure "To roll back unified contact store contacts from Exchange 2013 to Lync Server 2013," later in this section.</span></span>



</div>

<span data-ttu-id="9dced-119">La procédure suivante explique comment restaurer les contacts des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="9dced-119">The following procedure describes how to roll back user contacts.</span></span> <span data-ttu-id="9dced-120">Si vous utilisez l’applet de action **Move-Csuser** pour déplacer des utilisateurs entre lync Server 2013 et lync Server 2010, vous pouvez ignorer ces étapes dans la mesure où l’applet de **passe de migration-Csuser** restaure automatiquement Unifed magasin de contacts lors du déplacement des utilisateurs de Lync Server 2013 vers Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="9dced-120">If you use the **Move-CsUser** cmdlet to move users between Lync Server 2013 and Lync Server 2010, you can skip these steps because the **Move-CsUser** cmdlet automatically rolls back unifed contact store when it moves users from Lync Server 2013 to Lync Server 2010.</span></span> <span data-ttu-id="9dced-121">**Move-Csuser** n’entraîne pas la désactivation de la stratégie de magasin de contacts unifiée, de sorte que la migration vers le magasin de contacts unifié se reproduit si l’utilisateur est reculé sur Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="9dced-121">**Move-CsUser** does not disable unified contact store policy, so the migration to unified contact store will recur if the user is moved back to Lync Server 2013.</span></span>

<div>

## <a name="to-roll-back-user-contacts-from-lync-server-2013-to-lync-server-2010"></a><span data-ttu-id="9dced-122">Pour restaurer des contacts de l’utilisateur de Lync Server 2013 vers Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="9dced-122">To roll back user contacts from Lync Server 2013 to Lync Server 2010</span></span>

1.  <span data-ttu-id="9dced-123">Démarrez Lync Server Management Shell : cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="9dced-123">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="9dced-124">Désactivez le magasin de contacts unifié pour que les utilisateurs soient restaurés de façon à ce qu’ils ne soient pas à nouveau migrés après la restauration.</span><span class="sxs-lookup"><span data-stu-id="9dced-124">Disable unified contact store for the users to be rolled back so that they will not be remigrated after rollback.</span></span> <span data-ttu-id="9dced-125">(N’effectuez cette étape que si vous voulez vous assurer que les utilisateurs ne seront pas remigré ultérieurement.) Pour désactiver le magasin de contacts unifié pour des utilisateurs individuels, sur la ligne de commande, tapez :</span><span class="sxs-lookup"><span data-stu-id="9dced-125">(Perform this step only if you want to make sure that users will not remigrate in the future.) To disable unified contact store for individual users, at the command line, type:</span></span>
    
        Set-CsUserServicesPolicy -Identity "<policy name>" -UcsAllowed $False
    
    <span data-ttu-id="9dced-126">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="9dced-126">For example:</span></span>
    
        Set-CsUserServicesPolicy -Identity "UCS Enabled Users" -UcsAllowed $False

3.  <span data-ttu-id="9dced-127">Avant de déplacer un utilisateur de Lync Server 2013 vers Lync Server 2010, restaurez la liste d’amis pour les utilisateurs spécifiés sur Lync Server.</span><span class="sxs-lookup"><span data-stu-id="9dced-127">Before moving a user from Lync Server 2013 to Lync Server 2010, roll back the Buddy List for the specified users on Lync Server.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="9dced-128">Si cette étape n’est pas spécifiée, la liste d’amis sera perdue.</span><span class="sxs-lookup"><span data-stu-id="9dced-128">If this step is omitted, the Buddy List will be lost.</span></span>

    
    </div>

4.  <span data-ttu-id="9dced-129">Restaurez les utilisateurs spécifiés.</span><span class="sxs-lookup"><span data-stu-id="9dced-129">Roll back the specified users.</span></span> <span data-ttu-id="9dced-130">Dans la ligne de commande, tapez :</span><span class="sxs-lookup"><span data-stu-id="9dced-130">At the command line, type:</span></span>
    
        Invoke-CsUcsRollback -Identity "<user display name>"
    
    <span data-ttu-id="9dced-131">Exemple :</span><span class="sxs-lookup"><span data-stu-id="9dced-131">For example:</span></span>
    
        Invoke-CsUcsRollback -Identity "Ken Myer"
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="9dced-132">Nous vous déconseillons d’utiliser l’option – force pour forcer la restauration.</span><span class="sxs-lookup"><span data-stu-id="9dced-132">We do not recommend using the –Force option to force the rollback.</span></span> <span data-ttu-id="9dced-133">Si vous utilisez cette option, les contacts des utilisateurs seront perdus.</span><span class="sxs-lookup"><span data-stu-id="9dced-133">If you use this option, the users' contacts will be lost.</span></span>

    
    </div>

</div>

<div>

## <a name="to-roll-back-unified-contact-store-contacts-from-exchange-2013-to-lync-server-2013"></a><span data-ttu-id="9dced-134">Pour restaurer des contacts de magasin de contacts unifiés à partir d’Exchange 2013 vers Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9dced-134">To roll back unified contact store contacts from Exchange 2013 to Lync Server 2013</span></span>

1.  <span data-ttu-id="9dced-135">Démarrez Lync Server Management Shell : cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="9dced-135">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="9dced-136">Désactivez le magasin de contacts unifié pour que les utilisateurs soient restaurés de façon à ce qu’ils ne soient pas à nouveau migrés après la restauration.</span><span class="sxs-lookup"><span data-stu-id="9dced-136">Disable unified contact store for the users to be rolled back so that they will not be remigrated after rollback.</span></span> <span data-ttu-id="9dced-137">Pour désactiver le magasin de contacts unifié pour des utilisateurs individuels, sur la ligne de commande, tapez :</span><span class="sxs-lookup"><span data-stu-id="9dced-137">To disable unified contact store for individual users, at the command line, type:</span></span>
    
        Set-CsUserServicesPolicy -Identity "<policy name>" -UcsAllowed $False
    
    <span data-ttu-id="9dced-138">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="9dced-138">For example:</span></span>
    
        Set-CsUserServicesPolicy -Identity "UCS Enabled Users" -UcsAllowed $False

3.  <span data-ttu-id="9dced-139">Restaurez les utilisateurs spécifiés.</span><span class="sxs-lookup"><span data-stu-id="9dced-139">Roll back the specified users.</span></span> <span data-ttu-id="9dced-140">Dans la ligne de commande, tapez :</span><span class="sxs-lookup"><span data-stu-id="9dced-140">At the command line, type:</span></span>
    
        Invoke-CsUcsRollback -Identity "<user display name>"
    
    <span data-ttu-id="9dced-141">Exemple :</span><span class="sxs-lookup"><span data-stu-id="9dced-141">For example:</span></span>
    
        Invoke-CsUcsRollback -Identity "Ken Myer"
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="9dced-142">Vous devez d’abord restaurer l’utilisateur de Lync Server, puis déplacer la boîte aux lettres Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="9dced-142">You must first roll back the Lync Server user, and then move the Exchange 2013 mailbox.</span></span> <span data-ttu-id="9dced-143">L’administrateur Exchange ne peut pas restaurer Exchange tant que la restauration du serveur Lync n’est pas terminée.</span><span class="sxs-lookup"><span data-stu-id="9dced-143">The Exchange administrator is blocked from rolling back Exchange until the Lync Server rollback is complete.</span></span> <span data-ttu-id="9dced-144">Nous vous déconseillons d’utiliser l’option – force pour forcer la restauration.</span><span class="sxs-lookup"><span data-stu-id="9dced-144">We do not recommend using the –Force option to force the rollback.</span></span> <span data-ttu-id="9dced-145">Si vous utilisez cette option, les contacts des utilisateurs seront perdus.</span><span class="sxs-lookup"><span data-stu-id="9dced-145">If you use this option, the users' contacts will be lost.</span></span>

    
    </div>

4.  <span data-ttu-id="9dced-146">Après la restauration de l’utilisateur sur Lync Server, l’administrateur Exchange peut restaurer l’utilisateur Exchange à partir d’Exchange 2013 vers Exchange 2010.</span><span class="sxs-lookup"><span data-stu-id="9dced-146">After you roll back the user to Lync Server, the Exchange administrator can roll back the Exchange user from Exchange 2013 to Exchange 2010.</span></span>

<span data-ttu-id="9dced-147"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9dced-147"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

