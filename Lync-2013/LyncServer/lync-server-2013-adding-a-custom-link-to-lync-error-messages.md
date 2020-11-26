---
title: 'Lync Server 2013 : ajout d’un lien personnalisé à des messages d’erreur Lync'
description: 'Lync Server 2013 : ajout d’un lien personnalisé aux messages d’erreur Lync.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Adding a custom link to Lync error messages
ms:assetid: de756088-fcc3-4e47-bde8-4fa4cc852fd1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398979(v=OCS.15)
ms:contentKeyID: 48185607
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a5d333b6f27e10e5092de23fcdf1d37fd75e75a5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439281"
---
# <a name="adding-a-custom-link-to-lync-error-messages-in-lync-server-2013"></a>Ajout d’un lien personnalisé à des messages d’erreur Lync dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2013-02-20_

Personnalisez les messages d’erreur de Lync 2013 en ajoutant un lien vers votre propre dépannage ou les informations de votre support technique. Pour ce faire, utilisez les applets de applet **nouvelle-CSClientPolicy** ou **Set-CSClientPolicy** Lync Server Management Shell avec le paramètre CustomLinkInErrorMessages. Le texte du lien personnalisé est « cliquer ici pour afficher les rubriques d’aide de votre administrateur » et ne peut pas être personnalisé.

Par exemple, la commande suivante entraîne l’affichage du lien personnalisé dans la zone de note de bas de page de chaque message d’erreur Lync 2013 et définit la destination du lien sur http://contoso.com/help/LyncHelpDesk.aspx:

    New-CsClientPolicy -Identity LyncErrorLink -CustomLinkInErrorMessages "http://contoso/help/LyncHelpDesk.aspx"

Utilisez **Grant-CSClientPolicy** pour affecter cette nouvelle stratégie aux utilisateurs. Pour plus d’informations, reportez-vous à **New-CSClientPolicy** et **Grant-CSClientPolicy** dans la documentation Lync Server Management Shell.

</div>

<span> </span>

</div>

</div>

</div>

