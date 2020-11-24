---
title: Intégration d’une application de collaboration tierce avec Lync
description: Intégration d’une application de collaboration tierce avec Lync.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Integrating a third-party collaboration application with Lync
ms:assetid: 00b9312c-b0c8-4f79-8b76-05b2d820e197
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398068(v=OCS.15)
ms:contentKeyID: 48183224
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7adbe1abab83a569f581af034fc46abfef4cf819
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395093"
---
# <a name="integrating-a-third-party-collaboration-application-with-lync-server-2013"></a><span data-ttu-id="e7ce5-103">Intégration d’une application de collaboration tierce avec Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e7ce5-103">Integrating a third-party collaboration application with Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e7ce5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e7ce5-104">

<span> </span></span></span>

<span data-ttu-id="e7ce5-105">_**Dernière modification de la rubrique :** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="e7ce5-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="e7ce5-106">Vous pouvez intégrer Lync 2013 à toute application de collaboration en ligne tierce en ajoutant des informations sur l’application au registre.</span><span class="sxs-lookup"><span data-stu-id="e7ce5-106">You can integrate Lync 2013 with any third-party online collaboration application by adding information about the application to the registry.</span></span> <span data-ttu-id="e7ce5-107">Vous pouvez utiliser Lync 2013 pour démarrer des sessions de conférence de données hébergées sur un serveur interne, un service basé sur Internet, ou les deux.</span><span class="sxs-lookup"><span data-stu-id="e7ce5-107">You can use Lync 2013 to start data conferencing sessions hosted on an in-house server, an Internet-based service, or both.</span></span> <span data-ttu-id="e7ce5-108">La session de collaboration ou de conférence de données peut être démarrée à partir de la liste de contacts ou à partir d’une conversation par messagerie instantanée, audio ou vidéo.</span><span class="sxs-lookup"><span data-stu-id="e7ce5-108">The collaboration or data conferencing session can be started from the Contacts list or from an existing instant messaging, voice, or video session.</span></span> <span data-ttu-id="e7ce5-109">Lync 2013 agit uniquement comme véhicule pour le démarrage de l’application.</span><span class="sxs-lookup"><span data-stu-id="e7ce5-109">Lync 2013 acts only as the vehicle for starting the application.</span></span> <span data-ttu-id="e7ce5-110">Toutes les conversations Lync 2013 existantes restent actives après le démarrage de la session de collaboration en ligne.</span><span class="sxs-lookup"><span data-stu-id="e7ce5-110">Any existing Lync 2013 conversations remain active after the online collaboration session has begun.</span></span>

<span data-ttu-id="e7ce5-111">Les sections suivantes décrivent comment intégrer Lync 2013 aux applications de collaboration basées sur Internet et celles basées sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="e7ce5-111">The following sections describe how to integrate Lync 2013 with Internet-based and server-based collaboration applications.</span></span>

<div>

## <a name="integrating-an-internet-based-collaboration-application-with-lync-2013"></a><span data-ttu-id="e7ce5-112">Intégration d’une application de collaboration Internet-Based avec Lync 2013</span><span class="sxs-lookup"><span data-stu-id="e7ce5-112">Integrating an Internet-Based Collaboration Application with Lync 2013</span></span>

<span data-ttu-id="e7ce5-113">En règle générale, les étapes nécessaires à l’intégration d’une application de collaboration tierce sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="e7ce5-113">Generally, the steps involved in integrating a third-party collaboration application are as follows:</span></span>

1.  <span data-ttu-id="e7ce5-114">Des informations sur l’application sont ajoutées au registre.</span><span class="sxs-lookup"><span data-stu-id="e7ce5-114">Information about the application is added to the registry.</span></span>

2.  <span data-ttu-id="e7ce5-115">L’organisateur se connecte à Lync 2013 et sélectionne les contacts pour le partage et la collaboration de données.</span><span class="sxs-lookup"><span data-stu-id="e7ce5-115">The organizer signs in to Lync 2013 and selects contacts for data sharing and collaboration.</span></span> <span data-ttu-id="e7ce5-116">Il est possible que l’organisateur se trouve déjà dans une conversation et décide d’ajouter des conférences de données.</span><span class="sxs-lookup"><span data-stu-id="e7ce5-116">Or, the organizer may already be in a conversation and decide to add data conferencing.</span></span>

3.  <span data-ttu-id="e7ce5-117">Lync 2013 lit le registre, démarre l’application de collaboration, puis envoie un message SIP personnalisé (appINVITE) aux participants sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="e7ce5-117">Lync 2013 reads the registry, starts the collaboration application, and then sends a custom SIP message—an appINVITE—to the selected participants.</span></span>

4.  <span data-ttu-id="e7ce5-118">Les participants acceptent l’invitation et l’application de collaboration est démarrée sur l’ordinateur de chaque personne.</span><span class="sxs-lookup"><span data-stu-id="e7ce5-118">Participants accept the invitation, and the collaboration application is started on each person’s computer.</span></span> <span data-ttu-id="e7ce5-119">Lync 2013 utilise le registre pour déterminer quelle application de collaboration utiliser, puis démarre cette application en utilisant les paramètres inclus dans le message appINVITE.</span><span class="sxs-lookup"><span data-stu-id="e7ce5-119">Lync 2013 uses the registry to determine which collaboration application to use, and then starts that application by using the parameters included in the appINVITE message.</span></span>

<span data-ttu-id="e7ce5-120">Le tableau suivant décrit les entrées de Registre requises pour intégrer une application de collaboration basée sur Internet avec Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="e7ce5-120">The following table describes the registry entries required to integrate an Internet-based collaboration application with Lync 2013.</span></span> <span data-ttu-id="e7ce5-121">Ces entrées sont placées dans le registre à l’emplacement suivant :</span><span class="sxs-lookup"><span data-stu-id="e7ce5-121">These entries are placed in the registry in the following location:</span></span>

  - <span data-ttu-id="e7ce5-122">HKEY \_ logiciel de l' \_ ordinateur local \\ \\ Microsoft \\ Office 15,0 les paramètres des \\ \\ \\ applications Lync sessionmanager \\ \\</span><span class="sxs-lookup"><span data-stu-id="e7ce5-122">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Office\\15.0\\Lync\\SessionManager\\Apps\\Parameters</span></span>

### <a name="registry-entries-for-an-internet-based-collaboration-application"></a><span data-ttu-id="e7ce5-123">Entrées de Registre pour une application de collaboration basée sur Internet</span><span class="sxs-lookup"><span data-stu-id="e7ce5-123">Registry Entries for an Internet-based Collaboration Application</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e7ce5-124">Nom</span><span class="sxs-lookup"><span data-stu-id="e7ce5-124">Name</span></span></th>
<th><span data-ttu-id="e7ce5-125">Type</span><span class="sxs-lookup"><span data-stu-id="e7ce5-125">Type</span></span></th>
<th><span data-ttu-id="e7ce5-126">Données</span><span class="sxs-lookup"><span data-stu-id="e7ce5-126">Data</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e7ce5-127">Nom</span><span class="sxs-lookup"><span data-stu-id="e7ce5-127">Name</span></span></p></td>
<td><p><span data-ttu-id="e7ce5-128">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="e7ce5-128">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="e7ce5-129">Nom de l’application pour les menus Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="e7ce5-129">The application name for Lync 2013 menus.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7ce5-130">SmallIcon</span><span class="sxs-lookup"><span data-stu-id="e7ce5-130">SmallIcon</span></span></p></td>
<td><p><span data-ttu-id="e7ce5-131">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="e7ce5-131">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="e7ce5-132">Chemin d’accès à l’icône 16 pixels x 16 pixels, BMP ou PNG.</span><span class="sxs-lookup"><span data-stu-id="e7ce5-132">Path to 16-pixel x 16-pixel icon, BMP or PNG.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7ce5-133"> Path</span><span class="sxs-lookup"><span data-stu-id="e7ce5-133">Path</span></span></p></td>
<td><p><span data-ttu-id="e7ce5-134">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="e7ce5-134">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="e7ce5-135">Chemin du participant pour le démarrage de l’application de collaboration en ligne.</span><span class="sxs-lookup"><span data-stu-id="e7ce5-135">Participant path for starting the online collaboration application.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7ce5-136">OriginatorPath</span><span class="sxs-lookup"><span data-stu-id="e7ce5-136">OriginatorPath</span></span></p></td>
<td><p><span data-ttu-id="e7ce5-137">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="e7ce5-137">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="e7ce5-138">Chemin d’accès de l’organisateur du démarrage de l’application de collaboration en ligne.</span><span class="sxs-lookup"><span data-stu-id="e7ce5-138">Organizer path for starting the online collaboration application.</span></span> <span data-ttu-id="e7ce5-139">Ce chemin peut contenir un ou plusieurs paramètres personnalisés tels qu’ils sont définis dans la sous-clé paramètres.</span><span class="sxs-lookup"><span data-stu-id="e7ce5-139">This path can contain one or more custom parameters as defined in the Parameters subkey.</span></span> <span data-ttu-id="e7ce5-140">Par exemple, <code>https://meetserv.adatum.com/cc/%param1%/join?id=%param2%&amp;role=present&amp;pw=%param3%</code></span><span class="sxs-lookup"><span data-stu-id="e7ce5-140">For example, <code>https://meetserv.adatum.com/cc/%param1%/join?id=%param2%&amp;role=present&amp;pw=%param3%</code></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7ce5-141">SessionType</span><span class="sxs-lookup"><span data-stu-id="e7ce5-141">SessionType</span></span></p></td>
<td><p><span data-ttu-id="e7ce5-142">INSÉRÉ</span><span class="sxs-lookup"><span data-stu-id="e7ce5-142">DWORD</span></span></p></td>
<td><p><span data-ttu-id="e7ce5-143">0 = session locale.</span><span class="sxs-lookup"><span data-stu-id="e7ce5-143">0 = Local session.</span></span> <span data-ttu-id="e7ce5-144">L’application est démarrée sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="e7ce5-144">The application is started on the local computer.</span></span></p>
<p><span data-ttu-id="e7ce5-145">1 = session à deux parties (par défaut).</span><span class="sxs-lookup"><span data-stu-id="e7ce5-145">1 = Two-party session (default).</span></span> <span data-ttu-id="e7ce5-146">Lync 2013 démarre l’application localement, puis envoie une notification système à l’autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e7ce5-146">Lync 2013 starts the application locally, and then sends a system notification to the other user.</span></span> <span data-ttu-id="e7ce5-147">L’autre utilisateur clique sur la notification et démarre l’application spécifiée sur son ordinateur.</span><span class="sxs-lookup"><span data-stu-id="e7ce5-147">The other user clicks the notification and starts the specified application on their computer.</span></span></p>
<p><span data-ttu-id="e7ce5-148">2 = session multipartie.</span><span class="sxs-lookup"><span data-stu-id="e7ce5-148">2 = Multiparty session.</span></span> <span data-ttu-id="e7ce5-149">Lync 2013 démarre l’application localement, puis envoie des notifications système aux autres utilisateurs, en leur demandant de démarrer l’application spécifiée sur leur ordinateur.</span><span class="sxs-lookup"><span data-stu-id="e7ce5-149">Lync 2013 starts the application locally, and then sends system notifications to the other users, prompting them to start the specified application on their own computer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7ce5-150">ExensibleMenu</span><span class="sxs-lookup"><span data-stu-id="e7ce5-150">ExensibleMenu</span></span></p></td>
<td><p><span data-ttu-id="e7ce5-151">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="e7ce5-151">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="e7ce5-152">Liste des menus dans lesquels cette commande s’affiche, séparés par des points-virgules.</span><span class="sxs-lookup"><span data-stu-id="e7ce5-152">A list of the menus where this command will appear, separated by semi-colons.</span></span> <span data-ttu-id="e7ce5-153">Valeurs possibles :</span><span class="sxs-lookup"><span data-stu-id="e7ce5-153">Possible values are:</span></span></p>
<ul>
<li><p><span data-ttu-id="e7ce5-154">MainWindowActions</span><span class="sxs-lookup"><span data-stu-id="e7ce5-154">MainWindowActions</span></span></p></li>
<li><p><span data-ttu-id="e7ce5-155">MainWindowRightClick</span><span class="sxs-lookup"><span data-stu-id="e7ce5-155">MainWindowRightClick</span></span></p></li>
<li><p><span data-ttu-id="e7ce5-156">ConversationWindowActions</span><span class="sxs-lookup"><span data-stu-id="e7ce5-156">ConversationWindowActions</span></span></p></li>
<li><p><span data-ttu-id="e7ce5-157">ConversationWindowButton</span><span class="sxs-lookup"><span data-stu-id="e7ce5-157">ConversationWindowButton</span></span></p></li>
<li><p><span data-ttu-id="e7ce5-158">ConversationWindowRightClick</span><span class="sxs-lookup"><span data-stu-id="e7ce5-158">ConversationWindowRightClick</span></span></p></li>
</ul>
<p><span data-ttu-id="e7ce5-159">Si ExtensibleMenu n’est pas défini, les valeurs par défaut de MainWindowRightClick et ConversationWindowActions sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="e7ce5-159">If ExtensibleMenu is not defined, the default values of MainWindowRightClick and ConversationWindowActions are used.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e7ce5-160">Le tableau suivant décrit les entrées de Registre correspondant aux paramètres.</span><span class="sxs-lookup"><span data-stu-id="e7ce5-160">The following table describes the registry entries for parameters.</span></span> <span data-ttu-id="e7ce5-161">Ces entrées sont placées sur HKEY logiciel de l' \_ \_ utilisateur actuel \\ \\ Microsoft \\ Office \\ 15,0 les paramètres des \\ \\ applications Lync sessionmanager \\ \\ .</span><span class="sxs-lookup"><span data-stu-id="e7ce5-161">These entries are place at HKEY\_CURRENT\_USER\\Software\\Microsoft\\Office\\15.0\\Lync\\SessionManager\\Apps\\Parameters.</span></span>

### <a name="registry-entries-for-an-internet-based-collaboration-application"></a><span data-ttu-id="e7ce5-162">Entrées de Registre pour une application de collaboration basée sur Internet</span><span class="sxs-lookup"><span data-stu-id="e7ce5-162">Registry Entries for an Internet-based Collaboration Application</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e7ce5-163">Nom</span><span class="sxs-lookup"><span data-stu-id="e7ce5-163">Name</span></span></th>
<th><span data-ttu-id="e7ce5-164">Type</span><span class="sxs-lookup"><span data-stu-id="e7ce5-164">Type</span></span></th>
<th><span data-ttu-id="e7ce5-165">Données</span><span class="sxs-lookup"><span data-stu-id="e7ce5-165">Data</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e7ce5-166">TypeDonnées</span><span class="sxs-lookup"><span data-stu-id="e7ce5-166">Param1</span></span></p></td>
<td><p><span data-ttu-id="e7ce5-167">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="e7ce5-167">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="e7ce5-168">Permet d' <code>%Parm1%</code> Ajouter des valeurs spécifiques à l’utilisateur dans la clé de Registre OriginatorPath.</span><span class="sxs-lookup"><span data-stu-id="e7ce5-168">Used in tokenized format (<code>%Parm1%</code>) to add user-specific values to the OriginatorPath registry key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7ce5-169">TypeDonnées</span><span class="sxs-lookup"><span data-stu-id="e7ce5-169">Param2</span></span></p></td>
<td><p><span data-ttu-id="e7ce5-170">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="e7ce5-170">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="e7ce5-171">Voir Param1.</span><span class="sxs-lookup"><span data-stu-id="e7ce5-171">See Param1.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7ce5-172">Param3</span><span class="sxs-lookup"><span data-stu-id="e7ce5-172">Param3</span></span></p></td>
<td><p><span data-ttu-id="e7ce5-173">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="e7ce5-173">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="e7ce5-174">Voir Param1.</span><span class="sxs-lookup"><span data-stu-id="e7ce5-174">See Param1.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e7ce5-175">Les exemples de paramètres de registre suivants intègrent le client de collaboration adatum avec Lync 2013 :</span><span class="sxs-lookup"><span data-stu-id="e7ce5-175">The following example registry settings integrate ADatum Collaboration Client with Lync 2013:</span></span>

    Windows Registry Editor Version 5.00
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Lync\SessionManager]
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Lync\SessionManager\Apps]
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Lync\SessionManager\Apps\{C3F6E17A-855F-44a0-B90D-C0B92D38E5F1}]
    "Path"="https://meetingservice.adatum.com/cc/%param1%/meet/%param2%"
    "OriginatorPath"="https://meetserv.adatum.com/cc/%param1%/join?id=%param2%&role=present&pw=%param3%"
    "SessionType"=dword:00000002
    "ApplicationType"=dword:00000001
    "LiveServerIntegration"=dword:00000000
    "Name"="ADatum Online Collaboration Service"
    "Extensiblemenu"="MainWindowActions;MainWindowRightClick;ConversationWindowActions;ConversationWindowRightClick"
    
    [HKEY_CURRENT_USER\Software\Microsoft\Office\15.0\Lync\SessionManager]
    [HKEY_CURRENT_USER\Software\Microsoft\Office\15.0\Lync\SessionManager\Apps]
    [HKEY_CURRENT_USER\Software\Microsoft\Office\15.0\Lync\SessionManager\Apps\Parameters]
    [HKEY_CURRENT_USER\Software\Microsoft\Office\15.0\Lync\SessionManager\Apps\Parameters\{C3F6E17A-855F-44a0-B90D-C0B92D38E5F1}]
    "Param1"="meetserv"
    "Param2"="admin"
    "Param3"="abcdefg123"

</div>

<div>

## <a name="integrating-a-server-based-collaboration-application-with-lync-2013"></a><span data-ttu-id="e7ce5-176">Intégration d’une application de collaboration Server-Based avec Lync 2013</span><span class="sxs-lookup"><span data-stu-id="e7ce5-176">Integrating a Server-Based Collaboration Application with Lync 2013</span></span>

<span data-ttu-id="e7ce5-177">Les paramètres pour ajouter des commandes pour le démarrage d’une application de collaboration serveur à partir de Lync 2013 sont similaires à ceux décrits dans la section précédente, intégration d’une application de collaboration Internet-Based avec Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="e7ce5-177">The settings to add commands for starting a server-based collaboration application from within Lync 2013 are similar to those described in the previous section, Integrating an Internet-Based Collaboration Application with Lync 2013.</span></span> <span data-ttu-id="e7ce5-178">Toutefois, le OriginatorPath n’est pas obligatoire et certaines valeurs sont modifiées.</span><span class="sxs-lookup"><span data-stu-id="e7ce5-178">However, the OriginatorPath is not required, and some values are changed.</span></span> <span data-ttu-id="e7ce5-179">Les entrées de Registre sont placées à l’emplacement suivant :</span><span class="sxs-lookup"><span data-stu-id="e7ce5-179">Registry entries are placed in the following location:</span></span>

  - <span data-ttu-id="e7ce5-180">HKEY \_ logiciel de l' \_ ordinateur local \\ \\ Microsoft \\ Office 15,0 les paramètres des \\ \\ \\ applications Lync sessionmanager \\ \\</span><span class="sxs-lookup"><span data-stu-id="e7ce5-180">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Office\\15.0\\Lync\\SessionManager\\Apps\\Parameters</span></span>

### <a name="registry-entries-for-a-server-based-collaboration-application"></a><span data-ttu-id="e7ce5-181">Entrées de Registre pour une application de collaboration basée sur le serveur</span><span class="sxs-lookup"><span data-stu-id="e7ce5-181">Registry Entries for a Server-based Collaboration Application</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e7ce5-182">Nom</span><span class="sxs-lookup"><span data-stu-id="e7ce5-182">Name</span></span></th>
<th><span data-ttu-id="e7ce5-183">Type</span><span class="sxs-lookup"><span data-stu-id="e7ce5-183">Type</span></span></th>
<th><span data-ttu-id="e7ce5-184">Données</span><span class="sxs-lookup"><span data-stu-id="e7ce5-184">Data</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e7ce5-185">Nom</span><span class="sxs-lookup"><span data-stu-id="e7ce5-185">Name</span></span></p></td>
<td><p><span data-ttu-id="e7ce5-186">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="e7ce5-186">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="e7ce5-187">Nom de l’application tel qu’il apparaît dans le menu.</span><span class="sxs-lookup"><span data-stu-id="e7ce5-187">Name of the application as it appears on the menu.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7ce5-188">ApplicationType</span><span class="sxs-lookup"><span data-stu-id="e7ce5-188">ApplicationType</span></span></p></td>
<td><p><span data-ttu-id="e7ce5-189">INSÉRÉ</span><span class="sxs-lookup"><span data-stu-id="e7ce5-189">DWORD</span></span></p></td>
<td><p><span data-ttu-id="e7ce5-190">Valeur = 1.</span><span class="sxs-lookup"><span data-stu-id="e7ce5-190">Value = 1.</span></span> <span data-ttu-id="e7ce5-191">Définit le type d’application sur protocole.</span><span class="sxs-lookup"><span data-stu-id="e7ce5-191">Sets the application type to protocol.</span></span> <span data-ttu-id="e7ce5-192">Les autres valeurs possibles ne s’appliquent pas dans le cas présent.</span><span class="sxs-lookup"><span data-stu-id="e7ce5-192">The other possible values do not apply in this case.</span></span> <span data-ttu-id="e7ce5-193">Si ce n’est pas le cas, ApplicationType est défini sur 0 (exécutable).</span><span class="sxs-lookup"><span data-stu-id="e7ce5-193">If not present, ApplicationType is set to 0 (executable).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7ce5-194"> Path</span><span class="sxs-lookup"><span data-stu-id="e7ce5-194">Path</span></span></p></td>
<td><p><span data-ttu-id="e7ce5-195">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="e7ce5-195">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="e7ce5-196">Protocole utilisé pour démarrer l’application de collaboration.</span><span class="sxs-lookup"><span data-stu-id="e7ce5-196">Protocol used to start the collaboration application.</span></span> <span data-ttu-id="e7ce5-197">Pour Live Meeting 2007, la valeur de path est définie sur <code>meet:%conf-uri%</code> .</span><span class="sxs-lookup"><span data-stu-id="e7ce5-197">For Live Meeting 2007, the value of Path is set to <code>meet:%conf-uri%</code>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7ce5-198">SessionType</span><span class="sxs-lookup"><span data-stu-id="e7ce5-198">SessionType</span></span></p></td>
<td><p><span data-ttu-id="e7ce5-199">INSÉRÉ</span><span class="sxs-lookup"><span data-stu-id="e7ce5-199">DWORD</span></span></p></td>
<td><p><span data-ttu-id="e7ce5-200">0 = session locale.</span><span class="sxs-lookup"><span data-stu-id="e7ce5-200">0 = Local session.</span></span> <span data-ttu-id="e7ce5-201">L’application est démarrée sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="e7ce5-201">The application is started on the local computer.</span></span></p>
<p><span data-ttu-id="e7ce5-202">1 = session à deux parties (par défaut).</span><span class="sxs-lookup"><span data-stu-id="e7ce5-202">1 = Two-party session (default).</span></span> <span data-ttu-id="e7ce5-203">Lync 2013 démarre l’application localement, puis envoie une notification système à l’autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e7ce5-203">Lync 2013 starts the application locally, and then sends a system notification to the other user.</span></span> <span data-ttu-id="e7ce5-204">L’autre utilisateur clique sur la notification et démarre l’application spécifiée sur son ordinateur.</span><span class="sxs-lookup"><span data-stu-id="e7ce5-204">The other user clicks the notification and starts the specified application on their computer.</span></span></p>
<p><span data-ttu-id="e7ce5-205">2 = session multipartie.</span><span class="sxs-lookup"><span data-stu-id="e7ce5-205">2 = Multiparty session.</span></span> <span data-ttu-id="e7ce5-206">Lync 2013 démarre l’application localement, puis envoie des notifications système aux autres utilisateurs, en leur demandant de démarrer l’application spécifiée sur leur ordinateur.</span><span class="sxs-lookup"><span data-stu-id="e7ce5-206">Lync 2013 starts the application locally, and then sends system notifications to the other users, prompting them to start the specified application on their computer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7ce5-207">MCUType</span><span class="sxs-lookup"><span data-stu-id="e7ce5-207">MCUType</span></span></p></td>
<td><p><span data-ttu-id="e7ce5-208">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="e7ce5-208">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="e7ce5-209">DATA = le type du serveur.</span><span class="sxs-lookup"><span data-stu-id="e7ce5-209">DATA = The type of server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7ce5-210">ExtensibleMenu</span><span class="sxs-lookup"><span data-stu-id="e7ce5-210">ExtensibleMenu</span></span></p></td>
<td><p><span data-ttu-id="e7ce5-211">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="e7ce5-211">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="e7ce5-212">Liste des menus dans lesquels cette commande s’affiche, en les séparant par un point-virgule.</span><span class="sxs-lookup"><span data-stu-id="e7ce5-212">A list of the menus where this command will appear, separated by semicolons.</span></span> <span data-ttu-id="e7ce5-213">Valeurs possibles :</span><span class="sxs-lookup"><span data-stu-id="e7ce5-213">Possible values are:</span></span></p>
<ul>
<li><p><span data-ttu-id="e7ce5-214">MainWindowActions</span><span class="sxs-lookup"><span data-stu-id="e7ce5-214">MainWindowActions</span></span></p></li>
<li><p><span data-ttu-id="e7ce5-215">MainWindowRightClick</span><span class="sxs-lookup"><span data-stu-id="e7ce5-215">MainWindowRightClick</span></span></p></li>
<li><p><span data-ttu-id="e7ce5-216">ConversationWindowActions</span><span class="sxs-lookup"><span data-stu-id="e7ce5-216">ConversationWindowActions</span></span></p></li>
<li><p><span data-ttu-id="e7ce5-217">ConversationWindowButton</span><span class="sxs-lookup"><span data-stu-id="e7ce5-217">ConversationWindowButton</span></span></p></li>
<li><p><span data-ttu-id="e7ce5-218">ConversationWindowRightClick</span><span class="sxs-lookup"><span data-stu-id="e7ce5-218">ConversationWindowRightClick</span></span></p></li>
</ul>
<p><span data-ttu-id="e7ce5-219">Si ExtensibleMenu n’est pas défini, les valeurs par défaut de MainWindowRightClick et ConversationWindowActions sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="e7ce5-219">If ExtensibleMenu is not defined, the default values of MainWindowRightClick and ConversationWindowActions are used.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e7ce5-220">L’exemple suivant ajoute des commandes pour démarrer le client de collaboration adatum à partir de Lync 2013 :</span><span class="sxs-lookup"><span data-stu-id="e7ce5-220">The following example adds commands to start ADatum Collaboration Client from within Lync 2013:</span></span>

    Windows Registry Editor Version 5.00
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Lync\SessionManager]
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Lync\SessionManager\Apps]
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Lync\SessionManager\Apps\{27877e66-615c-4582-ab88-0cb2ca05d951}]
    "Path"="meet:%conf-uri%"
    "SessionType"=dword:00000002
    "LiveServerIntegration"=dword:00000001
    "ApplicationType"=dword:00000001
    "Name"="ADatum Collaboration Client"
    "MCUType"="Data"
    "Extensiblemenu"="MainWindowActions;MainWindowRightClick;ConversationWindowActions;ConversationWindowRightClick"

<span data-ttu-id="e7ce5-221"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e7ce5-221"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

