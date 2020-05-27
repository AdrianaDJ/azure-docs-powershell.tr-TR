---
title: AzureRM'den Azure PowerShell Az 1.0.0’a tüm değişiklikler
description: Bu geçiş kılavuzu, Azure PowerShell Az sürüm 1 yayınında yapılan yeni değişikliklerin listesini içerir.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2019
ms.openlocfilehash: d2e67ada70fed91a939dc72935e2fa639c731002
ms.sourcegitcommit: 7839b82f47ef8dd522eff900081c22de0d089cfc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/14/2020
ms.locfileid: "83387029"
---
# <a name="breaking-changes-for-az-100"></a><span data-ttu-id="2859a-103">Az 1.0.0 için yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="2859a-103">Breaking changes for Az 1.0.0</span></span>

<span data-ttu-id="2859a-104">Bu belge, AzureRM 6.x ve yeni Az modülü (sürüm 1.x ve sonrası) arasındaki değişiklikler hakkında ayrıntılı bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="2859a-104">This document provides detailed information on the changes between AzureRM 6.x and the new Az module, version 1.x and later.</span></span> <span data-ttu-id="2859a-105">İçindekiler tablosu, betiklerinizi etkileyebilecek modüle özgü değişiklikler de dahil olmak üzere, tam geçiş yolunda size kılavuzluk edecektir.</span><span class="sxs-lookup"><span data-stu-id="2859a-105">The table of contents will help guide you through a full migration path, including module-specific changes that may affect your scripts.</span></span>

<span data-ttu-id="2859a-106">AzureRM’den Az’ye geçiş işlemine başlangıç konusunda genel öneriler için bkz. [AzureRM’den Az modülüne geçişi başlatma](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="2859a-106">For general advice on getting started with a migration from AzureRM to Az, see [Start migration from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="2859a-107">İçindekiler</span><span class="sxs-lookup"><span data-stu-id="2859a-107">Table of Contents</span></span>

- [<span data-ttu-id="2859a-108">Hataya neden olan genel değişiklikler</span><span class="sxs-lookup"><span data-stu-id="2859a-108">General breaking changes</span></span>](#general-breaking-changes)
  - [<span data-ttu-id="2859a-109">Cmdlet isim ön eki değişiklikleri</span><span class="sxs-lookup"><span data-stu-id="2859a-109">Cmdlet noun prefix changes</span></span>](#cmdlet-noun-prefix-changes)
  - [<span data-ttu-id="2859a-110">Modül adı değişiklikleri</span><span class="sxs-lookup"><span data-stu-id="2859a-110">Module name changes</span></span>](#module-name-changes)
  - [<span data-ttu-id="2859a-111">Kaldırılan modüller</span><span class="sxs-lookup"><span data-stu-id="2859a-111">Removed modules</span></span>](#removed-modules)
  - [<span data-ttu-id="2859a-112">Windows PowerShell 5.1 ve .NET 4.7.2</span><span class="sxs-lookup"><span data-stu-id="2859a-112">Windows PowerShell 5.1 and .NET 4.7.2</span></span>](#windows-powershell-51-and-net-472)
  - [<span data-ttu-id="2859a-113">PSCredential ile kullanıcı oturumu açmanın geçici olarak kaldırılması</span><span class="sxs-lookup"><span data-stu-id="2859a-113">Temporary removal of user login using PSCredential</span></span>](#temporary-removal-of-user-login-using-pscredential)
  - [<span data-ttu-id="2859a-114">Web tarayıcısı istemi yerine varsayılan cihaz kodu ile oturum açma</span><span class="sxs-lookup"><span data-stu-id="2859a-114">Default device code login instead of web browser prompt</span></span>](#default-device-code-login-instead-of-web-browser-prompt)
- [<span data-ttu-id="2859a-115">Modüldeki yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="2859a-115">Module breaking changes</span></span>](#module-breaking-changes)
  - [<span data-ttu-id="2859a-116">Az.ApiManagement (eski adıyla AzureRM.ApiManagement)</span><span class="sxs-lookup"><span data-stu-id="2859a-116">Az.ApiManagement (previously AzureRM.ApiManagement)</span></span>](#azapimanagement-previously-azurermapimanagement)
  - [<span data-ttu-id="2859a-117">Az.Billing (eski adıyla AzureRM.Billing, AzureRM.Consumption ve AzureRM.UsageAggregates)</span><span class="sxs-lookup"><span data-stu-id="2859a-117">Az.Billing (previously AzureRM.Billing, AzureRM.Consumption, and AzureRM.UsageAggregates)</span></span>](#azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates)
  - [<span data-ttu-id="2859a-118">Az.CognitiveServices (eski adıyla AzureRM.CognitiveServices)</span><span class="sxs-lookup"><span data-stu-id="2859a-118">Az.CognitiveServices (previously AzureRM.CognitiveServices)</span></span>](#azcognitiveservices-previously-azurermcognitiveservices)
  - [<span data-ttu-id="2859a-119">Az.Compute (eski adıyla AzureRM.Compute)</span><span class="sxs-lookup"><span data-stu-id="2859a-119">Az.Compute (previously AzureRM.Compute)</span></span>](#azcompute-previously-azurermcompute)
  - [<span data-ttu-id="2859a-120">Az.DataFactory (eski adıyla AzureRM.DataFactories ve AzureRM.DataFactoryV2)</span><span class="sxs-lookup"><span data-stu-id="2859a-120">Az.DataFactory (previously AzureRM.DataFactories and AzureRM.DataFactoryV2)</span></span>](#azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2)
  - [<span data-ttu-id="2859a-121">Az.DataLakeAnalytics (eski adıyla AzureRM.DataLakeAnalytics)</span><span class="sxs-lookup"><span data-stu-id="2859a-121">Az.DataLakeAnalytics (previously AzureRM.DataLakeAnalytics)</span></span>](#azdatalakeanalytics-previously-azurermdatalakeanalytics)
  - [<span data-ttu-id="2859a-122">Az.DataLakeStore (eski adıyla AzureRM.DataLakeStore)</span><span class="sxs-lookup"><span data-stu-id="2859a-122">Az.DataLakeStore (previously AzureRM.DataLakeStore)</span></span>](#azdatalakestore-previously-azurermdatalakestore)
  - [<span data-ttu-id="2859a-123">Az.KeyVault (eski adıyla AzureRM.KeyVault)</span><span class="sxs-lookup"><span data-stu-id="2859a-123">Az.KeyVault (previously AzureRM.KeyVault)</span></span>](#azkeyvault-previously-azurermkeyvault)
  - [<span data-ttu-id="2859a-124">Az.Media (eski adıyla AzureRM.Media)</span><span class="sxs-lookup"><span data-stu-id="2859a-124">Az.Media (previously AzureRM.Media)</span></span>](#azmedia-previously-azurermmedia)
  - [<span data-ttu-id="2859a-125">Az.Monitor (eski adıyla AzureRM.Insights)</span><span class="sxs-lookup"><span data-stu-id="2859a-125">Az.Monitor (previously AzureRM.Insights)</span></span>](#azmonitor-previously-azurerminsights)
  - [<span data-ttu-id="2859a-126">Az.Network (eski adıyla AzureRM.Network)</span><span class="sxs-lookup"><span data-stu-id="2859a-126">Az.Network (previously AzureRM.Network)</span></span>](#aznetwork-previously-azurermnetwork)
  - [<span data-ttu-id="2859a-127">Az.OperationalInsights (eski adıyla AzureRM.OperationalInsights)</span><span class="sxs-lookup"><span data-stu-id="2859a-127">Az.OperationalInsights (previously AzureRM.OperationalInsights)</span></span>](#azoperationalinsights-previously-azurermoperationalinsights)
  - [<span data-ttu-id="2859a-128">Az.RecoveryServices (eski adıyla AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup ve AzureRM.RecoveryServices.SiteRecovery)</span><span class="sxs-lookup"><span data-stu-id="2859a-128">Az.RecoveryServices (previously AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup, and AzureRM.RecoveryServices.SiteRecovery)</span></span>](#azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery)
  - [<span data-ttu-id="2859a-129">Az.Resources (eski adıyla AzureRM.Resources)</span><span class="sxs-lookup"><span data-stu-id="2859a-129">Az.Resources (previously AzureRM.Resources)</span></span>](#azresources-previously-azurermresources)
  - [<span data-ttu-id="2859a-130">Az.ServiceFabric (eski adıyla AzureRM.ServiceFabric)</span><span class="sxs-lookup"><span data-stu-id="2859a-130">Az.ServiceFabric (previously AzureRM.ServiceFabric)</span></span>](#azservicefabric-previously-azurermservicefabric)
  - [<span data-ttu-id="2859a-131">Az.Sql (eski adıyla AzureRM.Sql)</span><span class="sxs-lookup"><span data-stu-id="2859a-131">Az.Sql (previously AzureRM.Sql)</span></span>](#azsql-previously-azurermsql)
  - [<span data-ttu-id="2859a-132">Az.Storage (eski adıyla Azure.Storage and AzureRM.Storage)</span><span class="sxs-lookup"><span data-stu-id="2859a-132">Az.Storage (previously Azure.Storage and AzureRM.Storage)</span></span>](#azstorage-previously-azurestorage-and-azurermstorage)
  - [<span data-ttu-id="2859a-133">Az.Websites (eski adıyla AzureRM.Websites)</span><span class="sxs-lookup"><span data-stu-id="2859a-133">Az.Websites (previously AzureRM.Websites)</span></span>](#azwebsites-previously-azurermwebsites)

## <a name="general-breaking-changes"></a><span data-ttu-id="2859a-134">Hataya neden olan genel değişiklikler</span><span class="sxs-lookup"><span data-stu-id="2859a-134">General breaking changes</span></span>

<span data-ttu-id="2859a-135">Bu bölümde, Az modülünün yeniden tasarımının bir parçası olan, hataya neden olan genel değişiklikler ayrıntılı olarak açıklanır.</span><span class="sxs-lookup"><span data-stu-id="2859a-135">This section details the general breaking changes that are part of the redesign of the Az module.</span></span>

### <a name="cmdlet-noun-prefix-changes"></a><span data-ttu-id="2859a-136">Cmdlet İsim Öneki Değişiklikleri</span><span class="sxs-lookup"><span data-stu-id="2859a-136">Cmdlet Noun Prefix Changes</span></span>

<span data-ttu-id="2859a-137">AzureRM modülünde cmdlet’ler isim ön eki olarak `AzureRM` veya `Azure` kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2859a-137">In the AzureRM module, cmdlets used either `AzureRM` or `Azure` as a noun prefix.</span></span>  <span data-ttu-id="2859a-138">Az ile birlikte cmdlet adları basitleştirilip normalleştirilerek tüm cmdlet’lerin isim ön eki olarak 'Az' kullanılacak.</span><span class="sxs-lookup"><span data-stu-id="2859a-138">Az simplifies and normalizes cmdlet names, so that all cmdlets use 'Az' as their cmdlet noun prefix.</span></span> <span data-ttu-id="2859a-139">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="2859a-139">For example:</span></span>

```azurepowershell-interactive
Get-AzureRMVM
Get-AzureKeyVaultSecret
```

<span data-ttu-id="2859a-140">Yeni ad:</span><span class="sxs-lookup"><span data-stu-id="2859a-140">Has changed to:</span></span>

```azurepowershell-interactive
Get-AzVM
Get-AzKeyVaultSecret
```

<span data-ttu-id="2859a-141">Bu yeni cmdlet adlarına geçişi kolaylaştırmak için Az ile birlikte iki yeni cmdlet sunuluyor: [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) ve [Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias).</span><span class="sxs-lookup"><span data-stu-id="2859a-141">To make the transition to these new cmdlet names simpler, Az introduces two new cmdlets, [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) and [Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias).</span></span>  <span data-ttu-id="2859a-142">`Enable-AzureRmAlias`, AzureRM’deki eski cmdlet adları için yeni Az cmdlet adlarına eşlenen diğer adlar oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2859a-142">`Enable-AzureRmAlias` creates aliases for the older cmdlet names in AzureRM that map to the newer Az cmdlet names.</span></span> <span data-ttu-id="2859a-143">`Enable-AzureRmAlias` ile `-Scope` bağımsız değişkenini kullanarak diğer adları nerede etkinleştireceğinizi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2859a-143">Using the `-Scope` argument with `Enable-AzureRmAlias` allows you to choose where aliases are enabled.</span></span>

<span data-ttu-id="2859a-144">Örneğin, şu AzureRM betiği:</span><span class="sxs-lookup"><span data-stu-id="2859a-144">For example, the following script in AzureRM:</span></span>

```azurepowershell-interactive
#Requires -Modules AzureRM.Storage
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="2859a-145">`Enable-AzureRmAlias` kullanılarak küçük değişikliklerle çalıştırılabilir:</span><span class="sxs-lookup"><span data-stu-id="2859a-145">Can be run with minimal changes using `Enable-AzureRmAlias`:</span></span>

```azurepowershell-interactive
#Requires -Modules Az.Storage
Enable-AzureRmAlias -Scope Process
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="2859a-146">`Enable-AzureRmAlias -Scope CurrentUser` çalıştırıldığında açtığınız tüm PowerShell oturumları için diğer adları etkinleştireceğinden, bu cmdlet’i çalıştırdıktan sonra şunun gibi bir betiğin hiç değiştirilmesi gerekmez:</span><span class="sxs-lookup"><span data-stu-id="2859a-146">Running `Enable-AzureRmAlias -Scope CurrentUser` will enable the aliases for all PowerShell sessions you open, so that after executing this cmdlet, a script like this would not need to be changed at all:</span></span>

```azurepowershell-interactive
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="2859a-147">Diğer ad cmdlet’leri kullanımının tüm ayrıntıları için bkz. [Enable-AzureRmAlias başvurusu](/powershell/module/az.accounts/enable-azurermalias).</span><span class="sxs-lookup"><span data-stu-id="2859a-147">For complete details on the usage of the alias cmdlets, see the [Enable-AzureRmAlias reference](/powershell/module/az.accounts/enable-azurermalias).</span></span>

<span data-ttu-id="2859a-148">Diğer adları devre dışı bırakmaya hazır olduğunuzda `Disable-AzureRmAlias` cmdlet'i oluşturulan diğer adları kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2859a-148">When you're ready to disable aliases, `Disable-AzureRmAlias` removes the created aliases.</span></span> <span data-ttu-id="2859a-149">Tüm ayrıntıları için bkz. [Disable-AzureRmAlias başvurusu](/powershell/module/az.accounts/disable-azurermalias).</span><span class="sxs-lookup"><span data-stu-id="2859a-149">For complete details, see the [Disable-AzureRmAlias reference](/powershell/module/az.accounts/disable-azurermalias).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2859a-150">Diğer adları devre dışı bırakırken, diğer adların etkin olduğu _tüm_ kapsamlarda devre dışı bırakıldıklarından emin olun.</span><span class="sxs-lookup"><span data-stu-id="2859a-150">When disabling aliases, make sure that they are disabled for _all_ scopes which had aliases enabled.</span></span>

### <a name="module-name-changes"></a><span data-ttu-id="2859a-151">Modül Adı Değişiklikleri</span><span class="sxs-lookup"><span data-stu-id="2859a-151">Module Name Changes</span></span>

<span data-ttu-id="2859a-152">Aşağıdaki modüller dışında, önceden `AzureRM.*` olan modül adları `Az.*` olarak değiştirildi:</span><span class="sxs-lookup"><span data-stu-id="2859a-152">The module names have changed from `AzureRM.*` to `Az.*`, except for the following modules:</span></span>

| <span data-ttu-id="2859a-153">AzureRM modülü</span><span class="sxs-lookup"><span data-stu-id="2859a-153">AzureRM module</span></span> | <span data-ttu-id="2859a-154">Az modülü</span><span class="sxs-lookup"><span data-stu-id="2859a-154">Az module</span></span> |
|----------------|-----------|
| <span data-ttu-id="2859a-155">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="2859a-155">Azure.Storage</span></span> | <span data-ttu-id="2859a-156">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2859a-156">Az.Storage</span></span> |
| <span data-ttu-id="2859a-157">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2859a-157">Azure.AnalysisServices</span></span> | <span data-ttu-id="2859a-158">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2859a-158">Az.AnalysisServices</span></span> |
| <span data-ttu-id="2859a-159">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="2859a-159">AzureRM.Profile</span></span> | <span data-ttu-id="2859a-160">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2859a-160">Az.Accounts</span></span> |
| <span data-ttu-id="2859a-161">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="2859a-161">AzureRM.Insights</span></span> | <span data-ttu-id="2859a-162">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2859a-162">Az.Monitor</span></span> |
| <span data-ttu-id="2859a-163">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="2859a-163">AzureRM.DataFactories</span></span> | <span data-ttu-id="2859a-164">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2859a-164">Az.DataFactory</span></span> |
| <span data-ttu-id="2859a-165">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="2859a-165">AzureRM.DataFactoryV2</span></span> | <span data-ttu-id="2859a-166">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2859a-166">Az.DataFactory</span></span> |
| <span data-ttu-id="2859a-167">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="2859a-167">AzureRM.RecoveryServices.Backup</span></span> | <span data-ttu-id="2859a-168">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2859a-168">Az.RecoveryServices</span></span> |
| <span data-ttu-id="2859a-169">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="2859a-169">AzureRM.RecoveryServices.SiteRecovery</span></span> | <span data-ttu-id="2859a-170">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2859a-170">Az.RecoveryServices</span></span> |
| <span data-ttu-id="2859a-171">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="2859a-171">AzureRM.Tags</span></span> | <span data-ttu-id="2859a-172">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2859a-172">Az.Resources</span></span> |
| <span data-ttu-id="2859a-173">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="2859a-173">AzureRM.MachineLearningCompute</span></span> | <span data-ttu-id="2859a-174">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="2859a-174">Az.MachineLearning</span></span> |
| <span data-ttu-id="2859a-175">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="2859a-175">AzureRM.UsageAggregates</span></span> | <span data-ttu-id="2859a-176">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="2859a-176">Az.Billing</span></span> |
| <span data-ttu-id="2859a-177">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="2859a-177">AzureRM.Consumption</span></span> | <span data-ttu-id="2859a-178">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="2859a-178">Az.Billing</span></span> |

<span data-ttu-id="2859a-179">Modül adlarındaki değişiklikler nedeniyle, belirli modülleri yüklemek için `#Requires` ve `Import-Module` deyimlerini kullanan tüm betiklerin yeni modülü kullanacak şekilde güncelleştirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="2859a-179">The changes in module names mean that any script that uses `#Requires` or `Import-Module` to load specific modules will need to be changed to use the new module instead.</span></span> <span data-ttu-id="2859a-180">Cmdlet sonekinin değişmediği modüllerde bu, modül adı değişmiş olsa da işlem alanını belirten sonekin _değişmediği_ anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="2859a-180">For modules where the cmdlet suffix has not changed, this means that although the module name has changed, the suffix indicating the operation space has _not_.</span></span>

#### <a name="migrating-requires-and-import-module-statements"></a><span data-ttu-id="2859a-181">#Requires ve Import-Module Deyimlerini Geçirme</span><span class="sxs-lookup"><span data-stu-id="2859a-181">Migrating #Requires and Import-Module Statements</span></span>

<span data-ttu-id="2859a-182">AzureRM modüllerine bağımlılığı bildirmek için `#Requires` veya `Import-Module` deyimini kullanan betikler yeni modül adlarını kullanacak şekilde güncelleştirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="2859a-182">Scripts that use `#Requires` or `Import-Module` to declare a dependency on AzureRM modules must be updated to use the new module names.</span></span> <span data-ttu-id="2859a-183">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="2859a-183">For example:</span></span>

```azurepowershell-interactive
#Requires -Module AzureRM.Compute
```

<span data-ttu-id="2859a-184">Şöyle değiştirilmelidir:</span><span class="sxs-lookup"><span data-stu-id="2859a-184">Should be changed to:</span></span>

```azurepowershell-interactive
#Requires -Module Az.Compute
```

<span data-ttu-id="2859a-185">`Import-Module` için:</span><span class="sxs-lookup"><span data-stu-id="2859a-185">For `Import-Module`:</span></span>

```azurepowershell-interactive
Import-Module -Name AzureRM.Compute
```

<span data-ttu-id="2859a-186">Şöyle değiştirilmelidir:</span><span class="sxs-lookup"><span data-stu-id="2859a-186">Should be changed to:</span></span>

```azurepowershell-interactive
Import-Module -Name Az.Compute
```

### <a name="migrating-fully-qualified-cmdlet-invocations"></a><span data-ttu-id="2859a-187">Tam Olarak Nitelenen Cmdlet Çağrılarını Geçirme</span><span class="sxs-lookup"><span data-stu-id="2859a-187">Migrating Fully-Qualified Cmdlet Invocations</span></span>

<span data-ttu-id="2859a-188">Şunun gibi modül adıyla nitelenen cmdlet çağrılarını kullanan betikler:</span><span class="sxs-lookup"><span data-stu-id="2859a-188">Scripts that use module-qualified cmdlet invocations, such as:</span></span>

```azurepowershell-interactive
AzureRM.Compute\Get-AzureRmVM
```

<span data-ttu-id="2859a-189">Yeni modülü ve cmdlet adlarını kullanacak şekilde değiştirilmelidir:</span><span class="sxs-lookup"><span data-stu-id="2859a-189">Must be changed to use the new module and cmdlet names:</span></span>

```azurepowershell-interactive
Az.Compute\Get-AzVM
```

### <a name="migrating-module-manifest-dependencies"></a><span data-ttu-id="2859a-190">Modül bildirimi bağımlılıklarını geçirme</span><span class="sxs-lookup"><span data-stu-id="2859a-190">Migrating module manifest dependencies</span></span>

<span data-ttu-id="2859a-191">Bir modül bildirimi (.psd1) dosyası aracılığıyla AzureRM modüllerine bağımlılığı ifade eden modüllerin `RequiredModules` bölümünde güncelleştirilmiş modül adları olmalıdır:</span><span class="sxs-lookup"><span data-stu-id="2859a-191">Modules that express dependencies on AzureRM modules through a module manifest (.psd1) file will need to updated the module names in their `RequiredModules` section:</span></span>

```powershell
RequiredModules = @(@{ModuleName="AzureRM.Profile"; ModuleVersion="5.8.2"})
```

<span data-ttu-id="2859a-192">Şöyle değiştirilmelidir:</span><span class="sxs-lookup"><span data-stu-id="2859a-192">Must be changed to:</span></span>

```powershell
RequiredModules = @(@{ModuleName="Az.Profile"; ModuleVersion="1.0.0"})
```

### <a name="removed-modules"></a><span data-ttu-id="2859a-193">Kaldırılan modüller</span><span class="sxs-lookup"><span data-stu-id="2859a-193">Removed modules</span></span>

<span data-ttu-id="2859a-194">Aşağıdaki modüller kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="2859a-194">The following modules have been removed:</span></span>

- `AzureRM.Backup`
- `AzureRM.Compute.ManagedService`
- `AzureRM.Scheduler`

<span data-ttu-id="2859a-195">Bu hizmetlere yönelik araçlar artık etkin bir şekilde desteklenmemektedir.</span><span class="sxs-lookup"><span data-stu-id="2859a-195">The tools for these services are no longer actively supported.</span></span>  <span data-ttu-id="2859a-196">Müşterilerin uygun olan en yakın zamanda alternatif hizmetlere geçmesi önerilir.</span><span class="sxs-lookup"><span data-stu-id="2859a-196">Customers are encouraged to move to alternative services as soon as it is convenient.</span></span>

### <a name="windows-powershell-51-and-net-472"></a><span data-ttu-id="2859a-197">Windows PowerShell 5.1 ve .NET 4.7.2</span><span class="sxs-lookup"><span data-stu-id="2859a-197">Windows PowerShell 5.1 and .NET 4.7.2</span></span>

<span data-ttu-id="2859a-198">Windows için PowerShell 5.1 ile Az kullanımı, .NET Framework 4.7.2 sürümünün yüklenmesini gerektirir.</span><span class="sxs-lookup"><span data-stu-id="2859a-198">Using Az with PowerShell 5.1 for Windows requires the installation of .NET Framework 4.7.2.</span></span> <span data-ttu-id="2859a-199">PowerShell Core 6.x ve sonraki sürümleri .NET Framework gerektirmez.</span><span class="sxs-lookup"><span data-stu-id="2859a-199">Using PowerShell Core 6.x or later does not require .NET Framework.</span></span>

### <a name="temporary-removal-of-user-login-using-pscredential"></a><span data-ttu-id="2859a-200">PSCredential ile Kullanıcı oturumu açmanın geçici olarak kaldırılması</span><span class="sxs-lookup"><span data-stu-id="2859a-200">Temporary removal of User login using PSCredential</span></span>

<span data-ttu-id="2859a-201">.NET Standard kimlik doğrulama akışındaki değişiklikler nedeniyle, PSCredential üzerinden kullanıcı oturumu açmayı geçici olarak kaldırıyoruz.</span><span class="sxs-lookup"><span data-stu-id="2859a-201">Due to changes in the authentication flow for .NET Standard, we are temporarily removing user login via PSCredential.</span></span> <span data-ttu-id="2859a-202">Bu özellik, Windows için PowerShell 5.1’in 15/1/2019 tarihli yayınında yeniden kullanıma sunulacaktır.</span><span class="sxs-lookup"><span data-stu-id="2859a-202">This capability will be re-introduced in the 1/15/2019 release for PowerShell 5.1 for Windows.</span></span> <span data-ttu-id="2859a-203">Bu konu, [bu GitHub sorununda](https://github.com/Azure/azure-powershell/issues/7430) ayrıntılı olarak açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="2859a-203">This is discussed in detail in [this GitHub issue.](https://github.com/Azure/azure-powershell/issues/7430)</span></span>

### <a name="default-device-code-login-instead-of-web-browser-prompt"></a><span data-ttu-id="2859a-204">Web tarayıcısı istemi yerine varsayılan cihaz kodu ile oturum açma</span><span class="sxs-lookup"><span data-stu-id="2859a-204">Default device code login instead of web browser prompt</span></span>

<span data-ttu-id="2859a-205">.NET Standard kimlik doğrulama akışındaki değişiklikler nedeniyle, etkileşimli oturum açma sırasında varsayılan oturum açma akışı olarak cihazla oturum açmayı kullanıyoruz.</span><span class="sxs-lookup"><span data-stu-id="2859a-205">Due to changes in the authentication flow for .NET Standard, we are using device login as the default login flow during interactive login.</span></span> <span data-ttu-id="2859a-206">Web tarayıcısı tabanlı oturum açma, Windows için PowerShell 5.1'de 15/1/2019 tarihli yayınla birlikte yeniden varsayılan seçenek olarak kullanıma sunulacaktır.</span><span class="sxs-lookup"><span data-stu-id="2859a-206">Web browser based login will be re-introduced for PowerShell 5.1 for Windows as the default in the 1/15/2019 release.</span></span> <span data-ttu-id="2859a-207">İlgili tarihte, kullanıcılar bir Switch parametresini kullanarak cihaz oturumunu seçebilecek.</span><span class="sxs-lookup"><span data-stu-id="2859a-207">At that time, users will be able to choose device login using a Switch parameter.</span></span>

## <a name="module-breaking-changes"></a><span data-ttu-id="2859a-208">Modüldeki yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="2859a-208">Module breaking changes</span></span>

<span data-ttu-id="2859a-209">Bu bölümde, belirli modüller ve cmdlet’lerde hataya neden olan değişiklikler ayrıntılı olarak açıklanır.</span><span class="sxs-lookup"><span data-stu-id="2859a-209">This section details specific breaking changes for individual modules and cmdlets.</span></span>

### <a name="azapimanagement-previously-azurermapimanagement"></a><span data-ttu-id="2859a-210">Az.ApiManagement (eski adıyla AzureRM.ApiManagement)</span><span class="sxs-lookup"><span data-stu-id="2859a-210">Az.ApiManagement (previously AzureRM.ApiManagement)</span></span>

- <span data-ttu-id="2859a-211">Aşağıdaki cmdlet’ler kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="2859a-211">Removed the following cmdlets:</span></span>
  - <span data-ttu-id="2859a-212">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="2859a-212">New-AzureRmApiManagementHostnameConfiguration</span></span>
  - <span data-ttu-id="2859a-213">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="2859a-213">Set-AzureRmApiManagementHostnames</span></span>
  - <span data-ttu-id="2859a-214">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="2859a-214">Update-AzureRmApiManagementDeployment</span></span>
  - <span data-ttu-id="2859a-215">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="2859a-215">Import-AzureRmApiManagementHostnameCertificate</span></span>
  - <span data-ttu-id="2859a-216">Bu özellikleri ayarlamak için bunun yerine **Set-AzApiManagement** cmdlet’ini kullanın</span><span class="sxs-lookup"><span data-stu-id="2859a-216">Use **Set-AzApiManagement** cmdlet to set these properties instead</span></span>
- <span data-ttu-id="2859a-217">Aşağıdaki özellikler kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="2859a-217">Removed the following properties:</span></span>
  - <span data-ttu-id="2859a-218">`PsApiManagementContext` öğesinden `PsApiManagementHostnameConfiguration` türündeki `PortalHostnameConfiguration`, `ProxyHostnameConfiguration`, `ManagementHostnameConfiguration` ve `ScmHostnameConfiguration` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="2859a-218">Removed property `PortalHostnameConfiguration`, `ProxyHostnameConfiguration`, `ManagementHostnameConfiguration` and `ScmHostnameConfiguration` of type `PsApiManagementHostnameConfiguration` from `PsApiManagementContext`.</span></span> <span data-ttu-id="2859a-219">Bunun yerine `PsApiManagementCustomHostNameConfiguration` türündeki `PortalCustomHostnameConfiguration`, `ProxyCustomHostnameConfiguration`, `ManagementCustomHostnameConfiguration` ve `ScmCustomHostnameConfiguration` özelliğini kullanın.</span><span class="sxs-lookup"><span data-stu-id="2859a-219">Instead use `PortalCustomHostnameConfiguration`, `ProxyCustomHostnameConfiguration`, `ManagementCustomHostnameConfiguration` and `ScmCustomHostnameConfiguration` of type `PsApiManagementCustomHostNameConfiguration`.</span></span>
  - <span data-ttu-id="2859a-220">PsApiManagementContext öğesinden `StaticIPs` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="2859a-220">Removed property `StaticIPs` from PsApiManagementContext.</span></span> <span data-ttu-id="2859a-221">Özellik `PublicIPAddresses` ve `PrivateIPAddresses` olarak bölündü.</span><span class="sxs-lookup"><span data-stu-id="2859a-221">The property has been split into `PublicIPAddresses` and `PrivateIPAddresses`.</span></span>
  - <span data-ttu-id="2859a-222">New-AzureApiManagementVirtualNetwork cmdlet’inden gerekli olan `Location` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="2859a-222">Removed required property `Location` from New-AzureApiManagementVirtualNetwork cmdlet.</span></span>

### <a name="azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates"></a><span data-ttu-id="2859a-223">Az.Billing (eski adıyla AzureRM.Billing, AzureRM.Consumption ve AzureRM.UsageAggregates)</span><span class="sxs-lookup"><span data-stu-id="2859a-223">Az.Billing (previously AzureRM.Billing, AzureRM.Consumption, and AzureRM.UsageAggregates)</span></span>

- <span data-ttu-id="2859a-224">`Get-AzConsumptionUsageDetail` cmdlet’inden `InvoiceName` parametresi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="2859a-224">The `InvoiceName` parameter was removed from the `Get-AzConsumptionUsageDetail` cmdlet.</span></span>  <span data-ttu-id="2859a-225">Fatura için betiklerin diğer kimlik parametrelerini kullanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="2859a-225">Scripts will need to use other identity parameters for the invoice.</span></span>

### <a name="azcognitiveservices-previously-azurermcognitiveservices"></a><span data-ttu-id="2859a-226">Az.CognitiveServices (eski adıyla AzureRM.CognitiveServices)</span><span class="sxs-lookup"><span data-stu-id="2859a-226">Az.CognitiveServices (previously AzureRM.CognitiveServices)</span></span>

- <span data-ttu-id="2859a-227">`Get-AzCognitiveServicesAccountSkus` cmdlet’inden `GetSkusWithAccountParamSetName` parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="2859a-227">Removed `GetSkusWithAccountParamSetName` parameter set from `Get-AzCognitiveServicesAccountSkus` cmdlet.</span></span>  <span data-ttu-id="2859a-228">ResourceGroupName ve Hesap Adı parametrelerini kullanmak yerine Sku’ları Hesap Türüne ve Konuma göre almalısınız.</span><span class="sxs-lookup"><span data-stu-id="2859a-228">You must get Skus by Account Type and Location, instead of using ResourceGroupName and Account Name.</span></span>

### <a name="azcompute-previously-azurermcompute"></a><span data-ttu-id="2859a-229">Az.Compute (eski adıyla AzureRM.Compute)</span><span class="sxs-lookup"><span data-stu-id="2859a-229">Az.Compute (previously AzureRM.Compute)</span></span>

- <span data-ttu-id="2859a-230">`PSVirtualMachine` ve `PSVirtualMachineScaleSet` nesnelerinde `Identity` özelliğinden `IdentityIds` kaldırıldı Betikler artık işleme kararları vermek için bu alanın değerini kullanmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="2859a-230">`IdentityIds` are removed from `Identity` property in `PSVirtualMachine` and `PSVirtualMachineScaleSet` objects Scripts should no longer use the value of this field to make processing decisions.</span></span>
- <span data-ttu-id="2859a-231">`PSVirtualMachineScaleSetVM` nesnesinin `InstanceView` özelliğinin `VirtualMachineInstanceView` olan türü `VirtualMachineScaleSetVMInstanceView` olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="2859a-231">The type of `InstanceView` property of `PSVirtualMachineScaleSetVM` object is changed from `VirtualMachineInstanceView` to `VirtualMachineScaleSetVMInstanceView`</span></span>
- <span data-ttu-id="2859a-232">`UpgradePolicy` özelliğinden `AutoOSUpgradePolicy` ve `AutomaticOSUpgrade` özelliği kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="2859a-232">`AutoOSUpgradePolicy` and `AutomaticOSUpgrade` properties are removed from `UpgradePolicy` property</span></span>
- <span data-ttu-id="2859a-233">`PSSnapshotUpdate` nesnesindeki `Sku` özelliğinin `DiskSku` olan türü `SnapshotSku` olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="2859a-233">The type of `Sku` property in `PSSnapshotUpdate` object is changed from `DiskSku` to `SnapshotSku`</span></span>
- <span data-ttu-id="2859a-234">`VmScaleSetVMParameterSet`, `Add-AzVMDataDisk` cmdlet’inden kaldırıldığından artık bir veri diskini ScaleSet VM’sine tek başına ekleyemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="2859a-234">`VmScaleSetVMParameterSet` is removed from `Add-AzVMDataDisk` cmdlet, you can no longer add a data disk individually to a ScaleSet VM.</span></span>

### <a name="azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2"></a><span data-ttu-id="2859a-235">Az.DataFactory (eski adıyla AzureRM.DataFactories ve AzureRM.DataFactoryV2)</span><span class="sxs-lookup"><span data-stu-id="2859a-235">Az.DataFactory (previously AzureRM.DataFactories and AzureRM.DataFactoryV2)</span></span>

- <span data-ttu-id="2859a-236">`New-AzDataFactoryEncryptValue` cmdlet’inde `GatewayName` parametresi zorunlu hale geldi</span><span class="sxs-lookup"><span data-stu-id="2859a-236">The `GatewayName` parameter has become mandatory in the `New-AzDataFactoryEncryptValue` cmdlet</span></span>
- <span data-ttu-id="2859a-237">`New-AzDataFactoryGatewayKey` cmdlet'i kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="2859a-237">Removed `New-AzDataFactoryGatewayKey` cmdlet</span></span>
- <span data-ttu-id="2859a-238">`Get-AzDataFactoryV2ActivityRun` cmdlet’inden `LinkedServiceName` parametresi kaldırıldı Betikler artık işleme kararları vermek için bu alanın değerini kullanmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="2859a-238">Removed `LinkedServiceName` parameter from `Get-AzDataFactoryV2ActivityRun` cmdlet Scripts should no longer use the value of this field to make processing decisions.</span></span>

### <a name="azdatalakeanalytics-previously-azurermdatalakeanalytics"></a><span data-ttu-id="2859a-239">Az.DataLakeAnalytics (eski adıyla AzureRM.DataLakeAnalytics)</span><span class="sxs-lookup"><span data-stu-id="2859a-239">Az.DataLakeAnalytics (previously AzureRM.DataLakeAnalytics)</span></span>

- <span data-ttu-id="2859a-240">Kullanım dışı cmdlet’ler kaldırıldı: `New-AzDataLakeAnalyticsCatalogSecret`, `Remove-AzDataLakeAnalyticsCatalogSecret` ve `Set-AzDataLakeAnalyticsCatalogSecret`</span><span class="sxs-lookup"><span data-stu-id="2859a-240">Removed deprecated cmdlets: `New-AzDataLakeAnalyticsCatalogSecret`, `Remove-AzDataLakeAnalyticsCatalogSecret`, and `Set-AzDataLakeAnalyticsCatalogSecret`</span></span>

### <a name="azdatalakestore-previously-azurermdatalakestore"></a><span data-ttu-id="2859a-241">Az.DataLakeStore (eski adıyla AzureRM.DataLakeStore)</span><span class="sxs-lookup"><span data-stu-id="2859a-241">Az.DataLakeStore (previously AzureRM.DataLakeStore)</span></span>

- <span data-ttu-id="2859a-242">Aşağıdaki cmdlet’lerin `Encoding` parametresinin `FileSystemCmdletProviderEncoding` olan türü `System.Text.Encoding` olarak değişti.</span><span class="sxs-lookup"><span data-stu-id="2859a-242">The following cmdlets have had the `Encoding` parameter changed from the type `FileSystemCmdletProviderEncoding` to `System.Text.Encoding`.</span></span> <span data-ttu-id="2859a-243">Bu değişiklikle birlikte `String` ve `Oem` kodlama değerleri kaldırılıyor.</span><span class="sxs-lookup"><span data-stu-id="2859a-243">This change removes the encoding values `String` and `Oem`.</span></span> <span data-ttu-id="2859a-244">Önceki diğer tüm kodlama değerleri olduğu gibi kaldı.</span><span class="sxs-lookup"><span data-stu-id="2859a-244">All the other prior encoding values remain.</span></span>
  - <span data-ttu-id="2859a-245">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2859a-245">New-AzureRmDataLakeStoreItem</span></span>
  - <span data-ttu-id="2859a-246">Add-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="2859a-246">Add-AzureRmDataLakeStoreItemContent</span></span>
  - <span data-ttu-id="2859a-247">Get-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="2859a-247">Get-AzureRmDataLakeStoreItemContent</span></span>
- <span data-ttu-id="2859a-248">`New-AzDataLakeStoreAccount` ve `Set-AzDataLakeStoreAccount` cmdlet’inden kullanım dışı `Tags` özellik diğer adı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="2859a-248">Removed deprecated `Tags` property alias from `New-AzDataLakeStoreAccount` and `Set-AzDataLakeStoreAccount` cmdlets</span></span>

  <span data-ttu-id="2859a-249">Şunları kullanan betikler:</span><span class="sxs-lookup"><span data-stu-id="2859a-249">Scripts using</span></span>
  ```azurepowershell-interactive
  New-AzureRMDataLakeStoreAccount -Tags @{TagName="TagValue"}
  ```

  <span data-ttu-id="2859a-250">Şöyle değiştirilmelidir:</span><span class="sxs-lookup"><span data-stu-id="2859a-250">Should be changed to</span></span>
  ```azurepowershell-interactive
  New-AzDataLakeStoreAccount -Tag @{TagName="TagValue"}
  ```

- <span data-ttu-id="2859a-251">`PSDataLakeStoreAccountBasic` nesnesinden kullanım dışı `Identity`, `EncryptionState`, `EncryptionProvisioningState`, `EncryptionConfig`, `FirewallState`, `FirewallRules`, `VirtualNetworkRules`, `TrustedIdProviderState`, `TrustedIdProviders`, `DefaultGroup`, `NewTier`, `CurrentTier`, `FirewallAllowAzureIps` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="2859a-251">Removed deprecated properties `Identity`, `EncryptionState`, `EncryptionProvisioningState`, `EncryptionConfig`, `FirewallState`, `FirewallRules`, `VirtualNetworkRules`, `TrustedIdProviderState`, `TrustedIdProviders`, `DefaultGroup`, `NewTier`, `CurrentTier`, `FirewallAllowAzureIps` from `PSDataLakeStoreAccountBasic` object.</span></span>  <span data-ttu-id="2859a-252">`Get-AzDataLakeStoreAccount` cmdlet’inden döndürülen `PSDatalakeStoreAccount` özelliğini kullanan hiçbir betik bu özelliklere başvurmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="2859a-252">Any script that uses the `PSDatalakeStoreAccount` returned from `Get-AzDataLakeStoreAccount` should not reference these properties.</span></span>

### <a name="azkeyvault-previously-azurermkeyvault"></a><span data-ttu-id="2859a-253">Az.KeyVault (eski adıyla AzureRM.KeyVault)</span><span class="sxs-lookup"><span data-stu-id="2859a-253">Az.KeyVault (previously AzureRM.KeyVault)</span></span>

- <span data-ttu-id="2859a-254">`PSKeyVaultKeyAttributes`, `PSKeyVaultKeyIdentityItem` ve `PSKeyVaultSecretAttributes` nesnesinden `PurgeDisabled` özelliği kaldırıldı Betikler artık işleme kararları vermek için ```PurgeDisabled``` özelliğine başvurmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="2859a-254">The `PurgeDisabled` property was removed from the `PSKeyVaultKeyAttributes`, `PSKeyVaultKeyIdentityItem`, and `PSKeyVaultSecretAttributes` objects Scripts should no longer reference the ```PurgeDisabled``` property to make processing decisions.</span></span>

### <a name="azmedia-previously-azurermmedia"></a><span data-ttu-id="2859a-255">Az.Media (eski adıyla AzureRM.Media)</span><span class="sxs-lookup"><span data-stu-id="2859a-255">Az.Media (previously AzureRM.Media)</span></span>

- <span data-ttu-id="2859a-256">`New-AzMediaService` cmdlet’inden kullanım dışı `Tags` özelliği diğer adı kaldırıldı Şunları kullanan betikler:</span><span class="sxs-lookup"><span data-stu-id="2859a-256">Remove deprecated `Tags` property alias from `New-AzMediaService` cmdlet Scripts using</span></span>
  ```azurepowershell-interactive
  New-AzureRMMediaService -Tags @{TagName="TagValue"}
  ```

  <span data-ttu-id="2859a-257">Şöyle değiştirilmelidir:</span><span class="sxs-lookup"><span data-stu-id="2859a-257">Should be changed to</span></span>
  ```azurepowershell-interactive
  New-AzMediaService -Tag @{TagName="TagValue"}
  ```

### <a name="azmonitor-previously-azurerminsights"></a><span data-ttu-id="2859a-258">Az.Monitor (eski adıyla AzureRM.Insights)</span><span class="sxs-lookup"><span data-stu-id="2859a-258">Az.Monitor (previously AzureRM.Insights)</span></span>

- <span data-ttu-id="2859a-259">`Set-AzDiagnosticSetting` cmdlet’inden alınan tekil parametre adları tercih edilerek çoğul ad `Categories` ve `Timegrains` parametresi kaldırıldı Şunları kullanan betikler:</span><span class="sxs-lookup"><span data-stu-id="2859a-259">Removed plural names `Categories` and `Timegrains` parameter in favor of singular parameter names from `Set-AzDiagnosticSetting` cmdlet Scripts using</span></span>
  ```azurepowershell-interactive
  Set-AzureRmDiagnosticSetting -Timegrains PT1M -Categories Category1, Category2
  ```

  <span data-ttu-id="2859a-260">Şöyle değiştirilmelidir:</span><span class="sxs-lookup"><span data-stu-id="2859a-260">Should be changed to</span></span>
  ```azurepowershell-interactive
  Set-AzDiagnosticSetting -Timegrain PT1M -Category Category1, Category2
  ```

### <a name="aznetwork-previously-azurermnetwork"></a><span data-ttu-id="2859a-261">Az.Network (eski adıyla AzureRM.Network)</span><span class="sxs-lookup"><span data-stu-id="2859a-261">Az.Network (previously AzureRM.Network)</span></span>

- <span data-ttu-id="2859a-262">`Get-AzServiceEndpointPolicyDefinition` cmdlet’inden kullanım dışı `ResourceId` parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="2859a-262">Removed deprecated `ResourceId` parameter from `Get-AzServiceEndpointPolicyDefinition` cmdlet</span></span>
- <span data-ttu-id="2859a-263">`PSVirtualNetwork` nesnesinden kullanım dışı `EnableVmProtection` özelliği kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="2859a-263">Removed deprecated `EnableVmProtection` property from `PSVirtualNetwork` object</span></span>
- <span data-ttu-id="2859a-264">Kullanım dışı `Set-AzVirtualNetworkGatewayVpnClientConfig` cmdlet’i kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="2859a-264">Removed deprecated `Set-AzVirtualNetworkGatewayVpnClientConfig` cmdlet</span></span>

<span data-ttu-id="2859a-265">Betikler artık bu alanların değerlerini temel alan işleme kararları almamalıdır.</span><span class="sxs-lookup"><span data-stu-id="2859a-265">Scripts should no longer make processing decisions based on the values fo these fields.</span></span>

### <a name="azoperationalinsights-previously-azurermoperationalinsights"></a><span data-ttu-id="2859a-266">Az.OperationalInsights (eski adıyla AzureRM.OperationalInsights)</span><span class="sxs-lookup"><span data-stu-id="2859a-266">Az.OperationalInsights (previously AzureRM.OperationalInsights)</span></span>

- <span data-ttu-id="2859a-267">`Get-AzOperationalInsightsDataSource` için varsayılan parametre kümesi kaldırıldı, varsayılan parametre kümesi `ByWorkspaceNameByKind` oldu</span><span class="sxs-lookup"><span data-stu-id="2859a-267">Default parameter set for `Get-AzOperationalInsightsDataSource` is removed, and `ByWorkspaceNameByKind` has become the default parameter set</span></span>

  <span data-ttu-id="2859a-268">Veri kaynaklarını şunu kullanarak listeleyen betikler:</span><span class="sxs-lookup"><span data-stu-id="2859a-268">Scripts that listed data sources using</span></span>
  ```azurepowershell-interactive
  Get-AzureRmOperationalInsightsDataSource
  ```

  <span data-ttu-id="2859a-269">Bir Tür belirtecek şekilde değiştirilmelidir</span><span class="sxs-lookup"><span data-stu-id="2859a-269">Should be changed to specify a Kind</span></span>
  ```azurepowershell-interactive
  Get-AzOperationalInsightsDataSource -Kind AzureActivityLog
  ```

### <a name="azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery"></a><span data-ttu-id="2859a-270">Az.RecoveryServices (eski adıyla AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup ve AzureRM.RecoveryServices.SiteRecovery)</span><span class="sxs-lookup"><span data-stu-id="2859a-270">Az.RecoveryServices (previously AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup, and AzureRM.RecoveryServices.SiteRecovery)</span></span>

- <span data-ttu-id="2859a-271">`New/Set-AzRecoveryServicesAsrPolicy` cmdlet’inden `Encryption` parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="2859a-271">Removed `Encryption` parameter from `New/Set-AzRecoveryServicesAsrPolicy` cmdlet</span></span>
- <span data-ttu-id="2859a-272">Artık `Restore-AzRecoveryServicesBackupItem` cmdlet'indeki yönetilen disk geri yükleme işlemleri için `TargetStorageAccountName` parametresi zorunludur</span><span class="sxs-lookup"><span data-stu-id="2859a-272">`TargetStorageAccountName` parameter is now mandatory for managed disk restores in `Restore-AzRecoveryServicesBackupItem` cmdlet</span></span>
- <span data-ttu-id="2859a-273">`Restore-AzRecoveryServicesBackupItem` cmdlet’inden `StorageAccountName` ve `StorageAccountResourceGroupName` parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="2859a-273">Removed `StorageAccountName` and `StorageAccountResourceGroupName` parameters in `Restore-AzRecoveryServicesBackupItem` cmdlet</span></span>
- <span data-ttu-id="2859a-274">`Get-AzRecoveryServicesBackupContainer` cmdlet’inden `Name` parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="2859a-274">Removed `Name`parameter in `Get-AzRecoveryServicesBackupContainer` cmdlet</span></span>

### <a name="azresources-previously-azurermresources"></a><span data-ttu-id="2859a-275">Az.Resources (eski adıyla AzureRM.Resources)</span><span class="sxs-lookup"><span data-stu-id="2859a-275">Az.Resources (previously AzureRM.Resources)</span></span>

- <span data-ttu-id="2859a-276">`New/Set-AzPolicyAssignment` cmdlet’inden `Sku` parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="2859a-276">Removed `Sku` parameter from `New/Set-AzPolicyAssignment` cmdlet</span></span>
- <span data-ttu-id="2859a-277">`New-AzADServicePrincipal` ve `New-AzADSpCredential` cmdlet’inden `Password` parametresi kaldırıldı Parolalar otomatik olarak oluşturulduğundan, daha önce parolayı sağlayan betikler:</span><span class="sxs-lookup"><span data-stu-id="2859a-277">Removed `Password` parameter from `New-AzADServicePrincipal` and `New-AzADSpCredential` cmdlet Passwords are automatically generated, scripts that provided the password:</span></span>

  ```azurepowershell-interactive
  New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 -Password $secPassword
  ```

  <span data-ttu-id="2859a-278">Parolayı çıktıdan alacak şekilde değiştirilmelidir:</span><span class="sxs-lookup"><span data-stu-id="2859a-278">Should be changed to retrieve the password from the output:</span></span>

  ```azurepowershell-interactive
  $credential = New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
  $secPassword = $credential.Secret
  ```

### <a name="azservicefabric-previously-azurermservicefabric"></a><span data-ttu-id="2859a-279">Az.ServiceFabric (eski adıyla AzureRM.ServiceFabric)</span><span class="sxs-lookup"><span data-stu-id="2859a-279">Az.ServiceFabric (previously AzureRM.ServiceFabric)</span></span>

- <span data-ttu-id="2859a-280">Aşağıdaki cmdlet dönüş türleri değişmiştir:</span><span class="sxs-lookup"><span data-stu-id="2859a-280">The following cmdlet return types have been changed:</span></span>
  - <span data-ttu-id="2859a-281">`ApplicationHealthPolicy` türündeki `ServiceTypeHealthPolicies` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="2859a-281">The property `ServiceTypeHealthPolicies` of type `ApplicationHealthPolicy` has been removed.</span></span>
  - <span data-ttu-id="2859a-282">`ClusterUpgradeDeltaHealthPolicy` türündeki `ApplicationHealthPolicies` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="2859a-282">The property `ApplicationHealthPolicies` of type `ClusterUpgradeDeltaHealthPolicy` has been removed.</span></span>
  - <span data-ttu-id="2859a-283">`ClusterUpgradePolicy` türündeki `OverrideUserUpgradePolicy` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="2859a-283">The property `OverrideUserUpgradePolicy` of type `ClusterUpgradePolicy` has been removed.</span></span>
  - <span data-ttu-id="2859a-284">Bu değişikliklerden aşağıdaki cmdlet’ler etkilenir:</span><span class="sxs-lookup"><span data-stu-id="2859a-284">These changes affect the following cmdlets:</span></span>
    - <span data-ttu-id="2859a-285">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="2859a-285">Add-AzServiceFabricClientCertificate</span></span>
    - <span data-ttu-id="2859a-286">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="2859a-286">Add-AzServiceFabricClusterCertificate</span></span>
    - <span data-ttu-id="2859a-287">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="2859a-287">Add-AzServiceFabricNode</span></span>
    - <span data-ttu-id="2859a-288">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="2859a-288">Add-AzServiceFabricNodeType</span></span>
    - <span data-ttu-id="2859a-289">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="2859a-289">Get-AzServiceFabricCluster</span></span>
    - <span data-ttu-id="2859a-290">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="2859a-290">Remove-AzServiceFabricClientCertificate</span></span>
    - <span data-ttu-id="2859a-291">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="2859a-291">Remove-AzServiceFabricClusterCertificate</span></span>
    - <span data-ttu-id="2859a-292">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="2859a-292">Remove-AzServiceFabricNode</span></span>
    - <span data-ttu-id="2859a-293">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="2859a-293">Remove-AzServiceFabricNodeType</span></span>
    - <span data-ttu-id="2859a-294">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="2859a-294">Remove-AzServiceFabricSetting</span></span>
    - <span data-ttu-id="2859a-295">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="2859a-295">Set-AzServiceFabricSetting</span></span>
    - <span data-ttu-id="2859a-296">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="2859a-296">Set-AzServiceFabricUpgradeType</span></span>
    - <span data-ttu-id="2859a-297">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="2859a-297">Update-AzServiceFabricDurability</span></span>
    - <span data-ttu-id="2859a-298">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="2859a-298">Update-AzServiceFabricReliability</span></span>

### <a name="azsql-previously-azurermsql"></a><span data-ttu-id="2859a-299">Az.Sql (eski adıyla AzureRM.Sql)</span><span class="sxs-lookup"><span data-stu-id="2859a-299">Az.Sql (previously AzureRM.Sql)</span></span>

- <span data-ttu-id="2859a-300">`Set-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet’inden `State` ve `ResourceId` parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="2859a-300">Removed `State` and `ResourceId` parameters from `Set-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet</span></span>
- <span data-ttu-id="2859a-301">Kullanım dışı cmdlet’ler kaldırıldı: `Get/Set-AzSqlServerBackupLongTermRetentionVault`, `Get/Start/Stop-AzSqlServerUpgrade`, `Get/Set-AzSqlDatabaseAuditingPolicy`, `Get/Set-AzSqlServerAuditingPolicy`, `Remove-AzSqlDatabaseAuditing`, `Remove-AzSqlServerAuditing`</span><span class="sxs-lookup"><span data-stu-id="2859a-301">Removed deprecated cmdlets: `Get/Set-AzSqlServerBackupLongTermRetentionVault`, `Get/Start/Stop-AzSqlServerUpgrade`, `Get/Set-AzSqlDatabaseAuditingPolicy`, `Get/Set-AzSqlServerAuditingPolicy`, `Remove-AzSqlDatabaseAuditing`, `Remove-AzSqlServerAuditing`</span></span>
- <span data-ttu-id="2859a-302">`Get-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet’inden kullanım dışı `Current` parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="2859a-302">Removed deprecated parameter `Current` from `Get-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet</span></span>
- <span data-ttu-id="2859a-303">`Get-AzSqlServerServiceObjective` cmdlet’inden kullanım dışı `DatabaseName` parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="2859a-303">Removed deprecated parameter `DatabaseName` from `Get-AzSqlServerServiceObjective` cmdlet</span></span>
- <span data-ttu-id="2859a-304">`Set-AzSqlDatabaseDataMaskingPolicy` cmdlet’inden kullanım dışı `PrivilegedLogin` parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="2859a-304">Removed deprecated parameter `PrivilegedLogin` from `Set-AzSqlDatabaseDataMaskingPolicy` cmdlet</span></span>

### <a name="azstorage-previously-azurestorage-and-azurermstorage"></a><span data-ttu-id="2859a-305">Az.Storage (eski adıyla Azure.Storage and AzureRM.Storage)</span><span class="sxs-lookup"><span data-stu-id="2859a-305">Az.Storage (previously Azure.Storage and AzureRM.Storage)</span></span>

- <span data-ttu-id="2859a-306">Yalnızca depolama hesabı adıyla bir Oauth depolama bağlamı oluşturulmasının desteklenmesi için varsayılan parametre kümesi `OAuthParameterSet` olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="2859a-306">To support creating an Oauth storage context with only the storage account name, the default parameter set has been changed to `OAuthParameterSet`</span></span>
  - <span data-ttu-id="2859a-307">Örnek: `$ctx = New-AzureStorageContext -StorageAccountName $accountName`</span><span class="sxs-lookup"><span data-stu-id="2859a-307">Example: `$ctx = New-AzureStorageContext -StorageAccountName $accountName`</span></span>
- <span data-ttu-id="2859a-308">`Get-AzStorageUsage` cmdlet’inde `Location` parametresi zorunlu hale geldi</span><span class="sxs-lookup"><span data-stu-id="2859a-308">The `Location` parameter has become mandatory in the `Get-AzStorageUsage` cmdlet</span></span>
- <span data-ttu-id="2859a-309">Depolama API’si metotları artık zaman uyumlu API çağrıları yerine Görev Tabanlı Zaman Uyumsuz Düzeni (TAP) kullanıyor.</span><span class="sxs-lookup"><span data-stu-id="2859a-309">The Storage API methods now use the Task-based Asynchronous Pattern (TAP), instead of synchronous API calls.</span></span> <span data-ttu-id="2859a-310">Aşağıdaki örneklerde yeni zaman uyumsuz komutlar gösterilir:</span><span class="sxs-lookup"><span data-stu-id="2859a-310">The following examples demonstrate the new asynchronous commands:</span></span>

#### <a name="blob-snapshot"></a><span data-ttu-id="2859a-311">Blob Anlık Görüntüsü</span><span class="sxs-lookup"><span data-stu-id="2859a-311">Blob Snapshot</span></span>

<span data-ttu-id="2859a-312">AzureRM:</span><span class="sxs-lookup"><span data-stu-id="2859a-312">AzureRM:</span></span>

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$b.ICloudBlob.Snapshot()
```

<span data-ttu-id="2859a-313">Az:</span><span class="sxs-lookup"><span data-stu-id="2859a-313">Az:</span></span>

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$task = $b.ICloudBlob.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="share-snapshot"></a><span data-ttu-id="2859a-314">Anlık Görüntüyü Paylaş</span><span class="sxs-lookup"><span data-stu-id="2859a-314">Share Snapshot</span></span>

<span data-ttu-id="2859a-315">AzureRM:</span><span class="sxs-lookup"><span data-stu-id="2859a-315">AzureRM:</span></span>

```azurepowershell-interactive
$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$snapshot = $Share.Snapshot()
```

<span data-ttu-id="2859a-316">Az:</span><span class="sxs-lookup"><span data-stu-id="2859a-316">Az:</span></span>

```azurepowershell-interactive
$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$task = $Share.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="undelete-soft-deleted-blob"></a><span data-ttu-id="2859a-317">Geçici silinen blob’un silinmesini geri al</span><span class="sxs-lookup"><span data-stu-id="2859a-317">Undelete soft-deleted blob</span></span>

<span data-ttu-id="2859a-318">AzureRM:</span><span class="sxs-lookup"><span data-stu-id="2859a-318">AzureRM:</span></span>

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$b.ICloudBlob.Undelete()
```

<span data-ttu-id="2859a-319">Az:</span><span class="sxs-lookup"><span data-stu-id="2859a-319">Az:</span></span>

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$task = $b.ICloudBlob.UndeleteAsync()
$task.Wait()
```

#### <a name="set-blob-tier"></a><span data-ttu-id="2859a-320">Blob Katmanını Ayarla</span><span class="sxs-lookup"><span data-stu-id="2859a-320">Set Blob Tier</span></span>

<span data-ttu-id="2859a-321">AzureRM:</span><span class="sxs-lookup"><span data-stu-id="2859a-321">AzureRM:</span></span>

```azurepowershell-interactive
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$blockBlob.ICloudBlob.SetStandardBlobTier("hot")

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$pageBlob.ICloudBlob.SetPremiumBlobTier("P4")
```

<span data-ttu-id="2859a-322">Az:</span><span class="sxs-lookup"><span data-stu-id="2859a-322">Az:</span></span>

```azurepowershell-interactive
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$task = $blockBlob.ICloudBlob.SetStandardBlobTierAsync("hot")
$task.Wait()

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$task = $pageBlob.ICloudBlob.SetPremiumBlobTierAsync("P4")
$task.Wait()
```

### <a name="azwebsites-previously-azurermwebsites"></a><span data-ttu-id="2859a-323">Az.Websites (eski adıyla AzureRM.Websites)</span><span class="sxs-lookup"><span data-stu-id="2859a-323">Az.Websites (previously AzureRM.Websites)</span></span>

- <span data-ttu-id="2859a-324">`PSAppServicePlan`, `PSCertificate`, `PSCloningInfo` ve `PSSite` nesnesinden kullanım dışı özellikler kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="2859a-324">Removed deprecated properties from the `PSAppServicePlan`, `PSCertificate`, `PSCloningInfo`, and `PSSite` objects</span></span>
