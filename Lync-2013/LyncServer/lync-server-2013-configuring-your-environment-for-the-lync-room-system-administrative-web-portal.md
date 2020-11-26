---
title: 'Lync Server 2013 : Configuration de votre environnement pour le portail web d’administration de Lync Room System'
description: 'Lync Server 2013 : configuration de votre environnement pour le portail Web d’administration du système de salle Lync.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring your environment for the Lync Room System Administrative Web Portal
ms:assetid: 1bf3cc55-cfa8-46ee-a8bc-6dab3bff76b2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn436325(v=OCS.15)
ms:contentKeyID: 56737623
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c942e1db799a7336a3eafb5571e82584694ddbf3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432292"
---
# <a name="configuring-your-lync-server-2013-environment-for-the-lync-room-system-administrative-web-portal"></a><span data-ttu-id="af673-103">Configuring your Lync Server 2013 environment for the Lync Room System Administrative Web Portal</span><span class="sxs-lookup"><span data-stu-id="af673-103">Configuring your Lync Server 2013 environment for the Lync Room System Administrative Web Portal</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="af673-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="af673-104">

<span> </span></span></span>

<span data-ttu-id="af673-105">_**Dernière modification de la rubrique :** 2014-05-22_</span><span class="sxs-lookup"><span data-stu-id="af673-105">_**Topic Last Modified:** 2014-05-22_</span></span>

<span data-ttu-id="af673-106">Pour utiliser le portail Web d’administration LRS (Lync Room System), vous devez installer ou configurer les éléments requis suivants.</span><span class="sxs-lookup"><span data-stu-id="af673-106">To use the Lync Room System (LRS) Administrative Web Portal, you will need to install or configure the following prerequisites.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="af673-107">Si le serveur est configuré à l’aide de l’authentification Kerberos et NTLM et qu’LRS s’exécute sur un ordinateur qui n’est pas joint au domaine, l’authentification Kerberos échoue et l’utilisateur ne verra pas l’état de LRS dans le portail d’administration.</span><span class="sxs-lookup"><span data-stu-id="af673-107">If the server is configured with both Kerberos and NTLM authentication, and LRS is running on a computer that is not joined to the domain, Kerberos authentication will fail and the user will not see the status of LRS in the administrative portal.</span></span> <span data-ttu-id="af673-108">Pour résoudre ce problème, configurez le serveur à l’aide de l’authentification NTLM ou de l’authentification NTLM et TLS-DSK (sans Kerberos), ou joignez l’ordinateur LRS au domaine.</span><span class="sxs-lookup"><span data-stu-id="af673-108">To resolve this issue, configure the server with NTLM authentication or both NTLM and TLS-DSK authentication (without Kerberos), or join the LRS computer to the domain.</span></span>



</div>

1.  <span data-ttu-id="af673-109">Installez les mises à jour cumulatives de Lync Server 2013 : juillet 2013 dans la topologie du serveur Lync.</span><span class="sxs-lookup"><span data-stu-id="af673-109">Install Lync Server 2013 Cumulative Updates: July 2013 in the Lync Server topology.</span></span>
    
    <span data-ttu-id="af673-110">Pour obtenir la mise à jour ou découvrir ce qu’elle contient, voir [mises à jour de Lync Server 2013](https://go.microsoft.com/fwlink/p/?linkid=323959).</span><span class="sxs-lookup"><span data-stu-id="af673-110">To get the update or see what’s included with it, see [Updates for Lync Server 2013](https://go.microsoft.com/fwlink/p/?linkid=323959).</span></span>

2.  <span data-ttu-id="af673-111">Créez un utilisateur Active Directory activé pour SIP.</span><span class="sxs-lookup"><span data-stu-id="af673-111">Create a SIP-enabled Active Directory user.</span></span>
    
    <span data-ttu-id="af673-112">Le portail Web d’administration LRS utilise ces informations d’identification pour interroger les informations de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="af673-112">The LRS Administrative Web Portal uses these credentials to query information from Lync Server.</span></span> <span data-ttu-id="af673-113">Le nom d’utilisateur recommandé est LRSApp.</span><span class="sxs-lookup"><span data-stu-id="af673-113">The recommended username is LRSApp.</span></span>

3.  <span data-ttu-id="af673-114">Créez un groupe de sécurité Active Directory nommé LRSSupportAdminGroup.</span><span class="sxs-lookup"><span data-stu-id="af673-114">Create an Active Directory security group with name LRSSupportAdminGroup.</span></span>
    
    <span data-ttu-id="af673-p103">Créez le groupe avec une étendue globale et le type Sécurité. Les utilisateurs activés pour SIP ajoutés à ce groupe seront autorisés à afficher la liste des pièces et à exécuter certaines commandes, telles que la collecte de journaux.</span><span class="sxs-lookup"><span data-stu-id="af673-p103">Create the group with Group Scope as Global and Group Type as Security. SIP enabled users who are added to this group will be authorized to see the list of rooms and execute certain commands, such as collecting logs.</span></span>

4.  <span data-ttu-id="af673-117">Créez un groupe de sécurité Active Directory nommé LRSFullAccessAdminGroup. </span><span class="sxs-lookup"><span data-stu-id="af673-117">Create an Active Directory security group with name LRSFullAccessAdminGroup.</span></span>
    
    <span data-ttu-id="af673-118">Pour pouvoir utiliser la fonctionnalité de portail d’administration, vous pouvez créer le groupe avec l’étendue du groupe en tant que type global et de groupe.</span><span class="sxs-lookup"><span data-stu-id="af673-118">Create the group with Group Scope as Global and Group Type as Security.SIP enabled users who are added to this group are authorized to use all admin portal functionality.</span></span>
    
     
    
    <span data-ttu-id="af673-119">![Liste des groupes d’administrateurs avec rôle de groupe de sécurité](images/Dn436325.5d432819-a2e2-452c-bc2a-5d4ee79d8c33(OCS.15).png "Liste des groupes d’administrateurs avec rôle de groupe de sécurité")</span><span class="sxs-lookup"><span data-stu-id="af673-119">![List of Admin Groups with security group role](images/Dn436325.5d432819-a2e2-452c-bc2a-5d4ee79d8c33(OCS.15).png "List of Admin Groups with security group role")</span></span>  
    
     

5.  <span data-ttu-id="af673-120">Ajoutez LRSFullAccessAdminGroup en tant que membre de LRSSupportAdminGroup.</span><span class="sxs-lookup"><span data-stu-id="af673-120">Add LRSFullAccessAdminGroup as a member of LRSSupportAdminGroup.</span></span>
    
    <span data-ttu-id="af673-121">![Page des membres des propriétés LRSSupportAdminGroup](images/Dn436325.91a4a28a-cacf-4ef6-aac1-915ec41c9648(OCS.15).png "Page des membres des propriétés LRSSupportAdminGroup")</span><span class="sxs-lookup"><span data-stu-id="af673-121">![LRSSupportAdminGroup Properties Members page](images/Dn436325.91a4a28a-cacf-4ef6-aac1-915ec41c9648(OCS.15).png "LRSSupportAdminGroup Properties Members page")</span></span>  
    
     

6.  <span data-ttu-id="af673-122">Créez un utilisateur Active Directory activé pour SIP avec le nom LRSSupport.</span><span class="sxs-lookup"><span data-stu-id="af673-122">Create a SIP enabled Active Directory user with name LRSSupport.</span></span> <span data-ttu-id="af673-123">Ajoutez cet utilisateur au groupe LRSSupportAdminGroup.</span><span class="sxs-lookup"><span data-stu-id="af673-123">Add this user to LRSSupportAdminGroup.</span></span>
    
    <span data-ttu-id="af673-124">![Page des membres des propriétés LRSSupportAdminGroup](images/Dn436325.7638055d-22ac-4909-914d-1966f5623909(OCS.15).png "Page des membres des propriétés LRSSupportAdminGroup")</span><span class="sxs-lookup"><span data-stu-id="af673-124">![LRSSupportAdminGroup Properties Members page](images/Dn436325.7638055d-22ac-4909-914d-1966f5623909(OCS.15).png "LRSSupportAdminGroup Properties Members page")</span></span>  
    
     

7.  <span data-ttu-id="af673-125">Installez ASP.NET MVC 4 pour Visual Studio 2010 SP1 et Visual Web Developer 2010 SP1, disponible dans le centre de téléchargement Microsoft à l’adresse [https://go.microsoft.com/fwlink/p/?LinkId=323967](https://go.microsoft.com/fwlink/p/?linkid=323967) .</span><span class="sxs-lookup"><span data-stu-id="af673-125">Install ASP.NET MVC 4 for Visual Studio 2010 SP1 and Visual Web Developer 2010 SP1, available in the Microsoft Download Center at [https://go.microsoft.com/fwlink/p/?LinkId=323967](https://go.microsoft.com/fwlink/p/?linkid=323967).</span></span>

<span data-ttu-id="af673-126"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="af673-126"></div>

<span> </span>

</div>

</div>

</span></span></div>

