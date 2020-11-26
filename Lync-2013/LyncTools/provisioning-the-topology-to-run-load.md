---
title: Mise en service de la topologie pour exécuter le chargement
description: Mise en service de la topologie pour exécuter le chargement.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Provisioning the Topology to Run Load
ms:assetid: 6fba03df-3914-4d2a-8208-e252ad993aff
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945598(v=OCS.15)
ms:contentKeyID: 51541424
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: da482fde949675acc1722305433b95b7a6a6b523
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446422"
---
# <a name="provisioning-the-topology-to-run-load"></a><span data-ttu-id="2c040-103">Mise en service de la topologie pour exécuter le chargement</span><span class="sxs-lookup"><span data-stu-id="2c040-103">Provisioning the Topology to Run Load</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2c040-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2c040-104">

<span> </span></span></span>

<span data-ttu-id="2c040-105">_**Dernière modification de la rubrique :** 2013-02-04_</span><span class="sxs-lookup"><span data-stu-id="2c040-105">_**Topic Last Modified:** 2013-02-04_</span></span>

<div>

<span data-ttu-id="2c040-106">Selon vos paramètres et la configuration de Lync Server 2013, il est possible que vous deviez apporter les modifications suivantes à votre environnement :</span><span class="sxs-lookup"><span data-stu-id="2c040-106">Depending on your existing settings and configuration of Lync Server 2013, you may need to make the following changes in your environment:</span></span>

1.  <span data-ttu-id="2c040-107">Définissez la stratégie d’exécution Windows PowerShell sur non restreinte.</span><span class="sxs-lookup"><span data-stu-id="2c040-107">Set the Windows PowerShell execution policy to Unrestricted.</span></span> <span data-ttu-id="2c040-108">Pour vérifier les paramètres de stratégie d’exécution, ouvrez Lync Server Management Shell et exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="2c040-108">To check your execution policy settings, open the Lync Server Management Shell and run the following command:</span></span>

    ``` powershell
        Get-ExecutionPolicy
    ```        

    <span data-ttu-id="2c040-109">Si cette commande n’a pas pour résultat la valeur Unrestricted, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="2c040-109">If this command does not return the value Unrestricted, run this command:</span></span>

    ``` powershell
        Set-ExecutionPolicy -Unrestricted
    ```

2.  <span data-ttu-id="2c040-110">Pour configurer efficacement Lync Server 2013, vous devez :</span><span class="sxs-lookup"><span data-stu-id="2c040-110">To effectively configure Lync Server 2013, you will need to:</span></span>
    
      - <span data-ttu-id="2c040-111">Familiarisez-vous avec la topologie Lync Server 2013 (par exemple, les noms d’ordinateurs, les instances de service, les noms de sites et les stratégies).</span><span class="sxs-lookup"><span data-stu-id="2c040-111">Be familiar with Lync Server 2013 topology (for example, computer names, service instances, site names, and policies).</span></span>
    
      - <span data-ttu-id="2c040-112">Assignez certains utilisateurs qui ont été créés dans des groupes, par exemple, des groupes de recherche de Response Group (par exemple, URI SIP).</span><span class="sxs-lookup"><span data-stu-id="2c040-112">Assign some of the users that were created to groups, such as Response Group hunt groups (for example, SIP URIs).</span></span>

3.  <span data-ttu-id="2c040-113">Pour exécuter le script à partir de la ligne de commande, vous pouvez utiliser les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="2c040-113">To run the script from the command line, you may use:</span></span>

    ``` powershell
        Powershell.exe -file <path to the file>
    ```
    
4.  <span data-ttu-id="2c040-114">En règle générale, après l’exécution de l’un des scripts de ce package, les traces obtenues à partir du script seront stockées dans un fichier dans le même chemin à partir duquel le script est appelé \<scriptname\> $h $ m $s.txt.</span><span class="sxs-lookup"><span data-stu-id="2c040-114">Typically, after one of the scripts in this package runs, the resulting traces from the script will be stored in a file in the same path from which the script was invoked, named \<scriptname\>$h$m$s.txt.</span></span> <span data-ttu-id="2c040-115">Par exemple, l’exécution de ArchivingPolicy.ps1 à 12:15 P.M.</span><span class="sxs-lookup"><span data-stu-id="2c040-115">For example, running ArchivingPolicy.ps1 at 12:15 P.M.</span></span> <span data-ttu-id="2c040-116">va générer un fichier journal tel que ArchivingPolicy121500.txt.</span><span class="sxs-lookup"><span data-stu-id="2c040-116">will generate a log file such as ArchivingPolicy121500.txt.</span></span>

5.  <span data-ttu-id="2c040-117">Enfin, Notez que bien que nous ayons fourni des exemples de configuration du serveur, vous êtes responsable de la modification ou de la suppression de la configuration lorsque vous avez terminé d’exécuter le chargement.</span><span class="sxs-lookup"><span data-stu-id="2c040-117">Finally, note that although we have provided examples to configure the server, you are responsible for modifying or deleting the configuration after you have finished running the load.</span></span>

<span data-ttu-id="2c040-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2c040-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

