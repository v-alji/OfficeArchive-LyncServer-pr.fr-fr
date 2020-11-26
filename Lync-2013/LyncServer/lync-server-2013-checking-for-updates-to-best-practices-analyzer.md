---
title: 'Lync Server 2013 : recherche de mises à jour apportées à l’analyseur de meilleures pratiques'
description: 'Lync Server 2013 : recherche de mises à jour apportées à l’analyseur de meilleures pratiques.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Checking for updates to Best Practices Analyzer
ms:assetid: 06f1da8b-99a7-4871-911e-bfb7542baced
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204645(v=OCS.15)
ms:contentKeyID: 48183307
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4c2662f143be9fc672461715d1c3da867886e686
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434913"
---
# <a name="checking-for-updates-to-best-practices-analyzer-in-lync-server-2013"></a><span data-ttu-id="abfb2-103">Vérification des mises à jour apportées par l’analyseur de meilleures pratiques dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="abfb2-103">Checking for updates to Best Practices Analyzer in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="abfb2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="abfb2-104">

<span> </span></span></span>

<span data-ttu-id="abfb2-105">_**Dernière modification de la rubrique :** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="abfb2-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="abfb2-106">Lorsque vous démarrez le vérificateur de meilleures pratiques, l’outil vous propose une option pour rechercher les dernières mises à jour apportées à l’outil.</span><span class="sxs-lookup"><span data-stu-id="abfb2-106">When you start Best Practices Analyzer, the tool provides you with an option to search for the latest updates to the tool.</span></span> <span data-ttu-id="abfb2-107">Si une mise à jour est disponible, vous pouvez télécharger la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="abfb2-107">If an update is available, you can download the update.</span></span> <span data-ttu-id="abfb2-108">Si vous choisissez de ne pas télécharger les mises à jour, ou si les meilleurs analyseurs ne sont pas en mesure d’accéder à Internet, vous pouvez continuer à utiliser la version déjà installée sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="abfb2-108">If you choose not to download updates, or if Best Practices Analyzer cannot access the Internet, you can continue to use the version that is already on the computer.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="abfb2-109">Si vous avez besoin d’une authentification par proxy pour accéder à Internet, l’analyseur de meilleures pratiques ne peut pas accéder aux nouvelles mises à jour à télécharger.</span><span class="sxs-lookup"><span data-stu-id="abfb2-109">If you need proxy authentication to access the Internet, Best Practices Analyzer cannot access new updates for you to download.</span></span> <span data-ttu-id="abfb2-110">Toutefois, vous pouvez télécharger manuellement la dernière version de RtcBPA.msi à partir du centre de téléchargement Microsoft à l’adresse <A href="https://go.microsoft.com/fwlink/p/?linkid=266539">https://go.microsoft.com/fwlink/p/?linkId=266539</A> .</span><span class="sxs-lookup"><span data-stu-id="abfb2-110">However, you can manually download the latest version of RtcBPA.msi from the Microsoft Download Center at <A href="https://go.microsoft.com/fwlink/p/?linkid=266539">https://go.microsoft.com/fwlink/p/?linkId=266539</A>.</span></span> <span data-ttu-id="abfb2-111">Après avoir téléchargé le fichier, vous pouvez le copier sur l’ordinateur sur lequel vous voulez mettre à jour les meilleurs analyseurs et utiliser le fichier. msi pour installer la nouvelle version de l’outil sur cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="abfb2-111">After downloading the file, you can copy it to the computer on which you want to update Best Practices Analyzer and use the .msi file to install the new version of the tool on that computer.</span></span>



</div>

<span data-ttu-id="abfb2-112">Pour mettre à jour les règles de l’analyseur de meilleures pratiques, vous devez exécuter l’outil en tant qu’administrateur sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="abfb2-112">To update Best Practices Analyzer rules, you must run the tool as an Administrator on the local computer.</span></span> <span data-ttu-id="abfb2-113">Si vous n’avez pas ouvert de session à l’aide d’un compte membre du groupe administrateurs et des mises à jour sont détectées, fermez l’analyseur de meilleures pratiques, puis utilisez la procédure suivante pour démarrer le programme.</span><span class="sxs-lookup"><span data-stu-id="abfb2-113">If you are not logged on using an account that is a member of the Administrators group and updates are detected, close Best Practices Analyzer, and then use the following procedure to start the program.</span></span>

<div>

## <a name="to-open-best-practices-analyzer-as-administrator-to-check-for-updates"></a><span data-ttu-id="abfb2-114">Pour ouvrir l’outil de recherche de meilleures pratiques en tant qu’administrateur pour rechercher les mises à jour</span><span class="sxs-lookup"><span data-stu-id="abfb2-114">To open Best Practices Analyzer as Administrator to check for updates</span></span>

1.  <span data-ttu-id="abfb2-115">Sur un ordinateur sur lequel le système d’analyse des recommandations est installé, cliquez sur **Démarrer**, pointez sur **Microsoft Lync Server 2013**, cliquez avec le bouton droit sur **Analyseur de meilleures pratiques**, puis cliquez sur **exécuter en tant qu’administrateur**.</span><span class="sxs-lookup"><span data-stu-id="abfb2-115">On a computer on which Best Practices Analyzer is installed, click **Start**, point to **Microsoft Lync Server 2013**, right-click **Best Practices Analyzer**, and then click **Run as administrator**.</span></span>

2.  <span data-ttu-id="abfb2-116">Spécifiez les informations d’identification d’un compte membre du groupe administrateurs.</span><span class="sxs-lookup"><span data-stu-id="abfb2-116">Specify credentials of an account that is a member of the Administrators group.</span></span>

<span data-ttu-id="abfb2-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="abfb2-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

