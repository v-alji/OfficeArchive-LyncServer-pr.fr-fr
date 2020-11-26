---
title: 'Lync Server 2013 : restauration d’un magasin de fichiers'
description: 'Lync Server 2013 : restauration d’un magasin de fichiers.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Restoring a file store
ms:assetid: 89916fc6-31d3-4c7f-9eaf-c02584761ef4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202180(v=OCS.15)
ms:contentKeyID: 51541491
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 201c4b20f224fa3a25e931689e564410c60143e6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436250"
---
# <a name="restoring-a-file-store-in-lync-server-2013"></a><span data-ttu-id="c7314-103">Restauration d’un magasin de fichiers dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c7314-103">Restoring a file store in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c7314-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c7314-104">

<span> </span></span></span>

<span data-ttu-id="c7314-105">_**Dernière modification de la rubrique :** 2013-02-18_</span><span class="sxs-lookup"><span data-stu-id="c7314-105">_**Topic Last Modified:** 2013-02-18_</span></span>

<span data-ttu-id="c7314-106">Les magasins de fichiers pour l’édition standard sont généralement situés sur le serveur Standard Edition Server.</span><span class="sxs-lookup"><span data-stu-id="c7314-106">File Stores for Standard Edition are typically located on the Standard Edition server.</span></span> <span data-ttu-id="c7314-107">Les magasins de fichiers pour Enterprise Edition sont généralement situés sur un serveur de fichiers ou un cluster.</span><span class="sxs-lookup"><span data-stu-id="c7314-107">File Stores for Enterprise Edition are typically located on a file server or cluster.</span></span> <span data-ttu-id="c7314-108">La procédure suivante vous explique comment restaurer un magasin de fichiers.</span><span class="sxs-lookup"><span data-stu-id="c7314-108">The following procedure describes how to restore a File Store.</span></span>

<div>

## <a name="to-restore-a-file-store"></a><span data-ttu-id="c7314-109">Pour restaurer un magasin de fichiers</span><span class="sxs-lookup"><span data-stu-id="c7314-109">To restore a File Store</span></span>

1.  <span data-ttu-id="c7314-110">En cas d’échec d’un magasin de fichiers, copiez le magasin de fichiers approprié à partir de $Backup \\ à l’emplacement de stockage des fichiers sur le serveur de fichiers ou Standard Edition Server, puis partagez le dossier.</span><span class="sxs-lookup"><span data-stu-id="c7314-110">If a File Store fails, copy the appropriate File Store from $Backup\\ to the File Store location on the file server or Standard Edition server, and then share the folder.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="c7314-111">Le chemin d’accès et le nom de fichier du magasin de fichiers restauré doivent être exactement les mêmes que ceux du magasin de fichiers sauvegardés, afin que les composants qui utilisent les fichiers puissent y accéder.</span><span class="sxs-lookup"><span data-stu-id="c7314-111">The path and file name for the restored File Store should be exactly the same as the backed up File Store, so that components that use the files can access them.</span></span>

    
    </div>

2.  <span data-ttu-id="c7314-112">Le cas échéant, définissez les listes de contrôle d’accès (ACL) pour le magasin de fichiers.</span><span class="sxs-lookup"><span data-stu-id="c7314-112">If necessary, set the access control lists (ACLs) for the File Store.</span></span> <span data-ttu-id="c7314-113">À partir de la ligne de commande, tapez :</span><span class="sxs-lookup"><span data-stu-id="c7314-113">At the command line, type:</span></span>
    
        Enable-CsTopology
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="c7314-114">Vous ne devez effectuer cette étape que si vous n’avez pas exécuté de générateur de topologie lors du processus de restauration.</span><span class="sxs-lookup"><span data-stu-id="c7314-114">You need to perform this step only if you have not otherwise run Topology Builder during your restoration process.</span></span>

    
    <span data-ttu-id="c7314-115"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c7314-115"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

