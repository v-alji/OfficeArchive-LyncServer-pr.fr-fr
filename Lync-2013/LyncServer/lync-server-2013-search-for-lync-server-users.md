---
title: 'Lync Server 2013 : Rechercher des utilisateurs de Lync Server'
description: 'Lync Server 2013 : Rechercher des utilisateurs de Lync Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Search for Lync Server users
ms:assetid: 3b9f6f55-d7a9-46ae-8e10-f221ba0d3bb5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429701(v=OCS.15)
ms:contentKeyID: 48183871
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d0c4860b7b89ad13b3a0003c5666a320172dad6d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441941"
---
# <a name="search-for-lync-server-users-in-lync-server-2013"></a><span data-ttu-id="39833-103">Rechercher des utilisateurs de Lync Server dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="39833-103">Search for Lync Server users in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="39833-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="39833-104">

<span> </span></span></span>

<span data-ttu-id="39833-105">_**Dernière modification de la rubrique :** 2014-05-14_</span><span class="sxs-lookup"><span data-stu-id="39833-105">_**Topic Last Modified:** 2014-05-14_</span></span>

<span data-ttu-id="39833-106">Vous pouvez utiliser les résultats d’une requête de recherche pour configurer des utilisateurs pour Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="39833-106">You can use the results of a search query to configure users for Lync Server 2013.</span></span> <span data-ttu-id="39833-107">Vous pouvez rechercher des utilisateurs par nom d’affichage, prénom, nom de famille, nom de compte SAM (Security Accounts Manager, Gestionnaire de comptes de sécurité), adresse SIP ou URI (Uniform Resource Identifier) de ligne.</span><span class="sxs-lookup"><span data-stu-id="39833-107">You can search for users by display name, first name, last name, Security Accounts Manager (SAM) account name, SIP address, or line Uniform Resource Identifier (URI).</span></span>

<span data-ttu-id="39833-108">Vous pouvez rechercher des utilisateurs à l’aide du panneau de configuration de Lync Server ou du composant logiciel enfichable utilisateurs et ordinateurs Active Directory.</span><span class="sxs-lookup"><span data-stu-id="39833-108">You can search for users by using the Lync Server Control Panel or the Active Directory Users and Computers snap-in.</span></span> <span data-ttu-id="39833-109">La procédure suivante vous explique comment utiliser le panneau de configuration de Lync Server pour rechercher des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="39833-109">The following procedure describes how to use Lync Server Control Panel to search for users.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="39833-110">Dans un environnement doté d’une topologie de forêt centrale, il est possible que les résultats de la recherche soient inexacts lorsque vous recherchez un utilisateur à l’aide de son adresse de messagerie.</span><span class="sxs-lookup"><span data-stu-id="39833-110">In an environment with a central forest topology, search results might not be accurate when you search for a user by the user’s email address.</span></span> <span data-ttu-id="39833-111">Au lieu de cela, vous pouvez rechercher des utilisateurs en spécifiant un préfixe d’adresse SIP (par exemple, SIP : nom), ajouter un filtre de recherche et sélectionner une adresse SIP contenant une adresse de messagerie partielle ou utiliser l’applet de requête <STRONG>Get-Csuser</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="39833-111">Instead, you can search for users by specifying a SIP address prefix, for example, sip:name, add a search filter and select a SIP address that contains a partial email address, or use the <STRONG>Get-CSUser</STRONG> cmdlet.</span></span>



</div>

<div>

## <a name="to-search-for-one-or-more-users"></a><span data-ttu-id="39833-112">Pour rechercher un ou plusieurs utilisateurs</span><span class="sxs-lookup"><span data-stu-id="39833-112">To search for one or more users</span></span>

1.  <span data-ttu-id="39833-113">À partir d’un compte d’utilisateur auquel est affecté le rôle CsUserAdministrator ou CsAdministrator, ouvrez une session sur un ordinateur de votre déploiement interne.</span><span class="sxs-lookup"><span data-stu-id="39833-113">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="39833-114">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="39833-114">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="39833-115">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="39833-115">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="39833-116">Dans la barre de navigation de gauche, cliquez sur **Utilisateurs**.</span><span class="sxs-lookup"><span data-stu-id="39833-116">In the left navigation bar, click **Users**.</span></span>

4.  <span data-ttu-id="39833-117">Dans la boîte de **recherche utilisateurs** , entrez tout ou la première partie du nom d’affichage, prénom, nom, nom de compte Sam, adresse SIP ou URI de ligne du compte d’utilisateur que vous souhaitez rechercher, puis cliquez sur **Rechercher**.</span><span class="sxs-lookup"><span data-stu-id="39833-117">In the **Search users** box, type all or the first portion of the display name, first name, last name, SAM account name, SIP address, or line URI of the user account that you want to search for, and then click **Find**.</span></span>

5.  <span data-ttu-id="39833-118">(Facultatif) Indiquez des critères de recherche supplémentaires pour affiner les résultats :</span><span class="sxs-lookup"><span data-stu-id="39833-118">(Optional) Specify additional search criteria to narrow the results:</span></span>
    
    1.  <span data-ttu-id="39833-119">Cliquez sur la flèche de développement située dans le coin supérieur droit de l’écran au-dessus des résultats de la **recherche**, puis cliquez sur **Ajouter un filtre**.</span><span class="sxs-lookup"><span data-stu-id="39833-119">Click the expand arrow button in the upper-right corner of the screen above **Search results**, and then click **Add Filter**.</span></span>
    
    2.  <span data-ttu-id="39833-120">Entrez la propriété User en le tapant ou en cliquant sur la flèche dans la liste déroulante pour sélectionner une propriété d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="39833-120">Enter the user property by typing it or clicking the arrow in the drop-down list to select a user property.</span></span>
    
    3.  <span data-ttu-id="39833-121">Dans la liste **égal à** , cliquez sur **égal à** ou **n’est pas égal à**.</span><span class="sxs-lookup"><span data-stu-id="39833-121">In the **Equal to** list, click **Equal to** or **Not equal to**.</span></span>
    
    4.  <span data-ttu-id="39833-122">Dans la zone de texte, tapez les critères de recherche que vous voulez utiliser pour filtrer les résultats de recherche, puis cliquez sur **Rechercher**.</span><span class="sxs-lookup"><span data-stu-id="39833-122">In the text box, type the search criteria you want to use to filter search results, and then click **Find**.</span></span>

6.  <span data-ttu-id="39833-123">Les résultats de la recherche apparaissent sous résultats de la **recherche**.</span><span class="sxs-lookup"><span data-stu-id="39833-123">The search results appear under **Search Results**.</span></span> <span data-ttu-id="39833-124">Vous pouvez sélectionner tout ou partie des utilisateurs de la liste et effectuer des tâches de configuration pour les utilisateurs sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="39833-124">You can select any or all of the users in the list and perform configuration tasks on the users you select.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="39833-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="39833-125">See Also</span></span>


[<span data-ttu-id="39833-126">Affichage d’informations sur les comptes d’utilisateurs activés pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="39833-126">Viewing information about user accounts enabled for Lync Server 2013</span></span>](lync-server-2013-viewing-information-about-user-accounts-enabled-for-lync-server.md)  
[<span data-ttu-id="39833-127">Activation et désactivation des utilisateurs pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="39833-127">Enabling and disabling users for Lync Server 2013</span></span>](lync-server-2013-enabling-and-disabling-users-for-lync-server.md)  
  

<span data-ttu-id="39833-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="39833-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

