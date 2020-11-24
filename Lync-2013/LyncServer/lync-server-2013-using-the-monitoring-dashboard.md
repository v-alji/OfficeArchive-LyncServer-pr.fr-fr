---
title: 'Lync Server 2013 : utilisation du tableau de bord de surveillance'
description: 'Lync Server 2013 : utilisation du tableau de bord de surveillance.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Using the Monitoring Dashboard
ms:assetid: e00e5783-116f-481f-ad17-3af847d6769a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721905(v=OCS.15)
ms:contentKeyID: 49733839
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e8a68fa1e55b7d0b8305c53802ddabaa904fa214
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395277"
---
# <a name="using-the-monitoring-dashboard-in-lync-server-2013"></a><span data-ttu-id="4826b-103">Utiliser le tableau de bord de surveillance dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4826b-103">Using the Monitoring Dashboard in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4826b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4826b-104">

<span> </span></span></span>

<span data-ttu-id="4826b-105">_**Dernière modification de la rubrique :** 2014-02-05_</span><span class="sxs-lookup"><span data-stu-id="4826b-105">_**Topic Last Modified:** 2014-02-05_</span></span>

<span data-ttu-id="4826b-106">Le tableau de bord de suivi fournit aux administrateurs un aperçu rapide de leur état d’intégrité système et de l’utilisation du système Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="4826b-106">The Monitoring Dashboard provides administrators with a quick overview of their Microsoft Lync Server 2013 system health and system usage.</span></span> <span data-ttu-id="4826b-107">Le tableau de bord est conçu pour afficher une vue agrégée des mesures système clés, et ce en affichant soit :</span><span class="sxs-lookup"><span data-stu-id="4826b-107">The Dashboard is designed to show an aggregate view of key system metrics and to do so by displaying either:</span></span>

  - <span data-ttu-id="4826b-p102">Les totaux du jour. Notez que les valeurs affichées pour le jour actuel représentent les données enregistrées de minuit à l’heure actuelle (sur la base de l’heure locale du serveur de rapports). Par conséquent, vous ne verrez que les données d’un jour partiel et non d’une période de 24 heures. Par exemple, si l’heure locale du serveur est 8:00, les données sur huit heures sont affichées, correspondant à la durée entre minuit et l’heure actuelle.</span><span class="sxs-lookup"><span data-stu-id="4826b-p102">Totals for the current day. Note that values shown for the current day represent data that has been recorded from midnight until the current time (based on the local time of the reporting server). That means that you will typically be viewing data for a partial day and not for a 24-hour period. For example, if the local time of the server is 8:00 AM, you see eight hours’ worth of data because there are eight hours between midnight and the current time of 8:00 AM.</span></span>

  - <span data-ttu-id="4826b-112">Les totaux de la semaine, et les totaux de la tendance des six semaines précédentes.</span><span class="sxs-lookup"><span data-stu-id="4826b-112">Totals for the week, and trend totals for the past six weeks.</span></span>

  - <span data-ttu-id="4826b-113">Les totaux du mois, et les totaux de la tendance des six mois précédents (pour l’utilisation du système uniquement).</span><span class="sxs-lookup"><span data-stu-id="4826b-113">Totals for the month, and trend totals for the past six months (for system usage only).</span></span>

<span data-ttu-id="4826b-114">Notez que vous pouvez utiliser l’applet de contrôle [Get-CsReportingConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsReportingConfiguration) pour renvoyer l’URL utilisée pour accéder aux rapports d’analyse Lync Server 2013 :</span><span class="sxs-lookup"><span data-stu-id="4826b-114">Note that you can use the [Get-CsReportingConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsReportingConfiguration) cmdlet to return the URL used for accessing Lync Server 2013 Monitoring Reports:</span></span>

    Get-CsReportingConfiguration

<span data-ttu-id="4826b-115">Par défaut, le Tableau de bord de suivi affiche les données des mesures suivantes pour la semaine en cours (et les totaux de la tendance des six semaines précédentes) :</span><span class="sxs-lookup"><span data-stu-id="4826b-115">By default, the Monitoring Dashboard shows data for the following metrics for the current week (and trend totals for the previous six weeks):</span></span>

<div>

## <a name="system-usage-metrics"></a><span data-ttu-id="4826b-116">Mesures d’utilisation du système</span><span class="sxs-lookup"><span data-stu-id="4826b-116">System Usage Metrics</span></span>

<span data-ttu-id="4826b-117">**Enregistrement**</span><span class="sxs-lookup"><span data-stu-id="4826b-117">**Registration**</span></span>

  - <span data-ttu-id="4826b-118">Ouvertures de sessions à utilisateur unique</span><span class="sxs-lookup"><span data-stu-id="4826b-118">Unique user logons</span></span>

<span data-ttu-id="4826b-119">**Égal à égal**</span><span class="sxs-lookup"><span data-stu-id="4826b-119">**Peer-to-peer**</span></span>

  - <span data-ttu-id="4826b-120">Nombre total de sessions</span><span class="sxs-lookup"><span data-stu-id="4826b-120">Total sessions</span></span>

  - <span data-ttu-id="4826b-121">Sessions de messagerie instantanée</span><span class="sxs-lookup"><span data-stu-id="4826b-121">IM sessions</span></span>

  - <span data-ttu-id="4826b-122">Sessions audio</span><span class="sxs-lookup"><span data-stu-id="4826b-122">Audio sessions</span></span>

  - <span data-ttu-id="4826b-123">Sessions vidéo</span><span class="sxs-lookup"><span data-stu-id="4826b-123">Video sessions</span></span>

  - <span data-ttu-id="4826b-124">Partage d’application</span><span class="sxs-lookup"><span data-stu-id="4826b-124">Application sharing</span></span>

  - <span data-ttu-id="4826b-125">Nombre total de minutes de session audio</span><span class="sxs-lookup"><span data-stu-id="4826b-125">Total audio session minutes</span></span>

  - <span data-ttu-id="4826b-126">Nombre moyen de minutes de session audio</span><span class="sxs-lookup"><span data-stu-id="4826b-126">Avg. audio session minutes</span></span>

<span data-ttu-id="4826b-127">**Conférence**</span><span class="sxs-lookup"><span data-stu-id="4826b-127">**Conference**</span></span>

  - <span data-ttu-id="4826b-128">Nombre total de conférences</span><span class="sxs-lookup"><span data-stu-id="4826b-128">Total conferences</span></span>

  - <span data-ttu-id="4826b-129">Conférences par messagerie instantanée</span><span class="sxs-lookup"><span data-stu-id="4826b-129">IM conferences</span></span>

  - <span data-ttu-id="4826b-130">Conférences A/V</span><span class="sxs-lookup"><span data-stu-id="4826b-130">A/V conferences</span></span>

  - <span data-ttu-id="4826b-131">Conférences de partage d’application</span><span class="sxs-lookup"><span data-stu-id="4826b-131">Application sharing conferences</span></span>

  - <span data-ttu-id="4826b-132">Conférences web</span><span class="sxs-lookup"><span data-stu-id="4826b-132">Web conferences</span></span>

  - <span data-ttu-id="4826b-133">Nombre total d’organisateurs</span><span class="sxs-lookup"><span data-stu-id="4826b-133">Total organizers</span></span>

  - <span data-ttu-id="4826b-134">Nombre total de minutes par conférence A/V</span><span class="sxs-lookup"><span data-stu-id="4826b-134">Total A/V conference minutes</span></span>

  - <span data-ttu-id="4826b-135">Nombre moyen de minutes par conférence A/V</span><span class="sxs-lookup"><span data-stu-id="4826b-135">Avg. A/V conference minutes</span></span>

  - <span data-ttu-id="4826b-136">Nombre total de conférences RTC</span><span class="sxs-lookup"><span data-stu-id="4826b-136">Total PSTN conferences</span></span>

  - <span data-ttu-id="4826b-137">Nombre total de participants RTC</span><span class="sxs-lookup"><span data-stu-id="4826b-137">Total PSTN participants</span></span>

  - <span data-ttu-id="4826b-138">Nombre total de minutes par participant RTC</span><span class="sxs-lookup"><span data-stu-id="4826b-138">Total PSTN participant minutes</span></span>

<span data-ttu-id="4826b-139">Outre les mesures d’utilisation du système, les mesures suivantes indiquent le total pour le jour actuel et les six jours précédents (si vous sélectionnez **Vue hebdomadaire**), ou pour la semaine en cours et les six semaines précédentes si vous sélectionnez **Vue mensuelle**.</span><span class="sxs-lookup"><span data-stu-id="4826b-139">In addition to the System Usage metrics, the following metrics displays total for the current day and the previous six days (if you select **Weekly View**) or for the current week and the past six weeks if you select **Monthly View**.</span></span>

</div>

<div>

## <a name="per-user-call-diagnostics"></a><span data-ttu-id="4826b-140">Diagnostics des appels par utilisateur</span><span class="sxs-lookup"><span data-stu-id="4826b-140">Per-User Call Diagnostics</span></span>

<span data-ttu-id="4826b-141">**Utilisateurs ayant rencontré des problèmes d’appel**</span><span class="sxs-lookup"><span data-stu-id="4826b-141">**Users with call failures**</span></span>

  - <span data-ttu-id="4826b-142">Nombre total d’utilisateurs ayant rencontré des problèmes d’appel</span><span class="sxs-lookup"><span data-stu-id="4826b-142">Total users with call failures</span></span>

  - <span data-ttu-id="4826b-143">Organisateurs de conférence ayant rencontré des problèmes d’appel</span><span class="sxs-lookup"><span data-stu-id="4826b-143">Conference organizers with call failures</span></span>

<span data-ttu-id="4826b-144">**Utilisateurs ayant eu des appels de qualité médiocre**</span><span class="sxs-lookup"><span data-stu-id="4826b-144">**Users with poor quality calls**</span></span>

  - <span data-ttu-id="4826b-145">Nombre total d’utilisateurs ayant eu des appels de qualité médiocre</span><span class="sxs-lookup"><span data-stu-id="4826b-145">Total users with poor quality calls</span></span>

</div>

<div>

## <a name="call-diagnostics"></a><span data-ttu-id="4826b-146">Diagnostics des appels</span><span class="sxs-lookup"><span data-stu-id="4826b-146">Call Diagnostics</span></span>

<span data-ttu-id="4826b-147">Égal à égal</span><span class="sxs-lookup"><span data-stu-id="4826b-147">Peer-to-peer</span></span>

  - <span data-ttu-id="4826b-148">Nombre total d’échecs</span><span class="sxs-lookup"><span data-stu-id="4826b-148">Total failures</span></span>

  - <span data-ttu-id="4826b-149">Taux d’échec global</span><span class="sxs-lookup"><span data-stu-id="4826b-149">Overall failure rate</span></span>

  - <span data-ttu-id="4826b-150">Taux d’échec de la messagerie instantanée</span><span class="sxs-lookup"><span data-stu-id="4826b-150">IM failure rate</span></span>

  - <span data-ttu-id="4826b-151">Taux d’échec audio</span><span class="sxs-lookup"><span data-stu-id="4826b-151">Audio failure rate</span></span>

  - <span data-ttu-id="4826b-152">Taux d’échec du partage d’application</span><span class="sxs-lookup"><span data-stu-id="4826b-152">Application sharing failure rate</span></span>

<span data-ttu-id="4826b-153">Conférence</span><span class="sxs-lookup"><span data-stu-id="4826b-153">Conference</span></span>

  - <span data-ttu-id="4826b-154">Nombre total d’échecs</span><span class="sxs-lookup"><span data-stu-id="4826b-154">Total failures</span></span>

  - <span data-ttu-id="4826b-155">Taux d’échec global</span><span class="sxs-lookup"><span data-stu-id="4826b-155">Overall failure rate</span></span>

  - <span data-ttu-id="4826b-156">Taux d’échec de la messagerie instantanée</span><span class="sxs-lookup"><span data-stu-id="4826b-156">IM failure rate</span></span>

  - <span data-ttu-id="4826b-157">Taux d’échec A/V</span><span class="sxs-lookup"><span data-stu-id="4826b-157">A/V failure rate</span></span>

  - <span data-ttu-id="4826b-158">Taux d’échec du partage d’application</span><span class="sxs-lookup"><span data-stu-id="4826b-158">Application sharing failure rate</span></span>

<span data-ttu-id="4826b-159">Cinq principaux serveurs par session ayant échoué</span><span class="sxs-lookup"><span data-stu-id="4826b-159">Top five servers by failed sessions</span></span>

</div>

<div>

## <a name="media-quality-diagnostics"></a><span data-ttu-id="4826b-160">Diagnostic de la qualité des médias</span><span class="sxs-lookup"><span data-stu-id="4826b-160">Media Quality Diagnostics</span></span>

<span data-ttu-id="4826b-161">Égal à égal</span><span class="sxs-lookup"><span data-stu-id="4826b-161">Peer-to-peer</span></span>

  - <span data-ttu-id="4826b-162">Nombre total d’appels de qualité médiocre</span><span class="sxs-lookup"><span data-stu-id="4826b-162">Total poor quality calls</span></span>

  - <span data-ttu-id="4826b-163">Pourcentage d’appels de qualité médiocre</span><span class="sxs-lookup"><span data-stu-id="4826b-163">Poor quality call percentage</span></span>

  - <span data-ttu-id="4826b-164">Appels PSTN de qualité médiocre</span><span class="sxs-lookup"><span data-stu-id="4826b-164">PSTN calls with poor quality</span></span>

<span data-ttu-id="4826b-165">Conférence</span><span class="sxs-lookup"><span data-stu-id="4826b-165">Conference</span></span>

  - <span data-ttu-id="4826b-166">Nombre total d’appels de qualité médiocre</span><span class="sxs-lookup"><span data-stu-id="4826b-166">Total poor quality calls</span></span>

  - <span data-ttu-id="4826b-167">Pourcentage d’appels de qualité médiocre</span><span class="sxs-lookup"><span data-stu-id="4826b-167">Poor quality call percentage</span></span>

  - <span data-ttu-id="4826b-168">Appels PSTN de qualité médiocre</span><span class="sxs-lookup"><span data-stu-id="4826b-168">PSTN calls with poor quality</span></span>

<span data-ttu-id="4826b-169">Cinq derniers serveurs par pourcentage d’appels de qualité médiocre</span><span class="sxs-lookup"><span data-stu-id="4826b-169">Top worst servers by poor quality call percentage</span></span>

</div>

<div>

## <a name="working-with-the-monitoring-dashboard"></a><span data-ttu-id="4826b-170">Travail avec le Tableau de bord de suivi</span><span class="sxs-lookup"><span data-stu-id="4826b-170">Working with the Monitoring Dashboard</span></span>

<span data-ttu-id="4826b-p103">Comme mentionné plus haut, les totaux par défaut sont affichés pour la semaine en cours et les valeurs de tendance pour les six semaines précédentes. Si vous préférez voir les totaux pour le mois en cours (ainsi que les valeurs de la tendance sur les six mois précédents), cliquez sur le lien **Vue mensuelle** dans le coin supérieur droit du tableau de bord. Si vous décidez d’afficher les totaux mensuels, le texte du lien devient **Vue hebdomadaire**. Vous pouvez revenir à la vue mensuelle en cliquant dessus.</span><span class="sxs-lookup"><span data-stu-id="4826b-p103">As noted, by default totals are shown for the current week and trend values are shown for the past six weeks. If you would prefer to see totals for the current month (as well as trend values for the past six months), click the **Monthly View** link in the upper right corner of the dashboard. If you decide to view monthly totals, the link text will change to **Weekly View**. You can switch back to the weekly view by clicking that link.</span></span>

<div>


> [!TIP]  
> <span data-ttu-id="4826b-p104">Le Tableau de bord de suivi ne vous permet que de voir les totaux de la semaine (ou du mois) en cours et les valeurs de tendance des six semaines précédentes (ou mois précédents). Vous ne pouvez pas modifier ces dates et périodes. Par exemple, le tableau de bord ne vous permet pas de voir les totaux des rapports pour la période commençant neuf mois plus tôt.</span><span class="sxs-lookup"><span data-stu-id="4826b-p104">The Monitoring Dashboard restricts you to looking at totals for the current week (or month) and trend values for the past six weeks (or months). You cannot change these dates and times. For example, you cannot use the Dashboard to view report totals for the time period beginning nine months ago.</span></span>



</div>

<span data-ttu-id="4826b-p105">Les valeurs affichées dans les colonnes **Cette semaine**, **Ce mois-ci** ou **Aujourd’hui** vous mènent à des informations détaillées sur l’élément. Rappelez-vous que le nom de la colonne et les valeurs qui y sont affichées changent en fonction de la mesure choisie et de votre choix de la vue hebdomadaire ou mensuelle. Par exemple, si vous cliquez sur les totaux affichés pour la mesure **Ouvertures de sessions à utilisateur unique**, vous verrez le **Rapport d’enregistrement de l’utilisateur** pour la période spécifiée. Vous pouvez retourner au Tableau de bord de suivi à tout moment en cliquant sur **Tableau de bord**.</span><span class="sxs-lookup"><span data-stu-id="4826b-p105">The values shown in the **This week**, **This month**, or **Today** columns link you to more detailed information about the item. Keep in mind that the column name and the values displayed in that column will often differ depending on the metric chosen and depending on whether you have selected weekly view or monthly view. For example, if you click the totals shown for the **Unique user logons** metric you will see the **User Registration Report** for the specified time period. You can return to the Monitoring Dashboard at any time by clicking **Dashboard**.</span></span>

<div>


> [!TIP]  
> <span data-ttu-id="4826b-182">Vous pouvez également accéder à la page d’accueil des rapports du serveur de surveillance en cliquant sur le lien <STRONG>rapports</STRONG> dans le coin supérieur droit du tableau de bord.</span><span class="sxs-lookup"><span data-stu-id="4826b-182">You can also access the Monitoring Server Reports home page by clicking the <STRONG>Reports</STRONG> link in the upper right corner of the Dashboard.</span></span>



</div>

<span data-ttu-id="4826b-183">La colonne **Tendance** montre un graphique en courbes indiquant les totaux des six semaines précédentes (ou, selon la mesure et l’intervalle de temps, les six derniers jours ou mois).</span><span class="sxs-lookup"><span data-stu-id="4826b-183">The **Trend** column displays a simple line graph that shows totals for the past six weeks (or, depending on the metric and the time interval, the past six days or the past six months).</span></span> <span data-ttu-id="4826b-184">Ces graphiques en courbes affichent un point de données sans nom pour chaque période (par exemple, un point de données sans nom pour chacune des six semaines précédentes).</span><span class="sxs-lookup"><span data-stu-id="4826b-184">These simple line graphs display one unlabeled data point for each time period (for example, one unlabeled data point for each of the past six weeks).</span></span> <span data-ttu-id="4826b-185">Cependant, vous pouvez récupérer les valeurs réelles pour ces graphiques en maintenant le pointeur de la souris sur le graphique.</span><span class="sxs-lookup"><span data-stu-id="4826b-185">However, you can retrieve actual values for these graphs by holding your mouse pointer over the graph.</span></span> <span data-ttu-id="4826b-186">Dans ce cas, une info-bulle affiche les valeurs maximale et minimale dans le graphique.</span><span class="sxs-lookup"><span data-stu-id="4826b-186">In that case, a tooltip shows you the maximum and minimum values in the graph.</span></span>

</div>

<div>

## <a name="exporting-data-from-the-monitoring-dashboard"></a><span data-ttu-id="4826b-187">Exportation de données à partir du Tableau de bord de suivi</span><span class="sxs-lookup"><span data-stu-id="4826b-187">Exporting Data from the Monitoring Dashboard</span></span>

<span data-ttu-id="4826b-p107">Le Tableau de bord de suivi permet d’exporter la vue en cours de différentes manières. Dans la barre d’outils du tableau de bord se trouve une icône représentant une disquette avec une flèche verte attachée. Si vous cliquez dessus, une liste déroulante avec les formats d’exportation de données suivants apparaît :</span><span class="sxs-lookup"><span data-stu-id="4826b-p107">The Monitoring Dashboard provides a number of ways to export the current dashboard view. On the Dashboard toolbar, you'll see an icon that looks like a floppy disk with a green arrow attached to it. If you click this icon, a dropdown list will appear giving you the following data export formats:</span></span>

  - <span data-ttu-id="4826b-191">fichier XML avec données de rapport ;</span><span class="sxs-lookup"><span data-stu-id="4826b-191">XML file with report data</span></span>

  - <span data-ttu-id="4826b-192">fichier CSV (valeurs séparées par des virgules) ;</span><span class="sxs-lookup"><span data-stu-id="4826b-192">CSV (comma delimited)</span></span>

  - <span data-ttu-id="4826b-193">fichier PDF ;</span><span class="sxs-lookup"><span data-stu-id="4826b-193">PDF</span></span>

  - <span data-ttu-id="4826b-194">fichier MHTML (archive Web) ;</span><span class="sxs-lookup"><span data-stu-id="4826b-194">MHTML (web archive)</span></span>

  - <span data-ttu-id="4826b-195">fichier Excel ;</span><span class="sxs-lookup"><span data-stu-id="4826b-195">Excel</span></span>

  - <span data-ttu-id="4826b-196">fichier TIFF ;</span><span class="sxs-lookup"><span data-stu-id="4826b-196">TIFF file</span></span>

  - <span data-ttu-id="4826b-197">fichier Word.</span><span class="sxs-lookup"><span data-stu-id="4826b-197">Word</span></span>

<span data-ttu-id="4826b-198">Pour exporter la vue active du tableau de bord (et ses valeurs), cliquez sur l’option d’exportation souhaitée.</span><span class="sxs-lookup"><span data-stu-id="4826b-198">To export the current dashboard view (and its values), click the desired export option.</span></span> <span data-ttu-id="4826b-199">Lync Server 2013 génère un rapport au format spécifié, puis vous donne la possibilité d’ouvrir ce rapport ou de l’enregistrer.</span><span class="sxs-lookup"><span data-stu-id="4826b-199">Lync Server 2013 generates a report in the specified format and then give you the option of opening that report or saving it.</span></span> <span data-ttu-id="4826b-200">Notez que, par défaut, Lync Server titre le **tableau de bord de surveillance** du rapport et l’enregistre dans votre dossier téléchargements.</span><span class="sxs-lookup"><span data-stu-id="4826b-200">Note that, by default, Lync Server titles the report **Monitoring Dashboard** and saves it to your Downloads folder.</span></span> <span data-ttu-id="4826b-201">Pour nommer le rapport différemment ou pour le stocker dans un autre dossier, cliquez sur la flèche située à côté du bouton **Enregistrer**, puis cliquez sur **Enregistrer sous**.</span><span class="sxs-lookup"><span data-stu-id="4826b-201">To give the report a different name or to store it in a different folder, click the arrow next to the **Save** button and then click **Save As**.</span></span> <span data-ttu-id="4826b-202">Si le nom **Tableau de bord de suivi** et le dossier d’enregistrement Téléchargements vous conviennent, vous pouvez simplement appuyer sur le bouton **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="4826b-202">If you are fine with name **Monitoring Dashboard** and with having the report saved in the Downloads folder you can just click the **Save** button.</span></span>

<span data-ttu-id="4826b-p109">Lorsque vous essayez d’exporter des données du tableau de bord, il est possible qu’une boîte de dialogue **Alerte de sécurité** apparaisse avec le message « Vos paramètres actuels ne permettent pas le téléchargement de ce fichier. » Dans ce cas, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="4826b-p109">It's possible that, when you try to export dashboard data, a **Security Alert** dialog box will appear along with the message "Your current settings do not allow this file to be downloaded." If that occurs, do the following:</span></span>

  - <span data-ttu-id="4826b-205">Dans Internet Explorer, sélectionnez **Options Internet**.</span><span class="sxs-lookup"><span data-stu-id="4826b-205">In Internet Explorer, select **Internet Options**.</span></span>

  - <span data-ttu-id="4826b-206">Dans la boîte de dialogue **Options Internet**, sous l’onglet **Sécurité**, cliquez sur **Sites approuvés**, puis sur **Sites**.</span><span class="sxs-lookup"><span data-stu-id="4826b-206">In the **Internet Options** dialog box, on the **Security** tab, click **Trusted sites** and then click **Sites**.</span></span>

  - <span data-ttu-id="4826b-207">Dans la boîte de dialogue **sites de confiance** , cliquez sur **Ajouter** pour ajouter Lync Server 2013 exécutant Lync Server 2013 rapports aux collections de sites Web de confiance.</span><span class="sxs-lookup"><span data-stu-id="4826b-207">In the **Trusted sites** dialog box, click **Add** to add the Lync Server 2013 that is running Lync Server 2013 Reports to the collections of trusted websites.</span></span>

  - <span data-ttu-id="4826b-208">Cliquez sur **Fermer**, puis sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="4826b-208">Click **Close** and then click **OK**.</span></span>

<span data-ttu-id="4826b-p110">Vous devez ensuite actualiser le Tableau de bord de suivi pour que les modifications prennent effet. Pour cela, appuyez sur F5 ou cliquez sur l’icône **Actualiser** de la barre d’outils du tableau de bord. (L’icône **Actualiser** représente un cercle contenant deux flèches vertes.)</span><span class="sxs-lookup"><span data-stu-id="4826b-p110">You will then need to refresh the Monitoring Dashboard before the changes take effect. To do that, either press F5 or click the **Refresh** icon in the Dashboard toolbar. (The **Refresh** icon is a circle with a pair of green arrows in it.)</span></span>

<span data-ttu-id="4826b-p111">Vous pouvez également créer une feuille de calcul Excel avec les flux de données actives, comprenant des liens vers les dernières données du Tableau de bord de suivi. Pour créer un fichier de flux de données actives, cliquez sur l’icône orange **Exporter vers un flux de données** dans la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="4826b-p111">You can also create an Excel spreadsheet that includes live data feeds, which includes links to the latest Monitoring Dashboard data. To create a live data feed file, click the orange **Export to Data Feed** icon in the toolbar.</span></span>

<span data-ttu-id="4826b-214">Si vous préférez imprimer le tableau de bord actif, cliquez sur l’icône d’imprimante située dans la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="4826b-214">If you would prefer to print the current Dashboard then click the printer icon in the toolbar.</span></span>

<span data-ttu-id="4826b-215"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4826b-215"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

