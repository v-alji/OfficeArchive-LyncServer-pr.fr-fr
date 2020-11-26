---
title: 'Lync Server 2013 : Préparation du schéma Active Directory'
description: 'Lync Server 2013 : préparation du schéma Active Directory.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Preparing the Active Directory schema
ms:assetid: 067726ae-fd3f-4133-a32f-26d2603ac674
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398119(v=OCS.15)
ms:contentKeyID: 48183300
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3df7533dcbabe278fd366b441cfd8daa83f54b23
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424113"
---
# <a name="preparing-the-active-directory-schema-in-lync-server-2013"></a><span data-ttu-id="7dce6-103">Préparation du schéma Active Directory dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7dce6-103">Preparing the Active Directory schema in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7dce6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7dce6-104">

<span> </span></span></span>

<span data-ttu-id="7dce6-105">_**Dernière modification de la rubrique :** 2012-08-27_</span><span class="sxs-lookup"><span data-stu-id="7dce6-105">_**Topic Last Modified:** 2012-08-27_</span></span>

<span data-ttu-id="7dce6-106">Avant de commencer à préparer les services de domaine Active Directory, vous pouvez ouvrir les fichiers de schéma à l’aide d’un éditeur de texte, tel que le bloc-notes Windows, ou voir [extensions de schéma Active Directory, classes et attributs utilisés par Lync server 2013](lync-server-2013-active-directory-schema-extensions-classes-and-attributes-used-by-lync-server.md) pour consulter toutes les extensions de schéma des services de domaine Active Directory qui seront modifiées pour lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="7dce6-106">Before you begin preparing Active Directory Domain Services, you can open the schema files by using a text editor, such as Windows Notepad, or see [Active Directory schema extensions, classes, and attributes used by Lync Server 2013](lync-server-2013-active-directory-schema-extensions-classes-and-attributes-used-by-lync-server.md) to review all the Active Directory Domain Services schema extensions that will be modified for Lync Server 2013.</span></span> <span data-ttu-id="7dce6-107">Lync Server utilise quatre fichiers de schéma :</span><span class="sxs-lookup"><span data-stu-id="7dce6-107">Lync Server uses four schema files:</span></span>

  - <span data-ttu-id="7dce6-108">ExternalSchema. ldf, utilisé à des fins d’interopérabilité avec Microsoft Exchange Server</span><span class="sxs-lookup"><span data-stu-id="7dce6-108">ExternalSchema.ldf, which is used for interoperability with Microsoft Exchange Server</span></span>

  - <span data-ttu-id="7dce6-109">ServerSchema. ldf, qui est le fichier de schéma principal de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7dce6-109">ServerSchema.ldf, which is the primary Lync Server 2013 schema file</span></span>

  - <span data-ttu-id="7dce6-110">BackCompatSchema. ldf, utilisé à des fins d’interopérabilité avec les composants des versions précédentes</span><span class="sxs-lookup"><span data-stu-id="7dce6-110">BackCompatSchema.ldf, which is used for interoperability with any components from prior releases</span></span>

  - <span data-ttu-id="7dce6-111">VersionSchema. ldf, qui est utilisé pour les informations de version du schéma préparé.</span><span class="sxs-lookup"><span data-stu-id="7dce6-111">VersionSchema.ldf, which is used for version information of the prepared schema</span></span>

<span data-ttu-id="7dce6-112">Tous les fichiers. ldf sont installés lors de la préparation du schéma, que vous passiez à partir d’une version précédente ou que vous effectuiez une nouvelle installation.</span><span class="sxs-lookup"><span data-stu-id="7dce6-112">All .ldf files are installed during schema preparation, regardless of whether you are migrating from a previous release or performing a clean installation.</span></span> <span data-ttu-id="7dce6-113">Ces fichiers de schéma sont installés dans l’ordre présenté dans la liste précédente et se trouvent dans \\ le \\ dossier de schéma de support sur le média d’installation.</span><span class="sxs-lookup"><span data-stu-id="7dce6-113">These schema files are installed in the sequence shown in the preceding list and are located in the \\Support\\schema folder on the installation media.</span></span>

<span data-ttu-id="7dce6-114">Les extensions de schéma Lync Server sont répliquées dans tous les domaines, ce qui a un impact sur le trafic réseau.</span><span class="sxs-lookup"><span data-stu-id="7dce6-114">The Lync Server schema extensions are replicated across all domains, which impacts network traffic.</span></span> <span data-ttu-id="7dce6-115">Exécutez la préparation du schéma à la fois lorsque le niveau d’utilisation du réseau est faible.</span><span class="sxs-lookup"><span data-stu-id="7dce6-115">Run schema preparation at a time when network usage is low.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="7dce6-116">Si vous avez besoin d’ajouter la prise en charge de Microsoft® Office Communicator Mobile 2007 R2 pour Java et Microsoft® Office Communicator Mobile pour Nokia 1,0 vers votre déploiement Lync Server 2013, vous devez préparer le schéma Active Directory pour Microsoft Office Communications Server 2007 R2 lors de l’installation de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="7dce6-116">If you need to add support for Microsoft® Office Communicator Mobile 2007 R2 for Java and Microsoft® Office Communicator Mobile for Nokia 1.0 mobile clients to your Lync Server 2013 deployment, you need to prepare the Active Directory schema for Microsoft Office Communications Server 2007 R2 during installation of Lync Server 2013.</span></span> <span data-ttu-id="7dce6-117">Pour le logiciel et la documentation nécessaires, voir <A href="https://go.microsoft.com/fwlink/p/?linkid=207172">https://go.microsoft.com/fwlink/p/?linkId=207172</A> .</span><span class="sxs-lookup"><span data-stu-id="7dce6-117">For the necessary software and documentation, see <A href="https://go.microsoft.com/fwlink/p/?linkid=207172">https://go.microsoft.com/fwlink/p/?linkId=207172</A>.</span></span>



</div>

<div>

## <a name="adsi-edit"></a><span data-ttu-id="7dce6-118">Modification ADSI</span><span class="sxs-lookup"><span data-stu-id="7dce6-118">ADSI Edit</span></span>

<span data-ttu-id="7dce6-119">L’éditeur d’interfaces de service Active Directory (ADSI Edit) est un outil d’administration AD DS qui vous permet de vérifier la préparation du schéma et la réplication.</span><span class="sxs-lookup"><span data-stu-id="7dce6-119">Active Directory Service Interfaces Editor (ADSI Edit) is an AD DS administration tool that you can use to verify schema preparation and replication.</span></span>

<span data-ttu-id="7dce6-120">ADSI Edit est installé par défaut lorsque vous installez le rôle AD DS pour définir un serveur comme contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="7dce6-120">ADSI Edit is installed by default when you install the AD DS role to make a server a domain controller.</span></span> <span data-ttu-id="7dce6-121">Pour Windows Server 2008 et Windows Server 2008 R2, ADSI Edit (adsied. msc) est inclus dans les outils d’administration de serveur distant.</span><span class="sxs-lookup"><span data-stu-id="7dce6-121">For Windows Server 2008 and Windows Server 2008 R2, ADSI Edit (adsiedit.msc) is included with the Remote Server Administration Tools (RSAT).</span></span> <span data-ttu-id="7dce6-122">Vous pouvez également installer le RSAT sur les serveurs de membres de domaine ou les serveurs autonomes.</span><span class="sxs-lookup"><span data-stu-id="7dce6-122">You can also install RSAT on domain member servers or stand-alone servers.</span></span> <span data-ttu-id="7dce6-123">Le package RSAT est copié sur ces serveurs par défaut lors de l’installation de Windows, mais il n’est pas installé par défaut.</span><span class="sxs-lookup"><span data-stu-id="7dce6-123">The RSAT package is copied to these servers by default when you install Windows, but it is not installed by default.</span></span> <span data-ttu-id="7dce6-124">Vous installez des outils individuels à l’aide du gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="7dce6-124">You install individual tools by using Server Manager.</span></span> <span data-ttu-id="7dce6-125">La modification ADSI est incluse dans **Outils d’administration de rôles**, outils de services de **domaine Active Directory**, **outils de contrôleur de domaine Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="7dce6-125">ADSI Edit is included under **Role Administration Tools**, **Active Directory Domain Services Tools**, **Active Directory Domain Controller Tools**.</span></span>

<span data-ttu-id="7dce6-126">Pour Windows Server 2003, l’édition ADSI est incluse dans les outils de support.</span><span class="sxs-lookup"><span data-stu-id="7dce6-126">For Windows Server 2003, ADSI Edit is included with the Support Tools.</span></span> <span data-ttu-id="7dce6-127">Les outils de support sont disponibles sur le CD Windows Server 2003 dans \\ le \\ dossier Outils de support, ou vous pouvez les télécharger à partir des outils de support technique de windows Server 2003 Service Pack 2 32-bit [https://go.microsoft.com/fwlink/p/?linkId=125770](https://go.microsoft.com/fwlink/p/?linkid=125770) .</span><span class="sxs-lookup"><span data-stu-id="7dce6-127">The Support Tools are available from the Windows Server 2003 CD in the \\SUPPORT\\TOOLS folder, or you can download them from “Windows Server 2003 Service Pack 2 32-bit Support Tools” at [https://go.microsoft.com/fwlink/p/?linkId=125770](https://go.microsoft.com/fwlink/p/?linkid=125770).</span></span> <span data-ttu-id="7dce6-128">Pour obtenir des instructions sur l’installation des outils d’assistance technique sur le CD du produit, voir la section « installer les outils de support Windows » à l’adresse [https://go.microsoft.com/fwlink/p/?linkId=125771](https://go.microsoft.com/fwlink/p/?linkid=125771) .</span><span class="sxs-lookup"><span data-stu-id="7dce6-128">Instructions for installing the Support Tools from the product CD are available from “Install Windows Support Tools” at [https://go.microsoft.com/fwlink/p/?linkId=125771](https://go.microsoft.com/fwlink/p/?linkid=125771).</span></span> <span data-ttu-id="7dce6-129">La Adsiedit.dll est automatiquement enregistrée lorsque vous installez les outils de support.</span><span class="sxs-lookup"><span data-stu-id="7dce6-129">Adsiedit.dll is automatically registered when you install the support tools.</span></span> <span data-ttu-id="7dce6-130">Toutefois, si vous avez copié les fichiers sur votre ordinateur, vous devez exécuter la commande **regsvr32** pour inscrire le fichier adsiedit.dll avant de pouvoir exécuter l’outil.</span><span class="sxs-lookup"><span data-stu-id="7dce6-130">If, however, you copied the files to your computer, you must run the **regsvr32** command to register the adsiedit.dll file before you can run the tool.</span></span>

</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="7dce6-131">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="7dce6-131">In This Section</span></span>

  - [<span data-ttu-id="7dce6-132">Exécution de la préparation du schéma Active Directory dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7dce6-132">Running Active Directory schema preparation in Lync Server 2013</span></span>](lync-server-2013-running-schema-preparation.md)

  - [<span data-ttu-id="7dce6-133">Vérification de la réplication de schéma Active Directory dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7dce6-133">Verifying Active Directory schema replication in Lync Server 2013</span></span>](lync-server-2013-verifying-schema-replication.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="7dce6-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7dce6-134">See Also</span></span>


[<span data-ttu-id="7dce6-135">Préparation de la forêt pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7dce6-135">Preparing the forest for Lync Server 2013</span></span>](lync-server-2013-preparing-the-forest.md)  
[<span data-ttu-id="7dce6-136">Préparation des domaines pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7dce6-136">Preparing domains for Lync Server 2013</span></span>](lync-server-2013-preparing-domains.md)  
  

<span data-ttu-id="7dce6-137"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7dce6-137"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

