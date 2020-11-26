---
title: 'Lync Server 2013 : planification de l’authentification à deux facteurs'
description: 'Lync Server 2013 : planification de l’authentification à deux facteurs.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for two-factor authentication
ms:assetid: 16f08710-8961-4659-acbf-ebb95a198fb4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn308562(v=OCS.15)
ms:contentKeyID: 54973683
ms.date: 04/06/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6a3a2cd5508f6ce9a8a389b0059a09747b9f9a09
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442872"
---
# <a name="planning-for-two-factor-authentication-in-lync-server-2013"></a><span data-ttu-id="56f94-103">Planification de l’authentification à deux facteurs dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="56f94-103">Planning for two-factor authentication in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="56f94-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="56f94-104">

<span> </span></span></span>

<span data-ttu-id="56f94-105">_**Dernière modification de la rubrique :** 2015-04-06_</span><span class="sxs-lookup"><span data-stu-id="56f94-105">_**Topic Last Modified:** 2015-04-06_</span></span>

<span data-ttu-id="56f94-106">La liste suivante répertorie les éléments à prendre en compte lors de la configuration d’un environnement Microsoft Lync Server 2013 pour prendre en charge l’authentification à deux facteurs.</span><span class="sxs-lookup"><span data-stu-id="56f94-106">The following is a list of deployment considerations when configuring a Microsoft Lync Server 2013 environment to support two-factor authentication.</span></span>

<div>

## <a name="client-support"></a><span data-ttu-id="56f94-107">Prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="56f94-107">Client Support</span></span>

<span data-ttu-id="56f94-108">Les mises à jour cumulatives de Lync 2013 pour Lync Server 2013 : le client de bureau 2013 de juillet et tous les clients mobiles prennent actuellement en charge l’authentification à deux facteurs.</span><span class="sxs-lookup"><span data-stu-id="56f94-108">The Lync 2013 Cumulative Updates for Lync Server 2013: July 2013 desktop client and all mobile clients currently support two-factor authentication.</span></span>

</div>

<div>

## <a name="topology-requirements"></a><span data-ttu-id="56f94-109">Conditions requises pour la topologie</span><span class="sxs-lookup"><span data-stu-id="56f94-109">Topology Requirements</span></span>

<span data-ttu-id="56f94-110">Les clients sont fortement invités à déployer l’authentification à deux facteurs à l’aide de la 2013 dédiée de Lync Server avec des mises à jour cumulatives pour Lync Server 2013:2013 Edge, Director et groupes d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="56f94-110">Customers are strongly encouraged to deploy two-factor authentication using dedicated Lync Server 2013 with Cumulative Updates for Lync Server 2013: July 2013 Edge, Director, and User Pools.</span></span> <span data-ttu-id="56f94-111">Pour activer l’authentification passive pour les utilisateurs de Lync, les autres méthodes d’authentification doivent être désactivées pour les autres rôles et services, notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="56f94-111">To enable passive authentication for Lync users, other authentication methods must be disabled for other roles and services, including the following:</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="56f94-112">Type de configuration</span><span class="sxs-lookup"><span data-stu-id="56f94-112">Configuration Type</span></span></th>
<th><span data-ttu-id="56f94-113">Type de service</span><span class="sxs-lookup"><span data-stu-id="56f94-113">Service Type</span></span></th>
<th><span data-ttu-id="56f94-114">Rôle serveur</span><span class="sxs-lookup"><span data-stu-id="56f94-114">Server Role</span></span></th>
<th><span data-ttu-id="56f94-115">Type d’authentification à désactiver</span><span class="sxs-lookup"><span data-stu-id="56f94-115">Authentication Type to Disable</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="56f94-116">Service web</span><span class="sxs-lookup"><span data-stu-id="56f94-116">Web Service</span></span></p></td>
<td><p><span data-ttu-id="56f94-117">WebServer</span><span class="sxs-lookup"><span data-stu-id="56f94-117">WebServer</span></span></p></td>
<td><p><span data-ttu-id="56f94-118">Directeur</span><span class="sxs-lookup"><span data-stu-id="56f94-118">Director</span></span></p></td>
<td><p><span data-ttu-id="56f94-119">Kerberos, NTLM et par certificat</span><span class="sxs-lookup"><span data-stu-id="56f94-119">Kerberos, NTLM, and Certificate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56f94-120">Service web</span><span class="sxs-lookup"><span data-stu-id="56f94-120">Web Service</span></span></p></td>
<td><p><span data-ttu-id="56f94-121">WebServer</span><span class="sxs-lookup"><span data-stu-id="56f94-121">WebServer</span></span></p></td>
<td><p><span data-ttu-id="56f94-122">Serveur frontal</span><span class="sxs-lookup"><span data-stu-id="56f94-122">Front End</span></span></p></td>
<td><p><span data-ttu-id="56f94-123">Kerberos, NTLM et par certificat</span><span class="sxs-lookup"><span data-stu-id="56f94-123">Kerberos, NTLM, and Certificate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56f94-124">Proxy</span><span class="sxs-lookup"><span data-stu-id="56f94-124">Proxy</span></span></p></td>
<td><p><span data-ttu-id="56f94-125">EdgeServer</span><span class="sxs-lookup"><span data-stu-id="56f94-125">EdgeServer</span></span></p></td>
<td><p><span data-ttu-id="56f94-126">Edge</span><span class="sxs-lookup"><span data-stu-id="56f94-126">Edge</span></span></p></td>
<td><p><span data-ttu-id="56f94-127">Kerberos et NTLM</span><span class="sxs-lookup"><span data-stu-id="56f94-127">Kerberos and NTLM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56f94-128">Proxy</span><span class="sxs-lookup"><span data-stu-id="56f94-128">Proxy</span></span></p></td>
<td><p><span data-ttu-id="56f94-129">Serveur d’inscriptions avancé</span><span class="sxs-lookup"><span data-stu-id="56f94-129">Registrar</span></span></p></td>
<td><p><span data-ttu-id="56f94-130">Serveur frontal</span><span class="sxs-lookup"><span data-stu-id="56f94-130">Front End</span></span></p></td>
<td><p><span data-ttu-id="56f94-131">Kerberos et NTLM</span><span class="sxs-lookup"><span data-stu-id="56f94-131">Kerberos and NTLM</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="56f94-132">Si ces types d’authentifications ne sont pas désactivés au niveau du service, toutes les autres versions du client Lync ne seront pas en mesure de se connecter une fois que l’authentification à deux facteurs est activée dans le cadre de votre déploiement.</span><span class="sxs-lookup"><span data-stu-id="56f94-132">Unless these authentication types are disabled at the service level, all other versions of the Lync client will be unable to sign in successfully once two-factor authentication is enabled within in your deployment.</span></span>

</div>

<div>

## <a name="lync-service-discovery"></a><span data-ttu-id="56f94-133">Découverte de service Lync</span><span class="sxs-lookup"><span data-stu-id="56f94-133">Lync Service Discovery</span></span>

<span data-ttu-id="56f94-134">Les enregistrements DNS utilisés par les clients internes et/ou externes pour détecter les services Lync doivent être configurés pour une résolution sur un serveur Lync qui n’est pas activé pour l’authentification à deux facteurs.</span><span class="sxs-lookup"><span data-stu-id="56f94-134">DNS records used by internal and/or external clients to discover Lync services should be configured to resolve to a Lync server that is not enabled for two-factor authentication.</span></span> <span data-ttu-id="56f94-135">Dans cette configuration, les utilisateurs de pools Lync qui ne sont pas activés pour l’authentification à deux facteurs ne seront pas obligés d’entrer un code confidentiel pour s’authentifier, alors que les utilisateurs de pools Lync qui sont activés pour l’authentification à deux facteurs seront obligés d’entrer leur code confidentiel pour s’authentifier.</span><span class="sxs-lookup"><span data-stu-id="56f94-135">With this configuration, users from Lync Pools that are not enabled for two-factor authentication will not be required to enter a PIN to authenticate, while users from Lync Pools that are enabled for two-factor authentication will be required to enter their PIN to authenticate.</span></span>

</div>

<div>

## <a name="exchange-authentication"></a><span data-ttu-id="56f94-136">Authentification Exchange</span><span class="sxs-lookup"><span data-stu-id="56f94-136">Exchange Authentication</span></span>

<span data-ttu-id="56f94-137">Les clients qui ont déployé l’authentification à deux facteurs pour Microsoft Exchange peuvent constater que certaines fonctionnalités du client Lync ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="56f94-137">Customers who have deployed two-factor authentication for Microsoft Exchange may find that certain features in the Lync client are unavailable.</span></span> <span data-ttu-id="56f94-138">Cette fonctionnalité est actuellement à l’étude, car le client Lync ne prend pas en charge l’authentification à deux facteurs pour les fonctionnalités qui dépendent de l’intégration Exchange.</span><span class="sxs-lookup"><span data-stu-id="56f94-138">This is currently by design, as the Lync client does not support two-factor authentication for features that are dependent on Exchange integration.</span></span>

</div>

<div>

## <a name="lync-contacts"></a><span data-ttu-id="56f94-139">Contacts Lync</span><span class="sxs-lookup"><span data-stu-id="56f94-139">Lync Contacts</span></span>

<span data-ttu-id="56f94-140">Les utilisateurs de Lync qui sont configurés pour utiliser la fonctionnalité de magasin de contacts unifiée pourront constater que leurs contacts ne sont plus disponibles une fois que vous êtes connecté à l’aide de l’authentification à deux facteurs.</span><span class="sxs-lookup"><span data-stu-id="56f94-140">Lync users who are configured to leverage the Unified Contact Store feature will find that their contacts are no longer available after signing in with two-factor authentication.</span></span>

<span data-ttu-id="56f94-141">Pour activer l’authentification à deux facteurs, vous devez utiliser l’applet de passe **Invoke-CsUcsRollback** pour supprimer les contacts des utilisateurs existants du magasin de contacts unifié et les stocker dans Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="56f94-141">You should use the **Invoke-CsUcsRollback** cmdlet to remove existing user contacts from the Unified Contact Store and store them in Lync Server 2013 before enabling two-factor authentication.</span></span>

</div>

<div>

## <a name="skill-search"></a><span data-ttu-id="56f94-142">Recherche de compétences</span><span class="sxs-lookup"><span data-stu-id="56f94-142">Skill Search</span></span>

<span data-ttu-id="56f94-143">Les clients qui ont configuré la fonction de recherche de compétences dans leur environnement Lync constateront que cette fonctionnalité ne fonctionne pas lorsque Lync est activé pour l’authentification à deux facteurs.</span><span class="sxs-lookup"><span data-stu-id="56f94-143">Customers who have configured the Skill Search feature in their Lync environment will find that this feature does not work when Lync is enabled for two-factor authentication.</span></span> <span data-ttu-id="56f94-144">Ce comportement est normal, car Microsoft SharePoint ne prend pas en charge l’authentification à deux facteurs pour le moment.</span><span class="sxs-lookup"><span data-stu-id="56f94-144">This is by design, as Microsoft SharePoint does not currently support two-factor authentication.</span></span>

</div>

<div>

## <a name="lync-credentials"></a><span data-ttu-id="56f94-145">Informations d’identification Lync</span><span class="sxs-lookup"><span data-stu-id="56f94-145">Lync Credentials</span></span>

<span data-ttu-id="56f94-146">Il existe un certain nombre de considérations de déploiement impliquant des informations d’identification Lync enregistrées qui peuvent avoir un impact sur les utilisateurs qui sont configurés pour utiliser l’authentification à deux facteurs.</span><span class="sxs-lookup"><span data-stu-id="56f94-146">There are a number of deployment considerations involving saved Lync credentials which may impact users who are configured to use two-factor authentication.</span></span>

<div>

## <a name="deleting-saved-credentials"></a><span data-ttu-id="56f94-147">Suppression des informations d’identification enregistrées</span><span class="sxs-lookup"><span data-stu-id="56f94-147">Deleting Saved Credentials</span></span>

<span data-ttu-id="56f94-148">Les utilisateurs du client de bureau doivent utiliser l’option **Supprimer mes informations de connexion** dans le client Lync et supprimer leur dossier de profil SIP de% LocalAppData% \\ Microsoft \\ Office \\ 15,0 \\ Lync avant d’essayer de vous connecter pour la première fois à l’aide de l’authentification à deux facteurs.</span><span class="sxs-lookup"><span data-stu-id="56f94-148">Desktop client users should use the **Delete my sign-in info** option in the Lync client and delete their SIP profile folder from %localappdata%\\Microsoft\\Office\\15.0\\Lync before attempting to sign for the first time using two-factor authentication.</span></span>

</div>

<div>

## <a name="disablentcredentials"></a><span data-ttu-id="56f94-149">DisableNTCredentials</span><span class="sxs-lookup"><span data-stu-id="56f94-149">DisableNTCredentials</span></span>

<span data-ttu-id="56f94-150">Lorsque la méthode d’authentification Kerberos ou NTLM est utilisée, les informations d’identification Windows de l’utilisateur sont utilisées automatiquement pour l’authentification.</span><span class="sxs-lookup"><span data-stu-id="56f94-150">With the Kerberos or NTLM authentication method, the user’s Windows credentials are used automatically for authentication.</span></span> <span data-ttu-id="56f94-151">Dans le cas d’un déploiement standard de Lync Server 2013 sur lequel Kerberos et/ou NTLM est activé pour l’authentification, l’utilisateur ne doit pas entrer ses informations d’identification chaque fois qu’il se connecte.</span><span class="sxs-lookup"><span data-stu-id="56f94-151">In a typical Lync Server 2013 deployment where Kerberos and/or NTLM is enabled for authentication, users should not have to enter their credentials every time that they sign in.</span></span>

<span data-ttu-id="56f94-152">Si les utilisateurs sont invités à entrer leurs informations d’identification avant leur code confidentiel, la clé de Registre **DisableNTCredentials** est peut être configurée involontairement sur les ordinateurs clients, éventuellement par le biais de la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="56f94-152">If users are unintentionally prompted for credentials before they are prompted to enter their PIN, the **DisableNTCredentials** registry key may be unintentionally configured on client computers, possibly through Group Policy.</span></span>

<span data-ttu-id="56f94-153">Pour empêcher l’invite supplémentaire pour les informations d’identification, créez l’entrée de Registre suivante sur la station de travail locale ou utilisez le modèle d’administration Lync pour appliquer à tous les utilisateurs pour un pool donné à l’aide d’une stratégie de groupe :</span><span class="sxs-lookup"><span data-stu-id="56f94-153">To prevent the additional prompt for credentials, create the following registry entry on the local workstation or use the Lync administrative template to apply to all users for a given pool using Group Policy:</span></span>

<span data-ttu-id="56f94-154">HKEY \_ \_ \\ stratégies logicielles \\ locales \\ Microsoft \\ Office \\ 15,0 \\ Lync</span><span class="sxs-lookup"><span data-stu-id="56f94-154">HKEY\_LOCAL\_MACHINE\\Software\\Policies\\Microsoft\\Office\\15.0\\Lync</span></span>

<span data-ttu-id="56f94-155">REG \_ DWORD : DisableNTCredentials</span><span class="sxs-lookup"><span data-stu-id="56f94-155">REG\_DWORD: DisableNTCredentials</span></span>

<span data-ttu-id="56f94-156">Valeur : 0x0</span><span class="sxs-lookup"><span data-stu-id="56f94-156">Value: 0x0</span></span>

</div>

<div>

## <a name="savepassword"></a><span data-ttu-id="56f94-157">SavePassword</span><span class="sxs-lookup"><span data-stu-id="56f94-157">SavePassword</span></span>

<span data-ttu-id="56f94-158">Lorsqu’un utilisateur se connecte à Lync pour la première fois, l’utilisateur est invité à enregistrer son mot de passe.</span><span class="sxs-lookup"><span data-stu-id="56f94-158">When a user signs in to Lync for the first time, the user is prompted to save his or her password.</span></span> <span data-ttu-id="56f94-159">Lorsqu’elle est sélectionnée, cette option permet le stockage du certificat client de l’utilisateur dans le magasin de certificats personnel et des informations d’identification Windows de l’utilisateur dans le Gestionnaire d’informations d’identification de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="56f94-159">If selected, this option allows the user’s client certificate to be stored in the personal certificate store and the user’s Windows credentials to be stored in the Credential Manager of the local computer.</span></span>

<span data-ttu-id="56f94-160">Le paramètre de Registre **SavePassword** doit être désactivé lorsque Lync est configuré pour prendre en charge l’authentification à deux facteurs.</span><span class="sxs-lookup"><span data-stu-id="56f94-160">The **SavePassword** registry setting should be disabled when Lync is configured to support two-factor authentication.</span></span> <span data-ttu-id="56f94-161">Pour empêcher les utilisateurs d’enregistrer leur mot de passe, modifiez l’entrée de Registre suivante sur la station de travail locale ou utilisez le modèle d’administration Lync pour appliquer à tous les utilisateurs pour un pool donné à l’aide d’une stratégie de groupe :</span><span class="sxs-lookup"><span data-stu-id="56f94-161">To prevent users from saving their passwords, change the following registry entry on the local workstation or use the Lync administrative template to apply to all users for a given pool using Group Policy:</span></span>

<span data-ttu-id="56f94-162">HKEY \_ \_ logiciel utilisateur \\ actuel \\ Microsoft \\ Office \\ 15,0 \\ Lync</span><span class="sxs-lookup"><span data-stu-id="56f94-162">HKEY\_CURRENT\_USER\\Software\\Microsoft\\Office\\15.0\\Lync</span></span>

<span data-ttu-id="56f94-163">REG \_ DWORD : SavePassword</span><span class="sxs-lookup"><span data-stu-id="56f94-163">REG\_DWORD: SavePassword</span></span>

<span data-ttu-id="56f94-164">Valeur : 0x0</span><span class="sxs-lookup"><span data-stu-id="56f94-164">Value: 0x0</span></span>

</div>

</div>

<div>

## <a name="ad-fs-20-token-replay"></a><span data-ttu-id="56f94-165">Relecture des jetons d’AD FS 2.0</span><span class="sxs-lookup"><span data-stu-id="56f94-165">AD FS 2.0 Token Replay</span></span>

<span data-ttu-id="56f94-p108">La fonctionnalité d’AD FS 2.0 de détection de relecture des jetons détecte et rejette les demandes de jeton multiples effectuées à l’aide d’un même jeton. Lorsqu’elle est activée, elle protège l’intégrité des demandes d’authentification dans le profil passif WS-Federation et le profil SAML WebSSO en vérifiant que le même jeton n’est pas utilisé plusieurs fois.</span><span class="sxs-lookup"><span data-stu-id="56f94-p108">AD FS 2.0 provides a feature referred to as token replay detection, by which multiple token requests using the same token can be detected and then discarded. When this feature is enabled, token replay detection protects the integrity of authentication requests in both the WS-Federation passive profile and the SAML WebSSO profile by making sure that the same token is never used more than once.</span></span>

<span data-ttu-id="56f94-168">Cette fonctionnalité doit être activée dans les cas dans lesquels la sécurité constitue un aspect essentiel, par exemple, dans le cadre de l’utilisation des kiosques.</span><span class="sxs-lookup"><span data-stu-id="56f94-168">This feature should be enabled in situations where security is a very high concern such as when using kiosks.</span></span> <span data-ttu-id="56f94-169">Pour plus d’informations sur la détection de relecture de jeton, voir recommandations en matière de planification et de déploiement sécurisés d’AD FS 2,0 à l’adresse [https://go.microsoft.com/fwlink/p/?LinkId=309215](https://go.microsoft.com/fwlink/p/?linkid=309215) .</span><span class="sxs-lookup"><span data-stu-id="56f94-169">For more information about token replay detection, see Best Practices for Secure Planning and Deployment of AD FS 2.0 at [https://go.microsoft.com/fwlink/p/?LinkId=309215](https://go.microsoft.com/fwlink/p/?linkid=309215).</span></span>

</div>

<div>

## <a name="external-user-access"></a><span data-ttu-id="56f94-170">Accès des utilisateurs externes</span><span class="sxs-lookup"><span data-stu-id="56f94-170">External User Access</span></span>

<span data-ttu-id="56f94-171">La configuration d’un proxy AD FS ou d’un proxy inverse pour prendre en charge l’authentification à deux facteurs de Lync à partir de réseaux externes n’est pas décrite dans les rubriques suivantes.</span><span class="sxs-lookup"><span data-stu-id="56f94-171">Configuring an AD FS Proxy or Reverse Proxy to support Lync two-factor authentication from external networks is not covered in these topics.</span></span>

<span data-ttu-id="56f94-172"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="56f94-172"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

