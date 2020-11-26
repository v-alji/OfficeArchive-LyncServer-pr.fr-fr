---
title: 'Lync Server 2013 : exportation de données archivées'
description: 'Lync Server 2013 : exportation de données archivées.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Exporting archived data
ms:assetid: 09450d54-769b-4741-924b-e390664d506f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204657(v=OCS.15)
ms:contentKeyID: 48183347
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 656751f1a2d03b50f0c938a8501ba3e95e304cff
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428334"
---
# <a name="exporting-archived-data-from-lync-server-2013"></a><span data-ttu-id="a0f56-103">Exportation de données archivées à partir de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a0f56-103">Exporting archived data from Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a0f56-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a0f56-104">

<span> </span></span></span>

<span data-ttu-id="a0f56-105">_**Dernière modification de la rubrique :** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="a0f56-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="a0f56-106">Il n’est pas possible de faire des recherches dans les données archivées dans les bases de données d’archivage ou bien ces données ne sont pas dans un format lisible. Cependant, vous pouvez utiliser l’applet de commande Export-CsArchivingData pour les extraire et les enregistrer en tant que fichier EML (Outlook Electronic Mail).</span><span class="sxs-lookup"><span data-stu-id="a0f56-106">Data archived in Archiving databases is not searchable or in a readable format, but you can use the Export-CsArchivingData cmdlet to extract records from the database and save them as an Outlook Electronic Mail (EML) file.</span></span> <span data-ttu-id="a0f56-107">Pour plus d’informations sur l’exportation de données archivées, voir [Export-CsArchivingData](https://docs.microsoft.com/powershell/module/skype/Export-CsArchivingData) dans la documentation sur les opérations.</span><span class="sxs-lookup"><span data-stu-id="a0f56-107">For details about exporting archived data, see [Export-CsArchivingData](https://docs.microsoft.com/powershell/module/skype/Export-CsArchivingData) in the Operations documentation.</span></span>

<span data-ttu-id="a0f56-108">Si vous activez l’intégration de Microsoft Exchange, les données sont archivées dans les magasins Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="a0f56-108">If you enable Microsoft Exchange integration, data is archived in Exchange 2013 stores.</span></span> <span data-ttu-id="a0f56-109">Les données archivées dans Exchange 2013 sont consultables et détectable.</span><span class="sxs-lookup"><span data-stu-id="a0f56-109">Data archived in Exchange 2013 is searchable and discoverable.</span></span> <span data-ttu-id="a0f56-110">Pour plus d’informations sur la prise en charge des communications intégrées pour Exchange 2013 et Lync Server 2013, voir [prise en charge de l’intégration d’Exchange Server et de SharePoint dans Lync server 2013](lync-server-2013-exchange-and-sharepoint-integration-support.md) dans la documentation relative à la prise en charge.</span><span class="sxs-lookup"><span data-stu-id="a0f56-110">For details about support for integrated communications for Exchange 2013 and Lync Server 2013, see [Exchange Server and SharePoint integration support in Lync Server 2013](lync-server-2013-exchange-and-sharepoint-integration-support.md) in the Supportability documentation.</span></span> <span data-ttu-id="a0f56-111">Pour plus d’informations sur l’accès aux données archivées dans Exchange, voir la documentation Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="a0f56-111">For details about accessing data that is archived in Exchange, see the Exchange 2013 documentation.</span></span>

<div>

## <a name="exporting-archiving-data-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="a0f56-112">Exportation des données d’archivage à l’aide d’applets de cmdlet Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="a0f56-112">Exporting Archiving Data by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="a0f56-113">Les données d’archivage peuvent être exportées à l’aide de l’applet de Export-CSArchivingData.</span><span class="sxs-lookup"><span data-stu-id="a0f56-113">Archiving data can be exported by using the Export-CSArchivingData cmdlet.</span></span> <span data-ttu-id="a0f56-114">Cette applet de commande peut être exécutée à partir de Lync Server 2013 Management Shell ou d’une session distante de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a0f56-114">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="a0f56-115">Pour plus d’informations sur l’utilisation de Windows PowerShell distant pour vous connecter à Lync Server, voir l’article de blog Lync Server Windows PowerShell « démarrage rapide : gestion de Microsoft Lync Server 2010 à l’aide de Remote PowerShell » [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="a0f56-115">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<span data-ttu-id="a0f56-116">**Pour exporter les données d’archivage**</span><span class="sxs-lookup"><span data-stu-id="a0f56-116">**To export archiving data**</span></span>

  - <span data-ttu-id="a0f56-117">Cette commande exporte toutes les données d’archivage écrites dans la base de données d’archivage atl-sql-001.litwareinc.com depuis le 1er juin 2012.</span><span class="sxs-lookup"><span data-stu-id="a0f56-117">This command exports all the archiving data written to the archiving database atl-sql-001.litwareinc.com since June 1, 2012.</span></span> <span data-ttu-id="a0f56-118">Le fichier de sortie obtenu sera stocké dans le dossier C : \\ ArchivingExports.</span><span class="sxs-lookup"><span data-stu-id="a0f56-118">The resulting output file will be stored in the folder C:\\ArchivingExports.</span></span>
    
        Export-CsArchivingData -Identity "ArchivingDatabase:atl-sql-001.litwareinc.com" -StartDate 6/1/2012 -OutputFolder "C:\ArchivingExports"

<span data-ttu-id="a0f56-119">**Pour exporter les données d’archivage d’un utilisateur unique**</span><span class="sxs-lookup"><span data-stu-id="a0f56-119">**To export archiving data for a single user**</span></span>

  - <span data-ttu-id="a0f56-120">La commande suivante exporte les données d’archivage d’un utilisateur unique : kenmyer@litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="a0f56-120">The following command exports archiving data for a single user: kenmyer@litwareinc.com.</span></span> <span data-ttu-id="a0f56-121">Pour cela, il suffit d’inclure le paramètre UserUri suivi de l’adresse SIP de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a0f56-121">This is done by including the UserUri parameter followed by the user’s SIP address.</span></span> <span data-ttu-id="a0f56-122">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="a0f56-122">For example:</span></span>
    
        Export-CsArchivingData -Identity "ArchivingDatabase:atl-sql-001.litwareinc.com" -StartDate 6/1/2012 -OutputFolder "C:\ArchivingExports" -UserUri "sip:kenmyer@litwareinc.com"

<span data-ttu-id="a0f56-123">Pour plus d’informations, consultez la rubrique d’aide de l’applet de passe [Export-CsArchivingData](https://docs.microsoft.com/powershell/module/skype/Export-CsArchivingData) .</span><span class="sxs-lookup"><span data-stu-id="a0f56-123">For more information, see the help topic for the [Export-CsArchivingData](https://docs.microsoft.com/powershell/module/skype/Export-CsArchivingData) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="a0f56-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a0f56-124">See Also</span></span>


[<span data-ttu-id="a0f56-125">Prise en charge de l’intégration d’Exchange Server et de SharePoint dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a0f56-125">Exchange Server and SharePoint integration support in Lync Server 2013</span></span>](lync-server-2013-exchange-and-sharepoint-integration-support.md)  


[<span data-ttu-id="a0f56-126">Export-CsArchivingData</span><span class="sxs-lookup"><span data-stu-id="a0f56-126">Export-CsArchivingData</span></span>](https://docs.microsoft.com/powershell/module/skype/Export-CsArchivingData)  
[<span data-ttu-id="a0f56-127">Gestion de l’archivage Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a0f56-127">Managing Lync Server 2013 Archiving</span></span>](lync-server-2013-managing-archiving.md)  
  

<span data-ttu-id="a0f56-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a0f56-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

