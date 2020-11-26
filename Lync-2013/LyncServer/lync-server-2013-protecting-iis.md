---
title: 'Lync Server 2013 : protection des services Internet (IIS)'
description: 'Lync Server 2013 : protection des services Internet (IIS).'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Protecting IIS in Lync Server 2013
ms:assetid: a67171a6-6703-4e09-abb3-35d335bb674e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn518332(v=OCS.15)
ms:contentKeyID: 62625492
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 51161f221c7235aad04850fdccc5d5e9db5cb579
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436838"
---
# <a name="protecting-iis-in-lync-server-2013"></a><span data-ttu-id="3a27b-103">Protection des services Internet (IIS) dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3a27b-103">Protecting IIS in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3a27b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3a27b-104">

<span> </span></span></span>

<span data-ttu-id="3a27b-105">_**Dernière modification de la rubrique :** 2013-12-05_</span><span class="sxs-lookup"><span data-stu-id="3a27b-105">_**Topic Last Modified:** 2013-12-05_</span></span>

<span data-ttu-id="3a27b-106">Dans Microsoft Office Communications Server 2007 et Microsoft Office Communications Server 2007 R2, Internet Information Services (IIS) s’exécutait sous un compte d’utilisateur standard.</span><span class="sxs-lookup"><span data-stu-id="3a27b-106">In Microsoft Office Communications Server 2007 and Microsoft Office Communications Server 2007 R2, Internet Information Services (IIS) ran under a standard user account.</span></span> <span data-ttu-id="3a27b-107">Cela pouvait entraîner un problème : si ce mot de passe est arrivé à expiration, il est possible que vous deviez nous faire perdre vos services Web.</span><span class="sxs-lookup"><span data-stu-id="3a27b-107">This had the potential to cause issues: if that password expired you could lose your Web Services, an issue that was often difficult to diagnose.</span></span> <span data-ttu-id="3a27b-108">Pour vous aider à éviter le problème d’expiration des mots de passe, Microsoft Lync Server 2013 vous permet de créer un compte d’ordinateur (pour un ordinateur qui n’existe pas réellement) qui peut faire office d’identité d’authentification pour tous les ordinateurs d’un site exécutant IIS.</span><span class="sxs-lookup"><span data-stu-id="3a27b-108">To help avoid the issue of expiring passwords, Microsoft Lync Server 2013 enables you to create a computer account (for a computer that doesn’t actually exist) that can serve as the authentication principal for all the computers in a site that are running IIS.</span></span> <span data-ttu-id="3a27b-109">Étant donné que ces comptes utilisent le protocole d’authentification Kerberos, les comptes sont désignés sous le nom de comptes Kerberos et le nouveau processus d’authentification est connu sous le nom d’authentification Web Kerberos.</span><span class="sxs-lookup"><span data-stu-id="3a27b-109">Because these accounts use the Kerberos authentication protocol, the accounts are referred to as Kerberos accounts, and the new authentication process is known as Kerberos web authentication.</span></span> <span data-ttu-id="3a27b-110">Cela vous permet de gérer tous vos serveurs IIS en utilisant un seul compte.</span><span class="sxs-lookup"><span data-stu-id="3a27b-110">This enables you to manage all your IIS servers by using a single account.</span></span>

<span data-ttu-id="3a27b-111">Pour exécuter vos serveurs sous ce principal d’authentification, vous devez d’abord créer un compte d’ordinateur à l’aide de l’applet de New-CsKerberosAccount cmdlet. ce compte est ensuite affecté à un ou plusieurs sites.</span><span class="sxs-lookup"><span data-stu-id="3a27b-111">To run your servers under this authentication principal, you must first create a computer account by using the New-CsKerberosAccount cmdlet; this account is then assigned to one or more sites.</span></span> <span data-ttu-id="3a27b-112">Une fois l’affectation créée, l’association entre le compte et le site 2013 de Lync Server est activée en exécutant l’applet de cmdlet Enable-CsTopology.</span><span class="sxs-lookup"><span data-stu-id="3a27b-112">After the assignment has been made, the association between the account and the Lync Server 2013 site is enabled by running the Enable-CsTopology cmdlet.</span></span> <span data-ttu-id="3a27b-113">Entre autres choses, cela crée le nom de principal de service (SPN) requis dans les services de domaine Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="3a27b-113">Among other things, this creates the required service principal name (SPN) in Active Directory Domain Services (AD DS).</span></span> <span data-ttu-id="3a27b-114">Les noms SPN permettent aux applications clientes de localiser un service.</span><span class="sxs-lookup"><span data-stu-id="3a27b-114">SPNs provide a way for client applications to locate a particular service.</span></span> <span data-ttu-id="3a27b-115">Pour plus d’informations, reportez-vous à la rubrique [New-CsKerberosAccount](https://docs.microsoft.com/powershell/module/skype/New-CsKerberosAccount) dans la documentation des opérations.</span><span class="sxs-lookup"><span data-stu-id="3a27b-115">For details, see [New-CsKerberosAccount](https://docs.microsoft.com/powershell/module/skype/New-CsKerberosAccount) in the Operations documentation.</span></span>

<div>

## <a name="best-practices"></a><span data-ttu-id="3a27b-116">Meilleures pratiques</span><span class="sxs-lookup"><span data-stu-id="3a27b-116">Best Practices</span></span>

<span data-ttu-id="3a27b-117">Pour renforcer la sécurité d’IIS, nous vous recommandons de mettre en œuvre un compte Kerberos pour les services Internet (IIS).</span><span class="sxs-lookup"><span data-stu-id="3a27b-117">To help increase security of IIS, we recommend that you implement a Kerberos account for IIS.</span></span> <span data-ttu-id="3a27b-118">Si vous n’avez pas implémenté de compte Kerberos, IIS s’exécute sous un compte d’utilisateur standard.</span><span class="sxs-lookup"><span data-stu-id="3a27b-118">If you do not implement a Kerberos account, IIS runs under a standard user account.</span></span>

<span data-ttu-id="3a27b-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3a27b-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

