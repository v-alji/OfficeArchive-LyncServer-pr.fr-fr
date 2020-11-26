---
title: Liste de vérification de déploiement de Lync Server 2013 pour les conférences A/V
description: Liste de vérification de déploiement de Lync Server 2013 pour les conférences A/V.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment checklist for A/V conferencing
ms:assetid: 6d47426f-6559-407b-9ac1-2453f0b7a2a2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ619183(v=OCS.15)
ms:contentKeyID: 49733684
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d9a4584172ed4c01eb163ea51aa4f62c2ce75185
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429754"
---
# <a name="deployment-checklist-for-av-conferencing-in-lync-server-2013"></a><span data-ttu-id="aa5b9-103">Liste de vérification de déploiement pour les conférences A/V dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="aa5b9-103">Deployment checklist for A/V conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="aa5b9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="aa5b9-104">

<span> </span></span></span>

<span data-ttu-id="aa5b9-105">_**Dernière modification de la rubrique :** 2012-09-30_</span><span class="sxs-lookup"><span data-stu-id="aa5b9-105">_**Topic Last Modified:** 2012-09-30_</span></span>

<span data-ttu-id="aa5b9-106">Comme pour le déploiement de vos autres composants Lync Server 2013, le déploiement de conférences A/V nécessite l’utilisation du générateur de topologie pour créer et publier une topologie incluant des conférences.</span><span class="sxs-lookup"><span data-stu-id="aa5b9-106">As with deployment of your other Lync Server 2013 components, deployment of A/V conferencing requires that you use Topology Builder to create and publish a topology that incorporates conferencing.</span></span>

<div>

## <a name="deployment-sequence"></a><span data-ttu-id="aa5b9-107">Séquence de déploiement</span><span class="sxs-lookup"><span data-stu-id="aa5b9-107">Deployment Sequence</span></span>

<span data-ttu-id="aa5b9-108">Vous pouvez déployer des conférences en même temps que le déploiement de votre topologie initiale ou après le déploiement d’au moins un pool frontal ou d’un serveur Standard Edition Server.</span><span class="sxs-lookup"><span data-stu-id="aa5b9-108">You can deploy conferencing at the same time that you deploy your initial topology or after you have deployed at least one Front End pool or Standard Edition server.</span></span>

</div>

<div>

## <a name="conferencing-deployment-process"></a><span data-ttu-id="aa5b9-109">Processus de déploiement de conférences</span><span class="sxs-lookup"><span data-stu-id="aa5b9-109">Conferencing Deployment Process</span></span>

<span data-ttu-id="aa5b9-110">Le tableau suivant fournit une vue d’ensemble des étapes nécessaires au déploiement des conférences dans une topologie existante.</span><span class="sxs-lookup"><span data-stu-id="aa5b9-110">The following table provides an overview of the steps required to deploy conferencing into an existing topology.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="aa5b9-111">Phase</span><span class="sxs-lookup"><span data-stu-id="aa5b9-111">Phase</span></span></th>
<th><span data-ttu-id="aa5b9-112">Étapes</span><span class="sxs-lookup"><span data-stu-id="aa5b9-112">Steps</span></span></th>
<th><span data-ttu-id="aa5b9-113">Rôles et appartenance aux groupes</span><span class="sxs-lookup"><span data-stu-id="aa5b9-113">Roles and group memberships</span></span></th>
<th><span data-ttu-id="aa5b9-114">Documentation</span><span class="sxs-lookup"><span data-stu-id="aa5b9-114">Documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aa5b9-115"><strong>Installer le matériel et les logiciels prérequis</strong></span><span class="sxs-lookup"><span data-stu-id="aa5b9-115"><strong>Install prerequisite hardware and software</strong></span></span></p></td>
<td><p><span data-ttu-id="aa5b9-116">Les conférences s’exécutent sur des serveurs front-end d’un pool frontal et de serveurs Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="aa5b9-116">Conferencing runs on Front End Servers of a Front End pool and Standard Edition servers.</span></span> <span data-ttu-id="aa5b9-117">Aucune configuration matérielle ou logicielle supplémentaire n’est requise en dehors de celle nécessaire à l’installation de ces serveurs.</span><span class="sxs-lookup"><span data-stu-id="aa5b9-117">It has no additional hardware or software requirements beyond what is required to install those servers.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="aa5b9-118">Lync Server 2013 utilise Office Web Apps et Office Web Apps Server pour gérer le partage et le rendu des présentations PowerPoint.</span><span class="sxs-lookup"><span data-stu-id="aa5b9-118">Lync Server 2013 uses Office Web Apps and the Office Web Apps Server to handle sharing and rendering of PowerPoint presentations.</span></span> <span data-ttu-id="aa5b9-119">Pour plus d’informations sur l’installation et la configuration d’Office Web Apps Server, reportez-vous à la rubrique <A href="lync-server-2013-enabling-office-web-apps-server-and-lync-server-2013.md">configuration de l’intégration avec Office Web Apps Server et Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="aa5b9-119">For details about installing and configuring the Office Web Apps Server, see <A href="lync-server-2013-enabling-office-web-apps-server-and-lync-server-2013.md">Configuring integration with Office Web Apps Server and Lync Server 2013</A>.</span></span>


</div></td>
<td><p><span data-ttu-id="aa5b9-120">Utilisateur du domaine qui est membre du groupe Administrateurs local</span><span class="sxs-lookup"><span data-stu-id="aa5b9-120">Domain user who is a member of the local Administrators group</span></span></p></td>
<td><p><span data-ttu-id="aa5b9-121"><a href="lync-server-2013-supported-hardware.md">Matériel compatible pour Lync Server 2013</a> dans la documentation de prise en charge</span><span class="sxs-lookup"><span data-stu-id="aa5b9-121"><a href="lync-server-2013-supported-hardware.md">Supported hardware for Lync Server 2013</a> in the Supportability documentation</span></span></p>
<p><span data-ttu-id="aa5b9-122"><a href="lync-server-2013-server-software-and-infrastructure-support.md">Support du logiciel serveur et de l’infrastructure dans Lync Server 2013</a> dans la documentation de prise en charge</span><span class="sxs-lookup"><span data-stu-id="aa5b9-122"><a href="lync-server-2013-server-software-and-infrastructure-support.md">Server software and infrastructure support in Lync Server 2013</a> in the Supportability documentation</span></span></p>
<p><span data-ttu-id="aa5b9-123"><a href="lync-server-2013-determining-your-system-requirements.md">Déterminez la configuration système requise pour Lync Server 2013</a> dans la documentation de planification.</span><span class="sxs-lookup"><span data-stu-id="aa5b9-123"><a href="lync-server-2013-determining-your-system-requirements.md">Determining your system requirements for Lync Server 2013</a> in the Planning documentation.</span></span></p>
<p><span data-ttu-id="aa5b9-124"><a href="lync-server-2013-technical-requirements-for-archiving.md">Configuration technique requise pour l’archivage dans Lync Server 2013</a> dans la documentation de planification.</span><span class="sxs-lookup"><span data-stu-id="aa5b9-124"><a href="lync-server-2013-technical-requirements-for-archiving.md">Technical requirements for Archiving in Lync Server 2013</a> in the Planning documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa5b9-125"><strong>Création de la topologie interne appropriée pour prendre en charge la conférence</strong></span><span class="sxs-lookup"><span data-stu-id="aa5b9-125"><strong>Create the appropriate internal topology to support conferencing</strong></span></span></p></td>
<td><p><span data-ttu-id="aa5b9-126">Exécutez le générateur de topologie pour ajouter des conférences à la topologie, puis publiez la topologie.</span><span class="sxs-lookup"><span data-stu-id="aa5b9-126">Run Topology Builder to add conferencing to the topology, and then publish the topology.</span></span></p></td>
<td><p><span data-ttu-id="aa5b9-127">Pour définir une topologie, un compte membre du groupe Utilisateurs local</span><span class="sxs-lookup"><span data-stu-id="aa5b9-127">To define a topology, an account that is a member of the local Users group</span></span></p>
<p><span data-ttu-id="aa5b9-128">Pour publier la topologie, un compte membre du groupe administrateurs de domaine et du groupe RTCUniversalServerAdmins et qui dispose des autorisations de contrôle total (lecture/écriture/modification) sur le partage de fichiers à utiliser pour le magasin de fichiers 2013 Lync Server (de manière à ce que le générateur de topologie puisse configurer les DACL requis)</span><span class="sxs-lookup"><span data-stu-id="aa5b9-128">To publish the topology, an account that is a member of the Domain Admins group and RTCUniversalServerAdmins group, and that has full control permissions (read/write/modify) on the file share to be used for the Lync Server 2013 file store (so that Topology Builder can configure the required DACLs)</span></span></p></td>
<td><p><span data-ttu-id="aa5b9-129"><a href="lync-server-2013-define-and-configure-a-topology-in-topology-builder.md">Définissez et configurez une topologie dans le générateur de topologies de Lync Server 2013</a> dans la documentation de déploiement.</span><span class="sxs-lookup"><span data-stu-id="aa5b9-129"><a href="lync-server-2013-define-and-configure-a-topology-in-topology-builder.md">Define and configure a topology in Topology Builder for Lync Server 2013</a> in the Deployment documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa5b9-130"><strong>Configuration des stratégies de conférence et de la prise en charge</strong></span><span class="sxs-lookup"><span data-stu-id="aa5b9-130"><strong>Configure conferencing policies and support</strong></span></span></p></td>
<td><p><span data-ttu-id="aa5b9-131">Utilisez le panneau de configuration de Lync Server 2013 ou Lync Server Management Shell pour configurer les paramètres de conférence.</span><span class="sxs-lookup"><span data-stu-id="aa5b9-131">Use the Lync Server 2013 Control Panel or Lync Server Management Shell to configure conferencing settings.</span></span></p></td>
<td><p><span data-ttu-id="aa5b9-132">Groupe RTCUniversalServerAdmins (Windows PowerShell uniquement) ou affecter des utilisateurs au rôle [] ou CSAdministrator</span><span class="sxs-lookup"><span data-stu-id="aa5b9-132">RTCUniversalServerAdmins group (Windows PowerShell only) or assign users to the [] or CSAdministrator role</span></span></p></td>
<td><p><span data-ttu-id="aa5b9-133"><a href="lync-server-2013-conferencing-policies.md">Stratégies de conférence dans Lync Server 2013</a> dans la documentation opérations.</span><span class="sxs-lookup"><span data-stu-id="aa5b9-133"><a href="lync-server-2013-conferencing-policies.md">Conferencing policies in Lync Server 2013</a> in the Operations documentation.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="see-also"></a><span data-ttu-id="aa5b9-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aa5b9-134">See Also</span></span>


[<span data-ttu-id="aa5b9-135">Vue d’ensemble des conférences dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="aa5b9-135">Overview of conferencing in Lync Server 2013</span></span>](lync-server-2013-overview-of-conferencing.md)  
[<span data-ttu-id="aa5b9-136">Définition de la configuration requise pour les conférences dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="aa5b9-136">Defining your requirements for conferencing in Lync Server 2013</span></span>](lync-server-2013-defining-your-requirements-for-conferencing.md)  
  

<span data-ttu-id="aa5b9-137"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="aa5b9-137"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

