---
title: 'Lync Server 2013 : Configuraton de la prise en charge des domaines externes autorisés'
description: 'Lync Server 2013 : configuration de la prise en charge des domaines externes autorisés.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure support for allowed external domains
ms:assetid: 3ee6e175-986d-4c33-b03a-b9f93083dca6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425908(v=OCS.15)
ms:contentKeyID: 48183943
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 13845638bca8791d43b8644c5dcb30ec73751a5b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433681"
---
# <a name="configure-support-for-allowed-external-domains-in-lync-server-2013"></a><span data-ttu-id="2cf5f-103">Configuration de la prise en charge des domaines externes autorisés dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2cf5f-103">Configure support for allowed external domains in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2cf5f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2cf5f-104">

<span> </span></span></span>

<span data-ttu-id="2cf5f-105">_**Dernière modification de la rubrique :** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="2cf5f-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="2cf5f-106">Si vous avez configuré la prise en charge des partenaires fédérés, vous pouvez gérer les domaines spécifiques qu’il est possible de fédérer avec votre organisation.</span><span class="sxs-lookup"><span data-stu-id="2cf5f-106">If you have configured support for federated partners, you can manage which specific domains can federate with your organization.</span></span> <span data-ttu-id="2cf5f-107">Vous pouvez configurer un ou plusieurs domaines externes spécifiques en tant que domaines fédérés autorisés.</span><span class="sxs-lookup"><span data-stu-id="2cf5f-107">You configure one or more specific external domains as allowed federated domains.</span></span> <span data-ttu-id="2cf5f-108">Pour ce faire, ajoutez chaque domaine à la liste des domaines autorisés.</span><span class="sxs-lookup"><span data-stu-id="2cf5f-108">To do this, add each domain to the list of allowed domains.</span></span> <span data-ttu-id="2cf5f-109">Même si la découverte des partenaires est activée pour votre organisation, procédez comme suit si le domaine est un partenaire fédéré qui peut avoir besoin de communiquer avec plus de 1 000 ou si vous avez besoin d’envoyer plus de 20 messages par seconde.</span><span class="sxs-lookup"><span data-stu-id="2cf5f-109">Even if partner discovery is enabled for your organization, do this if the domain is a federated partner that might need to communicate with more than 1,000 of your users or might need to send more than 20 messages per second.</span></span> <span data-ttu-id="2cf5f-110">Si la découverte de partenaire n’est pas activée pour votre organisation, seuls les utilisateurs de domaines externes que vous ajoutez à la liste des domaines autorisés peuvent participer à la messagerie instantanée et à la Conférence avec les utilisateurs de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="2cf5f-110">If partner discovery is not enabled for your organization, only users of external domains that you add to the allowed domains list can participate in IM and conferencing with users in your organization.</span></span> <span data-ttu-id="2cf5f-111">Si vous souhaitez limiter l’accès d’un domaine fédéré à un serveur spécifique exécutant le service Edge d’accès du partenaire fédéré, vous pouvez spécifier le nom de domaine du serveur exécutant le service Edge d’accès pour chaque domaine dans la liste des domaines autorisés.</span><span class="sxs-lookup"><span data-stu-id="2cf5f-111">If you want to restrict access for a federated domain to a specific server running the Access Edge service of the federated partner, you can specify the domain name of the server running the Access Edge service for each domain in the list of allowed domains.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="2cf5f-112">Cette procédure vous explique comment configurer la prise en charge des domaines spécifiques, mais l’implémentation de la prise en charge des utilisateurs fédérés nécessite également l’activation de la prise en charge des utilisateurs fédérés pour votre organisation, et la configuration et l’application de stratégies pour contrôler les utilisateurs qui peuvent collaborer avec des utilisateurs fédérés.</span><span class="sxs-lookup"><span data-stu-id="2cf5f-112">This procedure describes how to configure support for specific domains, but implementing support for federated users also requires that you enable support for federated users for your organization, and configure and apply policies to control which users can collaborate with federated users.</span></span> <span data-ttu-id="2cf5f-113">Pour plus d’informations sur l’activation de la prise en charge des utilisateurs fédérés, voir <A href="lync-server-2013-enable-or-disable-remote-user-access.md">activation ou désactivation de l’accès des utilisateurs distants dans Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="2cf5f-113">For details about enabling support for federated users, see <A href="lync-server-2013-enable-or-disable-remote-user-access.md">Enable or disable remote user access in Lync Server 2013</A>.</span></span> <span data-ttu-id="2cf5f-114">Pour plus d’informations sur la configuration des stratégies pour contrôler la Fédération, voir <A href="lync-server-2013-configure-policies-to-control-federated-user-access.md">configurer des stratégies pour contrôler l’accès des utilisateurs fédérés dans Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="2cf5f-114">For details about configuring policies to control federation, see <A href="lync-server-2013-configure-policies-to-control-federated-user-access.md">Configure policies to control federated user access in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="to-add-an-external-domain-to-the-list-of-allowed-domains"></a><span data-ttu-id="2cf5f-115">Pour ajouter un domaine externe à la liste des domaines autorisés</span><span class="sxs-lookup"><span data-stu-id="2cf5f-115">To add an external domain to the list of allowed domains</span></span>

1.  <span data-ttu-id="2cf5f-116">À partir d’un compte d’utilisateur membre du groupe RTCUniversalServerAdmins (ou doté de droits d’utilisateur équivalents), ou affectées au rôle CsAdministrator, connectez-vous à n’importe quel ordinateur dans votre déploiement interne.</span><span class="sxs-lookup"><span data-stu-id="2cf5f-116">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="2cf5f-117">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="2cf5f-117">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="2cf5f-118">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="2cf5f-118">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="2cf5f-119">Dans la barre de navigation de gauche, cliquez sur **accès utilisateur externe**, puis sur **domaines fédérés**.</span><span class="sxs-lookup"><span data-stu-id="2cf5f-119">In the left navigation bar, click **External User Access**, and then click **Federated Domains**.</span></span>

4.  <span data-ttu-id="2cf5f-120">Sur la page **domaines fédérés** , cliquez sur **nouveau**, puis cliquez sur **domaine autorisé**.</span><span class="sxs-lookup"><span data-stu-id="2cf5f-120">On the **Federated Domains** page, click **New**, and then click **Allowed domain**.</span></span>

5.  <span data-ttu-id="2cf5f-121">Dans **nouveaux domaines fédérés**, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="2cf5f-121">In **New Federated Domains**, do the following:</span></span>
    
      - <span data-ttu-id="2cf5f-122">Dans **nom de domaine (ou nom de domaine complet)**, tapez le nom du domaine du partenaire fédéré.</span><span class="sxs-lookup"><span data-stu-id="2cf5f-122">In **Domain name (or FQDN)**, type the name of the federated partner domain.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="2cf5f-123">Ce nom doit être unique et ne peut pas déjà exister en tant que domaine autorisé pour ce serveur exécutant le service Edge d’accès.</span><span class="sxs-lookup"><span data-stu-id="2cf5f-123">This name must be unique and cannot already exist as an allowed domain for this server running the Access Edge service.</span></span> <span data-ttu-id="2cf5f-124">Le nom ne peut pas contenir plus de 256 caractères.</span><span class="sxs-lookup"><span data-stu-id="2cf5f-124">The name cannot exceed 256 characters in length.</span></span><BR><span data-ttu-id="2cf5f-125">La recherche du nom de domaine du partenaire fédéré effectue une correspondance de suffixe.</span><span class="sxs-lookup"><span data-stu-id="2cf5f-125">The search on the federated partner domain name performs a suffix match.</span></span> <span data-ttu-id="2cf5f-126">Par exemple, si vous tapez <STRONG>contoso.com</STRONG>, la recherche renverra également le domaine <STRONG>it.contoso.com</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="2cf5f-126">For example, if you type <STRONG>contoso.com</STRONG>, the search will also return the domain <STRONG>it.contoso.com</STRONG>.</span></span><BR><span data-ttu-id="2cf5f-127">Un domaine de partenaire fédéré ne peut pas être bloqué et autorisé simultanément.</span><span class="sxs-lookup"><span data-stu-id="2cf5f-127">A federated partner domain cannot simultaneously be blocked and allowed.</span></span> <span data-ttu-id="2cf5f-128">Lync Server 2013 empêche cela d’avoir lieu de sorte que vous n’ayez pas à synchroniser vos listes.</span><span class="sxs-lookup"><span data-stu-id="2cf5f-128">Lync Server 2013 prevents this from happening so that you do not have to synch up your lists.</span></span>

        
        </div>
    
      - <span data-ttu-id="2cf5f-129">Si vous voulez limiter l’accès à ce domaine fédéré aux utilisateurs d’un serveur spécifique exécutant le service Edge d’accès (FQDN), tapez le nom de domaine complet **(FQDN)** du serveur du domaine fédéré exécutant le service Edge d’accès.</span><span class="sxs-lookup"><span data-stu-id="2cf5f-129">If you want to restrict access for this federated domain to users of a specific server running the Access Edge service, in **Access Edge service (FQDN)**, type the FQDN of the federated domain’s server running the Access Edge service.</span></span>
    
      - <span data-ttu-id="2cf5f-130">Si vous voulez fournir des informations supplémentaires, dans **commenter**, tapez les informations que vous voulez partager avec d’autres administrateurs système sur cette configuration.</span><span class="sxs-lookup"><span data-stu-id="2cf5f-130">If you want to provide additional information, in **Comment**, type information that you want to share with other system administrators about this configuration.</span></span>

6.  <span data-ttu-id="2cf5f-131">Cliquez sur **Valider**.</span><span class="sxs-lookup"><span data-stu-id="2cf5f-131">Click **Commit**.</span></span>

7.  <span data-ttu-id="2cf5f-132">Répétez les étapes 4 à 6 pour chaque domaine partenaire fédéré que vous souhaitez autoriser.</span><span class="sxs-lookup"><span data-stu-id="2cf5f-132">Repeat steps 4 through 6 for each federated partner domain that you want to allow.</span></span>

<span data-ttu-id="2cf5f-133">Pour autoriser l’accès des utilisateurs fédérés, vous devez également activer la prise en charge de l’accès des utilisateurs fédérés au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="2cf5f-133">To enable federated user access, you must also enable support for federated user access in your organization.</span></span> <span data-ttu-id="2cf5f-134">Pour plus d’informations, voir [activer ou désactiver l’accès des utilisateurs distants dans Lync Server 2013](lync-server-2013-enable-or-disable-remote-user-access.md).</span><span class="sxs-lookup"><span data-stu-id="2cf5f-134">For details, see [Enable or disable remote user access in Lync Server 2013](lync-server-2013-enable-or-disable-remote-user-access.md).</span></span>

<span data-ttu-id="2cf5f-135">Par ailleurs, vous devez configurer et appliquer la stratégie aux utilisateurs que vous souhaitez pouvoir collaborer avec des utilisateurs fédérés.</span><span class="sxs-lookup"><span data-stu-id="2cf5f-135">Additionally, you must configure and apply the policy to users that you want to be able to collaborate with federated users.</span></span> <span data-ttu-id="2cf5f-136">Pour plus d’informations, reportez-vous à la rubrique [Configuration des stratégies pour contrôler l’accès des utilisateurs fédérés dans Lync Server 2013](lync-server-2013-configure-policies-to-control-federated-user-access.md).</span><span class="sxs-lookup"><span data-stu-id="2cf5f-136">For details, see [Configure policies to control federated user access in Lync Server 2013](lync-server-2013-configure-policies-to-control-federated-user-access.md).</span></span>

<span data-ttu-id="2cf5f-137"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2cf5f-137"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

