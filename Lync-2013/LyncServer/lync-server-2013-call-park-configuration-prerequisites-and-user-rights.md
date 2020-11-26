---
title: 'Lync Server 2013 : Conditions prérequises pour la configuration du parcage d’appel et des droits utilisateur'
description: 'Lync Server 2013 : configuration du parc d’appel requis et droits d’utilisateur.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Call Park configuration prerequisites and user rights
ms:assetid: 25b8cfe0-e4e7-487c-9e78-8c040f629059
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425730(v=OCS.15)
ms:contentKeyID: 48183648
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b01187ad32fa7338765c0fa5b409b4e185e8ad35
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435711"
---
# <a name="call-park-configuration-prerequisites-and-user-rights-in-lync-server-2013"></a><span data-ttu-id="792ef-103">Conditions prérequises pour la configuration du parcage d’appel et des droits utilisateur dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="792ef-103">Call Park configuration prerequisites and user rights in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="792ef-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="792ef-104">

<span> </span></span></span>

<span data-ttu-id="792ef-105">_**Dernière modification de la rubrique :** 2012-09-10_</span><span class="sxs-lookup"><span data-stu-id="792ef-105">_**Topic Last Modified:** 2012-09-10_</span></span>

<span data-ttu-id="792ef-106">Le parc d’appels est une fonctionnalité de gestion des appels qui est installée par défaut lors du déploiement d’Enterprise Voice.</span><span class="sxs-lookup"><span data-stu-id="792ef-106">Call Park is a call management feature that is installed by default when you deploy Enterprise Voice.</span></span> <span data-ttu-id="792ef-107">Cette rubrique décrit ce que vous devez mettre en place avant de pouvoir configurer le parc d’appels et les droits d’utilisateur nécessaires à l’exécution des tâches de configuration.</span><span class="sxs-lookup"><span data-stu-id="792ef-107">This topic describes what you need to have in place before you can configure Call Park and the user rights that you need to perform configuration tasks.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="792ef-108">Les fichiers de conservation de musique personnalisés pour l’application de parc d’appels ne sont pas sauvegardés dans le cadre du processus de reprise après sinistre de Lync Server 2013 et les fichiers sont perdus si les fichiers téléchargés sur le pool sont endommagés, endommagés ou supprimés.</span><span class="sxs-lookup"><span data-stu-id="792ef-108">Customized music-on-hold files for the Call Park application are not backed up as part of the Lync Server 2013 disaster recovery process, and the files will be lost if the files uploaded to the pool are damaged, corrupted, or erased.</span></span> <span data-ttu-id="792ef-109">Veillez à toujours conserver une copie de sauvegarde distincte des fichiers de mise en attente musicale personnalisés que vous avez téléchargés pour le parcage d’appel.</span><span class="sxs-lookup"><span data-stu-id="792ef-109">Always keep a separate backup copy of the customized music-on-hold files that you have uploaded for Call Park.</span></span>



</div>

<span data-ttu-id="792ef-110">Cette section part du principe que vous avez lu la documentation de planification liée au parc d’appels (pour plus d’informations, reportez-vous à la [planification des fonctionnalités de gestion des appels dans Lync Server 2013](lync-server-2013-planning-for-call-management-features.md)).</span><span class="sxs-lookup"><span data-stu-id="792ef-110">This section assumes that you have read the planning documentation related to Call Park (see [Planning for call management features in Lync Server 2013](lync-server-2013-planning-for-call-management-features.md)).</span></span>

<div>

## <a name="call-park-configuration-prerequisites"></a><span data-ttu-id="792ef-111">Conditions préalables à la configuration du parc d’appels</span><span class="sxs-lookup"><span data-stu-id="792ef-111">Call Park Configuration Prerequisites</span></span>

<span data-ttu-id="792ef-112">Le parc d’appels nécessite les composants suivants :</span><span class="sxs-lookup"><span data-stu-id="792ef-112">Call Park requires the following components:</span></span>

  - <span data-ttu-id="792ef-113">service d’application</span><span class="sxs-lookup"><span data-stu-id="792ef-113">Application service</span></span>

  - <span data-ttu-id="792ef-114">application de parcage d’appel</span><span class="sxs-lookup"><span data-stu-id="792ef-114">Call Park application</span></span>

<span data-ttu-id="792ef-115">Ces composants sont installés automatiquement lorsque vous déployez Enterprise Voice.</span><span class="sxs-lookup"><span data-stu-id="792ef-115">These components are installed automatically when you deploy Enterprise Voice.</span></span>

<span data-ttu-id="792ef-116">Si vous voulez que les appelants entendent de la musique pendant le stationnement de l’appel, un fichier en attente de musique est également requis.</span><span class="sxs-lookup"><span data-stu-id="792ef-116">If you want callers to hear music while the call is parked, a music-on-hold file is also required.</span></span> <span data-ttu-id="792ef-117">Un fichier de Music-Holding par défaut est installé automatiquement lorsque vous déployez Enterprise Voice.</span><span class="sxs-lookup"><span data-stu-id="792ef-117">A default music-on-hold file is installed automatically when you deploy Enterprise Voice.</span></span> <span data-ttu-id="792ef-118">Vous pouvez remplacer le fichier par défaut par votre propre fichier audio.</span><span class="sxs-lookup"><span data-stu-id="792ef-118">You can substitute the default file with your own music-on-hold file.</span></span> <span data-ttu-id="792ef-119">Le parc d’appels utilise le magasin de fichiers pour contenir le fichier audio.</span><span class="sxs-lookup"><span data-stu-id="792ef-119">Call Park uses File Store to hold the audio file.</span></span>

</div>

<div>

## <a name="call-park-configuration-user-rights"></a><span data-ttu-id="792ef-120">Configuration du parc d’appels-droits d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="792ef-120">Call Park Configuration User Rights</span></span>

<span data-ttu-id="792ef-121">Pour configurer le parc d’appels, vous pouvez utiliser les outils d’administration suivants :</span><span class="sxs-lookup"><span data-stu-id="792ef-121">You can use the following administrative tools to configure Call Park:</span></span>

  - <span data-ttu-id="792ef-122">Panneau de configuration Lync Server</span><span class="sxs-lookup"><span data-stu-id="792ef-122">Lync Server Control Panel</span></span>

  - <span data-ttu-id="792ef-123">Lync Server Management Shell</span><span class="sxs-lookup"><span data-stu-id="792ef-123">Lync Server Management Shell</span></span>

<span data-ttu-id="792ef-124">Ces outils vous permettent de configurer la table de stationnement d’appel et de configurer d’autres paramètres utilisés par le parc d’appels.</span><span class="sxs-lookup"><span data-stu-id="792ef-124">You use these tools to set up the Call Park orbit table and to configure other settings used by Call Park.</span></span>

<span data-ttu-id="792ef-125">La configuration du parc d’appels nécessite l’un des rôles d’administration suivants, en fonction de la tâche :</span><span class="sxs-lookup"><span data-stu-id="792ef-125">Configuring Call Park requires any of the following administrative roles, depending on the task:</span></span>

  - <span data-ttu-id="792ef-126">**CsVoiceAdministrator :** Ce rôle d’administrateur peut créer, configurer et gérer l’ensemble des stratégies et paramètres relatifs à la voix.</span><span class="sxs-lookup"><span data-stu-id="792ef-126">**CsVoiceAdministrator:** This administrator role can create, configure, and manage all voice-related settings and policies.</span></span>

  - <span data-ttu-id="792ef-127">**CsUserAdministrator :** Ce rôle d’administrateur peut activer le parc d’appels dans la politique vocale.</span><span class="sxs-lookup"><span data-stu-id="792ef-127">**CsUserAdministrator:** This administrator role can enable Call Park in voice policy.</span></span> <span data-ttu-id="792ef-128">Ce rôle d’administrateur dispose également d’un accès en lecture seule à toutes les configurations vocales.</span><span class="sxs-lookup"><span data-stu-id="792ef-128">This administrator role also has read-only view access to all voice configurations.</span></span>

  - <span data-ttu-id="792ef-129">**CsServerAdministrator :** Ce rôle d’administrateur peut gérer, surveiller et résoudre les problèmes liés aux serveurs et services.</span><span class="sxs-lookup"><span data-stu-id="792ef-129">**CsServerAdministrator:** This administrator role can manage, monitor, and troubleshoot servers and services.</span></span>

  - <span data-ttu-id="792ef-130">**CsAdministrator :** Ce rôle d’administrateur peut effectuer toutes les tâches de CsVoiceAdministrator, CsServerAdministrator et CsUserAdministrator.</span><span class="sxs-lookup"><span data-stu-id="792ef-130">**CsAdministrator:** This administrator role can perform all of the tasks of CsVoiceAdministrator, CsServerAdministrator, and CsUserAdministrator.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="792ef-131">Pour plus d’informations sur les droits d’administration, voir <A href="lync-server-2013-planning-for-role-based-access-control.md">planification du contrôle d’accès basé sur les rôles dans Lync Server 2013</A> dans la documentation de planification.</span><span class="sxs-lookup"><span data-stu-id="792ef-131">For details about administrative rights, see <A href="lync-server-2013-planning-for-role-based-access-control.md">Planning for role-based access control in Lync Server 2013</A> in the Planning documentation.</span></span>



</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="792ef-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="792ef-132">See Also</span></span>


[<span data-ttu-id="792ef-133">Déploiement d’Enterprise Voice dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="792ef-133">Deploying Enterprise Voice in Lync Server 2013</span></span>](lync-server-2013-deploying-enterprise-voice.md)  


[<span data-ttu-id="792ef-134">Planifier les fonctionnalités de gestion des appels dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="792ef-134">Planning for call management features in Lync Server 2013</span></span>](lync-server-2013-planning-for-call-management-features.md)  
  

<span data-ttu-id="792ef-135"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="792ef-135"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

