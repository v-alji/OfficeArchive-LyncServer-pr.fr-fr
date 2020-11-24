---
title: 'Lync Server 2013 : Processus de déploiement pour la mobilité'
description: 'Lync Server 2013 : processus de déploiement pour la mobilité.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment process for mobility
ms:assetid: 5a1cebda-c14b-4ff4-9c36-f7caa868160f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690023(v=OCS.15)
ms:contentKeyID: 48184220
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b49d69af899f6d9f2ac1db5040d017a9d62ce9eb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394901"
---
# <a name="deployment-process-for-mobility-in-lync-server-2013"></a><span data-ttu-id="d9835-103">Processus de déploiement pour la mobilité dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d9835-103">Deployment process for mobility in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d9835-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d9835-104">

<span> </span></span></span>

<span data-ttu-id="d9835-105">_**Dernière modification de la rubrique :** 2013-02-19_</span><span class="sxs-lookup"><span data-stu-id="d9835-105">_**Topic Last Modified:** 2013-02-19_</span></span>

    Some information in this topic pertains to Cumulative Updates for Lync Server 2013: February 2013. It is noted accordingly.

<span data-ttu-id="d9835-106">Cette section décrit la procédure de déploiement de la fonctionnalité de mobilité de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d9835-106">This section describes the sequence of steps required to deploy the Lync Server 2013 mobility feature.</span></span>

### <a name="mobility-deployment-process"></a><span data-ttu-id="d9835-107">Processus de déploiement de mobilité</span><span class="sxs-lookup"><span data-stu-id="d9835-107">Mobility Deployment Process</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d9835-108">Phase</span><span class="sxs-lookup"><span data-stu-id="d9835-108">Phase</span></span></th>
<th><span data-ttu-id="d9835-109">Étapes</span><span class="sxs-lookup"><span data-stu-id="d9835-109">Steps</span></span></th>
<th><span data-ttu-id="d9835-110">Autorisations</span><span class="sxs-lookup"><span data-stu-id="d9835-110">Permissions</span></span></th>
<th><span data-ttu-id="d9835-111">Documentation de déploiement</span><span class="sxs-lookup"><span data-stu-id="d9835-111">Deployment documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d9835-112">Créer des enregistrements DNS (Domain Name System)</span><span class="sxs-lookup"><span data-stu-id="d9835-112">Create Domain Name System (DNS) records</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="d9835-113">Créer un enregistrement DNS CNAMe interne ou A (hôte, si IPv6, AAAA) pour résoudre l’URL du service de découverte automatique interne.</span><span class="sxs-lookup"><span data-stu-id="d9835-113">Create an internal DNS CNAME or A (host, if IPv6, AAAA) record to resolve the internal Autodiscover Service URL.</span></span></p></li>
<li><p><span data-ttu-id="d9835-114">Créer un enregistrement DNS canonique ou A (hôte, si IPv6, AAAA) pour résoudre l’URL du service de découverte automatique externe.</span><span class="sxs-lookup"><span data-stu-id="d9835-114">Create an external DNS CNAME or A (host, if IPv6, AAAA) record to resolve the external Autodiscover Service URL.</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="d9835-115">DomainAdmins</span><span class="sxs-lookup"><span data-stu-id="d9835-115">Domain Admins</span></span></p>
<p><span data-ttu-id="d9835-116">DnsAdmins</span><span class="sxs-lookup"><span data-stu-id="d9835-116">DnsAdmins</span></span></p></td>
<td><p><span data-ttu-id="d9835-117"><a href="lync-server-2013-creating-dns-records-for-the-autodiscover-service.md">Création d’enregistrements DNS pour le service de découverte automatique dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="d9835-117"><a href="lync-server-2013-creating-dns-records-for-the-autodiscover-service.md">Creating DNS records for the Autodiscover Service in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9835-118">Modifier les certificats</span><span class="sxs-lookup"><span data-stu-id="d9835-118">Modify certificates</span></span></p></td>
<td><p><span data-ttu-id="d9835-119">Ajoutez des entrées de nom de remplacement d’objet aux certificats suivants pour prendre en charge des connexions sécurisées pour les utilisateurs mobiles :</span><span class="sxs-lookup"><span data-stu-id="d9835-119">Add subject alternative name entries to the following certificates to support secure connections for mobile users:</span></span></p>
<ul>
<li><p><span data-ttu-id="d9835-120">Certificat de réalisateur</span><span class="sxs-lookup"><span data-stu-id="d9835-120">Director certificate</span></span></p></li>
<li><p><span data-ttu-id="d9835-121">Certificat de pool frontal</span><span class="sxs-lookup"><span data-stu-id="d9835-121">Front End pool certificate</span></span></p></li>
<li><p><span data-ttu-id="d9835-122">Certificat de proxy inverse</span><span class="sxs-lookup"><span data-stu-id="d9835-122">Reverse proxy certificate</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="d9835-123">Administrateur local</span><span class="sxs-lookup"><span data-stu-id="d9835-123">Local administrator</span></span></p></td>
<td><p><span data-ttu-id="d9835-124"><a href="lync-server-2013-modifying-certificates-for-mobility.md">Modification des certificats pour la mobilité dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="d9835-124"><a href="lync-server-2013-modifying-certificates-for-mobility.md">Modifying certificates for mobility in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9835-125">Configurer le proxy inverse</span><span class="sxs-lookup"><span data-stu-id="d9835-125">Configure the reverse proxy</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="d9835-126">Attribuez des certificats mis à jour avec des noms de substitution d’objet à l’écouteur SSL (Secure Sockets Layer).</span><span class="sxs-lookup"><span data-stu-id="d9835-126">Assign certificates updated with subject alternative names to the Secure Sockets Layer (SSL) Listener.</span></span></p></li>
<li><p><span data-ttu-id="d9835-127">Reconfigurez la règle de publication Web pour l’URL du service de découverte automatique externe.</span><span class="sxs-lookup"><span data-stu-id="d9835-127">Reconfigure the web publishing rule for the external Autodiscover Service URL.</span></span></p></li>
<li><p><span data-ttu-id="d9835-128">Assurez-vous qu’une règle de publication sur le Web existe pour l’URL des services Web Lync Server 2013 externes de votre pool frontal.</span><span class="sxs-lookup"><span data-stu-id="d9835-128">Be sure that a web publishing rule exists for the external Lync Server 2013 Web Services URL on your Front End pool.</span></span></p></li>
</ul>
<p><span data-ttu-id="d9835-129">Ou</span><span class="sxs-lookup"><span data-stu-id="d9835-129">Or</span></span></p>
<ul>
<li><p><span data-ttu-id="d9835-130">Si vous choisissez d’utiliser HTTP pour la demande de découverte automatique initiale et de ne pas mettre à jour les listes de noms alternatifs d’objet sur les certificats, configurez une nouvelle règle de publication Web ou reconfigurez une règle de publication existante pour le port 80 HTTP.</span><span class="sxs-lookup"><span data-stu-id="d9835-130">If you choose to use HTTP for the initial Autodiscover request and do not update subject alternative name lists on the certificates, configure a new web publishing rule or reconfigure an existing publishing rule for port 80 HTTP.</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="d9835-131">Administrateur local</span><span class="sxs-lookup"><span data-stu-id="d9835-131">Local administrator</span></span></p></td>
<td><p><span data-ttu-id="d9835-132"><a href="lync-server-2013-configuring-the-reverse-proxy-for-mobility.md">Configuration du proxy inverse pour la mobilité dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="d9835-132"><a href="lync-server-2013-configuring-the-reverse-proxy-for-mobility.md">Configuring the reverse proxy for mobility in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9835-133">Tester le déploiement de votre mobilité pour Lync 2010 mobile à l’aide du service de mobilité MCX</span><span class="sxs-lookup"><span data-stu-id="d9835-133">Test your mobility deployment for Lync 2010 Mobile using the Mcx Mobility Service</span></span></p></td>
<td><p><span data-ttu-id="d9835-134">Exécutez <strong>test-CsMcxP2PIM</strong> pour tester l’envoi d’un message instantané d’une personne à l’autre.</span><span class="sxs-lookup"><span data-stu-id="d9835-134">Run <strong>Test-CsMcxP2PIM</strong> to test sending an instant message from one person to another.</span></span></p>
<p><span data-ttu-id="d9835-135">Pour obtenir la liste complète des options, reportez-vous à la documentation cmdlet de Lync Server Management Shell pour <a href="https://docs.microsoft.com/powershell/module/skype/Test-CsMcxP2PIM">test-CsMcxP2PIM</a> .</span><span class="sxs-lookup"><span data-stu-id="d9835-135">See the Lync Server Management Shell cmdlet documentation for <a href="https://docs.microsoft.com/powershell/module/skype/Test-CsMcxP2PIM">Test-CsMcxP2PIM</a> for a complete list of options.</span></span></p></td>
<td><p><span data-ttu-id="d9835-136">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="d9835-136">CsAdministrator</span></span></p></td>
<td><p><span data-ttu-id="d9835-137"><a href="lync-server-2013-verifying-your-mobility-deployment.md">Vérification du déploiement de mobilité dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="d9835-137"><a href="lync-server-2013-verifying-your-mobility-deployment.md">Verifying your mobility deployment in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9835-138">Tester le déploiement de votre mobilité pour les clients mobiles Lync 2013 à l’aide des composants Web UCWA</span><span class="sxs-lookup"><span data-stu-id="d9835-138">Test your mobility deployment for Lync 2013 Mobile clients using the UCWA Web components</span></span></p></td>
<td><p><span data-ttu-id="d9835-139">Utilisez l’applet de <strong>contrôle test-CsUcwaConference</strong> pour tester et vérifier que les utilisateurs de tests prédéfinis ou une paire d’utilisateurs réels peuvent utiliser UCWA pour créer une conférence et y participer.</span><span class="sxs-lookup"><span data-stu-id="d9835-139">Use the <strong>Test-CsUcwaConference</strong> cmdlet to test and verify that pre-defined test users or a pair of actual users can use UCWA to create and participate in a conference.</span></span></p>
<p><span data-ttu-id="d9835-140">Pour obtenir la liste complète des options, reportez-vous à la documentation cmdlet de Lync Server Management Shell pour <a href="https://docs.microsoft.com/powershell/module/skype/Test-CsUcwaConference">test-CsUcwaConference</a> .</span><span class="sxs-lookup"><span data-stu-id="d9835-140">See the Lync Server Management Shell cmdlet documentation for <a href="https://docs.microsoft.com/powershell/module/skype/Test-CsUcwaConference">Test-CsUcwaConference</a> for a complete list of options.</span></span></p></td>
<td><p><span data-ttu-id="d9835-141">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="d9835-141">CsAdministrator</span></span></p></td>
<td><p><span data-ttu-id="d9835-142"><a href="lync-server-2013-verifying-your-mobility-deployment.md">Vérification du déploiement de mobilité dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="d9835-142"><a href="lync-server-2013-verifying-your-mobility-deployment.md">Verifying your mobility deployment in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d9835-143">Configurer les notifications push</span><span class="sxs-lookup"><span data-stu-id="d9835-143">Configure for push notifications</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="d9835-144">Pour les serveurs Edge Lync Server 2013, ajoutez un fournisseur d’hébergement Lync Server Online et configurez la Fédération du fournisseur d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="d9835-144">For Lync Server 2013 Edge Servers, add a Lync Server online hosting provider and configure hosting provider federation.</span></span></p></li>
<li><p><span data-ttu-id="d9835-145">Pour les serveurs Edge Lync Server 2010, ajoutez un fournisseur d’hébergement Lync Server Online et configurez la Fédération du fournisseur d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="d9835-145">For Lync Server 2010  Edge Servers, add a Lync Server online hosting provider and configure hosting provider federation.</span></span></p></li>
<li><p><span data-ttu-id="d9835-146">Pour les serveurs Edge Office Communications Server 2007 R2, ajoutez un partenaire fédéré.</span><span class="sxs-lookup"><span data-stu-id="d9835-146">For Office Communications Server 2007 R2 Edge Servers, add a federated partner.</span></span></p></li>
<li><p><span data-ttu-id="d9835-147">Si vous voulez prendre en charge les notifications de transmission via un réseau Wi-Fi, configurez une règle de pare-feu sortante pour le port TCP 5223.</span><span class="sxs-lookup"><span data-stu-id="d9835-147">If you want to support push notifications over a Wi-Fi network, configure a firewall rule outbound for TCP port 5223.</span></span></p></li>
<li><p><span data-ttu-id="d9835-148">Utilisez l’applet de cmdlet <strong>Set-CsPushNotificationConfiguration</strong> pour activer les notifications de transmission pour les services de notifications de transmission d’Apple (APNs) et Microsoft émission notification service (MPNS).</span><span class="sxs-lookup"><span data-stu-id="d9835-148">Use the <strong>Set-CsPushNotificationConfiguration</strong> cmdlet to enable push notifications to the Apple Push Notification Service (APNS) and Microsoft Push Notification Service (MPNS).</span></span> <span data-ttu-id="d9835-149">Cette fonctionnalité est désactivée par défaut.</span><span class="sxs-lookup"><span data-stu-id="d9835-149">This feature is disabled by default.</span></span></p></li>
<li><p><span data-ttu-id="d9835-150">Utilisez l’applet de <strong>contrôle test-CsFederatedPartner</strong> pour tester la configuration de la Fédération et l’applet de <strong>contrôle CsMCXPushNotification de test</strong> pour tester les notifications de transmission.</span><span class="sxs-lookup"><span data-stu-id="d9835-150">Use the <strong>Test-CsFederatedPartner</strong> cmdlet to test the federation configuration and the <strong>Test-CsMCXPushNotification</strong> cmdlet to test push notifications.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="d9835-151">Les notifications de transmission sont utilisées pour les clients mobiles Lync 2010 sur les appareils Apple et Windows Phone</span><span class="sxs-lookup"><span data-stu-id="d9835-151">Push notifications are used for Lync 2010 Mobile clients on Apple devices and Windows Phone</span></span><BR><span data-ttu-id="d9835-152">La notification de transmission est requise pour les clients mobiles Lync 2013 sur Windows Phone uniquement</span><span class="sxs-lookup"><span data-stu-id="d9835-152">Push notification is required for Lync 2013 Mobile clients on Windows Phone only</span></span>


</div></li>
</ul></td>
<td><p><span data-ttu-id="d9835-153">RtcUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="d9835-153">RtcUniversalServerAdmins</span></span></p></td>
<td><p><span data-ttu-id="d9835-154"><a href="lync-server-2013-configuring-for-push-notifications.md">Configuration des notifications push dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="d9835-154"><a href="lync-server-2013-configuring-for-push-notifications.md">Configuring for push notifications in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d9835-155">Configurer une stratégie de mobilité</span><span class="sxs-lookup"><span data-stu-id="d9835-155">Configure mobility policy</span></span></p></td>
<td><p><span data-ttu-id="d9835-156">Utilisez l’applet de cmdlet <strong>Set-CsMobilityPolicy</strong> pour autoriser ou rejeter les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="d9835-156">Use the <strong>Set-CsMobilityPolicy</strong> cmdlet to allow or disallow:</span></span></p>
<ul>
<li><p><span data-ttu-id="d9835-157">Appel via le bureau</span><span class="sxs-lookup"><span data-stu-id="d9835-157">Call via Work</span></span></p></li>
<li><p><span data-ttu-id="d9835-158">Activer les appels audio et vidéo IP</span><span class="sxs-lookup"><span data-stu-id="d9835-158">Enable IP Audio and IP Video</span></span></p></li>
<li><p><span data-ttu-id="d9835-159">Wi-Fi requis pour les appels audio et/ou vidéo IP</span><span class="sxs-lookup"><span data-stu-id="d9835-159">Require WiFi for IP Audio and/or IP Video</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="d9835-160">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="d9835-160">CsAdministrator</span></span></p></td>
<td><p><span data-ttu-id="d9835-161"><a href="lync-server-2013-configuring-mobility-policy.md">Configuration de la stratégie de mobilité dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="d9835-161"><a href="lync-server-2013-configuring-mobility-policy.md">Configuring mobility policy in Lync Server 2013</a></span></span></p></td>
</tr><span data-ttu-id="d9835-162">
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d9835-162">
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span></span></div>

