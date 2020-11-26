---
title: 'Lync Server 2013 : Gestion des annonces lors de la récupération d’urgence'
description: 'Lync Server 2013 : gérer les annonces lors de la récupération d’urgence.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Manage announcements during disaster recovery
ms:assetid: c33e51ea-421f-42d2-826b-b73968f6bd5b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721874(v=OCS.15)
ms:contentKeyID: 49733807
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d85dfcd15c9c3650bafafa6fa7702e19ac9c4f7d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426122"
---
# <a name="manage-announcements-during-disaster-recovery-in-lync-server-2013"></a><span data-ttu-id="91f7c-103">Gestion des annonces lors de la récupération d’urgence dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="91f7c-103">Manage announcements during disaster recovery in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="91f7c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="91f7c-104">

<span> </span></span></span>

<span data-ttu-id="91f7c-105">_**Dernière modification de la rubrique :** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="91f7c-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="91f7c-106">Lync Server 2013 prend en charge les annonces pour les appels vers des numéros non attribués lors des pannes.</span><span class="sxs-lookup"><span data-stu-id="91f7c-106">Lync Server 2013 supports announcements for calls to unassigned numbers during outages.</span></span> <span data-ttu-id="91f7c-107">La restauration de la fonctionnalité d’annonce pendant une interruption est facultative.</span><span class="sxs-lookup"><span data-stu-id="91f7c-107">Restoring announcement functionality during an outage is optional.</span></span> <span data-ttu-id="91f7c-108">Si vous choisissez de restaurer les annonces lors d’une panne, vous devez recréer votre configuration d’annonce dans le pool de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="91f7c-108">If you choose to restore announcements during an outage, you need recreate your announcement configuration in the backup pool.</span></span> <span data-ttu-id="91f7c-109">Cette section décrit ce que vous devez faire si vous choisissez de restaurer les annonces lors de la récupération d’urgence.</span><span class="sxs-lookup"><span data-stu-id="91f7c-109">This section describes what you need to do if you choose to restore announcements during disaster recovery.</span></span>

<span data-ttu-id="91f7c-110">Cette section s’applique aux plages de nombres non affectées qui utilisent l’application annonce.</span><span class="sxs-lookup"><span data-stu-id="91f7c-110">This section applies to unassigned number ranges that use the Announcement application.</span></span> <span data-ttu-id="91f7c-111">Cette section ne s’applique pas aux plages de nombres non affectées qui utilisent le standard automatique de messagerie unifiée (MU) Exchange.</span><span class="sxs-lookup"><span data-stu-id="91f7c-111">This section does not apply to unassigned number ranges that use Exchange Unified Messaging (UM) Auto Attendant.</span></span>

<div>

## <a name="before-an-outage"></a><span data-ttu-id="91f7c-112">Avant une panne</span><span class="sxs-lookup"><span data-stu-id="91f7c-112">Before an Outage</span></span>

<span data-ttu-id="91f7c-113">Que vous choisissiez d’utiliser les annonces au cours d’une période d’indisponibilité, vous devez effectuer des copies de sauvegarde distinctes de tous les fichiers audio personnalisés que vous avez configurés pour l’application d’annonce.</span><span class="sxs-lookup"><span data-stu-id="91f7c-113">Regardless of whether you choose to use announcements during outages, you should take separate backups of any customized audio files that you configured for the Announcement application.</span></span> <span data-ttu-id="91f7c-114">Les annonces personnalisées ne sont pas sauvegardées dans le cadre du processus de reprise après sinistre de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="91f7c-114">Customized announcements are not backed up as part of the Lync Server disaster recovery process.</span></span> <span data-ttu-id="91f7c-115">Si vous n’effectuez pas de sauvegardes distinctes des fichiers et que les fichiers que vous avez téléchargés sur le serveur ou le pool sont endommagés, endommagés ou effacés, ils sont perdus.</span><span class="sxs-lookup"><span data-stu-id="91f7c-115">If you do not take separate backups of the files and the files that you uploaded to the server or pool are damaged, corrupted, or erased, the files will be lost.</span></span>

<span data-ttu-id="91f7c-116">Si vous n’avez pas de copies de sauvegarde des fichiers audio personnalisés et que les fichiers audio d’origine ne sont plus disponibles, vous pouvez rechercher les fichiers audio que vous avez configurés pour une application d’annonce en consultant le magasin de fichiers du serveur ou du pool dans lequel vous avez importé les fichiers.</span><span class="sxs-lookup"><span data-stu-id="91f7c-116">If you do not have backup copies of customized audio files, and the original audio files are no longer available, you can find the audio files that you configured for an Announcement application by looking in the File Store for the server or pool where you originally imported the files.</span></span> <span data-ttu-id="91f7c-117">Vous pouvez copier tous les fichiers audio que vous avez configurés pour l’application annonce à partir du magasin de fichiers.</span><span class="sxs-lookup"><span data-stu-id="91f7c-117">You can copy all the audio files that you configured for the Announcement application from the File Store.</span></span>

<span data-ttu-id="91f7c-118">**Pour copier des fichiers audio à partir du magasin de fichiers**</span><span class="sxs-lookup"><span data-stu-id="91f7c-118">**To copy audio files from the file store**</span></span>

1.  <span data-ttu-id="91f7c-119">Dans la ligne de commande, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="91f7c-119">At the command line, run:</span></span>
    
        Xcopy <Source: Pool Announcement Service File Store path> <Destination>
    
    <span data-ttu-id="91f7c-120">Exemple :</span><span class="sxs-lookup"><span data-stu-id="91f7c-120">For example:</span></span>
    
        Xcopy "<Pool File Store Path>\X-ApplicationServer-X\AppServerFiles\RGS\AS" "<Destination: Backup location>"
    
    <span data-ttu-id="91f7c-121">Où X-ApplicationServer-X fait référence à l’ID de service du serveur d’applications du pool (par exemple, 1-ApplicationServer-1 ")</span><span class="sxs-lookup"><span data-stu-id="91f7c-121">Where X-ApplicationServer-X refers to the service ID of the Application Server of the pool (for example, 1-ApplicationServer-1")</span></span>


</div>

<div>

## <a name="during-an-outage"></a><span data-ttu-id="91f7c-122">Pendant une période d’interruption</span><span class="sxs-lookup"><span data-stu-id="91f7c-122">During an Outage</span></span>

<span data-ttu-id="91f7c-123">Pour utiliser l’application d’annonce au cours d’une période d’inactivité, vous devez recréer la configuration de l’annonce dans le pool de sauvegarde en effectuant les étapes décrites dans cette section.</span><span class="sxs-lookup"><span data-stu-id="91f7c-123">To use the Announcement application during an outage, you need to recreate the announcement configuration in the backup pool by performing the tasks described in this section.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="91f7c-124">Nous vous recommandons d’effectuer ces tâches après le basculement vers le pool de sauvegarde, car dès que vous effectuez l’étape 2, le pool de sauvegarde prend la propriété des plages de numéros non attribués.</span><span class="sxs-lookup"><span data-stu-id="91f7c-124">We recommend that you perform these tasks after you fail over to the backup pool, because as soon as you perform step 2, the backup pool takes ownership of the unassigned number ranges.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="91f7c-125">Ces étapes ne sont pas requises pour les plages de nombres qui utilisent un numéro de téléphone de standard automatique de messagerie unifiée Exchange.</span><span class="sxs-lookup"><span data-stu-id="91f7c-125">These steps are not required for number ranges that use an Exchange UM Auto Attendant phone number.</span></span>



</div>

<span data-ttu-id="91f7c-126">**Pour recréer la configuration d’annonce dans le pool de sauvegarde**</span><span class="sxs-lookup"><span data-stu-id="91f7c-126">**To recreate the announcement configuration in the backup pool**</span></span>

1.  <span data-ttu-id="91f7c-127">Recréez les annonces que vous avez déployées dans le pool principal du pool de sauvegarde en procédant comme suit :</span><span class="sxs-lookup"><span data-stu-id="91f7c-127">Recreate the announcements that you deployed in the primary pool in the backup pool by doing the following:</span></span>
    
    1.  <span data-ttu-id="91f7c-128">Importez les fichiers audio utilisés dans le pool principal vers le pool de sauvegarde en utilisant l’applet de passe **Import-CsAnnouncementFile** et en spécifiant le pool de sauvegarde du paramètre parent.</span><span class="sxs-lookup"><span data-stu-id="91f7c-128">Import any audio files used in the primary pool to the backup pool by using the **Import-CsAnnouncementFile** cmdlet and specifying the backup pool for the Parent parameter.</span></span>
    
    2.  <span data-ttu-id="91f7c-129">Recréez toutes les annonces à l’aide de l’applet **de nouvelle-CsAnnouncement** et en spécifiant le pool de sauvegarde pour le paramètre parent.</span><span class="sxs-lookup"><span data-stu-id="91f7c-129">Recreate each announcement by using the **New-CsAnnouncement** cmdlet and specifying the backup pool for the Parent parameter.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="91f7c-130">Pour plus d’informations sur l’utilisation de ces paramètres pour créer des annonces dans le pool de sauvegardes, voir <A href="lync-server-2013-create-an-announcement.md">créer une annonce dans Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="91f7c-130">For details about using these parameters to create announcements in the backup pool, see <A href="lync-server-2013-create-an-announcement.md">Create an announcement in Lync Server 2013</A>.</span></span>

    
    </div>

2.  <span data-ttu-id="91f7c-131">Une fois toutes les annonces recréées dans le pool de sauvegardes, redirigez toutes les plages de nombres non affectées qui utilisent les annonces du pool principal vers les annonces recréées dans le pool de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="91f7c-131">After all announcements are recreated in the backup pool, redirect all the unassigned number ranges that use announcements in the primary pool to the recreated announcements in the backup pool.</span></span>
    
    <span data-ttu-id="91f7c-132">Pour chaque plage de numéros non affecté qui utilise une annonce de la liste principale, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="91f7c-132">For each unassigned number range that uses an announcement in the primary pool, run the following:</span></span>
    
        Set-CsUnassignedNumber -Identity "<name of number range>" -AnnouncementService "<FQDN of backup pool>" -AnnouncementName "<announcement name in backup pool>"

</div>

<div>

## <a name="after-the-outage"></a><span data-ttu-id="91f7c-133">Après la panne</span><span class="sxs-lookup"><span data-stu-id="91f7c-133">After the Outage</span></span>

<span data-ttu-id="91f7c-134">Lorsque le pool principal devient disponible, vous devez rediriger les plages de numéros non affectées qui ont été modifiées pour revenir au pool principal.</span><span class="sxs-lookup"><span data-stu-id="91f7c-134">When the primary pool becomes available, you need to redirect the unassigned number ranges that you changed for the outage back to the primary pool.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="91f7c-135">Ces étapes ne sont pas requises pour les plages de nombres qui utilisent un numéro de téléphone de standard automatique de messagerie unifiée Exchange.</span><span class="sxs-lookup"><span data-stu-id="91f7c-135">These steps are not required for number ranges that use an Exchange UM Auto Attendant phone number.</span></span>



</div>

<span data-ttu-id="91f7c-136">**Pour restaurer les annonces dans le pool principal**</span><span class="sxs-lookup"><span data-stu-id="91f7c-136">**To restore announcements in the primary pool**</span></span>

1.  <span data-ttu-id="91f7c-137">Si vous deviez reconstruire le pool principal lors de la récupération, vous devez recréer les annonces dans le pool principal en important les fichiers audio et en créant des annonces, comme vous le feriez dans le pool de sauvegarde, à l’exception de la liste principale du paramètre parent.</span><span class="sxs-lookup"><span data-stu-id="91f7c-137">If you had to rebuild the primary pool during the recovery, you need to recreate the announcements in the primary pool by importing the audio files and creating announcements, just as you did in the backup pool, except that you specify the primary pool for the Parent parameter.</span></span> <span data-ttu-id="91f7c-138">Pour plus d’informations, consultez la section « au cours d’une interruption » plus haut dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="91f7c-138">For details, see "During an Outage" earlier in this topic.</span></span>

2.  <span data-ttu-id="91f7c-139">Pour chaque plage de nombres non affectée que vous avez modifiée pour l’interruption, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="91f7c-139">For each unassigned number range that you changed for the outage, run the following:</span></span>
    
        Set-CsUnassignedNumber [-Identity "<name of number range>"] -AnnouncementService "<FQDN of primary pool>" -AnnouncementName "<announcement name in primary pool>"

3.  <span data-ttu-id="91f7c-140">Vous pouvez également supprimer les annonces que vous avez recréées dans le pool de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="91f7c-140">Optionally, remove the announcements that you recreated in the backup pool.</span></span> <span data-ttu-id="91f7c-141">Obtenez la liste des annonces de l’application d’annonce de pool de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="91f7c-141">Get a list of announcements for the backup pool Announcement application.</span></span> <span data-ttu-id="91f7c-142">Dans la ligne de commande, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="91f7c-142">At the command line, run:</span></span>
    
        Get-CsAnnouncement -Identity "<Service:service ID>"
    
    <span data-ttu-id="91f7c-143">Exemple :</span><span class="sxs-lookup"><span data-stu-id="91f7c-143">For example:</span></span>
    
        Get-CsAnnouncement -Identity "ApplicationServer:redmond.contoso.com
    
    <span data-ttu-id="91f7c-144">Dans la liste résultante, recherchez les annonces que vous voulez supprimer et copiez les GUID.</span><span class="sxs-lookup"><span data-stu-id="91f7c-144">In the resulting list, locate the announcements you want to remove and copy the GUIDs.</span></span> <span data-ttu-id="91f7c-145">Pour chaque annonce que vous voulez supprimer, exécutez :</span><span class="sxs-lookup"><span data-stu-id="91f7c-145">For each announcement you want to remove, run:</span></span>
    
        Remove-CsAnnouncement -Identity "<Service:service ID/guid>"
    
    <span data-ttu-id="91f7c-146">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="91f7c-146">For example:</span></span>
    
        Remove-CsAnnouncement -Identity "ApplicationServer:redmond.contoso.com/1951f734-c80f-4fb2-965d-51807c792b90"


<span data-ttu-id="91f7c-147"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="91f7c-147"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

