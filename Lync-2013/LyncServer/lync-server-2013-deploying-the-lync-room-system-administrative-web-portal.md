---
title: 'Lync Server 2013 : déploiement du portail Web d’administration du système de salle Lync'
description: 'Lync Server 2013 : déploiement du portail Web d’administration du système de salle Lync.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying the Lync Room System Administrative Web Portal
ms:assetid: ecba5b36-632e-40b9-9c2e-ab825baf7a46
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn436324(v=OCS.15)
ms:contentKeyID: 56737621
ms.date: 05/04/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e67723b3ddf3f452c53411e560420bb0b043128e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49393992"
---
# <a name="deploying-the-lync-room-system-administrative-web-portal-in-lync-server-2013"></a><span data-ttu-id="cd128-103">Deploying the Lync Room System Administrative Web Portal in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cd128-103">Deploying the Lync Room System Administrative Web Portal in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cd128-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cd128-104">

<span> </span></span></span>

<span data-ttu-id="cd128-105">_**Dernière modification de la rubrique :** 2015-05-04_</span><span class="sxs-lookup"><span data-stu-id="cd128-105">_**Topic Last Modified:** 2015-05-04_</span></span>

<span data-ttu-id="cd128-106">Le portail Web d’administration Microsoft Lync Server 2013 Lync salle (LRS) est un portail Web que les organisations peuvent utiliser pour gérer leurs salles de conférence de systèmes de salle Lync.</span><span class="sxs-lookup"><span data-stu-id="cd128-106">The Microsoft Lync Server 2013 Lync Room System (LRS) Administrative Web Portal is a web portal that organizations can use to maintain their Lync Room System conference rooms.</span></span> <span data-ttu-id="cd128-107">Les administrateurs peuvent utiliser le portail Web d’administration LRS pour surveiller l’intégrité de LRS, par exemple en surveillant des périphériques audio/vidéo qui sont connectés.</span><span class="sxs-lookup"><span data-stu-id="cd128-107">Administrators can use the LRS Administrative Web Portal to monitor LRS health, for example by monitoring audio/video devices that are connected.</span></span> <span data-ttu-id="cd128-108">Ils peuvent également collecter à distance des informations de diagnostic pour surveiller l’intégrité des salles de conférence.</span><span class="sxs-lookup"><span data-stu-id="cd128-108">With this portal, administrators can remotely collect diagnostic information to monitor conference room health.</span></span>

<span data-ttu-id="cd128-109">Le portail Web d’administration LRS est déployé sur chaque serveur frontal Lync.</span><span class="sxs-lookup"><span data-stu-id="cd128-109">The LRS Administrative Web Portal is deployed on every Lync Front End Server.</span></span> <span data-ttu-id="cd128-110">Ce guide fournit aux administrateurs des instructions sur l’installation et la configuration du portail Web d’administration LRS.</span><span class="sxs-lookup"><span data-stu-id="cd128-110">This guide provides instructions for administrators about how to install and configure the LRS Administrative Web Portal.</span></span> <span data-ttu-id="cd128-111">Il est destiné aux administrateurs ayant connaissance de l’administration de Lync Server et disposant de droits d’administrateur pour modifier la topologie du serveur Lync.</span><span class="sxs-lookup"><span data-stu-id="cd128-111">It is intended for administrators who have knowledge of Lync Server administration, and who have administrator user rights to modify the Lync Server topology.</span></span>

<span data-ttu-id="cd128-112">Après le déploiement d’LRS portail Web d’administration sur le serveur, les administrateurs peuvent vérifier l’état de toutes les salles LRS en se connectant au site à partir de leur ordinateur ou de leur ordinateur portable.</span><span class="sxs-lookup"><span data-stu-id="cd128-112">After LRS Administrative Web Portal is deployed on the server, administrators can check the status of all LRS rooms by logging on to the site from their own computers or laptops.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="cd128-113">Lorsque vous installez le portail Web d’administration LRS dans un déploiement Microsoft Lync Server 2013, vous devez utiliser le <A href="https://go.microsoft.com/fwlink/p/?linkid=544806">portail Web d’administration de Microsoft Lync salle pour Lync server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="cd128-113">When you install the LRS Administrative Web Portal in a Microsoft Lync Server 2013 deployment, you should use the <A href="https://go.microsoft.com/fwlink/p/?linkid=544806">Microsoft Lync Room System Administrative Web Portal for Lync Server 2013</A>.</span></span><BR><span data-ttu-id="cd128-114">Une nouvelle version du portail Web d’administration LRS est disponible pour Skype entreprise Server 2015, mais vous ne devez pas installer cette version sauf si vous avez déployé Skype entreprise Server 2015.</span><span class="sxs-lookup"><span data-stu-id="cd128-114">A new version of the LRS Administrative Web Portal is available for Skype for Business Server 2015, but you should not install that version unless you have deployed Skype for Business Server 2015.</span></span> <span data-ttu-id="cd128-115">Téléchargez le <A href="https://go.microsoft.com/fwlink/?linkid=544807">portail Web d’administration du système de salle Microsoft Lync pour Skype entreprise Server 2015</A>.</span><span class="sxs-lookup"><span data-stu-id="cd128-115">Download the <A href="https://go.microsoft.com/fwlink/?linkid=544807">Microsoft Lync Room System Administrative Web Portal for Skype for Business Server 2015</A>.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="cd128-116">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="cd128-116">In This Section</span></span>

[<span data-ttu-id="cd128-117">Configuring your Lync Server 2013 environment for the Lync Room System Administrative Web Portal</span><span class="sxs-lookup"><span data-stu-id="cd128-117">Configuring your Lync Server 2013 environment for the Lync Room System Administrative Web Portal</span></span>](lync-server-2013-configuring-your-environment-for-the-lync-room-system-administrative-web-portal.md)

[<span data-ttu-id="cd128-118">Installing the Lync Room System Administrative Web Portal in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cd128-118">Installing the Lync Room System Administrative Web Portal in Lync Server 2013</span></span>](lync-server-2013-installing-the-lync-room-system-administrative-web-portal.md)

[<span data-ttu-id="cd128-119">Using the Lync Room System Administrative Web Portal in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cd128-119">Using the Lync Room System Administrative Web Portal in Lync Server 2013</span></span>](lync-server-2013-using-the-lync-room-system-administrative-web-portal.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="cd128-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cd128-120">See Also</span></span>


[<span data-ttu-id="cd128-121">Déploiement d’une conférence dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cd128-121">Deploying conferencing in Lync Server 2013</span></span>](lync-server-2013-deploying-conferencing.md)  
  

<span data-ttu-id="cd128-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cd128-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

