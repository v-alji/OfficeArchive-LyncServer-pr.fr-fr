---
title: 'Lync Server 2013 : Installation de l’outil de planification'
description: 'Lync Server 2013 : installation de l’outil de planification.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Installing the Planning Tool
ms:assetid: ebdc9e26-4b22-4b02-85b9-7462bcfe7c93
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615046(v=OCS.15)
ms:contentKeyID: 51541525
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 11836e2c86cb01d6f911670a9eeafef0c31c0af4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426906"
---
# <a name="installing-the-planning-tool-in-lync-server-2013"></a><span data-ttu-id="dee07-103">Installation de l’outil de planification dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dee07-103">Installing the Planning Tool in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="dee07-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="dee07-104">

<span> </span></span></span>

<span data-ttu-id="dee07-105">_**Dernière modification de la rubrique :** 2013-11-07_</span><span class="sxs-lookup"><span data-stu-id="dee07-105">_**Topic Last Modified:** 2013-11-07_</span></span>

<span data-ttu-id="dee07-106">Avant de commencer à concevoir et à planifier votre infrastructure Lync Server 2013 à l’aide de l’outil de planification Microsoft Lync Server 2013, vous devez commencer par installer l’outil de planification.</span><span class="sxs-lookup"><span data-stu-id="dee07-106">Before you begin designing and planning your Lync Server 2013 infrastructure by using the Microsoft Lync Server 2013, Planning Tool, you must first install the Planning Tool.</span></span> <span data-ttu-id="dee07-107">L’outil de planification n’a pas besoin d’être déployé vers une station de travail ou un serveur qui fait partie de l’infrastructure ou du domaine sur lequel vous envisagez d’installer Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="dee07-107">The Planning Tool does not need to be deployed to a workstation or server that is part of the domain or infrastructure where you plan to install Lync Server 2013.</span></span> <span data-ttu-id="dee07-108">Le fichier Lisez-moi fourni avec les détails de l’outil de planification est une information importante sur son installation et son utilisation.</span><span class="sxs-lookup"><span data-stu-id="dee07-108">The Readme file that accompanies the Planning Tool details important information about installing and using the tool.</span></span> <span data-ttu-id="dee07-109">Certaines des informations contenues dans le fichier Lisez-moi sont expliquées ici par souci de clarté.</span><span class="sxs-lookup"><span data-stu-id="dee07-109">Some of the information in the Readme file is duplicated here for clarity.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="dee07-110">L’outil de planification nécessite une installation par un utilisateur disposant de droits d’administrateur et d’autorisations sur l’ordinateur sur lequel l’outil doit être installé.</span><span class="sxs-lookup"><span data-stu-id="dee07-110">The Planning Tool requires installation by a user with administrator rights and permissions on the computer on which the tool is to be installed.</span></span>



</div>

<span data-ttu-id="dee07-111">Les systèmes d’exploitation pris en charge pour l’installation et l’exécution de l’outil de planification sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="dee07-111">The supported operating systems for installation and operation of the Planning Tool are:</span></span>

  - <span data-ttu-id="dee07-112">Windows 8</span><span class="sxs-lookup"><span data-stu-id="dee07-112">Windows 8</span></span>

  - <span data-ttu-id="dee07-113">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="dee07-113">Windows 8.1</span></span>

  - <span data-ttu-id="dee07-114">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="dee07-114">Windows Server 2012</span></span>

  - <span data-ttu-id="dee07-115">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="dee07-115">Windows Server 2012 R2</span></span>

  - <span data-ttu-id="dee07-116">Windows 7, édition 32 bits</span><span class="sxs-lookup"><span data-stu-id="dee07-116">Windows 7, 32-bit edition</span></span>

  - <span data-ttu-id="dee07-117">Windows 7, édition 64 bits avec WOW (Windows on Win32)</span><span class="sxs-lookup"><span data-stu-id="dee07-117">Windows 7, 64-bit edition using Windows on Win32 (WOW)</span></span>

  - <span data-ttu-id="dee07-118">Windows Server 2008 R2 avec WOW</span><span class="sxs-lookup"><span data-stu-id="dee07-118">Windows Server 2008 R2, using WOW</span></span>

<span data-ttu-id="dee07-119">Par ailleurs, l’outil de planification nécessite Microsoft .NET Framework 4,5.</span><span class="sxs-lookup"><span data-stu-id="dee07-119">Additionally, the Planning Tool requires Microsoft .NET Framework 4.5.</span></span>

<span data-ttu-id="dee07-120">Après avoir satisfait la configuration requise, vous pouvez ensuite installer l’outil de planification.</span><span class="sxs-lookup"><span data-stu-id="dee07-120">After the preinstallation requirements are met, you can then install the Planning Tool.</span></span>

<div>

## <a name="to-install-the-planning-tool"></a><span data-ttu-id="dee07-121">Pour installer l’outil de planification</span><span class="sxs-lookup"><span data-stu-id="dee07-121">To install the Planning Tool</span></span>

1.  <span data-ttu-id="dee07-122">Connectez-vous à l’ordinateur local en tant que membre du groupe administrateurs.</span><span class="sxs-lookup"><span data-stu-id="dee07-122">Log on to the local computer as a member of the Administrators group.</span></span>

2.  <span data-ttu-id="dee07-123">À l’aide de l’Explorateur Windows ou d’une fenêtre de commande, recherchez le répertoire dans lequel vous avez téléchargé les fichiers d’installation de l’outil de planification.</span><span class="sxs-lookup"><span data-stu-id="dee07-123">Using Windows Explorer or a command window, locate the directory where you downloaded the Planning Tool installation files.</span></span>

3.  <span data-ttu-id="dee07-124">Recherchez le LyncPlanningTool.msi.</span><span class="sxs-lookup"><span data-stu-id="dee07-124">Locate the LyncPlanningTool.msi.</span></span> <span data-ttu-id="dee07-125">Dans l’Explorateur Windows, double-cliquez sur le fichier.</span><span class="sxs-lookup"><span data-stu-id="dee07-125">In Windows Explorer, double-click the file.</span></span> <span data-ttu-id="dee07-126">Dans la fenêtre de commande, tapez le nom du fichier, puis appuyez sur **Entrée** pour exécuter le fichier.</span><span class="sxs-lookup"><span data-stu-id="dee07-126">In the command window, type the name of the file, and then press **Enter** to run the file.</span></span>

4.  <span data-ttu-id="dee07-127">Dans la page Bienvenue de l' **Assistant Installation de Microsoft Lync Server 2013,** cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="dee07-127">On the Welcome page of the **Microsoft Lync Server 2013, Planning Tool Setup Wizard**, click **Next**.</span></span>

5.  <span data-ttu-id="dee07-128">Passez en revue le **Contrat de Licence Utilisateur Final**, sélectionnez **J’accepte les termes du contrat de licence** si vous choisissez d’accepter les termes d’utilisation contenus dans le contrat de licence, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="dee07-128">Review the **End-User License Agreement**, select **I accept the terms in the License Agreement** if you choose to accept the terms of use in the license agreement, and then click **Next**.</span></span>

6.  <span data-ttu-id="dee07-129">Choisissez où vous souhaitez installer les fichiers de l’outil de planification.</span><span class="sxs-lookup"><span data-stu-id="dee07-129">Choose where to install the Planning Tool files.</span></span> <span data-ttu-id="dee07-130">Par défaut, il s’agit de l’emplacement par défaut C : \\ Program Files (x86) \\ Microsoft Lync Server 2013 \\ planning.</span><span class="sxs-lookup"><span data-stu-id="dee07-130">The default location is C:\\Program Files (x86)\\Microsoft Lync Server 2013\\Planning Tool.</span></span> <span data-ttu-id="dee07-131">Si vous souhaitez choisir un autre emplacement, cliquez sur **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="dee07-131">If you want to change the installation location, click **Change**.</span></span> <span data-ttu-id="dee07-132">Dans **Modifier le dossier de destination**, accédez à l’emplacement d’installation des fichiers ou tapez-le directement dans le champ, cliquez sur **OK**, puis sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="dee07-132">On **Change destination folder**, browse or type the location to install the files, click **OK**, and then click **Next**.</span></span>

7.  <span data-ttu-id="dee07-133">Le programme d’installation est désormais prêt à installer l’outil de planification.</span><span class="sxs-lookup"><span data-stu-id="dee07-133">The installer is now ready to install the Planning Tool.</span></span> <span data-ttu-id="dee07-134">Cliquez sur **Installer** pour commencer le processus d’installation.</span><span class="sxs-lookup"><span data-stu-id="dee07-134">Click **Install** to begin the installation process.</span></span>

8.  <span data-ttu-id="dee07-135">L’installation débute et la progression s’affiche.</span><span class="sxs-lookup"><span data-stu-id="dee07-135">The installation will start, and the progress will be displayed.</span></span> <span data-ttu-id="dee07-136">Une fois l’installation terminée, cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="dee07-136">After the installation is successfully completed, click **Finish**.</span></span>

9.  <span data-ttu-id="dee07-137">L’outil de planification est prêt à l’emploi.</span><span class="sxs-lookup"><span data-stu-id="dee07-137">The Planning Tool is ready for use.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="dee07-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dee07-138">See Also</span></span>


[<span data-ttu-id="dee07-139">Installer un logiciel facultatif dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dee07-139">Installing optional software in Lync Server 2013</span></span>](lync-server-2013-installing-optional-software.md)  
  

<span data-ttu-id="dee07-140"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="dee07-140"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

