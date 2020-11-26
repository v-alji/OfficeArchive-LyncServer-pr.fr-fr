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
# <a name="example-xmpp-configuration-in-lync-server-2013--xmpp-federation-with-google-talk"></a>Exemple de configuration XMPP dans Lync Server 2013 – Fédération XMPP avec Google Talk

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Dernière modification de la rubrique :** 2014-04-22_

Un exemple de configuration pour le déploiement du proxy XMPP définit une Fédération avec Google Talk.

<div>

## <a name="example-xmpp-configuration--xmpp-federation-with-google-talk"></a>Exemple de configuration XMPP – Fédération XMPP avec Google Talk

1.  Sur le serveur frontal, ouvrez l’Assistant Déploiement de Lync Server. Cliquez sur **installer** ou **mettre à jour le système serveur Lync**, puis cliquez sur **configurer** ou **Supprimer les composants Lync Server**. Cliquez de **nouveau sur exécuter**.

2.  Dans **configurer les composants serveur Lync**, cliquez sur **suivant**. L’écran de synthèse indique les actions à mesure qu’elles sont exécutées. Lorsque le déploiement est terminé, cliquez sur **afficher le journal** pour afficher les fichiers journaux disponibles. Cliquez sur **Terminer** pour terminer le déploiement.

3.  Sur le serveur Edge, ouvrez l’Assistant Déploiement de Lync Server. Cliquez sur **installer** ou **mettre à jour le système serveur Lync**, puis cliquez sur **configurer** ou **Supprimer les composants Lync Server**. Cliquez de **nouveau sur exécuter**.

4.  Ajoutez Google Talk en tant que partenaire XMPP autorisé. Pour le moment, Google parle ne prend en charge que les connexions TCP non chiffrées pour la Fédération de serveur à serveur et ne prend en charge que le serveur Dialback pour la vérification d’identité. (Voir <http://xmpp.org/extensions/xep-0220.html> ).
    
        New-CsXmppAllowedPartner gmail.com -TlsNegotiation NotSupported -SaslNegotiation NotSupported -EnableKeepAlive $false -SupportDialbackNegotiation $true

5.  Pour activer la Fédération Edge, tapez les informations suivantes :
    
        Set-CsAccessEdgeConfiguration -AllowFederatedUsers $true

6.  Dans **configurer les composants serveur Lync**, cliquez sur **suivant**. L’écran de synthèse indique les actions à mesure qu’elles sont exécutées. Une fois le déploiement effectué, cliquez sur **afficher le journal** pour afficher les fichiers journaux disponibles. Cliquez sur **Terminer** pour terminer le déploiement.

7.  Sur le serveur Edge, dans l’Assistant Déploiement de Lync Server, en regard de l' **étape 3 : demandez, installez ou attribuez des certificats**, cliquez de **nouveau sur exécuter**.
    
    <div>
    

    > [!TIP]
    > Si vous déployez le serveur Edge pour la première fois, vous verrez exécuter au lieu de réexécuter.

    
    </div>

8.  Dans la page **Tâches se rapportant aux certificats disponibles**, cliquez sur **Créer une demande de certificat**.

9.  Dans la page **demande de certificat** , cliquez sur certificat de **bord externe**.

10. Dans la page de **demande retardée ou immédiate** , activez la case à cocher **préparer la demande maintenant, puis l’envoyer plus tard** .

11. Dans la page **fichier de demande de certificat** , tapez le chemin d’accès complet et le nom du fichier dans lequel la demande doit être enregistrée (par exemple, c : \\ CERT \_ l' \_ Edge. cer).

12. Dans la page **spécifier un modèle de certificat secondaire** , pour utiliser un modèle autre que le modèle par défaut du serveur Web, activez la case à cocher utiliser un autre **modèle de certificat pour l’autorité de certification sélectionnée** .

13. Dans la page **paramètres de nom et de sécurité** , procédez comme suit :
    
    1.  Dans **nom convivial**, tapez un nom d’affichage pour le certificat.
    
    2.  En **longueur**, spécifiez la longueur en bits (en général, la valeur par défaut **2048**)
    
    3.  Vérifier que la case à cocher **marquer le certificat privé comme étant exportable** est activée

14. Dans la page informations sur l' **organisation** , tapez le nom de l’organisation et celle de l’unité d’organisation (par exemple, une division ou un service).

15. Dans la page **informations géographiques** , spécifiez les informations d’emplacement

16. Sur la page nom de l’objet **/nom** de l’objet, les informations à remplir automatiquement par l’Assistant sont affichées. Si d’autres noms d’objet sont nécessaires, vous pouvez les spécifier au cours des deux étapes suivantes.

17. Dans la page Configuration du protocole **SIP sur le nom de l’objet** , activez la case à cocher Domain pour ajouter un SIP. \<sipdomain\> entrée de la liste autres noms d’objet.

18. Dans la page **configurez** d’autres noms d’objet, spécifiez d’autres noms d’objet obligatoires.
    
    <div>
    

    > [!TIP]
    > Si le proxy XMPP est installé, le nom de domaine par défaut (par exemple, contoso.com) est renseigné dans les entrées du SAN. Si vous avez besoin d’entrées supplémentaires, ajoutez-les à cette étape.

    
    </div>

19. Dans la page Résumé de la **demande** , passez en revue les informations de certificat à utiliser pour générer la requête.

20. À la fin de l’exécution des commandes, vous pouvez **consulter le journal** ou cliquer sur **suivant** pour continuer.

21. Dans la page **fichier de demande de certificat** , vous pouvez afficher le fichier de demande de signature de certificat généré (CSR) en cliquant sur **Afficher** ou quitter l’Assistant Certificat en cliquant sur **Terminer**.

22. Copiez le fichier de demande et envoyez-le à votre autorité de certification publique.

23. Après avoir reçu, importé et attribué le certificat public, vous devez arrêter et redémarrer les services Edge Server. Démarrez Lync Server Management Shell : cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Lync Server Management Shell**. Dans Lync Server Management Shell, tapez :
    ```
        Stop-CsWindowsService
    ```
    
    ```
        Start-CsWindowsService
    ```
    
24. Pour configurer le système DNS pour la Fédération XMPP, ajoutez l’enregistrement SRV suivant à DNS externe : \_ XMPP-Server. \_ TCP.\<domain name\> L’enregistrement SRV sera résolu vers le nom de domaine complet d’accès du serveur Edge, avec une valeur de port de 5269

25. Configurez une nouvelle stratégie d’accès externe pour permettre à tous les utilisateurs d’ouvrir Lync Server Management Shell sur un serveur frontal et de taper :
    
        New-CsExternalAccessPolicy -Identity FedPic -EnableFederationAccess $true -EnablePublicCloudAccess $true
        Get-CsUser | Grant-CsExternalAccessPolicy -PolicyName FedPic

</div>

</div>

<span> </span>

</div>

</div>

</div>

