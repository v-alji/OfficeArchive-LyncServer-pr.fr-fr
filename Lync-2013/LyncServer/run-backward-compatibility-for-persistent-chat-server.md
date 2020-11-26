---
title: Exécution de compatibilité descendante pour la conversation permanente
description: Exécutez la compatibilité descendante pour le serveur de chat permanent.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Run backward compatibility for Persistent Chat Server
ms:assetid: 53f1a706-3104-4a94-8b4e-8badd9a066d6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204901(v=OCS.15)
ms:contentKeyID: 48184175
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b0486992d44e6385559d3e9df9f9ffc2125120da
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423378"
---
# <a name="run-backward-compatibility-for-persistent-chat-server"></a><span data-ttu-id="f2018-103">Exécution de compatibilité descendante pour la conversation permanente</span><span class="sxs-lookup"><span data-stu-id="f2018-103">Run backward compatibility for Persistent Chat Server</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f2018-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f2018-104">

<span> </span></span></span>

<span data-ttu-id="f2018-105">_**Dernière modification de la rubrique :** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="f2018-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="f2018-106">Le point de terminaison Lync Server 2013, le point de terminaison serveur Chat permanent fournit un moyen de créer une URL simple qui pointe vers un pool de serveurs de chat permanent.</span><span class="sxs-lookup"><span data-stu-id="f2018-106">The Lync Server 2013, Persistent Chat Server endpoint provides a way to create a simple URL that points to a Persistent Chat Server pool.</span></span> <span data-ttu-id="f2018-107">Cette fonctionnalité est utile pour les clients hérités (serveur de conversation de groupe Microsoft Office Communications Server 2007 R2 ou Lync Server 2010, discussion de groupe), car les utilisateurs peuvent entrer une URL simple dans la configuration manuelle lors d’une tentative de pointage sur un ordinateur exécutant Lync 2013, conversation persistante.</span><span class="sxs-lookup"><span data-stu-id="f2018-107">This is useful for legacy clients (Microsoft Office Communications Server 2007 R2 Group Chat Server or Lync Server 2010, Group Chat) because users can enter a simple URL in the manual configuration when trying to point the legacy client to a computer running Lync 2013, Persistent Chat.</span></span> <span data-ttu-id="f2018-108">Ce point de terminaison n’est pas utilisé par chat permanent et est requis uniquement pour les clients hérités.</span><span class="sxs-lookup"><span data-stu-id="f2018-108">This endpoint isn’t used by Persistent Chat, and is required for legacy clients only.</span></span> <span data-ttu-id="f2018-109">Cela est utile pour la période intermédiaire où les salles peuvent être migrées, mais les clients 2013 Lync n’ont pas été déployés au sein de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="f2018-109">This is useful for the interim period where rooms may be migrated, but the Lync 2013 clients have not been deployed throughout the organization.</span></span> <span data-ttu-id="f2018-110">Les utilisateurs exécutant une discussion de groupe Lync 2010 (client) peuvent toujours se connecter au serveur principal de chat serveur.</span><span class="sxs-lookup"><span data-stu-id="f2018-110">Users running Lync 2010 Group Chat (client) can then still connect to the Persistent Chat Server Back End Server.</span></span>

<span data-ttu-id="f2018-111">Vous n’avez pas besoin de créer plusieurs points de terminaison serveur de chat permanent ; vous avez simplement besoin d’une seule liste de serveurs de chat permanent.</span><span class="sxs-lookup"><span data-stu-id="f2018-111">You don’t need to create multiple Persistent Chat Server endpoints; you just need one for each Persistent Chat Server pool.</span></span> <span data-ttu-id="f2018-112">Les administrateurs peuvent créer plusieurs points de terminaison (un par liste), mais les clients hérités peuvent être configurés pour se connecter à un seul pool à la fois.</span><span class="sxs-lookup"><span data-stu-id="f2018-112">Administrators can create multiple endpoints (one per pool), but legacy clients can be configured to connect to only one pool at a time.</span></span> <span data-ttu-id="f2018-113">Dans le scénario classique ou standard, le déploiement hérité est un seul pool.</span><span class="sxs-lookup"><span data-stu-id="f2018-113">In the usual or mainstream scenario, the legacy deployment is one pool only.</span></span> <span data-ttu-id="f2018-114">Un nouveau déploiement migre généralement ce pool vers un nouveau serveur Lync Server 2013 et peut ajouter de nouveaux pools de serveurs de chat permanent supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="f2018-114">A new deployment generally migrates that pool to a new Lync Server 2013 and might add some new additional Persistent Chat Server pools.</span></span>

<span data-ttu-id="f2018-115">Ce scénario standard suit généralement ce modèle :</span><span class="sxs-lookup"><span data-stu-id="f2018-115">This mainstream scenario generally follows this pattern:</span></span>

  - <span data-ttu-id="f2018-116">Pour administrer les utilisateurs dotés d’un serveur Lync Server 2010, d’une liste de discussion de groupe et de vos clients de discussion de groupe Lync 2010, vous devez vous connecter à ce pool en utilisant certains utilisateurs bien connus (par défaut, SIP : ocschat@ \<domainName\> . com ou similaire).</span><span class="sxs-lookup"><span data-stu-id="f2018-116">You administer users with one Lync Server 2010, Group Chat pool, and your Lync 2010 Group Chat clients connect to that pool by using some well-known user (either default sip:ocschat@\<domainName\>.com, or a similar one).</span></span> <span data-ttu-id="f2018-117">Les utilisateurs utilisent les services de domaine Active Directory SIP et le service de recherche s’inscrit avec eux pour recevoir les demandes entrantes.</span><span class="sxs-lookup"><span data-stu-id="f2018-117">The users are SIP-enabled Active Directory Domain Services, and the Lookup service registers with them to receive incoming requests.</span></span>

  - <span data-ttu-id="f2018-118">Par la suite, vous installez un serveur de chat permanent Lync Server 2013 et un pool de serveurs de chat permanent.</span><span class="sxs-lookup"><span data-stu-id="f2018-118">Subsequently, you install a Lync Server 2013 Persistent Chat Server and Persistent Chat Server pool.</span></span>

  - <span data-ttu-id="f2018-119">Lorsque les utilisateurs sont généralement hors ligne (par exemple, un week-end) :</span><span class="sxs-lookup"><span data-stu-id="f2018-119">During a time when users are generally offline (for example, a weekend):</span></span>
    
      - <span data-ttu-id="f2018-120">Désactivez Lync Server 2010, discussion de groupe.</span><span class="sxs-lookup"><span data-stu-id="f2018-120">Turn off Lync Server 2010, Group Chat.</span></span>
    
      - <span data-ttu-id="f2018-121">Migrer les données de Lync Server 2010, pool de discussion de groupe vers le pool de serveurs Lync Server 2013 persistent.</span><span class="sxs-lookup"><span data-stu-id="f2018-121">Migrate data from the Lync Server 2010, Group Chat pool to the Lync Server 2013 Persistent Chat Server pool.</span></span>
    
      - <span data-ttu-id="f2018-122">Supprimez l’utilisateur connu des services de domaine Active Directory (AD FS).</span><span class="sxs-lookup"><span data-stu-id="f2018-122">Delete the well-known user from the Active Directory Domain Services.</span></span>
    
      - <span data-ttu-id="f2018-123">Créer un *point de terminaison hérité* avec le même URI SIP que l’utilisateur connu précédemment supprimé.</span><span class="sxs-lookup"><span data-stu-id="f2018-123">Create a new *legacy endpoint* with the same SIP URI as the previously deleted well-known user.</span></span>
    
      - <span data-ttu-id="f2018-124">Démarrez Lync Server 2013, serveurs de chat permanent.</span><span class="sxs-lookup"><span data-stu-id="f2018-124">Start the Lync Server 2013, Persistent Chat Servers.</span></span>

  - <span data-ttu-id="f2018-125">Les utilisateurs se connectent de nouveau en utilisant leur discussion de groupe Lync 2010 et se connectent à leurs données sans avoir besoin de modifier une configuration.</span><span class="sxs-lookup"><span data-stu-id="f2018-125">Users log back on by using their Lync 2010 Group Chat (client) and connect to their data without needing to change any configuration.</span></span>

  - <span data-ttu-id="f2018-126">Par la suite, vous pouvez désactiver la mise à niveau de Lync Server 2010, discussion de groupe.</span><span class="sxs-lookup"><span data-stu-id="f2018-126">At a later time, you can decommission the Lync Server 2010, Group Chat.</span></span> <span data-ttu-id="f2018-127">Par la suite, vous pouvez déployer Lync Server 2013, le serveur de chat permanent et installer de nouveaux pools de serveurs Lync Server 2013 permanents.</span><span class="sxs-lookup"><span data-stu-id="f2018-127">Subsequently, you can deploy Lync Server 2013, Persistent Chat Server, and install new Lync Server 2013 Persistent Chat Server pools.</span></span>

<span data-ttu-id="f2018-128">Pour plus d’informations sur la migration de Lync Server 2010, la discussion de groupe vers Lync Server 2013, le serveur de chat permanent, voir [migration de Lync server 2010, discussion de groupe ou conversation de groupe Microsoft Office Communications Server 2007 R2 vers Lync server 2013, serveur de chat permanent](migration-from-lync-server-2010-group-chat-or-office-communications-server-2007-r2-group-chat-to-lync-server-2013-persistent-chat-server.md).</span><span class="sxs-lookup"><span data-stu-id="f2018-128">For details about migrating from Lync Server 2010, Group Chat to Lync Server 2013, Persistent Chat Server, see [Migration from Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat to Lync Server 2013, Persistent Chat Server](migration-from-lync-server-2010-group-chat-or-office-communications-server-2007-r2-group-chat-to-lync-server-2013-persistent-chat-server.md).</span></span>

<span data-ttu-id="f2018-129">Pour procéder à la compatibilité descendante (pour créer un point de terminaison serveur Chat permanent qui pointe vers un pool de serveurs de chat permanent, qui peut être utilisé par les clients de pool de discussion de groupe existants) :</span><span class="sxs-lookup"><span data-stu-id="f2018-129">To run backward compatibility (to create a Persistent Chat Server endpoint that points to a Persistent Chat Server pool, which can be used by legacy Group Chat pool clients):</span></span>

    New-CsPersistentChatEndpoint -SipAddress <CO name, ex. persistentchat@contoso.com> -PersistentChatPoolFqdn <pool FQDN, like pcpool.contoso.com>

<span data-ttu-id="f2018-130">Ensuite, configurez les clients de chat permanent pour qu’ils utilisent cette adresse SIP comme objet de contact.</span><span class="sxs-lookup"><span data-stu-id="f2018-130">Next, configure Persistent Chat clients to use that SIP address as their contact object.</span></span> <span data-ttu-id="f2018-131">L’adresse SIP est créée à l’aide de l’applet de nouvelle applet de **CsPersistentChatEndpoint** pour un pool de serveurs de chat permanent spécifique.</span><span class="sxs-lookup"><span data-stu-id="f2018-131">The SIP address is created with the **New-CsPersistentChatEndpoint** cmdlet for a specific Persistent Chat Server pool.</span></span>

<span data-ttu-id="f2018-132">Pour ajouter le point de terminaison serveur Chat permanent à l’aide de l’interface de ligne de commande Windows PowerShell, considérez l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="f2018-132">To add the Persistent Chat Server endpoint by using Windows PowerShell command-line interface, consider the following example.</span></span> <span data-ttu-id="f2018-133">Dans le cas présent, vous configurez l’objet contact pour qu’il soit nommé « persistentchat » sur la topologie « contoso.com », où le nom de domaine complet (FQDN) du pool est « pcpool.contoso.com » :</span><span class="sxs-lookup"><span data-stu-id="f2018-133">In this case, you are configuring the contact object to be named "persistentchat" on the "contoso.com" topology, where the pool fully qualified domain name (FQDN) is "pcpool.contoso.com":</span></span>

    New-CsPersistentChatEndpoint -SipAddress sip:persistentchat@contoso.com -PersistentChatPoolFqdn pcpool.contoso.com

<div>

## <a name="see-also"></a><span data-ttu-id="f2018-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2018-134">See Also</span></span>


[<span data-ttu-id="f2018-135">Migration de Lync Server 2010, conversation de groupe ou de la conversation de groupe Office Communications Server 2007 R2 vers Lync Server 2013, serveur de conversation permanente</span><span class="sxs-lookup"><span data-stu-id="f2018-135">Migration from Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat to Lync Server 2013, Persistent Chat Server</span></span>](migration-from-lync-server-2010-group-chat-or-office-communications-server-2007-r2-group-chat-to-lync-server-2013-persistent-chat-server.md)  
  

<span data-ttu-id="f2018-136"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f2018-136"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

