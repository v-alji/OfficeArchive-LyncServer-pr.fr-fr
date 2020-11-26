---
title: Suppression de la base de données SQL Server pour un serveur d’archivage
description: Supprimez la base de données SQL Server d’un serveur d’archivage.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Remove the SQL Server database for an Archiving server
ms:assetid: 6e8a1fcd-ed09-43b0-82c9-60e7ce116a01
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688087(v=OCS.15)
ms:contentKeyID: 49733686
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 738f82f297e1ccb3c6f23f9ecea25657d409f0a6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440247"
---
# <a name="remove-the-sql-server-database-for-an-archiving-server"></a><span data-ttu-id="77d56-103">Suppression de la base de données SQL Server pour un serveur d’archivage</span><span class="sxs-lookup"><span data-stu-id="77d56-103">Remove the SQL Server database for an Archiving server</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="77d56-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="77d56-104">

<span> </span></span></span>

<span data-ttu-id="77d56-105">_**Dernière modification de la rubrique :** 2012-10-04_</span><span class="sxs-lookup"><span data-stu-id="77d56-105">_**Topic Last Modified:** 2012-10-04_</span></span>

<span data-ttu-id="77d56-106">Après avoir supprimé un serveur d’archivage Microsoft Lync Server 2010, vous pouvez supprimer les bases de données SQL Server qui ont hébergé les données du pool.</span><span class="sxs-lookup"><span data-stu-id="77d56-106">After you remove a Microsoft Lync Server 2010 Archiving Server, you can remove the SQL Server databases that hosted the pool data.</span></span> <span data-ttu-id="77d56-107">Utilisez les procédures suivantes pour supprimer les définitions du générateur de topologie, puis supprimez la base de données et les fichiers journaux du serveur de base de données.</span><span class="sxs-lookup"><span data-stu-id="77d56-107">Use the following procedures to remove the definitions from Topology Builder, and then remove the database and log files from the database server.</span></span>

<div>

## <a name="to-remove-the-sql-server-database-using-topology-builder"></a><span data-ttu-id="77d56-108">Pour supprimer la base de données SQL Server à l’aide du générateur de topologie</span><span class="sxs-lookup"><span data-stu-id="77d56-108">To remove the SQL Server database using Topology Builder</span></span>

1.  <span data-ttu-id="77d56-109">Sur le serveur frontal Lync Server 2013, ouvrez le générateur de topologie.</span><span class="sxs-lookup"><span data-stu-id="77d56-109">On the Lync Server 2013 Front End Server, open Topology Builder.</span></span>

2.  <span data-ttu-id="77d56-110">Dans le générateur de topologie, accédez à **composants partagés** puis aux **magasins SQL Server**, cliquez avec le bouton droit sur l’instance SQL Server associée au serveur d’archivage supprimé ou reconfiguré, puis cliquez sur **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="77d56-110">In Topology Builder, navigate to **Shared Components** and then **SQL Server Stores**, right-click the SQL Server instance associated with the removed or reconfigured Archiving Server, and then click **Delete**.</span></span>

3.  <span data-ttu-id="77d56-111">Publiez la topologie, puis vérifiez l’état de la réplication.</span><span class="sxs-lookup"><span data-stu-id="77d56-111">Publish the topology, and then check replication status.</span></span>

</div>

<div>

## <a name="to-remove-the-database-files-from-the-sql-server"></a><span data-ttu-id="77d56-112">Pour supprimer les fichiers de base de données du serveur SQL Server</span><span class="sxs-lookup"><span data-stu-id="77d56-112">To remove the database files from the SQL Server</span></span>

1.  <span data-ttu-id="77d56-113">Pour supprimer les bases de données du serveur SQL Server, vous devez être membre du groupe sysadmin SQL Server pour le serveur SQL sur lequel vous supprimez les fichiers de la base de données.</span><span class="sxs-lookup"><span data-stu-id="77d56-113">To remove the databases on the SQL Server, you must be a member of the SQL Server sysadmins group for the SQL Server where you are removing the database files.</span></span>

2.  <span data-ttu-id="77d56-114">Ouvrez Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="77d56-114">Open the Lync Server Management Shell.</span></span>

3.  <span data-ttu-id="77d56-115">Dans la ligne de commande, tapez ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="77d56-115">At the command line, type the following:</span></span>
    
        Uninstall-CsDataBase -DatabaseType Archiving -SqlServerFqdn <FQDN> [-SqlInstanceName <instance>]
    
    <span data-ttu-id="77d56-116">Emplacement du \<FQDN\> nom de domaine complet (FQDN) du serveur de base de données et \<instance\> est l’instance de base de données nommée (autrement dit, si elle a été définie).</span><span class="sxs-lookup"><span data-stu-id="77d56-116">Where \<FQDN\> is the fully qualified domain name (FQDN) of the database server, and \<instance\> is the named database instance (that is, if one was defined).</span></span>

4.  <span data-ttu-id="77d56-117">Lorsque l’applet de commande **Uninstall-CsDataBase** vous invite à confirmer les actions, lisez les informations, puis appuyez sur **Y** (ou appuyez sur entrée) pour continuer ou sur **N** , puis sur entrée si vous souhaitez arrêter l’applet de commande (autrement dit, en cas d’erreurs).</span><span class="sxs-lookup"><span data-stu-id="77d56-117">When the **Uninstall-CsDataBase** cmdlet prompts you to confirm actions, read the information, and then press **Y** (or press Enter) to proceed, or press **N** and then Enter if you want to stop the cmdlet (that is, in case there errors).</span></span>

<span data-ttu-id="77d56-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="77d56-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

