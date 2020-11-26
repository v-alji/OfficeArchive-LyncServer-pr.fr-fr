---
title: 'Lync Server 2013 : Configuration du proxy inverse pour la mobilité'
description: 'Lync Server 2013 : configuration du proxy inverse pour la mobilité.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring the reverse proxy for mobility
ms:assetid: 3f4a9e33-77e4-4c18-a73f-24d4bec8ea9c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690011(v=OCS.15)
ms:contentKeyID: 48183946
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b4e1a71f97bc1737299d54cc0f4c56f0f5981bef
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432484"
---
# <a name="configuring-the-reverse-proxy-for-mobility-in-lync-server-2013"></a><span data-ttu-id="93d64-103">Configuration du proxy inverse pour la mobilité dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="93d64-103">Configuring the reverse proxy for mobility in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="93d64-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="93d64-104">

<span> </span></span></span>

<span data-ttu-id="93d64-105">_**Dernière modification de la rubrique :** 2014-03-20_</span><span class="sxs-lookup"><span data-stu-id="93d64-105">_**Topic Last Modified:** 2014-03-20_</span></span>

<span data-ttu-id="93d64-106">Si vous souhaitez utiliser la découverte automatique pour les clients d’appareils mobiles, vous devez modifier ou créer une nouvelle règle de publication Web pour le proxy inverse, que vous ayez ou non mis à jour les listes de noms de remplacement de l’objet sur les certificats proxy inverse.</span><span class="sxs-lookup"><span data-stu-id="93d64-106">If you want to use automatic discovery for mobile device clients, you need to modify an existing or create a new web publishing rule for the reverse proxy whether or not you update the subject alternative name lists on the reverse proxy certificates.</span></span>

<span data-ttu-id="93d64-107">Si vous décidez d’utiliser HTTPs pour les demandes de service de découverte automatique Lync Server 2013 et de mettre à jour les listes de noms de remplacement d’objet sur les certificats de proxy inverse, vous devez affecter le certificat public mis à jour à l’écouteur SSL (Secure Sockets Layer) sur votre proxy inverse.</span><span class="sxs-lookup"><span data-stu-id="93d64-107">If you decide to use HTTPS for initial Lync Server 2013 Autodiscover Service requests and update the subject alternative names lists on the reverse proxy certificates, you need to assign the updated public certificate to the Secure Sockets Layer (SSL) Listener on your reverse proxy.</span></span> <span data-ttu-id="93d64-108">Pour plus d’informations sur les entrées de nom de remplacement d’objet requises, voir [configuration technique requise pour la mobilité dans Lync Server 2013](lync-server-2013-technical-requirements-for-mobility.md).</span><span class="sxs-lookup"><span data-stu-id="93d64-108">For details about the required subject alternative name entries, see [Technical requirements for mobility in Lync Server 2013](lync-server-2013-technical-requirements-for-mobility.md).</span></span> <span data-ttu-id="93d64-109">Vous devez ensuite modifier l’écouteur existant pour les services Web externes ou créer une nouvelle règle de publication Web pour l’URL du service de découverte automatique externe.</span><span class="sxs-lookup"><span data-stu-id="93d64-109">You then need to modify the existing listener for the external web services or create a new web publishing rule for the external Autodiscover Service URL.</span></span> <span data-ttu-id="93d64-110">Si vous ne disposez pas encore d’une règle de publication sur le Web pour l’URL des services Web Lync Server 2013 externes pour votre pool frontal, vous devez également publier une règle pour celle-ci.</span><span class="sxs-lookup"><span data-stu-id="93d64-110">If you do not already have a web publishing rule for the external Lync Server 2013 Web Services URL for your Front End pool, you also need to publish a rule for that.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="93d64-111">La règle de publication de proxy inverse et l’écouteur peuvent service à la fois les services Web externes et le service de découverte automatique, tant que le certificat attribué à l’écouteur contient le nom du sujet et les noms de remplacement de l’objet requis pour les deux.</span><span class="sxs-lookup"><span data-stu-id="93d64-111">The reverse proxy publishing rule and listener can service both the external web services and the Autodiscover Service, as long as the certificate assigned to the listener contains the necessary subject name and subject alternative names for both.</span></span> <span data-ttu-id="93d64-112">Pour plus d’informations sur la configuration par défaut de l’écouteur et de la règle de publication sur le Web, reportez-vous à la rubrique <A href="lync-server-2013-setting-up-reverse-proxy-servers.md">configuration de serveurs proxy inverse pour Lync Server 2013</A> pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="93d64-112">For details on the default configuration of the web listener and publishing rule, see <A href="lync-server-2013-setting-up-reverse-proxy-servers.md">Setting up reverse proxy servers for Lync Server 2013</A> for more details.</span></span>



</div>

<span data-ttu-id="93d64-113">Si vous décidez d’utiliser HTTP pour les demandes de service de découverte automatique initiales afin de ne pas avoir besoin de mettre à jour les autres noms d’objet du proxy inverse, vous devez créer ou modifier une règle de publication Web pour le port 80.</span><span class="sxs-lookup"><span data-stu-id="93d64-113">If you decide to use HTTP for initial Autodiscover Service requests so that you do not need to update subject alternative names for the reverse proxy, you need to create or modify a web publishing rule for port 80.</span></span>

<span data-ttu-id="93d64-114">Les procédures décrites dans cette section expliquent comment créer ou modifier les règles de publication Web dans Microsoft Forefront Threat Management Gateway 2010 pour la découverte automatique.</span><span class="sxs-lookup"><span data-stu-id="93d64-114">The procedures in this section describe how to create or modify the web publishing rules in Microsoft Forefront Threat Management Gateway 2010 for automatic discovery.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="93d64-115">Les procédures suivantes présupposent que vous avez installé l’édition standard de Forefront Threat Management Gateway (TMG) 2010.</span><span class="sxs-lookup"><span data-stu-id="93d64-115">These procedures assume that you have installed the Standard Edition of Forefront Threat Management Gateway (TMG) 2010.</span></span> <span data-ttu-id="93d64-116">Si vous utilisez un autre proxy inverse, les procédures sont similaires, mais doivent être mappées à la documentation du produit tiers.</span><span class="sxs-lookup"><span data-stu-id="93d64-116">If you are using another reverse proxy, the procedures are similar, but will need to be mapped to the documentation for the third-party product.</span></span>



</div>

<div>

## <a name="to-create-a-web-publishing-rule-for-the-external-autodiscover-url"></a><span data-ttu-id="93d64-117">Pour créer une règle de publication Web pour l’URL de découverte automatique externe</span><span class="sxs-lookup"><span data-stu-id="93d64-117">To create a web publishing rule for the external Autodiscover URL</span></span>

1.  <span data-ttu-id="93d64-118">Cliquez sur **Démarrer**, pointez sur **programmes**, sur **Microsoft Forefront TMG**, puis cliquez sur gestion de **Forefront TMG**.</span><span class="sxs-lookup"><span data-stu-id="93d64-118">Click **Start**, point to **Programs**, point to **Microsoft Forefront TMG**, and then click **Forefront TMG Management**.</span></span>

2.  <span data-ttu-id="93d64-119">Dans le volet gauche, développez **NomServeur**, cliquez avec le bouton droit sur **stratégie de pare-feu**, pointez sur **nouveau**, puis cliquez sur règle de **publication de site Web**.</span><span class="sxs-lookup"><span data-stu-id="93d64-119">In the left pane, expand **ServerName**, right-click **Firewall Policy**, point to **New**, and then click **Web Site Publishing Rule**.</span></span>

3.  <span data-ttu-id="93d64-120">Dans la page **Bienvenue dans la nouvelle règle de publication Web** , tapez un nom d’affichage pour la nouvelle règle de publication (par exemple, LyncDiscoveryURL).</span><span class="sxs-lookup"><span data-stu-id="93d64-120">On the **Welcome to the New Web Publishing Rule** page, type a display name for the new publishing rule (for example, LyncDiscoveryURL).</span></span>

4.  <span data-ttu-id="93d64-121">Dans la page **Sélectionner une action de règle** , sélectionnez **autoriser**.</span><span class="sxs-lookup"><span data-stu-id="93d64-121">On the **Select Rule Action** page, select **Allow**.</span></span>

5.  <span data-ttu-id="93d64-122">Dans la page **type de publication** , sélectionnez **publier un site Web ou un équilibrage de charge unique**.</span><span class="sxs-lookup"><span data-stu-id="93d64-122">On the **Publishing Type** page, select **Publish a single Web site or load balancer**.</span></span>

6.  <span data-ttu-id="93d64-123">Dans la page sécurité de la **connexion au serveur** , sélectionnez **utiliser SSL pour se connecter au serveur Web publié ou à la batterie de** serveurs.</span><span class="sxs-lookup"><span data-stu-id="93d64-123">On the **Server Connection Security** page, select **Use SSL to connect to the published Web server or server farm**.</span></span>

7.  <span data-ttu-id="93d64-124">Dans la page Détails de la **publication interne** , dans **nom du site interne**, tapez le nom de domaine complet (FQDN) de votre pool de répertoires (par exemple, lyncdir01. contoso. local).</span><span class="sxs-lookup"><span data-stu-id="93d64-124">On the **Internal Publishing Details** page, in **Internal Site name**, type the fully qualified domain name (FQDN) of your Director pool (for example, lyncdir01.contoso.local).</span></span> <span data-ttu-id="93d64-125">Si vous créez une règle pour l’URL des services Web externes sur le pool frontal, tapez l’adresse VIP de l’équilibrage de charge matérielle (HLB) en face du pool frontal.</span><span class="sxs-lookup"><span data-stu-id="93d64-125">If you are creating a rule for the external Web Services URL on the Front End pool, type the VIP address of the Hardware Load Balancer (HLB) in front of the Front End pool.</span></span>

8.  <span data-ttu-id="93d64-126">Dans la page Détails de la **publication interne** , dans **Path (facultatif)**, tapez **/ \* *_ en tant que chemin d’accès au dossier à publier, puis sélectionnez _* transférer l’en-tête d’hôte d’origine**.</span><span class="sxs-lookup"><span data-stu-id="93d64-126">On the **Internal Publishing Details** page, in **Path (optional)**, type \**/\**_ as the path of the folder to be published, and then select _\* Forward the original host header\*\*.</span></span>

9.  <span data-ttu-id="93d64-127">Dans la page **Détails du nom public** , procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="93d64-127">On the **Public Name Details** page, do the following:</span></span>
    
      - <span data-ttu-id="93d64-128">Sous **accepter les demandes pour**, sélectionnez **ce nom de domaine**.</span><span class="sxs-lookup"><span data-stu-id="93d64-128">Under **Accept Requests for**, select **This domain name**.</span></span>
    
      - <span data-ttu-id="93d64-129">Dans **nom public**, tapez **lyncdiscover.**\<sipdomain\></span><span class="sxs-lookup"><span data-stu-id="93d64-129">In **Public Name**, type **lyncdiscover.**\<sipdomain\></span></span> <span data-ttu-id="93d64-130">(URL du service de découverte automatique externe).</span><span class="sxs-lookup"><span data-stu-id="93d64-130">(the external Autodiscover Service URL).</span></span> <span data-ttu-id="93d64-131">Si vous créez une règle pour l’URL des services Web externes sur le pool frontal, tapez le nom de domaine complet (FQDN) pour les services Web externes dans votre liste frontale (par exemple, lyncwebextpool01.contoso.com).</span><span class="sxs-lookup"><span data-stu-id="93d64-131">If you are creating a rule for the external Web Services URL on the Front End pool, type the FQDN for the external Web Services on your Front End pool (for example, lyncwebextpool01.contoso.com).</span></span>
    
      - <span data-ttu-id="93d64-132">Dans **path**, tapez \* */\** _.</span><span class="sxs-lookup"><span data-stu-id="93d64-132">In **Path**, type \**/\** _.</span></span>

10. <span data-ttu-id="93d64-133">Sur _ *Sélectionnez écouteur Web*, dans l' **écouteur Web**, sélectionnez votre écouteur SSL existant avec le certificat public mis à jour.</span><span class="sxs-lookup"><span data-stu-id="93d64-133">On _ *Select Web Listener*\* page, in **Web Listener**, select your existing SSL Listener with the updated public certificate.</span></span>

11. <span data-ttu-id="93d64-134">Dans la page **délégation d’authentification** , sélectionnez **aucune délégation, mais le client pourra s’authentifier directement**.</span><span class="sxs-lookup"><span data-stu-id="93d64-134">On the **Authentication Delegation** page, select **No delegation, but client may authenticate directly**.</span></span>

12. <span data-ttu-id="93d64-135">Dans la page **jeu d’utilisateurs** , sélectionnez tous les **utilisateurs**.</span><span class="sxs-lookup"><span data-stu-id="93d64-135">On the **User Set** page, select **All Users**.</span></span>

13. <span data-ttu-id="93d64-136">Dans la page **fin de l’Assistant Nouvelle règle de publication Web** , vérifiez que les paramètres de règle de publication Web sont corrects, puis cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="93d64-136">On the **Completing the New Web Publishing Rule Wizard** page, verify that the web publishing rule settings are correct, and then click **Finish**.</span></span>

14. <span data-ttu-id="93d64-137">Dans la liste de règles de publication Web de Forefront TMG, double-cliquez sur la nouvelle règle que vous venez d’ajouter pour ouvrir les **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="93d64-137">In the Forefront TMG list of web publishing rules, double-click the new rule you just added to open **Properties**.</span></span>

15. <span data-ttu-id="93d64-138">Dans l’onglet **à** , procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="93d64-138">On the **To** tab, do the following:</span></span>
    
      - <span data-ttu-id="93d64-139">Sélectionnez **transférer l’en-tête d’hôte d’origine au lieu du premier**.</span><span class="sxs-lookup"><span data-stu-id="93d64-139">Select **Forward the original host header instead of the actual one**.</span></span>
    
      - <span data-ttu-id="93d64-140">**Les demandes de sélection semblent provenir de l’ordinateur Forefront TMG**.</span><span class="sxs-lookup"><span data-stu-id="93d64-140">Select **Requests appear to come from the Forefront TMG computer**.</span></span>

16. <span data-ttu-id="93d64-141">Dans l’onglet **pontage** , configurez les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="93d64-141">On the **Bridging** tab, configure the following:</span></span>
    
      - <span data-ttu-id="93d64-142">Sélectionnez **serveur Web**.</span><span class="sxs-lookup"><span data-stu-id="93d64-142">Select **Web server**.</span></span>
    
      - <span data-ttu-id="93d64-143">Sélectionnez **Rediriger les demandes vers le port http** et tapez **8080** pour le numéro de port.</span><span class="sxs-lookup"><span data-stu-id="93d64-143">Select **Redirect requests to HTTP port**, and type **8080** for the port number.</span></span>
    
      - <span data-ttu-id="93d64-144">Sélectionnez **Rediriger les demandes vers le port SSL** et tapez **4443** pour le numéro de port.</span><span class="sxs-lookup"><span data-stu-id="93d64-144">Select **Redirect requests to SSL port**, and type **4443** for the port number.</span></span>

17. <span data-ttu-id="93d64-145">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="93d64-145">Click **OK**.</span></span>

18. <span data-ttu-id="93d64-146">Cliquez sur **appliquer** dans le volet Détails pour enregistrer les modifications et mettre à jour la configuration.</span><span class="sxs-lookup"><span data-stu-id="93d64-146">Click **Apply** in the details pane to save the changes and update the configuration.</span></span>

19. <span data-ttu-id="93d64-147">Cliquez sur **règle de test** pour vérifier que la configuration de votre nouvelle règle est correcte.</span><span class="sxs-lookup"><span data-stu-id="93d64-147">Click **Test Rule** to verify that your new rule is set up correctly.</span></span>

</div>

<div>

## <a name="to-modify-an-existing-web-publishing-rule-to-add-the-external-autodiscover-san-and-url"></a><span data-ttu-id="93d64-148">Pour modifier une règle de publication sur le Web existante pour ajouter le SAN de découverte automatique et l’URL externes</span><span class="sxs-lookup"><span data-stu-id="93d64-148">To modify an existing web publishing rule to add the external Autodiscover SAN and URL</span></span>

1.  <span data-ttu-id="93d64-149">Cliquez sur **Démarrer**, pointez sur **programmes**, sur **Microsoft Forefront TMG**, puis cliquez sur gestion de **Forefront TMG**.</span><span class="sxs-lookup"><span data-stu-id="93d64-149">Click **Start**, point to **Programs**, point to **Microsoft Forefront TMG**, and then click **Forefront TMG Management**.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="93d64-150">Vous devrez répéter la modification pour chaque règle de publication et votre écouteur.</span><span class="sxs-lookup"><span data-stu-id="93d64-150">You will repeat the modification for each publishing rule and listener that you have.</span></span> <span data-ttu-id="93d64-151">En règle générale, il s’agit d’une règle et d’un écouteur pour les pools frontaux et l’un pour les directeurs ou pools de directeurs facultatifs, si vous les avez déployés.</span><span class="sxs-lookup"><span data-stu-id="93d64-151">Typically, this will be one rule and listener for the Front End pools and one for the optional Directors or Director pools, if you have deployed them.</span></span>

    
    </div>

2.  <span data-ttu-id="93d64-152">Dans le volet gauche, développez **NomServeur**, cliquez avec le bouton droit sur **stratégie de pare-feu**, puis cliquez sur la règle applicable.</span><span class="sxs-lookup"><span data-stu-id="93d64-152">In the left pane, expand **ServerName**, right-click **Firewall Policy**, click the applicable rule.</span></span> <span data-ttu-id="93d64-153">Sous l’onglet **tâches** , cliquez sur **modifier la règle sélectionnée**.</span><span class="sxs-lookup"><span data-stu-id="93d64-153">On the **Tasks** tab, click **Edit Selected rule**.</span></span>

3.  <span data-ttu-id="93d64-154">Dans l’onglet **nom du public** , dans **cette règle**, sélectionnez **demandes pour les sites Web suivants**.</span><span class="sxs-lookup"><span data-stu-id="93d64-154">On the **Public Name** tab, in **This rule applies to**, select **Requests for the following Web sites**.</span></span>

4.  <span data-ttu-id="93d64-155">Cliquez sur **Ajouter**, tapez le nom du nouveau site de découverte automatique (par exemple, « lyncdiscover.contoso.com »), puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="93d64-155">Click **Add**, type the name of the new Autodiscover site (for example, “lyncdiscover.contoso.com”), and then click **OK**.</span></span>

5.  <span data-ttu-id="93d64-156">Dans l’onglet **écouteur** , cliquez sur **Sélectionner un certificat** et attribuez le nouveau certificat aux entrées du réseau de découverte automatique ajoutées.</span><span class="sxs-lookup"><span data-stu-id="93d64-156">On the **Listener** tab, click **Select Certificate** and assign the new certificate with the added Autodiscover SAN entries.</span></span> <span data-ttu-id="93d64-157">Fermez les propriétés Listener et de publication Web.</span><span class="sxs-lookup"><span data-stu-id="93d64-157">Close the Listener and Web Publishing properties.</span></span>

6.  <span data-ttu-id="93d64-158">Cliquez sur **appliquer** dans le volet Détails pour enregistrer les modifications et mettre à jour la configuration.</span><span class="sxs-lookup"><span data-stu-id="93d64-158">Click **Apply** in the details pane to save the changes and update the configuration.</span></span>

7.  <span data-ttu-id="93d64-159">Cliquez sur **règle de test** pour vérifier que la configuration de votre nouvelle règle est correcte.</span><span class="sxs-lookup"><span data-stu-id="93d64-159">Click **Test Rule** to verify that your new rule is set up correctly.</span></span>

</div>

<div>

## <a name="to-create-a-web-publishing-rule-for-port-80"></a><span data-ttu-id="93d64-160">Pour créer une règle de publication Web pour le port 80</span><span class="sxs-lookup"><span data-stu-id="93d64-160">To create a web publishing rule for port 80</span></span>

1.  <span data-ttu-id="93d64-161">Cliquez sur **Démarrer**, pointez sur **programmes**, sur **Microsoft Forefront TMG**, puis cliquez sur gestion de **Forefront TMG**.</span><span class="sxs-lookup"><span data-stu-id="93d64-161">Click **Start**, point to **Programs**, point to **Microsoft Forefront TMG**, and then click **Forefront TMG Management**.</span></span>

2.  <span data-ttu-id="93d64-162">Dans le volet gauche, développez **NomServeur**, cliquez avec le bouton droit sur **stratégie de pare-feu**, pointez sur **nouveau**, puis cliquez sur règle de **publication de site Web**.</span><span class="sxs-lookup"><span data-stu-id="93d64-162">In the left pane, expand **ServerName**, right-click **Firewall Policy**, point to **New**, and then click **Web Site Publishing Rule**.</span></span>

3.  <span data-ttu-id="93d64-163">Dans la page **Bienvenue dans la nouvelle règle de publication Web** , tapez un nom d’affichage pour la nouvelle règle de publication (par exemple, la découverte automatique LYNC (http)).</span><span class="sxs-lookup"><span data-stu-id="93d64-163">On the **Welcome to the New Web Publishing Rule** page, type a display name for the new publishing rule (for example, Lync Autodiscover (HTTP)).</span></span>

4.  <span data-ttu-id="93d64-164">Dans la page **Sélectionner une action de règle** , sélectionnez **autoriser**.</span><span class="sxs-lookup"><span data-stu-id="93d64-164">On the **Select Rule Action** page, select **Allow**.</span></span>

5.  <span data-ttu-id="93d64-165">Dans la page **type de publication** , sélectionnez **publier un site Web ou un équilibrage de charge unique**.</span><span class="sxs-lookup"><span data-stu-id="93d64-165">On the **Publishing Type** page, select **Publish a single Web site or load balancer**.</span></span>

6.  <span data-ttu-id="93d64-166">Dans la page sécurité de la **connexion au serveur** , sélectionnez utiliser des **connexions non sécurisées pour la connexion au serveur Web publié ou à la batterie de serveurs**.</span><span class="sxs-lookup"><span data-stu-id="93d64-166">On the **Server Connection Security** page, select **Use non-secured connections to connect to the published Web server or server farm**.</span></span>

7.  <span data-ttu-id="93d64-167">Dans la page Détails de la **publication interne** , dans **nom du site interne**, tapez l’adresse VIP de l’équilibrage de charge matérielle (HLB) en face du pool frontal.</span><span class="sxs-lookup"><span data-stu-id="93d64-167">On the **Internal Publishing Details** page, in **Internal Site name**, type the VIP address of the Hardware Load Balancer (HLB) in front of the Front End pool.</span></span>

8.  <span data-ttu-id="93d64-168">Dans la page Détails de la **publication interne** , dans **Path (facultatif)**, tapez **/ \* *_ en tant que chemin d’accès au dossier à publier, puis sélectionnez _* transférer l’en-tête d’hôte d’origine au lieu de celle spécifiée dans le champ nom du site interne**.</span><span class="sxs-lookup"><span data-stu-id="93d64-168">On the **Internal Publishing Details** page, in **Path (optional)**, type \**/\**_ as the path of the folder to be published, and then select _\* Forward the original host header instead of the one specified in the Internal site name field\*\*.</span></span>

9.  <span data-ttu-id="93d64-169">Dans la page **Détails du nom public** , procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="93d64-169">On the **Public Name Details** page, do the following:</span></span>
    
      - <span data-ttu-id="93d64-170">Sous **accepter les demandes pour**, sélectionnez **ce nom de domaine**.</span><span class="sxs-lookup"><span data-stu-id="93d64-170">Under **Accept Requests for**, select **This domain name**.</span></span>
    
      - <span data-ttu-id="93d64-171">Dans **nom public**, tapez **lyncdiscover.**\<sipdomain\></span><span class="sxs-lookup"><span data-stu-id="93d64-171">In **Public Name**, type **lyncdiscover.**\<sipdomain\></span></span> <span data-ttu-id="93d64-172">(URL du service de découverte automatique externe).</span><span class="sxs-lookup"><span data-stu-id="93d64-172">(the external Autodiscover Service URL).</span></span>
    
      - <span data-ttu-id="93d64-173">Dans **path**, tapez \* */\** _.</span><span class="sxs-lookup"><span data-stu-id="93d64-173">In **Path**, type \**/\** _.</span></span>

10. <span data-ttu-id="93d64-174">Sur _ *Sélectionnez écouteur Web*, dans l' **écouteur Web**, sélectionnez un écouteur Web ou utilisez l’Assistant Nouvelle définition d’écoute Web pour en créer un autre.</span><span class="sxs-lookup"><span data-stu-id="93d64-174">On _ *Select Web Listener*\* page, in **Web Listener**, select a Web Listener or use the New Web Listener Definition Wizard to create a new one.</span></span>

11. <span data-ttu-id="93d64-175">Dans la page **délégation d’authentification** , sélectionnez **aucune délégation, et le client ne peut pas s’authentifier directement**.</span><span class="sxs-lookup"><span data-stu-id="93d64-175">On the **Authentication Delegation** page, select **No delegation, and client cannot authenticate directly**.</span></span>

12. <span data-ttu-id="93d64-176">Dans la page **jeu d’utilisateurs** , sélectionnez tous les **utilisateurs**.</span><span class="sxs-lookup"><span data-stu-id="93d64-176">On the **User Set** page, select **All Users**.</span></span>

13. <span data-ttu-id="93d64-177">Dans la page **fin de l’Assistant Nouvelle règle de publication Web** , vérifiez que les paramètres de règle de publication Web sont corrects, puis cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="93d64-177">On the **Completing the New Web Publishing Rule Wizard** page, verify that the web publishing rule settings are correct, and then click **Finish**.</span></span>

14. <span data-ttu-id="93d64-178">Dans la liste de règles de publication Web de Forefront TMG, double-cliquez sur la nouvelle règle que vous venez d’ajouter pour ouvrir les **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="93d64-178">In the Forefront TMG list of web publishing rules, double-click the new rule you just added to open **Properties**.</span></span>

15. <span data-ttu-id="93d64-179">Dans l’onglet **pontage** , configurez les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="93d64-179">On the **Bridging** tab, configure the following:</span></span>
    
      - <span data-ttu-id="93d64-180">Sélectionnez **serveur Web**.</span><span class="sxs-lookup"><span data-stu-id="93d64-180">Select **Web server**.</span></span>
    
      - <span data-ttu-id="93d64-181">Sélectionnez **Rediriger les demandes vers le port http** et tapez **8080** pour le numéro de port.</span><span class="sxs-lookup"><span data-stu-id="93d64-181">Select **Redirect requests to HTTP port**, and type **8080** for the port number.</span></span>
    
      - <span data-ttu-id="93d64-182">Vérifiez que l’option **Rediriger les demandes vers le port SSL** n’est pas sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="93d64-182">Verify that **Redirect requests to SSL port** is not selected.</span></span>

16. <span data-ttu-id="93d64-183">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="93d64-183">Click **OK**.</span></span>

17. <span data-ttu-id="93d64-184">Cliquez sur **appliquer** dans le volet Détails pour enregistrer les modifications et mettre à jour la configuration.</span><span class="sxs-lookup"><span data-stu-id="93d64-184">Click **Apply** in the details pane to save the changes and update the configuration.</span></span>

18. <span data-ttu-id="93d64-185">Cliquez sur **règle de test** pour vérifier que la configuration de votre nouvelle règle est correcte.</span><span class="sxs-lookup"><span data-stu-id="93d64-185">Click **Test Rule** to verify that your new rule is set up correctly.</span></span>

19. <span data-ttu-id="93d64-186">Vérifiez que l’URL du service de découverte automatique externe n’est pas définie sur une autre règle de publication Web.</span><span class="sxs-lookup"><span data-stu-id="93d64-186">Verify that the external Autodiscover Service URL is not defined on any other web publishing rule.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="93d64-187">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="93d64-187">See Also</span></span>


[<span data-ttu-id="93d64-188">Configuration des serveurs proxy inverses pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="93d64-188">Setting up reverse proxy servers for Lync Server 2013</span></span>](lync-server-2013-setting-up-reverse-proxy-servers.md)  
[<span data-ttu-id="93d64-189">Exigences techniques pour la mobilité dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="93d64-189">Technical requirements for mobility in Lync Server 2013</span></span>](lync-server-2013-technical-requirements-for-mobility.md)  
  

<span data-ttu-id="93d64-190"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="93d64-190"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

