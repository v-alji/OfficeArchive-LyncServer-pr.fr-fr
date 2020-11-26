---
title: Supprimer BackCompatSite
description: Supprimer BackCompatSite.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Remove BackCompatSite
ms:assetid: 039650e3-541b-45c2-a682-c4fa08423118
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204637(v=OCS.15)
ms:contentKeyID: 48183265
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 809324320ec1869ac0c9d324b8fc270a3cf8f174
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440298"
---
# <a name="remove-backcompatsite"></a><span data-ttu-id="cc748-103">Supprimer BackCompatSite</span><span class="sxs-lookup"><span data-stu-id="cc748-103">Remove BackCompatSite</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cc748-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cc748-104">

<span> </span></span></span>

<span data-ttu-id="cc748-105">_**Dernière modification de la rubrique :** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="cc748-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="cc748-106">Une fois que tous les pools ont été désactivés et que tous les serveurs Edge ont été désinstallés, exécutez l’Assistant Fusion du générateur de topologie pour supprimer **BackCompatSite**.</span><span class="sxs-lookup"><span data-stu-id="cc748-106">After all pools are deactivated and all Edge Servers have been uninstalled, run the Topology Builder Merge wizard to remove the **BackCompatSite**.</span></span>

<div>

## <a name="to-remove-backcompat-site-from-topology-builder"></a><span data-ttu-id="cc748-107">Pour supprimer le site de recompatibilité dans le générateur de topologie</span><span class="sxs-lookup"><span data-stu-id="cc748-107">To remove BackCompat site from Topology Builder</span></span>

1.  <span data-ttu-id="cc748-108">Ouvrez un déploiement existant à partir du générateur de topologie.</span><span class="sxs-lookup"><span data-stu-id="cc748-108">Open an existing deployment from Topology Builder.</span></span>

2.  <span data-ttu-id="cc748-109">Dans le menu **action** , cliquez sur **fusionner la topologie 2007 R2**.</span><span class="sxs-lookup"><span data-stu-id="cc748-109">In the **Action** menu, click **Merge 2007 R2 Topology**.</span></span>

3.  <span data-ttu-id="cc748-110">Cliquez sur **Suivant** pour continuer.</span><span class="sxs-lookup"><span data-stu-id="cc748-110">Click **Next** to continue.</span></span>

4.  <span data-ttu-id="cc748-111">Dans la page **spécifier le bord hérité** , assurez-vous que la liste des serveurs Edge est vide.</span><span class="sxs-lookup"><span data-stu-id="cc748-111">On the **Specify Legacy Edge** page, ensure that list of Edge Servers is empty.</span></span> <span data-ttu-id="cc748-112">S’il ne s’agit pas de la liste, appuyez sur le bouton **supprimer** pour supprimer tous les serveurs de périphérie hérités, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="cc748-112">If the list is not empty, use the **Remove** button to remove all the legacy Edge Servers, and then click **Next**.</span></span>
    
    <span data-ttu-id="cc748-113">![Assistant Fusion-topologie-définir la page de configuration du bord](images/JJ204637.fb35a59a-711e-4259-b177-7311df1fed3c(OCS.15).jpg "Assistant Fusion-topologie-définir la page de configuration du bord")</span><span class="sxs-lookup"><span data-stu-id="cc748-113">![Merge Topology Wizard, Specify Edge Setup page](images/JJ204637.fb35a59a-711e-4259-b177-7311df1fed3c(OCS.15).jpg "Merge Topology Wizard, Specify Edge Setup page")</span></span>  

5.  <span data-ttu-id="cc748-114">Dans la page **Specify Internal SIP port Setting** , cliquez sur **Next (suivant**).</span><span class="sxs-lookup"><span data-stu-id="cc748-114">On the **Specify Internal SIP port setting** page, click **Next**.</span></span>

6.  <span data-ttu-id="cc748-115">Dans la page **Résumé** , cliquez sur **suivant** pour commencer à fusionner les topologies afin de supprimer le site hérité.</span><span class="sxs-lookup"><span data-stu-id="cc748-115">On the **Summary** page, click **Next** to begin merging the topologies to remove the legacy site.</span></span>

7.  <span data-ttu-id="cc748-116">Dans la colonne **État** , assurez-vous que la valeur est **succès** , puis cliquez sur **Terminer** pour fermer l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="cc748-116">In the **Status** column, verify that the value is **Success** and then click **Finish** to close the wizard.</span></span>

8.  <span data-ttu-id="cc748-117">Dans le volet gauche du générateur de topologie, développez le BackCompatSite et assurez-vous qu’aucun serveur n’est répertorié.</span><span class="sxs-lookup"><span data-stu-id="cc748-117">In the left pane of Topology Builder, expand the BackCompatSite and ensure no servers are listed.</span></span>

9.  <span data-ttu-id="cc748-118">Cliquez avec le bouton droit sur le **BackCompatSite**, puis cliquez sur **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="cc748-118">Right-click the **BackCompatSite**, and then click **Delete**.</span></span>

10. <span data-ttu-id="cc748-119">Dans **Générateur de topologie**, sélectionnez le **serveur Lync** le plus en tête de nœud.</span><span class="sxs-lookup"><span data-stu-id="cc748-119">In **Topology Builder**, select the top-most node **Lync Server**.</span></span>

11. <span data-ttu-id="cc748-120">Dans le menu **action** , sélectionnez la **topologie de publication** , puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="cc748-120">From the **Action** menu, select **Publish Topology** and then click **Next**.</span></span>

12. <span data-ttu-id="cc748-121">Lorsque l' **Assistant Publication** est terminé, cliquez sur **Terminer** pour fermer l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="cc748-121">When the **Publishing wizard** completes, click **Finish** to close the wizard.</span></span>

<span data-ttu-id="cc748-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cc748-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

