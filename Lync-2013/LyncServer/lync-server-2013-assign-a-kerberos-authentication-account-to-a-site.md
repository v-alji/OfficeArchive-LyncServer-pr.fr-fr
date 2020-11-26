---
title: 'Lync Server 2013 : Attribution d’un compte d’authentification Kerberos sur un site'
description: 'Lync Server 2013 : attribuez un compte d’authentification Kerberos à un site.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Assign a Kerberos authentication account to a site
ms:assetid: 3d9c587c-c8b8-4f81-8ed9-1458a31fc292
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425901(v=OCS.15)
ms:contentKeyID: 48183929
ms.date: 04/18/2017
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: edcd80ef3ae15ae91dfab73ee8789054d897fe5c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439841"
---
# <a name="assign-a-kerberos-authentication-account-to-a-site-in-lync-server-2013"></a><span data-ttu-id="d9cd5-103">Attribution d’un compte d’authentification Kerberos sur un site dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d9cd5-103">Assign a Kerberos authentication account to a site in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d9cd5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d9cd5-104">

<span> </span></span></span>

<span data-ttu-id="d9cd5-105">_**Dernière modification de la rubrique :** 2017-04-18_</span><span class="sxs-lookup"><span data-stu-id="d9cd5-105">_**Topic Last Modified:** 2017-04-18_</span></span>

<span data-ttu-id="d9cd5-106">Pour effectuer cette procédure, vous devez être connecté en tant qu’utilisateur membre du groupe RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="d9cd5-106">To successfully complete this procedure you should be logged on as a user who is a member of the RTCUniversalServerAdmins group.</span></span>

<span data-ttu-id="d9cd5-107">Après avoir créé le compte Kerberos, vous devez l’attribuer à un site.</span><span class="sxs-lookup"><span data-stu-id="d9cd5-107">After creating the Kerberos account, you must assign it to a site.</span></span> <span data-ttu-id="d9cd5-108">Il s’agit d’un site Lync Server 2013, et non d’un site Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d9cd5-108">This is a Lync Server 2013 site, not an Active Directory site.</span></span> <span data-ttu-id="d9cd5-109">Vous pouvez créer plusieurs comptes d’authentification Kerberos par déploiement, mais vous ne pouvez attribuer qu’un seul compte à un site.</span><span class="sxs-lookup"><span data-stu-id="d9cd5-109">You can create multiple Kerberos authentication accounts per deployment, but you can assign only one account to a site.</span></span> <span data-ttu-id="d9cd5-110">Utilisez la procédure suivante pour affecter un compte d’authentification Kerberos précédemment créé à un site.</span><span class="sxs-lookup"><span data-stu-id="d9cd5-110">Use the following procedure to assign a previously created Kerberos authentication account to a site.</span></span> <span data-ttu-id="d9cd5-111">Pour plus d’informations sur la création du compte Kerberos, voir [créer un compte d’authentification Kerberos dans Lync Server 2013](lync-server-2013-create-a-kerberos-authentication-account.md).</span><span class="sxs-lookup"><span data-stu-id="d9cd5-111">For details about creating the Kerberos account, see [Create a Kerberos authentication account in Lync Server 2013](lync-server-2013-create-a-kerberos-authentication-account.md).</span></span>

<div>

## <a name="to-assign-a-kerberos-authentication-account-to-a-site"></a><span data-ttu-id="d9cd5-112">Pour attribuer un compte d’authentification Kerberos à un site</span><span class="sxs-lookup"><span data-stu-id="d9cd5-112">To assign a Kerberos authentication account to a site</span></span>

1.  <span data-ttu-id="d9cd5-113">En tant que membre du groupe RTCUniversalServerAdmins, connectez-vous à un ordinateur du domaine exécutant Lync Server 2013 ou sur un ordinateur sur lequel les outils d’administration sont installés.</span><span class="sxs-lookup"><span data-stu-id="d9cd5-113">As a member of the RTCUniversalServerAdmins group, log on to a computer in the domain running Lync Server 2013 or on to a computer where the administrative tools are installed.</span></span>

2.  <span data-ttu-id="d9cd5-114">Démarrez Lync Server Management Shell : cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="d9cd5-114">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="d9cd5-115">À partir de la ligne de commande, exécutez les deux commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="d9cd5-115">From the command line, run the following two commands:</span></span>
    
       ```powershell
        New-CsKerberosAccountAssignment -UserAccount "Domain\UserAccount"
                  -Identity "site:SiteName"
       ```          
    
       ```powershell
        Enable-CsTopology
       ```
    
    <span data-ttu-id="d9cd5-116">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="d9cd5-116">For example:</span></span>
    
       ```powershell
        New-CsKerberosAccountAssignment -UserAccount "contoso\kerbauth"
                  -Identity "site:redmond"
       ```
    
       ```powershell
        Enable-CsTopology
       ```
    
    <div class="">
    

    > [!NOTE]  
    > <span data-ttu-id="d9cd5-117">Vous devez spécifier le paramètre UserAccount en utilisant le format domaine\utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d9cd5-117">You must specify the UserAccount parameter by using the Domain\User format.</span></span> <span data-ttu-id="d9cd5-118">Le format User@Domain. extension n’est pas pris en charge pour référencer les objets ordinateur créés à des fins d’authentification Kerberos.</span><span class="sxs-lookup"><span data-stu-id="d9cd5-118">The User@Domain.extension format is not supported for referring to the computer objects created for Kerberos authentication purposes.</span></span>

    
    </div>

4.  <span data-ttu-id="d9cd5-119">**Facultatif**: il est possible que vous ayez configuré un nom de domaine complet (FQDN) de remplacement pour vos services Web, en fonction [du changement d’URL des services Web dans Lync Server 2013](lync-server-2013-change-the-web-services-url.md).</span><span class="sxs-lookup"><span data-stu-id="d9cd5-119">**OPTIONAL**: You may have configured an override FQDN (fully qualified domain name) for your WebServices, as per [Change the Web Services URL in Lync Server 2013](lync-server-2013-change-the-web-services-url.md).</span></span> <span data-ttu-id="d9cd5-120">Si tel est le cas, vous devez ajouter un SPN pour ce nom de domaine complet.</span><span class="sxs-lookup"><span data-stu-id="d9cd5-120">If that's the case, you'll need to add a SPN for this FQDN as well.</span></span> <span data-ttu-id="d9cd5-121">Par exemple, si le nom de domaine complet était WebServices. contoso. local, vous exécuterez :</span><span class="sxs-lookup"><span data-stu-id="d9cd5-121">For example, if the FQDN was webservices.contoso.local, you would run:</span></span>
    
    ```console
    setspn -S http/webservices.contoso.local kerbauth
    ```
5.     
    <div class="">
    

    > [!IMPORTANT]  
    > <span data-ttu-id="d9cd5-122">Après avoir apporté des modifications à l’authentification Kerberos (par exemple, ajout d’un compte ou suppression d’un compte), vous devez exécuter <STRONG>Enable-CsTopology</STRONG> à partir de l’invite de commandes de Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="d9cd5-122">After making any changes to Kerberos authentication, such as adding an account or removing an account, you must run <STRONG>Enable-CsTopology</STRONG> from the Lync Server Management Shell command prompt.</span></span>

    
    <span data-ttu-id="d9cd5-123"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d9cd5-123"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

