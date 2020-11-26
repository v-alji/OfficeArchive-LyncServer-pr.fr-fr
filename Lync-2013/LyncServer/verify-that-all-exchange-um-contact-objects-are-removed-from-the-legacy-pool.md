---
title: Vérifier que tous les objets de contact Exchange UM sont supprimés du pool hérité
description: Vérifiez que tous les objets de contact Exchange UM sont supprimés du pool hérité.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Verify that all Exchange UM Contact objects are removed from the legacy pool
ms:assetid: 5a813169-0ed7-4f84-a242-ed2cd4ea5c43
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688068(v=OCS.15)
ms:contentKeyID: 49733664
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8af5dea6cf746c55d8fecf074e132f721c380de1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440135"
---
# <a name="verify-that-all-exchange-um-contact-objects-are-removed-from-the-legacy-pool"></a>Vérifier que tous les objets de contact Exchange UM sont supprimés du pool hérité

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2012-09-26_

Utilisez l’outil **OCSUmUtil** ou l’applet de contrôle **Get-CsExumContact** pour vérifier que les objets de contact de messagerie unifiée Exchange ont été supprimés du pool Office Communications Server 2007 R2 hérité. **OCSUmUtil** se trouve dans le dossier suivant :

% Program Files% \\ fichiers communs \\ Lync Server 2013 \\ support \\OcsUMUtil.exe

**OCSUmUtil** doit être exécuté à partir d’un compte d’utilisateur disposant des éléments suivants :

  - Appartenance au groupe RTCUniversalServerAdmins et RTCUniversalUserAdmins (y compris les droits pour lire les paramètres de messagerie unifiée Exchange Server)

  - Droits de domaine pour créer des objets de contact dans le conteneur d’unité d’organisation (UO) spécifié

Pour plus d’informations sur l’utilisation de l’applet de connexion **Get-CsExumContact** , voir [Get-CsExumContact](https://docs.microsoft.com/powershell/module/skype/Get-CsExUmContact) dans la documentation Lync Server Management Shell.

</div>

<span> </span>

</div>

</div>

</div>

