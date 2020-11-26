---
title: 'Lync Server 2013 : Configuration de l’authentification Kerberos'
description: 'Lync Server 2013 : configuration de l’authentification Kerberos.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up Kerberos authentication
ms:assetid: dd8009ef-6265-4cc0-b2c7-e474cd1f4b09
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398976(v=OCS.15)
ms:contentKeyID: 48185601
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bb461968bc073edbfe640f609257f3e84c192461
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441717"
---
# <a name="setting-up-kerberos-authentication-in-lync-server-2013"></a><span data-ttu-id="e5b54-103">Configuration de l’authentification Kerberos dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e5b54-103">Setting up Kerberos authentication in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e5b54-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e5b54-104">

<span> </span></span></span>

<span data-ttu-id="e5b54-105">_**Dernière modification de la rubrique :** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="e5b54-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="e5b54-106">Lync Server 2013 prend en charge l’authentification NTLM et Kerberos pour les services Web.</span><span class="sxs-lookup"><span data-stu-id="e5b54-106">Lync Server 2013 supports NTLM and Kerberos authentication for Web Services.</span></span> <span data-ttu-id="e5b54-107">Office Communications Server 2007 et Office Communications Server 2007 R2 utilisaient le RTCComponentService et RTCService par défaut en tant que comptes d’utilisateurs pour exécuter les pools d’applications de services Web, ce qui permet d’affecter un nom de principal de service (SPN) aux comptes d’utilisateurs et d’agir en tant que principal d’authentification.</span><span class="sxs-lookup"><span data-stu-id="e5b54-107">Office Communications Server 2007 and Office Communications Server 2007 R2 used the default RTCComponentService and RTCService as the user accounts to run the Web Services application pools, allowing for a service principal name (SPN) to be assigned to the user accounts and to act as the authentication principal.</span></span> <span data-ttu-id="e5b54-108">Lync Server utilise NetworkService pour exécuter les services Web et NetworkService ne peut pas avoir de SPN qui lui est affecté.</span><span class="sxs-lookup"><span data-stu-id="e5b54-108">Lync Server uses NetworkService to run Web Services and NetworkService cannot have SPNs assigned to it.</span></span>

<span data-ttu-id="e5b54-109">Pour résoudre le problème que vous n’avez pas d’objets Active Directory devant contenir les noms d’application (SPN), le panneau de configuration de Lync Server peut utiliser les objets de compte d’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="e5b54-109">To solve the issue of not having Active Directory objects to hold the SPNs, Lync Server Control Panel can use computer account objects for this purpose.</span></span> <span data-ttu-id="e5b54-110">Les objets de compte d’ordinateur peuvent contenir les SPN et ne sont pas soumis à l’expiration du mot de passe, ce qui fut un problème lors de l’utilisation de comptes d’utilisateur dans les versions précédentes.</span><span class="sxs-lookup"><span data-stu-id="e5b54-110">The computer account objects can hold the SPNs and are not subject to password expiration, which was an issue with using user accounts in previous versions.</span></span>

<span data-ttu-id="e5b54-111">Les applets de cmdlet Windows PowerShell vous permettent de configurer les objets ordinateur pour fournir une authentification Kerberos.</span><span class="sxs-lookup"><span data-stu-id="e5b54-111">You use Windows PowerShell cmdlets to configure the computer objects to provide Kerberos authentication.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="e5b54-112">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="e5b54-112">In This Section</span></span>

  - [<span data-ttu-id="e5b54-113">Conditions prérequises à l’activation de l’authentification Kerberos dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e5b54-113">Prerequisites for enabling Kerberos authentication in Lync Server 2013</span></span>](lync-server-2013-prerequisites-for-enabling-kerberos-authentication.md)

  - [<span data-ttu-id="e5b54-114">Création d’un compte d’authentification Kerberos dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e5b54-114">Create a Kerberos authentication account in Lync Server 2013</span></span>](lync-server-2013-create-a-kerberos-authentication-account.md)

  - [<span data-ttu-id="e5b54-115">Attribution d’un compte d’authentification Kerberos sur un site dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e5b54-115">Assign a Kerberos authentication account to a site in Lync Server 2013</span></span>](lync-server-2013-assign-a-kerberos-authentication-account-to-a-site.md)

  - [<span data-ttu-id="e5b54-116">Configuration des mots de passe de compte d’authentification Kerberos dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e5b54-116">Setting up Kerberos authentication account passwords in Lync Server 2013</span></span>](lync-server-2013-setting-up-kerberos-authentication-account-passwords.md)

  - [<span data-ttu-id="e5b54-117">Ajout d’une authentification Kerberos à d’autres sites dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e5b54-117">In Lync Server 2013 add Kerberos authentication to other sites</span></span>](lync-server-2013-add-kerberos-authentication-to-other-sites.md)

  - [<span data-ttu-id="e5b54-118">Suppression de l’authentification Kerberos d’un site dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e5b54-118">In Lync Server 2013 remove Kerberos authentication from a site</span></span>](lync-server-2013-remove-kerberos-authentication-from-a-site.md)

  - [<span data-ttu-id="e5b54-119">Test et création de rapports sur l’état et l’affectation de l’authentification Kerberos dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e5b54-119">Testing and reporting the status and assignment of Kerberos authentication in Lync Server 2013</span></span>](lync-server-2013-testing-and-reporting-the-status-and-assignment-of-kerberos-authentication.md)

<span data-ttu-id="e5b54-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e5b54-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

