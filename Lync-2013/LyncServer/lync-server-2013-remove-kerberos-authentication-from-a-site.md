---
title: 'Lync Server 2013 : Suppression de l’authentification Kerberos d’un site'
description: 'Lync Server 2013 : supprimer l’authentification Kerberos d’un site.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Remove Kerberos authentication from a site
ms:assetid: 93171b02-bb36-42dc-943d-86d9dde45b59
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398749(v=OCS.15)
ms:contentKeyID: 48184806
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2a3d9100d07d37e98800cfce106bc75fcfaeaa59
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436383"
---
# <a name="in-lync-server-2013-remove-kerberos-authentication-from-a-site"></a><span data-ttu-id="f4edd-103">Suppression de l’authentification Kerberos d’un site dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f4edd-103">In Lync Server 2013 remove Kerberos authentication from a site</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f4edd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f4edd-104">

<span> </span></span></span>

<span data-ttu-id="f4edd-105">_**Dernière modification de la rubrique :** 2012-01-16_</span><span class="sxs-lookup"><span data-stu-id="f4edd-105">_**Topic Last Modified:** 2012-01-16_</span></span>

<span data-ttu-id="f4edd-106">Pour effectuer cette procédure, vous devez être connecté en tant qu’utilisateur membre du groupe RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="f4edd-106">To successfully complete this procedure you should be logged on as a user who is a member of the RTCUniversalServerAdmins group.</span></span>

<span data-ttu-id="f4edd-107">Si vous avez besoin de supprimer l’authentification Kerberos d’un site ou de retirer un site, vous devez supprimer l’attribution de compte d’authentification Kerberos du site en utilisant l’applet de passe **Remove-CsKerberosAccountAssignment** .</span><span class="sxs-lookup"><span data-stu-id="f4edd-107">If you need to remove Kerberos authentication from a site or retire a site, you must remove the Kerberos authentication account assignment from the site by using the **Remove-CsKerberosAccountAssignment** cmdlet.</span></span> <span data-ttu-id="f4edd-108">Utilisez la procédure suivante pour supprimer l’attribution du compte d’authentification Kerberos, qui supprime le devoir de tous les ordinateurs du site.</span><span class="sxs-lookup"><span data-stu-id="f4edd-108">Use the following procedure to remove the Kerberos authentication account assignment, which removes the assignment from all computers in the site.</span></span>

<div class=" ">


> [!WARNING]  
> <span data-ttu-id="f4edd-109">Si vous désactivez définitivement le compte Kerberos, utilisez utilisateurs et ordinateurs Active Directory pour le supprimer des services de domaine Active Directory (AD Active Directory) après avoir supprimé le devoir.</span><span class="sxs-lookup"><span data-stu-id="f4edd-109">If you are permanently retiring the Kerberos-enabled account, you should use Active Directory Users and Computers to delete it from Active Directory Domain Services after you have removed the assignment.</span></span> <span data-ttu-id="f4edd-110">Si vous envisagez d’utiliser l’objet à l’avenir, vous souhaiterez peut-être conserver l’objet Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f4edd-110">If you plan to use the object in the future, you might want to keep the Active Directory object.</span></span>



</div>

<div>

## <a name="to-remove-kerberos-authentication-from-a-site"></a><span data-ttu-id="f4edd-111">Pour supprimer l’authentification Kerberos d’un site</span><span class="sxs-lookup"><span data-stu-id="f4edd-111">To remove Kerberos authentication from a site</span></span>

1.  <span data-ttu-id="f4edd-112">En tant que membre du groupe RTCUniversalServerAdmins, connectez-vous à un ordinateur du domaine exécutant Lync Server 2013 ou sur un ordinateur sur lequel les outils d’administration sont installés.</span><span class="sxs-lookup"><span data-stu-id="f4edd-112">As a member of the RTCUniversalServerAdmins group, log on to a computer in the domain running Lync Server 2013 or on to a computer where the administrative tools are installed.</span></span>

2.  <span data-ttu-id="f4edd-113">Démarrez Lync Server Management Shell : cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="f4edd-113">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="f4edd-114">À partir de la ligne de commande, exécutez les deux commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="f4edd-114">From the command line, run the following two commands:</span></span>
    
       ```PowerShell
        Remove-CsKerberosAccountAssignment -Identity "site:SiteName"
       ```
    
       ```PowerShell
        Enable-CsTopology
       ```
    
    <span data-ttu-id="f4edd-115">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="f4edd-115">For example:</span></span>
    
       ```PowerShell
        Remove-CsKerberosAccountAssignment -Identity "site:Redmond"
       ```
    
       ```PowerShell
        Enable-CsTopology
       ```
    
    <div class=" ">
    

    > [!IMPORTANT]  
    > <span data-ttu-id="f4edd-116">Après avoir apporté des modifications à l’authentification Kerberos (par exemple, ajout d’un compte ou suppression d’un compte), vous devez exécuter <STRONG>Enable-CsTopology</STRONG> à partir de l’invite de commandes de Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="f4edd-116">After making any changes to Kerberos authentication, such as adding an account or removing an account, you must run <STRONG>Enable-CsTopology</STRONG> from the Lync Server Management Shell command prompt.</span></span>

    
    <span data-ttu-id="f4edd-117"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f4edd-117"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

