---
title: 'Lync Server 2013 : Utilisation de la connectivité Lync-Skype en tant qu’utilisateur final'
description: 'Lync Server 2013 : utilisation de Lync-Skype connectivité en tant qu’utilisateur final.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Using Lync-Skype connectivity as an end user
ms:assetid: ad22f731-118c-4349-8790-b1a72941cbdd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn440175(v=OCS.15)
ms:contentKeyID: 57793365
ms.date: 12/29/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dd669a5cf0b15f7fb2d411e4456553f5469d9f96
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438917"
---
# <a name="using-lync-skype-connectivity-in-lync-server-2013-as-an-end-user"></a><span data-ttu-id="b838e-103">Utilisation de la connectivité Lync-Skype dans Lync Server 2013 en tant qu’utilisateur final</span><span class="sxs-lookup"><span data-stu-id="b838e-103">Using Lync-Skype connectivity in Lync Server 2013 as an end user</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b838e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b838e-104">

<span> </span></span></span>

<span data-ttu-id="b838e-105">_**Dernière modification de la rubrique :** 2016-12-27_</span><span class="sxs-lookup"><span data-stu-id="b838e-105">_**Topic Last Modified:** 2016-12-27_</span></span>

<span data-ttu-id="b838e-106">Lync-Skype connectivité permet aux utilisateurs de Skype et aux utilisateurs de Lync de s’ajouter aux contacts, d’échanger des messages instantanés et d’effectuer des appels audio et vidéo.</span><span class="sxs-lookup"><span data-stu-id="b838e-106">Lync-Skype Connectivity enables Skype users and Lync users to add each other as contacts, exchange instant messages and make audio and video calls.</span></span> <span data-ttu-id="b838e-107">Lorsqu’un utilisateur de Skype ajoute un utilisateur Lync, un utilisateur Skype crée un contact dans Skype contenant l’URI (Uniform Resource Identifier) de l’utilisateur Lync.</span><span class="sxs-lookup"><span data-stu-id="b838e-107">When a Skype user adds a Lync user, a Skype user will create a contact in Skype containing the session initiation protocol (SIP) uniform resource identifier (URI) of the Lync user.</span></span> <span data-ttu-id="b838e-108">À l’inverse, quand un utilisateur de Lync ajoute un contact Skype, l’utilisateur de Lync crée un contact dans Lync qui contient le compte Microsoft (MSA) de l’utilisateur Skype, et non le nom d’utilisateur Skype.</span><span class="sxs-lookup"><span data-stu-id="b838e-108">Conversely, when a Lync user adds a Skype contact, the Lync user will create a contact in Lync that will contain the Microsoft Account (MSA) of the Skype user, and not the Skype user name.</span></span>

<span data-ttu-id="b838e-109">**Qu’est-ce qu’un MSA ?**</span><span class="sxs-lookup"><span data-stu-id="b838e-109">**What is an MSA?**</span></span> <span data-ttu-id="b838e-110">Les utilisateurs de Skype doivent se connecter à Skype avec un compte Microsoft (auparavant appelé Windows Live ID) pour communiquer avec des contacts Lync.</span><span class="sxs-lookup"><span data-stu-id="b838e-110">Skype users must sign in to Skype with a Microsoft account (previously called Windows Live ID) in order to communicate with Lync contacts.</span></span> <span data-ttu-id="b838e-111">Un compte Microsoft repose sur la combinaison d’une adresse de messagerie et d’un mot de passe, que vous pouvez également utiliser pour vous connecter à des services tels que la technologie de stockage Microsoft OneDrive, Windows Phone, le service de jeu Microsoft Xbox LIVE Online et le client de messagerie et de collaboration Microsoft Outlook (et, auparavant, service de messagerie Web Microsoft Hotmail ou Windows Live Messenger).</span><span class="sxs-lookup"><span data-stu-id="b838e-111">A Microsoft account consists of the combination of an email address and a password, which you can also use to sign in to services such as Microsoft OneDrive storage technology, Windows Phone, Microsoft Xbox LIVE online game service, and Microsoft Outlook messaging and collaboration client (and, previously, Microsoft Hotmail web-based e-mail service or Windows Live Messenger).</span></span> <span data-ttu-id="b838e-112">Si vous utilisez une adresse de messagerie et un mot de passe pour vous connecter à ces services, vous disposez déjà d’un compte Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b838e-112">If you use an email address and a password to sign in to these or other services, you already have a Microsoft account.</span></span> <span data-ttu-id="b838e-113">Pour plus d’informations sur la création d’un compte Microsoft, reportez-vous à la page de connexion au compte Microsoft à l’adresse [https://go.microsoft.com/fwlink/p/?LinkId=306061](https://go.microsoft.com/fwlink/p/?linkid=306061) .</span><span class="sxs-lookup"><span data-stu-id="b838e-113">For details about creating a Microsoft Account, see the Microsoft account sign-up page at [https://go.microsoft.com/fwlink/p/?LinkId=306061](https://go.microsoft.com/fwlink/p/?linkid=306061).</span></span> <span data-ttu-id="b838e-114">Vous pouvez fusionner votre compte Skype existant avec votre compte Microsoft pour l’authentification unique, dans de nombreuses applications et services.</span><span class="sxs-lookup"><span data-stu-id="b838e-114">You can merge your existing Skype account with your Microsoft account for single sign-on, across a variety of applications and services.</span></span> <span data-ttu-id="b838e-115">Une fois le compte fusionné, l’utilisateur de Skype peut envoyer une demande de contact aux utilisateurs de Lync.</span><span class="sxs-lookup"><span data-stu-id="b838e-115">Once the account is merged a Skype user can send a contact request to Lync users.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="b838e-116">Pour que les utilisateurs de Lync et Skype puissent communiquer de manière complète, les conditions suivantes doivent être remplies :</span><span class="sxs-lookup"><span data-stu-id="b838e-116">In order for Lync and Skype users to fully communicate with each other, the following requirements must be met:</span></span> 
> <UL>
> <LI>
> <P><span data-ttu-id="b838e-117">Les utilisateurs de Skype doivent être connectés à leur client Skype avec un compte Microsoft (MSA).</span><span class="sxs-lookup"><span data-stu-id="b838e-117">Skype users must be logged into their Skype client with a Microsoft Account (MSA).</span></span></P>
> <LI>
> <P><span data-ttu-id="b838e-118">Les utilisateurs de Lync doivent être activés pour la connectivité PIC (Public IM Connectivity) par leur administrateur Lync.</span><span class="sxs-lookup"><span data-stu-id="b838e-118">Lync users must be enabled for public IM connectivity by their Lync administrator.</span></span></P>
> <LI>
> <P><span data-ttu-id="b838e-119">Lorsqu’un utilisateur Skype ajoute un contact Lync, vérifiez que le mot Lync apparaît sous le nom du contact.</span><span class="sxs-lookup"><span data-stu-id="b838e-119">When a Skype user adds a Lync contact, verify that the word Lync appears below the contact’s name.</span></span> <span data-ttu-id="b838e-120">Cela indique qu’un URI Lync a été trouvé.</span><span class="sxs-lookup"><span data-stu-id="b838e-120">This indicates that a Lync URI has been found.</span></span></P>
> <LI>
> <P><span data-ttu-id="b838e-121">Lorsqu’un utilisateur Skype ajoute un contact Lync et que les résultats de la recherche ne sont pas retournés pour ce domaine Lync, le processus de mise en service de PIC n’est peut-être pas terminé ou le domaine Lync n’a pas encore été configuré.</span><span class="sxs-lookup"><span data-stu-id="b838e-121">When a Skype user adds a Lync contact and zero search results are returned for that Lync domain, the PIC provisioning process may not have completed, or the Lync domain has not yet been set up.</span></span></P>
> <LI>
> <P><span data-ttu-id="b838e-122">En fonction des paramètres de confidentialité de Lync et des utilisateurs Skype, la messagerie instantanée, la vidéo et la présence risquent de ne pas fonctionner tant que les nouveaux contacts ne sont pas acceptés par chaque utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b838e-122">Depending on the privacy settings of the Lync and Skype users, IM, video, and presence may not work until the new contacts are accepted by each user.</span></span></P></LI></UL>



</div>

<span data-ttu-id="b838e-123">**Pour ajouter un contact Skype à Lync 2013**</span><span class="sxs-lookup"><span data-stu-id="b838e-123">**To add a Skype contact to Lync 2013**</span></span>

1.  <span data-ttu-id="b838e-124">Dans Lync, cliquez sur **Ajouter un contact, puis ajoutez un contact qui n’est pas dans ma société**.</span><span class="sxs-lookup"><span data-stu-id="b838e-124">From Lync, click **Add a Contact, Add a Contact Not in My Organization**.</span></span>

2.  <span data-ttu-id="b838e-125">Dans la liste des fournisseurs de contacts disponibles, sélectionnez **Skype**.</span><span class="sxs-lookup"><span data-stu-id="b838e-125">From the list of available contact providers, select **Skype**.</span></span>

3.  <span data-ttu-id="b838e-126">Dans le champ **adresse de messagerie instantanée** , entrez le compte Microsoft (MSA) de l’utilisateur Skype.</span><span class="sxs-lookup"><span data-stu-id="b838e-126">In the **IM Address** field, enter the Microsoft Account (MSA) of the Skype user.</span></span>

4.  <span data-ttu-id="b838e-127">Dans la liste déroulante **Ajouter au groupe de contacts** , sélectionnez le groupe de contacts auquel vous souhaitez ajouter l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b838e-127">In the **Add to contact group** dropdown box, select a contact group to add the user to.</span></span>

5.  <span data-ttu-id="b838e-128">Dans la liste déroulante **définir la relation de confidentialité** , sélectionnez le paramètre de contact approprié, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="b838e-128">In the **Set privacy relationship** dropdown box, select the appropriate contact setting and then click **OK**.</span></span>

6.  <span data-ttu-id="b838e-129">L’utilisateur s’affiche désormais comme contact dans Lync.</span><span class="sxs-lookup"><span data-stu-id="b838e-129">The user will now appear as a contact in Lync.</span></span> <span data-ttu-id="b838e-130">Sélectionnez l’utilisateur, cliquez avec le bouton droit sur le nom d’utilisateur, puis cliquez sur **afficher la carte de visite** pour afficher les propriétés de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b838e-130">Select the user, right-click the user name, and click **See Contact Card** to view the user properties.</span></span> <span data-ttu-id="b838e-131">Vous pouvez désormais passer un appel audio ou vidéo à l’aide de l’utilisateur Skype que vous venez d’ajouter.</span><span class="sxs-lookup"><span data-stu-id="b838e-131">You can now establish an audio or video call with the newly added Skype user.</span></span>

<span data-ttu-id="b838e-132">Pour plus d’informations sur la prise en charge des contacts, consultez [Ajouter un contact dans Lync](https://support.office.com/article/add-a-contact-ae55b88d-b9af-48da-bffe-7cc720a5059a).</span><span class="sxs-lookup"><span data-stu-id="b838e-132">For additional information on support for contacts, see [Add a contact in Lync](https://support.office.com/article/add-a-contact-ae55b88d-b9af-48da-bffe-7cc720a5059a).</span></span>

<span data-ttu-id="b838e-133">Lorsque le compte Microsoft d’un utilisateur Skype utilise un nom de domaine personnalisé, tel que <strong>Bob@contoso.com</strong> , un utilisateur de Lync peut ajouter ce compte Microsoft à Lync de deux manières :</span><span class="sxs-lookup"><span data-stu-id="b838e-133">When a Skype user’s Microsoft account uses a custom domain name, such as <strong>bob@contoso.com</strong> , a Lync user can add that Microsoft account to Lync in two ways:</span></span>

1.  <span data-ttu-id="b838e-134">Utilisez l’icône **Ajouter un contact** ou</span><span class="sxs-lookup"><span data-stu-id="b838e-134">Use the **Add a Contact** icon, or</span></span>

2.  <span data-ttu-id="b838e-135">Utilisez le champ **Rechercher une personne ou une salle ou un numéro de** téléphone.</span><span class="sxs-lookup"><span data-stu-id="b838e-135">Use the **Find someone or a room, or a dial a number** field.</span></span>

<span data-ttu-id="b838e-136">Dans chaque instance, l’utilisateur de Lync doit entrer l’adresse e-mail de l’utilisateur Skype au format suivant : <strong>utilisateur (nom de domaine) @msn. com</strong> .</span><span class="sxs-lookup"><span data-stu-id="b838e-136">In each instance, the Lync user must enter the Skype user’s email in the following format: <strong>user(domain name)@msn.com</strong> .</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="b838e-137">Cette étape n’est pas requise pour les comptes Microsoft qui utilisent les noms de domaine suivants : <STRONG>@live. com, @hotmail. com ou @outlook. com</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="b838e-137">This step is not required for Microsoft accounts that use the following domain names: <STRONG>@live.com, @hotmail.com or @outlook.com</STRONG>.</span></span> <span data-ttu-id="b838e-138">Pour plus d’informations sur les noms de domaine personnalisés pris en charge, voir <A href="https://support.microsoft.com/kb/897567">domaines de messagerie instantanée publics pris en charge</A>.</span><span class="sxs-lookup"><span data-stu-id="b838e-138">For more information on supported custom domain names, see <A href="https://support.microsoft.com/kb/897567">Supported public IM domains</A>.</span></span>



</div>

<span data-ttu-id="b838e-139">**Pour ajouter un contact Skype à Lync lors de l’utilisation d’un nom de domaine personnalisé**</span><span class="sxs-lookup"><span data-stu-id="b838e-139">**To add a Skype contact to Lync when using a custom domain name**</span></span>

1.  <span data-ttu-id="b838e-140">Dans Lync, cliquez sur **Ajouter un contact, puis ajoutez un contact qui n’est pas dans ma société**.</span><span class="sxs-lookup"><span data-stu-id="b838e-140">From Lync, click **Add a Contact, Add a Contact Not in My Organization**.</span></span>

2.  <span data-ttu-id="b838e-141">Dans la liste des fournisseurs de contacts disponibles, sélectionnez **Skype**.</span><span class="sxs-lookup"><span data-stu-id="b838e-141">From the list of available contact providers, select **Skype**.</span></span>

3.  <span data-ttu-id="b838e-142">Dans le champ **adresse de messagerie instantanée** , entrez le compte Microsoft (MSA) de l’utilisateur Skype au format <strong>utilisateur (nom de domaine) @msn. com</strong>.</span><span class="sxs-lookup"><span data-stu-id="b838e-142">In the **IM Address** field, enter the Microsoft Account (MSA) of the Skype user in the format <strong>user(domain name)@msn.com</strong>.</span></span> <span data-ttu-id="b838e-143">Ainsi, pour l’utilisateur bob@contoso.com, l’entrée est <strong> Bob (contoso. com) @msn. com <strong> .</span><span class="sxs-lookup"><span data-stu-id="b838e-143">So for user bob@contoso.com, the entry would be <strong>bob(contoso.com)@msn.com<strong> .</span></span>

4.  <span data-ttu-id="b838e-144">Dans la zone de liste déroulante **Ajouter au groupe de contacts** , sélectionnez le groupe de contacts auquel vous souhaitez ajouter l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b838e-144">In the **Add to contact group** drop-down list box, select a contact group to add the user to.</span></span>

5.  <span data-ttu-id="b838e-145">Dans la zone de liste déroulante **définir la relation de confidentialité** , sélectionnez le paramètre de contact approprié, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="b838e-145">In the **Set privacy relationship** drop-down list box, select the appropriate contact setting and then click **OK**.</span></span>

6.  <span data-ttu-id="b838e-146">Un utilisateur de Lync peut également utiliser le champ **Rechercher une personne ou une salle ou composer un numéro** dans Lync et ajouter une adresse qui ressemble à l' <strong>utilisateur suivant (nom de domaine) @msn. com</strong> .</span><span class="sxs-lookup"><span data-stu-id="b838e-146">A Lync user can also use the **Find someone or a room, or dial a number** field in Lync, and add an address that resembles the following <strong>user(domain name)@msn.com</strong> .</span></span> <span data-ttu-id="b838e-147">Pour le compte Microsoft bob@contoso.com, l’entrée est <strong>Bob (contoso. com) @msn. com</strong> .</span><span class="sxs-lookup"><span data-stu-id="b838e-147">So for the bob@contoso.com Microsoft account, the entry would be <strong>bob(contoso.com)@msn.com</strong> .</span></span>

7.  <span data-ttu-id="b838e-148">Suivez les étapes 4 et 5 décrites plus haut dans cette procédure pour ajouter le contact à un groupe de contacts et pour sélectionner la relation de confidentialité appropriée.</span><span class="sxs-lookup"><span data-stu-id="b838e-148">Follow steps 4 and 5 earlier in this procedure to add the contact to a contact group and to select the appropriate privacy relationship.</span></span>

<span data-ttu-id="b838e-149">**Pour ajouter un contact Lync à Skype**</span><span class="sxs-lookup"><span data-stu-id="b838e-149">**To add a Lync contact to Skype**</span></span>

1.  <span data-ttu-id="b838e-150">Connectez-vous à Skype.</span><span class="sxs-lookup"><span data-stu-id="b838e-150">Sign in to Skype.</span></span> <span data-ttu-id="b838e-151">L’utilisateur Skype doit être connecté à son client Skype avec un compte Microsoft (MSA).</span><span class="sxs-lookup"><span data-stu-id="b838e-151">The Skype user must be logged into their Skype client with a Microsoft Account (MSA).</span></span>

2.  <span data-ttu-id="b838e-152">Sélectionnez l’icône Ajouter des contacts.</span><span class="sxs-lookup"><span data-stu-id="b838e-152">Select the Add Contacts icon.</span></span>

3.  <span data-ttu-id="b838e-153">Entrez l’URI SIP de l’utilisateur Lync.</span><span class="sxs-lookup"><span data-stu-id="b838e-153">Enter the SIP URI of the Lync user.</span></span> <span data-ttu-id="b838e-154">Par exemple, bob@contoso.com.</span><span class="sxs-lookup"><span data-stu-id="b838e-154">For example, bob@contoso.com.</span></span>

4.  <span data-ttu-id="b838e-155">Lorsque Skype trouve la correspondance dans les résultats de recherche, recherchez le mot **Lync** sous le nom de l’utilisateur Lync.</span><span class="sxs-lookup"><span data-stu-id="b838e-155">When Skype finds the match in the search results, look for the word **Lync** below the Lync user’s name.</span></span> <span data-ttu-id="b838e-156">Cela indique que Skype a trouvé l’URI SIP du client Lync.</span><span class="sxs-lookup"><span data-stu-id="b838e-156">This indicates Skype successfully located the Lync client’s SIP URI.</span></span> <span data-ttu-id="b838e-157">Cliquez sur le nom.</span><span class="sxs-lookup"><span data-stu-id="b838e-157">Click the name.</span></span>

5.  <span data-ttu-id="b838e-158">Dans le coin supérieur droit de la fenêtre, cliquez sur Ajouter aux contacts.</span><span class="sxs-lookup"><span data-stu-id="b838e-158">In the top right corner of the window, click Add to Contacts.</span></span>

6.  <span data-ttu-id="b838e-159">Le nouveau contact est désormais ajouté à votre liste de contacts, mais un point d’interrogation est affiché au lieu de son icône de statut jusqu’à ce qu’il accepte votre demande.</span><span class="sxs-lookup"><span data-stu-id="b838e-159">The new contact is now added to your contact list, but you’ll see a question mark instead of their status icon until they accept your request.</span></span> <span data-ttu-id="b838e-160">Lorsque votre contact a accepté votre demande, vous pouvez voir quand il est en ligne, lancer des conversations par messagerie instantanée et effectuer des appels audio et vidéo.</span><span class="sxs-lookup"><span data-stu-id="b838e-160">When your new contact accepts your request, you will be able to see when they are online, initiate IM conversations, and make audio and video calls.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="b838e-161">L’administrateur du serveur Lync doit configurer les paramètres de stratégie de l’utilisateur Lync pour autoriser les demandes entrantes.</span><span class="sxs-lookup"><span data-stu-id="b838e-161">The Lync Server administrator must configure the Lync user’s policy settings to allow incoming requests.</span></span> <span data-ttu-id="b838e-162">Si ce n’est pas le cas, l’utilisateur de Lync n’aura pas reçu de demandes de contact de l’utilisateur Skype.</span><span class="sxs-lookup"><span data-stu-id="b838e-162">If not, the Lync user will not receive contact requests from the Skype user.</span></span> <span data-ttu-id="b838e-163">En fonction de la configuration des paramètres de stratégie de l’utilisateur Lync, la demande d’ajout de l’utilisateur Skype apparaît sous l’onglet <STRONG>nouveau</STRONG> du client Lync. Pour commencer à communiquer avec l’utilisateur Skype, l’utilisateur de Lync doit ajouter l’utilisateur Skype à la liste de favoris ou à une liste de contacts.</span><span class="sxs-lookup"><span data-stu-id="b838e-163">Depending on the configuration of the Lync user’s policy settings, the request to add the Skype user will appear on the Lync client’s <STRONG>New</STRONG> tab. To begin communicating with the Skype user, the Lync user must add the Skype user to either the Favorites list or a contact list.</span></span> <span data-ttu-id="b838e-164">L’image ci-dessous montre l’emplacement du <STRONG>nouvel</STRONG> onglet dans le client Lync.</span><span class="sxs-lookup"><span data-stu-id="b838e-164">The image below shows the location of the <STRONG>New</STRONG> tab in the Lync client.</span></span>

    
    </div>

<span data-ttu-id="b838e-165">Un utilisateur de Lync doit configurer des alertes Lync pour s’assurer que les demandes envoyées à partir d’un utilisateur Skype apparaissent et qu’ils peuvent être détectés par l’utilisateur de Lync.</span><span class="sxs-lookup"><span data-stu-id="b838e-165">A Lync user must configure Lync alerts to ensure that requests sent from a Skype user appear and are discoverable by the Lync user.</span></span> <span data-ttu-id="b838e-166">Pour configurer les alertes Lync, suivez la procédure ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="b838e-166">To configure Lync alerts, complete the procedure that follows.</span></span>

<span data-ttu-id="b838e-167">**Pour configurer les alertes Lync**</span><span class="sxs-lookup"><span data-stu-id="b838e-167">**To configure Lync Alerts**</span></span>

1.  <span data-ttu-id="b838e-168">Dans le client Lync, cliquez sur l’icône **options** .</span><span class="sxs-lookup"><span data-stu-id="b838e-168">From the Lync client, click the **Options** icon.</span></span>

2.  <span data-ttu-id="b838e-169">Sélectionnez **alertes**.</span><span class="sxs-lookup"><span data-stu-id="b838e-169">Select **Alerts**.</span></span>

3.  <span data-ttu-id="b838e-170">Sous **alertes générales**, activez la case à cocher m’avertir **quand une personne m’ajoute à sa liste de contacts**.</span><span class="sxs-lookup"><span data-stu-id="b838e-170">Under **General alerts**, check **Tell me when someone adds me to his or her contact list**.</span></span>

4.  <span data-ttu-id="b838e-171">Sous **contacts n’utilisant pas Lync**, sélectionnez **autoriser les invitations, mais bloquer toutes les autres communications**.</span><span class="sxs-lookup"><span data-stu-id="b838e-171">Under **Contacts not using Lync**, select **Allow invites but block all other communications**.</span></span>

5.  <span data-ttu-id="b838e-172">Cliquez sur **OK** pour fermer la fenêtre d’options.</span><span class="sxs-lookup"><span data-stu-id="b838e-172">Click **OK** to close the Options window.</span></span>

<span data-ttu-id="b838e-173"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b838e-173"></div>

<span> </span>

</div>

</div>

</span></span></div>

