---
title: Vérification de la connectivité entre les serveurs internes et les serveurs Edge
description: Vérifiez la connectivité entre les serveurs internes et les serveurs Edge.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Verify connectivity between internal servers and Edge Servers
ms:assetid: 219f706e-2b8a-46c5-b394-c384240eef50
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398292(v=OCS.15)
ms:contentKeyID: 48183602
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f86f87428d7eaf91b8f70422cfee712584252fad
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395060"
---
# <a name="verify-connectivity-between-internal-servers-and-edge-servers-in-lync-server-2013"></a><span data-ttu-id="c0e1e-103">Vérification de la connectivité entre les serveurs internes et les serveurs Edge dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c0e1e-103">Verify connectivity between internal servers and Edge Servers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c0e1e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c0e1e-104">

<span> </span></span></span>

<span data-ttu-id="c0e1e-105">_**Dernière modification de la rubrique :** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="c0e1e-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="c0e1e-106">Dans Lync Server 2013, un Assistant validation distinct a été disponible pour vous permettre de valider la connectivité entre les serveurs Edge et les serveurs internes.</span><span class="sxs-lookup"><span data-stu-id="c0e1e-106">In Lync Server 2013, a separate validation wizard was available to help validate connectivity between Edge Servers and internal servers.</span></span> <span data-ttu-id="c0e1e-107">Dans Lync Server 2013, la validation de la connectivité est exécutée automatiquement lorsque vous installez vos serveurs Edge.</span><span class="sxs-lookup"><span data-stu-id="c0e1e-107">In Lync Server 2013 validation of connectivity is done automatically when you install your Edge Servers.</span></span>

<span data-ttu-id="c0e1e-108">Vous pouvez valider la réplication des informations de configuration sur le bord en exécutant l’applet de contrôle Windows PowerShell **Get-CsManagementStoreReplicationStatus** sur l’ordinateur interne sur lequel se trouve la Banque centrale de gestion (ou n’importe quel ordinateur ayant rejoint les composants principaux de Lync Server 2013 (OcsCore.msi).</span><span class="sxs-lookup"><span data-stu-id="c0e1e-108">You can validate the replication of configuration information to the edge by running the Windows PowerShell **Get-CsManagementStoreReplicationStatus** cmdlet on the internal computer on which the Central Management store is located (or any domain joined computer on which Lync Server 2013 Core Components (OcsCore.msi) is installed.</span></span> <span data-ttu-id="c0e1e-109">Les résultats initiaux risquent d’indiquer l’état « false » au lieu de « true » pour la réplication.</span><span class="sxs-lookup"><span data-stu-id="c0e1e-109">Initial results may indicate the status as "False" instead of "True" for replication.</span></span> <span data-ttu-id="c0e1e-110">Si tel est le cas, exécutez l’applet de connexion **Invoke-CsManagementStoreReplication** et attendez la fin de la réplication avant d’exécuter de nouveau **Get-CsManagementStoreReplicationStatus** .</span><span class="sxs-lookup"><span data-stu-id="c0e1e-110">If so, run the **Invoke-CsManagementStoreReplication** cmdlet and allow time for the replication to complete before running the **Get-CsManagementStoreReplicationStatus** again.</span></span>

<span data-ttu-id="c0e1e-111">Vous pouvez vérifier la connectivité des utilisateurs externes séparément, y compris à l’aide de l’analyseur de connectivité à distance d’Office Communications Server pour vérifier la connectivité des utilisateurs distants.</span><span class="sxs-lookup"><span data-stu-id="c0e1e-111">You can verify external user connectivity separately, including using the Office Communications Server Remote Connectivity Analyzer to verify remote user connectivity.</span></span> <span data-ttu-id="c0e1e-112">Pour plus d’informations, consultez [Vérifier la connectivité des utilisateurs externes dans Lync Server 2013](lync-server-2013-verify-connectivity-for-external-users.md).</span><span class="sxs-lookup"><span data-stu-id="c0e1e-112">For details, see [Verify connectivity for external users in Lync Server 2013](lync-server-2013-verify-connectivity-for-external-users.md).</span></span>

<span data-ttu-id="c0e1e-113"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c0e1e-113"></div>

<span> </span>

</div>

</div>

</span></span></div>

