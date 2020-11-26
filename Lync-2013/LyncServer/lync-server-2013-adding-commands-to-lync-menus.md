---
title: 'Lync Server 2013 : ajout de commandes aux menus Lync'
description: 'Lync Server 2013 : ajout de commandes aux menus Lync.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Adding commands to Lync menus
ms:assetid: a8443bc2-e234-4022-870a-00700f38b1ea
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412788(v=OCS.15)
ms:contentKeyID: 48185091
ms.date: 04/11/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ed4d62d085eaf115d107244ae50a7cc69e0aacd5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439239"
---
# <a name="adding-commands-to-lync-menus-in-lync-server-2013"></a><span data-ttu-id="78bce-103">Ajouter des commandes aux menus Lync dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="78bce-103">Adding commands to Lync menus in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="78bce-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="78bce-104">

<span> </span></span></span>

<span data-ttu-id="78bce-105">_**Dernière modification de la rubrique :** 2016-04-11_</span><span class="sxs-lookup"><span data-stu-id="78bce-105">_**Topic Last Modified:** 2016-04-11_</span></span>

<span data-ttu-id="78bce-106">Vous pouvez ajouter des commandes personnalisées aux menus de Lync 2013 et transmettre l’URI (Uniform Resource Identifier) SIP de l’utilisateur actuel et des contacts sélectionnés à l’application qui démarre la commande personnalisée.</span><span class="sxs-lookup"><span data-stu-id="78bce-106">You can add custom commands to Lync 2013 menus and pass the SIP Uniform Resource Identifier (URI) of the current user and selected contacts to the application that the custom command starts.</span></span>

<span data-ttu-id="78bce-107">Les commandes personnalisées que vous ajoutez peuvent apparaître dans un ou plusieurs des menus suivants :</span><span class="sxs-lookup"><span data-stu-id="78bce-107">The custom commands that you add can appear on one or more of the following menus:</span></span>

  - <span data-ttu-id="78bce-108">Menu Outils, dans la barre de menus de la fenêtre principale de Lync</span><span class="sxs-lookup"><span data-stu-id="78bce-108">The Tools menu, on the menu bar in the Lync main window</span></span>

  - <span data-ttu-id="78bce-109">Menu contextuel des contacts de la liste de contacts</span><span class="sxs-lookup"><span data-stu-id="78bce-109">The shortcut menu for contacts in the Contacts list</span></span>

  - <span data-ttu-id="78bce-110">Menu autres options, dans la fenêtre de conversation</span><span class="sxs-lookup"><span data-stu-id="78bce-110">The More Options menu, in the Conversation window</span></span>

  - <span data-ttu-id="78bce-111">Menu contextuel pour les personnes figurant dans la liste des participants de la fenêtre de conversation</span><span class="sxs-lookup"><span data-stu-id="78bce-111">The shortcut menu for people listed in the Conversation window participant list</span></span>

  - <span data-ttu-id="78bce-112">Menu options dans une carte de visite</span><span class="sxs-lookup"><span data-stu-id="78bce-112">The options menu in a contact card</span></span>

<span data-ttu-id="78bce-113">Vous pouvez définir des commandes personnalisées pour deux types d’applications (applications qui effectuent l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="78bce-113">You can define custom commands for two types of applications—applications that do either of the following:</span></span>

  - <span data-ttu-id="78bce-114">S’applique uniquement à l’utilisateur actuel et est démarré sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="78bce-114">Apply only to the current user and are started on the local computer.</span></span>

  - <span data-ttu-id="78bce-115">Impliquez des utilisateurs supplémentaires, tels qu’un programme de collaboration en ligne, qui doivent être démarrés sur l’ordinateur de chaque utilisateur.</span><span class="sxs-lookup"><span data-stu-id="78bce-115">Involve additional users, such as an online collaboration program, and must be started on each user's computer.</span></span>

<span data-ttu-id="78bce-116">La commande personnalisée peut être appelée de l’une des façons suivantes :</span><span class="sxs-lookup"><span data-stu-id="78bce-116">The custom command can be invoked in the following ways:</span></span>

  - <span data-ttu-id="78bce-117">Sélectionnez un ou plusieurs utilisateurs, puis choisissez la commande personnalisée.</span><span class="sxs-lookup"><span data-stu-id="78bce-117">Select one or more users, and then choose the custom command.</span></span>

  - <span data-ttu-id="78bce-118">Démarrer une conversation à deux ou plusieurs parties, puis sélectionner la commande personnalisée.</span><span class="sxs-lookup"><span data-stu-id="78bce-118">Start a two-party or multiparty conversation, and then choose the custom command.</span></span>

<div>

## <a name="to-add-a-custom-command"></a><span data-ttu-id="78bce-119">Pour ajouter une commande personnalisée</span><span class="sxs-lookup"><span data-stu-id="78bce-119">To add a custom command</span></span>

<span data-ttu-id="78bce-120">Utilisez les paramètres de Registre du tableau suivant pour ajouter une commande aux menus.</span><span class="sxs-lookup"><span data-stu-id="78bce-120">Use the registry settings in the following table to add a command to the menus.</span></span> <span data-ttu-id="78bce-121">Ces entrées sont placées dans le registre à l’un des emplacements suivants :</span><span class="sxs-lookup"><span data-stu-id="78bce-121">These entries are placed in the registry at one of the following locations:</span></span>

  - <span data-ttu-id="78bce-122">Pour le système d’exploitation 32 bits : HKEY logiciel de l' \_ \_ ordinateur local \\ \\ Microsoft \\ Office \\ 15,0 des \\ \\ applications Lync sessionmanager \\</span><span class="sxs-lookup"><span data-stu-id="78bce-122">For 32bit OS: HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Office\\15.0\\Lync\\SessionManager\\Apps</span></span>

  - <span data-ttu-id="78bce-123">Pour les systèmes d’exploitation 64 bits : HKEY logiciel de l' \_ \_ ordinateur local \\ \\ Wow6432Node \\ Microsoft \\ Office \\ 15,0 \\ Lync \\ sessionmanager \\ apps</span><span class="sxs-lookup"><span data-stu-id="78bce-123">For 64bit OS: HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\Office\\15.0\\Lync\\SessionManager\\Apps</span></span>

### <a name="custom-command-registry-entries"></a><span data-ttu-id="78bce-124">Entrées de registre de commandes personnalisées</span><span class="sxs-lookup"><span data-stu-id="78bce-124">Custom Command Registry Entries</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="78bce-125">Nom</span><span class="sxs-lookup"><span data-stu-id="78bce-125">Name</span></span></th>
<th><span data-ttu-id="78bce-126">Type</span><span class="sxs-lookup"><span data-stu-id="78bce-126">Type</span></span></th>
<th><span data-ttu-id="78bce-127">Données</span><span class="sxs-lookup"><span data-stu-id="78bce-127">Data</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="78bce-128">Nom</span><span class="sxs-lookup"><span data-stu-id="78bce-128">Name</span></span></p></td>
<td><p><span data-ttu-id="78bce-129">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="78bce-129">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="78bce-130">Nom de l’application tel qu’il apparaît dans le menu.</span><span class="sxs-lookup"><span data-stu-id="78bce-130">Name of the application as it appears on the menu.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78bce-131">ApplicationType</span><span class="sxs-lookup"><span data-stu-id="78bce-131">ApplicationType</span></span></p></td>
<td><p><span data-ttu-id="78bce-132">INSÉRÉ</span><span class="sxs-lookup"><span data-stu-id="78bce-132">DWORD</span></span></p></td>
<td><p><span data-ttu-id="78bce-133">0 = exécutable (par défaut)</span><span class="sxs-lookup"><span data-stu-id="78bce-133">0 = Executable (default)</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="78bce-134">Nécessite ApplicationInstallPath.</span><span class="sxs-lookup"><span data-stu-id="78bce-134">Requires ApplicationInstallPath.</span></span>


</div>
<p><span data-ttu-id="78bce-135">1 = Protocole</span><span class="sxs-lookup"><span data-stu-id="78bce-135">1 = Protocol</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78bce-136">ApplicationInstallPath</span><span class="sxs-lookup"><span data-stu-id="78bce-136">ApplicationInstallPath</span></span></p></td>
<td><p><span data-ttu-id="78bce-137">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="78bce-137">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="78bce-138">Chemin d’accès complet du fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="78bce-138">Full path of the executable.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="78bce-139">Doit être spécifié si ApplicationType est défini sur 0 (exécutable).</span><span class="sxs-lookup"><span data-stu-id="78bce-139">Must be specified if ApplicationType is 0 (Executable).</span></span>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78bce-140"> Path</span><span class="sxs-lookup"><span data-stu-id="78bce-140">Path</span></span></p></td>
<td><p><span data-ttu-id="78bce-141">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="78bce-141">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="78bce-142">Chemin complet pour démarrer avec tout autre paramètre, y compris les paramètres par défaut <em>% User-ID%</em> et% <em>contact-ID%</em>.</span><span class="sxs-lookup"><span data-stu-id="78bce-142">Full path to be started along with any parameters, including the default parameters <em>%user-id%</em> and <em>%contact-id%</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78bce-143">SessionType</span><span class="sxs-lookup"><span data-stu-id="78bce-143">SessionType</span></span></p></td>
<td><p><span data-ttu-id="78bce-144">INSÉRÉ</span><span class="sxs-lookup"><span data-stu-id="78bce-144">DWORD</span></span></p></td>
<td><p><span data-ttu-id="78bce-145">0 = session locale.</span><span class="sxs-lookup"><span data-stu-id="78bce-145">0 = Local session.</span></span> <span data-ttu-id="78bce-146">L’application est démarrée sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="78bce-146">The application is started on the local computer.</span></span></p>
<p><span data-ttu-id="78bce-147">1 = session à deux parties (par défaut).</span><span class="sxs-lookup"><span data-stu-id="78bce-147">1 = Two-party session (default).</span></span> <span data-ttu-id="78bce-148">Lync 2013 démarre l’application localement, puis envoie une notification de bureau à l’autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="78bce-148">Lync 2013 starts the application locally and then sends a desktop notification to the other user.</span></span> <span data-ttu-id="78bce-149">L’autre utilisateur clique sur la notification pour démarrer l’application sur son ordinateur.</span><span class="sxs-lookup"><span data-stu-id="78bce-149">The other user clicks the notification to start the application on their computer.</span></span></p>
<p><span data-ttu-id="78bce-150">2 = session multipartie.</span><span class="sxs-lookup"><span data-stu-id="78bce-150">2 = Multiparty session.</span></span> <span data-ttu-id="78bce-151">Lync 2013 démarre l’application localement, puis envoie des notifications de bureau aux autres utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="78bce-151">Lync 2013 starts the application locally and then sends desktop notifications to the other users.</span></span> <span data-ttu-id="78bce-152">L’autre utilisateur clique sur la notification pour démarrer l’application spécifiée sur son ordinateur.</span><span class="sxs-lookup"><span data-stu-id="78bce-152">The other user clicks the notification to start the specified application on their computer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78bce-153">ExtensibleMenu</span><span class="sxs-lookup"><span data-stu-id="78bce-153">ExtensibleMenu</span></span></p></td>
<td><p><span data-ttu-id="78bce-154">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="78bce-154">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="78bce-155">Liste des menus dans lesquels cette commande s’affiche, en les séparant par un point-virgule.</span><span class="sxs-lookup"><span data-stu-id="78bce-155">A list of the menus where this command will appear, separated by semicolons.</span></span> <span data-ttu-id="78bce-156">Valeurs possibles :</span><span class="sxs-lookup"><span data-stu-id="78bce-156">Possible values are:</span></span></p>
<p><span data-ttu-id="78bce-157">MainWindowActions</span><span class="sxs-lookup"><span data-stu-id="78bce-157">MainWindowActions</span></span></p>
<p><span data-ttu-id="78bce-158">MainWindowRightClick</span><span class="sxs-lookup"><span data-stu-id="78bce-158">MainWindowRightClick</span></span></p>
<p><span data-ttu-id="78bce-159">ConversationWindowActions</span><span class="sxs-lookup"><span data-stu-id="78bce-159">ConversationWindowActions</span></span></p>
<p><span data-ttu-id="78bce-160">ConversationWindowRightClick</span><span class="sxs-lookup"><span data-stu-id="78bce-160">ConversationWindowRightClick</span></span></p>
<p><span data-ttu-id="78bce-161">ContactCardMenu</span><span class="sxs-lookup"><span data-stu-id="78bce-161">ContactCardMenu</span></span></p>
<p><span data-ttu-id="78bce-162">Si ExtensibleMenu n’est pas défini, les valeurs par défaut de MainWindowRightClick et ConversationWindowActions sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="78bce-162">If ExtensibleMenu is not defined, the default values of MainWindowRightClick and ConversationWindowActions are used.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="78bce-163">Par exemple, l’éditeur du Registre suivant (. REG) affiche les résultats de l’ajout d’un élément de menu du gestionnaire de contacts commerciaux contoso au menu actions dans la fenêtre de conversation :</span><span class="sxs-lookup"><span data-stu-id="78bce-163">For example, the following Registry Editor (.REG) file shows the results of adding a Contoso Sales Contact Manager menu item to Actions menu in the Conversation window:</span></span>

    Windows Registry Editor Version 5.00
    [HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\15.0\Lync\SessionManager\Apps\{1F9F07C6-7E0B-462B-AAD7-98C6DBEA8F69}]
    "Name"="Contoso Sales Contact Manager"
    "HelpMessage"="The Contoso Sales Contact Manager is not installed. Contact the Help Desk for more information."
    "ApplicationType"=dword:00000000
    "ApplicationInstallPath"="C:\\cscm.exe"
    "Path"="C:\\cscm.exe %user-id% %contact-id%"
    "SessionType"=dword:00000001
    "ExtensibleMenu"="ConversationWindowActions;MainWindowRightClick"

</div>

<div>

## <a name="to-access-a-custom-command"></a><span data-ttu-id="78bce-164">Pour accéder à une commande personnalisée</span><span class="sxs-lookup"><span data-stu-id="78bce-164">To access a custom command</span></span>

<span data-ttu-id="78bce-165">Pour accéder à une commande personnalisée après l’avoir ajoutée, effectuez l’une des opérations suivantes, en fonction des valeurs ExtensibleMenu que vous définissez :</span><span class="sxs-lookup"><span data-stu-id="78bce-165">To access a custom command after it is added, do one of the following, depending on the ExtensibleMenu values that you define:</span></span>

  - <span data-ttu-id="78bce-166">**MainWindowActions**   Dans la fenêtre principale de Lync, cliquez sur **Outils**, puis sur votre commande personnalisée.</span><span class="sxs-lookup"><span data-stu-id="78bce-166">**MainWindowActions**   In the Lync main window, click **Tools**, and then click your custom command.</span></span>

  - <span data-ttu-id="78bce-167">**MainWindowRightClick**   Dans la fenêtre principale de Lync, cliquez avec le bouton droit sur un contact, puis cliquez sur votre commande personnalisée.</span><span class="sxs-lookup"><span data-stu-id="78bce-167">**MainWindowRightClick**   In the Lync main window, right-click a contact, and then click your custom command.</span></span>

  - <span data-ttu-id="78bce-168">**ConversationWindowActions**   Dans la fenêtre de conversation, cliquez sur l’icône **plus d’options** , puis cliquez sur votre commande personnalisée.</span><span class="sxs-lookup"><span data-stu-id="78bce-168">**ConversationWindowActions**   In the Conversation window, click the **More Options** icon, and then click your custom command.</span></span>

  - <span data-ttu-id="78bce-169">**ConversationWindowRightClick**   Dans la fenêtre de conversation, cliquez avec le bouton droit sur le nom d’un contact, puis cliquez sur votre commande personnalisée.</span><span class="sxs-lookup"><span data-stu-id="78bce-169">**ConversationWindowRightClick**   In the Conversation window, right-click a contact name, and then click your custom command.</span></span>

<span data-ttu-id="78bce-170"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="78bce-170"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

