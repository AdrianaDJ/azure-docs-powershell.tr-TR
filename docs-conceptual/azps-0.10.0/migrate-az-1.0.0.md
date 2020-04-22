---
title: AzureRM'den Azure PowerShell Az 1.0.0’a tüm değişiklikler
description: Bu geçiş kılavuzu, Azure PowerShell Az sürüm 1 yayınında yapılan yeni değişikliklerin listesini içerir.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2019
ms.openlocfilehash: e5121d61b0f5f68ff3e1f33d774e3533adfeb64f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "81445552"
---
# <a name="breaking-changes-for-az-100"></a><span data-ttu-id="99bfe-103">Az 1.0.0 için yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="99bfe-103">Breaking changes for Az 1.0.0</span></span>

<span data-ttu-id="99bfe-104">Bu belge, AzureRM 6.x ve yeni Az modülü (sürüm 1.x ve sonrası) arasındaki değişiklikler hakkında ayrıntılı bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="99bfe-104">This document provides detailed information on the changes between AzureRM 6.x and the new Az module, version 1.x and later.</span></span> <span data-ttu-id="99bfe-105">İçindekiler tablosu, betiklerinizi etkileyebilecek modüle özgü değişiklikler de dahil olmak üzere, tam geçiş yolunda size kılavuzluk edecektir.</span><span class="sxs-lookup"><span data-stu-id="99bfe-105">The table of contents will help guide you through a full migration path, including module-specific changes that may affect your scripts.</span></span>

<span data-ttu-id="99bfe-106">AzureRM’den Az’ye geçiş işlemine başlangıç konusunda genel öneriler için bkz. [AzureRM’den Az modülüne geçişi başlatma](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="99bfe-106">For general advice on getting started with a migration from AzureRM to Az, see [Start migration from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="99bfe-107">Az 1.0.0 ile Az 2.0.0 arasında da hataya neden olan değişiklikler bulunur.</span><span class="sxs-lookup"><span data-stu-id="99bfe-107">There have been breaking changes between Az 1.0.0 and Az 2.0.0 as well.</span></span> <span data-ttu-id="99bfe-108">AzureRM’den Az modülüne güncelleştirmek için bu kılavuzu izledikten sonra ek değişiklikler yapmanız gerekip gerekmediğini öğrenmek için bkz. [Az 2.0.0 hataya neden olan değişiklikler](migrate-az-2.0.0.md).</span><span class="sxs-lookup"><span data-stu-id="99bfe-108">After following this guide for updating from AzureRM to Az, see the [Az 2.0.0 breaking changes](migrate-az-2.0.0.md) to find out if you need to make additional changes.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="99bfe-109">İçindekiler</span><span class="sxs-lookup"><span data-stu-id="99bfe-109">Table of Contents</span></span>

- [<span data-ttu-id="99bfe-110">Hataya neden olan genel değişiklikler</span><span class="sxs-lookup"><span data-stu-id="99bfe-110">General breaking changes</span></span>](#general-breaking-changes)
  - [<span data-ttu-id="99bfe-111">Cmdlet isim ön eki değişiklikleri</span><span class="sxs-lookup"><span data-stu-id="99bfe-111">Cmdlet noun prefix changes</span></span>](#cmdlet-noun-prefix-changes)
  - [<span data-ttu-id="99bfe-112">Modül adı değişiklikleri</span><span class="sxs-lookup"><span data-stu-id="99bfe-112">Module name changes</span></span>](#module-name-changes)
  - [<span data-ttu-id="99bfe-113">Kaldırılan modüller</span><span class="sxs-lookup"><span data-stu-id="99bfe-113">Removed modules</span></span>](#removed-modules)
  - [<span data-ttu-id="99bfe-114">Windows PowerShell 5.1 ve .NET 4.7.2</span><span class="sxs-lookup"><span data-stu-id="99bfe-114">Windows PowerShell 5.1 and .NET 4.7.2</span></span>](#windows-powershell-51-and-net-472)
  - [<span data-ttu-id="99bfe-115">PSCredential ile kullanıcı oturumu açmanın geçici olarak kaldırılması</span><span class="sxs-lookup"><span data-stu-id="99bfe-115">Temporary removal of user login using PSCredential</span></span>](#temporary-removal-of-user-login-using-pscredential)
  - [<span data-ttu-id="99bfe-116">Web tarayıcısı istemi yerine varsayılan cihaz kodu ile oturum açma</span><span class="sxs-lookup"><span data-stu-id="99bfe-116">Default device code login instead of web browser prompt</span></span>](#default-device-code-login-instead-of-web-browser-prompt)
- [<span data-ttu-id="99bfe-117">Modüldeki yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="99bfe-117">Module breaking changes</span></span>](#module-breaking-changes)
  - [<span data-ttu-id="99bfe-118">Az.ApiManagement (eski adıyla AzureRM.ApiManagement)</span><span class="sxs-lookup"><span data-stu-id="99bfe-118">Az.ApiManagement (previously AzureRM.ApiManagement)</span></span>](#azapimanagement-previously-azurermapimanagement)
  - [<span data-ttu-id="99bfe-119">Az.Billing (eski adıyla AzureRM.Billing, AzureRM.Consumption ve AzureRM.UsageAggregates)</span><span class="sxs-lookup"><span data-stu-id="99bfe-119">Az.Billing (previously AzureRM.Billing, AzureRM.Consumption, and AzureRM.UsageAggregates)</span></span>](#azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates)
  - [<span data-ttu-id="99bfe-120">Az.CognitiveServices (eski adıyla AzureRM.CognitiveServices)</span><span class="sxs-lookup"><span data-stu-id="99bfe-120">Az.CognitiveServices (previously AzureRM.CognitiveServices)</span></span>](#azcognitiveservices-previously-azurermcognitiveservices)
  - [<span data-ttu-id="99bfe-121">Az.Compute (eski adıyla AzureRM.Compute)</span><span class="sxs-lookup"><span data-stu-id="99bfe-121">Az.Compute (previously AzureRM.Compute)</span></span>](#azcompute-previously-azurermcompute)
  - [<span data-ttu-id="99bfe-122">Az.DataFactory (eski adıyla AzureRM.DataFactories ve AzureRM.DataFactoryV2)</span><span class="sxs-lookup"><span data-stu-id="99bfe-122">Az.DataFactory (previously AzureRM.DataFactories and AzureRM.DataFactoryV2)</span></span>](#azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2)
  - [<span data-ttu-id="99bfe-123">Az.DataLakeAnalytics (eski adıyla AzureRM.DataLakeAnalytics)</span><span class="sxs-lookup"><span data-stu-id="99bfe-123">Az.DataLakeAnalytics (previously AzureRM.DataLakeAnalytics)</span></span>](#azdatalakeanalytics-previously-azurermdatalakeanalytics)
  - [<span data-ttu-id="99bfe-124">Az.DataLakeStore (eski adıyla AzureRM.DataLakeStore)</span><span class="sxs-lookup"><span data-stu-id="99bfe-124">Az.DataLakeStore (previously AzureRM.DataLakeStore)</span></span>](#azdatalakestore-previously-azurermdatalakestore)
  - [<span data-ttu-id="99bfe-125">Az.KeyVault (eski adıyla AzureRM.KeyVault)</span><span class="sxs-lookup"><span data-stu-id="99bfe-125">Az.KeyVault (previously AzureRM.KeyVault)</span></span>](#azkeyvault-previously-azurermkeyvault)
  - [<span data-ttu-id="99bfe-126">Az.Media (eski adıyla AzureRM.Media)</span><span class="sxs-lookup"><span data-stu-id="99bfe-126">Az.Media (previously AzureRM.Media)</span></span>](#azmedia-previously-azurermmedia)
  - [<span data-ttu-id="99bfe-127">Az.Monitor (eski adıyla AzureRM.Insights)</span><span class="sxs-lookup"><span data-stu-id="99bfe-127">Az.Monitor (previously AzureRM.Insights)</span></span>](#azmonitor-previously-azurerminsights)
  - [<span data-ttu-id="99bfe-128">Az.Network (eski adıyla AzureRM.Network)</span><span class="sxs-lookup"><span data-stu-id="99bfe-128">Az.Network (previously AzureRM.Network)</span></span>](#aznetwork-previously-azurermnetwork)
  - [<span data-ttu-id="99bfe-129">Az.OperationalInsights (eski adıyla AzureRM.OperationalInsights)</span><span class="sxs-lookup"><span data-stu-id="99bfe-129">Az.OperationalInsights (previously AzureRM.OperationalInsights)</span></span>](#azoperationalinsights-previously-azurermoperationalinsights)
  - [<span data-ttu-id="99bfe-130">Az.RecoveryServices (eski adıyla AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup ve AzureRM.RecoveryServices.SiteRecovery)</span><span class="sxs-lookup"><span data-stu-id="99bfe-130">Az.RecoveryServices (previously AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup, and AzureRM.RecoveryServices.SiteRecovery)</span></span>](#azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery)
  - [<span data-ttu-id="99bfe-131">Az.Resources (eski adıyla AzureRM.Resources)</span><span class="sxs-lookup"><span data-stu-id="99bfe-131">Az.Resources (previously AzureRM.Resources)</span></span>](#azresources-previously-azurermresources)
  - [<span data-ttu-id="99bfe-132">Az.ServiceFabric (eski adıyla AzureRM.ServiceFabric)</span><span class="sxs-lookup"><span data-stu-id="99bfe-132">Az.ServiceFabric (previously AzureRM.ServiceFabric)</span></span>](#azservicefabric-previously-azurermservicefabric)
  - [<span data-ttu-id="99bfe-133">Az.Sql (eski adıyla AzureRM.Sql)</span><span class="sxs-lookup"><span data-stu-id="99bfe-133">Az.Sql (previously AzureRM.Sql)</span></span>](#azsql-previously-azurermsql)
  - [<span data-ttu-id="99bfe-134">Az.Storage (eski adıyla Azure.Storage and AzureRM.Storage)</span><span class="sxs-lookup"><span data-stu-id="99bfe-134">Az.Storage (previously Azure.Storage and AzureRM.Storage)</span></span>](#azstorage-previously-azurestorage-and-azurermstorage)
  - [<span data-ttu-id="99bfe-135">Az.Websites (eski adıyla AzureRM.Websites)</span><span class="sxs-lookup"><span data-stu-id="99bfe-135">Az.Websites (previously AzureRM.Websites)</span></span>](#azwebsites-previously-azurermwebsites)

## <a name="general-breaking-changes"></a><span data-ttu-id="99bfe-136">Hataya neden olan genel değişiklikler</span><span class="sxs-lookup"><span data-stu-id="99bfe-136">General breaking changes</span></span>

<span data-ttu-id="99bfe-137">Bu bölümde, Az modülünün yeniden tasarımının bir parçası olan, hataya neden olan genel değişiklikler ayrıntılı olarak açıklanır.</span><span class="sxs-lookup"><span data-stu-id="99bfe-137">This section details the general breaking changes that are part of the redesign of the Az module.</span></span>

### <a name="cmdlet-noun-prefix-changes"></a><span data-ttu-id="99bfe-138">Cmdlet İsim Öneki Değişiklikleri</span><span class="sxs-lookup"><span data-stu-id="99bfe-138">Cmdlet Noun Prefix Changes</span></span>

<span data-ttu-id="99bfe-139">AzureRM modülünde cmdlet’ler isim ön eki olarak `AzureRM` veya `Azure` kullanılır.</span><span class="sxs-lookup"><span data-stu-id="99bfe-139">In the AzureRM module, cmdlets used either `AzureRM` or `Azure` as a noun prefix.</span></span>  <span data-ttu-id="99bfe-140">Az ile birlikte cmdlet adları basitleştirilip normalleştirilerek tüm cmdlet’lerin isim ön eki olarak 'Az' kullanılacak.</span><span class="sxs-lookup"><span data-stu-id="99bfe-140">Az simplifies and normalizes cmdlet names, so that all cmdlets use 'Az' as their cmdlet noun prefix.</span></span> <span data-ttu-id="99bfe-141">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="99bfe-141">For example:</span></span>

```azurepowershell-interactive
Get-AzureRMVM
Get-AzureKeyVaultSecret
```

<span data-ttu-id="99bfe-142">Yeni ad:</span><span class="sxs-lookup"><span data-stu-id="99bfe-142">Has changed to:</span></span>

```azurepowershell-interactive
Get-AzVM
Get-AzKeyVaultSecret
```

<span data-ttu-id="99bfe-143">Bu yeni cmdlet adlarına geçişi kolaylaştırmak için Az ile birlikte iki yeni cmdlet sunuluyor: [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) ve [Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias).</span><span class="sxs-lookup"><span data-stu-id="99bfe-143">To make the transition to these new cmdlet names simpler, Az introduces two new cmdlets, [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) and [Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias).</span></span>  <span data-ttu-id="99bfe-144">`Enable-AzureRmAlias`, AzureRM’deki eski cmdlet adları için yeni Az cmdlet adlarına eşlenen diğer adlar oluşturur.</span><span class="sxs-lookup"><span data-stu-id="99bfe-144">`Enable-AzureRmAlias` creates aliases for the older cmdlet names in AzureRM that map to the newer Az cmdlet names.</span></span> <span data-ttu-id="99bfe-145">`Enable-AzureRmAlias` ile `-Scope` bağımsız değişkenini kullanarak diğer adları nerede etkinleştireceğinizi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="99bfe-145">Using the `-Scope` argument with `Enable-AzureRmAlias` allows you to choose where aliases are enabled.</span></span>

<span data-ttu-id="99bfe-146">Örneğin, şu AzureRM betiği:</span><span class="sxs-lookup"><span data-stu-id="99bfe-146">For example, the following script in AzureRM:</span></span>

```azurepowershell-interactive
#Requires -Modules AzureRM.Storage
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="99bfe-147">`Enable-AzureRmAlias` kullanılarak küçük değişikliklerle çalıştırılabilir:</span><span class="sxs-lookup"><span data-stu-id="99bfe-147">Can be run with minimal changes using `Enable-AzureRmAlias`:</span></span>

```azurepowershell-interactive
#Requires -Modules Az.Storage
Enable-AzureRmAlias -Scope Process
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="99bfe-148">`Enable-AzureRmAlias -Scope CurrentUser` çalıştırıldığında açtığınız tüm PowerShell oturumları için diğer adları etkinleştireceğinden, bu cmdlet’i çalıştırdıktan sonra şunun gibi bir betiğin hiç değiştirilmesi gerekmez:</span><span class="sxs-lookup"><span data-stu-id="99bfe-148">Running `Enable-AzureRmAlias -Scope CurrentUser` will enable the aliases for all PowerShell sessions you open, so that after executing this cmdlet, a script like this would not need to be changed at all:</span></span>

```azurepowershell-interactive
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="99bfe-149">Diğer ad cmdlet’leri kullanımının tüm ayrıntıları için bkz. [Enable-AzureRmAlias başvurusu](/powershell/module/az.accounts/enable-azurermalias).</span><span class="sxs-lookup"><span data-stu-id="99bfe-149">For complete details on the usage of the alias cmdlets, see the [Enable-AzureRmAlias reference](/powershell/module/az.accounts/enable-azurermalias).</span></span>

<span data-ttu-id="99bfe-150">Diğer adları devre dışı bırakmaya hazır olduğunuzda `Disable-AzureRmAlias` cmdlet'i oluşturulan diğer adları kaldırır.</span><span class="sxs-lookup"><span data-stu-id="99bfe-150">When you're ready to disable aliases, `Disable-AzureRmAlias` removes the created aliases.</span></span> <span data-ttu-id="99bfe-151">Tüm ayrıntıları için bkz. [Disable-AzureRmAlias başvurusu](/powershell/module/az.accounts/disable-azurermalias).</span><span class="sxs-lookup"><span data-stu-id="99bfe-151">For complete details, see the [Disable-AzureRmAlias reference](/powershell/module/az.accounts/disable-azurermalias).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="99bfe-152">Diğer adları devre dışı bırakırken, diğer adların etkin olduğu _tüm_ kapsamlarda devre dışı bırakıldıklarından emin olun.</span><span class="sxs-lookup"><span data-stu-id="99bfe-152">When disabling aliases, make sure that they are disabled for _all_ scopes which had aliases enabled.</span></span>

### <a name="module-name-changes"></a><span data-ttu-id="99bfe-153">Modül Adı Değişiklikleri</span><span class="sxs-lookup"><span data-stu-id="99bfe-153">Module Name Changes</span></span>

<span data-ttu-id="99bfe-154">Aşağıdaki modüller dışında, önceden `AzureRM.*` olan modül adları `Az.*` olarak değiştirildi:</span><span class="sxs-lookup"><span data-stu-id="99bfe-154">The module names have changed from `AzureRM.*` to `Az.*`, except for the following modules:</span></span>

| <span data-ttu-id="99bfe-155">AzureRM modülü</span><span class="sxs-lookup"><span data-stu-id="99bfe-155">AzureRM module</span></span> | <span data-ttu-id="99bfe-156">Az modülü</span><span class="sxs-lookup"><span data-stu-id="99bfe-156">Az module</span></span> |
|----------------|-----------|
| <span data-ttu-id="99bfe-157">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="99bfe-157">Azure.Storage</span></span> | <span data-ttu-id="99bfe-158">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="99bfe-158">Az.Storage</span></span> |
| <span data-ttu-id="99bfe-159">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="99bfe-159">Azure.AnalysisServices</span></span> | <span data-ttu-id="99bfe-160">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="99bfe-160">Az.AnalysisServices</span></span> |
| <span data-ttu-id="99bfe-161">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="99bfe-161">AzureRM.Profile</span></span> | <span data-ttu-id="99bfe-162">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="99bfe-162">Az.Accounts</span></span> |
| <span data-ttu-id="99bfe-163">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="99bfe-163">AzureRM.Insights</span></span> | <span data-ttu-id="99bfe-164">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="99bfe-164">Az.Monitor</span></span> |
| <span data-ttu-id="99bfe-165">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="99bfe-165">AzureRM.DataFactories</span></span> | <span data-ttu-id="99bfe-166">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="99bfe-166">Az.DataFactory</span></span> |
| <span data-ttu-id="99bfe-167">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="99bfe-167">AzureRM.DataFactoryV2</span></span> | <span data-ttu-id="99bfe-168">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="99bfe-168">Az.DataFactory</span></span> |
| <span data-ttu-id="99bfe-169">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="99bfe-169">AzureRM.RecoveryServices.Backup</span></span> | <span data-ttu-id="99bfe-170">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="99bfe-170">Az.RecoveryServices</span></span> |
| <span data-ttu-id="99bfe-171">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="99bfe-171">AzureRM.RecoveryServices.SiteRecovery</span></span> | <span data-ttu-id="99bfe-172">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="99bfe-172">Az.RecoveryServices</span></span> |
| <span data-ttu-id="99bfe-173">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="99bfe-173">AzureRM.Tags</span></span> | <span data-ttu-id="99bfe-174">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="99bfe-174">Az.Resources</span></span> |
| <span data-ttu-id="99bfe-175">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="99bfe-175">AzureRM.MachineLearningCompute</span></span> | <span data-ttu-id="99bfe-176">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="99bfe-176">Az.MachineLearning</span></span> |
| <span data-ttu-id="99bfe-177">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="99bfe-177">AzureRM.UsageAggregates</span></span> | <span data-ttu-id="99bfe-178">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="99bfe-178">Az.Billing</span></span> |
| <span data-ttu-id="99bfe-179">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="99bfe-179">AzureRM.Consumption</span></span> | <span data-ttu-id="99bfe-180">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="99bfe-180">Az.Billing</span></span> |

<span data-ttu-id="99bfe-181">Modül adlarındaki değişiklikler nedeniyle, belirli modülleri yüklemek için `#Requires` ve `Import-Module` deyimlerini kullanan tüm betiklerin yeni modülü kullanacak şekilde güncelleştirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="99bfe-181">The changes in module names mean that any script that uses `#Requires` or `Import-Module` to load specific modules will need to be changed to use the new module instead.</span></span> <span data-ttu-id="99bfe-182">Cmdlet sonekinin değişmediği modüllerde bu, modül adı değişmiş olsa da işlem alanını belirten sonekin _değişmediği_ anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="99bfe-182">For modules where the cmdlet suffix has not changed, this means that although the module name has changed, the suffix indicating the operation space has _not_.</span></span>

#### <a name="migrating-requires-and-import-module-statements"></a><span data-ttu-id="99bfe-183">#Requires ve Import-Module Deyimlerini Geçirme</span><span class="sxs-lookup"><span data-stu-id="99bfe-183">Migrating #Requires and Import-Module Statements</span></span>

<span data-ttu-id="99bfe-184">AzureRM modüllerine bağımlılığı bildirmek için `#Requires` veya `Import-Module` deyimini kullanan betikler yeni modül adlarını kullanacak şekilde güncelleştirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="99bfe-184">Scripts that use `#Requires` or `Import-Module` to declare a dependency on AzureRM modules must be updated to use the new module names.</span></span> <span data-ttu-id="99bfe-185">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="99bfe-185">For example:</span></span>

```azurepowershell-interactive
#Requires -Module AzureRM.Compute
```

<span data-ttu-id="99bfe-186">Şöyle değiştirilmelidir:</span><span class="sxs-lookup"><span data-stu-id="99bfe-186">Should be changed to:</span></span>

```azurepowershell-interactive
#Requires -Module Az.Compute
```

<span data-ttu-id="99bfe-187">`Import-Module` için:</span><span class="sxs-lookup"><span data-stu-id="99bfe-187">For `Import-Module`:</span></span>

```azurepowershell-interactive
Import-Module -Name AzureRM.Compute
```

<span data-ttu-id="99bfe-188">Şöyle değiştirilmelidir:</span><span class="sxs-lookup"><span data-stu-id="99bfe-188">Should be changed to:</span></span>

```azurepowershell-interactive
Import-Module -Name Az.Compute
```

### <a name="migrating-fully-qualified-cmdlet-invocations"></a><span data-ttu-id="99bfe-189">Tam Olarak Nitelenen Cmdlet Çağrılarını Geçirme</span><span class="sxs-lookup"><span data-stu-id="99bfe-189">Migrating Fully-Qualified Cmdlet Invocations</span></span>

<span data-ttu-id="99bfe-190">Şunun gibi modül adıyla nitelenen cmdlet çağrılarını kullanan betikler:</span><span class="sxs-lookup"><span data-stu-id="99bfe-190">Scripts that use module-qualified cmdlet invocations, such as:</span></span>

```azurepowershell-interactive
AzureRM.Compute\Get-AzureRmVM
```

<span data-ttu-id="99bfe-191">Yeni modülü ve cmdlet adlarını kullanacak şekilde değiştirilmelidir:</span><span class="sxs-lookup"><span data-stu-id="99bfe-191">Must be changed to use the new module and cmdlet names:</span></span>

```azurepowershell-interactive
Az.Compute\Get-AzVM
```

### <a name="migrating-module-manifest-dependencies"></a><span data-ttu-id="99bfe-192">Modül bildirimi bağımlılıklarını geçirme</span><span class="sxs-lookup"><span data-stu-id="99bfe-192">Migrating module manifest dependencies</span></span>

<span data-ttu-id="99bfe-193">Bir modül bildirimi (.psd1) dosyası aracılığıyla AzureRM modüllerine bağımlılığı ifade eden modüllerin `RequiredModules` bölümünde güncelleştirilmiş modül adları olmalıdır:</span><span class="sxs-lookup"><span data-stu-id="99bfe-193">Modules that express dependencies on AzureRM modules through a module manifest (.psd1) file will need to updated the module names in their `RequiredModules` section:</span></span>

```powershell
RequiredModules = @(@{ModuleName="AzureRM.Profile"; ModuleVersion="5.8.2"})
```

<span data-ttu-id="99bfe-194">Şöyle değiştirilmelidir:</span><span class="sxs-lookup"><span data-stu-id="99bfe-194">Must be changed to:</span></span>

```powershell
RequiredModules = @(@{ModuleName="Az.Profile"; ModuleVersion="1.0.0"})
```

### <a name="removed-modules"></a><span data-ttu-id="99bfe-195">Kaldırılan modüller</span><span class="sxs-lookup"><span data-stu-id="99bfe-195">Removed modules</span></span>

<span data-ttu-id="99bfe-196">Aşağıdaki modüller kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="99bfe-196">The following modules have been removed:</span></span>

- `AzureRM.Backup`
- `AzureRM.Compute.ManagedService`
- `AzureRM.Scheduler`

<span data-ttu-id="99bfe-197">Bu hizmetlere yönelik araçlar artık etkin bir şekilde desteklenmemektedir.</span><span class="sxs-lookup"><span data-stu-id="99bfe-197">The tools for these services are no longer actively supported.</span></span>  <span data-ttu-id="99bfe-198">Müşterilerin uygun olan en yakın zamanda alternatif hizmetlere geçmesi önerilir.</span><span class="sxs-lookup"><span data-stu-id="99bfe-198">Customers are encouraged to move to alternative services as soon as it is convenient.</span></span>

### <a name="windows-powershell-51-and-net-472"></a><span data-ttu-id="99bfe-199">Windows PowerShell 5.1 ve .NET 4.7.2</span><span class="sxs-lookup"><span data-stu-id="99bfe-199">Windows PowerShell 5.1 and .NET 4.7.2</span></span>

<span data-ttu-id="99bfe-200">Windows için PowerShell 5.1 ile Az kullanımı, .NET Framework 4.7.2 sürümünün yüklenmesini gerektirir.</span><span class="sxs-lookup"><span data-stu-id="99bfe-200">Using Az with PowerShell 5.1 for Windows requires the installation of .NET Framework 4.7.2.</span></span> <span data-ttu-id="99bfe-201">PowerShell Core 6.x ve sonraki sürümleri .NET Framework gerektirmez.</span><span class="sxs-lookup"><span data-stu-id="99bfe-201">Using PowerShell Core 6.x or later does not require .NET Framework.</span></span>

### <a name="temporary-removal-of-user-login-using-pscredential"></a><span data-ttu-id="99bfe-202">PSCredential ile Kullanıcı oturumu açmanın geçici olarak kaldırılması</span><span class="sxs-lookup"><span data-stu-id="99bfe-202">Temporary removal of User login using PSCredential</span></span>

<span data-ttu-id="99bfe-203">.NET Standard kimlik doğrulama akışındaki değişiklikler nedeniyle, PSCredential üzerinden kullanıcı oturumu açmayı geçici olarak kaldırıyoruz.</span><span class="sxs-lookup"><span data-stu-id="99bfe-203">Due to changes in the authentication flow for .NET Standard, we are temporarily removing user login via PSCredential.</span></span> <span data-ttu-id="99bfe-204">Bu özellik, Windows için PowerShell 5.1’in 15/1/2019 tarihli yayınında yeniden kullanıma sunulacaktır.</span><span class="sxs-lookup"><span data-stu-id="99bfe-204">This capability will be re-introduced in the 1/15/2019 release for PowerShell 5.1 for Windows.</span></span> <span data-ttu-id="99bfe-205">Bu konu, [bu GitHub sorununda](https://github.com/Azure/azure-powershell/issues/7430) ayrıntılı olarak açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="99bfe-205">This is discussed in detail in [this GitHub issue.](https://github.com/Azure/azure-powershell/issues/7430)</span></span>

### <a name="default-device-code-login-instead-of-web-browser-prompt"></a><span data-ttu-id="99bfe-206">Web tarayıcısı istemi yerine varsayılan cihaz kodu ile oturum açma</span><span class="sxs-lookup"><span data-stu-id="99bfe-206">Default device code login instead of web browser prompt</span></span>

<span data-ttu-id="99bfe-207">.NET Standard kimlik doğrulama akışındaki değişiklikler nedeniyle, etkileşimli oturum açma sırasında varsayılan oturum açma akışı olarak cihazla oturum açmayı kullanıyoruz.</span><span class="sxs-lookup"><span data-stu-id="99bfe-207">Due to changes in the authentication flow for .NET Standard, we are using device login as the default login flow during interactive login.</span></span> <span data-ttu-id="99bfe-208">Web tarayıcısı tabanlı oturum açma, Windows için PowerShell 5.1'de 15/1/2019 tarihli yayınla birlikte yeniden varsayılan seçenek olarak kullanıma sunulacaktır.</span><span class="sxs-lookup"><span data-stu-id="99bfe-208">Web browser based login will be re-introduced for PowerShell 5.1 for Windows as the default in the 1/15/2019 release.</span></span> <span data-ttu-id="99bfe-209">İlgili tarihte, kullanıcılar bir Switch parametresini kullanarak cihaz oturumunu seçebilecek.</span><span class="sxs-lookup"><span data-stu-id="99bfe-209">At that time, users will be able to choose device login using a Switch parameter.</span></span>

## <a name="module-breaking-changes"></a><span data-ttu-id="99bfe-210">Modüldeki yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="99bfe-210">Module breaking changes</span></span>

<span data-ttu-id="99bfe-211">Bu bölümde, belirli modüller ve cmdlet’lerde hataya neden olan değişiklikler ayrıntılı olarak açıklanır.</span><span class="sxs-lookup"><span data-stu-id="99bfe-211">This section details specific breaking changes for individual modules and cmdlets.</span></span>

### <a name="azapimanagement-previously-azurermapimanagement"></a><span data-ttu-id="99bfe-212">Az.ApiManagement (eski adıyla AzureRM.ApiManagement)</span><span class="sxs-lookup"><span data-stu-id="99bfe-212">Az.ApiManagement (previously AzureRM.ApiManagement)</span></span>

- <span data-ttu-id="99bfe-213">Aşağıdaki cmdlet’ler kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="99bfe-213">Removed the following cmdlets:</span></span>
  - <span data-ttu-id="99bfe-214">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="99bfe-214">New-AzureRmApiManagementHostnameConfiguration</span></span>
  - <span data-ttu-id="99bfe-215">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="99bfe-215">Set-AzureRmApiManagementHostnames</span></span>
  - <span data-ttu-id="99bfe-216">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="99bfe-216">Update-AzureRmApiManagementDeployment</span></span>
  - <span data-ttu-id="99bfe-217">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="99bfe-217">Import-AzureRmApiManagementHostnameCertificate</span></span>
  - <span data-ttu-id="99bfe-218">Bu özellikleri ayarlamak için bunun yerine **Set-AzApiManagement** cmdlet’ini kullanın</span><span class="sxs-lookup"><span data-stu-id="99bfe-218">Use **Set-AzApiManagement** cmdlet to set these properties instead</span></span>
- <span data-ttu-id="99bfe-219">Aşağıdaki özellikler kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="99bfe-219">Removed the following properties:</span></span>
  - <span data-ttu-id="99bfe-220">`PsApiManagementContext` öğesinden `PsApiManagementHostnameConfiguration` türündeki `PortalHostnameConfiguration`, `ProxyHostnameConfiguration`, `ManagementHostnameConfiguration` ve `ScmHostnameConfiguration` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="99bfe-220">Removed property `PortalHostnameConfiguration`, `ProxyHostnameConfiguration`, `ManagementHostnameConfiguration` and `ScmHostnameConfiguration` of type `PsApiManagementHostnameConfiguration` from `PsApiManagementContext`.</span></span> <span data-ttu-id="99bfe-221">Bunun yerine `PsApiManagementCustomHostNameConfiguration` türündeki `PortalCustomHostnameConfiguration`, `ProxyCustomHostnameConfiguration`, `ManagementCustomHostnameConfiguration` ve `ScmCustomHostnameConfiguration` özelliğini kullanın.</span><span class="sxs-lookup"><span data-stu-id="99bfe-221">Instead use `PortalCustomHostnameConfiguration`, `ProxyCustomHostnameConfiguration`, `ManagementCustomHostnameConfiguration` and `ScmCustomHostnameConfiguration` of type `PsApiManagementCustomHostNameConfiguration`.</span></span>
  - <span data-ttu-id="99bfe-222">PsApiManagementContext öğesinden `StaticIPs` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="99bfe-222">Removed property `StaticIPs` from PsApiManagementContext.</span></span> <span data-ttu-id="99bfe-223">Özellik `PublicIPAddresses` ve `PrivateIPAddresses` olarak bölündü.</span><span class="sxs-lookup"><span data-stu-id="99bfe-223">The property has been split into `PublicIPAddresses` and `PrivateIPAddresses`.</span></span>
  - <span data-ttu-id="99bfe-224">New-AzureApiManagementVirtualNetwork cmdlet’inden gerekli olan `Location` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="99bfe-224">Removed required property `Location` from New-AzureApiManagementVirtualNetwork cmdlet.</span></span>

### <a name="azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates"></a><span data-ttu-id="99bfe-225">Az.Billing (eski adıyla AzureRM.Billing, AzureRM.Consumption ve AzureRM.UsageAggregates)</span><span class="sxs-lookup"><span data-stu-id="99bfe-225">Az.Billing (previously AzureRM.Billing, AzureRM.Consumption, and AzureRM.UsageAggregates)</span></span>

- <span data-ttu-id="99bfe-226">`Get-AzConsumptionUsageDetail` cmdlet’inden `InvoiceName` parametresi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="99bfe-226">The `InvoiceName` parameter was removed from the `Get-AzConsumptionUsageDetail` cmdlet.</span></span>  <span data-ttu-id="99bfe-227">Fatura için betiklerin diğer kimlik parametrelerini kullanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="99bfe-227">Scripts will need to use other identity parameters for the invoice.</span></span>

### <a name="azcognitiveservices-previously-azurermcognitiveservices"></a><span data-ttu-id="99bfe-228">Az.CognitiveServices (eski adıyla AzureRM.CognitiveServices)</span><span class="sxs-lookup"><span data-stu-id="99bfe-228">Az.CognitiveServices (previously AzureRM.CognitiveServices)</span></span>

- <span data-ttu-id="99bfe-229">`Get-AzCognitiveServicesAccountSkus` cmdlet’inden `GetSkusWithAccountParamSetName` parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="99bfe-229">Removed `GetSkusWithAccountParamSetName` parameter set from `Get-AzCognitiveServicesAccountSkus` cmdlet.</span></span>  <span data-ttu-id="99bfe-230">ResourceGroupName ve Hesap Adı parametrelerini kullanmak yerine Sku’ları Hesap Türüne ve Konuma göre almalısınız.</span><span class="sxs-lookup"><span data-stu-id="99bfe-230">You must get Skus by Account Type and Location, instead of using ResourceGroupName and Account Name.</span></span>

### <a name="azcompute-previously-azurermcompute"></a><span data-ttu-id="99bfe-231">Az.Compute (eski adıyla AzureRM.Compute)</span><span class="sxs-lookup"><span data-stu-id="99bfe-231">Az.Compute (previously AzureRM.Compute)</span></span>

- <span data-ttu-id="99bfe-232">`PSVirtualMachine` ve `PSVirtualMachineScaleSet` nesnelerinde `Identity` özelliğinden `IdentityIds` kaldırıldı Betikler artık işleme kararları vermek için bu alanın değerini kullanmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="99bfe-232">`IdentityIds` are removed from `Identity` property in `PSVirtualMachine` and `PSVirtualMachineScaleSet` objects Scripts should no longer use the value of this field to make processing decisions.</span></span>
- <span data-ttu-id="99bfe-233">`PSVirtualMachineScaleSetVM` nesnesinin `InstanceView` özelliğinin `VirtualMachineInstanceView` olan türü `VirtualMachineScaleSetVMInstanceView` olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="99bfe-233">The type of `InstanceView` property of `PSVirtualMachineScaleSetVM` object is changed from `VirtualMachineInstanceView` to `VirtualMachineScaleSetVMInstanceView`</span></span>
- <span data-ttu-id="99bfe-234">`UpgradePolicy` özelliğinden `AutoOSUpgradePolicy` ve `AutomaticOSUpgrade` özelliği kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="99bfe-234">`AutoOSUpgradePolicy` and `AutomaticOSUpgrade` properties are removed from `UpgradePolicy` property</span></span>
- <span data-ttu-id="99bfe-235">`PSSnapshotUpdate` nesnesindeki `Sku` özelliğinin `DiskSku` olan türü `SnapshotSku` olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="99bfe-235">The type of `Sku` property in `PSSnapshotUpdate` object is changed from `DiskSku` to `SnapshotSku`</span></span>
- <span data-ttu-id="99bfe-236">`VmScaleSetVMParameterSet`, `Add-AzVMDataDisk` cmdlet’inden kaldırıldığından artık bir veri diskini ScaleSet VM’sine tek başına ekleyemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="99bfe-236">`VmScaleSetVMParameterSet` is removed from `Add-AzVMDataDisk` cmdlet, you can no longer add a data disk individually to a ScaleSet VM.</span></span>

### <a name="azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2"></a><span data-ttu-id="99bfe-237">Az.DataFactory (eski adıyla AzureRM.DataFactories ve AzureRM.DataFactoryV2)</span><span class="sxs-lookup"><span data-stu-id="99bfe-237">Az.DataFactory (previously AzureRM.DataFactories and AzureRM.DataFactoryV2)</span></span>

- <span data-ttu-id="99bfe-238">`New-AzDataFactoryEncryptValue` cmdlet’inde `GatewayName` parametresi zorunlu hale geldi</span><span class="sxs-lookup"><span data-stu-id="99bfe-238">The `GatewayName` parameter has become mandatory in the `New-AzDataFactoryEncryptValue` cmdlet</span></span>
- <span data-ttu-id="99bfe-239">`New-AzDataFactoryGatewayKey` cmdlet'i kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="99bfe-239">Removed `New-AzDataFactoryGatewayKey` cmdlet</span></span>
- <span data-ttu-id="99bfe-240">`Get-AzDataFactoryV2ActivityRun` cmdlet’inden `LinkedServiceName` parametresi kaldırıldı Betikler artık işleme kararları vermek için bu alanın değerini kullanmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="99bfe-240">Removed `LinkedServiceName` parameter from `Get-AzDataFactoryV2ActivityRun` cmdlet Scripts should no longer use the value of this field to make processing decisions.</span></span>

### <a name="azdatalakeanalytics-previously-azurermdatalakeanalytics"></a><span data-ttu-id="99bfe-241">Az.DataLakeAnalytics (eski adıyla AzureRM.DataLakeAnalytics)</span><span class="sxs-lookup"><span data-stu-id="99bfe-241">Az.DataLakeAnalytics (previously AzureRM.DataLakeAnalytics)</span></span>

- <span data-ttu-id="99bfe-242">Kullanım dışı cmdlet’ler kaldırıldı: `New-AzDataLakeAnalyticsCatalogSecret`, `Remove-AzDataLakeAnalyticsCatalogSecret` ve `Set-AzDataLakeAnalyticsCatalogSecret`</span><span class="sxs-lookup"><span data-stu-id="99bfe-242">Removed deprecated cmdlets: `New-AzDataLakeAnalyticsCatalogSecret`, `Remove-AzDataLakeAnalyticsCatalogSecret`, and `Set-AzDataLakeAnalyticsCatalogSecret`</span></span>

### <a name="azdatalakestore-previously-azurermdatalakestore"></a><span data-ttu-id="99bfe-243">Az.DataLakeStore (eski adıyla AzureRM.DataLakeStore)</span><span class="sxs-lookup"><span data-stu-id="99bfe-243">Az.DataLakeStore (previously AzureRM.DataLakeStore)</span></span>

- <span data-ttu-id="99bfe-244">Aşağıdaki cmdlet’lerin `Encoding` parametresinin `FileSystemCmdletProviderEncoding` olan türü `System.Text.Encoding` olarak değişti.</span><span class="sxs-lookup"><span data-stu-id="99bfe-244">The following cmdlets have had the `Encoding` parameter changed from the type `FileSystemCmdletProviderEncoding` to `System.Text.Encoding`.</span></span> <span data-ttu-id="99bfe-245">Bu değişiklikle birlikte `String` ve `Oem` kodlama değerleri kaldırılıyor.</span><span class="sxs-lookup"><span data-stu-id="99bfe-245">This change removes the encoding values `String` and `Oem`.</span></span> <span data-ttu-id="99bfe-246">Önceki diğer tüm kodlama değerleri olduğu gibi kaldı.</span><span class="sxs-lookup"><span data-stu-id="99bfe-246">All the other prior encoding values remain.</span></span>
  - <span data-ttu-id="99bfe-247">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="99bfe-247">New-AzureRmDataLakeStoreItem</span></span>
  - <span data-ttu-id="99bfe-248">Add-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="99bfe-248">Add-AzureRmDataLakeStoreItemContent</span></span>
  - <span data-ttu-id="99bfe-249">Get-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="99bfe-249">Get-AzureRmDataLakeStoreItemContent</span></span>
- <span data-ttu-id="99bfe-250">`New-AzDataLakeStoreAccount` ve `Set-AzDataLakeStoreAccount` cmdlet’inden kullanım dışı `Tags` özellik diğer adı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="99bfe-250">Removed deprecated `Tags` property alias from `New-AzDataLakeStoreAccount` and `Set-AzDataLakeStoreAccount` cmdlets</span></span>

  <span data-ttu-id="99bfe-251">Şunları kullanan betikler:</span><span class="sxs-lookup"><span data-stu-id="99bfe-251">Scripts using</span></span>
  ```azurepowershell-interactive
  New-AzureRMDataLakeStoreAccount -Tags @{TagName="TagValue"}
  ```

  <span data-ttu-id="99bfe-252">Şöyle değiştirilmelidir:</span><span class="sxs-lookup"><span data-stu-id="99bfe-252">Should be changed to</span></span>
  ```azurepowershell-interactive
  New-AzDataLakeStoreAccount -Tag @{TagName="TagValue"}
  ```

- <span data-ttu-id="99bfe-253">`PSDataLakeStoreAccountBasic` nesnesinden kullanım dışı `Identity`, `EncryptionState`, `EncryptionProvisioningState`, `EncryptionConfig`, `FirewallState`, `FirewallRules`, `VirtualNetworkRules`, `TrustedIdProviderState`, `TrustedIdProviders`, `DefaultGroup`, `NewTier`, `CurrentTier`, `FirewallAllowAzureIps` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="99bfe-253">Removed deprecated properties `Identity`, `EncryptionState`, `EncryptionProvisioningState`, `EncryptionConfig`, `FirewallState`, `FirewallRules`, `VirtualNetworkRules`, `TrustedIdProviderState`, `TrustedIdProviders`, `DefaultGroup`, `NewTier`, `CurrentTier`, `FirewallAllowAzureIps` from `PSDataLakeStoreAccountBasic` object.</span></span>  <span data-ttu-id="99bfe-254">`Get-AzDataLakeStoreAccount` cmdlet’inden döndürülen `PSDatalakeStoreAccount` özelliğini kullanan hiçbir betik bu özelliklere başvurmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="99bfe-254">Any script that uses the `PSDatalakeStoreAccount` returned from `Get-AzDataLakeStoreAccount` should not reference these properties.</span></span>

### <a name="azkeyvault-previously-azurermkeyvault"></a><span data-ttu-id="99bfe-255">Az.KeyVault (eski adıyla AzureRM.KeyVault)</span><span class="sxs-lookup"><span data-stu-id="99bfe-255">Az.KeyVault (previously AzureRM.KeyVault)</span></span>

- <span data-ttu-id="99bfe-256">`PSKeyVaultKeyAttributes`, `PSKeyVaultKeyIdentityItem` ve `PSKeyVaultSecretAttributes` nesnesinden `PurgeDisabled` özelliği kaldırıldı Betikler artık işleme kararları vermek için ```PurgeDisabled``` özelliğine başvurmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="99bfe-256">The `PurgeDisabled` property was removed from the `PSKeyVaultKeyAttributes`, `PSKeyVaultKeyIdentityItem`, and `PSKeyVaultSecretAttributes` objects Scripts should no longer reference the ```PurgeDisabled``` property to make processing decisions.</span></span>

### <a name="azmedia-previously-azurermmedia"></a><span data-ttu-id="99bfe-257">Az.Media (eski adıyla AzureRM.Media)</span><span class="sxs-lookup"><span data-stu-id="99bfe-257">Az.Media (previously AzureRM.Media)</span></span>

- <span data-ttu-id="99bfe-258">`New-AzMediaService` cmdlet’inden kullanım dışı `Tags` özelliği diğer adı kaldırıldı Şunları kullanan betikler:</span><span class="sxs-lookup"><span data-stu-id="99bfe-258">Remove deprecated `Tags` property alias from `New-AzMediaService` cmdlet Scripts using</span></span>
  ```azurepowershell-interactive
  New-AzureRMMediaService -Tags @{TagName="TagValue"}
  ```

  <span data-ttu-id="99bfe-259">Şöyle değiştirilmelidir:</span><span class="sxs-lookup"><span data-stu-id="99bfe-259">Should be changed to</span></span>
  ```azurepowershell-interactive
  New-AzMediaService -Tag @{TagName="TagValue"}
  ```

### <a name="azmonitor-previously-azurerminsights"></a><span data-ttu-id="99bfe-260">Az.Monitor (eski adıyla AzureRM.Insights)</span><span class="sxs-lookup"><span data-stu-id="99bfe-260">Az.Monitor (previously AzureRM.Insights)</span></span>

- <span data-ttu-id="99bfe-261">`Set-AzDiagnosticSetting` cmdlet’inden alınan tekil parametre adları tercih edilerek çoğul ad `Categories` ve `Timegrains` parametresi kaldırıldı Şunları kullanan betikler:</span><span class="sxs-lookup"><span data-stu-id="99bfe-261">Removed plural names `Categories` and `Timegrains` parameter in favor of singular parameter names from `Set-AzDiagnosticSetting` cmdlet Scripts using</span></span>
  ```azurepowershell-interactive
  Set-AzureRmDiagnosticSetting -Timegrains PT1M -Categories Category1, Category2
  ```

  <span data-ttu-id="99bfe-262">Şöyle değiştirilmelidir:</span><span class="sxs-lookup"><span data-stu-id="99bfe-262">Should be changed to</span></span>
  ```azurepowershell-interactive
  Set-AzDiagnosticSetting -Timegrain PT1M -Category Category1, Category2
  ```

### <a name="aznetwork-previously-azurermnetwork"></a><span data-ttu-id="99bfe-263">Az.Network (eski adıyla AzureRM.Network)</span><span class="sxs-lookup"><span data-stu-id="99bfe-263">Az.Network (previously AzureRM.Network)</span></span>

- <span data-ttu-id="99bfe-264">`Get-AzServiceEndpointPolicyDefinition` cmdlet’inden kullanım dışı `ResourceId` parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="99bfe-264">Removed deprecated `ResourceId` parameter from `Get-AzServiceEndpointPolicyDefinition` cmdlet</span></span>
- <span data-ttu-id="99bfe-265">`PSVirtualNetwork` nesnesinden kullanım dışı `EnableVmProtection` özelliği kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="99bfe-265">Removed deprecated `EnableVmProtection` property from `PSVirtualNetwork` object</span></span>
- <span data-ttu-id="99bfe-266">Kullanım dışı `Set-AzVirtualNetworkGatewayVpnClientConfig` cmdlet’i kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="99bfe-266">Removed deprecated `Set-AzVirtualNetworkGatewayVpnClientConfig` cmdlet</span></span>

<span data-ttu-id="99bfe-267">Betikler artık bu alanların değerlerini temel alan işleme kararları almamalıdır.</span><span class="sxs-lookup"><span data-stu-id="99bfe-267">Scripts should no longer make processing decisions based on the values fo these fields.</span></span>

### <a name="azoperationalinsights-previously-azurermoperationalinsights"></a><span data-ttu-id="99bfe-268">Az.OperationalInsights (eski adıyla AzureRM.OperationalInsights)</span><span class="sxs-lookup"><span data-stu-id="99bfe-268">Az.OperationalInsights (previously AzureRM.OperationalInsights)</span></span>

- <span data-ttu-id="99bfe-269">`Get-AzOperationalInsightsDataSource` için varsayılan parametre kümesi kaldırıldı, varsayılan parametre kümesi `ByWorkspaceNameByKind` oldu</span><span class="sxs-lookup"><span data-stu-id="99bfe-269">Default parameter set for `Get-AzOperationalInsightsDataSource` is removed, and `ByWorkspaceNameByKind` has become the default parameter set</span></span>

  <span data-ttu-id="99bfe-270">Veri kaynaklarını şunu kullanarak listeleyen betikler:</span><span class="sxs-lookup"><span data-stu-id="99bfe-270">Scripts that listed data sources using</span></span>
  ```azurepowershell-interactive
  Get-AzureRmOperationalInsightsDataSource
  ```

  <span data-ttu-id="99bfe-271">Bir Tür belirtecek şekilde değiştirilmelidir</span><span class="sxs-lookup"><span data-stu-id="99bfe-271">Should be changed to specify a Kind</span></span>
  ```azurepowershell-interactive
  Get-AzOperationalInsightsDataSource -Kind AzureActivityLog
  ```

### <a name="azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery"></a><span data-ttu-id="99bfe-272">Az.RecoveryServices (eski adıyla AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup ve AzureRM.RecoveryServices.SiteRecovery)</span><span class="sxs-lookup"><span data-stu-id="99bfe-272">Az.RecoveryServices (previously AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup, and AzureRM.RecoveryServices.SiteRecovery)</span></span>

- <span data-ttu-id="99bfe-273">`New/Set-AzRecoveryServicesAsrPolicy` cmdlet’inden `Encryption` parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="99bfe-273">Removed `Encryption` parameter from `New/Set-AzRecoveryServicesAsrPolicy` cmdlet</span></span>
- <span data-ttu-id="99bfe-274">Artık `Restore-AzRecoveryServicesBackupItem` cmdlet'indeki yönetilen disk geri yükleme işlemleri için `TargetStorageAccountName` parametresi zorunludur</span><span class="sxs-lookup"><span data-stu-id="99bfe-274">`TargetStorageAccountName` parameter is now mandatory for managed disk restores in `Restore-AzRecoveryServicesBackupItem` cmdlet</span></span>
- <span data-ttu-id="99bfe-275">`Restore-AzRecoveryServicesBackupItem` cmdlet’inden `StorageAccountName` ve `StorageAccountResourceGroupName` parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="99bfe-275">Removed `StorageAccountName` and `StorageAccountResourceGroupName` parameters in `Restore-AzRecoveryServicesBackupItem` cmdlet</span></span>
- <span data-ttu-id="99bfe-276">`Get-AzRecoveryServicesBackupContainer` cmdlet’inden `Name` parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="99bfe-276">Removed `Name`parameter in `Get-AzRecoveryServicesBackupContainer` cmdlet</span></span>

### <a name="azresources-previously-azurermresources"></a><span data-ttu-id="99bfe-277">Az.Resources (eski adıyla AzureRM.Resources)</span><span class="sxs-lookup"><span data-stu-id="99bfe-277">Az.Resources (previously AzureRM.Resources)</span></span>

- <span data-ttu-id="99bfe-278">`New/Set-AzPolicyAssignment` cmdlet’inden `Sku` parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="99bfe-278">Removed `Sku` parameter from `New/Set-AzPolicyAssignment` cmdlet</span></span>
- <span data-ttu-id="99bfe-279">`New-AzADServicePrincipal` ve `New-AzADSpCredential` cmdlet’inden `Password` parametresi kaldırıldı Parolalar otomatik olarak oluşturulduğundan, daha önce parolayı sağlayan betikler:</span><span class="sxs-lookup"><span data-stu-id="99bfe-279">Removed `Password` parameter from `New-AzADServicePrincipal` and `New-AzADSpCredential` cmdlet Passwords are automatically generated, scripts that provided the password:</span></span>

  ```azurepowershell-interactive
  New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 -Password $secPassword
  ```

  <span data-ttu-id="99bfe-280">Parolayı çıktıdan alacak şekilde değiştirilmelidir:</span><span class="sxs-lookup"><span data-stu-id="99bfe-280">Should be changed to retrieve the password from the output:</span></span>

  ```azurepowershell-interactive
  $credential = New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
  $secPassword = $credential.Secret
  ```

### <a name="azservicefabric-previously-azurermservicefabric"></a><span data-ttu-id="99bfe-281">Az.ServiceFabric (eski adıyla AzureRM.ServiceFabric)</span><span class="sxs-lookup"><span data-stu-id="99bfe-281">Az.ServiceFabric (previously AzureRM.ServiceFabric)</span></span>

- <span data-ttu-id="99bfe-282">Aşağıdaki cmdlet dönüş türleri değişmiştir:</span><span class="sxs-lookup"><span data-stu-id="99bfe-282">The following cmdlet return types have been changed:</span></span>
  - <span data-ttu-id="99bfe-283">`ApplicationHealthPolicy` türündeki `ServiceTypeHealthPolicies` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="99bfe-283">The property `ServiceTypeHealthPolicies` of type `ApplicationHealthPolicy` has been removed.</span></span>
  - <span data-ttu-id="99bfe-284">`ClusterUpgradeDeltaHealthPolicy` türündeki `ApplicationHealthPolicies` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="99bfe-284">The property `ApplicationHealthPolicies` of type `ClusterUpgradeDeltaHealthPolicy` has been removed.</span></span>
  - <span data-ttu-id="99bfe-285">`ClusterUpgradePolicy` türündeki `OverrideUserUpgradePolicy` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="99bfe-285">The property `OverrideUserUpgradePolicy` of type `ClusterUpgradePolicy` has been removed.</span></span>
  - <span data-ttu-id="99bfe-286">Bu değişikliklerden aşağıdaki cmdlet’ler etkilenir:</span><span class="sxs-lookup"><span data-stu-id="99bfe-286">These changes affect the following cmdlets:</span></span>
    - <span data-ttu-id="99bfe-287">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="99bfe-287">Add-AzServiceFabricClientCertificate</span></span>
    - <span data-ttu-id="99bfe-288">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="99bfe-288">Add-AzServiceFabricClusterCertificate</span></span>
    - <span data-ttu-id="99bfe-289">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="99bfe-289">Add-AzServiceFabricNode</span></span>
    - <span data-ttu-id="99bfe-290">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="99bfe-290">Add-AzServiceFabricNodeType</span></span>
    - <span data-ttu-id="99bfe-291">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="99bfe-291">Get-AzServiceFabricCluster</span></span>
    - <span data-ttu-id="99bfe-292">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="99bfe-292">Remove-AzServiceFabricClientCertificate</span></span>
    - <span data-ttu-id="99bfe-293">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="99bfe-293">Remove-AzServiceFabricClusterCertificate</span></span>
    - <span data-ttu-id="99bfe-294">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="99bfe-294">Remove-AzServiceFabricNode</span></span>
    - <span data-ttu-id="99bfe-295">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="99bfe-295">Remove-AzServiceFabricNodeType</span></span>
    - <span data-ttu-id="99bfe-296">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="99bfe-296">Remove-AzServiceFabricSetting</span></span>
    - <span data-ttu-id="99bfe-297">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="99bfe-297">Set-AzServiceFabricSetting</span></span>
    - <span data-ttu-id="99bfe-298">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="99bfe-298">Set-AzServiceFabricUpgradeType</span></span>
    - <span data-ttu-id="99bfe-299">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="99bfe-299">Update-AzServiceFabricDurability</span></span>
    - <span data-ttu-id="99bfe-300">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="99bfe-300">Update-AzServiceFabricReliability</span></span>

### <a name="azsql-previously-azurermsql"></a><span data-ttu-id="99bfe-301">Az.Sql (eski adıyla AzureRM.Sql)</span><span class="sxs-lookup"><span data-stu-id="99bfe-301">Az.Sql (previously AzureRM.Sql)</span></span>

- <span data-ttu-id="99bfe-302">`Set-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet’inden `State` ve `ResourceId` parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="99bfe-302">Removed `State` and `ResourceId` parameters from `Set-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet</span></span>
- <span data-ttu-id="99bfe-303">Kullanım dışı cmdlet’ler kaldırıldı: `Get/Set-AzSqlServerBackupLongTermRetentionVault`, `Get/Start/Stop-AzSqlServerUpgrade`, `Get/Set-AzSqlDatabaseAuditingPolicy`, `Get/Set-AzSqlServerAuditingPolicy`, `Remove-AzSqlDatabaseAuditing`, `Remove-AzSqlServerAuditing`</span><span class="sxs-lookup"><span data-stu-id="99bfe-303">Removed deprecated cmdlets: `Get/Set-AzSqlServerBackupLongTermRetentionVault`, `Get/Start/Stop-AzSqlServerUpgrade`, `Get/Set-AzSqlDatabaseAuditingPolicy`, `Get/Set-AzSqlServerAuditingPolicy`, `Remove-AzSqlDatabaseAuditing`, `Remove-AzSqlServerAuditing`</span></span>
- <span data-ttu-id="99bfe-304">`Get-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet’inden kullanım dışı `Current` parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="99bfe-304">Removed deprecated parameter `Current` from `Get-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet</span></span>
- <span data-ttu-id="99bfe-305">`Get-AzSqlServerServiceObjective` cmdlet’inden kullanım dışı `DatabaseName` parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="99bfe-305">Removed deprecated parameter `DatabaseName` from `Get-AzSqlServerServiceObjective` cmdlet</span></span>
- <span data-ttu-id="99bfe-306">`Set-AzSqlDatabaseDataMaskingPolicy` cmdlet’inden kullanım dışı `PrivilegedLogin` parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="99bfe-306">Removed deprecated parameter `PrivilegedLogin` from `Set-AzSqlDatabaseDataMaskingPolicy` cmdlet</span></span>

### <a name="azstorage-previously-azurestorage-and-azurermstorage"></a><span data-ttu-id="99bfe-307">Az.Storage (eski adıyla Azure.Storage and AzureRM.Storage)</span><span class="sxs-lookup"><span data-stu-id="99bfe-307">Az.Storage (previously Azure.Storage and AzureRM.Storage)</span></span>

- <span data-ttu-id="99bfe-308">Yalnızca depolama hesabı adıyla bir Oauth depolama bağlamı oluşturulmasının desteklenmesi için varsayılan parametre kümesi `OAuthParameterSet` olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="99bfe-308">To support creating an Oauth storage context with only the storage account name, the default parameter set has been changed to `OAuthParameterSet`</span></span>
  - <span data-ttu-id="99bfe-309">Örnek: `$ctx = New-AzureStorageContext -StorageAccountName $accountName`</span><span class="sxs-lookup"><span data-stu-id="99bfe-309">Example: `$ctx = New-AzureStorageContext -StorageAccountName $accountName`</span></span>
- <span data-ttu-id="99bfe-310">`Get-AzStorageUsage` cmdlet’inde `Location` parametresi zorunlu hale geldi</span><span class="sxs-lookup"><span data-stu-id="99bfe-310">The `Location` parameter has become mandatory in the `Get-AzStorageUsage` cmdlet</span></span>
- <span data-ttu-id="99bfe-311">Depolama API’si metotları artık zaman uyumlu API çağrıları yerine Görev Tabanlı Zaman Uyumsuz Düzeni (TAP) kullanıyor.</span><span class="sxs-lookup"><span data-stu-id="99bfe-311">The Storage API methods now use the Task-based Asynchronous Pattern (TAP), instead of synchronous API calls.</span></span> <span data-ttu-id="99bfe-312">Aşağıdaki örneklerde yeni zaman uyumsuz komutlar gösterilir:</span><span class="sxs-lookup"><span data-stu-id="99bfe-312">The following examples demonstrate the new asynchronous commands:</span></span>

#### <a name="blob-snapshot"></a><span data-ttu-id="99bfe-313">Blob Anlık Görüntüsü</span><span class="sxs-lookup"><span data-stu-id="99bfe-313">Blob Snapshot</span></span>

<span data-ttu-id="99bfe-314">AzureRM:</span><span class="sxs-lookup"><span data-stu-id="99bfe-314">AzureRM:</span></span>

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$b.ICloudBlob.Snapshot()
```

<span data-ttu-id="99bfe-315">Az:</span><span class="sxs-lookup"><span data-stu-id="99bfe-315">Az:</span></span>

```azurepowershell-interactive
$b = Get-AzStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$task = $b.ICloudBlob.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="share-snapshot"></a><span data-ttu-id="99bfe-316">Anlık Görüntüyü Paylaş</span><span class="sxs-lookup"><span data-stu-id="99bfe-316">Share Snapshot</span></span>

<span data-ttu-id="99bfe-317">AzureRM:</span><span class="sxs-lookup"><span data-stu-id="99bfe-317">AzureRM:</span></span>

```azurepowershell-interactive
$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$snapshot = $Share.Snapshot()
```

<span data-ttu-id="99bfe-318">Az:</span><span class="sxs-lookup"><span data-stu-id="99bfe-318">Az:</span></span>

```azurepowershell-interactive
$Share = Get-AzStorageShare -Name $containerName -Context $ctx
$task = $Share.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="undelete-soft-deleted-blob"></a><span data-ttu-id="99bfe-319">Geçici silinen blob’un silinmesini geri al</span><span class="sxs-lookup"><span data-stu-id="99bfe-319">Undelete soft-deleted blob</span></span>

<span data-ttu-id="99bfe-320">AzureRM:</span><span class="sxs-lookup"><span data-stu-id="99bfe-320">AzureRM:</span></span>

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$b.ICloudBlob.Undelete()
```

<span data-ttu-id="99bfe-321">Az:</span><span class="sxs-lookup"><span data-stu-id="99bfe-321">Az:</span></span>

```azurepowershell-interactive
$b = Get-AzStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$task = $b.ICloudBlob.UndeleteAsync()
$task.Wait()
```

#### <a name="set-blob-tier"></a><span data-ttu-id="99bfe-322">Blob Katmanını Ayarla</span><span class="sxs-lookup"><span data-stu-id="99bfe-322">Set Blob Tier</span></span>

<span data-ttu-id="99bfe-323">AzureRM:</span><span class="sxs-lookup"><span data-stu-id="99bfe-323">AzureRM:</span></span>

```azurepowershell-interactive
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$blockBlob.ICloudBlob.SetStandardBlobTier("hot")

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$pageBlob.ICloudBlob.SetPremiumBlobTier("P4")
```

<span data-ttu-id="99bfe-324">Az:</span><span class="sxs-lookup"><span data-stu-id="99bfe-324">Az:</span></span>

```azurepowershell-interactive
$blockBlob = Get-AzStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$task = $blockBlob.ICloudBlob.SetStandardBlobTierAsync("hot")
$task.Wait()

$pageBlob = Get-AzStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$task = $pageBlob.ICloudBlob.SetPremiumBlobTierAsync("P4")
$task.Wait()
```

### <a name="azwebsites-previously-azurermwebsites"></a><span data-ttu-id="99bfe-325">Az.Websites (eski adıyla AzureRM.Websites)</span><span class="sxs-lookup"><span data-stu-id="99bfe-325">Az.Websites (previously AzureRM.Websites)</span></span>

- <span data-ttu-id="99bfe-326">`PSAppServicePlan`, `PSCertificate`, `PSCloningInfo` ve `PSSite` nesnesinden kullanım dışı özellikler kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="99bfe-326">Removed deprecated properties from the `PSAppServicePlan`, `PSCertificate`, `PSCloningInfo`, and `PSSite` objects</span></span>
