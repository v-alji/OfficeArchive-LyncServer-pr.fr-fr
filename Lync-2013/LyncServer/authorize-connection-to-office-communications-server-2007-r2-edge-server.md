---
title: Autoriser la connexion à un serveur Edge Office Communications Server 2007 R2
description: Autorisez la connexion à un serveur Edge Office Communications Server 2007 R2.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Authorize connection to Office Communications Server 2007 R2 Edge Server
ms:assetid: 14f6798a-28d6-4b3d-8734-942192e1bbf5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204702(v=OCS.15)
ms:contentKeyID: 48183493
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: de8dadb2c476c892f4ffd548ce176d12d3b1a1cf
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394260"
---
# <a name="authorize-connection-to-office-communications-server-2007-r2-edge-server"></a><span data-ttu-id="36f0f-103">Autoriser la connexion à un serveur Edge Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="36f0f-103">Authorize connection to Office Communications Server 2007 R2 Edge Server</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="36f0f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="36f0f-104">

<span> </span></span></span>

<span data-ttu-id="36f0f-105">_**Dernière modification de la rubrique :** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="36f0f-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="36f0f-106">Pour chaque serveur principal Lync Server 2013 ou Standard Edition Server dans votre pool de pilotes, vous devez mettre à jour la liste des serveurs internes autorisés à se connecter au serveur Edge Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="36f0f-106">For each Lync Server 2013 Front End Server or Standard Edition server in your pilot pool, you must update the list of internal servers that are authorized to connect to the Office Communications Server 2007 R2 Edge Server.</span></span> <span data-ttu-id="36f0f-107">Sans ces mises à jour, les conférences audio/vidéo externes (A/V) pour les utilisateurs qui rejoignent l’utilisation du serveur Edge hérité ne fonctionneront pas.</span><span class="sxs-lookup"><span data-stu-id="36f0f-107">Without these updates, external audio/visual (A/V) conferencing for users joining by using the legacy Edge Server will not work.</span></span>

<div>

## <a name="to-authorize-connection-to-office-communications-server-2007-r2-edge-server"></a><span data-ttu-id="36f0f-108">Pour autoriser la connexion à un serveur Edge Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="36f0f-108">To Authorize Connection to Office Communications Server 2007 R2 Edge Server</span></span>

1.  <span data-ttu-id="36f0f-109">À partir du serveur Office Communications Server 2007 R2 Edge, accédez au groupe **Outils d’administration** , puis ouvrez le composant logiciel enfichable Gestion de l' **ordinateur** .</span><span class="sxs-lookup"><span data-stu-id="36f0f-109">From the Office Communications Server 2007 R2 Edge Server, from the **Administrative Tools** group, open the **Computer Management** snap-in.</span></span>

2.  <span data-ttu-id="36f0f-110">Dans l’arborescence de la console, développez **services et applications**.</span><span class="sxs-lookup"><span data-stu-id="36f0f-110">In the console tree, expand **Services and Applications**.</span></span>

3.  <span data-ttu-id="36f0f-111">Cliquez avec le bouton droit sur **Office Communications Server 2007 R2**, puis cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="36f0f-111">Right-click **Office Communications Server 2007 R2**, and then click **Properties**.</span></span>

4.  <span data-ttu-id="36f0f-112">Cliquez sur l’onglet **interne** .</span><span class="sxs-lookup"><span data-stu-id="36f0f-112">Click the **Internal** tab.</span></span>

5.  <span data-ttu-id="36f0f-113">Sous **Ajouter un serveur**, cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="36f0f-113">Under **Add Server**, click **Add**.</span></span>

6.  <span data-ttu-id="36f0f-114">Dans la boîte de dialogue **Ajouter un serveur Office Communications Server** , entrez les informations appropriées :</span><span class="sxs-lookup"><span data-stu-id="36f0f-114">In the **Add Office Communications Server** dialog box, enter the appropriate information:</span></span>
    
      - <span data-ttu-id="36f0f-115">Spécifiez le nom de domaine complet (FQDN) de chaque serveur frontal Lync Server 2013 ou Standard Edition Server et de Lync Server 2013 pool.</span><span class="sxs-lookup"><span data-stu-id="36f0f-115">Specify the fully qualified domain name (FQDN) of each Lync Server 2013 Front End Server or Standard Edition server, and Lync Server 2013 pool.</span></span>
    
      - <span data-ttu-id="36f0f-116">Spécifiez le nom de domaine complet (FQDN) du réalisateur Lync Server 2013 si vous avez configuré un itinéraire statique sur le pool qui spécifie l’ordinateur tronçon suivant par son nom de domaine complet.</span><span class="sxs-lookup"><span data-stu-id="36f0f-116">Specify the FQDN of the Lync Server 2013 Director if you configured a static route on the pool that specifies the next hop computer by its FQDN.</span></span>

7.  <span data-ttu-id="36f0f-117">Après avoir ajouté une entrée pour chaque serveur Lync Server 2013, serveur frontal, serveur Standard Edition, pool et directeur, cliquez sur **appliquer** , puis sur **OK** pour fermer la page Propriétés.</span><span class="sxs-lookup"><span data-stu-id="36f0f-117">After you have added an entry for each Lync Server 2013, Front End Server, Standard Edition server, pool, and Director, click **Apply** and then click **OK** to close the Properties page.</span></span>

<span data-ttu-id="36f0f-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="36f0f-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

