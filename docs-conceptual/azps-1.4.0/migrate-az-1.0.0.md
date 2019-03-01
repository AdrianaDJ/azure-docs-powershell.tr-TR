---
title: Microsoft Azure PowerShell Az 1.0.0 için yeni değişiklikler
description: Bu geçiş kılavuzu, Azure PowerShell Az sürüm 1 yayınında yapılan yeni değişikliklerin listesini içerir.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/14/2018
ms.openlocfilehash: be3e19dc4b689adbc63b933dd9f3454122d5344a
ms.sourcegitcommit: 5630030c5cfa9828c3c024b69de59248263ef17f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/26/2019
ms.locfileid: "56837376"
---
# <a name="migration-guide-for-az-100"></a><span data-ttu-id="81e7f-103">Az 1.0.0 için Geçiş Kılavuzu</span><span class="sxs-lookup"><span data-stu-id="81e7f-103">Migration Guide for Az 1.0.0</span></span>

<span data-ttu-id="81e7f-104">Bu belgede AzureRM’nin 6.x sürümleri ile Az 1.0.0 sürümü arasındaki değişiklikler açıklanır.</span><span class="sxs-lookup"><span data-stu-id="81e7f-104">This document describes the changes between the 6.x versions of AzureRM and Az version 1.0.0.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="81e7f-105">İçindekiler</span><span class="sxs-lookup"><span data-stu-id="81e7f-105">Table of Contents</span></span>
- [<span data-ttu-id="81e7f-106">Hataya neden olan genel değişiklikler</span><span class="sxs-lookup"><span data-stu-id="81e7f-106">General breaking changes</span></span>](#general-breaking-changes)
  - [<span data-ttu-id="81e7f-107">Cmdlet İsim Öneki Değişiklikleri</span><span class="sxs-lookup"><span data-stu-id="81e7f-107">Cmdlet Noun Prefix Changes</span></span>](#cmdlet-noun-prefix-changes)
  - [<span data-ttu-id="81e7f-108">Modül adı değişiklikleri</span><span class="sxs-lookup"><span data-stu-id="81e7f-108">Module name changes</span></span>](#module-name-changes)
  - [<span data-ttu-id="81e7f-109">Kaldırılan modüller</span><span class="sxs-lookup"><span data-stu-id="81e7f-109">Removed modules</span></span>](#removed-modules)
  - [<span data-ttu-id="81e7f-110">Windows PowerShell 5.1 ve .NET 4.7.2</span><span class="sxs-lookup"><span data-stu-id="81e7f-110">Windows PowerShell 5.1 and .NET 4.7.2</span></span>](#windows-powershell-51-and-net-472)
  - [<span data-ttu-id="81e7f-111">PSCredential ile Kullanıcı oturumu açmanın geçici olarak kaldırılması</span><span class="sxs-lookup"><span data-stu-id="81e7f-111">Temporary removal of User login using PSCredential</span></span>](#temporary-removal-of-user-login-using-pscredential)
  - [<span data-ttu-id="81e7f-112">Web Tarayıcısı istemi yerine varsayılan Cihaz Kodu ile oturum açma</span><span class="sxs-lookup"><span data-stu-id="81e7f-112">Default Device Code login instead of Web Browser prompt</span></span>](#temporary-default-device-code-login-instead-of-web-browser-prompt)
- [<span data-ttu-id="81e7f-113">Modüldeki yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="81e7f-113">Module breaking changes</span></span>](#module-breaking-changes)
  - [<span data-ttu-id="81e7f-114">Az.ApiManagement (eski adıyla AzureRM.ApiManagement)</span><span class="sxs-lookup"><span data-stu-id="81e7f-114">Az.ApiManagement (previously AzureRM.ApiManagement)</span></span>](#azapimanagement-previously-azurermapimanagement)
  - [<span data-ttu-id="81e7f-115">Az.Billing (eski adıyla AzureRM.Billing, AzureRM.Consumption ve AzureRM.UsageAggregates)</span><span class="sxs-lookup"><span data-stu-id="81e7f-115">Az.Billing (previously AzureRM.Billing, AzureRM.Consumption, and AzureRM.UsageAggregates)</span></span>](#azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates)
  - [<span data-ttu-id="81e7f-116">Az.CognitiveServices (eski adıyla AzureRM.CognitiveServices)</span><span class="sxs-lookup"><span data-stu-id="81e7f-116">Az.CognitiveServices (previously AzureRM.CognitiveServices)</span></span>](#azcognitiveservices-previously-azurermcognitiveservices)
  - [<span data-ttu-id="81e7f-117">Az.Compute (eski adıyla AzureRM.Compute)</span><span class="sxs-lookup"><span data-stu-id="81e7f-117">Az.Compute (previously AzureRM.Compute)</span></span>](#azcompute-previously-azurermcompute)
  - [<span data-ttu-id="81e7f-118">Az.DataFactory (eski adıyla AzureRM.DataFactories ve AzureRM.DataFactoryV2)</span><span class="sxs-lookup"><span data-stu-id="81e7f-118">Az.DataFactory (previously AzureRM.DataFactories and AzureRM.DataFactoryV2)</span></span>](#azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2)
  - [<span data-ttu-id="81e7f-119">Az.DataLakeAnalytics (eski adıyla AzureRM.DataLakeAnalytics)</span><span class="sxs-lookup"><span data-stu-id="81e7f-119">Az.DataLakeAnalytics (previously AzureRM.DataLakeAnalytics)</span></span>](#azdatalakeanalytics-previously-azurermdatalakeanalytics)
  - [<span data-ttu-id="81e7f-120">Az.DataLakeStore (eski adıyla AzureRM.DataLakeStore)</span><span class="sxs-lookup"><span data-stu-id="81e7f-120">Az.DataLakeStore (previously AzureRM.DataLakeStore)</span></span>](#azdatalakestore-previously-azurermdatalakestore)
  - [<span data-ttu-id="81e7f-121">Az.KeyVault (eski adıyla AzureRM.KeyVault)</span><span class="sxs-lookup"><span data-stu-id="81e7f-121">Az.KeyVault (previously AzureRM.KeyVault)</span></span>](#azkeyvault-previously-azurermkeyvault)
  - [<span data-ttu-id="81e7f-122">Az.Media (eski adıyla AzureRM.Media)</span><span class="sxs-lookup"><span data-stu-id="81e7f-122">Az.Media (previously AzureRM.Media)</span></span>](#azmedia-previously-azurermmedia)
  - [<span data-ttu-id="81e7f-123">Az.Monitor (eski adıyla AzureRM.Insights)</span><span class="sxs-lookup"><span data-stu-id="81e7f-123">Az.Monitor (previously AzureRM.Insights)</span></span>](#azmonitor-previously-azurerminsights)
  - [<span data-ttu-id="81e7f-124">Az.Network (eski adıyla AzureRM.Network)</span><span class="sxs-lookup"><span data-stu-id="81e7f-124">Az.Network (previously AzureRM.Network)</span></span>](#aznetwork-previously-azurermnetwork)
  - [<span data-ttu-id="81e7f-125">Az.OperationalInsights (eski adıyla AzureRM.OperationalInsights)</span><span class="sxs-lookup"><span data-stu-id="81e7f-125">Az.OperationalInsights (previously AzureRM.OperationalInsights)</span></span>](#azoperationalinsights-previously-azurermoperationalinsights)
  - [<span data-ttu-id="81e7f-126">Az.RecoveryServices (eski adıyla AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup ve AzureRM.RecoveryServices.SiteRecovery)</span><span class="sxs-lookup"><span data-stu-id="81e7f-126">Az.RecoveryServices (previously AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup, and AzureRM.RecoveryServices.SiteRecovery)</span></span>](#azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery)
  - [<span data-ttu-id="81e7f-127">Az.Resources (eski adıyla AzureRM.Resources)</span><span class="sxs-lookup"><span data-stu-id="81e7f-127">Az.Resources (previously AzureRM.Resources)</span></span>](#azresources-previously-azurermresources)
  - [<span data-ttu-id="81e7f-128">Az.ServiceFabric (eski adıyla AzureRM.ServiceFabric)</span><span class="sxs-lookup"><span data-stu-id="81e7f-128">Az.ServiceFabric (previously AzureRM.ServiceFabric)</span></span>](#azservicefabric-previously-azurermservicefabric)
  - [<span data-ttu-id="81e7f-129">Az.Sql (eski adıyla AzureRM.Sql)</span><span class="sxs-lookup"><span data-stu-id="81e7f-129">Az.Sql (previously AzureRM.Sql)</span></span>](#azsql-previously-azurermsql)
  - [<span data-ttu-id="81e7f-130">Az.Storage (eski adıyla Azure.Storage and AzureRM.Storage)</span><span class="sxs-lookup"><span data-stu-id="81e7f-130">Az.Storage (previously Azure.Storage and AzureRM.Storage)</span></span>](#azstorage-previously-azurestorage-and-azurermstorage)
  - [<span data-ttu-id="81e7f-131">Az.Websites (eski adıyla AzureRM.Websites)</span><span class="sxs-lookup"><span data-stu-id="81e7f-131">Az.Websites (previously AzureRM.Websites)</span></span>](#azwebsites-previously-azurermwebsites)

## <a name="general-breaking-changes"></a><span data-ttu-id="81e7f-132">Hataya neden olan genel değişiklikler</span><span class="sxs-lookup"><span data-stu-id="81e7f-132">General breaking changes</span></span>
### <a name="cmdlet-noun-prefix-changes"></a><span data-ttu-id="81e7f-133">Cmdlet İsim Öneki Değişiklikleri</span><span class="sxs-lookup"><span data-stu-id="81e7f-133">Cmdlet Noun Prefix Changes</span></span>
<span data-ttu-id="81e7f-134">AzureRM’de cmdlet’ler ya 'AzureRM' ya da 'Azure' isim önekini kullanıyordu.</span><span class="sxs-lookup"><span data-stu-id="81e7f-134">In AzureRM, cmdlets used either 'AzureRM' or 'Azure' as a noun prefix.</span></span>  <span data-ttu-id="81e7f-135">Az ile birlikte cmdlet adları basitleştirilip normalleştirilerek tüm cmdlet’lerin isim öneki olarak 'Az' kullanılacak.</span><span class="sxs-lookup"><span data-stu-id="81e7f-135">Az simplifies and normalizes cmndlet names, so that all cmdlets use 'Az' as their cmdlet noun prefix.</span></span> <span data-ttu-id="81e7f-136">Örnek:</span><span class="sxs-lookup"><span data-stu-id="81e7f-136">For example:</span></span>
```powershell
Get-AzureRMVM
Get-AzureKeyVaultSecret
```

<span data-ttu-id="81e7f-137">Şuna dönüştü:</span><span class="sxs-lookup"><span data-stu-id="81e7f-137">Have changed to</span></span>
```powershell
Get-AzVM
Get-AzKeyVaultSecret
```

<span data-ttu-id="81e7f-138">Bu yeni cmdlet adlarına geçişi kolaylaştırmak için Az ile birlikte iki yeni cmdlet sunuluyor: ```Enable-AzureRmAlias``` ve ```Disable-AzureRmAlias```.</span><span class="sxs-lookup"><span data-stu-id="81e7f-138">To make the transition to these new cmdlet names simpler, Az introduces two new cmdlets, ```Enable-AzureRmAlias``` and ```Disable-AzureRmAlias```.</span></span>  <span data-ttu-id="81e7f-139">```Enable-AzureRmAlias```, AzureRM’deki eski cmdlet adlarından yeni Az cmdlet adlarına diğer adlar oluşturur.</span><span class="sxs-lookup"><span data-stu-id="81e7f-139">```Enable-AzureRmAlias``` creates aliases from the older cmdlet names in AzureRM to the newer Az cmdlet names.</span></span>  <span data-ttu-id="81e7f-140">Bu cmdlet, geçerli oturumda ya da tüm oturumlarda kullanıcı veya makine profilinizi değiştirerek diğer ad oluşturmanıza imkan tanır.</span><span class="sxs-lookup"><span data-stu-id="81e7f-140">The cmdlet allows creating aliases in the current session, or across all sessions by changing your user or machine profile.</span></span> 

<span data-ttu-id="81e7f-141">Örneğin, şu AzureRM betiği:</span><span class="sxs-lookup"><span data-stu-id="81e7f-141">For example, the following script in AzureRM:</span></span>
```powershell
#Requires -Modules AzureRM.Storage
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="81e7f-142">```Enable-AzureRmAlias``` kullanılarak küçük değişikliklerle çalıştırılabilir:</span><span class="sxs-lookup"><span data-stu-id="81e7f-142">Could be run with minimal changes using ```Enable-AzureRmAlias```:</span></span>
```powershell
#Requires -Modules Az.Storage
Enable-AzureRmAlias
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="81e7f-143">```Enable-AzureRmAlias -Scope CurrentUser``` çalıştırıldığında açtığınız tüm powershell oturumları için diğer adları etkinleştireceğinden, bu cmdlet’i çalıştırdıktan sonra şunun gibi bir betiğin hiç değiştirilmesi gerekmez:</span><span class="sxs-lookup"><span data-stu-id="81e7f-143">Running ```Enable-AzureRmAlias -Scope CurrentUser``` will enable the aliases for all powershell sessions you open, so that after executing this cmdlet, a script like this would not need to be changed at all:</span></span>
```powershell
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="81e7f-144">Diğer ad cmdlet’lerinin kullanımıyla ilgili tüm ayrıntıları öğrenmek için powershell isteminden şunu yürütün: ```Get-Help -Online Enable-AzureRmAlias```.</span><span class="sxs-lookup"><span data-stu-id="81e7f-144">For complete details on the usage of the alias cmdlets, execute ```Get-Help -Online Enable-AzureRmAlias``` from the powershell prompt.</span></span>

<span data-ttu-id="81e7f-145">```Disable-AzureRmAlias```, ```Enable-AzureRmAlias``` tarafından oluşturulan AzureRM cmdlet diğer adlarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="81e7f-145">```Disable-AzureRmAlias``` removes AzureRM cmdlet aliases created by ```Enable-AzureRmAlias```.</span></span>  <span data-ttu-id="81e7f-146">Tüm ayrıntıları öğrenmek için powershell isteminden şunu yürütün: ```Get-Help -Online Disable-AzureRmAlias```.</span><span class="sxs-lookup"><span data-stu-id="81e7f-146">For complete details, execute ```Get-Help -Online Disable-AzureRmAlias``` from the powershell prompt.</span></span>

### <a name="module-name-changes"></a><span data-ttu-id="81e7f-147">Modül Adı Değişiklikleri</span><span class="sxs-lookup"><span data-stu-id="81e7f-147">Module Name Changes</span></span>
- <span data-ttu-id="81e7f-148">Aşağıdaki modüller dışında, önceden `AzureRM.*` olan modül adları `Az.*` olarak değiştirildi:</span><span class="sxs-lookup"><span data-stu-id="81e7f-148">The module names have changed from `AzureRM.*` to `Az.*`, except for the following modules:</span></span>
```
AzureRM.Profile                       -> Az.Accounts
Azure.AnalysisServices                -> Az.AnalysisServices
AzureRM.Consumption                   -> Az.Billing
AzureRM.UsageAggregates               -> Az.Billing
AzureRM.DataFactories                 -> Az.DataFactory
AzureRM.DataFactoryV2                 -> Az.DataFactory
AzureRM.MachineLearningCompute        -> Az.MachineLearning
AzureRM.Insights                      -> Az.Monitor
AzureRM.RecoveryServices.Backup       -> Az.RecoveryServices
AzureRM.RecoveryServices.SiteRecovery -> Az.RecoveryServices
AzureRM.Tags                          -> Az.Resources
Azure.Storage                         -> Az.Storage
```

<span data-ttu-id="81e7f-149">Modül adlarındaki değişiklikler nedeniyle, belirli modülleri yüklemek için ```#Requires``` ve ```Import-Module``` deyimlerini kullanan tüm betiklerin yeni modülü kullanacak şekilde güncelleştirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="81e7f-149">The changes in module names mean that any script that uses ```#Requires``` or ```Import-Module``` to load specific modules will need to be changed to use the new module instead.</span></span>

#### <a name="migrating-requires-statements"></a><span data-ttu-id="81e7f-150">#Requires Deyimlerini Geçirme</span><span class="sxs-lookup"><span data-stu-id="81e7f-150">Migrating #Requires Statements</span></span>
<span data-ttu-id="81e7f-151">AzureRM modüllerine bağımlılığı bildirmek için #Requires deyimini kullanan betikler yeni modül adlarını kullanacak şekilde güncelleştirilmelidir</span><span class="sxs-lookup"><span data-stu-id="81e7f-151">Scripts that use #Requires to declare a dependency on AzureRM modules should be updated to use the new module names</span></span>
```powershell
#Requires -Module AzureRM.Compute
```

<span data-ttu-id="81e7f-152">Şöyle değiştirilmelidir:</span><span class="sxs-lookup"><span data-stu-id="81e7f-152">Should be changed to</span></span>
```powershell
#Requires -Module Az.Compute
```

#### <a name="migrating-import-module-statements"></a><span data-ttu-id="81e7f-153">Import-Module Deyimlerini Geçirme</span><span class="sxs-lookup"><span data-stu-id="81e7f-153">Migrating Import-Module Statements</span></span>
<span data-ttu-id="81e7f-154">AzureRM modüllerini yüklemek için ```Import-Module``` deyimini kullanan betikler yeni modül adlarını yansıtacak şekilde güncelleştirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="81e7f-154">Scripts that use ```Import-Module``` to load AzureRM modules will need to be updated to reflect the new module names.</span></span>
```powershell
Import-Module -Name AzureRM.Compute
```

<span data-ttu-id="81e7f-155">Şöyle değiştirilmelidir:</span><span class="sxs-lookup"><span data-stu-id="81e7f-155">Should be changed to</span></span>
```powershell
Import-Module -Name Az.Compute
```

### <a name="migrating-fully-qualified-cmdlet-invocations"></a><span data-ttu-id="81e7f-156">Tam Olarak Nitelenen Cmdlet Çağrılarını Geçirme</span><span class="sxs-lookup"><span data-stu-id="81e7f-156">Migrating Fully-Qualified Cmdlet Invocations</span></span>
<span data-ttu-id="81e7f-157">Şunun gibi modül adıyla nitelenen cmdlet çağrılarını kullanan betikler:</span><span class="sxs-lookup"><span data-stu-id="81e7f-157">Scripts that use module-qualified cmdlet invocations, like</span></span>
```powershell
AzureRM.Compute\Get-AzureRmVM
```

<span data-ttu-id="81e7f-158">Yeni modülü ve cmdlet adlarını kullanacak şekilde değiştirilmelidir</span><span class="sxs-lookup"><span data-stu-id="81e7f-158">Should be changed to use the new module and cmdlet names</span></span>
```powershell
Az.Compute\Get-AzVM
```

### <a name="migrating-module-manifest-dependencies"></a><span data-ttu-id="81e7f-159">Modül Bildirimi Bağımlılıklarını Geçirme</span><span class="sxs-lookup"><span data-stu-id="81e7f-159">Migrating Module Manifest Dependencies</span></span>
<span data-ttu-id="81e7f-160">Bir modül bildirimi (.psd1) dosyası aracılığıyla AzureRM modüllerine bağımlılığı ifade eden modüllerin 'RequiredModules' bölümünde güncelleştirilmiş modül adları olmalıdır</span><span class="sxs-lookup"><span data-stu-id="81e7f-160">Modules that express dependencies on AzureRM modules through a module manifest (.psd1) file will need to updated the module names in their 'RequiredModules' section</span></span>

```powershell
RequiredModules = @(@{ModuleName="AzureRM.Profile"; ModuleVersion="5.8.2"})
```

<span data-ttu-id="81e7f-161">Şöyle değiştirilmelidir:</span><span class="sxs-lookup"><span data-stu-id="81e7f-161">Should be changed to</span></span>

```powershell
RequiredModules = @(@{ModuleName="Az.Profile"; ModuleVersion="1.0.0"})
```

### <a name="removed-modules"></a><span data-ttu-id="81e7f-162">Kaldırılan modüller</span><span class="sxs-lookup"><span data-stu-id="81e7f-162">Removed modules</span></span>
- `AzureRM.Backup`
- `AzureRM.Compute.ManagedService`
- `AzureRM.Scheduler`

<span data-ttu-id="81e7f-163">Bu hizmetlere yönelik araçlar artık etkin bir şekilde desteklenmemektedir.</span><span class="sxs-lookup"><span data-stu-id="81e7f-163">The tooling for these services are no longer actively supported.</span></span>  <span data-ttu-id="81e7f-164">Müşterilerin uygun olan en yakın zamanda alternatif hizmetlere geçmesi önerilir.</span><span class="sxs-lookup"><span data-stu-id="81e7f-164">Customers are encouraged to move to alternative services as soon as it is convenient.</span></span>

### <a name="windows-powershell-51-and-net-472"></a><span data-ttu-id="81e7f-165">Windows PowerShell 5.1 ve .NET 4.7.2</span><span class="sxs-lookup"><span data-stu-id="81e7f-165">Windows PowerShell 5.1 and .NET 4.7.2</span></span>
- <span data-ttu-id="81e7f-166">Windows PowerShell 5.1 ile Az kullanımı, .NET 4.7.2 sürümünün yüklenmesini gerektirir.</span><span class="sxs-lookup"><span data-stu-id="81e7f-166">Using Az with Windows PowerShell 5.1 requires the installation of .NET 4.7.2.</span></span> <span data-ttu-id="81e7f-167">Bununla birlikte, PowerShell Core ile Az kullanımı için .NET 4.7.2 gerekmez.</span><span class="sxs-lookup"><span data-stu-id="81e7f-167">However, using Az with PowerShell Core does not require .NET 4.7.2.</span></span> 

### <a name="temporary-removal-of-user-login-using-pscredential"></a><span data-ttu-id="81e7f-168">PSCredential ile Kullanıcı oturumu açmanın geçici olarak kaldırılması</span><span class="sxs-lookup"><span data-stu-id="81e7f-168">Temporary removal of User login using PSCredential</span></span>
- <span data-ttu-id="81e7f-169">.NET Standard kimlik doğrulama akışındaki değişiklikler nedeniyle, PSCredential üzerinden kullanıcı oturumu açmayı geçici olarak kaldırıyoruz.</span><span class="sxs-lookup"><span data-stu-id="81e7f-169">Due to changes in the authentication flow for .NET Standard, we are temporarily removing user login via PSCredential.</span></span> <span data-ttu-id="81e7f-170">Bu özellik, Windows PowerShell 5.1’in 15.01.2019 tarihli yayınında yeniden kullanıma sunulacaktır.</span><span class="sxs-lookup"><span data-stu-id="81e7f-170">This capability will be re-introduced in the 1/15/2019 release for Windows PowerShell 5.1.</span></span> <span data-ttu-id="81e7f-171">Bu konu, [bu sorunda](https://github.com/Azure/azure-powershell/issues/7430) ayrıntılı olarak ele alınmıştır.</span><span class="sxs-lookup"><span data-stu-id="81e7f-171">This is duscussed in detail in [this issue.](https://github.com/Azure/azure-powershell/issues/7430)</span></span>

### <a name="default-device-code-login-instead-of-web-browser-prompt"></a><span data-ttu-id="81e7f-172">Web Tarayıcısı istemi yerine varsayılan Cihaz Kodu ile oturum açma</span><span class="sxs-lookup"><span data-stu-id="81e7f-172">Default Device Code login instead of Web Browser prompt</span></span>
- <span data-ttu-id="81e7f-173">.NET Standard kimlik doğrulama akışındaki değişiklikler nedeniyle, etkileşimli oturum açma sırasında varsayılan oturum açma akışı olarak cihazla oturum açmayı kullanıyoruz.</span><span class="sxs-lookup"><span data-stu-id="81e7f-173">Due to changes in the authentication flow for .NET Standard, we are using device login as the default login flow during interactive login.</span></span> <span data-ttu-id="81e7f-174">Web tarayıcısı tabanlı oturum açma, Windows PowerShell 5.1 için 15.01.2019 tarihli yayınla birlikte yeniden varsayılan seçenek olarak kullanıma sunulacaktır.</span><span class="sxs-lookup"><span data-stu-id="81e7f-174">Web browser based login will be re-introduced for Windows PowerShell 5.1 as the default in the 1/15/2019 release.</span></span> <span data-ttu-id="81e7f-175">İlgili tarihte, kullanıcılar bir Switch parametresini kullanarak cihaz oturumunu seçebilecek.</span><span class="sxs-lookup"><span data-stu-id="81e7f-175">At that time, users will be able to choose device login using a Switch parameter.</span></span>

## <a name="module-breaking-changes"></a><span data-ttu-id="81e7f-176">Modüldeki yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="81e7f-176">Module breaking changes</span></span>

### <a name="azapimanagement-previously-azurermapimanagement"></a><span data-ttu-id="81e7f-177">Az.ApiManagement (eski adıyla AzureRM.ApiManagement)</span><span class="sxs-lookup"><span data-stu-id="81e7f-177">Az.ApiManagement (previously AzureRM.ApiManagement)</span></span>
- <span data-ttu-id="81e7f-178">Şu cmdlet’ler kaldırılıyor:</span><span class="sxs-lookup"><span data-stu-id="81e7f-178">Removing the following cmdlets:</span></span>
  - <span data-ttu-id="81e7f-179">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="81e7f-179">New-AzureRmApiManagementHostnameConfiguration</span></span>
  - <span data-ttu-id="81e7f-180">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="81e7f-180">Set-AzureRmApiManagementHostnames</span></span>
  - <span data-ttu-id="81e7f-181">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="81e7f-181">Update-AzureRmApiManagementDeployment</span></span>
  - <span data-ttu-id="81e7f-182">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="81e7f-182">Import-AzureRmApiManagementHostnameCertificate</span></span>
  - <span data-ttu-id="81e7f-183">Bu özellikleri ayarlamak için bunun yerine **Set-AzApiManagement** cmdlet’ini kullanın</span><span class="sxs-lookup"><span data-stu-id="81e7f-183">Use **Set-AzApiManagement** cmdlet to set these properites instead</span></span>
- <span data-ttu-id="81e7f-184">Aşağıdaki özellikler kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="81e7f-184">Following properties were removed</span></span>
  - <span data-ttu-id="81e7f-185">`PsApiManagementContext` öğesinden `PsApiManagementHostnameConfiguration` türündeki `PortalHostnameConfiguration`, `ProxyHostnameConfiguration`, `ManagementHostnameConfiguration` ve `ScmHostnameConfiguration` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="81e7f-185">Removed property `PortalHostnameConfiguration`, `ProxyHostnameConfiguration`, `ManagementHostnameConfiguration` and `ScmHostnameConfiguration` of type `PsApiManagementHostnameConfiguration` from `PsApiManagementContext`.</span></span> <span data-ttu-id="81e7f-186">Bunun yerine `PsApiManagementCustomHostNameConfiguration` türündeki `PortalCustomHostnameConfiguration`, `ProxyCustomHostnameConfiguration`, `ManagementCustomHostnameConfiguration` ve `ScmCustomHostnameConfiguration` özelliğini kullanın.</span><span class="sxs-lookup"><span data-stu-id="81e7f-186">Instead use `PortalCustomHostnameConfiguration`, `ProxyCustomHostnameConfiguration`, `ManagementCustomHostnameConfiguration` and `ScmCustomHostnameConfiguration` of type `PsApiManagementCustomHostNameConfiguration`.</span></span>
  - <span data-ttu-id="81e7f-187">PsApiManagementContext öğesinden `StaticIPs` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="81e7f-187">Removed property `StaticIPs` from PsApiManagementContext.</span></span> <span data-ttu-id="81e7f-188">Özellik `PublicIPAddresses` ve `PrivateIPAddresses` olarak bölündü.</span><span class="sxs-lookup"><span data-stu-id="81e7f-188">The property has been split into `PublicIPAddresses` and `PrivateIPAddresses`.</span></span>
  - <span data-ttu-id="81e7f-189">New-AzureApiManagementVirtualNetwork cmdlet’inden gerekli olan `Location` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="81e7f-189">Removed required property `Location` from New-AzureApiManagementVirtualNetwork cmdlet.</span></span>

### <a name="azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates"></a><span data-ttu-id="81e7f-190">Az.Billing (eski adıyla AzureRM.Billing, AzureRM.Consumption ve AzureRM.UsageAggregates)</span><span class="sxs-lookup"><span data-stu-id="81e7f-190">Az.Billing (previously AzureRM.Billing, AzureRM.Consumption, and AzureRM.UsageAggregates)</span></span>
- <span data-ttu-id="81e7f-191">`Get-AzConsumptionUsageDetail` cmdlet’inden `InvoiceName` parametresi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="81e7f-191">The `InvoiceName` parameter was removed from the `Get-AzConsumptionUsageDetail` cmdlet.</span></span>  <span data-ttu-id="81e7f-192">Fatura için betiklerin diğer kimlik parametrelerini kullanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="81e7f-192">Scripts will need to use other identity parameters for the invoice.</span></span>

### <a name="azcognitiveservices-previously-azurermcognitiveservices"></a><span data-ttu-id="81e7f-193">Az.CognitiveServices (eski adıyla AzureRM.CognitiveServices)</span><span class="sxs-lookup"><span data-stu-id="81e7f-193">Az.CognitiveServices (previously AzureRM.CognitiveServices)</span></span>
- <span data-ttu-id="81e7f-194">`Get-AzCognitiveServicesAccountSkus` cmdlet’inden `GetSkusWithAccountParamSetName` parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="81e7f-194">Removed `GetSkusWithAccountParamSetName` parameter set from `Get-AzCognitiveServicesAccountSkus` cmdlet.</span></span>  <span data-ttu-id="81e7f-195">ResourceGroupName ve Hesap Adı parametrelerini kullanmak yerine Sku’ları Hesap Türüne ve Konuma göre almalısınız.</span><span class="sxs-lookup"><span data-stu-id="81e7f-195">You must get Skus by Account Type and Location, instead of using ResourceGroupName and Account Name.</span></span>

### <a name="azcompute-previously-azurermcompute"></a><span data-ttu-id="81e7f-196">Az.Compute (eski adıyla AzureRM.Compute)</span><span class="sxs-lookup"><span data-stu-id="81e7f-196">Az.Compute (previously AzureRM.Compute)</span></span>
- <span data-ttu-id="81e7f-197">`PSVirtualMachine` ve `PSVirtualMachineScaleSet` nesnelerinde `Identity` özelliğinden `IdentityIds` kaldırıldı Betikler artık işleme kararları vermek için bu alanın değerini kullanmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="81e7f-197">`IdentityIds` are removed from `Identity` property in `PSVirtualMachine` and `PSVirtualMachineScaleSet` objects Scripts should no longer use the value of this field to make processing decisions.</span></span>
- <span data-ttu-id="81e7f-198">`PSVirtualMachineScaleSetVM` nesnesinin `InstanceView` özelliğinin `VirtualMachineInstanceView` olan türü `VirtualMachineScaleSetVMInstanceView` olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="81e7f-198">The type of `InstanceView` property of `PSVirtualMachineScaleSetVM` object is changed from `VirtualMachineInstanceView` to `VirtualMachineScaleSetVMInstanceView`</span></span>
- <span data-ttu-id="81e7f-199">`UpgradePolicy` özelliğinden `AutoOSUpgradePolicy` ve `AutomaticOSUpgrade` özelliği kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="81e7f-199">`AutoOSUpgradePolicy` and `AutomaticOSUpgrade` properties are removed from `UpgradePolicy` property</span></span>
- <span data-ttu-id="81e7f-200">`PSSnapshotUpdate` nesnesindeki `Sku` özelliğinin `DiskSku` olan türü `SnapshotSku` olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="81e7f-200">The type of `Sku` property in `PSSnapshotUpdate` object is changed from `DiskSku` to `SnapshotSku`</span></span>
- <span data-ttu-id="81e7f-201">`Add-AzVMDataDisk` cmdlet’inden `VmScaleSetVMParameterSet` kaldırıldı, artık tek bir ScaleSet sanal makinesine veri diski ekleyemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="81e7f-201">`VmScaleSetVMParameterSet` is removed from `Add-AzVMDataDisk` cmdlet, you cna no longer add a data disk individually to a ScaleSet VM.</span></span>

### <a name="azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2"></a><span data-ttu-id="81e7f-202">Az.DataFactory (eski adıyla AzureRM.DataFactories ve AzureRM.DataFactoryV2)</span><span class="sxs-lookup"><span data-stu-id="81e7f-202">Az.DataFactory (previously AzureRM.DataFactories and AzureRM.DataFactoryV2)</span></span>
- <span data-ttu-id="81e7f-203">`New-AzDataFactoryEncryptValue` cmdlet’inde `GatewayName` parametresi zorunlu hale geldi</span><span class="sxs-lookup"><span data-stu-id="81e7f-203">The `GatewayName` parameter has become mandatory in the `New-AzDataFactoryEncryptValue` cmdlet</span></span>
- <span data-ttu-id="81e7f-204">`New-AzDataFactoryGatewayKey` cmdlet'i kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="81e7f-204">Removed `New-AzDataFactoryGatewayKey` cmdlet</span></span>
- <span data-ttu-id="81e7f-205">`Get-AzDataFactoryV2ActivityRun` cmdlet’inden `LinkedServiceName` parametresi kaldırıldı Betikler artık işleme kararları vermek için bu alanın değerini kullanmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="81e7f-205">Removed `LinkedServiceName` parameter from `Get-AzDataFactoryV2ActivityRun` cmdlet Scripts should no longer use the value of this field to make processing decisions.</span></span>

### <a name="azdatalakeanalytics-previously-azurermdatalakeanalytics"></a><span data-ttu-id="81e7f-206">Az.DataLakeAnalytics (eski adıyla AzureRM.DataLakeAnalytics)</span><span class="sxs-lookup"><span data-stu-id="81e7f-206">Az.DataLakeAnalytics (previously AzureRM.DataLakeAnalytics)</span></span>
- <span data-ttu-id="81e7f-207">Kullanım dışı cmdlet’ler kaldırıldı: `New-AzDataLakeAnalyticsCatalogSecret`, `Remove-AzDataLakeAnalyticsCatalogSecret` ve `Set-AzDataLakeAnalyticsCatalogSecret`</span><span class="sxs-lookup"><span data-stu-id="81e7f-207">Removed deprecated cmdlets: `New-AzDataLakeAnalyticsCatalogSecret`, `Remove-AzDataLakeAnalyticsCatalogSecret`, and `Set-AzDataLakeAnalyticsCatalogSecret`</span></span>

### <a name="azdatalakestore-previously-azurermdatalakestore"></a><span data-ttu-id="81e7f-208">Az.DataLakeStore (eski adıyla AzureRM.DataLakeStore)</span><span class="sxs-lookup"><span data-stu-id="81e7f-208">Az.DataLakeStore (previously AzureRM.DataLakeStore)</span></span>
- <span data-ttu-id="81e7f-209">Aşağıdaki cmdlet’lerin `Encoding` parametresinin `FileSystemCmdletProviderEncoding` olan türü `System.Text.Encoding` olarak değişti.</span><span class="sxs-lookup"><span data-stu-id="81e7f-209">The following cmdlets have had the `Encoding` parameter changed from the type `FileSystemCmdletProviderEncoding` to `System.Text.Encoding`.</span></span> <span data-ttu-id="81e7f-210">Bu değişiklikle birlikte `String` ve `Oem` kodlama değerleri kaldırılıyor.</span><span class="sxs-lookup"><span data-stu-id="81e7f-210">This change removes the encoding values `String` and `Oem`.</span></span> <span data-ttu-id="81e7f-211">Önceki diğer tüm kodlama değerleri olduğu gibi kaldı.</span><span class="sxs-lookup"><span data-stu-id="81e7f-211">All the other prior encoding values remain.</span></span>
  - <span data-ttu-id="81e7f-212">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="81e7f-212">New-AzureRmDataLakeStoreItem</span></span>
  - <span data-ttu-id="81e7f-213">Add-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="81e7f-213">Add-AzureRmDataLakeStoreItemContent</span></span>
  - <span data-ttu-id="81e7f-214">Get-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="81e7f-214">Get-AzureRmDataLakeStoreItemContent</span></span>
- <span data-ttu-id="81e7f-215">`New-AzDataLakeStoreAccount` ve `Set-AzDataLakeStoreAccount` cmdlet’inden kullanım dışı `Tags` özellik diğer adı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="81e7f-215">Removed deprecated `Tags` property alias from `New-AzDataLakeStoreAccount` and `Set-AzDataLakeStoreAccount` cmdlets</span></span>

  <span data-ttu-id="81e7f-216">Şunları kullanan betikler:</span><span class="sxs-lookup"><span data-stu-id="81e7f-216">Scripts using</span></span>
  ```powershell
  New-AzureRMDataLakeStoreAccount -Tags @{TagName="TagValue"}
  ```

  <span data-ttu-id="81e7f-217">Şöyle değiştirilmelidir:</span><span class="sxs-lookup"><span data-stu-id="81e7f-217">Should be changed to</span></span>
  ```powershell
  New-AzDataLakeStoreAccount -Tag @{TagName="TagValue"}
  ```

- <span data-ttu-id="81e7f-218">```PSDataLakeStoreAccountBasic``` nesnesinden kullanım dışı ```Identity```, ```EncryptionState```, ```EncrypotionProvisioningState```, ```EncryptionConfig```, ```FirewallState```, ```FirewallRules```, ```VirtualNetworkRules```, ```TrustedIdProviderState```, ```TrustedIdProviders```, ```DefaultGroup```, ```NewTier```, ```CurrentTier```, ```FirewallAllowAzureIps``` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="81e7f-218">Removed deprecated properties ```Identity```, ```EncryptionState```, ```EncrypotionProvisioningState```, ```EncryptionConfig```, ```FirewallState```, ```FirewallRules```, ```VirtualNetworkRules```, ```TrustedIdProviderState```, ```TrustedIdProviders```, ```DefaultGroup```, ```NewTier```, ```CurrentTier```, ```FirewallAllowAzureIps``` from ```PSDataLakeStoreAccountBasic``` object.</span></span>  <span data-ttu-id="81e7f-219">```Get-AzDataLakeStoreAccount``` cmdlet’inden döndürülen ```PSDatalakeStoreAccount``` özelliğini kullanan hiçbir betik bu özelliklere başvurmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="81e7f-219">Any script that uses the ```PSDatalakeStoreAccount``` returned from ```Get-AzDataLakeStoreAccount``` should not reference these properties.</span></span>

### <a name="azkeyvault-previously-azurermkeyvault"></a><span data-ttu-id="81e7f-220">Az.KeyVault (eski adıyla AzureRM.KeyVault)</span><span class="sxs-lookup"><span data-stu-id="81e7f-220">Az.KeyVault (previously AzureRM.KeyVault)</span></span>
- <span data-ttu-id="81e7f-221">`PSKeyVaultKeyAttributes`, `PSKeyVaultKeyIdentityItem` ve `PSKeyVaultSecretAttributes` nesnesinden `PurgeDisabled` özelliği kaldırıldı Betikler artık işleme kararları vermek için ```PurgeDisabled``` özelliğine başvurmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="81e7f-221">The `PurgeDisabled` property was removed from the `PSKeyVaultKeyAttributes`, `PSKeyVaultKeyIdentityItem`, and `PSKeyVaultSecretAttributes` objects Scripts shoudl no longer reference the ```PurgeDisabled``` property to make processing decisions.</span></span>

### <a name="azmedia-previously-azurermmedia"></a><span data-ttu-id="81e7f-222">Az.Media (eski adıyla AzureRM.Media)</span><span class="sxs-lookup"><span data-stu-id="81e7f-222">Az.Media (previously AzureRM.Media)</span></span>
- <span data-ttu-id="81e7f-223">`New-AzMediaService` cmdlet’inden kullanım dışı `Tags` özelliği diğer adı kaldırıldı Şunları kullanan betikler:</span><span class="sxs-lookup"><span data-stu-id="81e7f-223">Remove deprecated `Tags` property alias from `New-AzMediaService` cmdlet Scripts using</span></span>
  ```powershell
  New-AzureRMMediaService -Tags @{TagName="TagValue"}
  ```

  <span data-ttu-id="81e7f-224">Şöyle değiştirilmelidir:</span><span class="sxs-lookup"><span data-stu-id="81e7f-224">Should be changed to</span></span>
  ```powershell
  New-AzMMediaService -Tag @{TagName="TagValue"}
  ```
### <a name="azmonitor-previously-azurerminsights"></a><span data-ttu-id="81e7f-225">Az.Monitor (eski adıyla AzureRM.Insights)</span><span class="sxs-lookup"><span data-stu-id="81e7f-225">Az.Monitor (previously AzureRM.Insights)</span></span>
- <span data-ttu-id="81e7f-226">`Set-AzDiagnosticSetting` cmdlet’inden alınan tekil parametre adları tercih edilerek çoğul ad `Categories` ve `Timegrains` parametresi kaldırıldı Şunları kullanan betikler:</span><span class="sxs-lookup"><span data-stu-id="81e7f-226">Removed plural names `Categories` and `Timegrains` parameter in favor of singular parameter names from `Set-AzDiagnosticSetting` cmdlet Scripts using</span></span>
  ```powershell
  Set-AzureRmDiagnosticSetting -Timegrains PT1M -Categories Category1, Category2
  ```

  <span data-ttu-id="81e7f-227">Şöyle değiştirilmelidir:</span><span class="sxs-lookup"><span data-stu-id="81e7f-227">Should be changed to</span></span>
  ```powershell
  Set-AzDiagnosticSetting -Timegrain PT1M -Category Category1, Category2
  ```
### <a name="aznetwork-previously-azurermnetwork"></a><span data-ttu-id="81e7f-228">Az.Network (eski adıyla AzureRM.Network)</span><span class="sxs-lookup"><span data-stu-id="81e7f-228">Az.Network (previously AzureRM.Network)</span></span>
- <span data-ttu-id="81e7f-229">`Get-AzServiceEndpointPolicyDefinition` cmdlet’inden kullanım dışı `ResourceId` parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="81e7f-229">Removed deprecated `ResourceId` parameter from `Get-AzServiceEndpointPolicyDefinition` cmdlet</span></span>
- <span data-ttu-id="81e7f-230">`PSVirtualNetwork` nesnesinden kullanım dışı `EnableVmProtection` özelliği kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="81e7f-230">Removed deprecated `EnableVmProtection` property from `PSVirtualNetwork` object</span></span>
- <span data-ttu-id="81e7f-231">Kullanım dışı `Set-AzVirtualNetworkGatewayVpnClientConfig` cmdlet’i kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="81e7f-231">Removed deprecated `Set-AzVirtualNetworkGatewayVpnClientConfig` cmdlet</span></span>
  
<span data-ttu-id="81e7f-232">Betikler artık bu alanların değerlerini temel alan işleme kararları almamalıdır.</span><span class="sxs-lookup"><span data-stu-id="81e7f-232">Scripts shoudl no longer make processing decisions based on the values fo these fields.</span></span>

### <a name="azoperationalinsights-previously-azurermoperationalinsights"></a><span data-ttu-id="81e7f-233">Az.OperationalInsights (eski adıyla AzureRM.OperationalInsights)</span><span class="sxs-lookup"><span data-stu-id="81e7f-233">Az.OperationalInsights (previously AzureRM.OperationalInsights)</span></span>
- <span data-ttu-id="81e7f-234">`Get-AzOperationalInsightsDataSource` için varsayılan parametre kümesi kaldırıldı, varsayılan parametre kümesi `ByWorkspaceNameByKind` oldu</span><span class="sxs-lookup"><span data-stu-id="81e7f-234">Default parameter set for `Get-AzOperationalInsightsDataSource` is removed, and `ByWorkspaceNameByKind` has become the default parameter set</span></span>

  <span data-ttu-id="81e7f-235">Veri kaynaklarını şunu kullanarak listeleyen betikler:</span><span class="sxs-lookup"><span data-stu-id="81e7f-235">Scripts that listed data sources using</span></span>
  ```powershell
  Get-AzureRmOperationalInsightsDataSource
  ```

  <span data-ttu-id="81e7f-236">Bir Tür belirtecek şekilde değiştirilmelidir</span><span class="sxs-lookup"><span data-stu-id="81e7f-236">Should be changed to specify a Kind</span></span>
  ```powershell
  Get-AzOperationalInsightsDataSource -Kind AzureActivityLog
  ```

### <a name="azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery"></a><span data-ttu-id="81e7f-237">Az.RecoveryServices (eski adıyla AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup ve AzureRM.RecoveryServices.SiteRecovery)</span><span class="sxs-lookup"><span data-stu-id="81e7f-237">Az.RecoveryServices (previously AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup, and AzureRM.RecoveryServices.SiteRecovery)</span></span>
- <span data-ttu-id="81e7f-238">`New/Set-AzRecoveryServicesAsrPolicy` cmdlet’inden `Encryption` parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="81e7f-238">Removed `Encryption` parameter from `New/Set-AzRecoveryServicesAsrPolicy` cmdlet</span></span>
- <span data-ttu-id="81e7f-239">Artık `Restore-AzRecoveryServicesBackupItem` cmdlet'indeki yönetilen disk geri yükleme işlemleri için `TargetStorageAccountName` parametresi zorunludur</span><span class="sxs-lookup"><span data-stu-id="81e7f-239">`TargetStorageAccountName` parameter is now mandatory for managed disk restores in `Restore-AzRecoveryServicesBackupItem` cmdlet</span></span>
- <span data-ttu-id="81e7f-240">`Restore-AzRecoveryServicesBackupItem` cmdlet’inden `StorageAccountName` ve `StorageAccountResourceGroupName` parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="81e7f-240">Removed `StorageAccountName` and `StorageAccountResourceGroupName` parameters in `Restore-AzRecoveryServicesBackupItem` cmdlet</span></span>
- <span data-ttu-id="81e7f-241">`Get-AzRecoveryServicesBackupContainer` cmdlet’inden `Name` parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="81e7f-241">Removed `Name`parameter in `Get-AzRecoveryServicesBackupContainer` cmdlet</span></span>

### <a name="azresources-previously-azurermresources"></a><span data-ttu-id="81e7f-242">Az.Resources (eski adıyla AzureRM.Resources)</span><span class="sxs-lookup"><span data-stu-id="81e7f-242">Az.Resources (previously AzureRM.Resources)</span></span>
- <span data-ttu-id="81e7f-243">`New/Set-AzPolicyAssignment` cmdlet’inden `Sku` parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="81e7f-243">Removed `Sku` parameter from `New/Set-AzPolicyAssignment` cmdlet</span></span>
- <span data-ttu-id="81e7f-244">`New-AzADServicePrincipal` ve `New-AzADSpCredential` cmdlet’inden `Password` parametresi kaldırıldı Parolalar otomatik olarak oluşturulduğundan, daha önce parolayı sağlayan betikler:</span><span class="sxs-lookup"><span data-stu-id="81e7f-244">Removed `Password` parameter from `New-AzADServicePrincipal` and `New-AzADSpCredential` cmdlet Passwords are automatically generated, scripts that provided the password:</span></span>
  ```powershell
  New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 -Password $secPassword
  ```

  <span data-ttu-id="81e7f-245">Parolayı çıktıdan alacak şekilde değiştirilmelidir:</span><span class="sxs-lookup"><span data-stu-id="81e7f-245">Should be changed to retriedve the password from the output:</span></span>
  ```powershell
  $credential = New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
  $secPassword = $credential.Secret
  ```

### <a name="azservicefabric-previously-azurermservicefabric"></a><span data-ttu-id="81e7f-246">Az.ServiceFabric (eski adıyla AzureRM.ServiceFabric)</span><span class="sxs-lookup"><span data-stu-id="81e7f-246">Az.ServiceFabric (previously AzureRM.ServiceFabric)</span></span>
- <span data-ttu-id="81e7f-247">Aşağıdaki cmdlet dönüş türleri değişmiştir:</span><span class="sxs-lookup"><span data-stu-id="81e7f-247">The following cmdlet return types have been changed:</span></span>
  - <span data-ttu-id="81e7f-248">`ApplicationHealthPolicy` türündeki `SerivceTypeHealthPolicies` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="81e7f-248">The property `SerivceTypeHealthPolicies` of type `ApplicationHealthPolicy` has been removed.</span></span>
  - <span data-ttu-id="81e7f-249">`ClusterUpgradeDeltaHealthPolicy` türündeki `ApplicationHealthPolicies` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="81e7f-249">The property `ApplicationHealthPolicies` of type `ClusterUpgradeDeltaHealthPolicy` has been removed.</span></span>
  - <span data-ttu-id="81e7f-250">`ClusterUpgradePolicy` türündeki `OverrideUserUpgradePolicy` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="81e7f-250">The property `OverrideUserUpgradePolicy` of type `ClusterUpgradePolicy` has been removed.</span></span>
  - <span data-ttu-id="81e7f-251">Bu değişikliklerden aşağıdaki cmdlet’ler etkilenir:</span><span class="sxs-lookup"><span data-stu-id="81e7f-251">These changes affect the following cmdlets:</span></span>
    - <span data-ttu-id="81e7f-252">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="81e7f-252">Add-AzServiceFabricClientCertificate</span></span>
    - <span data-ttu-id="81e7f-253">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="81e7f-253">Add-AzServiceFabricClusterCertificate</span></span>
    - <span data-ttu-id="81e7f-254">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="81e7f-254">Add-AzServiceFabricNode</span></span>
    - <span data-ttu-id="81e7f-255">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="81e7f-255">Add-AzServiceFabricNodeType</span></span>
    - <span data-ttu-id="81e7f-256">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="81e7f-256">Get-AzServiceFabricCluster</span></span>
    - <span data-ttu-id="81e7f-257">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="81e7f-257">Remove-AzServiceFabricClientCertificate</span></span>
    - <span data-ttu-id="81e7f-258">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="81e7f-258">Remove-AzServiceFabricClusterCertificate</span></span>
    - <span data-ttu-id="81e7f-259">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="81e7f-259">Remove-AzServiceFabricNode</span></span>
    - <span data-ttu-id="81e7f-260">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="81e7f-260">Remove-AzServiceFabricNodeType</span></span>
    - <span data-ttu-id="81e7f-261">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="81e7f-261">Remove-AzServiceFabricSetting</span></span>
    - <span data-ttu-id="81e7f-262">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="81e7f-262">Set-AzServiceFabricSetting</span></span>
    - <span data-ttu-id="81e7f-263">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="81e7f-263">Set-AzServiceFabricUpgradeType</span></span>
    - <span data-ttu-id="81e7f-264">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="81e7f-264">Update-AzServiceFabricDurability</span></span>
    - <span data-ttu-id="81e7f-265">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="81e7f-265">Update-AzServiceFabricReliability</span></span>

### <a name="azsql-previously-azurermsql"></a><span data-ttu-id="81e7f-266">Az.Sql (eski adıyla AzureRM.Sql)</span><span class="sxs-lookup"><span data-stu-id="81e7f-266">Az.Sql (previously AzureRM.Sql)</span></span>
- <span data-ttu-id="81e7f-267">`Set-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet’inden `State` ve `ResourceId` parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="81e7f-267">Removed `State` and `ResourceId` parameters from `Set-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet</span></span>
- <span data-ttu-id="81e7f-268">Kullanım dışı cmdlet’ler kaldırıldı: `Get/Set-AzSqlServerBackupLongTermRetentionVault`, `Get/Start/Stop-AzSqlServerUpgrade`, `Get/Set-AzSqlDatabaseAuditingPolicy`, `Get/Set-AzSqlServerAuditingPolicy`, `Remove-AzSqlDatabaseAuditing`, `Remove-AzSqlServerAuditing`</span><span class="sxs-lookup"><span data-stu-id="81e7f-268">Removed deprecated cmdlets: `Get/Set-AzSqlServerBackupLongTermRetentionVault`, `Get/Start/Stop-AzSqlServerUpgrade`, `Get/Set-AzSqlDatabaseAuditingPolicy`, `Get/Set-AzSqlServerAuditingPolicy`, `Remove-AzSqlDatabaseAuditing`, `Remove-AzSqlServerAuditing`</span></span>
- <span data-ttu-id="81e7f-269">`Get-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet’inden kullanım dışı `Current` parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="81e7f-269">Removed deprecated parameter `Current` from `Get-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet</span></span>
- <span data-ttu-id="81e7f-270">`Get-AzSqlServerServiceObjective` cmdlet’inden kullanım dışı `DatabaseName` parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="81e7f-270">Removed deprecated parameter `DatabaseName` from `Get-AzSqlServerServiceObjective` cmdlet</span></span>
- <span data-ttu-id="81e7f-271">`Set-AzSqlDatabaseDataMaskingPolicy` cmdlet’inden kullanım dışı `PrivilegedLogin` parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="81e7f-271">Removed deprecated parameter `PrivilegedLogin` from `Set-AzSqlDatabaseDataMaskingPolicy` cmdlet</span></span>

### <a name="azstorage-previously-azurestorage-and-azurermstorage"></a><span data-ttu-id="81e7f-272">Az.Storage (eski adıyla Azure.Storage and AzureRM.Storage)</span><span class="sxs-lookup"><span data-stu-id="81e7f-272">Az.Storage (previously Azure.Storage and AzureRM.Storage)</span></span>
- <span data-ttu-id="81e7f-273">Yalnızca depolama hesabı adıyla bir Oauth depolama bağlamı oluşturulmasının desteklenmesi için varsayılan parametre kümesi `OAuthParameterSet` olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="81e7f-273">To support creating an Oauth storage context with only the storage account name, the default parameter set has been changed to `OAuthParameterSet`</span></span>
  - <span data-ttu-id="81e7f-274">Örnek: `$ctx = New-AzureStorageContext -StorageAccountName $accountName`</span><span class="sxs-lookup"><span data-stu-id="81e7f-274">Example: `$ctx = New-AzureStorageContext -StorageAccountName $accountName`</span></span>
- <span data-ttu-id="81e7f-275">`Get-AzStorageUsage` cmdlet’inde `Location` parametresi zorunlu hale geldi</span><span class="sxs-lookup"><span data-stu-id="81e7f-275">The `Location` parameter has become mandatory in the `Get-AzStorageUsage` cmdlet</span></span>
- <span data-ttu-id="81e7f-276">Depolama API’si metotları artık zaman uyumlu API çağrıları yerine Görev Tabanlı Zaman Uyumsuz Düzeni (TAP) kullanıyor.</span><span class="sxs-lookup"><span data-stu-id="81e7f-276">The Storage API methods now use the Task-based Asynchronous Pattern (TAP), instead of synchronous API calls.</span></span>
#### <a name="1-blob-snapshot"></a><span data-ttu-id="81e7f-277">1. Blob Anlık Görüntüsü</span><span class="sxs-lookup"><span data-stu-id="81e7f-277">1. Blob Snapshot</span></span>
##### <a name="before"></a><span data-ttu-id="81e7f-278">Önce:</span><span class="sxs-lookup"><span data-stu-id="81e7f-278">Before:</span></span>
```powershell
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$b.ICloudBlob.Snapshot()
```

##### <a name="after"></a><span data-ttu-id="81e7f-279">Sonra:</span><span class="sxs-lookup"><span data-stu-id="81e7f-279">After:</span></span>
```powershell
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$task = $b.ICloudBlob.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="2-share-snapshot"></a><span data-ttu-id="81e7f-280">2. Anlık Görüntüyü Paylaş</span><span class="sxs-lookup"><span data-stu-id="81e7f-280">2. Share Snapshot</span></span>
##### <a name="before"></a><span data-ttu-id="81e7f-281">Önce:</span><span class="sxs-lookup"><span data-stu-id="81e7f-281">Before:</span></span>
```powershell
$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$snapshot = $Share.Snapshot()
```
#####  <a name="after"></a><span data-ttu-id="81e7f-282">Sonra:</span><span class="sxs-lookup"><span data-stu-id="81e7f-282">After:</span></span>
```powershell

$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$task = $Share.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="3-undelete-a-soft-delete-blob"></a><span data-ttu-id="81e7f-283">3. Geçici silme işlemini geri alma</span><span class="sxs-lookup"><span data-stu-id="81e7f-283">3. Undelete a soft delete blob</span></span>
##### <a name="before"></a><span data-ttu-id="81e7f-284">Önce:</span><span class="sxs-lookup"><span data-stu-id="81e7f-284">Before:</span></span>
```powershell
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$b.ICloudBlob.Undelete()
```
##### <a name="after"></a><span data-ttu-id="81e7f-285">Sonra:</span><span class="sxs-lookup"><span data-stu-id="81e7f-285">After:</span></span>
```powershell
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$task = $b.ICloudBlob.UndeleteAsync()
$task.Wait()
```

#### <a name="4-set-blob-tier"></a><span data-ttu-id="81e7f-286">4. Blob Katmanını Ayarla</span><span class="sxs-lookup"><span data-stu-id="81e7f-286">4. Set Blob Tier</span></span>
##### <a name="before"></a><span data-ttu-id="81e7f-287">Önce:</span><span class="sxs-lookup"><span data-stu-id="81e7f-287">Before:</span></span>
```powershell
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$blockBlob.ICloudBlob.SetStandardBlobTier("hot")

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$pageBlob.ICloudBlob.SetPremiumBlobTier("P4")
```

##### <a name="after"></a><span data-ttu-id="81e7f-288">Sonra:</span><span class="sxs-lookup"><span data-stu-id="81e7f-288">After:</span></span>
```powershell
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$task = $blockBlob.ICloudBlob.SetStandardBlobTierAsync("hot")
$task.Wait()

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$task = $pageBlob.ICloudBlob.SetPremiumBlobTierAsync("P4")
$task.Wait()
```

### <a name="azwebsites-previously-azurermwebsites"></a><span data-ttu-id="81e7f-289">Az.Websites (eski adıyla AzureRM.Websites)</span><span class="sxs-lookup"><span data-stu-id="81e7f-289">Az.Websites (previously AzureRM.Websites)</span></span>
- <span data-ttu-id="81e7f-290">`PSAppServicePlan`, `PSCertificate`, `PSCloningInfo` ve `PSSite` nesnesinden kullanım dışı özellikler kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="81e7f-290">Removed deprecated properties from the `PSAppServicePlan`, `PSCertificate`, `PSCloningInfo`, and `PSSite` objects</span></span>