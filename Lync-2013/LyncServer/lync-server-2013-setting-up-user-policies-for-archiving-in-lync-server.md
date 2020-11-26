---
title: 'Lync Server 2013 : configuration de stratégies utilisateur pour l’archivage dans Lync Server'
description: 'Lync Server 2013 : configuration de stratégies utilisateur pour l’archivage dans Lync Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up user policies for Archiving in Lync Server
ms:assetid: 22d6cc76-6b5c-4a8c-bb8a-7996450ec085
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204742(v=OCS.15)
ms:contentKeyID: 48183626
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9e33abf6cf16c9c1367162aa8beee91874f4c725
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441626"
---
# <a name="setting-up-user-policies-for-archiving-in-lync-server-2013"></a><span data-ttu-id="95c74-103">Configuration de stratégies utilisateur pour l’archivage dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="95c74-103">Setting up user policies for Archiving in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="95c74-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="95c74-104">

<span> </span></span></span>

<span data-ttu-id="95c74-105">_**Dernière modification de la rubrique :** 2012-10-10_</span><span class="sxs-lookup"><span data-stu-id="95c74-105">_**Topic Last Modified:** 2012-10-10_</span></span>

<span data-ttu-id="95c74-106">L’activation ou la désactivation de l’archivage pour des utilisateurs spécifiques hébergés sur Lync Server 2013 nécessite la création et la configuration d’une ou plusieurs stratégies utilisateur, puis l’application de la stratégie appropriée à des utilisateurs ou groupes d’utilisateurs spécifiques.</span><span class="sxs-lookup"><span data-stu-id="95c74-106">Enabling or disabling Archiving for specific users homed on Lync Server 2013 requires creating and configuring one or more user policies, and then applying the appropriate policy to specific users or user groups.</span></span> <span data-ttu-id="95c74-107">Les stratégies utilisateur remplacent les stratégies de site et globales, mais uniquement pour les utilisateurs hébergés sur Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="95c74-107">User policies override site and global policies, but only for users homed on Lync Server 2013.</span></span>

<span data-ttu-id="95c74-108">Les utilisateurs sont toujours hébergés sur Lync Server.</span><span class="sxs-lookup"><span data-stu-id="95c74-108">Users are always homed in Lync Server.</span></span> <span data-ttu-id="95c74-109">Si l’intégration de Microsoft Exchange est activée, les utilisateurs dont les boîtes aux lettres se trouvent dans Microsoft Exchange Server 2013 n’ont pas besoin d’avoir leurs stratégies d’archivage dans le gestion de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="95c74-109">If Microsoft Exchange integration is enabled, users whose mailboxes are in Microsoft Exchange Server 2013 don’t need to have their Archiving policies in Lync Server managed.</span></span> <span data-ttu-id="95c74-110">Ces utilisateurs dotés de l’archivage seront gérés par Exchange In-Place attente.</span><span class="sxs-lookup"><span data-stu-id="95c74-110">These users with Archiving will be managed by Exchange In-Place Hold.</span></span>

<span data-ttu-id="95c74-111">Pour plus d’informations sur le fonctionnement des stratégies d’archivage, y compris la hiérarchie des stratégies globales, de site et d’utilisateur, voir fonctionnement [de l’archivage dans Lync Server 2013](lync-server-2013-how-archiving-works.md) dans la documentation de planification, la documentation de déploiement ou les opérations.</span><span class="sxs-lookup"><span data-stu-id="95c74-111">For details about how Archiving policies work, including the hierarchy for global, site, and user policies, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) in the Planning documentation, Deployment documentation, or Operations documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="95c74-112">Si vous avez activé l’intégration de Microsoft Exchange pour votre déploiement, les stratégies de blocage d' In-Place Exchange contrôlent l’activation de l’archivage pour les utilisateurs hébergés sur Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="95c74-112">If you enabled Microsoft Exchange integration for your deployment, Exchange In-Place Hold policies control whether archiving is enabled for the users who are homed on Exchange 2013.</span></span> <span data-ttu-id="95c74-113">Pour ces utilisateurs, les boîtes aux lettres doivent être placées dans In-Place attente.</span><span class="sxs-lookup"><span data-stu-id="95c74-113">Archiving for these users requires that they have their mailboxes put on In-Place Hold.</span></span> <span data-ttu-id="95c74-114">Pour plus d’informations, reportez-vous à la rubrique <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">configuration de stratégies d’archivage dans Lync server 2013 lors de l’utilisation d’une intégration Exchange Server</A> dans la documentation de déploiement.</span><span class="sxs-lookup"><span data-stu-id="95c74-114">For details, see <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Setting up policies for Archiving in Lync Server 2013 when using Exchange Server integration</A> in the Deployment documentation.</span></span><BR><span data-ttu-id="95c74-115">Vous devez spécifier toutes les options appropriées dans les configurations d’archivage avant de procéder à l’archivage.</span><span class="sxs-lookup"><span data-stu-id="95c74-115">You should specify all appropriate options in the Archiving configurations before enabling Archiving.</span></span> <span data-ttu-id="95c74-116">Pour plus d’informations, reportez-vous à <A href="lync-server-2013-configuring-archiving-options.md">Configuration des options d’archivage dans Lync Server 2013</A> dans la documentation de déploiement.</span><span class="sxs-lookup"><span data-stu-id="95c74-116">For details, see <A href="lync-server-2013-configuring-archiving-options.md">Configuring Archiving options in Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="95c74-117">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="95c74-117">In This Section</span></span>

  - [<span data-ttu-id="95c74-118">Création et configuration des stratégies utilisateur pour l’archivage dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="95c74-118">Creating and configuring user policies for Archiving in Lync Server 2013</span></span>](lync-server-2013-creating-and-configuring-user-policies-for-archiving-in-lync-server.md)

  - [<span data-ttu-id="95c74-119">Appliquer une stratégie d’archivage Lync Server à un utilisateur dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="95c74-119">Applying a Lync Server Archiving policy to a user in Lync Server 2013</span></span>](lync-server-2013-applying-a-lync-server-archiving-policy-to-a-user.md)

<span data-ttu-id="95c74-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="95c74-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

