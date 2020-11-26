---
title: Supprimer les paramètres de code confidentiel de conférence rendez-vous pour un site ou un groupe d’utilisateurs
description: Supprimer les paramètres de code confidentiel de conférence rendez-vous pour un site ou un groupe d’utilisateurs.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete dial-in conferencing PIN settings for a site or group of users
ms:assetid: 15a9faee-d024-4c0e-b2a0-fe7e7dc00589
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520955(v=OCS.15)
ms:contentKeyID: 48183498
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a40168780d5ac5f37ceb33dfaacd25b492d6307a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430475"
---
# <a name="delete-dial-in-conferencing-pin-settings-for-a-site-or-group-of-users-in-lync-server-2013"></a><span data-ttu-id="2734e-103">Supprimer les paramètres de code confidentiel de conférence rendez-vous pour un site ou un groupe d’utilisateurs dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2734e-103">Delete dial-in conferencing PIN settings for a site or group of users in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2734e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2734e-104">

<span> </span></span></span>

<span data-ttu-id="2734e-105">_**Dernière modification de la rubrique :** 2012-10-18_</span><span class="sxs-lookup"><span data-stu-id="2734e-105">_**Topic Last Modified:** 2012-10-18_</span></span>

<span data-ttu-id="2734e-106">Suivez ces étapes pour supprimer un utilisateur ou une stratégie de code secret de niveau site.</span><span class="sxs-lookup"><span data-stu-id="2734e-106">Follow these steps to delete a user-level or a site-level PIN policy.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="2734e-107">Vous ne pouvez pas supprimer la stratégie de code confidentiel globale.</span><span class="sxs-lookup"><span data-stu-id="2734e-107">You cannot delete the global PIN policy.</span></span>



</div>

<div>

## <a name="to-delete-a-user-or-site-pin-policy"></a><span data-ttu-id="2734e-108">Pour supprimer une stratégie de code confidentiel d’utilisateur ou de site</span><span class="sxs-lookup"><span data-stu-id="2734e-108">To delete a user or site PIN policy</span></span>

1.  <span data-ttu-id="2734e-109">À partir d’un compte d’utilisateur membre du groupe RTCUniversalServerAdmins (ou doté de droits d’utilisateur équivalents), ou affectées au rôle CsServerAdministrator ou CsAdministrator, connectez-vous à n’importe quel ordinateur se trouve sur le réseau sur lequel vous avez déployé Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="2734e-109">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or assigned to the CsServerAdministrator or CsAdministrator role, log on to any computer that is in the network in which you deployed Lync Server 2013.</span></span>

2.  <span data-ttu-id="2734e-110">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="2734e-110">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="2734e-111">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="2734e-111">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="2734e-112">Dans la barre de navigation de gauche, cliquez sur **Conférence**, puis sur **Stratégie de code confidentiel**.</span><span class="sxs-lookup"><span data-stu-id="2734e-112">In the left navigation bar, click **Conferencing**, and then click **PIN Policy**.</span></span>

4.  <span data-ttu-id="2734e-113">Dans la page de **stratégie de code confidentiel** , dans le champ de recherche, tapez tout ou partie du nom de la stratégie que vous voulez supprimer.</span><span class="sxs-lookup"><span data-stu-id="2734e-113">On the **PIN Policy** page, in the search field, type all or part of the name of the policy you want to delete.</span></span>

5.  <span data-ttu-id="2734e-114">Dans la liste des stratégies, cliquez sur la stratégie à supprimer, sur **Modifier**, puis sur **Supprimer**.</span><span class="sxs-lookup"><span data-stu-id="2734e-114">In the list of policies, click the policy that you want, click **Edit**, and then click **Delete**.</span></span>

6.  <span data-ttu-id="2734e-115">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="2734e-115">Click **OK**.</span></span>

<span data-ttu-id="2734e-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2734e-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

