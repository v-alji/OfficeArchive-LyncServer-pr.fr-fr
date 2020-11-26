---
title: 'Lync Server 2013 : Définition d’un Survivable Branch Appliance ou d’un serveur Survivable Branch Server'
description: 'Lync Server 2013 : définissez une unité ou un serveur Survivable.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Define a Survivable Branch Appliance or Server
ms:assetid: 1f49cfbe-30b3-4600-af15-47cb2f58d18a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398280(v=OCS.15)
ms:contentKeyID: 48183583
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 946aec82f33dffe268fefb3548b8db2f5c19e1a8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431098"
---
# <a name="define-a-survivable-branch-appliance-or-server-in-lync-server-2013"></a><span data-ttu-id="3bf3b-103">Définition d’un Survivable Branch Appliance ou d’un serveur Survivable Branch Server dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3bf3b-103">Define a Survivable Branch Appliance or Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3bf3b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3bf3b-104">

<span> </span></span></span>

<span data-ttu-id="3bf3b-105">_**Dernière modification de la rubrique :** 2012-10-07_</span><span class="sxs-lookup"><span data-stu-id="3bf3b-105">_**Topic Last Modified:** 2012-10-07_</span></span>

<span data-ttu-id="3bf3b-106">Suivez cette procédure sur le site central si vous n’avez pas défini l’appareil ou le serveur de succursale Survivable lorsque vous l’avez ajouté à votre topologie.</span><span class="sxs-lookup"><span data-stu-id="3bf3b-106">Perform this procedure at the central site if you did not define the Survivable Branch Appliance or Server when you added it to your topology.</span></span>

<div>

## <a name="to-define-a-survivable-branch-appliance-or-survivable-branch-server"></a><span data-ttu-id="3bf3b-107">Pour définir une unité de branchement ou un serveur de succursale survivant</span><span class="sxs-lookup"><span data-stu-id="3bf3b-107">To define a Survivable Branch Appliance or Survivable Branch Server</span></span>

1.  <span data-ttu-id="3bf3b-108">Cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Générateur de topologie de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="3bf3b-108">Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>

2.  <span data-ttu-id="3bf3b-109">Dans l’arborescence de la console, développez le site central, développez **sites de succursales**, puis développez le nom du site de succursale dans lequel vous envisagez de déployer l’application de succursale ou le serveur de succursale Survivable.</span><span class="sxs-lookup"><span data-stu-id="3bf3b-109">In the console tree, expand the central site, expand **Branch sites**, and then expand the name of the branch site where you plan to deploy the Survivable Branch Appliance or Survivable Branch Server.</span></span>

3.  <span data-ttu-id="3bf3b-110">Cliquez avec le bouton droit sur **périphériques survivables**, puis cliquez sur **nouvelle unité de branchement Survivable**.</span><span class="sxs-lookup"><span data-stu-id="3bf3b-110">Right-click **Survivable Branch Appliances**, and then click **New Survivable Branch Appliance**.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="3bf3b-111">Les <STRONG>appareils de branchement survivables</STRONG> vous permet de définir des serveurs de succursales survivables et des appareils de branchement plus survivant.</span><span class="sxs-lookup"><span data-stu-id="3bf3b-111"><STRONG>Survivable Branch Appliances</STRONG> is where you define Survivable Branch Servers and Survivable Branch Appliances.</span></span>

    
    </div>

4.  <span data-ttu-id="3bf3b-112">Dans la boîte de dialogue **définir une branche Survivable** , **cliquez sur** nom de domaine complet, tapez le nom de domaine complet (FQDN) de l’appareil ou du serveur de succursales survivant que vous déploierez sur ce site de succursale, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="3bf3b-112">In the **Define Survivable Branch Appliance** dialog box, click **FQDN**, type the fully qualified domain name (FQDN) of the Survivable Branch Appliance or Survivable Branch Server you will deploy at this branch site, and then click **Next**.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="3bf3b-113">Si vous définissez une unité de branchement Survivable, le nom que vous entrez dans <STRONG>FQDN</STRONG> doit être le même que celui du nom de domaine complet (FQDN) <STRONG>de l’appareil</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="3bf3b-113">If you are defining a Survivable Branch Appliance, the name you enter in <STRONG>FQDN</STRONG> must be the same as the Survivable Branch Appliance FQDN you assigned to the <STRONG>servicePrincipalName</STRONG> attribute.</span></span> <span data-ttu-id="3bf3b-114">Pour plus d’informations, reportez-vous <A href="lync-server-2013-add-a-survivable-branch-appliance-to-active-directory.md">à la rubrique ajouter une application de branchement survivant à Active Directory dans Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="3bf3b-114">For details, see <A href="lync-server-2013-add-a-survivable-branch-appliance-to-active-directory.md">Add a Survivable Branch Appliance to Active Directory in Lync Server 2013</A>.</span></span>

    
    </div>

5.  <span data-ttu-id="3bf3b-115">Cliquez sur **pool frontal**, cliquez sur le serveur frontal (pool de services d’application) sur le site central pour lequel est connectée cette unité de branchement ou serveur de succursale Survivable, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="3bf3b-115">Click **Front End pool**, click the Front End Server (User Services pool) at the central site that this Survivable Branch Appliance or Survivable Branch Server will connect to, and then click **Next**.</span></span>

6.  <span data-ttu-id="3bf3b-116">Cliquez sur **serveur de bord**, cliquez sur le pool de bords de l’appareil de succursales ou du serveur de succursales survivant qui sera connecté pour fournir une connectivité PSTN aux utilisateurs distants du site de succursale, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="3bf3b-116">Click **Edge Server**, click the Edge pool that this Survivable Branch Appliance or Survivable Branch Server will connect to provide PSTN connectivity to remote users of the branch site, and then click **Next**.</span></span>

7.  <span data-ttu-id="3bf3b-117">Cliquez sur FQDN de la **passerelle ou adresse IP**, puis tapez le nom de domaine complet ou l’adresse IP de l’homologue de la passerelle pour le routage des appels RTC entrants ou sortants.</span><span class="sxs-lookup"><span data-stu-id="3bf3b-117">Click **Gateway FQDN or IP Address**, and then type the FQDN or IP address of the gateway peer that the Survivable Branch Appliance or Survivable Branch Server is associated with for routing inbound or outbound PSTN calls.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="3bf3b-118">S’il s’agit de la définition d’une unité de branchement survivant, il s’agit de la passerelle à laquelle le serveur de médiation de l’appareil de branchement survivant se connecte pour la connectivité PSTN.</span><span class="sxs-lookup"><span data-stu-id="3bf3b-118">If you are defining a Survivable Branch Appliance, this is the gateway to which the Mediation Server inside the Survivable Branch Appliance will connect for PSTN connectivity.</span></span>

    
    </div>

8.  <span data-ttu-id="3bf3b-119">Cliquez sur **port d’écoute pour la passerelle RTC/IP**, puis acceptez le port par défaut.</span><span class="sxs-lookup"><span data-stu-id="3bf3b-119">Click **Listening Port for IP/PSTN Gateway**, and then accept the default port.</span></span>

9.  <span data-ttu-id="3bf3b-120">Dans **protocole de transport SIP**, cliquez sur le protocole de transport utilisé par l’unité de branchement ou le serveur de succursales survivant, puis cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="3bf3b-120">In **Sip Transport Protocol**, click the transport protocol the Survivable Branch Appliance or Survivable Branch Server will use, and then click **Finish**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="3bf3b-121">Pour des raisons de sécurité, nous vous recommandons vivement d’utiliser le protocole TLS (Transport Layer Security).</span><span class="sxs-lookup"><span data-stu-id="3bf3b-121">For security reasons, we strongly recommend that you use Transport Layer Security (TLS).</span></span> <span data-ttu-id="3bf3b-122">Si vous définissez une application branche Survivable, consultez la documentation fournie par le fabricant de votre appareil pour vérifier que votre application de branchement Survivable prend en charge le protocole TLS.</span><span class="sxs-lookup"><span data-stu-id="3bf3b-122">If you are defining a Survivable Branch Appliance, refer to your Survivable Branch Appliance vendor documentation to verify that your Survivable Branch Appliance supports the TLS protocol.</span></span>

    
    </div>

10. <span data-ttu-id="3bf3b-123">Dans l’arborescence de la console, cliquez avec le bouton droit sur la nouvelle branche ou serveur Survivable, cliquez sur **Topology**, puis sur **publier**.</span><span class="sxs-lookup"><span data-stu-id="3bf3b-123">In the console tree, right-click the new Survivable Branch Appliance or Server, click **Topology**, and then click **Publish**.</span></span>

<span data-ttu-id="3bf3b-124">**Étape suivante**: [déploiement d’une unité ou d’un serveur de succursale Survivable avec Lync Server 2013-tâche de succursale](lync-server-2013-deploy-a-survivable-branch-appliance-or-server-branch-site-task.md)</span><span class="sxs-lookup"><span data-stu-id="3bf3b-124">**Next step**: [Deploy a Survivable Branch Appliance or Server with Lync Server 2013 - branch site task](lync-server-2013-deploy-a-survivable-branch-appliance-or-server-branch-site-task.md)</span></span>

<span data-ttu-id="3bf3b-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3bf3b-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

