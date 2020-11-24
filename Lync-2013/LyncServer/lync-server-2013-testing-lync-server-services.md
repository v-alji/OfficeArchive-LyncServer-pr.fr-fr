---
title: 'Lync Server 2013 : test des services Lync Server'
description: 'Lync Server 2013 : test des services serveur Lync.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing Lync Server services
ms:assetid: b564b450-a746-4ec9-aabb-e076309ccd5f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn689119(v=OCS.15)
ms:contentKeyID: 63969644
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f04cf5e0c098c671b6fb126d4607f3cdba107712
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394484"
---
# <a name="testing-lync-server-services-in-lync-server-2013"></a>Test des services serveur Lync dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2014-06-05_


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Échéancier de vérification</p></td>
<td><p>Jour</p></td>
</tr>
<tr class="even">
<td><p>Outil de test</p></td>
<td><p>Windows PowerShell</p></td>
</tr>
<tr class="odd">
<td><p>Autorisations requises</p></td>
<td><p>Lorsque l’application est exécutée localement à l’aide de Lync Server Management Shell, les utilisateurs doivent être membres du groupe de sécurité RTCUniversalServerAdmins.</p>
<p>Lors de l’exécution à l’aide d’une instance distante de Windows PowerShell, un rôle RBAC doit être attribué aux utilisateurs qui ont l’autorisation d’exécuter l’applet de commande Test-CsComputer. Pour afficher la liste de tous les rôles RBAC qui peuvent utiliser cette applet de commande, exécutez la commande suivante à partir de l’invite Windows PowerShell :</p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsComputer&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a>Description

Test-CsComputer vérifie l’état de tous les services Lync Server 2013 en cours d’exécution sur l’ordinateur local. (Test-CsComputer peut uniquement être exécuté localement, il ne peut pas être exécuté à partir d’une instance distante de Windows PowerShell.) L’applet de contrôle vérifie également si les ports de pare-feu appropriés sont ouverts sur l’ordinateur et détermine si les groupes Active Directory créés lors de l’installation de Lync Server 2013 ont été ajoutés aux groupes locaux correspondants. Par exemple, Test-CsComputer vérifiera que le groupe Active Directory RTCUniversalUserAdmins a été ajouté au groupe administrateurs.

Pour plus d’informations, consultez la documentation d’aide de l’applet de [contrôle test-CsComputer](https://docs.microsoft.com/powershell/module/skype/Test-CsComputer) .

</div>

<div>

## <a name="running-the-test"></a>Exécution du test

L’applet de commande Test-CsComputer ne peut être exécutée que sur l’ordinateur local, vous ne pouvez pas appeler Test-CsComputer à partir d’une instance distante de Windows PowerShell. Par défaut, Test-CsComputer affiche un peu de sortie à l’écran, les informations renvoyées par l’applet de passe sont écrites dans un fichier HTML. Pour cette raison, nous vous recommandons d’inclure le paramètre Verbose et le paramètre de rapport chaque fois que vous exécutez test-CsComputer. Le paramètre Verbose fournit un affichage à l’écran détaillé légèrement plus détaillé lors de l’exécution de la cmdlet. Le paramètre rapport vous permet de spécifier un chemin d’accès et un nom de fichier pour le fichier HTML généré par test-CsComputer. Si vous n’incluez pas le paramètre de rapport, le fichier HTML sera automatiquement enregistré dans votre dossier utilisateurs et donner un nom semblable à ce qui suit : ce84964a-c4da-4622-ad34-c54ff3ed361f.html.

L’exemple de commande suivant exécute Test-CsComputer et enregistre la sortie dans un fichier nommé C : \\ Logs \\ComputerTest.html :

    Test-CsComputer -Report "C:\Logs\ComputerTest.html" -Verbose

Pour plus d’informations, consultez la documentation d’aide de l’applet de [contrôle test-CsComputer](https://docs.microsoft.com/powershell/module/skype/Test-CsComputer) .

</div>

<div>

## <a name="determining-success-or-failure"></a>Détermination du succès ou de l’échec

En raison du nombre de contrôles de vérification qu’il effectue, Test-CsComputer ne rapporte pas une simple **Oui, le test a réussi** ou **non, le test a échoué**. Au lieu de cela, vous devez afficher le fichier HTML généré à l’aide d’Internet Explorer pour déterminer la réussite ou l’échec de chaque test.

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a>Raisons pour lesquelles le test peut avoir échoué

Voici quelques raisons courantes pour lesquelles Test-CsComputer risque d’échouer :

  - L’ordinateur de test n’est peut-être pas activé pour une utilisation avec Lync Server. Cela peut se produire si les services serveur Lync ou les rôles serveur sur l’ordinateur ont changé et que l’applet de Enable-CsComputer n’était pas exécutée. Pour résoudre ce problème, exécutez la commande suivante :
    
        Enable-CsComputer

  - La réplication n’est peut-être pas à jour sur l’ordinateur de test. Vous pouvez vérifier l’état de réplication actuel d’un ordinateur en exécutant l’applet de contrôle Get-CsManagementStoreReplicationStatus :
    
        Get-CsManagementStoreReplicationStatus -ReplicaFqdn "atl-cs-001.litwareinc.com"
    
    Si l’état de la réplication n’est pas à jour, vous pouvez le faire manuellement en utilisant une commande similaire à celle-ci :
    
        Invoke-CsManagementStoreReplication -ReplicaFqdn "atl-cs-001.litwareinc.com"

  - La topologie peut être activée. Si vous modifiez la topologie du serveur Lync (modifications qui peuvent affecter l’ordinateur local), vous devez activer la nouvelle topologie. Vous pouvez activer la topologie à tout moment en exécutant la commande suivante :
    
        Enable-CsTopology

</div>

</div>

<span> </span>

</div>

</div>

</div>

