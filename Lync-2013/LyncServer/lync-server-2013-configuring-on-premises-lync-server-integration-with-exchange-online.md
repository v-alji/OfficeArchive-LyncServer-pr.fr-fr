---
title: Configuration de l’intégration Lync Server locale dans Exchange Online
description: Configuration de l’intégration Lync Server locale dans Exchange Online.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring on-premises Lync Server integration with Exchange Online
ms:assetid: 95a20117-2064-43c4-94fe-cac892cadb6f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh533880(v=OCS.15)
ms:contentKeyID: 48184900
ms.date: 03/30/2018
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 59c612bcdcdf4803bd6f9f2b38f1f9bb7dbad016
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432834"
---
# <a name="configuring-on-premises-lync-server-2013-integration-with-exchange-online"></a><span data-ttu-id="6f926-103">Configuration de l’intégration locale de Lync Server 2013 à Exchange Online</span><span class="sxs-lookup"><span data-stu-id="6f926-103">Configuring on-premises Lync Server 2013 integration with Exchange Online</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6f926-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6f926-104">

<span> </span></span></span>

<span data-ttu-id="6f926-105">_**Dernière modification de la rubrique :** 2018-03-30_</span><span class="sxs-lookup"><span data-stu-id="6f926-105">_**Topic Last Modified:** 2018-03-30_</span></span>

<span data-ttu-id="6f926-106">Les clients utilisant un déploiement local de Lync Server 2013 peuvent configurer l’interopérabilité avec Microsoft Outlook Web App dans Microsoft Exchange Online dans un mode de déploiement hybride.</span><span class="sxs-lookup"><span data-stu-id="6f926-106">Customers who are using on-premises Lync Server 2013 deployments can configure interoperability with Microsoft Outlook Web App in Microsoft Exchange Online in a hybrid deployment mode.</span></span> <span data-ttu-id="6f926-107">Les fonctionnalités d’interopérabilité comprennent l’ouverture de session unique, l’intégration de la messagerie instantanée et de la présence dans l’interface d’Outlook Web App.</span><span class="sxs-lookup"><span data-stu-id="6f926-107">Interoperability features include single sign on and instant messaging (IM) and presence integration with the Outlook Web App interface.</span></span> <span data-ttu-id="6f926-108">Pour activer cette intégration, vous devez configurer le serveur de périphérie dans votre déploiement Lync Server local en effectuant les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="6f926-108">To enable this integration, you must configure the Edge Server in your on-premises Lync Server deployment by completing the following tasks:</span></span>

  - <span data-ttu-id="6f926-109">configurer un espace d’adressage SIP partagé ;</span><span class="sxs-lookup"><span data-stu-id="6f926-109">Configure a shared SIP address space</span></span>

  - <span data-ttu-id="6f926-110">Configurer un fournisseur d’hébergement sur le serveur Edge</span><span class="sxs-lookup"><span data-stu-id="6f926-110">Configure a hosting provider on the Edge Server</span></span>

  - <span data-ttu-id="6f926-111">Vérification de la réplication du magasin central de gestion mis à jour</span><span class="sxs-lookup"><span data-stu-id="6f926-111">Verify replication of the updated Central Management store</span></span>

<span data-ttu-id="6f926-112">Si Lync Server 2013 est intégré à Exchange Online, un utilisateur qui tente de se connecter à la messagerie instantanée à partir d’OWA est considéré comme un utilisateur distant ou externe.</span><span class="sxs-lookup"><span data-stu-id="6f926-112">If Lync Server 2013 is integrated with Exchange Online, a user who is trying to sign in to IM from OWA is considered a remote or external user.</span></span> <span data-ttu-id="6f926-113">Dans ce scénario, l’option suivante doit être attribuée à l’utilisateur pour l’utilisation de la stratégie d’accès externe :</span><span class="sxs-lookup"><span data-stu-id="6f926-113">In this scenario, this user must have an external access policy assigned that has the following option selected:</span></span>

<span data-ttu-id="6f926-114">**Activer les communications avec les utilisateurs distants**</span><span class="sxs-lookup"><span data-stu-id="6f926-114">**Enable communications with remote users**</span></span>

<span data-ttu-id="6f926-115">Activez cette option si vous souhaitez que les utilisateurs de votre organisation qui se trouvent en dehors de votre pare-feu (par exemple, des télétravailleurs et des utilisateurs qui voyagent) puissent se connecter à Lync Server via Internet.</span><span class="sxs-lookup"><span data-stu-id="6f926-115">Enable this option if you want users in your organization who are outside your firewall, such as telecommuters and users who are traveling, to be able to connect to Lync Server over the Internet.</span></span>

<span data-ttu-id="6f926-116">Pour plus d’informations, consultez [gérer les stratégies d’accès externe dans Lync Server 2013](lync-server-2013-manage-external-access-policy-for-your-organization.md).</span><span class="sxs-lookup"><span data-stu-id="6f926-116">For more information, see [Manage external access policy in Lync Server 2013](lync-server-2013-manage-external-access-policy-for-your-organization.md).</span></span>

<div>

## <a name="configure-a-shared-sip-address-space"></a><span data-ttu-id="6f926-117">Configurer un espace d’adressage SIP partagé</span><span class="sxs-lookup"><span data-stu-id="6f926-117">Configure a Shared SIP Address Space</span></span>

<span data-ttu-id="6f926-118">Pour intégrer Lync Server 2013 local et Exchange Online, vous devez configurer un espace d’adressage SIP partagé.</span><span class="sxs-lookup"><span data-stu-id="6f926-118">To integrate on-premises Lync Server 2013 with Exchange Online, you must configure a shared SIP address space.</span></span> <span data-ttu-id="6f926-119">Le même espace d’adresse de domaine SIP est pris en charge par Lync Server et le service Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="6f926-119">The same SIP domain address space is supported by both Lync Server and the Exchange Online service.</span></span>

<span data-ttu-id="6f926-120">À l’aide de Lync Server Management Shell, configurez le serveur Edge pour la Fédération en exécutant l’applet de commande **Set-CSAccessEdgeConfiguration** en utilisant les paramètres qui s’affichent dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="6f926-120">Using the Lync Server Management Shell, configure the Edge Server for federation by running the **Set-CSAccessEdgeConfiguration** cmdlet, using the parameters that are displayed in the following example:</span></span>

    Set-CsAccessEdgeConfiguration -AllowFederatedUsers $True

  - <span data-ttu-id="6f926-121">**AllowFederatedUsers** indique si des utilisateurs internes sont autorisés à communiquer avec des utilisateurs de domaines fédérés.</span><span class="sxs-lookup"><span data-stu-id="6f926-121">**AllowFederatedUsers** specifies whether internal users are allowed to communicate with users from federated domains.</span></span> <span data-ttu-id="6f926-122">Cette propriété détermine également si les utilisateurs internes peuvent communiquer avec des utilisateurs dans un scénario d’espace d’adressage SIP partagé avec Lync Server et Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="6f926-122">This property also determines whether internal users can communicate with users in a shared SIP address space scenario with Lync Server and Exchange Online.</span></span>

<span data-ttu-id="6f926-123">Pour plus d’informations sur l’utilisation de Lync Server Management Shell, voir [Lync server 2013 Management Shell](lync-server-2013-lync-server-management-shell.md).</span><span class="sxs-lookup"><span data-stu-id="6f926-123">For details about how to use the Lync Server Management Shell, see [Lync Server 2013 Management Shell](lync-server-2013-lync-server-management-shell.md).</span></span>

</div>

<div>

## <a name="configure-a-hosting-provider-on-the-edge-server"></a><span data-ttu-id="6f926-124">Configurer un fournisseur d’hébergement sur le serveur Edge.</span><span class="sxs-lookup"><span data-stu-id="6f926-124">Configure a Hosting Provider on the Edge Server</span></span>

<span data-ttu-id="6f926-125">Utilisez Lync Server Management Shell pour configurer un fournisseur d’hébergement sur le serveur Edge.</span><span class="sxs-lookup"><span data-stu-id="6f926-125">Use the Lync Server Management Shell to configure a hosting provider on the Edge Server.</span></span> <span data-ttu-id="6f926-126">Pour cela, exécutez l’applet **de commande New-CsHostingProvider** en utilisant les paramètres dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="6f926-126">To do this, run the **New-CsHostingProvider** cmdlet, using the parameters in the following example:</span></span>

    New-CsHostingProvider -Identity "Exchange Online" -Enabled $True -EnabledSharedAddressSpace $True -HostsOCSUsers $False -ProxyFqdn "exap.um.outlook.com" -IsLocal $False -VerificationLevel UseSourceVerification

<div>


> [!NOTE]
> <span data-ttu-id="6f926-127">Si vous utilisez Office 365 activé par 21Vianet en Chine, remplacez dans cet exemple la valeur du paramètre <STRONG>ProxyFqdn</STRONG> (« exap.um.outlook.com ») par le FQDN du service activé par 21Vianet: « exap.um.partner.outlook.cn ».</span><span class="sxs-lookup"><span data-stu-id="6f926-127">If you are using Office 365 operated by 21Vianet in China, replace the value for the <STRONG>ProxyFqdn</STRONG> parameter in this example ("exap.um.outlook.com") with the FQDN for the service operated by 21Vianet: "exap.um.partner.outlook.cn".</span></span>



</div>

  - <span data-ttu-id="6f926-128">**Identity** spécifie un identificateur de valeur de chaîne unique pour le fournisseur d’hébergement que vous créez (par exemple, « Exchange Online »).</span><span class="sxs-lookup"><span data-stu-id="6f926-128">**Identity** specifies a unique string value identifier for the hosting provider that you are creating (for example, "Exchange Online").</span></span> <span data-ttu-id="6f926-129">Les valeurs contenant des espaces doivent être placées entre des guillemets doubles.</span><span class="sxs-lookup"><span data-stu-id="6f926-129">Values that contain spaces must be in double quotation marks.</span></span>

  - <span data-ttu-id="6f926-130">**Enabled** indique si la connexion réseau entre votre domaine et le fournisseur d’hébergement est activée.</span><span class="sxs-lookup"><span data-stu-id="6f926-130">**Enabled** indicates whether the network connection between your domain and the hosting provider is enabled.</span></span> <span data-ttu-id="6f926-131">Cette valeur doit être définie sur **true**.</span><span class="sxs-lookup"><span data-stu-id="6f926-131">This must be set to **True**.</span></span>

  - <span data-ttu-id="6f926-132">**EnabledSharedAddressSpace** indique si le fournisseur d’hébergement sera utilisé dans un scénario d’espace d’adressage SIP partagé.</span><span class="sxs-lookup"><span data-stu-id="6f926-132">**EnabledSharedAddressSpace** indicates whether the hosting provider will be used in a shared SIP address space scenario.</span></span> <span data-ttu-id="6f926-133">Cette valeur doit être définie sur **true**.</span><span class="sxs-lookup"><span data-stu-id="6f926-133">This must be set to **True**.</span></span>

  - <span data-ttu-id="6f926-134">**HostsOCSUsers** indique si le fournisseur d’hébergement est utilisé pour héberger Office Communications Server ou Lync Server.</span><span class="sxs-lookup"><span data-stu-id="6f926-134">**HostsOCSUsers** indicates whether the hosting provider is used to host Office Communications Server or Lync Server.</span></span> <span data-ttu-id="6f926-135">Ce doit être défini sur **false**.</span><span class="sxs-lookup"><span data-stu-id="6f926-135">This must be set to **False**.</span></span>

  - <span data-ttu-id="6f926-136">**ProxyFQDN** spécifie le nom de domaine complet du serveur proxy utilisé par le fournisseur d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="6f926-136">**ProxyFQDN** specifies the fully qualified domain name (FQDN) for the proxy server used by the hosting provider.</span></span> <span data-ttu-id="6f926-137">Pour Exchange Online, le nom de domaine complet est exap.um.outlook.com.</span><span class="sxs-lookup"><span data-stu-id="6f926-137">For Exchange Online, the FQDN is exap.um.outlook.com.</span></span>

  - <span data-ttu-id="6f926-138">**IsLocal** indique si le serveur proxy utilisé par le fournisseur d’hébergement est contenu dans la topologie de votre serveur Lync.</span><span class="sxs-lookup"><span data-stu-id="6f926-138">**IsLocal** indicates whether the proxy server used by the hosting provider is contained within your Lync Server topology.</span></span> <span data-ttu-id="6f926-139">Ce doit être défini sur **false**.</span><span class="sxs-lookup"><span data-stu-id="6f926-139">This must be set to **False**.</span></span>

  - <span data-ttu-id="6f926-140">**VerificationLevel** indique le niveau de vérification autorisé pour les messages échangés avec le fournisseur hébergé.</span><span class="sxs-lookup"><span data-stu-id="6f926-140">**VerificationLevel** indicates the verification level allowed for messages that are sent to and from the hosted provider.</span></span> <span data-ttu-id="6f926-141">Spécifiez **UseSourceVerification**.</span><span class="sxs-lookup"><span data-stu-id="6f926-141">Specify **UseSourceVerification**.</span></span> <span data-ttu-id="6f926-142">Cette option repose sur le niveau de vérification inclus dans les messages envoyés par le fournisseur d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="6f926-142">This option relies on the verification level that is included in messages that are sent from the hosting provider.</span></span> <span data-ttu-id="6f926-143">Si ce niveau n’est pas spécifié, le message est rejeté comme invérifiable.</span><span class="sxs-lookup"><span data-stu-id="6f926-143">If this level is not specified, the message will be rejected as being unverifiable.</span></span>

</div>

<div>

## <a name="verify-replication-of-the-updated-central-management-store"></a><span data-ttu-id="6f926-144">Vérifier la réplication du magasin central de gestion mis à jour</span><span class="sxs-lookup"><span data-stu-id="6f926-144">Verify Replication of the Updated Central Management Store</span></span>

<span data-ttu-id="6f926-145">Les modifications que vous avez apportées à l’aide des applets de demande dans les sections précédentes s’appliquent automatiquement au serveur Edge et prennent généralement moins d’une minute à répliquer.</span><span class="sxs-lookup"><span data-stu-id="6f926-145">The changes that you made by using the cmdlets in the preceding sections are automatically applied to the Edge Server, and generally take less than one minute to replicate.</span></span> <span data-ttu-id="6f926-146">Vous pouvez vérifier l’état de la réplication et l’application des modifications à votre serveur Edge en utilisant les applets de commande suivantes.</span><span class="sxs-lookup"><span data-stu-id="6f926-146">You can verify the replication status and that the changes were applied to your Edge Server by using the following cmdlets.</span></span>

<span data-ttu-id="6f926-147">Pour vérifier les mises à jour de réplication sur un serveur interne dans le déploiement de Lync Server, exécutez l’applet de commande suivante :</span><span class="sxs-lookup"><span data-stu-id="6f926-147">To verify replication updates on a server internal in your Lync Server deployment, run the following cmdlet:</span></span>

    Get-CsManagementStoreReplicationStatus

<span data-ttu-id="6f926-148">Pour vérifier que les modifications ont été appliquées, exécutez l’applet de commande suivante sur le serveur Edge :</span><span class="sxs-lookup"><span data-stu-id="6f926-148">To verify that the changes were applied, run the following cmdlet on the Edge Server:</span></span>

    Get-CsHostingProvider -LocalStore

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="6f926-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6f926-149">See Also</span></span>


[<span data-ttu-id="6f926-150">Mise à disposition de la messagerie vocale Lync Server 2013 aux utilisateurs sur la messagerie unifiée Exchange hébergée</span><span class="sxs-lookup"><span data-stu-id="6f926-150">Providing Lync Server 2013 users voice mail on hosted Exchange UM</span></span>](lync-server-2013-providing-lync-server-users-voice-mail-on-hosted-exchange-um.md)  
[<span data-ttu-id="6f926-151">Intégration de la messagerie unifiée Exchange hébergée dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6f926-151">Hosted Exchange Unified Messaging integration in Lync Server 2013</span></span>](lync-server-2013-hosted-exchange-unified-messaging-integration.md)  
  

<span data-ttu-id="6f926-152"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6f926-152"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>
