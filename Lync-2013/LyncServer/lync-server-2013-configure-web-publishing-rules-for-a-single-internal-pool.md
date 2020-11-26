---
title: 'Lync Server 2013 : Configuration des règles de publication web pour un pool interne unique'
description: 'Lync Server 2013 : configurez les règles de publication Web pour un pool interne unique.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure web publishing rules for a single internal pool
ms:assetid: 86ff4b2a-1ba9-46a2-a175-8b19e00a49dd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429712(v=OCS.15)
ms:contentKeyID: 48184725
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 45015c90fdac92fb488affc871f2cfaf9d7506a2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433534"
---
# <a name="configure-web-publishing-rules-for-a-single-internal-pool-in-lync-server-2013"></a><span data-ttu-id="a8e27-103">Configuration des règles de publication web pour un pool interne unique dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a8e27-103">Configure web publishing rules for a single internal pool in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a8e27-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a8e27-104">

<span> </span></span></span>

<span data-ttu-id="a8e27-105">_**Dernière modification de la rubrique :** 2014-07-07_</span><span class="sxs-lookup"><span data-stu-id="a8e27-105">_**Topic Last Modified:** 2014-07-07_</span></span>

<span data-ttu-id="a8e27-106">Microsoft Forefront Threat Management Gateway 2010 et le routage de requête d’application Internet Information Server (IIS ARR) utilise des règles de publication Web pour publier les ressources internes, telles qu’une URL de réunion, pour les utilisateurs sur Internet.</span><span class="sxs-lookup"><span data-stu-id="a8e27-106">Microsoft Forefront Threat Management Gateway 2010 and Internet Information Server Application Request Routing (IIS ARR) uses web publishing rules to publish internal resources, such as a meeting URL, to users on the Internet.</span></span>

<span data-ttu-id="a8e27-107">Outre les URL des services Web pour les répertoires virtuels, vous devez également créer des règles de publication pour les URL simples, l’URL LyncDiscover et le serveur Office Web Apps.</span><span class="sxs-lookup"><span data-stu-id="a8e27-107">In addition to the Web Services URLs for the virtual directories, you must also create publishing rules for simple URLs, the LyncDiscover URL, and the Office Web Apps Server.</span></span> <span data-ttu-id="a8e27-108">Pour chaque URL simple, vous devez créer une règle individuelle sur le proxy inverse qui pointe vers cette URL simple.</span><span class="sxs-lookup"><span data-stu-id="a8e27-108">For each simple URL, you must create an individual rule on the reverse proxy that points to that simple URL.</span></span>

<span data-ttu-id="a8e27-109">Si vous déployez la mobilité et utilisez la découverte automatique, vous devez créer une règle de publication pour l’URL du service de découverte automatique externe.</span><span class="sxs-lookup"><span data-stu-id="a8e27-109">If you are deploying mobility and using automatic discovery, you need to create a publishing rule for the external Autodiscover Service URL.</span></span> <span data-ttu-id="a8e27-110">La découverte automatique nécessite également des règles de publication pour l’URL des services Web Lync Server externes pour votre pool de directeurs et votre pool frontal.</span><span class="sxs-lookup"><span data-stu-id="a8e27-110">Automatic discovery also requires publishing rules for the external Lync Server Web Services URL for your Director pool and Front End pool.</span></span> <span data-ttu-id="a8e27-111">Pour plus d’informations sur la création de règles de publication sur le Web pour la découverte automatique, voir [configuration du proxy inverse pour la mobilité dans Lync Server 2013](lync-server-2013-configuring-the-reverse-proxy-for-mobility.md).</span><span class="sxs-lookup"><span data-stu-id="a8e27-111">For details about creating the web publishing rules for automatic discovery, see [Configuring the reverse proxy for mobility in Lync Server 2013](lync-server-2013-configuring-the-reverse-proxy-for-mobility.md).</span></span>

<span data-ttu-id="a8e27-112">Utilisez les procédures suivantes pour créer des règles de publication Web.</span><span class="sxs-lookup"><span data-stu-id="a8e27-112">Use the following procedures to create web publishing rules.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a8e27-113">Ces procédures présupposent que vous avez installé l’édition standard de Forefront Threat Management Gateway (TMG) 2010 ou que vous avez installé et configuré Internet Information Server avec l’extension de routage de requête d’application (IIS ARR).</span><span class="sxs-lookup"><span data-stu-id="a8e27-113">These procedures assume that you have installed the Standard Edition of Forefront Threat Management Gateway (TMG) 2010 or have installed and configured Internet Information Server with the Application request Routing (IIS ARR) extension.</span></span> <span data-ttu-id="a8e27-114">Vous utilisez TMG ou IIS ARR.</span><span class="sxs-lookup"><span data-stu-id="a8e27-114">You use either TMG or IIS ARR.</span></span>



</div>

<div>

## <a name="to-create-a-web-server-publishing-rule-on-the-computer-running-tmg-2010"></a><span data-ttu-id="a8e27-115">Pour créer une règle de publication sur le serveur Web sur l’ordinateur exécutant TMG 2010</span><span class="sxs-lookup"><span data-stu-id="a8e27-115">To create a web server publishing rule on the computer running TMG 2010</span></span>

1.  <span data-ttu-id="a8e27-116">Cliquez sur **Démarrer**, cliquez sur **programmes**, sélectionnez **Microsoft Forefront TMG**, puis cliquez sur **gestion de Forefront TMG**.</span><span class="sxs-lookup"><span data-stu-id="a8e27-116">Click **Start**, select **Programs**, select **Microsoft Forefront TMG**, and then click **Forefront TMG Management**.</span></span>

2.  <span data-ttu-id="a8e27-117">Dans le volet gauche, développez **NomServeur**, cliquez avec le bouton droit sur **stratégie de pare-feu**, sélectionnez **nouveau**, puis cliquez sur règle de **publication de site Web**.</span><span class="sxs-lookup"><span data-stu-id="a8e27-117">In the left pane, expand **ServerName**, right-click **Firewall Policy**, select **New**, and then click **Web Site Publishing Rule**.</span></span>

3.  <span data-ttu-id="a8e27-118">Dans la page **Bienvenue dans la nouvelle règle de publication Web** , tapez un nom d’affichage pour la règle de publication (par exemple, LyncServerWebDownloadsRule).</span><span class="sxs-lookup"><span data-stu-id="a8e27-118">On the **Welcome to the New Web Publishing Rule** page, type a display name for the publishing rule (for example, LyncServerWebDownloadsRule).</span></span>

4.  <span data-ttu-id="a8e27-119">Dans la page **Sélectionner une action de règle** , sélectionnez **autoriser**.</span><span class="sxs-lookup"><span data-stu-id="a8e27-119">On the **Select Rule Action** page, select **Allow**.</span></span>

5.  <span data-ttu-id="a8e27-120">Dans la page **type de publication** , sélectionnez **publier un site Web ou un équilibrage de charge unique**.</span><span class="sxs-lookup"><span data-stu-id="a8e27-120">On the **Publishing Type** page, select **Publish a single Web site or load balancer**.</span></span>

6.  <span data-ttu-id="a8e27-121">Dans la page sécurité de la **connexion au serveur** , sélectionnez **utiliser SSL pour se connecter au serveur Web publié ou à la batterie de** serveurs.</span><span class="sxs-lookup"><span data-stu-id="a8e27-121">On the **Server Connection Security** page, select **Use SSL to connect to the published Web server or server farm**.</span></span>

7.  <span data-ttu-id="a8e27-122">Dans la page Détails de la **publication interne** , tapez le nom de domaine complet (FQDN) de la batterie de serveurs Web interne qui héberge le contenu de la réunion et le contenu de votre carnet d’adresses dans la zone **nom du site interne** .</span><span class="sxs-lookup"><span data-stu-id="a8e27-122">On the **Internal Publishing Details** page, type the fully qualified domain name (FQDN) of the internal web farm that hosts your meeting content and Address Book content in the **Internal Site name** box.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="a8e27-123">Si votre serveur interne est un serveur Standard Edition Server, il s’agit du nom de domaine complet Standard Edition Server.</span><span class="sxs-lookup"><span data-stu-id="a8e27-123">If your internal server is a Standard Edition server, this FQDN is the Standard Edition server FQDN.</span></span> <span data-ttu-id="a8e27-124">S’il s’agit d’un pool frontal, il s’agit d’une adresse IP virtuelle d’équilibrage de charge matérielle qui charge les serveurs internes de batteries de serveurs.</span><span class="sxs-lookup"><span data-stu-id="a8e27-124">If your internal server is a Front End pool, this FQDN is a hardware load balancer virtual IP (VIP) that load balances the internal web farm servers.</span></span> <span data-ttu-id="a8e27-125">Le serveur TMG doit être en mesure de résoudre le nom de domaine complet sur l’adresse IP du serveur Web interne.</span><span class="sxs-lookup"><span data-stu-id="a8e27-125">The TMG server must be able to resolve the FQDN to the IP address of the internal web server.</span></span> <span data-ttu-id="a8e27-126">Si le serveur TMG ne peut pas résoudre le nom de domaine complet (FQDN) en adresse IP appropriée, vous pouvez sélectionner <STRONG>utiliser un nom d’ordinateur ou une adresse IP pour vous connecter au serveur publié</STRONG>, puis, dans la zone nom de l' <STRONG>ordinateur ou</STRONG> <STRONG>adresse IP</STRONG> , tapez l’adresse IP du serveur Web interne.</span><span class="sxs-lookup"><span data-stu-id="a8e27-126">If the TMG server is not able to resolve the FQDN to the proper IP address, you can select <STRONG>Use a computer name or IP address to connect to the published server</STRONG>, and then in the <STRONG>Computer name or</STRONG> <STRONG>IP address</STRONG> box, type the IP address of the internal web server.</span></span> <span data-ttu-id="a8e27-127">Dans ce cas, vous devez vous assurer que le port 53 est ouvert sur le serveur TMG et qu’il peut accéder à un serveur DNS résidant sur le réseau de périmètre.</span><span class="sxs-lookup"><span data-stu-id="a8e27-127">If you do this, you must ensure that port 53 is open on the TMG server and that it can reach a DNS server that resides in the perimeter network.</span></span> <span data-ttu-id="a8e27-128">Vous pouvez également utiliser des entrées dans le fichier hosts local pour fournir une résolution de nom.</span><span class="sxs-lookup"><span data-stu-id="a8e27-128">You can also use entries in the local hosts file to provide name resolution.</span></span>

    
    </div>

8.  <span data-ttu-id="a8e27-129">Dans la page Détails de la **publication interne** , dans la zone **chemin (facultatif)** , tapez \* */\** _ en tant que chemin d’accès au dossier à publier.</span><span class="sxs-lookup"><span data-stu-id="a8e27-129">On the **Internal Publishing Details** page, in the **Path (optional)** box, type \**/\** _ as the path of the folder to be published.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="a8e27-130">Dans l’Assistant Publication de site Web, vous ne pouvez spécifier qu’un seul chemin.</span><span class="sxs-lookup"><span data-stu-id="a8e27-130">In the website publishing wizard you can only specify one path.</span></span> <span data-ttu-id="a8e27-131">Vous pouvez ajouter des chemins supplémentaires en modifiant les propriétés de la règle.</span><span class="sxs-lookup"><span data-stu-id="a8e27-131">Additional paths can be added by modifying the properties of the rule.</span></span>

    
    </div>

9.  <span data-ttu-id="a8e27-132">Dans la page _ \*public Name Details\*\*, confirmez que **ce nom de domaine** est sélectionné sous **accepter les demandes pour**, tapez le nom de domaine complet (FQDN) des services Web externes dans la zone **nom public** .</span><span class="sxs-lookup"><span data-stu-id="a8e27-132">On the _ *Public Name Details*\* page, confirm that **This domain name** is selected under **Accept Requests for**, type the external Web Services FQDN, in the **Public Name** box.</span></span>

10. <span data-ttu-id="a8e27-133">Dans la page **Sélectionner un écouteur Web** , cliquez sur **nouveau** pour ouvrir l’Assistant Nouvelle définition d’écoute Web.</span><span class="sxs-lookup"><span data-stu-id="a8e27-133">On **Select Web Listener** page, click **New** to open the New Web Listener Definition Wizard.</span></span>

11. <span data-ttu-id="a8e27-134">Dans la page Bienvenue dans l' **Assistant Nouvelle écoute Web** , tapez un nom pour l’écouteur Web dans la zone **nom de l’écouteur Web** (par exemple, LyncServerWebServers).</span><span class="sxs-lookup"><span data-stu-id="a8e27-134">On the **Welcome to the New Web Listener Wizard** page, type a name for the web listener in the **Web listener name** box (for example, LyncServerWebServers).</span></span>

12. <span data-ttu-id="a8e27-135">Dans la page sécurité de la **connexion client** , sélectionnez **exiger des connexions SSL sécurisées avec les clients**.</span><span class="sxs-lookup"><span data-stu-id="a8e27-135">On the **Client Connection Security** page, select **Require SSL secured connections with clients**.</span></span>

13. <span data-ttu-id="a8e27-136">Dans la page **adresse IP de l’écouteur Web** , sélectionnez **externe**, puis cliquez sur **Sélectionner des adresses IP**.</span><span class="sxs-lookup"><span data-stu-id="a8e27-136">On the **Web Listener IP Address** page, select **External**, and then click **Select IP Addresses**.</span></span>

14. <span data-ttu-id="a8e27-137">Dans la page de sélection de l' **écouteur externe** , sélectionnez **adresse IP spécifiée dans l’ordinateur Forefront TMG du réseau sélectionné**, sélectionnez l’adresse IP appropriée, puis cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="a8e27-137">On the **External Listener IP selection** page, select **Specified IP address on the Forefront TMG computer in the selected network**, select the appropriate IP address, click **Add**.</span></span>

15. <span data-ttu-id="a8e27-138">Sur la page **certificats SSL de l’écouteur** , sélectionnez **attribuer un certificat pour chaque adresse IP**, sélectionnez l’adresse IP associée au FQDN Web externe, puis cliquez sur **Sélectionner un certificat**.</span><span class="sxs-lookup"><span data-stu-id="a8e27-138">On the **Listener SSL Certificates** page, select **Assign a certificate for each IP address**, select the IP address that is associated with the external web FQDN, and then click **Select Certificate**.</span></span>

16. <span data-ttu-id="a8e27-139">Dans la page **Sélectionner un certificat** , sélectionnez le certificat correspondant aux noms publics spécifiés à l’étape 9, puis cliquez sur **Sélectionner**.</span><span class="sxs-lookup"><span data-stu-id="a8e27-139">On the **Select Certificate** page, select the certificate that matches the public names specified in step 9, click **Select**.</span></span>

17. <span data-ttu-id="a8e27-140">Dans la page **paramètres d’authentification** , sélectionnez **aucune authentification**.</span><span class="sxs-lookup"><span data-stu-id="a8e27-140">On the **Authentication Setting** page, select **No Authentication**.</span></span>

18. <span data-ttu-id="a8e27-141">Sur la page des **paramètres de connexion unique** , cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="a8e27-141">On the **Single Sign On Setting** page, click **Next**.</span></span>

19. <span data-ttu-id="a8e27-142">Dans la page **fin de l’Assistant réception de Web** , vérifiez que les paramètres de l' **écouteur** sont corrects, puis cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="a8e27-142">On the **Completing the Web Listener Wizard** page, verify that the **Web listener** settings are correct, and then click **Finish**.</span></span>

20. <span data-ttu-id="a8e27-143">Dans la page **délégation d’authentification** , sélectionnez **aucune délégation, mais le client pourra s’authentifier directement**.</span><span class="sxs-lookup"><span data-stu-id="a8e27-143">On the **Authentication Delegation** page, select **No delegation, but client may authenticate directly**.</span></span>

21. <span data-ttu-id="a8e27-144">Dans la page **jeu d’utilisateurs** , cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="a8e27-144">On the **User Set** page, click **Next**.</span></span>

22. <span data-ttu-id="a8e27-145">Dans la page **fin de l’Assistant Nouvelle règle de publication Web** , vérifiez que les paramètres de règle de publication Web sont corrects, puis cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="a8e27-145">On the **Completing the New Web Publishing Rule Wizard** page, verify that the web publishing rule settings are correct, and then click **Finish**.</span></span>

23. <span data-ttu-id="a8e27-146">Cliquez sur **appliquer** dans le volet Détails pour enregistrer les modifications et mettre à jour la configuration.</span><span class="sxs-lookup"><span data-stu-id="a8e27-146">Click **Apply** in the details pane to save the changes and update the configuration.</span></span>

</div>

<div>

## <a name="to-create-a-web-server-publishing-rule-on-the-computer-running-iis-arr"></a><span data-ttu-id="a8e27-147">Pour créer une règle de publication sur le serveur Web sur l’ordinateur exécutant IIS ARR</span><span class="sxs-lookup"><span data-stu-id="a8e27-147">To create a web server publishing rule on the computer running IIS ARR</span></span>

1.  <span data-ttu-id="a8e27-148">Liez le certificat que vous allez utiliser pour le proxy inverse au protocole HTTPs.</span><span class="sxs-lookup"><span data-stu-id="a8e27-148">Bind the certificate that you will use for the reverse proxy to the HTTPS protocol.</span></span> <span data-ttu-id="a8e27-149">Cliquez sur **Démarrer**, cliquez sur **programmes**, sélectionnez **Outils d’administration**, puis cliquez sur **Gestionnaire des services Internet (IIS)**.</span><span class="sxs-lookup"><span data-stu-id="a8e27-149">Click **Start**, select **Programs**, select **Administrative Tools**, and then click **Internet Information Services (IIS) Manager**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="a8e27-150">Des informations d’aide, des captures d’écran et des recommandations supplémentaires sur le déploiement et la configuration d’IIS ARR sont disponibles dans l’article NextHop <A href="https://go.microsoft.com/fwlink/?linkid=293391">à l’aide d’IIS ARR en tant que proxy inverse de Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="a8e27-150">Additional help, screen shots and guidance on deploying and configuring IIS ARR can be found in the NextHop article <A href="https://go.microsoft.com/fwlink/?linkid=293391">Using IIS ARR as a Reverse Proxy for Lync Server 2013</A>.</span></span>

    
    </div>

2.  <span data-ttu-id="a8e27-151">Si vous ne l’avez pas déjà fait, importez le certificat que vous utiliserez pour le proxy inverse.</span><span class="sxs-lookup"><span data-stu-id="a8e27-151">If you have not already done so, import the certificate that you will use for the reverse proxy.</span></span> <span data-ttu-id="a8e27-152">Dans le **Gestionnaire des services Internet (IIS)**, cliquez sur le nom du serveur proxy inverse à gauche de la console.</span><span class="sxs-lookup"><span data-stu-id="a8e27-152">In **Internet Information Services (IIS) Manager**, click the reverse proxy server name on the left-hand size of the console.</span></span> <span data-ttu-id="a8e27-153">Au milieu de la console sous **IIS** , recherchez **certificats de serveur**.</span><span class="sxs-lookup"><span data-stu-id="a8e27-153">In the middle of the console under **IIS** locate **Server Certificates**.</span></span> <span data-ttu-id="a8e27-154">Cliquez sur **certificats de serveur** avec le bouton droit, puis sélectionnez **ouvrir la fonctionnalité**.</span><span class="sxs-lookup"><span data-stu-id="a8e27-154">Right-click **Server Certificates** and select **Open feature**.</span></span>

3.  <span data-ttu-id="a8e27-155">Sur le côté droit de la console, cliquez sur **Importer...**.</span><span class="sxs-lookup"><span data-stu-id="a8e27-155">On the right hand side of the console, click **Import…**.</span></span> <span data-ttu-id="a8e27-156">Tapez le chemin d’accès et le nom du fichier du certificat portant l’extension ou cliquez sur **...**</span><span class="sxs-lookup"><span data-stu-id="a8e27-156">Type the path and filename of the certificate with the extension, or click **…**</span></span> <span data-ttu-id="a8e27-157">pour rechercher le certificat.</span><span class="sxs-lookup"><span data-stu-id="a8e27-157">to browse for the certificate.</span></span> <span data-ttu-id="a8e27-158">Sélectionnez le certificat et cliquez sur **ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="a8e27-158">Select the certificate and click **Open**.</span></span> <span data-ttu-id="a8e27-159">Entrez le mot de passe utilisé pour protéger la clé privée (si vous avez attribué un mot de passe lors de l’exportation du certificat et de la clé privée).</span><span class="sxs-lookup"><span data-stu-id="a8e27-159">Supply the password used to protect the private key (if you assigned a password when exporting the certificate and private key).</span></span> <span data-ttu-id="a8e27-160">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="a8e27-160">Click **OK**.</span></span> <span data-ttu-id="a8e27-161">Si l’importation du certificat est réussie, le certificat apparaît comme entrée dans le milieu de la console en tant qu’entrée dans les **certificats de serveur**.</span><span class="sxs-lookup"><span data-stu-id="a8e27-161">If the certificate import was successful, the certificate will appear as an entry in the middle of the console as an entry in **Server Certificates**.</span></span>

4.  <span data-ttu-id="a8e27-162">Attribuez le certificat pour une utilisation par HTTPs.</span><span class="sxs-lookup"><span data-stu-id="a8e27-162">Assign the certificate for use by HTTPS.</span></span> <span data-ttu-id="a8e27-163">Sur le côté gauche de la console, sélectionnez le **site Web par défaut** du serveur IIS.</span><span class="sxs-lookup"><span data-stu-id="a8e27-163">On the left-hand side of the console, select the **Default Web Site** of the IIS server.</span></span> <span data-ttu-id="a8e27-164">Sur le côté droit, cliquez sur **liaisons...**.</span><span class="sxs-lookup"><span data-stu-id="a8e27-164">On the right-hand side, click **Bindings…**.</span></span> <span data-ttu-id="a8e27-165">Dans la boîte de dialogue **liaisons de sites** , cliquez sur **Ajouter...**.</span><span class="sxs-lookup"><span data-stu-id="a8e27-165">In the **Site Bindings** dialog, click **Add…**.</span></span> <span data-ttu-id="a8e27-166">Dans la boîte de dialogue **Ajouter une liaison de site** , sous **type :**, sélectionnez **https**.</span><span class="sxs-lookup"><span data-stu-id="a8e27-166">On the **Add Site Binding** dialog under **Type:**, select **https**.</span></span> <span data-ttu-id="a8e27-167">La sélection de https vous permet de sélectionner le certificat à utiliser pour HTTPS.</span><span class="sxs-lookup"><span data-stu-id="a8e27-167">Selecting https will allow you to select the certificate to use for https.</span></span> <span data-ttu-id="a8e27-168">Sous **certificat SSL :**, sélectionnez le certificat que vous avez importé pour le proxy inverse.</span><span class="sxs-lookup"><span data-stu-id="a8e27-168">Under **SSL certificate:**, select the certificate that you imported for the reverse proxy.</span></span> <span data-ttu-id="a8e27-169">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="a8e27-169">Click **OK**.</span></span> <span data-ttu-id="a8e27-170">Cliquez ensuite sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="a8e27-170">Then, click **Close**.</span></span> <span data-ttu-id="a8e27-171">Le certificat est désormais lié au proxy inverse pour SSL (Secure Socket Layer) et TLS (Transport Layer Security).</span><span class="sxs-lookup"><span data-stu-id="a8e27-171">The certificate is now bound to the reverse proxy for secure socket layer (SSL) and transport layer security (TLS).</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="a8e27-172">Si vous recevez un message d’avertissement lors de la fermeture des boîtes de dialogue de liaison, il manque des certificats intermédiaires, vous devez localiser et importer le certificat d’autorité racine de l’autorité de certification publique et les certificats d’autorité de certification intermédiaires.</span><span class="sxs-lookup"><span data-stu-id="a8e27-172">If you receive a warning when closing the Bindings dialogs that intermediate certificates are missing, you need to locate and import the public CA root authority certificate and any intermediate CA certificates.</span></span> <span data-ttu-id="a8e27-173">Reportez-vous aux instructions de l’autorité publique qui vous a demandé votre certificat et suivez les instructions pour demander et importer une chaîne de certificats.</span><span class="sxs-lookup"><span data-stu-id="a8e27-173">Consult the instructions at the public CA that you requested your certificate from and follow the instructions to request and import a certificate chain.</span></span> <span data-ttu-id="a8e27-174">Si vous avez exporté le certificat à partir de votre serveur Edge, vous pouvez exporter le certificat de l’autorité de certification racine et les certificats d’autorité de certification intermédiaires associés au serveur Edge.</span><span class="sxs-lookup"><span data-stu-id="a8e27-174">If you exported the certificate from your Edge Server, you can export the root CA certificate and any intermediate CA certificates associated with the Edge Server.</span></span> <span data-ttu-id="a8e27-175">Importez le certificat racine de l’autorité de certification dans la Banque d’autorités de certification racine de l’ordinateur (à ne pas confondre avec le magasin de l’utilisateur).</span><span class="sxs-lookup"><span data-stu-id="a8e27-175">Import the root CA certificate into the Computer’s (not to be confused with the User store) Trusted Root Certification Authorities store and intermediate certificates into the Computer’s Intermediate Certification Authorities store.</span></span>

    
    </div>

5.  <span data-ttu-id="a8e27-176">Sur le côté gauche de la console sous le nom du serveur IIS, cliquez avec le bouton droit sur **batteries de serveurs** , puis cliquez sur créer une **batterie de serveurs.**</span><span class="sxs-lookup"><span data-stu-id="a8e27-176">On the left-hand side of the console below the IIS server name, right-click **Server Farms** then click **Create Server Farm…**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="a8e27-177">Si vous ne voyez pas le nœud <STRONG>batteries de serveurs</STRONG> , vous devez installer le routage de demandes d’application.</span><span class="sxs-lookup"><span data-stu-id="a8e27-177">If you do not see the <STRONG>Server Farms</STRONG> node, you need to install Application Request Routing.</span></span> <span data-ttu-id="a8e27-178">Pour plus d’informations, reportez-vous à la rubrique <A href="lync-server-2013-setting-up-reverse-proxy-servers.md">configuration de serveurs proxy inverse pour Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="a8e27-178">For details, see <A href="lync-server-2013-setting-up-reverse-proxy-servers.md">Setting up reverse proxy servers for Lync Server 2013</A>.</span></span>

    
    </div>
    
    <span data-ttu-id="a8e27-179">Dans la boîte de dialogue **créer une batterie de serveurs** dans nom de la batterie de **serveurs**, tapez un nom (nom convivial pour les fins d’identification) pour la première URL.</span><span class="sxs-lookup"><span data-stu-id="a8e27-179">On the **Create Server Farm** dialog in **Server farm name**, type the a name (this can be a friendly name for identification purposes) for the first URL.</span></span> <span data-ttu-id="a8e27-180">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="a8e27-180">Click **Next**.</span></span>

6.  <span data-ttu-id="a8e27-181">Dans la boîte de dialogue **Ajouter un serveur** dans **adresse du serveur**, tapez le nom de domaine complet (FQDN) des services Web externes sur votre serveur frontal.</span><span class="sxs-lookup"><span data-stu-id="a8e27-181">On the **Add Server** dialog in **Server Address**, type the fully qualified domain name (FQDN) of the external web services on your Front End Server.</span></span> <span data-ttu-id="a8e27-182">Les noms qui seront utilisés ici, par exemple, sont les mêmes que ceux utilisés dans la section planification du proxy inverse, du [proxy de certificat-proxy inverse dans Lync Server 2013](lync-server-2013-certificate-summary-reverse-proxy.md).</span><span class="sxs-lookup"><span data-stu-id="a8e27-182">The names that will be used here for example purposes are the same that are used in the Planning section for the reverse proxy, [Certificate summary - Reverse proxy in Lync Server 2013](lync-server-2013-certificate-summary-reverse-proxy.md).</span></span> <span data-ttu-id="a8e27-183">Pour vous référer à la planification du proxy inverse, entrez le nom de domaine complet `webext.contoso.com` .</span><span class="sxs-lookup"><span data-stu-id="a8e27-183">Referring to the reverse proxy planning, we type the FQDN `webext.contoso.com`.</span></span> <span data-ttu-id="a8e27-184">Vérifiez que la case à cocher en regard de **connecté** est sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="a8e27-184">Confirm that the checkbox next to **Online** is selected.</span></span> <span data-ttu-id="a8e27-185">Cliquez sur **Ajouter** pour ajouter le serveur à la liste de serveurs Web pour cette configuration.</span><span class="sxs-lookup"><span data-stu-id="a8e27-185">Click **Add** to add the server to the pool of web servers for this configuration.</span></span>
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="a8e27-186">Lync Server fait appel à des équilibreurs de charge matérielle pour le regroupement du Director et des serveurs frontaux pour le trafic HTTP et HTTPs.</span><span class="sxs-lookup"><span data-stu-id="a8e27-186">Lync Server uses hardware load balancers to pool Director and Front End Servers for HTTP and HTTPS traffic.</span></span> <span data-ttu-id="a8e27-187">Vous devez fournir un nom de domaine complet uniquement lors de l’ajout d’un serveur à la batterie de serveurs IIS ARR.</span><span class="sxs-lookup"><span data-stu-id="a8e27-187">You will only supply one FQDN when adding a server to the IIS ARR Server Farm.</span></span> <span data-ttu-id="a8e27-188">Le nom de domaine complet (FQDN) sera le serveur principal ou le directeur des configurations serveur hors pool ou le nom de domaine complet (FQDN) de l’équilibrage de charge matérielle configuré pour les pools de serveurs.</span><span class="sxs-lookup"><span data-stu-id="a8e27-188">The FQDN will be the Front End Server or Director in non-pooled server configurations, or the FQDN of the configured hardware load balancer for server pools.</span></span> <span data-ttu-id="a8e27-189">La seule méthode prise en charge pour le trafic HTTP et HTTPs consiste à utiliser des équilibreurs de charge matérielle.</span><span class="sxs-lookup"><span data-stu-id="a8e27-189">The only supported method to load balance HTTP and HTTPS traffic is by using hardware load balancers.</span></span>

    
    </div>

7.  <span data-ttu-id="a8e27-190">Dans la boîte de dialogue **Ajouter un serveur** , cliquez sur **Paramètres avancés.**</span><span class="sxs-lookup"><span data-stu-id="a8e27-190">On the **Add Server** dialog, click **Advanced settings…**.</span></span> <span data-ttu-id="a8e27-191">Cette action ouvre une boîte de dialogue permettant de définir le routage de requête d’application pour les demandes de nom de domaine complet configuré.</span><span class="sxs-lookup"><span data-stu-id="a8e27-191">This opens a dialog to define application request routing for requests to the configured FQDN.</span></span> <span data-ttu-id="a8e27-192">L’objectif est de redéfinir le port utilisé lors du traitement de la requête par IIS ARR.</span><span class="sxs-lookup"><span data-stu-id="a8e27-192">The purpose is to redefine what port is used when the request is processed by IIS ARR.</span></span>
    
    <span data-ttu-id="a8e27-193">Par défaut, le port HTTP de destination doit être défini comme 8080.</span><span class="sxs-lookup"><span data-stu-id="a8e27-193">By default, the destination HTTP port must be defined as 8080.</span></span> <span data-ttu-id="a8e27-194">Cliquez sur en regard de la **80 port http** et définissez la valeur sur **8080**.</span><span class="sxs-lookup"><span data-stu-id="a8e27-194">Click next to the current **httpPort 80** and set the value to **8080**.</span></span> <span data-ttu-id="a8e27-195">Cliquez sur en regard de la **443 port HTTPS** et définissez la valeur sur **4443**.</span><span class="sxs-lookup"><span data-stu-id="a8e27-195">Click next to the current **httpsPort 443** and set the value to **4443**.</span></span> <span data-ttu-id="a8e27-196">Laissez le paramètre **Weight** sur 100.</span><span class="sxs-lookup"><span data-stu-id="a8e27-196">Leave the **weight** parameter at 100.</span></span> <span data-ttu-id="a8e27-197">Le cas échéant, vous pouvez redéfinir les pondérations pour une règle donnée une fois que vous avez des statistiques de référence.</span><span class="sxs-lookup"><span data-stu-id="a8e27-197">If needed, you can redefine weights for a given rule once you have baseline statistics.</span></span> <span data-ttu-id="a8e27-198">Cliquez sur **Terminer** pour terminer cette partie de la configuration de la règle.</span><span class="sxs-lookup"><span data-stu-id="a8e27-198">Click **Finish** to complete this part of the rule configuration.</span></span>

8.  <span data-ttu-id="a8e27-199">Il est possible qu’une boîte de dialogue de réécriture d’URL s’affiche pour vous informer que le gestionnaire des services Internet peut créer une règle de réécriture d’URL pour acheminer automatiquement toutes les demandes entrantes vers la batterie de serveurs.</span><span class="sxs-lookup"><span data-stu-id="a8e27-199">You may see a dialog Rewrite Rules that informs you that IIS Manager can create a URL rewrite rule to route all incoming requests to the server farm automatically.</span></span> <span data-ttu-id="a8e27-200">Cliquez sur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="a8e27-200">Click **Yes**.</span></span> <span data-ttu-id="a8e27-201">Vous ajusterez les règles manuellement, mais le fait de sélectionner Yes définit la configuration initiale.</span><span class="sxs-lookup"><span data-stu-id="a8e27-201">You will adjust the rules manually, but selecting Yes sets the initial configuration..</span></span>

9.  <span data-ttu-id="a8e27-202">Cliquez sur le nom de la batterie de serveurs que vous venez de créer.</span><span class="sxs-lookup"><span data-stu-id="a8e27-202">Click the name of the server farm that you have just created.</span></span> <span data-ttu-id="a8e27-203">Sous **batterie de serveurs** dans l’affichage fonctionnalités du gestionnaire de services Internet, vous double-cliquez sur **mise en cache**.</span><span class="sxs-lookup"><span data-stu-id="a8e27-203">Under **Server Farm** in IIS Manager Features View, you double-click **Caching**.</span></span> <span data-ttu-id="a8e27-204">Désactivez l’option **activer le cache disque**.</span><span class="sxs-lookup"><span data-stu-id="a8e27-204">Deselect **Enable disk cache**.</span></span> <span data-ttu-id="a8e27-205">Cliquez sur **appliquer** sur le côté droit.</span><span class="sxs-lookup"><span data-stu-id="a8e27-205">Click **Apply** on the right-hand side.</span></span>

10. <span data-ttu-id="a8e27-206">Cliquez sur le nom de la batterie de serveurs.</span><span class="sxs-lookup"><span data-stu-id="a8e27-206">Click the name of the server farm.</span></span> <span data-ttu-id="a8e27-207">Sous **batterie de serveurs** dans l’affichage fonctionnalités du gestionnaire de services Internet, vous double-cliquez sur **proxy**.</span><span class="sxs-lookup"><span data-stu-id="a8e27-207">Under **Server Farm** in IIS Manager Features View, you double-click **Proxy**.</span></span> <span data-ttu-id="a8e27-208">Dans la page Paramètres du proxy, remplacez la valeur du délai d’expiration **(secondes)** par une valeur adaptée à votre déploiement.</span><span class="sxs-lookup"><span data-stu-id="a8e27-208">On the Proxy settings page change the value for **Time-out (seconds)** to a value appropriate for your deployment.</span></span> <span data-ttu-id="a8e27-209">Cliquez sur **appliquer** pour enregistrer la modification.</span><span class="sxs-lookup"><span data-stu-id="a8e27-209">Click **Apply** to save the change.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="a8e27-210">La valeur du délai d’expiration du proxy est un nombre qui peut varier d’un déploiement au déploiement.</span><span class="sxs-lookup"><span data-stu-id="a8e27-210">The Proxy Time-out value is a number that will vary from deployment to deployment.</span></span> <span data-ttu-id="a8e27-211">Nous vous conseillons de surveiller votre déploiement et de modifier la valeur de la meilleure utilisation pour les clients.</span><span class="sxs-lookup"><span data-stu-id="a8e27-211">You should monitor your deployment and modify the value for the best experience for clients.</span></span> <span data-ttu-id="a8e27-212">Il est possible que vous puissiez définir la valeur sur une valeur inférieure ou égale à 200.</span><span class="sxs-lookup"><span data-stu-id="a8e27-212">You may be able to set the value as low as 200.</span></span> <span data-ttu-id="a8e27-213">Si vous prenez en charge des clients mobiles Lync dans votre environnement, définissez la valeur sur 960 pour autoriser les délais d’expiration de notifications de transmission d’Office 365 qui ont une valeur de délai d’expiration de 900.</span><span class="sxs-lookup"><span data-stu-id="a8e27-213">If you are supporting Lync mobile clients in your environment, you should set the value to 960 to allow for push notifications timeout from Office 365 which have a time-out value of 900.</span></span> <span data-ttu-id="a8e27-214">Il est très probable que vous deviez augmenter la valeur du délai d’expiration pour éviter que le client se déconnecte lorsque la valeur est trop faible ou que le nombre de connexions par le biais du proxy ne se déconnecte pas et qu’elle est désactivée longtemps après la déconnexion du client.</span><span class="sxs-lookup"><span data-stu-id="a8e27-214">It is very likely that you will need to increase the time-out value to avoid client disconnects when the value is too low or decrease the number if connections through the proxy do not disconnect and clear long after the client has disconnected.</span></span> <span data-ttu-id="a8e27-215">Le fait de surveiller et de définir la position normale pour votre environnement est le seul moyen de déterminer où se trouve le paramètre approprié pour cette valeur.</span><span class="sxs-lookup"><span data-stu-id="a8e27-215">Monitoring and base-lining what is normal for your environment is the only accurate means to determine where the right setting is for this value.</span></span>

    
    </div>

11. <span data-ttu-id="a8e27-216">Cliquez sur le nom de la batterie de serveurs.</span><span class="sxs-lookup"><span data-stu-id="a8e27-216">Click the name of the server farm.</span></span> <span data-ttu-id="a8e27-217">Sous **batterie de serveurs** dans l’affichage fonctionnalités du gestionnaire de services Internet, vous double-cliquez sur **règles de routage**.</span><span class="sxs-lookup"><span data-stu-id="a8e27-217">Under **Server Farm** in IIS Manager Features View, you double-click **Routing Rules**.</span></span> <span data-ttu-id="a8e27-218">Dans la boîte de dialogue Règles de routage sous routage, désactivez la case à cocher en regard de activer le déchargement SSL.</span><span class="sxs-lookup"><span data-stu-id="a8e27-218">On the Routing Rules dialog under Routing, clear the checkbox next to Enable SSL offloading.</span></span> <span data-ttu-id="a8e27-219">Si vous ne pouvez pas désactiver la case à cocher, activez la case à cocher **utiliser la réécriture d’URL pour inspecter les demandes entrantes**.</span><span class="sxs-lookup"><span data-stu-id="a8e27-219">If the ability to clear the checkbox is not available, select the checkbox for **Use URL Rewrite to inspect incoming requests**.</span></span> <span data-ttu-id="a8e27-220">Cliquez sur **appliquer** pour enregistrer vos modifications.</span><span class="sxs-lookup"><span data-stu-id="a8e27-220">Click **Apply** to save your changes.</span></span>
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="a8e27-221">Le déchargement SSL par le proxy inverse n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="a8e27-221">SSL Offloading by the reverse proxy is not supported.</span></span>

    
    </div>

12. <span data-ttu-id="a8e27-222">Répétez les étapes 5-11 pour chaque URL qui doit traverser le proxy inverse.</span><span class="sxs-lookup"><span data-stu-id="a8e27-222">Repeat Steps 5-11 for each URL that must pass through the reverse proxy.</span></span> <span data-ttu-id="a8e27-223">Une liste courante serait la suivante :</span><span class="sxs-lookup"><span data-stu-id="a8e27-223">A common list would be the following:</span></span>
    
      - <span data-ttu-id="a8e27-224">Services Web du serveur frontal externes : webext.contoso.com (déjà configurés par le biais du parcours initial)</span><span class="sxs-lookup"><span data-stu-id="a8e27-224">Front End Server Web services external: webext.contoso.com (already configured by initial walk through)</span></span>
    
      - <span data-ttu-id="a8e27-225">Services Web de Director externes pour Director : webdirext.contoso.com (facultatif si un directeur est déployé)</span><span class="sxs-lookup"><span data-stu-id="a8e27-225">Director Web services external for Director: webdirext.contoso.com (Optional if a Director is deployed)</span></span>
    
      - <span data-ttu-id="a8e27-226">URL simple : meet.contoso.com</span><span class="sxs-lookup"><span data-stu-id="a8e27-226">Simple URL meet: meet.contoso.com</span></span>
    
      - <span data-ttu-id="a8e27-227">Connexion simple pour les URL : dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="a8e27-227">Simple URL dialin: dialin.contoso.com</span></span>
    
      - <span data-ttu-id="a8e27-228">URL de découverte automatique Lync : lyncdiscover.contoso.com</span><span class="sxs-lookup"><span data-stu-id="a8e27-228">Lync Autodiscover URL: lyncdiscover.contoso.com</span></span>
    
      - <span data-ttu-id="a8e27-229">URL du serveur Office Web Apps : officewebapps01.contoso.com</span><span class="sxs-lookup"><span data-stu-id="a8e27-229">Office Web Apps Server URL: officewebapps01.contoso.com</span></span>
        
        <div>
        

        > [!IMPORTANT]  
        > <span data-ttu-id="a8e27-230">L’URL du serveur Office Web Apps utilisera une adresse port HTTPS différente.</span><span class="sxs-lookup"><span data-stu-id="a8e27-230">The URL for the Office Web Apps Server will use a different httpsPort address.</span></span> <span data-ttu-id="a8e27-231">À l’étape 7, vous définissez <STRONG>port HTTPS</STRONG> comme <STRONG>443</STRONG> et <STRONG>port http</STRONG> en tant que port <STRONG>80</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="a8e27-231">In step 7, you define the <STRONG>httpsPort</STRONG> as <STRONG>443</STRONG> and the <STRONG>httpPort</STRONG> as port <STRONG>80</STRONG>.</span></span> <span data-ttu-id="a8e27-232">Les autres paramètres de configuration sont les mêmes.</span><span class="sxs-lookup"><span data-stu-id="a8e27-232">All other configuration settings are the same.</span></span>

        
        </div>

13. <span data-ttu-id="a8e27-233">Sur le côté gauche de la console, cliquez sur le nom du serveur IIS.</span><span class="sxs-lookup"><span data-stu-id="a8e27-233">On the left-hand side of the console, click the IIS server name.</span></span> <span data-ttu-id="a8e27-234">Au milieu de la console, repérez la **réécriture d’URL** sous **IIS**.</span><span class="sxs-lookup"><span data-stu-id="a8e27-234">In the middle of the console, locate **URL Rewrite** under **IIS**.</span></span> <span data-ttu-id="a8e27-235">Double-cliquez sur réécriture d’URL pour ouvrir la configuration des règles de réécriture d’URL.</span><span class="sxs-lookup"><span data-stu-id="a8e27-235">Double-click URL Rewrite to open the URL Rewrite rules configuration.</span></span> <span data-ttu-id="a8e27-236">Vous devez voir les règles de chaque batterie de serveurs que vous avez créée lors des étapes précédentes.</span><span class="sxs-lookup"><span data-stu-id="a8e27-236">You should see rules for each Server Farm that you created in the previous steps.</span></span> <span data-ttu-id="a8e27-237">Si ce n’est pas le cas, vérifiez que vous avez cliqué sur le nom du **serveur IIS** juste en dessous du nœud de la **page de démarrage** dans la console du gestionnaire d’informations Internet.</span><span class="sxs-lookup"><span data-stu-id="a8e27-237">If you do not, confirm that you clicked on the **IIS Server** name immediately below the **Start Page** node in the Internet Information Server Manager console.</span></span>

14. <span data-ttu-id="a8e27-238">Dans la boîte de dialogue de **réécriture d’URL** , en utilisant webext.contoso.com en guise d’exemple, le nom complet de la règle telle qu’affichée est **arr \_ webext.contoso.com \_ LoadBalance \_ SSL**.</span><span class="sxs-lookup"><span data-stu-id="a8e27-238">In the **URL Rewrite** dialog, using webext.contoso.com as an example, the full name of the rule as displayed is **ARR\_webext.contoso.com\_loadbalance\_SSL**.</span></span>
    
      - <span data-ttu-id="a8e27-239">Double-cliquez sur la règle pour ouvrir la boîte de dialogue **modifier la règle de trafic entrant** .</span><span class="sxs-lookup"><span data-stu-id="a8e27-239">Double-click the rule to open the **Edit Inbound Rule** dialog.</span></span>
    
      - <span data-ttu-id="a8e27-240">Cliquez sur **Ajouter...**</span><span class="sxs-lookup"><span data-stu-id="a8e27-240">Click **Add…**</span></span> <span data-ttu-id="a8e27-241">dans la boîte de dialogue **conditions** .</span><span class="sxs-lookup"><span data-stu-id="a8e27-241">on the **Conditions** dialog.</span></span>
    
      - <span data-ttu-id="a8e27-242">Sur la **condition ajouter** dans l’entrée de la **condition :** tapez **{http \_ Host}**.</span><span class="sxs-lookup"><span data-stu-id="a8e27-242">On the **Add Condition** in **Condition input:** type **{HTTP\_HOST}**.</span></span> <span data-ttu-id="a8e27-243">(Lors de la saisie, une boîte de dialogue s’affiche pour vous permettre de sélectionner l’État).</span><span class="sxs-lookup"><span data-stu-id="a8e27-243">(As you type, a dialog appears that will let you select the condition).</span></span> <span data-ttu-id="a8e27-244">sous **vérifier si la chaîne d’entrée :** , sélectionnez **correspond au modèle**.</span><span class="sxs-lookup"><span data-stu-id="a8e27-244">under **Check if input string:** select **Matches the Pattern**.</span></span> <span data-ttu-id="a8e27-245">Dans le type **d’entrée de modèle** **\* *_. _* ignorer la casse** doit être sélectionné.</span><span class="sxs-lookup"><span data-stu-id="a8e27-245">In the **Pattern input** type **\**_. _\* Ignore case*\* should be selected.</span></span> <span data-ttu-id="a8e27-246">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="a8e27-246">Click **OK**.</span></span>
    
      - <span data-ttu-id="a8e27-247">Faites défiler la boîte de dialogue **modifier la règle de trafic entrant** pour rechercher la boîte de dialogue **action** .</span><span class="sxs-lookup"><span data-stu-id="a8e27-247">Scroll down in the **Edit Inbound Rule** dialog to locate the **Action** dialog.</span></span> <span data-ttu-id="a8e27-248">**Type d’action :** doit être défini sur **route vers la batterie de serveurs**, **schéma :** défini sur **https://**, **batterie de serveurs :** définie sur l’URL à laquelle s’applique cette règle.</span><span class="sxs-lookup"><span data-stu-id="a8e27-248">**Action Type:** should be set to **Route to Server Farm**, **Scheme:** set to **https://**, **Server farm:** set to the URL that this rule applies to.</span></span> <span data-ttu-id="a8e27-249">Pour cet exemple, ce doit être défini sur **webext.contoso.com**.</span><span class="sxs-lookup"><span data-stu-id="a8e27-249">For this example, this should be set to **webext.contoso.com**.</span></span> <span data-ttu-id="a8e27-250">**Path :** est défini sur **/{R : 0}**</span><span class="sxs-lookup"><span data-stu-id="a8e27-250">**Path:** is set to **/{R:0}**</span></span>
    
      - <span data-ttu-id="a8e27-251">Cliquez sur **appliquer** pour enregistrer vos modifications.</span><span class="sxs-lookup"><span data-stu-id="a8e27-251">Click **Apply** to save your changes.</span></span> <span data-ttu-id="a8e27-252">Cliquez sur **retour aux règles** pour revenir aux règles de réécriture d’URL.</span><span class="sxs-lookup"><span data-stu-id="a8e27-252">Click **Back to Rules** to return to the URL Rewrite rules.</span></span>

15. <span data-ttu-id="a8e27-253">Répétez la procédure définie à l’étape 14 pour chacune des règles de réécriture SSL que vous avez définies, une pour chaque URL de batterie de serveurs.</span><span class="sxs-lookup"><span data-stu-id="a8e27-253">Repeat the procedure defined in Step 14 for each of the SSL rewrite rules that you have defined, one per Server Farm URL.</span></span>
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="a8e27-254">Par défaut, les règles HTTP sont également créées et sont dénotées par leur appellation similaire aux règles SSL.</span><span class="sxs-lookup"><span data-stu-id="a8e27-254">By default, HTTP rules are created as well and are denoted by the similar naming to the SSL rules.</span></span> <span data-ttu-id="a8e27-255">Pour notre exemple actuel, la règle HTTP s’appelle <STRONG>ARR_webext. contoso. com _loadbalance</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="a8e27-255">For our current example, the HTTP rule would be named <STRONG>ARR_webext.contoso.com_loadbalance</STRONG>.</span></span> <span data-ttu-id="a8e27-256">Il n’est pas nécessaire de modifier ces règles et celles-ci peuvent être ignorées en toute sécurité.</span><span class="sxs-lookup"><span data-stu-id="a8e27-256">No modifications are needed to these rules and they can be safely ignored.</span></span>

    
    </div>

</div>

<div>

## <a name="to-modify-the-properties-of-the-web-publishing-rule-in-tmg-2010"></a><span data-ttu-id="a8e27-257">Pour modifier les propriétés de la règle de publication Web dans TMG 2010</span><span class="sxs-lookup"><span data-stu-id="a8e27-257">To modify the properties of the web publishing rule in TMG 2010</span></span>

1.  <span data-ttu-id="a8e27-258">Cliquez sur **Démarrer**, pointez sur **programmes**, sélectionnez **Microsoft Forefront TMG**, puis cliquez sur **gestion de Forefront TMG**.</span><span class="sxs-lookup"><span data-stu-id="a8e27-258">Click **Start**, point to **Programs**, select **Microsoft Forefront TMG**, and then click **Forefront TMG Management**.</span></span>

2.  <span data-ttu-id="a8e27-259">Dans le volet gauche, développez **NomServeur**, puis cliquez sur **stratégie de pare-feu**.</span><span class="sxs-lookup"><span data-stu-id="a8e27-259">In the left pane, expand **ServerName**, and then click **Firewall Policy**.</span></span>

3.  <span data-ttu-id="a8e27-260">Dans le volet Détails, cliquez avec le bouton droit sur la règle de publication sur le serveur Web que vous avez créée au cours de la procédure précédente (par exemple, LyncServerExternalRule), puis cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="a8e27-260">In the details pane, right-click the web server publishing rule that you created in the previous procedure (for example, LyncServerExternalRule), and then click **Properties**.</span></span>

4.  <span data-ttu-id="a8e27-261">Dans la page **Propriétés** , sous l’onglet **de** , effectuez les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="a8e27-261">On the **Properties** page, on the **From** tab, do the following:</span></span>
    
      - <span data-ttu-id="a8e27-262">Dans la liste **cette règle s’applique au trafic de ces sources** , cliquez sur **n’importe où**, puis cliquez sur **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="a8e27-262">In the **This rule applies to traffic from these sources** list, click **Anywhere**, and then click **Remove**.</span></span>
    
      - <span data-ttu-id="a8e27-263">Cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="a8e27-263">Click **Add**.</span></span>
    
      - <span data-ttu-id="a8e27-264">Dans **Ajouter des entités réseau**, développez **réseaux**, cliquez sur **externe**, cliquez sur **Ajouter**, puis sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="a8e27-264">In **Add Network Entities**, expand **Networks**, click **External**, click **Add**, and then click **Close**.</span></span>

5.  <span data-ttu-id="a8e27-265">Dans l’onglet **à** , assurez-vous que la case à cocher **transférer l’en-tête de l’hôte d’origine au lieu de la** case à cocher réel est activée.</span><span class="sxs-lookup"><span data-stu-id="a8e27-265">On the **To** tab, ensure that the **Forward the original host header instead of the actual one** check box is selected.</span></span>

6.  <span data-ttu-id="a8e27-266">Dans l’onglet **pontage** , activez la case à cocher **rediriger la demande vers le port SSL** , puis spécifiez le port **4443**.</span><span class="sxs-lookup"><span data-stu-id="a8e27-266">On the **Bridging** tab, select the **Redirect request to SSL port** check box, and then specify port **4443**.</span></span>

7.  <span data-ttu-id="a8e27-267">Dans l’onglet **nom du public** , ajoutez les URL simples (par exemple, meet.contoso.com et Dialin.contoso.com).</span><span class="sxs-lookup"><span data-stu-id="a8e27-267">On the **Public Name** tab, add the simple URLs (for example, meet.contoso.com and dialin.contoso.com).</span></span>

8.  <span data-ttu-id="a8e27-268">Cliquez sur **appliquer** pour enregistrer les modifications, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="a8e27-268">Click **Apply** to save changes, and then click **OK**.</span></span>

9.  <span data-ttu-id="a8e27-269">Cliquez sur **appliquer** dans le volet Détails pour enregistrer les modifications et mettre à jour la configuration.</span><span class="sxs-lookup"><span data-stu-id="a8e27-269">Click **Apply** in the details pane to save the changes and update the configuration.</span></span>

</div>

<div>

## <a name="to-modify-the-properties-of-the-web-publishing-rule-in-iis-arr"></a><span data-ttu-id="a8e27-270">Pour modifier les propriétés de la règle de publication Web dans IIS ARR</span><span class="sxs-lookup"><span data-stu-id="a8e27-270">To modify the properties of the web publishing rule in IIS ARR</span></span>

1.  <span data-ttu-id="a8e27-271">Cliquez sur **Démarrer**, cliquez sur **programmes**, sélectionnez **Outils d’administration**, puis cliquez sur **Gestionnaire des services Internet (IIS)**.</span><span class="sxs-lookup"><span data-stu-id="a8e27-271">Click **Start**, select **Programs**, select **Administrative Tools**, and then click **Internet Information Services (IIS) Manager**.</span></span>

2.  <span data-ttu-id="a8e27-272">Sur le côté gauche de la console, cliquez sur le nom du serveur IIS.</span><span class="sxs-lookup"><span data-stu-id="a8e27-272">On the left-hand side of the console, click the IIS server name.</span></span>

3.  <span data-ttu-id="a8e27-273">Au milieu de la console, repérez la **réécriture d’URL** sous **IIS**.</span><span class="sxs-lookup"><span data-stu-id="a8e27-273">In the middle of the console, locate **URL Rewrite** under **IIS**.</span></span> <span data-ttu-id="a8e27-274">Double-cliquez sur réécriture d’URL pour ouvrir la configuration des règles de réécriture d’URL.</span><span class="sxs-lookup"><span data-stu-id="a8e27-274">Double-click URL Rewrite to open the URL Rewrite rules configuration.</span></span>

4.  <span data-ttu-id="a8e27-275">Double-cliquez sur la règle que vous devez modifier.</span><span class="sxs-lookup"><span data-stu-id="a8e27-275">Double-click the rule that you need to modify.</span></span> <span data-ttu-id="a8e27-276">Apportez les modifications souhaitées, selon les besoins, en fonction de l' **URL**, des **conditions**, des **variables serveur** ou de l' **action**.</span><span class="sxs-lookup"><span data-stu-id="a8e27-276">Make your modifications, as needed, in **Match URL**, **Conditions**, **Server Variables** or **Action**.</span></span>

5.  <span data-ttu-id="a8e27-277">Cliquez sur **appliquer** pour valider les modifications.</span><span class="sxs-lookup"><span data-stu-id="a8e27-277">Click **Apply** to commit your changes.</span></span> <span data-ttu-id="a8e27-278">Cliquez sur **retour aux règles** pour modifier d’autres règles ou fermez la console du **Gestionnaire des services Internet** si vous avez effectué vos modifications.</span><span class="sxs-lookup"><span data-stu-id="a8e27-278">Click **Back to Rules** to modify other rules, or close the **IIS Manager** console if you are done with your changes.</span></span>

<span data-ttu-id="a8e27-279"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a8e27-279"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

