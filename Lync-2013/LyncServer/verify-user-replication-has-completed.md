---
title: Vérifier que la réplication utilisateur est terminée
description: Vérifiez que la réplication des utilisateurs est terminée.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Verify user replication has completed
ms:assetid: 119e9896-45e5-4f8b-af43-7b09360ada0b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204680(v=OCS.15)
ms:contentKeyID: 48183441
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 60bca44fcce811c29b1633bd4d3a39f832851885
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446071"
---
# <a name="verify-user-replication-has-completed"></a><span data-ttu-id="4c75e-103">Vérifier que la réplication utilisateur est terminée</span><span class="sxs-lookup"><span data-stu-id="4c75e-103">Verify user replication has completed</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4c75e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4c75e-104">

<span> </span></span></span>

<span data-ttu-id="4c75e-105">_**Dernière modification de la rubrique :** 2012-09-17_</span><span class="sxs-lookup"><span data-stu-id="4c75e-105">_**Topic Last Modified:** 2012-09-17_</span></span>

<span data-ttu-id="4c75e-106">Lorsque vous exécutez l’applet de contrôle **Move-Csuser** , il est possible que vous constatiez un échec en raison du fait que les informations utilisateur entre les services de domaine Active Directory (AD DS) et celles de Lync Server 2013 ne sont pas synchronisées, car la réplication initiale est incomplète.</span><span class="sxs-lookup"><span data-stu-id="4c75e-106">When running the **Move-CsUser** cmdlet, you may experience a failure because user information between Active Directory Domain Services (AD DS) and the Lync Server 2013 databases are out of sync because the initial replication is incomplete.</span></span> <span data-ttu-id="4c75e-107">Le temps nécessaire à la réussite de la synchronisation initiale du service Réplicateur d’utilisateurs de Lync Server 2013 dépend du nombre de contrôleurs de domaine hébergés dans la forêt Active Directory qui héberge le pool 2013 Server.</span><span class="sxs-lookup"><span data-stu-id="4c75e-107">The time it takes for the successful completion of the Lync Server 2013 User Replicator service's initial synchronization depends on the number of domain controllers that are hosted in the Active Directory forest that hosts the Lync Server 2013 pool.</span></span> <span data-ttu-id="4c75e-108">Le processus de synchronisation initiale du service Réplicateur d’utilisateurs de Lync Server 2013 se produit lorsque le serveur frontal de Lync Server 2013 est démarré pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="4c75e-108">The Lync Server 2013 User Replicator service initial synchronization process occurs when the Lync Server 2013 Front End Server is started for the first time.</span></span> <span data-ttu-id="4c75e-109">Après cela, la synchronisation est alors basée sur l’intervalle du réplicateur d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="4c75e-109">After that, the synchronization is then based on the User Replicator interval.</span></span> <span data-ttu-id="4c75e-110">Suivez les étapes ci-dessous pour vérifier que la réplication des utilisateurs a abouti avant d’exécuter l’applet **de commande Move-Csuser** .</span><span class="sxs-lookup"><span data-stu-id="4c75e-110">Complete the following steps to verify user replication has completed before running the **Move-CsUser** cmdlet.</span></span>

<div>

## <a name="to-verify-user-replication-has-completed"></a><span data-ttu-id="4c75e-111">Pour vérifier la fin de la réplication des utilisateurs</span><span class="sxs-lookup"><span data-stu-id="4c75e-111">To verify user replication has completed</span></span>

1.  <span data-ttu-id="4c75e-112">Ouvrez une session sur l’ordinateur sur lequel le générateur de topologie est installé en tant que membre du groupe administrateurs de domaine et du groupe RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="4c75e-112">Log on to the computer where Topology Builder is installed as a member of the Domain Admins group and the RTCUniversalServerAdmins group.</span></span>

2.  <span data-ttu-id="4c75e-113">Cliquez sur le menu **Démarrer** , puis sur **exécuter**.</span><span class="sxs-lookup"><span data-stu-id="4c75e-113">Click the **Start** menu, and then click **Run**.</span></span>

3.  <span data-ttu-id="4c75e-114">Entrez **eventvwr.exe** puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c75e-114">Enter **eventvwr.exe** and then click **OK**.</span></span>

4.  <span data-ttu-id="4c75e-115">Dans l’observateur d’événements, cliquez sur **journaux des applications et des services** pour le développer, puis sélectionnez Lync Server.</span><span class="sxs-lookup"><span data-stu-id="4c75e-115">In Event Viewer, click **Applications and Services logs** to expand it, and then select Lync Server.</span></span>

5.  <span data-ttu-id="4c75e-116">Dans le volet **actions** , cliquez sur **filtrer le journal actuel**.</span><span class="sxs-lookup"><span data-stu-id="4c75e-116">In the **Actions** pane click **Filter Current Log**.</span></span>

6.  <span data-ttu-id="4c75e-117">Dans la liste **sources d’événements** , cliquez sur réplicateur d' **utilisateurs LS**.</span><span class="sxs-lookup"><span data-stu-id="4c75e-117">From the **Event sources** list, click **LS User Replicator**.</span></span>

7.  <span data-ttu-id="4c75e-118">Dans **\<All Event IDs\>** entrer **30024** , puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c75e-118">In **\<All Event IDs\>** enter **30024** and then click **OK**.</span></span>

8.  <span data-ttu-id="4c75e-119">Dans la liste des événements filtrés, sous l’onglet **général** , recherchez une entrée qui indique que la réplication des utilisateurs s’est déroulée correctement.</span><span class="sxs-lookup"><span data-stu-id="4c75e-119">In the filtered events list, on the **General** tab, look for an entry that states user replication has completed successfully.</span></span>

<span data-ttu-id="4c75e-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4c75e-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

