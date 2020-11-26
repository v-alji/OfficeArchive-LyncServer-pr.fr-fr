---
title: 'Lync Server 2013 : premières étapes avant de commencer à migrer des utilisateurs de Lync Online vers Lync local'
description: 'Lync Server 2013 : premières étapes avant de commencer à migrer des utilisateurs de Lync Online vers Lync local.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: First steps before you start migrating users from Lync Online to Lync on-premises
ms:assetid: 98245b04-ded4-4186-8da3-ba1c554b5c39
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn689118(v=OCS.15)
ms:contentKeyID: 62258123
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 408820e461c0a9f7c0beaaaae3a502802048d3f5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428117"
---
# <a name="first-steps-before-you-start-migrating-users-from-lync-online-to-lync-on-premises-in-lync-server-2013"></a><span data-ttu-id="fee79-103">Premiers pas avant de commencer à migrer des utilisateurs de Lync Online vers Lync local dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fee79-103">First steps before you start migrating users from Lync Online to Lync on-premises in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fee79-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fee79-104">

<span> </span></span></span>

<span data-ttu-id="fee79-105">_**Dernière modification de la rubrique :** 2014-05-08_</span><span class="sxs-lookup"><span data-stu-id="fee79-105">_**Topic Last Modified:** 2014-05-08_</span></span>

<span data-ttu-id="fee79-106">Avant de commencer à déplacer des utilisateurs de Lync Online vers votre environnement local, assurez-vous que les conditions suivantes sont remplies :</span><span class="sxs-lookup"><span data-stu-id="fee79-106">Before you start moving Lync Online users to your on-premises environment, check that all of the following are true:</span></span>

  - <span data-ttu-id="fee79-107">Votre environnement Lync Server local doit être entièrement déployé et validé.</span><span class="sxs-lookup"><span data-stu-id="fee79-107">Your Lync Server on-premises environment must be fully deployed and validated.</span></span> <span data-ttu-id="fee79-108">Pour plus d’informations, reportez-vous à [déploiement de Lync Server 2013](lync-server-2013-deploying-lync-server.md).</span><span class="sxs-lookup"><span data-stu-id="fee79-108">For more information, see [Deploying Lync Server 2013](lync-server-2013-deploying-lync-server.md).</span></span>

  - <span data-ttu-id="fee79-109">Votre client Lync Online doit être configuré pour l’accès PowerShell à distance.</span><span class="sxs-lookup"><span data-stu-id="fee79-109">Your Lync Online tenant must be configured for remote PowerShell Access.</span></span>
    
    <span data-ttu-id="fee79-110">Pour ce faire, vous devez d’abord installer le module Lync Online pour Windows PowerShell que vous trouverez ici : [https://go.microsoft.com/fwlink/p/?LinkId=391911](https://go.microsoft.com/fwlink/p/?linkid=391911) .</span><span class="sxs-lookup"><span data-stu-id="fee79-110">To do this, first install the Lync Online module for Windows PowerShell, which you can get here: [https://go.microsoft.com/fwlink/p/?LinkId=391911](https://go.microsoft.com/fwlink/p/?linkid=391911).</span></span>
    
    <span data-ttu-id="fee79-111">Après avoir installé le module, vous pouvez établir une session distante en tapant les applets de commande suivantes dans Lync Server Management Shell :</span><span class="sxs-lookup"><span data-stu-id="fee79-111">After you install the module, you can establish a remote session by typing the following cmdlets in the Lync Server Management Shell:</span></span>
    
       ```PowerShell
        Import-Module LyncOnlineConnector
       ```  
    
       ```PowerShell
        $cred = Get-Credential
       ``` 
    
       ```PowerShell
        $CSSession = New-CsOnlineSession -Credential $cred
       ```
    
       ```PowerShell
        Import-PSSession $CSSession -AllowClobber
       ```
    
    <span data-ttu-id="fee79-112">Pour plus d’informations sur l’établissement d’une session PowerShell distante avec Lync Online, voir [connexion à Lync Online à l’aide de Windows PowerShell](https://docs.microsoft.com/SkypeForBusiness/set-up-your-computer-for-windows-powershell/set-up-your-computer-for-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="fee79-112">For more information about how to establish a remote PowerShell session with Lync Online, see [Connecting to Lync Online by using Windows PowerShell](https://docs.microsoft.com/SkypeForBusiness/set-up-your-computer-for-windows-powershell/set-up-your-computer-for-windows-powershell).</span></span>
  
    <span data-ttu-id="fee79-113">Pour plus d’informations sur l’utilisation du module Lync Online PowerShell, reportez-vous à la rubrique [utilisation de Windows PowerShell pour gérer Lync Online](https://docs.microsoft.com/SkypeForBusiness/set-up-your-computer-for-windows-powershell/set-up-your-computer-for-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="fee79-113">For more information about using the Lync Online PowerShell module, see [Using Windows PowerShell to manage Lync Online](https://docs.microsoft.com/SkypeForBusiness/set-up-your-computer-for-windows-powershell/set-up-your-computer-for-windows-powershell).</span></span>

  - <span data-ttu-id="fee79-114">Votre Lync Online doit être configuré pour l’espace d’adressage SIP partagé.</span><span class="sxs-lookup"><span data-stu-id="fee79-114">Your Lync Online must be configured for Shared SIP Address Space.</span></span> <span data-ttu-id="fee79-115">Pour ce faire, commencez par commencer une session PowerShell distante avec Lync Online.</span><span class="sxs-lookup"><span data-stu-id="fee79-115">To do this, first start a remote Powershell session with Lync Online.</span></span> <span data-ttu-id="fee79-116">Ensuite, exécutez l’applet de commande suivante :</span><span class="sxs-lookup"><span data-stu-id="fee79-116">Then run the following cmdlet:</span></span>
    
        Set-CsTenantFederationConfiguration -SharedSipAddressSpace $True

<span data-ttu-id="fee79-117">Une fois ces étapes terminées, vous pouvez passer à la [migration des utilisateurs Lync Online vers Lync local dans Lync Server 2013](lync-server-2013-migrating-lync-online-users-to-lync-on-premises.md).</span><span class="sxs-lookup"><span data-stu-id="fee79-117">After you’ve finished these steps, you can move on to [Migrating Lync Online users to Lync on-premises in Lync Server 2013](lync-server-2013-migrating-lync-online-users-to-lync-on-premises.md).</span></span>

<span data-ttu-id="fee79-118"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fee79-118"></div>

<span> </span>

</div>

</div>

</span></span></div>

