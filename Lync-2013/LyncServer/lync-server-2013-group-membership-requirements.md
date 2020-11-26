---
title: 'Lync Server 2013 : Exigences d’adhésion à un groupe'
description: 'Lync Server 2013 : exigences d’appartenance au groupe.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Group membership requirements
ms:assetid: 01876843-8717-4e72-baf5-866ac8cceee6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204623(v=OCS.15)
ms:contentKeyID: 48183239
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3f18fb6fbc782ecd41b7a782965f2cd6a82f6fd5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427837"
---
# <a name="group-membership-requirements-for-lync-server-2013"></a><span data-ttu-id="1207c-103">Exigences d’adhésion à un groupe pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1207c-103">Group membership requirements for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1207c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1207c-104">

<span> </span></span></span>

<span data-ttu-id="1207c-105">_**Dernière modification de la rubrique :** 2012-10-05_</span><span class="sxs-lookup"><span data-stu-id="1207c-105">_**Topic Last Modified:** 2012-10-05_</span></span>

<span data-ttu-id="1207c-106">Le tableau suivant résume le ou les groupes auxquels une personne doit appartenir pour installer, gérer et dépanner Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1207c-106">The following table summarizes the group or groups that a person should belong to in order to successfully install, manage, and troubleshoot Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1207c-107">Exécutable Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1207c-107">Lync Server 2013 Executable</span></span></th>
<th><span data-ttu-id="1207c-108">Appartenance au groupe requise</span><span class="sxs-lookup"><span data-stu-id="1207c-108">Group Membership Required</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1207c-109"><strong>Setup.exe</strong> -exécutable qui démarre l’installation des outils d’administration de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1207c-109"><strong>Setup.exe</strong> – Executable that starts the installation of the Lync Server 2013 administrative tools.</span></span></p></td>
<td><p><span data-ttu-id="1207c-110">Membre du groupe Administrateurs local sur l’ordinateur à partir duquel l’exécutable s’exécute.</span><span class="sxs-lookup"><span data-stu-id="1207c-110">Member of the Local Administrators group on the computer from which the executable is run.</span></span> <span data-ttu-id="1207c-111">Membre du groupe utilisateurs de domaine pour lire les informations dans les services de domaine Active Directory (AD FS).</span><span class="sxs-lookup"><span data-stu-id="1207c-111">Member of Domain Users group to read information in Active Directory Domain Services.</span></span> <span data-ttu-id="1207c-112">Ce niveau d’autorisation est requis, car l’installation automatique des packages MSI requis sur l’ordinateur local nécessite des privilèges permettant la lecture et l’écriture des ressources de l’ordinateur local protégé telles que des répertoires de fichiers de programmes et du Registre protégé comme la ruche de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="1207c-112">This level of permission is required because the automatic installation of required MSI packages on the local computer requires privileges that allow reading from and writing to protected local computer resources such as Program Files directories, and protected registry such as the Local Machine hive.</span></span></p>
<div>

> [!TIP]  
> <span data-ttu-id="1207c-113">Vous pouvez également déléguer les autorisations de configuration pour les utilisateurs ou les groupes auxquels vous ne souhaitez pas être membre du groupe administrateurs de domaine.</span><span class="sxs-lookup"><span data-stu-id="1207c-113">You can also delegate setup permissions to users or groups to whom you do not want to grant membership in the Domain Admins group.</span></span> <span data-ttu-id="1207c-114">Pour plus d’informations, reportez-vous à la rubrique <A href="lync-server-2013-granting-setup-permissions.md">octroi d’autorisations de configuration dans Lync Server 2013</A> dans la documentation de déploiement.</span><span class="sxs-lookup"><span data-stu-id="1207c-114">For details, see <A href="lync-server-2013-granting-setup-permissions.md">Granting setup permissions in Lync Server 2013</A> in the Deployment documentation.</span></span>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1207c-115"><strong>Deploy.exe</strong> – appelé par setup.exe, deploy.exe est responsable du déploiement des composants logiciels pour les rôles de serveur.</span><span class="sxs-lookup"><span data-stu-id="1207c-115"><strong>Deploy.exe</strong> – Called by setup.exe, deploy.exe is responsible for the deployment of the software components for the server roles.</span></span></p></td>
<td><p><span data-ttu-id="1207c-116">Membre du groupe Administrateurs local sur l’ordinateur à partir duquel l’exécutable s’exécute.</span><span class="sxs-lookup"><span data-stu-id="1207c-116">Member of the Local Administrators group on the computer from which the executable is run.</span></span> <span data-ttu-id="1207c-117">Membre du groupe utilisateurs de domaine pour lire des informations dans AD DS.</span><span class="sxs-lookup"><span data-stu-id="1207c-117">Member of Domain Users group to read information in AD DS.</span></span> <span data-ttu-id="1207c-118">Ce niveau d’autorisation est requis, car l’installation automatique des packages MSI requis sur l’ordinateur local nécessite des privilèges permettant la lecture et l’écriture des ressources de l’ordinateur local protégé telles que des répertoires de fichiers de programmes et du Registre protégé comme la ruche de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="1207c-118">This level of permission is required because the automatic installation of required MSI packages on the local computer requires privileges that allow reading from and writing to protected local computer resources such as Program Files directories, and protected registry such as the Local Machine hive.</span></span> <span data-ttu-id="1207c-119">L’appartenance au groupe RtcUniversalReadOnlyAdmins est nécessaire pour lire le magasin central de gestion.</span><span class="sxs-lookup"><span data-stu-id="1207c-119">Membership in RtcUniversalReadOnlyAdmins group is necessary to read the Central Management store.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="1207c-120">Si vous utilisez le système d’exploitation Windows Vista ou Windows 7, le contrôle de compte d’utilisateur vous invite à procéder à l’installation.</span><span class="sxs-lookup"><span data-stu-id="1207c-120">If you are running the Windows Vista operating system or Windows 7 operating system, you will be prompted by User Account Control (UAC) to proceed with installation.</span></span> <span data-ttu-id="1207c-121">Si vous avez ouvert une session avec un compte d’utilisateur standard, vous devez disposer d’une personne qui est membre du groupe Administrateurs local pour fournir des informations d’identification lorsque vous y êtes invité à fournir un compte disposant des autorisations d’installation du logiciel.</span><span class="sxs-lookup"><span data-stu-id="1207c-121">If you are logged on with a standard user account, you will need someone who is a member of the Local Administrators group to provide credentials when prompted for an account with permissions to install the software.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1207c-122"><strong>Bootstrapper.exe</strong> – appelé par setup.exe, bootstrapper.exe est responsable du déploiement et de la configuration des rôles de serveur.</span><span class="sxs-lookup"><span data-stu-id="1207c-122"><strong>Bootstrapper.exe</strong> – Called by setup.exe, bootstrapper.exe is responsible for deployment and configuration of server roles.</span></span></p></td>
<td><p><span data-ttu-id="1207c-123">Membre du groupe Administrateurs local sur l’ordinateur à partir duquel l’exécutable s’exécute.</span><span class="sxs-lookup"><span data-stu-id="1207c-123">Member of the Local Administrators group on the computer from which the executable is run.</span></span> <span data-ttu-id="1207c-124">Membre du groupe RTCUniversalServerAdmins pour exécuter Bootstrapper.exe.</span><span class="sxs-lookup"><span data-stu-id="1207c-124">Member of the RTCUniversalServerAdmins group to run Bootstrapper.exe.</span></span> <span data-ttu-id="1207c-125">Membre du groupe utilisateurs de domaine pour lire des informations dans AD DS.</span><span class="sxs-lookup"><span data-stu-id="1207c-125">Member of Domain Users group to read information in AD DS.</span></span> <span data-ttu-id="1207c-126">Ce niveau d’autorisation est requis, car l’installation automatique des packages MSI requis sur l’ordinateur local nécessite des privilèges permettant la lecture et l’écriture des ressources de l’ordinateur local protégé telles que des répertoires de fichiers de programmes et du Registre protégé comme la ruche de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="1207c-126">This level of permission is required because the automatic installation of required MSI packages on the local computer requires privileges that allow reading from and writing to protected local computer resources such as Program Files directories, and protected registry such as the Local Machine hive.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1207c-127"><strong>TopologyBuilder</strong> -interface utilisateur pilotée par l’Assistant pour créer, afficher, ajuster et valider des topologies Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1207c-127"><strong>TopologyBuilder</strong> – Wizard-driven user interface to create, view, adjust, and validate Lync Server 2013 topologies.</span></span></p></td>
<td><p><span data-ttu-id="1207c-128">Membre du groupe Administrateurs local sur l’ordinateur à partir duquel l’exécutable est exécuté pour afficher la topologie.</span><span class="sxs-lookup"><span data-stu-id="1207c-128">Member of the Local Administrators group on the computer from which the executable is run to view the topology.</span></span> <span data-ttu-id="1207c-129">Membre du groupe RTCUniversalServerAdmins pour modifier les paramètres de configuration.</span><span class="sxs-lookup"><span data-stu-id="1207c-129">Member of the RTCUniversalServerAdmins group to change configuration settings.</span></span> <span data-ttu-id="1207c-130">Membre du groupe RTCUniversalServerAdmins et du groupe administrateurs de domaine, ou membre du groupe RTCUniversalServerAdmins (uniquement si le groupe a reçu les autorisations de configuration du délégué), pour publier la topologie.</span><span class="sxs-lookup"><span data-stu-id="1207c-130">Member of the RTCUniversalServerAdmins group and Domain Admins group, or member of the RTCUniversalServerAdmins group (only if the group has been granted delegate setup permissions), to publish the topology.</span></span> <span data-ttu-id="1207c-131">Pour plus d’informations sur la délégation d’autorisations de configuration pour autoriser les membres du groupe de RTCUniversalServerAdmins à publier la topologie sans être membre du groupe administrateurs de domaine, voir <a href="lync-server-2013-granting-setup-permissions.md">octroi d’autorisations de configuration dans Lync Server 2013</a> dans la documentation de déploiement.</span><span class="sxs-lookup"><span data-stu-id="1207c-131">For details about delegating setup permissions to allow members of the RTCUniversalServerAdmins group to publish the topology without being members of the Domain Admins group, see <a href="lync-server-2013-granting-setup-permissions.md">Granting setup permissions in Lync Server 2013</a> in the Deployment documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1207c-132"><strong>AdminUIHost</strong> -interface utilisateur graphique basée sur le Web pour la gestion de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1207c-132"><strong>AdminUIHost</strong> – Web-based graphical user interface for managing Lync Server 2013.</span></span></p></td>
<td><p><span data-ttu-id="1207c-133">Membre du groupe ou membre CsAdministrator d’un autre rôle de contrôle d’accès basé sur un rôle (RBAC) auquel la tâche administrative spécifique est affectée.</span><span class="sxs-lookup"><span data-stu-id="1207c-133">Member of CsAdministrator group or member of another role-based access control (RBAC) role to which the specific administrative task is assigned.</span></span> <span data-ttu-id="1207c-134">Le panneau de configuration de Lync Server 2013 implémente les changements de configuration en exécutant les applets de commande Lync Server 2013 Management Shell.</span><span class="sxs-lookup"><span data-stu-id="1207c-134">Lync Server 2013 Control Panel implements configuration changes by running Lync Server 2013 Management Shell cmdlets.</span></span> <span data-ttu-id="1207c-135">Pour obtenir la liste des rôles prédéfinis et des membres du cmdlet qui peuvent être exécutés, reportez-vous à la section <a href="lync-server-2013-planning-for-role-based-access-control.md">planification du contrôle d’accès basé sur les rôles dans Lync Server 2013</a> dans la documentation de planification.</span><span class="sxs-lookup"><span data-stu-id="1207c-135">For a list of predefined roles and the cmdlets members are permitted to run, see <a href="lync-server-2013-planning-for-role-based-access-control.md">Planning for role-based access control in Lync Server 2013</a> in the Planning documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1207c-136"><strong>PowerShell.exe avec le module Lync Server 2013 chargé</strong> – outil d’administration de la ligne de commande avec des applets de commande spécifiques à la gestion de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1207c-136"><strong>PowerShell.exe with the Lync Server 2013 module loaded</strong> – Command-line administrative tool with cmdlets specific to management of Lync Server 2013.</span></span></p></td>
<td><p><span data-ttu-id="1207c-137">Membre du groupe ou membre de CsAdministrator d’un autre rôle RBAC auquel l’applet de cmdlet spécifique a été attribuée.</span><span class="sxs-lookup"><span data-stu-id="1207c-137">Member of CsAdministrator group or member of another RBAC role to which the specific cmdlet has been assigned.</span></span> <span data-ttu-id="1207c-138">Pour obtenir la liste des rôles prédéfinis et des membres du cmdlet qui peuvent être exécutés, reportez-vous à la section <a href="lync-server-2013-planning-for-role-based-access-control.md">planification du contrôle d’accès basé sur les rôles dans Lync Server 2013</a> dans la documentation de planification.</span><span class="sxs-lookup"><span data-stu-id="1207c-138">For a list of predefined roles and the cmdlets members are permitted to run, see <a href="lync-server-2013-planning-for-role-based-access-control.md">Planning for role-based access control in Lync Server 2013</a> in the Planning documentation.</span></span></p>
<p><span data-ttu-id="1207c-139">Ou membre d’un ou plusieurs des groupes suivants, en fonction de l’applet de commande :</span><span class="sxs-lookup"><span data-stu-id="1207c-139">Or, member of one or more of the following groups, depending on the cmdlet:</span></span></p>
<ul>
<li><p><span data-ttu-id="1207c-140">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="1207c-140">RTCUniversalServerAdmins</span></span></p></li>
<li><p><span data-ttu-id="1207c-141">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="1207c-141">RTCUniversalUserAdmins</span></span></p></li>
<li><p><span data-ttu-id="1207c-142">RTCUniversalReadOnlyAdmins</span><span class="sxs-lookup"><span data-stu-id="1207c-142">RTCUniversalReadOnlyAdmins</span></span></p></li>
</ul></td>
</tr><span data-ttu-id="1207c-143">
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1207c-143">
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span></span></div>

