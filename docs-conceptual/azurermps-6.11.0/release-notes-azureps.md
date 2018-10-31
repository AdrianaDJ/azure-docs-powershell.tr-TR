---
title: Azure PowerShell Değişiklik Günlüğü | Microsoft Docs
description: Azure PowerShell'in en son sürümünde yapılan değişikliklerin geçmişi aşağıda verilmiştir.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 08/28/2018
ms.openlocfilehash: eec8b5960f787fa9ca1130b4f8b49c9d896aa99e
ms.sourcegitcommit: 5f946a535eccca0b3ddf3db8f617b32564a88938
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50001516"
---
# <a name="release-notes"></a><span data-ttu-id="b7e09-103">Sürüm notları</span><span class="sxs-lookup"><span data-stu-id="b7e09-103">Release notes</span></span>

<span data-ttu-id="b7e09-104">Azure PowerShell'in bu sürümünde yapılan değişikliklerin listesi aşağıda verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="b7e09-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="6110---october-2018"></a><span data-ttu-id="b7e09-105">6.11.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="b7e09-105">6.11.0 - October 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="b7e09-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="b7e09-106">AzureRM.Profile</span></span>
* <span data-ttu-id="b7e09-107">CloudShell’de Get-AzureRmSubscription sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="b7e09-107">Fix issue with Get-AzureRmSubscription in CloudShell</span></span>
* <span data-ttu-id="b7e09-108">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-108">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="b7e09-109">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="b7e09-109">AzureRM.Backup</span></span>
* <span data-ttu-id="b7e09-110">Azure Backup cmdlet’leri kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="b7e09-110">Deprecated Azure Backup cmdlets.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="b7e09-111">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="b7e09-111">AzureRM.Compute</span></span>
* <span data-ttu-id="b7e09-112">'New-AzureRmVm' için basit parametre kümesi kullanıldığında hızlandırılmış ağların açılacağı VM boyutları beyaz listesine yeni boyutlar eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-112">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzureRmVm'</span></span>
* <span data-ttu-id="b7e09-113">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-113">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="b7e09-114">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b7e09-114">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="b7e09-115">Sanal Ağ Kuralları desteği ekleme</span><span class="sxs-lookup"><span data-stu-id="b7e09-115">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="b7e09-116">Get-AzureRmDataLakeStoreVirtualNetworkRule: Azure Data Lake Store sanal ağ kuralını alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="b7e09-116">Get-AzureRmDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="b7e09-117">Add-AzureRmDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabına sanal ağ kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="b7e09-117">Add-AzureRmDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="b7e09-118">Set-AzureRmDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabında belirtilen sanal ağ kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="b7e09-118">Set-AzureRmDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="b7e09-119">Remove-AzureRmDataLakeStoreVirtualNetworkRule: Azure Data Lake Store sanal ağ kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="b7e09-119">Remove-AzureRmDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="b7e09-120">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="b7e09-120">AzureRM.Network</span></span>
* <span data-ttu-id="b7e09-121">Test-AzureRmNetworkWatcherConnectivity cmdlet'i güncelleştirildi, arka uca protokol değerini geçiriyor.</span><span class="sxs-lookup"><span data-stu-id="b7e09-121">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="b7e09-122">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-122">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="b7e09-123">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="b7e09-123">AzureRM.Resources</span></span>
* <span data-ttu-id="b7e09-124">Get-AzureRMRoleDefinition cmdlet'inin anlaşılmaz bir özel durum oluşturmasına neden olan hata (varsayılan profilin içinde abonelik olmadığında ve hiçbir kapsam belirtilmediğinde), senaryoya anlamlı bir özel durum eklenerek düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-124">Fix isssue where Get-AzureRMRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="b7e09-125">Ayrıca varsayılan parametre kümesi 'RoleDefinitionNameParameterSet' olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="b7e09-125">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="6100---october-2018"></a><span data-ttu-id="b7e09-126">6.10.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="b7e09-126">6.10.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="b7e09-127">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="b7e09-127">Azure.Storage</span></span>
* <span data-ttu-id="b7e09-128">Hedefte meta veri sorunu olduğunda Fix Copy Blob/File meta verileri kopyalamayacak</span><span class="sxs-lookup"><span data-stu-id="b7e09-128">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="b7e09-129">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="b7e09-129">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="b7e09-130">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="b7e09-130">Start-AzureStorageFileCopy</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="b7e09-131">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b7e09-131">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="b7e09-132">Mevcut hesap olmadan Get-AzureRmCognitiveServicesAccountSkus desteği.</span><span class="sxs-lookup"><span data-stu-id="b7e09-132">Support Get-AzureRmCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="b7e09-133">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="b7e09-133">AzureRM.Compute</span></span>
* <span data-ttu-id="b7e09-134">Get-AzureRmVM -ResourceGroupName <rg> gerektiğinde 50'den fazla sonuç döndürecek şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-134">Fix Get-AzureRmVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="b7e09-135">New-AzureRmVmss cmdlet'inin yardımına 'SimpleParameterSet' örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-135">Added an example of the 'SimpleParameterSet' to New-AzureRmVmss cmdlet help.</span></span>
* <span data-ttu-id="b7e09-136">Azure Disk Şifrelemesi ilerleme durumu iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-136">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="b7e09-137">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="b7e09-137">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="b7e09-138">ADF .Net SDK sürümü 2.3.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-138">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="b7e09-139">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="b7e09-139">AzureRM.Network</span></span>
* <span data-ttu-id="b7e09-140">NetworkProfile işlevselliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-140">Added NetworkProfile functionality.</span></span> <span data-ttu-id="b7e09-141">yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-141">new cmdlets added</span></span>
    - <span data-ttu-id="b7e09-142">Get-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b7e09-142">Get-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="b7e09-143">New-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b7e09-143">New-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="b7e09-144">Remove-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b7e09-144">Remove-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="b7e09-145">Set-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b7e09-145">Set-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="b7e09-146">New-AzureRMContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="b7e09-146">New-AzureRMContainerNicConfig</span></span>
    - <span data-ttu-id="b7e09-147">New-AzureRmContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="b7e09-147">New-AzureRmContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="b7e09-148">Alt Ağ Modeline hizmet ilişki bağlantısı eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-148">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="b7e09-149">New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-149">Added cmdlet New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap</span></span>
* <span data-ttu-id="b7e09-150">Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-150">Added cmdlet Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="b7e09-151">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="b7e09-151">AzureRM.RedisCache</span></span>
* <span data-ttu-id="b7e09-152">Bundan sonra Size parametresi olarak her dizeye izin veriliyor.</span><span class="sxs-lookup"><span data-stu-id="b7e09-152">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="b7e09-153">PSArgumentCompleter açılan listesine P5 eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-153">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="b7e09-154">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="b7e09-154">AzureRM.Resources</span></span>
* <span data-ttu-id="b7e09-155">Set-AzureRmPolicyDefinition'a eksik -Mode parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-155">Add missing -Mode parameter to Set-AzureRmPolicyDefinition</span></span>
* <span data-ttu-id="b7e09-156">Origin öğesi User içeren işlemler için Get-AzureRmProviderOperation commandlet hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-156">Fix Get-AzureRmProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="b7e09-157">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="b7e09-157">AzureRM.Sql</span></span>
* <span data-ttu-id="b7e09-158">Bazı yedekleme cmdlet'lerinin geçerli Azure aboneliğini tanıyamamasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-158">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="b7e09-159">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="b7e09-159">AzureRM.Storage</span></span>
* <span data-ttu-id="b7e09-160">Belirli bir konumunun Depolama kaynağı kullanımını alma desteği ve genel Depolama kayrağı kullanımını almak için uyarı iletisi ekleme kullanımdan kalktı.</span><span class="sxs-lookup"><span data-stu-id="b7e09-160">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="b7e09-161">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="b7e09-161">Get-AzureRmStorageUsage</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="b7e09-162">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="b7e09-162">AzureRM.Websites</span></span>
* <span data-ttu-id="b7e09-163">Yeni Get-AzureRMWebAppContainerContinuousDeploymentUrl Cmdlet'i - Kapsayıcı Sürekli Dağıtım Web Kancası URL'sini alıyor</span><span class="sxs-lookup"><span data-stu-id="b7e09-163">New Cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="b7e09-164">Yeni New-AzureRMWebAppContainerPSSession ve Enter-WebAppContainerPSSession Cmdlet'leri - Windows kapsayıcı uygulamasında PowerShell uzak oturumunu başlatıyor</span><span class="sxs-lookup"><span data-stu-id="b7e09-164">New Cmdlets New-AzureRMWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="690---september-2018"></a><span data-ttu-id="b7e09-165">6.9.0 - Eylül 2018</span><span class="sxs-lookup"><span data-stu-id="b7e09-165">6.9.0 - September 2018</span></span>
#### <a name="general"></a><span data-ttu-id="b7e09-166">Genel</span><span class="sxs-lookup"><span data-stu-id="b7e09-166">General</span></span>
* <span data-ttu-id="b7e09-167">AzureRM.SignalR, AzureRM toplu modülüne eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-167">AzureRM.SignalR was added to the AzureRM rollup module</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="b7e09-168">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="b7e09-168">AzureRM.Profile</span></span>
* <span data-ttu-id="b7e09-169">Depolama ortak kodunda küçük değişiklikler yapıldı</span><span class="sxs-lookup"><span data-stu-id="b7e09-169">Minor changes to the storage common code</span></span>
* <span data-ttu-id="b7e09-170">Yardım dosyaları tüm parametre türlerini içerecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-170">Updated help files to include full parameter types.</span></span>
- <span data-ttu-id="b7e09-171">ServicePrincipalCertificateWithSubscriptionId parametre kümesindeki -ServicePrincipal parametresi zorunlu olmaktan çıkarıldı</span><span class="sxs-lookup"><span data-stu-id="b7e09-171">Changed -ServicePrincipal to non-mandatory in the ServicePrincipalCertificateWithSubscriptionId parameter set</span></span> 

#### <a name="azurestorage"></a><span data-ttu-id="b7e09-172">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="b7e09-172">Azure.Storage</span></span>
* <span data-ttu-id="b7e09-173">OAuth ile Depolama Bağlamı oluşturma desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-173">Support create Storage Context with OAuth.</span></span> 
    - <span data-ttu-id="b7e09-174">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="b7e09-174">New-AzureStorageContext</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="b7e09-175">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="b7e09-175">AzureRM.Cdn</span></span>
* <span data-ttu-id="b7e09-176">CDN fiyatlandırma SKU'suna Standard_Microsoft eklendi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-176">Added Standard_Microsoft in Cdn pricing sku.</span></span> 

#### <a name="azurermcompute"></a><span data-ttu-id="b7e09-177">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="b7e09-177">AzureRM.Compute</span></span>
* <span data-ttu-id="b7e09-178">Keyvault ve Storage bağımlılıkları ortak bağımlılıklara taşındı</span><span class="sxs-lookup"><span data-stu-id="b7e09-178">Move dependencies on Keyvault and Storage to the common dependencies</span></span>
* <span data-ttu-id="b7e09-179">AEM cmdlet'lerine daha fazla sanal makine boyutu için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-179">Add support for more virutal machine sizes to AEM cmdlets</span></span>
* <span data-ttu-id="b7e09-180">New-AzureRmVmssIpConfig cmdlet'ine Add PublicIPPrefix parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-180">Add PublicIPPrefix parameter to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="b7e09-181">Invoke-AzureRmVMRunCommand cmdlet'ine ResourceId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-181">Add ResourceId parameter to Invoke-AzureRmVMRunCommand cmdelt</span></span>
* <span data-ttu-id="b7e09-182">Invoke-AzureRmVmssVMRunCommand cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-182">Add Invoke-AzureRmVmssVMRunCommand cmdlet</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="b7e09-183">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="b7e09-183">AzureRM.Dns</span></span>
* <span data-ttu-id="b7e09-184">DNS kaydı oluşturma işlemi sırasında diğer ad kaydı desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-184">Added support for alias record during dns record creation</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="b7e09-185">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="b7e09-185">AzureRM.Insights</span></span>
* <span data-ttu-id="b7e09-186">6833 ve 7102 numaralı sorunlar giderildi (Tanılama Ayarları bölümü)</span><span class="sxs-lookup"><span data-stu-id="b7e09-186">Fixed issues #6833 and #7102 (Diagnostic Settings area)</span></span>
    - <span data-ttu-id="b7e09-187">Tanılama ayarlarını oluşturma ve listeleme/alma sırasında karşılaşılan varsayılan ad 'service' sorunları</span><span class="sxs-lookup"><span data-stu-id="b7e09-187">Issues with the default name, i.e. 'service', during creation and listing/getting of diagnostic settings</span></span>
    - <span data-ttu-id="b7e09-188">Kategoriye sahip tanılama ayarı oluşturma sorunları</span><span class="sxs-lookup"><span data-stu-id="b7e09-188">Issues creating diagnostic settings with categories</span></span>
* <span data-ttu-id="b7e09-189">Ölçümler zaman dilimi parametreleri için kullanımdan kaldırma iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-189">Added deprecation message for metrics time grains parameters</span></span>
    - <span data-ttu-id="b7e09-190">Zaman dilimi parametreleri yine kabul ediliyor (bu bir hataya neden olan değişiklik değil) ancak yalnızca PT1M geçerli olduğu için bu parametreler arka uçta yoksayılıyor</span><span class="sxs-lookup"><span data-stu-id="b7e09-190">Timegrains parameters are still being accepted (this is a non-breaking change,) but they are ignored in the backend since only PT1M is valid</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="b7e09-191">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="b7e09-191">AzureRM.Network</span></span>
* <span data-ttu-id="b7e09-192">LoadBalancer cmdlet'lerinde değişiklikler yapıldı</span><span class="sxs-lookup"><span data-stu-id="b7e09-192">Changes to LoadBalancer cmdlets</span></span>
  - <span data-ttu-id="b7e09-193">LoadBalancerInboundNatPoolConfig: IdleTimeoutInMinutes, EnableFloatingIp ve EnableTcpReset parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-193">LoadBalancerInboundNatPoolConfig: added parameters IdleTimeoutInMinutes, EnableFloatingIp and EnableTcpReset</span></span>
  - <span data-ttu-id="b7e09-194">LoadBalancerInboundNatRuleConfig: EnableTcpReset parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-194">LoadBalancerInboundNatRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="b7e09-195">LoadBalancerRuleConfig: EnableTcpReset parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-195">LoadBalancerRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="b7e09-196">LoadBalancerProbeConfig: Protocol parametresi için "Https" değeri desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-196">LoadBalancerProbeConfig: added support for value "Https" for parameter Protocol</span></span>
* <span data-ttu-id="b7e09-197">Yeni LoadBalancer alt kaynağı OutboundRule için yeni komutlar eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-197">Added new commands for new LoadBalancer's subresource OutboundRule</span></span>
  - <span data-ttu-id="b7e09-198">Add-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b7e09-198">Add-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="b7e09-199">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b7e09-199">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="b7e09-200">New-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b7e09-200">New-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="b7e09-201">Set-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b7e09-201">Set-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="b7e09-202">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b7e09-202">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>
* <span data-ttu-id="b7e09-203">PSNetworkInterface için yeni HostedWorkloads özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-203">Added new HostedWorkloads property for PSNetworkInterface</span></span>
* <span data-ttu-id="b7e09-204">ARM aracılığıyla Azure Güvenlik Duvarı özelliği için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-204">Added new cmdlets for feature: Azure Firewall via ARM</span></span>
  - <span data-ttu-id="b7e09-205">Get-AzureRmFirewall eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-205">Added Get-AzureRmFirewall</span></span>
  - <span data-ttu-id="b7e09-206">Set-AzureRmFirewall eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-206">Added Set-AzureRmFirewall</span></span>
  - <span data-ttu-id="b7e09-207">New-AzureRmFirewall eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-207">Added New-AzureRmFirewall</span></span>
  - <span data-ttu-id="b7e09-208">Remove-AzureRmFirewall eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-208">Added Remove-AzureRmFirewall</span></span>
  - <span data-ttu-id="b7e09-209">New-AzureRmFirewallApplicationRuleCollection eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-209">Added New-AzureRmFirewallApplicationRuleCollection</span></span>
  - <span data-ttu-id="b7e09-210">New-AzureRmFirewallApplicationRule eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-210">Added New-AzureRmFirewallApplicationRule</span></span>
  - <span data-ttu-id="b7e09-211">New-AzureRmFirewallNatRuleCollection eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-211">Added New-AzureRmFirewallNatRuleCollection</span></span>
  - <span data-ttu-id="b7e09-212">New-AzureRmFirewallNatRule eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-212">Added New-AzureRmFirewallNatRule</span></span>
  - <span data-ttu-id="b7e09-213">New-AzureRmFirewallNetworkRuleCollection eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-213">Added New-AzureRmFirewallNetworkRuleCollection</span></span>
  - <span data-ttu-id="b7e09-214">New-AzureRmFirewallNetworkRule eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-214">Added New-AzureRmFirewallNetworkRule</span></span>
* <span data-ttu-id="b7e09-215">Application Gateway'de Güvenilen Kök sertifika ve Otomatik ölçeklendirme yapılandırması desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-215">Added support for Trusted Root certificate and Autoscale configuration in Application Gateway</span></span>
  - <span data-ttu-id="b7e09-216">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="b7e09-216">New Cmdlets added:</span></span>
      - <span data-ttu-id="b7e09-217">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="b7e09-217">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="b7e09-218">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="b7e09-218">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="b7e09-219">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="b7e09-219">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="b7e09-220">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="b7e09-220">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="b7e09-221">Set-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="b7e09-221">Set-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="b7e09-222">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="b7e09-222">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="b7e09-223">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="b7e09-223">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="b7e09-224">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="b7e09-224">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="b7e09-225">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="b7e09-225">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
  - <span data-ttu-id="b7e09-226">Cmdlet'ler isteğe bağlı -TrustedRootCertificate parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-226">Cmdlets updated with optonal parameter -TrustedRootCertificate</span></span>
      - <span data-ttu-id="b7e09-227">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b7e09-227">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="b7e09-228">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b7e09-228">Set-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="b7e09-229">New-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="b7e09-229">New-AzureRmApplicationGatewayBackendHttpSetting</span></span>
      - <span data-ttu-id="b7e09-230">Set-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="b7e09-230">Set-AzureRmApplicationGatewayBackendHttpSetting</span></span>
  - <span data-ttu-id="b7e09-231">Cmdlet'ler isteğe bağlı -AutoscaleConfiguration parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-231">Cmdlets updated with optonal parameter -AutoscaleConfiguration</span></span>
      - <span data-ttu-id="b7e09-232">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b7e09-232">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="b7e09-233">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b7e09-233">Set-AzureRmApplicationGateway</span></span>
* <span data-ttu-id="b7e09-234">Arabirim Uç Noktası için Get-AzureInterfaceEndpoint cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-234">Add cmdlet for Interface Endpoint Get-AzureInterfaceEndpoint</span></span>
* <span data-ttu-id="b7e09-235">Bir alt ağda birden fazla adres ön eki için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-235">Added support for multiple address prefixes in a subnet.</span></span> <span data-ttu-id="b7e09-236">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="b7e09-236">Updated cmdlets:</span></span>
  - <span data-ttu-id="b7e09-237">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b7e09-237">New-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="b7e09-238">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b7e09-238">Set-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="b7e09-239">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b7e09-239">Add-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="b7e09-240">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b7e09-240">Get-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="b7e09-241">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b7e09-241">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>
  - <span data-ttu-id="b7e09-242">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="b7e09-242">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="b7e09-243">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="b7e09-243">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="b7e09-244">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="b7e09-244">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="b7e09-245">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b7e09-245">Add-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="b7e09-246">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b7e09-246">New-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="b7e09-247">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b7e09-247">Set-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="b7e09-248">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="b7e09-248">Add-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="b7e09-249">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="b7e09-249">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="b7e09-250">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="b7e09-250">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="b7e09-251">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="b7e09-251">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="b7e09-252">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b7e09-252">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="b7e09-253">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b7e09-253">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="b7e09-254">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b7e09-254">New-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="b7e09-255">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="b7e09-255">New-AzureRmNetworkInterface</span></span>
* <span data-ttu-id="b7e09-256">Alt ağ temsilcisi seçme cmdlet'leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-256">Adding cmdlets for subnet delegation.</span></span>
  - <span data-ttu-id="b7e09-257">New-AzureRmDelegation: Bir alt ağa eklenebilecek yeni bir temsilci oluşturur</span><span class="sxs-lookup"><span data-stu-id="b7e09-257">New-AzureRmDelegation: Creates a new delegation, which can be added to a subnet</span></span>
  - <span data-ttu-id="b7e09-258">Remove-AzureRmDelegation: Bir alt ağı alır ve belirtilen temsilci adını o alt ağdan kaldırır</span><span class="sxs-lookup"><span data-stu-id="b7e09-258">Remove-AzureRmDelegation: Takes in a subnet and removes the provided delegation name from that subnet</span></span>
  - <span data-ttu-id="b7e09-259">Add-AzureRmDelegation: Bir alt ağı alır ve belirtilen hizmet adını o alt ağa temsilci olarak ekler</span><span class="sxs-lookup"><span data-stu-id="b7e09-259">Add-AzureRmDelegation: Takes in a subnet and adds the provided service name as a delegation to that subnet</span></span>
  - <span data-ttu-id="b7e09-260">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="b7e09-260">Get-AzureRmDelegation</span></span>
  - <span data-ttu-id="b7e09-261">Get-AzureRmAvailableServiceDelegations</span><span class="sxs-lookup"><span data-stu-id="b7e09-261">Get-AzureRmAvailableServiceDelegations</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="b7e09-262">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="b7e09-262">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="b7e09-263">Yönetilen disk desteği</span><span class="sxs-lookup"><span data-stu-id="b7e09-263">Support for managed Managed disk</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="b7e09-264">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="b7e09-264">AzureRM.RedisCache</span></span>
* <span data-ttu-id="b7e09-265">Insights bağımlılığı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-265">Updated Insights dependency.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="b7e09-266">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="b7e09-266">AzureRM.Resources</span></span>
* <span data-ttu-id="b7e09-267">New-AzureRmResourceGroupDeployment cmdlet'i yeni RollbackAction parametresi eklenerek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-267">Update New-AzureRmResourceGroupDeployment with new parameter RollbackAction</span></span>
    - <span data-ttu-id="b7e09-268">Yeni parametreyle OnErrorDeployment desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-268">Add support for OnErrorDeployment with the new parameter.</span></span>
* <span data-ttu-id="b7e09-269">İlke atamalarında yönetilen kimlik desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-269">Support managed identity on policy assignments.</span></span>
* <span data-ttu-id="b7e09-270">Varsayılan değerlere sahip parametrelerin artık 'New-AzureRmPolicyAssignment' ile ilke atama işlemi sırasında belirtilmesi zorunlu değil</span><span class="sxs-lookup"><span data-stu-id="b7e09-270">Parameters with default values are no longer requred when assigning a policy with 'New-AzureRmPolicyAssignment'</span></span>
* <span data-ttu-id="b7e09-271">İlke diğer adlarını almak için yeni Get-AzureRmPolicyAlias cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-271">Add new cmdlet Get-AzureRmPolicyAlias for retrieving policy aliases</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="b7e09-272">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b7e09-272">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="b7e09-273">7161 numaralı sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-273">Fixed issue #7161</span></span>

#### <a name="azurermsignalr"></a><span data-ttu-id="b7e09-274">AzureRM.SignalR</span><span class="sxs-lookup"><span data-stu-id="b7e09-274">AzureRM.SignalR</span></span>
* <span data-ttu-id="b7e09-275">SKU adları Free_F1 ve Standard_S1 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-275">Update SKU names to Free_F1 and Standard_S1</span></span>
* <span data-ttu-id="b7e09-276">PSSignalRResource nesnesine sürüm alanı, PSSignalRKeys nesnesine de bağlantı dizesi eklendi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-276">Add version field to the PSSignalRResource object and connection string to the PSSignalRKeys object.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="b7e09-277">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="b7e09-277">AzureRM.Storage</span></span>
* <span data-ttu-id="b7e09-278">AzureRm.Storage için Değiştirilemezlik İlkesi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-278">Support Immutability Policy in AzureRm.Storage</span></span> 
    - <span data-ttu-id="b7e09-279">Remove-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b7e09-279">Remove-AzureRmStorageAccountNetworkRule</span></span>
    - <span data-ttu-id="b7e09-280">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="b7e09-280">Get-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="b7e09-281">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="b7e09-281">Update-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="b7e09-282">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="b7e09-282">New-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="b7e09-283">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="b7e09-283">Remove-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="b7e09-284">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="b7e09-284">Add-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="b7e09-285">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="b7e09-285">Remove-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="b7e09-286">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="b7e09-286">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="b7e09-287">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="b7e09-287">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="b7e09-288">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="b7e09-288">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="b7e09-289">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="b7e09-289">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="b7e09-290">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="b7e09-290">AzureRM.Websites</span></span>
* <span data-ttu-id="b7e09-291">İki yeni cmdlet eklendi: Get-AzureRmDeletedWebApp ve Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="b7e09-291">Added two new cmdlets: Get-AzureRmDeletedWebApp and Restore-AzureRmDeletedWebApp</span></span>
* <span data-ttu-id="b7e09-292">Windows kapsayıcısı ile App Service planı oluşturmak için New-AzureRmAppServicePlan -HyperV anahtarı eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-292">New-AzureRmAppServicePlan -HyperV switch is added for create app service plan with windows container</span></span>
* <span data-ttu-id="b7e09-293">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - Windows kapsayıcı uygulaması oluşturmak ve yönetmek için yeni parametreler (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-293">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - New parameters (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) added for creating and managing windows container app</span></span>

## <a name="681---august-2018"></a><span data-ttu-id="b7e09-294">6.8.1 - Ağustos 2018</span><span class="sxs-lookup"><span data-stu-id="b7e09-294">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="b7e09-295">Genel</span><span class="sxs-lookup"><span data-stu-id="b7e09-295">General</span></span>
* <span data-ttu-id="b7e09-296">Varsayılan kaynak gruplarının ayarlanmamasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-296">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="b7e09-297">Ortak çalışma zamanı bütünleştirilmiş kodları güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-297">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="b7e09-298">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b7e09-298">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="b7e09-299">Varsayılan kaynak gruplarının ayarlanmamasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-299">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="b7e09-300">https://github.com/Azure/azure-powershell/issues/6603 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-300">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="b7e09-301">Import-AzureRmApiManagementApi ve \*-AzureRmApiManagementCertificate cmdlet’leri artık göreli yolları işleyebiliyor</span><span class="sxs-lookup"><span data-stu-id="b7e09-301">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="b7e09-302">https://github.com/Azure/azure-powershell/issues/6879 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-302">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="b7e09-303">CertificateInformation, Set-AzureRmApiManagement cmdlet’inin düzgün çalışmasını sağlayan, ayarlanabilir bir özelliktir.</span><span class="sxs-lookup"><span data-stu-id="b7e09-303">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="b7e09-304">4.0.4-preview nuget’e yükselterek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-304">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="b7e09-305">https://github.com/Azure/azure-powershell/issues/6853 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-305">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="b7e09-306">Odata filtresi Ürün üzerinde Ada Göre Arama için düzeltildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-306">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="b7e09-307">https://github.com/Azure/azure-powershell/issues/6814 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-307">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="b7e09-308">Odata filtresi API üzerinde Ada Göre Arama için düzeltildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-308">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="b7e09-309">Azure İzleyici günlükçüsüne yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-309">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="b7e09-310">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="b7e09-310">AzureRM.Compute</span></span>
* <span data-ttu-id="b7e09-311">Hata çıktısında hedefin eksik olmasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-311">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="b7e09-312">Yönetilen diske sahip VM için depolama hesabı türüyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-312">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="b7e09-313">Varsayılan kaynak gruplarının ayarlanmamasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-313">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="b7e09-314">Azure Çin gibi diğer ortamlar için AEM Uzantı cmdlet'leri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-314">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="b7e09-315">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="b7e09-315">AzureRM.Network</span></span>
* <span data-ttu-id="b7e09-316">Varsayılan cmdlet çıkış gösterimi, tablo görünümü olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-316">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="b7e09-317">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="b7e09-317">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="b7e09-318">Duraklatılmış kapasite ölçeklendirilmeye çalışılırken Update-AzureRmPowerBIEmbeddedCapacity üzerindeki hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-318">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="b7e09-319">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="b7e09-319">AzureRM.Resources</span></span>
* <span data-ttu-id="b7e09-320">Market’ten yönetilen uygulama oluşturmayla ilgili sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-320">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="b7e09-321">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b7e09-321">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="b7e09-322">Düzeltilen sorunlar</span><span class="sxs-lookup"><span data-stu-id="b7e09-322">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="b7e09-323">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="b7e09-323">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="b7e09-324">Çoklu değer yönlendirme yöntemi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-324">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="b7e09-325">Çoklu değer yönlendirme için yeni 'MaxReturn' parametresi</span><span class="sxs-lookup"><span data-stu-id="b7e09-325">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="b7e09-326">Alt ağ yönlendirme yöntemi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-326">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="b7e09-327">Uç noktalarda IP adresi aralıkları (alt ağları) desteği</span><span class="sxs-lookup"><span data-stu-id="b7e09-327">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="b7e09-328">Profillerde Özel Üst Bilgi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-328">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="b7e09-329">Profillerde Beklenen durum kodu aralığı desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-329">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="b7e09-330">Uç noktalarda Özel Üst Bilgi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-330">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="b7e09-331">6.8.0 - Ağustos 2018</span><span class="sxs-lookup"><span data-stu-id="b7e09-331">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="b7e09-332">Genel</span><span class="sxs-lookup"><span data-stu-id="b7e09-332">General</span></span>
* <span data-ttu-id="b7e09-333">Varsayılan kaynak gruplarının ayarlanmamasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-333">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="b7e09-334">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="b7e09-334">AzureRM.Profile</span></span>
* <span data-ttu-id="b7e09-335">Connect-AzureRmAccount sırasında döndürülen belirteçlere sona erme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-335">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="b7e09-336">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="b7e09-336">AzureRM.Compute</span></span>
* <span data-ttu-id="b7e09-337">Hata çıktısında hedefin eksik olmasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-337">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="b7e09-338">Yönetilen diske sahip VM için depolama hesabı türüyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-338">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="b7e09-339">Azure Çin gibi diğer ortamlar için AEM Uzantı cmdlet'leri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-339">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="b7e09-340">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="b7e09-340">AzureRM.IotHub</span></span>
* <span data-ttu-id="b7e09-341">New-AzureRmIotHubExportDevices ve New-AzureRmIotHubImportDevices için düzeltme örnekleri</span><span class="sxs-lookup"><span data-stu-id="b7e09-341">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="b7e09-342">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="b7e09-342">AzureRM.Network</span></span>
* <span data-ttu-id="b7e09-343">Varsayılan model gösterimi tablo görünümü olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-343">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="b7e09-344">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="b7e09-344">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="b7e09-345">Duraklatılmış kapasite ölçeklendirilmeye çalışılırken Update-AzureRmPowerBIEmbeddedCapacity üzerindeki hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-345">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="b7e09-346">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="b7e09-346">AzureRM.Resources</span></span>
* <span data-ttu-id="b7e09-347">Marketten yönetilen uygulamayla ilgili sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-347">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="b7e09-348">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b7e09-348">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="b7e09-349">Sorunlar için düzeltme</span><span class="sxs-lookup"><span data-stu-id="b7e09-349">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="b7e09-350">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="b7e09-350">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="b7e09-351">Çoklu değer yönlendirme yöntemi desteği</span><span class="sxs-lookup"><span data-stu-id="b7e09-351">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="b7e09-352">Çoklu değer yönlendirme için yeni 'MaxReturn' parametresi</span><span class="sxs-lookup"><span data-stu-id="b7e09-352">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="b7e09-353">Alt ağ yönlendirme yöntemi desteği</span><span class="sxs-lookup"><span data-stu-id="b7e09-353">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="b7e09-354">Uç noktalarda IP adresi aralıkları (alt ağları) desteği</span><span class="sxs-lookup"><span data-stu-id="b7e09-354">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="b7e09-355">Profillerde Özel Üst Bilgi desteği</span><span class="sxs-lookup"><span data-stu-id="b7e09-355">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="b7e09-356">Profillerde Beklenen durum kodu aralığı desteği</span><span class="sxs-lookup"><span data-stu-id="b7e09-356">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="b7e09-357">Uç noktalarda Özel Üst Bilgi desteği</span><span class="sxs-lookup"><span data-stu-id="b7e09-357">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="b7e09-358">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="b7e09-358">AzureRM.Websites</span></span>
* <span data-ttu-id="b7e09-359">Varsayılan kaynak gruplarının yanlış ayarlanmasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-359">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="b7e09-360">6.7.0 - Ağustos 2018</span><span class="sxs-lookup"><span data-stu-id="b7e09-360">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="b7e09-361">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="b7e09-361">AzureRM.Profile</span></span>
* <span data-ttu-id="b7e09-362">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-362">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="b7e09-363">Bağlam çakışmasını önlemek için varsayılan bağlam adına kullanıcı kimliği eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-363">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="b7e09-364">Bağlam #6398 seçerken sorunlara neden olan Clear-AzureRmContext ile ilgili sorunlar giderildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-364">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="b7e09-365">'Connect-AzureRmAccount' için kiracı etki alanının '-TenantId' parametresine geçirilmesi etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-365">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="b7e09-366">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="b7e09-366">Azure.Storage</span></span>
* <span data-ttu-id="b7e09-367">Azure Dosya Paylaşımı kotasındaki 5 TB'lık sınır kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="b7e09-367">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="b7e09-368">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="b7e09-368">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="b7e09-369">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b7e09-369">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="b7e09-370">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-370">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="b7e09-371">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b7e09-371">Azure.AnalysisServices</span></span>
* <span data-ttu-id="b7e09-372">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-372">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="b7e09-373">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b7e09-373">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="b7e09-374">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-374">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="b7e09-375">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="b7e09-375">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="b7e09-376">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-376">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="b7e09-377">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="b7e09-377">AzureRM.Automation</span></span>
* <span data-ttu-id="b7e09-378">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-378">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="b7e09-379">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="b7e09-379">AzureRM.Backup</span></span>
* <span data-ttu-id="b7e09-380">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-380">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="b7e09-381">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="b7e09-381">AzureRM.Batch</span></span>
* <span data-ttu-id="b7e09-382">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-382">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="b7e09-383">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="b7e09-383">AzureRM.Billing</span></span>
* <span data-ttu-id="b7e09-384">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-384">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="b7e09-385">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="b7e09-385">AzureRM.Cdn</span></span>
* <span data-ttu-id="b7e09-386">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-386">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="b7e09-387">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b7e09-387">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="b7e09-388">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-388">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="b7e09-389">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="b7e09-389">AzureRM.Compute</span></span>
* <span data-ttu-id="b7e09-390">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-390">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="b7e09-391">New-AzureRmVmssConfig’e EvictionPolicy parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-391">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="b7e09-392">Hiçbir konum belirtilmediyse New-AzureRmVm’nin DiskFileParameterSet parametresinde varsayılan konum kullanılıyor.</span><span class="sxs-lookup"><span data-stu-id="b7e09-392">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="b7e09-393">Save-AzureRmVMImage cmdlet'inde parametre açıklaması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-393">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="b7e09-394">Singlepass ile ilgili bazı senaryolarda Get-AzureRmVMDiskEncryptionStatus cmdlet’i düzeltildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-394">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="b7e09-395">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="b7e09-395">AzureRM.Consumption</span></span>
* <span data-ttu-id="b7e09-396">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-396">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="b7e09-397">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="b7e09-397">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="b7e09-398">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-398">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="b7e09-399">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="b7e09-399">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="b7e09-400">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-400">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="b7e09-401">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="b7e09-401">AzureRM.DataFactories</span></span>
* <span data-ttu-id="b7e09-402">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-402">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="b7e09-403">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="b7e09-403">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="b7e09-404">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-404">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="b7e09-405">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="b7e09-405">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="b7e09-406">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-406">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="b7e09-407">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b7e09-407">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="b7e09-408">DebugPreference Powershell komut satırından ayarlandığında hata ayıklama düzeltildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-408">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="b7e09-409">Set-AzureRmDataLakeStoreItemAcl örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-409">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="b7e09-410">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-410">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="b7e09-411">Set-AzureRmDataLakeStoreItemAclEntry örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-411">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="b7e09-412">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="b7e09-412">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="b7e09-413">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-413">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="b7e09-414">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="b7e09-414">AzureRM.Dns</span></span>
* <span data-ttu-id="b7e09-415">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-415">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="b7e09-416">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="b7e09-416">AzureRM.EventGrid</span></span>
* <span data-ttu-id="b7e09-417">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-417">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="b7e09-418">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="b7e09-418">AzureRM.EventHub</span></span>
* <span data-ttu-id="b7e09-419">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-419">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="b7e09-420">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="b7e09-420">AzureRM.HDInsight</span></span>
* <span data-ttu-id="b7e09-421">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-421">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="b7e09-422">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="b7e09-422">AzureRM.Insights</span></span>
* <span data-ttu-id="b7e09-423">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-423">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="b7e09-424">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="b7e09-424">AzureRM.IotHub</span></span>
* <span data-ttu-id="b7e09-425">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-425">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="b7e09-426">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b7e09-426">AzureRM.KeyVault</span></span>
* <span data-ttu-id="b7e09-427">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-427">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="b7e09-428">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="b7e09-428">AzureRM.LogicApp</span></span>
* <span data-ttu-id="b7e09-429">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-429">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="b7e09-430">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="b7e09-430">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="b7e09-431">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-431">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="b7e09-432">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="b7e09-432">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="b7e09-433">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-433">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="b7e09-434">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="b7e09-434">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="b7e09-435">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-435">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="b7e09-436">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="b7e09-436">AzureRM.Media</span></span>
* <span data-ttu-id="b7e09-437">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-437">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="b7e09-438">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="b7e09-438">AzureRM.Network</span></span>
* <span data-ttu-id="b7e09-439">Set-AzureRmLocalNetworkGateway örneği eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-439">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="b7e09-440">Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey ve New-AzureRmVirtualNetworkGatewayConnection için örnek ve açıklamalar eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-440">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="b7e09-441">Remove-AzureRmVirtualNetworkGatewayIpConfig ve Reset-AzureRmVirtualNetworkGateway örnekleri eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-441">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="b7e09-442">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey örneği eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-442">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="b7e09-443">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey örneği eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-443">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="b7e09-444">Set-AzureRmVirtualNetworkGatewayConnection örneği eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-444">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="b7e09-445">ApplicationSecurityGroup, RouteTable ve Usage için en son kod oluşturucu kullanılarak cmdlet’ler yeniden oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="b7e09-445">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="b7e09-446">Varolmayan bir alt ağ alma girişiminde bulunulduğunda Get-AzureRmVirtualNetworkSubnetConfig cmdlet'inin hata iletisi netleştirildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-446">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="b7e09-447">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="b7e09-447">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="b7e09-448">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-448">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="b7e09-449">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b7e09-449">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="b7e09-450">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-450">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="b7e09-451">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="b7e09-451">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="b7e09-452">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-452">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="b7e09-453">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="b7e09-453">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="b7e09-454">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-454">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="b7e09-455">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b7e09-455">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="b7e09-456">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-456">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="b7e09-457">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="b7e09-457">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="b7e09-458">Get-AzureRmRecoveryServicesBackItem cmdlet’ine ilke filtresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-458">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="b7e09-459">Komut, verilen ilke kimliği tarafından korunan yedekleme öğelerinin listesini döndürüyor.</span><span class="sxs-lookup"><span data-stu-id="b7e09-459">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="b7e09-460">Microsoft.Azure.Management.RecoveryServices.Backup, sürüm 3.0.0 önizlemesine güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-460">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="b7e09-461">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-461">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="b7e09-462">Restore-AzureRmRecoveryServicesBackupItem’e TargetResourceGroupName parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-462">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="b7e09-463">Yönetilen disklerin geri yüklendiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="b7e09-463">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="b7e09-464">Yönetilen disklerle yapılan VM yedeklemesi için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="b7e09-464">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="b7e09-465">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="b7e09-465">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="b7e09-466">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-466">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="b7e09-467">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="b7e09-467">AzureRM.RedisCache</span></span>
* <span data-ttu-id="b7e09-468">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-468">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="b7e09-469">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="b7e09-469">AzureRM.Relay</span></span>
* <span data-ttu-id="b7e09-470">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-470">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="b7e09-471">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="b7e09-471">AzureRM.Resources</span></span>
* <span data-ttu-id="b7e09-472">Abonelik kapsamındaki şablon dağıtımı destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="b7e09-472">Support template deployment at subscription scope.</span></span> <span data-ttu-id="b7e09-473">Yeni Cmdlet’ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="b7e09-473">Add new Cmdlets:</span></span>
    - <span data-ttu-id="b7e09-474">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="b7e09-474">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="b7e09-475">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="b7e09-475">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="b7e09-476">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="b7e09-476">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="b7e09-477">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="b7e09-477">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="b7e09-478">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="b7e09-478">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="b7e09-479">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="b7e09-479">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="b7e09-480">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="b7e09-480">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="b7e09-481">Set-AzureRmResource’a bağlam geçirilirken hata oluşmasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-481">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="b7e09-482">New-AzureRmResourceGroupDeployment cmdlet'indeki örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-482">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="b7e09-483">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-483">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="b7e09-484">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="b7e09-484">AzureRM.Scheduler</span></span>
* <span data-ttu-id="b7e09-485">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-485">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="b7e09-486">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b7e09-486">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="b7e09-487">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-487">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="b7e09-488">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b7e09-488">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="b7e09-489">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-489">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="b7e09-490">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="b7e09-490">AzureRM.Sql</span></span>
* <span data-ttu-id="b7e09-491">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-491">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="b7e09-492">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="b7e09-492">AzureRM.Storage</span></span>
* <span data-ttu-id="b7e09-493">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-493">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="b7e09-494">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="b7e09-494">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="b7e09-495">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-495">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="b7e09-496">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="b7e09-496">AzureRM.Tags</span></span>
* <span data-ttu-id="b7e09-497">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-497">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="b7e09-498">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="b7e09-498">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="b7e09-499">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-499">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="b7e09-500">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="b7e09-500">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="b7e09-501">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-501">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="b7e09-502">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="b7e09-502">AzureRM.Websites</span></span>
* <span data-ttu-id="b7e09-503">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-503">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="b7e09-504">6.6.0 - Temmuz 2018</span><span class="sxs-lookup"><span data-stu-id="b7e09-504">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="b7e09-505">Genel</span><span class="sxs-lookup"><span data-stu-id="b7e09-505">General</span></span>
* <span data-ttu-id="b7e09-506">Tüm yardım dosyaları tam parametre türleriyle doğru giriş/çıkış türlerini içerecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-506">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="b7e09-507">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="b7e09-507">AzureRM.Profile</span></span>
* <span data-ttu-id="b7e09-508">Kaynağın geçerli yapılandırmasının hedef kaynakla uyumlu olduğunu doğrulayabilmek için Common.Strategy kitaplığı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-508">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="b7e09-509">Common.Storage'a ps1xml türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-509">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="b7e09-510">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="b7e09-510">Azure.Storage</span></span>
* <span data-ttu-id="b7e09-511">DefaultProfile’dan Depolama Bağlamı almak için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-511">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="b7e09-512">Cmdlet'lerin çıkış türü özelliklerine Ps1XmlAttribute eklendi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-512">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="b7e09-513">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b7e09-513">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="b7e09-514">https://github.com/Azure/azure-powershell/issues/6370 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-514">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="b7e09-515">PsApiManagementApi'yi ApiContract'e çevirmek için Automapper hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-515">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="b7e09-516">https://github.com/Azure/azure-powershell/issues/6515 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-516">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="b7e09-517">Kodlama Türü ile aşırı yüklemeyi önlemek için File.Save hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-517">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="b7e09-518">https://github.com/Azure/azure-powershell/issues/6560 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-518">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="b7e09-519">apiId üzerindeki desen özel durumunu düzelten 4.0.3 Nuget sürümüne yükseltildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-519">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="b7e09-520">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="b7e09-520">AzureRM.Compute</span></span>
* <span data-ttu-id="b7e09-521">PremiumLRS depolama hesap türü yeniden adlandırması nedeniyle New-AzureRmVm'de DiskFileParameterSet kullanılarak sanal makine oluşturmanın başarısız olmasıyla ilgili hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-521">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="b7e09-522">Invoke-AzureRmVMRunCommand cmdlet'i düzeltildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-522">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="b7e09-523">Abonelikteki tüm kullanılabilir kümelerin listelenebilmesi için Get-AzureRmAvailabilitySet güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-523">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="b7e09-524">(ResouceGroupName parametresi artık isteğe bağlı.)</span><span class="sxs-lookup"><span data-stu-id="b7e09-524">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="b7e09-525">Uygun sanal makinelerde Hızlandırılmış Ağı etkinleştirmek için 'New-AzureRmVm' cmdlet'inin SimpleParameterSet öğesi güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-525">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="b7e09-526">Kullanıcının belirttiği LB zaten mevcut olduğunda vmss oluşturmanın başarısız olması için New-AzureRmVmss basit parametre kümesi güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-526">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="b7e09-527">New-AzureRmDisk örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-527">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="b7e09-528">'New-AzureRmVM' için örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-528">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="b7e09-529">Set-AzureRmVMOSDisk açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-529">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="b7e09-530">Yazımı ve ön eki düzeltmek amacıyla Set-AzureRmVMBginfoExtension için Örnek 1 güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-530">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="b7e09-531">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="b7e09-531">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="b7e09-532">ADF .Net SDK sürümü 1.1.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-532">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="b7e09-533">Veri fabrikaları arasında paylaşılan şirket içinde barındırılan tümleştirme çalışma zamanı desteği.</span><span class="sxs-lookup"><span data-stu-id="b7e09-533">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="b7e09-534">Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet'ine yeni -SharedIntegrationRuntimeResourceId parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-534">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="b7e09-535">Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet'ine isteğe bağlı yeni -LinkedDataFactoryName parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-535">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="b7e09-536">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b7e09-536">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="b7e09-537">DataPlane SDK'sı (Microsoft.Azure.DataLake.Store) sürümü 1.1.9'a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-537">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="b7e09-538">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="b7e09-538">AzureRM.EventHub</span></span>
* <span data-ttu-id="b7e09-539">Kaldırma cmdlet'lerine InputObject ve ResourceId yöneltmesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-539">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="b7e09-540">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="b7e09-540">AzureRM.Insights</span></span>
* <span data-ttu-id="b7e09-541">Yardım dosyalarındaki OutputType biçimlendirmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-541">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="b7e09-542">Microsoft.Azure.Management.Monitor SDK 0.19.1-preview kullanımı</span><span class="sxs-lookup"><span data-stu-id="b7e09-542">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="b7e09-543">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b7e09-543">AzureRM.KeyVault</span></span>
* <span data-ttu-id="b7e09-544">Set-AzureRmKeyVaultAccessPolicy'de yönlendirme sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-544">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="b7e09-545">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="b7e09-545">AzureRM.Network</span></span>
* <span data-ttu-id="b7e09-546">LoadBalancerInboundNatPoolConfig cmdlet'leri için örnekler eklendi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-546">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="b7e09-547">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="b7e09-547">AzureRM.Resources</span></span>
* <span data-ttu-id="b7e09-548">'Get-AzureRmResource' için hem etiket adı hem de değer sağlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-548">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="b7e09-549">'Set-AzureRmResource' için yönlendirme senaryosu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-549">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="b7e09-550">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b7e09-550">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="b7e09-551">Kaldırma cmdlet'lerine InputObject ve ResourceId yöneltmesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-551">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="b7e09-552">birkaç sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-552">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="b7e09-553">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="b7e09-553">AzureRM.Sql</span></span>
* <span data-ttu-id="b7e09-554">Aşağıdaki cmdlet'lere Sunucu Gelişmiş Tehdit Koruması desteği ekleniyor:</span><span class="sxs-lookup"><span data-stu-id="b7e09-554">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="b7e09-555">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b7e09-555">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="b7e09-556">Aşağıdaki cmdlet'lere Güvenlik Açığı Değerlendirme desteği ekleniyor:</span><span class="sxs-lookup"><span data-stu-id="b7e09-556">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="b7e09-557">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="b7e09-557">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="b7e09-558">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="b7e09-558">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="b7e09-559">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="b7e09-559">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="b7e09-560">Remove-AzureRmSqlServerFirewallRulecmdlet'indeki örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-560">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="b7e09-561">Get-AzureSqlSyncGroupLog içinde ABD temelli olmayan kültürde yanlış tarih saat işlemesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-561">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="b7e09-562">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="b7e09-562">AzureRM.Storage</span></span>
* <span data-ttu-id="b7e09-563">Cmdlet'lerin çıkış türü özelliklerine Ps1XmlAttribute eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-563">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="b7e09-564">Tablo görünümünde StorageAccount cmdlet'i çıkışı gösteriliyor</span><span class="sxs-lookup"><span data-stu-id="b7e09-564">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="b7e09-565">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b7e09-565">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="b7e09-566">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b7e09-566">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="b7e09-567">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b7e09-567">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="b7e09-568">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="b7e09-568">AzureRM.Tags</span></span>
* <span data-ttu-id="b7e09-569">Tag cmdlet'inin yardımında hatayı deyim kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="b7e09-569">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="b7e09-570">6.5.0 - Temmuz 2018</span><span class="sxs-lookup"><span data-stu-id="b7e09-570">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="b7e09-571">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="b7e09-571">AzureRM.Profile</span></span>
* <span data-ttu-id="b7e09-572">'Get-AzureRmContextAutosaveSetting' için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-572">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="b7e09-573">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="b7e09-573">Azure.Storage</span></span>
* <span data-ttu-id="b7e09-574">Salt yazılır Sas belirteciyle Karşıya Yükleme Blobu veya Dosyası desteği</span><span class="sxs-lookup"><span data-stu-id="b7e09-574">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="b7e09-575">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="b7e09-575">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="b7e09-576">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="b7e09-576">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="b7e09-577">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b7e09-577">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="b7e09-578">AS'ye gerekli ResourceGroupName özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-578">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="b7e09-579">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="b7e09-579">AzureRM.Automation</span></span>
* <span data-ttu-id="b7e09-580">'New-AzureRMAutomationSchedule' için yardım güncelleştirildi ve örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-580">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="b7e09-581">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="b7e09-581">AzureRM.Compute</span></span>
* <span data-ttu-id="b7e09-582">Update/New-AzureRmAvailabilitySet komutlarına -Tag parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-582">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="b7e09-583">'Add-AzureRmVmssExtension' için örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-583">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="b7e09-584">'Remove-AzureRmVmssExtension' için örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-584">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="b7e09-585">'Set-AzureRmVMAccessExtension' için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-585">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="b7e09-586">New-AzureRmVmss için SimpleParameterSet güncelleştirilerek SinglePlacementGroup varsayılan olarak false değerine ayarlandı ve kullanıcının tek yerleşim grubunda VMSS oluşturmasına olanak tanıyan 'SinglePlacementGroup' geçiş parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-586">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="b7e09-587">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="b7e09-587">AzureRM.EventHub</span></span>
* <span data-ttu-id="b7e09-588">PSEventHubDRConfigurationAttributes sınıfına, çoğaltma işlemi devam ederken bekleyen çoğaltma işlemlerinin sayısını veren salt okunur 'PendingReplicationOperationsCount' özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-588">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="b7e09-589">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b7e09-589">AzureRM.KeyVault</span></span>
* <span data-ttu-id="b7e09-590">Set-AzureRmKeyVaultAccessPolicy için hata iletisi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-590">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="b7e09-591">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="b7e09-591">AzureRM.LogicApp</span></span>
* <span data-ttu-id="b7e09-592">New-AzureRmLogicApp’te "parametre kümesi çözümlenemedi" hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-592">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="b7e09-593">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="b7e09-593">AzureRM.Network</span></span>
* <span data-ttu-id="b7e09-594">Set/Add-AzureRmVirtualNetworkPeering için birden çok Kiracıdaki Sanal Makineler arasında eşleme etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-594">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="b7e09-595">Aşağıdaki cmdlet’ler Application Gateway için güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-595">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="b7e09-596">New-AzureRmApplicationGateway : EnableFIPS bayrağı ve Zones desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-596">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="b7e09-597">New-AzureRmApplicationGatewaySku : Yeni Standard_v2 ve WAF_v2 sku'ları eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-597">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="b7e09-598">Set-AzureRmApplicationGatewaySku : Yeni Standard_v2 ve WAF_v2 sku'ları eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-598">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="b7e09-599">RouteTable cmdlet’leri en son oluşturucu sürümüyle yeniden oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="b7e09-599">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="b7e09-600">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="b7e09-600">AzureRM.Relay</span></span>
* <span data-ttu-id="b7e09-601">Markdown dosyaları güncelleştirildi, örnekteki parametre adı sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="b7e09-601">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="b7e09-602">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="b7e09-602">AzureRM.Resources</span></span>
* <span data-ttu-id="b7e09-603">Roleassignment ve roledefinition cmdlet’leri güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="b7e09-603">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="b7e09-604">Disk belleğinin parçası olarak yapılan ek roledefinition çağrıları kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="b7e09-604">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="b7e09-605">Get-AzureRmRoleAssignment cmdlet’i düzeltildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-605">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="b7e09-606">-ExpandPrincipalGroups komut parametresi işlevselliği düzeltildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-606">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="b7e09-607">'-ResourceType' parametresinin büyük/küçük harfe duyarlı olduğu 'Get-AzureRmResource' sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-607">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="b7e09-608">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b7e09-608">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="b7e09-609">Liste cmdlet’lerine top ve skip parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-609">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="b7e09-610">Standard'dan Premium NameSpace'e geçiş cmdlet’leri eklendi :</span><span class="sxs-lookup"><span data-stu-id="b7e09-610">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="b7e09-611">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="b7e09-611">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="b7e09-612">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="b7e09-612">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="b7e09-613">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="b7e09-613">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="b7e09-614">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="b7e09-614">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="b7e09-615">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="b7e09-615">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="b7e09-616">PSServiceBusDRConfigurationAttributes sınıfına, çoğaltma işlemi sürerken beklemede olan çoğaltma işlemi sayısını veren salt okunur 'PendingReplicationOperationsCount' özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-616">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="b7e09-617">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b7e09-617">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="b7e09-618">'New-AzureRmServiceFabricCluster' için örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-618">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="b7e09-619">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="b7e09-619">AzureRM.Sql</span></span>
* <span data-ttu-id="b7e09-620">Müşterilerin Sql Server örneğine veya Yönetilen Örneğe TDE Sertifikası ekleyebilmeleri için yeni Management.Sql Cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-620">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="b7e09-621">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="b7e09-621">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="b7e09-622">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="b7e09-622">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="b7e09-623">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="b7e09-623">AzureRM.Websites</span></span>
* <span data-ttu-id="b7e09-624">Artık `Set-AzureRmWebApp -AssignIdentity` ve `Set-AzureRmWebAppSlot -AssignIdentity` false olarak ayarlandığında site object.Removing önizleme etiketinden Identity özelliğini kaldırıyor.</span><span class="sxs-lookup"><span data-stu-id="b7e09-624">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="b7e09-625">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-625">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="b7e09-626">`Set-AzureRmWebApp -PhpVersion` geçerli bir php sürümü off değerini destekliyor</span><span class="sxs-lookup"><span data-stu-id="b7e09-626">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="b7e09-627">6.4.0 - Temmuz 2018</span><span class="sxs-lookup"><span data-stu-id="b7e09-627">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="b7e09-628">Genel</span><span class="sxs-lookup"><span data-stu-id="b7e09-628">General</span></span>
* <span data-ttu-id="b7e09-629">Modüllerin çoğu için yardım dosyalarındaki OutputType biçimlendirmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-629">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="b7e09-630">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="b7e09-630">AzureRM.Profile</span></span>
* <span data-ttu-id="b7e09-631">Temel çıkış türlerine Ps1Xml özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-631">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="b7e09-632">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="b7e09-632">AzureRM.Compute</span></span>
* <span data-ttu-id="b7e09-633">VMSS için IP Etiketi özelliği</span><span class="sxs-lookup"><span data-stu-id="b7e09-633">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="b7e09-634">'New-AzureRmVmssIpTagConfig' cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-634">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="b7e09-635">New-AzureRmVmssIpConfig cmdlet'ine IpTag parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-635">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="b7e09-636">VMSS için Otomatik İşletim Sistemi Geri Alma özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-636">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="b7e09-637">New-AzureRmVmssConfig ve Update-AzureRmVmss cmdlet'lerine DisableAutoRollback parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-637">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="b7e09-638">VMSS için İşletim Sistemi Yükseltme Geçmişi özelliği</span><span class="sxs-lookup"><span data-stu-id="b7e09-638">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="b7e09-639">Get-AzureRmVmss cmdlet'ine OSUpgradeHistory anahtarı parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-639">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="b7e09-640">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="b7e09-640">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="b7e09-641">Aşağıdaki komutlarla Katalog ACL'si için destek eklendi:</span><span class="sxs-lookup"><span data-stu-id="b7e09-641">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="b7e09-642">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="b7e09-642">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="b7e09-643">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="b7e09-643">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="b7e09-644">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="b7e09-644">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="b7e09-645">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b7e09-645">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="b7e09-646">Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry ve Set-AzureRmDataLakeStoreItemAcl için iptal desteği ve ilerleme izleme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-646">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="b7e09-647">Export-AzureRmDataLakeStoreChildItemProperties için iptal desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-647">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="b7e09-648">Özyinelemeli işlemler gerçekleştiren cmdlet'ler için hata ayıklama iletilerinin boşaltılması hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-648">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="b7e09-649">DataLake cmdlet'lerinin test konumu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-649">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="b7e09-650">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="b7e09-650">AzureRM.EventHub</span></span>
* <span data-ttu-id="b7e09-651">Get-AzureRmEventHub ve Get-AzureRmEventHubConsumerGroup Listeleme İşlemleri cmdlet'lerine İsteğe Bağlı MaxCount parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-651">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="b7e09-652">New-AzureRmEventHub cmdlet'inde yeni Olay Hub'ı oluşturma sırasında en az bir parametreye ihtiyaç duyma sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-652">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="b7e09-653">Varsayılan Parametre kümesi sağlandı.</span><span class="sxs-lookup"><span data-stu-id="b7e09-653">Provided Default Parameter set.</span></span>
* <span data-ttu-id="b7e09-654">Kullanıcının New-AzureRmEventHubKey cmdlet'ine KeyValue eklemesini sağlayan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-654">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="b7e09-655">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b7e09-655">AzureRM.KeyVault</span></span>
* <span data-ttu-id="b7e09-656">Get-AzureRmKeyVault -Tag ile tüm kaynakların döndürülmesine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-656">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="b7e09-657">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="b7e09-657">AzureRM.Network</span></span>
* <span data-ttu-id="b7e09-658">Zone-Redundant VirtualNetworkGateways için yeni SKU'lar kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="b7e09-658">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="b7e09-659">ARM aracılığıyla ExpressRoute Partner API'leri özelliği için yeni komutlar eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-659">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="b7e09-660">Get-AzureRmExpressRouteCrossConnection eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-660">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="b7e09-661">Set-AzureRmExpressRouteCrossConnection eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-661">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="b7e09-662">Add-AzureRmExpressRouteCrossConnectionPeering eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-662">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="b7e09-663">Get-AzureRmExpressRouteCrossConnectionPeering eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-663">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="b7e09-664">Remove-AzureRmExpressRouteCrossConnectionPeering eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-664">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="b7e09-665">Get-AzureRMExpressRouteCrossConnectionArpTable eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-665">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="b7e09-666">Get-AzureRMExpressRouteCrossConnectionRouteTable eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-666">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="b7e09-667">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-667">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="b7e09-668">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="b7e09-668">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="b7e09-669">Get-AzureRmRecoveryServicesBackupStatus cmdlet'i eklendi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-669">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="b7e09-670">Bu cmdlet bir sanal makinenin kimliğini alır ve sanal makinenin abonelik içindeki kasaların koruması altında olup olmadığını denetler.</span><span class="sxs-lookup"><span data-stu-id="b7e09-670">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="b7e09-671">Böyle bir kasa varsa cmdlet, bu kasanın ayrıntılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b7e09-671">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="b7e09-672">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="b7e09-672">AzureRM.Resources</span></span>
* <span data-ttu-id="b7e09-673">Get-AzureRmPolicyAssignment cmdlet'leri güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="b7e09-673">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="b7e09-674">Yönetim grubu düzeyinde -Scope değerlerini listeleme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-674">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="b7e09-675">Yönetim grubu düzeyinde -Scope değerlerine sahip olan tek atamaları alma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-675">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="b7e09-676">control parametresine -Effective ve -All anahtarları eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-676">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="b7e09-677">Get/New/Remove/Set-AzureRmPolicyDefinition cmdlet'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-677">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="b7e09-678">Belirli bir yönetim grubuna işlem uygulamayı sağlayan için -ManagementGroupName parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-678">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="b7e09-679">Belirli bir aboneliğe işlem uygulamayı sağlayan Add -SubscriptionId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-679">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="b7e09-680">Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlet'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-680">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="b7e09-681">Belirli bir yönetim grubuna işlem uygulamayı sağlayan -ManagementGroupName parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-681">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="b7e09-682">Belirli bir aboneliğe işlem uygulamayı sağlayan Add -SubscriptionId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-682">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="b7e09-683">'New-AzureRmResourceGroupDeployment' içinde 'TemplateParameterObject' kullanırken parametrelerde KeyVault gizli dizi başvurusu desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-683">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="b7e09-684">'New-AzureRmADAppCredential' için '-EndDate' parametresinin yoksayılmasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-684">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="b7e09-685">'Add-AzureRmADGroupMember' cmdlet'inin istekte bulunmak için yanlış URL'yi kullandığı sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-685">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="b7e09-686">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b7e09-686">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="b7e09-687">Kullanıcının New-AzureRmServiceBusKey cmdlet'ine KeyValue eklemesini sağlayan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-687">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="b7e09-688">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="b7e09-688">AzureRM.Sql</span></span>
* <span data-ttu-id="b7e09-689">New-AzureRmSqlDatabaseRestorePoint yardımında Kullanıcı Tanımlı Geri Yükleme Noktaları netleştirildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-689">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="b7e09-690">Birden fazla cmdlet'te -ComputeGeneration parametresinin belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-690">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="b7e09-691">6.3.0 - Haziran 2018</span><span class="sxs-lookup"><span data-stu-id="b7e09-691">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="b7e09-692">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="b7e09-692">AzureRM.Profile</span></span>
* <span data-ttu-id="b7e09-693">Enable-AzureRmContextAutoSave için hata iletileri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-693">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="b7e09-694">'Connect-AzureRmAccount' cmdlet'i eski bir bağlam olmadan çalıştırıldığında her abonelik için bir bağlam oluşturur</span><span class="sxs-lookup"><span data-stu-id="b7e09-694">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="b7e09-695">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="b7e09-695">Azure.Storage</span></span>
* <span data-ttu-id="b7e09-696">Yardım dosyalarına -Permissions parametresi hakkında daha fazla bilgi eklendi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-696">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="b7e09-697">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="b7e09-697">AzureRM.Compute</span></span>
* <span data-ttu-id="b7e09-698">'Get-AzureRmVmDiskEncryptionStatus' için veri diski bulunmayan VM'lerde karşılaşılan bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-698">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="b7e09-699">Aşağıdaki cmdlet'leri düzeltmek için bilgisayar istemci kitaplığı sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-699">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="b7e09-700">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="b7e09-700">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="b7e09-701">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="b7e09-701">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="b7e09-702">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="b7e09-702">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="b7e09-703">Aşağıdaki cmdlet'ler 'operation ID' ve 'operation status' bilgilerini doğru gösterecek şekilde düzeltildi:</span><span class="sxs-lookup"><span data-stu-id="b7e09-703">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="b7e09-704">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b7e09-704">Start-AzureRmVM</span></span>
    - <span data-ttu-id="b7e09-705">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b7e09-705">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="b7e09-706">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b7e09-706">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="b7e09-707">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b7e09-707">Set-AzureRmVM</span></span>
    - <span data-ttu-id="b7e09-708">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b7e09-708">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="b7e09-709">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b7e09-709">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="b7e09-710">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="b7e09-710">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="b7e09-711">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="b7e09-711">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="b7e09-712">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b7e09-712">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="b7e09-713">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b7e09-713">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="b7e09-714">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b7e09-714">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="b7e09-715">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b7e09-715">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="b7e09-716">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="b7e09-716">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="b7e09-717">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="b7e09-717">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="b7e09-718">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="b7e09-718">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="b7e09-719">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="b7e09-719">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="b7e09-720">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="b7e09-720">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="b7e09-721">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="b7e09-721">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="b7e09-722">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="b7e09-722">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="b7e09-723">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="b7e09-723">AzureRM.EventGrid</span></span>
* <span data-ttu-id="b7e09-724">Gerekli olması halinde parametrelerin boş dizeyle değiştirilmesine izin vermek için Update-AzureRmEventGridSubscription cmdlet'i içindeki SubjectBeginsWith/SubjectEndsWith için ValidateNotNullOrEmpty doğrulama koşulları kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="b7e09-724">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="b7e09-725">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b7e09-725">AzureRM.KeyVault</span></span>
* <span data-ttu-id="b7e09-726">Get-AzureRmKeyVault -Tag çalıştırıldığında etiket döndürülmeme sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-726">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="b7e09-727">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="b7e09-727">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="b7e09-728">Policy Insights cmdlet'leri genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="b7e09-728">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="b7e09-729">API 2018-04-04 sürümünü kullanın</span><span class="sxs-lookup"><span data-stu-id="b7e09-729">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="b7e09-730">PolicyDefinitionReferenceId, Get-AzureRmPolicyStateSummary sonuçlarına eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-730">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="b7e09-731">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="b7e09-731">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="b7e09-732">RecoveryServices.Backup cmdlet'lerine -Vault parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-732">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="b7e09-733">Bu parametre iletildiğinde Set-AzureRmRecoveryServicesContext cmdlet'ini geçersiz kılar.</span><span class="sxs-lookup"><span data-stu-id="b7e09-733">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="b7e09-734">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="b7e09-734">AzureRM.Sql</span></span>
* <span data-ttu-id="b7e09-735">Yardım dosyasındaki Get-AzureRmSqlDatabaseExpanded örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-735">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="b7e09-736">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="b7e09-736">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="b7e09-737">Yardım dosyasındaki Add-AzureRmTrafficManagerEndpointConfig bölümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-737">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="b7e09-738">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="b7e09-738">AzureRM.Websites</span></span>
* <span data-ttu-id="b7e09-739">'Set-AzureRmWebApp', -AssignIdentity kullanıldığında AppSettings verilerini geçersiz kılmayacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-739">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="b7e09-740">'New-AzureRmWebAppSlot', isteğe bağlı parametre olarak AppServicePlan girişini kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-740">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="b7e09-741">6.2.1 - Haziran 2018</span><span class="sxs-lookup"><span data-stu-id="b7e09-741">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="b7e09-742">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b7e09-742">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="b7e09-743">PSWorkspace modeli Network için tür parametresini kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-743">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="b7e09-744">6.2.0 - Haziran 2018</span><span class="sxs-lookup"><span data-stu-id="b7e09-744">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="b7e09-745">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="b7e09-745">AzureRM.Profile</span></span>
* <span data-ttu-id="b7e09-746">Modülün içeri aktarılması sırasında Newtonsoft.Json 10.0.3 sürümünün yüklenmemesine ilişkin sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-746">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="b7e09-747">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="b7e09-747">AzureRM.Compute</span></span>
* <span data-ttu-id="b7e09-748">VMSS VM Güncelleştirme özelliği</span><span class="sxs-lookup"><span data-stu-id="b7e09-748">VMSS VM Update feature</span></span>
    - <span data-ttu-id="b7e09-749">'Update-AzureRmVmssVM' ve 'New-AzureRmVMDataDisk' cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-749">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="b7e09-750">VMSS VM’sine veri diski eklemeyi desteklemek için 'Add-AzureRmVMDataDisk' cmdlet’ine VirtualMachineScaleSetVM parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-750">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="b7e09-751">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="b7e09-751">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="b7e09-752">ADF .Net SDK sürümü, aşağıdaki değişiklikleri içeren 0.8.0-preview sürümüne güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="b7e09-752">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="b7e09-753">Fabrika deposunu yapılandırma işlemi eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-753">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="b7e09-754">QuickBooks LinkedService, consumerKey ve consumerSecret özelliklerini kullanıma sunmak üzere güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-754">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="b7e09-755">SecretBase’ten Object’e birkaç model türü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-755">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="b7e09-756">Blob Etkinliklerini tetikleme eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-756">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="b7e09-757">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b7e09-757">AzureRM.KeyVault</span></span>
* <span data-ttu-id="b7e09-758">Belgeler örnek çıktı ile güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-758">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="b7e09-759">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="b7e09-759">AzureRM.Network</span></span>
* <span data-ttu-id="b7e09-760">Ağ İzleyicisi cmdlet’leri üzerindeki Trafik Analizi parametreleri etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-760">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="b7e09-761">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="b7e09-761">AzureRM.Resources</span></span>
* <span data-ttu-id="b7e09-762">'Get-AzureRmResource' cmdlet’inden döndürülen 'PSResource' nesnesinin 'Properties' özelliğiyle ilgili bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-762">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="b7e09-763">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="b7e09-763">AzureRM.Scheduler</span></span>
* <span data-ttu-id="b7e09-764">Güncelleştirilen ServiceBusQueueJob’ın yeni Kimlik Doğrulaması değerlerini ayarlamamasıyla ilgili bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-764">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="b7e09-765">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="b7e09-765">AzureRM.Sql</span></span>
* <span data-ttu-id="b7e09-766">Şu cmdlet’ler isteğe bağlı LicenseType parametresiyle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="b7e09-766">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="b7e09-767">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b7e09-767">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="b7e09-768">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="b7e09-768">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="b7e09-769">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="b7e09-769">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="b7e09-770">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="b7e09-770">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="b7e09-771">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b7e09-771">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="b7e09-772">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="b7e09-772">AzureRM.Websites</span></span>
* <span data-ttu-id="b7e09-773">'New-AzureRMWebApp' Strategy kütüphanesindeki ortak algoritmaları kullanmak üzere güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-773">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="b7e09-774">6.1.0 - Mayıs 2018</span><span class="sxs-lookup"><span data-stu-id="b7e09-774">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="b7e09-775">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="b7e09-775">AzureRM.Profile</span></span>
* <span data-ttu-id="b7e09-776">'Clear-AzureRmContext' komutunun çalıştırılmasının boş bir bağlamı önceki varsayılan bağlamın adıyla tutmasına ve böylece kullanıcının eski ad ile yeni bir bağlam oluşturamadığı bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-776">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="b7e09-777">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b7e09-777">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="b7e09-778">AS’de Ağ geçidi ilişkilendirme/ilişkilendirme kaldırma işlemlerini etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="b7e09-778">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="b7e09-779">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b7e09-779">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="b7e09-780">ApiVersions, ApiReleases ve ApiRevisions desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-780">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="b7e09-781">ServiceFabric Arka Ucu desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-781">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="b7e09-782">Application Insights Günlükçüsü desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-782">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="b7e09-783">‘Temel’ sku’yu Api Yönetim hizmetinin geçerli sku’su olarak algılama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-783">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="b7e09-784">Özel CA tarafından Kök veya CA olarak yayınlanan Sertifikaları yükleme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-784">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="b7e09-785">Özel SSL sertifikalarını KeyVault ve Çoklu ara sunucu ana bilgisayar adlarıyla kabul etme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-785">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="b7e09-786">MSI kimliği desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-786">Added support for MSI identity</span></span>
* <span data-ttu-id="b7e09-787">İlkeleri Url ile kabul etme desteği eklendi NOT: Aşağıdaki cmdlet’ler gelecekteki sürümlerde kullanım dışı kalacaktır</span><span class="sxs-lookup"><span data-stu-id="b7e09-787">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="b7e09-788">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="b7e09-788">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="b7e09-789">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="b7e09-789">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="b7e09-790">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="b7e09-790">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="b7e09-791">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="b7e09-791">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="b7e09-792">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="b7e09-792">AzureRM.Batch</span></span>
* <span data-ttu-id="b7e09-793">Yeni Get-AzureBatchPoolNodeCounts cmdlet’ini yayınlama</span><span class="sxs-lookup"><span data-stu-id="b7e09-793">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="b7e09-794">Yeni AzureBatchComputeNodeServiceLogUpload cmdlet’ini yayınlama</span><span class="sxs-lookup"><span data-stu-id="b7e09-794">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="b7e09-795">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="b7e09-795">AzureRM.Consumption</span></span>
* <span data-ttu-id="b7e09-796">Get-AzureRmConsumptionUsageDetail cmdlet’inde yeni Expand, ResourceGroup, InstanceName, InstanceId, Tags ve Top parametrelerini ekleme</span><span class="sxs-lookup"><span data-stu-id="b7e09-796">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="b7e09-797">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b7e09-797">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="b7e09-798">Export-AzureRmDataLakeStoreChildItemProperties için düzeltme örneği</span><span class="sxs-lookup"><span data-stu-id="b7e09-798">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="b7e09-799">Set-AzureRmDataLakeStoreItemAclEntry komutunda Özyineleme durumu için null parametresi özel durumunu düzeltme</span><span class="sxs-lookup"><span data-stu-id="b7e09-799">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="b7e09-800">Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry’ye yönelik yardım dosyalarını düzeltme</span><span class="sxs-lookup"><span data-stu-id="b7e09-800">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="b7e09-801">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="b7e09-801">AzureRM.Network</span></span>
* <span data-ttu-id="b7e09-802">Ağ SDK sürümünü 18.0.0-önizleme’den 19.0.0-önizlemeye yükseltme</span><span class="sxs-lookup"><span data-stu-id="b7e09-802">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="b7e09-803">Protokol yapılandırması oluşturma cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-803">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="b7e09-804">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="b7e09-804">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="b7e09-805">Varolan express route bağlantı hattına yeni bir bağlantı hattı ekleme cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-805">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="b7e09-806">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="b7e09-806">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="b7e09-807">Varolan express route bağlantı hattındaki bir bağlantı hattı bağlantısını kaldırma cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-807">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="b7e09-808">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="b7e09-808">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="b7e09-809">Bağlantı hattı bağlantısı alma cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="b7e09-809">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="b7e09-810">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="b7e09-810">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="b7e09-811">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b7e09-811">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="b7e09-812">Oluşturulan sertifikalarla sunucu kimlik doğrulaması kullanımı düzeltildi (Sorun No. 5998)</span><span class="sxs-lookup"><span data-stu-id="b7e09-812">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="b7e09-813">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="b7e09-813">AzureRM.Sql</span></span>
* <span data-ttu-id="b7e09-814">AuditActions veya AuditActionGroups’un kaldırılmasını sağlamak üzere Denetim cmdlet’leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="b7e09-814">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="b7e09-815">Yeni bir esnek saklama ilkesi ayarlarken komutun ‘Azure kurtarma hizmeti kasası ve ilkesiyle uzun süreli saklama ilkesini yapılandırma artık desteklenmiyor. Lütfen yeni esnek saklama ilkesi ile istek gönderin’ hatasını verdiği Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b7e09-815">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="b7e09-816">komutuna ilişkin sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="b7e09-816">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="b7e09-817">Ölçek ve katman ilişkili özelliklere yönelik Sku özelliğini destekleyen yeni Veritabanı API’sini kullanmak için tüm Azure Sql Database/ElasticPool Creation/Update cmdlet’lerini güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="b7e09-817">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="b7e09-818">Güncelleştirilen cmlet’ler arasında şunlar yer almaktadır:</span><span class="sxs-lookup"><span data-stu-id="b7e09-818">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="b7e09-819">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b7e09-819">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="b7e09-820">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="b7e09-820">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="b7e09-821">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="b7e09-821">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="b7e09-822">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="b7e09-822">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="b7e09-823">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b7e09-823">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="b7e09-824">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="b7e09-824">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="b7e09-825">-Name parametresini kullanırken -ResourceGroupName parametresinin gerekli olması için 'Get-AzureRmTrafficManagerProfile'a yönelik parametreleri güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="b7e09-825">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>