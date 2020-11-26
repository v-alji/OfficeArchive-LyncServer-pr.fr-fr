---
title: 'Lync Server 2013 : supprimer une annonce'
description: 'Lync Server 2013 : supprimer une annonce.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete an announcement
ms:assetid: 26ea7149-4470-4c22-9bab-8a4065aca44e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687998(v=OCS.15)
ms:contentKeyID: 49733588
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 722028f684734504d86bfc986250a2a1dd17fabc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430622"
---
# <a name="delete-an-announcement-in-lync-server-2013"></a><span data-ttu-id="1e8e7-103">Supprimer une annonce dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1e8e7-103">Delete an announcement in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1e8e7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1e8e7-104">

<span> </span></span></span>

<span data-ttu-id="1e8e7-105">_**Dernière modification de la rubrique :** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="1e8e7-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="1e8e7-106">Utilisez la procédure suivante pour supprimer une annonce utilisée pour les appels vers des numéros non attribués.</span><span class="sxs-lookup"><span data-stu-id="1e8e7-106">Use the following procedure to delete an announcement that is used for calls to unassigned numbers.</span></span>

<div>

## <a name="to-delete-an-announcement"></a><span data-ttu-id="1e8e7-107">Pour supprimer une annonce</span><span class="sxs-lookup"><span data-stu-id="1e8e7-107">To delete an announcement</span></span>

1.  <span data-ttu-id="1e8e7-108">Ouvrez une session sur l’ordinateur sur lequel Lync Server Management Shell est installé en tant que membre du groupe RTCUniversalServerAdmins ou avec les droits d’utilisateur nécessaires, comme décrit dans la rubrique [autorisations de configuration du délégué dans Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="1e8e7-108">Log on to the computer where Lync Server Management Shell is installed as a member of the RTCUniversalServerAdmins group or with the necessary user rights as described in [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="1e8e7-109">Démarrez Lync Server Management Shell : cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="1e8e7-109">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="1e8e7-p101">Répertoriez toutes les annonces de votre organisation. À partir de la ligne de commande, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="1e8e7-p101">List all the announcements in your organization. At the command line, run:</span></span>
    
        Get-CsAnnouncement

4.  <span data-ttu-id="1e8e7-p102">Dans la liste obtenue, recherchez l’annonce à supprimer et copiez le GUID. À partir de la ligne de commande, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="1e8e7-p102">In the resulting list, locate the announcement you want to delete, and copy the GUID. Then, at the command line, run:</span></span>
    
        Remove-CsAnnouncement -Identity "<Service:service ID/guid>" 
    
    <span data-ttu-id="1e8e7-114">Exemple :</span><span class="sxs-lookup"><span data-stu-id="1e8e7-114">For example:</span></span>
    
        Remove-CsAnnouncement -Identity "ApplicationServer:Redmond.contoso.com/1951f734-c80f-4fb2-965d-51807c792b90"
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="1e8e7-115">Pour plus d’informations sur les autres options, voir <A href="https://docs.microsoft.com/powershell/module/skype/Get-CsAnnouncement">Get-CsAnnouncement</A> et <A href="https://docs.microsoft.com/powershell/module/skype/Remove-CsAnnouncement">Remove-CsAnnouncement</A>.</span><span class="sxs-lookup"><span data-stu-id="1e8e7-115">For details about more options, see <A href="https://docs.microsoft.com/powershell/module/skype/Get-CsAnnouncement">Get-CsAnnouncement</A> and <A href="https://docs.microsoft.com/powershell/module/skype/Remove-CsAnnouncement">Remove-CsAnnouncement</A>.</span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="1e8e7-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e8e7-116">See Also</span></span>


[<span data-ttu-id="1e8e7-117">Créer une annonce dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1e8e7-117">Create an announcement in Lync Server 2013</span></span>](lync-server-2013-create-an-announcement.md)  


[<span data-ttu-id="1e8e7-118">Remove-CsAnnouncement</span><span class="sxs-lookup"><span data-stu-id="1e8e7-118">Remove-CsAnnouncement</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsAnnouncement)  
[<span data-ttu-id="1e8e7-119">Get-CsAnnouncement</span><span class="sxs-lookup"><span data-stu-id="1e8e7-119">Get-CsAnnouncement</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsAnnouncement)  
  

<span data-ttu-id="1e8e7-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1e8e7-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

