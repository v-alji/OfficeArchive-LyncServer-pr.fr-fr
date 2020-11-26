---
title: 'Lync Server 2013 : Configuration du serveur de conversation permanente'
description: 'Lync Server 2013 : configuration du serveur de chat permanent.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure Persistent Chat Server
ms:assetid: 85028aff-a38e-4748-958e-59e707a47532
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205054(v=OCS.15)
ms:contentKeyID: 48184709
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d45320e1fa6b247f13cfffa9945b45390f2ae6c5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433814"
---
# <a name="configure-persistent-chat-server-in-lync-server-2013"></a><span data-ttu-id="4a602-103">Configuration du serveur de conversation permanente dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4a602-103">Configure Persistent Chat Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4a602-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4a602-104">

<span> </span></span></span>

<span data-ttu-id="4a602-105">_**Dernière modification de la rubrique :** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="4a602-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="4a602-106">Pour créer une nouvelle configuration de chat permanent</span><span class="sxs-lookup"><span data-stu-id="4a602-106">To create a new Persistent Chat configuration</span></span>

    New-CsPersistentChatConfiguration -Identity <XdsIdentity> [-DefaultChatHistory <Integer>] [-MaxChatContentSizeMB <Integer>] [-MaxFileSizeKB <Integer>] [-ParticipantUpdateLimit <Integer>] [-FileServiceUrl <UrlForFileUpload>] [-RoomManagementUrl <RoomManagementUrl>] [-Instance <PSObject>] [-Force <Switch Parameter>] [-Confirm <Switch Parameter>] [-WhatIf <Switch Parameter>]

<span data-ttu-id="4a602-107">Pour obtenir une configuration de conversation permanente</span><span class="sxs-lookup"><span data-stu-id="4a602-107">To get Persistent Chat configuration</span></span>

    Get-CsPersistentChatConfiguration [-LocalStore <Switch Parameter>] [-Identity <XdsIdentity>]

<span data-ttu-id="4a602-108">Pour supprimer une configuration de conversation permanente</span><span class="sxs-lookup"><span data-stu-id="4a602-108">To remove Persistent Chat configuration</span></span>

    Remove-CsPersistentChatConfiguration -Identity <XdsIdentity>

<span data-ttu-id="4a602-109">Pour définir la configuration de chat permanent</span><span class="sxs-lookup"><span data-stu-id="4a602-109">To set Persistent Chat configuration</span></span>

    Set-CsPersistentChatConfiguration [-DefaultChatHistory <Integer>] [-MaxChatContentSizeMB <Integer>] [-MaxFileSizeKB <Integer>] [-ParticipantUpdateLimit <Integer>] [-FileServiceUrl <UrlForFileUpload>] [-RoomManagementUrl <RoomManagementUrl>] [-Instance <PSObject >] [-Force <Switch Parameter>] [-Confirm <Switch Parameter>] [-WhatIf <Switch Parameter>]

<span data-ttu-id="4a602-110">Pour Lync Server 2013, tout le trafic de service Web est pris en charge sur les serveurs frontaux 2013 serveur Lync.</span><span class="sxs-lookup"><span data-stu-id="4a602-110">For Lync Server 2013, all web service traffic is supported on the Lync Server 2013, Front End Servers.</span></span> <span data-ttu-id="4a602-111">Par conséquent, l’adresse gcweb01 sur un serveur de chat permanent n’est pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="4a602-111">Therefore, the gcweb01 address on Persistent Chat Server is not necessary.</span></span> <span data-ttu-id="4a602-112">Nous sommes toujours en mesure de prendre en charge l’accès au service Web interne, car nous fournissons uniquement le service Web de chargement/téléchargement de fichiers sur le site Web *interne* (et non vers le site Web *externe* pour les utilisateurs distants).</span><span class="sxs-lookup"><span data-stu-id="4a602-112">We still support internal web service access because we provide the File Upload/Download Web service to the *internal* website only (not to the *external* website for remote users).</span></span>

<span data-ttu-id="4a602-113"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4a602-113"></div>

<span> </span>

</div>

</div>

</span></span></div>

