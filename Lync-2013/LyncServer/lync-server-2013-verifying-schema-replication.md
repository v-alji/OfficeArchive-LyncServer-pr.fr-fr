---
title: 'Lync Server 2013 : Vérification de la réplication de schéma'
description: 'Lync Server 2013 : vérification de la réplication de schéma.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Verifying schema replication
ms:assetid: ad01a7cf-aa79-4648-ba5a-a7a09172db36
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412822(v=OCS.15)
ms:contentKeyID: 48185124
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 019cd06db05a9ba683767f550a712ef188b47508
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438896"
---
# <a name="verifying-active-directory-schema-replication-in-lync-server-2013"></a><span data-ttu-id="7b45c-103">Vérification de la réplication de schéma Active Directory dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7b45c-103">Verifying Active Directory schema replication in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7b45c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7b45c-104">

<span> </span></span></span>

<span data-ttu-id="7b45c-105">_**Dernière modification de la rubrique :** 2012-10-29_</span><span class="sxs-lookup"><span data-stu-id="7b45c-105">_**Topic Last Modified:** 2012-10-29_</span></span>

<span data-ttu-id="7b45c-106">Avant de procéder à la préparation de la forêt, vérifiez manuellement que celle-ci a été répliquée.</span><span class="sxs-lookup"><span data-stu-id="7b45c-106">Before you run forest preparation, manually verify that the schema partition has been replicated.</span></span>

<div>

## <a name="to-manually-verify-schema-replication"></a><span data-ttu-id="7b45c-107">Pour vérifier manuellement la réplication de schéma</span><span class="sxs-lookup"><span data-stu-id="7b45c-107">To manually verify schema replication</span></span>

1.  <span data-ttu-id="7b45c-108">Ouvrez une session sur un contrôleur de domaine en tant que membre du groupe administrateurs d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="7b45c-108">Log on to a domain controller as a member of the Enterprise Admins group.</span></span>

2.  <span data-ttu-id="7b45c-109">Ouvrez ADSI Edit en cliquant sur **Démarrer**, sur **Outils d’administration**, puis sur **modification ADSI**.</span><span class="sxs-lookup"><span data-stu-id="7b45c-109">Open ADSI Edit by clicking **Start**, clicking **Administrative Tools**, and then clicking **ADSI Edit**.</span></span>
    
    <div>
    

    > [!TIP]  
    > <span data-ttu-id="7b45c-110">Vous pouvez également exécuter <STRONG>adsied. msc</STRONG> à partir de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="7b45c-110">Alternatively, you can run <STRONG>adsiedit.msc</STRONG> from the command line.</span></span>

    
    </div>

3.  <span data-ttu-id="7b45c-111">Dans l’arborescence Microsoft Management Console (MMC), si ce n’est pas déjà fait, cliquez sur **ADSI Edit**.</span><span class="sxs-lookup"><span data-stu-id="7b45c-111">In the Microsoft Management Console (MMC) tree, if it is not already selected, click **ADSI Edit**.</span></span>

4.  <span data-ttu-id="7b45c-112">Dans le menu **Action**, cliquez sur **Connexion**.</span><span class="sxs-lookup"><span data-stu-id="7b45c-112">On the **Action** menu, click **Connect to**.</span></span>

5.  <span data-ttu-id="7b45c-113">Dans la boîte de dialogue **Paramètres de connexion** sous **Sélectionnez un contexte d’attribution de noms connu**, sélectionnez **Schéma**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="7b45c-113">In the **Connection Settings** dialog box under **Select a well known Naming Context**, select **Schema**, and then click **OK**.</span></span>

6.  <span data-ttu-id="7b45c-114">Sous le conteneur de schéma, recherchez CN=ms-RTC-SIP-SchemaVersion.</span><span class="sxs-lookup"><span data-stu-id="7b45c-114">Under the schema container, search for CN=ms-RTC-SIP-SchemaVersion.</span></span> <span data-ttu-id="7b45c-115">Si cet objet existe et que la valeur de l’attribut **rangeUpper** est 1150 et que la valeur de l’attribut **rangeLower** est 3, le schéma a été correctement mis à jour et répliqué.</span><span class="sxs-lookup"><span data-stu-id="7b45c-115">If this object exists, and the value of the **rangeUpper** attribute is 1150 and the value of the **rangeLower** attribute is 3, then the schema was successfully updated and replicated.</span></span> <span data-ttu-id="7b45c-116">Si cet objet n’existe pas ou si les valeurs des attributs **rangeUpper** et **rangeLower** ne sont pas spécifiées, le schéma n’a pas été modifié ou n’a pas été répliqué.</span><span class="sxs-lookup"><span data-stu-id="7b45c-116">If this object does not exist or the values of the **rangeUpper** and **rangeLower** attributes are not as specified, then the schema was not modified or has not replicated.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="7b45c-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7b45c-117">See Also</span></span>


[<span data-ttu-id="7b45c-118">Exécution de la préparation du schéma Active Directory dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7b45c-118">Running Active Directory schema preparation in Lync Server 2013</span></span>](lync-server-2013-running-schema-preparation.md)  


[<span data-ttu-id="7b45c-119">Préparation du schéma Active Directory dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7b45c-119">Preparing the Active Directory schema in Lync Server 2013</span></span>](lync-server-2013-preparing-the-active-directory-schema.md)  
  

<span data-ttu-id="7b45c-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7b45c-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

