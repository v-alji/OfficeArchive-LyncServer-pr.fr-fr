---
title: 'Lync Server 2013 : Création des enregistrements DNS pour les serveurs proxy inverses'
description: 'Lync Server 2013 : créer des enregistrements DNS pour les serveurs proxy inverse.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create DNS records for reverse proxy servers
ms:assetid: b3513339-e49b-4665-80f1-b5a1c81a0e2e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429719(v=OCS.15)
ms:contentKeyID: 48185181
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ef785ebbd7160274b631a2d2b6b1f1dcc866e5fc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431945"
---
# <a name="create-dns-records-for-reverse-proxy-servers-in-lync-server-2013"></a>Création des enregistrements DNS pour les serveurs proxy inverses dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2013-03-29_

Créer un DNS externe un enregistrement qui pointe vers l’interface externe publique de votre serveur Microsoft Internet Security and Acceleration (ISA) Server 2006 SP1, de la passerelle de gestion des menaces Forefront 2010 ou du routage [2013 de](lync-server-2013-configure-dns-for-edge-support.md)requête sur Internet Information Server Vous avez besoin d’enregistrements DNS pour les noms de domaine complets des services Web externes de chaque liste, le directeur (ou le pool de directeurs) et chaque URL simple.

Les enregistrements DNS minimaux pour la résolution du client vers le proxy inverse, les enregistrements suivants doivent être créés :

  - Un ou plusieurs enregistrements d’hôte qui définissent les services Web externes publiés pour les directeurs et les pools de directeurs (par exemple, **webdirext.contoso.com**)

  - Un ou plusieurs enregistrements d’hôte (A) qui définissent les services Web externes publiés pour les services Web externes hébergés sur les pools frontaux et les rôles de serveur Standard Edition (par exemple, **webext.contoso.com**)

  - Des enregistrements d’hôte (A) pour les URL simples (par exemple, **Dialin.contoso.com** et **Meet.contoso.com**);

  - L’enregistrement d’hôte (A) pour l’enregistrement externe Discover Lync et fournit également un pointeur vers la découverte automatique pour toutes les applications Web, y compris Lync Web App, le planificateur et la mobilité (par exemple, **lyncdiscover.contoso.com**)

  - Les enregistrements d’hôte (A) pour l’URL du serveur Office Web Apps (par exemple, **officewebapp01.contoso.com**)

Pour plus d’informations, reportez-vous à la section [DNS Summary-inverse dans Lync Server 2013](lync-server-2013-dns-summary-reverse-proxy.md).

</div>

<span> </span>

</div>

</div>

</div>

