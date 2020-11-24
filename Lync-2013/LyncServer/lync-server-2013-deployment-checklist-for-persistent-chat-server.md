---
title: 'Lync Server 2013 : Liste de vérification du déploiement pour le serveur de conversation permanente'
description: 'Lync Server 2013 : liste de vérification de déploiement pour le serveur de chat permanent.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment checklist for Persistent Chat Server
ms:assetid: b1108f8f-88a2-4660-8086-d25ba76f7239
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412851(v=OCS.15)
ms:contentKeyID: 48185155
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 28d96da5e2961634e6a81450796e5d1ae3426819
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394620"
---
# <a name="deployment-checklist-for-persistent-chat-server-in-lync-server-2013"></a><span data-ttu-id="88466-103">Liste de vérification du déploiement pour le serveur de conversation permanente dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="88466-103">Deployment checklist for Persistent Chat Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="88466-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="88466-104">

<span> </span></span></span>

<span data-ttu-id="88466-105">_**Dernière modification de la rubrique :** 2012-10-16_</span><span class="sxs-lookup"><span data-stu-id="88466-105">_**Topic Last Modified:** 2012-10-16_</span></span>

<span data-ttu-id="88466-106">Le déploiement de Lync Server 2013, de chat permanent serveur nécessite que vous le déployiez dans l’ordre approprié et que vous ayez effectué toutes les étapes de déploiement requises.</span><span class="sxs-lookup"><span data-stu-id="88466-106">Deployment of Lync Server 2013, Persistent Chat Server requires that you deploy it in the correct sequence and that you complete all required deployment steps.</span></span>

<div>

## <a name="deployment-sequence"></a><span data-ttu-id="88466-107">Séquence de déploiement</span><span class="sxs-lookup"><span data-stu-id="88466-107">Deployment Sequence</span></span>

<span data-ttu-id="88466-108">Vous pouvez déployer le serveur de chat permanent après le déploiement de votre topologie initiale, y compris au moins un serveur Lync Server 2013, un pool frontal ou un serveur Lync Server 2013, Standard Edition Server.</span><span class="sxs-lookup"><span data-stu-id="88466-108">You can deploy Persistent Chat Server after you deploy your initial topology, including at least one Lync Server 2013, Front End pool or one Lync Server 2013, Standard Edition server.</span></span> <span data-ttu-id="88466-109">Cette rubrique décrit la procédure de déploiement d’un serveur de chat permanent en l’ajoutant à un déploiement existant.</span><span class="sxs-lookup"><span data-stu-id="88466-109">This topic describes how to deploy Persistent Chat Server by adding it to an existing deployment.</span></span>

</div>

<div>

## <a name="deployment-process"></a><span data-ttu-id="88466-110">Processus de déploiement</span><span class="sxs-lookup"><span data-stu-id="88466-110">Deployment Process</span></span>

<span data-ttu-id="88466-111">Le tableau suivant répertorie les étapes de base de déploiement d’un serveur de conversation permanent et fournit des liens pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="88466-111">The following table lists the basic steps to deploy Persistent Chat Server and provides links for more details.</span></span>

### <a name="persistent-chat-server-deployment-process"></a><span data-ttu-id="88466-112">Processus de déploiement d’un serveur de chat permanent</span><span class="sxs-lookup"><span data-stu-id="88466-112">Persistent Chat Server Deployment Process</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="88466-113">Tâche</span><span class="sxs-lookup"><span data-stu-id="88466-113">Task</span></span></th>
<th><span data-ttu-id="88466-114">Étapes</span><span class="sxs-lookup"><span data-stu-id="88466-114">Steps</span></span></th>
<th><span data-ttu-id="88466-115">Rôles et appartenance aux groupes nécessaires</span><span class="sxs-lookup"><span data-stu-id="88466-115">Required roles and group memberships</span></span></th>
<th><span data-ttu-id="88466-116">Rubriques associées</span><span class="sxs-lookup"><span data-stu-id="88466-116">Related topics</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="88466-117"><strong>Installer le matériel et les logiciels prérequis</strong></span><span class="sxs-lookup"><span data-stu-id="88466-117"><strong>Install prerequisite hardware and software</strong></span></span></p></td>
<td><p><span data-ttu-id="88466-118">Sur le matériel conforme à la configuration système requise, installez ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="88466-118">On hardware that meets system requirements, install the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="88466-119">Sur les serveurs front-end serveur Chat permanent :</span><span class="sxs-lookup"><span data-stu-id="88466-119">On the Persistent Chat Server Front End Servers:</span></span></p></li>
</ul>
<ul>
<li><p><span data-ttu-id="88466-120">Un système d’exploitation conforme à la configuration système requise</span><span class="sxs-lookup"><span data-stu-id="88466-120">An operating system that meets system requirements</span></span></p></li>
<li><p><span data-ttu-id="88466-121">Configuration logicielle requise pour les ordinateurs exécutant Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="88466-121">Software prerequisites for computers running Lync Server 2013</span></span></p></li>
<li><p><span data-ttu-id="88466-122">Serveur SQL Server sur le serveur qui héberge la base de données de serveur Chat permanent</span><span class="sxs-lookup"><span data-stu-id="88466-122">SQL Server on the server that will host Persistent Chat Server database</span></span></p></li>
</ul>
<p><span data-ttu-id="88466-123">Si la conformité du serveur Chat permanent est requise :</span><span class="sxs-lookup"><span data-stu-id="88466-123">If Persistent Chat Server compliance is required:</span></span></p>
<ul>
<li><p><span data-ttu-id="88466-124">Serveur SQL Server sur le serveur qui héberge la base de données de compatibilité serveur Chat permanent</span><span class="sxs-lookup"><span data-stu-id="88466-124">SQL Server on the server that will host Persistent Chat Server compliance database</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="88466-125">Un utilisateur membre du groupe Administrateurs local.</span><span class="sxs-lookup"><span data-stu-id="88466-125">Any user who is a member of the local Administrators group.</span></span></p></td>
<td><p><span data-ttu-id="88466-126"><a href="lync-server-2013-supported-hardware.md">Matériel compatible pour Lync Server 2013</a> dans la documentation de prise en charge</span><span class="sxs-lookup"><span data-stu-id="88466-126"><a href="lync-server-2013-supported-hardware.md">Supported hardware for Lync Server 2013</a> in the Supportability documentation</span></span></p>
<p><span data-ttu-id="88466-127"><a href="lync-server-2013-server-software-and-infrastructure-support.md">Support du logiciel serveur et de l’infrastructure dans Lync Server 2013</a> dans la documentation de prise en charge</span><span class="sxs-lookup"><span data-stu-id="88466-127"><a href="lync-server-2013-server-software-and-infrastructure-support.md">Server software and infrastructure support in Lync Server 2013</a> in the Supportability documentation</span></span></p>
<p><span data-ttu-id="88466-128"><a href="lync-server-2013-determining-your-system-requirements.md">Détermination de la configuration système requise pour Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="88466-128"><a href="lync-server-2013-determining-your-system-requirements.md">Determining your system requirements for Lync Server 2013</a></span></span></p>
<p><span data-ttu-id="88466-129"><a href="lync-server-2013-technical-requirements-for-persistent-chat-server.md">Configuration requise pour le serveur de chat permanent dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="88466-129"><a href="lync-server-2013-technical-requirements-for-persistent-chat-server.md">Technical requirements for Persistent Chat Server in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88466-130"><strong>Créer la topologie interne appropriée pour prendre en charge le serveur de chat permanent (et éventuellement la conformité avec la conversation permanente)</strong></span><span class="sxs-lookup"><span data-stu-id="88466-130"><strong>Create the appropriate internal topology to support Persistent Chat Server (and optionally, Persistent Chat compliance)</strong></span></span></p></td>
<td><p><span data-ttu-id="88466-131">Exécutez le générateur de topologie pour ajouter un pool de serveurs de chat permanent à votre topologie :</span><span class="sxs-lookup"><span data-stu-id="88466-131">Run Topology Builder to add a Persistent Chat Server pool to your topology:</span></span></p>
<ul>
<li><p><span data-ttu-id="88466-132">Ajouter des composants serveur de chat permanent à la topologie</span><span class="sxs-lookup"><span data-stu-id="88466-132">Add Persistent Chat Server components to the topology</span></span></p></li>
<li><p><span data-ttu-id="88466-133">Créer une base de données SQL Server pour le magasin serveur Chat permanent (et un serveur SQL de sauvegarde pour la récupération d’urgence)</span><span class="sxs-lookup"><span data-stu-id="88466-133">Create a SQL Server database for the Persistent Chat Server store (and a backup SQL Server for disaster recovery)</span></span></p></li>
<li><p><span data-ttu-id="88466-134">Définir un nouveau magasin de fichiers Lync ou utiliser un magasin de fichiers Lync existant pour les fichiers du serveur de chat permanent</span><span class="sxs-lookup"><span data-stu-id="88466-134">Define a new Lync File Store or use an existing Lync File Store for Persistent Chat Server files</span></span></p></li>
<li><p><span data-ttu-id="88466-135">Associez le pool Lync Server 2013 qui peut acheminer les demandes vers ce pool de serveurs de chat permanent.</span><span class="sxs-lookup"><span data-stu-id="88466-135">Associate the Lync Server 2013 pool that can route requests to this Persistent Chat Server pool</span></span></p></li>
</ul>
<p><span data-ttu-id="88466-136">Si la conformité de conversation permanente est requise :</span><span class="sxs-lookup"><span data-stu-id="88466-136">If Persistent Chat compliance is required:</span></span></p>
<ul>
<li><p><span data-ttu-id="88466-137">Ajouter un magasin de conformité des conversations permanentes</span><span class="sxs-lookup"><span data-stu-id="88466-137">Add Persistent Chat Compliance Store</span></span></p></li>
<li><p><span data-ttu-id="88466-138">Cliquez sur la case à cocher de la définition de pool de serveurs de conversation permanente pour activer la conformité</span><span class="sxs-lookup"><span data-stu-id="88466-138">Click the Persistent Chat Server pool definition check box for enabling compliance</span></span></p></li>
<li><p><span data-ttu-id="88466-139">Publication de la topologie</span><span class="sxs-lookup"><span data-stu-id="88466-139">Publish the topology</span></span></p></li>
</ul>
<p><span data-ttu-id="88466-140">Si vous installez le serveur Chat permanent sur l’édition standard, le nom de domaine complet (FQDN) du pool de serveurs de chat permanent doit correspondre au serveur Standard Edition Server, et les bases de données SQL Server sont colocalisées sur l’instance SQL Server Express sur le serveur Standard Edition Server</span><span class="sxs-lookup"><span data-stu-id="88466-140">If you install Persistent Chat Server on Standard Edition, the fully qualified domain name (FQDN) of the Persistent Chat Server pool must match the Standard Edition server, and the SQL Server databases are collocated on the SQL Server Express instance on the Standard Edition server</span></span></p></td>
<td><p><span data-ttu-id="88466-141">Pour définir une topologie, un compte membre du groupe Utilisateurs local</span><span class="sxs-lookup"><span data-stu-id="88466-141">To define a topology, an account that is a member of the local Users group.</span></span></p>
<p><span data-ttu-id="88466-142">Pour publier la topologie, un compte membre du groupe administrateurs de domaine et du groupe RTCUniversalServerAdmins et l’utilisateur doit également disposer des autorisations de contrôle total (lecture/écriture/modification) sur le magasin de fichiers Lync pour les fichiers du serveur de chat permanent (de sorte que le générateur de topologie puisse configurer les DACL requis).</span><span class="sxs-lookup"><span data-stu-id="88466-142">To publish the topology, an account that is a member of the Domain Admins group and RTCUniversalServerAdmins group, and the user should also have full control permissions (read/write/modify) on the Lync File Store for Persistent Chat Server files (so that Topology Builder can configure the required DACLs).</span></span></p></td>
<td><p><span data-ttu-id="88466-143"><a href="lync-server-2013-adding-persistent-chat-server-to-your-deployment.md">Ajouter un serveur de chat permanent à votre déploiement dans Lync Server 2013</a> dans la documentation de déploiement</span><span class="sxs-lookup"><span data-stu-id="88466-143"><a href="lync-server-2013-adding-persistent-chat-server-to-your-deployment.md">Adding Persistent Chat Server to your deployment in Lync Server 2013</a> in the Deployment documentation</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88466-144"><strong>Déployer un serveur de conversation permanente</strong></span><span class="sxs-lookup"><span data-stu-id="88466-144"><strong>Deploy Persistent Chat Server</strong></span></span></p></td>
<td><p><span data-ttu-id="88466-145">Exécutez le programme d’installation de Lync Server sur tous les ordinateurs exécutant la fonction de chat permanent serveur.</span><span class="sxs-lookup"><span data-stu-id="88466-145">Run the Lync Server setup on all the computers running Persistent Chat Server.</span></span> <span data-ttu-id="88466-146">La configuration du serveur de chat permanent est intégrée à l’Assistant Déploiement de Lync Server 2013, qui fournit les instructions suivantes :</span><span class="sxs-lookup"><span data-stu-id="88466-146">The Persistent Chat Server setup is integrated into the Lync Server 2013 Deployment wizard that provides the following instructions:</span></span></p>
<ul>
<li><p><span data-ttu-id="88466-147">Déployer le magasin de gestion local</span><span class="sxs-lookup"><span data-stu-id="88466-147">Deploy local management store</span></span></p></li>
<li><p><span data-ttu-id="88466-148">Installer les services serveur de chat permanent</span><span class="sxs-lookup"><span data-stu-id="88466-148">Install Persistent Chat Server services</span></span></p></li>
<li><p><span data-ttu-id="88466-149">Demander et affecter des certificats</span><span class="sxs-lookup"><span data-stu-id="88466-149">Request and assign certificates</span></span></p></li>
<li><p><span data-ttu-id="88466-150">Exécuter et démarrer les services</span><span class="sxs-lookup"><span data-stu-id="88466-150">Run and start the services</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="88466-151">Un utilisateur membre du groupe Administrateurs local.</span><span class="sxs-lookup"><span data-stu-id="88466-151">Any user who is a member of the local Administrators group.</span></span></p></td>
<td><p><span data-ttu-id="88466-152"><a href="lync-server-2013-deploying-persistent-chat-server.md">Déploiement d’un serveur de chat permanent dans Lync Server 2013</a> dans la documentation de déploiement</span><span class="sxs-lookup"><span data-stu-id="88466-152"><a href="lync-server-2013-deploying-persistent-chat-server.md">Deploying Persistent Chat Server in Lync Server 2013</a> in the Deployment documentation</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88466-153"><strong>Créer un administrateur de conversation permanente</strong></span><span class="sxs-lookup"><span data-stu-id="88466-153"><strong>Create a Persistent Chat administrator</strong></span></span></p></td>
<td><p><span data-ttu-id="88466-154">Ajoutez des utilisateurs au groupe de sécurité CsPersistentChatAdministrator.</span><span class="sxs-lookup"><span data-stu-id="88466-154">Add users to the CsPersistentChatAdministrator security group.</span></span></p></td>
<td><p><span data-ttu-id="88466-155">Un utilisateur membre des administrateurs de domaines.</span><span class="sxs-lookup"><span data-stu-id="88466-155">Any user who is a member of domain administrators.</span></span></p></td>
<td><p><span data-ttu-id="88466-156"><a href="lync-server-2013-adding-a-persistent-chat-administrator.md">Ajouter un administrateur de chat permanent dans Lync Server 2013</a> dans la documentation de déploiement</span><span class="sxs-lookup"><span data-stu-id="88466-156"><a href="lync-server-2013-adding-a-persistent-chat-administrator.md">Adding a Persistent Chat administrator in Lync Server 2013</a> in the Deployment documentation</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88466-157"><strong>Configuration du serveur de conversation permanente</strong></span><span class="sxs-lookup"><span data-stu-id="88466-157"><strong>Configure Persistent Chat Server</strong></span></span></p></td>
<td><p><span data-ttu-id="88466-158">Configurez les utilisateurs :</span><span class="sxs-lookup"><span data-stu-id="88466-158">Configure users:</span></span></p>
<ul>
<li><p><span data-ttu-id="88466-159">La stratégie doit être activée pour permettre à l’utilisateur d’accéder au serveur de chat permanent.</span><span class="sxs-lookup"><span data-stu-id="88466-159">User has to be enabled by policy to access Persistent Chat Server.</span></span> <span data-ttu-id="88466-160">Par défaut, la stratégie est désactivée pour tous les utilisateurs et peut être définie au niveau de l’étendue globale/Site/Pool/Utilisateur.</span><span class="sxs-lookup"><span data-stu-id="88466-160">By default, the policy is turned off for all users and can be defined at global/site/pool/user scopes.</span></span></p></li>
<li><p><span data-ttu-id="88466-161">Configurer les paramètres</span><span class="sxs-lookup"><span data-stu-id="88466-161">Configure settings</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="88466-p104">L’utilisateur doit être membre du groupe CsPersistentChatAdministrator. Pour changer de stratégie, l’utilisateur doit au moins faire partie du groupe CsUserAdministrator.</span><span class="sxs-lookup"><span data-stu-id="88466-p104">User must be a member of CsPersistentChatAdministrator. To change policy, user must be in CsUserAdministrator, at a minimum.</span></span></p></td>
<td><p><span data-ttu-id="88466-164"><a href="lync-server-2013-configuring-persistent-chat-server.md">Configuration du serveur de chat permanent dans Lync Server 2013</a> dans la documentation de déploiement</span><span class="sxs-lookup"><span data-stu-id="88466-164"><a href="lync-server-2013-configuring-persistent-chat-server.md">Configuring Persistent Chat Server in Lync Server 2013</a> in the Deployment documentation</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!IMPORTANT]  
> <span data-ttu-id="88466-165">Vous pouvez déployer un ou plusieurs pools de serveurs de chat permanent.</span><span class="sxs-lookup"><span data-stu-id="88466-165">You can deploy one or more Persistent Chat Server pools.</span></span> <span data-ttu-id="88466-166">Nous prenons en charge plusieurs pools de serveurs de chat permanent pour des raisons réglementaires dans lesquelles les données générées dans une région donnée doivent rester dans cette région.</span><span class="sxs-lookup"><span data-stu-id="88466-166">We support multiple Persistent Chat Server pools for regulatory reasons whereby data generated in a given region is required to stay in that region.</span></span> <span data-ttu-id="88466-167">Par exemple, si vous déployez un pool de serveurs de chat permanent à Chicago et un autre sur Zurich pour se conformer aux réglementations relatives aux données en Suisse, les utilisateurs peuvent se connecter aux salles dans les pools de serveurs de chat permanent, à condition qu’ils y aient accès.</span><span class="sxs-lookup"><span data-stu-id="88466-167">For example, if you deploy a Persistent Chat Server pool in Chicago, and another in Zurich to comply with regulations for data in Switzerland, users can connect to rooms in both the Persistent Chat Server pools, provided they have access.</span></span>



<span data-ttu-id="88466-168"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="88466-168"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

