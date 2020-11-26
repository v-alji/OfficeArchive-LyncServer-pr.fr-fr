---
title: 'Lync Server 2013 : Utilisation d’applets de commande pour inverser la préparation d’un domaine'
description: 'Lync Server 2013 : utilisation de cmdlets pour contrepasser la préparation du domaine.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Using cmdlets to reverse domain preparation
ms:assetid: 014dba5d-fcb3-44c9-9d63-ae0755276dac
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398071(v=OCS.15)
ms:contentKeyID: 48183227
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1d26cc97ee934ee959838f38f4e2f52f9bf89566
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439015"
---
# <a name="using-cmdlets-to-reverse-domain-preparation-for-lync-server-2013"></a><span data-ttu-id="627d7-103">Utilisation d’applets de commande pour inverser la préparation d’un domaine pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="627d7-103">Using cmdlets to reverse domain preparation for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="627d7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="627d7-104">

<span> </span></span></span>

<span data-ttu-id="627d7-105">_**Dernière modification de la rubrique :** 2012-10-29_</span><span class="sxs-lookup"><span data-stu-id="627d7-105">_**Topic Last Modified:** 2012-10-29_</span></span>

<span data-ttu-id="627d7-106">Utilisez l’applet de action **Disable-CsAdDomain** pour inverser l’étape de préparation du domaine.</span><span class="sxs-lookup"><span data-stu-id="627d7-106">Use the **Disable-CsAdDomain** cmdlet to reverse the domain preparation step.</span></span>

<div>

## <a name="to-use-cmdlets-to-reverse-domain-preparation"></a><span data-ttu-id="627d7-107">Pour utiliser des applets de cmdlet pour contrepasser la préparation du domaine</span><span class="sxs-lookup"><span data-stu-id="627d7-107">To use cmdlets to reverse domain preparation</span></span>

1.  <span data-ttu-id="627d7-108">Ouvrez une session sur n’importe quel serveur du domaine en tant que membre du groupe Domain Admins.</span><span class="sxs-lookup"><span data-stu-id="627d7-108">Log on to any server in the domain as a member of the Domain Admins group.</span></span>

2.  <span data-ttu-id="627d7-109">Démarrez Lync Server Management Shell : cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="627d7-109">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="627d7-110">Exécutez :</span><span class="sxs-lookup"><span data-stu-id="627d7-110">Run:</span></span>
    
        Disable-CsAdDomain [-Domain <Fqdn>] [-DomainController <Fqdn>] [-Force <SwitchParameter>] 
        [-GlobalCatalog <Fqdn>] [-GlobalSettingsDomainController <Fqdn>] 
    
    <span data-ttu-id="627d7-111">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="627d7-111">For example:</span></span>
    
        Disable-CsAdDomain -Domain domain1.contoso.net -GlobalSettingsDomainController dc01.domain1.contoso.net -Force
    
    <span data-ttu-id="627d7-112">Si le paramètre force est présent, la préparation du domaine est restaurée, même si un ou plusieurs serveurs frontaux ou serveurs de conférence A/V du domaine sont activés.</span><span class="sxs-lookup"><span data-stu-id="627d7-112">If the Force parameter is present, domain preparation is rolled back, even if one or more Front End Servers or A/V Conferencing Servers in the domain are activated.</span></span> <span data-ttu-id="627d7-113">Si le paramètre force n’est pas présent, la restauration de la préparation du domaine est arrêtée si un serveur frontal ou un serveur de conférence A/V du domaine est activé.</span><span class="sxs-lookup"><span data-stu-id="627d7-113">If the Force parameter is not present, domain preparation rollback is terminated if any Front End Servers or A/V Conferencing Servers in the domain are activated.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="627d7-114">Le paramètre GlobalSettingsDomainController vous permet d’indiquer l’emplacement de stockage des paramètres globaux.</span><span class="sxs-lookup"><span data-stu-id="627d7-114">The parameter GlobalSettingsDomainController allows you to indicate where global settings are stored.</span></span> <span data-ttu-id="627d7-115">Si vos paramètres sont stockés dans le conteneur système (qui est généralement utilisé avec des déploiements de mise à niveau pour lesquels le paramètre global n’a pas été déplacé vers le conteneur de configuration), vous définissez un contrôleur de domaine à la racine de votre forêt Active Directory.</span><span class="sxs-lookup"><span data-stu-id="627d7-115">If your settings are stored in the System container (which is typical with upgrade deployments that have not had the global setting migrated to the Configuration container), you define a domain controller in the root of your Active Directory forest.</span></span> <span data-ttu-id="627d7-116">Si les paramètres globaux se trouvent dans le conteneur de configuration (ce qui est caractéristique des nouveaux déploiements ou des déploiements de mise à niveau où les paramètres ont été migrés vers le conteneur de configuration, vous devez définir un contrôleur de domaine dans la forêt.</span><span class="sxs-lookup"><span data-stu-id="627d7-116">If the global settings are in the Configuration container (which is typical with new deployments or upgrade deployments where the settings have been migrated to the Configuration container), you define any domain controller in the forest.</span></span> <span data-ttu-id="627d7-117">Si vous ne spécifiez pas ce paramètre, l’applet de commande suppose que les paramètres sont stockés dans le conteneur de configuration et font référence à tout contrôleur de domaine dans AD &nbsp; DS.</span><span class="sxs-lookup"><span data-stu-id="627d7-117">If you do not specify this parameter, the cmdlet assumes that the settings are stored in the Configuration container and refers to any domain controller in AD&nbsp;DS.</span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="627d7-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="627d7-118">See Also</span></span>


[<span data-ttu-id="627d7-119">Exécution de la préparation du domaine pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="627d7-119">Running domain preparation for Lync Server 2013</span></span>](lync-server-2013-running-domain-preparation.md)  


[<span data-ttu-id="627d7-120">Préparation des domaines pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="627d7-120">Preparing domains for Lync Server 2013</span></span>](lync-server-2013-preparing-domains.md)  
  

<span data-ttu-id="627d7-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="627d7-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

