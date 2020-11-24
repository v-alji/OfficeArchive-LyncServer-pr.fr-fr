---
title: 'Lync Server 2013 : Importation des cas de test de routage des communications vocales'
description: 'Lync Server 2013 : importer des cas de test de routage vocal.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Import voice routing test cases
ms:assetid: 6546e24c-9ad2-428b-92b2-63948ed0f884
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398460(v=OCS.15)
ms:contentKeyID: 48184325
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 06ce1b144de03406b7b78d6957371ed2bc303e95
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394897"
---
# <a name="import-voice-routing-test-cases-in-lync-server-2013"></a>Importation des cas de test de routage des communications vocales dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2013-02-21_

Les scénarios de test vous permettent de tester les itinéraires vocaux au sein de votre organisation : vous définissez des éléments tels que le numéro à composer, le plan de numérotation et la politique vocale à utiliser, et Lync Server 2013 peut alors vérifier que le numéro fourni peut être acheminé au réseau PSTN.

Les cas de test, qui peuvent être créés à l’aide du panneau de configuration de Lync Server, sont généralement enregistrés uniquement sur le serveur où le cas a été créé et exécuté à l’origine. Toutefois, ces cas de test peuvent être exportés sous forme de fichiers XML (avec l’extension. vtest), puis importés sur d’autres serveurs. Cela vous permet d’exécuter les mêmes tests sur différents ordinateurs situés à différents endroits de votre topologie.

<div>

## <a name="to-import-a-voice-routing-test-case"></a>Pour importer un cas de test de routage vocal

1.  Connectez-vous à l’ordinateur en tant que membre du groupe RTCUniversalServerAdmins ou en tant que membre du rôle CsVoiceAdministrator, CsServerAdministrator ou CsAdministrator. Pour plus d’informations, reportez-vous à la section [délégation des autorisations de configuration dans Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).

2.  Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server. Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).

3.  Dans la barre de navigation de gauche, cliquez sur **Routage des communications vocales**.

4.  Dans le menu **actions** , cliquez sur **Importer les cas de test**.

5.  Recherchez le fichier de cas de test (. vtest) que vous voulez importer, puis cliquez sur **ouvrir**.

6.  Cliquez sur **Valider**, puis sur **Tout valider**.
    
    <div>
    

    > [!NOTE]  
    > Chaque fois que vous importez un fichier. vtest, vous devez exécuter la commande <STRONG>valider tout</STRONG> pour publier le cas de test. Pour plus d’informations, reportez-vous <A href="lync-server-2013-publish-pending-changes-to-the-voice-routing-configuration.md">à la rubrique publier des modifications en attente sur la configuration de l’acheminement de la voix dans Lync Server 2013</A> dans la documentation

    
    </div>

</div>

<div>

## <a name="see-also"></a>Voir aussi


[Exportation des cas de test de routage des communications vocales dans Lync Server 2013](lync-server-2013-export-voice-routing-test-cases.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

