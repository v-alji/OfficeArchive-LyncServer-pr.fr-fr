---
title: Déploiement d’un Survivable Branch Appliance ou d’un serveur Survivable Branch Server - Tâches pour un site central
description: Déploiement d’une unité ou d’un serveur de succursale Survivable.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying a Survivable Branch Appliance or Server - central site tasks
ms:assetid: 0f631a36-fc2e-41cd-8a0d-f27e84f4a89e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398189(v=OCS.15)
ms:contentKeyID: 48183422
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4460ea215d6fc80ee89f1ca9bc42f08ac5d14617
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430132"
---
# <a name="deploying-a-survivable-branch-appliance-or-server-with-lync-server-2013---central-site-tasks"></a>Déploiement d’un Survivable Branch Appliance ou d’un serveur Survivable Branch Server avec Lync Server 2013 - Tâches pour un site central

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2012-10-18_

Suivez les étapes décrites dans cette section sur le site central. Si vous déployez un serveur de succursales survivant, ignorez la première tâche.

<div>


> [!IMPORTANT]
> Avant d’effectuer les tâches décrites dans cette section, les conditions suivantes doivent être en place : 
> <UL>
> <LI>
> <P>Le serveur Lync doit être configuré sur le site central.</P>
> <LI>
> <P>Un technicien d’installation sur le site de succursale doit être ajouté au groupe RTCUniversalSBATechnicians.</P></LI></UL>Par ailleurs, il est recommandé d’effectuer les opérations suivantes :
> <UL>
> <LI>
> <P>Déploiement d’un serveur DHCP sur chaque site de succursale pour permettre aux clients d’obtenir des adresses IP.</P>
> <LI>
> <P>À la place du déploiement d’un serveur DHCP sur chaque site de succursale, activez le protocole DHCP de Lync Server sur l’appareil de succursales survivant ou sur le serveur de succursales survivant en utilisant l’applet de cmdlet Lync Server Management Shell <STRONG>Set-CsRegistrarConfiguration – EnableDHCPServer $true</STRONG>. Pour plus d’informations, reportez-vous à la section « Configuration matérielle et logicielle requise » dans la rubrique Configuration de la <A href="lync-server-2013-branch-site-resiliency-requirements.md">résilience de site pour Lync Server 2013</A> dans la documentation de planification.</P></LI></UL>



</div>

<div>

## <a name="in-this-section"></a>Dans cette section

  - [Ajout d’un Survivable Branch Appliance à Active Directory dans Lync Server 2013](lync-server-2013-add-a-survivable-branch-appliance-to-active-directory.md)

  - [Ajout des sites de succursale à votre topologie dans Lync Server 2013](lync-server-2013-add-branch-sites-to-your-topology.md)

  - [Définition d’un Survivable Branch Appliance ou d’un serveur Survivable Branch Server dans Lync Server 2013](lync-server-2013-define-a-survivable-branch-appliance-or-server.md)

</div>

</div>

<span> </span>

</div>

</div>

</div>

