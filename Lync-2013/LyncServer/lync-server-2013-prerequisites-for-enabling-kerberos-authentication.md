---
title: 'Lync Server 2013 : Conditions prérequises à l’activation de l’authentification Kerberos'
description: 'Lync Server 2013 : conditions préalables à l’activation de l’authentification Kerberos.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Prerequisites for enabling Kerberos authentication
ms:assetid: 3f276a21-7476-4bc0-9fd1-59e844d2e9c1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425909(v=OCS.15)
ms:contentKeyID: 48183945
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 65a45bad0eb249fdbc717fe05f080ce737c87c6f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436971"
---
# <a name="prerequisites-for-enabling-kerberos-authentication-in-lync-server-2013"></a><span data-ttu-id="12277-103">Conditions prérequises à l’activation de l’authentification Kerberos dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="12277-103">Prerequisites for enabling Kerberos authentication in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="12277-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="12277-104">

<span> </span></span></span>

<span data-ttu-id="12277-105">_**Dernière modification de la rubrique :** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="12277-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="12277-106">Avant d’activer l’authentification Kerberos, assurez-vous d’avoir effectué toutes les préparations de configuration et d’infrastructure prérequises :</span><span class="sxs-lookup"><span data-stu-id="12277-106">Before enabling Kerberos authentication, make sure that you complete all prerequisite configuration and infrastructure preparations:</span></span>

  - <span data-ttu-id="12277-107">Le schéma Active Directory est étendu pour Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="12277-107">Active Directory schema is extended for Lync Server 2013.</span></span>

  - <span data-ttu-id="12277-108">La préparation de la forêt Active Directory est terminée pour Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="12277-108">Active Directory forest preparation is completed for Lync Server 2013.</span></span>

  - <span data-ttu-id="12277-109">La préparation du domaine Active Directory est terminée pour Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="12277-109">Active Directory domain preparation is completed for Lync Server 2013.</span></span>

  - <span data-ttu-id="12277-110">Le centre de gestion central est correctement installé et disponible.</span><span class="sxs-lookup"><span data-stu-id="12277-110">Central Management store is successfully installed and available.</span></span>

  - <span data-ttu-id="12277-111">Le module topologique a été créé et publié à l’aide du générateur de topologie.</span><span class="sxs-lookup"><span data-stu-id="12277-111">The topology has been created and published by using Topology Builder.</span></span>

  - <span data-ttu-id="12277-112">Les serveurs et rôles nécessitant la définition et le déploiement de services Web, notamment les serveurs front end, les serveurs Standard Edition et les directeurs.</span><span class="sxs-lookup"><span data-stu-id="12277-112">Servers and roles that require Web Services have been defined and deployed, including Front End Servers, Standard Edition servers, and Directors.</span></span>

  - <span data-ttu-id="12277-113">Internet Information Services (IIS) est configuré et déployé avec les services de rôle recommandés pour prendre en charge les services Web dans Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="12277-113">Internet Information Services (IIS) is configured and deployed with the recommended role services to support Web Services in Lync Server 2013.</span></span>

<span data-ttu-id="12277-114">Lorsque les conditions préalables sont remplies, vous devez être prêt à créer un ou plusieurs comptes pour les services Web à utiliser pour l’authentification Kerberos pour votre déploiement.</span><span class="sxs-lookup"><span data-stu-id="12277-114">After the prerequisites have been met, you should be ready to create one or more accounts for Web Services to use for Kerberos authentication for your deployment.</span></span> <span data-ttu-id="12277-115">Au minimum, vous devez créer un compte d’authentification Kerberos pour chaque déploiement.</span><span class="sxs-lookup"><span data-stu-id="12277-115">At a minimum, you need to create one Kerberos authentication account for each deployment.</span></span> <span data-ttu-id="12277-116">Toutefois, vous pouvez créer un compte pour chaque site afin de fournir une authentification Kerberos locale sur le site.</span><span class="sxs-lookup"><span data-stu-id="12277-116">However, you can create an account for each site to provide local Kerberos authentication at the site.</span></span> <span data-ttu-id="12277-117">Vous ne pouvez spécifier qu’un seul compte d’authentification Kerberos par site.</span><span class="sxs-lookup"><span data-stu-id="12277-117">You can only specify one Kerberos authentication account per site.</span></span>

<span data-ttu-id="12277-118"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="12277-118"></div>

<span> </span>

</div>

</div>

</span></span></div>

