---
title: 'Lync Server 2013 : configuration des services de fédération Active Directory (AD FS 2,0)'
description: 'Lync Server 2013 : configuration des services de fédération Active Directory (AD FS 2,0).'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Active Directory Federation Services (AD FS 2.0)
ms:assetid: 0ba8657f-55b8-41b3-960c-fdc5eeee6978
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn308561(v=OCS.15)
ms:contentKeyID: 54973682
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bc21500273d8576f54f6110783e61764ec9723a2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433401"
---
# <a name="configuring-active-directory-federation-services-ad-fs-20-for-lync-server-2013"></a><span data-ttu-id="feb41-103">Configuration des services ADFS 2,0 (Active Directory Federation Services) pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="feb41-103">Configuring Active Directory Federation Services (AD FS 2.0) for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="feb41-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="feb41-104">

<span> </span></span></span>

<span data-ttu-id="feb41-105">_**Dernière modification de la rubrique :** 2013-07-03_</span><span class="sxs-lookup"><span data-stu-id="feb41-105">_**Topic Last Modified:** 2013-07-03_</span></span>

<span data-ttu-id="feb41-106">Cette section décrit la configuration d’Active Directory Federation Services (AD FS 2.0) pour prendre en charge l’authentification multifacteur.</span><span class="sxs-lookup"><span data-stu-id="feb41-106">The following section describes how to configure Active Directory Federation Services (AD FS 2.0) to support multi-factor authentication.</span></span> <span data-ttu-id="feb41-107">Pour plus d’informations sur l’installation d’AD FS 2,0, consultez la rubrique AD FS 2,0 étape par étape et comment les guides [https://go.microsoft.com/fwlink/p/?LinkId=313374](https://go.microsoft.com/fwlink/p/?linkid=313374) .</span><span class="sxs-lookup"><span data-stu-id="feb41-107">For information on how to install AD FS 2.0, see AD FS 2.0 Step-by-Step and How To Guides at [https://go.microsoft.com/fwlink/p/?LinkId=313374](https://go.microsoft.com/fwlink/p/?linkid=313374).</span></span>

<div class="">


> [!NOTE]  
> <span data-ttu-id="feb41-108">Lorsque vous installez AD FS 2.0, vous ne devez pas utiliser le Gestionnaire de serveur Windows pour ajouter le rôle Active Directory Federation Services.</span><span class="sxs-lookup"><span data-stu-id="feb41-108">When installing AD FS 2.0, do not use the Windows Server Manager to add the Active Directory Federation Services role.</span></span> <span data-ttu-id="feb41-109">Au lieu de cela, téléchargez et installez le package de services ADFS (Active Directory Federation Services) 2,0 à l’adresse <A href="https://go.microsoft.com/fwlink/p/?linkid=313375">https://go.microsoft.com/fwlink/p/?LinkId=313375</A> .</span><span class="sxs-lookup"><span data-stu-id="feb41-109">Instead, download and install the Active Directory Federation Services 2.0 RTW package at <A href="https://go.microsoft.com/fwlink/p/?linkid=313375">https://go.microsoft.com/fwlink/p/?LinkId=313375</A>.</span></span>



</div>

<div>


<span data-ttu-id="feb41-110">**Pour configurer AD FS pour l’authentification à deux facteurs**</span><span class="sxs-lookup"><span data-stu-id="feb41-110">**To configure AD FS for two-factor Authentication**</span></span>

1.  <span data-ttu-id="feb41-111">Connectez-vous à l’ordinateur AD FS 2.0 à l’aide d’un compte d’administrateur de domaine.</span><span class="sxs-lookup"><span data-stu-id="feb41-111">Log in to the AD FS 2.0 computer using a Domain Admin account.</span></span>

2.  <span data-ttu-id="feb41-112">Lancez Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="feb41-112">Start Windows PowerShell.</span></span>

3.  <span data-ttu-id="feb41-113">À partir de la ligne de commande Windows PowerShell, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="feb41-113">From the Windows PowerShell command-line, run the following command:</span></span>
    ```powershell
    add-pssnapin Microsoft.Adfs.PowerShell
    ```
4.  <span data-ttu-id="feb41-114">Établissez un partenariat avec chaque 2013 Lync Server avec des mises à jour cumulatives pour Lync Server 2013 : le directeur 2013 de juillet, le pool d’entreprise et le serveur Standard Edition Server qui seront activés pour l’authentification passive en exécutant la commande suivante, en remplaçant le nom du serveur propre à votre déploiement :</span><span class="sxs-lookup"><span data-stu-id="feb41-114">Establish a partnership with each Lync Server 2013 with Cumulative Updates for Lync Server 2013: July 2013 Director, Enterprise Pool, and Standard Edition server that will be enabled for passive authentication by running the following command, replacing the server name specific to your deployment:</span></span>
    ```powershell
    Add-ADFSRelyingPartyTrust -Name LyncPool01-PassiveAuth -MetadataURL https://lyncpool01.contoso.com/passiveauth/federationmetadata/2007-06/federationmetadata.xml
     ```
5.  <span data-ttu-id="feb41-115">Dans le menu Outils d’administration, lancez la console de gestion AD FS 2.0.</span><span class="sxs-lookup"><span data-stu-id="feb41-115">From the Administrative Tools menu, launch the AD FS 2.0 Management console.</span></span>

6.  <span data-ttu-id="feb41-116">Développez **relations d’approbation** de confiance entre les \> **parties**.</span><span class="sxs-lookup"><span data-stu-id="feb41-116">Expand **Trust Relationships** \> **Relying Party Trusts**.</span></span>

7.  <span data-ttu-id="feb41-117">Vérifiez qu’une nouvelle approbation a été créée pour votre Lync Server 2013 avec des mises à jour cumulatives pour Lync Server 2013:2013 du pool d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="feb41-117">Verify that a new trust has been created for your Lync Server 2013 with Cumulative Updates for Lync Server 2013: July 2013 Enterprise Pool or Standard Edition server.</span></span>

8.  <span data-ttu-id="feb41-118">Créez et affectez une règle d’autorisation d’émission pour votre relation d’approbation de la partie de confiance à l’aide de Windows PowerShell en exécutant les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="feb41-118">Create and assign an Issuance Authorization Rule for your relying party trust using Windows PowerShell by running the following commands:</span></span>
    
       ```powershell
        $IssuanceAuthorizationRules = '@RuleTemplate = "AllowAllAuthzRule" => issue(Type = "http://schemas.microsoft.com/authorization/claims/permit", Value = "true");'
       ```
    
       ```powershell
        Set-ADFSRelyingPartyTrust -TargetName LyncPool01-PassiveAuth 
        -IssuanceAuthorizationRules $IssuanceAuthorizationRules
       ```

9.  <span data-ttu-id="feb41-119">Créez et affectez une règle de transformation d’émission pour votre relation d’approbation de la partie de confiance à l’aide de Windows PowerShell en exécutant les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="feb41-119">Create and assign an Issuance Transform Rule for your relying party trust using Windows PowerShell by running the following commands:</span></span>
    
       ```powershell
        $IssuanceTransformRules = '@RuleTemplate = "PassThroughClaims" @RuleName = "Sid" c:[Type == "http://schemas.microsoft.com/ws/2008/06/identity/claims/primarysid"]=> issue(claim = c);'
       ```
    
       ```powershell
        Set-ADFSRelyingPartyTrust -TargetName LyncPool01-PassiveAuth -IssuanceTransformRules $IssuanceTransformRules
       ```

10. <span data-ttu-id="feb41-120">Dans la console de gestion AD FS 2.0, cliquez avec le bouton droit sur votre relation d’approbation de la partie de confiance, puis sélectionnez **Modifier les règles de revendication**.</span><span class="sxs-lookup"><span data-stu-id="feb41-120">From the AD FS 2.0 Management console, right click on your relying party trust and select **Edit Claim Rules**.</span></span>

11. <span data-ttu-id="feb41-121">Sélectionnez l’onglet **Règles d’autorisation d’émission**, puis vérifiez que la règle d’autorisation a été correctement créée.</span><span class="sxs-lookup"><span data-stu-id="feb41-121">Select the **Issuance Authorization Rules** tab and verify that the new authorization rule was created successfully.</span></span>

12. <span data-ttu-id="feb41-122">Sélectionnez l’onglet **Règles de transformation d’émission**, puis vérifiez que la règle de transformation d’émission a été créée correctement.</span><span class="sxs-lookup"><span data-stu-id="feb41-122">Select the **Issuance Transform Rules** tab and verify that the new transform rule was created successfully.</span></span>

<span data-ttu-id="feb41-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="feb41-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

