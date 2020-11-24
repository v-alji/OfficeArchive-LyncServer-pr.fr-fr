---
title: 'Lync Server 2013 : Publication de la topologie'
description: 'Lync Server 2013 : publier votre topologie.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Publish your topology
ms:assetid: bfed3829-7a54-4b5c-a7cb-28871acd35e7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412935(v=OCS.15)
ms:contentKeyID: 48185287
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f4d27d2d3644eb1f174e2f3fab47197f2c122a97
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394552"
---
# <a name="publish-your-topology-in-lync-server-2013"></a><span data-ttu-id="a76d7-103">Publication de la topologie dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a76d7-103">Publish your topology in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a76d7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a76d7-104">

<span> </span></span></span>

<span data-ttu-id="a76d7-105">_**Dernière modification de la rubrique :** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="a76d7-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="a76d7-106">Chaque fois que vous utilisez le générateur de topologie pour générer votre topologie, vous devez publier la topologie sur une base de données dans la Banque centrale de gestion pour que les données puissent être utilisées pour le déploiement de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a76d7-106">Each time you use Topology Builder to build your topology, you must publish the topology to a database in the Central Management store so that the data can be used to deploy Lync Server 2013.</span></span> <span data-ttu-id="a76d7-107">Utilisez la procédure suivante pour publier votre topologie.</span><span class="sxs-lookup"><span data-stu-id="a76d7-107">Use the following procedure to publish your topology.</span></span>

<div>

## <a name="to-publish-the-topology"></a><span data-ttu-id="a76d7-108">Pour publier la topologie</span><span class="sxs-lookup"><span data-stu-id="a76d7-108">To publish the topology</span></span>

1.  <span data-ttu-id="a76d7-109">Démarrer le générateur de topologie : cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Générateur de topologie de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="a76d7-109">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>

2.  <span data-ttu-id="a76d7-110">Dans le générateur de topologie, dans l’arborescence de la console, cliquez avec le bouton droit sur **Lync 2013**, puis cliquez sur **topologie de publication**.</span><span class="sxs-lookup"><span data-stu-id="a76d7-110">In Topology Builder, in the console tree, right-click **Lync 2013**, and then click **Publish Topology**.</span></span>

3.  <span data-ttu-id="a76d7-111">Dans la page **Bienvenue** de l’Assistant, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="a76d7-111">On the **Welcome** page of the wizard, click **Next**.</span></span>

4.  <span data-ttu-id="a76d7-112">Dans le **Générateur de topologie a détecté une page CMS Store** , cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="a76d7-112">On the **Topology Builder found a CMS store** page, click **Next**.</span></span>

5.  <span data-ttu-id="a76d7-113">Dans la page **Créer d’autres bases de données**, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="a76d7-113">On the **Create other databases** page, click **Next**.</span></span>

6.  <span data-ttu-id="a76d7-114">Lorsque l’état indique la création réussie de la base de données, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="a76d7-114">When the status indicates that database creation succeeded, do the following:</span></span>
    
      - <span data-ttu-id="a76d7-115">Pour afficher le journal, cliquez sur **Afficher le journal**.</span><span class="sxs-lookup"><span data-stu-id="a76d7-115">To view the log, click **View log**.</span></span>
    
      - <span data-ttu-id="a76d7-116">Pour fermer l’Assistant, cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="a76d7-116">To close the wizard, click **Finish**.</span></span>
        
        <div>
        

        > [!IMPORTANT]  
        > <span data-ttu-id="a76d7-117">S’il s’agit d’une nouvelle installation d’un serveur de périphérie ou d’un pool de périphériques, vous devez exporter la configuration de serveur Edge à partir d’un serveur frontal, d’un pool frontal ou d’un serveur Standard Edition Server.</span><span class="sxs-lookup"><span data-stu-id="a76d7-117">If this is a new installation of an Edge Server or Edge pool, you must export the Edge Server configuration from an existing Front End Server, Front End pool, or Standard Edition server.</span></span> <span data-ttu-id="a76d7-118">Pour exporter la configuration, reportez-vous à la section <A href="lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md">Export de votre topologie Lync Server 2013 et copiez-la sur du média externe pour l’installation Edge</A>.</span><span class="sxs-lookup"><span data-stu-id="a76d7-118">To export the configuration, see <A href="lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md">Export your Lync Server 2013 topology and copy it to external media for edge installation</A>.</span></span> <span data-ttu-id="a76d7-119">Dans le cadre de l’installation et du déploiement, vous allez importer le fichier de configuration à partir du média externe ou du partage réseau via l’Assistant Déploiement de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="a76d7-119">You will import the configuration file from the external media or network share during the setup and deployment phase of the Edge Servers through the Lync Server Deployment Wizard.</span></span><BR><span data-ttu-id="a76d7-120">Une fois les serveurs Edge opérationnels et la base de données du magasin de gestion des configurations locales répliquant le déploiement interne, les mises à jour ultérieures apportées à la configuration de Lync Server 2013 seront publiées et répliquées sur les serveurs de périphérie.</span><span class="sxs-lookup"><span data-stu-id="a76d7-120">Once the Edge Servers are operational and the local configuration management store database is replicating with the internal deployment, subsequent updates to the Lync Server 2013 configuration will be published and replicated to the Edge Servers.</span></span>

        
        <span data-ttu-id="a76d7-121"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a76d7-121"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

