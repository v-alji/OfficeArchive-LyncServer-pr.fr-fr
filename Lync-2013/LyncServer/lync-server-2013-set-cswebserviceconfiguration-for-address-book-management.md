---
title: 'Lync Server 2013 : Set-CsWebServiceConfiguration pour la gestion du carnet d’adresses'
description: 'Lync Server 2013 : Set-CsWebServiceConfiguration pour la gestion du carnet d’adresses.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Set-CsWebServiceConfiguration for Address Book management
ms:assetid: 79d0edf5-23f3-4845-a7b7-e11b5a928bab
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429709(v=OCS.15)
ms:contentKeyID: 48184572
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 37dcd7676829c5a91e05667fa0ae0d74dc6f7dc1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423996"
---
# <a name="set-cswebserviceconfiguration-for-address-book-management-in-lync-server-2013"></a><span data-ttu-id="1c5eb-103">Set-CsWebServiceConfiguration la gestion du carnet d’adresses dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1c5eb-103">Set-CsWebServiceConfiguration for Address Book management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1c5eb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1c5eb-104">

<span> </span></span></span>

<span data-ttu-id="1c5eb-105">_**Dernière modification de la rubrique :** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="1c5eb-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="1c5eb-106">Qui peut exécuter cette applet de commande : par défaut, les membres des groupes suivants sont autorisés à exécuter l’applet de commande Set-CsWebServiceConfiguration localement : RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="1c5eb-106">Who can run this cmdlet: By default, members of the following groups are authorized to run the Set-CsWebServiceConfiguration cmdlet locally: RTCUniversalServerAdmins.</span></span> <span data-ttu-id="1c5eb-107">Pour renvoyer la liste de tous les rôles de contrôle d’accès basés sur des rôles (RBAC) affectés à cette applet de commande (y compris les rôles RBAC personnalisés que vous avez créés vous-même), exécutez la commande suivante à partir de l’invite Windows PowerShell :</span><span class="sxs-lookup"><span data-stu-id="1c5eb-107">To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself), run the following command from the Windows PowerShell prompt:</span></span>

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Set-CsWebServiceConfiguration"}

<span data-ttu-id="1c5eb-108">L’applet de l’applet de Set-CsWebServiceConfiguration permet à l’administrateur de redéfinir un attribut existant dans la configuration des services Web.</span><span class="sxs-lookup"><span data-stu-id="1c5eb-108">The Set-CsWebServiceConfiguration cmdlet allows the administrator to redefine an existing attribute in the configuration of the Web Services.</span></span>

<span data-ttu-id="1c5eb-109">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="1c5eb-109">For example:</span></span>

    Set-CsWebServiceConfiguration -Identity site:Redmond -EnableGroupExpansion $True

<div>

## <a name="see-also"></a><span data-ttu-id="1c5eb-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1c5eb-110">See Also</span></span>


[<span data-ttu-id="1c5eb-111">Set-CsWebServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="1c5eb-111">Set-CsWebServiceConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsWebServiceConfiguration)  
  

<span data-ttu-id="1c5eb-112"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1c5eb-112"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

