---
title: 'Lync Server 2013 : Suppression des autorisations d’utilisateur authentifié'
description: 'Lync Server 2013 : les autorisations des utilisateurs authentifiés sont supprimées.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Authenticated user permissions are removed
ms:assetid: 5fcd70a5-813a-4076-9bb6-5b0d47505038
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398425(v=OCS.15)
ms:contentKeyID: 48184304
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 59da0ec893395405010afdd0263bd6be5d646881
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438154"
---
# <a name="authenticated-user-permissions-are-removed-in-lync-server-2013"></a><span data-ttu-id="c0d49-103">Suppression des autorisations d’utilisateur authentifié dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c0d49-103">Authenticated user permissions are removed in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c0d49-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c0d49-104">

<span> </span></span></span>

<span data-ttu-id="c0d49-105">_**Dernière modification de la rubrique :** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="c0d49-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="c0d49-106">Dans un environnement Active Directory verrouillé, les entrées de contrôle d’accès utilisateur authentifiées (ACE) sont supprimées des conteneurs Active Directory par défaut, y compris des utilisateurs, de la configuration ou du système et des unités d’organisation (UO) où les objets utilisateur et ordinateur sont stockés.</span><span class="sxs-lookup"><span data-stu-id="c0d49-106">In a locked-down Active Directory environment, authenticated user access control entries (ACEs) are removed from the default Active Directory containers, including the Users, Configuration or System, and organizational units (OUs) where User and Computer objects are stored.</span></span> <span data-ttu-id="c0d49-107">La suppression des entrées ACE d’utilisateur authentifiés empêche l’accès en lecture aux informations Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c0d49-107">Removing authenticated user ACEs prevents read access to Active Directory information.</span></span> <span data-ttu-id="c0d49-108">Toutefois, la suppression des ACE génère des problèmes pour Lync Server 2013, car elle dépend des autorisations en lecture sur ces conteneurs pour permettre aux utilisateurs d’effectuer la préparation du domaine.</span><span class="sxs-lookup"><span data-stu-id="c0d49-108">However, removing the ACEs creates issues for Lync Server 2013 because it depends on read permissions to these containers to allow users to run domain preparation.</span></span>

<span data-ttu-id="c0d49-109">Dans ce cas, l’appartenance au groupe administrateurs de domaine, qui est nécessaire pour exécuter la préparation du domaine, l’activation du serveur et la création de pool, ne accorde plus l’accès en lecture aux informations Active Directory stockées dans les conteneurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="c0d49-109">In this situation, membership in the Domain Admins group, which is required to run domain preparation, server activation, and pool creation, no longer grants read access to Active Directory information stored in the default containers.</span></span> <span data-ttu-id="c0d49-110">Pour vérifier la fin de la procédure de préparation de la forêt requise, vous devez attribuer manuellement des autorisations d’accès en lecture à divers conteneurs du domaine racine de la forêt.</span><span class="sxs-lookup"><span data-stu-id="c0d49-110">You must manually grant read-access permissions on various containers in the forest root domain to check that the prerequisite forest preparation procedure is complete.</span></span>

<span data-ttu-id="c0d49-111">Pour permettre à un utilisateur d’exécuter la préparation du domaine, l’activation du serveur ou la création de pool sur n’importe quel domaine racine sans forêt, vous disposez des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="c0d49-111">To enable a user to run domain preparation, server activation, or pool creation on any non-forest root domain, you have the following options:</span></span>

  - <span data-ttu-id="c0d49-112">Utilisez un compte membre du groupe administrateurs d’entreprise pour exécuter la préparation du domaine.</span><span class="sxs-lookup"><span data-stu-id="c0d49-112">Use an account that is a member of the Enterprise Admins group to run domain preparation.</span></span>

  - <span data-ttu-id="c0d49-113">Utilisez un compte membre du groupe administrateurs de domaine et octroyez des autorisations d’accès en lecture à ce compte sur chacun des conteneurs suivants dans le domaine racine de la forêt :</span><span class="sxs-lookup"><span data-stu-id="c0d49-113">Use an account that is a member of the Domain Admins group and grant this account read-access permissions on each of the following containers in the forest root domain:</span></span>
    
      - <span data-ttu-id="c0d49-114">Domaines</span><span class="sxs-lookup"><span data-stu-id="c0d49-114">Domain</span></span>
    
      - <span data-ttu-id="c0d49-115">Configuration ou système</span><span class="sxs-lookup"><span data-stu-id="c0d49-115">Configuration or System</span></span>

<span data-ttu-id="c0d49-116">Si vous ne voulez pas utiliser un compte membre du groupe administrateurs d’entreprise pour exécuter la préparation du domaine ou d’autres tâches de configuration, autorisez explicitement le compte auquel vous voulez utiliser l’accès en lecture sur les conteneurs pertinents de la racine de la forêt.</span><span class="sxs-lookup"><span data-stu-id="c0d49-116">If you do not want to use an account that is a member of the Enterprise Admins group to run domain preparation or other Setup tasks, explicitly grant the account you want to use read access on the relevant containers in the forest root.</span></span>

<div>

## <a name="to-give-users-read-access-permissions-on-containers-in-the-forest-root-domain"></a><span data-ttu-id="c0d49-117">Pour octroyer aux utilisateurs des autorisations de lecture dans le domaine racine de la forêt</span><span class="sxs-lookup"><span data-stu-id="c0d49-117">To give users read-access permissions on containers in the forest root domain</span></span>

1.  <span data-ttu-id="c0d49-118">Ouvrez une session sur l’ordinateur joint au domaine racine de la forêt avec un compte membre du groupe administrateurs de domaine pour le domaine racine de la forêt.</span><span class="sxs-lookup"><span data-stu-id="c0d49-118">Log on to the computer joined to the forest root domain with an account that is a member of the Domain Admins group for the forest root domain.</span></span>

2.  <span data-ttu-id="c0d49-119">Exécutez adsied. msc pour le domaine racine de la forêt.</span><span class="sxs-lookup"><span data-stu-id="c0d49-119">Run adsiedit.msc for the forest root domain.</span></span>
    
    <span data-ttu-id="c0d49-120">Si les ACE d’utilisateur authentifiés ont été supprimées du domaine, de la configuration ou du conteneur système, vous devez accorder des autorisations en lecture seule au conteneur, comme décrit dans les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="c0d49-120">If authenticated user ACEs were removed from the Domain, Configuration, or System container, you must grant read-only permissions to the container, as described in the following steps.</span></span>

3.  <span data-ttu-id="c0d49-121">Cliquez avec le bouton droit sur le conteneur, puis cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="c0d49-121">Right-click the container, and then click **Properties**.</span></span>

4.  <span data-ttu-id="c0d49-122">Cliquez sur l’onglet **sécurité** .</span><span class="sxs-lookup"><span data-stu-id="c0d49-122">Click the **Security** tab.</span></span>

5.  <span data-ttu-id="c0d49-123">Cliquez sur **Avancé**.</span><span class="sxs-lookup"><span data-stu-id="c0d49-123">Click **Advanced**.</span></span>

6.  <span data-ttu-id="c0d49-124">Dans l’onglet **autorisations** , cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="c0d49-124">On the **Permissions** tab, click **Add**.</span></span>

7.  <span data-ttu-id="c0d49-125">Entrez le nom du groupe ou de l’utilisateur en utilisant le format suivant : `domain\account name` , puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="c0d49-125">Type the name of the user or group receiving permissions by using the following format: `domain\account name`, and then click **OK**.</span></span>

8.  <span data-ttu-id="c0d49-126">Dans l’onglet **objets** , dans **s’applique à**, cliquez sur **cet objet uniquement**.</span><span class="sxs-lookup"><span data-stu-id="c0d49-126">On the **Objects** tab, in **Applies To**, click **This Object Only**.</span></span>

9.  <span data-ttu-id="c0d49-127">Dans **autorisations**, sélectionnez les entrées ACE suivantes, puis cliquez sur l’option **autoriser** la colonne : **contenu** de la liste, **lecture de toutes les propriétés** et **autorisations de lecture**.</span><span class="sxs-lookup"><span data-stu-id="c0d49-127">In **Permissions**, select the following Allow ACEs by clicking the **Allow** column: **List Content**, **Read All Properties**, and **Read Permissions**.</span></span>

10. <span data-ttu-id="c0d49-128">Cliquez sur **OK** à deux reprises.</span><span class="sxs-lookup"><span data-stu-id="c0d49-128">Click **OK** twice.</span></span>

11. <span data-ttu-id="c0d49-129">Répétez ces étapes pour chacun des conteneurs pertinents répertoriés à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="c0d49-129">Repeat these steps for any of the relevant containers listed in Step 2.</span></span>

<span data-ttu-id="c0d49-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c0d49-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

