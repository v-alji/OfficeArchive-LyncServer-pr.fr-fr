---
title: 'Lync Server 2013 : Configuration des certificats pour le serveur proxy inverse'
description: 'Lync Server 2013 : configurer des certificats pour le proxy inverse.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Set up certificates for the reverse proxy
ms:assetid: c03a08ec-a67b-4f11-b0d7-6677461beaaa
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412938(v=OCS.15)
ms:contentKeyID: 48185291
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f4b84241775bb3594840b68551048c01ff5faba2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441745"
---
# <a name="set-up-certificates-for-the-reverse-proxy-in-lync-server-2013"></a><span data-ttu-id="64d1a-103">Configuration des certificats pour le serveur proxy inverse dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="64d1a-103">Set up certificates for the reverse proxy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="64d1a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="64d1a-104">

<span> </span></span></span>

<span data-ttu-id="64d1a-105">_**Dernière modification de la rubrique :** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="64d1a-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="64d1a-106">Chaque serveur proxy inverse nécessite un certificat de serveur Web pour une utilisation par le service d’écoute.</span><span class="sxs-lookup"><span data-stu-id="64d1a-106">Each reverse proxy server requires a web server certificate for use by the listening service.</span></span> <span data-ttu-id="64d1a-107">Le certificat de serveur Web doit être émis par une autorité de certification (CA) publique.</span><span class="sxs-lookup"><span data-stu-id="64d1a-107">The web server certificate must be issued by a public certification authority (CA).</span></span>

<span data-ttu-id="64d1a-108">Pour plus d’informations sur ce problème et sur les autres exigences relatives aux certificats, voir [exigences relatives aux certificats pour l’accès des utilisateurs externes dans Lync Server 2013](lync-server-2013-certificate-requirements-for-external-user-access.md).</span><span class="sxs-lookup"><span data-stu-id="64d1a-108">For details about this and other certificate requirements, see [Certificate requirements for external user access in Lync Server 2013](lync-server-2013-certificate-requirements-for-external-user-access.md).</span></span>

<div>

## <a name="to-set-up-a-web-services-certificate-for-the-reverse-proxy"></a><span data-ttu-id="64d1a-109">Pour configurer un certificat de services Web pour le proxy inverse</span><span class="sxs-lookup"><span data-stu-id="64d1a-109">To set up a Web Services certificate for the reverse proxy</span></span>

  - <span data-ttu-id="64d1a-110">Vous avez déjà configuré votre proxy inverse, y compris la configuration du certificat de services Web.</span><span class="sxs-lookup"><span data-stu-id="64d1a-110">You should have already set up your reverse proxy, including setting up the Web Services certificate.</span></span> <span data-ttu-id="64d1a-111">Si vous ne l’avez pas fait avant de commencer le déploiement de vos serveurs de périphérie, suivez les procédures décrites dans la [configuration de serveurs proxy inverse pour Lync Server 2013](lync-server-2013-setting-up-reverse-proxy-servers.md) pour créer une demande et installer le certificat de services Web, puis créez chaque règle de publication Web et configurez-la pour utiliser le certificat.</span><span class="sxs-lookup"><span data-stu-id="64d1a-111">If you did not do so before starting your deployment of your Edge Servers, use the procedures in [Setting up reverse proxy servers for Lync Server 2013](lync-server-2013-setting-up-reverse-proxy-servers.md) to create request and install the Web Services certificate, and then create each web publishing rule and configure it to use the certificate.</span></span>

<span data-ttu-id="64d1a-112"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="64d1a-112"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

