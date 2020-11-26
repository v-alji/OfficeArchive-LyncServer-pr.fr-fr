---
title: Configuration de Lync Server 2013 pour fonctionner avec Office Web Apps Server
description: Configuration de Lync Server 2013 pour fonctionner avec Office Web Apps Server.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Lync Server 2013 to work with Office Web Apps Server
ms:assetid: 6231e519-9010-4ff9-b5a6-b5859c2b3e11
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204944(v=OCS.15)
ms:contentKeyID: 48184288
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 07e53500e0ad272c81340c25946f5b7f8e72a121
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433011"
---
# <a name="configuring-lync-server-2013-to-work-with-office-web-apps-server"></a><span data-ttu-id="e0e34-103">Configuration de Lync Server 2013 pour fonctionner avec Office Web Apps Server</span><span class="sxs-lookup"><span data-stu-id="e0e34-103">Configuring Lync Server 2013 to work with Office Web Apps Server</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e0e34-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e0e34-104">

<span> </span></span></span>

<span data-ttu-id="e0e34-105">_**Dernière modification de la rubrique :** 2013-04-22_</span><span class="sxs-lookup"><span data-stu-id="e0e34-105">_**Topic Last Modified:** 2013-04-22_</span></span>

<span data-ttu-id="e0e34-106">Pour pouvoir configurer Lync Server 2013 de manière à utiliser Office Web Apps Server, Office Web Apps Server doit être déployé et configuré.</span><span class="sxs-lookup"><span data-stu-id="e0e34-106">Before you can configure Lync Server 2013 to use Office Web Apps Server, Office Web Apps Server must be deployed and configured.</span></span> <span data-ttu-id="e0e34-107">Pour plus d’informations sur l’installation et la configuration d’un serveur Office Web Apps, voir le Guide de mise en route de Office Web Apps Server **et Office** Web Apps pour plus d’informations sur l’installation et la configuration d’une batterie de serveurs Office Web Apps pour une disponibilité élevée.</span><span class="sxs-lookup"><span data-stu-id="e0e34-107">See the document **Guide to Deploying Office Web Apps Server and Office Web Apps** for detail information on how to install and configure a single Office Web Apps Server, or for information on how to install and configure an Office Web Apps Server Farm for high availability.</span></span>

<span data-ttu-id="e0e34-108">Après l’installation réussie d’Office Web Apps Server et la configuration correcte de votre batterie de serveurs Web, vous devez configurer Lync Server pour communiquer avec le nouveau serveur. pour ce faire, ajoutez l’URL de découverte d’Office Web Apps Server à votre topologie de serveur Lync.</span><span class="sxs-lookup"><span data-stu-id="e0e34-108">After Office Web Apps Server has been successfully installed and your Web farm correctly configured, you must then configure Lync Server to communicate with the new server; this is done by adding the Office Web Apps Server discovery URL to your Lync Server topology.</span></span> <span data-ttu-id="e0e34-109">Pour ajouter Office Web Apps Server à votre topologie, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="e0e34-109">To add Office Web Apps Server to your topology, complete the following steps:</span></span>

1.  <span data-ttu-id="e0e34-110">Cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Générateur de topologie de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="e0e34-110">Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>

2.  <span data-ttu-id="e0e34-111">Dans la boîte de dialogue **Générateur de topologies**, sélectionnez **Télécharger la topologie à partir d’un déploiement existant**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="e0e34-111">In the **Topology Builder** dialog box, select **Download Topology from existing deployment** and then click **OK**.</span></span>

3.  <span data-ttu-id="e0e34-p103">Dans la boîte de dialogue **Enregistrer la topologie sous**, tapez le nom de votre document de topologie (par exemple, **PreWebAppsServerTopology**) dans la zone \**Nom du fichier\**, puis cliquez sur **Enregistrer**. Vous pouvez par la suite extraire et republier cette topologie si vous rencontrez des problèmes avec votre nouvelle topologie.</span><span class="sxs-lookup"><span data-stu-id="e0e34-p103">In the **Save Topology As** dialog box, type a name for your topology document (for example, **PreWebAppsServerTopology**) in the **File name** box and then click **Save**. This topology can later be retrieved and republished if you encounter problems with your new topology.</span></span>

4.  <span data-ttu-id="e0e34-114">Dans le générateur de topologie, développez **Lync Server 2013**, développez le nom de votre site, développez **Pools front end Enterprise Edition**, cliquez avec le bouton droit sur le nom de l’un de vos pools, puis cliquez sur **modifier les propriétés**.</span><span class="sxs-lookup"><span data-stu-id="e0e34-114">In Topology Builder, expand **Lync Server 2013**, expand the name of your site, expand **Enterprise Edition Front End pools**, right-click the name of one of your pools, and then click **Edit Properties**.</span></span>

5.  <span data-ttu-id="e0e34-115">Dans la boîte de dialogue **Modifier les propriétés**, sous l’onglet **Général**, recherchez l’en-tête **Serveur Office Web Apps associé**, puis cliquez sur **Nouveau** (ou sélectionnez un serveur Office Web Apps Server existant dans la liste déroulante).</span><span class="sxs-lookup"><span data-stu-id="e0e34-115">In the **Edit Properties** dialog box, on the **General** tab, find the heading **Associate Office Web Apps Server** and then click **New** (or select an existing Office Web Apps Server from the drop-down list).</span></span>

6.  <span data-ttu-id="e0e34-116">Dans la boîte de dialogue **Définir un nouveau serveur Office Web Apps**, tapez le nom de domaine complet de votre ordinateur Office Web Apps Server dans la zone **Nom de domaine complet du serveur Office Web Apps**. L’URL de découverte du serveur Office Web Apps Server est alors automatiquement entrée dans la zone **URL de découverte du serveur Office Web Apps**.</span><span class="sxs-lookup"><span data-stu-id="e0e34-116">In the **Define New Office Web Apps Server** dialog box, type the fully qualified domain name (FQDN) of your Office Web Apps Server computer in the **Office Web Apps Server FQDN** box; when you do this, your Office Web Apps Server discovery URL should automatically be entered into the **Office Web Apps Server discovery URL** box.</span></span>
    
    <span data-ttu-id="e0e34-117">Si Office Web Apps Server est installé en local et dans la même zone réseau que Lync Server 2013, l’option **Office Web Apps Server déployée sur un réseau externe (c’est-à-dire le périmètre/Internet)** ne doit pas être sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="e0e34-117">If the Office Web Apps Server is installed on-premises and in the same network zone as Lync Server 2013 then the option **Office Web Apps Server is deployed in an external network (that is, perimeter/Internet)** should not be selected.</span></span>
    
    <span data-ttu-id="e0e34-118">Si le serveur Office Web Apps Server est déployé à l’extérieur de votre pare-feu interne, sélectionnez alors l’option **Le serveur Office Web Apps est déployé sur un réseau externe (périmètre/Internet)**.</span><span class="sxs-lookup"><span data-stu-id="e0e34-118">If the Office Web Apps Server is deployed outside your internal firewall, then select the option **Office Web Apps Server is deployed in an external network (that is, perimeter/Internet)**.</span></span>

7.  <span data-ttu-id="e0e34-119">Dans la boîte de dialogue **définir un nouveau serveur Office Web Apps** , cliquez sur **OK**, puis sur **OK** dans la boîte de dialogue **modifier les propriétés** .</span><span class="sxs-lookup"><span data-stu-id="e0e34-119">In the **Define New Office Web Apps Server** dialog box, click **OK**, and then click **OK** in the **Edit Properties** dialog box.</span></span> <span data-ttu-id="e0e34-120">L’URL de découverte d’Office Web Apps figure alors sous la forme d’une des associations du pool.</span><span class="sxs-lookup"><span data-stu-id="e0e34-120">The Office Web Apps discovery URL will then be listed as one of the pool's Associations.</span></span>

<span data-ttu-id="e0e34-121">Vous devez répéter ce processus pour chaque pool à associer à votre serveur Office Web Apps Server.</span><span class="sxs-lookup"><span data-stu-id="e0e34-121">You will have to repeat this process for each pool that needs to be associated with your Office Web Apps Server.</span></span>

<span data-ttu-id="e0e34-122">Après avoir ajouté l’URL de découverte à la topologie, vous devez publier cette topologie mise à jour.</span><span class="sxs-lookup"><span data-stu-id="e0e34-122">After you have added the discovery URL to the topology you must then publish this updated topology.</span></span> <span data-ttu-id="e0e34-123">Pour cela, dans le Générateur de topologie :</span><span class="sxs-lookup"><span data-stu-id="e0e34-123">To do that in Topology Builder:</span></span>

1.  <span data-ttu-id="e0e34-124">Cliquez sur **Action**, puis sur **Publier la topologie**.</span><span class="sxs-lookup"><span data-stu-id="e0e34-124">Click **Action** and then click **Publish Topology**.</span></span>

2.  <span data-ttu-id="e0e34-125">Dans l’Assistant Publication de la topologie, dans la page **Publier la topologie**, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="e0e34-125">In the Publish Topology wizard, on the **Publish the Topology** page, click **Next**.</span></span>

3.  <span data-ttu-id="e0e34-126">Dans la page **Assistant Publication terminé**, cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="e0e34-126">On the **Publishing wizard complete** page, click **Finish**.</span></span>

4.  <span data-ttu-id="e0e34-127">Fermez le Générateur de topologie.</span><span class="sxs-lookup"><span data-stu-id="e0e34-127">Close Topology Builder.</span></span>

<span data-ttu-id="e0e34-128"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e0e34-128"></div>

<span> </span>

</div>

</div>

</span></span></div>

