---
title: 'Lync Server 2013 : créer ou modifier une configuration de partenaire XMPP'
description: 'Lync Server 2013 : création ou modification de la configuration de partenaire XMPP.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or edit XMPP partner configuration
ms:assetid: 362dbe5e-8ee9-4aba-8c26-5907312b4a60
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ552447(v=OCS.15)
ms:contentKeyID: 48679558
ms.date: 09/03/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 19289df1920287984f104bb1bdfa214d6f83f5cf
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431854"
---
# <a name="create-or-edit-xmpp-partner-configuration-in-lync-server-2013"></a><span data-ttu-id="98bd8-103">Créer ou modifier une configuration de partenaire XMPP dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="98bd8-103">Create or edit XMPP partner configuration in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="98bd8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="98bd8-104">

<span> </span></span></span>

<span data-ttu-id="98bd8-105">_**Dernière modification de la rubrique :** 2014-09-03_</span><span class="sxs-lookup"><span data-stu-id="98bd8-105">_**Topic Last Modified:** 2014-09-03_</span></span>

<span data-ttu-id="98bd8-106">Microsoft Lync Server 2013 intègre un proxy XMPP (extensible Messaging and Presence Protocol) sur le serveur Edge et une passerelle XMPP sur le serveur frontal ou le pool frontal.</span><span class="sxs-lookup"><span data-stu-id="98bd8-106">Microsoft Lync Server 2013 integrates an Extensible Messaging and Presence Protocol (XMPP) proxy on the Edge Server and an XMPP Gateway on the Front End Server or Front End pool.</span></span> <span data-ttu-id="98bd8-107">Pour autoriser les connexions à partir de déploiements XMPP, vous devez configurer XMPP dans le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="98bd8-107">To allow connections from other XMPP deployments, you must configure XMPP in the Lync Server Control Panel.</span></span> <span data-ttu-id="98bd8-108">Vous pouvez configurer les paramètres sur la base d’un domaine XMPP.</span><span class="sxs-lookup"><span data-stu-id="98bd8-108">You configure settings on an XMPP domain basis.</span></span> <span data-ttu-id="98bd8-109">Pour créer une association de partenariat, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="98bd8-109">To create a new partner association, you do the following:</span></span>

<div>

## <a name="to-create-a-new-federated-partner-or-edit-an-existing-configuration"></a><span data-ttu-id="98bd8-110">Pour créer un nouveau partenaire fédéré ou modifier une configuration existante</span><span class="sxs-lookup"><span data-stu-id="98bd8-110">To create a new federated partner or edit an existing configuration</span></span>

1.  <span data-ttu-id="98bd8-111">À partir d’un compte d’utilisateur membre du groupe RTCUniversalServerAdmins (ou doté de droits d’utilisateur équivalents), ou affectées au rôle CsAdministrator, connectez-vous à n’importe quel ordinateur dans votre déploiement interne.</span><span class="sxs-lookup"><span data-stu-id="98bd8-111">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="98bd8-112">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="98bd8-112">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="98bd8-113">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="98bd8-113">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="98bd8-114">Dans la barre de navigation de gauche, cliquez sur **Fédération et accès externe**, puis sur **partenaires fédérés de XMPP**.</span><span class="sxs-lookup"><span data-stu-id="98bd8-114">In the left navigation bar, click **Federation and External Access**, and then click **XMPP Federated Partners**.</span></span>

4.  <span data-ttu-id="98bd8-115">Pour créer une nouvelle configuration, cliquez sur **nouveau** .</span><span class="sxs-lookup"><span data-stu-id="98bd8-115">To create a new configuration, click **New**</span></span>

5.  <span data-ttu-id="98bd8-116">Pour modifier une configuration existante, sélectionnez-la, puis cliquez sur **modifier** .</span><span class="sxs-lookup"><span data-stu-id="98bd8-116">To edit an existing configuration, select the configuration and click **Edit**</span></span>

6.  <span data-ttu-id="98bd8-117">Pour créer ou modifier des configurations pour les **partenaires fédérés de XMPP**, vous devez définir les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="98bd8-117">To create or edit configurations for **XMPP Federated Partners**, you define the following settings:</span></span>

7.  <span data-ttu-id="98bd8-118">**Domaine principal** (obligatoire).</span><span class="sxs-lookup"><span data-stu-id="98bd8-118">**Primary domain** (Required).</span></span> <span data-ttu-id="98bd8-119">Le domaine principal est le domaine de base du partenaire XMPP.</span><span class="sxs-lookup"><span data-stu-id="98bd8-119">The primary domain is the base domain of the XMPP partner.</span></span> <span data-ttu-id="98bd8-120">Par exemple, vous devez entrer **fabrikam.com** pour le nom de domaine de partenaire XMPP.</span><span class="sxs-lookup"><span data-stu-id="98bd8-120">For example, you would enter **fabrikam.com** for the XMPP partner domain name.</span></span> <span data-ttu-id="98bd8-121">Il s’agit d’une entrée obligatoire.</span><span class="sxs-lookup"><span data-stu-id="98bd8-121">This is a required entry.</span></span>

8.  <span data-ttu-id="98bd8-122">**Description**.</span><span class="sxs-lookup"><span data-stu-id="98bd8-122">**Description**.</span></span> <span data-ttu-id="98bd8-123">La description est destinée aux notes ou autres informations d’identification pour cette configuration particulière.</span><span class="sxs-lookup"><span data-stu-id="98bd8-123">The description is for notes or other identifying information for this particular configuration.</span></span> <span data-ttu-id="98bd8-124">Cette entrée est facultative.</span><span class="sxs-lookup"><span data-stu-id="98bd8-124">This entry is optional.</span></span>

9.  <span data-ttu-id="98bd8-125">**Domaines supplémentaires**.</span><span class="sxs-lookup"><span data-stu-id="98bd8-125">**Additional domains**.</span></span> <span data-ttu-id="98bd8-126">Les domaines supplémentaires sont des domaines qui font partie du domaine de votre partenaire XMPP qui doivent être inclus dans le cadre de la communication XMPP autorisée.</span><span class="sxs-lookup"><span data-stu-id="98bd8-126">Additional domains are domains that are a part of your XMPP partner’s domain that should be included as part of the allowed XMPP communication.</span></span> <span data-ttu-id="98bd8-127">Par exemple, si le domaine principal est **fabrikam.com**, vous répertoriez tous les autres domaines sous fabrikam.com que vous communiquerez par le biais de la fonction XMPP.</span><span class="sxs-lookup"><span data-stu-id="98bd8-127">For example, if the primary domain is **fabrikam.com**, then you would list all other domains that are under fabrikam.com that you will communicate with by way of XMPP.</span></span> <span data-ttu-id="98bd8-128">Par exemple, vous pouvez entrer **Corp.fabrikam.com** et **it.fabrikam.com** pour le domaine XMPP d’entreprise et le domaine XMPP information technologies dans le domaine XMPP principal de fabrikam. com.</span><span class="sxs-lookup"><span data-stu-id="98bd8-128">For example, you might enter **corp.fabrikam.com** and **it.fabrikam.com** for the Corporate XMPP domain and the Information Technologies XMPP domain under fabrikam.com’s main XMPP domain.</span></span>

10. <span data-ttu-id="98bd8-129">**Type de partenaire**.</span><span class="sxs-lookup"><span data-stu-id="98bd8-129">**Partner type**.</span></span> <span data-ttu-id="98bd8-130">Le **type de partenariat** est un paramètre requis et vous donne accès à trois options dans un menu déroulant.</span><span class="sxs-lookup"><span data-stu-id="98bd8-130">The **Partner type** is a required setting and gives you a selection of three choices in a drop-down menu.</span></span> <span data-ttu-id="98bd8-131">Vous devez choisir l’une des options suivantes pour décrire et mettre en œuvre les contacts qui peuvent être ajoutés.</span><span class="sxs-lookup"><span data-stu-id="98bd8-131">You must choose one of the following to describe and enforce what contacts can be added.</span></span> <span data-ttu-id="98bd8-132">Vous pouvez sélectionner l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="98bd8-132">You can select from:</span></span>
    
      - <span data-ttu-id="98bd8-133">**Federated**.</span><span class="sxs-lookup"><span data-stu-id="98bd8-133">**Federated**.</span></span> <span data-ttu-id="98bd8-134">Un type de partenaire **fédéré** est une connexion de confiance entre un serveur Lync ou un déploiement partenaire d’Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="98bd8-134">A **Federated** partner type is a trusted connection between a Lync Server or Office Communications Server 2007 R2 partner deployment.</span></span>
    
      - <span data-ttu-id="98bd8-135">**Public vérifié**.</span><span class="sxs-lookup"><span data-stu-id="98bd8-135">**Public verified**.</span></span> <span data-ttu-id="98bd8-136">Un partenaire vérifié par le **public** est le moment où les contacts qui font partie d’un déploiement vérifié par le fournisseur peuvent être ajoutés à la liste des contacts de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="98bd8-136">A **Public verified** partner is when contacts that are part of a deployment that are verified by the provider can be added to your user’s list of contacts.</span></span> <span data-ttu-id="98bd8-137">Il est possible d’envoyer des invitations à partir de l’utilisateur Lync ou de l’utilisateur de Lync.</span><span class="sxs-lookup"><span data-stu-id="98bd8-137">Invites can be sent from the Lync user or the Lync user can accept invites from the partner contact.</span></span>
    
      - <span data-ttu-id="98bd8-138">**Public non vérifié**.</span><span class="sxs-lookup"><span data-stu-id="98bd8-138">**Public unverified**.</span></span> <span data-ttu-id="98bd8-139">Une relation **invalidée publique** implique qu’il n’y a aucun État établi et vérifiable entre les deux déploiements.</span><span class="sxs-lookup"><span data-stu-id="98bd8-139">A **Public unverified** relationship implies that there is no established and verifiable status between the two deployments.</span></span> <span data-ttu-id="98bd8-140">Un utilisateur de Lync doit inviter le contact non vérifié à ce contact pour pouvoir l’ajouter à sa liste de contacts.</span><span class="sxs-lookup"><span data-stu-id="98bd8-140">A Lync user must invite the unverified contact for that contact to be able to add the Lync user to his contact list.</span></span> <span data-ttu-id="98bd8-141">Par exemple, Google GTalk n’est pas un service de XMPP vérifié publique en relation avec Lync Server.</span><span class="sxs-lookup"><span data-stu-id="98bd8-141">For example, Google GTalk is not a public verified XMPP service as it relates to Lync Server.</span></span> <span data-ttu-id="98bd8-142">Un utilisateur GTalk ne sera pas en mesure d’ajouter l’utilisateur Lync en tant que contact, sauf s’il y a une invitation explicite envoyée par l’utilisateur Lync.</span><span class="sxs-lookup"><span data-stu-id="98bd8-142">A GTalk user will not be able to add the Lync user as a contact unless there is an explicit invite sent from the Lync user.</span></span>

11. <span data-ttu-id="98bd8-143">Remarques sur la négociation du flux et les méthodes de sécurité Transport Layer Security (TLS) et l’authentification du logiciel et de la couche de sécurité (SASL) :</span><span class="sxs-lookup"><span data-stu-id="98bd8-143">Notes on stream negotiation and the security methods Transport Layer Security (TLS) and Software Authentication and Security Layer (SASL):</span></span>
    
    <span data-ttu-id="98bd8-144">Les **normes** xsf (réseau de base) et l’IETF ( **Internet Engineering Task Force** ) définissent un ensemble de règles et de normes pour l’utilisation et la gestion des certificats clients TLS, des certificats de serveur TLS et du mécanisme SASL.</span><span class="sxs-lookup"><span data-stu-id="98bd8-144">The **XMPP Standards Foundation** (XSF) and the **Internet Engineering Task Force** (IETF) define a set of rules and standards for using and managing TLS client certificates, TLS server certificates, and the SASL mechanism.</span></span> <span data-ttu-id="98bd8-145">L’utilisation de TLS et de SASL est le processus requis pour sécuriser le flux XMPP.</span><span class="sxs-lookup"><span data-stu-id="98bd8-145">Using TLS and SASL is the required process for securing the XMPP stream.</span></span> <span data-ttu-id="98bd8-146">À partir de la norme XMPP document **XEP-0178**, "spécifie un flux de protocoles recommandé pour l’utilisation du mécanisme externe SASL avec des certificats PKIX, en particulier quand un service XMPP indique que le protocole TLS est requis pour négocier.»</span><span class="sxs-lookup"><span data-stu-id="98bd8-146">From the XMPP Standards document **XEP-0178**, “specifies a recommended protocol flow for use of the SASL EXTERNAL mechanism with PKIX certificates, especially when an XMPP service indicates that TLS is mandatory-to-negotiate.”</span></span> <span data-ttu-id="98bd8-147">PKIX, comme indiqué dans la documentation XSF, fait référence à l’infrastructure à clé publique (PKI).</span><span class="sxs-lookup"><span data-stu-id="98bd8-147">PKIX, as stated in the XSF documentation, refers to public key infrastructure, also known as PKI.</span></span>
    
    <span data-ttu-id="98bd8-148">Pour plus d’informations sur les exigences XMPP, voir le document XSF XEP-0178.</span><span class="sxs-lookup"><span data-stu-id="98bd8-148">Refer to the XSF document XEP-0178 for more details on the XMPP requirements.</span></span> <span data-ttu-id="98bd8-149">Pour plus d’informations, reportez-vous à la rubrique « XEP-0178 : meilleures pratiques pour l’utilisation de SASL en externe avec des certificats ».</span><span class="sxs-lookup"><span data-stu-id="98bd8-149">For details, refer to “XEP-0178: Best Practices for Use of SASL EXTERNAL with Certificates”.</span></span> <http://xmpp.org/extensions/xep-0178.html>
    
    <span data-ttu-id="98bd8-150">Reportez-vous au document IETF « extensible Messaging and Presence Protocol » (XMPP) : Core», section 5,0 <https://tools.ietf.org/html/rfc6120> , négociation de STARTTLS</span><span class="sxs-lookup"><span data-stu-id="98bd8-150">Refer to the IETF document “Extensible Messaging and Presence Protocol (XMPP): Core“, Section 5.0, STARTTLS Negotiation <https://tools.ietf.org/html/rfc6120>.</span></span>
    
      - <span data-ttu-id="98bd8-151">**Négociation TLS**.</span><span class="sxs-lookup"><span data-stu-id="98bd8-151">**TLS Negotiation**.</span></span> <span data-ttu-id="98bd8-152">Définit les règles de négociation TLS.</span><span class="sxs-lookup"><span data-stu-id="98bd8-152">Defines the TLS negotiation rules.</span></span> <span data-ttu-id="98bd8-153">Un service XMPP peut nécessiter le protocole TLS, peut rendre TLS facultatif ou vous définissez que TLS n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="98bd8-153">An XMPP service can require TLS, can make TLS optional, or you define that TLS is not supported.</span></span> <span data-ttu-id="98bd8-154">Le choix de l’option facultative quitte le service XMPP pour une décision de demande obligatoire.</span><span class="sxs-lookup"><span data-stu-id="98bd8-154">Choosing Optional leaves the requirement up to the XMPP service for a mandatory-to-negotiate decision.</span></span> <span data-ttu-id="98bd8-155">Pour afficher tous les paramètres et détails possibles relatifs aux négociations SASL, TLS et Dialback, y compris les configurations d’erreur non valides et connues, voir [paramètres de négociation des partenaires fédérés de XMPP dans Lync Server 2013](lync-server-2013-negotiation-settings-for-xmpp-federated-partners.md).</span><span class="sxs-lookup"><span data-stu-id="98bd8-155">To view all possible settings and details for SASL, TLS and Dialback negotiation –including not valid and known error configurations - see [Negotiation settings for XMPP federated partners in Lync Server 2013](lync-server-2013-negotiation-settings-for-xmpp-federated-partners.md).</span></span>
        
          - <span></span>  
            <span data-ttu-id="98bd8-156">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="98bd8-156">**Required**.</span></span> <span data-ttu-id="98bd8-157">Le service XMPP nécessite une négociation TLS.</span><span class="sxs-lookup"><span data-stu-id="98bd8-157">The XMPP service requires TLS negotiation.</span></span>
        
          - <span></span>  
            <span data-ttu-id="98bd8-158">**Facultatif**.</span><span class="sxs-lookup"><span data-stu-id="98bd8-158">**Optional**.</span></span> <span data-ttu-id="98bd8-159">Le service XMPP indique que TLS est requis pour négocier.</span><span class="sxs-lookup"><span data-stu-id="98bd8-159">The XMPP service indicates that TLS is mandatory-to-negotiate.</span></span>
        
          - <span></span>  
            <span data-ttu-id="98bd8-160">**Non pris en charge**.</span><span class="sxs-lookup"><span data-stu-id="98bd8-160">**Not Supported**.</span></span> <span data-ttu-id="98bd8-161">Le service XMPP ne prend pas en charge le protocole TLS.</span><span class="sxs-lookup"><span data-stu-id="98bd8-161">The XMPP service does not support TLS.</span></span>
    
      - <span data-ttu-id="98bd8-162">**Négociation SASL**.</span><span class="sxs-lookup"><span data-stu-id="98bd8-162">**SASL negotiation**.</span></span> <span data-ttu-id="98bd8-163">Définit les règles de négociation SASL.</span><span class="sxs-lookup"><span data-stu-id="98bd8-163">Defines the SASL negotiation rules.</span></span> <span data-ttu-id="98bd8-164">Un service XMPP peut être requis pour rendre SASL une option de SASL, ou vous définissez que SASL n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="98bd8-164">An XMPP service can require SASL, can make SASL optional, or you define that SASL is not supported.</span></span> <span data-ttu-id="98bd8-165">Le choix facultatif pour une décision d’obligation de négociation est requis par le service XMPP du partenaire.</span><span class="sxs-lookup"><span data-stu-id="98bd8-165">Choosing Optional leaves the requirement up to the partner XMPP service for a mandatory-to-negotiate decision.</span></span>
        
        <div>
        

        > [!WARNING]  
        > <span data-ttu-id="98bd8-166">SASL nécessite le protocole TLS.</span><span class="sxs-lookup"><span data-stu-id="98bd8-166">SASL requires TLS.</span></span> <span data-ttu-id="98bd8-167">Pour utiliser SASL, TLS doit obligatoirement être requis ou facultatif.</span><span class="sxs-lookup"><span data-stu-id="98bd8-167">To use SASL, TLS must either be required or optional.</span></span> <span data-ttu-id="98bd8-168">Toute configuration qui définit SASL comme étant obligatoire ou facultative doit disposer d’une prise en charge de TLS.</span><span class="sxs-lookup"><span data-stu-id="98bd8-168">Any configuration that defines SASL as either required or optional must have TLS support.</span></span> <span data-ttu-id="98bd8-169">Lorsque vous cliquez sur <STRONG>valider</STRONG> pour enregistrer vos modifications, si vous n’avez pas configuré TLS sur obligatoire ou facultatif, vous êtes averti que SASL doit prendre en charge le protocole TLS et que vos modifications ne sont pas enregistrées.</span><span class="sxs-lookup"><span data-stu-id="98bd8-169">When clicking <STRONG>Commit</STRONG> to save your changes, if you have not set TLS to required or optional, you will be warned that SASL must have TLS support and your changes are not saved.</span></span> <span data-ttu-id="98bd8-170">Pour résoudre ce problème, définissez TLS sur <STRONG>obligatoire</STRONG> ou <STRONG>facultatif</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="98bd8-170">To resolve the error, set TLS to <STRONG>Required</STRONG> or <STRONG>Optional</STRONG>.</span></span> <span data-ttu-id="98bd8-171">Si l’utilisation de SASL est en option et si la prise en charge de la négociation TLS n’est pas possible, vous devez définir la négociation SASL sur <STRONG>non prise en charge</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="98bd8-171">If use of SASL is optional and TLS negotiation support is not possible, you must set SASL negotiation to <STRONG>Not Supported</STRONG>.</span></span> <span data-ttu-id="98bd8-172">Confirmez avec le service XMPP quels sont les flux de négociation appropriés pour TLS et SASL ou le service d’interruption de service.</span><span class="sxs-lookup"><span data-stu-id="98bd8-172">Confirm with the XMPP service what the proper negotiation streams must be for TLS and SASL or service interruption will occur.</span></span>

        
        </div>
        
          - <span></span>  
            <span data-ttu-id="98bd8-173">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="98bd8-173">**Required**.</span></span> <span data-ttu-id="98bd8-174">Le service XMPP nécessite une négociation SASL.</span><span class="sxs-lookup"><span data-stu-id="98bd8-174">The XMPP service requires SASL negotiation.</span></span>
        
          - <span></span>  
            <span data-ttu-id="98bd8-175">**Facultatif**.</span><span class="sxs-lookup"><span data-stu-id="98bd8-175">**Optional**.</span></span> <span data-ttu-id="98bd8-176">Le service XMPP indique que SASL est requis pour négocier.</span><span class="sxs-lookup"><span data-stu-id="98bd8-176">The XMPP service indicates that SASL is mandatory-to-negotiate.</span></span>
        
          - <span></span>  
            <span data-ttu-id="98bd8-177">**Non pris en charge**.</span><span class="sxs-lookup"><span data-stu-id="98bd8-177">**Not Supported**.</span></span> <span data-ttu-id="98bd8-178">Le service XMPP ne prend pas en charge SASL.</span><span class="sxs-lookup"><span data-stu-id="98bd8-178">The XMPP service does not support SASL.</span></span>
    
      - <span data-ttu-id="98bd8-179">**Négociation Dialback**.</span><span class="sxs-lookup"><span data-stu-id="98bd8-179">**Dialback negotiation**.</span></span> <span data-ttu-id="98bd8-180">Dialback négociation est définie par le fichier XSF dans document **XEP-220 : Server Dialback** <http://xmpp.org/extensions/xep-0220.html> .</span><span class="sxs-lookup"><span data-stu-id="98bd8-180">Dialback negotiation is defined by the XSF in document **XEP-220 : Server Dialback** <http://xmpp.org/extensions/xep-0220.html>.</span></span> <span data-ttu-id="98bd8-181">Le processus de dialback serveur utilise le DNS (Domain Name System) et un serveur faisant autorité pour vérifier que la requête provient d’un partenaire XMPP valide.</span><span class="sxs-lookup"><span data-stu-id="98bd8-181">The server dialback process uses the domain name system (DNS) and an authoritative server to verify that the request came from a valid XMPP partner.</span></span> <span data-ttu-id="98bd8-182">Pour ce faire, le serveur d’origine crée un message d’un type spécifique avec une clé dialback générée et recherche le serveur de réception dans DNS.</span><span class="sxs-lookup"><span data-stu-id="98bd8-182">To do this, the originating server creates a message of a specific type with a generated dialback key and looks up the receiving server in DNS.</span></span> <span data-ttu-id="98bd8-183">Le serveur d’origine envoie la clé dans un flux XML à la recherche DNS résultante, le serveur de réception en principe.</span><span class="sxs-lookup"><span data-stu-id="98bd8-183">The originating server sends the key in an XML stream to the resulting DNS lookup, presumably the receiving server.</span></span> <span data-ttu-id="98bd8-184">Dès réception de la clé via le flux XML, le serveur de réception ne répond pas au serveur d’origine, mais envoie la clé à un serveur faisant autorité connu.</span><span class="sxs-lookup"><span data-stu-id="98bd8-184">On receipt of the key over the XML stream, the receiving server does not respond to the originating server, but sends the key to a known authoritative server.</span></span> <span data-ttu-id="98bd8-185">Le serveur faisant autorité vérifie que la clé est valide ou n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="98bd8-185">The authoritative server verifies that the key is either valid or not valid.</span></span> <span data-ttu-id="98bd8-186">Si ce n’est pas le cas, le serveur de réception ne répond pas au serveur d’origine.</span><span class="sxs-lookup"><span data-stu-id="98bd8-186">If not valid, the receiving server does not respond to the originating server.</span></span> <span data-ttu-id="98bd8-187">Si la clé est valide, le serveur de réception informe le serveur d’origine qu’elle est valide et qu’elle peut commencer.</span><span class="sxs-lookup"><span data-stu-id="98bd8-187">If the key is valid, the receiving server informs the originating server that the identity and key is valid and the conversation can commence.</span></span>
        
        <span data-ttu-id="98bd8-188">Il existe deux États valides pour la **négociation Dialback**:</span><span class="sxs-lookup"><span data-stu-id="98bd8-188">There are two valid states for **Dialback negotiation**:</span></span>
        
          - <span></span>  
            <span data-ttu-id="98bd8-189">**True**.</span><span class="sxs-lookup"><span data-stu-id="98bd8-189">**True**.</span></span> <span data-ttu-id="98bd8-190">Le serveur XMPP est configuré pour utiliser la négociation Dialback si une requête doit être reçue d’un serveur d’origine.</span><span class="sxs-lookup"><span data-stu-id="98bd8-190">The XMPP server is configured to use Dialback negotiation if a request should be received from an originating server</span></span>
        
          - <span></span>  
            <span data-ttu-id="98bd8-191">**False**.</span><span class="sxs-lookup"><span data-stu-id="98bd8-191">**False**.</span></span> <span data-ttu-id="98bd8-192">Le serveur XMPP n’est pas configuré pour utiliser la négociation Dialback et, si une requête doit être reçue d’un serveur d’origine, il est ignoré.</span><span class="sxs-lookup"><span data-stu-id="98bd8-192">The XMPP server is not configured to use Dialback negotiation and if a request should be received from an originating server, it will be ignored</span></span>

<span data-ttu-id="98bd8-193"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="98bd8-193"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

