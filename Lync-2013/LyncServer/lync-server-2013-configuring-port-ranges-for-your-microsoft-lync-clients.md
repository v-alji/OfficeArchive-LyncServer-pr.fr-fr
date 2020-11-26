---
title: 'Lync Server 2013 : configuration de plages de ports pour vos clients Microsoft Lync'
description: 'Lync Server 2013 : configuration de plages de ports pour vos clients Microsoft Lync.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring port ranges for your Microsoft Lync clients
ms:assetid: 287d5cea-7ada-461c-9b4a-9da2af315e71
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204760(v=OCS.15)
ms:contentKeyID: 48183694
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1e7fcabf81f8e0110010b1a4fb8e697fb0da986c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432729"
---
# <a name="configuring-port-ranges-for-your-microsoft-lync-clients-in-lync-server-2013"></a><span data-ttu-id="35cc0-103">Configuration de plages de ports pour vos clients Microsoft Lync dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="35cc0-103">Configuring port ranges for your Microsoft Lync clients in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="35cc0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="35cc0-104">

<span> </span></span></span>

<span data-ttu-id="35cc0-105">_**Dernière modification de la rubrique :** 2014-04-22_</span><span class="sxs-lookup"><span data-stu-id="35cc0-105">_**Topic Last Modified:** 2014-04-22_</span></span>

<span data-ttu-id="35cc0-106">Par défaut, les applications clientes Lync peuvent utiliser n’importe quel port entre les ports 1024 et 65535 lorsqu’une session de communication est utilisée. en effet, les plages de port spécifiques ne sont pas activées automatiquement pour les clients.</span><span class="sxs-lookup"><span data-stu-id="35cc0-106">By default, Lync client applications can use any port between ports 1024 and 65535 when involved in a communication session; this is because specific port ranges are not automatically enabled for clients.</span></span> <span data-ttu-id="35cc0-107">Toutefois, pour pouvoir utiliser la qualité de service, vous devez réaffecter les différents types de trafic (audio, vidéo, média, partage d’application et transfert de fichier) à une série de plages de ports uniques.</span><span class="sxs-lookup"><span data-stu-id="35cc0-107">In order to use Quality of Service, however, you will need to reassign the various traffic types (audio, video, media, application sharing, and file transfer) to a series of unique port ranges.</span></span> <span data-ttu-id="35cc0-108">Pour ce faire, vous pouvez utiliser l’applet de Set-CsConferencingConfiguration.</span><span class="sxs-lookup"><span data-stu-id="35cc0-108">This can be done by using the Set-CsConferencingConfiguration cmdlet.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="35cc0-109">Les utilisateurs finaux ne peuvent pas apporter ces modifications.</span><span class="sxs-lookup"><span data-stu-id="35cc0-109">End users cannot make these changes themselves.</span></span> <span data-ttu-id="35cc0-110">Les modifications de port ne peuvent être effectuées que par les administrateurs à l’aide de l’applet de Set-CsConferencingConfiguration.</span><span class="sxs-lookup"><span data-stu-id="35cc0-110">Port changes can only be made by administrators using the Set-CsConferencingConfiguration cmdlet.</span></span>



</div>

<span data-ttu-id="35cc0-111">Vous pouvez déterminer les plages de ports actuellement utilisées pour les sessions de communication en exécutant la commande suivante à partir de Microsoft Lync Server 2013 Management Shell :</span><span class="sxs-lookup"><span data-stu-id="35cc0-111">You can determine which port ranges are currently used for communication sessions by running the following command from within the Microsoft Lync Server 2013 Management Shell:</span></span>

    Get-CsConferencingConfiguration

<span data-ttu-id="35cc0-112">Si vous avez apporté des modifications à vos paramètres de conférence depuis que vous avez installé Lync Server 2013, vous devez obtenir des informations sur les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="35cc0-112">Assuming that you have not made any changes to your conferencing settings since you installed Lync Server 2013, you should get back information that includes these property values:</span></span>

    ClientMediaPortRangeEnabled : False
    ClientAudioPort             : 5350
    ClientAudioPortRange        : 40
    ClientVideoPort             : 5350
    ClientVideoPortRange        : 40
    ClientAppSharingPort        : 5350
    ClientAppSharingPortRange   : 40
    ClientFileTransferPort      : 5350
    ClientTransferPortRange     : 40

<span data-ttu-id="35cc0-113">Si vous observez de près la sortie précédente, vous verrez deux points importants.</span><span class="sxs-lookup"><span data-stu-id="35cc0-113">If you look closely at the preceding output, you'll see two things of importance.</span></span> <span data-ttu-id="35cc0-114">Tout d’abord, la propriété ClientMediaPortRangeEnabled est définie sur false :</span><span class="sxs-lookup"><span data-stu-id="35cc0-114">First, the ClientMediaPortRangeEnabled property is set to False:</span></span>

    ClientMediaPortRangeEnabled : False

<span data-ttu-id="35cc0-115">C’est important, car lorsque cette propriété est définie sur false, les clients Lync utiliseront tout port disponible entre 1024 et 65535 lorsqu’une session de communication sera utilisée. C’est vrai, quels que soient les autres paramètres de port (par exemple, ClientMediaPort ou ClientVideoPort).</span><span class="sxs-lookup"><span data-stu-id="35cc0-115">That's important because, when this property is set to False, Lync clients will use any available port between ports 1024 and 65535 when involved in a communication session; this is true regardless of any other port settings (for example, ClientMediaPort or ClientVideoPort).</span></span> <span data-ttu-id="35cc0-116">Si vous souhaitez restreindre l’utilisation à un ensemble spécifique de ports (ce que vous voulez faire si vous envisagez d’implémenter la qualité de service), vous devez d’abord activer les plages de port de média client.</span><span class="sxs-lookup"><span data-stu-id="35cc0-116">If you want to restrict usage to a specified set of ports (and this is something you do want to do if you plan on implementing Quality of Service) then you must first enable client media port ranges.</span></span> <span data-ttu-id="35cc0-117">Vous pouvez effectuer cette opération à l’aide de la commande Windows PowerShell suivante :</span><span class="sxs-lookup"><span data-stu-id="35cc0-117">That can be done using the following Windows PowerShell command:</span></span>

    Set-CsConferencingConfiguration -ClientMediaPortRangeEnabled $True

<span data-ttu-id="35cc0-118">La commande précédente permet d’activer les plages de port de média client pour la collection globale de paramètres de configuration de conférence. Toutefois, ces paramètres peuvent également être appliqués à l’étendue du site et/ou à l’étendue du service (pour le service du serveur de conférence uniquement).</span><span class="sxs-lookup"><span data-stu-id="35cc0-118">The preceding command enables client media port ranges for the global collection of conferencing configuration settings; however, these settings can also be applied to the site scope and/or the service scope (for the Conferencing Server service only).</span></span> <span data-ttu-id="35cc0-119">Pour activer les plages de port de média client pour un site ou un serveur spécifique, spécifiez l’identité de ce site ou serveur lors de l’appel de Set-CsConferencingConfiguration :</span><span class="sxs-lookup"><span data-stu-id="35cc0-119">To enable client media port ranges for a specific site or server, specify the Identity of that site or server when calling Set-CsConferencingConfiguration:</span></span>

    Set-CsConferencingConfiguration -Identity "site:Redmond" -ClientMediaPortRangeEnabled $True

<span data-ttu-id="35cc0-120">Vous pouvez également utiliser cette commande pour activer simultanément les plages de ports pour tous les paramètres de configuration de la Conférence :</span><span class="sxs-lookup"><span data-stu-id="35cc0-120">Alternatively, you can use this command to simultaneously enable port ranges for all your conferencing configuration settings:</span></span>

    Get-CsConferencingConfiguration | Set-CsConferencingConfiguration  -ClientMediaPortRangeEnabled $True

<span data-ttu-id="35cc0-121">Le deuxième élément important que vous remarquerez est que la sortie de l’exemple indique que, par défaut, les plages de ports multimédias définies pour chaque type de trafic réseau sont identiques :</span><span class="sxs-lookup"><span data-stu-id="35cc0-121">The second thing of importance you will notice is that the sample output shows that, by default, the media port ranges set for each type of network traffic are identical:</span></span>

    ClientAudioPort             : 5350
    ClientVideoPort             : 5350
    ClientAppSharingPort        : 5350
    ClientFileTransferPort      : 5350

<span data-ttu-id="35cc0-122">Pour implémenter QoS, chacune de ces plages de port doit être unique.</span><span class="sxs-lookup"><span data-stu-id="35cc0-122">In order to implement QoS, each of these port ranges will need to be unique.</span></span> <span data-ttu-id="35cc0-123">Par exemple, vous pouvez configurer les plages de ports comme suit :</span><span class="sxs-lookup"><span data-stu-id="35cc0-123">For example, you might configure the port ranges like this:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="35cc0-124">Type de trafic client</span><span class="sxs-lookup"><span data-stu-id="35cc0-124">Client Traffic Type</span></span></th>
<th><span data-ttu-id="35cc0-125">Début du port</span><span class="sxs-lookup"><span data-stu-id="35cc0-125">Port Start</span></span></th>
<th><span data-ttu-id="35cc0-126">Plage de ports</span><span class="sxs-lookup"><span data-stu-id="35cc0-126">Port Range</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="35cc0-127">Audio</span><span class="sxs-lookup"><span data-stu-id="35cc0-127">Audio</span></span></p></td>
<td><p><span data-ttu-id="35cc0-128">50020</span><span class="sxs-lookup"><span data-stu-id="35cc0-128">50020</span></span></p></td>
<td><p><span data-ttu-id="35cc0-129">CX3-20</span><span class="sxs-lookup"><span data-stu-id="35cc0-129">20</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35cc0-130">Vidéo</span><span class="sxs-lookup"><span data-stu-id="35cc0-130">Video</span></span></p></td>
<td><p><span data-ttu-id="35cc0-131">58000</span><span class="sxs-lookup"><span data-stu-id="35cc0-131">58000</span></span></p></td>
<td><p><span data-ttu-id="35cc0-132">CX3-20</span><span class="sxs-lookup"><span data-stu-id="35cc0-132">20</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35cc0-133">Partage d'application</span><span class="sxs-lookup"><span data-stu-id="35cc0-133">Application sharing</span></span></p></td>
<td><p><span data-ttu-id="35cc0-134">42000</span><span class="sxs-lookup"><span data-stu-id="35cc0-134">42000</span></span></p></td>
<td><p><span data-ttu-id="35cc0-135">CX3-20</span><span class="sxs-lookup"><span data-stu-id="35cc0-135">20</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35cc0-136">Transfert de fichiers</span><span class="sxs-lookup"><span data-stu-id="35cc0-136">File transfer</span></span></p></td>
<td><p><span data-ttu-id="35cc0-137">42020</span><span class="sxs-lookup"><span data-stu-id="35cc0-137">42020</span></span></p></td>
<td><p><span data-ttu-id="35cc0-138">CX3-20</span><span class="sxs-lookup"><span data-stu-id="35cc0-138">20</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="35cc0-139">Dans le tableau ci-dessus, les plages de port client représentent un sous-ensemble des plages de ports configurées pour vos serveurs.</span><span class="sxs-lookup"><span data-stu-id="35cc0-139">In the preceding table, client port ranges represent a subset of the port ranges configured for your servers.</span></span> <span data-ttu-id="35cc0-140">Par exemple, sur les serveurs, le partage d’application a été configuré de manière à utiliser les ports 40803 à 49151 ; sur les ordinateurs clients, le partage d’application est configuré de manière à utiliser les ports 42000 à 42019.</span><span class="sxs-lookup"><span data-stu-id="35cc0-140">For example, on the servers, application sharing was configured to use ports 40803 through 49151; on the client computers, application sharing is configured to use ports 42000 through 42019.</span></span> <span data-ttu-id="35cc0-141">Pour simplifier l’administration de la qualité de service (QoS), il n’est pas nécessaire de représenter un sous-ensemble de ports utilisés sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="35cc0-141">This, too is done primarily to make administration of QoS easier: client ports do not have to represent a subset of the ports used on the server.</span></span> <span data-ttu-id="35cc0-142">(Par exemple, sur les ordinateurs clients, vous pouvez configurer le partage d’application à utiliser, par exemple, les ports 10000 à 10019.) Néanmoins, nous vous conseillons de faire en sorte que les plages de port de votre client constituent un sous-ensemble de vos plages de port serveur.</span><span class="sxs-lookup"><span data-stu-id="35cc0-142">(For example, on the client computers you could configure application sharing to use, say, ports 10000 through 10019.) However, it is recommended that you make your client port ranges a subset of your server port ranges.</span></span>

<span data-ttu-id="35cc0-143">Par ailleurs, vous avez peut-être remarqué que les ports 8348 étaient mis de côté pour le partage d’application sur les serveurs, mais que seuls 20 ports étaient mis de côté pour le partage d’application sur les clients.</span><span class="sxs-lookup"><span data-stu-id="35cc0-143">In addition, you might have noticed that 8348 ports were set aside for application sharing on the servers, but only 20 ports were set aside for application sharing on the clients.</span></span> <span data-ttu-id="35cc0-144">C’est également recommandé, mais il ne s’agit pas d’une règle matérielle et rapide.</span><span class="sxs-lookup"><span data-stu-id="35cc0-144">This, too is recommended, but is not a hard-and-fast rule.</span></span> <span data-ttu-id="35cc0-145">En règle générale, vous pouvez considérer chaque port disponible pour représenter une seule session de communication : Si vous disposez de ports 100 disponibles dans une plage de ports qui signifie que l’ordinateur en question peut participer, au plus, des sessions de communication 100 à tout moment.</span><span class="sxs-lookup"><span data-stu-id="35cc0-145">In general, you can consider each available port to represent a single communication session: if you have 100 ports available in a port range that means that the computer in question could participate in, at most, 100 communication sessions at any given time.</span></span> <span data-ttu-id="35cc0-146">Étant donné que les serveurs seront susceptibles de participer dans de nombreuses conversations qu’aux clients, il est préférable d’ouvrir de nombreux ports supplémentaires sur les serveurs plutôt que sur les clients.</span><span class="sxs-lookup"><span data-stu-id="35cc0-146">Because servers will likely take part in many more conversations than clients, it makes sense to open many more ports on servers than on clients.</span></span> <span data-ttu-id="35cc0-147">La mise en place de 20 ports pour le partage d’application sur un client implique qu’un utilisateur peut participer à 20 sessions de partage d’application sur l’appareil spécifié, en même temps.</span><span class="sxs-lookup"><span data-stu-id="35cc0-147">Setting aside 20 ports for application sharing on a client means that a user could participate in 20 application sharing sessions on the specified device, and all at the same time.</span></span> <span data-ttu-id="35cc0-148">Cela devrait s’avérer suffisant pour la plupart de vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="35cc0-148">That should prove sufficient for the vast majority of your users.</span></span>

<span data-ttu-id="35cc0-149">Pour affecter les plages de port précédentes à votre collection globale de paramètres de configuration de conférence, vous pouvez utiliser la commande Lync Server Management Shell suivante :</span><span class="sxs-lookup"><span data-stu-id="35cc0-149">To assign the preceding port ranges to your global collection of conferencing configuration settings you can use the following Lync Server Management Shell command:</span></span>

    Set-CsConferencingConfiguration -Identity global -ClientAudioPort 50020 -ClientAudioPortRange 20 -ClientVideoPort 58000 -ClientVideoPortRange 20 -ClientAppSharingPort 42000 -ClientAppSharingPortRange 20 - ClientFileTransferPort 42020 -ClientFileTransferPortRange 20

<span data-ttu-id="35cc0-150">Vous pouvez utiliser cette commande pour affecter les mêmes plages de ports à tous les paramètres de configuration de la Conférence :</span><span class="sxs-lookup"><span data-stu-id="35cc0-150">Or, use this command to assign these same port ranges for all your conferencing configuration settings:</span></span>

    Get-CsConferencingConfiguration | Set-CsConferencingConfiguration -ClientAudioPort 50020 -ClientAudioPortRange 20 -ClientVideoPort 58000 -ClientVideoPortRange 20 -ClientAppSharingPort 42000 -ClientAppSharingPortRange 20 - ClientFileTransferPort 42020 -ClientFileTransferPortRange 20

<span data-ttu-id="35cc0-151">Les utilisateurs individuels doivent se déconnecter de Lync, puis reconnectez-vous pour que les modifications prennent effet.</span><span class="sxs-lookup"><span data-stu-id="35cc0-151">Individual users must log off from Lync and then log back on before these changes will actually take effect.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="35cc0-152">Vous pouvez également activer les plages de port de média client, puis les affecter à l’aide d’une seule commande.</span><span class="sxs-lookup"><span data-stu-id="35cc0-152">You can also enable client media port ranges, and then assign those port ranges, using a single command.</span></span> <span data-ttu-id="35cc0-153">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="35cc0-153">For example:</span></span><BR><CODE>Set-CsConferencingConfiguration -ClientMediaPortRangeEnabled $True -ClientAudioPort 50020 -ClientAudioPortRange 20 -ClientVideoPort 58000 -ClientVideoPortRange 20 -ClientAppSharingPort 42000 -ClientAppSharingPortRange 20 -ClientFileTransferPort 42020 -ClientFileTransferPortRange 20</CODE>



<span data-ttu-id="35cc0-154"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="35cc0-154"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

