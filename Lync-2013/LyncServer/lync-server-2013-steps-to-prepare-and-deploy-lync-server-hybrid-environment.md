---
title: 'Lync Server 2013 : Procédure de préparation et de déploiement d’un environnement hybride Lync Server'
description: 'Lync Server 2013 : étapes de préparation et de déploiement de l’environnement Lync Server hybride.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Steps to prepare and deploy Lync Server 2013 hybrid environment
ms:assetid: a50d4f7b-63f4-4663-af63-56ca87e4e3e7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205157(v=OCS.15)
ms:contentKeyID: 48185060
ms.date: 12/29/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ffb791a8a45b2220d8987c8d688f346447747c00
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49393945"
---
# <a name="steps-to-prepare-and-deploy-lync-server-2013-hybrid-environment"></a><span data-ttu-id="3e822-103">Procédure de préparation et de déploiement d’un environnement hybride Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3e822-103">Steps to prepare and deploy Lync Server 2013 hybrid environment</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3e822-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3e822-104">

<span> </span></span></span>

<span data-ttu-id="3e822-105">_**Dernière modification de la rubrique :** 2016-12-08_</span><span class="sxs-lookup"><span data-stu-id="3e822-105">_**Topic Last Modified:** 2016-12-08_</span></span>

<span data-ttu-id="3e822-106">Le tableau suivant répertorie les étapes nécessaires pour préparer votre environnement pour un déploiement hybride avec Skype entreprise Online et Microsoft Office 365.</span><span class="sxs-lookup"><span data-stu-id="3e822-106">The following table lists the steps required to prepare your environment for a hybrid deployment with Skype for Business Online and Microsoft Office 365.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3e822-107">Terminé ?</span><span class="sxs-lookup"><span data-stu-id="3e822-107">Completed?</span></span></th>
<th><span data-ttu-id="3e822-108">Étape</span><span class="sxs-lookup"><span data-stu-id="3e822-108">Step</span></span></th>
<th><span data-ttu-id="3e822-109">Description</span><span class="sxs-lookup"><span data-stu-id="3e822-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><p><span data-ttu-id="3e822-110">Créer un compte client pour Office 365 et activer Lync Online</span><span class="sxs-lookup"><span data-stu-id="3e822-110">Create a tenant account for Office 365 and enable Lync Online</span></span></p></td>
<td><p><span data-ttu-id="3e822-111">En savoir plus sur Office 365 et Lync Online dans <a href="https://go.microsoft.com/fwlink/p/?linkid=254980">office 365</a>.</span><span class="sxs-lookup"><span data-stu-id="3e822-111">Learn about Office 365 and Lync Online at <a href="https://go.microsoft.com/fwlink/p/?linkid=254980">Office 365</a>.</span></span></p>
<p><span data-ttu-id="3e822-112">Pour vérifier que votre environnement est prêt pour Office 365, consultez la <a href="https://go.microsoft.com/fwlink/p/?linkid=401408">Configuration système requise</a>.</span><span class="sxs-lookup"><span data-stu-id="3e822-112">To make sure that your environment is ready for Office 365, see the <a href="https://go.microsoft.com/fwlink/p/?linkid=401408">System Requirements</a>.</span></span></p>
<p><span data-ttu-id="3e822-113">Pour plus d’informations sur la configuration d’Office 365, voir <a href="https://go.microsoft.com/fwlink/p/?linkid=254982">mise en route d’office 365</a> et <a href="https://go.microsoft.com/fwlink/p/?linkid=254979">Configurer Office 365</a>.</span><span class="sxs-lookup"><span data-stu-id="3e822-113">For details about setting up Office 365, see <a href="https://go.microsoft.com/fwlink/p/?linkid=254982">Getting Started with Office 365</a> and <a href="https://go.microsoft.com/fwlink/p/?linkid=254979">Set Up Office 365</a>.</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="3e822-114">Ajout de votre domaine et vérification de la propriété</span><span class="sxs-lookup"><span data-stu-id="3e822-114">Add your domain and verify ownership</span></span></p></td>
<td><p><span data-ttu-id="3e822-115">Votre domaine est parfois appelé <em>domaine personnel</em>.</span><span class="sxs-lookup"><span data-stu-id="3e822-115">Your domain is sometimes also referred to as your <em>vanity domain</em>.</span></span> <span data-ttu-id="3e822-116">Vous devez ajouter votre domaine à votre organisation Office 365, puis suivre les étapes permettant de valider le domaine avec Office 365.</span><span class="sxs-lookup"><span data-stu-id="3e822-116">You must add your domain to your Office 365 organization, and then follow the steps to validate the domain with Office 365.</span></span> <span data-ttu-id="3e822-117">Cela permet de confirmer que vous êtes bien le propriétaire du domaine.</span><span class="sxs-lookup"><span data-stu-id="3e822-117">This is to confirm that you are the owner of the domain.</span></span></p>
<p><span data-ttu-id="3e822-118">Pour ajouter votre domaine à votre organisation 365 Office, suivez les étapes décrites dans l’article <a href="https://go.microsoft.com/fwlink/p/?linkid=254983">ajouter votre domaine à office 365</a>.</span><span class="sxs-lookup"><span data-stu-id="3e822-118">To add your domain to your Office 365 organization, follow the steps described at <a href="https://go.microsoft.com/fwlink/p/?linkid=254983">Add your domain to Office 365</a>.</span></span></p>
<p><span data-ttu-id="3e822-119">Effectuez toutes les étapes de chaque section de la rubrique, y compris la &quot; modification des enregistrements DNS pour vos services 365 Office.&quot;</span><span class="sxs-lookup"><span data-stu-id="3e822-119">Complete all of the steps in each section in the topic, including &quot;Edit DNS records for your Office 365 services.&quot;</span></span></p></td>
</tr>
<tr class="odd">
<td></td>
<td><p><span data-ttu-id="3e822-120">Vérifier la compatibilité de l’environnement</span><span class="sxs-lookup"><span data-stu-id="3e822-120">Verify environment readiness</span></span></p></td>
<td><p><span data-ttu-id="3e822-121">Vous pouvez utiliser l’Assistant Installation d’Office 365 pour vous aider à déployer Office 365.</span><span class="sxs-lookup"><span data-stu-id="3e822-121">You can use the Office 365 Setup Assistant to help you deploy Office 365.</span></span> <span data-ttu-id="3e822-122">Pour plus d’informations, reportez-vous <a href="https://go.microsoft.com/fwlink/p/?linkid=254985">à utiliser l’Assistant de configuration pour déterminer la disponibilité d’Office 365</a>.</span><span class="sxs-lookup"><span data-stu-id="3e822-122">For more information, see <a href="https://go.microsoft.com/fwlink/p/?linkid=254985">Use Setup Assistant to determine Office 365 readiness</a>.</span></span></p>
<p><span data-ttu-id="3e822-123">Pour plus d’informations sur l’utilisation de l’outil et le déploiement d’Office 365, voir le <a href="https://go.microsoft.com/fwlink/p/?linkid=257337">Guide de déploiement d’office 365</a>.</span><span class="sxs-lookup"><span data-stu-id="3e822-123">For details about using the tool and deploying Office 365, see <a href="https://go.microsoft.com/fwlink/p/?linkid=257337">Office 365 deployment guide</a>.</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="3e822-124">Préparer la synchronisation Active Directory</span><span class="sxs-lookup"><span data-stu-id="3e822-124">Prepare for Active Directory synchronization</span></span></p></td>
<td><p><span data-ttu-id="3e822-125">La synchronisation Active Directory maintient votre annuaire Active Directory local synchronisé en continu avec Office 365.</span><span class="sxs-lookup"><span data-stu-id="3e822-125">Active Directory synchronization keeps your on-premises Active Directory continuously synchronized with Office 365.</span></span> <span data-ttu-id="3e822-126">Cela vous permet de créer des versions synchronisées de chaque groupe et compte d’utilisateur et de synchroniser la liste d’adresses globale de votre environnement Microsoft Exchange Server local vers Microsoft Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="3e822-126">This lets you create synchronized versions of each user account and group, and also enables global address list (GAL) synchronization from your local Microsoft Exchange Server environment to Microsoft Exchange Online.</span></span></p>
<div>

> [!IMPORTANT]  
> <span data-ttu-id="3e822-127">Vous devez synchroniser les comptes d’annonces de tous les utilisateurs de Lync au sein de votre organisation entre votre déploiement local et votre déploiement Lync en ligne, même si les utilisateurs ne sont pas déplacés vers Lync Online.</span><span class="sxs-lookup"><span data-stu-id="3e822-127">You need to synchronize the AD accounts for all Lync users in your organization between your on-premises and online Lync deployments, even if users are not moved to Lync Online.</span></span> <span data-ttu-id="3e822-128">Si vous ne synchronisez pas tous les utilisateurs, la communication entre les utilisateurs locaux et en ligne dans votre organisation risque de ne pas fonctionner comme vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="3e822-128">If you do not synchronize all users, communication between on-premises and online users in your organization may not work as expected.</span></span>


</div>
<p><span data-ttu-id="3e822-129">Pour préparer votre environnement en vue de la synchronisation Active Directory, suivez les étapes décrites dans la feuille de route de la <a href="https://go.microsoft.com/fwlink/p/?linkid=254988">synchronisation d’annuaires</a>, y compris la configuration de l’authentification unique.</span><span class="sxs-lookup"><span data-stu-id="3e822-129">To prepare your environment for Active Directory synchronization, follow the steps described in <a href="https://go.microsoft.com/fwlink/p/?linkid=254988">Directory synchronization Roadmap</a>, including setting up single sign-on.</span></span></p></td>
</tr>
<tr class="odd">
<td></td>
<td><p><span data-ttu-id="3e822-130">Créer des certificats pour les services AD FS (Active Directory Federation Services)</span><span class="sxs-lookup"><span data-stu-id="3e822-130">Create certificates for Active Directory Federation Services (AD FS)</span></span></p></td>
<td><p><span data-ttu-id="3e822-131">Vous devrez créer les certificats utilisés pour la Fédération des identités avec Office 365.</span><span class="sxs-lookup"><span data-stu-id="3e822-131">You will need to create the certificates that are used for identity federation with Office 365.</span></span> <span data-ttu-id="3e822-132">Pour plus d’informations, reportez-vous à la section « certificats de serveur de Fédération » de la rubrique planifier pour le déploiement d’AD FS pour une utilisation avec une connexion unique de la <a href="https://go.microsoft.com/fwlink/p/?linkid=285376">liste de contrôle : utiliser AD FS pour implémenter et gérer l’authentification unique</a>.</span><span class="sxs-lookup"><span data-stu-id="3e822-132">For more information, see the “Federation server certificates” section of the Plan for and deploy AD FS for use with single sign-on topic at <a href="https://go.microsoft.com/fwlink/p/?linkid=285376">Checklist: Use AD FS to implement and manage single sign-on</a>.</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="3e822-133">Attribuer des certificats pour AD FS</span><span class="sxs-lookup"><span data-stu-id="3e822-133">Assign certificates for AD FS</span></span></p></td>
<td><p><span data-ttu-id="3e822-134">Après avoir créé les certificats utilisés pour la Fédération des identités avec Office 365, vous devez les installer et les affecter.</span><span class="sxs-lookup"><span data-stu-id="3e822-134">After you create the certificates that are used for identity federation with Office 365, you must install and assign them.</span></span></p></td>
</tr>
<tr class="odd">
<td></td>
<td><p><span data-ttu-id="3e822-135">Déplacer les utilisateurs pilotes vers Skype entreprise Online</span><span class="sxs-lookup"><span data-stu-id="3e822-135">Move pilot users to Skype for Business Online</span></span></p></td>
<td><p><span data-ttu-id="3e822-136">Après avoir suivi les étapes de préparation et de configuration de votre environnement pour Skype entreprise Online, vous pouvez commencer à déplacer les utilisateurs pilotes vers Lync Online.</span><span class="sxs-lookup"><span data-stu-id="3e822-136">After you have completed the steps to prepare and configure your environment for Skype for Business Online, you can start moving pilot users to Lync Online.</span></span></p>
<p><span data-ttu-id="3e822-137">Voir <a href="lync-server-2013-move-users-to-lync-online.md">déplacer des utilisateurs vers Lync Online dans Lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="3e822-137">See <a href="lync-server-2013-move-users-to-lync-online.md">Move users to Lync Online in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="3e822-138">Administration des utilisateurs dans un déploiement hybride</span><span class="sxs-lookup"><span data-stu-id="3e822-138">Administering users in a hybrid deployment</span></span></p></td>
<td><p><span data-ttu-id="3e822-139">Pour plus d’informations sur la façon d’administrer les utilisateurs dans un déploiement hybride, consultez <a href="lync-server-2013-administering-users-in-a-hybrid-deployment.md">administration des utilisateurs dans un déploiement 2013 hybride de Lync Server</a>.</span><span class="sxs-lookup"><span data-stu-id="3e822-139">For details about how to administer users in a hybrid deployment, see <a href="lync-server-2013-administering-users-in-a-hybrid-deployment.md">Administering users in a hybrid Lync Server 2013 deployment</a>.</span></span></p></td>
</tr><span data-ttu-id="3e822-140">
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3e822-140">
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span></span></div>

