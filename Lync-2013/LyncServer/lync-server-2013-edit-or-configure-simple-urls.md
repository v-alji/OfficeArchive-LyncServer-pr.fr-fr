---
title: 'Lync Server 2013 : Modification ou configuration des URL simples'
description: 'Lync Server 2013 : modifiez ou configurez des URL simples.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Edit or configure simple URLs
ms:assetid: 0008aeea-4ae9-4e36-83cd-ef7ff7b6e128
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398063(v=OCS.15)
ms:contentKeyID: 48183216
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f9152a65083f71510f4cdb1189b3982afdd68b4c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49393784"
---
# <a name="edit-or-configure-simple-urls-in-lync-server-2013"></a><span data-ttu-id="f29d8-103">Modification ou configuration des URL simples dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f29d8-103">Edit or configure simple URLs in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f29d8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f29d8-104">

<span> </span></span></span>

<span data-ttu-id="f29d8-105">_**Dernière modification de la rubrique :** 2014-02-04_</span><span class="sxs-lookup"><span data-stu-id="f29d8-105">_**Topic Last Modified:** 2014-02-04_</span></span>

<span data-ttu-id="f29d8-106">Cette procédure ne nécessite pas d’appartenance à un administrateur local ou à un groupe de domaines privilégiés.</span><span class="sxs-lookup"><span data-stu-id="f29d8-106">This procedure does not require membership in a local administrator or privileged domain group.</span></span> <span data-ttu-id="f29d8-107">Vous devez vous connecter à un ordinateur en tant qu’utilisateur standard.</span><span class="sxs-lookup"><span data-stu-id="f29d8-107">You should log on to a computer as a standard user.</span></span>

<span data-ttu-id="f29d8-108">Lync Server 2013 utilise des URL simples pour diriger les appels internes et externes vers des services du serveur frontal ou du réalisateur, s’il a été déployé.</span><span class="sxs-lookup"><span data-stu-id="f29d8-108">Lync Server 2013 uses simple URLs to direct internal and external calls to services on the Front End Server or on the Director, if one has been deployed.</span></span> <span data-ttu-id="f29d8-109">Pour plus d’informations sur les URL simples, voir [planification d’URL simples dans Lync Server 2013](lync-server-2013-planning-for-simple-urls.md) dans la documentation de planification.</span><span class="sxs-lookup"><span data-stu-id="f29d8-109">For more information about simple URLs, see [Planning for simple URLs in Lync Server 2013](lync-server-2013-planning-for-simple-urls.md) in the Planning documentation.</span></span> <span data-ttu-id="f29d8-110">Vous pouvez sélectionner le format de vos URL simples à partir de plusieurs options.</span><span class="sxs-lookup"><span data-stu-id="f29d8-110">You can select the format for your simple URLs from several options.</span></span> <span data-ttu-id="f29d8-111">Pour plus d’informations sur ces options, voir [configurations DNS requises pour les URL simples dans Lync Server 2013](lync-server-2013-dns-requirements-for-simple-urls.md) dans la documentation de planification.</span><span class="sxs-lookup"><span data-stu-id="f29d8-111">For details about these options, see [DNS requirements for simple URLs in Lync Server 2013](lync-server-2013-dns-requirements-for-simple-urls.md) in the Planning documentation.</span></span>

<span data-ttu-id="f29d8-112">Par défaut, les URL simples seront configurées sous la forme (par exemple, l’URL de connexion simple) : https://dialin .\<SIP Domain\></span><span class="sxs-lookup"><span data-stu-id="f29d8-112">By default, simple URLs will be configured in the form of (for example, the dial-in simple URL): https://dialin.\<SIP Domain\></span></span>

<div>

## <a name="to-configure-simple-urls"></a><span data-ttu-id="f29d8-113">Pour configurer des URL simples</span><span class="sxs-lookup"><span data-stu-id="f29d8-113">To configure simple URLs</span></span>

1.  <span data-ttu-id="f29d8-114">Dans le générateur de topologie, cliquez avec le bouton droit sur le nœud du **serveur Lync** , puis cliquez sur **modifier les propriétés**.</span><span class="sxs-lookup"><span data-stu-id="f29d8-114">In Topology Builder, right-click the **Lync Server** node, and then click **Edit Properties**.</span></span>

2.  <span data-ttu-id="f29d8-115">Dans le volet **URL simples**, sélectionnez **URL d’accès téléphonique :** (Dial-In) ou **URL de réunion :** (Meet) pour modifier l’URL, puis cliquez sur **Modifier l’URL**.</span><span class="sxs-lookup"><span data-stu-id="f29d8-115">In the **Simple URLs** pane, select either **Phone access URLs:** (Dial-in) or **Meeting URLs:** (Meet) to edit, and then click **Edit URL**.</span></span>

3.  <span data-ttu-id="f29d8-116">Mettez à jour l’URL comme vous le souhaitez puis cliquez sur **OK** pour enregistrer l’URL modifiée.</span><span class="sxs-lookup"><span data-stu-id="f29d8-116">Update the URL to the value you want, and then click **OK** to save the edited URL.</span></span> <span data-ttu-id="f29d8-117">L’exemple présenté ici a modifié l’URL d’accès à la Conférence rendez-vous en https://pool01.contoso.net/dialin .</span><span class="sxs-lookup"><span data-stu-id="f29d8-117">The example shown here has modified the Dial-in URL to https://pool01.contoso.net/dialin.</span></span>

4.  <span data-ttu-id="f29d8-118">Modifiez l’URL Meet en procédant de la même manière, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="f29d8-118">Edit the Meet URL by using the same steps, if necessary.</span></span>

</div>

<div>

## <a name="to-define-the-optional-admin-simple-url"></a><span data-ttu-id="f29d8-119">Pour définir l’URL simple Admin facultative</span><span class="sxs-lookup"><span data-stu-id="f29d8-119">To define the optional Admin simple URL</span></span>

1.  <span data-ttu-id="f29d8-120">Dans le générateur de topologie, cliquez avec le bouton droit sur le nœud du **serveur Lync** , puis cliquez sur **modifier les propriétés**.</span><span class="sxs-lookup"><span data-stu-id="f29d8-120">In Topology Builder, right-click the **Lync Server** node, and then click **Edit Properties**.</span></span>

2.  <span data-ttu-id="f29d8-121">Dans la zone **URL d’accès administratif** , entrez l’URL de votre choix pour l’accès administratif au panneau de configuration de Lync Server 2013, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="f29d8-121">In the **Administrative access URL** box, enter the simple URL you want for administrative access to Lync Server 2013 Control Panel, and then click **OK**.</span></span>
    
    <div>
    

    > [!TIP]  
    > <span data-ttu-id="f29d8-122">Nous vous recommandons d’utiliser l’URL la plus simple possible pour l’URL d’administration.</span><span class="sxs-lookup"><span data-stu-id="f29d8-122">We recommend using the simplest possible URL for the Admin URL.</span></span> <span data-ttu-id="f29d8-123">L’option la plus simple est <STRONG> https://admin .</STRONG> &lt; Domain (domaine) &gt; .</span><span class="sxs-lookup"><span data-stu-id="f29d8-123">The simplest option is <STRONG>https://admin.</STRONG>&lt;domain&gt;.</span></span>

    
    </div>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="f29d8-124">Si vous changez une URL simple après son déploiement initial, vous devez savoir quels changements impactent vos enregistrements et certificats DNS pour les URL simples.</span><span class="sxs-lookup"><span data-stu-id="f29d8-124">If you change a simple URL after initial deployment, you must be aware of what changes impact your Domain Name System (DNS) records and certificates for simple URLs.</span></span> <span data-ttu-id="f29d8-125">Si le changement a un impact sur la base d’une URL simple, vous devez également modifier les enregistrements DNS et les certificats.</span><span class="sxs-lookup"><span data-stu-id="f29d8-125">If the change impacts the base of a simple URL, then you must change the DNS records and certificates as well.</span></span> <span data-ttu-id="f29d8-126">Par exemple, https://lync.contoso.com/Meet https://meet.contoso.com si vous modifiez l’URL de base de lync.contoso.com à Meet.contoso.com, vous devez modifier les enregistrements DNS et les certificats pour faire référence à Meet.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="f29d8-126">For example, changing from https://lync.contoso.com/Meet to https://meet.contoso.com changes the base URL from lync.contoso.com to meet.contoso.com, so you would need to change the DNS records and certificates to refer to meet.contoso.com.</span></span> <span data-ttu-id="f29d8-127">Si vous avez changé l’URL simple de https://lync.contoso.com/Meet à https://lync.contoso.com/Meetings , l’URL de base de Lync.contoso.com reste inchangée et aucune modification du DNS ou du certificat n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="f29d8-127">If you changed the simple URL from https://lync.contoso.com/Meet to https://lync.contoso.com/Meetings, the base URL of lync.contoso.com stays the same, so no DNS or certificate changes are needed.</span></span> <span data-ttu-id="f29d8-128">Néanmoins, chaque fois que vous modifiez un nom d’URL simple, vous devez exécuter l’applet de passe <STRONG>Enable-CsComputer</STRONG> sur chaque réalisateur et serveur frontal pour enregistrer la modification.</span><span class="sxs-lookup"><span data-stu-id="f29d8-128">Whenever you change a simple URL name, however, you must run the <STRONG>Enable-CsComputer</STRONG> cmdlet on each Director and Front End Server to register the change.</span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="f29d8-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f29d8-129">See Also</span></span>


[<span data-ttu-id="f29d8-130">Planification des URL simples dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f29d8-130">Planning for simple URLs in Lync Server 2013</span></span>](lync-server-2013-planning-for-simple-urls.md)  
  

<span data-ttu-id="f29d8-131"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f29d8-131"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

