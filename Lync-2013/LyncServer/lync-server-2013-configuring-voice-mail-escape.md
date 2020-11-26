---
title: 'Lync Server 2013 : configuration de l’échappement de la messagerie vocale'
description: 'Lync Server 2013 : configuration de l’échappement de la messagerie vocale.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring voice mail escape
ms:assetid: a1d19e6c-82ff-4768-8ae5-da981368ce40
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688157(v=OCS.15)
ms:contentKeyID: 49733761
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: afbb2dd10c7ff8809eb8dfbcc64e40a599aa06a4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432400"
---
# <a name="configuring-voice-mail-escape-in-lync-server-2013"></a><span data-ttu-id="13860-103">Configuration de l’échappement de la messagerie vocale dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="13860-103">Configuring voice mail escape in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="13860-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="13860-104">

<span> </span></span></span>

<span data-ttu-id="13860-105">_**Dernière modification de la rubrique :** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="13860-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="13860-106">Lorsqu’un utilisateur configure la sonnerie simultanée sur un téléphone mobile, un appelant est généralement routé vers la messagerie vocale personnelle de l’utilisateur si le téléphone mobile est éteint, n’a plus de batterie ou est hors réseau.</span><span class="sxs-lookup"><span data-stu-id="13860-106">When a user configures simultaneous ringing to a mobile phone, a caller will typically be routed to the user’s personal voice mail if the mobile phone is turned off, out of battery power, or out of range.</span></span> <span data-ttu-id="13860-107">Avec Lync Server 2013, les utilisateurs peuvent choisir de faire Router leurs appels d’entreprise vers leur système de messagerie vocale.</span><span class="sxs-lookup"><span data-stu-id="13860-107">With Lync Server 2013, users can opt to have business-related calls routed to their corporate voice mail system.</span></span> <span data-ttu-id="13860-108">Plus précisément, un minuteur peut être configuré, et si l’appel est traité par la messagerie vocale de l’opérateur dans la plage de temps définie, Lync Server se déconnecte du système de messagerie vocale de l’opérateur (et de la messagerie vocale personnelle de l’utilisateur), tandis que les points de terminaison du système d’entreprise continuent à sonner.</span><span class="sxs-lookup"><span data-stu-id="13860-108">Specifically, a timer can be configured, and if the call is answered by the carrier’s voice mail within the range of time defined, Lync Server will disconnect from the carrier’s voice mail system (and the user’s personal voice mail), while the user’s remaining endpoints in the corporate system continue to ring.</span></span> <span data-ttu-id="13860-109">De cette manière, l’appelant est acheminé automatiquement vers la messagerie vocale d’entreprise de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="13860-109">This way, the caller is automatically routed to the user’s corporate voice mail.</span></span>

<span data-ttu-id="13860-110">Cette configuration est effectuée à l’aide de l’applet de commande Lync Server Management Shell, **Set-CsVoicePolicy**, au niveau de la stratégie vocale, avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="13860-110">This configuration is performed using the Lync Server Management Shell cmdlet, **Set-CsVoicePolicy**, at the voice policy level, with the following parameters.</span></span>

<div>

## <a name="to-configure-voice-mail-escape"></a><span data-ttu-id="13860-111">Pour configurer la redirection vers la messagerie vocale</span><span class="sxs-lookup"><span data-stu-id="13860-111">To configure voice mail escape</span></span>

1.  <span data-ttu-id="13860-112">Démarrez Lync Server Management Shell : cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="13860-112">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="13860-113">Spécifiez les paramètres ci-dessous sur **Set-CsVoicePolicy** :</span><span class="sxs-lookup"><span data-stu-id="13860-113">Specify the following parameters to **Set-CsVoicePolicy**:</span></span>
    
      - <span data-ttu-id="13860-114">**EnableVoicemailEscapeTimer** : active ou désactive le minuteur de redirection.</span><span class="sxs-lookup"><span data-stu-id="13860-114">**EnableVoicemailEscapeTimer** - Enables or disables the escape timer.</span></span>
    
      - <span data-ttu-id="13860-p102">**PSTNVoicemailEscapeTimer** : spécifie la valeur de délai d’attente en millisecondes. La valeur par défaut est 1 500 millisecondes et la valeur peut être comprise entre 0 milliseconde et 8 000 millisecondes.</span><span class="sxs-lookup"><span data-stu-id="13860-p102">**PSTNVoicemailEscapeTimer** - Specifies the timeout value in milliseconds. The default value is 1500 milliseconds, and the value can range from 0 milliseconds to 8000 milliseconds.</span></span>

</div>

<div>

## <a name="example"></a><span data-ttu-id="13860-117">Exemple</span><span class="sxs-lookup"><span data-stu-id="13860-117">Example</span></span>

    Set-CsVoicePolicy UserVoicePolicy -EnableVoiceMailEscapeTimer $true - PSTNVoicemailEscapeTimer 2000
    
    Set-CsVoicePolicy -Identity site:SitePolicy -EnableVoiceMailEscapeTimer $true -PSTNVoicemailEscapeTimer 1500

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="13860-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="13860-118">See Also</span></span>


[<span data-ttu-id="13860-119">Configuration des stratégies de voix et des enregistrements d’utilisation RTC pour autoriser les fonctionnalités d’appel et les privilèges dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="13860-119">Configuring voice policies and PSTN usage records to authorize calling features and privileges in Lync Server 2013</span></span>](lync-server-2013-configuring-voice-policies-and-pstn-usage-records-to-authorize-calling-features-and-privileges.md)  
  

<span data-ttu-id="13860-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="13860-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

