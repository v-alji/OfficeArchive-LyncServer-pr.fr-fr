---
title: 'Lync Server 2013 : Installation des composants serveur Lync Server'
description: 'Lync Server 2013 : Installez les composants Lync Server Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Install Lync Server server components
ms:assetid: 186aed6e-7adf-4a92-9f2e-f9a4de5ff202
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398239(v=OCS.15)
ms:contentKeyID: 48183528
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1930926f3a46be868d838abf646eb8702c9713a8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427165"
---
# <a name="install-server-components-for-lync-server-2013"></a><span data-ttu-id="47657-103">Installation des composants serveur pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="47657-103">Install server components for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="47657-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="47657-104">

<span> </span></span></span>

<span data-ttu-id="47657-105">_**Dernière modification de la rubrique :** 2014-05-05_</span><span class="sxs-lookup"><span data-stu-id="47657-105">_**Topic Last Modified:** 2014-05-05_</span></span>

<span data-ttu-id="47657-106">Avant d’effectuer cette procédure, vérifiez que vous êtes connecté au serveur à l’aide d’un compte d’utilisateur de domaine qui est un administrateur local et un membre du groupe RTCUniversalReadOnlyAdmins dans Active Directory.</span><span class="sxs-lookup"><span data-stu-id="47657-106">Before following these steps, make sure you’re logged onto the server with a domain user account that’s both a local administrator and a member of the RTCUniversalReadOnlyAdmins group in Active Directory.</span></span>

<span data-ttu-id="47657-107">L’Assistant Déploiement de Lync Server est utilisé pour installer les composants nécessaires pour chaque rôle serveur Lync et pour activer le serveur.</span><span class="sxs-lookup"><span data-stu-id="47657-107">The Lync Server Deployment Wizard is used to install the needed components for each Lync server role and to activate the server.</span></span> <span data-ttu-id="47657-108">Cet article vous guide dans la procédure de déploiement d’un serveur Standard Edition Server ou d’un serveur frontal dans votre infrastructure Lync.</span><span class="sxs-lookup"><span data-stu-id="47657-108">This article walks you through the steps of deploying a Standard Edition server or a Front End Server in your Lync infrastructure.</span></span>

<div>

## <a name="to-install-lync-server-components"></a><span data-ttu-id="47657-109">Pour installer les composants serveur Lync</span><span class="sxs-lookup"><span data-stu-id="47657-109">To install Lync Server components</span></span>

1.  <span data-ttu-id="47657-110">Si l’Assistant Déploiement de Lync Server n’est pas en cours d’exécution, démarrez-le sur le serveur sur lequel vous voulez installer Lync.</span><span class="sxs-lookup"><span data-stu-id="47657-110">If the Lync Server Deployment Wizard isn’t running, start it on the server you want to install Lync onto.</span></span>

2.  <span data-ttu-id="47657-111">Cliquez sur **installer ou mettre à jour le système de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="47657-111">Click **Install or Update Lync Server System**.</span></span>

3.  <span data-ttu-id="47657-112">Dans l’Assistant Déploiement, confirmez que l' **étape 1 : installer le magasin de configuration local** est une coche verte, ce qui signifie que ce serveur possède une copie locale du Store correctement installée.</span><span class="sxs-lookup"><span data-stu-id="47657-112">In the Deployment Wizard, confirm that **Step 1: Install Local Configuration Store** has a green check mark, which means that this server has a local copy of the store installed successfully.</span></span> <span data-ttu-id="47657-113">Si ce n’est pas le cas, vous devez installer le magasin de configuration local sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="47657-113">If it’s not checked, you need to install the Local Configuration store on the server.</span></span> <span data-ttu-id="47657-114">Suivez les étapes décrites dans [installer le magasin de configuration local dans Lync Server 2013](lync-server-2013-install-the-local-configuration-store.md) , puis revenez ici.</span><span class="sxs-lookup"><span data-stu-id="47657-114">Follow the steps at [Install the Local Configuration store in Lync Server 2013](lync-server-2013-install-the-local-configuration-store.md) and then come back here.</span></span>

4.  <span data-ttu-id="47657-115">Lorsque vous êtes prêt à installer les composants Lync Server 2013 sur votre serveur, cliquez sur **exécuter** en regard de l' **étape 2 : configurer ou supprimer les composants Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="47657-115">When you’re ready to install the Lync Server 2013 components on your server, click **Run** next to **Step 2: Setup or Remove Lync Server Components**.</span></span>

5.  <span data-ttu-id="47657-116">Sur la page **configurer les composants Lync Server** , cliquez sur **suivant** pour configurer les composants comme définis dans votre topologie publiée.</span><span class="sxs-lookup"><span data-stu-id="47657-116">On the **Set Up Lync Server Components** page, click **Next** to set up components as defined in your published topology.</span></span>

6.  <span data-ttu-id="47657-117">La page de **commandes en cours d’exécution** affiche un récapitulatif des commandes et des informations d’installation lorsque la configuration est effectuée.</span><span class="sxs-lookup"><span data-stu-id="47657-117">The **Executing Commands** page will display a summary of commands and installation information as the set up takes place.</span></span> <span data-ttu-id="47657-118">Une fois l’opération terminée, vous pouvez sélectionner un journal à afficher dans la liste, puis cliquer sur **Afficher le journal**.</span><span class="sxs-lookup"><span data-stu-id="47657-118">When it’s done, you can use the list to select a log to view, and then click **View Log**.</span></span>

7.  <span data-ttu-id="47657-119">Lorsque l’installation des composants Lync Server 2013 est terminée et que vous avez examiné les journaux le cas échéant, cliquez sur **Terminer** pour achever cette étape de l’installation.</span><span class="sxs-lookup"><span data-stu-id="47657-119">When Lync Server 2013 components setup is done, and you’ve reviewed the logs as needed, click **Finish** to complete this step in the installation.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="47657-120">Si vous êtes invité à redémarrer le serveur (ce qui peut se produire si l’expérience de bureau Windows est nécessaire), faites-le.</span><span class="sxs-lookup"><span data-stu-id="47657-120">If you’re prompted to restart the server (which might happen if Windows Desktop Experience needed to be installed), definitely do that.</span></span> <span data-ttu-id="47657-121">Lorsque l’ordinateur est restauré et en cours d’exécution, vous devez effectuer ces étapes à nouveau, en commençant à l’étape 3 ci-dessus (exécutez l’étape 2 de l’Assistant Déploiement une fois).</span><span class="sxs-lookup"><span data-stu-id="47657-121">When the computer is back up and running, you need to do these steps over again, starting from step three listed above (basically run Step 2 in the Deployment Wizard one more time).</span></span>

    
    <span data-ttu-id="47657-122"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="47657-122"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

