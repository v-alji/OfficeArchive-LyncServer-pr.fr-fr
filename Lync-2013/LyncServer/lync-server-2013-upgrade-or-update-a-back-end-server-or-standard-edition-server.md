---
title: Mise à niveau ou mise à jour d’un serveur principal ou d’un serveur Standard Edition Server
description: Mise à niveau ou mise à jour d’un serveur principal ou d’un serveur Standard Edition.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Upgrade or update a Back End Server or Standard Edition server
ms:assetid: f95f8d3a-e039-484e-97bd-d727db21a12b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721942(v=OCS.15)
ms:contentKeyID: 49733879
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c529546bdcf88ada6fd82399d3b65b46b4312db0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440821"
---
# <a name="upgrade-or-update-a-back-end-server-or-standard-edition-server-in-lync-server-2013"></a><span data-ttu-id="efd10-103">Mise à niveau ou mise à jour d’un serveur principal ou d’un serveur Standard Edition Server dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="efd10-103">Upgrade or update a Back End Server or Standard Edition server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="efd10-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="efd10-104">

<span> </span></span></span>

<span data-ttu-id="efd10-105">_**Dernière modification de la rubrique :** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="efd10-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="efd10-106">Cette rubrique explique comment installer une mise à jour sur un serveur principal Enterprise Edition ou un serveur Standard Edition Server.</span><span class="sxs-lookup"><span data-stu-id="efd10-106">This topic explains how to install an update on an Enterprise Edition Back End Server or a Standard Edition server.</span></span>

<span data-ttu-id="efd10-107">Si un serveur principal est arrêté pendant au moins 30 minutes lors de la mise à niveau, les utilisateurs peuvent alors basculer en mode de résilience.</span><span class="sxs-lookup"><span data-stu-id="efd10-107">If a Back End Server is down for at least 30 minutes while you are upgrading it, users may then go into resiliency mode.</span></span> <span data-ttu-id="efd10-108">Lorsque la mise à niveau est terminée et que les serveurs dorsaux sont à nouveau connectés avec les serveurs frontaux de la liste, les utilisateurs sont retournés à toutes les fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="efd10-108">When the upgrade is finished and the Back End Servers has again connected with the Front End Servers in the pool, users are returned to full functionality.</span></span> <span data-ttu-id="efd10-109">Si la mise à niveau dure moins de 30 minutes, les utilisateurs ne sont pas affectés.</span><span class="sxs-lookup"><span data-stu-id="efd10-109">If the upgrade takes less than 30 minutes, users will not be affected.</span></span>

<div>

## <a name="to-update-a-back-end-server-or-standard-edition-server"></a><span data-ttu-id="efd10-110">Pour mettre à jour un serveur principal ou un serveur Standard Edition</span><span class="sxs-lookup"><span data-stu-id="efd10-110">To update a back end server or Standard Edition server</span></span>

1.  <span data-ttu-id="efd10-111">Connectez-vous au serveur que vous mettez à niveau en tant que membre du rôle CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="efd10-111">Log on to the server you are upgrading as a member of the CsAdministrator role.</span></span>

2.  <span data-ttu-id="efd10-112">Téléchargez la mise à jour et extrayez-la sur le disque dur local.</span><span class="sxs-lookup"><span data-stu-id="efd10-112">Download the update and extract it to the local hard disk.</span></span>

3.  <span data-ttu-id="efd10-113">Démarrez Lync Server Management Shell : cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="efd10-113">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

4.  <span data-ttu-id="efd10-114">Arrêtez les services Lync Server.</span><span class="sxs-lookup"><span data-stu-id="efd10-114">Stop Lync Server services.</span></span> <span data-ttu-id="efd10-115">À partir de la ligne de commande, tapez :</span><span class="sxs-lookup"><span data-stu-id="efd10-115">At the command line, type:</span></span>
    
        Stop-CsWindowsService

5.  <span data-ttu-id="efd10-116">Arrêtez les services World Wide Web.</span><span class="sxs-lookup"><span data-stu-id="efd10-116">Stop the World Wide Web service.</span></span> <span data-ttu-id="efd10-117">À partir de la ligne de commande, tapez :</span><span class="sxs-lookup"><span data-stu-id="efd10-117">At the command line, type:</span></span>
    
        net stop w3svc

6.  <span data-ttu-id="efd10-118">Fermez toutes les fenêtres de Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="efd10-118">Close all Lync Server Management Shell windows.</span></span>

7.  <span data-ttu-id="efd10-119">Installez la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="efd10-119">Install the update.</span></span>

8.  <span data-ttu-id="efd10-120">Démarrez Lync Server Management Shell : cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="efd10-120">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

9.  <span data-ttu-id="efd10-121">Arrêtez de nouveau les services Lync Server pour détecter les assemblys du cache d’assembly global (GAC)-d</span><span class="sxs-lookup"><span data-stu-id="efd10-121">Stop Lync Server services again to catch Global Assembly Cache (GAC) –d assemblies.</span></span> <span data-ttu-id="efd10-122">À partir de la ligne de commande, tapez :</span><span class="sxs-lookup"><span data-stu-id="efd10-122">At the command line, type:</span></span>
    
        Stop-CsWindowsService

10. <span data-ttu-id="efd10-123">Redémarrez les services World Wide Web.</span><span class="sxs-lookup"><span data-stu-id="efd10-123">Restart the World Wide Web service.</span></span> <span data-ttu-id="efd10-124">À partir de la ligne de commande, tapez :</span><span class="sxs-lookup"><span data-stu-id="efd10-124">At the command line, type:</span></span>
    
        net start w3svc

11. <span data-ttu-id="efd10-125">Appliquez les modifications apportées par LyncServerUpdateInstaller.exe aux bases de données SQL Server en effectuant l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="efd10-125">Apply the changes made by LyncServerUpdateInstaller.exe to the SQL Server databases by doing one of the following:</span></span>
    
      - <span data-ttu-id="efd10-126">S’il s’agit d’un serveur principal Enterprise Edition et qu’il n’y a pas de bases de données colocalisées sur ce serveur, telles que des bases de données d’archivage ou de surveillance, tapez les informations suivantes dans une ligne de commande :</span><span class="sxs-lookup"><span data-stu-id="efd10-126">If this is an Enterprise Edition Back End Server and there are no collocated databases on this server, such as Archiving or Monitoring databases, then type the following at a command line:</span></span>
        
            Install-CsDatabase -Update -ConfiguredDatabases -SqlServerFqdn <SQL Server FQDN>
    
      - <span data-ttu-id="efd10-127">S’il s’agit d’une base de données serveur principal de la version Enterprise Edition et de bases de données colocalisées sur ce serveur, tapez les informations suivantes à partir de la ligne de commande suivante :</span><span class="sxs-lookup"><span data-stu-id="efd10-127">If this is an Enterprise Edition Back End Server and there are collocated databases on this server, then type the following at a command line:</span></span>
        
            Install-CsDatabase -Update -ConfiguredDatabases -SqlServerFqdn <SQL Server FQDN>  -ExcludeCollocatedStores
    
      - <span data-ttu-id="efd10-128">S’il s’agit d’un serveur Standard Edition Server, tapez les informations suivantes dans une ligne de commande :</span><span class="sxs-lookup"><span data-stu-id="efd10-128">If this is an Standard Edition server, type the following at a command line:</span></span>
        
            Install-CsDatabase -Update -LocalDatabases

<span data-ttu-id="efd10-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="efd10-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

