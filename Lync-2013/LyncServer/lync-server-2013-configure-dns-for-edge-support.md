---
title: 'Lync Server 2013 : Configuration de DNS pour la prise en charge de périphérie'
description: 'Lync Server 2013 : configurer le système DNS pour la prise en charge de Edge.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure DNS for edge support
ms:assetid: 955493e6-aa29-424d-bb81-1ef87b3b15e3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398756(v=OCS.15)
ms:contentKeyID: 48184894
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 706f4915adda58dbb72b8dd8921e0cc612833718
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395120"
---
# <a name="configure-dns-for-edge-support-in-lync-server-2013"></a><span data-ttu-id="1821d-103">Configuration de DNS pour la prise en charge de périphérie dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1821d-103">Configure DNS for edge support in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1821d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1821d-104">

<span> </span></span></span>

<span data-ttu-id="1821d-105">_**Dernière modification de la rubrique :** 2013-02-15_</span><span class="sxs-lookup"><span data-stu-id="1821d-105">_**Topic Last Modified:** 2013-02-15_</span></span>

<span data-ttu-id="1821d-106">Vous devez configurer les enregistrements DNS (Domain Name System) pour les interfaces de périphérie interne et externe, y compris les interfaces de serveur Edge et de proxy inverse.</span><span class="sxs-lookup"><span data-stu-id="1821d-106">You must configure Domain Name System (DNS) records for internal and external edge interfaces, including both Edge Server and reverse proxy interfaces.</span></span> <span data-ttu-id="1821d-107">Par défaut, les serveurs de périphérie ne sont pas joints à un domaine et ne disposent pas de nom de domaine complet (nom de domaine complet).</span><span class="sxs-lookup"><span data-stu-id="1821d-107">By default, Edge Servers are not joined to a domain and will not have a fully qualified domain name (fully qualified domain name).</span></span> <span data-ttu-id="1821d-108">Le serveur de périphérie est uniquement désigné par le nom court (ordinateur), et non par un nom de domaine complet.</span><span class="sxs-lookup"><span data-stu-id="1821d-108">The Edge Server is only referred to by the short (machine) name, not a fully qualified domain name.</span></span> <span data-ttu-id="1821d-109">Toutefois, le générateur de topologie utilise les noms de domaine complets et non les noms courts.</span><span class="sxs-lookup"><span data-stu-id="1821d-109">However, Topology Builder uses FQDNs, not short names.</span></span> <span data-ttu-id="1821d-110">Le nom du serveur de périphérie doit correspondre au nom de domaine complet utilisé par le générateur de topologie.</span><span class="sxs-lookup"><span data-stu-id="1821d-110">The name of the Edge Server must match the FQDN used by Topology Builder.</span></span> <span data-ttu-id="1821d-111">Pour ce faire, vous devez définir un suffixe DNS qui, lorsqu’il est combiné avec le nom de l’ordinateur, génère le FQDN attendu.</span><span class="sxs-lookup"><span data-stu-id="1821d-111">To do this, you define a DNS suffix that, when combined with the machine name, results in the expected FQDN.</span></span> <span data-ttu-id="1821d-112">Utilisez la procédure suivante dans « pour ajouter le suffixe DNS au nom de l’ordinateur sur un serveur Edge qui n’est pas joint à un domaine » pour ajouter le suffixe DNS au nom de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="1821d-112">Use the following procedure in “To add the DNS suffix to the computer name on and Edge Server that is not joined to a domain” to add the DNS suffix to the computer name.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="1821d-113">Par défaut, DNS utilise un algorithme de tourniquet pour faire pivoter l’ordre des données d’enregistrement de ressource renvoyées dans les réponses de la requête lorsque plusieurs enregistrements de ressource du même type existent pour un nom de domaine DNS interrogé.</span><span class="sxs-lookup"><span data-stu-id="1821d-113">By default, DNS uses a round robin algorithm to rotate the order of resource record data returned in query answers where multiple resource records of the same type exist for a queried DNS domain name.</span></span> <span data-ttu-id="1821d-114">L’équilibrage de charge DNS de Lync Server 2013 dépend du mécanisme de tourniquet DNS en tant que composant du mécanisme d’équilibrage de charge DNS.</span><span class="sxs-lookup"><span data-stu-id="1821d-114">Lync Server 2013 DNS load balancing, depends on DNS round-robin as a part of the DNS Load Balancing mechanism.</span></span> <span data-ttu-id="1821d-115">Vérifiez que le paramètre de tourniquet n’a pas été désactivé.</span><span class="sxs-lookup"><span data-stu-id="1821d-115">Verify that round-robin setting has not been disabled.</span></span> <span data-ttu-id="1821d-116">Si vous utilisez un serveur DNS qui n’exécute pas de système d’exploitation Windows, vérifiez que la commande d’enregistrement de ressource à répétition alternée est activée.</span><span class="sxs-lookup"><span data-stu-id="1821d-116">If you are using a DNS server that is not running a Windows operating system, verify that round-robin resource record ordering is enabled.</span></span>



</div>

<span data-ttu-id="1821d-117">Pour créer et vérifier chaque enregistrement SRV DNS, procédez comme suit dans «**pour créer un enregistrement SRV DNS**».</span><span class="sxs-lookup"><span data-stu-id="1821d-117">Use the following procedures in “**To create a DNS SRV record**” to create and verify each DNS SRV record.</span></span> <span data-ttu-id="1821d-118">Utilisez la procédure de la section «**pour créer un enregistrement DNS a**» pour définir les enregistrements DNS a requis pour l’accès des utilisateurs externes.</span><span class="sxs-lookup"><span data-stu-id="1821d-118">Use the procedure in “**To create a DNS A record**” to define the DNS A records required for external user access.</span></span> <span data-ttu-id="1821d-119">Pour vérifier que les enregistrements sont configurés et qu’ils fonctionnent correctement, voir la section «**pour vérifier un enregistrement DNS**» de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="1821d-119">To confirm that the records are configured and working correctly, see “**To verify a DNS record**” in this topic.</span></span> <span data-ttu-id="1821d-120">Pour plus d’informations sur les enregistrements nécessaires à la prise en charge de l’accès des utilisateurs externes, voir [déterminer les exigences DNS pour Lync Server 2013](lync-server-2013-determine-dns-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="1821d-120">For details about each record required to support external user access, see [Determine DNS requirements for Lync Server 2013](lync-server-2013-determine-dns-requirements.md).</span></span>

<div>

## <a name="to-add-the-dns-suffix-to-the-computer-name-on-an-edge-server-that-is-not-joined-to-a-domain"></a><span data-ttu-id="1821d-121">Pour ajouter le suffixe DNS au nom de l’ordinateur sur un serveur Edge qui n’est pas joint à un domaine</span><span class="sxs-lookup"><span data-stu-id="1821d-121">To add the DNS suffix to the computer name on an Edge Server that is not joined to a domain</span></span>

1.  <span data-ttu-id="1821d-122">Sur l’ordinateur, cliquez sur **Démarrer**, cliquez avec le bouton droit sur **ordinateur**, puis cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="1821d-122">On the computer, click **Start**, right-click **Computer**, and then click **Properties**.</span></span>

2.  <span data-ttu-id="1821d-123">Sous **paramètres de nom d’ordinateur, de domaine et de groupe de travail**, cliquez sur **modifier les paramètres**.</span><span class="sxs-lookup"><span data-stu-id="1821d-123">Under **Computer name, domain, and workgroup settings**, click **Change settings**.</span></span>

3.  <span data-ttu-id="1821d-124">Dans l’onglet nom de l' **ordinateur** , cliquez sur **modifier**.</span><span class="sxs-lookup"><span data-stu-id="1821d-124">On the **Computer Name** tab, click **Change**.</span></span>

4.  <span data-ttu-id="1821d-125">Dans la **modification du nom ou du domaine** de l’ordinateur, cliquez sur **plus**.</span><span class="sxs-lookup"><span data-stu-id="1821d-125">In **Computer Name/Domain Changes**, click **More**.</span></span>

5.  <span data-ttu-id="1821d-126">Dans **nom d’ordinateur NetBIOS et suffixe DNS**, dans **suffixe DNS principal de cet ordinateur**, tapez le nom de votre domaine interne (par exemple, Corp.contoso.com), puis cliquez sur **OK** à trois reprises.</span><span class="sxs-lookup"><span data-stu-id="1821d-126">In **DNS Suffix and NetBIOS Computer Name**, in **Primary DNS suffix of this computer**, type the name of your internal domain (for example, corp.contoso.com), and then click **OK** three times.</span></span>

6.  <span data-ttu-id="1821d-127">Redémarrez l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="1821d-127">Restart the computer.</span></span>

</div>

<div>

## <a name="to-create-a-dns-srv-record"></a><span data-ttu-id="1821d-128">Pour créer un enregistrement SRV DNS</span><span class="sxs-lookup"><span data-stu-id="1821d-128">To create a DNS SRV record</span></span>

1.  <span data-ttu-id="1821d-129">Sur le serveur DNS approprié, cliquez sur **Démarrer**, sur **panneau de configuration**, sur **Outils d’administration**, puis sur **DNS**.</span><span class="sxs-lookup"><span data-stu-id="1821d-129">On the appropriate DNS server, click **Start**, click **Control Panel**, click **Administrative Tools**, and then click **DNS**.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="1821d-130">Vous devez configurer le DNS de manière à ce qu’il y ait : 1) entrées DNS externes pour les recherches DNS externes par les utilisateurs distants et les partenaires fédérés ; 2) entrées pour les recherches DNS pour une utilisation par les serveurs Edge au sein du réseau de périmètre (également connu sous le nom de DMZ, zone démilitarisée et sous-réseau filtré), y compris les enregistrements des serveurs internes exécutant Lync Server 2013 ; et 3) entrées DNS internes pour les recherches par les clients et serveurs internes exécutant Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1821d-130">You need to configure DNS so that there are: 1) external DNS entries for external DNS lookups by remote users and federated partners; 2) entries for DNS lookups for use by the Edge Servers within the perimeter network (also known as DMZ, demilitarized zone, and screened subnet), including A records for the internal servers running Lync Server 2013; and 3) internal DNS entries for lookups by the internal clients and servers running Lync Server 2013.</span></span>

    
    </div>

2.  <span data-ttu-id="1821d-131">Dans l’arborescence de la console de votre domaine SIP, développez **zones de recherche directe**, puis cliquez avec le bouton droit sur le domaine sur lequel Lync Server 2013 est installé.</span><span class="sxs-lookup"><span data-stu-id="1821d-131">In the console tree for your SIP domain, expand **Forward Lookup Zones**, and then right-click the domain where Lync Server 2013 is installed.</span></span>

3.  <span data-ttu-id="1821d-132">Cliquez sur **nouveaux enregistrements**.</span><span class="sxs-lookup"><span data-stu-id="1821d-132">Click **Other New Records**.</span></span>

4.  <span data-ttu-id="1821d-133">Dans **Sélectionner un type d’enregistrement de ressource**, tapez **emplacement du service (SRV)**, puis cliquez sur **créer un enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="1821d-133">In **Select a resource record type**, type **Service Location (SRV)**, and then click **Create Record**.</span></span>

5.  <span data-ttu-id="1821d-134">Fournissez toutes les informations requises pour l’enregistrement SRV DNS.</span><span class="sxs-lookup"><span data-stu-id="1821d-134">Provide all required information for the DNS SRV record.</span></span>

</div>

<div>

## <a name="to-create-a-dns-a-record"></a><span data-ttu-id="1821d-135">Pour créer un enregistrement DNS A</span><span class="sxs-lookup"><span data-stu-id="1821d-135">To create a DNS A record</span></span>

1.  <span data-ttu-id="1821d-136">Sur le serveur DNS, cliquez sur **Démarrer**, sur **panneau de configuration**, sur **Outils d’administration**, puis sur **DNS**.</span><span class="sxs-lookup"><span data-stu-id="1821d-136">On the DNS server, click **Start**, click **Control Panel**, click **Administrative Tools**, and then click **DNS**.</span></span>

2.  <span data-ttu-id="1821d-137">Dans l’arborescence de la console de votre domaine SIP, développez **zones de recherche directe**, puis cliquez avec le bouton droit sur le domaine dans lequel Lync Server 2013 est installé.</span><span class="sxs-lookup"><span data-stu-id="1821d-137">In the console tree for your SIP domain, expand **Forward Lookup Zones**, and then right-click the domain in which Lync Server 2013 is installed.</span></span>

3.  <span data-ttu-id="1821d-138">Cliquez sur **nouvel hôte (A)**.</span><span class="sxs-lookup"><span data-stu-id="1821d-138">Click **New Host (A)**.</span></span>

4.  <span data-ttu-id="1821d-139">Fournissez toutes les informations requises pour l’enregistrement SRV DNS.</span><span class="sxs-lookup"><span data-stu-id="1821d-139">Provide all required information for the DNS SRV record.</span></span>

</div>

<div>

## <a name="to-verify-a-dns-record"></a><span data-ttu-id="1821d-140">Pour vérifier un enregistrement DNS</span><span class="sxs-lookup"><span data-stu-id="1821d-140">To verify a DNS record</span></span>

1.  <span data-ttu-id="1821d-141">Connectez-vous à un ordinateur client dans le domaine.</span><span class="sxs-lookup"><span data-stu-id="1821d-141">Log on to a client computer in the domain.</span></span>

2.  <span data-ttu-id="1821d-142">Cliquez sur **Démarrer**, puis sur **Exécuter**.</span><span class="sxs-lookup"><span data-stu-id="1821d-142">Click **Start**, and then click **Run**.</span></span>

3.  <span data-ttu-id="1821d-143">À l’invite de commandes, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="1821d-143">At the command prompt, run the following command:</span></span>
    
        nslookup <FQDN edge interface>

4.  <span data-ttu-id="1821d-144">Vérifiez que vous recevez une réponse qui est résolue en adresse IP appropriée pour le nom de domaine complet (FQDN).</span><span class="sxs-lookup"><span data-stu-id="1821d-144">Verify that you receive a reply that resolves to the appropriate IP address for the FQDN.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="1821d-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1821d-145">See Also</span></span>


[<span data-ttu-id="1821d-146">Création d’un enregistrement SRV DNS pour l’intégrer à la messagerie unifiée Exchange hébergée</span><span class="sxs-lookup"><span data-stu-id="1821d-146">Create a DNS SRV record for integration with hosted Exchange UM</span></span>](lync-server-2013-create-a-dns-srv-record-for-integration-with-hosted-exchange-um.md)  


[<span data-ttu-id="1821d-147">Détermination de la configuration requise pour DNS pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1821d-147">Determine DNS requirements for Lync Server 2013</span></span>](lync-server-2013-determine-dns-requirements.md)  
  

<span data-ttu-id="1821d-148"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1821d-148"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

