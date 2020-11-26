---
title: 'Lync Server 2013 : configuration de la prise en charge de la Fédération pour un client Lync Online'
description: 'Lync Server 2013 : configuration de la prise en charge de la Fédération pour un client Lync Online.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring federation support for a Lync Online customer
ms:assetid: e5f7f38d-ede5-4af3-88c2-026e8a78df12
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202193(v=OCS.15)
ms:contentKeyID: 48185669
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6b5e7995e686a9492b3a4be98a92b848716cacf9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433114"
---
# <a name="configuring-federation-support-for-a-lync-online-customer-in-lync-server-2013"></a><span data-ttu-id="a275c-103">Configuration de la prise en charge de la Fédération pour un client Lync Online dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a275c-103">Configuring federation support for a Lync Online customer in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a275c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a275c-104">

<span> </span></span></span>

<span data-ttu-id="a275c-105">_**Dernière modification de la rubrique :** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="a275c-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="a275c-106">Vous pouvez fournir des services de communication aux utilisateurs de votre organisation de l’une des façons suivantes :</span><span class="sxs-lookup"><span data-stu-id="a275c-106">You can provide communications services to users in your organization in any of the following ways:</span></span>

  - <span data-ttu-id="a275c-107">Déploiement de Lync Server 2013 au sein de votre organisation (connu sous le nom de *services locaux*) et configuration de comptes d’utilisateur Lync 2013 au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="a275c-107">Deploying Lync Server 2013 in your organization (known as *on-premises services*) and setting up Lync 2013 user accounts in your organization.</span></span>

  - <span data-ttu-id="a275c-108">Configurer un compte client Microsoft Lync Online 2010 auprès d’un fournisseur d’hébergement et configurer des comptes d’utilisateurs avec le fournisseur d’hébergement (appelé *services en ligne*).</span><span class="sxs-lookup"><span data-stu-id="a275c-108">Setting up a Microsoft Lync Online 2010 customer account with a Hosting Provider and setting up user accounts with the Hosting Provider (known as *online services*).</span></span>

<span data-ttu-id="a275c-109">Si vous déployez Lync 2013 au sein de votre organisation, vous pouvez fédérer avec les domaines d’un ou de plusieurs clients Microsoft Lync Online 2010.</span><span class="sxs-lookup"><span data-stu-id="a275c-109">If you deploy Lync 2013 in your organization, you can federate with the domains of one or more Microsoft Lync Online 2010 customers.</span></span> <span data-ttu-id="a275c-110">Pour permettre la Fédération entre les utilisateurs de votre déploiement local Lync 2013 et des utilisateurs d’un client 2010 Online, vous devez configurer la prise en charge du domaine et des utilisateurs du client Lync Online.</span><span class="sxs-lookup"><span data-stu-id="a275c-110">To enable federation between users of your on-premises Lync 2013 deployment and users of a Lync Online 2010 customer, you must configure support for the domain and users of the Lync Online customer.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a275c-111">Cette documentation décrit uniquement les procédures de configuration de votre organisation pour la prise en charge de la Fédération avec un client 2010 Lync Online.</span><span class="sxs-lookup"><span data-stu-id="a275c-111">This documentation describes only the procedures for configuring your organization to support federation with an Lync Online 2010 customer.</span></span> <span data-ttu-id="a275c-112">Cette documentation ne décrit pas les procédures de configuration du client 2010 Lync Online pour la prise en charge de la Fédération.</span><span class="sxs-lookup"><span data-stu-id="a275c-112">This documentation does not describe the procedures for configuring the Lync Online 2010 customer to support federation.</span></span> <span data-ttu-id="a275c-113">Pour plus d’informations sur Lync Online Services, consultez Lync Online à l’adresse <A href="https://go.microsoft.com/fwlink/p/?linkid=218941">https://go.microsoft.com/fwlink/p/?linkId=218941</A> .</span><span class="sxs-lookup"><span data-stu-id="a275c-113">For details about Lync Online services, see Lync Online at <A href="https://go.microsoft.com/fwlink/p/?linkid=218941">https://go.microsoft.com/fwlink/p/?linkId=218941</A>.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="a275c-114">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="a275c-114">In This Section</span></span>

  - [<span data-ttu-id="a275c-115">Conditions préalables à la Fédération avec un client Lync Online dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a275c-115">Prerequisites for federating with a Lync Online customer in Lync Server 2013</span></span>](lync-server-2013-prerequisites-for-federating-with-a-lync-online-customer.md)

  - [<span data-ttu-id="a275c-116">Configurer la prise en charge de la Fédération pour un domaine Lync Online dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a275c-116">Configure federation support for a Lync Online domain in Lync Server 2013</span></span>](lync-server-2013-configure-federation-support-for-a-lync-online-domain.md)

  - [<span data-ttu-id="a275c-117">Configurer l’accès utilisateur pour la Fédération avec un client Lync Online dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a275c-117">Configure user access for federation with a Lync Online customer in Lync Server 2013</span></span>](lync-server-2013-configure-user-access-for-federation-with-a-lync-online-customer.md)

  - [<span data-ttu-id="a275c-118">Vérifier les communications avec un client Lync Online dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a275c-118">Verify communications with a Lync Online customer in Lync Server 2013</span></span>](lync-server-2013-verify-communications-with-a-lync-online-customer.md)

<span data-ttu-id="a275c-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a275c-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

