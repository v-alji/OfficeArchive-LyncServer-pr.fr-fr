---
title: 'Lync Server 2013 : tester les autorisations d’administrateur'
description: 'Lync Server 2013 : tester les autorisations d’administrateur.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test admin permissions
ms:assetid: 5dda3efd-0f84-4848-819e-87b1551066b1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn767945(v=OCS.15)
ms:contentKeyID: 63969607
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 07e15be288ed31afe9303d91ce3e623d19822428
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444314"
---
# <a name="test-admin-permissions-in-lync-server-2013"></a><span data-ttu-id="bc9a1-103">Tester les autorisations d’administrateur dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bc9a1-103">Test admin permissions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bc9a1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bc9a1-104">

<span> </span></span></span>

<span data-ttu-id="bc9a1-105">_**Dernière modification de la rubrique :** 2014-08-18_</span><span class="sxs-lookup"><span data-stu-id="bc9a1-105">_**Topic Last Modified:** 2014-08-18_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bc9a1-106">Échéancier de vérification</span><span class="sxs-lookup"><span data-stu-id="bc9a1-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="bc9a1-107">Après le déploiement initial de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="bc9a1-107">After initial Lync Server deployment.</span></span> <span data-ttu-id="bc9a1-108">Le cas échéant, en cas de problèmes liés aux autorisations.</span><span class="sxs-lookup"><span data-stu-id="bc9a1-108">As needed if permission-related issues arise.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc9a1-109">Outil de test</span><span class="sxs-lookup"><span data-stu-id="bc9a1-109">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="bc9a1-110">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="bc9a1-110">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc9a1-111">Autorisations requises</span><span class="sxs-lookup"><span data-stu-id="bc9a1-111">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="bc9a1-112">Lorsque l’application est exécutée localement à l’aide de Lync Server Management Shell, les utilisateurs doivent être membres du groupe de sécurité RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="bc9a1-112">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="bc9a1-113">Lors de l’exécution à l’aide d’une instance distante de Windows PowerShell, un rôle RBAC doit être attribué aux utilisateurs qui ont l’autorisation d’exécuter l’applet de commande Test-CsOUPermission.</span><span class="sxs-lookup"><span data-stu-id="bc9a1-113">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsOUPermission cmdlet.</span></span> <span data-ttu-id="bc9a1-114">Pour afficher la liste de tous les rôles RBAC qui peuvent utiliser cette applet de commande, exécutez la commande suivante à partir de l’invite Windows PowerShell :</span><span class="sxs-lookup"><span data-stu-id="bc9a1-114">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsOUPermission&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="bc9a1-115">Description</span><span class="sxs-lookup"><span data-stu-id="bc9a1-115">Description</span></span>

<span data-ttu-id="bc9a1-116">Lorsque vous installez Lync Server 2013 1, les tâches effectuées par le programme d’installation fournissent au groupe RTCUniversalUserAdmins les autorisations Active Directory nécessaires pour gérer les utilisateurs, ordinateurs, contacts, contacts d’application et personnes InetOrg.</span><span class="sxs-lookup"><span data-stu-id="bc9a1-116">When you install Lync Server 2013 one of the tasks that were performed by the Setup program gives the RTCUniversalUserAdmins group the Active Directory permissions that are needed to manage users, computers, contacts, application contacts, and InetOrg persons.</span></span> <span data-ttu-id="bc9a1-117">Si vous avez désactivé l’héritage des autorisations dans le programme d’installation d’Active Directory, vous ne pourrez pas affecter ces autorisations.</span><span class="sxs-lookup"><span data-stu-id="bc9a1-117">If you have disabled permission inheritance in Active Directory setup won't be able to assign those permissions.</span></span> <span data-ttu-id="bc9a1-118">Les membres du groupe RTCUniversalUserAdmins ne seront donc pas en mesure de gérer les entités du serveur Lync.</span><span class="sxs-lookup"><span data-stu-id="bc9a1-118">As a result, members of the RTCUniversalUserAdmins group won't be able to manage Lync Server entities.</span></span> <span data-ttu-id="bc9a1-119">Ces privilèges de gestion ne seront accessibles qu’aux administrateurs de domaine.</span><span class="sxs-lookup"><span data-stu-id="bc9a1-119">Those management privileges will only be available to domain administrators.</span></span>

<span data-ttu-id="bc9a1-120">L’applet de contrôle Test-CsOUPermission vérifie que les autorisations requises nécessaires pour gérer les utilisateurs, les ordinateurs et d’autres objets sont définies sur un conteneur Active Directory.</span><span class="sxs-lookup"><span data-stu-id="bc9a1-120">The Test-CsOUPermission cmdlet verifies that the required permissions that are needed to manage users, computers, and other objects are set on an Active Directory container.</span></span> <span data-ttu-id="bc9a1-121">Si ces autorisations ne sont pas définies, vous pouvez résoudre ce problème en exécutant l’applet de la cmdlet [Grant-CsOUPermission](https://docs.microsoft.com/powershell/module/skype/Grant-CsOUPermission) .</span><span class="sxs-lookup"><span data-stu-id="bc9a1-121">If those permissions are not set, you can resolve this problem by running the [Grant-CsOUPermission](https://docs.microsoft.com/powershell/module/skype/Grant-CsOUPermission) cmdlet.</span></span>

<span data-ttu-id="bc9a1-122">Notez que les Grant-CsOUPermission peuvent affecter des autorisations uniquement aux membres du groupe RTCUniversalUserAdmins.</span><span class="sxs-lookup"><span data-stu-id="bc9a1-122">Note that Grant-CsOUPermission can only assign permissions to members of the RTCUniversalUserAdmins group.</span></span> <span data-ttu-id="bc9a1-123">Vous ne pouvez pas utiliser cette applet de cmdlet pour accorder des autorisations à un utilisateur ou à un groupe arbitraire.</span><span class="sxs-lookup"><span data-stu-id="bc9a1-123">You can’t use this cmdlet to grant permissions to an arbitrary user or group.</span></span> <span data-ttu-id="bc9a1-124">Si vous souhaitez qu’un autre utilisateur ou groupe dispose d’autorisations de gestion des utilisateurs, vous devez ajouter cet utilisateur (ou groupe) au groupe RTCUniversalUserAdmins.</span><span class="sxs-lookup"><span data-stu-id="bc9a1-124">If you want a different user or group to have user management permissions, you should add that user (or group) to the RTCUniversalUserAdmins group.</span></span>

<span data-ttu-id="bc9a1-125">Pour plus d’informations sur les autorisations d’UO, voir l’article l' [héritage des autorisations est désactivé sur les ordinateurs, les utilisateurs ou les conteneurs InetOrgPerson dans Lync Server 2013](lync-server-2013-permissions-inheritance-is-disabled-on-computers-users-or-inetorgperson-containers.md).</span><span class="sxs-lookup"><span data-stu-id="bc9a1-125">For more information on OU permissions, see the article [Permissions inheritance Is disabled on computers, users, or InetOrgPerson containers in Lync Server 2013](lync-server-2013-permissions-inheritance-is-disabled-on-computers-users-or-inetorgperson-containers.md).</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="bc9a1-126">Exécution du test</span><span class="sxs-lookup"><span data-stu-id="bc9a1-126">Running the test</span></span>

<span data-ttu-id="bc9a1-127">Pour vérifier que les autorisations de gestion sont définies sur un conteneur, exécutez l’applet de contrôle Test-CsOUPermission suivi du nom unique du conteneur et du type d’autorisations que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="bc9a1-127">To verify that management permissions are set on a container, run the Test-CsOUPermission cmdlet followed by the distinguished name of the container and by the type of permissions that you are verifying.</span></span> <span data-ttu-id="bc9a1-128">Par exemple, cette commande vérifie si les autorisations des utilisateurs sont définies sur l’unité d’organisation UO = Redmond, DC = litwareinc, DC = com :</span><span class="sxs-lookup"><span data-stu-id="bc9a1-128">For example, this command checks whether user permissions are set on the OU ou=Redmond,dc=litwareinc,dc=com:</span></span>

    Test-CsOUPermission -OU "ou=Redmond,dc=litwareinc,dc=com" -ObjectType "user"

<span data-ttu-id="bc9a1-129">Pour vérifier plusieurs autorisations en utilisant une seule commande, placez chaque type d’autorisation entre guillemets, puis séparez-les par des virgules.</span><span class="sxs-lookup"><span data-stu-id="bc9a1-129">To verify multiple permissions by using a single command, enclose each permission type enclosed in quotation marks, then separate those types by using commas.</span></span> <span data-ttu-id="bc9a1-130">Par exemple, la commande suivante vérifie les autorisations de l’utilisateur, de l’ordinateur et des contacts :</span><span class="sxs-lookup"><span data-stu-id="bc9a1-130">For example, this one command verifies user, computer, and contact permissions:</span></span>

    Test-CsOUPermission -OU "ou=Redmond,dc=litwareinc,dc=com" -ObjectType "user", "computer", "contact"

<span data-ttu-id="bc9a1-131">Pour plus d’informations, consultez la rubrique d’aide de l’applet de [contrôle test-CsOUPermission](https://docs.microsoft.com/powershell/module/skype/Test-CsOUPermission) .</span><span class="sxs-lookup"><span data-stu-id="bc9a1-131">For more information, see the help topic for the [Test-CsOUPermission](https://docs.microsoft.com/powershell/module/skype/Test-CsOUPermission) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="bc9a1-132">Détermination du succès ou de l’échec</span><span class="sxs-lookup"><span data-stu-id="bc9a1-132">Determining success or failure</span></span>

<span data-ttu-id="bc9a1-133">Si les autorisations requises ont déjà été définies, Test-CsOUPermission renverra une réponse à un mot :</span><span class="sxs-lookup"><span data-stu-id="bc9a1-133">If the required permissions have already been set then Test-CsOUPermission will return a one-word response:</span></span>

<span data-ttu-id="bc9a1-134">Vrai</span><span class="sxs-lookup"><span data-stu-id="bc9a1-134">True</span></span>

<span data-ttu-id="bc9a1-135">Si les autorisations requises ne sont pas définies, Test-CsOUPermission renverra la valeur false.</span><span class="sxs-lookup"><span data-stu-id="bc9a1-135">If the required permissions are not set then Test-CsOUPermission will return the value False.</span></span> <span data-ttu-id="bc9a1-136">Il se peut que vous deviez rechercher un moment pour trouver cette valeur.</span><span class="sxs-lookup"><span data-stu-id="bc9a1-136">You might have to search for a moment to find this value.</span></span> <span data-ttu-id="bc9a1-137">En général, il est intégré à plusieurs avertissements.</span><span class="sxs-lookup"><span data-stu-id="bc9a1-137">It will typically be embedded inside several accompanying warnings.</span></span> <span data-ttu-id="bc9a1-138">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="bc9a1-138">For example:</span></span>

<span data-ttu-id="bc9a1-139">AVERTISSEMENT : entrée de contrôle d’accès (ACE) ATL-CS-001 \\ RTCUniversalUserReadOnlyGroup ; allow ; ReadProperty; ContainerInherit; Descendants ; bf967aba-0de6-11D0-00aa003049e2 ; d819615a-3b9b-4738-b47e-f1bd8ee3aea4</span><span class="sxs-lookup"><span data-stu-id="bc9a1-139">WARNING: access control entry (ACE) atl-cs-001\\RTCUniversalUserReadOnlyGroup; allow; ReadProperty; ContainerInherit; Descendents; bf967aba-0de6-11d0-00aa003049e2; d819615a-3b9b-4738-b47e-f1bd8ee3aea4</span></span>

<span data-ttu-id="bc9a1-140">AVERTISSEMENT : les entrées de contrôle d’accès (ACE) sur l’objet « UO = AmeriqueduNord, DC = ATL-CS-001 \\ DC = litwareinc, DC = com » ne sont pas prêtes.</span><span class="sxs-lookup"><span data-stu-id="bc9a1-140">WARNING: The access control entries (ACEs) on the object "OU=NorthAmerica,DC=atl-cs-001\\DC=litwareinc,DC=com" are not ready.</span></span>

<span data-ttu-id="bc9a1-141">False</span><span class="sxs-lookup"><span data-stu-id="bc9a1-141">False</span></span>

<span data-ttu-id="bc9a1-142">AVERTISSEMENT : le traitement des « tests-CsOUPermission » s’est terminé avec des avertissements.</span><span class="sxs-lookup"><span data-stu-id="bc9a1-142">WARNING: "Test-CsOUPermission" processing has completed with warnings.</span></span> <span data-ttu-id="bc9a1-143">des avertissements "2" ont été enregistrés lors de cette exécution.</span><span class="sxs-lookup"><span data-stu-id="bc9a1-143">"2" warnings were recorded during this run.</span></span>

<span data-ttu-id="bc9a1-144">AVERTISSEMENT : des résultats détaillés sont disponibles à l’adresse « C : \\ Users \\ admin \\ AppData, \\ \\ Temp local \\Test-CsOUPermission-5d7a89af-f854-4a9c-87e3-69e37e58de.html ».</span><span class="sxs-lookup"><span data-stu-id="bc9a1-144">WARNING: Detailed results can be found at "C:\\Users\\Admin\\AppData\\Local\\Temp\\Test-CsOUPermission-5d7a89af-f854-4a9c-87e3-69e37e58de.html".</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="bc9a1-145">Raisons pour lesquelles le test peut avoir échoué</span><span class="sxs-lookup"><span data-stu-id="bc9a1-145">Reasons why the test might have failed</span></span>

<span data-ttu-id="bc9a1-146">Si Test-CsOUPermission échoue, cela signifie généralement que l’autorisation spécifiée n’a pas été affectée au groupe RTCUniversalUserAdmins.</span><span class="sxs-lookup"><span data-stu-id="bc9a1-146">If Test-CsOUPermission fails that will usually mean that the specified permission has not been assign to the RTCUniversalUserAdmins group.</span></span> <span data-ttu-id="bc9a1-147">Vous pouvez résoudre ce problème et affecter les autorisations requises à l’aide de l’applet de Grant-CsOUPermission.</span><span class="sxs-lookup"><span data-stu-id="bc9a1-147">You can resolve this problem, and assign the required permissions, by using the Grant-CsOUPermission cmdlet.</span></span> <span data-ttu-id="bc9a1-148">Par exemple, cette commande fournit les autorisations d’UO pour les utilisateurs, les contacts et inetOrgPersons au groupe RTCUniversalUserAdmins :</span><span class="sxs-lookup"><span data-stu-id="bc9a1-148">For example, this command gives OU permissions for users, contacts, and inetOrgPersons to the RTCUniversalUserAdmins group:</span></span>

    Grant-CsOUPermission -OU "ou=Redmond,dc=litwareinc,dc=com" -ObjectType "user", "contact", "inetOrgPerson"

<span data-ttu-id="bc9a1-149">Pour plus d’informations, consultez la rubrique d’aide de l’applet de Grant-CsOUPermission.</span><span class="sxs-lookup"><span data-stu-id="bc9a1-149">For more information, see the help topic for the Grant-CsOUPermission cmdlet.</span></span>

<span data-ttu-id="bc9a1-150"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bc9a1-150"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

