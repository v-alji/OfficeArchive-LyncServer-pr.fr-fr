---
title: 'Lync Server 2013 : tester l’accès des utilisateurs mobiles'
description: 'Lync Server 2013 : tester l’accès des utilisateurs mobiles.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test mobile user access
ms:assetid: 81d97420-428b-41b7-91ef-185d572d3456
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn767947(v=OCS.15)
ms:contentKeyID: 63969624
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e99a05e6ef9fe925126026452823e5edcc100ede
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441241"
---
# <a name="test-mobile-user-access-in-lync-server-2013"></a><span data-ttu-id="7b1bc-103">Test de l’accès des utilisateurs mobiles dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7b1bc-103">Test mobile user access in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7b1bc-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7b1bc-104">

<span> </span></span></span>

<span data-ttu-id="7b1bc-105">_**Dernière modification de la rubrique :** 2014-06-07_</span><span class="sxs-lookup"><span data-stu-id="7b1bc-105">_**Topic Last Modified:** 2014-06-07_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7b1bc-106">Échéancier de vérification</span><span class="sxs-lookup"><span data-stu-id="7b1bc-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="7b1bc-107">Mois</span><span class="sxs-lookup"><span data-stu-id="7b1bc-107">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7b1bc-108">Outil de test</span><span class="sxs-lookup"><span data-stu-id="7b1bc-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="7b1bc-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="7b1bc-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7b1bc-110">Autorisations requises</span><span class="sxs-lookup"><span data-stu-id="7b1bc-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="7b1bc-111">Lorsque l’application est exécutée localement à l’aide de Lync Server Management Shell, les utilisateurs doivent être membres du groupe de sécurité RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="7b1bc-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="7b1bc-112">Lors de l’exécution à l’aide d’une instance distante de Windows PowerShell, un rôle RBAC doit être attribué aux utilisateurs qui ont l’autorisation d’exécuter l’applet de commande Test-CsMcxConference.</span><span class="sxs-lookup"><span data-stu-id="7b1bc-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsMcxConference cmdlet.</span></span> <span data-ttu-id="7b1bc-113">Pour afficher la liste de tous les rôles RBAC qui peuvent utiliser cette applet de commande, exécutez la commande suivante à partir de l’invite Windows PowerShell :</span><span class="sxs-lookup"><span data-stu-id="7b1bc-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsMcxConference&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="7b1bc-114">Description</span><span class="sxs-lookup"><span data-stu-id="7b1bc-114">Description</span></span>

<span data-ttu-id="7b1bc-115">Le service de mobilité permet aux utilisateurs de périphériques mobiles d’effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="7b1bc-115">The Mobility Service enables mobile device users to do such things as:</span></span>

1.  <span data-ttu-id="7b1bc-116">Échangez des messages instantanés et des informations de présence.</span><span class="sxs-lookup"><span data-stu-id="7b1bc-116">Exchange instant messages and presence information.</span></span>

2.  <span data-ttu-id="7b1bc-117">Stockez et récupérez les messages vocaux en interne plutôt qu’avec leur opérateur sans fil.</span><span class="sxs-lookup"><span data-stu-id="7b1bc-117">Store and retrieve voice mail internally instead of with their wireless provider.</span></span>

3.  <span data-ttu-id="7b1bc-118">Tirez parti des fonctionnalités du serveur Lync, telles que les appels par le biais de tâches et de conférences rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="7b1bc-118">Take advantage of Lync Server capabilities such as Call via Work and dial-out conferencing.</span></span> <span data-ttu-id="7b1bc-119">L’applet de contrôle Test-CsMcxConference fournit un moyen rapide et facile de vérifier que les utilisateurs peuvent participer à des conférences Lync Server en utilisant un appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="7b1bc-119">The Test-CsMcxConference cmdlet provides a quick and easy way to verify that users can join and participate in Lync Server conferences by using a mobile device.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="7b1bc-120">Exécution du test</span><span class="sxs-lookup"><span data-stu-id="7b1bc-120">Running the test</span></span>

<span data-ttu-id="7b1bc-121">Pour exécuter cette vérification, vous devez créer trois objets d’informations d’identification Windows PowerShell (objets contenant le nom et le mot de passe du compte) pour chaque compte.</span><span class="sxs-lookup"><span data-stu-id="7b1bc-121">To run this check, you must create three Windows PowerShell credentials objects (objects that contain the account name and password) for each account.</span></span> <span data-ttu-id="7b1bc-122">Vous devez alors inclure ces objets d’informations d’identification et les adresses SIP des deux comptes lorsque vous appelez Test-CsMcxConference comme le montre l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="7b1bc-122">You must then include those credentials objects and the SIP addresses of the two accounts when you call Test-CsMcxConference as shown in the following example:</span></span>

    $organizerCred = Get-Credential "litwareinc\kenmyer"
    $user1Cred = Get-Credential "litwareinc\packerman"
    $user2Cred = Get-Credential "litwareinc\adelaney"
    
    Test-CsMcxConference -TargetFqdn "atl-cs-001.litwareinc.com" -Authentication Negotiate -OrganizerSipAddress "sip:kenmyer@litwareinc.com" -OrganizerCredential $organizerCred -UserSipAddress "sip:pilar@litwareinc.com" -UserCredential $user1Cred -User2SipAddress "sip:adelaney@litwareinc.com" -User2Credential $user2Cred

<span data-ttu-id="7b1bc-123">Pour plus d’informations, consultez la rubrique d’aide de l’applet de [contrôle test-CsMcxConference](https://docs.microsoft.com/powershell/module/skype/Test-CsMcxConference) .</span><span class="sxs-lookup"><span data-stu-id="7b1bc-123">For more information, see the help topic for the [Test-CsMcxConference](https://docs.microsoft.com/powershell/module/skype/Test-CsMcxConference) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="7b1bc-124">Détermination du succès ou de l’échec</span><span class="sxs-lookup"><span data-stu-id="7b1bc-124">Determining success or failure</span></span>

<span data-ttu-id="7b1bc-125">Si la vérification aboutit, Test-CsMcxConference signalera le résultat du test réussite :</span><span class="sxs-lookup"><span data-stu-id="7b1bc-125">If the check succeeds, Test-CsMcxConference will report a test result of Success:</span></span>

<span data-ttu-id="7b1bc-126">Nom de domaine complet (FQDN) cible : atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="7b1bc-126">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="7b1bc-127">URI de destination : http://atl-cs-001.litwareinc.com:443/mcx</span><span class="sxs-lookup"><span data-stu-id="7b1bc-127">Target Uri : http://atl-cs-001.litwareinc.com:443/mcx</span></span>

<span data-ttu-id="7b1bc-128">Résultat : réussite</span><span class="sxs-lookup"><span data-stu-id="7b1bc-128">Result : Success</span></span>

<span data-ttu-id="7b1bc-129">Latence : 00:00:00</span><span class="sxs-lookup"><span data-stu-id="7b1bc-129">Latency : 00:00:00</span></span>

<span data-ttu-id="7b1bc-130">Message d’erreur :</span><span class="sxs-lookup"><span data-stu-id="7b1bc-130">Error Message :</span></span>

<span data-ttu-id="7b1bc-131">Diagnostic</span><span class="sxs-lookup"><span data-stu-id="7b1bc-131">Diagnosis :</span></span>

<span data-ttu-id="7b1bc-132">Si la vérification échoue Test-CsMcxConference signale un résultat de test de l’échec.</span><span class="sxs-lookup"><span data-stu-id="7b1bc-132">If the check is unsuccessful Test-CsMcxConference will report a test result of Failure.</span></span> <span data-ttu-id="7b1bc-133">Ce résultat de test est généralement accompagné d’un message d’erreur détaillé et d’un diagnostic.</span><span class="sxs-lookup"><span data-stu-id="7b1bc-133">This test result will typically be accompanied by a detailed error message and diagnosis.</span></span> <span data-ttu-id="7b1bc-134">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="7b1bc-134">For example:</span></span>

<span data-ttu-id="7b1bc-135">Nom de domaine complet (FQDN) cible : atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="7b1bc-135">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="7b1bc-136">URI de destination : https://atl-cs-001.litwareinc.com:443/mcx</span><span class="sxs-lookup"><span data-stu-id="7b1bc-136">Target Uri : https://atl-cs-001.litwareinc.com:443/mcx</span></span>

<span data-ttu-id="7b1bc-137">Résultat : échec</span><span class="sxs-lookup"><span data-stu-id="7b1bc-137">Result : Failure</span></span>

<span data-ttu-id="7b1bc-138">Latence : 00:00:00</span><span class="sxs-lookup"><span data-stu-id="7b1bc-138">Latency : 00:00:00</span></span>

<span data-ttu-id="7b1bc-139">Message d’erreur : aucune réponse n’est reçue pour le service Web-Ticket.</span><span class="sxs-lookup"><span data-stu-id="7b1bc-139">Error Message : No response received for Web-Ticket service.</span></span>

<span data-ttu-id="7b1bc-140">Exception interne : la requête HHTP n’est pas autorisée avec le client</span><span class="sxs-lookup"><span data-stu-id="7b1bc-140">Inner Exception:The HHTP request is unauthorized with client</span></span>

<span data-ttu-id="7b1bc-141">schéma de négociation « NTLM ».</span><span class="sxs-lookup"><span data-stu-id="7b1bc-141">negotiation scheme 'Ntlm'.</span></span> <span data-ttu-id="7b1bc-142">En-tête d’authentification reçu</span><span class="sxs-lookup"><span data-stu-id="7b1bc-142">The authentication header received</span></span>

<span data-ttu-id="7b1bc-143">à partir du serveur était « Negotiate ».</span><span class="sxs-lookup"><span data-stu-id="7b1bc-143">from the server was 'Negotiate'.</span></span>

<span data-ttu-id="7b1bc-144">Exception interne : le serveur distant a renvoyé une erreur : (401)</span><span class="sxs-lookup"><span data-stu-id="7b1bc-144">Inner Exception:The remote server returned an error: (401)</span></span>

<span data-ttu-id="7b1bc-145">Non autorisé.</span><span class="sxs-lookup"><span data-stu-id="7b1bc-145">Unauthorized.</span></span>

<span data-ttu-id="7b1bc-146">Diagnostic</span><span class="sxs-lookup"><span data-stu-id="7b1bc-146">Diagnosis :</span></span>

<span data-ttu-id="7b1bc-147">Diagnostic interne : X-MS-Server-Fqdb : atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="7b1bc-147">Inner Diagnosis:X-MS-server-Fqdb : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="7b1bc-148">Cache-Control : privée</span><span class="sxs-lookup"><span data-stu-id="7b1bc-148">Cache-Control : private</span></span>

<span data-ttu-id="7b1bc-149">Type de contenu : texte/html ; charset = UTF-8.</span><span class="sxs-lookup"><span data-stu-id="7b1bc-149">Content-Type : text/html; charset=utf-8.</span></span>

<span data-ttu-id="7b1bc-150">Serveur : Microsoft-IIS/8.5</span><span class="sxs-lookup"><span data-stu-id="7b1bc-150">Server : Microsoft-IIS/8.5</span></span>

<span data-ttu-id="7b1bc-151">WWW-Authenticate : Negotiate, NTLM</span><span class="sxs-lookup"><span data-stu-id="7b1bc-151">WWW-Authenticate : Negotiate,NTLM</span></span>

<span data-ttu-id="7b1bc-152">X-par : ASP.NET</span><span class="sxs-lookup"><span data-stu-id="7b1bc-152">X-Powered-By : ASP.NET</span></span>

<span data-ttu-id="7b1bc-153">X-type de contenu-options : nosniff</span><span class="sxs-lookup"><span data-stu-id="7b1bc-153">X-Content-Type-Options : nosniff</span></span>

<span data-ttu-id="7b1bc-154">Date : Wed, 28 2014 19:22:19 GMT</span><span class="sxs-lookup"><span data-stu-id="7b1bc-154">Date : Wed, 28 May 2014 19:22:19 GMT</span></span>

<span data-ttu-id="7b1bc-155">Longueur du contenu : 6305</span><span class="sxs-lookup"><span data-stu-id="7b1bc-155">Content-Length : 6305</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="7b1bc-156">Raisons pour lesquelles le test peut avoir échoué</span><span class="sxs-lookup"><span data-stu-id="7b1bc-156">Reasons why the test might have failed</span></span>

<span data-ttu-id="7b1bc-157">Si Test-CsMcxConference échoue, vous devez commencer par vérifier que le service de mobilité est en cours d’exécution et qu’il est accessible.</span><span class="sxs-lookup"><span data-stu-id="7b1bc-157">If Test-CsMcxConference fails you should begin by verifying that the mobility service is running and can be accessed.</span></span> <span data-ttu-id="7b1bc-158">Vous pouvez effectuer cette opération à l’aide d’un navigateur Web pour vérifier qu’il est possible d’accéder à l’URL du service de mobilité pour votre pool Lync Server.</span><span class="sxs-lookup"><span data-stu-id="7b1bc-158">That can be done by using a web browser to verify that the mobility service URL for your Lync Server pool can be accessed.</span></span> <span data-ttu-id="7b1bc-159">Par exemple, la commande suivante vérifie l’URL du pool atl-cs-001.litwareinc.com :</span><span class="sxs-lookup"><span data-stu-id="7b1bc-159">For example, this command verifies the URL for the pool atl-cs-001.litwareinc.com:</span></span>

`https://atl-cs-001.litwareinc.com/mcx/mcxservice.svc`

<span data-ttu-id="7b1bc-160">S’il est possible d’accéder au service de mobilité, il est conseillé de vérifier que vos utilisateurs test disposent de comptes Lync Server valides.</span><span class="sxs-lookup"><span data-stu-id="7b1bc-160">If the mobility service can be accessed you should then verify that your test users have valid Lync Server accounts.</span></span> <span data-ttu-id="7b1bc-161">Vous pouvez récupérer les informations sur le compte à l’aide d’une commande similaire à celle-ci :</span><span class="sxs-lookup"><span data-stu-id="7b1bc-161">You can retrieve account information by using a command similar to this:</span></span>

    Get-CsUser -Identity "sip:kenmyer@litwareinc.com" | Select-Object Enabled

<span data-ttu-id="7b1bc-162">Si la propriété Enabled n’est pas égale à true ou en cas d’échec de la commande, cela signifie que l’utilisateur ne possède pas de compte Lync Server valide. Vérifiez également que chaque compte d’utilisateur est activé pour la mobilité.</span><span class="sxs-lookup"><span data-stu-id="7b1bc-162">If the Enabled property is not equal to True or if the command fails, that means that the user does not have a valid Lync Server account.You should also verify that each user account is enabled for mobility.</span></span> <span data-ttu-id="7b1bc-163">Pour ce faire, vous devez d’abord déterminer la stratégie de mobilité affectée au compte :</span><span class="sxs-lookup"><span data-stu-id="7b1bc-163">To do that, first determine the mobility policy that is assigned to the account:</span></span>

    Get-CsUser -Identity "sip:kenmyer@litwareinc.com" | Select-Object MobilityPolicy

<span data-ttu-id="7b1bc-164">Lorsque vous connaissez le nom de la stratégie, utilisez l’applet de contrôle Get-CsMobilityPolicy pour vérifier que la stratégie en question (par exemple, RedmondMobilityPolicy) a la propriété EnableMobility définie sur true :</span><span class="sxs-lookup"><span data-stu-id="7b1bc-164">After you know the policy name, use the Get-CsMobilityPolicy cmdlet to verify that the policy in question (for example, RedmondMobilityPolicy) has the EnableMobility property set to True:</span></span>

    Get-CsMobilityPolicy -Identity "RedmondMobilityPolicy"

<span data-ttu-id="7b1bc-165">Si vous recevez un message d’erreur « en-tête d’authentification » lorsque vous exécutez Test-CsMcxConference cela signifie que vous n’avez pas spécifié de compte d’utilisateur valide, vérifiez le nom d’utilisateur et le mot de passe, puis relancez le test.</span><span class="sxs-lookup"><span data-stu-id="7b1bc-165">If you receive an “authentication header” error message when you run Test-CsMcxConference that often means that you have not specified a valid user account, Verify the user name and password and then try the test again.</span></span> <span data-ttu-id="7b1bc-166">Si vous êtes convaincu que le compte d’utilisateur est valide, utilisez l’applet de contrôle Get-CsWebServiceConfiguration et vérifiez la valeur de la propriété UseWindowsAuth.</span><span class="sxs-lookup"><span data-stu-id="7b1bc-166">If you are convinced that the user account is valid, then use the Get-CsWebServiceConfiguration cmdlet and check the value of the UseWindowsAuth property.</span></span> <span data-ttu-id="7b1bc-167">Cela vous indique les méthodes d’authentification activées au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="7b1bc-167">That will tell you which authentication methods are enabled in your organization.</span></span>

<span data-ttu-id="7b1bc-168">Pour obtenir des conseils supplémentaires sur la résolution des problèmes liés au service de mobilité, voir le billet de blog [résolution des problèmes de connectivité externes Lync Mobility](https://blogs.technet.com/b/nexthop/archive/2012/02/21/troubleshooting-external-lync-mobility-connectivity-issues-step-by-step.aspx).</span><span class="sxs-lookup"><span data-stu-id="7b1bc-168">For more tips about how to troubleshoot the mobility service, see the blog post [Troubleshooting External Lync Mobility Connectivity Issues Step-by-Step](https://blogs.technet.com/b/nexthop/archive/2012/02/21/troubleshooting-external-lync-mobility-connectivity-issues-step-by-step.aspx).</span></span>

<span data-ttu-id="7b1bc-169"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7b1bc-169"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

