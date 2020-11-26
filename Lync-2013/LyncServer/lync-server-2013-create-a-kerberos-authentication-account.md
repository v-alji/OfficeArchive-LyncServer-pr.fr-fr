---
title: 'Lync Server 2013 : Création d’un compte d’authentification Kerberos'
description: 'Lync Server 2013 : créer un compte d’authentification Kerberos.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create a Kerberos authentication account
ms:assetid: 63f0cef6-562a-4209-ae25-71f8dc7c7295
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398449(v=OCS.15)
ms:contentKeyID: 48184348
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b2f8e87a8ffcc95af4a44e516ac4e1f4d635d737
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432176"
---
# <a name="create-a-kerberos-authentication-account-in-lync-server-2013"></a><span data-ttu-id="919f1-103">Création d’un compte d’authentification Kerberos dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="919f1-103">Create a Kerberos authentication account in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="919f1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="919f1-104">

<span> </span></span></span>

<span data-ttu-id="919f1-105">_**Dernière modification de la rubrique :** 2012-01-02_</span><span class="sxs-lookup"><span data-stu-id="919f1-105">_**Topic Last Modified:** 2012-01-02_</span></span>

<span data-ttu-id="919f1-106">Pour effectuer cette procédure, vous devez être connecté au serveur ou au domaine au minimum en tant que membre du groupe Domain Admins.</span><span class="sxs-lookup"><span data-stu-id="919f1-106">To successfully complete this procedure, you should be logged on to the server or domain minimally as a member of the Domain Admins group.</span></span>

<span data-ttu-id="919f1-107">Vous pouvez créer des comptes d’authentification Kerberos pour chaque site, ou vous pouvez créer un compte d’authentification Kerberos unique et l’utiliser pour tous les sites.</span><span class="sxs-lookup"><span data-stu-id="919f1-107">You can create Kerberos authentication accounts for each site or you can create a single Kerberos authentication account and use it for all sites.</span></span> <span data-ttu-id="919f1-108">Les applets de cmdlet Windows PowerShell vous permettent de créer et de gérer les comptes, y compris l’identification des comptes attribués à chaque site.</span><span class="sxs-lookup"><span data-stu-id="919f1-108">You use Windows PowerShell cmdlets to create and manage the accounts, including identifying the accounts assigned to each site.</span></span> <span data-ttu-id="919f1-109">Le générateur de topologie et le panneau de configuration de Lync Server 2013 n’affichent pas de comptes d’authentification Kerberos.</span><span class="sxs-lookup"><span data-stu-id="919f1-109">Topology Builder and the Lync Server 2013 Control Panel do not display Kerberos authentication accounts.</span></span> <span data-ttu-id="919f1-110">Utilisez la procédure suivante pour créer un ou plusieurs comptes d’utilisateur à utiliser pour l’authentification Kerberos.</span><span class="sxs-lookup"><span data-stu-id="919f1-110">Use the following procedure to create one or more user accounts to be used for Kerberos authentication.</span></span>

<div>

## <a name="to-create-a-kerberos-account"></a><span data-ttu-id="919f1-111">Pour créer un compte Kerberos</span><span class="sxs-lookup"><span data-stu-id="919f1-111">To create a Kerberos account</span></span>

1.  <span data-ttu-id="919f1-112">En tant que membre du groupe Domain Admins, connectez-vous à un ordinateur du domaine exécutant Lync Server 2013 ou sur un ordinateur sur lequel les outils d’administration sont installés.</span><span class="sxs-lookup"><span data-stu-id="919f1-112">As a member of the Domain Admins group, log on to a computer in the domain running Lync Server 2013 or on to a computer where the administrative tools are installed.</span></span>

2.  <span data-ttu-id="919f1-113">Démarrez Lync Server Management Shell : cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="919f1-113">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="919f1-114">À partir de la ligne de commande, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="919f1-114">From the command line, run the following command:</span></span>
    
        New-CsKerberosAccount -UserAccount "Domain\UserAccount" -ContainerDN "CN=Users,DC=DomainName,DC=DomainExtension"
    
    <span data-ttu-id="919f1-115">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="919f1-115">For example:</span></span>
    
        New-CsKerberosAccount -UserAccount "Contoso\KerbAuth" -ContainerDN "CN=Users,DC=contoso,DC=com"

4.  <span data-ttu-id="919f1-116">Vérifiez que l’objet ordinateur a été créé en ouvrant utilisateurs et ordinateurs Active Directory, développez le conteneur **utilisateurs** , puis vérifiez que l’objet ordinateur du compte d’utilisateur est dans le conteneur.</span><span class="sxs-lookup"><span data-stu-id="919f1-116">Confirm that the Computer object was created by opening Active Directory User and Computers, expand the **Users** container, and then confirm that the Computer object for the user account is in the container.</span></span>

<span data-ttu-id="919f1-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="919f1-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

