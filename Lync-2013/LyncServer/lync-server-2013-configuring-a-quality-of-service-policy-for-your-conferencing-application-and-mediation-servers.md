---
title: 'Lync Server 2013 : Configuration d’une stratégie de qualité de service pour les serveurs de conférence, d’application et de médiation'
description: 'Lync Server 2013 : configuration d’une stratégie de qualité de service pour vos serveurs de conférence, d’application et de médiation.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring a Quality of Service policy for your Conferencing, Application, and Mediation servers
ms:assetid: 8adcbbc5-c9f5-476d-ab7f-72e61859cacf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205076(v=OCS.15)
ms:contentKeyID: 48184769
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0ee82c5f1f6b3025c4052b7e27c1013e0624b756
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433485"
---
# <a name="configuring-a-quality-of-service-policy-in-lync-server-2013-for-your-conferencing-application-and-mediation-servers"></a><span data-ttu-id="4c372-103">Configuration d’une stratégie de qualité de service dans Lync Server 2013 pour les serveurs de conférence, d’application et de médiation</span><span class="sxs-lookup"><span data-stu-id="4c372-103">Configuring a Quality of Service policy in Lync Server 2013 for your Conferencing, Application, and Mediation servers</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4c372-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4c372-104">

<span> </span></span></span>

<span data-ttu-id="4c372-105">_**Dernière modification de la rubrique :** 2014-06-23_</span><span class="sxs-lookup"><span data-stu-id="4c372-105">_**Topic Last Modified:** 2014-06-23_</span></span>

<span data-ttu-id="4c372-106">La configuration de plages de ports facilite l’utilisation de la qualité de service en s’assurant que tout le trafic d’un type spécifique (par exemple, tout le trafic audio) est acheminé par le même ensemble de ports.</span><span class="sxs-lookup"><span data-stu-id="4c372-106">Configuring port ranges facilitates the use of Quality of Service by ensuring that all traffic of a specified type (for example, all audio traffic) travels through the same set of ports.</span></span> <span data-ttu-id="4c372-107">Ainsi, le système peut facilement identifier et marquer un paquet donné : si le port 49152 est réservé au trafic audio, tout paquet transmis via le port 49152 peut être marqué avec un code DSCP indiquant qu’il s’agit d’un paquet audio.</span><span class="sxs-lookup"><span data-stu-id="4c372-107">This makes it easy for the system to identify and mark a given packet: if port 49152 is reserved for audio traffic, then any packet traveling through port 49152 can be marked with a DSCP code that indicates that this is an audio packet.</span></span> <span data-ttu-id="4c372-108">Cela permet aux routeurs d’identifier le paquet en tant que paquet audio et de lui attribuer une priorité plus élevée que les paquets non marqués (par exemple, les paquets utilisés pour copier un fichier d’un serveur vers un autre).</span><span class="sxs-lookup"><span data-stu-id="4c372-108">In turn, this enables routers to identify the packet as an audio packet, and give it higher priority than unmarked packets (such as packets used to copy a file from one server to another).</span></span>

<span data-ttu-id="4c372-109">En revanche, le simple fait de limiter un ensemble de ports à un type spécifique de trafic n’entraîne pas le passage de paquets avec le code DSCP approprié.</span><span class="sxs-lookup"><span data-stu-id="4c372-109">However, simply restricting a set of ports to a specific type of traffic does not result in packets traveling through those ports being marked with the appropriate DSCP code.</span></span> <span data-ttu-id="4c372-110">En plus de définir des plages de ports, vous devez également créer des politiques de qualité de service qui spécifient le code DSCP à associer à chaque plage de ports.</span><span class="sxs-lookup"><span data-stu-id="4c372-110">In addition to defining port ranges you must also create Quality of Service policies that specify the DSCP code to be associated with each port range.</span></span> <span data-ttu-id="4c372-111">Pour Microsoft Lync Server 2013, il s’agit généralement de créer deux stratégies : une pour le son et une pour la vidéo.</span><span class="sxs-lookup"><span data-stu-id="4c372-111">For Microsoft Lync Server 2013 that typically means creating two policies: one for audio and one for video.</span></span>

<span data-ttu-id="4c372-112">Les stratégies de qualité de service sont plus faciles à créer et à gérer via une stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="4c372-112">Quality of Service policies are most-easily created, and managed, by using Group Policy.</span></span> <span data-ttu-id="4c372-113">(Ces mêmes stratégies peuvent également être créées à l’aide de stratégies de sécurité locales.</span><span class="sxs-lookup"><span data-stu-id="4c372-113">(These same policies can also be created by using local security policies.</span></span> <span data-ttu-id="4c372-114">Toutefois, vous devez répéter la même procédure sur chacun d’eux et sur tous les ordinateurs.) Votre ensemble initial de stratégies de QoS (une pour le son et l’autre pour la vidéo) ne doit être appliqué qu’aux ordinateurs Lync Server exécutant le serveur de conférence, le serveur d’applications et/ou les services de médiation Server.</span><span class="sxs-lookup"><span data-stu-id="4c372-114">However, that requires you to repeat the same procedure on each and every computer.) Your initial set of QoS policies (one for audio and one for video) should be applied only to Lync Server computers running the Conferencing server, Application server, and/or Mediation server services.</span></span> <span data-ttu-id="4c372-115">Si tous ces ordinateurs sont situés dans le même UO d’annuaire Active Directory, vous pouvez simplement affecter le nouvel objet de stratégie de groupe à cette unité d’organisation.</span><span class="sxs-lookup"><span data-stu-id="4c372-115">If all of these computers are located in the same Active Directory OU then you can simply assign the new Group Policy object (GPO) to that OU.</span></span> <span data-ttu-id="4c372-116">Vous pouvez également effectuer d’autres opérations pour cibler la nouvelle stratégie sur les ordinateurs spécifiques. par exemple, vous pouvez placer les ordinateurs appropriés dans un groupe de sécurité, puis utiliser le filtrage de la sécurité de la stratégie de groupe pour appliquer l’objet de stratégie de groupe à ce groupe de sécurité.</span><span class="sxs-lookup"><span data-stu-id="4c372-116">Alternatively, you can take other steps to target the new policy to the specified computers; for example, you can place the appropriate computers in a security group, then use Group Policy security filtering to apply the GPO just to that security group.</span></span>

<span data-ttu-id="4c372-117">Pour créer une stratégie de qualité de service pour la gestion du son, connectez-vous à un ordinateur sur lequel est installée la gestion des stratégies de groupe.</span><span class="sxs-lookup"><span data-stu-id="4c372-117">In order to create a Quality of Service policy for managing audio, log on to a computer where Group Policy Management has been installed.</span></span> <span data-ttu-id="4c372-118">Ouvrez gestion des stratégies de groupe (cliquez sur **Démarrer**, pointez sur **Outils d’administration**, cliquez sur **gestion des stratégies de groupe**), puis procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="4c372-118">Open Group Policy Management (click **Start**, point to **Administrative Tools**, and then click **Group Policy Management**) and then complete the following procedure:</span></span>

1.  <span data-ttu-id="4c372-119">Dans gestion des stratégies de groupe, recherchez le conteneur dans lequel la nouvelle stratégie doit être créée.</span><span class="sxs-lookup"><span data-stu-id="4c372-119">In Group Policy Management, locate the container where the new policy should be created.</span></span> <span data-ttu-id="4c372-120">Par exemple, si tous vos ordinateurs serveur Lync résident dans une unité d’organisation nommée Lync Server, la nouvelle stratégie doit être créée dans l’unité d’organisation Lync Server.</span><span class="sxs-lookup"><span data-stu-id="4c372-120">For example, if all your Lync Server computers are located in an OU named Lync Server then the new policy should be created in the Lync Server OU.</span></span>

2.  <span data-ttu-id="4c372-121">Cliquez avec le bouton droit sur le conteneur approprié, puis cliquez sur **créer un objet de stratégie de groupe dans ce domaine et associez-le ici**.</span><span class="sxs-lookup"><span data-stu-id="4c372-121">Right-click the appropriate container and then click **Create a GPO in this domain, and Link it here**.</span></span>

3.  <span data-ttu-id="4c372-122">Dans la boîte de dialogue **nouvel objet GPO** , tapez le nom du nouvel objet de stratégie de groupe dans la zone **nom** (par exemple, **Lync Server QoS**), puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c372-122">In the **New GPO** dialog box, type a name for the new Group Policy object in the **Name** box (for example, **Lync Server QoS**) and then click **OK**.</span></span>

4.  <span data-ttu-id="4c372-123">Cliquez avec le bouton droit sur la stratégie que vous venez de créer, puis cliquez sur **modifier**.</span><span class="sxs-lookup"><span data-stu-id="4c372-123">Right-click the newly-created policy and then click **Edit**.</span></span>

5.  <span data-ttu-id="4c372-124">Dans l’éditeur de gestion des stratégies de groupe, développez **Configuration ordinateur**, **stratégies**, développez **Paramètres Windows**, cliquez avec le bouton droit sur **QoS basée sur une stratégie**, puis cliquez sur **créer une nouvelle stratégie**.</span><span class="sxs-lookup"><span data-stu-id="4c372-124">In the Group Policy Management Editor, expand **Computer Configuration**, expand **Policies**, expand **Windows Settings**, right-click **Policy-based QoS**, and then click **Create new policy**.</span></span>

6.  <span data-ttu-id="4c372-125">Dans la boîte de dialogue **QoS basée** sur une stratégie, dans la page d’ouverture, tapez un nom pour la nouvelle stratégie (par exemple, **Lync Server QoS**) dans la zone **nom** .</span><span class="sxs-lookup"><span data-stu-id="4c372-125">In the **Policy-based QoS** dialog box, on the opening page, type a name for the new policy (e.g., **Lync Server QoS**) in the **Name** box.</span></span> <span data-ttu-id="4c372-126">Sélectionnez **spécifier la valeur DSCP** et définissez la valeur sur **46**.</span><span class="sxs-lookup"><span data-stu-id="4c372-126">Select **Specify DSCP Value** and set the value to **46**.</span></span> <span data-ttu-id="4c372-127">Laissez l’option **spécifier le taux de limitation en sortie** non sélectionnée, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="4c372-127">Leave **Specify Outbound Throttle Rate** unselected, and then click **Next**.</span></span>

7.  <span data-ttu-id="4c372-128">Dans la page suivante, assurez-vous que l’option **toutes les applications** est sélectionnée, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="4c372-128">On the next page, make sure that **All applications** is selected and then click **Next**.</span></span> <span data-ttu-id="4c372-129">Cela permet de s’assurer que toutes les applications correspondent aux paquets de la plage de ports spécifiée avec le code DSCP spécifié.</span><span class="sxs-lookup"><span data-stu-id="4c372-129">This simply ensures that all applications will match packets from the specified port range with the specified DSCP code.</span></span>

8.  <span data-ttu-id="4c372-130">Sur la troisième page, assurez-vous que toutes les **adresses IP source et adresse IP de destination** sont sélectionnées, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="4c372-130">On the third page, make sure that both **Any source IP address and Any destination IP address** are selected and then click **Next**.</span></span> <span data-ttu-id="4c372-131">Ces deux paramètres garantissent le fonctionnement de la gestion des paquets indépendamment de l’ordinateur (adresse IP) ayant envoyé ces paquets et de l’ordinateur (adresse IP) recevant ces paquets.</span><span class="sxs-lookup"><span data-stu-id="4c372-131">These two settings ensure that packets will be managed regardless of which computer (IP address) sent those packets and which computer (IP address) will receive those packets.</span></span>

9.  <span data-ttu-id="4c372-132">Dans la page 4, sélectionnez **TCP et UDP** dans la liste déroulante **Sélectionner le protocole que cette stratégie de QoS applique à** .</span><span class="sxs-lookup"><span data-stu-id="4c372-132">On page four, select **TCP and UDP** from the **Select the protocol this QoS policy applies to** dropdown list.</span></span> <span data-ttu-id="4c372-133">TCP (Transmission Control Protocol) et UDP (User Datagram Protocol) sont les deux protocoles réseau les plus fréquemment utilisés par Lync Server et ses applications clientes.</span><span class="sxs-lookup"><span data-stu-id="4c372-133">TCP (Transmission Control Protocol) and UDP (User Datagram Protocol) are the two networking protocols most-commonly used by Lync Server and its client applications.</span></span>

10. <span data-ttu-id="4c372-134">Sous le titre **Spécifiez le numéro de port source**, sélectionnez **à partir de ce port ou plage de sources**.</span><span class="sxs-lookup"><span data-stu-id="4c372-134">Under the heading **Specify the source port number**, select **From this source port or range**.</span></span> <span data-ttu-id="4c372-135">Dans la zone texte de l’accompagnement, tapez la plage de ports réservée aux transmissions audio.</span><span class="sxs-lookup"><span data-stu-id="4c372-135">In the accompanying text box, type the port range reserved for audio transmissions.</span></span> <span data-ttu-id="4c372-136">Par exemple, si vous avez réservé ports 49152 via ports 57500 pour le trafic audio, entrez la plage de ports à l’aide du format suivant : **49152:57500**.</span><span class="sxs-lookup"><span data-stu-id="4c372-136">For example, if you reserved ports 49152 through ports 57500 for audio traffic enter the port range using this format: **49152:57500**.</span></span> <span data-ttu-id="4c372-137">Cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="4c372-137">Click **Finish**.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="4c372-138">La valeur DSCP de 46 est légèrement arbitraire : bien que le DSCP 46 soit souvent utilisé pour marquer les paquets audio, vous ne devez pas utiliser DSCP 46 pour les communications audio.</span><span class="sxs-lookup"><span data-stu-id="4c372-138">The DSCP value of 46 is somewhat arbitrary: although DSCP 46 is often used for marking audio packets, you do not have to use DSCP 46 for audio communications.</span></span> <span data-ttu-id="4c372-139">Si vous avez déjà implémenté la qualité de service (QoS) et que vous utilisez un autre code DSCP pour l’audio (par exemple, DSCP 40), vous devez configurer votre stratégie de qualité de service pour utiliser ce code (c’est-à-dire 40 pour le son).</span><span class="sxs-lookup"><span data-stu-id="4c372-139">If you have already implemented QoS and you are using a different DSCP code for audio (for example, DSCP 40) then you should configure your Quality of Service policy to use that same code (i.e., 40 for audio).</span></span> <span data-ttu-id="4c372-140">Si vous implémentez actuellement la qualité de service, nous vous conseillons d’utiliser le DSCP 46 pour l’audio, car cette valeur est couramment utilisée pour marquer les paquets audio.</span><span class="sxs-lookup"><span data-stu-id="4c372-140">If you are just now implementing Quality of Service, then it is recommended that you use DSCP 46 for audio, simply because that value is commonly used to mark audio packets.</span></span>



</div>

<span data-ttu-id="4c372-141">Une fois que vous avez créé la stratégie de QoS pour le trafic audio, vous devez créer une deuxième stratégie pour le trafic vidéo (et éventuellement une troisième stratégie de gestion du trafic de partage d’application).</span><span class="sxs-lookup"><span data-stu-id="4c372-141">After you have created the QoS policy for audio traffic you should then create a second policy for video traffic (and, optionally, a third policy for managing application sharing traffic).</span></span> <span data-ttu-id="4c372-142">Pour créer une stratégie pour la vidéo, suivez la même procédure que celle que vous avez suivie lors de la création de la stratégie audio, en effectuant les substitutions suivantes :</span><span class="sxs-lookup"><span data-stu-id="4c372-142">To create a policy for video, follow the same basic procedure you followed when creating the audio policy, making these substitutions:</span></span>

  - <span data-ttu-id="4c372-143">Utilisez un nom de stratégie différent (et unique) (par exemple, **Lync Server Video**).</span><span class="sxs-lookup"><span data-stu-id="4c372-143">Use a different (and unique) policy name (for example, **Lync Server Video**).</span></span>

  - <span data-ttu-id="4c372-144">Définissez la valeur DSCP sur **34** au lieu de 46.</span><span class="sxs-lookup"><span data-stu-id="4c372-144">Set the DSCP value to **34** instead of 46.</span></span> <span data-ttu-id="4c372-145">(Notez que vous n’avez pas besoin d’utiliser une valeur DSCP de 34.</span><span class="sxs-lookup"><span data-stu-id="4c372-145">(Note that you do not have to use a DSCP value of 34.</span></span> <span data-ttu-id="4c372-146">La seule condition requise est d’utiliser une autre valeur DSCP pour la vidéo que celle utilisée pour l’audio.</span><span class="sxs-lookup"><span data-stu-id="4c372-146">The only requirement is that you use a different DSCP value for video than you used for audio.)</span></span>

  - <span data-ttu-id="4c372-147">Utilisez la plage de ports déjà configurée pour le trafic vidéo.</span><span class="sxs-lookup"><span data-stu-id="4c372-147">Use the previously-configured port range for video traffic.</span></span> <span data-ttu-id="4c372-148">Par exemple, si vous avez réservé ports 57501 à 65535 pour la vidéo, définissez la plage de ports comme suit : **57501:65535**.</span><span class="sxs-lookup"><span data-stu-id="4c372-148">For example, if you have reserved ports 57501 through 65535 for video, then set the port range to this: **57501:65535**.</span></span>

<span data-ttu-id="4c372-149">Si vous décidez de créer une stratégie de gestion du trafic de partage d’application, vous devez créer une troisième stratégie en effectuant les substitutions suivantes :</span><span class="sxs-lookup"><span data-stu-id="4c372-149">If you decide to create a policy for managing application sharing traffic you must create a third policy, making the following substitutions:</span></span>

  - <span data-ttu-id="4c372-150">Utilisez un nom de stratégie différent (et unique) (par exemple, le **partage d’applications serveur Lync**).</span><span class="sxs-lookup"><span data-stu-id="4c372-150">Use a different (and unique) policy name (for example, **Lync Server Application Sharing**).</span></span>

  - <span data-ttu-id="4c372-151">Définissez la valeur DSCP sur **24** au lieu de 46.</span><span class="sxs-lookup"><span data-stu-id="4c372-151">Set the DSCP value to **24** instead of 46.</span></span> <span data-ttu-id="4c372-152">(De nouveau, vous n’avez pas besoin d’utiliser une valeur DSCP de 24.</span><span class="sxs-lookup"><span data-stu-id="4c372-152">(Again, you do not have to use a DSCP value of 24.</span></span> <span data-ttu-id="4c372-153">La seule condition requise est d’utiliser une autre valeur DSCP pour le partage d’application que celle utilisée pour l’audio ou la vidéo.)</span><span class="sxs-lookup"><span data-stu-id="4c372-153">The only requirement is that you use a different DSCP value for application sharing than you used for audio or for video.)</span></span>

  - <span data-ttu-id="4c372-154">Utilisez la plage de ports déjà configurée pour le trafic vidéo.</span><span class="sxs-lookup"><span data-stu-id="4c372-154">Use the previously-configured port range for video traffic.</span></span> <span data-ttu-id="4c372-155">Par exemple, si vous avez réservé ports 40803 à 49151 pour le partage d’application, définissez l’intervalle de ports comme suit : **40803:49151**.</span><span class="sxs-lookup"><span data-stu-id="4c372-155">For example, if you have reserved ports 40803 through 49151 for application sharing, then set the port range to this: **40803:49151**.</span></span>

<span data-ttu-id="4c372-156">Les nouvelles stratégies que vous avez créées ne sont pas prises en compte tant que la stratégie de groupe n’a pas été actualisée sur vos ordinateurs serveur Lync.</span><span class="sxs-lookup"><span data-stu-id="4c372-156">The new policies you have created will not take effect until Group Policy has been refreshed on your Lync Server computers.</span></span> <span data-ttu-id="4c372-157">Bien que la stratégie de groupe s’actualise périodiquement, vous pouvez forcer une actualisation immédiate en exécutant la commande suivante sur chaque ordinateur dans lequel la stratégie de groupe doit être actualisée :</span><span class="sxs-lookup"><span data-stu-id="4c372-157">Although Group Policy periodically refreshes on its own, you can force an immediate refresh by running the following command on each computer where Group Policy needs to be refreshed:</span></span>

    Gpupdate.exe /force

<span data-ttu-id="4c372-158">Vous pouvez exécuter cette commande à partir de Lync Server Management Shell ou à partir de n’importe quelle fenêtre de commande qui s’exécute sous informations d’identification d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="4c372-158">This command can be run from within the Lync Server Management Shell or from any command window that is running under administrator credentials.</span></span> <span data-ttu-id="4c372-159">Pour exécuter une fenêtre de commande sous informations d’identification d’administrateur, cliquez sur **Démarrer**, cliquez avec le bouton droit sur **invite de commandes**, puis cliquez sur **exécuter en tant qu’administrateur**.</span><span class="sxs-lookup"><span data-stu-id="4c372-159">To run a command window under administrator credentials, click **Start**, right-click **Command Prompt**, and then click **Run as administrator**.</span></span>

<span data-ttu-id="4c372-160">Pour vérifier que les nouvelles stratégies de QoS sont appliquées, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="4c372-160">To verify that the new QoS policies have been applied, do the following:</span></span>

1.  <span data-ttu-id="4c372-161">Sur un ordinateur serveur Lync, cliquez sur **Démarrer** , puis sur **exécuter**.</span><span class="sxs-lookup"><span data-stu-id="4c372-161">On a Lync Server computer, click **Start** and then click **Run**.</span></span>

2.  <span data-ttu-id="4c372-162">Dans la boîte de dialogue **exécuter** , tapez **regedit** , puis appuyez sur entrée.</span><span class="sxs-lookup"><span data-stu-id="4c372-162">In the **Run** dialog box, type **regedit** and then press ENTER.</span></span>

3.  <span data-ttu-id="4c372-163">Dans l’éditeur du Registre, développez **ordinateur**, sur **HKEY \_ local \_ machine**, développez **logiciel**, développez **stratégies**, développez **Microsoft**, développez **Windows**, puis cliquez sur **QoS**.</span><span class="sxs-lookup"><span data-stu-id="4c372-163">In Registry Editor, expand **Computer**, expand **HKEY\_LOCAL\_MACHINE**, expand **SOFTWARE**, expand **Policies**, expand **Microsoft**, expand **Windows**, and then click **QoS**.</span></span> <span data-ttu-id="4c372-164">Sous **QoS** , vous devez voir les clés de Registre correspondant aux stratégies de QoS que vous venez de créer.</span><span class="sxs-lookup"><span data-stu-id="4c372-164">Under **QoS** you should see registry keys for each of the QoS policies you just created.</span></span> <span data-ttu-id="4c372-165">Par exemple, si vous avez créé deux nouvelles stratégies (l’une ayant pour nom QoS du serveur audio Lync Server et l’autre nommée QoS vidéo de Lync Server Video QoS), vous devez les entrées de Registre pour la qualité de service audio de Lync Server et la qualité QoS vidéo de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="4c372-165">For example, if you created two new policies (one named Lync Server Audio QoS and the other named Lync Server Video QoS) you should registry entries for Lync Server Audio QoS and Lync Server Video QoS.</span></span>

<span data-ttu-id="4c372-166">Pour vous assurer que les paquets réseau sont marqués avec la valeur DSCP appropriée, vous devez également créer une nouvelle entrée de Registre sur chaque ordinateur en suivant la procédure suivante :</span><span class="sxs-lookup"><span data-stu-id="4c372-166">To help ensure that network packets are marked with the appropriate DSCP value, you should also create a new registry entry on each computer by completing the following procedure:</span></span>

1.  <span data-ttu-id="4c372-167">Cliquez sur **Démarrer** , puis sur **exécuter**.</span><span class="sxs-lookup"><span data-stu-id="4c372-167">Click **Start** and then click **Run**.</span></span>

2.  <span data-ttu-id="4c372-168">Dans la boîte de dialogue **exécuter** , tapez **regedit** , puis appuyez sur entrée.</span><span class="sxs-lookup"><span data-stu-id="4c372-168">In the **Run** dialog box, type **regedit** and then press ENTER.</span></span>

3.  <span data-ttu-id="4c372-169">Dans l’éditeur du Registre, développez l' **\_ \_ ordinateur local HKEY**, développez **système**, **CurrentControlSet**, développez **services**, puis cliquez sur **tcpip**.</span><span class="sxs-lookup"><span data-stu-id="4c372-169">In the Registry Editor, expand **HKEY\_LOCAL\_MACHINE**, expand **SYSTEM**, expand **CurrentControlSet**, expand **services**, and then expand **Tcpip**.</span></span>

4.  <span data-ttu-id="4c372-170">Cliquez avec le bouton droit sur **tcpip**, pointez sur **nouveau**, puis cliquez sur **clé**.</span><span class="sxs-lookup"><span data-stu-id="4c372-170">Right-click **Tcpip**, point to **New**, and then click **Key**.</span></span> <span data-ttu-id="4c372-171">Une fois la nouvelle clé de Registre créée, tapez **QoS** , puis appuyez sur entrée pour renommer la clé.</span><span class="sxs-lookup"><span data-stu-id="4c372-171">After the new registry key is created, type **QoS** and then press ENTER to rename the key.</span></span>

5.  <span data-ttu-id="4c372-172">Cliquez avec le bouton droit sur **QoS**, pointez sur **nouveau**, puis cliquez sur **valeur de chaîne**.</span><span class="sxs-lookup"><span data-stu-id="4c372-172">Right-click **QoS**, point to **New**, and then click **String Value**.</span></span> <span data-ttu-id="4c372-173">Après la création de la nouvelle valeur du Registre, tapez **ne pas utiliser NLA** , puis appuyez sur entrée pour renommer la valeur.</span><span class="sxs-lookup"><span data-stu-id="4c372-173">After the new registry value is created, type **Do not use NLA** and then press ENTER to rename the value.</span></span>

6.  <span data-ttu-id="4c372-174">Double-cliquez sur **ne pas utiliser NLA**.</span><span class="sxs-lookup"><span data-stu-id="4c372-174">Double-click **Do not use NLA**.</span></span> <span data-ttu-id="4c372-175">Dans la boîte de dialogue modification de la **chaîne** , tapez **1** dans la zone données de la **valeur** , puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c372-175">In the **Edit String** dialog box, type **1** in the **Value data** box and then click **OK**.</span></span>

7.  <span data-ttu-id="4c372-176">Fermez l’éditeur du Registre, puis redémarrez votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="4c372-176">Close the Registry Editor and then reboot your computer.</span></span>

<span data-ttu-id="4c372-177"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4c372-177"></div>

<span> </span>

</div>

</div>

</span></span></div>

