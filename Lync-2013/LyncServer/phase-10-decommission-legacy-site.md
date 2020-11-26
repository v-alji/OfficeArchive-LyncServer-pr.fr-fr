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
# <a name="phase-10-decommission-legacy-site"></a>Étape 10 : désaffecter le site hérité

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2012-10-16_

Les rubriques suivantes fournissent des recommandations en matière de mise en service de pools, et de désactivation et de suppression de serveurs et de pools à partir d’un déploiement hérité d’Office Communications Server 2007 R2. Toutes les procédures indiquées dans cette section ne sont pas obligatoires. Lisez les informations contenues dans ces rubriques pour déterminer la procédure de désactivation à utiliser.

<div>


> [!WARNING]  
> Si vous avez importé des annuaires de conférences pour les conférences rendez-vous sur Lync Server 2013, il est important de basculer la propriété de l’annuaire de conférences vers Lync Server 2013 avant de commencer à mettre vos pools en service. Si vous désorganisez un pool sans avoir préalablement transféré la propriété de l’annuaire de conférences, la fonctionnalité de connexion à toutes les réunions migrées ne fonctionnera plus. Vous devez effectuer cette étape pour une transition de propriété unique pour chaque annuaire de conférences de votre pool hérité.



</div>

<div>


> [!IMPORTANT]  
> Pour plus d’informations sur la migration et la mise à niveau des applications UCMA (Unified Communications Managed API), avant de désaffecter votre environnement hérité, voir <A href="https://go.microsoft.com/fwlink/p/?linkid=269555">https://go.microsoft.com/fwlink/p/?LinkId=269555</A>



</div>

<div>

## <a name="in-this-section"></a>Dans cette section

  - [Déplacer des répertoires de conférences](move-conference-directories.md)

  - [Mettre à jour les enregistrements SRV DNS](update-dns-srv-records.md)

  - [Désaffectation de serveurs et de pools](decommissioning-servers-and-pools.md)

  - [Supprimer BackCompatSite](remove-backcompatsite.md)

</div>

</div>

<span> </span>

</div>

</div>

</div>

