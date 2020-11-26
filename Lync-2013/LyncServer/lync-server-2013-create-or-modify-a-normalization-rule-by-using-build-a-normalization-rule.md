---
title: Création ou modification d’une règle de normalisation à l’aide de l’onglet créer une règle de normalisation
description: Créez ou modifiez une règle de normalisation à l’aide de l’onglet créer une règle de normalisation.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or modify a normalization rule by using Build a Normalization Rule
ms:assetid: e8547d7b-f74d-4a73-9a7d-df20d7a87fcd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399036(v=OCS.15)
ms:contentKeyID: 48185889
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 824936359c070090ad4225a3ead6e8e46fe14785
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431750"
---
# <a name="create-or-modify-a-normalization-rule-by-using-build-a-normalization-rule-in-lync-server-2013"></a><span data-ttu-id="3ab54-103">Créer ou modifier une règle de normalisation à l’aide de l’application créer une règle de normalisation dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3ab54-103">Create or modify a normalization rule by using Build a Normalization Rule in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3ab54-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3ab54-104">

<span> </span></span></span>

<span data-ttu-id="3ab54-105">_**Dernière modification de la rubrique :** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="3ab54-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="3ab54-106">Pour créer ou modifier une règle de normalisation dans le panneau de configuration de Lync Server, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="3ab54-106">Complete the following steps if you want to create or modify a normalization rule in Lync Server Control Panel.</span></span> <span data-ttu-id="3ab54-107">Par ailleurs, si vous voulez créer ou modifier une règle de normalisation manuellement, voir [créer ou modifier une règle de normalisation manuellement dans Lync Server 2013](lync-server-2013-create-or-modify-a-normalization-rule-manually.md).</span><span class="sxs-lookup"><span data-stu-id="3ab54-107">Alternatively, if you want to create or modify a normalization rule manually, see [Create or modify a normalization rule manually in Lync Server 2013](lync-server-2013-create-or-modify-a-normalization-rule-manually.md).</span></span>

<div>

## <a name="to-define-a-rule-by-using-build-a-normalization-rule"></a><span data-ttu-id="3ab54-108">Pour définir une règle à l’aide de la création d’une règle de normalisation</span><span class="sxs-lookup"><span data-stu-id="3ab54-108">To define a rule by using Build a Normalization Rule</span></span>

1.  <span data-ttu-id="3ab54-109">Connectez-vous à l’ordinateur en tant que membre du groupe RTCUniversalServerAdmins ou en tant que membre du rôle CsVoiceAdministrator, CsServerAdministrator ou CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="3ab54-109">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the CsVoiceAdministrator, CsServerAdministrator, or CsAdministrator role.</span></span> <span data-ttu-id="3ab54-110">Pour plus d’informations, reportez-vous à la section [délégation des autorisations de configuration dans Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="3ab54-110">For details, see [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="3ab54-111">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="3ab54-111">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="3ab54-112">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="3ab54-112">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="3ab54-113">Facultatif Suivez les étapes de la rubrique [créer un plan de numérotation dans Lync server 2013 à l'](lync-server-2013-create-a-dial-plan.md) étape 11 ou [modifiez un plan de numérotation dans Lync Server 2013 à l'](lync-server-2013-modify-a-dial-plan.md) étape 10.</span><span class="sxs-lookup"><span data-stu-id="3ab54-113">(Optional) Follow the steps in [Create a dial plan in Lync Server 2013](lync-server-2013-create-a-dial-plan.md) through step 11 or [Modify a dial plan in Lync Server 2013](lync-server-2013-modify-a-dial-plan.md) through step 10.</span></span>

4.  <span data-ttu-id="3ab54-114">Dans la section **Nouvelle règle de normalisation** ou **Modifier une règle de normalisation**, entrez un nom décrivant le modèle de numéro en cours de normalisation dans le champ **Nom** (par exemple, **5DigitExtension**).</span><span class="sxs-lookup"><span data-stu-id="3ab54-114">In **New Normalization Rule** or **Edit Normalization Rule**, type a name that describes the number pattern being normalized in **Name** (for example, **5DigitExtension**).</span></span>

5.  <span data-ttu-id="3ab54-115">(Facultatif) Dans **Description**, entrez une description de la règle de normalisation (par exemple, « Traduit les postes à 5 chiffres »).</span><span class="sxs-lookup"><span data-stu-id="3ab54-115">(Optional) In **Description**, type a description of the normalization rule (for example, "Translates 5-digit extensions").</span></span>

6.  <span data-ttu-id="3ab54-116">Dans **Créer une règle de normalisation**, entrez les valeurs dans les champs suivants :</span><span class="sxs-lookup"><span data-stu-id="3ab54-116">In **Build a Normalization Rule**, enter values in the following fields:</span></span>
    
      - <span data-ttu-id="3ab54-117">**Chiffres de début**   (Facultatif) Spécifiez les chiffres de début des numéros composés que le modèle doit suivre.</span><span class="sxs-lookup"><span data-stu-id="3ab54-117">**Starting digits**   (Optional) Specify the leading digits of dialed numbers you want the pattern to match.</span></span> <span data-ttu-id="3ab54-118">Par exemple, tapez **425** si vous souhaitez que le modèle suive les numéros composés commençant par 425.</span><span class="sxs-lookup"><span data-stu-id="3ab54-118">For example, type **425** if you want the pattern to match dialed numbers beginning with 425.</span></span>
    
      - <span data-ttu-id="3ab54-119">**Longueur**   Spécifiez le nombre de chiffres du modèle à suivre et indiquez si vous souhaitez que le modèle suive exactement cette longueur, les numéros composés affichant au moins cette longueur ou les numéros composés quelle que soit leur longueur.</span><span class="sxs-lookup"><span data-stu-id="3ab54-119">**Length**   Specify the number of digits in the matching pattern and select whether you want the pattern to match this length exactly, match dialed numbers that are at least this length, or match dialed numbers of any length.</span></span>
    
      - <span data-ttu-id="3ab54-120">**Chiffres à supprimer**   (Facultatif) Spécifiez le nombre de chiffres de début à supprimer des numéros composés que le modèle doit suivre.</span><span class="sxs-lookup"><span data-stu-id="3ab54-120">**Digits to remove**   (Optional) Specify the number of starting digits to be removed from dialed numbers you want the pattern to match.</span></span>
    
      - <span data-ttu-id="3ab54-121">**Chiffres à ajouter**   (Facultatif) Spécifiez les chiffres à ajouter aux numéros composés que le modèle doit suivre.</span><span class="sxs-lookup"><span data-stu-id="3ab54-121">**Digits to add**   (Optional) Specify digits to be added to dialed numbers you want the pattern to match.</span></span>
    
    <span data-ttu-id="3ab54-p105">Les valeurs que vous entrez dans ces champs s’affichent dans **Modèle à suivre** et **Règle de conversion**. Par exemple, si vous laissez vide le champ **Chiffres de début**, tapez **7** dans le champ **Longueur** et sélectionnez **Exactement**, puis spécifiez **0** dans le champ **Chiffres à supprimer**, l’expression régulière obtenue dans **Modèle à suivre** est :</span><span class="sxs-lookup"><span data-stu-id="3ab54-p105">The values you enter in these fields are reflected in **Pattern to match** and **Translation rule**. For example, if you leave **Starting digits** empty, type **7** into the **Length** field and select **Exactly**, and specify **0** in **Digits to remove**, the resulting regular expression in the **Pattern to match** is:</span></span>
    
    <span data-ttu-id="3ab54-124">**^ ( \\ d {7} ) $**</span><span class="sxs-lookup"><span data-stu-id="3ab54-124">**^(\\d{7})$**</span></span>

7.  <span data-ttu-id="3ab54-125">Dans **Règle de conversion**, spécifiez comme suit le modèle du format des numéros de téléphone E.164 convertis :</span><span class="sxs-lookup"><span data-stu-id="3ab54-125">In **Translation rule**, specify a pattern for the format of translated E.164 phone numbers as follows:</span></span>
    
      - <span data-ttu-id="3ab54-126">Une valeur qui représente le nombre de chiffres spécifiés dans le modèle à suivre.</span><span class="sxs-lookup"><span data-stu-id="3ab54-126">A value that represents the number of digits specified in the matching pattern.</span></span> <span data-ttu-id="3ab54-127">Par exemple, si le modèle correspondant est **^ ( \\ j {7} ) $** , **$1** dans la règle de traduction représente les numéros numérotés à 7 chiffres.</span><span class="sxs-lookup"><span data-stu-id="3ab54-127">For example, if the matching pattern is **^(\\d{7})$** then **$1** in the translation rule represents 7-digit dialed numbers.</span></span>
    
      - <span data-ttu-id="3ab54-128">(Facultatif) Entrez une valeur dans le champ **Chiffres à ajouter** pour spécifier les chiffres à ajouter au numéro converti (par exemple, **+1425**).</span><span class="sxs-lookup"><span data-stu-id="3ab54-128">(Optional) Type a value into the **Digits to add** field to specify digits to be prepended to the translated number (for example, **+1425**).</span></span>
    
    <span data-ttu-id="3ab54-129">Par exemple, si le modèle **à faire correspondre** contient **^ ( \\ d {7} ) $** en tant que modèle pour les numéros numérotés et la **règle de traduction** contenant **+ 1425 $1** comme modèle pour les numéros de téléphone E. 164, la règle normalise 5550100 à + 14255550100.</span><span class="sxs-lookup"><span data-stu-id="3ab54-129">For example, if **Pattern to match** contains **^(\\d{7})$** as the pattern for dialed numbers and **Translation rule** contains **+1425$1** as the pattern for E.164 phone numbers, the rule normalizes 5550100 to +14255550100.</span></span>

8.  <span data-ttu-id="3ab54-130">(Facultatif) Si la règle de normalisation est convertie en un numéro de téléphone interne à votre entreprise, sélectionnez **Poste interne**.</span><span class="sxs-lookup"><span data-stu-id="3ab54-130">(Optional) If the normalization rule results in a phone number that is internal to your organization, select **Internal extension**.</span></span>

9.  <span data-ttu-id="3ab54-p107">(Facultatif) Entrez un numéro pour tester la règle de normalisation, puis cliquez sur **OK**. Les résultats du test s’affichent sous **Numéro composé à tester**.</span><span class="sxs-lookup"><span data-stu-id="3ab54-p107">(Optional) Enter a number to test the normalization rule, and then click **Go**. The test results are displayed under **Enter a number to test**.</span></span>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="3ab54-133">Vous pouvez enregistrer une règle de normalisation n’ayant pas encore passé le test afin de la reconfigurer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="3ab54-133">You can save a normalization rule that does not yet pass the test and then reconfigure it later.</span></span> <span data-ttu-id="3ab54-134">Pour plus d’informations, consultez <A href="lync-server-2013-test-voice-routing.md">tester le routage vocal dans Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="3ab54-134">For details, see <A href="lync-server-2013-test-voice-routing.md">Test voice routing in Lync Server 2013</A>.</span></span>

    
    </div>

10. <span data-ttu-id="3ab54-135">Cliquez sur **OK** pour enregistrer la règle de normalisation.</span><span class="sxs-lookup"><span data-stu-id="3ab54-135">Click **OK** to save the normalization rule.</span></span>

11. <span data-ttu-id="3ab54-136">Cliquez sur **OK** pour enregistrer le plan de numérotation.</span><span class="sxs-lookup"><span data-stu-id="3ab54-136">Click **OK** to save the dial plan.</span></span>

12. <span data-ttu-id="3ab54-137">Dans la page **Plan de numérotation**, cliquez sur **Valider**, puis sur **Valider tout**.</span><span class="sxs-lookup"><span data-stu-id="3ab54-137">On the **Dial Plan** page, click **Commit**, and then click **Commit all**.</span></span>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="3ab54-138">Lorsque vous créez ou modifiez une règle de normalisation, vous devez exécuter la commande <STRONG>Valider tout</STRONG> pour publier la modification de configuration.</span><span class="sxs-lookup"><span data-stu-id="3ab54-138">Whenever you create or change a normalization rule, you must run the <STRONG>Commit all</STRONG> command to publish the configuration change.</span></span> <span data-ttu-id="3ab54-139">Pour plus d’informations, reportez-vous <A href="lync-server-2013-publish-pending-changes-to-the-voice-routing-configuration.md">à la rubrique publier des modifications en attente sur la configuration de l’acheminement de la voix dans Lync Server 2013</A> dans la documentation</span><span class="sxs-lookup"><span data-stu-id="3ab54-139">For details, see <A href="lync-server-2013-publish-pending-changes-to-the-voice-routing-configuration.md">Publish pending changes to the voice routing configuration in Lync Server 2013</A> in the Operations documentation.</span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="3ab54-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3ab54-140">See Also</span></span>


[<span data-ttu-id="3ab54-141">Création ou modification manuelle d’une règle de normalisation dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3ab54-141">Create or modify a normalization rule manually in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-normalization-rule-manually.md)  
[<span data-ttu-id="3ab54-142">Créer un plan de numérotation dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3ab54-142">Create a dial plan in Lync Server 2013</span></span>](lync-server-2013-create-a-dial-plan.md)  
[<span data-ttu-id="3ab54-143">Modification d’un plan de numérotation dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3ab54-143">Modify a dial plan in Lync Server 2013</span></span>](lync-server-2013-modify-a-dial-plan.md)  
[<span data-ttu-id="3ab54-144">Publier les modifications en attente apportées à la configuration du routage de la voix dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3ab54-144">Publish pending changes to the voice routing configuration in Lync Server 2013</span></span>](lync-server-2013-publish-pending-changes-to-the-voice-routing-configuration.md)  


[<span data-ttu-id="3ab54-145">Test du routage des communications vocales dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3ab54-145">Test voice routing in Lync Server 2013</span></span>](lync-server-2013-test-voice-routing.md)  
  

<span data-ttu-id="3ab54-146"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3ab54-146"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

