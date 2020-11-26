---
title: 'Lync Server 2013 : règles de mise à jour d’appareils'
description: 'Lync Server 2013 : règles de mise à jour d’appareil.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Device Update rules
ms:assetid: a2f7e293-3342-4566-9605-410cb95f3b3b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994062(v=OCS.15)
ms:contentKeyID: 51803973
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bd6d34c290f4a08f67143294fcc5dd18e1acf9d1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429373"
---
# <a name="device-update-rules-in-lync-server-2013"></a><span data-ttu-id="f3bc7-103">Règles de mise à jour des appareils dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f3bc7-103">Device Update rules in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f3bc7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f3bc7-104">

<span> </span></span></span>

<span data-ttu-id="f3bc7-105">_**Dernière modification de la rubrique :** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="f3bc7-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="f3bc7-106">Périodiquement, Microsoft publie un nouvel ensemble de mises à jour de microprogramme de périphérique pour Lync Phone Edition.</span><span class="sxs-lookup"><span data-stu-id="f3bc7-106">Periodically, Microsoft releases a new set of device firmware updates for Lync Phone Edition.</span></span> <span data-ttu-id="f3bc7-107">Les *règles de mise à jour* de l’appareil associent les mises à jour du microprogramme aux périphériques matériels (téléphones et autres appareils exécutant Lync Phone Edition).</span><span class="sxs-lookup"><span data-stu-id="f3bc7-107">*Device update rules* associate firmware updates with hardware devices—phones and other devices running Lync Phone Edition.</span></span>

<span data-ttu-id="f3bc7-108">Pour obtenir le dernier ensemble de règles de mise à jour de l’appareil, accédez à la page aide et support sur le site Web de Microsoft et recherchez « Phone Edition ».</span><span class="sxs-lookup"><span data-stu-id="f3bc7-108">To get the latest set of device update rules, go to the Help and Support page on the Microsoft website, and search for "Phone Edition."</span></span> <span data-ttu-id="f3bc7-109">Téléchargez le package de mise à jour et extrayez les fichiers vers un dossier sur l’ordinateur sur lequel les mises à jour doivent être téléchargées.</span><span class="sxs-lookup"><span data-stu-id="f3bc7-109">Download the update package, and extract the files to a folder on the computer where the updates are to be uploaded.</span></span> <span data-ttu-id="f3bc7-110">Une fois les fichiers extraits, importez les règles de mise à jour de l’appareil trouvées dans le fichier extrait. Fichier CAB (nom UCUpdates.cab).</span><span class="sxs-lookup"><span data-stu-id="f3bc7-110">After the files have been extracted, import the device update rules found in the extracted .CAB file (which have the name UCUpdates.cab).</span></span> <span data-ttu-id="f3bc7-111">Utilisez ensuite le panneau de configuration de Lync Server ou les applets de commande Windows PowerShell pour afficher et gérer ces règles pour les appareils de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="f3bc7-111">Then, use the Lync Server Control Panel or Windows PowerShell cmdlets to view and manage these rules for your organization’s devices.</span></span>

<span data-ttu-id="f3bc7-112">Les rubriques suivantes vous expliquent comment importer, afficher et gérer des règles de mise à jour d’appareil.</span><span class="sxs-lookup"><span data-stu-id="f3bc7-112">The following topics tell you how to import, view, and manage device update rules.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="f3bc7-113">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="f3bc7-113">In This Section</span></span>

  - [<span data-ttu-id="f3bc7-114">Afficher des informations sur les règles de mise à jour des appareils dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f3bc7-114">View information about Device Update rules in Lync Server 2013</span></span>](lync-server-2013-view-information-about-device-update-rules.md)

  - [<span data-ttu-id="f3bc7-115">Importer des règles de mise à jour de périphériques dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f3bc7-115">Import Device Update rules in Lync Server 2013</span></span>](lync-server-2013-import-device-update-rules.md)

  - [<span data-ttu-id="f3bc7-116">Approuver une règle de mise à jour d’appareil dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f3bc7-116">Approve a Device Update rule in Lync Server 2013</span></span>](lync-server-2013-approve-a-device-update-rule.md)

  - [<span data-ttu-id="f3bc7-117">Supprimer une règle de mise à jour d’appareil dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f3bc7-117">Remove a Device Update rule in Lync Server 2013</span></span>](lync-server-2013-remove-a-device-update-rule.md)

  - [<span data-ttu-id="f3bc7-118">Réinitialiser une règle de mise à jour d’appareil dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f3bc7-118">Reset a Device Update rule in Lync Server 2013</span></span>](lync-server-2013-reset-a-device-update-rule.md)

  - [<span data-ttu-id="f3bc7-119">Restaurer une règle de mise à jour d’appareil dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f3bc7-119">Restore a Device Update rule in Lync Server 2013</span></span>](lync-server-2013-restore-a-device-update-rule.md)

<span data-ttu-id="f3bc7-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f3bc7-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

