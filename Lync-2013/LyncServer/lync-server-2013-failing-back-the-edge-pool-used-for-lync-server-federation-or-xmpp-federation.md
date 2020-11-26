---
title: Restauration du pool Edge utilisé pour la fédération XMPP ou Lync Server
description: Échec du pool Edge utilisé pour la Fédération Lync Server Federation ou XMPP.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Failing back the Edge pool used for Lync Server federation or XMPP federation
ms:assetid: d40097a1-1bed-44dc-aeb6-0871927ab2b9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721897(v=OCS.15)
ms:contentKeyID: 49733831
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 137910d71de1d6177356e0b7bacbd6d17022d71d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428299"
---
# <a name="failing-back-the-edge-pool-used-for-lync-server-federation-or-xmpp-federation-in-lync-server-2013"></a><span data-ttu-id="dc45e-103">Restauration du pool Edge utilisé pour la fédération XMPP ou Lync Server dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dc45e-103">Failing back the Edge pool used for Lync Server federation or XMPP federation in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="dc45e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="dc45e-104">

<span> </span></span></span>

<span data-ttu-id="dc45e-105">_**Dernière modification de la rubrique :** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="dc45e-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="dc45e-106">Après un échec de remise du pool de frontière d’hébergement de la Fédération, utilisez la procédure suivante pour restaurer le routage de Fédération de Lync Server et/ou l’itinéraire de Fédération XMPP pour qu’il utilise de nouveau ce pool de périphéries restauré.</span><span class="sxs-lookup"><span data-stu-id="dc45e-106">After a failed Edge pool that used to host federation has been brought back online, use this procedure to fail back the Lync Server federation route and/or the XMPP federation route to again use this restored Edge pool.</span></span>

<div>

## <a name="failing-back-federation-to-a-restored-edge-pool"></a><span data-ttu-id="dc45e-107">Échec de la Fédération d’arrière-plan vers un pool de périphérie restauré</span><span class="sxs-lookup"><span data-stu-id="dc45e-107">Failing Back Federation to a Restored Edge Pool</span></span>

1.  <span data-ttu-id="dc45e-108">Sur le pool Edge qui est désormais disponible, démarrez les services Edge.</span><span class="sxs-lookup"><span data-stu-id="dc45e-108">On the Edge pool that is now available again, start the Edge Services.</span></span>

2.  <span data-ttu-id="dc45e-109">Si vous souhaitez restaurer l’itinéraire de Fédération de Lync Server pour utiliser le serveur de périphérie restauré, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="dc45e-109">If you want to fail back the Lync Server federation route to use the restored Edge Server, do the following:</span></span>
    
      - <span data-ttu-id="dc45e-110">Sur un serveur frontal, ouvrez le générateur de topologie.</span><span class="sxs-lookup"><span data-stu-id="dc45e-110">On a Front End server, open Topology Builder.</span></span> <span data-ttu-id="dc45e-111">Développez **pools de bords**, puis cliquez avec le bouton droit sur le serveur Edge ou le pool de serveurs Edge actuellement configuré pour la Fédération.</span><span class="sxs-lookup"><span data-stu-id="dc45e-111">Expand **Edge pools**, then right click the Edge server or Edge server pool that is currently configured for Federation.</span></span> <span data-ttu-id="dc45e-112">Sélectionnez **modifier les propriétés**.</span><span class="sxs-lookup"><span data-stu-id="dc45e-112">Select **Edit properties**.</span></span>
    
      - <span data-ttu-id="dc45e-113">Dans **modifier les propriétés** sous **général**, décochez **la case Activer la Fédération pour ce pool de périphériques (port 5061)**.</span><span class="sxs-lookup"><span data-stu-id="dc45e-113">In **Edit Properties** under **General**, clear **Enable federation for this Edge pool (Port 5061)**.</span></span> <span data-ttu-id="dc45e-114">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="dc45e-114">Click **OK**.</span></span>
    
      - <span data-ttu-id="dc45e-115">Développez **pools de bords**, puis cliquez avec le bouton droit sur le serveur Edge d’origine ou sur le pool de serveurs Edge que vous souhaitez utiliser pour la Fédération.</span><span class="sxs-lookup"><span data-stu-id="dc45e-115">Expand **Edge pools**, then right click the original Edge server or Edge server pool that you again want to use for Federation.</span></span> <span data-ttu-id="dc45e-116">Sélectionnez **modifier les propriétés**.</span><span class="sxs-lookup"><span data-stu-id="dc45e-116">Select **Edit properties**.</span></span>
    
      - <span data-ttu-id="dc45e-117">Dans **modifier les propriétés** sous **général**, sélectionnez **activer la Fédération pour ce pool Edge (port 5061)**.</span><span class="sxs-lookup"><span data-stu-id="dc45e-117">In **Edit Properties** under **General**, select **Enable federation for this Edge pool (Port 5061)**.</span></span> <span data-ttu-id="dc45e-118">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="dc45e-118">Click **OK**.</span></span>
    
      - <span data-ttu-id="dc45e-119">Cliquez sur **action**, sélectionnez **topologie**, puis **publier**.</span><span class="sxs-lookup"><span data-stu-id="dc45e-119">Click **Action**, select **Topology**, select **Publish**.</span></span> <span data-ttu-id="dc45e-120">Lorsque le système vous **le** demande, cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="dc45e-120">When prompted on **Publish the topology**, click **Next**.</span></span> <span data-ttu-id="dc45e-121">Lorsque la publication est terminée, cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="dc45e-121">When the Publish is finished, click **Finish**.</span></span>
    
      - <span data-ttu-id="dc45e-122">Sur le serveur Edge, ouvrez l’Assistant Déploiement de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="dc45e-122">On the Edge server, open the Lync Server Deployment wizard.</span></span> <span data-ttu-id="dc45e-123">Cliquez sur **installer ou mettre à jour le système serveur Lync**, puis cliquez sur **configurer ou supprimer les composants Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="dc45e-123">Click **Install or Update Lync Server System**, then click **Setup or Remove Lync Server Components**.</span></span> <span data-ttu-id="dc45e-124">Cliquez de **nouveau sur exécuter**.</span><span class="sxs-lookup"><span data-stu-id="dc45e-124">Click **Run Again**.</span></span>
    
      - <span data-ttu-id="dc45e-125">Dans configurer les composants serveur Lync, cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="dc45e-125">At Setup Lync Server components, click **Next**.</span></span> <span data-ttu-id="dc45e-126">L’écran de synthèse indique les actions à mesure qu’elles sont exécutées.</span><span class="sxs-lookup"><span data-stu-id="dc45e-126">The summary screen will show actions as they are executed.</span></span> <span data-ttu-id="dc45e-127">Lorsque le déploiement est effectué, cliquez sur **afficher le journal** pour afficher les fichiers journaux disponibles.</span><span class="sxs-lookup"><span data-stu-id="dc45e-127">Once the deployment is done, click **View Log** to view available log files.</span></span> <span data-ttu-id="dc45e-128">Cliquez sur **Terminer** pour terminer le déploiement.</span><span class="sxs-lookup"><span data-stu-id="dc45e-128">Click **Finish** to complete the deployment.</span></span>

3.  <span data-ttu-id="dc45e-129">Si vous souhaitez restaurer l’itinéraire de la Fédération XMPP de manière à utiliser le serveur de périphérie de restauration, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="dc45e-129">If you want to fail back the XMPP federation route to use the restored Edge Server, do the following:</span></span>
    
      - <span data-ttu-id="dc45e-130">Exécutez l’applet de commande suivante pour rediriger l’itinéraire de Fédération XMPP vers le pool Edge qui hébergera maintenant la Fédération de XMPP (dans cet exemple, EdgeServer1) :</span><span class="sxs-lookup"><span data-stu-id="dc45e-130">Run the following cmdlet to repoint the XMPP federation route to the Edge pool which will now host XMPP federation (in this example, EdgeServer1):</span></span>
        
            Set-CsSite Site1 -XmppExternalFederationRoute EdgeServer1.contoso.com
        
        <span data-ttu-id="dc45e-131">Dans cet exemple, site1 est le site contenant le pool de bords qui héberge désormais l’itinéraire de Fédération XMPP et EdgeServer1.contoso.com est le nom de domaine complet d’un serveur Edge dans ce pool.</span><span class="sxs-lookup"><span data-stu-id="dc45e-131">In this example, Site1 is the site containing the Edge pool which will now host the XMPP federation route, and EdgeServer1.contoso.com is the FQDN of an Edge Server in that pool.</span></span>
    
      - <span data-ttu-id="dc45e-132">Si vous ne disposez pas encore d’un enregistrement DNS SRV pour la Fédération XMPP qui se résout au pool de périphérie qui hébergera maintenant la Fédération de XMPP, vous devez l’ajouter, comme dans l’exemple ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="dc45e-132">If you do not already have a DNS SRV record for XMPP federation which resolves to the Edge pool which will now host XMPP federation, you must add it, as in the following example.</span></span> <span data-ttu-id="dc45e-133">Cet enregistrement SRV doit avoir une valeur de port de 5269.</span><span class="sxs-lookup"><span data-stu-id="dc45e-133">This SRV record must have a port value of 5269.</span></span>
        
            _xmpp-server._tcp.contoso.com
    
      - <span data-ttu-id="dc45e-134">Sur le serveur DNS externe, modifiez l’enregistrement DNS A pour la Fédération XMPP de sorte qu’il pointe sur EdgeServer2.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="dc45e-134">On the external DNS server, change the DNS A record for XMPP federation to point to EdgeServer2.contoso.com.</span></span>
    
      - <span data-ttu-id="dc45e-135">Assurez-vous que le pool de bords qui hébergera désormais la Fédération XMPP dispose d’une ouverture externe du port 5269.</span><span class="sxs-lookup"><span data-stu-id="dc45e-135">Verify that the Edge pool which will now host XMPP federation has port 5269 open externally.</span></span>

4.  <span data-ttu-id="dc45e-136">Si le pool frontal restait en cours d’exécution sur le site contenant le pool de périphériques ayant échoué et a été restauré, vous devez mettre à jour les services de conférence Web et de service de conférence A/V sur ces pools frontal pour pouvoir utiliser les pools de périphérie sur leur site local.</span><span class="sxs-lookup"><span data-stu-id="dc45e-136">If the Front End pools remained running in the site containing the Edge pool that failed and has been restored, you should update the Web Conferencing Service and A/V Conferencing Service on these Front End pools to again use the Edge pools at their local site.</span></span> <span data-ttu-id="dc45e-137">Pour plus d’informations, reportez-vous à [la section changement du pool de bords associé à un pool frontal dans Lync Server 2013](lync-server-2013-changing-the-edge-pool-associated-with-a-front-end-pool.md).</span><span class="sxs-lookup"><span data-stu-id="dc45e-137">For more information, see [Changing the Edge pool associated with a Front End pool in Lync Server 2013](lync-server-2013-changing-the-edge-pool-associated-with-a-front-end-pool.md).</span></span>

5.  <span data-ttu-id="dc45e-138">Si le pool frontal sur le même site que le pool d’échecs en panne ne fonctionne pas, vous pouvez désormais utiliser Invoke-CsPoolFailback pour restaurer le pool frontal.</span><span class="sxs-lookup"><span data-stu-id="dc45e-138">If the Front End pool at the same site as the failed Edge pool also failed, you can now use Invoke–CsPoolFailback to fail back the Front End pool.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="dc45e-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dc45e-139">See Also</span></span>


[<span data-ttu-id="dc45e-140">Basculement vers le pool Edge utilisé pour la fédération Lync Server dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dc45e-140">Failing over the Edge pool used for Lync Server federation in Lync Server 2013</span></span>](lync-server-2013-failing-over-the-edge-pool-used-for-lync-server-federation.md)  
[<span data-ttu-id="dc45e-141">Basculement vers le pool Edge utilisé pour la fédération XMPP dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dc45e-141">Failing over the Edge pool used for XMPP federation in Lync Server 2013</span></span>](lync-server-2013-failing-over-the-edge-pool-used-for-xmpp-federation.md)  


[<span data-ttu-id="dc45e-142">Récupération d’urgence de serveur Edge dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dc45e-142">Edge Server disaster recovery in Lync Server 2013</span></span>](lync-server-2013-edge-server-disaster-recovery.md)  
  

<span data-ttu-id="dc45e-143"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="dc45e-143"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

