---
title: Outils du kit de ressources techniques Lync Server 2013 permanents
description: Outils du kit de ressources techniques Lync Server 2013 permanents.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Lync Server 2013 Persistent Chat Resource Kit Tools
ms:assetid: 7a34d2ba-eb25-4e22-92d1-b9baf81b102c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945599(v=OCS.15)
ms:contentKeyID: 51541423
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 336e81c97da73da47eee654161a7d8d8956f9edb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438415"
---
# <a name="lync-server-2013-persistent-chat-resource-kit-tools"></a><span data-ttu-id="afc3c-103">Outils du kit de ressources techniques Lync Server 2013 permanents</span><span class="sxs-lookup"><span data-stu-id="afc3c-103">Lync Server 2013 Persistent Chat Resource Kit Tools</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="afc3c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="afc3c-104">

<span> </span></span></span>

<span data-ttu-id="afc3c-105">_**Dernière modification de la rubrique :** 2013-02-24_</span><span class="sxs-lookup"><span data-stu-id="afc3c-105">_**Topic Last Modified:** 2013-02-24_</span></span>

<span data-ttu-id="afc3c-106">Les outils du kit de ressources techniques Lync Server 2013 persistent pour faciliter les tâches de routine pour les administrateurs informatiques qui déploient et gèrent Lync Server 2013 permanent Chat Server.</span><span class="sxs-lookup"><span data-stu-id="afc3c-106">The Lync Server 2013 Persistent Chat Resource Kit tools help to make routine tasks easier for IT administrators who deploy and manage Lync Server 2013 Persistent Chat Server.</span></span> <span data-ttu-id="afc3c-107">Outre les instructions d’installation, cette rubrique décrit la finalité de chaque outil et des exemples de son utilisation.</span><span class="sxs-lookup"><span data-stu-id="afc3c-107">In addition to installation instructions, this topic describes the purpose of each tool, and examples of its use.</span></span>

<div>

## <a name="installation-of-the-resource-kit-tools"></a><span data-ttu-id="afc3c-108">Installation des outils du kit de ressources</span><span class="sxs-lookup"><span data-stu-id="afc3c-108">Installation of the Resource Kit Tools</span></span>

<span data-ttu-id="afc3c-109">Pour installer Lync Server 2013, les outils du kit de ressources, téléchargez **PersistentChatReskit.msi**.</span><span class="sxs-lookup"><span data-stu-id="afc3c-109">To install the Lync Server 2013, Resource Kit Tools, download **PersistentChatReskit.msi**.</span></span> <span data-ttu-id="afc3c-110">Exécutez **PersistentChatReskit.msi** pour effectuer une installation simple.</span><span class="sxs-lookup"><span data-stu-id="afc3c-110">Run **PersistentChatReskit.msi** to do a simple installation.</span></span> <span data-ttu-id="afc3c-111">Le fichier. msi installe tous les outils dans le chemin d’accès suivant : \\ **Program Files \\ Microsoft Lync Server 2013 \\ persistent Server Resource Kit**.</span><span class="sxs-lookup"><span data-stu-id="afc3c-111">The .msi installs all the tools in the following path: \\**Program Files\\ Microsoft Lync Server 2013\\Persistent Chat Server Resource Kit**.</span></span> <span data-ttu-id="afc3c-112">Les outils exécutables autonomes se trouvent dans ce dossier.</span><span class="sxs-lookup"><span data-stu-id="afc3c-112">Tools that are self-contained executables are in this folder.</span></span> <span data-ttu-id="afc3c-113">Les outils qui comportent également des fichiers se trouvent dans leurs propres sous-dossiers.</span><span class="sxs-lookup"><span data-stu-id="afc3c-113">Tools that also have files are in their own subfolders.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="afc3c-114">Après avoir installé les outils de kit de ressources de Lync Server 2013, vous devez installer <STRONG>PsExec.exe</STRONG> et copier <STRONG>PsExec.exe</STRONG> dans le chemin d’accès suivant : \\ <STRONG>Program Files \ Microsoft Lync Server 2013 \ Kit\ChatStressTool de ressources du serveur de conversation persistant</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="afc3c-114">After installing the Lync Server 2013, Resource Kit Tools, you must install <STRONG>PsExec.exe</STRONG> and copy <STRONG>PsExec.exe</STRONG> to the following path: \\<STRONG>Program Files\ Microsoft Lync Server 2013\Persistent Chat Server Resource Kit\ChatStressTool</STRONG>.</span></span> <span data-ttu-id="afc3c-115">Si vous ne copiez pas <STRONG>PsExec.exe</STRONG>, l’outil de contrainte de conversation permanente génère une exception d’erreur et ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="afc3c-115">If you do not copy <STRONG>PsExec.exe</STRONG>, the Persistent Chat Stress Tool will throw an error exception, and not perform correctly.</span></span> <span data-ttu-id="afc3c-116">Assurez-vous de respecter cette exigence préalable avant d’exécuter l’outil.</span><span class="sxs-lookup"><span data-stu-id="afc3c-116">Make sure that you meet this prerequisite requirement prior to running the tool.</span></span> <span data-ttu-id="afc3c-117">Pour plus d’informations sur l’installation de <STRONG>PsExec.exe</STRONG>, voir <A href="https://go.microsoft.com/fwlink/p/?linkid=282246">https://go.microsoft.com/fwlink/p/?LinkId=282246</A> .</span><span class="sxs-lookup"><span data-stu-id="afc3c-117">For details about installing <STRONG>PsExec.exe</STRONG>, see <A href="https://go.microsoft.com/fwlink/p/?linkid=282246">https://go.microsoft.com/fwlink/p/?LinkId=282246</A>.</span></span>



</div>

</div>

<div>

## <a name="supported-environments"></a><span data-ttu-id="afc3c-118">Environnements pris en charge</span><span class="sxs-lookup"><span data-stu-id="afc3c-118">Supported Environments</span></span>

<span data-ttu-id="afc3c-119">Pour des performances optimales, les outils du kit de ressources de Lync Server 2013 doivent être installés dans le même environnement et avec les mêmes spécifications requises pour Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="afc3c-119">For optimal performance, the Lync Server 2013, Resource Kit Tools should be installed in the same environment and with the same specifications that are required for Lync Server 2013.</span></span>

</div>

<div>

## <a name="resource-kit-tools-overview"></a><span data-ttu-id="afc3c-120">Présentation des outils du kit de ressources</span><span class="sxs-lookup"><span data-stu-id="afc3c-120">Resource Kit Tools Overview</span></span>

<span data-ttu-id="afc3c-121">Voici les outils fournis dans le kit de ressources de conversation permanente Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="afc3c-121">Here are the tools that are provided in the Lync Server 2013 Persistent Chat Resource Kit.</span></span> <span data-ttu-id="afc3c-122">La section suivante fournit une description de chaque outil, y compris la configuration requise et un exemple d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="afc3c-122">The following section provides a description of each tool, including requirements and example usage.</span></span>

  - <span data-ttu-id="afc3c-123">AffCheck</span><span class="sxs-lookup"><span data-stu-id="afc3c-123">AffCheck</span></span>

  - <span data-ttu-id="afc3c-124">ChatMonitoringSummary</span><span class="sxs-lookup"><span data-stu-id="afc3c-124">ChatMonitoringSummary</span></span>

  - <span data-ttu-id="afc3c-125">Outil ChatStress</span><span class="sxs-lookup"><span data-stu-id="afc3c-125">ChatStress Tool</span></span>

  - <span data-ttu-id="afc3c-126">ChatUpgradeVerifier</span><span class="sxs-lookup"><span data-stu-id="afc3c-126">ChatUpgradeVerifier</span></span>

  - <span data-ttu-id="afc3c-127">ChatUsageReport</span><span class="sxs-lookup"><span data-stu-id="afc3c-127">ChatUsageReport</span></span>

  - <span data-ttu-id="afc3c-128">ScheduleADSyncforPrincipal</span><span class="sxs-lookup"><span data-stu-id="afc3c-128">ScheduleADSyncforPrincipal</span></span>

</div>

<div>

## <a name="affcheck"></a><span data-ttu-id="afc3c-129">AffCheck</span><span class="sxs-lookup"><span data-stu-id="afc3c-129">AffCheck</span></span>

<div>

## <a name="description"></a><span data-ttu-id="afc3c-130">Description</span><span class="sxs-lookup"><span data-stu-id="afc3c-130">Description</span></span>

<span data-ttu-id="afc3c-131">L’outil AffCheck vérifie que la base de données principale de la base de données principale de chat et les enregistrements d’affiliation de groupe correspondent à ceux des services de domaine Active Directory (AD FS).</span><span class="sxs-lookup"><span data-stu-id="afc3c-131">The AffCheck tool confirms that the Persistent Chat back-end database user and group affiliation records match that of Active Directory Domain Services.</span></span>

</div>

<div>

## <a name="requirements"></a><span data-ttu-id="afc3c-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="afc3c-132">Requirements</span></span>

<span data-ttu-id="afc3c-133">L’outil est installé avec le programme d’installation PersistentChatResKit sur un ordinateur appartenant à un domaine.</span><span class="sxs-lookup"><span data-stu-id="afc3c-133">The tool is installed with the PersistentChatResKit installer on a domain joined machine.</span></span>

<span data-ttu-id="afc3c-134">Le compte d’utilisateur sous lequel l’outil est exécuté doit avoir accès en lecture à la base de données principale de chat permanent et aux services de domaine Active Directory.</span><span class="sxs-lookup"><span data-stu-id="afc3c-134">The user account under which the tool is run must have Read access to the Persistent Chat back-end database and Active Directory Domain Services.</span></span>

</div>

<div>

## <a name="usage"></a><span data-ttu-id="afc3c-135">Utilisation</span><span class="sxs-lookup"><span data-stu-id="afc3c-135">Usage</span></span>

<span data-ttu-id="afc3c-136">Configurez le fichier AffCheck.exe.config conformément aux instructions du fichier de configuration et exécutez l’outil AffCheck sans paramètres de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="afc3c-136">Configure the AffCheck.exe.config file according to the instructions in the config file and run the AffCheck tool without command-line parameters.</span></span> <span data-ttu-id="afc3c-137">Le contenu du AffCheck.exe.config par défaut est le suivant.</span><span class="sxs-lookup"><span data-stu-id="afc3c-137">Following are the contents of the default AffCheck.exe.config.</span></span>

<span data-ttu-id="afc3c-138">**AffCheck.exe.config :**</span><span class="sxs-lookup"><span data-stu-id="afc3c-138">**AffCheck.exe.config:**</span></span>

```XML
    <?xml version="1.0" encoding="utf-8" ?>
    <configuration>
      <appSettings>
        <!--Domain Controller IP Address-->
        <add key="LDAP" value="LDAP://0.0.0.0/"/>
        
        <!-- Domain DN  This is case sensitive, it must match exactly-->
        <add key="DomainComponent" value ="DC=DOMAIN,DC=COM"/>
        
        <!--Domain Administrator Login and Password-->
        <add key="DomainLogin" value="DOMAIN\Administrator"/>
        <add key="DomainPassword" value ="password"/>
        
        <!-- Connection string to Group Chat Database-->
        <add key="ConnectionString" value="data source=SQL_SERVER\INSTANCE;initial catalog=DATABASE_NAME;integrated security=SSPI"/>
        
        <!--Check group affiliations-->
        <add key="CheckGroups" value="true"/>
        
        <!--Check user affilations-->
        <add key="CheckUsers" value="true"/>
        
        <!--List all affiliations if there is a mismatch between database and active directory-->
        <add key="ListAffiliations" value="true"/>
    
        <!--If you need to offset the results of the number of affilations in AD(can be negative to add to AD parent count)-->
        <add key="Offset" value ="0"/>
    
        <!--If you need to ignore certain parents, provide a semi colon delimitted list.-->
        <add key="Ignore" value ="DC=uatest,DC=test,DC=contoso,DC=com;DC=test,DC=contoso,DC=com"/>
      </appSettings>
    </configuration>
  ```
</div>

</div>

<div>

## <a name="chatmonitoringsummary"></a><span data-ttu-id="afc3c-139">ChatMonitoringSummary</span><span class="sxs-lookup"><span data-stu-id="afc3c-139">ChatMonitoringSummary</span></span>

<div>

## <a name="description"></a><span data-ttu-id="afc3c-140">Description</span><span class="sxs-lookup"><span data-stu-id="afc3c-140">Description</span></span>

<span data-ttu-id="afc3c-141">L’outil PersistentChatMonitoringSummary déplace les informations de surveillance des conversations persistantes de la base de données de surveillance dans un fichier journal CSV spécifié.</span><span class="sxs-lookup"><span data-stu-id="afc3c-141">The PersistentChatMonitoringSummary tool moves Persistent Chat monitoring information from the monitoring database into a specified CSV log file.</span></span>

<span data-ttu-id="afc3c-142">Le fichier CSV contient une répartition des sessions de conversation persistantes en nombre de sessions totales, de sessions réussies, d’échecs inattendus, d’échecs attendus et de la description des échecs inattendus.</span><span class="sxs-lookup"><span data-stu-id="afc3c-142">The CSV file will contain a breakdown of Persistent Chat sessions by number of total sessions, successful sessions, unexpected failures, expected failures, and a breakdown of the unexpected failures by diagnostic ID, number of failures, and failure description.</span></span>

</div>

<div>

## <a name="requirements"></a><span data-ttu-id="afc3c-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="afc3c-143">Requirements</span></span>

<span data-ttu-id="afc3c-144">Installez les outils du kit de ressources de chat permanent sur un ordinateur appartenant à un domaine ayant accès à la base de données de surveillance.</span><span class="sxs-lookup"><span data-stu-id="afc3c-144">Install the Persistent Chat Resource Kit tools on a domain-joined machine that has access to the Monitoring database.</span></span>

<span data-ttu-id="afc3c-145">Le compte d’utilisateur sous lequel l’outil s’exécute doit avoir accès en lecture à la base de données de surveillance.</span><span class="sxs-lookup"><span data-stu-id="afc3c-145">The user account under which the tool runs must have Read access to the Monitoring database.</span></span>

<span data-ttu-id="afc3c-146">Le fichier, PersistentChatMonitoringSummary.exe.config, doit contenir une \<connectionStrings\> section définissant la chaîne de connexion à la base de données de surveillance.</span><span class="sxs-lookup"><span data-stu-id="afc3c-146">The file, PersistentChatMonitoringSummary.exe.config, must contain a \<connectionStrings\> section that defines the connection string to the Monitoring database.</span></span> <span data-ttu-id="afc3c-147">Elle doit également contenir une clé pour le PersistentChatEndpointUri pour lequel les données d’analyse seront collectées et un chemin d’accès de fichier vers un emplacement pour le fichier CSV qui sera généré.</span><span class="sxs-lookup"><span data-stu-id="afc3c-147">It must also contain a key for the PersistentChatEndpointUri that the monitoring data will be gathered for, and a file path to a location for the CSV file that will be generated.</span></span> <span data-ttu-id="afc3c-148">Pour obtenir des exemples, consultez le fichier de configuration installé.</span><span class="sxs-lookup"><span data-stu-id="afc3c-148">Refer to the installed config file for examples.</span></span> <span data-ttu-id="afc3c-149">Le fichier doit se trouver dans le même répertoire que l’outil.</span><span class="sxs-lookup"><span data-stu-id="afc3c-149">The file must be located in the same directory as the tool.</span></span>

</div>

<div>

## <a name="usage"></a><span data-ttu-id="afc3c-150">Utilisation</span><span class="sxs-lookup"><span data-stu-id="afc3c-150">Usage</span></span>

```Batch
    PersistentChatMonitoringSummary [-StartDateTime <date>] [-EndDateTime <date>]
```

<span data-ttu-id="afc3c-151">Ces paramètres définissent la sélection de données :</span><span class="sxs-lookup"><span data-stu-id="afc3c-151">These parameters define the selection of data:</span></span>

<span data-ttu-id="afc3c-152">**StartDateTime :** Éventuellement, spécifiez la date de début de la période de sélection.</span><span class="sxs-lookup"><span data-stu-id="afc3c-152">**StartDateTime:** Optionally specifies the start date of the selection period.</span></span> <span data-ttu-id="afc3c-153">Par défaut : 1/1/1753 12:00:00 AM</span><span class="sxs-lookup"><span data-stu-id="afc3c-153">Default: 1/1/1753 12:00:00 AM</span></span>

<span data-ttu-id="afc3c-154">**EndDateTime :** Spécifie éventuellement la dernière date de la période de sélection.</span><span class="sxs-lookup"><span data-stu-id="afc3c-154">**EndDateTime:** Optionally specifies the last date of the selection period.</span></span> <span data-ttu-id="afc3c-155">Par défaut : désormais</span><span class="sxs-lookup"><span data-stu-id="afc3c-155">Default: Now</span></span>

</div>

<div>

## <a name="example"></a><span data-ttu-id="afc3c-156">Exemple</span><span class="sxs-lookup"><span data-stu-id="afc3c-156">Example</span></span>

```Batch
    C:\Users\Administrator.VDOMAIN>Desktop\PersistentChatMonitoringSummary.exe
    Reading database connection information, Persistent Chat endpoint uri, and csv output path information from the application config file...
    Connecting to Monitoring database with connection string specified in the application config file...
    Gathering Persistent Chat Session Summary information between "1/1/1753 12:00:00 AM" and "11/19/2012 10:11:25 AM" for Persistent Chat Endpoint Uri "persistentChatEndpointUri@domain.com"...
    Press enter to continue or hit ctr-c if these settings are incorrect...
    
    The summary information about Persistent Chat sessions from the Monitoring database has been output to C:\PersistentChatMonitoring_dd4ace24-4c8a-4a3d-8fd4-591bdfacf47b.csv
    Press enter to exit...
```

</div>

</div>

<div>

## <a name="persistent-chat-stress-tool"></a><span data-ttu-id="afc3c-157">Outil de stress permanent de conversation</span><span class="sxs-lookup"><span data-stu-id="afc3c-157">Persistent Chat Stress Tool</span></span>

<div>

## <a name="description"></a><span data-ttu-id="afc3c-158">Description</span><span class="sxs-lookup"><span data-stu-id="afc3c-158">Description</span></span>

<span data-ttu-id="afc3c-159">L’outil de contraintes Permanentles de conversation fournit un moyen facile de simuler l’utilisation de la messagerie instantanée pour tester les performances du monde réel, y compris des modèles utilisateur variés pour mieux s’adapter à vos scénarios d’utilisation prévus.</span><span class="sxs-lookup"><span data-stu-id="afc3c-159">The Persistent Chat Stress tool provides an easy way to simulate usage of Persistent Chat to test real-world performance, including varied user models to better fit your expected usage scenarios.</span></span>

</div>

<div>

## <a name="requirements"></a><span data-ttu-id="afc3c-160">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="afc3c-160">Requirements</span></span>

<span data-ttu-id="afc3c-161">Installez les outils du kit de ressources de chat permanent sur un ordinateur appartenant à un domaine ayant accès à la base de données principale de conversation permanente.</span><span class="sxs-lookup"><span data-stu-id="afc3c-161">Install the Persistent Chat Resource Kit tools onto a domain-joined machine that has access to the Persistent Chat back-end database.</span></span>

<span data-ttu-id="afc3c-162">En plus de cet ordinateur *contrôleur* , vous aurez besoin de plusieurs machines de *chargement* .</span><span class="sxs-lookup"><span data-stu-id="afc3c-162">In addition to this *controller* machine, you will need several *loader* machines.</span></span> <span data-ttu-id="afc3c-163">Pour chaque 10K d’utilisation de votre modèle utilisateur, vous avez besoin d’au moins 4 Go de RAM libre sur un ordinateur de chargement.</span><span class="sxs-lookup"><span data-stu-id="afc3c-163">For every 10K users in your user model, you will need at least 4GB of free RAM on a loader machine.</span></span> <span data-ttu-id="afc3c-164">Par exemple, une opération d’exécution avec des utilisateurs de 80K nécessite environ 32 Go de mémoire vive (RAM) sur tous les ordinateurs de chargement.</span><span class="sxs-lookup"><span data-stu-id="afc3c-164">For example, a run with 80K users will require about 32GB of RAM spread across all loader machines.</span></span> <span data-ttu-id="afc3c-165">Nous vous recommandons d’avoir au moins trois machines de charge, quelle que soit la charge attendue.</span><span class="sxs-lookup"><span data-stu-id="afc3c-165">We recommend that you have at least three loader machines, regardless of expected load.</span></span>

<span data-ttu-id="afc3c-166">Les machines de chargeur doivent disposer de l’infrastructure .NET 4,5 ainsi que de l’infrastructure Visual C++ 2012 installée.</span><span class="sxs-lookup"><span data-stu-id="afc3c-166">Loader machines must have the .NET 4.5 Framework as well as the Visual C++ 2012 Redistributable installed.</span></span>

</div>

<div>

## <a name="configuration"></a><span data-ttu-id="afc3c-167">Configuration</span><span class="sxs-lookup"><span data-stu-id="afc3c-167">Configuration</span></span>

<span data-ttu-id="afc3c-168">Copiez les fichiers ChatStressTool dans un dossier partagé accessible à partir de tous les ordinateurs de chargement.</span><span class="sxs-lookup"><span data-stu-id="afc3c-168">Copy ChatStressTool files into a shared folder accessible from all loader machines.</span></span>

<span data-ttu-id="afc3c-169">Créer des utilisateurs et des canaux à utiliser dans le stress :</span><span class="sxs-lookup"><span data-stu-id="afc3c-169">Create users and channels for use in the stress run:</span></span>

  - <span data-ttu-id="afc3c-170">Créez autant d’utilisateurs que vous le souhaitez, vous pouvez les activer pour Lync et définir leur stratégie de discussion persistante sur activé.</span><span class="sxs-lookup"><span data-stu-id="afc3c-170">Create as many users as your user model calls for, enable them for Lync, and set their Persistent Chat policy to Enabled.</span></span>

  - <span data-ttu-id="afc3c-171">Créez une catégorie pour vos canaux de stress, puis créez autant de salles que nécessaire dans cette catégorie.</span><span class="sxs-lookup"><span data-stu-id="afc3c-171">Create a category for your stress channels, and then create as many rooms as are needed under that category.</span></span> <span data-ttu-id="afc3c-172">La catégorie doit avoir tous les utilisateurs de stress dans sa liste **autorisée** (par le biais de l’ajout de leur UO) et les salles de stress doivent avoir un paramètre de confidentialité d' **Open**.</span><span class="sxs-lookup"><span data-stu-id="afc3c-172">The category should have all stress users in its **Allowed** list (by way of adding their OU), and stress rooms should have a privacy setting of **Open**.</span></span>

  - <span data-ttu-id="afc3c-173">Nous vous recommandons de créer des salles de stress supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="afc3c-173">We recommend creating extra stress rooms.</span></span> <span data-ttu-id="afc3c-174">Vous pouvez créer des salles 50 000 à l’aide de la commande d’interface de ligne de commande Windows PowerShell suivante :</span><span class="sxs-lookup"><span data-stu-id="afc3c-174">You can create 50,000 rooms with the following Windows PowerShell command-line interface command:</span></span>
    ```Powershell
        for ($i = 0; $i -le 50000; $i++) { New-CsPersistentChatRoom -Category <parent category> -Name "StressChan_$i" -Privacy Open }
    ```    

<span data-ttu-id="afc3c-175">Modifiez les fichiers de configuration pour qu’ils s’intègrent à votre topologie :</span><span class="sxs-lookup"><span data-stu-id="afc3c-175">Edit the configuration files to fit your topology:</span></span>

<span data-ttu-id="afc3c-176">Dans **LoaderProcess.exe.config**, remplacez « Controller.contoso.com » par le nom de domaine complet (FQDN) de l’ordinateur contrôleur.</span><span class="sxs-lookup"><span data-stu-id="afc3c-176">In **LoaderProcess.exe.config**, change “controller.contoso.com” to the controller machine’s fully qualified domain name (FQDN).</span></span>

<span data-ttu-id="afc3c-177">Dans **StressLauncher.exe.config :**</span><span class="sxs-lookup"><span data-stu-id="afc3c-177">In **StressLauncher.exe.config:**</span></span>

1.  <span data-ttu-id="afc3c-178">Remplacez la valeur de paramètre « LoaderBinary » par le chemin d’accès du dossier partagé.</span><span class="sxs-lookup"><span data-stu-id="afc3c-178">Change the “LoaderBinary” setting value to the shared folder’s path.</span></span>

2.  <span data-ttu-id="afc3c-179">Changez « AdminUser »/« AdminPassword » en informations d’identification disposant d’un accès administrateur aux machines de chargeur.</span><span class="sxs-lookup"><span data-stu-id="afc3c-179">Change “AdminUser”/”AdminPassword” to credentials that have admin access to loader machines.</span></span>

3.  <span data-ttu-id="afc3c-180">Remplacez « ChannelCategory » par le nom de la catégorie sous laquelle les canaux de stress ont été créés.</span><span class="sxs-lookup"><span data-stu-id="afc3c-180">Change “ChannelCategory” to the name of the category that stress channels have been created under.</span></span>

4.  <span data-ttu-id="afc3c-181">Remplacez « UserNamePattern » et « UserPasswordPattern » par un modèle qui correspond à vos informations d’identification de l’utilisateur stress.</span><span class="sxs-lookup"><span data-stu-id="afc3c-181">Change “UserNamePattern” and “UserPasswordPattern” to a template that matches your stress user credentials.</span></span> <span data-ttu-id="afc3c-182">{0} est remplacé par le numéro d’index de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="afc3c-182">{0} is replaced with the user’s index number.</span></span>

5.  <span data-ttu-id="afc3c-183">Remplacez « Domain » par le domaine SIP de votre topologie de test.</span><span class="sxs-lookup"><span data-stu-id="afc3c-183">Change “Domain” to the SIP domain of your test topology.</span></span>

6.  <span data-ttu-id="afc3c-184">Changez « ConnectionString » en chaîne de connexion pour votre base de données principale de conversation permanente.</span><span class="sxs-lookup"><span data-stu-id="afc3c-184">Change “ConnectionString” to a connection string for your Persistent Chat back-end database.</span></span>

7.  <span data-ttu-id="afc3c-185">Changez « UserIndexStart » en index du premier utilisateur de stress.</span><span class="sxs-lookup"><span data-stu-id="afc3c-185">Change “UserIndexStart” to the index of the first stress user.</span></span>

8.  <span data-ttu-id="afc3c-186">Remplacez « LyncFQDN » par le nom de domaine complet (FQDN) du pool frontal.</span><span class="sxs-lookup"><span data-stu-id="afc3c-186">Change “LyncFQDN” to the FQDN of your Front End pool.</span></span>

9.  <span data-ttu-id="afc3c-187">Modifiez la liste « machines » pour inclure les noms d’ordinateur pour tous les ordinateurs de chargement.</span><span class="sxs-lookup"><span data-stu-id="afc3c-187">Modify the “Machines” list to include machine names for all of your loader machines.</span></span>

10. <span data-ttu-id="afc3c-188">Modifiez la valeur de l’option baseAddress du point de terminaison de service (la valeur par défaut est « controller.contoso.com ») en nom de domaine complet (FQDN) de votre ordinateur de contrôleur.</span><span class="sxs-lookup"><span data-stu-id="afc3c-188">Change the baseAddress of the service endpoint (default is “controller.contoso.com”) to the FQDN of your controller machine.</span></span>

</div>

<div>

## <a name="usage"></a><span data-ttu-id="afc3c-189">Utilisation</span><span class="sxs-lookup"><span data-stu-id="afc3c-189">Usage</span></span>

<span data-ttu-id="afc3c-190">Une fois la configuration terminée, ouvrez StressLauncher.exe sur l’ordinateur contrôleur.</span><span class="sxs-lookup"><span data-stu-id="afc3c-190">After configuration is complete, open StressLauncher.exe on the controller machine.</span></span> <span data-ttu-id="afc3c-191">Vous pouvez lancer StressLauncher comme n’importe quel utilisateur.</span><span class="sxs-lookup"><span data-stu-id="afc3c-191">You can launch StressLauncher as any user.</span></span> <span data-ttu-id="afc3c-192">Les informations d’identification à partir desquelles les processus de chargeur s’exécutent sur les ordinateurs de chargement doivent être spécifiées dans le fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="afc3c-192">The credentials under which the loader processes start on the loader machines must be specified in the config file.</span></span> <span data-ttu-id="afc3c-193">Vous devez également fournir une chaîne de connexion qui dispose d’un accès en lecture à la base de données principale de conversation permanente.</span><span class="sxs-lookup"><span data-stu-id="afc3c-193">You also must give a connection string that has Read access to the Persistent Chat back-end database.</span></span> <span data-ttu-id="afc3c-194">Si cette chaîne de connexion utilise l’authentification Windows intégrée, vous devez lancer StressLauncher en tant qu’utilisateur disposant de cet accès.</span><span class="sxs-lookup"><span data-stu-id="afc3c-194">If this connection string uses integrated Windows authentication, you must launch StressLauncher as a user that has this access.</span></span>

<span data-ttu-id="afc3c-195">Modifiez les paramètres du modèle utilisateur selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="afc3c-195">Alter the user model settings as needed.</span></span> <span data-ttu-id="afc3c-196">Cliquez sur **Démarrer la charge** pour lancer une exécution.</span><span class="sxs-lookup"><span data-stu-id="afc3c-196">Click **Start Load** to initiate a run.</span></span> <span data-ttu-id="afc3c-197">Après quelques minutes, les utilisateurs commenceront à se connecter et la barre de progression commencera à remplir.</span><span class="sxs-lookup"><span data-stu-id="afc3c-197">After a minute or so, users will start being signed in, and the progress bar will begin to fill.</span></span> <span data-ttu-id="afc3c-198">À ce stade, vous pouvez peut-être utiliser l’ordinateur de contrôleur fonctionnant et prendre des mesures de performance.</span><span class="sxs-lookup"><span data-stu-id="afc3c-198">At this point, you may can the controller machine working and take performance measurements.</span></span>

</div>

</div>

<div>

## <a name="chatupgradeverifier"></a><span data-ttu-id="afc3c-199">ChatUpgradeVerifier</span><span class="sxs-lookup"><span data-stu-id="afc3c-199">ChatUpgradeVerifier</span></span>

<div>

## <a name="description"></a><span data-ttu-id="afc3c-200">Description</span><span class="sxs-lookup"><span data-stu-id="afc3c-200">Description</span></span>

<span data-ttu-id="afc3c-201">ChatUpgradeVerifier est un outil de comparaison de base de données spécifique d’une conversation permanente.</span><span class="sxs-lookup"><span data-stu-id="afc3c-201">ChatUpgradeVerifier is a Persistent Chat specific database comparison tool.</span></span> <span data-ttu-id="afc3c-202">L’outil compare la base de données de discussion de groupe 2007 R2 ou la base de données de discussion de groupe 2010 (2007/2010Db) à la base de données de conversation 2013 2013Db ().</span><span class="sxs-lookup"><span data-stu-id="afc3c-202">The tool compares either the Group Chat 2007 R2 or Group Chat 2010 Database (2007/2010Db) to the Persistent Chat 2013 Database (2013Db).</span></span>

<span data-ttu-id="afc3c-203">L’outil vérifie, une par une, chaque catégorie, salle de conversation permanente et complément en 2007/2010Db pour voir s’il apparaît dans le 2013Db.</span><span class="sxs-lookup"><span data-stu-id="afc3c-203">The tool will check, one by one, each category, Persistent Chat room, and add-in in 2007/2010Db to see if it appears in the 2013Db.</span></span> <span data-ttu-id="afc3c-204">La comparaison inclut la vérification de tous les paramètres d’une catégorie, d’une salle de conversation ou d’un complément, de tout principal sur la catégorie et de n’importe quel principal d’un rôle dans la catégorie ou la salle de conversation.</span><span class="sxs-lookup"><span data-stu-id="afc3c-204">The comparison includes checking all settings on the category, chat room, or add-in, any principals in scope on the category, and any principal in a role on either the category or the chat room.</span></span> <span data-ttu-id="afc3c-205">Si une catégorie ou une salle de conversation ne s’affiche pas correctement dans le 2013Db, les différences seront générées dans un fichier de conflits.</span><span class="sxs-lookup"><span data-stu-id="afc3c-205">If a category or a chat room does not appear correctly in the 2013Db, the differences will be output to a conflicts file.</span></span> <span data-ttu-id="afc3c-206">Si, à l’issue de la mise à niveau, le 2007/2010Db est modifié et que cet outil est exécuté, il y a une différence de sortie dans le fichier de conflits.</span><span class="sxs-lookup"><span data-stu-id="afc3c-206">If, after the upgrade has occurred, the 2007/2010Db is changed and then this tool is run, there will be a differences output to the conflicts file.</span></span> <span data-ttu-id="afc3c-207">Notez que cette application est un outil de comparaison de bases de données uniquement et ne valide pas le processus de mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="afc3c-207">Note that this application is a database comparison tool only and does not validate the upgrade process.</span></span>

</div>

<div>

## <a name="requirements"></a><span data-ttu-id="afc3c-208">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="afc3c-208">Requirements</span></span>

<span data-ttu-id="afc3c-209">Installez les outils du kit de ressources pour les discussions permanentes sur un ordinateur appartenant à un domaine ayant accès aux bases de données principales de chat permanent (versions précédentes et actuelles pour les discussions permanentes).</span><span class="sxs-lookup"><span data-stu-id="afc3c-209">Install the Persistent Chat Resource Kit tools on a domain-joined machine that has access to the Persistent Chat back-end databases (previous and current versions for Persistent Chat).</span></span>

<span data-ttu-id="afc3c-210">Le compte d’utilisateur sous lequel l’outil s’exécute doit disposer d’un accès en lecture aux bases de données de chat permanent.</span><span class="sxs-lookup"><span data-stu-id="afc3c-210">The user account under which the tool runs must have Read access to the Persistent Chat databases.</span></span>

<span data-ttu-id="afc3c-211">Le fichier ChatUpgradeVerifier.exe.config doit contenir le paramètre GroupChat2007R2Db ou GroupChat2010Db, avec une chaîne de connexion à la base de données de discussion de groupe appropriée (groupchat 2007R2 ou 2010).</span><span class="sxs-lookup"><span data-stu-id="afc3c-211">The ChatUpgradeVerifier.exe.config file must contain either the GroupChat2007R2Db parameter or the GroupChat2010Db parameter, with a connection string to the appropriate Group Chat database (either Groupchat 2007R2 or 2010).</span></span> <span data-ttu-id="afc3c-212">Elle doit également contenir un paramètre PersistentChat2013Db, avec une chaîne de connexion à la base de données chat 2013.</span><span class="sxs-lookup"><span data-stu-id="afc3c-212">It must also contain a PersistentChat2013Db parameter, with a connection string to the Persistent Chat 2013 database.</span></span>

</div>

<div>

## <a name="usage"></a><span data-ttu-id="afc3c-213">Utilisation</span><span class="sxs-lookup"><span data-stu-id="afc3c-213">Usage</span></span>

<span data-ttu-id="afc3c-214">Exécutez **ChatUpgradeVerifier** sans aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="afc3c-214">Run **ChatUpgradeVerifier** without any parameters.</span></span>

</div>

<div>

## <a name="example"></a><span data-ttu-id="afc3c-215">Exemple</span><span class="sxs-lookup"><span data-stu-id="afc3c-215">Example</span></span>

<span data-ttu-id="afc3c-216">![Exécution de ChatUpgradeVerifier.exe.](images/JJ945599.4c273bc3-7926-47c7-ade7-34522721ebf9(OCS.15).jpg "Exécution de ChatUpgradeVerifier.exe.")</span><span class="sxs-lookup"><span data-stu-id="afc3c-216">![Running ChatUpgradeVerifier.exe.](images/JJ945599.4c273bc3-7926-47c7-ade7-34522721ebf9(OCS.15).jpg "Running ChatUpgradeVerifier.exe.")</span></span>

</div>

</div>

<div>

## <a name="persistent-chat-usage-report"></a><span data-ttu-id="afc3c-217">Rapport d’utilisation persistante des conversations</span><span class="sxs-lookup"><span data-stu-id="afc3c-217">Persistent Chat Usage Report</span></span>

<div>

## <a name="description"></a><span data-ttu-id="afc3c-218">Description</span><span class="sxs-lookup"><span data-stu-id="afc3c-218">Description</span></span>

<span data-ttu-id="afc3c-219">L’outil ChatUsageReport génère un rapport HTML de l’utilisation du service de chat permanent.</span><span class="sxs-lookup"><span data-stu-id="afc3c-219">The ChatUsageReport tool generates an HTML report of Persistent Chat service usage.</span></span>

</div>

<div>

## <a name="requirements"></a><span data-ttu-id="afc3c-220">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="afc3c-220">Requirements</span></span>

<span data-ttu-id="afc3c-221">Installez les outils du kit de ressources de chat permanent sur un ordinateur appartenant à un domaine ayant accès à la base de données principale de conversation permanente.</span><span class="sxs-lookup"><span data-stu-id="afc3c-221">Install the Persistent Chat Resource Kit tools on a domain-joined machine that has access to the Persistent Chat back-end database.</span></span>

<span data-ttu-id="afc3c-222">Le compte d’utilisateur sous lequel l’outil est exécuté doit avoir accès en lecture à la base de données principale de conversation permanente.</span><span class="sxs-lookup"><span data-stu-id="afc3c-222">The user account under which the tool is run must have Read access to the Persistent Chat back-end database.</span></span>

<span data-ttu-id="afc3c-223">Le fichier, ChatUsageReport.exe.config, doit contenir une \<connectionStrings\> section définissant la chaîne de connexion à la base de données principale de chat.</span><span class="sxs-lookup"><span data-stu-id="afc3c-223">The file, ChatUsageReport.exe.config, must contain a \<connectionStrings\> section defining the connection string to the Persistent Chat back-end database.</span></span> <span data-ttu-id="afc3c-224">Le contenu du fichier de configuration par défaut est inclus ici, à des fins de référence.</span><span class="sxs-lookup"><span data-stu-id="afc3c-224">The contents of the default config file are included here, for your reference.</span></span>

</div>

<div>

## <a name="usage"></a><span data-ttu-id="afc3c-225">Utilisation</span><span class="sxs-lookup"><span data-stu-id="afc3c-225">Usage</span></span>

```Powershell
    ChatUsageReport [-StartDate {date}] [-EndDate {date}] [-TopActiveUsers {n}] [-TopActiveRooms {n}] [-LeastActiveRooms {n}] [-RoomsInactiveSince {Date}] [-OutputFolder {path}]
```
<span data-ttu-id="afc3c-226">Ces paramètres définissent la sélection de données :</span><span class="sxs-lookup"><span data-stu-id="afc3c-226">These parameters define the selection of data:</span></span>

<span data-ttu-id="afc3c-227">**DateDébut :** Le cas échéant, spécifie la date de début UTC de la période de sélection.</span><span class="sxs-lookup"><span data-stu-id="afc3c-227">**StartDate:** Optionally specifies the UTC start date of the selection period.</span></span> <span data-ttu-id="afc3c-228">Par défaut : date au plus tôt</span><span class="sxs-lookup"><span data-stu-id="afc3c-228">Default: Earliest Date</span></span>

<span data-ttu-id="afc3c-229">**Date_fin :** Facultatif, spécifie la date de fin UTC de la période de sélection.</span><span class="sxs-lookup"><span data-stu-id="afc3c-229">**EndDate:** Optionally specifies the UTC end date of the selection period.</span></span> <span data-ttu-id="afc3c-230">Par défaut : désormais</span><span class="sxs-lookup"><span data-stu-id="afc3c-230">Default: Now</span></span>

<span data-ttu-id="afc3c-231">Ces paramètres définissent le mode d’affichage des données :</span><span class="sxs-lookup"><span data-stu-id="afc3c-231">These parameters define how and what data is displayed:</span></span>

<span data-ttu-id="afc3c-232">**TopActiveUsers :** Si ce paramètre est spécifié, le rapport inclut les n utilisateurs les plus actifs en fonction du nombre de messages que l’utilisateur a publiés dans la salle de conversation pendant la période sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="afc3c-232">**TopActiveUsers:** If this is specified, the report will include the n most active users in terms of the number of messages the user has posted in the chat room for the selected period.</span></span> <span data-ttu-id="afc3c-233">Par défaut : 10</span><span class="sxs-lookup"><span data-stu-id="afc3c-233">Default: 10</span></span>

<span data-ttu-id="afc3c-234">**TopActiveRooms :** Si ce paramètre est spécifié, le rapport inclura les n salles de conversation les plus actives pour le nombre de messages publiés dans la salle pendant la période sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="afc3c-234">**TopActiveRooms:** If this is specified, the report will include the n most active chat rooms in terms of the number of messages posted in the room for the selected period.</span></span> <span data-ttu-id="afc3c-235">Par défaut : 10</span><span class="sxs-lookup"><span data-stu-id="afc3c-235">Default: 10</span></span>

<span data-ttu-id="afc3c-236">**LeastActiveRooms :** Si ce paramètre est spécifié, le rapport inclura le numéro des salles de conversation actives pour le nombre de messages publiés dans la salle de conversation pendant la période sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="afc3c-236">**LeastActiveRooms:** If this is specified, the report will include the n least active chat rooms in terms of the number of messages posted in the chat room for the selected period.</span></span> <span data-ttu-id="afc3c-237">Au moins un message sera publié dans les salles.</span><span class="sxs-lookup"><span data-stu-id="afc3c-237">Rooms will have at least one message posted.</span></span> <span data-ttu-id="afc3c-238">Par défaut : 10</span><span class="sxs-lookup"><span data-stu-id="afc3c-238">Default: 10</span></span>

<span data-ttu-id="afc3c-239">**RoomsInactiveSince :** Si ce paramètre est spécifié, le rapport inclura une liste des salles de conversation inactives depuis la date spécifiée.</span><span class="sxs-lookup"><span data-stu-id="afc3c-239">**RoomsInactiveSince:** If this is specified, the report will include a list of chat rooms that have been inactive since the specified date.</span></span> <span data-ttu-id="afc3c-240">Valeur par défaut : heure entière</span><span class="sxs-lookup"><span data-stu-id="afc3c-240">Default: Entire Time</span></span>

<span data-ttu-id="afc3c-241">**OutputFolder :** Le dossier dans lequel se trouvent les images ChatUsageReport.html et Graph.</span><span class="sxs-lookup"><span data-stu-id="afc3c-241">**OutputFolder:** The folder where the ChatUsageReport.html and the graph images will be placed.</span></span> <span data-ttu-id="afc3c-242">Cette opération doit être définie dans le fichier de configuration ou la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="afc3c-242">This must be defined in the config file or on the command line.</span></span>

<span data-ttu-id="afc3c-243">Toutes les valeurs de paramètres de ligne de commande peuvent également être spécifiées dans le fichier ChatUsageReport.exe.config se trouvant dans le même répertoire que l’outil.</span><span class="sxs-lookup"><span data-stu-id="afc3c-243">All of the command line parameter values can also be specified in the ChatUsageReport.exe.config file that is located in the same directory as the tool.</span></span> <span data-ttu-id="afc3c-244">Si une valeur est spécifiée dans le fichier de configuration et la ligne de commande, la valeur de la ligne de commande remplace la valeur du fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="afc3c-244">If any value is specified in both the config file and the command line, the command line value will override the config file value.</span></span>

</div>

<div>

## <a name="output"></a><span data-ttu-id="afc3c-245">Sortie</span><span class="sxs-lookup"><span data-stu-id="afc3c-245">Output</span></span>

<span data-ttu-id="afc3c-246">Le rapport inclut toujours la sortie suivante :</span><span class="sxs-lookup"><span data-stu-id="afc3c-246">The report will always include the following output:</span></span>

  - <span data-ttu-id="afc3c-247">N premières salles de conversation actives par nombre de publications de messages pour la période sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="afc3c-247">Top n most active chat rooms by number of message posts for selected period.</span></span>

  - <span data-ttu-id="afc3c-248">N premiers utilisateurs actifs par nombre de billets de messages pour la période sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="afc3c-248">Top n most active users by number of message posts for selected period.</span></span>

  - <span data-ttu-id="afc3c-249">Top n des salles de conversation actives par nombre de publications de messages pour la période sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="afc3c-249">Top n least active chat rooms by number of message posts for selected period.</span></span>

  - <span data-ttu-id="afc3c-250">Des salles de conversation inactives pour toute la durée de vie de la base de données ou depuis la date spécifiée.</span><span class="sxs-lookup"><span data-stu-id="afc3c-250">Chat rooms that are inactive for the entire life of the database, or since the specified date.</span></span>

  - <span data-ttu-id="afc3c-251">Tendance quotidienne de publication des messages pour la période sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="afc3c-251">Daily message post trend for selected period.</span></span>

  - <span data-ttu-id="afc3c-252">Tendance hebdomadaire des publications de messages pour la période sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="afc3c-252">Weekly message post trend for selected period.</span></span>

  - <span data-ttu-id="afc3c-253">Tendance mensuelle des publications de messages pour la période sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="afc3c-253">Monthly message post trend for selected period.</span></span>

  - <span data-ttu-id="afc3c-254">Nombre total de publications de messages pour la période sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="afc3c-254">Total message posts for selected period.</span></span>

  - <span data-ttu-id="afc3c-255">Nombre total d’espaces activés.</span><span class="sxs-lookup"><span data-stu-id="afc3c-255">Total number of enabled rooms.</span></span>

</div>

<div>

## <a name="example"></a><span data-ttu-id="afc3c-256">Exemple</span><span class="sxs-lookup"><span data-stu-id="afc3c-256">Example</span></span>

<span data-ttu-id="afc3c-257">L’exemple suivant génère un rapport sur l’utilisation de la 2001 entière et place le rapport dans le OutputFolder spécifié dans le ChatUsageReport.exe.config.</span><span class="sxs-lookup"><span data-stu-id="afc3c-257">The following example generates a usage report for the entire year 2001 and places the report in the OutputFolder specified in the ChatUsageReport.exe.config.</span></span>

```Powershell
    ChatUsageReport -RoomsInactiveSince 06-20-2010
```
<span data-ttu-id="afc3c-258">ChatUsageReport.exe.config :</span><span class="sxs-lookup"><span data-stu-id="afc3c-258">ChatUsageReport.exe.config:</span></span>

```XML
    <?xml version="1.0" encoding="utf-8" ?>
    <configuration>
      <connectionStrings>
        <!-- The PersistentChat connection string must be defined in this file. -->
        <add name="PersistentChat" connectionString="Data Source=contoso.com\RTC;Initial Catalog=mgc;Integrated Security=SSPI"/>
      </connectionStrings>
      <appSettings>
        <!-- The OutputFolder must be defined here or on the command line. -->
        <add key="OutputFolder" value="."/>
        <!-- The values below are the same as the application defaults. -->
        <add key="StartDate" value="01/01/0001"/>
        <add key="EndDate" value="12/31/9999"/>
        <add key="TopActiveUsers" value="10"/>
        <add key="TopActiveRooms" value="10"/>
        <add key="LeastActiveRooms" value="10"/>
        <add key="RoomsInactiveSince" value="01/01/0001"/>
      </appSettings>
    </configuration></configuration>
```
</div>

</div>

<div>

## <a name="scheduleadsyncforprincipal"></a><span data-ttu-id="afc3c-259">ScheduleADSyncForPrincipal</span><span class="sxs-lookup"><span data-stu-id="afc3c-259">ScheduleADSyncForPrincipal</span></span>

<div>

## <a name="description"></a><span data-ttu-id="afc3c-260">Description</span><span class="sxs-lookup"><span data-stu-id="afc3c-260">Description</span></span>

<span data-ttu-id="afc3c-261">ScheduleADSyncForPrincipal est un script Microsoft SQL Server 2012 qui doit être exécuté directement depuis SQL Server Management Studio lorsqu’il est connecté à la base de données principale de conversation permanente.</span><span class="sxs-lookup"><span data-stu-id="afc3c-261">ScheduleADSyncForPrincipal is a Microsoft SQL Server 2012 script that must be run directly from within SQL Server Management Studio when connected to the Persistent Chat back-end database.</span></span> <span data-ttu-id="afc3c-262">Ce script vous permet de forcer une conversation permanente à synchroniser ses enregistrements d’un utilisateur avec des services de domaine Active Directory, plutôt que d’attendre la durée de la synchronisation planifiée.</span><span class="sxs-lookup"><span data-stu-id="afc3c-262">This script enables you to force Persistent Chat to synchronize its records of a user with those of Active Directory Domain Services, rather than waiting for the scheduled synchronization time.</span></span>

</div>

<div>

## <a name="requirements"></a><span data-ttu-id="afc3c-263">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="afc3c-263">Requirements</span></span>

<span data-ttu-id="afc3c-264">Le compte d’utilisateur sous lequel le script est exécuté doit avoir accès au propriétaire de la base de données principale de conversation permanente.</span><span class="sxs-lookup"><span data-stu-id="afc3c-264">The user account under which the script is run must have owner access to the Persistent Chat back-end database.</span></span>

</div>

<div>

## <a name="usage"></a><span data-ttu-id="afc3c-265">Utilisation</span><span class="sxs-lookup"><span data-stu-id="afc3c-265">Usage</span></span>

<span data-ttu-id="afc3c-266">Le contenu du script par défaut est le suivant :</span><span class="sxs-lookup"><span data-stu-id="afc3c-266">Following are the contents of the default script:</span></span>

```Powershell
    /*
    This script will schedule a principal for a forced AD synchronization cycle
    
    If you're using Sql Server Management Studio, pressing Ctrl+Shift+M will 
    allow you to specify values for the template parameter.
    */
    
        insert into
          tblPrincipalMeta
          (
           prinID
          ,prinAffiliationsDirty
          ,prinAttributesDirty
          ,prinDeleted
          )
          select
            prinID
           ,1
           ,1
           ,0
          from
            tblPrincipal
          where
            prinID not in (select prinID from tblPrincipalMeta) and
            prinID = <PrinID,int,0>
     
        update
          tblPrincipalMeta
        set
          prinAffiliationsDirty = 1
         ,prinAttributesDirty = 1
         ,tryCount = 0
         ,nextTry = null
        where
         prinID = <PrinID,int,0>
```

<span data-ttu-id="afc3c-267"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="afc3c-267"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

