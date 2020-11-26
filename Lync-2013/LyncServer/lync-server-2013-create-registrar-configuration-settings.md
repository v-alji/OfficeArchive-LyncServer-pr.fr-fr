---
title: 'Lync Server 2013 : créer des paramètres de configuration du Bureau d’enregistrement'
description: 'Lync Server 2013 : créer des paramètres de configuration du Bureau d’enregistrement.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create Registrar configuration settings
ms:assetid: eddfbdd2-cfd0-4c03-986e-443d6728db7d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182601(v=OCS.15)
ms:contentKeyID: 48185758
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1ada10302b3c2319e0f713ce2d3bea00b6fed126
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431602"
---
# <a name="create-registrar-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="2a5e8-103">Créer des paramètres de configuration du Bureau d’enregistrement dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2a5e8-103">Create Registrar configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2a5e8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2a5e8-104">

<span> </span></span></span>

<span data-ttu-id="2a5e8-105">_**Dernière modification de la rubrique :** 2013-03-17_</span><span class="sxs-lookup"><span data-stu-id="2a5e8-105">_**Topic Last Modified:** 2013-03-17_</span></span>

<span data-ttu-id="2a5e8-p101">Vous pouvez utiliser le serveur d’inscriptions avancé pour configurer les méthodes d’authentification du serveur proxy. Le protocole d’authentification que vous spécifiez détermine le type de difficultés que les serveurs du pool posent aux clients. Les protocoles disponibles sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="2a5e8-p101">You can use the Registrar to configure proxy server authentication methods. The authentication protocol you specify determines which type of challenges the servers in the pool issue to clients. The available protocols are:</span></span>

  - <span data-ttu-id="2a5e8-109">**Kerberos**   Il s’agit du schéma d’authentification par mot de passe le plus puissant disponible pour les clients, mais uniquement pour les clients d’entreprise, car cela nécessite une connexion client à un centre de distribution de clés (contrôleur de domaine Kerberos).</span><span class="sxs-lookup"><span data-stu-id="2a5e8-109">**Kerberos**   This is the strongest password-based authentication scheme available to clients, but it is normally available only to enterprise clients because it requires client connection to a Key Distribution Center (Kerberos domain controller).</span></span> <span data-ttu-id="2a5e8-110">Ce paramètre est adapté si le serveur ne doit authentifier que des clients entreprise.</span><span class="sxs-lookup"><span data-stu-id="2a5e8-110">This setting is appropriate if the server authenticates only enterprise clients.</span></span>

  - <span data-ttu-id="2a5e8-111">**NTLM**   Il s’agit de l’authentification par mot de passe disponible pour les clients qui utilisent un modèle de hachage de réponse à la demande du mot de passe.</span><span class="sxs-lookup"><span data-stu-id="2a5e8-111">**NTLM**   This is the password-based authentication available to clients that use a challenge-response hashing scheme on the password.</span></span> <span data-ttu-id="2a5e8-112">C’est la seule forme d’authentification proposée aux clients ne disposant pas d’une connectivité à un centre de distribution des clés (contrôleur de domaine Kerberos), comme les utilisateurs distants.</span><span class="sxs-lookup"><span data-stu-id="2a5e8-112">This is the only form of authentication available to clients without connectivity to a Key Distribution Center (Kerberos domain controller), such as remote users.</span></span> <span data-ttu-id="2a5e8-113">Si un serveur n’authentifie que des utilisateurs distants, vous devez choisir NTLM.</span><span class="sxs-lookup"><span data-stu-id="2a5e8-113">If a server authenticates only remote users, you should choose NTLM.</span></span>

  - <span data-ttu-id="2a5e8-114">**Authentification par certificat**   Il s’agit de la nouvelle méthode d’authentification lorsque le serveur doit obtenir des certificats de clients Lync Phone Edition, de téléphones communs, de Lync 2013 et de l’application Lync du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="2a5e8-114">**Certificate authentication**   This is the new authentication method when the server needs to obtain certificates from Lync Phone Edition clients, common area phones, Lync 2013 and the Lync Windows Store app.</span></span> <span data-ttu-id="2a5e8-115">Sur les clients Lync Phone Edition, une fois que l’utilisateur s’est connecté et est authentifié par le biais d’un code confidentiel (PIN), Lync Server 2013 configure l’URI SIP sur le téléphone et met en place un certificat signé Lync Server ou un certificat utilisateur qui identifie Joe (par exemple : SN=joe@contoso.com) sur le téléphone.</span><span class="sxs-lookup"><span data-stu-id="2a5e8-115">On Lync Phone Edition clients, after a user signs in and is successfully authenticated by providing a personal identification number (PIN), Lync Server 2013 then provisions the SIP URI to the phone and provisions a Lync Server signed certificate or a user certificate that identifies Joe (Ex: SN=joe@contoso.com ) to the phone.</span></span> <span data-ttu-id="2a5e8-116">This certificate is used for authenticating with the Registrar and Web Services.</span><span class="sxs-lookup"><span data-stu-id="2a5e8-116">This certificate is used for authenticating with the Registrar and Web Services.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="2a5e8-p105">Nous vous recommandons d’activer Kerberos et NTLM lorsqu’un serveur prend en charge l’authentification des clients distants et d’entreprise. Le serveur Edge et les serveurs internes communiquent pour veiller à ce qu’une authentification NTLM seulement soit proposée aux clients distants. Si seul Kerberos est activé sur ces serveurs, ils ne peuvent pas authentifier les utilisateurs distants. Si des utilisateurs d’entreprise s’authentifient également sur le serveur, Kerberos est utilisé.</span><span class="sxs-lookup"><span data-stu-id="2a5e8-p105">We recommend that you enable both Kerberos and NTLM when a server supports authentication for both remote and enterprise clients. The Edge Server and internal servers communicate to ensure that only NTLM authentication is offered to remote clients. If only Kerberos is enabled on these servers, they cannot authenticate remote users. If enterprise users also authenticate against the server, Kerberos is used.</span></span><BR><span data-ttu-id="2a5e8-121">Si vous allez utiliser les clients de l’application Lync du Windows Store, vous devez activer l’authentification par certificat.</span><span class="sxs-lookup"><span data-stu-id="2a5e8-121">If you will use Lync Windows Store app clients, you must enable certificate authentication.</span></span>



</div>

<span data-ttu-id="2a5e8-122">Pour créer un serveur d’inscriptions avancé, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="2a5e8-122">Follow these steps to create a new Registrar.</span></span>

<div>

## <a name="to-create-new-registrar-configuration-settings"></a><span data-ttu-id="2a5e8-123">Pour créer des paramètres de configuration du serveur d’inscriptions avancé</span><span class="sxs-lookup"><span data-stu-id="2a5e8-123">To create new Registrar configuration settings</span></span>

1.  <span data-ttu-id="2a5e8-124">À partir d’un compte d’utilisateur membre du groupe RTCUniversalServerAdmins (ou doté de droits d’utilisateur équivalents), ou affectées au rôle CsServerAdministrator ou CsAdministrator, connectez-vous à n’importe quel ordinateur se trouve sur le réseau sur lequel vous avez déployé Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="2a5e8-124">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or assigned to the CsServerAdministrator or CsAdministrator role, log on to any computer that is in the network in which you deployed Lync Server 2013.</span></span>

2.  <span data-ttu-id="2a5e8-125">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="2a5e8-125">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="2a5e8-126">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="2a5e8-126">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="2a5e8-127">Dans la barre de navigation de gauche, cliquez sur **Sécurité**, puis sur **Serveur d’inscriptions avancé**.</span><span class="sxs-lookup"><span data-stu-id="2a5e8-127">In the left navigation bar, click **Security** and then click **Registrar**.</span></span>

4.  <span data-ttu-id="2a5e8-128">Dans la page **Serveur d’inscriptions avancé**, cliquez sur **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="2a5e8-128">On the **Registrar** page, click **New**</span></span>

5.  <span data-ttu-id="2a5e8-129">Dans **Sélectionner un service**, cliquez sur le service auquel le serveur d’inscriptions avancé s’appliquera, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="2a5e8-129">In **Select a Service**, click the service to which the Registrar is to be applied and then click **OK**.</span></span>

6.  <span data-ttu-id="2a5e8-130">Dans **Nouveau paramètre de serveur d’inscriptions avancé**, sélectionnez un ou plusieurs des éléments ci-dessous selon les fonctionnalités des clients et la prise en charge de votre environnement :</span><span class="sxs-lookup"><span data-stu-id="2a5e8-130">In **New Registrar Setting**, select one or more of the following depending on the capabilities of the clients and support in your environment:</span></span>
    
      - <span data-ttu-id="2a5e8-131">**Activer l’authentification Kerberos** pour que les serveurs du pool émettent des demandes à l’aide de l’authentification Kerberos.</span><span class="sxs-lookup"><span data-stu-id="2a5e8-131">**Enable Kerberos authentication** to have the servers in the pool issue challenges using Kerberos authentication.</span></span>
    
      - <span data-ttu-id="2a5e8-132">**Activer l’authentification NTLM** pour que les serveurs du pool émettent des demandes à l’aide de l’authentification NTLM.</span><span class="sxs-lookup"><span data-stu-id="2a5e8-132">**Enable NTLM authentication** to have the servers in the pool issue challenges using NTLM.</span></span>
    
      - <span data-ttu-id="2a5e8-133">**Activer l’authentification par certificat** pour que les serveurs du pool émettent des certificats pour les clients.</span><span class="sxs-lookup"><span data-stu-id="2a5e8-133">**Enable certificate authentication** to have the servers in the pool issue certificates to clients.</span></span>

7.  <span data-ttu-id="2a5e8-134">Cliquez sur **Valider**.</span><span class="sxs-lookup"><span data-stu-id="2a5e8-134">Click **Commit**.</span></span>

<span data-ttu-id="2a5e8-135"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2a5e8-135"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

