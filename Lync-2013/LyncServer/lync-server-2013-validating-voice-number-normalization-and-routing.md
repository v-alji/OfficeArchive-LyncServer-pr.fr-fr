---
title: 'Lync Server 2013 : validation de la normalisation et du routage des numéros vocaux'
description: 'Lync Server 2013 : validation de la normalisation et du routage des numéros vocaux.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Validating voice number normalization and routing
ms:assetid: a6a825c7-6928-4e80-b7e9-803b7f7ebd13
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720922(v=OCS.15)
ms:contentKeyID: 63969633
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5f28f679cbb991bdb90362eb61c9c7b68879791e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438623"
---
# <a name="validating-voice-number-normalization-and-routing-in-lync-server-2013"></a><span data-ttu-id="0e4c1-103">Validation de la normalisation et du routage des numéros vocaux dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0e4c1-103">Validating voice number normalization and routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0e4c1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0e4c1-104">

<span> </span></span></span>

<span data-ttu-id="0e4c1-105">_**Dernière modification de la rubrique :** 2014-05-19_</span><span class="sxs-lookup"><span data-stu-id="0e4c1-105">_**Topic Last Modified:** 2014-05-19_</span></span>

<span data-ttu-id="0e4c1-106">Le bon fonctionnement de la normalisation et du routage des numéros est essentiel pour l’environnement d’entreprise voix.</span><span class="sxs-lookup"><span data-stu-id="0e4c1-106">Correct number normalization and routing is very important for functional Enterprise Voice environment.</span></span> <span data-ttu-id="0e4c1-107">En particulier lors des migrations du système PBX vers un environnement Lync Server autonome, l’une des clés de la migration réussie consiste à afficher et à documenter toutes les règles de numérotation existantes, et à créer des règles de normalisation appropriées, des politiques vocales, des utilisations de téléphone et des itinéraires.</span><span class="sxs-lookup"><span data-stu-id="0e4c1-107">Especially during migrations from private branch exchange (PBX) to stand-alone Lync Server environment, one of the keys to successful migration is to reveal and document all existing dialing rules, and create appropriate normalization rules, voice policies, phone usages and routes.</span></span>

<span data-ttu-id="0e4c1-108">La validation de la normalisation et de l’acheminement des numéros est important non seulement pendant les migrations, mais également dans le cadre du fonctionnement normal et stable du système.</span><span class="sxs-lookup"><span data-stu-id="0e4c1-108">Validating number normalization and routing is important not only during migrations but also during normal, stable operation of the system.</span></span>

<span data-ttu-id="0e4c1-109">Nous vous recommandons d’effectuer cette validation quotidiennement en utilisant le panneau de configuration de Lync Server, en commençant par le développement d’un ensemble de scénarios de test puissants par rapport à l’ensemble actuel de règles de normalisation publiées dans les paramètres globaux de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="0e4c1-109">We recommend conducting this validation daily by using the Lync Server Control Panel, starting with developing a robust set of test cases against the current set of normalization rules that were published in the Lync Server global settings.</span></span> <span data-ttu-id="0e4c1-110">Ces cas de test doivent être exécutés quotidiennement pour mettre en évidence les modifications indésirables apportées et validées au plan de numérotation.</span><span class="sxs-lookup"><span data-stu-id="0e4c1-110">These test cases should be run daily to highlight any unwanted changes that were made and committed to the dial plan.</span></span>

<span data-ttu-id="0e4c1-111">Le panneau de configuration de Lync Server vous permet également de visualiser, de tester, de modifier, d’archiver et de partager des informations de configuration sur le routage de la voix et de modifier les règles de normalisation des numéros vocaux d’entreprise, les plans de numérotation, la politique vocale et les itinéraires.</span><span class="sxs-lookup"><span data-stu-id="0e4c1-111">Lync Server Control Panel also helps you visualize, test, change, archive, and share configuration information about voice routing and in changing Enterprise Voice number normalization rules, dial plans, voice policy, and routes.</span></span> <span data-ttu-id="0e4c1-112">Les fonctionnalités suivantes sont disponibles pour effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="0e4c1-112">It has additional features for doing the following:</span></span>

  - <span data-ttu-id="0e4c1-113">Exportation et importation ou sauvegarde de données de routage de la voix entre systèmes ;</span><span class="sxs-lookup"><span data-stu-id="0e4c1-113">Exporting and importing or backing up voice routing data between systems.</span></span>

  - <span data-ttu-id="0e4c1-114">Test de la configuration avant de les télécharger sur un système en direct.</span><span class="sxs-lookup"><span data-stu-id="0e4c1-114">Testing configuration changes before uploading them to a live system.</span></span>

  - <span data-ttu-id="0e4c1-115">Création et exécution de cas de test de configuration pour garantir la facilité d’utilisation du routage des données après avoir apporté des modifications à celui-ci, mais avant de les valider.</span><span class="sxs-lookup"><span data-stu-id="0e4c1-115">Creating and running configuration test cases to help ensure the usability of routing data after you make changes to it, but before committing them the changes to a deployed system.</span></span>

  - <span data-ttu-id="0e4c1-116">La création et la modification des règles de normalisation des numéros, des profils d’emplacement, de la stratégie vocale et des données de routage sans écrire les expressions régulières nécessaires.</span><span class="sxs-lookup"><span data-stu-id="0e4c1-116">Creating and changing number normalization rules, location profiles, voice policy, and routing data without writing the necessary regular expressions.</span></span>

  - <span data-ttu-id="0e4c1-117">Analyse d’un profil d’emplacement à des fins de compatibilité avec Lync Server Phone Edition.</span><span class="sxs-lookup"><span data-stu-id="0e4c1-117">Analyzing a location profile for compatibility with the Lync Server Phone Edition.</span></span>

  - <span data-ttu-id="0e4c1-118">Vous trouverez des informations supplémentaires sur les tests de routage [de voix dans la boîte de test routage de la voix dans Lync Server 2013](lync-server-2013-test-voice-routing.md)</span><span class="sxs-lookup"><span data-stu-id="0e4c1-118">More information about voice routing tests can be found at [Test voice routing in Lync Server 2013](lync-server-2013-test-voice-routing.md)</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="0e4c1-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e4c1-119">See Also</span></span>


[<span data-ttu-id="0e4c1-120">Test du routage des communications vocales dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0e4c1-120">Test voice routing in Lync Server 2013</span></span>](lync-server-2013-test-voice-routing.md)  
  

<span data-ttu-id="0e4c1-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0e4c1-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

