---
title: 'Lync Server 2013 : Création ou modification des fournisseurs fédérés SIP hébergés'
description: 'Lync Server 2013 : créez ou modifiez des fournisseurs fédérés SIP hébergés.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or edit hosted SIP federated providers
ms:assetid: 0dd6dcb6-a88d-46b8-9c96-b35967309bcd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ552445(v=OCS.15)
ms:contentKeyID: 48679556
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: aaaa1b29b9a85332b85dfb7a1f258503fa4e9c77
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431903"
---
# <a name="create-or-edit-hosted-sip-federated-providers-lync-server-2013"></a><span data-ttu-id="7189d-103">Création ou modification des fournisseurs fédérés SIP hébergés dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7189d-103">Create or edit hosted SIP federated providers Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7189d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7189d-104">

<span> </span></span></span>

<span data-ttu-id="7189d-105">_**Dernière modification de la rubrique :** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="7189d-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="7189d-106">La connectivité de messagerie instantanée du fournisseur hébergé permet aux utilisateurs de votre organisation d’utiliser la messagerie instantanée pour communiquer avec les utilisateurs de services de messagerie instantanée proposés par des fournisseurs hébergés, notamment Microsoft 365 et Lync Online.</span><span class="sxs-lookup"><span data-stu-id="7189d-106">Hosted provider instant messaging (IM) connectivity enables users in your organization to use IM to communicate with users of IM services provided by hosted providers, including Microsoft 365 and Lync Online.</span></span>

<span data-ttu-id="7189d-107">Chaque fournisseur hébergé est configuré à l’aide du nom de domaine complet du serveur Edge du fournisseur, et le niveau de vérification par défaut **permet aux utilisateurs de communiquer uniquement avec des personnes de leur liste de contacts qui utilisent ce fournisseur**.</span><span class="sxs-lookup"><span data-stu-id="7189d-107">Each hosted provider is configured with the provider’s Edge server fully qualified domain name, and the default verification level **Allow users to communicate only with people on their Contacts list who use this provider**.</span></span>

<span data-ttu-id="7189d-108">Pour créer ou modifier des fournisseurs hébergés, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="7189d-108">Use the following procedure to create or edit Hosted providers:</span></span>

<div>

## <a name="to-create-or-edit-hosted-providers"></a><span data-ttu-id="7189d-109">Pour créer ou modifier des fournisseurs hébergés</span><span class="sxs-lookup"><span data-stu-id="7189d-109">To create or edit hosted providers</span></span>

1.  <span data-ttu-id="7189d-110">À partir d’un compte d’utilisateur membre du groupe RTCUniversalServerAdmins (ou doté de droits d’utilisateur équivalents), ou affectées au rôle CsAdministrator, connectez-vous à n’importe quel ordinateur dans votre déploiement interne.</span><span class="sxs-lookup"><span data-stu-id="7189d-110">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="7189d-111">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="7189d-111">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="7189d-112">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="7189d-112">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="7189d-113">Dans la barre de navigation de gauche, cliquez sur **Fédération et accès externe**, puis sur **fournisseurs fédérés SIP**.</span><span class="sxs-lookup"><span data-stu-id="7189d-113">In the left navigation bar, click **Federation and External Access**, and then click **SIP Federated Providers**.</span></span>

4.  <span data-ttu-id="7189d-114">Si vous avez besoin de créer un nouveau fournisseur hébergé, cliquez sur **nouveau** , puis cliquez sur **fournisseur hébergé**.</span><span class="sxs-lookup"><span data-stu-id="7189d-114">If you need to create a new Hosted provider, click **New** and then click **Hosted provider**.</span></span>

5.  <span data-ttu-id="7189d-115">Si vous avez besoin de modifier une entrée de la liste des fournisseurs hébergés, sélectionnez un fournisseur hébergé, cliquez sur **modifier**, puis sur **afficher les détails**.</span><span class="sxs-lookup"><span data-stu-id="7189d-115">If you need to edit an entry from the list of Hosted providers, select a hosted provider, click **Edit**, then click **Show details**.</span></span>

6.  <span data-ttu-id="7189d-116">Dans la page **modifier le fournisseur fédéré SIP** , vous pouvez taper ou modifier les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="7189d-116">On the **Edit SIP Federated Provider** page, you can type or edit the following settings:</span></span>
    
      - <span data-ttu-id="7189d-117">**Activer les communications avec ce fournisseur**   Ce paramètre permet de communiquer avec les utilisateurs de ce fournisseur.</span><span class="sxs-lookup"><span data-stu-id="7189d-117">**Enable communications with this provider**   Selecting this setting enables communications with this provider’s users.</span></span>
    
      - <span data-ttu-id="7189d-118">**Nom du fournisseur :**   Une propriété requise, tapez le nom du fournisseur tel qu’il sera reflété dans la liste des fournisseurs fédérés SIP.</span><span class="sxs-lookup"><span data-stu-id="7189d-118">**Provider name:**   A required property, type the name of the provider as it will be reflected in the listing of SIP Federated Providers.</span></span>
    
      - <span data-ttu-id="7189d-119">**Service Edge d’accès (FQDN) :**   Une propriété requise, tapez le nom de domaine complet du service Edge d’accès du fournisseur hébergé que vous configurez.</span><span class="sxs-lookup"><span data-stu-id="7189d-119">**Access Edge service (FQDN):**   A required property, type the fully qualified domain name of the Access Edge service of the hosted provider that you are configuring.</span></span> <span data-ttu-id="7189d-120">Ces informations doivent être fournies par le fournisseur hébergé et ne doivent être changées que si le fournisseur hébergé apporte une modification au FQDN du service Edge d’accès au fournisseur hébergé.</span><span class="sxs-lookup"><span data-stu-id="7189d-120">This information should be provided by the hosted provider, and should only be changed if the hosted provider makes a change to the FQDN of the Access Edge service at the hosted provider.</span></span>
    
      - <span data-ttu-id="7189d-121">**Niveau de vérification par défaut :**   Le paramètre par défaut, **permettre aux utilisateurs de communiquer avec des personnes de leur liste de contacts qui utilisent ce fournisseur** , limite la communication aux contacts que vous avez acceptés et qui figurent dans votre liste de contacts.</span><span class="sxs-lookup"><span data-stu-id="7189d-121">**Default verification level:**   The default setting, **Allow users to communicate with people on their Contacts list who use this provider** will limit communication to contacts that you have accepted and are in your contact list.</span></span>
        
        <span data-ttu-id="7189d-122">Sélectionner **permettre aux utilisateurs de communiquer avec tout le monde à l’aide de ce fournisseur** supprime la restriction que vous devez avoir reçu et accepté une invitation de contact.</span><span class="sxs-lookup"><span data-stu-id="7189d-122">Selecting **Allow users to communicate with everyone using this provider** removes the restriction that you must have received and accepted a contact invite.</span></span> <span data-ttu-id="7189d-123">Ce paramètre ne limite pas qui peut vous contacter à partir du réseau du fournisseur hébergé.</span><span class="sxs-lookup"><span data-stu-id="7189d-123">This setting does not limit who can contact you from the hosted provider’s network.</span></span>

7.  <span data-ttu-id="7189d-124">Lorsque vous avez configuré les paramètres, cliquez sur **valider** pour enregistrer ou cliquez sur **Annuler** pour ignorer vos modifications.</span><span class="sxs-lookup"><span data-stu-id="7189d-124">When you are done configuring the settings, click **Commit** to save, or click **Cancel** to discard your changes.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="7189d-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7189d-125">See Also</span></span>


[<span data-ttu-id="7189d-126">Configuration des stratégies de contrôle d’accès des utilisateurs publics dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7189d-126">Configure policies to control public user access in Lync Server 2013</span></span>](lync-server-2013-configure-policies-to-control-public-user-access.md)  
[<span data-ttu-id="7189d-127">Activation ou désactivation de la fédération et de la connectivité PIC dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7189d-127">Enable or disable federation and public IM connectivity in Lync Server 2013</span></span>](lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md)  
  

<span data-ttu-id="7189d-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7189d-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

