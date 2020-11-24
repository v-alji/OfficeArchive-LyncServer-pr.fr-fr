---
title: 'Lync Server 2013 : Schéma de base de données de conversation permanente'
description: 'Lync Server 2013 : schéma de base de données de discussions persistantes.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Persistent Chat database schema
ms:assetid: 58d7d94f-42f5-4c3e-8fe5-901fbe92152e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558653(v=OCS.15)
ms:contentKeyID: 48184228
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 66151201f65310cc8e6d3f2251be4f86ce2be15d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394353"
---
# <a name="persistent-chat-database-schema-in-lync-server-2013"></a><span data-ttu-id="5f012-103">Schéma de base de données de conversation permanente dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5f012-103">Persistent Chat database schema in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5f012-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5f012-104">

<span> </span></span></span>

<span data-ttu-id="5f012-105">_**Dernière modification de la rubrique :** 2012-09-18_</span><span class="sxs-lookup"><span data-stu-id="5f012-105">_**Topic Last Modified:** 2012-09-18_</span></span>

<span data-ttu-id="5f012-106">Ce document décrit le schéma de la base de données de chat persistante dans le logiciel de communication de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="5f012-106">This documents the schema of the Persistent Chat database in Lync Server 2013 communications software.</span></span>

<span data-ttu-id="5f012-107">La base de données de chat permanent fait référence à la base de données qui correspond à l' **PersistentChatStore** de rôles de serveur principal Lync Server 2013 (qui correspond à la base de données MGC) et **PersistentChatComplianceStore** (qui correspond à la base de données mgccomp).</span><span class="sxs-lookup"><span data-stu-id="5f012-107">The Persistent Chat database refers to the database corresponding to the Lync Server 2013 Back End Server roles **PersistentChatStore** (corresponding to the mgc database) and **PersistentChatComplianceStore** (corresponding to the mgccomp database).</span></span> <span data-ttu-id="5f012-108">L’objectif de la publication de ce schéma consiste à vous permettre de créer des requêtes et d’accéder à des informations sur la création de rapports utiles sur l’utilisation des discussions, des salles actives, les principaux bureaux d’information, etc.</span><span class="sxs-lookup"><span data-stu-id="5f012-108">The goal of publishing this schema is to enable you to build queries and gain some insights into building useful reporting around chat usage, active rooms, top posters, and so on.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="5f012-109">Nous nous réservons le droit d’évolutionr ce schéma.</span><span class="sxs-lookup"><span data-stu-id="5f012-109">We reserve the right to evolve this schema.</span></span> <span data-ttu-id="5f012-110">Microsoft n’apporte aucune garantie de conservation de la compatibilité descendante avec ce schéma publié.</span><span class="sxs-lookup"><span data-stu-id="5f012-110">Microsoft does not make any guarantees to maintain full backward compatibility with this published schema.</span></span>



</div>

<span data-ttu-id="5f012-111">Suivez ces meilleures pratiques :</span><span class="sxs-lookup"><span data-stu-id="5f012-111">Follow these best practices:</span></span>

  - <span data-ttu-id="5f012-112">Aucune sélection \* //est prise en charge, car la liste de colonnes peut grandir.</span><span class="sxs-lookup"><span data-stu-id="5f012-112">No SELECT\* // is supported because the column list can grow.</span></span>

  - <span data-ttu-id="5f012-113">Aucune modification de schéma générée par l’utilisateur n’est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="5f012-113">No user-generated schema modifications are supported.</span></span>

  - <span data-ttu-id="5f012-114">Aucune opération d’écriture n’est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="5f012-114">No write operations are supported.</span></span>

  - <span data-ttu-id="5f012-115">Testez toutes les requêtes que vous créez sur des bases de données de taille représentative pour vous assurer que les requêtes peuvent être effectuées à un niveau en fonction de vos besoins.</span><span class="sxs-lookup"><span data-stu-id="5f012-115">Test any queries that you build on representatively-sized databases to be sure that the queries can perform at a level to meet your needs.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="5f012-116">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="5f012-116">In This Section</span></span>

  - [<span data-ttu-id="5f012-117">Liste des tables de serveur de conversation permanente dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5f012-117">List of Persistent Chat Server tables in Lync Server 2013</span></span>](lync-server-2013-list-of-persistent-chat-server-tables.md)

  - [<span data-ttu-id="5f012-118">Liste des tables de conformité avec le serveur de conversation permanente dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5f012-118">List of Persistent Chat Server compliance tables in Lync Server 2013</span></span>](lync-server-2013-list-of-persistent-chat-server-compliance-tables.md)

  - [<span data-ttu-id="5f012-119">Détails de la table des serveurs de conversation permanente dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5f012-119">Persistent Chat Server table details in Lync Server 2013</span></span>](lync-server-2013-persistent-chat-server-table-details.md)

  - [<span data-ttu-id="5f012-120">Exemples de requêtes de base de données de conversation permanente pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5f012-120">Sample Persistent Chat database queries for Lync Server 2013</span></span>](lync-server-2013-sample-persistent-chat-database-queries.md)

<span data-ttu-id="5f012-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5f012-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

