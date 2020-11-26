---
title: 'Lync Server 2013 : déploiement de l’outil SEFAUtil'
description: 'Lync Server 2013 : déploiement de l’outil SEFAUtil.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploy the SEFAUtil tool
ms:assetid: fb556e50-88dd-4404-a3d5-be36f5ba41e6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945659(v=OCS.15)
ms:contentKeyID: 51541534
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 311f14f33dff30b388836a7f02483c4afe5da1b1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430153"
---
# <a name="deploy-the-sefautil-tool-in-lync-server-2013"></a><span data-ttu-id="d3be4-103">Deploy the SEFAUtil tool in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d3be4-103">Deploy the SEFAUtil tool in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d3be4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d3be4-104">

<span> </span></span></span>

<span data-ttu-id="d3be4-105">_**Dernière modification de la rubrique :** 2013-01-30_</span><span class="sxs-lookup"><span data-stu-id="d3be4-105">_**Topic Last Modified:** 2013-01-30_</span></span>

<span data-ttu-id="d3be4-106">Pour déployer et gérer la cueillette des appels de groupe, vous devez utiliser l’outil Kit de ressources SEFAUtil.</span><span class="sxs-lookup"><span data-stu-id="d3be4-106">To deploy and manage Group Call Pickup, you need to use the SEFAUtil resource kit tool.</span></span> <span data-ttu-id="d3be4-107">L’outil fait partie des outils du kit de ressources Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d3be4-107">The tool is part of the Lync Server 2013 resource kit tools.</span></span> <span data-ttu-id="d3be4-108">Pour pouvoir installer SEFAUtil, vous devez disposer d’un pool d’applications approuvé dans votre topologie, spécifier SEFAUtil en tant qu’application approuvée et activer la topologie.</span><span class="sxs-lookup"><span data-stu-id="d3be4-108">Before you can install SEFAUtil, you must have a trusted application pool in your topology, specify SEFAUtil as a trusted application, and enable the topology.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="d3be4-109">Le Kit de développement logiciel (SDK) Microsoft Unified Communications Managed API (UCMA) 3.0 Core doit être sur les ordinateurs sur lesquels vous voulez exécuter l’outil SEFAUtil.</span><span class="sxs-lookup"><span data-stu-id="d3be4-109">Microsoft Unified Communications Managed API (UCMA) 3.0 Core SDK must be installed on any computer where you plan to run the SEFAUtil tool.</span></span>



</div>

<span data-ttu-id="d3be4-110">Vous pouvez exécuter SEFAUtil dans n’importe quel pool frontal de votre déploiement.</span><span class="sxs-lookup"><span data-stu-id="d3be4-110">You can run the SEFAUtil in any Front End pool in your deployment.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="d3be4-111">Pour plus d’informations sur l’exécution de SEFAUtil, voir l’article de blog TechNet intitulé « Comment puis-je lancer SEFAutil ? »</span><span class="sxs-lookup"><span data-stu-id="d3be4-111">For more details about running SEFAUtil, see the Technet blog article, "How to get SEFAutil running?"</span></span> <span data-ttu-id="d3be4-112">à <A href="https://go.microsoft.com/fwlink/?linkid=278940">https://go.microsoft.com/fwlink/?LinkId=278940</A> .</span><span class="sxs-lookup"><span data-stu-id="d3be4-112">at <A href="https://go.microsoft.com/fwlink/?linkid=278940">https://go.microsoft.com/fwlink/?LinkId=278940</A>.</span></span>



</div>

<div>

## <a name="to-deploy-sefautil"></a><span data-ttu-id="d3be4-113">Pour déployer SEFAUtil</span><span class="sxs-lookup"><span data-stu-id="d3be4-113">To deploy SEFAUtil</span></span>

1.  <span data-ttu-id="d3be4-114">Ouvrez une session sur l’ordinateur sur lequel Lync Server Management Shell est installé en tant que membre du groupe RTCUniversalServerAdmins ou avec les droits d’utilisateur nécessaires, comme décrit dans la rubrique [autorisations de configuration du délégué dans Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="d3be4-114">Log on to the computer where Lync Server Management Shell is installed as a member of the RTCUniversalServerAdmins group or with the necessary user rights as described in [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="d3be4-115">Démarrez Lync Server Management Shell : cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="d3be4-115">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="d3be4-116">L’outil SEFAUtil ne peut être exécuté que sur un ordinateur qui fait partie d’un pool d’applications approuvées.</span><span class="sxs-lookup"><span data-stu-id="d3be4-116">The SEFAUtil tool can be run only on a computer that is part of a trusted application pool.</span></span> <span data-ttu-id="d3be4-117">Le cas échéant, définissez un pool d’applications approuvé pour le pool frontal sur lequel vous envisagez d’exécuter SEFAUtil.</span><span class="sxs-lookup"><span data-stu-id="d3be4-117">If needed, define a trusted application pool for the Front End pool where you plan to run SEFAUtil.</span></span> <span data-ttu-id="d3be4-118">Dans la ligne de commande, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="d3be4-118">At the command line, run:</span></span>
    
        New-CsTrustedApplicationPool -id <Pool FQDN> -Registrar <Pool Registrar FQDN> -site Site:<Pool Site>

4.  <span data-ttu-id="d3be4-p104">Définissez l’outil SEFAUtil en tant qu’application approuvée. Sur la ligne de commande, exécutez :</span><span class="sxs-lookup"><span data-stu-id="d3be4-p104">Define the SEFAUtil tool as a trusted application. At the command line, run:</span></span>
    
        New-CsTrustedApplication -ApplicationId sefautil -TrustedApplicationPoolFqdn <Pool FQDN>  -Port 7489
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="d3be4-121">Vous pouvez utiliser un autre port si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="d3be4-121">You can use a different port if needed.</span></span>

    
    </div>

5.  <span data-ttu-id="d3be4-p105">Activez la topologie avec vos modifications. Sur la ligne de commande, exécutez :</span><span class="sxs-lookup"><span data-stu-id="d3be4-p105">Enable the topology with your changes. At the command line, run:</span></span>
    
        Enable-CsTopology

6.  <span data-ttu-id="d3be4-124">Installez les outils du kit de ressources de Lync Server 2013 sur un serveur frontal qui se trouve dans le pool d’applications approuvé que vous avez créé à l’étape 3.</span><span class="sxs-lookup"><span data-stu-id="d3be4-124">Install the Lync Server 2013 resource kit tools on a Front End Server that is in the trusted application pool that you created in step 3.</span></span>

7.  <span data-ttu-id="d3be4-125">Vérifiez que l’outil SEFAUtil s’exécute correctement ainsi :</span><span class="sxs-lookup"><span data-stu-id="d3be4-125">Verify that the SEFAUtil tool is running correctly, as follows:</span></span>
    
    1.  <span data-ttu-id="d3be4-126">Exécutez l’outil à partir de l’invite de commande Windows avec des droits d’administrateur pour afficher les paramètres de transfert d’appel d’un utilisateur de votre déploiement.</span><span class="sxs-lookup"><span data-stu-id="d3be4-126">Run the tool from the Windows command prompt with administrator privileges to display the call forwarding settings of a user in your deployment.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="d3be4-127">L’outil se trouve à l’emplacement \Program Files\Microsoft Lync Server 2013 \ reskit.</span><span class="sxs-lookup"><span data-stu-id="d3be4-127">The tool is located at \Program Files\Microsoft Lync Server 2013\Reskit.</span></span>

        
        </div>
    
    2.  <span data-ttu-id="d3be4-p106">Affichez les paramètres de transfert d’appel d’un utilisateur. Sur la ligne de commande, exécutez :</span><span class="sxs-lookup"><span data-stu-id="d3be4-p106">Display the call forwarding settings of a user. At the command line, run:</span></span>
        
            SEFAUtil.exe <user SIP address> /server:<Lync Server/Pool FQDN>
        
        <span data-ttu-id="d3be4-130">Les paramètres de transfert d’appel de l’utilisateur s’afficheront.</span><span class="sxs-lookup"><span data-stu-id="d3be4-130">The call forwarding settings for the user will be displayed.</span></span>

<span data-ttu-id="d3be4-131"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d3be4-131"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

