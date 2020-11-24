---
title: 'Lync Server 2013 : Déploiement d’un magasin de contacts unifié'
description: 'Lync Server 2013 : déploiement d’un magasin de contacts unifié'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying unified contact store
ms:assetid: 68959d58-ac8a-45de-afcd-b9de2c36799c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204963(v=OCS.15)
ms:contentKeyID: 48184373
ms.date: 06/06/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 056792d2e4ea66699b276d0d571e83c8a0256483
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49393985"
---
# <a name="deploying-unified-contact-store-in-lync-server-2013"></a><span data-ttu-id="bc685-103">Déploiement d’un magasin de contacts unifié dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bc685-103">Deploying unified contact store in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bc685-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bc685-104">

<span> </span></span></span>

<span data-ttu-id="bc685-105">_**Dernière modification de la rubrique :** 2016-06-06_</span><span class="sxs-lookup"><span data-stu-id="bc685-105">_**Topic Last Modified:** 2016-06-06_</span></span>

<span data-ttu-id="bc685-106">L’activation d’un magasin de contacts unifié dans Lync Server 2013 ne nécessite aucun paramètre de topologie.</span><span class="sxs-lookup"><span data-stu-id="bc685-106">Enabling unified contact store in Lync Server 2013 does not require any topology settings.</span></span> <span data-ttu-id="bc685-107">L’activation du magasin de contacts unifié pour les utilisateurs nécessite ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="bc685-107">Enabling unified contact store for users requires the following:</span></span>

  - <span data-ttu-id="bc685-108">La stratégie du magasin de contacts unifié est activée (par défaut).</span><span class="sxs-lookup"><span data-stu-id="bc685-108">Unified contact store policy is enabled (default is enabled).</span></span>

  - <span data-ttu-id="bc685-109">Les utilisateurs se connectent avec Lync 2013 au moins une fois.</span><span class="sxs-lookup"><span data-stu-id="bc685-109">Users log in with Lync 2013 at least once.</span></span>

<span data-ttu-id="bc685-110">Après la migration des contacts d’un utilisateur, ce qui se produit automatiquement lorsqu’un utilisateur se connecte à l’aide de Lync 2013, l’utilisateur peut accéder et gérer ses contacts Lync à partir de Lync 2013, Outlook 2013 ou Outlook Web Access.</span><span class="sxs-lookup"><span data-stu-id="bc685-110">After a user’s contacts have been migrated, which happens automatically when a user logs in with Lync 2013, the user can access and manage their Lync contacts from Lync 2013, Outlook 2013, or Outlook Web Access.</span></span> <span data-ttu-id="bc685-111">L’utilisateur n’a pas besoin d’être connecté à Lync pour gérer ses contacts à partir d’Outlook ou d’Outlook Web Access.</span><span class="sxs-lookup"><span data-stu-id="bc685-111">The user does not have to be logged in to Lync to manage their contacts from Outlook or Outlook Web Access.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="bc685-112">Si un utilisateur se connecte à partir de Lync 2010 après la migration, les contacts et les groupes sont disponibles et à jour, mais l’utilisateur ne peut pas gérer (c’est-à-dire ajouter, supprimer, déplacer, marquer, supprimer ou modifier) ces contacts.</span><span class="sxs-lookup"><span data-stu-id="bc685-112">If a user logs in from Lync 2010 after migration, contacts and groups are available and up-to-date, but the user cannot manage (that is, add, delete, move, tag, untag, or modify) those contacts.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="bc685-113">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="bc685-113">In This Section</span></span>

  - [<span data-ttu-id="bc685-114">Activation des utilisateurs pour le magasin de contacts unifié dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bc685-114">Enable users for unified contact store in Lync Server 2013</span></span>](lync-server-2013-enable-users-for-unified-contact-store.md)

  - [<span data-ttu-id="bc685-115">Migration des utilisateurs vers le magasin de contacts unifié dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bc685-115">Migrate users to unified contact store in Lync Server 2013</span></span>](lync-server-2013-migrate-users-to-unified-contact-store.md)

  - [<span data-ttu-id="bc685-116">Restauration des utilisateurs migrés dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bc685-116">Roll back migrated users in Lync Server 2013</span></span>](lync-server-2013-roll-back-migrated-users.md)

<span data-ttu-id="bc685-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bc685-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

