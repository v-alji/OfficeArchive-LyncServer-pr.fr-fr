---
title: 'Lync Server 2013 : test des services Lync Server'
description: 'Lync Server 2013 : test des services serveur Lync.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing Lync Server services
ms:assetid: b564b450-a746-4ec9-aabb-e076309ccd5f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn689119(v=OCS.15)
ms:contentKeyID: 63969644
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f04cf5e0c098c671b6fb126d4607f3cdba107712
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394484"
---
# <a name="testing-lync-server-services-in-lync-server-2013"></a><span data-ttu-id="facc1-103">Test des services serveur Lync dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="facc1-103">Testing Lync Server services in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="facc1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="facc1-104">

<span> </span></span></span>

<span data-ttu-id="facc1-105">_**Dernière modification de la rubrique :** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="facc1-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="facc1-106">Échéancier de vérification</span><span class="sxs-lookup"><span data-stu-id="facc1-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="facc1-107">Jour</span><span class="sxs-lookup"><span data-stu-id="facc1-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="facc1-108">Outil de test</span><span class="sxs-lookup"><span data-stu-id="facc1-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="facc1-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="facc1-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="facc1-110">Autorisations requises</span><span class="sxs-lookup"><span data-stu-id="facc1-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="facc1-111">Lorsque l’application est exécutée localement à l’aide de Lync Server Management Shell, les utilisateurs doivent être membres du groupe de sécurité RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="facc1-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="facc1-112">Lors de l’exécution à l’aide d’une instance distante de Windows PowerShell, un rôle RBAC doit être attribué aux utilisateurs qui ont l’autorisation d’exécuter l’applet de commande Test-CsComputer.</span><span class="sxs-lookup"><span data-stu-id="facc1-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsComputer cmdlet.</span></span> <span data-ttu-id="facc1-113">Pour afficher la liste de tous les rôles RBAC qui peuvent utiliser cette applet de commande, exécutez la commande suivante à partir de l’invite Windows PowerShell :</span><span class="sxs-lookup"><span data-stu-id="facc1-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsComputer&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="facc1-114">Description</span><span class="sxs-lookup"><span data-stu-id="facc1-114">Description</span></span>

<span data-ttu-id="facc1-115">Test-CsComputer vérifie l’état de tous les services Lync Server 2013 en cours d’exécution sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="facc1-115">Test-CsComputer verifies the status of all the Lync Server 2013 services that are running on the local computer.</span></span> <span data-ttu-id="facc1-116">(Test-CsComputer peut uniquement être exécuté localement, il ne peut pas être exécuté à partir d’une instance distante de Windows PowerShell.) L’applet de contrôle vérifie également si les ports de pare-feu appropriés sont ouverts sur l’ordinateur et détermine si les groupes Active Directory créés lors de l’installation de Lync Server 2013 ont été ajoutés aux groupes locaux correspondants.</span><span class="sxs-lookup"><span data-stu-id="facc1-116">(Test-CsComputer can only be run locally, it cannot be run from a remote instance of Windows PowerShell.) The cmdlet also checks whether the appropriate firewall ports are opened on the computer, and determines whether the Active Directory groups that were created when you installed Lync Server 2013 were added to the corresponding local groups.</span></span> <span data-ttu-id="facc1-117">Par exemple, Test-CsComputer vérifiera que le groupe Active Directory RTCUniversalUserAdmins a été ajouté au groupe administrateurs.</span><span class="sxs-lookup"><span data-stu-id="facc1-117">For example, Test-CsComputer will verify that the Active Directory group RTCUniversalUserAdmins was added to the Administrators group.</span></span>

<span data-ttu-id="facc1-118">Pour plus d’informations, consultez la documentation d’aide de l’applet de [contrôle test-CsComputer](https://docs.microsoft.com/powershell/module/skype/Test-CsComputer) .</span><span class="sxs-lookup"><span data-stu-id="facc1-118">For more information, see the Help documentation for the [Test-CsComputer](https://docs.microsoft.com/powershell/module/skype/Test-CsComputer) cmdlet.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="facc1-119">Exécution du test</span><span class="sxs-lookup"><span data-stu-id="facc1-119">Running the test</span></span>

<span data-ttu-id="facc1-120">L’applet de commande Test-CsComputer ne peut être exécutée que sur l’ordinateur local, vous ne pouvez pas appeler Test-CsComputer à partir d’une instance distante de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="facc1-120">The Test-CsComputer cmdlet can only be run on the local computer, you can't call Test-CsComputer from a remote instance of Windows PowerShell.</span></span> <span data-ttu-id="facc1-121">Par défaut, Test-CsComputer affiche un peu de sortie à l’écran, les informations renvoyées par l’applet de passe sont écrites dans un fichier HTML.</span><span class="sxs-lookup"><span data-stu-id="facc1-121">By default, Test-CsComputer displays very little output on-screen, instead information returned by the cmdlet is written to an HTML file.</span></span> <span data-ttu-id="facc1-122">Pour cette raison, nous vous recommandons d’inclure le paramètre Verbose et le paramètre de rapport chaque fois que vous exécutez test-CsComputer.</span><span class="sxs-lookup"><span data-stu-id="facc1-122">Because of that, we recommend that you include the Verbose parameter and the Report parameter any time that you run Test-CsComputer.</span></span> <span data-ttu-id="facc1-123">Le paramètre Verbose fournit un affichage à l’écran détaillé légèrement plus détaillé lors de l’exécution de la cmdlet.</span><span class="sxs-lookup"><span data-stu-id="facc1-123">The Verbose parameter will provide slightly more detailed output on-screen while the cmdlet runs.</span></span> <span data-ttu-id="facc1-124">Le paramètre rapport vous permet de spécifier un chemin d’accès et un nom de fichier pour le fichier HTML généré par test-CsComputer.</span><span class="sxs-lookup"><span data-stu-id="facc1-124">The Report parameter allows you to specify a file path and file name for the HTML file generated by Test-CsComputer.</span></span> <span data-ttu-id="facc1-125">Si vous n’incluez pas le paramètre de rapport, le fichier HTML sera automatiquement enregistré dans votre dossier utilisateurs et donner un nom semblable à ce qui suit : ce84964a-c4da-4622-ad34-c54ff3ed361f.html.</span><span class="sxs-lookup"><span data-stu-id="facc1-125">If you do not include the Report parameter the HTML file will automatically be saved to your Users folder and be given a name similar to this: ce84964a-c4da-4622-ad34-c54ff3ed361f.html.</span></span>

<span data-ttu-id="facc1-126">L’exemple de commande suivant exécute Test-CsComputer et enregistre la sortie dans un fichier nommé C : \\ Logs \\ComputerTest.html :</span><span class="sxs-lookup"><span data-stu-id="facc1-126">The following sample command runs Test-CsComputer and saves the output to a file that is named C:\\Logs\\ComputerTest.html:</span></span>

    Test-CsComputer -Report "C:\Logs\ComputerTest.html" -Verbose

<span data-ttu-id="facc1-127">Pour plus d’informations, consultez la documentation d’aide de l’applet de [contrôle test-CsComputer](https://docs.microsoft.com/powershell/module/skype/Test-CsComputer) .</span><span class="sxs-lookup"><span data-stu-id="facc1-127">For more information, see the Help documentation for the [Test-CsComputer](https://docs.microsoft.com/powershell/module/skype/Test-CsComputer) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="facc1-128">Détermination du succès ou de l’échec</span><span class="sxs-lookup"><span data-stu-id="facc1-128">Determining success or failure</span></span>

<span data-ttu-id="facc1-129">En raison du nombre de contrôles de vérification qu’il effectue, Test-CsComputer ne rapporte pas une simple **Oui, le test a réussi** ou **non, le test a échoué**.</span><span class="sxs-lookup"><span data-stu-id="facc1-129">Because of the number of verification checks that it performs, Test-CsComputer does not report back a simple **Yes, the test succeeded** or **No, the test failed**.</span></span> <span data-ttu-id="facc1-130">Au lieu de cela, vous devez afficher le fichier HTML généré à l’aide d’Internet Explorer pour déterminer la réussite ou l’échec de chaque test.</span><span class="sxs-lookup"><span data-stu-id="facc1-130">Instead, you have to view the generated HTML file by using Internet Explorer to determine the success or failure of each test.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="facc1-131">Raisons pour lesquelles le test peut avoir échoué</span><span class="sxs-lookup"><span data-stu-id="facc1-131">Reasons why the test might have failed</span></span>

<span data-ttu-id="facc1-132">Voici quelques raisons courantes pour lesquelles Test-CsComputer risque d’échouer :</span><span class="sxs-lookup"><span data-stu-id="facc1-132">Here are some common reasons why Test-CsComputer might fail:</span></span>

  - <span data-ttu-id="facc1-133">L’ordinateur de test n’est peut-être pas activé pour une utilisation avec Lync Server.</span><span class="sxs-lookup"><span data-stu-id="facc1-133">The test computer might not be enabled for use with Lync Server.</span></span> <span data-ttu-id="facc1-134">Cela peut se produire si les services serveur Lync ou les rôles serveur sur l’ordinateur ont changé et que l’applet de Enable-CsComputer n’était pas exécutée.</span><span class="sxs-lookup"><span data-stu-id="facc1-134">This can occur if the Lync Server services or server roles on the computer have changed and the Enable-CsComputer cmdlet was not run.</span></span> <span data-ttu-id="facc1-135">Pour résoudre ce problème, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="facc1-135">To resolve this issue, run the following command:</span></span>
    
        Enable-CsComputer

  - <span data-ttu-id="facc1-136">La réplication n’est peut-être pas à jour sur l’ordinateur de test.</span><span class="sxs-lookup"><span data-stu-id="facc1-136">Replication might not be up to date on the test computer.</span></span> <span data-ttu-id="facc1-137">Vous pouvez vérifier l’état de réplication actuel d’un ordinateur en exécutant l’applet de contrôle Get-CsManagementStoreReplicationStatus :</span><span class="sxs-lookup"><span data-stu-id="facc1-137">You can check the current replication status for a computer by running the Get-CsManagementStoreReplicationStatus cmdlet:</span></span>
    
        Get-CsManagementStoreReplicationStatus -ReplicaFqdn "atl-cs-001.litwareinc.com"
    
    <span data-ttu-id="facc1-138">Si l’état de la réplication n’est pas à jour, vous pouvez le faire manuellement en utilisant une commande similaire à celle-ci :</span><span class="sxs-lookup"><span data-stu-id="facc1-138">If the replication status is not up to date, you can manually force replication to occur by using a command similar to this:</span></span>
    
        Invoke-CsManagementStoreReplication -ReplicaFqdn "atl-cs-001.litwareinc.com"

  - <span data-ttu-id="facc1-139">La topologie peut être activée.</span><span class="sxs-lookup"><span data-stu-id="facc1-139">The topology might have to be enabled.</span></span> <span data-ttu-id="facc1-140">Si vous modifiez la topologie du serveur Lync (modifications qui peuvent affecter l’ordinateur local), vous devez activer la nouvelle topologie.</span><span class="sxs-lookup"><span data-stu-id="facc1-140">If you change the Lync Server topology (changes that might affect the local computer), then you must enable the new topology.</span></span> <span data-ttu-id="facc1-141">Vous pouvez activer la topologie à tout moment en exécutant la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="facc1-141">You can enable the topology at any time by running this command:</span></span>
    
        Enable-CsTopology

<span data-ttu-id="facc1-142"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="facc1-142"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

