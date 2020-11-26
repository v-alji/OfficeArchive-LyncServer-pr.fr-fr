---
title: Documentation des outils du kit de ressources Lync Server 2013
description: Documentation des outils du kit de ressources Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Lync Server 2013 Resource Kit Tools Documentation
ms:assetid: b1c341f1-86fa-479d-ba4d-28df5a4c1622
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945604(v=OCS.15)
ms:contentKeyID: 51541429
ms.date: 02/02/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6866e04615014daa7e93f7e7f1081b10325d087d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446706"
---
# <a name="lync-server-2013-resource-kit-tools-documentation"></a><span data-ttu-id="88c68-103">Documentation des outils du kit de ressources Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="88c68-103">Lync Server 2013 Resource Kit Tools Documentation</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="88c68-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="88c68-104">

<span> </span></span></span>

<span data-ttu-id="88c68-105">_**Dernière modification de la rubrique :** 2014-01-09_</span><span class="sxs-lookup"><span data-stu-id="88c68-105">_**Topic Last Modified:** 2014-01-09_</span></span>

<span data-ttu-id="88c68-106">Cette rubrique décrit les outils qui font partie du kit de ressources de Lync Server 2013, notamment l’objet de chaque outil et des exemples de son utilisation. Les outils du kit de ressources de Lync Server 2013 permettent d’effectuer des tâches de routine plus facilement pour les administrateurs informatiques qui déploient et gèrent Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="88c68-106">This topic describes the tools that are part of the Lync Server 2013 Resource Kit, including the purpose of each tool, and examples of its use.The Lync Server 2013, Resource Kit Tools help to make routine tasks easier for IT administrators who deploy and manage Lync Server 2013.</span></span> <span data-ttu-id="88c68-107">Par exemple, l’outil **Web Conf Data** permet de contrôler aisément les données téléchargées par les utilisateurs au cours d’une réunion en ligne.</span><span class="sxs-lookup"><span data-stu-id="88c68-107">For example, the **Web Conf Data** tool can be used to easily control data that is uploaded by users during an online meeting.</span></span> <span data-ttu-id="88c68-108">L’outil **SEFAUtil** permet de définir le transfert des appels de délégué et le répondeur automatique pour les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="88c68-108">The **SEFAUtil** tool can be used to set up delegate call forwarding and answering for users.</span></span> <span data-ttu-id="88c68-109">Nous recommandons aux administrateurs informatiques d’utiliser ces outils pour gérer plus efficacement Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="88c68-109">We encourage IT administrators to use these tools to more effectively manage Lync Server 2013.</span></span>

<div>

## <a name="installation-of-the-resource-kit-tools"></a><span data-ttu-id="88c68-110">Installation des outils du kit de ressources</span><span class="sxs-lookup"><span data-stu-id="88c68-110">Installation of the Resource Kit Tools</span></span>

<span data-ttu-id="88c68-111">Pour installer Lync Server 2013, les outils du kit de ressources, téléchargez **OCSReskit.msi**.</span><span class="sxs-lookup"><span data-stu-id="88c68-111">To install the Lync Server 2013, Resource Kit Tools, download **OCSReskit.msi**.</span></span> <span data-ttu-id="88c68-112">Vous pouvez télécharger le programme d’installation des outils du kit de ressources à partir du centre de téléchargement à l’adresse [https://go.microsoft.com/fwlink/p/?LinkID=330429](https://go.microsoft.com/fwlink/p/?linkid=330429) .</span><span class="sxs-lookup"><span data-stu-id="88c68-112">You can download the Resource Kit Tools installer from the Download Center at [https://go.microsoft.com/fwlink/p/?LinkID=330429](https://go.microsoft.com/fwlink/p/?linkid=330429).</span></span>

<span data-ttu-id="88c68-113">Exécutez **OCSResKit.msi** pour effectuer une installation simple.</span><span class="sxs-lookup"><span data-stu-id="88c68-113">Run **OCSResKit.msi** to do a simple installation.</span></span> <span data-ttu-id="88c68-114">Le fichier. msi installe tous les outils dans le chemin d’accès suivant : **% fichiers programme% \\ Microsoft Lync Server 2013 \\ reskit**.</span><span class="sxs-lookup"><span data-stu-id="88c68-114">The .msi installs all the tools in the following path: **%Program Files%\\Microsoft Lync Server 2013\\ResKit**.</span></span> <span data-ttu-id="88c68-115">Les outils exécutables autonomes se trouvent dans ce dossier.</span><span class="sxs-lookup"><span data-stu-id="88c68-115">Tools that are self-contained executables are in this folder.</span></span> <span data-ttu-id="88c68-116">Les outils qui comportent également des fichiers se trouvent dans leurs propres sous-dossiers.</span><span class="sxs-lookup"><span data-stu-id="88c68-116">Tools that also have files are in their own subfolders.</span></span>

</div>

<div>

## <a name="supported-environments"></a><span data-ttu-id="88c68-117">Environnements pris en charge</span><span class="sxs-lookup"><span data-stu-id="88c68-117">Supported Environments</span></span>

<span data-ttu-id="88c68-118">Pour des performances optimales, les outils du kit de ressources de Lync Server 2013 doivent être installés dans le même environnement et avec les mêmes spécifications requises pour Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="88c68-118">For optimal performance, the Lync Server 2013, Resource Kit Tools should be installed in the same environment and with the same specifications that are required for Lync Server 2013.</span></span>

</div>

<div>

## <a name="resource-kit-tools-overview"></a><span data-ttu-id="88c68-119">Présentation des outils du kit de ressources</span><span class="sxs-lookup"><span data-stu-id="88c68-119">Resource Kit Tools Overview</span></span>

<span data-ttu-id="88c68-120">La liste suivante décrit les outils fournis dans le kit de ressources de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="88c68-120">The following list describes the tools that are provided in the Lync Server 2013 Resource Kit.</span></span> <span data-ttu-id="88c68-121">Pour plus d’informations, reportez-vous à la section suivante.</span><span class="sxs-lookup"><span data-stu-id="88c68-121">A description of each tool, including the requirements and example usage is covered in the following section.</span></span>

  - <span data-ttu-id="88c68-122">ABSConfig</span><span class="sxs-lookup"><span data-stu-id="88c68-122">ABSConfig</span></span>

  - <span data-ttu-id="88c68-123">Bandwidth Policy Service Monitor</span><span class="sxs-lookup"><span data-stu-id="88c68-123">Bandwidth Policy Service Monitor</span></span>

  - <span data-ttu-id="88c68-124">Bandwidth Utilization Analyzer</span><span class="sxs-lookup"><span data-stu-id="88c68-124">Bandwidth Utilization Analyzer</span></span>

  - <span data-ttu-id="88c68-125">Call Parkometer</span><span class="sxs-lookup"><span data-stu-id="88c68-125">Call Parkometer</span></span>

  - <span data-ttu-id="88c68-126">CleanupStorageServiceData</span><span class="sxs-lookup"><span data-stu-id="88c68-126">CleanupStorageServiceData</span></span>

  - <span data-ttu-id="88c68-127">DBAnalyze</span><span class="sxs-lookup"><span data-stu-id="88c68-127">DBAnalyze</span></span>

  - <span data-ttu-id="88c68-128">ImportStorageServiceData</span><span class="sxs-lookup"><span data-stu-id="88c68-128">ImportStorageServiceData</span></span>

  - <span data-ttu-id="88c68-129">LCSSync</span><span class="sxs-lookup"><span data-stu-id="88c68-129">LCSSync</span></span>

  - <span data-ttu-id="88c68-130">LookupUserConsole</span><span class="sxs-lookup"><span data-stu-id="88c68-130">LookupUserConsole</span></span>

  - <span data-ttu-id="88c68-131">MsTurnPing</span><span class="sxs-lookup"><span data-stu-id="88c68-131">MsTurnPing</span></span>

  - <span data-ttu-id="88c68-132">Network Configuration Viewer</span><span class="sxs-lookup"><span data-stu-id="88c68-132">Network Configuration Viewer</span></span>

  - <span data-ttu-id="88c68-133">Response Group Agent Live</span><span class="sxs-lookup"><span data-stu-id="88c68-133">Response Group Agent Live</span></span>

  - <span data-ttu-id="88c68-134">SEFAUtil</span><span class="sxs-lookup"><span data-stu-id="88c68-134">SEFAUtil</span></span>

  - <span data-ttu-id="88c68-135">SYSPrep.ps1</span><span class="sxs-lookup"><span data-stu-id="88c68-135">SYSPrep.ps1</span></span>

  - <span data-ttu-id="88c68-136">Unassigned Number Announcements Migration</span><span class="sxs-lookup"><span data-stu-id="88c68-136">Unassigned Number Announcements Migration</span></span>

  - <span data-ttu-id="88c68-137">Web Conf Data</span><span class="sxs-lookup"><span data-stu-id="88c68-137">Web Conf Data</span></span>

</div>

<div>

## <a name="absconfig"></a><span data-ttu-id="88c68-138">ABSConfig</span><span class="sxs-lookup"><span data-stu-id="88c68-138">ABSConfig</span></span>

<span data-ttu-id="88c68-139">L’outil de configuration du service de carnet d’adresses (ABSConfig) est un outil administratif qui permet aux administrateurs de personnaliser la configuration du service de carnet d’adresses dans Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="88c68-139">The Address Book Service Configuration tool (ABSConfig) is an administrative tool that helps administrators customize Address Book Service configuration in Lync Server 2013.</span></span> <span data-ttu-id="88c68-140">Cet outil permet également aux administrateurs de Lync Server 2013 de restaurer les paramètres de service de carnet d’adresses par défaut.</span><span class="sxs-lookup"><span data-stu-id="88c68-140">This tool also enables Lync Server 2013 administrators to restore the default Address Book Service settings.</span></span>

<div>

## <a name="description"></a><span data-ttu-id="88c68-141">Description</span><span class="sxs-lookup"><span data-stu-id="88c68-141">Description</span></span>

<span data-ttu-id="88c68-142">ABSConfig est une application graphique d’interface utilisateur qui permet aux administrateurs de configurer des attributs de services de domaine Active Directory liés au service de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="88c68-142">ABSConfig is a graphical user interface application that enables administrators to configure Active Directory Domain Services attributes that are related to Address Book Service.</span></span>

<span data-ttu-id="88c68-143">Les principaux scénarios suivants s’appliquent à l’outil :</span><span class="sxs-lookup"><span data-stu-id="88c68-143">The primary scenarios for the tool are the following:</span></span>

  - <span data-ttu-id="88c68-144">Pour permettre aux administrateurs de mapper les attributs dans les services de domaine Active Directory aux attributs de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="88c68-144">To enable administrators to map attributes in Active Directory Domain Services to the attributes for Lync Server 2013.</span></span>

  - <span data-ttu-id="88c68-145">permettre aux administrateurs de spécifier un attribut des services de domaine Active Directory à inclure dans les fichiers du service de carnet d’adresses ou à exclure de ceux-ci ;</span><span class="sxs-lookup"><span data-stu-id="88c68-145">To enable administrators to specify the Active Directory Domain Services attribute to be included or excluded in the Address Book Service files.</span></span>

  - <span data-ttu-id="88c68-146">permettre aux administrateurs de restaurer les paramètres par défaut du service de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="88c68-146">To enable administrators to restore default Address Book Service settings.</span></span>

<span data-ttu-id="88c68-147">L’outil ABSConfig peut être démarré en utilisant le fichier absConfig.exe.</span><span class="sxs-lookup"><span data-stu-id="88c68-147">The ABSConfig tool can be started by using the absConfig.exe file.</span></span> <span data-ttu-id="88c68-148">L’outil s’ouvre dans l’onglet **configurer les attributs** . Le tableau suivant contient des options permettant de mapper les attributs des services de domaine Active Directory aux champs d’attribut pour Lync Server 2013 et de spécifier les utilisateurs à inclure ou exclure dans les fichiers du service de carnet d’adresses en fonction de filtres d’attributs spécifiques.</span><span class="sxs-lookup"><span data-stu-id="88c68-148">The tool opens to the **Configure Attributes** tab. This table has options to map Active Directory Domain Services attributes to the attribute fields for Lync Server 2013 and to specify which users to include or exclude in Address Book Service files based on specific attribute filters.</span></span> <span data-ttu-id="88c68-149">D’autres options permettent de personnaliser la valeur du numéro de téléphone à inclure dans le fichier de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="88c68-149">It also has options to customize which value of the phone number to be included in the Address Book file.</span></span> <span data-ttu-id="88c68-150">L’option **Restore Defaults (Paramètres par défaut)** permet aux administrateurs de restaurer les valeurs par défaut des paramètres du service de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="88c68-150">The **Restore Defaults** option enables administrators to restore Address Book Service settings to default values.</span></span>

</div>

<div>

## <a name="changes-from-lync-server-2010"></a><span data-ttu-id="88c68-151">Modifications de Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="88c68-151">Changes from Lync Server 2010</span></span>

<span data-ttu-id="88c68-152">Dans l’outil de configuration ABS de Lync Server 2013, les attributs (lignes) risquent d’être supprimés en décochez la case « Activer » pour l’attribut.</span><span class="sxs-lookup"><span data-stu-id="88c68-152">In Lync Server 2013 ABS Configuration tool, attributes (rows) may be removed by unchecking the “enable” checkbox for the attribute.</span></span> <span data-ttu-id="88c68-153">Ce résultat est le même que celui de la suppression de la ligne dans Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="88c68-153">This has the same effect as deleting the row in Lync Server 2010.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="88c68-154">La case à cocher Activer se trouve dans l’extrémité droite de la colonne. Il est possible que vous deviez faire défiler la liste vers la droite pour afficher la colonne</span><span class="sxs-lookup"><span data-stu-id="88c68-154">The enable checkbox is in the far right column; you may need to scroll right to see the column</span></span>



</div>

</div>

<div>

## <a name="output"></a><span data-ttu-id="88c68-155">Sortie</span><span class="sxs-lookup"><span data-stu-id="88c68-155">Output</span></span>

<span data-ttu-id="88c68-156">ABSConfig stocke la configuration du service de carnet d’adresses dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="88c68-156">ABSConfig stores the Address Book Service configuration in the database.</span></span>

    Path: %ProgramFiles%\Microsoft Lync Server 2013\Reskit

</div>

<div>

## <a name="purpose"></a><span data-ttu-id="88c68-157">Objectif</span><span class="sxs-lookup"><span data-stu-id="88c68-157">Purpose</span></span>

<span data-ttu-id="88c68-158">ABSConfig offre un moyen rapide et facile de personnaliser le service de carnet d’adresses Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="88c68-158">ABSConfig provides a quick and easy way to customize Lync Server 2013 Address Book Service.</span></span>

</div>

<div>

## <a name="requirements"></a><span data-ttu-id="88c68-159">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="88c68-159">Requirements</span></span>

<div>

## <a name="computer"></a><span data-ttu-id="88c68-160">Ordinateur</span><span class="sxs-lookup"><span data-stu-id="88c68-160">Computer</span></span>

<span data-ttu-id="88c68-161">ABSConfig ne peut être exécuté qu’à partir d’un ordinateur appartenant à un domaine sur lequel Lync Server 2013 est installé.</span><span class="sxs-lookup"><span data-stu-id="88c68-161">ABSConfig can be run only from a domain-joined computer that has Lync Server 2013 installed.</span></span> <span data-ttu-id="88c68-162">Dans le cas de Lync Server 2013, Enterprise Edition, cet outil peut être exécuté sur n’importe quel serveur frontal sur lequel le service de carnet d’adresses est activé lors de l’installation.</span><span class="sxs-lookup"><span data-stu-id="88c68-162">In the case of Lync Server 2013, Enterprise Edition, this tool can be run on any Front End servers that have the Address Book Service enabled during setup.</span></span>

</div>

<div>

## <a name="network"></a><span data-ttu-id="88c68-163">Réseau</span><span class="sxs-lookup"><span data-stu-id="88c68-163">Network</span></span>

<span data-ttu-id="88c68-164">L’ordinateur doit pouvoir se connecter au pool frontal et à la base de données principale.</span><span class="sxs-lookup"><span data-stu-id="88c68-164">The computer should be able to connect to the Front End pool and back-end database.</span></span>

</div>

<div>

## <a name="software"></a><span data-ttu-id="88c68-165">Logiciels</span><span class="sxs-lookup"><span data-stu-id="88c68-165">Software</span></span>

<span data-ttu-id="88c68-166">Les composants logiciels suivants doivent être installés avant d’exécuter l’outil ABSConfig :</span><span class="sxs-lookup"><span data-stu-id="88c68-166">The following software components must be installed before running the ABSConfig tool:</span></span>

  - <span data-ttu-id="88c68-167">Microsoft Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="88c68-167">Microsoft Lync Server 2013</span></span>

</div>

<div>

## <a name="users"></a><span data-ttu-id="88c68-168">Utilisateurs</span><span class="sxs-lookup"><span data-stu-id="88c68-168">Users</span></span>

<span data-ttu-id="88c68-169">Administrateurs disposant des autorisations requises pour mettre à jour le déploiement de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="88c68-169">Administrators who have the permissions required to update the Lync Server 2013 deployment.</span></span>

</div>

</div>

<div>

## <a name="examples"></a><span data-ttu-id="88c68-170">Exemples</span><span class="sxs-lookup"><span data-stu-id="88c68-170">Examples</span></span>

<span data-ttu-id="88c68-p109">ABSConfig peut être démarré en tapant **ABSConfig.exe** dans une invite de commandes. L’interface utilisateur de l’outil ABSConfig se présente comme suit :</span><span class="sxs-lookup"><span data-stu-id="88c68-p109">ABSConfig can be started by typing **ABSConfig.exe** at a command prompt. Shown below is the ABSConfig tool user interface.</span></span>

<span data-ttu-id="88c68-173">![Outil ABSConfig.exe.](images/JJ945604.6fb63a70-7b63-4b8b-b7d1-82fe9aa2028f(OCS.15).jpg "Outil ABSConfig.exe.")</span><span class="sxs-lookup"><span data-stu-id="88c68-173">![The ABSConfig.exe tool.](images/JJ945604.6fb63a70-7b63-4b8b-b7d1-82fe9aa2028f(OCS.15).jpg "The ABSConfig.exe tool.")</span></span>

</div>

<div>

## <a name="summary"></a><span data-ttu-id="88c68-174">Résumé</span><span class="sxs-lookup"><span data-stu-id="88c68-174">Summary</span></span>

<span data-ttu-id="88c68-175">L’outil ABSConfig fournit aux administrateurs un outil rapide et facile à utiliser pour personnaliser le service de carnet d’adresses Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="88c68-175">The ABSConfig tool provides administrators a quick and easy to use tool to customize Lync Server 2013 Address Book Service.</span></span>

</div>

</div>

<div>

## <a name="bandwidth-policy-service-monitor"></a><span data-ttu-id="88c68-176">Bandwidth Policy Service Monitor</span><span class="sxs-lookup"><span data-stu-id="88c68-176">Bandwidth Policy Service Monitor</span></span>

<span data-ttu-id="88c68-177">L’outil Bandwidth Policy Service Monitor permet aux administrateurs d’afficher la liste des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="88c68-177">The Bandwidth Policy Service Monitor tool is intended to allow administrators to view a list of the following:</span></span>

1.  <span data-ttu-id="88c68-178">Tous les services de stratégie de bande passante configurés pour Lync Server 2013 (authentification et noyau) dans la topologie</span><span class="sxs-lookup"><span data-stu-id="88c68-178">All the configured Lync Server 2013 Bandwidth Policy services (Authentication and Core) in the topology</span></span>

2.  <span data-ttu-id="88c68-179">connexions effectuées par chaque service aux autres services de stratégie de bande passante et aux serveurs Edge ;</span><span class="sxs-lookup"><span data-stu-id="88c68-179">The connections that each service makes to other Bandwidth Policy services and to the Edge servers</span></span>

3.  <span data-ttu-id="88c68-180">liaisons configurées dans le document de configuration du réseau et utilisation de la bande passante en temps réel, telle que signalée par les services de stratégie de bande passante individuels.</span><span class="sxs-lookup"><span data-stu-id="88c68-180">All the links that are configured in the Network configuration document and real-time bandwidth usage as reported by each of the Bandwidth Policy services</span></span>

<div>

## <a name="description"></a><span data-ttu-id="88c68-181">Description</span><span class="sxs-lookup"><span data-stu-id="88c68-181">Description</span></span>

<span data-ttu-id="88c68-p110">L’outil Bandwidth Policy Service Monitor est implémenté sous la forme d’une application à interface utilisateur graphique. Les administrateurs démarrent l’outil en exécutant PDPMonUI.exe.</span><span class="sxs-lookup"><span data-stu-id="88c68-p110">The Bandwidth Policy Service Monitor tool is implemented as a GUI-based application. Administrators start the tool by running PDPMonUI.exe.</span></span>

<span data-ttu-id="88c68-p111">Lorsque l’outil démarre, il tente de découvrir la liste des services de stratégie de bande passante dans la topologie. Une fois la mise à jour initiale effectuée, le volet situé à gauche de la fenêtre reçoit une liste de services regroupés selon les clusters auxquels ils appartiennent.</span><span class="sxs-lookup"><span data-stu-id="88c68-p111">When the tool starts, it attempts to discover the list of Bandwidth Policy services in the topology. After the initial update is done, the pane to the left of the window is populated with a list of services that are grouped by the clusters that they belong to.</span></span>

<span data-ttu-id="88c68-p112">Lorsque les administrateurs sélectionnent un service de stratégie de bande passante particulier, le volet situé à droite affiche les informations relatives à ce service particulier. Ce volet inclut également deux onglets principaux qui affichent des informations.</span><span class="sxs-lookup"><span data-stu-id="88c68-p112">When administrators select a particular Bandwidth Policy Service, the pane on the right displays the information about that particular service. That pane also has two main tabs that display information.</span></span>

<div>

## <a name="machine-info-tab"></a><span data-ttu-id="88c68-188">Onglet Machine Info (Informations sur l’ordinateur)</span><span class="sxs-lookup"><span data-stu-id="88c68-188">Machine Info Tab</span></span>

<span data-ttu-id="88c68-189">L’onglet **Machine Info (Informations sur l’ordinateur)** fournit des informations sur le service de stratégie de bande passante sélectionné, ainsi que la liste et l’état des connexions effectuées par le service de stratégie de bande passante sélectionné aux autres services.</span><span class="sxs-lookup"><span data-stu-id="88c68-189">The **Machine Info** tab shows the details of the Bandwidth Policy Service that is selected and the list and state of all the connections that are made by the selected Bandwidth Policy Service to other services.</span></span>

</div>

<div>

## <a name="topology-info-tab"></a><span data-ttu-id="88c68-190">Onglet Topology Info (Informations sur la topologie)</span><span class="sxs-lookup"><span data-stu-id="88c68-190">Topology Info Tab</span></span>

<span data-ttu-id="88c68-p113">L’onglet **Topology Info (Informations sur la topologie)** affiche la liste des liaisons configurées dans les paramètres de configuration du réseau. Pour chaque liaison, la capacité de bande passante audio et vidéo est indiquée. La bande passante actuellement utilisée est également indiquée, en Kbps et en pourcentage de la capacité. L’outil utilise des couleurs pour mettre en valeur les liaisons dont l’utilisation atteint presque la capacité maximale afin que les administrateurs puissent les isoler rapidement.</span><span class="sxs-lookup"><span data-stu-id="88c68-p113">The **Topology Info** tab shows a list of all the links that are configured in the Network configuration settings. For each link, the audio and video bandwidth capacity is displayed. Additionally, the currently utilized bandwidth is displayed, both in Kbps and as a percentage of the capacity. The tool uses color-coding to highlight links that have utilization that is close to the capacity—this allows administrators to quickly isolate such links.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="88c68-p114"> Si l’outil Bandwidth Policy Service Monitor rencontre des défaillances lorsqu’il se connecte aux services de stratégie de la bande passante configurés, aucune information n’apparaît sous les onglets <STRONG>Machine Info (Informations sur l’ordinateur) </STRONG> et <STRONG>Topology Info (Informations sur la topologie)</STRONG>. Il est toutefois possible que l’outil se connecte avant de perdre la connexion au service. En pareil cas, les administrateurs peuvent voir des informations obsolètes. Les onglets incluent des informations d’horodatage (<STRONG>Last Updated (Dernière mise à jour)</STRONG>) qui permettent aux administrateurs de voir la date/l’heure de la dernière mise à jour des données pour un service de stratégie de bande passante particulier.</span><span class="sxs-lookup"><span data-stu-id="88c68-p114">If the Bandwidth Policy Service Monitor tool experiences failure when it connects to any of the configured Bandwidth Policy services, the information in the <STRONG>Machine Info</STRONG> and the <STRONG>Topology Info</STRONG> tabs won’t be populated. However, it is possible that the tool might connect initially but subsequently lose its connection to the service. In such cases, administrators might see outdated information. There is a <STRONG>Last Updated</STRONG> time stamp on each of the tabs that can allow administrators to see when the data was last updated for a particular Bandwidth Policy Service.</span></span>



</div>

</div>

</div>

<div>

## <a name="output"></a><span data-ttu-id="88c68-199">Sortie</span><span class="sxs-lookup"><span data-stu-id="88c68-199">Output</span></span>

<span data-ttu-id="88c68-200">Il n’y a aucune sortie de ligne de commande. La sortie du programme apparaît dans l’interface utilisateur graphique principale.</span><span class="sxs-lookup"><span data-stu-id="88c68-200">There is no command-line output; the program output is contained within the main graphical user interface (GUI).</span></span>

</div>

<div>

## <a name="purpose"></a><span data-ttu-id="88c68-201">Objectif</span><span class="sxs-lookup"><span data-stu-id="88c68-201">Purpose</span></span>

<span data-ttu-id="88c68-p115">L’outil Bandwidth Policy Service Monitor permet aux administrateurs de consulter l’état des services de stratégie de bande passante définis dans la topologie. Ils peuvent également voir l’utilisation de la bande passante en temps réel pour toutes les liaisons définies dans le document de configuration du réseau.</span><span class="sxs-lookup"><span data-stu-id="88c68-p115">The purpose of the Bandwidth Policy Service Monitor tool is to allow administrators visibility into the state of each of the Bandwidth Policy services that are defined in the topology. In addition, administrators can see real-time bandwidth usage for all the links that are defined in the Network configuration document.</span></span>

</div>

<div>

## <a name="requirements"></a><span data-ttu-id="88c68-204">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="88c68-204">Requirements</span></span>

<span data-ttu-id="88c68-205">L’outil Moniteur du service de stratégie de bande passante doit être exécuté sur un ordinateur qui fait partie de la topologie du serveur Lync.</span><span class="sxs-lookup"><span data-stu-id="88c68-205">The Bandwidth Policy Service Monitor tool needs to be run on a computer that is part of the Lync Server topology.</span></span>

</div>

<div>

## <a name="summary"></a><span data-ttu-id="88c68-206">Résumé</span><span class="sxs-lookup"><span data-stu-id="88c68-206">Summary</span></span>

<span data-ttu-id="88c68-207">L’outil Bandwidth Policy Service Monitor est utile pour contrôler l’état des services de stratégie de bande passante dans la topologie et connaître l’utilisation de la bande passante en temps réel pour les liaisons définies dans les paramètres de configuration du réseau.</span><span class="sxs-lookup"><span data-stu-id="88c68-207">The Bandwidth Policy Service Monitor tool can be a valuable resource to administrators so they can inspect the state of all the Bandwidth Policy services in the topology—and more importantly—they can obtain real-time bandwidth utilization for the links that are defined in the Network configuration settings.</span></span>

</div>

</div>

<div>

## <a name="bandwidth-utilization-analyzer"></a><span data-ttu-id="88c68-208">Bandwidth Utilization Analyzer</span><span class="sxs-lookup"><span data-stu-id="88c68-208">Bandwidth Utilization Analyzer</span></span>

<span data-ttu-id="88c68-p116">L’outil Bandwidth Utilization Analyzer crée des rapports sur divers affichages de la consommation de bande passante par les points de terminaison d’UC entre les liaisons de réseau étendu dans le réseau d’entreprise. Ces rapports permettent d’identifier le modèle actuel de consommation de la bande passante et de planifier la capacité de bande passante.</span><span class="sxs-lookup"><span data-stu-id="88c68-p116">Bandwidth Utilization Analyzer is a tool that creates reports about various views of bandwidth consumption by the UC endpoints across WAN links in the enterprise network. These reports can be used to understand the current bandwidth consumption pattern and to aid in bandwidth capacity planning.</span></span>

<div>

## <a name="description"></a><span data-ttu-id="88c68-211">Description</span><span class="sxs-lookup"><span data-stu-id="88c68-211">Description</span></span>

<span data-ttu-id="88c68-p117">Bandwidth Utilization Analyzer est implémenté sous la forme d’une application à interface utilisateur graphique. Cet outil génère des rapports spécifiques sur l’utilisation de la bande passante audio dans le réseau et constitue une aide pour planifier la capacité. Il traite également la capacité de bande passante affectée aux diverses liaisons par itération.</span><span class="sxs-lookup"><span data-stu-id="88c68-p117">Bandwidth Utilization Analyzer is implemented as a GUI-based application. This tool generates reports specifically for audio utilization across the network and helps with capacity planning. It also iterates on the bandwidth capacity that is assigned to various links.</span></span>

</div>

<div>

## <a name="output"></a><span data-ttu-id="88c68-215">Sortie</span><span class="sxs-lookup"><span data-stu-id="88c68-215">Output</span></span>

<span data-ttu-id="88c68-216">Bandwidth Utilization Analyzer offre une représentation graphique de la capacité de bande passante et de l’utilisation de la bande passante audio pour les liaisons de réseau étendu configurées dans le système.</span><span class="sxs-lookup"><span data-stu-id="88c68-216">Bandwidth Utilization Analyzer provides graphic al plots of bandwidth capacity and utilization for audio for all the WAN links that are configured in the system.</span></span>

</div>

<div>

## <a name="purpose"></a><span data-ttu-id="88c68-217">Objectif</span><span class="sxs-lookup"><span data-stu-id="88c68-217">Purpose</span></span>

<span data-ttu-id="88c68-p118">Dans tous les déploiements voix et vidéo, il est essentiel de surveiller et comprendre les tendances d’utilisation de la bande passante par le trafic multimédia au sein du réseau de l’entreprise. L’outil Bandwidth Utilization Analyzer permet aux administrateurs d’y parvenir. L’outil effectue les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="88c68-p118">In any voice and video deployment, it’s critical to monitor and understand the trend of bandwidth utilization of media traffic across the enterprise network. The Bandwidth Utilization Analyzer tool allows an administrator to achieve just that. This tool does the following:</span></span>

  - <span data-ttu-id="88c68-221">génère des rapports spécifiques sur l’utilisation de la bande passante audio dans le réseau ;</span><span class="sxs-lookup"><span data-stu-id="88c68-221">Generates specific reports for audio utilization across the network</span></span>

  - <span data-ttu-id="88c68-222">permet de planifier la capacité plus efficacement et de traiter la capacité de bande passante affectée aux diverses liaisons par itération.</span><span class="sxs-lookup"><span data-stu-id="88c68-222">Helps with more effective capacity planning and iteration on the bandwidth capacity that is assigned to various links</span></span>

<span data-ttu-id="88c68-223">Bandwidth Utilization Analyzer peut générer une représentation graphique des rapports sur la capacité et l’utilisation de la bande passante, comme suit :</span><span class="sxs-lookup"><span data-stu-id="88c68-223">Bandwidth Utilization Analyzer can generate graphical plots of bandwidth capacity and utilization reports; they are as follows:</span></span>

  - <span data-ttu-id="88c68-224">liaisons de réseau étendu au sein du réseau d’entreprise ;</span><span class="sxs-lookup"><span data-stu-id="88c68-224">All the WAN links in the enterprise network</span></span>

  - <span data-ttu-id="88c68-225">filtrage des liaisons de réseau étendu sélectionnées ;</span><span class="sxs-lookup"><span data-stu-id="88c68-225">Filtered by selected WAN links that have been chosen</span></span>

  - <span data-ttu-id="88c68-226">filtrage des liaisons de réseau étendu ayant dépassé leur capacité ;</span><span class="sxs-lookup"><span data-stu-id="88c68-226">Filtered by WAN links that have exceeded link capacity</span></span>

  - <span data-ttu-id="88c68-227">filtrage des liaisons de réseau étendu ayant sous-utilisé la bande passante approvisionnée ;</span><span class="sxs-lookup"><span data-stu-id="88c68-227">Filtered by WAN links that have been under-utilizing the provisioned bandwidth</span></span>

  - <span data-ttu-id="88c68-228">filtrage des liaisons de réseau étendu ayant atteint des niveaux critiques (utilisation de la bande passante supérieure à 90 % de la capacité de bande passante de la liaison de réseau étendu) ;</span><span class="sxs-lookup"><span data-stu-id="88c68-228">Filter by WAN links that have been reaching critical levels (a bandwidth utilization that is greater than 90% of bandwidth capacity of the WAN link)</span></span>

  - <span data-ttu-id="88c68-229">filtrage selon le type de liaison de réseau étendu (liaisons réseau-site, liaisons inter-régions et liaisons au sein d’un site) ;</span><span class="sxs-lookup"><span data-stu-id="88c68-229">Filtered by WAN link type—network-site links, interregional links, and links within a site</span></span>

  - <span data-ttu-id="88c68-230">filtrage par région réseau.</span><span class="sxs-lookup"><span data-stu-id="88c68-230">Filtered by network region</span></span>

<div>

## <a name="applications"></a><span data-ttu-id="88c68-231">Applications</span><span class="sxs-lookup"><span data-stu-id="88c68-231">Applications</span></span>

<span data-ttu-id="88c68-232">Bandwidth Utilization Analyzer inclut les deux applications (outils) suivantes :</span><span class="sxs-lookup"><span data-stu-id="88c68-232">Bandwidth Utilization Analyzer has the following two applications (tools):</span></span>

  - <span data-ttu-id="88c68-233">**WanLinkLogCollector.exe**   Cet outil permet de saisir les informations utiles. </span><span class="sxs-lookup"><span data-stu-id="88c68-233">**WanLinkLogCollector.exe**   This tool enables its user to input the required information.</span></span>

  - <span data-ttu-id="88c68-234">**BandwidthUtilizationAnalyzer.xlsm**  Un rapport de feuille de calcul Microsoft Excel est automatiquement lancé par WanLinkLogCollector.exe.</span><span class="sxs-lookup"><span data-stu-id="88c68-234">**BandwidthUtilizationAnalyzer.xlsm**  A Microsoft Excel spreadsheet software report is automatically launched by WanLinkLogCollector.exe.</span></span> <span data-ttu-id="88c68-235">Cette application permet à l’utilisateur d’appliquer des filtres au rapport, comme indiqué plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="88c68-235">This application allows the user to apply filters to the report as shown later in this article.</span></span>

</div>

<div>

## <a name="phases-of-using-bandwidth-utilization-analyzer"></a><span data-ttu-id="88c68-236">Phases d’utilisation de Bandwidth Utilization Analyzer</span><span class="sxs-lookup"><span data-stu-id="88c68-236">Phases of Using Bandwidth Utilization Analyzer</span></span>

<span data-ttu-id="88c68-237">L’utilisation de Bandwidth Utilization Analyzer implique deux phases :</span><span class="sxs-lookup"><span data-stu-id="88c68-237">There are two phases when using Bandwidth Utilization Analyzer:</span></span>

  - <span data-ttu-id="88c68-238">collecte des journaux, effectuée à l’aide de WanLinkLogCollector.exe ;</span><span class="sxs-lookup"><span data-stu-id="88c68-238">Collect logs, which is performed by using WanLinkLogCollector.exe</span></span>

  - <span data-ttu-id="88c68-239">personnalisation des rapports, effectuée à l’aide de BandwidthUtilizationAnalyzer.xlsm.</span><span class="sxs-lookup"><span data-stu-id="88c68-239">Customize reports, which is performed by using BandwidthUtilizationAnalyzer.xlsm</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="88c68-240">Il est recommandé que BandwidthUtilizationAnalyzer.xlsm ne soit pas démarré manuellement par les utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="88c68-240">We strongly recommend that BandwidthUtilizationAnalyzer.xlsm not be manually launched by end users.</span></span>



</div>

</div>

<div>

## <a name="starting-bandwidth-utilization-analyzer"></a><span data-ttu-id="88c68-241">Démarrage de Bandwidth Utilization Analyzer</span><span class="sxs-lookup"><span data-stu-id="88c68-241">Starting Bandwidth Utilization Analyzer</span></span>

<span data-ttu-id="88c68-242">Démarrez WanLinkLogCollector.exe dans une invite de commandes ou à l’aide de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="88c68-242">Start WanLinkLogCollector.exe at the command prompt or by using Windows Explorer.</span></span>

<span data-ttu-id="88c68-243">**Utilisation de WanLinkLogCollector.exe**</span><span class="sxs-lookup"><span data-stu-id="88c68-243">**Using WanLinkLogCollector.exe**</span></span>

<span data-ttu-id="88c68-244">L’utilisation de WanLinkLogCollector.exe comporte trois étapes :</span><span class="sxs-lookup"><span data-stu-id="88c68-244">There are three steps to using WanLinkLogCollector.exe:</span></span>

1.  <span data-ttu-id="88c68-245">**Définition de la chronologie**   Indiquez la chronologie pour laquelle le rapport doit être généré.</span><span class="sxs-lookup"><span data-stu-id="88c68-245">**Log the timeline**   Provide the timeline that the report needs to be generated for</span></span>

2.  <span data-ttu-id="88c68-246">**Définition des répertoires de fichiers**   Indiquez les informations relatives à l’emplacement des fichiers.</span><span class="sxs-lookup"><span data-stu-id="88c68-246">**Specify the file directories**   Provide file location information</span></span>

3.  <span data-ttu-id="88c68-247">**Collecter les journaux et lancer la visionneuse de rapports**  Exécuter la commande pour générer le rapport</span><span class="sxs-lookup"><span data-stu-id="88c68-247">**Collect the logs and launch the report viewer**  Execute the command to generate the report</span></span>

<div>

## <a name="step-1---log-the-timeline"></a><span data-ttu-id="88c68-248">Étape 1 - Définition de la chronologie</span><span class="sxs-lookup"><span data-stu-id="88c68-248">Step 1 - Log the timeline</span></span>

<span data-ttu-id="88c68-249">La définition de la chronologie permet à l’utilisateur de l’outil de spécifier les éléments suivants, comme indiqué dans la figure suivante. </span><span class="sxs-lookup"><span data-stu-id="88c68-249">Logging the timeline allows the tool user to specify the following as shown in the figure below.</span></span>

1.  <span data-ttu-id="88c68-250">**Date de début** Date de début de la chronologie pour laquelle le rapport doit être généré (par exemple, 1er août 2010).</span><span class="sxs-lookup"><span data-stu-id="88c68-250">**Start date** This is the start date of the timeline that the report is to be generated for; for example, August 1, 2010.</span></span>

2.  <span data-ttu-id="88c68-251">**Date de fin** Date de fin de la chronologie pour laquelle le rapport doit être généré (par exemple, 30 septembre 2010).</span><span class="sxs-lookup"><span data-stu-id="88c68-251">**End date** This is the end date of the timeline that the report is to be generated for; for example, September 30, 2010.</span></span>
    
    <span data-ttu-id="88c68-252">![Dates de début et de fin dans l’utilisation de la bande passante A](images/JJ945604.2c597cfc-3372-4d41-816b-26202f607ad8(OCS.15).jpg "Dates de début et de fin dans l’utilisation de la bande passante A")</span><span class="sxs-lookup"><span data-stu-id="88c68-252">![Start and End dates in the Bandwidth Utilization A](images/JJ945604.2c597cfc-3372-4d41-816b-26202f607ad8(OCS.15).jpg "Start and End dates in the Bandwidth Utilization A")</span></span>  

</div>

<div>

## <a name="step-2---specify-the-file-directories"></a><span data-ttu-id="88c68-253">Étape 2 - Définition des répertoires de fichiers</span><span class="sxs-lookup"><span data-stu-id="88c68-253">Step 2 - Specify the file directories</span></span>

<span data-ttu-id="88c68-254">Les répertoires de fichiers suivants peuvent être spécifiés par l’utilisateur, comme indiqué.</span><span class="sxs-lookup"><span data-stu-id="88c68-254">The following file directories can be specified by the user as shown.</span></span>

  - <span data-ttu-id="88c68-255">**Emplacement des fichiers journaux du serveur** Emplacement du dossier dans lequel les journaux du serveur de stratégie de bande passante sont stockés.</span><span class="sxs-lookup"><span data-stu-id="88c68-255">**Server log files location** The folder location where Bandwidth policy server logs are stored.</span></span> <span data-ttu-id="88c68-256">Il s’agit généralement de \<fileserver\> \\ \<choice of FE\> \\ AppServerFiles \\ PDP.</span><span class="sxs-lookup"><span data-stu-id="88c68-256">This is typically in \<fileserver\>\\\<choice of FE\>\\AppServerFiles\\PDP.</span></span>

  - <span data-ttu-id="88c68-257">**Emplacement de stockage des fichiers temporaires** Emplacement du fichier temporaire où les fichiers intermédiaires sont stockés lors de la génération du rapport.</span><span class="sxs-lookup"><span data-stu-id="88c68-257">**Temporary file storage location** The temporary file location where intermediate files are stored while the report is being generated.</span></span>

<span data-ttu-id="88c68-258">![Répertoires de fichiers dans l’utilisation de la bande passante anal](images/JJ945604.d66daeac-1669-45e3-932d-3f6782840c2a(OCS.15).jpg "Répertoires de fichiers dans l’utilisation de la bande passante anal")</span><span class="sxs-lookup"><span data-stu-id="88c68-258">![File directories in the Bandwidth Utilization Anal](images/JJ945604.d66daeac-1669-45e3-932d-3f6782840c2a(OCS.15).jpg "File directories in the Bandwidth Utilization Anal")</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="88c68-259">Vérifiez que l’utilisateur de l’outil dispose d’un accès suffisant aux journaux de serveur et au dossier du magasin des fichiers temporaires.</span><span class="sxs-lookup"><span data-stu-id="88c68-259">Ensure that sufficient file access to the server logs and the temporary file store folder is provided to the tool user.</span></span>



</div>

</div>

<div>

## <a name="step-3---collect-the-logs-and-start-the-report-viewer"></a><span data-ttu-id="88c68-260">Étape 3 - Collecte des journaux et démarrage de la visionneuse de rapports</span><span class="sxs-lookup"><span data-stu-id="88c68-260">Step 3 - Collect the logs and start the report viewer</span></span>

<span data-ttu-id="88c68-p121">Pour collecter les journaux et démarrer la visionneuse de rapports, cliquez sur **Execute (Exécuter)** comme indiqué ci-dessous. Cette opération permet de collecter les données requises.</span><span class="sxs-lookup"><span data-stu-id="88c68-p121">To collect the logs and start the report viewer, click **Execute** as shown below. This step collects the required data.</span></span>

<span data-ttu-id="88c68-263">![Collecte de données dans la Analité de l’utilisation de la bande passante](images/JJ945604.0019cb2c-7c01-4dc9-ac90-ac47c47d1bfd(OCS.15).jpg "Collecte de données dans la Analité de l’utilisation de la bande passante")</span><span class="sxs-lookup"><span data-stu-id="88c68-263">![Collecting data in the Bandwidth Utilization Analy](images/JJ945604.0019cb2c-7c01-4dc9-ac90-ac47c47d1bfd(OCS.15).jpg "Collecting data in the Bandwidth Utilization Analy")</span></span>

<span data-ttu-id="88c68-264">Une fois le contenu saisi validé, le message suivant apparaît.</span><span class="sxs-lookup"><span data-stu-id="88c68-264">When the input validation is successful, the message shown below is displayed.</span></span>

<span data-ttu-id="88c68-265">![Journaux de notification collectés dans la bande passante utili](images/JJ945604.eda91da8-3285-4eab-8ccb-c6d89c8cc221(OCS.15).jpg "Journaux de notification collectés dans la bande passante utili")</span><span class="sxs-lookup"><span data-stu-id="88c68-265">![Logs collected notification in the Bandwidth Utili](images/JJ945604.eda91da8-3285-4eab-8ccb-c6d89c8cc221(OCS.15).jpg "Logs collected notification in the Bandwidth Utili")</span></span>

<span data-ttu-id="88c68-p122">Cliquez sur **OK**. BandwidthUtilizationAnalyzer.xlsm démarre automatiquement. Suivez les instructions du message. Pour plus d’informations, voir **Utilisation de BandwidthUtilizationAnalyzer.xlsm** dans la section suivante.</span><span class="sxs-lookup"><span data-stu-id="88c68-p122">Click **OK**. BandwidthUtilizationAnalyzer.xlsm is automatically started. Follow the instructions in the message box. For details, see **Using BandwidthUtilizationAnalyzer.xlsm** in the next section.</span></span>

</div>

<div>


<span data-ttu-id="88c68-270">**Utilisation de BandwidthUtilizationAnalyzer.xlsm**</span><span class="sxs-lookup"><span data-stu-id="88c68-270">**Using BandwidthUtilizationAnalyzer.xlsm**</span></span>

1.  <span data-ttu-id="88c68-271">Une fois BandwidthUtilizationAnalyzer.xlsm démarré automatiquement, cliquez sur **Refresh (Actualiser)**, comme indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="88c68-271">When BandwidthUtilizationAnalyzer.xlsm is automatically started, click **Refresh** as shown below.</span></span>
    
    <span data-ttu-id="88c68-272">![BandwidthUtilizationAnalyzer.xlsm](images/JJ945604.c4e675b9-1671-400e-a712-6db82d731b39(OCS.15).jpg "BandwidthUtilizationAnalyzer.xlsm  ")</span><span class="sxs-lookup"><span data-stu-id="88c68-272">![BandwidthUtilizationAnalyzer.xlsm](images/JJ945604.c4e675b9-1671-400e-a712-6db82d731b39(OCS.15).jpg "BandwidthUtilizationAnalyzer.xlsm")</span></span>

2.  <span data-ttu-id="88c68-273">Si un dossier de fichiers est ouvert, sélectionnez consolidated.csv à l’emplacement spécifié dans le message, comme indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="88c68-273">When a file folder is opened, select consolidated.csv from the location that is specified in the message box as shown below.</span></span> <span data-ttu-id="88c68-274">Il indique également l’emplacement **C : \\ temp**.</span><span class="sxs-lookup"><span data-stu-id="88c68-274">It also shows the location as **C:\\Temp**.</span></span>
    
    <span data-ttu-id="88c68-275">![Ouverture d’un dossier dans BandwidthUtilizationAnalyzer.](images/JJ945604.601cc572-cee9-45fb-9ed1-c4b96a2fa21e(OCS.15).jpg "Ouverture d’un dossier dans BandwidthUtilizationAnalyzer.")</span><span class="sxs-lookup"><span data-stu-id="88c68-275">![Opening a folder in BandwidthUtilizationAnalyzer.](images/JJ945604.601cc572-cee9-45fb-9ed1-c4b96a2fa21e(OCS.15).jpg "Opening a folder in BandwidthUtilizationAnalyzer.")</span></span>

3.  <span data-ttu-id="88c68-276">Cliquez sur **Import (Importer)**.</span><span class="sxs-lookup"><span data-stu-id="88c68-276">Click **Import**.</span></span>

4.  <span data-ttu-id="88c68-p124">La représentation graphique est générée automatiquement. Elle est disponible lorsque le pointeur de traitement en arrière-plan disparaît.</span><span class="sxs-lookup"><span data-stu-id="88c68-p124">The graphical plot is automatically generated. It is available when the working-in-the-background pointer disappears.</span></span>
    
    <span data-ttu-id="88c68-279">![Application de filtres dans le mode état.](images/JJ945604.1416468e-e3ab-478e-b569-e42ba9c27a17(OCS.15).jpg "Application de filtres dans le mode état.")</span><span class="sxs-lookup"><span data-stu-id="88c68-279">![Applying filters in Report View.](images/JJ945604.1416468e-e3ab-478e-b569-e42ba9c27a17(OCS.15).jpg "Applying filters in Report View.")</span></span>

</div>

<div>

## <a name="applying-filters-to-the-report-view"></a><span data-ttu-id="88c68-280">Application de filtres à l’affichage du rapport</span><span class="sxs-lookup"><span data-stu-id="88c68-280">Applying Filters to the Report View</span></span>

<span data-ttu-id="88c68-281">Les filtres suivants peuvent être appliqués à l’affichage du rapport :</span><span class="sxs-lookup"><span data-stu-id="88c68-281">The filters that can be applied to the report view as shown below are described as follows:</span></span>

<span data-ttu-id="88c68-282">![Application de filtres dans le mode état.](images/JJ945604.1416468e-e3ab-478e-b569-e42ba9c27a17(OCS.15).jpg "Application de filtres dans le mode état.")</span><span class="sxs-lookup"><span data-stu-id="88c68-282">![Applying filters in Report View.](images/JJ945604.1416468e-e3ab-478e-b569-e42ba9c27a17(OCS.15).jpg "Applying filters in Report View.")</span></span>

1.  <span data-ttu-id="88c68-283">**Name (Nom)** Filtrage des liaisons de réseau étendu (le filtre apparaît dans la partie droite du graphique). Le préfixe représente les types de liaisons suivants (voir l’encadré bleu vertical) :</span><span class="sxs-lookup"><span data-stu-id="88c68-283">**Name** Filter by WAN links (the filter is on the right side of the graph).The prefix denotes the following link types; see the vertical (blue) box:</span></span>
    
      - <span data-ttu-id="88c68-284">**S Site (S (site))** Liaison de réseau étendu entre un site réseau et une région réseau</span><span class="sxs-lookup"><span data-stu-id="88c68-284">**S Site** The WAN link from a network site to a network region</span></span>
    
      - <span data-ttu-id="88c68-285">**IS Inter-Site (IS (intersite))** Liaison de réseau étendu entre deux sites réseau</span><span class="sxs-lookup"><span data-stu-id="88c68-285">**IS Inter-Site** The WAN link between two network sites</span></span>
    
      - <span data-ttu-id="88c68-286">**R Inter-Region (R (inter-régions))** Liaison de réseau étendu entre deux régions réseau</span><span class="sxs-lookup"><span data-stu-id="88c68-286">**R Inter-Region** The WAN link between two network region</span></span>

2.  <span data-ttu-id="88c68-287">**Exceeded limit (Limite dépassée)** Filtrage des liaisons de réseau étendu pour lesquelles l’utilisation de la bande passante est supérieure à la capacité de bande passante</span><span class="sxs-lookup"><span data-stu-id="88c68-287">**Exceeded limit** Filter by WAN links whose bandwidth utilization is more than the bandwidth capacity</span></span>

3.  <span data-ttu-id="88c68-288">**Critical levels (Niveaux critiques)** Filtrage des liaisons de réseau étendu pour lesquelles l’utilisation de la bande passante a atteint 90 % ou plus de la capacité de bande passante</span><span class="sxs-lookup"><span data-stu-id="88c68-288">**Critical levels** Filter by WAN links whose bandwidth utilization has reached 90% or more than the bandwidth capacity</span></span>

4.  <span data-ttu-id="88c68-289">**Under-utilized (Sous-utilisé)** Filtrage des liaisons de réseau étendu pour lesquelles l’utilisation de la bande passante est inférieure à 25 % de la capacité de bande passante</span><span class="sxs-lookup"><span data-stu-id="88c68-289">**Under-utilized** Filter by WAN links whose bandwidth utilization has been less than 25% of the bandwidth capacity</span></span>

5.  <span data-ttu-id="88c68-290">**Link type (Type de liaison)** Filtrage des types de liaisons de réseau étendu suivants :</span><span class="sxs-lookup"><span data-stu-id="88c68-290">**Link type** Filter by the following WAN links types:</span></span>
    
      - <span data-ttu-id="88c68-291">**Network site (Site réseau)**</span><span class="sxs-lookup"><span data-stu-id="88c68-291">**Network site** type</span></span>
    
      - <span data-ttu-id="88c68-292">**Inter-site (intersite)**</span><span class="sxs-lookup"><span data-stu-id="88c68-292">**Inter-site** type</span></span>
    
      - <span data-ttu-id="88c68-293">**Inter-Region (Inter-régions)**</span><span class="sxs-lookup"><span data-stu-id="88c68-293">**Inter-Region link** type</span></span>

6.  <span data-ttu-id="88c68-294">**Region (Région)** Filtrage de la région réseau</span><span class="sxs-lookup"><span data-stu-id="88c68-294">**Region** Filter by network region</span></span>

<span data-ttu-id="88c68-295">Les figures suivantes présentent les filtres décrits précédemment.</span><span class="sxs-lookup"><span data-stu-id="88c68-295">The following figures show the previously described filters.</span></span>

<span data-ttu-id="88c68-p125">Filtrage sur **Name (Nom)**. Sélectionnez la liste des liaisons devant être affichées dans le graphique.</span><span class="sxs-lookup"><span data-stu-id="88c68-p125">Filter by **Name**. Select the list of links that need to be displayed in the graph.</span></span>

<span data-ttu-id="88c68-298">![Filtrage par nom dans BandwidthUtilizationAnalyzer.](images/JJ945604.002b7c8e-f0da-48ce-9e1a-5c34d2cab063(OCS.15).jpg "Filtrage par nom dans BandwidthUtilizationAnalyzer.")</span><span class="sxs-lookup"><span data-stu-id="88c68-298">![Filtering by Name in BandwidthUtilizationAnalyzer.](images/JJ945604.002b7c8e-f0da-48ce-9e1a-5c34d2cab063(OCS.15).jpg "Filtering by Name in BandwidthUtilizationAnalyzer.")</span></span>

<span data-ttu-id="88c68-299">Filtrage sur **Exceeded limit (Limite dépassée)**.</span><span class="sxs-lookup"><span data-stu-id="88c68-299">Filter by **Exceeded limit**.</span></span> <span data-ttu-id="88c68-300">Sélectionnez **True** pour appliquer le filtre.</span><span class="sxs-lookup"><span data-stu-id="88c68-300">Select **True** to enforce the filter.</span></span>

<span data-ttu-id="88c68-301">![Filtrage par limite dépassée.](images/JJ945604.5946c95e-76ce-46ca-8f3e-a79be1e5c527(OCS.15).jpg "Filtrage par limite dépassée.")</span><span class="sxs-lookup"><span data-stu-id="88c68-301">![Filtering by Exceeded Limit.](images/JJ945604.5946c95e-76ce-46ca-8f3e-a79be1e5c527(OCS.15).jpg "Filtering by Exceeded Limit.")</span></span>

<span data-ttu-id="88c68-302">Filtrage sur **Critical levels (Niveaux critiques)**.</span><span class="sxs-lookup"><span data-stu-id="88c68-302">Filter by **Critical levels**.</span></span> <span data-ttu-id="88c68-303">Sélectionnez **True** pour appliquer le filtre.</span><span class="sxs-lookup"><span data-stu-id="88c68-303">Select **True** to enforce the filter.</span></span>

<span data-ttu-id="88c68-304">![Filtrage par niveaux critiques.](images/JJ945604.60771a52-d8ba-4cb9-a02d-d6c888cb5505(OCS.15).jpg "Filtrage par niveaux critiques.")</span><span class="sxs-lookup"><span data-stu-id="88c68-304">![Filtering by Critical Levels.](images/JJ945604.60771a52-d8ba-4cb9-a02d-d6c888cb5505(OCS.15).jpg "Filtering by Critical Levels.")</span></span>

<span data-ttu-id="88c68-305">Filtrage sur **Under utilized (Sous-utilisé)**.</span><span class="sxs-lookup"><span data-stu-id="88c68-305">Filter by **Under utilized**.</span></span> <span data-ttu-id="88c68-306">Sélectionnez **True** pour appliquer le filtre.</span><span class="sxs-lookup"><span data-stu-id="88c68-306">Select **True** to enforce the filter.</span></span>

<span data-ttu-id="88c68-307">![Filtrage en sous utilisé.](images/JJ945604.95a2bf01-5aba-4927-af47-1ad3c459d791(OCS.15).jpg "Filtrage en sous utilisé.")</span><span class="sxs-lookup"><span data-stu-id="88c68-307">![Filtering by Under Utilized.](images/JJ945604.95a2bf01-5aba-4927-af47-1ad3c459d791(OCS.15).jpg "Filtering by Under Utilized.")</span></span>

<span data-ttu-id="88c68-308">Filtrage sur **Link Type (Type de liaison)**.</span><span class="sxs-lookup"><span data-stu-id="88c68-308">Filter by **Link Type**.</span></span> <span data-ttu-id="88c68-309">Sélectionnez le ou les types devant être affichés.</span><span class="sxs-lookup"><span data-stu-id="88c68-309">Select the type or types that need to be displayed.</span></span>

<span data-ttu-id="88c68-310">![Filtrage par type de lien.](images/JJ945604.08757949-06bd-4cf3-809f-d81fd23a6639(OCS.15).jpg "Filtrage par type de lien.")</span><span class="sxs-lookup"><span data-stu-id="88c68-310">![Filtering by Link Type.](images/JJ945604.08757949-06bd-4cf3-809f-d81fd23a6639(OCS.15).jpg "Filtering by Link Type.")</span></span>

<span data-ttu-id="88c68-311">Filtrage sur **Region (Région)**.</span><span class="sxs-lookup"><span data-stu-id="88c68-311">Filter by **Region**.</span></span> <span data-ttu-id="88c68-312">Sélectionnez la liste des régions pour lesquelles afficher les liaisons.</span><span class="sxs-lookup"><span data-stu-id="88c68-312">Select a list of regions whose links need to be displayed.</span></span>

<span data-ttu-id="88c68-313">![Filtrage par région.](images/JJ945604.5de4cec4-6c09-48bb-98c7-b56f7bdb3d5a(OCS.15).jpg "Filtrage par région.")</span><span class="sxs-lookup"><span data-stu-id="88c68-313">![Filtering by Region.](images/JJ945604.5de4cec4-6c09-48bb-98c7-b56f7bdb3d5a(OCS.15).jpg "Filtering by Region.")</span></span>

</div>

</div>

</div>

<div>

## <a name="requirements"></a><span data-ttu-id="88c68-314">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="88c68-314">Requirements</span></span>

  - <span data-ttu-id="88c68-315">.NET Framework 3.5</span><span class="sxs-lookup"><span data-stu-id="88c68-315">The .NET Framework 3.5</span></span>

  - <span data-ttu-id="88c68-316">Microsoft Excel 2010 ou Excel 2007</span><span class="sxs-lookup"><span data-stu-id="88c68-316">Microsoft Excel 2010 or Excel 2007</span></span>

</div>

<div>

## <a name="summary"></a><span data-ttu-id="88c68-317">Résumé</span><span class="sxs-lookup"><span data-stu-id="88c68-317">Summary</span></span>

<span data-ttu-id="88c68-p131">Bandwidth Utilization Analyzer permet de représenter l’utilisation de la bande passante audio pour le trafic des communications unifiées dans le réseau. Il permet également de créer des rapports sur l’utilisation de la bande passante vidéo dans le réseau.</span><span class="sxs-lookup"><span data-stu-id="88c68-p131">Bandwidth Utilization Analyzer is used to plot the audio bandwidth utilization for UC traffic across the network. This tool can be used to report the utilization of video bandwidth on the network as well.</span></span>

</div>

</div>

<div>

## <a name="call-parkometer"></a><span data-ttu-id="88c68-320">Call Parkometer</span><span class="sxs-lookup"><span data-stu-id="88c68-320">Call Parkometer</span></span>

<span data-ttu-id="88c68-321">L’application en ligne de commande Call Parkometer permet d’accéder facilement à la base de données des orbites de parcage d’appel.</span><span class="sxs-lookup"><span data-stu-id="88c68-321">Call Parkometer is a command-line application that provides easy access to the Call Park orbit database.</span></span>

<div>

## <a name="description"></a><span data-ttu-id="88c68-322">Description</span><span class="sxs-lookup"><span data-stu-id="88c68-322">Description</span></span>

<span data-ttu-id="88c68-323">L’outil Call Parkometer permet de suivre les appels actuellement parqués.</span><span class="sxs-lookup"><span data-stu-id="88c68-323">Call Parkometer is a tool to track currently parked calls.</span></span> <span data-ttu-id="88c68-324">Il collecte également des statistiques sur les orbites et l’utilisation du serveur de parcage d’appel.</span><span class="sxs-lookup"><span data-stu-id="88c68-324">It also collects statistics about orbits and Call Park Server (CPS) usage.</span></span> <span data-ttu-id="88c68-325">Cet outil de ligne de commande fournit les deux accès en lecture et en écriture à la base de données SQL Server de CPS orbite à partir d’un ordinateur connecté localement ou distant.</span><span class="sxs-lookup"><span data-stu-id="88c68-325">This command-line tool provides both read and write-access to the CPS orbit SQL Server database from a local or remotely connected computer.</span></span>

<span data-ttu-id="88c68-p133">Toutes les options s’excluent mutuellement. La syntaxe suivante est appliquée à la ligne de commande :</span><span class="sxs-lookup"><span data-stu-id="88c68-p133">All options are mutually exclusive. Command-line syntax is as follows:</span></span>

  - <span data-ttu-id="88c68-328">
            Paramètre \*\*–o\*\* : répertorie toutes les plages d’orbites configurées pour ce pool.</span><span class="sxs-lookup"><span data-stu-id="88c68-328">**–o** parameter—lists all orbit ranges configured for this pool.</span></span>

  - <span data-ttu-id="88c68-p134">
            Paramètre \*\*–n\*\* : répertorie toutes les orbites actuellement utilisées dans ce pool. Les informations suivantes sont affichées :</span><span class="sxs-lookup"><span data-stu-id="88c68-p134">**–n** parameter—lists all currently used orbits in this pool. The information displayed is as follows:</span></span>
    
      - <span data-ttu-id="88c68-331">URI (Uniform Resource Identifier) SIP du parqué et du parqueur.</span><span class="sxs-lookup"><span data-stu-id="88c68-331">SIP Uniform Resource Identifier (URI) of the parkee and parker.</span></span>
    
      - <span data-ttu-id="88c68-332">Nom d’hôte du serveur de parcage d’appel sur lequel l’appel est parqué.</span><span class="sxs-lookup"><span data-stu-id="88c68-332">Host name of the CPS where the call is parked.</span></span>
    
      - <span data-ttu-id="88c68-333">Date/heure du parcage de l’appel.</span><span class="sxs-lookup"><span data-stu-id="88c68-333">Time stamp of when the call was parked.</span></span>

  - <span data-ttu-id="88c68-334">
            Paramètre \*\*–f\*\* : indique le nombre d’orbites actuellement libres dans le pool.</span><span class="sxs-lookup"><span data-stu-id="88c68-334">**–f** parameter—lists the number of currently free orbits in the pool.</span></span>

  - <span data-ttu-id="88c68-335">**-r \<n\>** paramètre : affiche la liste des \<n\> derniers appels en stationnement.</span><span class="sxs-lookup"><span data-stu-id="88c68-335">**–r \<n\>** parameter—lists the \<n\> last parked calls.</span></span> <span data-ttu-id="88c68-336">Les informations suivantes sont affichées :</span><span class="sxs-lookup"><span data-stu-id="88c68-336">The information displayed is as follows:</span></span>
    
      - <span data-ttu-id="88c68-337">URI SIP du parqué.</span><span class="sxs-lookup"><span data-stu-id="88c68-337">Parkee SIP URI.</span></span>
    
      - <span data-ttu-id="88c68-338">URI SIP du parqueur.</span><span class="sxs-lookup"><span data-stu-id="88c68-338">Parker SIP URI.</span></span>
    
      - <span data-ttu-id="88c68-339">Nom d’hôte du serveur de parcage d’appel sur lequel l’appel est parqué.</span><span class="sxs-lookup"><span data-stu-id="88c68-339">Host name of the CPS where the call was parked.</span></span>
    
      - <span data-ttu-id="88c68-340">Date/heure de récupération ou d’abandon de l’appel.</span><span class="sxs-lookup"><span data-stu-id="88c68-340">Time stamp of when the call was retrieved or dropped.</span></span>

  - <span data-ttu-id="88c68-341">**-t \<n\>** tests de paramètre réservant une orbite dans la base de données afin d’afficher la randomisation des numéros d’orbites attribués.</span><span class="sxs-lookup"><span data-stu-id="88c68-341">**-t\<n\>** parameter - tests reserving an orbit in the database to show the randomness of the assigned orbit numbers.</span></span>

</div>

<div>

## <a name="output"></a><span data-ttu-id="88c68-342">Sortie</span><span class="sxs-lookup"><span data-stu-id="88c68-342">Output</span></span>

<span data-ttu-id="88c68-343">Selon les paramètres d’entrée spécifiés dans l’invite de commandes, l’outil Call Parkometer affiche la sortie suivante :</span><span class="sxs-lookup"><span data-stu-id="88c68-343">Depending on the input parameters that are specified at a command prompt, Call Parkometer displays the following output:</span></span>

  - <span data-ttu-id="88c68-344">plages d’orbites configurées pour ce pool ;</span><span class="sxs-lookup"><span data-stu-id="88c68-344">All orbit ranges that are configured for this pool</span></span>

  - <span data-ttu-id="88c68-345">appels actuellement parqués ;</span><span class="sxs-lookup"><span data-stu-id="88c68-345">Currently parked calls</span></span>

  - <span data-ttu-id="88c68-346">nombre d’orbites libres (disponibles) ;</span><span class="sxs-lookup"><span data-stu-id="88c68-346">Number of free (available) orbits</span></span>

  - <span data-ttu-id="88c68-347">appels parqués récemment ;</span><span class="sxs-lookup"><span data-stu-id="88c68-347">Recently parked calls</span></span>

  - <span data-ttu-id="88c68-348">orbites réservées pour le test des valeurs d’orbite uniformes et aléatoires.</span><span class="sxs-lookup"><span data-stu-id="88c68-348">Reserved orbits for testing uniform and random orbit values</span></span>

</div>

<div>

## <a name="purpose"></a><span data-ttu-id="88c68-349">Objectif</span><span class="sxs-lookup"><span data-stu-id="88c68-349">Purpose</span></span>

<span data-ttu-id="88c68-p136">L’outil CPS vie à fournir un accès par ligne de commande à la base de données du serveur de parcage d’appel. L’administrateur peut consulter l’utilisation du serveur de parcage d’appel et déterminer le nombre d’orbites affectées à un pool.</span><span class="sxs-lookup"><span data-stu-id="88c68-p136">The purpose of the CPS tool is to provide command-line access to the CPS database. The administrator can view the CPS usage and determine the number of orbits assigned to a pool.</span></span>

</div>

<div>

## <a name="requirements"></a><span data-ttu-id="88c68-352">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="88c68-352">Requirements</span></span>

<span data-ttu-id="88c68-353">Aucune configuration n’est requise si cet outil est exécuté sur l’ordinateur qui exécute le serveur de parcage d’appel.</span><span class="sxs-lookup"><span data-stu-id="88c68-353">There are no requirements if this tool is run on the same computer that is running CPS.</span></span> <span data-ttu-id="88c68-354">Si cet outil est exécuté sur un ordinateur distant, la base de données SQL Server utilisée par Lync Server 2013 doit être configurée pour autoriser l’accès à distance.</span><span class="sxs-lookup"><span data-stu-id="88c68-354">If this tool is run on a remote computer, the SQL Server database used by Lync Server 2013 must be configured to allow remote access.</span></span> <span data-ttu-id="88c68-355">L’appel de Parkometer doit être configuré à l’aide d’une chaîne de connexion de base de données SQL Server pour se connecter au serveur SQL Server du pool.</span><span class="sxs-lookup"><span data-stu-id="88c68-355">Call Parkometer must be configured with a SQL Server database connection string to connect to the pool’s SQL Server.</span></span> <span data-ttu-id="88c68-356">Cette chaîne de connexion de base de données SQL Server est définie dans le fichier de configuration **parkometer.exe.config**. Il doit être placé dans le même répertoire que parkometer.exe.</span><span class="sxs-lookup"><span data-stu-id="88c68-356">This SQL Server database connection string is defined in the configuration file, **parkometer.exe.config**. It must be placed in the same directory where parkometer.exe is located.</span></span> <span data-ttu-id="88c68-357">Le fichier XML suivant est un exemple de parkometer.exe.config. Le nom d’utilisateur (par exemple, « monmotdepasse »), le \\ mot de passe (par exemple, la monmotdepasse) et le nom d’hôte (par exemple, « MyServer »).</span><span class="sxs-lookup"><span data-stu-id="88c68-357">The following XML file is an example of a parkometer.exe.config. The parameters that must be configured are user name (for example, mydomain\\Administrator), password (for example, mypassword), and host name (for example, myserver).</span></span>

```xml
    <?xml version="1.0" encoding="utf-8" ?>
    <configuration>
      <appSettings>
       <add key="SQL" value="server=myserver\RTC;
    database=cpsdyn;
    User Id=mydomain\Administrator;
    Password=mypassword.;
    Integrated Security=false;"/>
      </appSettings>
    </configuration>
```

</div>

<div>

## <a name="examples"></a><span data-ttu-id="88c68-358">Exemples</span><span class="sxs-lookup"><span data-stu-id="88c68-358">Examples</span></span>

<span data-ttu-id="88c68-359">Plages d’orbites déployées : le paramètre –o répertorie les plages d’orbites configurées pour ce pool</span><span class="sxs-lookup"><span data-stu-id="88c68-359">Deployed orbit ranges: the –o parameter lists all orbit ranges that are configured for this pool as shown</span></span>

<span data-ttu-id="88c68-360">![Plages orbites dans Parkometer d’appel.](images/JJ945604.9ede64cb-29d9-4782-a34b-b76c42fbdcad(OCS.15).jpg "Plages orbites dans Parkometer d’appel.")</span><span class="sxs-lookup"><span data-stu-id="88c68-360">![Orbit ranges in Call Parkometer.](images/JJ945604.9ede64cb-29d9-4782-a34b-b76c42fbdcad(OCS.15).jpg "Orbit ranges in Call Parkometer.")</span></span>

<span data-ttu-id="88c68-361">Appels actuellement parqués : le paramètre –n répertorie les orbites actuellement utilisées sur ce pool</span><span class="sxs-lookup"><span data-stu-id="88c68-361">Currently parked calls: the –n parameter lists all currently used orbits on this pool as shown</span></span>

<span data-ttu-id="88c68-362">![Appels actuellement en cours d’appel dans Parkometer.](images/JJ945604.07a7eec4-7999-4c92-93f0-95525b244b4c(OCS.15).jpg "Appels actuellement en cours d’appel dans Parkometer.")</span><span class="sxs-lookup"><span data-stu-id="88c68-362">![Currently-parked calls in Call Parkometer.](images/JJ945604.07a7eec4-7999-4c92-93f0-95525b244b4c(OCS.15).jpg "Currently-parked calls in Call Parkometer.")</span></span>

<span data-ttu-id="88c68-363">Nombre d’orbites libres : le paramètre –f indique le nombre d’orbites actuellement libres dans le pool</span><span class="sxs-lookup"><span data-stu-id="88c68-363">Number of free orbits: the –f parameter lists the number of currently free orbits in the pool as shown</span></span>

<span data-ttu-id="88c68-364">![Orbites libres dans Parkometer d’appel.](images/JJ945604.ecc1d621-0ca0-4ecf-a579-08b41c6f08ed(OCS.15).jpg "Orbites libres dans Parkometer d’appel.")</span><span class="sxs-lookup"><span data-stu-id="88c68-364">![Free orbits in Call Parkometer.](images/JJ945604.ecc1d621-0ca0-4ecf-a579-08b41c6f08ed(OCS.15).jpg "Free orbits in Call Parkometer.")</span></span>

<span data-ttu-id="88c68-365">Appels récemment mis en garde : le paramètre – r \<n\> recense les \<n\> derniers appels parqués, comme illustré ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="88c68-365">Recently parked calls: the –r \<n\> parameter lists the \<n\> last parked calls as shown</span></span>

<span data-ttu-id="88c68-366">![Appels récemment dans le Parkometer.](images/JJ945604.1c5eb27d-faa1-491b-b4aa-b484255c3353(OCS.15).jpg "Appels récemment dans le Parkometer.")</span><span class="sxs-lookup"><span data-stu-id="88c68-366">![Recently-parked calls in Call Parkometer.](images/JJ945604.1c5eb27d-faa1-491b-b4aa-b484255c3353(OCS.15).jpg "Recently-parked calls in Call Parkometer.")</span></span>

<span data-ttu-id="88c68-367">Test de réservation orbite : les \<n\> tests de paramètre – t servent à réapprovisionner une orbite dans la base de données, comme illustré</span><span class="sxs-lookup"><span data-stu-id="88c68-367">Test orbit reservation: the –t \<n\> parameter tests reserving an orbit in the database as shown</span></span>

<span data-ttu-id="88c68-368">![Testez les réservations orbites dans l’appel Parkometer.](images/JJ945604.84c9b69e-7af0-4224-8711-a43a28f08691(OCS.15).jpg "Testez les réservations orbites dans l’appel Parkometer.")</span><span class="sxs-lookup"><span data-stu-id="88c68-368">![Test orbit reservations in Call Parkometer.](images/JJ945604.84c9b69e-7af0-4224-8711-a43a28f08691(OCS.15).jpg "Test orbit reservations in Call Parkometer.")</span></span>

</div>

<div>

## <a name="summary"></a><span data-ttu-id="88c68-369">Résumé</span><span class="sxs-lookup"><span data-stu-id="88c68-369">Summary</span></span>

<span data-ttu-id="88c68-370">L’outil en ligne de commande Call Parkometer fournit des informations détaillées sur le serveur de parcage d’appel.</span><span class="sxs-lookup"><span data-stu-id="88c68-370">Call Parkometer is a command-line tool that provides detailed information about the Call Park Server.</span></span>

</div>

</div>

<div>

## <a name="cleanupstorageservicedata"></a><span data-ttu-id="88c68-371">CleanupStorageServiceData</span><span class="sxs-lookup"><span data-stu-id="88c68-371">CleanupStorageServiceData</span></span>

<span data-ttu-id="88c68-372">Le kit de ressources de CleanupStorageServiceData permet la suppression des données orphelines de la base de données utilisée par le service de stockage Lync Server (LYSS).</span><span class="sxs-lookup"><span data-stu-id="88c68-372">The CleanupStorageServiceData resource kit tool allows for deleting of orphaned data from the database used by the Lync Server Storage Service (LYSS).</span></span> <span data-ttu-id="88c68-373">La seule fonction du service de stockage consiste à mettre en tampon la communication entre Lync Server et les différents points de terminaison de stockage des données principaux tels que SQL Server et Exchange.</span><span class="sxs-lookup"><span data-stu-id="88c68-373">One function of the storage service is to buffer communication between Lync Server and various back-end data storage endpoints, like SQL Server and Exchange.</span></span>

<div>

## <a name="description"></a><span data-ttu-id="88c68-374">Description</span><span class="sxs-lookup"><span data-stu-id="88c68-374">Description</span></span>

<span data-ttu-id="88c68-375">Pour prendre en charge une haute disponibilité, LYSS accepte et enregistre temporairement des copies de ces données sur plusieurs serveurs frontaux du pool, et supprime ces données une fois qu’elles ont été transmises à l’emplacement de stockage de longue durée final.</span><span class="sxs-lookup"><span data-stu-id="88c68-375">To support high availability, LYSS accepts and saves copies of the data on multiple front end servers in the pool temporarily, and removes that data once it has been delivered to its final long-term storage location.</span></span> <span data-ttu-id="88c68-376">Dans le cas d’une opération normale, il est possible qu’il n’y ait pas de situations normales, qu’un serveur se bloque ou rencontre un problème de traitement et que certaines données ne soient pas nettoyées correctement.</span><span class="sxs-lookup"><span data-stu-id="88c68-376">There are unusual situations which may occur during otherwise normal operation, when a server might crash or experience a processing issue, and some data might not get cleaned up properly.</span></span> <span data-ttu-id="88c68-377">Ces données sont inoffensives, mais elles consomment des ressources de traitement limitées.</span><span class="sxs-lookup"><span data-stu-id="88c68-377">This data is harmless, but it does consume limited processing resources.</span></span> <span data-ttu-id="88c68-378">La plupart des opérations de maintenance de données requises normales sont automatisées, mais cet outil permet d’identifier et de supprimer en toute sécurité ces données orphelines lorsque la suppression automatisée n’est pas possible.</span><span class="sxs-lookup"><span data-stu-id="88c68-378">Much of the normal required data maintenance is automated, but this tool allows for the safe identification and removal of such orphaned data when automated removal is not possible.</span></span> <span data-ttu-id="88c68-379">L’utilisation de cet outil est indiquée lors du déclenchement d’une alerte de système d’exploitation du gestionnaire d’intégrité, qui demande à l’administrateur de supprimer les données inutiles des bases de données LYSS locales du pool.</span><span class="sxs-lookup"><span data-stu-id="88c68-379">Usage of this tool is indicated when a health monitoring System Center Operations Manager (SCOM) alert is raised which asks the administrator to remove the unneeded data from the local LYSS databases in the pool.</span></span> <span data-ttu-id="88c68-380">Il s’agit d’un événement correspondant dans le journal des événements sur le front end qui déclenchait l’alerte.</span><span class="sxs-lookup"><span data-stu-id="88c68-380">There will be a corresponding event in the event log on the front end which triggered the alert.</span></span> <span data-ttu-id="88c68-381">Les détails de l’événement contiennent les informations relatives à la quantité de données orphelines contenues sur le front end et sont déclenchées lorsque ces données dépassent certains seuils prédéfinis.</span><span class="sxs-lookup"><span data-stu-id="88c68-381">The event details will contain information about the amount of orphaned data contained on the front end, and is raised when that data exceeds certain pre-determine thresholds</span></span>

</div>

<div>

## <a name="requirements"></a><span data-ttu-id="88c68-382">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="88c68-382">Requirements</span></span>

<span data-ttu-id="88c68-383">Installez les outils du kit de ressources de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="88c68-383">Install the Lync Server 2013, Resource Kit Tools.</span></span> <span data-ttu-id="88c68-384">L’outil s’exécute sur des ordinateurs liés à un domaine dans lesquels Lync Server et Lync Server 2013 Management Shell sont installés.</span><span class="sxs-lookup"><span data-stu-id="88c68-384">The tool runs on domain-joined machines where Lync Server and Lync Server 2013 Management Shell are installed.</span></span> <span data-ttu-id="88c68-385">L’outil utilise une cmdlet de Management Shell pour identifier tous les serveurs frontaux dans la liste.</span><span class="sxs-lookup"><span data-stu-id="88c68-385">The tool uses a cmdlet from the management shell to identify all Front End servers in the pool.</span></span> <span data-ttu-id="88c68-386">Deuxièmement, l’outil doit être exécuté à partir d’un ordinateur du pool sur lequel la base de données **RtcLocal** est installée.</span><span class="sxs-lookup"><span data-stu-id="88c68-386">Secondly, the tool must be executed from a machine in the pool which has the **RtcLocal** database installed.</span></span> <span data-ttu-id="88c68-387">Cette base de données est utilisée par l’outil CleanupStorageServiceData pour obtenir les détails de connexion nécessaires pour communiquer avec le service de routage de Lync Server. Enfin, le compte ou les informations d’identification appelant l’outil doivent disposer d’autorisations en lecture/écriture sur le partage de fichiers sur lequel il souhaite écrire le journal de sortie. Par ailleurs, cet outil dépend du niveau de cohérence de l’État.</span><span class="sxs-lookup"><span data-stu-id="88c68-387">This database is used by the CleanupStorageServiceData tool to get the connection details needed to communicate with the Lync Server Routing Service.Finally, the account or credential invoking the tool must have read/write permission to the file share to which they want to write the output log.Also, this tool depends on the pool being in a stable state.</span></span> <span data-ttu-id="88c68-388">Par essence cela signifie que chaque serveur frontal doit être en cours d’exécution, que l’instance SQL Server LYNCLOCAL et la base de données LYSS doivent être en mesure de se connecter, et chaque groupe de routage doit disposer d’un ensemble complet de 1 serveur frontal principal et de deux serveurs front-end secondaires.</span><span class="sxs-lookup"><span data-stu-id="88c68-388">In essence this means that every Front End server is expected to be up and running, the SQL Server LYNCLOCAL instance and LYSS database must be able to be connected to, and each routing group must have a complete set of 1 primary Front End servers and 2 secondary Front End servers.</span></span>

</div>

<div>

## <a name="examples"></a><span data-ttu-id="88c68-389">Exemples</span><span class="sxs-lookup"><span data-stu-id="88c68-389">Examples</span></span>

<span data-ttu-id="88c68-390">C : \\ Program Files \\ Microsoft Lync Server 2013 \\ reskit \\ StorageService \> ImportStorageServiceData.exe</span><span class="sxs-lookup"><span data-stu-id="88c68-390">C:\\Program Files\\Microsoft Lync Server 2013\\ResKit\\StorageService\> ImportStorageServiceData.exe</span></span>

    Description:
    This tool will remove orphaned data from the Storage Service database
    for a pool. You are required to run this tool on a machine inside the
    pool which has the Lync Server Management Shell installed and has RtcLocal database installed.
    Usage: Default behavior is to clean up orphaned data from the all the 
           Storage Service databases in the current pool.
    Additional Options:
    -Verbose    : Turn verbose output on.
    -LogPath    : The UNC path to which to write the log.
    ------------------------------------------------------------------------------
    Please wait while we initialize...
    Found 4 front end servers
    Replica Instances for LYSS Service
    Address: server2.vdomain.com - Primaries: 7 Secondaries: 14
    Address: server.vdomain.com - Primaries: 7 Secondaries: 14
    Address: server1.vdomain.com - Primaries: 7 Secondaries: 14
    Address: server3.vdomain.com - Primaries: 7 Secondaries: 14
    Primary Total Count = 28, Secondary Total Count = 56
    Finding and removing orphaned data for 28 routing groups
    Removing 1 stale groups from FE server.vdomain.com
    No stale routing groups detected on FE server2.vdomain.com
    No stale routing groups detected on FE server1.vdomain.com
    No stale routing groups detected on FE server3.vdomain.com
    Searching for stale queue items
    Removed 20 stale queue items for routing group 17D5435AE40259F7BBDF1866776386E4
    No stale queue items found for routing group 1975349662315F90B119DACB4F2AE3AD
    No stale queue items found for routing group 1A23E3D58BDB5A458A0B73F34AB7ACBE
    No stale queue items found for routing group 1AC91E3A1029535A80123121989CEADC
    No stale queue items found for routing group 3313935458E35B9B9759E08A15D251E6
    No stale queue items found for routing group 39BB0035B06B5427873FC6099720462A
    No stale queue items found for routing group 40721948E7B55CE893A53E911F76D185
    No stale queue items found for routing group 4501E04EAE4856059346949FF817C220
    No stale queue items found for routing group 4D833C98801F546F8E45E417EE028E2E
    No stale queue items found for routing group 5AD77443AD955A22A876749BE66D5317
    No stale queue items found for routing group 69844A271E6C5633A1F2B46A42287DD6
    No stale queue items found for routing group 69DA3BE407A95C7284EB4B1337718C93
    No stale queue items found for routing group 8437358AB34A5CC8967D5EF39494AB8D
    No stale queue items found for routing group 8ED455B1789655359816E1C5BF4C430F
    No stale queue items found for routing group 904F6C9B8AC951AE8B3C86684D3832E4
    No stale queue items found for routing group 90AAB3AE9A1950E0ADE7809A27021D63
    No stale queue items found for routing group 944F5724C65C5F93900DC1C8C898B102
    No stale queue items found for routing group 9E8A2630250C51769E39F63F0FB552BA
    No stale queue items found for routing group A11E27AE439A582288D4657EDA86B565
    No stale queue items found for routing group A9B10C76E764556FAEA3E47301EDF518
    No stale queue items found for routing group AEA2699E74ED59848ACEA7896699430D
    No stale queue items found for routing group B269961603E75065AFDA4F4F006DA5E4
    No stale queue items found for routing group BB873D9A3DA959DAB2FD743E5AA619F7
    No stale queue items found for routing group BCC6A48FBA2454B79B9EDB276657A404
    No stale queue items found for routing group C8EF4805722B5F6C876EBC0440B420FD
    No stale queue items found for routing group CA38EBDAC4845489ACE208C2240E4056
    No stale queue items found for routing group F5921887DB025C5F908CE42DB7F1AEE8
    No stale queue items found for routing group F9E606A825395422B3BF7A01ECBB7B1F
    Writing log: M:\Dev\Server\ResKit\StorageService\CleanupStorageServiceData.Log_20121009_151040
    Tool has finished execution.  Errors encountered: 0
    C:\Program Files\Microsoft Lync Server 2013\ResKit\StorageService>

</div>

</div>

<div>

## <a name="dbanalyze"></a><span data-ttu-id="88c68-391">DBAnalyze</span><span class="sxs-lookup"><span data-stu-id="88c68-391">DBAnalyze</span></span>

<div>

## <a name="description"></a><span data-ttu-id="88c68-392">Description</span><span class="sxs-lookup"><span data-stu-id="88c68-392">Description</span></span>

<span data-ttu-id="88c68-393">DBAnalyze est un outil de ligne de commande qui permet aux administrateurs de collecter des rapports d’analyse sur les bases de données Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="88c68-393">DBAnalyze is a command-line tool that helps administrators to gather analysis reports about the Lync Server 2013 databases.</span></span> <span data-ttu-id="88c68-394">DBAnalyze inclut les modes suivants : diagnostic, données des utilisateurs, conférence, unités de contrôle multipoint et fragmentation des disques :</span><span class="sxs-lookup"><span data-stu-id="88c68-394">DBAnalyze has the following modes: diagnostic, user data, conference, MCUs, and disk fragmentation:</span></span>

  - <span data-ttu-id="88c68-395">**Diagnostic mode (Mode Diagnostic)**    Crée un rapport incluant des informations sur les tables (nombre d’enregistrements, fragmentation, taille des données et taille d’index), la taille des fichiers de données et des fichiers journaux, l’heure de la dernière sauvegarde, la répartition des contacts entre les serveurs exécutant Microsoft Office Communications Server, le nombre moyen d’autorisations, les contacts, les conteneurs, les abonnements, les publications, les points de terminaison par utilisateur, les éventuels utilisateurs hébergés de façon incorrecte, les utilisateurs ne pouvant pas être acheminés, le nombre moyen de conférences organisées par utilisateur, les conférences planifiées, les conférences actives et la version des bases de données.</span><span class="sxs-lookup"><span data-stu-id="88c68-395">**Diagnostic mode**   Creates a report that includes information about tables (number of records, fragmentation, data size, and index size), data and log file sizes, the last back-up time, contact distribution among servers that are running Microsoft Office Communications Server, the average number of permissions, contacts, containers, subscriptions, publications, endpoints per user, any improperly homed users, users that can’t be routed, the average number of conferences organized per user, scheduled conferences, active conferences, and the database version.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="88c68-396">L’exécution du mode Diagnostic peut affecter les performances des serveurs.</span><span class="sxs-lookup"><span data-stu-id="88c68-396">Running diagnostic mode can affect server performance.</span></span>

    
    </div>

  - <span data-ttu-id="88c68-397">**Mode données utilisateur**  Signale les données de contact, de conteneur, d’abonnement, de composition, d’autorisation et de groupe de contacts pour un utilisateur spécifié ou pour les utilisateurs qui disposent de cet utilisateur dans leurs listes de contacts et d’autorisations.</span><span class="sxs-lookup"><span data-stu-id="88c68-397">**User data mode**  Reports contact, container, subscription, publication, permission, and contact-group data for a specified user or for users who have that user in their contact and permission lists.</span></span> <span data-ttu-id="88c68-398">Ce mode transmet également des données résumées sur les conférences organisées par un utilisateur ou auxquelles il est invité.</span><span class="sxs-lookup"><span data-stu-id="88c68-398">This mode also reports summary data for conferences that a user organizes or is invited to.</span></span>

  - <span data-ttu-id="88c68-399">**Conference mode (Mode Conférence)**    Transmet des données détaillées sur une conférence spécifique (heure planifiée, liste des invités, liste des types de média autorisés, unités de contrôle multipoint actives, liste des participants actifs, état de signalisation des participants).</span><span class="sxs-lookup"><span data-stu-id="88c68-399">**Conference mode**   Reports detailed data for a specific conference, including all schedule-time details for the conference, the invitee list, the list of media types allowed for the conference, active MCUs (multipoint control units), the active participant list, and each participant’s signaling state.</span></span>

  - <span data-ttu-id="88c68-400">**Decode Meeting ID (Décodage de l’ID de réunion)**   Décode un ID de réunion PSTN spécifié par le commutateur **/pstnid** sans se connecter au serveur principal pour obtenir des informations détaillées.</span><span class="sxs-lookup"><span data-stu-id="88c68-400">**Decode Meeting ID**  Decodes a public switched telephone network (PSTN) meeting ID that is specified by the **/pstnid** switch but does not connect to the back end for detailed information.</span></span>

  - <span data-ttu-id="88c68-401">**Resolve conference (Résolution d’une conférence)**    Décode un ID de réunion PSTN spécifié par le commutateur **/pstnid** et affiche des informations sur la conférence indiquée par l’ID.</span><span class="sxs-lookup"><span data-stu-id="88c68-401">**Resolve conference**   Decodes a PSTN meeting ID that is specified by the **/pstnid** switch and displays information about the conference indicated by the ID.</span></span>

  - <span data-ttu-id="88c68-402">**MCUs mode (Mode Unités de contrôle multipoint)**   Indique l’ID, le type de média, l’URL, le statut de pulsation, la charge des conférences et la charge des participants pour chaque unité de contrôle multipoint du pool.</span><span class="sxs-lookup"><span data-stu-id="88c68-402">**MCUs mode**  Reports the ID, media type, URL, heartbeat status, conference load, and participant load for each MCU in the pool.</span></span>

  - <span data-ttu-id="88c68-403">**Disk fragmentation mode (Mode Fragmentation des disques)**   Affiche le statut de fragmentation des disques.</span><span class="sxs-lookup"><span data-stu-id="88c68-403">**Disk fragmentation mode**  Displays the fragmentation status of all disks.</span></span>

<span data-ttu-id="88c68-p143">Cet outil permet de diagnostiquer plusieurs problèmes ou de planifier la capacité. Par exemple, si la plupart des utilisateurs hébergés sur un serveur A définissent des utilisateurs hébergés sur le serveur B comme contacts, l’administrateur peut déplacer les utilisateurs du serveur A vers le serveur B afin de réduire le trafic entre les serveurs.</span><span class="sxs-lookup"><span data-stu-id="88c68-p143">This tool can be used to diagnose various problems or to assist administrators with capacity planning. For example, if most of the users homed on server A choose users homed on server B as their contacts, the administrator can move the users on server A to server B to reduce cross-server traffic.</span></span>

</div>

<div>

## <a name="output"></a><span data-ttu-id="88c68-406">Sortie</span><span class="sxs-lookup"><span data-stu-id="88c68-406">Output</span></span>

<span data-ttu-id="88c68-407">Cet outil génère des rapports prédéfinis sur la base de données Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="88c68-407">This tool outputs predefined reports about the Lync Server 2013 database.</span></span> <span data-ttu-id="88c68-408">**Chemin :** % ProgramFiles% \\ Microsoft Lync Server 2013 \\ reskit</span><span class="sxs-lookup"><span data-stu-id="88c68-408">**Path:** %ProgramFiles%\\Microsoft Lync Server 2013\\Reskit</span></span>

</div>

<div>

## <a name="purpose"></a><span data-ttu-id="88c68-409">Objectif</span><span class="sxs-lookup"><span data-stu-id="88c68-409">Purpose</span></span>

<span data-ttu-id="88c68-410">Pour installer Dbanalyze.exe, copiez-le dans un dossier local, puis exécutez l’outil.</span><span class="sxs-lookup"><span data-stu-id="88c68-410">To install Dbanalyze.exe, copy it to a local folder and then run the tool.</span></span> <span data-ttu-id="88c68-411">Pour utiliser l’outil, exécutez la commande suivante à partir de la ligne de commande.`dbanalyze.exe [/v] [/report:value] [/sqlserver:value] [/user:user@domain.com] [/conf:value][/pstnid:Value] [/maxcontacts:value]`</span><span class="sxs-lookup"><span data-stu-id="88c68-411">To use the tool, run the following command from the command line.`dbanalyze.exe [/v] [/report:value] [/sqlserver:value] [/user:user@domain.com] [/conf:value][/pstnid:Value] [/maxcontacts:value]`</span></span> <span data-ttu-id="88c68-412">Les descriptions des options de la ligne de commande sont décrites ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="88c68-412">The descriptions for the command-line options are shown below.</span></span>

<span data-ttu-id="88c68-413">![Options de ligne de commande pour les Dbanalyze.exe.](images/JJ945604.22bf3432-af6d-495b-8f48-d94c5d259523(OCS.15).jpg "Options de ligne de commande pour les Dbanalyze.exe.")</span><span class="sxs-lookup"><span data-stu-id="88c68-413">![Command line options for Dbanalyze.exe.](images/JJ945604.22bf3432-af6d-495b-8f48-d94c5d259523(OCS.15).jpg "Command line options for Dbanalyze.exe.")</span></span>

</div>

<div>

## <a name="requirements"></a><span data-ttu-id="88c68-414">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="88c68-414">Requirements</span></span>

<span data-ttu-id="88c68-415">**Ordinateur** DBAnalyze ne peut être exécuté qu’à partir d’un ordinateur appartenant à un domaine sur lequel Lync Server 2013 est installé.</span><span class="sxs-lookup"><span data-stu-id="88c68-415">**Computer** DBAnalyze can be run only from a domain-joined computer that has Lync Server 2013 installed.</span></span>

<span data-ttu-id="88c68-416">**Réseau** L’ordinateur doit pouvoir se connecter à la base de données principale.</span><span class="sxs-lookup"><span data-stu-id="88c68-416">**Network** The computer should be able to connect to the back-end database.</span></span>

<span data-ttu-id="88c68-417">Le **logiciel** ; Les composants logiciels de Lync Server 2013 doivent être installés avant d’exécuter DBAnalyze.</span><span class="sxs-lookup"><span data-stu-id="88c68-417">**Software** Lync Server 2013 software components must be installed before running DBAnalyze.</span></span>

<span data-ttu-id="88c68-418">**Utilisateurs** Le tableau ci-dessous indique les administrateurs disposant des autorisations nécessaires pour accéder aux bases de données Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="88c68-418">**Users** The table below shows the administrators who have the necessary permissions to access Lync Server 2013 databases.</span></span>

<span data-ttu-id="88c68-419">![Tableau des autorisations pour Dbanalyze.exe.](images/JJ945604.b8931e9e-834e-4dec-8a84-2fc47d1613e9(OCS.15).jpg "Tableau des autorisations pour Dbanalyze.exe.")</span><span class="sxs-lookup"><span data-stu-id="88c68-419">![Permissions table for Dbanalyze.exe.](images/JJ945604.b8931e9e-834e-4dec-8a84-2fc47d1613e9(OCS.15).jpg "Permissions table for Dbanalyze.exe.")</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="88c68-420">Un compte d’administrateur local est nécessaire pour le mode <STRONG>/report:disk</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="88c68-420">A local administrator account is required for <STRONG>/report:disk</STRONG> mode.</span></span>



</div>

</div>

<div>

## <a name="examples"></a><span data-ttu-id="88c68-421">Exemples</span><span class="sxs-lookup"><span data-stu-id="88c68-421">Examples</span></span>

<span data-ttu-id="88c68-422">Les exemples suivants constituent des commandes Dbanalyze.exe correctes :</span><span class="sxs-lookup"><span data-stu-id="88c68-422">The following are examples of valid Dbanalyze.exe commands:</span></span>

    dbanalyze.exe /report:diag
    dbanalyze.exe /report:user /user:usera@domainb.com
    dbanalyze.exe /report:conf /user:bob@example.com /conf:1W9J71SKSX2X
    dbanalyze.exe /report:resolve /pstnid:12345
    dbanalyze.exe /report:mcus
    dbanalyze.exe /report:disk

</div>

<div>

## <a name="summary"></a><span data-ttu-id="88c68-423">Résumé</span><span class="sxs-lookup"><span data-stu-id="88c68-423">Summary</span></span>

<span data-ttu-id="88c68-424">DBAnalyzer permet aux administrateurs d’analyser rapidement et facilement des bases de données Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="88c68-424">DBAnalyzer provides administrators a quick and easy to analyze Lync Server 2013 databases.</span></span>

</div>

</div>

<div>

## <a name="importstorageservicedata"></a><span data-ttu-id="88c68-425">ImportStorageServiceData</span><span class="sxs-lookup"><span data-stu-id="88c68-425">ImportStorageServiceData</span></span>

<span data-ttu-id="88c68-426">L’outil de kit de ressources ImportStorageServiceData permet de réimporter les données de file d’attente et de point de terminaison éliminées du service de stockage Lync Server dans le service de stockage.</span><span class="sxs-lookup"><span data-stu-id="88c68-426">The ImportStorageServiceData resource kit tool allows for re-importing Queue and Endpoint data that was flushed out of the Storage Service (LYSS) back into the Storage Service.</span></span>

<div>

## <a name="description"></a><span data-ttu-id="88c68-427">Description</span><span class="sxs-lookup"><span data-stu-id="88c68-427">Description</span></span>

<span data-ttu-id="88c68-428">L’élimination de données du service de stockage peut être automatique (périodique) selon le statut des éléments de file d’attente ou la taille de la base de données.</span><span class="sxs-lookup"><span data-stu-id="88c68-428">The data flushed out of the Storage Service could have been automatic (periodic) based on Queue Item status or database size.</span></span> <span data-ttu-id="88c68-429">Elle peut survenir suite à l’invocation manuelle de l’applet de commande de basculement du pool ou StorageServiceFullFlush (invoquée par l’applet de commande de basculement du pool).</span><span class="sxs-lookup"><span data-stu-id="88c68-429">It could have happened due to the manual invocation of the pool failover cmdlet, or the StorageServiceFullFlush cmdlet (which the pool failover cmdlet invokes).</span></span> <span data-ttu-id="88c68-430">Notez que les données ne peuvent pas être réimportées si la taille de la base de données du service de stockage (LYSS) au premier plan se trouve au-dessus du niveau normal, car cela risque de provoquer une exportation supplémentaire de données. De plus, tous les problèmes susceptibles d’avoir contribué à des erreurs qui entraînaient l’augmentation de la file d’attente du service de stockage doivent être résolus (par exemple, des erreurs de point de terminaison Exchange, des problèmes de réseau ou d’autres problèmes).</span><span class="sxs-lookup"><span data-stu-id="88c68-430">Note that data should ideally not be re-imported if any of the Storage Service (LYSS ) database size on the front ends is above the normal level, because doing so will likely just cause more data to be exported back out. Furthermore, any problems which could have contributed to errors that caused the Storage Service Queue to grow should first be resolved (for example Exchange endpoint errors, network issues, or other problems).</span></span>

<span data-ttu-id="88c68-431">**Scénario 1 :** lors du basculement du pool, les fichiers peuvent être éliminés du service de stockage de chaque serveur frontal.</span><span class="sxs-lookup"><span data-stu-id="88c68-431">**Scenario 1:** during pool failover, files may be flushed out from storage service for each front end.</span></span> <span data-ttu-id="88c68-432">Une fois le basculement terminé, l’outil doit être exécuté pour réimporter les données.</span><span class="sxs-lookup"><span data-stu-id="88c68-432">After failover is completed, the tool should be run to re-import the data.</span></span>

<span data-ttu-id="88c68-433">**Scénario 2 :** les données sont éliminées automatiquement chaque jour ou suite au dépassement de certains seuils de taille par la base de données du service de stockage (par exemple, 60 %, 80 %, 90 % de remplissage).</span><span class="sxs-lookup"><span data-stu-id="88c68-433">**Scenario 2:** data is being flushed automatically each day or in response to Storage Service database exceeding certain size thresholds ( for example 60%, 80%, 90% full ).</span></span> <span data-ttu-id="88c68-434">Ces données éliminées automatiquement doivent être régulièrement réimportées par l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="88c68-434">This automatically flushed data should be re-imported routinely by the administrator.</span></span> <span data-ttu-id="88c68-435">Dans le cas ci-dessus, si le Pack de contrôle SCOM n’est pas déployé, il existe des événements pour le service de stockage Lync Server relatif aux données vidées du service de stockage.</span><span class="sxs-lookup"><span data-stu-id="88c68-435">In the above situation, if the monitoring SCOM pack is not deployed, there are events for Lync Server Storage Service relating to data being flushed from the Storage Service.</span></span> <span data-ttu-id="88c68-436">Les ID d’événement 32075 (démarrage du vidage complet), 32076 (fin du vidage complet), 32082 (démarrage du vidage de niveau maintenance), 32083 (fin du vidage de niveau maintenance), 32089 (vidage effectué à cause du remplissage de la base de données).</span><span class="sxs-lookup"><span data-stu-id="88c68-436">Event IDs of 32075 (full flush operation is started), 32076 (full flush has completed), 32082 (maintenance level flush started), 32083 (maintenance level flush complete), 32089 (flush occurred due to filling up of database).</span></span> <span data-ttu-id="88c68-437">Notez que ces ID d’événement correspondent à la version finale.</span><span class="sxs-lookup"><span data-stu-id="88c68-437">Note these event Ids correspond to the RTM release.</span></span> <span data-ttu-id="88c68-438">Lorsqu’un administrateur voit ces événements, cela signifie qu’il y a des fichiers qui ont été vidés. Ces données doivent être importées régulièrement à l’aide de cet outil, par exemple une fois par semaine.</span><span class="sxs-lookup"><span data-stu-id="88c68-438">When an administrator sees these events, it means that there are files that have been flushed out. This data should routinely be imported back using this tool, for example once per week.</span></span>

<span data-ttu-id="88c68-439">Dans le cas d’un service en ligne, si le Pack de gestion de l’intégrité pour Lync Server est déployé, de nouvelles alertes peuvent être déclenchées qui demandent à l’administrateur de réimporter les données vidées dans le service de stockage.</span><span class="sxs-lookup"><span data-stu-id="88c68-439">For the Online Service release, if health monitoring SCOM pack for Lync Server is deployed, there are new alerts which may be raised which ask the administrator to re-import the flushed data back into Storage Service.</span></span> <span data-ttu-id="88c68-440">Il y aura un événement correspondant dans le journal des événements sur le serveur frontal qui déclenchait l’alerte.</span><span class="sxs-lookup"><span data-stu-id="88c68-440">There will be a corresponding event in the event log on the Front End server which triggered the alert.</span></span> <span data-ttu-id="88c68-441">L’événement fournit une description du chemin d’accès parent sous lequel se trouvent les fichiers de données vidées, ainsi que du nombre de fichiers qui répondent aux critères d’alerte.</span><span class="sxs-lookup"><span data-stu-id="88c68-441">The event will give a description of the Parent path under which the flushed data files are located, as well as how many files there are which meet the alert criteria.</span></span> <span data-ttu-id="88c68-442">Le critère d’alerte est que le chemin d’accès parent est inférieur ou égal à X jours (où X et Y sont prédéfinis dans le StorageService, mais peut être substitué en modifiant le fichier APPCONFIG.) Vous trouverez ci-dessous deux exemples d’événements qui peuvent déclencher l’alerte d’intégrité, en étant leur chemin parent.</span><span class="sxs-lookup"><span data-stu-id="88c68-442">The alert criteria is that there are X or more files under the particular parent path which are at least Y days old ( where X and Y are preset within the StorageService but can be overridden by changing the APPCONFIG file.)Two examples of events which can trigger the health alert are shown below, with the difference being their parent path.</span></span> <span data-ttu-id="88c68-443">Il existe une possibilité de partage de fichiers de service Web, tandis que l’autre est le répertoire de données d’application local de chaque frontal.</span><span class="sxs-lookup"><span data-stu-id="88c68-443">One possibility is under Web service file share, while the other possibility is the local Application Data directory of each front end.</span></span> <span data-ttu-id="88c68-444">(par exemple, c : \\ ProgramData \\ Microsoft \\ Lync Server \\ StorageService).</span><span class="sxs-lookup"><span data-stu-id="88c68-444">( for example c:\\ProgramData\\Microsoft\\Lync Server\\StorageService ).</span></span> <span data-ttu-id="88c68-445">L’administrateur doit alors exécuter cet outil reskit.</span><span class="sxs-lookup"><span data-stu-id="88c68-445">The administrator will then run this reskit tool.</span></span>

<span data-ttu-id="88c68-446">Cet outil augmente la charge processeur et d’E/S sur le serveur frontal sur lequel il est exécuté, ainsi que sur les autre serveurs frontaux, si les données n’appartiennent pas au serveur frontal sur lequel l’outil est exécuté.</span><span class="sxs-lookup"><span data-stu-id="88c68-446">This tool will increase CPU and IO load on the front end it is running on, as well as other front ends, in the situation that the data is not owned by the front end that the tool is executed on.</span></span> <span data-ttu-id="88c68-447">Il est recommandé d’exécuter cet outil lorsque les serveurs frontaux ne sont pas soumis à une charge processeur et d’E/S importante, par exemple en dehors des heures de pointe.</span><span class="sxs-lookup"><span data-stu-id="88c68-447">We recommend runng this tool when front ends are not under heavy CPU and IO load, for example outside of peak hours.</span></span> <span data-ttu-id="88c68-448">Deuxièmement, cet outil peut prendre 2 à 3 minutes pour importer un fichier de données.</span><span class="sxs-lookup"><span data-stu-id="88c68-448">Secondly, this tool can 2 to 3 minutes to import one data file.</span></span> <span data-ttu-id="88c68-449">Tenez compte de ce qui suit lors de l’estimation de la durée d’exécution de l’outil. Par défaut, le fichier journal détaillé généré par l’outil apparaît sur le magasin de fichiers.</span><span class="sxs-lookup"><span data-stu-id="88c68-449">Keep this in mind when estimating how long tool will be running.The verbose log file generated by the tool will by default appear on the File Store.</span></span> <span data-ttu-id="88c68-450">Supprimez-le si aucune erreur n’est signalée, car la taille de celui-ci peut atteindre plusieurs Mo, voire davantage.</span><span class="sxs-lookup"><span data-stu-id="88c68-450">Delete it if there are no errors reported, because the log file can be tens of MB or more.</span></span>

<span data-ttu-id="88c68-451">![Exemples de journaux d’événements du serveur de stockage.](images/JJ945604.3a903ef7-ea8a-4606-8229-a3e32f13af3a(OCS.15).jpg "Exemples de journaux d’événements du serveur de stockage.")</span><span class="sxs-lookup"><span data-stu-id="88c68-451">![Sample Storage Server event log events.](images/JJ945604.3a903ef7-ea8a-4606-8229-a3e32f13af3a(OCS.15).jpg "Sample Storage Server event log events.")</span></span>

</div>

<div>

## <a name="requirements"></a><span data-ttu-id="88c68-452">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="88c68-452">Requirements</span></span>

<span data-ttu-id="88c68-453">Installez les outils du kit de ressources de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="88c68-453">Install the Lync Server 2013, Resource Kit Tools.</span></span> <span data-ttu-id="88c68-454">L’outil s’exécute sur des ordinateurs liés à un domaine dans lesquels Lync Server et Lync Server Management Shell sont installés.</span><span class="sxs-lookup"><span data-stu-id="88c68-454">The tool runs on domain-joined machines where Lync Server and Lync Server Management Shell are installed.</span></span> <span data-ttu-id="88c68-455">L’outil utilise une cmdlet de Management Shell pour identifier tous les serveurs frontaux de la liste.</span><span class="sxs-lookup"><span data-stu-id="88c68-455">The tool uses a cmdlet from the management shell to identify all the Front End servers in the pool.</span></span> <span data-ttu-id="88c68-456">Deuxièmement, l’outil doit être exécuté à partir d’un ordinateur du pool sur lequel la base de données **RtcLocal** est installée.</span><span class="sxs-lookup"><span data-stu-id="88c68-456">Secondly, the tool must be executed from a machine in the pool which has the **RtcLocal** database installed.</span></span> <span data-ttu-id="88c68-457">Cette base de données est utilisée par l’outil pour récupérer l’emplacement du partage de fichiers WebService pour le pool. Par ailleurs, avant d’utiliser l’outil, chaque serveur frontal doit d’abord activer l’accès distant Windows PowerShell à l’aide de **Enable-PSRemoting** sur chaque serveur frontal, ainsi que de l’ordinateur à partir duquel l’outil est exécuté.</span><span class="sxs-lookup"><span data-stu-id="88c68-457">This database is used by the tool to retrieve the location of the WEBSERVICE file share for the pool.Additionally, before using the tool, each Front End server must first enable Windows PowerShell Remoting using **Enable-PSRemoting** on each Front End server, as well as the machine that the tool is executed from.</span></span> <span data-ttu-id="88c68-458">Dans le cas contraire, les commandes Windows PowerShell distantes de cet outil échoueront.</span><span class="sxs-lookup"><span data-stu-id="88c68-458">Otherwise, remote Windows PowerShell commands from this tool will fail.</span></span> <span data-ttu-id="88c68-459">La fonctionnalité d’accès distant de Windows PowerShell peut être désactivée sur tous les serveurs frontaux de la liste une fois l’opération terminée.</span><span class="sxs-lookup"><span data-stu-id="88c68-459">Windows PowerShell Remoting can be turned off on all Front End servers in the pool after it is finished.</span></span> <span data-ttu-id="88c68-460">Enfin, le compte ou les informations d’identification appelant l’outil doivent disposer d’autorisations en lecture/écriture sur le partage de fichiers WebPart pour le pool sur lequel ils exécutent cet outil.</span><span class="sxs-lookup"><span data-stu-id="88c68-460">Finally, the account or credential invoking the tool must have read/write permission to the webservice file share for the pool they are executing this tool on.</span></span> <span data-ttu-id="88c68-461">Dans le cas contraire, l’outil échoue avec des erreurs d’autorisation d’e/s.</span><span class="sxs-lookup"><span data-stu-id="88c68-461">Otherwise the tool will fail with IO Permission errors.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="88c68-462">Sur Windows Server 2012, la mise à niveau de Windows PowerShell est activée par défaut, mais pas sur le système d’exploitation Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="88c68-462">On Windows Server 2012, Windows PowerShell Remoting is enabled by default, but not on the Windows Server 2008 operating system.</span></span>



</div>

</div>

<div>

## <a name="examples"></a><span data-ttu-id="88c68-463">Exemples</span><span class="sxs-lookup"><span data-stu-id="88c68-463">Examples</span></span>

    >  C:\StorageService>ImportStorageServiceData.exe
    Description:
    This tool will re-import Storage Service (LYSS) flushed queue data back in.  For a pool: you are required to run this tool on a machine inside the pool which has the Lync Server Management Shell installed.  Additionally, all front end machines need to have Windows Powershell Remoting enabled before executing this tool by executing Enable-PSRemoting.  Also, please ensure that all Storage Service instance DB Size are at the 'Normal' level (verify this by viewing Eventlog events). Otherwise re-importing may cause data to be flushed out again if any Storage Service instance DB size level goes above 'Normal'.
    Usage: Default behavior is to Import data from web service file share as well as any files on all Front End machines in pool.
    Additional Options:
    -Verbose                    : Turn verbose output on.
    
    -StorageServiceHostName     : Host Name of Storage Service WCF endpoint.  ( Default=localhost netnamedpipe binding. )
                                        
    -FileSharePath              : Import only all data from just under the UNC path specified.
    
    ActivityID: cc3b62ff-bb66-4e61-a6e2-96cb3626315c. <-- Use this to correlate with StorageService trace logs if troubleshooting.
    Type Server name (TCP binding) or press <enter> for localhost (NamePipe binding):
    Using NetNamedPipeBinding...
    OnTopologyChanged Event received
    Web Service File Share: \\dc.vdomain.com\OcsFileStore\co1-WebServices-1\StorageService
    
    Front Ends:
    server.vdomain.com
    server2.vdomain.com
    server1.vdomain.com
    server3.vdomain.com
    Looking under directory: \\dc.vdomain.com\OcsFileStore\co1-WebServices-1\StorageService for exported data.
    # Files found: 8
    Starting Import for file:\\dc.vdomain.com\OcsFileStore\co1-WebServices-1\StorageService\DataExport\2
    0120910\SERVER.vdomain.com\944f5724c65c5f93900dc1c8c898b102__0.xml
    Items deserialized: 20
    
    All items in file were enqueued successfully, will try to delete file: \\dc.vdomain.com\OcsFileStore\co1-WebServices-1\StorageService\DataExport\20120910\SERVER.vdomain.com\944f5724c65c5f93900dc1c8c898b102__0.xml
    
    All items in file failed to enqueue so file will not be deleted.  File path: \\dc.vdomain.com\OcsFileStore\co1-WebServices-1\StorageService\DataExport\20120910\SERVER.vdomain.com\944f5724c65c5f93900dc1c8c898b102__0.xml
    
    Summary for file \\dc.vdomain.com\OcsFileStore\co1-WebServices-1\StorageService\DataExport\20120910\SERVER.vdomain.com\944f5724c65c5f93900dc1c8c898b102__0.xml: succeeded: 20, failed: 0
    
    Starting Import for file:\\dc.vdomain.com\OcsFileStore\co1-WebServices-1\StorageService\DataExport\20120910\SERVER1.vdomain.com\17d5435ae40259f7bbdf1866776386e4__0.xml
    Items deserialized: 20
    
    [cc3b62ff-bb66-4e61-a6e2-96cb3626315c] Send EnqueueMessages to redirected, targetServer=server1.vdomain.com, queueItems=20
    
    All items in file were enqueued successfully, will try to delete file: \\dc.vdomain.com\OcsFileStore\co1-WebServices-1\StorageService\DataExport\20120910\SERVER1.vdomain.com\17d5435ae40259f7bbdf1866776386e4__0.xml
    
    All items in file failed to enqueue so file will not be deleted.  File path: \\dc.vdomain.com\OcsFileStore\co1-WebServices-1\StorageService\DataExport\20120910\SERVER1.vdomain.com\17d5435ae40259f7bbdf1866776386e4__0.xml
    
    Summary for file \\dc.vdomain.com\OcsFileStore\co1-WebServices-1\StorageService\DataExport\20120910\
    SERVER1.vdomain.com\17d5435ae40259f7bbdf1866776386e4__0.xml: succeeded: 20, failed: 0
    
    Starting Import for file:\\dc.vdomain.com\OcsFileStore\co1-WebServices-1\StorageService\DataExport\20120910\SERVER1.vdomain.com\904f6c9b8ac951ae8b3c86684d3832e4__0.xml
    
    Items deserialized: 20
    [cc3b62ff-bb66-4e61-a6e2-96cb3626315c] Send EnqueueMessages to redirected, targetServer=server1.vdomain.com, queueItems=20
    
    All items in file were enqueued successfully, will try to delete file: \\dc.vdomain.com\OcsFileStore
    \co1-WebServices-1\StorageService\DataExport\20120910\SERVER1.vdomain.com\904f6c9b8ac951ae8b3c86684d
    3832e4__0.xml
    
    All items in file failed to enqueue so file will not be deleted.  File path: \\dc.vdomain.com\OcsFil
    eStore\co1-WebServices-1\StorageService\DataExport\20120910\SERVER1.vdomain.com\904f6c9b8ac951ae8b3c
    86684d3832e4__0.xml
    
    
    Summary for file \\dc.vdomain.com\OcsFileStore\co1-WebServices-1\StorageService\DataExport\20120910\
    SERVER1.vdomain.com\904f6c9b8ac951ae8b3c86684d3832e4__0.xml: succeeded: 20, failed: 0
    
    Starting Import for file:\\dc.vdomain.com\OcsFileStore\co1-WebServices-1\StorageService\DataExport\2
    0120910\SERVER2.vdomain.com\69844a271e6c5633a1f2b46a42287dd6__0.xml
    
    Items deserialized: 20
    
    [cc3b62ff-bb66-4e61-a6e2-96cb3626315c] Send EnqueueMessages to redirected, targetServer=server2.vdom
    ain.com, queueItems=20
    
    All items in file were enqueued successfully, will try to delete file: \\dc.vdomain.com\OcsFileStore
    \co1-WebServices-1\StorageService\DataExport\20120910\SERVER2.vdomain.com\69844a271e6c5633a1f2b46a42
    287dd6__0.xml
    
    All items in file failed to enqueue so file will not be deleted.  File path: \\dc.vdomain.com\OcsFil
    eStore\co1-WebServices-1\StorageService\DataExport\20120910\SERVER2.vdomain.com\69844a271e6c5633a1f2
    b46a42287dd6__0.xml
    
    Summary for file \\dc.vdomain.com\OcsFileStore\co1-WebServices-1\StorageService\DataExport\20120910\
    SERVER2.vdomain.com\69844a271e6c5633a1f2b46a42287dd6__0.xml: succeeded: 20, failed: 0
    
    Starting Import for file:\\dc.vdomain.com\OcsFileStore\co1-WebServices-1\StorageService\DataExport\2
    0120910\SERVER3.vdomain.com\3313935458e35b9b9759e08a15d251e6__0.xml
    
    Items deserialized: 20
    
    [cc3b62ff-bb66-4e61-a6e2-96cb3626315c] Send EnqueueMessages to redirected, targetServer=server3.vdom
    ain.com, queueItems=1
    
    All items in file were enqueued successfully, will try to delete file: \\dc.vdomain.com\OcsFileStore
    \co1-WebServices-1\StorageService\DataExport\20120910\SERVER3.vdomain.com\3313935458e35b9b9759e08a15
    d251e6__0.xml
    
    All items in file failed to enqueue so file will not be deleted.  File path: \\dc.vdomain.com\OcsFil
    eStore\co1-WebServices-1\StorageService\DataExport\20120910\SERVER3.vdomain.com\3313935458e35b9b9759
    e08a15d251e6__0.xml
    
    Summary for file \\dc.vdomain.com\OcsFileStore\co1-WebServices-1\StorageService\DataExport\20120910\
    SERVER3.vdomain.com\3313935458e35b9b9759e08a15d251e6__0.xml: succeeded: 20, failed: 0
    
    Starting Import for file:\\dc.vdomain.com\OcsFileStore\co1-WebServices-1\StorageService\DataExport\2
    0120910\SERVER3.vdomain.com\4501e04eae4856059346949ff817c220__0.xml
    Items deserialized: 20
    [cc3b62ff-bb66-4e61-a6e2-96cb3626315c] Send EnqueueMessages to redirected, targetServer=server3.vdom
    ain.com, queueItems=1
    All items in file were enqueued successfully, will try to delete file: \\dc.vdomain.com\OcsFileStore
    \co1-WebServices-1\StorageService\DataExport\20120910\SERVER3.vdomain.com\4501e04eae4856059346949ff8
    17c220__0.xml
    All items in file failed to enqueue so file will not be deleted.  File path: \\dc.vdomain.com\OcsFil
    eStore\co1-WebServices-1\StorageService\DataExport\20120910\SERVER3.vdomain.com\4501e04eae4856059346
    949ff817c220__0.xml
    
    Summary for file \\dc.vdomain.com\OcsFileStore\co1-WebServices-1\StorageService\DataExport\20120910\
    SERVER3.vdomain.com\4501e04eae4856059346949ff817c220__0.xml: succeeded: 20, failed: 0
    Starting Import for file:\\dc.vdomain.com\OcsFileStore\co1-WebServices-1\StorageService\DataExport\2
    0120910\SERVER3.vdomain.com\5ad77443ad955a22a876749be66d5317__0.xml
    
    Items deserialized: 20
    [cc3b62ff-bb66-4e61-a6e2-96cb3626315c] Send EnqueueMessages to redirected, targetServer=server3.vdom
    ain.com, queueItems=20
    All items in file were enqueued successfully, will try to delete file: \\dc.vdomain.com\OcsFileStore
    \co1-WebServices-1\StorageService\DataExport\20120910\SERVER3.vdomain.com\5ad77443ad955a22a876749be6
    6d5317__0.xml
    All items in file failed to enqueue so file will not be deleted.  File path: \\dc.vdomain.com\OcsFil
    eStore\co1-WebServices-1\StorageService\DataExport\20120910\SERVER3.vdomain.com\5ad77443ad955a22a876
    749be66d5317__0.xml
    Summary for file \\dc.vdomain.com\OcsFileStore\co1-WebServices-1\StorageService\DataExport\20120910\
    SERVER3.vdomain.com\5ad77443ad955a22a876749be66d5317__0.xml: succeeded: 20, failed: 0
    Starting Import for file:\\dc.vdomain.com\OcsFileStore\co1-WebServices-1\StorageService\DataExport\2
    0120910\SERVER3.vdomain.com\a11e27ae439a582288d4657eda86b565__0.xml
    Items deserialized: 20
    [cc3b62ff-bb66-4e61-a6e2-96cb3626315c] Send EnqueueMessages to redirected, targetServer=server3.vdom
    ain.com, queueItems=20
    All items in file were enqueued successfully, will try to delete file: \\dc.vdomain.com\OcsFileStore
    \co1-WebServices-1\StorageService\DataExport\20120910\SERVER3.vdomain.com\a11e27ae439a582288d4657eda
    86b565__0.xml
    All items in file failed to enqueue so file will not be deleted.  File path: \\dc.vdomain.com\OcsFil
    eStore\co1-WebServices-1\StorageService\DataExport\20120910\SERVER3.vdomain.com\a11e27ae439a582288d4
    657eda86b565__0.xml
    Summary for file \\dc.vdomain.com\OcsFileStore\co1-WebServices-1\StorageService\DataExport\20120910\
    SERVER3.vdomain.com\a11e27ae439a582288d4657eda86b565__0.xml: succeeded: 20, failed: 0
    All files have been imported into Storage Service for path: \\dc.vdomain.com\OcsFileStore\co1-WebSer
    vices-1\StorageService
    Importing files for: server.vdomain.com
    No files founds.
    Importing files for: server2.vdomain.com
    No files founds.
    Importing files for: server1.vdomain.com
    No files founds.
    Importing files for: server3.vdomain.com
    No files founds.
    Writing log: \\dc.vdomain.com\OcsFileStore\co1-WebServices-1\StorageService\ImportStorageServiceData
    Log20120910_1609SS
    Tool has finished execution.
    >  C:\StorageService>

</div>

</div>

<div>

## <a name="lcssync"></a><span data-ttu-id="88c68-464">LCSSync</span><span class="sxs-lookup"><span data-stu-id="88c68-464">LCSSync</span></span>

<span data-ttu-id="88c68-465">L’outil LCSSync facilite le déploiement du logiciel de communication Lync Server 2013 dans un environnement multiforêt.</span><span class="sxs-lookup"><span data-stu-id="88c68-465">The LCSSync tool helps to deploy Lync Server 2013 communications software in a multi-forest environment.</span></span> <span data-ttu-id="88c68-466">Cet outil permet de synchroniser des utilisateurs et des groupes à partir de forêts utilisateur différentes en tant qu’objet de contact services de domaine Active Directory (AD FS) à une forêt centrale sur laquelle Lync Server 2013 est installé.</span><span class="sxs-lookup"><span data-stu-id="88c68-466">This tool is used to synchronize users and groups from different user forests as an Active Directory Domain Services contact object to a central forest where Lync Server 2013 is installed.</span></span>

<div>

## <a name="description"></a><span data-ttu-id="88c68-467">Description</span><span class="sxs-lookup"><span data-stu-id="88c68-467">Description</span></span>

<span data-ttu-id="88c68-468">LCSSync utilise les objets de contact des services de domaine Active Directory synchronisés dans la forêt centrale pour permettre aux utilisateurs de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="88c68-468">LCSSync uses the synchronized Active Directory Domain Services contact objects in the central forest to enable users for Lync Server.</span></span> <span data-ttu-id="88c68-469">Pour fournir une connexion unique, le compte d’utilisateur principal doit être mappé à l’objet de contact services de domaine Active Directory (AD FS) dans la forêt centrale de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="88c68-469">To provide single sign-in, the primary user account must be mapped to the Active Directory Domain Services contact object in the central forest for Lync Server 2013.</span></span> <span data-ttu-id="88c68-470">Cet outil aide à effectuer l’opération de mappage.</span><span class="sxs-lookup"><span data-stu-id="88c68-470">This tool helps perform that mapping.</span></span> <span data-ttu-id="88c68-471">Il fournit des modèles pour la création des agents de gestion dans Microsoft Identity Integration Server.</span><span class="sxs-lookup"><span data-stu-id="88c68-471">This tool provides templates for creating Management Agents in the Microsoft Identity Integration Server.</span></span>

</div>

<div>

## <a name="summary"></a><span data-ttu-id="88c68-472">Résumé</span><span class="sxs-lookup"><span data-stu-id="88c68-472">Summary</span></span>

<span data-ttu-id="88c68-473">L’outil LCSSync facilite le déploiement de Lync Server dans un environnement multiforêt.</span><span class="sxs-lookup"><span data-stu-id="88c68-473">The LCSSync tool helps to deploy Lync Server in a multi-forest environment.</span></span>

</div>

</div>

<div>

## <a name="lookupuserconsole"></a><span data-ttu-id="88c68-474">LookupUserConsole</span><span class="sxs-lookup"><span data-stu-id="88c68-474">LookupUserConsole</span></span>

<span data-ttu-id="88c68-475">L’outil LookupUserConsole affiche des informations de routage internes de Lync Server concernant des utilisateurs spécifiques.</span><span class="sxs-lookup"><span data-stu-id="88c68-475">The LookupUserConsole tool displays internal Lync Server routing information about specific users.</span></span> <span data-ttu-id="88c68-476">Ces informations peuvent être utiles au personnel du support technique Microsoft dans le cadre du diagnostic des problèmes de déploiement et de routage.</span><span class="sxs-lookup"><span data-stu-id="88c68-476">This information may be useful to Microsoft support personal in diagnosing deployment and routing problems.</span></span>

<div>

## <a name="description"></a><span data-ttu-id="88c68-477">Description</span><span class="sxs-lookup"><span data-stu-id="88c68-477">Description</span></span>

<span data-ttu-id="88c68-478">L’exécution d' LookupUserConsole.exe entraîne l’ouverture d’une invite de commandes qui accepte les adresses SIP et tente d’afficher des informations de routage du serveur Lync internes associées.</span><span class="sxs-lookup"><span data-stu-id="88c68-478">Executing LookupUserConsole.exe will open a command prompt that accepts SIP addresses and attempts to display internal Lync Server routing information relating them.</span></span> <span data-ttu-id="88c68-479">Tapez **exit** pour quitter l’outil LookupUserConsole.</span><span class="sxs-lookup"><span data-stu-id="88c68-479">Type **exit** to quit the LookupUserConsole tool.</span></span>

</div>

<div>

## <a name="requirements"></a><span data-ttu-id="88c68-480">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="88c68-480">Requirements</span></span>

<span data-ttu-id="88c68-481">Installez les outils du kit de ressources de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="88c68-481">Install the Lync Server 2013, Resource Kit Tools.</span></span> <span data-ttu-id="88c68-482">L’outil s’exécute sur des ordinateurs liés à un domaine sur lesquels Lync Server est installé</span><span class="sxs-lookup"><span data-stu-id="88c68-482">The tool runs on domain-joined machines where Lync Server is installed</span></span>

</div>

<div>

## <a name="examples"></a><span data-ttu-id="88c68-483">Exemples</span><span class="sxs-lookup"><span data-stu-id="88c68-483">Examples</span></span>

<span data-ttu-id="88c68-484">C : \\ fichiers programme \\ Microsoft Lync Server 2013 \\ reskit \>LookupUserConsole.exe</span><span class="sxs-lookup"><span data-stu-id="88c68-484">C:\\Program Files\\Microsoft Lync Server 2013\\ResKit\>LookupUserConsole.exe</span></span>

    > sip:john.doe@vdomain.com
    
      Execution time (ms):                            171.094
      Exeuction result:                               Success
      SIP URI:                                        sip:john.doe@vdomain.com
      User info:
        SID:                                          S-1-5-21-2831376166-29632525...    Display name:                                     John Doe
        Grouping ID:                                  00000000-0000-0000-0000-...
        Line URI:                                     <null>
        Policy assignment:                            TenantId={00000000--0000-000....
        SIP enabled:                                  True
        UC enabled:                                   False
        Tenant ID:                                    00000000-0000-0000-0000-...  Cluster info:
        Active cluster:                               pool0.vdomain.com
        Backup registrar cluster:                     <null>
        Deployment location:                          <null>
        Home Front-End FQDN:                          SERVER.vdomain.com
        Primary Registrar cluster:                    pool0.vdomain.com
        Remote Director external SIP FQDN:            <null>
        Remote Director internal SIP FQDN:            <null>
        Remote Director Web FQDN:                     <null>
        Routing group ID:                             4501e04e-ae48-5605-9346...
        Service tag ID:                               1266953005
        User Front-End resolved:                      True
        User in local forest:                         True
        User in remote forest:                        False
        User in split domain:                         False
        User-Services cluster:                        pool0.vdomain.com
    
    > sip:nouser@vdomain.com
    
      Execution time (ms):                            948.7574
      Exeuction result:                               UserDoesNotExist
    
    > exit

</div>

</div>

<div>

## <a name="msturnping"></a><span data-ttu-id="88c68-485">MsTurnPing</span><span class="sxs-lookup"><span data-stu-id="88c68-485">MsTurnPing</span></span>

<span data-ttu-id="88c68-486">L’outil MSTurnPing permet à un administrateur de logiciels de communications Microsoft Lync Server 2013 de vérifier l’état des serveurs exécutant les services d’authentification par périphérique audio et vidéo, ainsi que les serveurs qui exécutent des services de stratégie de bande passante dans la topologie.</span><span class="sxs-lookup"><span data-stu-id="88c68-486">The MSTurnPing tool allows an administrator of Microsoft Lync Server 2013 communications software to check the status of the servers running the Audio/Video Edge and Audio/Video Authentication services as well as the servers that are running Bandwidth Policy Services in the topology.</span></span>

<div>

## <a name="description"></a><span data-ttu-id="88c68-487">Description</span><span class="sxs-lookup"><span data-stu-id="88c68-487">Description</span></span>

<span data-ttu-id="88c68-488">L’outil MSTurnPing permet à un administrateur de logiciels de communication de Lync Server 2013 de vérifier l’état des serveurs exécutant les services d’authentification par périphérique audio/vidéo et audio/vidéo, ainsi que les serveurs qui exécutent des services de stratégie de bande passante dans la topologie.</span><span class="sxs-lookup"><span data-stu-id="88c68-488">The MSTurnPing tool allows an administrator of Lync Server 2013 communications software to check the status of the servers running the Audio/Video Edge and Audio/Video Authentication services as well as the servers that are running Bandwidth Policy Services in the topology.</span></span>

<span data-ttu-id="88c68-489">L’outil permet d’effectuer les tests suivants :</span><span class="sxs-lookup"><span data-stu-id="88c68-489">The tool allows the administrator to perform the following tests:</span></span>

1.  <span data-ttu-id="88c68-490">Test des serveurs Edge A/V : l’outil effectue des tests sur tous les serveurs Edge A/V dans la topologie comme suit :</span><span class="sxs-lookup"><span data-stu-id="88c68-490">A/V Edge Server test: The tool performs tests against all A/V Edge Servers in the topology by doing the following:</span></span>
    
      - <span data-ttu-id="88c68-491">Vérifier que le service d’authentification audio/vidéo de Lync Server est démarré et peut fournir des informations d’identification appropriées.</span><span class="sxs-lookup"><span data-stu-id="88c68-491">Verifying that the Lync Server Audio/Video Authentication service is started and can issue proper credentials.</span></span>
    
      - <span data-ttu-id="88c68-492">Vérifier que le service Edge audio/vidéo de Lync Server est démarré et peut allouer correctement les ressources sur le bord externe.</span><span class="sxs-lookup"><span data-stu-id="88c68-492">Verifying that the Lync Server Audio/Video Edge service is started and can allocate the resources on the external edge successfully.</span></span>

2.  <span data-ttu-id="88c68-493">Test des services de stratégie de bande passante : l’outil effectue des tests sur tous les serveurs exécutant les services de stratégie de bande passante dans la topologie comme suit :</span><span class="sxs-lookup"><span data-stu-id="88c68-493">Bandwidth Policy Service test: The tool performs tests against all the servers that are running the Bandwidth Policy Services in the topology by doing the following:</span></span>
    
      - <span data-ttu-id="88c68-494">Vérifier que le service de stratégie de bande passante de Lync Server (authentification) est démarré et peut fournir des informations d’identification appropriées.</span><span class="sxs-lookup"><span data-stu-id="88c68-494">Verifying that the Lync Server Bandwidth Policy Service (Authentication) is started and can issue proper credentials.</span></span>
    
      - <span data-ttu-id="88c68-495">Vérifier que le service de stratégie de bande passante de Lync Server (cœur) est démarré et peut procéder à la vérification de la bande passante.</span><span class="sxs-lookup"><span data-stu-id="88c68-495">Verifying that the Lync Server Bandwidth Policy Service (Core) is started and can perform the bandwidth check successfully.</span></span>

<span data-ttu-id="88c68-496">Cet outil doit être exécuté à partir d’un ordinateur qui fait partie de la topologie et sur lequel le magasin local est installé. </span><span class="sxs-lookup"><span data-stu-id="88c68-496">This tool must be run from a computer that is part of the topology and has the local store installed.</span></span>

</div>

<div>

## <a name="output"></a><span data-ttu-id="88c68-497">Sortie</span><span class="sxs-lookup"><span data-stu-id="88c68-497">Output</span></span>

<span data-ttu-id="88c68-498">L’outil génère des résultats pour chacune des opérations.</span><span class="sxs-lookup"><span data-stu-id="88c68-498">The tool outputs the results of each of the operations.</span></span>

  - <span data-ttu-id="88c68-499">Pour le test **AudioVideoEdgeServer**, l’outil génère les résultats suivants :</span><span class="sxs-lookup"><span data-stu-id="88c68-499">If the **AudioVideoEdgeServer** test is performed, the tool outputs are the following:</span></span>
    
      - <span data-ttu-id="88c68-500">Les résultats des tests pour les ordinateurs qui fournissent le service d’authentification audio/vidéo de Lync Server dans la topologie ;</span><span class="sxs-lookup"><span data-stu-id="88c68-500">The test results of the computers that provide the Lync Server Audio/Video Authentication service in the topology</span></span>
    
      - <span data-ttu-id="88c68-501">Les résultats des tests pour les ordinateurs qui fournissent le service Edge audio/vidéo de Lync Server dans la topologie</span><span class="sxs-lookup"><span data-stu-id="88c68-501">The test results of the computers that provide the Lync Server Audio/Video Edge service in the topology</span></span>

  - <span data-ttu-id="88c68-502">Pour le test **BandwidthPolicyServer**, l’outil génère les résultats suivants :</span><span class="sxs-lookup"><span data-stu-id="88c68-502">If the **BandwidthPolicyServer** test is performed, the tool outputs are the following:</span></span>
    
      - <span data-ttu-id="88c68-503">Les résultats des tests pour les ordinateurs qui fournissent le service de stratégie de bande passante Lync Server (authentification) dans la topologie ;</span><span class="sxs-lookup"><span data-stu-id="88c68-503">The test results of the computers that provide the Lync Server Bandwidth Policy Service (Authentication) in the topology</span></span>
    
      - <span data-ttu-id="88c68-504">Les résultats des tests pour les ordinateurs qui fournissent le service de stratégie de bande passante Lync Server (cœur) dans la topologie ;</span><span class="sxs-lookup"><span data-stu-id="88c68-504">The test results of the computers that provide the Lync Server Bandwidth Policy Service (Core) in the topology</span></span>

</div>

<div>

## <a name="requirements"></a><span data-ttu-id="88c68-505">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="88c68-505">Requirements</span></span>

  - <span data-ttu-id="88c68-506">Cet outil doit être exécuté à partir d’un ordinateur de la topologie sur lequel le magasin local est installé.</span><span class="sxs-lookup"><span data-stu-id="88c68-506">This tool must be run from a computer that is in the topology and that has the local store.</span></span>

  - <span data-ttu-id="88c68-507">L’outil doit être exécuté par un administrateur ayant accès au magasin local.</span><span class="sxs-lookup"><span data-stu-id="88c68-507">The tool must be run as an administrator who has access to the local store.</span></span>

</div>

<div>

## <a name="examples"></a><span data-ttu-id="88c68-508">Exemples</span><span class="sxs-lookup"><span data-stu-id="88c68-508">Examples</span></span>

<span data-ttu-id="88c68-509">Voici un exemple de saisie pour l’outil.</span><span class="sxs-lookup"><span data-stu-id="88c68-509">The following is an example of the tool input.</span></span>

    MsTurnPing -ServerRole AudioVideoEdgeServer
    
    MsTurnPing -ServerRole BandwidthPolicyServer

</div>

<div>

## <a name="summary"></a><span data-ttu-id="88c68-510">Résumé</span><span class="sxs-lookup"><span data-stu-id="88c68-510">Summary</span></span>

<span data-ttu-id="88c68-511">Cet outil peut être utile pour les administrateurs de Lync Server 2013 qui souhaitent vérifier l’état des serveurs qui exécutent les services audio/vidéo et de stratégie de bande passante.</span><span class="sxs-lookup"><span data-stu-id="88c68-511">This tool can be a valuable resource to Lync Server 2013 administrators who want to check the status of the servers that are running audio/video and bandwidth policy services.</span></span>

</div>

</div>

<div>

## <a name="network-configuration-viewer"></a><span data-ttu-id="88c68-512">Network Configuration Viewer</span><span class="sxs-lookup"><span data-stu-id="88c68-512">Network Configuration Viewer</span></span>

<span data-ttu-id="88c68-513">La visionneuse de configurations réseau peut être utilisée par les administrateurs de logiciels de communications Microsoft Lync Server 2013 pour afficher la topologie de réseau de contrôle d’admission des appels pour une entreprise mise en service pour autoriser les sessions de communication en temps réel, comme les appels vocaux ou vidéo selon la capacité de bande passante spécifiée.</span><span class="sxs-lookup"><span data-stu-id="88c68-513">Network Configuration Viewer can be used by Microsoft Lync Server 2013 communications software administrators to view call admission control (CAC) network topology for an enterprise that is provisioned to allow real-time communication sessions, such as voice or video calls based on specified bandwidth capacity.</span></span> <span data-ttu-id="88c68-514">Les administrateurs de Lync Server 2013 définissent des stratégies CAC qui sont appliquées par les services de stratégie de bande passante installés avec Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="88c68-514">Lync Server 2013 administrators define CAC policies, which are enforced by the Bandwidth Policy services that are installed with Lync Server 2013.</span></span>

<div>

## <a name="description"></a><span data-ttu-id="88c68-515">Description</span><span class="sxs-lookup"><span data-stu-id="88c68-515">Description</span></span>

<span data-ttu-id="88c68-516">Network Configuration Viewer (NetworkConfigurationViewer.exe) permet aux administrateurs d’effectuer les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="88c68-516">Network Configuration Viewer (NetworkConfigurationViewer.exe) allows administrators to perform the following tasks:</span></span>

  - <span data-ttu-id="88c68-517">Chargez et affichez la topologie de réseau CAC à partir d’un déploiement 2013 Lync Server dans un format graphique.</span><span class="sxs-lookup"><span data-stu-id="88c68-517">Load and view CAC network topology from a Lync Server 2013 deployment in a graphical format.</span></span>

  - <span data-ttu-id="88c68-518">charger et afficher la topologie réseau de contrôle d’admission des appels à partir d‘un fichier journal de serveur de stratégie de bande passante dans un format graphique ;</span><span class="sxs-lookup"><span data-stu-id="88c68-518">Load and view CAC network topology from a Bandwidth Policy Server log file in a graphical format.</span></span>

  - <span data-ttu-id="88c68-519">enregistrer et stocker la topologie réseau de contrôle d’admission des appels dans un format XML sur le disque ;</span><span class="sxs-lookup"><span data-stu-id="88c68-519">Save and store CAC network topology in an XML format on the disk.</span></span>

  - <span data-ttu-id="88c68-520">enregistrer et stocker le diagramme de la topologie réseau de contrôle d’admission des appels au format JPG ou BMP ;</span><span class="sxs-lookup"><span data-stu-id="88c68-520">Save and store CAC network topology diagram in JPG or BMP format.</span></span>

  - <span data-ttu-id="88c68-521">afficher les données de configuration de la topologie réseau de contrôle d’admission des appels ;</span><span class="sxs-lookup"><span data-stu-id="88c68-521">View CAC network topology configuration data.</span></span>

  - <span data-ttu-id="88c68-522">afficher la topologie réseau de contrôle d’admission des appels dans une arborescence ;</span><span class="sxs-lookup"><span data-stu-id="88c68-522">View CAC network topology in a tree-view style.</span></span>

  - <span data-ttu-id="88c68-523">définir des connecteurs personnalisés pour les liaisons de la topologie réseau de contrôle d’admission des appels (par exemple, liaisons site-région, région-région et site-site) ;</span><span class="sxs-lookup"><span data-stu-id="88c68-523">Define custom connectors for CAC network topology links (for example, site-to-region, region-to-region, and site-to-site links).</span></span>

  - <span data-ttu-id="88c68-524">afficher les informations de site, informations de région, stratégies de bande passante et liaisons réseau approvisionnées de la topologie réseau de contrôle d’admission des appels.</span><span class="sxs-lookup"><span data-stu-id="88c68-524">View CAC network topology site information, region Information, and provisioned bandwidth policies and network links.</span></span>

</div>

<div>

## <a name="purpose"></a><span data-ttu-id="88c68-525">Objectif</span><span class="sxs-lookup"><span data-stu-id="88c68-525">Purpose</span></span>

<span data-ttu-id="88c68-526">Afficher les liaisons de la topologie réseau de contrôle d’admission des appels dans une interface graphique.</span><span class="sxs-lookup"><span data-stu-id="88c68-526">View enterprise CAC network topology links in a graphical interface.</span></span>

</div>

<div>

## <a name="examples"></a><span data-ttu-id="88c68-527">Exemples</span><span class="sxs-lookup"><span data-stu-id="88c68-527">Examples</span></span>

<span data-ttu-id="88c68-528">**Chargez et affichez la topologie de réseau CAC à partir d’un déploiement 2013 Lync Server dans un format graphique :** Les administrateurs de Lync Server 2013 peuvent charger et afficher la configuration topologique du réseau CAC sur n’importe quel ordinateur Lync Server 2013 à l’aide de l’option **Télécharger la configuration réseau** , comme illustré dans la figure ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="88c68-528">**Load and view CAC network topology from a Lync Server 2013 deployment in a graphical format:** Lync Server 2013 administrators can load and view CAC network topology configuration on any Lync Server 2013 computer by using the **Download Network Configuration** option as shown in the figure below.</span></span> <span data-ttu-id="88c68-529">L’outil ne parvient pas à télécharger ou à afficher une telle configuration lors de son déploiement sur un ordinateur qui n’est pas connecté au magasin de configuration Lync.</span><span class="sxs-lookup"><span data-stu-id="88c68-529">The tool will fail to download or view such a configuration when deployed on a computer that does not have connectivity to the Lync configuration store.</span></span>

<span data-ttu-id="88c68-530">![Téléchargement de la configuration réseau.](images/JJ945604.8d126d3f-2545-4f13-a244-974f09614982(OCS.15).jpg "Téléchargement de la configuration réseau.")</span><span class="sxs-lookup"><span data-stu-id="88c68-530">![Downloading the network configuration.](images/JJ945604.8d126d3f-2545-4f13-a244-974f09614982(OCS.15).jpg "Downloading the network configuration.")</span></span>

<span data-ttu-id="88c68-531">**Chargez et affichez la topologie de réseau CAC à partir d’un fichier journal du serveur de stratégie de bande passante dans un format graphique :** Les serveurs de stratégie de bande passante Lync Server 2013 enregistrent la topologie du réseau CAC dans le cadre du mécanisme de journalisation dans l’emplacement du partage de fichiers 2013 Server.</span><span class="sxs-lookup"><span data-stu-id="88c68-531">**Load and View CAC network topology from a Bandwidth Policy server log file in a graphical format:** Lync Server 2013 Bandwidth Policy servers save the CAC network topology as a part of the logging mechanism under the Lync Server 2013 file share location.</span></span> <span data-ttu-id="88c68-532">Les administrateurs de Lync Server peuvent afficher ce type de fichier dans un format graphique à l’aide de l’option **ouvrir la configuration réseau** , comme illustré ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="88c68-532">Lync Server administrators can view such a file in a graphical format by using the **Open Network Configuration** option as shown below.</span></span>

<span data-ttu-id="88c68-533">![Ouverture d’un fichier journal du serveur de stratégie de bande passante.](images/JJ945604.3e503e92-aacb-4921-a8d2-23f860fe2df6(OCS.15).jpg "Ouverture d’un fichier journal du serveur de stratégie de bande passante.")</span><span class="sxs-lookup"><span data-stu-id="88c68-533">![Opening a Bandwidth Policy Server log file.](images/JJ945604.3e503e92-aacb-4921-a8d2-23f860fe2df6(OCS.15).jpg "Opening a Bandwidth Policy Server log file.")</span></span>

<span data-ttu-id="88c68-534">Enregistrer et stocker la topologie de réseau CAC au format XML sur le disque : les administrateurs de Lync Server 2013 peuvent enregistrer le fichier de configuration de topologie de réseau CAC au format XML en utilisant l’option **enregistrer une copie de la configuration réseau** , comme illustré ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="88c68-534">Save and store CAC network topology in an XML format on the disk: Lync Server 2013 administrators can save the CAC network topology configuration file in an XML format by using the **Save a copy of Network Configuration** option as shown below.</span></span> <span data-ttu-id="88c68-535">Le fichier de configuration enregistré peut ensuite être utilisé en mode hors connexion à des fins d’affichage graphique.</span><span class="sxs-lookup"><span data-stu-id="88c68-535">The saved configuration file can then be used offline for graphical viewing purposes.</span></span>

<span data-ttu-id="88c68-536">![Enregistrez la configuration réseau sous forme de fichier XML.](images/JJ945604.6eeef3b0-78b5-4ee6-8d94-1a4ddf3d8676(OCS.15).jpg "Enregistrez la configuration réseau sous forme de fichier XML.")</span><span class="sxs-lookup"><span data-stu-id="88c68-536">![Saving the network configuration as an XML file.](images/JJ945604.6eeef3b0-78b5-4ee6-8d94-1a4ddf3d8676(OCS.15).jpg "Saving the network configuration as an XML file.")</span></span>

<span data-ttu-id="88c68-537">Enregistrez et stockez le diagramme de topologie du réseau CAC au format JPG ou BMP : les administrateurs de Lync Server 2013 peuvent enregistrer la configuration de topologie de réseau CAC dans des formats de fichiers JPG et BMP en utilisant l’option **enregistrer le diagramme de configuration réseau en tant qu’image** , comme illustré ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="88c68-537">Save and Store CAC network topology diagram in JPG or BMP format: Lync Server 2013 administrators can save the CAC network topology configuration in a graphical format (JPG and BMP file formats) by using the **Save Network Configuration diagram as picture** option as shown below.</span></span>

<span data-ttu-id="88c68-538">![Enregistrez la configuration réseau en tant qu’image.](images/JJ945604.145a6fb9-58b1-46b1-bbd5-a661ceba07b4(OCS.15).jpg "Enregistrez la configuration réseau en tant qu’image.")</span><span class="sxs-lookup"><span data-stu-id="88c68-538">![Saving the network configuration as a picture.](images/JJ945604.145a6fb9-58b1-46b1-bbd5-a661ceba07b4(OCS.15).jpg "Saving the network configuration as a picture.")</span></span>

<span data-ttu-id="88c68-539">**Afficher les données de configuration de la topologie du réseau CAC :** Les administrateurs de Lync Server 2013 peuvent afficher les données de configuration du réseau associées, telles que les régions réseau, les sites réseau, les profils de bande passante et les adresses IP de sous-réseau du site, en utilisant l’option Afficher les données de configuration du réseau, comme illustré ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="88c68-539">**View CAC network topology configuration data:** Lync Server 2013 administrators can view related network configuration data such as network regions, network sites, bandwidth profiles, and site subnet IP addresses in a textual format by using the View Network Configuration data option as shown below.</span></span>

<span data-ttu-id="88c68-540">![Affichage des données de configuration du réseau.](images/JJ945604.b72a4c21-a042-4d91-bf96-fcb396af0679(OCS.15).jpg "Affichage des données de configuration du réseau.")</span><span class="sxs-lookup"><span data-stu-id="88c68-540">![Viewing network configuration data.](images/JJ945604.b72a4c21-a042-4d91-bf96-fcb396af0679(OCS.15).jpg "Viewing network configuration data.")</span></span>

<span data-ttu-id="88c68-541">**Voir la topologie du réseau CAC dans un style d’arborescence :** Les administrateurs de Lync Server 2013 peuvent afficher les données de configuration du réseau associées dans un style d’affichage d’arborescence graphique à l’aide du panneau de configuration sur le côté gauche de la fenêtre d’outils, comme illustré ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="88c68-541">**View CAC network topology in a tree-view style:** Lync Server 2013 administrators can view related network configuration data in a graphical tree view style by using the control panel on the left side of the tool window as shown below.</span></span>

<span data-ttu-id="88c68-542">![Afficher les données de configuration du réseau dans une arborescence.](images/JJ945604.4d924ac9-fd96-430f-b211-ee35b7ef9a23(OCS.15).jpg "Afficher les données de configuration du réseau dans une arborescence.")</span><span class="sxs-lookup"><span data-stu-id="88c68-542">![Viewing network configuration data in a tree-view.](images/JJ945604.4d924ac9-fd96-430f-b211-ee35b7ef9a23(OCS.15).jpg "Viewing network configuration data in a tree-view.")</span></span>

<span data-ttu-id="88c68-543">**Définissez des connecteurs personnalisés pour les liens de topologie de réseau CAC (par exemple, les liens de site à zone, de région à zone et de site à site) :** Les administrateurs de Lync Server 2013 peuvent définir des connecteurs graphiques personnalisés pour les liaisons réseau WAN de configuration réseau CAC en utilisant l’option paramètres, comme illustré ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="88c68-543">**Define custom connectors for CAC network topology links (such as site-to-region, region-to-region, and site-to-site links):** Lync Server 2013 administrators can define custom graphical connectors for CAC network configuration WAN links by using the Settings option as shown below.</span></span> <span data-ttu-id="88c68-544">Ceci permet de différencier divers types de liaisons réseau approvisionnées dans la configuration du réseau.</span><span class="sxs-lookup"><span data-stu-id="88c68-544">This helps differentiate between various types of network links that are provisioned in the network configuration.</span></span>

<span data-ttu-id="88c68-545">![Définir des connecteurs personnalisés pour la topologie de réseau CAC](images/JJ945604.b20bea67-c8e1-453e-b1dd-e2aa17b62566(OCS.15).jpg "Définir des connecteurs personnalisés pour la topologie de réseau CAC")</span><span class="sxs-lookup"><span data-stu-id="88c68-545">![Define custom connectors for CAC network topology](images/JJ945604.b20bea67-c8e1-453e-b1dd-e2aa17b62566(OCS.15).jpg "Define custom connectors for CAC network topology")</span></span>

<span data-ttu-id="88c68-546">**Affichez les informations de site et les stratégies de bande passante approvisionnées du réseau CAC.** Les administrateurs de Lync Server 2013 peuvent afficher les informations relatives à la région du réseau CAC, les informations du site et les informations de configuration de la bande passante CAC en utilisant les options ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="88c68-546">**View CAC network topology site information, region information, and provisioned bandwidth policies:** Lync Server 2013 administrators can view related CAC network region information, site information, and CAC bandwidth provisioning information by using options shown below.</span></span> <span data-ttu-id="88c68-547">(Par exemple, cliquez sur **informations** dans une région réseau ou un objet de site réseau.)</span><span class="sxs-lookup"><span data-stu-id="88c68-547">(For example, click **Info** in a network region or network site object.)</span></span>

<span data-ttu-id="88c68-548">![Définition de connecteurs personnalisés pour votre réseau.](images/JJ945604.26262c75-4342-41c3-bc98-1793aa6a7713(OCS.15).jpg "Définition de connecteurs personnalisés pour votre réseau.")</span><span class="sxs-lookup"><span data-stu-id="88c68-548">![Defining custom connectors for your network.](images/JJ945604.26262c75-4342-41c3-bc98-1793aa6a7713(OCS.15).jpg "Defining custom connectors for your network.")</span></span>

</div>

<div>

## <a name="summary"></a><span data-ttu-id="88c68-549">Résumé</span><span class="sxs-lookup"><span data-stu-id="88c68-549">Summary</span></span>

<span data-ttu-id="88c68-550">Cet outil peut être utile pour les administrateurs de Lync Server 2013 qui aimeraient voir la topologie de réseau CAC pour leur déploiement sous forme graphique.</span><span class="sxs-lookup"><span data-stu-id="88c68-550">This tool can be a valuable resource to Lync Server 2013 administrators who would like to view CAC network topology for their deployment in a graphical format.</span></span>

</div>

</div>

<div>

## <a name="response-group-agent-live"></a><span data-ttu-id="88c68-551">Response Group Agent Live</span><span class="sxs-lookup"><span data-stu-id="88c68-551">Response Group Agent Live</span></span>

<span data-ttu-id="88c68-552">L’application Response Group permet aux agents d’accéder à des informations utiles en temps réel via son service web intégré.</span><span class="sxs-lookup"><span data-stu-id="88c68-552">The Response Group application gives agents the ability to access useful real-time information using its built-in Web service.</span></span> <span data-ttu-id="88c68-553">Aucun affichage graphique de ces données n’est toutefois disponible en dehors de l’application.</span><span class="sxs-lookup"><span data-stu-id="88c68-553">Unfortunately, no graphical view of this data is available outside the application.</span></span> <span data-ttu-id="88c68-554">Pour résoudre ce problème, l’outil Response Group agent pour le kit de ressources techniques permet d’accéder à ces informations de manière simple et graphique, ainsi que des informations sur le logiciel de communications Microsoft Lync 2013 en temps réel, comme la présence d’autres agents.</span><span class="sxs-lookup"><span data-stu-id="88c68-554">The Response Group Agent Live Resource Kit tool solves this issue by providing a simple and graphical way to access this information, enhanced with real-time Microsoft Lync 2013 communications software information such as the presence of other agents.</span></span>

<div>

## <a name="description"></a><span data-ttu-id="88c68-555">Description</span><span class="sxs-lookup"><span data-stu-id="88c68-555">Description</span></span>

<span data-ttu-id="88c68-556">L’application Windows Response Group Agent Live fournit des fonctionnalités de connexion et de déconnexion et donne des informations en temps réel (appartenance aux groupes, nombre actuel d’appels, etc.) aux agents Response Group.</span><span class="sxs-lookup"><span data-stu-id="88c68-556">Response Group Agent Live is a Windows application that provides sign-in and sign-out functionality and some real-time information (such as group membership and current number of calls) to Response Group agents.</span></span> <span data-ttu-id="88c68-557">Il s’agit d’une version améliorée de la page groupes d’agents (accessible à partir de Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="88c68-557">It is meant to be an enhanced version of the Agent Groups page (accessible from Lync 2013.</span></span>

</div>

<div>

## <a name="purpose"></a><span data-ttu-id="88c68-558">Objectif</span><span class="sxs-lookup"><span data-stu-id="88c68-558">Purpose</span></span>

<span data-ttu-id="88c68-p165">L’application Response Group place les appels entrants en file d’attente avant de les acheminer vers des groupes d’agents. Pour identifier les appels à traiter de façon appropriée, les agents peuvent accéder à des informations en temps réel sur leurs groupes d’agents (agents disponibles, nombre d’appels en attente dans chaque file d’attente, etc.). Ces informations, à l’origine accessibles via le service Response Group uniquement, sont mises à disposition de façon intuitive par Response Group Agent Live.</span><span class="sxs-lookup"><span data-stu-id="88c68-p165">The Response Group application queues incoming calls, and then routes them to agent groups. To make informed decisions about which calls to service, agents can access real-time information about their agent groups, such as what other agents are available and how many calls are waiting in each queue. This information, initially accessible only through the Response Group service, is made available in an intuitive way by Response Group Agent Live.</span></span>

<div>

## <a name="features"></a><span data-ttu-id="88c68-562">Fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="88c68-562">Features</span></span>

<span data-ttu-id="88c68-563">L’outil Live Response agent agent est intégré au service Response Group et au kit de développement logiciel (SDK) Microsoft Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="88c68-563">The Response Group Agent Live tool is built on the Response Group service and the Microsoft Lync 2013 SDK.</span></span> <span data-ttu-id="88c68-564">Il fournit aux agents Response Group les informations et fonctionnalités disponibles via le service Response Group (appartenance à des groupes, présence des autres agents, nombre d’appels en attente, etc.).</span><span class="sxs-lookup"><span data-stu-id="88c68-564">It provides Response Group agents the information and capabilities that are available from the Response Group service (such as group membership, presence of other agents, and number of waiting calls).</span></span>

<span data-ttu-id="88c68-565">La figure suivante illustre l’interface principale de Response Group Agent Live.</span><span class="sxs-lookup"><span data-stu-id="88c68-565">The figure below illustrates the main interface of Response Group Agent Live.</span></span>

<span data-ttu-id="88c68-566">![Outil en ligne de l’agent Response Group.](images/JJ945604.63cb0374-a6ef-4a59-b60e-bec86a880d09(OCS.15).jpg "Outil en ligne de l’agent Response Group.")</span><span class="sxs-lookup"><span data-stu-id="88c68-566">![The Response Group Agent Live tool.](images/JJ945604.63cb0374-a6ef-4a59-b60e-bec86a880d09(OCS.15).jpg "The Response Group Agent Live tool.")</span></span>

<span data-ttu-id="88c68-567">Les trois fonctionnalités principales suivantes sont accessibles aux agents dans Response Group Agent Live :</span><span class="sxs-lookup"><span data-stu-id="88c68-567">The following three main features are available for agents in Response Group Agent Live:</span></span>

  - <span data-ttu-id="88c68-568">**Se connecter/** déconnecter : Contrairement à la page groupes d’agents (accessible à partir de Lync 2013), l’agent Response Group n’autorise que les agents à se connecter ou se déconnecter de tous les groupes d’agents en même temps.</span><span class="sxs-lookup"><span data-stu-id="88c68-568">**Sign-in/out:** Contrary to the Agent Groups page (accessible from Lync 2013), Response Group Agent Live allows only agents to sign-in or out of all agent groups at once.</span></span> <span data-ttu-id="88c68-569">Cette application propose trois méthodes rapides pour la connexion ou la déconnexion des agents :</span><span class="sxs-lookup"><span data-stu-id="88c68-569">This application provides three quick ways for agents to sign in or out:</span></span>
    
      - <span data-ttu-id="88c68-570">Cliquer sur les boutons Sign-in/out (Connexion/Déconnexion) (vert et rouge) dans l’application.</span><span class="sxs-lookup"><span data-stu-id="88c68-570">Click the Sign-in/out (green and red) buttons within the application.</span></span>
    
      - <span data-ttu-id="88c68-571">Cliquer avec le bouton droit sur la barre d’état système, et sélectionner Sign in (Connexion) ou Sign out (Déconnexion).</span><span class="sxs-lookup"><span data-stu-id="88c68-571">Right-click the system tray icon, and select sign in or sign out.</span></span>
    
      - <span data-ttu-id="88c68-572">Utiliser des raccourcis clavier configurables.</span><span class="sxs-lookup"><span data-stu-id="88c68-572">Using configurable keyboard shortcuts.</span></span>

  - <span data-ttu-id="88c68-573">**Appartenance à un groupe :** Lorsqu’un groupe d’agent est sélectionné, l’option agent de Response Group affiche la liste des agents de ce groupe dans le volet droit.</span><span class="sxs-lookup"><span data-stu-id="88c68-573">**Group membership:** When an agent group is selected, Response Group Agent Live displays the list of agents in this group in the right pane.</span></span> <span data-ttu-id="88c68-574">Si Lync 2013 est en cours d’exécution sur le même ordinateur que cette application, les informations de présence et la carte de visite s’affichent dans l’agent Response Group en direct.</span><span class="sxs-lookup"><span data-stu-id="88c68-574">If Lync 2013 is running on the same computer as this application, presence information and the contact card are displayed in the Response Group Agent Live.</span></span> <span data-ttu-id="88c68-575">Les agents peuvent envoyer un message instantané ou appeler d’autres agents directement depuis là.</span><span class="sxs-lookup"><span data-stu-id="88c68-575">Agents can send an IM or call other agents directly from there.</span></span>

  - <span data-ttu-id="88c68-p169">**Statistiques en temps réel :** Response Group Agent Live fournit des statistiques en temps réel pour tous les groupes d’agents. La fréquence de mise à jour est d’une minute. Lorsqu’un Response Group répond à un appel, un indicateur visuel est ajouté près du nom du groupe et le nombre actuel d’appels placés en file d’attente est indiqué. Pour afficher le délai d’attente le plus long, il suffit de placer le pointeur de la souris sur un groupe.</span><span class="sxs-lookup"><span data-stu-id="88c68-p169">**Real-time statistics:** Response Group Agent Live provides real-time statistics for all agent groups. The update frequency is one minute. When a call is answered by a Response Group, a visual indicator is added next to the group name with the current number of queued calls. Pausing the pointer over a group also displays the longest waiting time.</span></span>

</div>

</div>

<div>

## <a name="requirements"></a><span data-ttu-id="88c68-580">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="88c68-580">Requirements</span></span>

<span data-ttu-id="88c68-581">Response Group Agent Live nécessite .NET Framework 4.0.</span><span class="sxs-lookup"><span data-stu-id="88c68-581">Response Group Agent Live requires the .NET Framework 4.0.</span></span> <span data-ttu-id="88c68-582">Par ailleurs, pour tirer parti des fonctionnalités de présence et de carte de visite, Lync 2013 doit être installé en local (et être en cours d’exécution).</span><span class="sxs-lookup"><span data-stu-id="88c68-582">In addition, to take advantage of the presence and contact card features, Lync 2013 must be installed locally (and be running).</span></span>

<div>

## <a name="configuration"></a><span data-ttu-id="88c68-583">Configuration</span><span class="sxs-lookup"><span data-stu-id="88c68-583">Configuration</span></span>

<span data-ttu-id="88c68-p171">Response Group Agent Live peut être personnalisé selon les préférences individuelles via la boîte de dialogue Options de l’application. L’administrateur peut également définir l’adresse de l’hôte par défaut en modifiant directement la propriété defaultHostAddress du fichier RGAgentLive.exe.config.</span><span class="sxs-lookup"><span data-stu-id="88c68-p171">Response Group Agent Live can be customized to individual preferences by using the Options dialog box in the application. In addition, the administrator can define the default host address by editing directly the defaultHostAddress property of the RGAgentLive.exe.config file.</span></span>

<span data-ttu-id="88c68-p172">La figure suivante illustre la boîte de dialogue Options qui permet aux agents de configurer l’adresse de l’hôte et les raccourcis clavier. Pour accéder à cette boîte de dialogue, il suffit de cliquer sur le bouton Options dans la partie supérieure droite de l’interface principale.</span><span class="sxs-lookup"><span data-stu-id="88c68-p172">The figure below illustrates the Options dialog box that agents can use to configure the host address and shortcut keys. This dialog is accessed by clicking the Options button on the top right of the main interface.</span></span>

<span data-ttu-id="88c68-588">![Boîte de dialogue Options d’agent de Response Group.](images/JJ945604.3cc15e29-8699-45ab-90c3-e1565fa6ebf6(OCS.15).jpg "Boîte de dialogue Options d’agent de Response Group.")</span><span class="sxs-lookup"><span data-stu-id="88c68-588">![The Response Group Agent Live Options dialog box.](images/JJ945604.3cc15e29-8699-45ab-90c3-e1565fa6ebf6(OCS.15).jpg "The Response Group Agent Live Options dialog box.")</span></span>

<span data-ttu-id="88c68-589">Les trois paramètres suivants peuvent être personnalisés dans la configuration de Response Group Agent Live :</span><span class="sxs-lookup"><span data-stu-id="88c68-589">The following three different settings can be customized in the Response Group Agent Live configuration:</span></span>

  - <span data-ttu-id="88c68-p173">Host address (Adresse de l’hôte) : il s’agit généralement du nom de domaine complet du pool web appartenant au pool d’accueil de l’agent. L’adresse exacte du service Response Group est dérivée automatiquement en arrière-plan à partir de ces informations (en ajoutant le chemin d’accès correct après l’hôte).</span><span class="sxs-lookup"><span data-stu-id="88c68-p173">Host address: This is typically the web pool FQDN belonging to the agent’s home pool. The exact Response Group service address is automatically derived in the background from this information (by appending the right path after the host).</span></span>

  - <span data-ttu-id="88c68-p174">Shortcuts (Raccourcis) : les raccourcis exacts pour la connexion/déconnexion peuvent être personnalisés. La seule limitation impose aux raccourcis d’inclure la touche du logo Windows (en plus d’une ou plusieurs autres touches).</span><span class="sxs-lookup"><span data-stu-id="88c68-p174">Shortcuts: The exact shortcuts to sign-in/out can be customized. The only limitation is that both shortcuts must contain the “Windows Logo” key (in addition to at least another key).</span></span>

  - <span data-ttu-id="88c68-594">Start with Windows (Démarrer avec Windows) : l’application peut être configurée pour démarrer automatiquement avec Windows.</span><span class="sxs-lookup"><span data-stu-id="88c68-594">Start with Windows: The application can be configured to start automatically with Windows.</span></span>

</div>

</div>

<div>

## <a name="examples"></a><span data-ttu-id="88c68-595">Exemples</span><span class="sxs-lookup"><span data-stu-id="88c68-595">Examples</span></span>

<span data-ttu-id="88c68-596">La figure suivante illustre l’appel d’un autre agent ou l’envoi d’un message instantané à un autre agent en cliquant avec le bouton droit sur le contact dans le volet droit.</span><span class="sxs-lookup"><span data-stu-id="88c68-596">The figure below illustrates how to call or send an IM to another agent by right-clicking the contact in the right pane.</span></span>

<span data-ttu-id="88c68-597">![Passer un appel ou envoyer un message instantané.](images/JJ945604.009cebe0-5a93-4745-89c3-8a16c7c13009(OCS.15).jpg "Passer un appel ou envoyer un message instantané.")</span><span class="sxs-lookup"><span data-stu-id="88c68-597">![Making a call or sending an IM.](images/JJ945604.009cebe0-5a93-4745-89c3-8a16c7c13009(OCS.15).jpg "Making a call or sending an IM.")</span></span>

<span data-ttu-id="88c68-598">La figure suivante illustre l’affichage par Response Group Agent Live du nombre actuel d’appels dans la file d’attente et le délai d’attente le plus long parmi tous les appels entrants.</span><span class="sxs-lookup"><span data-stu-id="88c68-598">The figure below illustrates how Response Group Agent Live displays the current number of calls in the queue and the longest waiting time among all these incoming calls.</span></span>

<span data-ttu-id="88c68-599">![Affichage des informations de la file d’attente.](images/JJ945604.131d7f79-b7ed-41f5-a9da-ffc556e31037(OCS.15).jpg "Affichage des informations de la file d’attente.")</span><span class="sxs-lookup"><span data-stu-id="88c68-599">![Viewing queue information.](images/JJ945604.131d7f79-b7ed-41f5-a9da-ffc556e31037(OCS.15).jpg "Viewing queue information.")</span></span>

</div>

<div>

## <a name="summary"></a><span data-ttu-id="88c68-600">Résumé</span><span class="sxs-lookup"><span data-stu-id="88c68-600">Summary</span></span>

<span data-ttu-id="88c68-601">Les connexion et déconnexion rapides, l’appartenance aux groupes et les statistiques de base en temps réel constituent des fonctionnalités intéressantes de Response Group Agent seulement disponibles en dehors de l’application à partir du service Response Group.</span><span class="sxs-lookup"><span data-stu-id="88c68-601">Fast sign-in and sign-out, group membership, and basic real-time statistics are interesting Response Group agent features that are only available outside the application from the Response Group service.</span></span> <span data-ttu-id="88c68-602">À l’aide de l’outil de gestion des ressources de l’agent Response Group, les administrateurs Lync peuvent fournir à leurs agents une application Windows qui leur permet d’effectuer des tâches de manière plus rapide et graphique.</span><span class="sxs-lookup"><span data-stu-id="88c68-602">With the Response Group Agent Live Resource Kit tool, Lync administrators can provide their agents with a Windows application that allows them to perform tasks in a faster and graphical way.</span></span>

</div>

</div>

<div>

## <a name="sefautil"></a><span data-ttu-id="88c68-603">SEFAUtil</span><span class="sxs-lookup"><span data-stu-id="88c68-603">SEFAUtil</span></span>

<span data-ttu-id="88c68-604">L’outil de ligne de commande SEFAUtil (activation de fonctionnalité d’extension secondaire) est un outil de ligne de commande qui permet aux administrateurs de logiciels Microsoft Lync 2013 Server et aux agents de support technique de configurer la sonnerie de délégué, le transfert d’appel, les sonneries simultanées, les paramètres d’appel d’équipe et le prélèvement d’appel de groupe pour le compte d’un utilisateur de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="88c68-604">SEFAUtil (secondary extension feature activation) is a command-line tool that enables Microsoft Lync Server 2013 communications software administrators and helpdesk agents to configure delegate-ringing, call-forwarding, simultaneous ringing, team-call settings and group call pickup on behalf of a Lync Server 2013 user.</span></span> <span data-ttu-id="88c68-605">L’outil permet également aux administrateurs d’interroger les paramètres de routage des appels publiés pour un utilisateur particulier. L’outil SEFAUtil permet à l’administrateur d’activer/désactiver/modifier le transfert d’appel ou la sonnerie simultanée pour le compte de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="88c68-605">The tool also allows administrators to query the call-routing settings that are published for a particular user.The SEFAUtil tool allows the administrator to enable/disable/modify call forwarding or simultaneously ringing on behalf of the user.</span></span> <span data-ttu-id="88c68-606">L’administrateur peut spécifier la cible (sous la forme d’un URI SIP) ou utiliser une cible qui a déjà été publiée par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="88c68-606">The administrator can specify the target (in the form of a SIP URI) or use a target that has already been published by the user.</span></span> <span data-ttu-id="88c68-607">Cet outil permet également aux administrateurs d’ajouter ou de supprimer des délégués ou des membres du groupe d’appel d’équipe pour le compte de l’utilisateur. Cet outil est bâti sur le 3,0 de Microsoft Unified Communications Management API (UCMA) et nécessite que les administrateurs créent une application fiable dans le magasin central de gestion pour SEFAUtil</span><span class="sxs-lookup"><span data-stu-id="88c68-607">This tool also allows administrators to add or remove delegates or team-call group members on behalf of the user.This tool is built on Microsoft Unified Communications Managed API (UCMA) 3.0 and requires that administrators create a trusted application in the Central Management store for SEFAUtil</span></span>

<span data-ttu-id="88c68-608">SEFAUtil (l’activation de la fonctionnalité d’extension secondaire) permet aux administrateurs et aux agents de support technique de Lync Server 2013 de configurer la sonnerie de délégué, le transfert d’appel, la sonnerie simultanée, les paramètres d’appel d’équipe et le prélèvement d’appel de groupe pour le compte d’un utilisateur de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="88c68-608">SEFAUtil (secondary extension feature activation) enables Lync Server 2013 administrators and helpdesk agents to configure delegate-ringing, call-forwarding, simultaneous ringing, team-call settings and group call pickup on behalf of a Lync Server 2013 user.</span></span> <span data-ttu-id="88c68-609">L’outil permet également aux administrateurs d’interroger les paramètres de routage des appels publiés pour un utilisateur particulier.</span><span class="sxs-lookup"><span data-stu-id="88c68-609">This tool also allows administrators to query the call-routing settings that are published for a particular user.</span></span>

<div>

## <a name="description"></a><span data-ttu-id="88c68-610">Description</span><span class="sxs-lookup"><span data-stu-id="88c68-610">Description</span></span>

<span data-ttu-id="88c68-611">La version actuelle de SEFAUtil n’est qu’un outil en ligne de commande, sans interface utilisateur graphique.</span><span class="sxs-lookup"><span data-stu-id="88c68-611">The current version of SEFAUtil is only a command-line tool; there is no supporting graphical user interface.</span></span> <span data-ttu-id="88c68-612">Cet outil repose sur le 3,0 de Microsoft Unified Communications Managed API (UCMA).</span><span class="sxs-lookup"><span data-stu-id="88c68-612">This tool is based on Microsoft Unified Communications Managed API (UCMA) 3.0.</span></span> <span data-ttu-id="88c68-613">Ses fonctionnalités permettent aux administrateurs et agents du support technique d’effectuer les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="88c68-613">The features in this tool allow administrators and helpdesk agents to do the following:</span></span>

  - <span data-ttu-id="88c68-614">afficher les paramètres de routage des appels d’un utilisateur (transfert d’appel, délégation, sonnerie simultanée, appel d’équipe et prise d’appel de groupe inclus) ;</span><span class="sxs-lookup"><span data-stu-id="88c68-614">View all call routing settings for a user (includes call-forwarding, delegation, simultaneous ringing, team-call and group call pickup)</span></span>

  - <span data-ttu-id="88c68-615">activer/désactiver/modifier les paramètres de transfert d’appel (destination et minuteur d’absence de réponse inclus) ;</span><span class="sxs-lookup"><span data-stu-id="88c68-615">Enable/disable/modify call-forwarding setting (includes destination and no-answer timer)</span></span>

  - <span data-ttu-id="88c68-616">activer/désactiver/modifier les configurations immédiates de transfert d’appel ;</span><span class="sxs-lookup"><span data-stu-id="88c68-616">Enable/disable/modify call-forwarding immediate configurations</span></span>

  - <span data-ttu-id="88c68-617">activer/désactiver/modifier les paramètres de délégation ;</span><span class="sxs-lookup"><span data-stu-id="88c68-617">Enable/disable/modify delegation settings</span></span>

  - <span data-ttu-id="88c68-618">activer/désactiver/modifier les paramètres d’appel d’équipe ;</span><span class="sxs-lookup"><span data-stu-id="88c68-618">Enable/disable/modify team-call group settings</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="88c68-619">Nouveautés de l’outil SEFAUtil de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="88c68-619">New in Lync Server 2013 SEFAUtil tool</span></span>

    
    </div>

  - <span data-ttu-id="88c68-620">activer/désactiver/modifier les paramètres de sonnerie simultanée (destination incluse) ;</span><span class="sxs-lookup"><span data-stu-id="88c68-620">Enable/disable/modify simultaneous ringing settings (includes destination)</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="88c68-621">Nouveautés de l’outil SEFAUtil de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="88c68-621">New in Lync Server 2013 SEFAUtil tool</span></span>

    
    </div>

  - <span data-ttu-id="88c68-622">activer/désactiver/modifier les paramètres de prise d’appel de groupe.</span><span class="sxs-lookup"><span data-stu-id="88c68-622">Enable/disable/modify group call pickup settings</span></span>
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="88c68-623">Nouveautés de l’outil SEFAUtil de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="88c68-623">New in Lync Server 2013 SEFAUtil tool</span></span>

    
    </div>

<span data-ttu-id="88c68-624">Cet outil présente les limitations suivantes :</span><span class="sxs-lookup"><span data-stu-id="88c68-624">This tool has the following limitations:</span></span>

  - <span data-ttu-id="88c68-625">Pris en charge uniquement pour les utilisateurs hébergés dans un pool de serveurs Lync</span><span class="sxs-lookup"><span data-stu-id="88c68-625">Supported only for users homed in a Lync Server pool</span></span>

  - <span data-ttu-id="88c68-626">modification en bloc des paramètres de routage des appels de plusieurs utilisateurs non prise en charge.</span><span class="sxs-lookup"><span data-stu-id="88c68-626">Bulk-edit of call routing settings for several users is not supported</span></span>

</div>

<div>

## <a name="output"></a><span data-ttu-id="88c68-627">Sortie</span><span class="sxs-lookup"><span data-stu-id="88c68-627">Output</span></span>

<span data-ttu-id="88c68-p179">La version actuelle de cet outil génère une sortie dans la fenêtre d’invite de commandes uniquement. Pour plus d’informations, voir la section Exemples plus loin dans ce document.</span><span class="sxs-lookup"><span data-stu-id="88c68-p179">The current version of this tool provides output only in the Command Prompt window. For details, see the Examples section later in this document.</span></span>

</div>

<div>

## <a name="purpose"></a><span data-ttu-id="88c68-630">Objectif</span><span class="sxs-lookup"><span data-stu-id="88c68-630">Purpose</span></span>

<span data-ttu-id="88c68-631">Voici certains des principaux scénarios d’utilisation de cet outil :</span><span class="sxs-lookup"><span data-stu-id="88c68-631">Following are some of the key scenarios where this tool may be used:</span></span>

  - <span data-ttu-id="88c68-632">Bob est une direction qui a été déplacée vers la téléphonie de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="88c68-632">Bob is an executive and has been moved to Lync Server telephony.</span></span> <span data-ttu-id="88c68-633">Il dispose d’une délégation sur son système PBX existant.</span><span class="sxs-lookup"><span data-stu-id="88c68-633">He has delegation on his existing PBX system.</span></span> <span data-ttu-id="88c68-634">Dans le cadre de la migration vers Lync, l’administrateur est en mesure de configurer le routage de Bob pour refléter sa configuration de délégation existante.</span><span class="sxs-lookup"><span data-stu-id="88c68-634">As part of the move to Lync, the administrator is able to configure Bob’s routing to reflect his pre-existing delegation configuration.</span></span>

  - <span data-ttu-id="88c68-p181">En plein déplacement, Alice réalise qu’elle attend un appel important d’un de ses clients. Elle se trouve toutefois à l’hôtel et n’a accès à aucun ordinateur. Elle contacte le support technique pour leur demander de transférer vers son numéro de téléphone portable tous les appels reçus sur son numéro de téléphone professionnel. Les membres du personnel du support technique peuvent effectuer cette opération de configuration pour elle.</span><span class="sxs-lookup"><span data-stu-id="88c68-p181">Alice is travelling and realizes that she is expecting an important call from one of her customers. However, she is in a hotel and has no access to a computer. She calls the helpdesk and requests that they forward to her mobile number all the calls made to her work number. The helpdesk personnel are able to do the configuration on her behalf.</span></span>

  - <span data-ttu-id="88c68-p182">Les appels reçus par Jean sur son numéro de téléphone professionnel sont transférés vers la messagerie vocale de son téléphone portable lorsqu’il se trouve sur son lieu de travail. Pour autant, tout semble fonctionner correctement dans la plupart des autres endroits. Le technicien du support technique consulte la configuration de routage de Jean et découvre que la sonnerie simultanée est configurée sur le téléphone portable de Jean. Il interroge Jean sur la couverture mobile sur son lieu de travail et parvient à déterminer que la règle de sonnerie simultanée est à l’origine du transfert des appels vers le messagerie vocale du téléphone portable de Jean lorsque sa couverture réseau est médiocre.</span><span class="sxs-lookup"><span data-stu-id="88c68-p182">Joe’s calls to his work number are going to his mobile voicemail whenever he is at work; however, things appear to be working correctly in most other locations. The helpdesk technician is able to view Joe’s routing configuration and discovers that Joe has simultaneous ringing configured to his mobile phone. The technician asks Joe about the mobile coverage at his office and is able to determine that the simultaneous ringing rule is what is causing the calls to go to Joe’s mobile voicemail when his network coverage is poor.</span></span>

  - <span data-ttu-id="88c68-642">Michel est un nouvel employé de contoso et il rejoint une nouvelle équipe sur laquelle tous les membres sont configurés pour l’appel d’équipe, lorsque l’utilisateur a activé Microsoft Lync, l’administrateur est en mesure de définir les paramètres de son groupe d’appel d’équipe pour inclure tous les membres de son équipe, l’administrateur peut également ajouter Michel en tant que membre du groupe d’appel d’équipe.</span><span class="sxs-lookup"><span data-stu-id="88c68-642">Mike is a new employee at Contoso and he’s joining a new team on which all members are configured for team-call, when being enabled for Microsoft Lync, the administrator is able to set his team-call group settings to include all his new team members, additionally, the administrator adds Mike as a team-call group member for each of the members in his team.</span></span>

  - <span data-ttu-id="88c68-643">Une pratique du service client dépendant du service Ressources humaines de Contoso consiste à offrir un service personnel à tous les appelants dès le premier appel.</span><span class="sxs-lookup"><span data-stu-id="88c68-643">A customer service practice in the human resources department at Contoso is to provide personal service for all callers since the first call.</span></span> <span data-ttu-id="88c68-644">Tous les membres du service étant assis à proximité les uns des autres, la sonnerie de tous les téléphones en même temps en raison de l’activation de l’appel d’équipe est très perturbant pour le personnel.</span><span class="sxs-lookup"><span data-stu-id="88c68-644">Given that all members of the department sit very close to each other, having all phones ringing at the same time with team-call is very disruptive for the team.</span></span> <span data-ttu-id="88c68-645">Pour fournir le meilleur service sans perturber les membres de l’équipe, l’administrateur de Lync tire parti de la fonctionnalité de cueillette des appels de groupe.</span><span class="sxs-lookup"><span data-stu-id="88c68-645">To provide the best service without disrupting the team members, the Lync administrator takes advantage of the Group Call Pickup capability.</span></span> <span data-ttu-id="88c68-646">Il ajoute tous les membres du service à un groupe de prise d’appel et communique le numéro de ce groupe au service.</span><span class="sxs-lookup"><span data-stu-id="88c68-646">The administrator adds all department members to a pickup group and communicates to the department the pickup group number.</span></span> <span data-ttu-id="88c68-647">Pierre remarque que le téléphone de Samira sonne, alors que celle-ci s’est absentée, et prend donc l’appel à partir de son propre bureau.</span><span class="sxs-lookup"><span data-stu-id="88c68-647">When Samantha is absent from her desk, Joe notices her phone ringing and he proceeds to answer the call from his desk.</span></span>

</div>

<div>

## <a name="requirements"></a><span data-ttu-id="88c68-648">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="88c68-648">Requirements</span></span>

<span data-ttu-id="88c68-p184">L’outil SEFAUtil peut seulement être exécuté sur un ordinateur faisant partie d’un pool d’applications approuvées. UCMA 3.0 doit être installé sur cet ordinateur. Pour exécuter l’outil, une application approuvée avec l’ID d’application SEFAUtil doit être créée sur ce pool.</span><span class="sxs-lookup"><span data-stu-id="88c68-p184">The SEFAUtil tool can be run only on a computer that is a part of a Trusted Application Pool. UCMA 3.0 must be installed on that computer. To run the tool, a new Trusted Application with the SEFAUtil application ID must be created on that pool.</span></span>

<span data-ttu-id="88c68-652">**Création d’une application approuvée pour l’outil SEFAUtil**</span><span class="sxs-lookup"><span data-stu-id="88c68-652">**Creating a new Trusted Application for the SEFAUtil tool**</span></span>

1.  <span data-ttu-id="88c68-653">L’outil SEFAUtil ne peut être exécuté que sur un ordinateur qui fait partie d’un pool d’applications approuvées.</span><span class="sxs-lookup"><span data-stu-id="88c68-653">The SEFAUTil tool can be run only on a computer that is part of a trusted application pool.</span></span> <span data-ttu-id="88c68-654">Le cas échéant, l’ajout d’un pool en tant que nouveau pool d’applications approuvé peut être réalisé via Lync Server Management Shell avec l’applet de commande suivante :</span><span class="sxs-lookup"><span data-stu-id="88c68-654">If needed, adding a pool as a new trusted application pool can be done via the Lync Server Management Shell with the following cmdlet:</span></span>
    
        New-CsTrustedApplicationPool -id <Pool FQDN> -Registrar <Pool Registrar FQDN> -site Site:<Pool Site>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="88c68-655">UCMA 3.0 doit être installé sur les ordinateurs qui seront utilisés pour exécuter l’outil SEFAUtil.</span><span class="sxs-lookup"><span data-stu-id="88c68-655">UCMA 3.0 must be installed on any computer that will be used to run the SEFAUtil tool.</span></span>

    
    </div>

2.  <span data-ttu-id="88c68-656">Une application approuvée doit être définie dans la topologie pour l’outil SEFAUtil.</span><span class="sxs-lookup"><span data-stu-id="88c68-656">A trusted application needs to be defined in the topology for the SEFAUtil tool.</span></span> <span data-ttu-id="88c68-657">Pour définir SEFAUtil en tant que nouvelle application fiable, utilisez Lync Server Management Shell et exécutez l’applet de commande suivante :</span><span class="sxs-lookup"><span data-stu-id="88c68-657">To define SEFAUtil as a new trusted application, use the Lync Server Management Shell and execute the following cmdlet:</span></span>
    
        New-CsTrustedApplication -ApplicationId sefautil -TrustedApplicationPoolFqdn <Pool FQDN>  -Port 7489
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="88c68-658">Un autre port peut être utilisé au besoin.</span><span class="sxs-lookup"><span data-stu-id="88c68-658">A different port can be used if needed.</span></span>

    
    </div>

3.  <span data-ttu-id="88c68-659">Les modifications apportées à la topologie doivent être activées.</span><span class="sxs-lookup"><span data-stu-id="88c68-659">The topology changes need to be enabled.</span></span> <span data-ttu-id="88c68-660">Il est possible d’activer les changements de topologie via Lync Server Management Shell en exécutant l’applet de commande suivante :</span><span class="sxs-lookup"><span data-stu-id="88c68-660">Enabling the topology changes can be done via the Lync Server Management Shell by executing the following cmdlet:</span></span>
    
        Enable-CsToplogy

4.  <span data-ttu-id="88c68-661">Le cas échéant, installez les outils du kit de ressources de Lync Server 2013 sur le serveur qui sera utilisé pour exécuter l’outil SEFAUtil (le serveur doit faire partie d’un pool d’applications approuvé).</span><span class="sxs-lookup"><span data-stu-id="88c68-661">If needed, install the Lync Server 2013 Resource Kit Tools in the server that will be used to run the SEFAUtil tool (the server must be part of a trusted application pool).</span></span>

5.  <span data-ttu-id="88c68-662">Vérifiez que SEFAUtil est correctement exécuté.</span><span class="sxs-lookup"><span data-stu-id="88c68-662">Verify the SEFAUtil is running correctly.</span></span> <span data-ttu-id="88c68-663">Pour ce faire, exécutez l’outil à partir d’une invite de commandes de Windows avec des privilèges d’administrateur pour afficher les paramètres de transfert d’appel d’un utilisateur dans le déploiement.</span><span class="sxs-lookup"><span data-stu-id="88c68-663">To do this, run the tool from a windows command prompt with administrator privileges to display the call forwarding settings of a user in the deployment.</span></span> <span data-ttu-id="88c68-664">Par défaut, l’outil se trouve dans la section : "... \\ Fichiers programme \\ Microsoft Lync Server 2013 \\ reskit.</span><span class="sxs-lookup"><span data-stu-id="88c68-664">By default the tool will be located in: “…\\Program Files\\Microsoft Lync Server 2013\\Reskit”.</span></span> <span data-ttu-id="88c68-665">Pour afficher les paramètres de transfert d’appel d’un utilisateur, utilisez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="88c68-665">To display the call forwarding settings of a user, use the following command:</span></span>
    
        SEFAUtil.exe <user SIP address> /server:<Lync Server/Pool FQDN>
    
    <span data-ttu-id="88c68-666">Les paramètres de transfert d’appel de l’utilisateur doivent s’afficher.</span><span class="sxs-lookup"><span data-stu-id="88c68-666">The call forwarding settings of the user should be displayed.</span></span>

<div>

## <a name="group-call-pickup"></a><span data-ttu-id="88c68-667">Prise d’appel de groupe</span><span class="sxs-lookup"><span data-stu-id="88c68-667">Group Call Pickup</span></span>

<span data-ttu-id="88c68-668">La collecte d’appels de groupe nécessite une configuration supplémentaire dans Lync Server pour que la fonctionnalité soit entièrement activée.</span><span class="sxs-lookup"><span data-stu-id="88c68-668">Group Call Pickup requires additional configuration in Lync Server for the capability to be fully enabled.</span></span> <span data-ttu-id="88c68-669">Avant d’affecter les groupes de prise d’appels aux utilisateurs, consultez la documentation sur la prise d’appel de groupe pour connaître les étapes de planification et de déploiement de cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="88c68-669">Before assigning pickup groups to users, refer to the Group Call Pickup product documentation for the planning and deployment steps of this capability.</span></span>

</div>

</div>

<div>

## <a name="examples"></a><span data-ttu-id="88c68-670">Exemples</span><span class="sxs-lookup"><span data-stu-id="88c68-670">Examples</span></span>

<div>

## <a name="display-current-call-handling-settings"></a><span data-ttu-id="88c68-671">Afficher les paramètres actuels de gestion des appels</span><span class="sxs-lookup"><span data-stu-id="88c68-671">Display Current Call Handling Settings</span></span>

<span data-ttu-id="88c68-672">La commande suivante affiche le traitement des appels pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="88c68-672">The following command displays the call handling for the user.</span></span> `SEFAUtil.exe /server:lyncserver.contoso.com katarina@contoso.com`

<div>


> [!NOTE]  
> <span data-ttu-id="88c68-673">Cet exemple utilise le commutateur <STRONG>/Server</STRONG> pour spécifier le serveur Lync auquel se connecter.</span><span class="sxs-lookup"><span data-stu-id="88c68-673">This example uses the <STRONG>/server</STRONG> switch to specify the Lync Server to connect to.</span></span>



</div>

<span data-ttu-id="88c68-674">**Sortie**</span><span class="sxs-lookup"><span data-stu-id="88c68-674">**Output**</span></span>

    User Aor: sip:katarina@contoso.com
    Display Name: Katarina Larsson
    UM Enabled: True
    Simulring enabled: False
    User Ring time: 00:00:20
    Call Forward No Answer to: voicemail

</div>

<div>

## <a name="set-the-call-forwardno-answer-destination"></a><span data-ttu-id="88c68-675">Définir la destination du transfert d’appel/en cas d’absence de réponse</span><span class="sxs-lookup"><span data-stu-id="88c68-675">Set the Call Forward/No Answer Destination</span></span>

<span data-ttu-id="88c68-676">Cet exemple définit la destination d’appel/non de réponse et le délai de sonnerie.</span><span class="sxs-lookup"><span data-stu-id="88c68-676">This example sets the call forward/no answer destination and the ring delay.</span></span> <span data-ttu-id="88c68-677">Ici, le commutateur/Server n’est pas fourni ; SEFAUtil tente de découvrir automatiquement le serveur Lync.</span><span class="sxs-lookup"><span data-stu-id="88c68-677">Here, the /server switch is not provided; SEFAUtil attempts to autodiscover the Lync Server.</span></span>

    SEFAUtil.exe /server:lyncserver.contoso.com sip:katarina@contoso.com /enablefwdnoanswer /callanswerwaittime:30 /setfwddestination:+1425555 0126@contoso.com;user=phone

<span data-ttu-id="88c68-678">**Sortie**</span><span class="sxs-lookup"><span data-stu-id="88c68-678">**Output**</span></span>

    User Aor: sip:katarina@contoso.com
    Display Name: Katarina Larsson
    UM Enabled: True
    Simulring enabled: False
    User Ring time: 00:00:30
    Call Forward No Answer to: sip:+14255550126@contoso.com;user=phone

</div>

<div>

## <a name="enable-call-forwarding-immediately"></a><span data-ttu-id="88c68-679">Activer le transfert d’appel immédiatement</span><span class="sxs-lookup"><span data-stu-id="88c68-679">Enable Call Forwarding Immediately</span></span>

<span data-ttu-id="88c68-680">Cet exemple active immédiatement le transfert d’appel vers un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="88c68-680">This example immediately enables call-forwarding to another user.</span></span>

    SEFAUtil.exe sip:katarina@contoso.com /enablefwdimmediate /setfwddestination:anders@contoso.com

<span data-ttu-id="88c68-681">**Sortie**</span><span class="sxs-lookup"><span data-stu-id="88c68-681">**Output**</span></span>

    User Aor: sip:katarina@contoso.com
    Display Name: Katarina Larsson
    UM Enabled: True
    Simulring enabled: False
    Forward immediate to: sip:anders@contoso.com

</div>

<div>

## <a name="disable-call-forwarding-immediately"></a><span data-ttu-id="88c68-682">Désactiver immédiatement le transfert d’appel</span><span class="sxs-lookup"><span data-stu-id="88c68-682">Disable Call Forwarding Immediately</span></span>

<span data-ttu-id="88c68-683">Cet exemple désactivé immédiatement le transfert d’appel.</span><span class="sxs-lookup"><span data-stu-id="88c68-683">This example immediately disables call forwarding.</span></span>

    SEFAUtil.exe /server:lyncserver.contoso.com katarina@contoso.com  /disablefwdimmediate

<span data-ttu-id="88c68-684">**Sortie**</span><span class="sxs-lookup"><span data-stu-id="88c68-684">**Output**</span></span>

    User Aor: sip:katarina@contoso.com
    Display Name: Katarina Larsson
    UM Enabled: True
    Simulring enabled: False
    User Ring time: 00:00:30
    Call Forward No Answer to: voicemail

</div>

<div>

## <a name="add-a-user-as-a-delegate-and-set-up-simultaneous-ringing-of-delegates"></a><span data-ttu-id="88c68-685">Ajouter un utilisateur en tant que délégué et définir la sonnerie simultanée des délégués</span><span class="sxs-lookup"><span data-stu-id="88c68-685">Add a User as a Delegate and Set Up Simultaneous Ringing of Delegates</span></span>

<span data-ttu-id="88c68-686">Cet exemple ajoute un utilisateur en tant que délégué et définit la sonnerie simultanée des délégués.</span><span class="sxs-lookup"><span data-stu-id="88c68-686">This example adds a user as a delegate and sets up simultaneous ringing of delegates.</span></span>

    SEFAUtil.exe /server:lyncserver.contoso.com sip:katarina@contoso.com /adddelegate:joe@contoso.com /simulringdelegates

<span data-ttu-id="88c68-687">**Sortie**</span><span class="sxs-lookup"><span data-stu-id="88c68-687">**Output**</span></span>

    User Aor: sip:katarina@contoso.com
    Display Name: Katarina Larsson
    UM Enabled: True
    Simultaneously Ringing Delegates: sip:joe@contoso.com

</div>

<div>

## <a name="change-simultaneous-ringing-rule-of-delegates"></a><span data-ttu-id="88c68-688">Modifier la règle de sonnerie simultanée des délégués</span><span class="sxs-lookup"><span data-stu-id="88c68-688">Change Simultaneous Ringing Rule of Delegates</span></span>

<span data-ttu-id="88c68-689">Cet exemple modifie la règle de sonnerie simultanée définie dans l’exemple précédent en règle de sonnerie différée.</span><span class="sxs-lookup"><span data-stu-id="88c68-689">This example changes the simultaneous ringing rule that was set in the previous example to the delayed ringing rule.</span></span>

    SEFAUtil.exe /server:lyncserver.contoso.com sip:katarina@contoso.com /delayringdelegates:10

<span data-ttu-id="88c68-690">**Sortie**</span><span class="sxs-lookup"><span data-stu-id="88c68-690">**Output**</span></span>

    User Aor: sip:katarina@contoso.com
    Display Name: Katarina Larsson
    UM Enabled: True
    Simulring enabled: False
    Delay Ringing Delegates (delay:10 seconds): sip:joe@contoso.com

</div>

<div>

## <a name="remove-the-delegate"></a><span data-ttu-id="88c68-691">Supprimer le délégué</span><span class="sxs-lookup"><span data-stu-id="88c68-691">Remove the Delegate</span></span>

<span data-ttu-id="88c68-692">Cet exemple supprime le délégué.</span><span class="sxs-lookup"><span data-stu-id="88c68-692">This example removes the delegate.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="88c68-693">Une fois le dernier délégué supprimé, la sonnerie sur le poste de délégués est désactivée automatiquement.</span><span class="sxs-lookup"><span data-stu-id="88c68-693">When the last delegate is removed, delegate ringing is automatically disabled.</span></span>



</div>

    SEFAUtil.exe /server:lyncserver.contoso.com sip:katarina@contoso.com /removedelegate:joe@contoso.com

<span data-ttu-id="88c68-694">**Sortie**</span><span class="sxs-lookup"><span data-stu-id="88c68-694">**Output**</span></span>

    User Aor: sip:katarina@contoso.com
    Display Name: Katarina Larsson
    UM Enabled: True
    Simulring enabled: False
    User Ring time: 00:00:30
    Call Forward No Answer to: voicemail

</div>

<div>

## <a name="add-a-delegate-and-set-up-the-call-forward-to-delegates-rule"></a><span data-ttu-id="88c68-695">Ajouter un délégué et définir la règle de transfert d’appel aux délégués</span><span class="sxs-lookup"><span data-stu-id="88c68-695">Add a Delegate and Set Up the Call-Forward to Delegates Rule</span></span>

<span data-ttu-id="88c68-696">Cet exemple ajoute un délégué et définit la règle de transfert d’appel aux délégués.</span><span class="sxs-lookup"><span data-stu-id="88c68-696">This example adds a delegate and sets up the call-forward to delegates rule.</span></span>

    SEFAUtil.exe /server:lyncserver.contoso.com sip:katarina@contoso.com /adddelegate:anders@contoso.com /fwdtodelegates

<span data-ttu-id="88c68-697">**Sortie**</span><span class="sxs-lookup"><span data-stu-id="88c68-697">**Output**</span></span>

    User Aor: sip:katarina@contoso.com
    Display Name: Katarina Larsson
    UM Enabled: True
    Forwarding calls to Delegates: sip:anders@contoso.com

</div>

<div>

## <a name="enable-simultaneous-ringing-and-set-a-destination-number"></a><span data-ttu-id="88c68-698">Activer la sonnerie simultanée et définir un numéro de destination</span><span class="sxs-lookup"><span data-stu-id="88c68-698">Enable Simultaneous Ringing and Set a Destination Number</span></span>

<span data-ttu-id="88c68-699">Cet exemple active la sonnerie simultanée et définit un numéro de destination pour la sonnerie simultanée.</span><span class="sxs-lookup"><span data-stu-id="88c68-699">This example enables simultaneous ringing and sets a simultaneous ringing destination number.</span></span>

    SEFAUtil.exe /server:lyncserver.contoso.com sip:katarina@contoso.com /setsimulringdestination:+14255550126 /enablesimulring

<div>


> [!NOTE]  
> <span data-ttu-id="88c68-700">Pour modifier le numéro de destination de la sonnerie simultanée d’un utilisateur pour lequel la sonnerie simultanée est déjà activée, conservez la commande avec le commutateur /enablesimulring, sans quoi le numéro de destination ne sera pas modifié.</span><span class="sxs-lookup"><span data-stu-id="88c68-700">To change the simultaneous ringing destination number of a user that has already simultaneous ringing enabled, keep the command with the /enablesimulring switch, otherwise the destination number will not be changed.</span></span>



</div>

<span data-ttu-id="88c68-701">**Sortie**</span><span class="sxs-lookup"><span data-stu-id="88c68-701">**Output**</span></span>

    User Aor: sip:katarina@contoso.com
    Display Name: Katarina Larsson
    UM Enabled: True
    Simulring enabled: True
    Simul_Ringing to: sip:+14255550126@contoso.com;user=phone

</div>

<div>

## <a name="disable-simultaneous-ringing"></a><span data-ttu-id="88c68-702">Désactiver la sonnerie simultanée</span><span class="sxs-lookup"><span data-stu-id="88c68-702">Disable Simultaneous Ringing</span></span>

<span data-ttu-id="88c68-703">Cet exemple désactive la sonnerie simultanée.</span><span class="sxs-lookup"><span data-stu-id="88c68-703">This example disables simultaneous ringing.</span></span>

    SEFAUtil.exe /server:lyncserver.contoso.com sip:katarina@contoso.com /disablesimulring

<span data-ttu-id="88c68-704">**Sortie**</span><span class="sxs-lookup"><span data-stu-id="88c68-704">**Output**</span></span>

    User Aor: sip:katarina@contoso.com
    Display Name: Katarina Larsson
    UM Enabled: True
    Simulring enabled: False
    User Ring time: 00:00:30
    Call Forward No Answer to: voicemail

</div>

<div>

## <a name="add-a-team-member-for-team-call-and-set-up-simultaneous-ringing-to-the-team-call-members-group"></a><span data-ttu-id="88c68-705">Ajouter un membre d’équipe pour l’appel d’équipe et définir la sonnerie simultanée sur le groupe d’appel d’équipe</span><span class="sxs-lookup"><span data-stu-id="88c68-705">Add a Team Member for Team-Call and Set up Simultaneous Ringing to the Team-Call Members Group</span></span>

<span data-ttu-id="88c68-706">Cet exemple ajoute un membre d’équipe au groupe d’appel d’équipe d’un utilisateur et active la sonnerie simultanée sur le groupe d’appel d’équipe.</span><span class="sxs-lookup"><span data-stu-id="88c68-706">This example adds a team member to the team-call group of a user and enables simultaneous ringing to the team-call group.</span></span>

    SEFAUtil.exe /server:lyncserver.contoso.com sip:katarina@contoso.com /addteammember:anders@contoso.com /simulringteam

<div>


> [!NOTE]  
> <span data-ttu-id="88c68-707">L’ajout d’un membre au groupe d’appel d’équipe d’un utilisateur définit automatiquement les paramètres de sonnerie simultanée des utilisateurs sur la sonnerie simultanée de son groupe d’appel d’équipe.</span><span class="sxs-lookup"><span data-stu-id="88c68-707">Adding a member to the team-call group of a user will automatically switch the simultaneous ringing settigs of the users to simulring his team-call group.</span></span>



</div>

<span data-ttu-id="88c68-708">**Sortie**</span><span class="sxs-lookup"><span data-stu-id="88c68-708">**Output**</span></span>

    User Aor: sip:katarina@contoso.com
    Display Name: Katarina Larsson
    UM Enabled: True
    Team ringing enabled. Team: sip:anders@contoso.com

</div>

<div>

## <a name="remove-a-member-from-the-team-call-group"></a><span data-ttu-id="88c68-709">Supprimer un membre du groupe d’appel d’équipe</span><span class="sxs-lookup"><span data-stu-id="88c68-709">Remove a Member from the Team-Call Group</span></span>

<span data-ttu-id="88c68-710">Cet exemple supprime un membre d’équipe du groupe d’appel d’équipe d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="88c68-710">This example removes a team member of the team-call group of a user.</span></span>

    SEFAUtil.exe /server:lyncserver.contoso.com sip:katarina@contoso.com /removeteammember:anders@contoso.com

<div>


> [!NOTE]  
> <span data-ttu-id="88c68-711">Si le membre supprimé est le seul du groupe d’appel d’équipe, la sonnerie simultanée du groupe d’appel d’équipe est automatiquement désactivée.</span><span class="sxs-lookup"><span data-stu-id="88c68-711">If the member being removed is the only member of the team-call group, simultaneously ringing to the team-call group will be automatically disabled.</span></span>



</div>

<span data-ttu-id="88c68-712">**Sortie**</span><span class="sxs-lookup"><span data-stu-id="88c68-712">**Output**</span></span>

    User Aor: sip:katarina@contoso.com
    Display Name: Katarina Larsson
    UM Enabled: True
    User Ring time: 00:00:30
    Call Forward No Answer to: voicemail

</div>

<div>

## <a name="set-the-delayed-ring-to-the-team-call-group"></a><span data-ttu-id="88c68-713">Définir la sonnerie différée sur le groupe d’appel d’équipe</span><span class="sxs-lookup"><span data-stu-id="88c68-713">Set the Delayed Ring to the Team-Call Group</span></span>

<span data-ttu-id="88c68-714">Cet exemple définit la sonnerie différée sur le paramètre d’heure du groupe d’appel d’équipe.</span><span class="sxs-lookup"><span data-stu-id="88c68-714">This example changes the delayed ring to the team-call group time setting.</span></span>

    SEFAUtil.exe /server:lyncserver.contoso.com sip:katarina@contoso.com /delayringteam:5

<span data-ttu-id="88c68-715">**Sortie**</span><span class="sxs-lookup"><span data-stu-id="88c68-715">**Output**</span></span>

    User Aor: sip:katarina@contoso.com
    Display Name: Katarina Larsson
    UM Enabled: True
    Delay Ringing Team (delay:5 seconds). Team: sip:anders@contoso.com

</div>

<div>

## <a name="enable-team-call"></a><span data-ttu-id="88c68-716">Activer l’appel d’équipe</span><span class="sxs-lookup"><span data-stu-id="88c68-716">Enable Team-Call</span></span>

<span data-ttu-id="88c68-717">Cet exemple active l’appel d’équipe pour un utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="88c68-717">This example enables team-call for a given user.</span></span>

    SEFAUtil.exe /server:lyncserver.contoso.com sip:katarina@contoso.com /simulringteam

<div>


> [!NOTE]  
> <span data-ttu-id="88c68-718">S’il n’y a aucun membre dans le groupe d’appel d’équipe de l’utilisateur, l’appel d’équipe ne sera pas activé.</span><span class="sxs-lookup"><span data-stu-id="88c68-718">If the team-call group of the user has no members, team-call won’t be enabled.</span></span>



</div>

<span data-ttu-id="88c68-719">**Sortie**</span><span class="sxs-lookup"><span data-stu-id="88c68-719">**Output**</span></span>

</div>

<div>

## <a name="disable-team-call"></a><span data-ttu-id="88c68-720">Désactiver l’appel d’équipe</span><span class="sxs-lookup"><span data-stu-id="88c68-720">Disable Team-Call</span></span>

<span data-ttu-id="88c68-721">Cet exemple désactive l’appel d’équipe pour un utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="88c68-721">This example disables team-call for a given user.</span></span>

    SEFAUtil.exe /server:lyncserver.contoso.com sip:katarina@contoso.com /disableteamcall

<span data-ttu-id="88c68-722">**Sortie**</span><span class="sxs-lookup"><span data-stu-id="88c68-722">**Output**</span></span>

    User Aor: sip:katarina@contoso.com
    Display Name: Katarina Larsson
    UM Enabled: True
    User Ring time: 00:00:30
    Call Forward No Answer to: voicemail

</div>

<div>

## <a name="enable-group-call-pickup-and-assign-a-pickup-group-to-a-user"></a><span data-ttu-id="88c68-723">Activer la prise d’appel de groupe et affecter un groupe de prise d’appel à un utilisateur</span><span class="sxs-lookup"><span data-stu-id="88c68-723">Enable Group Call Pickup and Assign a Pickup Group to a User</span></span>

<span data-ttu-id="88c68-724">Cet exemple affecte un groupe de prise d’appel à un utilisateur et active la prise d’appel de groupe.</span><span class="sxs-lookup"><span data-stu-id="88c68-724">This example assigns a pickup group to a user and enables Group Call Pickup.</span></span>

    SEFAUtil.exe /server:lyncserver.contoso.com sip:katarina@contoso.com /enablegrouppickup:199

<span data-ttu-id="88c68-725">**Sortie**</span><span class="sxs-lookup"><span data-stu-id="88c68-725">**Output**</span></span>

    User Aor: sip:katarina@contoso.com
    Display Name: Katarina Larsson
    UM Enabled: True
    Group Pickup Orbit: sip:199;phone-context=user-default@ contoso.com;user=phone

</div>

<div>

## <a name="disable-group-call-pickup"></a><span data-ttu-id="88c68-726">Désactiver la prise d’appel de groupe</span><span class="sxs-lookup"><span data-stu-id="88c68-726">Disable Group Call Pickup</span></span>

<span data-ttu-id="88c68-727">Cet exemple désactive la prise d’appel de groupe pour un utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="88c68-727">This example disables Group Call Pickup for a given user.</span></span>

    SEFAUtil.exe /server:lyncserver.contoso.com sip:katarina@contoso.com /disablegrouppickup

<div>


> [!NOTE]  
> <span data-ttu-id="88c68-p191">Lorsque vous désactivez la prise d’appel de groupe pour un utilisateur, le numéro de groupe affecté à cet utilisateur n’est pas conservé. Si vous souhaitez ultérieurement réactiver la prise d’appel de groupe pour cet utilisateur, vous devez réaffecter le numéro de groupe avec le commutateur /enablegrouppickup.</span><span class="sxs-lookup"><span data-stu-id="88c68-p191">When you disable Group Call Pickup for a user, the group number that was assigned to the user is not retained. If you subsequently want to re-enable Group Call Pickup for that user, you must assign the group number again with the /enablegrouppickup switch.</span></span>



</div>

    User Aor: sip:katarina@contoso.com
    Display Name: Katarina Larsson
    UM Enabled: True

</div>

</div>

</div>

<div>

## <a name="sysprepps1"></a><span data-ttu-id="88c68-730">SYSPrep.ps1</span><span class="sxs-lookup"><span data-stu-id="88c68-730">SYSPrep.ps1</span></span>

<div>

## <a name="description"></a><span data-ttu-id="88c68-731">Description</span><span class="sxs-lookup"><span data-stu-id="88c68-731">Description</span></span>

<span data-ttu-id="88c68-732">SYSPrep.ps1 est un script Windows PowerShell qui installe les conditions préalables de Lync Server 2013 suivantes sur votre ordinateur de système d’exploitation Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="88c68-732">SYSPrep.ps1 is a Windows PowerShell script that will install the following Lync Server 2013 prerequisites on your Windows Server 2008 operating system machine.</span></span>

  - <span data-ttu-id="88c68-733">Microsoft .Net Framework 4.5</span><span class="sxs-lookup"><span data-stu-id="88c68-733">Microsoft .Net Framework 4.5</span></span>

  - <span data-ttu-id="88c68-734">Microsoft SQL Server Express ;</span><span class="sxs-lookup"><span data-stu-id="88c68-734">Microsoft SQL Server Express</span></span>

  - <span data-ttu-id="88c68-735">Windows Powershell version 3.0</span><span class="sxs-lookup"><span data-stu-id="88c68-735">Windows Powershell version 3.0</span></span>

  - <span data-ttu-id="88c68-736">Visual C++ 2010 Redistributable</span><span class="sxs-lookup"><span data-stu-id="88c68-736">Visual C++ 2010 Redistributable</span></span>

  - <span data-ttu-id="88c68-737">Mises à jour d’Internet Information Services</span><span class="sxs-lookup"><span data-stu-id="88c68-737">Internet Information Server Updates</span></span>

  - <span data-ttu-id="88c68-738">Windows Identity Foundation</span><span class="sxs-lookup"><span data-stu-id="88c68-738">Windows Identity Foundation</span></span>

  - <span data-ttu-id="88c68-739">Fichiers principaux de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="88c68-739">Lync Server 2013 Core files</span></span>

<span data-ttu-id="88c68-740">Si le nom du script est semblable à l’outil de préparation du système pour les systèmes d’exploitation Microsoft Windows, ils sont toutefois différents.</span><span class="sxs-lookup"><span data-stu-id="88c68-740">While the script name is similar to the System Preparation Tool for the Microsoft Windows operating systems, they are different.</span></span> <span data-ttu-id="88c68-741">Ce script installe uniquement les prérequis requis pour Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="88c68-741">This script will only install the required prerequisites for Lync Server 2013.</span></span> <span data-ttu-id="88c68-742">Une fois ceux-ci installés, l’outil Windows SYSPrep peut ensuite être utilisé pour créer une image du serveur.</span><span class="sxs-lookup"><span data-stu-id="88c68-742">Once those prerequisites are installed, the Windows SYSPrep tool can then be used to create an image of the server.</span></span>

</div>

<div>

## <a name="requirements"></a><span data-ttu-id="88c68-743">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="88c68-743">Requirements</span></span>

<span data-ttu-id="88c68-744">Avant d’exécuter le script SYSPrep.ps1, vous devez copier les fichiers requis vers un dossier local de l’ordinateur du système d’exploitation Windows Server 2008 (par exemple **, D : \\ Setup)**.</span><span class="sxs-lookup"><span data-stu-id="88c68-744">Prior to running the SYSPrep.ps1 script, you must copy the prerequisite files to a local folder on the Windows Server 2008 operating system machine (for example **D:\\Setup)**.</span></span> <span data-ttu-id="88c68-745">Ce dossier doit également inclure une copie des fichiers 2013 du serveur Lync, spécifiquement **Setup.exe.**</span><span class="sxs-lookup"><span data-stu-id="88c68-745">This folder must also include a copy of the Lync Server 2013 files, specifically **Setup.exe.**</span></span> <span data-ttu-id="88c68-746">Les fichiers des logiciels prérequis peuvent être téléchargés aux emplacements suivants :</span><span class="sxs-lookup"><span data-stu-id="88c68-746">The prerequisite files can be downloaded from the following locations:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="88c68-747">Logiciels prérequis</span><span class="sxs-lookup"><span data-stu-id="88c68-747">Prerequisite</span></span></th>
<th><span data-ttu-id="88c68-748">Emplacement</span><span class="sxs-lookup"><span data-stu-id="88c68-748">Location</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="88c68-749">Microsoft .Net Framework 4.5</span><span class="sxs-lookup"><span data-stu-id="88c68-749">Microsoft .Net Framework 4.5</span></span></p></td>
<td><p>https://go.microsoft.com/?linkid=9816306</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88c68-750">Microsoft SQL Server Express 2008 R2</span><span class="sxs-lookup"><span data-stu-id="88c68-750">Microsoft SQL Server Express 2008 R2</span></span></p></td>
<td><p>https://www.microsoft.com/download/details.aspx?id=23650</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88c68-751">Windows Powershell version 3.0</span><span class="sxs-lookup"><span data-stu-id="88c68-751">Windows Powershell version 3.0</span></span></p></td>
<td><p>https://www.microsoft.com/download/details.aspx?id=34595</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88c68-752">Visual C++ 2010 Redistributable</span><span class="sxs-lookup"><span data-stu-id="88c68-752">Visual C++ 2010 Redistributable</span></span></p></td>
<td><p>https://www.microsoft.com/download/details.aspx?id=5555</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88c68-753">Mises à jour d’Internet Information Services</span><span class="sxs-lookup"><span data-stu-id="88c68-753">Internet Information Server Updates</span></span></p></td>
<td><p>https://www.microsoft.com/download/details.aspx?id=34869</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88c68-754">Windows Identity Foundation</span><span class="sxs-lookup"><span data-stu-id="88c68-754">Windows Identity Foundation</span></span></p></td>
<td><p>https://www.microsoft.com/download/details.aspx?id=17331</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88c68-755">Lync Server 2013 Setup.exe</span><span class="sxs-lookup"><span data-stu-id="88c68-755">Lync Server 2013 Setup.exe</span></span></p></td>
<td><p><span data-ttu-id="88c68-756">Copier à partir de la version média de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="88c68-756">Copy from Lync Server 2013 media</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="parameter"></a><span data-ttu-id="88c68-757">Paramètre</span><span class="sxs-lookup"><span data-stu-id="88c68-757">Parameter</span></span>

<span data-ttu-id="88c68-758">Le paramètre **–SetupFolder** prend comme argument l’emplacement de répertoire des fichiers prérequis.</span><span class="sxs-lookup"><span data-stu-id="88c68-758">The **–SetupFolder** parameter takes as an argument the directory location of the prerequisite files</span></span>

</div>

<div>

## <a name="examples"></a><span data-ttu-id="88c68-759">Exemples</span><span class="sxs-lookup"><span data-stu-id="88c68-759">Examples</span></span>

<span data-ttu-id="88c68-760">Pour exécuter le script de SYSPrep.ps1 et installer les composants requis de Lync Server 2013, exécutez la commande suivante à partir d’une invite de commandes avec élévation de privilèges :</span><span class="sxs-lookup"><span data-stu-id="88c68-760">To run the SYSPrep.ps1 script and install the Lync Server 2013 prerequisites, run the following command from an elevated command prompt:</span></span>

    ./SysPrep.PS1 -SetupFolder D:\Setup

</div>

</div>

<div>

## <a name="unassigned-number-announcements-migration"></a><span data-ttu-id="88c68-761">Unassigned Number Announcements Migration</span><span class="sxs-lookup"><span data-stu-id="88c68-761">Unassigned Number Announcements Migration</span></span>

<span data-ttu-id="88c68-762">L’outil de migration annonces du numéro non attribué permet à un administrateur de Lync de déplacer la configuration des numéros non attribués, qui est mise en service par l’application d’annonce à partir d’un serveur ou d’un pool Lync source vers un serveur ou un pool Lync de destination.</span><span class="sxs-lookup"><span data-stu-id="88c68-762">The Unassigned Number Announcements Migration tool enables a Lync administrator to move the unassigned numbers configuration that is serviced by the announcement application from a source Lync Server or Pool to a destination Lync Server or Pool.</span></span>

<div>

## <a name="description"></a><span data-ttu-id="88c68-763">Description</span><span class="sxs-lookup"><span data-stu-id="88c68-763">Description</span></span>

<span data-ttu-id="88c68-764">L’outil Unassigned Number Announcements Migration est un script Windows PowerShell qui déplace la configuration des numéros non attribués pris en charge par l’application d’annonce entre un pool ou un serveur source et un autre pool ou serveur.</span><span class="sxs-lookup"><span data-stu-id="88c68-764">The Unassigned Number Announcements Migration tool is a Windows PowerShell script that moves the unassigned numbers configuration serviced by the announcement application of a source server or pool to a different server or pool.</span></span>

<span data-ttu-id="88c68-765">Lorsqu’il est exécuté, le script Unassigned Number Announcements Migration effectue les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="88c68-765">When executed, the Unassigned Number Announcements Migration script will perform the following operations:</span></span>

1.  <span data-ttu-id="88c68-766">Déplacer tous les fichiers audio utilisés par les annonces de numéros non attribués de l’application d’annonce hébergée sur le pool ou serveur source vers le magasin de fichiers du pool ou serveur de destination.</span><span class="sxs-lookup"><span data-stu-id="88c68-766">Move all the audio files used by the unassigned number announcements of the announcement application hosted in the source server or pool to the file store of the destination server or pool.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="88c68-767">les fichiers audio sont supprimés du pool de sources une fois qu’ils sont copiés sur le pool de destination.</span><span class="sxs-lookup"><span data-stu-id="88c68-767">the audio files are removed from the source pool once they’re copied to the destination pool.</span></span>

    
    </div>

2.  <span data-ttu-id="88c68-768">Déplacer les annonces de numéros non attribués configurées pour l’application d’annonce hébergée dans le pool ou serveur source vers le pool ou serveur de destination.</span><span class="sxs-lookup"><span data-stu-id="88c68-768">Move all unassigned number announcements configured for the announcement application hosted in the source server or pool to the destination server or pool.</span></span>

3.  <span data-ttu-id="88c68-769">Réaffecter toutes les plages de numéros non attribués prises en charge par l’application d’annonce hébergée dans le pool ou serveur source vers le pool ou serveur de destination.</span><span class="sxs-lookup"><span data-stu-id="88c68-769">Reassign all the unassigned number ranges that are serviced by the announcement application hosted in the source server or pool to the destination server or pool.</span></span>

<span data-ttu-id="88c68-770">Une fois le script correctement exécuté, toutes les plages de numéros affectés prises en charge par l’application d’annonce hébergée dans le pool ou serveur source sont à présent prises en charge avec la même configuration par le pool ou le serveur de destination.</span><span class="sxs-lookup"><span data-stu-id="88c68-770">After successfully running the script, all the unassigned number ranges that were serviced by the announcement application hosted in the source server or pool will now be serviced with the same configuration by the destination server or pool.</span></span>

</div>

<div>

## <a name="output"></a><span data-ttu-id="88c68-771">Sortie</span><span class="sxs-lookup"><span data-stu-id="88c68-771">Output</span></span>

<span data-ttu-id="88c68-772">Le script **Move-CsAnnouncementConfiguration** indique dans la fenêtre Lync Management Shell à partir de laquelle il a exécuté la réussite ou l’échec de l’opération de migration.</span><span class="sxs-lookup"><span data-stu-id="88c68-772">The **Move-CsAnnouncementConfiguration** script indicates in the Lync Management Shell window from where it’s executed the success or failure of the migration operation.</span></span>

<span data-ttu-id="88c68-p194">Si l’exécution de l’opération est interrompue par une erreur, les plages de numéros non attribués correctement déplacées vers la destination sont conservées dans la destination sous une forme opérationnelle et le reste des plages de numéros non attribués à migrer sont conservés dans la source sous une forme opérationnelle également. Pour migrer entièrement le reste de la configuration, exécutez à nouveau le script après avoir traité l’erreur.</span><span class="sxs-lookup"><span data-stu-id="88c68-p194">If the execution of the operation is interrupted by any error, the unassigned number ranges that were successfully moved to the destination will remain in the destination in an operational form and the rest of the unassigned number ranges to be migrated will remain in the source as well in an operational form. To fully migrate the rest of the configuration, rerun the script after addressing the error.</span></span>

</div>

<div>

## <a name="purpose"></a><span data-ttu-id="88c68-775">Objectif</span><span class="sxs-lookup"><span data-stu-id="88c68-775">Purpose</span></span>

<span data-ttu-id="88c68-776">Le script Unassigned Number Announcements Migration peut être utilisé dans le cadre des scénarios suivants :</span><span class="sxs-lookup"><span data-stu-id="88c68-776">The Unassigned Number Announcements Migration script can be used in the following three scenarios:</span></span>

  - <span data-ttu-id="88c68-777">**Migration des paramètres de configuration vers une nouvelle version de Lync Server :** Contoso est en train de migrer vers Lync Server 2013 et dans le cadre du processus de migration, l’administrateur du serveur Lync souhaite déplacer la configuration des numéros non attribués servi par l’application de l’annonce à partir du déploiement de Lync Server 2010 vers le nouveau déploiement Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="88c68-777">**Migrating configuration settings to a new version of Lync Server:** Contoso is in the process of migrating to Lync Server 2013 and as part of the migration process the Lync Server administrator would like to move the unassigned numbers configuration serviced by the announcement application from the Lync Server 2010 deployment to the new Lync Server 2013 deployment.</span></span> <span data-ttu-id="88c68-778">Pour modifier les paramètres de configuration, l’administrateur du serveur Lync utilise l’outil de migration annonces du numéro non attribué.</span><span class="sxs-lookup"><span data-stu-id="88c68-778">To move the configuration settings, the Lync Server administrator uses the Unassigned Number Announcements Migration tool.</span></span>

  - <span data-ttu-id="88c68-779">**Restauration d’un déploiement de Lync server 2013 vers Lync server 2010 :** En raison de facteurs inattendus, contoso doit restaurer la migration vers le nouveau déploiement Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="88c68-779">**Rolling back a deployment from Lync Server 2013 to Lync Server 2010:** Due unexpected factors, Contoso has to roll back the migration to the new Lync Server 2013 deployment.</span></span> <span data-ttu-id="88c68-780">Pour limiter les perturbations du service, l’administrateur du serveur Lync utilise l’outil de migration annonces de numéros non attribués pour rétablir la configuration du déploiement de Lync Server 2013 sur le déploiement de Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="88c68-780">To minimize disruptions to the service, the Lync Server administrator uses the Unassigned Number Announcements Migration tool to roll back the configuration from the Lync Server 2013 deployment to the Lync Server 2010 deployment.</span></span>

  - <span data-ttu-id="88c68-781">**Déplacer des données entre des déploiements Lync :** Contoso est en train de remplacer tous les serveurs d’un pool par des serveurs plus récents.</span><span class="sxs-lookup"><span data-stu-id="88c68-781">**Moving data between Lync deployments:** Contoso is in the process of replacing all the servers of one pool with newer servers.</span></span> <span data-ttu-id="88c68-782">Sa stratégie consiste à déployer un nouveau pool Lync Server 2013, à déplacer toutes les données de l’ancien vers le nouveau pool, puis à déconseiller l’ancien pool.</span><span class="sxs-lookup"><span data-stu-id="88c68-782">Their strategy is to deploy a new Lync Server 2013 pool, move all the data from the old to the new pool, and then deprecate the old pool.</span></span> <span data-ttu-id="88c68-783">Une fois le nouveau pool déployé, l’outil Unassigned Number Announcements Migration est utilisé pour déplacer la configuration de l’ancien pool vers le nouveau.</span><span class="sxs-lookup"><span data-stu-id="88c68-783">Once the new pool is deployed, the Unassigned Number Announcements Migration tool is used to move the configuration from the old pool to the new one.</span></span>

<div>

## <a name="requirements"></a><span data-ttu-id="88c68-784">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="88c68-784">Requirements</span></span>

<span data-ttu-id="88c68-785">Les principaux éléments de configuration suivants sont requis pour exécuter correctement l’outil :</span><span class="sxs-lookup"><span data-stu-id="88c68-785">The following are the main requirements needed to successfully run the tool:</span></span>

1.  <span data-ttu-id="88c68-786">Le script doit être exécuté à partir d’un ordinateur sur lequel Lync Server 2013 Management Shell est installé.</span><span class="sxs-lookup"><span data-stu-id="88c68-786">The script must be run from a computer that has Lync Server 2013 Management Shell installed.</span></span>

2.  <span data-ttu-id="88c68-787">L’application d’annonce doit être déployée correctement sur les serveurs ou les pools Lync sources et cibles.</span><span class="sxs-lookup"><span data-stu-id="88c68-787">The announcement application has to be successfully deployed in the source and destination Lync Servers or Pools.</span></span>

<div>

## <a name="move-csannouncementconfiguration-script"></a><span data-ttu-id="88c68-788">Script Move-CsAnnouncementConfiguration.</span><span class="sxs-lookup"><span data-stu-id="88c68-788">Move-CsAnnouncementConfiguration script</span></span>

<span data-ttu-id="88c68-789">Le script Move-CsAnnouncementConfiguration nécessite les deux paramètres décrits dans le tableau suivant. </span><span class="sxs-lookup"><span data-stu-id="88c68-789">The Move-CsAnnouncementConfiguration script requires the two parameters that are described in the table below.</span></span>

<span data-ttu-id="88c68-790">![Paramètres de déplacement-CsAnnouncementConfiguration.](images/JJ945604.7ab66ad3-d0db-4d77-8b93-ebccf0cb0663(OCS.15).jpg "Paramètres Move-CsAnnouncementConfiguration.")</span><span class="sxs-lookup"><span data-stu-id="88c68-790">![Move-CsAnnouncementConfiguration parameters.](images/JJ945604.7ab66ad3-d0db-4d77-8b93-ebccf0cb0663(OCS.15).jpg "Move-CsAnnouncementConfiguration parameters.")</span></span>

</div>

</div>

</div>

<div>

## <a name="examples"></a><span data-ttu-id="88c68-791">Exemples</span><span class="sxs-lookup"><span data-stu-id="88c68-791">Examples</span></span>

<div>

## <a name="moving-the-unassigned-number-announcements-configuration-from-a-lync-server-2010-pool-to-a-lync-server-2013-pool"></a><span data-ttu-id="88c68-792">Déplacement de la configuration annonces du numéro non attribué d’un pool Lync Server 2010 vers un pool Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="88c68-792">Moving the Unassigned Number Announcements Configuration from a Lync Server 2010 Pool to a Lync Server 2013 Pool</span></span>

<span data-ttu-id="88c68-793">Dans cet exemple, les annonces de numéro non affectées du pool de destination (Lync Server 2010) sont placées dans la liste de destination (Lync Server 2013).</span><span class="sxs-lookup"><span data-stu-id="88c68-793">This example moves the unassigned number announcements from the source pool (Lync Server 2010) to the destination pool (Lync Server 2013).</span></span>

    Move-CsAnnouncementConfiguration.ps1 -Source LS2010Pool.contoso.com -Destination LS2013Pool.contoso.com

</div>

<div>

## <a name="moving-the-unassigned-number-announcements-configuration-from-a-lync-server-2013-pool-to-a-lync-server-2010-pool"></a><span data-ttu-id="88c68-794">Déplacement de la configuration annonces du numéro non attribué d’un pool Lync Server 2013 vers un pool Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="88c68-794">Moving the Unassigned Number Announcements Configuration from a Lync Server 2013 Pool to a Lync Server 2010 Pool</span></span>

<span data-ttu-id="88c68-795">Dans cet exemple, les annonces de numéro non affectées du pool de destination (Lync Server 2013) sont placées dans la liste de destination (Lync Server 2010).</span><span class="sxs-lookup"><span data-stu-id="88c68-795">This example moves the unassigned number announcements from the source pool (Lync Server 2013) to the destination pool (Lync Server 2010).</span></span>

    Move-CsAnnouncementConfiguration.ps1 -Source LS2013Pool.contoso.com -Destination LS2010Pool.contoso.com

</div>

</div>

</div>

<div>

## <a name="web-conf-data"></a><span data-ttu-id="88c68-796">Web Conf Data</span><span class="sxs-lookup"><span data-stu-id="88c68-796">Web Conf Data</span></span>

<span data-ttu-id="88c68-797">L’outil de données Web conf permet à un administrateur de logiciels de communication Lync Server 2013 d’avoir davantage de contrôle sur les données associées aux conférences Web de l’organisateur.</span><span class="sxs-lookup"><span data-stu-id="88c68-797">The Web Conf Data Tool allows an administrator of Lync Server 2013 communications software to have more control over the data associated with an organizer’s Web conferences.</span></span> <span data-ttu-id="88c68-798">Les scénarios incluent la possibilité de supprimer les données de réunion d’un utilisateur spécifique sur la base de critères de date/heure.</span><span class="sxs-lookup"><span data-stu-id="88c68-798">Scenarios include the ability to delete a specific user’s meeting data based on a time stamp criteria.</span></span>

<div>

## <a name="description"></a><span data-ttu-id="88c68-799">Description</span><span class="sxs-lookup"><span data-stu-id="88c68-799">Description</span></span>

<span data-ttu-id="88c68-800">Cet outil permet aux administrateurs d’effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="88c68-800">This tool allows the administrator to perform the following operations:</span></span>

1.  <span data-ttu-id="88c68-801">Rechercher les données de conférence web associées à un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="88c68-801">Find all Web conferencing data associated with a single user.</span></span>

2.  <span data-ttu-id="88c68-802">Supprimer les données de conférence web associées à un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="88c68-802">Delete all Web conferencing data associated with a single user.</span></span>

3.  <span data-ttu-id="88c68-803">Supprimer les données de conférence web associées à un utilisateur antérieures à une date donnée.</span><span class="sxs-lookup"><span data-stu-id="88c68-803">Delete all Web conferencing data associated with a single user that is older than a certain date.</span></span>

4.  <span data-ttu-id="88c68-804">Déplacer les données de conférence web associées à un utilisateur lorsque celui-ci est déplacé d’un pool vers un autre.</span><span class="sxs-lookup"><span data-stu-id="88c68-804">Move all Web conferencing data associated with a single user when that user is moved from one pool to another.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="88c68-805">Les outils du kit de ressources pour Lync Server 2010 pris en charge lors du déplacement de toutes les données de conférence Web associées à un utilisateur unique lorsque ce dernier est déplacé d’un pool à un autre.</span><span class="sxs-lookup"><span data-stu-id="88c68-805">The Resource Kit Tools for Lync Server 2010 supported moving all Web conferencing data associated with a single user when that user is moved from one pool to another.</span></span> <span data-ttu-id="88c68-806">Cette fonctionnalité a été supprimée de cet outil et remplacée par le paramètre  <STRONG>MoveConferenceData</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="88c68-806">That functionality is now deprecated from this tool in favor of the <STRONG>MoveConferenceData</STRONG> parameter.</span></span> <span data-ttu-id="88c68-807">Pour plus d’informations sur ce paramètre, voir l’applet de connexion <A href="https://technet.microsoft.com/library/gg398528(v=ocs.15)">Move-Csuser</A> .</span><span class="sxs-lookup"><span data-stu-id="88c68-807">For details about this parameter, see the <A href="https://technet.microsoft.com/library/gg398528(v=ocs.15)">Move-CsUser</A> cmdlet.</span></span>



</div>

<span data-ttu-id="88c68-p200">L’outil supprime les données de réunion uniquement pour les réunions inactives. Les réunions actives (ou réunions en sessions) ne peuvent pas être supprimées.</span><span class="sxs-lookup"><span data-stu-id="88c68-p200">The tool deletes meeting data only for meetings that are inactive. Active meetings (or meetings in sessions) cannot be deleted.</span></span>

<span data-ttu-id="88c68-p201">Cet outil doit être exécuté à partir d’un ordinateur situé dans le même pool que l’utilisateur cible. L’utilisateur dont les données de contenu de réunion sont gérées par cet outil doit être hébergé dans le même pool d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="88c68-p201">This tool must be run from a computer that is in the same pool as the target user. The user whose meeting content data is being managed by this tool must be homed in the same user pool.</span></span>

</div>

<div>

## <a name="output"></a><span data-ttu-id="88c68-812">Sortie</span><span class="sxs-lookup"><span data-stu-id="88c68-812">Output</span></span>

<span data-ttu-id="88c68-813">L’outil génère des résultats pour chacune des opérations :</span><span class="sxs-lookup"><span data-stu-id="88c68-813">This tool outputs the results of each of the operations:</span></span>

  - <span data-ttu-id="88c68-814">Si une requête est exécutée, l’outil génère la liste de tous les dossiers de données des réunions inactives organisées par cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="88c68-814">If a query is performed, the tool outputs the list of all inactive meeting data folders that have that user as an organizer.</span></span>

  - <span data-ttu-id="88c68-815">En cas de suppression, l’outil génère la liste des dossiers de données de toutes les réunions pour lesquelles les données seront supprimées.</span><span class="sxs-lookup"><span data-stu-id="88c68-815">If a delete is performed, the tool outputs the list of all meeting data folders whose data will be deleted.</span></span>

</div>

<div>

## <a name="requirements"></a><span data-ttu-id="88c68-816">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="88c68-816">Requirements</span></span>

<span data-ttu-id="88c68-817">L’outil doit être exécuté dans le même pool qui héberge actuellement l’organisateur.</span><span class="sxs-lookup"><span data-stu-id="88c68-817">The tool needs to be run in the same pool where the organizer is currently homed.</span></span>

<span data-ttu-id="88c68-818">L’outil doit être exécuté à l’aide de privilèges d’administrateur avec un accès au magasin de fichiers de contenu.</span><span class="sxs-lookup"><span data-stu-id="88c68-818">The tool must be run using administrator privileges with access to the Content File Store.</span></span>

</div>

<div>

## <a name="examples"></a><span data-ttu-id="88c68-819">Exemples</span><span class="sxs-lookup"><span data-stu-id="88c68-819">Examples</span></span>

<span data-ttu-id="88c68-820">Le tableau suivant décrit les paramètres (certains d’entre eux sont utilisés dans les exemples).</span><span class="sxs-lookup"><span data-stu-id="88c68-820">The following table describes the parameters, some of which are used in the examples.</span></span>

<span data-ttu-id="88c68-821">![Paramètres de l’outil de données Web CONF.](images/JJ945604.a733c1c6-5dfc-4874-a74f-bfdee81c1401(OCS.15).jpg "Paramètres de l’outil de données Web CONF.")</span><span class="sxs-lookup"><span data-stu-id="88c68-821">![Web Conf Data Tool parameters.](images/JJ945604.a733c1c6-5dfc-4874-a74f-bfdee81c1401(OCS.15).jpg "Web Conf Data Tool parameters.")</span></span>

    WebConfDataTool.exe /User:user0@contoso.com /Action:query ""/ExpirationDate:08/09/2010 12:00:00""

<span data-ttu-id="88c68-p202">L’exemple précédent montre le fonctionnement d’une commande de requête. La sortie d’une telle commande est une liste des dossiers de contenu de réunion affectés par cet outil.</span><span class="sxs-lookup"><span data-stu-id="88c68-p202">The preceding example shows how a query command would work. The output of such a command would be a list of all meeting content folders that would be affected by this tool.</span></span>

    WebConfDataTool.exe /User:user0@contoso.com /Action:delete

<span data-ttu-id="88c68-p203">L’exemple précédent est une commande de suppression. Cette commande supprime les dossiers des réunions inactives pour cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="88c68-p203">The preceding is an example of a delete command. The delete command will remove all inactive meeting folders from this user.</span></span>

</div>

<div>

## <a name="summary"></a><span data-ttu-id="88c68-826">Résumé</span><span class="sxs-lookup"><span data-stu-id="88c68-826">Summary</span></span>

<span data-ttu-id="88c68-827">Cet outil offre aux administrateurs un contrôle plus précis sur les données de réunion de conférence.</span><span class="sxs-lookup"><span data-stu-id="88c68-827">This tool can be a valuable resource to administrators who need more precise control over conference meeting data.</span></span>

<span data-ttu-id="88c68-828"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="88c68-828"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>
