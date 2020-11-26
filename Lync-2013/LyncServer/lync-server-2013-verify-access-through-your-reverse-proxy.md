---
title: 'Lync Server 2013 : Vérification de l’accès avec le proxy inverse'
description: 'Lync Server 2013 : vérifier l’accès via votre proxy inverse.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Verify access through your reverse proxy
ms:assetid: 3076a786-e022-4d41-91ec-1bf252b2a468
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429697(v=OCS.15)
ms:contentKeyID: 48183753
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 593aac5574f0dcf683351f12a6392f6116480ac5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443474"
---
# <a name="verify-access-through-your-reverse-proxy-in-lync-server-2013"></a><span data-ttu-id="b196f-103">Vérification de l’accès avec le proxy inverse dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b196f-103">Verify access through your reverse proxy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b196f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b196f-104">

<span> </span></span></span>

<span data-ttu-id="b196f-105">_**Dernière modification de la rubrique :** 2013-03-29_</span><span class="sxs-lookup"><span data-stu-id="b196f-105">_**Topic Last Modified:** 2013-03-29_</span></span>

<span data-ttu-id="b196f-106">Utilisez la procédure suivante pour vérifier que vos utilisateurs peuvent accéder aux informations sur le proxy inverse.</span><span class="sxs-lookup"><span data-stu-id="b196f-106">Use the following procedure to verify that your users can access information on the reverse proxy.</span></span> <span data-ttu-id="b196f-107">Vous devrez peut-être effectuer la configuration de pare-feu et la configuration de DNS (Domain Name System) pour que Access fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="b196f-107">You might need to complete the firewall configuration and Domain Name System (DNS) configuration before access will work correctly.</span></span>

<div>

## <a name="to-verify-that-you-can-access-the-website-through-the-internet"></a><span data-ttu-id="b196f-108">Pour vérifier que vous pouvez accéder au site Web via Internet</span><span class="sxs-lookup"><span data-stu-id="b196f-108">To verify that you can access the website through the Internet</span></span>

  - <span data-ttu-id="b196f-109">Ouvrez un navigateur Web, tapez les URL de la barre d' **adresse** que les clients utilisent pour accéder aux fichiers du carnet d’adresses et au site Web pour les conférences comme suit :</span><span class="sxs-lookup"><span data-stu-id="b196f-109">Open a web browser, type the URLs in the **Address** bar that clients use to access the Address Book files and the website for conferencing as follows:</span></span>
    
      - <span data-ttu-id="b196f-110">Pour le serveur du carnet d’adresses, tapez une URL semblable à ce qui suit : **https://externalwebfarmFQDN/abs** où externalwebfarmFQDN est le nom de domaine complet (FQDN) du service Web externe qui héberge les services du carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="b196f-110">For Address Book Server, type a URL similar to the following: **https://externalwebfarmFQDN/abs** where externalwebfarmFQDN is the external FQDN of the external web services that hosts Address Book services.</span></span> <span data-ttu-id="b196f-111">L’utilisateur doit être confronté à un défi HTTP, car la sécurité d’annuaire dans le dossier serveur du carnet d’adresses est configurée par défaut sur authentification Windows.</span><span class="sxs-lookup"><span data-stu-id="b196f-111">The user should receive an HTTP challenge, because directory security on the Address Book Server folder is configured to Windows authentication by default.</span></span>
    
      - <span data-ttu-id="b196f-112">Pour Conférence, tapez une URL semblable à ce qui suit : **https://externalwebfarmFQDN/meet** où externalwebfarmFQDN est le nom de domaine complet externe de la batterie de serveurs Web qui héberge le contenu de la réunion.</span><span class="sxs-lookup"><span data-stu-id="b196f-112">For conferencing, type a URL similar to the following: **https://externalwebfarmFQDN/meet** where externalwebfarmFQDN is the external FQDN of the web farm that hosts meeting content.</span></span> <span data-ttu-id="b196f-113">Cette URL doit afficher la page de résolution des problèmes pour les conférences.</span><span class="sxs-lookup"><span data-stu-id="b196f-113">This URL should display the troubleshooting page for conferencing.</span></span> <span data-ttu-id="b196f-114">Vous pouvez également vérifier que votre URL simple pour les conférences fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="b196f-114">Alternatively, confirm that your Simple URL for conferencing functions correctly.</span></span> <span data-ttu-id="b196f-115">Un exemple d’URL simple pour la participation à la Conférence peut être https://meet.contoso.com</span><span class="sxs-lookup"><span data-stu-id="b196f-115">An example Simple URL for the conference join might be https://meet.contoso.com</span></span>
    
      - <span data-ttu-id="b196f-116">Pour extension du groupe de distribution, tapez une URL semblable à ce qui suit : **https://externalwebfarmFQDN/GroupExpansion/service.svc** .</span><span class="sxs-lookup"><span data-stu-id="b196f-116">For distribution group expansion, type a URL similar to the following: **https://externalwebfarmFQDN/GroupExpansion/service.svc**.</span></span> <span data-ttu-id="b196f-117">L’utilisateur doit recevoir un défi HTTP, car la sécurité d’annuaire sur le service d’extension du groupe de distribution est configurée par défaut sur l’authentification Windows.</span><span class="sxs-lookup"><span data-stu-id="b196f-117">The user should receive an HTTP challenge, because directory security on the distribution group expansion service is configured to Windows authentication by default.</span></span>
    
      - <span data-ttu-id="b196f-118">Pour composer un numéro de téléphone, tapez l’URL simple semblable à la suivante, **https://externalwebfarmFQDN/dialin** où externalwebfarmFQDN est le nom de domaine complet (FQDN) externe de la batterie de serveurs Web qui héberge la page de conférence rendez-vous pour la Conférence rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="b196f-118">For dial-in, type the simple URL similar to the following **https://externalwebfarmFQDN/dialin** where externalwebfarmFQDN is the external FQDN of the web farm that hosts the dial-in page for dial-in conferencing.</span></span> <span data-ttu-id="b196f-119">L’utilisateur doit être dirigé vers la page de connexion.</span><span class="sxs-lookup"><span data-stu-id="b196f-119">The user should be directed to the dial-in page.</span></span> <span data-ttu-id="b196f-120">Vous pouvez également vérifier que votre URL de connexion simple fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="b196f-120">Alternatively, confirm that your Simple URL dial-in functions correctly.</span></span> <span data-ttu-id="b196f-121">Un exemple d’URL simple pour les appels entrants peut être https://dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="b196f-121">An example Simple URL for dial-in might be https://dialin.contoso.com</span></span>
    
      - <span data-ttu-id="b196f-122">Pour confirmer le fonctionnement de l’URL de découverte automatique, tapez https://lyncdiscover .</span><span class="sxs-lookup"><span data-stu-id="b196f-122">To confirm that the autodiscover URL is working, type https://lyncdiscover.</span></span> <span data-ttu-id="b196f-123">externaldomainFQDN.</span><span class="sxs-lookup"><span data-stu-id="b196f-123">externaldomainFQDN.</span></span> <span data-ttu-id="b196f-124">Le navigateur doit vous inviter à ouvrir un fichier.</span><span class="sxs-lookup"><span data-stu-id="b196f-124">The browser should prompt you to open a file.</span></span> <span data-ttu-id="b196f-125">Sélectionnez Bloc-notes pour l’ouvrir.</span><span class="sxs-lookup"><span data-stu-id="b196f-125">Select Notepad to open it.</span></span> <span data-ttu-id="b196f-126">Une réponse classique serait semblable à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="b196f-126">A typical response would be similar to:</span></span>
        
            {"AccessLocation":"External","Root":{"Links":[{"href":"https:\/\/extweb.contoso.com\/Autodiscover\/AutodiscoverService.svc\/root\/domain","token":"Domain"},
            {"href":"https:\/\/extweb.contoso.com\/Autodiscover\/AutodiscoverService.svc\/root\/user","token":"User"},
            {"href":"https:\/\/lyncweb.contoso.com\/Autodiscover\/AutodiscoverService.svc\/root\/oauth\/user","token":"OAuth"}]}}

<span data-ttu-id="b196f-127"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b196f-127"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

