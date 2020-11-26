---
title: 'Lync Server 2013 : Préparation de l’environnement pour VDI'
description: 'Lync Server 2013 : préparation de votre environnement pour VDI.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Preparing your environment for VDI
ms:assetid: a3ec2e13-1a73-4b1c-a54a-8db7d4cd50f9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205154(v=OCS.15)
ms:contentKeyID: 48185052
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e90b9e0f09d3082a28406f1a1dc715285ee4d7e3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424085"
---
# <a name="preparing-your-lync-server-2013-environment-for-vdi"></a><span data-ttu-id="daa79-103">Préparation de l’environnement Lync Server 2013 pour VDI</span><span class="sxs-lookup"><span data-stu-id="daa79-103">Preparing your Lync Server 2013 environment for VDI</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="daa79-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="daa79-104">

<span> </span></span></span>

<span data-ttu-id="daa79-105">_**Dernière modification de la rubrique :** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="daa79-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="daa79-106">Pour préparer l’environnement pour le plug-in Lync VDI, l’administrateur doit procéder comme suit.</span><span class="sxs-lookup"><span data-stu-id="daa79-106">To prepare the environment for the Lync VDI plug-in, the administrator must perform the following steps.</span></span>

1.  <span data-ttu-id="daa79-107">Dans Lync Server 2013, assurez-vous que EnableMediaRedirection est défini sur TRUE pour tous les utilisateurs de VDI.</span><span class="sxs-lookup"><span data-stu-id="daa79-107">In Lync Server 2013, ensure that EnableMediaRedirection is set to TRUE for all VDI users.</span></span> <span data-ttu-id="daa79-108">Pour plus d’informations, consultez les rubriques d’aide pour la cmdlet [New-CsClientPolicy](https://docs.microsoft.com/powershell/module/skype/New-CsClientPolicy) et l’applet de connexion [Set-CsClientPolicy](https://docs.microsoft.com/powershell/module/skype/Set-CsClientPolicy) .</span><span class="sxs-lookup"><span data-stu-id="daa79-108">For details, see the Help topics for the [New-CsClientPolicy](https://docs.microsoft.com/powershell/module/skype/New-CsClientPolicy) cmdlet and the [Set-CsClientPolicy](https://docs.microsoft.com/powershell/module/skype/Set-CsClientPolicy) cmdlet.</span></span>

2.  <span data-ttu-id="daa79-109">Sur l’ordinateur du centre de données, installez le client 2013 Lync sur toutes les machines virtuelles.</span><span class="sxs-lookup"><span data-stu-id="daa79-109">On the data center computer, install the Lync 2013 client on all virtual machines.</span></span>

3.  <span data-ttu-id="daa79-110">Sur l’ordinateur local, installez le plug-in Lync VDI.</span><span class="sxs-lookup"><span data-stu-id="daa79-110">On the local computers, install the Lync VDI plug-in.</span></span>

<span data-ttu-id="daa79-111"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="daa79-111"></div>

<span> </span>

</div>

</div>

</span></span></div>

