---
title: 'Lync Server 2013 : TLS et MTLS'
description: 'Lync Server 2013 : TLS et MTLS.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: TLS and MTLS for Lync Server 2013
ms:assetid: b32a5b85-fc82-42dc-a9b2-96400f8cd2b8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn481133(v=OCS.15)
ms:contentKeyID: 59893873
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a0ccee47e635435dd5f0d5eae03711c0cd5e517b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439696"
---
# <a name="tls-and-mtls-for-lync-server-2013"></a><span data-ttu-id="988e2-103">TLS et MTLS pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="988e2-103">TLS and MTLS for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="988e2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="988e2-104">

<span> </span></span></span>

<span data-ttu-id="988e2-105">_**Dernière modification de la rubrique :** 2013-11-07_</span><span class="sxs-lookup"><span data-stu-id="988e2-105">_**Topic Last Modified:** 2013-11-07_</span></span>

<span data-ttu-id="988e2-106">Les protocoles de transport TLS (Transport Layer Security) et MTLS (Mutual TLS) fournissent des communications chiffrées et une authentification du point de terminaison sur Internet.</span><span class="sxs-lookup"><span data-stu-id="988e2-106">Transport Layer Security (TLS) and Mutual Transport Layer Security (MTLS) protocols provide encrypted communications and endpoint authentication on the Internet.</span></span> <span data-ttu-id="988e2-107">Microsoft Lync Server 2013 utilise ces deux protocoles pour créer le réseau des serveurs de confiance et garantir que toutes les communications réseau sont chiffrées.</span><span class="sxs-lookup"><span data-stu-id="988e2-107">Microsoft Lync Server 2013 uses these two protocols to create the network of trusted servers and to ensure that all communications over that network are encrypted.</span></span> <span data-ttu-id="988e2-108">Toutes les communications SIP entre les serveurs interviennent sur MTLS.</span><span class="sxs-lookup"><span data-stu-id="988e2-108">All SIP communications between servers occur over MTLS.</span></span> <span data-ttu-id="988e2-109">Les communications SIP du client au serveur interviennent sur TLS.</span><span class="sxs-lookup"><span data-stu-id="988e2-109">SIP communications from client to server occur over TLS.</span></span>

<span data-ttu-id="988e2-110">TLS permet aux utilisateurs, par le biais de leur logiciel client, d’authentifier les serveurs Lync Server 2013 auxquels ils se connectent.</span><span class="sxs-lookup"><span data-stu-id="988e2-110">TLS enables users, through their client software, to authenticate the Lync Server 2013 servers to which they connect.</span></span> <span data-ttu-id="988e2-111">Sur une connexion TLS, le client demande un certificat valide du serveur.</span><span class="sxs-lookup"><span data-stu-id="988e2-111">On a TLS connection, the client requests a valid certificate from the server.</span></span> <span data-ttu-id="988e2-112">Pour être valide, le certificat doit avoir été émis par une autorité de certification qui est également approuvée par le client et le nom DNS du serveur doit correspondre au nom DNS dans le certificat.</span><span class="sxs-lookup"><span data-stu-id="988e2-112">To be valid, the certificate must have been issued by a CA that is also trusted by the client and the DNS name of the server must match the DNS name on the certificate.</span></span> <span data-ttu-id="988e2-113">Si le certificat est valide, le client utilise la clé publique du certificat pour chiffrer les clés de chiffrement symétriques à utiliser pour la communication, de sorte que seul le propriétaire d’origine du certificat peut utiliser sa clé privée pour déchiffrer le contenu de la communication.</span><span class="sxs-lookup"><span data-stu-id="988e2-113">If the certificate is valid, the client uses the public key in the certificate to encrypt the symmetric encryption keys to be used for the communication, so only the original owner of the certificate can use its private key to decrypt the contents of the communication.</span></span> <span data-ttu-id="988e2-114">La connexion résultante est approuvée et à partir de ce point n’est pas contestée par d’autres serveurs ou clients approuvés.</span><span class="sxs-lookup"><span data-stu-id="988e2-114">The resulting connection is trusted and from that point is not challenged by other trusted servers or clients.</span></span> <span data-ttu-id="988e2-115">Dans ce contexte, le protocole SSL (Secure Sockets Layer) utilisé avec les services Web peut être associé au protocole TLS.</span><span class="sxs-lookup"><span data-stu-id="988e2-115">Within this context, Secure Sockets Layer (SSL) as used with Web services can be associated as TLS-based.</span></span>

<span data-ttu-id="988e2-116">Les connexions serveur à serveur s’appuient sur MTLS pour l’authentification mutuelle.</span><span class="sxs-lookup"><span data-stu-id="988e2-116">Server-to-server connections rely on MTLS for mutual authentication.</span></span> <span data-ttu-id="988e2-117">Sur une connexion MTLS, le serveur à l’origine d’un message et le serveur le recevant échangent des certificats à partir d’une autorité de certification mutuellement approuvée.</span><span class="sxs-lookup"><span data-stu-id="988e2-117">On an MTLS connection, the server originating a message and the server receiving it exchange certificates from a mutually trusted CA.</span></span> <span data-ttu-id="988e2-118">Les certificats prouvent l’identité d’un serveur à un autre.</span><span class="sxs-lookup"><span data-stu-id="988e2-118">The certificates prove the identity of each server to the other.</span></span> <span data-ttu-id="988e2-119">Dans les déploiements de Lync Server 2013, les certificats émis par une autorité de certification d’entreprise qui sont au cours de leur période de validité et qui ne sont pas révoqués par l’autorité de certification sont automatiquement considérés comme valides par tous les clients et serveurs internes dans la mesure où tous les membres d’un domaine Active Directory approuvent la CA d’entreprise dans ce domaine.</span><span class="sxs-lookup"><span data-stu-id="988e2-119">In Lync Server 2013 deployments, certificates issued by the enterprise CA that are during their validity period and not revoked by the issuing CA are automatically considered valid by all internal clients and servers because all members of an Active Directory domain trust the Enterprise CA in that domain.</span></span> <span data-ttu-id="988e2-120">Dans les scénarios fédérés, l’autorité de certification émettrice doit être approuvée par les deux partenaires fédérés.</span><span class="sxs-lookup"><span data-stu-id="988e2-120">In federated scenarios, the issuing CA must be trusted by both federated partners.</span></span> <span data-ttu-id="988e2-121">Chaque partenaire peut utiliser une autorité différente s’il le souhaite, tant que cette autorité est également approuvée par l’autre partenaire.</span><span class="sxs-lookup"><span data-stu-id="988e2-121">Each partner can use a different CA, if desired, so long as that CA is also trusted by the other partner.</span></span> <span data-ttu-id="988e2-122">Cette approbation est plus facilement obtenue par les serveurs Edge qui disposent d’un certificat de l’autorité de certification racine du partenaire parmi leurs autorités de certification racines de confiance, ou bien en utilisant une autorité tierce qui est approuvée par les deux parties.</span><span class="sxs-lookup"><span data-stu-id="988e2-122">This trust is most easily accomplished by the Edge Servers having the partner’s root CA certificate in their trusted root CAs, or by use of a third-party CA that is trusted by both parties.</span></span>

<span data-ttu-id="988e2-123">TLS et MTLS permettent d’empêcher les attaques par écoute et les attaques d’intercepteur.</span><span class="sxs-lookup"><span data-stu-id="988e2-123">TLS and MTLS help prevent both eavesdropping and man-in-the middle attacks.</span></span> <span data-ttu-id="988e2-124">Dans le cas d’une attaque d’intercepteur, l’attaquant réachemine les communications entre deux entités de réseau via l’ordinateur de l’attaquant sans que l’autre partie n’en ait connaissance.</span><span class="sxs-lookup"><span data-stu-id="988e2-124">In a man-in-the-middle attack, the attacker reroutes communications between two network entities through the attacker’s computer without the knowledge of either party.</span></span> <span data-ttu-id="988e2-125">Les caractéristiques de protocoles TLS et Lync Server 2013 des serveurs de confiance (uniquement celles spécifiées dans le générateur de topologie) permettent de limiter le risque d’une attaque du milieu au milieu de la couche d’application en utilisant le chiffrement de bout en bout coordonné à l’aide du chiffrement de clé publique entre les deux points de terminaison. un attaquant doit disposer d’un certificat valide et approuvé avec la clé privée correspondante et est délivré au nom du service sur lequel le client communique pour déchiffrer la communication.</span><span class="sxs-lookup"><span data-stu-id="988e2-125">TLS and Lync Server 2013 specification of trusted servers (only those specified in Topology Builder) mitigate the risk of a man-in-the middle attack partially on the application layer by using end-to-end encryption coordinated using the Public Key cryptography between the two endpoints, and an attacker would have to have a valid and trusted certificate with the corresponding private key and issued to the name of the service to which the client is communicating to decrypt the communication.</span></span> <span data-ttu-id="988e2-126">Enfin, vous devez toutefois respecter les meilleures pratiques de sécurité avec votre infrastructure réseau (dans ce cas, DNS d’entreprise).</span><span class="sxs-lookup"><span data-stu-id="988e2-126">Ultimately, however, you must follow best security practices with your networking infrastructure (in this case corporate DNS).</span></span> <span data-ttu-id="988e2-127">Lync Server 2013 suppose que le serveur DNS est digne de confiance de la même façon que les contrôleurs de domaine et les catalogues globaux sont approuvés, mais le service DNS fournit un niveau de protection contre les attaques de détournement de DNS en empêchant le serveur d’un attaquant de répondre avec le nom usurpé.</span><span class="sxs-lookup"><span data-stu-id="988e2-127">Lync Server 2013 assumes that the DNS server is trusted in the same way that domain controllers and global catalogs are trusted, but DNS does provide a level of safeguard against DNS hijack attacks by preventing an attacker’s server from responding successfully to a request to the spoofed name.</span></span>

<span data-ttu-id="988e2-128">La figure suivante montre à un niveau élevé la façon dont Lync Server 2013 utilise MTLS pour créer un réseau de serveurs approuvés.</span><span class="sxs-lookup"><span data-stu-id="988e2-128">The following figure shows at a high level how Lync Server 2013 uses MTLS to create a network of trusted servers.</span></span>

<span data-ttu-id="988e2-129">**Connexions approuvées dans un réseau Lync Server**</span><span class="sxs-lookup"><span data-stu-id="988e2-129">**Trusted connections in a Lync Server network**</span></span>

<span data-ttu-id="988e2-130">![437749da-c372-4f0d-ac72-ccfd5191696b](images/Dn481133.437749da-c372-4f0d-ac72-ccfd5191696b(OCS.15).jpg "437749da-c372-4f0d-ac72-ccfd5191696b")</span><span class="sxs-lookup"><span data-stu-id="988e2-130">![437749da-c372-4f0d-ac72-ccfd5191696b](images/Dn481133.437749da-c372-4f0d-ac72-ccfd5191696b(OCS.15).jpg "437749da-c372-4f0d-ac72-ccfd5191696b")</span></span>

<span data-ttu-id="988e2-131"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="988e2-131"></div>

<span> </span>

</div>

</div>

</span></span></div>

