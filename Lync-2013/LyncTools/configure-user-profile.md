---
title: Configurer un profil utilisateur
description: Configurer le profil utilisateur.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Configure User Profile
ms:assetid: 52713245-e502-4539-a238-66ff1aca26b1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945594(v=OCS.15)
ms:contentKeyID: 51541419
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 682297da43797dd2d774094e85e8688ef3c64d98
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443676"
---
# <a name="configure-user-profile"></a><span data-ttu-id="19167-103">Configurer un profil utilisateur</span><span class="sxs-lookup"><span data-stu-id="19167-103">Configure User Profile</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="19167-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="19167-104">

<span> </span></span></span>

<span data-ttu-id="19167-105">_**Dernière modification de la rubrique :** 2018-10-11_</span><span class="sxs-lookup"><span data-stu-id="19167-105">_**Topic Last Modified:** 2018-10-11_</span></span>

<span data-ttu-id="19167-106">Les outils inclus dans le package d’outils de stress et de performance de Lync Server 2013 vous permettent de créer et de configurer des comptes d’utilisateurs test que vous pouvez utiliser pour effectuer des simulations de charge.</span><span class="sxs-lookup"><span data-stu-id="19167-106">The tools included in the Lync Server 2013 Stress and Performance Tool package enable you to create and configure test user accounts that you can use to run load simulations.</span></span> <span data-ttu-id="19167-107">Utilisez l’outil de création d’utilisateurs de Lync Server 2013 pour créer les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="19167-107">Use the Lync Server 2013 User Creation Tool to create the users.</span></span> <span data-ttu-id="19167-108">(Pour plus d’informations, consultez [créer des utilisateurs et des contacts](create-users-and-contacts.md).) Une fois les utilisateurs créés, configurez les profils utilisateur à l’aide de l’outil de configuration de chargement de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="19167-108">(For details, see [Create Users and Contacts](create-users-and-contacts.md).) After users are created, configure the user profiles by using the Lync Server 2013 Load Configuration Tool.</span></span>

<div>

## <a name="running-the-lync-server-2013-load-configuration-tool"></a><span data-ttu-id="19167-109">Exécution de l’outil de configuration de chargement de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="19167-109">Running the Lync Server 2013 Load Configuration Tool</span></span>

<span data-ttu-id="19167-110">Pour configurer les profils utilisateur, exécutez l’outil de configuration de chargement de Lync Server 2013 (UserProfileGenerator.exe), puis remplissez chacun des onglets.</span><span class="sxs-lookup"><span data-stu-id="19167-110">To configure user profiles, run the Lync Server 2013 Load Configuration Tool (UserProfileGenerator.exe) and fill out each of the tabs.</span></span> <span data-ttu-id="19167-111">UserProfileGenerator.exe génère un répertoire pour chaque ordinateur client dont vous avez besoin pour exécuter la simulation.</span><span class="sxs-lookup"><span data-stu-id="19167-111">UserProfileGenerator.exe generates a directory for each of the client computers that you need to run the simulation.</span></span> <span data-ttu-id="19167-112">Chaque annuaire client inclut également un script permettant de démarrer toutes les instances de l’outil de stress et de performance de Lync Server 2013 (LyncPerfTool.exe).</span><span class="sxs-lookup"><span data-stu-id="19167-112">Each client directory also comes with a script to start all the instances of the Lync Server 2013 Stress and Performance Tool (LyncPerfTool.exe).</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="19167-113">Les valeurs spécifiques à l’utilisateur spécifiées dans UserProfileGenerator doivent correspondre aux valeurs spécifiées dans l’outil de création d’utilisateurs de Lync Server 2013 (UserProvisioningTool) pour le pool.</span><span class="sxs-lookup"><span data-stu-id="19167-113">The user-specific values specified in UserProfileGenerator must match the values specified in the Lync Server 2013 User Creation Tool (UserProvisioningTool) for the pool.</span></span>



</div>

<span data-ttu-id="19167-114">Renseignez les champs de chaque onglet de l’outil de configuration de chargement de Lync Server 2013, comme décrit dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="19167-114">Fill in the fields on each tab of the Lync Server 2013 Load Configuration Tool, as described in the following sections.</span></span>

<div>

## <a name="common-configuration"></a><span data-ttu-id="19167-115">Configuration courante</span><span class="sxs-lookup"><span data-stu-id="19167-115">Common Configuration</span></span>

<span data-ttu-id="19167-116">L’onglet **configuration commune** de l’outil de configuration de chargement de Lync Server 2013 est illustré dans la figure ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="19167-116">The **Common Configuration** tab of the Lync Server 2013 Load Configuration Tool is shown in the following figure.</span></span> <span data-ttu-id="19167-117">Remplissez les champs de l’onglet **configuration courante** , comme décrit dans les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="19167-117">Fill in the fields of the **Common Configuration** tab, as described in the following steps.</span></span>

<span data-ttu-id="19167-118">![Onglet Configuration commune.](images/JJ945594.c68dcc8f-10f2-499e-95a2-fccbcc206c2f(OCS.15).jpg "Onglet Configuration commune.")</span><span class="sxs-lookup"><span data-stu-id="19167-118">![Common Configuration tab.](images/JJ945594.c68dcc8f-10f2-499e-95a2-fccbcc206c2f(OCS.15).jpg "Common Configuration tab.")</span></span>

1.  <span data-ttu-id="19167-119">Dans **nombre d’ordinateurs disponibles**, tapez ou cliquez sur le nombre d’ordinateurs que vous voulez utiliser pour exécuter LyncPerfTool.exe.</span><span class="sxs-lookup"><span data-stu-id="19167-119">In **Number of Available Machines**, type or click the number of computers that you want to use to run LyncPerfTool.exe.</span></span> <span data-ttu-id="19167-120">Nous vous recommandons d’avoir un ordinateur pour tous les utilisateurs de 4 500 que vous allez simuler.</span><span class="sxs-lookup"><span data-stu-id="19167-120">We recommend that you have one computer for every 4,500 users that you will be simulating.</span></span> <span data-ttu-id="19167-121">Ce nombre peut varier si vous réduisez le niveau de charge ou si vous utilisez uniquement un sous-ensemble des fonctionnalités disponibles.</span><span class="sxs-lookup"><span data-stu-id="19167-121">That number may vary if you reduce the load level or if you use only a subset of the available features.</span></span> <span data-ttu-id="19167-122">(Les niveaux de charge sont définis sous l’onglet **scénarios généraux** .)</span><span class="sxs-lookup"><span data-stu-id="19167-122">(Load levels are set on the **General Scenarios** tab.)</span></span>

2.  <span data-ttu-id="19167-123">Dans **préfixe pour noms d’utilisateur**, tapez le préfixe correspondant au nom d’utilisateur des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="19167-123">In **Prefix for User Names**, type the prefix for the user name of the users.</span></span> <span data-ttu-id="19167-124">Pour vous connecter, il s’agit de l’URI (Uniform Resource Identifier) : UserPrefix de début de l' \[ utilisateur... (Nombre d’utilisateurs-1) \] @User domaine.</span><span class="sxs-lookup"><span data-stu-id="19167-124">To log in, the Uniform Resource Identifier (URI) will be: UserPrefix\[User Start Index…(Number Of Users-1)\]@User Domain.</span></span>

3.  <span data-ttu-id="19167-125">Dans **mot de passe pour tous les utilisateurs**, entrez le mot de passe utilisé pour créer les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="19167-125">In **Password for All Users**, enter the password that was used for creating the users.</span></span> <span data-ttu-id="19167-126">Si vous laissez ce champ vide, le nom d’utilisateur sera utilisé comme mot de passe.</span><span class="sxs-lookup"><span data-stu-id="19167-126">If you leave this field empty, the username will be used as the password.</span></span>

4.  <span data-ttu-id="19167-127">Dans **index de début** de l’utilisateur, cliquez ou tapez l’index du premier utilisateur à configurer.</span><span class="sxs-lookup"><span data-stu-id="19167-127">In **User Start Index**, click or type the index of the first user to be configured.</span></span> <span data-ttu-id="19167-128">Vous pouvez configurer différentes plages pour différents types ou niveaux de charge, mais vous devez exécuter UserProfileGenerator.exe une fois par plage que vous souhaitez configurer.</span><span class="sxs-lookup"><span data-stu-id="19167-128">You can configure different ranges for different types or levels of load, but you must run UserProfileGenerator.exe once per the range that you want to configure.</span></span>

5.  <span data-ttu-id="19167-129">Dans **nombre d’utilisateurs**, cliquez ou tapez le nombre total d’utilisateurs que vous allez configurer.</span><span class="sxs-lookup"><span data-stu-id="19167-129">In **Number of Users**, click or type the total number of users you are going to configure.</span></span>

6.  <span data-ttu-id="19167-130">Dans **domaine** de l’utilisateur, tapez le domaine utilisé pour l’URI SIP.</span><span class="sxs-lookup"><span data-stu-id="19167-130">In **User Domain**, type the domain used for the SIP URI.</span></span> <span data-ttu-id="19167-131">Il est utilisé pour créer l’URI SIP de chaque utilisateur pour se connecter au serveur frontal Lync Server 2013 ou Standard Edition Server.</span><span class="sxs-lookup"><span data-stu-id="19167-131">This is used to construct the SIP URI of each user to log on to the Lync Server 2013 Front End Server or Standard Edition server.</span></span> <span data-ttu-id="19167-132">Il peut être différent du domaine du compte.</span><span class="sxs-lookup"><span data-stu-id="19167-132">It can be different from the account domain.</span></span>

7.  <span data-ttu-id="19167-133">Dans **domaine de compte**, tapez la connexion au domaine AD FS (Active Directory Domain Services).</span><span class="sxs-lookup"><span data-stu-id="19167-133">In **Account Domain**, type the Active Directory Domain Services domain logon.</span></span>

8.  <span data-ttu-id="19167-134">Entrez le nombre maximal de points de terminaison concurrents en **se connectant par seconde (par instance)** pour lesquels vous voulez que l’outil se connecte à tous les points de terminaison/utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="19167-134">Enter the maximum number of concurrent endpoints in **Sign In Per Second (per instance)** for which you want the tool to log in all the endpoints/users.</span></span> <span data-ttu-id="19167-135">Le taux recommandé est \< = 2 par seconde/standard PT.</span><span class="sxs-lookup"><span data-stu-id="19167-135">The recommended rate is \<=2 per second/standard SKU FE.</span></span>

9.  <span data-ttu-id="19167-136">Dans **proxy d’accès ou nom de domaine complet du pool**, tapez le nom de domaine complet (FQDN) du serveur auquel vous souhaitez que les clients se connectent.</span><span class="sxs-lookup"><span data-stu-id="19167-136">In **Access Proxy or Pool FQDN**, type the fully qualified domain name (FQDN) of the server that you want the clients to connect to.</span></span> <span data-ttu-id="19167-137">Si les utilisateurs se connectent en externe, spécifiez le proxy d’accès.</span><span class="sxs-lookup"><span data-stu-id="19167-137">If the users are logging on externally, specify the access proxy.</span></span> <span data-ttu-id="19167-138">Si les utilisateurs sont internes, spécifiez le nom de domaine complet (FQDN) du pool ou du serveur Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="19167-138">If the users are internal, specify the FQDN of their pool or Standard Edition server.</span></span>

10. <span data-ttu-id="19167-139">Dans **port**, cliquez ou tapez le port que les utilisateurs utiliseront pour SIP (la valeur par défaut est 5061).</span><span class="sxs-lookup"><span data-stu-id="19167-139">In **Port**, click or type the port that you want users to use for SIP (the default is 5061).</span></span>

<span data-ttu-id="19167-140">Pour les paramètres de serveur de réseau externe, spécifiez le **nom de domaine complet du proxy ou du pool d’accès** et le **port**.</span><span class="sxs-lookup"><span data-stu-id="19167-140">For External Network Server Settings, specify the **Access Proxy or Pool FQDN** and the **Port**.</span></span> <span data-ttu-id="19167-141">Ces paramètres sont utilisés uniquement pour la simulation de charge de points de terminaison externes.</span><span class="sxs-lookup"><span data-stu-id="19167-141">These settings are used only for External endpoints load simulation.</span></span>

</div>

<div>

## <a name="general-scenarios"></a><span data-ttu-id="19167-142">Scénarios généraux</span><span class="sxs-lookup"><span data-stu-id="19167-142">General Scenarios</span></span>

<span data-ttu-id="19167-143">L’onglet **scénarios généraux** de l’outil de configuration de chargement de Lync Server 2013 est présenté dans la figure ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="19167-143">The **General Scenarios** tab of the Lync Server 2013 Load Configuration Tool is shown in the following figure.</span></span>

<span data-ttu-id="19167-144">Configurez les niveaux de charge et les paramètres pour chacun des scénarios généraux que vous souhaitez exécuter, ou laissez-le désactivé.</span><span class="sxs-lookup"><span data-stu-id="19167-144">Configure the load levels and parameters for each of the general scenarios that you want to run, or leave disabled.</span></span>

<span data-ttu-id="19167-145">![Onglet scénarios généraux.](images/JJ945594.4f046d39-b532-4baf-99a6-c89d1d6d1fcc(OCS.15).jpg "Onglet scénarios généraux.")</span><span class="sxs-lookup"><span data-stu-id="19167-145">![General Scenarios tab.](images/JJ945594.4f046d39-b532-4baf-99a6-c89d1d6d1fcc(OCS.15).jpg "General Scenarios tab.")</span></span>

1.  <span data-ttu-id="19167-146">Dans la **messagerie instantanée**, qui inclut les services d’égal à égal et de conférence, spécifiez la valeur appropriée pour le niveau de charge.</span><span class="sxs-lookup"><span data-stu-id="19167-146">In **Instant Messaging**, which includes peer-to-peer and conferencing, specify the appropriate value for the Load Level.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="19167-147">Les valeurs de niveau de charge de tous les champs (à l’exception des services d’informations de lieu) sont <STRONG>désactivées</STRONG>, <STRONG>faible</STRONG>, <STRONG>moyenne</STRONG>, <STRONG>haute</STRONG>et <STRONG>personnalisée</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="19167-147">Load level values for all fields (except Location Information Services) are <STRONG>Disabled</STRONG>, <STRONG>Low</STRONG>, <STRONG>Medium</STRONG>, <STRONG>High</STRONG>, and <STRONG>Custom</STRONG>.</span></span> <span data-ttu-id="19167-148">Lorsque les valeurs faible, moyenne, haute ou personnalisée sont sélectionnées, des configurations sont générées pour chaque modalité et chaque client.</span><span class="sxs-lookup"><span data-stu-id="19167-148">When Low, Medium, High, or Custom is selected, configurations will be generated for each modality and client.</span></span> <span data-ttu-id="19167-149">Élevé entraîne la génération de la valeur maximale prise en charge pour le serveur, moyenne correspond à 60% du chargement et la valeur basse correspond à 30% du chargement.</span><span class="sxs-lookup"><span data-stu-id="19167-149">High will result in the maximum supported load to be generated for the server, Medium corresponds to 60 percent of the load, and Low corresponds to 30 percent of the load.</span></span>

    
    </div>

2.  <span data-ttu-id="19167-150">Dans **audioconférence**, qui est le niveau de conférences audio uniquement, spécifiez la valeur appropriée pour le niveau de charge.</span><span class="sxs-lookup"><span data-stu-id="19167-150">In **Audio Conferencing**, which is audio conferencing only, specify the appropriate value for Load Level.</span></span> <span data-ttu-id="19167-151">Les appels d’égal à égal sont abordés dans la section scénarios vocaux, plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="19167-151">Peer-to-peer calls are covered in the Voice Scenarios section later in this topic.</span></span> <span data-ttu-id="19167-152">Pour activer multivue, ouvrez l’onglet **avancé** pour cette modalité.</span><span class="sxs-lookup"><span data-stu-id="19167-152">To enable MultiView, open the **Advanced** tab for that modality.</span></span>

3.  <span data-ttu-id="19167-153">Dans **partage d’application**, spécifiez la valeur appropriée pour le niveau de charge.</span><span class="sxs-lookup"><span data-stu-id="19167-153">In **Application Sharing**, specify the appropriate value for Load Level.</span></span>

4.  <span data-ttu-id="19167-154">Dans la **collaboration de données**, qui inclut les conférences de données, spécifiez la valeur appropriée pour le niveau de charge.</span><span class="sxs-lookup"><span data-stu-id="19167-154">In **Data Collaboration**, which includes data conferencing, specify the appropriate value for Load Level.</span></span>

5.  <span data-ttu-id="19167-155">Dans **extension** de la liste de distribution, spécifiez la valeur appropriée pour le niveau de charge.</span><span class="sxs-lookup"><span data-stu-id="19167-155">In **Distribution List Expansion**, specify the appropriate value for Load Level.</span></span> <span data-ttu-id="19167-156">Vous devez également cliquer sur le bouton **avancé** , puis renseigner les champs avec les mêmes valeurs que celles configurées sous l’onglet **liste de distribution** de l’outil de création d’utilisateurs de Lync Server (UserProvisioningTool.exe).</span><span class="sxs-lookup"><span data-stu-id="19167-156">You must also click the **Advanced** button, and then fill in the fields with the same values that you configured on the **Distribution List** tab of the Lync Server User Creation Tool (UserProvisioningTool.exe).</span></span> <span data-ttu-id="19167-157">Pour plus d’informations sur ces champs, voir [créer des utilisateurs et des contacts](create-users-and-contacts.md) .</span><span class="sxs-lookup"><span data-stu-id="19167-157">For details about these fields, see [Create Users and Contacts](create-users-and-contacts.md)</span></span>

6.  <span data-ttu-id="19167-158">Dans la **requête Web du carnet d'** adresses, qui est le service de recherche dans le carnet d’adresses (et non le téléchargement du fichier du carnet d’adresses), spécifiez la valeur appropriée pour le niveau de charge.</span><span class="sxs-lookup"><span data-stu-id="19167-158">In **Address Book Web Query**, which is the address book lookup service (not the address book file download), specify the appropriate value for Load Level.</span></span> <span data-ttu-id="19167-159">Pour activer les téléchargements du carnet d’adresses, cliquez sur le bouton **avancé** correspondant, puis affectez à **EnableABSDownload** la valeur true.</span><span class="sxs-lookup"><span data-stu-id="19167-159">To enable address book downloads, click the corresponding **Advanced** button, and then set **EnableABSDownload** to true.</span></span>

7.  <span data-ttu-id="19167-160">Dans **service Response Group**, spécifiez la valeur appropriée pour le niveau de charge.</span><span class="sxs-lookup"><span data-stu-id="19167-160">In **Response Group Service**, specify the appropriate value for Load Level.</span></span> <span data-ttu-id="19167-161">Vous devez également cliquer sur le bouton **avancé** correspondant, puis spécifier les URI des groupes de réponse que vous avez déjà créés lors de la mise en service des agents de groupe de réponse.</span><span class="sxs-lookup"><span data-stu-id="19167-161">You must also click the corresponding **Advanced** button, and then specify the URIs of the response groups you have already created when provisioning Response Group Service agents.</span></span> <span data-ttu-id="19167-162">Vous devez spécifier au moins un groupe de réponse.</span><span class="sxs-lookup"><span data-stu-id="19167-162">You must specify at least one response group.</span></span> <span data-ttu-id="19167-163">Utilisez des points-virgules pour séparer plusieurs groupes de réponse.</span><span class="sxs-lookup"><span data-stu-id="19167-163">Use semicolons to separate multiple response groups.</span></span> <span data-ttu-id="19167-164">Mettez à jour RGSUriSuffixStartIndex et RGSUriSuffixEndIndex sur les valeurs réelles.</span><span class="sxs-lookup"><span data-stu-id="19167-164">Update RGSUriSuffixStartIndex and RGSUriSuffixEndIndex to the actual values.</span></span>

8.  <span data-ttu-id="19167-165">Dans **services d’information d’emplacement**, sélectionnez la valeur appropriée pour le niveau de charge.</span><span class="sxs-lookup"><span data-stu-id="19167-165">In **Location Information Services**, select the appropriate value for Load Level.</span></span> <span data-ttu-id="19167-166">Le niveau de charge des services d’information d’emplacement doit être **activé** ou **désactivé**.</span><span class="sxs-lookup"><span data-stu-id="19167-166">The load level for Location Information Services must be **Enabled** or **Disabled**.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="19167-167">Chacun des scénarios est associé à un bouton <STRONG>avancé</STRONG> qui s’affiche à côté de celui-ci, ainsi qu’un ensemble de cases à cocher permettant de définir des variations des scénarios.</span><span class="sxs-lookup"><span data-stu-id="19167-167">Each of the scenarios has an <STRONG>Advanced</STRONG> button located next to it, and a set of check boxes that enable variations of the scenarios.</span></span> <span data-ttu-id="19167-168">Moyens <STRONG>ad-hoc</STRONG> pour générer une simulation de conférences qui seront créées tout au long de l’heure.</span><span class="sxs-lookup"><span data-stu-id="19167-168"><STRONG>Ad-hoc</STRONG> means to generate simulation of conferences that will be created throughout the hour.</span></span> <span data-ttu-id="19167-169">L’environnement de <STRONG>grande taille</STRONG> signifie que le scénario de conférence sera simulé.</span><span class="sxs-lookup"><span data-stu-id="19167-169"><STRONG>Large Conf</STRONG> means that Large Conference Scenario will be simulated.</span></span> <span data-ttu-id="19167-170"><STRONG>Externe</STRONG> signifie également simuler des utilisateurs externes.</span><span class="sxs-lookup"><span data-stu-id="19167-170"><STRONG>External</STRONG> means to also simulate external users.</span></span><BR><span data-ttu-id="19167-171">Ces boutons et cases à cocher autorisent l’accès à des valeurs propres à chaque scénario, qui modifient le comportement de l’outil de stress et de performance de Lync Server 2013 (LyncPerfTool) et permettent la personnalisation possible.</span><span class="sxs-lookup"><span data-stu-id="19167-171">These buttons and check boxes allow access to values specific to each scenario that will change the behavior of the Lync Server 2013 Stress and Performance Tool (LyncPerfTool) and make customization possible.</span></span> <span data-ttu-id="19167-172">Pour chaque scénario sous l’onglet <STRONG>scénarios généraux</STRONG> (à l’exception de services d’information d’emplacement), si la valeur de niveau de charge est <STRONG>personnalisé</STRONG>, le taux de conversation est calculé à l’aide du champ correspondant dans la boîte de dialogue <STRONG>avancé</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="19167-172">For each scenario on the <STRONG>General Scenarios</STRONG> tab (except for Location Information Services), if the value of Load Level is <STRONG>Custom</STRONG>, then the conversation rate will be calculated using the corresponding field in the <STRONG>Advanced</STRONG> dialog box.</span></span> <span data-ttu-id="19167-173">Le nom du champ est différent selon le scénario, mais la description du champ indique le message suivant : « Remarque : ce numéro sera utilisé uniquement si personnalisé est sélectionné dans le menu déroulant. »</span><span class="sxs-lookup"><span data-stu-id="19167-173">The field name differs, depending on the scenario, but the field description will state, "NOTE: This number will only be used if Custom is selected from the drop-down menu."</span></span> <span data-ttu-id="19167-174">En règle générale, les valeurs <STRONG>élevé</STRONG>, <STRONG>moyen</STRONG>et <STRONG>faible</STRONG> modifient les taux de conversation par modalité en fonction du modèle utilisateur qui est un bilan de tous les scénarios.</span><span class="sxs-lookup"><span data-stu-id="19167-174">In general, the values <STRONG>High</STRONG>, <STRONG>Medium</STRONG>, and <STRONG>Low</STRONG> will alter the conversation rates per modality in line with the User Model that is a balance of all the scenarios.</span></span> <span data-ttu-id="19167-175">S’il est nécessaire de modifier le niveau de charge par modalité en raison d’une différence d’utilisation prévue, nous vous recommandons d’utiliser une fréquence de conversation <STRONG>personnalisée</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="19167-175">If there is a need to change the load level per modality due to a difference in expected usage, we recommend using a <STRONG>Custom</STRONG> conversation rate.</span></span><BR>



</div>

</div>

<div>

## <a name="voice-scenarios"></a><span data-ttu-id="19167-176">Scénarios vocaux</span><span class="sxs-lookup"><span data-stu-id="19167-176">Voice Scenarios</span></span>

<span data-ttu-id="19167-177">L’onglet **scénarios vocaux** de l’outil de configuration de chargement de Lync Server 2013 est présenté dans la figure ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="19167-177">The **Voice Scenarios** tab of the Lync Server 2013 Load Configuration Tool is shown in the following figure.</span></span>

<span data-ttu-id="19167-178">Utilisez l’onglet **scénarios vocaux** pour configurer tous les scénarios liés à la voix.</span><span class="sxs-lookup"><span data-stu-id="19167-178">Use the **Voice Scenarios** tab to configure all of the voice-related scenarios.</span></span>

<span data-ttu-id="19167-179">![Onglet scénarios vocaux.](images/JJ945594.28edf664-da59-40b0-9a0e-196f01e9ca86(OCS.15).jpg "Onglet scénarios vocaux.")</span><span class="sxs-lookup"><span data-stu-id="19167-179">![Voice Scenarios tab.](images/JJ945594.28edf664-da59-40b0-9a0e-196f01e9ca86(OCS.15).jpg "Voice Scenarios tab.")</span></span>

1.  <span data-ttu-id="19167-180">Dans **VoIP**, cliquez sur le bouton **avancé** , puis spécifiez des valeurs pour les champs **PhoneAreaCode** et **LocationProfile** (plan de numérotation).</span><span class="sxs-lookup"><span data-stu-id="19167-180">In **VoIP**, click the **Advanced** button, and then provide values for the **PhoneAreaCode** and **LocationProfile** (dial plan) fields.</span></span> <span data-ttu-id="19167-181">Vous devez également spécifier une valeur pour le **niveau de charge**.</span><span class="sxs-lookup"><span data-stu-id="19167-181">You must also specify a value for **Load Level**.</span></span> <span data-ttu-id="19167-182">Si le niveau de **VoIP** charge des **passerelles VoIP et RTC/PSTN** est activé, un fichier de configuration de réseau téléphonique commuté (PSTN) vers des communications unifiées (UC) est toujours généré qui simule des appels externes.</span><span class="sxs-lookup"><span data-stu-id="19167-182">If Load Level for **VoIP** and **UC/PSTN Gateway** is Enabled, then a public switched telephone network (PSTN) to unified communications (UC) configuration file will always be generated that will simulate external calls.</span></span>

2.  <span data-ttu-id="19167-183">Dans **passerelle UC/PSTN**, spécifiez une valeur pour niveau de charge.</span><span class="sxs-lookup"><span data-stu-id="19167-183">In **UC/PSTN Gateway**, specify a value for Load Level.</span></span> <span data-ttu-id="19167-184">Si vous sélectionnez un niveau de charge différent de **désactivé**, vous devez indiquer une valeur pour le **Code de zone RTC** en cliquant sur le bouton **Ajouter** sous serveur de médiation et RTC.</span><span class="sxs-lookup"><span data-stu-id="19167-184">If you select a load level other than **Disabled**, you must supply a value for **PSTN Area Code** by clicking the **Add** button under Mediation Server and PSTN.</span></span> <span data-ttu-id="19167-185">Vérifiez que vous disposez d’un itinéraire configuré pour ce code de zone.</span><span class="sxs-lookup"><span data-stu-id="19167-185">Verify that you have a route configured for that area code.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="19167-186">Vous pouvez utiliser le panneau de configuration de Lync Server ou Lync Server Management Shell pour vérifier la configuration des itinéraires vocaux.</span><span class="sxs-lookup"><span data-stu-id="19167-186">You can use either the Lync Server Control Panel or the Lync Server Management Shell to verify voice route configuration.</span></span>

    
    </div>

3.  <span data-ttu-id="19167-187">Dans le **surveillant de conférences**, spécifiez une valeur pour le niveau de charge.</span><span class="sxs-lookup"><span data-stu-id="19167-187">In **Conferencing Attendant**, specify a value for Load Level.</span></span> <span data-ttu-id="19167-188">Le choix d’un niveau de charge (différent de **désactivé**) permettra d’activer le champ **numéro de téléphone** .</span><span class="sxs-lookup"><span data-stu-id="19167-188">Selecting a load level (other than **Disabled**) will enable the **Telephone Number** field.</span></span> <span data-ttu-id="19167-189">Entrez le numéro de téléphone du standard automatique que vous souhaitez utiliser.</span><span class="sxs-lookup"><span data-stu-id="19167-189">Enter the telephone number of the Auto Attendant that you want to use.</span></span> <span data-ttu-id="19167-190">Cliquez sur le bouton **avancé** , puis spécifiez une valeur pour le champ **LocationProfile** .</span><span class="sxs-lookup"><span data-stu-id="19167-190">Also, click the **Advanced** button, and then specify a value for the **LocationProfile** field.</span></span>

4.  <span data-ttu-id="19167-191">Dans **service de parc d’appels**, spécifiez la valeur appropriée pour le **niveau de charge**.</span><span class="sxs-lookup"><span data-stu-id="19167-191">In **Call Park Service**, specify the appropriate value for **Load Level**.</span></span>

5.  <span data-ttu-id="19167-192">Sur le **serveur de médiation et sur PSTN**, pour chaque serveur de médiation que vous souhaitez utiliser, vous devez disposer d’un simulateur PSTN distinct.</span><span class="sxs-lookup"><span data-stu-id="19167-192">In **Mediation Server and PSTN**, for each Mediation Server that you want to use, you must have a separate PSTN simulator.</span></span> <span data-ttu-id="19167-193">Une fois que vous avez déterminé le client que vous allez utiliser comme simulateur, vous devez configurer votre serveur de médiation pour router les appels vers cet ordinateur sur le port de simulateur PSTN que vous avez configuré.</span><span class="sxs-lookup"><span data-stu-id="19167-193">After you have determined which client you are going to use as the simulator, you need to configure your Mediation Server to route calls to that computer on the PSTN Simulator port that you configured.</span></span> <span data-ttu-id="19167-194">Cliquez sur **Ajouter** pour configurer la valeur du serveur de médiation.</span><span class="sxs-lookup"><span data-stu-id="19167-194">Click **Add** to configure the value for the Mediation Server.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="19167-195">Dans chacun des scénarios, un bouton <STRONG>avancé</STRONG> est placé en regard.</span><span class="sxs-lookup"><span data-stu-id="19167-195">Each of the scenarios has an <STRONG>Advanced</STRONG> button located next to it.</span></span> <span data-ttu-id="19167-196">Ces boutons autorisent l’accès à des valeurs propres à chaque scénario, qui changeront le comportement de l’outil de stress et de performance de Lync Server 2013 (LyncPerfTool), et activez la personnalisation.</span><span class="sxs-lookup"><span data-stu-id="19167-196">These buttons allow access to values specific to each scenario that will change the behavior of the Lync Server 2013 Stress and Performance Tool (LyncPerfTool) and enable customization.</span></span> <span data-ttu-id="19167-197">Pour chaque scénario sous l’onglet <STRONG>scénarios vocaux</STRONG> , si la valeur de <STRONG>niveau de charge</STRONG> est <STRONG>personnalisée</STRONG>, le taux de conversation est calculé à l’aide du champ correspondant dans la boîte de dialogue <STRONG>avancé</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="19167-197">For each scenario on the <STRONG>Voice Scenarios</STRONG> tab, if the value of <STRONG>Load Level</STRONG> is <STRONG>Custom</STRONG>, then the conversation rate will be calculated by using the corresponding field in the <STRONG>Advanced</STRONG> dialog box.</span></span> <span data-ttu-id="19167-198">Le nom du champ est différent selon le scénario, mais la description du champ indique le message suivant : « Remarque : ce numéro sera utilisé uniquement si personnalisé est sélectionné dans le menu déroulant. »</span><span class="sxs-lookup"><span data-stu-id="19167-198">The field name differs, depending on the scenario, but the field description will state, "NOTE: This number will only be used if Custom is selected from the drop-down menu."</span></span>



</div>

</div>

<div>

## <a name="reach"></a><span data-ttu-id="19167-199">Arrivez</span><span class="sxs-lookup"><span data-stu-id="19167-199">Reach</span></span>

<span data-ttu-id="19167-200">La fonction joindre est une nouvelle interface de Lync Server 2013 qui prend en charge les scénarios de conférence via le serveur UCWA (Unified Communications Web API) installé sur le serveur Front-End.</span><span class="sxs-lookup"><span data-stu-id="19167-200">Reach is a new experience in Lync Server 2013 that supports conferencing scenarios through the Unified Communications Web API (UCWA) server that is installed on the Front-End server.</span></span> <span data-ttu-id="19167-201">L’onglet **joindre** de l’outil de configuration de chargement de Lync Server 2013 est illustré dans la figure suivante.</span><span class="sxs-lookup"><span data-stu-id="19167-201">The **Reach** tab of the Lync Server 2013 Load Configuration Tool is shown in the following figure.</span></span>

<span data-ttu-id="19167-202">Utilisez l’onglet **joindre** pour configurer tous les scénarios liés à la portée.</span><span class="sxs-lookup"><span data-stu-id="19167-202">Use the **Reach** tab to configure all the reach-related scenarios.</span></span>

<span data-ttu-id="19167-203">![Onglet joindre](images/JJ945594.65ccf6de-0e8d-47ba-93f3-9dcb39d3fd62(OCS.15).jpg "Onglet joindre")</span><span class="sxs-lookup"><span data-stu-id="19167-203">![Reach tab.](images/JJ945594.65ccf6de-0e8d-47ba-93f3-9dcb39d3fd62(OCS.15).jpg "Reach tab.")</span></span>

1.  <span data-ttu-id="19167-204">Cliquez sur le bouton **avancé** en regard de **paramètres d’atteinte générale**.</span><span class="sxs-lookup"><span data-stu-id="19167-204">Click the **Advanced** button next to **General Reach Settings**.</span></span> <span data-ttu-id="19167-205">Définissez le champ **UcwaTargetServerUrl** sur l’adresse IP virtuelle du pool de réalisateurs ou le VIP du pool frontal.</span><span class="sxs-lookup"><span data-stu-id="19167-205">Set the field **UcwaTargetServerUrl** to the Director pool virtual IP (VIP) or the Front End pool VIP.</span></span>

2.  <span data-ttu-id="19167-206">Dans **partage d’application**, **collaboration de données** et **messagerie instantanée**, sélectionnez la valeur appropriée pour le **niveau de charge**.</span><span class="sxs-lookup"><span data-stu-id="19167-206">In **Application Sharing**, **Data Collaboration**, and **IM**, select the appropriate value for **Load Level**.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="19167-207">Dans chacun des scénarios, un bouton <STRONG>avancé</STRONG> est placé en regard.</span><span class="sxs-lookup"><span data-stu-id="19167-207">Each of the scenarios has an <STRONG>Advanced</STRONG> button located next to it.</span></span> <span data-ttu-id="19167-208">Ces boutons autorisent l’accès à des valeurs propres à chaque scénario, qui changeront le comportement de l’outil de stress et de performance de Lync Server 2013 (LyncPerfTool), et activez la personnalisation.</span><span class="sxs-lookup"><span data-stu-id="19167-208">These buttons allow access to values specific to each scenario that will change the behavior of the Lync Server 2013 Stress and Performance Tool (LyncPerfTool) and enable customization.</span></span> <span data-ttu-id="19167-209">Pour chacun des scénarios d’atteinte, si le <STRONG>niveau de charge</STRONG> est <STRONG>personnalisé</STRONG>, la valeur spécifiée dans le champ <STRONG>ConversationsPerHour</STRONG> est utilisée à la place de la valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="19167-209">For each of the Reach scenarios, if the <STRONG>Load Level</STRONG> is <STRONG>Custom</STRONG>, then the value specified in the <STRONG>ConversationsPerHour</STRONG> field is used instead of the default</span></span>



</div>

<span data-ttu-id="19167-210">Utilisez l’onglet **mobilité** pour configurer tous les scénarios liés à la mobilité.</span><span class="sxs-lookup"><span data-stu-id="19167-210">Use the **Mobility** tab to configure all of the mobility-related scenarios.</span></span>

<span data-ttu-id="19167-211">![Onglet mobilité.](images/JJ945594.4dd8f3e0-921c-48a5-8b23-2a0330d3c334(OCS.15).jpg "Onglet mobilité.")</span><span class="sxs-lookup"><span data-stu-id="19167-211">![Mobility tab.](images/JJ945594.4dd8f3e0-921c-48a5-8b23-2a0330d3c334(OCS.15).jpg "Mobility tab.")</span></span>

1.  <span data-ttu-id="19167-212">Cliquez sur le bouton **avancé** en regard de **mobilité (UCWA)**.</span><span class="sxs-lookup"><span data-stu-id="19167-212">Click the **Advanced** button next to **Mobility (UCWA)**.</span></span> <span data-ttu-id="19167-213">Définissez le champ **UcwaTargetServerUrl** sur l’adresse IP virtuelle du pool de réalisateurs ou le VIP du pool frontal.</span><span class="sxs-lookup"><span data-stu-id="19167-213">Set the field **UcwaTargetServerUrl** to the Director pool virtual IP (VIP) or the Front End pool VIP.</span></span>

2.  <span data-ttu-id="19167-214">Sur le **\\ son de présence et de messagerie instantanée P2P**, sélectionnez la valeur appropriée pour **niveau de charge** pour activer la simulation de scénarios de mobilité.</span><span class="sxs-lookup"><span data-stu-id="19167-214">In **Presence and P2P Instant Messaging\\Audio**, select the appropriate value for **Load Level** to enable Mobility Scenario simulation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="19167-215">Dans chacun des scénarios, un bouton <STRONG>avancé</STRONG> est placé en regard.</span><span class="sxs-lookup"><span data-stu-id="19167-215">Each of the scenarios has an <STRONG>Advanced</STRONG> button located next to it.</span></span> <span data-ttu-id="19167-216">Ces boutons autorisent l’accès à des valeurs propres à chaque scénario, qui changeront le comportement de l’outil de stress et de performance de Lync Server 2013 (LyncPerfTool), et activez la personnalisation.</span><span class="sxs-lookup"><span data-stu-id="19167-216">These buttons allow access to values specific to each scenario that will change the behavior of the Lync Server 2013 Stress and Performance Tool (LyncPerfTool) and enable customization.</span></span> <span data-ttu-id="19167-217">Pour chacun des scénarios d’atteinte, si le <STRONG>niveau de charge</STRONG> est <STRONG>personnalisé</STRONG>, la valeur spécifiée dans le champ <STRONG>ConversationsPerHour</STRONG> est utilisée à la place de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="19167-217">For each of the Reach scenarios, if the <STRONG>Load Level</STRONG> is <STRONG>Custom</STRONG>, then the value specified in the <STRONG>ConversationsPerHour</STRONG> field is used instead of the default.</span></span>



</div>

</div>

<div>

## <a name="summary"></a><span data-ttu-id="19167-218">Résumé</span><span class="sxs-lookup"><span data-stu-id="19167-218">Summary</span></span>

<span data-ttu-id="19167-219">L’onglet **Résumé** de l’outil de configuration de chargement de Lync Server 2013 est illustré dans la figure ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="19167-219">The **Summary** tab of the Lync Server 2013 Load Configuration Tool is shown in the following figure.</span></span>

<span data-ttu-id="19167-220">![Onglet Résumé.](images/JJ945594.c675e869-8ded-4195-8c2a-68d844fc96ad(OCS.15).jpg "Onglet Résumé.")</span><span class="sxs-lookup"><span data-stu-id="19167-220">![Summary tab.](images/JJ945594.c675e869-8ded-4195-8c2a-68d844fc96ad(OCS.15).jpg "Summary tab.")</span></span>

<span data-ttu-id="19167-221">L’onglet **Résumé** indique quels utilisateurs utiliser pour chacun des scénarios.</span><span class="sxs-lookup"><span data-stu-id="19167-221">The **Summary** tab indicates which users to use for each of the scenarios.</span></span> <span data-ttu-id="19167-222">Il est possible de configurer manuellement la plage des numéros d’utilisateur en activant la case à cocher Activer la génération de plages d' **utilisateurs personnalisés** , puis en double-cliquant sur le scénario dans la table dont vous souhaitez **personnaliser la plage d’utilisateurs.**</span><span class="sxs-lookup"><span data-stu-id="19167-222">It is possible to manually configure user number ranges by selecting the **Enable Custom User Range Generation** check box, and then double-clicking the scenario in the table that has the **User Range** that you want to customize.</span></span> <span data-ttu-id="19167-223">Vérifier (RunClient.bat) ajouter un délai de connexion au démarrage, afin d’inclure les retards dans les fichiers de commandes générés pour correspondre au taux de connexion.</span><span class="sxs-lookup"><span data-stu-id="19167-223">Check (RunClient.bat) Add sign-in delay when starting, in order to include delays in the generated batch files to correspond with the sign-in rate.</span></span> <span data-ttu-id="19167-224">Cela peut s’avérer utile pour éviter une surcharge du serveur lors de la connexion d’un grand nombre d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="19167-224">This is useful to prevent server overload when signing in a large number of users.</span></span> <span data-ttu-id="19167-225">Cliquez sur **générer des fichiers**, puis sélectionnez le dossier dans lequel vous voulez générer la configuration.</span><span class="sxs-lookup"><span data-stu-id="19167-225">Click **Generate Files**, and select the folder where you want to generate the configuration.</span></span> <span data-ttu-id="19167-226">Une boîte de dialogue similaire à la figure suivante s’affichera lors de la création de vos fichiers.</span><span class="sxs-lookup"><span data-stu-id="19167-226">A dialog box similar to the following figure will appear when your files have been successfully created.</span></span>

<span data-ttu-id="19167-227">![Accusé de réception de la création de fichiers.](images/JJ945594.00dc1e92-bfba-48e7-9568-b97ad864491e(OCS.15).jpg "Accusé de réception de la création de fichiers.")</span><span class="sxs-lookup"><span data-stu-id="19167-227">![Acknowledgement that files have been created.](images/JJ945594.00dc1e92-bfba-48e7-9568-b97ad864491e(OCS.15).jpg "Acknowledgement that files have been created.")</span></span>

</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="19167-228">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="19167-228">See Also</span></span>


[<span data-ttu-id="19167-229">Créer des utilisateurs et des contacts</span><span class="sxs-lookup"><span data-stu-id="19167-229">Create Users and Contacts</span></span>](create-users-and-contacts.md)  
</div>
</div>
<span></span>
</div>
</div>
</div>
