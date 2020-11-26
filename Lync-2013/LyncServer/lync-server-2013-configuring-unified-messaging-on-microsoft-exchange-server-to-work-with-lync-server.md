---
title: 'Lync Server 2013 : Configuration de la messagerie unifiée sur Microsoft Exchange Server de sorte qu’elle fonctionne avec Lync Server'
description: 'Lync Server 2013 : configuration de la messagerie unifiée sur Microsoft Exchange Server pour qu’elle fonctionne avec Lync Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Unified Messaging on Microsoft Exchange Server to work with Lync Server 2013
ms:assetid: 058da9c4-23af-4ddb-9f63-70133a8aafc6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398106(v=OCS.15)
ms:contentKeyID: 48183289
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 53c303f0ae659536aafcbdfcd829ed236e35a0ba
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432428"
---
# <a name="configuring-unified-messaging-on-microsoft-exchange-server-to-work-with-lync-server-2013"></a><span data-ttu-id="6a7b3-103">Configuration de la messagerie unifiée sur Microsoft Exchange Server de sorte qu’elle fonctionne avec Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6a7b3-103">Configuring Unified Messaging on Microsoft Exchange Server to work with Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6a7b3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6a7b3-104">

<span> </span></span></span>

<span data-ttu-id="6a7b3-105">_**Dernière modification de la rubrique :** 2012-10-11_</span><span class="sxs-lookup"><span data-stu-id="6a7b3-105">_**Topic Last Modified:** 2012-10-11_</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="6a7b3-106">Si vous souhaitez utiliser la messagerie unifiée Exchange pour fournir des services de réponse d’appel, Outlook Voice Access ou de standard automatique pour les utilisateurs voix entreprise, consultez la rubrique <A href="lync-server-2013-planning-for-exchange-unified-messaging-integration.md">planification de l’intégration de la messagerie unifiée Exchange dans Lync Server 2013</A> dans la documentation de planification, puis suivez les instructions de cette section.</span><span class="sxs-lookup"><span data-stu-id="6a7b3-106">If you want to use Exchange Unified Messaging (UM) to provide call answering, Outlook Voice Access, or auto-attendant services for Enterprise Voice users, read <A href="lync-server-2013-planning-for-exchange-unified-messaging-integration.md">Planning for Exchange Unified Messaging integration in Lync Server 2013</A> in the Planning documentation, and then follow the instructions in this section.</span></span>



</div>

<span data-ttu-id="6a7b3-107">Pour configurer la messagerie unifiée (MU) Exchange pour qu’elle fonctionne avec la voix entreprise, vous devez effectuer les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="6a7b3-107">To configure Exchange Unified Messaging (UM) to work with Enterprise Voice, you’ll need to perform the following tasks:</span></span>

  - <span data-ttu-id="6a7b3-108">Configurer des certificats sur le serveur exécutant les services de messagerie unifiée Exchange</span><span class="sxs-lookup"><span data-stu-id="6a7b3-108">Configure certificates on the server running Exchange Unified Messaging (UM) services</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="6a7b3-109">Ajoutez tous les serveurs d’accès client et de boîte aux lettres à toutes les offres de numérotation URI SIP UM.</span><span class="sxs-lookup"><span data-stu-id="6a7b3-109">Add all Client Access and Mailbox servers to all UM SIP URI dial plans.</span></span> <span data-ttu-id="6a7b3-110">Si ce n’est pas le cas, le routage des appels sortants ne fonctionne pas comme prévu.</span><span class="sxs-lookup"><span data-stu-id="6a7b3-110">If not, outbound call routing won’t work as expected.</span></span>

    
    </div>

  - <span data-ttu-id="6a7b3-111">Créez un ou plusieurs plans de numérotation URI SIP UM, ainsi que les numéros de téléphone d’accès d’abonné, le cas échéant, puis créez les plans de numérotation de serveur Lync correspondants.</span><span class="sxs-lookup"><span data-stu-id="6a7b3-111">Create one or more UM SIP URI dial plans, along with the subscriber access phone numbers, as needed, and then create corresponding Lync Server dial plans.</span></span>

  - <span data-ttu-id="6a7b3-112">Utilisez le script de **exchucutil.ps1** pour :</span><span class="sxs-lookup"><span data-stu-id="6a7b3-112">Use the **exchucutil.ps1** script to:</span></span>
    
      - <span data-ttu-id="6a7b3-113">Créer des passerelles IP de messagerie unifiée.</span><span class="sxs-lookup"><span data-stu-id="6a7b3-113">Create UM IP gateways.</span></span>
    
      - <span data-ttu-id="6a7b3-114">Créer des groupes de recherche de MU.</span><span class="sxs-lookup"><span data-stu-id="6a7b3-114">Create UM hunt groups.</span></span>
    
      - <span data-ttu-id="6a7b3-115">Accordez l’autorisation Lync Server 2013 pour lire les objets services de domaine Active Directory de messagerie unifiée.</span><span class="sxs-lookup"><span data-stu-id="6a7b3-115">Grant Lync Server 2013 permission to read UM Active Directory Domain Services objects.</span></span>

  - <span data-ttu-id="6a7b3-116">Créer un objet de standard automatique de messagerie unifiée.</span><span class="sxs-lookup"><span data-stu-id="6a7b3-116">Create a UM auto-attendant object.</span></span>

  - <span data-ttu-id="6a7b3-117">Créer un objet d’accès abonné.</span><span class="sxs-lookup"><span data-stu-id="6a7b3-117">Create a subscriber access object.</span></span>

  - <span data-ttu-id="6a7b3-118">Créer un URI SIP pour chaque utilisateur et en associant les utilisateurs à l’aide d’un plan de numérotation URI SIP UM.</span><span class="sxs-lookup"><span data-stu-id="6a7b3-118">Create a SIP URI for each user and associating users with a UM SIP URI dial plan.</span></span>

<div>

## <a name="requirements-and-recommendations"></a><span data-ttu-id="6a7b3-119">Conditions requises et recommandations</span><span class="sxs-lookup"><span data-stu-id="6a7b3-119">Requirements and Recommendations</span></span>

<span data-ttu-id="6a7b3-120">Avant de commencer, la documentation de cette section suppose que vous avez déployé les rôles Exchange 2013 suivants : accès client et boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="6a7b3-120">Before you begin, the documentation in this section assumes that you have deployed the following Exchange 2013 roles: Client Access and Mailbox.</span></span> <span data-ttu-id="6a7b3-121">Dans Microsoft Exchange Server 2013, la messagerie unifiée Exchange s’exécute en tant que service sur ces serveurs.</span><span class="sxs-lookup"><span data-stu-id="6a7b3-121">In Microsoft Exchange Server 2013, Exchange UM runs as a service on these servers.</span></span>

<span data-ttu-id="6a7b3-122">Pour plus d’informations sur le déploiement d’Exchange 2013, voir la bibliothèque TechNet Exchange 2013 sur [https://go.microsoft.com/fwlink/p/?LinkId=266637](https://go.microsoft.com/fwlink/p/?linkid=266637)</span><span class="sxs-lookup"><span data-stu-id="6a7b3-122">For details about deploying Exchange 2013, see the Exchange 2013 TechNet Library at [https://go.microsoft.com/fwlink/p/?LinkId=266637](https://go.microsoft.com/fwlink/p/?linkid=266637)</span></span>

<span data-ttu-id="6a7b3-123">Notez également ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="6a7b3-123">Also note the following:</span></span>

  - <span data-ttu-id="6a7b3-124">Si Exchange UM est installé dans plusieurs forêts, vous devez effectuer les étapes d’intégration d’Exchange Server pour chaque forêt de messagerie unifiée.</span><span class="sxs-lookup"><span data-stu-id="6a7b3-124">If Exchange UM is installed in multiple forests, the Exchange Server integration steps must be performed for each UM forest.</span></span> <span data-ttu-id="6a7b3-125">De plus, chaque forêt de messagerie unifiée doit être configurée pour approuver la forêt dans laquelle Lync Server 2013 est déployé et la forêt dans laquelle Lync Server 2013 est déployée doit être configurée pour approuver chaque forêt de messagerie unifiée.</span><span class="sxs-lookup"><span data-stu-id="6a7b3-125">In addition, each UM forest must be configured to trust the forest in which Lync Server 2013 is deployed, and the forest in which Lync Server 2013 is deployed must be configured to trust each UM forest.</span></span>

  - <span data-ttu-id="6a7b3-126">Des étapes d’intégration sont effectuées à la fois sur les rôles de serveur Exchange et sur le serveur exécutant Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6a7b3-126">Integration steps are performed on both the Exchange Server roles where Unified Messaging services are running, and on the server running Lync Server 2013.</span></span> <span data-ttu-id="6a7b3-127">Vous devez effectuer les étapes d’intégration de la messagerie unifiée Exchange Server avant d’effectuer les étapes d’intégration de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6a7b3-127">You should perform the Exchange Server Unified Messaging integration steps before you perform the Lync Server 2013 integration steps.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="6a7b3-128">Pour savoir quelles étapes d’intégration sont exécutées sur les serveurs et quels rôles d’administrateur, voir <A href="lync-server-2013-deployment-process-for-integrating-on-premises-unified-messaging.md">processus de déploiement pour l’intégration de la messagerie unifiée locale et de Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="6a7b3-128">To see which integration steps are performed on which servers and by which administrator roles, see <A href="lync-server-2013-deployment-process-for-integrating-on-premises-unified-messaging.md">Deployment process for integrating on-premises Unified Messaging and Lync Server 2013</A>.</span></span>

    
    </div>

<span data-ttu-id="6a7b3-129">Les outils suivants doivent être disponibles sur chaque serveur exécutant la messagerie unifiée Exchange :</span><span class="sxs-lookup"><span data-stu-id="6a7b3-129">The following tools must be available on each server running Exchange UM:</span></span>

  - <span data-ttu-id="6a7b3-130">Exchange Management Shell</span><span class="sxs-lookup"><span data-stu-id="6a7b3-130">Exchange Management Shell</span></span>

  - <span data-ttu-id="6a7b3-131">Le script **exchucutil.ps1**, qui effectue les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="6a7b3-131">The script **exchucutil.ps1**, which performs the following tasks:</span></span>
    
      - <span data-ttu-id="6a7b3-132">Crée une passerelle IP de MU pour chaque serveur Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6a7b3-132">Creates a UM IP gateway for each Lync Server 2013.</span></span>
    
      - <span data-ttu-id="6a7b3-133">Crée un groupe de recherche pour chaque passerelle.</span><span class="sxs-lookup"><span data-stu-id="6a7b3-133">Creates a hunt group for each gateway.</span></span> <span data-ttu-id="6a7b3-134">L’identificateur pilote de chaque groupe de recherche spécifie le plan de numérotation d’URI SIP de MU utilisé par le pool frontal ou le serveur Standard Edition associé à la passerelle.</span><span class="sxs-lookup"><span data-stu-id="6a7b3-134">The pilot identifier of each hunt group specifies the UM SIP URI dial plan used by the Front End pool or Standard Edition server that is associated with the gateway.</span></span>
    
      - <span data-ttu-id="6a7b3-135">Octroie à Lync Server 2013 une autorisation de lecture d’objets de messagerie unifiée Exchange dans les services de domaine Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6a7b3-135">Grants Lync Server 2013 permission to read Exchange UM objects in Active Directory Domain Services.</span></span>

</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="6a7b3-136">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="6a7b3-136">In This Section</span></span>

  - [<span data-ttu-id="6a7b3-137">Configurer des certificats sur le serveur exécutant la messagerie unifiée Microsoft Exchange Server</span><span class="sxs-lookup"><span data-stu-id="6a7b3-137">Configure certificates on the server running Microsoft Exchange Server Unified Messaging</span></span>](lync-server-2013-configure-certificates-on-the-server-running-microsoft-exchange-server-unified-messaging.md)

  - [<span data-ttu-id="6a7b3-138">Configurer la messagerie unifiée sur Microsoft Exchange pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6a7b3-138">Configure Unified Messaging on Microsoft Exchange for Lync Server 2013</span></span>](lync-server-2013-configure-unified-messaging-on-microsoft-exchange.md)

<span data-ttu-id="6a7b3-139"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6a7b3-139"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

