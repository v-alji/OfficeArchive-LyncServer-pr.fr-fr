---
title: 'Lync Server 2013 : création ou modification manuelle d’une règle de traduction'
description: 'Lync Server 2013 : création ou modification manuelle d’une règle de traduction.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or modify a translation rule manually
ms:assetid: 049d1db3-af58-48c5-be89-52e1d068a4bd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398099(v=OCS.15)
ms:contentKeyID: 48183276
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4f393ca1983e072090cc27d47b142dace8b566c5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431735"
---
# <a name="create-or-modify-a-translation-rule-manually-in-lync-server-2013"></a><span data-ttu-id="a02e5-103">Créer ou modifier une règle de traduction manuellement dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a02e5-103">Create or modify a translation rule manually in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a02e5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a02e5-104">

<span> </span></span></span>

<span data-ttu-id="a02e5-105">_**Dernière modification de la rubrique :** 2012-08-06_</span><span class="sxs-lookup"><span data-stu-id="a02e5-105">_**Topic Last Modified:** 2012-08-06_</span></span>

<span data-ttu-id="a02e5-106">Suivez ces étapes si vous voulez définir une règle de traduction en écrivant une expression régulière pour le modèle et la règle de traduction correspondants.</span><span class="sxs-lookup"><span data-stu-id="a02e5-106">Follow these steps if you want to define a translation rule by writing a regular expression for the matching pattern and translation rule.</span></span> <span data-ttu-id="a02e5-107">Vous pouvez également entrer un ensemble de valeurs dans l’outil **créer une règle de traduction** et activer le panneau de configuration de Lync Server pour générer le modèle correspondant et la règle de traduction correspondants pour vous.</span><span class="sxs-lookup"><span data-stu-id="a02e5-107">Alternatively, you can enter a set of values in the **Build a Translation Rule** tool and enable Lync Server Control Panel to generate the corresponding matching pattern and translation rule for you.</span></span> <span data-ttu-id="a02e5-108">Pour plus d’informations, reportez-vous à [créer ou modifier une règle de traduction à l’aide de l’outil créer une règle de traduction dans Lync Server 2013](lync-server-2013-create-or-modify-a-translation-rule-by-using-the-build-a-translation-rule-tool.md).</span><span class="sxs-lookup"><span data-stu-id="a02e5-108">For details, see [Create or modify a translation rule by using the Build a Translation Rule tool in Lync Server 2013](lync-server-2013-create-or-modify-a-translation-rule-by-using-the-build-a-translation-rule-tool.md).</span></span>

<div>

## <a name="to-define-a-translation-rule-manually"></a><span data-ttu-id="a02e5-109">Pour définir une règle de traduction manuellement</span><span class="sxs-lookup"><span data-stu-id="a02e5-109">To define a translation rule manually</span></span>

1.  <span data-ttu-id="a02e5-110">Connectez-vous à l’ordinateur en tant que membre du groupe RTCUniversalServerAdmins ou en tant que membre du rôle CsVoiceAdministrator, CsServerAdministrator ou CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="a02e5-110">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the CsVoiceAdministrator, CsServerAdministrator, or CsAdministrator role.</span></span> <span data-ttu-id="a02e5-111">Pour plus d’informations, reportez-vous à la section [délégation des autorisations de configuration dans Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="a02e5-111">For details, see [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="a02e5-112">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="a02e5-112">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="a02e5-113">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="a02e5-113">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="a02e5-114">Pour commencer à définir une règle de traduction, suivez les étapes décrites dans l’article [configurer un Trunk with Media bypass dans Lync server 2013](lync-server-2013-configure-a-trunk-with-media-bypass.md) à l’étape 10 ou [configurer un Trunk sans dérivation multimédia dans Lync Server 2013](lync-server-2013-configure-a-trunk-without-media-bypass.md) à l’étape 9.</span><span class="sxs-lookup"><span data-stu-id="a02e5-114">To begin defining a translation rule, follow the steps in [Configure a trunk with media bypass in Lync Server 2013](lync-server-2013-configure-a-trunk-with-media-bypass.md) through step 10 or [Configure a trunk without media bypass in Lync Server 2013](lync-server-2013-configure-a-trunk-without-media-bypass.md) through step 9.</span></span>

4.  <span data-ttu-id="a02e5-115">Dans le champ **Nom** dans la page **Nouvelle règle de traduction** ou **Modifier la règle de traduction**, tapez un nom décrivant le modèle de numéro en cours de traduction.</span><span class="sxs-lookup"><span data-stu-id="a02e5-115">In the **Name** field on the **New Translation Rule** or **Edit Translation Rule** page, type a name that describes the number pattern being translated.</span></span>

5.  <span data-ttu-id="a02e5-116">(Facultatif) Dans **Description**, entrez la description de la règle de traduction, par exemple **US International long-distance dialing**.</span><span class="sxs-lookup"><span data-stu-id="a02e5-116">(Optional) In **Description**, type a description of the translation rule, for example **US International long-distance dialing**.</span></span>

6.  <span data-ttu-id="a02e5-117">Cliquez sur **Modifier** au bas de la section **Créer une règle de traduction**.</span><span class="sxs-lookup"><span data-stu-id="a02e5-117">Click **Edit** at the bottom of the **Build a Translation Rule** section.</span></span>

7.  <span data-ttu-id="a02e5-118">Entrez ce qui suit dans **Taper une expression régulière** :</span><span class="sxs-lookup"><span data-stu-id="a02e5-118">Enter the following in **Type a Regular Expression**:</span></span>
    
      - <span data-ttu-id="a02e5-119">Dans **Suivre ce modèle**, spécifiez le modèle qui sera utilisé pour correspondre aux numéros à traduire.</span><span class="sxs-lookup"><span data-stu-id="a02e5-119">In **Match this pattern**, specify the pattern that will be used to match the numbers to be translated.</span></span>
    
      - <span data-ttu-id="a02e5-120">Dans **Règle de traduction**, spécifiez un modèle pour le format des numéros traduits.</span><span class="sxs-lookup"><span data-stu-id="a02e5-120">In **Translation rule**, specify a pattern for the format of translated numbers.</span></span>
    
    <span data-ttu-id="a02e5-121">Par exemple, si vous tapez **^ \\ + ( \\ j {9} \\ + +) $** dans **correspondre à ce modèle** et **011 $1** dans la **règle de traduction**, la règle traduira + 441235551010 à 011441235551010.</span><span class="sxs-lookup"><span data-stu-id="a02e5-121">For example, if you enter **^\\+(\\d{9}\\d+)$** in **Match this pattern** and **011$1** in **Translation rule**, the rule will translate +441235551010 to 011441235551010.</span></span>

8.  <span data-ttu-id="a02e5-122">Cliquez sur **OK** pour enregistrer la règle de traduction.</span><span class="sxs-lookup"><span data-stu-id="a02e5-122">Click **OK** to save the translation rule.</span></span>

9.  <span data-ttu-id="a02e5-123">Cliquez sur **OK** pour enregistrer la configuration de la jonction.</span><span class="sxs-lookup"><span data-stu-id="a02e5-123">Click **OK** to save the trunk configuration.</span></span>

10. <span data-ttu-id="a02e5-124">Dans la page **Configuration de la jonction**, cliquez sur **Valider**, puis sur **Valider tout**.</span><span class="sxs-lookup"><span data-stu-id="a02e5-124">On the **Trunk Configuration** page, click **Commit**, and then click **Commit all**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="a02e5-125">Chaque fois que vous créez ou modifiez une règle de traduction, vous devez exécuter la commande <STRONG>Valider tout</STRONG> pour publier la modification de la configuration.</span><span class="sxs-lookup"><span data-stu-id="a02e5-125">Whenever you create or modify a translation rule, you must run the <STRONG>Commit all</STRONG> command to publish the configuration change.</span></span> <span data-ttu-id="a02e5-126">Pour plus d’informations, reportez-vous <A href="lync-server-2013-publish-pending-changes-to-the-voice-routing-configuration.md">à la rubrique publier des modifications en attente sur la configuration de l’acheminement de la voix dans Lync Server 2013</A> dans la documentation</span><span class="sxs-lookup"><span data-stu-id="a02e5-126">For details, see <A href="lync-server-2013-publish-pending-changes-to-the-voice-routing-configuration.md">Publish pending changes to the voice routing configuration in Lync Server 2013</A> in the Operations documentation.</span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="a02e5-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a02e5-127">See Also</span></span>


[<span data-ttu-id="a02e5-128">Créer ou modifier une règle de traduction à l’aide de l’outil créer une règle de traduction dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a02e5-128">Create or modify a translation rule by using the Build a Translation Rule tool in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-translation-rule-by-using-the-build-a-translation-rule-tool.md)  
[<span data-ttu-id="a02e5-129">Configure a trunk with media bypass in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a02e5-129">Configure a trunk with media bypass in Lync Server 2013</span></span>](lync-server-2013-configure-a-trunk-with-media-bypass.md)  
[<span data-ttu-id="a02e5-130">Configurer un Trunk sans dérivation multimédia dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a02e5-130">Configure a trunk without media bypass in Lync Server 2013</span></span>](lync-server-2013-configure-a-trunk-without-media-bypass.md)  
[<span data-ttu-id="a02e5-131">Publier les modifications en attente apportées à la configuration du routage de la voix dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a02e5-131">Publish pending changes to the voice routing configuration in Lync Server 2013</span></span>](lync-server-2013-publish-pending-changes-to-the-voice-routing-configuration.md)  


[<span data-ttu-id="a02e5-132">Options de contournement global de médias dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a02e5-132">Global media bypass options in Lync Server 2013</span></span>](lync-server-2013-global-media-bypass-options.md)  
  

<span data-ttu-id="a02e5-133"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a02e5-133"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

