---
title: 'Lync Server 2013 : Update-CsAddressBook pour la gestion du carnet d’adresses'
description: 'Lync Server 2013 : Update-CsAddressBook pour la gestion du carnet d’adresses.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Update-CsAddressBook for Address Book management
ms:assetid: 0ffd2ef8-201c-44aa-8c64-1c7b0eaa7d48
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429695(v=OCS.15)
ms:contentKeyID: 48183428
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4adc7f94e2f31f64f6517b8cdf9bbcb0649f6c8b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394845"
---
# <a name="update-csaddressbook-for-address-book-management-in-lync-server-2013"></a><span data-ttu-id="19cf6-103">Update-CsAddressBook la gestion du carnet d’adresses dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="19cf6-103">Update-CsAddressBook for Address Book management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="19cf6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="19cf6-104">

<span> </span></span></span>

<span data-ttu-id="19cf6-105">_**Dernière modification de la rubrique :** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="19cf6-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="19cf6-106">Qui peut exécuter cette applet de commande : par défaut, les membres des groupes suivants sont autorisés à exécuter l’applet de commande Update-CsAddressBook localement : RTCUniversalUserAdmins, RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="19cf6-106">Who can run this cmdlet: By default, members of the following groups are authorized to run the Update-CsAddressBook cmdlet locally: RTCUniversalUserAdmins, RTCUniversalServerAdmins.</span></span> <span data-ttu-id="19cf6-107">Pour renvoyer la liste de tous les rôles de contrôle d’accès basés sur des rôles (RBAC) affectés à cette applet de commande (y compris les rôles RBAC personnalisés que vous avez créés vous-même), exécutez la commande suivante à partir de l’invite Windows PowerShell :</span><span class="sxs-lookup"><span data-stu-id="19cf6-107">To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself), run the following command from the Windows PowerShell prompt:</span></span>

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Update-CsAddressBook"}

<span data-ttu-id="19cf6-108">L’applet de commande Update-CsAddressBook remplace la commande **abserver.exe-syncNow** d’Office Communications Server.</span><span class="sxs-lookup"><span data-stu-id="19cf6-108">The Update-CsAddressBook cmdlet replaces the **abserver.exe –syncNow** command from Office Communications Server.</span></span> <span data-ttu-id="19cf6-109">L’objectif de l’applet de connexion consiste à lancer une synchronisation immédiatement au lieu d’attendre la fin prévue.</span><span class="sxs-lookup"><span data-stu-id="19cf6-109">The cmdlet’s purpose is to initiate a synchronization immediately rather than waiting for the scheduled time.</span></span> <span data-ttu-id="19cf6-110">Le premier exemple de commande met à jour tous les carnets d’adresses au sein de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="19cf6-110">The first example command updates all Address Books in the organization.</span></span> <span data-ttu-id="19cf6-111">Le second met à jour uniquement le carnet d’adresses associé au serveur défini.</span><span class="sxs-lookup"><span data-stu-id="19cf6-111">The second updates only the Address Book associated with the defined server.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="19cf6-112">Dans Lync Server 2013, le réplicateur d’utilisateurs de Lync Server capte les modifications d’Active Directory et met à jour la base de données utilisateur de Lync Server en fonction d’un intervalle configuré.</span><span class="sxs-lookup"><span data-stu-id="19cf6-112">In Lync Server 2013, Lync Server User Replicator will pick up the changes from Active Directory and update the Lync Server user database based on a configured interval.</span></span> <span data-ttu-id="19cf6-113">Le réplicateur d’utilisateurs de Lync Server propage également les modifications apportées à la base de données RTCab sans qu’il soit nécessaire d’exécuter Update-CSAddressBook.</span><span class="sxs-lookup"><span data-stu-id="19cf6-113">Lync Server User Replicator will also propagate the changes to the RTCab database quickly without the administrator having to run Update-CSAddressBook.</span></span> <span data-ttu-id="19cf6-114">Les administrateurs devront uniquement exécuter Update-CSAddressBook si le téléchargement du fichier du carnet d’adresses est activé.</span><span class="sxs-lookup"><span data-stu-id="19cf6-114">Administrators will only need to run Update -CSAddressBook if the Address Book file download is enabled.</span></span>



</div>

<span data-ttu-id="19cf6-115">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="19cf6-115">For example:</span></span>

   ```PowerShell
    Update-CsAddressBook
   ```

   ```PowerShell
    Update-CsAddressBook -Fqdn atl-abs-001.contoso.com
   ```

<div>

## <a name="see-also"></a><span data-ttu-id="19cf6-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="19cf6-116">See Also</span></span>


[<span data-ttu-id="19cf6-117">Update-CsAddressBook</span><span class="sxs-lookup"><span data-stu-id="19cf6-117">Update-CsAddressBook</span></span>](https://docs.microsoft.com/powershell/module/skype/Update-CsAddressBook)  
  

<span data-ttu-id="19cf6-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="19cf6-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

