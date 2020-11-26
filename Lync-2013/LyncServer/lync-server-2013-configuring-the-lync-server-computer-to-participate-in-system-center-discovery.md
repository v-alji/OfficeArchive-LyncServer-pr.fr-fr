---
title: Configuration de l’ordinateur serveur Lync pour participer à la découverte de System Center
description: Configurer l’ordinateur Lync Server pour qu’il participe à la découverte de System Center.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring the Lync Server computer to participate in System Center discovery
ms:assetid: 2f9c9cb0-3120-4571-9cd2-657c2123fe21
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204776(v=OCS.15)
ms:contentKeyID: 48183731
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 44d25ba3de673084b2e64e17790a2776cbe57f07
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432561"
---
# <a name="configuring-the-lync-server-2013-computer-to-participate-in-system-center-discovery"></a><span data-ttu-id="00f59-103">Configuration de l’ordinateur Lync Server 2013 pour participer à la découverte de System Center</span><span class="sxs-lookup"><span data-stu-id="00f59-103">Configuring the Lync Server 2013 computer to participate in System Center discovery</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="00f59-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="00f59-104">

<span> </span></span></span>

<span data-ttu-id="00f59-105">_**Dernière modification de la rubrique :** 2012-10-20_</span><span class="sxs-lookup"><span data-stu-id="00f59-105">_**Topic Last Modified:** 2012-10-20_</span></span>

<span data-ttu-id="00f59-106">Pour vous assurer que votre nouvel agent Lync Server est impliqué dans le processus de découverte pour System Center Operations Manager, vous devez effectuer la procédure suivante sur chaque ordinateur sur lequel la console System Center Operations Manager a été installée :</span><span class="sxs-lookup"><span data-stu-id="00f59-106">To make sure that your new Lync Server agent participates in discovery process for System Center Operations Manager, you must complete the following procedure on each computer where the System Center Operations Manager console has been installed:</span></span>

1.  <span data-ttu-id="00f59-107">Dans l’onglet **administration** , cliquez sur **géré par l’agent**.</span><span class="sxs-lookup"><span data-stu-id="00f59-107">On the **Administration** tab, click **Agent Managed**.</span></span>

2.  <span data-ttu-id="00f59-108">Cliquez avec le bouton droit sur le nom de l’ordinateur, puis cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="00f59-108">Right-click the name of the computer, and then click **Properties**.</span></span> <span data-ttu-id="00f59-109">Dans la boîte de dialogue **Propriétés** , sous l’onglet **sécurité** , sélectionnez **Autoriser cet agent à agir en tant que proxy et détecter les objets gérés sur d’autres ordinateurs**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="00f59-109">In the **Properties** dialog box, on the **Security** tab, select **Allow this agent to act as a proxy and discover managed objects on other computers**, and then click **OK**.</span></span>

<span data-ttu-id="00f59-110">À l’issue de l’étape 2, redémarrez le service agent d’intégrité.</span><span class="sxs-lookup"><span data-stu-id="00f59-110">After completing step 2, reboot the Health Agent service.</span></span> <span data-ttu-id="00f59-111">(Le réinitialisation du service entraînera une découverte du nouvel ordinateur.</span><span class="sxs-lookup"><span data-stu-id="00f59-111">(Rebooting the service will “force” discovery of the new machine.</span></span> <span data-ttu-id="00f59-112">Si vous ne redémarrez pas le service, il peut s’écouler jusqu’à 4 heures avant la découverte du nouvel ordinateur par System Center Operations Manager.).</span><span class="sxs-lookup"><span data-stu-id="00f59-112">If you do not reboot the service, it could take as long as 4 hours before the new machine is discovered by System Center Operations Manager.).</span></span> <span data-ttu-id="00f59-113">Après le redémarrage du service, vérifiez qu’aucun événement d’erreur n’est enregistré dans le journal des événements Operations Manager sur cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="00f59-113">After the service has rebooted, verify that no error events are being recorded in the Operations Manager event log on that computer.</span></span>

<span data-ttu-id="00f59-114"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="00f59-114"></div>

<span> </span>

</div>

</div>

</span></span></div>

