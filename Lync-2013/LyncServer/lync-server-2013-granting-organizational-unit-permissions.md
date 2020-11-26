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
# <a name="granting-organizational-unit-permissions-in-lync-server-2013"></a>Octroi d’autorisations d’unité organisationnelle dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2012-05-14_

Vous pouvez utiliser l’applet de passe **Grant-CsOuPermission** pour octroyer des autorisations aux objets d’unités d’organisation (UO) spécifiques de sorte que les membres des groupes universels RTC créés par la préparation de la forêt puissent y accéder sans être membres du groupe administrateurs de domaine. Les autorisations ajoutées à l’unité d’organisation spécifiée sont les mêmes que celles apportées par l’applet de action **Enable-CsAdDomain** à la préparation du domaine.

Utilisez l’applet de **contrôle test-CsOuPermission** pour vérifier les autorisations que vous avez configurées à l’aide de l’applet de contrôle **Grant-CsOuPermission** .

Vous pouvez utiliser l’applet de passe **Revoke-CsOuPermission** pour supprimer les autorisations accordées à l’aide de l’applet de passe **Grant-CsOuPermission** .

<div>

## <a name="to-grant-ou-permissions"></a>Pour octroyer des autorisations d’UO

1.  Ouvrez une session sur un ordinateur exécutant Lync Server 2013 dans le domaine dans lequel vous voulez accorder des autorisations d’UO. Utilisez un compte membre du groupe administrateurs de domaine ou administrateurs d’entreprise si l’unité d’organisation se trouve dans un domaine enfant différent.

2.  Démarrez Lync Server Management Shell : cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Lync Server Management Shell**.

3.  Exécutez :
    
        Grant-CsOuPermission -ObjectType <User | Computer | InetOrgPerson | Contact | AppContact | Device> -OU <DN of the OU> [-Domain <Domain FQDN>]
    
    Si vous ne spécifiez pas le paramètre domain, la valeur par défaut est le domaine local.

</div>

<div>

## <a name="to-verify-ou-permissions"></a>Pour vérifier les autorisations d’UO

1.  Ouvrez une session sur un ordinateur exécutant Lync Server 2013 dans le domaine dans lequel vous voulez vérifier les autorisations d’UO que vous avez accordées à l’aide de l’applet de contrôle **Grant-CsOuPermission** . Utilisez un compte membre du groupe administrateurs de domaine ou administrateurs d’entreprise si l’unité d’organisation se trouve dans un domaine enfant différent.

2.  Démarrez Lync Server Management Shell : cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Lync Server Management Shell**.

3.  Exécutez :
    
        Test-CsOuPermission -ObjectType <User | Computer | InetOrgPerson | Contact | AppContact | Device> -OU <DN of the OU> [-Domain <Domain FQDN>]
    
    Si vous ne spécifiez pas le paramètre domain, la valeur par défaut est le domaine local.

</div>

<div>

## <a name="to-revoke-ou-permissions"></a>Pour révoquer les autorisations d’UO

1.  Ouvrez une session sur un ordinateur exécutant Lync Server 2013 dans le domaine dans lequel vous voulez révoquer les autorisations d’unité d’organisation accordées par l’applet de connexion **Grant-CsOuPermission** . Utilisez un compte membre du groupe administrateurs de domaine ou administrateurs d’entreprise si l’unité d’organisation se trouve dans un domaine enfant différent.

2.  Démarrez Lync Server Management Shell : cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Lync Server Management Shell**.

3.  Exécutez :
    
        Revoke-CsOuPermission -ObjectType <User | Computer | InetOrgPerson | Contact | AppContact | Device> -OU <DN of the OU> [-Domain <Domain FQDN>]
    
    Si vous ne spécifiez pas le paramètre domain, la valeur par défaut est le domaine local.

</div>

</div>

<span> </span>

</div>

</div>

</div>

