---
title: 'Lync Server 2013 : Demande des certificats à l’avance (facultatif)'
description: 'Lync Server 2013 : demander des certificats à l’avance (facultatif).'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Request certificates in advance (optional)
ms:assetid: 9d6d7de6-ff2a-46da-b1b7-a354c8e383e4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412733(v=OCS.15)
ms:contentKeyID: 48184915
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7d92ac9b68012487d07f25f08649689611117202
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442718"
---
# <a name="request-certificates-in-advance-optional-for-lync-server-2013"></a><span data-ttu-id="7b6ce-103">Demande des certificats à l’avance (facultatif) pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7b6ce-103">Request certificates in advance (optional) for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7b6ce-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7b6ce-104">

<span> </span></span></span>

<span data-ttu-id="7b6ce-105">_**Dernière modification de la rubrique :** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="7b6ce-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="7b6ce-106">Des certificats sont requis pour tous les serveurs internes exécutant Lync Server 2013, y compris chaque serveur principal Enterprise Edition, Standard Edition Server, directeur, serveur Edge et serveur de médiation autonome.</span><span class="sxs-lookup"><span data-stu-id="7b6ce-106">Certificates are required for all internal servers that are running Lync Server 2013, including each Enterprise Edition Front End Server, Standard Edition server, Director, Edge Server and stand-alone Mediation Server.</span></span> <span data-ttu-id="7b6ce-107">Même si une autorité de certification d’entreprise interne est recommandée pour les serveurs internes, vous pouvez également utiliser une autorité de certification publique.</span><span class="sxs-lookup"><span data-stu-id="7b6ce-107">Although an internal enterprise certification authority (CA) is recommended for internal servers, you can also use a public CA.</span></span> <span data-ttu-id="7b6ce-108">Pour plus d’informations sur les exigences relatives aux certificats et sur l’utilisation d’une autorité de certification publique, voir la [Configuration requise pour les serveurs internes dans Lync Server 2013](lync-server-2013-certificate-requirements-for-internal-servers.md) dans la documentation de planification.</span><span class="sxs-lookup"><span data-stu-id="7b6ce-108">For details about certificate requirements and about the use of a public CA, see [Certificate requirements for internal servers in Lync Server 2013](lync-server-2013-certificate-requirements-for-internal-servers.md) in the Planning documentation.</span></span>

<span data-ttu-id="7b6ce-109">Le programme d’installation de Lync Server 2013 inclut l’Assistant certificat, qui facilite la tâche de demande, d’attribution et d’installation de certificats lors du déploiement.</span><span class="sxs-lookup"><span data-stu-id="7b6ce-109">Lync Server 2013 setup includes the Certificate Wizard, which facilitates the tasks of requesting, assigning, and installing certificates during deployment.</span></span> <span data-ttu-id="7b6ce-110">Si vous souhaitez demander des certificats avant d’installer des serveurs (par exemple, pour gagner du temps au cours du déploiement réel des serveurs), vous pouvez le faire à l’aide d’un ordinateur sur lequel sont installés les outils d’administration de Lync Server 2013 ou à l’aide d’une procédure de demande de certificat définie au sein de votre organisation, à condition que les certificats soient exportés et contiennent tous</span><span class="sxs-lookup"><span data-stu-id="7b6ce-110">If you want to request certificates prior to installing servers (for instance, to save time during actual deployment of servers), you can do so by using a computer on which the Lync Server 2013 administrative tools are installed or by using a certificate request procedure defined in your organization, as long as you make sure that the certificates are exportable and contain all the required subject alternative names.</span></span> <span data-ttu-id="7b6ce-111">La demande de certificats à l’avance est facultative.</span><span class="sxs-lookup"><span data-stu-id="7b6ce-111">Requesting certificates in advance is optional.</span></span> <span data-ttu-id="7b6ce-112">Dans le cas contraire, vous devez les demander dans le cadre de l’installation de chaque serveur nécessitant un certificat.</span><span class="sxs-lookup"><span data-stu-id="7b6ce-112">If you do not request them in advance, you must request them as part of the setup of each server that requires a certificate.</span></span>

<span data-ttu-id="7b6ce-113">Cette documentation de déploiement fournit des procédures d’utilisation de l’Assistant Certificat pour demander des certificats dans le cadre du processus d’installation, comme décrit dans la rubrique [configurer des certificats pour les serveurs dans Lync server 2013](lync-server-2013-configure-certificates-for-servers.md), [configurer des certificats pour le directeur dans Lync Server 2013](lync-server-2013-configure-certificates-for-the-director.md)et [installer les fichiers pour le serveur de médiation dans les sections Lync Server 2013](lync-server-2013-install-the-files-for-mediation-server.md) de cette documentation de déploiement.</span><span class="sxs-lookup"><span data-stu-id="7b6ce-113">This Deployment documentation provides procedures for using the Certificate Wizard to request certificates as part of the setup process, as described in the [Configure certificates for servers in Lync Server 2013](lync-server-2013-configure-certificates-for-servers.md), [Configure certificates for the Director in Lync Server 2013](lync-server-2013-configure-certificates-for-the-director.md), and [Install the files for Mediation Server in Lync Server 2013](lync-server-2013-install-the-files-for-mediation-server.md) sections of this Deployment documentation.</span></span> <span data-ttu-id="7b6ce-114">Si vous demandez des certificats à l’avance, vous devez modifier les procédures de déploiement des certificats dans ces sections selon les besoins en matière d’importation et d’attribution de certificats au lieu de les demander au moment du déploiement.</span><span class="sxs-lookup"><span data-stu-id="7b6ce-114">If you request certificates in advance, you must modify the certificate deployment procedures in those sections as appropriate to importing and assigning the certificates instead of requesting them at the time of deployment.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="7b6ce-115">Lync Server 2013 inclut la prise en charge des certificats SHA-256 pour les connexions de clients exécutant les systèmes d’exploitation Windows Vista, Windows Server &nbsp; 2008, Windows server &nbsp; 2008 &nbsp; R2 et Windows 7 et Lync Phone Edition.</span><span class="sxs-lookup"><span data-stu-id="7b6ce-115">Lync Server 2013 includes support for SHA-256 certificates for connections from clients running the Windows Vista, Windows Server&nbsp;2008, Windows Server&nbsp;2008&nbsp;R2, and Windows 7 operating systems, and Lync Phone Edition.</span></span> <span data-ttu-id="7b6ce-116">Pour prendre en charge l’accès externe à l’aide de l’algorithme SHA-256, le certificat externe est émis par une autorité de certification publique utilisant SHA-256.</span><span class="sxs-lookup"><span data-stu-id="7b6ce-116">To support external access using SHA-256, the external certificate is issued by a public CA using SHA-256.</span></span>



<span data-ttu-id="7b6ce-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7b6ce-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

