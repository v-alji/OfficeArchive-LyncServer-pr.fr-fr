---
title: Prise en charge d’Active Directory dans Lync Server 2013
description: Prise en charge de Lync Server 2013 Active Directory.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Active Directory support
ms:assetid: 28ed9ac4-586d-4803-ad45-99c4fa793f54
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425756(v=OCS.15)
ms:contentKeyID: 48183679
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 349862b2f541ef3033c9a725a6ff04c6a4e219f7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439407"
---
# <a name="active-directory-support-in-lync-server-2013"></a>Prise en charge d’Active Directory dans Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2012-12-04_

Les topologies locales services de domaine Active Directory prises en charge par Lync Server 2013 sont les suivantes :

  - Forêt unique avec domaine unique

  - Forêt unique avec un arbre unique et plusieurs domaines

  - Forêt unique avec plusieurs arbres et des espaces de noms disjoints

  - Plusieurs forêts dans une topologie de forêt centrale

  - Plusieurs forêts dans une topologie de forêt de ressources

<div>


> [!NOTE]  
> Lync Server 2013 ne prend pas en charge les domaines à étiquette unique. Par exemple, une forêt avec un domaine racine appelé <STRONG>contoso. local</STRONG> est prise en charge, mais un domaine racine à une seule étiquette nommé <STRONG>local</STRONG> n’est pas pris en charge. Pour plus d’informations, reportez-vous à l’article 300684 de la base de connaissances Microsoft, intitulé « informations sur la configuration de Windows pour les domaines avec des noms DNS en une seule étiquette » <A href="https://go.microsoft.com/fwlink/p/?linkid=143752">https://go.microsoft.com/fwlink/p/?linkId=143752</A> .



</div>

<div>


> [!NOTE]  
> Lync Server 2013 ne prend pas en charge le changement de nom de domaines. Si vous avez besoin de renommer un domaine sur lequel Lync Server est déployé, vous devez commencer par désinstaller Lync Server, puis renommer le domaine, puis réinstaller Lync Server.



</div>

Pour plus d’informations sur les topologies prises en charge et la configuration requise pour les déploiements sur site, voir [Configuration requise pour les services de domaine Active Directory, support et topologies dans Lync Server 2013](lync-server-2013-active-directory-domain-services-requirements-support-and-topologies.md) dans la documentation de planification.

</div>

<span> </span>

</div>

</div>

</div>

