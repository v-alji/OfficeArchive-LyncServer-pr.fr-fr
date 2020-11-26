---
title: 'Lync Server 2013 : protection des données en transit : bases de données de serveur d’archivage, de surveillance, de conformité de conversation de groupe'
description: 'Lync Server 2013 : protection des données lors du transfert : archivage, surveillance, bases de données serveur de conformité des discussions de groupe.'
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
manager: serdars
audience: admin
f1.keywords:
- NOCSH
TOCTitle: Protecting data in transit – archiving, monitoring, group chat compliance server databases in Lync Server 2013
ms:assetid: ea219705-1015-43a7-890b-e7e67b451e7c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn518336(v=OCS.15)
ms:contentKeyID: 62625494
ms.date: 07/23/2014
mtps_version: v=OCS.15
ms.openlocfilehash: d4d4127bb0404bca376da450d0b0c58cf3b76560
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436845"
---
# <a name="protecting-data-in-transit--archiving-monitoring-group-chat-compliance-server-databases-in-lync-server-2013"></a><span data-ttu-id="ea00c-103">Protection des données en transit : bases de données de serveur d’archivage, de surveillance, de conformité de conversation de groupe dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ea00c-103">Protecting data in transit – archiving, monitoring, group chat compliance server databases in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ea00c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ea00c-104">

<span> </span></span></span>

<span data-ttu-id="ea00c-105">_**Dernière modification de la rubrique :** 2013-12-05_</span><span class="sxs-lookup"><span data-stu-id="ea00c-105">_**Topic Last Modified:** 2013-12-05_</span></span>

<span data-ttu-id="ea00c-106">Serveur d’archivage Microsoft Lync Server 2013 et analyse serveur Utilisez le service Message Queuing (également appelé MSMQ) pour collecter et déplacer de manière fiable des messages de données du point de collection vers les serveurs de référentiel.</span><span class="sxs-lookup"><span data-stu-id="ea00c-106">Microsoft Lync Server 2013 Archiving Server and Monitoring Server both use the Message Queuing (also known as MSMQ) service to collect and reliably move data messages from the collection point to the repository servers.</span></span> <span data-ttu-id="ea00c-107">Le service de conformité recueille des données conjointement avec le serveur de discussion de groupe, qui utilise également Message Queuing.</span><span class="sxs-lookup"><span data-stu-id="ea00c-107">Compliance service collects data in conjunction with the Group Chat Server, which also uses Message Queuing.</span></span>

<span data-ttu-id="ea00c-108">Dans Lync Server 2013, il n’existe aucune protection interne pour les données sur le réseau. Toutefois, s’il est nécessaire de sécuriser ce trafic, le service de messagerie électronique peut fournir un chiffrement à un niveau de message sur la file d’attente d’envoi de messages.</span><span class="sxs-lookup"><span data-stu-id="ea00c-108">In Lync Server 2013, there is no internal protection for data on the wire; however, if there is a requirement to secure this traffic, the Message Queuing service can provide encryption at a message level on the sending message queue.</span></span> <span data-ttu-id="ea00c-109">Pour cela, il est possible d’utiliser des certificats gérés par les services de domaine Active Directory (AD FS).</span><span class="sxs-lookup"><span data-stu-id="ea00c-109">This is accomplished using certificates that are managed by the Active Directory Domain Services.</span></span> <span data-ttu-id="ea00c-110">Pour plus d’informations, reportez-vous à l’annexe D : Message Queuing et communication Internet dans Windows Server 2008 à [https://go.microsoft.com/fwlink/p/?LinkId=145238](https://go.microsoft.com/fwlink/p/?linkid=145238) l’adresse ou à l’annexe I : Message Queuing et communication Internet dans Windows server 2008 R2 sur [https://go.microsoft.com/fwlink/p/?LinkId=211883](https://go.microsoft.com/fwlink/p/?linkid=211883) windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="ea00c-110">For details, see Appendix D: Message Queuing and Internet Communication in Windows Server 2008 at [https://go.microsoft.com/fwlink/p/?LinkId=145238](https://go.microsoft.com/fwlink/p/?linkid=145238) or Appendix I: Message Queuing and Internet Communication in Windows Server 2008 R2 at [https://go.microsoft.com/fwlink/p/?LinkId=211883](https://go.microsoft.com/fwlink/p/?linkid=211883) for Windows Server 2008 R2.</span></span>

<span data-ttu-id="ea00c-111"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ea00c-111"></div>

<span> </span>

</div>

</div>

</span></span></div>

