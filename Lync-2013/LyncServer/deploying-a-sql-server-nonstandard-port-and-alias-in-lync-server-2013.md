---
title: Déploiement d’un port non standard et d’un alias SQL Server dans Lync Server 2013
description: Déploiement d’un port et d’un alias SQL Server non standard dans Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying a SQL Server nonstandard port and alias in Lync Server 2013
ms:assetid: 2da92c1f-250e-407a-8651-fb2aec76aeb0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn776290(v=OCS.15)
ms:contentKeyID: 62634609
ms.date: 09/17/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: da76db2b946a47e13fe3549d7184b0b12894a83a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394036"
---
# <a name="deploying-a-sql-server-nonstandard-port-and-alias-in-lync-server-2013"></a><span data-ttu-id="b18dd-103">Déploiement d’un port non standard et d’un alias SQL Server dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b18dd-103">Deploying a SQL Server nonstandard port and alias in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b18dd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b18dd-104">

<span> </span></span></span>

<span data-ttu-id="b18dd-105">_**Dernière modification de la rubrique :** 2015-09-16_</span><span class="sxs-lookup"><span data-stu-id="b18dd-105">_**Topic Last Modified:** 2015-09-16_</span></span>

<span data-ttu-id="b18dd-106">Microsoft Lync Server 2013 prend en charge l’utilisation d’un port et d’un alias non standard dans SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b18dd-106">Microsoft Lync Server 2013 supports using a non-standard port and alias in SQL Server.</span></span> <span data-ttu-id="b18dd-107">L’utilisation d’un port SQL Server non standard et d’un alias augmente la sécurité et crée un environnement plus flexible pour le déploiement Lync.</span><span class="sxs-lookup"><span data-stu-id="b18dd-107">Using a SQL Server non-standard port and an alias increases security and creates a more flexible environment for the Lync deployment.</span></span> <span data-ttu-id="b18dd-108">Ces étapes ne constituent qu’une seule étape de sécurisation correcte de votre environnement Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b18dd-108">These steps are only a single step in properly securing your Lync Server 2013 environment.</span></span> <span data-ttu-id="b18dd-109">Des étapes supplémentaires sont nécessaires pour réduire la surface d’attaque d’une implémentation 2013 de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b18dd-109">Additional steps should be taken to reduce the attack surface of a Lync Server 2013 implementation.</span></span>

<span data-ttu-id="b18dd-110">L’article suivant décrit les étapes nécessaires pour configurer un port et un alias SQL Server non standard dans Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b18dd-110">The following article describes the steps required to setup a SQL Server non-standard port and alias in Lync Server 2013.</span></span>

<div>

## <a name="deploying-a-sql-server-non-standard-port-and-alias-in-lync-server-2013"></a><span data-ttu-id="b18dd-111">Déploiement d’un port et d’un alias SQL Server non standard dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b18dd-111">Deploying a SQL Server Non-Standard Port and Alias in Lync Server 2013</span></span>

<span data-ttu-id="b18dd-112">Le générateur de topologie de Lync Server 2013 prend en charge l’utilisation d’un alias SQL Server comme nom de domaine complet au lieu du nom de domaine complet SQL Server réel lors de la configuration de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b18dd-112">Lync Server 2013 Topology Builder supports using a SQL Server alias as the Fully Qualified Domain Name (FQDN) instead of the actual SQL Server FQDN when configuring Lync Server 2013.</span></span> <span data-ttu-id="b18dd-113">Cela permet de masquer le nom de domaine complet SQL Server réel auprès d’un attaquant malveillant.</span><span class="sxs-lookup"><span data-stu-id="b18dd-113">This allows the actual SQL Server FQDN to be hidden from any malicious attacker.</span></span> <span data-ttu-id="b18dd-114">De plus, l’utilisation d’un port non standard masque le port réel de n’importe quel attaquant tentant d’attaquer la base de données sur le port 1433 standard, comme illustré dans la figure ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="b18dd-114">In addition, using a non-standard port obscures the actual port from any would be attacker attempting to attack the database on the standard port 1433, as shown in the following figure.</span></span>

<span data-ttu-id="b18dd-115">![Un pirate ne connaît pas le numéro de port à attaquer.](images/Dn776290.2f3923e0-2bdc-416b-a66b-bf56599eb14e(OCS.15).jpg "Un pirate ne connaît pas le numéro de port à attaquer.")</span><span class="sxs-lookup"><span data-stu-id="b18dd-115">![A hacker doesn't know the port number to attack.](images/Dn776290.2f3923e0-2bdc-416b-a66b-bf56599eb14e(OCS.15).jpg "A hacker doesn't know the port number to attack.")</span></span>

<span data-ttu-id="b18dd-116">Pour réussir à déterminer le port que Lync Server 2013 utilise pour communiquer avec SQL Server, l’attaquant doit analyser tous les ports pour obtenir les informations de port.</span><span class="sxs-lookup"><span data-stu-id="b18dd-116">In order to be successful in determining the port Lync Server 2013 is using to communicate with SQL Server, the attacker would need to scan all ports to obtain the port information.</span></span> <span data-ttu-id="b18dd-117">Une analyse de port par un attaquant augmente le risque que la sécurité puisse détecter et arrêter l’instruction.</span><span class="sxs-lookup"><span data-stu-id="b18dd-117">A port scan by an attacker increases the chances that security can detect and stop the instruction.</span></span> <span data-ttu-id="b18dd-118">Outre l’ajout d’une sécurité accrue avec un port non standard, vous pouvez également utiliser un alias SQL Server pour offrir une souplesse au déploiement.</span><span class="sxs-lookup"><span data-stu-id="b18dd-118">In addition to adding increased security with a non-standard port, you can also use a SQL Server alias to provide flexibility for the deployment.</span></span> <span data-ttu-id="b18dd-119">Cela est utile pour réduire les changements de configuration dans les situations dans lesquelles un changement de nom SQL Server est requis.</span><span class="sxs-lookup"><span data-stu-id="b18dd-119">This is valuable in order to reduce configuration changes in situations where a SQL Server name change is required.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="b18dd-120">SQL Server fournit deux méthodes de tolérance de panne (mise en miroir et mise en miroir).</span><span class="sxs-lookup"><span data-stu-id="b18dd-120">SQL Server provides two fault tolerance methods (Failover Clustering and Mirroring).</span></span> <span data-ttu-id="b18dd-121">Les méthodes de tolérance de panne SQL Server sont prises en charge à l’aide d’un port et d’un alias SQL Server non standard avec Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b18dd-121">Both SQL Server fault tolerance methods are supported using a SQL Server non-standard port and alias with Lync Server 2013.</span></span> <span data-ttu-id="b18dd-122">Si le serveur principal SQL Server utilisé par le pool est dans une configuration en miroir, le service de navigateur SQL sur les serveurs principaux SQL Server doit être en cours d’exécution pour les serveurs frontaux pour la connexion à la base de données en miroir lorsque les bases de données sont basculées vers le serveur SQL Server en miroir.</span><span class="sxs-lookup"><span data-stu-id="b18dd-122">If the SQL Server backend used by the pool is in a mirrored configuration, then the SQL browser service on the SQL Server backend servers should be running for Front End servers to connect to the mirrored database when the databases are failed over to the mirrored SQL Server.</span></span>



</div>

<span data-ttu-id="b18dd-123">Lors de la configuration de la connectivité de base de données SQL Server à partir du générateur de topologie, ou lors de l’utilisation de l’applet de connexion Install-CsDatabase, il n’est pas possible de définir explicitement un numéro de port SQL Server non standard et de l’associer à une instance SQL.</span><span class="sxs-lookup"><span data-stu-id="b18dd-123">When configuring SQL Server database connectivity from within Topology Builder, or when using the Install-CsDatabase cmdlet, it’s not possible to explicitly define a SQL Server non-standard port number and associate it with a SQL instance.</span></span> <span data-ttu-id="b18dd-124">Pour définir un port non standard, vous devez utiliser les utilitaires SQL Server et Windows Server.</span><span class="sxs-lookup"><span data-stu-id="b18dd-124">To set a non-standard port, you’ll need to use SQL Server and Windows Server utilities.</span></span>

<span data-ttu-id="b18dd-125">Pour configurer un port et un alias SQL Server non standard pour une utilisation avec Lync Server 2013, vous devez effectuer trois étapes principales.</span><span class="sxs-lookup"><span data-stu-id="b18dd-125">To set up a SQL Server non-standard port and alias for use with Lync Server 2013, you will need to complete three primary steps.</span></span> <span data-ttu-id="b18dd-126">Ces étapes sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="b18dd-126">These steps are:</span></span>

  - <span data-ttu-id="b18dd-127">Vérifiez que Lync Server 2013 dispose des dernières mises à jour.</span><span class="sxs-lookup"><span data-stu-id="b18dd-127">Confirm that Lync Server 2013 has the Latest Updates Applied.</span></span>

  - <span data-ttu-id="b18dd-128">Configurez le port et l’alias SQL Server non standard.</span><span class="sxs-lookup"><span data-stu-id="b18dd-128">Setup the SQL Server Non-Standard Port and Alias.</span></span>

  - <span data-ttu-id="b18dd-129">Configurer Lync Server 2013 avec l’alias SQL Server à l’aide du générateur de topologie.</span><span class="sxs-lookup"><span data-stu-id="b18dd-129">Configure Lync Server 2013 with the SQL Server alias using Topology Builder.</span></span>

  - <span data-ttu-id="b18dd-130">Publiez la topologie et vérifiez la base de données.</span><span class="sxs-lookup"><span data-stu-id="b18dd-130">Publish the Topology, and Verify the Database.</span></span>

<div>

## <a name="confirm-that-lync-server-2013-has-the-latest-updates-applied"></a><span data-ttu-id="b18dd-131">Vérifiez que Lync Server 2013 a installé les dernières mises à jour.</span><span class="sxs-lookup"><span data-stu-id="b18dd-131">Confirm that Lync Server 2013 has the Latest Updates Applied</span></span>

<span data-ttu-id="b18dd-132">Il est important de tenir à jour Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b18dd-132">It is important to keep Lync Server 2013 up to date.</span></span> <span data-ttu-id="b18dd-133">Pour rechercher les mises à jour les plus récentes et obtenir des informations sur la façon de les appliquer, voir [mises à jour de Lync Server 2013](https://support.microsoft.com/kb/2809243).</span><span class="sxs-lookup"><span data-stu-id="b18dd-133">To check for the most recent updates and information on how to apply them, see [Updates for Lync Server 2013](https://support.microsoft.com/kb/2809243).</span></span>

</div>

<div>

## <a name="setup-the-sql-server-non-standard-port-and-alias"></a><span data-ttu-id="b18dd-134">Configurer le port et l’alias SQL Server non standard</span><span class="sxs-lookup"><span data-stu-id="b18dd-134">Setup the SQL Server Non-Standard Port and Alias</span></span>

<span data-ttu-id="b18dd-135">Le port et l’alias SQL Server non standard doivent être définis sur l’instance de base de données avant d’être référencés à partir du générateur de topologie Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b18dd-135">The SQL Server non-standard port and alias must be set up on the database instance before it can be referenced from Lync Server 2013 Topology Builder.</span></span> <span data-ttu-id="b18dd-136">Pour configurer un port et un alias SQL Server non standard, vous devez effectuer trois étapes principales.</span><span class="sxs-lookup"><span data-stu-id="b18dd-136">To set up a SQL Server non-standard port and alias, you will have to complete three primary steps.</span></span> <span data-ttu-id="b18dd-137">Ces étapes sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="b18dd-137">These steps are as follows:</span></span>

  - <span data-ttu-id="b18dd-138">Changer les valeurs par défaut du protocole TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="b18dd-138">Change the Default TCP/IP Protocol Values.</span></span>

  - <span data-ttu-id="b18dd-139">Créez et configurez un alias SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b18dd-139">Create and Configure a SQL Server Alias.</span></span>

  - <span data-ttu-id="b18dd-140">Créer un enregistrement de ressource de nom canonique DNS (Domain Name System) (CNAMe).</span><span class="sxs-lookup"><span data-stu-id="b18dd-140">Create a Domain Name System (DNS) Canonical Name (CNAME) Resource Record.</span></span>

<span data-ttu-id="b18dd-141">**Modifier les valeurs par défaut du protocole TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="b18dd-141">**Modify the Default TCP/IP Protocol Values**</span></span>

1.  <span data-ttu-id="b18dd-142">Sélectionnez **Démarrer**, puis sélectionnez **Gestionnaire de configuration SQL Server**, comme illustré dans la figure ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="b18dd-142">Select **Start**, and choose **SQL Server Configuration Manager**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="b18dd-143">![Icône SQL Server Management Studio](images/Dn776290.6e811f27-cea9-4437-b44c-55bff013150f(OCS.15).png "Icône SQL Server Management Studio")</span><span class="sxs-lookup"><span data-stu-id="b18dd-143">![The SQL Server Management Studio icon](images/Dn776290.6e811f27-cea9-4437-b44c-55bff013150f(OCS.15).png "The SQL Server Management Studio icon")</span></span>

2.  <span data-ttu-id="b18dd-144">Dans le volet de navigation, sélectionnez l' **instance SQL** Server, choisissez de développer **configuration du réseau SQL Server**, puis sélectionnez **protocoles pour \<instance name\>**, comme illustré dans la figure ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="b18dd-144">In the navigation pane, choose to expand the **SQL Server instance**, choose to expand **SQL Server Network Configuration**, and choose **Protocols for \<instance name\>**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="b18dd-145">![Naviguer dans les propriétés TCP/IP](images/Dn776290.3d7a964c-f17e-47fd-8f0c-535453da7fad(OCS.15).jpg "Naviguer dans les propriétés TCP/IP")</span><span class="sxs-lookup"><span data-stu-id="b18dd-145">![Navigate to TCP/IP Properties](images/Dn776290.3d7a964c-f17e-47fd-8f0c-535453da7fad(OCS.15).jpg "Navigate to TCP/IP Properties")</span></span>

3.  <span data-ttu-id="b18dd-146">Dans le volet droit, cliquez avec le bouton droit sur **TCP/IP**, puis sélectionnez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="b18dd-146">In the right pane, right-click **TCP/IP**, and select **Properties**.</span></span> <span data-ttu-id="b18dd-147">La boîte de dialogue Propriétés TCP/IP s’affiche.</span><span class="sxs-lookup"><span data-stu-id="b18dd-147">The TCP/IP Properties dialog box is displayed.</span></span>

4.  <span data-ttu-id="b18dd-148">Sélectionnez l’onglet **adresses IP** . L’onglet adresses IP affiche toutes les adresses IP actives du serveur.</span><span class="sxs-lookup"><span data-stu-id="b18dd-148">Select the **IP Addresses** tab. The IP Addresses tab shows all of the active IP addresses on the server.</span></span> <span data-ttu-id="b18dd-149">Celles-ci sont au format IP1, IP2, jusqu’à IPAll, comme illustré dans la figure ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="b18dd-149">These are in the format IP1, IP2, up to IPAll, as shown in the following figure.</span></span>
    
    <span data-ttu-id="b18dd-150">![Ouvrir les propriétés TCP/IP.](images/Dn776290.ed2fd70d-1836-4ebf-80fe-09191d96585e(OCS.15).jpg "Ouvrir les propriétés TCP/IP.")</span><span class="sxs-lookup"><span data-stu-id="b18dd-150">![Open TCP/IP properties.](images/Dn776290.ed2fd70d-1836-4ebf-80fe-09191d96585e(OCS.15).jpg "Open TCP/IP properties.")</span></span>

5.  <span data-ttu-id="b18dd-151">Effacez le champ **TCP Dynamic ports** pour toutes les adresses IP.</span><span class="sxs-lookup"><span data-stu-id="b18dd-151">Clear the **TCP Dynamic Ports** field for all IP addresses.</span></span> <span data-ttu-id="b18dd-152">Si le champ contient un caractère zéro, cela signifie que SQL Server écoute sur les ports dynamiques.</span><span class="sxs-lookup"><span data-stu-id="b18dd-152">If the field contains a zero character, then it means SQL Server is listening on dynamic ports.</span></span> <span data-ttu-id="b18dd-153">Assurez-vous que ces champs sont effacés et ne contiennent pas de zéro.</span><span class="sxs-lookup"><span data-stu-id="b18dd-153">Make sure these fields are cleared and do not contain a zero.</span></span>

6.  <span data-ttu-id="b18dd-154">Pour l’adresse IP que Lync Server utilisera pour la connexion à la base de données, assurez-vous que l' **option activé** est définie sur **Oui**, comme illustré dans la figure ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="b18dd-154">For the IP address that Lync Server will be using to connect to the database, make sure that **Enabled** is set to **Yes**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="b18dd-155">![Définir Activé sur Oui pour l’adresse IP correcte.](images/Dn776290.7f818b91-0793-4594-8932-90447270fad9(OCS.15).jpg "Définir Activé sur Oui pour l’adresse IP correcte.")</span><span class="sxs-lookup"><span data-stu-id="b18dd-155">![Set enabled as Yes for the correct IP.](images/Dn776290.7f818b91-0793-4594-8932-90447270fad9(OCS.15).jpg "Set enabled as Yes for the correct IP.")</span></span>

7.  <span data-ttu-id="b18dd-156">Dans la section **IPAll** en bas de la boîte de dialogue, entrez le port souhaité dans le champ **port TCP** , comme illustré dans la figure ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="b18dd-156">In the **IPAll** section at the bottom of the dialog, enter the desired port in the **TCP Port** field, as shown in the following figure.</span></span> <span data-ttu-id="b18dd-157">Dans cet exemple, nous utilisons le port 50062, mais vous pouvez utiliser n’importe quel port entre 49152 et 65535.</span><span class="sxs-lookup"><span data-stu-id="b18dd-157">In this example, we use port 50062, but you can use any port between 49152 and 65535.</span></span> <span data-ttu-id="b18dd-158">Il s’agit des ports attribués à une utilisation dynamique et privée, ce qui évite tout conflit avec d’autres ports utilisés dans le déploiement de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b18dd-158">These are the ports assigned to dynamic and private use, and this ensures you won’t conflict with other ports being used in the Lync Server 2013 deployment.</span></span>
    
    <span data-ttu-id="b18dd-159">![Définir le port dans la section IPAll.](images/Dn776290.b5af53e2-7961-4664-b586-3ca8f3a17f06(OCS.15).jpg "Définir le port dans la section IPAll.")</span><span class="sxs-lookup"><span data-stu-id="b18dd-159">![Set port in IPAll section.](images/Dn776290.b5af53e2-7961-4664-b586-3ca8f3a17f06(OCS.15).jpg "Set port in IPAll section.")</span></span>

8.  <span data-ttu-id="b18dd-160">Cliquez sur **OK** pour quitter la boîte de dialogue Propriétés TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="b18dd-160">Choose **OK** to exit the TCP/IP Properties dialog.</span></span>

9.  <span data-ttu-id="b18dd-161">Redémarrez l’instance SQL Server en sélectionnant **services SQL Server** dans le volet gauche de la fenêtre Gestionnaire de configuration SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b18dd-161">Restart the SQL Server instance by selecting **SQL Server Services** in the left pane of SQL Server Configuration Manager.</span></span> <span data-ttu-id="b18dd-162">Ensuite, cliquez avec le bouton droit sur **SQL Server \<instance name\>** dans le volet droit, puis sélectionnez **redémarrer**, comme illustré dans la figure ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="b18dd-162">Then right-click **SQL Server \<instance name\>** in the right pane, and select **Restart**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="b18dd-163">![Réinitialiser le service SQL Server service pour l’instance.](images/Dn776290.a965c8cf-f769-4b52-bb38-c48a438cf491(OCS.15).jpg "Réinitialiser le service SQL Server service pour l’instance.")</span><span class="sxs-lookup"><span data-stu-id="b18dd-163">![Reset the SQL Server service for instance.](images/Dn776290.a965c8cf-f769-4b52-bb38-c48a438cf491(OCS.15).jpg "Reset the SQL Server service for instance.")</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="b18dd-164">Veillez à mettre à jour les paramètres de votre pare-feu pour qu’il s’adapte au nouveau port SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b18dd-164">Make sure you update your firewall settings to accommodate the new SQL Server port.</span></span>



</div>

<span data-ttu-id="b18dd-165">**Créer et configurer un alias SQL Server**</span><span class="sxs-lookup"><span data-stu-id="b18dd-165">**Create and Configure a SQL Server Alias**</span></span>

1.  <span data-ttu-id="b18dd-166">Sélectionnez **Démarrer**, puis sélectionnez **Gestionnaire de configuration SQL Server**, comme illustré dans la figure ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="b18dd-166">Select **Start**, and choose **SQL Server Configuration Manager**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="b18dd-167">![Icône SQL Server Management Studio](images/Dn776290.6e811f27-cea9-4437-b44c-55bff013150f(OCS.15).png "Icône SQL Server Management Studio")</span><span class="sxs-lookup"><span data-stu-id="b18dd-167">![The SQL Server Management Studio icon](images/Dn776290.6e811f27-cea9-4437-b44c-55bff013150f(OCS.15).png "The SQL Server Management Studio icon")</span></span>

2.  <span data-ttu-id="b18dd-168">Dans le volet gauche, choisissez d’étendre l' **instance SQL Server**, choisissez de développer **\<version\> configuration du client natif SQL**, puis sélectionnez **alias**, comme illustré dans la figure ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="b18dd-168">In the left pane, choose to expand **SQL Server instance**, choose to expand **SQL Native Client \<version\> Configuration**, and then choose **Aliases**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="b18dd-169">![Alias dans le gestionnaire de configuration SQL Server.](images/Dn776290.95341826-55d7-425f-ae19-d47d6668c5d8(OCS.15).jpg "Alias dans le gestionnaire de configuration SQL Server.")</span><span class="sxs-lookup"><span data-stu-id="b18dd-169">![Aliases in SQL Server Configuration Manager.](images/Dn776290.95341826-55d7-425f-ae19-d47d6668c5d8(OCS.15).jpg "Aliases in SQL Server Configuration Manager.")</span></span>

3.  <span data-ttu-id="b18dd-170">Cliquez avec le bouton droit sur **alias**, puis sélectionnez **nouveau pseudonyme..**..</span><span class="sxs-lookup"><span data-stu-id="b18dd-170">Right-click **Aliases**, and select **New Alias…**.</span></span>

4.  <span data-ttu-id="b18dd-171">Entrez le **nom** de l’alias, le **numéro de port**, le **protocole** et le **serveur**, comme illustré dans la figure ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="b18dd-171">Enter the **Alias Name**, **Port Number**, **Protocol**, and **Server**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="b18dd-172">![Création d’un alias](images/Dn776290.03653588-aecf-4fdd-b58a-95f5b372d478(OCS.15).jpg "Création d’un alias")</span><span class="sxs-lookup"><span data-stu-id="b18dd-172">![Creating a new alias](images/Dn776290.03653588-aecf-4fdd-b58a-95f5b372d478(OCS.15).jpg "Creating a new alias")</span></span>
    
    <div>
    

    > [!CAUTION]  
    > <span data-ttu-id="b18dd-173">Assurez-vous d’entrer le même port non standard utilisé lors de l’étape précédente, car il s’agit du port sur lequel SQL Server sera écouté.</span><span class="sxs-lookup"><span data-stu-id="b18dd-173">Make sure to enter the same non-standard port you used in the previous step since that is the port SQL Server will be listening on.</span></span> <span data-ttu-id="b18dd-174">S’il s’agit d’un alias configuré qui se connecte à un nom de domaine complet (FQDN) SQL Server incorrect, désactivez puis réactivez le protocole réseau associé.</span><span class="sxs-lookup"><span data-stu-id="b18dd-174">If a configured alias is connecting to the wrong SQL Server FQDN or Instance, disable and then re-enable the associated network protocol.</span></span> <span data-ttu-id="b18dd-175">Cette opération a pour effet d’effacer toutes les informations de connexion mises en cache et de permettre au client de se connecter correctement.</span><span class="sxs-lookup"><span data-stu-id="b18dd-175">Doing this clears any cached connection information and allows the client to connect correctly.</span></span>

    
    </div>

<span data-ttu-id="b18dd-176">**Créer un enregistrement de ressource CNAMe DNS**</span><span class="sxs-lookup"><span data-stu-id="b18dd-176">**Create a DNS CNAME Resource Record**</span></span>

1.  <span data-ttu-id="b18dd-177">Connectez-vous à l’ordinateur gestion du DNS.</span><span class="sxs-lookup"><span data-stu-id="b18dd-177">Sign into the computer managing DNS.</span></span>

2.  <span data-ttu-id="b18dd-178">Cliquez sur **Démarrer**, puis sélectionnez **Gestionnaire de serveur**, comme illustré dans la figure ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="b18dd-178">Select **Start**, and choose **Server Manager**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="b18dd-179">![Ouverture du gestionnaire de serveur](images/Dn776290.3e4bd8ad-2a65-4a05-af40-c8dd3583bc8f(OCS.15).jpg "Ouverture du gestionnaire de serveur")</span><span class="sxs-lookup"><span data-stu-id="b18dd-179">![Opening Server Manager](images/Dn776290.3e4bd8ad-2a65-4a05-af40-c8dd3583bc8f(OCS.15).jpg "Opening Server Manager")</span></span>

3.  <span data-ttu-id="b18dd-180">Sélectionnez la liste déroulante **Outils** et sélectionnez **DNS**, comme illustré dans la figure ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="b18dd-180">Choose the **Tools** drop-down, and select **DNS**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="b18dd-181">![Ouverture du DNS à partir du gestionnaire de serveur.](images/Dn776290.415e1da1-7c9a-4a4e-a896-ca34a76aaeff(OCS.15).jpg "Ouverture du DNS à partir du gestionnaire de serveur.")</span><span class="sxs-lookup"><span data-stu-id="b18dd-181">![Opening DNS from Server Manager.](images/Dn776290.415e1da1-7c9a-4a4e-a896-ca34a76aaeff(OCS.15).jpg "Opening DNS from Server Manager.")</span></span>

4.  <span data-ttu-id="b18dd-182">Dans le volet gauche, développez le nœud nom du serveur, développez le nœud zones de recherche directes, puis sélectionnez le domaine approprié.</span><span class="sxs-lookup"><span data-stu-id="b18dd-182">In the left pane, expand the server name node, expand the Forward Lookup Zones node, and choose the relevant domain.</span></span>

5.  <span data-ttu-id="b18dd-183">Cliquez avec le bouton droit sur le domaine, puis sélectionnez **nouveau pseudonyme (CNAME)...**, comme illustré dans la figure ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="b18dd-183">Right-click the domain, and select **New Alias (CNAME)…**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="b18dd-184">![Sélection de l’option de création d’un alias CNAMe](images/Dn776290.abe66cca-b53c-427a-9094-1a59dc6840ca(OCS.15).jpg "Sélection de l’option de création d’un alias CNAMe")</span><span class="sxs-lookup"><span data-stu-id="b18dd-184">![Selecting option to create a new alias CNAME](images/Dn776290.abe66cca-b53c-427a-9094-1a59dc6840ca(OCS.15).jpg "Selecting option to create a new alias CNAME")</span></span>

6.  <span data-ttu-id="b18dd-185">Entrez le **nom** de l’alias et le nom **de domaine complet (FQDN) de SQL Server**, comme illustré dans la figure ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="b18dd-185">Enter the **Alias Name** and the **FQDN for SQL Server**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="b18dd-186">![Remplissage de la boîte de dialogue nouveau pseudonyme CNAMe.](images/Dn776290.dd0ebd2d-3407-4459-8bd9-2b389a7bc440(OCS.15).jpg "Remplissage de la boîte de dialogue nouveau pseudonyme CNAMe.")</span><span class="sxs-lookup"><span data-stu-id="b18dd-186">![Filling in the new alias CNAME dialog.](images/Dn776290.dd0ebd2d-3407-4459-8bd9-2b389a7bc440(OCS.15).jpg "Filling in the new alias CNAME dialog.")</span></span>

7.  <span data-ttu-id="b18dd-187">Cliquez sur **OK** pour enregistrer le CNAME et l’afficher dans le Gestionnaire DNS.</span><span class="sxs-lookup"><span data-stu-id="b18dd-187">Choose **OK** to save the CNAME and view it in DNS Manager.</span></span>

</div>

<div>

## <a name="validate-database-connectivity"></a><span data-ttu-id="b18dd-188">Valider la connectivité de base de données</span><span class="sxs-lookup"><span data-stu-id="b18dd-188">Validate Database Connectivity</span></span>

<span data-ttu-id="b18dd-189">Il existe de nombreuses façons de vérifier qu’elle fonctionne.</span><span class="sxs-lookup"><span data-stu-id="b18dd-189">There are many different ways to make sure it is working.</span></span> <span data-ttu-id="b18dd-190">Vous voulez vous assurer que la base de données SQL Server écoute sur le port spécifié à l’aide de l’alias.</span><span class="sxs-lookup"><span data-stu-id="b18dd-190">You want to make sure that the SQL Server database is listening on the specified port using the alias.</span></span> <span data-ttu-id="b18dd-191">Une vérification rapide peut être effectuée à l’aide des commandes **netstat** et **Telnet** .</span><span class="sxs-lookup"><span data-stu-id="b18dd-191">A quick check can be completed using the **netstat** and **telnet** commands.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="b18dd-192">Le client Telnet est une fonctionnalité qui est fournie avec Windows Server, mais qui doit être installée.</span><span class="sxs-lookup"><span data-stu-id="b18dd-192">Telnet Client is a Feature that comes with Windows Server but that must be installed.</span></span> <span data-ttu-id="b18dd-193">Une fonctionnalité de serveur Windows peut être installée en ouvrant le gestionnaire de serveur et en sélectionnant Ajouter des rôles et des fonctionnalités dans le menu gérer.</span><span class="sxs-lookup"><span data-stu-id="b18dd-193">A Windows Server Feature can be installed by opening Server Manager and selecting Add Roles and Features from the Manage menu.</span></span>



</div>

<span data-ttu-id="b18dd-194">**Utiliser netstat et Telnet pour vérifier la connectivité de base de données**</span><span class="sxs-lookup"><span data-stu-id="b18dd-194">**Use netstat and telnet to verify database connectivity**</span></span>

1.  <span data-ttu-id="b18dd-195">Sélectionnez **Démarrer**, puis tapez **cmd** pour ouvrir une invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="b18dd-195">Select **Start**, and type **cmd** to open a command prompt.</span></span>

2.  <span data-ttu-id="b18dd-196">Tapez **netstat-a-f**, puis vérifiez que SQL Server s’exécute avec le port approprié, comme illustré dans la figure ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="b18dd-196">Type **netstat -a -f**, and confirm that SQL Server is running with the correct port, as shown in the following figure.</span></span>
    
    <span data-ttu-id="b18dd-197">![Utiliser netstat pour vérifier le port.](images/Dn776290.4ff3a1b2-c5eb-4496-8be7-374c351fa027(OCS.15).jpg "Utiliser netstat pour vérifier le port.")</span><span class="sxs-lookup"><span data-stu-id="b18dd-197">![Using netstat to verify port.](images/Dn776290.4ff3a1b2-c5eb-4496-8be7-374c351fa027(OCS.15).jpg "Using netstat to verify port.")</span></span>

3.  <span data-ttu-id="b18dd-198">Tapez **telnet \<alias name\> \<port \#\>** pour confirmer la connexion à l’instance SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b18dd-198">Type **telnet \<alias name\> \<port \#\>** to confirm the connection to the SQL Server instance.</span></span> <span data-ttu-id="b18dd-199">S’il s’agit d’une connexion réussie, Telnet se connecte et aucune erreur ne s’affiche.</span><span class="sxs-lookup"><span data-stu-id="b18dd-199">If the connection is successful, telnet will connect and you shouldn’t see an error.</span></span> <span data-ttu-id="b18dd-200">Cela montre que l’instance SQL Server écoute sur le port approprié avec l’alias approprié.</span><span class="sxs-lookup"><span data-stu-id="b18dd-200">This shows that the SQL Server instance is listening on the correct port with the correct alias.</span></span> <span data-ttu-id="b18dd-201">Si vous ne parvenez pas à vous connecter à la base de données SQL Server, Telnet affiche une erreur indiquant que la connexion ne peut pas être effectuée.</span><span class="sxs-lookup"><span data-stu-id="b18dd-201">If there’s a problem connecting to the SQL Server database, then telnet shows an error that the connection cannot be made.</span></span> <span data-ttu-id="b18dd-202">À présent que vous avez vérifié la connectivité de la base de données sur le serveur de base de données, vous pouvez effectuer la même opération sur Lync Server (sur le réseau) et vous assurer qu’aucun pare-feu ne bloque l’accès.</span><span class="sxs-lookup"><span data-stu-id="b18dd-202">Now that you have checked database connectivity on the database server, you can do the same thing from Lync Server (over the network) and make sure there aren’t any firewalls blocking access along the way.</span></span>

</div>

<div>

## <a name="conclusion"></a><span data-ttu-id="b18dd-203">Conclusion</span><span class="sxs-lookup"><span data-stu-id="b18dd-203">Conclusion</span></span>

<span data-ttu-id="b18dd-204">Une fois l’alias SQL Server configuré, vous pouvez l’utiliser pour créer une topologie Lync Server 2013 dans l’outil générateur de topologie.</span><span class="sxs-lookup"><span data-stu-id="b18dd-204">Once the SQL Server alias has been configured, you can use it to create a Lync Server 2013 topology in the Topology Builder tool.</span></span> <span data-ttu-id="b18dd-205">Pour plus d’informations sur les topologies, reportez-vous à [la rubrique définition et configuration de la topologie dans Lync Server 2013](lync-server-2013-defining-and-configuring-the-topology.md).</span><span class="sxs-lookup"><span data-stu-id="b18dd-205">For more information about topologies, see [Defining and configuring the topology in Lync Server 2013](lync-server-2013-defining-and-configuring-the-topology.md).</span></span>

</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="b18dd-206">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b18dd-206">See Also</span></span>


<span data-ttu-id="b18dd-207">[Microsoft Lync Server 2013](microsoft-lync-server-2013.md)  
 [Planification de la sécurité dans Lync Server 2013](lync-server-2013-planning-for-security.md)</span><span class="sxs-lookup"><span data-stu-id="b18dd-207">[Microsoft Lync Server 2013](microsoft-lync-server-2013.md) 
[Planning for security in Lync Server 2013](lync-server-2013-planning-for-security.md)</span></span>  
[<span data-ttu-id="b18dd-208">Définition et configuration de la topologie dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b18dd-208">Defining and configuring the topology in Lync Server 2013</span></span>](lync-server-2013-defining-and-configuring-the-topology.md)  
[<span data-ttu-id="b18dd-209">Déploiement de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b18dd-209">Deploying Lync Server 2013</span></span>](lync-server-2013-deploying-lync-server.md)  
  

<span data-ttu-id="b18dd-210"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b18dd-210"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

