---
title: 'Lync Server 2013 : processus de déploiement de l’application annonce'
description: 'Lync Server 2013 : processus de déploiement de l’application d’annonce.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment process for the Announcement application
ms:assetid: 72c66249-c4ce-48ce-b1b9-90ebf77d7805
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398545(v=OCS.15)
ms:contentKeyID: 48184500
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 559977c32f63fae312164b5b0c36698fa13afb09
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429642"
---
# <a name="deployment-process-for-the-announcement-application-in-lync-server-2013"></a><span data-ttu-id="8429b-103">Processus de déploiement de l’application d’annonce dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8429b-103">Deployment process for the Announcement application in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8429b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8429b-104">

<span> </span></span></span>

<span data-ttu-id="8429b-105">_**Dernière modification de la rubrique :** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="8429b-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="8429b-106">Cette section fournit une vue d’ensemble des étapes de déploiement de l’application d’annonce.</span><span class="sxs-lookup"><span data-stu-id="8429b-106">This section provides an overview of the steps involved in deploying the Announcement application.</span></span> <span data-ttu-id="8429b-107">Vous devez déployer Enterprise Voice avant de configurer les annonces.</span><span class="sxs-lookup"><span data-stu-id="8429b-107">You must deploy Enterprise Voice before you configure announcements.</span></span> <span data-ttu-id="8429b-108">Les composants requis par l’application d’annonce sont installés et activés lorsque vous déployez Enterprise Voice.</span><span class="sxs-lookup"><span data-stu-id="8429b-108">The components required by the Announcement application are installed and enabled when you deploy Enterprise Voice.</span></span>

### <a name="announcement-deployment-process"></a><span data-ttu-id="8429b-109">Procédure de déploiement des annonces</span><span class="sxs-lookup"><span data-stu-id="8429b-109">Announcement Deployment Process</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8429b-110">Phase</span><span class="sxs-lookup"><span data-stu-id="8429b-110">Phase</span></span></th>
<th><span data-ttu-id="8429b-111">Étapes</span><span class="sxs-lookup"><span data-stu-id="8429b-111">Steps</span></span></th>
<th><span data-ttu-id="8429b-112">Rôles</span><span class="sxs-lookup"><span data-stu-id="8429b-112">Roles</span></span></th>
<th><span data-ttu-id="8429b-113">Documentation de déploiement</span><span class="sxs-lookup"><span data-stu-id="8429b-113">Deployment documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8429b-114">Configurer les paramètres d’annonce</span><span class="sxs-lookup"><span data-stu-id="8429b-114">Configure Announcement settings</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="8429b-115">Créez l’annonce en enregistrant et en téléchargeant des fichiers audio ou en utilisant la synthèse vocale (TTS).</span><span class="sxs-lookup"><span data-stu-id="8429b-115">Create the announcement by recording and uploading audio files or by using text-to-speech (TTS).</span></span></p></li>
<li><p><span data-ttu-id="8429b-116">Configurez les plages de numéros non attribués dans la table des numéros non attribués et associez-les à l’annonce appropriée.</span><span class="sxs-lookup"><span data-stu-id="8429b-116">Configure the unassigned number ranges in the unassigned number table and associate them with the appropriate announcement.</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="8429b-117">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="8429b-117">RTCUniversalServerAdmins</span></span></p>
<p><span data-ttu-id="8429b-118">CsVoiceAdministrator</span><span class="sxs-lookup"><span data-stu-id="8429b-118">CsVoiceAdministrator</span></span></p>
<p><span data-ttu-id="8429b-119">CsServerAdministrator</span><span class="sxs-lookup"><span data-stu-id="8429b-119">CsServerAdministrator</span></span></p>
<p><span data-ttu-id="8429b-120">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="8429b-120">CsAdministrator</span></span></p>
<p><span data-ttu-id="8429b-121">CsViewOnlyAdministrator</span><span class="sxs-lookup"><span data-stu-id="8429b-121">CsViewOnlyAdministrator</span></span></p></td>
<td><p><span data-ttu-id="8429b-122"><a href="lync-server-2013-create-an-announcement.md">Créer une annonce dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="8429b-122"><a href="lync-server-2013-create-an-announcement.md">Create an announcement in Lync Server 2013</a></span></span></p>
<p><span data-ttu-id="8429b-123"><a href="lync-server-2013-configure-the-unassigned-number-table.md">Configuration de la table des numéros non attribués dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="8429b-123"><a href="lync-server-2013-configure-the-unassigned-number-table.md">Configure the unassigned number table in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8429b-124">Vérifier le déploiement de votre annonce</span><span class="sxs-lookup"><span data-stu-id="8429b-124">Verify your Announcement deployment</span></span></p></td>
<td><p><span data-ttu-id="8429b-125">Testez vos annonces en les écoutant afin de vérifier que votre configuration fonctionne comme prévu.</span><span class="sxs-lookup"><span data-stu-id="8429b-125">Test by listening to announcements to verify that your configuration works as expected.</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="8429b-126"><a href="lync-server-2013-optional-verify-announcement-deployment.md">Facultatif Vérifier le déploiement d’annonce dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="8429b-126"><a href="lync-server-2013-optional-verify-announcement-deployment.md">(Optional) Verify Announcement deployment in Lync Server 2013</a></span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="8429b-127">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8429b-127">


</div>

<span> </span>

</div>

</div>

</span></span></div>

