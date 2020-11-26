---
title: Installation des systèmes d’exploitaition et des logiciels prérequis sur les serveurs
description: Installation de systèmes d’exploitation et logiciels prérequis sur des serveurs.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Install operating systems and prerequisite software on servers
ms:assetid: 055991e0-5aeb-43fc-a7ba-d4b02316d73b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398103(v=OCS.15)
ms:contentKeyID: 48183288
ms.date: 07/24/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2bae9e57db9c2f1d3f3bde7ce9cc7071b73aa01d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427172"
---
# <a name="install-operating-systems-and-prerequisite-software-on-servers-for-lync-server-2013"></a><span data-ttu-id="e256c-103">Installation des systèmes d’exploitaition et des logiciels prérequis sur les serveurs pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e256c-103">Install operating systems and prerequisite software on servers for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e256c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e256c-104">

<span> </span></span></span>

<span data-ttu-id="e256c-105">_**Dernière modification de la rubrique :** 2014-07-24_</span><span class="sxs-lookup"><span data-stu-id="e256c-105">_**Topic Last Modified:** 2014-07-24_</span></span>

<span data-ttu-id="e256c-106">Après avoir configuré l’infrastructure matérielle et système, vous devez installer les systèmes d’exploitation Windows appropriés et les mises à jour, en plus de tous les autres logiciels requis sur chaque serveur que vous déployez.</span><span class="sxs-lookup"><span data-stu-id="e256c-106">After you have set up the hardware and system infrastructure, you need to install the appropriate Windows operating systems and updates, in addition to all other prerequisite software on each server that you are deploying.</span></span> <span data-ttu-id="e256c-107">Cela comprend chaque rôle serveur Lync Server 2013 et les serveurs d’infrastructure supplémentaires qui exécutent SQL Server qui sont requis pour votre déploiement.</span><span class="sxs-lookup"><span data-stu-id="e256c-107">This includes each Lync Server 2013 server role and any additional infrastructure servers or servers running SQL Server that are required for your deployment.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="e256c-108">Cette section décrit l’installation de systèmes d’exploitation et logiciels prérequis pour les serveurs internes.</span><span class="sxs-lookup"><span data-stu-id="e256c-108">This section describes installation of operating systems and prerequisite software for internal servers.</span></span> <span data-ttu-id="e256c-109">Si vous déployez des serveurs Edge pour prendre en charge l’accès utilisateur externe, vous devez également installer les systèmes d’exploitation et les logiciels requis pour ces serveurs, y compris les serveurs de périphérie et les serveurs proxy inverse.</span><span class="sxs-lookup"><span data-stu-id="e256c-109">If you are deploying Edge Servers to support external user access, you also need to install operating systems and prerequisite software for those servers, including Edge Servers and reverse proxy servers.</span></span> <span data-ttu-id="e256c-110">Pour plus d’informations sur la façon de préparer des serveurs pour prendre en charge l’accès utilisateur externe, voir préparation de l' <A href="lync-server-2013-preparing-for-installation-of-servers-in-the-perimeter-network.md">installation de serveurs dans le réseau de périmètre pour Lync Server 2013</A> dans la documentation de déploiement.</span><span class="sxs-lookup"><span data-stu-id="e256c-110">For details about preparing servers to support external user access, see <A href="lync-server-2013-preparing-for-installation-of-servers-in-the-perimeter-network.md">Preparing for installation of servers in the perimeter network for Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<div>

## <a name="install-windows-operating-systems-on-servers"></a><span data-ttu-id="e256c-111">Installer des systèmes d’exploitation Windows sur des serveurs</span><span class="sxs-lookup"><span data-stu-id="e256c-111">Install Windows Operating Systems on Servers</span></span>

<span data-ttu-id="e256c-112">Sur chaque serveur que vous déployez, installez le système d’exploitation Windows approprié en procédant comme suit :</span><span class="sxs-lookup"><span data-stu-id="e256c-112">On each server that you are deploying, install the appropriate Windows operating system as follows:</span></span>

  - <span data-ttu-id="e256c-113">**Serveurs exécutant Lync Server 2013**   Pour plus d’informations sur la configuration requise du système d’exploitation pour les serveurs exécutant Lync Server 2013, voir [prise en charge du système d’exploitation serveur et outils dans Lync server 2013](lync-server-2013-server-and-tools-operating-system-support.md) dans la documentation de prise en charge.</span><span class="sxs-lookup"><span data-stu-id="e256c-113">**Servers running Lync Server 2013**   For details about the operating system requirements for servers running Lync Server 2013, see [Server and tools operating system support in Lync Server 2013](lync-server-2013-server-and-tools-operating-system-support.md) in the Supportability documentation.</span></span>

  - <span data-ttu-id="e256c-114">**Serveurs de base de données**   Pour plus d’informations sur la configuration système requise pour les serveurs de base de données, y compris la base de données principale, la base de données d’archivage et la base de données de surveillance, voir la documentation SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e256c-114">**Database servers**   For details about operating system requirements for database servers, including the back-end database, Archiving database, and Monitoring database, see the SQL Server documentation.</span></span> <span data-ttu-id="e256c-115">Pour SQL Server 2012, consultez la documentation SQL Server 2012 en ligne à l’adresse [https://go.microsoft.com/fwlink/p/?linkId=218015](https://go.microsoft.com/fwlink/p/?linkid=218015) .</span><span class="sxs-lookup"><span data-stu-id="e256c-115">For SQL Server 2012, see the SQL Server 2012 Books Online at [https://go.microsoft.com/fwlink/p/?linkId=218015](https://go.microsoft.com/fwlink/p/?linkid=218015).</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="e256c-116">Si vous installez Lync Server 2013 sur Windows Server &nbsp; 2008 &nbsp; R2 avec SP1, vous devez commencer par installer la mise à jour décrite dans l’article 2646886 de la base de connaissances Microsoft, « correctif : corruption du tas se produit lorsqu’un module appelle la méthode INSERTENTITYBODY dans IIS 7,5 », à <A class=uri href="https://go.microsoft.com/fwlink/p/?linkid=3052%26kbid=2646886"> https://go.microsoft.com/fwlink/p/?linkid=3052&amp ; kbid = 2646886</A>.</span><span class="sxs-lookup"><span data-stu-id="e256c-116">If you are installing Lync Server 2013 on Windows Server&nbsp;2008&nbsp;R2 with SP1, you must first install the update described in the Microsoft Knowledge Based article 2646886, “FIX: Heap corruption occurs when a module calls the InsertEntityBody method in IIS 7.5”, at <A class=uri href="https://go.microsoft.com/fwlink/p/?linkid=3052%26kbid=2646886">https://go.microsoft.com/fwlink/p/?linkid=3052&amp;kbid=2646886</A>.</span></span><BR><span data-ttu-id="e256c-117">Vous devez également modifier le registre comme décrit dans l’article de la base de connaissances, les <A href="https://go.microsoft.com/fwlink/p/?linkid=506893">ID d’événement 32402 et 61045 sont enregistrés dans les serveurs frontaux Lync Server 2013 installés dans Windows Server 2012 R2</A>.</span><span class="sxs-lookup"><span data-stu-id="e256c-117">You must also modify the registry as described in the KB article, <A href="https://go.microsoft.com/fwlink/p/?linkid=506893">Event IDs 32402, 61045 are logged in Lync Server 2013 Front End servers that are installed in Windows Server 2012 R2</A>.</span></span>



</div>

</div>

<div>

## <a name="install-windows-update-on-servers"></a><span data-ttu-id="e256c-118">Installer Windows Update sur les serveurs</span><span class="sxs-lookup"><span data-stu-id="e256c-118">Install Windows Update on Servers</span></span>

<span data-ttu-id="e256c-119">Installez les mises à jour suivantes à partir de Windows Update sur chaque serveur :</span><span class="sxs-lookup"><span data-stu-id="e256c-119">Install the following updates from Windows Update on each server:</span></span>

  - <span data-ttu-id="e256c-120">**Windows Update pour les serveurs exécutant Lync Server 2013**   Pour plus d’informations sur les mises à jour de Windows Update requises pour les serveurs exécutant Lync Server 2013, voir [configuration logicielle requise supplémentaire pour Lync Server 2013](lync-server-2013-additional-software-requirements.md) dans la documentation de planification.</span><span class="sxs-lookup"><span data-stu-id="e256c-120">**Windows Update for servers running Lync Server 2013**   For details about the updates from Windows Update that are required for servers running Lync Server 2013, see [Additional software requirements for Lync Server 2013](lync-server-2013-additional-software-requirements.md) in the Planning documentation.</span></span>

  - <span data-ttu-id="e256c-121">**Serveurs de base de données**   Pour plus d’informations sur les mises à jour de Windows Update requises pour les serveurs de base de données, y compris la base de données principale, la base de données d’archivage et la base de données de surveillance, voir la documentation SQL Server 2012.</span><span class="sxs-lookup"><span data-stu-id="e256c-121">**Database servers**   For details about the updates from Windows Update that are required for database servers, including the back-end database, Archiving database, and Monitoring database, see the SQL Server 2012 documentation.</span></span> <span data-ttu-id="e256c-122">Pour SQL Server 2012, consultez la documentation SQL Server 2012 en ligne à l’adresse [https://go.microsoft.com/fwlink/p/?linkId=218015](https://go.microsoft.com/fwlink/p/?linkid=218015) .</span><span class="sxs-lookup"><span data-stu-id="e256c-122">For SQL Server 2012, see the SQL Server 2012 Books Online at [https://go.microsoft.com/fwlink/p/?linkId=218015](https://go.microsoft.com/fwlink/p/?linkid=218015).</span></span>

</div>

<div>

## <a name="install-other-prerequisite-software-on-servers"></a><span data-ttu-id="e256c-123">Installer d’autres logiciels prérequis sur des serveurs</span><span class="sxs-lookup"><span data-stu-id="e256c-123">Install Other Prerequisite Software on Servers</span></span>

<span data-ttu-id="e256c-124">Lync Server 2013 nécessite l’installation des logiciels supplémentaires suivants sur les serveurs :</span><span class="sxs-lookup"><span data-stu-id="e256c-124">Lync Server 2013 requires the installation of the following additional software on servers:</span></span>

  - <span data-ttu-id="e256c-125">**Logiciels requis pour les serveurs exécutant Lync Server 2013**   Les logiciels requis supplémentaires pour les serveurs exécutant Lync Server 2013 dépendent du rôle de serveur déployé.</span><span class="sxs-lookup"><span data-stu-id="e256c-125">**Prerequisite software for servers running Lync Server 2013**   The additional software prerequisites for servers running Lync Server 2013 depend on the server role being deployed.</span></span> <span data-ttu-id="e256c-126">Pour en savoir plus sur la configuration logicielle requise pour chaque serveur, voir [configuration logicielle requise pour Lync server 2013](lync-server-2013-additional-software-requirements.md) dans la documentation de planification.</span><span class="sxs-lookup"><span data-stu-id="e256c-126">For details about the specific software requirements for each server, see [Additional software requirements for Lync Server 2013](lync-server-2013-additional-software-requirements.md) in the Planning documentation.</span></span>

  - <span data-ttu-id="e256c-127">**Windows Identity Foundation**   Pour pouvoir prendre en charge les scénarios d’authentification de serveur à serveur, Lync Server 2013 nécessite l’installation de Windows Identity Foundation.</span><span class="sxs-lookup"><span data-stu-id="e256c-127">**Windows Identity Foundation**   Lync Server 2013 requires the installation of Windows Identity Foundation in order to support server-to-server authentication scenarios.</span></span> <span data-ttu-id="e256c-128">Pour vérifier qu’il est déjà installé sur votre ordinateur, accédez au panneau de configuration, cliquez sur **programmes et fonctionnalités**, **consultez les mises à jour installées** et Regardez sous **Microsoft Windows**.</span><span class="sxs-lookup"><span data-stu-id="e256c-128">To verify that it has already been installed on your computer, go to Control Panel, click **Programs and Features**, **View installed updates**, and look under **Microsoft Windows**.</span></span> <span data-ttu-id="e256c-129">Pour plus d’informations sur l’installation de Windows Identity Foundation, voir [https://go.microsoft.com/fwlink/p/?linkId=204657](https://go.microsoft.com/fwlink/p/?linkid=204657) .</span><span class="sxs-lookup"><span data-stu-id="e256c-129">For details about installing Windows Identity Foundation, see [https://go.microsoft.com/fwlink/p/?linkId=204657](https://go.microsoft.com/fwlink/p/?linkid=204657).</span></span>

  - <span data-ttu-id="e256c-130">**Microsoft .NET Framework 4,5**   L’édition 64 bits de Microsoft .NET Framework 4,5 est requise pour Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e256c-130">**Microsoft .NET Framework 4.5**   The 64-bit edition of Microsoft .NET Framework 4.5 is required for Lync Server 2013.</span></span>

  - <span data-ttu-id="e256c-131">**Logiciels requis pour les serveurs de base de données**   Pour plus d’informations sur la mise à jour Windows requise pour les serveurs de base de données, y compris la base de données principale, la base de données d’archivage et la base de données de surveillance, voir la documentation SQL Server 2012 à l’adresse [https://go.microsoft.com/fwlink/p/?linkId=218015](https://go.microsoft.com/fwlink/p/?linkid=218015) .</span><span class="sxs-lookup"><span data-stu-id="e256c-131">**Prerequisite software for database servers**   For details about the Windows Update required for database servers, including the back-end database, Archiving database, and Monitoring database, see the SQL Server 2012 documentation at [https://go.microsoft.com/fwlink/p/?linkId=218015](https://go.microsoft.com/fwlink/p/?linkid=218015).</span></span>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="e256c-132">Lync Server 2013 installe automatiquement Microsoft SQL Server 2012 Express sur chaque serveur Standard Edition et chaque serveur exécutant Lync Server 2013 sur lequel se trouve le magasin de configurations local.</span><span class="sxs-lookup"><span data-stu-id="e256c-132">Lync Server 2013 automatically installs Microsoft SQL Server 2012 Express on each Standard Edition server and each server running Lync Server 2013 on which the local configuration store is located.</span></span>

    
    </div>

  - <span data-ttu-id="e256c-133">**Windows Media Format Runtime**   Tout serveur frontal et serveur Standard Edition sur lequel les conférences seront déployées doit avoir installé le runtime format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e256c-133">**Windows Media Format Runtime**   All Front End Servers and Standard Edition servers where conferencing will be deployed must have the Windows Media Format Runtime installed.</span></span> <span data-ttu-id="e256c-134">Le runtime du format Windows Media est requis pour l’exécution des fichiers Windows Media audio (. WMA) que les applications de parc d’appels, d’annonce et de Response Group sont lues pour les annonces et la musique.</span><span class="sxs-lookup"><span data-stu-id="e256c-134">The Windows Media Format Runtime is required to run the Windows Media Audio (.wma) files that the Call Park, Announcement, and Response Group applications play for announcements and music.</span></span>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="e256c-135">Pour Windows Server 2012 et Windows Server 2012 R2, le runtime Windows Media Format Runtime s’installe avec Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="e256c-135">For Windows Server 2012 and Windows Server 2012 R2 the Windows Media Format Runtime installs with Microsoft Media Foundation.</span></span>

    
    </div>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="e256c-136">Pour Windows Server &nbsp; 2008 et Windows server &nbsp; 2008 &nbsp; R2, le runtime du format Windows Media est installé dans le cadre de l’expérience de bureau Windows.</span><span class="sxs-lookup"><span data-stu-id="e256c-136">For Windows Server&nbsp;2008 and Windows Server&nbsp;2008&nbsp;R2 the Windows Media Format Runtime installs as part of the Windows Desktop Experience.</span></span> <span data-ttu-id="e256c-137">Nous vous recommandons d’installer la version de bureau de Windows avant d’installer Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e256c-137">It is recommended that you install Windows Desktop Experience before you install Lync Server 2013.</span></span> <span data-ttu-id="e256c-138">Si Lync Server 2013 ne trouve pas ce logiciel sur le serveur, il vous invite à l’installer, puis vous devez redémarrer le serveur pour terminer l’installation.</span><span class="sxs-lookup"><span data-stu-id="e256c-138">If Lync Server 2013 does not find this software on the server, it will prompt you to install it, and then you must restart the server to complete installation.</span></span>

    
    <span data-ttu-id="e256c-139"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e256c-139"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

