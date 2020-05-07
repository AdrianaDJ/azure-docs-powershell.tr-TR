---
title: Azure PowerShell’e Genel Bakış | Microsoft Docs
description: Yükleme ve yapılandırma bağlantılarıyla birlikte Azure PowerShell’e genel bakış.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.manager: carmonm
ms.date: 08/31/2017
ms.openlocfilehash: 0541975e55620a8792c0d51213c4ed02ea29988f
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/05/2020
ms.locfileid: "67863419"
---
# <a name="overview-of-azure-powershell"></a><span data-ttu-id="f5a73-103">Azure PowerShell’e Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="f5a73-103">Overview of Azure PowerShell</span></span>

[!INCLUDE[az-replacing-azurerm.md](../includes/az-replacing-azurerm.md)]

<span data-ttu-id="f5a73-104">Azure PowerShell, Azure kaynaklarınızı yönetmek için [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) modelini kullanan bir dizi cmdlet sunar.</span><span class="sxs-lookup"><span data-stu-id="f5a73-104">Azure PowerShell provides a set of cmdlets that use the [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) model for managing your Azure resources.</span></span> <span data-ttu-id="f5a73-105">[Azure Cloud Shell](/azure/cloud-shell/overview) ile tarayıcınızda kullanabilir veya yerel makinenize yükleyip herhangi bir PowerShell oturumunda kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f5a73-105">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or you can install it on your local machine and use it in any PowerShell session.</span></span>

<span data-ttu-id="f5a73-106">[Cloud Shell](/azure/cloud-shell/overview)’i kullanarak Azure PowerShell’i tarayıcınızda çalıştırın veya kendi bilgisayarınıza [yükleyin](install-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="f5a73-106">Use the [Cloud Shell](/azure/cloud-shell/overview) to run the Azure PowerShell in your browser, or [install](install-azurerm-ps.md) it on own computer.</span></span> <span data-ttu-id="f5a73-107">Daha sonra, hizmeti kullanmaya başlamak için [Başlangıç](get-started-azureps.md) makalesini okuyun.</span><span class="sxs-lookup"><span data-stu-id="f5a73-107">Then read the [Get Started](get-started-azureps.md) article to begin using it.</span></span> <span data-ttu-id="f5a73-108">En son sürüm hakkında bilgi edinmek için [sürüm notlarına](release-notes-azureps.md) bakın.</span><span class="sxs-lookup"><span data-stu-id="f5a73-108">For information about the latest release, see the [release notes](release-notes-azureps.md).</span></span>

<span data-ttu-id="f5a73-109">Aşağıdaki örnekler, yaygın senaryoları Azure PowerShell ile nasıl gerçekleştireceğinizi öğrenmenize yardımcı olabilir:</span><span class="sxs-lookup"><span data-stu-id="f5a73-109">The following samples can help you learn how to perform common scenarios with Azure PowerShell:</span></span>

* [<span data-ttu-id="f5a73-110">Linux Sanal Makineleri</span><span class="sxs-lookup"><span data-stu-id="f5a73-110">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="f5a73-111">Windows Sanal Makineleri</span><span class="sxs-lookup"><span data-stu-id="f5a73-111">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="f5a73-112">Web Apps</span><span class="sxs-lookup"><span data-stu-id="f5a73-112">Web Apps</span></span>](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="f5a73-113">SQL Veritabanları</span><span class="sxs-lookup"><span data-stu-id="f5a73-113">SQL Databases</span></span>](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

## <a name="learn-powershell-basics"></a><span data-ttu-id="f5a73-114">PowerShell temel bilgilerini öğrenme</span><span class="sxs-lookup"><span data-stu-id="f5a73-114">Learn PowerShell basics</span></span>

<span data-ttu-id="f5a73-115">PowerShell'i tanımıyorsanız, PowerShell'e giriş makalesi size yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="f5a73-115">If you are unfamiliar with PowerShell, you may find an introduction to PowerShell helpful.</span></span>

* [<span data-ttu-id="f5a73-116">PowerShell’i yükleme</span><span class="sxs-lookup"><span data-stu-id="f5a73-116">Installing PowerShell</span></span>](/powershell/scripting/installing-windows-powershell)
* [<span data-ttu-id="f5a73-117">PowerShell ile betik oluşturma</span><span class="sxs-lookup"><span data-stu-id="f5a73-117">Scripting with PowerShell</span></span>](/powershell/scripting/scripting-with-windows-powershell)

<span data-ttu-id="f5a73-118">Şu videoyu da izleyebilirsiniz: [Temel PowerShell Bilgileri: (1. Bölüm) PowerShell’i Kullanmaya Başlama](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span><span class="sxs-lookup"><span data-stu-id="f5a73-118">You can also watch this video: [PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span></span>

## <a name="other-azure-powershell-modules"></a><span data-ttu-id="f5a73-119">Diğer Azure PowerShell modülleri</span><span class="sxs-lookup"><span data-stu-id="f5a73-119">Other Azure PowerShell modules</span></span>

* [<span data-ttu-id="f5a73-120">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="f5a73-120">Azure Active Directory</span></span>](/powershell/azure/active-directory/)
* [<span data-ttu-id="f5a73-121">Azure Information Protection</span><span class="sxs-lookup"><span data-stu-id="f5a73-121">Azure Information Protection</span></span>](/powershell/azure/aip/)
* [<span data-ttu-id="f5a73-122">Azure Service Fabric</span><span class="sxs-lookup"><span data-stu-id="f5a73-122">Azure Service Fabric</span></span>](/powershell/azure/service-fabric/)
* [<span data-ttu-id="f5a73-123">Azure Elastik DB</span><span class="sxs-lookup"><span data-stu-id="f5a73-123">Azure ElasticDB</span></span>](/powershell/azure/elasticdbjobs/)
