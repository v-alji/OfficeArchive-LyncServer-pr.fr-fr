---
title: 'Lync Server 2013 : personnalisation de l’installation d’un client'
description: 'Lync Server 2013 : personnalisation de l’installation du client.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Customizing client installation
ms:assetid: 5c1a85f1-5ebb-48fb-acb7-3bf46decbf80
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204934(v=OCS.15)
ms:contentKeyID: 48184254
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8dd1942c298ccbc8b6a2950baf4f24cc2f797a92
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431371"
---
# <a name="customizing-client-installation-in-lync-server-2013"></a><span data-ttu-id="7eba5-103">Personnalisation de l’installation du client dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7eba5-103">Customizing client installation in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7eba5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7eba5-104">

<span> </span></span></span>

<span data-ttu-id="7eba5-105">_**Dernière modification de la rubrique :** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="7eba5-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="7eba5-106">Les administrateurs d’entreprise peuvent personnaliser l’installation d’Office 2013 de Windows Installer (. msi) en utilisant les méthodes décrites dans cette section.</span><span class="sxs-lookup"><span data-stu-id="7eba5-106">Enterprise administrators can customize the Office 2013 Windows Installer-based (.msi) installation by using the methods discussed in this section.</span></span> <span data-ttu-id="7eba5-107">Dans la mesure où il n’y a pas d’options de personnalisation, l’outil peut utiliser une combinaison de ces méthodes dans votre déploiement Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="7eba5-107">Because no single tool provides all customization options, you’ll likely use a combination of these methods in your Lync 2013 deployment.</span></span> <span data-ttu-id="7eba5-108">Au minimum, vous pouvez utiliser les outils décrits dans les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="7eba5-108">At a minimum, you might use the tools described in the following sections:</span></span>

  - <span data-ttu-id="7eba5-109">[À l’aide de l’outil de personnalisation Office (OPO) dans Lync Server 2013](lync-server-2013-using-the-office-customization-tool-oct.md) pour personnaliser les options et fonctionnalités de configuration pour Lync et d’autres programmes Office.</span><span class="sxs-lookup"><span data-stu-id="7eba5-109">[Using the Office Customization Tool (OCT) in Lync Server 2013](lync-server-2013-using-the-office-customization-tool-oct.md) to customize setup options and features for Lync and other Office programs.</span></span>

  - <span data-ttu-id="7eba5-110">À [l’aide de Config.xml pour effectuer des tâches d’installation dans Lync Server 2013](lync-server-2013-using-config-xml-to-perform-installation-tasks.md) , spécifiez le chemin d’accès du point d’installation réseau et effectuez une installation silencieuse.</span><span class="sxs-lookup"><span data-stu-id="7eba5-110">[Using Config.xml to perform installation tasks in Lync Server 2013](lync-server-2013-using-config-xml-to-perform-installation-tasks.md) to specify the path of the network installation point and perform silent installation.</span></span>

  - <span data-ttu-id="7eba5-111">Vous pouvez utiliser les [options de la ligne de commande du programme d’installation dans Lync Server 2013](lync-server-2013-using-setup-command-line-options.md) pour spécifier le fichier Config.xml à utiliser lors de l’installation.</span><span class="sxs-lookup"><span data-stu-id="7eba5-111">[Using Setup command-line options in Lync Server 2013](lync-server-2013-using-setup-command-line-options.md) to specify the Config.xml file to use during installation.</span></span>

  - <span data-ttu-id="7eba5-112">[Configuration des stratégies de démarrage de clients dans Lync Server 2013](lync-server-2013-configuring-client-bootstrapping-policies.md) à l’aide du composant logiciel enfichable Éditeur d’objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="7eba5-112">[Configuring client bootstrapping policies in Lync Server 2013](lync-server-2013-configuring-client-bootstrapping-policies.md) by using the Group Policy Object Editor MMC snap-in.</span></span>

<span data-ttu-id="7eba5-113">Lors du déploiement de la suite de produits Office, il est probable que vous souhaitiez configurer d’autres options.</span><span class="sxs-lookup"><span data-stu-id="7eba5-113">There will probably be other options you’ll want to configure as you deploy the Office suite of products.</span></span> <span data-ttu-id="7eba5-114">Les rubriques de cette section donnent un aperçu de ces outils de personnalisation et présentent des considérations spécifiques à Lync.</span><span class="sxs-lookup"><span data-stu-id="7eba5-114">The topics in this section give an overview of these customization tools and discuss Lync-specific considerations.</span></span> <span data-ttu-id="7eba5-115">Vous trouverez également des liens vers l’aide détaillée d’Office pour chaque outil.</span><span class="sxs-lookup"><span data-stu-id="7eba5-115">Included are links to detailed Office help for each tool.</span></span>

<span data-ttu-id="7eba5-116"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7eba5-116"></div>

<span> </span>

</div>

</div>

</span></span></div>

