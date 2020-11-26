---
title: 'Lync Server 2013 : configuration des stratégies de site pour l’archivage'
description: 'Lync Server 2013 : configuration des stratégies de site pour l’archivage.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up site policies for Archiving
ms:assetid: dc2ea206-8b9c-44dd-a479-efb217593c89
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205325(v=OCS.15)
ms:contentKeyID: 48185613
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 27e5b80b7f62ddc18d418415307457c7f2c4010d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441689"
---
# <a name="setting-up-site-policies-for-archiving-in-lync-server-2013"></a><span data-ttu-id="de015-103">Configuration de stratégies de site pour l’archivage dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="de015-103">Setting up site policies for Archiving in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="de015-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="de015-104">

<span> </span></span></span>

<span data-ttu-id="de015-105">_**Dernière modification de la rubrique :** 2012-10-09_</span><span class="sxs-lookup"><span data-stu-id="de015-105">_**Topic Last Modified:** 2012-10-09_</span></span>

<span data-ttu-id="de015-106">Vous pouvez activer ou désactiver l’archivage pour des sites spécifiques en créant et en configurant une stratégie d’archivage pour chacun de ces sites.</span><span class="sxs-lookup"><span data-stu-id="de015-106">You can enable or disable Archiving for specific sites by creating and configuring an Archiving policy for each of those sites.</span></span> <span data-ttu-id="de015-107">Une stratégie de site remplace la stratégie globale, mais les stratégies utilisateur remplacent les stratégies de site.</span><span class="sxs-lookup"><span data-stu-id="de015-107">A site policy overrides the global policy, but user policies override site policies.</span></span> <span data-ttu-id="de015-108">Les stratégies d’archivage ne s’appliquent que si vous n’utilisez pas l’intégration de Microsoft Exchange ou, si vous utilisez l’intégration de Microsoft Exchange, mais que certains utilisateurs ne sont pas hébergés sur Exchange 2013 et que leurs boîtes aux lettres sont placées dans In-Place attente.</span><span class="sxs-lookup"><span data-stu-id="de015-108">Archiving policies only apply if you do not use Microsoft Exchange integration or, if you do use Microsoft Exchange integration, but have some users who are not homed on Exchange 2013 and have their mailboxes put on In-Place Hold.</span></span>

<span data-ttu-id="de015-109">Pour plus d’informations sur le fonctionnement des stratégies d’archivage, y compris la hiérarchie pour les stratégies globales, de site et d’utilisateur, voir fonctionnement [de l’archivage dans Lync Server 2013](lync-server-2013-how-archiving-works.md) Planning documentation, documentation de déploiement, ou documentation sur les opérations.</span><span class="sxs-lookup"><span data-stu-id="de015-109">For details about how Archiving policies work, including the hierarchy for global, site, and user policies, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) Planning documentation, Deployment documentation, or Operations documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="de015-110">Si vous activez l’intégration de Microsoft Exchange pour votre déploiement, les stratégies de blocage d' In-Place Exchange contrôlent l’activation de l’archivage pour les utilisateurs hébergés sur Exchange 2013 et disposant de leurs boîtes aux lettres dans In-Place attente.</span><span class="sxs-lookup"><span data-stu-id="de015-110">If you enable Microsoft Exchange integration for your deployment, Exchange In-Place Hold policies control whether archiving is enabled for the users who are homed on Exchange 2013 and have their mailboxes put on In-Place Hold.</span></span> <span data-ttu-id="de015-111">Pour plus d’informations, reportez-vous à la rubrique <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">configuration de stratégies d’archivage dans Lync server 2013 lors de l’utilisation d’une intégration Exchange Server</A> dans la documentation de déploiement.</span><span class="sxs-lookup"><span data-stu-id="de015-111">For details, see <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Setting up policies for Archiving in Lync Server 2013 when using Exchange Server integration</A> in the Deployment documentation.</span></span><BR><span data-ttu-id="de015-112">Vous devez spécifier toutes les options appropriées dans les configurations de l’archivage avant d’activer l’archivage des communications internes ou externes dans les stratégies d’archivage.</span><span class="sxs-lookup"><span data-stu-id="de015-112">You should specify all appropriate options in the Archiving configurations before enabling Archiving of internal or external communications in the Archiving policies.</span></span> <span data-ttu-id="de015-113">Pour plus d’informations, reportez-vous à <A href="lync-server-2013-configuring-archiving-options.md">Configuration des options d’archivage dans Lync Server 2013</A> dans la documentation de déploiement.</span><span class="sxs-lookup"><span data-stu-id="de015-113">For details, see <A href="lync-server-2013-configuring-archiving-options.md">Configuring Archiving options in Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<div>

## <a name="to-create-an-archiving-policy-for-a-site"></a><span data-ttu-id="de015-114">Pour créer une stratégie d’archivage pour un site</span><span class="sxs-lookup"><span data-stu-id="de015-114">To create an archiving policy for a site</span></span>

1.  <span data-ttu-id="de015-115">À partir d’un compte d’utilisateur auquel est affecté un des rôles CsArchivingAdministrator ou CsAdministrator, ouvrez une session sur un ordinateur de votre déploiement interne.</span><span class="sxs-lookup"><span data-stu-id="de015-115">From a user account that is assigned to the CsArchivingAdministrator or CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="de015-116">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="de015-116">Open a browser window, and then enter the Admin URL to open the Lync Server 2013 Control Panel.</span></span>

3.  <span data-ttu-id="de015-117">Dans la barre de navigation gauche, cliquez sur **surveillance et archivage**, puis cliquez sur **stratégie d’archivage**.</span><span class="sxs-lookup"><span data-stu-id="de015-117">In the left navigation bar, click **Monitoring and Archiving**, and then click **Archiving Policy**.</span></span>
    
    <span data-ttu-id="de015-118">Pour plus d’informations sur le fonctionnement des stratégies d’archivage, y compris la hiérarchie pour les stratégies globales, de site et d’utilisateur, voir fonctionnement [de l’archivage dans Lync Server 2013](lync-server-2013-how-archiving-works.md) Planning documentation, documentation de déploiement, ou documentation sur les opérations.</span><span class="sxs-lookup"><span data-stu-id="de015-118">For details about how Archiving policies work, including the hierarchy for global, site, and user policies, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) Planning documentation, Deployment documentation, or Operations documentation.</span></span>

4.  <span data-ttu-id="de015-119">Cliquez sur **Créer**, puis sur **Stratégie de site**.</span><span class="sxs-lookup"><span data-stu-id="de015-119">Click **New**, and then click **Site policy**.</span></span>

5.  <span data-ttu-id="de015-120">Dans **Sélectionner un site**, cliquez sur le site auquel la stratégie doit s’appliquer.</span><span class="sxs-lookup"><span data-stu-id="de015-120">In **Select a site**, click the site to which the policy is to be applied.</span></span>

6.  <span data-ttu-id="de015-121">Dans **Nouvelle stratégie d’archivage**, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="de015-121">In **New Archiving Policy**, do the following:</span></span>
    
      - <span data-ttu-id="de015-122">Dans **Nom**, spécifiez le nom pour la stratégie de site.</span><span class="sxs-lookup"><span data-stu-id="de015-122">In **Name**, specify the name for the site policy.</span></span>
    
      - <span data-ttu-id="de015-123">Dans **Description**, entrez des informations décrivant la stratégie de site (par exemple, stratégie de site pour Redmond).</span><span class="sxs-lookup"><span data-stu-id="de015-123">In **Description**, provide information about what the site policy is (for example, site policy for Redmond).</span></span>
    
      - <span data-ttu-id="de015-124">Pour contrôler l’archivage des communications internes pour le site spécifié, activez ou désactivez la case à cocher **Archiver les communications internes**.</span><span class="sxs-lookup"><span data-stu-id="de015-124">To control archiving of internal communications for the specified site, select or clear the **Archive internal communications** check box.</span></span>
    
      - <span data-ttu-id="de015-125">Pour contrôler l’archivage des communications externes pour le site spécifié, activez ou désactivez la case à cocher **Archiver les communications externes**.</span><span class="sxs-lookup"><span data-stu-id="de015-125">To control archiving of external communications for the specified site, select or clear the **Archive external communications** check box.</span></span>

7.  <span data-ttu-id="de015-126">Cliquez sur **Valider**.</span><span class="sxs-lookup"><span data-stu-id="de015-126">Click **Commit**.</span></span>

<span data-ttu-id="de015-127"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="de015-127"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

