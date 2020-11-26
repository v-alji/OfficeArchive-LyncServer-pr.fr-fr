---
title: 'Lync Server 2013 : paramètres nouveaux et modifiés pour Lync 2013'
description: 'Lync Server 2013 : paramètres nouveaux et modifiés pour Lync 2013.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: New and changed settings for Lync 2013
ms:assetid: bb13789c-7eda-461c-a387-02ea8ca4dabe
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205204(v=OCS.15)
ms:contentKeyID: 48185241
ms.date: 12/08/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1bf744e1bae774904733390ec624be523ad32bc1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445483"
---
# <a name="new-and-changed-settings-for-lync-2013"></a><span data-ttu-id="61c8f-103">Paramètres nouveaux et modifiés pour Lync 2013</span><span class="sxs-lookup"><span data-stu-id="61c8f-103">New and changed settings for Lync 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="61c8f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="61c8f-104">

<span> </span></span></span>

<span data-ttu-id="61c8f-105">_**Dernière modification de la rubrique :** 2014-12-05_</span><span class="sxs-lookup"><span data-stu-id="61c8f-105">_**Topic Last Modified:** 2014-12-05_</span></span>

<span data-ttu-id="61c8f-106">Cette rubrique traite des modifications apportées aux applets de applet Lync Server Management Shell qui sont associées directement à la gestion des clients.</span><span class="sxs-lookup"><span data-stu-id="61c8f-106">This topic discusses changes to Lync Server Management Shell cmdlets that relate directly to client management.</span></span> <span data-ttu-id="61c8f-107">Lync Server 2013 introduit plusieurs nouveaux paramètres et déprécie les paramètres des fonctionnalités qui peuvent être configurées par le biais d’autres moyens.</span><span class="sxs-lookup"><span data-stu-id="61c8f-107">Lync Server 2013 introduces several new parameters, and deprecates parameters for features that can be configured through other means.</span></span>

<div>

## <a name="new-client-management-parameters"></a><span data-ttu-id="61c8f-108">Nouveaux paramètres de gestion des clients</span><span class="sxs-lookup"><span data-stu-id="61c8f-108">New Client Management Parameters</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="61c8f-109">Nouveau</span><span class="sxs-lookup"><span data-stu-id="61c8f-109">New</span></span></th>
<th><span data-ttu-id="61c8f-110">Cmdlet Lync Server Management Shell</span><span class="sxs-lookup"><span data-stu-id="61c8f-110">Lync Server Management Shell Cmdlet</span></span></th>
<th><span data-ttu-id="61c8f-111">Description</span><span class="sxs-lookup"><span data-stu-id="61c8f-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="61c8f-112">TracingLevel</span><span class="sxs-lookup"><span data-stu-id="61c8f-112">TracingLevel</span></span></p></td>
<td><p><span data-ttu-id="61c8f-113">CsClientPolicy</span><span class="sxs-lookup"><span data-stu-id="61c8f-113">CsClientPolicy</span></span></p></td>
<td><p><span data-ttu-id="61c8f-114">Lorsque cette propriété est définie sur true, le suivi logiciel est activé dans Lync ; Lorsque la valeur est définie sur false, le suivi logiciel est désactivé.</span><span class="sxs-lookup"><span data-stu-id="61c8f-114">When set to True, software tracing will be enabled in Lync; when set to False, software tracing will be disabled.</span></span> <span data-ttu-id="61c8f-115">Le suivi logiciel implique de maintenir un enregistrement détaillé de tout ce qu’un programme effectue (y compris les appels d’API de suivi).</span><span class="sxs-lookup"><span data-stu-id="61c8f-115">Software tracing involves keeping a detailed record of everything that a program does (including tracking API calls).</span></span> <span data-ttu-id="61c8f-116">Le suivi est particulièrement utile pour les développeurs et pour le personnel de support de l’application. Ce paramètre est équivalent au paramètre de stratégie de groupe Communications Server 2007 R2 &quot; activez le suivi pour Communicator. &quot; Les paramètres sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="61c8f-116">Tracing is mostly useful to developers and to application support personnel.This setting is equivalent to the Communications Server 2007 R2 Group Policy setting &quot;Turn on tracing for Communicator.&quot; The settings are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="61c8f-117">Désactivé = le suivi est désactivé et l’utilisateur ne peut pas modifier ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="61c8f-117">Off = Tracing is disabled and the user cannot change this setting.</span></span></p></li>
<li><p><span data-ttu-id="61c8f-118">Clair = le suivi minimal est effectué et l’utilisateur ne peut pas modifier ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="61c8f-118">Light = Minimal tracing is performed, and the user cannot change this setting.</span></span></p></li>
<li><p><span data-ttu-id="61c8f-119">On = suivi détaillé est effectué et l’utilisateur ne peut pas modifier ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="61c8f-119">On = Verbose tracing is performed, and the user cannot change this setting.</span></span></p></li>
</ul>
<p><span data-ttu-id="61c8f-120">Par défaut, TracingLevel est défini sur une valeur null.</span><span class="sxs-lookup"><span data-stu-id="61c8f-120">By default TracingLevel is set to a null value.</span></span> <span data-ttu-id="61c8f-121">Cela signifie qu’un suivi minimal est effectué, mais que l’utilisateur peut activer ou désactiver ce suivi minimal.</span><span class="sxs-lookup"><span data-stu-id="61c8f-121">That means that minimal tracing is performed, but the user can enable or disable this minimal tracing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61c8f-122">EnableMediaRedirection</span><span class="sxs-lookup"><span data-stu-id="61c8f-122">EnableMediaRedirection</span></span></p></td>
<td><p><span data-ttu-id="61c8f-123">CsClientPolicy</span><span class="sxs-lookup"><span data-stu-id="61c8f-123">CsClientPolicy</span></span></p></td>
<td><p><span data-ttu-id="61c8f-124">Lorsque ce paramètre est défini sur true ($True) autorise la séparation des flux audio et vidéo à partir du trafic réseau, cela permet aux appareils clients de procéder au codage et au décodage de l’audio et de la vidéo localement.</span><span class="sxs-lookup"><span data-stu-id="61c8f-124">When set to True ($True) allows audio and video streams to be separated from other network traffic, In turn, this allows client devices to do encoding and decoding of audio and video locally.</span></span> <span data-ttu-id="61c8f-125">La redirection de média entraîne généralement une utilisation plus lente de la bande passante, une extensibilité du serveur plus élevée et une meilleure interface utilisateur par rapport aux techniques similaires, telles que l’accès à l’appareil distant ou la compression du codec.</span><span class="sxs-lookup"><span data-stu-id="61c8f-125">Media redirection typically results in lower bandwidth usage, higher server scalability, and a more-optimal user experience compared to similar techniques such as device remoting or codec compression.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61c8f-126">AllowLargeMeetings</span><span class="sxs-lookup"><span data-stu-id="61c8f-126">AllowLargeMeetings</span></span></p></td>
<td><p><span data-ttu-id="61c8f-127">CsConferencing</span><span class="sxs-lookup"><span data-stu-id="61c8f-127">CsConferencing</span></span></p></td>
<td><p><span data-ttu-id="61c8f-128">Lorsque cette propriété est définie sur true, toutes les réunions Lync sont considérées comme des &quot; réunions de grande taille. &quot; Dans une grande réunion, des restrictions sont placées sur le nombre de notifications envoyées aux participants, en plus de la taille de la liste de la réunion qui est transmise par défaut.</span><span class="sxs-lookup"><span data-stu-id="61c8f-128">When set to True, all Lync Meetings are treated as &quot;large meetings.&quot; With a large meeting, restrictions are placed on the number of notifications that are sent to participants, in addition to the size of the meeting roster that is transmitted by default.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61c8f-129">DisablePowerPointAnnotations</span><span class="sxs-lookup"><span data-stu-id="61c8f-129">DisablePowerPointAnnotations</span></span></p></td>
<td><p><span data-ttu-id="61c8f-130">CsConferencing</span><span class="sxs-lookup"><span data-stu-id="61c8f-130">CsConferencing</span></span></p></td>
<td><p><span data-ttu-id="61c8f-131">Lorsque cette propriété est définie sur true ($True), les utilisateurs ne peuvent pas ajouter d’annotations aux diapositives PowerPoint utilisées dans une conférence.</span><span class="sxs-lookup"><span data-stu-id="61c8f-131">When set to True ($True) users won’t be able to add annotations to PowerPoint slides used in a conference.</span></span> <span data-ttu-id="61c8f-132">Toutefois, en fonction de la valeur de la propriété AllowAnnotations, les utilisateurs auront toujours accès à d’autres fonctionnalités de tableau blanc.</span><span class="sxs-lookup"><span data-stu-id="61c8f-132">However (depending on the value of the AllowAnnotations property), users will still have access to other whiteboarding features.</span></span> <span data-ttu-id="61c8f-133">La valeur par défaut est false, ce qui signifie que les annotations PowerPoint sont autorisées.</span><span class="sxs-lookup"><span data-stu-id="61c8f-133">The default value is False, meaning that PowerPoint annotations are allowed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61c8f-134">AllowSharedNotes</span><span class="sxs-lookup"><span data-stu-id="61c8f-134">AllowSharedNotes</span></span></p></td>
<td><p><span data-ttu-id="61c8f-135">CsConferencing</span><span class="sxs-lookup"><span data-stu-id="61c8f-135">CsConferencing</span></span></p></td>
<td><p><span data-ttu-id="61c8f-136">Lorsque cette propriété est définie sur true (valeur par défaut), tous les blocs-notes OneNote ouverts liés à la Conférence seront automatiquement mis à jour avec des informations telles que des participants à la Conférence et des détails sur le contenu partagé pendant la Conférence.</span><span class="sxs-lookup"><span data-stu-id="61c8f-136">When set to True (the default value) any open OneNote notebooks linked to the conference will automatically be updated with information such as conference participants and details about content shared during the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61c8f-137">EnableInviteCustomization</span><span class="sxs-lookup"><span data-stu-id="61c8f-137">EnableInviteCustomization</span></span></p></td>
<td><p><span data-ttu-id="61c8f-138">CsMeetingConfiguration</span><span class="sxs-lookup"><span data-stu-id="61c8f-138">CsMeetingConfiguration</span></span></p></td>
<td><p><span data-ttu-id="61c8f-139">Utilisé avec les autres nouveaux paramètres de CsMeetingConfiguration pour personnaliser les invitations aux réunions générées par le complément réunion en ligne pour Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="61c8f-139">Used along with the other new CsMeetingConfiguration parameters to customize the meeting invitations generated by the Online Meeting Add-in for Lync 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61c8f-140">LogoURL</span><span class="sxs-lookup"><span data-stu-id="61c8f-140">LogoURL</span></span></p></td>
<td><p><span data-ttu-id="61c8f-141">CsMeetingConfiguration</span><span class="sxs-lookup"><span data-stu-id="61c8f-141">CsMeetingConfiguration</span></span></p></td>
<td><p><span data-ttu-id="61c8f-142">Ajoute le logo de votre organisation à toutes les invitations générées par le complément réunion en ligne pour Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="61c8f-142">Adds your organization’s logo to all invitations generated by the Online Meeting Add-in for Lync 2013.</span></span> <span data-ttu-id="61c8f-143">Vous spécifiez l’URL d’une image GIF ou JPG.</span><span class="sxs-lookup"><span data-stu-id="61c8f-143">You specify the URL of a GIF or JPG image.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61c8f-144">HelpURL</span><span class="sxs-lookup"><span data-stu-id="61c8f-144">HelpURL</span></span></p></td>
<td><p><span data-ttu-id="61c8f-145">CsMeetingConfiguration</span><span class="sxs-lookup"><span data-stu-id="61c8f-145">CsMeetingConfiguration</span></span></p></td>
<td><p><span data-ttu-id="61c8f-146">Ajoute l’adresse d’aide ou d’assistance de votre organisation à toutes les invitations générées par le complément réunion en ligne pour Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="61c8f-146">Adds your organization’s help or support URL to all invitations generated by the Online Meeting Add-in for Lync 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61c8f-147">LegalURL</span><span class="sxs-lookup"><span data-stu-id="61c8f-147">LegalURL</span></span></p></td>
<td><p><span data-ttu-id="61c8f-148">CsMeetingConfiguration</span><span class="sxs-lookup"><span data-stu-id="61c8f-148">CsMeetingConfiguration</span></span></p></td>
<td><p><span data-ttu-id="61c8f-149">Ajoute du texte légal ou une exclusion de responsabilité à toutes les invitations générées par le complément réunion en ligne pour Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="61c8f-149">Adds legal text or disclaimer text to all invitations generated by the Online Meeting Add-in for Lync 2013.</span></span> <span data-ttu-id="61c8f-150">Vous spécifiez l’URL de l’emplacement du texte.</span><span class="sxs-lookup"><span data-stu-id="61c8f-150">You specify the URL for the location of the text.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61c8f-151">CustomFooterText</span><span class="sxs-lookup"><span data-stu-id="61c8f-151">CustomFooterText</span></span></p></td>
<td><p><span data-ttu-id="61c8f-152">CsMeetingConfiguration</span><span class="sxs-lookup"><span data-stu-id="61c8f-152">CsMeetingConfiguration</span></span></p></td>
<td><p><span data-ttu-id="61c8f-153">Ajoute un pied de page personnalisé à toutes les invitations générées par le complément réunion en ligne pour Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="61c8f-153">Adds a custom footer to all invitations generated by the Online Meeting Add-in for Lync 2013.</span></span> <span data-ttu-id="61c8f-154">Vous spécifiez l’URL de l’emplacement du texte de pied de page personnalisé.</span><span class="sxs-lookup"><span data-stu-id="61c8f-154">You specify the URL for the location of the custom footer text.</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="deprecated-client-management-parameters"></a><span data-ttu-id="61c8f-155">Paramètres de gestion des clients déconseillés</span><span class="sxs-lookup"><span data-stu-id="61c8f-155">Deprecated Client Management Parameters</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="61c8f-156">Paramètre</span><span class="sxs-lookup"><span data-stu-id="61c8f-156">Parameter</span></span></th>
<th><span data-ttu-id="61c8f-157">Cmdlet Lync Server Management Shell</span><span class="sxs-lookup"><span data-stu-id="61c8f-157">Lync Server Management Shell Cmdlet</span></span></th>
<th><span data-ttu-id="61c8f-158">Description</span><span class="sxs-lookup"><span data-stu-id="61c8f-158">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="61c8f-159">CustomizedHelpUrl</span><span class="sxs-lookup"><span data-stu-id="61c8f-159">CustomizedHelpUrl</span></span></p></td>
<td><p><span data-ttu-id="61c8f-160">CsClientPolicy</span><span class="sxs-lookup"><span data-stu-id="61c8f-160">CsClientPolicy</span></span></p></td>
<td><p><span data-ttu-id="61c8f-161">Ce paramètre a été déconseillé pour une utilisation avec Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="61c8f-161">This parameter has been deprecated for use with Lync Server 2013.</span></span> <span data-ttu-id="61c8f-162">Lorsqu’il est utilisé avec EnableEnterpriseCustomizedHelp, ce paramètre a autorisé une organisation à spécifier une URL de telle sorte que lorsque les utilisateurs cliquent sur le menu aide de Lync, l’aide personnalisée s’affiche.</span><span class="sxs-lookup"><span data-stu-id="61c8f-162">When used in conjunction with EnableEnterpriseCustomizedHelp, this parameter enabled an organization to specify a URL so that when users clicked the Help menu in Lync, customized help would display.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61c8f-163">EnableEnterpriseCustomizedHelp</span><span class="sxs-lookup"><span data-stu-id="61c8f-163">EnableEnterpriseCustomizedHelp</span></span></p></td>
<td><p><span data-ttu-id="61c8f-164">CsClientPolicy</span><span class="sxs-lookup"><span data-stu-id="61c8f-164">CsClientPolicy</span></span></p></td>
<td><p><span data-ttu-id="61c8f-165">Ce paramètre a été déconseillé pour une utilisation avec Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="61c8f-165">This parameter has been deprecated for use with Lync Server 2013.</span></span> <span data-ttu-id="61c8f-166">Lorsqu’il est utilisé avec CustomizedHelpUrl, ce paramètre a activé les organisations pour afficher une aide personnalisée.</span><span class="sxs-lookup"><span data-stu-id="61c8f-166">When used in conjunction with CustomizedHelpUrl, this parameter enabled organizations to display customized help.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61c8f-167">EnableSQMData</span><span class="sxs-lookup"><span data-stu-id="61c8f-167">EnableSQMData</span></span></p></td>
<td><p><span data-ttu-id="61c8f-168">CsClientPolicy</span><span class="sxs-lookup"><span data-stu-id="61c8f-168">CsClientPolicy</span></span></p></td>
<td><p><span data-ttu-id="61c8f-169">Le paramètre EnableSQMData de la cmdlet Set-CSClientPolicy a été supprimé dans Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="61c8f-169">The EnableSQMData parameter of the Set-CSClientPolicy cmdlet has been removed in Lync Server 2013.</span></span> <span data-ttu-id="61c8f-170">Au lieu de cela, vous pouvez utiliser le paramètre de stratégie de groupe partagé pour les données de gestion de la qualité des logiciels pour déterminer l’interface utilisateur pour l’option d’amélioration du produit dans la page d’options général du client Lync :</span><span class="sxs-lookup"><span data-stu-id="61c8f-170">Instead, you can use the shared Group Policy setting for Software Quality Management (SQM) data to determine the user interface for the Customer Experience Improvement option in the Lync client General options page:</span></span></p>
<p><span data-ttu-id="61c8f-171">HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\Common\QMEnable</span><span class="sxs-lookup"><span data-stu-id="61c8f-171">HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\Common\QMEnable</span></span></p>
<p><span data-ttu-id="61c8f-172">Doubl</span><span class="sxs-lookup"><span data-stu-id="61c8f-172">Values:</span></span></p>
<p><span data-ttu-id="61c8f-173">1 = afficher et activer la case à cocher (l’utilisateur peut désactiver la case à cocher)</span><span class="sxs-lookup"><span data-stu-id="61c8f-173">1 = Display and select the check box (the user can clear the check box)</span></span></p>
<p><span data-ttu-id="61c8f-174">0 = désactiver et désactiver la case à cocher (l’utilisateur ne peut pas remplacer)</span><span class="sxs-lookup"><span data-stu-id="61c8f-174">0 = Turn off and disable the check box (user can't override)</span></span></p>
<p><span data-ttu-id="61c8f-175">NULL = la valeur est déterminée par le programme d’installation d’Office et la case à cocher est affichée pour que les utilisateurs puissent définir tels choix</span><span class="sxs-lookup"><span data-stu-id="61c8f-175">Null = The value is determined by Office setup, and the check box is displayed for users to set as they choose</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61c8f-176">AllowExchangeContactStore</span><span class="sxs-lookup"><span data-stu-id="61c8f-176">AllowExchangeContactStore</span></span></p></td>
<td><p><span data-ttu-id="61c8f-177">CsClientPolicy</span><span class="sxs-lookup"><span data-stu-id="61c8f-177">CsClientPolicy</span></span></p></td>
<td><p><span data-ttu-id="61c8f-178">Ce paramètre a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="61c8f-178">This parameter has been removed.</span></span> <span data-ttu-id="61c8f-179">Au lieu de cela, lorsque vous déployez Lync Server 2013 et que vous publiez la topologie, le magasin de contacts unifié est activé par défaut pour tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="61c8f-179">Instead, when you deploy Lync Server 2013 and publish the topology, unified contact store is enabled for all users by default.</span></span> <span data-ttu-id="61c8f-180">Cela signifie que tous les contacts d’un utilisateur sont conservés dans Exchange et sont disponibles dans Lync, Outlook et Outlook Web Access.</span><span class="sxs-lookup"><span data-stu-id="61c8f-180">This means that all a user’s contacts are kept in Exchange and are available in Lync, Outlook, and Outlook Web Access.</span></span> <span data-ttu-id="61c8f-181">Vous pouvez utiliser l’applet de passe Set-CsUserServicesPolicy pour personnaliser les utilisateurs qui disposent d’un magasin de contacts unifié disponible.</span><span class="sxs-lookup"><span data-stu-id="61c8f-181">You can use the Set-CsUserServicesPolicy cmdlet to customize which users have unified contact store available.</span></span> <span data-ttu-id="61c8f-182">Vous pouvez activer les utilisateurs globalement, par site, par client ou par individu ou groupe d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="61c8f-182">You can enable users globally, by site, by tenant, or by individuals or groups of individuals.</span></span> <span data-ttu-id="61c8f-183">Pour plus d’informations, reportez-vous à <a href="lync-server-2013-enable-users-for-unified-contact-store.md">activer les utilisateurs pour le magasin de contacts unifié dans Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="61c8f-183">For details, see <a href="lync-server-2013-enable-users-for-unified-contact-store.md">Enable users for unified contact store in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61c8f-184">MAPIPollInterval</span><span class="sxs-lookup"><span data-stu-id="61c8f-184">MAPIPollInterval</span></span></p></td>
<td><p><span data-ttu-id="61c8f-185">CsClientPolicy</span><span class="sxs-lookup"><span data-stu-id="61c8f-185">CsClientPolicy</span></span></p></td>
<td><p><span data-ttu-id="61c8f-186">Ce paramètre n’est pas utilisé par Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="61c8f-186">This parameter is not used by Lync 2013.</span></span> <span data-ttu-id="61c8f-187">Dans les versions précédentes, ce paramètre spécifiait le nombre de fois où le client récupérait des données MAPI à partir de dossiers publics Exchange</span><span class="sxs-lookup"><span data-stu-id="61c8f-187">In previous releases, this parameter specified how often the client retrieved MAPI data from Exchange public folders</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61c8f-188">DisableICE</span><span class="sxs-lookup"><span data-stu-id="61c8f-188">DisableICE</span></span></p></td>
<td><p><span data-ttu-id="61c8f-189">CsClientPolicy</span><span class="sxs-lookup"><span data-stu-id="61c8f-189">CsClientPolicy</span></span></p></td>
<td><p><span data-ttu-id="61c8f-190">Ce paramètre a été déconseillé dans Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="61c8f-190">This parameter was deprecated in Lync 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="61c8f-191">


</div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="61c8f-191">


</div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

