---
title: 'Lync Server 2013 : meilleures pratiques pour votre infrastructure principale'
description: 'Lync Server 2013 : meilleures pratiques pour votre infrastructure de base.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Best practices for your core infrastructure in Lync Server 2013
ms:assetid: 44aff88d-536c-4613-a81e-5398c9c6a648
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn518328(v=OCS.15)
ms:contentKeyID: 61071242
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d0ea7cb9c7685a3b6f7c04146ec5631bbac10fe6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436040"
---
# <a name="best-practices-for-your-core-infrastructure-in-lync-server-2013"></a><span data-ttu-id="0864d-103">Recommandations en matière d’infrastructure de base dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0864d-103">Best practices for your core infrastructure in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0864d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0864d-104">

<span> </span></span></span>

<span data-ttu-id="0864d-105">_**Dernière modification de la rubrique :** 2014-01-27_</span><span class="sxs-lookup"><span data-stu-id="0864d-105">_**Topic Last Modified:** 2014-01-27_</span></span>

<span data-ttu-id="0864d-106">Vous avez probablement déjà pris des mesures pour intégrer la tolérance de pannes dans votre système, en utilisant des pratiques telles que la garantie de la redondance matérielle, la prévention de la perte d'alimentation, l'installation régulière des mises à jour, l'établissement des mesures de sécurité antivirus et la surveillance de l'activité du serveur.</span><span class="sxs-lookup"><span data-stu-id="0864d-106">You have probably already taken steps to design fault tolerance in your system, using practices such as ensuring hardware redundancy, guarding against power loss, routinely installing security updates and antivirus measures, and Monitoring Server activity.</span></span> <span data-ttu-id="0864d-107">Ces pratiques profitent non seulement de votre infrastructure Microsoft Lync Server 2013, mais aussi de votre réseau entier.</span><span class="sxs-lookup"><span data-stu-id="0864d-107">These practices benefit not only your Microsoft Lync Server 2013 infrastructure, but also your entire network.</span></span> <span data-ttu-id="0864d-108">Si vous n’avez pas implémenté ces pratiques, nous vous conseillons de le faire avant de déployer Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0864d-108">If you have not implemented these practices, we recommend that you do so before deploying Lync Server 2013.</span></span>

<span data-ttu-id="0864d-109">Pour vous aider à protéger les serveurs dans votre déploiement de Lync Server 2013 contre les dommages accidentels ou intentionnelles susceptibles d’entraîner un temps d’arrêt, prenez les précautions suivantes :</span><span class="sxs-lookup"><span data-stu-id="0864d-109">To help protect the servers in your Lync Server 2013 deployment from accidental or purposeful harm that might result in downtime, take the following precautions:</span></span>

  - <span data-ttu-id="0864d-110">Maintenez vos serveurs à jour avec les mises à jour de sécurité.</span><span class="sxs-lookup"><span data-stu-id="0864d-110">Keep your servers up-to-date with security updates.</span></span> <span data-ttu-id="0864d-111">En vous abonnant au service de notification de sécurité de Microsoft, vous recevez la notification immédiate des bulletins de sécurité pour les produits Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0864d-111">Subscribing to the Microsoft Security Notification Service helps ensure that you receive immediate notification of security bulletin releases for any Microsoft product.</span></span> <span data-ttu-id="0864d-112">Pour vous abonner, accédez au site Web Microsoft Technical Security notifications à l’adresse [https://go.microsoft.com/fwlink/p/?LinkId=145202](https://go.microsoft.com/fwlink/p/?linkid=145202) .</span><span class="sxs-lookup"><span data-stu-id="0864d-112">To subscribe, go to the Microsoft Technical Security Notifications website at [https://go.microsoft.com/fwlink/p/?LinkId=145202](https://go.microsoft.com/fwlink/p/?linkid=145202).</span></span>

  - <span data-ttu-id="0864d-113">Assurez-vous que les droits d'accès sont configurés correctement.</span><span class="sxs-lookup"><span data-stu-id="0864d-113">Ensure that access rights are set up correctly.</span></span>

  - <span data-ttu-id="0864d-p103">Conservez vos serveurs dans un environnement physique qui empêche l'accès non autorisé. Assurez-vous que le logiciel antivirus adéquat est installé sur tous vos serveurs. Maintenez le logiciel à jour avec les derniers fichiers de signatures de virus. Utilisez la fonction de mise à jour automatique de votre application antivirus pour maintenir à jour les signatures de virus.</span><span class="sxs-lookup"><span data-stu-id="0864d-p103">Keep your servers in a physical environment that prevents unauthorized access. Ensure that adequate antivirus software is installed on all your servers. Keep the software up-to-date with the latest virus signature files. Use the automatic update feature of your antivirus application to keep the virus signatures current.</span></span>

  - <span data-ttu-id="0864d-118">Nous vous recommandons de désactiver les services du système d’exploitation Windows Server qui ne sont pas nécessaires sur les ordinateurs sur lesquels vous installez Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0864d-118">We recommend that you disable the Windows Server operating system services that are not required on the computers where you install Lync Server 2013.</span></span>

  - <span data-ttu-id="0864d-119">Chiffrez les systèmes d'exploitation et les lecteurs de disques où les données sont stockées à l'aide d'un système de chiffrement de volume complet, sauf si vous pouvez garantir un contrôle constant et total des serveurs, l'isolement physique complet et la désaffectation adéquate et sûre des disques remplacés ou défaillants.</span><span class="sxs-lookup"><span data-stu-id="0864d-119">Encrypt operating systems and disk drives where data is stored with a full-volume encryption system, unless you can guarantee constant and complete control of the servers, total physical isolation, and proper and secure decommissioning of replaced or failed disk drives.</span></span>

  - <span data-ttu-id="0864d-120">Désactivez tous les ports DMA (Direct Memory Access) externes du serveur, sauf si vous pouvez garantir un contrôle très strict de l'accès physique aux serveurs.</span><span class="sxs-lookup"><span data-stu-id="0864d-120">Disable all external Direct Memory Access (DMA) ports of the server, unless you can guarantee very tight control over the physical access to the servers.</span></span> <span data-ttu-id="0864d-121">Les attaques basées sur DMA, qui peuvent être lancées assez facilement, risquent d'exposer des informations très sensibles, telles que les clés de chiffrement privées.</span><span class="sxs-lookup"><span data-stu-id="0864d-121">DMA-based attacks, which can be initiated fairly easily, could expose very sensitive information, such as private encryption keys.</span></span>

<span data-ttu-id="0864d-122"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0864d-122"></div>

<span> </span>

</div>

</div>

</span></span></div>

