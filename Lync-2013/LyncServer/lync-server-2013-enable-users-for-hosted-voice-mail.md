---
title: 'Lync Server 2013 : Activation des utilisateurs pour la messagerie vocale hébergée'
description: 'Lync Server 2013 : activez les utilisateurs pour la messagerie vocale hébergée.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enable users for hosted voice mail
ms:assetid: fa559f8f-ef99-43a1-b580-9e998b95efb8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413062(v=OCS.15)
ms:contentKeyID: 48185919
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3853a70d433c09029a02f2ca6256b5988defdcb2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437468"
---
# <a name="enable-users-for-hosted-voice-mail-in-lync-server-2013"></a><span data-ttu-id="e4de1-103">Activation des utilisateurs pour la messagerie vocale hébergée dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e4de1-103">Enable users for hosted voice mail in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e4de1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e4de1-104">

<span> </span></span></span>

<span data-ttu-id="e4de1-105">_**Dernière modification de la rubrique :** 2012-09-24_</span><span class="sxs-lookup"><span data-stu-id="e4de1-105">_**Topic Last Modified:** 2012-09-24_</span></span>

<span data-ttu-id="e4de1-106">Suivez la procédure pour activer les utilisateurs de Lync Server 2013 pour la messagerie vocale sur un service de messagerie unifiée Exchange hébergé.</span><span class="sxs-lookup"><span data-stu-id="e4de1-106">Follow the procedure to enable Lync Server 2013 users for voice mail on a hosted Exchange Unified Messaging (UM) service.</span></span>

<span data-ttu-id="e4de1-107">Pour plus d’informations, reportez-vous à la rubrique [gestion des utilisateurs Exchange hébergés dans Lync Server 2013](lync-server-2013-hosted-exchange-user-management.md) dans la documentation de planification.</span><span class="sxs-lookup"><span data-stu-id="e4de1-107">For details, see [Hosted Exchange user management in Lync Server 2013](lync-server-2013-hosted-exchange-user-management.md) in the Planning documentation.</span></span>

<span data-ttu-id="e4de1-108">Pour plus d’informations sur l’applet [de connexion Set-Csuser](https://docs.microsoft.com/powershell/module/skype/Set-CsUser) , voir la documentation Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="e4de1-108">For details about the [Set-CsUser](https://docs.microsoft.com/powershell/module/skype/Set-CsUser) cmdlet, see the Lync Server Management Shell documentation.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="e4de1-109">Pour 2013 que l’utilisateur de la messagerie vocale hébergée puisse être activé, une stratégie de messagerie vocale hébergée qui s’applique à son compte d’utilisateur doit être déployée.</span><span class="sxs-lookup"><span data-stu-id="e4de1-109">Before a Lync Server 2013 user can be enabled for hosted voice mail, a hosted voice mail policy that applies to their user account must be deployed.</span></span> <span data-ttu-id="e4de1-110">Pour plus d’informations, reportez-vous <A href="lync-server-2013-hosted-voice-mail-policies.md">à stratégies de messagerie vocale hébergées dans Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="e4de1-110">For details, see <A href="lync-server-2013-hosted-voice-mail-policies.md">Hosted voice mail policies in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="to-enable-users-for-hosted-voice-mail"></a><span data-ttu-id="e4de1-111">Pour autoriser les utilisateurs à utiliser la messagerie vocale hébergée</span><span class="sxs-lookup"><span data-stu-id="e4de1-111">To enable users for hosted voice mail</span></span>

1.  <span data-ttu-id="e4de1-112">Démarrez Lync Server Management Shell : cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="e4de1-112">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="e4de1-113">Exécutez l’applet de dialogue Set-CsUser pour configurer le compte d’utilisateur pour la messagerie vocale hébergée.</span><span class="sxs-lookup"><span data-stu-id="e4de1-113">Run the Set-CsUser cmdlet to configure the user account for hosted voice mail.</span></span> <span data-ttu-id="e4de1-114">Par exemple, exécutez :</span><span class="sxs-lookup"><span data-stu-id="e4de1-114">For example, run:</span></span>
    
        Set-CsUser -HostedVoiceMail $True -Identity "contoso\kenmyer"
    
    <span data-ttu-id="e4de1-115">L’exemple qui précède définit les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="e4de1-115">The preceding example sets the following parameters:</span></span>
    
      - <span data-ttu-id="e4de1-116">**HostedVoiceMail** permet d’acheminer les appels de messagerie vocale d’un utilisateur vers la messagerie unifiée Exchange hébergée.</span><span class="sxs-lookup"><span data-stu-id="e4de1-116">**HostedVoiceMail** enables a user’s voice mail calls to be routed to hosted Exchange UM.</span></span> <span data-ttu-id="e4de1-117">Il signale également Microsoft Lync 2013 pour allumer l’indicateur « appel de la messagerie vocale ».</span><span class="sxs-lookup"><span data-stu-id="e4de1-117">It also signals Microsoft Lync 2013 to light up the “call voice mail” indicator.</span></span>
    
      - <span data-ttu-id="e4de1-118">**Identité** indique le compte d’utilisateur à modifier.</span><span class="sxs-lookup"><span data-stu-id="e4de1-118">**Identity** specifies the user account to be modified.</span></span> <span data-ttu-id="e4de1-119">La valeur IDENTITY peut être spécifiée en utilisant l’un des formats suivants :</span><span class="sxs-lookup"><span data-stu-id="e4de1-119">The Identity value can be specified using any of the following formats:</span></span>
        
          - <span data-ttu-id="e4de1-120">Adresse SIP de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="e4de1-120">The user's SIP address</span></span>
        
          - <span data-ttu-id="e4de1-121">Nom d’utilisateur principal d’Active Directory de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="e4de1-121">The user's Active Directory User-Principal-Name</span></span>
        
          - <span data-ttu-id="e4de1-122">Le nom de connexion au domaine de l’utilisateur \\ (par exemple, Contoso \\ kenmyer);</span><span class="sxs-lookup"><span data-stu-id="e4de1-122">The user's domain\\logon name (for example, contoso\\kenmyer)</span></span>
        
          - <span data-ttu-id="e4de1-123">Le Display-Name de services de domaine Active Directory de l’utilisateur (par exemple, Ken Myer).</span><span class="sxs-lookup"><span data-stu-id="e4de1-123">The user's Active Directory Domain Services Display-Name (for example, Ken Myer).</span></span> <span data-ttu-id="e4de1-124">Si vous utilisez le Display-Name comme valeur d’identité, vous pouvez utiliser le \* caractère générique astérisque ().</span><span class="sxs-lookup"><span data-stu-id="e4de1-124">If using the Display-Name as the Identity value, you can use the asterisk (\*) wildcard character.</span></span> <span data-ttu-id="e4de1-125">Par exemple, l’identité « \* Smith » renvoie tous les utilisateurs qui ont une Display-Name se terminant par la valeur de chaîne « Smith ».</span><span class="sxs-lookup"><span data-stu-id="e4de1-125">For example, the Identity "\* Smith" returns all the users who have a Display-Name that ends with the string value "Smith".</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="e4de1-126">Le nom de compte SAM-nom Active Directory de l’utilisateur ne peut pas être utilisé en tant que valeur d’identité, car le nom de compte SAM n’est pas nécessairement unique dans la forêt.</span><span class="sxs-lookup"><span data-stu-id="e4de1-126">The user’s Active Directory SAM-Account-Name cannot be used as the Identity value because the SAM-Account-Name is not necessarily unique in the forest.</span></span>

        
        <span data-ttu-id="e4de1-127"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e4de1-127"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

