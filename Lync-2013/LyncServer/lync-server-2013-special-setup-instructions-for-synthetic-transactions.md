---
title: 'Lync Server 2013 : instructions de configuration spéciales pour les transactions synthétiques'
description: 'Lync Server 2013 : instructions de configuration spéciales pour les transactions synthétiques.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Special setup instructions for synthetic transactions
ms:assetid: 694cbe05-5dba-4035-a01c-c87ebfb0478b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688080(v=OCS.15)
ms:contentKeyID: 49733676
ms.date: 11/16/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7e288a9d7f15f4b84df591d152a912509c77129a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441598"
---
# <a name="special-setup-instructions-for-synthetic-transactions-in-lync-server-2013"></a><span data-ttu-id="abd98-103">Instructions de configuration spéciales pour les transactions synthétiques dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="abd98-103">Special setup instructions for synthetic transactions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="abd98-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="abd98-104">

<span> </span></span></span>

<span data-ttu-id="abd98-105">_**Dernière modification de la rubrique :** 2015-11-16_</span><span class="sxs-lookup"><span data-stu-id="abd98-105">_**Topic Last Modified:** 2015-11-16_</span></span>

<span data-ttu-id="abd98-106">La plupart des transactions synthétiques peuvent s’exécuter sur un nœud d’observation en l’aspect ; autrement dit, dès que la transaction synthétique a été ajoutée aux paramètres de configuration du nœud d’observation, le nœud d’observation peut commencer à utiliser la transaction synthétique lors de ses tests.</span><span class="sxs-lookup"><span data-stu-id="abd98-106">Most synthetic transactions can run on a watcher node as-is; that is, as soon as the synthetic transaction has been added to the watcher node configuration settings, the watcher node can begin using the synthetic transaction during its test passes.</span></span> <span data-ttu-id="abd98-107">Toutefois, ce n’est pas vrai pour toutes les transactions synthétiques.</span><span class="sxs-lookup"><span data-stu-id="abd98-107">However, this is not true for all synthetic transactions.</span></span> <span data-ttu-id="abd98-108">Les exceptions (transactions synthétiques qui nécessitent des instructions de configuration spéciales) sont décrites dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="abd98-108">The exceptions—synthetic transactions that require special setup instructions—are discussed in the following sections.</span></span>

<div>

## <a name="dealing-with-server-timeout-errors"></a><span data-ttu-id="abd98-109">Gestion des erreurs de temporisation du serveur</span><span class="sxs-lookup"><span data-stu-id="abd98-109">Dealing With Server Timeout Errors</span></span>

<span data-ttu-id="abd98-110">Dans certains cas, il est possible que vous rencontriez des erreurs de temporisation serveur (code d’erreur 504).</span><span class="sxs-lookup"><span data-stu-id="abd98-110">In some cases you might find that your synthetic transactions are failing with server timeout errors (error code 504).</span></span> <span data-ttu-id="abd98-111">Ces erreurs se produisent généralement en raison de problèmes de pare-feu.</span><span class="sxs-lookup"><span data-stu-id="abd98-111">These errors are typically due to firewall problems.</span></span> <span data-ttu-id="abd98-112">Lors de l’exécution d’une transaction synthétique, cette transaction s’exécute sous le processus MonitoringHost.exe. à son tour, MonitoringHost.exe démarre une instance du processus de PowerShell.exe.</span><span class="sxs-lookup"><span data-stu-id="abd98-112">When a synthetic transaction is executed, that transaction runs under the MonitoringHost.exe process; in turn, MonitoringHost.exe starts an instance of the PowerShell.exe process.</span></span> <span data-ttu-id="abd98-113">Si MonitoringHost.exe ou PowerShell.exe est bloqué par votre pare-feu, la transaction synthétique échoue et génère une erreur 504.</span><span class="sxs-lookup"><span data-stu-id="abd98-113">If either MonitoringHost.exe or PowerShell.exe is blocked by your firewall then the synthetic transaction will fail and will generate a 504 error.</span></span>

<span data-ttu-id="abd98-114">Pour résoudre ce problème, vous devez créer manuellement des règles de pare-feu entrant pour MonitoringHost.exe et PowerShell.exe sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="abd98-114">To resolve this issue, you should manually create inbound firewall rules for both MonitoringHost.exe and PowerShell.exe on the local machine.</span></span> <span data-ttu-id="abd98-115">Cette opération peut être réalisée via un pare-feu Windows ou un logiciel de pare-feu local tiers, en fonction de la configuration préexistante de votre serveur.</span><span class="sxs-lookup"><span data-stu-id="abd98-115">This can be done via Windows firewall or a third-party local firewall software, depending on your server's preexisting configuration.</span></span>

<span data-ttu-id="abd98-116">Si vous utilisez un pare-feu réseau entre l’ordinateur hôte de transactions synthétiques et les serveurs Lync que vous tentez de surveiller, vous devez traiter l’hôte en tant qu’ordinateur client et observer toutes les exigences de port de pare-feu des [ports et protocoles pour les serveurs internes dans Lync Server 2013](lync-server-2013-ports-and-protocols-for-internal-servers.md).</span><span class="sxs-lookup"><span data-stu-id="abd98-116">If you're employing a network firewall device between the synthetic transaction host machine and the Lync Servers you're attempting to monitor, you should treat the host as a client machine, and observer all firewall port requirements from [Ports and protocols for internal servers in Lync Server 2013](lync-server-2013-ports-and-protocols-for-internal-servers.md).</span></span>

</div>

<div>

## <a name="data-conferencing-synthetic-transactions"></a><span data-ttu-id="abd98-117">Transactions synthétiques de conférence de données</span><span class="sxs-lookup"><span data-stu-id="abd98-117">Data Conferencing Synthetic Transactions</span></span>

<span data-ttu-id="abd98-118">Si votre ordinateur de nœud d’observateur se trouve en dehors de votre réseau de périmètre, vous ne pourrez probablement pas exécuter la transaction synthétique de conférence de données, sauf si vous désactivez d’abord les paramètres de proxy d’Internet Explorer pour le compte de service réseau.</span><span class="sxs-lookup"><span data-stu-id="abd98-118">If your watcher node computer is located outside your perimeter network, you will probably not be able to run the Data Conferencing Synthetic Transaction unless you first disable the Internet Explorer proxy settings for the Network Service account.</span></span> <span data-ttu-id="abd98-119">Pour désactiver les paramètres de proxy pour ce service, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="abd98-119">To disable the proxy settings for this service, complete the following procedure:</span></span>

1.  <span data-ttu-id="abd98-120">Sur l’ordinateur du nœud d’observation, cliquez sur **Démarrer**, sur **tous les programmes**, sur **accessoires**, cliquez avec le bouton droit sur **invite de commandes**, puis cliquez sur **exécuter en tant qu’administrateur**.</span><span class="sxs-lookup"><span data-stu-id="abd98-120">On the watcher node computer, click **Start**, click **All Programs**, click **Accessories**, right-click **Command Prompt**, and then click **Run as administrator**.</span></span>

2.  <span data-ttu-id="abd98-121">Dans la fenêtre de la console, tapez la commande suivante, puis appuyez sur entrée :</span><span class="sxs-lookup"><span data-stu-id="abd98-121">In the console window, type the following command and then press ENTER:</span></span>
    
        bitsadmin /util /SetIEProxy NetworkService NO_PROXY

<span data-ttu-id="abd98-122">Le message suivant s’affiche dans la fenêtre de commande :</span><span class="sxs-lookup"><span data-stu-id="abd98-122">The following message will appear in the command window:</span></span>

    BITSAdmin is deprecated and is not guaranteed to be available in future versions of Windows. Administration tools for the BITS service are now provided by BITS PowerShell cmdlets.
    
    Internet proxy settings for account NetworkService set to NO_PROXY. 
    (connection = default)

<span data-ttu-id="abd98-123">Ce message signifie que vous avez désactivé les paramètres de proxy d’Internet Explorer pour le compte de service réseau.</span><span class="sxs-lookup"><span data-stu-id="abd98-123">This message means that you have disabled the Internet Explorer proxy settings for the Network Service account.</span></span>

</div>

<div>

## <a name="exchange-unified-messaging-synthetic-transactions"></a><span data-ttu-id="abd98-124">Transactions synthétiques de la messagerie unifiée Exchange</span><span class="sxs-lookup"><span data-stu-id="abd98-124">Exchange Unified Messaging Synthetic Transactions</span></span>

<span data-ttu-id="abd98-125">La transaction synthétique de la messagerie unifiée Exchange vérifie que les utilisateurs test peuvent se connecter à des comptes de messagerie vocale hébergés dans Exchange.</span><span class="sxs-lookup"><span data-stu-id="abd98-125">The Exchange Unified Messaging (UM) synthetic transaction verifies that test users can connect to voicemail accounts homed in Exchange.</span></span> <span data-ttu-id="abd98-126">Ces utilisateurs doivent être préconfigurés avec des comptes de messagerie vocale pour pouvoir utiliser les tests de MU Exchange.</span><span class="sxs-lookup"><span data-stu-id="abd98-126">These test users will need to be preconfigured with voicemail accounts before they can use the Exchange UM tests.</span></span>

</div>

<div>

## <a name="persistent-chat-synthetic-transactions"></a><span data-ttu-id="abd98-127">Transactions synthétiques de conversation permanente</span><span class="sxs-lookup"><span data-stu-id="abd98-127">Persistent Chat Synthetic Transactions</span></span>

<span data-ttu-id="abd98-128">Pour utiliser la transaction synthétique des conversations permanentes, les administrateurs doivent d’abord créer un canal et donner aux utilisateurs du test l’autorisation d’utiliser ce dernier.</span><span class="sxs-lookup"><span data-stu-id="abd98-128">To use the Persistent Chat synthetic transaction, administrators must first create a channel and give the test users permissions to use it.</span></span> <span data-ttu-id="abd98-129">L’applet de [contrôle test-CsPersistentChatMessage](https://docs.microsoft.com/powershell/module/skype/Test-CsPersistentChatMessage) peut être utilisée pour configurer correctement ces utilisateurs de test :</span><span class="sxs-lookup"><span data-stu-id="abd98-129">The [Test-CsPersistentChatMessage](https://docs.microsoft.com/powershell/module/skype/Test-CsPersistentChatMessage) cmdlet can be used to properly configure these test users:</span></span>

    $cred1 = Get-Credential "litwareinc\kenmyer"
    $cred2 = Get-Credential "litwareinc\pilar"
    
    Test-CsPersistentChatMessage -TargetFqdn atl-cs-001.litwareinc.com -SenderSipAddress sip:kenmyer@litwareinc.com -SenderCredential $cred1 -ReceiverSipAddress sip:pilar@litwareinc.com -ReceiverCredential $cred2 -TestUser1SipAddress sip:kenmyer@litwareinc.com -TestUser2SipAddress sip:pilar@litwareinc.com -Setup $True

<span data-ttu-id="abd98-130">Cette tâche de configuration doit être exécutée au sein de l’entreprise :</span><span class="sxs-lookup"><span data-stu-id="abd98-130">This setup task must be run from inside the enterprise:</span></span>

  - <span data-ttu-id="abd98-131">S’il est exécuté à partir d’un ordinateur qui n’est pas serveur, l’utilisateur qui exécute l’applet de commande doit être membre du rôle PersistentChatAdministrators pour le contrôle Role-Based d’accès (RBAC).</span><span class="sxs-lookup"><span data-stu-id="abd98-131">If run from a nonserver machine, the user who runs the cmdlet must be a member of the PersistentChatAdministrators role for Role-Based Access Control (RBAC).</span></span>

  - <span data-ttu-id="abd98-132">S’il est exécuté sur le serveur lui-même, l’utilisateur qui exécute l’applet de contrôle doit être membre du groupe RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="abd98-132">If run from the server itself, the user who runs the cmdlet should be a member of the RTCUniversalServerAdmins group.</span></span>

<span data-ttu-id="abd98-133">Dans la commande précédente, le paramètre d’installation était inclus et défini sur true ($True).</span><span class="sxs-lookup"><span data-stu-id="abd98-133">In the preceding command, the Setup parameter was included and set to True ($True).</span></span> <span data-ttu-id="abd98-134">Si vous incluez le paramètre Setup, Test-CsPersistentChatMessage créer une salle de conversation persistante spéciale et remplir cette salle avec les utilisateurs test.</span><span class="sxs-lookup"><span data-stu-id="abd98-134">If you include the Setup parameter, Test-CsPersistentChatMessage will create a special Persistent Chat room and populate that room with the test users.</span></span> <span data-ttu-id="abd98-135">Cela permet de s’assurer qu’une salle de conversation est réellement disponible aux fins de test.</span><span class="sxs-lookup"><span data-stu-id="abd98-135">This helps to ensure that there is actually a chat room available for testing purposes.</span></span> <span data-ttu-id="abd98-136">Notez que le paramètre d’installation ne doit être exécuté qu’à partir d’un serveur frontal.</span><span class="sxs-lookup"><span data-stu-id="abd98-136">Note that the Setup parameter should be run only from a Front End Server.</span></span>

<span data-ttu-id="abd98-137">La salle de conversation créée par Test-CsPersistentChatMessage peut être supprimée uniquement par un administrateur.</span><span class="sxs-lookup"><span data-stu-id="abd98-137">The chat room that is created by Test-CsPersistentChatMessage can be deleted only by an administrator.</span></span>

</div>

<div>

## <a name="pstn-peer-to-peer-call-synthetic-transactions"></a><span data-ttu-id="abd98-138">Transactions synthétiques d’appels d’égal à égal RTC</span><span class="sxs-lookup"><span data-stu-id="abd98-138">PSTN Peer-to-Peer Call Synthetic Transactions</span></span>

<span data-ttu-id="abd98-139">La transaction synthétique [test-CsPstnPeerToPeerCall](https://docs.microsoft.com/powershell/module/skype/Test-CsPstnPeerToPeerCall) vérifie la possibilité de passer et de recevoir des appels par le biais du réseau téléphonique public commuté (RTC).</span><span class="sxs-lookup"><span data-stu-id="abd98-139">The [Test-CsPstnPeerToPeerCall](https://docs.microsoft.com/powershell/module/skype/Test-CsPstnPeerToPeerCall) synthetic transaction verifies the ability to place and receive calls via the public switched telephone network (PSTN).</span></span>

<span data-ttu-id="abd98-140">Pour exécuter cette transaction synthétique, les administrateurs doivent configurer les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="abd98-140">To run this synthetic transaction, administrators must configure:</span></span>

  - <span data-ttu-id="abd98-141">Deux utilisateurs de test (un appelant et un destinataire) activés pour voix entreprise.</span><span class="sxs-lookup"><span data-stu-id="abd98-141">Two test users (a caller and a receiver) enabled for Enterprise Voice.</span></span>

  - <span data-ttu-id="abd98-142">Numéros de sélection directe à l’arrivée (SDA) pour chaque compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="abd98-142">Direct Inward Dialing (DID) numbers for each user account.</span></span>

  - <span data-ttu-id="abd98-143">Politiques vocales et itinéraires vocaux permettant d’appeler le numéro du destinataire pour joindre la passerelle PSTN.</span><span class="sxs-lookup"><span data-stu-id="abd98-143">Voice policies and voice routes that enable calls to the receiver’s number to reach the PSTN gateway.</span></span>

  - <span data-ttu-id="abd98-144">Passerelle RTC qui accepte les appels et les éléments multimédias qui acheminent les appels vers les appels vers le pool d’hébergement d’un destinataire en fonction du numéro composé.</span><span class="sxs-lookup"><span data-stu-id="abd98-144">A PSTN gateway that accepts calls, and media that route calls backs to a receiver’s home pool based on the number dialed.</span></span>

</div>

<div>

## <a name="unified-contact-store-synthetic-transactions"></a><span data-ttu-id="abd98-145">Transactions synthétiques du magasin de contacts unifié</span><span class="sxs-lookup"><span data-stu-id="abd98-145">Unified Contact Store Synthetic Transactions</span></span>

<span data-ttu-id="abd98-146">La transaction synthétique du magasin de contacts unifié vérifie que Lync Server 2013 est en mesure de récupérer des contacts de la part d’un utilisateur à partir de Microsoft Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="abd98-146">The Unified Contact Store synthetic transaction verifies that Lync Server 2013 is able to retrieve contacts on behalf of a user from Microsoft Exchange Server 2013.</span></span>

<span data-ttu-id="abd98-147">Pour utiliser cette transaction synthétique, les conditions suivantes doivent être remplies :</span><span class="sxs-lookup"><span data-stu-id="abd98-147">To use this synthetic transaction, the following conditions must be met:</span></span>

  - <span data-ttu-id="abd98-148">La [gestion de l’authentification de serveur à serveur (OAuth) et des applications partenaires dans Lync server 2013](lync-server-2013-managing-server-to-server-authentication-oauth-and-partner-applications.md) doivent être configurées entre lync Server 2013 et Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="abd98-148">[Managing server-to-server authentication (OAuth) and partner applications in Lync Server 2013](lync-server-2013-managing-server-to-server-authentication-oauth-and-partner-applications.md) must be configured between Lync Server 2013 and Exchange 2013.</span></span>

  - <span data-ttu-id="abd98-149">Les utilisateurs test doivent avoir une boîte aux lettres Exchange 2013 valide.</span><span class="sxs-lookup"><span data-stu-id="abd98-149">Test users must have a valid Exchange 2013 mailbox.</span></span>

<span data-ttu-id="abd98-150">Une fois ces conditions satisfaites, les administrateurs peuvent exécuter la commande suivante pour vérifier que l’utilisateur possédant l’adresse kenmyer@litwareinc.com peut récupérer ses contacts auprès du magasin de contacts unifié :</span><span class="sxs-lookup"><span data-stu-id="abd98-150">After these conditions are met, administrators can run the following command to verify that the user with the SIP address kenmyer@litwareinc.com can retrieve his contacts from the unified contact store:</span></span>

    Test-CsUnifiedContactStore -TargetFqdn atl-cs-001.litwareinc.com -UserSipAddress "sip:kenmyer@litwareinc.com" -RegistrarPort 5061 -Authentication TrustedServer -Setup

<span data-ttu-id="abd98-151">Notez l’utilisation du paramètre Setup utilisé dans la commande précédente.</span><span class="sxs-lookup"><span data-stu-id="abd98-151">Note the use of the Setup parameter used in the preceding command.</span></span> <span data-ttu-id="abd98-152">Si le paramètre Setup est inclus lors de l’exécution d' Test-CsUnifiedContactStore, les contacts de l’utilisateur spécifié (dans ce cas, sip :kenmyer@litwareinc.com) seront déplacés vers le magasin de contacts unifié.</span><span class="sxs-lookup"><span data-stu-id="abd98-152">If the Setup parameter is included when running Test-CsUnifiedContactStore then the specified user’s contacts (in this case, sip:kenmyer@litwareinc.com) will be moved to the unified contact store.</span></span> <span data-ttu-id="abd98-153">(Bien entendu, si le contact de l’utilisateur se trouve déjà dans le magasin de contacts unifié, il n’est pas nécessaire de le déplacer.) Le paramètre Setup est généralement utilisé une seule fois (la première fois Test-CsUnifiedContactStore est exécutée) et ne doit être utilisée qu’avec les utilisateurs test. c’est-à-dire, avec les comptes d’utilisateurs qui ne seront jamais enregistrés sur Lync Server.</span><span class="sxs-lookup"><span data-stu-id="abd98-153">(Of course, if the user’s contacts are already in the Unified Contact Store then they do not have to be moved.) The Setup parameter is typically used only one time (the first time Test-CsUnifiedContactStore is executed), and should only be used with test users; that is, with user accounts that will never actually be logged on to Lync Server.</span></span> <span data-ttu-id="abd98-154">Une fois que l’utilisateur a migré vers le magasin de contacts unifié, vous pouvez vérifier que les contacts de l’utilisateur peuvent être récupérés en appelant Test-CsUnifiedContactStore sans définir le paramètre d’installation :</span><span class="sxs-lookup"><span data-stu-id="abd98-154">After your test user has been migrated to the unified contact store, you can verify that the user’s contacts can be retrieved by calling Test-CsUnifiedContactStore without the Setup parameter:</span></span>

    Test-CsUnifiedContactStore -TargetFqdn atl-cs-001.litwareinc.com -UserSipAddress "sip:kenmyer@litwareinc.com" -RegistrarPort 5061 -Authentication TrustedServer

</div>

<div>

## <a name="xmpp-synthetic-transactions"></a><span data-ttu-id="abd98-155">Transactions synthétiques XMPP</span><span class="sxs-lookup"><span data-stu-id="abd98-155">XMPP Synthetic Transactions</span></span>

<span data-ttu-id="abd98-156">La transaction synthétique de messagerie instantanée (extensible Messaging and Presence Protocol) nécessite que la fonctionnalité XMPP soit configurée avec un ou plusieurs domaines fédérés.</span><span class="sxs-lookup"><span data-stu-id="abd98-156">The XMPP (Extensible Messaging and Presence Protocol) IM synthetic transaction requires that the XMPP feature be configured with one or more federated domains.</span></span>

<span data-ttu-id="abd98-157">Pour activer la transaction synthétique XMPP, un paramètre XmppTestReceiverMailAddress doit être fourni avec un compte d’utilisateur sur un domaine XMPP routable.</span><span class="sxs-lookup"><span data-stu-id="abd98-157">To enable the XMPP synthetic transaction, an XmppTestReceiverMailAddress parameter must be provided with a user account at a routable XMPP domain.</span></span> <span data-ttu-id="abd98-158">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="abd98-158">For example:</span></span>

    Set-CsWatcherNodeConfiguration -Identity pool0.contoso.com -Tests @{Add="XmppIM"} -XmppTestReceiverMailAddress user1@litwareinc.com

<span data-ttu-id="abd98-159">Dans cet exemple, une règle Lync Server 2013 doit exister pour acheminer les messages pour litwareinc.com vers une passerelle XMPP.</span><span class="sxs-lookup"><span data-stu-id="abd98-159">In this example, a Lync Server 2013 rule will need to exist to route messages for litwareinc.com to an XMPP gateway.</span></span>

<span data-ttu-id="abd98-160"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="abd98-160"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

