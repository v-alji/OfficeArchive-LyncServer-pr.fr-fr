---
title: 'Lync Server 2013 : exécuter des tests de routage de voix informels'
description: 'Lync Server 2013 : exécuter des tests de routage de voix informels.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Run informal voice routing tests
ms:assetid: ea0e6059-bf04-4b03-b6d3-8f5534b731e2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399049(v=OCS.15)
ms:contentKeyID: 48185904
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6029be34f4e4e7b366cb73f56ca611b4773331fd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442263"
---
# <a name="run-informal-voice-routing-tests-in-lync-server-2013"></a><span data-ttu-id="ee3fc-103">Exécuter des tests de routage de voix informels dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ee3fc-103">Run informal voice routing tests in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ee3fc-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ee3fc-104">

<span> </span></span></span>

<span data-ttu-id="ee3fc-105">_**Dernière modification de la rubrique :** 2012-08-07_</span><span class="sxs-lookup"><span data-stu-id="ee3fc-105">_**Topic Last Modified:** 2012-08-07_</span></span>

<span data-ttu-id="ee3fc-106">Vous pouvez utiliser la boîte de dialogue **créer des informations de cas de test de routage de voix** pour exécuter des tests informels avant de créer un cas de test réel.</span><span class="sxs-lookup"><span data-stu-id="ee3fc-106">You can use the **Create voice routing test case information** dialog box to run informal tests before creating an actual test case.</span></span> <span data-ttu-id="ee3fc-107">Lorsque vous êtes satisfait du résultat d’un test, vous pouvez l’enregistrer comme un cas de test formel.</span><span class="sxs-lookup"><span data-stu-id="ee3fc-107">When you are satisfied with the outcome of a test, you have the option of saving it as a formal test case.</span></span>

<div>

## <a name="to-run-an-informal-voice-routing-test"></a><span data-ttu-id="ee3fc-108">Pour exécuter un test de routage vocal informel</span><span class="sxs-lookup"><span data-stu-id="ee3fc-108">To run an informal voice routing test</span></span>

1.  <span data-ttu-id="ee3fc-109">Connectez-vous à l’ordinateur en tant que membre du groupe RTCUniversalServerAdmins ou en tant que membre du rôle CsVoiceAdministrator, CsServerAdministrator ou CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="ee3fc-109">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the CsVoiceAdministrator, CsServerAdministrator, or CsAdministrator role.</span></span> <span data-ttu-id="ee3fc-110">Pour plus d’informations, reportez-vous à la section [délégation des autorisations de configuration dans Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="ee3fc-110">For details, see [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="ee3fc-111">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ee3fc-111">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="ee3fc-112">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="ee3fc-112">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="ee3fc-113">Dans la barre de navigation de gauche, cliquez sur **routage des communications vocales**, puis cliquez sur **tester le routage vocal**.</span><span class="sxs-lookup"><span data-stu-id="ee3fc-113">In the left navigation bar, click **Voice Routing**, and then click **Test Voice Routing**.</span></span>

4.  <span data-ttu-id="ee3fc-114">Dans la page **test de routage vocal** , cliquez sur **créer des informations de cas de test de routage vocal**.</span><span class="sxs-lookup"><span data-stu-id="ee3fc-114">On the **Test Voice Routing** page, click **Create voice routing test case information**.</span></span>

5.  <span data-ttu-id="ee3fc-115">Dans le champ **numéro composé** , entrez le numéro de téléphone que vous voulez utiliser pour ce test.</span><span class="sxs-lookup"><span data-stu-id="ee3fc-115">In the **Dialed number** field, type in the phone number you want to use for this test.</span></span> <span data-ttu-id="ee3fc-116">Ce numéro sera normalisé et affiché dans le champ **nombre normalisé** du volet **résultats** .</span><span class="sxs-lookup"><span data-stu-id="ee3fc-116">This number will be normalized and displayed in the **Normalized number** field of the **Results** pane.</span></span>

6.  <span data-ttu-id="ee3fc-117">Dans la liste **plan de numérotation** , sélectionnez le plan de numérotation à utiliser pour tester le numéro numéroté.</span><span class="sxs-lookup"><span data-stu-id="ee3fc-117">In the **Dial plan** list, select the dial plan to use for testing the dialed number.</span></span> <span data-ttu-id="ee3fc-118">Par défaut est le plan de numérotation global.</span><span class="sxs-lookup"><span data-stu-id="ee3fc-118">Default is the Global dial plan.</span></span>
    
    <span data-ttu-id="ee3fc-119">Lors de l’exécution du test, la première règle de normalisation de ce plan de numérotation qui correspond au numéro composé sera affichée dans le champ **règle de normalisation** du volet **résultats** .</span><span class="sxs-lookup"><span data-stu-id="ee3fc-119">When you run the test, the first normalization rule in this dial plan that matches the dialed number will be displayed in the **Normalization rule** field of the **Results** pane.</span></span>

7.  <span data-ttu-id="ee3fc-120">Dans la liste **politique vocale** , sélectionnez la stratégie vocale à utiliser pour tester le numéro numéroté.</span><span class="sxs-lookup"><span data-stu-id="ee3fc-120">In the **Voice Policy** list, select the voice policy to use for testing the dialed number.</span></span> <span data-ttu-id="ee3fc-121">La valeur par défaut est la stratégie de voix globale.</span><span class="sxs-lookup"><span data-stu-id="ee3fc-121">Default is the Global voice policy.</span></span>
    
    <span data-ttu-id="ee3fc-122">Lors de l’exécution du test, le premier enregistrement d’utilisation RTC correspondant à cette stratégie vocale est affiché dans le premier champ d' **utilisation RTC** du volet **résultats** .</span><span class="sxs-lookup"><span data-stu-id="ee3fc-122">When you run the test, the first matching PSTN usage record in this voice policy will be displayed in the **First PSTN usage** field of the **Results** pane.</span></span> <span data-ttu-id="ee3fc-123">Par ailleurs, le premier itinéraire vocal correspondant associé à cet enregistrement d’utilisation RTC sera affiché dans le premier champ de **routage** .</span><span class="sxs-lookup"><span data-stu-id="ee3fc-123">Also, the first matching voice route that is associated with this PSTN usage record will be displayed in the **First route** field.</span></span>

8.  <span data-ttu-id="ee3fc-124">Facultatif Activez la case à cocher **remplir à partir de l’utilisateur** si vous souhaitez tester le numéro numéroté par rapport à la stratégie vocale attribuée à un utilisateur particulier.</span><span class="sxs-lookup"><span data-stu-id="ee3fc-124">(Optional) Select the **Populate from user** check box if you want to test the dialed number against the voice policy assigned to a particular user.</span></span>
    
    1.  <span data-ttu-id="ee3fc-125">Cliquez sur **Parcourir** pour afficher la boîte de dialogue **Sélectionner des utilisateurs voix entreprise** .</span><span class="sxs-lookup"><span data-stu-id="ee3fc-125">Click **Browse** to display the **Select Enterprise Voice Users** dialog box.</span></span>
    
    2.  <span data-ttu-id="ee3fc-126">Cliquez sur **Rechercher** pour afficher la liste des utilisateurs activés pour voix entreprise.</span><span class="sxs-lookup"><span data-stu-id="ee3fc-126">Click **Find** to display the list of users who are enabled for Enterprise Voice.</span></span>
    
    3.  <span data-ttu-id="ee3fc-127">Double-cliquez sur le nom d’utilisateur dont vous souhaitez utiliser la politique vocale affectée pour ce test.</span><span class="sxs-lookup"><span data-stu-id="ee3fc-127">Double-click the user name whose assigned voice policy you want to use for this test.</span></span> <span data-ttu-id="ee3fc-128">Le champ **politique** est désormais rempli par la stratégie vocale affectée à l’utilisateur sélectionné.</span><span class="sxs-lookup"><span data-stu-id="ee3fc-128">The **Policy** field is now populated with the voice policy assigned to the selected user.</span></span>
    
    <span data-ttu-id="ee3fc-129">Lors de l’exécution du test, le premier enregistrement d’utilisation RTC (réseau téléphonique commuté) correspondant à cette stratégie vocale sera affiché dans le **premier champ d’utilisation RTC** du volet **résultats** .</span><span class="sxs-lookup"><span data-stu-id="ee3fc-129">When you run the test, the first matching public switched telephone network (PSTN) usage record in this voice policy will be displayed in the **First PSTN usage** field of the **Results** pane.</span></span> <span data-ttu-id="ee3fc-130">Par ailleurs, le premier itinéraire vocal correspondant associé à cet enregistrement d’utilisation RTC sera affiché dans le premier champ de **routage** .</span><span class="sxs-lookup"><span data-stu-id="ee3fc-130">Also, the first matching voice route that is associated with this PSTN usage record will be displayed in the **First route** field.</span></span>

9.  <span data-ttu-id="ee3fc-131">Cliquez sur **exécuter** pour exécuter le cas de test.</span><span class="sxs-lookup"><span data-stu-id="ee3fc-131">Click **Run** to run the test case.</span></span> <span data-ttu-id="ee3fc-132">Les résultats sont affichés dans le volet droit de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="ee3fc-132">The results are shown in the right panel of the dialog box.</span></span>

10. <span data-ttu-id="ee3fc-133">Facultatif Cliquez sur **Enregistrer sous** si vous voulez enregistrer cette configuration de test en tant que cas de test formel.</span><span class="sxs-lookup"><span data-stu-id="ee3fc-133">(Optional) Click **Save as** if you want to save this test configuration as a formal test case.</span></span>
    
    1.  <span data-ttu-id="ee3fc-134">Dans le champ **nom** de la boîte de dialogue **enregistrer les informations de cas de test de routage de voix** , tapez un nom unique pour le cas de test.</span><span class="sxs-lookup"><span data-stu-id="ee3fc-134">In the **Name** field of the **Save Voice Routing Test Case Information** dialog box, type a unique name for the test case.</span></span>
        
        <span data-ttu-id="ee3fc-135">Ce nom doit être unique parmi les cas de test de routage vocal dans votre déploiement voix entreprise.</span><span class="sxs-lookup"><span data-stu-id="ee3fc-135">The name must be unique among all voice routing test cases in your Enterprise Voice deployment.</span></span> <span data-ttu-id="ee3fc-136">Il peut y avoir une longueur maximale de 32 caractères et contenir des caractères alphanumériques, en plus de la barre oblique inverse ( \\ ), du point (.) ou du trait de soulignement ( \_ ).</span><span class="sxs-lookup"><span data-stu-id="ee3fc-136">It can be up to 32 characters in length and may contain any alphanumeric characters, in addition to the backslash (\\), period (.), or underscore (\_).</span></span>
    
    2.  <span data-ttu-id="ee3fc-137">Notez que les champs restants de la boîte de dialogue Enregistrer les informations de cas de test de l' **itinéraire vocale** sont en lecture seule et sont préremplis par rapport à la configuration *et* aux résultats du test informel.</span><span class="sxs-lookup"><span data-stu-id="ee3fc-137">Note that the remaining fields on the **Save Voice Routing Test Case Information** dialog box are read-only, and are prepopulated from the informal test configuration *and* results.</span></span> <span data-ttu-id="ee3fc-138">Vérifiez qu’il s’agit de la configuration que vous voulez enregistrer pour le cas de test.</span><span class="sxs-lookup"><span data-stu-id="ee3fc-138">Verify that this is the configuration that you want to save for the test case.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="ee3fc-139">Les valeurs des résultats de test permettent de préremplir les champs de la boîte de dialogue Enregistrer les informations de cas de test de l' <STRONG>acheminement du message</STRONG> , comme suit :</span><span class="sxs-lookup"><span data-stu-id="ee3fc-139">Values from the test results are used to prepopulate fields on the <STRONG>Save Voice Routing Test Case Information</STRONG> dialog box as follows:</span></span> 
        > <UL>
        > <LI>
        > <P><span data-ttu-id="ee3fc-140">La <STRONG>traduction attendue</STRONG> est préremplie avec la valeur du champ <STRONG>nombre normalisé</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="ee3fc-140"><STRONG>Expected translation</STRONG> is prepopulated with the value in the <STRONG>Normalized number</STRONG> field.</span></span></P>
        > <LI>
        > <P><span data-ttu-id="ee3fc-141">Le champ <STRONG>route attendu</STRONG> est pré-rempli avec la valeur du <STRONG>premier champ itinéraire</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="ee3fc-141"><STRONG>Expected route</STRONG> is prepopulated with the value in the <STRONG>First route</STRONG> field.</span></span></P>
        > <LI>
        > <P><span data-ttu-id="ee3fc-142">L' <STRONG>enregistrement d’utilisation RTC attendu</STRONG> est pré-rempli avec la valeur du premier champ d' <STRONG>utilisation PSTN</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="ee3fc-142"><STRONG>Expected PSTN usage record</STRONG> is prepopulated with the value in the <STRONG>First PSTN usage</STRONG> field.</span></span></P></LI></UL><span data-ttu-id="ee3fc-143">Si les correspondances pour une de ces valeurs n’ont pas été trouvées lors de la série de tests, le champ correspondant est vide dans la boîte de dialogue Enregistrer les informations de cas de test de l' <STRONG>acheminement du message</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="ee3fc-143">If matches for any of these values were not found during the test run, the corresponding field is empty on the <STRONG>Save Voice Routing Test Case Information</STRONG> dialog box.</span></span>

        
        </div>
    
    3.  <span data-ttu-id="ee3fc-144">Cliquez sur **OK** pour enregistrer le cas de test, ou cliquez sur **Annuler** pour revenir à la boîte de dialogue Afficher les informations de cas de **test de routage**</span><span class="sxs-lookup"><span data-stu-id="ee3fc-144">Click **Ok** to save the test case, or click **Cancel** to return to return to the **View voice routing test case information** dialog box to further develop the test before saving it.</span></span>

11. <span data-ttu-id="ee3fc-145">Cliquez sur **Valider**, puis sur **Tout valider**.</span><span class="sxs-lookup"><span data-stu-id="ee3fc-145">Click **Commit**, and then click **Commit all**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="ee3fc-146">Chaque fois que vous créez un cas de test de routage de voix, vous devez exécuter la commande <STRONG>valider tout</STRONG> pour publier le cas de test.</span><span class="sxs-lookup"><span data-stu-id="ee3fc-146">Whenever you create a voice routing test case, you must run the <STRONG>Commit all</STRONG> command to publish the test case.</span></span> <span data-ttu-id="ee3fc-147">Pour plus d’informations, reportez-vous <A href="lync-server-2013-publish-pending-changes-to-the-voice-routing-configuration.md">à la rubrique publier des modifications en attente sur la configuration de l’acheminement de la voix dans Lync Server 2013</A> dans la documentation</span><span class="sxs-lookup"><span data-stu-id="ee3fc-147">For details, see <A href="lync-server-2013-publish-pending-changes-to-the-voice-routing-configuration.md">Publish pending changes to the voice routing configuration in Lync Server 2013</A> in the Operations documentation.</span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="ee3fc-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ee3fc-148">See Also</span></span>


[<span data-ttu-id="ee3fc-149">Création d’un cas de test de routage des communications vocales dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ee3fc-149">Create a voice routing test case in Lync Server 2013</span></span>](lync-server-2013-create-a-voice-routing-test-case.md)  
[<span data-ttu-id="ee3fc-150">Exécuter des cas de test de routage de voix dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ee3fc-150">Run voice routing test cases in Lync Server 2013</span></span>](lync-server-2013-run-voice-routing-test-cases.md)  
[<span data-ttu-id="ee3fc-151">Exportation des cas de test de routage des communications vocales dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ee3fc-151">Export voice routing test cases in Lync Server 2013</span></span>](lync-server-2013-export-voice-routing-test-cases.md)  
[<span data-ttu-id="ee3fc-152">Importation des cas de test de routage des communications vocales dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ee3fc-152">Import voice routing test cases in Lync Server 2013</span></span>](lync-server-2013-import-voice-routing-test-cases.md)  


[<span data-ttu-id="ee3fc-153">Configuration des plans de numérotation dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ee3fc-153">Configuring dial plans in Lync Server 2013</span></span>](lync-server-2013-configuring-dial-plans.md)  
[<span data-ttu-id="ee3fc-154">Configuration des stratégies vocales, des enregistrements d’utilisation RTC et des itinéraires vocaux dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ee3fc-154">Configuring voice policies, PSTN usage records, and voice routes in Lync Server 2013</span></span>](lync-server-2013-configuring-voice-policies-pstn-usage-records-and-voice-routes.md)  
  

<span data-ttu-id="ee3fc-155"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ee3fc-155"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

