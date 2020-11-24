---
title: 'Lync Server 2013 : Vérification de la connectivité pour les utilisateurs externes'
description: 'Lync Server 2013 : vérifier la connectivité pour les utilisateurs externes.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Verify connectivity for external users
ms:assetid: 5c02bd6e-1c96-448a-a21d-58c9961c6640
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398402(v=OCS.15)
ms:contentKeyID: 48184249
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 50ef728157d01b93e7d0b8420442ce083a42b5b2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395045"
---
# <a name="verify-connectivity-for-external-users-in-lync-server-2013"></a><span data-ttu-id="e4e90-103">Vérification de la connectivité pour les utilisateurs externes dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e4e90-103">Verify connectivity for external users in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e4e90-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e4e90-104">

<span> </span></span></span>

<span data-ttu-id="e4e90-105">_**Dernière modification de la rubrique :** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="e4e90-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="e4e90-106">La validation de la connectivité des utilisateurs externes nécessite de garantir la connectivité des utilisateurs au serveur et au port du service Edge d’accès.</span><span class="sxs-lookup"><span data-stu-id="e4e90-106">Validating connectivity for external users requires ensuring connectivity from users to the server and port for the Access Edge service.</span></span>

<span data-ttu-id="e4e90-107">Pour confirmer votre configuration et la possibilité de vous connecter, d’envoyer et de recevoir les messages appropriés pour les scénarios requis par l’accès des utilisateurs externes est le site de l’analyseur de connectivité à distance ( <http://www.testocsconnectivity.com> ).</span><span class="sxs-lookup"><span data-stu-id="e4e90-107">A valuable resource for confirming your configuration and the ability to connect, send and receive the correct messages for the scenarios that external user access requires is the Remote Connectivity Analyzer site (<http://www.testocsconnectivity.com>).</span></span> <span data-ttu-id="e4e90-108">Le site est géré et entretenu par le support technique de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e4e90-108">The site is managed and maintained by Microsoft Support.</span></span> <span data-ttu-id="e4e90-109">Pour accéder à l’analyseur de connectivité à distance, ouvrez le site Web dans un navigateur et suivez les instructions pour sélectionner le scénario.</span><span class="sxs-lookup"><span data-stu-id="e4e90-109">To reach the Remote Connectivity Analyzer, open the Web site in a browser and follow the instructions to select the scenario.</span></span>

<div>

## <a name="test-connectivity-of-external-users-and-external-access"></a><span data-ttu-id="e4e90-110">Tester la connectivité des utilisateurs externes et des accès externes</span><span class="sxs-lookup"><span data-stu-id="e4e90-110">Test Connectivity of External Users and External access</span></span>

<span data-ttu-id="e4e90-111">Les tests pour l’accès utilisateur externe doivent inclure chaque type d’utilisateur externe pris en charge par votre organisation, y compris tout ou partie des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="e4e90-111">Tests for external user access should include each type of external user that your organization supports, including any or all of the following:</span></span>

  - <span data-ttu-id="e4e90-112">Utilisateurs d’au moins un domaine fédéré et test de la messagerie instantanée, de la présence, de A/V et du partage de bureau.</span><span class="sxs-lookup"><span data-stu-id="e4e90-112">Users from at least one federated domain, and test IM, presence, A/V and desktop sharing.</span></span>

  - <span data-ttu-id="e4e90-113">Utilisateurs de chaque fournisseur de services de messagerie instantanée publique pris en charge par votre organisation (et pour lesquels la mise en service est terminée).</span><span class="sxs-lookup"><span data-stu-id="e4e90-113">Users of each public IM service provider that your organization supports (and for which provisioning has been completed).</span></span>

  - <span data-ttu-id="e4e90-114">Utilisateurs anonymes.</span><span class="sxs-lookup"><span data-stu-id="e4e90-114">Anonymous users.</span></span>

  - <span data-ttu-id="e4e90-115">Les utilisateurs de votre organisation qui sont connectés à Lync à distance, mais qui ne l’utilisent pas.</span><span class="sxs-lookup"><span data-stu-id="e4e90-115">Users within your organization who are logged into Lync remotely, but not using VPN.</span></span>

<span data-ttu-id="e4e90-116">Ces tests déterminent si votre serveur Edge est :</span><span class="sxs-lookup"><span data-stu-id="e4e90-116">These tests determine whether your Edge Server is:</span></span>

  - <span data-ttu-id="e4e90-117">Écoute sur les ports requis à l’aide d’un client telnet depuis l’extérieur de votre réseau.</span><span class="sxs-lookup"><span data-stu-id="e4e90-117">Listening on the necessary ports by using a telnet client from outside your network.</span></span>
    
      - <span data-ttu-id="e4e90-118">Exemple : Telnet sip.contoso.com 443</span><span class="sxs-lookup"><span data-stu-id="e4e90-118">Example: telnet sip.contoso.com 443</span></span>
    
      - <span data-ttu-id="e4e90-119">Effectuez le test précédent sur les ports que vous utilisez sur le serveur Edge ou le pool de serveurs Edge en fonction de votre déploiement.</span><span class="sxs-lookup"><span data-stu-id="e4e90-119">Perform the preceding test on ports you are using on the Edge Server or Edge Server pool depending on your deployment.</span></span>

  - <span data-ttu-id="e4e90-120">Effectuer une résolution DNS externe précise.</span><span class="sxs-lookup"><span data-stu-id="e4e90-120">Performing accurate external DNS resolution.</span></span>
    
      - <span data-ttu-id="e4e90-121">Depuis l’extérieur de votre réseau, effectuez un test ping sur chacun des FQDN externes de votre pool Edge ou Edge.</span><span class="sxs-lookup"><span data-stu-id="e4e90-121">From outside your network ping each of the external FQDN’s of your Edge or Edge pool.</span></span> <span data-ttu-id="e4e90-122">Même si le test échoue, vous verrez les adresses IP, que vous pouvez comparer à celles que vous avez affectées.</span><span class="sxs-lookup"><span data-stu-id="e4e90-122">Even if the ping fails you will see the IP addresses, which you can compare to the ones you have assigned.</span></span>

<span data-ttu-id="e4e90-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e4e90-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

