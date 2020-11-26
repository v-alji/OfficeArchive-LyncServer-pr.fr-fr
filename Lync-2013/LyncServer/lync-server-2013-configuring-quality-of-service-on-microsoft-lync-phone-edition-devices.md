---
title: Configuration de la qualité de service sur les appareils Microsoft Lync Phone Edition
description: Configuration de la qualité de service sur les appareils Microsoft Lync Phone Edition.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Quality of Service on Microsoft Lync Phone Edition devices
ms:assetid: a6eb2620-a512-4ab6-bdfd-eb76be43bbfe
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205137(v=OCS.15)
ms:contentKeyID: 48185004
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c0d1e4f10c6b4a550f5da25f8bd2e9fe97606255
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432701"
---
# <a name="configuring-quality-of-service-on-microsoft-lync-phone-edition-devices-in-lync-server-2013"></a><span data-ttu-id="08582-103">Configuration de la qualité de service sur les appareils Microsoft Lync Phone Edition dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="08582-103">Configuring Quality of Service on Microsoft Lync Phone Edition devices in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="08582-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="08582-104">

<span> </span></span></span>

<span data-ttu-id="08582-105">_**Dernière modification de la rubrique :** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="08582-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="08582-106">Même si la qualité de service (QoS) n’est pas activée par défaut pour les appareils tels que les iPhone, la qualité de service (QoS) est activée par défaut pour les appareils exécutant Lync Phone Edition.</span><span class="sxs-lookup"><span data-stu-id="08582-106">Although Quality of Service (QoS) is not enabled by default for devices such as iPhones, QoS is enabled by default for devices running Lync Phone Edition.</span></span> <span data-ttu-id="08582-107">(Ces appareils sont généralement désignés sous le nom de téléphones de communications unifiées ou unifiées.) Pour vérifier cela, exécutez la commande Windows PowerShell suivante à partir de Lync Server Management Shell :</span><span class="sxs-lookup"><span data-stu-id="08582-107">(These devices are commonly referred to as UC or Unified Communication phones.) To verify this, run the following Windows PowerShell command from within the Lync Server Management Shell:</span></span>

    Get-CsUCPhoneConfiguration

<span data-ttu-id="08582-108">Si vous n’avez apporté aucune modification aux paramètres de configuration de votre téléphone UC, vous obtiendrez des informations similaires à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="08582-108">If you have not made any changes to your UC phone configuration settings then you will get back information that looks like this:</span></span>

    Identity             : Global
    CalendarPollInterval : 00:03:00
    EnforcePhoneLock     : True
    PhoneLockTimeout     : 00:10:00
    MinPhonePinLength    : 6
    SIPSecurityMode      : High
    VoiceDiffServTag     : 40
    Voice8021p           : 0
    LoggingLevel         : Off

<span data-ttu-id="08582-109">Pour des raisons de qualité de service, une seule de ces propriétés est particulièrement intéressante : VoiceDiffServTag.</span><span class="sxs-lookup"><span data-stu-id="08582-109">For Quality of Service purposes, only one of these properties is of interest: VoiceDiffServTag.</span></span> <span data-ttu-id="08582-110">Le VoiceDiffServTag représente la valeur DSCP affectée au trafic vocal émis à partir d’un appareil Lync Phone Edition.</span><span class="sxs-lookup"><span data-stu-id="08582-110">The VoiceDiffServTag represents the DSCP value assigned to voice traffic emanating from a Lync Phone Edition device.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="08582-111">Le paramètre Voice8021p n’est plus pris en charge dans Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="08582-111">The Voice8021p parameter is no longer supported in Lync Server 2013.</span></span> <span data-ttu-id="08582-112">Le paramètre reste valide pour la compatibilité descendante avec Microsoft Lync Server 2010 ; Néanmoins, il n’a aucun effet sur les appareils utilisés avec Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="08582-112">The parameter is still valid for backward compatibility with Microsoft Lync Server 2010; however, it has no effect on devices used with Lync Server 2013.</span></span>



</div>

<span data-ttu-id="08582-113">Dans la plupart des réseaux, le marquage de paquets Lync Phone Edition avec un VoiceDiffServTag de 40 ne doit pas provoquer de problèmes.</span><span class="sxs-lookup"><span data-stu-id="08582-113">In most networks, marking Lync Phone Edition packets with a VoiceDiffServTag of 40 should not cause any problems.</span></span> <span data-ttu-id="08582-114">À la place, le trafic audio est presque toujours marqué avec le le code DSCP 46.</span><span class="sxs-lookup"><span data-stu-id="08582-114">However, 40 is not the value typically used for audio traffic; instead, audio traffic is almost always marked with the DSCP code 46.</span></span> <span data-ttu-id="08582-115">Pour garantir la cohérence de votre réseau, il peut être préférable de changer la propriété VoiceDiffServTag de vos téléphones UC vers 46.</span><span class="sxs-lookup"><span data-stu-id="08582-115">In order to maintain consistency throughout your network, you might want to change the VoiceDiffServTag property of your UC phones to 46.</span></span>

<span data-ttu-id="08582-116">Pour ce faire, vous pouvez utiliser Windows PowerShell ou le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="08582-116">To do that, you can use either Windows PowerShell or the Lync Server Control Panel.</span></span> <span data-ttu-id="08582-117">Pour modifier la valeur VoiceDiffServTag à l’aide de Windows PowerShell, exécutez la commande suivante à partir de Lync Server Management Shell :</span><span class="sxs-lookup"><span data-stu-id="08582-117">To modify the VoiceDiffServTag value by using Windows PowerShell, run the following command from within the Lync Server Management Shell:</span></span>

    Set-CsUCPhoneConfiguration -VoiceDiffServTag 46

<span data-ttu-id="08582-118">La commande précédente modifie la collection globale des paramètres de configuration de téléphone UC.</span><span class="sxs-lookup"><span data-stu-id="08582-118">The preceding command modifies the global collection of UC phone configuration settings.</span></span> <span data-ttu-id="08582-119">Notez, toutefois, que les paramètres de téléphone monouc peuvent également être attribués à l’étendue du site.</span><span class="sxs-lookup"><span data-stu-id="08582-119">Note, however, that UC phone settings can also be assigned to the site scope.</span></span> <span data-ttu-id="08582-120">Pour modifier les paramètres de configuration de téléphone UC sur l’étendue du site, vous devez spécifier l’identité du site.</span><span class="sxs-lookup"><span data-stu-id="08582-120">To modify UC phone configuration settings at the site scope, you must specify the site Identity.</span></span> <span data-ttu-id="08582-121">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="08582-121">For example:</span></span>

    Set-CsUCPhoneConfiguration -Identity "site:Redmond" -VoiceDiffServTag 46

<span data-ttu-id="08582-122">Vous pouvez également utiliser la commande suivante pour modifier simultanément l’ensemble des paramètres de configuration du téléphone de communications unifiées :</span><span class="sxs-lookup"><span data-stu-id="08582-122">You can also use the following command to simultaneously modify all your UC phone configuration settings:</span></span>

    Get-CsUCPhoneConfiguration | Set-CsUCPhoneConfiguration -VoiceDiffServTag 46

<span data-ttu-id="08582-123">Si vous préférez apporter cette modification à l’aide du panneau de configuration de Lync Server, démarrez le panneau de configuration, puis procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="08582-123">If you prefer to make this change using Lync Server Control Panel, then start the Control Panel and then complete the following procedure:</span></span>

1.  <span data-ttu-id="08582-124">Cliquez sur **clients** , puis sur Configuration de l' **appareil**.</span><span class="sxs-lookup"><span data-stu-id="08582-124">Click **Clients** and then click **Device Configuration**.</span></span>

2.  <span data-ttu-id="08582-125">Dans l’onglet Configuration de l' **appareil** , double-cliquez sur l’ensemble de paramètres que vous souhaitez modifier (par exemple, **Global**).</span><span class="sxs-lookup"><span data-stu-id="08582-125">On the **Device Configuration** tab, double-click the collection of settings you want to modify (for example, **Global**).</span></span>

3.  <span data-ttu-id="08582-126">Dans la boîte de dialogue **modifier la configuration** de l’appareil, définissez la valeur de la zone **qualité de service (QoS)** sur **46** , puis cliquez sur **valider**.</span><span class="sxs-lookup"><span data-stu-id="08582-126">In the **Edit Device Configuration** dialog box, set the value of the **Voice Quality of Service (QoS)** box to **46** and then click **Commit**.</span></span>

<span data-ttu-id="08582-127">Si vous avez plusieurs collections, vous devrez répéter ce processus pour chaque ensemble de paramètres de téléphone de communications unifiées.</span><span class="sxs-lookup"><span data-stu-id="08582-127">If you have multiple collections you will need to repeat this process for each collection of UC phone settings.</span></span> <span data-ttu-id="08582-128">Le panneau de configuration de Lync Server ne vous permet pas de modifier simultanément plusieurs collections de paramètres.</span><span class="sxs-lookup"><span data-stu-id="08582-128">Lync Server Control Panel will not allow you to simultaneously modify multiple setting collections.</span></span>

<span data-ttu-id="08582-129">Si vous disposez de périphériques qui ne sont pas basés sur le système d’exploitation Windows (par exemple, iPhone) au sein de votre organisation, ces appareils ne sont pas touchés par le changement du paramètre VoiceDiffServTag.</span><span class="sxs-lookup"><span data-stu-id="08582-129">If you have devices that are not based on the Windows operating system (such as iPhones) in your organization these devices will not be affected by changing the VoiceDiffServTag setting.</span></span> <span data-ttu-id="08582-130">Pour modifier les valeurs DSCP sur ces appareils, vous devez vous référer au manuel d’administration de chaque type d’appareil.</span><span class="sxs-lookup"><span data-stu-id="08582-130">If you want to change DSCP values on those devices you will need to refer to the administration manual for each of your device types.</span></span>

<span data-ttu-id="08582-131"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="08582-131"></div>

<span> </span>

</div>

</div>

</span></span></div>

