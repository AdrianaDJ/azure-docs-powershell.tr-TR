---
title: Azure PowerShell’e Genel Bakış | Microsoft Docs
description: Yükleme ve yapılandırma bağlantılarıyla birlikte Azure PowerShell’e genel bakış.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.manager: carmonm
ms.date: 08/31/2017
ms.openlocfilehash: ff973378a92e834e9f9b880c6154c2b997b67cda
ms.sourcegitcommit: 5971c92cb023bdd1d71fa2ad0a3b378abfbd092a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/23/2018
---
# <a name="overview-of-azure-powershell"></a><span data-ttu-id="bf5c3-103">Azure PowerShell’e Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="bf5c3-103">Overview of Azure PowerShell</span></span>

<span data-ttu-id="bf5c3-104">Azure PowerShell, Azure kaynaklarınızı yönetmek için [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) modelini kullanan bir dizi cmdlet sunar.</span><span class="sxs-lookup"><span data-stu-id="bf5c3-104">Azure PowerShell provides a set of cmdlets that use the [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) model for managing your Azure resources.</span></span> <span data-ttu-id="bf5c3-105">[Azure Cloud Shell](/azure/cloud-shell/overview) ile tarayıcınızda kullanabilir veya yerel makinenize yükleyip herhangi bir PowerShell oturumunda kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bf5c3-105">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or you can install it on your local machine and use it in any PowerShell session.</span></span>

<span data-ttu-id="bf5c3-106">[Cloud Shell](/azure/cloud-shell/overview)’i kullanarak Azure PowerShell’i tarayıcınızda çalıştırın veya kendi bilgisayarınıza [yükleyin](install-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="bf5c3-106">Use the [Cloud Shell](/azure/cloud-shell/overview) to run the Azure PowerShell in your browser, or [install](install-azurerm-ps.md) it on own computer.</span></span> <span data-ttu-id="bf5c3-107">Daha sonra, hizmeti kullanmaya başlamak için [Başlangıç](get-started-azureps.md) makalesini okuyun.</span><span class="sxs-lookup"><span data-stu-id="bf5c3-107">Then read the [Get Started](get-started-azureps.md) article to begin using it.</span></span> <span data-ttu-id="bf5c3-108">En son sürüm hakkında bilgi edinmek için [sürüm notlarına](release-notes-azureps.md) bakın.</span><span class="sxs-lookup"><span data-stu-id="bf5c3-108">For information about the latest release, see the [release notes](release-notes-azureps.md).</span></span>

<span data-ttu-id="bf5c3-109">Aşağıdaki örnekler, yaygın senaryoları Azure PowerShell ile nasıl gerçekleştireceğinizi öğrenmenize yardımcı olabilir:</span><span class="sxs-lookup"><span data-stu-id="bf5c3-109">The following samples can help you learn how to perform common scenarios with Azure PowerShell:</span></span>

* [<span data-ttu-id="bf5c3-110">Linux Sanal Makineleri</span><span class="sxs-lookup"><span data-stu-id="bf5c3-110">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="bf5c3-111">Windows Sanal Makineleri</span><span class="sxs-lookup"><span data-stu-id="bf5c3-111">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="bf5c3-112">Web Apps</span><span class="sxs-lookup"><span data-stu-id="bf5c3-112">Web Apps</span></span>](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="bf5c3-113">SQL Veritabanları</span><span class="sxs-lookup"><span data-stu-id="bf5c3-113">SQL Databases</span></span>](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

> [!NOTE]
> <span data-ttu-id="bf5c3-114">Dönüştürülemeyen klasik dağıtım modelini kullanan dağıtımlarınız varsa, Azure PowerShell'in Hizmet Yönetimi sürümünü yükleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bf5c3-114">If you have deployments that use the classic deployment model that cannot be converted, you can install the Service Management version of Azure PowerShell.</span></span> <span data-ttu-id="bf5c3-115">Daha fazla bilgi için bkz. [Azure PowerShell Hizmet Yönetimi modülünü yükleme](/powershell/azure/servicemanagement/install-azure-ps).</span><span class="sxs-lookup"><span data-stu-id="bf5c3-115">For more information, see [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span>

### <a name="need-help-with-powershell"></a><span data-ttu-id="bf5c3-116">PowerShell konusunda yardıma mı ihtiyacınız var?</span><span class="sxs-lookup"><span data-stu-id="bf5c3-116">Need help with PowerShell?</span></span>

<span data-ttu-id="bf5c3-117">PowerShell'i tanımıyorsanız, PowerShell'e giriş makalesi size yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="bf5c3-117">If you are unfamiliar with PowerShell, you may find an introduction to PowerShell helpful.</span></span>

* [<span data-ttu-id="bf5c3-118">PowerShell’i yükleme</span><span class="sxs-lookup"><span data-stu-id="bf5c3-118">Installing PowerShell</span></span>](/powershell/scripting/installing-windows-powershell)
* [<span data-ttu-id="bf5c3-119">PowerShell ile betik oluşturma</span><span class="sxs-lookup"><span data-stu-id="bf5c3-119">Scripting with PowerShell</span></span>](/powershell/scripting/scripting-with-windows-powershell)

<span data-ttu-id="bf5c3-120">Şu videoyu da izleyebilirsiniz: [Temel PowerShell Bilgileri: (1. Bölüm) PowerShell’i Kullanmaya Başlama](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span><span class="sxs-lookup"><span data-stu-id="bf5c3-120">You can also watch this video: [PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span></span>

<span data-ttu-id="bf5c3-121">Dilerseniz Microsoft Sanal Akademi’nin [PowerShell Jumpstart’ı Kullanmaya Başlama](https://mva.microsoft.com/liveevents/powershell-jumpstart) etkinliğine de katılabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bf5c3-121">Or attend the Microsoft Virtual Academy's [Getting Started with PowerShell Jumpstart](https://mva.microsoft.com/liveevents/powershell-jumpstart).</span></span>

## <a name="other-azure-powershell-modules"></a><span data-ttu-id="bf5c3-122">Diğer Azure PowerShell modülleri</span><span class="sxs-lookup"><span data-stu-id="bf5c3-122">Other Azure PowerShell modules</span></span>

* [<span data-ttu-id="bf5c3-123">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="bf5c3-123">Azure Active Directory</span></span>](/powershell/azure/active-directory/)
* [<span data-ttu-id="bf5c3-124">Azure Information Protection</span><span class="sxs-lookup"><span data-stu-id="bf5c3-124">Azure Information Protection</span></span>](/powershell/azure/aip/)
* [<span data-ttu-id="bf5c3-125">Azure Service Fabric</span><span class="sxs-lookup"><span data-stu-id="bf5c3-125">Azure Service Fabric</span></span>](/powershell/azure/service-fabric/)
* [<span data-ttu-id="bf5c3-126">Azure Elastik DB</span><span class="sxs-lookup"><span data-stu-id="bf5c3-126">Azure ElasticDB</span></span>](/powershell/azure/elasticdbjobs/)