---
title: 'Lync Server 2013 : possibilité de test d’utiliser l’extension de groupe'
description: 'Lync Server 2013 : possibilité de test d’utiliser l’extension de groupe.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing ability to employ group expansion
ms:assetid: 9b0fc954-6f9c-411a-ab32-94ebabc42de2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn743836(v=OCS.15)
ms:contentKeyID: 63969634
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6267bc2099fc420c5c57e1ef80f4bf4491334938
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441108"
---
# <a name="testing-ability-to-employ-group-expansion-in-lync-server-2013"></a><span data-ttu-id="b18fc-103">Fonctionnalité de test permettant d’utiliser l’extension de groupe dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b18fc-103">Testing ability to employ group expansion in Lync Server 2013</span></span>

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
<p><span data-ttu-id="b18fc-112">Lors de l’exécution à l’aide d’une instance distante de Windows PowerShell, un rôle RBAC doit être attribué aux utilisateurs qui ont l’autorisation d’exécuter l’applet de commande Test-CsGroupExpansion.</span><span class="sxs-lookup"><span data-stu-id="b18fc-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsGroupExpansion cmdlet.</span></span> <span data-ttu-id="b18fc-113">Pour afficher la liste de tous les rôles RBAC qui peuvent utiliser cette applet de commande, exécutez la commande suivante à partir de l’invite Windows PowerShell :</span><span class="sxs-lookup"><span data-stu-id="b18fc-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsGroupExpansion&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="b18fc-114">Description</span><span class="sxs-lookup"><span data-stu-id="b18fc-114">Description</span></span>

<span data-ttu-id="b18fc-115">L’applet de passe Test-CsGroupExpansion vous permet de déterminer si l’extension du groupe est appliquée au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="b18fc-115">The Test-CsGroupExpansion cmdlet lets you determine whether group expansion is working within your organization.</span></span> <span data-ttu-id="b18fc-116">Lorsque l’extension du groupe est activée, les utilisateurs configurent les groupes de distribution en tant que contact.</span><span class="sxs-lookup"><span data-stu-id="b18fc-116">When group expansion is enabled, users configure distribution groups as a contact.</span></span> <span data-ttu-id="b18fc-117">Cela signifie que les utilisateurs peuvent alors envoyer le même message instantané à tous les membres du groupe en envoyant le message au groupe plutôt qu’à des membres individuels du groupe.</span><span class="sxs-lookup"><span data-stu-id="b18fc-117">That means that those users can then send the same instant message to all the group members by addressing the message to the group instead of to individual members of that group.</span></span> <span data-ttu-id="b18fc-118">L’extension de groupe vous permet d’afficher rapidement et facilement tous les membres du groupe et leur statut actuel.</span><span class="sxs-lookup"><span data-stu-id="b18fc-118">Group expansion enables you to quickly and easily view all the group members and their current status.</span></span>

<span data-ttu-id="b18fc-119">À l’aide de l’applet de contrôle Test-CsGroupExpansion, vous spécifiez un groupe de distribution Active Directory à l’aide de l’adresse de messagerie du groupe.</span><span class="sxs-lookup"><span data-stu-id="b18fc-119">With the Test-CsGroupExpansion cmdlet, you specify an Active Directory distribution group by using the group’s email address.</span></span> <span data-ttu-id="b18fc-120">Test-CsGroupExpansion ensuite utiliser l’extension de groupe pour récupérer l’appartenance au groupe et comparer la liste récupérée à l’appartenance de l’adresse de messagerie de groupe que vous avez fournie.</span><span class="sxs-lookup"><span data-stu-id="b18fc-120">Test-CsGroupExpansion then uses group expansion to retrieve the group membership and compare the retrieved list to the membership of the group email address that you supplied.</span></span> <span data-ttu-id="b18fc-121">Si les deux listes correspondent, l’extension du groupe fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="b18fc-121">If the two lists match, then group expansion is working correctly.</span></span> <span data-ttu-id="b18fc-122">Notez que vous pouvez tester l’extension du groupe de deux manières : en testant le service proprement dit ou en testant le service Web associé.</span><span class="sxs-lookup"><span data-stu-id="b18fc-122">Note that you can test group expansion in two ways: by testing the service itself or by testing the associated web service.</span></span>

<span data-ttu-id="b18fc-123">Pour plus d’informations, consultez la documentation d’aide de l’applet de [contrôle test-CsGroupExpansion](https://docs.microsoft.com/powershell/module/skype/Test-CsGroupExpansion) .</span><span class="sxs-lookup"><span data-stu-id="b18fc-123">For more information, see the Help documentation for the [Test-CsGroupExpansion](https://docs.microsoft.com/powershell/module/skype/Test-CsGroupExpansion) cmdlet.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="b18fc-124">Exécution du test</span><span class="sxs-lookup"><span data-stu-id="b18fc-124">Running the test</span></span>

<span data-ttu-id="b18fc-125">Vous pouvez exécuter l’applet de contrôle Test-CsGroupExpansion à l’aide d’un compte de test préconfiguré (voir Configuration de comptes de test pour exécuter des tests Lync Server) ou du compte d’un utilisateur qui a été activé pour Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b18fc-125">The Test-CsGroupExpansion cmdlet can be run using either a preconfigured test account (see Setting Up Test Accounts for Running Lync Server Tests) or the account of any user who was enabled for Lync Server.</span></span> <span data-ttu-id="b18fc-126">Pour effectuer cette vérification à l’aide d’un compte de test, vous devez simplement spécifier le nom de domaine complet (FQDN) du pool de serveurs Lync testé et l’adresse de courrier d’un groupe de distribution valide.</span><span class="sxs-lookup"><span data-stu-id="b18fc-126">To run this check using a test account, you just have to specify the FQDN of the Lync Server pool being tested and the email address for a valid distribution group.</span></span> <span data-ttu-id="b18fc-127">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="b18fc-127">For example:</span></span>

    Test-CsGroupExpansion -TargetFqdn "atl-cs-001.litwareinc.com" -GroupEmailAddress "Sales@litwareinc.com"

<span data-ttu-id="b18fc-128">Pour effectuer cette vérification à l’aide d’un compte d’utilisateur réel, vous devez d’abord créer un objet d’informations d’identification Lync Server contenant le nom et le mot de passe du compte.</span><span class="sxs-lookup"><span data-stu-id="b18fc-128">To run this check using an actual user account, you must first create a Lync Server credentials object that contains the account name and password.</span></span> <span data-ttu-id="b18fc-129">Lorsque le système appelle test-CsGroupExpansion, vous devez inclure l’objet Credential et l’adresse SIP associée au compte.</span><span class="sxs-lookup"><span data-stu-id="b18fc-129">You must then include that credentials object and the SIP address assigned to the account when the system calls Test-CsGroupExpansion:</span></span>

    $credential = Get-Credential "litwareinc\kenmyer"
    Test-CsGroupExpansion -TargetFqdn "atl-cs-001.litwareinc.com" -GroupEmailAddress "Sales@litwareinc.com" -UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential

<span data-ttu-id="b18fc-130">Pour plus d’informations, consultez la documentation d’aide de l’applet de [contrôle test-CsGroupExpansion](https://docs.microsoft.com/powershell/module/skype/Test-CsGroupExpansion) .</span><span class="sxs-lookup"><span data-stu-id="b18fc-130">For more information, see the Help documentation for the [Test-CsGroupExpansion](https://docs.microsoft.com/powershell/module/skype/Test-CsGroupExpansion) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="b18fc-131">Détermination du succès ou de l’échec</span><span class="sxs-lookup"><span data-stu-id="b18fc-131">Determining success or failure</span></span>

<span data-ttu-id="b18fc-132">Si l’utilisateur spécifié peut utiliser l’extension de groupe, vous recevrez une sortie similaire à celle-ci avec la propriété Result marquée comme **réussie :**</span><span class="sxs-lookup"><span data-stu-id="b18fc-132">If the specified user can use group expansion, you'll receive output similar to this with the Result property marked as **Success:**</span></span>

<span data-ttu-id="b18fc-133">TargetUri https://atl-cs-001.litwareinc.com:443/groupexpansion/service.svc</span><span class="sxs-lookup"><span data-stu-id="b18fc-133">TargetUri : https://atl-cs-001.litwareinc.com:443/groupexpansion/service.svc</span></span>

<span data-ttu-id="b18fc-134">TargetFqdn : atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="b18fc-134">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="b18fc-135">Résultat : réussite</span><span class="sxs-lookup"><span data-stu-id="b18fc-135">Result : Success</span></span>

<span data-ttu-id="b18fc-136">Latence : 00:00:01.1234976</span><span class="sxs-lookup"><span data-stu-id="b18fc-136">Latency : 00:00:01.1234976</span></span>

<span data-ttu-id="b18fc-137">Error</span><span class="sxs-lookup"><span data-stu-id="b18fc-137">Error :</span></span>

<span data-ttu-id="b18fc-138">Diagnostic</span><span class="sxs-lookup"><span data-stu-id="b18fc-138">Diagnosis :</span></span>

<span data-ttu-id="b18fc-139">Si l’utilisateur spécifié ne peut pas utiliser l’extension de groupe, le résultat s’affichera en tant qu’échec et des informations supplémentaires seront enregistrées dans les propriétés d’erreur et de diagnostic :</span><span class="sxs-lookup"><span data-stu-id="b18fc-139">If the specified user can't use group expansion, then the Result will be shown as Failure and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="b18fc-140">TargetUri https://atl-cs-001.litwareinc.com:443/groupexpansion/service.svc</span><span class="sxs-lookup"><span data-stu-id="b18fc-140">TargetUri : https://atl-cs-001.litwareinc.com:443/groupexpansion/service.svc</span></span>

<span data-ttu-id="b18fc-141">TargetFqdn : atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="b18fc-141">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="b18fc-142">Résultat : échec</span><span class="sxs-lookup"><span data-stu-id="b18fc-142">Result : Failure</span></span>

<span data-ttu-id="b18fc-143">Latence : 00:00:00</span><span class="sxs-lookup"><span data-stu-id="b18fc-143">Latency : 00:00:00</span></span>

<span data-ttu-id="b18fc-144">Error</span><span class="sxs-lookup"><span data-stu-id="b18fc-144">Error :</span></span>

<span data-ttu-id="b18fc-145">Diagnostic</span><span class="sxs-lookup"><span data-stu-id="b18fc-145">Diagnosis :</span></span>

<span data-ttu-id="b18fc-146">Test-CsGroupExpansion : le point de terminaison n’a pas pu s’inscrire.</span><span class="sxs-lookup"><span data-stu-id="b18fc-146">Test-CsGroupExpansion : The endpoint was unable to register.</span></span> <span data-ttu-id="b18fc-147">Afficher le code d’après pour une raison spécifique.</span><span class="sxs-lookup"><span data-stu-id="b18fc-147">See the ErrorCode for specific reason.</span></span>

<span data-ttu-id="b18fc-148">La sortie précédente indique que le test a échoué, car l’utilisateur spécifié n’a pas pu s’inscrire sur Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b18fc-148">The previous output states that the test failed because the specified user was unable to register with Lync Server.</span></span> <span data-ttu-id="b18fc-149">Cela se produit généralement si le compte de test n’existe pas ou n’a pas été activé pour Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b18fc-149">This will typically occur if the test account does not exist or has not enabled for Lync Server.</span></span> <span data-ttu-id="b18fc-150">Vous pouvez vérifier que le compte existe et déterminez si le compte a été activé pour nm-OCS-14-3e en exécutant une commande semblable à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="b18fc-150">You can verify that the account exists, and determine whether or not the account has been enabled for nm-ocs-14-3rd by running a command similar to the following:</span></span>

    Get-CsUser -Identity "sip:kenmyer@litwareinc.com" | Select-Object SipAddress, Enabled

<span data-ttu-id="b18fc-151">Si Test-CsGroupExpansion échoue, il est possible que vous souhaitiez réexécuter le test, cette fois-ci, y compris le paramètre Verbose :</span><span class="sxs-lookup"><span data-stu-id="b18fc-151">If Test-CsGroupExpansion fails, then you might want to rerun the test, this time including the Verbose parameter:</span></span>

    Test-CsGroupExpansion -TargetFqdn "atl-cs-001.litwareinc.com" -GroupEmailAddress "Sales@litwareinc.com" -Verbose

<span data-ttu-id="b18fc-152">Lorsque le paramètre Verbose est inclus Test-CsGroupExpansion renvoie un compte étape par étape de chaque action qu’il a effectuée lorsqu’il a activé la fonctionnalité de connexion de l’utilisateur à Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b18fc-152">When the Verbose parameter is included Test-CsGroupExpansion will return a step-by-step account of each action it tried when it checked the ability of the specified user to log on to Lync Server.</span></span> <span data-ttu-id="b18fc-153">Par exemple, cette sortie indique que le groupe de distribution spécifié est introuvable :</span><span class="sxs-lookup"><span data-stu-id="b18fc-153">For example, this output indicates that the specified distribution group couldn't be found:</span></span>

<span data-ttu-id="b18fc-154">Essayez d’obtenir le ticket Web.</span><span class="sxs-lookup"><span data-stu-id="b18fc-154">Trying to get web ticket.</span></span>

<span data-ttu-id="b18fc-155">URL du service Web : https://atl-cs-001.litwareinc.com:443/WebTicket/WebTicketService.svc</span><span class="sxs-lookup"><span data-stu-id="b18fc-155">Web Service url : https://atl-cs-001.litwareinc.com:443/WebTicket/WebTicketService.svc</span></span>

<span data-ttu-id="b18fc-156">À l’aide de l’authentification NTLM/Kerb.</span><span class="sxs-lookup"><span data-stu-id="b18fc-156">Using NTLM/Kerb auth.</span></span>

<span data-ttu-id="b18fc-157">GetWebTicketActivity terminé.</span><span class="sxs-lookup"><span data-stu-id="b18fc-157">GetWebTicketActivity completed.</span></span>

<span data-ttu-id="b18fc-158">Activité « VerifyDistributionList » démarrée.</span><span class="sxs-lookup"><span data-stu-id="b18fc-158">'VerifyDistributionList' activity started.</span></span>

<span data-ttu-id="b18fc-159">DLX état de réponse du service Web est : NotFound.</span><span class="sxs-lookup"><span data-stu-id="b18fc-159">DLX Web Service Response Status is: NotFound.</span></span>

<span data-ttu-id="b18fc-160">Activité « VerifyDistributionList » terminée en « 0,2597923 » secondes.</span><span class="sxs-lookup"><span data-stu-id="b18fc-160">'VerifyDistributionList' activity completed in '0.2597923' secs.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="b18fc-161">Raisons pour lesquelles le test peut avoir échoué</span><span class="sxs-lookup"><span data-stu-id="b18fc-161">Reasons why the test might have failed</span></span>

<span data-ttu-id="b18fc-162">Voici quelques raisons courantes pour lesquelles Test-CsGroupExpansion risque d’échouer :</span><span class="sxs-lookup"><span data-stu-id="b18fc-162">Here are some common reasons why Test-CsGroupExpansion might fail:</span></span>

  - <span data-ttu-id="b18fc-163">Vous avez spécifié un compte d’utilisateur non valide.</span><span class="sxs-lookup"><span data-stu-id="b18fc-163">You specified an invalid user account.</span></span> <span data-ttu-id="b18fc-164">Vous pouvez vérifier qu’un compte d’utilisateur existe en exécutant une commande semblable à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="b18fc-164">You can verify that a user account exists by running a command similar to this:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com"

  - <span data-ttu-id="b18fc-165">Le compte d’utilisateur est valide, mais le compte n’est pas activé pour Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b18fc-165">The user account is valid, but the account is currently not enabled for Lync Server.</span></span> <span data-ttu-id="b18fc-166">Pour vérifier qu’un compte d’utilisateur a été activé pour Lync Server, exécutez une commande semblable à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="b18fc-166">To verify that a user account was enabled for Lync Server, run a command similar to the following:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object Enabled
    
    <span data-ttu-id="b18fc-167">Si la propriété Enabled est définie sur false, cela signifie que l’utilisateur n’est actuellement pas activé pour Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b18fc-167">If the Enabled property is set to False, that means that the user is currently not enabled for Lync Server.</span></span>

  - <span data-ttu-id="b18fc-168">L’extension du groupe est peut-être désactivée.</span><span class="sxs-lookup"><span data-stu-id="b18fc-168">Group expansion might be disabled.</span></span> <span data-ttu-id="b18fc-169">Il est possible de désactiver l’extension de groupe.</span><span class="sxs-lookup"><span data-stu-id="b18fc-169">It is possible to turn off group expansion.</span></span> <span data-ttu-id="b18fc-170">Si l’extension du groupe a été désactivée, l’applet de Test-CsGroupExpansion.</span><span class="sxs-lookup"><span data-stu-id="b18fc-170">If group expansion was disabled then the Test-CsGroupExpansion cmdlet will fail.</span></span> <span data-ttu-id="b18fc-171">Pour déterminer si l’extension du groupe est activée, utilisez une commande semblable à celle-ci :</span><span class="sxs-lookup"><span data-stu-id="b18fc-171">To determine whether group expansion is enabled, use a command similar to this:</span></span>
    
        Get-CsWebServiceConfiguration | Select-Object Identity, EnableGroupExpansion

<span data-ttu-id="b18fc-172"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b18fc-172"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

