---
title: 'Lync Server 2013 : désactivation de la contournement de média réseau'
description: 'Lync Server 2013 : désactivation de l’exclusion de médias réseau.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Disabling network media bypass
ms:assetid: 936d2678-d712-4589-b172-b5793013652f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688141(v=OCS.15)
ms:contentKeyID: 49733741
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1472711417218aa87936a3ccabe1bb465dd07c20
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429097"
---
# <a name="disabling-network-media-bypass-in-lync-server-2013"></a><span data-ttu-id="34a6f-103">Désactivation de la contournement de média réseau dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="34a6f-103">Disabling network media bypass in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="34a6f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="34a6f-104">

<span> </span></span></span>

<span data-ttu-id="34a6f-105">_**Dernière modification de la rubrique :** 2012-10-15_</span><span class="sxs-lookup"><span data-stu-id="34a6f-105">_**Topic Last Modified:** 2012-10-15_</span></span>

<span data-ttu-id="34a6f-106">Les paramètres de contournement de média s’appliquent globalement dans le déploiement de Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="34a6f-106">Media bypass settings apply globally across a Microsoft Lync Server 2013 deployment.</span></span> <span data-ttu-id="34a6f-107">Bypass Media accepte les appels pour ignorer le serveur de médiation.</span><span class="sxs-lookup"><span data-stu-id="34a6f-107">Media bypass allows calls to bypass the Mediation Server.</span></span> <span data-ttu-id="34a6f-108">Pour plus d’informations sur l’utilisation du contournement du contenu multimédia, voir [planification d’une dérivation multimédia dans Lync Server 2013](lync-server-2013-planning-for-media-bypass.md) dans la section planification. Vous pouvez désactiver la dérivation multimédia du panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="34a6f-108">For details about when to use Media bypass, see [Planning for media bypass in Lync Server 2013](lync-server-2013-planning-for-media-bypass.md) in the Planning section.You can disable media bypass from the Lync Server Control Panel.</span></span> <span data-ttu-id="34a6f-109">Pour plus d’informations sur l’activation et la configuration du contournement du son, voir [activation du contournement de média réseau dans Lync Server 2013](lync-server-2013-enabling-network-media-bypass.md)</span><span class="sxs-lookup"><span data-stu-id="34a6f-109">For details on enabling and configuring medial bypass, see [Enabling network media bypass in Lync Server 2013](lync-server-2013-enabling-network-media-bypass.md)</span></span>

<div>

## <a name="to-disable-media-bypass"></a><span data-ttu-id="34a6f-110">Pour désactiver la dérivation multimédia</span><span class="sxs-lookup"><span data-stu-id="34a6f-110">To disable media bypass</span></span>

1.  <span data-ttu-id="34a6f-111">À partir d’un compte d’utilisateur membre du groupe RTCUniversalServerAdmins (ou doté de droits d’utilisateur équivalents), ou affectées au rôle CsAdministrator, connectez-vous à n’importe quel ordinateur dans votre déploiement interne.</span><span class="sxs-lookup"><span data-stu-id="34a6f-111">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="34a6f-112">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="34a6f-112">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="34a6f-113">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="34a6f-113">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="34a6f-114">Dans la barre de navigation de gauche, cliquez sur **configuration du réseau** , puis sur **Global**.</span><span class="sxs-lookup"><span data-stu-id="34a6f-114">In the left navigation bar, click **Network Configuration** and then click **Global**.</span></span>

4.  <span data-ttu-id="34a6f-115">Dans la page **Global** , cliquez sur configuration **globale** .</span><span class="sxs-lookup"><span data-stu-id="34a6f-115">On the **Global** page, click the **Global** configuration.</span></span> <span data-ttu-id="34a6f-116">Il n’y a toujours qu’une seule configuration et elle est toujours nommée global.</span><span class="sxs-lookup"><span data-stu-id="34a6f-116">There is always only one configuration, and it is always named Global.</span></span>

5.  <span data-ttu-id="34a6f-117">Dans le menu **édition** , cliquez sur **afficher les détails**.</span><span class="sxs-lookup"><span data-stu-id="34a6f-117">On the **Edit** menu, click **View details**.</span></span>

6.  <span data-ttu-id="34a6f-118">Dans la page **modifier le paramètre global** , décochez la case **activer le contournement multimédia** .</span><span class="sxs-lookup"><span data-stu-id="34a6f-118">On the **Edit Global Setting** page, clear the **Enable media bypass** check box.</span></span>

7.  <span data-ttu-id="34a6f-119">Cliquez sur **valider** pour enregistrer vos modifications.</span><span class="sxs-lookup"><span data-stu-id="34a6f-119">Click **Commit** to save your changes.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="34a6f-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="34a6f-120">See Also</span></span>


[<span data-ttu-id="34a6f-121">Activation du contournement de média réseau dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="34a6f-121">Enabling network media bypass in Lync Server 2013</span></span>](lync-server-2013-enabling-network-media-bypass.md)  
  

<span data-ttu-id="34a6f-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="34a6f-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

