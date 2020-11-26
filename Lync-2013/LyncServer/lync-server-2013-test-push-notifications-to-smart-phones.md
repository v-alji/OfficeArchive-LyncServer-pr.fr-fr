---
title: 'Lync Server 2013 : tester les notifications de transmission vers des téléphones intelligents'
description: 'Lync Server 2013 : tester les notifications de transmission vers des téléphones intelligents.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test push notifications to smart phones
ms:assetid: 8f5ca7d1-1ccb-4cb0-b417-730559e79b6e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn767948(v=OCS.15)
ms:contentKeyID: 63969626
ms.date: 03/15/2017
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4b92ef444a5331c9a673fd2db506631554e96eea
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441227"
---
# <a name="test-push-notifications-to-smart-phones-in-lync-server-2013"></a><span data-ttu-id="700f8-103">Tester des notifications de transmission vers des téléphones intelligents dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="700f8-103">Test push notifications to smart phones in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="700f8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="700f8-104">

<span> </span></span></span>

<span data-ttu-id="700f8-105">_**Dernière modification de la rubrique :** 2017-03-15_</span><span class="sxs-lookup"><span data-stu-id="700f8-105">_**Topic Last Modified:** 2017-03-15_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="700f8-106">Échéancier de vérification</span><span class="sxs-lookup"><span data-stu-id="700f8-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="700f8-107">Mois</span><span class="sxs-lookup"><span data-stu-id="700f8-107">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="700f8-108">Outil de test</span><span class="sxs-lookup"><span data-stu-id="700f8-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="700f8-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="700f8-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="700f8-110">Autorisations requises</span><span class="sxs-lookup"><span data-stu-id="700f8-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="700f8-111">Lorsque l’application est exécutée localement à l’aide de Lync Server Management Shell, les utilisateurs doivent être membres du groupe de sécurité RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="700f8-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="700f8-112">Lors de l’exécution à l’aide d’une instance distante de Windows PowerShell, un rôle RBAC doit être attribué aux utilisateurs qui ont l’autorisation d’exécuter l’applet de commande Test-CsMcxPushNotification.</span><span class="sxs-lookup"><span data-stu-id="700f8-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsMcxPushNotification cmdlet.</span></span> <span data-ttu-id="700f8-113">Pour afficher la liste de tous les rôles RBAC qui peuvent utiliser cette applet de commande, exécutez la commande suivante à partir de l’invite Windows PowerShell :</span><span class="sxs-lookup"><span data-stu-id="700f8-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsMcxPushNotification&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="700f8-114">Description</span><span class="sxs-lookup"><span data-stu-id="700f8-114">Description</span></span>

<span data-ttu-id="700f8-115">Le service de notifications d’émission (service de notification d’appel et service de notification d’appel Microsoft) peut envoyer des notifications relatives à des événements tels que les nouveaux messages instantanés et les nouveaux messages vocaux sur des appareils mobiles tels que les iPhone et les téléphones Windows, même si le client Lync sur ces appareils est actuellement suspendu ou en cours d’exécution en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="700f8-115">The push notification service (Apple Push Notification Service and Microsoft Push Notification Service) can send notifications about events such as new instant messages or new voice mail to mobile devices such as iPhones and Windows Phones, even if the Lync client on those devices is currently suspended or running in the background.</span></span> <span data-ttu-id="700f8-116">Le service de notifications d’émission est un service basé sur le Cloud qui s’exécute sur les serveurs Microsoft.</span><span class="sxs-lookup"><span data-stu-id="700f8-116">The push notification service is a cloud-based service that is running on Microsoft servers.</span></span> <span data-ttu-id="700f8-117">Pour tirer parti des notifications de transmission, vous devez être en mesure de vous connecter au centre de notifications de transmission Clearinghouse et de vous y authentifier.</span><span class="sxs-lookup"><span data-stu-id="700f8-117">In order to take advantage of push notifications, you must be able to connect to, and be authenticated by, the push notification clearinghouse.</span></span> <span data-ttu-id="700f8-118">L’applet de contrôle Test-CsMcxPushNotification permet aux administrateurs de vérifier que les demandes de notifications de transmission peuvent être routées via votre serveur Edge vers le centre de notifications de type Clearinghouse.</span><span class="sxs-lookup"><span data-stu-id="700f8-118">The Test-CsMcxPushNotification cmdlet enables administrators to verify that push notification requests can be routed through your Edge server to the push notification clearinghouse.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="700f8-119">Exécution du test</span><span class="sxs-lookup"><span data-stu-id="700f8-119">Running the test</span></span>

<span data-ttu-id="700f8-120">Pour tester le service de notifications d’émission, appelez l’applet de contrôle Test-CsMcxPushNotification.</span><span class="sxs-lookup"><span data-stu-id="700f8-120">To test the push notification service, call the Test-CsMcxPushNotification cmdlet.</span></span> <span data-ttu-id="700f8-121">Vérifiez que vous spécifiez le nom de domaine complet de votre serveur Edge :</span><span class="sxs-lookup"><span data-stu-id="700f8-121">Make sure that you specify the fully qualified domain name of your Edge server:</span></span>

    Test-CsMcxPushNotification -AccessEdgeFqdn "atl-edge-001.litwareinc.com"

<span data-ttu-id="700f8-122">Pour plus d’informations, consultez la rubrique d’aide de l’applet de [contrôle test-CsMcxPushNotification](https://docs.microsoft.com/powershell/module/skype/Test-CsMcxPushNotification) .</span><span class="sxs-lookup"><span data-stu-id="700f8-122">For more information, see the help topic for the [Test-CsMcxPushNotification](https://docs.microsoft.com/powershell/module/skype/Test-CsMcxPushNotification) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="700f8-123">Détermination du succès ou de l’échec</span><span class="sxs-lookup"><span data-stu-id="700f8-123">Determining success or failure</span></span>

<span data-ttu-id="700f8-124">Si Test-CsMcxPushNotification réussit, l’applet de contrôle renverra le résultat de test réussite :</span><span class="sxs-lookup"><span data-stu-id="700f8-124">If Test-CsMcxPushNotification succeeds the cmdlet will return the test result Success:</span></span>

<span data-ttu-id="700f8-125">TargetFqdn : atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="700f8-125">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="700f8-126">Résultat : réussite</span><span class="sxs-lookup"><span data-stu-id="700f8-126">Result : Success</span></span>

<span data-ttu-id="700f8-127">Latence : 00:00:00</span><span class="sxs-lookup"><span data-stu-id="700f8-127">Latency : 00:00:00</span></span>

<span data-ttu-id="700f8-128">Error</span><span class="sxs-lookup"><span data-stu-id="700f8-128">Error :</span></span>

<span data-ttu-id="700f8-129">Diagnostic</span><span class="sxs-lookup"><span data-stu-id="700f8-129">Diagnosis :</span></span>

<span data-ttu-id="700f8-130">Si Test-CsMcxPushNotification n’est pas en mesure de se connecter au centre de notifications de type Clearinghouse, l’applet de connexion ne renverra généralement aucun résultat de test d’échec</span><span class="sxs-lookup"><span data-stu-id="700f8-130">If Test-CsMcxPushNotification is unable to connect to the push notification clearinghouse the cmdlet will typically not return a test result of Failure.</span></span> <span data-ttu-id="700f8-131">En règle générale, la commande échoue entièrement.</span><span class="sxs-lookup"><span data-stu-id="700f8-131">Instead the command will usually fail completely.</span></span> <span data-ttu-id="700f8-132">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="700f8-132">For example:</span></span>

<span data-ttu-id="700f8-133">Test-CsMcxPushNotification : une réponse de 504 (délai du serveur) a été reçue du réseau et l’opération a échoué.</span><span class="sxs-lookup"><span data-stu-id="700f8-133">Test-CsMcxPushNotification : A 504 (Server time-out) response was received from the network and the operation failed.</span></span> <span data-ttu-id="700f8-134">Pour plus d’informations, consultez les détails de l’exception.</span><span class="sxs-lookup"><span data-stu-id="700f8-134">See the exception details for more information.</span></span>

<span data-ttu-id="700f8-135">À la ligne : 1 car : 27</span><span class="sxs-lookup"><span data-stu-id="700f8-135">At line:1 char:27</span></span>

<span data-ttu-id="700f8-136">\+Test-CsMcxPushNotification \< \< \< \< -AccessEdgeFqdn lyncedge.mydomain.com</span><span class="sxs-lookup"><span data-stu-id="700f8-136">\+ Test-CsMcxPushNotification \<\<\<\< -AccessEdgeFqdn lyncedge.mydomain.com</span></span>

<span data-ttu-id="700f8-137">\+ CategoryInfo : OperationStopped : ( :) \[ Test-CsMcxPushNotification \] , FailureResponseException</span><span class="sxs-lookup"><span data-stu-id="700f8-137">\+ CategoryInfo : OperationStopped: (:) \[Test-CsMcxPushNotification\], FailureResponseException</span></span>

<span data-ttu-id="700f8-138">\+ FullyQualifiedErrorId : WorkflowNotCompleted, Microsoft. RTC. Management. SyntheticTransactions. TestMcxPushNotificationCmdlet</span><span class="sxs-lookup"><span data-stu-id="700f8-138">\+ FullyQualifiedErrorId : WorkflowNotCompleted,Microsoft.Rtc.Management.SyntheticTransactions.TestMcxPushNotificationCmdlet</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="700f8-139">Raisons pour lesquelles le test peut avoir échoué</span><span class="sxs-lookup"><span data-stu-id="700f8-139">Reasons why the test might have failed</span></span>

<span data-ttu-id="700f8-140">Si le service de notifications de transmission ne fonctionne pas, ce qui signifie généralement que vous rencontrez des problèmes de communication avec votre serveur Edge ou que vous rencontrez des problèmes pour communiquer avec le centre de suppression</span><span class="sxs-lookup"><span data-stu-id="700f8-140">If the push notification service fails that usually indicates either problems communicating with your Edge server, or problems communicating with the Push Notification Clearing House.</span></span> <span data-ttu-id="700f8-141">Si vous rencontrez des problèmes lorsque vous exécutez test-CsMcxPushNotification, la première chose à faire est de vérifier que votre serveur Edge fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="700f8-141">If you encounter problems when you run Test-CsMcxPushNotification, the first thing that you should do is verify that your Edge server is working correctly.</span></span> <span data-ttu-id="700f8-142">Pour ce faire, vous pouvez utiliser l’applet de Test-CsAVEdgeConnectivity cmdlet :</span><span class="sxs-lookup"><span data-stu-id="700f8-142">One way to do that is to use the Test-CsAVEdgeConnectivity cmdlet:</span></span>

    $credential = Get-Credential "litwareinc\kenmyer"
    
    Test-CsAVEdgeConnectivity -TargetFqdn "atl-cs-001.litwareinc.com" -UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential

<span data-ttu-id="700f8-143">Ce contrôle vérifie qu’un utilisateur spécifié peut se connecter au serveur Edge.</span><span class="sxs-lookup"><span data-stu-id="700f8-143">This check verifies that a specified user can connect to the Edge server.</span></span>

<span data-ttu-id="700f8-144">Si le serveur Edge semble fonctionner correctement, il se peut que vous ne puissiez pas vous connecter au centre de notifications de transmission Clearinghouse.</span><span class="sxs-lookup"><span data-stu-id="700f8-144">If the Edge server seems to be working correctly, that often means that you are unable to connect to the push notification clearinghouse.</span></span> <span data-ttu-id="700f8-145">En règle générale, cela signifie généralement que vous n’avez pas configuré l’URI de Clearinghouse correctement ou que vous n’avez pas d’enregistrement SRV DNS qui pointe vers cette URL.</span><span class="sxs-lookup"><span data-stu-id="700f8-145">In turn, that typically means that you either have not configured the clearinghouse URI correctly or that you do not have a DNS SRV record that points to this URL.</span></span> <span data-ttu-id="700f8-146">Vous pouvez vérifier que l’URI est défini sur la valeur correcte (sip :push@push.lync.com) en exécutant la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="700f8-146">You can verify that the URI is set to the correct value (sip:push@push.lync.com) by running this command:</span></span>

    Get-CsMcxConfiguration

<span data-ttu-id="700f8-147">Si la propriété PushNotificationProxyUri est définie sur une valeur autre que sip :push@push.lync.com, vous pouvez corriger ce problème à l’aide de l’applet de action Set-McxConfiguration.</span><span class="sxs-lookup"><span data-stu-id="700f8-147">If the PushNotificationProxyUri property is set to anything other than sip:push@push.lync.com then you can correct that problem by using the Set-McxConfiguration cmdlet.</span></span> <span data-ttu-id="700f8-148">Par exemple, cette commande définit correctement l’URI au sein de votre organisation :</span><span class="sxs-lookup"><span data-stu-id="700f8-148">For example, this command correctly sets the URI throughout your organization:</span></span>

    Get-CsMcxConfiguration | Set-CsMcxConfiguration -PushNotificationProxyUri "sip:push@push.lync.com"

<span data-ttu-id="700f8-149">Pour plus d’informations, consultez la rubrique d’aide relative à l’applet de passe [Set-CsMcxConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsMcxConfiguration) .</span><span class="sxs-lookup"><span data-stu-id="700f8-149">For more information, see the help topic for the [Set-CsMcxConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsMcxConfiguration) cmdlet.</span></span>

<span data-ttu-id="700f8-150">Si l’URI est configuré correctement, l’étape suivante consiste à vérifier que vous disposez d’un enregistrement DNS SRV qui est résolu vers votre domaine SIP et votre serveur Edge.</span><span class="sxs-lookup"><span data-stu-id="700f8-150">If the URI is configured correctly, your next step should be to verify that you have a DNS SRV record that resolves to your SIP domain and your Edge server.</span></span> <span data-ttu-id="700f8-151">Pour plus d’informations sur la configuration de ces enregistrements, voir la rubrique d’aide configuration requise pour la mobilité.</span><span class="sxs-lookup"><span data-stu-id="700f8-151">For more information about how to configure these records, see the help topic DNS Requirements for Mobility.</span></span> <span data-ttu-id="700f8-152">Notez que le message d’erreur suivant indique généralement un problème avec les enregistrements DNS :</span><span class="sxs-lookup"><span data-stu-id="700f8-152">Note that the following error message usually indicates a problem with DNS records:</span></span>

<span data-ttu-id="700f8-153">Une réponse de 504 (délai d’expiration du serveur) a été reçue du réseau et l’opération a échoué.</span><span class="sxs-lookup"><span data-stu-id="700f8-153">A 504 (Server time-out) response was received from the network and the operation failed.</span></span> <span data-ttu-id="700f8-154">Pour plus d’informations, consultez les détails de l’exception.</span><span class="sxs-lookup"><span data-stu-id="700f8-154">See the exception details for more information.</span></span>

<span data-ttu-id="700f8-155">Il est également possible que Test-CsMcxConfiguration ne fonctionne pas avec ce message d’erreur :</span><span class="sxs-lookup"><span data-stu-id="700f8-155">It’s also possible that Test-CsMcxConfiguration will fail with this error message:</span></span>

<span data-ttu-id="700f8-156">Test-CsMcxPushNotification : la demande de notifications de type pousser a été refusée.</span><span class="sxs-lookup"><span data-stu-id="700f8-156">Test-CsMcxPushNotification : Push Notification request was rejected.</span></span>

<span data-ttu-id="700f8-157">À la ligne : 1 car : 27</span><span class="sxs-lookup"><span data-stu-id="700f8-157">At line:1 char:27</span></span>

<span data-ttu-id="700f8-158">\+ Test-CsMcxPushNotification \<\<\<\<</span><span class="sxs-lookup"><span data-stu-id="700f8-158">\+ Test-CsMcxPushNotification \<\<\<\<</span></span>

<span data-ttu-id="700f8-159">\+ CategoryInfo : OperationStopped : ( :) \[ Test-CsMcxPushNotification \] , SyntheticTransactionException</span><span class="sxs-lookup"><span data-stu-id="700f8-159">\+ CategoryInfo : OperationStopped: (:) \[Test-CsMcxPushNotification\], SyntheticTransactionException</span></span>

<span data-ttu-id="700f8-160">\+ FullyQualifiedErrorId : WorkflowNotCompleted, Microsoft. RTC. Management. SyntheticTransactions. TestMcxPushNotificationCmdlet</span><span class="sxs-lookup"><span data-stu-id="700f8-160">\+ FullyQualifiedErrorId : WorkflowNotCompleted,Microsoft.Rtc.Management.SyntheticTransactions.TestMcxPushNotificationCmdlet</span></span>

<span data-ttu-id="700f8-161">Le message « la demande de notifications de transmission a été refusée » s’affiche généralement si vous avez activé le filtrage d’URL et que vous bloquez les préfixes http : et https :.</span><span class="sxs-lookup"><span data-stu-id="700f8-161">The “Push notification request was rejected” message typically occurs if you have enabled URL filtering and are blocking the http: and https: prefixes.</span></span> <span data-ttu-id="700f8-162">Vous pouvez déterminer les préfixes bloqués à l’aide d’une commande semblable à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="700f8-162">You can determine which prefixes are being blocked by using a command similar to the following:</span></span>

```PowerShell 
 (Get-CsImFilterConfiguration -Identity Global).Prefixes
```

<span data-ttu-id="700f8-163">Si http : ou https : apparaissent dans les résultats, vous devez les supprimer de la liste des préfixes bloqués pour que les notifications de transmission fonctionnent.</span><span class="sxs-lookup"><span data-stu-id="700f8-163">If http: or https: appear in the results, you must remove them from the blocked prefix list for push notifications to work.</span></span> <span data-ttu-id="700f8-164">Pour cela, vous pouvez utiliser des commandes similaires à celles-ci :</span><span class="sxs-lookup"><span data-stu-id="700f8-164">That can be done by using commands similar to these:</span></span>

    Set-CsImFilterConfiguration -Identity site:Redmond -Prefixes @{remove="http:"}
    Set-CsImFilterConfiguration -Identity site:Redmond -Prefixes @{remove="https:"}

<span data-ttu-id="700f8-165">Pour plus d’informations, consultez la rubrique d’aide relative à l’applet de passe [Set-CsImFilterConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsImFilterConfiguration).</span><span class="sxs-lookup"><span data-stu-id="700f8-165">For more information, see the help topic for the [Set-CsImFilterConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsImFilterConfiguration)cmdlet.</span></span>

<span data-ttu-id="700f8-166"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="700f8-166"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

