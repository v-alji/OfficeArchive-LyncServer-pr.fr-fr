---
title: 'Lync Server 2013 : modèles utilisateur'
description: 'Lync Server 2013 : modèles utilisateur.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Lync Server 2013 user models
ms:assetid: c551371c-d740-4372-bada-f0d713ec0d33
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398811(v=OCS.15)
ms:contentKeyID: 49733811
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 15be3f4c002de6cfb9ade4f13d80aedb59d76a82
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439148"
---
# <a name="user-models-in-lync-server-2013"></a><span data-ttu-id="54a37-103">Modèles utilisateur dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="54a37-103">User models in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="54a37-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="54a37-104">

<span> </span></span></span>

<span data-ttu-id="54a37-105">_**Dernière modification de la rubrique :** 2013-10-07_</span><span class="sxs-lookup"><span data-stu-id="54a37-105">_**Topic Last Modified:** 2013-10-07_</span></span>

<span data-ttu-id="54a37-106">Les modèles d’utilisateur décrits ici fournissent la base des mesures de planification de capacité et des recommandations décrites dans [planification de la capacité de Lync Server 2013 à l’aide des modèles utilisateur](lync-server-2013-capacity-planning-using-the-user-models.md).</span><span class="sxs-lookup"><span data-stu-id="54a37-106">The user models described here provide the basis for the capacity planning measurements and recommendations described in [Capacity planning for Lync Server 2013 using the user models](lync-server-2013-capacity-planning-using-the-user-models.md).</span></span>

<div>

## <a name="lync-server-2013-user-models"></a><span data-ttu-id="54a37-107">Modèles utilisateur Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="54a37-107">Lync Server 2013 User Models</span></span>

<span data-ttu-id="54a37-108">Le tableau suivant décrit le modèle utilisateur d’inscription, de contacts, de messagerie instantanée et de présence pour Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="54a37-108">The following table describes the user model for registration, contacts, instant messaging (IM), and presence for Lync Server 2013.</span></span>

### <a name="environment-and-registration-user-model"></a><span data-ttu-id="54a37-109">Modèle utilisateur pour l’environnement et l’enregistrement</span><span class="sxs-lookup"><span data-stu-id="54a37-109">Environment and Registration User Model</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="54a37-110">Catégorie</span><span class="sxs-lookup"><span data-stu-id="54a37-110">Category</span></span></th>
<th><span data-ttu-id="54a37-111">Description</span><span class="sxs-lookup"><span data-stu-id="54a37-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="54a37-112">Taille et distribution de déploiement</span><span class="sxs-lookup"><span data-stu-id="54a37-112">Deployment size and distribution</span></span></p></td>
<td><p><span data-ttu-id="54a37-113">Nous modélisons un déploiement important comptant trois sites centraux, avec un pool frontal par site.</span><span class="sxs-lookup"><span data-stu-id="54a37-113">We model a large deployment with three central sites, with one Front End pool per site.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54a37-114">Pourcentage d’utilisateurs Active Directory</span><span class="sxs-lookup"><span data-stu-id="54a37-114">Percentage of Active Directory users</span></span></p></td>
<td><p><span data-ttu-id="54a37-115">Nous supposons que 70% de tous les utilisateurs d’Active Directory au sein de l’organisation sont activés pour Lync Server.</span><span class="sxs-lookup"><span data-stu-id="54a37-115">We assume that 70% of all Active Directory users in the organization are enabled for Lync Server.</span></span> <span data-ttu-id="54a37-116">80% des utilisateurs activés sont connectés au serveur Lync chaque jour (80% d’accès concurrentiel).</span><span class="sxs-lookup"><span data-stu-id="54a37-116">80% of those enabled users are logged on to Lync Server each day (80% concurrency).</span></span> <span data-ttu-id="54a37-117">Le nombre d’employés dans le reste de cette section concerne des utilisateurs connectés simultanément.</span><span class="sxs-lookup"><span data-stu-id="54a37-117">The concurrent users are the basis for the numbers in the rest of this section.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54a37-118">Modifications Active Directory</span><span class="sxs-lookup"><span data-stu-id="54a37-118">Active Directory changes</span></span></p></td>
<td><p><span data-ttu-id="54a37-119">Nous supposons que 0,5% du total des utilisateurs sont créés et activés pour Lync dans Active Directory chaque semaine, et qu' 0,5% du total des utilisateurs sont désactivés à partir d’Active Directory et de Lync chaque semaine.</span><span class="sxs-lookup"><span data-stu-id="54a37-119">We assume that 0.5% of total users are created and enabled for Lync in Active Directory each week, and that 0.5% of total users are disabled from Active Directory and from Lync each week.</span></span> <span data-ttu-id="54a37-120">5% des utilisateurs disposent d’au moins un attribut Active Directory modifié chaque semaine.</span><span class="sxs-lookup"><span data-stu-id="54a37-120">5% of users have at least one Active Directory attribute changed each week.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54a37-121">Groupes de distribution Active Directory</span><span class="sxs-lookup"><span data-stu-id="54a37-121">Active Directory distribution groups</span></span></p></td>
<td><p><span data-ttu-id="54a37-122">Nous partons du principe que le nombre de groupes de distribution Active Directory au sein de l’organisation est égal à trois fois supérieur au nombre de tous les utilisateurs dans Active Directory.</span><span class="sxs-lookup"><span data-stu-id="54a37-122">We assume that the number of Active Directory distribution groups in the organization is equal to three times the number of all users in Active Directory.</span></span> <span data-ttu-id="54a37-123">Les groupes de distribution possèdent les tailles suivantes :</span><span class="sxs-lookup"><span data-stu-id="54a37-123">The distribution groups have the following sizes:</span></span></p>
<ul>
<li><p><span data-ttu-id="54a37-124">64 % comprennent de 2 à 30 utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="54a37-124">64% have 2-30 users</span></span></p></li>
<li><p><span data-ttu-id="54a37-125">13 % comprennent de 31 à 50 utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="54a37-125">13% have 31-50 users</span></span></p></li>
<li><p><span data-ttu-id="54a37-126">10 % comprennent de 51 à 100 utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="54a37-126">10% have 51-100 users</span></span></p></li>
<li><p><span data-ttu-id="54a37-127">13 % comprennent de 101 à 500 utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="54a37-127">13% have 101-500 users</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54a37-128">Utilisateurs VoIP (Voix sur IP)</span><span class="sxs-lookup"><span data-stu-id="54a37-128">Voice over IP (VoIP) users</span></span></p></td>
<td><p><span data-ttu-id="54a37-129">60% des utilisateurs de Lync Server sont activés pour les communications unifiées (UC) (c’est-à-dire que leurs numéros de téléphone sont détenus par Lync Server).</span><span class="sxs-lookup"><span data-stu-id="54a37-129">60% of Lync Server users are enabled for unified communications (UC) (that is, their phone numbers are owned by Lync Server).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54a37-130">Répartition des clients enregistrés</span><span class="sxs-lookup"><span data-stu-id="54a37-130">Registered client distribution</span></span></p></td>
<td><p><span data-ttu-id="54a37-131">65% de clients exécutent le logiciel Lync 2013, y compris Lync et Lync Phone Edition.</span><span class="sxs-lookup"><span data-stu-id="54a37-131">65% of clients run Lync 2013 software, including Lync and Lync Phone Edition.</span></span></p>
<p><span data-ttu-id="54a37-132">30% de clients exécutant un logiciel client à partir d’une version précédente de Lync.</span><span class="sxs-lookup"><span data-stu-id="54a37-132">30% of clients running client software from a previous version of Lync.</span></span></p>
<p><span data-ttu-id="54a37-133">5% de clients utilisant Lync Web App.</span><span class="sxs-lookup"><span data-stu-id="54a37-133">5% of clients using Lync Web App.</span></span></p>
<p><span data-ttu-id="54a37-p104">Si la mobilité est activée, nous partons du principe que 40 % des utilisateurs utilisent la mobilité en même temps que les autres options de clients inscrits mentionnées précédemment. Dans ce cas, le rapport du point de présence multiple (MPOP) client est de 1/1,9. Si la mobilité est désactivée, ce rapport est de 1/1,5.</span><span class="sxs-lookup"><span data-stu-id="54a37-p104">If mobility is enabled, we assume that 40% of users are using mobility concurrently with the other previously cited registered client options. In this case the client multiple point of presence (MPOP) ratio is 1:1.9. If mobility is disabled, the MPOP ratio is 1:1.5.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54a37-137">Répartition des utilisateurs distants</span><span class="sxs-lookup"><span data-stu-id="54a37-137">Remote user distribution</span></span></p></td>
<td><p><span data-ttu-id="54a37-138">70 % des utilisateurs se connectent en interne.</span><span class="sxs-lookup"><span data-stu-id="54a37-138">70% of users connecting internally.</span></span></p>
<p><span data-ttu-id="54a37-139">30% des utilisateurs se connectant via un serveur Edge et un directeur.</span><span class="sxs-lookup"><span data-stu-id="54a37-139">30% of users connecting through an Edge Server and a Director.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54a37-140">Répartition des contacts</span><span class="sxs-lookup"><span data-stu-id="54a37-140">Contact distribution</span></span></p></td>
<td><p><span data-ttu-id="54a37-p105">Un utilisateur peut avoir 1 000 contacts au maximum. Cela concerne moins de 1 % des utilisateurs. Moins de 25 % des utilisateurs ont 100 contacts ou plus.</span><span class="sxs-lookup"><span data-stu-id="54a37-p105">The maximum number of contacts a user has is 1,000. Less than 1% of users have 1,000 contacts. Less than 25% of users have 100 or more contacts.</span></span></p>
<p><span data-ttu-id="54a37-p106">La moyenne est de 80 contacts pour les utilisateurs d’un nuage public. Parmi ces utilisateurs :</span><span class="sxs-lookup"><span data-stu-id="54a37-p106">Average of 80 contacts for users with public cloud connectivity. Of these users:</span></span></p>
<ul>
<li><p><span data-ttu-id="54a37-p107">50 % des contacts font partie de l’entreprise. 10 % de ces utilisateurs sont des utilisateurs distants, qui se connectent en dehors du pare-feu.</span><span class="sxs-lookup"><span data-stu-id="54a37-p107">50% of the contacts are within the organization. 10% of those users are remote users, connecting from outside the firewall.</span></span></p></li>
<li><p><span data-ttu-id="54a37-148">40% des contacts sont des utilisateurs du cloud public (par exemple, les utilisateurs d’AOL, de Yahoo !, de MSN ou de Google Talk).</span><span class="sxs-lookup"><span data-stu-id="54a37-148">40% of the contacts are public cloud users (such as users of AOL, Yahoo!, MSN, or Google Talk).</span></span></p></li>
<li><p><span data-ttu-id="54a37-149">10 % des contacts sont des partenaires fédérés.</span><span class="sxs-lookup"><span data-stu-id="54a37-149">10% of the contacts are from federated partners.</span></span></p>
<div>

> [!IMPORTANT]  
> <UL>
> <LI>
> <P><span data-ttu-id="54a37-150">À compter du 1er septembre, 2012, le contrat de licence de l’utilisateur Microsoft Lync Public IM Connectivity (« PIC USL ») ne sera plus disponible à l’achat pour les contrats de nouveau ou de renouvellement.</span><span class="sxs-lookup"><span data-stu-id="54a37-150">As of September 1st, 2012, the Microsoft Lync Public IM Connectivity User Subscription License (“PIC USL”) is no longer available for purchase for new or renewing agreements.</span></span> <span data-ttu-id="54a37-151">Les clients disposant de licences actives seront en mesure de continuer à fédérer avec Yahoo !</span><span class="sxs-lookup"><span data-stu-id="54a37-151">Customers with active licenses will be able to continue to federate with Yahoo!</span></span> <span data-ttu-id="54a37-152">Messenger jusqu’à la date d’arrêt du service.</span><span class="sxs-lookup"><span data-stu-id="54a37-152">Messenger until the service shut down date.</span></span> <span data-ttu-id="54a37-153">Date de fin de vie du 2014 juin pour AOL et Yahoo !</span><span class="sxs-lookup"><span data-stu-id="54a37-153">An end of life date of June 2014 for AOL and Yahoo!</span></span> <span data-ttu-id="54a37-154">a été annoncé.</span><span class="sxs-lookup"><span data-stu-id="54a37-154">has been announced.</span></span> <span data-ttu-id="54a37-155">Pour plus d’informations, voir <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">prise en charge de la connectivité de messagerie instantanée publique dans Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="54a37-155">For details, see <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Support for public instant messenger connectivity in Lync Server 2013</A>.</span></span></P>
> <LI>
> <P><span data-ttu-id="54a37-156">La fonction USL (PIC) est une licence d’abonnement par mois qui est requise pour que Lync Server ou Office Communications Server se fédérer avec Yahoo !</span><span class="sxs-lookup"><span data-stu-id="54a37-156">The PIC USL is a per-user per-month subscription license that is required for Lync Server or Office Communications Server to federate with Yahoo!</span></span> <span data-ttu-id="54a37-157">Messenger.</span><span class="sxs-lookup"><span data-stu-id="54a37-157">Messenger.</span></span> <span data-ttu-id="54a37-158">La capacité de Microsoft à fournir ce service est subordonné à la prise en charge de Yahoo !, le contrat sous-jacent pour lequel le son est arrêté.</span><span class="sxs-lookup"><span data-stu-id="54a37-158">Microsoft’s ability to provide this service has been contingent upon support from Yahoo!, the underlying agreement for which is winding down.</span></span></P>
> <LI>
> <P><span data-ttu-id="54a37-159">Plus que jamais, Lync est un outil puissant de connexion entre organisations et de personnes dans le monde entier.</span><span class="sxs-lookup"><span data-stu-id="54a37-159">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="54a37-160">La Fédération avec Windows Live Messenger ne nécessite aucune licence d’utilisateur/appareil supplémentaire au-delà de la CAL standard Lync.</span><span class="sxs-lookup"><span data-stu-id="54a37-160">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard CAL.</span></span> <span data-ttu-id="54a37-161">Skype Federation sera ajouté à cette liste et permettra aux utilisateurs de Lync de joindre des centaines de millions de personnes à la messagerie instantanée et à la voix.</span><span class="sxs-lookup"><span data-stu-id="54a37-161">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people with IM and voice.</span></span></P></LI></UL>


</div></li>
</ul>
<p><span data-ttu-id="54a37-p111">La moyenne est de 50 contacts pour les utilisateurs ne pouvant pas se connecter à un cloud public. Parmi ces utilisateurs :</span><span class="sxs-lookup"><span data-stu-id="54a37-p111">Average of 50 contacts for users without public cloud connectivity. Of these users:</span></span></p>
<ul>
<li><p><span data-ttu-id="54a37-p112">80 % des contacts font partie de l’entreprise. 10 % de ces utilisateurs sont des utilisateurs distants qui se connectent en dehors du pare-feu.</span><span class="sxs-lookup"><span data-stu-id="54a37-p112">80% of the contacts are within the organization. 10% of those users are remote users, connecting from outside the firewall.</span></span></p></li>
<li><p><span data-ttu-id="54a37-166">20 % des contacts sont des partenaires fédérés.</span><span class="sxs-lookup"><span data-stu-id="54a37-166">20% of the contacts are from federated partners.</span></span></p>
<p><span data-ttu-id="54a37-p113">Chaque utilisateur possède 1 groupe de distribution dans sa liste de contacts. Pour les tests de performance, nous partons du principe que les groupes de distribution sont toujours développés.</span><span class="sxs-lookup"><span data-stu-id="54a37-p113">Each user has 1 distribution group in their contact list. For performance testing, we assume that distribution groups are always expanded.</span></span></p></li>
</ul>
<p><span data-ttu-id="54a37-169">25% des contacts d’un utilisateur utilisent XMPP.</span><span class="sxs-lookup"><span data-stu-id="54a37-169">25% of a user’s contacts use XMPP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54a37-170">Durée d’une session</span><span class="sxs-lookup"><span data-stu-id="54a37-170">Session time</span></span></p></td>
<td><p><span data-ttu-id="54a37-p114">En moyenne, un utilisateur se connecte 12 heures. Tous les utilisateurs se connectent dans les 120 minutes suivant le début de la session.</span><span class="sxs-lookup"><span data-stu-id="54a37-p114">The average user logon session lasts 12 hours. All users log on within 120 minutes of the start of the session.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="im-and-presence-user-model"></a><span data-ttu-id="54a37-173">Modèle utilisateur pour la messagerie instantanée et la présence</span><span class="sxs-lookup"><span data-stu-id="54a37-173">IM and Presence User Model</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="54a37-174">Catégorie</span><span class="sxs-lookup"><span data-stu-id="54a37-174">Category</span></span></th>
<th><span data-ttu-id="54a37-175">Description</span><span class="sxs-lookup"><span data-stu-id="54a37-175">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="54a37-176">Sessions de messagerie instantanée P2P</span><span class="sxs-lookup"><span data-stu-id="54a37-176">Peer-to-peer IM sessions</span></span></p></td>
<td><p><span data-ttu-id="54a37-177">En moyenne, chaque utilisateur ouvre six sessions de messagerie instantanée P2P par jour.</span><span class="sxs-lookup"><span data-stu-id="54a37-177">Each user averages six peer-to-peer IM sessions per day.</span></span></p>
<p><span data-ttu-id="54a37-178">10 messages instantanés par session.</span><span class="sxs-lookup"><span data-stu-id="54a37-178">10 instant messages per session.</span></span></p>
<p><span data-ttu-id="54a37-179">Chaque message est associé à deux messages de type SIP et à 2 SIP 200 OK (pour les indicateurs d’État tels que « &lt; nom &gt; est en train d’écrire »)</span><span class="sxs-lookup"><span data-stu-id="54a37-179">Each message is matched by two SIP INFO messages and 2 SIP 200 OK messages (for the status indicators such as “&lt;Name&gt; is Typing”)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54a37-180">Interrogation de présence</span><span class="sxs-lookup"><span data-stu-id="54a37-180">Presence polling</span></span></p></td>
<td><p><span data-ttu-id="54a37-p115">Globalement, nous estimons l’interrogation de présence à 60 interrogations par utilisateur et par heure. La moyenne par utilisateur est estimée à :</span><span class="sxs-lookup"><span data-stu-id="54a37-p115">Overall, we assume presence polling at an average of 60 polls per user per hour. For each user, assume an average of:</span></span></p>
<ul>
<li><p><span data-ttu-id="54a37-p116">Une interrogation par jour de présence des utilisateurs sous l’onglet d’organisation de l’utilisateur (mais pas dans la liste des contacts). En moyenne, 15 utilisateurs ne sont pas des contacts sous l’onglet d’organisation de l’utilisateur. Deux opérations d’affichage de carte de visite par jour.</span><span class="sxs-lookup"><span data-stu-id="54a37-p116">One poll per day of the presence of users in the user’s organization tab (but not Contacts list). Average number of non-contacts in the user’s organization tab is 15 users. Two contact card viewing operations per day.</span></span></p></li>
<li><p><span data-ttu-id="54a37-186">Une interrogation de présence chaque fois que l’utilisateur clique sur le nom d’un autre utilisateur pour commencer une conversation, estimée à une par heure.</span><span class="sxs-lookup"><span data-stu-id="54a37-186">One presence poll every time the user clicks another user to start a conversation, estimated at once per hour.</span></span></p></li>
<li><p><span data-ttu-id="54a37-p117">Six recherches utilisateur sont effectuées par heure. À chaque recherche, une interrogation par lot est envoyée à tout le monde dans la liste des résultats de recherche. Nous supposons que la taille moyenne des résultats de recherche est de 20. Pour les résultats restant à l’écran, l’interrogation par lot est actualisée toutes les 5 minutes. Nous partons du principe qu’il y a deux actualisations par heure.</span><span class="sxs-lookup"><span data-stu-id="54a37-p117">Six user searches per hour. Every time a search is performed, a batch poll is sent for everyone in the search result list. We assume the average size of search results is 20. If the search results stay on screen, the batch poll is refreshed every 5 minutes; we assume that there will be two such refreshes per hour.</span></span></p></li>
<li><p><span data-ttu-id="54a37-191">Lorsque l’utilisateur ouvre ou prévisualise un message électronique dans Outlook, une interrogation de présence des utilisateurs dans les champs À : et Cc : du message, estimée à cinq messages électroniques par heure et quatre utilisateurs par message.</span><span class="sxs-lookup"><span data-stu-id="54a37-191">When the user opens or previews an email in Outlook, a poll of the presence of users in the To: and CC: fields of the email, estimated at five emails per hour and four users per email.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54a37-192">Abonnements aux informations de présence</span><span class="sxs-lookup"><span data-stu-id="54a37-192">Presence subscriptions</span></span></p></td>
<td><p><span data-ttu-id="54a37-p118">Lorsqu’un premier utilisateur ajoute un autre contact, il s’<em>abonne</em> à cinq catégories d’informations concernant ce contact. Des mises à jour de ces catégories d’informations sont envoyées automatiquement au premier utilisateur.</span><span class="sxs-lookup"><span data-stu-id="54a37-p118">When one user adds another as a contact, the first user is <em>subscribing</em> to five categories of information about the second user. Updates of these categories of information are automatically sent to the first user.</span></span></p>
<p><span data-ttu-id="54a37-195">Pour chaque client, une seule demande d’abonnement par lot est envoyée pour obtenir le statut de présence d’une moyenne de 40 contacts, avec 40 boîtes de dialogue supplémentaires afin d’obtenir la présence des contacts fédérés.</span><span class="sxs-lookup"><span data-stu-id="54a37-195">For each client, a single batch subscription request is sent to obtain the presence state of an average of 40 contacts, with an additional 40 dialogs to obtain presence for federated contacts.</span></span></p>
<p><span data-ttu-id="54a37-196">La présence des membres d’un groupe de distribution développé se détermine par les abonnements de présence permanents, et non par l’interrogation, et est modelée sous forme d’une expansion par utilisateur toutes les 2 heures.</span><span class="sxs-lookup"><span data-stu-id="54a37-196">Presence for members of an expanded distribution group is found through persistent presence subscriptions, not polling, and is modeled as 1 expansion per user for each 2 hours.</span></span></p>
<p><span data-ttu-id="54a37-p119">Les <em>abonnements courts</em> se produisent si un utilisateur ouvre une session, qu’il existe un abonnement par lot pour tous les contacts de l’utilisateur et que l’utilisateur ferme sa session peu de temps après. Nous partons du principe que 6 abonnements courts se font par utilisateur et par heure, où chaque abonnement dure 10 minutes.</span><span class="sxs-lookup"><span data-stu-id="54a37-p119"><em>Short subscriptions</em> happen when a user logs in, there is a batch subscription for all the user’s contacts, and then the user soon logs off. We assume 6 short subscriptions per user per hour, where each subscription lasts 10 minutes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54a37-199">Publication de présence</span><span class="sxs-lookup"><span data-stu-id="54a37-199">Presence Publication</span></span></p></td>
<td><p><span data-ttu-id="54a37-200">En moyenne, le statut de présence est publié 4 fois par utilisateur et par heure, avec un maximum de 6 fois.</span><span class="sxs-lookup"><span data-stu-id="54a37-200">Presence state is published at an average of 4 publications per user per hour, with a maximum 6 per user per hour.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54a37-201">Taille du document de présence</span><span class="sxs-lookup"><span data-stu-id="54a37-201">Presence Document Size</span></span></p></td>
<td><p><span data-ttu-id="54a37-202">La taille moyenne d’un document de présence complet est estimée à 4 Ko, avec un maximum de 25 Ko.</span><span class="sxs-lookup"><span data-stu-id="54a37-202">The average size of a complete presence document is assumed to be 4K, with a maximum of 25K.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="54a37-203">Le tableau ci-dessous décrit le modèle utilisateur pour l’utilisation d’un carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="54a37-203">The following table describes the user model for address book use.</span></span>

### <a name="address-book-usage-user-model"></a><span data-ttu-id="54a37-204">Modèle utilisateur pour l’utilisation d’un carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="54a37-204">Address Book Usage User Model</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="54a37-205">Mode de recherche d’un carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="54a37-205">Address Book search mode</span></span></th>
<th><span data-ttu-id="54a37-206">Utilisation</span><span class="sxs-lookup"><span data-stu-id="54a37-206">Usage</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="54a37-207">Requête web du carnet d’adresses uniquement (toutes les requêtes sont effectuées par le service de requête web du carnet d’adresses)</span><span class="sxs-lookup"><span data-stu-id="54a37-207">Address Book Web Query only (all queries performed by Address Book Web Query service)</span></span></p></td>
<td><p><span data-ttu-id="54a37-208">Quatre requêtes de préfixe quotidiennes par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="54a37-208">Four prefix queries per user per day.</span></span></p>
<p><span data-ttu-id="54a37-p120">60 requêtes de recherche exacte quotidiennes par utilisateur. 40 % de ces requêtes sont traitées par lot, avec une moyenne de 20 contacts par requête. Les 60 % restants concernent un seul contact.</span><span class="sxs-lookup"><span data-stu-id="54a37-p120">60 exact search queries per user per day. 40% of those are batched, with an average of 20 contacts per query. The other 60% of the queries are for a single contact.</span></span></p>
<p><span data-ttu-id="54a37-p121">25 requêtes de photos quotidiennes par utilisateur. 24 concernent une seule photo, la dernière étant une requête par lot avec une moyenne de 20 contacts.</span><span class="sxs-lookup"><span data-stu-id="54a37-p121">25 photo queries per user per day. 24 are for a single photo, the other is a batch query with an average of 20 contacts.</span></span></p>
<p><span data-ttu-id="54a37-214">Une requête quotidienne par utilisateur de recherche dans toute l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="54a37-214">One total organization search query per user per day.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54a37-p122">Mode mixte : utilisation du fichier de carnet d’adresses et des requêtes web. Il s’agit du mode par défaut.</span><span class="sxs-lookup"><span data-stu-id="54a37-p122">Mixed mode, both address book file and web queries used. This is the default mode.</span></span></p></td>
<td><p><span data-ttu-id="54a37-217">Deux types de requête uniquement sont transmis sur le réseau, à savoir les requêtes de photos et les requêtes de recherche dans toute l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="54a37-217">Only two types of queries go to the network, the photo and total organizational search queries.</span></span></p>
<p><span data-ttu-id="54a37-p123">25 requêtes de photos quotidiennes par utilisateur. 24 concernent une seule photo, la dernière étant une requête par lot avec une moyenne de 20 contacts.</span><span class="sxs-lookup"><span data-stu-id="54a37-p123">25 photo queries per user per day. 24 are for a single photo, the other is a batch query with an average of 20 contacts.</span></span></p>
<p><span data-ttu-id="54a37-220">Une requête quotidienne par utilisateur de recherche dans toute l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="54a37-220">One total organization search query per user per day.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="54a37-221">Le tableau ci-dessous décrit le modèle de conférence.</span><span class="sxs-lookup"><span data-stu-id="54a37-221">The following table describes the conferencing model.</span></span>

### <a name="conferencing-model"></a><span data-ttu-id="54a37-222">Modèle de conférence</span><span class="sxs-lookup"><span data-stu-id="54a37-222">Conferencing Model</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="54a37-223">Catégorie</span><span class="sxs-lookup"><span data-stu-id="54a37-223">Category</span></span></th>
<th><span data-ttu-id="54a37-224">Description</span><span class="sxs-lookup"><span data-stu-id="54a37-224">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="54a37-225">Réunions planifiées et &quot; réunions à l’heure actuelle &quot;</span><span class="sxs-lookup"><span data-stu-id="54a37-225">Scheduled meetings versus &quot;Meet now&quot; meetings</span></span></p></td>
<td><p><span data-ttu-id="54a37-226">60 % des réunions sont planifiées, 40 % ne le sont pas.</span><span class="sxs-lookup"><span data-stu-id="54a37-226">60% scheduled, 40% unscheduled.</span></span></p>
<p><span data-ttu-id="54a37-227">Pour les réunions planifiées, nous partons du principe que les conférences sont affectées par 80%, qui sont des occurrences de conférences périodiques. 10% sont des réunions à durée unique. 8% sont des réunions anonymes à la fois et 2% sont des réunions ponctuelles.</span><span class="sxs-lookup"><span data-stu-id="54a37-227">Of the scheduled meetings, we assume that 80% are assigned conferences, which are occurences of recurring conferences; 10% are one-time open meetings; 8% are one-time anonymous meetings, and 2% are one-time closed meetings.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54a37-228">Répartition des clients de conférence</span><span class="sxs-lookup"><span data-stu-id="54a37-228">Conferencing client distribution</span></span></p></td>
<td><p><span data-ttu-id="54a37-229">Pour les réunions planifiées :</span><span class="sxs-lookup"><span data-stu-id="54a37-229">For scheduled meetings:</span></span></p>
<ul>
<li><p><span data-ttu-id="54a37-230">65% des utilisateurs de conférences utilisent Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="54a37-230">65% of conferencing users use Lync 2013.</span></span></p></li>
<li><p><span data-ttu-id="54a37-231">5% des utilisateurs de la Conférence utilisent Microsoft Lync Web App.</span><span class="sxs-lookup"><span data-stu-id="54a37-231">5% of conferencing users use Microsoft Lync Web App.</span></span></p></li>
<li><p><span data-ttu-id="54a37-232">30% des utilisateurs de la Conférence utilisent des clients antérieurs, dont Microsoft Lync 2010, Office Communicator 2007 R2, Office Communicator 2007 et Microsoft Office Communicator Web Access (version 2007).</span><span class="sxs-lookup"><span data-stu-id="54a37-232">30% of conferencing users use earlier clients, including Microsoft Lync 2010, Office Communicator 2007 R2, Office Communicator 2007, and Microsoft Office Communicator Web Access (2007 release).</span></span></p></li>
</ul>
<p><span data-ttu-id="54a37-233">Pour les réunions non planifiées :</span><span class="sxs-lookup"><span data-stu-id="54a37-233">For unscheduled meetings:</span></span></p>
<ul>
<li><p><span data-ttu-id="54a37-234">70% des utilisateurs de conférences utilisent Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="54a37-234">70% of conferencing users use Lync 2013.</span></span></p></li>
<li><p><span data-ttu-id="54a37-235">30% des utilisateurs de la Conférence utilisent des clients antérieurs, dont Microsoft Lync 2010, Office Communicator 2007 R2, Office Communicator 2007 et Microsoft Office Communicator Web Access (version 2007).</span><span class="sxs-lookup"><span data-stu-id="54a37-235">30% of conferencing users use earlier clients, including Microsoft Lync 2010, Office Communicator 2007 R2, Office Communicator 2007, and Microsoft Office Communicator Web Access (2007 release).</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54a37-236">Simultanéité des réunions</span><span class="sxs-lookup"><span data-stu-id="54a37-236">Meeting concurrency</span></span></p></td>
<td><p><span data-ttu-id="54a37-p124">5 % des utilisateurs participeront à des conférences pendant les heures de travail. Ainsi, dans un pool de 80 000 utilisateurs, il peut arriver que 4 000 utilisateurs participent à tout moment à des conférences.</span><span class="sxs-lookup"><span data-stu-id="54a37-p124">5% of users will be in conferences during working hours. Thus, in an 80,000-user pool, as many as 4,000 users might be in conferences at any one time.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54a37-239">Répartition des appels audio d’une réunion</span><span class="sxs-lookup"><span data-stu-id="54a37-239">Meeting audio distribution</span></span></p></td>
<td><p><span data-ttu-id="54a37-240">40 % d’appels audio VoIP et de conférences rendez-vous combinés, avec un ratio d’utilisateurs VoIP par rapport aux utilisateurs d’appels entrants égal à 3:1.</span><span class="sxs-lookup"><span data-stu-id="54a37-240">40% mixed VoIP audio and dial-in conferencing, with a 3:1 ratio of VoIP users to dial-in users.</span></span></p>
<p><span data-ttu-id="54a37-241">35 % d’appels audio VoIP uniquement.</span><span class="sxs-lookup"><span data-stu-id="54a37-241">35% VoIP audio only.</span></span></p>
<p><span data-ttu-id="54a37-242">15 % d’audioconférences rendez-vous uniquement.</span><span class="sxs-lookup"><span data-stu-id="54a37-242">15% dial-in conferencing audio only.</span></span></p>
<p><span data-ttu-id="54a37-243">10 % sans appel audio (conférences de messagerie instantanée uniquement, avec une moyenne de cinq messages envoyés par utilisateur).</span><span class="sxs-lookup"><span data-stu-id="54a37-243">10% no audio (IM-only conferences, with an average of five messages sent per user).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54a37-244">Utilisation de différents médias dans le cadre des conférences</span><span class="sxs-lookup"><span data-stu-id="54a37-244">Media mix for conferences</span></span></p></td>
<td><p><span data-ttu-id="54a37-245">75 % des conférences ont lieu sur Internet, notamment par des méthodes de collaboration audio ou autres.</span><span class="sxs-lookup"><span data-stu-id="54a37-245">75% of conferences are web conferences, which include audio plus some other collaboration modalities.</span></span></p>
<p><span data-ttu-id="54a37-246">Pour ces conférences, les autres méthodes de collaboration sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="54a37-246">For these conferences, the other collaboration methods are as follows:</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="54a37-247">Le total de ces nombres dépasse 100 %, car une conférence peut faire appel à plusieurs méthodes de collaboration.</span><span class="sxs-lookup"><span data-stu-id="54a37-247">These numbers add up to more than 100% because one conference can have multiple collaboration methods.</span></span>


</div>
<ul>
<li><p><span data-ttu-id="54a37-p125">50 % utilisent le partage d’application. Nous supposons qu’un utilisateur envoie des données avec un pic de 1,1 Mo par seconde.</span><span class="sxs-lookup"><span data-stu-id="54a37-p125">50% add application sharing. We assume one users sends data at a peak of 1.1 MB per second.</span></span></p></li>
<li><p><span data-ttu-id="54a37-250">50 % font appel à la messagerie instantanée (avec en moyenne 2 messages par utilisateur).</span><span class="sxs-lookup"><span data-stu-id="54a37-250">50% add instant messaging (with an average of 2 messages per user).</span></span></p></li>
<li><p><span data-ttu-id="54a37-p126">20 % ont recours à la collaboration de données, à travers de PowerPoint ou d’un tableau blanc, par exemple. En moyenne, 2 fichiers PowerPoint d’environ 10 Mo (sans vidéo incorporée) ou 30 Mo (avec vidéo incorporée) chacun sont présentés lors d’une conférence. On dénombre 20 annotations par tableau blanc en moyenne.</span><span class="sxs-lookup"><span data-stu-id="54a37-p126">20% add data collaboration, including PowerPoint or whiteboard In these, an average of 2 PowerPoint files presented per conference, with an average PowerPoint file size of 10 MB (without embedded video) or 30 MB (with embedded video). Average of 20 annotations per whiteboard.</span></span></p></li>
<li><p><span data-ttu-id="54a37-p127">20 % utilisent de la vidéo. De ces utilisateurs, 70 % participent à des conférences activées pour la vidéo multiview, où chaque utilisateur reçoit 2 à 3 flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="54a37-p127">20% add video. Of these users, 70% are in conferences enabled for multiview video, where each user receives 2-3 video streams.</span></span></p></li>
<li><p><span data-ttu-id="54a37-255">15 % ajoutent des notes partagées.</span><span class="sxs-lookup"><span data-stu-id="54a37-255">15% add shared notes.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54a37-256">Répartition des participants aux réunions</span><span class="sxs-lookup"><span data-stu-id="54a37-256">Meeting participant distribution</span></span></p></td>
<td><p><span data-ttu-id="54a37-257">50 % d’utilisateurs internes authentifiés.</span><span class="sxs-lookup"><span data-stu-id="54a37-257">50% internal, authenticated users.</span></span></p>
<p><span data-ttu-id="54a37-258">25 % d’utilisateurs distants authentifiés.</span><span class="sxs-lookup"><span data-stu-id="54a37-258">25% remote access, authenticated users.</span></span></p>
<p><span data-ttu-id="54a37-259">15 % d’utilisateurs anonymes.</span><span class="sxs-lookup"><span data-stu-id="54a37-259">15% anonymous users.</span></span></p>
<p><span data-ttu-id="54a37-260">10 % d’utilisateurs fédérés.</span><span class="sxs-lookup"><span data-stu-id="54a37-260">10% federated users.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54a37-261">Répartition de la participation aux réunions</span><span class="sxs-lookup"><span data-stu-id="54a37-261">Meeting join distribution</span></span></p></td>
<td><p><span data-ttu-id="54a37-262">Il est simulé que les utilisateurs se joignent à la réunion dans les 5 premières minutes.</span><span class="sxs-lookup"><span data-stu-id="54a37-262">Users are simulated as joining the meeting within the first 5 minutes.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="54a37-263">Dans les pools front-end standard, Lync Server 2013 a une taille de réunion prise en charge maximale de 250 utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="54a37-263">In regular Front End pools, Lync Server 2013 has a maximum supported meeting size of 250 users.</span></span> <span data-ttu-id="54a37-264">Chaque pool peut héberger 250 utilisateurs à la fois.</span><span class="sxs-lookup"><span data-stu-id="54a37-264">Each pool can host one 250-user meeting at a time.</span></span> <span data-ttu-id="54a37-265">Quand une réunion regroupant autant de participants a lieu, le pool peut également héberger d’autres conférences plus petites.</span><span class="sxs-lookup"><span data-stu-id="54a37-265">While this large meeting is occurring, the pool can also host other smaller conferences.</span></span> <span data-ttu-id="54a37-266">Vous pouvez également prendre en charge les réunions rassemblant jusqu’à 1 000 utilisateurs en configurant un pool dédié pour les héberger.</span><span class="sxs-lookup"><span data-stu-id="54a37-266">Additionally, you can support meetings of up to 1000 users by setting up a dedicated pool to host these meetings.</span></span> <span data-ttu-id="54a37-267">Pour plus d’informations, consultez [prise en charge des réunions de grande envergure dans Lync Server 2013](lync-server-2013-support-for-large-meetings.md).</span><span class="sxs-lookup"><span data-stu-id="54a37-267">For details, see [Support for large meetings in Lync Server 2013](lync-server-2013-support-for-large-meetings.md).</span></span>

<span data-ttu-id="54a37-268">Les conférences sont simulées comme suit :</span><span class="sxs-lookup"><span data-stu-id="54a37-268">Conferences were simulated as follows:</span></span>

  - <span data-ttu-id="54a37-269">85 % des conférences comptent quatre participants.</span><span class="sxs-lookup"><span data-stu-id="54a37-269">85% of conferences had four participants.</span></span>

  - <span data-ttu-id="54a37-270">10 % des conférences comptent six participants.</span><span class="sxs-lookup"><span data-stu-id="54a37-270">10% of conferences had six participants.</span></span>

  - <span data-ttu-id="54a37-271">5 % des conférences comptent 11 participants.</span><span class="sxs-lookup"><span data-stu-id="54a37-271">5% of conferences had 11 participants.</span></span>

  - <span data-ttu-id="54a37-272">Une conférence importante compte 250 utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="54a37-272">One large conference of 250 users.</span></span>

<span data-ttu-id="54a37-273">Le tableau ci-dessous fournit des détails sur le modèle utilisateur pour les conférences auxquelles participent des utilisateurs d’appels entrants.</span><span class="sxs-lookup"><span data-stu-id="54a37-273">The following table provides details about the user model for conferences involving dial-in users.</span></span>

### <a name="dial-in-conferencing-user-model"></a><span data-ttu-id="54a37-274">Modèle utilisateur pour les conférences rendez-vous</span><span class="sxs-lookup"><span data-stu-id="54a37-274">Dial-In Conferencing User Model</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="54a37-275">Catégorie</span><span class="sxs-lookup"><span data-stu-id="54a37-275">Category</span></span></th>
<th><span data-ttu-id="54a37-276">Description</span><span class="sxs-lookup"><span data-stu-id="54a37-276">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="54a37-277">Authentifié/anonyme</span><span class="sxs-lookup"><span data-stu-id="54a37-277">Authenticated/anonymous</span></span></p></td>
<td><p><span data-ttu-id="54a37-p129">70 % des appelants se joignent anonymement et sont invités à entrer un nom enregistré. 30 % participent en tant qu’utilisateurs authentifiés.</span><span class="sxs-lookup"><span data-stu-id="54a37-p129">70% of callers join as anonymous and are prompted for a recorded name. 30% join as authenticated users.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54a37-280">Durée de conversation et attente musicale</span><span class="sxs-lookup"><span data-stu-id="54a37-280">Call duration and music on hold</span></span></p></td>
<td><p><span data-ttu-id="54a37-281">Durée moyenne de conversation sans attente musicale : 50 secondes.</span><span class="sxs-lookup"><span data-stu-id="54a37-281">Average call duration without music on hold: 50 seconds.</span></span></p>
<p><span data-ttu-id="54a37-282">50 % des appelants entendent une musique d’attente pendant 5 minutes en moyenne.</span><span class="sxs-lookup"><span data-stu-id="54a37-282">50% of call-in users hear music on hold, for an average of 5 minutes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54a37-283">Numérotation DTMF</span><span class="sxs-lookup"><span data-stu-id="54a37-283">Dual-tone multifrequency (DTMF)</span></span></p></td>
<td><p><span data-ttu-id="54a37-p130">15 % des conférences rendez-vous ont des responsables téléphoniques. 10 % des conférences mixtes qui incluent des utilisateurs d’appels entrants ont également des responsables téléphoniques.</span><span class="sxs-lookup"><span data-stu-id="54a37-p130">15% of conferences that are dial-in only have phone leaders. 10% of mixed conferences that include dial-in users also have phone leaders.</span></span></p>
<p><span data-ttu-id="54a37-286">20 % des responsables téléphoniques utilisent deux commandes DTMF par conférence.</span><span class="sxs-lookup"><span data-stu-id="54a37-286">20% of phone leaders use 2 DTMF commands per conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54a37-287">Langues d’annonce</span><span class="sxs-lookup"><span data-stu-id="54a37-287">Announcement languages</span></span></p></td>
<td><p><span data-ttu-id="54a37-288">Les simulations utilisent l’anglais comme langue pour les annonces.</span><span class="sxs-lookup"><span data-stu-id="54a37-288">Simulations use English as the announcement language.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="54a37-289">Le tableau ci-dessous fournit des détails sur le modèle utilisateur pour les salles d’attente de conférence.</span><span class="sxs-lookup"><span data-stu-id="54a37-289">The following table provides details about the user model for conference lobbies.</span></span>

### <a name="conference-lobby-user-model"></a><span data-ttu-id="54a37-290">Modèle d’utilisateur pour les salles d’attente de conférence</span><span class="sxs-lookup"><span data-stu-id="54a37-290">Conference Lobby User Model</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="54a37-291">Catégorie</span><span class="sxs-lookup"><span data-stu-id="54a37-291">Category</span></span></th>
<th><span data-ttu-id="54a37-292">Description</span><span class="sxs-lookup"><span data-stu-id="54a37-292">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="54a37-293">Nombre d’utilisateurs dans la salle d’attente</span><span class="sxs-lookup"><span data-stu-id="54a37-293">Number of users in lobby</span></span></p></td>
<td><p><span data-ttu-id="54a37-294">5 % des utilisateurs d’appels entrants et 25 % d’utilisateurs d’autres catégories passent par la salle d’attente.</span><span class="sxs-lookup"><span data-stu-id="54a37-294">5% of dial-in users go through the lobby, and 25% of other users go through the lobby</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54a37-295">Autorisation à quitter la salle d’attente</span><span class="sxs-lookup"><span data-stu-id="54a37-295">Admitting from lobby</span></span></p></td>
<td><p><span data-ttu-id="54a37-296">Pendant les simulations, le présentateur autorise tous les utilisateurs à participer avant l’expiration du délai du client.</span><span class="sxs-lookup"><span data-stu-id="54a37-296">In simulations, all users were admitted by the presenter before client timeout.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="54a37-297">Le tableau ci-dessous décrit le modèle utilisateur pour d’autres sessions P2P.</span><span class="sxs-lookup"><span data-stu-id="54a37-297">The following table describes the user model for other peer-to-peer sessions.</span></span>

### <a name="peer-to-peer-sessions-user-model"></a><span data-ttu-id="54a37-298">Modèle utilisateur pour les sessions P2P</span><span class="sxs-lookup"><span data-stu-id="54a37-298">Peer-to-Peer Sessions User Model</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="54a37-299">Catégorie</span><span class="sxs-lookup"><span data-stu-id="54a37-299">Category</span></span></th>
<th><span data-ttu-id="54a37-300">Description</span><span class="sxs-lookup"><span data-stu-id="54a37-300">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="54a37-301">Partage d’application</span><span class="sxs-lookup"><span data-stu-id="54a37-301">Application sharing</span></span></p></td>
<td><p><span data-ttu-id="54a37-302">Chaque utilisateur participe à cinq sessions de partage d’application P2P par mois, avec une moyenne de 0,25 session par jour.</span><span class="sxs-lookup"><span data-stu-id="54a37-302">Each user participates in 5 peer-to-peer application sharing sessions per month, for an average of 0.25 sessions per day.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54a37-303">Transfert de fichiers</span><span class="sxs-lookup"><span data-stu-id="54a37-303">File transfer</span></span></p></td>
<td><p><span data-ttu-id="54a37-p131">Chaque utilisateur participe à une session de transfert de fichiers P2P par mois (dans le cadre d’une session de messagerie instantanée), avec une moyenne de 0,05 session par jour. En moyenne, le volume transféré lors d’une session est de 1 Mo.</span><span class="sxs-lookup"><span data-stu-id="54a37-p131">Each user participates in 1 peer-to-peer file transfer session per month (as part of an IM session), for an average of 0.05 sessions per day. The average session file size transferred is 1 MB.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="54a37-306">Le tableau ci-dessous décrit le modèle utilisateur pour les stratégies.</span><span class="sxs-lookup"><span data-stu-id="54a37-306">The following table describes the user model for policies.</span></span>

### <a name="policies-user-model"></a><span data-ttu-id="54a37-307">Modèle utilisateur des stratégies</span><span class="sxs-lookup"><span data-stu-id="54a37-307">Policies User Model</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="54a37-308">Catégorie</span><span class="sxs-lookup"><span data-stu-id="54a37-308">Category</span></span></th>
<th><span data-ttu-id="54a37-309">Description</span><span class="sxs-lookup"><span data-stu-id="54a37-309">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="54a37-310">Stratégies de conférence, de présence et d’archivage</span><span class="sxs-lookup"><span data-stu-id="54a37-310">Conferencing, Presence, and Archiving Policies</span></span></p></td>
<td><p><span data-ttu-id="54a37-311">Nous partons du principe qu’il y a une stratégie globale, 10 stratégies de conférence, 4 stratégies d’archivage et 10 stratégies de présence.</span><span class="sxs-lookup"><span data-stu-id="54a37-311">We assume that there is one global policy, 10 tag conferencing policies, 4 Archiving policies, and 10 tag presence policies.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54a37-312">Stratégie vocale</span><span class="sxs-lookup"><span data-stu-id="54a37-312">Voice Policy</span></span></p></td>
<td><p><span data-ttu-id="54a37-313">Nous supposons qu’il existe une stratégie globale et 2 stratégies de mots clés par site.</span><span class="sxs-lookup"><span data-stu-id="54a37-313">We assume that there is one global policy and 2 tag policies per site.</span></span> <span data-ttu-id="54a37-314">100 % des sites ont une stratégie de site et 30 % des utilisateurs sont gérés par une stratégie par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="54a37-314">100% of sites have a site policy, and 30% of users have a per-user policy assigned.</span></span> <span data-ttu-id="54a37-315">Nous prenons pour hypothèse un plan de numérotation par site et deux itinéraires par site.</span><span class="sxs-lookup"><span data-stu-id="54a37-315">We assume one dial plan per site and two routes per site.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="busy-hour"></a><span data-ttu-id="54a37-316">Heure de pointe</span><span class="sxs-lookup"><span data-stu-id="54a37-316">Busy Hour</span></span>

<span data-ttu-id="54a37-p133">Pour les sessions P2P, la charge maximale est calculée à partir des « tentatives d’appels aux heures de pointe » (BHCA). Cette mesure utilisée dans le secteur de la téléphonie suppose que 50 % de tous les appels d’une journée seront passés en 20 % du temps. Elle est calculée à l’aide de la formule suivante :</span><span class="sxs-lookup"><span data-stu-id="54a37-p133">For peer-to-peer sessions, peak load is calculated using busy hour call attempts (BHCA). This voice industry term assumes that 50% of all calls for the day will be completed in 20% of the time. It is calculated using the following formula:</span></span>

`BHCA=(total calls * 0.5) / 1.6`

<span data-ttu-id="54a37-320">Lors d’un test de performance, l’heure de pointe a été simulée en exécutant des sessions VoIP et d’autres sessions P2P aux heures de pointe pendant au moins 1,6 heure par jour.</span><span class="sxs-lookup"><span data-stu-id="54a37-320">Performance testing simulated busy hour by running VoIP and other peer-to-peer sessions at a busy hour load for at least 1.6 hours per day.</span></span>

<span data-ttu-id="54a37-p134">Le pic de charge des conférences suppose que 75 % de toutes les conférences d’une journée de huit heures ont lieu pendant quatre heures de pointe. Ces heures de pointe représentent 1,5 fois la charge de conférence moyenne.</span><span class="sxs-lookup"><span data-stu-id="54a37-p134">Conferencing peak load assumes that 75% of all conferences for an eight-hour day happen in 4 peak time hours. Those peak hours have 1.5 times the average conferencing load.</span></span>

</div>

<div>

## <a name="enterprise-voice-to-pstn-calls"></a><span data-ttu-id="54a37-323">Appels voix entreprise vers RTC</span><span class="sxs-lookup"><span data-stu-id="54a37-323">Enterprise Voice to PSTN Calls</span></span>

<span data-ttu-id="54a37-324">Les affirmations suivantes s’appliquent aux appels vocaux d’entreprise :</span><span class="sxs-lookup"><span data-stu-id="54a37-324">The following assumptions apply to Enterprise Voice calls:</span></span>

  - <span data-ttu-id="54a37-325">50% des utilisateurs sont activés pour voix entreprise et 60% de ces utilisateurs sont activés pour la fonction d’appel RTC.</span><span class="sxs-lookup"><span data-stu-id="54a37-325">50% of users are enabled for Enterprise Voice, and 60% of these users are enabled for PSTN calling.</span></span>

  - <span data-ttu-id="54a37-p135">Chacun de ces derniers utilisateurs passe 4 appels RTC pendant les heures de pointe. Chaque appel dure 3 minutes.</span><span class="sxs-lookup"><span data-stu-id="54a37-p135">Each of these users enabled for PSTN calling makes 4 PSTN calls during the busy hour. Each call duration is 3 minutes.</span></span>

  - <span data-ttu-id="54a37-328">65 % des appels vocaux RTC utilisent la déviation du trafic multimédia.</span><span class="sxs-lookup"><span data-stu-id="54a37-328">65% of these PSTN voice calls use media bypass.</span></span>

</div>

<div>

## <a name="mobility"></a><span data-ttu-id="54a37-329">Mobilité</span><span class="sxs-lookup"><span data-stu-id="54a37-329">Mobility</span></span>

<span data-ttu-id="54a37-p136">40 % des utilisateurs inscrits sont présumés être activés pour la mobilité. Pour chacun d’entre eux, nous partons du principe que l’activité du client mobile vient s’ajouter à celle des autres instances MPOP de l’utilisateur, à l’exception des interactions en conférence pour lesquelles le client de mobilité n’est qu’un autre type de client pouvant être utilisé pour participer à des conférences.</span><span class="sxs-lookup"><span data-stu-id="54a37-p136">40% of registered users are assumed to be enabled for Mobility. For each user that has mobility enabled, we assume that the activity of the mobile client is additive to that of the other MPOP instances for that user, with the exception of conferencing interactions, for which the mobility client is just another client type that can be used to participate in conferences.</span></span>

</div>

<div>

## <a name="persistent-chat"></a><span data-ttu-id="54a37-332">Conversation permanente</span><span class="sxs-lookup"><span data-stu-id="54a37-332">Persistent Chat</span></span>

<span data-ttu-id="54a37-333">Nous supposons que 25 % des utilisateurs inscrits participent à des sessions de conversation permanentes avec les caractéristiques suivantes :</span><span class="sxs-lookup"><span data-stu-id="54a37-333">We assume that 25% of registered users will be involved in Persistent chat sessions, with the following characteristics:</span></span>

  - <span data-ttu-id="54a37-334">1,5 salle de conversation par utilisateur sont prévues en moyenne.</span><span class="sxs-lookup"><span data-stu-id="54a37-334">An average of 1.5 chat rooms per user</span></span>

  - <span data-ttu-id="54a37-335">Chaque salle de conversation engendre 12 demandes d’interrogation par heure, en ciblant une moyenne de 10 utilisateurs chacune.</span><span class="sxs-lookup"><span data-stu-id="54a37-335">Each chat room results in 12 polling requests per hour, targeting an average of 10 users each</span></span>

</div>

<div>

## <a name="response-group-and-call-park"></a><span data-ttu-id="54a37-336">Response Group et parcage d’appel</span><span class="sxs-lookup"><span data-stu-id="54a37-336">Response Group and Call Park</span></span>

<span data-ttu-id="54a37-p137">Nous supposons que 0,15 % des utilisateurs inscrits appartiennent à des groupes Response group. Nous partons du principe que 0,02 % des utilisateurs inscrits ont des appels parqués à tout moment donné.</span><span class="sxs-lookup"><span data-stu-id="54a37-p137">We assume that 0.15% of registered users belong to response groups. We assume that 0.02% of registered users have parked calls at any given point of time.</span></span>

<span data-ttu-id="54a37-339"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="54a37-339"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

