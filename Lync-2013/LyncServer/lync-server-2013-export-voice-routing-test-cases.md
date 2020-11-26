---
title: 'Lync Server 2013 : Exportation des cas de test de routage des communications vocales'
description: 'Lync Server 2013 : exporter des cas de test de routage vocal.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Export voice routing test cases
ms:assetid: 489ac472-1a35-4755-b390-48f7cdf31e94
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425957(v=OCS.15)
ms:contentKeyID: 48184050
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 934bd183a17c46cf82fe5bc04faaa55a9bbe4731
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428348"
---
# <a name="export-voice-routing-test-cases-in-lync-server-2013"></a><span data-ttu-id="9dbf5-103">Exportation des cas de test de routage des communications vocales dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9dbf5-103">Export voice routing test cases in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9dbf5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9dbf5-104">

<span> </span></span></span>

<span data-ttu-id="9dbf5-105">_**Dernière modification de la rubrique :** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="9dbf5-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="9dbf5-106">Les scénarios de test vous permettent de tester les itinéraires vocaux au sein de votre organisation : vous définissez des éléments tels que le numéro à composer, le plan de numérotation et la politique vocale à utiliser, et Lync Server peut alors vérifier que le numéro fourni est bien acheminé au réseau PSTN.</span><span class="sxs-lookup"><span data-stu-id="9dbf5-106">Test cases provide a way for you to test voice routes in your organization: you define such things as the number to be dialed and the dial plan and voice policy to be employed, and Lync Server can then verify that, given those conditions, the supplied number can successfully be routed to the PSTN network.</span></span>

<span data-ttu-id="9dbf5-107">Les cas de test, qui peuvent être créés à l’aide du panneau de configuration de Lync Server, sont généralement enregistrés uniquement sur le serveur où le cas a été créé et exécuté à l’origine.</span><span class="sxs-lookup"><span data-stu-id="9dbf5-107">Test cases, which can be created by using Lync Server Control Panel, are typically saved only on the server where the case was originally created and run.</span></span> <span data-ttu-id="9dbf5-108">Toutefois, ces cas de test peuvent être exportés sous forme de fichiers XML (avec l’extension. vtest), puis importés sur d’autres serveurs.</span><span class="sxs-lookup"><span data-stu-id="9dbf5-108">However, these test cases can be exported as XML files (with the .vtest extension) and then imported on other servers.</span></span> <span data-ttu-id="9dbf5-109">Cela vous permet d’exécuter les mêmes tests sur différents ordinateurs situés à différents endroits de votre topologie.</span><span class="sxs-lookup"><span data-stu-id="9dbf5-109">This enables you to run the same tests on different computers located at different points in your topology.</span></span>

<div>

## <a name="to-export-a-voice-routing-test-case"></a><span data-ttu-id="9dbf5-110">Pour exporter un cas de test de routage vocal</span><span class="sxs-lookup"><span data-stu-id="9dbf5-110">To export a voice routing test case</span></span>

1.  <span data-ttu-id="9dbf5-111">Dans le panneau de configuration de Lync Server, cliquez sur **routage des communications vocales** , puis cliquez sur **tester le routage vocal**.</span><span class="sxs-lookup"><span data-stu-id="9dbf5-111">In Lync Server Control Panel, click **Voice Routing** and then click **Test Voice Routing**.</span></span>

2.  <span data-ttu-id="9dbf5-112">Dans l’onglet **tester le routage vocal** , sélectionnez le cas de test (ou les cas de test) à exporter.</span><span class="sxs-lookup"><span data-stu-id="9dbf5-112">On the **Test Voice Routing** tab, select the test case (or test cases) to be exported.</span></span> <span data-ttu-id="9dbf5-113">Pour sélectionner plusieurs cas de test, cliquez sur la première case à exporter, puis maintenez la touche CTRL enfoncée et sélectionnez les cas supplémentaires à exporter.</span><span class="sxs-lookup"><span data-stu-id="9dbf5-113">To select multiple test cases, click the first case to be exported, then hold down the Ctrl key and select the additional cases to be exported.</span></span>

3.  <span data-ttu-id="9dbf5-114">Cliquez sur **action**, puis sur **Exporter les cas de test**.</span><span class="sxs-lookup"><span data-stu-id="9dbf5-114">Click **Action**, then click **Export test cases**.</span></span>

4.  <span data-ttu-id="9dbf5-115">Dans la boîte de dialogue **Enregistrer sous** , sélectionnez un dossier pour stocker les cas de test exportés et tapez un nom pour le fichier XML obtenu dans la zone **nom de fichier** .</span><span class="sxs-lookup"><span data-stu-id="9dbf5-115">In the **Save As** dialog box, select a folder to store the exported test cases and type a name for the resulting XML file in the **File name** box.</span></span> <span data-ttu-id="9dbf5-116">Notez que si vous exportez plusieurs cas de tests, tous ces cas de test seront enregistrés dans un fichier XML unique.</span><span class="sxs-lookup"><span data-stu-id="9dbf5-116">Note that if you are exporting multiple tests cases all of these test cases will be saved to a single XML file.</span></span>

5.  <span data-ttu-id="9dbf5-117">Pour enregistrer les cas de test, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="9dbf5-117">To save the test cases, click **Save**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="9dbf5-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9dbf5-118">See Also</span></span>


[<span data-ttu-id="9dbf5-119">Importation des cas de test de routage des communications vocales dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9dbf5-119">Import voice routing test cases in Lync Server 2013</span></span>](lync-server-2013-import-voice-routing-test-cases.md)  
  

<span data-ttu-id="9dbf5-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9dbf5-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

