---
title: 'Lync Server 2013 : Get-CsWebServiceConfiguration pour la gestion du carnet d’adresses'
description: 'Lync Server 2013 : Get-CsWebServiceConfiguration pour la gestion du carnet d’adresses.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Get-CsWebServiceConfiguration for Address Book management
ms:assetid: 0b223733-5224-47d1-9b47-2109e6f135c9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429692(v=OCS.15)
ms:contentKeyID: 48183372
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bb22d7607f9ac18cda9c8653374ae86839b033e0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427942"
---
# <a name="get-cswebserviceconfiguration-for-address-book-management-in-lync-server-2013"></a><span data-ttu-id="95234-103">Get-CsWebServiceConfiguration la gestion du carnet d’adresses dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="95234-103">Get-CsWebServiceConfiguration for Address Book management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="95234-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="95234-104">

<span> </span></span></span>

<span data-ttu-id="95234-105">_**Dernière modification de la rubrique :** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="95234-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="95234-106">Qui peut exécuter cette applet de commande : par défaut, les membres des groupes suivants sont autorisés à exécuter l’applet de commande Get-CsWebServiceConfiguration localement : RTCUniversalUserAdmins, RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="95234-106">Who can run this cmdlet: By default, members of the following groups are authorized to run the Get-CsWebServiceConfiguration cmdlet locally: RTCUniversalUserAdmins, RTCUniversalServerAdmins.</span></span> <span data-ttu-id="95234-107">Pour renvoyer la liste de tous les rôles de contrôle d’accès basés sur des rôles (RBAC) affectés à cette applet de commande (y compris les rôles RBAC personnalisés que vous avez créés vous-même), exécutez la commande suivante à partir de l’invite Windows PowerShell :</span><span class="sxs-lookup"><span data-stu-id="95234-107">To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself), run the following command from the Windows PowerShell prompt:</span></span>

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Get-CsWebServiceConfiguration"}

<span data-ttu-id="95234-108">Get-CsWebServiceConfiguration renvoie des informations sur la configuration des services Web actuellement utilisée au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="95234-108">Get-CsWebServiceConfiguration returns information of the Web Services configuration currently in use in your organization.</span></span> <span data-ttu-id="95234-109">Le statut de la fonction d’extension de liste de distribution est particulièrement utile pour les services du carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="95234-109">Of interest to the Address Book Services is the status of Distribution List Expansion function.</span></span> <span data-ttu-id="95234-110">Si l’attribut EnableGroupExpansion est vrai, votre organisation autorise actuellement l’extension du groupe.</span><span class="sxs-lookup"><span data-stu-id="95234-110">If the attribute EnableGroupExpansion is True, your organization currently allows group expansion.</span></span>

<span data-ttu-id="95234-111">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="95234-111">For example:</span></span>

    Get-CsWebServiceConfiguration -Identity site:Redmond

<div>

## <a name="see-also"></a><span data-ttu-id="95234-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="95234-112">See Also</span></span>


[<span data-ttu-id="95234-113">Get-CsWebServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="95234-113">Get-CsWebServiceConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsWebServiceConfiguration)  
  

<span data-ttu-id="95234-114"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="95234-114"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

