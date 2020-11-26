---
title: Migrer le carnet d’adresses
description: Migration du carnet d’adresses.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migrate Address Book
ms:assetid: ac7f0f39-4c6d-4702-8e25-93a73e3d800f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205160(v=OCS.15)
ms:contentKeyID: 48185064
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ad6acd8cca58aa4e09e21b9b45cbdddec527b5f8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438609"
---
# <a name="migrate-address-book"></a><span data-ttu-id="a2108-103">Migrer le carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="a2108-103">Migrate Address Book</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a2108-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a2108-104">

<span> </span></span></span>

<span data-ttu-id="a2108-105">_**Dernière modification de la rubrique :** 2012-10-09_</span><span class="sxs-lookup"><span data-stu-id="a2108-105">_**Topic Last Modified:** 2012-10-09_</span></span>

<span data-ttu-id="a2108-106">En règle générale, le carnet d’adresses de Lync Server 2010 est migré en même temps que le reste de votre topologie.</span><span class="sxs-lookup"><span data-stu-id="a2108-106">In general, the Lync Server 2010 Address Book is migrated along with the rest of your topology.</span></span> <span data-ttu-id="a2108-107">Toutefois, vous devrez peut-être effectuer certaines étapes après la migration si vous avez personnalisé les éléments suivants dans votre environnement Lync Server 2010 :</span><span class="sxs-lookup"><span data-stu-id="a2108-107">However, you might need to perform some post-migration steps if you customized the following in your Lync Server 2010 environment:</span></span>

  - <span data-ttu-id="a2108-108">Définissez la propriété WMI **PartitionbyOU** pour regrouper les entrées du carnet d’adresses par unité d’organisation.</span><span class="sxs-lookup"><span data-stu-id="a2108-108">Set the **PartitionbyOU** WMI property to group Address Book entries by organizational unit (OU).</span></span>

  - <span data-ttu-id="a2108-109">Personnalisé les règles de normalisation du carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="a2108-109">Customized the Address Book normalization rules.</span></span>

  - <span data-ttu-id="a2108-110">La valeur par défaut du paramètre **UseNormalizationRules** a été remplacée par false.</span><span class="sxs-lookup"><span data-stu-id="a2108-110">Changed the default value for the **UseNormalizationRules** parameter to False.</span></span>

<span data-ttu-id="a2108-111">**Entrées du carnet d’adresses groupé**</span><span class="sxs-lookup"><span data-stu-id="a2108-111">**Grouped Address Book Entries**</span></span>

<span data-ttu-id="a2108-112">Si vous définissez la propriété WMI **PartitionbyOU** sur true pour créer des carnets d’adresses pour chaque unité d’organisation, vous devez configurer l’attribut Active Directory **msRTCSIP-GroupingId** sur les utilisateurs et les contacts si vous voulez continuer à regrouper les entrées du carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="a2108-112">If you set the **PartitionbyOU** WMI property to True to create address books for each OU, you need to set the **msRTCSIP-GroupingId** Active Directory attribute on users and contacts if you want to continue grouping address book entries.</span></span> <span data-ttu-id="a2108-113">Il est possible que vous souhaitiez regrouper les entrées du carnet d’adresses afin de limiter l’étendue des recherches dans le carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="a2108-113">You might want to group address book entries to limit the scope of Address Book searches.</span></span> <span data-ttu-id="a2108-114">Pour utiliser l’attribut **msRTCSIP-GroupingId** , écrivez un script pour remplir l’attribut, en attribuant la même valeur à tous les utilisateurs que vous voulez regrouper.</span><span class="sxs-lookup"><span data-stu-id="a2108-114">To use the **msRTCSIP-GroupingId** attribute, write a script to populate the attribute, assigning the same value for all of the users that you want to group together.</span></span> <span data-ttu-id="a2108-115">Par exemple, attribuez une valeur unique à tous les utilisateurs d’une unité d’organisation.</span><span class="sxs-lookup"><span data-stu-id="a2108-115">For example, assign a single value for all the users in an OU.</span></span>

<span data-ttu-id="a2108-116">**Règles de normalisation du carnet d’adresses**</span><span class="sxs-lookup"><span data-stu-id="a2108-116">**Address Book Normalization Rules**</span></span>

<span data-ttu-id="a2108-117">Si vous avez personnalisé des règles de normalisation du carnet d’adresses dans votre environnement Lync Server 2010, vous devez migrer les règles personnalisées vers votre pool de pilotes.</span><span class="sxs-lookup"><span data-stu-id="a2108-117">If you customized Address Book normalization rules in your Lync Server 2010 environment, you must migrate the customized rules to your pilot pool.</span></span> <span data-ttu-id="a2108-118">Si vous n’avez pas personnalisé les règles de normalisation du carnet d’adresses, vous n’avez rien à migrer pour le service de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="a2108-118">If you did not customize Address Book normalization rules, you have nothing to migrate for Address Book service.</span></span> <span data-ttu-id="a2108-119">Les règles de normalisation par défaut de Lync Server 2013 sont les mêmes que celles par défaut de Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="a2108-119">The default normalization rules for Lync Server 2013 are the same as the default rules for Lync Server 2010.</span></span> <span data-ttu-id="a2108-120">Suivez la procédure décrite plus loin dans cette section pour migrer des règles de normalisation personnalisées.</span><span class="sxs-lookup"><span data-stu-id="a2108-120">Follow the procedure later in this section to migrate customized normalization rules.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a2108-121">Si votre organisation utilise le contrôle d’appel distant et que vous avez personnalisé des règles de normalisation du carnet d’adresses, vous devez effectuer la procédure décrite dans cette rubrique avant de pouvoir utiliser le contrôle d’appel distant.</span><span class="sxs-lookup"><span data-stu-id="a2108-121">If your organization uses remote call control and you customized Address Book normalization rules, you must perform the procedure in this topic before you can use remote call control.</span></span> <span data-ttu-id="a2108-122">Cette procédure requiert l’appartenance au groupe RTCUniversalServerAdmins ou aux droits équivalents.</span><span class="sxs-lookup"><span data-stu-id="a2108-122">The procedure requires membership in the RTCUniversalServerAdmins group or equivalent rights.</span></span>



</div>

<span data-ttu-id="a2108-123">**UseNormalizationRules défini sur false**</span><span class="sxs-lookup"><span data-stu-id="a2108-123">**UseNormalizationRules Set to False**</span></span>

<span data-ttu-id="a2108-124">Si vous définissez la valeur de **UseNormalizationRules** sur false pour que les utilisateurs puissent utiliser les numéros de téléphone tels qu’ils sont définis dans les services de domaine Active Directory (AD FS) sans que Lync Server 2013 applique des règles de normalisation, vous devez définir les paramètres **UseNormalizationRules** et **IgnoreGenericRules** sur true.</span><span class="sxs-lookup"><span data-stu-id="a2108-124">If you set the value for **UseNormalizationRules** to False so that users can use phone numbers as they are defined in Active Directory Domain Services without having Lync Server 2013 apply normalization rules, you need to set the **UseNormalizationRules** and **IgnoreGenericRules** parameters to True.</span></span> <span data-ttu-id="a2108-125">Suivez la procédure décrite plus loin dans cette section pour définir ces paramètres sur true.</span><span class="sxs-lookup"><span data-stu-id="a2108-125">Follow the procedure later in this section to set these parameters to True.</span></span>

<div>

## <a name="to-migrate-address-book-customized-normalization-rules"></a><span data-ttu-id="a2108-126">Pour migrer des règles de normalisation personnalisées du carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="a2108-126">To migrate Address Book customized normalization rules</span></span>

1.  <span data-ttu-id="a2108-127">Recherchez la \_ normalisation des \_ numéros de téléphone de l’entreprise \_ \_Rules.txt fichier à la racine du dossier partagé du carnet d’adresses, puis copiez-le à la racine du dossier partagé du carnet d’adresses dans votre pool de pilotes 2013 de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="a2108-127">Find the Company\_Phone\_Number\_Normalization\_Rules.txt file in the root of the Address Book shared folder, and copy it to the root of the Address Book shared folder in your Lync Server 2013 pilot pool.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="a2108-128">Les règles de normalisation de votre carnet d’adresses sont installées dans votre répertoire de fichiers de composants Web ABS.</span><span class="sxs-lookup"><span data-stu-id="a2108-128">The sample Address Book normalization rules have been installed in your ABS Web component file directory.</span></span> <span data-ttu-id="a2108-129">Le chemin d’accès est <STRONG>$installedDriveLetter : \Program Files\Microsoft Lync Server 2013 \ Web Components\Address Book Files\Files\ Sample_Company_Phone_Number_Normalization_Rules.txt,</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="a2108-129">The path is <STRONG>$installedDriveLetter:\Program Files\Microsoft Lync Server 2013\Web Components\Address Book Files\Files\ Sample_Company_Phone_Number_Normalization_Rules.txt,</STRONG>.</span></span> <span data-ttu-id="a2108-130">Ce fichier peut être copié et renommé en tant que &nbsp; <STRONG>Company_Phone_Number_Normalization_Rules.txt</STRONG> &nbsp; dans le répertoire racine du dossier partagé du carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="a2108-130">This file can be copied and renamed as &nbsp;<STRONG>Company_Phone_Number_Normalization_Rules.txt</STRONG> &nbsp;to the address book shared folder’s root directory.</span></span> <span data-ttu-id="a2108-131">Par exemple, dans le carnet d’adresses partagé dans <STRONG>$serverX</STRONG>, &nbsp; le chemin d’accès est semblable à ce qui suit : <STRONG> \\ $serverX \LyncFileShare\2-WebServices-1\ABFiles</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="a2108-131">For example, the address book shared in <STRONG>$serverX</STRONG>,&nbsp;the path will be similar to: <STRONG>\\$serverX \LyncFileShare\2-WebServices-1\ABFiles</STRONG>.</span></span>

    
    </div>

2.  <span data-ttu-id="a2108-132">Utilisez un éditeur de texte, tel que le bloc-notes, pour ouvrir le \_ \_ fichierRules.txt le numéro de téléphone de l’entreprise \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="a2108-132">Use a text editor, such as Notepad, to open the Company\_Phone\_Number\_Normalization\_Rules.txt file.</span></span>

3.  <span data-ttu-id="a2108-133">Certains types d’entrée ne fonctionnent pas correctement dans Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a2108-133">Certain types of entries will not work correctly in Lync Server 2013.</span></span> <span data-ttu-id="a2108-134">Parcourez le fichier pour obtenir les types d’entrée décrits dans cette étape, modifiez-les comme vous le souhaitez et enregistrez les modifications apportées au dossier partagé du carnet d’adresses dans votre pool de pilotes.</span><span class="sxs-lookup"><span data-stu-id="a2108-134">Look through the file for the types of entries described in this step, edit them as necessary, and save the changes to the Address Book shared folder in your pilot pool.</span></span>
    
    <span data-ttu-id="a2108-135">Les chaînes qui comprennent des espaces blancs ou des signes de ponctuation peuvent entraîner l’échec des règles de normalisation, car ces caractères sont supprimés de la chaîne qui est en entrée dans les règles de normalisation.</span><span class="sxs-lookup"><span data-stu-id="a2108-135">Strings that include required whitespace or punctuation cause normalization rules to fail because these characters are stripped out of the string that is input to the normalization rules.</span></span> <span data-ttu-id="a2108-136">Si vous avez des chaînes qui incluent des espaces blancs ou des signes de ponctuation requis, vous devez modifier les chaînes.</span><span class="sxs-lookup"><span data-stu-id="a2108-136">If you have strings that include required whitespace or punctuation, you need to modify the strings.</span></span> <span data-ttu-id="a2108-137">Par exemple, la chaîne suivante entraînera l’échec de la règle de normalisation :</span><span class="sxs-lookup"><span data-stu-id="a2108-137">For example, the following string would cause the normalization rule to fail:</span></span>
    
        \s*\(\s*\d\d\d\s*\)\s*\-\s*\d\d\d\s*\-\s*\d\d\d\d
    
    <span data-ttu-id="a2108-138">La chaîne suivante n’entraînera pas l’échec de la règle de normalisation :</span><span class="sxs-lookup"><span data-stu-id="a2108-138">The following string would not cause the normalization rule to fail:</span></span>
    
        \s*\(?\s*\d\d\d\s*\)?\s*\-?\s*\d\d\d\s*\-?\s*\d\d\d\d

</div>

<div>

## <a name="to-set-usenormalizationrules-and-ignoregenericrules-to-true"></a><span data-ttu-id="a2108-139">Pour définir UseNormalizationRules et IgnoreGenericRules sur true</span><span class="sxs-lookup"><span data-stu-id="a2108-139">To set UseNormalizationRules and IgnoreGenericRules to true</span></span>

1.  <span data-ttu-id="a2108-140">Démarrez Lync Server Management Shell : cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="a2108-140">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="a2108-141">Effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="a2108-141">Do one of the following:</span></span>
    
      - <span data-ttu-id="a2108-142">Si votre déploiement inclut uniquement Lync Server 2013, exécutez l’applet de commande suivante au niveau global pour modifier les valeurs de **UseNormalizationRules** et **IgnoreGenericRules** sur true :</span><span class="sxs-lookup"><span data-stu-id="a2108-142">If your deployment includes only Lync Server 2013, run the following cmdlet at the global level to change the values for **UseNormalizationRules** and **IgnoreGenericRules** to True:</span></span>
        
            Set-CsAddressBookConfiguration -identity <XdsIdentity> -UseNormalizationRules=$true -IgnoreGenericRules=$true
    
      - <span data-ttu-id="a2108-143">Si votre déploiement inclut une combinaison de Lync Server 2013 et de Lync Server 2010 ou Office Communications Server 2007 R2, exécutez l’applet de commande suivante et affectez-la à chaque pool Lync Server 2013 dans la topologie :</span><span class="sxs-lookup"><span data-stu-id="a2108-143">If your deployment includes a combination of Lync Server 2013 and Lync Server 2010 or Office Communications Server 2007 R2, run the following cmdlet and assign it to each Lync Server 2013 pool in the topology:</span></span>
        
            New-CsAddressBookConfiguration -identity <XdsIdentity> -UseNormalizationRules=$true -IgnoreGenericRules=$true

3.  <span data-ttu-id="a2108-144">Attendez la fin de la réplication du magasin de gestion centrale sur tous les pools.</span><span class="sxs-lookup"><span data-stu-id="a2108-144">Wait for Central Management store replication to occur on all pools.</span></span>

4.  <span data-ttu-id="a2108-145">Modifiez le fichier de règles de normalisation du téléphone, \_ « \_ \_ \_Rules.txt de normalisation des numéros de téléphone de l’entreprise », pour que votre déploiement efface le contenu.</span><span class="sxs-lookup"><span data-stu-id="a2108-145">Modify the phone normalization rules file, "Company\_Phone\_Number\_Normalization\_Rules.txt", for your deployment to clear the content.</span></span> <span data-ttu-id="a2108-146">Le fichier se trouve sur le partage de fichiers de chaque pool Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a2108-146">The file is on the file share of each Lync Server 2013 pool.</span></span> <span data-ttu-id="a2108-147">Si le fichier n’est pas présent, créez-en un dans la zone nom de la normalisation du numéro de téléphone de l’entreprise \_ \_ \_ \_Rules.txt</span><span class="sxs-lookup"><span data-stu-id="a2108-147">If the file is not present, then create an empty file named "Company\_Phone\_Number\_Normalization\_Rules.txt".</span></span>

5.  <span data-ttu-id="a2108-148">Attendez quelques minutes pour que tous les pools du serveur principal lisent les nouveaux fichiers.</span><span class="sxs-lookup"><span data-stu-id="a2108-148">Wait several minutes for all Front End pools to read the new files.</span></span>

6.  <span data-ttu-id="a2108-149">Exécutez l’applet de commande suivante sur chaque pool Lync Server 2013 dans votre déploiement :</span><span class="sxs-lookup"><span data-stu-id="a2108-149">Run the following cmdlet on each Lync Server 2013 pool in your deployment:</span></span>
    
        Update-CsAddressBook

<span data-ttu-id="a2108-150"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a2108-150"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

