---
title: 'Lync Server 2013 : configuration des autorisations pour l’archivage'
description: 'Lync Server 2013 : configuration des autorisations d’archivage.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up permissions for Archiving
ms:assetid: 67f97c94-52f5-4a83-a35c-8c307d5de9a4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204961(v=OCS.15)
ms:contentKeyID: 48184364
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1f06c4fb48772a41621ece765dcc90555f0cd2d5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395065"
---
# <a name="setting-up-permissions-for-archiving-in-lync-server-2013"></a><span data-ttu-id="3c80e-103">Configuration des autorisations d’archivage dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3c80e-103">Setting up permissions for Archiving in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3c80e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3c80e-104">

<span> </span></span></span>

<span data-ttu-id="3c80e-105">_**Dernière modification de la rubrique :** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="3c80e-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="3c80e-106">Dans Lync Server 2013, les tâches spécifiques requièrent toujours que les utilisateurs qui effectuent ces tâches soient membres d’un ou plusieurs groupes spécifiques.</span><span class="sxs-lookup"><span data-stu-id="3c80e-106">In Lync Server 2013, specific tasks still require that users who perform those tasks be members of one or more specific groups.</span></span> <span data-ttu-id="3c80e-107">Toutefois, vous pouvez également utiliser le contrôle d’accès basé sur les rôles (RBAC) pour octroyer des privilèges en attribuant aux utilisateurs des rôles d’administrateur de Lync Server prédéfinis. Avant de déployer l’archivage, assurez-vous que les droits d’utilisateur et les autorisations appropriés sont en place, et que tous les utilisateurs auxquels vous voulez attribuer un rôle RBAC spécifique ont été attribués à ce rôle.</span><span class="sxs-lookup"><span data-stu-id="3c80e-107">However, you can also use role-based access control (RBAC) to grant privileges by assigning users to predefined Lync Server administrative roles.Before you deploy Archiving, be sure that the appropriate user rights and permissions are in place, and that any users who you want to assign to a specific RBAC role have been assigned to that role.</span></span> <span data-ttu-id="3c80e-108">Pour plus d’informations sur les droits d’utilisateur, les autorisations et les rôles pour le déploiement de la prise en charge de l’archivage, voir [liste de vérification de déploiement pour l’archivage dans Lync Server 2013](lync-server-2013-deployment-checklist-for-archiving.md), qui est disponible dans la documentation de planification et la documentation de déploiement.</span><span class="sxs-lookup"><span data-stu-id="3c80e-108">For details about the user rights, permissions, and roles for deploying support for Archiving, see [Deployment checklist for Archiving in Lync Server 2013](lync-server-2013-deployment-checklist-for-archiving.md), which is available in the Planning documentation and the Deployment documentation.</span></span> <span data-ttu-id="3c80e-109">Pour plus d’informations sur le contrôle RBAC, voir [planification du contrôle d’accès basé sur un rôle dans Lync Server 2013](lync-server-2013-planning-for-role-based-access-control.md) dans la documentation de planification.</span><span class="sxs-lookup"><span data-stu-id="3c80e-109">For details about RBAC, see [Planning for role-based access control in Lync Server 2013](lync-server-2013-planning-for-role-based-access-control.md) in the Planning documentation.</span></span>

<span data-ttu-id="3c80e-110"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3c80e-110"></div>

<span> </span>

</div>

</div>

</span></span></div>

