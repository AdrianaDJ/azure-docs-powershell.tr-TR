---
title: Azure PowerShell’e Genel Bakış
description: Azure PowerShell Az modülünü yükleme ve kullanmaya başlama hakkında bilgiler içeren genel bir bakış.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.manager: carmonm
ms.date: 01/10/2019
ms.openlocfilehash: 45ab083dd133c8c7b8dbe902484c92564bc216b9
ms.sourcegitcommit: 8f59e11e5c991543964154d63648aa1e6ae22512
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/26/2019
ms.locfileid: "58475694"
---
# <a name="overview-of-azure-powershell"></a><span data-ttu-id="fc50c-103">Azure PowerShell’e Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="fc50c-103">Overview of Azure PowerShell</span></span>

<span data-ttu-id="fc50c-104">Azure PowerShell, Azure kaynaklarınızı yönetmek için [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) modelini kullanan bir dizi cmdlet sunar.</span><span class="sxs-lookup"><span data-stu-id="fc50c-104">Azure PowerShell provides a set of cmdlets that use the [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) model for managing your Azure resources.</span></span> <span data-ttu-id="fc50c-105">Azure PowerShell'in .NET Standard’ı kullanması Windows, macOS ve Linux’ta kullanılabilmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="fc50c-105">Azure PowerShell uses .NET Standard, making it available for Windows, macOS, and Linux.</span></span>
<span data-ttu-id="fc50c-106">Azure PowerShell, Azure Cloud Shell üzerinde de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="fc50c-106">Azure PowerShell is also available on Azure Cloud Shell.</span></span>

## <a name="about-the-new-az-module"></a><span data-ttu-id="fc50c-107">Yeni Az modülü hakkında</span><span class="sxs-lookup"><span data-stu-id="fc50c-107">About the new Az module</span></span>

<span data-ttu-id="fc50c-108">Bu belgede, Azure PowerShell’e yönelik yeni Az modülü açıklanır.</span><span class="sxs-lookup"><span data-stu-id="fc50c-108">This documentation describes the new Az module for Azure PowerShell.</span></span> <span data-ttu-id="fc50c-109">Bu yeni modül, en baştan itibaren .NET Standard platformunda yazılmıştır.</span><span class="sxs-lookup"><span data-stu-id="fc50c-109">This new module is written from the ground up in .NET Standard.</span></span> <span data-ttu-id="fc50c-110">.NET Standard’ın kullanılması, Azure PowerShell’in Windows’da PowerShell 5 veya diğer tüm platformlarda PowerShell 6 altında çalışmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="fc50c-110">Using .NET Standard allows Azure PowerShell to run under PowerShell 5 on Windows or PowerShell 6 on any platform.</span></span> <span data-ttu-id="fc50c-111">Artık PowerShell üzerinden Azure ile etkileşim kurmak için kullanılması hedeflenen yöntem Az modülüdür.</span><span class="sxs-lookup"><span data-stu-id="fc50c-111">The Az module is now the intended way to interact with Azure through PowerShell.</span></span>
<span data-ttu-id="fc50c-112">AzureRM için hata düzeltmeleri sağlanmaya devam edilecek olsa da artık yeni özellikler sağlanmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="fc50c-112">AzureRM will continue to get bug fixes, but no longer receive new features.</span></span>

<span data-ttu-id="fc50c-113">[Azure PowerShell Az modülüne giriş](new-azureps-module-az.md) makalesini okuyarak komutların nasıl yeniden adlandırıldığı ve AzureRM’ye yönelik bakım planları dahil olmak üzere yeni modülle ilgili tüm ayrıntıları öğrenin.</span><span class="sxs-lookup"><span data-stu-id="fc50c-113">Learn the full details about the new module, including how commands have been renamed and the maintenance plans for AzureRM, in the [Introducing the Azure PowerShell Az module](new-azureps-module-az.md).</span></span> <span data-ttu-id="fc50c-114">Yeni modülü hemen kullanmaya başlamak istiyorsanız bkz. [AzureRM’den Az’ye geçiş](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="fc50c-114">If you want to get started with using the new module right away, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>

<span data-ttu-id="fc50c-115">[AzureRM belgeleri](/powershell/azure/azurerm) de sağlanır.</span><span class="sxs-lookup"><span data-stu-id="fc50c-115">The [AzureRM documentation](/powershell/azure/azurerm) is also available.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="fc50c-116">Azure belgelerinin yeni modüldeki cmdlet adlarını yansıtacak şekilde güncelleştirilmesi sürerken makalelerde AzureRM komutları kullanılmaya devam edilebilir.</span><span class="sxs-lookup"><span data-stu-id="fc50c-116">While the Azure documentation is being updated to reflect the new module cmdlet names, articles may still use the AzureRM commands.</span></span> <span data-ttu-id="fc50c-117">Az modülünü yükledikten sonra `Enable-AzureRmAlias` ile AzureRM cmdlet'i diğer adlarını etkinleştirmeniz önerilir.</span><span class="sxs-lookup"><span data-stu-id="fc50c-117">After installing the Az module, it's recommended that you enable the AzureRM cmdlet aliases with `Enable-AzureRmAlias`.</span></span> <span data-ttu-id="fc50c-118">Daha ayrıntılı bilgi edinmek için [AzureRM’den Az’ye geçiş](migrate-from-azurerm-to-az.md) makalesine bakın.</span><span class="sxs-lookup"><span data-stu-id="fc50c-118">See the [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md) article for more details.</span></span>

## <a name="run-or-install"></a><span data-ttu-id="fc50c-119">Çalıştırma veya yükleme</span><span class="sxs-lookup"><span data-stu-id="fc50c-119">Run or install</span></span>

<span data-ttu-id="fc50c-120">Azure PowerShell’i, Windows’da PowerShell 5.1 veya sonraki sürümlerine, diğer platformlarda PowerShell 6’ya yükleyebilir veya Azure Cloud Shell’de çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fc50c-120">You can install Azure PowerShell on PowerShell 5.1 or higher on Windows, PowerShell 6 on any platform, or run in Azure Cloud Shell.</span></span>

* <span data-ttu-id="fc50c-121">Tarayıcınızda Azure Cloud Shell ile çalıştırmak için bkz. [Azure Cloud Shell'de PowerShell için Hızlı Başlangıç](/azure/cloud-shell/quickstart-powershell).</span><span class="sxs-lookup"><span data-stu-id="fc50c-121">To run in your browser with Azure Cloud Shell, see [Quickstart for PowerShell in Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).</span></span>
* <span data-ttu-id="fc50c-122">Azure PowerShell'i sisteminize yüklemek için bkz. [Azure PowerShell'i yükleme](install-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="fc50c-122">To install Azure PowerShell on your system, see [Install Azure PowerShell](install-az-ps.md).</span></span>

<span data-ttu-id="fc50c-123">En son Azure PowerShell sürümü hakkında bilgi edinmek için [sürüm notlarına](release-notes-azureps.md) bakın.</span><span class="sxs-lookup"><span data-stu-id="fc50c-123">For information about the latest Azure PowerShell release, see the [release notes](release-notes-azureps.md).</span></span>

## <a name="get-started"></a><span data-ttu-id="fc50c-124">Başlarken</span><span class="sxs-lookup"><span data-stu-id="fc50c-124">Get Started</span></span>

<span data-ttu-id="fc50c-125">Azure PowerShell ile ilgili temel kavramları öğrenmek için [Azure PowerShell'i Kullanmaya Başlama](get-started-azureps.md) makalesini gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="fc50c-125">Read the [Get Started with Azure PowerShell](get-started-azureps.md) article to learn the Azure PowerShell basics.</span></span> <span data-ttu-id="fc50c-126">PowerShell'i tanımıyorsanız, bir tanıtımı incelemeniz yararlı olabilir:</span><span class="sxs-lookup"><span data-stu-id="fc50c-126">If you're not familiar with PowerShell, an introduction might be helpful:</span></span>

* [<span data-ttu-id="fc50c-127">PowerShell yükleme</span><span class="sxs-lookup"><span data-stu-id="fc50c-127">Install PowerShell</span></span>](/powershell/scripting/install/installing-powershell)
* [<span data-ttu-id="fc50c-128">PowerShell ile betik oluşturma</span><span class="sxs-lookup"><span data-stu-id="fc50c-128">Scripting with PowerShell</span></span>](/powershell/scripting/powershell-scripting)
* [<span data-ttu-id="fc50c-129">PowerShell Temel Bilgileri: (Bölüm 1) PowerShell'i Kullanmaya Başlama</span><span class="sxs-lookup"><span data-stu-id="fc50c-129">PowerShell Basics: (Part 1) Getting Started with PowerShell</span></span>](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1)
* <span data-ttu-id="fc50c-130">Microsoft Virtual Academy'de [PowerShell Jumpstart’ı Kullanmaya Başlama](https://mva.microsoft.com/liveevents/powershell-jumpstart)</span><span class="sxs-lookup"><span data-stu-id="fc50c-130">Microsoft Virtual Academy's [Getting Started with PowerShell Jumpstart](https://mva.microsoft.com/liveevents/powershell-jumpstart)</span></span>

<span data-ttu-id="fc50c-131">Aşağıdaki örnekler Azure'ın bazı yaygın kullanımları konusunda yardımcı olabilir:</span><span class="sxs-lookup"><span data-stu-id="fc50c-131">The following samples can help you with some common uses of Azure:</span></span>

* [<span data-ttu-id="fc50c-132">Linux Sanal Makineleri</span><span class="sxs-lookup"><span data-stu-id="fc50c-132">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="fc50c-133">Windows Sanal Makineleri</span><span class="sxs-lookup"><span data-stu-id="fc50c-133">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="fc50c-134">Web Apps</span><span class="sxs-lookup"><span data-stu-id="fc50c-134">Web Apps</span></span>](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="fc50c-135">SQL Veritabanları</span><span class="sxs-lookup"><span data-stu-id="fc50c-135">SQL Databases</span></span>](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

## <a name="build-your-skills-with-microsoft-learn"></a><span data-ttu-id="fc50c-136">Microsoft Learn ile becerilerinizi geliştirin</span><span class="sxs-lookup"><span data-stu-id="fc50c-136">Build your skills with Microsoft Learn</span></span>

- [<span data-ttu-id="fc50c-137">PowerShell betiklerini kullanarak Azure görevlerini otomatikleştirme</span><span class="sxs-lookup"><span data-stu-id="fc50c-137">Automate Azure tasks using scripts with PowerShell</span></span>](/learn/modules/automate-azure-tasks-with-powershell/)
- [<span data-ttu-id="fc50c-138">Daha fazla etkileşimli öğrenme içeriği...</span><span class="sxs-lookup"><span data-stu-id="fc50c-138">More interactive learning...</span></span>](/learn/browse/?term=powershell)

## <a name="other-azure-powershell-modules"></a><span data-ttu-id="fc50c-139">Diğer Azure PowerShell modülleri</span><span class="sxs-lookup"><span data-stu-id="fc50c-139">Other Azure PowerShell modules</span></span>

* [<span data-ttu-id="fc50c-140">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="fc50c-140">Azure Active Directory</span></span>](/powershell/azure/active-directory/)
* [<span data-ttu-id="fc50c-141">Azure Service Fabric</span><span class="sxs-lookup"><span data-stu-id="fc50c-141">Azure Service Fabric</span></span>](/powershell/azure/service-fabric/)
* [<span data-ttu-id="fc50c-142">Azure Elastik DB</span><span class="sxs-lookup"><span data-stu-id="fc50c-142">Azure ElasticDB</span></span>](/powershell/azure/elasticdbjobs/)
