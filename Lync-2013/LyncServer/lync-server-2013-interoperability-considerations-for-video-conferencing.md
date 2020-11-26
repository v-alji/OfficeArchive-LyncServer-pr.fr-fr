---
title: 'Lync Server 2013 : considérations d’interopérabilité pour les conférences vidéo'
description: 'Lync Server 2013 : considérations d’interopérabilité pour les conférences vidéo.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Interoperability considerations for video conferencing
ms:assetid: 31ead3b5-ed95-42d4-96e2-7d9403d5c026
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204790(v=OCS.15)
ms:contentKeyID: 48183782
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 89675954ea4c4f188f50aab8fb2cb49494bcc247
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426787"
---
# <a name="interoperability-considerations-for-video-conferencing-in-lync-server-2013"></a><span data-ttu-id="e1d08-103">Considérations en matière d’interopérabilité pour les conférences vidéo dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e1d08-103">Interoperability considerations for video conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e1d08-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e1d08-104">

<span> </span></span></span>

<span data-ttu-id="e1d08-105">_**Dernière modification de la rubrique :** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="e1d08-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="e1d08-106">Cette section décrit l’utilisation de l’application par l’utilisateur lors de la phase de coexistence de la migration, en cas d’interopérabilité entre les clients hérités et un pool Lync Server 2013 ou un serveur Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e1d08-106">This section describes the user experience during the coexistence phase of migration, when there is interoperability between legacy clients and a Lync Server 2013 pool or Lync Server 2013 clients and a legacy pool.</span></span>

<div>

## <a name="lync-server-2013-pools"></a><span data-ttu-id="e1d08-107">Pools Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e1d08-107">Lync Server 2013 Pools</span></span>

<span data-ttu-id="e1d08-108">Les utilisateurs peuvent observer le comportement suivant lorsqu’un client hérité est utilisé dans un pool Lync Server 2013 :</span><span class="sxs-lookup"><span data-stu-id="e1d08-108">Users will experience the following behavior when a legacy client is used in a Lync Server 2013 pool:</span></span>

  - <span data-ttu-id="e1d08-109">Pour les appels à deux participants, la résolution vidéo est identique à celle du pool hérité.</span><span class="sxs-lookup"><span data-stu-id="e1d08-109">For two-party calls, video resolution is the same as in the legacy pool.</span></span>

  - <span data-ttu-id="e1d08-110">Dans le cadre de conférences multiparties, les fonctionnalités de résolution vidéo et de visioconférence sont les mêmes que dans le pool hérité.</span><span class="sxs-lookup"><span data-stu-id="e1d08-110">For multiparty conferences, video resolution and video conferencing features are the same as in the legacy pool.</span></span> <span data-ttu-id="e1d08-111">Le mode Galerie et la haute résolution ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="e1d08-111">Gallery View and high resolution are not available.</span></span>

</div>

<div>

## <a name="legacy-pools"></a><span data-ttu-id="e1d08-112">Pools hérités</span><span class="sxs-lookup"><span data-stu-id="e1d08-112">Legacy Pools</span></span>

<span data-ttu-id="e1d08-113">Les utilisateurs peuvent découvrir le comportement suivant lorsqu’un client Lync Server 2013 est utilisé dans un pool hérité :</span><span class="sxs-lookup"><span data-stu-id="e1d08-113">Users will experience the following behavior when a Lync Server 2013 client is used in a legacy pool:</span></span>

  - <span data-ttu-id="e1d08-114">Pour les appels à deux parties, les clients Lync Server 2013 peuvent utiliser les nouvelles fonctionnalités comme suit :</span><span class="sxs-lookup"><span data-stu-id="e1d08-114">For two-party calls, Lync Server 2013 clients can use new features as follows:</span></span>
    
      - <span data-ttu-id="e1d08-115">H. 264 est disponible si les deux participants utilisent les clients Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e1d08-115">H.264 is available if both participants are using Lync Server 2013 clients.</span></span>
    
      - <span data-ttu-id="e1d08-116">Le client Lync Server 2013 utilise la valeur par défaut pour TotalReceiveVideoBitRateKb, car le serveur hérité n’envoie pas ces informations avec la mise en service intrabande.</span><span class="sxs-lookup"><span data-stu-id="e1d08-116">The Lync Server 2013 client uses the default value for TotalReceiveVideoBitRateKb, since the legacy server doesn’t send this information with in-band provisioning.</span></span>

  - <span data-ttu-id="e1d08-117">Dans le cadre de conférences multipièces, les fonctionnalités de résolution vidéo et de visioconférence sont les mêmes que celles d’un client hérité dans le pool hérité.</span><span class="sxs-lookup"><span data-stu-id="e1d08-117">For multiparty conferences, video resolution and video conferencing features are the same as experienced by a legacy client in the legacy pool.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="e1d08-118">Lorsqu’un serveur hérité héberge un client Lync Server 2013, il est possible de configurer une bande passante de conférence vidéo de sorte que tous les utilisateurs du pool reçoivent uniquement de la vidéo basse résolution, mais qu’ils envoient une vidéo haute résolution.</span><span class="sxs-lookup"><span data-stu-id="e1d08-118">When a legacy server hosts a Lync Server 2013 client, it's possible to configure video conferencing bandwidth so that all users on the pool receive only low-resolution video, but send high-resolution video.</span></span> <span data-ttu-id="e1d08-119">C’est le cas, par exemple, lorsque MaxVideoRateAllowed est défini sur CAF-250K dans la configuration multimédia et VideoBitRateKb est défini sur 2000 KB/s dans la stratégie de conférence.</span><span class="sxs-lookup"><span data-stu-id="e1d08-119">An example of this is when MaxVideoRateAllowed is set to CIF-250K in the media configuration and VideoBitRateKb is set to 2000 kbps in conferencing policy.</span></span> <span data-ttu-id="e1d08-120">Dans cette situation, l’effet net n’est pas possible pour les utilisateurs du pool.</span><span class="sxs-lookup"><span data-stu-id="e1d08-120">The net effect in this situation is that high resolution is not possible for users on the pool.</span></span><BR><span data-ttu-id="e1d08-121">Étant donné que MaxVideoRateAllowed n’est plus utilisé pour les clients Lync Server 2013, il n’est pas possible d’empêcher les clients Lync Server 2013 de demander une vidéo haute résolution.</span><span class="sxs-lookup"><span data-stu-id="e1d08-121">Because MaxVideoRateAllowed is no longer used for Lync Server 2013 clients, it cannot prevent Lync Server 2013 clients from requesting high-resolution video.</span></span> <span data-ttu-id="e1d08-122">Au lieu de cela, définissez VideoBitRateKb dans la stratégie de conférence pour que tous les utilisateurs du pool aient la même valeur que MaxVideoRateAllowed (c’est-à-dire que la valeur CAF est définie sur 250 kb/s, 600 ou la valeur HD est définie sur 1500 kb/s).</span><span class="sxs-lookup"><span data-stu-id="e1d08-122">Instead, set VideoBitRateKb in conferencing policy for all users on the pool to the same value as MaxVideoRateAllowed (that is, CIF is set to 250 kbps, or VGA is set to 600 kbps, or HD is set to 1500 kbps).</span></span>



<span data-ttu-id="e1d08-123"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e1d08-123"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

