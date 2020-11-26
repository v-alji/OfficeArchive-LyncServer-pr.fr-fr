---
title: Supprimer une entrée d’hôte autorisée
description: Supprimer une entrée d’hôte autorisée.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Remove an authorized host entry
ms:assetid: 56a04140-347e-4eef-bede-0e858534f71e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204902(v=OCS.15)
ms:contentKeyID: 48184177
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 95aa8df1745ad3108654fcb9b441b5919d42ec40
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443257"
---
# <a name="remove-an-authorized-host-entry"></a><span data-ttu-id="449e5-103">Supprimer une entrée d’hôte autorisée</span><span class="sxs-lookup"><span data-stu-id="449e5-103">Remove an authorized host entry</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="449e5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="449e5-104">

<span> </span></span></span>

<span data-ttu-id="449e5-105">_**Dernière modification de la rubrique :** 2012-09-26_</span><span class="sxs-lookup"><span data-stu-id="449e5-105">_**Topic Last Modified:** 2012-09-26_</span></span>

<span data-ttu-id="449e5-106">Cette rubrique explique comment supprimer une entrée d’hôte autorisé héritée (connue sous le nom d' *entrée d’application fiable* dans Lync Server 2013).</span><span class="sxs-lookup"><span data-stu-id="449e5-106">This topic describes how to remove a legacy authorized host entry (known as a *trusted application entry* in Lync Server 2013).</span></span> <span data-ttu-id="449e5-107">Vous devez supprimer les entrées d’hôte autorisées existantes pour toutes les passerelles SIP/CSTA dans votre déploiement d’Office Communications Server 2007 R2 lors de la migration du contrôle d’appel distant vers un déploiement Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="449e5-107">You must remove existing authorized host entries for any SIP/CSTA gateways in your Office Communications Server 2007 R2 deployment when you migrate remote call control to a Lync Server 2013 deployment.</span></span> <span data-ttu-id="449e5-108">Vous devez utiliser les outils d’administration inclus dans Office Communications Server 2007 R2 pour supprimer les entrées d’hébergement autorisées existantes.</span><span class="sxs-lookup"><span data-stu-id="449e5-108">You must use the administrative tools included with Office Communications Server 2007 R2 to remove the existing authorized host entries.</span></span>

<div>

## <a name="to-remove-an-authorized-host-entry-in-an-office-communications-server-2007-r2-deployment"></a><span data-ttu-id="449e5-109">Pour supprimer une entrée d’hôte autorisée dans un déploiement d’Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="449e5-109">To remove an authorized host entry in an Office Communications Server 2007 R2 deployment</span></span>

1.  <span data-ttu-id="449e5-110">Ouvrez la console d’administration d’Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="449e5-110">Open the Office Communications Server 2007 R2 administrative console.</span></span>

2.  <span data-ttu-id="449e5-111">Développez l’arborescence, puis cliquez avec le bouton droit sur le pool dans lequel l’hôte autorisé a été créé.</span><span class="sxs-lookup"><span data-stu-id="449e5-111">Expand the tree and right-click the pool where the authorized host was created.</span></span>

3.  <span data-ttu-id="449e5-112">Cliquez sur **Propriétés**, puis sur **Propriétés du front end**.</span><span class="sxs-lookup"><span data-stu-id="449e5-112">Click **Properties**, and then click **Front End Properties**.</span></span>

4.  <span data-ttu-id="449e5-113">Cliquez sur l’onglet **autorisation d’hébergement** .</span><span class="sxs-lookup"><span data-stu-id="449e5-113">Click the **Host Authorization** tab.</span></span>

5.  <span data-ttu-id="449e5-114">Sélectionnez un serveur, puis cliquez sur **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="449e5-114">Select a server, and then click **Remove**.</span></span>

6.  <span data-ttu-id="449e5-115">Dans **Propriétés**, cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="449e5-115">In **Properties**, click **OK**.</span></span>

<span data-ttu-id="449e5-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="449e5-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

