---
title: 'Lync Server 2013 : configurer une application SNMP'
description: 'Lync Server 2013 : configurer une application SNMP.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure an SNMP application
ms:assetid: c4b4a736-3b2e-45b9-a965-19d22161ad57
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412972(v=OCS.15)
ms:contentKeyID: 48185346
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e7374b61ad85d7ddcb40ef1db535e17f86dea58f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434108"
---
# <a name="configure-an-snmp-application-in-lync-server-2013"></a><span data-ttu-id="a6403-103">Configurer une application SNMP dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a6403-103">Configure an SNMP application in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a6403-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a6403-104">

<span> </span></span></span>

<span data-ttu-id="a6403-105">_**Dernière modification de la rubrique :** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="a6403-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="a6403-106">Lync Server 2013 inclut une interface de service Web standard que vous pouvez utiliser pour connecter le service d’informations d’emplacement aux applications SNMP (simple Network Management Protocol) qui correspondent aux adresses MAC et aux informations sur les ports et aux commutateurs.</span><span class="sxs-lookup"><span data-stu-id="a6403-106">Lync Server 2013 includes a standard web service interface that you can use to connect the Location Information service to Simple Network Management Protocol (SNMP) applications that match MAC addresses with port and switch information.</span></span>

<span data-ttu-id="a6403-107">Si une application SNMP est installée et que le service des informations de géolocalisation ne trouve pas de correspondance dans la base de données de localisation, le service d’information d’emplacement interroge automatiquement l’application à l’aide de l’adresse MAC fournie par le client.</span><span class="sxs-lookup"><span data-stu-id="a6403-107">If an SNMP application is installed and the Location Information service fails to find a match in the location database, the Location Information service automatically queries the application by using the MAC address provided by the client.</span></span> <span data-ttu-id="a6403-108">Le service d’information d’emplacement utilise alors le port et les informations de commutation renvoyées par l’application SNMP pour interroger de nouveau la base de données d’emplacement.</span><span class="sxs-lookup"><span data-stu-id="a6403-108">The Location Information service then uses the port and switch information returned by the SNMP application to query the location database again.</span></span>

<span data-ttu-id="a6403-109">Pour plus d’informations, consultez la rubrique [Set-CsWebServiceConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsWebServiceConfiguration).</span><span class="sxs-lookup"><span data-stu-id="a6403-109">For details, see [Set-CsWebServiceConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsWebServiceConfiguration).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a6403-110">Les adresses MAC ne sont pas disponibles sur les ordinateurs exécutant Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a6403-110">MAC addresses are not available on computers running Windows 8.</span></span>



</div>

<div>

## <a name="to-configure-the-snmp-application-url"></a><span data-ttu-id="a6403-111">Pour configurer l’URL de l’application SNMP</span><span class="sxs-lookup"><span data-stu-id="a6403-111">To configure the SNMP application URL</span></span>

1.  <span data-ttu-id="a6403-112">Démarrez Lync Server Management Shell : cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="a6403-112">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="a6403-113">Exécutez l’applet de commande suivante pour configurer l’URL de l’application SNMP.</span><span class="sxs-lookup"><span data-stu-id="a6403-113">Run the following cmdlet to configure the URL for the SNMP application.</span></span>
    
        Set-CsWebServiceConfiguration -MACResolverUrl "<SNMP application url>" 

<span data-ttu-id="a6403-114"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a6403-114"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

