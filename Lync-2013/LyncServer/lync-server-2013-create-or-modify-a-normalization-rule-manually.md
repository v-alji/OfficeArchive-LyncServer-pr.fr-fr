---
title: 'Lync Server 2013 : Création ou modification manuelle d’une règle de normalisation'
description: 'Lync Server 2013 : créez ou modifiez manuellement une règle de normalisation.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or modify a normalization rule manually
ms:assetid: fc0335e6-8830-4cfb-8c64-6aeb98c0a992
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413074(v=OCS.15)
ms:contentKeyID: 48185943
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a7cc61706dd91b52822747d59693c8998d244c08
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431763"
---
# <a name="create-or-modify-a-normalization-rule-manually-in-lync-server-2013"></a><span data-ttu-id="8cdf8-103">Création ou modification manuelle d’une règle de normalisation dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8cdf8-103">Create or modify a normalization rule manually in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8cdf8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8cdf8-104">

<span> </span></span></span>

<span data-ttu-id="8cdf8-105">_**Dernière modification de la rubrique :** 2012-09-22_</span><span class="sxs-lookup"><span data-stu-id="8cdf8-105">_**Topic Last Modified:** 2012-09-22_</span></span>

<span data-ttu-id="8cdf8-106">Suivez les étapes ci-dessous si vous voulez créer ou modifier une règle de normalisation manuellement.</span><span class="sxs-lookup"><span data-stu-id="8cdf8-106">Complete the following steps if you want to create or modify a normalization rule manually.</span></span> <span data-ttu-id="8cdf8-107">Pour créer ou modifier une règle de normalisation à l’aide de l’application créer une règle de normalisation dans le panneau de configuration de Lync Server, voir [créer ou modifier une règle de normalisation à l’aide de l’application créer une règle de normalisation dans Lync Server 2013](lync-server-2013-create-or-modify-a-normalization-rule-by-using-build-a-normalization-rule.md).</span><span class="sxs-lookup"><span data-stu-id="8cdf8-107">If you want to create or modify a normalization rule by using Build a Normalization Rule in Lync Server Control Panel, see [Create or modify a normalization rule by using Build a Normalization Rule in Lync Server 2013](lync-server-2013-create-or-modify-a-normalization-rule-by-using-build-a-normalization-rule.md).</span></span>

<div>

## <a name="to-define-a-normalization-rule-manually"></a><span data-ttu-id="8cdf8-108">Pour définir une règle de normalisation manuellement</span><span class="sxs-lookup"><span data-stu-id="8cdf8-108">To define a normalization rule manually</span></span>

1.  <span data-ttu-id="8cdf8-109">Connectez-vous à l’ordinateur en tant que membre du groupe RTCUniversalServerAdmins ou en tant que membre du rôle CsVoiceAdministrator, CsServerAdministrator ou CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="8cdf8-109">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the CsVoiceAdministrator, CsServerAdministrator, or CsAdministrator role.</span></span> <span data-ttu-id="8cdf8-110">Pour plus d’informations, reportez-vous à la section [délégation des autorisations de configuration dans Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="8cdf8-110">For details, see [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="8cdf8-111">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="8cdf8-111">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="8cdf8-112">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="8cdf8-112">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="8cdf8-113">Facultatif Suivez les étapes de la rubrique [créer un plan de numérotation dans Lync server 2013](lync-server-2013-create-a-dial-plan.md) ou [modifier un plan de numérotation dans Lync Server 2013](lync-server-2013-modify-a-dial-plan.md).</span><span class="sxs-lookup"><span data-stu-id="8cdf8-113">(Optional) Follow the steps in [Create a dial plan in Lync Server 2013](lync-server-2013-create-a-dial-plan.md) or [Modify a dial plan in Lync Server 2013](lync-server-2013-modify-a-dial-plan.md).</span></span>

4.  <span data-ttu-id="8cdf8-114">Dans **Nouvelle règle de normalisation** ou **Modifier une règle de normalisation**, entrez un nom qui décrive le modèle de numéro à normaliser dans **Nom** (par exemple, nommez la règle de normalisation **5DigitExtension**).</span><span class="sxs-lookup"><span data-stu-id="8cdf8-114">In **New Normalization Rule** or **Edit Normalization Rule**, type a name that describes the number pattern being normalized in **Name** (for example, name the normalization rule **5DigitExtension**).</span></span>

5.  <span data-ttu-id="8cdf8-115">(Facultatif) Dans le champ **Description**, entrez la description de la règle de normalisation, par exemple, « Traduit les numéros de poste à 5 chiffres ».</span><span class="sxs-lookup"><span data-stu-id="8cdf8-115">(Optional) In **Description** field, type a description of the normalization rule (for example, "Translates 5-digit extensions").</span></span>

6.  <span data-ttu-id="8cdf8-116">Dans **Créer une règle de normalisation**, cliquez sur **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="8cdf8-116">In **Build a Normalization Rule**, click **Edit**.</span></span>

7.  <span data-ttu-id="8cdf8-117">Entrez ce qui suit dans **Taper une expression régulière** :</span><span class="sxs-lookup"><span data-stu-id="8cdf8-117">Enter the following in **Type a Regular Expression**:</span></span>
    
      - <span data-ttu-id="8cdf8-118">Dans **Suivre ce modèle**, indiquez le modèle que vous souhaitez utiliser pour le numéro de téléphone composé.</span><span class="sxs-lookup"><span data-stu-id="8cdf8-118">In **Match this pattern**, specify the pattern that you want to use to match the dialed phone number.</span></span>
    
      - <span data-ttu-id="8cdf8-119">Dans **Règle de conversion**, précisez un modèle pour le format des numéros de téléphone E.164 convertis.</span><span class="sxs-lookup"><span data-stu-id="8cdf8-119">In **Translation rule**, specify a pattern for the format of translated E.164 phone numbers.</span></span>
    
    <span data-ttu-id="8cdf8-120">Par exemple, si vous entrez **^ ( \\ d {7} ) $** dans **respecter ce modèle** et **+ 1425 $1** dans la **règle de traduction**, la règle normalise les 5550100 à + 14255550100.</span><span class="sxs-lookup"><span data-stu-id="8cdf8-120">For example, if you enter **^(\\d{7})$** in **Match this pattern** and **+1425$1** in **Translation rule**, the rule normalizes 5550100 to +14255550100.</span></span>

8.  <span data-ttu-id="8cdf8-121">(Facultatif) Si la règle de normalisation est convertie en un numéro de téléphone interne à votre entreprise, sélectionnez **Poste interne**.</span><span class="sxs-lookup"><span data-stu-id="8cdf8-121">(Optional) If the normalization rule results in a phone number that is internal to your organization, select **Internal extension**.</span></span>

9.  <span data-ttu-id="8cdf8-p104">(Facultatif) Entrez un numéro pour tester la règle de normalisation, puis cliquez sur **OK**. Les résultats du test s’affichent sous **Numéro composé à tester**.</span><span class="sxs-lookup"><span data-stu-id="8cdf8-p104">(Optional) Enter a number to test the normalization rule and then click **Go**. The test results are displayed under **Enter a number to test**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="8cdf8-124">Vous pouvez enregistrer une règle de normalisation n’ayant pas encore passé le test afin de la reconfigurer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="8cdf8-124">You can save a normalization rule that does not yet pass the test and then reconfigure it later.</span></span> <span data-ttu-id="8cdf8-125">Pour plus d’informations, consultez <A href="lync-server-2013-test-voice-routing.md">tester le routage vocal dans Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="8cdf8-125">For details, see <A href="lync-server-2013-test-voice-routing.md">Test voice routing in Lync Server 2013</A>.</span></span>

    
    </div>

10. <span data-ttu-id="8cdf8-126">Cliquez sur **OK** pour enregistrer la règle de normalisation.</span><span class="sxs-lookup"><span data-stu-id="8cdf8-126">Click **OK** to save the normalization rule.</span></span>

11. <span data-ttu-id="8cdf8-127">Cliquez sur **OK** pour enregistrer le plan de numérotation.</span><span class="sxs-lookup"><span data-stu-id="8cdf8-127">Click **OK** to save the dial plan.</span></span>

12. <span data-ttu-id="8cdf8-128">Dans la page **Plan de numérotation**, cliquez sur **Valider**, puis sur **Valider tout**.</span><span class="sxs-lookup"><span data-stu-id="8cdf8-128">On the **Dial Plan** page, click **Commit**, and then click **Commit all**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="8cdf8-129">Lorsque vous créez ou modifiez une règle de normalisation, vous devez exécuter la commande <STRONG>Valider tout</STRONG> pour publier la modification de configuration.</span><span class="sxs-lookup"><span data-stu-id="8cdf8-129">Whenever you create or change a normalization rule, you must run the <STRONG>Commit all</STRONG> command to publish the configuration change.</span></span> <span data-ttu-id="8cdf8-130">Pour plus d’informations, reportez-vous <A href="lync-server-2013-publish-pending-changes-to-the-voice-routing-configuration.md">à la rubrique publier des modifications en attente sur la configuration de l’acheminement de la voix dans Lync Server 2013</A> dans la documentation</span><span class="sxs-lookup"><span data-stu-id="8cdf8-130">For details, see <A href="lync-server-2013-publish-pending-changes-to-the-voice-routing-configuration.md">Publish pending changes to the voice routing configuration in Lync Server 2013</A> in the Operations documentation.</span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="8cdf8-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8cdf8-131">See Also</span></span>


[<span data-ttu-id="8cdf8-132">Créer ou modifier une règle de normalisation à l’aide de l’application créer une règle de normalisation dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8cdf8-132">Create or modify a normalization rule by using Build a Normalization Rule in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-normalization-rule-by-using-build-a-normalization-rule.md)  
[<span data-ttu-id="8cdf8-133">Créer un plan de numérotation dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8cdf8-133">Create a dial plan in Lync Server 2013</span></span>](lync-server-2013-create-a-dial-plan.md)  
[<span data-ttu-id="8cdf8-134">Modification d’un plan de numérotation dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8cdf8-134">Modify a dial plan in Lync Server 2013</span></span>](lync-server-2013-modify-a-dial-plan.md)  
[<span data-ttu-id="8cdf8-135">Publier les modifications en attente apportées à la configuration du routage de la voix dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8cdf8-135">Publish pending changes to the voice routing configuration in Lync Server 2013</span></span>](lync-server-2013-publish-pending-changes-to-the-voice-routing-configuration.md)  


[<span data-ttu-id="8cdf8-136">Test du routage des communications vocales dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8cdf8-136">Test voice routing in Lync Server 2013</span></span>](lync-server-2013-test-voice-routing.md)  
  

<span data-ttu-id="8cdf8-137"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8cdf8-137"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

