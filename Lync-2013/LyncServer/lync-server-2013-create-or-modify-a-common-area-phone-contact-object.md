---
title: 'Lync Server 2013 : création ou modification d’un objet de contact pour les téléphones communs'
description: 'Lync Server 2013 : création ou modification d’un objet de contact de téléphone de zone commune.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or modify a common area phone Contact object
ms:assetid: eec33ad1-e4f2-49b2-91d6-d5a9d2e1714b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994083(v=OCS.15)
ms:contentKeyID: 51803995
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: adc5ede23f495a63b2d556b556817d4171a08723
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431840"
---
# <a name="create-or-modify-a-common-area-phone-contact-object-in-lync-server-2013"></a><span data-ttu-id="cf93b-103">Création ou modification d’un objet de contact pour les téléphones communs dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cf93b-103">Create or modify a common area phone Contact object in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cf93b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cf93b-104">

<span> </span></span></span>

<span data-ttu-id="cf93b-105">_**Dernière modification de la rubrique :** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="cf93b-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="cf93b-106">Pour créer des objets de contact de services de domaine Active Directory pour tous vos téléphones de zone commune, utilisez l’applet **de contrôle New-CsCommonAreaPhone** .</span><span class="sxs-lookup"><span data-stu-id="cf93b-106">To create Active Directory Domain Services contact objects for all your common area phones, use the **New-CsCommonAreaPhone** cmdlet.</span></span> <span data-ttu-id="cf93b-107">Cette applet de cmdlet peut créer de nouveaux objets de contact à utiliser avec des téléphones de type zone commune ou associer des objets de contact existants à un nouveau téléphone.</span><span class="sxs-lookup"><span data-stu-id="cf93b-107">This cmdlet can either create new contact objects for use with common area phones, or it can associate existing contact objects with a new common area phone.</span></span> <span data-ttu-id="cf93b-108">Pour modifier les propriétés des objets de contact associés aux téléphones de zone commune, utilisez l’applet de passe **Set-CsCommonAreaPhone** .</span><span class="sxs-lookup"><span data-stu-id="cf93b-108">To modify the properties of the contact objects associated with common area phones, use the **Set-CsCommonAreaPhone** cmdlet.</span></span> <span data-ttu-id="cf93b-109">Les paramètres facultatifs pour **Set-CsCommonAreaPhone** vous permettent de modifier des éléments tels que le nom d’affichage Active Directory du contact ou l’URI (Uniform Resource Identifier) de ligne associé au téléphone, et d’activer et de désactiver le compte à utiliser avec Lync Server.</span><span class="sxs-lookup"><span data-stu-id="cf93b-109">Optional parameters for **Set-CsCommonAreaPhone** enable you to change items, such as the contact’s Active Directory display name or the line Uniform Resource Identifier (URI) associated with the phone, and enable and disable the account for use with Lync Server.</span></span> <span data-ttu-id="cf93b-110">Pour plus d’informations sur les modifications que vous pouvez apporter, voir la section paramètres de [Set-CsCommonAreaPhone](https://docs.microsoft.com/powershell/module/skype/Set-CsCommonAreaPhone).</span><span class="sxs-lookup"><span data-stu-id="cf93b-110">For details about all the available modifications, see the Parameters section at [Set-CsCommonAreaPhone](https://docs.microsoft.com/powershell/module/skype/Set-CsCommonAreaPhone).</span></span> <span data-ttu-id="cf93b-111">Pour plus d’informations sur les paramètres de **New-CsCommonAreaPhone** , voir [New-CsCommonAreaPhone](https://docs.microsoft.com/powershell/module/skype/New-CsCommonAreaPhone).</span><span class="sxs-lookup"><span data-stu-id="cf93b-111">For details about **New-CsCommonAreaPhone** parameters, see [New-CsCommonAreaPhone](https://docs.microsoft.com/powershell/module/skype/New-CsCommonAreaPhone).</span></span>

<span data-ttu-id="cf93b-112">Vous pouvez exécuter ces deux applets de commande à partir de Lync Server 2013 Management Shell ou à partir d’une session distante de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="cf93b-112">You can run these two cmdlets from either the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="cf93b-113">Pour plus d’informations sur l’utilisation de Windows PowerShell distant pour vous connecter à Lync Server, voir l’article de blog Lync Server Windows PowerShell « démarrage rapide : gestion de Microsoft Lync Server 2010 à l’aide de Remote PowerShell » [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="cf93b-113">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>


<div>

## <a name="creating-a-common-area-phone-contact-object"></a><span data-ttu-id="cf93b-114">Création d’un objet de contact pour les téléphones communs</span><span class="sxs-lookup"><span data-stu-id="cf93b-114">Creating a common area phone contact object</span></span>

  - <span data-ttu-id="cf93b-115">Pour créer un objet de contact de téléphone de zone commune, utilisez l’applet **de nouvelle applet de nouveau-CsCommonAreaPhone** .</span><span class="sxs-lookup"><span data-stu-id="cf93b-115">To create a new common area phone contact object, use the **New-CsCommonAreaPhone** cmdlet.</span></span> <span data-ttu-id="cf93b-116">Au minimum, vous devez fournir les informations suivantes lors de la création d’un objet de contact :</span><span class="sxs-lookup"><span data-stu-id="cf93b-116">At a minimum, you must supply the following information when creating a contact object:</span></span>
    
      - <span data-ttu-id="cf93b-117">**LineURI**: numéro de téléphone attribué au numéro de téléphone de la zone commune.</span><span class="sxs-lookup"><span data-stu-id="cf93b-117">**LineUri**: The telephone number assigned to the common area phone.</span></span> <span data-ttu-id="cf93b-118">Notez que vous devez utiliser le format E. 164 lorsque vous spécifiez le numéro de téléphone.</span><span class="sxs-lookup"><span data-stu-id="cf93b-118">Note that you must use the E.164 format when specifying the phone number.</span></span>
    
      - <span data-ttu-id="cf93b-119">**RegistrarPool**: nom de domaine complet (FQDN) du pool d’inscriptions qui hébergera l’objet contact.</span><span class="sxs-lookup"><span data-stu-id="cf93b-119">**RegistrarPool**: The fully qualified domain name (FQDN) of the Registrar pool that will host the contact object.</span></span>
    
      - <span data-ttu-id="cf93b-120">**UO**: nom unique du conteneur Active Directory où l’objet de contact est créé.</span><span class="sxs-lookup"><span data-stu-id="cf93b-120">**OU**: Distinguished name of the Active Directory container where the contact object will be created.</span></span>
    
    <span data-ttu-id="cf93b-121">Nous vous recommandons également de fournir un nom complet des services de domaine Active Directory.</span><span class="sxs-lookup"><span data-stu-id="cf93b-121">We also recommend that you provide an Active Directory Domain Services display name.</span></span> <span data-ttu-id="cf93b-122">Dans le cas contraire, vous devrez utiliser un GUID pour spécifier l’identité du téléphone.</span><span class="sxs-lookup"><span data-stu-id="cf93b-122">Otherwise, you will need to use a GUID to specify the phone Identity.</span></span> <span data-ttu-id="cf93b-123">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="cf93b-123">For example:</span></span>
    
        New-CsCommonAreaPhone -LineUri "tel:+12065551219" -RegistrarPool "atl-cs-001.litwareinc.com" -OU "OU=Phones,dc=litwareinc,dc=com" -DisplayName "Lobby"

</div>

<div>

## <a name="modifying-a-common-area-phone-contact-object"></a><span data-ttu-id="cf93b-124">Modification d’un objet de contact pour les téléphones communs</span><span class="sxs-lookup"><span data-stu-id="cf93b-124">Modifying a common area phone contact object</span></span>

  - <span data-ttu-id="cf93b-125">Pour modifier les propriétés d’un numéro de téléphone commun existant, vous pouvez utiliser l’applet de cmdlet **Set-CsCommonAreaPhone** .</span><span class="sxs-lookup"><span data-stu-id="cf93b-125">To modify the properties of an existing common area phone, contact object use the **Set-CsCommonAreaPhone** cmdlet.</span></span> <span data-ttu-id="cf93b-126">Par exemple, cette commande configure l’adresse SIP pour le numéro de téléphone commun avec le champ DisplayName lobby :</span><span class="sxs-lookup"><span data-stu-id="cf93b-126">For example, this command configures the SIP address for the common area phone with the DisplayName Lobby:</span></span>
    
        Set-CsCommonAreaPhone -Identity "Lobby" -SipAddress "sip:lobby@litwareinc.com"

</div>

<span data-ttu-id="cf93b-127">Pour plus d’informations, consultez les rubriques d’aide pour la cmdlet [New-CsCommonAreaPhone](https://docs.microsoft.com/powershell/module/skype/New-CsCommonAreaPhone) et l’applet de connexion [Set-CsCommonAreaPhone](https://docs.microsoft.com/powershell/module/skype/Set-CsCommonAreaPhone) .</span><span class="sxs-lookup"><span data-stu-id="cf93b-127">For details, see the Help topics for the [New-CsCommonAreaPhone](https://docs.microsoft.com/powershell/module/skype/New-CsCommonAreaPhone) cmdlet and the [Set-CsCommonAreaPhone](https://docs.microsoft.com/powershell/module/skype/Set-CsCommonAreaPhone) cmdlet.</span></span>

<span data-ttu-id="cf93b-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cf93b-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

