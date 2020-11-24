---
title: 'Lync Server 2013 : configuration du serveur de gestion principal'
description: 'Lync Server 2013 : configuration du serveur de gestion principal.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring the primary management server
ms:assetid: 44e2e9a8-c130-4c66-9871-80b1ff11b27c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204844(v=OCS.15)
ms:contentKeyID: 48183986
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 43f986f4f03e96cafa27dfdd302bb98a00d8b2ae
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395217"
---
# <a name="configuring-the-primary-management-server-in-lync-server-2013"></a><span data-ttu-id="be784-103">Configuration du serveur de gestion principal dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="be784-103">Configuring the primary management server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="be784-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="be784-104">

<span> </span></span></span>

<span data-ttu-id="be784-105">_**Dernière modification de la rubrique :** 2014-03-19_</span><span class="sxs-lookup"><span data-stu-id="be784-105">_**Topic Last Modified:** 2014-03-19_</span></span>

<span data-ttu-id="be784-106">Pour tirer pleinement parti des nouvelles fonctionnalités de l’analyse de l’intégrité intégrées aux administrateurs Microsoft Lync Server 2013, vous devez commencer par désigner un ordinateur pour agir en tant que serveur d’administration principal. sur cet ordinateur, vous devez ensuite installer System Center Operations Manager 2007 R2 ou System Center Operations Manager 2012.</span><span class="sxs-lookup"><span data-stu-id="be784-106">In order to take full advantage of the new health monitoring capabilities included in Microsoft Lync Server 2013 administrators must first designate a computer to act as your primary management server; on that computer you must then install System Center Operations Manager 2007 R2 or System Center Operations Manager 2012.</span></span> <span data-ttu-id="be784-107">Par ailleurs, vous devez installer une version prise en charge de SQL Server pour pouvoir fonctionner en tant que base de données principale Operations Manager.</span><span class="sxs-lookup"><span data-stu-id="be784-107">In addition, you must install a supported version of SQL Server to function as your Operations Manager back-end database.</span></span> <span data-ttu-id="be784-108">Si vous utilisez System Center Operations Manager 2012, vous pouvez utiliser l’une des versions suivantes de SQL Server comme base de données principale :</span><span class="sxs-lookup"><span data-stu-id="be784-108">If you are using System Center Operations Manager 2012 you can use any of the following versions of SQL Server as your back-end database:</span></span>

  - <span data-ttu-id="be784-109">SQL Server 2008 R2 Service Pack 1</span><span class="sxs-lookup"><span data-stu-id="be784-109">SQL Server 2008 R2 Service Pack 1</span></span>

  - <span data-ttu-id="be784-110">SQL Server 2008 R2 Service Pack 2</span><span class="sxs-lookup"><span data-stu-id="be784-110">SQL Server 2008 R2 Service Pack 2</span></span>

<span data-ttu-id="be784-111">Si vous utilisez System Center Operations Manager 2007 R2, il est recommandé d’installer SQL Server 2005 Service Pack 4 ou SQL Server 2008 Service Pack 3.</span><span class="sxs-lookup"><span data-stu-id="be784-111">If you are using System Center Operations Manager 2007 R2 it is recommended that you install either SQL Server 2005 Service Pack 4 or SQL Server 2008 Service Pack 3.</span></span> <span data-ttu-id="be784-112">Vous pouvez également utiliser SQL Server 2008 R2 en tant que base de données principale pour System Center Operations Manager 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="be784-112">You can also use SQL Server 2008 R2 as the backend database for System Center Operations Manager 2007 R2.</span></span> <span data-ttu-id="be784-113">Pour plus d’informations sur la configuration de SQL Server 2008 R2 pour l’utilisation de System Center Operations Manager 2007 R2, voir l’annexe 1 de cette documentation.</span><span class="sxs-lookup"><span data-stu-id="be784-113">See Appendix 1 of this documentation for more information on configuring SQL Server 2008 R2 to work with System Center Operations Manager 2007 R2.</span></span>

<span data-ttu-id="be784-114">Lorsque vous installez System Center Operations Manager 2012 ou System Center Operations Manager 2007 R2, vous devez installer tous les composants de ce produit, y compris :</span><span class="sxs-lookup"><span data-stu-id="be784-114">When you install System Center Operations Manager 2012 or System Center Operations Manager 2007 R2 you need to install all the components of that product, including:</span></span>

  - <span data-ttu-id="be784-115">Base de données opérationnelle</span><span class="sxs-lookup"><span data-stu-id="be784-115">Operational database</span></span>

  - <span data-ttu-id="be784-116">Serveur</span><span class="sxs-lookup"><span data-stu-id="be784-116">Server</span></span>

  - <span data-ttu-id="be784-117">Console</span><span class="sxs-lookup"><span data-stu-id="be784-117">Console</span></span>

  - <span data-ttu-id="be784-118">Cmdlets Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="be784-118">Windows PowerShell cmdlets</span></span>

  - <span data-ttu-id="be784-119">Console web</span><span class="sxs-lookup"><span data-stu-id="be784-119">Web console</span></span>

  - <span data-ttu-id="be784-120">Créateur de rapports</span><span class="sxs-lookup"><span data-stu-id="be784-120">Reporting</span></span>

  - <span data-ttu-id="be784-121">Entrepôt de données</span><span class="sxs-lookup"><span data-stu-id="be784-121">Data warehouse</span></span>

<span data-ttu-id="be784-122">Ces composants et leur installation ne seront pas abordés en détail dans ce document.</span><span class="sxs-lookup"><span data-stu-id="be784-122">These components and their installation will not be discussed in detail in this document.</span></span> <span data-ttu-id="be784-123">Pour plus d’informations sur System Center Operations Manager 2007 R2, voir la documentation Operations Manager 2007 R2 sur <https://go.microsoft.com/fwlink/p/?linkid=257526> le document System Center Operations manager 2012 <https://go.microsoft.com/fwlink/p/?linkid=257527> .</span><span class="sxs-lookup"><span data-stu-id="be784-123">For details about System Center Operations Manager 2007 R2, see the Operations Manager 2007 R2 documentation at <https://go.microsoft.com/fwlink/p/?linkid=257526> and the System Center Operations Manager 2012 documentation at <https://go.microsoft.com/fwlink/p/?linkid=257527>.</span></span> <span data-ttu-id="be784-124">Suivez ces instructions si vous envisagez d’utiliser SQL Server 2005 ou SQL Server 2008 Service Pack 1 comme base de données principale.</span><span class="sxs-lookup"><span data-stu-id="be784-124">You should follow those instructions if you are going to use SQL Server 2005 or SQL Server 2008 Service Pack 1 as your back-end database.</span></span>

<span data-ttu-id="be784-125">Si vous utilisez System Center Operations Manager 2012, vous pouvez utiliser SQL Server 2012 comme base de données principale.</span><span class="sxs-lookup"><span data-stu-id="be784-125">If you are using System Center Operations Manager 2012 then you can use SQL Server 2012 as your back-end database.</span></span> <span data-ttu-id="be784-126">Pour plus d’informations sur SQL Server 2012, voir la documentation en ligne pour SQL Server 2012 à l’adresse [https://go.microsoft.com/fwlink/p/?LinkId=257528](https://go.microsoft.com/fwlink/p/?linkid=257528) .</span><span class="sxs-lookup"><span data-stu-id="be784-126">For details about SQL Server 2012, see Books Online for SQL Server 2012 at [https://go.microsoft.com/fwlink/p/?LinkId=257528](https://go.microsoft.com/fwlink/p/?linkid=257528).</span></span>

<span data-ttu-id="be784-127">Gardez à l’esprit que vous ne pouvez avoir qu’un seul serveur de gestion principal par déploiement de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="be784-127">Keep in mind that you can only have a single Primary Management Server per Lync Server deployment.</span></span> <span data-ttu-id="be784-128">Par ailleurs, si vous pouvez utiliser System Center Operations Manager 2012 ou System Center Operations Manager 2007 R2, vous ne pouvez pas exécuter les deux applications en même temps, vous devez en choisir une.</span><span class="sxs-lookup"><span data-stu-id="be784-128">Also, while you can use either System Center Operations Manager 2012 or System Center Operations Manager 2007 R2, you cannot run the two applications simultaneously—you must choose one or the other.</span></span> <span data-ttu-id="be784-129">Par exemple, si vous exécutez System Center Operations Manager 2012, tous vos agents System Center doivent également exécuter System Center Operations Manager 2012.</span><span class="sxs-lookup"><span data-stu-id="be784-129">For example, if you are running System Center Operations Manager 2012 then all your System Center agents must also be running System Center Operations Manager 2012.</span></span> <span data-ttu-id="be784-130">Vous ne pouvez pas disposer de certains agents exécutant System Center Operations Manager 2012 et d’autres agents exécutant System Center Operations Manager 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="be784-130">You cannot have some agents running System Center Operations Manager 2012 and other agents running System Center Operations Manager 2007 R2.</span></span>

<span data-ttu-id="be784-131"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="be784-131"></div>

<span> </span>

</div>

</div>

</span></span></div>

