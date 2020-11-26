---
title: 'Skype Entreprise Server 2015 : test de récupération d’urgence'
description: 'Lync Server 2013 : test de récupération d’urgence.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Disaster recovery test
ms:assetid: 04f5e747-d837-4350-9fc0-8605dbf025a7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn747887(v=OCS.15)
ms:contentKeyID: 63969571
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fa22abd37f656134c54381d63f29d3160ff85257
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437832"
---
# <a name="disaster-recovery-test-in-lync-server-2013"></a><span data-ttu-id="10471-103">Test de récupération d’urgence dans Skype Entreprise Server 2015</span><span class="sxs-lookup"><span data-stu-id="10471-103">Disaster recovery test in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="10471-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="10471-104">

<span> </span></span></span>

<span data-ttu-id="10471-105">_**Dernière modification de la rubrique :** 2015-01-26_</span><span class="sxs-lookup"><span data-stu-id="10471-105">_**Topic Last Modified:** 2015-01-26_</span></span>

<span data-ttu-id="10471-106">Effectuez une récupération du système pour un serveur de pool Lync Server 2013 pour tester votre processus de récupération d’urgence documenté.</span><span class="sxs-lookup"><span data-stu-id="10471-106">Perform a system recovery for a Lync Server 2013 pool server to test your documented disaster recovery process.</span></span> <span data-ttu-id="10471-107">Ce test simule une défaillance matérielle complète d’un serveur et permet de s’assurer que les ressources, les plans et les données sont disponibles pour la récupération.</span><span class="sxs-lookup"><span data-stu-id="10471-107">This test will simulate a complete hardware failure for one server, and will help guarantee that the resources, plans, and data is available for recovery.</span></span> <span data-ttu-id="10471-108">Essayez d’alterner l’angle du test chaque mois afin que votre organisation teste chaque fois la défaillance d’un autre serveur ou d’un autre équipement.</span><span class="sxs-lookup"><span data-stu-id="10471-108">Try to rotate the focus of the test each month so that your organization tests the failure of a different server or other piece of equipment every time.</span></span>

<span data-ttu-id="10471-p102">Notez que le calendrier des tests de récupération d'urgence de votre organisation varie. Il est très important que les tests de récupération d’urgence ne soient ni ignorés ni négligés.</span><span class="sxs-lookup"><span data-stu-id="10471-p102">Note that the schedule by which organizations perform Disaster Recovery testing will vary. It is very important that disaster recovery testing is not ignored or neglected.</span></span>

<div>


<span data-ttu-id="10471-111">Exportez votre topologie, les stratégies et les paramètres de configuration de Lync Server 2013 vers un fichier.</span><span class="sxs-lookup"><span data-stu-id="10471-111">Export your Lync Server 2013 topology, policies, and configuration settings to a file.</span></span> <span data-ttu-id="10471-112">Ce fichier peut, entre autres, être utilisé pour restaurer ces informations dans le magasin central de gestion après une mise à niveau, une défaillance matérielle ou un autre problème ayant entraîné une perte de données.</span><span class="sxs-lookup"><span data-stu-id="10471-112">Among other things, this file can then be used to restore this information to the Central Management store after an upgrade, a hardware failure, or some other issue has resulted in data loss.</span></span>

<span data-ttu-id="10471-113">Importez votre topologie et vos paramètres de configuration de Lync Server 2013 vers le magasin de gestion central ou vers l’ordinateur local, comme illustré dans les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="10471-113">Import your Lync Server 2013 topology, policies, and configuration settings to either the Central Management store or to the local computer as shown in the following commands:</span></span>

`Import-CsConfiguration -ByteInput <Byte[]> [-Force <SwitchParameter>] [-LocalStore <SwitchParameter>]`

`Import-CsConfiguration -FileName <String> [-Force <SwitchParameter>] [-LocalStore <SwitchParameter>]`

<span data-ttu-id="10471-114">Pour sauvegarder les données de Lync Server 2013 de production, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="10471-114">To back up production Lync Server 2013 data:</span></span>

  - <span data-ttu-id="10471-115">Sauvegardez les bases de données RTC et LCSLog à l’aide du processus de sauvegarde SQL Server standard pour vider la base de données sur un fichier ou un appareil de vidage de bande.</span><span class="sxs-lookup"><span data-stu-id="10471-115">Back up the RTC and LCSLog databases by using the standard SQL Server backup process to dump the database to a file or tape dump device.</span></span>

  - <span data-ttu-id="10471-116">Sauvegardez les données dans un fichier ou sur une bande à l’aide de l’application de sauvegarde tierce.</span><span class="sxs-lookup"><span data-stu-id="10471-116">Use third-party backup application to back up the data to file or to tape.</span></span>

  - <span data-ttu-id="10471-117">Créez un export XML de la base de données RTC intégrale à l’aide de l’applet de commande Export-CsUserData.</span><span class="sxs-lookup"><span data-stu-id="10471-117">Use the Export-CsUserData cmdlet to create an XML export of the whole RTC database.</span></span>

  - <span data-ttu-id="10471-118">Sauvegardez le contenu d’une réunion et les journaux de conformité à l’aide de la sauvegarde du système de fichiers ou d’un utilitaire de sauvegarde/restauration tiers.</span><span class="sxs-lookup"><span data-stu-id="10471-118">Use the file system backup or third-party to back up meeting content and compliance logs.</span></span>

  - <span data-ttu-id="10471-119">Utilisez l’outil de ligne de commande Export-CsConfiguration pour sauvegarder les paramètres de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="10471-119">Use the Export-CsConfiguration command-line tool to back up Lync Server 2013 settings.</span></span>

<span data-ttu-id="10471-120">La première étape de la procédure de basculement comporte un déplacement forcé des utilisateurs du pool de production vers le pool de récupération d’urgence.</span><span class="sxs-lookup"><span data-stu-id="10471-120">The first step in the failover procedure includes a forced move of users from the production pool to the Disaster Recovery pool.</span></span>

<span data-ttu-id="10471-121">Il s’agit d’un déplacement forcé, car le pool de production n’est pas disponible pour accepter le déplacement des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="10471-121">This will be a forced move because the production pool won't be available to accept the user relocation.</span></span>

<span data-ttu-id="10471-122">Le processus de déplacement d’utilisateur de Lync Server 2013 est une modification apportée à un attribut sur l’objet de compte d’utilisateur, en plus de la mise à jour d’un enregistrement dans la base de données SQL RTC.</span><span class="sxs-lookup"><span data-stu-id="10471-122">The Lync Server 2013 move user process is effectively a change to an attribute on the user account object in addition to a record update on the RTC SQL database.</span></span>

<span data-ttu-id="10471-123">Ces données peuvent être restaurées par le biais des deux procédures suivantes :</span><span class="sxs-lookup"><span data-stu-id="10471-123">This data can be restored through the following two processes:</span></span>

  - <span data-ttu-id="10471-124">La base de données RTC peut être restaurée à partir de l’appareil de vidage de sauvegarde original à partir du serveur SQL de production en utilisant le processus de restauration standard de SQL Server, ou à l’aide d’une utilitaire de sauvegarde/restauration tierce.</span><span class="sxs-lookup"><span data-stu-id="10471-124">RTC database can be restored from the original backup dump device from the production SQL Server using the standard SQL Server restore process, or using a third-party backup/restore utility.</span></span>

  - <span data-ttu-id="10471-125">Les données de contact des utilisateurs peuvent être restaurées avec l’utilitaire DBIMPEXP.exe à l’aide du fichier XML créé à partir de l’export SQL Server de production.</span><span class="sxs-lookup"><span data-stu-id="10471-125">User contact data can be restored with the DBIMPEXP.exe utility using the XML file that was created from the production SQL Server export.</span></span>

<span data-ttu-id="10471-126">Une fois ces données restaurées, les utilisateurs peuvent se connecter efficacement au pool Lync Server 2013 de reprise après sinistre et fonctionner comme d’habitude.</span><span class="sxs-lookup"><span data-stu-id="10471-126">After this data is restored, users can effectively connect to the Disaster Recovery Lync Server 2013 pool, and operate as usual.</span></span>

<span data-ttu-id="10471-127">Pour permettre aux utilisateurs de se connecter au pool de reprise après sinistre Lync Server 2013, une modification de l’enregistrement DNS sera requise.</span><span class="sxs-lookup"><span data-stu-id="10471-127">To enable users to connect to the Disaster Recovery Lync Server 2013 pool, a DNS record change will be required.</span></span>

<span data-ttu-id="10471-128">Le pool Lync Server 2013 de production sera référencé par les clients à l’aide de la configuration automatique et des enregistrements SRV DNS de :</span><span class="sxs-lookup"><span data-stu-id="10471-128">The production Lync Server 2013 pool will be referenced by clients using the auto-configuration and DNS SRV records of:</span></span>

  - <span data-ttu-id="10471-129">SRV : \_ SIP. \_ TLS.\<domain\></span><span class="sxs-lookup"><span data-stu-id="10471-129">SRV: \_sip.\_tls.\<domain\></span></span> <span data-ttu-id="10471-130">/CNAME : SIP.\<domain\></span><span class="sxs-lookup"><span data-stu-id="10471-130">/CNAME: SIP.\<domain\></span></span>

  - <span data-ttu-id="10471-131">CNAME : SIP.\<domain\></span><span class="sxs-lookup"><span data-stu-id="10471-131">CNAME: SIP.\<domain\></span></span> <span data-ttu-id="10471-132">/cvc-pool-1.\<domain\></span><span class="sxs-lookup"><span data-stu-id="10471-132">/cvc-pool-1.\<domain\></span></span>

<span data-ttu-id="10471-133">Pour faciliter le basculement, cet enregistrement CNAME doit être mis à jour de manière à référencer le nom de domaine complet (FQDN) DROCSPool :</span><span class="sxs-lookup"><span data-stu-id="10471-133">To facilitate the failover, this CNAME record must be updated to reference the DROCSPool FQDN:</span></span>

  - <span data-ttu-id="10471-134">CNAME : SIP.\<domain\></span><span class="sxs-lookup"><span data-stu-id="10471-134">CNAME: SIP.\<domain\></span></span> <span data-ttu-id="10471-135">/DROCSPool.\<domain\></span><span class="sxs-lookup"><span data-stu-id="10471-135">/DROCSPool.\<domain\></span></span>

  - <span data-ttu-id="10471-136">SIP.\<domain\></span><span class="sxs-lookup"><span data-stu-id="10471-136">Sip.\<domain\></span></span>

  - <span data-ttu-id="10471-137">Violation.\<domain\></span><span class="sxs-lookup"><span data-stu-id="10471-137">AV.\<domain\></span></span>

  - <span data-ttu-id="10471-138">webconf.\<domain\></span><span class="sxs-lookup"><span data-stu-id="10471-138">webconf.\<domain\></span></span>

  - <span data-ttu-id="10471-139">OCSServices.\<domain\></span><span class="sxs-lookup"><span data-stu-id="10471-139">OCSServices.\<domain\></span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="10471-140">Pour des procédures d’administration et de gestion détaillées, reportez-vous à la rubrique <A href="lync-server-2013-backing-up-and-restoring-lync-server.md">sauvegarde et restauration de Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="10471-140">For detailed administration and management procedures, see <A href="lync-server-2013-backing-up-and-restoring-lync-server.md">Backing up and restoring Lync Server 2013</A>.</span></span>



</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="10471-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="10471-141">See Also</span></span>


[<span data-ttu-id="10471-142">Planification de la haute disponibilité et de la récupération d’urgence dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="10471-142">Planning for high availability and disaster recovery in Lync Server 2013</span></span>](lync-server-2013-planning-for-high-availability-and-disaster-recovery.md)  
[<span data-ttu-id="10471-143">Cmdlets de sauvegarde et de haute disponibilité dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="10471-143">Backup and high availability cmdlets in Lync Server 2013</span></span>](https://docs.microsoft.com/powershell/module/skype/?view=skype-ps)  


[<span data-ttu-id="10471-144">Importation-CsConfiguration</span><span class="sxs-lookup"><span data-stu-id="10471-144">Import-CsConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Import-CsConfiguration)  
[<span data-ttu-id="10471-145">Sauvegarde et restauration de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="10471-145">Backing up and restoring Lync Server 2013</span></span>](lync-server-2013-backing-up-and-restoring-lync-server.md)  
[<span data-ttu-id="10471-146">Gestion de la récupération d’urgence, de la haute disponibilité et du service de sauvegarde de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="10471-146">Managing Lync Server 2013 disaster recovery, high availability, and Backup Service</span></span>](lync-server-2013-managing-lync-server-disaster-recovery-high-availability-and-backup-service.md)  
  

<span data-ttu-id="10471-147"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="10471-147"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

