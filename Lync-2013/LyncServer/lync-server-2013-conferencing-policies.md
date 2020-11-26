---
title: 'Lync Server 2013 : stratégies de conférence'
description: 'Lync Server 2013 : stratégies de conférence.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Conferencing policies
ms:assetid: 8f92eb7c-ee66-4df6-a726-4bff93b122cb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688133(v=OCS.15)
ms:contentKeyID: 49733732
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6f117cfb077fc24c3e728e208d8bef78cd3284ae
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434311"
---
# <a name="conferencing-policies-in-lync-server-2013"></a><span data-ttu-id="99576-103">Stratégies de conférence dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="99576-103">Conferencing policies in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="99576-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="99576-104">

<span> </span></span></span>

<span data-ttu-id="99576-105">_**Dernière modification de la rubrique :** 2012-09-18_</span><span class="sxs-lookup"><span data-stu-id="99576-105">_**Topic Last Modified:** 2012-09-18_</span></span>

<span data-ttu-id="99576-106">La stratégie de conférence définit les fonctionnalités que les utilisateurs peuvent utiliser pendant une conférence (également appelée réunion).</span><span class="sxs-lookup"><span data-stu-id="99576-106">Conferencing policy defines the features and capabilities that users have available during a conference (also known as a meeting).</span></span> <span data-ttu-id="99576-107">Les paramètres d’une stratégie de conférence englobent une grande variété d’options de planification et de participation, notamment la possibilité d’utiliser des fonctions audio et vidéo IP dans une réunion et de déterminer le nombre maximal de participants.</span><span class="sxs-lookup"><span data-stu-id="99576-107">Conferencing policy settings encompass a wide variety of scheduling and participation options, ranging from whether a meeting can include IP audio and video to the maximum number of people who can attend.</span></span> <span data-ttu-id="99576-108">Les administrateurs peuvent utiliser une stratégie de conférence pour gérer la sécurité, la bande passante et les aspects juridiques des réunions.</span><span class="sxs-lookup"><span data-stu-id="99576-108">Administrators can use conferencing policy to manage security, bandwidth, and legal aspects of meetings.</span></span>

<span data-ttu-id="99576-109">Vous pouvez définir une stratégie de conférence sur trois niveaux : étendue globale, étendue de site et étendue d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="99576-109">You can define conferencing policy on three levels: global scope, site scope, and user scope.</span></span> <span data-ttu-id="99576-110">Les paramètres s’appliquent à un utilisateur spécifique de l’étendue la plus étroite à la plus large.</span><span class="sxs-lookup"><span data-stu-id="99576-110">Settings apply to a specific user from the narrowest scope to the widest scope.</span></span> <span data-ttu-id="99576-111">Si vous attribuez une stratégie utilisateur à un utilisateur, ces paramètres sont prioritaires.</span><span class="sxs-lookup"><span data-stu-id="99576-111">If you assign a user policy to a user, those settings take precedence.</span></span> <span data-ttu-id="99576-112">Si vous n’affectez pas une stratégie utilisateur à un utilisateur, les paramètres de la stratégie par site s’appliquent.</span><span class="sxs-lookup"><span data-stu-id="99576-112">If you do not assign a user policy, site settings apply.</span></span> <span data-ttu-id="99576-113">Si vous n’appliquez aucune stratégie par utilisateur ou par site, la stratégie globale fournit les paramètres par défaut.</span><span class="sxs-lookup"><span data-stu-id="99576-113">If no user or site policies apply, global policy provides the default settings.</span></span>

<span data-ttu-id="99576-114">Une stratégie globale existe par défaut, par conséquent vous ne pouvez pas en créer une nouvelle.</span><span class="sxs-lookup"><span data-stu-id="99576-114">A global policy exists by default, so you cannot create a new global policy.</span></span> <span data-ttu-id="99576-115">Vous ne pouvez pas non plus supprimer la stratégie globale existante, mais vous pouvez modifier la stratégie globale existante pour personnaliser les paramètres par défaut.</span><span class="sxs-lookup"><span data-stu-id="99576-115">You also cannot delete the existing global policy, but you can change the existing global policy to customize your default settings.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="99576-116">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="99576-116">In This Section</span></span>

  - [<span data-ttu-id="99576-117">Afficher les informations de stratégie de conférence dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="99576-117">View conferencing policy information in Lync Server 2013</span></span>](lync-server-2013-view-conferencing-policy-information.md)

  - [<span data-ttu-id="99576-118">Création ou modification d’une stratégie de conférence dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="99576-118">Create or modify a conferencing policy in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-conferencing-policy.md)

  - [<span data-ttu-id="99576-119">Supprimer une stratégie de conférence existante dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="99576-119">Delete an existing conferencing policy in Lync Server 2013</span></span>](lync-server-2013-delete-an-existing-conferencing-policy.md)

  - [<span data-ttu-id="99576-120">Référence des paramètres de stratégie de conférence pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="99576-120">Conferencing policy settings reference for Lync Server 2013</span></span>](lync-server-2013-conferencing-policy-settings-reference.md)

<span data-ttu-id="99576-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="99576-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

