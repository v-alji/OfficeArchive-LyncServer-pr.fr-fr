---
title: Configuration d’une entrée d’application approuvée pour le contrôle d’appel distant
description: Configurer une entrée d’application fiable pour le contrôle d’appel distant.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure a trusted application entry for remote call control
ms:assetid: 37777f93-8b24-40cf-808e-7c6230eb2132
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558636(v=OCS.15)
ms:contentKeyID: 48183829
ms.date: 11/03/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fa5341dc220853670cf000f5b0d5dc379c02fa51
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434152"
---
# <a name="configure-a-trusted-application-entry-for-remote-call-control-in-lync-server-2013"></a><span data-ttu-id="47446-103">Configuration d’une entrée d’application approuvée pour le contrôle d’appel distant dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="47446-103">Configure a trusted application entry for remote call control in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="47446-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="47446-104">

<span> </span></span></span>

<span data-ttu-id="47446-105">_**Dernière modification de la rubrique :** 2015-11-02_</span><span class="sxs-lookup"><span data-stu-id="47446-105">_**Topic Last Modified:** 2015-11-02_</span></span>

<span data-ttu-id="47446-106">La passerelle SIP/CSTA doit être configurée en tant qu’application approuvée afin que Lync Server applique un itinéraire statique pour acheminer les appels vers la passerelle.</span><span class="sxs-lookup"><span data-stu-id="47446-106">The SIP/CSTA gateway must be configured as a trusted application in order for Lync Server to apply a static route to route calls to the gateway.</span></span>

<div>


> [!IMPORTANT]
> <span data-ttu-id="47446-107">Si vous effectuez une migration à partir d’une version précédente du déploiement de Lync Server, assurez-vous que vous avez supprimé toutes les entrées d’applications approuvées (auparavant connues sous le nom d’entrées d’hébergement autorisées) que vous avez créées pour la passerelle SIP/CSTA avant de suivre les procédures décrites dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="47446-107">If you're migrating users from a previous version of Lync Server deployment, be sure that you removed all existing trusted application entries (previously known as authorized host entries) you created for the SIP/CSTA gateway before following the procedures in this topic.</span></span> <span data-ttu-id="47446-108">Pour plus d’informations, reportez-vous à <A href="lync-server-2013-remove-a-legacy-authorized-host-optional.md">la rubrique supprimer un ancien hôte autorisé de Lync Server 2013 (facultatif)</A>.</span><span class="sxs-lookup"><span data-stu-id="47446-108">For details, see <A href="lync-server-2013-remove-a-legacy-authorized-host-optional.md">Remove a legacy authorized host in Lync Server 2013 (optional)</A>.</span></span><BR><span data-ttu-id="47446-109">Si vous envisagez de déployer le nouveau contrôle d’appel distant à l’aide d’une connexion TCP (Transmission Control Protocol), vous devez vérifier que <STRONG>l’utilisation du service de limitation aux adresses IP sélectionnées</STRONG> doit être définie sur les applications et les pools de confiance existants, si vous souhaitez utiliser le même port TCP pour la nouvelle application de confiance.</span><span class="sxs-lookup"><span data-stu-id="47446-109">If you plan to deploy new remote call control by using a Transmission Control Protocol (TCP) connection, you need to verify that <STRONG>Limit service usage to selected IP addresses</STRONG> should be set on existing trusted applications and pools, if you want to use the same TCP port for the new trusted application.</span></span>



</div>

<div>

## <a name="to-configure-a-trusted-application-entry-for-the-sipcsta-gateway"></a><span data-ttu-id="47446-110">Pour configurer une entrée d’application fiable pour la passerelle SIP/CSTA</span><span class="sxs-lookup"><span data-stu-id="47446-110">To configure a trusted application entry for the SIP/CSTA gateway</span></span>

1.  <span data-ttu-id="47446-111">Ouvrez une session sur l’ordinateur sur lequel Lync Server Management Shell est installé en tant que membre du groupe RTCUniversalServerAdmins ou d’un rôle de contrôle d’accès basé sur un rôle (RBAC) auquel vous avez affecté l’applet **de commande New-CsTrustedApplicationPool** .</span><span class="sxs-lookup"><span data-stu-id="47446-111">Log on to the computer where Lync Server Management Shell is installed as a member of the RTCUniversalServerAdmins group or a role-based access control (RBAC) role to which you have assigned the **New-CsTrustedApplicationPool** cmdlet.</span></span>

2.  <span data-ttu-id="47446-112">Démarrez Lync Server Management Shell : cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="47446-112">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="47446-113">Pour créer une entrée d’application fiable, effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="47446-113">To create a trusted application entry, do one of the following:</span></span>
    
      - <span data-ttu-id="47446-114">Pour une connexion TLS (Transport Layer Security), à l’invite de commandes, tapez ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="47446-114">For a Transport Layer Security (TLS) connection, type the following at the command prompt:</span></span>
        
            New-CsTrustedApplicationPool -Identity <FQDN of the SIP/CSTA gateway> [-Registrar <Service ID or FQDN of the Registrar service>] -Site <Site ID for the site where you want to create the trusted application pool>
        
        <span data-ttu-id="47446-115">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="47446-115">For example:</span></span>
        
            New-CsTrustedApplicationPool -Identity rccgateway.contoso.net -Registrar registrar1.contoso.net -Site co1 -TreatAsAuthenticated $true -ThrottleAsServer $true
    
      - <span data-ttu-id="47446-116">Pour une connexion TCP (Transmission Control Protocol), à l’invite de commandes, tapez ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="47446-116">For a Transmission Control Protocol (TCP) connection, type the following at the command prompt:</span></span>
        
            New-CsTrustedApplicationPool -Identity <IP address or FQDN of the SIP/CSTA gateway> [-Registrar <Service ID or FQDN of the Registrar service>] -Site <Site ID for the site where you want to create the trusted application pool>
        
        <span data-ttu-id="47446-117">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="47446-117">For example:</span></span>
        
            New-CsTrustedApplicationPool -Identity 192.168.0.240 -Registrar registrar1.contoso.net -Site co1 -TreatAsAuthenticated $true -ThrottleAsServer $true

4.  <span data-ttu-id="47446-118">Pour ajouter l’application fiable au pool, effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="47446-118">To add the trusted application to the pool, do one of the following:</span></span>
    
      - <span data-ttu-id="47446-119">Pour une connexion TLS, à l’invite de commandes, tapez ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="47446-119">For a TLS connection, type the following at the command prompt:</span></span>
        
            New-CsTrustedApplication -ApplicationID <application name> -TrustedApplicationPoolFqdn <FQDN of the SIP/CSTA gateway> -Port <SIP listening port on the gateway>
        
        <span data-ttu-id="47446-120">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="47446-120">For example:</span></span>
        
            New-CsTrustedApplication -ApplicationID RccGateway-1 -TrustedApplicationPoolFqdn rccgateway.contoso.net -Port 5065
    
      - <span data-ttu-id="47446-121">Pour une connexion TCP, à l’invite de commandes, tapez ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="47446-121">For a TCP connection, type the following at the command prompt:</span></span>
        
            New-CsTrustedApplication -ApplicationID <application name> -TrustedApplicationPoolFqdn <IP address or FQDN of the SIP/CSTA gateway> -Port <SIP listening port on the gateway> -EnableTcp
        
        <span data-ttu-id="47446-122">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="47446-122">For example:</span></span>
        
            New-CsTrustedApplication -ApplicationID RccGateway-1 -TrustedApplicationPoolFqdn 192.169.0.240 -Port 5065 -EnableTcp

5.  <span data-ttu-id="47446-123">Pour implémenter les modifications publiées apportées à la topologie, à l’invite de commandes, tapez ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="47446-123">To implement the published changes you have made to the topology, type the following at the command prompt:</span></span>
    
        Enable-CsTopology

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="47446-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="47446-124">See Also</span></span>


[<span data-ttu-id="47446-125">Configuration d’un itinéraire statique pour le contrôle d’appel distant dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="47446-125">Configure a static route for remote call control in Lync Server 2013</span></span>](lync-server-2013-configure-a-static-route-for-remote-call-control.md)  
[<span data-ttu-id="47446-126">Définition d’une adresse IP de passerelle SIP/CSTA dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="47446-126">Define a SIP/CSTA gateway IP address in Lync Server 2013</span></span>](lync-server-2013-define-a-sip-csta-gateway-ip-address.md)  
  

<span data-ttu-id="47446-127"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="47446-127"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

