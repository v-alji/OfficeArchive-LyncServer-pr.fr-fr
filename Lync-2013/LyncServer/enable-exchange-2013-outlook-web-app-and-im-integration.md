---
title: Activation d’Outlook Web App et de l’intégration de la messagerie instantanée dans Exchange 2013
description: Activez 2013 Exchange Web App et l’intégration de la messagerie instantanée dans Outlook Web App.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enable Exchange 2013 Outlook Web App and IM integration
ms:assetid: 44d08cf0-b17d-46e1-a4f0-fcc2fe96a958
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204857(v=OCS.15)
ms:contentKeyID: 48184027
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a7fd6e8600f255d6ac4dde52487776cdb5fe1a51
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394028"
---
# <a name="enable-exchange-2013-outlook-web-app-and-im-integration"></a><span data-ttu-id="66c98-103">Activation d’Outlook Web App et de l’intégration de la messagerie instantanée dans Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="66c98-103">Enable Exchange 2013 Outlook Web App and IM integration</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="66c98-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="66c98-104">

<span> </span></span></span>

<span data-ttu-id="66c98-105">_**Dernière modification de la rubrique :** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="66c98-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="66c98-106">Pour activer l’intégration de la messagerie instantanée et de l’intégration de la messagerie instantanée Exchange 2013 à Lync Server 2013, vous devez ajouter le serveur de serveur d’accès au client Exchange 2013 à la topologie Lync Server 2013 comme serveur d’applications de confiance.</span><span class="sxs-lookup"><span data-stu-id="66c98-106">To enable Exchange 2013 Outlook Web Access (OWA) and instant messaging (IM) integration with Lync Server 2013, you must add the Exchange 2013 Client Access Server (CAS) server to the Lync Server 2013 topology as a trusted application server.</span></span>

<div>

## <a name="to-create-a-trusted-application-pool"></a><span data-ttu-id="66c98-107">Pour créer un pool d’applications approuvé</span><span class="sxs-lookup"><span data-stu-id="66c98-107">To create a trusted application pool</span></span>

1.  <span data-ttu-id="66c98-108">Démarrez Lync Server 2013 Management Shell.</span><span class="sxs-lookup"><span data-stu-id="66c98-108">Start the Lync Server 2013 Management Shell.</span></span>

2.  <span data-ttu-id="66c98-109">Exécutez l’applet de commande suivante :</span><span class="sxs-lookup"><span data-stu-id="66c98-109">Run the following cmdlet:</span></span>
    
        Get-CsSite
    
    <span data-ttu-id="66c98-110">Le siteID est alors renvoyé pour le siteName dans lequel vous créez le pool.</span><span class="sxs-lookup"><span data-stu-id="66c98-110">This returns the siteID for the siteName in which you are creating the pool.</span></span> <span data-ttu-id="66c98-111">Pour plus d’informations, reportez-vous à la rubrique [Get-CsSite](https://docs.microsoft.com/powershell/module/skype/Get-CsSite) dans la documentation Lync Server 2013 Management Shell.</span><span class="sxs-lookup"><span data-stu-id="66c98-111">For details, see [Get-CsSite](https://docs.microsoft.com/powershell/module/skype/Get-CsSite) in the Lync Server 2013 Management Shell documentation.</span></span>

3.  <span data-ttu-id="66c98-112">Exécutez l’applet de commande suivante :</span><span class="sxs-lookup"><span data-stu-id="66c98-112">Run the following cmdlet:</span></span>
    
        New-CsTrustedApplicationPool -Identity <E14 CAS FQDN> -ThrottleAsServer $true -TreatAsAuthenticated $true -ComputerFQDN <E14 CAS FQDN> -Site <Site> -Registrar <Pool FQDN in the site> -RequiresReplication $false
    
    <span data-ttu-id="66c98-113">Pour plus d’informations, reportez-vous à [New-CsTrustedApplicationPool](https://docs.microsoft.com/powershell/module/skype/New-CsTrustedApplicationPool) dans la documentation de Lync Server 2013 Management Shell.</span><span class="sxs-lookup"><span data-stu-id="66c98-113">For details, see [New-CsTrustedApplicationPool](https://docs.microsoft.com/powershell/module/skype/New-CsTrustedApplicationPool) in the Lync Server 2013 Management Shell documentation.</span></span>
    
    <span data-ttu-id="66c98-114">Le nom de domaine complet du serveur Exchange doit être configuré en tant que nom du sujet du certificat OWA Exchange (SN) ou le nom de l’autre nom de l’objet.</span><span class="sxs-lookup"><span data-stu-id="66c98-114">The Exchange Server FQDN should be configured as the Exchange OWA certificate Subject Name (SN), or the Subject Alternate Name (SAN).</span></span>
    
    <span data-ttu-id="66c98-115">Dans Exchange OWA, vérifiez que le nom de domaine complet (FQDN) du pool est également approuvé.</span><span class="sxs-lookup"><span data-stu-id="66c98-115">In Exchange OWA, verify that the pool’s FQDN is trusted as well.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="66c98-116">Si votre serveur CAS n’est <EM>pas</EM> localisé sur le même serveur qui exécute Exchange 2013 Unified Messaging (um), ignorez les étapes restantes de cette procédure et effectuez la procédure « créer une application sécurisée pour le serveur CAS Exchange 2013 », plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="66c98-116">If your CAS server is <EM>not</EM> collocated on the same server that is running Exchange 2013 Unified Messaging (UM), skip the remaining steps in this procedure and perform the “Create a trusted application for the Exchange 2013 CAS server” procedure later in this topic.</span></span> <span data-ttu-id="66c98-117">Si votre serveur CAS est colocalisé sur le même serveur qui exécute Exchange 2013 Unified Messaging (UM), suivez les étapes décrites dans cette procédure et n’exécutez pas la procédure « créer une application fiable pour le serveur CAS Exchange 2013 », plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="66c98-117">If your CAS server is collocated on the same server that is running Exchange 2013 Unified Messaging (UM), complete the steps in this procedure and do not perform the “Create a trusted application for the Exchange 2013 CAS server” procedure later in this topic.</span></span>

    
    </div>

4.  <span data-ttu-id="66c98-118">Exécutez **Enable-CsTopology**.</span><span class="sxs-lookup"><span data-stu-id="66c98-118">Run **Enable-CsTopology**.</span></span>

5.  <span data-ttu-id="66c98-119">Ouvrez le générateur de topologie et téléchargez la topologie existante.</span><span class="sxs-lookup"><span data-stu-id="66c98-119">Open Topology Builder and download the existing topology.</span></span>

6.  <span data-ttu-id="66c98-120">Dans le volet gauche, développez l’arborescence jusqu’à ce que vous atteigniez **serveurs d’application approuvés**.</span><span class="sxs-lookup"><span data-stu-id="66c98-120">In the left pane, expand the tree until you reach **Trusted application servers**.</span></span>

7.  <span data-ttu-id="66c98-121">Développez le nœud **serveurs d’applications de confiance** .</span><span class="sxs-lookup"><span data-stu-id="66c98-121">Expand the **Trusted application servers** node.</span></span>

8.  <span data-ttu-id="66c98-122">Le serveur Exchange 2013 CAS est désormais répertorié comme serveur d’applications de confiance.</span><span class="sxs-lookup"><span data-stu-id="66c98-122">You should now see the Exchange 2013 CAS server listed as a trusted application server.</span></span>

</div>

<div>

## <a name="to-create-a-trusted-application-for-the-exchange-2013-cas-server"></a><span data-ttu-id="66c98-123">Pour créer une application fiable pour le serveur CAS Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="66c98-123">To create a trusted application for the Exchange 2013 CAS server</span></span>

1.  <span data-ttu-id="66c98-124">Démarrez Lync Server 2013 Management Shell.</span><span class="sxs-lookup"><span data-stu-id="66c98-124">Start the Lync Server 2013 Management Shell.</span></span>

2.  <span data-ttu-id="66c98-125">Si votre serveur CAS n’est *pas* localisé sur le même serveur qui exécute Exchange 2013 Unified Messaging (um), exécutez l’applet de commande suivante :</span><span class="sxs-lookup"><span data-stu-id="66c98-125">If your CAS server is *not* collocated on the same server that is running Exchange 2013 Unified Messaging (UM), run the following cmdlet:</span></span>
    
        New-CsTrustedApplication -ApplicationId <AppID String> -TrustedApplicationPoolFqdn <E14 CAS FQDN> -Port <available port number>
    
    <span data-ttu-id="66c98-126">Pour plus d’informations, reportez-vous à la rubrique [New-CsTrustedApplication](https://docs.microsoft.com/powershell/module/skype/New-CsTrustedApplication) dans la documentation de Lync Server 2013 Management Shell.</span><span class="sxs-lookup"><span data-stu-id="66c98-126">For details, see the topic [New-CsTrustedApplication](https://docs.microsoft.com/powershell/module/skype/New-CsTrustedApplication) in the Lync Server 2013 Management Shell documentation.</span></span>

3.  <span data-ttu-id="66c98-127">Exécutez **Enable-CsTopology**.</span><span class="sxs-lookup"><span data-stu-id="66c98-127">Run **Enable-CsTopology**.</span></span>

4.  <span data-ttu-id="66c98-128">Dans le concepteur de topologies, dans le volet gauche, développez l’arborescence jusqu’à ce que vous atteigniez des **serveurs d’application approuvés**.</span><span class="sxs-lookup"><span data-stu-id="66c98-128">From Topology Builder, in the left pane, expand the tree until you reach **Trusted application servers**.</span></span>

5.  <span data-ttu-id="66c98-129">Développez le nœud **serveurs d’applications de confiance** .</span><span class="sxs-lookup"><span data-stu-id="66c98-129">Expand the **Trusted application servers** node.</span></span>

6.  <span data-ttu-id="66c98-130">Le serveur Exchange 2013 CAS est désormais répertorié comme serveur d’applications de confiance.</span><span class="sxs-lookup"><span data-stu-id="66c98-130">You should now see the Exchange 2013 CAS server listed as a trusted application server.</span></span>

<span data-ttu-id="66c98-131"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="66c98-131"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

