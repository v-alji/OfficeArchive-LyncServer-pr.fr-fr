---
title: 'Lync Server 2013 : afficher une liste des applications approuvées'
description: 'Lync Server 2013 : afficher une liste des applications approuvées.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: View a list of trusted applications
ms:assetid: f09300b3-67cf-4e70-a51a-23d62479b913
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182604(v=OCS.15)
ms:contentKeyID: 48185844
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 01d45c682550640c3fc7284e0b60ca6844896b5d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444111"
---
# <a name="view-a-list-of-trusted-applications-in-lync-server-2013"></a><span data-ttu-id="8fc11-103">Afficher une liste des applications approuvées dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8fc11-103">View a list of trusted applications in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8fc11-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8fc11-104">

<span> </span></span></span>

<span data-ttu-id="8fc11-105">_**Dernière modification de la rubrique :** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="8fc11-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="8fc11-106">Vous pouvez utiliser le panneau de configuration de Lync Server 2013 pour afficher la liste des applications approuvées que vous avez déployées dans votre environnement Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="8fc11-106">You can use Lync Server 2013 Control Panel to view a list of the trusted applications that you have deployed in your Lync Server 2013 environment.</span></span> <span data-ttu-id="8fc11-107">Une application fiable est une application basée sur le kit de développement logiciel (Unified Communications Managed API UCMA) 3,0 principal du SDK approuvé par Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="8fc11-107">A trusted application is an application based on Microsoft Unified Communications Managed API (UCMA) 3.0 Core SDK that is trusted by Lync Server 2013.</span></span> <span data-ttu-id="8fc11-108">Cette relation d’approbation est résumée dans la liste suivante :</span><span class="sxs-lookup"><span data-stu-id="8fc11-108">This trust relationship is summarized in the following list:</span></span>

  - <span data-ttu-id="8fc11-109">Les applications approuvées ne sont pas confrontées à l’authentification par Lync Server.</span><span class="sxs-lookup"><span data-stu-id="8fc11-109">Trusted applications are not challenged for authentication by Lync Server.</span></span>

  - <span data-ttu-id="8fc11-110">Les applications approuvées ne sont pas limitées par Lync Server pour les transactions SIP, les connexions ou les appels voix sur IP sortants.</span><span class="sxs-lookup"><span data-stu-id="8fc11-110">Trusted applications are not throttled by Lync Server for SIP transactions, connections or outgoing Voice over Internet Protocol (VoIP) calls.</span></span>

  - <span data-ttu-id="8fc11-111">Les applications approuvées peuvent emprunter l’identité d’un utilisateur et participer à des conférences sans apparaître dans les listes.</span><span class="sxs-lookup"><span data-stu-id="8fc11-111">Trusted applications can impersonate any user and can join conferences without appearing in rosters.</span></span>

  - <span data-ttu-id="8fc11-112">Les applications approuvées sont hautement disponibles et résilientes.</span><span class="sxs-lookup"><span data-stu-id="8fc11-112">Trusted applications are highly available and resilient.</span></span>

<span data-ttu-id="8fc11-113">Dans le panneau de configuration de Lync Server, vous pouvez voir le nom de l’application, le pool sur lequel elle s’exécute et le port utilisé.</span><span class="sxs-lookup"><span data-stu-id="8fc11-113">In Lync Server Control Panel, you can see the name of the applications, the pool where they run, and the port they use.</span></span>

<div>

## <a name="to-view-a-list-of-trusted-applications"></a><span data-ttu-id="8fc11-114">Pour afficher une liste des applications approuvées</span><span class="sxs-lookup"><span data-stu-id="8fc11-114">To view a list of trusted applications</span></span>

1.  <span data-ttu-id="8fc11-115">À partir d’un compte d’utilisateur affecté au CsServerAdministrator, CsAdministrator, CsHelpDesk ou CsViewOnlyAdministrator, ouvrez une session sur n’importe quel ordinateur dans votre déploiement interne.</span><span class="sxs-lookup"><span data-stu-id="8fc11-115">From a user account that is assigned to the CsServerAdministrator, CsAdministrator, CsHelpDesk, or CsViewOnlyAdministrator role, log on to any computer in your internal deployment.</span></span> <span data-ttu-id="8fc11-116">Pour plus d’informations sur les rôles d’administration prédéfinis disponibles dans Lync Server 2013, voir [planification du contrôle d’accès basé sur les rôles dans Lync server 2013](lync-server-2013-planning-for-role-based-access-control.md).</span><span class="sxs-lookup"><span data-stu-id="8fc11-116">For details about the predefined administrative roles available in Lync Server 2013, see [Planning for role-based access control in Lync Server 2013](lync-server-2013-planning-for-role-based-access-control.md).</span></span>

2.  <span data-ttu-id="8fc11-117">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="8fc11-117">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="8fc11-118">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="8fc11-118">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="8fc11-119">Dans la barre de navigation de gauche, cliquez sur **Topology** et sur **application de confiance**.</span><span class="sxs-lookup"><span data-stu-id="8fc11-119">In the left navigation bar, click **Topology** and the click **Trusted Application**.</span></span>

4.  <span data-ttu-id="8fc11-120">Dans la page **application fiable** , cliquez sur un en-tête de colonne pour trier les applications si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="8fc11-120">On the **Trusted Application** page, click a column heading to sort the applications, if needed.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="8fc11-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8fc11-121">See Also</span></span>


[<span data-ttu-id="8fc11-122">Gestion de la topologie Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8fc11-122">Managing the Lync Server 2013 topology</span></span>](lync-server-2013-managing-the-lync-server-topology.md)  
  

<span data-ttu-id="8fc11-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8fc11-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

