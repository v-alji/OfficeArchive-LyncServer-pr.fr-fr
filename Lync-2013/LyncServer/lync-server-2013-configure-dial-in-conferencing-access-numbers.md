---
title: 'Lync Server 2013 : Configuration des numéros d’accès aux conférences rendez-vous'
description: 'Lync Server 2013 : configurer des numéros d’accès de conférence rendez-vous.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure dial-in conferencing access numbers
ms:assetid: d8a18030-f318-43dd-834d-70e5014b5e8a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398952(v=OCS.15)
ms:contentKeyID: 48185623
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0edb3492c243b36b69c4b48df8c22adc4ece7999
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395148"
---
# <a name="configure-dial-in-conferencing-access-numbers-in-lync-server-2013"></a><span data-ttu-id="ec78a-103">Configuration des numéros d’accès aux conférences rendez-vous dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ec78a-103">Configure dial-in conferencing access numbers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ec78a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ec78a-104">

<span> </span></span></span>

<span data-ttu-id="ec78a-105">_**Dernière modification de la rubrique :** 2011-07-17_</span><span class="sxs-lookup"><span data-stu-id="ec78a-105">_**Topic Last Modified:** 2011-07-17_</span></span>

<span data-ttu-id="ec78a-106">Lorsque vous déployez des conférences rendez-vous, vous devez configurer les numéros de téléphone que les utilisateurs peuvent appeler à partir du réseau téléphonique commuté pour participer à la partie audio des conférences.</span><span class="sxs-lookup"><span data-stu-id="ec78a-106">When you deploy dial-in conferencing, you need to set up phone numbers that users can dial from the public switched telephone network (PSTN) to join the audio portion of conferences.</span></span> <span data-ttu-id="ec78a-107">Ces numéros s’affichent dans les invitations à une réunion et sur la page web des paramètres de configuration des conférences rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="ec78a-107">These dial-in access numbers appear in meeting invitations and on the Dial-in Conferencing Settings webpage.</span></span>

<span data-ttu-id="ec78a-108">Avant de créer des numéros d’accès aux conférences rendez-vous, vous devez planifier vos régions de conférences rendez-vous puis configurer les plans de numérotation correspondants.</span><span class="sxs-lookup"><span data-stu-id="ec78a-108">Before you can create dial-in access numbers, you must first plan your dial-in conferencing regions and then configure dial plans with the regions.</span></span> <span data-ttu-id="ec78a-109">Pour plus d’informations sur les régions, voir [exigences relatives aux conférences rendez-vous dans Lync Server 2013](lync-server-2013-dial-in-conferencing-requirements.md) dans la documentation de planification.</span><span class="sxs-lookup"><span data-stu-id="ec78a-109">For details about regions, see [Dial-in conferencing requirements in Lync Server 2013](lync-server-2013-dial-in-conferencing-requirements.md) in the Planning documentation.</span></span> <span data-ttu-id="ec78a-110">Pour plus d’informations sur la configuration de plans de numérotation pour les conférences rendez-vous, voir [configurer des plans de numérotation pour les conférences rendez-vous dans Lync Server 2013](lync-server-2013-configure-dial-plans-for-dial-in-conferencing.md).</span><span class="sxs-lookup"><span data-stu-id="ec78a-110">For details about configuring dial plans for dial-in conferencing, see [Configure dial plans for dial-in conferencing in Lync Server 2013](lync-server-2013-configure-dial-plans-for-dial-in-conferencing.md).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="ec78a-111">Vous ne pouvez pas utiliser de nouveau numéro d’accès rendez-vous tant que la réplication des services de domaine Active Directory (AD &nbsp; DS) n’est pas terminée.</span><span class="sxs-lookup"><span data-stu-id="ec78a-111">You cannot use a new dial-in access number until Active Directory Domain Services (AD&nbsp;DS) replication of that access number is complete.</span></span> <span data-ttu-id="ec78a-112">La réplication peut durer plusieurs heures.</span><span class="sxs-lookup"><span data-stu-id="ec78a-112">Replication can take several hours to complete.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="ec78a-113">Une fois que vous avez créé les numéros d’accès aux conférences rendez-vous, vous pouvez modifier le nom complet des objets contact Active Directory pour permettre aux utilisateurs d’identifier plus facilement le numéro d’accès approprié.</span><span class="sxs-lookup"><span data-stu-id="ec78a-113">After you create dial-in access numbers, you can modify the display name for the Active Directory contact objects so that users can more easily identify the correct access number.</span></span> <span data-ttu-id="ec78a-114">Utilisez l’applet de cmdlet <STRONG>Set-CsDialInConferencingAccessNumber</STRONG> pour modifier le nom d’affichage.</span><span class="sxs-lookup"><span data-stu-id="ec78a-114">Use the <STRONG>Set-CsDialInConferencingAccessNumber</STRONG> cmdlet to modify the display name.</span></span> <span data-ttu-id="ec78a-115">Vous ne devez pas modifier manuellement les objets Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ec78a-115">You should not modify Active Directory objects manually.</span></span> <span data-ttu-id="ec78a-116">Pour plus d’informations sur la modification d’un numéro d’accès, reportez-vous à la documentation Lync Server Management Shell pour l’applet <STRONG>de connexion Set-CsDialInConferencingAccessNumber</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="ec78a-116">For details about modifying an access number, see Lync Server Management Shell documentation for the <STRONG>Set-CsDialInConferencingAccessNumber</STRONG> cmdlet.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="ec78a-117">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="ec78a-117">In This Section</span></span>

[<span data-ttu-id="ec78a-118">Création ou modification d’un numéro d’accès à une conférence rendez-vous dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ec78a-118">Create or modify a dial-in conferencing access number in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-dial-in-conferencing-access-number.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="ec78a-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec78a-119">See Also</span></span>


[<span data-ttu-id="ec78a-120">Configuration requise pour les conférences rendez-vous dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ec78a-120">Dial-in conferencing requirements in Lync Server 2013</span></span>](lync-server-2013-dial-in-conferencing-requirements.md)  


[<span data-ttu-id="ec78a-121">Configuration des plans de numérotation pour les conférences rendez-vous dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ec78a-121">Configure dial plans for dial-in conferencing in Lync Server 2013</span></span>](lync-server-2013-configure-dial-plans-for-dial-in-conferencing.md)  
  

<span data-ttu-id="ec78a-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ec78a-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

