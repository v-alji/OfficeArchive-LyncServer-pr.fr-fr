---
title: 'Lync Server 2013 : Configuration technique requise pour l’application Annonces'
description: 'Lync Server 2013 : exigences techniques pour l’application d’annonce.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Technical requirements for the Announcement application
ms:assetid: fbd8c204-3765-4b22-a0c9-a781b5126366
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205413(v=OCS.15)
ms:contentKeyID: 48185944
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: adc5019408b79301bbcda3993ceb7d96ee4d9b7d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444307"
---
# <a name="technical-requirements-for-the-announcement-application-in-lync-server-2013"></a><span data-ttu-id="f0c84-103">Configuration technique requise pour l’application Annonces dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f0c84-103">Technical requirements for the Announcement application in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f0c84-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f0c84-104">

<span> </span></span></span>

<span data-ttu-id="f0c84-105">_**Dernière modification de la rubrique :** 2013-11-07_</span><span class="sxs-lookup"><span data-stu-id="f0c84-105">_**Topic Last Modified:** 2013-11-07_</span></span>

<span data-ttu-id="f0c84-106">Cette section décrit les exigences techniques suivantes pour l’application d’annonce :</span><span class="sxs-lookup"><span data-stu-id="f0c84-106">This section describes the following technical requirements for the Announcement application:</span></span>

  - <span data-ttu-id="f0c84-107">Configuration matérielle minimale requise</span><span class="sxs-lookup"><span data-stu-id="f0c84-107">Hardware requirements</span></span>

  - <span data-ttu-id="f0c84-108">Configuration logicielle requise</span><span class="sxs-lookup"><span data-stu-id="f0c84-108">Software requirements</span></span>

  - <span data-ttu-id="f0c84-109">Conditions requises en matière de ports</span><span class="sxs-lookup"><span data-stu-id="f0c84-109">Port requirements</span></span>

  - <span data-ttu-id="f0c84-110">Configuration requise pour le fichier audio</span><span class="sxs-lookup"><span data-stu-id="f0c84-110">Audio file requirements</span></span>

<div>

## <a name="hardware-requirements"></a><span data-ttu-id="f0c84-111">Configuration matérielle requise</span><span class="sxs-lookup"><span data-stu-id="f0c84-111">Hardware Requirements</span></span>

<span data-ttu-id="f0c84-112">La configuration matérielle requise pour l’application d’annonce est identique à celle des serveurs frontaux.</span><span class="sxs-lookup"><span data-stu-id="f0c84-112">The Announcement application has the same hardware requirements as Front End Servers.</span></span> <span data-ttu-id="f0c84-113">Pour plus d’informations sur la configuration matérielle requise, voir [plates-formes matérielles pour Lync Server 2013](lync-server-2013-server-hardware-platforms.md) dans la documentation relative à la prise en charge.</span><span class="sxs-lookup"><span data-stu-id="f0c84-113">For details about hardware requirements, see [Server hardware platforms for Lync Server 2013](lync-server-2013-server-hardware-platforms.md) in the Supportability documentation.</span></span>

</div>

<div>

## <a name="software-requirements"></a><span data-ttu-id="f0c84-114">Configuration logicielle requise</span><span class="sxs-lookup"><span data-stu-id="f0c84-114">Software Requirements</span></span>

<span data-ttu-id="f0c84-115">La configuration requise pour le système d’exploitation et les composants logiciels requis par le biais de l’application d’annonce sont les mêmes.</span><span class="sxs-lookup"><span data-stu-id="f0c84-115">The Announcement application has the same operating system requirements and software prerequisites as Front End Servers.</span></span> <span data-ttu-id="f0c84-116">Pour plus d’informations sur la configuration logicielle requise, voir [prise en charge du système d’exploitation serveur et outils dans Lync Server 2013](lync-server-2013-server-and-tools-operating-system-support.md) dans la documentation relative à la prise en charge.</span><span class="sxs-lookup"><span data-stu-id="f0c84-116">For details about software requirements, see [Server and tools operating system support in Lync Server 2013](lync-server-2013-server-and-tools-operating-system-support.md) in the Supportability documentation.</span></span>

<span data-ttu-id="f0c84-117">Tous les serveurs front-end ou les serveurs Standard Edition qui exécutent l’application d’annonce doivent avoir installé le runtime du format Windows Media pour les serveurs exécutant Windows Server 2008 R2 ou Microsoft Media Foundation pour les serveurs exécutant Windows Server 2012 ou Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="f0c84-117">All Front End Servers or Standard Edition servers that run the Announcement application must have the Windows Media Format Runtime installed for servers running Windows Server 2008 R2, or Microsoft Media Foundation for servers running Windows Server 2012 or Windows Server 2012 R2.</span></span> <span data-ttu-id="f0c84-118">Pour Windows Server 2008 R2, le runtime Windows Media Format Runtime est installé dans le cadre de l’expérience de bureau Windows.</span><span class="sxs-lookup"><span data-stu-id="f0c84-118">For Windows Server 2008 R2, the Windows Media Format Runtime is installed as part of Windows Desktop Experience.</span></span> <span data-ttu-id="f0c84-119">Windows Media Format Runtime ou Microsoft Media Foundation est requis pour les fichiers Windows Media audio (. WMA) que l’application d’annonce exécute pour les annonces et la musique.</span><span class="sxs-lookup"><span data-stu-id="f0c84-119">Windows Media Format Runtime or Microsoft Media Foundation is required for Windows Media Audio (.wma) files that the Announcement application plays for announcements and music.</span></span>

</div>

<div>

## <a name="port-requirements"></a><span data-ttu-id="f0c84-120">Configuration requise pour les ports</span><span class="sxs-lookup"><span data-stu-id="f0c84-120">Port Requirements</span></span>

<span data-ttu-id="f0c84-121">L’application d’annonce utilise le port suivant :</span><span class="sxs-lookup"><span data-stu-id="f0c84-121">The Announcement application uses the following port:</span></span>

  - <span data-ttu-id="f0c84-122">**Port 5071**   Utilisé pour les requêtes d’écoute SIP</span><span class="sxs-lookup"><span data-stu-id="f0c84-122">**Port 5071**   Used for SIP listening requests</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="f0c84-123">Ce port est le paramètre par défaut, que vous pouvez modifier en utilisant l’applet de commande <STRONG>Set-CsApplicationServer</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="f0c84-123">This port is the default setting, which you can change by using the <STRONG>Set-CsApplicationServer</STRONG> cmdlet.</span></span> <span data-ttu-id="f0c84-124">Pour plus d’informations sur cette applet de connexion, consultez la documentation Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="f0c84-124">For details about this cmdlet, see the Lync Server Management Shell documentation.</span></span>



</div>

</div>

<div>

## <a name="audio-file-requirements"></a><span data-ttu-id="f0c84-125">Conditions requises pour les fichiers audio</span><span class="sxs-lookup"><span data-stu-id="f0c84-125">Audio File Requirements</span></span>

<span data-ttu-id="f0c84-126">L’application d’annonce prend en charge le format de fichier Wave (. wav) et le format de fichier Windows Media audio (. WMA) pour la musique et les annonces.</span><span class="sxs-lookup"><span data-stu-id="f0c84-126">The Announcement application supports Wave (.wav) file format and Windows Media audio (.wma) file format for music and announcements.</span></span> <span data-ttu-id="f0c84-127">La configuration requise pour le fichier audio pour l’application d’annonce est identique à celle de l’application Response Group.</span><span class="sxs-lookup"><span data-stu-id="f0c84-127">Audio file requirements for the Announcement application are the same as for the Response Group application.</span></span> <span data-ttu-id="f0c84-128">Pour plus d’informations, voir [configuration technique requise pour Response Group dans Lync Server 2013](lync-server-2013-technical-requirements-for-response-group.md).</span><span class="sxs-lookup"><span data-stu-id="f0c84-128">For details, see [Technical requirements for Response Group in Lync Server 2013](lync-server-2013-technical-requirements-for-response-group.md).</span></span>

<span data-ttu-id="f0c84-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f0c84-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

