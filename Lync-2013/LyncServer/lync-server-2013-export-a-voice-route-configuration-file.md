---
title: 'Lync Server 2013 : exporter un fichier de configuration de l’itinéraire vocal'
description: 'Lync Server 2013 : exporter un fichier de configuration de l’itinéraire vocal.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Export a voice route configuration file
ms:assetid: 02ce922d-9ca8-4513-b09f-9de51f5c5bdc
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398081(v=OCS.15)
ms:contentKeyID: 48183248
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 30bf342e11be41015df3cfd76f6a875381cb8b64
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428369"
---
# <a name="export-a-voice-route-configuration-file-in-lync-server-2013"></a><span data-ttu-id="6c399-103">Exporter un fichier de configuration de l’itinéraire vocale dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6c399-103">Export a voice route configuration file in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6c399-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6c399-104">

<span> </span></span></span>

<span data-ttu-id="6c399-105">_**Dernière modification de la rubrique :** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="6c399-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="6c399-106">Si vous voulez enregistrer votre configuration de routage de la voix sans la publier, procédez comme suit pour utiliser les commandes d’exportation et d’importation du panneau de configuration de Lync Server pour enregistrer et récupérer une capture instantanée de votre configuration de routage de votre voix.</span><span class="sxs-lookup"><span data-stu-id="6c399-106">If you want to save your voice routing configuration without publishing it, follow these steps to use the Lync Server Control Panel configuration export and import commands to save and retrieve a snapshot of your voice routing configuration.</span></span> <span data-ttu-id="6c399-107">Lorsque vous importez un fichier de configuration de l’acheminement vocal (. VCFG), mais que des modifications ont été apportées à la configuration de l’acheminement du message sur le serveur, les pages du groupe de **routage vocal** dans Lync Server Control Panel indiquent qu’il n’y a pas de modifications non validées sur le routage vocal.</span><span class="sxs-lookup"><span data-stu-id="6c399-107">When you import a voice routing configuration file (.vcfg), but changes have been made to the voice routing configuration on the server in the meantime, the pages in the **Voice Routing** group in Lync Server Control Panel will indicate that there are uncommitted changes to voice routing.</span></span> <span data-ttu-id="6c399-108">Ces modifications non validées représentent les différences entre les deux configurations qui doivent être rapprochées.</span><span class="sxs-lookup"><span data-stu-id="6c399-108">Those uncommitted changes are the differences between the two configurations that require reconciliation.</span></span>

<span data-ttu-id="6c399-109">Si vous avez apporté des modifications non validées aux paramètres sur n’importe quelle page du groupe, les modifications sont enregistrées dans le fichier de configuration de la voix exporté (. VCFG).</span><span class="sxs-lookup"><span data-stu-id="6c399-109">If you have made any uncommitted changes to the settings on any page within the group, the changes are saved in the exported voice configuration file (.vcfg).</span></span> <span data-ttu-id="6c399-110">Cela vous permet de procéder à des modifications de la configuration de l’acheminement des messages pendant plusieurs sessions avant de publier les modifications.</span><span class="sxs-lookup"><span data-stu-id="6c399-110">This enables you to make voice routing configuration changes during multiple sessions before you publish the changes.</span></span>

<div>

## <a name="to-export-a-voice-routing-configuration"></a><span data-ttu-id="6c399-111">Pour exporter une configuration du routage des communications vocales</span><span class="sxs-lookup"><span data-stu-id="6c399-111">To export a voice routing configuration</span></span>

1.  <span data-ttu-id="6c399-112">Connectez-vous à l’ordinateur en tant que membre du groupe RTCUniversalServerAdmins ou en tant que membre du rôle CsVoiceAdministrator, CsServerAdministrator ou CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="6c399-112">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the CsVoiceAdministrator, CsServerAdministrator, or CsAdministrator role.</span></span> <span data-ttu-id="6c399-113">Pour plus d’informations, reportez-vous à la section [délégation des autorisations de configuration dans Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="6c399-113">For details, see [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="6c399-114">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="6c399-114">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="6c399-115">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="6c399-115">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="6c399-116">Dans la barre de navigation de gauche, cliquez sur **Routage des communications vocales**.</span><span class="sxs-lookup"><span data-stu-id="6c399-116">In the left navigation bar, click **Voice Routing**.</span></span>

4.  <span data-ttu-id="6c399-117">Dans le menu **Actions**, cliquez sur **Exporter la configuration**.</span><span class="sxs-lookup"><span data-stu-id="6c399-117">On the **Actions** menu, click **Export configuration**.</span></span>

5.  <span data-ttu-id="6c399-118">Spécifiez un emplacement et un nom de fichier, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="6c399-118">Specify a location and file name, and then click **Save**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="6c399-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6c399-119">See Also</span></span>


[<span data-ttu-id="6c399-120">Importation d’un fichier de configuration d’itinéraire de communications vocales dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6c399-120">Import a voice route configuration file in Lync Server 2013</span></span>](lync-server-2013-import-a-voice-route-configuration-file.md)  
  

<span data-ttu-id="6c399-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6c399-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

