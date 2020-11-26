---
title: 'Lync Server 2013 : Définition de règles de normalisation'
description: 'Lync Server 2013 : définition des règles de normalisation.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Defining normalization rules
ms:assetid: ed31d56c-00b5-4f72-bd9f-beb4100d441f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399071(v=OCS.15)
ms:contentKeyID: 48185741
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3a123e17b1d3256781ff34e4cade2b344ba8fe14
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430993"
---
# <a name="defining-normalization-rules-in-lync-server-2013"></a><span data-ttu-id="785d1-103">Définition de règles de normalisation dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="785d1-103">Defining normalization rules in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="785d1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="785d1-104">

<span> </span></span></span>

<span data-ttu-id="785d1-105">_**Dernière modification de la rubrique :** 2014-04-22_</span><span class="sxs-lookup"><span data-stu-id="785d1-105">_**Topic Last Modified:** 2014-04-22_</span></span>

<span data-ttu-id="785d1-106">Les règles de normalisation de Lync Server 2013 utilisent des expressions régulières du .NET Framework pour convertir les numéros de téléphone numérotés au format E. 164. en d’autres termes, les règles de normalisation emportent le numéro de téléphone composé par un utilisateur et convertissent ce numéro au format utilisé en interne par Lync Server.</span><span class="sxs-lookup"><span data-stu-id="785d1-106">Lync Server 2013 normalization rules use .NET Framework regular expressions to translate dialed phone numbers to E.164 format; in other words, normalization rules take the phone number dialed by a user and convert that number to the format used internally by Lync Server.</span></span> <span data-ttu-id="785d1-107">Une ou plusieurs règles de normalisation doivent être affectées à chaque plan de numérotation.</span><span class="sxs-lookup"><span data-stu-id="785d1-107">Each dial plan must be assigned one or more normalization rules.</span></span>

<span data-ttu-id="785d1-108">Pour plus d’informations sur les règles de normalisation, voir [plans de numérotation et règles de normalisation dans Lync Server 2013](lync-server-2013-dial-plans-and-normalization-rules.md) dans la documentation de planification.</span><span class="sxs-lookup"><span data-stu-id="785d1-108">For details about normalization rules, see [Dial plans and normalization rules in Lync Server 2013](lync-server-2013-dial-plans-and-normalization-rules.md) in the Planning documentation.</span></span>

<span data-ttu-id="785d1-109">Pour plus d’informations sur la façon d’écrire des expressions régulières, voir « expressions régulières .NET Framework » à l’adresse [https://go.microsoft.com/fwlink/p/?linkId=140927](https://go.microsoft.com/fwlink/p/?linkid=140927) .</span><span class="sxs-lookup"><span data-stu-id="785d1-109">For details about how to write regular expressions, see ".NET Framework Regular Expressions" at [https://go.microsoft.com/fwlink/p/?linkId=140927](https://go.microsoft.com/fwlink/p/?linkid=140927).</span></span>

<span data-ttu-id="785d1-110">Pour définir ou modifier une règle de normalisation, vous pouvez utiliser l’une des méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="785d1-110">You can use either of the following methods to define or edit a normalization rule:</span></span>

  - <span data-ttu-id="785d1-111">Utiliser l’outil **créer une règle de normalisation** pour spécifier des valeurs pour les chiffres de début, la longueur, les chiffres à supprimer et les chiffres à ajouter, puis laisser le panneau de configuration de Lync Server générer le modèle correspondant et la règle de traduction correspondants.</span><span class="sxs-lookup"><span data-stu-id="785d1-111">Use the **Build a Normalization Rule** tool to specify values for the starting digits, length, digits to remove and digits to add, and then let Lync Server Control Panel generate the corresponding matching pattern and translation rule for you.</span></span>

  - <span data-ttu-id="785d1-112">Rédigez manuellement des expressions régulières pour définir les modèles correspondants et les règles de traduction.</span><span class="sxs-lookup"><span data-stu-id="785d1-112">Write regular expressions manually to define the matching pattern and translation rule.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="785d1-113">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="785d1-113">In This Section</span></span>

  - [<span data-ttu-id="785d1-114">Créer ou modifier une règle de normalisation à l’aide de l’application créer une règle de normalisation dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="785d1-114">Create or modify a normalization rule by using Build a Normalization Rule in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-normalization-rule-by-using-build-a-normalization-rule.md)

  - [<span data-ttu-id="785d1-115">Création ou modification manuelle d’une règle de normalisation dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="785d1-115">Create or modify a normalization rule manually in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-normalization-rule-manually.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="785d1-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="785d1-116">See Also</span></span>


[<span data-ttu-id="785d1-117">Créer un plan de numérotation dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="785d1-117">Create a dial plan in Lync Server 2013</span></span>](lync-server-2013-create-a-dial-plan.md)  
[<span data-ttu-id="785d1-118">Modification d’un plan de numérotation dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="785d1-118">Modify a dial plan in Lync Server 2013</span></span>](lync-server-2013-modify-a-dial-plan.md)  
  

<span data-ttu-id="785d1-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="785d1-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

