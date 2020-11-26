---
title: 'Lync Server 2013 : Préparation des services de domaine Active Directory verrouillés'
description: 'Lync Server 2013 : préparation d’un service de domaine Active Directory (AD FS) verrouillé.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Preparing a locked-down Active Directory Domain Services
ms:assetid: 68bde963-3fa3-4102-88d6-ac931c1dd2d7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398492(v=OCS.15)
ms:contentKeyID: 48184377
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4aea04b138de2630935713eda7cbef9e4d21572a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424225"
---
# <a name="preparing-a-locked-down-active-directory-domain-services-in-lync-server-2013"></a><span data-ttu-id="6e62b-103">Préparation des services de domaine Active Directory verrouillés dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6e62b-103">Preparing a locked-down Active Directory Domain Services in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6e62b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6e62b-104">

<span> </span></span></span>

<span data-ttu-id="6e62b-105">_**Dernière modification de la rubrique :** 2012-05-14_</span><span class="sxs-lookup"><span data-stu-id="6e62b-105">_**Topic Last Modified:** 2012-05-14_</span></span>

<span data-ttu-id="6e62b-106">Les organisations verrouillent souvent les services de domaine Active Directory pour réduire les risques liés à la sécurité.</span><span class="sxs-lookup"><span data-stu-id="6e62b-106">Organizations often lock down Active Directory Domain Services to help mitigate security risks.</span></span> <span data-ttu-id="6e62b-107">Toutefois, un environnement Active Directory verrouillé peut limiter les autorisations requises par Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6e62b-107">However, a locked-down Active Directory environment can limit the permissions that Lync Server 2013 requires.</span></span> <span data-ttu-id="6e62b-108">La préparation correcte d’un environnement Active Directory verrouillé pour Lync Server 2013 implique quelques considérations et étapes supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="6e62b-108">Properly preparing a locked-down Active Directory environment for Lync Server 2013 involves some additional considerations and steps.</span></span>

<span data-ttu-id="6e62b-109">Il existe deux méthodes courantes pour lesquelles les autorisations sont limitées dans un environnement Active Directory verrouillé :</span><span class="sxs-lookup"><span data-stu-id="6e62b-109">Two common ways in which permissions are limited in a locked-down Active Directory environment are as follows:</span></span>

  - <span data-ttu-id="6e62b-110">Les entrées de contrôle d’accès des utilisateurs authentifiées (ACE) sont supprimées des conteneurs.</span><span class="sxs-lookup"><span data-stu-id="6e62b-110">Authenticated user access control entries (ACEs) are removed from containers.</span></span>

  - <span data-ttu-id="6e62b-111">L’héritage des autorisations est désactivé sur les conteneurs d’objets utilisateur, de contact, de InetOrgPerson ou d’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="6e62b-111">Permissions inheritance is disabled on containers of User, Contact, InetOrgPerson, or Computer objects.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="6e62b-112">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="6e62b-112">In This Section</span></span>

  - [<span data-ttu-id="6e62b-113">Suppression des autorisations d’utilisateur authentifié dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6e62b-113">Authenticated user permissions are removed in Lync Server 2013</span></span>](lync-server-2013-authenticated-user-permissions-are-removed.md)

  - [<span data-ttu-id="6e62b-114">Désactivation de l’héritage des autorisations sur les conteneurs des objets Ordinateur, Utilisateur ou InetOrgPerson dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6e62b-114">Permissions inheritance Is disabled on computers, users, or InetOrgPerson containers in Lync Server 2013</span></span>](lync-server-2013-permissions-inheritance-is-disabled-on-computers-users-or-inetorgperson-containers.md)

<span data-ttu-id="6e62b-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6e62b-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

