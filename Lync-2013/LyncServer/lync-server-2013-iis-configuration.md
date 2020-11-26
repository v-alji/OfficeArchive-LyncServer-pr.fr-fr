---
title: 'Lync Server 2013 : Configuration des services Internet (IIS)'
description: 'Lync Server 2013 : configuration d’IIS.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: IIS configuration
ms:assetid: b458babf-bf64-43f0-8a8e-612f5096b63c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412871(v=OCS.15)
ms:contentKeyID: 48185169
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 901aca7bf5ff8824b54e93754569a6ef5defc10e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427431"
---
# <a name="iis-configuration-in-lync-server-2013"></a><span data-ttu-id="f07dd-103">Configuration des services Internet (IIS) dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f07dd-103">IIS configuration in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f07dd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f07dd-104">

<span> </span></span></span>

<span data-ttu-id="f07dd-105">_**Dernière modification de la rubrique :** 2014-02-17_</span><span class="sxs-lookup"><span data-stu-id="f07dd-105">_**Topic Last Modified:** 2014-02-17_</span></span>

<span data-ttu-id="f07dd-106">Pour effectuer cette procédure, vous devez être connecté au serveur au minimum en tant qu’administrateur local et utilisateur de domaine.</span><span class="sxs-lookup"><span data-stu-id="f07dd-106">To successfully complete this procedure, you should be logged on to the server minimally as a local administrator and a domain user.</span></span>

<span data-ttu-id="f07dd-107">Avant de configurer et d’installer le serveur frontal pour Lync Server 2013, Standard Edition ou le premier serveur frontal d’un pool, vous installez et configurez le rôle de serveur et les services Web pour Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="f07dd-107">Before you configure and install the Front End Server for Lync Server 2013, Standard Edition or the first Front End Server in a pool, you install and configure the server role and Web Services for Internet Information Services (IIS).</span></span>

<div class=" ">


> [!IMPORTANT]  
> <span data-ttu-id="f07dd-108">Si votre organisation nécessite que vous localisiez IIS et tous les services Web sur un lecteur autre que le lecteur système, vous pouvez modifier le chemin d’accès d’installation pour les fichiers Lync Server 2013 dans la boîte de dialogue de configuration lors de l’installation initiale des outils d’administration de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f07dd-108">If your organization requires that you locate IIS and all Web Services on a drive other than the system drive, you can change the installation location path for the Lync Server 2013 files in the Setup dialog box when you initially install the Lync Server 2013 Administrative tools.</span></span> <span data-ttu-id="f07dd-109">Vous installez les outils d’administration avant d’installer IIS.</span><span class="sxs-lookup"><span data-stu-id="f07dd-109">You install the Administrative tools before installing IIS.</span></span> <span data-ttu-id="f07dd-110">Si vous installez les fichiers d’installation dans ce chemin d’accès, y compris les OCSCore.msi, les autres fichiers Lync Server 2013 sont également déployés sur ce lecteur.</span><span class="sxs-lookup"><span data-stu-id="f07dd-110">If you install the Setup files to this path, including OCSCore.msi, the rest of the Lync Server 2013 files will be deployed to this drive as well.</span></span> <span data-ttu-id="f07dd-111">Pour dtails, voir <A href="lync-server-2013-install-lync-server-administrative-tools.md">installer les outils d’administration de Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="f07dd-111">For dtails, see <A href="lync-server-2013-install-lync-server-administrative-tools.md">Install Lync Server 2013 administrative tools</A>.</span></span> <span data-ttu-id="f07dd-112">Pour plus d’informations sur la façon de déplacer le INETPUB déployé par Windows Server Manager lors de l’installation d’IIS, voir <A href="https://go.microsoft.com/fwlink/p/?linkid=216888">https://go.microsoft.com/fwlink/p/?linkId=216888</A> .</span><span class="sxs-lookup"><span data-stu-id="f07dd-112">For details about how to relocate the INETPUB deployed by Windows Server Manager when installing IIS, see <A href="https://go.microsoft.com/fwlink/p/?linkid=216888">https://go.microsoft.com/fwlink/p/?linkId=216888</A>.</span></span>



</div>

<span data-ttu-id="f07dd-113">Le tableau suivant indique les services de rôles IIS 7,5 requis.</span><span class="sxs-lookup"><span data-stu-id="f07dd-113">The following table indicates the required IIS 7.5 role services.</span></span>

### <a name="iis-75-role-services"></a><span data-ttu-id="f07dd-114">Services de rôle 7,5 IIS</span><span class="sxs-lookup"><span data-stu-id="f07dd-114">IIS 7.5 Role Services</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f07dd-115">Titre du rôle</span><span class="sxs-lookup"><span data-stu-id="f07dd-115">Role Heading</span></span></th>
<th><span data-ttu-id="f07dd-116">Service de rôle</span><span class="sxs-lookup"><span data-stu-id="f07dd-116">Role Service</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f07dd-117">Fonctionnalités HTTP communes installées</span><span class="sxs-lookup"><span data-stu-id="f07dd-117">Common HTTP features installed</span></span></p></td>
<td><p><span data-ttu-id="f07dd-118">Contenu statique</span><span class="sxs-lookup"><span data-stu-id="f07dd-118">Static content</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f07dd-119">Fonctionnalités HTTP communes installées</span><span class="sxs-lookup"><span data-stu-id="f07dd-119">Common HTTP features installed</span></span></p></td>
<td><p><span data-ttu-id="f07dd-120">Document par défaut</span><span class="sxs-lookup"><span data-stu-id="f07dd-120">Default document</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f07dd-121">Fonctionnalités HTTP communes installées</span><span class="sxs-lookup"><span data-stu-id="f07dd-121">Common HTTP features installed</span></span></p></td>
<td><p><span data-ttu-id="f07dd-122">Erreurs HTTP</span><span class="sxs-lookup"><span data-stu-id="f07dd-122">HTTP errors</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f07dd-123">Développement d’applications</span><span class="sxs-lookup"><span data-stu-id="f07dd-123">Application development</span></span></p></td>
<td><p><span data-ttu-id="f07dd-124">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="f07dd-124">ASP.NET</span></span></p>
<p><span data-ttu-id="f07dd-125">Windows Server 2012 nécessite également ASP. NET 4.5</span><span class="sxs-lookup"><span data-stu-id="f07dd-125">Windows Server 2012 also requires ASP.NET4.5</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f07dd-126">Développement d’applications</span><span class="sxs-lookup"><span data-stu-id="f07dd-126">Application development</span></span></p></td>
<td><p><span data-ttu-id="f07dd-127">Extensibilité .NET</span><span class="sxs-lookup"><span data-stu-id="f07dd-127">.NET extensibility</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f07dd-128">Développement d’applications</span><span class="sxs-lookup"><span data-stu-id="f07dd-128">Application development</span></span></p></td>
<td><p><span data-ttu-id="f07dd-129">Extensions ISAPI (Internet Server API)</span><span class="sxs-lookup"><span data-stu-id="f07dd-129">Internet Server API (ISAPI) extensions</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f07dd-130">Développement d’applications</span><span class="sxs-lookup"><span data-stu-id="f07dd-130">Application development</span></span></p></td>
<td><p><span data-ttu-id="f07dd-131">Filtres ISAPI</span><span class="sxs-lookup"><span data-stu-id="f07dd-131">ISAPI filters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f07dd-132">État d’intégrité et diagnostics</span><span class="sxs-lookup"><span data-stu-id="f07dd-132">Health and diagnostics</span></span></p></td>
<td><p><span data-ttu-id="f07dd-133">Journalisation HTTP</span><span class="sxs-lookup"><span data-stu-id="f07dd-133">HTTP logging</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f07dd-134">État d’intégrité et diagnostics</span><span class="sxs-lookup"><span data-stu-id="f07dd-134">Health and diagnostics</span></span></p></td>
<td><p><span data-ttu-id="f07dd-135">Outils de journalisation</span><span class="sxs-lookup"><span data-stu-id="f07dd-135">Logging tools</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f07dd-136">État d’intégrité et diagnostics</span><span class="sxs-lookup"><span data-stu-id="f07dd-136">Health and diagnostics</span></span></p></td>
<td><p><span data-ttu-id="f07dd-137">Suivi</span><span class="sxs-lookup"><span data-stu-id="f07dd-137">Tracing</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f07dd-138">Sécurité</span><span class="sxs-lookup"><span data-stu-id="f07dd-138">Security</span></span></p></td>
<td><p><span data-ttu-id="f07dd-139">Authentification anonyme (installée et activée par défaut)</span><span class="sxs-lookup"><span data-stu-id="f07dd-139">Anonymous authentication (installed and enabled by default)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f07dd-140">Sécurité</span><span class="sxs-lookup"><span data-stu-id="f07dd-140">Security</span></span></p></td>
<td><p><span data-ttu-id="f07dd-141">Authentification Windows</span><span class="sxs-lookup"><span data-stu-id="f07dd-141">Windows authentication</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f07dd-142">Sécurité</span><span class="sxs-lookup"><span data-stu-id="f07dd-142">Security</span></span></p></td>
<td><p><span data-ttu-id="f07dd-143">Authentification du mappage de certificat client</span><span class="sxs-lookup"><span data-stu-id="f07dd-143">Client Certificate Mapping authentication</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f07dd-144">Sécurité</span><span class="sxs-lookup"><span data-stu-id="f07dd-144">Security</span></span></p></td>
<td><p><span data-ttu-id="f07dd-145">Filtrage de requête</span><span class="sxs-lookup"><span data-stu-id="f07dd-145">Request filtering</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f07dd-146">Performances</span><span class="sxs-lookup"><span data-stu-id="f07dd-146">Performance</span></span></p></td>
<td><p><span data-ttu-id="f07dd-147">Compression de contenu statique</span><span class="sxs-lookup"><span data-stu-id="f07dd-147">Static content compression</span></span></p>
<p><span data-ttu-id="f07dd-148">Compression de contenu dynamique</span><span class="sxs-lookup"><span data-stu-id="f07dd-148">Dynamic content compression</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f07dd-149">Outils de gestion</span><span class="sxs-lookup"><span data-stu-id="f07dd-149">Management Tools</span></span></p></td>
<td><p><span data-ttu-id="f07dd-150">Console de gestion des services Internet (IIS)</span><span class="sxs-lookup"><span data-stu-id="f07dd-150">IIS Management Console</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f07dd-151">Outils de gestion</span><span class="sxs-lookup"><span data-stu-id="f07dd-151">Management Tools</span></span></p></td>
<td><p><span data-ttu-id="f07dd-152">Scripts et outils de gestion des services Internet (IIS)</span><span class="sxs-lookup"><span data-stu-id="f07dd-152">IIS Management Scripts and Tools</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f07dd-153">Sur le système d’exploitation Windows Server 2008 R2 SP1 x64, vous pouvez utiliser Windows PowerShell 2,0.</span><span class="sxs-lookup"><span data-stu-id="f07dd-153">On the Windows Server 2008 R2 SP1 x64 operating system, you can use Windows PowerShell 2.0.</span></span> <span data-ttu-id="f07dd-154">Vous devez d’abord importer le module ServerManager, puis installer les services de rôles et de rôles IIS 7,5.</span><span class="sxs-lookup"><span data-stu-id="f07dd-154">You must first import the ServerManager module, and then install the IIS 7.5 role and role services.</span></span>

   ```PowerShell
    Import-Module ServerManager
   ```

   ```PowerShell
    Add-WindowsFeature Web-Server, Web-Static-Content, Web-Default-Doc, Web-Scripting-Tools, Web-Windows-Auth, Web-Asp-Net, Web-Log-Libraries, Web-Http-Tracing, Web-Stat-Compression, Web-Dyn-Compression, Web-ISAPI-Ext, Web-ISAPI-Filter, Web-Http-Errors, Web-Http-Logging, Web-Net-Ext, Web-Client-Auth, Web-Filtering, Web-Mgmt-Console
   ```

<div class=" ">


> [!NOTE]  
> <span data-ttu-id="f07dd-155">L’authentification anonyme est installée par défaut avec le rôle serveur IIS.</span><span class="sxs-lookup"><span data-stu-id="f07dd-155">Anonymous authentication is installed by default with the IIS server role.</span></span> <span data-ttu-id="f07dd-156">Vous pouvez gérer l’authentification anonyme après l’installation d’IIS.</span><span class="sxs-lookup"><span data-stu-id="f07dd-156">You can manage anonymous authentication after the installation of IIS.</span></span> <span data-ttu-id="f07dd-157">Pour en savoir plus, voir Activer l’authentification anonyme (IIS 7) <A href="https://go.microsoft.com/fwlink/p/?linkid=203935">https://go.microsoft.com/fwlink/p/?linkId=203935</A> .</span><span class="sxs-lookup"><span data-stu-id="f07dd-157">For details, see “Enable Anonymous Authentication (IIS 7)” at <A href="https://go.microsoft.com/fwlink/p/?linkid=203935">https://go.microsoft.com/fwlink/p/?linkId=203935</A>.</span></span>



</div>

<span data-ttu-id="f07dd-158">Le tableau suivant indique les services de rôles IIS 8,0 et IIS 8,5 requis pour Windows Server 2012 et Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="f07dd-158">The following table indicates the required IIS 8.0 and IIS 8.5 role services for Windows Server 2012 and Windows Server 2012 R2.</span></span>

<div class=" ">


> [!NOTE]  
> <span data-ttu-id="f07dd-159">Pour Windows Server 2012 et Windows Server 2012 R2, l’applet de applet de Add-WindowsFeature a été remplacée par l’applet de Install-WindowsFeature.</span><span class="sxs-lookup"><span data-stu-id="f07dd-159">For Windows Server 2012 and Windows Server 2012 R2, the Add-WindowsFeature cmdlet has been replaced by the Install-WindowsFeature cmdlet.</span></span> <span data-ttu-id="f07dd-160">Pour plus d’informations, consultez la rubrique <A href="https://go.microsoft.com/fwlink/p/?linkid=392274">installer-WindowsFeature</A>.</span><span class="sxs-lookup"><span data-stu-id="f07dd-160">For details, see <A href="https://go.microsoft.com/fwlink/p/?linkid=392274">Install-WindowsFeature</A>.</span></span>



</div>

### <a name="iis-80-and-iis-85-role-services"></a><span data-ttu-id="f07dd-161">Services de rôle IIS 8,0 et IIS 8,5</span><span class="sxs-lookup"><span data-stu-id="f07dd-161">IIS 8.0 and IIS 8.5 Role Services</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f07dd-162">Titre du rôle</span><span class="sxs-lookup"><span data-stu-id="f07dd-162">Role Heading</span></span></th>
<th><span data-ttu-id="f07dd-163">Service de rôle</span><span class="sxs-lookup"><span data-stu-id="f07dd-163">Role Service</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f07dd-164">Serveur Web (IIS)</span><span class="sxs-lookup"><span data-stu-id="f07dd-164">Web Server (IIS)</span></span></p></td>
<td><p><span data-ttu-id="f07dd-165">Serveur Web</span><span class="sxs-lookup"><span data-stu-id="f07dd-165">Web Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f07dd-166">Fonctionnalités HTTP communes</span><span class="sxs-lookup"><span data-stu-id="f07dd-166">Common HTTP Features</span></span></p></td>
<td><p><span data-ttu-id="f07dd-167">Document par défaut</span><span class="sxs-lookup"><span data-stu-id="f07dd-167">Default Document</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f07dd-168">Fonctionnalités HTTP communes</span><span class="sxs-lookup"><span data-stu-id="f07dd-168">Common HTTP Features</span></span></p></td>
<td><p><span data-ttu-id="f07dd-169">Exploration des répertoires</span><span class="sxs-lookup"><span data-stu-id="f07dd-169">Directory Browsing</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f07dd-170">Fonctionnalités HTTP communes</span><span class="sxs-lookup"><span data-stu-id="f07dd-170">Common HTTP Features</span></span></p></td>
<td><p><span data-ttu-id="f07dd-171">Erreurs HTTP</span><span class="sxs-lookup"><span data-stu-id="f07dd-171">HTTP Errors</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f07dd-172">Fonctionnalités HTTP communes</span><span class="sxs-lookup"><span data-stu-id="f07dd-172">Common HTTP Features</span></span></p></td>
<td><p><span data-ttu-id="f07dd-173">Contenu statique</span><span class="sxs-lookup"><span data-stu-id="f07dd-173">Static content</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f07dd-174">Fonctionnalités HTTP communes</span><span class="sxs-lookup"><span data-stu-id="f07dd-174">Common HTTP Features</span></span></p></td>
<td><p><span data-ttu-id="f07dd-175">Redirection HTTP</span><span class="sxs-lookup"><span data-stu-id="f07dd-175">HTTP Redirection</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f07dd-176">Intégrité et diagnostics</span><span class="sxs-lookup"><span data-stu-id="f07dd-176">Health and Diagnostics</span></span></p></td>
<td><p><span data-ttu-id="f07dd-177">Journalisation HTTP</span><span class="sxs-lookup"><span data-stu-id="f07dd-177">HTTP Logging</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f07dd-178">Intégrité et diagnostics</span><span class="sxs-lookup"><span data-stu-id="f07dd-178">Health and Diagnostics</span></span></p></td>
<td><p><span data-ttu-id="f07dd-179">Outils de journalisation</span><span class="sxs-lookup"><span data-stu-id="f07dd-179">Logging Tools</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f07dd-180">Intégrité et diagnostics</span><span class="sxs-lookup"><span data-stu-id="f07dd-180">Health and Diagnostics</span></span></p></td>
<td><p><span data-ttu-id="f07dd-181">Moniteur de requête</span><span class="sxs-lookup"><span data-stu-id="f07dd-181">Request Monitor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f07dd-182">Intégrité et diagnostics</span><span class="sxs-lookup"><span data-stu-id="f07dd-182">Health and Diagnostics</span></span></p></td>
<td><p><span data-ttu-id="f07dd-183">Suivi</span><span class="sxs-lookup"><span data-stu-id="f07dd-183">Tracing</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f07dd-184">Sécurité</span><span class="sxs-lookup"><span data-stu-id="f07dd-184">Security</span></span></p></td>
<td><p><span data-ttu-id="f07dd-185">Filtrage des demandes</span><span class="sxs-lookup"><span data-stu-id="f07dd-185">Request Filtering</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f07dd-186">Sécurité</span><span class="sxs-lookup"><span data-stu-id="f07dd-186">Security</span></span></p></td>
<td><p><span data-ttu-id="f07dd-187">Authentification de base</span><span class="sxs-lookup"><span data-stu-id="f07dd-187">Basic Authentication</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f07dd-188">Sécurité</span><span class="sxs-lookup"><span data-stu-id="f07dd-188">Security</span></span></p></td>
<td><p><span data-ttu-id="f07dd-189">Authentification par mappage de certificat client</span><span class="sxs-lookup"><span data-stu-id="f07dd-189">Client Certificate Mapping Authentication</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f07dd-190">Sécurité</span><span class="sxs-lookup"><span data-stu-id="f07dd-190">Security</span></span></p></td>
<td><p><span data-ttu-id="f07dd-191">Authentification Windows</span><span class="sxs-lookup"><span data-stu-id="f07dd-191">Windows Authentication</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f07dd-192">Développement d’applications</span><span class="sxs-lookup"><span data-stu-id="f07dd-192">Application Development</span></span></p></td>
<td><p><span data-ttu-id="f07dd-193">Extensibilité .net 3,5</span><span class="sxs-lookup"><span data-stu-id="f07dd-193">.Net Extensibility 3.5</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f07dd-194">Développement d’applications</span><span class="sxs-lookup"><span data-stu-id="f07dd-194">Application Development</span></span></p></td>
<td><p><span data-ttu-id="f07dd-195">Extensibilité .net 4,5</span><span class="sxs-lookup"><span data-stu-id="f07dd-195">.Net Extensibility 4.5</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f07dd-196">Développement d’applications</span><span class="sxs-lookup"><span data-stu-id="f07dd-196">Application Development</span></span></p></td>
<td><p><span data-ttu-id="f07dd-197">ASP.Net 3,5</span><span class="sxs-lookup"><span data-stu-id="f07dd-197">ASP.Net 3.5</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f07dd-198">Développement d’applications</span><span class="sxs-lookup"><span data-stu-id="f07dd-198">Application Development</span></span></p></td>
<td><p><span data-ttu-id="f07dd-199">ASP.Net 4,5</span><span class="sxs-lookup"><span data-stu-id="f07dd-199">ASP.Net 4.5</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f07dd-200">Développement d’applications</span><span class="sxs-lookup"><span data-stu-id="f07dd-200">Application Development</span></span></p></td>
<td><p><span data-ttu-id="f07dd-201">Extensions ISAPI</span><span class="sxs-lookup"><span data-stu-id="f07dd-201">ISAPI Extensions</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f07dd-202">Développement d’applications</span><span class="sxs-lookup"><span data-stu-id="f07dd-202">Application Development</span></span></p></td>
<td><p><span data-ttu-id="f07dd-203">Filtres ISAPI</span><span class="sxs-lookup"><span data-stu-id="f07dd-203">ISAPI Filters</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f07dd-204">Développement d’applications</span><span class="sxs-lookup"><span data-stu-id="f07dd-204">Application Development</span></span></p></td>
<td><p><span data-ttu-id="f07dd-205">Inclusions côté serveur</span><span class="sxs-lookup"><span data-stu-id="f07dd-205">Server Side Includes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f07dd-206">Outils de gestion</span><span class="sxs-lookup"><span data-stu-id="f07dd-206">Management Tools</span></span></p></td>
<td><p><span data-ttu-id="f07dd-207">Console de gestion des services Internet (IIS)</span><span class="sxs-lookup"><span data-stu-id="f07dd-207">IIS Management Console</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f07dd-208">Outils de gestion</span><span class="sxs-lookup"><span data-stu-id="f07dd-208">Management Tools</span></span></p></td>
<td><p><span data-ttu-id="f07dd-209">Compatibilité de la métabase IIS 6</span><span class="sxs-lookup"><span data-stu-id="f07dd-209">IIS 6 Metabase compatibility</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f07dd-210">Outils de gestion</span><span class="sxs-lookup"><span data-stu-id="f07dd-210">Management Tools</span></span></p></td>
<td><p><span data-ttu-id="f07dd-211">Scripts et outils de gestion des services Internet (IIS)</span><span class="sxs-lookup"><span data-stu-id="f07dd-211">IIS Management Scripts and Tools</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f07dd-212">Fonctionnalités d’infrastructure .net 3,5</span><span class="sxs-lookup"><span data-stu-id="f07dd-212">.Net 3.5 Framework Features</span></span></p></td>
<td><p><span data-ttu-id="f07dd-213">.Net 3,5 Framework</span><span class="sxs-lookup"><span data-stu-id="f07dd-213">.Net 3.5 Framework</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f07dd-214">Fonctionnalités d’infrastructure .net 4,5</span><span class="sxs-lookup"><span data-stu-id="f07dd-214">.Net 4.5 Framework Features</span></span></p></td>
<td><p><span data-ttu-id="f07dd-215">.NET Framework 4,5</span><span class="sxs-lookup"><span data-stu-id="f07dd-215">.Net Framework 4.5</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f07dd-216">Fonctionnalités d’infrastructure .net 4,5</span><span class="sxs-lookup"><span data-stu-id="f07dd-216">.Net 4.5 Framework Features</span></span></p></td>
<td><p><span data-ttu-id="f07dd-217">ASP.Net 4,5</span><span class="sxs-lookup"><span data-stu-id="f07dd-217">ASP.Net 4.5</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f07dd-218">Fonctionnalités d’infrastructure .net 4,5</span><span class="sxs-lookup"><span data-stu-id="f07dd-218">.Net 4.5 Framework Features</span></span></p></td>
<td><p><span data-ttu-id="f07dd-219">Activation HTTP</span><span class="sxs-lookup"><span data-stu-id="f07dd-219">HTTP Activation</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f07dd-220">Fonctionnalités d’infrastructure .net 4,5</span><span class="sxs-lookup"><span data-stu-id="f07dd-220">.Net 4.5 Framework Features</span></span></p></td>
<td><p><span data-ttu-id="f07dd-221">Partage de port TCP</span><span class="sxs-lookup"><span data-stu-id="f07dd-221">TCP Port Sharing</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f07dd-222">Service de transfert intelligent en arrière-plan</span><span class="sxs-lookup"><span data-stu-id="f07dd-222">Background Intelligent Transfer Service</span></span></p></td>
<td><p><span data-ttu-id="f07dd-223">Extensions serveur IIS</span><span class="sxs-lookup"><span data-stu-id="f07dd-223">IIS Server Extensions</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f07dd-224">Services d’entrée manuscrite</span><span class="sxs-lookup"><span data-stu-id="f07dd-224">Ink and Handwriting Services</span></span></p></td>
<td><p><span data-ttu-id="f07dd-225">Services d’entrée manuscrite</span><span class="sxs-lookup"><span data-stu-id="f07dd-225">Ink and Handwriting Services</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f07dd-226">Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f07dd-226">Media Foundation</span></span></p></td>
<td><p><span data-ttu-id="f07dd-227">Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f07dd-227">Media Foundation</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f07dd-228">Interfaces utilisateur et infrastructure</span><span class="sxs-lookup"><span data-stu-id="f07dd-228">User Interfaces and Infrastructure</span></span></p></td>
<td><p><span data-ttu-id="f07dd-229">Outils et infrastructure de gestion graphique</span><span class="sxs-lookup"><span data-stu-id="f07dd-229">Graphical Management Tools and Infrastructure</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f07dd-230">Interfaces utilisateur et infrastructure</span><span class="sxs-lookup"><span data-stu-id="f07dd-230">User Interfaces and Infrastructure</span></span></p></td>
<td><p><span data-ttu-id="f07dd-231">Expérience de bureau</span><span class="sxs-lookup"><span data-stu-id="f07dd-231">Desktop Experience</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f07dd-232">Interfaces utilisateur et infrastructure</span><span class="sxs-lookup"><span data-stu-id="f07dd-232">User Interfaces and Infrastructure</span></span></p></td>
<td><p><span data-ttu-id="f07dd-233">Shell graphique serveur</span><span class="sxs-lookup"><span data-stu-id="f07dd-233">Server Graphical Shell</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f07dd-234">Windows Identity Foundation 3.5</span><span class="sxs-lookup"><span data-stu-id="f07dd-234">Windows Identity Foundation 3.5</span></span></p></td>
<td><p><span data-ttu-id="f07dd-235">Windows Identity Foundation 3.5</span><span class="sxs-lookup"><span data-stu-id="f07dd-235">Windows Identity Foundation 3.5</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f07dd-236">Service d’activation de processus Windows</span><span class="sxs-lookup"><span data-stu-id="f07dd-236">Windows Process Activation Service</span></span></p></td>
<td><p><span data-ttu-id="f07dd-237">Modèle de processus</span><span class="sxs-lookup"><span data-stu-id="f07dd-237">Process Model</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f07dd-238">Service d’activation de processus Windows</span><span class="sxs-lookup"><span data-stu-id="f07dd-238">Windows Process Activation Service</span></span></p></td>
<td><p><span data-ttu-id="f07dd-239">API de configuration</span><span class="sxs-lookup"><span data-stu-id="f07dd-239">Configuration APIs</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f07dd-240">Dans Windows Server 2012 et Windows Server 2012 R2, vous pouvez utiliser Windows PowerShell 3,0 pour installer la configuration requise pour les services Internet (IIS).</span><span class="sxs-lookup"><span data-stu-id="f07dd-240">In Windows Server 2012 and Windows Server 2012 R2, you can use Windows PowerShell 3.0 to install the IIS Requirements.</span></span> <span data-ttu-id="f07dd-241">À l’aide du module ServerManager dans Windows PowerShell 3,0, tapez :</span><span class="sxs-lookup"><span data-stu-id="f07dd-241">Using the ServerManager module in Windows PowerShell 3.0, type:</span></span>

   ```PowerShell
    Import-Module ServerManager
   ```

   ```PowerShell
    Add-WindowsFeature Web-Server, Web-Static-Content, Web-Default-Doc, Web-Http-Errors, Web-Asp-Net, Web-Net-Ext, Web-ISAPI-Ext, Web-ISAPI-Filter, Web-Http-Logging, Web-Log-Libraries, Web-Request-Monitor, Web-Http-Tracing, Web-Basic-Auth, Web-Windows-Auth, Web-Client-Auth, Web-Filtering, Web-Stat-Compression, Web-Dyn-Compression, NET-Framework-45-Core, NET-WCF-HTTP-Activation45, Web-Asp-Net45, Web-Mgmt-Tools, Web-Scripting-Tools, Web-Mgmt-Console, Web-Mgmt-Compat, Windows-Identity-Foundation, Server-Media-Foundation, BITS -Source D:\sources\sxs
   ```

<div class=" ">


> [!IMPORTANT]  
> <span data-ttu-id="f07dd-242">Une nouveauté de Windows Server 2012 est le paramètre – source qui définit l’emplacement où se trouve le média source de Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="f07dd-242">New with Windows Server 2012 is the –Source parameter that defines where the Windows Server 2012 source media can be found.</span></span> <span data-ttu-id="f07dd-243">Le média peut être défini comme lecteur DVD (par exemple, D:\Sources\Sxs) ou sur un partage réseau pour lequel les fichiers multimédias ont été copiés (par exemple, \\ fileserver\windows2012\sources\Sxs).</span><span class="sxs-lookup"><span data-stu-id="f07dd-243">The media can be defined as a DVD drive (for example, D:\Sources\Sxs), or to a network share that the media files have been copied (for example, \\fileserver\windows2012\sources\Sxs).</span></span>



</div>

<div>

## <a name="see-also"></a><span data-ttu-id="f07dd-244">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f07dd-244">See Also</span></span>


[<span data-ttu-id="f07dd-245">Configuration requise pour les services Internet (IIS) pour les pools frontaux et les serveurs Standard Edition dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f07dd-245">IIS requirements for Front End pools and Standard Edition servers in Lync Server 2013</span></span>](lync-server-2013-iis-requirements-for-front-end-pools-and-standard-edition-servers.md)  
  

<span data-ttu-id="f07dd-246"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f07dd-246"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

