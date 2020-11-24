---
title: 'Lync Server 2013 : test de connexion à Lync Phone Edition'
description: 'Lync Server 2013 : test de la connexion de Lync Phone Edition.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing Lync Phone Edition login
ms:assetid: 1ccde6bf-9a2d-4fcf-b81f-1bc9fee2cfbb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn690128(v=OCS.15)
ms:contentKeyID: 63969583
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d21d65676c4f5e0f867c7d9556cdea50419be69b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394485"
---
# <a name="testing-lync-phone-edition-login-in-lync-server-2013"></a><span data-ttu-id="51f3f-103">Test de la connexion Lync Phone Edition dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="51f3f-103">Testing Lync Phone Edition login in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="51f3f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="51f3f-104">

<span> </span></span></span>

<span data-ttu-id="51f3f-105">_**Dernière modification de la rubrique :** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="51f3f-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="51f3f-106">Échéancier de vérification</span><span class="sxs-lookup"><span data-stu-id="51f3f-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="51f3f-107">Jour</span><span class="sxs-lookup"><span data-stu-id="51f3f-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51f3f-108">Outil de test</span><span class="sxs-lookup"><span data-stu-id="51f3f-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="51f3f-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="51f3f-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51f3f-110">Autorisations requises</span><span class="sxs-lookup"><span data-stu-id="51f3f-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="51f3f-111">Lorsque l’application est exécutée localement à l’aide de Lync Server Management Shell, les utilisateurs doivent être membres du groupe de sécurité RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="51f3f-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="51f3f-112">Lors de l’exécution à l’aide d’une instance distante de Windows PowerShell, un rôle RBAC doit être attribué aux utilisateurs qui ont l’autorisation d’exécuter l’applet de commande Test-CsPhoneBootstrap.</span><span class="sxs-lookup"><span data-stu-id="51f3f-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsPhoneBootstrap cmdlet.</span></span> <span data-ttu-id="51f3f-113">Pour afficher la liste de tous les rôles RBAC qui peuvent utiliser cette applet de commande, exécutez la commande suivante à partir de l’invite Windows PowerShell :</span><span class="sxs-lookup"><span data-stu-id="51f3f-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsPhoneBootstrap&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="51f3f-114">Description</span><span class="sxs-lookup"><span data-stu-id="51f3f-114">Description</span></span>

<span data-ttu-id="51f3f-115">L’applet de connexion Test-CsPhoneBootstrap permet aux administrateurs de vérifier qu’un utilisateur donné (en utilisant le numéro de téléphone et le code confidentiel qui lui est affecté) peut se connecter au système à partir d’un appareil compatible Lync 2013 Phone Edition.</span><span class="sxs-lookup"><span data-stu-id="51f3f-115">The Test-CsPhoneBootstrap cmdlet enables administrators to verify that a given user—using the phone number and PIN assigned to him or her—can log on to the system from a Lync 2013 Phone Edition-compatible device.</span></span> <span data-ttu-id="51f3f-116">(Aucun appareil n’est réellement requis pour exécuter le test.)</span><span class="sxs-lookup"><span data-stu-id="51f3f-116">(No device is actually needed to run the test.)</span></span>

<span data-ttu-id="51f3f-117">Pour que Test-CsPhoneBootstrap le contrôle, le pool d’inscriptions qui héberge le compte d’utilisateur testé doit être détectable par le biais du protocole DHCP.</span><span class="sxs-lookup"><span data-stu-id="51f3f-117">In order for Test-CsPhoneBootstrap to make its check, the Registrar pool that hosts the user account being tested must be discoverable using DHCP.</span></span> <span data-ttu-id="51f3f-118">Pour déterminer si un bureau d’enregistrement est détectable de cette manière, utilisez l’applet de contrôle Get-CsRegistrarConfiguration et vérifiez la valeur de la propriété EnableDHCPServer.</span><span class="sxs-lookup"><span data-stu-id="51f3f-118">To determine whether a Registrar is discoverable in this manner, use the cmdlet Get-CsRegistrarConfiguration and check the value of the EnableDHCPServer property.</span></span> <span data-ttu-id="51f3f-119">Si cette propriété est définie sur false, vous devez utiliser Set-CsRegistrarConfiguration pour définir la valeur de la propriété sur true et rendre le Bureau d’enregistrement détectable via le protocole DHCP.</span><span class="sxs-lookup"><span data-stu-id="51f3f-119">If this property is set to False, you must use Set-CsRegistrarConfiguration to set the property value to True and make the Registrar discoverable using DHCP.</span></span> <span data-ttu-id="51f3f-120">Vous pouvez également effectuer cette opération à l’aide du serveur DHCP d’entreprise et de la configuration des options spécifiques de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="51f3f-120">This can also be done by using Enterprise DHCP Server and configuring the Lync Server-specific options.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="51f3f-121">Exécution du test</span><span class="sxs-lookup"><span data-stu-id="51f3f-121">Running the test</span></span>

<span data-ttu-id="51f3f-122">Pour exécuter l’applet de applet de Test-CsPhoneBootstrap, vous devez au moins indiquer le numéro de téléphone et le code confidentiel (PIN) du client pour un utilisateur de serveur Lync valide.</span><span class="sxs-lookup"><span data-stu-id="51f3f-122">To run the Test-CsPhoneBootstrap cmdlet, you must, at a minimum, supply the phone number and client personal identification number (PIN) for a valid Lync Server user.</span></span> <span data-ttu-id="51f3f-123">Par exemple, cette commande teste la capacité de connexion de l’utilisateur disposant du numéro de téléphone 12065551219 et du code confidentiel 0712 :</span><span class="sxs-lookup"><span data-stu-id="51f3f-123">For example, this command tests the logon ability for the user who has the phone number 12065551219 and the PIN 0712:</span></span>

    Test-CsPhoneBootstrap -PhoneOrExt "+12065551219" -Pin "0712"

<span data-ttu-id="51f3f-124">Pour une vérification plus complète, vous pouvez également inclure l’adresse SIP de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="51f3f-124">For a more comprehensive check, you can also include the user’s SIP address.</span></span> <span data-ttu-id="51f3f-125">Dans ce cas, le numéro de téléphone, le code confidentiel du client et l’adresse SIP doivent être valides pour que le test réussisse :</span><span class="sxs-lookup"><span data-stu-id="51f3f-125">In that case, the phone number, client PIN, and SIP address must all be valid for the test to succeed:</span></span>

    Test-CsPhoneBootstrap -PhoneOrExt "+12065551219" -Pin "0712" -UserSipAddress "sip:kenmyer@litwareinc.com"

<span data-ttu-id="51f3f-126">Pour plus d’informations, consultez la documentation d’aide de l’applet de [contrôle test-CsPhoneBootstrap](https://docs.microsoft.com/powershell/module/skype/Test-CsPhoneBootstrap) .</span><span class="sxs-lookup"><span data-stu-id="51f3f-126">For more information, see the Help documentation for the [Test-CsPhoneBootstrap](https://docs.microsoft.com/powershell/module/skype/Test-CsPhoneBootstrap) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="51f3f-127">Détermination du succès ou de l’échec</span><span class="sxs-lookup"><span data-stu-id="51f3f-127">Determining success or failure</span></span>

<span data-ttu-id="51f3f-128">Si l’utilisateur spécifié a réussi à se connecter à Lync Server, vous recevrez une sortie similaire à celle-ci, avec la propriété Result marquée comme **réussie :**</span><span class="sxs-lookup"><span data-stu-id="51f3f-128">If the specified user was able to connect to Lync Server, you'll receive output similar to this, with the Result property marked as **Success:**</span></span>

<span data-ttu-id="51f3f-129">TargetUri https://atl-cs-001.litwareinc.com:443/CertProv/</span><span class="sxs-lookup"><span data-stu-id="51f3f-129">TargetUri : https://atl-cs-001.litwareinc.com:443/CertProv/</span></span>

<span data-ttu-id="51f3f-130">CertProvisioningService. svc</span><span class="sxs-lookup"><span data-stu-id="51f3f-130">CertProvisioningService.svc</span></span>

<span data-ttu-id="51f3f-131">TargetFqdn : atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="51f3f-131">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="51f3f-132">Résultat : réussite</span><span class="sxs-lookup"><span data-stu-id="51f3f-132">Result : Success</span></span>

<span data-ttu-id="51f3f-133">Latence : 00:00:06.3981276</span><span class="sxs-lookup"><span data-stu-id="51f3f-133">Latency : 00:00:06.3981276</span></span>

<span data-ttu-id="51f3f-134">Error</span><span class="sxs-lookup"><span data-stu-id="51f3f-134">Error :</span></span>

<span data-ttu-id="51f3f-135">Diagnostic</span><span class="sxs-lookup"><span data-stu-id="51f3f-135">Diagnosis :</span></span>

<span data-ttu-id="51f3f-136">Si l’utilisateur spécifié n’a pas réussi à établir une connexion, le résultat s’affichera en panne et des informations supplémentaires seront enregistrées dans les propriétés d’erreur et de diagnostic :</span><span class="sxs-lookup"><span data-stu-id="51f3f-136">If the specified user was not able to make a connection, then the Result will be shown as Failure, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="51f3f-137">TargetFqdn : atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="51f3f-137">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="51f3f-138">Résultat : échec</span><span class="sxs-lookup"><span data-stu-id="51f3f-138">Result : Failure</span></span>

<span data-ttu-id="51f3f-139">Latence : 00:00:04.1993845</span><span class="sxs-lookup"><span data-stu-id="51f3f-139">Latency : 00:00:04.1993845</span></span>

<span data-ttu-id="51f3f-140">Erreur : erreur-absence de réponse pour le service Web-Ticket.</span><span class="sxs-lookup"><span data-stu-id="51f3f-140">Error : ERROR - No response received for Web-Ticket service.</span></span>

<span data-ttu-id="51f3f-141">Diagnostic</span><span class="sxs-lookup"><span data-stu-id="51f3f-141">Diagnosis :</span></span>

<span data-ttu-id="51f3f-142">La sortie précédente indique que le test a échoué, car le service de ticket Web ne répond pas.</span><span class="sxs-lookup"><span data-stu-id="51f3f-142">The previous output states that the test failed because the Web Ticket service did not respond.</span></span> <span data-ttu-id="51f3f-143">Cela peut être dû à un problème avec le service proprement dit, ou à l’adresse du SIP, au numéro de téléphone ou au code confidentiel client transmis à test-CsPhoneBootstrap.</span><span class="sxs-lookup"><span data-stu-id="51f3f-143">This could be due to a problem with the service itself, or it might be due to the SIP address, phone number, or client PIN passed to Test-CsPhoneBootstrap.</span></span> <span data-ttu-id="51f3f-144">Vous pouvez vérifier l’adresse SIP et le numéro de téléphone de l’utilisateur à l’aide d’une commande similaire à celle-ci :</span><span class="sxs-lookup"><span data-stu-id="51f3f-144">You can verify the user’s SIP address and phone number by using a command similar to this one:</span></span>

    Get-CsUser -Identity "sip:kenmyer@litwareinc.com" | Select-Object SipAddress, LineUri

<span data-ttu-id="51f3f-145">Vous pouvez aussi vérifier que l’utilisateur dispose d’un code confidentiel valide à l’aide d’une commande comme suit :</span><span class="sxs-lookup"><span data-stu-id="51f3f-145">And you can verify that the user has a valid PIN by using a command as follows:</span></span>

    Get-CsClientPinInfo -Identity "sip:kenmyer@litwareinc.com" 

<span data-ttu-id="51f3f-146">Si Test-CsPhoneBootstrap échoue, il est possible que vous souhaitiez réexécuter le test, cette fois-ci, y compris le paramètre Verbose :</span><span class="sxs-lookup"><span data-stu-id="51f3f-146">If Test-CsPhoneBootstrap fails, then you might want to rerun the test, this time including the Verbose parameter:</span></span>

    Test-CsPhoneBootstrap -PhoneOrExt "+12065551219" -Pin "0712" -Verbose

<span data-ttu-id="51f3f-147">Lorsque le paramètre Verbose est inclus, Test-CsPhoneBootstrap renvoie un compte étape par étape de chaque action qu’il a effectuée lors de la vérification de la capacité de l’utilisateur spécifié à se connecter à Lync Server.</span><span class="sxs-lookup"><span data-stu-id="51f3f-147">When the Verbose parameter is included, Test-CsPhoneBootstrap will return a step-by-step account of each action it tried when it checked the ability of the specified user to log on to Lync Server.</span></span> <span data-ttu-id="51f3f-148">Par exemple, voici une partie de la sortie d’un échec d’ouverture de session, une session dans laquelle un code confidentiel incorrect a été inclus :</span><span class="sxs-lookup"><span data-stu-id="51f3f-148">For example, here is a portion of the output for an unsuccessful logon, a session in which an incorrect PIN was included:</span></span>

<span data-ttu-id="51f3f-149">Utilisation de PIN auth avec le numéro de téléphone \\ : 12065551219 code confidentiel : 0712</span><span class="sxs-lookup"><span data-stu-id="51f3f-149">Using PIN auth with Phone\\Ext : 12065551219 Pin : 0712</span></span>

<span data-ttu-id="51f3f-150">Impossible d’obtenir le ticket Web</span><span class="sxs-lookup"><span data-stu-id="51f3f-150">Could not get web ticket</span></span>

<span data-ttu-id="51f3f-151">Recherchez</span><span class="sxs-lookup"><span data-stu-id="51f3f-151">CHECK :</span></span>

<span data-ttu-id="51f3f-152">\- L’URL du service Web est valide et les services Web sont opérationnels</span><span class="sxs-lookup"><span data-stu-id="51f3f-152">\- Web service url is valid and the web services are functional</span></span>

<span data-ttu-id="51f3f-153">\- Si vous utilisez PhoneNo \\ code confidentiel pour l’authentification, vérifiez qu’il correspond à l’URI de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="51f3f-153">\- If using PhoneNo\\PIN to authenticate, make sure they match the user uri</span></span>

<span data-ttu-id="51f3f-154">\- Si vous utilisez l’authentification Kerberos NTLM, assurez- \\ vous d’avoir fourni les informations d’identification valides.</span><span class="sxs-lookup"><span data-stu-id="51f3f-154">\- If using NTLM\\Kerberos auth, make sure you provided valid credentials</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="51f3f-155">Raisons pour lesquelles le test peut avoir échoué</span><span class="sxs-lookup"><span data-stu-id="51f3f-155">Reasons why the test might have failed</span></span>

<span data-ttu-id="51f3f-156">Voici quelques raisons courantes pour lesquelles Test-CsPhoneBootstrap risque d’échouer :</span><span class="sxs-lookup"><span data-stu-id="51f3f-156">Here are some common reasons why Test-CsPhoneBootstrap might fail:</span></span>

  - <span data-ttu-id="51f3f-157">Vous avez peut-être spécifié une adresse SIP qui n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="51f3f-157">You might have specified a SIP address that is not valid.</span></span> <span data-ttu-id="51f3f-158">Vous pouvez vérifier l’exactitude d’une adresse SIP en utilisant une commande telle que celle-ci :</span><span class="sxs-lookup"><span data-stu-id="51f3f-158">You can verify that a SIP address is correct by using a command such as this one:</span></span>
    
        Get-CsUser -Identity "sip:kenmyer@litwareinc.com"

  - <span data-ttu-id="51f3f-159">Vous avez peut-être spécifié un code confidentiel qui n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="51f3f-159">You might have specified a PIN that is not valid.</span></span> <span data-ttu-id="51f3f-160">Même si vous ne pouvez pas récupérer le numéro de téléphone de l’utilisateur, vous pouvez vérifier que l’utilisateur a au moins un numéro de code confidentiel en utilisant une commande semblable à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="51f3f-160">Although you can't retrieve the user’s PIN number, you can verify that the user at least has a PIN number by using a command similar to this:</span></span>
    
        Get-CsClientPinInfo -Identity "sip:kenmyer@litwareinc.com"

  - <span data-ttu-id="51f3f-161">Vous avez peut-être spécifié un numéro de téléphone qui n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="51f3f-161">You might have specified a phone number that is not valid.</span></span> <span data-ttu-id="51f3f-162">Vous pouvez vérifier le téléphone d’un utilisateur à l’aide d’une commande semblable à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="51f3f-162">You can verify a user’s phone by using a command similar to the following:</span></span>
    
        Get-CsUser -Identity "sip:kenmyer@litwareinc.com" | Select-Object LineUri

  - <span data-ttu-id="51f3f-163">Le pool d’inscriptions n’est pas activé par DHCP.</span><span class="sxs-lookup"><span data-stu-id="51f3f-163">The Registrar pool is not DHCP-enabled.</span></span> <span data-ttu-id="51f3f-164">Pour déterminer si votre pool d’inscriptions est activé pour DHCP, exécutez l’applet de contrôle Get-CsRegistrarConfiguration et vérifiez la valeur de la propriété EnableDHCPServer.</span><span class="sxs-lookup"><span data-stu-id="51f3f-164">To determine whether your Registrar pool is enabled for DHCP, run the Get-CsRegistrarConfiguration cmdlet and check the value of the EnableDHCPServer property.</span></span> <span data-ttu-id="51f3f-165">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="51f3f-165">For example:</span></span>
    
        Get-CsRegistrarConfiguration -Identity "global"

<span data-ttu-id="51f3f-166"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="51f3f-166"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

