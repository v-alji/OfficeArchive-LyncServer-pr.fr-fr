---
title: Test et signalement de la disponibilité fonctionnelle de l’authentification Kerberos
description: Testez et signalez la compatibilité fonctionnelle pour l’authentification Kerberos.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test and report functional readiness for Kerberos authentication
ms:assetid: d52c39e5-747d-4f29-88aa-30fd6f26b99c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398925(v=OCS.15)
ms:contentKeyID: 48185519
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5d32591a8cced7dce2e0bb78cc26189dce1900a3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444300"
---
# <a name="test-and-report-functional-readiness-for-kerberos-authentication-in-lync-server-2013"></a><span data-ttu-id="e6abe-103">Test et signalement de la disponibilité fonctionnelle de l’authentification Kerberos dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e6abe-103">Test and report functional readiness for Kerberos authentication in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e6abe-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e6abe-104">

<span> </span></span></span>

<span data-ttu-id="e6abe-105">_**Dernière modification de la rubrique :** 2012-01-16_</span><span class="sxs-lookup"><span data-stu-id="e6abe-105">_**Topic Last Modified:** 2012-01-16_</span></span>

<span data-ttu-id="e6abe-106">Pour effectuer cette procédure, vous devez être connecté en tant qu’utilisateur membre du groupe RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="e6abe-106">To successfully complete this procedure you should be logged on as a user who is a member of the RTCUniversalServerAdmins group.</span></span>

<span data-ttu-id="e6abe-107">Vous pouvez utiliser l’applet de contrôle Windows PowerShell **test-CsKerberosAccountAssignment** pour tester et signaler la disponibilité fonctionnelle d’une affectation de site pour l’authentification Kerberos.</span><span class="sxs-lookup"><span data-stu-id="e6abe-107">You can use the **Test-CsKerberosAccountAssignment** Windows PowerShell cmdlet to test and report the functional readiness of a site assignment for Kerberos authentication.</span></span> <span data-ttu-id="e6abe-108">Cette commande interroge le site spécifié dans le paramètre d’identité obligatoire.</span><span class="sxs-lookup"><span data-stu-id="e6abe-108">This command queries the site specified in the required Identity parameter.</span></span> <span data-ttu-id="e6abe-109">Le paramètre de rapport facultatif implique que l’applet de commande rédige un rapport HTML vers C : \\ logs sur l’ordinateur sur lequel la commande est exécutée.</span><span class="sxs-lookup"><span data-stu-id="e6abe-109">The optional Report parameter causes the cmdlet to write an HTML report to C:\\Logs on the computer on which the command is run.</span></span> <span data-ttu-id="e6abe-110">Le paramètre facultatif détaillé signale les informations d’activité à l’écran.</span><span class="sxs-lookup"><span data-stu-id="e6abe-110">The optional Verbose parameter reports activity information to the screen.</span></span>

<div>

## <a name="to-test-and-report-functional-readiness-for-kerberos-authentication-for-a-site"></a><span data-ttu-id="e6abe-111">Pour tester et signaler la compatibilité fonctionnelle pour l’authentification Kerberos pour un site</span><span class="sxs-lookup"><span data-stu-id="e6abe-111">To test and report functional readiness for Kerberos authentication for a site</span></span>

1.  <span data-ttu-id="e6abe-112">En tant que membre du groupe RTCUniversalServerAdmins, connectez-vous à un ordinateur du domaine exécutant Lync Server 2013 ou sur l’ordinateur sur lequel les outils d’administration sont installés.</span><span class="sxs-lookup"><span data-stu-id="e6abe-112">As a member of the RTCUniversalServerAdmins group, log on to a computer in the domain running Lync Server 2013 or on to the computer where the administrative tools are installed.</span></span>

2.  <span data-ttu-id="e6abe-113">Démarrez Lync Server Management Shell : cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="e6abe-113">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="e6abe-114">À partir de la ligne de commande, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="e6abe-114">From the command line, run the following command:</span></span>
    
        Test-CsKerberosAccountAssignment -Identity "site:SiteName" -Report "c:\logs\FileName.htm" -Verbose
    
    <span data-ttu-id="e6abe-115">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="e6abe-115">For example:</span></span>
    
        Test-CsKerberosAccountAssignment -Identity "site:Redmond" -Report "c:\logs\KerberosReport.htm" -Verbose

<span data-ttu-id="e6abe-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e6abe-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

