---
title: 'Lync Server 2013 : modification d’un itinéraire vocal'
description: 'Lync Server 2013 : modifier un itinéraire vocal.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Modify a voice route
ms:assetid: afc562cc-8807-489b-8850-dbbe1c1ab9f5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412838(v=OCS.15)
ms:contentKeyID: 48185143
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0aa507f3d0f459dd200b9c772f3a330d7da36197
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425534"
---
# <a name="modify-a-voice-route-in-lync-server-2013"></a><span data-ttu-id="863a3-103">Modifier un itinéraire vocal dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="863a3-103">Modify a voice route in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="863a3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="863a3-104">

<span> </span></span></span>

<span data-ttu-id="863a3-105">_**Dernière modification de la rubrique :** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="863a3-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="863a3-106">Cette rubrique explique comment modifier un itinéraire vocal.</span><span class="sxs-lookup"><span data-stu-id="863a3-106">This topic explains how to edit a voice route.</span></span> <span data-ttu-id="863a3-107">Pour créer un nouvel itinéraire, reportez-vous à [la rubrique Création d’un itinéraire vocal dans Lync Server 2013](lync-server-2013-create-a-voice-route.md).</span><span class="sxs-lookup"><span data-stu-id="863a3-107">To create a new route, see [Create a voice route in Lync Server 2013](lync-server-2013-create-a-voice-route.md).</span></span>

<div>

## <a name="to-modify-a-voice-route"></a><span data-ttu-id="863a3-108">Pour modifier un itinéraire des communications vocales</span><span class="sxs-lookup"><span data-stu-id="863a3-108">To modify a voice route</span></span>

1.  <span data-ttu-id="863a3-109">Connectez-vous à l’ordinateur en tant que membre du groupe RTCUniversalServerAdmins ou en tant que membre du rôle CsVoiceAdministrator, CsServerAdministrator ou CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="863a3-109">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the CsVoiceAdministrator, CsServerAdministrator, or CsAdministrator role.</span></span> <span data-ttu-id="863a3-110">Pour plus d’informations, reportez-vous à la section [délégation des autorisations de configuration dans Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="863a3-110">For details, see [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="863a3-111">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="863a3-111">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="863a3-112">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="863a3-112">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="863a3-113">Dans la barre de navigation de gauche, cliquez sur **Routage des communications vocales**, puis sur **Itinéraire**.</span><span class="sxs-lookup"><span data-stu-id="863a3-113">In the left navigation bar, click **Voice Routing**, and then click **Route**.</span></span>

4.  <span data-ttu-id="863a3-114">Dans la page **Itinéraire**, utilisez l’une des méthodes ci-dessous pour modifier un itinéraire des communications vocales :</span><span class="sxs-lookup"><span data-stu-id="863a3-114">On the **Route** page, use either of the following methods to modify a voice route:</span></span>
    
      - <span data-ttu-id="863a3-115">Sélectionnez un nom d’itinéraire des communications vocales, cliquez sur **Modifier**, puis sur **Afficher les détails**.</span><span class="sxs-lookup"><span data-stu-id="863a3-115">Click a voice route name, click **Edit**, and then click **Show details**.</span></span>
    
      - <span data-ttu-id="863a3-p104">Sélectionnez un nom d’itinéraire des communications vocales, cliquez sur **Modifier**, sur **Copier** et enfin sur **Coller**. Sélectionnez la copie de l’itinéraire des communications vocales créée à l’instant, cliquez sur **Modifier**, puis sur **Afficher les détails**.</span><span class="sxs-lookup"><span data-stu-id="863a3-p104">Click a voice route name, click **Edit**, click **Copy**, and then click **Paste**. Click the new copy of the voice route that you just created, click **Edit**, and then click **Show details**.</span></span>

5.  <span data-ttu-id="863a3-118">Dans la page **Modifier l’itinéraire des communications vocales**, dans le champ **Nom**, tapez un nom descriptif pour l’itinéraire des communications vocales.</span><span class="sxs-lookup"><span data-stu-id="863a3-118">In the **Name** field on the **Edit Voice Route** page, type a descriptive name for the voice route.</span></span>

6.  <span data-ttu-id="863a3-119">(Facultatif) Dans le champ **Description**, tapez une description supplémentaire du nouvel itinéraire des communications vocales.</span><span class="sxs-lookup"><span data-stu-id="863a3-119">(Optional) In the **Description** field, type in additional descriptive information for the voice route.</span></span>

7.  <span data-ttu-id="863a3-120">Pour spécifier les modèles que cet itinéraire doit prendre en compte, vous pouvez générer une expression régulière à l’aide de l’outil **Créer un modèle à suivre** ou l’écrire manuellement.</span><span class="sxs-lookup"><span data-stu-id="863a3-120">To specify the patterns you want this route to accommodate, you can either use the **Build a pattern to match** tool to generate a regular expression, or write the regular expression manually.</span></span>
    
      - <span data-ttu-id="863a3-p105">Pour utiliser l’outil **Créer un modèle à suivre** afin de générer une expression régulière, entrez les valeurs comme suit. Vous pouvez spécifier deux types de correspondance de modèles :</span><span class="sxs-lookup"><span data-stu-id="863a3-p105">To use the **Build a pattern to match** tool to generate a regular expression, enter values as follows. You can specify two types of pattern matching:</span></span>
        
          - <span data-ttu-id="863a3-123">**Chiffres de départ pour les nombres que vous souhaitez autoriser :** Entrez les valeurs de préfixe que ce routage doit accepter (y compris les touches de début + si nécessaire).</span><span class="sxs-lookup"><span data-stu-id="863a3-123">**Starting digits for numbers that you want to allow:** Enter prefix values that this route must accommodate (including the leading + if needed).</span></span> <span data-ttu-id="863a3-124">Par exemple, tapez **+ 425** , puis cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="863a3-124">For example, type **+425** and then click **Add**.</span></span> <span data-ttu-id="863a3-125">Répétez cette procédure pour chaque valeur de préfixe que vous voulez inclure dans l’itinéraire.</span><span class="sxs-lookup"><span data-stu-id="863a3-125">Repeat this for each prefix value that you want to include in the route.</span></span>
        
          - <span data-ttu-id="863a3-126">**Exceptions :** Si vous voulez spécifier une ou plusieurs exceptions pour une valeur de préfixe, mettez en surbrillance le préfixe et cliquez sur **exceptions**.</span><span class="sxs-lookup"><span data-stu-id="863a3-126">**Exceptions:** If you want to specify one or more exceptions for a prefix value, highlight the prefix and click **Exceptions**.</span></span> <span data-ttu-id="863a3-127">Tapez une ou plusieurs valeurs pour les modèles correspondants pour lesquels vous ne souhaitez *pas* que cet itinéraire puisse être pris en charge.</span><span class="sxs-lookup"><span data-stu-id="863a3-127">Type in one or more values for the matching patterns that you do *not* want this route to accommodate.</span></span> <span data-ttu-id="863a3-128">Par exemple, pour exclure les nombres commençant par + 425237 de l’itinéraire, entrez la valeur **+ 425237** dans le champ **exceptions** , puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="863a3-128">For example, to exclude numbers starting with +425237 from the route, enter a value of **+425237** in the **Exceptions** field, and then click **OK**.</span></span>
    
      - <span data-ttu-id="863a3-129">Pour définir manuellement le modèle de correspondance, cliquez sur **Modifier** dans l’outil **Créer un modèle à suivre**, puis entrez une expression régulière .NET Framework afin de spécifier le modèle de correspondance pour les numéros de téléphone de destination auxquels l’itinéraire est appliqué.</span><span class="sxs-lookup"><span data-stu-id="863a3-129">To define the matching pattern manually, click **Edit** in the **Build a pattern to match** tool and then type in a .NET Framework regular expression to specify the matching pattern for destination phone numbers to which the route is applied.</span></span> <span data-ttu-id="863a3-130">Pour plus d’informations sur la façon d’écrire des expressions régulières, voir « expressions régulières .NET Framework » à l’adresse [https://go.microsoft.com/fwlink/p/?linkId=140927](https://go.microsoft.com/fwlink/p/?linkid=140927) .</span><span class="sxs-lookup"><span data-stu-id="863a3-130">For information about how to write regular expressions, see ".NET Framework Regular Expressions" at [https://go.microsoft.com/fwlink/p/?linkId=140927](https://go.microsoft.com/fwlink/p/?linkid=140927).</span></span>

8.  <span data-ttu-id="863a3-p109">Sélectionnez l’option **Supprimer l’ID de l’appelant** si vous ne souhaitez pas que l’ID du téléphone à l’origine de l’appel sortant soit affiché au destinataire. Si vous sélectionnez cette option, vous devez spécifier un **autre ID de l’appelant** qui s’affichera pour l’ID d’appelant du destinataire.</span><span class="sxs-lookup"><span data-stu-id="863a3-p109">Select **Suppress caller ID** if you do not want the ID of the phone that is making the outbound call to appear to the call recipient. If you select this option, you must specify an **Alternate caller ID** that will appear on the recipient’s caller ID display.</span></span>

9.  <span data-ttu-id="863a3-133">Pour associer une ou plusieurs jonctions RTC à l’itinéraire des communications vocales, cliquez sur **Ajouter**, puis sélectionnez une jonction dans la liste.</span><span class="sxs-lookup"><span data-stu-id="863a3-133">To associate one or more public switched telephone network (PSTN) trunks with the voice route, click **Add**, and then select a trunk from the list.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="863a3-134">Si votre déploiement inclut des serveurs de médiation Microsoft Office Communications Server 2007 R2, ils sont également disponibles dans la liste.</span><span class="sxs-lookup"><span data-stu-id="863a3-134">If your deployment includes any Microsoft Office Communications Server 2007 R2 Mediation Servers, they will also be available in the list.</span></span>

    
    </div>

10. <span data-ttu-id="863a3-135">Pour associer une ou plusieurs utilisations RTC à l’itinéraire vocal, cliquez sur **Sélectionner** et sélectionnez un enregistrement dans la liste des enregistrements d’utilisation RTC définis pour votre déploiement voix entreprise.</span><span class="sxs-lookup"><span data-stu-id="863a3-135">To associate one or more PSTN usages with the voice route, click **Select** and choose a record from the list of PSTN usage records that have been defined for your Enterprise Voice deployment.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="863a3-136">Pour afficher les propriétés de chacun des enregistrements d’utilisation RTC disponibles, voir <A href="lync-server-2013-view-pstn-usage-records.md">afficher les enregistrements d’utilisation RTC dans Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="863a3-136">To view the properties of each of the available PSTN usage records, see <A href="lync-server-2013-view-pstn-usage-records.md">View PSTN usage records in Lync Server 2013</A>.</span></span><BR><span data-ttu-id="863a3-137">Pour créer ou modifier des enregistrements d’utilisation RTC, voir <A href="lync-server-2013-create-a-voice-policy-and-configure-pstn-usage-records.md">créer une stratégie vocale et configurer les enregistrements d’utilisation RTC dans Lync server 2013</A> ou <A href="lync-server-2013-modify-a-voice-policy-and-configure-pstn-usage-records.md">modifier une stratégie vocale et configurer les enregistrements d’utilisation RTC dans Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="863a3-137">To create or edit PSTN usage records, see <A href="lync-server-2013-create-a-voice-policy-and-configure-pstn-usage-records.md">Create a voice policy and configure PSTN usage records in Lync Server 2013</A> or <A href="lync-server-2013-modify-a-voice-policy-and-configure-pstn-usage-records.md">Modify a voice policy and configure PSTN usage records in Lync Server 2013</A>.</span></span>

    
    </div>

11. <span data-ttu-id="863a3-p110">Organisez les enregistrements d’utilisation RTC pour obtenir des performances optimales. Pour modifier la position d’un enregistrement dans la liste, sélectionnez son nom, puis cliquez sur la flèche vers le haut ou vers le bas.</span><span class="sxs-lookup"><span data-stu-id="863a3-p110">Arrange the PSTN usage records for optimum performance. To change a record’s position in the list, highlight the record name and click the up or down arrow.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="863a3-140">Contrairement à une stratégie de voix dans laquelle l’ordre d’apparition des enregistrements d’utilisation RTC est important, l’ordre des enregistrements d’utilisation RTC dans un itinéraire des communications vocales n’est pas significatif.</span><span class="sxs-lookup"><span data-stu-id="863a3-140">In contrast to a voice policy where the order in which PSTN usage records are listed is important, the order of PSTN usage records in a voice route is insignificant.</span></span> <span data-ttu-id="863a3-141">Il est toutefois recommandé d’organiser la liste par fréquence d’utilisation, par exemple : RedmondLocal, RedmondLongDist, RedmondInternational, RedmondBackup.</span><span class="sxs-lookup"><span data-stu-id="863a3-141">However, we recommend that you organize the list by frequency of use, for example: RedmondLocal, RedmondLongDist, RedmondInternational, RedmondBackup.</span></span> <span data-ttu-id="863a3-142">(Lync Server parcourt la liste à partir du haut vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="863a3-142">(Lync Server traverses the list from the top down.)</span></span>

    
    </div>

12. <span data-ttu-id="863a3-p112">(Facultatif) Tapez une valeur dans le champ **Entrez un numéro traduit à tester** et cliquez sur **OK**. Les résultats du test sont affichés sous le champ.</span><span class="sxs-lookup"><span data-stu-id="863a3-p112">(Optional) Type a value into the **Enter a translated number to test** field and click **Go**. The test results are displayed under the field.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="863a3-145">Vous pouvez enregistrer un itinéraire vocal qui ne transmet pas encore le test et le reconfigurer plus tard.</span><span class="sxs-lookup"><span data-stu-id="863a3-145">You can save a voice route that does not yet pass the test and then reconfigure it later.</span></span> <span data-ttu-id="863a3-146">Pour plus d’informations, consultez <A href="lync-server-2013-test-voice-routing.md">tester le routage vocal dans Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="863a3-146">For details, see <A href="lync-server-2013-test-voice-routing.md">Test voice routing in Lync Server 2013</A>.</span></span>

    
    </div>

13. <span data-ttu-id="863a3-147">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="863a3-147">Click **OK**.</span></span>

14. <span data-ttu-id="863a3-148">Dans la page **Itinéraire**, cliquez sur **Valider**, puis sur **Tout valider**.</span><span class="sxs-lookup"><span data-stu-id="863a3-148">On the **Route** page, click **Commit**, and then click **Commit all**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="863a3-149">Chaque fois que vous créez ou modifiez un itinéraire des communications vocales, vous devez exécuter la commande <STRONG>Tout valider</STRONG> pour publier la modification de la configuration.</span><span class="sxs-lookup"><span data-stu-id="863a3-149">Whenever you create or modify a voice route, you must run the <STRONG>Commit all</STRONG> command to publish the configuration change.</span></span> <span data-ttu-id="863a3-150">Pour plus d’informations, reportez-vous <A href="lync-server-2013-publish-pending-changes-to-the-voice-routing-configuration.md">à la rubrique publier des modifications en attente sur la configuration de l’acheminement de la voix dans Lync Server 2013</A> dans la documentation</span><span class="sxs-lookup"><span data-stu-id="863a3-150">For details, see <A href="lync-server-2013-publish-pending-changes-to-the-voice-routing-configuration.md">Publish pending changes to the voice routing configuration in Lync Server 2013</A> in the Operations documentation.</span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="863a3-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="863a3-151">See Also</span></span>


[<span data-ttu-id="863a3-152">Créer un itinéraire vocal dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="863a3-152">Create a voice route in Lync Server 2013</span></span>](lync-server-2013-create-a-voice-route.md)  
[<span data-ttu-id="863a3-153">Afficher les enregistrements d’utilisation RTC dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="863a3-153">View PSTN usage records in Lync Server 2013</span></span>](lync-server-2013-view-pstn-usage-records.md)  
[<span data-ttu-id="863a3-154">Créer une stratégie de voix et configurer les enregistrements d’utilisation RTC dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="863a3-154">Create a voice policy and configure PSTN usage records in Lync Server 2013</span></span>](lync-server-2013-create-a-voice-policy-and-configure-pstn-usage-records.md)  
[<span data-ttu-id="863a3-155">Modifier une stratégie vocale et configurer les enregistrements d’utilisation RTC dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="863a3-155">Modify a voice policy and configure PSTN usage records in Lync Server 2013</span></span>](lync-server-2013-modify-a-voice-policy-and-configure-pstn-usage-records.md)  
[<span data-ttu-id="863a3-156">Publier les modifications en attente apportées à la configuration du routage de la voix dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="863a3-156">Publish pending changes to the voice routing configuration in Lync Server 2013</span></span>](lync-server-2013-publish-pending-changes-to-the-voice-routing-configuration.md)  


[<span data-ttu-id="863a3-157">Test du routage des communications vocales dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="863a3-157">Test voice routing in Lync Server 2013</span></span>](lync-server-2013-test-voice-routing.md)  
  

<span data-ttu-id="863a3-158"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="863a3-158"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

