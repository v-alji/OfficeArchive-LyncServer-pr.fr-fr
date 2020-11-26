---
title: 'Lync Server 2013 : test de la configuration du nœud observateur d’observateurs'
description: 'Lync Server 2013 : test de la configuration du nœud FileSystemWatcher.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing watcher node configuration
ms:assetid: f9ecd85c-0ae9-4906-b786-6b002b5a77c6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn751537(v=OCS.15)
ms:contentKeyID: 63969667
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f1eeb141eee011d7e06f5dd49e483e026484d733
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440926"
---
# <a name="testing-watcher-node-configuration-in-lync-server-2013"></a><span data-ttu-id="482c8-103">Test de la configuration du nœud FileSystemWatcher dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="482c8-103">Testing watcher node configuration in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="482c8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="482c8-104">

<span> </span></span></span>

<span data-ttu-id="482c8-105">_**Dernière modification de la rubrique :** 2014-11-03_</span><span class="sxs-lookup"><span data-stu-id="482c8-105">_**Topic Last Modified:** 2014-11-03_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="482c8-106">Échéancier de vérification</span><span class="sxs-lookup"><span data-stu-id="482c8-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="482c8-107">Jour</span><span class="sxs-lookup"><span data-stu-id="482c8-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="482c8-108">Outil de test</span><span class="sxs-lookup"><span data-stu-id="482c8-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="482c8-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="482c8-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="482c8-110">Autorisations requises</span><span class="sxs-lookup"><span data-stu-id="482c8-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="482c8-111">Lorsque l’application est exécutée localement à l’aide de Lync Server Management Shell, les utilisateurs doivent être membres du groupe de sécurité RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="482c8-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="482c8-112">Lors de l’exécution à l’aide d’une instance distante de Windows PowerShell, un rôle RBAC doit être attribué aux utilisateurs qui ont l’autorisation d’exécuter l’applet de commande <strong>test-CsWatcherNodeConfiguration</strong> .</span><span class="sxs-lookup"><span data-stu-id="482c8-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the <strong>Test-CsWatcherNodeConfiguration</strong> cmdlet.</span></span> <span data-ttu-id="482c8-113">Pour afficher la liste de tous les rôles RBAC qui peuvent utiliser cette applet de commande, exécutez la commande suivante à partir de l’invite Windows PowerShell :</span><span class="sxs-lookup"><span data-stu-id="482c8-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot; Test-CsWatcherNodeConfiguration&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="482c8-114">Description</span><span class="sxs-lookup"><span data-stu-id="482c8-114">Description</span></span>

<span data-ttu-id="482c8-115">Si vous utilisez Microsoft System Center Operations Manager pour contrôler Lync Server 2013, vous avez la possibilité de configurer des « nœuds d’observation » : les ordinateurs qui exécutent de manière régulière et automatique les transactions de synthèse pour vérifier que le serveur Lync fonctionne comme prévu.</span><span class="sxs-lookup"><span data-stu-id="482c8-115">If you are using Microsoft System Center Operations Manager to monitor Lync Server 2013 then you have the option of setting up "watcher nodes": computers that periodically, and automatically, run synthetic transactions to verify that Lync Server is working as expected.</span></span> <span data-ttu-id="482c8-116">Les nœuds d’observation sont assignés aux pools et sont gérés à l’aide des cmdlets **CsWatcherNodeConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="482c8-116">Watcher nodes are assigned to pools, and are managed by using the **CsWatcherNodeConfiguration** cmdlets.</span></span> <span data-ttu-id="482c8-117">Notez que vous n’avez pas besoin d’installer de nœuds FileSystemWatcher si vous utilisez System Center Operations Manager.</span><span class="sxs-lookup"><span data-stu-id="482c8-117">Note that you do not need to install watcher nodes if you are using System Center Operations Manager.</span></span> <span data-ttu-id="482c8-118">Vous pouvez toujours surveiller votre système sans utiliser de nœuds FileSystemWatcher.</span><span class="sxs-lookup"><span data-stu-id="482c8-118">You can still monitor your system without using watcher nodes.</span></span> <span data-ttu-id="482c8-119">La seule différence réside dans le fait que les transactions synthétiques que vous souhaitez exécuter doivent être appelées manuellement au lieu d’être automatiquement appelées par Operations Manager.</span><span class="sxs-lookup"><span data-stu-id="482c8-119">The only difference is that any synthetic transactions that you want to run must be invoked manually instead of automatically invoked by Operations Manager.</span></span>

<span data-ttu-id="482c8-120">L’applet de **contrôle test-CsWatcherNodeConfiguration** vous permet de vérifier qu’un nœud d’observateur a été correctement configuré et qu’il est affecté à un pool Lync Server 2013 valide.</span><span class="sxs-lookup"><span data-stu-id="482c8-120">The **Test-CsWatcherNodeConfiguration** cmdlet enables you to verify that a watcher node was configured correctly and is assigned to a valid Lync Server 2013 pool.</span></span> <span data-ttu-id="482c8-121">Notez que l’applet de **contrôle test-CsWatcherNodeConfiguration** doit être exécutée sur le nœud Watcher lui-même.</span><span class="sxs-lookup"><span data-stu-id="482c8-121">Note that the **Test-CsWatcherNodeConfiguration** cmdlet must be run on the watcher node itself.</span></span> <span data-ttu-id="482c8-122">L’applet de commande ne peut pas être exécutée sur des ordinateurs distants.</span><span class="sxs-lookup"><span data-stu-id="482c8-122">The cmdlet cannot be run against remote computers.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="482c8-123">Exécution du test</span><span class="sxs-lookup"><span data-stu-id="482c8-123">Running the test</span></span>

<span data-ttu-id="482c8-124">La commande suivante vérifie les paramètres de configuration de chaque nœud FileSystemWatcher utilisé au sein de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="482c8-124">The following command verifies the configuration settings for each watcher node that is being used in the organization.</span></span>

    Test-CsWatcherNodeConfiguration

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="482c8-125">Détermination du succès ou de l’échec</span><span class="sxs-lookup"><span data-stu-id="482c8-125">Determining success or failure</span></span>

<span data-ttu-id="482c8-126">La sortie d’exemple réussie suivante illustre un système avec quatre serveurs Edge.</span><span class="sxs-lookup"><span data-stu-id="482c8-126">The following successful sample output shows a system with four edge servers.</span></span>

<span data-ttu-id="482c8-127">Validation de la liste de ressources atl-cs-001.litwareinc.com par rapport à la topologie.</span><span class="sxs-lookup"><span data-stu-id="482c8-127">Validating target pool atl-cs-001.litwareinc.com against topology.</span></span>

<span data-ttu-id="482c8-128">Réussite : atl-cs-001.litwareinc.com de réserve cible existe dans la topologie.</span><span class="sxs-lookup"><span data-stu-id="482c8-128">Success: Target pool atl-cs-001.litwareinc.com exists in topology.</span></span>

<span data-ttu-id="482c8-129">Réussite : le rôle de bureau d’enregistrement de la liste de atl-cs-001.litwareinc.com est installé.</span><span class="sxs-lookup"><span data-stu-id="482c8-129">Success: Target pool atl-cs-001.litwareinc.com has Registrar role installed.</span></span>

<span data-ttu-id="482c8-130">Réussite : la version du pool cible atl-cs-001.litwareinc.com est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="482c8-130">Success: Target pool atl-cs-001.litwareinc.com is supported version.</span></span>

<span data-ttu-id="482c8-131">Réussite : le numéro de port pour le pool cible 5061 atl-cs-001.litwareinc.com est correct.</span><span class="sxs-lookup"><span data-stu-id="482c8-131">Success: Port number for 5061 Target pool atl-cs-001.litwareinc.com is correct.</span></span>

<span data-ttu-id="482c8-132">La vérification de l’absence de pools dans la configuration de nœud d’observateur est démarrée.</span><span class="sxs-lookup"><span data-stu-id="482c8-132">Checking for missing pools in watcher node configuration is started.</span></span> <span data-ttu-id="482c8-133">Si des erreurs sont détectées, elles sont imprimées.</span><span class="sxs-lookup"><span data-stu-id="482c8-133">If any error is detected, it will be printed.</span></span>

<span data-ttu-id="482c8-134">La vérification de l’absence de pools dans la configuration du nœud d’observation est terminée.</span><span class="sxs-lookup"><span data-stu-id="482c8-134">Checking for missing pools in watcher node configuration is finished.</span></span>

<span data-ttu-id="482c8-135">La recherche de clés de registre de nœud d’observation créées par l’installation du nœud d’observateur est démarrée.</span><span class="sxs-lookup"><span data-stu-id="482c8-135">Checking for watcher node registry keys created by watcher node installation, is started.</span></span> <span data-ttu-id="482c8-136">Si des erreurs sont détectées, elles sont imprimées.</span><span class="sxs-lookup"><span data-stu-id="482c8-136">If any error is detected, it will be printed.</span></span>

<span data-ttu-id="482c8-137">La vérification des clés de registre de nœud d’observation créées par l’installation du nœud d’observation est terminée.</span><span class="sxs-lookup"><span data-stu-id="482c8-137">Checking for watcher node registry keys created by watcher node installation, is finished.</span></span> <span data-ttu-id="482c8-138">Le type d’authentification détecté est Negotiate.</span><span class="sxs-lookup"><span data-stu-id="482c8-138">Detected authentication type is Negotiate.</span></span>

<span data-ttu-id="482c8-139">Validation réussie de l’existence des informations d’identification de l’utilisateur du test SIP : user1@ atl-cs-001.litwareinc.com dans le magasin de gestion des informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="482c8-139">Successfully validated existence of test user’s credential sip:user1@ atl-cs-001.litwareinc.com in credential management store.</span></span>

<span data-ttu-id="482c8-140">Validation réussie de l’existence des informations d’identification de l’utilisateur du test SIP : user2@ atl-cs-001.litwareinc.com dans le magasin de gestion des informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="482c8-140">Successfully validated existence of test user’s credential sip:user2@ atl-cs-001.litwareinc.com in credential management store.</span></span>

<span data-ttu-id="482c8-141">La vérification de l’absence de pools dans la configuration de nœud d’observateur est démarrée.</span><span class="sxs-lookup"><span data-stu-id="482c8-141">Checking for missing pools in watcher node configuration is started.</span></span> <span data-ttu-id="482c8-142">Si des erreurs sont détectées, elles sont imprimées.</span><span class="sxs-lookup"><span data-stu-id="482c8-142">If any error is detected, it will be printed.</span></span>

<span data-ttu-id="482c8-143">AVERTISSEMENT : le pool atl-cs-001.litwareinc.com possède le Bureau d’enregistrement</span><span class="sxs-lookup"><span data-stu-id="482c8-143">WARNING: Pool atl-cs-001.litwareinc.com has Registrar</span></span>

<span data-ttu-id="482c8-144">rôle installé, mais aucun utilisateur de test n’est configuré pour celui-ci.</span><span class="sxs-lookup"><span data-stu-id="482c8-144">role installed, but there are no test users configured for it.</span></span>

<span data-ttu-id="482c8-145">La vérification de l’absence de pools dans la configuration du nœud d’observation est terminée.</span><span class="sxs-lookup"><span data-stu-id="482c8-145">Checking for missing pools in watcher node configuration is finished.</span></span>

<span data-ttu-id="482c8-146">La vérification des clés de registre de nœud d’observateur créées par l’installation du nœud d’observateur est</span><span class="sxs-lookup"><span data-stu-id="482c8-146">Checking for watcher node registry keys created by watcher node installation, is</span></span>

<span data-ttu-id="482c8-147">lance.</span><span class="sxs-lookup"><span data-stu-id="482c8-147">started.</span></span> <span data-ttu-id="482c8-148">Si des erreurs sont détectées, elles sont imprimées.</span><span class="sxs-lookup"><span data-stu-id="482c8-148">If any error is detected, it will be printed.</span></span>

<span data-ttu-id="482c8-149">Test-CsWatcherNodeConfiguration : impossible de trouver la clé de registre d’intégrité dans</span><span class="sxs-lookup"><span data-stu-id="482c8-149">Test-CsWatcherNodeConfiguration : Cannot find Health registry key in</span></span>

<span data-ttu-id="482c8-150">Logiciel \\ \\ de communications en temps réel Microsoft en temps réel.</span><span class="sxs-lookup"><span data-stu-id="482c8-150">Software\\Microsoft\\Real-Time Communications.</span></span> <span data-ttu-id="482c8-151">Vérifiez que le nœud FileSystemWatcher. msi est</span><span class="sxs-lookup"><span data-stu-id="482c8-151">Make sure watcher node .msi is</span></span>

<span data-ttu-id="482c8-152">installé correctement.</span><span class="sxs-lookup"><span data-stu-id="482c8-152">installed properly.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="482c8-153">Raisons pour lesquelles le test peut avoir échoué</span><span class="sxs-lookup"><span data-stu-id="482c8-153">Reasons why the test might have failed</span></span>

<span data-ttu-id="482c8-154">Voici quelques raisons courantes pour lesquelles **les tests-CsWatcherNodeConfiguration** peuvent échouer :</span><span class="sxs-lookup"><span data-stu-id="482c8-154">Here are some common reasons why **Test-CsWatcherNodeConfiguration** might fail:</span></span>

  - <span data-ttu-id="482c8-155">Le nœud de l’observateur n’est pas correctement installé.</span><span class="sxs-lookup"><span data-stu-id="482c8-155">Watcher node is not correctly installed.</span></span>

  - <span data-ttu-id="482c8-156">Aucun utilisateur de test n’est configuré.</span><span class="sxs-lookup"><span data-stu-id="482c8-156">No test users are configured.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="482c8-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="482c8-157">See Also</span></span>


[<span data-ttu-id="482c8-158">Get-CsWatcherNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="482c8-158">Get-CsWatcherNodeConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsWatcherNodeConfiguration)  
[<span data-ttu-id="482c8-159">New-CsWatcherNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="482c8-159">New-CsWatcherNodeConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsWatcherNodeConfiguration)  
[<span data-ttu-id="482c8-160">Remove-CsWatcherNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="482c8-160">Remove-CsWatcherNodeConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsWatcherNodeConfiguration)  
[<span data-ttu-id="482c8-161">Set-CsWatcherNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="482c8-161">Set-CsWatcherNodeConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsWatcherNodeConfiguration)  
  

<span data-ttu-id="482c8-162"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="482c8-162"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

