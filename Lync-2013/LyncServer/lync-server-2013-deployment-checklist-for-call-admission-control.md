---
title: 'Lync Server 2013 : Liste de vérification du déploiement pour le contrôle d’admission des appels'
description: 'Lync Server 2013 : liste de vérification de déploiement pour le contrôle d’admission des appels.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment checklist for call admission control
ms:assetid: 7e56a169-3e63-44ab-bf28-1fdeb52381c8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398631(v=OCS.15)
ms:contentKeyID: 48184621
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ea5b16d41228faf01637e7e0d78f5ce56f950a19
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49393821"
---
# <a name="deployment-checklist-for-call-admission-control-in-lync-server-2013"></a><span data-ttu-id="c7b7b-103">Liste de vérification du déploiement pour le contrôle d’admission des appels dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c7b7b-103">Deployment checklist for call admission control in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c7b7b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c7b7b-104">

<span> </span></span></span>

<span data-ttu-id="c7b7b-105">_**Dernière modification de la rubrique :** 2012-10-08_</span><span class="sxs-lookup"><span data-stu-id="c7b7b-105">_**Topic Last Modified:** 2012-10-08_</span></span>

<span data-ttu-id="c7b7b-106">Pour planifier efficacement le contrôle d’admission des appels, vous devez tenir compte des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="c7b7b-106">To plan effectively for call admission control (CAC), you need to consider the following:</span></span>

  - <span data-ttu-id="c7b7b-107">Conditions préalables pour le déploiement de CAC.</span><span class="sxs-lookup"><span data-stu-id="c7b7b-107">Prerequisites for deploying CAC.</span></span>

  - <span data-ttu-id="c7b7b-108">Informations requises pour les décisions CAC et de configuration que vous devez effectuer avant le déploiement.</span><span class="sxs-lookup"><span data-stu-id="c7b7b-108">Information required for CAC and configuration decisions that you must make in advance of deployment.</span></span>

<div>

## <a name="deployment-prerequisites-for-call-admission-control"></a><span data-ttu-id="c7b7b-109">Prérequis de déploiement pour le contrôle d’admission des appels</span><span class="sxs-lookup"><span data-stu-id="c7b7b-109">Deployment Prerequisites for Call Admission Control</span></span>

<span data-ttu-id="c7b7b-110">Avant de déployer le contrôle d’admission des appels, vous devez déjà avoir déployé vos serveurs internes Lync Server 2013, y compris un pool frontal ou un serveur Standard Edition Server.</span><span class="sxs-lookup"><span data-stu-id="c7b7b-110">Before you deploy call admission control, you must already have deployed your Lync Server 2013 internal servers, including either a Front End pool or a Standard Edition server.</span></span>

</div>

<div>

## <a name="information-requirements-for-call-admission-control"></a><span data-ttu-id="c7b7b-111">Exigences en matière de contrôle d’admission des appels</span><span class="sxs-lookup"><span data-stu-id="c7b7b-111">Information Requirements for Call Admission Control</span></span>

<span data-ttu-id="c7b7b-112">Le tableau suivant récapitule les informations requises pour le déploiement du contrôle d’admission des appels.</span><span class="sxs-lookup"><span data-stu-id="c7b7b-112">The following table summarizes the required information for deploying call admission control.</span></span>

### <a name="information-requirements-for-call-admission-control-deployment"></a><span data-ttu-id="c7b7b-113">Exigences relatives aux informations pour le déploiement de contrôles d’admission des appels</span><span class="sxs-lookup"><span data-stu-id="c7b7b-113">Information Requirements for Call Admission Control Deployment</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c7b7b-114">Information</span><span class="sxs-lookup"><span data-stu-id="c7b7b-114">Information</span></span></th>
<th><span data-ttu-id="c7b7b-115">Résumé des informations requises</span><span class="sxs-lookup"><span data-stu-id="c7b7b-115">Summary of Information Required</span></span></th>
<th><span data-ttu-id="c7b7b-116">Documentation</span><span class="sxs-lookup"><span data-stu-id="c7b7b-116">Documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c7b7b-117">Fonctionnalités du serveur Lync requises par votre organisation</span><span class="sxs-lookup"><span data-stu-id="c7b7b-117">Lync Server capabilities required by your organization</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="c7b7b-118">Fonctionnalités devant être prises en charge par votre organisation</span><span class="sxs-lookup"><span data-stu-id="c7b7b-118">Capabilities to be supported by your organization</span></span></p></li>
<li><p><span data-ttu-id="c7b7b-119">Fonctionnalités à activer pour les utilisateurs individuels</span><span class="sxs-lookup"><span data-stu-id="c7b7b-119">Capabilities to be enabled for individual users</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="c7b7b-120"><a href="lync-server-2013-defining-your-requirements-for-call-admission-control.md">Définition de la configuration requise pour le contrôle d’admission des appels dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="c7b7b-120"><a href="lync-server-2013-defining-your-requirements-for-call-admission-control.md">Defining your requirements for call admission control in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7b7b-121">Topologies et composants à déployer</span><span class="sxs-lookup"><span data-stu-id="c7b7b-121">Topologies and components to be deployed</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="c7b7b-122">Les composants liés au CAC sont automatiquement installés dans le cadre de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c7b7b-122">CAC related components are automatically installed as part of Lync Server 2013</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="c7b7b-123"><a href="lync-server-2013-defining-your-requirements-for-call-admission-control.md">Définition de la configuration requise pour le contrôle d’admission des appels dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="c7b7b-123"><a href="lync-server-2013-defining-your-requirements-for-call-admission-control.md">Defining your requirements for call admission control in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7b7b-124">Configuration système requise</span><span class="sxs-lookup"><span data-stu-id="c7b7b-124">System requirements</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="c7b7b-125">Configuration matérielle minimale requise</span><span class="sxs-lookup"><span data-stu-id="c7b7b-125">Hardware requirements</span></span></p></li>
<li><p><span data-ttu-id="c7b7b-126">Configuration logicielle requise</span><span class="sxs-lookup"><span data-stu-id="c7b7b-126">Software requirements</span></span></p></li>
<li><p><span data-ttu-id="c7b7b-127">Exigences en matière de colocalisation</span><span class="sxs-lookup"><span data-stu-id="c7b7b-127">Collocation requirements</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="c7b7b-128"><a href="lync-server-2013-determining-your-system-requirements.md">Détermination de la configuration système requise pour Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="c7b7b-128"><a href="lync-server-2013-determining-your-system-requirements.md">Determining your system requirements for Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7b7b-129">Conditions d’infrastructure requises</span><span class="sxs-lookup"><span data-stu-id="c7b7b-129">Infrastructure requirements</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="c7b7b-130">Aucun besoin d’infrastructure spécifique n’est nécessaire pour le CAC</span><span class="sxs-lookup"><span data-stu-id="c7b7b-130">No specific infrastructure requirements are necessary for CAC</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="c7b7b-131"><a href="lync-server-2013-infrastructure-requirements-for-call-admission-control.md">Configuration requise pour l’infrastructure pour le contrôle d’admission des appels dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="c7b7b-131"><a href="lync-server-2013-infrastructure-requirements-for-call-admission-control.md">Infrastructure requirements for call admission control in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7b7b-132">Exigences relatives à l’interface réseau</span><span class="sxs-lookup"><span data-stu-id="c7b7b-132">Network interface requirements</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="c7b7b-133">Informations d’interface interne et externe</span><span class="sxs-lookup"><span data-stu-id="c7b7b-133">Internal and external interface information</span></span></p></li>
<li><p><span data-ttu-id="c7b7b-134">Informations de routage (y compris les informations sur le blog NextHop à partir du <a href="https://go.microsoft.com/fwlink/p/?linkid=203149">https://go.microsoft.com/fwlink/p/?LinkId=203149</a> canal de réponse client de l’équipe Microsoft Lync Server)</span><span class="sxs-lookup"><span data-stu-id="c7b7b-134">Routing information (including information on the NextHop blog at <a href="https://go.microsoft.com/fwlink/p/?linkid=203149">https://go.microsoft.com/fwlink/p/?LinkId=203149</a>, Microsoft Lync Server team’s customer response channel)</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="c7b7b-135"><a href="lync-server-2013-deploying-external-user-access.md">Déploiement de l’accès des utilisateurs externes dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="c7b7b-135"><a href="lync-server-2013-deploying-external-user-access.md">Deploying external user access in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7b7b-136">Stratégie de déploiement</span><span class="sxs-lookup"><span data-stu-id="c7b7b-136">Deployment strategy</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="c7b7b-137">Séquence de déploiement</span><span class="sxs-lookup"><span data-stu-id="c7b7b-137">Deployment sequence</span></span></p></li>
<li><p><span data-ttu-id="c7b7b-138">Groupe de travail ou domaine</span><span class="sxs-lookup"><span data-stu-id="c7b7b-138">Workgroup or domain</span></span></p></li>
<li><p><span data-ttu-id="c7b7b-139">Sécurité</span><span class="sxs-lookup"><span data-stu-id="c7b7b-139">Security</span></span></p></li>
<li><p><span data-ttu-id="c7b7b-140">Surveillance et audit</span><span class="sxs-lookup"><span data-stu-id="c7b7b-140">Monitoring and auditing</span></span></p></li>
<li><p><span data-ttu-id="c7b7b-141">Considérations en matière de matériel</span><span class="sxs-lookup"><span data-stu-id="c7b7b-141">Hardware considerations</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="c7b7b-142"><a href="lync-server-2013-best-practices-for-call-admission-control.md">Meilleures pratiques liées au contrôle d’admission des appels dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="c7b7b-142"><a href="lync-server-2013-best-practices-for-call-admission-control.md">Best practices for call admission control in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7b7b-143">Processus de déploiement</span><span class="sxs-lookup"><span data-stu-id="c7b7b-143">Deployment process</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="c7b7b-144">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="c7b7b-144">Prerequisites</span></span></p></li>
<li><p><span data-ttu-id="c7b7b-145">Exigences relatives aux informations</span><span class="sxs-lookup"><span data-stu-id="c7b7b-145">Information requirements</span></span></p></li>
<li><p><span data-ttu-id="c7b7b-146">Processus et procédures</span><span class="sxs-lookup"><span data-stu-id="c7b7b-146">Process and procedures</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="c7b7b-147"><a href="lync-server-2013-configure-call-admission-control.md">Configurer le contrôle d’admission des appels dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="c7b7b-147"><a href="lync-server-2013-configure-call-admission-control.md">Configure call admission control in Lync Server 2013</a></span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="c7b7b-148">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c7b7b-148">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

