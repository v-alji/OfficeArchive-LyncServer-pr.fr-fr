---
title: 'Lync Server 2013 : Configuration des paramètres de réacheminement de la messagerie vocale'
description: 'Lync Server 2013 : configurer les paramètres de reroutage de la messagerie vocale.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure voice mail rerouting settings
ms:assetid: 7ab6be28-eabb-4a79-a796-648887d71b83
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398606(v=OCS.15)
ms:contentKeyID: 48184593
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 669ea5585f9e732b6a49d9749b8939c14b4e0d9f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395232"
---
# <a name="configure-voice-mail-rerouting-settings-in-lync-server-2013"></a><span data-ttu-id="de973-103">Configuration des paramètres de réacheminement de la messagerie vocale dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="de973-103">Configure voice mail rerouting settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="de973-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="de973-104">

<span> </span></span></span>

<span data-ttu-id="de973-105">_**Dernière modification de la rubrique :** 2012-10-18_</span><span class="sxs-lookup"><span data-stu-id="de973-105">_**Topic Last Modified:** 2012-10-18_</span></span>

<span data-ttu-id="de973-106">Les appareils de succursales survivables et les serveurs de succursales surchargés peuvent fournir une survie de la messagerie vocale pour les utilisateurs de succursales en cas de panne du réseau étendu, si la messagerie unifiée Exchange est installée sur le site central et si le standard automatique des messages UM Exchange (AA) est déployé.</span><span class="sxs-lookup"><span data-stu-id="de973-106">Survivable Branch Appliances and Survivable Branch Servers can provide voice mail survivability for branch users during a WAN outage, if Exchange Unified Messaging (UM) is installed at the central site and an Exchange UM Message Auto Attendant (AA) is deployed.</span></span> <span data-ttu-id="de973-107">Nous vous recommandons de configurer le AA pour qu’il accepte uniquement les messages, ce qui désactive d’autres fonctionnalités génériques, telles que le transfert vers un utilisateur ou le transfert vers un opérateur.</span><span class="sxs-lookup"><span data-stu-id="de973-107">We recommend that your Exchange administrator configure the AA to accept messages only, which disables other generic functionality, such as transfer to a user or transfer to an operator.</span></span> <span data-ttu-id="de973-108">Par ailleurs, vous pouvez utiliser un AA générique ou un AA personnalisé pour diriger l’appel.</span><span class="sxs-lookup"><span data-stu-id="de973-108">Alternatively, you might use a generic AA or an AA customized to route the call.</span></span>

<span data-ttu-id="de973-109">Pour plus d’informations, reportez-vous à la section « Préparation de la survie de la messagerie vocale » dans la rubrique Configuration de la [résilience de site pour Lync Server 2013](lync-server-2013-branch-site-resiliency-requirements.md) dans la documentation de planification.</span><span class="sxs-lookup"><span data-stu-id="de973-109">For details, see the “Preparing for Voice Mail Survivability” section of [Branch-site resiliency requirements for Lync Server 2013](lync-server-2013-branch-site-resiliency-requirements.md) in the Planning documentation.</span></span>

<div>

## <a name="to-configure-voice-mail-survivability"></a><span data-ttu-id="de973-110">Pour configurer la survie de la messagerie vocale</span><span class="sxs-lookup"><span data-stu-id="de973-110">To configure voice mail survivability</span></span>

1.  <span data-ttu-id="de973-111">Demandez à votre administrateur Exchange de configurer le système AA pour accepter les messages uniquement (dans l’environnement Exchange, utilisez l’applet de commande suivante : **Set-UMAutoAttendant \<AA name\> -CallSomeoneEnabled $false**.</span><span class="sxs-lookup"><span data-stu-id="de973-111">Ask your Exchange administrator to configure the AA to accept messages only (in the Exchange Shell use the following cmdlet: **Set-UMAutoAttendant \<AA name\> -CallSomeoneEnabled $false**.</span></span> <span data-ttu-id="de973-112">Le paramètre spécifiant d’autoriser les messages de sortie (*SendVoiceMsgEnabled*) est vrai par défaut.</span><span class="sxs-lookup"><span data-stu-id="de973-112">The parameter that specifies to allow leaving messages (*SendVoiceMsgEnabled*) is true by default.</span></span>

2.  <span data-ttu-id="de973-113">Dans Lync Server Management Shell, utilisez l’applet **de nouvelle applet de nouveau-CSVoiceMailReroutingConfiguration** pour définir le numéro de téléphone AA en tant que numéro de téléphone du standard automatique de messagerie unifiée dans la configuration de routage de la messagerie vocale sur l’appareil ou le serveur de succursale Survivable.</span><span class="sxs-lookup"><span data-stu-id="de973-113">In the Lync Server Management Shell, use the **New-CSVoiceMailReroutingConfiguration** cmdlet to set the AA phone number as the Exchange UM Auto Attendant phone number in the voice mail rerouting configuration on the Survivable Branch Appliance or Survivable Branch Server.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="de973-114">Si vous avez besoin de modifier le paramètre de reroutage de la messagerie vocale ultérieurement, utilisez l’applet de passe <STRONG>Set-CsVoiceMailReRoutingConfiguration</STRONG> pour le faire.</span><span class="sxs-lookup"><span data-stu-id="de973-114">If you need to modify the voice mail rerouting setting later, use the <STRONG>Set-CsVoiceMailReRoutingConfiguration</STRONG> cmdlet to do so.</span></span> <span data-ttu-id="de973-115">Pour en savoir plus, à propos <STRONG>des nouvelles</STRONG> et de <STRONG>Set-CSVoiceMailReroutingConfiguration</STRONG>, voir les rubriques d’aide sur l’interpréteur de vue.</span><span class="sxs-lookup"><span data-stu-id="de973-115">For details, about <STRONG>New-</STRONG> and <STRONG>Set-CSVoiceMailReroutingConfiguration</STRONG>, in the Shell Help topics.</span></span>

    
    </div>

3.  <span data-ttu-id="de973-116">Définissez le numéro d’accès de l’abonné Exchange UM qui correspond au plan de numérotation de messagerie UNIFIÉe Exchange de l’utilisateur de succursale en tant que numéro d’accès de l’abonné à la messagerie UNIFIÉe Exchange dans la configuration de routage de la messagerie vocale de l’appareil ou du serveur de succursales Survivables.</span><span class="sxs-lookup"><span data-stu-id="de973-116">Set the Exchange UM subscriber access number that corresponds to the branch user’s Exchange UM dial plan as the Exchange UM subscriber access number in the voice mail rerouting configuration on the Survivable Branch Appliance or Survivable Branch Server.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="de973-117">Configurez le plan de numérotation des utilisateurs d’Exchange UM pour qu’un seul plan de numérotation soit associé à tous les utilisateurs de succursales ayant besoin d’accéder à la fonctionnalité obtenir la messagerie vocale lors d’une panne du réseau étendu.</span><span class="sxs-lookup"><span data-stu-id="de973-117">Configure the Exchange UM users’ dial plan so that there is only one dial plan associated with all branch users who need access to the Get Voice Mail functionality during a WAN outage.</span></span>

    
    </div>

<span data-ttu-id="de973-118">**Étape suivante** pour les appareils de succursales survivables ou les serveurs de succursales survivables : [utilisateurs familiaux sur une unité ou un serveur de succursales survivant dans Lync Server 2013](lync-server-2013-home-users-on-a-survivable-branch-appliance-or-server.md).</span><span class="sxs-lookup"><span data-stu-id="de973-118">**Next step** for Survivable Branch Appliances or Survivable Branch Servers: [Home users on a Survivable Branch Appliance or Server in Lync Server 2013](lync-server-2013-home-users-on-a-survivable-branch-appliance-or-server.md).</span></span>

<span data-ttu-id="de973-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="de973-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

