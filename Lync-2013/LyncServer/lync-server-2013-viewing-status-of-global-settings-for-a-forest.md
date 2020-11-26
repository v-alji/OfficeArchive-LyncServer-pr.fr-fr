---
title: 'Lync Server 2013 : affichage de l’état des paramètres globaux d’une forêt'
description: 'Lync Server 2013 : affichage de l’état des paramètres globaux d’une forêt.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: View status of global settings for a forest
ms:assetid: 2ab0f2f1-9908-4e6f-aff3-d6b3cc474b6b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn747889(v=OCS.15)
ms:contentKeyID: 63969590
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d9f722ea66f6c54c816703bd1af1d3def57bbd84
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443908"
---
# <a name="view-status-of-global-settings-for-a-forest-in-lync-server-2013"></a><span data-ttu-id="10bfe-103">Afficher l’état des paramètres globaux pour une forêt dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="10bfe-103">View status of global settings for a forest in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="10bfe-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="10bfe-104">

<span> </span></span></span>

<span data-ttu-id="10bfe-105">_**Dernière modification de la rubrique :** 2014-05-20_</span><span class="sxs-lookup"><span data-stu-id="10bfe-105">_**Topic Last Modified:** 2014-05-20_</span></span>

<span data-ttu-id="10bfe-106">Les administrateurs doivent vérifier les paramètres globaux d’un déploiement de Lync Server 2013 au mois.</span><span class="sxs-lookup"><span data-stu-id="10bfe-106">Administrators should review the global settings for a Lync Server 2013 deployment monthly.</span></span> <span data-ttu-id="10bfe-107">L’objectif consiste à passer en revue des paramètres implémentés à l’aide d’un ensemble de configurations connues : une configuration de référence pour garantir que les paramètres soient valides et déterminez si la documentation de référence doit être mise à jour.</span><span class="sxs-lookup"><span data-stu-id="10bfe-107">The objective would be to review implemented settings against a set of known configurations—a baseline configuration to help guarantee that settings are valid and to determine whether the baseline documentation should be updated.</span></span> <span data-ttu-id="10bfe-108">Les modifications apportées au paramètre global doivent être implémentées par le biais d’un processus de contrôle des modifications qui devrait inclure la documentation des nouveaux paramètres.</span><span class="sxs-lookup"><span data-stu-id="10bfe-108">Changes to global setting should be implemented through a Change Control process which should include documenting the new settings.</span></span>

<span data-ttu-id="10bfe-109">Les paramètres globaux qui doivent être examinés sont décrits dans les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="10bfe-109">Global settings that should be reviewed are described in the following sections:</span></span>

<div>

## <a name="check-general-settings"></a><span data-ttu-id="10bfe-110">Vérifier les paramètres généraux</span><span class="sxs-lookup"><span data-stu-id="10bfe-110">Check general settings</span></span>

<span data-ttu-id="10bfe-111">Vérifiez les paramètres généraux, y compris les domaines compatibles SIP (Session Initiation Protocol) pour Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="10bfe-111">Check general settings, including the supported Session Initiation Protocol (SIP) domains for Lync Server 2013.</span></span>

<span data-ttu-id="10bfe-112">Les informations de domaine SIP peuvent être renvoyées à l’aide de Windows PowerShell et de l’applet **de cmdlet Get-CsSipDomain** .</span><span class="sxs-lookup"><span data-stu-id="10bfe-112">SIP domain information can be returned by using Windows PowerShell and the **Get-CsSipDomain** cmdlet.</span></span> <span data-ttu-id="10bfe-113">Pour obtenir ces informations, exécutez la `Get-CsSipDomain` commande Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="10bfe-113">To return this information, run the `Get-CsSipDomain` Windows PowerShell command.</span></span>

<span data-ttu-id="10bfe-114">Get-CsSipDomain renverra des informations similaires à ce qui suit pour tous les domaines SIP autorisés :</span><span class="sxs-lookup"><span data-stu-id="10bfe-114">Get-CsSipDomain will return information similar to this for all the authorized SIP domains:</span></span>

<span data-ttu-id="10bfe-115">Nom d’identité IsDefault</span><span class="sxs-lookup"><span data-stu-id="10bfe-115">Identity Name IsDefault</span></span>

<span data-ttu-id="10bfe-116">\-------- ---- ---------</span><span class="sxs-lookup"><span data-stu-id="10bfe-116">\-------- ---- ---------</span></span>

<span data-ttu-id="10bfe-117">fabrikam.com fabrikam.com true</span><span class="sxs-lookup"><span data-stu-id="10bfe-117">fabrikam.com fabrikam.com True</span></span>

<span data-ttu-id="10bfe-118">na.fabrikam.com na.fabrikam.com false</span><span class="sxs-lookup"><span data-stu-id="10bfe-118">na.fabrikam.com na.fabrikam.com False</span></span>

<span data-ttu-id="10bfe-119">Si la propriété IsDefault est définie sur true, le domaine correspondant est le domaine SIP par défaut.</span><span class="sxs-lookup"><span data-stu-id="10bfe-119">If the IsDefault property is set to True, the corresponding domain is your default SIP domain.</span></span> <span data-ttu-id="10bfe-120">Vous pouvez utiliser l’applet de passe Set-CsSipDomain pour changer le domaine SIP par défaut de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="10bfe-120">You can use the Set-CsSipDomain cmdlet to change the default SIP domain for your organization.</span></span> <span data-ttu-id="10bfe-121">Toutefois, vous ne pouvez pas supprimer le domaine SIP par défaut, car cela vous laisserait sans domaine par défaut.</span><span class="sxs-lookup"><span data-stu-id="10bfe-121">However, you can't just delete the default SIP domain because that would leave you without a default domain.</span></span> <span data-ttu-id="10bfe-122">Si vous souhaitez supprimer le domaine fabrikam.com (comme illustré dans l’exemple précédent), vous devez commencer par configurer na.fabrikam.com comme domaine par défaut.</span><span class="sxs-lookup"><span data-stu-id="10bfe-122">If you wanted to delete the fabrikam.com domain (as shown in the previous example), you would first have to configure na.fabrikam.com to be your default domain.</span></span>

</div>

<div>

## <a name="check-meeting-settings"></a><span data-ttu-id="10bfe-123">Vérifier les paramètres de la réunion</span><span class="sxs-lookup"><span data-stu-id="10bfe-123">Check meeting settings</span></span>

<span data-ttu-id="10bfe-124">Les paramètres de réunion incluent les définitions de stratégie de réunion et la prise en charge de la participation d’utilisateurs anonymes à des réunions.</span><span class="sxs-lookup"><span data-stu-id="10bfe-124">Meeting settings include meeting policy definitions and support for participation of anonymous users in meetings.</span></span>

<span data-ttu-id="10bfe-125">Les paramètres de configuration de réunion peuvent être récupérés à l’aide de Windows PowerShell et de l’applet **de cmdlet Get-CsMeetingConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="10bfe-125">Meeting configuration settings can be retrieved by using Windows PowerShell and the **Get-CsMeetingConfiguration** cmdlet.</span></span> <span data-ttu-id="10bfe-126">Par exemple, la commande suivante renvoie des informations sur les paramètres de configuration de la réunion globale :</span><span class="sxs-lookup"><span data-stu-id="10bfe-126">For example, this command returns information about the global meeting configuration settings:</span></span>

<span data-ttu-id="10bfe-127">Get-CsMeetingConfiguration : les paramètres de configuration de la réunion « global » peuvent également être configurés sur l’étendue du site.</span><span class="sxs-lookup"><span data-stu-id="10bfe-127">Get-CsMeetingConfiguration –Identity "Global"Meeting configuration settings can also be configured at the site scope.</span></span> <span data-ttu-id="10bfe-128">Pour cette raison, vous souhaiterez peut-être utiliser la commande suivante qui renvoie des informations sur tous les paramètres de configuration de la réunion :</span><span class="sxs-lookup"><span data-stu-id="10bfe-128">Because of that, you might want to use the following command, which returns information about all the meeting configuration settings:</span></span>

`Get-CsMeetingConfiguration`

<span data-ttu-id="10bfe-129">L’applet de commande **Get-CsMeetingConfiguration** renvoie des informations similaires à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="10bfe-129">The **Get-CsMeetingConfiguration** cmdlet returns information similar to the following:</span></span>

<span data-ttu-id="10bfe-130">Identity : global</span><span class="sxs-lookup"><span data-stu-id="10bfe-130">Identity : Global</span></span>

<span data-ttu-id="10bfe-131">PstnCallersBypassLobby : true</span><span class="sxs-lookup"><span data-stu-id="10bfe-131">PstnCallersBypassLobby : True</span></span>

<span data-ttu-id="10bfe-132">EnableAssignedConferenceType : true</span><span class="sxs-lookup"><span data-stu-id="10bfe-132">EnableAssignedConferenceType : True</span></span>

<span data-ttu-id="10bfe-133">DesignateAsPresenter : société</span><span class="sxs-lookup"><span data-stu-id="10bfe-133">DesignateAsPresenter : Company</span></span>

<span data-ttu-id="10bfe-134">AssignedConferenceTypeByDefault : true</span><span class="sxs-lookup"><span data-stu-id="10bfe-134">AssignedConferenceTypeByDefault : True</span></span>

<span data-ttu-id="10bfe-135">AdmitAnonymousUsersByDefault : true</span><span class="sxs-lookup"><span data-stu-id="10bfe-135">AdmitAnonymousUsersByDefault : True</span></span>

<span data-ttu-id="10bfe-136">Là encore, le dernier élément de la liste, **AdmitAnonymousUsersByDefault**, active ou désactive la possibilité pour les utilisateurs anonymes de participer aux réunions.</span><span class="sxs-lookup"><span data-stu-id="10bfe-136">Again, the final item in the list, **AdmitAnonymousUsersByDefault**, enables or disables the ability of anonymous users to participate in meetings.</span></span>

<span data-ttu-id="10bfe-137">Lors de la vérification des paramètres de configuration de la réunion, vous trouverez peut-être utile de comparer les paramètres actuels par rapport aux équivalents par défaut.</span><span class="sxs-lookup"><span data-stu-id="10bfe-137">When checking meeting configuration settings, you might find it useful to compare the current settings against the default equivalents.</span></span> <span data-ttu-id="10bfe-138">Vous pouvez afficher les paramètres de configuration de la réunion par défaut en exécutant la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="10bfe-138">You can view the default meeting configuration settings by running the following command:</span></span>

`New-CsMeetingConfiguration -Identity "Global" -InMemory`

<span data-ttu-id="10bfe-139">La commande précédente crée une instance en mémoire uniquement des paramètres de configuration de réunion globale, une instance qui utilise la valeur par défaut pour chaque propriété.</span><span class="sxs-lookup"><span data-stu-id="10bfe-139">The previous command creates an in-memory-only instance of the global meeting configuration settings, an instance that uses the default value for each property.</span></span> <span data-ttu-id="10bfe-140">Aucun paramètre de configuration de réunion réel n’est créé lors de l’exécution de la commande.</span><span class="sxs-lookup"><span data-stu-id="10bfe-140">No actual meeting configuration settings are created when you run the command.</span></span> <span data-ttu-id="10bfe-141">Toutefois, toutes les valeurs de propriété par défaut s’affichent à l’écran.</span><span class="sxs-lookup"><span data-stu-id="10bfe-141">However, all the default property values will be displayed on-screen.</span></span>

</div>

<div>

## <a name="check-edge-servers-and-their-settings"></a><span data-ttu-id="10bfe-142">Vérifier les serveurs Edge et leurs paramètres</span><span class="sxs-lookup"><span data-stu-id="10bfe-142">Check Edge Servers and their settings</span></span>

<span data-ttu-id="10bfe-143">Vous pouvez récupérer les informations sur le serveur Edge à l’aide de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="10bfe-143">Edge Server information can be retrieved by using Windows PowerShell.</span></span> <span data-ttu-id="10bfe-144">Cette commande renvoie des informations sur tous les serveurs Edge configurés pour une utilisation au sein de votre organisation :</span><span class="sxs-lookup"><span data-stu-id="10bfe-144">This command returns information about all the Edge Servers configured for use in your organization:</span></span>

`Get-CsService -EdgeServer`

<span data-ttu-id="10bfe-145">Les informations renvoyées incluent tous les paramètres de nom de domaine complet et de port de chaque serveur Edge :</span><span class="sxs-lookup"><span data-stu-id="10bfe-145">The returned information includes all of the FQDN and port settings for each Edge Server:</span></span>

<span data-ttu-id="10bfe-146">Identité : EdgeServer : dc.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="10bfe-146">Identity : EdgeServer: dc.fabrikam.com</span></span>

<span data-ttu-id="10bfe-147">Bureau d’enregistrement : LYNC-SE.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="10bfe-147">Registrar : Registrar: LYNC-SE.fabrikam.com</span></span>

<span data-ttu-id="10bfe-148">AccessEdgeInternalSipPort : 5061</span><span class="sxs-lookup"><span data-stu-id="10bfe-148">AccessEdgeInternalSipPort : 5061</span></span>

<span data-ttu-id="10bfe-149">AccessEdgeExternalSipPort : 5061</span><span class="sxs-lookup"><span data-stu-id="10bfe-149">AccessEdgeExternalSipPort : 5061</span></span>

<span data-ttu-id="10bfe-150">AccessEdgeClientPort : 443</span><span class="sxs-lookup"><span data-stu-id="10bfe-150">AccessEdgeClientPort : 443</span></span>

<span data-ttu-id="10bfe-151">DataPsomServerPort : 8057</span><span class="sxs-lookup"><span data-stu-id="10bfe-151">DataPsomServerPort : 8057</span></span>

<span data-ttu-id="10bfe-152">DataPsomClientPort : 444</span><span class="sxs-lookup"><span data-stu-id="10bfe-152">DataPsomClientPort : 444</span></span>

<span data-ttu-id="10bfe-153">MediaRelayAuthEdgePort : 5062</span><span class="sxs-lookup"><span data-stu-id="10bfe-153">MediaRelayAuthEdgePort : 5062</span></span>

<span data-ttu-id="10bfe-154">MediaRelayAuthInternalTurnTcpPort : 443</span><span class="sxs-lookup"><span data-stu-id="10bfe-154">MediaRelayAuthInternalTurnTcpPort : 443</span></span>

<span data-ttu-id="10bfe-155">MediaRelayAuthExternalTurnTcpPort : 445</span><span class="sxs-lookup"><span data-stu-id="10bfe-155">MediaRelayAuthExternalTurnTcpPort : 445</span></span>

<span data-ttu-id="10bfe-156">MediaRelayAuthInternalTurnUdpPort : 3478</span><span class="sxs-lookup"><span data-stu-id="10bfe-156">MediaRelayAuthInternalTurnUdpPort : 3478</span></span>

<span data-ttu-id="10bfe-157">MediaRelayAuthExternalTurnUdpPort : 3478</span><span class="sxs-lookup"><span data-stu-id="10bfe-157">MediaRelayAuthExternalTurnUdpPort : 3478</span></span>

<span data-ttu-id="10bfe-158">MediaCommunicationPortStart : 50000</span><span class="sxs-lookup"><span data-stu-id="10bfe-158">MediaCommunicationPortStart : 50000</span></span>

<span data-ttu-id="10bfe-159">MediaComunicationPortCount : 10000</span><span class="sxs-lookup"><span data-stu-id="10bfe-159">MediaComunicationPortCount : 10000</span></span>

<span data-ttu-id="10bfe-160">AccessEdgeExternalFqdn : dc.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="10bfe-160">AccessEdgeExternalFqdn : dc.fabrikam.com</span></span>

<span data-ttu-id="10bfe-161">DataEdgeExternalFqdn : dc.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="10bfe-161">DataEdgeExternalFqdn : dc.fabrikam.com</span></span>

<span data-ttu-id="10bfe-162">AVEdgeExternalFqdn :</span><span class="sxs-lookup"><span data-stu-id="10bfe-162">AVEdgeExternalFqdn :</span></span>

<span data-ttu-id="10bfe-163">InternalInterfaceFqdn :</span><span class="sxs-lookup"><span data-stu-id="10bfe-163">InternalInterfaceFqdn :</span></span>

<span data-ttu-id="10bfe-164">ExternalMrasFqdn : dc.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="10bfe-164">ExternalMrasFqdn : dc.fabrikam.com</span></span>

<span data-ttu-id="10bfe-165">DependentServiceList : {Registrar : LYNC-SE.fabrikam.com,</span><span class="sxs-lookup"><span data-stu-id="10bfe-165">DependentServiceList : {Registrar:LYNC-SE.fabrikam.com,</span></span>

<span data-ttu-id="10bfe-166">ConferencingServer : LYNC-SE. fabrikam</span><span class="sxs-lookup"><span data-stu-id="10bfe-166">ConferencingServer:LYNC-SE.fabrikam</span></span>

<span data-ttu-id="10bfe-167">com, MediationServer : LYNC-SE.</span><span class="sxs-lookup"><span data-stu-id="10bfe-167">com, MediationServer:LYNC-SE.</span></span>

<span data-ttu-id="10bfe-168">fabrikam.com}</span><span class="sxs-lookup"><span data-stu-id="10bfe-168">fabrikam.com}</span></span>

<span data-ttu-id="10bfe-169">ServiceId : fabrikam.com-EdgeServer-2</span><span class="sxs-lookup"><span data-stu-id="10bfe-169">ServiceId : fabrikam.com-EdgeServer-2</span></span>

<span data-ttu-id="10bfe-170">SiteId : site :fabrikam. com</span><span class="sxs-lookup"><span data-stu-id="10bfe-170">SiteId : site:fabrikam.com</span></span>

<span data-ttu-id="10bfe-171">PoolFqdn : dc.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="10bfe-171">PoolFqdn : dc.fabrikam.com</span></span>

<span data-ttu-id="10bfe-172">Version : 5</span><span class="sxs-lookup"><span data-stu-id="10bfe-172">Version : 5</span></span>

<span data-ttu-id="10bfe-173">Rôle : EdgeServer</span><span class="sxs-lookup"><span data-stu-id="10bfe-173">Role : EdgeServer</span></span>

<div>

## <a name="check-federation-settings"></a><span data-ttu-id="10bfe-174">Vérifier les paramètres de Fédération</span><span class="sxs-lookup"><span data-stu-id="10bfe-174">Check federation settings</span></span>

<span data-ttu-id="10bfe-175">Vérifiez les paramètres de Fédération (par exemple, s’il est configuré et, si la réponse est « oui »), les nom de domaine complet et port.</span><span class="sxs-lookup"><span data-stu-id="10bfe-175">Check Federation settings, such as whether it is configured and, if the answer is "yes,", the FQDN and port.</span></span> <span data-ttu-id="10bfe-176">La Fédération est activée et désactivée à l’aide de l’ensemble global de paramètres de configuration de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="10bfe-176">Federation is enabled and disabled by using the global collection of Access Edge configuration settings.</span></span> <span data-ttu-id="10bfe-177">Entre autres choses, cela signifie que la Fédération est configurée sur une base « tout-le » : une Fédération est activée pour l’ensemble de l’organisation ou la Fédération est désactivée pour l’ensemble de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="10bfe-177">Among other things, these mean that federation is configured on an all-or-nothing basis: either federation is enabled for the whole organization or federation is disabled for the whole organization</span></span>

<span data-ttu-id="10bfe-178">Les paramètres de configuration de Microsoft Edge peuvent être retournés à l’aide de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="10bfe-178">Your Access Edge configuration settings can be returned by using Windows PowerShell.</span></span> <span data-ttu-id="10bfe-179">Pour cela, exécutez la commande Windows PowerShell suivante :</span><span class="sxs-lookup"><span data-stu-id="10bfe-179">To do that, run the following Windows PowerShell command:</span></span>

`Get-CsAccessEdgeConfiguration`

<span data-ttu-id="10bfe-180">Ensuite, cette commande renvoie des données similaires à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="10bfe-180">In turn, that command will return data similar to this:</span></span>

<span data-ttu-id="10bfe-181">Identity : global</span><span class="sxs-lookup"><span data-stu-id="10bfe-181">Identity : Global</span></span>

<span data-ttu-id="10bfe-182">AllowAnonymousUsers : false</span><span class="sxs-lookup"><span data-stu-id="10bfe-182">AllowAnonymousUsers : False</span></span>

<span data-ttu-id="10bfe-183">AllowFederatedUsers : false</span><span class="sxs-lookup"><span data-stu-id="10bfe-183">AllowFederatedUsers : False</span></span>

<span data-ttu-id="10bfe-184">AllowOutsideUsers : false</span><span class="sxs-lookup"><span data-stu-id="10bfe-184">AllowOutsideUsers : False</span></span>

<span data-ttu-id="10bfe-185">Concentrez-vous : faux</span><span class="sxs-lookup"><span data-stu-id="10bfe-185">BeClearingHouse : False</span></span>

<span data-ttu-id="10bfe-186">EnablePartnerDiscovery : false</span><span class="sxs-lookup"><span data-stu-id="10bfe-186">EnablePartnerDiscovery : False</span></span>

<span data-ttu-id="10bfe-187">EnableArchivingDisclaimer : false</span><span class="sxs-lookup"><span data-stu-id="10bfe-187">EnableArchivingDisclaimer : False</span></span>

<span data-ttu-id="10bfe-188">KeepCrlsUpToDateForPeers : true</span><span class="sxs-lookup"><span data-stu-id="10bfe-188">KeepCrlsUpToDateForPeers : True</span></span>

<span data-ttu-id="10bfe-189">MarkSourceVerifiableOnOutgoingMessages : true</span><span class="sxs-lookup"><span data-stu-id="10bfe-189">MarkSourceVerifiableOnOutgoingMessages : True</span></span>

<span data-ttu-id="10bfe-190">OutgoingTlsCountForFederatedPartners : 4</span><span class="sxs-lookup"><span data-stu-id="10bfe-190">OutgoingTlsCountForFederatedPartners : 4</span></span>

<span data-ttu-id="10bfe-191">RoutingMethod : UseDnsSrvRouting</span><span class="sxs-lookup"><span data-stu-id="10bfe-191">RoutingMethod : UseDnsSrvRouting</span></span>

<span data-ttu-id="10bfe-192">Si la propriété **AllowFederatedUsers** est définie sur true, cela signifie que la Fédération est activée pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="10bfe-192">If the **AllowFederatedUsers** property is set to True, that means that federation is enabled for your organization.</span></span> <span data-ttu-id="10bfe-193">(Si vous définissez la propriété **AllowFederatedUsers** sur true, dans un scénario de domaine fractionné, vos utilisateurs locaux pourront communiquer en toute transparence avec vos utilisateurs dans le Cloud.)</span><span class="sxs-lookup"><span data-stu-id="10bfe-193">(Setting **AllowFederatedUsers** to True also means that, in a split domain scenario, your on-premises users will be able to communicate seamlessly with your in-the-cloud users.)</span></span>

<span data-ttu-id="10bfe-194">Pour récupérer les paramètres de nom de domaine complet et de port de votre serveur Edge, voir la tâche précédente (serveurs de bord et leurs paramètres).</span><span class="sxs-lookup"><span data-stu-id="10bfe-194">To retrieve the FQDN and port settings for your Edge Server, see the previous task (Edge Servers and their settings).</span></span>

<span data-ttu-id="10bfe-195">L’activation de la Fédération au niveau de l’étendue globale signifie que les utilisateurs peuvent éventuellement communiquer avec des utilisateurs fédérés.</span><span class="sxs-lookup"><span data-stu-id="10bfe-195">Enabling federation at the global scope only means that users can potentially communicate with federated users.</span></span> <span data-ttu-id="10bfe-196">Pour déterminer si des utilisateurs individuels peuvent communiquer avec des utilisateurs fédérés, vous devez examiner la stratégie d’accès des utilisateurs externes affectée à cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="10bfe-196">To determine whether any individual users can actually communicate with federated users requires you to examine the external user access policy assigned to that user.</span></span>

<span data-ttu-id="10bfe-197">Les informations d’accès des utilisateurs externes peuvent être renvoyées à l’aide de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="10bfe-197">External user access information can be returned by using Windows PowerShell.</span></span> <span data-ttu-id="10bfe-198">Par exemple, cette commande renvoie des informations sur la stratégie globale d’accès des utilisateurs externes :</span><span class="sxs-lookup"><span data-stu-id="10bfe-198">For example, this command returns information for the global external user access policy:</span></span>

`Get-CsExternalAccessPolicy -Identity "Global"`

<span data-ttu-id="10bfe-199">Cette commande renvoie des informations pour toutes les stratégies d’accès des utilisateurs externes :</span><span class="sxs-lookup"><span data-stu-id="10bfe-199">And this command returns information for all the external user access policies:</span></span>

`Get-CsExternalAccessPolicy`

<span data-ttu-id="10bfe-200">Les informations renvoyées sont similaires à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="10bfe-200">The returned information will resemble this:</span></span>

<span data-ttu-id="10bfe-201">Identity : false</span><span class="sxs-lookup"><span data-stu-id="10bfe-201">Identity : False</span></span>

<span data-ttu-id="10bfe-202">Description</span><span class="sxs-lookup"><span data-stu-id="10bfe-202">Description :</span></span>

<span data-ttu-id="10bfe-203">EnableFederationAccess : false</span><span class="sxs-lookup"><span data-stu-id="10bfe-203">EnableFederationAccess : False</span></span>

<span data-ttu-id="10bfe-204">EnablePublicCloudAccess : false</span><span class="sxs-lookup"><span data-stu-id="10bfe-204">EnablePublicCloudAccess : False</span></span>

<span data-ttu-id="10bfe-205">EnablePublicCloudAccessAudioVideoAccess : false</span><span class="sxs-lookup"><span data-stu-id="10bfe-205">EnablePublicCloudAccessAudioVideoAccess : False</span></span>

<span data-ttu-id="10bfe-206">EnableOutsideAccess : false</span><span class="sxs-lookup"><span data-stu-id="10bfe-206">EnableOutsideAccess : False</span></span>

<span data-ttu-id="10bfe-207">Si **EnableFederationAccess** est défini sur true, les utilisateurs gérés par la stratégie donnée peuvent communiquer avec des utilisateurs fédérés.</span><span class="sxs-lookup"><span data-stu-id="10bfe-207">If **EnableFederationAccess** is set to True, then users managed by the given policy can communicate with federated users.</span></span>

</div>

</div>

<div>

## <a name="check-archiving-settings"></a><span data-ttu-id="10bfe-208">Vérifier les paramètres d’archivage</span><span class="sxs-lookup"><span data-stu-id="10bfe-208">Check archiving settings</span></span>

<span data-ttu-id="10bfe-209">Vérifiez les paramètres d’archivage des communications internes et fédérées. Avant de vérifier les paramètres de l’archivage interne et externe, vérifiez que l’archivage est activé.</span><span class="sxs-lookup"><span data-stu-id="10bfe-209">Check archiving settings for internal and federated communications.Before verifying the settings for internal and external archiving, you should verify that archiving is enabled.</span></span>

<span data-ttu-id="10bfe-210">Les paramètres de configuration de l’archivage peuvent être vérifiés à l’aide de Windows PowerShell et de l’applet de Get-CsArchivingConfiguration.</span><span class="sxs-lookup"><span data-stu-id="10bfe-210">Archiving configuration settings can be verified by using Windows PowerShell and the Get-CsArchivingConfiguration cmdlet:</span></span>

`Get-CsArchivingConfiguration -Identity "Global"`

<span data-ttu-id="10bfe-211">Notez que vous pouvez également configurer les paramètres d’archivage à l’étendue du site.</span><span class="sxs-lookup"><span data-stu-id="10bfe-211">Note that archiving settings can also be configured at the site scope.</span></span> <span data-ttu-id="10bfe-212">Pour renvoyer des informations sur les paramètres d’archivage, utilisez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="10bfe-212">To return information about all the archiving settings, use this command:</span></span>

`Get-CsArchivingConfiguration`

<span data-ttu-id="10bfe-213">L’applet de requête Get-CsArchivingConfiguration renvoie des données similaires à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="10bfe-213">The Get-CsArchivingConfiguration cmdlet returns data similar to this:</span></span>

<span data-ttu-id="10bfe-214">Identity : global</span><span class="sxs-lookup"><span data-stu-id="10bfe-214">Identity : Global</span></span>

<span data-ttu-id="10bfe-215">EnableArchiving : false</span><span class="sxs-lookup"><span data-stu-id="10bfe-215">EnableArchiving : False</span></span>

<span data-ttu-id="10bfe-216">EnablePurging : false</span><span class="sxs-lookup"><span data-stu-id="10bfe-216">EnablePurging : False</span></span>

<span data-ttu-id="10bfe-217">PurgeExportedArchivesOnly : false</span><span class="sxs-lookup"><span data-stu-id="10bfe-217">PurgeExportedArchivesOnly : False</span></span>

<span data-ttu-id="10bfe-218">BlockOnArchiveFailure : false</span><span class="sxs-lookup"><span data-stu-id="10bfe-218">BlockOnArchiveFailure : False</span></span>

<span data-ttu-id="10bfe-219">KeepArchivingDataForDays : 14</span><span class="sxs-lookup"><span data-stu-id="10bfe-219">KeepArchivingDataForDays : 14</span></span>

<span data-ttu-id="10bfe-220">PurgeHourOfDay : 2</span><span class="sxs-lookup"><span data-stu-id="10bfe-220">PurgeHourOfDay : 2</span></span>

<span data-ttu-id="10bfe-221">ArchiveDuplicateMessages : true</span><span class="sxs-lookup"><span data-stu-id="10bfe-221">ArchiveDuplicateMessages : True</span></span>

<span data-ttu-id="10bfe-222">CachePurgingInterval : 24</span><span class="sxs-lookup"><span data-stu-id="10bfe-222">CachePurgingInterval : 24</span></span>

<span data-ttu-id="10bfe-223">Si la propriété EnableArchiving est définie sur false, cela signifie qu’aucune session de communication n’est archivée.</span><span class="sxs-lookup"><span data-stu-id="10bfe-223">If the EnableArchiving property is set to False, that means that no communication sessions will be archived.</span></span> <span data-ttu-id="10bfe-224">Si vous voulez uniquement archiver des sessions de messagerie instantanée, utilisez une commande telle que celle qui suit pour activer l’archivage des sessions de messagerie instantanée :</span><span class="sxs-lookup"><span data-stu-id="10bfe-224">If you want to archive instant messaging sessions only, use a command such as the following to enable the archiving of IM sessions:</span></span>

`Set-CsArchivingConfiguration -Identity "Global" -EnableArchiving "IMOnly"`

<span data-ttu-id="10bfe-225">Pour archiver des sessions de conférence et des sessions de messagerie instantanée, utilisez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="10bfe-225">To archive conferencing sessions and instant messaging sessions, use this command:</span></span>

`Set-CsArchivingConfiguration -Identity "Global" -EnableArchiving "IMOnly"`

<span data-ttu-id="10bfe-226">Si vous souhaitez comparer vos paramètres d’archivage actuels avec les paramètres par défaut, exécutez la commande Windows PowerShell suivante :</span><span class="sxs-lookup"><span data-stu-id="10bfe-226">If you’d like to compare your current archiving settings with the default settings, run the following Windows PowerShell command:</span></span>

`New-CsArchivingConfiguration -Identity "Global" -InMemory`

<span data-ttu-id="10bfe-227">Cette commande crée une instance en mémoire uniquement des paramètres de configuration de l’archivage global.</span><span class="sxs-lookup"><span data-stu-id="10bfe-227">That command creates an in-memory-only instance of the global archiving configuration settings.</span></span> <span data-ttu-id="10bfe-228">Ce n’est pas une collection réelle de paramètres qui est utilisée par Lync Server.</span><span class="sxs-lookup"><span data-stu-id="10bfe-228">This is not a real collection of settings that is used by Lync Server.</span></span> <span data-ttu-id="10bfe-229">Toutefois, elle affiche les valeurs par défaut de toutes les propriétés de configuration de l’archivage.</span><span class="sxs-lookup"><span data-stu-id="10bfe-229">However, it does display the default values for all the archiving configuration properties.</span></span>

<span data-ttu-id="10bfe-230">Vous pouvez également utiliser cette commande pour renvoyer le nom de domaine complet de vos serveurs d’archivage :</span><span class="sxs-lookup"><span data-stu-id="10bfe-230">You can also use this command to return the FQDN of your Archiving servers:</span></span>

`Get-CsService -ArchivingServer`

<span data-ttu-id="10bfe-231">Après vérification de l’activation de l’archivage, vous pouvez afficher vos politiques d’archivage pour déterminer si les sessions internes et externes de communication sont archivées.</span><span class="sxs-lookup"><span data-stu-id="10bfe-231">After you have verified that archiving is enabled, you can then view your archiving policies to determine whether internal and external communication sessions are being archived.</span></span>

<span data-ttu-id="10bfe-232">Vous pouvez récupérer les informations de stratégie d’archivage à l’aide de l’applet de Get-CsArchivingPolicy.</span><span class="sxs-lookup"><span data-stu-id="10bfe-232">Archiving policy information can be retrieved by using the Get-CsArchivingPolicy cmdlet.</span></span> <span data-ttu-id="10bfe-233">Par exemple, cette commande renvoie des informations sur la stratégie d’archivage globale :</span><span class="sxs-lookup"><span data-stu-id="10bfe-233">For example, this command returns information about the global archiving policy:</span></span>

`Get-CsArchivingPolicy -Identity "Global"`

<span data-ttu-id="10bfe-234">Étant donné que les stratégies d’archivage peuvent également être configurées au niveau du site et de l’étendue par utilisateur, vous pouvez également utiliser cette commande pour renvoyer des informations sur toutes les stratégies d’archivage :</span><span class="sxs-lookup"><span data-stu-id="10bfe-234">Because archiving policies can also be configured at the site and the per-user scope, you might also want to use this command, which returns information about all the archiving policies:</span></span>

`Get-CsArchivingPolicy`

<span data-ttu-id="10bfe-235">Les informations que vous recevez de Get-CsArchivingPolicy sont similaires à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="10bfe-235">The information that you receive from Get-CsArchivingPolicy will resemble this:</span></span>

<span data-ttu-id="10bfe-236">Identity : global</span><span class="sxs-lookup"><span data-stu-id="10bfe-236">Identity : Global</span></span>

<span data-ttu-id="10bfe-237">Description</span><span class="sxs-lookup"><span data-stu-id="10bfe-237">Description :</span></span>

<span data-ttu-id="10bfe-238">ArchiveInternal : false</span><span class="sxs-lookup"><span data-stu-id="10bfe-238">ArchiveInternal : False</span></span>

<span data-ttu-id="10bfe-239">ArchiveExternal : false</span><span class="sxs-lookup"><span data-stu-id="10bfe-239">ArchiveExternal : False</span></span>

<span data-ttu-id="10bfe-240">Notez que, par défaut, l’archivage interne et externe est désactivé dans une stratégie d’archivage.</span><span class="sxs-lookup"><span data-stu-id="10bfe-240">Note that, by default, both internal and external archiving are disabled in an archiving policy.</span></span>

</div>

<div>

## <a name="check-cdr-settings"></a><span data-ttu-id="10bfe-241">Vérifier les paramètres CDR</span><span class="sxs-lookup"><span data-stu-id="10bfe-241">Check CDR settings</span></span>

<span data-ttu-id="10bfe-242">Vérifiez les paramètres d’enregistrement des détails des appels (CDR) pour l’enregistrement des détails des appels d’égal à égal, de conférence et d’appel vocal.</span><span class="sxs-lookup"><span data-stu-id="10bfe-242">Check Call Detail Record (CDR) settings for peer-to-peer, conferencing, and Voice call detail recording.</span></span> <span data-ttu-id="10bfe-243">Des informations détaillées sur vos paramètres CDR peuvent être renvoyées à l’aide de l’applet **de passe Get-CsCdrConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="10bfe-243">Detailed information about your CDR settings can be returned by using the **Get-CsCdrConfiguration** cmdlet.</span></span> <span data-ttu-id="10bfe-244">Par exemple, cette commande renvoie des informations sur la collection globale de paramètres de configuration de CDR :</span><span class="sxs-lookup"><span data-stu-id="10bfe-244">For example, this command returns information about the global collection of CDR configuration settings:</span></span>

`Get-CsCdrConfiguration -Identity "Global"`

<span data-ttu-id="10bfe-245">Comme CDR peut également être configuré sur l’étendue du site, vous souhaiterez peut-être également exécuter cette commande, qui renvoie des informations sur tous les paramètres de configuration de CDR :</span><span class="sxs-lookup"><span data-stu-id="10bfe-245">Because CDR can also be configured at the site scope, you might also want to run this command, which returns information about all the CDR configuration settings:</span></span>

`Get-CsCdrConfiguration`

<span data-ttu-id="10bfe-246">L’applet de requête Get-CsCdrConfiguration renvoie des informations similaires pour chaque ensemble de paramètres de configuration CDR :</span><span class="sxs-lookup"><span data-stu-id="10bfe-246">The Get-CsCdrConfiguration cmdlet returns information similar to this for each collection of CDR configuration settings:</span></span>

<span data-ttu-id="10bfe-247">Identity : global</span><span class="sxs-lookup"><span data-stu-id="10bfe-247">Identity : Global</span></span>

<span data-ttu-id="10bfe-248">EnableCDR : true</span><span class="sxs-lookup"><span data-stu-id="10bfe-248">EnableCDR : True</span></span>

<span data-ttu-id="10bfe-249">EnablePurging : true</span><span class="sxs-lookup"><span data-stu-id="10bfe-249">EnablePurging : True</span></span>

<span data-ttu-id="10bfe-250">KeepCallDetailForDays : 60</span><span class="sxs-lookup"><span data-stu-id="10bfe-250">KeepCallDetailForDays : 60</span></span>

<span data-ttu-id="10bfe-251">KeepErrorReportForDays : 60</span><span class="sxs-lookup"><span data-stu-id="10bfe-251">KeepErrorReportForDays : 60</span></span>

<span data-ttu-id="10bfe-252">PurgeHourOfDay : 2</span><span class="sxs-lookup"><span data-stu-id="10bfe-252">PurgeHourOfDay : 2</span></span>

<span data-ttu-id="10bfe-253">Des informations similaires peuvent être renvoyées pour la surveillance QoE en utilisant l’applet de requête Get-CsQoEConfiguration.</span><span class="sxs-lookup"><span data-stu-id="10bfe-253">Similar information can be returned for QoE monitoring by using the Get-CsQoEConfiguration cmdlet.</span></span> <span data-ttu-id="10bfe-254">Par exemple, cette commande renvoie des informations sur la collection globale de paramètres de configuration QoE :</span><span class="sxs-lookup"><span data-stu-id="10bfe-254">For example, this command returns information about the global collection of QoE configuration settings:</span></span>

`Get-QoEConfiguration -Identity "Global"`

<span data-ttu-id="10bfe-255">Cette information ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="10bfe-255">That information will resemble this:</span></span>

<span data-ttu-id="10bfe-256">Identity : global</span><span class="sxs-lookup"><span data-stu-id="10bfe-256">Identity : Global</span></span>

<span data-ttu-id="10bfe-257">ExternalConsumerIssuedCertId :</span><span class="sxs-lookup"><span data-stu-id="10bfe-257">ExternalConsumerIssuedCertId :</span></span>

<span data-ttu-id="10bfe-258">EnablePurging : true</span><span class="sxs-lookup"><span data-stu-id="10bfe-258">EnablePurging : True</span></span>

<span data-ttu-id="10bfe-259">KeepQoEDataForDays : 60</span><span class="sxs-lookup"><span data-stu-id="10bfe-259">KeepQoEDataForDays : 60</span></span>

<span data-ttu-id="10bfe-260">PurgeHourOfDay : 1</span><span class="sxs-lookup"><span data-stu-id="10bfe-260">PurgeHourOfDay : 1</span></span>

<span data-ttu-id="10bfe-261">EnableExternalConsumer : false</span><span class="sxs-lookup"><span data-stu-id="10bfe-261">EnableExternalConsumer : False</span></span>

<span data-ttu-id="10bfe-262">ExternalConsumerName :</span><span class="sxs-lookup"><span data-stu-id="10bfe-262">ExternalConsumerName :</span></span>

<span data-ttu-id="10bfe-263">ExternalConsumerURL :</span><span class="sxs-lookup"><span data-stu-id="10bfe-263">ExternalConsumerURL :</span></span>

<span data-ttu-id="10bfe-264">EnableQoE : true</span><span class="sxs-lookup"><span data-stu-id="10bfe-264">EnableQoE : True</span></span>

<span data-ttu-id="10bfe-265">Si vous souhaitez comparer vos paramètres de CDR actuels avec les paramètres CDR par défaut, les valeurs par défaut peuvent être examinées en exécutant la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="10bfe-265">If you want to compare your current CDR settings with the default CDR settings, the default values can be reviewed by running this command:</span></span>

`New-CsCdrConfiguration -Identity "Global" -InMemory`

<span data-ttu-id="10bfe-266">De même, les valeurs par défaut pour la surveillance QoE peuvent être récupérées à l’aide de la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="10bfe-266">Likewise, the default values for QoE monitoring can be retrieved by using this command:</span></span>

`New-CsQoEConfiguration -Identity "Global" -InMemory`

<span data-ttu-id="10bfe-267">Vous pouvez également renvoyer le nom de domaine complet de vos serveurs de surveillance en exécutant la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="10bfe-267">You can also return the FQDN of your Monitoring servers by running this command:</span></span>

`Get-CsService -MonitoringServer`

</div>

<div>

## <a name="check-voice-settings"></a><span data-ttu-id="10bfe-268">Vérifier les paramètres de la voix</span><span class="sxs-lookup"><span data-stu-id="10bfe-268">Check voice settings</span></span>

<span data-ttu-id="10bfe-269">Les paramètres vocaux sont généralement importants pour les administrateurs dans les politiques vocales et les itinéraires vocaux : les politiques vocales contiennent les paramètres qui déterminent les fonctionnalités exposées aux utilisateurs individuels (par exemple, la possibilité de transférer ou de transférer les appels), tandis que les itinéraires vocaux déterminent le routage des appels (et si) sur le RTC.</span><span class="sxs-lookup"><span data-stu-id="10bfe-269">The voice settings typically important to administrators are contained in voice policies and voice routes: voice policies contain the settings that determine the capabilities exposed to individual users (such as the ability to forward or transfer calls), while voice routes determine how (and if) calls are routed across the PSTN.</span></span>

<span data-ttu-id="10bfe-270">Les informations de la stratégie vocale peuvent être récupérées à l’aide de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="10bfe-270">Voice policy information can be retrieved by using Windows PowerShell.</span></span> <span data-ttu-id="10bfe-271">Par exemple, la commande suivante renvoie des informations sur la politique vocale globale :</span><span class="sxs-lookup"><span data-stu-id="10bfe-271">For example, this command returns information about the global voice policy:</span></span>

`Get-CsVoicePolicy -Identity "Global"`

<span data-ttu-id="10bfe-272">Cette commande renvoie des informations sur toutes les stratégies vocales configurées pour une utilisation au sein de l’Organisation :</span><span class="sxs-lookup"><span data-stu-id="10bfe-272">And this command returns information about all the voice policies configured for use in the organization:</span></span>

`Get-CsVoicePolicy`

<span data-ttu-id="10bfe-273">Les informations renvoyées par la cmdlet Get-CsVoicePolicy ressemble à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="10bfe-273">The information returned by the Get-CsVoicePolicy cmdlet resembles the following:</span></span>

<span data-ttu-id="10bfe-274">Identity : global</span><span class="sxs-lookup"><span data-stu-id="10bfe-274">Identity : Global</span></span>

<span data-ttu-id="10bfe-275">PstnUsages : {}</span><span class="sxs-lookup"><span data-stu-id="10bfe-275">PstnUsages : {}</span></span>

<span data-ttu-id="10bfe-276">Description</span><span class="sxs-lookup"><span data-stu-id="10bfe-276">Description :</span></span>

<span data-ttu-id="10bfe-277">AllowSimulRing : true</span><span class="sxs-lookup"><span data-stu-id="10bfe-277">AllowSimulRing : True</span></span>

<span data-ttu-id="10bfe-278">AllowCallForwarding : true</span><span class="sxs-lookup"><span data-stu-id="10bfe-278">AllowCallForwarding : True</span></span>

<span data-ttu-id="10bfe-279">AllowPSTNReRouting : true</span><span class="sxs-lookup"><span data-stu-id="10bfe-279">AllowPSTNReRouting : True</span></span>

<span data-ttu-id="10bfe-280">Nom : DefaultPolicy</span><span class="sxs-lookup"><span data-stu-id="10bfe-280">Name : DefaultPolicy</span></span>

<span data-ttu-id="10bfe-281">EnableDelegation : true</span><span class="sxs-lookup"><span data-stu-id="10bfe-281">EnableDelegation : True</span></span>

<span data-ttu-id="10bfe-282">EnableTeamCall : true</span><span class="sxs-lookup"><span data-stu-id="10bfe-282">EnableTeamCall : True</span></span>

<span data-ttu-id="10bfe-283">EnableCallTransfer : true</span><span class="sxs-lookup"><span data-stu-id="10bfe-283">EnableCallTransfer : True</span></span>

<span data-ttu-id="10bfe-284">EnableCallPark : false</span><span class="sxs-lookup"><span data-stu-id="10bfe-284">EnableCallPark : False</span></span>

<span data-ttu-id="10bfe-285">EnableMaliciousCallTracing : false</span><span class="sxs-lookup"><span data-stu-id="10bfe-285">EnableMaliciousCallTracing : False</span></span>

<span data-ttu-id="10bfe-286">EnableBWPolicyOverride : false</span><span class="sxs-lookup"><span data-stu-id="10bfe-286">EnableBWPolicyOverride : False</span></span>

<span data-ttu-id="10bfe-287">PreventPSTNTollBypass : false</span><span class="sxs-lookup"><span data-stu-id="10bfe-287">PreventPSTNTollBypass : False</span></span>

<span data-ttu-id="10bfe-288">Vous pouvez également créer des requêtes qui renvoient un sous-ensemble de vos stratégies vocales.</span><span class="sxs-lookup"><span data-stu-id="10bfe-288">You can also create queries that returned a subset of your voice policies.</span></span> <span data-ttu-id="10bfe-289">Par exemple, cette commande renvoie toutes les stratégies vocales qui autorisent le transfert d’appel :</span><span class="sxs-lookup"><span data-stu-id="10bfe-289">For example, this command returns all the voice policies that allow call forwarding:</span></span>

`Get-CsVoicePolicy | Where-Object {$_.AllowCallForwarding -eq $True}`

<span data-ttu-id="10bfe-290">Ainsi, cette commande renvoie toutes les stratégies vocales qui n’autorisent pas le transfert d’appel :</span><span class="sxs-lookup"><span data-stu-id="10bfe-290">And this command returns all the voice policies that don’t allow call forwarding:</span></span>

`Get-CsVoicePolicy | Where-Object {$_.AllowCallForwarding -eq $False}`

<span data-ttu-id="10bfe-291">Dans Windows PowerShell, utilisez l’applet de applet Get-CsVoiceRouting pour renvoyer des informations sur vos itinéraires vocaux :</span><span class="sxs-lookup"><span data-stu-id="10bfe-291">In Windows PowerShell, use the Get-CsVoiceRouting cmdlet to return information about your voice routes:</span></span>

`Get-CsVoiceRoute`

<span data-ttu-id="10bfe-292">Cette commande renvoie des informations telles que celle-ci pour tous les itinéraires vocaux :</span><span class="sxs-lookup"><span data-stu-id="10bfe-292">That command returns information such as this for all the voice routes:</span></span>

<span data-ttu-id="10bfe-293">Identité : LocalRoute</span><span class="sxs-lookup"><span data-stu-id="10bfe-293">Identity : LocalRoute</span></span>

<span data-ttu-id="10bfe-294">Priorité : 0</span><span class="sxs-lookup"><span data-stu-id="10bfe-294">Priority : 0</span></span>

<span data-ttu-id="10bfe-295">Description</span><span class="sxs-lookup"><span data-stu-id="10bfe-295">Description :</span></span>

<span data-ttu-id="10bfe-296">NumberPattern : ^ ( \\ + 1 \[ 0-9 \] {10} ) $</span><span class="sxs-lookup"><span data-stu-id="10bfe-296">NumberPattern : ^(\\+1\[0-9\]{10})$</span></span>

<span data-ttu-id="10bfe-297">PstnUsages : {}</span><span class="sxs-lookup"><span data-stu-id="10bfe-297">PstnUsages : {}</span></span>

<span data-ttu-id="10bfe-298">PstnGatewayList : {}</span><span class="sxs-lookup"><span data-stu-id="10bfe-298">PstnGatewayList : {}</span></span>

<span data-ttu-id="10bfe-299">Nom : LocalRoute</span><span class="sxs-lookup"><span data-stu-id="10bfe-299">Name : LocalRoute</span></span>

<span data-ttu-id="10bfe-300">SuppressCallerId :</span><span class="sxs-lookup"><span data-stu-id="10bfe-300">SuppressCallerId :</span></span>

<span data-ttu-id="10bfe-301">AlternateCallerId :</span><span class="sxs-lookup"><span data-stu-id="10bfe-301">AlternateCallerId :</span></span>

<span data-ttu-id="10bfe-302">Lync Server vous permet de créer des itinéraires vocaux sans utilisation PSTN et de ne spécifier aucune passerelle PSTN.</span><span class="sxs-lookup"><span data-stu-id="10bfe-302">Lync Server allows you to create voice routes that do not have a PSTN usage and do not specify a PSTN gateway.</span></span> <span data-ttu-id="10bfe-303">Toutefois, vous ne pouvez pas acheminer les appels sur un itinéraire vocal qui ne possède pas les deux valeurs de propriété configurées.</span><span class="sxs-lookup"><span data-stu-id="10bfe-303">However, you can't actually route calls over a voice route that does not have these two property values configured.</span></span> <span data-ttu-id="10bfe-304">Pour cette raison, il peut être utile d’exécuter cette commande de manière périodique, qui renvoie l’identité d’un itinéraire vocal sans utilisation RTC :</span><span class="sxs-lookup"><span data-stu-id="10bfe-304">Because of that, you might find it useful to periodically run this command, which returns the identity of any voice route that does not have a PSTN usage:</span></span>

`Get-CsVoiceRoute | Where-Object {$_.PstnUsages -eq $Null} | Select-Object Identity`

<span data-ttu-id="10bfe-305">De même, cette commande renvoie l’identité d’un itinéraire vocal qui n’a pas été configuré pour avoir une passerelle RTC :</span><span class="sxs-lookup"><span data-stu-id="10bfe-305">Similarly, this command returns the identity of any voice route that has not been configured to have a PSTN gateway:</span></span>

`Get-CsVoiceRoute | Where-Object {$_.PstnGatewayList -eq $Null}} | Select-Object Identity`

</div>

<div>

## <a name="check-conferencing-attendant-settings"></a><span data-ttu-id="10bfe-306">Vérifier les paramètres du surveillant de conférences</span><span class="sxs-lookup"><span data-stu-id="10bfe-306">Check Conferencing Attendant settings</span></span>

<span data-ttu-id="10bfe-307">Vérifiez les paramètres du surveillant de conférences pour la Conférence rendez-vous PSTN.</span><span class="sxs-lookup"><span data-stu-id="10bfe-307">Check conferencing Attendant settings for PSTN dial-in conferencing.</span></span> <span data-ttu-id="10bfe-308">Les paramètres du surveillant de conférences peuvent uniquement être récupérés à l’aide de l’applet de passe **Get-CsDialInConferencingConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="10bfe-308">Conferencing Attendant settings can only be retrieved by using the **Get-CsDialInConferencingConfiguration** cmdlet.</span></span> <span data-ttu-id="10bfe-309">Ces paramètres ne sont pas disponibles dans le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="10bfe-309">These settings are not available in the Lync Server Control Panel.</span></span> <span data-ttu-id="10bfe-310">Pour afficher les paramètres de votre surveillant de conférences, utilisez une commande Windows PowerShell semblable à la suivante qui renvoie la collection globale de paramètres du surveillant de conférences :</span><span class="sxs-lookup"><span data-stu-id="10bfe-310">To view your Conferencing Attendant settings, use a Windows PowerShell command similar to the following, which returns the global collection of Conferencing Attendant settings:</span></span>

`Get-CsDialInConferencingConfiguration -Identity "Global"`

<span data-ttu-id="10bfe-311">Notez que les paramètres du surveillant de conférences peuvent également être configurés sur l’étendue du site.</span><span class="sxs-lookup"><span data-stu-id="10bfe-311">Note that Conferencing Attendant settings can also be configured at the site scope.</span></span> <span data-ttu-id="10bfe-312">Pour renvoyer des informations sur tous les paramètres du surveillant de conférences, utilisez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="10bfe-312">To return information about all the Conferencing Attendant settings, use this command instead:</span></span>

`Get-CsDialInConferencingConfiguration`

<span data-ttu-id="10bfe-313">L’applet de requête Get-CsDialInConferencingConfiguration renvoie des données similaires à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="10bfe-313">The Get-CsDialInConferencingConfiguration cmdlet returns data similar to this:</span></span>

<span data-ttu-id="10bfe-314">Identity : global</span><span class="sxs-lookup"><span data-stu-id="10bfe-314">Identity : Global</span></span>

<span data-ttu-id="10bfe-315">EntryExitAnnouncementsType : UseNames</span><span class="sxs-lookup"><span data-stu-id="10bfe-315">EntryExitAnnouncementsType : UseNames</span></span>

<span data-ttu-id="10bfe-316">EnableNameRecording : true</span><span class="sxs-lookup"><span data-stu-id="10bfe-316">EnableNameRecording : True</span></span>

<span data-ttu-id="10bfe-317">EntryExitAnnouncementsEnabledByDefault : false</span><span class="sxs-lookup"><span data-stu-id="10bfe-317">EntryExitAnnouncementsEnabledByDefault : False</span></span>

<span data-ttu-id="10bfe-318">Si EntryExitAnnouncementsEnabledByDefault est défini sur false, cela signifie que les annonces de conférences sont désactivées.</span><span class="sxs-lookup"><span data-stu-id="10bfe-318">If EntryExitAnnouncementsEnabledByDefault is set to False, that means the conferencing announcements are disabled.</span></span> <span data-ttu-id="10bfe-319">Pour activer les annonces d’entrée et de sortie, exécutez une commande Windows PowerShell semblable à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="10bfe-319">To enable entry and exit announcements, run a Windows PowerShell command similar to this:</span></span>

`Set-CsDialInConferencingConfiguration -Identity "Global" -EntryExitAnnouncementsEnabledByDefault $True`

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="10bfe-320">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="10bfe-320">See Also</span></span>


[<span data-ttu-id="10bfe-321">Get-CsSipDomain</span><span class="sxs-lookup"><span data-stu-id="10bfe-321">Get-CsSipDomain</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsSipDomain)  
[<span data-ttu-id="10bfe-322">Get-CsMeetingConfiguration</span><span class="sxs-lookup"><span data-stu-id="10bfe-322">Get-CsMeetingConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsMeetingConfiguration)  
[<span data-ttu-id="10bfe-323">Get-CsService</span><span class="sxs-lookup"><span data-stu-id="10bfe-323">Get-CsService</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsService)  
[<span data-ttu-id="10bfe-324">Get-CsAccessEdgeConfiguration</span><span class="sxs-lookup"><span data-stu-id="10bfe-324">Get-CsAccessEdgeConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsAccessEdgeConfiguration)  
[<span data-ttu-id="10bfe-325">Get-CsExternalAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="10bfe-325">Get-CsExternalAccessPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsExternalAccessPolicy)  
[<span data-ttu-id="10bfe-326">Get-CsArchivingConfiguration</span><span class="sxs-lookup"><span data-stu-id="10bfe-326">Get-CsArchivingConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsArchivingConfiguration)  
[<span data-ttu-id="10bfe-327">Get-CsCdrConfiguration</span><span class="sxs-lookup"><span data-stu-id="10bfe-327">Get-CsCdrConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsCdrConfiguration)  
[<span data-ttu-id="10bfe-328">Get-CsQoEConfiguration</span><span class="sxs-lookup"><span data-stu-id="10bfe-328">Get-CsQoEConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsQoEConfiguration)  
[<span data-ttu-id="10bfe-329">Get-CsVoicePolicy</span><span class="sxs-lookup"><span data-stu-id="10bfe-329">Get-CsVoicePolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsVoicePolicy)  
[<span data-ttu-id="10bfe-330">Get-CsVoiceRoute</span><span class="sxs-lookup"><span data-stu-id="10bfe-330">Get-CsVoiceRoute</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsVoiceRoute)  
[<span data-ttu-id="10bfe-331">Get-CsDialInConferencingConfiguration</span><span class="sxs-lookup"><span data-stu-id="10bfe-331">Get-CsDialInConferencingConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsDialInConferencingConfiguration)  
  

<span data-ttu-id="10bfe-332"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="10bfe-332"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

