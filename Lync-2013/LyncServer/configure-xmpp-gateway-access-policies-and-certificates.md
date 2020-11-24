---
title: Configuration des certificats et des stratégies d’accès de passerelle XMPP
description: Configurez les stratégies d’accès à la passerelle XMPP et les certificats.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Configure XMPP gateway access policies and certificates
ms:assetid: fac02f4e-d14d-4be3-b53c-74c82436fd93
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721945(v=OCS.15)
ms:contentKeyID: 49733882
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e958100501ad9ca87d1ab970162f4be8c7692a99
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394097"
---
# <a name="configure-xmpp-gateway-access-policies-and-certificates"></a><span data-ttu-id="a5d17-103">Configuration des certificats et des stratégies d’accès de passerelle XMPP</span><span class="sxs-lookup"><span data-stu-id="a5d17-103">Configure XMPP gateway access policies and certificates</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a5d17-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a5d17-104">

<span> </span></span></span>

<span data-ttu-id="a5d17-105">_**Dernière modification de la rubrique :** 2012-10-15_</span><span class="sxs-lookup"><span data-stu-id="a5d17-105">_**Topic Last Modified:** 2012-10-15_</span></span>

<span data-ttu-id="a5d17-106">La Fédération XMPP définit un déploiement externe en fonction du protocole XMPP (eXtensible Messaging and Presence Protocol).</span><span class="sxs-lookup"><span data-stu-id="a5d17-106">XMPP federation defines an external deployment based on the eXtensible Messaging and Presence Protocol (XMPP).</span></span> <span data-ttu-id="a5d17-107">Une configuration XMPP permet aux utilisateurs de Lync d’accéder aux utilisateurs de domaine XMPP en procédant comme suit :</span><span class="sxs-lookup"><span data-stu-id="a5d17-107">An XMPP configuration allows Lync users access to XMPP domain users by:</span></span>

  - <span data-ttu-id="a5d17-108">Messagerie instantanée et présence-personne à personne uniquement</span><span class="sxs-lookup"><span data-stu-id="a5d17-108">IM and Presence – person to person only</span></span>

  - <span data-ttu-id="a5d17-109">Créer des contacts fédérés de XMPP dans le client Lync</span><span class="sxs-lookup"><span data-stu-id="a5d17-109">Creation of XMPP federated contacts in the Lync client</span></span>

<span data-ttu-id="a5d17-110">Lorsque vous configurez des stratégies pour la prise en charge des partenaires fédérés du protocole de messagerie extensible et de présence, les stratégies s’appliquent aux utilisateurs des domaines fédérés de XMPP (par exemple, Windows Live) et aux domaines fédérés SIP (Session Initiation Protocol).</span><span class="sxs-lookup"><span data-stu-id="a5d17-110">When you configure policies for support of extensible messaging and presence protocol (XMPP) federated partners, the policies apply to users of XMPP federated domains, but not to users of session initiation protocol (SIP) instant messaging (IM) service providers (for example, Windows Live), or SIP federated domains.</span></span> <span data-ttu-id="a5d17-111">Vous configurez un partenaire fédéré de XMPP pour chaque domaine fédéré XMPP que vous voulez autoriser vos utilisateurs à ajouter des contacts et à communiquer avec eux.</span><span class="sxs-lookup"><span data-stu-id="a5d17-111">You configure an XMPP Federated Partner for each XMPP federated domain that you want to allow your users to add contacts and communicate with.</span></span> <span data-ttu-id="a5d17-112">Une fois les stratégies en place, vous devez configurer les certificats de passerelle XMPP.</span><span class="sxs-lookup"><span data-stu-id="a5d17-112">Once the policies are in place, you need to configure the XMPP Gateway certificates.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a5d17-113">Pour lancer la migration de la passerelle XMPP, vous devez déployer la passerelle de Lync Server 2013 XMPP et configurer des stratégies d’accès pour permettre aux utilisateurs de Lync Server 2013 la passerelle XMPP.</span><span class="sxs-lookup"><span data-stu-id="a5d17-113">To begin the XMPP Gateway migration, you need to deploy the Lync Server 2013 XMPP Gateway, and configure access policies to enable users for Lync Server 2013 XMPP Gateway.</span></span> <span data-ttu-id="a5d17-114">Pour pouvoir effectuer cette procédure, tous les utilisateurs doivent être déplacés vers le déploiement Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a5d17-114">All users must be moved to the Lync Server 2013 deployment before you perform these steps.</span></span> <span data-ttu-id="a5d17-115">Pour plus d’informations, consultez <A href="configure-xmpp-gateway-on-lync-server-2013.md">configurer la passerelle XMPP sur Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="a5d17-115">For details, see <A href="configure-xmpp-gateway-on-lync-server-2013.md">Configure XMPP gateway on Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="configure-an-external-access-policy-to-enable-users-for-lync-server-2013-xmpp-gateway"></a><span data-ttu-id="a5d17-116">Configurer une stratégie d’accès externe pour permettre aux utilisateurs de Lync Server 2013-passerelle XMPP</span><span class="sxs-lookup"><span data-stu-id="a5d17-116">Configure an External Access Policy to Enable Users for Lync Server 2013 XMPP Gateway</span></span>

1.  <span data-ttu-id="a5d17-117">Ouvrez le Paneau de configuration Lync Server.</span><span class="sxs-lookup"><span data-stu-id="a5d17-117">Open Lync Server Control Panel.</span></span>

2.  <span data-ttu-id="a5d17-118">Dans la barre de navigation de gauche, cliquez sur **Fédération et accès externe**, puis sur **stratégie d’accès externe**.</span><span class="sxs-lookup"><span data-stu-id="a5d17-118">In the left navigation bar, click **Federation and External Access**, and then click **External Access Policy**.</span></span>

3.  <span data-ttu-id="a5d17-119">Cliquez sur **nouveau** , puis sur stratégie de l' **utilisateur**.</span><span class="sxs-lookup"><span data-stu-id="a5d17-119">Click **New** and then click **User policy**.</span></span>

4.  <span data-ttu-id="a5d17-120">Entrez le nom de la stratégie de l’utilisateur pour l’accès externe.</span><span class="sxs-lookup"><span data-stu-id="a5d17-120">Enter a name for the external access user policy.</span></span>

5.  <span data-ttu-id="a5d17-121">Entrez une description pour la stratégie utilisateur d’accès externe.</span><span class="sxs-lookup"><span data-stu-id="a5d17-121">Provide a description for external access user policy.</span></span>

6.  <span data-ttu-id="a5d17-122">Sélectionnez **activer les communications avec les utilisateurs fédérés**.</span><span class="sxs-lookup"><span data-stu-id="a5d17-122">Select **Enable communications with federated users**.</span></span>

7.  <span data-ttu-id="a5d17-123">Sélectionnez **activer les communications avec les utilisateurs fédérés de XMPP**.</span><span class="sxs-lookup"><span data-stu-id="a5d17-123">Select **Enable communications with XMPP federated users**.</span></span>

8.  <span data-ttu-id="a5d17-124">Cliquez sur **valider** pour enregistrer les modifications apportées à la stratégie de site ou d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a5d17-124">Click **Commit** to save your changes to the site or user policy.</span></span>

<span data-ttu-id="a5d17-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a5d17-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

