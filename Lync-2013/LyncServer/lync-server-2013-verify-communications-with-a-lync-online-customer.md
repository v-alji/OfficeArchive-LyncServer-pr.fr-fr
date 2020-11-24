---
title: 'Lync Server 2013 : vérifier les communications avec un client Lync Online'
description: 'Lync Server 2013 : vérifier les communications avec un client Lync Online.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Verify communications with a Lync Online customer
ms:assetid: c8287b15-e1bb-4b26-8354-0ec90b2fcfe7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202189(v=OCS.15)
ms:contentKeyID: 48185378
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 867b0f7ffffd563c869b9bcd5443a3cb91b156af
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395061"
---
# <a name="verify-communications-with-a-lync-online-customer-in-lync-server-2013"></a><span data-ttu-id="66c9a-103">Vérifier les communications avec un client Lync Online dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="66c9a-103">Verify communications with a Lync Online customer in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="66c9a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="66c9a-104">

<span> </span></span></span>

<span data-ttu-id="66c9a-105">_**Dernière modification de la rubrique :** 2012-10-08_</span><span class="sxs-lookup"><span data-stu-id="66c9a-105">_**Topic Last Modified:** 2012-10-08_</span></span>

<span data-ttu-id="66c9a-106">Pour permettre aux utilisateurs de Lync de votre organisation de communiquer avec des utilisateurs d’un client Microsoft Lync Online 2010, vous devez effectuer les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="66c9a-106">To enable Lync users in your organization to communicate with users of a Microsoft Lync Online 2010 customer, you must have completed the following steps:</span></span>

  - <span data-ttu-id="66c9a-107">Rempli toutes les conditions préalables.</span><span class="sxs-lookup"><span data-stu-id="66c9a-107">Met all prerequisites.</span></span> <span data-ttu-id="66c9a-108">Cela inclut le déploiement de vos serveurs internes et de périphérie, l’activation de la prise en charge de la Fédération pour votre organisation et la configuration des comptes d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="66c9a-108">This includes deploying your internal and edge servers, enabling federation support for your organization, and setting up user accounts.</span></span> <span data-ttu-id="66c9a-109">Pour plus d’informations, reportez-vous [à la configuration requise pour fédérer avec un client Lync Online dans Lync Server 2013](lync-server-2013-prerequisites-for-federating-with-a-lync-online-customer.md).</span><span class="sxs-lookup"><span data-stu-id="66c9a-109">For details, see [Prerequisites for federating with a Lync Online customer in Lync Server 2013](lync-server-2013-prerequisites-for-federating-with-a-lync-online-customer.md).</span></span>

  - <span data-ttu-id="66c9a-110">Configuration de la prise en charge de l’accès au domaine dans votre déploiement interne.</span><span class="sxs-lookup"><span data-stu-id="66c9a-110">Configured domain access support in your internal deployment.</span></span> <span data-ttu-id="66c9a-111">Cela inclut la création d’une entrée de fournisseur d’hébergement et la configuration de votre déploiement pour autoriser l’accès à partir du domaine du client Lync Online.</span><span class="sxs-lookup"><span data-stu-id="66c9a-111">This includes creating a host provider entry and configuring your deployment to allow access from the Lync Online customer’s domain.</span></span> <span data-ttu-id="66c9a-112">Pour plus d’informations, voir [configurer la prise en charge de la Fédération pour un domaine Lync Online dans Lync Server 2013](lync-server-2013-configure-federation-support-for-a-lync-online-domain.md).</span><span class="sxs-lookup"><span data-stu-id="66c9a-112">For details, see [Configure federation support for a Lync Online domain in Lync Server 2013](lync-server-2013-configure-federation-support-for-a-lync-online-domain.md).</span></span>

  - <span data-ttu-id="66c9a-113">Configuré vos comptes d’utilisateurs pour la prise en charge de la Fédération ;</span><span class="sxs-lookup"><span data-stu-id="66c9a-113">Configured your user accounts to support federation.</span></span> <span data-ttu-id="66c9a-114">Pour plus d’informations, voir [configurer l’accès utilisateur pour la Fédération avec un client Lync Online dans Lync Server 2013](lync-server-2013-configure-user-access-for-federation-with-a-lync-online-customer.md).</span><span class="sxs-lookup"><span data-stu-id="66c9a-114">For details, see [Configure user access for federation with a Lync Online customer in Lync Server 2013](lync-server-2013-configure-user-access-for-federation-with-a-lync-online-customer.md).</span></span>

<span data-ttu-id="66c9a-115">Après avoir effectué toutes les étapes décrites dans le tableau ci-dessous, vous devez effectuer toutes les 2010 étapes de configuration de ses services en ligne pour la prise en charge de la Fédération avec votre organisation, en testant les communications entre un utilisateur interne au sein de votre organisation et un utilisateur du client Lync Online.</span><span class="sxs-lookup"><span data-stu-id="66c9a-115">After you complete all of these steps and the administrator of the Lync Online 2010 customer completes all configuration of their online services to support federation with your organization, verify communications by testing communications between an internal user in your organization and a user of the Lync Online customer.</span></span> <span data-ttu-id="66c9a-116">Si la communication échoue, utilisez l’outil de journalisation de votre serveur de périphérie pour capturer les fichiers de journaux et de suivi afin de résoudre le problème.</span><span class="sxs-lookup"><span data-stu-id="66c9a-116">If communication is not successful, use the Logging Tool from your Edge Server to capture log and trace files in order to troubleshoot the problem.</span></span> <span data-ttu-id="66c9a-117">Pour plus d’informations sur l’utilisation de l’outil journalisation, voir [ouvrir les outils d’administration de Lync Server 2013](lync-server-2013-open-lync-server-administrative-tools.md) dans la documentation sur les opérations.</span><span class="sxs-lookup"><span data-stu-id="66c9a-117">For details about using the Logging Tool, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md) in the Operations documentation.</span></span> <span data-ttu-id="66c9a-118">Pour plus d’informations sur l’outil de journalisation, voir la documentation de l’outil de journalisation Lync Server 2010 dans la bibliothèque TechNet à l’adresse [https://go.microsoft.com/fwlink/p/?linkId=199265](https://go.microsoft.com/fwlink/p/?linkid=199265) .</span><span class="sxs-lookup"><span data-stu-id="66c9a-118">For details about the Logging Tool, see the Lync Server 2010 Logging Tool documentation on the TechNet Library at [https://go.microsoft.com/fwlink/p/?linkId=199265](https://go.microsoft.com/fwlink/p/?linkid=199265).</span></span>

<span data-ttu-id="66c9a-119"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="66c9a-119"></div>

<span> </span>

</div>

</div>

</span></span></div>

