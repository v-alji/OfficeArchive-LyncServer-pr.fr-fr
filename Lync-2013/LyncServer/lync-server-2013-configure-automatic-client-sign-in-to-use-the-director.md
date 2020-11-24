---
title: >
  Lync Server 2013 : Configuration de la connexion automatique du client pour utiliser le directeur
description: 'Lync Server 2013 : configurer le client automatique Sign-In pour utiliser le directeur.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure Automatic Client Sign-In to use the Director
ms:assetid: 85369ffc-53ae-43be-8a23-84a094faecff
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398678(v=OCS.15)
ms:contentKeyID: 48184703
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b9c45a1a677d3a30704d8dca1771ef865cef29ec
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394940"
---
# <a name="configure-automatic-client-sign-in-to-use-the-director-in-lync-server-2013"></a><span data-ttu-id="40bab-103">Configuration de la connexion automatique du client pour utiliser le directeur dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="40bab-103">Configure Automatic Client Sign-In to use the Director in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="40bab-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="40bab-104">

<span> </span></span></span>

<span data-ttu-id="40bab-105">_**Dernière modification de la rubrique :** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="40bab-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="40bab-106">Lorsque vous déployez un serveur Lync Server 2013, un réalisateur ou un pool de directeurs, nous vous recommandons d’utiliser le client automatique Sign-In de la meilleure pratique.</span><span class="sxs-lookup"><span data-stu-id="40bab-106">When you deploy a Lync Server 2013, Director or a pool of Directors, we recommend that you use Automatic Client Sign-In as a best practice.</span></span> <span data-ttu-id="40bab-107">Pour plus d’informations sur la configuration des serveurs DNS pour la connexion automatique au client, voir [configuration DNS requise pour la connexion automatique au client dans Lync Server 2013](lync-server-2013-dns-requirements-for-automatic-client-sign-in.md) dans la documentation de planification.</span><span class="sxs-lookup"><span data-stu-id="40bab-107">For details about how to configure DNS servers for automatic client sign-in, see [DNS requirements for automatic client sign-in in Lync Server 2013](lync-server-2013-dns-requirements-for-automatic-client-sign-in.md) in the Planning documentation.</span></span>

<span data-ttu-id="40bab-108">Si vous avez déjà déployé la connexion automatique au client, consultez les sections suivantes pour le configurer sur votre ou vos directeurs.</span><span class="sxs-lookup"><span data-stu-id="40bab-108">If you have already deployed Automatic Client Sign-In, see the following sections to configure it on your Director(s).</span></span>

<div>

## <a name="single-director-instance"></a><span data-ttu-id="40bab-109">Instance de réalisateur unique</span><span class="sxs-lookup"><span data-stu-id="40bab-109">Single Director Instance</span></span>

<span data-ttu-id="40bab-110">Si vous disposez déjà d’un client automatique Sign-In déployé et qu’il pointe vers un serveur frontal ou un pool frontal, vous devez modifier l’enregistrement SRV DNS pour qu’il pointe vers le directeur.</span><span class="sxs-lookup"><span data-stu-id="40bab-110">If you already have Automatic Client Sign-In deployed and it is pointing to a Front End Server or a Front End pool, you need to change the DNS SRV record to point to the Director.</span></span>

</div>

<div>

## <a name="director-pool"></a><span data-ttu-id="40bab-111">Pool de réalisateurs</span><span class="sxs-lookup"><span data-stu-id="40bab-111">Director Pool</span></span>

<span data-ttu-id="40bab-112">Si vous disposez déjà d’un client automatique Sign-In déployé et qu’il pointe vers un serveur frontal ou un pool frontal, vous devez modifier l’enregistrement SRV DNS pour qu’il pointe vers le pool de Directors.</span><span class="sxs-lookup"><span data-stu-id="40bab-112">If you already have Automatic Client Sign-In deployed and it is pointing to a Front End Server or a Front End pool, you need to change the DNS SRV record to point to the Director pool.</span></span>

<span data-ttu-id="40bab-113"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="40bab-113"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

