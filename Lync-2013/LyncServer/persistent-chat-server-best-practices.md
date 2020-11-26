---
title: Meilleures pratiques liées au serveur de conversation permanente
description: Pratiques recommandées pour le serveur de chat permanent.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Persistent Chat Server best practices
ms:assetid: dc18e7f7-599b-4d32-abf7-cd9e691426a2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398970(v=OCS.15)
ms:contentKeyID: 48185612
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5c575c0afa0366e88748eadfcf4c04fccb20b375
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438784"
---
# <a name="persistent-chat-server-best-practices"></a><span data-ttu-id="f45cf-103">Meilleures pratiques liées au serveur de conversation permanente</span><span class="sxs-lookup"><span data-stu-id="f45cf-103">Persistent Chat Server best practices</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f45cf-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f45cf-104">

<span> </span></span></span>

<span data-ttu-id="f45cf-105">_**Dernière modification de la rubrique :** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="f45cf-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="f45cf-106">Lorsque vous créez des catégories et des salles de conversation permanente et que vous concevez votre étendue et votre appartenance, les conseils suivants peuvent vous aider à planifier :</span><span class="sxs-lookup"><span data-stu-id="f45cf-106">As you create your categories and Persistent Chat rooms and design your scoping and membership, the following tips can help your planning:</span></span>

  - <span data-ttu-id="f45cf-107">Si votre entreprise n’a pas besoin d’une paroi éthique, n’Affinez pas l’étendue dans votre arborescence de catégories.</span><span class="sxs-lookup"><span data-stu-id="f45cf-107">If your company does not require an ethical wall, do not narrow the scope in your category tree.</span></span> <span data-ttu-id="f45cf-108">Placez tous vos utilisateurs dans l’étendue d’une catégorie et créez toutes les salles de conversation dans cette catégorie.</span><span class="sxs-lookup"><span data-stu-id="f45cf-108">Put all your users in the scope of one category, and create all chat rooms in that category.</span></span> <span data-ttu-id="f45cf-109">Par la suite, utilisez uniquement les listes d’appartenance pour octroyer ou restreindre l’accès à chaque salle de conversation.</span><span class="sxs-lookup"><span data-stu-id="f45cf-109">Subsequently, use only membership lists to grant or restrict access to each chat room.</span></span>

  - <span data-ttu-id="f45cf-110">Dans la plupart des cas, vous devez permettre aux utilisateurs de créer des salles de conversation pour que les discussions relatives aux nouvelles rubriques puissent être démarrées à tout moment.</span><span class="sxs-lookup"><span data-stu-id="f45cf-110">In most cases, you should enable users to create new chat rooms so that discussions about new topics can be started any time.</span></span> <span data-ttu-id="f45cf-111">Pour cela, vous devez créer la liste de **créateurs** comme la liste **AllowedMembers** .</span><span class="sxs-lookup"><span data-stu-id="f45cf-111">Do this by making the **Creators** list the same as the **AllowedMembers** list.</span></span> <span data-ttu-id="f45cf-112">Toutefois, si vous voulez autoriser uniquement une équipe de support centrale ou des utilisateurs spécifiques à créer des salles, faites de la liste des **créateurs** en tant que sous-ensemble approprié.</span><span class="sxs-lookup"><span data-stu-id="f45cf-112">However, if you want to allow only a central support team or designated users to create rooms, then make the **Creators** list as the appropriate subset.</span></span>

  - <span data-ttu-id="f45cf-113">Donnez à chaque salle de conversation un nom complet et une description qui décrivent l’endroit où il s’inscrit à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="f45cf-113">Give each chat room a complete name and description summary that describes where it fits in with your organization.</span></span> <span data-ttu-id="f45cf-114">Dans la mesure où les utilisateurs ne peuvent pas voir le nom de la catégorie lorsqu’ils utilisent la salle de conversation, vous ne pouvez pas compter sur le nom de la catégorie pour permettre aux utilisateurs de déterminer le Forum de discussion prévu pour la salle de conversation.</span><span class="sxs-lookup"><span data-stu-id="f45cf-114">Because users cannot see the category name when they use the chat room, you cannot rely on the category name to help users determine the intended discussion forum for the chat room.</span></span>

  - <span data-ttu-id="f45cf-115">Vous pouvez avoir besoin d’un flux de travail de création de salle personnalisé si vous disposez de certaines conventions d’affectation de noms ou de contrôles Access ou de validations à implémenter.</span><span class="sxs-lookup"><span data-stu-id="f45cf-115">You may want to have a custom room creation workflow if you have certain naming conventions or other access controls or validations to implement.</span></span> <span data-ttu-id="f45cf-116">La configuration de chat permanent vous permet de personnaliser le **RoomManagementUrl** sur un nom que vous avez hébergé.</span><span class="sxs-lookup"><span data-stu-id="f45cf-116">The Persistent Chat configuration enables you to customize the **RoomManagementUrl** to something that you host.</span></span> <span data-ttu-id="f45cf-117">Par exemple, quand un utilisateur clique sur **créer une salle** dans son client Lync, il peut être redirigé vers votre solution personnalisée.</span><span class="sxs-lookup"><span data-stu-id="f45cf-117">For example, when users click **Create a room** in their Lync client, they can be redirected to your custom solution.</span></span>

  - <span data-ttu-id="f45cf-118">Créez divers compléments qui vous permettent d’améliorer l’exploitation des salles de conversation en ajoutant d’autres données métiers dans des salles de conversation.</span><span class="sxs-lookup"><span data-stu-id="f45cf-118">Create a variety of add-ins that help to enhance the experience of chat rooms by bringing in other business data into chat rooms.</span></span> <span data-ttu-id="f45cf-119">Les administrateurs doivent inscrire les compléments qu’ils souhaitent autoriser dans le système.</span><span class="sxs-lookup"><span data-stu-id="f45cf-119">Administrators must register the add-ins that they want to allow in the system.</span></span> <span data-ttu-id="f45cf-120">Les gestionnaires de salle de conversation et les créateurs peuvent choisir dans la liste des compléments autorisés pour les composants les plus pertinents pour leurs salles respectives.</span><span class="sxs-lookup"><span data-stu-id="f45cf-120">Chat room managers and creators can choose from the list of allowed add-ins for the ones most relevant to their respective rooms.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="f45cf-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f45cf-121">See Also</span></span>


[<span data-ttu-id="f45cf-122">Gestion des catégories, des salles et des compléments dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f45cf-122">Managing categories, rooms, and add-ins in Lync Server 2013</span></span>](lync-server-2013-managing-categories-rooms-and-add-ins.md)  
  

<span data-ttu-id="f45cf-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f45cf-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

