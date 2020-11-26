---
title: 'Lync Server 2013 : test de la configuration d’une base de données'
description: 'Lync Server 2013 : test de la configuration de la base de données.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing database configuration
ms:assetid: 60f7fcd2-5efe-4791-b159-b0f9bf39a41b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn727307(v=OCS.15)
ms:contentKeyID: 63969606
ms.date: 07/07/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2b9f88eee99c4a2d523cc84df401dcc1d7b9fe59
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441038"
---
# <a name="testing-database-configuration-in-lync-server-2013"></a><span data-ttu-id="7e715-103">Test de la configuration d’une base de données dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7e715-103">Testing database configuration in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7e715-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7e715-104">

<span> </span></span></span>

<span data-ttu-id="7e715-105">_**Dernière modification de la rubrique :** 2016-07-07_</span><span class="sxs-lookup"><span data-stu-id="7e715-105">_**Topic Last Modified:** 2016-07-07_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7e715-106">Échéancier de vérification</span><span class="sxs-lookup"><span data-stu-id="7e715-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="7e715-107">Jour</span><span class="sxs-lookup"><span data-stu-id="7e715-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e715-108">Outil de test</span><span class="sxs-lookup"><span data-stu-id="7e715-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="7e715-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="7e715-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e715-110">Autorisations requises</span><span class="sxs-lookup"><span data-stu-id="7e715-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="7e715-111">Lorsque l’application est exécutée en local à l’aide de Lync Server Management Shell, les utilisateurs doivent être membres du groupe de sécurité RTCUniversalServerAdmins et doivent disposer de privilèges d’administrateur sur le serveur SQL Server.</span><span class="sxs-lookup"><span data-stu-id="7e715-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group, and need to have Administrator privileges on the SQL server.</span></span></p>
<p><span data-ttu-id="7e715-112">Lors de l’exécution à l’aide d’une instance distante de Windows PowerShell, un rôle RBAC doit être attribué aux utilisateurs qui ont l’autorisation d’exécuter l’applet de commande <strong>test-CsDatabase</strong> .</span><span class="sxs-lookup"><span data-stu-id="7e715-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the <strong>Test-CsDatabase</strong> cmdlet.</span></span> <span data-ttu-id="7e715-113">Pour afficher la liste de tous les rôles RBAC qui peuvent utiliser cette applet de commande, exécutez la commande suivante à partir de l’invite Windows PowerShell :</span><span class="sxs-lookup"><span data-stu-id="7e715-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsDatabase&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="7e715-114">Description</span><span class="sxs-lookup"><span data-stu-id="7e715-114">Description</span></span>

<span data-ttu-id="7e715-115">L’applet de **contrôle test-CsDatabase** vérifie la connectivité à une ou plusieurs bases de données Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="7e715-115">The **Test-CsDatabase** cmdlet verifies connectivity to one or more Lync Server 2013 databases.</span></span> <span data-ttu-id="7e715-116">Lors de l’exécution, l’applet de connexion **test-CsDatabase** lit la topologie du serveur Lync, tente de se connecter aux bases de données pertinentes, puis signale la réussite ou l’échec de chaque tentative.</span><span class="sxs-lookup"><span data-stu-id="7e715-116">When run, the **Test-CsDatabase** cmdlet reads the Lync Server topology, attempts to connect to relevant databases, and then reports back the success or failure of each try.</span></span> <span data-ttu-id="7e715-117">S’il est possible de créer une connexion, l’applet de contrôle renvoie également des informations telles que le nom de la base de données, les informations de version de SQL Server et l’emplacement de toutes les bases de données de miroirs installées.</span><span class="sxs-lookup"><span data-stu-id="7e715-117">If a connection can be made, the cmdlet will also report back such information as the database name, SQL Server version information, and the location of any installed mirror databases.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="7e715-118">Exécution du test</span><span class="sxs-lookup"><span data-stu-id="7e715-118">Running the test</span></span>

<span data-ttu-id="7e715-119">La commande décrite dans l’exemple 1 vérifie la configuration de la base de données de gestion centrale.</span><span class="sxs-lookup"><span data-stu-id="7e715-119">The command shown in Example 1 verifies the configuration of the Central Management database.</span></span>

    Test-CsDatabase -CentralManagementDatabase

<span data-ttu-id="7e715-120">L’exemple 2 vérifie toutes les bases de données serveur Lync installées sur l’ordinateur atl-sql-001.litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="7e715-120">Example 2 verifies all the Lync Server databases installed on the computer atl-sql-001.litwareinc.com.</span></span>

    Test-CsDatabase -ConfiguredDatabases -SqlServerFqdn "atl-sql-001.litwareinc.com"

<span data-ttu-id="7e715-121">Dans l’exemple 3, la vérification est effectuée uniquement pour la base de données d’archivage installée sur l’ordinateur atl-sql-001.litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="7e715-121">In Example 3, verification is performed only for the Archiving database installed on the computer atl-sql-001.litwareinc.com.</span></span> <span data-ttu-id="7e715-122">Notez que le paramètre SqlInstanceName est inclus pour spécifier l’instance SQL Server (Archinst) de l’emplacement de la base de données d’archivage.</span><span class="sxs-lookup"><span data-stu-id="7e715-122">Note that the SqlInstanceName parameter is included to specify the SQL Server instance (Archinst) where the Archiving database is located.</span></span>

    Test-CsDatabase -DatabaseType "Archiving" -SqlServerFqdn "atl-sql-001.litwareinc.com" -SqlInstanceName "archinst"

<span data-ttu-id="7e715-123">La commande affichée dans l’exemple 4 vérifie les bases de données installées sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="7e715-123">The command shown in Example 4 verifies the databases installed on the local computer.</span></span>

    Test-CsDatabase -LocalService

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="7e715-124">Détermination du succès ou de l’échec</span><span class="sxs-lookup"><span data-stu-id="7e715-124">Determining success or failure</span></span>

<span data-ttu-id="7e715-125">Si la connectivité de la base de données est correctement configurée, vous recevrez une sortie similaire à celle-ci, avec la propriété réussite marquée comme **vraie**:</span><span class="sxs-lookup"><span data-stu-id="7e715-125">If database connectivity is configured correctly, you'll receive output similar to this, with the Succeed property marked as **True**:</span></span>

<span data-ttu-id="7e715-126">SqlServerFqdn : atl-sql-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="7e715-126">SqlServerFqdn : atl-sql-001.litwareinc.com</span></span>

<span data-ttu-id="7e715-127">SqlInstanceName : RTC</span><span class="sxs-lookup"><span data-stu-id="7e715-127">SqlInstanceName : rtc</span></span>

<span data-ttu-id="7e715-128">MirrorSqlServerFqdn :</span><span class="sxs-lookup"><span data-stu-id="7e715-128">MirrorSqlServerFqdn :</span></span>

<span data-ttu-id="7e715-129">MirrorSqlInstanceName :</span><span class="sxs-lookup"><span data-stu-id="7e715-129">MirrorSqlInstanceName :</span></span>

<span data-ttu-id="7e715-130">DatabaseName : XDS</span><span class="sxs-lookup"><span data-stu-id="7e715-130">DatabaseName : xds</span></span>

<span data-ttu-id="7e715-131">DataSource :</span><span class="sxs-lookup"><span data-stu-id="7e715-131">DataSource :</span></span>

<span data-ttu-id="7e715-132">SQLServerVersion :</span><span class="sxs-lookup"><span data-stu-id="7e715-132">SQLServerVersion :</span></span>

<span data-ttu-id="7e715-133">ExpectedVersion : 10.13.2</span><span class="sxs-lookup"><span data-stu-id="7e715-133">ExpectedVersion : 10.13.2</span></span>

<span data-ttu-id="7e715-134">InstalledVersion :</span><span class="sxs-lookup"><span data-stu-id="7e715-134">InstalledVersion :</span></span>

<span data-ttu-id="7e715-135">Réussite : vrai</span><span class="sxs-lookup"><span data-stu-id="7e715-135">Succeed : True</span></span>

<span data-ttu-id="7e715-136">SqlServerFqdn : atl-sql-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="7e715-136">SqlServerFqdn : atl-sql-001.litwareinc.com</span></span>

<span data-ttu-id="7e715-137">SqlInstanceName : RTC</span><span class="sxs-lookup"><span data-stu-id="7e715-137">SqlInstanceName : rtc</span></span>

<span data-ttu-id="7e715-138">MirrorSqlServerFqdn :</span><span class="sxs-lookup"><span data-stu-id="7e715-138">MirrorSqlServerFqdn :</span></span>

<span data-ttu-id="7e715-139">MirrorSqlInstanceName :</span><span class="sxs-lookup"><span data-stu-id="7e715-139">MirrorSqlInstanceName :</span></span>

<span data-ttu-id="7e715-140">DatabaseName : lis</span><span class="sxs-lookup"><span data-stu-id="7e715-140">DatabaseName : lis</span></span>

<span data-ttu-id="7e715-141">DataSource :</span><span class="sxs-lookup"><span data-stu-id="7e715-141">DataSource :</span></span>

<span data-ttu-id="7e715-142">SQLServerVersion :</span><span class="sxs-lookup"><span data-stu-id="7e715-142">SQLServerVersion :</span></span>

<span data-ttu-id="7e715-143">ExpectedVersion : 3.1.1</span><span class="sxs-lookup"><span data-stu-id="7e715-143">ExpectedVersion : 3.1.1</span></span>

<span data-ttu-id="7e715-144">InstalledVersion :</span><span class="sxs-lookup"><span data-stu-id="7e715-144">InstalledVersion :</span></span>

<span data-ttu-id="7e715-145">Réussite : vrai</span><span class="sxs-lookup"><span data-stu-id="7e715-145">Succeed : True</span></span>

<span data-ttu-id="7e715-146">Si la base de données est configurée correctement mais toujours disponible, le champ réussite s’affichera comme **faux**, et des alertes et informations supplémentaires seront fournies :</span><span class="sxs-lookup"><span data-stu-id="7e715-146">If the database is configured correctly but still available, the Succeed field will be shown as **False**, and additional warnings and information will be provided:</span></span>

<span data-ttu-id="7e715-147">SqlServerFqdn : atl-sql-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="7e715-147">SqlServerFqdn : atl-sql-001.litwareinc.com</span></span>

<span data-ttu-id="7e715-148">SqlInstanceName : RTC</span><span class="sxs-lookup"><span data-stu-id="7e715-148">SqlInstanceName : rtc</span></span>

<span data-ttu-id="7e715-149">MirrorSqlServerFqdn :</span><span class="sxs-lookup"><span data-stu-id="7e715-149">MirrorSqlServerFqdn :</span></span>

<span data-ttu-id="7e715-150">MirrorSqlInstanceName :</span><span class="sxs-lookup"><span data-stu-id="7e715-150">MirrorSqlInstanceName :</span></span>

<span data-ttu-id="7e715-151">DatabaseName : XDS</span><span class="sxs-lookup"><span data-stu-id="7e715-151">DatabaseName : xds</span></span>

<span data-ttu-id="7e715-152">DataSource :</span><span class="sxs-lookup"><span data-stu-id="7e715-152">DataSource :</span></span>

<span data-ttu-id="7e715-153">SQLServerVersion :</span><span class="sxs-lookup"><span data-stu-id="7e715-153">SQLServerVersion :</span></span>

<span data-ttu-id="7e715-154">ExpectedVersion : 10.13.2</span><span class="sxs-lookup"><span data-stu-id="7e715-154">ExpectedVersion : 10.13.2</span></span>

<span data-ttu-id="7e715-155">InstalledVersion :</span><span class="sxs-lookup"><span data-stu-id="7e715-155">InstalledVersion :</span></span>

<span data-ttu-id="7e715-156">Réussite : faux</span><span class="sxs-lookup"><span data-stu-id="7e715-156">Succeed : False</span></span>

<span data-ttu-id="7e715-157">SqlServerFqdn : atl-cs-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="7e715-157">SqlServerFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="7e715-158">SqlInstanceName : RTC</span><span class="sxs-lookup"><span data-stu-id="7e715-158">SqlInstanceName : rtc</span></span>

<span data-ttu-id="7e715-159">MirrorSqlServerFqdn :</span><span class="sxs-lookup"><span data-stu-id="7e715-159">MirrorSqlServerFqdn :</span></span>

<span data-ttu-id="7e715-160">MirrorSqlInstanceName :</span><span class="sxs-lookup"><span data-stu-id="7e715-160">MirrorSqlInstanceName :</span></span>

<span data-ttu-id="7e715-161">DatabaseName : lis</span><span class="sxs-lookup"><span data-stu-id="7e715-161">DatabaseName : lis</span></span>

<span data-ttu-id="7e715-162">DataSource :</span><span class="sxs-lookup"><span data-stu-id="7e715-162">DataSource :</span></span>

<span data-ttu-id="7e715-163">SQLServerVersion :</span><span class="sxs-lookup"><span data-stu-id="7e715-163">SQLServerVersion :</span></span>

<span data-ttu-id="7e715-164">ExpectedVersion : 3.1.1</span><span class="sxs-lookup"><span data-stu-id="7e715-164">ExpectedVersion : 3.1.1</span></span>

<span data-ttu-id="7e715-165">InstalledVersion :</span><span class="sxs-lookup"><span data-stu-id="7e715-165">InstalledVersion :</span></span>

<span data-ttu-id="7e715-166">Réussite : faux</span><span class="sxs-lookup"><span data-stu-id="7e715-166">Succeed : False</span></span>

<span data-ttu-id="7e715-167">AVERTISSEMENT : Test-CsDatabase rencontré des erreurs.</span><span class="sxs-lookup"><span data-stu-id="7e715-167">WARNING: Test-CsDatabase encountered errors.</span></span> <span data-ttu-id="7e715-168">Consulter le fichier journal d’un</span><span class="sxs-lookup"><span data-stu-id="7e715-168">Consult the log file for a</span></span>

<span data-ttu-id="7e715-169">analyse détaillée et vérification de la prise en considération de toutes les erreurs (2) et avertissements (0)</span><span class="sxs-lookup"><span data-stu-id="7e715-169">detailed analysis, and to make sure that all errors (2) and warnings (0) are addressed</span></span>

<span data-ttu-id="7e715-170">avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="7e715-170">before continuing.</span></span>

<span data-ttu-id="7e715-171">AVERTISSEMENT : des résultats détaillés sont disponibles à l’adresse suivante :</span><span class="sxs-lookup"><span data-stu-id="7e715-171">WARNING: Detailed results can be found at</span></span>

<span data-ttu-id="7e715-172">"C : \\ les utilisateurs \\ testent \\ AppData \\ local \\ temp \\ 2 \\ test-CsDatabase-b18d488a-8044-4679-bbf2-</span><span class="sxs-lookup"><span data-stu-id="7e715-172">"C:\\Users\\Testing\\AppData\\Local\\Temp\\2\\Test-CsDatabase-b18d488a-8044-4679-bbf2-</span></span>

<span data-ttu-id="7e715-173">04d593cce8e6.html».</span><span class="sxs-lookup"><span data-stu-id="7e715-173">04d593cce8e6.html".</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="7e715-174">Raisons pour lesquelles le test peut avoir échoué</span><span class="sxs-lookup"><span data-stu-id="7e715-174">Reasons why the test might have failed</span></span>

<span data-ttu-id="7e715-175">Voici quelques raisons courantes pour lesquelles **les tests-CsDatabase** peuvent échouer :</span><span class="sxs-lookup"><span data-stu-id="7e715-175">Here are some common reasons why **Test-CsDatabase** might fail:</span></span>

  - <span data-ttu-id="7e715-176">Une valeur de paramètre incorrecte a été fournie.</span><span class="sxs-lookup"><span data-stu-id="7e715-176">An incorrect parameter value was supplied.</span></span> <span data-ttu-id="7e715-177">S’il est utilisé, les paramètres facultatifs doivent être correctement configurés ou le test échoue.</span><span class="sxs-lookup"><span data-stu-id="7e715-177">If used, the optional parameters must be configured correctly or the test will fail.</span></span> <span data-ttu-id="7e715-178">Réexécutez la commande sans les paramètres facultatifs et déterminez si l’opération aboutit.</span><span class="sxs-lookup"><span data-stu-id="7e715-178">Rerun the command without the optional parameters and see whether that succeeds.</span></span>

  - <span data-ttu-id="7e715-179">Cette commande échoue si la base de données est mal configurée ou n’est pas encore déployée.</span><span class="sxs-lookup"><span data-stu-id="7e715-179">This command will fail if the database is misconfigured or not yet deployed.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="7e715-180">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7e715-180">See Also</span></span>


[<span data-ttu-id="7e715-181">Get-CsDatabaseMirrorState</span><span class="sxs-lookup"><span data-stu-id="7e715-181">Get-CsDatabaseMirrorState</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsDatabaseMirrorState)  
[<span data-ttu-id="7e715-182">Get-CsService</span><span class="sxs-lookup"><span data-stu-id="7e715-182">Get-CsService</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsService)  
[<span data-ttu-id="7e715-183">Get-CsUserDatabaseState</span><span class="sxs-lookup"><span data-stu-id="7e715-183">Get-CsUserDatabaseState</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsUserDatabaseState)  
  

<span data-ttu-id="7e715-184"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7e715-184"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

