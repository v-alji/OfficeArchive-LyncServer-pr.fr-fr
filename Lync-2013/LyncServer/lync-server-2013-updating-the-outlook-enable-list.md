---
title: 'Lync Server 2013 : mise à jour de la liste d’activations d’Outlook'
description: 'Lync Server 2013 : mise à jour de la liste d’activations d’Outlook.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Updating the Outlook enable list
ms:assetid: 5db120dc-52f9-4dde-acb9-3824ae245086
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ215438(v=OCS.15)
ms:contentKeyID: 48242739
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 96edc327fa1b63d5da95eb6ea36a2296659910d6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394841"
---
# <a name="updating-the-outlook-enable-list-in-lync-server-2013"></a><span data-ttu-id="a387f-103">Mise à jour de la liste d’activations d’Outlook dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a387f-103">Updating the Outlook enable list in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a387f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a387f-104">

<span> </span></span></span>

<span data-ttu-id="a387f-105">_**Dernière modification de la rubrique :** 2013-01-07_</span><span class="sxs-lookup"><span data-stu-id="a387f-105">_**Topic Last Modified:** 2013-01-07_</span></span>

<span data-ttu-id="a387f-106">Vous pouvez vous assurer que le complément réunion en ligne pour Microsoft Lync 2013 reste actif pour les utilisateurs en créant une stratégie qui l’inclut dans la liste de gestion des compléments pour Outlook.</span><span class="sxs-lookup"><span data-stu-id="a387f-106">You can ensure that Online Meeting Add-in for Microsoft Lync 2013 always remains enabled for users by creating a policy that includes it in the Add-in Management List for Outlook.</span></span> <span data-ttu-id="a387f-107">La stratégie de liste de gestion des compléments est incluse dans les fichiers de modèles d’administration Office pour la console de gestion des stratégies de groupe.</span><span class="sxs-lookup"><span data-stu-id="a387f-107">The Add-in Management List policy is included in the Office administrative template files for the Group Policy Management Console.</span></span> <span data-ttu-id="a387f-108">Il crée une clé de Registre sous \\ stratégies logiciel HKCU \\ \\ Microsoft \\ Office \\ 15,0 \\ Outlook15 \\ résilience \\ AddinList.</span><span class="sxs-lookup"><span data-stu-id="a387f-108">It creates a registry key under HKCU\\Software\\Policies\\Microsoft\\Office\\15.0\\Outlook15\\Resiliency\\AddinList.</span></span> <span data-ttu-id="a387f-109">Vous pouvez ajouter une valeur pour le ucaddin.dll à cette clé et configurer la valeur ucaddin.dll pour qu’elle soit toujours activée et que les utilisateurs ne puissent pas la désactiver manuellement.</span><span class="sxs-lookup"><span data-stu-id="a387f-109">You can add a value for the ucaddin.dll to this key, and configure the ucaddin.dll value so that it is always enabled and so that users cannot manually disable it</span></span>

<div>

## <a name="to-add-ucaddindll-to-the-outlook-add-in-list"></a><span data-ttu-id="a387f-110">Pour ajouter des ucaddin.dll dans la liste des compléments Outlook</span><span class="sxs-lookup"><span data-stu-id="a387f-110">To Add ucaddin.dll to the Outlook Add-in List</span></span>

  - <span data-ttu-id="a387f-111">Pour la clé de Registre AddinList, située sous \\ stratégies logicielles HKCU \\ \\ Microsoft \\ Office \\ 15,0 \\ Outlook15 \\ de résilience \\ AddinList, ajoutez la valeur suivante :</span><span class="sxs-lookup"><span data-stu-id="a387f-111">To the AddinList registry key, located under HKCU\\Software\\Policies\\Microsoft\\Office\\15.0\\Outlook15\\Resiliency\\AddinList, add the following value:</span></span>
    
      - <span data-ttu-id="a387f-112">Type de Registre = \_ St SZ</span><span class="sxs-lookup"><span data-stu-id="a387f-112">Registry Type = REG\_SZ</span></span>
    
      - <span data-ttu-id="a387f-113">Nom = ucaddin.dll</span><span class="sxs-lookup"><span data-stu-id="a387f-113">Name = ucaddin.dll</span></span>
    
      - <span data-ttu-id="a387f-114">Valeur = 1 (indique que le complément est toujours activé et ne peut pas être géré par l’utilisateur final)</span><span class="sxs-lookup"><span data-stu-id="a387f-114">Value = 1 (specifies that the add-in is always enabled and cannot be managed by the end user)</span></span>

<span data-ttu-id="a387f-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a387f-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

