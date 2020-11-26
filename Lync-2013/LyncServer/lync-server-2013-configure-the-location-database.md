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
# <a name="configure-the-location-database-in-lync-server-2013"></a><span data-ttu-id="6f45b-103">Configure the location database in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6f45b-103">Configure the location database in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6f45b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6f45b-104">

<span> </span></span></span>

<span data-ttu-id="6f45b-105">_**Dernière modification de la rubrique :** 2012-09-17_</span><span class="sxs-lookup"><span data-stu-id="6f45b-105">_**Topic Last Modified:** 2012-09-17_</span></span>

<span data-ttu-id="6f45b-106">Pour permettre aux clients de détecter automatiquement leur emplacement au sein d’un réseau, vous devez d’abord configurer la base de données d’emplacements.</span><span class="sxs-lookup"><span data-stu-id="6f45b-106">To enable clients to automatically detect their location within a network, you first need to configure the location database.</span></span> <span data-ttu-id="6f45b-107">Si vous ne configurez pas de base de données de géolocalisation **et que** la stratégie d’emplacement est définie sur **Oui** ou **exclusion de responsabilité**, l’utilisateur est invité à entrer manuellement un emplacement.</span><span class="sxs-lookup"><span data-stu-id="6f45b-107">If you do not configure a location database, and **Location Required** in the location policy is set to **Yes** or **Disclaimer**, the user will be prompted to manually enter a location.</span></span>

<span data-ttu-id="6f45b-108">Pour configurer la base de données de localisation, vous devez effectuer les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="6f45b-108">To configure the location database, you will perform the following tasks:</span></span>

1.  <span data-ttu-id="6f45b-109">Remplissez la base de données avec une correspondance des éléments réseau avec les emplacements.</span><span class="sxs-lookup"><span data-stu-id="6f45b-109">Populate the database with a mapping of network elements to locations.</span></span> <span data-ttu-id="6f45b-110">Si vous utilisez une passerelle ELIN), vous devez inclure la ELIN dans le \<CompanyName\> champ.</span><span class="sxs-lookup"><span data-stu-id="6f45b-110">If you use an Emergency Location Identification Number (ELIN) gateway, you need to include the ELIN in the \<CompanyName\> field.</span></span>

2.  <span data-ttu-id="6f45b-111">Validez les adresses par rapport à la base de données MSAG gérée par le fournisseur de service E9-1-1.</span><span class="sxs-lookup"><span data-stu-id="6f45b-111">Validate the addresses against the master street address guide (MSAG) that is maintained by the E9-1-1 service provider.</span></span>

3.  <span data-ttu-id="6f45b-112">Publiez la base de données mise à jour.</span><span class="sxs-lookup"><span data-stu-id="6f45b-112">Publish the updated database.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="6f45b-113">Vous pouvez également définir une base de données source de emplacement secondaire qui peut être utilisée dans l’emplacement de la base de données de localisation.</span><span class="sxs-lookup"><span data-stu-id="6f45b-113">Alternately, you can define a secondary location source database that can be used in placed of the location database.</span></span> <span data-ttu-id="6f45b-114">Pour plus d’informations, voir <A href="lync-server-2013-configure-a-secondary-location-information-service.md">configurer un service d’information d’emplacement secondaire dans Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="6f45b-114">For details, see <A href="lync-server-2013-configure-a-secondary-location-information-service.md">Configure a secondary Location Information service in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="6f45b-115">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="6f45b-115">In This Section</span></span>

  - [<span data-ttu-id="6f45b-116">Peupler la base de données de localisation dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6f45b-116">Populate the location database in Lync Server 2013</span></span>](lync-server-2013-populate-the-location-database.md)

  - [<span data-ttu-id="6f45b-117">Valider des adresses dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6f45b-117">Validate addresses in Lync Server 2013</span></span>](lync-server-2013-validate-addresses.md)

  - [<span data-ttu-id="6f45b-118">Publier la base de données de localisation à partir de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6f45b-118">Publish the location database from Lync Server 2013</span></span>](lync-server-2013-publish-the-location-database.md)

<span data-ttu-id="6f45b-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6f45b-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

