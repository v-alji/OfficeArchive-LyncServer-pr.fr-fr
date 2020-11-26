---
title: Définition et configuration d’un pool frontal ou d’un serveur Standard Edition
description: Définissez et configurez une réserve frontale ou un serveur Standard Edition Server.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Define and configure a Front End pool or Standard Edition server
ms:assetid: 713fc263-23dd-414a-b001-82932e4fe966
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398538(v=OCS.15)
ms:contentKeyID: 48184457
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fd632564f0a5afd1f899ee8487f633c4685d12a7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431070"
---
# <a name="define-and-configure-a-front-end-pool-or-standard-edition-server-in-lync-server-2013"></a><span data-ttu-id="5fed2-103">Définition et configuration d’un pool frontal ou d’un serveur Standard Edition dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5fed2-103">Define and configure a Front End pool or Standard Edition server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5fed2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5fed2-104">

<span> </span></span></span>

<span data-ttu-id="5fed2-105">_**Dernière modification de la rubrique :** 2013-03-08_</span><span class="sxs-lookup"><span data-stu-id="5fed2-105">_**Topic Last Modified:** 2013-03-08_</span></span>

<span data-ttu-id="5fed2-106">Cette procédure ne nécessite pas d’appartenance à un administrateur local ou à un groupe de domaines privilégiés.</span><span class="sxs-lookup"><span data-stu-id="5fed2-106">This procedure does not require membership in a local administrator or privileged domain group.</span></span> <span data-ttu-id="5fed2-107">Vous devez vous connecter à un ordinateur en tant qu’utilisateur standard.</span><span class="sxs-lookup"><span data-stu-id="5fed2-107">You should log on to a computer as a standard user.</span></span>

<span data-ttu-id="5fed2-108">Si vous déployez un serveur d’entreprise, un nombre minimum de serveurs frontaux dans un pool doit être en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="5fed2-108">If you are deploying an Enterprise server, a minimum number of Front End Servers in a pool must be running at all times.</span></span> <span data-ttu-id="5fed2-109">Le tableau suivant récapitule ces exigences.</span><span class="sxs-lookup"><span data-stu-id="5fed2-109">The following table summarizes these requirements.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5fed2-110">Nombre total de serveurs frontaux de la liste</span><span class="sxs-lookup"><span data-stu-id="5fed2-110">Total number of Front End Servers in the pool</span></span></th>
<th><span data-ttu-id="5fed2-111">Nombre de serveurs devant être exécutés pour que le pool soit opérationnel</span><span class="sxs-lookup"><span data-stu-id="5fed2-111">Number of servers that must be running for pool to be functional</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5fed2-112">1-2</span><span class="sxs-lookup"><span data-stu-id="5fed2-112">1-2</span></span></p></td>
<td><p><span data-ttu-id="5fed2-113">1</span><span class="sxs-lookup"><span data-stu-id="5fed2-113">1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5fed2-114">3-4</span><span class="sxs-lookup"><span data-stu-id="5fed2-114">3-4</span></span></p></td>
<td><p><span data-ttu-id="5fed2-115">2</span><span class="sxs-lookup"><span data-stu-id="5fed2-115">2</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5fed2-116">5-6</span><span class="sxs-lookup"><span data-stu-id="5fed2-116">5-6</span></span></p></td>
<td><p><span data-ttu-id="5fed2-117">3</span><span class="sxs-lookup"><span data-stu-id="5fed2-117">3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5fed2-118">7-8</span><span class="sxs-lookup"><span data-stu-id="5fed2-118">7-8</span></span></p></td>
<td><p><span data-ttu-id="5fed2-119">4</span><span class="sxs-lookup"><span data-stu-id="5fed2-119">4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5fed2-120">9-10</span><span class="sxs-lookup"><span data-stu-id="5fed2-120">9-10</span></span></p></td>
<td><p><span data-ttu-id="5fed2-121">5</span><span class="sxs-lookup"><span data-stu-id="5fed2-121">5</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5fed2-122">11-12</span><span class="sxs-lookup"><span data-stu-id="5fed2-122">11-12</span></span></p></td>
<td><p><span data-ttu-id="5fed2-123">6</span><span class="sxs-lookup"><span data-stu-id="5fed2-123">6</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]
> <span data-ttu-id="5fed2-124">Pour Lync Server 2013, chaque fois que vous ajoutez ou supprimez un serveur frontal de la liste, vous devez redémarrer les services.</span><span class="sxs-lookup"><span data-stu-id="5fed2-124">For Lync Server 2013, any time you add or remove a Front End Server from the pool, you must restart services.</span></span> <span data-ttu-id="5fed2-125">La suppression et l’ajout de serveurs doivent être effectuées en tant qu’opérations séparées.</span><span class="sxs-lookup"><span data-stu-id="5fed2-125">Removing and adding servers should be done as separate operations.</span></span> <span data-ttu-id="5fed2-126">Par exemple, si vous envisagez d’ajouter deux serveurs frontaux et de supprimer deux serveurs frontaux, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="5fed2-126">For example, if you are going to add two Front End Servers and remove two Front End Servers, use the following process:</span></span> 
> <OL>
> <LI>
> <P><span data-ttu-id="5fed2-127">Supprimez les deux serveurs frontaux.</span><span class="sxs-lookup"><span data-stu-id="5fed2-127">Remove the two Front End Servers.</span></span></P>
> <LI>
> <P><span data-ttu-id="5fed2-128">Publiez et réactivez la topologie.</span><span class="sxs-lookup"><span data-stu-id="5fed2-128">Publish and re-activate the topology.</span></span></P>
> <LI>
> <P><span data-ttu-id="5fed2-129">Redémarrer les services</span><span class="sxs-lookup"><span data-stu-id="5fed2-129">Restart the services</span></span></P>
> <LI>
> <P><span data-ttu-id="5fed2-130">Ajoutez les deux serveurs front-end.</span><span class="sxs-lookup"><span data-stu-id="5fed2-130">Add the two Front End Servers.</span></span></P>
> <LI>
> <P><span data-ttu-id="5fed2-131">Publiez et réactivez la topologie.</span><span class="sxs-lookup"><span data-stu-id="5fed2-131">Publish and re-activate the topology.</span></span></P>
> <LI>
> <P><span data-ttu-id="5fed2-132">Redémarrez les services.</span><span class="sxs-lookup"><span data-stu-id="5fed2-132">Restart the services.</span></span></P></LI></OL>



</div>

<span data-ttu-id="5fed2-133">Après avoir défini votre topologie, utilisez la procédure suivante pour définir un pool frontal pour votre site.</span><span class="sxs-lookup"><span data-stu-id="5fed2-133">After you have defined your topology, use the following procedure to define a Front End pool for your site.</span></span> <span data-ttu-id="5fed2-134">Pour plus d’informations sur la définition de la topologie, voir [définir et configurer une topologie dans le générateur de topologies pour Lync Server 2013](lync-server-2013-define-and-configure-a-topology-in-topology-builder.md).</span><span class="sxs-lookup"><span data-stu-id="5fed2-134">For details about defining the topology, see [Define and configure a topology in Topology Builder for Lync Server 2013](lync-server-2013-define-and-configure-a-topology-in-topology-builder.md).</span></span>

<div>

## <a name="to-define-a-front-end-pool"></a><span data-ttu-id="5fed2-135">Pour définir un pool frontal</span><span class="sxs-lookup"><span data-stu-id="5fed2-135">To define a Front End pool</span></span>

1.  <span data-ttu-id="5fed2-136">Dans l’Assistant définir un nouveau pool frontal, dans la page **définir le nouveau pool frontal** , cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="5fed2-136">In the Define New Front End Pool Wizard, on the **Define the New Front End pool** page, click **Next**.</span></span>

2.  <span data-ttu-id="5fed2-137">Dans la page **définir le nom de domaine complet du pool frontal** , entrez un nom de domaine complet (FQDN) pour le pool que vous êtes en train de créer, puis **cliquez** sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="5fed2-137">On the **Define the Front End pool FQDN** page, enter a fully qualified domain name (FQDN) for the pool you are creating, click **Enterprise Edition Front End pool**, and then click **Next**.</span></span>

3.  <span data-ttu-id="5fed2-138">Dans la page **définir les ordinateurs de ce pool** , entrez un nom de domaine complet pour le premier serveur frontal de la liste, puis cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="5fed2-138">On the **Define the computers in this pool** page, enter a computer FQDN for the first Front End Server in the pool, and then click **Add**.</span></span> <span data-ttu-id="5fed2-139">Répétez cette étape pour tous les ordinateurs que vous voulez ajouter à la liste, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="5fed2-139">Repeat this step for any additional computers (up to twelve) that you want to add to the pool, and then click **Next**.</span></span>

4.  <span data-ttu-id="5fed2-140">Dans la page **Sélectionner des fonctionnalités** , activez les cases à cocher des fonctionnalités que vous voulez inclure dans ce pool frontal.</span><span class="sxs-lookup"><span data-stu-id="5fed2-140">On the **Select features** page, select the check boxes for the features that you want on this Front End pool.</span></span> <span data-ttu-id="5fed2-141">Par exemple, si vous déployez uniquement les fonctionnalités de messagerie instantanée et de présence, activez la case à cocher **Conférence** pour autoriser la messagerie instantanée à plusieurs éléments, mais sans sélectionner les cases à cocher Conférence rendez **-vous (RTC)**, **voix entreprise** ou **contrôle d’admission des appels** , car elles représentent les fonctionnalités de voix, de vidéo et de conférence de collaboration.</span><span class="sxs-lookup"><span data-stu-id="5fed2-141">For example, if you are deploying only instant messaging (IM) and presence features, you would select the **Conferencing** check box to allow multiparty IM but would not select the **Dial-in (PSTN) conferencing**, **Enterprise Voice**, or **Call Admission Control** check boxes, because they represent voice, video, and collaborative conferencing features.</span></span>
    
      - <span data-ttu-id="5fed2-142">**Conférences**   téléphoniques   Cette sélection permet d’obtenir une gamme étendue de fonctionnalités, notamment :</span><span class="sxs-lookup"><span data-stu-id="5fed2-142">**Conferencing**   This selection enables a rich set of features including:</span></span>
        
          - <span data-ttu-id="5fed2-143">Messagerie instantanée avec plus de deux parties dans une session de messagerie instantanée.</span><span class="sxs-lookup"><span data-stu-id="5fed2-143">IM with more than two parties in an IM session.</span></span>
        
          - <span data-ttu-id="5fed2-144">Conférences, qui comprennent la collaboration sur des documents, le partage d’application et le partage de bureau.</span><span class="sxs-lookup"><span data-stu-id="5fed2-144">Conferencing, which includes document collaboration, application sharing, and desktop sharing.</span></span>
        
          - <span data-ttu-id="5fed2-145">Une conférence a/V, qui permet aux utilisateurs d’effectuer des conférences audio/vidéo (A/V) en temps réel sans recourir à des services externes tels que le service Live Meeting ou un pont audio tiers.</span><span class="sxs-lookup"><span data-stu-id="5fed2-145">A/V conferencing, which enables users to have real-time audio/video (A/V) conferences without the need for external services such as the Live Meeting service or a third-party audio bridge.</span></span>
    
      - <span data-ttu-id="5fed2-146">**Conférence rendez-vous (RTC)**   Permet aux utilisateurs d’accéder à la partie audio d’une conférence 2013 Server Lync à l’aide d’un téléphone RTC (réseau téléphonique commuté) sans nécessiter un fournisseur de services d’audioconférence.</span><span class="sxs-lookup"><span data-stu-id="5fed2-146">**Dial-in (PSTN) conferencing**   Allows users to join the audio portion of a Lync Server 2013 conference by using a public switched telephone network (PSTN) phone without requiring an audio conferencing provider.</span></span>
    
      - <span data-ttu-id="5fed2-147">**Voix entreprise**   Enterprise Voice est la solution de voix sur IP (VoIP) dans Lync Server 2013, qui permet aux utilisateurs de passer et de recevoir des appels téléphoniques.</span><span class="sxs-lookup"><span data-stu-id="5fed2-147">**Enterprise Voice**   Enterprise Voice is the Voice over IP (VoIP) solution in Lync Server 2013 that allows users to make and receive phone calls.</span></span> <span data-ttu-id="5fed2-148">Vous déploierez cette fonctionnalité si vous envisagez d’utiliser Lync Server 2013 pour les appels vocaux, la messagerie vocale et d’autres fonctions qui utilisent un appareil matériel ou un client logiciel.</span><span class="sxs-lookup"><span data-stu-id="5fed2-148">You would deploy this feature if you plan to use Lync Server 2013 for voice calls, voice mail, and other functions that use a hardware device or a software client.</span></span>
    
      - <span data-ttu-id="5fed2-149">**Contrôle d’admission des appels (CAC)**   Le CAC détermine, en fonction de la bande passante disponible du réseau, s’il est possible d’établir des sessions de communication en temps réel telles que des appels vocaux ou vidéo.</span><span class="sxs-lookup"><span data-stu-id="5fed2-149">**Call admission control (CAC)**   CAC determines, based on available network bandwidth, whether to allow real-time communications sessions such as voice or video calls to be established.</span></span> <span data-ttu-id="5fed2-150">Si vous avez déployé uniquement la messagerie instantanée et la présence, CAC n’est pas nécessaire, car aucune de ces deux fonctionnalités n’utilise le CAC.</span><span class="sxs-lookup"><span data-stu-id="5fed2-150">If you have deployed only IM and presence, CAC is not needed because neither of these two features uses CAC.</span></span>
    
      - <span data-ttu-id="5fed2-151">**Archivage**   L’archivage vous permet d’archiver le contenu des messages instantanés, le contenu de la réunion ou les deux envoyés par le biais de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="5fed2-151">**Archiving**   Archiving provides a way for you to archive IM content, conferencing (meeting) content, or both that is sent through Lync Server 2013.</span></span>
    
      - <span data-ttu-id="5fed2-152">**Surveiller**   Monitoring Server vous permet de collecter des données numériques qui décrivent la qualité multimédia sur votre réseau et vos points de terminaison, des informations sur l’utilisation des appels VoIP, des messages INSTANTANÉs, des conversations A/V, des réunions, du partage d’application et des transferts de fichiers, et des erreurs d’appel et de résolution des problèmes pour les appels en échec.</span><span class="sxs-lookup"><span data-stu-id="5fed2-152">**Monitoring**   Monitoring Server enables you to collect numerical data that describes the media quality on your network and endpoints, usage information related to VoIP calls, IM messages, A/V conversations, meetings, application sharing, and file transfers, and call error and troubleshooting information for failed calls.</span></span>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="5fed2-153">Si vous voulez activer le CAC dans votre déploiement, il est nécessaire d’activer le service CAC dans exactement un pool par site central.</span><span class="sxs-lookup"><span data-stu-id="5fed2-153">If you would like to enable CAC in your deployment, it is required that you enable CAC in exactly one pool per central site.</span></span> <span data-ttu-id="5fed2-154">Le CAC est recommandé si vous déployez des fonctions vocales ou des conférences A/V.</span><span class="sxs-lookup"><span data-stu-id="5fed2-154">CAC is recommended if you are deploying voice features or A/V conferencing.</span></span>

    
    </div>
    
    <span data-ttu-id="5fed2-155">Le tableau suivant répertorie les fonctionnalités disponibles (haut) et les fonctions proposées aux utilisateurs (à gauche).</span><span class="sxs-lookup"><span data-stu-id="5fed2-155">The following table shows the available features (top) and the functions offered to users (left).</span></span> <span data-ttu-id="5fed2-156">Les sélections du tableau sont celles que vous devez sélectionner pour activer ces fonctionnalités pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="5fed2-156">The selections in the table are what you should select to enable those features for your organization.</span></span>
    
    
    <table>
    <colgroup>
    <col style="width: 20%" />
    <col style="width: 20%" />
    <col style="width: 20%" />
    <col style="width: 20%" />
    <col style="width: 20%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th></th>
    <th><span data-ttu-id="5fed2-157">Conférence</span><span class="sxs-lookup"><span data-stu-id="5fed2-157">Conferencing</span></span></th>
    <th><span data-ttu-id="5fed2-158">Conférence rendez-vous</span><span class="sxs-lookup"><span data-stu-id="5fed2-158">Dial-In Conferencing</span></span></th>
    <th><span data-ttu-id="5fed2-159">Voix Entreprise</span><span class="sxs-lookup"><span data-stu-id="5fed2-159">Enterprise Voice</span></span></th>
    <th><span data-ttu-id="5fed2-160">Contrôle d’admission des appels</span><span class="sxs-lookup"><span data-stu-id="5fed2-160">Call Admission Control</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="5fed2-161">Messagerie instantanée et présence</span><span class="sxs-lookup"><span data-stu-id="5fed2-161">Instant messaging and presence</span></span></p></td>
    <td><p><span data-ttu-id="5fed2-162">X</span><span class="sxs-lookup"><span data-stu-id="5fed2-162">X</span></span></p></td>
    <td></td>
    <td></td>
    <td></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="5fed2-163">Conférence</span><span class="sxs-lookup"><span data-stu-id="5fed2-163">Conferencing</span></span></p></td>
    <td><p><span data-ttu-id="5fed2-164">X</span><span class="sxs-lookup"><span data-stu-id="5fed2-164">X</span></span></p></td>
    <td><p><span data-ttu-id="5fed2-165">X</span><span class="sxs-lookup"><span data-stu-id="5fed2-165">X</span></span></p></td>
    <td></td>
    <td></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="5fed2-166">Conférence A/V</span><span class="sxs-lookup"><span data-stu-id="5fed2-166">A/V conferencing</span></span></p></td>
    <td><p><span data-ttu-id="5fed2-167">X</span><span class="sxs-lookup"><span data-stu-id="5fed2-167">X</span></span></p></td>
    <td><p><span data-ttu-id="5fed2-168">X</span><span class="sxs-lookup"><span data-stu-id="5fed2-168">X</span></span></p></td>
    <td></td>
    <td><p><span data-ttu-id="5fed2-169">X</span><span class="sxs-lookup"><span data-stu-id="5fed2-169">X</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="5fed2-170">Voix Entreprise</span><span class="sxs-lookup"><span data-stu-id="5fed2-170">Enterprise Voice</span></span></p></td>
    <td></td>
    <td></td>
    <td><p><span data-ttu-id="5fed2-171">X</span><span class="sxs-lookup"><span data-stu-id="5fed2-171">X</span></span></p></td>
    <td><p><span data-ttu-id="5fed2-172">X</span><span class="sxs-lookup"><span data-stu-id="5fed2-172">X</span></span></p></td>
    </tr>
    </tbody>
    </table>


5.  <span data-ttu-id="5fed2-173">Dans la page **Sélectionner des rôles de serveur colocalisés** , vous pouvez Collocate le serveur de médiation sur le serveur frontal ou le déployer en tant que serveur autonome.</span><span class="sxs-lookup"><span data-stu-id="5fed2-173">On the **Select collocated server roles** page, you can to collocate the Mediation Server on the Front End Server or to deploy it as a stand-alone server.</span></span>
    
    <span data-ttu-id="5fed2-174">Vous pouvez collocate le serveur de médiation sur le pool frontal.</span><span class="sxs-lookup"><span data-stu-id="5fed2-174">You can collocate the Mediation Server on the Front End pool.</span></span>
    
      - <span data-ttu-id="5fed2-175">Si vous envisagez de collocate le serveur de médiation sur le pool frontal Enterprise Edition, assurez-vous que la case à cocher est activée.</span><span class="sxs-lookup"><span data-stu-id="5fed2-175">If you intend to collocate the Mediation Server on the Enterprise Edition Front End pool, ensure the check box is selected.</span></span> <span data-ttu-id="5fed2-176">Le rôle serveur sera déployé sur les serveurs du pool.</span><span class="sxs-lookup"><span data-stu-id="5fed2-176">The server role will be deployed on the pool servers.</span></span>
    
      - <span data-ttu-id="5fed2-177">Si vous envisagez de déployer le serveur de médiation en tant que serveur autonome, décochez la case correspondante.</span><span class="sxs-lookup"><span data-stu-id="5fed2-177">If you intend to deploy the Mediation Server as a stand-alone server, clear the appropriate check box.</span></span> <span data-ttu-id="5fed2-178">Vous déploierez le serveur de médiation dans une étape de déploiement séparée après le déploiement complet du serveur frontal.</span><span class="sxs-lookup"><span data-stu-id="5fed2-178">You will deploy Mediation Server in a separate deployment step after you completely deploy the Front End Server.</span></span>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="5fed2-179">Nous vous recommandons de collocate le serveur de médiation, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="5fed2-179">We recommend that you collocate the Mediation Server if possible.</span></span> <span data-ttu-id="5fed2-180">Pour plus d’informations sur la prise en charge des serveurs de médiation autonomes ou autonomes, voir <A href="lync-server-2013-components-and-topologies-for-mediation-server.md">composants et topologies du serveur de médiation dans Lync Server 2013</A> dans la documentation de planification.</span><span class="sxs-lookup"><span data-stu-id="5fed2-180">For details about support for collocated or stand-alone Mediation Servers, see <A href="lync-server-2013-components-and-topologies-for-mediation-server.md">Components and topologies for Mediation Server in Lync Server 2013</A> in the Planning documentation.</span></span>

    
    </div>

6.  <span data-ttu-id="5fed2-181">Les **rôles serveur Associate avec cette page de pool frontal** vous permettent de définir et d’associer des rôles de serveur avec le pool frontal.</span><span class="sxs-lookup"><span data-stu-id="5fed2-181">The **Associate server roles with this Front End pool** page lets you define and associate server roles with the Front End pool.</span></span> <span data-ttu-id="5fed2-182">Le rôle suivant est disponible :</span><span class="sxs-lookup"><span data-stu-id="5fed2-182">The following role is available:</span></span>
    
    <span data-ttu-id="5fed2-183">**Activer un pool de bords**   Définit et associe un serveur Edge unique ou un pool de serveurs Edge.</span><span class="sxs-lookup"><span data-stu-id="5fed2-183">**Enable an Edge pool**   Defines and associates a single Edge Server or a pool of Edge Servers.</span></span> <span data-ttu-id="5fed2-184">Un serveur Edge facilite la communication et la collaboration entre les utilisateurs au sein de l’organisation et les personnes qui travaillent en dehors de celle-ci, notamment les utilisateurs fédérés.</span><span class="sxs-lookup"><span data-stu-id="5fed2-184">An Edge Server facilitates communication and collaboration between users inside the organization and people outside the organization, including federated users.</span></span>
    
    <span data-ttu-id="5fed2-185">Vous pouvez utiliser deux scénarios possibles pour déployer et associer les rôles de serveur :</span><span class="sxs-lookup"><span data-stu-id="5fed2-185">There are two possible scenarios that you can use to deploy and associate the server roles:</span></span>
    
    <span data-ttu-id="5fed2-186">Dans le premier scénario, vous définissez une nouvelle topologie pour une nouvelle installation.</span><span class="sxs-lookup"><span data-stu-id="5fed2-186">For scenario one, you are defining a new topology for a new installation.</span></span> <span data-ttu-id="5fed2-187">Vous pouvez aborder l’installation de deux manières :</span><span class="sxs-lookup"><span data-stu-id="5fed2-187">You can approach the installation in one of two ways:</span></span>
    
      - <span data-ttu-id="5fed2-188">Laissez la case à cocher désactivée et continuez de définir la topologie.</span><span class="sxs-lookup"><span data-stu-id="5fed2-188">Leave the check box clear and proceed with defining the topology.</span></span> <span data-ttu-id="5fed2-189">Une fois les rôles serveur frontal et principal publiés, configurés et testés, vous pouvez réexécuter le Générateur de topologies afin de les ajouter à la topologie.</span><span class="sxs-lookup"><span data-stu-id="5fed2-189">After you have published, configured, and tested the Front End and Back End Server roles, you can run Topology Builder again to add the role servers to the topology.</span></span> <span data-ttu-id="5fed2-190">Cette stratégie vous permet de tester le pool frontal et le serveur exécutant SQL Server sans complications supplémentaires provenant de rôles supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="5fed2-190">This strategy will enable you to test the Front End pool and the server running SQL Server without additional complications from additional roles.</span></span> <span data-ttu-id="5fed2-191">Une fois les tests initiaux réalisés, vous pouvez réexécuter le Générateur de topologies afin de sélectionner les rôles à déployer.</span><span class="sxs-lookup"><span data-stu-id="5fed2-191">After you have completed your initial testing, you can run Topology Builder again to select the roles you need to deploy.</span></span>
    
      - <span data-ttu-id="5fed2-192">Sélectionnez les rôles à installer, puis configurez le matériel en fonction des rôles sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="5fed2-192">Select roles that you need to install, and then set up the hardware to accommodate the selected roles.</span></span>
    
    <span data-ttu-id="5fed2-193">Dans le scénario 2, vous disposez d’un déploiement existant et votre infrastructure est prête pour de nouveaux rôles ou vous devez associer des rôles existants à un nouveau serveur frontal :</span><span class="sxs-lookup"><span data-stu-id="5fed2-193">For scenario two, you have an existing deployment and your infrastructure is ready for new roles or you need to associate existing roles with a new Front End Server:</span></span>
    
      - <span data-ttu-id="5fed2-194">Dans ce cas, vous devez sélectionner les rôles que vous souhaitez déployer ou associer au nouveau serveur frontal.</span><span class="sxs-lookup"><span data-stu-id="5fed2-194">In this case, you will select the roles that you intend to deploy or associate with the new Front End Server.</span></span> <span data-ttu-id="5fed2-195">Dans les deux cas, vous devez définir les rôles, configurer le matériel nécessaire et effectuer l’installation.</span><span class="sxs-lookup"><span data-stu-id="5fed2-195">In either case, you will proceed with the definition of the roles, set up any needed hardware, and proceed with the installation.</span></span>

7.  <span data-ttu-id="5fed2-196">Dans la page **définir le SQL Store** , effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="5fed2-196">On the **Define the SQL store** page, do one of the following:</span></span>
    
      - <span data-ttu-id="5fed2-197">Pour utiliser un magasin SQL Server qui a déjà été défini dans votre topologie, sélectionnez une instance dans **Magasin SQL**.</span><span class="sxs-lookup"><span data-stu-id="5fed2-197">To use an existing SQL Server store that has already been defined in your topology, select an instance from **SQL store**.</span></span>
    
      - <span data-ttu-id="5fed2-198">Pour définir une nouvelle instance SQL Server pour stocker des informations de pool, cliquez sur **nouveau** , puis spécifiez le **nom de domaine complet SQL Server** dans la boîte de dialogue **définir un nouveau SQL Store** .</span><span class="sxs-lookup"><span data-stu-id="5fed2-198">To define a new SQL Server instance to store pool information, click **New** and then specify the **SQL Server FQDN** in the **Define New SQL Store** dialog box.</span></span>
    
      - <span data-ttu-id="5fed2-199">Pour spécifier le nom d’une instance SQL Server, sélectionnez **Instance nommée**, puis spécifiez le nom de l’instance.</span><span class="sxs-lookup"><span data-stu-id="5fed2-199">To specify the name of a SQL Server instance, select **Named Instance**, and then specify the name of the instance.</span></span>
    
      - <span data-ttu-id="5fed2-200">Pour utiliser l’instance par défaut, cliquez sur **Instance par défaut**.</span><span class="sxs-lookup"><span data-stu-id="5fed2-200">To use the default instance, click **Default instance**.</span></span>
    
      - <span data-ttu-id="5fed2-201">Pour utiliser la mise en miroir SQL, sélectionnez **activer la mise en miroir SQL** et sélectionnez une instance existante ou créez une nouvelle instance.</span><span class="sxs-lookup"><span data-stu-id="5fed2-201">To use SQL Mirroring, select **Enable SQL mirroring** and select an existing instance or create a new instance.</span></span>

8.  <span data-ttu-id="5fed2-202">Dans la page **définir le partage de fichiers** , effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="5fed2-202">On the **Define the file share** page, do one of the following:</span></span>
    
      - <span data-ttu-id="5fed2-203">Pour utiliser un partage de fichiers qui a déjà été défini dans votre topologie, sélectionnez **Utiliser un partage de fichiers précédemment défini**.</span><span class="sxs-lookup"><span data-stu-id="5fed2-203">To use a file share that has already been defined in your topology, select **Use a previously defined file share**.</span></span>
    
      - <span data-ttu-id="5fed2-204">Pour définir un nouveau partage de fichiers, sélectionnez **Définir un nouveau partage de fichiers**. Dans la zone **Nom de domaine complet du serveur de fichiers**, entrez le nom de domaine complet (FQDN) du serveur de fichiers existant où le partage de fichiers doit être placé, puis entrez un nom pour le partage de fichiers dans la zone **Partage de fichiers**.</span><span class="sxs-lookup"><span data-stu-id="5fed2-204">To define a new file share, select **Define a new file share**, in the **File Server FQDN** box, enter the FQDN of the existing file server where the file share is to reside, and then enter a name for the file share in the **File Share** box.</span></span>
    
    <div>
    

    > [!IMPORTANT]
    > <span data-ttu-id="5fed2-205">Le partage de fichiers pour Lync Server 2013 ne se trouve pas sur le serveur frontal.</span><span class="sxs-lookup"><span data-stu-id="5fed2-205">The file share for Lync Server 2013 cannot be located on the Front End Server.</span></span> <span data-ttu-id="5fed2-206">Notez que dans cet exemple, le partage de fichiers a été localisé sur le serveur principal SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5fed2-206">Note that in this example, the file share has been located on the SQL Server-based Back End Server.</span></span> <span data-ttu-id="5fed2-207">Il est possible qu’il ne s’agit pas d’un emplacement optimal pour les besoins de votre organisation, et qu’un serveur de fichiers soit un meilleur choix.</span><span class="sxs-lookup"><span data-stu-id="5fed2-207">This might not be an optimal location for your organization’s requirements, and a file server might be a better choice.</span></span> <span data-ttu-id="5fed2-208">Vous pouvez définir le partage de fichiers sans avoir à le créer.</span><span class="sxs-lookup"><span data-stu-id="5fed2-208">You can define the file share without the file share having been created.</span></span> <span data-ttu-id="5fed2-209">Vous devrez créer le partage de fichiers à l’emplacement défini avant de publier la topologie.</span><span class="sxs-lookup"><span data-stu-id="5fed2-209">You will need to create the file share in the location you define before you publish the topology.</span></span>

    
    </div>

9.  <span data-ttu-id="5fed2-210">Dans la page **spécifier l’URL du service Web** , effectuez l’une des opérations suivantes ou les deux :</span><span class="sxs-lookup"><span data-stu-id="5fed2-210">On the **Specify the Web Services URL** page, do one or both of the following:</span></span>
    
    <div>
    

    > [!IMPORTANT]
    > <span data-ttu-id="5fed2-211">L’URL de base correspond à l’identité des services web pour l’URL, moins https://.</span><span class="sxs-lookup"><span data-stu-id="5fed2-211">The base URL is the Web Services identity for the URL, minus the https://.</span></span> <span data-ttu-id="5fed2-212">Par exemple, si l’URL complète des services Web du pool est https://pool01.contoso.net , l’URL de base est pool01.contoso.net.</span><span class="sxs-lookup"><span data-stu-id="5fed2-212">For example, if the full URL for the Web Services of the pool is https://pool01.contoso.net, the base URL is pool01.contoso.net.</span></span>

    
    </div>
    
    <div>
    

    > [!WARNING]
    > <span data-ttu-id="5fed2-213">Si vous avez plusieurs pools frontal ou serveur principal, le nom de domaine complet des services Web externes doit être unique.</span><span class="sxs-lookup"><span data-stu-id="5fed2-213">If you have more than one Front End pool or Front End Server, the external Web services FQDN must be unique.</span></span> <span data-ttu-id="5fed2-214">Par exemple, si vous définissez le nom de domaine complet des services Web externes d’un serveur frontal en tant que <STRONG>pool01.contoso.com</STRONG>, vous ne pouvez pas utiliser <STRONG>pool01.contoso.com</STRONG> pour un autre pool frontal ou serveur frontal.</span><span class="sxs-lookup"><span data-stu-id="5fed2-214">For example, if you define the external Web services FQDN of a Front End Server as <STRONG>pool01.contoso.com</STRONG>, you cannot use <STRONG>pool01.contoso.com</STRONG> for another Front End pool or Front End Server.</span></span>

    
    </div>
    
    1.  <span data-ttu-id="5fed2-215">Si vous configurez l’équilibrage de charge DNS, activez la case à cocher **remplacer le FQDN du pool de services Web interne** , entrez l’URL de base interne (qui doit être différente de celle du pool de nom de domaine complet (par exemple, Internal- \<your base URL\> ) dans l' **URL de base interne**.</span><span class="sxs-lookup"><span data-stu-id="5fed2-215">If you are configuring DNS load balancing, select the **Override internal Web Services pool FQDN** check box, enter the internal base URL (which must be different from the pool FQDN and could be, for example, internal-\<your base URL\>) in **Internal Base URL**.</span></span>
        
        <div>
        

        > [!WARNING]
        > <span data-ttu-id="5fed2-216">Si vous décidez de remplacer les services Web internes par un nom de domaine complet autonome, chaque nom de domaine complet doit être unique à partir de n’importe quel autre pool frontal, directeur ou pool de directeurs.</span><span class="sxs-lookup"><span data-stu-id="5fed2-216">If you decide to override the Internal web services with a self-defined FQDN, each FQDN must be unique from any other Front End pool, Director or a Director pool.</span></span> <span data-ttu-id="5fed2-217"><STRONG>Utilisez uniquement les caractères standard</STRONG> (tels que A–Z, a–z, 0–9, et les traits d’union) quand vous définissez les URL ou les noms de domaine complets.</span><span class="sxs-lookup"><span data-stu-id="5fed2-217"><STRONG>Use only standard characters</STRONG> (including A–Z, a–z, 0–9, and hyphens) when defining URLs or fully qualified domain names.</span></span> <span data-ttu-id="5fed2-218">N’utilisez pas les caractères ou traits de soulignement Unicode.</span><span class="sxs-lookup"><span data-stu-id="5fed2-218">Do not use Unicode characters or underscores.</span></span> <span data-ttu-id="5fed2-219">Souvent, les caractères non standard dans une URL ou un FQDN ne sont pas pris en charge par le DNS externe et les autorités de certification publique (quand l’URL ou le FQDN doit être assigné au nom ou à l’autre nom de l’objet dans le certificat).</span><span class="sxs-lookup"><span data-stu-id="5fed2-219">Nonstandard characters in a URL or FQDN are often not supported by external DNS and public CAs (that is, when the URL or FQDN must be assigned to the subject name or subject alternative name in the certificate).</span></span>

        
        </div>
    
    2.  <span data-ttu-id="5fed2-220">Si vous le souhaitez, entrez l’URL de base externe dans **URL de base externe**.</span><span class="sxs-lookup"><span data-stu-id="5fed2-220">Optionally enter the external base URL in **External Base URL**.</span></span> <span data-ttu-id="5fed2-221">Pour différencier votre nom de domaine interne, entrez l’URL de base externe.</span><span class="sxs-lookup"><span data-stu-id="5fed2-221">You would enter the external base URL to differentiate it from your internal domain naming.</span></span> <span data-ttu-id="5fed2-222">Par exemple, votre domaine interne est contoso.net, mais votre nom de domaine externe est contoso.com.</span><span class="sxs-lookup"><span data-stu-id="5fed2-222">For example, your internal domain is contoso.net, but your external domain name is contoso.com.</span></span> <span data-ttu-id="5fed2-223">Vous devez définir l’URL en utilisant le nom de domaine contoso.com.</span><span class="sxs-lookup"><span data-stu-id="5fed2-223">You would define the URL using the contoso.com domain name.</span></span> <span data-ttu-id="5fed2-224">Cela est également important dans le cas d’un proxy inverse.</span><span class="sxs-lookup"><span data-stu-id="5fed2-224">This is also important in the case of a reverse proxy.</span></span> <span data-ttu-id="5fed2-225">Le nom de domaine de l’URL de base externe est le même que le nom de domaine du nom de domaine complet du proxy inverse.</span><span class="sxs-lookup"><span data-stu-id="5fed2-225">The external base URL domain name would be the same as the domain name of the FQDN of the reverse proxy.</span></span> <span data-ttu-id="5fed2-226">La messagerie instantanée et la présence nécessitent un accès HTTP au pool frontal.</span><span class="sxs-lookup"><span data-stu-id="5fed2-226">Instant messaging and presence does require HTTP access to the Front End pool.</span></span>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="5fed2-227">Pour utiliser l’équilibrage de charge DNS, vous devez créer les enregistrements DNS appropriés.</span><span class="sxs-lookup"><span data-stu-id="5fed2-227">To use DNS load balancing, you must create the appropriate DNS records.</span></span> <span data-ttu-id="5fed2-228">Pour plus d’informations, reportez-vous à <A href="lync-server-2013-configure-dns-for-load-balancing.md">configurer le DNS pour l’équilibrage de charge dans Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="5fed2-228">For details, see <A href="lync-server-2013-configure-dns-for-load-balancing.md">Configure DNS for load balancing in Lync Server 2013</A>.</span></span>

    
    </div>

10. <span data-ttu-id="5fed2-229">Si vous avez sélectionné l’option **conférences** dans la page **Sélectionner des fonctionnalités** , dans la page **Sélectionner un serveur Office Web Apps** , sélectionnez **associer le pool à un serveur Office Web Apps** , puis cliquez sur **nouveau** (ou sélectionnez un serveur Office Web Apps existant dans la liste déroulante).</span><span class="sxs-lookup"><span data-stu-id="5fed2-229">If you selected **Conferencing** on the **Select Features** page, on the **Select an Office Web Apps Server** page select **Associate pool with an Office Web Apps Server** and then click **New** (or select an existing Office Web Apps Server from the drop-down list).</span></span>

11. <span data-ttu-id="5fed2-230">Dans la boîte de dialogue **Définir un nouveau serveur Office Web Apps**, tapez le nom de domaine complet de votre ordinateur Office Web Apps Server dans la zone **Nom de domaine complet du serveur Office Web Apps**. L’URL de découverte du serveur Office Web Apps Server est alors automatiquement entrée dans la zone **URL de découverte du serveur Office Web Apps**.</span><span class="sxs-lookup"><span data-stu-id="5fed2-230">In the **Define New Office Web Apps Server** dialog box, type the fully qualified domain name (FQDN) of your Office Web Apps Server computer in the **Office Web Apps Server FQDN** box; when you do this, your Office Web Apps Server discovery URL should automatically be entered into the **Office Web Apps Server discovery URL** box.</span></span>
    
    <span data-ttu-id="5fed2-231">Si Office Web Apps Server est installé en local et dans la même zone réseau que Lync Server 2013, l’option **Office Web Apps Server déployée sur un réseau externe (c’est-à-dire le périmètre/Internet)** ne doit pas être sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="5fed2-231">If the Office Web Apps Server is installed on-premises and in the same network zone as Lync Server 2013 then the option **Office Web Apps Server is deployed in an external network (that is, perimeter/Internet)** should not be selected.</span></span>
    
    <span data-ttu-id="5fed2-232">Si le serveur Office Web Apps Server est déployé à l’extérieur de votre pare-feu interne, sélectionnez alors l’option **Le serveur Office Web Apps est déployé sur un réseau externe (périmètre/Internet)**.</span><span class="sxs-lookup"><span data-stu-id="5fed2-232">If the Office Web Apps Server is deployed outside your internal firewall, then select the option **Office Web Apps Server is deployed in an external network (that is, perimeter/Internet)**.</span></span>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="5fed2-233">Pour plus d’informations, reportez-vous à la rubrique <A href="lync-server-2013-enabling-office-web-apps-server-and-lync-server-2013.md">configuration de l’intégration avec Office Web Apps Server et Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="5fed2-233">For details, see <A href="lync-server-2013-enabling-office-web-apps-server-and-lync-server-2013.md">Configuring integration with Office Web Apps Server and Lync Server 2013</A>.</span></span>

    
    </div>

12. <span data-ttu-id="5fed2-234">Dans la page **définir le SQL Store d’archivage** , sélectionnez une instance existante ou SQL Server, ou définissez une nouvelle instance pour stocker les données associées aux données d’archivage.</span><span class="sxs-lookup"><span data-stu-id="5fed2-234">On the **Define the Archiving SQL store** page, select an existing instance or SQL Server, or define a new instance to store the data associated with archiving data.</span></span>

13. <span data-ttu-id="5fed2-235">Dans la page **définir la surveillance du SQL Store** , sélectionnez une instance existante ou SQL Server, ou définissez une nouvelle instance pour le stockage des données associées aux données d’analyse.</span><span class="sxs-lookup"><span data-stu-id="5fed2-235">On the **Define the Monitoring SQL store** page, select an existing instance or SQL Server, or define a new instance to store the data associated with monitoring data.</span></span>

14. <span data-ttu-id="5fed2-236">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="5fed2-236">Click **Next**.</span></span> <span data-ttu-id="5fed2-237">Si vous avez défini d’autres serveurs de rôles sur la page **associer des rôles de serveur à cette liste frontale** , des pages d’assistant de configuration de rôles distinctes s’ouvrent pour vous permettre de configurer les rôles de serveur.</span><span class="sxs-lookup"><span data-stu-id="5fed2-237">If you defined other role servers on the **Associate server roles with this Front End pool** page, separate role configuration wizard pages will open to let you configure the server roles.</span></span> <span data-ttu-id="5fed2-238">Pour plus d’informations, reportez-vous aux rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="5fed2-238">For details, see the following:</span></span>
    
    [<span data-ttu-id="5fed2-239">Déploiement de l’accès des utilisateurs externes dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5fed2-239">Deploying external user access in Lync Server 2013</span></span>](lync-server-2013-deploying-external-user-access.md)

15. <span data-ttu-id="5fed2-240">Si vous n’avez pas sélectionné de rôles serveur supplémentaires à configurer et déployer ou lorsque vous avez terminé la configuration des serveurs de rôles supplémentaires, cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="5fed2-240">If you did not select additional server roles to configure and deploy, or when you have finished the configuration of the additional role servers, click **Finish**.</span></span>

<span data-ttu-id="5fed2-241"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5fed2-241"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

