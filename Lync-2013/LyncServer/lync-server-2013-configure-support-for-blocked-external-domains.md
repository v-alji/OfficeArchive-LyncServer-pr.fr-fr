---
title: 'Lync Server 2013 : Configuration de la prise en charge pour les domaines externes bloqués'
description: 'Lync Server 2013 : configuration de la prise en charge des domaines externes bloqués.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure support for blocked external domains
ms:assetid: 49103138-e1ab-42bf-91aa-57cf23bbf260
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ619176(v=OCS.15)
ms:contentKeyID: 49733638
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 81c2c76dc32dd5e8d458dad4e91ff375d2ab005c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433674"
---
# <a name="configure-support-for-blocked-external-domains-in-lync-server-2013"></a><span data-ttu-id="903e0-103">Configuration de la prise en charge pour les domaines externes bloqués dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="903e0-103">Configure support for blocked external domains in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="903e0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="903e0-104">

<span> </span></span></span>

<span data-ttu-id="903e0-105">_**Dernière modification de la rubrique :** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="903e0-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="903e0-106">Si vous avez configuré la prise en charge des partenaires fédérés, vous pouvez gérer les domaines qui seront bloqués par votre organisation.</span><span class="sxs-lookup"><span data-stu-id="903e0-106">If you have configured support for federated partners, you can manage which domains will be blocked from federating with your organization.</span></span> <span data-ttu-id="903e0-107">Si cette option est activée, la liste des domaines bloqués fera office de liste de blocage (liste d’entrées explicites qui ne seront pas autorisées) et sera appliquée dans découverte de domaine fédéré.</span><span class="sxs-lookup"><span data-stu-id="903e0-107">The list of blocked domains will act as a block list (listing of explicit entries that are not to be allowed) and will apply in federated domain discovery, if you have this option enabled.</span></span> <span data-ttu-id="903e0-108">Pour plus d’informations, voir [activer ou désactiver la découverte des partenaires de Fédération dans Lync Server 2013](lync-server-2013-enable-or-disable-discovery-of-federation-partners.md).</span><span class="sxs-lookup"><span data-stu-id="903e0-108">For details, see [Enable or disable discovery of federation partners in Lync Server 2013](lync-server-2013-enable-or-disable-discovery-of-federation-partners.md).</span></span>

<span data-ttu-id="903e0-109">Bloquer un ou plusieurs domaines externes pour vous connecter à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="903e0-109">Block one or more external domains from connecting to your organization.</span></span> <span data-ttu-id="903e0-110">Pour ce faire, ajoutez le domaine à la liste des domaines bloqués.</span><span class="sxs-lookup"><span data-stu-id="903e0-110">To do this, add the domain to the list of blocked domains.</span></span>

<div>

## <a name="to-add-an-external-domain-to-the-list-of-blocked-domains"></a><span data-ttu-id="903e0-111">Pour ajouter un domaine externe à la liste des domaines bloqués</span><span class="sxs-lookup"><span data-stu-id="903e0-111">To add an external domain to the list of blocked domains</span></span>

1.  <span data-ttu-id="903e0-112">À partir d’un compte d’utilisateur membre du groupe RTCUniversalServerAdmins (ou doté de droits d’utilisateur équivalents), ou affectées au rôle CsAdministrator, connectez-vous à n’importe quel ordinateur dans votre déploiement interne.</span><span class="sxs-lookup"><span data-stu-id="903e0-112">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="903e0-113">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="903e0-113">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="903e0-114">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="903e0-114">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="903e0-115">Dans la barre de navigation de gauche, cliquez sur **accès des utilisateurs externes**.</span><span class="sxs-lookup"><span data-stu-id="903e0-115">In the left navigation bar, click **External User Access**.</span></span>

4.  <span data-ttu-id="903e0-116">Cliquez sur **domaines fédérés**, sur **nouveau**, puis sur **domaine bloqué**.</span><span class="sxs-lookup"><span data-stu-id="903e0-116">Click **Federated Domains**, click **New**, and then click **Blocked domain**.</span></span>

5.  <span data-ttu-id="903e0-117">Dans **nouveaux domaines fédérés**, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="903e0-117">In **New Federated Domains**, do the following:</span></span>
    
      - <span data-ttu-id="903e0-118">Dans **nom de domaine (ou nom de domaine complet)**, tapez le nom du domaine de partenaire fédéré que vous souhaitez bloquer.</span><span class="sxs-lookup"><span data-stu-id="903e0-118">In **Domain name (or FQDN)**, type the name of the federated partner domain that you want to block.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="903e0-119">Le nom ne peut pas contenir plus de 256 caractères.</span><span class="sxs-lookup"><span data-stu-id="903e0-119">The name cannot exceed 256 characters in length.</span></span><BR><span data-ttu-id="903e0-120">La recherche du nom de domaine du partenaire fédéré effectue une correspondance de suffixe.</span><span class="sxs-lookup"><span data-stu-id="903e0-120">The search on the federated partner domain name performs a suffix match.</span></span> <span data-ttu-id="903e0-121">Par exemple, si vous tapez <STRONG>contoso.com</STRONG>, la recherche renverra également le domaine <STRONG>it.contoso.com</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="903e0-121">For example, if you type <STRONG>contoso.com</STRONG>, the search will also return the domain <STRONG>it.contoso.com</STRONG>.</span></span><BR><span data-ttu-id="903e0-122">Un domaine de partenaire fédéré ne peut pas être bloqué et autorisé simultanément.</span><span class="sxs-lookup"><span data-stu-id="903e0-122">A federated partner domain cannot simultaneously be blocked and allowed.</span></span> <span data-ttu-id="903e0-123">Lync Server 2013 empêche cela d’avoir lieu de sorte que vous n’ayez pas à synchroniser vos listes.</span><span class="sxs-lookup"><span data-stu-id="903e0-123">Lync Server 2013 prevents this from happening so that you do not have to synch up your lists.</span></span>

        
        </div>
    
      - <span data-ttu-id="903e0-124">Facultatif Dans **Commentaire**, tapez les informations que vous voulez partager avec d’autres administrateurs système sur cette configuration.</span><span class="sxs-lookup"><span data-stu-id="903e0-124">(Optional) In **Comment**, type information that you want to share with other system administrators about this configuration.</span></span>

6.  <span data-ttu-id="903e0-125">Cliquez sur **Valider**.</span><span class="sxs-lookup"><span data-stu-id="903e0-125">Click **Commit**.</span></span>

7.  <span data-ttu-id="903e0-126">Répétez les étapes 4 à 6 pour chaque partenaire fédéré que vous souhaitez bloquer.</span><span class="sxs-lookup"><span data-stu-id="903e0-126">Repeat steps 4 through 6 for each federated partner that you want to block.</span></span>

<span data-ttu-id="903e0-127">Pour autoriser l’accès des utilisateurs fédérés, vous devez également activer la prise en charge de l’accès des utilisateurs fédérés au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="903e0-127">To enable federated user access, you must also enable support for federated user access in your organization.</span></span> <span data-ttu-id="903e0-128">Pour plus d’informations, voir [activer ou désactiver l’accès des utilisateurs distants dans Lync Server 2013](lync-server-2013-enable-or-disable-remote-user-access.md).</span><span class="sxs-lookup"><span data-stu-id="903e0-128">For details, see [Enable or disable remote user access in Lync Server 2013](lync-server-2013-enable-or-disable-remote-user-access.md).</span></span>

<span data-ttu-id="903e0-129">Par ailleurs, vous devez configurer et appliquer la stratégie aux utilisateurs que vous souhaitez pouvoir collaborer avec des utilisateurs fédérés.</span><span class="sxs-lookup"><span data-stu-id="903e0-129">Additionally, you must configure and apply the policy to users that you want to be able to collaborate with federated users.</span></span> <span data-ttu-id="903e0-130">Pour plus d’informations, reportez-vous à la rubrique [Configuration des stratégies pour contrôler l’accès des utilisateurs fédérés dans Lync Server 2013](lync-server-2013-configure-policies-to-control-federated-user-access.md).</span><span class="sxs-lookup"><span data-stu-id="903e0-130">For details, see [Configure policies to control federated user access in Lync Server 2013](lync-server-2013-configure-policies-to-control-federated-user-access.md).</span></span>

<span data-ttu-id="903e0-131"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="903e0-131"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

