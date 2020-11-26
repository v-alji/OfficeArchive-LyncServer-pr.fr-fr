---
title: 'Lync Server 2013 : configuration d’une autorité de certification d’entreprise pour l’authentification par carte à puce'
description: 'Lync Server 2013 : configuration de l’autorité de certification d’entreprise pour l’authentification par carte à puce.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Enterprise CA for smart card authentication
ms:assetid: c24e0891-e108-4cb6-9902-c6a4c8e68455
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn308571(v=OCS.15)
ms:contentKeyID: 54973692
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 98044c96dd04d02fd87609918f309cf65227b133
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433149"
---
# <a name="configuring-enterprise-ca-for-smart-card-authentication-in-lync-server-2013"></a><span data-ttu-id="0002c-103">Configuration de l’autorité de certification d’entreprise pour l’authentification par carte à puce dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0002c-103">Configuring Enterprise CA for smart card authentication in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0002c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0002c-104">

<span> </span></span></span>

<span data-ttu-id="0002c-105">_**Dernière modification de la rubrique :** 2013-07-03_</span><span class="sxs-lookup"><span data-stu-id="0002c-105">_**Topic Last Modified:** 2013-07-03_</span></span>

<span data-ttu-id="0002c-106">La section suivante décrit comment configurer une autorité de certification racine d’entreprise pour prendre en charge l’authentification par carte à puce.</span><span class="sxs-lookup"><span data-stu-id="0002c-106">The following section describes how to configure an Enterprise Root Certification Authority (CA) to support smart card authentication.</span></span> <span data-ttu-id="0002c-107">Pour plus d’informations sur l’installation d’une autorité de certification racine d’entreprise, voir installer une autorité de certification racine d’entreprise à l’adresse [https://go.microsoft.com/fwlink/p/?LinkID=313364](https://go.microsoft.com/fwlink/p/?linkid=313364) .</span><span class="sxs-lookup"><span data-stu-id="0002c-107">For information on how to install an Enterprise Root CA, see Install an Enterprise Root Certification Authority at [https://go.microsoft.com/fwlink/p/?LinkID=313364](https://go.microsoft.com/fwlink/p/?linkid=313364).</span></span>

<div>

## <a name="configuring-an-enterprise-root-certificate-authority-to-support-smart-card-authentication"></a><span data-ttu-id="0002c-108">Configuration d’une autorité de certification racine d’entreprise pour prendre en charge l’authentification par carte à puce</span><span class="sxs-lookup"><span data-stu-id="0002c-108">Configuring an Enterprise Root Certificate Authority to Support Smart Card Authentication</span></span>

<span data-ttu-id="0002c-109">La procédure ci-dessous décrit la configuration d’une autorité de certification racine d’entreprise pour prendre en charge l’authentification par carte à puce :</span><span class="sxs-lookup"><span data-stu-id="0002c-109">The following steps describe how to configure an Enterprise Root CA to support Smart Card Authentication:</span></span>

1.  <span data-ttu-id="0002c-110">Connectez-vous à l’ordinateur de l’autorité de certification d’entreprise à l’aide d’un compte d’administrateur de domaine.</span><span class="sxs-lookup"><span data-stu-id="0002c-110">Log in to the Enterprise CA computer using a Domain Admin account.</span></span>

2.  <span data-ttu-id="0002c-111">Lancez le gestionnaire système, puis vérifiez que le rôle Inscription de l’autorité de certification par le biais du web est installé.</span><span class="sxs-lookup"><span data-stu-id="0002c-111">Launch System Manager, and verify that the Certificate Authority Web Enrollment role is installed.</span></span>

3.  <span data-ttu-id="0002c-112">Dans le menu **Outils d’administration**, ouvrez la console de gestion **Autorité de certification**.</span><span class="sxs-lookup"><span data-stu-id="0002c-112">From the **Administrative Tools** menu, open the **Certification Authority** management console.</span></span>

4.  <span data-ttu-id="0002c-113">Dans le volet de navigation, développez **Autorité de certification**.</span><span class="sxs-lookup"><span data-stu-id="0002c-113">In the Navigation pane, expand **Certification Authority**.</span></span>

5.  <span data-ttu-id="0002c-114">Cliquez avec le bouton droit sur **Modèles de certificat**, sélectionnez **Nouveau**, puis **Modèle de certificat à délivrer**.</span><span class="sxs-lookup"><span data-stu-id="0002c-114">Right click on **Certificate Templates**, select **New**, then select **Certificate Template to Issue**.</span></span>

6.  <span data-ttu-id="0002c-115">Sélectionnez **Agent d’inscription**, **Utilisateur de carte à puce** et **Connexion par carte à puce**.</span><span class="sxs-lookup"><span data-stu-id="0002c-115">Select **Enrollment Agent**, **Smartcard User**, and **Smartcard Logon**.</span></span>

7.  <span data-ttu-id="0002c-116">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="0002c-116">Click **OK**.</span></span>

8.  <span data-ttu-id="0002c-117">Cliquez avec le bouton droit sur **Modèles de certificat**.</span><span class="sxs-lookup"><span data-stu-id="0002c-117">Right click on **Certificate Templates**.</span></span>

9.  <span data-ttu-id="0002c-118">Sélectionnez **Gérer**.</span><span class="sxs-lookup"><span data-stu-id="0002c-118">Select **Manage**.</span></span>

10. <span data-ttu-id="0002c-119">Ouvrez les propriétés du modèle utilisateur de carte à puce.</span><span class="sxs-lookup"><span data-stu-id="0002c-119">Open the properties of the Smartcard User template.</span></span>

11. <span data-ttu-id="0002c-120">Cliquez sur l’onglet **Sécurité**.</span><span class="sxs-lookup"><span data-stu-id="0002c-120">Click on the **Security** tab.</span></span>

12. <span data-ttu-id="0002c-121">Modifiez les autorisations, comme suit :</span><span class="sxs-lookup"><span data-stu-id="0002c-121">Change the permissions as follows:</span></span>
    
      - <span data-ttu-id="0002c-122">Ajoutez des comptes Active Directory d’utilisateurs individuels avec les autorisations Lire/Inscrire (Autoriser) ou</span><span class="sxs-lookup"><span data-stu-id="0002c-122">Add individual user AD accounts with Read/Enroll (Allow) permissions, or</span></span>
    
      - <span data-ttu-id="0002c-123">Ajoutez un groupe de sécurité contenant des utilisateurs de carte à puce avec les autorisations Lire/Inscrire (Autoriser) ou</span><span class="sxs-lookup"><span data-stu-id="0002c-123">Add a security group containing smart card users with Read/Enroll (Allow) permissions, or</span></span>
    
      - <span data-ttu-id="0002c-124">Ajoutez le groupe Utilisateurs du domaine avec les autorisations Lire/Inscrire (Autoriser).</span><span class="sxs-lookup"><span data-stu-id="0002c-124">Add the Domain Users group with Read/Enroll (Allow) permissions</span></span>

<span data-ttu-id="0002c-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0002c-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

