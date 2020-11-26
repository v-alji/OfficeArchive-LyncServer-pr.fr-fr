---
title: 'Lync Server 2013 : Get-CsAddressBookConfiguration pour la gestion du carnet d’adresses'
description: 'Lync Server 2013 : Get-CsAddressBookConfiguration pour la gestion du carnet d’adresses.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Get-CsAddressBookConfiguration for Address Book management
ms:assetid: bd62f916-caf3-4e10-ada4-631bbb331ef1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429721(v=OCS.15)
ms:contentKeyID: 48185264
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 91b96aead7b7038464f3166691a5952b9ff850dc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427977"
---
# <a name="get-csaddressbookconfiguration-for-address-book-management-in-lync-server-2013"></a><span data-ttu-id="6ef22-103">Get-CsAddressBookConfiguration la gestion du carnet d’adresses dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6ef22-103">Get-CsAddressBookConfiguration for Address Book management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6ef22-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6ef22-104">

<span> </span></span></span>

<span data-ttu-id="6ef22-105">_**Dernière modification de la rubrique :** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="6ef22-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="6ef22-106">Qui peut exécuter cette applet de commande : par défaut, les membres des groupes suivants sont autorisés à exécuter l’applet de commande Get-CsAddressBookConfiguration localement : RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="6ef22-106">Who can run this cmdlet: By default, members of the following groups are authorized to run the Get-CsAddressBookConfiguration cmdlet locally: RTCUniversalServerAdmins.</span></span> <span data-ttu-id="6ef22-107">Pour renvoyer la liste de tous les rôles de contrôle d’accès basés sur des rôles (RBAC) affectés à cette applet de commande (y compris les rôles RBAC personnalisés que vous avez créés vous-même), exécutez la commande suivante à partir de l’invite Windows PowerShell :</span><span class="sxs-lookup"><span data-stu-id="6ef22-107">To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself), run the following command from the Windows PowerShell prompt:</span></span>

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Get-CsAddressBookConfiguration"}

<span data-ttu-id="6ef22-108">L’applet de méthode Get-CsAddressBookConfiguration renvoie des informations sur une configuration qui existe déjà.</span><span class="sxs-lookup"><span data-stu-id="6ef22-108">The cmdlet Get-CsAddressBookConfiguration returns information about a configuration that already exists.</span></span>

<span data-ttu-id="6ef22-109">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="6ef22-109">For example:</span></span>

    Get-CsAddressBookConfiguration -Identity site:Redmond

<span data-ttu-id="6ef22-110">Le regroupement des fonctionnalités d' Get-CsAddressBookConfiguration et de Set-CsAddressBookConfiguration permet à l’administrateur de définir les configurations à modifier, puis d’appliquer les modifications.</span><span class="sxs-lookup"><span data-stu-id="6ef22-110">Combining the functionality of Get-CsAddressBookConfiguration and Set-CsAddressBookConfiguration allows the administrator to define which configurations to modify and then apply the modifications.</span></span> <span data-ttu-id="6ef22-111">Par exemple, l’Association suivante :</span><span class="sxs-lookup"><span data-stu-id="6ef22-111">For example, this combined:</span></span>

    Get-CsAddressBookConfiguration -Filter site:* | Set-CsAddressBookConfiguration -RunTimeOfDay 23:00

<span data-ttu-id="6ef22-112">Renvoie toutes les configurations de tous les sites et applique le RunTimeOfDay de 23:00 heures aux configurations.</span><span class="sxs-lookup"><span data-stu-id="6ef22-112">Returns all configurations in all sites and applies the RunTimeOfDay of 23:00 hours to the configurations.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="6ef22-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6ef22-113">See Also</span></span>


[<span data-ttu-id="6ef22-114">Get-CsAddressBookConfiguration</span><span class="sxs-lookup"><span data-stu-id="6ef22-114">Get-CsAddressBookConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsAddressBookConfiguration)  
  

<span data-ttu-id="6ef22-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6ef22-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

