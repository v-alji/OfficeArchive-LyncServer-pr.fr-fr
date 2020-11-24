---
title: 'Lync Server 2013 : utilisation des options de ligne de commande du programme d’installation'
description: 'Lync Server 2013 : utilisation des options de ligne de commande du programme d’installation.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Using Setup command-line options
ms:assetid: 99878c3c-ff31-48e2-8424-580d7b07a7bf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205129(v=OCS.15)
ms:contentKeyID: 48184957
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 15c3490ead090766462ce83cb13ffe62355032cd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49393897"
---
# <a name="using-setup-command-line-options-in-lync-server-2013"></a><span data-ttu-id="4ae01-103">Utilisation des options de ligne de commande du programme d’installation dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4ae01-103">Using Setup command-line options in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4ae01-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4ae01-104">

<span> </span></span></span>

<span data-ttu-id="4ae01-105">_**Dernière modification de la rubrique :** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="4ae01-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="4ae01-p101">La ligne de commande Setup.exe est utilisée pour très peu d’opérations dans le programme d’installation d’Office. Au lieu d’utiliser les options de ligne de commande du programme d’installation, vous utiliserez généralement l’outil de personnalisation Office et le fichier Config.xml pour personnaliser l’installation du produit et de ses fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="4ae01-p101">The Setup.exe command line is used for very few operations in Office setup. Instead of using the Setup command-line options, you’ll typically use the Office Customization Tool and the Config.xml file for product setup and feature customization.</span></span>

<span data-ttu-id="4ae01-108">La ligne de commande de Setup.exe reconnaît les options de ligne de commande décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="4ae01-108">The Office Setup.exe command line recognizes the command-line options described in the following table.</span></span>

### <a name="office-setup-command-line-options"></a><span data-ttu-id="4ae01-109">Options de ligne de commande du programme d’installation Office</span><span class="sxs-lookup"><span data-stu-id="4ae01-109">Office Setup Command-Line Options</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4ae01-110">Options de ligne de commande du programme d’installation</span><span class="sxs-lookup"><span data-stu-id="4ae01-110">Setup Command-Line Option</span></span></th>
<th><span data-ttu-id="4ae01-111">Description</span><span class="sxs-lookup"><span data-stu-id="4ae01-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4ae01-112">/admin</span><span class="sxs-lookup"><span data-stu-id="4ae01-112">/admin</span></span></p></td>
<td><p><span data-ttu-id="4ae01-113">Exécute l’outil de personnalisation Office pour créer un fichier de personnalisation de l’installation (fichier .msp).</span><span class="sxs-lookup"><span data-stu-id="4ae01-113">Runs the Office Customization Tool to create a Setup customization file (.msp file).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ae01-114">/adminfile [chemin]</span><span class="sxs-lookup"><span data-stu-id="4ae01-114">/adminfile [path]</span></span></p></td>
<td><p><span data-ttu-id="4ae01-p102">Applique le fichier de personnalisation de l’installation spécifié à l’installation. Vous pouvez spécifier un chemin d’accès à un fichier de personnalisation spécifique (fichier .msp) ou au dossier dans lequel vous stockez les fichiers de personnalisation.</span><span class="sxs-lookup"><span data-stu-id="4ae01-p102">Applies the specified Setup customization file to the installation. You can specify a path of a specific customization file (.msp file) or to the folder where you store customization files.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ae01-117">/config [chemin]</span><span class="sxs-lookup"><span data-stu-id="4ae01-117">/config [path]</span></span></p></td>
<td><p><span data-ttu-id="4ae01-118">Spécifie le fichier Config.xml utilisé par le programme d’installation lors de l’installation.</span><span class="sxs-lookup"><span data-stu-id="4ae01-118">Specifies the Config.xml file that Setup uses during the installation.</span></span> <span data-ttu-id="4ae01-119">Utilisez l’option/config pour spécifier le Config.xml fichier que vous avez personnalisé pour les installations de Lync 2013, par exemple : <code>/config \\server\share\Lync15\Lync.WW\Config.xml</code></span><span class="sxs-lookup"><span data-stu-id="4ae01-119">Use the /config option to specify the Config.xml file you customized for Lync 2013 installations, for example: <code>/config \\server\share\Lync15\Lync.WW\Config.xml</code></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ae01-120">/Modify Lync</span><span class="sxs-lookup"><span data-stu-id="4ae01-120">/modify Lync</span></span></p></td>
<td><p><span data-ttu-id="4ae01-121">Utilisée avec un fichier Config.xml modifié, cette option permet d’exécuter le programme d’installation en mode maintenance et d’apporter des modifications à une installation Office existante.</span><span class="sxs-lookup"><span data-stu-id="4ae01-121">Used with a modified Config.xml file to run Setup in maintenance mode and make changes to an existing Office installation.</span></span> <span data-ttu-id="4ae01-122">Par exemple, vous pouvez utiliser l’option/Modify pour ajouter ou supprimer des fonctionnalités Lync.</span><span class="sxs-lookup"><span data-stu-id="4ae01-122">For example, you can use the /modify option to add or remove Lync features.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ae01-123">/Repair Lync</span><span class="sxs-lookup"><span data-stu-id="4ae01-123">/repair Lync</span></span></p></td>
<td><p><span data-ttu-id="4ae01-124">Exécute le programme d’installation à partir de l’ordinateur de l’utilisateur pour réparer Lync.</span><span class="sxs-lookup"><span data-stu-id="4ae01-124">Runs Setup from the user’s computer to repair Lync.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ae01-125">/Uninstall Lync</span><span class="sxs-lookup"><span data-stu-id="4ae01-125">/uninstall Lync</span></span></p></td>
<td><p><span data-ttu-id="4ae01-126">Exécute le programme d’installation pour supprimer Lync de l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4ae01-126">Runs Setup to remove Lync from the user’s computer.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4ae01-127">Pour plus d’informations sur l’utilisation des options de ligne de commande du programme d’installation, voir <https://go.microsoft.com/fwlink/p/?linkid=267515> .</span><span class="sxs-lookup"><span data-stu-id="4ae01-127">For details about using the setup command-line options, see <https://go.microsoft.com/fwlink/p/?linkid=267515>.</span></span>

<span data-ttu-id="4ae01-128"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4ae01-128"></div>

<span> </span>

</div>

</div>

</span></span></div>

