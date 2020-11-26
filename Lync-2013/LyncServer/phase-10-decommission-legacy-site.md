---
title: 'Étape 10 : désaffecter le site hérité'
description: 'Étape 10 : désaffecter le site hérité.'
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: 'Phase 10: Decommission legacy site'
ms:assetid: d591a310-3b5c-4092-b19e-0349616e40df
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205300(v=OCS.15)
ms:contentKeyID: 48185540
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9692301a1da38cfd69780ce2524f00dd428454e5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443271"
---
# <a name="phase-10-decommission-legacy-site"></a><span data-ttu-id="d8630-103">Étape 10 : désaffecter le site hérité</span><span class="sxs-lookup"><span data-stu-id="d8630-103">Phase 10: Decommission legacy site</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d8630-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d8630-104">

<span> </span></span></span>

<span data-ttu-id="d8630-105">_**Dernière modification de la rubrique :** 2012-10-16_</span><span class="sxs-lookup"><span data-stu-id="d8630-105">_**Topic Last Modified:** 2012-10-16_</span></span>

<span data-ttu-id="d8630-106">Les rubriques suivantes fournissent des recommandations en matière de mise en service de pools, et de désactivation et de suppression de serveurs et de pools à partir d’un déploiement hérité d’Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="d8630-106">The following topics provide guidance in decommissioning pools, and deactivating and removing servers and pools from a legacy deployment of Office Communications Server 2007 R2.</span></span> <span data-ttu-id="d8630-107">Toutes les procédures indiquées dans cette section ne sont pas obligatoires.</span><span class="sxs-lookup"><span data-stu-id="d8630-107">Not all of the procedures listed in this section are required.</span></span> <span data-ttu-id="d8630-108">Lisez les informations contenues dans ces rubriques pour déterminer la procédure de désactivation à utiliser.</span><span class="sxs-lookup"><span data-stu-id="d8630-108">Read the information in each of these topics to determine which decommissioning procedure to use.</span></span>

<div>


> [!WARNING]  
> <span data-ttu-id="d8630-109">Si vous avez importé des annuaires de conférences pour les conférences rendez-vous sur Lync Server 2013, il est important de basculer la propriété de l’annuaire de conférences vers Lync Server 2013 avant de commencer à mettre vos pools en service.</span><span class="sxs-lookup"><span data-stu-id="d8630-109">If you imported conference directories for dial-in conferencing to Lync Server 2013, it is important to transition conference directory ownership to Lync Server 2013 before you begin to decommission your pools.</span></span> <span data-ttu-id="d8630-110">Si vous désorganisez un pool sans avoir préalablement transféré la propriété de l’annuaire de conférences, la fonctionnalité de connexion à toutes les réunions migrées ne fonctionnera plus.</span><span class="sxs-lookup"><span data-stu-id="d8630-110">If you decommission a pool without first transitioning conference directory ownership, the dial-in feature for all migrated meetings will no longer work.</span></span> <span data-ttu-id="d8630-111">Vous devez effectuer cette étape pour une transition de propriété unique pour chaque annuaire de conférences de votre pool hérité.</span><span class="sxs-lookup"><span data-stu-id="d8630-111">You must perform the step to transition ownership once for each conference directory in your legacy pool.</span></span>



</div>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="d8630-112">Pour plus d’informations sur la migration et la mise à niveau des applications UCMA (Unified Communications Managed API), avant de désaffecter votre environnement hérité, voir <A href="https://go.microsoft.com/fwlink/p/?linkid=269555">https://go.microsoft.com/fwlink/p/?LinkId=269555</A></span><span class="sxs-lookup"><span data-stu-id="d8630-112">For information on migrating and upgrading Microsoft Unified Communications Managed API (UCMA) applications, prior to decommissioning your legacy environment, see <A href="https://go.microsoft.com/fwlink/p/?linkid=269555">https://go.microsoft.com/fwlink/p/?LinkId=269555</A></span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="d8630-113">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="d8630-113">In This Section</span></span>

  - [<span data-ttu-id="d8630-114">Déplacer des répertoires de conférences</span><span class="sxs-lookup"><span data-stu-id="d8630-114">Move conference directories</span></span>](move-conference-directories.md)

  - [<span data-ttu-id="d8630-115">Mettre à jour les enregistrements SRV DNS</span><span class="sxs-lookup"><span data-stu-id="d8630-115">Update DNS SRV records</span></span>](update-dns-srv-records.md)

  - [<span data-ttu-id="d8630-116">Désaffectation de serveurs et de pools</span><span class="sxs-lookup"><span data-stu-id="d8630-116">Decommissioning servers and pools</span></span>](decommissioning-servers-and-pools.md)

  - [<span data-ttu-id="d8630-117">Supprimer BackCompatSite</span><span class="sxs-lookup"><span data-stu-id="d8630-117">Remove BackCompatSite</span></span>](remove-backcompatsite.md)

<span data-ttu-id="d8630-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d8630-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

