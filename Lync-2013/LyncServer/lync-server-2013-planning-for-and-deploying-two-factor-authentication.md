---
title: 'Lync Server 2013 : planification et déploiement de l’authentification à deux facteurs'
description: 'Lync Server 2013 : planification et déploiement de l’authentification à deux facteurs.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for and deploying two-factor authentication
ms:assetid: 442a88df-ebc2-4335-9c59-0ce1adc1471e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn308563(v=OCS.15)
ms:contentKeyID: 54973686
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e1e04fa7a0c1184152328882a7c7b4bea8e42ec0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437118"
---
# <a name="two-factor-authentication-in-lync-server-2013"></a><span data-ttu-id="a6d3c-103">Authentification à deux facteurs dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a6d3c-103">Two-factor authentication in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a6d3c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a6d3c-104">

<span> </span></span></span>

<span data-ttu-id="a6d3c-105">_**Dernière modification de la rubrique :** 2013-07-11_</span><span class="sxs-lookup"><span data-stu-id="a6d3c-105">_**Topic Last Modified:** 2013-07-11_</span></span>

<span data-ttu-id="a6d3c-106">L’authentification à deux facteurs fournit une sécurité améliorée en demandant aux utilisateurs de répondre à deux critères d’authentification : une combinaison nom d’utilisateur/mot de passe et un jeton ou un certificat.</span><span class="sxs-lookup"><span data-stu-id="a6d3c-106">Two-factor authentication provides improved security by requiring users to meet two authentication criteria: a user name/password combination and a token or certificate.</span></span> <span data-ttu-id="a6d3c-107">Cette technique est également appelée « quelque chose que vous avez, quelque chose ce que vous savez ».</span><span class="sxs-lookup"><span data-stu-id="a6d3c-107">This is also known as “something you have, something you know.”</span></span> <span data-ttu-id="a6d3c-108">Un exemple classique d’authentification à deux facteurs avec un certificat est l’utilisation de cartes à puce.</span><span class="sxs-lookup"><span data-stu-id="a6d3c-108">A typical example of two-factor authentication with a certificate is the use of smart cards.</span></span> <span data-ttu-id="a6d3c-109">Une carte à puce contient un certificat associé au compte d’utilisateur et peut être validé par rapport aux informations d’utilisateur et de certificat stockées sur un serveur.</span><span class="sxs-lookup"><span data-stu-id="a6d3c-109">A smart card contains a certificate associated with the user account, and can be validated against user and certificate information stored on a server.</span></span> <span data-ttu-id="a6d3c-110">En comparant les informations utilisateur (nom d’utilisateur et mot de passe) au certificat fourni, le serveur valide les informations d’identification et authentifie l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a6d3c-110">By comparing the user information (user name and password) to the certificate provided, the server validates the credentials and authenticates the user.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="a6d3c-111">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="a6d3c-111">In This Section</span></span>

[<span data-ttu-id="a6d3c-112">Planification de l’authentification à deux facteurs dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a6d3c-112">Planning for two-factor authentication in Lync Server 2013</span></span>](lync-server-2013-planning-for-two-factor-authentication.md)

[<span data-ttu-id="a6d3c-113">Configuration de l’authentification à deux facteurs dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a6d3c-113">Configuring two-factor authentication in Lync Server 2013</span></span>](lync-server-2013-configuring-two-factor-authentication.md)

[<span data-ttu-id="a6d3c-114">Utilisation de l’authentification à deux facteurs avec le client Lync et Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a6d3c-114">Using two-factor authentication with Lync client and Lync Server 2013</span></span>](lync-server-2013-using-two-factor-authentication-with-lync-client.md)

<span data-ttu-id="a6d3c-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a6d3c-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

