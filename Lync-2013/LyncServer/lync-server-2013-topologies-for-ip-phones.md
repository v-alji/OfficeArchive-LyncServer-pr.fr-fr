---
title: 'Lync Server 2013 : topologies pour téléphones IP'
description: 'Lync Server 2013 : topologies pour téléphones IP.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Topologies for IP phones
ms:assetid: 26ebffcf-43ff-4e70-847d-0fbc90e94e57
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425740(v=OCS.15)
ms:contentKeyID: 48183662
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7a151a83a69e1f7e14dcbed8d8ab1038157fa839
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439662"
---
# <a name="topologies-for-ip-phones-in-lync-server-2013"></a><span data-ttu-id="8bd1f-103">Topologies pour téléphones IP dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8bd1f-103">Topologies for IP phones in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8bd1f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8bd1f-104">

<span> </span></span></span>

<span data-ttu-id="8bd1f-105">_**Dernière modification de la rubrique :** 2012-06-21_</span><span class="sxs-lookup"><span data-stu-id="8bd1f-105">_**Topic Last Modified:** 2012-06-21_</span></span>

<span data-ttu-id="8bd1f-106">Cette section fournit une vue d’ensemble du processus de connectivité et explique les différences entre la connexion d’un téléphone IP à un réseau interne et externe.</span><span class="sxs-lookup"><span data-stu-id="8bd1f-106">This section provides an overview of the connectivity process and explains the differences between how an IP phone connects in an internal and external network.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="8bd1f-107">Lync Server prend en charge les téléphones IP suivants : le téléphone de bureau Aastra 6721ip, Aastra 6725ip Phone, le téléphone IP HP 4110 (téléphone pour la zone commune 4120), le numéro de téléphone IP, le téléphone de bureau, le téléphone de bureau, le téléphone de bureau, le téléphone de bureau et l’Polycom Polycom.</span><span class="sxs-lookup"><span data-stu-id="8bd1f-107">Lync Server provides support for the following IP phones: the Aastra 6721ip common area phone, Aastra 6725ip desk phone, HP 4110 IP Phone (common area phone), HP 4120 IP Phone (desk phone), Polycom CX600 IP desk phone, Polycom CX700 IP desk phone, Polycom CX500 IP common area phone, and Polycom CX3000 IP conference phone.</span></span> <span data-ttu-id="8bd1f-108">De ces téléphones, mais le Polycom CX700 peut exécuter Lync Phone Edition.</span><span class="sxs-lookup"><span data-stu-id="8bd1f-108">Of those phones, all but the Polycom CX700 can run Lync Phone Edition.</span></span>



</div>

<span data-ttu-id="8bd1f-109">Le diagramme suivant décrit tous les composants impliqués dans la connectivité des appareils au sein de l’environnement d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="8bd1f-109">The following diagram describes all the components involved in device connectivity within the corporate environment.</span></span>

<span data-ttu-id="8bd1f-110">**Topologie interne**</span><span class="sxs-lookup"><span data-stu-id="8bd1f-110">**Internal Topology**</span></span>

<span data-ttu-id="8bd1f-111">![3d88893e-df57-46e3-855a-a1d24589030a](images/Gg425740.3d88893e-df57-46e3-855a-a1d24589030a(OCS.15).jpg "3d88893e-df57-46e3-855a-a1d24589030a")</span><span class="sxs-lookup"><span data-stu-id="8bd1f-111">![3d88893e-df57-46e3-855a-a1d24589030a](images/Gg425740.3d88893e-df57-46e3-855a-a1d24589030a(OCS.15).jpg "3d88893e-df57-46e3-855a-a1d24589030a")</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="8bd1f-112">La figure précédente est une représentation logique qui n’est pas une vue d’ensemble physique.</span><span class="sxs-lookup"><span data-stu-id="8bd1f-112">The previous figure is a logical representation, not a physical overview.</span></span> <span data-ttu-id="8bd1f-113">Par exemple, les services de domaine Active Directory (AD DS) se trouvent rarement sur le même ordinateur que les composants serveur Lync.</span><span class="sxs-lookup"><span data-stu-id="8bd1f-113">For example, Active Directory Domain Services (AD DS) is rarely located on the same machine as any Lync Server components.</span></span> <span data-ttu-id="8bd1f-114">Le magasin utilisateur peut se trouver sur le serveur principal ou sur les serveurs d’archivage et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="8bd1f-114">The user store can be located on the Back End Server or on the Archiving and Monitoring Servers.</span></span> <span data-ttu-id="8bd1f-115">Lync Server Management Shell, le serveur Web et les services de mise à jour font partie du rôle serveur frontal.</span><span class="sxs-lookup"><span data-stu-id="8bd1f-115">The Lync Server Management Shell, web server, and update services are all part of the Front End Server role.</span></span>



</div>

<span data-ttu-id="8bd1f-116">Le diagramme suivant fournit une vue d’ensemble des composants impliqués lorsque l’appareil se trouve en dehors du réseau d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="8bd1f-116">The following diagram provides an overview of the components involved when the device is located outside the corporate network.</span></span>

<span data-ttu-id="8bd1f-117">**Topologie externe**</span><span class="sxs-lookup"><span data-stu-id="8bd1f-117">**External Topology**</span></span>

<span data-ttu-id="8bd1f-118">![8ce6bb8e-b89c-4c4e-ac6d-41ac6c68f6f3](images/Gg425740.8ce6bb8e-b89c-4c4e-ac6d-41ac6c68f6f3(OCS.15).jpg "8ce6bb8e-b89c-4c4e-ac6d-41ac6c68f6f3")</span><span class="sxs-lookup"><span data-stu-id="8bd1f-118">![8ce6bb8e-b89c-4c4e-ac6d-41ac6c68f6f3](images/Gg425740.8ce6bb8e-b89c-4c4e-ac6d-41ac6c68f6f3(OCS.15).jpg "8ce6bb8e-b89c-4c4e-ac6d-41ac6c68f6f3")</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="8bd1f-119">Le service Web de mise à jour d’appareil fournit un site Web interne et externe, mais seul le premier est affiché ici.</span><span class="sxs-lookup"><span data-stu-id="8bd1f-119">The Device Update Web service provides an external and internal website, but only the external one is shown here.</span></span><BR><span data-ttu-id="8bd1f-120">L’emplacement du Bureau d’enregistrement et l’URL du service Web de mise à jour de l’appareil pour l’organisation doivent être publiés dans DNS si l’accès externe doit être activé.</span><span class="sxs-lookup"><span data-stu-id="8bd1f-120">The location of the Registrar and the URL of the Device Update Web service for the organization must be published in DNS if external access is to be enabled.</span></span> <span data-ttu-id="8bd1f-121">Par ailleurs, le serveur de périphérie doit être déployé et correctement configuré pour autoriser les communications externes entre l’appareil et l’environnement d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="8bd1f-121">Additionally, the Edge Server must be deployed and correctly configured to allow external communications from the device to the corporate environment and back.</span></span> <span data-ttu-id="8bd1f-122">Ce paramètre est omis du diagramme précédent, car le déploiement Edge n’est pas spécifique à la connectivité de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="8bd1f-122">This is omitted from the previous diagram because Edge deployment is not specific to device connectivity.</span></span>



<span data-ttu-id="8bd1f-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8bd1f-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

