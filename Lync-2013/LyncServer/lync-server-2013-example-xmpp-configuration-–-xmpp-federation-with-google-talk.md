---
title: Exemple de configuration XMPP – Fédération XMPP avec Google Talk
description: Exemple de configuration XMPP-Fédération XMPP avec Google Talk.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
manager: serdars
audience: admin
f1.keywords:
- NOCSH
TOCTitle: Example XMPP configuration – XMPP federation with Google Talk
ms:assetid: 360a2f7b-015b-4e93-ac67-0f609c21f1a2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204807(v=OCS.15)
ms:contentKeyID: 48183848
ms.date: 07/23/2014
mtps_version: v=OCS.15
ms.openlocfilehash: e6ea920fad0344e784aac104ab5528d89b90f47b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428448"
---
# <a name="example-xmpp-configuration-in-lync-server-2013--xmpp-federation-with-google-talk"></a><span data-ttu-id="bfcc5-103">Exemple de configuration XMPP dans Lync Server 2013 – Fédération XMPP avec Google Talk</span><span class="sxs-lookup"><span data-stu-id="bfcc5-103">Example XMPP configuration in Lync Server 2013 – XMPP federation with Google Talk</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bfcc5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bfcc5-104">

<span> </span></span></span>

<span data-ttu-id="bfcc5-105">_**Dernière modification de la rubrique :** 2014-04-22_</span><span class="sxs-lookup"><span data-stu-id="bfcc5-105">_**Topic Last Modified:** 2014-04-22_</span></span>

<span data-ttu-id="bfcc5-106">Un exemple de configuration pour le déploiement du proxy XMPP définit une Fédération avec Google Talk.</span><span class="sxs-lookup"><span data-stu-id="bfcc5-106">An example configuration for deploying the XMPP Proxy defines a federation with Google Talk.</span></span>

<div>

## <a name="example-xmpp-configuration--xmpp-federation-with-google-talk"></a><span data-ttu-id="bfcc5-107">Exemple de configuration XMPP – Fédération XMPP avec Google Talk</span><span class="sxs-lookup"><span data-stu-id="bfcc5-107">Example XMPP configuration – XMPP federation with Google Talk</span></span>

1.  <span data-ttu-id="bfcc5-108">Sur le serveur frontal, ouvrez l’Assistant Déploiement de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="bfcc5-108">On the Front End Server, open the Lync Server Deployment Wizard.</span></span> <span data-ttu-id="bfcc5-109">Cliquez sur **installer** ou **mettre à jour le système serveur Lync**, puis cliquez sur **configurer** ou **Supprimer les composants Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="bfcc5-109">Click **Install** or **Update Lync Server System**, then click **Setup** or **Remove Lync Server Components**.</span></span> <span data-ttu-id="bfcc5-110">Cliquez de **nouveau sur exécuter**.</span><span class="sxs-lookup"><span data-stu-id="bfcc5-110">Click **Run Again**.</span></span>

2.  <span data-ttu-id="bfcc5-111">Dans **configurer les composants serveur Lync**, cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="bfcc5-111">At **Setup Lync Server components**, click **Next**.</span></span> <span data-ttu-id="bfcc5-112">L’écran de synthèse indique les actions à mesure qu’elles sont exécutées.</span><span class="sxs-lookup"><span data-stu-id="bfcc5-112">The summary screen will show actions as they are executed.</span></span> <span data-ttu-id="bfcc5-113">Lorsque le déploiement est terminé, cliquez sur **afficher le journal** pour afficher les fichiers journaux disponibles.</span><span class="sxs-lookup"><span data-stu-id="bfcc5-113">After the deployment is complete, click **View Log** to view available log files.</span></span> <span data-ttu-id="bfcc5-114">Cliquez sur **Terminer** pour terminer le déploiement.</span><span class="sxs-lookup"><span data-stu-id="bfcc5-114">Click **Finish** to complete the deployment.</span></span>

3.  <span data-ttu-id="bfcc5-115">Sur le serveur Edge, ouvrez l’Assistant Déploiement de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="bfcc5-115">On the Edge Server, open the Lync Server Deployment Wizard.</span></span> <span data-ttu-id="bfcc5-116">Cliquez sur **installer** ou **mettre à jour le système serveur Lync**, puis cliquez sur **configurer** ou **Supprimer les composants Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="bfcc5-116">Click **Install** or **Update Lync Server System**, then click **Setup** or **Remove Lync Server Components**.</span></span> <span data-ttu-id="bfcc5-117">Cliquez de **nouveau sur exécuter**.</span><span class="sxs-lookup"><span data-stu-id="bfcc5-117">Click **Run Again**.</span></span>

4.  <span data-ttu-id="bfcc5-118">Ajoutez Google Talk en tant que partenaire XMPP autorisé.</span><span class="sxs-lookup"><span data-stu-id="bfcc5-118">Add Google Talk as an XMPP allowed partner.</span></span> <span data-ttu-id="bfcc5-119">Pour le moment, Google parle ne prend en charge que les connexions TCP non chiffrées pour la Fédération de serveur à serveur et ne prend en charge que le serveur Dialback pour la vérification d’identité.</span><span class="sxs-lookup"><span data-stu-id="bfcc5-119">Google Talk currently only supports unencrypted, TCP connections for server-to-server XMPP federation and only supports Server Dialback for identity verification.</span></span> <span data-ttu-id="bfcc5-120">(Voir <http://xmpp.org/extensions/xep-0220.html> ).</span><span class="sxs-lookup"><span data-stu-id="bfcc5-120">(See <http://xmpp.org/extensions/xep-0220.html>).</span></span>
    
        New-CsXmppAllowedPartner gmail.com -TlsNegotiation NotSupported -SaslNegotiation NotSupported -EnableKeepAlive $false -SupportDialbackNegotiation $true

5.  <span data-ttu-id="bfcc5-121">Pour activer la Fédération Edge, tapez les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="bfcc5-121">To enable Edge Federation, type the following:</span></span>
    
        Set-CsAccessEdgeConfiguration -AllowFederatedUsers $true

6.  <span data-ttu-id="bfcc5-122">Dans **configurer les composants serveur Lync**, cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="bfcc5-122">At **Setup Lync Server components**, click **Next**.</span></span> <span data-ttu-id="bfcc5-123">L’écran de synthèse indique les actions à mesure qu’elles sont exécutées.</span><span class="sxs-lookup"><span data-stu-id="bfcc5-123">The summary screen will show actions as they are executed.</span></span> <span data-ttu-id="bfcc5-124">Une fois le déploiement effectué, cliquez sur **afficher le journal** pour afficher les fichiers journaux disponibles.</span><span class="sxs-lookup"><span data-stu-id="bfcc5-124">After the deployment is done, click **View Log** to view available log files.</span></span> <span data-ttu-id="bfcc5-125">Cliquez sur **Terminer** pour terminer le déploiement.</span><span class="sxs-lookup"><span data-stu-id="bfcc5-125">Click **Finish** to complete the deployment.</span></span>

7.  <span data-ttu-id="bfcc5-126">Sur le serveur Edge, dans l’Assistant Déploiement de Lync Server, en regard de l' **étape 3 : demandez, installez ou attribuez des certificats**, cliquez de **nouveau sur exécuter**.</span><span class="sxs-lookup"><span data-stu-id="bfcc5-126">On the Edge Server, in the Lync Server Deployment Wizard, next to **Step 3: Request, Install, or Assign Certificates**, click **Run again**.</span></span>
    
    <div>
    

    > [!TIP]
    > <span data-ttu-id="bfcc5-127">Si vous déployez le serveur Edge pour la première fois, vous verrez exécuter au lieu de réexécuter.</span><span class="sxs-lookup"><span data-stu-id="bfcc5-127">If you are deploying the Edge Server for the first time, you will see Run instead of Run Again.</span></span>

    
    </div>

8.  <span data-ttu-id="bfcc5-128">Dans la page **Tâches se rapportant aux certificats disponibles**, cliquez sur **Créer une demande de certificat**.</span><span class="sxs-lookup"><span data-stu-id="bfcc5-128">On the **Available Certificate Tasks** page, click **Create a new certificate request**.</span></span>

9.  <span data-ttu-id="bfcc5-129">Dans la page **demande de certificat** , cliquez sur certificat de **bord externe**.</span><span class="sxs-lookup"><span data-stu-id="bfcc5-129">On the **Certificate Request** page, click **External Edge Certificate**.</span></span>

10. <span data-ttu-id="bfcc5-130">Dans la page de **demande retardée ou immédiate** , activez la case à cocher **préparer la demande maintenant, puis l’envoyer plus tard** .</span><span class="sxs-lookup"><span data-stu-id="bfcc5-130">On the **Delayed or Immediate Request** page, select the **Prepare the request now, but send it later** check box.</span></span>

11. <span data-ttu-id="bfcc5-131">Dans la page **fichier de demande de certificat** , tapez le chemin d’accès complet et le nom du fichier dans lequel la demande doit être enregistrée (par exemple, c : \\ CERT \_ l' \_ Edge. cer).</span><span class="sxs-lookup"><span data-stu-id="bfcc5-131">On the **Certificate Request File** page, type the full path and file name of the file to which the request is to be saved (for example, c:\\cert\_exernal\_edge.cer).</span></span>

12. <span data-ttu-id="bfcc5-132">Dans la page **spécifier un modèle de certificat secondaire** , pour utiliser un modèle autre que le modèle par défaut du serveur Web, activez la case à cocher utiliser un autre **modèle de certificat pour l’autorité de certification sélectionnée** .</span><span class="sxs-lookup"><span data-stu-id="bfcc5-132">On the **Specify Alternate Certificate Template** page, to use a template other than the default WebServer template, select the **Use alternative certificate template for the selected certification authority** check box.</span></span>

13. <span data-ttu-id="bfcc5-133">Dans la page **paramètres de nom et de sécurité** , procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="bfcc5-133">On the **Name and Security Settings** page, do the following:</span></span>
    
    1.  <span data-ttu-id="bfcc5-134">Dans **nom convivial**, tapez un nom d’affichage pour le certificat.</span><span class="sxs-lookup"><span data-stu-id="bfcc5-134">In **Friendly name**, type a display name for the certificate</span></span>
    
    2.  <span data-ttu-id="bfcc5-135">En **longueur**, spécifiez la longueur en bits (en général, la valeur par défaut **2048**)</span><span class="sxs-lookup"><span data-stu-id="bfcc5-135">In **Bit length**, specify the bit length (typically, the default of **2048**)</span></span>
    
    3.  <span data-ttu-id="bfcc5-136">Vérifier que la case à cocher **marquer le certificat privé comme étant exportable** est activée</span><span class="sxs-lookup"><span data-stu-id="bfcc5-136">Verify that the **Mark certificate private key as exportable** check box is selected</span></span>

14. <span data-ttu-id="bfcc5-137">Dans la page informations sur l' **organisation** , tapez le nom de l’organisation et celle de l’unité d’organisation (par exemple, une division ou un service).</span><span class="sxs-lookup"><span data-stu-id="bfcc5-137">On the **Organization Information** page, type the name for the organization and the organizational unit (for example, a division or department)</span></span>

15. <span data-ttu-id="bfcc5-138">Dans la page **informations géographiques** , spécifiez les informations d’emplacement</span><span class="sxs-lookup"><span data-stu-id="bfcc5-138">On the **Geographical Information** page, specify the location information</span></span>

16. <span data-ttu-id="bfcc5-139">Sur la page nom de l’objet **/nom** de l’objet, les informations à remplir automatiquement par l’Assistant sont affichées.</span><span class="sxs-lookup"><span data-stu-id="bfcc5-139">On the **Subject Name/Subject Alternate Names** page, the information to be automatically populated by the wizard is displayed.</span></span> <span data-ttu-id="bfcc5-140">Si d’autres noms d’objet sont nécessaires, vous pouvez les spécifier au cours des deux étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="bfcc5-140">If additional subject alternative names are needed, you specify them in the next two steps</span></span>

17. <span data-ttu-id="bfcc5-141">Dans la page Configuration du protocole **SIP sur le nom de l’objet** , activez la case à cocher Domain pour ajouter un SIP.</span><span class="sxs-lookup"><span data-stu-id="bfcc5-141">On the **SIP Domain Setting on Subject Alternate Names (SANs)** page, select the domain check box to add a sip.</span></span> <span data-ttu-id="bfcc5-142">\<sipdomain\> entrée de la liste autres noms d’objet.</span><span class="sxs-lookup"><span data-stu-id="bfcc5-142">\<sipdomain\> entry to the subject alternative names list.</span></span>

18. <span data-ttu-id="bfcc5-143">Dans la page **configurez** d’autres noms d’objet, spécifiez d’autres noms d’objet obligatoires.</span><span class="sxs-lookup"><span data-stu-id="bfcc5-143">On the **Configure Additional Subject Alternate Names** page, specify any additional subject alternative names that are required.</span></span>
    
    <div>
    

    > [!TIP]
    > <span data-ttu-id="bfcc5-144">Si le proxy XMPP est installé, le nom de domaine par défaut (par exemple, contoso.com) est renseigné dans les entrées du SAN.</span><span class="sxs-lookup"><span data-stu-id="bfcc5-144">If the XMPP proxy is installed, by default the domain name (such as contoso.com) is populated in the SAN entries.</span></span> <span data-ttu-id="bfcc5-145">Si vous avez besoin d’entrées supplémentaires, ajoutez-les à cette étape.</span><span class="sxs-lookup"><span data-stu-id="bfcc5-145">If you require more entries, add them in this step.</span></span>

    
    </div>

19. <span data-ttu-id="bfcc5-146">Dans la page Résumé de la **demande** , passez en revue les informations de certificat à utiliser pour générer la requête.</span><span class="sxs-lookup"><span data-stu-id="bfcc5-146">On the **Request Summary** page, review the certificate information to be used to generate the request.</span></span>

20. <span data-ttu-id="bfcc5-147">À la fin de l’exécution des commandes, vous pouvez **consulter le journal** ou cliquer sur **suivant** pour continuer.</span><span class="sxs-lookup"><span data-stu-id="bfcc5-147">After the commands finish running, you can **View Log**, or click **Next** to continue.</span></span>

21. <span data-ttu-id="bfcc5-148">Dans la page **fichier de demande de certificat** , vous pouvez afficher le fichier de demande de signature de certificat généré (CSR) en cliquant sur **Afficher** ou quitter l’Assistant Certificat en cliquant sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="bfcc5-148">On the **Certificate Request File** page, you can view the generated certificate signing request (CSR) file by clicking **View** or exit the Certificate Wizard by clicking **Finish**.</span></span>

22. <span data-ttu-id="bfcc5-149">Copiez le fichier de demande et envoyez-le à votre autorité de certification publique.</span><span class="sxs-lookup"><span data-stu-id="bfcc5-149">Copy the request file and submit to your public certification authority.</span></span>

23. <span data-ttu-id="bfcc5-150">Après avoir reçu, importé et attribué le certificat public, vous devez arrêter et redémarrer les services Edge Server.</span><span class="sxs-lookup"><span data-stu-id="bfcc5-150">After receiving, importing and assigning the public certificate, you must stop and restart the Edge Server services.</span></span> <span data-ttu-id="bfcc5-151">Démarrez Lync Server Management Shell : cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="bfcc5-151">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**..</span></span> <span data-ttu-id="bfcc5-152">Dans Lync Server Management Shell, tapez :</span><span class="sxs-lookup"><span data-stu-id="bfcc5-152">In the Lync Server Management Shell, type:</span></span>
    ```
        Stop-CsWindowsService
    ```
    
    ```
        Start-CsWindowsService
    ```
    
24. <span data-ttu-id="bfcc5-153">Pour configurer le système DNS pour la Fédération XMPP, ajoutez l’enregistrement SRV suivant à DNS externe : \_ XMPP-Server. \_ TCP.\<domain name\></span><span class="sxs-lookup"><span data-stu-id="bfcc5-153">To configure DNS for XMPP federation, you add the following SRV record to external DNS:\_xmpp-server.\_tcp.\<domain name\></span></span> <span data-ttu-id="bfcc5-154">L’enregistrement SRV sera résolu vers le nom de domaine complet d’accès du serveur Edge, avec une valeur de port de 5269</span><span class="sxs-lookup"><span data-stu-id="bfcc5-154">The SRV record will resolve to the access edge FQDN of the Edge server, with a port value of 5269</span></span>

25. <span data-ttu-id="bfcc5-155">Configurez une nouvelle stratégie d’accès externe pour permettre à tous les utilisateurs d’ouvrir Lync Server Management Shell sur un serveur frontal et de taper :</span><span class="sxs-lookup"><span data-stu-id="bfcc5-155">Configure a new External Access Policy to enable all users by opening the Lync Server Management Shell on a Front End Server and typing:</span></span>
    
        New-CsExternalAccessPolicy -Identity FedPic -EnableFederationAccess $true -EnablePublicCloudAccess $true
        Get-CsUser | Grant-CsExternalAccessPolicy -PolicyName FedPic

<span data-ttu-id="bfcc5-156"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bfcc5-156"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

