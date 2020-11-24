---
title: 'Lync Server 2013 : Publication de la topologie mise à jour'
description: 'Lync Server 2013 : Publiez la topologie mise à jour.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Publish the updated topology
ms:assetid: 59455dd1-6a9e-433f-a714-d3636c068100
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204910(v=OCS.15)
ms:contentKeyID: 48184203
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c27cca2eae86eadaf1ff37e2c3520eaec3f86c98
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394560"
---
# <a name="publish-the-updated-topology-in-lync-server-2013"></a><span data-ttu-id="e71df-103">Publication de la topologie mise à jour dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e71df-103">Publish the updated topology in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e71df-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e71df-104">

<span> </span></span></span>

<span data-ttu-id="e71df-105">_**Dernière modification de la rubrique :** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="e71df-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="e71df-106">Après avoir effectué la mise à jour de votre topologie dans le générateur de topologie, vous devez publier la topologie dans le centre de gestion central avant de pouvoir configurer et utiliser le serveur de chat permanent.</span><span class="sxs-lookup"><span data-stu-id="e71df-106">After updating your topology in Topology Builder, you must publish the topology to the Central Management store before you can configure and use Persistent Chat Server.</span></span> <span data-ttu-id="e71df-107">Les copies en lecture seule des données sont répliquées sur tous les serveurs de la topologie afin de maintenir la synchronisation de tous les serveurs avec la topologie et d’autres modifications intervenues dans la configuration.</span><span class="sxs-lookup"><span data-stu-id="e71df-107">Read-only copies of the data are replicated to all servers in the topology to keep all servers in sync with topology and other configuration changes.</span></span>

<div>

## <a name="to-publish-an-updated-topology"></a><span data-ttu-id="e71df-108">Pour publier une topologie mise à jour</span><span class="sxs-lookup"><span data-stu-id="e71df-108">To publish an updated topology</span></span>

<span data-ttu-id="e71df-109">Avant de publier votre topologie, installez les bases de données pour le serveur de chat permanent.</span><span class="sxs-lookup"><span data-stu-id="e71df-109">Before you publish your topology, install the databases for Persistent Chat Server.</span></span> <span data-ttu-id="e71df-110">Utilisez le générateur de topologie pour installer des bases de données en sélectionnant **action** et **installer la base de données**.</span><span class="sxs-lookup"><span data-stu-id="e71df-110">Use Topology Builder to install databases by selecting **Action** and **Install Database**.</span></span>

1.  <span data-ttu-id="e71df-111">Sur un ordinateur exécutant Lync Server 2013 ou sur lequel sont installés les outils d’administration de Lync Server, connectez-vous à l’aide d’un compte membre du groupe **administrateurs de domaine** et du groupe **RTCUniversalServerAdmins** . et qui dispose des autorisations de contrôle total (en lecture, écriture et modification) sur le magasin de fichiers à utiliser pour le stockage des fichiers du serveur de chat permanent (de sorte que le générateur de topologie puisse configurer les listes de contrôle d’accès discrétionnaire requises (DACL)) ou un compte avec des droits d’utilisateur équivalents.</span><span class="sxs-lookup"><span data-stu-id="e71df-111">On a computer that is running Lync Server 2013 or on which the Lync Server administrative tools are installed, log on using an account that is a member of both the **Domain Admins** group and the **RTCUniversalServerAdmins** group, and that has full control permissions (that is, read, write, and modify) on the file store to be used for the Persistent Chat Server file store (so that Topology Builder can configure the required discretionary access control lists (DACLs)), or an account with equivalent user rights.</span></span>

2.  <span data-ttu-id="e71df-112">Démarrer le générateur de topologie.</span><span class="sxs-lookup"><span data-stu-id="e71df-112">Start Topology Builder.</span></span> <span data-ttu-id="e71df-113">Sélectionnez l’option **Télécharger la topologie à partir du déploiement existant** ou **Ouvrez la topologie à partir d’un fichier local** si vous l’avez enregistrée localement.</span><span class="sxs-lookup"><span data-stu-id="e71df-113">Select **Download Topology from existing deployment**, or **Open Topology from a local file** if you saved it locally.</span></span>

3.  <span data-ttu-id="e71df-114">Dans l’arborescence de la console, cliquez avec le bouton droit sur **Lync Server 2013**, puis cliquez sur **publier la topologie**.</span><span class="sxs-lookup"><span data-stu-id="e71df-114">In the console tree, right-click **Lync Server 2013**, and then click **Publish Topology**.</span></span>

4.  <span data-ttu-id="e71df-115">Dans la page **Publier la topologie**, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="e71df-115">On the **Publish the topology** page, click **Next**.</span></span>

5.  <span data-ttu-id="e71df-116">Dans la page **Assistant Publication terminé**, assurez-vous que la topologie a été publiée correctement, puis cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="e71df-116">On the **Publishing wizard complete** page, verify that the topology was successfully published, and then click **Finish**.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="e71df-117">Après la publication de la topologie, vous devez configurer la prise en charge du serveur de chat permanent pour pouvoir archiver le contenu.</span><span class="sxs-lookup"><span data-stu-id="e71df-117">After publishing the topology, you must configure support for Persistent Chat Server before any content can be archived.</span></span>

    
    <span data-ttu-id="e71df-118"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e71df-118"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

