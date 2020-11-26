---
title: Supprimer une collection existante de paramètres de configuration de la version du client
description: Supprimez une collection existante de paramètres de configuration de la version du client.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete an existing collection of client version configuration settings
ms:assetid: 70bf1216-d0d2-45ce-881f-b8edadf3cec7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ898480(v=OCS.15)
ms:contentKeyID: 50873760
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 25a7d384bdfd84a1a6e04041988c16788a116626
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430566"
---
# <a name="delete-an-existing-collection-of-client-version-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="58f27-103">Supprimer une collection existante de paramètres de configuration de la version du client dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="58f27-103">Delete an existing collection of client version configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="58f27-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="58f27-104">

<span> </span></span></span>

<span data-ttu-id="58f27-105">_**Dernière modification de la rubrique :** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="58f27-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="58f27-106">Si vous voulez supprimer les paramètres de configuration de client déjà configurés pour un site, vous pouvez supprimer les paramètres dans Lync Server 2013 Control Panel ou Lync Server 2013 Management Shell.</span><span class="sxs-lookup"><span data-stu-id="58f27-106">If you want to remove the client configuration settings that have been previously configured for a site, you can remove the settings from Lync Server 2013 Control Panel or Lync Server 2013 Management Shell.</span></span>

<div>

## <a name="to-remove-client-configuration-settings-by-using-lync-server-control-panel"></a><span data-ttu-id="58f27-107">Pour supprimer les paramètres de configuration du client à l’aide du panneau de configuration de Lync Server</span><span class="sxs-lookup"><span data-stu-id="58f27-107">To remove client configuration settings by using Lync Server Control Panel</span></span>

1.  <span data-ttu-id="58f27-108">À partir d’un compte d’utilisateur auquel est affecté le rôle CsUserAdministrator ou CsAdministrator, ouvrez une session sur un ordinateur de votre déploiement interne.</span><span class="sxs-lookup"><span data-stu-id="58f27-108">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="58f27-109">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="58f27-109">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="58f27-110">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="58f27-110">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="58f27-111">Dans la barre de navigation de gauche, cliquez sur **clients**, puis sur le bouton de navigation configuration de la **version du client** .</span><span class="sxs-lookup"><span data-stu-id="58f27-111">In the left navigation bar, click **Clients**, and then click the **Client Version Configuration** navigation button.</span></span>

4.  <span data-ttu-id="58f27-112">Sélectionnez le site, cliquez sur **modifier**, sur **supprimer**, puis sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="58f27-112">Select the site, click **Edit**, click **Delete**, and then click **OK**.</span></span>

</div>

<div>

## <a name="removing-client-version-configuration-settings-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="58f27-113">Suppression des paramètres de configuration de la version du client à l’aide des cmdlets Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="58f27-113">Removing Client Version Configuration Settings by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="58f27-114">Vous pouvez supprimer des paramètres de configuration de la version du client à l’aide de l’applet de contrôle **Remove-CsClientVersionConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="58f27-114">You can delete client version configuration settings by using the **Remove-CsClientVersionConfiguration** cmdlet.</span></span> <span data-ttu-id="58f27-115">Cette applet de commande peut être exécutée à partir de Lync Server 2013 Management Shell ou d’une session distante de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="58f27-115">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="58f27-116">Pour plus d’informations sur l’utilisation de Windows PowerShell distant pour vous connecter à Lync Server, voir l’article de blog Lync Server Windows PowerShell « démarrage rapide : gestion de Microsoft Lync Server 2010 à l’aide de Remote PowerShell » [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="58f27-116">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-remove-a-specified-collection-of-client-version-configuration-settings"></a><span data-ttu-id="58f27-117">Pour supprimer une collection spécifiée de paramètres de configuration de la version du client</span><span class="sxs-lookup"><span data-stu-id="58f27-117">To remove a specified collection of client version configuration settings</span></span>

  - <span data-ttu-id="58f27-118">La commande suivante supprime les paramètres de configuration de la version du client appliqués au site de Redmond :</span><span class="sxs-lookup"><span data-stu-id="58f27-118">The following command removes the client version configuration settings applied to the Redmond site:</span></span>
    
        Remove-CsClientVersionConfiguration -Identity "site:Redmond"

</div>

<div>

## <a name="to-remove-all-the-client-version-configuration-settings-applied-to-the-site-scope"></a><span data-ttu-id="58f27-119">Pour supprimer tous les paramètres de configuration de la version du client appliqués à l’étendue du site</span><span class="sxs-lookup"><span data-stu-id="58f27-119">To remove all the client version configuration settings applied to the site scope</span></span>

  - <span data-ttu-id="58f27-120">Cette commande supprime tous les paramètres de configuration de la version du client configurés pour l’étendue du site :</span><span class="sxs-lookup"><span data-stu-id="58f27-120">This command removes all the client version configuration settings configured at the site scope:</span></span>
    
        Get-CsClientVersionConfiguration -Filter site:* | Remove-CsClientVersionConfiguration

</div>

<div>

## <a name="to-remove-all-the-client-version-configuration-settings-based-on-the-value-of-the-defaultaction-property"></a><span data-ttu-id="58f27-121">Pour supprimer tous les paramètres de configuration de la version du client en fonction de la valeur de la propriété DefaultAction</span><span class="sxs-lookup"><span data-stu-id="58f27-121">To remove all the client version configuration settings based on the value of the DefaultAction property</span></span>

  - <span data-ttu-id="58f27-122">Cette commande supprime tous les paramètres de configuration de la version du client pour lesquels l’action par défaut a été définie sur « bloquer » :</span><span class="sxs-lookup"><span data-stu-id="58f27-122">And this command removes all the client version configuration settings where the default action has been set to "Block":</span></span>
    
        Get-CsClientVersionConfiguration | Where-Object {$_.DefaultAction -eq "Block" | Remove-CsClientVersionConfiguration

</div>

<span data-ttu-id="58f27-123">Pour plus d’informations, consultez la rubrique d’aide relative à l’applet de connexion [Remove-CsClientVersionConfiguration](https://technet.microsoft.com/library/Gg425925(v=OCS.15)) .</span><span class="sxs-lookup"><span data-stu-id="58f27-123">For details, see the Help topic for the [Remove-CsClientVersionConfiguration](https://technet.microsoft.com/library/Gg425925(v=OCS.15)) cmdlet.</span></span>

<span data-ttu-id="58f27-124"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="58f27-124"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

