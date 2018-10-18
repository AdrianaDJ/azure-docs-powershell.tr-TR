---
title: Azure PowerShell’e Genel Bakış | Microsoft Docs
description: Yükleme ve yapılandırma bağlantılarıyla birlikte Azure PowerShell’e genel bakış.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.manager: carmonm
ms.date: 09/11/2018
ms.openlocfilehash: f03243f6f560407b63aff154494cf164d670d810
ms.sourcegitcommit: f6f5e256143aa6c097de3e57e930d8badea49f30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/18/2018
ms.locfileid: "49398898"
---
# <a name="overview-of-azure-powershell"></a><span data-ttu-id="97a16-103">Azure PowerShell’e Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="97a16-103">Overview of Azure PowerShell</span></span>

<span data-ttu-id="97a16-104">Azure PowerShell, Azure kaynaklarınızı yönetmek için [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) modelini kullanan bir dizi cmdlet sunar.</span><span class="sxs-lookup"><span data-stu-id="97a16-104">Azure PowerShell provides a set of cmdlets that use the [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) model for managing your Azure resources.</span></span> <span data-ttu-id="97a16-105">[Azure Cloud Shell](/azure/cloud-shell/overview) ile tarayıcınızda kullanabilir veya yerel makinenize yükleyip herhangi bir PowerShell oturumunda kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="97a16-105">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or you can install it on your local machine and use it in any PowerShell session.</span></span>

<span data-ttu-id="97a16-106">[Cloud Shell](/azure/cloud-shell/overview)’i kullanarak Azure PowerShell’i tarayıcınızda çalıştırın veya kendi bilgisayarınıza [yükleyin](install-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="97a16-106">Use the [Cloud Shell](/azure/cloud-shell/overview) to run the Azure PowerShell in your browser, or [install](install-azurerm-ps.md) it on own computer.</span></span> <span data-ttu-id="97a16-107">Daha sonra, hizmeti kullanmaya başlamak için [Başlangıç](get-started-azureps.md) makalesini okuyun.</span><span class="sxs-lookup"><span data-stu-id="97a16-107">Then read the [Get Started](get-started-azureps.md) article to begin using it.</span></span> <span data-ttu-id="97a16-108">En son sürüm hakkında bilgi edinmek için [sürüm notlarına](release-notes-azureps.md) bakın.</span><span class="sxs-lookup"><span data-stu-id="97a16-108">For information about the latest release, see the [release notes](release-notes-azureps.md).</span></span>

<span data-ttu-id="97a16-109">Aşağıdaki örnekler, yaygın senaryoları Azure PowerShell ile nasıl gerçekleştireceğinizi öğrenmenize yardımcı olabilir:</span><span class="sxs-lookup"><span data-stu-id="97a16-109">The following samples can help you learn how to perform common scenarios with Azure PowerShell:</span></span>

* [<span data-ttu-id="97a16-110">Linux Sanal Makineleri</span><span class="sxs-lookup"><span data-stu-id="97a16-110">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="97a16-111">Windows Sanal Makineleri</span><span class="sxs-lookup"><span data-stu-id="97a16-111">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="97a16-112">Web Apps</span><span class="sxs-lookup"><span data-stu-id="97a16-112">Web Apps</span></span>](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="97a16-113">SQL Veritabanları</span><span class="sxs-lookup"><span data-stu-id="97a16-113">SQL Databases</span></span>](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

> [!NOTE]
> <span data-ttu-id="97a16-114">Dönüştürülemeyen klasik dağıtım modelini kullanan dağıtımlarınız varsa, Azure PowerShell'in Hizmet Yönetimi sürümünü yükleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="97a16-114">If you have deployments that use the classic deployment model that cannot be converted, you can install the Service Management version of Azure PowerShell.</span></span> <span data-ttu-id="97a16-115">Daha fazla bilgi için bkz. [Azure PowerShell Hizmet Yönetimi modülünü yükleme](/powershell/azure/servicemanagement/install-azure-ps).</span><span class="sxs-lookup"><span data-stu-id="97a16-115">For more information, see [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span>

## <a name="learn-powershell-basics"></a><span data-ttu-id="97a16-116">PowerShell temel bilgilerini öğrenme</span><span class="sxs-lookup"><span data-stu-id="97a16-116">Learn PowerShell basics</span></span>

<span data-ttu-id="97a16-117">PowerShell'i tanımıyorsanız, PowerShell'e giriş bilgileri size yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="97a16-117">If you're unfamiliar with PowerShell, an introduction to PowerShell may be helpful.</span></span>

* [<span data-ttu-id="97a16-118">PowerShell’i yükleme</span><span class="sxs-lookup"><span data-stu-id="97a16-118">Installing PowerShell</span></span>](/powershell/scripting/setup/installing-windows-powershell)
* [<span data-ttu-id="97a16-119">PowerShell ile betik oluşturma</span><span class="sxs-lookup"><span data-stu-id="97a16-119">Scripting with PowerShell</span></span>](/powershell/scripting/powershell-scripting)

<span data-ttu-id="97a16-120">Şu videoyu da izleyebilirsiniz: [Temel PowerShell Bilgileri: (1. Bölüm) PowerShell’i Kullanmaya Başlama](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span><span class="sxs-lookup"><span data-stu-id="97a16-120">You can also watch this video: [PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span></span>

<span data-ttu-id="97a16-121">Dilerseniz Microsoft Sanal Akademi’nin [PowerShell Jumpstart’ı Kullanmaya Başlama](https://mva.microsoft.com/liveevents/powershell-jumpstart) etkinliğine de katılabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="97a16-121">Or attend the Microsoft Virtual Academy's [Getting Started with PowerShell Jumpstart](https://mva.microsoft.com/liveevents/powershell-jumpstart).</span></span>

## <a name="build-your-skills-with-microsoft-learn"></a><span data-ttu-id="97a16-122">Microsoft Learn ile becerilerinizi geliştirin</span><span class="sxs-lookup"><span data-stu-id="97a16-122">Build your skills with Microsoft Learn</span></span>

- [<span data-ttu-id="97a16-123">PowerShell betiklerini kullanarak Azure görevlerini otomatikleştirme</span><span class="sxs-lookup"><span data-stu-id="97a16-123">Automate Azure tasks using scripts with PowerShell</span></span>](/learn/modules/automate-azure-tasks-with-powershell/)
- [<span data-ttu-id="97a16-124">Daha fazla etkileşimli öğrenme içeriği...</span><span class="sxs-lookup"><span data-stu-id="97a16-124">More interactive learning...</span></span>](/learn/browse/?term=powershell)

## <a name="other-azure-powershell-modules"></a><span data-ttu-id="97a16-125">Diğer Azure PowerShell modülleri</span><span class="sxs-lookup"><span data-stu-id="97a16-125">Other Azure PowerShell modules</span></span>

* [<span data-ttu-id="97a16-126">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="97a16-126">Azure Active Directory</span></span>](/powershell/azure/active-directory/)
* [<span data-ttu-id="97a16-127">Azure Information Protection</span><span class="sxs-lookup"><span data-stu-id="97a16-127">Azure Information Protection</span></span>](/powershell/azure/aip/)
* [<span data-ttu-id="97a16-128">Azure Service Fabric</span><span class="sxs-lookup"><span data-stu-id="97a16-128">Azure Service Fabric</span></span>](/powershell/azure/service-fabric/)
* [<span data-ttu-id="97a16-129">Azure Elastik DB</span><span class="sxs-lookup"><span data-stu-id="97a16-129">Azure ElasticDB</span></span>](/powershell/azure/elasticdbjobs/)
