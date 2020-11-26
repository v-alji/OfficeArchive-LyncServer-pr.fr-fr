---
title: 'Lync Server 2013 : installation des fichiers de l’agent Operation Manager'
description: 'Lync Server 2013 : installation des fichiers de l’agent Operation Manager.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Installing the Operation Manager agent files
ms:assetid: e2246c44-0c75-43fc-8b04-26e53c5dd572
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205345(v=OCS.15)
ms:contentKeyID: 48185692
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 61bba93549e4831b65657a1fe80c918bbcb45572
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426920"
---
# <a name="installing-the-operation-manager-agent-files-in-lync-server-2013"></a>Installation des fichiers de l’agent Operation Manager dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2012-10-20_

Pour installer les fichiers de l’agent Operations Manager sur l’ordinateur, procédez comme suit.

1.  Sur votre média de configuration de System Center, double-cliquez sur **SetupOM.exe**.

2.  Dans installation de System Center Operation Manager, cliquez sur **installer l’agent Operations Manager**.

3.  Dans l’Assistant Configuration de System Center, dans la page Bienvenue dans l’Assistant **configuration de System Center Operations Manager** , cliquez sur **suivant**.

4.  Dans la page **dossier de destination** , sélectionnez le dossier dans lequel les fichiers de l’agent Operations Manager seront installés, puis cliquez sur **suivant**.

5.  Dans la page **configuration du groupe de gestion** , sélectionnez spécifier les informations du groupe d' **administration**, puis cliquez sur **suivant**.

6.  Dans la page **configuration du groupe** de gestion, tapez le nom de votre groupe d’administration Operations Manager dans la zone Nom du groupe de **gestion** , puis tapez le nom d’hôte de votre serveur Operations Manager (par exemple, ATL-SCOM-001) dans la zone serveur de **gestion** . Si vous avez modifié le numéro de port utilisé par Operations Manager, entrez le nouveau numéro de port dans la zone port du serveur de gestion. Dans le cas contraire, laissez le port à la valeur par défaut 5723, puis cliquez sur **suivant**.

7.  Sur la page **compte d’action** de l’agent, sélectionnez **système local**, puis cliquez sur **suivant**.

8.  Sur la page **Microsoft Update** , sélectionnez **je ne veux pas utiliser Microsoft Update**, puis cliquez sur **suivant**.

9.  Sur la page **prêt pour l’installation** , cliquez sur **installer**.

10. Dans la page **fin de l’Assistant Configuration de System Center Operations Manager** , cliquez sur **Terminer**.

11. Cliquez sur **Quitter**.

Si vous utilisez System Center 2007 R2, vous pouvez vérifier que l’agent a été créé en cliquant sur **Démarrer**, sur **tous les programmes**, sur **System Center Operations Manager 2007 R2**, puis sur **Operations Manager Shell**. In the Operations Manager Shell, type the following Windows PowerShell command, and then press ENTER:

    Get-Agent 

La liste de tous vos agents Operations Manager s’affiche à l’écran.

Si vous utilisez System Center 2012, exécutez la commande suivante à partir du shell Operations 2012 Manager :

    Get-SCOMAgent

</div>

<span> </span>

</div>

</div>

</div>

