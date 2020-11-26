---
title: 'Lync Server 2013 : test de l’accès au magasin de contacts unifié'
description: 'Lync Server 2013 : test de l’accès au magasin de contacts unifié'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing Unified Contact Store access
ms:assetid: 761f46bd-2e14-4f40-82b9-afa1eaa816b0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn727309(v=OCS.15)
ms:contentKeyID: 63969621
ms.date: 05/16/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 58238685133c51130c414e0d7a8cd761d0233f5d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440940"
---
# <a name="testing-unified-contact-store-access-in-lync-server-2013"></a><span data-ttu-id="988fd-103">Test de l’accès au magasin de contacts unifié dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="988fd-103">Testing Unified Contact Store access in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="988fd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="988fd-104">

<span> </span></span></span>

<span data-ttu-id="988fd-105">_**Dernière modification de la rubrique :** 2015-05-15_</span><span class="sxs-lookup"><span data-stu-id="988fd-105">_**Topic Last Modified:** 2015-05-15_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="988fd-106">Échéancier de vérification</span><span class="sxs-lookup"><span data-stu-id="988fd-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="988fd-107">Jour</span><span class="sxs-lookup"><span data-stu-id="988fd-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="988fd-108">Outil de test</span><span class="sxs-lookup"><span data-stu-id="988fd-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="988fd-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="988fd-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="988fd-110">Autorisations requises</span><span class="sxs-lookup"><span data-stu-id="988fd-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="988fd-111">Lorsque l’application est exécutée localement à l’aide de Lync Server Management Shell, les utilisateurs doivent être membres du groupe de sécurité RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="988fd-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="988fd-112">Lors de l’exécution à l’aide d’une instance distante de Windows PowerShell, un rôle RBAC doit être attribué aux utilisateurs qui ont l’autorisation d’exécuter l’applet de commande <strong>test-CsUnifiedContactStore</strong> .</span><span class="sxs-lookup"><span data-stu-id="988fd-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the <strong>Test-CsUnifiedContactStore</strong> cmdlet.</span></span> <span data-ttu-id="988fd-113">Pour afficher la liste de tous les rôles RBAC qui peuvent utiliser cette applet de commande, exécutez la commande suivante à partir de l’invite Windows PowerShell :</span><span class="sxs-lookup"><span data-stu-id="988fd-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsUnifiedContactStore&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="988fd-114">Description</span><span class="sxs-lookup"><span data-stu-id="988fd-114">Description</span></span>

<span data-ttu-id="988fd-115">Le magasin de contacts unifié introduit dans Lync Server 2013 permet aux administrateurs de stocker les contacts d’un utilisateur dans Microsoft Exchange Server 2013 au lieu de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="988fd-115">The unified contact store introduced in Lync Server 2013 gives administrators the option of storing a user's contacts in Microsoft Exchange Server 2013 instead of in Lync Server.</span></span> <span data-ttu-id="988fd-116">Cela permet à l’utilisateur d’accéder au même jeu de contacts dans Outlook Web Access en plus de Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="988fd-116">This allows the user to access the same set of contacts in Outlook Web Access in addition to Lync 2013.</span></span> <span data-ttu-id="988fd-117">(Vous pouvez continuer à stocker vos contacts dans Lync Server.</span><span class="sxs-lookup"><span data-stu-id="988fd-117">(Or, you can continue to store contacts in Lync Server.</span></span> <span data-ttu-id="988fd-118">Dans ce cas, les utilisateurs doivent tenir compte de deux ensembles de contacts distincts : un pour une utilisation avec Outlook et Outlook Web Access, et un pour une utilisation avec Lync 2013.)</span><span class="sxs-lookup"><span data-stu-id="988fd-118">In that case, users will have to maintain two separate sets of contacts: one for use with Outlook and Outlook Web Access, and one for use with Lync 2013.)</span></span>

<span data-ttu-id="988fd-119">Vous pouvez déterminer si les contacts d’un utilisateur ont été déplacés dans le magasin de contacts unifié en exécutant l’applet de **contrôle CsUnifiedContactStore de test** .</span><span class="sxs-lookup"><span data-stu-id="988fd-119">You can determine whether or not a user's contacts were moved to the unified contact store by running the **Test-CsUnifiedContactStore** cmdlet.</span></span> <span data-ttu-id="988fd-120">L’applet de connexion **test-CsUnifiedContactStore** prend le compte d’utilisateur spécifié, se connecte au magasin de contacts unifié et tente de récupérer un contact pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="988fd-120">The **Test-CsUnifiedContactStore** cmdlet will take the specified user account, connect to the unified contact store, and attempt to retrieve a contact for the user.</span></span> <span data-ttu-id="988fd-121">Si aucun contact ne peut être récupéré, la commande échoue avec le message «aucun contact n’a été reçu pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="988fd-121">If no contacts can be retrieved then the command will fail together with the message "No contacts were received for the user.</span></span> <span data-ttu-id="988fd-122">Vérifiez qu’il existe des contacts pour l’utilisateur.»</span><span class="sxs-lookup"><span data-stu-id="988fd-122">Verify that contacts exist for the user."</span></span>

<span data-ttu-id="988fd-123">Notez que l’applet **de contrôle test-CsUnifiedContactStore** échoue si l’utilisateur a effectué une migration réussie vers le magasin de contacts unifié, mais qu’aucun contact n’a été trouvé dans sa liste de contacts.</span><span class="sxs-lookup"><span data-stu-id="988fd-123">Note that the **Test-CsUnifiedContactStore** cmdlet will fail if the user has successfully migrated to the unified contact store but has no contacts on his or her Contacts list.</span></span> <span data-ttu-id="988fd-124">L’utilisateur spécifié doit avoir au moins un contact pour que l’applet de **contrôle test-CsUnifiedContactStore** se termine correctement.</span><span class="sxs-lookup"><span data-stu-id="988fd-124">The specified user must have at least one contact for the **Test-CsUnifiedContactStore** cmdlet to complete successfully.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="988fd-125">Exécution du test</span><span class="sxs-lookup"><span data-stu-id="988fd-125">Running the test</span></span>

<span data-ttu-id="988fd-126">Les commandes indiquées dans l’exemple ci-dessous déterminent si les contacts de l’utilisateur litwareinc \\ kenmyer se trouvent dans le magasin de contacts unifié.</span><span class="sxs-lookup"><span data-stu-id="988fd-126">The commands shown in the following example determine whether contacts for the user litwareinc\\kenmyer can be found in the unified contact store.</span></span> <span data-ttu-id="988fd-127">Pour ce faire, la première commande de l’exemple utilise l’applet de commande **Get-Credential** pour créer un objet d’information d’identification d’interface de ligne de commande Windows PowerShell pour l’utilisateur litwareinc \\ kenmyer.</span><span class="sxs-lookup"><span data-stu-id="988fd-127">To do this, the first command in the example uses the **Get-Credential** cmdlet to create a Windows PowerShell command-line interface credentials object for the user litwareinc\\kenmyer.</span></span> <span data-ttu-id="988fd-128">Notez que vous devez fournir le mot de passe de ce compte pour créer un objet d’informations d’identification valide et vérifier que l’applet de contrôle **CsUnifiedContactStore** peut exécuter sa vérification.</span><span class="sxs-lookup"><span data-stu-id="988fd-128">Note that you must supply the password for this account to create a valid credentials object and to make sure that the **Test-CsUnifiedContactStore** cmdlet can run its check.</span></span>

<span data-ttu-id="988fd-129">La deuxième commande de l’exemple utilise l’objet Credentials fourni ($x) et l’adresse SIP de l’utilisateur litwareinc \\ kenmyer pour déterminer si ses contacts sont accessibles dans le magasin de contacts unifié.</span><span class="sxs-lookup"><span data-stu-id="988fd-129">The second command in the example uses the supplied credentials object ($x) and the SIP address of the user litwareinc\\kenmyer to determine whether his contacts can be found in the unified contact store.</span></span>

    $credential = Get-Credential "litwareinc\kenmyer"
    
    Test-CsUnifiedContactStore -TargetFqdn "atl-cs-001.litwareinc.com" -UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="988fd-130">Détermination du succès ou de l’échec</span><span class="sxs-lookup"><span data-stu-id="988fd-130">Determining success or failure</span></span>

<span data-ttu-id="988fd-131">Si l’accès au magasin de contacts est correctement configuré, vous recevrez une sortie similaire à celle-ci, avec la propriété Result marquée comme **réussie :**</span><span class="sxs-lookup"><span data-stu-id="988fd-131">If access to the contact store is configured correctly, you'll receive output similar to this, with the Result property marked as **Success:**</span></span>

<span data-ttu-id="988fd-132">Nom de domaine complet (FQDN) cible : atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="988fd-132">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="988fd-133">Résultat : réussite</span><span class="sxs-lookup"><span data-stu-id="988fd-133">Result : Success</span></span>

<span data-ttu-id="988fd-134">Latence : 00:00:14.9862716</span><span class="sxs-lookup"><span data-stu-id="988fd-134">Latency : 00:00:14.9862716</span></span>

<span data-ttu-id="988fd-135">Message d’erreur :</span><span class="sxs-lookup"><span data-stu-id="988fd-135">Error Message :</span></span>

<span data-ttu-id="988fd-136">Diagnostic</span><span class="sxs-lookup"><span data-stu-id="988fd-136">Diagnosis :</span></span>

<span data-ttu-id="988fd-137">Si l’accès au magasin de contacts n’est pas configuré correctement, le résultat est affiché en tant qu' **échec** et des informations supplémentaires sont enregistrées dans les propriétés d’erreur et de diagnostic :</span><span class="sxs-lookup"><span data-stu-id="988fd-137">If access to the contact store is not configured correctly, the Result will be shown as **Failure**, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="988fd-138">AVERTISSEMENT : impossible de lire le numéro de port du Bureau d’enregistrement pour le nom complet fourni</span><span class="sxs-lookup"><span data-stu-id="988fd-138">WARNING: Failed to read Registrar port number for the given fully qualified</span></span>

<span data-ttu-id="988fd-139">nom de domaine (FQDN).</span><span class="sxs-lookup"><span data-stu-id="988fd-139">domain name (FQDN).</span></span> <span data-ttu-id="988fd-140">Utilisation du numéro de port de bureau par défaut.</span><span class="sxs-lookup"><span data-stu-id="988fd-140">Using default Registrar port number.</span></span> <span data-ttu-id="988fd-141">Sauf</span><span class="sxs-lookup"><span data-stu-id="988fd-141">Exception:</span></span>

<span data-ttu-id="988fd-142">System. InvalidOperationException : aucun cluster correspondant détecté dans la topologie.</span><span class="sxs-lookup"><span data-stu-id="988fd-142">System.InvalidOperationException: No matching cluster found in topology.</span></span>

<span data-ttu-id="988fd-143">dès</span><span class="sxs-lookup"><span data-stu-id="988fd-143">at</span></span>

<span data-ttu-id="988fd-144">Microsoft. RTC. Management. SyntheticTransactions. SipSyntheticTransaction. TryRetri</span><span class="sxs-lookup"><span data-stu-id="988fd-144">Microsoft.Rtc.Management.SyntheticTransactions.SipSyntheticTransaction.TryRetri</span></span>

<span data-ttu-id="988fd-145">eveRegistrarPortFromTopology (Int32& registrarPortNumber)</span><span class="sxs-lookup"><span data-stu-id="988fd-145">eveRegistrarPortFromTopology(Int32& registrarPortNumber)</span></span>

<span data-ttu-id="988fd-146">Nom de domaine complet (FQDN) cible : atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="988fd-146">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="988fd-147">Résultat : échec</span><span class="sxs-lookup"><span data-stu-id="988fd-147">Result : Failure</span></span>

<span data-ttu-id="988fd-148">Latence : 00:00:00</span><span class="sxs-lookup"><span data-stu-id="988fd-148">Latency : 00:00:00</span></span>

<span data-ttu-id="988fd-149">Message d’erreur : 10060, une tentative de connexion a échoué car la partie connectée</span><span class="sxs-lookup"><span data-stu-id="988fd-149">Error Message : 10060, A connection attempt failed because the connected party</span></span>

<span data-ttu-id="988fd-150">ne répond pas correctement après un certain temps, ou</span><span class="sxs-lookup"><span data-stu-id="988fd-150">did not properly respond after a period of time, or</span></span>

<span data-ttu-id="988fd-151">échec de la connexion établie, car l’hôte connecté a</span><span class="sxs-lookup"><span data-stu-id="988fd-151">established connection failed because connected host has</span></span>

<span data-ttu-id="988fd-152">échec de la réponse à 10.188.116.96:5061</span><span class="sxs-lookup"><span data-stu-id="988fd-152">failed to respond 10.188.116.96:5061</span></span>

<span data-ttu-id="988fd-153">Exception interne : une tentative de connexion a échoué, car le</span><span class="sxs-lookup"><span data-stu-id="988fd-153">Inner Exception:A connection attempt failed because the</span></span>

<span data-ttu-id="988fd-154">la fête connectée ne répond pas correctement après un délai de</span><span class="sxs-lookup"><span data-stu-id="988fd-154">connected party did not properly respond after a period of</span></span>

<span data-ttu-id="988fd-155">heure ou échec de la connexion en raison d’un hôte connecté</span><span class="sxs-lookup"><span data-stu-id="988fd-155">time, or established connection failed because connected host</span></span>

<span data-ttu-id="988fd-156">échec de la réponse à 10.188.116.96:5061</span><span class="sxs-lookup"><span data-stu-id="988fd-156">has failed to respond 10.188.116.96:5061</span></span>

<span data-ttu-id="988fd-157">Diagnostic</span><span class="sxs-lookup"><span data-stu-id="988fd-157">Diagnosis :</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="988fd-158">Raisons pour lesquelles le test peut avoir échoué</span><span class="sxs-lookup"><span data-stu-id="988fd-158">Reasons why the test might have failed</span></span>

<span data-ttu-id="988fd-159">Voici quelques raisons courantes pour lesquelles **les tests-CsUnifiedContactStore** peuvent échouer :</span><span class="sxs-lookup"><span data-stu-id="988fd-159">Here are some common reasons why **Test-CsUnifiedContactStore** might fail:</span></span>

  - <span data-ttu-id="988fd-160">Une valeur de paramètre incorrecte a été fournie.</span><span class="sxs-lookup"><span data-stu-id="988fd-160">An incorrect parameter value was supplied.</span></span> <span data-ttu-id="988fd-161">S’il est utilisé, les paramètres facultatifs doivent être correctement configurés ou le test échoue.</span><span class="sxs-lookup"><span data-stu-id="988fd-161">If used, the optional parameters must be configured correctly or the test will fail.</span></span> <span data-ttu-id="988fd-162">Réexécutez la commande sans les paramètres facultatifs et déterminez si l’opération aboutit.</span><span class="sxs-lookup"><span data-stu-id="988fd-162">Rerun the command without the optional parameters and see whether that succeeds.</span></span>

  - <span data-ttu-id="988fd-163">La connexion au magasin de contacts unifié a échoué et la tentative de récupération d’un contact pour l’utilisateur n’est pas possible.</span><span class="sxs-lookup"><span data-stu-id="988fd-163">Connect to the unified contact store failed, and the attempt to retrieve a contact for the user was not possible.</span></span> <span data-ttu-id="988fd-164">Il y a peut-être des problèmes de connectivité réseau.</span><span class="sxs-lookup"><span data-stu-id="988fd-164">There may be network connectivity issues.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="988fd-165">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="988fd-165">See Also</span></span>


[<span data-ttu-id="988fd-166">New-CsUserServicesPolicy</span><span class="sxs-lookup"><span data-stu-id="988fd-166">New-CsUserServicesPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsUserServicesPolicy)  
[<span data-ttu-id="988fd-167">Set-CsUserServicesPolicy</span><span class="sxs-lookup"><span data-stu-id="988fd-167">Set-CsUserServicesPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsUserServicesPolicy)  
  

<span data-ttu-id="988fd-168"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="988fd-168"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

