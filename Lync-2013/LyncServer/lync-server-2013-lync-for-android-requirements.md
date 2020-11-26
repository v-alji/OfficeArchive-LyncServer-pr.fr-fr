---
title: 'Configuration requise pour Lync Server 2013 : Lync pour Android'
description: 'Configuration requise pour Lync Server 2013 : Lync pour Android.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Lync for Android requirements
ms:assetid: 4ff53e03-0c1f-4a2b-9cec-1131c2a48563
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690980(v=OCS.15)
ms:contentKeyID: 53312965
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2d3d3aa6e428c3a73f1b9263fe9cf13e5aa9fff0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426416"
---
# <a name="lync-for-android-requirements-in-lync-server-2013"></a><span data-ttu-id="0d3ef-103">Configuration requise pour Lync pour Android dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0d3ef-103">Lync for Android requirements in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0d3ef-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0d3ef-104">

<span> </span></span></span>

<span data-ttu-id="0d3ef-105">_**Dernière modification de la rubrique :** 2014-04-24_</span><span class="sxs-lookup"><span data-stu-id="0d3ef-105">_**Topic Last Modified:** 2014-04-24_</span></span>

<span data-ttu-id="0d3ef-106">Microsoft Lync 2013 Microsoft Lync 2013 pour Android fournit des fonctionnalités de messagerie instantanée, de présence améliorée et de participation à une réunion Lync pour les utilisateurs de votre organisation qui se connectent à partir d’un appareil Android.</span><span class="sxs-lookup"><span data-stu-id="0d3ef-106">Microsoft Lync 2013 Microsoft Lync 2013 for Android provides instant messaging (IM), enhanced presence, and Lync meeting join capabilities for users in your organization who are connecting from an Android device.</span></span> <span data-ttu-id="0d3ef-107">Cette rubrique décrit les considérations relatives à Lync 2013 pour Android, notamment les conditions préalables, les exigences techniques et les composants requis.</span><span class="sxs-lookup"><span data-stu-id="0d3ef-107">This topic describes considerations for Lync 2013 for Android, including prerequisites, technical requirements, and required components.</span></span>

<div>

## <a name="lync-for-android-prerequisite"></a><span data-ttu-id="0d3ef-108">Prérequis Lync pour Android</span><span class="sxs-lookup"><span data-stu-id="0d3ef-108">Lync for Android Prerequisite</span></span>

<span data-ttu-id="0d3ef-109">Pour prendre en charge Lync 2013 pour Android, l’appareil Android doit satisfaire les exigences suivantes :</span><span class="sxs-lookup"><span data-stu-id="0d3ef-109">To support Lync 2013 for Android, the Android device must meet the following requirements:</span></span>

  - <span data-ttu-id="0d3ef-110">L’appareil Android doit exécuter Android 4,0 ou une version ultérieure du système d’exploitation basé sur le téléphone ou la tablette, y compris des tablettes, à l’exception de celles dotées du microprocesseur Tegra2.</span><span class="sxs-lookup"><span data-stu-id="0d3ef-110">The Android device must be running Android 4.0 or a later phone- or tablet-oriented operating system, including tablets, except those with the Tegra2 chip.</span></span>

  - <span data-ttu-id="0d3ef-111">L’appareil doit disposer d’un processeur double cœur de 1,2 GHz ou supérieur.</span><span class="sxs-lookup"><span data-stu-id="0d3ef-111">The device must have a 1.2 GHz dual core or higher CPU.</span></span>

  - <span data-ttu-id="0d3ef-112">La résolution de l’appareil photo (avant/arrière) doit être VGA ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="0d3ef-112">The device camera (front/rear) resolution should be VGA or higher.</span></span>

  - <span data-ttu-id="0d3ef-113">Les autres exigences matérielles doivent être alignées sur le document de définition de compatibilité Android 4,0.</span><span class="sxs-lookup"><span data-stu-id="0d3ef-113">Other hardware requirements should be aligned with Android 4.0 Compatibility Definition Document.</span></span>

</div>

<div>

## <a name="other-technical-considerations"></a><span data-ttu-id="0d3ef-114">Autres considérations techniques</span><span class="sxs-lookup"><span data-stu-id="0d3ef-114">Other Technical Considerations</span></span>

<span data-ttu-id="0d3ef-115">Sur la plateforme d’appareil Android, l’application Lync peut s’exécuter en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="0d3ef-115">On the Android device platform, the Lync application can run in the background.</span></span> <span data-ttu-id="0d3ef-116">Par conséquent, contrairement aux autres plateformes d’appareils mobiles, les notifications de transmission ne sont pas requises pour les appareils Android.</span><span class="sxs-lookup"><span data-stu-id="0d3ef-116">Therefore, unlike other mobile device platforms, push notifications are not required for Android devices.</span></span> <span data-ttu-id="0d3ef-117">La seule façon de quitter l’application Lync sur un appareil Android consiste à se déconnecter de Lync explicitement.</span><span class="sxs-lookup"><span data-stu-id="0d3ef-117">The only way to exit the Lync application on an Android device is to explicitly sign out of Lync.</span></span> <span data-ttu-id="0d3ef-118">Cette version de l’application Lync n’est pas prise en charge sur les appareils dotés de chipsets Tegra 2.</span><span class="sxs-lookup"><span data-stu-id="0d3ef-118">This version of the Lync application is not supported on devices with Tegra 2 chipsets.</span></span>

<span data-ttu-id="0d3ef-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0d3ef-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

