---
title: 'Lync Server 2013 : utilisation de Microsoft SQL Server 2008 R2 en tant que base de données System Center Operations Manager'
description: 'Lync Server 2013 : utilisation de Microsoft SQL Server 2008 R2 en tant que base de données System Center Operations Manager.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Using Microsoft SQL Server 2008 R2 as your System Center Operations Manager database
ms:assetid: 0efe76da-8854-499e-bdc7-3623244a8e85
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687969(v=OCS.15)
ms:contentKeyID: 49733555
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 870c079e7e5e871fc62358e9bdd21653193fad7c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394813"
---
# <a name="using-microsoft-sql-server-2008-r2-as-your-system-center-operations-manager-database-for-lync-server-2013"></a><span data-ttu-id="ce622-103">Utilisation de Microsoft SQL Server 2008 R2 en tant que base de données Gestionnaire d’opérations System Center pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ce622-103">Using Microsoft SQL Server 2008 R2 as your System Center Operations Manager database for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ce622-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ce622-104">

<span> </span></span></span>

<span data-ttu-id="ce622-105">_**Dernière modification de la rubrique :** 2013-07-29_</span><span class="sxs-lookup"><span data-stu-id="ce622-105">_**Topic Last Modified:** 2013-07-29_</span></span>

<span data-ttu-id="ce622-106">Pour utiliser SQL Server 2008 R2 en tant que base de données principale, suivez les étapes décrites dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="ce622-106">To use SQL Server 2008 R2 as your back-end database, complete the steps detailed in this topic.</span></span>

<div>

## <a name="configuring-sql-server-2008-r2-and-sql-server-reporting-services"></a><span data-ttu-id="ce622-107">Configuration de SQL Server 2008 R2 et SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="ce622-107">Configuring SQL Server 2008 R2 and SQL Server Reporting Services</span></span>

<span data-ttu-id="ce622-108">Avant de commencer à installer System Center Operations Manager, vous devez apporter deux modifications à SQL Server 2008 R2 et à votre configuration SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="ce622-108">Before you begin installing System Center Operations Manager you must make two changes to your SQL Server 2008 R2 and your SQL Server Reporting Services configuration.</span></span> <span data-ttu-id="ce622-109">(Ces modifications sont requises uniquement si vous utilisez SQL Server 2008 R2 en tant que base de données Operations Manager.) Tout d’abord, procédez comme suit sur l’ordinateur qui héberge votre base de données Operations Manager :</span><span class="sxs-lookup"><span data-stu-id="ce622-109">(These changes are required only if you are using SQL Server 2008 R2 as your Operations Manager database.) First, do the following on the computer that will host your Operations Manager database:</span></span>

1.  <span data-ttu-id="ce622-110">Cliquez sur **Démarrer** , puis sur **exécuter**.</span><span class="sxs-lookup"><span data-stu-id="ce622-110">Click **Start** and then click **Run**.</span></span>

2.  <span data-ttu-id="ce622-111">Dans la boîte de dialogue **exécuter** , tapez **C : \\ Program Files \\ Microsoft SQL Server \\ MSRS10 \_ 50. ARCHINST \\ Reporting Services \\ reportserver** , puis appuyez sur entrée.</span><span class="sxs-lookup"><span data-stu-id="ce622-111">In the **Run** dialog box, type **C:\\Program Files\\Microsoft SQL Server\\ MSRS10\_50.ARCHINST\\Reporting Services\\ReportServer** and then press ENTER.</span></span>

3.  <span data-ttu-id="ce622-112">Dans le dossier **reportserver** , ouvrez le fichier **rsreportserver.config** dans bloc-notes ou dans un autre éditeur de texte.</span><span class="sxs-lookup"><span data-stu-id="ce622-112">In the **ReportServer** folder, open the file **rsreportserver.config** in Notepad or any other text editor.</span></span>

4.  <span data-ttu-id="ce622-113">Au début du fichier, vous verrez une série de nœuds « ajouter une touche ».</span><span class="sxs-lookup"><span data-stu-id="ce622-113">Near the beginning of the file you will see a series of "Add Key" nodes.</span></span> <span data-ttu-id="ce622-114">Recherchez l’entrée commençant par **\< Ajouter Key = « SecureConnectionLevel »** et définissez la valeur sur **0**:</span><span class="sxs-lookup"><span data-stu-id="ce622-114">Find the entry that begins **\<Add Key="SecureConnectionLevel"** and set the value to **0**:</span></span>
    
        <Add Key="SecureConnectionLevel" Value="0"/>

5.  <span data-ttu-id="ce622-115">Enregistrez le fichier **rsreportserver.config** puis fermez votre éditeur de texte.</span><span class="sxs-lookup"><span data-stu-id="ce622-115">Save the file **rsreportserver.config** and then close your text editor.</span></span>

<span data-ttu-id="ce622-116">Après avoir effectué la mise à jour du fichier de configuration du serveur de rapports, vous devez affecter le certificat approprié à SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="ce622-116">After updating the Report Server configuration file you must then assign the correct certificate to SQL Server Reporting Services.</span></span> <span data-ttu-id="ce622-117">Pour cela, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="ce622-117">To do that:</span></span>

1.  <span data-ttu-id="ce622-118">Cliquez sur **Démarrer**, **sur tous les programmes**, sur **Microsoft SQL Server 2008 R2**, sur **outils de configuration**, puis sur gestionnaire de **configuration Reporting Services**.</span><span class="sxs-lookup"><span data-stu-id="ce622-118">Click **Start**, click **All Programs**, click **Microsoft SQL Server 2008 R2**, click **Configuration Tools**, and then click **Reporting Services Configuration Manager**.</span></span>

2.  <span data-ttu-id="ce622-119">Dans la boîte de dialogue **connexion de configuration de Reporting Services** , assurez-vous que le nom de votre serveur apparaît dans la zone **nom du serveur** .</span><span class="sxs-lookup"><span data-stu-id="ce622-119">In the **Reporting Services Configuration Connection** dialog box, make sure that the name of your server appears in the **Server Name** box.</span></span> <span data-ttu-id="ce622-120">Sélectionnez l’instance de SQL Server qui héberge votre base de données Operations Manager (par exemple, **ARCHINST**) dans la liste déroulante de l' **instance Report Server** , puis cliquez sur **se connecter**.</span><span class="sxs-lookup"><span data-stu-id="ce622-120">Select the SQL Server instance that will host your Operations Manager database (for example, **ARCHINST**) from the **Report Server Instance** drop-down list and then click **Connect**.</span></span>

3.  <span data-ttu-id="ce622-121">Dans le gestionnaire de configuration Reporting Services, cliquez sur **URL du service Web**.</span><span class="sxs-lookup"><span data-stu-id="ce622-121">In Reporting Services Configuration Manager, click **Web Service URL**.</span></span>

4.  <span data-ttu-id="ce622-122">Dans la page **URL du service Web** , sélectionnez le certificat à utiliser pour la création de rapports services dans la liste déroulante **certificat SSL** , puis cliquez sur **appliquer**.</span><span class="sxs-lookup"><span data-stu-id="ce622-122">On the **Web Service URL** page, select the certificate to be used for your Reporting Services from the **SSL Certificate** dropdown list and then click **Apply**.</span></span> <span data-ttu-id="ce622-123">Après quelques secondes, une paire d’URL est affichée sous **URL du service Web de Report Server**.</span><span class="sxs-lookup"><span data-stu-id="ce622-123">After a few seconds, you will see a pair of URLs listed under **Report Server Web Service URLs**.</span></span>

5.  <span data-ttu-id="ce622-124">Cliquez sur les deux URL pour vérifier que vous pouvez accéder à SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="ce622-124">Click both of the URLs to verify that you can access SQL Server Reporting Services.</span></span>

6.  <span data-ttu-id="ce622-125">Fermez le gestionnaire de configuration de report services.</span><span class="sxs-lookup"><span data-stu-id="ce622-125">Close Reporting Services Configuration Manager.</span></span>

</div>

<div>

## <a name="creating-a-system-center-operations-manager-database-for-use-with-sql-server-2008-r2"></a><span data-ttu-id="ce622-126">Création d’une base de données System Center Operations Manager à utiliser avec SQL Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ce622-126">Creating a System Center Operations Manager database for use with SQL Server 2008 R2</span></span>

<span data-ttu-id="ce622-127">Si vous voulez configurer System Center Operations Manager de façon à utiliser une base de données SQL Server 2008 R2, vous devez « manuellement » créer la base de données Operations Manager sur l’ordinateur exécutant SQL Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="ce622-127">If you want to configure System Center Operations Manager to use a SQL Server 2008 R2 database, you will need to "manually" create the Operations Manager database on the computer running SQL Server 2008 R2.</span></span> <span data-ttu-id="ce622-128">(De nouveau, cette procédure n’est pas nécessaire si vous utilisez SQL Server 2005 ou SQL Server 2008 comme base de données principale.)</span><span class="sxs-lookup"><span data-stu-id="ce622-128">(Again, these steps are not required if you are using SQL Server 2005 or SQL Server 2008 as your back-end database.)</span></span>

<span data-ttu-id="ce622-129">Pour créer manuellement une base de données Operations Manager, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="ce622-129">To manually create an Operations Manager database do the following:</span></span>

1.  <span data-ttu-id="ce622-130">Sur le média de configuration de System Center Operations Manager 2007 R2, dans le \\ dossier amd64 de SupportTools, double-cliquez sur **DBCreateWizard.exe**.</span><span class="sxs-lookup"><span data-stu-id="ce622-130">On the System Center Operations Manager 2007 R2 setup media, in the SupportTools\\AMD64 folder, double-click **DBCreateWizard.exe**.</span></span>

2.  <span data-ttu-id="ce622-131">Dans l’Assistant Configuration de la base de données, dans la page **Bienvenue dans l’Assistant Configuration de la base de données** , cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="ce622-131">In the Database Configuration Wizard, on the **Welcome to the Database Configuration Wizard** page, click **Next**.</span></span>

3.  <span data-ttu-id="ce622-132">Dans la page **informations de la base de données** , conservez tous les paramètres, puis cliquez sur **suivant** .</span><span class="sxs-lookup"><span data-stu-id="ce622-132">On the **Database Information** page leave all the settings as-is and then click **Next**</span></span>

4.  <span data-ttu-id="ce622-133">Dans la **page Configuration du groupe de gestion** , tapez un nom pour votre groupe d’administration (par exemple, analyse du **serveur Lync**) dans la zone **nom du groupe de gestion** , puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="ce622-133">On the **Management Group Configuration** page type a name for your Management Group (for example, **Lync Server Monitoring**) in the **Management Group name** box and then click **Next**.</span></span>

5.  <span data-ttu-id="ce622-134">Dans la page **rapports d’erreurs Operations Manager** , cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="ce622-134">On the **Operations Manager Error Reports** page click **Next**.</span></span>

6.  <span data-ttu-id="ce622-135">Dans la page **Résumé** , cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="ce622-135">On the **Summary** page click **Finish**.</span></span>

</div>

<div>

## <a name="creating-a-system-center-operations-manager-data-warehouse-for-use-with-sql-server-2008-r2"></a><span data-ttu-id="ce622-136">Création d’un entrepôt de données System Center Operations Manager à utiliser avec SQL Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ce622-136">Creating a System Center Operations Manager data warehouse for use with SQL Server 2008 R2</span></span>

<span data-ttu-id="ce622-137">Microsoft Lync Server 2013 est fourni avec trois nouveaux rapports System Center Operations Manager :</span><span class="sxs-lookup"><span data-stu-id="ce622-137">Microsoft Lync Server 2013 ships with three new System Center Operations Manager reports:</span></span>

  - <span data-ttu-id="ce622-138">**Rapport de disponibilité des scénarios de fin à fin**   Ce rapport détaille la disponibilité et la durée de fonctionnement des services clés de Lync Server tels que l’inscription ou la présence.</span><span class="sxs-lookup"><span data-stu-id="ce622-138">**End to End Scenario Availability Report**   This report details the availability/uptime for key Lync Server services such as registration or presence.</span></span>

  - <span data-ttu-id="ce622-139">**Rapport de capacité**   À l’aide des informations des compteurs de performance, ce rapport affiche des tendances pour les composants système, tels que la disponibilité de la mémoire et l’utilisation du processeur.</span><span class="sxs-lookup"><span data-stu-id="ce622-139">**Capacity Report**   Using performance counter information, this report shows trends for system components such as memory availability and processor usage.</span></span>

  - <span data-ttu-id="ce622-140">**Rapport de composant**   Ce rapport répertorie les principaux générateurs d’alertes regroupés par composant Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ce622-140">**Component Report**   This report lists the top alert generators grouped by Lync Server component.</span></span>

<span data-ttu-id="ce622-141">Pour pouvoir utiliser ces nouveaux rapports, vous devez installer un Data Warehouse System Center Operations Manager.</span><span class="sxs-lookup"><span data-stu-id="ce622-141">In order to use these new reports you must install a System Center Operations Manager data warehouse.</span></span> <span data-ttu-id="ce622-142">(Un entrepôt de données fournit un espace de stockage de données opérationnelles longue durée.) Pour utiliser un entrepôt de données avec SQL Server 2008 R2, vous devez effectuer les étapes suivantes sur l’ordinateur qui héberge votre base de données SQL Server :</span><span class="sxs-lookup"><span data-stu-id="ce622-142">(A data warehouse provides for long-term storage of operations data.) To use a data warehouse with SQL Server 2008 R2 you must carry out the following steps on the computer that hosts your SQL Server database:</span></span>

1.  <span data-ttu-id="ce622-143">Sur le média de configuration de System Center Operations Manager, dans le \\ dossier SupportTools de configuration \\ , double-cliquez sur **DBCreateWizard.exe**.</span><span class="sxs-lookup"><span data-stu-id="ce622-143">On the System Center Operations Manager setup media, in the Setup\\SupportTools\\AMD64 folder, double-click **DBCreateWizard.exe**.</span></span>

2.  <span data-ttu-id="ce622-144">Dans l’Assistant Configuration de la base de données, dans la page **Bienvenue dans l’Assistant Configuration de la base de données** , cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="ce622-144">In the Database Configuration Wizard, on the **Welcome to the Database Configuration Wizard** page, click **Next**.</span></span>

3.  <span data-ttu-id="ce622-145">Dans la page **informations de la base de** données, sélectionnez **base de données du Data Warehouse Operations Manager** dans la liste déroulante **type de base de données** , puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="ce622-145">On the **Database Information** page, select **Operations Manager Data Warehouse Database** from the **Database Type** dropdown list and then click **Next**.</span></span>

4.  <span data-ttu-id="ce622-146">Dans la page **Résumé** , cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="ce622-146">On the **Summary** page click **Finish**.</span></span>

</div>

<div>

## <a name="installing-the-system-center-operations-manager-console"></a><span data-ttu-id="ce622-147">Installation de la console System Center Operations Manager</span><span class="sxs-lookup"><span data-stu-id="ce622-147">Installing the System Center Operations Manager console</span></span>

<span data-ttu-id="ce622-148">La console Operations Manager est l’outil principal utilisé pour gérer System Center Operations Manager.</span><span class="sxs-lookup"><span data-stu-id="ce622-148">The Operations Manager console is the primary tool used to manage System Center Operations Manager.</span></span> <span data-ttu-id="ce622-149">Avant d’installer la console Operations Manager, assurez-vous d’avoir installé une version prise en charge de SQL Server, ainsi que le service SQL Server Reporting.</span><span class="sxs-lookup"><span data-stu-id="ce622-149">Before you install the Operations Manager console, make sure that you have installed a supported version of SQL Server along with the SQL Server Reporting Service.</span></span> <span data-ttu-id="ce622-150">Il est également recommandé d’exécuter le gestionnaire de configuration Reporting Services de SQL Server pour vérifier que le service de création de rapports est correctement installé et configuré.</span><span class="sxs-lookup"><span data-stu-id="ce622-150">It is also recommended that you run SQL Server's Reporting Services Configuration Manager to verify that the Reporting Service has been correctly installed and configured.</span></span>

<span data-ttu-id="ce622-151">Pour installer la console System Center Operations Manager, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="ce622-151">To install the System Center Operations Manager console:</span></span>

1.  <span data-ttu-id="ce622-152">Sur le média de configuration de System Center Operations Manager, double-cliquez sur **SetupOM.exe**.</span><span class="sxs-lookup"><span data-stu-id="ce622-152">On the System Center Operations Manager setup media, double-click **SetupOM.exe**.</span></span>

2.  <span data-ttu-id="ce622-153">Dans le programme d’installation de System Center Operations Manager 2007 R2, cliquez sur **vérifier les conditions préalables**.</span><span class="sxs-lookup"><span data-stu-id="ce622-153">In System Center Operations Manager 2007 R2 Setup, click **Check Prerequisites**.</span></span>

3.  <span data-ttu-id="ce622-154">Dans la visionneuse de logiciels de System Center Operations Manager, sélectionnez les composants System Center à installer : (**serveur**; **Console**; et **PowerShell**), puis cliquez sur **vérifier**.</span><span class="sxs-lookup"><span data-stu-id="ce622-154">In the System Center Operations Manager Prerequisite Viewer, select the System Center components to be installed: (**Server**; **Console**; and **PowerShell**) and then click **Check**.</span></span> <span data-ttu-id="ce622-155">Vérifiez qu’aucun problème de blocage n’a été signalé, puis cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="ce622-155">Verify that no blocking issues have been reported and then click **Close**.</span></span> <span data-ttu-id="ce622-156">Si un problème de blocage a été signalé, corrigez le problème, puis cliquez sur **vérifier** pour réexécuter les tests préalables.</span><span class="sxs-lookup"><span data-stu-id="ce622-156">If a blocking issue has been reported, correct the problem and then click **Check** to re-run the prerequisite testing.</span></span>

4.  <span data-ttu-id="ce622-157">Dans le programme d’installation de System Center Operations Manager, cliquez sur **installer Operations Manager**.</span><span class="sxs-lookup"><span data-stu-id="ce622-157">In System Center Operations Manager Setup, click **Install Operations Manager**.</span></span>

5.  <span data-ttu-id="ce622-158">Dans l’Assistant Configuration de System Center Operations Manager, dans la page Bienvenue dans l' **Assistant Configuration de System Center Operations Manager** , cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="ce622-158">In the System Center Operations Manager Setup wizard, on the **Welcome to the System Center Operations Manager Setup Wizard** page, click **Next**.</span></span>

6.  <span data-ttu-id="ce622-159">Sur la page **contrat de licence utilisateur final** , sélectionnez **J’accepte les conditions du contrat de licence** , puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="ce622-159">On the **End-User License Agreement** page, select **I accept the terms in the license agreement** and then click **Next**.</span></span>

7.  <span data-ttu-id="ce622-160">Sur la page **inscription de produit** , tapez votre nom dans la zone nom d' **utilisateur** et le nom de votre organisation dans la zone **organisation** .</span><span class="sxs-lookup"><span data-stu-id="ce622-160">On the **Product Registration** page, type your name in the **User Name** box and name of your organization in the **Organization** box.</span></span> <span data-ttu-id="ce622-161">Tapez votre clé de produit System Center Operations Manager dans la zone **Entrez votre clé** de produit à 25 chiffres, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="ce622-161">Type your System Center Operations Manager product key in the **Enter your 25 digit CD Key** box and then click **Next**.</span></span>

8.  <span data-ttu-id="ce622-162">Dans la page **configuration personnalisée** , sélectionnez les options du centre de systèmes à installer, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="ce622-162">On the **Custom Setup** page select the System Center options to be installed and then click **Next**.</span></span> <span data-ttu-id="ce622-163">Sélectionnez serveur de **gestion**, **interfaces utilisateur** et **console Web** à installer.</span><span class="sxs-lookup"><span data-stu-id="ce622-163">You should select **Management Server**, **User Interfaces**, and **Web Console** to be installed.</span></span> <span data-ttu-id="ce622-164">La **base de données** ne doit pas être sélectionnée et ne peut pas être installée.</span><span class="sxs-lookup"><span data-stu-id="ce622-164">**Database** should not be selected and should not be installed.</span></span>

9.  <span data-ttu-id="ce622-165">Dans la page d' **instance du serveur de base de données SC** , vérifiez que le nom de l’ordinateur sur lequel les bases de données du gestionnaire d’opérations sont installées apparaît dans la zone **serveur de base de données System Center** .</span><span class="sxs-lookup"><span data-stu-id="ce622-165">On the **SC Database Server Instance** page, verify that the name of the computer where the Operations Manager databases are installed appears in the **System Center Database Server** box.</span></span> <span data-ttu-id="ce622-166">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="ce622-166">Click **Next**.</span></span>

10. <span data-ttu-id="ce622-167">Sur la **page compte d’action du serveur de gestion** , sélectionnez **domaine ou compte d’ordinateur local** , puis entrez les valeurs appropriées dans les zones **compte d’utilisateur**, **mot de passe** et **domaine ou ordinateur local** .</span><span class="sxs-lookup"><span data-stu-id="ce622-167">On the **Management Server Action Account** page, select **Domain or Local Computer Account** and then enter the appropriate values in the **User Account**, **Password**, and **Domain or local computer** boxes.</span></span> <span data-ttu-id="ce622-168">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="ce622-168">Click **Next**.</span></span>

11. <span data-ttu-id="ce622-169">Sur la page du **compte de service SDK et de configuration** , sélectionnez **domaine ou compte d’ordinateur local** , puis entrez les valeurs appropriées dans les zones **compte d’utilisateur**, **mot de passe** et **domaine ou ordinateur local** .</span><span class="sxs-lookup"><span data-stu-id="ce622-169">On the **SDK and Config Service Account** page, select **Domain or Local Computer Account** and then enter the appropriate values in the **User Account**, **Password**, and **Domain or local computer** boxes.</span></span> <span data-ttu-id="ce622-170">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="ce622-170">Click **Next**.</span></span>

12. <span data-ttu-id="ce622-171">Dans la page **rapports d’erreurs Operations Manager** , cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="ce622-171">On the **Operations Manager Error Reports** page click **Next**.</span></span>

13. <span data-ttu-id="ce622-172">Sur la page du **programme d’amélioration** du produit, cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="ce622-172">On the **Customer Experience Improvement Program** page click **Next**.</span></span>

14. <span data-ttu-id="ce622-173">Dans la page êtes-vous **prêt à installer le programme** , cliquez sur **installer**.</span><span class="sxs-lookup"><span data-stu-id="ce622-173">On the **Ready to Install the Program** page, click **Install**.</span></span>

15. <span data-ttu-id="ce622-174">Dans la page **fin de la procédure de configuration de System Center Operations Manager** , désactivez la **clé de chiffrement de sauvegarde** et **Démarrez les cases à cocher** de la console, puis cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="ce622-174">On the **Completing the System Center Operations Manager Setup** page, clear the **Backup Encryption Key** and **Start the console checkboxes** and then click **Finish**.</span></span>

16. <span data-ttu-id="ce622-175">Dans le programme d’installation de System Center Operations Manager, cliquez sur **quitter**.</span><span class="sxs-lookup"><span data-stu-id="ce622-175">In System Center Operations Manager Setup click **Exit**.</span></span>

</div>

<div>

## <a name="installing-system-center-reporting-services"></a><span data-ttu-id="ce622-176">Installation de System Center Reporting Services</span><span class="sxs-lookup"><span data-stu-id="ce622-176">Installing System Center Reporting Services</span></span>

<span data-ttu-id="ce622-177">Après l’installation et la configuration de la console System Center Operations Manager, vous devez installer System Center Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="ce622-177">After installing and configuring the System Center Operations Manager console you must then install System Center Reporting Services.</span></span> <span data-ttu-id="ce622-178">Si vous utilisez SQL Server 2008 R2 comme base de données principale Operations Manager, cela signifie que vous devez tout d’abord apporter un changement temporaire au groupe de sécurité associé à SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="ce622-178">If you are using SQL Server 2008 R2 as your Operations Manager back-end database, that means that you must first make a temporary change to the security group associated with SQL Server Reporting Services.</span></span> <span data-ttu-id="ce622-179">Si vous utilisez SQL Server 2008 R2, vous devez effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="ce622-179">If you are using SQL Server 2008 R2, you must do the following:</span></span>

1.  <span data-ttu-id="ce622-180">Cliquez sur **Démarrer**, pointez sur **Outils d’administration**, puis cliquez sur **Gestionnaire de serveur**.</span><span class="sxs-lookup"><span data-stu-id="ce622-180">Click **Start**, point to **Administrative Tools**, and then click **Server Manager**.</span></span>

2.  <span data-ttu-id="ce622-181">Dans le gestionnaire de serveur, développez **configuration**, **utilisateurs et groupes locaux**, puis cliquez sur **groupes**.</span><span class="sxs-lookup"><span data-stu-id="ce622-181">In Server Manager, expand **Configuration**, expand **Local Users and Groups**, and then click **Groups**.</span></span>

3.  <span data-ttu-id="ce622-182">Recherchez le groupe suivant, dans lequel ATL-SC-001 représente le nom de votre ordinateur et ARCHINST représente l’instance SQL Server de la base de données du centre de données : **SQLServerReportServerUser $ ATL-SC-001 $ MSRS10 \_ 50. ARCHINST**.</span><span class="sxs-lookup"><span data-stu-id="ce622-182">Locate the following group, where atl-sc-001 represents the name of your computer and ARCHINST represents the SQL Server instance for the System Center database: **SQLServerReportServerUser$atl-sc-001$MSRS10\_50.ARCHINST**.</span></span>

4.  <span data-ttu-id="ce622-183">Cliquez avec le bouton droit sur le groupe, puis cliquez sur **Renommer**.</span><span class="sxs-lookup"><span data-stu-id="ce622-183">Right-click the group and then click **Rename**.</span></span> <span data-ttu-id="ce622-184">Renommez le groupe en supprimant **\_ 50** du nom du groupe.</span><span class="sxs-lookup"><span data-stu-id="ce622-184">Rename the group by deleting **\_50** from the group name.</span></span> <span data-ttu-id="ce622-185">Par exemple : **SQLServerReportServerUser $ ATL-SC-001 $ MSRS10. ARCHINST**.</span><span class="sxs-lookup"><span data-stu-id="ce622-185">For example: **SQLServerReportServerUser$atl-sc-001$MSRS10.ARCHINST**.</span></span>

5.  <span data-ttu-id="ce622-186">Fermez le gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="ce622-186">Close Server Manager.</span></span>

<span data-ttu-id="ce622-187">À ce stade, vous êtes prêt à installer System Center Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="ce622-187">At this point you are ready to install System Center Reporting Services.</span></span> <span data-ttu-id="ce622-188">Pour ce faire :</span><span class="sxs-lookup"><span data-stu-id="ce622-188">To do this:</span></span>

1.  <span data-ttu-id="ce622-189">Sur le média de configuration de System Center Operations Manager 2007 R2, double-cliquez sur **SetupOM.exe**.</span><span class="sxs-lookup"><span data-stu-id="ce622-189">On the System Center Operations Manager 2007 R2 Setup media, double-click **SetupOM.exe**.</span></span>

2.  <span data-ttu-id="ce622-190">Dans System Center Operations Manager 2007 R2, cliquez sur **installer le rapport Operations Manager**.</span><span class="sxs-lookup"><span data-stu-id="ce622-190">In System Center Operations Manager 2007 R2 Setup, click **Install Operations Manager Reporting**.</span></span>

3.  <span data-ttu-id="ce622-191">Dans l’Assistant Configuration de création de rapports de System Center Operations Manager 2007 R2, dans la page Bienvenue dans le **programme d’installation de création de rapports Operations Manager** , cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="ce622-191">In the System Center Operations Manager 2007 R2 Reporting Setup wizard, on the **Welcome to Operations Manager Reporting Setup** page, click **Next**.</span></span>

4.  <span data-ttu-id="ce622-192">Dans la page **contrat de licence utilisateur final** , sélectionnez **J’accepte les conditions du contrat de licence** , puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="ce622-192">On the **End-user License Agreement** page select **I accept the terms of the license agreement** and then click **Next**.</span></span>

5.  <span data-ttu-id="ce622-193">Sur la page **inscription de produit** , assurez-vous que votre nom et le nom de votre organisation apparaissent dans les zones nom d' **utilisateur** et **organisation** , puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="ce622-193">On the **Product Registration** page, ensure that your name and the name of your organization appear in the **User Name** and **Organization** boxes and then click **Next**.</span></span>

6.  <span data-ttu-id="ce622-194">Dans la page **configuration personnalisée** , cliquez sur **serveur de création de rapports** , sélectionnez **ce composant, et tous les composants dépendants, seront installés sur le lecteur de disque local**.</span><span class="sxs-lookup"><span data-stu-id="ce622-194">On the **Custom Setup** page, click **Reporting Server** and select **This component, and all dependent components, will be installed on local disk drive**.</span></span> <span data-ttu-id="ce622-195">Cliquez sur **entrepôt de données** et sélectionnez **ce composant ne sera pas disponible**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="ce622-195">Click **Data Warehouse** and select **This component will not be available**, and then click **Next**.</span></span>

7.  <span data-ttu-id="ce622-196">Dans la page **connexion à un serveur de gestion racine** , tapez le nom de votre serveur de gestion de la racine Operations Manager dans la zone **serveur de gestion racine** , puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="ce622-196">On the **Connect to the Root Management Server** page, type the name of your Operations Manager root management server in the **Root Management Server** box and then click **Next**.</span></span>

8.  <span data-ttu-id="ce622-197">Dans la page **se connecter à l’entrepôt de données Operations Manager** , entrez l’instance SQL Server dans laquelle se trouve votre entrepôt de données dans la zone **instance SQL Server** .</span><span class="sxs-lookup"><span data-stu-id="ce622-197">On the **Connect to the Operations Manager Data Warehouse** page, type the SQL Server instance where your data warehouse is located in the **SQL Server Instance** box.</span></span> <span data-ttu-id="ce622-198">(Si votre entrepôt de données se trouve dans l’instance par défaut, tapez simplement le nom du serveur, par exemple : ATL-SQL-001.) Vérifiez que le nom de la base de données **OperationsManagerDW** s’affiche dans la zone **nom** et que le port **1433** s’affiche dans la zone **port SQL Server** .</span><span class="sxs-lookup"><span data-stu-id="ce622-198">(If your data warehouse is located in the Default instance then simply type the server name; for example: atl-sql-001.) Verify that the database name **OperationsManagerDW** appears in the **Name** box, and that port **1433** appears in the **SQL Server port** box.</span></span> <span data-ttu-id="ce622-199">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="ce622-199">Click **Next**.</span></span>

9.  <span data-ttu-id="ce622-200">Dans la page d' **instance SQL Server Report** , sélectionnez votre serveur SQL Server Reporting dans la liste déroulante **Enter SQL Server Reporting Services** , puis cliquez sur **Next (suivant**).</span><span class="sxs-lookup"><span data-stu-id="ce622-200">On the **SQL Server Reporting Instance** page, select your SQL Server reporting server from the **Enter the SQL Server Reporting Services Server** dropdown list and then click **Next**.</span></span>

10. <span data-ttu-id="ce622-201">Sur la page **compte d’écriture du magasin de données** , entrez le nom et le mot de passe de l’utilisateur auquel vous souhaitez attribuer des autorisations d’écriture dans l’entrepôt de données dans les zones compte d' **utilisateur** et **mot de passe** .</span><span class="sxs-lookup"><span data-stu-id="ce622-201">On the **Data Warehouse Write Account** page, enter the name and password of the user to be initially assigned write permissions to the data warehouse in the **User Account** and **Password** boxes.</span></span> <span data-ttu-id="ce622-202">Sélectionnez le domaine de l’utilisateur dans la liste déroulante **Domain** , puis cliquez sur **Next (suivant**).</span><span class="sxs-lookup"><span data-stu-id="ce622-202">Select the user's domain from the **Domain** dropdown list and then click **Next**.</span></span>

11. <span data-ttu-id="ce622-203">Sur la page **compte du lecteur de données** , entrez le nom et le mot de passe du compte d’utilisateur à utiliser lorsque SQL Reporting Services interroge l’entrepôt de données dans les zones compte d' **utilisateur** et **mot de passe** .</span><span class="sxs-lookup"><span data-stu-id="ce622-203">On the **Data Reader Account** page, enter the name and password of the user account to be used when SQL Reporting Services queries the data warehouse in the **User Account** and **Password** boxes.</span></span> <span data-ttu-id="ce622-204">Sélectionnez le domaine de compte dans la liste déroulante **Domain** , puis cliquez sur **Next (suivant**).</span><span class="sxs-lookup"><span data-stu-id="ce622-204">Select the account domain from the **Domain** dropdown list and then click **Next**.</span></span>

12. <span data-ttu-id="ce622-205">Dans la page **rapports de données opérationnelles** , cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="ce622-205">On the **Operational Data Reports** page, click **Next**.</span></span>

13. <span data-ttu-id="ce622-206">Sur la page **Microsoft Update** , cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="ce622-206">On the **Microsoft Update** page, click **Next**.</span></span>

14. <span data-ttu-id="ce622-207">Dans la page êtes-vous **prêt à installer le programme** , cliquez sur **installer**.</span><span class="sxs-lookup"><span data-stu-id="ce622-207">On the **Ready to Install the Program** page, click **Install**.</span></span>

15. <span data-ttu-id="ce622-208">Dans la page **fin de l’Assistant Installation des composants de création de rapports Operations Manager** , cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="ce622-208">On the **Completing the Operations Manager Reporting Components Setup Wizard** page, click **Finish**.</span></span>

16. <span data-ttu-id="ce622-209">Dans le programme d’installation de System Center Operations Manager 2007 R2, cliquez sur **quitter**.</span><span class="sxs-lookup"><span data-stu-id="ce622-209">In System Center Operations Manager 2007 R2 Setup, click **Exit**.</span></span>

<span data-ttu-id="ce622-210">Après l’installation de la fonctionnalité de création de rapports du centre de systèmes, vous pouvez utiliser la procédure suivante pour réinitialiser le nom du groupe de sécurité associé à la création de rapports SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ce622-210">After System Center reporting has been installed you then use the following procedure to reset the name of the security group associated with SQL Server reporting.</span></span> <span data-ttu-id="ce622-211">Là encore, cette procédure est requise uniquement si vous utilisez SQL Server :</span><span class="sxs-lookup"><span data-stu-id="ce622-211">Again, this procedure is only required if you are using SQL Server:</span></span>

1.  <span data-ttu-id="ce622-212">Cliquez sur **Démarrer**, pointez sur **Outils d’administration**, puis cliquez sur **Gestionnaire de serveur**.</span><span class="sxs-lookup"><span data-stu-id="ce622-212">Click **Start**, point to **Administrative Tools**, and then click **Server Manager**.</span></span>

2.  <span data-ttu-id="ce622-213">Dans le gestionnaire de serveur, développez **configuration**, **utilisateurs et groupes locaux**, puis cliquez sur **groupes**.</span><span class="sxs-lookup"><span data-stu-id="ce622-213">In Server Manager, expand **Configuration**, expand **Local Users and Groups**, and then click **Groups**.</span></span>

3.  <span data-ttu-id="ce622-214">Recherchez le groupe suivant, dans lequel ATL-SC-001 représente le nom de votre ordinateur et ARCHINST représente l’instance SQL Server pour les bases de données d’archivage et de surveillance : **SQLServerReportServerUser $ ATL-SC-001 $ MSRS10. ARCHINST**.</span><span class="sxs-lookup"><span data-stu-id="ce622-214">Locate the following group, where atl-sc-001 represents the name of your computer and ARCHINST represents the SQL Server instance for the archiving and monitoring databases: **SQLServerReportServerUser$atl-sc-001$MSRS10.ARCHINST**.</span></span>

4.  <span data-ttu-id="ce622-215">Cliquez avec le bouton droit sur le groupe, puis cliquez sur **Renommer**.</span><span class="sxs-lookup"><span data-stu-id="ce622-215">Right-click the group and then click **Rename**.</span></span> <span data-ttu-id="ce622-216">Pour renommer le groupe, ajoutez **\_ 50** à la fin du nom du groupe, juste avant le nom de l’instance SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ce622-216">Rename the group by adding **\_50** to the end of the group name, right before the SQL Server instance name.</span></span> <span data-ttu-id="ce622-217">Par exemple : **SQLServerReportServerUser $ ATL-SC-001 $ MSRS10 \_ 50. ARCHINST**.</span><span class="sxs-lookup"><span data-stu-id="ce622-217">For example: **SQLServerReportServerUser$atl-sc-001$MSRS10\_50.ARCHINST**.</span></span>

5.  <span data-ttu-id="ce622-218">Fermez le gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="ce622-218">Close Server Manager.</span></span>

<span data-ttu-id="ce622-219">Si la console opérations de System Center est ouverte, vous devez fermer l’application, puis la redémarrer. dans le cas contraire, l’onglet **création de rapports** n’apparaît pas dans l’interface utilisateur de la console opérations.</span><span class="sxs-lookup"><span data-stu-id="ce622-219">If the System Center Operations Console is open you will need to close the application and then restart it; if you do not do this the **Reporting** tab will not appear in the Operations Console user interface.</span></span> <span data-ttu-id="ce622-220">Notez que, après le redémarrage de la console d’opérations pour la première fois, tous les rapports d’analyse apparaissent dans l’onglet **rapports** .</span><span class="sxs-lookup"><span data-stu-id="ce622-220">Note that, after restarting the Operations Console the first time, it could take several minutes before all the Monitoring Reports appear on the **Reporting** tab.</span></span>

<span data-ttu-id="ce622-221"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ce622-221"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

