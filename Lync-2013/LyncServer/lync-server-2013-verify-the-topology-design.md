---
title: 'Lync Server 2013 : Vérification de la conception de la topologie'
description: 'Lync Server 2013 : vérifier la conception topologique.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Verify the topology design
ms:assetid: c1b61814-239e-4101-aab0-de3db1d8793c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412951(v=OCS.15)
ms:contentKeyID: 48185311
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: cb1e65343aacddbc11d3b909dfdff715503cab93
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438910"
---
# <a name="verify-the-topology-design-in-lync-server-2013"></a><span data-ttu-id="3b7c4-103">Vérification de la conception de la topologie dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3b7c4-103">Verify the topology design in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3b7c4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3b7c4-104">

<span> </span></span></span>

<span data-ttu-id="3b7c4-105">_**Dernière modification de la rubrique :** 2012-01-02_</span><span class="sxs-lookup"><span data-stu-id="3b7c4-105">_**Topic Last Modified:** 2012-01-02_</span></span>

<span data-ttu-id="3b7c4-106">Le générateur de topologie vérifie automatiquement la topologie.</span><span class="sxs-lookup"><span data-stu-id="3b7c4-106">Topology Builder automatically verifies the topology.</span></span> <span data-ttu-id="3b7c4-107">Toute erreur de topologie se caractérise par une erreur de validation, indiquée par l’icône d’erreur de validation située en regard du rôle de serveur.</span><span class="sxs-lookup"><span data-stu-id="3b7c4-107">Any topology error is identified as a validation error, indicated by the validation error icon next to the server role.</span></span> <span data-ttu-id="3b7c4-108">Il est important de vérifier également que la topologie représente correctement la topologie de votre déploiement.</span><span class="sxs-lookup"><span data-stu-id="3b7c4-108">It is important to also verify that the topology correctly represents the topology for your deployment.</span></span>

<div>

## <a name="to-verify-the-topology-prior-to-publication"></a><span data-ttu-id="3b7c4-109">Pour vérifier la topologie avant la publication</span><span class="sxs-lookup"><span data-stu-id="3b7c4-109">To verify the topology prior to publication</span></span>

1.  <span data-ttu-id="3b7c4-110">Vérifiez que toutes les URL simples sont configurées correctement.</span><span class="sxs-lookup"><span data-stu-id="3b7c4-110">Check that all simple URLs are configured correctly.</span></span>

2.  <span data-ttu-id="3b7c4-111">Vérifiez que le serveur SQL Server est en ligne et que l’ordinateur sur lequel le Générateur de topologies est installé peut y accéder. Vérifiez également que les règles de pare-feu nécessaires sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="3b7c4-111">Confirm that the SQL Server-based server is online and available to the computer where Topology Builder is installed, including any necessary firewall rules.</span></span>

3.  <span data-ttu-id="3b7c4-112">Vérifiez que le partage de fichiers est disponible et qu’il dispose des autorisations appropriées définies.</span><span class="sxs-lookup"><span data-stu-id="3b7c4-112">Confirm that the file share is available and has the proper permissions defined.</span></span>

4.  <span data-ttu-id="3b7c4-113">Confirmez que les rôles serveur corrects qui répondent à la configuration requise pour le déploiement sont définis dans la topologie.</span><span class="sxs-lookup"><span data-stu-id="3b7c4-113">Confirm that the correct server roles that meet the deployment requirements are defined in the topology.</span></span>

5.  <span data-ttu-id="3b7c4-114">Vérifiez que les serveurs existent dans les services de domaine Active Directory (AD FS).</span><span class="sxs-lookup"><span data-stu-id="3b7c4-114">Verify that the servers exist in Active Directory Domain Services.</span></span> <span data-ttu-id="3b7c4-115">Ce problème se produit automatiquement si vous avez rejoint le domaine.</span><span class="sxs-lookup"><span data-stu-id="3b7c4-115">This will happen automatically if you have joined the servers to the domain.</span></span>

<span data-ttu-id="3b7c4-116">Lorsque vous avez vérifié la topologie et qu’aucune erreur de validation n’a été détectée, vous êtes prêt à publier la topologie.</span><span class="sxs-lookup"><span data-stu-id="3b7c4-116">When you have verified the topology and there are no validation errors, you should be ready to publish the topology.</span></span> <span data-ttu-id="3b7c4-117">S’il existe des erreurs de validation, vous devez les corriger avant de pouvoir publier la topologie.</span><span class="sxs-lookup"><span data-stu-id="3b7c4-117">If there are validation errors, you must correct these before you can publish the topology.</span></span> <span data-ttu-id="3b7c4-118">Pour plus d’informations sur la publication de votre topologie, voir [publier la topologie dans Lync Server 2013](lync-server-2013-publish-the-topology.md).</span><span class="sxs-lookup"><span data-stu-id="3b7c4-118">For details about publishing your topology, see [Publish the topology in Lync Server 2013](lync-server-2013-publish-the-topology.md).</span></span>

<span data-ttu-id="3b7c4-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3b7c4-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

