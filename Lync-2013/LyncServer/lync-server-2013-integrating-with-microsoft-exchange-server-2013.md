---
title: 'Lync Server 2013 : intégration avec Microsoft Exchange Server 2013'
description: 'Lync Server 2013 : intégration avec Microsoft Exchange Server 2013.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Integrating Lync Server 2013 and Exchange Server 2013
ms:assetid: 795dc1c6-524f-4012-8b66-103b55198044
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688098(v=OCS.15)
ms:contentKeyID: 49733697
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 54ab4a81e5455bc0a44677b1509876f39ff4d985
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426878"
---
# <a name="integrating-microsoft-lync-server-2013-and-microsoft-exchange-server-2013"></a><span data-ttu-id="e20db-103">Intégration de Microsoft Lync Server 2013 et Microsoft Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="e20db-103">Integrating Microsoft Lync Server 2013 and Microsoft Exchange Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e20db-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e20db-104">

<span> </span></span></span>

<span data-ttu-id="e20db-105">_**Dernière modification de la rubrique :** 2014-07-09_</span><span class="sxs-lookup"><span data-stu-id="e20db-105">_**Topic Last Modified:** 2014-07-09_</span></span>

<span data-ttu-id="e20db-106">Exchange et Lync Server présentent un historique d’intégration et de compatibilité longs.</span><span class="sxs-lookup"><span data-stu-id="e20db-106">Exchange and Lync Server have a long history of integration and compatibility.</span></span> <span data-ttu-id="e20db-107">Cette intégration est plus notable dans l’application cliente correspondante.</span><span class="sxs-lookup"><span data-stu-id="e20db-107">This integration is most noticeable within their respective client application.</span></span> <span data-ttu-id="e20db-108">Par exemple, les informations de présence Lync peuvent être rapportées dans Microsoft Outlook. de même, Lync peut utiliser le calendrier Outlook pour mettre automatiquement à jour les informations de présence.</span><span class="sxs-lookup"><span data-stu-id="e20db-108">For example, Lync presence information can be reported in Microsoft Outlook; likewise, Lync can use Outlook calendar to automatically update that presence information.</span></span> <span data-ttu-id="e20db-109">(Par exemple, Lync peut définir votre statut sur occupé chaque fois que votre calendrier indique qu’une réunion est planifiée.) Même si vous n’avez pas besoin d’exécuter Exchange pour pouvoir exécuter Lync Server (ou inversement), il n’y a pas de doute que l’utilisation conjointe de deux produits a pour but epitomizes de définir le terme « meilleures ».</span><span class="sxs-lookup"><span data-stu-id="e20db-109">(For example, Lync can change your status to Busy any time your calendar shows that you have a meeting scheduled.) Although you do not have to run Exchange in order to run Lync Server (or vice-versa) there's little doubt that using the two products together epitomizes the very definition of the term "better together."</span></span>

<span data-ttu-id="e20db-110">Ceci est particulièrement vrai avec la version de Microsoft Lync Server 2013 et Microsoft Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e20db-110">This is especially true with the release of Microsoft Lync Server 2013 and Microsoft Exchange Server 2013.</span></span> <span data-ttu-id="e20db-111">Outre les fonctionnalités telles que la messagerie unifiée et la messagerie instantanée et la présence, qui se trouvent dans Microsoft Exchange Server 2010 et Microsoft Lync Server 2010, les publications 2013 des produits serveur incluent un certain nombre de nouvelles fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="e20db-111">In addition to features, such as unified messaging and IM and presence, that are found in Microsoft Exchange Server 2010 and Microsoft Lync Server 2010, the 2013 releases of the server products include a number of new capabilities.</span></span> <span data-ttu-id="e20db-112">Ces fonctionnalités incluent les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="e20db-112">These capabilities include such things as:</span></span>

  - <span data-ttu-id="e20db-113">**Intégration de l’archivage Lync**.</span><span class="sxs-lookup"><span data-stu-id="e20db-113">**Lync Archiving Integration**.</span></span> <span data-ttu-id="e20db-114">Dans les administrateurs de Lync Server 2013, vous avez toujours la possibilité d’archiver les transcriptions de messagerie instantanée et de conférence Web sur SQL Server (de la même façon que ces transcriptions ont été archivées dans Lync Server 2010).</span><span class="sxs-lookup"><span data-stu-id="e20db-114">In Lync Server 2013 administrators still have the option of having instant messaging and Web conferencing transcripts archived to SQL Server (the same way these transcripts were archived in Lync Server 2010).</span></span> <span data-ttu-id="e20db-115">En revanche, les administrateurs peuvent choisir d’archiver les transcriptions dans Exchange 2013, en stockant ces transcriptions dans les boîtes aux lettres individuelles de l’utilisateur de la même manière qu’Exchange Archive les communications.</span><span class="sxs-lookup"><span data-stu-id="e20db-115">Alternatively, however, administrators can choose to have transcripts archived to Exchange 2013, storing those transcripts in the individual user mailboxes in the same way in which Exchange archives communications.</span></span> <span data-ttu-id="e20db-116">Il s’agit d’un référentiel unique pour toutes vos communications électroniques (Exchange et Lync Server), ce qui facilite la recherche et la récupération des communications archivées en cas de besoin.</span><span class="sxs-lookup"><span data-stu-id="e20db-116">That means a single repository for all your electronic communications (from both Exchange and Lync Server), which makes it much easier to search for and retrieve those archived communications should the need arise.</span></span>

  - <span data-ttu-id="e20db-117">**Magasin de contacts unifié**</span><span class="sxs-lookup"><span data-stu-id="e20db-117">**Unified Contact Store**.</span></span> <span data-ttu-id="e20db-118">Dans Lync Server 2010, les utilisateurs doivent tenir à jour des listes de contacts distinctes dans Outlook et Lync. pour vous assurer que les mêmes contacts étaient disponibles dans les deux produits, vous devez tenir à jour des listes de contacts en double, une pour Outlook et une pour Lync.</span><span class="sxs-lookup"><span data-stu-id="e20db-118">In Lync Server 2010, users had to maintain separate contact lists in Outlook and Lync; in fact, to ensure that you had the same contacts available in both products you had to maintain duplicate contact lists, one for Outlook and one for Lync.</span></span> <span data-ttu-id="e20db-119">Toutefois, avec Lync Server 2013, les contacts des utilisateurs peuvent être stockés dans Exchange 2013 et dans le magasin de contacts unifié.</span><span class="sxs-lookup"><span data-stu-id="e20db-119">With Lync Server 2013, however, user contacts can be stored in Exchange 2013 and the unified contact store.</span></span> <span data-ttu-id="e20db-120">L’utilisation d’un seul magasin de contacts permet aux utilisateurs de conserver un seul ensemble de contacts, avec ce même ensemble de contacts disponible dans Lync 2013, Outlook 2013 et Outlook Web Access 2013.</span><span class="sxs-lookup"><span data-stu-id="e20db-120">Using a single contact store enables users to maintain just one set of contacts, with that same set of contacts being available in Lync 2013, Outlook 2013, and Outlook Web Access 2013.</span></span>

  - <span data-ttu-id="e20db-121">**Planification de réunions Lync à partir d’OWA**.</span><span class="sxs-lookup"><span data-stu-id="e20db-121">**Lync Meeting Scheduling from OWA**.</span></span> <span data-ttu-id="e20db-122">Grâce à l’intégration de Lync Server 2013 et Exchange 2013, les utilisateurs peuvent planifier des réunions Lync à partir d’Outlook Web Access 2013.</span><span class="sxs-lookup"><span data-stu-id="e20db-122">With Lync Server 2013 and Exchange 2013 integration, users can schedule Lync meetings from Outlook Web Access 2013.</span></span>

  - <span data-ttu-id="e20db-123">**Photos haute résolution**.</span><span class="sxs-lookup"><span data-stu-id="e20db-123">**High resolution photos**.</span></span> <span data-ttu-id="e20db-124">Lync 2010 ne peut pas afficher de petites photos de vos contacts. Cela est dû au fait que ces photos étaient stockées dans Active Directory et qu’Active Directory impose une limitation de 48 pixels par 48 en taille de pixel sur les photos stockées.</span><span class="sxs-lookup"><span data-stu-id="e20db-124">Lync 2010 could only display small photos of your contacts; that's because those photos were stored in Active Directory, and Active Directory imposes a 48 pixel by 48 pixel size limitation on stored photos.</span></span> <span data-ttu-id="e20db-125">Toutefois, avec Lync Server 2013, les photos peuvent être stockées dans Microsoft Exchange. Cela permet de disposer de photos haute résolution de plus de 648 pixels par 648 pixels.</span><span class="sxs-lookup"><span data-stu-id="e20db-125">With Lync Server 2013, however, photos can be stored in Microsoft Exchange; that allows for high-resolution photos as large as 648 pixels by 648 pixels.</span></span> <span data-ttu-id="e20db-126">Comme vous pouvez le constater, Lync 2013 a été mis à jour de manière à autoriser l’affichage de ces photographies haute résolution.</span><span class="sxs-lookup"><span data-stu-id="e20db-126">As you might expect, Lync 2013 has been upgraded to allow for the display of these high-resolution photographs.</span></span>

<span data-ttu-id="e20db-127">Gardez à l’esprit que ces nouvelles fonctionnalités nécessitent l’utilisation de Lync Server 2013 et Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="e20db-127">Keep in mind that these new features require the use of both Lync Server 2013 and Exchange 2013.</span></span> <span data-ttu-id="e20db-128">De plus, les utilisateurs qui espèrent tirer pleinement parti de ces nouvelles fonctionnalités doivent disposer de comptes sur Lync Server 2013 et Exchange 2013 et utiliser les versions les plus récentes du logiciel client (par exemple, Lync 2013).</span><span class="sxs-lookup"><span data-stu-id="e20db-128">In addition to that, users who hope to take full advantage of these new capabilities must have accounts on Lync Server 2013 and Exchange 2013, and must be using the latest versions of the client software (e.g., Lync 2013).</span></span> <span data-ttu-id="e20db-129">Par exemple, le magasin de contacts unifié n’est pas disponible pour les utilisateurs qui ont été hébergés sur Lync Server 2010. de même, les photos de haute résolution ne peuvent pas être affichées dans Lync 2010.</span><span class="sxs-lookup"><span data-stu-id="e20db-129">For example, the unified contact store is not available to users who have been homed on Lync Server 2010; likewise, high-resolution photos cannot be displayed in Lync 2010.</span></span>

<span data-ttu-id="e20db-130">Cette documentation fournit des informations sur l’intégration de Lync Server 2013 et Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="e20db-130">This documentation provides information on integrating Lync Server 2013 and Exchange 2013.</span></span> <span data-ttu-id="e20db-131">incluant des informations détaillées sur l’activation de nouvelles fonctionnalités telles que l’intégration de l’archivage et le magasin de contacts unifié.</span><span class="sxs-lookup"><span data-stu-id="e20db-131">including step-by-step information on enabling new features such archiving Integration and the unified contact store.</span></span> <span data-ttu-id="e20db-132">Ce document ne décrit pas la configuration initiale et la configuration de ces deux produits.</span><span class="sxs-lookup"><span data-stu-id="e20db-132">What this documentation does not do is discuss the initial setup and configuration of these two products.</span></span> <span data-ttu-id="e20db-133">Pour plus d’informations sur le déploiement de Lync Server 2013, voir le centre de technologie de Lync Server 2013 [https://go.microsoft.com/fwlink/p/?LinkId=246127](https://go.microsoft.com/fwlink/p/?linkid=246127) .</span><span class="sxs-lookup"><span data-stu-id="e20db-133">For details about deploying Lync Server 2013 see the Lync Server 2013 Tech Center at [https://go.microsoft.com/fwlink/p/?LinkId=246127](https://go.microsoft.com/fwlink/p/?linkid=246127).</span></span> <span data-ttu-id="e20db-134">Pour plus d’informations sur le déploiement d’Exchange 2013, consultez le centre de technologie Exchange 2013 à l’adresse [https://go.microsoft.com/fwlink/p/?LinkId=268528](https://go.microsoft.com/fwlink/p/?linkid=268528) .</span><span class="sxs-lookup"><span data-stu-id="e20db-134">For details about deploying Exchange 2013 see the Exchange 2013 Tech Center at [https://go.microsoft.com/fwlink/p/?LinkId=268528](https://go.microsoft.com/fwlink/p/?linkid=268528).</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="e20db-135">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="e20db-135">In This Section</span></span>

[<span data-ttu-id="e20db-136">Conditions préalables à l’intégration de Microsoft Lync Server 2013 et Microsoft Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="e20db-136">Prerequisites for integrating Microsoft Lync Server 2013 and Microsoft Exchange Server 2013</span></span>](lync-server-2013-prerequisites-for-integrating-with-exchange-server-2013.md)

[<span data-ttu-id="e20db-137">Configuration des applications partenaires dans Microsoft Lync Server 2013 et Microsoft Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="e20db-137">Configuring partner applications in Microsoft Lync Server 2013 and Microsoft Exchange Server 2013</span></span>](lync-server-2013-configuring-partner-applications-in-lync-server-2013-and-exchange-server-2013.md)

[<span data-ttu-id="e20db-138">Configuration de Microsoft Lync Server 2013 pour l’utilisation de l’archivage Microsoft Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="e20db-138">Configuring Microsoft Lync Server 2013 to use Microsoft Exchange Server 2013 archiving</span></span>](configuring-lync-server-2013-to-use-microsoft-exchange-server-2013-archiving.md)

[<span data-ttu-id="e20db-139">Configuration de Microsoft SharePoint Server 2013 pour rechercher des données Microsoft Lync Server 2013 archivées</span><span class="sxs-lookup"><span data-stu-id="e20db-139">Configuring Microsoft SharePoint Server 2013 to search for archived Microsoft Lync Server 2013 data</span></span>](lync-server-2013-configuring-microsoft-sharepoint-server-2013-to-search-for-archived-lync-server-2013-data.md)

[<span data-ttu-id="e20db-140">Configuration de Microsoft Lync Server 2013 pour utiliser le magasin de contacts unifié</span><span class="sxs-lookup"><span data-stu-id="e20db-140">Configuring Microsoft Lync Server 2013 to use the unified contact store</span></span>](lync-server-2013-configuring-lync-server-to-use-the-unified-contact-store.md)

[<span data-ttu-id="e20db-141">Configuration de l’utilisation de photos haute résolution dans Microsoft Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e20db-141">Configuring the use of high-resolution photos in Microsoft Lync Server 2013</span></span>](lync-server-2013-configuring-the-use-of-high-resolution-photos.md)

[<span data-ttu-id="e20db-142">Configuration de la messagerie unifiée Microsoft Exchange Server 2013 pour Microsoft Lync Server 2013 la messagerie vocale</span><span class="sxs-lookup"><span data-stu-id="e20db-142">Configuring Microsoft Exchange Server 2013 Unified Messaging for Microsoft Lync Server 2013 voice mail</span></span>](lync-server-2013-configuring-microsoft-exchange-server-2013-unified-messaging-for-lync-server-2013-voice-mail.md)

[<span data-ttu-id="e20db-143">Intégration de Microsoft Lync Server 2013 et Microsoft Outlook Web App 2013</span><span class="sxs-lookup"><span data-stu-id="e20db-143">Integrating Microsoft Lync Server 2013 and Microsoft Outlook Web App 2013</span></span>](lync-server-2013-integrating-lync-server-and-outlook-web-app-2013.md)

<span data-ttu-id="e20db-144"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e20db-144"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

