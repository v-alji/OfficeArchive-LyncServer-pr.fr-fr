---
title: Configuration des enregistrements DNS pour le déploiement d’un pool pilote
description: Configurer les enregistrements DNS pour le déploiement du pool de pilotes.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Configure DNS records for pilot pool deployment
ms:assetid: eb421bad-4bf1-4837-a077-7795094692d9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721921(v=OCS.15)
ms:contentKeyID: 49733855
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1e41e163432ba910f6d083cc508e8ad8c9f2006d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394441"
---
# <a name="configure-dns-records-for-pilot-pool-deployment"></a><span data-ttu-id="501eb-103">Configuration des enregistrements DNS pour le déploiement d’un pool pilote</span><span class="sxs-lookup"><span data-stu-id="501eb-103">Configure DNS records for pilot pool deployment</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="501eb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="501eb-104">

<span> </span></span></span>

<span data-ttu-id="501eb-105">_**Dernière modification de la rubrique :** 2012-09-29_</span><span class="sxs-lookup"><span data-stu-id="501eb-105">_**Topic Last Modified:** 2012-09-29_</span></span>

<span data-ttu-id="501eb-106">Avant de déployer le pool de pilotes de Lync Server 2013, vous devez mettre à jour les entrées de l’hôte DNS pour le pool de pilotes.</span><span class="sxs-lookup"><span data-stu-id="501eb-106">Prior to deploying the Lync Server 2013 pilot pool, you must update the DNS Host A entries for the pilot pool.</span></span> <span data-ttu-id="501eb-107">Pour effectuer cette procédure, vous devez être connecté au serveur ou au domaine en tant que membre du groupe Domain Admins ou membre du groupe DnsAdmins.</span><span class="sxs-lookup"><span data-stu-id="501eb-107">To successfully complete this procedure, you should be logged on to the server or domain as a member of the Domain Admins group or a member of the DnsAdmins group.</span></span>

<span data-ttu-id="501eb-108">**Pour configurer les enregistrements d’un hôte DNS**</span><span class="sxs-lookup"><span data-stu-id="501eb-108">**To configure DNS Host A records**</span></span>

1.  <span data-ttu-id="501eb-109">Sur le serveur DNS (Domain Name System), cliquez sur **Démarrer**, sur **Outils d’administration**, puis sur **DNS**.</span><span class="sxs-lookup"><span data-stu-id="501eb-109">On the Domain Name System (DNS) server, click **Start**, click **Administrative Tools**, and then click **DNS**.</span></span>

2.  <span data-ttu-id="501eb-110">Dans l’arborescence de la console pour votre domaine, développez **zones de recherche directe**, puis cliquez avec le bouton droit sur le domaine dans lequel Lync Server 2013 sera installé.</span><span class="sxs-lookup"><span data-stu-id="501eb-110">In the console tree for your domain, expand **Forward Lookup Zones**, and then right-click the domain in which Lync Server 2013 will be installed.</span></span>

3.  <span data-ttu-id="501eb-111">Cliquez sur **nouvel hôte (A ou AAAA)**.</span><span class="sxs-lookup"><span data-stu-id="501eb-111">Click **New Host (A or AAAA)**.</span></span>

4.  <span data-ttu-id="501eb-112">Cliquez sur **nom**, tapez le nom d’hôte du pool Lync Server 2013 (le nom de domaine est censé partir de la zone dans laquelle l’enregistrement est défini et qu’il n’est pas nécessaire d’entrer dans le cadre de l’enregistrement a).</span><span class="sxs-lookup"><span data-stu-id="501eb-112">Click **Name**, type the host name for the Lync Server 2013 pool (the domain name is assumed from the zone that the record is defined in and does not need to be entered as part of the A record).</span></span>

5.  <span data-ttu-id="501eb-113">Cliquez sur **adresse IP**, tapez l’adresse IP de la liste frontale.</span><span class="sxs-lookup"><span data-stu-id="501eb-113">Click **IP Address**, type the IP address for the Front End pool.</span></span>

6.  <span data-ttu-id="501eb-114">Cliquez sur **Ajouter un hôte**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="501eb-114">Click **Add Host**, and then click **OK**.</span></span>

7.  <span data-ttu-id="501eb-115">Lorsque vous avez terminé, cliquez sur **terminé**.</span><span class="sxs-lookup"><span data-stu-id="501eb-115">When you are finished, click **Done**.</span></span>

<span data-ttu-id="501eb-116"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="501eb-116"></div>

<span> </span>

</div>

</div>

</span></span></div>

