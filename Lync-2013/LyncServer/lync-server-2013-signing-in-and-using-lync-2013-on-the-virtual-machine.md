---
title: Connexion à Lync 2013 et utilisation sur l’ordinateur virtuel
description: 'Lync Server 2013 : connexion et utilisation de Lync 2013 sur l’ordinateur virtuel.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Signing in and using Lync 2013 on the virtual machine
ms:assetid: 6140fc19-5bef-4b58-9b0f-19112b5ecd00
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204948(v=OCS.15)
ms:contentKeyID: 48184318
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ad9a92d450fb9d60aed70617089d95280528892f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444694"
---
# <a name="signing-in-and-using-lync-2013-on-the-virtual-machine"></a><span data-ttu-id="f878a-103">Connexion à Lync 2013 et utilisation sur l’ordinateur virtuel</span><span class="sxs-lookup"><span data-stu-id="f878a-103">Signing in and using Lync 2013 on the virtual machine</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f878a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f878a-104">

<span> </span></span></span>

<span data-ttu-id="f878a-105">_**Dernière modification de la rubrique :** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="f878a-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="f878a-106">Une fois que le plug-in VDI est activé, les étapes suivantes se produisent lorsque l’utilisateur se connecte à Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="f878a-106">After the VDI plug-in is enabled, the following steps occur when the user signs in to Lync 2013.</span></span>

1.  <span data-ttu-id="f878a-107">L’utilisateur tape ses informations d’identification dans le client 2013 Lync exécuté sur l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="f878a-107">The user types his or her credentials in to the Lync 2013 client running on the virtual machine.</span></span>

2.  <span data-ttu-id="f878a-108">Après que Lync a détecté la disponibilité du plug-in VDI, Lync invite l’utilisateur à entrer à nouveau ses informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="f878a-108">After Lync detects the availability of the VDI plug-in, Lync prompts the user to re-enter his or her credentials.</span></span> <span data-ttu-id="f878a-109">Dans cette boîte de dialogue, nous recommandons à l’utilisateur d’activer la case à cocher **Enregistrer mon mot de passe** afin qu’il n’ait pas à les entrer de nouveau lors de connexions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="f878a-109">In this dialog box, we recommend that the user select the **Save my password** check box so that he or she will not be required to enter credentials during subsequent sign in.</span></span>

3.  <span data-ttu-id="f878a-110">Lync entame le jumelage avec le plug-in VDI.</span><span class="sxs-lookup"><span data-stu-id="f878a-110">Lync begins pairing with the VDI plug-in.</span></span> <span data-ttu-id="f878a-111">Avant de procéder à un jumelage, le client affiche deux icônes dans la barre d’État Lync.</span><span class="sxs-lookup"><span data-stu-id="f878a-111">Before pairing is complete, the client displays two icons in the Lync status bar.</span></span> <span data-ttu-id="f878a-112">L’icône située dans le coin inférieur gauche indique qu’aucun périphérique audio n’est disponible et que l’icône clignotant dans le coin inférieur droit indique que le jumelage VDI est en cours, comme illustré ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="f878a-112">The icon in the lower left indicates that no audio devices are available, and the blinking icon in the lower right indicates that the VDI pairing is in progress, as shown:</span></span>
    
    <span data-ttu-id="f878a-113">![Icône VDI de Lync montrant une jumelage réussie](images/JJ204948.303d618c-4bc8-41c4-8553-2475de0d395e(OCS.15).png "Icône VDI de Lync montrant une jumelage réussie")</span><span class="sxs-lookup"><span data-stu-id="f878a-113">![Lync VDI icon showing successful pairing](images/JJ204948.303d618c-4bc8-41c4-8553-2475de0d395e(OCS.15).png "Lync VDI icon showing successful pairing")</span></span>  

4.  <span data-ttu-id="f878a-114">Une fois le jumelage VDI réussi, les icônes changent pour indiquer le périphérique audio qui sera utilisé pour les appels et la réussite du jumelage VDI :</span><span class="sxs-lookup"><span data-stu-id="f878a-114">After VDI pairing is successful, the icons change to indicate the audio device that will be used for calls and the VDI pairing success:</span></span>
    
    <span data-ttu-id="f878a-115">![Icône d’appariement VDI de Lync indiquant le succès](images/JJ204948.57be3387-a3e5-4949-831e-f5ff9fcc5598(OCS.15).png "Icône d’appariement VDI de Lync indiquant le succès")</span><span class="sxs-lookup"><span data-stu-id="f878a-115">![Lync VDI pairing icon showing success](images/JJ204948.57be3387-a3e5-4949-831e-f5ff9fcc5598(OCS.15).png "Lync VDI pairing icon showing success")</span></span>  

5.  <span data-ttu-id="f878a-116">Après paires Lync avec le plug-in VDI, l’utilisateur peut voir son statut de connexion sur les appareils compatibles Lync qui sont connectés à l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="f878a-116">After Lync pairs with the VDI plug-in, the user can see his or her presence on Lync compatible devices that are connected to the local computer.</span></span> <span data-ttu-id="f878a-117">L’utilisateur peut désormais passer et répondre aux appels comme d’habitude.</span><span class="sxs-lookup"><span data-stu-id="f878a-117">The user can now place and answer calls as usual.</span></span>

<span data-ttu-id="f878a-118"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f878a-118"></div>

<span> </span>

</div>

</div>

</span></span></div>

