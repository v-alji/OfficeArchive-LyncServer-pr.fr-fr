---
title: 'Lync Server 2013 : Utilisation des commandes d’applet pour inverser la préparation d’une forêt'
description: 'Lync Server 2013 : utilisation de cmdlets pour inverser la préparation de la forêt.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Using cmdlets to reverse forest preparation
ms:assetid: f48c7eb3-ccb0-48e6-ac79-ab7c7062b9d3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413024(v=OCS.15)
ms:contentKeyID: 48185822
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: acac87bdaeb7e730f93401fa62ea2678a713bb8f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439638"
---
# <a name="using-cmdlets-to-reverse-forest-preparation-for-lync-server-2013"></a>Utilisation des commandes d’applet pour inverser la préparation d’une forêt pour Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2013-06-19_

Utilisez l’applet de action **Disable-CsAdForest** pour inverser l’étape de préparation de la forêt.

<div>


> [!WARNING]  
> Si vous exécutez l’applet de contrôle <STRONG>Disable-CsAdForest</STRONG> dans un environnement dans lequel vous avez également une version antérieure de Lync Server déployée, les paramètres globaux de la version précédente sont également supprimés.



</div>

<div>

## <a name="to-use-cmdlets-to-reverse-forest-preparation"></a>Pour utiliser des applets de cmdlet pour inverser la préparation de la forêt

1.  Ouvrez une session sur un ordinateur qui est joint à un domaine en tant que membre du groupe Domain Admins dans le domaine racine de la forêt.

2.  Démarrez Lync Server Management Shell : cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Lync Server Management Shell**.

3.  Exécutez :
    
        Disable-CsAdForest [-Force] [-GroupDomain <FQDN of the domain in which universal groups were created>]
    
    Par exemple :
    
        Disable-CsAdForest -Force -GroupDomain contoso.net
    
    Le paramètre Force spécifie si l’exécution de la tâche doit être forcée. Si ce paramètre n’est pas présent, la commande ne s’exécute pas s’il n’y a pas encore de domaine dans la forêt pour Lync Server 2013. Si le paramètre force est spécifié, l’action se poursuit indépendamment de l’état des autres domaines dans la forêt.
    
    Si vous ne spécifiez pas le paramètre GroupDomain, la valeur par défaut est le domaine local.

</div>

<div>

## <a name="see-also"></a>Voir aussi


[Exécution de la préparation de la forêt pour Lync Server 2013](lync-server-2013-running-forest-preparation.md)  


[Préparation de la forêt pour Lync Server 2013](lync-server-2013-preparing-the-forest.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

