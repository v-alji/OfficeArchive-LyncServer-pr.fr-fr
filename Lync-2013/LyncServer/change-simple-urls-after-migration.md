---
title: Modification des URL simples après la migration
description: Modification des URL simples après la migration.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Change simple URLs after migration
ms:assetid: addb0dc8-8324-42b1-9a00-f4bd14fdf5c0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721844(v=OCS.15)
ms:contentKeyID: 49733777
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b2f9974106d28bcfdc64c2255337baf721a937e7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394248"
---
# <a name="change-simple-urls-after-migration"></a><span data-ttu-id="30371-103">Modification des URL simples après la migration</span><span class="sxs-lookup"><span data-stu-id="30371-103">Change simple URLs after migration</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="30371-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="30371-104">

<span> </span></span></span>

<span data-ttu-id="30371-105">_**Dernière modification de la rubrique :** 2012-09-22_</span><span class="sxs-lookup"><span data-stu-id="30371-105">_**Topic Last Modified:** 2012-09-22_</span></span>

<span data-ttu-id="30371-106">Lync Server prend en charge trois URL simples :</span><span class="sxs-lookup"><span data-stu-id="30371-106">Lync Server supports three simple URLs:</span></span>

  - <span data-ttu-id="30371-107">La **fonction réunion** est utilisée comme URL de base pour toutes les conférences du site ou de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="30371-107">**Meet** is used as the base URL for all conferences in the site or organization.</span></span> <span data-ttu-id="30371-108">Avec l’URL de la réunion, vous pouvez facilement comprendre les liens permettant de participer à des réunions, et facilement communiquer et diffuser.</span><span class="sxs-lookup"><span data-stu-id="30371-108">With the Meet simple URL, links to join meetings are easy to comprehend, and easy to communicate and distribute.</span></span>

  - <span data-ttu-id="30371-109">Le rendez **-** vous permet d’accéder à la page Web des paramètres de conférence rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="30371-109">**Dial-in** enables access to the Dial-in Conferencing Settings webpage.</span></span> <span data-ttu-id="30371-110">L’URL d’accès à un rendez-vous est incluse dans toutes les invitations à une réunion de sorte que les utilisateurs qui souhaitent se connecter à la réunion puissent accéder au numéro de téléphone et aux informations de code confidentiel nécessaires.</span><span class="sxs-lookup"><span data-stu-id="30371-110">The Dial-in simple URL is included in all meeting invitations so that users who want to dial in to the meeting can access the necessary phone number and PIN information.</span></span>

  - <span data-ttu-id="30371-111">L' **administrateur** vous permet d’accéder rapidement au panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="30371-111">**Admin** enables quick access to the Lync Server Control Panel.</span></span> <span data-ttu-id="30371-112">L’URL simple Admin est interne à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="30371-112">The Admin simple URL is internal to your organization.</span></span>

<span data-ttu-id="30371-113">Après avoir effectué la migration vers Lync Server 2013, vous devez tenir compte de la façon dont le changement a un impact sur vos enregistrements et certificats DNS pour des URL simples.</span><span class="sxs-lookup"><span data-stu-id="30371-113">After migrating to Lync Server 2013, you must be aware of how the change impacts your DNS records and certificates for simple URLs.</span></span> <span data-ttu-id="30371-114">Si le réalisateur du serveur Lync Server 2010 hérité reste en cours d’utilisation dans la topologie, aucune modification de vos URL simples n’est requise.</span><span class="sxs-lookup"><span data-stu-id="30371-114">If the legacy Lync Server 2010 Director remains in use in the topology, no changes to your simple URLs are required.</span></span> <span data-ttu-id="30371-115">Si le directeur de Lync Server 2010 est supprimé de la topologie après la migration, les enregistrements DNS d’URL simples doivent être mis à jour de manière à ce qu’ils pointent vers l’une des listes 2013 du serveur Lync.</span><span class="sxs-lookup"><span data-stu-id="30371-115">If the Lync Server 2010 Director is removed from the topology after migration, the simple URL DNS records must be updated to point to one of the Lync Server 2013 pools.</span></span> <span data-ttu-id="30371-116">Néanmoins, chaque fois que vous modifiez un nom d’URL simple, vous devez exécuter Enable-CsComputer de chaque directeur et serveur frontal pour enregistrer la modification.</span><span class="sxs-lookup"><span data-stu-id="30371-116">Whenever you change a simple URL name, however, you must run Enable-CsComputer on each Director and Front End Server to register the change.</span></span>

<div>

## <a name="changing-simple-urls-after-migration"></a><span data-ttu-id="30371-117">Modification d’URL simples après la migration</span><span class="sxs-lookup"><span data-stu-id="30371-117">Changing Simple URLs after Migration</span></span>

<span data-ttu-id="30371-118">**Pour mettre à jour l’URL de réunion simple**</span><span class="sxs-lookup"><span data-stu-id="30371-118">**To update the Meet simple URL**</span></span>

1.  <span data-ttu-id="30371-119">Dans le générateur de topologie, cliquez avec le bouton droit sur le nœud supérieur **Lync Server**, puis cliquez sur **modifier les propriétés**.</span><span class="sxs-lookup"><span data-stu-id="30371-119">In Topology Builder, right-click the top node **Lync Server**, and then click **Edit Properties**.</span></span>

2.  <span data-ttu-id="30371-120">Sélectionnez **URL simples** dans le volet gauche, puis sous **URL de la réunion :** sélectionnez l’URL de la réunion, puis cliquez sur **modifier l’URL**.</span><span class="sxs-lookup"><span data-stu-id="30371-120">Select **Simple URLs** in the left pane, then below **Meeting URLs:** select the Meet URL and then click **Edit URL**.</span></span>

3.  <span data-ttu-id="30371-121">Mettez à jour l’URL comme vous le souhaitez puis cliquez sur **OK** pour enregistrer l’URL modifiée.</span><span class="sxs-lookup"><span data-stu-id="30371-121">Update the URL to the value you want, and then click **OK** to save the edited URL.</span></span>

<span data-ttu-id="30371-122">**Pour mettre à jour l’URL simple d’administration**</span><span class="sxs-lookup"><span data-stu-id="30371-122">**To update the Admin simple URL**</span></span>

1.  <span data-ttu-id="30371-123">Dans le générateur de topologie, cliquez avec le bouton droit sur le nœud supérieur **Lync Server**, puis cliquez sur **modifier les propriétés**.</span><span class="sxs-lookup"><span data-stu-id="30371-123">In Topology Builder, right-click the top node **Lync Server**, and then click **Edit Properties**.</span></span>

2.  <span data-ttu-id="30371-124">Sélectionnez **URL simples** dans le volet gauche, puis sous **URL d’accès administratif** , entrez l’URL de votre choix pour l’accès administratif à Lync Server 2013 panneau de configuration, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="30371-124">Select **Simple URLs** in the left pane, then below **Administrative access URL** box, enter the simple URL you want for administrative access to Lync Server 2013 Control Panel, and then click **OK**.</span></span>
    
    <div>
    

    > [!TIP]  
    > <span data-ttu-id="30371-125">Nous vous recommandons d’utiliser l’URL la plus simple possible pour l’URL d’administration.</span><span class="sxs-lookup"><span data-stu-id="30371-125">We recommend using the simplest possible URL for the Admin URL.</span></span> <span data-ttu-id="30371-126">L’option la plus simple est <STRONG> https://admin .</STRONG> &lt; Domain (domaine) &gt; .</span><span class="sxs-lookup"><span data-stu-id="30371-126">The simplest option is <STRONG>https://admin.</STRONG>&lt;domain&gt;.</span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="30371-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30371-127">See Also</span></span>


[<span data-ttu-id="30371-128">Planification des URL simples dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="30371-128">Planning for simple URLs in Lync Server 2013</span></span>](lync-server-2013-planning-for-simple-urls.md)  
  

<span data-ttu-id="30371-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="30371-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

