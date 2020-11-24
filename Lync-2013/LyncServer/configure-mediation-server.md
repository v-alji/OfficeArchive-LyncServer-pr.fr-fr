---
title: Configurer le serveur de médiation
description: Configuration du serveur de médiation.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Configure Mediation Server
ms:assetid: 583236fd-33cd-4045-81df-baa58ed07779
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204913(v=OCS.15)
ms:contentKeyID: 48184207
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5723d9446122b85f7bd1812f7c6f411c5c1c9dbe
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394437"
---
# <a name="configure-mediation-server"></a><span data-ttu-id="a06a2-103">Configurer le serveur de médiation</span><span class="sxs-lookup"><span data-stu-id="a06a2-103">Configure Mediation Server</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a06a2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a06a2-104">

<span> </span></span></span>

<span data-ttu-id="a06a2-105">_**Dernière modification de la rubrique :** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="a06a2-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="a06a2-106">Cette procédure décrit la procédure de configuration du pool Lync Server 2013 de manière à utiliser le serveur de médiation Lync Server 2013 au lieu du serveur de médiation traditionnel d’Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="a06a2-106">This procedure details the steps to configure the Lync Server 2013 pool to use the Lync Server 2013 Mediation Server, instead of the legacy Office Communications Server 2007 R2 Mediation Server.</span></span>

<span data-ttu-id="a06a2-107">Pour publier, activer ou désactiver une topologie lors de l’ajout ou de la suppression d’un rôle serveur, vous devez être connecté en tant qu’utilisateur membre des groupes RTCUniversalServerAdmins et Admins du domaine.</span><span class="sxs-lookup"><span data-stu-id="a06a2-107">To successfully publish, enable, or disable a topology when adding or removing a server role, you should be logged in as a user who is a member of the RTCUniversalServerAdmins and Domain Admins groups.</span></span> <span data-ttu-id="a06a2-108">Il est également possible de déléguer les droits d’administrateur et les autorisations nécessaires pour ajouter des rôles de serveur.</span><span class="sxs-lookup"><span data-stu-id="a06a2-108">It is also possible to delegate the proper administrator rights and permissions for adding server roles.</span></span> <span data-ttu-id="a06a2-109">Pour plus d’informations, voir autorisations de configuration de délégué dans la documentation de déploiement Standard Edition Server ou Enterprise Edition Server.</span><span class="sxs-lookup"><span data-stu-id="a06a2-109">For details, see Delegate Setup Permissions in the Standard Edition server or Enterprise Edition server Deployment documentation.</span></span> <span data-ttu-id="a06a2-110">Pour les autres modifications de configuration, seule l’appartenance au groupe RTCUniversalServerAdmins est requise.</span><span class="sxs-lookup"><span data-stu-id="a06a2-110">For other configuration changes, only membership in the RTCUniversalServerAdmins group is required.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a06a2-111">Pour obtenir les dernières informations sur la recherche de passerelles RTC, de PBX IP et de services d’agrégation de messages SIP qualifiés compatibles avec Lync Server 2013, voir « Microsoft Unified Communications Open Interoperability » à l’adresse <A href="https://go.microsoft.com/fwlink/p/?linkid=206015">https://go.microsoft.com/fwlink/p/?linkId=206015</A> .</span><span class="sxs-lookup"><span data-stu-id="a06a2-111">For the latest information on finding qualified PSTN gateways, IP-PBXs, and SIP trunking services that work with Lync Server 2013, see "Microsoft Unified Communications Open Interoperability Program" at <A href="https://go.microsoft.com/fwlink/p/?linkid=206015">https://go.microsoft.com/fwlink/p/?linkId=206015</A>.</span></span>



</div>

<div>

## <a name="to-configure-mediation-server-using-topology-builder"></a><span data-ttu-id="a06a2-112">Pour configurer la médiation serveur à l’aide du générateur de topologie</span><span class="sxs-lookup"><span data-stu-id="a06a2-112">To configure Mediation Server Using Topology Builder</span></span>

1.  <span data-ttu-id="a06a2-113">Ouvrez une topologie existante à partir du générateur de topologie.</span><span class="sxs-lookup"><span data-stu-id="a06a2-113">Open an existing topology from Topology Builder.</span></span>

2.  <span data-ttu-id="a06a2-114">Dans le volet gauche, sélectionnez **passerelles RTC**.</span><span class="sxs-lookup"><span data-stu-id="a06a2-114">In the left pane, navigate to **PSTN gateways**.</span></span>

3.  <span data-ttu-id="a06a2-115">Cliquez avec le bouton droit sur **passerelles RTC**, puis cliquez sur **nouvelle passerelle IP/PSTN**.</span><span class="sxs-lookup"><span data-stu-id="a06a2-115">Right-click **PSTN gateways**, and then click **New IP/PSTN Gateway**.</span></span>

4.  <span data-ttu-id="a06a2-116">Complétez la page **définir une nouvelle passerelle IP/RTC** en utilisant les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="a06a2-116">Complete the **Define New IP/PSTN Gateway** page with the following information:</span></span>
    
      - <span data-ttu-id="a06a2-117">Entrez le nom de domaine complet ou l’adresse IP de la passerelle.</span><span class="sxs-lookup"><span data-stu-id="a06a2-117">Enter the gateway FQDN or IP address.</span></span> <span data-ttu-id="a06a2-118">Le FQDN de la passerelle est requis si la passerelle utilise le protocole TLS.</span><span class="sxs-lookup"><span data-stu-id="a06a2-118">The FQDN of the gateway is required if the gateway uses the TLS protocol.</span></span>
    
      - <span data-ttu-id="a06a2-119">Acceptez la valeur par défaut du **port d’écoute pour la passerelle IP/PSTN** ou entrez le nouveau port d’écoute s’il a été modifié.</span><span class="sxs-lookup"><span data-stu-id="a06a2-119">Accept the default value of the **Listening port for IP/PSTN gateway** or enter the new listening port if it was modified.</span></span>
    
      - <span data-ttu-id="a06a2-120">Définissez le **protocole de transport SIP**.</span><span class="sxs-lookup"><span data-stu-id="a06a2-120">Set the **Sip Transport Protocol**.</span></span>

5.  <span data-ttu-id="a06a2-121">Dans le volet gauche, accédez au **pool frontal d’Enterprise Edition** ou au **serveur Standard Edition Server**.</span><span class="sxs-lookup"><span data-stu-id="a06a2-121">In the left pane, navigate to the **Enterprise Edition Front End pool** or the **Standard Edition Server**.</span></span>

6.  <span data-ttu-id="a06a2-122">Cliquez avec le bouton droit sur la liste, puis cliquez sur **modifier les propriétés**.</span><span class="sxs-lookup"><span data-stu-id="a06a2-122">Right-click the pool, and then click **Edit Properties**.</span></span>

7.  <span data-ttu-id="a06a2-123">Sous **serveur de médiation**, définissez les **ports Listening**.</span><span class="sxs-lookup"><span data-stu-id="a06a2-123">Under **Mediation Server**, set the **Listening ports**.</span></span>

8.  <span data-ttu-id="a06a2-124">Ensuite, associez la passerelle RTC nouvellement créée en la sélectionnant et en cliquant sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="a06a2-124">Next, associate the newly created PSTN gateway by selecting it and clicking **Add**.</span></span>

9.  <span data-ttu-id="a06a2-125">Dans **Générateur de topologie**, sélectionnez le **serveur Lync** le plus en tête de nœud.</span><span class="sxs-lookup"><span data-stu-id="a06a2-125">In **Topology Builder**, select the top-most node **Lync Server**.</span></span>

10. <span data-ttu-id="a06a2-126">Dans le menu **action** , sélectionnez la **topologie de publication** , puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="a06a2-126">From the **Action** menu, select **Publish Topology** and then click **Next**.</span></span>

11. <span data-ttu-id="a06a2-127">Lorsque l' **Assistant Publication** est terminé, cliquez sur **Terminer** pour fermer l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="a06a2-127">When the **Publishing wizard** completes, click **Finish** to close the wizard.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a06a2-128">Il est important que vous complétiez le sujet suivant, que vous <A href="change-voice-routes-to-use-the-new-lync-server-2013-mediation-server.md">Modifiez les itinéraires vocaux pour utiliser le nouveau serveur de médiation Lync Server 2013</A> pour vous assurer que les itinéraires vocaux pointent vers le serveur de médiation approprié.</span><span class="sxs-lookup"><span data-stu-id="a06a2-128">It is important that you complete the next topic, <A href="change-voice-routes-to-use-the-new-lync-server-2013-mediation-server.md">Change voice routes to use the new Lync Server 2013 Mediation Server</A> to ensure that the voice routes are pointing to the correct Mediation Server.</span></span>



<span data-ttu-id="a06a2-129"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a06a2-129"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

