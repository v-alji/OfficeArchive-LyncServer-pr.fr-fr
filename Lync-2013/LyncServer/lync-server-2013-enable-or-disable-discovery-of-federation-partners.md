---
title: 'Lync Server 2013 : Activation ou désactivation de la découverte de partenaires de fédération'
description: 'Lync Server 2013 : activez ou désactivez la découverte des partenaires de Fédération.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enable or disable discovery of federation partners
ms:assetid: 91fd036b-b1af-47cf-b1cf-0aa0a783c2aa
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182550(v=OCS.15)
ms:contentKeyID: 48184857
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 36b91120ffc1ce2bd6cd8b8114f0330e6d39d996
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428901"
---
# <a name="enable-or-disable-discovery-of-federation-partners-in-lync-server-2013"></a><span data-ttu-id="448ff-103">Activation ou désactivation de la découverte de partenaires de fédération dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="448ff-103">Enable or disable discovery of federation partners in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="448ff-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="448ff-104">

<span> </span></span></span>

<span data-ttu-id="448ff-105">_**Dernière modification de la rubrique :** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="448ff-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="448ff-106">Au moment où vous avez déployé vos serveurs de périphérie et la Fédération activée pour votre organisation, vous devez indiquer si vous souhaitez prendre en charge la découverte automatique des domaines partenaires fédérés.</span><span class="sxs-lookup"><span data-stu-id="448ff-106">At the time you deployed your Edge Servers and enabled federation for your organization, you should have specified whether to support automatic discovery of federated partner domains.</span></span> <span data-ttu-id="448ff-107">Suivez la procédure décrite dans cette rubrique pour modifier cette configuration.</span><span class="sxs-lookup"><span data-stu-id="448ff-107">Use the procedure in this topic to change that configuration.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="448ff-108">La procédure suivante suppose que vous avez déjà activé la Fédération pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="448ff-108">The following procedure assumes that you have already enabled federation for your organization.</span></span> <span data-ttu-id="448ff-109">Pour plus d’informations sur l’activation de la Fédération, voir <A href="lync-server-2013-enable-or-disable-remote-user-access.md">activation ou désactivation de l’accès des utilisateurs distants dans Lync Server 2013</A> dans la documentation de déploiement ou la documentation des opérations.</span><span class="sxs-lookup"><span data-stu-id="448ff-109">For details about enabling federation, see <A href="lync-server-2013-enable-or-disable-remote-user-access.md">Enable or disable remote user access in Lync Server 2013</A> in the Deployment documentation or the Operations documentation.</span></span>



</div>

<div>

## <a name="to-enable-or-disable-automatic-discovery-of-federated-domains-for-your-organization"></a><span data-ttu-id="448ff-110">Pour activer ou désactiver la découverte automatique des domaines fédérés pour votre organisation</span><span class="sxs-lookup"><span data-stu-id="448ff-110">To enable or disable automatic discovery of federated domains for your organization</span></span>

1.  <span data-ttu-id="448ff-111">À partir d’un compte d’utilisateur membre du groupe RTCUniversalServerAdmins (ou doté de droits d’utilisateur équivalents), ou affectées au rôle CsAdministrator, connectez-vous à n’importe quel ordinateur dans votre déploiement interne.</span><span class="sxs-lookup"><span data-stu-id="448ff-111">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="448ff-112">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="448ff-112">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="448ff-113">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="448ff-113">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="448ff-114">Dans la barre de navigation de gauche, cliquez sur **accès utilisateur externe**, puis sur **configuration de Microsoft Edge Access**.</span><span class="sxs-lookup"><span data-stu-id="448ff-114">In the left navigation bar, click **External User Access**, click **Access Edge Configuration**.</span></span>

4.  <span data-ttu-id="448ff-115">Dans la page **configuration de Microsoft Edge** , cliquez sur **Global**, sur **modifier**, puis sur **afficher les détails**.</span><span class="sxs-lookup"><span data-stu-id="448ff-115">On the **Access Edge Configuration** page, click **Global**, click **Edit**, and then click **Show details**.</span></span>

5.  <span data-ttu-id="448ff-116">Dans **modification** de la configuration d’un point d’accès, sous **activer les communications avec des utilisateurs fédérés**, activez ou désactivez la case à cocher **activer la découverte** automatique du domaine pour activer ou désactiver la découverte automatique des domaines partenaires.</span><span class="sxs-lookup"><span data-stu-id="448ff-116">In **Edit Access Edge Configuration**, under **Enable communications with federated users**, select or clear the **Enable partner domain discovery** check box to enable or disable automatic discovery of partner domains.</span></span>

6.  <span data-ttu-id="448ff-117">Cliquez sur **Valider**.</span><span class="sxs-lookup"><span data-stu-id="448ff-117">Click **Commit**.</span></span>

<span data-ttu-id="448ff-118">Pour permettre aux utilisateurs fédérés de collaborer avec des utilisateurs dans le déploiement de Lync Server, vous devez également avoir configuré au moins une stratégie d’accès externe pour prendre en charge l’accès des utilisateurs fédérés.</span><span class="sxs-lookup"><span data-stu-id="448ff-118">To enable federated users to collaborate with users in your Lync Server deployment, you must have also configured at least one external access policy to support federated user access.</span></span> <span data-ttu-id="448ff-119">Pour plus d’informations, reportez-vous à [activation ou désactivation de la connectivité de Fédération et de messagerie instantanée publique dans Lync Server 2013](lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md) dans la documentation de déploiement ou la documentation des opérations.</span><span class="sxs-lookup"><span data-stu-id="448ff-119">For details, see [Enable or disable federation and public IM connectivity in Lync Server 2013](lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md) in the Deployment documentation or the Operations documentation.</span></span> <span data-ttu-id="448ff-120">Pour plus d’informations sur le contrôle de l’accès pour des domaines fédérés spécifiques, voir [gérer des domaines fédérés SIP pour votre organisation dans Lync server 2013](lync-server-2013-manage-sip-federated-domains-for-your-organization.md), [gérer des fournisseurs fédérés SIP pour votre organisation dans Lync Server 2013](lync-server-2013-manage-sip-federated-providers-for-your-organization.md) et [gérer les partenaires fédérés fédérés dans Lync Server 2013](lync-server-2013-manage-xmpp-federated-partners-for-your-organization.md) dans la documentation sur les opérations.</span><span class="sxs-lookup"><span data-stu-id="448ff-120">For details about controlling access for specific federated domains, see [Manage SIP federated domains for your organization in Lync Server 2013](lync-server-2013-manage-sip-federated-domains-for-your-organization.md), [Manage SIP federated providers for your organization in Lync Server 2013](lync-server-2013-manage-sip-federated-providers-for-your-organization.md) and [Manage XMPP federated partners in Lync Server 2013](lync-server-2013-manage-xmpp-federated-partners-for-your-organization.md) in the Operations documentation.</span></span>

</div>

<div>

## <a name="enabling-or-disabling-discovery-of-federation-partners-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="448ff-121">Activation ou désactivation de la découverte de partenaires de Fédération à l’aide d’applets de cmdlet Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="448ff-121">Enabling or Disabling Discovery of Federation Partners by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="448ff-122">La découverte des partenaires de Fédération peut être gérée à l’aide de Windows PowerShell et de l’applet de Set-CsAccessEdgeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="448ff-122">Discovery of federation partners can be managed by using Windows PowerShell and the Set-CsAccessEdgeConfiguration cmdlet.</span></span> <span data-ttu-id="448ff-123">Cette applet de commande peut être exécutée à partir de Lync Server 2013 Management Shell ou d’une session distante de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="448ff-123">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="448ff-124">Pour plus d’informations sur l’utilisation de Windows PowerShell distant pour vous connecter à Lync Server, voir l’article de blog Lync Server Windows PowerShell « démarrage rapide : gestion de Microsoft Lync Server 2010 à l’aide de Remote PowerShell » [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="448ff-124">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-enable-discovery-of-federation-partners"></a><span data-ttu-id="448ff-125">Pour activer la découverte des partenaires de Fédération</span><span class="sxs-lookup"><span data-stu-id="448ff-125">To enable discovery of federation partners</span></span>

  - <span data-ttu-id="448ff-126">Pour activer la découverte des partenaires de Fédération, définissez la valeur de la propriété **EnablePartnerDiscovery** sur True ($true).</span><span class="sxs-lookup"><span data-stu-id="448ff-126">To enable discovery of federation partners, set the value of the **EnablePartnerDiscovery** property to True ($True).</span></span> <span data-ttu-id="448ff-127">Notez que vous devez activer le routage DNS SRV pour pouvoir modifier cette valeur de propriété.</span><span class="sxs-lookup"><span data-stu-id="448ff-127">Note that you must enable DNS SRV routing in order to change this property value.</span></span>
    
        Set-CsAccessEdgeConfiguration -UseDnsSrvRouting -EnablePartnerDiscovery $True

</div>

<div>

## <a name="to-disable-discovery-of-federation-partners"></a><span data-ttu-id="448ff-128">Pour désactiver la découverte des partenaires de Fédération</span><span class="sxs-lookup"><span data-stu-id="448ff-128">To disable discovery of federation partners</span></span>

  - <span data-ttu-id="448ff-129">Pour désactiver la découverte des partenaires de Fédération, définissez la valeur de la propriété **EnablePartnerDiscovery** sur false ($false) :</span><span class="sxs-lookup"><span data-stu-id="448ff-129">To disable discovery of federation partners, set the value of the **EnablePartnerDiscovery** property to False ($False):</span></span>
    
        Set-CsAccessEdgeConfiguration -UseDnsSrvRouting -EnablePartnerDiscovery $False

<span data-ttu-id="448ff-130"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="448ff-130"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

