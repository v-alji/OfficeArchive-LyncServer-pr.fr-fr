---
title: 'Lync Server 2013 : Configuration de conférences rendez-vous'
description: 'Lync Server 2013 : configuration de conférences rendez-vous.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring dial-in conferencing
ms:assetid: 79a98c5d-a0a8-4729-828d-b9166842432c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398600(v=OCS.15)
ms:contentKeyID: 48184587
ms.date: 10/03/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d9c3353caa1344b717b0f64c271149f078f194e5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433205"
---
# <a name="configuring-dial-in-conferencing-in-lync-server-2013"></a><span data-ttu-id="a3b54-103">Configuration de conférences rendez-vous dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a3b54-103">Configuring dial-in conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a3b54-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a3b54-104">

<span> </span></span></span>

<span data-ttu-id="a3b54-105">_**Dernière modification de la rubrique :** 2014-10-03_</span><span class="sxs-lookup"><span data-stu-id="a3b54-105">_**Topic Last Modified:** 2014-10-03_</span></span>

<span data-ttu-id="a3b54-106">Cette section vous guide dans la configuration de la Conférence rendez-vous Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a3b54-106">This section guides you through the configuration of Lync Server 2013 dial-in conferencing.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="a3b54-107">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="a3b54-107">In This Section</span></span>

  - [<span data-ttu-id="a3b54-108">Configuration requise et autorisations pour la configuration de conférence rendez-vous dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a3b54-108">Dial-in conferencing configuration prerequisites and permissions in Lync Server 2013</span></span>](lync-server-2013-dial-in-conferencing-configuration-prerequisites-and-permissions.md)

  - [<span data-ttu-id="a3b54-109">Liste de vérification du déploiement pour la conférence rendez-vous dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a3b54-109">Deployment checklist for dial-in conferencing in Lync Server 2013</span></span>](lync-server-2013-deployment-checklist-for-dial-in-conferencing.md)

  - [<span data-ttu-id="a3b54-110">Configuration des plans de numérotation pour les conférences rendez-vous dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a3b54-110">Configure dial plans for dial-in conferencing in Lync Server 2013</span></span>](lync-server-2013-configure-dial-plans-for-dial-in-conferencing.md)

  - [<span data-ttu-id="a3b54-111">Vérifier que le plan de numérotation Lync Server 2013 a des régions affectées</span><span class="sxs-lookup"><span data-stu-id="a3b54-111">Make sure dial plans Lync Server 2013 have assigned regions</span></span>](lync-server-2013-make-sure-dial-plans-have-assigned-regions.md)

  - [<span data-ttu-id="a3b54-112">(Facultatif) Vérification des paramètres de stratégie de code confidentiel dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a3b54-112">(Optional) Verify PIN policy settings in Lync Server 2013</span></span>](lync-server-2013-optional-verify-pin-policy-settings.md)

  - [<span data-ttu-id="a3b54-113">Configuration de la stratégie de conférence rendez-vous dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a3b54-113">Configure conferencing policy for dial-in in Lync Server 2013</span></span>](lync-server-2013-configure-conferencing-policy-for-dial-in.md)

  - [<span data-ttu-id="a3b54-114">Configuration des numéros d’accès aux conférences rendez-vous dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a3b54-114">Configure dial-in conferencing access numbers in Lync Server 2013</span></span>](lync-server-2013-configure-dial-in-conferencing-access-numbers.md)

  - [<span data-ttu-id="a3b54-115">(Facultatif) Vérification des paramètres de conférence rendez-vous dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a3b54-115">(Optional) Verify dial-in conferencing settings in Lync Server 2013</span></span>](lync-server-2013-optional-verify-dial-in-conferencing-settings.md)

  - [<span data-ttu-id="a3b54-116">(Facultatif) Modification du mappage des clés des commandes DTMF dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a3b54-116">(Optional) Modify key mapping for DTMF commands in Lync Server 2013</span></span>](lync-server-2013-optional-modify-key-mapping-for-dtmf-commands.md)

  - [<span data-ttu-id="a3b54-117">(Facultatif) Activation et désactivation des annonces indiquant qu’un utilisateur rejoint ou quitte une conférence dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a3b54-117">(Optional) Enable and disable conference join and leave announcements in Lync Server 2013</span></span>](lync-server-2013-optional-enable-and-disable-conference-join-and-leave-announcements.md)

  - [<span data-ttu-id="a3b54-118">(Facultatif) Vérification de la conférence rendez-vous dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a3b54-118">(Optional) Verify dial-in conferencing in Lync Server 2013</span></span>](lync-server-2013-optional-verify-dial-in-conferencing.md)

  - [<span data-ttu-id="a3b54-119">Déploiement du complément de réunion en ligne pour Lync 2013</span><span class="sxs-lookup"><span data-stu-id="a3b54-119">Deploy the Online Meeting Add-in for Lync 2013</span></span>](lync-server-2013-deploy-the-online-meeting-add-in-for-lync-2013.md)

  - [<span data-ttu-id="a3b54-120">Configuration des paramètres des comptes d’utilisateurs dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a3b54-120">Configure user account settings in Lync Server 2013</span></span>](lync-server-2013-configure-user-account-settings.md)

  - [<span data-ttu-id="a3b54-121">(Recommended) Create Conference Directories</span><span class="sxs-lookup"><span data-stu-id="a3b54-121">(Recommended) Create Conference Directories</span></span>](recommended-create-conference-directories.md)

  - [<span data-ttu-id="a3b54-122">(Facultatif) Accueil des utilisateurs dans les conférences rendez-vous dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a3b54-122">(Optional) Welcome users to dial-in conferencing in Lync Server 2013</span></span>](lync-server-2013-optional-welcome-users-to-dial-in-conferencing.md)

</div>

<div>

## <a name="related-sections"></a><span data-ttu-id="a3b54-123">Sections associées</span><span class="sxs-lookup"><span data-stu-id="a3b54-123">Related Sections</span></span>

[<span data-ttu-id="a3b54-124">Déploiement de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a3b54-124">Deploying Lync Server 2013</span></span>](lync-server-2013-deploying-lync-server.md)

<span data-ttu-id="a3b54-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a3b54-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

