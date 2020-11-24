---
title: 'Lync Server 2013 : Configuration technique requise pour le parcage d’appel'
description: 'Lync Server 2013 : exigences techniques pour le parc d’appels.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Technical requirements for Call Park
ms:assetid: 38bcf302-2b72-4492-9266-f6dc31b566e1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204818(v=OCS.15)
ms:contentKeyID: 48183897
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6ddc17b40f78c42c090d1a87b4580ebdad0a07f6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394681"
---
# <a name="technical-requirements-for-call-park-in-lync-server-2013"></a><span data-ttu-id="24257-103">Configuration technique requise pour le parcage d’appel dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="24257-103">Technical requirements for Call Park in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="24257-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="24257-104">

<span> </span></span></span>

<span data-ttu-id="24257-105">_**Dernière modification de la rubrique :** 2013-11-07_</span><span class="sxs-lookup"><span data-stu-id="24257-105">_**Topic Last Modified:** 2013-11-07_</span></span>

<span data-ttu-id="24257-106">Cette section décrit les exigences techniques suivantes en matière de stationnement d’appel :</span><span class="sxs-lookup"><span data-stu-id="24257-106">This section describes the following technical requirements for Call Park:</span></span>

  - <span data-ttu-id="24257-107">Configuration matérielle minimale requise</span><span class="sxs-lookup"><span data-stu-id="24257-107">Hardware requirements</span></span>

  - <span data-ttu-id="24257-108">Configuration logicielle requise</span><span class="sxs-lookup"><span data-stu-id="24257-108">Software requirements</span></span>

  - <span data-ttu-id="24257-109">Conditions requises en matière de ports</span><span class="sxs-lookup"><span data-stu-id="24257-109">Port requirements</span></span>

  - <span data-ttu-id="24257-110">Configuration requise pour le fichier audio</span><span class="sxs-lookup"><span data-stu-id="24257-110">Audio file requirements</span></span>

<div>

## <a name="hardware-requirements"></a><span data-ttu-id="24257-111">Configuration matérielle requise</span><span class="sxs-lookup"><span data-stu-id="24257-111">Hardware Requirements</span></span>

<span data-ttu-id="24257-112">La configuration matérielle requise pour l’application de parc d’appels est identique à celle des serveurs frontaux.</span><span class="sxs-lookup"><span data-stu-id="24257-112">The Call Park application has the same hardware requirements as Front End Servers.</span></span> <span data-ttu-id="24257-113">Pour plus d’informations sur la configuration matérielle requise, voir [plates-formes matérielles pour Lync Server 2013](lync-server-2013-server-hardware-platforms.md) dans la documentation relative à la prise en charge.</span><span class="sxs-lookup"><span data-stu-id="24257-113">For details about hardware requirements, see [Server hardware platforms for Lync Server 2013](lync-server-2013-server-hardware-platforms.md) in the Supportability documentation.</span></span>

</div>

<div>

## <a name="software-requirements"></a><span data-ttu-id="24257-114">Configuration logicielle requise</span><span class="sxs-lookup"><span data-stu-id="24257-114">Software Requirements</span></span>

<span data-ttu-id="24257-115">La configuration requise pour les systèmes d’exploitation et les logiciels requis par le biais de l’application de parc d’appels est la même que celle des serveurs frontaux.</span><span class="sxs-lookup"><span data-stu-id="24257-115">The Call Park application has the same operating system requirements and software prerequisites as Front End Servers.</span></span> <span data-ttu-id="24257-116">Pour plus d’informations sur la configuration logicielle requise, voir [prise en charge du système d’exploitation serveur et outils dans Lync Server 2013](lync-server-2013-server-and-tools-operating-system-support.md) dans la documentation relative à la prise en charge.</span><span class="sxs-lookup"><span data-stu-id="24257-116">For details about software requirements, see [Server and tools operating system support in Lync Server 2013](lync-server-2013-server-and-tools-operating-system-support.md) in the Supportability documentation.</span></span>

<span data-ttu-id="24257-117">Tous les serveurs frontaux et les serveurs Standard Edition Server pour lesquels l’application de parc d’appels est déployée doivent avoir installé le runtime du format Windows Media pour les serveurs exécutant Windows Server 2008 R2 ou Microsoft Media Foundation pour les serveurs exécutant Windows Server 2012 ou Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="24257-117">All Front End Servers and Standard Edition servers where the Call Park application is deployed must have the Windows Media Format Runtime installed for servers running Windows Server 2008 R2, or Microsoft Media Foundation for servers running Windows Server 2012 or Windows Server 2012 R2.</span></span> <span data-ttu-id="24257-118">Pour Windows Server 2008 R2, le runtime Windows Media Format Runtime est installé dans le cadre de l’expérience de bureau Windows.</span><span class="sxs-lookup"><span data-stu-id="24257-118">For Windows Server 2008 R2, Windows Media Format Runtime is installed as part of Windows Desktop Experience.</span></span> <span data-ttu-id="24257-119">Windows Media Format Runtime ou Microsoft Media Foundation est requis pour les fichiers Windows Media audio (. WMA) pour lesquels le parc est lu pour la musique en attente.</span><span class="sxs-lookup"><span data-stu-id="24257-119">Windows Media Format Runtime or Microsoft Media Foundation is required for Windows Media Audio (.wma) files that Call Park plays for music on hold.</span></span>

</div>

<div>

## <a name="port-requirements"></a><span data-ttu-id="24257-120">Configuration requise pour les ports</span><span class="sxs-lookup"><span data-stu-id="24257-120">Port Requirements</span></span>

<span data-ttu-id="24257-121">L’application de parc d’appels utilise le port suivant :</span><span class="sxs-lookup"><span data-stu-id="24257-121">The Call Park application uses the following port:</span></span>

  - <span data-ttu-id="24257-122">**Port 5075** : utilisé pour les demandes d’écoute SIP.</span><span class="sxs-lookup"><span data-stu-id="24257-122">**Port 5075**   Used for SIP listening requests.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="24257-123">Ce port est un paramètre par défaut que vous pouvez modifier à l’aide de l’applet de commande <STRONG>Set-CsApplicationServer</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="24257-123">This port is a default setting that you can change by using the <STRONG>Set-CsApplicationServer</STRONG> cmdlet.</span></span> <span data-ttu-id="24257-124">Pour plus d’informations sur cette applet de connexion, consultez la documentation Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="24257-124">For details about this cmdlet, see the Lync Server Management Shell documentation.</span></span>



</div>

</div>

<div>

## <a name="audio-file-requirements"></a><span data-ttu-id="24257-125">Conditions requises pour les fichiers audio</span><span class="sxs-lookup"><span data-stu-id="24257-125">Audio File Requirements</span></span>

<span data-ttu-id="24257-126">L’application de parc d’appels prend uniquement en charge les fichiers Windows Media audio (. WMA) pour la musique en attente.</span><span class="sxs-lookup"><span data-stu-id="24257-126">The Call Park application supports only Windows Media Audio (.wma) files for music on hold.</span></span> <span data-ttu-id="24257-127">Pour personnaliser les fichiers d’attente musicale, vous pouvez utiliser Microsoft Expression Encoder 4.</span><span class="sxs-lookup"><span data-stu-id="24257-127">You can use the Microsoft Expression Encoder 4 to customize files for music on hold.</span></span> <span data-ttu-id="24257-128">Pour télécharger Expression Encoder 4, voir « Expression Encoder 4 » à l’adresse [https://go.microsoft.com/fwlink/p/?linkId=202843](https://go.microsoft.com/fwlink/p/?linkid=202843) .</span><span class="sxs-lookup"><span data-stu-id="24257-128">To download Expression Encoder 4, see "Expression Encoder 4" at [https://go.microsoft.com/fwlink/p/?linkId=202843](https://go.microsoft.com/fwlink/p/?linkid=202843).</span></span> <span data-ttu-id="24257-129">Utilisez l’outil pour convertir le fichier au format .wma.</span><span class="sxs-lookup"><span data-stu-id="24257-129">Use the tool to convert the file to a .wma format.</span></span> <span data-ttu-id="24257-130">Le format recommandé pour les fichiers de la musique de parc d’appels est l’audio multimédia 9, 44 kHz, 16 bits, mono, CBR, 32 kbps.</span><span class="sxs-lookup"><span data-stu-id="24257-130">The recommended format for Call Park music-on-hold files is Media Audio 9, 44 kHz, 16 bits, Mono, CBR, 32 kbps.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="24257-131">Le fichier converti est lu sur le téléphone à seulement 16 kHz, même s’il a été enregistré à 44 kHz.</span><span class="sxs-lookup"><span data-stu-id="24257-131">The converted file plays over the phone only at 16 kHz, even if it was recorded at 44 kHz.</span></span>



<span data-ttu-id="24257-132"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="24257-132"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

