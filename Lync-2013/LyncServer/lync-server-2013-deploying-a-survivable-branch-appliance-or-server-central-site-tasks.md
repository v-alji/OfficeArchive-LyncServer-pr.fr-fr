---
title: Déploiement d’un Survivable Branch Appliance ou d’un serveur Survivable Branch Server - Tâches pour un site central
description: Déploiement d’une unité ou d’un serveur de succursale Survivable.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying a Survivable Branch Appliance or Server - central site tasks
ms:assetid: 0f631a36-fc2e-41cd-8a0d-f27e84f4a89e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398189(v=OCS.15)
ms:contentKeyID: 48183422
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4460ea215d6fc80ee89f1ca9bc42f08ac5d14617
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430132"
---
# <a name="deploying-a-survivable-branch-appliance-or-server-with-lync-server-2013---central-site-tasks"></a><span data-ttu-id="e0f4a-103">Déploiement d’un Survivable Branch Appliance ou d’un serveur Survivable Branch Server avec Lync Server 2013 - Tâches pour un site central</span><span class="sxs-lookup"><span data-stu-id="e0f4a-103">Deploying a Survivable Branch Appliance or Server with Lync Server 2013 - central site tasks</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e0f4a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e0f4a-104">

<span> </span></span></span>

<span data-ttu-id="e0f4a-105">_**Dernière modification de la rubrique :** 2012-10-18_</span><span class="sxs-lookup"><span data-stu-id="e0f4a-105">_**Topic Last Modified:** 2012-10-18_</span></span>

<span data-ttu-id="e0f4a-106">Suivez les étapes décrites dans cette section sur le site central.</span><span class="sxs-lookup"><span data-stu-id="e0f4a-106">Complete the tasks in this section at the central site.</span></span> <span data-ttu-id="e0f4a-107">Si vous déployez un serveur de succursales survivant, ignorez la première tâche.</span><span class="sxs-lookup"><span data-stu-id="e0f4a-107">If you’re deploying a Survivable Branch Server, skip the first task.</span></span>

<div>


> [!IMPORTANT]
> <span data-ttu-id="e0f4a-108">Avant d’effectuer les tâches décrites dans cette section, les conditions suivantes doivent être en place :</span><span class="sxs-lookup"><span data-stu-id="e0f4a-108">Before you perform the tasks in this section, the following conditions must be in place:</span></span> 
> <UL>
> <LI>
> <P><span data-ttu-id="e0f4a-109">Le serveur Lync doit être configuré sur le site central.</span><span class="sxs-lookup"><span data-stu-id="e0f4a-109">Lync Server must be set up at the central site.</span></span></P>
> <LI>
> <P><span data-ttu-id="e0f4a-110">Un technicien d’installation sur le site de succursale doit être ajouté au groupe RTCUniversalSBATechnicians.</span><span class="sxs-lookup"><span data-stu-id="e0f4a-110">An installation technician at the branch site must be added to the RTCUniversalSBATechnicians group.</span></span></P></LI></UL><span data-ttu-id="e0f4a-111">Par ailleurs, il est recommandé d’effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="e0f4a-111">In addition, we recommend that you do the following:</span></span>
> <UL>
> <LI>
> <P><span data-ttu-id="e0f4a-112">Déploiement d’un serveur DHCP sur chaque site de succursale pour permettre aux clients d’obtenir des adresses IP.</span><span class="sxs-lookup"><span data-stu-id="e0f4a-112">Deploy a DHCP server at each branch site to enable clients to obtain IP addresses.</span></span></P>
> <LI>
> <P><span data-ttu-id="e0f4a-113">À la place du déploiement d’un serveur DHCP sur chaque site de succursale, activez le protocole DHCP de Lync Server sur l’appareil de succursales survivant ou sur le serveur de succursales survivant en utilisant l’applet de cmdlet Lync Server Management Shell <STRONG>Set-CsRegistrarConfiguration – EnableDHCPServer $true</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="e0f4a-113">As an alternative to deploying a DHCP server at each branch site, enable Lync Server DHCP on the Survivable Branch Appliance or Survivable Branch Server by using the Lync Server Management Shell cmdlet <STRONG>Set-CsRegistrarConfiguration –EnableDHCPServer $true</STRONG>.</span></span> <span data-ttu-id="e0f4a-114">Pour plus d’informations, reportez-vous à la section « Configuration matérielle et logicielle requise » dans la rubrique Configuration de la <A href="lync-server-2013-branch-site-resiliency-requirements.md">résilience de site pour Lync Server 2013</A> dans la documentation de planification.</span><span class="sxs-lookup"><span data-stu-id="e0f4a-114">For details, see the “Hardware and Software Requirements” section of <A href="lync-server-2013-branch-site-resiliency-requirements.md">Branch-site resiliency requirements for Lync Server 2013</A> in the Planning documentation.</span></span></P></LI></UL>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="e0f4a-115">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="e0f4a-115">In This Section</span></span>

  - [<span data-ttu-id="e0f4a-116">Ajout d’un Survivable Branch Appliance à Active Directory dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e0f4a-116">Add a Survivable Branch Appliance to Active Directory in Lync Server 2013</span></span>](lync-server-2013-add-a-survivable-branch-appliance-to-active-directory.md)

  - [<span data-ttu-id="e0f4a-117">Ajout des sites de succursale à votre topologie dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e0f4a-117">Add branch sites to your topology in Lync Server 2013</span></span>](lync-server-2013-add-branch-sites-to-your-topology.md)

  - [<span data-ttu-id="e0f4a-118">Définition d’un Survivable Branch Appliance ou d’un serveur Survivable Branch Server dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e0f4a-118">Define a Survivable Branch Appliance or Server in Lync Server 2013</span></span>](lync-server-2013-define-a-survivable-branch-appliance-or-server.md)

<span data-ttu-id="e0f4a-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e0f4a-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

