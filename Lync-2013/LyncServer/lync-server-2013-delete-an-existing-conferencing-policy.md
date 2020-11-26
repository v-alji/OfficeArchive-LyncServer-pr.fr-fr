---
title: 'Lync Server 2013 : supprimer une stratégie de conférence existante'
description: 'Lync Server 2013 : supprimez une stratégie de conférence existante.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete an existing conferencing policy
ms:assetid: 709ed771-790f-4bf1-a4de-b37ca5168688
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688089(v=OCS.15)
ms:contentKeyID: 49733688
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0b64e51acc6e6dc91b938244da28057b01957069
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430503"
---
# <a name="delete-an-existing-conferencing-policy-in-lync-server-2013"></a><span data-ttu-id="41a49-103">Supprimer une stratégie de conférence existante dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="41a49-103">Delete an existing conferencing policy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="41a49-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="41a49-104">

<span> </span></span></span>

<span data-ttu-id="41a49-105">_**Dernière modification de la rubrique :** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="41a49-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="41a49-106">Suivez ces étapes pour supprimer un utilisateur ou une stratégie de conférence au niveau du site.</span><span class="sxs-lookup"><span data-stu-id="41a49-106">Follow these steps to delete a user-level or a site-level conferencing policy.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="41a49-107">Vous ne pouvez pas supprimer la stratégie de conférence globale.</span><span class="sxs-lookup"><span data-stu-id="41a49-107">You cannot delete the global conferencing policy.</span></span>



</div>

<div>

## <a name="to-delete-a-site-or-user-conferencing-policy"></a><span data-ttu-id="41a49-108">Pour supprimer une stratégie de site ou de conférence utilisateur</span><span class="sxs-lookup"><span data-stu-id="41a49-108">To delete a site or user conferencing policy</span></span>

1.  <span data-ttu-id="41a49-109">À partir d’un compte d’utilisateur auquel est affecté le rôle CsUserAdministrator ou CsAdministrator, ouvrez une session sur un ordinateur de votre déploiement interne.</span><span class="sxs-lookup"><span data-stu-id="41a49-109">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="41a49-110">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="41a49-110">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="41a49-111">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="41a49-111">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="41a49-112">Dans la barre de navigation de gauche, cliquez sur **Conférence** , puis sur **stratégie de conférence**.</span><span class="sxs-lookup"><span data-stu-id="41a49-112">In the left navigation bar, click **Conferencing** and then click **Conferencing Policy**.</span></span>

4.  <span data-ttu-id="41a49-113">Dans la liste des stratégies de conférence, cliquez sur la stratégie de site ou d’utilisateur à supprimer, cliquez sur **Modifier**, puis sur **Supprimer**.</span><span class="sxs-lookup"><span data-stu-id="41a49-113">In the list of conferencing policies, click the site or user policy that you want to delete, click **Edit**, and then click **Delete**.</span></span>

</div>

<div>

## <a name="removing-conferencing-policies-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="41a49-114">Suppression de stratégies de conférence à l’aide d’applets de cmdlet Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="41a49-114">Removing Conferencing Policies by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="41a49-115">Vous pouvez supprimer des stratégies de conférence à l’aide de Lync Server Management Shell et de l’applet de passe **Remove-CsConferencingPolicy** .</span><span class="sxs-lookup"><span data-stu-id="41a49-115">You can delete conferencing policies by using Lync Server Management Shell and the **Remove-CsConferencingPolicy** cmdlet.</span></span> <span data-ttu-id="41a49-116">Vous pouvez exécuter cette applet de commande sur Lync Server 2013 Management Shell ou à partir d’une session distante de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="41a49-116">You can run this cmdlet from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="41a49-117">Pour plus d’informations sur l’utilisation de Windows PowerShell distant pour vous connecter à Lync Server, voir l’article de blog Lync Server Windows PowerShell « démarrage rapide : gestion de Microsoft Lync Server 2010 à l’aide de Remote PowerShell » [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="41a49-117">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-remove-a-specified-conferencing-policy"></a><span data-ttu-id="41a49-118">Pour supprimer une stratégie de conférence spécifiée</span><span class="sxs-lookup"><span data-stu-id="41a49-118">To remove a specified conferencing policy</span></span>

  - <span data-ttu-id="41a49-119">La commande suivante permet de supprimer la stratégie de conférence dont le paramètre Identity a la valeur RedmondConferencingPolicy :</span><span class="sxs-lookup"><span data-stu-id="41a49-119">The following command removes the conferencing policy with the Identity RedmondConferencingPolicy:</span></span>
    
        Remove-CsConferencingPolicy -Identity "RedmondConferencingPolicy"

</div>

<div>

## <a name="to-remove-all-of-the-conferencing-policies-applied-to-the-per-user-scope"></a><span data-ttu-id="41a49-120">Pour supprimer toutes les stratégies de conférence appliquées à l’étendue par utilisateur</span><span class="sxs-lookup"><span data-stu-id="41a49-120">To remove all of the conferencing policies applied to the per-user scope</span></span>

  - <span data-ttu-id="41a49-121">La commande suivante supprime toutes les stratégies de conférence configurées pour l’étendue par utilisateur :</span><span class="sxs-lookup"><span data-stu-id="41a49-121">The following command removes all the conferencing policies configured at the per-user scope:</span></span>
    
        Get-CsConferencingPolicy -Filter "tag:*" | Remove-CsConferencingPolicy

</div>

<div>

## <a name="to-remove-all-of-the-conferencing-polices-that-allow-recording-by-external-users"></a><span data-ttu-id="41a49-122">Pour supprimer toutes les stratégies de conférence autorisant l’enregistrement par des utilisateurs externes</span><span class="sxs-lookup"><span data-stu-id="41a49-122">To remove all of the conferencing polices that allow recording by external users</span></span>

  - <span data-ttu-id="41a49-123">La commande suivante supprime toutes les stratégies de conférence qui permettent aux utilisateurs externes d’enregistrer la Conférence :</span><span class="sxs-lookup"><span data-stu-id="41a49-123">The following command deletes any conferencing policies that allow external users to record the conference:</span></span>
    
        Get-CsConferencingPolicy | Where-Object {$_.AllowExternalUsersToRecordMeetings -eq $True} | Remove-CsConferencingPolicy

</div>

<span data-ttu-id="41a49-124">Pour plus d’informations, consultez la rubrique [Remove-CsConferencingPolicy](https://docs.microsoft.com/powershell/module/skype/Remove-CsConferencingPolicy).</span><span class="sxs-lookup"><span data-stu-id="41a49-124">For details, see [Remove-CsConferencingPolicy](https://docs.microsoft.com/powershell/module/skype/Remove-CsConferencingPolicy).</span></span>

<span data-ttu-id="41a49-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="41a49-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

