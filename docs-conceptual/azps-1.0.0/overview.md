---
title: Azure PowerShell’e Genel Bakış
description: Azure PowerShell Az modülünü yükleme ve kullanmaya başlama hakkında bilgiler içeren genel bir bakış.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.manager: carmonm
ms.date: 10/29/2018
ms.openlocfilehash: 7982e122d49db4d558648231d1ab8bfeed80be2d
ms.sourcegitcommit: 4acddc7026522c4fe39de2c4424917d88ee01b7e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/21/2018
ms.locfileid: "53736469"
---
# <a name="overview-of-azure-powershell"></a><span data-ttu-id="3eb19-103">Azure PowerShell’e Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="3eb19-103">Overview of Azure PowerShell</span></span>

<span data-ttu-id="3eb19-104">Azure PowerShell, Azure kaynaklarınızı yönetmek için [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) modelini kullanan bir dizi cmdlet sunar.</span><span class="sxs-lookup"><span data-stu-id="3eb19-104">Azure PowerShell provides a set of cmdlets that use the [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) model for managing your Azure resources.</span></span> <span data-ttu-id="3eb19-105">Azure PowerShell .NET Standard’ı kullandığından, Windows, macOS ve Linux’ta kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="3eb19-105">Azure PowerShell uses .NET Standard, making it available for Windows, macOS, and Linux.</span></span>
<span data-ttu-id="3eb19-106">Azure PowerShell, Azure Cloud Shell’den de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="3eb19-106">Azure PowerShell is also available from Azure Cloud Shell.</span></span>

<span data-ttu-id="3eb19-107">[Azure Cloud Shell](/azure/cloud-shell/overview)’i kullanarak Azure PowerShell’i tarayıcınızda çalıştırın veya [yerel olarak yükleyin](install-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="3eb19-107">Use [Azure Cloud Shell](/azure/cloud-shell/overview) to run Azure PowerShell in your browser, or [install locally](install-az-ps.md).</span></span> <span data-ttu-id="3eb19-108">Azure PowerShell ile ilgili temel kavramları öğrenmek ve Azure’ı kullanmaya başlamak için [Kullanmaya Başlama](get-started-azureps.md) makalesine göz atın.</span><span class="sxs-lookup"><span data-stu-id="3eb19-108">Check out the [Get Started](get-started-azureps.md) article to learn the Azure PowerShell basics and get started with Azure.</span></span>

<span data-ttu-id="3eb19-109">En son Azure PowerShell sürümü hakkında bilgi edinmek için [sürüm notlarına](release-notes-azureps.md) bakın.</span><span class="sxs-lookup"><span data-stu-id="3eb19-109">For information about the latest Azure PowerShell release, see the [release notes](release-notes-azureps.md).</span></span>

## <a name="about-the-new-az-module"></a><span data-ttu-id="3eb19-110">Yeni Az modülü hakkında</span><span class="sxs-lookup"><span data-stu-id="3eb19-110">About the new Az module</span></span>

<span data-ttu-id="3eb19-111">Bu belgede, Azure PowerShell’e yönelik yeni Az modülü açıklanır.</span><span class="sxs-lookup"><span data-stu-id="3eb19-111">This documentation describes the new Az module for Azure PowerShell.</span></span> <span data-ttu-id="3eb19-112">Bu yeni modül, en baştan itibaren .NET Standard platformunda yazılmıştır.</span><span class="sxs-lookup"><span data-stu-id="3eb19-112">This new module is written from the ground up in .NET Standard.</span></span> <span data-ttu-id="3eb19-113">.NET Standard’ın kullanılması, Azure PowerShell’in Windows’da PowerShell 5.x veya diğer tüm platformlarda PowerShell 6 altında çalışmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="3eb19-113">Using .NET Standard allows Azure PowerShell to run under PowerShell 5.x on Windows or PowerShell 6 on any platform.</span></span> <span data-ttu-id="3eb19-114">Artık PowerShell üzerinden Azure ile etkileşim kurmak için kullanılması hedeflenen yöntem Az modülüdür.</span><span class="sxs-lookup"><span data-stu-id="3eb19-114">The Az module is now the intended way to interact with Azure through PowerShell.</span></span>
<span data-ttu-id="3eb19-115">AzureRM için hata düzeltmeleri sağlanmaya devam edilecek olsa da artık yeni özellikler sağlanmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="3eb19-115">AzureRM will continue to get bug fixes, but no longer receive new features.</span></span>

<span data-ttu-id="3eb19-116">[Azure PowerShell Az modülüne giriş](new-azureps-module-az.md) makalesini okuyarak komutların nasıl yeniden adlandırıldığı ve AzureRM’ye yönelik bakım planları dahil olmak üzere yeni modülle ilgili tüm ayrıntıları öğrenin.</span><span class="sxs-lookup"><span data-stu-id="3eb19-116">Learn the full details about the new module, including how commands have been renamed and the maintenance plans for AzureRM, in the [Introducing the Azure PowerShell Az module](new-azureps-module-az.md).</span></span> <span data-ttu-id="3eb19-117">Yeni modülü hemen kullanmaya başlamak istiyorsanız bkz. [AzureRM’den Az’ye geçiş](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="3eb19-117">If you want to get started with using the new module right away, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>

<span data-ttu-id="3eb19-118">[AzureRM belgeleri](/powershell/azure/azurerm) de sağlanır.</span><span class="sxs-lookup"><span data-stu-id="3eb19-118">The [AzureRM documentation](/powershell/azure/azurerm) is also available.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="3eb19-119">Azure belgelerini yeni modüldeki cmdlet adlarını yansıtacak şekilde güncelleştirme çalışmaları sırasında makalelerde AzureRM komutları kullanılmaya devam edilebilir.</span><span class="sxs-lookup"><span data-stu-id="3eb19-119">While the Azure documentation is being updated to reflect the new module cmdlet names, articles may still use the AzureRM commands.</span></span> <span data-ttu-id="3eb19-120">Az modülünü yükledikten sonra `Enable-AzureRmAlias` ile AzureRM cmdlet'i diğer adlarını etkinleştirmeniz önerilir.</span><span class="sxs-lookup"><span data-stu-id="3eb19-120">After installing the Az module, it's recommended that you enable the AzureRM cmdlet aliases with `Enable-AzureRmAlias`.</span></span> <span data-ttu-id="3eb19-121">Daha ayrıntılı bilgi edinmek için [AzureRM’den Az’ye geçiş](migrate-from-azurerm-to-az.md) makalesine bakın.</span><span class="sxs-lookup"><span data-stu-id="3eb19-121">See the [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md) article for more details.</span></span>

## <a name="common-scenarios"></a><span data-ttu-id="3eb19-122">Genel senaryolar</span><span class="sxs-lookup"><span data-stu-id="3eb19-122">Common scenarios</span></span>

<span data-ttu-id="3eb19-123">Aşağıdaki örnekler, yaygın senaryoları Azure PowerShell ile nasıl gerçekleştireceğinizi öğrenmenize yardımcı olabilir:</span><span class="sxs-lookup"><span data-stu-id="3eb19-123">The following samples can help you learn how to perform common scenarios with Azure PowerShell:</span></span>

* [<span data-ttu-id="3eb19-124">Linux Sanal Makineleri</span><span class="sxs-lookup"><span data-stu-id="3eb19-124">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="3eb19-125">Windows Sanal Makineleri</span><span class="sxs-lookup"><span data-stu-id="3eb19-125">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="3eb19-126">Web Apps</span><span class="sxs-lookup"><span data-stu-id="3eb19-126">Web Apps</span></span>](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="3eb19-127">SQL Veritabanları</span><span class="sxs-lookup"><span data-stu-id="3eb19-127">SQL Databases</span></span>](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

## <a name="learn-powershell-basics"></a><span data-ttu-id="3eb19-128">PowerShell temel bilgilerini öğrenme</span><span class="sxs-lookup"><span data-stu-id="3eb19-128">Learn PowerShell basics</span></span>

<span data-ttu-id="3eb19-129">PowerShell'i tanımıyorsanız bir tanıtımı incelemeniz yararlı olabilir.</span><span class="sxs-lookup"><span data-stu-id="3eb19-129">If you're unfamiliar with PowerShell, an introduction may be helpful.</span></span>

* [<span data-ttu-id="3eb19-130">PowerShell’i yükleme</span><span class="sxs-lookup"><span data-stu-id="3eb19-130">Installing PowerShell</span></span>](/powershell/scripting/setup/installing-windows-powershell)
* [<span data-ttu-id="3eb19-131">PowerShell ile betik oluşturma</span><span class="sxs-lookup"><span data-stu-id="3eb19-131">Scripting with PowerShell</span></span>](/powershell/scripting/powershell-scripting)

<span data-ttu-id="3eb19-132">Ayrıca şu videoyu izleyebilirsiniz: [PowerShell Temel Bilgileri: (Bölüm 1) PowerShell'i Kullanmaya Başlama](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span><span class="sxs-lookup"><span data-stu-id="3eb19-132">You can also watch this video: [PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span></span>

<span data-ttu-id="3eb19-133">Dilerseniz Microsoft Sanal Akademi’nin [PowerShell Jumpstart’ı Kullanmaya Başlama](https://mva.microsoft.com/liveevents/powershell-jumpstart) etkinliğine de katılabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3eb19-133">Or attend the Microsoft Virtual Academy's [Getting Started with PowerShell Jumpstart](https://mva.microsoft.com/liveevents/powershell-jumpstart).</span></span>

## <a name="build-your-skills-with-microsoft-learn"></a><span data-ttu-id="3eb19-134">Microsoft Learn ile becerilerinizi geliştirin</span><span class="sxs-lookup"><span data-stu-id="3eb19-134">Build your skills with Microsoft Learn</span></span>

- [<span data-ttu-id="3eb19-135">PowerShell betiklerini kullanarak Azure görevlerini otomatikleştirme</span><span class="sxs-lookup"><span data-stu-id="3eb19-135">Automate Azure tasks using scripts with PowerShell</span></span>](/learn/modules/automate-azure-tasks-with-powershell/)
- [<span data-ttu-id="3eb19-136">Daha fazla etkileşimli öğrenme içeriği...</span><span class="sxs-lookup"><span data-stu-id="3eb19-136">More interactive learning...</span></span>](/learn/browse/?term=powershell)

## <a name="other-azure-powershell-modules"></a><span data-ttu-id="3eb19-137">Diğer Azure PowerShell modülleri</span><span class="sxs-lookup"><span data-stu-id="3eb19-137">Other Azure PowerShell modules</span></span>

* [<span data-ttu-id="3eb19-138">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="3eb19-138">Azure Active Directory</span></span>](/powershell/azure/active-directory/)
* [<span data-ttu-id="3eb19-139">Azure Information Protection</span><span class="sxs-lookup"><span data-stu-id="3eb19-139">Azure Information Protection</span></span>](/powershell/azure/aip/)
* [<span data-ttu-id="3eb19-140">Azure Service Fabric</span><span class="sxs-lookup"><span data-stu-id="3eb19-140">Azure Service Fabric</span></span>](/powershell/azure/service-fabric/)
* [<span data-ttu-id="3eb19-141">Azure Elastik DB</span><span class="sxs-lookup"><span data-stu-id="3eb19-141">Azure ElasticDB</span></span>](/powershell/azure/elasticdbjobs/)
