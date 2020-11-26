---
title: 'Lync Server 2013 : Autre configuration logicielle requise'
description: 'Lync Server 2013 : exigences logicielles supplémentaires.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Additional software requirements
ms:assetid: 87b318e3-03ae-41f7-af5e-29bb294f6af0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398686(v=OCS.15)
ms:contentKeyID: 48184731
ms.date: 12/09/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fbc36f23a2246c9d653e47954064182c756f0dff
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443152"
---
# <a name="additional-software-requirements-for-lync-server-2013"></a><span data-ttu-id="c216c-103">Autre configuration logicielle requise pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c216c-103">Additional software requirements for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c216c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c216c-104">

<span> </span></span></span>

<span data-ttu-id="c216c-105">_**Dernière modification de la rubrique :** 2016-12-08_</span><span class="sxs-lookup"><span data-stu-id="c216c-105">_**Topic Last Modified:** 2016-12-08_</span></span>

<span data-ttu-id="c216c-106">Outre le matériel et les exigences en matière de système d’exploitation pour les plates-formes serveur, Lync Server 2013 nécessite l’installation de logiciels supplémentaires sur les serveurs que vous déployez.</span><span class="sxs-lookup"><span data-stu-id="c216c-106">In addition to the hardware and operating system requirements for server platforms, Lync Server 2013 requires the installation of additional software on the servers that you deploy.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="c216c-107">Pour plus d’informations sur la configuration requise pour la plateforme pour les serveurs exécutant Lync Server, voir <A href="lync-server-2013-server-hardware-platforms.md">plates-formes matérielles pour Lync server 2013</A> et <A href="lync-server-2013-server-and-tools-operating-system-support.md">serveur et outils pris en charge dans Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="c216c-107">For details about the platform requirements for servers running Lync Server, see <A href="lync-server-2013-server-hardware-platforms.md">Server hardware platforms for Lync Server 2013</A> and <A href="lync-server-2013-server-and-tools-operating-system-support.md">Server and tools operating system support in Lync Server 2013</A>.</span></span> <span data-ttu-id="c216c-108">Pour plus d’informations sur la configuration système requise pour les ordinateurs et appareils clients, voir <A href="lync-server-2013-planning-for-clients-and-devices.md">planification des clients et des appareils dans Lync Server 2013</A> dans la documentation de planification.</span><span class="sxs-lookup"><span data-stu-id="c216c-108">For details about system requirements for client computers and devices, see <A href="lync-server-2013-planning-for-clients-and-devices.md">Planning for clients and devices in Lync Server 2013</A> in the Planning documentation.</span></span> <span data-ttu-id="c216c-109">Pour plus d’informations sur la configuration logicielle requise pour les outils d’administration, consultez la <A href="lync-server-2013-administrative-tools-software-requirements.md">configuration logicielle requise pour les outils d’administration dans Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="c216c-109">For details about software requirements for administrative tools, see <A href="lync-server-2013-administrative-tools-software-requirements.md">Administrative tools software requirements in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="additional-software-necessary-for-all-internal-server-roles"></a><span data-ttu-id="c216c-110">Logiciel supplémentaire nécessaire pour tous les rôles de serveur internes</span><span class="sxs-lookup"><span data-stu-id="c216c-110">Additional Software Necessary for All Internal Server Roles</span></span>

<span data-ttu-id="c216c-111">Cette section répertorie les logiciels nécessaires sur tous les rôles de serveur interne, à l’exception des rôles serveur Edge.</span><span class="sxs-lookup"><span data-stu-id="c216c-111">This section lists software necessary on all internal server roles, which are all Lync Server server roles except for Edge Server.</span></span> <span data-ttu-id="c216c-112">La configuration requise pour les serveurs Edge et les pools Edge est répertoriée plus loin dans cette rubrique sous **logiciels supplémentaires pour les serveurs de périphérie**.</span><span class="sxs-lookup"><span data-stu-id="c216c-112">The requirements for the Edge Servers and Edge pools are listed later in this topic under **Additional Software for Edge Servers**.</span></span>

</div>

<div>

## <a name="windows-powershell-30"></a><span data-ttu-id="c216c-113">Windows PowerShell 3.0</span><span class="sxs-lookup"><span data-stu-id="c216c-113">Windows PowerShell 3.0</span></span>

<span data-ttu-id="c216c-114">Chaque serveur exécutant Lync Server 2013 doit avoir installé la version appropriée de Windows PowerShell 3,0.</span><span class="sxs-lookup"><span data-stu-id="c216c-114">Each server running Lync Server 2013 must have the correct release of Windows PowerShell 3.0 installed.</span></span> <span data-ttu-id="c216c-115">Pour plus d’informations, consultez [installation de Windows PowerShell 3,0 pour Lync Server 2013](lync-server-2013-installing-windows-powershell-3-0.md).</span><span class="sxs-lookup"><span data-stu-id="c216c-115">For details, see [Installing Windows PowerShell 3.0 for Lync Server 2013](lync-server-2013-installing-windows-powershell-3-0.md).</span></span>

</div>

<div>

## <a name="microsoft-net-framework-45"></a><span data-ttu-id="c216c-116">Microsoft .NET Framework 4.5</span><span class="sxs-lookup"><span data-stu-id="c216c-116">Microsoft .NET Framework 4.5</span></span>

<span data-ttu-id="c216c-117">Le serveur Lync nécessite Microsoft .NET Framework 4,5 sur tous les rôles de serveur interne et sur les ordinateurs sur lesquels vous allez exécuter les outils d’administration de Lync Server ou Microsoft Lync Server 2013, outil de planification.</span><span class="sxs-lookup"><span data-stu-id="c216c-117">Lync Server requires Microsoft .NET Framework 4.5 on all internal server roles and on any computer where you will run the Lync Server administrative tools or Microsoft Lync Server 2013, Planning Tool.</span></span> <span data-ttu-id="c216c-118">Pour Lync Server 2013, vous devez installer manuellement l’édition 64 bits de Microsoft .NET Framework 4,5 sur le serveur avant de procéder à l’installation de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c216c-118">For Lync Server 2013, you must manually install the 64-bit edition of Microsoft .NET Framework 4.5 on the server prior to installing Lync Server 2013.</span></span> <span data-ttu-id="c216c-119">Pour l’installer manuellement, téléchargez l’infrastructure Microsoft .NET 4,5 à partir du centre de téléchargement Microsoft sur [https://go.microsoft.com/fwlink/p/?LinkId=268529](https://go.microsoft.com/fwlink/p/?linkid=268529)</span><span class="sxs-lookup"><span data-stu-id="c216c-119">To manually install it, download the Microsoft .NET 4.5 Framework from the Microsoft Download Center at [https://go.microsoft.com/fwlink/p/?LinkId=268529](https://go.microsoft.com/fwlink/p/?linkid=268529)</span></span>

<div>

## <a name="installing-microsoft-net-framework-45-on-servers-running-windows-server-2012"></a><span data-ttu-id="c216c-120">Installation de Microsoft .NET Framework 4,5 sur des serveurs exécutant Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c216c-120">Installing Microsoft .NET Framework 4.5 on Servers Running Windows Server 2012</span></span>

<span data-ttu-id="c216c-121">Lorsque vous installez Microsoft .NET Framework 4,5 sur des serveurs exécutant Lync Server 2013 et Windows Server 2012, vous devez effectuer une étape supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="c216c-121">When you install Microsoft .NET Framework 4.5 on servers that will run Lync Server 2013 and Windows Server 2012, you must perform one additional step.</span></span> <span data-ttu-id="c216c-122">Après avoir installé .NET Framework 4,5, utilisez le gestionnaire de serveur pour installer l’activation HTTP.</span><span class="sxs-lookup"><span data-stu-id="c216c-122">After .NET Framework 4.5 is installed, use Server Manager to install HTTP Activation.</span></span>

<span data-ttu-id="c216c-123">**Pour installer l’activation HTTP de .NET 4,5 sur Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c216c-123">**To Install .NET 4.5 HTTP Activation on Windows Server 2012**</span></span>

1.  <span data-ttu-id="c216c-124">Dans le menu **Démarrer** , cliquez sur **programmes**, sur **Outils d’administration**, puis sur gestionnaire de **serveur**.</span><span class="sxs-lookup"><span data-stu-id="c216c-124">From the **Start** menu, click **Programs**, then click **Administrative Tools**, then click **Server Manager**.</span></span>

2.  <span data-ttu-id="c216c-125">Dans le gestionnaire de serveur, sous **fonctionnalités récapitulatives**, sélectionnez **Ajouter des fonctionnalités**.</span><span class="sxs-lookup"><span data-stu-id="c216c-125">In Server Manager, under **Features Summary**, choose **Add Features**.</span></span>

3.  <span data-ttu-id="c216c-126">Développez **.NET Framework 4,5**.</span><span class="sxs-lookup"><span data-stu-id="c216c-126">Expand **.NET Framework 4.5**.</span></span>

4.  <span data-ttu-id="c216c-127">Sélectionnez **activation WCF** si ce n’est pas déjà fait.</span><span class="sxs-lookup"><span data-stu-id="c216c-127">Select **WCF Activation** if it isn’t already selected.</span></span> <span data-ttu-id="c216c-128">Ensuite, sélectionnez **activation http**.</span><span class="sxs-lookup"><span data-stu-id="c216c-128">Then select **HTTP Activation**.</span></span>

5.  <span data-ttu-id="c216c-129">Cliquez sur **suivant** et suivez les invites pour terminer l’installation.</span><span class="sxs-lookup"><span data-stu-id="c216c-129">Click **Next** and follow the prompts to finish the installation.</span></span>

</div>

</div>

<div>

## <a name="windows-identity-foundation"></a><span data-ttu-id="c216c-130">Windows Identity Foundation</span><span class="sxs-lookup"><span data-stu-id="c216c-130">Windows Identity Foundation</span></span>

<span data-ttu-id="c216c-131">**Windows Identity Foundation** dans Lync Server 2013 nécessite l’installation de Windows Identity Foundation afin de prendre en charge les scénarios d’authentification de serveur à serveur.</span><span class="sxs-lookup"><span data-stu-id="c216c-131">**Windows Identity Foundation** in Lync Server 2013 requires the installation of Windows Identity Foundation in order to support server to server authentication scenarios.</span></span> <span data-ttu-id="c216c-132">Windows Server 2008 R2 et Windows Server 2012 nécessitent différentes procédures pour installer Windows identify Foundation.</span><span class="sxs-lookup"><span data-stu-id="c216c-132">Windows Server 2008 R2 and Windows Server 2012 require different procedures to install the Windows Identify Foundation.</span></span> <span data-ttu-id="c216c-133">Sélectionnez votre système d’exploitation serveur dans la liste suivante :</span><span class="sxs-lookup"><span data-stu-id="c216c-133">Select your server operating system from the following list:</span></span>

  - <span data-ttu-id="c216c-134">Windows Server 2008 R2 pour Windows Server 2008 R2, vous recherchez s’il a déjà été installé sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c216c-134">Windows Server 2008 R2   For Windows Server 2008 R2, you check to see if it has already been installed on your computer.</span></span> <span data-ttu-id="c216c-135">Pour ce faire, accédez à **Ajout/suppression de programmes**, **Affichez les mises à jour installées** et Regardez sous **Windows** pour l’entrée **Windows Identity Foundation (KB974405)**.</span><span class="sxs-lookup"><span data-stu-id="c216c-135">To do this, go to **Add/Remove Programs**, **View Installed Updates**, and look under **Windows** for the entry **Windows Identity Foundation (KB974405)**.</span></span> <span data-ttu-id="c216c-136">Pour plus d’informations sur l’installation de Windows Identity Foundation, voir [https://go.microsoft.com/fwlink/p/?linkId=204657](https://go.microsoft.com/fwlink/p/?linkid=204657) .</span><span class="sxs-lookup"><span data-stu-id="c216c-136">For details about installing Windows Identity Foundation, see [https://go.microsoft.com/fwlink/p/?linkId=204657](https://go.microsoft.com/fwlink/p/?linkid=204657).</span></span>

  - <span data-ttu-id="c216c-137">Windows Server 2012 pour Windows Server 2012, utilisez le **Gestionnaire de serveur** pour installer Windows Identity Foundation.</span><span class="sxs-lookup"><span data-stu-id="c216c-137">Windows Server 2012   For Windows Server 2012, you use **Server Manager** to install the Windows Identity Foundation.</span></span> <span data-ttu-id="c216c-138">Dans l' **Assistant Ajout de rôles et de fonctionnalités** du gestionnaire de serveur, sélectionnez **fonctionnalités**.</span><span class="sxs-lookup"><span data-stu-id="c216c-138">In the Server Manager **Add Roles and Features Wizard**, select **Features**.</span></span> <span data-ttu-id="c216c-139">Dans la liste, sélectionnez **Windows Identity Foundation 3,5** .</span><span class="sxs-lookup"><span data-stu-id="c216c-139">Select **Windows Identity Foundation 3.5** from the list.</span></span> <span data-ttu-id="c216c-140">Cliquez sur **suivant**, puis sur **installer**.</span><span class="sxs-lookup"><span data-stu-id="c216c-140">Click **Next**, then click **Install**.</span></span>

</div>

<div>

## <a name="additional-software-for-all-front-end-servers-and-standard-edition-servers"></a><span data-ttu-id="c216c-141">Logiciels supplémentaires pour tous les serveurs frontaux et les serveurs Standard Edition Server</span><span class="sxs-lookup"><span data-stu-id="c216c-141">Additional Software for All Front End Servers and Standard Edition Servers</span></span>

<span data-ttu-id="c216c-142">Tous les serveurs frontaux et les serveurs Standard Edition doivent également exécuter Internet Information Services (IIS) avec certains modules.</span><span class="sxs-lookup"><span data-stu-id="c216c-142">All Front End Servers and Standard Edition servers must also run Internet Information Services (IIS) with certain modules.</span></span> <span data-ttu-id="c216c-143">De plus, tous les serveurs frontaux et les serveurs Standard Edition dans lesquels les conférences, les applications de parc d’appel, les annonces ou les groupes de réponse sont déployés doivent exécuter Windows Media Format Runtime.</span><span class="sxs-lookup"><span data-stu-id="c216c-143">Additionally, all Front End Servers and Standard Edition servers where conferencing, Call Park application, Announcement, or Response Groups are deployed must run Windows Media Format Runtime.</span></span>

<div>

## <a name="internet-information-services-iis"></a><span data-ttu-id="c216c-144">services Internet (IIS)</span><span class="sxs-lookup"><span data-stu-id="c216c-144">Internet Information Services (IIS)</span></span>

<span data-ttu-id="c216c-145">Les serveurs frontaux et les serveurs Standard Edition doivent exécuter Internet Information Services (IIS), avec les modules suivants :</span><span class="sxs-lookup"><span data-stu-id="c216c-145">Front End Servers and Standard Edition servers must run Internet Information Services (IIS), with the following modules:</span></span>

  - <span data-ttu-id="c216c-146">Contenu statique</span><span class="sxs-lookup"><span data-stu-id="c216c-146">Static Content</span></span>

  - <span data-ttu-id="c216c-147">Document par défaut</span><span class="sxs-lookup"><span data-stu-id="c216c-147">Default Document</span></span>

  - <span data-ttu-id="c216c-148">Erreurs HTTP</span><span class="sxs-lookup"><span data-stu-id="c216c-148">HTTP Errors</span></span>

  - <span data-ttu-id="c216c-149">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="c216c-149">ASP.NET</span></span>

  - <span data-ttu-id="c216c-150">Extensibilité .NET</span><span class="sxs-lookup"><span data-stu-id="c216c-150">.NET Extensibility</span></span>

  - <span data-ttu-id="c216c-151">Extensions ISAPI (Internet Server API)</span><span class="sxs-lookup"><span data-stu-id="c216c-151">Internet Server API (ISAPI) Extensions</span></span>

  - <span data-ttu-id="c216c-152">Filtres ISAPI</span><span class="sxs-lookup"><span data-stu-id="c216c-152">ISAPI Filters</span></span>

  - <span data-ttu-id="c216c-153">Journalisation HTTP</span><span class="sxs-lookup"><span data-stu-id="c216c-153">HTTP Logging</span></span>

  - <span data-ttu-id="c216c-154">Outils de journalisation</span><span class="sxs-lookup"><span data-stu-id="c216c-154">Logging Tools</span></span>

  - <span data-ttu-id="c216c-155">Suivi</span><span class="sxs-lookup"><span data-stu-id="c216c-155">Tracing</span></span>

  - <span data-ttu-id="c216c-156">Authentification Windows</span><span class="sxs-lookup"><span data-stu-id="c216c-156">Windows Authentication</span></span>

  - <span data-ttu-id="c216c-157">Filtrage des demandes</span><span class="sxs-lookup"><span data-stu-id="c216c-157">Request Filtering</span></span>

  - <span data-ttu-id="c216c-158">Compression du contenu statique</span><span class="sxs-lookup"><span data-stu-id="c216c-158">Static Content Compression</span></span>

  - <span data-ttu-id="c216c-159">Compression du contenu dynamique</span><span class="sxs-lookup"><span data-stu-id="c216c-159">Dynamic Content Compression</span></span>

  - <span data-ttu-id="c216c-160">Console de gestion des services Internet (IIS)</span><span class="sxs-lookup"><span data-stu-id="c216c-160">IIS Management Console</span></span>

  - <span data-ttu-id="c216c-161">Scripts et outils de gestion des services Internet (IIS)</span><span class="sxs-lookup"><span data-stu-id="c216c-161">IIS Management Scripts and Tools</span></span>

  - <span data-ttu-id="c216c-162">Authentification anonyme (installée par défaut lors de l’installation d’IIS)</span><span class="sxs-lookup"><span data-stu-id="c216c-162">Anonymous Authentication (this is installed by default when IIS is installed.)</span></span>

  - <span data-ttu-id="c216c-163">Authentification par mappage de certificat client</span><span class="sxs-lookup"><span data-stu-id="c216c-163">Client Certificate Mapping Authentication</span></span>

</div>

<div>

## <a name="windows-media-format-runtime-and-windows-desktop-experience"></a><span data-ttu-id="c216c-164">Windows Media Format Runtime et expérience de bureau Windows</span><span class="sxs-lookup"><span data-stu-id="c216c-164">Windows Media Format Runtime and Windows Desktop Experience</span></span>

<span data-ttu-id="c216c-165">**Expérience de bureau Windows** Tout serveur frontal et serveur Standard Edition sur lequel les conférences seront déployées doit avoir installé le runtime format Windows Media, qui, à l’exception de Windows Server 2012, est installé dans le cadre de l’expérience de bureau Windows.</span><span class="sxs-lookup"><span data-stu-id="c216c-165">**Windows Desktop Experience** All Front End Servers and Standard Edition servers where conferencing will be deployed must have the Windows Media Format Runtime installed, which, except for Windows Server 2012 is installed as part of the Windows desktop experience.</span></span> <span data-ttu-id="c216c-166">Windows Server 2012 nécessite Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="c216c-166">Windows Server 2012 requires Microsoft Media Foundation.</span></span> <span data-ttu-id="c216c-167">Le runtime du format Windows Media est requis pour l’exécution des fichiers Windows Media audio (. WMA) que les applications de parc d’appels, d’annonce et de Response Group sont lues pour les annonces et la musique.</span><span class="sxs-lookup"><span data-stu-id="c216c-167">The Windows Media Format Runtime is required to run the Windows Media Audio (.wma) files that the Call Park, Announcement, and Response Group applications play for announcements and music.</span></span>

<span data-ttu-id="c216c-168">Nous vous recommandons d’installer l’expérience de bureau Windows avant d’installer Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c216c-168">We recommend that you install Windows desktop experience before you install Lync Server 2013.</span></span> <span data-ttu-id="c216c-169">Si Lync Server 2013 ne trouve pas ce logiciel sur le serveur, il vous invite à l’installer, puis vous devez redémarrer le serveur pour terminer l’installation.</span><span class="sxs-lookup"><span data-stu-id="c216c-169">If Lync Server 2013 does not find this software on the server, it will prompt you to install it, and then you must restart the server to complete installation.</span></span>

</div>

</div>

<div>

## <a name="additional-software-for-front-end-servers-and-standard-edition-servers-running-on-windows-server-2012"></a><span data-ttu-id="c216c-170">Logiciels supplémentaires pour les serveurs frontaux et les serveurs Standard Edition Server fonctionnant sous Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c216c-170">Additional Software for Front End Servers and Standard Edition Servers Running on Windows Server 2012</span></span>

<span data-ttu-id="c216c-171">Les serveurs frontaux requièrent .NET 3,5, qui n’est pas installé par défaut sur Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="c216c-171">Front End Servers require .NET 3.5, which is not installed by default on Windows Server 2012.</span></span> <span data-ttu-id="c216c-172">Pour l’installer, placez votre support d’installation de Windows Server 2012 dans le lecteur D et tapez ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="c216c-172">To install it, put your Windows Server 2012 installation media in Drive D and type the following:</span></span>

    Add-WindowsFeature RSAT-ADDS, Web-Server, Web-Static-Content, Web-Default-Doc, Web-Http-Errors, Web-Asp-Net, Web-Net-Ext, Web-ISAPI-Ext, Web-ISAPI-Filter, Web-Http-Logging, Web-Log-Libraries, Web-Request-Monitor, Web-Http-Tracing, Web-Basic-Auth, Web-Windows-Auth, Web-Client-Auth, Web-Filtering, Web-Stat-Compression, Web-Dyn-Compression, NET-WCF-HTTP-Activation45, Web-Asp-Net45, Web-Mgmt-Tools, Web-Scripting-Tools, Web-Mgmt-Compat, Desktop-Experience, Telnet-Client, BITS -Source D:\sources\sxs

<span data-ttu-id="c216c-173">Pour plus d’informations sur l’installation de .NET 3,5 sur des serveurs exécutant Windows Server 2012, voir « considérations relatives au déploiement de Microsoft .NET Framework 3,5 » à l’adresse <https://go.microsoft.com/fwlink/p/?linkid=275032> .</span><span class="sxs-lookup"><span data-stu-id="c216c-173">For details about installing .NET 3.5 on servers running Windows Server 2012, see "Microsoft .NET Framework 3.5 Deployment Considerations" at <https://go.microsoft.com/fwlink/p/?linkid=275032>.</span></span>

</div>

<div>

## <a name="additional-software-for-directors"></a><span data-ttu-id="c216c-174">Logiciels supplémentaires pour les directeurs</span><span class="sxs-lookup"><span data-stu-id="c216c-174">Additional Software for Directors</span></span>

<span data-ttu-id="c216c-175">Les directeurs doivent exécuter Internet Information Services (IIS), avec les modules suivants :</span><span class="sxs-lookup"><span data-stu-id="c216c-175">Directors must run Internet Information Services (IIS), with the following modules:</span></span>

  - <span data-ttu-id="c216c-176">Contenu statique</span><span class="sxs-lookup"><span data-stu-id="c216c-176">Static Content</span></span>

  - <span data-ttu-id="c216c-177">Document par défaut</span><span class="sxs-lookup"><span data-stu-id="c216c-177">Default Document</span></span>

  - <span data-ttu-id="c216c-178">Erreurs HTTP</span><span class="sxs-lookup"><span data-stu-id="c216c-178">HTTP Errors</span></span>

  - <span data-ttu-id="c216c-179">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="c216c-179">ASP.NET</span></span>

  - <span data-ttu-id="c216c-180">Extensibilité .NET</span><span class="sxs-lookup"><span data-stu-id="c216c-180">.NET Extensibility</span></span>

  - <span data-ttu-id="c216c-181">Extensions ISAPI (Internet Server API)</span><span class="sxs-lookup"><span data-stu-id="c216c-181">Internet Server API (ISAPI) Extensions</span></span>

  - <span data-ttu-id="c216c-182">Filtres ISAPI</span><span class="sxs-lookup"><span data-stu-id="c216c-182">ISAPI Filters</span></span>

  - <span data-ttu-id="c216c-183">Journalisation HTTP</span><span class="sxs-lookup"><span data-stu-id="c216c-183">HTTP Logging</span></span>

  - <span data-ttu-id="c216c-184">Outils de journalisation</span><span class="sxs-lookup"><span data-stu-id="c216c-184">Logging Tools</span></span>

  - <span data-ttu-id="c216c-185">Suivi</span><span class="sxs-lookup"><span data-stu-id="c216c-185">Tracing</span></span>

  - <span data-ttu-id="c216c-186">Authentification Windows</span><span class="sxs-lookup"><span data-stu-id="c216c-186">Windows Authentication</span></span>

  - <span data-ttu-id="c216c-187">Filtrage des demandes</span><span class="sxs-lookup"><span data-stu-id="c216c-187">Request Filtering</span></span>

  - <span data-ttu-id="c216c-188">Compression du contenu statique</span><span class="sxs-lookup"><span data-stu-id="c216c-188">Static Content Compression</span></span>

  - <span data-ttu-id="c216c-189">Console de gestion des services Internet (IIS)</span><span class="sxs-lookup"><span data-stu-id="c216c-189">IIS Management Console</span></span>

  - <span data-ttu-id="c216c-190">Scripts et outils de gestion des services Internet (IIS)</span><span class="sxs-lookup"><span data-stu-id="c216c-190">IIS Management Scripts and Tools</span></span>

  - <span data-ttu-id="c216c-191">Authentification anonyme (installée par défaut lors de l’installation d’IIS)</span><span class="sxs-lookup"><span data-stu-id="c216c-191">Anonymous Authentication (This is installed by default when IIS is installed.)</span></span>

  - <span data-ttu-id="c216c-192">Authentification par mappage de certificat client</span><span class="sxs-lookup"><span data-stu-id="c216c-192">Client Certificate Mapping Authentication</span></span>

</div>

<div>

## <a name="additional-software-for-persistent-chat-front-end-servers"></a><span data-ttu-id="c216c-193">Logiciel supplémentaire pour les serveurs front end chat persistants</span><span class="sxs-lookup"><span data-stu-id="c216c-193">Additional Software for Persistent Chat Front End Servers</span></span>

<span data-ttu-id="c216c-194">Les serveurs front-end chat permanents doivent exécuter Message Queuing (également appelé MSMQ), qui est un composant de Windows Server.</span><span class="sxs-lookup"><span data-stu-id="c216c-194">Persistent Chat Front End Servers must run Message Queuing (also known as MSMQ), which is a component of Windows Server.</span></span>

<span data-ttu-id="c216c-195">Pour plus d’informations sur l’activation de MSMQ, [cliquez ici.](https://technet.microsoft.com/library/cc771474.aspx)</span><span class="sxs-lookup"><span data-stu-id="c216c-195">For information on enabling MSMQ, [click here.](https://technet.microsoft.com/library/cc771474.aspx)</span></span>

</div>

<div>

## <a name="additional-software-for-edge-servers"></a><span data-ttu-id="c216c-196">Logiciels supplémentaires pour les serveurs de périphérie</span><span class="sxs-lookup"><span data-stu-id="c216c-196">Additional Software for Edge Servers</span></span>

<span data-ttu-id="c216c-197">Les serveurs Edge nécessitent le logiciel suivant :</span><span class="sxs-lookup"><span data-stu-id="c216c-197">Edge Servers require the following software:</span></span>

  - <span data-ttu-id="c216c-198">Chaque serveur exécutant Lync Server 2013 doit avoir installé la version appropriée de Windows PowerShell 3,0.</span><span class="sxs-lookup"><span data-stu-id="c216c-198">Each server running Lync Server 2013 must have the correct release of Windows PowerShell 3.0 installed.</span></span> <span data-ttu-id="c216c-199">Pour plus d’informations, consultez [installation de Windows PowerShell 3,0 pour Lync Server 2013](lync-server-2013-installing-windows-powershell-3-0.md).</span><span class="sxs-lookup"><span data-stu-id="c216c-199">For details, see [Installing Windows PowerShell 3.0 for Lync Server 2013](lync-server-2013-installing-windows-powershell-3-0.md).</span></span>

  - <span data-ttu-id="c216c-200">Lync Server nécessite Microsoft .NET Framework 4,5.</span><span class="sxs-lookup"><span data-stu-id="c216c-200">Lync Server requires Microsoft .NET Framework 4.5.</span></span> <span data-ttu-id="c216c-201">Pour Lync Server 2013 installé sur Windows Server 2008 R2, vous devez installer manuellement l’édition 64 bits de Microsoft .NET Framework 4,5 sur le serveur avant d’installer Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c216c-201">For Lync Server 2013 installed on Windows Server 2008 R2, you must manually install the 64-bit edition of Microsoft .NET Framework 4.5 on the server prior to installing Lync Server 2013.</span></span> <span data-ttu-id="c216c-202">Pour l’installer manuellement, téléchargez l’infrastructure Microsoft .NET 4,5 à partir du centre de téléchargement Microsoft sur [https://go.microsoft.com/fwlink/p/?LinkId=268529](https://go.microsoft.com/fwlink/p/?linkid=268529)</span><span class="sxs-lookup"><span data-stu-id="c216c-202">To manually install it, download the Microsoft .NET 4.5 Framework from the Microsoft Download Center at [https://go.microsoft.com/fwlink/p/?LinkId=268529](https://go.microsoft.com/fwlink/p/?linkid=268529)</span></span>

  - <span data-ttu-id="c216c-203">**Windows Identity Foundation** dans Lync Server 2013 nécessite l’installation de Windows Identity Foundation afin de prendre en charge les scénarios d’authentification de serveur à serveur.</span><span class="sxs-lookup"><span data-stu-id="c216c-203">**Windows Identity Foundation** in Lync Server 2013 requires the installation of Windows Identity Foundation in order to support server to server authentication scenarios.</span></span> <span data-ttu-id="c216c-204">Windows Server 2008 R2 et Windows Server 2012 nécessitent différentes procédures pour installer Windows identify Foundation.</span><span class="sxs-lookup"><span data-stu-id="c216c-204">Windows Server 2008 R2 and Windows Server 2012 require different procedures to install the Windows Identify Foundation.</span></span> <span data-ttu-id="c216c-205">Sélectionnez votre système d’exploitation serveur dans la liste suivante :</span><span class="sxs-lookup"><span data-stu-id="c216c-205">Select your server operating system from the following list:</span></span>
    
      - <span data-ttu-id="c216c-206">Windows Server 2008 R2 pour Windows Server 2008 R2, vous recherchez s’il a déjà été installé sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c216c-206">Windows Server 2008 R2   For Windows Server 2008 R2, you check to see if it has already been installed on your computer.</span></span> <span data-ttu-id="c216c-207">Pour ce faire, accédez à **Ajout/suppression de programmes**, **Affichez les mises à jour installées** et Regardez sous **Windows** pour l’entrée **Windows Identity Foundation (KB974405)**.</span><span class="sxs-lookup"><span data-stu-id="c216c-207">To do this, go to **Add/Remove Programs**, **View Installed Updates**, and look under **Windows** for the entry **Windows Identity Foundation (KB974405)**.</span></span> <span data-ttu-id="c216c-208">Pour plus d’informations sur l’installation de Windows Identity Foundation, voir [https://go.microsoft.com/fwlink/p/?linkId=204657](https://go.microsoft.com/fwlink/p/?linkid=204657) .</span><span class="sxs-lookup"><span data-stu-id="c216c-208">For details about installing Windows Identity Foundation, see [https://go.microsoft.com/fwlink/p/?linkId=204657](https://go.microsoft.com/fwlink/p/?linkid=204657).</span></span>
    
      - <span data-ttu-id="c216c-209">Windows Server 2012 pour Windows Server 2012, utilisez le **Gestionnaire de serveur** pour installer Windows Identity Foundation.</span><span class="sxs-lookup"><span data-stu-id="c216c-209">Windows Server 2012   For Windows Server 2012, you use **Server Manager** to install the Windows Identity Foundation.</span></span> <span data-ttu-id="c216c-210">Dans l' **Assistant Ajout de rôles et de fonctionnalités** du gestionnaire de serveur, sélectionnez **fonctionnalités**.</span><span class="sxs-lookup"><span data-stu-id="c216c-210">In the Server Manager **Add Roles and Features Wizard**, select **Features**.</span></span> <span data-ttu-id="c216c-211">Dans la liste, sélectionnez **Windows Identity Foundation 3,5** .</span><span class="sxs-lookup"><span data-stu-id="c216c-211">Select **Windows Identity Foundation 3.5** from the list.</span></span> <span data-ttu-id="c216c-212">Cliquez sur **suivant**, puis sur **installer**.</span><span class="sxs-lookup"><span data-stu-id="c216c-212">Click **Next**, then click **Install**.</span></span>

</div>

<div>

## <a name="do-not-install-layered-socket-providers-on-media-servers"></a><span data-ttu-id="c216c-213">Ne pas installer les fournisseurs de Socket Layer sur les serveurs multimédias</span><span class="sxs-lookup"><span data-stu-id="c216c-213">Do Not Install Layered Socket Providers on Media Servers</span></span>

<span data-ttu-id="c216c-214">N’installez aucun logiciel client Microsoft Internet Security and Acceleration (ISA) Server, ou tout autre logiciel de fournisseur de services de couche Winsock (LSP) sur un serveur frontal ou un serveur de médiation autonome.</span><span class="sxs-lookup"><span data-stu-id="c216c-214">Do not install any Microsoft Internet Security and Acceleration (ISA) Server client software, or any other Winsock Layered Service Providers (LSP) software, on any Front End Servers or stand-alone Mediation Servers.</span></span> <span data-ttu-id="c216c-215">L’installation de ce logiciel peut entraîner de mauvaises performances du trafic multimédia.</span><span class="sxs-lookup"><span data-stu-id="c216c-215">Installing this software could cause poor media traffic performance.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="c216c-216">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c216c-216">See Also</span></span>


[<span data-ttu-id="c216c-217">Configuration logicielle requise pour les outils d’administration dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c216c-217">Administrative tools software requirements in Lync Server 2013</span></span>](lync-server-2013-administrative-tools-software-requirements.md)  
  

<span data-ttu-id="c216c-218"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c216c-218"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

