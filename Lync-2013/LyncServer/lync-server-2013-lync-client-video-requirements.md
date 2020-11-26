---
title: 'Configuration requise pour le client Lync Server 2013 :'
description: 'Configuration requise pour la vidéo Lync Server 2013 : client Lync.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Lync client video requirements
ms:assetid: 8f68f4c2-3194-487c-bd2f-fbe71ba8ad70
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688132(v=OCS.15)
ms:contentKeyID: 49733731
ms.date: 01/29/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ea1d4a993650ec8102d8b66ea5aa936ad1613f20
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426437"
---
# <a name="lync-client-video-requirements-for-lync-server-2013"></a><span data-ttu-id="6ecdb-103">Configuration vidéo requise pour le client Lync pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6ecdb-103">Lync client video requirements for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6ecdb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6ecdb-104">

<span> </span></span></span>

<span data-ttu-id="6ecdb-105">_**Dernière modification de la rubrique :** 2016-01-29_</span><span class="sxs-lookup"><span data-stu-id="6ecdb-105">_**Topic Last Modified:** 2016-01-29_</span></span>

<span data-ttu-id="6ecdb-106">Cette section décrit la prise en charge de matériel vidéo pour les appels vidéo Lync 2013 et explique comment déterminer la qualité vidéo prévue pour différentes configurations d’ordinateur, de tablette et de périphérique mobile.</span><span class="sxs-lookup"><span data-stu-id="6ecdb-106">This section describes video hardware support for Lync 2013 video calls and describes how to determine the expected video quality for various computer, tablet, and mobile device configurations.</span></span>

<div>

## <a name="windows-desktop-and-tablet-video-requirements-and-capabilities"></a><span data-ttu-id="6ecdb-107">Configurations et capacités requises pour les ordinateurs de bureau et les tablettes Windows</span><span class="sxs-lookup"><span data-stu-id="6ecdb-107">Windows Desktop and Tablet Video Requirements and Capabilities</span></span>

<span data-ttu-id="6ecdb-108">Lync 2013 introduit l’accélération matérielle pour le codage et le décodage vidéo en fonction de la norme de codage vidéo de H. 264/MPEG-4 partie 10 avancée.</span><span class="sxs-lookup"><span data-stu-id="6ecdb-108">Lync 2013 introduces hardware acceleration for video encoding and decoding based on the H.264/MPEG-4 Part 10 Advanced Video Coding standard.</span></span> <span data-ttu-id="6ecdb-109">Cette fonctionnalité permet aux ordinateurs dont la vitesse d’horloge du processeur est faible d’encoder et de décoder des vidéos avec des résolutions supérieures.</span><span class="sxs-lookup"><span data-stu-id="6ecdb-109">This feature allows computers with lower CPU clock speeds to encode and decode higher resolution video.</span></span> <span data-ttu-id="6ecdb-110">La configuration requise pour le matériel vidéo dépend de la configuration de l’ordinateur et de la résolution vidéo souhaitée.</span><span class="sxs-lookup"><span data-stu-id="6ecdb-110">Video hardware requirements vary depending on the computer configuration and the video resolution wanted.</span></span>

<div>

## <a name="video-hardware-requirements"></a><span data-ttu-id="6ecdb-111">Configuration matérielle requise pour la vidéo</span><span class="sxs-lookup"><span data-stu-id="6ecdb-111">Video Hardware Requirements</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6ecdb-112">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="6ecdb-112">Feature</span></span></th>
<th><span data-ttu-id="6ecdb-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6ecdb-113">Requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6ecdb-114">Décodage matériel accéléré H.264 à l’aide de l’accélération vidéo DirectX (DXVA)</span><span class="sxs-lookup"><span data-stu-id="6ecdb-114">Hardware accelerated H.264 decoding using DirectX Video Acceleration (DXVA)</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="6ecdb-115">La carte graphique doit prendre en charge DirectX 9.0 et exposer le mode de décodage DXVA2_ModeH264_VLD_NoFGT.</span><span class="sxs-lookup"><span data-stu-id="6ecdb-115">Graphics card must support DirectX 9.0 and must expose the DXVA2_ModeH264_VLD_NoFGT decoding mode.</span></span></p></li>
<li><p><span data-ttu-id="6ecdb-116">Le pilote de carte graphique le plus récent doit être installé.</span><span class="sxs-lookup"><span data-stu-id="6ecdb-116">The latest graphics card driver must be installed.</span></span></p></li>
</ul>
<div>

> [!NOTE]  
> <span data-ttu-id="6ecdb-117">Pour plus d’informations sur les modes de décodage, voir <A href="https://go.microsoft.com/fwlink/p/?linkid=268530">https://go.microsoft.com/fwlink/p/?LinkId=268530</A> .</span><span class="sxs-lookup"><span data-stu-id="6ecdb-117">For details about decoding modes, see <A href="https://go.microsoft.com/fwlink/p/?linkid=268530">https://go.microsoft.com/fwlink/p/?LinkId=268530</A>.</span></span>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ecdb-118">Encodage matériel accéléré H.264 : chipset requis</span><span class="sxs-lookup"><span data-stu-id="6ecdb-118">Hardware accelerated H.264 encoding: Chipset Requirements</span></span></p></td>
<td><p><span data-ttu-id="6ecdb-119">Les solutions d’encodage vidéo matériel accéléré Intel suivantes sont prises en charge :</span><span class="sxs-lookup"><span data-stu-id="6ecdb-119">The following Intel hardware accelerated video encoding solutions are supported:</span></span></p>
<ul>
<li><p><span data-ttu-id="6ecdb-120">Chipsets vidéo Intel HD 2000, 2500, 3000 et 4000 (ou versions ultérieures) avec les codes vidéo intégrés.</span><span class="sxs-lookup"><span data-stu-id="6ecdb-120">Second and third generation Intel HD Graphics 2000, 2500, 3000, and 4000 chipsets (or later versions) with integrated hardware video encoders.</span></span> <span data-ttu-id="6ecdb-121">L’installation du pilote 15.28.9.2884 Intel HD Graphics ou version ultérieure contenant les éléments suivants est requise :</span><span class="sxs-lookup"><span data-stu-id="6ecdb-121">Installation of the Intel HD Graphics driver 15.28.9.2884 or the latest driver containing the following is required:</span></span></p>
<ul>
<li><p><span data-ttu-id="6ecdb-122">pilote d’affichage 9.17.10.2884 ou version ultérieure ;</span><span class="sxs-lookup"><span data-stu-id="6ecdb-122">Display driver 9.17.10.2884 or the latest driver</span></span></p></li>
<li><p><span data-ttu-id="6ecdb-123">HMFT (Hardware Media Foundation Transform) 3.12.10.31 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="6ecdb-123">Hardware media foundation transform (HMFT) version 3.12.10.31 or the latest HMFT</span></span></p></li>
</ul></li>
</ul>
<p><span data-ttu-id="6ecdb-124">Les solutions de codage vidéo accélérées sur le matériel AMD suivantes sont prises en charge (nécessite des mises à jour CU1 pour Lync Server 2013) :</span><span class="sxs-lookup"><span data-stu-id="6ecdb-124">The following AMD hardware accelerated video encoding solutions are supported (requires CU1 Updates for Lync Server 2013):</span></span></p>
<ul>
<li><p><span data-ttu-id="6ecdb-p103">AMD Video Codec Engine, disponible dans plusieurs cartes graphiques discrètes et les unités de traitement accéléré intégrées des processeurs accélérés AMD série A. Le pilote 9.12.0.0 AMD Video Codec Engine ou une version ultérieure doit être installé.</span><span class="sxs-lookup"><span data-stu-id="6ecdb-p103">AMD Video Codec Engine, which is available in several discrete graphics cards and in integrated accelerated processing units of AMD A-Series Accelerated Processors. The AMD Video Codec Engine driver 9.12.0.0 or higher must be installed.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ecdb-127">Encodage matériel accéléré H.264 : caméra requise</span><span class="sxs-lookup"><span data-stu-id="6ecdb-127">Hardware accelerated H.264 encoding: Camera Requirements</span></span></p></td>
<td><p><span data-ttu-id="6ecdb-128">Caméras vidéo USB avec encodeur matériel H.264 intégré conforme à la spécification USB Video Class (UVC) version 1.5.</span><span class="sxs-lookup"><span data-stu-id="6ecdb-128">USB video cameras with integrated H.264 hardware encoder that conforms to the USB Video Class (UVC) specification version 1.5.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="6ecdb-129">Lync 2013 prend en charge les appareils photo 1,5 UVC avec Windows 8 ou Windows 8,1, qui inclut la prise en charge de UVC 1,5.</span><span class="sxs-lookup"><span data-stu-id="6ecdb-129">Lync 2013 supports UVC 1.5 cameras with Windows 8 or Windows 8.1, which includes support for UVC 1.5.</span></span> <span data-ttu-id="6ecdb-130">Dans la mesure où Windows 7 n’inclut pas la prise en charge de UVC 1,5, Lync 2013 considère les appareils photo 1,5 UVC comme des caméras normales sans prise en charge du codage matériel.</span><span class="sxs-lookup"><span data-stu-id="6ecdb-130">Because Windows 7 does not include support for UVC 1.5, Lync 2013 treats UVC 1.5 cameras as regular cameras with no hardware encoding support.</span></span>


</div></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="determining-h264-video-encoding-and-decoding-capabilities"></a><span data-ttu-id="6ecdb-131">Détermination des capacités de codage et de décodage vidéo de H. 264</span><span class="sxs-lookup"><span data-stu-id="6ecdb-131">Determining H.264 Video Encoding and Decoding Capabilities</span></span>

<span data-ttu-id="6ecdb-132">En règle générale, quatre facteurs principaux déterminent les capacités d’encodage et de décodage maximales d’une configuration donnée :</span><span class="sxs-lookup"><span data-stu-id="6ecdb-132">Generally, there are four major factors that determine the maximum encoding and decoding capability of a particular computer configuration:</span></span>

  - <span data-ttu-id="6ecdb-133">Prise en charge du décodage matériel accéléré avec DXVA</span><span class="sxs-lookup"><span data-stu-id="6ecdb-133">Support for hardware accelerated decoding by using DXVA</span></span>

  - <span data-ttu-id="6ecdb-134">Prise en charge de l’encodage matériel accéléré</span><span class="sxs-lookup"><span data-stu-id="6ecdb-134">Support for hardware accelerated encoding</span></span>

  - <span data-ttu-id="6ecdb-135">Nombre de cœurs physiques</span><span class="sxs-lookup"><span data-stu-id="6ecdb-135">Number of physical cores</span></span>

  - <span data-ttu-id="6ecdb-136">Indice de performance Windows (WEI)</span><span class="sxs-lookup"><span data-stu-id="6ecdb-136">Windows Experience Index (WEI)</span></span>

<span data-ttu-id="6ecdb-137">L’Outil d’évaluation système Windows (WinSAT) détermine l’indice WEI.</span><span class="sxs-lookup"><span data-stu-id="6ecdb-137">The Windows System Assessment Tool (WinSAT) determines the WEI.</span></span> <span data-ttu-id="6ecdb-138">Lorsque vous exécutez l’outil de vérification WINS, il génère un document XML d’évaluation formel sur l’ordinateur dans le répertoire% windir% \\ performance \\ WinSAT \\ .</span><span class="sxs-lookup"><span data-stu-id="6ecdb-138">When you run the WinSAT tool, it generates a Formal.Assessment XML document on the computer in the %windir%\\Performance\\WinSAT\\DataStore directory.</span></span> <span data-ttu-id="6ecdb-139">Ce fichier XML contient les deux scores suivants qui sont essentiels pour déterminer les capacités d’encodage et de décodage :</span><span class="sxs-lookup"><span data-stu-id="6ecdb-139">This XML file contains the following two scores that are of particular importance for determining encoding and decoding capabilities:</span></span>

  - <span data-ttu-id="6ecdb-140">La valeur VideoEncodeScore indique la capacité d’encodage vidéo logiciel de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="6ecdb-140">The VideoEncodeScore indicates the software-based video encoding capability of the computer.</span></span>

  - <span data-ttu-id="6ecdb-141">La valeur GraphicsScore indique la capacité d’encodage matériel accéléré de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="6ecdb-141">The GraphicsScore value indicates the hardware accelerated encoding capability of the computer.</span></span>

<span data-ttu-id="6ecdb-p106">Les trois tableaux suivants expliquent les capacités d’encodage et de décodage maximales pour différents types de PC en fonction de l’accélération matérielle prise en charge. Pour des résolutions de 640x360 et supérieures, la fréquence d’images maximale prise en charge est de 30 images par secondes (i/s). Pour des résolutions inférieures à 640x360, la fréquence d’images maximale prise en charge est de 15 i/s.</span><span class="sxs-lookup"><span data-stu-id="6ecdb-p106">The following three tables explain the maximum encoding and decoding capability for different PC types depending on what hardware acceleration they support. For resolutions of 640x360 and higher, the maximum supported frame rate is 30 frames per second (fps). For resolutions lower than 640x360, the maximum supported frame rate is 15 fps.</span></span>

### <a name="computer-without-dxva-and-without-hardware-accelerated-encoder"></a><span data-ttu-id="6ecdb-145">Ordinateur sans DXVA et sans encodeur matériel accéléré</span><span class="sxs-lookup"><span data-stu-id="6ecdb-145">Computer Without DXVA And Without Hardware Accelerated Encoder</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6ecdb-146">Résolution d’encodeur compatible</span><span class="sxs-lookup"><span data-stu-id="6ecdb-146">Capable Encoder Resolution</span></span></th>
<th><span data-ttu-id="6ecdb-147">Résolution de décodeur compatible</span><span class="sxs-lookup"><span data-stu-id="6ecdb-147">Capable Decoder Resolution</span></span></th>
<th><span data-ttu-id="6ecdb-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6ecdb-148">Requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6ecdb-149">424x240</span><span class="sxs-lookup"><span data-stu-id="6ecdb-149">424x240</span></span></p></td>
<td><p><span data-ttu-id="6ecdb-150">424x240 (640x360 à 15 i/s pour des scénarios de réception uniquement)</span><span class="sxs-lookup"><span data-stu-id="6ecdb-150">424x240 (640x360 at 15fps for receive only scenarios)</span></span></p></td>
<td><p><span data-ttu-id="6ecdb-151">1 cœur et VideoEncodeScore ≥ 4,0</span><span class="sxs-lookup"><span data-stu-id="6ecdb-151">1 Core and VideoEncodeScore ≥ 4.0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ecdb-152">640x360</span><span class="sxs-lookup"><span data-stu-id="6ecdb-152">640x360</span></span></p></td>
<td><p><span data-ttu-id="6ecdb-153">640x360</span><span class="sxs-lookup"><span data-stu-id="6ecdb-153">640x360</span></span></p></td>
<td><p><span data-ttu-id="6ecdb-154">2 cœurs et VideoEncodeScore ≥ 4,5</span><span class="sxs-lookup"><span data-stu-id="6ecdb-154">2 Cores and VideoEncodeScore ≥ 4.5</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ecdb-155">640x360</span><span class="sxs-lookup"><span data-stu-id="6ecdb-155">640x360</span></span></p></td>
<td><p><span data-ttu-id="6ecdb-156">1280x720</span><span class="sxs-lookup"><span data-stu-id="6ecdb-156">1280x720</span></span></p></td>
<td><p><span data-ttu-id="6ecdb-157">2 cœurs et VideoEncodeScore ≥ 4,5</span><span class="sxs-lookup"><span data-stu-id="6ecdb-157">2 Cores and VideoEncodeScore ≥ 4.5</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ecdb-158">640x360</span><span class="sxs-lookup"><span data-stu-id="6ecdb-158">640x360</span></span></p></td>
<td><p><span data-ttu-id="6ecdb-159">1920x1080</span><span class="sxs-lookup"><span data-stu-id="6ecdb-159">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="6ecdb-160">4 cœurs et VideoEncodeScore ≥ 4,5</span><span class="sxs-lookup"><span data-stu-id="6ecdb-160">4 Cores and VideoEncodeScore ≥ 4.5</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ecdb-161">1280x720</span><span class="sxs-lookup"><span data-stu-id="6ecdb-161">1280x720</span></span></p></td>
<td><p><span data-ttu-id="6ecdb-162">1280x720</span><span class="sxs-lookup"><span data-stu-id="6ecdb-162">1280x720</span></span></p></td>
<td><p><span data-ttu-id="6ecdb-163">4 cœurs et VideoEncodeScore ≥ 7,3</span><span class="sxs-lookup"><span data-stu-id="6ecdb-163">4 Cores and VideoEncodeScore ≥ 7.3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ecdb-164">1280x720</span><span class="sxs-lookup"><span data-stu-id="6ecdb-164">1280x720</span></span></p></td>
<td><p><span data-ttu-id="6ecdb-165">1920x1080</span><span class="sxs-lookup"><span data-stu-id="6ecdb-165">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="6ecdb-166">4 cœurs et VideoEncodeScore ≥ 7,3</span><span class="sxs-lookup"><span data-stu-id="6ecdb-166">4 Cores and VideoEncodeScore ≥ 7.3</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ecdb-167">1920x1080</span><span class="sxs-lookup"><span data-stu-id="6ecdb-167">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="6ecdb-168">1920x1080</span><span class="sxs-lookup"><span data-stu-id="6ecdb-168">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="6ecdb-169">N/A</span><span class="sxs-lookup"><span data-stu-id="6ecdb-169">N/A</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="computer-with-dxva-but-without-hardware-accelerated-encoder"></a><span data-ttu-id="6ecdb-170">Ordinateur avec DXVA mais sans encodeur matériel accéléré</span><span class="sxs-lookup"><span data-stu-id="6ecdb-170">Computer With DXVA But Without Hardware Accelerated Encoder</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6ecdb-171">Résolution d’encodeur compatible</span><span class="sxs-lookup"><span data-stu-id="6ecdb-171">Capable Encoder Resolution</span></span></th>
<th><span data-ttu-id="6ecdb-172">Résolution de décodeur compatible</span><span class="sxs-lookup"><span data-stu-id="6ecdb-172">Capable Decoder Resolution</span></span></th>
<th><span data-ttu-id="6ecdb-173">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6ecdb-173">Requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6ecdb-174">424x240</span><span class="sxs-lookup"><span data-stu-id="6ecdb-174">424x240</span></span></p></td>
<td><p><span data-ttu-id="6ecdb-175">1920x1080</span><span class="sxs-lookup"><span data-stu-id="6ecdb-175">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="6ecdb-176">1 cœur et VideoEncodeScore ≥ 3,0</span><span class="sxs-lookup"><span data-stu-id="6ecdb-176">1 Core and VideoEncodeScore ≥ 3.0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ecdb-177">640x360</span><span class="sxs-lookup"><span data-stu-id="6ecdb-177">640x360</span></span></p></td>
<td><p><span data-ttu-id="6ecdb-178">1920x1080</span><span class="sxs-lookup"><span data-stu-id="6ecdb-178">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="6ecdb-179">2 cœurs et VideoEncodeScore ≥ 4,5</span><span class="sxs-lookup"><span data-stu-id="6ecdb-179">2 Cores and VideoEncodeScore ≥ 4.5</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ecdb-180">960x540</span><span class="sxs-lookup"><span data-stu-id="6ecdb-180">960x540</span></span></p></td>
<td><p><span data-ttu-id="6ecdb-181">1920x1080</span><span class="sxs-lookup"><span data-stu-id="6ecdb-181">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="6ecdb-182">2 cœurs et VideoEncodeScore ≥ 6,0</span><span class="sxs-lookup"><span data-stu-id="6ecdb-182">2 Cores and VideoEncodeScore ≥ 6.0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ecdb-183">1280x720</span><span class="sxs-lookup"><span data-stu-id="6ecdb-183">1280x720</span></span></p></td>
<td><p><span data-ttu-id="6ecdb-184">1920x1080</span><span class="sxs-lookup"><span data-stu-id="6ecdb-184">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="6ecdb-185">4 cœurs et VideoEncodeScore ≥ 6,7</span><span class="sxs-lookup"><span data-stu-id="6ecdb-185">4 Cores and VideoEncodeScore ≥ 6.7</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ecdb-186">1920x1080</span><span class="sxs-lookup"><span data-stu-id="6ecdb-186">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="6ecdb-187">1920x1080</span><span class="sxs-lookup"><span data-stu-id="6ecdb-187">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="6ecdb-188">4 cœurs et VideoEncodeScore ≥ 8,2</span><span class="sxs-lookup"><span data-stu-id="6ecdb-188">4 Cores and VideoEncodeScore ≥ 8.2</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="6ecdb-p107">Le score WinSAT sur Windows 7 est limité à un maximum de 7,9. C’est pourquoi la capacité d’encodage d’un ordinateur sans encodeur matériel accéléré ne peut être obtenue que sur Windows 8 ou Windows 8.1, pour lequel le score WinSAT est de 9,9 au maximum.</span><span class="sxs-lookup"><span data-stu-id="6ecdb-p107">The WinSAT score on Windows 7 is limited to a maximum of 7.9. Therefore, the encoding capability for a computer without a hardware accelerated encoder can only be achieved on Windows 8 or Windows 8.1, where the maximum WinSAT score is 9.9.</span></span>



</div>

### <a name="computer-with-dxva-and-with-intel-hd-graphics-hardware-accelerated-encoder"></a><span data-ttu-id="6ecdb-191">Ordinateur avec DXVA et avec un encodeur matériel accéléré Intel HD Graphics</span><span class="sxs-lookup"><span data-stu-id="6ecdb-191">Computer With DXVA And With Intel HD Graphics Hardware Accelerated Encoder</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6ecdb-192">Résolution d’encodeur compatible</span><span class="sxs-lookup"><span data-stu-id="6ecdb-192">Capable Encoder Resolution</span></span></th>
<th><span data-ttu-id="6ecdb-193">Résolution de décodeur compatible</span><span class="sxs-lookup"><span data-stu-id="6ecdb-193">Capable Decoder Resolution</span></span></th>
<th><span data-ttu-id="6ecdb-194">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6ecdb-194">Requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6ecdb-195">1280x720</span><span class="sxs-lookup"><span data-stu-id="6ecdb-195">1280x720</span></span></p></td>
<td><p><span data-ttu-id="6ecdb-196">1920x1080</span><span class="sxs-lookup"><span data-stu-id="6ecdb-196">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="6ecdb-197">Intel HD Graphics deuxième et troisième générations</span><span class="sxs-lookup"><span data-stu-id="6ecdb-197">All 2nd and 3rd generation Intel HD Graphics</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ecdb-198">1920x1080</span><span class="sxs-lookup"><span data-stu-id="6ecdb-198">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="6ecdb-199">1920x1080</span><span class="sxs-lookup"><span data-stu-id="6ecdb-199">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="6ecdb-200">Intel HD Graphics deuxième et troisième générations avec GraphicsScore ≥ 5,0</span><span class="sxs-lookup"><span data-stu-id="6ecdb-200">2nd and 3rd generation Intel HD Graphics and GraphicsScore ≥ 5.0</span></span></p></td>
</tr>
</tbody>
</table>


</div>

</div>

<div>

## <a name="mobile-device-video-capabilities"></a><span data-ttu-id="6ecdb-201">Fonctionnalités vidéo sur les appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="6ecdb-201">Mobile Device Video Capabilities</span></span>

<span data-ttu-id="6ecdb-202">Le tableau ci-dessous décrit les fonctionnalités vidéo maximales pour les appareils mobiles pris en charge.</span><span class="sxs-lookup"><span data-stu-id="6ecdb-202">The following table describes the maximum video capabilities for supported mobile devices.</span></span> <span data-ttu-id="6ecdb-203">Pour plus d’informations sur la prise en charge des appareils mobiles, voir [planification pour les clients mobiles dans Lync Server 2013](lync-server-2013-planning-for-mobile-clients.md).</span><span class="sxs-lookup"><span data-stu-id="6ecdb-203">For more information about mobile device support, see [Planning for mobile clients in Lync Server 2013](lync-server-2013-planning-for-mobile-clients.md).</span></span>


<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6ecdb-204">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="6ecdb-204">Feature</span></span></th>
<th><span data-ttu-id="6ecdb-205">Windows Phone</span><span class="sxs-lookup"><span data-stu-id="6ecdb-205">Windows Phone</span></span></th>
<th><span data-ttu-id="6ecdb-206">iPhone</span><span class="sxs-lookup"><span data-stu-id="6ecdb-206">iPhone</span></span></th>
<th><span data-ttu-id="6ecdb-207">iPad</span><span class="sxs-lookup"><span data-stu-id="6ecdb-207">iPad</span></span></th>
<th><span data-ttu-id="6ecdb-208">Android</span><span class="sxs-lookup"><span data-stu-id="6ecdb-208">Android</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6ecdb-209">Résolution d’encodage maximale H.264</span><span class="sxs-lookup"><span data-stu-id="6ecdb-209">H.264 encoding maximum resolution</span></span></p></td>
<td><p><span data-ttu-id="6ecdb-210">VGA</span><span class="sxs-lookup"><span data-stu-id="6ecdb-210">VGA</span></span></p></td>
<td><p><span data-ttu-id="6ecdb-211">QVGA : iPhone 4S</span><span class="sxs-lookup"><span data-stu-id="6ecdb-211">QVGA: iPhone 4S</span></span></p>
<p><span data-ttu-id="6ecdb-212">VGA : iPhone 5</span><span class="sxs-lookup"><span data-stu-id="6ecdb-212">VGA: iPhone 5</span></span></p>
<p><span data-ttu-id="6ecdb-213">720p : iPhone 5S et version ultérieure</span><span class="sxs-lookup"><span data-stu-id="6ecdb-213">720p: iPhone 5S and later</span></span></p></td>
<td><p><span data-ttu-id="6ecdb-214">VGA : iPad 2 et version ultérieure/iPad mini 1 et version ultérieure</span><span class="sxs-lookup"><span data-stu-id="6ecdb-214">VGA: iPad 2 and later/iPad mini 1 and later</span></span></p>
<p><span data-ttu-id="6ecdb-215">720p : iPad Air/iPad mini 2/iPad Pro et version ultérieure</span><span class="sxs-lookup"><span data-stu-id="6ecdb-215">720p: iPad Air/iPad mini 2/iPad Pro and later</span></span></p></td>
<td><p><span data-ttu-id="6ecdb-216">Jusqu’à VGA en fonction du modèle d’appareil</span><span class="sxs-lookup"><span data-stu-id="6ecdb-216">Up to VGA depending on device model</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ecdb-217">Résolution de décodage maximale H.264</span><span class="sxs-lookup"><span data-stu-id="6ecdb-217">H.264 decoding maximum resolution</span></span></p></td>
<td><p><span data-ttu-id="6ecdb-218">VGA</span><span class="sxs-lookup"><span data-stu-id="6ecdb-218">VGA</span></span></p></td>
<td><p><span data-ttu-id="6ecdb-219">QVGA : iPhone 4S</span><span class="sxs-lookup"><span data-stu-id="6ecdb-219">QVGA: iPhone 4S</span></span></p>
<p><span data-ttu-id="6ecdb-220">VGA : iPhone 5</span><span class="sxs-lookup"><span data-stu-id="6ecdb-220">VGA: iPhone 5</span></span></p>
<p><span data-ttu-id="6ecdb-221">720p : iPhone 5S et version ultérieure</span><span class="sxs-lookup"><span data-stu-id="6ecdb-221">720p: iPhone 5S and later</span></span></p></td>
<td><p><span data-ttu-id="6ecdb-222">VGA : iPad 2 et version ultérieure/iPad mini 1 et version ultérieure</span><span class="sxs-lookup"><span data-stu-id="6ecdb-222">VGA: iPad 2 and later/iPad mini 1 and later</span></span></p>
<p><span data-ttu-id="6ecdb-223">720p : iPad Air/iPad mini 2/iPad Pro et version ultérieure</span><span class="sxs-lookup"><span data-stu-id="6ecdb-223">720p: iPad Air/iPad mini 2/iPad Pro and later</span></span></p></td>
<td><p><span data-ttu-id="6ecdb-224">Jusqu’à VGA en fonction du modèle d’appareil</span><span class="sxs-lookup"><span data-stu-id="6ecdb-224">Up to VGA depending on device model</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="6ecdb-225">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6ecdb-225">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

