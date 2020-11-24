---
title: Configuration des serveurs d’applications approuvées
description: Configurer des serveurs d’application approuvés.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Configure trusted application servers
ms:assetid: 20c3815f-3048-4940-8c0f-cdfcd0801d5d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204735(v=OCS.15)
ms:contentKeyID: 48183592
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 39f439ea3e5996e0a3464540069024b70c415e3d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394433"
---
# <a name="configure-trusted-application-servers"></a><span data-ttu-id="5b4b2-103">Configuration des serveurs d’applications approuvées</span><span class="sxs-lookup"><span data-stu-id="5b4b2-103">Configure trusted application servers</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5b4b2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5b4b2-104">

<span> </span></span></span>

<span data-ttu-id="5b4b2-105">_**Dernière modification de la rubrique :** 2012-10-11_</span><span class="sxs-lookup"><span data-stu-id="5b4b2-105">_**Topic Last Modified:** 2012-10-11_</span></span>

<span data-ttu-id="5b4b2-106">Dans un environnement mixte, si vous créez un nouveau serveur d’applications de confiance, vous devez définir le pool de sauts suivant comme pool Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="5b4b2-106">In a mixed environment, if you create a new trusted application server, you must set the next hop pool to be a Lync Server 2013 pool.</span></span> <span data-ttu-id="5b4b2-107">Dans un environnement mixte, le pool Lync Server 2010 hérité et le pool 2013 du serveur Lync apparaissent dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="5b4b2-107">In a mixed environment, both the legacy Lync Server 2010 pool and the Lync Server 2013 pool appear in the drop down list.</span></span> <span data-ttu-id="5b4b2-108">La sélection du pool hérité n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="5b4b2-108">Selecting the legacy pool is not supported.</span></span>

<span data-ttu-id="5b4b2-109">**Sélectionner Lync Server 2013 comme tronçon suivant lors de la création d’un serveur d’applications de confiance**</span><span class="sxs-lookup"><span data-stu-id="5b4b2-109">**Select Lync Server 2013 as next hop when creating a Trusted application server**</span></span>

1.  <span data-ttu-id="5b4b2-110">Ouvrez le générateur de topologie.</span><span class="sxs-lookup"><span data-stu-id="5b4b2-110">Open Topology Builder.</span></span>

2.  <span data-ttu-id="5b4b2-111">Dans le volet de gauche, cliquez avec le bouton droit sur **serveurs d’applications de confiance** , puis cliquez sur **nouveau pool d’applications de confiance**.</span><span class="sxs-lookup"><span data-stu-id="5b4b2-111">In the left pane, right click **Trusted application servers** and click **New Trusted Application Pool**.</span></span>

3.  <span data-ttu-id="5b4b2-112">Entrez le **nom de domaine complet (FQDN)** du pool d’applications de confiance et sélectionnez s’il s’agit d’un serveur unique ou d’un serveur multiple.</span><span class="sxs-lookup"><span data-stu-id="5b4b2-112">Enter the **Pool FQDN** of the trusted application pool and select whether it will be a single-server or multiple-server.</span></span>

4.  <span data-ttu-id="5b4b2-113">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="5b4b2-113">Click **Next**.</span></span>

5.  <span data-ttu-id="5b4b2-114">Dans la page **Sélectionner le tronçon suivant** , dans la liste, sélectionnez le pool frontal de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="5b4b2-114">On the **Select the next hop** page, from the list, select the Lync Server 2013 Front End pool.</span></span>

6.  <span data-ttu-id="5b4b2-115">Cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="5b4b2-115">Click **Finish**.</span></span>

7.  <span data-ttu-id="5b4b2-116">Sélectionnez le nœud supérieur **serveur Lync** et dans le menu **action** , sélectionnez **publier**.</span><span class="sxs-lookup"><span data-stu-id="5b4b2-116">Select the top node **Lync Server** and from the **Action** menu, select **Publish**.</span></span>
    
    <span data-ttu-id="5b4b2-117">Vérifiez que le **pool d’applications approuvé** a été créé avec succès et est associé au pool frontal approprié.</span><span class="sxs-lookup"><span data-stu-id="5b4b2-117">Verify the **Trusted Application Pool** has been created successfully and is associated with the correct Front End pool.</span></span>

<span data-ttu-id="5b4b2-118"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5b4b2-118"></div>

<span> </span>

</div>

</div>

</span></span></div>

