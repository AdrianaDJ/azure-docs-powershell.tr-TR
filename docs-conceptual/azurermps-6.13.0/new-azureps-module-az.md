---
title: Azure PowerShell Az modülüne giriş
description: Azure PowerShell'in AzureRM modülünün yerini alan yeni Az modülüne giriş.
ms.date: 11/07/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: b0f31341d4344bdac5b4d657a1f66acfd9984dda
ms.sourcegitcommit: 558436c824d9b59731aa9b963cdc8df4dea932e7
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/29/2018
ms.locfileid: "52587321"
---
# <a name="introducing-the-new-azure-powershell-az-module"></a><span data-ttu-id="4a63f-103">Yeni Azure PowerShell Az modülüne giriş</span><span class="sxs-lookup"><span data-stu-id="4a63f-103">Introducing the new Azure PowerShell Az module</span></span>

<span data-ttu-id="4a63f-104">Kasım 2018'den başlayarak, Azure PowerShell `Az` modülü tam genel önizlemeye sunulmuştur.</span><span class="sxs-lookup"><span data-stu-id="4a63f-104">Starting in November 2018, the Azure PowerShell `Az` module is available for full public preview.</span></span>
<span data-ttu-id="4a63f-105">Az daha kısa komutlar, gelişmiş kararlılık sunar ve Windows, macOS ve Linux'ı destekler.</span><span class="sxs-lookup"><span data-stu-id="4a63f-105">Az offers shorter commands, improved stability, and supports Windows, macOS, and Linux.</span></span> <span data-ttu-id="4a63f-106">Ayrıca Az, AzureRM ile özellik eşliği ve AzureRM'den kolay geçiş yolu da sunar.</span><span class="sxs-lookup"><span data-stu-id="4a63f-106">Az also offers feature parity and an easy migration path from AzureRM.</span></span>

<span data-ttu-id="4a63f-107">Az .NET Standard kitaplığını kullanır ve bu da PowerShell 5.x ile PowerShell 6.x üzerinde çalıştığı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="4a63f-107">Az uses the .NET Standard library, which means it runs on PowerShell 5.x and PowerShell 6.x.</span></span>
<span data-ttu-id="4a63f-108">PowerShell 6.x Linux, macOS ve Windows üzerinde çalışabildiğinden, Az tüm platformlarda kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="4a63f-108">Since PowerShell 6.x can run on Linux, macOS, and Windows, that means Az is available for all platforms.</span></span>
<span data-ttu-id="4a63f-109">.NET Standard'ın kullanılması, Azure PowerShell'in kod tabanını kullanıcıları çok az etkileyerek birleştirmemize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="4a63f-109">Using .NET Standard allows us to unify the code base of Azure PowerShell with minimal impact on users.</span></span>

<span data-ttu-id="4a63f-110">Az yeni bir modüldür, dolayısıyla sürüm sıfırlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="4a63f-110">Az is a new module, so the version has been reset.</span></span> <span data-ttu-id="4a63f-111">İlk kararlı sürüm 1.0 olacaktır, ama Kasım 2018 itibarıyla modülün AzureRm ile özellik eşliği vardır.</span><span class="sxs-lookup"><span data-stu-id="4a63f-111">The first stable release will be 1.0, but the module has feature parity with AzureRm as of November 2018.</span></span>

## <a name="upgrade-to-az"></a><span data-ttu-id="4a63f-112">Az modülüne yükseltme</span><span class="sxs-lookup"><span data-stu-id="4a63f-112">Upgrade to Az</span></span>

<span data-ttu-id="4a63f-113">Kullanıcıların yeni `Az` modülüne yükseltmenizi öneririz.</span><span class="sxs-lookup"><span data-stu-id="4a63f-113">It's recommended that users upgrade to the new `Az` module.</span></span> <span data-ttu-id="4a63f-114">Bunu yapmak için:</span><span class="sxs-lookup"><span data-stu-id="4a63f-114">To do so:</span></span>

* [<span data-ttu-id="4a63f-115">Azure PowerShell AzureRM modülünü kaldırın</span><span class="sxs-lookup"><span data-stu-id="4a63f-115">Uninstall the Azure PowerShell AzureRM module</span></span>](/powershell/azure/uninstall-azurerm-ps)
* [<span data-ttu-id="4a63f-116">Azure PowerShell Az modülünü yükleyin</span><span class="sxs-lookup"><span data-stu-id="4a63f-116">Install the Azure PowerShell Az module</span></span>](/powershell/azure/install-az-ps)
* <span data-ttu-id="4a63f-117">Yeni komut kümesine alışırken `Enable-AzureRMAlias` ile AzureRM için uyumluluk modunu etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="4a63f-117">Enable compatibility mode for AzureRM with `Enable-AzureRMAlias` while you become familiar with the new command set.</span></span>

## <a name="migrate-existing-scripts-to-az"></a><span data-ttu-id="4a63f-118">Mevcut betikleri için Az modülüne geçirme</span><span class="sxs-lookup"><span data-stu-id="4a63f-118">Migrate existing scripts to Az</span></span>

<span data-ttu-id="4a63f-119">Önemli güncelleştirmeler çok rahat yapılamayabilir.</span><span class="sxs-lookup"><span data-stu-id="4a63f-119">Major updates can be inconvenient.</span></span> <span data-ttu-id="4a63f-120">Öte yandan, yeni söz dizimindeki güncelleştirmelerle çalışırken mevcut betikleri de kullanmanıza yardımcı olmak için `Az` modülünün bir uyumluluk modu vardır.</span><span class="sxs-lookup"><span data-stu-id="4a63f-120">However, the `Az` module has a compatibility mode to help you use existing scripts while you work on updates to the new syntax.</span></span> <span data-ttu-id="4a63f-121">`AzureRM` uyumluluk modunu etkinleştirmek için `Enable-AzureRmAlias` cmdlet'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="4a63f-121">Use the `Enable-AzureRmAlias` cmdlet to enable the `AzureRM` compatibility mode.</span></span> <span data-ttu-id="4a63f-122">Bu cmdlet, `AzureRM` cmdlet adlarını yeni `Az` cmdlet'lerinin diğer adları olarak tanımlar.</span><span class="sxs-lookup"><span data-stu-id="4a63f-122">This cmdlet defines `AzureRM` cmdlet names as aliases for the new `Az` cmdlet names.</span></span>

<span data-ttu-id="4a63f-123">Yeni cmdlet adları kolay öğrenilecek şekilde tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="4a63f-123">The new cmdlet names have been designed to be easy to learn.</span></span> <span data-ttu-id="4a63f-124">Cmdlet adlarında `AzureRm` veya `Azure` kullanmak yerine `Az` kullanın.</span><span class="sxs-lookup"><span data-stu-id="4a63f-124">Instead of using `AzureRm` or `Azure` in cmdlet names, use `Az`.</span></span> <span data-ttu-id="4a63f-125">Örneğin, eski `New-AzureRmVm` komutu `New-AzVm` komutuna dönüştürülmüştür.</span><span class="sxs-lookup"><span data-stu-id="4a63f-125">For example, the old command `New-AzureRmVm` has become `New-AzVm`.</span></span>

<span data-ttu-id="4a63f-126">Geçiş işleminin tam açıklaması için bkz. [AzureRM'den Az'ye geçiş](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="4a63f-126">For a full description of the migration process, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>

## <a name="the-future-of-support-for-azurerm"></a><span data-ttu-id="4a63f-127">AzureRM desteğinin geleceği</span><span class="sxs-lookup"><span data-stu-id="4a63f-127">The future of support for AzureRM</span></span>

<span data-ttu-id="4a63f-128">Aralık 2018'de `Az` sürüm 1.0 kullanıma sunulduğunda, mevcut `AzureRM` modülü artık yeni cmdlet'ler veya özellikler almayacaktır.</span><span class="sxs-lookup"><span data-stu-id="4a63f-128">The existing `AzureRM` module will no longer receive new cmdlets or features when `Az` version 1.0 is released in December 2018.</span></span> <span data-ttu-id="4a63f-129">Öte yandan, `AzureRM` hala resmi olarak korunmaktadır ve hata düzeltmeleri alacaktır.</span><span class="sxs-lookup"><span data-stu-id="4a63f-129">However, `AzureRM` is still officially maintained and will get bug fixes.</span></span> <span data-ttu-id="4a63f-130">En son Azure hizmetleri ve özelliklerini yakından izlemek için, `Az` modülüne geçmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="4a63f-130">To keep up with the latest Azure services and features, you should switch to the `Az` module.</span></span>