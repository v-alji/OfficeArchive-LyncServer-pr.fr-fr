---
title: 'Lync Server 2013 : test de la configuration du serveur LIS'
description: 'Lync Server 2013 : test de la configuration du serveur LIS.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing LIS server configuration
ms:assetid: 6b06e7ab-522f-41a2-878b-e89cd4e3c6da
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn690129(v=OCS.15)
ms:contentKeyID: 63969614
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ba4d16d2ce48e3e5bb89e863f02902d05ce77bd7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394501"
---
# <a name="testing-lis-server-configuration-in-lync-server-2013"></a><span data-ttu-id="b18fc-103">Test de la configuration du serveur LIS dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b18fc-103">Testing LIS server configuration in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b18fc-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b18fc-104">

<span> </span></span></span>

<span data-ttu-id="b18fc-105">_**Dernière modification de la rubrique :** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="b18fc-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b18fc-106">Échéancier de vérification</span><span class="sxs-lookup"><span data-stu-id="b18fc-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="b18fc-107">Jour</span><span class="sxs-lookup"><span data-stu-id="b18fc-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b18fc-108">Outil de test</span><span class="sxs-lookup"><span data-stu-id="b18fc-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="b18fc-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="b18fc-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b18fc-110">Autorisations requises</span><span class="sxs-lookup"><span data-stu-id="b18fc-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="b18fc-111">Lorsque l’application est exécutée localement à l’aide de Lync Server Management Shell, les utilisateurs doivent être membres du groupe de sécurité RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="b18fc-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="b18fc-112">Lors de l’exécution à l’aide d’une instance distante de Windows PowerShell, un rôle RBAC doit être attribué aux utilisateurs qui ont l’autorisation d’exécuter l’applet de commande Test-CsLisConfiguration.</span><span class="sxs-lookup"><span data-stu-id="b18fc-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsLisConfiguration cmdlet.</span></span> <span data-ttu-id="b18fc-113">Pour afficher la liste de tous les rôles RBAC qui peuvent utiliser cette applet de commande, exécutez la commande suivante à partir de l’invite Windows PowerShell :</span><span class="sxs-lookup"><span data-stu-id="b18fc-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsLisConfiguration&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="b18fc-114">Description</span><span class="sxs-lookup"><span data-stu-id="b18fc-114">Description</span></span>

<span data-ttu-id="b18fc-115">Le cmdlet Test-CsLisConfiguration vérifie la possibilité de contacter le service Web LIS.</span><span class="sxs-lookup"><span data-stu-id="b18fc-115">The Test-CsLisConfiguration cmdlet verifies your ability to contact the LIS web service.</span></span> <span data-ttu-id="b18fc-116">Si le service Web peut être contacté, le test sera considéré comme ayant réussi, qu’il y ait ou non d’emplacements spécifiques.</span><span class="sxs-lookup"><span data-stu-id="b18fc-116">If the web service can be contacted, then the test will be considered a success, regardless of whether any specific locations can be found.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="b18fc-117">Exécution du test</span><span class="sxs-lookup"><span data-stu-id="b18fc-117">Running the test</span></span>

<span data-ttu-id="b18fc-118">Vous pouvez exécuter l’applet de contrôle Test-CsLisConfguration à l’aide d’un compte de test préconfiguré (voir Configuration de comptes de test pour exécuter des tests Lync Server) ou du compte d’un utilisateur qui est activé pour Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b18fc-118">The Test-CsLisConfguration cmdlet can be run using either a preconfigured test account (see Setting Up Test Accounts for Running Lync Server Tests) or the account of any user who is enabled for Lync Server.</span></span> <span data-ttu-id="b18fc-119">Pour effectuer cette vérification à l’aide d’un compte de test, vous devez simplement spécifier le nom de domaine complet (FQDN) du pool de serveurs Lync testé.</span><span class="sxs-lookup"><span data-stu-id="b18fc-119">To run this check using a test account, you just have to specify the FQDN of the Lync Server pool being tested.</span></span> <span data-ttu-id="b18fc-120">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="b18fc-120">For example:</span></span>

    Test-CsLisConfiguration -TargetFqdn "atl-cs-001.litwareinc.com"

<span data-ttu-id="b18fc-121">Pour effectuer cette vérification à l’aide d’un compte d’utilisateur réel, vous devez d’abord créer un objet d’informations d’identification Windows PowerShell contenant le nom et le mot de passe du compte.</span><span class="sxs-lookup"><span data-stu-id="b18fc-121">To run this check using an actual user account, you must first create a Windows PowerShell credentials object that contains the account name and password.</span></span> <span data-ttu-id="b18fc-122">Vous devez alors inclure cet objet Credential et l’adresse SIP attribuée au compte lorsque vous appelez le test-CsLisConfiguration :</span><span class="sxs-lookup"><span data-stu-id="b18fc-122">You must then include that credentials object and the SIP address assigned to the account when you call Test-CsLisConfiguration:</span></span>

    $credential = Get-Credential "litwareinc\kenmyer"
    Test-CsLisConfiguration -TargetFqdn "atl-cs-001.litwareinc.com"-UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential

<span data-ttu-id="b18fc-123">Pour plus d’informations, consultez la documentation d’aide de l’applet de [contrôle test-CsLisConfiguration](https://docs.microsoft.com/powershell/module/skype/Test-CsLisConfiguration) .</span><span class="sxs-lookup"><span data-stu-id="b18fc-123">For more information, see the Help documentation for the [Test-CsLisConfiguration](https://docs.microsoft.com/powershell/module/skype/Test-CsLisConfiguration) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="b18fc-124">Détermination du succès ou de l’échec</span><span class="sxs-lookup"><span data-stu-id="b18fc-124">Determining success or failure</span></span>

<span data-ttu-id="b18fc-125">Si le LIS est configuré correctement, vous recevrez une sortie similaire à celle-ci, avec la propriété Result marquée comme **réussie :**</span><span class="sxs-lookup"><span data-stu-id="b18fc-125">If the LIS is correctly configured, you'll receive output similar to this, with the Result property marked as **Success:**</span></span>

<span data-ttu-id="b18fc-126">TargetUri https://atl-cs-001.litwareinc.com:443/locationinformation/</span><span class="sxs-lookup"><span data-stu-id="b18fc-126">TargetUri : https://atl-cs-001.litwareinc.com:443/locationinformation/</span></span>

<span data-ttu-id="b18fc-127">liservice. svc</span><span class="sxs-lookup"><span data-stu-id="b18fc-127">liservice.svc</span></span>

<span data-ttu-id="b18fc-128">TargetFqdn : atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="b18fc-128">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="b18fc-129">Résultat : réussite</span><span class="sxs-lookup"><span data-stu-id="b18fc-129">Result : Success</span></span>

<span data-ttu-id="b18fc-130">Latence : 00:00:06.1616913</span><span class="sxs-lookup"><span data-stu-id="b18fc-130">Latency : 00:00:06.1616913</span></span>

<span data-ttu-id="b18fc-131">Error</span><span class="sxs-lookup"><span data-stu-id="b18fc-131">Error :</span></span>

<span data-ttu-id="b18fc-132">Diagnostic</span><span class="sxs-lookup"><span data-stu-id="b18fc-132">Diagnosis :</span></span>

<span data-ttu-id="b18fc-133">Si l’utilisateur spécifié ne peut pas se connecter ou se déconnecter, le résultat est affiché en tant qu’échec et des informations supplémentaires sont enregistrées dans les propriétés d’erreur et de diagnostic :</span><span class="sxs-lookup"><span data-stu-id="b18fc-133">If the specified user can't log on or log off, the Result will be shown as Failure, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="b18fc-134">TargetUri</span><span class="sxs-lookup"><span data-stu-id="b18fc-134">TargetUri :</span></span>

<span data-ttu-id="b18fc-135">TargetFqdn : atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="b18fc-135">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="b18fc-136">Résultat : échec</span><span class="sxs-lookup"><span data-stu-id="b18fc-136">Result : Failure</span></span>

<span data-ttu-id="b18fc-137">Latence : 00:00:00</span><span class="sxs-lookup"><span data-stu-id="b18fc-137">Latency : 00:00:00</span></span>

<span data-ttu-id="b18fc-138">Erreur : 11004, le nom demandé est valide, mais aucune donnée de la requête</span><span class="sxs-lookup"><span data-stu-id="b18fc-138">Error : 11004, The requested name is valid but no data of the requested</span></span>

<span data-ttu-id="b18fc-139">type détecté</span><span class="sxs-lookup"><span data-stu-id="b18fc-139">type was found</span></span>

<span data-ttu-id="b18fc-140">Diagnostic</span><span class="sxs-lookup"><span data-stu-id="b18fc-140">Diagnosis :</span></span>

<span data-ttu-id="b18fc-141">Test-CsLisConfiguration : aucun cluster correspondant détecté dans la topologie.</span><span class="sxs-lookup"><span data-stu-id="b18fc-141">Test-CsLisConfiguration : No matching cluster found in topology.</span></span>

<span data-ttu-id="b18fc-142">Par exemple, la sortie précédente inclut la remarque « aucun cluster correspondant trouvé dans la topologie ».</span><span class="sxs-lookup"><span data-stu-id="b18fc-142">For example, the previous output includes the note “No matching cluster found in topology.”</span></span> <span data-ttu-id="b18fc-143">Il s’agit généralement d’un problème avec le serveur Edge : les LIS utilisant le serveur de périphérie pour se connecter au fournisseur de services et valider les adresses.</span><span class="sxs-lookup"><span data-stu-id="b18fc-143">That typically indicates a problem with the Edge Server: the LIS using the Edge Server to connect to the service provider and validate addresses.</span></span>

<span data-ttu-id="b18fc-144">Si Test-CsLisConfiguration échoue, vous souhaiterez peut-être réexécuter le test, cette fois-ci, y compris le paramètre Verbose :</span><span class="sxs-lookup"><span data-stu-id="b18fc-144">If Test-CsLisConfiguration fails then you might want to rerun the test, this time including the Verbose parameter:</span></span>

    Test-CsLisConfiguration -TargetFqdn "atl-cs-001.litwareinc.com" -Verbose

<span data-ttu-id="b18fc-145">Lorsque le paramètre Verbose est inclus, Test-CsLisConfiguration renvoie un compte étape par étape de chaque action qu’il a effectuée lors de la vérification de la capacité de l’utilisateur spécifié à se connecter à Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b18fc-145">When the Verbose parameter is included, Test-CsLisConfiguration will return a step-by-step account of each action it tried when it checked the ability of the specified user to log on to Lync Server.</span></span> <span data-ttu-id="b18fc-146">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="b18fc-146">For example:</span></span>

<span data-ttu-id="b18fc-147">Appel de service d’information d’emplacement.</span><span class="sxs-lookup"><span data-stu-id="b18fc-147">Calling Location Information Service.</span></span>

<span data-ttu-id="b18fc-148">Path du service = https://atl-cs-001.litwareinc.com:443/locationinformation/liservice.svc</span><span class="sxs-lookup"><span data-stu-id="b18fc-148">Service Path = https://atl-cs-001.litwareinc.com:443/locationinformation/liservice.svc</span></span>

<span data-ttu-id="b18fc-149">Sous-réseau =</span><span class="sxs-lookup"><span data-stu-id="b18fc-149">Subnet =</span></span>

<span data-ttu-id="b18fc-150">BssId = 5</span><span class="sxs-lookup"><span data-stu-id="b18fc-150">BssId = 5</span></span>

<span data-ttu-id="b18fc-151">ChassisId =</span><span class="sxs-lookup"><span data-stu-id="b18fc-151">ChassisId =</span></span>

<span data-ttu-id="b18fc-152">PortId =</span><span class="sxs-lookup"><span data-stu-id="b18fc-152">PortId =</span></span>

<span data-ttu-id="b18fc-153">PortIdSubType = type non défini</span><span class="sxs-lookup"><span data-stu-id="b18fc-153">PortIdSubType = Undefined Type</span></span>

<span data-ttu-id="b18fc-154">Mac</span><span class="sxs-lookup"><span data-stu-id="b18fc-154">Mac</span></span>

<span data-ttu-id="b18fc-155">Une demande de service Web d’information d’emplacement d’exception a échoué avec le code de réponse Item400. '</span><span class="sxs-lookup"><span data-stu-id="b18fc-155">An exception 'Location Information Web Service request has failed with a response code Item400.'</span></span> <span data-ttu-id="b18fc-156">Il s’est produit lors de l’exécution du flux de travail Microsoft. RTC. SyntheticTrsnactions. flux de travail. STLisConfigurationWorkflow.</span><span class="sxs-lookup"><span data-stu-id="b18fc-156">occurred during Workflow Microsoft.Rtc.SyntheticTrsnactions.Workflows.STLisConfigurationWorkflow execution.</span></span>

<span data-ttu-id="b18fc-157">Si vous examinez soigneusement la sortie précédente, vous verrez que l’applet de la cmdlet a essayé d’appeler le service d’information d’emplacement.</span><span class="sxs-lookup"><span data-stu-id="b18fc-157">If you examine the previous output closely, you’ll see that the cmdlet failed after it tried to call the Location Information Service.</span></span> <span data-ttu-id="b18fc-158">L’un des paramètres qui ont été utilisés dans cet appel est le suivant :</span><span class="sxs-lookup"><span data-stu-id="b18fc-158">One of the parameters that were used in that call was this:</span></span>

<span data-ttu-id="b18fc-159">BssId = 5</span><span class="sxs-lookup"><span data-stu-id="b18fc-159">BssId = 5</span></span>

<span data-ttu-id="b18fc-160">Ce n’est pas une valeur valide pour le champ BssID (Service Set Identifier).</span><span class="sxs-lookup"><span data-stu-id="b18fc-160">That’s not a valid value for the Basic Service Set Identifier (BssID).</span></span> <span data-ttu-id="b18fc-161">Au lieu de cela, un BssID doit ressembler à ceci :</span><span class="sxs-lookup"><span data-stu-id="b18fc-161">Instead, a BssID should resemble this:</span></span>

<span data-ttu-id="b18fc-162">12-34-56-78-90-AB</span><span class="sxs-lookup"><span data-stu-id="b18fc-162">12-34-56-78-90-ab</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="b18fc-163">Raisons pour lesquelles le test peut avoir échoué</span><span class="sxs-lookup"><span data-stu-id="b18fc-163">Reasons why the test might have failed</span></span>

<span data-ttu-id="b18fc-164">Voici quelques raisons courantes pour lesquelles Test-CsLisConfiguration risque d’échouer :</span><span class="sxs-lookup"><span data-stu-id="b18fc-164">Here are some common reasons why Test-CsLisConfiguration might fail:</span></span>

  - <span data-ttu-id="b18fc-165">Une valeur de paramètre incorrecte a été fournie.</span><span class="sxs-lookup"><span data-stu-id="b18fc-165">An incorrect parameter value was supplied.</span></span> <span data-ttu-id="b18fc-166">Comme indiqué dans l’exemple précédent, les paramètres facultatifs doivent être correctement configurés ou le test échoue.</span><span class="sxs-lookup"><span data-stu-id="b18fc-166">As shown in the previous example, the optional parameters must be configured correctly or the test will fail.</span></span> <span data-ttu-id="b18fc-167">Réexécutez la commande sans les paramètres facultatifs et déterminez si l’opération aboutit.</span><span class="sxs-lookup"><span data-stu-id="b18fc-167">Rerun the command without the optional parameters and see whether that succeeds.</span></span>

<span data-ttu-id="b18fc-168"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b18fc-168"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

