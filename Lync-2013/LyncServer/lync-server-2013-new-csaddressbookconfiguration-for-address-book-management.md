---
title: 'Lync Server 2013 : New-CsAddressBookConfiguration pour la gestion du carnet d’adresses'
description: 'Lync Server 2013 : New-CsAddressBookConfiguration pour la gestion du carnet d’adresses.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: New-CsAddressBookConfiguration for Address Book management
ms:assetid: a58ddc8c-ae04-4141-b69e-e45374a67d72
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429718(v=OCS.15)
ms:contentKeyID: 48184985
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c85d85fefe701456ad253f1afc69b73093b30996
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445448"
---
# <a name="new-csaddressbookconfiguration-for-address-book-management-in-lync-server-2013"></a><span data-ttu-id="87492-103">New-CsAddressBookConfiguration la gestion du carnet d’adresses dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="87492-103">New-CsAddressBookConfiguration for Address Book management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="87492-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="87492-104">

<span> </span></span></span>

<span data-ttu-id="87492-105">_**Dernière modification de la rubrique :** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="87492-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="87492-106">Qui peut exécuter cette applet de commande : par défaut, les membres des groupes suivants sont autorisés à exécuter l’applet de commande New-CsAddressBookConfiguration localement : RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="87492-106">Who can run this cmdlet: By default, members of the following groups are authorized to run the New-CsAddressBookConfiguration cmdlet locally: RTCUniversalServerAdmins.</span></span> <span data-ttu-id="87492-107">Pour renvoyer la liste de tous les rôles de contrôle d’accès basés sur des rôles (RBAC) affectés à cette applet de commande (y compris les rôles RBAC personnalisés que vous avez créés vous-même), exécutez la commande suivante à partir de l’invite Windows PowerShell :</span><span class="sxs-lookup"><span data-stu-id="87492-107">To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself), run the following command from the Windows PowerShell prompt:</span></span>

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "New-CsAddressBookConfiguration"}

<span data-ttu-id="87492-108">L’applet de l’applet de New-CsAddressBookConfiguration crée une nouvelle configuration pour gérer le comportement du carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="87492-108">The New-CsAddressBookConfiguration cmdlet creates a new configuration to manage the behavior of the Address book.</span></span> <span data-ttu-id="87492-109">Spécifiques à cette applet de commande permet de définir si le service de carnet d’adresses crée les fichiers de téléchargement du client, la façon dont les règles de normalisation sont utilisées et la durée de conservation des fichiers delta et compacts avant l’incorporation d’une nouvelle création de fichier complète, de l’heure de la création du carnet d’adresses de fichiers complets et de la synchronisation des informations dans la base de données utilisateur</span><span class="sxs-lookup"><span data-stu-id="87492-109">Specific to this cmdlet is the ability to define if the Address Book Service creates the client download files, how and if normalization rules are used, how long to retain delta and compact delta files, delta file size before incorporating a new full file creation, what time of day the full file Address Book is created, and what the internal should be for synchronization of information in the User database.</span></span>

<span data-ttu-id="87492-110">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="87492-110">For example:</span></span>

    New-CsAddressBookConfiguration -Identity site:Redmond -KeepDuration 15 -SynchronizePollingInterval 00:10:00

<div>

## <a name="see-also"></a><span data-ttu-id="87492-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="87492-111">See Also</span></span>


[<span data-ttu-id="87492-112">Nouveau-CsAddressBookConfiguration</span><span class="sxs-lookup"><span data-stu-id="87492-112">New-CsAddressBookConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsAddressBookConfiguration)  
  

<span data-ttu-id="87492-113"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="87492-113"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

