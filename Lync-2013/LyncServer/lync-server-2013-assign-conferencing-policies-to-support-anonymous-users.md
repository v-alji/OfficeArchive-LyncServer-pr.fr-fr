---
title: 'Lync Server 2013 : Affectation des stratégies de conférence pour la prise en charge les utilisateurs anonymes'
description: 'Lync Server 2013 : attribution de stratégies de conférence pour prendre en charge les utilisateurs anonymes.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Assign conferencing policies to support anonymous users
ms:assetid: 662de022-1111-40f7-bad4-f2b686f30973
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg521007(v=OCS.15)
ms:contentKeyID: 48184333
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 07e94c3097e3e21f854e91fdee1ad0b33c3b9f53
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443210"
---
# <a name="assign-conferencing-policies-to-support-anonymous-users-in-lync-server-2013"></a><span data-ttu-id="7a54b-103">Affectation des stratégies de conférence pour la prise en charge les utilisateurs anonymes dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7a54b-103">Assign conferencing policies to support anonymous users in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7a54b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7a54b-104">

<span> </span></span></span>

<span data-ttu-id="7a54b-105">_**Dernière modification de la rubrique :** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="7a54b-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="7a54b-106">Par défaut, tous les utilisateurs ne peuvent pas inviter des utilisateurs anonymes à participer à une réunion.</span><span class="sxs-lookup"><span data-stu-id="7a54b-106">By default, all users are prevented from inviting anonymous users to participate in a meeting.</span></span> <span data-ttu-id="7a54b-107">Vous contrôlez qui peut inviter des utilisateurs anonymes en configurant une stratégie de conférence pour prendre en charge les utilisateurs anonymes et en appliquant cette stratégie de conférence à des utilisateurs spécifiques.</span><span class="sxs-lookup"><span data-stu-id="7a54b-107">You control who can invite anonymous users by configuring a conferencing policy to support anonymous users, and applying that conferencing policy to specific users.</span></span> <span data-ttu-id="7a54b-108">Pour plus d’informations sur la configuration des stratégies de conférence pour prendre en charge les utilisateurs anonymes, voir [créer ou modifier une stratégie de conférence dans Lync server 2013](lync-server-2013-create-or-modify-a-conferencing-policy.md) et [gérer la Fédération et l’accès externe à Lync Server 2013](lync-server-2013-managing-federation-and-external-access-to-lync-server-2013.md).</span><span class="sxs-lookup"><span data-stu-id="7a54b-108">For details about how to configure a conferencing policies to support anonymous users, see [Create or modify a conferencing policy in Lync Server 2013](lync-server-2013-create-or-modify-a-conferencing-policy.md) and [Managing federation and external access to Lync Server 2013](lync-server-2013-managing-federation-and-external-access-to-lync-server-2013.md).</span></span>

<span data-ttu-id="7a54b-109">Suivez la procédure décrite dans cette section pour appliquer une stratégie de conférence que vous avez déjà créée à un ou plusieurs utilisateurs ou groupes d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="7a54b-109">Use the procedure in this section to apply a conferencing policy that you have already created to one or more users or user groups.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="7a54b-110">En plus de configurer et d’appliquer une stratégie pour permettre aux utilisateurs d’inviter des utilisateurs anonymes, vous devez également activer la prise en charge des utilisateurs anonymes pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="7a54b-110">In addition to configuring and applying a policy to enable users to invite anonymous users, you must also enable support for anonymous users for your organization.</span></span> <span data-ttu-id="7a54b-111">Pour plus d’informations, reportez-vous à la rubrique <A href="lync-server-2013-configure-policies-to-control-public-user-access.md">Configuration des stratégies pour contrôler l’accès des utilisateurs publics dans Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="7a54b-111">For details, see <A href="lync-server-2013-configure-policies-to-control-public-user-access.md">Configure policies to control public user access in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="to-configure-a-user-policy-for-anonymous-participation-in-meetings"></a><span data-ttu-id="7a54b-112">Pour configurer une stratégie utilisateur pour la participation anonyme aux réunions</span><span class="sxs-lookup"><span data-stu-id="7a54b-112">To configure a user policy for anonymous participation in meetings</span></span>

1.  <span data-ttu-id="7a54b-113">À partir d’un compte d’utilisateur membre du groupe RTCUniversalServerAdmins (ou doté de droits d’utilisateur équivalents), ou affectées au rôle CsAdministrator, connectez-vous à n’importe quel ordinateur dans votre déploiement interne.</span><span class="sxs-lookup"><span data-stu-id="7a54b-113">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="7a54b-114">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="7a54b-114">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="7a54b-115">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="7a54b-115">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="7a54b-116">Dans la barre de navigation de gauche, cliquez sur **Conférence**, puis effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="7a54b-116">In the left navigation bar, click **Conferencing**, and then do one of the following:</span></span>
    
    1.  <span data-ttu-id="7a54b-117">Pour créer une nouvelle stratégie d’utilisateur, cliquez sur **nouveau**, puis cliquez sur stratégie de l' **utilisateur**.</span><span class="sxs-lookup"><span data-stu-id="7a54b-117">To create a new user policy, click **New**, and then click **User policy**.</span></span> <span data-ttu-id="7a54b-118">Dans le champ **nom** , créez un nom unique qui indique l’objet de la stratégie de l’utilisateur (par exemple, **EnableAnonymous** pour une stratégie utilisateur qui autorise les communications avec des utilisateurs anonymes).</span><span class="sxs-lookup"><span data-stu-id="7a54b-118">Create a unique name in the **Name** field that indicates what the user policy covers (for example, **EnableAnonymous** for a user policy that enables communications with anonymous users).</span></span>
    
    2.  <span data-ttu-id="7a54b-119">Pour configurer une stratégie d’utilisateur existante, cliquez sur la stratégie appropriée répertoriée dans le tableau, cliquez sur **modifier**, puis sur **afficher les détails**.</span><span class="sxs-lookup"><span data-stu-id="7a54b-119">To configure an existing user policy, click the appropriate policy listed in the table, click **Edit**, and then click **Show details**.</span></span>

4.  <span data-ttu-id="7a54b-120">Dans la boîte de dialogue **stratégies de conférence** , activez la case à cocher **autoriser les participants à inviter des utilisateurs anonymes** .</span><span class="sxs-lookup"><span data-stu-id="7a54b-120">In the **Conferencing Policies** dialog box, select the **Allow participants to invite anonymous users** check box.</span></span>

5.  <span data-ttu-id="7a54b-121">Cliquez sur **Valider**.</span><span class="sxs-lookup"><span data-stu-id="7a54b-121">Click **Commit**.</span></span>

6.  <span data-ttu-id="7a54b-122">Dans la barre de navigation de gauche, cliquez sur **utilisateurs**, puis recherchez le compte d’utilisateur que vous voulez configurer.</span><span class="sxs-lookup"><span data-stu-id="7a54b-122">In the left navigation bar, click **Users**, search on the user account that you want to configure.</span></span>

7.  <span data-ttu-id="7a54b-123">Dans le tableau répertoriant les résultats de la recherche, cliquez sur le compte d’utilisateur, sur **Modifier**, puis sur **Afficher les détails**.</span><span class="sxs-lookup"><span data-stu-id="7a54b-123">In the table that lists the search results, click the user account, click **Edit**, and then click **Show details**.</span></span>

8.  <span data-ttu-id="7a54b-124">Dans **modifier l’utilisateur de Lync Server** sous **stratégie de conférence**, sélectionnez la stratégie de l’utilisateur avec la configuration d’accès anonyme pour les utilisateurs que vous souhaitez appliquer à cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7a54b-124">In **Edit Lync Server User** under **Conferencing policy**, select the user policy with the anonymous user access configuration that you want to apply to this user.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="7a54b-125">Les paramètres <STRONG> &lt; automatiques &gt; </STRONG> appliquent les paramètres d’installation par défaut du serveur et sont appliqués automatiquement par le serveur.</span><span class="sxs-lookup"><span data-stu-id="7a54b-125">The <STRONG>&lt;Automatic&gt;</STRONG> settings apply the default server installation settings and are applied automatically by the server.</span></span>

    
    </div>

<span data-ttu-id="7a54b-126">Pour permettre aux utilisateurs d’inviter des utilisateurs anonymes à des conférences, vous devez également activer la prise en charge des utilisateurs anonymes au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="7a54b-126">To enable users to invite anonymous users to conferences, you must also enable support for anonymous users in your organization.</span></span> <span data-ttu-id="7a54b-127">Pour plus d’informations, reportez-vous à la rubrique [Configuration des stratégies pour contrôler l’accès des utilisateurs publics dans Lync Server 2013](lync-server-2013-configure-policies-to-control-public-user-access.md) dans la documentation de déploiement ou la documentation des opérations.</span><span class="sxs-lookup"><span data-stu-id="7a54b-127">For details, see [Configure policies to control public user access in Lync Server 2013](lync-server-2013-configure-policies-to-control-public-user-access.md) in the Deployment documentation or the Operations documentation.</span></span>

<span data-ttu-id="7a54b-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7a54b-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

