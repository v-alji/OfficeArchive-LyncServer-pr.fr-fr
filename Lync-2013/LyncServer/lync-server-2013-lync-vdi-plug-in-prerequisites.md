---
title: 'Lync Server 2013 : Configuration requise pour le plug-in Lync VDI'
description: 'Configurations requises pour le plug-in Lync Server 2013 :'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Lync VDI plug-in prerequisites
ms:assetid: da25a976-7624-4dfc-b332-9c4db4ee78da
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205304(v=OCS.15)
ms:contentKeyID: 48185552
ms.date: 03/07/2017
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4389f776747426d07442e29418ab97e9609de7ee
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426241"
---
# <a name="lync-vdi-plug-in-prerequisites-in-lync-server-2013"></a><span data-ttu-id="5aaf3-103">Configuration requise pour le plug-in Lync VDI dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5aaf3-103">Lync VDI plug-in prerequisites in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5aaf3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5aaf3-104">

<span> </span></span></span>

<span data-ttu-id="5aaf3-105">_**Dernière modification de la rubrique :** 2017-03-07_</span><span class="sxs-lookup"><span data-stu-id="5aaf3-105">_**Topic Last Modified:** 2017-03-07_</span></span>

<span data-ttu-id="5aaf3-106">Dans un environnement VDI (Virtual Desktop Infrastructure), les machines virtuelles et l’ordinateur local de l’utilisateur doivent respecter les exigences indiquées dans cette section.</span><span class="sxs-lookup"><span data-stu-id="5aaf3-106">In a virtual desktop infrastructure (VDI) environment, the virtual machines and the user’s local computer must meet the requirements outlined in this section.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="5aaf3-107">Pour plus d’informations sur l’installation et le déploiement de l’environnement virtualisé, voir votre fournisseur de solution de virtualisation.</span><span class="sxs-lookup"><span data-stu-id="5aaf3-107">Refer to your virtualization solution provider for details about how to install and deploy the virtualized environment.</span></span> <span data-ttu-id="5aaf3-108">Pour plus d’informations sur le déploiement d’un environnement virtualisé basé sur Hyper-V et sur les services Bureau à distance, consultez les articles suivants dans la bibliothèque Microsoft TechNet :</span><span class="sxs-lookup"><span data-stu-id="5aaf3-108">For information about deploying a virtualized environment based on Hyper-V and Remote Desktop Services, see the following articles in the Microsoft TechNet Library:</span></span> 
> <UL>
> <LI>
> <P><span data-ttu-id="5aaf3-109">Hyper-V à <A class=uri href="https://go.microsoft.com/fwlink/p/?linkid=247514">https://go.microsoft.com/fwlink/p/?linkid=247514</A></span><span class="sxs-lookup"><span data-stu-id="5aaf3-109">Hyper-V at <A class=uri href="https://go.microsoft.com/fwlink/p/?linkid=247514">https://go.microsoft.com/fwlink/p/?linkid=247514</A></span></span></P>
> <LI>
> <P><span data-ttu-id="5aaf3-110">Services Bureau à distance dans Windows Server &nbsp; 2008 &nbsp; R2 sur <A class=uri href="https://go.microsoft.com/fwlink/p/?linkid=247513">https://go.microsoft.com/fwlink/p/?linkid=247513</A></span><span class="sxs-lookup"><span data-stu-id="5aaf3-110">Remote Desktop Services in Windows Server&nbsp;2008&nbsp;R2 at <A class=uri href="https://go.microsoft.com/fwlink/p/?linkid=247513">https://go.microsoft.com/fwlink/p/?linkid=247513</A></span></span></P></LI></UL>



</div>

<span data-ttu-id="5aaf3-111">Vous trouverez ci-dessous une configuration requise pour les machines virtuelles exécutées sur l’ordinateur du centre de données :</span><span class="sxs-lookup"><span data-stu-id="5aaf3-111">The following are requirements for the virtual machines running on the data center computer:</span></span>

  - <span data-ttu-id="5aaf3-112">Les machines virtuelles doivent être configurées avec Windows 10, Windows 8,1, Windows 8, Windows 7 ou Windows Server 2008 R2 avec les derniers Service Packs.</span><span class="sxs-lookup"><span data-stu-id="5aaf3-112">Virtual machines must be configured with Windows 10, Windows 8.1, Windows 8, Windows 7, or Windows Server 2008 R2 with the latest service packs.</span></span>

<span data-ttu-id="5aaf3-113">Pour l’utilisateur et l’ordinateur local de l’utilisateur, vous devez disposer des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="5aaf3-113">The following are requirements for the user and the user’s local computer:</span></span>

  - <span data-ttu-id="5aaf3-114">L’utilisateur doit être hébergé sur Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="5aaf3-114">The user must be homed on Lync Server 2013.</span></span>

  - <span data-ttu-id="5aaf3-115">L’ordinateur local doit exécuter Windows Embedded Standard 7 avec SP1, Windows 7 avec SP1, Windows 8, Windows 8,1 incorporé ou Windows 8,1 (non incorporé).</span><span class="sxs-lookup"><span data-stu-id="5aaf3-115">The local computer must be running Windows Embedded Standard 7 with SP1, Windows 7 with SP1, Windows 8, Windows 8.1 Embedded, or Windows 8.1 (not embedded).</span></span>

  - <span data-ttu-id="5aaf3-116">Si vous utilisez les services Bureau à distance, le nombre de bits du plug-in Lync VDI (c’est-à-dire, si l’application est 32 ou 64 bits) doit correspondre à la valeur de bits du système d’exploitation de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="5aaf3-116">If you are using Remote Desktop Services, the Lync VDI plug-in bitness (that is, whether the application is 32-bit or 64-bit) must match the local computer’s operating system bitness.</span></span> <span data-ttu-id="5aaf3-117">Il n’est pas nécessaire de faire correspondre le nombre binaire du système d’exploitation de l’ordinateur local et du système d’exploitation sur la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="5aaf3-117">The bitness of the operating system on the local computer and the operating system on the virtual machine do not need to match.</span></span> <span data-ttu-id="5aaf3-118">Si vous utilisez une autre solution ou plateforme de virtualisation, consultez la rubrique recommandations de la part de votre fournisseur de solutions de virtualisation concernant les exigences de nombre de bits.</span><span class="sxs-lookup"><span data-stu-id="5aaf3-118">If you are using another virtualization solution or platform, refer to guidance from your virtualization solution provider about bitness requirements.</span></span>

  - <span data-ttu-id="5aaf3-119">L’ordinateur local doit exécuter la version la plus récente du client de bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="5aaf3-119">The local computer must be running the latest version of the remote desktop client.</span></span> <span data-ttu-id="5aaf3-120">Installez les dernières mises à jour du client des services Bureau à distance de Microsoft ou le dernier logiciel du client Bureau à distance de votre fournisseur de solutions de virtualisation.</span><span class="sxs-lookup"><span data-stu-id="5aaf3-120">Install the latest updates of Remote Desktop Services client from Microsoft or the latest remote desktop client software from your virtualization solution provider.</span></span> <span data-ttu-id="5aaf3-121">Pour obtenir les dernières mises à jour de services Bureau à distance, voir [https://go.microsoft.com/fwlink/p/?LinkId=268032](https://go.microsoft.com/fwlink/p/?linkid=268032) .</span><span class="sxs-lookup"><span data-stu-id="5aaf3-121">For the latest Remote Desktop Services updates, see [https://go.microsoft.com/fwlink/p/?LinkId=268032](https://go.microsoft.com/fwlink/p/?linkid=268032).</span></span>

  - <span data-ttu-id="5aaf3-122">Sur l’ordinateur local, les paramètres du client Bureau à distance doivent être configurés afin que le son soit lu sur l’ordinateur local et que l’enregistrement à distance soit désactivé.</span><span class="sxs-lookup"><span data-stu-id="5aaf3-122">On the local computer, the remote desktop client settings must be configured so that audio plays on the local computer and remote recording is disabled.</span></span> <span data-ttu-id="5aaf3-123">Pour configurer ces paramètres pour la connexion Bureau à distance dans Windows, reportez-vous à la section « pour configurer les paramètres de connexion Bureau à distance ».</span><span class="sxs-lookup"><span data-stu-id="5aaf3-123">To configure these settings for Remote Desktop Connection in Windows, see the next section, "To configure Remote Desktop Connection settings."</span></span>

<div>

## <a name="to-configure-remote-desktop-connection-settings"></a><span data-ttu-id="5aaf3-124">Pour configurer les paramètres de connexion Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="5aaf3-124">To configure Remote Desktop Connection settings</span></span>

<span data-ttu-id="5aaf3-125">Pour préparer la connexion Bureau à distance dans Windows pour le plug-in Lync VDI, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="5aaf3-125">To prepare Remote Desktop Connection in Windows for the Lync VDI plug-in, follow these steps.</span></span>

1.  <span data-ttu-id="5aaf3-126">Si l’ordinateur local exécute Windows 8, ignorez cette étape.</span><span class="sxs-lookup"><span data-stu-id="5aaf3-126">If the local computer is running Windows 8, skip this step.</span></span> <span data-ttu-id="5aaf3-127">Si l’ordinateur local exécute Windows 7 avec SP1, installez la dernière version de Windows 8 du client de services Bureau à distance, disponible à l’adresse [https://go.microsoft.com/fwlink/p/?LinkId=268032](https://go.microsoft.com/fwlink/p/?linkid=268032) .</span><span class="sxs-lookup"><span data-stu-id="5aaf3-127">If the local computer is running Windows 7 with SP1, install the latest Windows 8 version of the Remote Desktop Services client, available at [https://go.microsoft.com/fwlink/p/?LinkId=268032](https://go.microsoft.com/fwlink/p/?linkid=268032).</span></span>

2.  <span data-ttu-id="5aaf3-128">Démarrez le client des services Bureau à distance en cliquant sur **Démarrer**, puis sur **Connexion Bureau à distance**.</span><span class="sxs-lookup"><span data-stu-id="5aaf3-128">Start the Remote Desktop Services client by clicking **Start**, and then clicking **Remote Desktop Connection**.</span></span>

3.  <span data-ttu-id="5aaf3-129">Cliquez sur **Options**.</span><span class="sxs-lookup"><span data-stu-id="5aaf3-129">Click **Options**.</span></span>

4.  <span data-ttu-id="5aaf3-130">Cliquez sur l’onglet **Ressources locales**. Sous **Sortie audio de l’ordinateur distant**, cliquez sur **Paramètres**, puis procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="5aaf3-130">Click the **Local Resources** tab. Under **Remote audio**, click **Settings**, and then do the following:</span></span>
    
      - <span data-ttu-id="5aaf3-131">Sous **Lecture audio à distance**, sélectionnez **Lire sur cet ordinateur**.</span><span class="sxs-lookup"><span data-stu-id="5aaf3-131">Under **Remote audio playback**, select **Play on this computer**.</span></span>
    
      - <span data-ttu-id="5aaf3-132">Sous **Enregistrement audio à distance**, sélectionnez **Ne pas enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="5aaf3-132">Under **Remote audio recording**, select **Do not record**.</span></span>
    
      - <span data-ttu-id="5aaf3-133">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="5aaf3-133">Click **OK**.</span></span>

5.  <span data-ttu-id="5aaf3-134">Cliquez sur l’onglet **Expérience**. Sous **Performance**, désactivez la case à cocher **Mise en cache permanente des bitmaps**.</span><span class="sxs-lookup"><span data-stu-id="5aaf3-134">Click the **Experience** tab. Under **Performance**, clear the **Persistent bitmap caching** check box.</span></span>

6.  <span data-ttu-id="5aaf3-135">Cliquez sur l’onglet **général** . Dans **ordinateur**, tapez le nom de l’ordinateur virtuel, puis cliquez sur **se connecter**.</span><span class="sxs-lookup"><span data-stu-id="5aaf3-135">Click the **General** tab. In **Computer**, type the name of the virtual machine, and then click **Connect**.</span></span>

<span data-ttu-id="5aaf3-136"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5aaf3-136"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

