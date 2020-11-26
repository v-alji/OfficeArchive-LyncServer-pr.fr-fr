---
title: 'Lync Server 2013 : Ajout des sites de succursale à votre topologie'
description: 'Lync Server 2013 : ajoutez des sites de succursale à votre topologie.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Add branch sites to your topology
ms:assetid: b9c35fb0-0081-4aeb-8f95-ac2fcc6c3335
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412905(v=OCS.15)
ms:contentKeyID: 48185216
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3c7a12373c6a60a2902ee451d39c99f756e2b2f5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439365"
---
# <a name="add-branch-sites-to-your-topology-in-lync-server-2013"></a><span data-ttu-id="50704-103">Ajout des sites de succursale à votre topologie dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="50704-103">Add branch sites to your topology in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="50704-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="50704-104">

<span> </span></span></span>

<span data-ttu-id="50704-105">_**Dernière modification de la rubrique :** 2012-10-05_</span><span class="sxs-lookup"><span data-stu-id="50704-105">_**Topic Last Modified:** 2012-10-05_</span></span>

<span data-ttu-id="50704-106">Les sites de succursales représentent des agences physiques qui sont connectées à vos bureaux principaux par le biais d’une liaison WAN.</span><span class="sxs-lookup"><span data-stu-id="50704-106">Branch sites represent physical branch offices that are connected to your main offices over a WAN link.</span></span> <span data-ttu-id="50704-107">Pour ajouter un site de succursale à votre topologie Lync, procédez comme suit sur le site central.</span><span class="sxs-lookup"><span data-stu-id="50704-107">To add a branch site to your Lync topology, perform this procedure at the central site.</span></span>

<div>

## <a name="to-add-branch-sites-to-your-topology"></a><span data-ttu-id="50704-108">Pour ajouter des sites de succursales à votre topologie</span><span class="sxs-lookup"><span data-stu-id="50704-108">To add branch sites to your topology</span></span>

1.  <span data-ttu-id="50704-109">Cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server**, puis sur **Générateur de topologie de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="50704-109">Click **Start**, click **All Programs**, click **Microsoft Lync Server**, and then click **Lync Server Topology Builder**.</span></span>

2.  <span data-ttu-id="50704-110">Dans l’arborescence de la console, développez le site central, cliquez avec le bouton droit sur **sites de succursales**, puis cliquez sur **nouveau site de succursale**.</span><span class="sxs-lookup"><span data-stu-id="50704-110">In the console tree, expand the central site, right-click **Branch Sites**, and then click **New Branch Site**.</span></span>

3.  <span data-ttu-id="50704-111">Dans la boîte de dialogue **définir un nouveau site de succursale** , cliquez sur **nom**, puis tapez le nom du site de la succursale.</span><span class="sxs-lookup"><span data-stu-id="50704-111">In the **Define New Branch Site** dialog box, click **Name**, and then type the name of the branch site.</span></span>

4.  <span data-ttu-id="50704-112">Facultatif Cliquez sur **Description**, puis tapez une description significative pour le site de la succursale.</span><span class="sxs-lookup"><span data-stu-id="50704-112">(Optional) Click **Description**, and then type a meaningful description for the branch site.</span></span>

5.  <span data-ttu-id="50704-113">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="50704-113">Click **Next**.</span></span>

6.  <span data-ttu-id="50704-114">Facultatif Dans la boîte de dialogue **définir un nouveau site de succursale** suivante, effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="50704-114">(Optional) In the next **Define New Branch Site** dialog box, do any of the following:</span></span>
    
      - <span data-ttu-id="50704-115">Cliquez sur **City**, puis tapez le nom de la ville dans laquelle se trouve le site de la succursale.</span><span class="sxs-lookup"><span data-stu-id="50704-115">Click **City**, and then type the name of the city in which the branch site is located.</span></span>
    
      - <span data-ttu-id="50704-116">Cliquez sur **état/région**, puis tapez le nom de l’État ou de la région où se trouve le site de la succursale.</span><span class="sxs-lookup"><span data-stu-id="50704-116">Click **State/Region**, and then type the name of the state or region in which the branch site is located.</span></span>
    
      - <span data-ttu-id="50704-117">Cliquez sur **indicatif du pays**, puis tapez le code d’appel à deux chiffres correspondant au pays/la région où se trouve le site de la succursale.</span><span class="sxs-lookup"><span data-stu-id="50704-117">Click **Country Code**, and then type the two-digit calling code for the country/region in which the branch site is located.</span></span>

7.  <span data-ttu-id="50704-118">Cliquez sur **suivant**, puis effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="50704-118">Click **Next**, and then do one of the following:</span></span>
    
      - <span data-ttu-id="50704-119">Si vous utilisez un appareil ou un serveur de succursales survivant sur ce site, assurez-vous que la case à cocher **ouvrir le nouvel Assistant survie à la fermeture de cet Assistant** est activée, cliquez sur **Terminer**, puis suivez les instructions de l’Assistant qui s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="50704-119">If you are using a Survivable Branch Appliance or Server at this site, be sure that the **Open the New Survivable Wizard when this wizard closes** check box is selected, click **Finish**, and then follow the directions in the wizard that opens.</span></span> <span data-ttu-id="50704-120">Pour plus d’informations sur les éléments de l’Assistant, voir [définir une unité ou un serveur de succursales survivant dans Lync Server 2013](lync-server-2013-define-a-survivable-branch-appliance-or-server.md).</span><span class="sxs-lookup"><span data-stu-id="50704-120">For information about wizard items, see [Define a Survivable Branch Appliance or Server in Lync Server 2013](lync-server-2013-define-a-survivable-branch-appliance-or-server.md).</span></span>
    
      - <span data-ttu-id="50704-121">Si vous n’utilisez pas d’appareil ou serveur de succursales survivant sur ce site, désactivez la case à cocher **ouvrir le nouvel Assistant survie lorsque cet Assistant se ferme** , puis cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="50704-121">If you are not using a Survivable Branch Appliance or Server at this site, clear the **Open the New Survivable Wizard when this wizard closes** check box, and then click **Finish**.</span></span>

8.  <span data-ttu-id="50704-122">Répétez les étapes précédentes pour chaque site de succursale que vous voulez ajouter à la topologie.</span><span class="sxs-lookup"><span data-stu-id="50704-122">Repeat the previous steps for each branch site that you want to add to the topology.</span></span>

<span data-ttu-id="50704-123">**Étape suivante :**</span><span class="sxs-lookup"><span data-stu-id="50704-123">**Next step:**</span></span>

<span data-ttu-id="50704-124">Pour les appareils ou serveurs de succursales Survivables : [définir une unité ou un serveur de succursale Survivable dans Lync Server 2013](lync-server-2013-define-a-survivable-branch-appliance-or-server.md)</span><span class="sxs-lookup"><span data-stu-id="50704-124">For Survivable Branch Appliances or Servers: [Define a Survivable Branch Appliance or Server in Lync Server 2013](lync-server-2013-define-a-survivable-branch-appliance-or-server.md)</span></span>

<span data-ttu-id="50704-125">Pour la connectivité PSTN non résiliente : [définissez une passerelle PSTN pour un site de succursale dans Lync server 2013](lync-server-2013-define-a-pstn-gateway-for-a-branch-site.md), [configurez un Trunk avec une dérivation multimédia dans Lync Server 2013](lync-server-2013-configure-a-trunk-with-media-bypass.md)ou [configurez un Trunk sans dérivation multimédia dans Lync Server 2013](lync-server-2013-configure-a-trunk-without-media-bypass.md)</span><span class="sxs-lookup"><span data-stu-id="50704-125">For non-resilient PSTN connectivity: [Define a PSTN gateway for a branch site in Lync Server 2013](lync-server-2013-define-a-pstn-gateway-for-a-branch-site.md), [Configure a trunk with media bypass in Lync Server 2013](lync-server-2013-configure-a-trunk-with-media-bypass.md), or [Configure a trunk without media bypass in Lync Server 2013](lync-server-2013-configure-a-trunk-without-media-bypass.md)</span></span>

<span data-ttu-id="50704-126"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="50704-126"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

