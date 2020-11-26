---
title: 'Lync Server 2013 : installation du portail Web d’administration du système de salle Lync'
description: 'Lync Server 2013 : installation du portail Web d’administration du système de salle Lync.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Installing the Lync Room System Administrative Web Portal
ms:assetid: dd19e368-c338-4e21-a40d-6439d46a9748
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn436326(v=OCS.15)
ms:contentKeyID: 56737622
ms.date: 04/09/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0fba239346d75142bb4009c58e0ac67e8e1f3bcb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427004"
---
# <a name="installing-the-lync-room-system-administrative-web-portal-in-lync-server-2013"></a><span data-ttu-id="d5100-103">Installing the Lync Room System Administrative Web Portal in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d5100-103">Installing the Lync Room System Administrative Web Portal in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d5100-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d5100-104">

<span> </span></span></span>

<span data-ttu-id="d5100-105">_**Dernière modification de la rubrique :** 2015-04-09_</span><span class="sxs-lookup"><span data-stu-id="d5100-105">_**Topic Last Modified:** 2015-04-09_</span></span>

<span data-ttu-id="d5100-106">Vous pouvez télécharger le portail Web d’administration du système de salle Microsoft Lync à partir du centre de téléchargement Microsoft [https://go.microsoft.com/fwlink/p/?LinkId=324044](https://go.microsoft.com/fwlink/p/?linkid=324044) .</span><span class="sxs-lookup"><span data-stu-id="d5100-106">You can download the Microsoft Lync Room System Administrative Web Portal from the Microsoft Download Center at [https://go.microsoft.com/fwlink/p/?LinkId=324044](https://go.microsoft.com/fwlink/p/?linkid=324044).</span></span>

<span data-ttu-id="d5100-107">Pour installer le portail Web d’administration du système de salle Lync, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="d5100-107">To install the Lync Room System Administrative Web Portal, use the following steps.</span></span>

1.  <span data-ttu-id="d5100-108">Configurez le port d’application fiable en exécutant l’applet de commande suivante dans Lync Server Management Shell :</span><span class="sxs-lookup"><span data-stu-id="d5100-108">Configure the Trusted Application Port by running the following cmdlet in Lync Server Management Shell:</span></span>
    
        Set-CsWebServer -Identity POOLFQDN -MeetingRoomAdminPortalInternalListeningPort 4456 -MeetingRoomAdminPortalExternalListeningPort 4457

2.  <span data-ttu-id="d5100-109">Pour installer le portail de salle de réunion, téléchargez **LyncRoomAdminPortal.exe** puis exécutez-le en tant qu’administrateur.</span><span class="sxs-lookup"><span data-stu-id="d5100-109">To install the Meeting Room Portal, download **LyncRoomAdminPortal.exe** and then run it as an administrator.</span></span>

3.  <span data-ttu-id="d5100-110">Ouvrez le fichier Web.config à partir de l’emplacement suivant :</span><span class="sxs-lookup"><span data-stu-id="d5100-110">Open the Web.config file from the following location:</span></span>
    
    <span data-ttu-id="d5100-111">% Program Files% \\ Microsoft Lync Server 2013 \\ composants WebPart \\ réunion portail de salle de réunion \\ </span><span class="sxs-lookup"><span data-stu-id="d5100-111">%Program Files%\\Microsoft Lync Server 2013\\Web Components\\Meeting Room Portal\\Int\\Handler</span></span>\\\\

4.  <span data-ttu-id="d5100-112">Dans le fichier Web.Config, remplacez PortalUserName par le nom d’utilisateur créé à l’étape 2 de la section « Configuration des conditions préalables pour le portail d’administration du système de salle Lync » (le nom recommandé pour l’étape est LRSApp) :</span><span class="sxs-lookup"><span data-stu-id="d5100-112">In the Web.Config file, change the PortalUserName to the username created in Step 2 under the section “Configuring Prerequisites for Lync Room System Admin Portal” (the recommended name in the step is LRSApp):</span></span>
    
        <add key="PortalUserName" value="sip:LRSApp@domain.com" />

5.  <span data-ttu-id="d5100-113">Le portail d’administration LRS étant une application fiable, vous n’avez pas besoin de fournir le mot de passe dans la configuration du portail.</span><span class="sxs-lookup"><span data-stu-id="d5100-113">Because the LRS Admin Portal is a trusted application, you do not need to provide the password in the portal configuration.</span></span> <span data-ttu-id="d5100-114">Si cet utilisateur utilise un autre serveur d’inscriptions que le serveur d’inscriptions local, vous devez le spécifier en ajoutant la ligne suivante dans le fichier Web.Config :</span><span class="sxs-lookup"><span data-stu-id="d5100-114">If this user is using a different registrar than local registrar, you need to specify the registrar for it by adding the following line in the Web.Config file:</span></span>
    
        <add key="PortalUserRegistrarFQDN" value="pool-xxxx.domain.com" />

6.  <span data-ttu-id="d5100-115">Si le port utilisé n’est pas le port 5061, ajoutez la ligne suivante dans le fichier Web.Config : </span><span class="sxs-lookup"><span data-stu-id="d5100-115">If the port used is other than 5061, add the following line in the Web.Config file:</span></span>
    
        <add key="PortalUserRegistrarPort" value="5061" />

<div>

## <a name="verifying-installation-of-the-lync-room-system-administrative-web-portal"></a><span data-ttu-id="d5100-116">Vérification de l’installation du portail Web d’administration du système de salle Lync</span><span class="sxs-lookup"><span data-stu-id="d5100-116">Verifying Installation of the Lync Room System Administrative Web Portal</span></span>

<span data-ttu-id="d5100-117">Pour vérifier l’installation du portail Web d’administration du système de salle Lync, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="d5100-117">To verify installation of the Lync Room System Administrative Web Portal, do the following:</span></span>


1.  <span data-ttu-id="d5100-118">Sur un serveur frontal, accédez à l’URL suivante :</span><span class="sxs-lookup"><span data-stu-id="d5100-118">On a Front End server, browse to the following URL:</span></span>
    
    <span data-ttu-id="d5100-119"> https:// \<fe-server\> /LRS</span><span class="sxs-lookup"><span data-stu-id="d5100-119">https://\<fe-server\>/lrs</span></span>
    
    <span data-ttu-id="d5100-120">Aucune erreur ne doit s’afficher, comme dans l’image suivante :</span><span class="sxs-lookup"><span data-stu-id="d5100-120">You should not see any errors, as shown in the following image:</span></span>
    
    <span data-ttu-id="d5100-121">![Écran Connexion au portail d’administration Lync Room System](images/Dn436326.050bcf70-2f3b-46b2-9b96-ebd12679b713(OCS.15).png "Écran Connexion au portail d’administration Lync Room System")</span><span class="sxs-lookup"><span data-stu-id="d5100-121">![Lync Room System Admin Portal Sign In screen](images/Dn436326.050bcf70-2f3b-46b2-9b96-ebd12679b713(OCS.15).png "Lync Room System Admin Portal Sign In screen")</span></span>

2.  <span data-ttu-id="d5100-122">Si aucune erreur ne s’affiche, essayez d’accéder à l’URL suivante à partir d’un autre ordinateur dans la topologie :</span><span class="sxs-lookup"><span data-stu-id="d5100-122">If you do not see any errors, try accessing the following URL from any other computer in the topology:</span></span>
    
    <span data-ttu-id="d5100-123"> https:// \<fe-server\> /LRS</span><span class="sxs-lookup"><span data-stu-id="d5100-123">https://\<fe-server\>/lrs</span></span>
    
    <span data-ttu-id="d5100-124">Pour accéder à la page, vous devez ajouter les enregistrements DNS comme décrit dans la section « enregistrements DNS requis pour la connexion automatique au client » [https://go.microsoft.com/fwlink/p/?LinkId=318056](https://go.microsoft.com/fwlink/p/?linkid=318056) .</span><span class="sxs-lookup"><span data-stu-id="d5100-124">To access the page, you will need to add the DNS records as described in “Required DNS Records for Automatic Client Sign-In” at [https://go.microsoft.com/fwlink/p/?LinkId=318056](https://go.microsoft.com/fwlink/p/?linkid=318056).</span></span>

<span data-ttu-id="d5100-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d5100-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

