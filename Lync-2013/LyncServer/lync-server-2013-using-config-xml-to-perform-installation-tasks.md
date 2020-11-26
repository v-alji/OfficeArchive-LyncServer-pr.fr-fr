---
title: 'Lync Server 2013 : utilisation de Config.xml pour effectuer des tâches d’installation'
description: 'Lync Server 2013 : utilisation de Config.xml pour effectuer des tâches d’installation.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Using Config.xml to perform installation tasks
ms:assetid: 0813184a-ab40-417c-b3a3-c2090766b831
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204651(v=OCS.15)
ms:contentKeyID: 48183332
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 22fff14e21a120c3a0ee2cd6432fd1eba2bbee5f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438952"
---
# <a name="using-configxml-to-perform-installation-tasks-in-lync-server-2013"></a><span data-ttu-id="e1511-103">Utilisation de Config.xml pour effectuer des tâches d’installation dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e1511-103">Using Config.xml to perform installation tasks in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e1511-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e1511-104">

<span> </span></span></span>

<span data-ttu-id="e1511-105">_**Dernière modification de la rubrique :** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="e1511-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="e1511-p101">Même si l’outil de personnalisation Office est le principal outil pour l’installation personnalisée, les administrateurs peuvent utiliser le fichier Config.xml pour spécifier des instructions d’installation non disponibles dans cet outil. Les personnalisations ci-dessous ne peuvent être effectuées qu’avec le fichier Config.xml :</span><span class="sxs-lookup"><span data-stu-id="e1511-p101">Although the Office Customization Tool (OCT) is the primary tool for customization installation, administrators can use the Config.xml file to specify additional installation instructions that are not available in the OCT. The following customizations can only be made by using the Config.xml file:</span></span>

  - <span data-ttu-id="e1511-108">Spécifiez le chemin d’accès au point d’installation réseau.</span><span class="sxs-lookup"><span data-stu-id="e1511-108">Specify the path of the network installation point.</span></span>

  - <span data-ttu-id="e1511-109">Sélectionnez les produits à installer.</span><span class="sxs-lookup"><span data-stu-id="e1511-109">Select the products to install.</span></span>

  - <span data-ttu-id="e1511-110">Configurez la journalisation et l’emplacement du fichier de personnalisation de l’installation et les mises à jour des logiciels.</span><span class="sxs-lookup"><span data-stu-id="e1511-110">Configure logging and the location of the Setup customization file and software updates.</span></span>

  - <span data-ttu-id="e1511-111">Spécifiez les options d’installation, comme le nom d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e1511-111">Specify installation options, such as user name.</span></span>

  - <span data-ttu-id="e1511-112">Copiez la source d’installation locale sur l’ordinateur de l’utilisateur sans installer Office.</span><span class="sxs-lookup"><span data-stu-id="e1511-112">Copy the local installation source (LIS) to the user's computer without installing Office.</span></span>

  - <span data-ttu-id="e1511-113">Ajoutez ou supprimez des langues dans l’installation.</span><span class="sxs-lookup"><span data-stu-id="e1511-113">Add or remove languages from the installation.</span></span>

<span data-ttu-id="e1511-114">Nous vous recommandons d’utiliser le fichier Config.xml pour configurer l’installation silencieuse de Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="e1511-114">We recommend that you use the Config.xml file to configure Lync 2013 silent installation.</span></span>

<span data-ttu-id="e1511-115">Par défaut, le fichier Config.xml stocké dans le dossier de produit principal (par exemple, \\ produit. WW) envoie le programme d’installation de ce produit.</span><span class="sxs-lookup"><span data-stu-id="e1511-115">By default, the Config.xml file that is stored in the core product folder (for example, \\product.WW) directs Setup to install that product.</span></span> <span data-ttu-id="e1511-116">Par exemple, le fichier Config.xml dans le dossier suivant installe Lync 2013 :</span><span class="sxs-lookup"><span data-stu-id="e1511-116">For example, the Config.xml file in the following folder installs Lync 2013:</span></span>

  - <span data-ttu-id="e1511-117">\\\\\\partage serveur \\ Lync15 \\ Lync. WW \\Config.xml</span><span class="sxs-lookup"><span data-stu-id="e1511-117">\\\\server\\share\\Lync15\\Lync.WW \\Config.xml</span></span>

<span data-ttu-id="e1511-118">Le tableau suivant répertorie les éléments Config.xml les plus fréquemment utilisés pour l’installation de Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="e1511-118">The Config.xml elements most commonly used for Lync 2013 installation are listed in the following table.</span></span>

### <a name="configxml-elements"></a><span data-ttu-id="e1511-119">Éléments de Config.xml</span><span class="sxs-lookup"><span data-stu-id="e1511-119">Config.xml elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e1511-120">Élément</span><span class="sxs-lookup"><span data-stu-id="e1511-120">Element</span></span></th>
<th><span data-ttu-id="e1511-121">Description</span><span class="sxs-lookup"><span data-stu-id="e1511-121">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e1511-122">Configuration</span><span class="sxs-lookup"><span data-stu-id="e1511-122">Configuration</span></span></p></td>
<td><p><span data-ttu-id="e1511-123">Élément de niveau supérieur (obligatoire).</span><span class="sxs-lookup"><span data-stu-id="e1511-123">Top-level element (required).</span></span> <span data-ttu-id="e1511-124">Contient l’attribut Product, par exemple : Product = Lync</span><span class="sxs-lookup"><span data-stu-id="e1511-124">Contains the Product attribute, for example: Product=Lync</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e1511-125">OptionState</span><span class="sxs-lookup"><span data-stu-id="e1511-125">OptionState</span></span></p></td>
<td><p><span data-ttu-id="e1511-126">Spécifie la façon dont des fonctionnalités de produits spécifiques sont gérées lors de l’installation.</span><span class="sxs-lookup"><span data-stu-id="e1511-126">Specifies how specific product features are handled during installation.</span></span> <span data-ttu-id="e1511-127">Utilisez les attributs suivants pour empêcher l’installation de Business Connectivity Services, qui inclut les composants partagés qui interfèrent avec Outlook 2010 :</span><span class="sxs-lookup"><span data-stu-id="e1511-127">Use the following attributes to prevent installation of Business Connectivity Services, which includes shared components that interfere with Outlook 2010:</span></span></p>
<ul>
<li><p><span data-ttu-id="e1511-128">ID = &quot; LOBiMain&quot;</span><span class="sxs-lookup"><span data-stu-id="e1511-128">Id=&quot;LOBiMain&quot;</span></span></p></li>
<li><p><span data-ttu-id="e1511-129">État = &quot; absent&quot;</span><span class="sxs-lookup"><span data-stu-id="e1511-129">State=&quot;Absent&quot;</span></span></p></li>
<li><p><span data-ttu-id="e1511-130">Enfant = &quot; force&quot;</span><span class="sxs-lookup"><span data-stu-id="e1511-130">Children=&quot;Force&quot;</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e1511-131">Display</span><span class="sxs-lookup"><span data-stu-id="e1511-131">Display</span></span></p></td>
<td><p><span data-ttu-id="e1511-p105">Niveau d’interface utilisateur affiché pour l’utilisateur par le programme d’installation. Les attributs type sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="e1511-p105">The level of UI that Setup displays to the user. Typical attributes include the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="e1511-134">CompletionNotice = &quot; Oui &quot;  |  &quot; non &quot; (par défaut)</span><span class="sxs-lookup"><span data-stu-id="e1511-134">CompletionNotice=&quot;Yes&quot; | &quot;No&quot;(default)</span></span></p></li>
<li><p><span data-ttu-id="e1511-135">AcceptEULA = &quot; Oui &quot;  |  &quot; non &quot; (par défaut)</span><span class="sxs-lookup"><span data-stu-id="e1511-135">AcceptEula=&quot;Yes&quot; | &quot;No&quot;(default)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e1511-136">Journalisation</span><span class="sxs-lookup"><span data-stu-id="e1511-136">Logging</span></span></p></td>
<td><p><span data-ttu-id="e1511-p106">Options déterminant le type de journalisation mis en œuvre par le programme d’installation. Les attributs types sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="e1511-p106">Options for the kind of logging that Setup performs. Typical attributes include the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="e1511-139">Type = &quot; désactivé &quot;  |  &quot; standard &quot; (par défaut) | &quot; Détaillée&quot;</span><span class="sxs-lookup"><span data-stu-id="e1511-139">Type =&quot;Off&quot; | &quot;Standard&quot;(default) | &quot;Verbose&quot;</span></span></p></li>
<li><p><span data-ttu-id="e1511-140">Template=”filename.txt” (nom du fichier journal)</span><span class="sxs-lookup"><span data-stu-id="e1511-140">Template=”filename.txt” (the name of the log file)</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e1511-141">Paramètre</span><span class="sxs-lookup"><span data-stu-id="e1511-141">Setting</span></span></p></td>
<td><p><span data-ttu-id="e1511-p107">Spécifie les valeurs des propriétés de Windows Installer. Les attributs type sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="e1511-p107">Specifies values for Windows Installer properties. Typical attributes include the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="e1511-144">Définition &quot; de l’ID = nom &quot; (le nom de la propriété du programme d’installation de Windows)</span><span class="sxs-lookup"><span data-stu-id="e1511-144">Setting Id=&quot;name&quot; (the name of the Windows Installer property)</span></span></p></li>
<li><p><span data-ttu-id="e1511-145">Value = &quot; value &quot; (valeur à attribuer à la propriété)</span><span class="sxs-lookup"><span data-stu-id="e1511-145">Value=&quot;value&quot; (the value to assign to the property)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e1511-146">DistributionPoint</span><span class="sxs-lookup"><span data-stu-id="e1511-146">DistributionPoint</span></span></p></td>
<td><p><span data-ttu-id="e1511-p108">Chemin d’accès complet du point d’installation réseau à partir duquel l’installation doit s’exécuter. Comprend l’attribut Location :</span><span class="sxs-lookup"><span data-stu-id="e1511-p108">The fully qualified path of the network installation point from which the installation is to run. Includes the Location attribute:</span></span></p>
<ul>
<li><p><span data-ttu-id="e1511-149">Location=”path”</span><span class="sxs-lookup"><span data-stu-id="e1511-149">Location=”path”</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e1511-150">L’exemple suivant montre un fichier Config.xml pour une installation silencieuse classique de Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="e1511-150">The following example shows a Config.xml file for a typical silent installation of Lync 2013.</span></span>

    <Configuration Product="Lync">
      <OptionState Id="LOBiMain" State="Absent" Children="Force" />
      <Display Level="None" CompletionNotice="No" AcceptEula="Yes" />
      <Logging Type="verbose" Path="%temp%" Template="LyncSetupVerbose(*).log" />
      <Setting Id="SETUP_REBOOT" Value="Never" />
      <DistributionPoint Location="\\server\share\Lync15" />
    </Configuration>

<span data-ttu-id="e1511-151">Des informations détaillées sur l’utilisation du fichier Config.xml pour effectuer des tâches d’installation et de maintenance d’Office sont disponibles à l’adresse <https://go.microsoft.com/fwlink/p/?linkid=267514> .</span><span class="sxs-lookup"><span data-stu-id="e1511-151">Detailed information about using the Config.xml file to perform Office installation and maintenance tasks is available at <https://go.microsoft.com/fwlink/p/?linkid=267514>.</span></span>

<div>

## <a name="to-customize-the-configxml-file"></a><span data-ttu-id="e1511-152">Pour personnaliser le fichier Config.xml</span><span class="sxs-lookup"><span data-stu-id="e1511-152">To customize the Config.xml file</span></span>

1.  <span data-ttu-id="e1511-153">Ouvrez le fichier Config.xml avec un éditeur de texte, comme le Bloc-notes.</span><span class="sxs-lookup"><span data-stu-id="e1511-153">Open the Config.xml file by using a text editor tool, such as Notepad.</span></span>

2.  <span data-ttu-id="e1511-154">Recherchez les lignes qui contiennent les éléments à modifier.</span><span class="sxs-lookup"><span data-stu-id="e1511-154">Locate the lines that contain the elements you want to change.</span></span>

3.  <span data-ttu-id="e1511-155">Modifiez l’entrée de l’élément avec les options automatisées que vous voulez utiliser.</span><span class="sxs-lookup"><span data-stu-id="e1511-155">Modify the element entry with the silent options that you want to use.</span></span> <span data-ttu-id="e1511-156">Veillez à supprimer les séparateurs de commentaires, « \<\!--" and "--\> ».</span><span class="sxs-lookup"><span data-stu-id="e1511-156">Make sure that you remove the comment delimiters, "\<\!--" and "--\>".</span></span> <span data-ttu-id="e1511-157">Par exemple, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="e1511-157">For example, use the following syntax:</span></span>
    
        < DistributionPoint Location="\\server\share\Lync15" />

4.  <span data-ttu-id="e1511-158">Enregistrez le fichier Config.xml.</span><span class="sxs-lookup"><span data-stu-id="e1511-158">Save the Config.xml file.</span></span>

<span data-ttu-id="e1511-159"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e1511-159"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

