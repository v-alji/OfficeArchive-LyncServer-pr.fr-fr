---
title: Configuration des fédérations SIP et XMPP et de la messagerie instantanée publique
description: Configuration de la Fédération SIP et de la Fédération de XMPP et de la messagerie instantanée publique.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring SIP federation, XMPP federation and public instant messaging
ms:assetid: a6d04f0b-5cb8-4084-a3a2-d501938971f9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205134(v=OCS.15)
ms:contentKeyID: 48184998
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7b83c29da75c99e7a338bfd7732aec8ec49cbf47
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432652"
---
# <a name="configuring-sip-federation-xmpp-federation-and-public-instant-messaging-in-lync-server-2013"></a><span data-ttu-id="b41e5-103">Configuration des fédérations SIP et XMPP et de la messagerie instantanée publique dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b41e5-103">Configuring SIP federation, XMPP federation and public instant messaging in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b41e5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b41e5-104">

<span> </span></span></span>

<span data-ttu-id="b41e5-105">_**Dernière modification de la rubrique :** 2013-10-07_</span><span class="sxs-lookup"><span data-stu-id="b41e5-105">_**Topic Last Modified:** 2013-10-07_</span></span>

<span data-ttu-id="b41e5-106">La Fédération, la connectivité de messagerie instantanée publique et le protocole XMPP (extensible Messaging and Presence Protocol) définissent une catégorie différente d’utilisateurs externes – utilisateurs fédérés.</span><span class="sxs-lookup"><span data-stu-id="b41e5-106">Federation, public instant messaging connectivity and Extensible Messaging and Presence Protocol (XMPP) define a different class of external users – Federated users.</span></span> <span data-ttu-id="b41e5-107">Les utilisateurs d’un déploiement de déploiement de Lync Server ou de déploiement XMPP peuvent avoir accès à un ensemble de services limité et être authentifiés par le déploiement externe.</span><span class="sxs-lookup"><span data-stu-id="b41e5-107">Users of a federated Lync Server deployment or XMPP deployment have access to a limited set of services and are authenticated by the external deployment.</span></span> <span data-ttu-id="b41e5-108">Les utilisateurs distants sont membres de votre déploiement Lync Server et ont accès à tous les services proposés par votre déploiement.</span><span class="sxs-lookup"><span data-stu-id="b41e5-108">Remote users are members of your Lync Server deployment and have access to all services offered by your deployment.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="b41e5-109">Date de fin de vie du 2014 juin pour AOL et Yahoo !</span><span class="sxs-lookup"><span data-stu-id="b41e5-109">An end of life date of June 2014 for AOL and Yahoo!</span></span> <span data-ttu-id="b41e5-110">a été annoncé.</span><span class="sxs-lookup"><span data-stu-id="b41e5-110">has been announced.</span></span> <span data-ttu-id="b41e5-111">Pour plus d’informations, voir <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">prise en charge de la connectivité de messagerie instantanée publique dans Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="b41e5-111">For details, see <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Support for public instant messenger connectivity in Lync Server 2013</A>.</span></span>



</div>

<span data-ttu-id="b41e5-112">La connectivité de messagerie instantanée publique est un type spécial de Fédération qui permet à un client du serveur Lync d’accéder aux fournisseurs de messagerie instantanée publics à l’aide de la 2013 Lync.</span><span class="sxs-lookup"><span data-stu-id="b41e5-112">Public instant messaging connectivity is a special type of federation that allows a Lync Server client to access configured public Instant Messaging partners using the Lync 2013.</span></span> <span data-ttu-id="b41e5-113">Les partenaires de connectivité de messagerie instantanée publics actuels sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="b41e5-113">The current public instant messaging connectivity partners are:</span></span>

  - <span></span>  
    <span data-ttu-id="b41e5-114">America Online</span><span class="sxs-lookup"><span data-stu-id="b41e5-114">America Online</span></span>

  - <span></span>  
    <span data-ttu-id="b41e5-115">Windows Live</span><span class="sxs-lookup"><span data-stu-id="b41e5-115">Windows Live</span></span>

  - <span></span>  
    <span data-ttu-id="b41e5-116">Yahoo !\!</span><span class="sxs-lookup"><span data-stu-id="b41e5-116">Yahoo\!</span></span>

<span data-ttu-id="b41e5-117">Une configuration de connectivité de messagerie instantanée publique permet aux utilisateurs de Lync d’accéder aux utilisateurs de la connectivité de messagerie instantanée publique de la façon suivante :</span><span class="sxs-lookup"><span data-stu-id="b41e5-117">A public instant messaging connectivity configuration allows Lync users access to public instant messaging connectivity users by:</span></span>

  - <span data-ttu-id="b41e5-118">Messagerie instantanée et présence</span><span class="sxs-lookup"><span data-stu-id="b41e5-118">IM and Presence</span></span>

  - <span data-ttu-id="b41e5-119">Visibilité des contacts sur la connectivité de messagerie instantanée publique dans le client Lync</span><span class="sxs-lookup"><span data-stu-id="b41e5-119">Visibility of public instant messaging connectivity contacts in Lync client</span></span>

  - <span data-ttu-id="b41e5-120">Personne à personne conversations par messagerie instantanée avec les contacts</span><span class="sxs-lookup"><span data-stu-id="b41e5-120">Person to person IM conversations with contacts</span></span>

  - <span data-ttu-id="b41e5-121">Appels audio et vidéo avec les utilisateurs de Windows Live</span><span class="sxs-lookup"><span data-stu-id="b41e5-121">Audio and video calls with Windows Live users</span></span>

<span data-ttu-id="b41e5-122">Lync Server Federation définit un accord entre le déploiement de votre serveur Lync et d’autres déploiements Office Communications Server 2007 R2 ou Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b41e5-122">Lync Server federation defines an agreement between your Lync Server deployment and other Office Communications Server 2007 R2 or Lync Server deployments.</span></span> <span data-ttu-id="b41e5-123">Une configuration fédérée de Lync Server permet aux utilisateurs de Lync d’accéder aux utilisateurs fédérés en procédant comme suit :</span><span class="sxs-lookup"><span data-stu-id="b41e5-123">A Lync Server federated configuration allows Lync users access to federated users by:</span></span>

  - <span data-ttu-id="b41e5-124">Messagerie instantanée et présence</span><span class="sxs-lookup"><span data-stu-id="b41e5-124">IM and Presence</span></span>

  - <span data-ttu-id="b41e5-125">Création de contacts fédérés dans le client Lync</span><span class="sxs-lookup"><span data-stu-id="b41e5-125">Creation of federated contacts in the Lync client</span></span>

<span data-ttu-id="b41e5-126">La Fédération XMPP définit un déploiement externe en fonction du protocole de messagerie eXtensible et de présence.</span><span class="sxs-lookup"><span data-stu-id="b41e5-126">XMPP federation defines an external deployment based on the eXtensible Messaging and Presence Protocol.</span></span> <span data-ttu-id="b41e5-127">Une configuration XMPP permet aux utilisateurs de Lync d’accéder aux utilisateurs de domaine XMPP autorisés en procédant comme suit :</span><span class="sxs-lookup"><span data-stu-id="b41e5-127">An XMPP configuration allows Lync users access to allowed XMPP domain users by:</span></span>

  - <span data-ttu-id="b41e5-128">Messagerie instantanée et présence-personne à personne uniquement</span><span class="sxs-lookup"><span data-stu-id="b41e5-128">IM and Presence – person to person only</span></span>

  - <span data-ttu-id="b41e5-129">Créer des contacts fédérés de XMPP dans le client Lync</span><span class="sxs-lookup"><span data-stu-id="b41e5-129">Creation of XMPP federated contacts in the Lync client</span></span>

<div>


> [!IMPORTANT]
> <span data-ttu-id="b41e5-p106">La fonctionnalité XMPP de Lync Server 2013 est testée et prise en charge par Microsoft pour la fédération de messagerie instantanée avec Google Talk. Pour d’autres systèmes XMPP, contactez le fournisseur tier pour vérifier qu’il prend en charge la fédération avec Lync Server 2013 et pour obtenir d’autres recommandations de déploiement et de dépannage.</span><span class="sxs-lookup"><span data-stu-id="b41e5-p106">The XMPP capability of Lync Server 2013 is tested and supported by Microsoft for instant messaging federation with Google Talk. For any other XMPP systems contact the third-party vendor to verify that they support federation with Lync Server 2013, and for any deployment or troubleshooting recommendations.</span></span>



</div>

<div>

## <a name="edge-server-external-federation-public-instant-messaging-connectivity-and-xmpp-users-deployment-process"></a><span data-ttu-id="b41e5-132">Processus de déploiement de la Fédération externe du serveur Edge, de la connectivité de messagerie instantanée publique et du processus de déploiement des utilisateurs XMPP</span><span class="sxs-lookup"><span data-stu-id="b41e5-132">Edge Server External Federation, Public Instant Messaging Connectivity and XMPP Users Deployment Process</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b41e5-133">Phase</span><span class="sxs-lookup"><span data-stu-id="b41e5-133">Phase</span></span></th>
<th><span data-ttu-id="b41e5-134">Étapes</span><span class="sxs-lookup"><span data-stu-id="b41e5-134">Steps</span></span></th>
<th><span data-ttu-id="b41e5-135">Autorisations</span><span class="sxs-lookup"><span data-stu-id="b41e5-135">Permissions</span></span></th>
<th><span data-ttu-id="b41e5-136">Documentation</span><span class="sxs-lookup"><span data-stu-id="b41e5-136">Documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b41e5-137">Déterminez les options à ajouter au déploiement Edge existant.</span><span class="sxs-lookup"><span data-stu-id="b41e5-137">Determine the options to add to the existing Edge deployment</span></span></p></td>
<td><p><span data-ttu-id="b41e5-138">Exécutez le générateur de topologie pour modifier les paramètres du serveur de bord et créez et publiez la topologie.</span><span class="sxs-lookup"><span data-stu-id="b41e5-138">Run Topology Builder to edit Edge Server settings and create and publish the topology.</span></span> <span data-ttu-id="b41e5-139">Votre topologie de périphérie existante réplique les modifications du magasin central de gestion sur le serveur Edge.</span><span class="sxs-lookup"><span data-stu-id="b41e5-139">Your existing Edge topology will replicate changes from the Central Management store to the Edge Server.</span></span></p></td>
<td><p><span data-ttu-id="b41e5-140">Groupe administrateurs de domaine et groupe RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="b41e5-140">Domain Admins group and RTCUniversalServerAdmins group</span></span></p>



> [!NOTE]
> <span data-ttu-id="b41e5-141">Vous pouvez modifier une topologie à l’aide d’un compte membre du groupe utilisateurs locaux, mais la publication d’une topologie nécessite un compte membre du groupe administrateurs de domaine et du groupe RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="b41e5-141">You can edit a topology using an account that is a member of the local users group, but publishing a topology requires an account that is a member of the Domain Admins group and the RTCUniversalServerAdmins group</span></span>

</td>
<td><p><span data-ttu-id="b41e5-142"><a href="lync-server-2013-building-an-edge-and-director-topology.md">Création d’une topologie de serveurs Edge et directeurs dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="b41e5-142"><a href="lync-server-2013-building-an-edge-and-director-topology.md">Building an edge and Director topology in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b41e5-143">Préparer l’installation</span><span class="sxs-lookup"><span data-stu-id="b41e5-143">Prepare for setup</span></span></p></td>
<td><ol>
<li><p><span data-ttu-id="b41e5-144">Vérifiez que les conditions système préalables sont remplies.</span><span class="sxs-lookup"><span data-stu-id="b41e5-144">Ensure that system prerequisites are met.</span></span></p></li>
<li><p><span data-ttu-id="b41e5-145">Configurer les enregistrements DNS internes et externes pour la prise en charge de la connectivité de messagerie instantanée publique, de la Fédération Lync et de la Fédération de XMPP</span><span class="sxs-lookup"><span data-stu-id="b41e5-145">Configure internal and external DNS records, to support public instant messaging connectivity, Lync Federation and XMPP Federation</span></span></p></li>
<li><p><span data-ttu-id="b41e5-146">Configurer les ports et les protocoles dans le pare-feu pour prendre en charge les types de Fédération que vous déployez</span><span class="sxs-lookup"><span data-stu-id="b41e5-146">Configure ports and protocols at the firewall to support the types of federation that you are deploying</span></span></p></li>
<li><p><span data-ttu-id="b41e5-147">Obtenez et installez des certificats publics.</span><span class="sxs-lookup"><span data-stu-id="b41e5-147">Obtain and install public certificates.</span></span> <span data-ttu-id="b41e5-148">Le temps requis pour obtenir des certificats dépend de l’autorité de certification qui émet le certificat.</span><span class="sxs-lookup"><span data-stu-id="b41e5-148">The time required to obtain certificates depends on which certification authority (CA) issues the certificate.</span></span> <span data-ttu-id="b41e5-149">Cette étape est facultative à ce stade du déploiement.</span><span class="sxs-lookup"><span data-stu-id="b41e5-149">This step is optional at this point in the deployment.</span></span> <span data-ttu-id="b41e5-150">Si vous n’effectuez pas cette étape à ce stade, vous devez le faire pendant la configuration du serveur de périmètre.</span><span class="sxs-lookup"><span data-stu-id="b41e5-150">If you do not perform this step at this point, you must do it during Edge Server configuration.</span></span> <span data-ttu-id="b41e5-151">Le service Edge Server ne peut pas être démarré tant qu’aucun certificat n’est obtenu</span><span class="sxs-lookup"><span data-stu-id="b41e5-151">The Edge Server service cannot be started until certificates are obtained</span></span></p></li>
</ol></td>
<td><p><span data-ttu-id="b41e5-152">En fonction de votre organisation, car ces rôles sont généralement répartis entre de nombreux groupes de tâches.</span><span class="sxs-lookup"><span data-stu-id="b41e5-152">As appropriate to your organization, as these roles are typically split amongst numerous work groups</span></span></p></td>
<td><p><span data-ttu-id="b41e5-153"><a href="lync-server-2013-planning-for-sip-xmpp-federation-and-public-instant-messaging.md">Planification de la Fédération SIP, de XMPP et de la messagerie instantanée publique dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="b41e5-153"><a href="lync-server-2013-planning-for-sip-xmpp-federation-and-public-instant-messaging.md">Planning for SIP, XMPP federation, and public instant messaging in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b41e5-154">Configurer des serveurs de périphérie pour des scénarios de Fédération</span><span class="sxs-lookup"><span data-stu-id="b41e5-154">Set up Edge Servers for Federation Scenarios</span></span></p></td>
<td><ol>
<li><p><span data-ttu-id="b41e5-155">Transférez le fichier de configuration topologique exporté vers chaque serveur Edge ou attendez la fin de la réplication.</span><span class="sxs-lookup"><span data-stu-id="b41e5-155">Transport the exported topology configuration file to each Edge Server or allow replication to complete</span></span></p></li>
<li><p><span data-ttu-id="b41e5-156">Re-Run l’Assistant déploiement pour installer les composants de prise en charge de la Fédération</span><span class="sxs-lookup"><span data-stu-id="b41e5-156">Re-Run the Deployment Wizard to install supporting components for Federation</span></span></p></li>
<li><p><span data-ttu-id="b41e5-157">Configurer les serveurs de périphérie</span><span class="sxs-lookup"><span data-stu-id="b41e5-157">Configure the Edge Servers</span></span></p></li>
<li><p><span data-ttu-id="b41e5-158">Demander et installer des certificats pour chaque serveur Edge</span><span class="sxs-lookup"><span data-stu-id="b41e5-158">Request and install certificates for each Edge Server</span></span></p></li>
<li><p><span data-ttu-id="b41e5-159">Redémarrer les services Edge Server</span><span class="sxs-lookup"><span data-stu-id="b41e5-159">Restart the Edge Server services</span></span></p></li>
</ol></td>
<td><p><span data-ttu-id="b41e5-160">Groupe administrateurs</span><span class="sxs-lookup"><span data-stu-id="b41e5-160">Administrators group</span></span></p></td>
<td><p><span data-ttu-id="b41e5-161"><a href="lync-server-2013-setting-up-lync-federation.md">Configuration de la fédération Lync dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="b41e5-161"><a href="lync-server-2013-setting-up-lync-federation.md">Setting up Lync federation in Lync Server 2013</a></span></span></p>
<p><span data-ttu-id="b41e5-162"><a href="lync-server-2013-setting-up-public-instant-messaging-connectivity.md">Configuration de la connectivité PIC dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="b41e5-162"><a href="lync-server-2013-setting-up-public-instant-messaging-connectivity.md">Setting up public instant messaging connectivity in Lync Server 2013</a></span></span></p>
<p><span data-ttu-id="b41e5-163"><a href="lync-server-2013-setting-up-xmpp-federation.md">Configuration de la fédération XMPP dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="b41e5-163"><a href="lync-server-2013-setting-up-xmpp-federation.md">Setting up XMPP federation in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b41e5-164">Configurer la prise en charge de l’accès des utilisateurs externes.</span><span class="sxs-lookup"><span data-stu-id="b41e5-164">Configure support for external user access.</span></span></p></td>
<td><ol>
<li><p><span data-ttu-id="b41e5-165">Utiliser l’accès aux utilisateurs externes de Lync Server Control Panel</span><span class="sxs-lookup"><span data-stu-id="b41e5-165">Use the Lync Server Control Panel External User Access</span></span></p></li>
<li><p><span data-ttu-id="b41e5-166">Configurer une stratégie d’accès externe pour activer les communications avec les utilisateurs fédérés ou les utilisateurs publics</span><span class="sxs-lookup"><span data-stu-id="b41e5-166">Configure External Access Policy to enable Communications with federated users or public users</span></span></p></li>
<li><p><span data-ttu-id="b41e5-167">Configurer des domaines fédérés SIP pour autoriser ou bloquer des domaines</span><span class="sxs-lookup"><span data-stu-id="b41e5-167">Configure SIP Federated Domains to Allow or Block domains</span></span></p></li>
<li><p><span data-ttu-id="b41e5-168">Activer les fournisseurs fédérés SIP pour les fournisseurs de connectivité de messagerie instantanée publics</span><span class="sxs-lookup"><span data-stu-id="b41e5-168">Enable SIP Federated Providers for public instant messaging connectivity providers</span></span></p></li>
<li><p><span data-ttu-id="b41e5-169">Configurer des partenaires fédérés de XMPP par domaine XMPP</span><span class="sxs-lookup"><span data-stu-id="b41e5-169">Configure XMPP Federated Partners per XMPP domain</span></span></p></li>
</ol></td>
<td><p><span data-ttu-id="b41e5-170">RTCUniversalServerAdmins groupe ou compte d’utilisateur affecté au rôle CSAdministrator</span><span class="sxs-lookup"><span data-stu-id="b41e5-170">RTCUniversalServerAdmins group or user account that is assigned to the CSAdministrator role</span></span></p></td>
<td><p><span data-ttu-id="b41e5-171"><a href="lync-server-2013-configuring-support-for-external-user-access.md">Configuration de la prise en charge de l’accès des utilisateurs externes dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="b41e5-171"><a href="lync-server-2013-configuring-support-for-external-user-access.md">Configuring support for external user access in Lync Server 2013</a></span></span></p>
<p><span data-ttu-id="b41e5-172"><a href="lync-server-2013-configure-media-encryption-for-public-providers.md">Configuration du chiffrement multimédia pour les fournisseurs publics dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="b41e5-172"><a href="lync-server-2013-configure-media-encryption-for-public-providers.md">Configure media encryption for public providers in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b41e5-173">Vérifier la configuration de votre serveur de périphérie</span><span class="sxs-lookup"><span data-stu-id="b41e5-173">Verify your Edge Server configuration</span></span></p></td>
<td><p><span data-ttu-id="b41e5-174">Vérifier la connectivité du serveur et la réplication des données de configuration de serveurs internes</span><span class="sxs-lookup"><span data-stu-id="b41e5-174">Verify server connectivity and replication of configuration data from internal servers</span></span></p></td>
<td><p><span data-ttu-id="b41e5-175">Pour la vérification de la réplication, du groupe RTCUniversalServerAdmins ou du compte d’utilisateur qui est attribué à CSAdministrator roleFor vérification de la connectivité utilisateur, un utilisateur pour chaque type d’utilisateur fédéré</span><span class="sxs-lookup"><span data-stu-id="b41e5-175">For verification of replication, RTCUniversalServerAdmins group or user account that is assigned to the CSAdministrator roleFor verification of user connectivity, a user for each type of Federated user</span></span></p></td>
<td><p><span data-ttu-id="b41e5-176"><a href="lync-server-2013-verifying-your-edge-deployment.md">Vérification de votre déploiement Edge dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="b41e5-176"><a href="lync-server-2013-verifying-your-edge-deployment.md">Verifying your edge deployment in Lync Server 2013</a></span></span></p>
<p><span data-ttu-id="b41e5-177"><a href="lync-server-2013-example-xmpp-configuration-–-xmpp-federation-with-google-talk.md">Exemple de configuration XMPP dans Lync Server 2013 – Fédération XMPP avec Google Talk</a></span><span class="sxs-lookup"><span data-stu-id="b41e5-177"><a href="lync-server-2013-example-xmpp-configuration-–-xmpp-federation-with-google-talk.md">Example XMPP configuration in Lync Server 2013 – XMPP federation with Google Talk</a></span></span></p></td>
</tr><span data-ttu-id="b41e5-178">
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b41e5-178">
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

