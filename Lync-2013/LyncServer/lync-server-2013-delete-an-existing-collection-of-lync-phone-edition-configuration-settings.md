---
title: Supprimer une collection existante de paramètres de configuration de Lync Phone Edition
description: Supprimez une collection existante de paramètres de configuration de Lync Phone Edition.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete an existing collection of Lync Phone Edition configuration settings
ms:assetid: 1bfc427d-4dcd-4199-b25f-8d5cfec2164f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687984(v=OCS.15)
ms:contentKeyID: 49733574
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5137590a37b8bbb47f7445d20639157953597ca6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430554"
---
# <a name="delete-an-existing-collection-of-lync-phone-edition-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="d6a2b-103">Supprimer une collection existante de paramètres de configuration de Lync Phone Edition dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d6a2b-103">Delete an existing collection of Lync Phone Edition configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d6a2b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d6a2b-104">

<span> </span></span></span>

<span data-ttu-id="d6a2b-105">_**Dernière modification de la rubrique :** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="d6a2b-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="d6a2b-106">Si vous ne voulez plus utiliser un ensemble de paramètres pour les appareils exécutant Lync Phone Edition, supprimez-le.</span><span class="sxs-lookup"><span data-stu-id="d6a2b-106">If you no longer want to use a collection of settings for devices running Lync Phone Edition, delete it.</span></span> <span data-ttu-id="d6a2b-107">Si vous supprimez une collection pour un site, les paramètres globaux s’appliquent aux téléphones de ce site.</span><span class="sxs-lookup"><span data-stu-id="d6a2b-107">If you delete a collection for a site, the global settings will apply to the phones in that site.</span></span> <span data-ttu-id="d6a2b-108">Vous ne pouvez pas supprimer la collection globale.</span><span class="sxs-lookup"><span data-stu-id="d6a2b-108">You cannot delete the global collection.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="d6a2b-109">Au lieu de supprimer une collection, il est possible que vous vouliez simplement modifier certains paramètres.</span><span class="sxs-lookup"><span data-stu-id="d6a2b-109">Instead of deleting a collection, you might just want to change some of the settings.</span></span> <span data-ttu-id="d6a2b-110">Pour plus d’informations sur la façon de procéder, voir <A href="lync-server-2013-create-or-modify-a-collection-of-lync-phone-edition-configuration-settings.md">créer ou modifier un ensemble de paramètres de configuration de Lync Phone Edition dans Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="d6a2b-110">For details about how to do so, see <A href="lync-server-2013-create-or-modify-a-collection-of-lync-phone-edition-configuration-settings.md">Create or modify a collection of Lync Phone Edition configuration settings in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="to-delete-a-collection-of-lync-phone-edition-configuration-settings"></a><span data-ttu-id="d6a2b-111">Pour supprimer une collection de paramètres de configuration de Lync Phone Edition</span><span class="sxs-lookup"><span data-stu-id="d6a2b-111">To delete a collection of Lync Phone Edition configuration settings</span></span>

1.  <span data-ttu-id="d6a2b-112">À partir d’un compte d’utilisateur auquel est affecté le rôle CsUserAdministrator ou CsAdministrator, ouvrez une session sur un ordinateur de votre déploiement interne.</span><span class="sxs-lookup"><span data-stu-id="d6a2b-112">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="d6a2b-113">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="d6a2b-113">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="d6a2b-114">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="d6a2b-114">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="d6a2b-115">Dans la barre de navigation de gauche, cliquez sur **clients**, puis sur le bouton navigation de **configuration d’appareil** .</span><span class="sxs-lookup"><span data-stu-id="d6a2b-115">In the left navigation bar, click **Clients**, and then click the **Device Configuration** navigation button.</span></span>

4.  <span data-ttu-id="d6a2b-116">Dans la page Configuration de l' **appareil** , cliquez sur la collection que vous voulez supprimer, cliquez sur le menu **modifier** , puis cliquez sur **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="d6a2b-116">On the **Device Configuration** page, click the collection you want to delete, click the **Edit** menu, and then click **Delete**.</span></span>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="d6a2b-117">Si vous supprimez la collection globale, les paramètres sont restaurés par défaut.</span><span class="sxs-lookup"><span data-stu-id="d6a2b-117">If you delete the global collection, the settings just revert to the default settings.</span></span> <span data-ttu-id="d6a2b-118">La collection n’est pas déplacée.</span><span class="sxs-lookup"><span data-stu-id="d6a2b-118">The collection does not go away.</span></span>

    
    </div>

5.  <span data-ttu-id="d6a2b-119">Dans la boîte de confirmation, cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="d6a2b-119">In the confirmation box, click **OK**.</span></span>

</div>

<div>

## <a name="removing-lync-phone-edition-configuration-settings-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="d6a2b-120">Supprimer les paramètres de configuration de Lync Phone Edition en utilisant des applets de cmdlet Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="d6a2b-120">Removing Lync Phone Edition Configuration Settings by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="d6a2b-121">Vous pouvez supprimer des paramètres de configuration de Lync Phone Edition à l’aide de Windows PowerShell et de l’applet de passe **Remove-CsUCConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="d6a2b-121">You can delete Lync Phone Edition configuration settings by using Windows PowerShell and the **Remove-CsUCConfiguration** cmdlet.</span></span> <span data-ttu-id="d6a2b-122">Vous pouvez exécuter cette applet de commande sur Lync Server 2013 Management Shell ou à partir d’une session distante de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d6a2b-122">You can run this cmdlet either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="d6a2b-123">Pour plus d’informations sur l’utilisation de Windows PowerShell distant pour vous connecter à Lync Server, voir l’article de blog Lync Server Windows PowerShell « démarrage rapide : gestion de Microsoft Lync Server 2010 à l’aide de Remote PowerShell » [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="d6a2b-123">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-remove-a-specified-collection-of-lync-phone-edition-configuration-settings"></a><span data-ttu-id="d6a2b-124">Pour supprimer une collection de paramètres de configuration de Lync Phone Edition spécifiée</span><span class="sxs-lookup"><span data-stu-id="d6a2b-124">To remove a specified collection of Lync Phone Edition configuration settings</span></span>

  - <span data-ttu-id="d6a2b-125">Cette commande supprime les paramètres de configuration de téléphone UC appliqués au site de Redmond :</span><span class="sxs-lookup"><span data-stu-id="d6a2b-125">This command deletes the UC phone configuration settings applied to the Redmond site:</span></span>
    
        Remove-CsUCPhoneConfiguration -Identity "site:Redmond"

</div>

<div>

## <a name="to-remove-all-of-the-lync-phone-edition-configuration-settings-applied-to-the-site-scope"></a><span data-ttu-id="d6a2b-126">Pour supprimer tous les paramètres de configuration de Lync Phone Edition appliqués à l’étendue du site</span><span class="sxs-lookup"><span data-stu-id="d6a2b-126">To remove all of the Lync Phone Edition configuration settings applied to the site scope</span></span>

  - <span data-ttu-id="d6a2b-127">Cette commande supprime tous les paramètres de configuration de téléphone de UC appliqués à l’étendue du service :</span><span class="sxs-lookup"><span data-stu-id="d6a2b-127">This command removes all the UC phone configuration settings applied to the service scope:</span></span>
    
        Get-CsUCPhoneConfiguration -Filter "site:*" | Remove-CsUCPhoneConfiguration

</div>

<div>

## <a name="to-remove-all-of-the-lync-phone-edition-configuration-settings-where-phone-locking-is-disabled"></a><span data-ttu-id="d6a2b-128">Pour supprimer tous les paramètres de configuration de Lync Phone Edition dans lesquels le verrouillage de téléphone est désactivé</span><span class="sxs-lookup"><span data-stu-id="d6a2b-128">To remove all of the Lync Phone Edition configuration settings where phone locking is disabled</span></span>

  - <span data-ttu-id="d6a2b-129">Cette commande supprime tous les ensembles de paramètres de configuration du téléphone de type UC pour lesquels le verrouillage du téléphone a été désactivé :</span><span class="sxs-lookup"><span data-stu-id="d6a2b-129">This command deletes any collection of UC phone configuration settings where phone locking has been disabled:</span></span>
    
        Get-CsUCPhoneConfiguration | Where-Object {$_.EnforcePhoneLock -eq $False} | Remove-CsUCPhoneConfiguration

</div>

<span data-ttu-id="d6a2b-130">Pour plus d’informations, consultez la rubrique [Remove-CsUCPhoneConfiguration](https://technet.microsoft.com/library/Gg398249(v=OCS.15)).</span><span class="sxs-lookup"><span data-stu-id="d6a2b-130">For details, see [Remove-CsUCPhoneConfiguration](https://technet.microsoft.com/library/Gg398249(v=OCS.15)).</span></span>

<span data-ttu-id="d6a2b-131"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d6a2b-131"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

