---
title: 'Lync Server 2013 : utilisation de l’authentification à deux facteurs avec le client Lync'
description: 'Lync Server 2013 : utilisation de l’authentification à deux facteurs avec le client Lync.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Using two-factor authentication with Lync client
ms:assetid: d4136e61-c3ab-4b26-85c8-c1b2c24f5ee3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn338071(v=OCS.15)
ms:contentKeyID: 55115593
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dbfde1d04d4e641c8fbe4817ffce214df891b565
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438686"
---
# <a name="using-two-factor-authentication-with-lync-client-and-lync-server-2013"></a><span data-ttu-id="55deb-103">Utilisation de l’authentification à deux facteurs avec le client Lync et Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="55deb-103">Using two-factor authentication with Lync client and Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="55deb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="55deb-104">

<span> </span></span></span>

<span data-ttu-id="55deb-105">_**Dernière modification de la rubrique :** 2013-07-11_</span><span class="sxs-lookup"><span data-stu-id="55deb-105">_**Topic Last Modified:** 2013-07-11_</span></span>

<span data-ttu-id="55deb-106">Cette rubrique vous explique comment tirer parti de l’authentification à deux facteurs avec le client 2013 Lync.</span><span class="sxs-lookup"><span data-stu-id="55deb-106">This topic described how to take advantage of two-factor authentication with Lync 2013 client.</span></span>

<div>

## <a name="sign-in-to-lync-2013-for-the-first-time"></a><span data-ttu-id="55deb-107">Se connecter à Lync 2013 pour la première fois</span><span class="sxs-lookup"><span data-stu-id="55deb-107">Sign in to Lync 2013 for the first time</span></span>

<span data-ttu-id="55deb-108">Vos informations de connexion à Lync sont généralement configurées automatiquement lorsque Lync 2013 est installé.</span><span class="sxs-lookup"><span data-stu-id="55deb-108">Your Lync sign-in information is usually configured automatically when Lync 2013 is installed.</span></span> <span data-ttu-id="55deb-109">La première fois que vous utilisez Lync, il est possible que vous deviez démarrer manuellement le client.</span><span class="sxs-lookup"><span data-stu-id="55deb-109">But the first time you use Lync, you might have to manually start the client.</span></span>

<span data-ttu-id="55deb-110">**Pour vous connecter à Lync pour la première fois**</span><span class="sxs-lookup"><span data-stu-id="55deb-110">**To sign in to Lync for the first time**</span></span>

1.  <span data-ttu-id="55deb-111">Ouvrez une session sur le réseau de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="55deb-111">Log on to your organization’s network.</span></span>

2.  <span data-ttu-id="55deb-112">Sélectionnez **Démarrer** \> **tous les programmes** \> **Microsoft Lync \> Lync 2013**.</span><span class="sxs-lookup"><span data-stu-id="55deb-112">Select **Start** \> **All Programs** \> **Microsoft Lync \> Lync 2013**.</span></span>
    
    <span data-ttu-id="55deb-113">L’écran de connexion Lync doit apparaître.</span><span class="sxs-lookup"><span data-stu-id="55deb-113">You should see the Lync sign-in screen.</span></span>
    
      - <span data-ttu-id="55deb-114">Si la zone Adresse de connexion est déjà renseignée, vérifiez que l’adresse affichée est correcte.</span><span class="sxs-lookup"><span data-stu-id="55deb-114">If the sign-in address box is already filled in, confirm that the address shown is correct.</span></span>
    
      - <span data-ttu-id="55deb-115">Si ce n’est pas le cas, ou si la zone est vide, entrez votre adresse de connexion Lync (il s’agit généralement de votre adresse de messagerie).</span><span class="sxs-lookup"><span data-stu-id="55deb-115">If it’s not correct, or if the box is empty, enter your Lync sign-in address (this is usually the same as your email address).</span></span>
    
      - <span data-ttu-id="55deb-116">Si la zone Mot de passe qui s’affiche n’est pas renseignée, ajoutez votre mot de passe.</span><span class="sxs-lookup"><span data-stu-id="55deb-116">If an empty password box is displayed, add your password.</span></span>

3.  <span data-ttu-id="55deb-117">Sélectionnez **Se connecter**.</span><span class="sxs-lookup"><span data-stu-id="55deb-117">Select **Sign-in**.</span></span>

</div>

<div>

## <a name="sign-out-of-lync"></a><span data-ttu-id="55deb-118">Se déconnecter de Lync</span><span class="sxs-lookup"><span data-stu-id="55deb-118">Sign out of Lync</span></span>

<span data-ttu-id="55deb-119">Lorsque vous avez terminé d’utiliser Lync, vous pouvez fermer l’affichage, vous déconnecter de votre session ou quitter le programme à partir du menu fichier.</span><span class="sxs-lookup"><span data-stu-id="55deb-119">When you’re finished using Lync, you can close the display, sign out of your session, or exit from the program, all from the File menu.</span></span> <span data-ttu-id="55deb-120">Le tableau ci-dessous explique les différences entre ces trois options :</span><span class="sxs-lookup"><span data-stu-id="55deb-120">The following table explains the differences in the options.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="55deb-121">Option</span><span class="sxs-lookup"><span data-stu-id="55deb-121">Option</span></span></th>
<th><span data-ttu-id="55deb-122">Action</span><span class="sxs-lookup"><span data-stu-id="55deb-122">What it does</span></span></th>
<th><span data-ttu-id="55deb-123">Utilisation</span><span class="sxs-lookup"><span data-stu-id="55deb-123">How to perform it</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="55deb-124">Fermer</span><span class="sxs-lookup"><span data-stu-id="55deb-124">Close</span></span></p></td>
<td><p><span data-ttu-id="55deb-125">Ferme votre affichage Lync tout en permettant à la session Lync identifiée avec votre ID d’utilisateur de continuer à s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="55deb-125">Closes your Lync display but lets the Lync session identified with your user ID continue to run.</span></span> <span data-ttu-id="55deb-126">Cela vous permet de continuer à recevoir des notifications et à interagir avec d’autres personnes.</span><span class="sxs-lookup"><span data-stu-id="55deb-126">This is so you can continue to get notifications and interact with others.</span></span></p>
<p><span data-ttu-id="55deb-127">Vous pouvez obtenir l’affichage à tout moment en cliquant sur l’icône Lync dans la barre des tâches ou dans la zone de notification située en bas de votre écran.</span><span class="sxs-lookup"><span data-stu-id="55deb-127">You can get the display back at any time by clicking the Lync icon on the taskbar or the notification area at the bottom of your screen.</span></span></p></td>
<td><p><span data-ttu-id="55deb-128">Dans la fenêtre principale de Lync, effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="55deb-128">On the Lync main window, do one of the following:</span></span></p>
<ol>
<li><p><span data-ttu-id="55deb-129">Sélectionnez le bouton <strong>options</strong> , puis cliquez sur Fermer le <strong>fichier</strong> &gt; <strong>Close</strong>.</span><span class="sxs-lookup"><span data-stu-id="55deb-129">Select the <strong>Options</strong> button, then select <strong>File</strong> &gt; <strong>Close</strong>.</span></span></p></li>
<li><p><span data-ttu-id="55deb-130">Cliquez sur le bouton <strong>Fermer</strong> (X) dans le coin supérieur droit de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="55deb-130">Click the <strong>Close</strong> button (X) in the upper-right corner of the window.</span></span></p></li>
</ol></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55deb-131">Se déconnecter</span><span class="sxs-lookup"><span data-stu-id="55deb-131">Sign out</span></span></p></td>
<td><p><span data-ttu-id="55deb-132">Met fin à la session Lync associée à votre ID d’utilisateur, mais Lync continue de s’exécuter en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="55deb-132">Ends the Lync session associated with your user ID, but Lync continues to run in the background.</span></span> <span data-ttu-id="55deb-133">Lorsque vous vous déconnectez, la fenêtre de connexion s’affiche.</span><span class="sxs-lookup"><span data-stu-id="55deb-133">When you sign out, the sign-in window will appear.</span></span></p>
<div>

> [!TIP]  
> <span data-ttu-id="55deb-p105">Sélectionnez <STRONG>Supprimer mes informations de connexion</STRONG> lorsque vous vous déconnectez pour supprimer l’enregistrement de votre ID d’ouverture de session et le mot de passe de l’ordinateur. Cela permet au support technique de résoudre plus facilement les problèmes de connexion. Vos informations de connexion sont mieux sécurisées, car l’ouverture de session avec vos informations d’identification est plus difficile pour des utilisateurs non autorisés.</span><span class="sxs-lookup"><span data-stu-id="55deb-p105">Select <STRONG>Delete my sign-in information</STRONG> when you sign out to remove the record of your logon ID and password from the computer. Doing this might make it easier for support people to troubleshoot sign-in issues. It can also help ensure your sign-in information is more secure by making it difficult for unauthorized users to log on with your credentials.</span></span>


</div></td>
<td><p><span data-ttu-id="55deb-137">Dans la fenêtre principale de Lync, cliquez sur le bouton <strong>options</strong> , <strong>puis sélectionnez</strong> &gt; <strong>se déconnecter</strong>.</span><span class="sxs-lookup"><span data-stu-id="55deb-137">On the Lync main window, select the <strong>Options</strong> button, then select <strong>File</strong> &gt; <strong>Sign Out</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55deb-138">Quitter</span><span class="sxs-lookup"><span data-stu-id="55deb-138">Exit</span></span></p></td>
<td><p><span data-ttu-id="55deb-139">Met fin à votre session Lync et arrête Lync sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="55deb-139">Ends your Lync session and shuts down Lync on your computer.</span></span> <span data-ttu-id="55deb-140">Après avoir quitté le programme, si vous souhaitez redémarrer Lync, cliquez sur <strong>Démarrer</strong> &gt; <strong>tous les programmes</strong> &gt; <strong>Microsoft Lync</strong> &gt; <strong>Lync 2013</strong>.</span><span class="sxs-lookup"><span data-stu-id="55deb-140">After exiting, if you want to restart Lync, select <strong>Start</strong> &gt; <strong>All Programs</strong> &gt; <strong>Microsoft Lync</strong> &gt; <strong>Lync 2013</strong>.</span></span></p></td>
<td><p><span data-ttu-id="55deb-141">Dans la fenêtre principale de Lync, cliquez sur le bouton <strong>options</strong> , puis sélectionnez fermeture de <strong>fichier</strong> &gt; <strong>Exit</strong>.</span><span class="sxs-lookup"><span data-stu-id="55deb-141">On the Lync main window, select the <strong>Options</strong> button, then select <strong>File</strong> &gt; <strong>Exit</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="sign-in-to-lync-with-a-smart-card"></a><span data-ttu-id="55deb-142">Se connecter à Lync avec une carte à puce</span><span class="sxs-lookup"><span data-stu-id="55deb-142">Sign in to Lync with a Smart Card</span></span>

<span data-ttu-id="55deb-143">Certaines organisations utilisent désormais une procédure de connexion à plusieurs étapes, appelée authentification à deux facteurs, pour renforcer la sécurité de leurs utilisateurs Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="55deb-143">Some organizations now use a multi-step sign-in process, called two-factor authentication, to increase security for their Lync 2013 users.</span></span> <span data-ttu-id="55deb-144">Si vous utilisez cette option, vous avez besoin d’une carte à puce pour vous connecter à Lync.</span><span class="sxs-lookup"><span data-stu-id="55deb-144">If you’re expected to use this option, you’ll need a “smart card” to sign in to Lync.</span></span> <span data-ttu-id="55deb-145">Les cartes à puce sont disponibles dans deux variétés, physiques et virtuelles :</span><span class="sxs-lookup"><span data-stu-id="55deb-145">Smart cards come in two varieties, physical and virtual:</span></span>

  - <span data-ttu-id="55deb-146">**Physiques**   À propos de la taille d’une carte de crédit.</span><span class="sxs-lookup"><span data-stu-id="55deb-146">**Physical**   About the size of a credit card.</span></span> <span data-ttu-id="55deb-147">Vous l’insérez dans un lecteur de carte à puce lorsque vous vous connectez.</span><span class="sxs-lookup"><span data-stu-id="55deb-147">You insert it into a smart card reader when you log in.</span></span>

  - <span data-ttu-id="55deb-148">**Virtuel**   Il ne s’agit pas d’un objet physique, mais d’un identificateur électronique qui est écrit sur un processeur spécial sur votre ordinateur, qui, par essence, génère la carte à puce sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="55deb-148">**Virtual**   Not a physical object, but an electronic identifier that gets written to a special chip on your computer, which in essence builds the smart card into your computer.</span></span> <span data-ttu-id="55deb-149">Disponible uniquement sur les ordinateurs Windows 8 qui contiennent le processeur TPM (Trusted Platform Module).</span><span class="sxs-lookup"><span data-stu-id="55deb-149">Available only for use with Windows 8 computers that contain the TPM (Trusted Platform Module) chip.</span></span>

<div>

## <a name="enroll-your-smart-card"></a><span data-ttu-id="55deb-150">Inscription de votre carte à puce</span><span class="sxs-lookup"><span data-stu-id="55deb-150">Enroll your smart card</span></span>

<span data-ttu-id="55deb-151">Pour que vous puissiez vous connecter à l’aide d’une carte à puce, celle-ci doit être « inscrite »; autrement dit, vos informations d’identification d’utilisateur doivent être identifiées sur la carte.</span><span class="sxs-lookup"><span data-stu-id="55deb-151">Before you can sign in with a smart card, the card must be “enrolled”—that is, your user credentials have to be identified with the card.</span></span> <span data-ttu-id="55deb-152">C’est le cas, qu’il s’agisse d’une carte physique ou virtuelle.</span><span class="sxs-lookup"><span data-stu-id="55deb-152">This is the case whether the card is physical or virtual.</span></span> <span data-ttu-id="55deb-153">Ce processus a pu être déjà exécuté par votre administrateur de serveur Lync.</span><span class="sxs-lookup"><span data-stu-id="55deb-153">This process may already been carried out by your Lync Server administrator.</span></span> <span data-ttu-id="55deb-154">Si vous ne savez pas si vous avez terminé, contactez-les.</span><span class="sxs-lookup"><span data-stu-id="55deb-154">Check with them if you’re not sure whether that has been done.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="55deb-155">Dans la mesure où chaque carte à puce virtuelle est associée uniquement à l’appareil sur lequel elle est installée, une carte séparée doit être inscrite pour chaque ordinateur Windows 8 que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="55deb-155">Since each virtual smart card is associated only with the device it’s installed on, a separate card will need to be enrolled for each Windows 8 computer you use.</span></span>



</div>

<span data-ttu-id="55deb-156">**Pour inscrire manuellement votre carte à puce**</span><span class="sxs-lookup"><span data-stu-id="55deb-156">**To manually enroll your smart card**</span></span>

1.  <span data-ttu-id="55deb-157">Ouvrez une session sur l’ordinateur sur lequel vous exécutez Lync.</span><span class="sxs-lookup"><span data-stu-id="55deb-157">Log on to the computer you’ll be running Lync on.</span></span>

2.  <span data-ttu-id="55deb-158">À l’aide d’Internet Explorer, accédez à la page d’inscription web de l’autorité de certification de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="55deb-158">Using Internet Explorer, browse to your organization’s Certificate Authority Web Enrollment page.</span></span>
    
    <span data-ttu-id="55deb-159">Si ce n’est déjà fait, demandez à votre administrateur de serveur Lync l’adresse Web de cette ressource.</span><span class="sxs-lookup"><span data-stu-id="55deb-159">Ask your Lync Server administrator for the web address of this resource if you don’t already have it.</span></span> <span data-ttu-id="55deb-160">L’URL ressemble à ceci : https://MyCA.\ [nom \] . com/certsrv.</span><span class="sxs-lookup"><span data-stu-id="55deb-160">The URL will look something like this: https://MyCA.\[yourcompanyname\].com/certsrv.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="55deb-161">Si vous utilisez Internet Explorer 10, vous devrez peut être afficher ce site web en mode de compatibilité.</span><span class="sxs-lookup"><span data-stu-id="55deb-161">If you’re using Internet Explorer 10, you may need to view this website in Compatibility Mode.</span></span>

    
    </div>

3.  <span data-ttu-id="55deb-162">Lorsque vous êtes invité à ouvrir une session dans la page de certification, connectez-vous à l’aide de votre compte de domaine (plutôt qu’en tant qu’administrateur de votre ordinateur).</span><span class="sxs-lookup"><span data-stu-id="55deb-162">When you’re prompted to log on to the certification page, log on using your domain account (rather than as administrator of your computer).</span></span>

4.  <span data-ttu-id="55deb-163">Dans la page d’accueil du site web, sélectionnez **Demander un certificat**.</span><span class="sxs-lookup"><span data-stu-id="55deb-163">On the website Welcome Page, select **Request a certificate**.</span></span>

5.  <span data-ttu-id="55deb-164">Sélectionnez **Demande avancée**.</span><span class="sxs-lookup"><span data-stu-id="55deb-164">Select **Advanced Request**.</span></span>

6.  <span data-ttu-id="55deb-165">Sélectionnez **Créer et envoyer une demande auprès de cette autorité de certification**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="55deb-165">Select **Create and submit a request to this CA**, then click **Next**.</span></span>

7.  <span data-ttu-id="55deb-166">La page Station d’inscription de carte à puce s’affiche.</span><span class="sxs-lookup"><span data-stu-id="55deb-166">Now you’ll see a page called Smart Card Enrollment Station.</span></span> <span data-ttu-id="55deb-167">Acceptez la demande d’installation du contrôle ActiveX, puis renseignez les champs de l’écran Demande de certificat avancée, comme suit :</span><span class="sxs-lookup"><span data-stu-id="55deb-167">Approve the request to install the ActiveX control, and then complete the Advanced Certificate Request form as follows:</span></span>
    
    1.  <span data-ttu-id="55deb-168">Sélectionnez **Utilisateur de carte à puce** dans la liste déroulante **Modèle de certificat**.</span><span class="sxs-lookup"><span data-stu-id="55deb-168">Select **Smartcard user** from the **Certificate Template** dropdown list.</span></span>
    
    2.  <span data-ttu-id="55deb-169">Sélectionnez **Créer un jeu de clés**.</span><span class="sxs-lookup"><span data-stu-id="55deb-169">Select **Create new key set**.</span></span>
    
    3.  <span data-ttu-id="55deb-170">Recherchez les informations relatives au fabricant sur l’étiquette de votre carte à puce, puis sélectionnez le fabricant dans la liste déroulante **Fournisseur de services de chiffrement**.</span><span class="sxs-lookup"><span data-stu-id="55deb-170">Find the manufacturer information on the label of your smart card and select that manufacturer from the **CSP** dropdown list.</span></span>
    
    4.  <span data-ttu-id="55deb-171">Sélectionnez **Fournisseur de services de chiffrement** comme format de la demande, si cette option n’est pas déjà sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="55deb-171">Select **CSP** as the Request Format, if it’s not already selected.</span></span>
    
    5.  <span data-ttu-id="55deb-172">Dans la liste déroulante Algorithme de hachage, sélectionnez **sha1** si cette option n’est pas déjà sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="55deb-172">Select **sha1** from the Hash Algorithm dropdown list, if it’s not already selected.</span></span>
    
    6.  <span data-ttu-id="55deb-173">Attribuez un nom reconnaissable à votre certificat, puis cliquez sur **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="55deb-173">Give your certificate a name you’ll recognize, and click **Submit**.</span></span>

8.  <span data-ttu-id="55deb-174">Insérez votre carte à puce vierge dans le lecteur de cartes relié à la station d’inscription, puis cliquez sur **Inscrire**.</span><span class="sxs-lookup"><span data-stu-id="55deb-174">Now insert your blank smart card into the card reader attached to the enrollment station and click **Enroll**.</span></span>

9.  <span data-ttu-id="55deb-175">Lorsque vous y êtes invité, entrez votre code confidentiel, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="55deb-175">When prompted, enter your personal identification number (PIN), and then click **OK**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="55deb-176">Si le support technique ne vous a pas communiqué de code confidentiel spécial pour inscrire votre carte à puce, utilisez la valeur de code confidentiel par défaut de la carte à puce (12345678).</span><span class="sxs-lookup"><span data-stu-id="55deb-176">If your technical support person has not given you a special PIN to use to enroll your smart card, use the default smart card PIN value, which is 12345678.</span></span>

    
    </div>

10. <span data-ttu-id="55deb-177">Sélectionnez l’option forçant l’utilisateur (vous) à modifier le code confidentiel à la première utilisation de la carte.</span><span class="sxs-lookup"><span data-stu-id="55deb-177">Select the option to force the user (you) to change the PIN the first time the smart card is used.</span></span>

11. <span data-ttu-id="55deb-178">Insérez votre carte à puce vierge dans le lecteur de cartes relié à la station d’inscription, puis cliquez sur **Inscrire**.</span><span class="sxs-lookup"><span data-stu-id="55deb-178">Now insert your blank smart card into the card reader attached to the enrollment station and click **Enroll**.</span></span>

12. <span data-ttu-id="55deb-179">Lorsque vous y êtes invité, entrez votre code confidentiel, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="55deb-179">When prompted, enter your personal identification number (PIN), and then click **OK**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="55deb-180">Si le support technique ne vous a pas communiqué de code confidentiel spécial pour inscrire votre carte à puce, utilisez la valeur de code confidentiel par défaut de la carte à puce (12345678).</span><span class="sxs-lookup"><span data-stu-id="55deb-180">If your technical support person has not given you a special PIN to use to enroll your smart card, use the default smart card PIN value, which is 12345678.</span></span>

    
    </div>

13. <span data-ttu-id="55deb-181">Sélectionnez l’option forçant l’utilisateur (vous) à modifier le code confidentiel à la première utilisation de la carte.</span><span class="sxs-lookup"><span data-stu-id="55deb-181">Select the option to force the user (you) to change the PIN the first time the smart card is used.</span></span>

14. <span data-ttu-id="55deb-182">Cliquez sur **OK** pour confirmer que le certificat affiché inclut vos informations.</span><span class="sxs-lookup"><span data-stu-id="55deb-182">Click **OK** to confirm that the certificate displayed has your information on it.</span></span>

15. <span data-ttu-id="55deb-183">Une fois que vous recevez l’avis confirmant l’émission du certificat, cliquez sur **Installer ce certificat** pour terminer la procédure d’inscription.</span><span class="sxs-lookup"><span data-stu-id="55deb-183">Once you see the notice that the certificate has been issued, click **Install this certificate** to complete the enrollment process.</span></span>

</div>

<div>

## <a name="sign-in-to-lync-with-your-smart-card-credentials"></a><span data-ttu-id="55deb-184">Connectez-vous à Lync à l’aide de vos informations d’identification de carte à puce</span><span class="sxs-lookup"><span data-stu-id="55deb-184">Sign in to Lync with your smart card credentials</span></span>

<span data-ttu-id="55deb-185">Avant d’utiliser votre carte à puce pour la première fois, il est recommandé de cliquer sur **Supprimer mes informations de connexion** dans la page de connexion à Lync.</span><span class="sxs-lookup"><span data-stu-id="55deb-185">Before you use your smart card for the first time, it’s recommended that you click **Delete my sign-in info** on the Lync sign-in page.</span></span> <span data-ttu-id="55deb-186">Cela permet de supprimer les informations d’identification de connexion stockées sur votre ordinateur et d’éliminer une source possible d’erreur.</span><span class="sxs-lookup"><span data-stu-id="55deb-186">Doing this clears any sign-in credentials stored on your computer, and eliminates a possible source of error.</span></span>

<span data-ttu-id="55deb-187">**Pour vous connecter à Lync à l’aide de vos informations d’identification de carte à puce**</span><span class="sxs-lookup"><span data-stu-id="55deb-187">**To sign in to Lync with your smart card credentials**</span></span>

1.  <span data-ttu-id="55deb-188">Démarrez le client Lync.</span><span class="sxs-lookup"><span data-stu-id="55deb-188">Start the Lync client.</span></span>

2.  <span data-ttu-id="55deb-189">Dans l’écran Se connecter, tapez le nom de compte d’utilisateur de connexion dans la zone **Adresse de connexion**, puis cliquez sur **Se connecter**.</span><span class="sxs-lookup"><span data-stu-id="55deb-189">On the Sign in screen, type your sign in user account name in the **Sign-in address** box, and then click **Sign In**.</span></span>

3.  <span data-ttu-id="55deb-190">Si vous utilisez une carte à puce virtuelle, ignorez cette étape.</span><span class="sxs-lookup"><span data-stu-id="55deb-190">If you are using a virtual smart card, skip this step.</span></span>
    
    <span data-ttu-id="55deb-191">Si vous utilisez une carte à puce physique, insérez la carte à puce dans le lecteur de cartes à puce, puis, lorsque vous y êtes invité, cliquez sur **OK** lorsque la carte est détectée.</span><span class="sxs-lookup"><span data-stu-id="55deb-191">If you are using a physical smart card, insert the smart card into your smart card reader and prompted to do so, and then click **OK** when the card is detected.</span></span>

4.  <span data-ttu-id="55deb-192">Tapez le code confidentiel de votre carte à puce, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="55deb-192">Type in the PIN number you for your smart card and then click **OK**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="55deb-193">Si le support technique ne vous a pas communiqué de code confidentiel, utilisez la valeur par défaut (12345678).</span><span class="sxs-lookup"><span data-stu-id="55deb-193">If you were not assigned a smart card PIN number by your support person, use the default value, which is 12345678.</span></span>

    
    <span data-ttu-id="55deb-194"></div>

</div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="55deb-194"></div>

</div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

