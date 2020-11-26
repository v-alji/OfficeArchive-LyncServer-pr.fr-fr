---
title: 'Lync Server 2013 : Création et vérification des enregistrements SRV DNS'
description: 'Lync Server 2013 : création et vérification des enregistrements SRV DNS.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create and verify DNS SRV records
ms:assetid: 86888c7e-1401-458f-9a7b-08ac726deeec
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398680(v=OCS.15)
ms:contentKeyID: 48184714
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a71c876d0b26b9305feed7146fa6321a3983588d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432015"
---
# <a name="create-and-verify-dns-srv-records-in-lync-server-2013"></a><span data-ttu-id="39f33-103">Création et vérification des enregistrements SRV DNS dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="39f33-103">Create and verify DNS SRV records in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="39f33-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="39f33-104">

<span> </span></span></span>

<span data-ttu-id="39f33-105">_**Dernière modification de la rubrique :** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="39f33-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="39f33-106">Pour effectuer cette procédure, vous devez être connecté au serveur ou au domaine au minimum en tant que membre du groupe administrateurs de domaine ou membre du groupe DnsAdmins.</span><span class="sxs-lookup"><span data-stu-id="39f33-106">To successfully complete this procedure, you should be logged on to the server or domain minimally as a member of the Domain Admins group or a member of the DnsAdmins group.</span></span>

<span data-ttu-id="39f33-107">Cette rubrique décrit comment configurer les enregistrements DNS (Domain Name System) nécessaires à la création dans les déploiements Lync Server 2013 et ceux requis pour la connexion automatique du client.</span><span class="sxs-lookup"><span data-stu-id="39f33-107">This topic describes how to configure the Domain Name System (DNS) records that you are required to create in Lync Server 2013 deployments and those required for automatic client sign in.</span></span> <span data-ttu-id="39f33-108">Lorsque vous créez un pool frontal, le programme d’installation crée des objets et des paramètres Active Directory pour le pool, y compris le nom de domaine complet (FQDN) du pool.</span><span class="sxs-lookup"><span data-stu-id="39f33-108">When you create a Front End pool, Setup creates Active Directory objects and settings for the pool, including the pool fully qualified domain name (FQDN).</span></span> <span data-ttu-id="39f33-109">Des objets et des paramètres similaires sont créés pour un serveur Standard Edition Server.</span><span class="sxs-lookup"><span data-stu-id="39f33-109">Similar objects and settings are created for a Standard Edition server.</span></span> <span data-ttu-id="39f33-110">Pour que les clients puissent se connecter au pool ou Standard Edition Server, le nom de domaine complet (FQDN) du pool ou du serveur Standard Edition doit être enregistré dans DNS.</span><span class="sxs-lookup"><span data-stu-id="39f33-110">For clients to be able to connect to the pool or Standard Edition server, the FQDN of the pool or Standard Edition server must be registered in DNS.</span></span> <span data-ttu-id="39f33-111">Vous devez créer des enregistrements DNS SRV dans votre DNS interne pour chaque domaine SIP.</span><span class="sxs-lookup"><span data-stu-id="39f33-111">You must create DNS SRV records in your internal DNS for every SIP domain.</span></span> <span data-ttu-id="39f33-112">Cette procédure part du principe que votre DNS interne comporte des zones pour vos domaines d’utilisateur SIP.</span><span class="sxs-lookup"><span data-stu-id="39f33-112">This procedure assumes that your internal DNS has zones for your SIP user domains.</span></span>

<div>

## <a name="to-configure-a-dns-srv-record"></a><span data-ttu-id="39f33-113">Pour configurer un enregistrement SRV DNS</span><span class="sxs-lookup"><span data-stu-id="39f33-113">To configure a DNS SRV record</span></span>

1.  <span data-ttu-id="39f33-114">Sur le serveur DNS, cliquez sur **Démarrer**, sur **Outils d’administration**, puis sur **DNS**.</span><span class="sxs-lookup"><span data-stu-id="39f33-114">On the DNS server, click **Start**, click **Administrative Tools**, and then click **DNS**.</span></span>

2.  <span data-ttu-id="39f33-115">Dans l’arborescence de la console de votre domaine SIP, développez **zones de recherche directe**, puis cliquez avec le bouton droit sur le domaine SIP sur lequel Lync Server 2013 sera installé.</span><span class="sxs-lookup"><span data-stu-id="39f33-115">In the console tree for your SIP domain, expand **Forward Lookup Zones**, and then right-click the SIP domain in which Lync Server 2013 will be installed.</span></span>

3.  <span data-ttu-id="39f33-116">Cliquez sur **nouveaux enregistrements**.</span><span class="sxs-lookup"><span data-stu-id="39f33-116">Click **Other New Records**.</span></span>

4.  <span data-ttu-id="39f33-117">Dans **Choisissez un type d’enregistrement de ressource**, cliquez sur **Emplacement du service (SRV)**, puis sur **Créer un enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="39f33-117">In **Select a resource record type**, click **Service Location (SRV)**, and then click **Create Record**.</span></span>

5.  <span data-ttu-id="39f33-118">Cliquez sur **service**, puis tapez **\_ sipinternaltls**.</span><span class="sxs-lookup"><span data-stu-id="39f33-118">Click **Service**, and then type **\_sipinternaltls**.</span></span>

6.  <span data-ttu-id="39f33-119">Cliquez sur **protocole**, puis tapez **\_ TCP**.</span><span class="sxs-lookup"><span data-stu-id="39f33-119">Click **Protocol**, and then type **\_tcp**.</span></span>

7.  <span data-ttu-id="39f33-120">Cliquez sur **Numéro de port**, puis saisissez **5061**.</span><span class="sxs-lookup"><span data-stu-id="39f33-120">Click **Port Number**, and then type **5061**.</span></span>

8.  <span data-ttu-id="39f33-121">Cliquez sur **Hôte offrant ce service**, puis tapez le nom de domaine complet du pool ou du serveur en édition Standard.</span><span class="sxs-lookup"><span data-stu-id="39f33-121">Click **Host offering this service**, and then type the FQDN of the pool or Standard Edition server.</span></span>

9.  <span data-ttu-id="39f33-122">Cliquez sur **OK**, puis sur **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="39f33-122">Click **OK**, and then click **Done**.</span></span>

</div>

<div>

## <a name="to-verify-the-creation-of-a-dns-srv-record"></a><span data-ttu-id="39f33-123">Pour vérifier la création d’un enregistrement SRV DNS</span><span class="sxs-lookup"><span data-stu-id="39f33-123">To verify the creation of a DNS SRV record</span></span>

1.  <span data-ttu-id="39f33-124">Ouvrez une session sur un ordinateur client du domaine dont le compte est membre du groupe Utilisateurs authentifiés ou qui dispose des autorisations équivalentes.</span><span class="sxs-lookup"><span data-stu-id="39f33-124">Log on to a client computer in the domain with an account that is a member of the Authenticated Users group or has equivalent permissions.</span></span>

2.  <span data-ttu-id="39f33-125">Cliquez sur **Démarrer**, puis sur **Exécuter**.</span><span class="sxs-lookup"><span data-stu-id="39f33-125">Click **Start**, and then click **Run**.</span></span>

3.  <span data-ttu-id="39f33-126">Dans la zone **ouvrir** , tapez **cmd**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="39f33-126">In the **Open** box, type **cmd**, and then click **OK**.</span></span>

4.  <span data-ttu-id="39f33-127">À l’invite de commandes, tapez **nslookup**, puis appuyez sur entrée.</span><span class="sxs-lookup"><span data-stu-id="39f33-127">At the command prompt, type **nslookup**, and then press ENTER.</span></span>

5.  <span data-ttu-id="39f33-128">Tapez **Set type = SRV**, puis appuyez sur entrée.</span><span class="sxs-lookup"><span data-stu-id="39f33-128">Type **set type=srv**, and then press ENTER.</span></span>

6.  <span data-ttu-id="39f33-129">Tapez **\_ sipinternaltls. \_ tcp.contoso.com**, puis appuyez sur entrée.</span><span class="sxs-lookup"><span data-stu-id="39f33-129">Type **\_sipinternaltls.\_tcp.contoso.com**, and then press ENTER.</span></span> <span data-ttu-id="39f33-130">Le résultat affiché pour l’enregistrement TLS (Transport Layer Security) est le suivant :</span><span class="sxs-lookup"><span data-stu-id="39f33-130">The output displayed for the Transport Layer Security (TLS) record is as follows:</span></span>
    
    <span data-ttu-id="39f33-131">Serveur : \<dns server\> . contoso.com</span><span class="sxs-lookup"><span data-stu-id="39f33-131">Server: \<dns server\>.contoso.com</span></span>
    
    <span data-ttu-id="39f33-132">Corriger \<IP address of DNS server\></span><span class="sxs-lookup"><span data-stu-id="39f33-132">Address: \<IP address of DNS server\></span></span>
    
    <span data-ttu-id="39f33-133">Réponse ne faisant pas autorité :</span><span class="sxs-lookup"><span data-stu-id="39f33-133">Non-authoritative answer:</span></span>
    
    <span data-ttu-id="39f33-134">\_sipinternaltls. \_ emplacement du service SRV tcp.contoso.com :</span><span class="sxs-lookup"><span data-stu-id="39f33-134">\_sipinternaltls.\_tcp.contoso.com SRV service location:</span></span>
    
    <span data-ttu-id="39f33-135">Priority = 0</span><span class="sxs-lookup"><span data-stu-id="39f33-135">priority = 0</span></span>
    
    <span data-ttu-id="39f33-136">épaisseur = 0</span><span class="sxs-lookup"><span data-stu-id="39f33-136">weight = 0</span></span>
    
    <span data-ttu-id="39f33-137">port = 5061</span><span class="sxs-lookup"><span data-stu-id="39f33-137">port = 5061</span></span>
    
    <span data-ttu-id="39f33-138">SVR nom d’hôte = poolname.contoso.com (ou enregistrement d’un serveur Standard Edition)</span><span class="sxs-lookup"><span data-stu-id="39f33-138">svr hostname = poolname.contoso.com (or Standard Edition server A record)</span></span>
    
    <span data-ttu-id="39f33-139">poolname.contoso.com adresse Internet = \<virtual IP Address of the load balancer\> ou \<IP address of a single Enterprise Edition server for pools with only one Enterprise Edition server\>\<IP address of the Standard Edition server\></span><span class="sxs-lookup"><span data-stu-id="39f33-139">poolname.contoso.com internet address = \<virtual IP Address of the load balancer\> or \<IP address of a single Enterprise Edition server for pools with only one Enterprise Edition server\> or \<IP address of the Standard Edition server\></span></span>

7.  <span data-ttu-id="39f33-140">Lorsque vous avez terminé, à l’invite de commandes, tapez **Exit**, puis appuyez sur entrée.</span><span class="sxs-lookup"><span data-stu-id="39f33-140">When you are finished, at the command prompt, type **exit**, and then press ENTER.</span></span>

</div>

<div>

## <a name="to-verify-that-the-fqdn-of-the-front-end-pool-or-standard-edition-server-can-be-resolved"></a><span data-ttu-id="39f33-141">Pour vérifier que le nom de domaine complet (FQDN) du pool frontal ou du serveur Standard Edition peut être résolu</span><span class="sxs-lookup"><span data-stu-id="39f33-141">To verify that the FQDN of the Front End pool or Standard Edition server can be resolved</span></span>

1.  <span data-ttu-id="39f33-142">Connectez-vous à un ordinateur client dans le domaine.</span><span class="sxs-lookup"><span data-stu-id="39f33-142">Log on to a client computer in the domain.</span></span>

2.  <span data-ttu-id="39f33-143">Cliquez sur **Démarrer**, puis sur **Exécuter**.</span><span class="sxs-lookup"><span data-stu-id="39f33-143">Click **Start**, and then click **Run**.</span></span>

3.  <span data-ttu-id="39f33-144">Dans la zone **ouvrir** , tapez **cmd**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="39f33-144">In the **Open** box, type **cmd**, and then click **OK**.</span></span>

4.  <span data-ttu-id="39f33-145">À l’invite de commandes, tapez **nslookup** \<FQDN of the Front End pool\> , puis \<FQDN of the Standard Edition server\> Appuyez sur entrée.</span><span class="sxs-lookup"><span data-stu-id="39f33-145">At the command prompt, type **nslookup** \<FQDN of the Front End pool\> or \<FQDN of the Standard Edition server\>, and then press ENTER.</span></span>

5.  <span data-ttu-id="39f33-146">Vérifiez que vous recevez une réponse qui est résolue en adresse IP appropriée pour le nom de domaine complet (FQDN).</span><span class="sxs-lookup"><span data-stu-id="39f33-146">Verify that you receive a reply that resolves to the appropriate IP address for the FQDN.</span></span>

<span data-ttu-id="39f33-147"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="39f33-147"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

