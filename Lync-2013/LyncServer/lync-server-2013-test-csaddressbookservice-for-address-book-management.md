---
title: 'Lync Server 2013 : Test-CsAddressBookService pour la gestion du carnet d’adresses'
description: 'Lync Server 2013 : Test-CsAddressBookService pour la gestion du carnet d’adresses.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test-CsAddressBookService for Address Book management
ms:assetid: b88cea74-41fd-4c0e-9284-7135bff27a27
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429720(v=OCS.15)
ms:contentKeyID: 48185206
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 345886c68c814534fcbfd4debfd3be8562fae5a2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444279"
---
# <a name="test-csaddressbookservice-for-address-book-management-in-lync-server-2013"></a><span data-ttu-id="cba49-103">Test-CsAddressBookService la gestion du carnet d’adresses dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cba49-103">Test-CsAddressBookService for Address Book management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cba49-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cba49-104">

<span> </span></span></span>

<span data-ttu-id="cba49-105">_**Dernière modification de la rubrique :** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="cba49-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="cba49-106">Qui peut exécuter cette applet de commande : par défaut, les membres des groupes suivants sont autorisés à exécuter l’applet de commande Test-CsAddressBookService : RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="cba49-106">Who can run this cmdlet: By default, members of the following groups are authorized to run the Test-CsAddressBookService cmdlet: RTCUniversalServerAdmins.</span></span> <span data-ttu-id="cba49-107">Pour renvoyer la liste de tous les rôles de contrôle d’accès basés sur des rôles (RBAC) affectés à cette applet de commande (y compris les rôles RBAC personnalisés que vous avez créés vous-même), exécutez la commande suivante à partir de l’invite Windows PowerShell :</span><span class="sxs-lookup"><span data-stu-id="cba49-107">To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself), run the following command from the Windows PowerShell prompt:</span></span>

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Test-CsAddressBookService"}

<span data-ttu-id="cba49-108">Lync Server 2013 contient un nombre d’applets de commande qui initialisent des commandes de synthèse pour vérifier qu’une fonction ou une fonctionnalité spécifique fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="cba49-108">Lync Server 2013 contains a number of cmdlets that initiate synthetic commands to confirm that a specific function or feature is working properly.</span></span> <span data-ttu-id="cba49-109">Test-CsAddressBookService confirme qu’un utilisateur défini peut communiquer et demander les fichiers locaux à partir du service Web du carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="cba49-109">Test-CsAddressBookService confirms that a defined user can connect and request the local files from the Address Book Web service.</span></span>

<span data-ttu-id="cba49-110">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="cba49-110">For example:</span></span>

    Test-CsAddressBookService -TargetFqdn atl-cs-001.contoso.com -UserCredential contoso\bob -UserSipAddress "sip:bob@contoso.com"

<div>

## <a name="see-also"></a><span data-ttu-id="cba49-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cba49-111">See Also</span></span>


[<span data-ttu-id="cba49-112">Test-CsAddressBookService</span><span class="sxs-lookup"><span data-stu-id="cba49-112">Test-CsAddressBookService</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsAddressBookService)  
  

<span data-ttu-id="cba49-113"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cba49-113"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

