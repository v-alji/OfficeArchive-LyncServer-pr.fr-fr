---
title: 'Lync Server 2013 : ajout et activation d’un compte d’utilisateur pour Lync Server'
description: 'Lync Server 2013 : ajoutez et activez un compte d’utilisateur pour Lync Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Add and enable user account for Lync Server
ms:assetid: 1edd1c1c-307d-450b-abea-33aaf56bdf13
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520961(v=OCS.15)
ms:contentKeyID: 48183578
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4f70ae2da122a0db3986a75677c1d29234fbe0e3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439372"
---
# <a name="add-and-enable-user-account-for-lync-server-2013"></a><span data-ttu-id="f2d4f-103">Ajouter et activer un compte d’utilisateur pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f2d4f-103">Add and enable user account for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f2d4f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f2d4f-104">

<span> </span></span></span>

<span data-ttu-id="f2d4f-105">_**Dernière modification de la rubrique :** 2012-11-02_</span><span class="sxs-lookup"><span data-stu-id="f2d4f-105">_**Topic Last Modified:** 2012-11-02_</span></span>

<span data-ttu-id="f2d4f-106">Après avoir activé un compte d’utilisateur dans utilisateurs et ordinateurs Active Directory, vous pouvez utiliser le panneau de configuration de Lync Server pour créer et activer les nouveaux comptes d’utilisateurs Lync Server 2013 en ajoutant un utilisateur Active Directory à Lync Server.</span><span class="sxs-lookup"><span data-stu-id="f2d4f-106">After enabling a user account in Active Directory Users and Computers, you can use Lync Server Control Panel to create and enable new Lync Server 2013 user accounts by adding an Active Directory user to Lync Server.</span></span>

<div>

## <a name="to-add-and-enable-a-new-lync-server-user"></a><span data-ttu-id="f2d4f-107">Pour ajouter et activer un nouvel utilisateur Lync Server</span><span class="sxs-lookup"><span data-stu-id="f2d4f-107">To add and enable a new Lync Server user</span></span>

1.  <span data-ttu-id="f2d4f-108">À partir d’un compte d’utilisateur auquel est affecté le rôle CsUserAdministrator ou CsAdministrator, ouvrez une session sur un ordinateur de votre déploiement interne.</span><span class="sxs-lookup"><span data-stu-id="f2d4f-108">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="f2d4f-109">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="f2d4f-109">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="f2d4f-110">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="f2d4f-110">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="f2d4f-111">Dans la barre de navigation de gauche, cliquez sur **Utilisateurs**.</span><span class="sxs-lookup"><span data-stu-id="f2d4f-111">In the left navigation bar, click **Users**.</span></span>

4.  <span data-ttu-id="f2d4f-112">Cliquez sur **activer les utilisateurs**.</span><span class="sxs-lookup"><span data-stu-id="f2d4f-112">Click **Enable users**.</span></span>

5.  <span data-ttu-id="f2d4f-113">Dans la boîte de dialogue **nouveau serveur Lync** , cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="f2d4f-113">On the **New Lync Server User** dialog, click **Add**.</span></span>

6.  <span data-ttu-id="f2d4f-114">Dans la boîte de dialogue **Rechercher des utilisateurs** , tapez tout ou la première partie du nom, le nom d’affichage, le prénom, le nom, le nom du compte Sam (Security Accounts Manager), l’adresse de messagerie, le nom d’utilisateur principal (UPN) ou le numéro de téléphone du compte d’utilisateur Active Directory souhaité, puis cliquez sur **Rechercher**.</span><span class="sxs-lookup"><span data-stu-id="f2d4f-114">In the **Search users** box, type all or the first portion of the name, display name, first name, last name, Security Accounts Manager (SAM) account name, email address, User Principal Name (UPN), or phone number of the Active Directory user account that you want, and then click **Find**.</span></span>

7.  <span data-ttu-id="f2d4f-115">Dans le tableau, sélectionnez le compte que vous voulez ajouter à Lync Server, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="f2d4f-115">In the table, select the account you want to add to Lync Server, and then click **OK**.</span></span>

8.  <span data-ttu-id="f2d4f-116">Affectez l’utilisateur à un pool, spécifiez des détails supplémentaires et attribuez les stratégies à l’utilisateur de votre choix, puis cliquez sur **activer**.</span><span class="sxs-lookup"><span data-stu-id="f2d4f-116">Assign the user to a pool, specify any additional details, and assign the policies to the user you want, and then click **Enable**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="f2d4f-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2d4f-117">See Also</span></span>


[<span data-ttu-id="f2d4f-118">Désactiver ou réactiver le compte d’utilisateur pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f2d4f-118">Disable or re-enable user account for Lync Server 2013</span></span>](lync-server-2013-disable-or-re-enable-user-account-for-lync-server.md)  
[<span data-ttu-id="f2d4f-119">Supprimer un compte d’utilisateur de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f2d4f-119">Remove a user account from Lync Server 2013</span></span>](lync-server-2013-remove-a-user-account-from-lync-server.md)  


[<span data-ttu-id="f2d4f-120">Activation et désactivation des utilisateurs pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f2d4f-120">Enabling and disabling users for Lync Server 2013</span></span>](lync-server-2013-enabling-and-disabling-users-for-lync-server.md)  
  

<span data-ttu-id="f2d4f-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f2d4f-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

