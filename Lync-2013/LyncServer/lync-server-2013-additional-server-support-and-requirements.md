---
title: 'Lync Server 2013 : Autres prises en charge et configurations de serveur requises'
description: 'Lync Server 2013 : assistance et configuration serveur supplémentaires.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Additional server support and requirements
ms:assetid: 7622986b-abd6-4f45-8b5b-d5e2368521e8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398577(v=OCS.15)
ms:contentKeyID: 48184535
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3af9b3489ba62b3b2dc7cf4fa16cabfe80003e1e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440009"
---
# <a name="additional-server-support-and-requirements-in-lync-server-2013"></a><span data-ttu-id="95dd6-103">Autres prises en charge et configurations de serveur requises dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="95dd6-103">Additional server support and requirements in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="95dd6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="95dd6-104">

<span> </span></span></span>

<span data-ttu-id="95dd6-105">_**Dernière modification de la rubrique :** 2013-12-09_</span><span class="sxs-lookup"><span data-stu-id="95dd6-105">_**Topic Last Modified:** 2013-12-09_</span></span>

<span data-ttu-id="95dd6-106">Outre la prise en charge logicielle décrite dans les autres sections de cette documentation sur la prise en charge, Lync Server 2013 présente les limites de support suivantes :</span><span class="sxs-lookup"><span data-stu-id="95dd6-106">In addition to the software support described in the other sections of this Supportability documentation, Lync Server 2013 has the following support limitations:</span></span>

  - <span data-ttu-id="95dd6-107">Lync Server 2013 prend en charge le système de nom de domaine (DNS) et l’équilibrage de charge matérielle pour des rôles de serveur spécifiques.</span><span class="sxs-lookup"><span data-stu-id="95dd6-107">Lync Server 2013 supports Domain Name System (DNS) and hardware load balancing for specific server roles.</span></span> <span data-ttu-id="95dd6-108">Il prend également en charge l’équilibrage de charge des applications pour les serveurs de médiation, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="95dd6-108">It also supports application load balancing for Mediation Servers, where appropriate.</span></span> <span data-ttu-id="95dd6-109">Pour plus d’informations sur les situations d’utilisation, consultez la documentation de planification.</span><span class="sxs-lookup"><span data-stu-id="95dd6-109">For details about when to use each, see the Planning documentation.</span></span>

  - <span data-ttu-id="95dd6-110">Lync Server 2013 utilise le protocole DLX (distribution de liste de distribution) pour développer des listes de distribution.</span><span class="sxs-lookup"><span data-stu-id="95dd6-110">Lync Server 2013 uses the Distribution List Expansion Protocol (DLX) to expand distribution lists.</span></span> <span data-ttu-id="95dd6-111">Ce protocole spécifie également la méthode de service Web qui est utilisée pour obtenir l’appartenance d’une liste de distribution.</span><span class="sxs-lookup"><span data-stu-id="95dd6-111">This protocol also specifies the web service method that is used to get the membership of a distribution list.</span></span> <span data-ttu-id="95dd6-112">Microsoft Exchange Server prend en charge les groupes dynamiques qui n’ont pas de membres attribués de manière statique.</span><span class="sxs-lookup"><span data-stu-id="95dd6-112">Microsoft Exchange Server supports dynamic groups that do not have members statically assigned to them.</span></span> <span data-ttu-id="95dd6-113">Au lieu de cela, il stocke les requêtes évaluées lors du développement du groupe.</span><span class="sxs-lookup"><span data-stu-id="95dd6-113">Instead, they store queries that are evaluated when the group is expanded.</span></span> <span data-ttu-id="95dd6-114">DLX ne prend pas en charge les listes de distribution dynamiques.</span><span class="sxs-lookup"><span data-stu-id="95dd6-114">DLX does not support dynamic distribution lists.</span></span> <span data-ttu-id="95dd6-115">Cette limitation DLX s’applique à toutes les versions de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="95dd6-115">This DLX limitation applies to all versions of Lync Server.</span></span>

  - <span data-ttu-id="95dd6-116">L’Assistant permettre aux utilisateurs ne prenant pas en charge la conversion automatique des caractères non anglais en un URI compatible SIP, vous devez modifier manuellement l’adresse SIP.</span><span class="sxs-lookup"><span data-stu-id="95dd6-116">The Enable User Wizard does not support automatic conversion of non-English characters to a SIP-compliant URI, so you must modify the SIP address manually.</span></span>

  - <span data-ttu-id="95dd6-117">Pour les serveurs exécutant un logiciel antivirus, voir [exclusions de l’analyse antivirus pour Lync Server 2013](lync-server-2013-antivirus-scanning-exclusions.md) pour les exclusions de virus proposées et autres recommandations en matière de sécurité.</span><span class="sxs-lookup"><span data-stu-id="95dd6-117">For servers running antivirus software, refer to [Antivirus scanning exclusions for Lync Server 2013](lync-server-2013-antivirus-scanning-exclusions.md) for suggested virus exclusions and other security related recommendations.</span></span>

  - <span data-ttu-id="95dd6-118">Si vous utilisez IPsec, nous vous recommandons de désactiver IPsec par rapport aux plages de port utilisées pour le trafic audio et vidéo.</span><span class="sxs-lookup"><span data-stu-id="95dd6-118">If you use IPsec, we recommend disabling IPsec over the port ranges used for audio and video traffic.</span></span> <span data-ttu-id="95dd6-119">Pour plus d’informations, reportez-vous à la section [exceptions IPSec dans Lync Server 2013](lync-server-2013-ipsec-exceptions.md) dans la documentation de planification.</span><span class="sxs-lookup"><span data-stu-id="95dd6-119">For details, see [IPsec exceptions in Lync Server 2013](lync-server-2013-ipsec-exceptions.md) in the Planning documentation.</span></span>

  - <span data-ttu-id="95dd6-120">Si votre organisation utilise une infrastructure de qualité de service (QoS), le sous-système multimédia est compatible avec cette infrastructure.</span><span class="sxs-lookup"><span data-stu-id="95dd6-120">If your organization uses a Quality of Service (QoS) infrastructure, the media subsystem is designed to work within this existing infrastructure.</span></span> <span data-ttu-id="95dd6-121">Pour plus d’informations sur l’implémentation de QoS, voir [gestion de la qualité de service (QoS) dans Lync Server 2013](lync-server-2013-managing-quality-of-service-qos.md) dans la documentation des opérations.</span><span class="sxs-lookup"><span data-stu-id="95dd6-121">For details about implementing QoS, see [Managing Quality of Service (QoS) in Lync Server 2013](lync-server-2013-managing-quality-of-service-qos.md) in the Operations documentation.</span></span>

  - <span data-ttu-id="95dd6-122">L’utilisation du pare-feu du système d’exploitation est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="95dd6-122">Use of the operating system firewall is supported.</span></span> <span data-ttu-id="95dd6-123">Lync Server 2013 gère les exceptions de pare-feu pour le pare-feu du système d’exploitation, à l’exception du logiciel de base de données Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="95dd6-123">Lync Server 2013 manages the firewall exceptions for the operating system firewall, except for Microsoft SQL Server database software.</span></span> <span data-ttu-id="95dd6-124">Pour plus d’informations sur la configuration requise pour le pare-feu SQL Server, voir la documentation SQL Server.</span><span class="sxs-lookup"><span data-stu-id="95dd6-124">For details about SQL Server firewall requirements, see the SQL Server documentation.</span></span>

  - <span data-ttu-id="95dd6-125">Les interfaces externes utilisées pour mettre en œuvre la prise en charge de l’accès des utilisateurs externes doivent se trouver sur un sous-réseau distinct et *non* sur le même réseau que les interfaces internes.</span><span class="sxs-lookup"><span data-stu-id="95dd6-125">The external interfaces used to implement support for external user access must be on a separate subnet, *not* on the same network as the internal interfaces.</span></span>

  - <span data-ttu-id="95dd6-p106">La fonctionnalité XMPP de Lync Server 2013 est testée et prise en charge par Microsoft pour la fédération de messagerie instantanée avec Google Talk. Pour d’autres systèmes XMPP, contactez le fournisseur tier pour vérifier qu’il prend en charge la fédération avec Lync Server 2013 et pour obtenir d’autres recommandations de déploiement et de dépannage.</span><span class="sxs-lookup"><span data-stu-id="95dd6-p106">The XMPP capability of Lync Server 2013 is tested and supported by Microsoft for instant messaging federation with Google Talk. For any other XMPP systems contact the third-party vendor to verify that they support federation with Lync Server 2013, and for any deployment or troubleshooting recommendations.</span></span>

  - <span data-ttu-id="95dd6-128">Avec la publication des mises à jour cumulatives de Lync Server 2013 : juillet 2013, Lync Server 2013 prend désormais en charge l’authentification à deux facteurs.</span><span class="sxs-lookup"><span data-stu-id="95dd6-128">With the release of Lync Server 2013 Cumulative Updates: July 2013, Lync Server 2013 now supports two-factor authentication.</span></span> <span data-ttu-id="95dd6-129">Pour plus d’informations, reportez-vous à la rubrique [authentification à deux facteurs dans Lync Server 2013](lync-server-2013-planning-for-and-deploying-two-factor-authentication.md).</span><span class="sxs-lookup"><span data-stu-id="95dd6-129">For more information, see [Two-factor authentication in Lync Server 2013](lync-server-2013-planning-for-and-deploying-two-factor-authentication.md).</span></span>

  - <span data-ttu-id="95dd6-130">La plupart des serveurs internes nécessitent un type de certificat défini comme **authentification d’ouverture** (OAuth).</span><span class="sxs-lookup"><span data-stu-id="95dd6-130">Most internal servers require a certificate type defined as **Open Authentication** (OAuth).</span></span> <span data-ttu-id="95dd6-131">Vous devez demander et attribuer un certificat OAuth lors de la phase de **demande, d’installation et d’attribution des certificats** de l’Assistant Déploiement de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="95dd6-131">You are required to request and assign an OAuth certificate during the **Request, Install and Assign Certificates** phase of the Lync Server Deployment Wizard.</span></span> <span data-ttu-id="95dd6-132">La taille minimale d’une clé de certificat OAuth est de 1024 bits.</span><span class="sxs-lookup"><span data-stu-id="95dd6-132">The minimum size for an OAuth certificate key is 1024 bits.</span></span> <span data-ttu-id="95dd6-133">Un avertissement risque de s’afficher si vous demandez un certificat dont la longueur de la clé est inférieure à 2048 bits.</span><span class="sxs-lookup"><span data-stu-id="95dd6-133">A warning may be displayed if you request a certificate with a key length less than 2048 bits in length.</span></span> <span data-ttu-id="95dd6-134">Pour éviter d’éventuels problèmes dans le cas où une longueur de clé de 2048 est appliquée au lieu d’être prévenu, il est vivement recommandé de toujours utiliser une longueur de clé d' 2048 pour les certificats OAuth.</span><span class="sxs-lookup"><span data-stu-id="95dd6-134">To avoid potential problems in the event that a key length of 2048 is enforced instead of warned, it is strongly recommended to always use a key length of 2048 for OAuth certificates.</span></span>

  - <span data-ttu-id="95dd6-135">Lync Server 2013 et Microsoft Exchange Server 2010 Service Pack 1 (SP1) prennent en charge les algorithmes 140-2 FIPS (Federal Information Processing Standard) si les systèmes d’exploitation Windows Server 2008 R2 sont configurés pour utiliser les algorithmes 140-2 FIPS pour le chiffrement du système.</span><span class="sxs-lookup"><span data-stu-id="95dd6-135">Lync Server 2013 and Microsoft Exchange Server 2010 Service Pack 1 (SP1) operate with support for Federal Information Processing Standard (FIPS) 140-2 algorithms if the Windows Server 2008 R2 operating systems are configured to use the FIPS 140-2 algorithms for system cryptography.</span></span> <span data-ttu-id="95dd6-136">Pour mettre en œuvre la prise en charge du FIPS, vous devez configurer chaque serveur exécutant Lync Server 2013 pour le prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="95dd6-136">To implement FIPS support, you must configure each server running Lync Server 2013 to support it.</span></span> <span data-ttu-id="95dd6-137">Pour plus d’informations sur les algorithmes compatibles FIPS et sur l’implémentation de la prise en charge de la sécurité FIPS, voir l’article de la base de connaissances Microsoft 811833, «chiffrement de système : utiliser les algorithmes compatibles FIPS pour le chiffrement, le hachage et le paramètre de sécurité de signature dans Windows XP et les versions ultérieures de Windows sur [https://go.microsoft.com/fwlink/p/?linkid=3052\&kbid=811833](https://go.microsoft.com/fwlink/p/?linkid=3052%26kbid=811833) .</span><span class="sxs-lookup"><span data-stu-id="95dd6-137">For details about FIPS-compliant algorithms and how to implement FIPS support, see Microsoft Knowledge Base article 811833, "System cryptography: Use FIPS compliant algorithms for encryption, hashing, and signing security setting in Windows XP and in later versions of Windows at [https://go.microsoft.com/fwlink/p/?linkid=3052\&kbid=811833](https://go.microsoft.com/fwlink/p/?linkid=3052%26kbid=811833).</span></span> <span data-ttu-id="95dd6-138">Pour plus d’informations sur la prise en charge et les limitations de FIPS 140-2 dans Exchange 2010, voir « Exchange 2010 SP1 et prise en charge des algorithmes compatibles FIPS » à l’adresse [https://go.microsoft.com/fwlink/p/?linkId=205335](https://go.microsoft.com/fwlink/p/?linkid=205335) .</span><span class="sxs-lookup"><span data-stu-id="95dd6-138">For details about FIPS 140-2 support and limitations in Exchange 2010, see "Exchange 2010 SP1 and Support for FIPS Compliant Algorithms" at [https://go.microsoft.com/fwlink/p/?linkId=205335](https://go.microsoft.com/fwlink/p/?linkid=205335).</span></span>

<span data-ttu-id="95dd6-139">Lync Server 2013 nécessite l’installation d’autres logiciels sur des composants spécifiques avant ou lors du déploiement.</span><span class="sxs-lookup"><span data-stu-id="95dd6-139">Lync Server 2013 requires the installation of other software on specific components prior to or during deployment.</span></span> <span data-ttu-id="95dd6-140">Cela inclut les logiciels disponibles avec le système d’exploitation, le logiciel téléchargeable et les logiciels qui sont automatiquement installés lors de l’installation de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="95dd6-140">This includes software that is available with the operating system, downloadable software, and software that is automatically installed during installation of Lync Server 2013.</span></span> <span data-ttu-id="95dd6-141">Vous trouverez ci-dessous une liste de logiciels supplémentaires qui peuvent être nécessaires :</span><span class="sxs-lookup"><span data-stu-id="95dd6-141">Following is a list of additional software that can be required:</span></span>

  - <span data-ttu-id="95dd6-142">Windows Update</span><span class="sxs-lookup"><span data-stu-id="95dd6-142">Windows Update</span></span>

  - <span data-ttu-id="95dd6-143">Windows Identity Foundation</span><span class="sxs-lookup"><span data-stu-id="95dd6-143">Windows Identity Foundation</span></span>

  - <span data-ttu-id="95dd6-144">Microsoft .NET 4,5 Framework</span><span class="sxs-lookup"><span data-stu-id="95dd6-144">Microsoft .NET 4.5 Framework</span></span>

  - <span data-ttu-id="95dd6-145">Microsoft Visual C++ 2012 redistribuable</span><span class="sxs-lookup"><span data-stu-id="95dd6-145">Microsoft Visual C++ 2012 Redistributable</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="95dd6-146">Microsoft Visual C++ 2012 redistribuable est automatiquement installé lors de l’installation de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="95dd6-146">Microsoft Visual C++ 2012 Redistributable is automatically installed when you install Lync Server 2013.</span></span> <span data-ttu-id="95dd6-147">Vous ne devez pas installer et utiliser une autre version.</span><span class="sxs-lookup"><span data-stu-id="95dd6-147">You should not install and use any other version.</span></span>

    
    </div>

  - <span data-ttu-id="95dd6-148">Module de réécriture d’URL version 2,0 redistribuable</span><span class="sxs-lookup"><span data-stu-id="95dd6-148">URL Rewrite Module version 2.0 Redistributable</span></span>

  - <span data-ttu-id="95dd6-149">Module d’exécution du format Windows Media</span><span class="sxs-lookup"><span data-stu-id="95dd6-149">Windows Media Format Runtime</span></span>

  - <span data-ttu-id="95dd6-150">Windows PowerShell version 3,0</span><span class="sxs-lookup"><span data-stu-id="95dd6-150">Windows PowerShell version 3.0</span></span>

  - <span data-ttu-id="95dd6-151">Plug-in Microsoft Silverlight 4 Browser (Silverlight 4.0.50524.0 ou la version la plus récente du panneau de configuration de Lync Server)</span><span class="sxs-lookup"><span data-stu-id="95dd6-151">Microsoft Silverlight 4 browser plug-in (Silverlight 4.0.50524.0 or the latest version for Lync Server Control Panel)</span></span>

  - <span data-ttu-id="95dd6-152">Outils de services de domaine Active Directory</span><span class="sxs-lookup"><span data-stu-id="95dd6-152">Active Directory Domain Services tools</span></span>

<span data-ttu-id="95dd6-153">Certaines de ces configurations logicielles s’appliquent uniquement aux rôles ou composants serveur spécifiques.</span><span class="sxs-lookup"><span data-stu-id="95dd6-153">Some of these software requirements only apply to specific server roles or components.</span></span> <span data-ttu-id="95dd6-154">Pour plus d’informations sur la configuration logicielle requise, voir [configuration logicielle requise pour Lync Server 2013](lync-server-2013-additional-software-requirements.md) dans la documentation de planification.</span><span class="sxs-lookup"><span data-stu-id="95dd6-154">For details about these software requirements, see [Additional software requirements for Lync Server 2013](lync-server-2013-additional-software-requirements.md) in the Planning documentation.</span></span>

<span data-ttu-id="95dd6-155"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="95dd6-155"></div>

<span> </span>

</div>

</div>

</span></span></div>

