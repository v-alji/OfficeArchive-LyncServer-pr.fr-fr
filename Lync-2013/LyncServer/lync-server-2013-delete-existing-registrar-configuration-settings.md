---
title: 'Lync Server 2013 : supprimer les paramètres de configuration du Bureau d’enregistrement existants'
description: 'Lync Server 2013 : supprimez les paramètres de configuration du Bureau d’enregistrement existants.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete existing Registrar configuration settings
ms:assetid: ae43cd75-cae4-4f78-b037-779a2cdb583b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182571(v=OCS.15)
ms:contentKeyID: 48185132
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b625b97724edf0ecf8928ec31d89a6166230c4c7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430454"
---
# <a name="delete-existing-registrar-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="d13cd-103">Supprimer les paramètres de configuration du Bureau d’enregistrement existants dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d13cd-103">Delete existing Registrar configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d13cd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d13cd-104">

<span> </span></span></span>

<span data-ttu-id="d13cd-105">_**Dernière modification de la rubrique :** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="d13cd-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="d13cd-106">Pour supprimer un bureau d’enregistrement, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="d13cd-106">Follow these steps to delete a Registrar.</span></span>

<div>

## <a name="to-delete-registrar-configuration-settings"></a><span data-ttu-id="d13cd-107">Pour supprimer des paramètres de configuration du serveur d’inscriptions avancé</span><span class="sxs-lookup"><span data-stu-id="d13cd-107">To delete Registrar configuration settings</span></span>

1.  <span data-ttu-id="d13cd-108">À partir d’un compte d’utilisateur membre du groupe RTCUniversalServerAdmins (ou doté de droits d’utilisateur équivalents), ou affectées au rôle CsServerAdministrator ou CsAdministrator, connectez-vous à n’importe quel ordinateur se trouve sur le réseau sur lequel vous avez déployé Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d13cd-108">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or assigned to the CsServerAdministrator or CsAdministrator role, log on to any computer that is in the network in which you deployed Lync Server 2013.</span></span>

2.  <span data-ttu-id="d13cd-109">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="d13cd-109">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="d13cd-110">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="d13cd-110">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="d13cd-111">Dans la barre de navigation de gauche, cliquez sur **Sécurité**, puis sur **Serveur d’inscriptions avancé**.</span><span class="sxs-lookup"><span data-stu-id="d13cd-111">In the left navigation bar, click **Security** and then click **Registrar**.</span></span>

4.  <span data-ttu-id="d13cd-112">Dans la page **Serveur d’inscriptions avancé**, dans le champ de recherche, tapez entièrement ou partiellement le nom du serveur d’inscriptions avancé à supprimer.</span><span class="sxs-lookup"><span data-stu-id="d13cd-112">On the **Registrar** page, and in the search field, type all or part of the name of the Registrar you want to delete.</span></span>

5.  <span data-ttu-id="d13cd-113">Dans la liste, sélectionnez le serveur d’inscriptions avancé souhaité, cliquez sur **Modifier**, puis sur **Supprimer**.</span><span class="sxs-lookup"><span data-stu-id="d13cd-113">In the list, click the Registrar that you want, click **Edit**, and then click **Delete**.</span></span>

6.  <span data-ttu-id="d13cd-114">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="d13cd-114">Click **OK**.</span></span>

</div>

<div>

## <a name="removing-registrar-configuration-settings-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="d13cd-115">Suppression des paramètres de configuration du Bureau d’enregistrement à l’aide des cmdlets Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="d13cd-115">Removing Registrar Configuration Settings by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="d13cd-116">Vous pouvez supprimer les paramètres de configuration du Bureau d’enregistrement à l’aide de Windows PowerShell et de l’applet de passe **Remove-CsProxyConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="d13cd-116">You can delete the Registrar configuration settings by using Windows PowerShell and the **Remove-CsProxyConfiguration** cmdlet.</span></span> <span data-ttu-id="d13cd-117">Vous pouvez exécuter cette applet de commande sur Lync Server 2013 Management Shell ou à partir d’une session distante de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d13cd-117">You can run this cmdlet from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="d13cd-118">Pour plus d’informations sur l’utilisation de Windows PowerShell distant pour vous connecter à Lync Server, voir l’article de blog Lync Server Windows PowerShell « démarrage rapide : gestion de Microsoft Lync Server 2010 à l’aide de Remote PowerShell » [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="d13cd-118">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-remove-a-specific-set-of-registrar-security-settings"></a><span data-ttu-id="d13cd-119">Pour supprimer un ensemble spécifique de paramètres de sécurité du serveur d’inscriptions avancé</span><span class="sxs-lookup"><span data-stu-id="d13cd-119">To remove a specific set of Registrar security settings</span></span>

  - <span data-ttu-id="d13cd-120">La commande ci-dessous supprime les paramètres de sécurité du serveur d’inscriptions avancé appliqués au serveur Edge atl-edge-011.litwareinc.com :</span><span class="sxs-lookup"><span data-stu-id="d13cd-120">The following command removes the Registrar security settings applied to the edge Server atl-edge-011.litwareinc.com:</span></span>
    
        Remove-CsProxyConfiguration -Identity service:EdgeServer:atl-edge-011.litwareinc.com

</div>

<div>

## <a name="to-remove-all-of-the-registrar-security-settings-applied-to-the-site-scope"></a><span data-ttu-id="d13cd-121">Pour supprimer tous les paramètres de sécurité du serveur d’inscriptions avancé appliqués à l’étendue Site</span><span class="sxs-lookup"><span data-stu-id="d13cd-121">To remove all of the Registrar security settings applied to the site scope</span></span>

  - <span data-ttu-id="d13cd-122">La commande ci-dessous supprime tous les paramètres de sécurité du serveur d’inscriptions avancé appliqués au service de serveur d’inscriptions avancé :</span><span class="sxs-lookup"><span data-stu-id="d13cd-122">The following command removes all the Registrar security settings applied to the Registrar service:</span></span>
    
        Get-CsProxyConfiguration -Filter "service:Registrar:*" | Remove-CsProxyConfiguration

</div>

<div>

## <a name="to-remove-all-of-the-registrar-security-settings-that-allow-ntlm-authentication"></a><span data-ttu-id="d13cd-123">Pour supprimer tous les paramètres de sécurité du serveur d’inscriptions avancé qui permettent l’authentification NTLM</span><span class="sxs-lookup"><span data-stu-id="d13cd-123">To remove all of the Registrar security settings that allow NTLM authentication</span></span>

  - <span data-ttu-id="d13cd-124">La commande ci-dessous supprime tous les paramètres de sécurité du serveur d’inscriptions avancé qui permettent l’utilisation de NTLM pour l’authentification client :</span><span class="sxs-lookup"><span data-stu-id="d13cd-124">The following command deletes all the Registrar security settings that allow the use of NTLM for client authentication:</span></span>
    
        Get-CsProxyConfiguration | Where-Object {$_.UseNtlmForClientToProxyAuth -eq $True}| Remove-CsProxyConfiguration

</div>

<span data-ttu-id="d13cd-125">Pour plus d’informations, consultez la rubrique [Remove-CsProxyConfiguration](https://docs.microsoft.com/powershell/module/skype/Remove-CsProxyConfiguration).</span><span class="sxs-lookup"><span data-stu-id="d13cd-125">For details, see [Remove-CsProxyConfiguration](https://docs.microsoft.com/powershell/module/skype/Remove-CsProxyConfiguration).</span></span>

<span data-ttu-id="d13cd-126"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d13cd-126"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

