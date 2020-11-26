---
title: 'Lync Server 2013 : Octroi d’autorisations d’unité organisationnelle'
description: 'Lync Server 2013 : octroi d’autorisations d’unité d’organisation.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Granting organizational unit permissions
ms:assetid: 95ee5ffa-39b1-4d80-87a2-27bb364f7396
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398763(v=OCS.15)
ms:contentKeyID: 48184849
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 47ad862241e409190620afa7dbf4fa73adf339de
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427895"
---
# <a name="granting-organizational-unit-permissions-in-lync-server-2013"></a><span data-ttu-id="ab500-103">Octroi d’autorisations d’unité organisationnelle dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ab500-103">Granting organizational unit permissions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ab500-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ab500-104">

<span> </span></span></span>

<span data-ttu-id="ab500-105">_**Dernière modification de la rubrique :** 2012-05-14_</span><span class="sxs-lookup"><span data-stu-id="ab500-105">_**Topic Last Modified:** 2012-05-14_</span></span>

<span data-ttu-id="ab500-106">Vous pouvez utiliser l’applet de passe **Grant-CsOuPermission** pour octroyer des autorisations aux objets d’unités d’organisation (UO) spécifiques de sorte que les membres des groupes universels RTC créés par la préparation de la forêt puissent y accéder sans être membres du groupe administrateurs de domaine.</span><span class="sxs-lookup"><span data-stu-id="ab500-106">You can use the **Grant-CsOuPermission** cmdlet to grant permissions to objects in specified organizational units (OUs) so that members of the RTC universal groups created by forest preparation can access them without being members of the Domain Admins group.</span></span> <span data-ttu-id="ab500-107">Les autorisations ajoutées à l’unité d’organisation spécifiée sont les mêmes que celles apportées par l’applet de action **Enable-CsAdDomain** à la préparation du domaine.</span><span class="sxs-lookup"><span data-stu-id="ab500-107">The permissions added to the specified OU are the same permissions that the **Enable-CsAdDomain** cmdlet adds to the computers and users containers during domain preparation.</span></span>

<span data-ttu-id="ab500-108">Utilisez l’applet de **contrôle test-CsOuPermission** pour vérifier les autorisations que vous avez configurées à l’aide de l’applet de contrôle **Grant-CsOuPermission** .</span><span class="sxs-lookup"><span data-stu-id="ab500-108">Use the **Test-CsOuPermission** cmdlet to verify the permissions you set up by using the **Grant-CsOuPermission** cmdlet.</span></span>

<span data-ttu-id="ab500-109">Vous pouvez utiliser l’applet de passe **Revoke-CsOuPermission** pour supprimer les autorisations accordées à l’aide de l’applet de passe **Grant-CsOuPermission** .</span><span class="sxs-lookup"><span data-stu-id="ab500-109">You can use the **Revoke-CsOuPermission** cmdlet to remove permissions that you granted by using the **Grant-CsOuPermission** cmdlet.</span></span>

<div>

## <a name="to-grant-ou-permissions"></a><span data-ttu-id="ab500-110">Pour octroyer des autorisations d’UO</span><span class="sxs-lookup"><span data-stu-id="ab500-110">To grant OU permissions</span></span>

1.  <span data-ttu-id="ab500-111">Ouvrez une session sur un ordinateur exécutant Lync Server 2013 dans le domaine dans lequel vous voulez accorder des autorisations d’UO.</span><span class="sxs-lookup"><span data-stu-id="ab500-111">Log on to a computer running Lync Server 2013 in the domain where you want to grant OU permissions.</span></span> <span data-ttu-id="ab500-112">Utilisez un compte membre du groupe administrateurs de domaine ou administrateurs d’entreprise si l’unité d’organisation se trouve dans un domaine enfant différent.</span><span class="sxs-lookup"><span data-stu-id="ab500-112">Use an account that is a member of the Domain Admins group or the Enterprise Admins group if the OU is in a different child domain.</span></span>

2.  <span data-ttu-id="ab500-113">Démarrez Lync Server Management Shell : cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="ab500-113">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="ab500-114">Exécutez :</span><span class="sxs-lookup"><span data-stu-id="ab500-114">Run:</span></span>
    
        Grant-CsOuPermission -ObjectType <User | Computer | InetOrgPerson | Contact | AppContact | Device> -OU <DN of the OU> [-Domain <Domain FQDN>]
    
    <span data-ttu-id="ab500-115">Si vous ne spécifiez pas le paramètre domain, la valeur par défaut est le domaine local.</span><span class="sxs-lookup"><span data-stu-id="ab500-115">If you do not specify the Domain parameter, the default value is the local domain.</span></span>

</div>

<div>

## <a name="to-verify-ou-permissions"></a><span data-ttu-id="ab500-116">Pour vérifier les autorisations d’UO</span><span class="sxs-lookup"><span data-stu-id="ab500-116">To verify OU permissions</span></span>

1.  <span data-ttu-id="ab500-117">Ouvrez une session sur un ordinateur exécutant Lync Server 2013 dans le domaine dans lequel vous voulez vérifier les autorisations d’UO que vous avez accordées à l’aide de l’applet de contrôle **Grant-CsOuPermission** .</span><span class="sxs-lookup"><span data-stu-id="ab500-117">Log on to a computer running Lync Server 2013 in the domain where you want to verify OU permissions that you granted by using the **Grant-CsOuPermission** cmdlet.</span></span> <span data-ttu-id="ab500-118">Utilisez un compte membre du groupe administrateurs de domaine ou administrateurs d’entreprise si l’unité d’organisation se trouve dans un domaine enfant différent.</span><span class="sxs-lookup"><span data-stu-id="ab500-118">Use an account that is a member of the Domain Admins group or the Enterprise Admins group if the OU is in a different child domain.</span></span>

2.  <span data-ttu-id="ab500-119">Démarrez Lync Server Management Shell : cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="ab500-119">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="ab500-120">Exécutez :</span><span class="sxs-lookup"><span data-stu-id="ab500-120">Run:</span></span>
    
        Test-CsOuPermission -ObjectType <User | Computer | InetOrgPerson | Contact | AppContact | Device> -OU <DN of the OU> [-Domain <Domain FQDN>]
    
    <span data-ttu-id="ab500-121">Si vous ne spécifiez pas le paramètre domain, la valeur par défaut est le domaine local.</span><span class="sxs-lookup"><span data-stu-id="ab500-121">If you do not specify the Domain parameter, the default value is the local domain.</span></span>

</div>

<div>

## <a name="to-revoke-ou-permissions"></a><span data-ttu-id="ab500-122">Pour révoquer les autorisations d’UO</span><span class="sxs-lookup"><span data-stu-id="ab500-122">To revoke OU permissions</span></span>

1.  <span data-ttu-id="ab500-123">Ouvrez une session sur un ordinateur exécutant Lync Server 2013 dans le domaine dans lequel vous voulez révoquer les autorisations d’unité d’organisation accordées par l’applet de connexion **Grant-CsOuPermission** .</span><span class="sxs-lookup"><span data-stu-id="ab500-123">Log on to a computer running Lync Server 2013 in the domain where you want to revoke OU permissions that were granted by the **Grant-CsOuPermission** cmdlet.</span></span> <span data-ttu-id="ab500-124">Utilisez un compte membre du groupe administrateurs de domaine ou administrateurs d’entreprise si l’unité d’organisation se trouve dans un domaine enfant différent.</span><span class="sxs-lookup"><span data-stu-id="ab500-124">Use an account that is a member of the Domain Admins group or the Enterprise Admins group if the OU is in a different child domain.</span></span>

2.  <span data-ttu-id="ab500-125">Démarrez Lync Server Management Shell : cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="ab500-125">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="ab500-126">Exécutez :</span><span class="sxs-lookup"><span data-stu-id="ab500-126">Run:</span></span>
    
        Revoke-CsOuPermission -ObjectType <User | Computer | InetOrgPerson | Contact | AppContact | Device> -OU <DN of the OU> [-Domain <Domain FQDN>]
    
    <span data-ttu-id="ab500-127">Si vous ne spécifiez pas le paramètre domain, la valeur par défaut est le domaine local.</span><span class="sxs-lookup"><span data-stu-id="ab500-127">If you do not specify the Domain parameter, the default value is the local domain.</span></span>

<span data-ttu-id="ab500-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ab500-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

