---
title: 'Lync Server 2013 : guide d’approvisionnement pour la connectivité Lync-Skype'
description: 'Lync Server 2013 : Guide de mise en service pour la connectivité Lync-Skype.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Provisioning guide for Lync-Skype connectivity
ms:assetid: 69adda9b-5b72-4538-9be6-079b2f462e09
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn440173(v=OCS.15)
ms:contentKeyID: 57793363
ms.date: 11/26/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9859a7a621ba4329fe0436fe50a0d9de1d0ae1ef
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436740"
---
# <a name="provisioning-guide-for-lync-skype-connectivity-in-lync-server-2013"></a><span data-ttu-id="4833e-103">Guide d’approvisionnement pour la connectivité Lync-Skype dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4833e-103">Provisioning guide for Lync-Skype connectivity in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4833e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4833e-104">

<span> </span></span></span>

<span data-ttu-id="4833e-105">_**Dernière modification de la rubrique :** 2014-11-26_</span><span class="sxs-lookup"><span data-stu-id="4833e-105">_**Topic Last Modified:** 2014-11-26_</span></span>

<span data-ttu-id="4833e-106">Lync Server 2013 prend en charge la connectivité avec Skype.</span><span class="sxs-lookup"><span data-stu-id="4833e-106">Lync Server 2013 supports connectivity with Skype.</span></span> <span data-ttu-id="4833e-107">Cette connectivité permet aux utilisateurs de Lync 2013 d’ajouter des contacts Skype à l’aide du compte Microsoft de l’utilisateur Skype.</span><span class="sxs-lookup"><span data-stu-id="4833e-107">This connectivity enables your Lync 2013 users to add Skype contacts by using the Skype user’s Microsoft Account (MSA).</span></span> <span data-ttu-id="4833e-108">Les clients Skype peuvent également ajouter des utilisateurs Lync à leur liste de contacts.</span><span class="sxs-lookup"><span data-stu-id="4833e-108">Skype clients can also add Lync users to their contact list.</span></span> <span data-ttu-id="4833e-109">En fonction des stratégies qui sont définies par l’intermédiaire de Lync Server, les utilisateurs de Lync et de Skype pourront communiquer à l’aide de la messagerie instantanée, voir la présence de chacun d’eux et lancer des appels audio et vidéo.</span><span class="sxs-lookup"><span data-stu-id="4833e-109">Based on policies administratively set in Lync Server, Lync and Skype users will be able to communicate using instant messaging, see each other’s presence, and initiate audio and video calls.</span></span> <span data-ttu-id="4833e-110">Lync-Skype connectivité est également une fonctionnalité de Lync Online qui peut être activée pour les clients de Lync Online à partir du centre d’administration Lync dans le centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="4833e-110">Lync-Skype connectivity is also a feature of Lync Online, and can be enabled for Lync Online customers from the Lync Administration Center within the Microsoft 365 admin center.</span></span>

<div>

> [!IMPORTANT]  
> <span data-ttu-id="4833e-p102">Si Lync Server est configuré pour se connecter à Windows Messenger via la connectivité PIC (Public IM Connectivity), votre déploiement est déjà configuré pour la connectivité Lync-Skype. Vous pouvez éventuellement modifier votre entrée Messenger PIC existante pour utiliser Skype. Pour plus d'informations, voir « Configurer le paramètre de fournisseur PIC Skype pour Lync » plus loin dans ce guide.</span><span class="sxs-lookup"><span data-stu-id="4833e-p102">If Lync Server is already configured to connect with Windows Messenger by using Public Instant Messaging Connectivity (PIC), your deployment is already configured for Lync-Skype connectivity. The only change you may want to consider is to rename your existing Messenger PIC entry as Skype. For details, see Configure the Skype PIC provider setting for Lync later in this guide.</span></span>

</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="4833e-114">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="4833e-114">In This Section</span></span>

  - [<span data-ttu-id="4833e-115">Remarque concernant la connectivité Lync-Skype dans Lync Server 2013 pour les clients Lync Online</span><span class="sxs-lookup"><span data-stu-id="4833e-115">Note about Lync-Skype connectivity in Lync Server 2013 for Lync Online customers</span></span>](lync-server-2013-note-about-lync-skype-connectivity-for-lync-on.md)

  - [<span data-ttu-id="4833e-116">Accès au site d’approvisionnement de connectivité PIC de Lync Server à partir de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4833e-116">Accessing the Lync Server public IM connectivity provisioning site from Lync Server 2013</span></span>](lync-server-2013-accessing-the-lync-server-public-im-connectivity-provisioning-site.md)

  - [<span data-ttu-id="4833e-117">Activation de la connectivité Lync-Skype dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4833e-117">Enabling Lync-Skype connectivity in Lync Server 2013</span></span>](lync-server-2013-enabling-lync-skype-connectivity.md)

  - [<span data-ttu-id="4833e-118">Utilisation de la connectivité Lync-Skype dans Lync Server 2013 en tant qu’utilisateur final</span><span class="sxs-lookup"><span data-stu-id="4833e-118">Using Lync-Skype connectivity in Lync Server 2013 as an end user</span></span>](lync-server-2013-using-lync-skype-connectivity-as-an-end-user.md)

  - [<span data-ttu-id="4833e-119">Forum aux questions : approvisionnement de Lync Server 2013 pour la connectivité Skype</span><span class="sxs-lookup"><span data-stu-id="4833e-119">Frequently Asked Questions: Provisioning Lync Server 2013 for Skype connectivity</span></span>](lync-server-2013-frequently-asked-questions-provisioning-lync-server-for-skype-connectivity.md)

<span data-ttu-id="4833e-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4833e-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

