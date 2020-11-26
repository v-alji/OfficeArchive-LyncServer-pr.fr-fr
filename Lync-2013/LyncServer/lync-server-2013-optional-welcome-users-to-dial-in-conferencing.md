---
title: 'Lync Server 2013 : (Facultatif) Accueil des utilisateurs dans les conférences rendez-vous'
description: 'Lync Server 2013 : (facultatif) Bienvenue les utilisateurs à la Conférence rendez-vous.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: (Optional) Welcome users to dial-in conferencing
ms:assetid: caa4fd61-f506-4c09-bb5b-1aa260d7a720
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398846(v=OCS.15)
ms:contentKeyID: 48185443
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0d33c7184a8cf22699b4ebe8d8ea8b4ef1c133a3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424841"
---
# <a name="optional-welcome-users-to-dial-in-conferencing-in-lync-server-2013"></a><span data-ttu-id="95c99-103">(Facultatif) Accueil des utilisateurs dans les conférences rendez-vous dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="95c99-103">(Optional) Welcome users to dial-in conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="95c99-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="95c99-104">

<span> </span></span></span>

<span data-ttu-id="95c99-105">_**Dernière modification de la rubrique :** 2012-09-30_</span><span class="sxs-lookup"><span data-stu-id="95c99-105">_**Topic Last Modified:** 2012-09-30_</span></span>

<span data-ttu-id="95c99-106">Après avoir configuré les conférences rendez-vous et les tests pour vérifier qu’ils fonctionnent correctement, vous devez définir des codes confidentiels (pin) de départ pour les utilisateurs et informer les utilisateurs de la disponibilité de la fonctionnalité, y compris des instructions d’introduction telles que le code confidentiel initial et le lien vers la page Web des paramètres de conférence rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="95c99-106">After you configure dial-in conferencing and test to verify that it is functioning properly, you should set initial personal identification numbers (PINs) for users and notify users about the availability of the feature, including introductory instructions such as the initial PIN and the link to the Dial-in Conferencing Settings webpage.</span></span> <span data-ttu-id="95c99-107">Cette étape est facultative.</span><span class="sxs-lookup"><span data-stu-id="95c99-107">This step is optional.</span></span> <span data-ttu-id="95c99-108">En règle générale, vous utilisez l’applet de connexion **Set-CsClientPin** pour réinitialiser des épingles, mais vous pouvez utiliser la procédure décrite dans cette rubrique pour la première fois si vous voulez envoyer un message de bienvenue aux informations.</span><span class="sxs-lookup"><span data-stu-id="95c99-108">Typically, you use the **Set-CsClientPin** cmdlet to reset PINs, but you can use the procedure in this topic the first time if you want to send a welcome email with the information.</span></span> <span data-ttu-id="95c99-109">Si vous ne souhaitez pas envoyer ce message, utilisez plutôt **Set-CsClientPin**.</span><span class="sxs-lookup"><span data-stu-id="95c99-109">If you do not want to send the email, you can use **Set-CsClientPin** instead.</span></span>

<span data-ttu-id="95c99-110">Vous pouvez utiliser le script **Set-CsPinSendCAWelcomeMail** pour définir le code confidentiel et envoyer un message électronique de bienvenue à un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="95c99-110">You can use the **Set-CsPinSendCAWelcomeMail** script to set the PIN and send a welcome email to a single user.</span></span> <span data-ttu-id="95c99-111">Par défaut, le script ne réinitialise pas de code confidentiel s’il est déjà défini, mais vous pouvez utiliser le paramètre **force** pour réinitialiser le code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="95c99-111">By default, the script does not reset a PIN if it is already set, but you can use the **Force** parameter to force reset a PIN.</span></span> <span data-ttu-id="95c99-112">Le message électronique est envoyé à l’aide du protocole SMTP (Simple Mail Transfer Protocol).</span><span class="sxs-lookup"><span data-stu-id="95c99-112">The email message is sent using Simple Mail Transfer Protocol (SMTP).</span></span>

<span data-ttu-id="95c99-113">Vous pouvez créer un script qui exécute le script **Set-CsPinSendCAWelcomeMail** de manière itérative pour définir des codes confidentiels et envoyer un message électronique à un groupe d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="95c99-113">You can create a script that runs the **Set-CsPinSendCAWelcomeMail** script iteratively to set PINs and send email to a group of users.</span></span> <span data-ttu-id="95c99-114">Vous pouvez modifier le modèle de courrier (autrement dit, le fichier **CAWelcomeEmailTemplate.html** ) pour ajouter des liens vers des pages intranet ou modifier le texte du message.</span><span class="sxs-lookup"><span data-stu-id="95c99-114">You can modify the email template (that is, the **CAWelcomeEmailTemplate.html** file) to add more links to intranet pages or modify the email text.</span></span>

<div>

## <a name="to-set-an-initial-pin-and-send-welcome-email"></a><span data-ttu-id="95c99-115">Pour définir un code confidentiel initial et envoyer un message de bienvenue</span><span class="sxs-lookup"><span data-stu-id="95c99-115">To set an initial PIN and send welcome email</span></span>

1.  <span data-ttu-id="95c99-116">Ouvrez une session en tant que membre du groupe RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="95c99-116">Log on as a member of the RTCUniversalServerAdmins group.</span></span>

2.  <span data-ttu-id="95c99-117">Démarrez Lync Server Management Shell : cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="95c99-117">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="95c99-118">Exécutez la commande suivante dans l’invite de commandes :</span><span class="sxs-lookup"><span data-stu-id="95c99-118">Run the following at the command prompt:</span></span>
    
        Set-CsPinSendCAWelcomeMail -UserUri <user identifier>
        -From <email address of sender> [-Subject <subject for email message>]
        [-UserEmailAddress <destination email address>]
        [-Cc <email address of recipients who receive copy of email>]
        [-Bcc <email address of recipients who receive blind copies>]
        [-TemplatePath <path for email template>]
        [-SmtpServer] <SMTP server name>]
        [-BodyAsPlainText] [-UseSsl]
        [-Pin <new numeric PIN>] [-Force] `
        [-Credential <SMTP server credentials used to send email with the specified From address>]
    
    <span data-ttu-id="95c99-119">**SmtpServer**   Par défaut, le script utilise la valeur de la variable d’environnement réservée **$PSEmailServer** pour ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="95c99-119">**SmtpServer**   By default, the script uses the value of the reserved environment variable **$PSEmailServer** for this parameter.</span></span> <span data-ttu-id="95c99-120">Si la variable **$PSEmailServer** n’est pas définie, vous devez spécifier ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="95c99-120">If the **$PSEmailServer** variable is not set, you must specify this parameter.</span></span>
    
    <span data-ttu-id="95c99-121">**Informations d’identification**   Par défaut, le script utilise les informations d’identification de l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="95c99-121">**Credential**   By default, the script uses the credentials of the current user.</span></span> <span data-ttu-id="95c99-122">Si l’utilisateur actuel n’a pas le droit d’envoyer un message électronique au nom de l’expéditeur spécifié dans le champ De, vous devez entrer ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="95c99-122">If the current user does not have permission to send email on behalf of the specified From address, you must specify this parameter.</span></span> <span data-ttu-id="95c99-123">En règle générale, spécifiez ce paramètre si vous n’indiquez pas votre adresse de messagerie dans le champ De.</span><span class="sxs-lookup"><span data-stu-id="95c99-123">As a general rule, specify this parameter if you do not specify your email address as the From address.</span></span>
    
    <span data-ttu-id="95c99-124">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="95c99-124">For example:</span></span>
    
        Set-CsPinSendCAWelcomeMail -UserUri "bob@contoso.com"
        -From "marco@contoso.com"
    
    <span data-ttu-id="95c99-125">Cet exemple crée un nouveau code confidentiel, puis envoie un courrier de bienvenue de Marco à Bob.</span><span class="sxs-lookup"><span data-stu-id="95c99-125">This example creates a new PIN and then sends a welcome email from Marco to Bob.</span></span> <span data-ttu-id="95c99-126">Il utilise le texte du message électronique enregistré dans le modèle par défaut et crée le message électronique au format HTML.</span><span class="sxs-lookup"><span data-stu-id="95c99-126">It uses the email text from the default template and creates the email message in HTML format.</span></span> <span data-ttu-id="95c99-127">Le sujet par défaut est « bienvenue dans la conférence téléphonique ».</span><span class="sxs-lookup"><span data-stu-id="95c99-127">The default Subject is "Welcome to Dial In Conferencing".</span></span>
    
    <span data-ttu-id="95c99-128">Autre exemple :</span><span class="sxs-lookup"><span data-stu-id="95c99-128">Another example:</span></span>
    
        Set-CsPinSendCAWelcomeMail -UserUri "bob@contoso.com"
        -From "marco@contoso.com" -Subject "Your new dial-in conferencing PIN"
        -Pin "383042650" -Force
        -Credential Admin@contoso.com -UseSsl
    
    <span data-ttu-id="95c99-129">Cet exemple force un nouveau code secret dont la valeur est « 383042650 » pour Bob, même si Bob possédait un code confidentiel existant, puis envoie un courrier de bienvenue de Marco à Bob.</span><span class="sxs-lookup"><span data-stu-id="95c99-129">This example forces a new PIN with a value of "383042650" for Bob, even though Bob had an existing PIN, and then sends a welcome email from Marco to Bob.</span></span> <span data-ttu-id="95c99-130">Comme le paramètre Credential est spécifié, la personne exécutant la commande est invitée à entrer un mot de passe.</span><span class="sxs-lookup"><span data-stu-id="95c99-130">Because the Credential parameter is specified, the person running the command is prompted to enter a password.</span></span> <span data-ttu-id="95c99-131">Le message est envoyé à l’aide du protocole SSL (Secure Sockets Layer).</span><span class="sxs-lookup"><span data-stu-id="95c99-131">The email is sent by using the Secure Sockets Layer (SSL).</span></span>

<span data-ttu-id="95c99-132"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="95c99-132"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

