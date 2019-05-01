---
title: Azure PowerShell Az modülüne giriş
description: Azure PowerShell'in AzureRM modülünün yerini alan yeni Az modülüne giriş.
ms.date: 12/13/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 10665a72bc7dcae8ecf36b5ef4e2ab285a0e78b7
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63068838"
---
# <a name="introducing-the-new-azure-powershell-az-module"></a><span data-ttu-id="51b91-103">Yeni Azure PowerShell Az modülüne giriş</span><span class="sxs-lookup"><span data-stu-id="51b91-103">Introducing the new Azure PowerShell Az module</span></span>

<span data-ttu-id="51b91-104">Azure PowerShell Az modülü, Aralık 2018’de genel yayın aşamasına ulaşmıştır ve artık Azure ile etkileşim kurmak için kullanılması hedeflenen PowerShell modülüdür.</span><span class="sxs-lookup"><span data-stu-id="51b91-104">Starting in December 2018, the Azure PowerShell Az module is in general release and now the intended PowerShell module for interacting with Azure.</span></span> <span data-ttu-id="51b91-105">Az tarafından daha kısa komutlar, gelişmiş kararlılık ve platformlar arası destek sunulur.</span><span class="sxs-lookup"><span data-stu-id="51b91-105">Az offers shorter commands, improved stability, and cross-platform support.</span></span> <span data-ttu-id="51b91-106">Ayrıca Az, AzureRM ile özellik eşliği ve AzureRM'den kolay geçiş yolu da sunar.</span><span class="sxs-lookup"><span data-stu-id="51b91-106">Az also offers feature parity and an easy migration path from AzureRM.</span></span>

<span data-ttu-id="51b91-107">Az, .NET Standard kitaplığını kullanır ve bu da PowerShell 5 ile PowerShell 6 üzerinde çalıştığı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="51b91-107">Az uses the .NET Standard library, which means it runs on PowerShell 5 and PowerShell 6.</span></span>
<span data-ttu-id="51b91-108">PowerShell 6 Linux, macOS ve Windows üzerinde çalışabildiğinden, Azure PowerShell artık tüm platformlarda kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="51b91-108">Since PowerShell 6 can run on Linux, macOS, and Windows, Azure PowerShell is now available for all platforms.</span></span>
<span data-ttu-id="51b91-109">.NET Standard'ın kullanılması, Azure PowerShell'in kod tabanını kullanıcıları çok az etkileyerek birleştirmemize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="51b91-109">Using .NET Standard allows us to unify the code base of Azure PowerShell with minimal impact on users.</span></span>

<span data-ttu-id="51b91-110">Az yeni bir modül olduğundan, sürüm 1.0.0 olarak sıfırlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="51b91-110">Az is a new module, so the version has been reset to 1.0.0.</span></span>

## <a name="upgrade-to-az"></a><span data-ttu-id="51b91-111">Az modülüne yükseltme</span><span class="sxs-lookup"><span data-stu-id="51b91-111">Upgrade to Az</span></span>

<span data-ttu-id="51b91-112">Tüm kullanıcıların yeni Az modülüne yükseltmesi önerilir.</span><span class="sxs-lookup"><span data-stu-id="51b91-112">It's recommended that all users upgrade to the new Az module.</span></span> <span data-ttu-id="51b91-113">Bunu yapmak için:</span><span class="sxs-lookup"><span data-stu-id="51b91-113">To do so:</span></span>

* <span data-ttu-id="51b91-114">__ÖNERİLİR__: [Azure PowerShell AzureRM modülünü kaldırın](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module)</span><span class="sxs-lookup"><span data-stu-id="51b91-114">__RECOMMENDED__: [Uninstall the Azure PowerShell AzureRM module](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module)</span></span>
* [<span data-ttu-id="51b91-115">Azure PowerShell Az modülünü yükleyin</span><span class="sxs-lookup"><span data-stu-id="51b91-115">Install the Azure PowerShell Az module</span></span>](/powershell/azure/install-az-ps)
* <span data-ttu-id="51b91-116">Yeni komut kümesine alışırken `Enable-AzureRMAlias` ile AzureRM cmdlet’lerine yönelik diğer adları eklemek için uyumluluk modunu etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="51b91-116">Enable compatibility mode to add aliases for AzureRM cmdlets with `Enable-AzureRMAlias` while you become familiar with the new command set.</span></span> <span data-ttu-id="51b91-117">Diğer adları __yalnızca__ AzureRM yüklü değilse etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="51b91-117">__Only__ enable aliases if you do not have AzureRM installed.</span></span>

## <a name="migrate-existing-scripts-to-az"></a><span data-ttu-id="51b91-118">Mevcut betikleri için Az modülüne geçirme</span><span class="sxs-lookup"><span data-stu-id="51b91-118">Migrate existing scripts to Az</span></span>

<span data-ttu-id="51b91-119">Önemli güncelleştirmeler çok rahat yapılamayabilir.</span><span class="sxs-lookup"><span data-stu-id="51b91-119">Major updates can be inconvenient.</span></span> <span data-ttu-id="51b91-120">Öte yandan, yeni söz dizimindeki güncelleştirmelerle çalışırken mevcut betikleri de kullanmanıza yardımcı olmak için Az modülünün bir uyumluluk modu vardır.</span><span class="sxs-lookup"><span data-stu-id="51b91-120">However, the Az module has a compatibility mode to help you use existing scripts while you work on updates to the new syntax.</span></span> <span data-ttu-id="51b91-121">AzureRM uyumluluk modunu etkinleştirmek için `Enable-AzureRmAlias` cmdlet'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="51b91-121">Use the `Enable-AzureRmAlias` cmdlet to enable the AzureRM compatibility mode.</span></span> <span data-ttu-id="51b91-122">Bu cmdlet, AzureRM cmdlet adlarını yeni Az cmdlet'lerinin diğer adları olarak tanımlar.</span><span class="sxs-lookup"><span data-stu-id="51b91-122">This cmdlet defines AzureRM cmdlet names as aliases for the new Az cmdlet names.</span></span>

<span data-ttu-id="51b91-123">Yeni cmdlet adları kolay öğrenilecek şekilde tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="51b91-123">The new cmdlet names have been designed to be easy to learn.</span></span> <span data-ttu-id="51b91-124">Cmdlet adlarında `AzureRm` veya `Azure` kullanmak yerine `Az` kullanın.</span><span class="sxs-lookup"><span data-stu-id="51b91-124">Instead of using `AzureRm` or `Azure` in cmdlet names, use `Az`.</span></span> <span data-ttu-id="51b91-125">Örneğin, eski `New-AzureRMVm` komutu `New-AzVm` komutuna dönüştürülmüştür.</span><span class="sxs-lookup"><span data-stu-id="51b91-125">For example, the old command `New-AzureRMVm` has become `New-AzVm`.</span></span>

<span data-ttu-id="51b91-126">Geçiş işleminin tam açıklaması için bkz. [AzureRM'den Az'ye geçiş](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="51b91-126">For a full description of the migration process, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>

## <a name="the-future-of-support-for-azurerm"></a><span data-ttu-id="51b91-127">AzureRM desteğinin geleceği</span><span class="sxs-lookup"><span data-stu-id="51b91-127">The future of support for AzureRM</span></span>

<span data-ttu-id="51b91-128">Mevcut AzureRM modülü için artık yeni cmdlet’ler veya özellikler sağlanmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="51b91-128">The existing AzureRM module will no longer receive new cmdlets or features.</span></span> <span data-ttu-id="51b91-129">Bununla birlikte, AzureRM hala resmi olarak bakım kapsamındadır ve Aralık 2020'ye kadar hata düzeltmeleri sağlanacaktır.</span><span class="sxs-lookup"><span data-stu-id="51b91-129">However, AzureRM is still officially maintained and will get bug fixes up through December 2020.</span></span> <span data-ttu-id="51b91-130">En son Azure hizmetlerini ve özelliklerini takip etmek için Az modülüne geçin.</span><span class="sxs-lookup"><span data-stu-id="51b91-130">To keep up with the latest Azure services and features, switch to the Az module.</span></span>
