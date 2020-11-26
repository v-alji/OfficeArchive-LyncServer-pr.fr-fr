---
title: 'Lync Server 2013 : installation de Lync pour Windows Phone'
description: 'Lync Server 2013 : installation de Lync pour Windows Phone.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Installing Lync for Windows Phone
ms:assetid: bf502546-ff69-489f-a92e-a78b58803d53
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690996(v=OCS.15)
ms:contentKeyID: 51541513
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6f5da90a5dc0babdc6944e4f9c426fe896d4f156
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427046"
---
# <a name="installing-lync-for-windows-phone-in-lync-server-2013"></a><span data-ttu-id="43fcd-103">Installation de Lync pour Windows Phone dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="43fcd-103">Installing Lync for Windows Phone in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="43fcd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="43fcd-104">

<span> </span></span></span>

<span data-ttu-id="43fcd-105">_**Dernière modification de la rubrique :** 2014-02-03_</span><span class="sxs-lookup"><span data-stu-id="43fcd-105">_**Topic Last Modified:** 2014-02-03_</span></span>

<span data-ttu-id="43fcd-106">Lync 2013 pour Windows Phone est une application qui est disponible sur Windows Phone Marketplace.</span><span class="sxs-lookup"><span data-stu-id="43fcd-106">Lync 2013 for Windows Phone is a user-installable application that is available in the Windows Phone Marketplace.</span></span>

<div>

## <a name="installing-lync-for-windows-mobile"></a><span data-ttu-id="43fcd-107">Installation de Lync pour Windows Mobile</span><span class="sxs-lookup"><span data-stu-id="43fcd-107">Installing Lync for Windows Mobile</span></span>

<span data-ttu-id="43fcd-108">Vous pouvez indiquer à vos utilisateurs d’installer Lync 2013 pour Windows Phone sur leurs appareils en les redirigeant vers Windows Phone Marketplace à l’adresse <https://go.microsoft.com/fwlink/p/?linkid=231901> .</span><span class="sxs-lookup"><span data-stu-id="43fcd-108">You can instruct your users to install Lync 2013 for Windows Phone on their devices by directing them to the Windows Phone Marketplace at <https://go.microsoft.com/fwlink/p/?linkid=231901>.</span></span>

</div>

<div>

## <a name="if-you-use-a-dns-srv-record-to-publish-exchange-web-services"></a><span data-ttu-id="43fcd-109">Si vous utilisez un enregistrement SRV DNS pour publier des services Web Exchange</span><span class="sxs-lookup"><span data-stu-id="43fcd-109">If You Use a DNS SRV Record to Publish Exchange Web Services</span></span>

<span data-ttu-id="43fcd-110">Pour activer l’intégration Exchange pour les clients Lync, certaines organisations publient l’URL du service Web Exchange à l’aide d’un enregistrement SRV DNS.</span><span class="sxs-lookup"><span data-stu-id="43fcd-110">To enable Exchange integration for Lync clients, some organizations publish the Exchange Web Services URL by using a DNS SRV record.</span></span> <span data-ttu-id="43fcd-111">Le document « comprendre et résoudre les problèmes d’intégration d’Exchange », disponible dans le centre de téléchargement Microsoft à [https://go.microsoft.com/fwlink/?LinkID=391095](https://go.microsoft.com/fwlink/?linkid=391095) , décrit les scénarios dans lesquels cela peut être nécessaire.</span><span class="sxs-lookup"><span data-stu-id="43fcd-111">The document "Understanding and Troubleshooting Exchange Integration," available in the Microsoft Download Center at [https://go.microsoft.com/fwlink/?LinkID=391095](https://go.microsoft.com/fwlink/?linkid=391095), describes scenarios in which this might be necessary.</span></span> <span data-ttu-id="43fcd-112">Toutefois, l’intégration Exchange pour les utilisateurs Windows Phone ne fonctionnera pas dans ce scénario, car la plateforme Windows Phone ne prend pas en charge les recherches SRV.</span><span class="sxs-lookup"><span data-stu-id="43fcd-112">However, Exchange integration for Windows Phone users will not work in this scenario, because the Windows Phone platform does not support SRV lookups.</span></span> <span data-ttu-id="43fcd-113">Vous devez indiquer aux utilisateurs Windows Phone de spécifier l’URL du service Web Exchange au lieu de laisser le téléphone détecter automatiquement le serveur.</span><span class="sxs-lookup"><span data-stu-id="43fcd-113">You will need to instruct Windows Phone users to specify the Exchange Web Services URL instead of allowing the phone to automatically detect the server.</span></span>

<span data-ttu-id="43fcd-114">Demandez à vos utilisateurs de configurer les paramètres Lync sur leurs téléphones Windows comme suit :</span><span class="sxs-lookup"><span data-stu-id="43fcd-114">Instruct your users to configure the Lync settings on their Windows Phones as follows:</span></span>

1.  <span data-ttu-id="43fcd-115">Dans les paramètres de Lync pour Windows Phone, sélectionnez l’écran **Exchange** .</span><span class="sxs-lookup"><span data-stu-id="43fcd-115">In Windows Phone, in the Lync settings, select the **Exchange** screen.</span></span>

2.  <span data-ttu-id="43fcd-116">Pour **Désactiver** l’option **détecter automatiquement le serveur,**</span><span class="sxs-lookup"><span data-stu-id="43fcd-116">Move **Auto-Detect Server** to **Off**.</span></span>

3.  <span data-ttu-id="43fcd-117">Appuyez sur le champ vide, puis entrez le nom de domaine complet (FQDN) ou l’URL des services Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="43fcd-117">Tap the empty field and enter the fully qualified domain name (FQDN) or URL for Exchange Web Services.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="43fcd-118">Vous pouvez spécifier le nom de domaine complet (FQDN) ou l’URL complète de votre serveur de services Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="43fcd-118">You can specify either the fully qualified domain name (FQDN) or the full URL of your Exchange Web Services server.</span></span> <span data-ttu-id="43fcd-119">Si vous spécifiez le nom de domaine complet, le protocole (https://) et le chemin d’accès aux services Web Exchange (/EWS/Exchange.asmx) sont automatiquement ajoutés.</span><span class="sxs-lookup"><span data-stu-id="43fcd-119">If you specify the FQDN, the protocol (https://) and the Exchange Web Services path (/ews/exchange.asmx) are added automatically.</span></span> <span data-ttu-id="43fcd-120">Si votre chemin d’accès aux services Web Exchange est différent, vous pouvez spécifier l’URL complète.</span><span class="sxs-lookup"><span data-stu-id="43fcd-120">If your Exchange Web Services path is different, you can specify the full URL.</span></span>

    
    </div>

4.  <span data-ttu-id="43fcd-121">Fermez l’écran.</span><span class="sxs-lookup"><span data-stu-id="43fcd-121">Close the screen.</span></span>

</div>

<div>

## <a name="verifying-mobile-client-installation"></a><span data-ttu-id="43fcd-122">Vérification de l’installation du client mobile</span><span class="sxs-lookup"><span data-stu-id="43fcd-122">Verifying Mobile Client Installation</span></span>

<span data-ttu-id="43fcd-123">Après avoir configuré le client et que vous êtes connecté avec succès, utilisez les tests suivants pour vérifier que votre installation de Lync 2013 fonctionne correctement sur votre appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="43fcd-123">After you configure the client and sign in successfully, use the following tests to verify that your installation of Lync 2013 is working correctly on your mobile device.</span></span>

<span data-ttu-id="43fcd-124">**Recherche d’un contact dans l’annuaire d’entreprise**</span><span class="sxs-lookup"><span data-stu-id="43fcd-124">**Search for a contact in the corporate directory**</span></span>

1.  <span data-ttu-id="43fcd-125">Dans la liste des contacts, appuyez sur **Rechercher** en bas.</span><span class="sxs-lookup"><span data-stu-id="43fcd-125">In the Contacts list, tap **Search** at the bottom.</span></span>

2.  <span data-ttu-id="43fcd-126">Recherchez un contact qui n’existe que dans la liste d’adresses globale.</span><span class="sxs-lookup"><span data-stu-id="43fcd-126">Search for a contact that exists only in the global address list.</span></span>

3.  <span data-ttu-id="43fcd-127">Vérifiez que le nom du contact figure dans les résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="43fcd-127">Verify that the contact name appears in the search results.</span></span>

<span data-ttu-id="43fcd-128">**Test de la messagerie instantanée et de la présence**</span><span class="sxs-lookup"><span data-stu-id="43fcd-128">**Test instant messaging and presence**</span></span>

1.  <span data-ttu-id="43fcd-129">Dans la liste Contacts, tapez sur un contact.</span><span class="sxs-lookup"><span data-stu-id="43fcd-129">In the Contacts list, tap a contact.</span></span>

2.  <span data-ttu-id="43fcd-130">Sur la carte de visite, appuyez sur l’icône de **messagerie instantanée** .</span><span class="sxs-lookup"><span data-stu-id="43fcd-130">In the contact card, tap the **IM** icon.</span></span>

3.  <span data-ttu-id="43fcd-131">Vérifiez qu’une fenêtre de messagerie instantanée apparaît et que vous pouvez taper et envoyer un message instantané.</span><span class="sxs-lookup"><span data-stu-id="43fcd-131">Verify that an instant messaging (IM) window appears and that you can type and send an IM.</span></span>

<span data-ttu-id="43fcd-132">**Test de la conférence rendez-vous**</span><span class="sxs-lookup"><span data-stu-id="43fcd-132">**Test dial-out conferencing**</span></span>

1.  <span data-ttu-id="43fcd-133">Dans Outlook, planifiez une réunion Lync.</span><span class="sxs-lookup"><span data-stu-id="43fcd-133">In Outlook, schedule a Lync meeting.</span></span>

2.  <span data-ttu-id="43fcd-134">Sur l’appareil mobile, ouvrez l’invitation à la réunion.</span><span class="sxs-lookup"><span data-stu-id="43fcd-134">On the mobile device, open the meeting invitation.</span></span>

3.  <span data-ttu-id="43fcd-135">Cliquez sur le lien dans la réunion afin de la rejoindre.</span><span class="sxs-lookup"><span data-stu-id="43fcd-135">Click the link in the meeting to join.</span></span>

4.  <span data-ttu-id="43fcd-136">Répondez à l’appel du service de conférence et vérifiez que vous êtes connecté au système audio de la réunion.</span><span class="sxs-lookup"><span data-stu-id="43fcd-136">Answer the call from the conference service and verify that you are connected to meeting audio.</span></span>

<span data-ttu-id="43fcd-137">**Test des notifications Push**</span><span class="sxs-lookup"><span data-stu-id="43fcd-137">**Test push notifications**</span></span>

1.  <span data-ttu-id="43fcd-138">Sur l’appareil mobile de l’utilisateur, connectez-vous à Lync avec le compte de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="43fcd-138">On user A’s mobile device, sign in to Lync with user A’s account.</span></span>

2.  <span data-ttu-id="43fcd-139">Ouvrez une autre application sur l’appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="43fcd-139">Open another application on the mobile device.</span></span>

3.  <span data-ttu-id="43fcd-140">Sur un autre client, connectez-vous à Lync avec le compte de l’utilisateur B.</span><span class="sxs-lookup"><span data-stu-id="43fcd-140">On a different client, sign in to Lync with user B’s account.</span></span>

4.  <span data-ttu-id="43fcd-141">Envoyez un message instantané de l’utilisateur B à l’utilisateur A.</span><span class="sxs-lookup"><span data-stu-id="43fcd-141">Send an IM from user B to user A.</span></span>

5.  <span data-ttu-id="43fcd-142">Vérifiez que la notification de messagerie instantanée s’affiche sur l’appareil mobile de l’utilisateur A.</span><span class="sxs-lookup"><span data-stu-id="43fcd-142">Verify that the IM notification appears on user A’s mobile device.</span></span>

<span data-ttu-id="43fcd-143"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="43fcd-143"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

