---
title: 'Lync Server 2013 : Paramètres de négociation pour les partenaires fédérés XMPP'
description: 'Lync Server 2013 : paramètres de négociation pour les partenaires fédérés de XMPP.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Negotiation settings for XMPP federated partners
ms:assetid: ef773942-ef92-4f71-85a1-738dfebdfa00
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ552456(v=OCS.15)
ms:contentKeyID: 48679567
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6ac3d9c69d407dc750a1afb35f0a448869a88f09
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445584"
---
# <a name="negotiation-settings-for-xmpp-federated-partners-in-lync-server-2013"></a><span data-ttu-id="636a5-103">Paramètres de négociation pour les partenaires fédérés XMPP dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="636a5-103">Negotiation settings for XMPP federated partners in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="636a5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="636a5-104">

<span> </span></span></span>

<span data-ttu-id="636a5-105">_**Dernière modification de la rubrique :** 2012-10-21_</span><span class="sxs-lookup"><span data-stu-id="636a5-105">_**Topic Last Modified:** 2012-10-21_</span></span>

<span data-ttu-id="636a5-106">Les paramètres des types de négociations dans la configuration d’un partenaire XMPP possèdent une large gamme de combinaisons possibles.</span><span class="sxs-lookup"><span data-stu-id="636a5-106">The settings for the negotiation types in the configuration of an XMPP Partner have a wide variety of possible combinations.</span></span> <span data-ttu-id="636a5-107">Toutes ces combinaisons ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="636a5-107">Not all of these combinations are valid.</span></span> <span data-ttu-id="636a5-108">Le tableau décrit dans cette rubrique définit les paramètres valides et non valides.</span><span class="sxs-lookup"><span data-stu-id="636a5-108">The table detailed in this topic will define the valid and not valid settings.</span></span> <span data-ttu-id="636a5-109">Les configurations courantes sont présentées dans la première table, la deuxième table présentant toutes les combinaisons possibles.</span><span class="sxs-lookup"><span data-stu-id="636a5-109">Common configurations are presented in the first table, the second table detailing all possible combinations.</span></span> <span data-ttu-id="636a5-110">Notez que vous ne pouvez pas utiliser *l’authentification simple et la couche de sécurité* (SASL) **, sauf si** le protocole TLS ( *Transport Layer Security* ) est également disponible.</span><span class="sxs-lookup"><span data-stu-id="636a5-110">Note that you cannot have *Simple Authentication and Security Layer* (SASL) **unless** *Transport Layer Security* (TLS) is also available.</span></span> <span data-ttu-id="636a5-111">SASL est envoyé dans un format non chiffré (lisible) et ne doit jamais être transmis tant qu’il est protégé par un autre moyen, tel que TLS.</span><span class="sxs-lookup"><span data-stu-id="636a5-111">SASL is sent in an unencrypted (readable) format and should never be transmitted unless protected by another means, such as TLS.</span></span>

### <a name="common-xmpp-federation-negotiation-methods"></a><span data-ttu-id="636a5-112">Méthodes courantes de négociation de Fédération XMPP</span><span class="sxs-lookup"><span data-stu-id="636a5-112">Common XMPP Federation Negotiation Methods</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="636a5-113">TLS (Transport Layer Security)</span><span class="sxs-lookup"><span data-stu-id="636a5-113">Transport Layer Security (TLS)</span></span></th>
<th><span data-ttu-id="636a5-114">Authentification simple et couche de sécurité (SASL)</span><span class="sxs-lookup"><span data-stu-id="636a5-114">Simple Authentication and Security Layer (SASL)</span></span></th>
<th><span data-ttu-id="636a5-115">Authentification Dialback</span><span class="sxs-lookup"><span data-stu-id="636a5-115">Dialback Authentication</span></span></th>
<th><span data-ttu-id="636a5-116">Méthode (s) d’authentification attendue</span><span class="sxs-lookup"><span data-stu-id="636a5-116">Expected Authentication Method(s)</span></span></th>
<th><span data-ttu-id="636a5-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="636a5-117">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="636a5-118">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="636a5-118">Required</span></span></p></td>
<td><p><span data-ttu-id="636a5-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="636a5-119">Required</span></span></p></td>
<td><p><span data-ttu-id="636a5-120">False</span><span class="sxs-lookup"><span data-stu-id="636a5-120">False</span></span></p></td>
<td><p><span data-ttu-id="636a5-121">SASL via TLS</span><span class="sxs-lookup"><span data-stu-id="636a5-121">SASL over TLS</span></span></p></td>
<td><p><span data-ttu-id="636a5-122">TLS et SASL requis permettent de s’assurer que le flux de messages SASL est sécurisé.</span><span class="sxs-lookup"><span data-stu-id="636a5-122">TLS and SASL required helps to ensure that the SASL message stream is secure.</span></span> <span data-ttu-id="636a5-123">Dialback n’est pas disponible et ne peut pas être utilisé pour une méthode de secours si le partenaire fédéré de XMPP n’a pas configuré TLS sur requis ou facultatif.</span><span class="sxs-lookup"><span data-stu-id="636a5-123">Dialback is not available and cannot be used for a fallback method if the XMPP federated partner has not set TLS to required or optional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="636a5-124">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="636a5-124">Required</span></span></p></td>
<td><p><span data-ttu-id="636a5-125">Facultatif</span><span class="sxs-lookup"><span data-stu-id="636a5-125">Optional</span></span></p></td>
<td><p><span data-ttu-id="636a5-126">Vrai</span><span class="sxs-lookup"><span data-stu-id="636a5-126">True</span></span></p></td>
<td><p><span data-ttu-id="636a5-127">SASL via TLS, TLS Dialback, TCP Dialback</span><span class="sxs-lookup"><span data-stu-id="636a5-127">SASL over TLS, TLS Dialback, TCP Dialback</span></span></p></td>
<td><p><span data-ttu-id="636a5-128">Par le biais du protocole TLS, si le partenaire fédéré XMPP a défini SASL sur l’option Optional ou Required SASL est utilisé.</span><span class="sxs-lookup"><span data-stu-id="636a5-128">By requiring TLS, if the XMPP federated partner has set SASL to optional or required SASL is used.</span></span> <span data-ttu-id="636a5-129">Si SASL n’est pas disponible, Dialback sur TLS sera utilisé.</span><span class="sxs-lookup"><span data-stu-id="636a5-129">If SASL is not available, Dialback over TLS will be used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="636a5-130">Facultatif </span><span class="sxs-lookup"><span data-stu-id="636a5-130">Optional</span></span></p></td>
<td><p><span data-ttu-id="636a5-131">Facultatif</span><span class="sxs-lookup"><span data-stu-id="636a5-131">Optional</span></span></p></td>
<td><p><span data-ttu-id="636a5-132">Vrai</span><span class="sxs-lookup"><span data-stu-id="636a5-132">True</span></span></p></td>
<td><p><span data-ttu-id="636a5-133">SASL via TLS, TLS Dialback, TCP Dialback</span><span class="sxs-lookup"><span data-stu-id="636a5-133">SASL over TLS, TLS Dialback, TCP Dialback</span></span></p></td>
<td><p><span data-ttu-id="636a5-134">S’ils sont très flexibles dans les méthodes de négociation proposées, ces paramètres dépendent des paramètres du partenaire de Fédération XMPP.</span><span class="sxs-lookup"><span data-stu-id="636a5-134">While very flexible in the negotiation methods offered, these settings rely on the XMPP federation partner’s settings.</span></span> <span data-ttu-id="636a5-135">Si les protocoles TLS sont facultatifs ou requis alors que SASL n’est pas pris en charge, les Dialback TLS seront disponibles.</span><span class="sxs-lookup"><span data-stu-id="636a5-135">If the partner has TLS optional or required but SASL is not supported, TLS Dialback will be available.</span></span> <span data-ttu-id="636a5-136">Si le partenaire utilise les protocoles TLS et SASL définis sur facultatif ou requis, la sélection optimale de TLS sur SASL est utilisée.</span><span class="sxs-lookup"><span data-stu-id="636a5-136">If the partner has TLS and SASL set to optional or required, the optimal selection of TLS over SASL is used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="636a5-137">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="636a5-137">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="636a5-138">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="636a5-138">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="636a5-139">Vrai</span><span class="sxs-lookup"><span data-stu-id="636a5-139">True</span></span></p></td>
<td><p><span data-ttu-id="636a5-140">TCP Dialback</span><span class="sxs-lookup"><span data-stu-id="636a5-140">TCP Dialback</span></span></p></td>
<td><p><span data-ttu-id="636a5-141">Dans de nombreux cas, TCP Dialback est la seule solution possible.</span><span class="sxs-lookup"><span data-stu-id="636a5-141">In many cases, TCP Dialback is the only possible solution.</span></span> <span data-ttu-id="636a5-142">Moins désirable que d’autres options, il fournit un certain niveau de confiance.</span><span class="sxs-lookup"><span data-stu-id="636a5-142">Less desirable than other options, it does provide some level of trust.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="xmpp-federation-negotiation-methods-matrix---complete"></a><span data-ttu-id="636a5-143">Matrice des méthodes de négociation de Fédération XMPP-complet</span><span class="sxs-lookup"><span data-stu-id="636a5-143">XMPP Federation Negotiation Methods Matrix - Complete</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="636a5-144">TLS (Transport Layer Security)</span><span class="sxs-lookup"><span data-stu-id="636a5-144">Transport Layer Security (TLS)</span></span></th>
<th><span data-ttu-id="636a5-145">Authentification simple et couche de sécurité (SASL)</span><span class="sxs-lookup"><span data-stu-id="636a5-145">Simple Authentication and Security Layer (SASL)</span></span></th>
<th><span data-ttu-id="636a5-146">Authentification Dialback</span><span class="sxs-lookup"><span data-stu-id="636a5-146">Dialback Authentication</span></span></th>
<th><span data-ttu-id="636a5-147">Méthode d’authentification attendue</span><span class="sxs-lookup"><span data-stu-id="636a5-147">Expected Authentication Method</span></span></th>
<th><span data-ttu-id="636a5-148">Remarques, avertissement ou erreur pour une configuration incorrecte</span><span class="sxs-lookup"><span data-stu-id="636a5-148">Notes, Warning or Error for Not Valid Configuration</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="636a5-149">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="636a5-149">Required</span></span></p></td>
<td><p><span data-ttu-id="636a5-150">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="636a5-150">Required</span></span></p></td>
<td><p><span data-ttu-id="636a5-151">Vrai</span><span class="sxs-lookup"><span data-stu-id="636a5-151">True</span></span></p></td>
<td><p><span data-ttu-id="636a5-152">SASL via TLS</span><span class="sxs-lookup"><span data-stu-id="636a5-152">SASL over TLS</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="636a5-153">Dialback ne fonctionnera pas si les protocoles SASL et TLS sont requis.</span><span class="sxs-lookup"><span data-stu-id="636a5-153">Dialback will not operate if both SASL and TLS are required.</span></span>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="636a5-154">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="636a5-154">Required</span></span></p></td>
<td><p><span data-ttu-id="636a5-155">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="636a5-155">Required</span></span></p></td>
<td><p><span data-ttu-id="636a5-156">False</span><span class="sxs-lookup"><span data-stu-id="636a5-156">False</span></span></p></td>
<td><p><span data-ttu-id="636a5-157">SASL via TLS</span><span class="sxs-lookup"><span data-stu-id="636a5-157">SASL over TLS</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="636a5-158">Facultatif</span><span class="sxs-lookup"><span data-stu-id="636a5-158">Optional</span></span></p></td>
<td><p><span data-ttu-id="636a5-159">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="636a5-159">Required</span></span></p></td>
<td><p><span data-ttu-id="636a5-160">Vrai</span><span class="sxs-lookup"><span data-stu-id="636a5-160">True</span></span></p></td>
<td><p><span data-ttu-id="636a5-161">SASL via TLS, TLS Dialback, TCP Dialback</span><span class="sxs-lookup"><span data-stu-id="636a5-161">SASL over TLS, TLS Dialback, TCP Dialback</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="636a5-162">SASL nécessite le protocole TLS.</span><span class="sxs-lookup"><span data-stu-id="636a5-162">SASL requires TLS.</span></span> <span data-ttu-id="636a5-163">L’autorisation d’une connexion de TLS pouvant être facultative risque de provoquer des négociations de session en échec.</span><span class="sxs-lookup"><span data-stu-id="636a5-163">Allowing TLS to be optional may result in failed session negotiations.</span></span>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="636a5-164">Facultatif</span><span class="sxs-lookup"><span data-stu-id="636a5-164">Optional</span></span></p></td>
<td><p><span data-ttu-id="636a5-165">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="636a5-165">Required</span></span></p></td>
<td><p><span data-ttu-id="636a5-166">False</span><span class="sxs-lookup"><span data-stu-id="636a5-166">False</span></span></p></td>
<td><p><span data-ttu-id="636a5-167">SASL via TLS</span><span class="sxs-lookup"><span data-stu-id="636a5-167">SASL over TLS</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="636a5-168">SASL nécessite le protocole TLS.</span><span class="sxs-lookup"><span data-stu-id="636a5-168">SASL requires TLS.</span></span> <span data-ttu-id="636a5-169">L’autorisation d’une connexion de TLS pouvant être facultative risque de provoquer des négociations de session en échec.</span><span class="sxs-lookup"><span data-stu-id="636a5-169">Allowing TLS to be optional may result in failed session negotiations.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="636a5-170">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="636a5-170">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="636a5-171">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="636a5-171">Required</span></span></p></td>
<td><p><span data-ttu-id="636a5-172">Vrai</span><span class="sxs-lookup"><span data-stu-id="636a5-172">True</span></span></p></td>
<td><p><span data-ttu-id="636a5-173">TCP Dialback</span><span class="sxs-lookup"><span data-stu-id="636a5-173">TCP Dialback</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="636a5-174">SASL nécessite le protocole TLS.</span><span class="sxs-lookup"><span data-stu-id="636a5-174">SASL requires TLS.</span></span> <span data-ttu-id="636a5-175">L’autorisation d’une connexion de TLS pouvant être facultative risque de provoquer des négociations de session en échec.</span><span class="sxs-lookup"><span data-stu-id="636a5-175">Allowing TLS to be optional may result in failed session negotiations.</span></span>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="636a5-176">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="636a5-176">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="636a5-177">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="636a5-177">Required</span></span></p></td>
<td><p><span data-ttu-id="636a5-178">False</span><span class="sxs-lookup"><span data-stu-id="636a5-178">False</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="636a5-179">Configuration non valide</span><span class="sxs-lookup"><span data-stu-id="636a5-179">Not Valid Configuration</span></span>


</div></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="636a5-180">Dans la mesure où SASL nécessite le protocole TLS et que TLS n’est pas disponible, la fonctionnalité SASL/TLS ne peut pas aboutir.</span><span class="sxs-lookup"><span data-stu-id="636a5-180">Because SASL requires TLS, and TLS is not available, SASL/TLS cannot succeed.</span></span> <span data-ttu-id="636a5-181">TCP Dialback est défini sur false et ne peut pas être utilisé.</span><span class="sxs-lookup"><span data-stu-id="636a5-181">TCP Dialback is set to false, and cannot be used.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="636a5-182">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="636a5-182">Required</span></span></p></td>
<td><p><span data-ttu-id="636a5-183">Facultatif</span><span class="sxs-lookup"><span data-stu-id="636a5-183">Optional</span></span></p></td>
<td><p><span data-ttu-id="636a5-184">Vrai</span><span class="sxs-lookup"><span data-stu-id="636a5-184">True</span></span></p></td>
<td><p><span data-ttu-id="636a5-185">SASL via TLS, TLS Dialback</span><span class="sxs-lookup"><span data-stu-id="636a5-185">SASL over TLS, TLS Dialback</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="636a5-186">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="636a5-186">Required</span></span></p></td>
<td><p><span data-ttu-id="636a5-187">Facultatif</span><span class="sxs-lookup"><span data-stu-id="636a5-187">Optional</span></span></p></td>
<td><p><span data-ttu-id="636a5-188">False</span><span class="sxs-lookup"><span data-stu-id="636a5-188">False</span></span></p></td>
<td><p><span data-ttu-id="636a5-189">SASL via TLS</span><span class="sxs-lookup"><span data-stu-id="636a5-189">SASL over TLS</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="636a5-190">Facultatif </span><span class="sxs-lookup"><span data-stu-id="636a5-190">Optional</span></span></p></td>
<td><p><span data-ttu-id="636a5-191">Facultatif</span><span class="sxs-lookup"><span data-stu-id="636a5-191">Optional</span></span></p></td>
<td><p><span data-ttu-id="636a5-192">Vrai</span><span class="sxs-lookup"><span data-stu-id="636a5-192">True</span></span></p></td>
<td><p><span data-ttu-id="636a5-193">SASL via TLS, TLS Dialback, TCP Dialback</span><span class="sxs-lookup"><span data-stu-id="636a5-193">SASL over TLS, TLS Dialback, TCP Dialback</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="636a5-194">SASL nécessite le protocole TLS.</span><span class="sxs-lookup"><span data-stu-id="636a5-194">SASL requires TLS.</span></span> <span data-ttu-id="636a5-195">L’autorisation d’une connexion de TLS pouvant être facultative risque de provoquer des négociations de session en échec.</span><span class="sxs-lookup"><span data-stu-id="636a5-195">Allowing TLS to be optional may result in failed session negotiations.</span></span>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="636a5-196">Facultatif </span><span class="sxs-lookup"><span data-stu-id="636a5-196">Optional</span></span></p></td>
<td><p><span data-ttu-id="636a5-197">Facultatif</span><span class="sxs-lookup"><span data-stu-id="636a5-197">Optional</span></span></p></td>
<td><p><span data-ttu-id="636a5-198">False</span><span class="sxs-lookup"><span data-stu-id="636a5-198">False</span></span></p></td>
<td><p><span data-ttu-id="636a5-199">SASL via TLS</span><span class="sxs-lookup"><span data-stu-id="636a5-199">SASL over TLS</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="636a5-200">SASL nécessite le protocole TLS.</span><span class="sxs-lookup"><span data-stu-id="636a5-200">SASL requires TLS.</span></span> <span data-ttu-id="636a5-201">L’autorisation d’une connexion de TLS pouvant être facultative risque de provoquer des négociations de session en échec.</span><span class="sxs-lookup"><span data-stu-id="636a5-201">Allowing TLS to be optional may result in failed session negotiations.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="636a5-202">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="636a5-202">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="636a5-203">Facultatif</span><span class="sxs-lookup"><span data-stu-id="636a5-203">Optional</span></span></p></td>
<td><p><span data-ttu-id="636a5-204">Vrai</span><span class="sxs-lookup"><span data-stu-id="636a5-204">True</span></span></p></td>
<td><p><span data-ttu-id="636a5-205">TCP Dialback</span><span class="sxs-lookup"><span data-stu-id="636a5-205">TCP Dialback</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="636a5-206">SASL nécessite le protocole TLS.</span><span class="sxs-lookup"><span data-stu-id="636a5-206">SASL requires TLS.</span></span> <span data-ttu-id="636a5-207">L’autorisation d’une connexion de TLS pouvant être facultative risque de provoquer des négociations de session en échec.</span><span class="sxs-lookup"><span data-stu-id="636a5-207">Allowing TLS to be optional may result in failed session negotiations.</span></span>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="636a5-208">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="636a5-208">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="636a5-209">Facultatif</span><span class="sxs-lookup"><span data-stu-id="636a5-209">Optional</span></span></p></td>
<td><p><span data-ttu-id="636a5-210">False</span><span class="sxs-lookup"><span data-stu-id="636a5-210">False</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="636a5-211">Configuration non valide</span><span class="sxs-lookup"><span data-stu-id="636a5-211">Not Valid Configuration</span></span>


</div></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="636a5-212">SASL nécessite le protocole TLS.</span><span class="sxs-lookup"><span data-stu-id="636a5-212">SASL requires TLS.</span></span> <span data-ttu-id="636a5-213">L’autorisation d’une connexion de TLS pouvant être facultative risque de provoquer des négociations de session en échec.</span><span class="sxs-lookup"><span data-stu-id="636a5-213">Allowing TLS to be optional may result in failed session negotiations.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="636a5-214">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="636a5-214">Required</span></span></p></td>
<td><p><span data-ttu-id="636a5-215">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="636a5-215">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="636a5-216">Vrai</span><span class="sxs-lookup"><span data-stu-id="636a5-216">True</span></span></p></td>
<td><p><span data-ttu-id="636a5-217">Dialback TLS</span><span class="sxs-lookup"><span data-stu-id="636a5-217">TLS Dialback</span></span></p></td>
<td><p><span data-ttu-id="636a5-218">La configuration autorise Dialback TLS.</span><span class="sxs-lookup"><span data-stu-id="636a5-218">Configuration allows for TLS Dialback.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="636a5-219">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="636a5-219">Required</span></span></p></td>
<td><p><span data-ttu-id="636a5-220">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="636a5-220">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="636a5-221">False</span><span class="sxs-lookup"><span data-stu-id="636a5-221">False</span></span></p></td>
<td><p><span data-ttu-id="636a5-222">Configuration non valide</span><span class="sxs-lookup"><span data-stu-id="636a5-222">Not Valid Configuration</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="636a5-223">SASL ou Dialback doit être activé.</span><span class="sxs-lookup"><span data-stu-id="636a5-223">SASL or Dialback must be enabled.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="636a5-224">Facultatif</span><span class="sxs-lookup"><span data-stu-id="636a5-224">Optional</span></span></p></td>
<td><p><span data-ttu-id="636a5-225">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="636a5-225">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="636a5-226">Vrai</span><span class="sxs-lookup"><span data-stu-id="636a5-226">True</span></span></p></td>
<td><p><span data-ttu-id="636a5-227">Dialback TLS, TCP Dialback</span><span class="sxs-lookup"><span data-stu-id="636a5-227">TLS Dialback, TCP Dialback</span></span></p></td>
<td><p><span data-ttu-id="636a5-228">En fonction des choix de négociation des autres points de terminaison, les protocoles TCP ou TLS Dialback seront acceptés.</span><span class="sxs-lookup"><span data-stu-id="636a5-228">Based on negotiation choices of the other end point, TCP or TLS Dialback will be accepted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="636a5-229">Facultatif</span><span class="sxs-lookup"><span data-stu-id="636a5-229">Optional</span></span></p></td>
<td><p><span data-ttu-id="636a5-230">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="636a5-230">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="636a5-231">False</span><span class="sxs-lookup"><span data-stu-id="636a5-231">False</span></span></p></td>
<td><p><span data-ttu-id="636a5-232">Configuration non valide</span><span class="sxs-lookup"><span data-stu-id="636a5-232">Not Valid Configuration</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="636a5-233">SASL ou Dialback doit être activé.</span><span class="sxs-lookup"><span data-stu-id="636a5-233">SASL or Dialback must be enabled.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="636a5-234">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="636a5-234">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="636a5-235">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="636a5-235">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="636a5-236">Vrai</span><span class="sxs-lookup"><span data-stu-id="636a5-236">True</span></span></p></td>
<td><p><span data-ttu-id="636a5-237">TCP Dialback</span><span class="sxs-lookup"><span data-stu-id="636a5-237">TCP Dialback</span></span></p></td>
<td><p><span data-ttu-id="636a5-238">TCP Dialback est la seule méthode de négociation disponible.</span><span class="sxs-lookup"><span data-stu-id="636a5-238">TCP Dialback is the only negotiation method available</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="636a5-239">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="636a5-239">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="636a5-240">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="636a5-240">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="636a5-241">False</span><span class="sxs-lookup"><span data-stu-id="636a5-241">False</span></span></p></td>
<td><p><span data-ttu-id="636a5-242">Configuration non valide</span><span class="sxs-lookup"><span data-stu-id="636a5-242">Not Valid Configuration</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="636a5-243">SASL ou Dialback doit être activé.</span><span class="sxs-lookup"><span data-stu-id="636a5-243">SASL or Dialback must be enabled.</span></span>


<span data-ttu-id="636a5-244"></div></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="636a5-244"></div></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span></span></div>

