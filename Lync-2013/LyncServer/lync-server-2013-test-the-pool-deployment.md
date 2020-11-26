---
title: 'Lync Server 2013 : Test du déploiement du pool'
description: 'Lync Server 2013 : testez le déploiement du pool.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test the pool deployment
ms:assetid: ffd80617-155a-4041-bbeb-74503e7938dd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413092(v=OCS.15)
ms:contentKeyID: 48185976
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 28101a252eda5048ded9f1eaf76c092c5cb7f986
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444230"
---
# <a name="test-the-pool-deployment-in-lync-server-2013"></a><span data-ttu-id="16eb0-103">Test du déploiement du pool dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="16eb0-103">Test the pool deployment in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="16eb0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="16eb0-104">

<span> </span></span></span>

<span data-ttu-id="16eb0-105">_**Dernière modification de la rubrique :** 2013-09-25_</span><span class="sxs-lookup"><span data-stu-id="16eb0-105">_**Topic Last Modified:** 2013-09-25_</span></span>

<span data-ttu-id="16eb0-106">La procédure suivante vous explique comment tester le déploiement du pool frontal.</span><span class="sxs-lookup"><span data-stu-id="16eb0-106">The following procedure describes how to test the deployment of the Front End pool.</span></span>

<div>

## <a name="to-test-the-pool-deployment"></a><span data-ttu-id="16eb0-107">Pour tester le déploiement du pool</span><span class="sxs-lookup"><span data-stu-id="16eb0-107">To test the pool deployment</span></span>

1.  <span data-ttu-id="16eb0-108">Utilisez les ordinateurs et les utilisateurs Active Directory pour ajouter l’objet utilisateur Active Directory du rôle administrateur pour le déploiement de Lync Server 2013 (sur lequel est installé le panneau de configuration Lync Server 2013) vers le groupe **CSAdministrator** .</span><span class="sxs-lookup"><span data-stu-id="16eb0-108">Use Active Directory Computers and Users to add the Active Directory user object of the administrator role for the Lync Server 2013 deployment (on which Lync Server 2013 Control Panel is installed) to the **CSAdministrator** group.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="16eb0-109">Si vous n’ajoutez pas les utilisateurs et les groupes appropriés au groupe CsAdministors, vous recevez un message d’erreur lors de l’ouverture du panneau de configuration de Lync Server, qui indique que l’accès à un contrôle de contrôle d’accès basé sur les rôles (RBAC) est refusé en raison d’un échec de l’autorisation de contrôle d’accès basé sur un rôle.»</span><span class="sxs-lookup"><span data-stu-id="16eb0-109">If you do not add the appropriate users and groups to the CsAdministors group, you will receive an error when opening Lync Server Control Panel, which states that “Unauthorized: Access is denied due to a role-based access control (RBAC) authorization failure.”</span></span>

    
    </div>

2.  <span data-ttu-id="16eb0-110">Si l’objet utilisateur est actuellement connecté, fermez, puis rouvrez la session pour inscrire la nouvelle affectation de groupe.</span><span class="sxs-lookup"><span data-stu-id="16eb0-110">If the user object is currently logged on, log off and then log on again to register the new group assignment.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="16eb0-111">Le compte d’utilisateur ne peut pas être l’administrateur local de tout serveur exécutant Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="16eb0-111">The user account cannot be the local administrator of any server running Lync Server 2013.</span></span>

    
    </div>

3.  <span data-ttu-id="16eb0-112">Utilisez le compte administratif pour vous connecter à l’ordinateur sur lequel le panneau de configuration de Lync Server est installé.</span><span class="sxs-lookup"><span data-stu-id="16eb0-112">Use the administrative account to log on to the computer where Lync Server Control Panel is installed.</span></span>

4.  <span data-ttu-id="16eb0-113">Démarrez le panneau de configuration de Lync Server, puis fournissez les informations d’identification, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="16eb0-113">Start Lync Server Control Panel, and then provide credentials, if prompted.</span></span> <span data-ttu-id="16eb0-114">Le panneau de configuration de Lync Server affiche des informations de déploiement.</span><span class="sxs-lookup"><span data-stu-id="16eb0-114">Lync Server Control Panel displays deployment information.</span></span>

5.  <span data-ttu-id="16eb0-115">Dans la barre de navigation de gauche, cliquez sur **Topology**, puis vérifiez que l’état du service affiche un ordinateur avec une flèche verte et qu’une coche verte pour l’état de réplication est située en regard de chaque rôle serveur Lync Server déployé et remis en ligne.</span><span class="sxs-lookup"><span data-stu-id="16eb0-115">In the left navigation bar, click **Topology**, and then confirm that the service status shows a computer with a green arrow and that a green check mark for replication status is next to each Lync Server server role that has been deployed and brought online.</span></span>

6.  <span data-ttu-id="16eb0-116">Dans la barre de navigation de gauche, cliquez sur **Utilisateurs**, puis sur **Activer les utilisateurs**.</span><span class="sxs-lookup"><span data-stu-id="16eb0-116">In the left navigation bar, click **Users**, and then click **Enable users**.</span></span>

7.  <span data-ttu-id="16eb0-117">Dans la page **nouveau serveur Lync** , cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="16eb0-117">On the **New Lync Server User** page, click **Add**.</span></span>

8.  <span data-ttu-id="16eb0-118">Pour définir les paramètres de recherche des objets que vous souhaitez trouver, sur la page **Sélectionner à partir d’Active Directory**, vous pouvez sélectionner **Rechercher**, puis éventuellement cliquer sur **Ajouter un filtre**.</span><span class="sxs-lookup"><span data-stu-id="16eb0-118">To define search parameters for the objects you want to find, on the **Select from Active Directory** page, you can select **Search**, and then optionally click **Add Filter**.</span></span> <span data-ttu-id="16eb0-119">Vous pouvez également sélectionner **Recherche LDAP** et entrer une expression LDAP pour filtrer ou limiter les objets qui seront renvoyés.</span><span class="sxs-lookup"><span data-stu-id="16eb0-119">You can also select **LDAP search** and enter an LDAP expression to filter or limit the objects that will be returned.</span></span> <span data-ttu-id="16eb0-120">Après avoir choisi les options de recherche, **sélectionnez Rechercher**.</span><span class="sxs-lookup"><span data-stu-id="16eb0-120">After you have decided on your Search options, clink **Find**.</span></span>

9.  <span data-ttu-id="16eb0-121">Dans le volet résultats de la recherche, sélectionnez tous les objets pour cette session de recherche, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="16eb0-121">In the Search results pane, select all the objects for this search session, and then click **OK**.</span></span>

10. <span data-ttu-id="16eb0-122">Dans la page **nouvel utilisateur de Lync Server** , le ou les objets que vous avez sélectionnés apparaissent dans l’affichage **utilisateurs** .</span><span class="sxs-lookup"><span data-stu-id="16eb0-122">On the **New Lync Server User** page, the object or objects you selected are in the **Users** display.</span></span> <span data-ttu-id="16eb0-123">Dans la liste **attribuer des utilisateurs à un pool** , sélectionnez le serveur sur lequel les objets doivent être hébergés.</span><span class="sxs-lookup"><span data-stu-id="16eb0-123">In the **Assign users to a pool** list, select the server where the objects should be homed.</span></span>
    
    <span data-ttu-id="16eb0-124">Vous trouverez ci-dessous un certain nombre d’options de configuration des objets.</span><span class="sxs-lookup"><span data-stu-id="16eb0-124">Following are a number of options for configuring the objects.</span></span>
    
      - <span data-ttu-id="16eb0-125">**Générer l’URL SIP de l’utilisateur**</span><span class="sxs-lookup"><span data-stu-id="16eb0-125">**Generate user’s SIP URI**</span></span>
    
      - <span data-ttu-id="16eb0-126">**Téléphonie**</span><span class="sxs-lookup"><span data-stu-id="16eb0-126">**Telephony**</span></span>
    
      - <span data-ttu-id="16eb0-127">**URI de ligne**</span><span class="sxs-lookup"><span data-stu-id="16eb0-127">**Line URI**</span></span>
    
      - <span data-ttu-id="16eb0-128">**Stratégie de conférence**</span><span class="sxs-lookup"><span data-stu-id="16eb0-128">**Conferencing policy**</span></span>
    
      - <span data-ttu-id="16eb0-129">**Stratégie de version du client**</span><span class="sxs-lookup"><span data-stu-id="16eb0-129">**Client version policy**</span></span>
    
      - <span data-ttu-id="16eb0-130">**Stratégie de code confidentiel**</span><span class="sxs-lookup"><span data-stu-id="16eb0-130">**PIN policy**</span></span>
    
      - <span data-ttu-id="16eb0-131">**Stratégie d’accès externe**</span><span class="sxs-lookup"><span data-stu-id="16eb0-131">**External access policy**</span></span>
    
      - <span data-ttu-id="16eb0-132">**Stratégie d’archivage**</span><span class="sxs-lookup"><span data-stu-id="16eb0-132">**Archiving policy**</span></span>
    
      - <span data-ttu-id="16eb0-133">**Stratégie d’emplacement**</span><span class="sxs-lookup"><span data-stu-id="16eb0-133">**Location policy**</span></span>
    
      - <span data-ttu-id="16eb0-134">**Stratégie du client**</span><span class="sxs-lookup"><span data-stu-id="16eb0-134">**Client policy**</span></span>
    
    <span data-ttu-id="16eb0-135">Pour tester la fonctionnalité de base, sélectionnez l’option de votre choix pour le paramètre **URI SIP de l’utilisateur générer** (les autres options dans la configuration utiliseront les paramètres par défaut), puis cliquez sur **activer**.</span><span class="sxs-lookup"><span data-stu-id="16eb0-135">For the purposes of testing the basic functionality, select the option you prefer for the **Generate user’s SIP URI** setting (the other options in the configuration will use default settings), and then click **Enable**.</span></span>

11. <span data-ttu-id="16eb0-136">Une page de résumé s’ouvre et affiche une coche dans la colonne **activé** pour indiquer que les objets sont désormais prêts à l’emploi.</span><span class="sxs-lookup"><span data-stu-id="16eb0-136">A summary page is displayed that shows a check mark in the **Enabled** column to indicate that the objects are now ready for use.</span></span> <span data-ttu-id="16eb0-137">La colonne **adresse SIP** affiche l’adresse dont vous avez besoin pour la configuration de connexion de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="16eb0-137">The **SIP address** column displays the address you need for the user sign-in configuration.</span></span>

12. <span data-ttu-id="16eb0-138">Connectez un utilisateur à un ordinateur joint au domaine et un autre utilisateur à un autre ordinateur du domaine.</span><span class="sxs-lookup"><span data-stu-id="16eb0-138">Log one user on to a computer that is joined to the domain, and another user on to another computer in the domain.</span></span>

13. <span data-ttu-id="16eb0-139">Installez Lync 2013 sur chacun des deux ordinateurs client, puis vérifiez que les deux utilisateurs peuvent se connecter à Lync Server 2013 et pouvoir vous envoyer des messages instantanés.</span><span class="sxs-lookup"><span data-stu-id="16eb0-139">Install Lync 2013 on each of the two client computers, and then verify that both users can sign in to Lync Server 2013 and can send instant messages to each other.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="16eb0-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="16eb0-140">See Also</span></span>


[<span data-ttu-id="16eb0-141">Déploiement de clients et d’appareils dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="16eb0-141">Deploying clients and devices in Lync Server 2013</span></span>](lync-server-2013-deploying-clients-and-devices.md)  
  

<span data-ttu-id="16eb0-142"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="16eb0-142"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

