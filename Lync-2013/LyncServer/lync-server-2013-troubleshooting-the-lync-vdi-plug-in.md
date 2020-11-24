---
title: 'Lync Server 2013 : résolution des problèmes du plug-in Lync VDI'
description: 'Lync Server 2013 : résolution des problèmes du plug-in Lync VDI.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Troubleshooting the Lync VDI plug-in
ms:assetid: 183c9449-b907-409c-b5ed-b02af3bd93ee
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204713(v=OCS.15)
ms:contentKeyID: 48183525
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3cd2c0e3c8a47225f00ce280706dea2287e4dc8b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394316"
---
# <a name="troubleshooting-the-lync-vdi-plug-in-in-lync-server-2013"></a><span data-ttu-id="1f838-103">Résoudre les problèmes du plug-in Lync VDI dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1f838-103">Troubleshooting the Lync VDI plug-in in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1f838-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1f838-104">

<span> </span></span></span>

<span data-ttu-id="1f838-105">_**Dernière modification de la rubrique :** 2012-10-10_</span><span class="sxs-lookup"><span data-stu-id="1f838-105">_**Topic Last Modified:** 2012-10-10_</span></span>

<div>

## <a name="troubleshooting-issues-with-installing-the-lync-vdi-plug-in-on-a-thin-client"></a><span data-ttu-id="1f838-106">Résolution des problèmes liés à l’installation du plug-in Lync VDI sur un client léger</span><span class="sxs-lookup"><span data-stu-id="1f838-106">Troubleshooting Issues with Installing the Lync VDI Plug-in on a Thin Client</span></span>

<span data-ttu-id="1f838-107">Si vous rencontrez des problèmes lors de l’installation du plug-in VDI sur un client léger, vérifiez les points suivants :</span><span class="sxs-lookup"><span data-stu-id="1f838-107">If there are issues with installing the VDI plug-in on a thin client, check the following:</span></span>

  - <span data-ttu-id="1f838-108">Assurez-vous que l’espace est suffisant dans le dossier que vous avez spécifié dans les variables système TEMP et TMP.</span><span class="sxs-lookup"><span data-stu-id="1f838-108">Ensure that there is sufficient space in the folder that you specified in the TEMP and TMP system variables.</span></span>

  - <span data-ttu-id="1f838-p101">Assurez-vous que la protection en écriture est désactivée. Reportez-vous à la documentation du fabricant de votre périphérique pour en savoir plus.</span><span class="sxs-lookup"><span data-stu-id="1f838-p101">Ensure that write-protect is turned off. Refer to your device manufacturer’s documentation for instructions.</span></span>

</div>

<div>

## <a name="troubleshooting-issues-with-pairing"></a><span data-ttu-id="1f838-111">Résolution des problèmes liés au jumelage</span><span class="sxs-lookup"><span data-stu-id="1f838-111">Troubleshooting Issues with Pairing</span></span>

<span data-ttu-id="1f838-112">Lorsque le jumelage enfichable VDI échoue, l’icône de jumelage en bas à droite s’affiche sous la forme d’un « X » rouge, comme illustré ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="1f838-112">When VDI plug-in pairing fails, the pairing icon in the lower right displays as a red “X” as shown:</span></span>

<span data-ttu-id="1f838-113">![Icône VDI de Lync montrant une jumelage réussie](images/JJ204948.303d618c-4bc8-41c4-8553-2475de0d395e(OCS.15).png "Icône VDI de Lync montrant une jumelage réussie")</span><span class="sxs-lookup"><span data-stu-id="1f838-113">![Lync VDI icon showing successful pairing](images/JJ204948.303d618c-4bc8-41c4-8553-2475de0d395e(OCS.15).png "Lync VDI icon showing successful pairing")</span></span>

<span data-ttu-id="1f838-114">Voici quelques raisons possibles d’échecs et des actions correctives que vous pouvez effectuer.</span><span class="sxs-lookup"><span data-stu-id="1f838-114">The following are possible reasons for failures and the corrective actions you can take.</span></span>

  - <span data-ttu-id="1f838-115">**L’utilisateur a entré des informations d’identification incorrectes au moment de la connexion.**</span><span class="sxs-lookup"><span data-stu-id="1f838-115">**The user entered incorrect credentials during sign-in.**</span></span>
    
    <span data-ttu-id="1f838-116">L’utilisateur doit se déconnecter de Lync et se reconnecter avec les informations d’identification appropriées.</span><span class="sxs-lookup"><span data-stu-id="1f838-116">The user should sign out of Lync and sign in again with the correct credentials.</span></span> <span data-ttu-id="1f838-117">La boîte de dialogue de jumelage réapparaît et indique si le jumelage a réussi.</span><span class="sxs-lookup"><span data-stu-id="1f838-117">The pairing dialog box will reappear and show whether pairing is successful.</span></span>

  - <span data-ttu-id="1f838-118">**Une autre instance du client Bureau à distance est en cours d’exécution.**</span><span class="sxs-lookup"><span data-stu-id="1f838-118">**Another instance of the remote desktop client is running.**</span></span>
    
    <span data-ttu-id="1f838-119">S’ils utilisent une connexion Bureau à distance dans Windows, les utilisateurs doivent procéder comme suit :</span><span class="sxs-lookup"><span data-stu-id="1f838-119">If they are using Remote Desktop Connection in Windows, users should do the following:</span></span>
    
    1.  <span data-ttu-id="1f838-120">Démarrez le Gestionnaire des tâches : appuyez sur **Alt+Ctrl+Suppr**, puis cliquez sur **Démarrer le Gestionnaire des tâches**.</span><span class="sxs-lookup"><span data-stu-id="1f838-120">Start Task Manager: Press **Alt+Ctrl+Delete**, and then click **Start Task Manager**.</span></span>
    
    2.  <span data-ttu-id="1f838-121">Cliquez sur l’onglet **Processus** et recherchez tous les processus nommés **mstsc.exe** dans la liste.</span><span class="sxs-lookup"><span data-stu-id="1f838-121">Click the **Processes** tab and look for all processes named **mstsc.exe** in the list.</span></span>
    
    3.  <span data-ttu-id="1f838-122">Mettez chaque processus **mstsc.exe** en surbrillance et cliquez sur **Arrêter le processus**. </span><span class="sxs-lookup"><span data-stu-id="1f838-122">Highlight each **mstsc.exe** process and then click **End Process**.</span></span>
    
    4.  <span data-ttu-id="1f838-123">Démarrez une nouvelle session Bureau à distance et réessayez de vous connecter. </span><span class="sxs-lookup"><span data-stu-id="1f838-123">Start a new remote desktop session and try connecting again.</span></span>

  - <span data-ttu-id="1f838-124">**Les fichiers nécessaires n’ont pas été installés correctement.**</span><span class="sxs-lookup"><span data-stu-id="1f838-124">**The necessary files did not install correctly.**</span></span>
    
    <span data-ttu-id="1f838-125">Une fois que le plug-in est installé sur l’ordinateur local, les fichiers suivants doivent figurer sous C : \\ Program Files \\ Microsoft Office \\ Office15 (ou la lettre de lecteur appropriée) :</span><span class="sxs-lookup"><span data-stu-id="1f838-125">After the plug-in is installed on the local computer, the following files should be present under C:\\Program Files\\Microsoft Office\\Office15 (or the appropriate drive letter):</span></span>
    
      - <span data-ttu-id="1f838-126">LyncVdiPlugin.dll</span><span class="sxs-lookup"><span data-stu-id="1f838-126">LyncVdiPlugin.dll</span></span>
    
      - <span data-ttu-id="1f838-127">UcVdi.dll</span><span class="sxs-lookup"><span data-stu-id="1f838-127">UcVdi.dll</span></span>
    
    <span data-ttu-id="1f838-128">S’il existe des problèmes avec le jumelage d’infrastructure VDI, assurez-vous que ces fichiers sont présents sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="1f838-128">If there are any issues with VDI pairing, check to make sure that these files are present on the local computer.</span></span>

  - <span data-ttu-id="1f838-129">**Le client Lync s’exécute sur l’ordinateur local.**</span><span class="sxs-lookup"><span data-stu-id="1f838-129">**The Lync client is running on the local computer.**</span></span>
    
    <span data-ttu-id="1f838-130">Pour utiliser le plug-in Lync VDI, un client Lync ne doit pas être en cours d’exécution sur l’ordinateur local ; sinon, le jumelage échoue.</span><span class="sxs-lookup"><span data-stu-id="1f838-130">To use the Lync VDI plugin, a Lync client must not be running on the local computer, otherwise pairing will fail.</span></span> <span data-ttu-id="1f838-131">En règle générale, l’utilisateur ne doit pas installer un client Lync sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="1f838-131">As a best practice, the user should not install a Lync client on the local computer.</span></span>

<span data-ttu-id="1f838-132"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1f838-132"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

