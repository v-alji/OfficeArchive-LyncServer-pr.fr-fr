---
title: 'Lync Server 2013 : test de l’authentification du client Lync'
description: 'Lync Server 2013 : test de l’authentification du client Lync.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing Lync Client authentication
ms:assetid: e22114cb-4456-4e5f-93ab-51592c4a8209
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn689120(v=OCS.15)
ms:contentKeyID: 63969659
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 03694b7fd56d7847d8d493304b97af335d2a5b4d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394488"
---
# <a name="testing-lync-client-authentication-in-lync-server-2013"></a><span data-ttu-id="1951c-103">Test de l’authentification du client Lync dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1951c-103">Testing Lync Client authentication in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1951c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1951c-104">

<span> </span></span></span>

<span data-ttu-id="1951c-105">_**Dernière modification de la rubrique :** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="1951c-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1951c-106">Échéancier de vérification</span><span class="sxs-lookup"><span data-stu-id="1951c-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="1951c-107">Jour</span><span class="sxs-lookup"><span data-stu-id="1951c-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1951c-108">Outil de test</span><span class="sxs-lookup"><span data-stu-id="1951c-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="1951c-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="1951c-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1951c-110">Autorisations requises</span><span class="sxs-lookup"><span data-stu-id="1951c-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="1951c-111">Lorsque l’application est exécutée localement à l’aide de Lync Server Management Shell, les utilisateurs doivent être membres du groupe de sécurité RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="1951c-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="1951c-112">Lors de l’exécution à l’aide d’une instance distante de Windows PowerShell, un rôle RBAC doit être attribué aux utilisateurs qui ont l’autorisation d’exécuter l’applet de commande Test-CsClientAuth.</span><span class="sxs-lookup"><span data-stu-id="1951c-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsClientAuth cmdlet.</span></span> <span data-ttu-id="1951c-113">Pour afficher la liste de tous les rôles RBAC qui peuvent utiliser cette applet de commande, exécutez la commande suivante à partir de l’invite Windows PowerShell :</span><span class="sxs-lookup"><span data-stu-id="1951c-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsClientAuth&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="1951c-114">Description</span><span class="sxs-lookup"><span data-stu-id="1951c-114">Description</span></span>

<span data-ttu-id="1951c-115">L’applet de connexion Test-CsClientAuth permet de déterminer si un utilisateur peut se connecter au serveur Lync à l’aide d’un certificat client, vous pouvez exécuter l’applet de Test-CsClientAuth.</span><span class="sxs-lookup"><span data-stu-id="1951c-115">The Test-CsClientAuth cmdlet enables you to determine whether a user can log on to the Lync Server by using a client certificate, you can run the Test-CsClientAuth cmdlet.</span></span> <span data-ttu-id="1951c-116">Après avoir appelé test-CsClientAuth, l’applet de commande contacte le service de mise en service des certificats et télécharge une copie des certificats clients pour l’utilisateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="1951c-116">After calling Test-CsClientAuth, the cmdlet will contact the certificate provisioning service and download a copy of any client certificates for the specified user.</span></span> <span data-ttu-id="1951c-117">S’il est possible de trouver et de télécharger un certificat client, Test-CsClientAuth tentera alors de se connecter à l’aide de celui-ci.</span><span class="sxs-lookup"><span data-stu-id="1951c-117">If a client certificate can be found and downloaded, Test-CsClientAuth will then attempt to log on by using that certificate.</span></span> <span data-ttu-id="1951c-118">En cas de réussite de l’ouverture de session, Test-CsClientAuth se déconnecte et signale que le test a réussi.</span><span class="sxs-lookup"><span data-stu-id="1951c-118">If logon succeeds, Test-CsClientAuth will log off and report that the test succeeded.</span></span> <span data-ttu-id="1951c-119">Si un certificat est introuvable ou n’a pas pu être téléchargé, ou si l’applet de connexion n’est pas en mesure de se connecter à l’aide de ce certificat, Test-CsClientAuth signalera que le test a échoué.</span><span class="sxs-lookup"><span data-stu-id="1951c-119">If a certificate cannot be found or downloaded, or if the cmdlet is unable to logon using that certificate, then Test-CsClientAuth will report that the test failed.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="1951c-120">Exécution du test</span><span class="sxs-lookup"><span data-stu-id="1951c-120">Running the test</span></span>

<span data-ttu-id="1951c-121">L’applet de contrôle Test-CsClientAuth est exécutée en utilisant le compte d’un utilisateur qui est activé pour Lync Server.</span><span class="sxs-lookup"><span data-stu-id="1951c-121">The Test-CsClientAuth cmdlet is run by using the account of any user who is enabled for Lync Server.</span></span> <span data-ttu-id="1951c-122">Pour effectuer cette vérification à l’aide d’un compte d’utilisateur réel, vous devez d’abord créer un objet d’informations d’identification Windows PowerShell contenant le nom et le mot de passe du compte.</span><span class="sxs-lookup"><span data-stu-id="1951c-122">To run this check using an actual user account, you must first create a Windows PowerShell credentials object that contains the account name and password.</span></span> <span data-ttu-id="1951c-123">Lorsque le système appelle test-CsClientAuth, vous devez inclure l’objet Credential et l’adresse SIP associée au compte.</span><span class="sxs-lookup"><span data-stu-id="1951c-123">You must then include that credentials object and the SIP address assigned to the account when the system calls Test-CsClientAuth:</span></span>

    $credential = Get-Credential "litwareinc\kenmyer"
    Test-CsClientAuth -TargetFqdn "atl-cs-001.litwareinc.com"-UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential

<span data-ttu-id="1951c-124">Pour plus d’informations, consultez la documentation d’aide de l’applet de [contrôle test-CsClientAuth](https://technet.microsoft.com/library/gg398712\(v=ocs.14\).aspx) .</span><span class="sxs-lookup"><span data-stu-id="1951c-124">For more information, see the Help documentation for the [Test-CsClientAuth](https://technet.microsoft.com/library/gg398712\(v=ocs.14\).aspx) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="1951c-125">Détermination du succès ou de l’échec</span><span class="sxs-lookup"><span data-stu-id="1951c-125">Determining success or failure</span></span>

<span data-ttu-id="1951c-126">Si l’utilisateur spécifié peut se connecter à Lync Server à l’aide d’un certificat client, vous recevrez une sortie semblable à ce qui suit, avec la propriété Result marquée comme **réussie :**</span><span class="sxs-lookup"><span data-stu-id="1951c-126">If the specified user can log on to Lync Server by using a client certificate, you will receive output similar to this, with the Result property marked as **Success:**</span></span>

<span data-ttu-id="1951c-127">TargetFqdn : atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="1951c-127">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="1951c-128">Résultat : réussite</span><span class="sxs-lookup"><span data-stu-id="1951c-128">Result : Success</span></span>

<span data-ttu-id="1951c-129">Latence : 00:00:06.8630376</span><span class="sxs-lookup"><span data-stu-id="1951c-129">Latency : 00:00:06.8630376</span></span>

<span data-ttu-id="1951c-130">Error</span><span class="sxs-lookup"><span data-stu-id="1951c-130">Error :</span></span>

<span data-ttu-id="1951c-131">Diagnostic</span><span class="sxs-lookup"><span data-stu-id="1951c-131">Diagnosis :</span></span>

<span data-ttu-id="1951c-132">Si l’utilisateur spécifié ne peut pas se connecter, le résultat s’affichera en tant qu’échec et des informations supplémentaires seront enregistrées dans les propriétés d’erreur et de diagnostic :</span><span class="sxs-lookup"><span data-stu-id="1951c-132">If the specified user can not log on, the Result will be shown as Failure and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="1951c-133">TargetFqdn : atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="1951c-133">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="1951c-134">Résultat : échec</span><span class="sxs-lookup"><span data-stu-id="1951c-134">Result : Failure</span></span>

<span data-ttu-id="1951c-135">Latence : 00:00:03.3645259</span><span class="sxs-lookup"><span data-stu-id="1951c-135">Latency : 00:00:03.3645259</span></span>

<span data-ttu-id="1951c-136">Erreur : nous n’avons pas pu télécharger un certificat CS pour l’utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="1951c-136">Error : Could not download a CS Certificate for the given user.</span></span> <span data-ttu-id="1951c-137">Vérifier si</span><span class="sxs-lookup"><span data-stu-id="1951c-137">Check if</span></span>

<span data-ttu-id="1951c-138">les informations d’identification et URI fournies sont correctes.</span><span class="sxs-lookup"><span data-stu-id="1951c-138">provided uri and credentials are correct.</span></span>

<span data-ttu-id="1951c-139">Diagnostic</span><span class="sxs-lookup"><span data-stu-id="1951c-139">Diagnosis :</span></span>

<span data-ttu-id="1951c-140">Par exemple, la sortie précédente indique que le test a échoué car un certificat client valide a pu être localisé pour l’utilisateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="1951c-140">For example, the previous output states that the test failed because a valid client certificate couldn't be located for the specified user.</span></span> <span data-ttu-id="1951c-141">Vous pouvez renvoyer une liste des certificats clients émis à un utilisateur en exécutant une commande comme suit :</span><span class="sxs-lookup"><span data-stu-id="1951c-141">You can return a list of the client certificates issued to a user by running a command as follows:</span></span>

    Get-CsClientCertificate -Identity "sip:kenmyer@litwareinc.com"

<span data-ttu-id="1951c-142">Si Test-CsClientAuth échoue, il est possible que vous souhaitiez réexécuter le test, cette fois-ci, y compris le paramètre Verbose :</span><span class="sxs-lookup"><span data-stu-id="1951c-142">If Test-CsClientAuth fails, then you might want to rerun the test, this time including the Verbose parameter:</span></span>

    $credential = Get-Credential "litwareinc\kenmyer"
    Test-CsClientAuth -TargetFqdn "atl-cs-001.litwareinc.com"-UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential -Verbose

<span data-ttu-id="1951c-143">Lorsque le paramètre Verbose est inclus, Test-CsClientAuth renvoie un compte étape par étape de chaque action qu’il a effectuée lors de la vérification de la capacité de l’utilisateur spécifié à se connecter à Lync Server.</span><span class="sxs-lookup"><span data-stu-id="1951c-143">When the Verbose parameter is included, Test-CsClientAuth will return a step-by-step account of each action it tried when it checked the ability of the specified user to log on to Lync Server.</span></span> <span data-ttu-id="1951c-144">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="1951c-144">For example:</span></span>

<span data-ttu-id="1951c-145">Tentative de téléchargement d’un certificat CS pour l’utilisateur : kenmyer@litwareinc.com Endpoint : STEpid</span><span class="sxs-lookup"><span data-stu-id="1951c-145">Trying to download a CS certificate for User : kenmyer@litwareinc.com endpoint : STEpid</span></span>

<span data-ttu-id="1951c-146">URL du service Web : https://atl-cs-001.litwareinc.com:443/CertProv/CertprovisioningService.svc</span><span class="sxs-lookup"><span data-stu-id="1951c-146">Web Service url : https://atl-cs-001.litwareinc.com:443/CertProv/CertprovisioningService.svc</span></span>

<span data-ttu-id="1951c-147">Impossible de télécharger un certificat CS à partir du service Web.</span><span class="sxs-lookup"><span data-stu-id="1951c-147">Could not download a CS certificate from web service.</span></span>

<span data-ttu-id="1951c-148">Recherchez</span><span class="sxs-lookup"><span data-stu-id="1951c-148">CHECK:</span></span>

<span data-ttu-id="1951c-149">\- L’URL du service Web est valide et les services Web sont opérationnels</span><span class="sxs-lookup"><span data-stu-id="1951c-149">\- Web service url is valid and the web services are functional</span></span>

<span data-ttu-id="1951c-150">\-Si vous utilisez PhoneNo \\ \\ code confidentiel pour l’authentification, vérifiez qu’il correspond à l’URI de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1951c-150">\- If using PhoneNo\\\\Pin to authenticate, make sure they match the user uri</span></span>

<span data-ttu-id="1951c-151">\- Si vous utilisez l’authentification Kerberos NTLM, assurez- \\ vous d’avoir fourni les informations d’identification valides.</span><span class="sxs-lookup"><span data-stu-id="1951c-151">\- If using NTLM\\Kerberos auth, make sure you provided valid credentials</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="1951c-152">Raisons pour lesquelles le test peut avoir échoué</span><span class="sxs-lookup"><span data-stu-id="1951c-152">Reasons why the test might have failed</span></span>

<span data-ttu-id="1951c-153">Voici quelques raisons courantes pour lesquelles Test-CsClientAuth risque d’échouer :</span><span class="sxs-lookup"><span data-stu-id="1951c-153">Here are some common reasons why Test-CsClientAuth might fail:</span></span>

  - <span data-ttu-id="1951c-154">Vous avez spécifié un compte d’utilisateur qui n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="1951c-154">You specified a user account that was not valid.</span></span> <span data-ttu-id="1951c-155">Vous pouvez vérifier qu’un compte d’utilisateur existe en exécutant une commande semblable à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="1951c-155">You can verify that a user account exists by running a command similar to this:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com"

  - <span data-ttu-id="1951c-156">Le compte d’utilisateur est valide, mais le compte n’est pas activé pour Lync Server.</span><span class="sxs-lookup"><span data-stu-id="1951c-156">The user account is valid, but the account is currently not enabled for Lync Server.</span></span> <span data-ttu-id="1951c-157">Pour vérifier qu’un compte d’utilisateur est activé pour Lync Server, exécutez une commande semblable à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="1951c-157">To verify that a user account is enabled for Lync Server, run a command similar to the following:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object Enabled
    
    <span data-ttu-id="1951c-158">Si la propriété Enabled est définie sur false, cela signifie que l’utilisateur n’est actuellement pas activé pour Lync Server.</span><span class="sxs-lookup"><span data-stu-id="1951c-158">If the Enabled property is set to False, that means that the user is currently not enabled for Lync Server.</span></span>

  - <span data-ttu-id="1951c-159">Il est possible que l’utilisateur test ne dispose pas d’un certificat client valide.</span><span class="sxs-lookup"><span data-stu-id="1951c-159">The test user might not have a valid client certificate.</span></span> <span data-ttu-id="1951c-160">Vous pouvez renvoyer des informations sur les certificats clients attribués à un utilisateur à l’aide d’une commande semblable à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="1951c-160">You can return information about the client certificates assigned to a user by using a command similar to this:</span></span>
    
        Get-CsClientCertificate -Identity "sip:kenmyer@litwareinc.com"

<span data-ttu-id="1951c-161"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1951c-161"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

