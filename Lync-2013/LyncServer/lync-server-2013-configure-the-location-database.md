---
title: 'Lync Server 2013 : configurer la base de données de localisation'
description: 'Lync Server 2013 : configurer la base de données de localisation.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure the location database
ms:assetid: 8544be31-6958-47ef-b926-fdc80d56191c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398679(v=OCS.15)
ms:contentKeyID: 48184704
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 877c83976ca0db9abc3a9e57d4a1cf5adaa1291a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433611"
---
# <a name="configure-the-location-database-in-lync-server-2013"></a>Configure the location database in Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2012-09-17_

Pour permettre aux clients de détecter automatiquement leur emplacement au sein d’un réseau, vous devez d’abord configurer la base de données d’emplacements. Si vous ne configurez pas de base de données de géolocalisation **et que** la stratégie d’emplacement est définie sur **Oui** ou **exclusion de responsabilité**, l’utilisateur est invité à entrer manuellement un emplacement.

Pour configurer la base de données de localisation, vous devez effectuer les tâches suivantes :

1.  Remplissez la base de données avec une correspondance des éléments réseau avec les emplacements. Si vous utilisez une passerelle ELIN), vous devez inclure la ELIN dans le \<CompanyName\> champ.

2.  Validez les adresses par rapport à la base de données MSAG gérée par le fournisseur de service E9-1-1.

3.  Publiez la base de données mise à jour.

<div>


> [!NOTE]  
> Vous pouvez également définir une base de données source de emplacement secondaire qui peut être utilisée dans l’emplacement de la base de données de localisation. Pour plus d’informations, voir <A href="lync-server-2013-configure-a-secondary-location-information-service.md">configurer un service d’information d’emplacement secondaire dans Lync Server 2013</A>.



</div>

<div>

## <a name="in-this-section"></a>Dans cette section

  - [Peupler la base de données de localisation dans Lync Server 2013](lync-server-2013-populate-the-location-database.md)

  - [Valider des adresses dans Lync Server 2013](lync-server-2013-validate-addresses.md)

  - [Publier la base de données de localisation à partir de Lync Server 2013](lync-server-2013-publish-the-location-database.md)

</div>

</div>

<span> </span>

</div>

</div>

</div>

