---
title: 'Lync Server 2013 : configuration des stratégies de qualité de service pour les clients exécutant Windows 7 ou Windows 8'
description: 'Lync Server 2013 : configuration des stratégies de qualité de service pour les clients exécutant Windows 7 ou Windows 8.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Quality of Service policies for clients running on Windows 7 or Windows 8
ms:assetid: efff2b98-b3fb-4183-a4f0-329a9105ce2c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205371(v=OCS.15)
ms:contentKeyID: 48185785
ms.date: 03/29/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: faba5fc54ef73bfc738f94ee7209fc46a7cdc208
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432694"
---
# <a name="configuring-quality-of-service-policies-in-lync-server-2013-for-clients-running-on-windows-7-or-windows-8"></a><span data-ttu-id="b15dc-103">Configuration des stratégies de qualité de service dans Lync Server 2013 pour les clients exécutant Windows 7 ou Windows 8</span><span class="sxs-lookup"><span data-stu-id="b15dc-103">Configuring Quality of Service policies in Lync Server 2013 for clients running on Windows 7 or Windows 8</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b15dc-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b15dc-104">

<span> </span></span></span>

<span data-ttu-id="b15dc-105">_**Dernière modification de la rubrique :** 2016-03-29_</span><span class="sxs-lookup"><span data-stu-id="b15dc-105">_**Topic Last Modified:** 2016-03-29_</span></span>

<span data-ttu-id="b15dc-106">Outre la spécification des plages de port destinées aux clients Lync, vous devez également créer des stratégies de qualité de service distinctes qui seront appliquées aux ordinateurs clients.</span><span class="sxs-lookup"><span data-stu-id="b15dc-106">In addition to specifying port ranges for use by your Lync clients you must also create separate Quality of Service policies that will be applied to client computers.</span></span> <span data-ttu-id="b15dc-107">(La qualité de service créée pour les serveurs de conférence, d’application et de médiation ne doit pas être appliquée aux ordinateurs clients.) Ces informations s’appliquent uniquement aux ordinateurs exécutant le client Lync 2013 et Windows 7 ou Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b15dc-107">(The Quality of Service policies created for Conferencing, Application, and Mediation servers should not be applied to client computers.) This information applies only to computers running the Lync 2013 client and either Windows 7 or Windows 8.</span></span>

<span data-ttu-id="b15dc-108">L’exemple suivant utilise ce jeu de plages de ports pour créer une stratégie audio et une stratégie de vidéo :</span><span class="sxs-lookup"><span data-stu-id="b15dc-108">The following example uses this set of port ranges to create an audio policy and a video policy:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b15dc-109">Type de trafic client</span><span class="sxs-lookup"><span data-stu-id="b15dc-109">Client Traffic Type</span></span></th>
<th><span data-ttu-id="b15dc-110">Début du port</span><span class="sxs-lookup"><span data-stu-id="b15dc-110">Port Start</span></span></th>
<th><span data-ttu-id="b15dc-111">Plage de ports</span><span class="sxs-lookup"><span data-stu-id="b15dc-111">Port Range</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b15dc-112">Audio</span><span class="sxs-lookup"><span data-stu-id="b15dc-112">Audio</span></span></p></td>
<td><p><span data-ttu-id="b15dc-113">50020</span><span class="sxs-lookup"><span data-stu-id="b15dc-113">50020</span></span></p></td>
<td><p><span data-ttu-id="b15dc-114">CX3-20</span><span class="sxs-lookup"><span data-stu-id="b15dc-114">20</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b15dc-115">Vidéo</span><span class="sxs-lookup"><span data-stu-id="b15dc-115">Video</span></span></p></td>
<td><p><span data-ttu-id="b15dc-116">58000</span><span class="sxs-lookup"><span data-stu-id="b15dc-116">58000</span></span></p></td>
<td><p><span data-ttu-id="b15dc-117">CX3-20</span><span class="sxs-lookup"><span data-stu-id="b15dc-117">20</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b15dc-118">Partage d'application</span><span class="sxs-lookup"><span data-stu-id="b15dc-118">Application sharing</span></span></p></td>
<td><p><span data-ttu-id="b15dc-119">42000</span><span class="sxs-lookup"><span data-stu-id="b15dc-119">42000</span></span></p></td>
<td><p><span data-ttu-id="b15dc-120">CX3-20</span><span class="sxs-lookup"><span data-stu-id="b15dc-120">20</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b15dc-121">Transfert de fichiers</span><span class="sxs-lookup"><span data-stu-id="b15dc-121">File transfer</span></span></p></td>
<td><p><span data-ttu-id="b15dc-122">42020</span><span class="sxs-lookup"><span data-stu-id="b15dc-122">42020</span></span></p></td>
<td><p><span data-ttu-id="b15dc-123">CX3-20</span><span class="sxs-lookup"><span data-stu-id="b15dc-123">20</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b15dc-124">Pour créer une stratégie audio de qualité de service pour les ordinateurs Windows 7 ou Windows 8, vous devez d’abord vous connecter à un ordinateur sur lequel la gestion des stratégies de groupe a été installée.</span><span class="sxs-lookup"><span data-stu-id="b15dc-124">To create a Quality of Service audio policy for Windows 7 or Windows 8 computers, first log on to a computer where Group Policy Management has been installed.</span></span> <span data-ttu-id="b15dc-125">Ouvrez gestion des stratégies de groupe (cliquez sur **Démarrer**, pointez sur **Outils d’administration**, cliquez sur **gestion des stratégies de groupe**), puis procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="b15dc-125">Open Group Policy Management (click **Start**, point to **Administrative Tools**, and then click **Group Policy Management**) and then complete the following procedure:</span></span>

1.  <span data-ttu-id="b15dc-126">Dans gestion des stratégies de groupe, recherchez le conteneur dans lequel la nouvelle stratégie doit être créée.</span><span class="sxs-lookup"><span data-stu-id="b15dc-126">In Group Policy Management, locate the container where the new policy should be created.</span></span> <span data-ttu-id="b15dc-127">Par exemple, si tous vos ordinateurs clients se trouvent dans une unité d’organisation nommée clients, la nouvelle stratégie doit être créée dans l’unité d’organisation cliente.</span><span class="sxs-lookup"><span data-stu-id="b15dc-127">For example, if all your client computers are located in an OU named Clients then the new policy should be created in the Client OU.</span></span>

2.  <span data-ttu-id="b15dc-128">Cliquez avec le bouton droit sur le conteneur approprié, puis cliquez sur **créer un objet de stratégie de groupe dans ce domaine et associez-le ici**.</span><span class="sxs-lookup"><span data-stu-id="b15dc-128">Right-click the appropriate container and then click **Create a GPO in this domain, and Link it here**.</span></span>

3.  <span data-ttu-id="b15dc-129">Dans la boîte de dialogue **nouvel objet GPO** , tapez le nom du nouvel objet de stratégie de groupe dans la zone **nom** (par exemple, **audio Lync**), puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="b15dc-129">In the **New GPO** dialog box, type a name for the new Group Policy object in the **Name** box (for example, **Lync Audio**) and then click **OK**.</span></span>

4.  <span data-ttu-id="b15dc-130">Cliquez avec le bouton droit sur la stratégie que vous venez de créer, puis cliquez sur **modifier**.</span><span class="sxs-lookup"><span data-stu-id="b15dc-130">Right-click the newly-created policy and then click **Edit**.</span></span>

5.  <span data-ttu-id="b15dc-131">Dans l’éditeur de gestion des stratégies de groupe, développez **Configuration ordinateur**, **stratégies**, développez **Paramètres Windows**, cliquez avec le bouton droit sur **QoS basée sur une stratégie**, puis cliquez sur **créer une nouvelle stratégie**.</span><span class="sxs-lookup"><span data-stu-id="b15dc-131">In the Group Policy Management Editor, expand **Computer Configuration**, expand **Policies**, expand **Windows Settings**, right-click **Policy-based QoS**, and then click **Create new policy**.</span></span>

6.  <span data-ttu-id="b15dc-132">Dans la boîte de dialogue **QoS basée sur une stratégie** , dans la page d’ouverture, tapez un nom pour la nouvelle stratégie (par exemple, **audio Lync**) dans la zone **nom** .</span><span class="sxs-lookup"><span data-stu-id="b15dc-132">In the **Policy-based QoS** dialog box, on the opening page, type a name for the new policy (e.g., **Lync Audio**) in the **Name** box.</span></span> <span data-ttu-id="b15dc-133">Sélectionnez **spécifier la valeur DSCP** et définissez la valeur sur **46**.</span><span class="sxs-lookup"><span data-stu-id="b15dc-133">Select **Specify DSCP Value** and set the value to **46**.</span></span> <span data-ttu-id="b15dc-134">Laissez l’option **spécifier le taux de limitation en sortie** non sélectionnée, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="b15dc-134">Leave **Specify Outbound Throttle Rate** unselected, and then click **Next**.</span></span>

7. <span data-ttu-id="b15dc-135">Sur la page suivante, sélectionnez **uniquement les applications ayant ce nom d’exécutable** , entrez le nom **Lync.exe**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="b15dc-135">On the next page, select **Only applications with this executable name** and enter the name **Lync.exe**, and then click **Next**.</span></span> <span data-ttu-id="b15dc-136">Ce paramètre indique à la stratégie de classer uniquement le trafic correspondant du client Lync.</span><span class="sxs-lookup"><span data-stu-id="b15dc-136">This setting instructs the policy to only prioritize matching traffic from the Lync client.</span></span>

8.  <span data-ttu-id="b15dc-137">Sur la troisième page, assurez-vous que toutes les **adresses IP source** et **adresse IP de destination** sont sélectionnées, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="b15dc-137">On the third page, make sure that both **Any source IP address** and **Any destination IP address** are selected and then click **Next**.</span></span> <span data-ttu-id="b15dc-138">Ces deux paramètres garantissent le fonctionnement de la gestion des paquets indépendamment de l’ordinateur (adresse IP) ayant envoyé ces paquets et de l’ordinateur (adresse IP) recevant ces paquets.</span><span class="sxs-lookup"><span data-stu-id="b15dc-138">These two settings ensure that packets will be managed regardless of which computer (IP address) sent those packets and which computer (IP address) will receive those packets.</span></span>

9.  <span data-ttu-id="b15dc-139">Dans la page 4, sélectionnez **TCP et UDP** dans la liste déroulante **Sélectionner le protocole que cette stratégie de QoS applique à** .</span><span class="sxs-lookup"><span data-stu-id="b15dc-139">On page four, select **TCP and UDP** from the **Select the protocol this QoS policy applies to** dropdown list.</span></span> <span data-ttu-id="b15dc-140">TCP (Transmission Control Protocol) et UDP (User Datagram Protocol) sont les deux protocoles réseau les plus fréquemment utilisés par Lync Server et ses applications clientes.</span><span class="sxs-lookup"><span data-stu-id="b15dc-140">TCP (Transmission Control Protocol) and UDP (User Datagram Protocol) are the two networking protocols most-commonly used by Lync Server and its client applications.</span></span>

10. <span data-ttu-id="b15dc-141">Sous le titre **Spécifiez le numéro de port source**, sélectionnez **à partir de ce port ou plage de sources**.</span><span class="sxs-lookup"><span data-stu-id="b15dc-141">Under the heading **Specify the source port number**, select **From this source port or range**.</span></span> <span data-ttu-id="b15dc-142">Dans la zone texte de l’accompagnement, tapez la plage de ports réservée aux transmissions audio.</span><span class="sxs-lookup"><span data-stu-id="b15dc-142">In the accompanying text box, type the port range reserved for audio transmissions.</span></span> <span data-ttu-id="b15dc-143">Par exemple, si vous avez réservé ports 50020 via ports 50039 pour le trafic audio, entrez la plage de ports à l’aide du format suivant : **50020:50039**.</span><span class="sxs-lookup"><span data-stu-id="b15dc-143">For example, if you reserved ports 50020 through ports 50039 for audio traffic enter the port range using this format: **50020:50039**.</span></span> <span data-ttu-id="b15dc-144">Cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="b15dc-144">Click **Finish**.</span></span>

<span data-ttu-id="b15dc-145">Une fois que vous avez créé la stratégie QoS pour le son, vous devez créer une deuxième stratégie pour la vidéo.</span><span class="sxs-lookup"><span data-stu-id="b15dc-145">After you have created the QoS policy for audio you should then create a second policy for video.</span></span> <span data-ttu-id="b15dc-146">Pour créer une stratégie pour la vidéo, suivez la même procédure que celle que vous avez suivie lors de la création de la stratégie audio, en effectuant les substitutions suivantes :</span><span class="sxs-lookup"><span data-stu-id="b15dc-146">To create a policy for video, follow the same basic procedure you followed when creating the audio policy, making these substitutions:</span></span>

  - <span data-ttu-id="b15dc-147">Utilisez un nom de stratégie différent (et unique) (par exemple, **vidéo Lync**).</span><span class="sxs-lookup"><span data-stu-id="b15dc-147">Use a different (and unique) policy name (for example, **Lync Video**).</span></span>

  - <span data-ttu-id="b15dc-148">Définissez la valeur DSCP sur **34** au lieu de 46.</span><span class="sxs-lookup"><span data-stu-id="b15dc-148">Set the DSCP value to **34** instead of 46.</span></span> <span data-ttu-id="b15dc-149">(Comme indiqué précédemment, vous n’avez pas besoin d’utiliser la valeur DSCP 34 ; il vous suffit d’affecter une valeur DSCP différente de celle utilisée pour l’audio.)</span><span class="sxs-lookup"><span data-stu-id="b15dc-149">(As noted previously, you do not have to use the DSCP value 34; you simply must assign a different DSCP value than the one used for audio.)</span></span>

  - <span data-ttu-id="b15dc-150">Utilisez la plage de ports déjà configurée pour le trafic vidéo.</span><span class="sxs-lookup"><span data-stu-id="b15dc-150">Use the previously-configured port range for video traffic.</span></span> <span data-ttu-id="b15dc-151">Par exemple, si vous avez réservé ports 58000 à 58019 pour la vidéo, définissez la plage de ports comme suit : **58000:58019**.</span><span class="sxs-lookup"><span data-stu-id="b15dc-151">For example, if you have reserved ports 58000 through 58019 for video, then set the port range to this: **58000:58019**.</span></span>

<span data-ttu-id="b15dc-152">Si vous décidez de créer une stratégie pour gérer le trafic de partage d’application, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="b15dc-152">If you decide to create a policy for managing application sharing traffic make these substitutions:</span></span>

  - <span data-ttu-id="b15dc-153">Utilisez un nom de stratégie différent (et unique) (par exemple, le **partage d’applications serveur Lync**).</span><span class="sxs-lookup"><span data-stu-id="b15dc-153">Use a different (and unique) policy name (for example, **Lync Server Application Sharing**).</span></span>

  - <span data-ttu-id="b15dc-154">Définissez la valeur DSCP sur **24** au lieu de 46.</span><span class="sxs-lookup"><span data-stu-id="b15dc-154">Set the DSCP value to **24** instead of 46.</span></span> <span data-ttu-id="b15dc-155">(De nouveau, cette valeur ne doit pas être de 24 ; il doit simplement être différent des valeurs DSCP utilisées pour l’audio et la vidéo.)</span><span class="sxs-lookup"><span data-stu-id="b15dc-155">(Again, this value does not have to be 24; it simply must be different than the DSCP values used for audio and for video.)</span></span>

  - <span data-ttu-id="b15dc-156">Utilisez la plage de ports déjà configurée pour le trafic vidéo.</span><span class="sxs-lookup"><span data-stu-id="b15dc-156">Use the previously-configured port range for video traffic.</span></span> <span data-ttu-id="b15dc-157">Par exemple, si vous avez réservé ports 42000 à 42019 pour le partage d’application, définissez l’intervalle de ports comme suit : **42000:42019**.</span><span class="sxs-lookup"><span data-stu-id="b15dc-157">For example, if you have reserved ports 42000 through 42019 for application sharing, then set the port range to this: **42000:42019**.</span></span>

<span data-ttu-id="b15dc-158">Pour une stratégie de transfert de fichiers :</span><span class="sxs-lookup"><span data-stu-id="b15dc-158">For a file transfer policy:</span></span>

  - <span data-ttu-id="b15dc-159">Utilisez un nom de stratégie différent (et unique) (par exemple, **transferts de fichiers Lync Server**).</span><span class="sxs-lookup"><span data-stu-id="b15dc-159">Use a different (and unique) policy name (for example, **Lync Server File Transfers**).</span></span>

  - <span data-ttu-id="b15dc-160">Définissez la valeur DSCP sur **14**.</span><span class="sxs-lookup"><span data-stu-id="b15dc-160">Set the DSCP value to **14**.</span></span> <span data-ttu-id="b15dc-161">(De nouveau, cette valeur ne doit pas être 14 ; il doit simplement s’agir d’un code DSCP unique.)</span><span class="sxs-lookup"><span data-stu-id="b15dc-161">(Again, this value does not have to be 14; it simply must be a unique DSCP code.)</span></span>

  - <span data-ttu-id="b15dc-162">Utilisez la plage de ports déjà configurée pour l’application.</span><span class="sxs-lookup"><span data-stu-id="b15dc-162">Use the previously-configured port range for application.</span></span> <span data-ttu-id="b15dc-163">Par exemple, si vous avez réservé ports 42020 à 42039 pour le partage d’application, définissez l’intervalle de ports comme suit : **42020:42039**.</span><span class="sxs-lookup"><span data-stu-id="b15dc-163">For example, if you have reserved ports 42020 through 42039 for application sharing, then set the port range to this: **42020:42039**.</span></span>

<span data-ttu-id="b15dc-164">Les nouvelles stratégies que vous avez créées ne sont pas prises en compte tant que la stratégie de groupe n’a pas été actualisée sur les ordinateurs clients.</span><span class="sxs-lookup"><span data-stu-id="b15dc-164">The new policies you have created will not take effect until Group Policy has been refreshed on your client computers.</span></span> <span data-ttu-id="b15dc-165">Bien que la stratégie de groupe s’actualise périodiquement, vous pouvez forcer une actualisation immédiate en exécutant la commande suivante sur chaque ordinateur dans lequel la stratégie de groupe doit être actualisée :</span><span class="sxs-lookup"><span data-stu-id="b15dc-165">Although Group Policy periodically refreshes on its own, you can force an immediate refresh by running the following command on each computer where Group Policy needs to be refreshed:</span></span>

    Gpudate.exe /force

<span data-ttu-id="b15dc-166">Vous pouvez exécuter cette commande à partir de n’importe quelle fenêtre de commande exécutée sous informations d’identification d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="b15dc-166">This command can be run from any command window that is running under administrator credentials.</span></span> <span data-ttu-id="b15dc-167">Pour exécuter une fenêtre de commande sous informations d’identification d’administrateur, cliquez sur **Démarrer**, cliquez avec le bouton droit sur **invite de commandes**, puis cliquez sur **exécuter en tant qu’administrateur**.</span><span class="sxs-lookup"><span data-stu-id="b15dc-167">To run a command window under administrator credentials, click **Start**, right-click **Command Prompt**, and then click **Run as administrator**.</span></span>

<span data-ttu-id="b15dc-168">Gardez à l’esprit que ces stratégies doivent être ciblées vers les ordinateurs clients.</span><span class="sxs-lookup"><span data-stu-id="b15dc-168">Keep in mind that these policies should be targeted towards your client computers.</span></span> <span data-ttu-id="b15dc-169">Ils ne doivent pas être appliqués aux serveurs exécutant Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b15dc-169">They should not be applied to servers running Lync Server.</span></span>

<span data-ttu-id="b15dc-170">Pour vous assurer que les paquets réseau sont marqués avec la valeur DSCP appropriée, vous devez également créer une nouvelle entrée de Registre sur chaque ordinateur en suivant la procédure suivante :</span><span class="sxs-lookup"><span data-stu-id="b15dc-170">To help ensure that network packets are marked with the appropriate DSCP value, you should also create a new registry entry on each computer by completing the following procedure:</span></span>

1.  <span data-ttu-id="b15dc-171">Cliquez sur **Démarrer** , puis sur **exécuter**.</span><span class="sxs-lookup"><span data-stu-id="b15dc-171">Click **Start** and then click **Run**.</span></span>

2.  <span data-ttu-id="b15dc-172">Dans la boîte de dialogue **exécuter** , tapez **regedit** , puis appuyez sur entrée.</span><span class="sxs-lookup"><span data-stu-id="b15dc-172">In the **Run** dialog box, type **regedit** and then press ENTER.</span></span>

3.  <span data-ttu-id="b15dc-173">Dans l’éditeur du Registre, développez l' **\_ \_ ordinateur local HKEY**, développez **système**, **CurrentControlSet**, développez **services**, puis cliquez sur **tcpip**.</span><span class="sxs-lookup"><span data-stu-id="b15dc-173">In the Registry Editor, expand **HKEY\_LOCAL\_MACHINE**, expand **SYSTEM**, expand **CurrentControlSet**, expand **services**, and then expand **Tcpip**.</span></span>

4.  <span data-ttu-id="b15dc-174">Cliquez avec le bouton droit sur **tcpip**, pointez sur **nouveau**, puis cliquez sur **clé**.</span><span class="sxs-lookup"><span data-stu-id="b15dc-174">Right-click **Tcpip**, point to **New**, and then click **Key**.</span></span> <span data-ttu-id="b15dc-175">Une fois la nouvelle clé de Registre créée, tapez **QoS** , puis appuyez sur entrée pour renommer la clé.</span><span class="sxs-lookup"><span data-stu-id="b15dc-175">After the new registry key is created, type **QoS** and then press ENTER to rename the key.</span></span>

5.  <span data-ttu-id="b15dc-176">Cliquez avec le bouton droit sur **QoS**, pointez sur **nouveau**, puis cliquez sur **valeur de chaîne**.</span><span class="sxs-lookup"><span data-stu-id="b15dc-176">Right-click **QoS**, point to **New**, and then click **String Value**.</span></span> <span data-ttu-id="b15dc-177">Après la création de la nouvelle valeur du Registre, tapez **ne pas utiliser NLA** , puis appuyez sur entrée pour renommer la valeur.</span><span class="sxs-lookup"><span data-stu-id="b15dc-177">After the new registry value is created, type **Do not use NLA** and then press ENTER to rename the value.</span></span>

6.  <span data-ttu-id="b15dc-178">Double-cliquez sur **ne pas utiliser NLA**.</span><span class="sxs-lookup"><span data-stu-id="b15dc-178">Double-click **Do not use NLA**.</span></span> <span data-ttu-id="b15dc-179">Dans la boîte de dialogue modification de la **chaîne** , tapez **1** dans la zone données de la **valeur** , puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="b15dc-179">In the **Edit String** dialog box, type **1** in the **Value data** box and then click **OK**.</span></span>

7.  <span data-ttu-id="b15dc-180">Fermez l’éditeur du Registre, puis redémarrez votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="b15dc-180">Close the Registry Editor and then reboot your computer.</span></span>

<div>

## <a name="configuring-quality-of-service-on-computers-with-multiple-network-adapters"></a><span data-ttu-id="b15dc-181">Configuration de la qualité de service sur des ordinateurs dotés de plusieurs cartes réseau</span><span class="sxs-lookup"><span data-stu-id="b15dc-181">Configuring Quality of Service on Computers with Multiple Network Adapters</span></span>

<span data-ttu-id="b15dc-182">Si vous disposez d’un ordinateur doté de plusieurs cartes réseau, vous risquez de rencontrer des problèmes pour lesquels les valeurs DSCP apparaissent sous la forme de 0x00 au lieu de la valeur configurée.</span><span class="sxs-lookup"><span data-stu-id="b15dc-182">If you have a computer that has multiple network adapters you might occasionally run into issues where DSCP values are shown as 0x00 rather than the configured value.</span></span> <span data-ttu-id="b15dc-183">Cela se produit généralement sur les ordinateurs sur lesquels une ou plusieurs des cartes réseau ne sont pas en mesure d’accéder à votre domaine Active Directory (par exemple, si ces cartes sont utilisées pour un réseau privé).</span><span class="sxs-lookup"><span data-stu-id="b15dc-183">This will typically occur on computers where one or more of the network adapters are not able to access your Active Directory domain (for example, if these adapters are used for a private network).</span></span> <span data-ttu-id="b15dc-184">Dans les cas similaires, les valeurs DSCP seront balisées pour les adaptateurs qui peuvent accéder au domaine, mais ne seront pas balisés pour les cartes qui ne peuvent pas accéder au domaine.</span><span class="sxs-lookup"><span data-stu-id="b15dc-184">In cases like that, DSCP values will be tagged for the adapters that can access the domain, but will not be tagged for adapters that cannot access the domain.</span></span>

<span data-ttu-id="b15dc-185">Si vous souhaitez baliser les valeurs DSCP pour toutes les cartes réseau d’un ordinateur, y compris les cartes qui n’ont pas accès à votre domaine, vous devez ajouter et configurer une valeur dans le registre.</span><span class="sxs-lookup"><span data-stu-id="b15dc-185">If you would like to tag DSCP values for all the network adapters in a computer, including adapters that do not have access to your domain, then you will need to add and configure a value to the registry.</span></span> <span data-ttu-id="b15dc-186">Pour cela, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="b15dc-186">That can be done by completing the following procedure:</span></span>

1.  <span data-ttu-id="b15dc-187">Cliquez sur **Démarrer** , puis sur **exécuter**.</span><span class="sxs-lookup"><span data-stu-id="b15dc-187">Click **Start** and then click **Run**.</span></span>

2.  <span data-ttu-id="b15dc-188">Dans la boîte de dialogue **exécuter** , tapez **regedit** , puis appuyez sur entrée.</span><span class="sxs-lookup"><span data-stu-id="b15dc-188">In the **Run** dialog box, type **regedit** and then press ENTER.</span></span>

3.  <span data-ttu-id="b15dc-189">Dans l’éditeur du Registre, développez l' **\_ \_ ordinateur local HKEY**, développez **système**, **CurrentControlSet**, développez **services**, puis cliquez sur **tcpip**.</span><span class="sxs-lookup"><span data-stu-id="b15dc-189">In the Registry Editor, expand **HKEY\_LOCAL\_MACHINE**, expand **SYSTEM**, expand **CurrentControlSet**, expand **services**, and then expand **Tcpip**.</span></span>

4.  <span data-ttu-id="b15dc-190">Si vous ne voyez pas de clé de registre intitulée **QoS** , cliquez avec le bouton droit sur **tcpip**, pointez sur **nouveau**, puis cliquez sur **clé**.</span><span class="sxs-lookup"><span data-stu-id="b15dc-190">If you do not see a registry key labeled **QoS** then right-click **Tcpip**, point to **New**, and then click **Key**.</span></span> <span data-ttu-id="b15dc-191">Une fois la nouvelle clé créée, tapez **QoS** , puis appuyez sur entrée pour renommer la clé.</span><span class="sxs-lookup"><span data-stu-id="b15dc-191">After the new key is created, type **QoS** and then press ENTER to rename the key.</span></span>

5.  <span data-ttu-id="b15dc-192">Cliquez avec le bouton droit sur **QoS**, pointez sur **nouveau**, puis cliquez sur **valeur de chaîne**.</span><span class="sxs-lookup"><span data-stu-id="b15dc-192">Right-click **QoS**, point to **New**, and then click **String Value**.</span></span> <span data-ttu-id="b15dc-193">Après la création de la nouvelle valeur du Registre, tapez **ne pas utiliser NLA** , puis appuyez sur entrée pour renommer la valeur.</span><span class="sxs-lookup"><span data-stu-id="b15dc-193">After the new registry value is created, type **Do not use NLA** and then press ENTER to rename the value.</span></span>

6.  <span data-ttu-id="b15dc-194">Double-cliquez sur **ne pas utiliser NLA**.</span><span class="sxs-lookup"><span data-stu-id="b15dc-194">Double-click **Do not use NLA**.</span></span> <span data-ttu-id="b15dc-195">Dans la boîte de dialogue modification de la **chaîne** , tapez **1** dans la zone données de la **valeur** , puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="b15dc-195">In the **Edit String** dialog box, type **1** in the **Value data** box and then click **OK**.</span></span>

<span data-ttu-id="b15dc-196">Après avoir créé et configuré la nouvelle valeur de Registre, vous devez redémarrer votre ordinateur pour que les modifications soient prises en compte.</span><span class="sxs-lookup"><span data-stu-id="b15dc-196">After creating and configuring the new registry value you will need to reboot your computer in order for the changes to take effect.</span></span>

<span data-ttu-id="b15dc-197"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b15dc-197"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

