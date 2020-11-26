---
title: 'Lync Server 2013 : cmdlets Lync Server par catégorie'
description: 'Lync Server 2013 : cmdlets Lync Server par catégories.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Lync Server 2013 cmdlets by category
ms:assetid: 4ce274d7-b0ec-40b8-b85e-9a0613916ffb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398306(v=OCS.15)
ms:contentKeyID: 48184106
ms.date: 09/20/2017
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: df562bd11d54c9ecda4fe3d6172ed1d8bd2627d6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426276"
---
# <a name="lync-server-2013-cmdlets-by-category"></a><span data-ttu-id="948dc-103">Applets de cmdlet Lync Server 2013 par catégorie</span><span class="sxs-lookup"><span data-stu-id="948dc-103">Lync Server 2013 cmdlets by category</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="948dc-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="948dc-104">

<span> </span></span></span>

<span data-ttu-id="948dc-105">_**Dernière modification de la rubrique :** 2017-09-20_</span><span class="sxs-lookup"><span data-stu-id="948dc-105">_**Topic Last Modified:** 2017-09-20_</span></span>

<span data-ttu-id="948dc-106">Microsoft Lync Server 2013 est fourni avec une cmdlet presque 550 conçue spécifiquement pour permettre aux administrateurs de gérer Lync Server à partir de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="948dc-106">Microsoft Lync Server 2013 ships with almost 550 cmdlets specifically designed to allow administrators to manage Lync Server from the command line.</span></span> <span data-ttu-id="948dc-107">Vous accédez aux cmdlets à partir de Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="948dc-107">You access the cmdlets from the Lync Server Management Shell.</span></span> <span data-ttu-id="948dc-108">Vous pouvez obtenir de l’aide sur une cmdlet directement à partir de la ligne de commande en tapant une commande semblable à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="948dc-108">You can retrieve help on a cmdlet directly from the command line by typing a command similar to the following:</span></span>

    Get-Help New-CsVoicePolicy -Full

<span data-ttu-id="948dc-109">La commande précédente récupère toutes les rubriques d’aide disponibles pour l’applet de commande **New-CsVoicePolicy** .</span><span class="sxs-lookup"><span data-stu-id="948dc-109">The preceding command will retrieve all the help available for the **New-CsVoicePolicy** cmdlet.</span></span> <span data-ttu-id="948dc-110">Remplacez **New-CsVoicePolicy** par le nom de l’applet de recherche pour laquelle vous souhaitez obtenir de l’aide.</span><span class="sxs-lookup"><span data-stu-id="948dc-110">Substitute the reference to **New-CsVoicePolicy** with the name of the cmdlet for which you want to retrieve help.</span></span>

<span data-ttu-id="948dc-111">Pour obtenir la liste complète des applets de commande disponibles pour gérer Microsoft Lync Server 2013, à l’invite de commandes de Lync Server Management Shell, tapez ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="948dc-111">To retrieve a full list of cmdlets available for managing Microsoft Lync Server 2013, type the following at the Lync Server Management Shell command prompt:</span></span>

    Get-Command * -Module Lync -CommandType cmdlet

<span data-ttu-id="948dc-112">Si vous n’êtes pas sûr des cmdlets dont vous avez besoin, nous avons également fourni une liste classés des cmdlets et leurs rubriques d’aide.</span><span class="sxs-lookup"><span data-stu-id="948dc-112">If you are unsure which cmdlets you need, we have also provided a categorized list of cmdlets and their help topics.</span></span> <span data-ttu-id="948dc-113">Vous constaterez que certaines de ces applets de technologie apparaissent dans plusieurs catégories, ce qui était intentionnel lors de leur application à plusieurs zones du produit.</span><span class="sxs-lookup"><span data-stu-id="948dc-113">You will find that some of the cmdlets show up in more than one category, which was intentional as they apply to multiple areas of the product.</span></span> <span data-ttu-id="948dc-114">La liste suivante répertorie les catégories :</span><span class="sxs-lookup"><span data-stu-id="948dc-114">The following is a list of categories:</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="948dc-115">Référence sur les applets de la cmdlet Skype entreprise a été déplacée vers docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="948dc-115">Skype for Business cmdlet reference has moved to docs.microsoft.com.</span></span> <span data-ttu-id="948dc-116">Cliquer sur les liens ci-dessous vous permet d’atteindre la nouvelle page docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="948dc-116">Clicking on the links below will take you to the new docs.microsoft.com page.</span></span> <span data-ttu-id="948dc-117">Le contenu est désormais ouvert et est disponible pour les contributions de la Communauté par le biais de GitHub.</span><span class="sxs-lookup"><span data-stu-id="948dc-117">The content is now open sourced and available for community contributions through GitHub.</span></span> <span data-ttu-id="948dc-118">Vous voulez participer ?</span><span class="sxs-lookup"><span data-stu-id="948dc-118">Interested in contributing?</span></span> <span data-ttu-id="948dc-119">Consultez le fichier README dans le référentiel Samples : <A href="https://github.com/microsoftdocs/office-docs-powershell">https://github.com/MicrosoftDocs/office-docs-powershell</A></span><span class="sxs-lookup"><span data-stu-id="948dc-119">Check out the README in the repo here: <A href="https://github.com/microsoftdocs/office-docs-powershell">https://github.com/MicrosoftDocs/office-docs-powershell</A></span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="948dc-120">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="948dc-120">In This Section</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="948dc-121"><a href="lync-server-2013-user-management-cmdlets.md">Cmdlets de gestion des utilisateurs dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="948dc-121"><a href="lync-server-2013-user-management-cmdlets.md">User management cmdlets in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="948dc-122"><a href="lync-server-2013-voice-application-cmdlets.md">Cmdlets de l’application vocale dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="948dc-122"><a href="lync-server-2013-voice-application-cmdlets.md">Voice application cmdlets in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="948dc-123"><a href="lync-server-2013-client-management-cmdlets.md">Cmdlets de gestion des clients dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="948dc-123"><a href="lync-server-2013-client-management-cmdlets.md">Client management cmdlets in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="948dc-124"><a href="lync-server-2013-advanced-enterprise-voice-cmdlets.md">Applets de applet voix entreprise avancées dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="948dc-124"><a href="lync-server-2013-advanced-enterprise-voice-cmdlets.md">Advanced Enterprise Voice cmdlets in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="948dc-125"><a href="lync-server-2013-im-and-presence-cmdlets.md">Cmdlets de la messagerie instantanée et de la présence dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="948dc-125"><a href="lync-server-2013-im-and-presence-cmdlets.md">IM and presence cmdlets in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="948dc-126"><a href="lync-server-2013-pstn-connectivity-cmdlets.md">Applets de connexion RTC dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="948dc-126"><a href="lync-server-2013-pstn-connectivity-cmdlets.md">PSTN connectivity cmdlets in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="948dc-127"><a href="lync-server-2013-conferencing-cmdlets.md">Cmdlets de conférence dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="948dc-127"><a href="lync-server-2013-conferencing-cmdlets.md">Conferencing cmdlets in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="948dc-128"><a href="lync-server-2013-phones-and-devices-cmdlets.md">Cmdlets et périphériques de téléphone dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="948dc-128"><a href="lync-server-2013-phones-and-devices-cmdlets.md">Phones and devices cmdlets in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="948dc-129"><a href="lync-server-2013-infrastructure-and-deployment-cmdlets.md">Cmdlets Infrastructure and Deployment dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="948dc-129"><a href="lync-server-2013-infrastructure-and-deployment-cmdlets.md">Infrastructure and deployment cmdlets in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="948dc-130"><a href="lync-server-2013-migration-and-coexistence-cmdlets.md">Cmdlets de migration et de coexistence dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="948dc-130"><a href="lync-server-2013-migration-and-coexistence-cmdlets.md">Migration and coexistence cmdlets in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="948dc-131"><a href="lync-server-2013-security-cmdlets.md">Cmdlets de sécurité dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="948dc-131"><a href="lync-server-2013-security-cmdlets.md">Security cmdlets in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="948dc-132"><a href="lync-server-2013-lync-server-management-shell-configuration-cmdlets.md">Cmdlets de configuration de Lync Server Management Shell dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="948dc-132"><a href="lync-server-2013-lync-server-management-shell-configuration-cmdlets.md">Lync Server Management Shell configuration cmdlets in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="948dc-133"><a href="lync-server-2013-server-roles-and-services-cmdlets.md">Applets de service et rôles de serveur dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="948dc-133"><a href="lync-server-2013-server-roles-and-services-cmdlets.md">Server roles and services cmdlets in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="948dc-134"><a href="lync-server-2013-mobility-cmdlets.md">Cmdlets de mobilité dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="948dc-134"><a href="lync-server-2013-mobility-cmdlets.md">Mobility cmdlets in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="948dc-135"><a href="lync-server-2013-application-management-cmdlets.md">Cmdlets de gestion des applications dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="948dc-135"><a href="lync-server-2013-application-management-cmdlets.md">Application management cmdlets in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="948dc-136"><a href="lync-server-2013-persistent-chat-server-cmdlets.md">Cmdlets Server chat permanent dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="948dc-136"><a href="lync-server-2013-persistent-chat-server-cmdlets.md">Persistent Chat Server cmdlets in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="948dc-137"><a href="lync-server-2013-federation-and-external-access-cmdlets.md">Applets de la Fédération et accès externe dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="948dc-137"><a href="lync-server-2013-federation-and-external-access-cmdlets.md">Federation and external access cmdlets in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="948dc-138"><a href="lync-server-2013-centralized-logging-cmdlets.md">Cmdlets d’enregistrement centralisé dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="948dc-138"><a href="lync-server-2013-centralized-logging-cmdlets.md">Centralized Logging cmdlets in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="948dc-139"><a href="lync-server-2013-enterprise-voice-cmdlets.md">Cmdlets voix entreprise dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="948dc-139"><a href="lync-server-2013-enterprise-voice-cmdlets.md">Enterprise Voice cmdlets in Lync Server 2013</a></span></span></p></td>
<td></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="see-also"></a><span data-ttu-id="948dc-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="948dc-140">See Also</span></span>


[<span data-ttu-id="948dc-141">Blog Lync Server PowerShell</span><span class="sxs-lookup"><span data-stu-id="948dc-141">Lync Server PowerShell Blog</span></span>](https://go.microsoft.com/fwlink/p/?linkid=203150)  
  

<span data-ttu-id="948dc-142"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="948dc-142"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

