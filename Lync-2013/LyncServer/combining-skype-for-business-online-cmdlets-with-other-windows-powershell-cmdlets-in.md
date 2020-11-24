---
title: Combiner les applets de applet de Skype entreprise Online avec d’autres cmdlets Windows PowerShell dans
description: Combinant les applets de applet de Skype entreprise Online et d’autres cmdlets Windows PowerShell.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Combining Skype for Business Online cmdlets with other Windows PowerShell cmdlets
ms:assetid: 8bb8800a-f966-4570-8c8b-db87a91ad783
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362816(v=OCS.15)
ms:contentKeyID: 56558835
ms.date: 05/04/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5bd18f60891d48a54eb2f77f189ea8417e0b5e93
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394444"
---
# <a name="combining-skype-for-business-online-cmdlets-with-other-windows-powershell-cmdlets-in"></a><span data-ttu-id="25e74-103">Combiner les applets de applet de Skype entreprise Online avec d’autres cmdlets Windows PowerShell dans</span><span class="sxs-lookup"><span data-stu-id="25e74-103">Combining Skype for Business Online cmdlets with other Windows PowerShell cmdlets in</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="25e74-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="25e74-104">

<span> </span></span></span>

<span data-ttu-id="25e74-105">_**Dernière modification de la rubrique :** 2013-07-05_</span><span class="sxs-lookup"><span data-stu-id="25e74-105">_**Topic Last Modified:** 2013-07-05_</span></span>

<span data-ttu-id="25e74-106">Lorsque vous vous connectez à Skype entreprise Online à l’aide de Windows PowerShell 40, vous pouvez utiliser les applets de applet de ligne Skype entreprise online.</span><span class="sxs-lookup"><span data-stu-id="25e74-106">When you connect to Skype for Business Online by using Windows PowerShell, approximately 40 Skype for Business Online cmdlets will available for your use.</span></span> <span data-ttu-id="25e74-107">Toutefois, vous n’êtes pas limité à l’utilisation de ces applets de connexion 40 lors de la gestion de Skype entreprise online.</span><span class="sxs-lookup"><span data-stu-id="25e74-107">However, you are not limited to using just those 40 cmdlets when managing Skype for Business Online.</span></span> <span data-ttu-id="25e74-108">Outre les applets de connexion Skype entreprise Online, vous pouvez également utiliser n’importe quelle applet de cmdlet Windows PowerShell installée sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="25e74-108">In addition to the Skype for Business Online cmdlets, you can also use any other Windows PowerShell cmdlets that are installed on your computer.</span></span> <span data-ttu-id="25e74-109">(Lors de l’installation de Windows PowerShell 3,0, des centaines d’applets de construction Windows PowerShell sont également installés.) Vos commandes peuvent mélanger et faire correspondre des applets de commande Skype entreprise Online et d’autres cmdlets disponibles sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="25e74-109">(When you install Windows PowerShell 3.0, hundreds of core Windows PowerShell cmdlets are installed, as well.) Your commands can mix and match Skype for Business Online cmdlets and any other cmdlets available on your computer.</span></span>

<span data-ttu-id="25e74-110">Bien que le cours complet dans Windows PowerShell 3,0 ne dépasse pas le cadre de cet article, voici quelques exemples qui vous montrent pourquoi vous voudrez peut-être mélanger et faire correspondre des cmdlets.</span><span class="sxs-lookup"><span data-stu-id="25e74-110">Although a complete course in Windows PowerShell 3.0 goes beyond the scope of this article, here are a few examples that show why you might want to mix and match cmdlets.</span></span> <span data-ttu-id="25e74-111">Tout d’abord, aucune des applets de commande de Skype entreprise Online ne comprend une commande Imprimer et aucune commande de ce type n’est disponible dans la console Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="25e74-111">First of all, none of the Skype for Business Online cmdlets include a Print command, and no such command can be found in the Windows PowerShell console, either.</span></span> <span data-ttu-id="25e74-112">Comment obtenir une impression des informations récupérées par une cmdlet ?</span><span class="sxs-lookup"><span data-stu-id="25e74-112">So how do you get a printout of the information retrieved by a cmdlet?</span></span> <span data-ttu-id="25e74-113">Pour récupérer les informations, vous pouvez récupérer les informations, puis les envoyer à l’applet de **connexion Out-Printer** :</span><span class="sxs-lookup"><span data-stu-id="25e74-113">One way is to retrieve the information, and then send that information to the **Out-Printer** cmdlet:</span></span>

    Get-CsTenant | Out-Printer

<span data-ttu-id="25e74-114">Dans la mesure où aucun paramètre supplémentaire n’est inclus, toutes les informations renvoyées par l’applet de **connexion hors imprimante** seront imprimées sur l’imprimante par défaut.</span><span class="sxs-lookup"><span data-stu-id="25e74-114">Because no additional parameters are included, all the information returned by **the Out-Printer** cmdlet will be printed to the default printer.</span></span>

<span data-ttu-id="25e74-115">De même, aucune des applets de connexion Skype entreprise Online ne comprend un paramètre qui vous permet d’enregistrer les données dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="25e74-115">Likewise, none of the Skype for Business Online cmdlets include a parameter that allows you to save data to a file.</span></span> <span data-ttu-id="25e74-116">Ce n’est pas tout : cette commande utilise l’applet de commande **out-file** pour enregistrer les informations renvoyées dans le fichier texte C : \\ logs \\Tenants.txt :</span><span class="sxs-lookup"><span data-stu-id="25e74-116">But that’s OK: this command uses the **Out-File** cmdlet to save the returned information to the text file C:\\Logs\\Tenants.txt:</span></span>

    Get-Tenant | Out-File -FilePath "C:\Logs\Tenants.txt"

<span data-ttu-id="25e74-117">Cette commande utilise l’applet de commande **Select-Object** pour limiter les données renvoyées et affichées à l’écran.</span><span class="sxs-lookup"><span data-stu-id="25e74-117">And this command uses the **Select-Object** cmdlet to limit the data that is returned and displayed onscreen.</span></span> <span data-ttu-id="25e74-118">Dans cet exemple, l’applet de connexion [Get-CsOnlineUser](https://technet.microsoft.com/library/JJ994026(v=OCS.15)) récupère des informations pour tous vos utilisateurs de Skype entreprise Online, et l’applet de connexion **Select-Object** est utilisée pour limiter les données affichées à la valeur d’identité de l’utilisateur et à sa stratégie d’archivage :</span><span class="sxs-lookup"><span data-stu-id="25e74-118">In this example, the [Get-CsOnlineUser](https://technet.microsoft.com/library/JJ994026(v=OCS.15)) cmdlet retrieves information for all of your Skype for Business Online users, and then the **Select-Object** cmdlet is used to limit the displayed data to the user’s Identity value and their archiving policy:</span></span>

    Get-CsOnlineUser | Select-Object Identity, ArchivingPolicy

<span data-ttu-id="25e74-119">Étant donné que des centaines de cmdlets peuvent être utilisées sur votre ordinateur, il est possible que vous ayez des difficultés à identifier les applets de applet de connexion de Skype entreprise Online et celles qui ne le sont pas.</span><span class="sxs-lookup"><span data-stu-id="25e74-119">Because there will be hundreds of cmdlets available for use on your computer, you might have difficulty determining which cmdlets are Skype for Business Online cmdlets and which ones are not.</span></span> <span data-ttu-id="25e74-120">Pour renvoyer une liste des applets de applet de Skype entreprise Online (et uniquement les applets de connexion Skype entreprise Online), vous devez d’abord déterminer le nom du module Windows PowerShell temporaire contenant toutes les applets de connexion Skype entreprise online.</span><span class="sxs-lookup"><span data-stu-id="25e74-120">To return a list of the Skype for Business Online cmdlets (and only Skype for Business Online cmdlets), you must first determine the name of the temporary Windows PowerShell module that contains all the Skype for Business Online cmdlets.</span></span> <span data-ttu-id="25e74-121">Pour cela, exécutez la commande suivante à partir de l’invite Windows PowerShell :</span><span class="sxs-lookup"><span data-stu-id="25e74-121">To do that, run this command from the Windows PowerShell prompt:</span></span>

    Get-Module

<span data-ttu-id="25e74-122">Des informations similaires à ce qui suit s’affichent à l’écran :</span><span class="sxs-lookup"><span data-stu-id="25e74-122">Information similar to the following will appear onscreen:</span></span>

    ModuleType Name                 ExportedCommands
    ---------- ----                 ----------------
    Manifest   Microsoft.PowerS...  {Add-Computer, Add-Content, A...}
    Script     tmp_5astd3uh.m5v     {Disable-CsMeetingRoom, Enabl...}

<span data-ttu-id="25e74-123">Le module avec le script ModuleType est le module qui contient les applets de connexion Skype entreprise online.</span><span class="sxs-lookup"><span data-stu-id="25e74-123">The module with the ModuleType Script is the module that contains the Skype for Business Online cmdlets.</span></span> <span data-ttu-id="25e74-124">Pour renvoyer la liste de ces applets de commande, exécutez l’applet de **commande Get-Command** en utilisant le nom du module de script comme nom de module :</span><span class="sxs-lookup"><span data-stu-id="25e74-124">To return a list of those cmdlets, run the **Get-Command** cmdlet, using the name of the Script module as the module name:</span></span>

    Get-Command -Module tmp_5astd3uh.m5v

<span data-ttu-id="25e74-125">Il est possible que vous puissiez avoir plusieurs modules avec un ModuleType égal à script.</span><span class="sxs-lookup"><span data-stu-id="25e74-125">It’s possible that you could have multiple modules with a ModuleType equal to Script.</span></span> <span data-ttu-id="25e74-126">Dans ce cas, vous pouvez exécuter la commande suivante pour déterminer le module qui inclut l’applet **de commande Get-CsTenant** :</span><span class="sxs-lookup"><span data-stu-id="25e74-126">In that case, you can run the following command to find out which module includes the **Get-CsTenant** cmdlet:</span></span>

    Get-Command Get-CsTenant

<span data-ttu-id="25e74-127">Le module renvoyé pour l’applet de connexion **Get-CsTenant** sera le module contenant toutes les applets de connexion Skype entreprise Online :</span><span class="sxs-lookup"><span data-stu-id="25e74-127">The module returned for the **Get-CsTenant** cmdlet will be the module containing all the Skype for Business Online cmdlets:</span></span>

    CommandType     Name                                               ModuleName
    -----------     ----                                               ----------
    Function        Get-CsTenant                                       tmp_5astd3uh.m5v

<div>

## <a name="see-also"></a><span data-ttu-id="25e74-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25e74-128">See Also</span></span>


<span data-ttu-id="25e74-129">[Présentation de Windows PowerShell et Skype Entreprise Online](https://technet.microsoft.com/library/Dn362785(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="25e74-129">[An introduction to Windows PowerShell and Skype for Business Online](https://technet.microsoft.com/library/Dn362785(v=OCS.15))</span></span>  
  

<span data-ttu-id="25e74-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="25e74-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

