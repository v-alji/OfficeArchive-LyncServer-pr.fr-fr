---
title: 'Lync Server 2013 : spécifier la conservation des données CDR'
description: 'Lync Server 2013 : spécifier la conservation des données CDR.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Specifying retention of CDR data
ms:assetid: c0fd6056-87bc-4136-902a-f1b37cd3a1ca
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182581(v=OCS.15)
ms:contentKeyID: 48185299
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d9367721a2390ad701702818590ac14e69da0df9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423784"
---
# <a name="specifying-retention-of-cdr-data-in-lync-server-2013"></a><span data-ttu-id="72c44-103">Spécifier la conservation des données CDR dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="72c44-103">Specifying retention of CDR data in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="72c44-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="72c44-104">

<span> </span></span></span>

<span data-ttu-id="72c44-105">_**Dernière modification de la rubrique :** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="72c44-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="72c44-p101">Par défaut, les données d’enregistrement des détails des appels sont vidées après un délai de 60 jours. Vous pouvez utiliser les paramètres de la page **Enregistrement des détails des appels** pour conserver les données pendant une période plus longue ou plus courte. Si vous désactivez la fonctionnalité d’enregistrement des détails des appels, les données capturées avant l’enregistrement seront également vidées.</span><span class="sxs-lookup"><span data-stu-id="72c44-p101">By default, call detail recording (CDR) data is purged after 60 days. You can use the settings on the **Call Detail Recording** page to retain the data for a longer or shorter period of time. If you disable CDR, data that was captured before CDR was enabled will also be subject to purging.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="72c44-p102">Vous devez configurer l’enregistrement des détails des appels et la qualité de l’expérience (QoE) afin de conserver les données pendant le même nombre de jours. Chaque appel dans les rapports des détails des appels (disponibles à partir de la page web Rapports du serveur de surveillance) comprend des informations d’enregistrement des détails des appels et QoE. Si la durée de vidage pour les données d’enregistrement des détails des appels et de QoE est différente, certains appels peuvent inclure uniquement des données d’enregistrement des détails des appels et d’autres exclusivement des données QoE.</span><span class="sxs-lookup"><span data-stu-id="72c44-p102">You should configure CDR and Quality of Experience (QoE) to retain data for the same number of days. Each call in the call detail reports (CDRs), available from the Monitoring Server Reports webpage, includes CDR and QoE information. If the purging duration for CDR and QoE is different, some calls might only include CDR data, while other may only include QoE data.</span></span>



</div>

<span data-ttu-id="72c44-112">Utilisez les procédures suivantes pour configurer les paramètres de vidage des données d’enregistrement des détails des appels.</span><span class="sxs-lookup"><span data-stu-id="72c44-112">Use the following procedures to configure purge settings for CDR data.</span></span>

<div>

## <a name="to-specify-retention-of-cdr-data"></a><span data-ttu-id="72c44-113">Pour spécifier la conservation des données d’enregistrement des détails des appels</span><span class="sxs-lookup"><span data-stu-id="72c44-113">To specify retention of CDR data</span></span>

1.  <span data-ttu-id="72c44-114">À partir d’un compte d’utilisateur membre du groupe RTCUniversalServerAdmins (ou doté de droits d’utilisateur équivalents), ou affectées au rôle CsServerAdministrator ou CsAdministrator, connectez-vous à n’importe quel ordinateur se trouve sur le réseau sur lequel vous avez déployé Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="72c44-114">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or assigned to the CsServerAdministrator or CsAdministrator role, log on to any computer that is in the network in which you deployed Lync Server 2013.</span></span>

2.  <span data-ttu-id="72c44-115">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="72c44-115">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="72c44-116">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="72c44-116">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="72c44-117">Dans la barre de navigation de gauche, cliquez sur **Surveillance et archivage**, puis cliquez sur **Enregistrement des détails des appels**.</span><span class="sxs-lookup"><span data-stu-id="72c44-117">In the left navigation bar, click **Monitoring and Archiving**, and then click **Call Detail Recording**.</span></span>

4.  <span data-ttu-id="72c44-118">Dans la page **Enregistrement des détails des appels**, cliquez sur le site approprié dans le tableau, cliquez sur **Modifier**, puis sur **Afficher les détails**.</span><span class="sxs-lookup"><span data-stu-id="72c44-118">On the **Call Detail Recording** page, click the appropriate site in the table, click **Edit**, and then click **Show Details**.</span></span>

5.  <span data-ttu-id="72c44-119">Pour activer le vidage, sélectionnez **Activer le vidage des enregistrements des détails des appels**.</span><span class="sxs-lookup"><span data-stu-id="72c44-119">To turn on purging, select **Enable purging of CDRs**.</span></span>

6.  <span data-ttu-id="72c44-120">Dans **Conserver les enregistrements des détails des appels pendant la durée maximale (jours) :**, sélectionnez le nombre maximum de jours pendant lesquels les enregistrements des détails des appels sont à conserver.</span><span class="sxs-lookup"><span data-stu-id="72c44-120">In **Keep CDRs for maximum duration (days):** select the maximum number of days that call detail recordings should be retained.</span></span>

7.  <span data-ttu-id="72c44-121">Dans **Conserver les données de signalement d’erreurs pendant la durée maximale (jours) :**, sélectionnez le nombre maximum de jours pendant lesquels les rapports d’erreurs sont à conserver.</span><span class="sxs-lookup"><span data-stu-id="72c44-121">In **Keep error report data for maximum duration (days):** select the maximum number of days that error reports should be retained.</span></span>

8.  <span data-ttu-id="72c44-122">Cliquez sur **Valider**.</span><span class="sxs-lookup"><span data-stu-id="72c44-122">Click **Commit**.</span></span>

</div>

<div>

## <a name="specifying-cdr-retention-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="72c44-123">Spécification de la rétention CDR en utilisant des applets de cmdlet Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="72c44-123">Specifying CDR Retention by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="72c44-124">Vous pouvez créer des paramètres de rétention CDR à l’aide de Windows PowerShell et de l’applet de Set-CsCdrConfiguration.</span><span class="sxs-lookup"><span data-stu-id="72c44-124">You can create CDR retention settings by using Windows PowerShell and the Set-CsCdrConfiguration cmdlet.</span></span> <span data-ttu-id="72c44-125">Vous pouvez exécuter cette applet de commande sur Lync Server 2013 Management Shell ou à partir d’une session distante de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="72c44-125">You can run this cmdlet either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="72c44-126">Pour plus d’informations sur l’utilisation de Windows PowerShell distant pour vous connecter à Lync Server, voir l’article de blog Lync Server Windows PowerShell « démarrage rapide : gestion de Microsoft Lync Server 2010 à l’aide de Remote PowerShell » [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="72c44-126">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-specify-cdr-retention-for-a-specific-location"></a><span data-ttu-id="72c44-127">Pour spécifier la conservation des enregistrements des détails des appels pour un emplacement particulier</span><span class="sxs-lookup"><span data-stu-id="72c44-127">To specify CDR retention for a specific location</span></span>

  - <span data-ttu-id="72c44-128">Cette commande vide les enregistrements des détails des appels pour le site de Redmond, et configure ce site pour qu’il conserve les enregistrements des détails des appels et les données de signalement d’erreurs pendant 20 jours.</span><span class="sxs-lookup"><span data-stu-id="72c44-128">This command enables purging of CDR data for the Redmond site, and configures the site to maintain both CDR data and error reports data for 20 days.</span></span>
    
        Set-CsCdrConfiguration -Identity "site:Redmond" -EnablePurging -KeepCallDetailForDays 20 -KeepErrorReportForDays 20

</div>

<div>

## <a name="to-specify-cdr-retention-for-multiple-locations"></a><span data-ttu-id="72c44-129">Pour spécifier la conservation des enregistrements des détails des appels pour plusieurs emplacements</span><span class="sxs-lookup"><span data-stu-id="72c44-129">To specify CDR retention for multiple locations</span></span>

  - <span data-ttu-id="72c44-130">Cette commande configure la conservation des enregistrements des détails des appels pour tous les paramètres de configuration des enregistrements des détails des appels actuellement appliqués dans l’organisation.</span><span class="sxs-lookup"><span data-stu-id="72c44-130">This command configures CDR retention for all the CDR configuration settings in use in an organization.</span></span>
    
        Get-CsCdrConfiguration | Set-CsCdrConfiguration-EnablePurging -KeepCallDetailForDays 20 -KeepErrorReportForDays 20

</div>

<span data-ttu-id="72c44-131">Pour plus d’informations, consultez la rubrique d’aide relative à l’applet de passe [Set-CsCdrConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsCdrConfiguration) .</span><span class="sxs-lookup"><span data-stu-id="72c44-131">For more information, see the help topic for the [Set-CsCdrConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsCdrConfiguration) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="72c44-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="72c44-132">See Also</span></span>


[<span data-ttu-id="72c44-133">Enregistrement des détails des appels (CDR) dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="72c44-133">Call detail recording (CDR) in Lync Server 2013</span></span>](lync-server-2013-call-detail-recording-cdr.md)  
  

<span data-ttu-id="72c44-134"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="72c44-134"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

