---
title: 'Lync Server 2013 : Installation de la base de données de serveur Standard Edition'
description: 'Lync Server 2013 : installation de la base de données Standard Edition Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Install Standard Edition server database
ms:assetid: 0bd3a804-aad6-48cb-981b-54725af032db
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398167(v=OCS.15)
ms:contentKeyID: 48183385
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0a20d2c01de94ad88960555db78c57c6b79d92f7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427151"
---
# <a name="install-standard-edition-server-database-for-lync-server-2013"></a><span data-ttu-id="b3913-103">Installation de la base de données de serveur Standard Edition pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b3913-103">Install Standard Edition server database for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b3913-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b3913-104">

<span> </span></span></span>

<span data-ttu-id="b3913-105">_**Dernière modification de la rubrique :** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="b3913-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="b3913-106">La configuration d’un serveur Standard Edition Server en tant que serveur unique dans votre infrastructure qui est identique à celle d’autres installations de serveur dans le cadre de l' **Assistant Déploiement** est une sélection spécifique à la configuration du serveur initial.</span><span class="sxs-lookup"><span data-stu-id="b3913-106">Setting up a Standard Edition server as the only server in your infrastructure that homes users differs from other server installations in that there is a selection in the **Deployment Wizard** specifically for setting up the initial server.</span></span>

<div>

## <a name="to-install-a-standard-edition-server"></a><span data-ttu-id="b3913-107">Pour installer un serveur Standard Edition Server</span><span class="sxs-lookup"><span data-stu-id="b3913-107">To install a Standard Edition server</span></span>

1.  <span data-ttu-id="b3913-108">Ouvrez une session sur le serveur sur lequel vous allez installer Standard Edition Server en tant qu’administrateur local ou un domaine équivalent.</span><span class="sxs-lookup"><span data-stu-id="b3913-108">Log on to the server where you are going to install Standard Edition server as a local administrator or a domain equivalent.</span></span>

2.  <span data-ttu-id="b3913-109">Si vous n’avez pas encore préparé les services de domaine Active Directory, vous devez d’abord effectuer ces procédures.</span><span class="sxs-lookup"><span data-stu-id="b3913-109">If you have not prepared Active Directory Domain Services, then first perform those procedures.</span></span> <span data-ttu-id="b3913-110">Pour plus d’informations, consultez [préparation des services de domaine Active Directory pour Lync Server 2013](lync-server-2013-preparing-active-directory-domain-services.md).</span><span class="sxs-lookup"><span data-stu-id="b3913-110">For details, see [Preparing Active Directory Domain Services for Lync Server 2013](lync-server-2013-preparing-active-directory-domain-services.md).</span></span>

3.  <span data-ttu-id="b3913-111">Dans l’Assistant Déploiement de Lync Server, cliquez sur **préparer le premier serveur Standard Edition**.</span><span class="sxs-lookup"><span data-stu-id="b3913-111">In the Lync Server Deployment Wizard, click **Prepare first Standard Edition server**.</span></span>

4.  <span data-ttu-id="b3913-112">Sur la page **préparer Single Standard Edition Server** , cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="b3913-112">On the **Prepare single Standard Edition Server** page, click **Next**.</span></span>

5.  <span data-ttu-id="b3913-113">Sur la page **exécution des commandes** , SQL Server 2012 Express est installé en tant que magasin de gestion centrale.</span><span class="sxs-lookup"><span data-stu-id="b3913-113">On the **Executing Commands** page, the SQL Server 2012 Express is installed as the Central Management store.</span></span> <span data-ttu-id="b3913-114">Des règles de pare-feu nécessaires sont créées.</span><span class="sxs-lookup"><span data-stu-id="b3913-114">Necessary firewall rules are created.</span></span> <span data-ttu-id="b3913-115">Lorsque l’installation de la base de données et du logiciel requis est terminée, cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="b3913-115">When the installation of the database and prerequisite software is completed, click **Finish**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="b3913-116">L’installation initiale risque de prendre un certain temps sans qu’aucune mise à jour ne s’affiche à l’écran de synthèse de la sortie de commande.</span><span class="sxs-lookup"><span data-stu-id="b3913-116">The initial installation may take some time with no visible updates to the command output summary screen.</span></span> <span data-ttu-id="b3913-117">Le problème est dû à l’installation de SQL Server Express.</span><span class="sxs-lookup"><span data-stu-id="b3913-117">This is due to the installation of the SQL Server Express.</span></span> <span data-ttu-id="b3913-118">Si vous avez besoin de surveiller l’installation de la base de données, utilisez le gestionnaire des tâches pour contrôler la configuration.</span><span class="sxs-lookup"><span data-stu-id="b3913-118">If you need to monitor the installation of the database, use Task Manager to monitor the setup.</span></span>

    
    </div>

6.  <span data-ttu-id="b3913-119">Dans la page Assistant Déploiement de Lync Server, cliquez sur **installer le générateur de topologie** si vous n’avez pas encore installé les outils d’administration.</span><span class="sxs-lookup"><span data-stu-id="b3913-119">On the Lync Server Deployment Wizard page, click **Install Topology Builder** if you have not previously installed the administrative tools.</span></span> <span data-ttu-id="b3913-120">Pour en savoir plus, voir [installer les outils d’administration de Lync Server 2013](lync-server-2013-install-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="b3913-120">For details, see [Install Lync Server 2013 administrative tools](lync-server-2013-install-lync-server-administrative-tools.md).</span></span>

7.  <span data-ttu-id="b3913-121">Vérifiez que la case à cocher « préparer Active Directory » et « préparer le premier serveur Standard Edition » et « installer le générateur de topologie » est activée.</span><span class="sxs-lookup"><span data-stu-id="b3913-121">Confirm that there are green check marks next to “Prepare Active Directory,” “Prepare first Standard Edition server,” and “Install Topology Builder.”</span></span>

<span data-ttu-id="b3913-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b3913-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

