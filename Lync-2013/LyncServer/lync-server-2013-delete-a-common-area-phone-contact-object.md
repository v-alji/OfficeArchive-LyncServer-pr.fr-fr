---
title: 'Lync Server 2013 : supprimer un objet de contact de téléphone de zone commune'
description: 'Lync Server 2013 : supprimer un objet de contact de téléphone pour les zones communes.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete a common area phone Contact object
ms:assetid: f4c139dc-f07c-4c75-9345-e291aea41173
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994087(v=OCS.15)
ms:contentKeyID: 51803999
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e918f7a46269f70577f28b2c3e55297959430721
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395108"
---
# <a name="delete-a-common-area-phone-contact-object-in-lync-server-2013"></a><span data-ttu-id="ff83b-103">Supprimer un objet de contact de téléphone pour les zones communes dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ff83b-103">Delete a common area phone Contact object in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ff83b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ff83b-104">

<span> </span></span></span>

<span data-ttu-id="ff83b-105">_**Dernière modification de la rubrique :** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="ff83b-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="ff83b-106">Vous souhaiterez peut-être supprimer l’objet contact associé à un téléphone de zone commune.</span><span class="sxs-lookup"><span data-stu-id="ff83b-106">You might want to delete the contact object associated with a common area phone.</span></span> <span data-ttu-id="ff83b-107">Par exemple, si vous supprimez le téléphone d’une salon d’employé, il est inutile d’avoir un objet de contact associé à ce téléphone.</span><span class="sxs-lookup"><span data-stu-id="ff83b-107">For example, if you remove the phone from an employee lounge, there’s no need to have a contact object associated with that phone.</span></span> <span data-ttu-id="ff83b-108">L’applet de passe **Remove-CsCommonAreaPhone** vous permet de supprimer les comptes de téléphone de zone commune.</span><span class="sxs-lookup"><span data-stu-id="ff83b-108">The **Remove-CsCommonAreaPhone** cmdlet provides a way for you to delete common area phone accounts.</span></span> <span data-ttu-id="ff83b-109">Lorsque vous exécutez cette cmdlet, le téléphone est supprimé de la liste des téléphones communs renvoyés par **Get-CsCommonAreaPhone**.</span><span class="sxs-lookup"><span data-stu-id="ff83b-109">When you run this cmdlet, the phone is deleted from the list of common area phones returned by **Get-CsCommonAreaPhone**.</span></span> <span data-ttu-id="ff83b-110">Par ailleurs, l’objet contact associé à ce téléphone est supprimé des services de domaine Active Directory (AD FS).</span><span class="sxs-lookup"><span data-stu-id="ff83b-110">In addition, the contact object associated with that phone is deleted from Active Directory Domain Services.</span></span>

<span data-ttu-id="ff83b-111">Utilisez **Remove-CsCommonAreaPhone** pour supprimer un téléphone standard ou tous les téléphones communs qui possèdent un élément commun, comme un nom d’affichage ou un indicatif de pays ou de région.</span><span class="sxs-lookup"><span data-stu-id="ff83b-111">Use **Remove-CsCommonAreaPhone** to remove one common area phone or all common area phones that have a common element, such as a display name or country and area code.</span></span> <span data-ttu-id="ff83b-112">Vous pouvez exécuter cette applet de commande à partir de Lync Server 2013 Management Shell ou d’une session distante de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ff83b-112">You can run this cmdlet from either the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="ff83b-113">Pour plus d’informations sur l’utilisation de Windows PowerShell distant pour vous connecter à Lync Server, voir l’article de blog Lync Server Windows PowerShell « démarrage rapide : gestion de Microsoft Lync Server 2010 à l’aide de Remote PowerShell » [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="ff83b-113">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>


<div>

## <a name="removing-a-specified-common-area-phone"></a><span data-ttu-id="ff83b-114">Suppression d’un téléphone commun spécifié</span><span class="sxs-lookup"><span data-stu-id="ff83b-114">Removing a Specified Common Area Phone</span></span>

  - <span data-ttu-id="ff83b-115">La commande suivante permet de supprimer le téléphone de zone commune avec l’adresse SIP sip :mainlobby@litwareinc.com :</span><span class="sxs-lookup"><span data-stu-id="ff83b-115">The following command removes the common area phone with the SIP address sip:mainlobby@litwareinc.com:</span></span>
    
        Remove-CsCommonAreaPhone -Identity "sip:mainlobby@litwareinc.com"

</div>

<div>

## <a name="removing-common-area-phones-based-on-their-display-name"></a><span data-ttu-id="ff83b-116">Suppression de téléphones communs en fonction de leur nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="ff83b-116">Removing Common Area Phones Based on Their Display Name</span></span>

  - <span data-ttu-id="ff83b-117">Cette commande supprime tous les téléphones de surface courants dans lesquels le nom d’affichage inclut la valeur de chaîne « bâtiment 14 » :</span><span class="sxs-lookup"><span data-stu-id="ff83b-117">This command removes all the common area phones where the display name includes the string value "Building 14":</span></span>
    
        Get-CsCommonAreaPhone | Where-Object {$_.DisplayName -match "Building 14"} | Remove-CsCommonAreaPhone

</div>

<div>

## <a name="removing-common-area-phones-based-on-their-country-and-area-codes"></a><span data-ttu-id="ff83b-118">Supprimer des téléphones communs en fonction de leur indicatif national et de leur région</span><span class="sxs-lookup"><span data-stu-id="ff83b-118">Removing Common Area Phones Based on Their Country and Area Codes</span></span>

  - <span data-ttu-id="ff83b-119">Cette commande supprime tous les téléphones de surface commune pour les États-Unis (code pays 1) et l’indicatif régional 425 :</span><span class="sxs-lookup"><span data-stu-id="ff83b-119">This command removes all the common area phones for the United States (country code 1) and the area code 425:</span></span>
    
        Get-CsCommonAreaPhone | Where-Object {$_.LineUri  -match "^tel:\+1425"} | Remove-CsCommonAreaPhone

</div>

<span data-ttu-id="ff83b-120">Pour plus d’informations, consultez la rubrique d’aide relative à l’applet de connexion [Remove-CsCommonAreaPhone](https://docs.microsoft.com/powershell/module/skype/Remove-CsCommonAreaPhone) .</span><span class="sxs-lookup"><span data-stu-id="ff83b-120">For details, see the Help topic for the [Remove-CsCommonAreaPhone](https://docs.microsoft.com/powershell/module/skype/Remove-CsCommonAreaPhone) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="ff83b-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ff83b-121">See Also</span></span>


[<span data-ttu-id="ff83b-122">Get-CsCommonAreaPhone</span><span class="sxs-lookup"><span data-stu-id="ff83b-122">Get-CsCommonAreaPhone</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsCommonAreaPhone)  
  

<span data-ttu-id="ff83b-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ff83b-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

