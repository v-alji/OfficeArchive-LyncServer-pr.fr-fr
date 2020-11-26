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
# <a name="using-configxml-to-perform-installation-tasks-in-lync-server-2013"></a>Utilisation de Config.xml pour effectuer des tâches d’installation dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2012-10-02_

Même si l’outil de personnalisation Office est le principal outil pour l’installation personnalisée, les administrateurs peuvent utiliser le fichier Config.xml pour spécifier des instructions d’installation non disponibles dans cet outil. Les personnalisations ci-dessous ne peuvent être effectuées qu’avec le fichier Config.xml :

  - Spécifiez le chemin d’accès au point d’installation réseau.

  - Sélectionnez les produits à installer.

  - Configurez la journalisation et l’emplacement du fichier de personnalisation de l’installation et les mises à jour des logiciels.

  - Spécifiez les options d’installation, comme le nom d’utilisateur.

  - Copiez la source d’installation locale sur l’ordinateur de l’utilisateur sans installer Office.

  - Ajoutez ou supprimez des langues dans l’installation.

Nous vous recommandons d’utiliser le fichier Config.xml pour configurer l’installation silencieuse de Lync 2013.

Par défaut, le fichier Config.xml stocké dans le dossier de produit principal (par exemple, \\ produit. WW) envoie le programme d’installation de ce produit. Par exemple, le fichier Config.xml dans le dossier suivant installe Lync 2013 :

  - \\\\\\partage serveur \\ Lync15 \\ Lync. WW \\Config.xml

Le tableau suivant répertorie les éléments Config.xml les plus fréquemment utilisés pour l’installation de Lync 2013.

### <a name="configxml-elements"></a>Éléments de Config.xml

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Élément</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Configuration</p></td>
<td><p>Élément de niveau supérieur (obligatoire). Contient l’attribut Product, par exemple : Product = Lync</p></td>
</tr>
<tr class="even">
<td><p>OptionState</p></td>
<td><p>Spécifie la façon dont des fonctionnalités de produits spécifiques sont gérées lors de l’installation. Utilisez les attributs suivants pour empêcher l’installation de Business Connectivity Services, qui inclut les composants partagés qui interfèrent avec Outlook 2010 :</p>
<ul>
<li><p>ID = &quot; LOBiMain&quot;</p></li>
<li><p>État = &quot; absent&quot;</p></li>
<li><p>Enfant = &quot; force&quot;</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>Display</p></td>
<td><p>Niveau d’interface utilisateur affiché pour l’utilisateur par le programme d’installation. Les attributs type sont les suivants :</p>
<ul>
<li><p>CompletionNotice = &quot; Oui &quot;  |  &quot; non &quot; (par défaut)</p></li>
<li><p>AcceptEULA = &quot; Oui &quot;  |  &quot; non &quot; (par défaut)</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>Journalisation</p></td>
<td><p>Options déterminant le type de journalisation mis en œuvre par le programme d’installation. Les attributs types sont les suivants :</p>
<ul>
<li><p>Type = &quot; désactivé &quot;  |  &quot; standard &quot; (par défaut) | &quot; Détaillée&quot;</p></li>
<li><p>Template=”filename.txt” (nom du fichier journal)</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>Paramètre</p></td>
<td><p>Spécifie les valeurs des propriétés de Windows Installer. Les attributs type sont les suivants :</p>
<ul>
<li><p>Définition &quot; de l’ID = nom &quot; (le nom de la propriété du programme d’installation de Windows)</p></li>
<li><p>Value = &quot; value &quot; (valeur à attribuer à la propriété)</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>DistributionPoint</p></td>
<td><p>Chemin d’accès complet du point d’installation réseau à partir duquel l’installation doit s’exécuter. Comprend l’attribut Location :</p>
<ul>
<li><p>Location=”path”</p></li>
</ul></td>
</tr>
</tbody>
</table>


L’exemple suivant montre un fichier Config.xml pour une installation silencieuse classique de Lync 2013.

    <Configuration Product="Lync">
      <OptionState Id="LOBiMain" State="Absent" Children="Force" />
      <Display Level="None" CompletionNotice="No" AcceptEula="Yes" />
      <Logging Type="verbose" Path="%temp%" Template="LyncSetupVerbose(*).log" />
      <Setting Id="SETUP_REBOOT" Value="Never" />
      <DistributionPoint Location="\\server\share\Lync15" />
    </Configuration>

Des informations détaillées sur l’utilisation du fichier Config.xml pour effectuer des tâches d’installation et de maintenance d’Office sont disponibles à l’adresse <https://go.microsoft.com/fwlink/p/?linkid=267514> .

<div>

## <a name="to-customize-the-configxml-file"></a>Pour personnaliser le fichier Config.xml

1.  Ouvrez le fichier Config.xml avec un éditeur de texte, comme le Bloc-notes.

2.  Recherchez les lignes qui contiennent les éléments à modifier.

3.  Modifiez l’entrée de l’élément avec les options automatisées que vous voulez utiliser. Veillez à supprimer les séparateurs de commentaires, « \<\!--" and "--\> ». Par exemple, utilisez la syntaxe suivante :
    
        < DistributionPoint Location="\\server\share\Lync15" />

4.  Enregistrez le fichier Config.xml.

</div>

</div>

<span> </span>

</div>

</div>

</div>

