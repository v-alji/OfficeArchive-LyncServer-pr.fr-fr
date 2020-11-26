---
title: 'Lync Server 2013 : tester l’accès d’une application Web anonyme'
description: 'Lync Server 2013 : Testez l’accès anonyme à l’application Web.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test anonymous Web App access
ms:assetid: 92f691cd-e05e-4bab-beb5-251d4b837a19
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn767949(v=OCS.15)
ms:contentKeyID: 63969630
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 11c33840912fefcaeef069e14773cfefd0834a8b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441269"
---
# <a name="test-anonymous-web-app-access-in-lync-server-2013"></a><span data-ttu-id="b0bdd-103">Tester l’accès d’une application Web anonyme dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b0bdd-103">Test anonymous Web App access in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b0bdd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b0bdd-104">

<span> </span></span></span>

<span data-ttu-id="b0bdd-105">_**Dernière modification de la rubrique :** 2014-06-07_</span><span class="sxs-lookup"><span data-stu-id="b0bdd-105">_**Topic Last Modified:** 2014-06-07_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b0bdd-106">Échéancier de vérification</span><span class="sxs-lookup"><span data-stu-id="b0bdd-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="b0bdd-107">Mois</span><span class="sxs-lookup"><span data-stu-id="b0bdd-107">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0bdd-108">Outil de test</span><span class="sxs-lookup"><span data-stu-id="b0bdd-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="b0bdd-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="b0bdd-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0bdd-110">Autorisations requises</span><span class="sxs-lookup"><span data-stu-id="b0bdd-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="b0bdd-111">Lorsque l’application est exécutée localement à l’aide de Lync Server Management Shell, les utilisateurs doivent être membres du groupe de sécurité RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="b0bdd-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="b0bdd-112">Lors de l’exécution à l’aide d’une instance distante de Windows PowerShell, un rôle RBAC doit être attribué aux utilisateurs qui ont l’autorisation d’exécuter l’applet de commande Test-CsWebAppAnonymous.</span><span class="sxs-lookup"><span data-stu-id="b0bdd-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsWebAppAnonymous cmdlet.</span></span> <span data-ttu-id="b0bdd-113">Pour afficher la liste de tous les rôles RBAC qui peuvent utiliser cette applet de commande, exécutez la commande suivante à partir de l’invite Windows PowerShell :</span><span class="sxs-lookup"><span data-stu-id="b0bdd-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsWebAppAnonymous&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="b0bdd-114">Description</span><span class="sxs-lookup"><span data-stu-id="b0bdd-114">Description</span></span>

<span data-ttu-id="b0bdd-115">L’applet de connexion Test-CsWebAppAnonymous vérifie qu’un utilisateur anonyme peut participer à des conférences Lync Server à l’aide de Lync Web App.</span><span class="sxs-lookup"><span data-stu-id="b0bdd-115">The Test-CsWebAppAnonymous cmdlet verifies that an anonymous user can join Lync Server conferences by using the Lync Web App.</span></span> <span data-ttu-id="b0bdd-116">Lorsque vous exécutez l’applet de connexion, Test-CsWebAppAnonymous contacte le service de ticket Web pour obtenir un ticket Web pour l’utilisateur anonyme.</span><span class="sxs-lookup"><span data-stu-id="b0bdd-116">When you run the cmdlet, Test-CsWebAppAnonymous contacts the Web Ticket service to obtain a web ticket for the anonymous user.</span></span> <span data-ttu-id="b0bdd-117">Si l’applet de demande réussit à obtenir ce ticket, Test-CsWebAppAnonymous contacte ensuite Lync Server et tente d’établir des conférences distinctes pour la messagerie instantanée, le partage d’application et la collaboration sur les données.</span><span class="sxs-lookup"><span data-stu-id="b0bdd-117">If the cmdlet succeeds in obtaining this ticket, Test-CsWebAppAnonymous will then contact Lync Server and attempt to establish separate conferences for instant messaging, application sharing, and data collaboration.</span></span>

<span data-ttu-id="b0bdd-118">Notez que Test-CsWebAppAnonymous vérifie uniquement les API et les connexions utilisées pour créer ces conférences.</span><span class="sxs-lookup"><span data-stu-id="b0bdd-118">Note that Test-CsWebAppAnonymous only verifies the APIs and connections used to create these conferences.</span></span> <span data-ttu-id="b0bdd-119">Le cmdlet ne crée et ne fait pas de conférences.</span><span class="sxs-lookup"><span data-stu-id="b0bdd-119">The cmdlet does not actually create and conduct any conferences.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="b0bdd-120">Exécution du test</span><span class="sxs-lookup"><span data-stu-id="b0bdd-120">Running the test</span></span>

<span data-ttu-id="b0bdd-121">Vous pouvez exécuter l’applet de applet de Test-CsWebAppAnonymous à l’aide d’une paire de comptes de test préconfigurés ou des comptes de deux utilisateurs qui sont activés pour Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b0bdd-121">The Test-CsWebAppAnonymous cmdlet can be run using either a pair of preconfigured test accounts or the accounts of any two users who are enabled for Lync Server.</span></span> <span data-ttu-id="b0bdd-122">Pour exécuter cette vérification à l’aide de comptes de test, vous devez simplement spécifier le nom de domaine complet du pool de serveurs Lync testé.</span><span class="sxs-lookup"><span data-stu-id="b0bdd-122">To run this check using test accounts, you just have to specify the fully qualified domain name of the Lync Server pool being tested.</span></span> <span data-ttu-id="b0bdd-123">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="b0bdd-123">For example:</span></span>

    Test-CsWebAppAnonymous -TargetFqdn atl-cs-001.litwareinc.com

<span data-ttu-id="b0bdd-124">Pour exécuter cette vérification à l’aide de comptes d’utilisateurs réels, vous devez créer deux objets d’informations d’identification Lync Server Management Shell (objets contenant le nom de compte et le mot de passe) pour chaque compte.</span><span class="sxs-lookup"><span data-stu-id="b0bdd-124">To run this check using actual user accounts, you must create two Lync Server Management Shell credentials objects (objects that contain the account name and password) for each account.</span></span> <span data-ttu-id="b0bdd-125">Vous devez alors inclure ces objets d’informations d’identification et les adresses SIP des deux comptes lors de l’appel de test-CsWebAppAnonymous :</span><span class="sxs-lookup"><span data-stu-id="b0bdd-125">You must then include those credentials objects and the SIP addresses of the two accounts when you call Test-CsWebAppAnonymous:</span></span>

    $cred1 = Get-Credential "litwareinc\kenmyer"
    
    Test-CsWebApp -TargetFqdn atl-cs-001.litwareinc.com -UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $cred1

<span data-ttu-id="b0bdd-126">Pour plus d’informations, consultez la rubrique d’aide de l’applet de Test-CsWebAppAnonymous.</span><span class="sxs-lookup"><span data-stu-id="b0bdd-126">For more information, see the help topic for the Test-CsWebAppAnonymous cmdlet.</span></span> <span data-ttu-id="b0bdd-127">Notez que Test-CsWebAppAnonymous est déconseillé pour une utilisation sur Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b0bdd-127">Note that Test-CsWebAppAnonymous is deprecated for use on Lync Server 2013.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="b0bdd-128">Détermination du succès ou de l’échec</span><span class="sxs-lookup"><span data-stu-id="b0bdd-128">Determining success or failure</span></span>

<span data-ttu-id="b0bdd-129">Si Test-CsWebAppAnonymous pouvez rejoindre l’utilisateur anonyme dans ses conférences, l’applet de contrôle renverra le résultat du test réussite :</span><span class="sxs-lookup"><span data-stu-id="b0bdd-129">If Test-CsWebAppAnonymous can join the anonymous user to his or her conferences, the cmdlet will return the test result Success:</span></span>

<span data-ttu-id="b0bdd-130">Nom de domaine complet cible :</span><span class="sxs-lookup"><span data-stu-id="b0bdd-130">Target Fqdn :</span></span>

<span data-ttu-id="b0bdd-131">Résultat : réussite</span><span class="sxs-lookup"><span data-stu-id="b0bdd-131">Result : Success</span></span>

<span data-ttu-id="b0bdd-132">Latence : 00:00:00</span><span class="sxs-lookup"><span data-stu-id="b0bdd-132">Latency : 00:00:00</span></span>

<span data-ttu-id="b0bdd-133">Message d’erreur :</span><span class="sxs-lookup"><span data-stu-id="b0bdd-133">Error Message :</span></span>

<span data-ttu-id="b0bdd-134">Diagnostic</span><span class="sxs-lookup"><span data-stu-id="b0bdd-134">Diagnosis :</span></span>

<span data-ttu-id="b0bdd-135">Si l’utilisateur anonyme ne peut pas participer aux conférences nécessaires, le résultat du test sera marqué comme ayant échoué.</span><span class="sxs-lookup"><span data-stu-id="b0bdd-135">If the anonymous user can't join the necessary conferences then the test result will be marked as Failure.</span></span> <span data-ttu-id="b0bdd-136">En règle générale, Test-CsWebAppAnonymous signale également un message d’erreur et un diagnostic détaillés :</span><span class="sxs-lookup"><span data-stu-id="b0bdd-136">Typically Test-CsWebAppAnonymous will also report back a detailed error message and diagnosis:</span></span>

<span data-ttu-id="b0bdd-137">Nom de domaine complet (FQDN) cible : atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="b0bdd-137">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="b0bdd-138">Résultat : échec</span><span class="sxs-lookup"><span data-stu-id="b0bdd-138">Result : Failure</span></span>

<span data-ttu-id="b0bdd-139">Latence : 00:00:05.9746266</span><span class="sxs-lookup"><span data-stu-id="b0bdd-139">Latency : 00:00:05.9746266</span></span>

<span data-ttu-id="b0bdd-140">Message d’erreur : aucune réponse n’est reçue pour le service Web-Ticket</span><span class="sxs-lookup"><span data-stu-id="b0bdd-140">Error Message : No response received for Web-Ticket service</span></span>

<span data-ttu-id="b0bdd-141">Diagnostic : la requête HTTP n’est pas autorisée avec le client</span><span class="sxs-lookup"><span data-stu-id="b0bdd-141">Diagnosis : The HTTP request is unauthorized with client</span></span>

<span data-ttu-id="b0bdd-142">schéma d’authentification « NTLM ».</span><span class="sxs-lookup"><span data-stu-id="b0bdd-142">authentication scheme 'Ntlm'.</span></span> <span data-ttu-id="b0bdd-143">L’authentification</span><span class="sxs-lookup"><span data-stu-id="b0bdd-143">The authentication</span></span>

<span data-ttu-id="b0bdd-144">l’en-tête reçu du serveur était « Negotiate, NTLM ».</span><span class="sxs-lookup"><span data-stu-id="b0bdd-144">header received from the server was 'Negotiate,NTLM'.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="b0bdd-145">Raisons pour lesquelles le test peut avoir échoué</span><span class="sxs-lookup"><span data-stu-id="b0bdd-145">Reasons why the test might have failed</span></span>

<span data-ttu-id="b0bdd-146">Test-CsWebAppAnonymous les échecs se produisent généralement autour des erreurs d’authentification de l’utilisateur : vous devez exécuter le test à l’aide d’un compte d’utilisateur valide, même si l’applet de contrôle vérifie la capacité d’un utilisateur anonyme à se connecter à Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b0bdd-146">Test-CsWebAppAnonymous failures usually revolve around user authentication errors: you must run the test using a valid user account even though the cmdlet is checking the ability of an anonymous user to connect to Lync Server.</span></span> <span data-ttu-id="b0bdd-147">Si Test-CsWebAppAnonymous échoue, vous devez vérifier que l’utilisateur spécifié a valide un compte d’utilisateur de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b0bdd-147">If Test-CsWebAppAnonymous fails, you should verify that the specified user has valid a Lync Server user account.</span></span> <span data-ttu-id="b0bdd-148">Vous pouvez récupérer les informations de compte de Lync Server en utilisant une commande similaire à celle-ci :</span><span class="sxs-lookup"><span data-stu-id="b0bdd-148">You can retrieve Lync Server account information by using a command similar to this:</span></span>

    Get-CsUser -Identity "sip:kenmyer@litwareinc.com" | Select-Object Enabled

<span data-ttu-id="b0bdd-149">Si la propriété Enabled n’est pas égale à true ou en cas d’échec de la commande, cela signifie que l’utilisateur ne possède pas de compte Lync Server valide.</span><span class="sxs-lookup"><span data-stu-id="b0bdd-149">If the Enabled property is not equal to True or if the command fails, that means that the user does not have a valid Lync Server account.</span></span>

<span data-ttu-id="b0bdd-150">Vous devez également vérifier que le mot de passe que vous avez fourni lorsque vous exécutez l’applet de contrôle est un mot de passe valide.</span><span class="sxs-lookup"><span data-stu-id="b0bdd-150">You should also verify that the password that you supplied when you run the cmdlet is a valid password.</span></span>

<span data-ttu-id="b0bdd-151">Des problèmes de configuration liés à Office Web Apps Server peuvent également entraîner l’échec de Test-CsWebAppAnonymous. C’est souvent le cas si vous recevez le code de diagnostic suivant :</span><span class="sxs-lookup"><span data-stu-id="b0bdd-151">Configuration problems with Office Web Apps Server can also cause Test-CsWebAppAnonymous to fail; that will often be the case if you receive the following diagnosis:</span></span>

<span data-ttu-id="b0bdd-152">La requête HTTP n’est pas autorisée avec le schéma d’authentification du client « NTLM ».</span><span class="sxs-lookup"><span data-stu-id="b0bdd-152">The HTTP request is unauthorized with client authentication scheme 'Ntlm'.</span></span> <span data-ttu-id="b0bdd-153">L’en-tête d’authentification reçu du serveur était « Negotiate, NTLM ».</span><span class="sxs-lookup"><span data-stu-id="b0bdd-153">The authentication header received from the server was 'Negotiate,NTLM'.</span></span>

<span data-ttu-id="b0bdd-154">Pour plus d’informations sur le diagnostic et la résolution des problèmes liés au serveur Office Web Apps, voir le billet de blog [Office Web Apps server 2013-les ordinateurs sont toujours signalés comme défectueux](http://www.wictorwilen.se/office-web-apps-server-2013---machines-are-always-reported-as-unhealthy).</span><span class="sxs-lookup"><span data-stu-id="b0bdd-154">For more information on diagnosing and resolving Office Web Apps Server problems see the blog post [Office Web Apps Server 2013 - machines are always reported as Unhealthy](http://www.wictorwilen.se/office-web-apps-server-2013---machines-are-always-reported-as-unhealthy).</span></span>

<span data-ttu-id="b0bdd-155"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b0bdd-155"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

