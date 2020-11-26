---
title: 'Lync Server 2013 : Remarque sur la connectivité Lync-Skype pour Lync sur'
description: 'Lync Server 2013 : Remarque sur la connectivité Lync-Skype pour Lync.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Note about Lync-Skype connectivity for Lync On
ms:assetid: 1d0f5c1a-74c6-468f-9877-ad2b1ddf355f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn440169(v=OCS.15)
ms:contentKeyID: 57793359
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3f7d9758f277f2f987677c2c0ffa0a4447ba31d1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424974"
---
# <a name="note-about-lync-skype-connectivity-in-lync-server-2013-for-lync-online-customers"></a><span data-ttu-id="a39fd-103">Remarque concernant la connectivité Lync-Skype dans Lync Server 2013 pour les clients Lync Online</span><span class="sxs-lookup"><span data-stu-id="a39fd-103">Note about Lync-Skype connectivity in Lync Server 2013 for Lync Online customers</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a39fd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a39fd-104">

<span> </span></span></span>

<span data-ttu-id="a39fd-105">_**Dernière modification de la rubrique :** 2013-09-23_</span><span class="sxs-lookup"><span data-stu-id="a39fd-105">_**Topic Last Modified:** 2013-09-23_</span></span>

<span data-ttu-id="a39fd-106">Ce document a été rédigé pour faciliter l’organisation de la connectivité Lync-Skype de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="a39fd-106">This document was written to help Lync Server on-premise administrators set up Lync-Skype connectivity.</span></span>  <span data-ttu-id="a39fd-107">Lync-Skype connectivité est également une fonctionnalité de Lync Online, qui fait partie d’Office 365 et Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="a39fd-107">Lync-Skype connectivity is also a feature of Lync Online, which is part of Office 365 and Microsoft 365.</span></span> <span data-ttu-id="a39fd-108">Vous pouvez activer la fonctionnalité de connectivité Lync-Skype à partir du centre d’administration Lync dans le centre d’administration.</span><span class="sxs-lookup"><span data-stu-id="a39fd-108">You can enable the Lync-Skype connectivity feature from the Lync Administration Center within the admin center.</span></span>

<span data-ttu-id="a39fd-109">Pour Microsoft 365 moyenne entreprise, Office 365 entreprise, Microsoft 365 éducation et Office 365 pour le secteur public : se connecter au portail Office 365 ou au centre d’administration Microsoft 365 et accéder au **Centre d’administration Lync**.</span><span class="sxs-lookup"><span data-stu-id="a39fd-109">For Microsoft 365 Midsize Business, Office 365 Enterprise, Microsoft 365 Education, and Office 365 for Government: Sign in to the Office 365 portal or Microsoft 365 admin center and navigate to the **Lync Administration Center**.</span></span> <span data-ttu-id="a39fd-110">Accédez à **communications externes**.</span><span class="sxs-lookup"><span data-stu-id="a39fd-110">Go to **External Communications**.</span></span> <span data-ttu-id="a39fd-111">Sous **fournisseurs de services de messagerie instantanée publique**, cliquez sur **activer**.</span><span class="sxs-lookup"><span data-stu-id="a39fd-111">Under **Public IM Service Providers**, click **Enable**.</span></span> <span data-ttu-id="a39fd-112">Si vous voulez contrôler l’accès d’un utilisateur individuel à Lync-Skype connectivité, vous pouvez le faire en modifiant les paramètres de communication externe des utilisateurs individuels.</span><span class="sxs-lookup"><span data-stu-id="a39fd-112">If you want to control individual user access to Lync-Skype Connectivity, you can do so by editing individual users’ External Communications settings.</span></span>

<span data-ttu-id="a39fd-113">Pour Microsoft 365 petite entreprise Premium : Connectez-vous à Microsoft 365, puis accédez à **paramètres du service d’administration \> \> messagerie instantanée, réunions et conférences**.</span><span class="sxs-lookup"><span data-stu-id="a39fd-113">For Microsoft 365 Small Business Premium: Sign in to Microsoft 365, and go to **Admin \> Service Settings \> Instant messaging, meetings and conferencing**.</span></span> <span data-ttu-id="a39fd-114">Activez les communications externes.</span><span class="sxs-lookup"><span data-stu-id="a39fd-114">Turn on External communications.</span></span> <span data-ttu-id="a39fd-115">Le commutateur communications externes active les deux Lync-Skype connectivité et les communications avec d’autres organisations qui utilisent Lync.</span><span class="sxs-lookup"><span data-stu-id="a39fd-115">The External communications switch turns on both Lync-Skype connectivity and communications with other organizations that use Lync.</span></span> <span data-ttu-id="a39fd-116">En fonction du moment où vous avez commencé à utiliser Lync Online, le commutateur communications externes dans un état « activé » peut indiquer que seules les communications avec d’autres organisations Lync sont activées.</span><span class="sxs-lookup"><span data-stu-id="a39fd-116">Depending on when you started using Lync Online, the External communications switch in an "on" state may initially indicate only that communications with other Lync organizations is activated.</span></span> <span data-ttu-id="a39fd-117">Pour activer Lync-Skype connectivité, il suffit de basculer entre le commutateur et le basculement.</span><span class="sxs-lookup"><span data-stu-id="a39fd-117">To turn on Lync-Skype Connectivity, simply toggle the switch off and then back on again.</span></span>

<span data-ttu-id="a39fd-118"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a39fd-118"></div>

<span> </span>

</div>

</div>

</span></span></div>

