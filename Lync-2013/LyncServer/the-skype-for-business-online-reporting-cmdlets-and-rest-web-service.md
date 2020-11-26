---
title: Cmdlets de création de rapports Skype entreprise Online et service Web REST
description: Cmdlets de création de rapports Skype entreprise Online et service Web REST.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: The Skype for Business Online reporting cmdlets and REST web service
ms:assetid: cadd73a7-c08a-4102-b73a-ccb3ad4987bf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362845(v=OCS.15)
ms:contentKeyID: 56563409
ms.date: 05/04/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f2160e0910d42f811ec8b03fa50450d5f73c59b1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423406"
---
# <a name="the-skype-for-business-online-reporting-cmdlets-and-rest-web-service"></a><span data-ttu-id="6cbde-103">Cmdlets de création de rapports Skype entreprise Online et service Web REST</span><span class="sxs-lookup"><span data-stu-id="6cbde-103">The Skype for Business Online reporting cmdlets and REST web service</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6cbde-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6cbde-104">

<span> </span></span></span>

<span data-ttu-id="6cbde-105">_**Dernière modification de la rubrique :** 2014-09-05_</span><span class="sxs-lookup"><span data-stu-id="6cbde-105">_**Topic Last Modified:** 2014-09-05_</span></span>

<span data-ttu-id="6cbde-106">Outre les fonctionnalités de création de rapports, Skype entreprise Online fournit l’accès à cinq cmdlets Windows PowerShell pour générer ces rapports et peut également être utilisé par les administrateurs pour retourner des données de rapport personnalisées.</span><span class="sxs-lookup"><span data-stu-id="6cbde-106">In conjunction with the reporting features, Skype for Business Online provides access to five Windows PowerShell cmdlets that help generate those reports and are also can be used by administrators to return customized reporting data.</span></span> <span data-ttu-id="6cbde-107">Skype entreprise Online inclut également le reste (le transfert d’état de la présentation), qui peut être utilisé par les développeurs pour récupérer des informations de rapport personnalisées.</span><span class="sxs-lookup"><span data-stu-id="6cbde-107">Skype for Business Online also includes the REST (Representational State Transfer), which can be used by developers to retrieve customized reporting information.</span></span>

<span data-ttu-id="6cbde-108">Les applets de création de rapports disponibles aux administrateurs sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="6cbde-108">The reporting cmdlets available to administrators include:</span></span>

  - <span data-ttu-id="6cbde-109">Get-CsActiveUserReport, qui fournit des informations sur le nombre d’utilisateurs actifs (c’est-à-dire les utilisateurs qui se sont connectés à Skype entreprise Online et ayant participé à au moins une conférence ou une session d’égal à égal).</span><span class="sxs-lookup"><span data-stu-id="6cbde-109">Get-CsActiveUserReport, which provides information about the number of active users (that is, users who have logged on to Skype for Business Online and participated in at least one conference or peer-to-peer communication session).</span></span>

  - <span data-ttu-id="6cbde-110">Get-CsAVConferenceTimeReport, qui fournit des informations sur la durée (en minutes) des utilisateurs qui ont passé dans les conférences audio/vidéo.</span><span class="sxs-lookup"><span data-stu-id="6cbde-110">Get-CsAVConferenceTimeReport, which provides information about the amount of time (in minutes) users spent in audio/video conferences.</span></span>

  - <span data-ttu-id="6cbde-111">Get-CsConferenceReport, qui fournit des informations sur le nombre et le type de conférences auxquelles les utilisateurs ont participé.</span><span class="sxs-lookup"><span data-stu-id="6cbde-111">Get-CsConferenceReport, which provides information about the number and type of conferences that users participated in.</span></span>

  - <span data-ttu-id="6cbde-112">Get-CsP2PAVTimeReport, qui fournit des informations sur le délai (en minutes) passé aux utilisateurs dans des sessions d’égal à égal incluant des contenus audio et/ou vidéo.</span><span class="sxs-lookup"><span data-stu-id="6cbde-112">Get-CsP2PAVTimeReport, which provides information about the amount of time (in minutes) users spent in peer-to-peer sessions that included audio and/or video.</span></span>

  - <span data-ttu-id="6cbde-113">Get-CsP2PSessionReport, qui fournit des informations sur le nombre et le type de sessions d’égal à égal auxquelles l’utilisateur a participé.</span><span class="sxs-lookup"><span data-stu-id="6cbde-113">Get-CsP2PSessionReport, which provides information about the number and type of peer-to-peer sessions that users participated in.</span></span>

<span data-ttu-id="6cbde-114">La plupart des administrateurs utiliseront les rapports disponibles dans le centre d’administration 365 de Microsoft : pas seulement les rapports générés automatiquement, mais ils fournissent également une représentation graphique des données qui est souvent plus facile à interpréter que les valeurs de nombre brut renvoyées par les applets de fonction de création de rapports.</span><span class="sxs-lookup"><span data-stu-id="6cbde-114">Most administrators will use the reports available in the Microsoft 365 admin center: not only are those reports auto-generated, but they also provide a graphical representation of the data that is often easier to interpret than the raw number values returned by the reporting cmdlets.</span></span> <span data-ttu-id="6cbde-115">Toutefois, les administrateurs habitués à Windows PowerShell peuvent utiliser les applets de applet de création de rapports pour renvoyer des données qui ne sont pas facilement disponibles dans les rapports Lync Online.</span><span class="sxs-lookup"><span data-stu-id="6cbde-115">However, administrators familiar with Windows PowerShell can use the reporting cmdlets to return data that is not readily available from the Lync Online reports.</span></span> <span data-ttu-id="6cbde-116">Par exemple, les applets de l’applet de création de rapports renvoient des informations sur la durée de la session (le temps, en minutes, de la date de fin de chaque session).</span><span class="sxs-lookup"><span data-stu-id="6cbde-116">For example, the reporting cmdlets return information about session duration (the amount of time, in minutes, that each session lasted).</span></span> <span data-ttu-id="6cbde-117">Les durées de session individuelles ne sont pas disponibles dans les rapports Lync Online.</span><span class="sxs-lookup"><span data-stu-id="6cbde-117">Individual session durations are not available using the Lync Online reports.</span></span> <span data-ttu-id="6cbde-118">De même, dans l’affichage quotidien, les rapports Lync Online affichent uniquement les informations relatives aux 14 jours précédents.</span><span class="sxs-lookup"><span data-stu-id="6cbde-118">Likewise, in daily view the Lync Online reports display information only for the preceding 14 days.</span></span> <span data-ttu-id="6cbde-119">Si vous voulez passer en revue le total quotidien d’un autre jour (par exemple, une date de quatre mois auparavant), vous pouvez utiliser les applets de contrôle de création de rapports.</span><span class="sxs-lookup"><span data-stu-id="6cbde-119">If you would like to review the daily totals for a different day (for example, a date from four months ago) you can do so by using the reporting cmdlets.</span></span>

<span data-ttu-id="6cbde-120">Les administrateurs peuvent également être intéressés par l’article [qui utilise Excel pour récupérer les données de rapport d’office 365](https://msdn.microsoft.com/library/dn781442.aspx), qui explique comment utiliser la fonctionnalité de requête de données OData dans Microsoft Excel pour créer un rapport Office 365 personnalisé.</span><span class="sxs-lookup"><span data-stu-id="6cbde-120">Administrators might also be interested in the article [Using Excel to Retrieve Office 365 Reporting Data](https://msdn.microsoft.com/library/dn781442.aspx), which explains how to use the OData data querying feature in Microsoft Excel to create custom office 365 report.</span></span> <span data-ttu-id="6cbde-121">Les rapports personnalisés vous permettent de dicter les données qui sont renvoyées par le service de création de rapports d’Office 365.</span><span class="sxs-lookup"><span data-stu-id="6cbde-121">Custom reports give you the ability to dictate which data (and how much data) is returned from the Office 365 reporting service.</span></span> <span data-ttu-id="6cbde-122">Les rapports personnalisés vous permettent également de procéder de la sorte en spécifiant la manière dont les données doivent être triées et regroupées et permettent d’accéder à des informations qui ne sont pas affichées dans le centre d’administration.</span><span class="sxs-lookup"><span data-stu-id="6cbde-122">Custom reports also enable you to do such things as specify how the data should be sorted and grouped, and provide access to information that is not displayed in the admin center.</span></span>

<span data-ttu-id="6cbde-123">Les administrateurs possédant un arrière-plan de développement peuvent utiliser le service Web REST pour obtenir des informations qui ne sont pas affichées dans le centre d’administration de Skype entreprise online.</span><span class="sxs-lookup"><span data-stu-id="6cbde-123">Administrators with a development background can use the REST web service to obtain information not displayed in the Skype for Business Online admin center.</span></span> <span data-ttu-id="6cbde-124">Le service REST est semblable au service SOAP, car chaque technologie fournit un moyen de transférer des données XML entre un client et un serveur.</span><span class="sxs-lookup"><span data-stu-id="6cbde-124">The REST service is similar to the SOAP service, in that each technology provides a way to transfer XML data between a client and a server.</span></span> <span data-ttu-id="6cbde-125">Toutefois, le service REST a au moins deux avantages par rapport au service SOAP.</span><span class="sxs-lookup"><span data-stu-id="6cbde-125">However, the REST service has at least two advantages over the SOAP service.</span></span> <span data-ttu-id="6cbde-126">Pour un, REST effectue des transferts de données XML à l’aide d’un format normalisé connu sous le nom de syndication ATOM.</span><span class="sxs-lookup"><span data-stu-id="6cbde-126">For one, REST performs XML data transfers using a standardized format known as the ATOM syndication format.</span></span> <span data-ttu-id="6cbde-127">En revanche, le protocole SOAP utilise un format non standard lors du transfert de données.</span><span class="sxs-lookup"><span data-stu-id="6cbde-127">By contrast, SOAP using a non-standard format when transferring data.</span></span> <span data-ttu-id="6cbde-128">De plus, le REST est en mesure de transférer des données entre des réseaux qui bloquent les verbes HTTP autres que GET et POST.</span><span class="sxs-lookup"><span data-stu-id="6cbde-128">In addition, REST is able to transfer data across networks that block HTTP verbs other than GET and POST.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="6cbde-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6cbde-129">See Also</span></span>


<span data-ttu-id="6cbde-130">[Rapports Lync Online](https://technet.microsoft.com/library/dn362827\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="6cbde-130">[Lync Online reporting](https://technet.microsoft.com/library/dn362827\(v=ocs.15\))</span></span>  


[<span data-ttu-id="6cbde-131">Service Web de création de rapports Office 365</span><span class="sxs-lookup"><span data-stu-id="6cbde-131">The Office 365 Reporting Web Service</span></span>](https://msdn.microsoft.com/library/office/jj984325.aspx)  
[<span data-ttu-id="6cbde-132">Découvrir le service Web de création de rapports d’Office 365</span><span class="sxs-lookup"><span data-stu-id="6cbde-132">Learning About the Office 365 Reporting Web Service</span></span>](https://msdn.microsoft.com/library/office/jj984321.aspx)  
<span data-ttu-id="6cbde-133">[Cmdlets de rapport Exchange Online](https://technet.microsoft.com/library/jj200780\(v=exchg.150\).aspx)</span><span class="sxs-lookup"><span data-stu-id="6cbde-133">[The Exchange Online Reporting Cmdlets](https://technet.microsoft.com/library/jj200780\(v=exchg.150\).aspx)</span></span>  
[<span data-ttu-id="6cbde-134">Utiliser Excel pour récupérer les données de rapport d’Office 365</span><span class="sxs-lookup"><span data-stu-id="6cbde-134">Using Excel to Retrieve Office 365 Reporting Data</span></span>](https://msdn.microsoft.com/library/dn781442.aspx)  
  

<span data-ttu-id="6cbde-135"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6cbde-135"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

