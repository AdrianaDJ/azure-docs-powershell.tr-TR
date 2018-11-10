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
ms.openlocfilehash: 8a7b184ed06eb078956229fa67d02840014e3aaf
ms.sourcegitcommit: ac4b53bb42a25aae013a9d8cd9ae98ada9397274
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/08/2018
ms.locfileid: "51275529"
---
# <a name="release-notes"></a><span data-ttu-id="aaa79-103">Sürüm notları</span><span class="sxs-lookup"><span data-stu-id="aaa79-103">Release notes</span></span>

<span data-ttu-id="aaa79-104">Azure PowerShell'in bu sürümünde yapılan değişikliklerin listesi aşağıda verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="aaa79-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="6120---november-2018"></a><span data-ttu-id="aaa79-105">6.12.0 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="aaa79-105">6.12.0 - November 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="aaa79-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="aaa79-106">AzureRM.Profile</span></span>
* <span data-ttu-id="aaa79-107">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-107">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="aaa79-108">Connect-AzureRmAccount cmdlet'indeki TenantId parametresi Tenant olarak yeniden adlandırıldı ve TenantId için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-108">Rename param TenantId in cmdlet Connect-AzureRmAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="aaa79-109">Connect-AzureRmAccount için TenantId açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-109">Updated TenantId description for Connect-AzureRmAccount</span></span>
* <span data-ttu-id="aaa79-110">Kiracı etki alanı sağlanırken başarısız oturum açma durumunda gösterilen hata iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-110">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="aaa79-111">Kiracıda abonelikleri olmayan hesaplar için bağlam adı çakışmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-111">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="aaa79-112">MSI kullanırken DataLake uç noktalarıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-112">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="aaa79-113">Bağlantı olmadığında 'Disconnect-AzureRmAccount' oluşturulmasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-113">Fix issue where 'Disconnect-AzureRmAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azurermautomation"></a><span data-ttu-id="aaa79-114">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="aaa79-114">AzureRM.Automation</span></span>
* <span data-ttu-id="aaa79-115">Cmdlet DLL dosya adı Microsoft.Azure.Commands.Automation.dll olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-115">Renamed cmdlet DLL filename to Microsoft.Azure.Commands.Automation.dll</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="aaa79-116">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="aaa79-116">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="aaa79-117">Get-AzureRmCognitiveServicesAccountSkus işlemi eklendi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-117">Add Get-AzureRmCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="aaa79-118">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="aaa79-118">AzureRM.Compute</span></span>
* <span data-ttu-id="aaa79-119">Add-AzureRmVmssVMDataDisk ve Remove-AzureRmVmssVMDataDisk cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-119">Add Add-AzureRmVmssVMDataDisk and Remove-AzureRmVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="aaa79-120">Get-AzureRmVMImage, AutomaticOSUpgradeProperties gösteriyor</span><span class="sxs-lookup"><span data-stu-id="aaa79-120">Get-AzureRmVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="aaa79-121">Json biçiminde SetAzureRmVMChefExtension -BootstrapOptions ve -JsonAttribute seçeneği değerlerinin ayarlanmamasıyla ilgili hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-121">Fixed SetAzureRmVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="aaa79-122">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="aaa79-122">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="aaa79-123">DataLake paketi 1.1.10'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-123">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="aaa79-124">Çok iş parçacıklı işlemlere varsayılan Concurrency değeri eklendi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-124">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="aaa79-125">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="aaa79-125">AzureRM.Insights</span></span>
* <span data-ttu-id="aaa79-126">7267 numaralı (Otomatik ölçeklendirme alanı) sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-126">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="aaa79-127">Yeni otomatik ölçeklendirme kuralı oluşturma sırasında numaralandırılmış parametrelerin düzgün ayarlanmamasıyla ilgili sorunlar (bunlar her zaman varsayılan değere ayarlanıyordu).</span><span class="sxs-lookup"><span data-stu-id="aaa79-127">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="aaa79-128">Set-AzureRMDiagnosticSetting'in ayar oluşturma sırasında kategorilerin açıkça belirtilmesini gerektirmesiyle ilgili 7513 numaralı [Insights] sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-128">Fixed issue #7513 [Insights] Set-AzureRMDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="aaa79-129">Artık cmdlet oluşturma sırasında açık kategori gösteriminin etkinleştirilmesini gerektirmiyor; başka bir deyişle belgelerinde belirtildiği gibi çalışıyor</span><span class="sxs-lookup"><span data-stu-id="aaa79-129">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="aaa79-130">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="aaa79-130">AzureRM.Network</span></span>
* <span data-ttu-id="aaa79-131">Aşağıdaki parametrelerde PeeringType parametresi zorunlu parametre olarak değiştirildi:-</span><span class="sxs-lookup"><span data-stu-id="aaa79-131">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="aaa79-132">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="aaa79-132">Get-AzureRmExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="aaa79-133">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="aaa79-133">Get-AzureRmExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="aaa79-134">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="aaa79-134">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="aaa79-135">Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="aaa79-135">Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="aaa79-136">Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="aaa79-136">Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="aaa79-137">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="aaa79-137">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="aaa79-138">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="aaa79-138">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="aaa79-139">İlke düzeltme cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-139">Added policy remediation cmdlets</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="aaa79-140">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="aaa79-140">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="aaa79-141">Kurtarma hizmetlerinde Azure dosya paylaşımları için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-141">Added support for azure file shares in recovery services.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="aaa79-142">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="aaa79-142">AzureRM.Resources</span></span>
* <span data-ttu-id="aaa79-143">https://github.com/Azure/azure-powershell/issues/7402 düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="aaa79-143">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="aaa79-144">'Get-AzureRmResource' için '-ResourceId' parametresi kullanılarak kaynakların listelenmesine olanak tanındı</span><span class="sxs-lookup"><span data-stu-id="aaa79-144">Allow listing resources using the '-ResourceId' parameter for 'Get-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="aaa79-145">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="aaa79-145">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="aaa79-146">PSServiceBusMigrationConfigurationAttributes'e Geçiş durumunun bilinmesine yardımcı olacak salt okunur MigrationState özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-146">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="aaa79-147">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="aaa79-147">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="aaa79-148">Linux Vmss'ye sertifika ekleme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-148">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="aaa79-149">'Add-AzureRmServiceFabricClusterCertificate' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-149">Fix 'Add-AzureRmServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="aaa79-150">Yeni sertifikadan doğru parmak izi kullanıyor (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="aaa79-150">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="aaa79-151">Özel durum doğru görüntüleniyor (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="aaa79-151">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="aaa79-152">'Update-AzureRmServiceFabricDurability', Vmss CreateOrUpdate işlemini başlatmadan önce küme yapılandırmasını güncelleştirecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-152">Fix 'Update-AzureRmServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="6110---october-2018"></a><span data-ttu-id="aaa79-153">6.11.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="aaa79-153">6.11.0 - October 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="aaa79-154">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="aaa79-154">AzureRM.Profile</span></span>
* <span data-ttu-id="aaa79-155">CloudShell’de Get-AzureRmSubscription sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="aaa79-155">Fix issue with Get-AzureRmSubscription in CloudShell</span></span>
* <span data-ttu-id="aaa79-156">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-156">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="aaa79-157">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="aaa79-157">AzureRM.Backup</span></span>
* <span data-ttu-id="aaa79-158">Azure Backup cmdlet’leri kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="aaa79-158">Deprecated Azure Backup cmdlets.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="aaa79-159">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="aaa79-159">AzureRM.Compute</span></span>
* <span data-ttu-id="aaa79-160">'New-AzureRmVm' için basit parametre kümesi kullanıldığında hızlandırılmış ağların açılacağı VM boyutları beyaz listesine yeni boyutlar eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-160">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzureRmVm'</span></span>
* <span data-ttu-id="aaa79-161">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-161">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="aaa79-162">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="aaa79-162">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="aaa79-163">Sanal Ağ Kuralları desteği ekleme</span><span class="sxs-lookup"><span data-stu-id="aaa79-163">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="aaa79-164">Get-AzureRmDataLakeStoreVirtualNetworkRule: Azure Data Lake Store sanal ağ kuralını alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="aaa79-164">Get-AzureRmDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="aaa79-165">Add-AzureRmDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabına sanal ağ kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="aaa79-165">Add-AzureRmDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="aaa79-166">Set-AzureRmDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabında belirtilen sanal ağ kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="aaa79-166">Set-AzureRmDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="aaa79-167">Remove-AzureRmDataLakeStoreVirtualNetworkRule: Azure Data Lake Store sanal ağ kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="aaa79-167">Remove-AzureRmDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="aaa79-168">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="aaa79-168">AzureRM.Network</span></span>
* <span data-ttu-id="aaa79-169">Test-AzureRmNetworkWatcherConnectivity cmdlet'i güncelleştirildi, arka uca protokol değerini geçiriyor.</span><span class="sxs-lookup"><span data-stu-id="aaa79-169">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="aaa79-170">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-170">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="aaa79-171">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="aaa79-171">AzureRM.Resources</span></span>
* <span data-ttu-id="aaa79-172">Get-AzureRMRoleDefinition cmdlet'inin anlaşılmaz bir özel durum oluşturmasına neden olan hata (varsayılan profilin içinde abonelik olmadığında ve hiçbir kapsam belirtilmediğinde), senaryoya anlamlı bir özel durum eklenerek düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-172">Fix isssue where Get-AzureRMRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="aaa79-173">Ayrıca varsayılan parametre kümesi 'RoleDefinitionNameParameterSet' olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="aaa79-173">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="6100---october-2018"></a><span data-ttu-id="aaa79-174">6.10.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="aaa79-174">6.10.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="aaa79-175">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="aaa79-175">Azure.Storage</span></span>
* <span data-ttu-id="aaa79-176">Hedefte meta veri sorunu olduğunda Fix Copy Blob/File meta verileri kopyalamayacak</span><span class="sxs-lookup"><span data-stu-id="aaa79-176">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="aaa79-177">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="aaa79-177">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="aaa79-178">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="aaa79-178">Start-AzureStorageFileCopy</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="aaa79-179">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="aaa79-179">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="aaa79-180">Mevcut hesap olmadan Get-AzureRmCognitiveServicesAccountSkus desteği.</span><span class="sxs-lookup"><span data-stu-id="aaa79-180">Support Get-AzureRmCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="aaa79-181">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="aaa79-181">AzureRM.Compute</span></span>
* <span data-ttu-id="aaa79-182">Get-AzureRmVM -ResourceGroupName <rg> gerektiğinde 50'den fazla sonuç döndürecek şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-182">Fix Get-AzureRmVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="aaa79-183">New-AzureRmVmss cmdlet'inin yardımına 'SimpleParameterSet' örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-183">Added an example of the 'SimpleParameterSet' to New-AzureRmVmss cmdlet help.</span></span>
* <span data-ttu-id="aaa79-184">Azure Disk Şifrelemesi ilerleme durumu iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-184">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="aaa79-185">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="aaa79-185">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="aaa79-186">ADF .Net SDK sürümü 2.3.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-186">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="aaa79-187">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="aaa79-187">AzureRM.Network</span></span>
* <span data-ttu-id="aaa79-188">NetworkProfile işlevselliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-188">Added NetworkProfile functionality.</span></span> <span data-ttu-id="aaa79-189">yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-189">new cmdlets added</span></span>
    - <span data-ttu-id="aaa79-190">Get-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="aaa79-190">Get-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="aaa79-191">New-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="aaa79-191">New-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="aaa79-192">Remove-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="aaa79-192">Remove-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="aaa79-193">Set-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="aaa79-193">Set-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="aaa79-194">New-AzureRMContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="aaa79-194">New-AzureRMContainerNicConfig</span></span>
    - <span data-ttu-id="aaa79-195">New-AzureRmContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="aaa79-195">New-AzureRmContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="aaa79-196">Alt Ağ Modeline hizmet ilişki bağlantısı eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-196">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="aaa79-197">New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-197">Added cmdlet New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap</span></span>
* <span data-ttu-id="aaa79-198">Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-198">Added cmdlet Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="aaa79-199">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="aaa79-199">AzureRM.RedisCache</span></span>
* <span data-ttu-id="aaa79-200">Bundan sonra Size parametresi olarak her dizeye izin veriliyor.</span><span class="sxs-lookup"><span data-stu-id="aaa79-200">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="aaa79-201">PSArgumentCompleter açılan listesine P5 eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-201">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="aaa79-202">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="aaa79-202">AzureRM.Resources</span></span>
* <span data-ttu-id="aaa79-203">Set-AzureRmPolicyDefinition'a eksik -Mode parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-203">Add missing -Mode parameter to Set-AzureRmPolicyDefinition</span></span>
* <span data-ttu-id="aaa79-204">Origin öğesi User içeren işlemler için Get-AzureRmProviderOperation commandlet hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-204">Fix Get-AzureRmProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="aaa79-205">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="aaa79-205">AzureRM.Sql</span></span>
* <span data-ttu-id="aaa79-206">Bazı yedekleme cmdlet'lerinin geçerli Azure aboneliğini tanıyamamasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-206">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="aaa79-207">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="aaa79-207">AzureRM.Storage</span></span>
* <span data-ttu-id="aaa79-208">Belirli bir konumunun Depolama kaynağı kullanımını alma desteği ve genel Depolama kayrağı kullanımını almak için uyarı iletisi ekleme kullanımdan kalktı.</span><span class="sxs-lookup"><span data-stu-id="aaa79-208">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="aaa79-209">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="aaa79-209">Get-AzureRmStorageUsage</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="aaa79-210">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="aaa79-210">AzureRM.Websites</span></span>
* <span data-ttu-id="aaa79-211">Yeni Get-AzureRMWebAppContainerContinuousDeploymentUrl Cmdlet'i - Kapsayıcı Sürekli Dağıtım Web Kancası URL'sini alıyor</span><span class="sxs-lookup"><span data-stu-id="aaa79-211">New Cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="aaa79-212">Yeni New-AzureRMWebAppContainerPSSession ve Enter-WebAppContainerPSSession Cmdlet'leri - Windows kapsayıcı uygulamasında PowerShell uzak oturumunu başlatıyor</span><span class="sxs-lookup"><span data-stu-id="aaa79-212">New Cmdlets New-AzureRMWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="690---september-2018"></a><span data-ttu-id="aaa79-213">6.9.0 - Eylül 2018</span><span class="sxs-lookup"><span data-stu-id="aaa79-213">6.9.0 - September 2018</span></span>
#### <a name="general"></a><span data-ttu-id="aaa79-214">Genel</span><span class="sxs-lookup"><span data-stu-id="aaa79-214">General</span></span>
* <span data-ttu-id="aaa79-215">AzureRM.SignalR, AzureRM toplu modülüne eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-215">AzureRM.SignalR was added to the AzureRM rollup module</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="aaa79-216">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="aaa79-216">AzureRM.Profile</span></span>
* <span data-ttu-id="aaa79-217">Depolama ortak kodunda küçük değişiklikler yapıldı</span><span class="sxs-lookup"><span data-stu-id="aaa79-217">Minor changes to the storage common code</span></span>
* <span data-ttu-id="aaa79-218">Yardım dosyaları tüm parametre türlerini içerecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-218">Updated help files to include full parameter types.</span></span>
* <span data-ttu-id="aaa79-219">ServicePrincipalCertificateWithSubscriptionId parametre kümesindeki -ServicePrincipal parametresi zorunlu olmaktan çıkarıldı</span><span class="sxs-lookup"><span data-stu-id="aaa79-219">Changed -ServicePrincipal to non-mandatory in the ServicePrincipalCertificateWithSubscriptionId parameter set</span></span> 

#### <a name="azurestorage"></a><span data-ttu-id="aaa79-220">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="aaa79-220">Azure.Storage</span></span>
* <span data-ttu-id="aaa79-221">OAuth ile Depolama Bağlamı oluşturma desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-221">Support create Storage Context with OAuth.</span></span> 
    - <span data-ttu-id="aaa79-222">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="aaa79-222">New-AzureStorageContext</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="aaa79-223">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="aaa79-223">AzureRM.Cdn</span></span>
* <span data-ttu-id="aaa79-224">CDN fiyatlandırma SKU'suna Standard_Microsoft eklendi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-224">Added Standard_Microsoft in Cdn pricing sku.</span></span> 

#### <a name="azurermcompute"></a><span data-ttu-id="aaa79-225">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="aaa79-225">AzureRM.Compute</span></span>
* <span data-ttu-id="aaa79-226">Keyvault ve Storage bağımlılıkları ortak bağımlılıklara taşındı</span><span class="sxs-lookup"><span data-stu-id="aaa79-226">Move dependencies on Keyvault and Storage to the common dependencies</span></span>
* <span data-ttu-id="aaa79-227">AEM cmdlet'lerine daha fazla sanal makine boyutu için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-227">Add support for more virutal machine sizes to AEM cmdlets</span></span>
* <span data-ttu-id="aaa79-228">New-AzureRmVmssIpConfig cmdlet'ine Add PublicIPPrefix parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-228">Add PublicIPPrefix parameter to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="aaa79-229">Invoke-AzureRmVMRunCommand cmdlet'ine ResourceId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-229">Add ResourceId parameter to Invoke-AzureRmVMRunCommand cmdelt</span></span>
* <span data-ttu-id="aaa79-230">Invoke-AzureRmVmssVMRunCommand cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-230">Add Invoke-AzureRmVmssVMRunCommand cmdlet</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="aaa79-231">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="aaa79-231">AzureRM.Dns</span></span>
* <span data-ttu-id="aaa79-232">DNS kaydı oluşturma işlemi sırasında diğer ad kaydı desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-232">Added support for alias record during dns record creation</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="aaa79-233">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="aaa79-233">AzureRM.Insights</span></span>
* <span data-ttu-id="aaa79-234">6833 ve 7102 numaralı sorunlar giderildi (Tanılama Ayarları bölümü)</span><span class="sxs-lookup"><span data-stu-id="aaa79-234">Fixed issues #6833 and #7102 (Diagnostic Settings area)</span></span>
    - <span data-ttu-id="aaa79-235">Tanılama ayarlarını oluşturma ve listeleme/alma sırasında karşılaşılan varsayılan ad 'service' sorunları</span><span class="sxs-lookup"><span data-stu-id="aaa79-235">Issues with the default name, i.e. 'service', during creation and listing/getting of diagnostic settings</span></span>
    - <span data-ttu-id="aaa79-236">Kategoriye sahip tanılama ayarı oluşturma sorunları</span><span class="sxs-lookup"><span data-stu-id="aaa79-236">Issues creating diagnostic settings with categories</span></span>
* <span data-ttu-id="aaa79-237">Ölçümler zaman dilimi parametreleri için kullanımdan kaldırma iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-237">Added deprecation message for metrics time grains parameters</span></span>
    - <span data-ttu-id="aaa79-238">Zaman dilimi parametreleri yine kabul ediliyor (bu bir hataya neden olan değişiklik değil) ancak yalnızca PT1M geçerli olduğu için bu parametreler arka uçta yoksayılıyor</span><span class="sxs-lookup"><span data-stu-id="aaa79-238">Timegrains parameters are still being accepted (this is a non-breaking change,) but they are ignored in the backend since only PT1M is valid</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="aaa79-239">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="aaa79-239">AzureRM.Network</span></span>
* <span data-ttu-id="aaa79-240">LoadBalancer cmdlet'lerinde değişiklikler yapıldı</span><span class="sxs-lookup"><span data-stu-id="aaa79-240">Changes to LoadBalancer cmdlets</span></span>
  - <span data-ttu-id="aaa79-241">LoadBalancerInboundNatPoolConfig: IdleTimeoutInMinutes, EnableFloatingIp ve EnableTcpReset parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-241">LoadBalancerInboundNatPoolConfig: added parameters IdleTimeoutInMinutes, EnableFloatingIp and EnableTcpReset</span></span>
  - <span data-ttu-id="aaa79-242">LoadBalancerInboundNatRuleConfig: EnableTcpReset parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-242">LoadBalancerInboundNatRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="aaa79-243">LoadBalancerRuleConfig: EnableTcpReset parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-243">LoadBalancerRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="aaa79-244">LoadBalancerProbeConfig: Protocol parametresi için "Https" değeri desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-244">LoadBalancerProbeConfig: added support for value "Https" for parameter Protocol</span></span>
* <span data-ttu-id="aaa79-245">Yeni LoadBalancer alt kaynağı OutboundRule için yeni komutlar eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-245">Added new commands for new LoadBalancer's subresource OutboundRule</span></span>
  - <span data-ttu-id="aaa79-246">Add-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="aaa79-246">Add-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="aaa79-247">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="aaa79-247">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="aaa79-248">New-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="aaa79-248">New-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="aaa79-249">Set-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="aaa79-249">Set-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="aaa79-250">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="aaa79-250">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>
* <span data-ttu-id="aaa79-251">PSNetworkInterface için yeni HostedWorkloads özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-251">Added new HostedWorkloads property for PSNetworkInterface</span></span>
* <span data-ttu-id="aaa79-252">ARM aracılığıyla Azure Güvenlik Duvarı özelliği için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-252">Added new cmdlets for feature: Azure Firewall via ARM</span></span>
  - <span data-ttu-id="aaa79-253">Get-AzureRmFirewall eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-253">Added Get-AzureRmFirewall</span></span>
  - <span data-ttu-id="aaa79-254">Set-AzureRmFirewall eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-254">Added Set-AzureRmFirewall</span></span>
  - <span data-ttu-id="aaa79-255">New-AzureRmFirewall eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-255">Added New-AzureRmFirewall</span></span>
  - <span data-ttu-id="aaa79-256">Remove-AzureRmFirewall eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-256">Added Remove-AzureRmFirewall</span></span>
  - <span data-ttu-id="aaa79-257">New-AzureRmFirewallApplicationRuleCollection eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-257">Added New-AzureRmFirewallApplicationRuleCollection</span></span>
  - <span data-ttu-id="aaa79-258">New-AzureRmFirewallApplicationRule eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-258">Added New-AzureRmFirewallApplicationRule</span></span>
  - <span data-ttu-id="aaa79-259">New-AzureRmFirewallNatRuleCollection eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-259">Added New-AzureRmFirewallNatRuleCollection</span></span>
  - <span data-ttu-id="aaa79-260">New-AzureRmFirewallNatRule eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-260">Added New-AzureRmFirewallNatRule</span></span>
  - <span data-ttu-id="aaa79-261">New-AzureRmFirewallNetworkRuleCollection eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-261">Added New-AzureRmFirewallNetworkRuleCollection</span></span>
  - <span data-ttu-id="aaa79-262">New-AzureRmFirewallNetworkRule eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-262">Added New-AzureRmFirewallNetworkRule</span></span>
* <span data-ttu-id="aaa79-263">Application Gateway'de Güvenilen Kök sertifika ve Otomatik ölçeklendirme yapılandırması desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-263">Added support for Trusted Root certificate and Autoscale configuration in Application Gateway</span></span>
  - <span data-ttu-id="aaa79-264">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="aaa79-264">New Cmdlets added:</span></span>
      - <span data-ttu-id="aaa79-265">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="aaa79-265">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="aaa79-266">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="aaa79-266">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="aaa79-267">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="aaa79-267">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="aaa79-268">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="aaa79-268">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="aaa79-269">Set-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="aaa79-269">Set-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="aaa79-270">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="aaa79-270">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="aaa79-271">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="aaa79-271">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="aaa79-272">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="aaa79-272">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="aaa79-273">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="aaa79-273">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
  - <span data-ttu-id="aaa79-274">Cmdlet'ler isteğe bağlı -TrustedRootCertificate parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-274">Cmdlets updated with optonal parameter -TrustedRootCertificate</span></span>
      - <span data-ttu-id="aaa79-275">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="aaa79-275">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="aaa79-276">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="aaa79-276">Set-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="aaa79-277">New-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="aaa79-277">New-AzureRmApplicationGatewayBackendHttpSetting</span></span>
      - <span data-ttu-id="aaa79-278">Set-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="aaa79-278">Set-AzureRmApplicationGatewayBackendHttpSetting</span></span>
  - <span data-ttu-id="aaa79-279">Cmdlet'ler isteğe bağlı -AutoscaleConfiguration parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-279">Cmdlets updated with optonal parameter -AutoscaleConfiguration</span></span>
      - <span data-ttu-id="aaa79-280">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="aaa79-280">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="aaa79-281">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="aaa79-281">Set-AzureRmApplicationGateway</span></span>
* <span data-ttu-id="aaa79-282">Arabirim Uç Noktası için Get-AzureInterfaceEndpoint cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-282">Add cmdlet for Interface Endpoint Get-AzureInterfaceEndpoint</span></span>
* <span data-ttu-id="aaa79-283">Bir alt ağda birden fazla adres ön eki için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-283">Added support for multiple address prefixes in a subnet.</span></span> <span data-ttu-id="aaa79-284">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="aaa79-284">Updated cmdlets:</span></span>
  - <span data-ttu-id="aaa79-285">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="aaa79-285">New-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="aaa79-286">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="aaa79-286">Set-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="aaa79-287">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="aaa79-287">Add-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="aaa79-288">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="aaa79-288">Get-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="aaa79-289">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="aaa79-289">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>
  - <span data-ttu-id="aaa79-290">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="aaa79-290">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="aaa79-291">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="aaa79-291">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="aaa79-292">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="aaa79-292">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="aaa79-293">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="aaa79-293">Add-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="aaa79-294">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="aaa79-294">New-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="aaa79-295">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="aaa79-295">Set-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="aaa79-296">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="aaa79-296">Add-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="aaa79-297">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="aaa79-297">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="aaa79-298">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="aaa79-298">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="aaa79-299">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="aaa79-299">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="aaa79-300">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="aaa79-300">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="aaa79-301">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="aaa79-301">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="aaa79-302">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="aaa79-302">New-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="aaa79-303">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="aaa79-303">New-AzureRmNetworkInterface</span></span>
* <span data-ttu-id="aaa79-304">Alt ağ temsilcisi seçme cmdlet'leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-304">Adding cmdlets for subnet delegation.</span></span>
  - <span data-ttu-id="aaa79-305">New-AzureRmDelegation: Bir alt ağa eklenebilecek yeni bir temsilci oluşturur</span><span class="sxs-lookup"><span data-stu-id="aaa79-305">New-AzureRmDelegation: Creates a new delegation, which can be added to a subnet</span></span>
  - <span data-ttu-id="aaa79-306">Remove-AzureRmDelegation: Bir alt ağı alır ve belirtilen temsilci adını o alt ağdan kaldırır</span><span class="sxs-lookup"><span data-stu-id="aaa79-306">Remove-AzureRmDelegation: Takes in a subnet and removes the provided delegation name from that subnet</span></span>
  - <span data-ttu-id="aaa79-307">Add-AzureRmDelegation: Bir alt ağı alır ve belirtilen hizmet adını o alt ağa temsilci olarak ekler</span><span class="sxs-lookup"><span data-stu-id="aaa79-307">Add-AzureRmDelegation: Takes in a subnet and adds the provided service name as a delegation to that subnet</span></span>
  - <span data-ttu-id="aaa79-308">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="aaa79-308">Get-AzureRmDelegation</span></span>
  - <span data-ttu-id="aaa79-309">Get-AzureRmAvailableServiceDelegations</span><span class="sxs-lookup"><span data-stu-id="aaa79-309">Get-AzureRmAvailableServiceDelegations</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="aaa79-310">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="aaa79-310">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="aaa79-311">Yönetilen disk desteği</span><span class="sxs-lookup"><span data-stu-id="aaa79-311">Support for managed Managed disk</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="aaa79-312">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="aaa79-312">AzureRM.RedisCache</span></span>
* <span data-ttu-id="aaa79-313">Insights bağımlılığı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-313">Updated Insights dependency.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="aaa79-314">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="aaa79-314">AzureRM.Resources</span></span>
* <span data-ttu-id="aaa79-315">New-AzureRmResourceGroupDeployment cmdlet'i yeni RollbackAction parametresi eklenerek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-315">Update New-AzureRmResourceGroupDeployment with new parameter RollbackAction</span></span>
    - <span data-ttu-id="aaa79-316">Yeni parametreyle OnErrorDeployment desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-316">Add support for OnErrorDeployment with the new parameter.</span></span>
* <span data-ttu-id="aaa79-317">İlke atamalarında yönetilen kimlik desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-317">Support managed identity on policy assignments.</span></span>
* <span data-ttu-id="aaa79-318">Varsayılan değerlere sahip parametrelerin artık 'New-AzureRmPolicyAssignment' ile ilke atama işlemi sırasında belirtilmesi zorunlu değil</span><span class="sxs-lookup"><span data-stu-id="aaa79-318">Parameters with default values are no longer requred when assigning a policy with 'New-AzureRmPolicyAssignment'</span></span>
* <span data-ttu-id="aaa79-319">İlke diğer adlarını almak için yeni Get-AzureRmPolicyAlias cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-319">Add new cmdlet Get-AzureRmPolicyAlias for retrieving policy aliases</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="aaa79-320">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="aaa79-320">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="aaa79-321">7161 numaralı sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-321">Fixed issue #7161</span></span>

#### <a name="azurermsignalr"></a><span data-ttu-id="aaa79-322">AzureRM.SignalR</span><span class="sxs-lookup"><span data-stu-id="aaa79-322">AzureRM.SignalR</span></span>
* <span data-ttu-id="aaa79-323">SKU adları Free_F1 ve Standard_S1 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-323">Update SKU names to Free_F1 and Standard_S1</span></span>
* <span data-ttu-id="aaa79-324">PSSignalRResource nesnesine sürüm alanı, PSSignalRKeys nesnesine de bağlantı dizesi eklendi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-324">Add version field to the PSSignalRResource object and connection string to the PSSignalRKeys object.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="aaa79-325">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="aaa79-325">AzureRM.Storage</span></span>
* <span data-ttu-id="aaa79-326">AzureRm.Storage için Değiştirilemezlik İlkesi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-326">Support Immutability Policy in AzureRm.Storage</span></span> 
    - <span data-ttu-id="aaa79-327">Remove-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="aaa79-327">Remove-AzureRmStorageAccountNetworkRule</span></span>
    - <span data-ttu-id="aaa79-328">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="aaa79-328">Get-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="aaa79-329">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="aaa79-329">Update-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="aaa79-330">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="aaa79-330">New-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="aaa79-331">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="aaa79-331">Remove-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="aaa79-332">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="aaa79-332">Add-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="aaa79-333">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="aaa79-333">Remove-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="aaa79-334">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="aaa79-334">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="aaa79-335">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="aaa79-335">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="aaa79-336">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="aaa79-336">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="aaa79-337">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="aaa79-337">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="aaa79-338">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="aaa79-338">AzureRM.Websites</span></span>
* <span data-ttu-id="aaa79-339">İki yeni cmdlet eklendi: Get-AzureRmDeletedWebApp ve Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="aaa79-339">Added two new cmdlets: Get-AzureRmDeletedWebApp and Restore-AzureRmDeletedWebApp</span></span>
* <span data-ttu-id="aaa79-340">Windows kapsayıcısı ile App Service planı oluşturmak için New-AzureRmAppServicePlan -HyperV anahtarı eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-340">New-AzureRmAppServicePlan -HyperV switch is added for create app service plan with windows container</span></span>
* <span data-ttu-id="aaa79-341">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - Windows kapsayıcı uygulaması oluşturmak ve yönetmek için yeni parametreler (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-341">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - New parameters (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) added for creating and managing windows container app</span></span>

## <a name="681---august-2018"></a><span data-ttu-id="aaa79-342">6.8.1 - Ağustos 2018</span><span class="sxs-lookup"><span data-stu-id="aaa79-342">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="aaa79-343">Genel</span><span class="sxs-lookup"><span data-stu-id="aaa79-343">General</span></span>
* <span data-ttu-id="aaa79-344">Varsayılan kaynak gruplarının ayarlanmamasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-344">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="aaa79-345">Ortak çalışma zamanı bütünleştirilmiş kodları güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-345">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="aaa79-346">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="aaa79-346">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="aaa79-347">Varsayılan kaynak gruplarının ayarlanmamasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-347">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="aaa79-348">https://github.com/Azure/azure-powershell/issues/6603 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-348">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="aaa79-349">Import-AzureRmApiManagementApi ve \*-AzureRmApiManagementCertificate cmdlet’leri artık göreli yolları işleyebiliyor</span><span class="sxs-lookup"><span data-stu-id="aaa79-349">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="aaa79-350">https://github.com/Azure/azure-powershell/issues/6879 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-350">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="aaa79-351">CertificateInformation, Set-AzureRmApiManagement cmdlet’inin düzgün çalışmasını sağlayan, ayarlanabilir bir özelliktir.</span><span class="sxs-lookup"><span data-stu-id="aaa79-351">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="aaa79-352">4.0.4-preview nuget’e yükselterek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-352">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="aaa79-353">https://github.com/Azure/azure-powershell/issues/6853 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-353">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="aaa79-354">Odata filtresi Ürün üzerinde Ada Göre Arama için düzeltildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-354">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="aaa79-355">https://github.com/Azure/azure-powershell/issues/6814 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-355">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="aaa79-356">Odata filtresi API üzerinde Ada Göre Arama için düzeltildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-356">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="aaa79-357">Azure İzleyici günlükçüsüne yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-357">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="aaa79-358">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="aaa79-358">AzureRM.Compute</span></span>
* <span data-ttu-id="aaa79-359">Hata çıktısında hedefin eksik olmasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-359">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="aaa79-360">Yönetilen diske sahip VM için depolama hesabı türüyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-360">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="aaa79-361">Varsayılan kaynak gruplarının ayarlanmamasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-361">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="aaa79-362">Azure Çin gibi diğer ortamlar için AEM Uzantı cmdlet'leri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-362">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="aaa79-363">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="aaa79-363">AzureRM.Network</span></span>
* <span data-ttu-id="aaa79-364">Varsayılan cmdlet çıkış gösterimi, tablo görünümü olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-364">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="aaa79-365">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="aaa79-365">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="aaa79-366">Duraklatılmış kapasite ölçeklendirilmeye çalışılırken Update-AzureRmPowerBIEmbeddedCapacity üzerindeki hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-366">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="aaa79-367">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="aaa79-367">AzureRM.Resources</span></span>
* <span data-ttu-id="aaa79-368">Market’ten yönetilen uygulama oluşturmayla ilgili sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-368">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="aaa79-369">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="aaa79-369">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="aaa79-370">Düzeltilen sorunlar</span><span class="sxs-lookup"><span data-stu-id="aaa79-370">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="aaa79-371">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="aaa79-371">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="aaa79-372">Çoklu değer yönlendirme yöntemi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-372">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="aaa79-373">Çoklu değer yönlendirme için yeni 'MaxReturn' parametresi</span><span class="sxs-lookup"><span data-stu-id="aaa79-373">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="aaa79-374">Alt ağ yönlendirme yöntemi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-374">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="aaa79-375">Uç noktalarda IP adresi aralıkları (alt ağları) desteği</span><span class="sxs-lookup"><span data-stu-id="aaa79-375">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="aaa79-376">Profillerde Özel Üst Bilgi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-376">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="aaa79-377">Profillerde Beklenen durum kodu aralığı desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-377">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="aaa79-378">Uç noktalarda Özel Üst Bilgi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-378">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="aaa79-379">6.8.0 - Ağustos 2018</span><span class="sxs-lookup"><span data-stu-id="aaa79-379">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="aaa79-380">Genel</span><span class="sxs-lookup"><span data-stu-id="aaa79-380">General</span></span>
* <span data-ttu-id="aaa79-381">Varsayılan kaynak gruplarının ayarlanmamasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-381">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="aaa79-382">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="aaa79-382">AzureRM.Profile</span></span>
* <span data-ttu-id="aaa79-383">Connect-AzureRmAccount sırasında döndürülen belirteçlere sona erme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-383">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="aaa79-384">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="aaa79-384">AzureRM.Compute</span></span>
* <span data-ttu-id="aaa79-385">Hata çıktısında hedefin eksik olmasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-385">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="aaa79-386">Yönetilen diske sahip VM için depolama hesabı türüyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-386">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="aaa79-387">Azure Çin gibi diğer ortamlar için AEM Uzantı cmdlet'leri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-387">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="aaa79-388">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="aaa79-388">AzureRM.IotHub</span></span>
* <span data-ttu-id="aaa79-389">New-AzureRmIotHubExportDevices ve New-AzureRmIotHubImportDevices için düzeltme örnekleri</span><span class="sxs-lookup"><span data-stu-id="aaa79-389">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="aaa79-390">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="aaa79-390">AzureRM.Network</span></span>
* <span data-ttu-id="aaa79-391">Varsayılan model gösterimi tablo görünümü olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-391">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="aaa79-392">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="aaa79-392">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="aaa79-393">Duraklatılmış kapasite ölçeklendirilmeye çalışılırken Update-AzureRmPowerBIEmbeddedCapacity üzerindeki hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-393">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="aaa79-394">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="aaa79-394">AzureRM.Resources</span></span>
* <span data-ttu-id="aaa79-395">Marketten yönetilen uygulamayla ilgili sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-395">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="aaa79-396">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="aaa79-396">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="aaa79-397">Sorunlar için düzeltme</span><span class="sxs-lookup"><span data-stu-id="aaa79-397">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="aaa79-398">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="aaa79-398">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="aaa79-399">Çoklu değer yönlendirme yöntemi desteği</span><span class="sxs-lookup"><span data-stu-id="aaa79-399">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="aaa79-400">Çoklu değer yönlendirme için yeni 'MaxReturn' parametresi</span><span class="sxs-lookup"><span data-stu-id="aaa79-400">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="aaa79-401">Alt ağ yönlendirme yöntemi desteği</span><span class="sxs-lookup"><span data-stu-id="aaa79-401">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="aaa79-402">Uç noktalarda IP adresi aralıkları (alt ağları) desteği</span><span class="sxs-lookup"><span data-stu-id="aaa79-402">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="aaa79-403">Profillerde Özel Üst Bilgi desteği</span><span class="sxs-lookup"><span data-stu-id="aaa79-403">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="aaa79-404">Profillerde Beklenen durum kodu aralığı desteği</span><span class="sxs-lookup"><span data-stu-id="aaa79-404">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="aaa79-405">Uç noktalarda Özel Üst Bilgi desteği</span><span class="sxs-lookup"><span data-stu-id="aaa79-405">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="aaa79-406">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="aaa79-406">AzureRM.Websites</span></span>
* <span data-ttu-id="aaa79-407">Varsayılan kaynak gruplarının yanlış ayarlanmasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-407">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="aaa79-408">6.7.0 - Ağustos 2018</span><span class="sxs-lookup"><span data-stu-id="aaa79-408">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="aaa79-409">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="aaa79-409">AzureRM.Profile</span></span>
* <span data-ttu-id="aaa79-410">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-410">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="aaa79-411">Bağlam çakışmasını önlemek için varsayılan bağlam adına kullanıcı kimliği eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-411">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="aaa79-412">Bağlam #6398 seçerken sorunlara neden olan Clear-AzureRmContext ile ilgili sorunlar giderildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-412">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="aaa79-413">'Connect-AzureRmAccount' için kiracı etki alanının '-TenantId' parametresine geçirilmesi etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-413">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="aaa79-414">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="aaa79-414">Azure.Storage</span></span>
* <span data-ttu-id="aaa79-415">Azure Dosya Paylaşımı kotasındaki 5 TB'lık sınır kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="aaa79-415">Remove the 5TB limitation for Azure File Share quota</span></span>
* <span data-ttu-id="aaa79-416">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="aaa79-416">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="aaa79-417">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="aaa79-417">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="aaa79-418">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-418">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="aaa79-419">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="aaa79-419">Azure.AnalysisServices</span></span>
* <span data-ttu-id="aaa79-420">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-420">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="aaa79-421">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="aaa79-421">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="aaa79-422">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-422">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="aaa79-423">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="aaa79-423">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="aaa79-424">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-424">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="aaa79-425">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="aaa79-425">AzureRM.Automation</span></span>
* <span data-ttu-id="aaa79-426">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-426">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="aaa79-427">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="aaa79-427">AzureRM.Backup</span></span>
* <span data-ttu-id="aaa79-428">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-428">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="aaa79-429">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="aaa79-429">AzureRM.Batch</span></span>
* <span data-ttu-id="aaa79-430">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-430">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="aaa79-431">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="aaa79-431">AzureRM.Billing</span></span>
* <span data-ttu-id="aaa79-432">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-432">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="aaa79-433">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="aaa79-433">AzureRM.Cdn</span></span>
* <span data-ttu-id="aaa79-434">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-434">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="aaa79-435">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="aaa79-435">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="aaa79-436">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-436">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="aaa79-437">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="aaa79-437">AzureRM.Compute</span></span>
* <span data-ttu-id="aaa79-438">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-438">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="aaa79-439">New-AzureRmVmssConfig’e EvictionPolicy parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-439">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="aaa79-440">Hiçbir konum belirtilmediyse New-AzureRmVm’nin DiskFileParameterSet parametresinde varsayılan konum kullanılıyor.</span><span class="sxs-lookup"><span data-stu-id="aaa79-440">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="aaa79-441">Save-AzureRmVMImage cmdlet'inde parametre açıklaması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-441">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="aaa79-442">Singlepass ile ilgili bazı senaryolarda Get-AzureRmVMDiskEncryptionStatus cmdlet’i düzeltildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-442">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="aaa79-443">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="aaa79-443">AzureRM.Consumption</span></span>
* <span data-ttu-id="aaa79-444">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-444">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="aaa79-445">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="aaa79-445">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="aaa79-446">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-446">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="aaa79-447">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="aaa79-447">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="aaa79-448">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-448">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="aaa79-449">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="aaa79-449">AzureRM.DataFactories</span></span>
* <span data-ttu-id="aaa79-450">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-450">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="aaa79-451">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="aaa79-451">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="aaa79-452">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-452">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="aaa79-453">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="aaa79-453">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="aaa79-454">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-454">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="aaa79-455">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="aaa79-455">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="aaa79-456">DebugPreference Powershell komut satırından ayarlandığında hata ayıklama düzeltildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-456">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="aaa79-457">Set-AzureRmDataLakeStoreItemAcl örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-457">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="aaa79-458">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-458">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="aaa79-459">Set-AzureRmDataLakeStoreItemAclEntry örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-459">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="aaa79-460">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="aaa79-460">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="aaa79-461">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-461">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="aaa79-462">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="aaa79-462">AzureRM.Dns</span></span>
* <span data-ttu-id="aaa79-463">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-463">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="aaa79-464">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="aaa79-464">AzureRM.EventGrid</span></span>
* <span data-ttu-id="aaa79-465">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-465">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="aaa79-466">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="aaa79-466">AzureRM.EventHub</span></span>
* <span data-ttu-id="aaa79-467">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-467">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="aaa79-468">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="aaa79-468">AzureRM.HDInsight</span></span>
* <span data-ttu-id="aaa79-469">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-469">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="aaa79-470">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="aaa79-470">AzureRM.Insights</span></span>
* <span data-ttu-id="aaa79-471">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-471">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="aaa79-472">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="aaa79-472">AzureRM.IotHub</span></span>
* <span data-ttu-id="aaa79-473">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-473">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="aaa79-474">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="aaa79-474">AzureRM.KeyVault</span></span>
* <span data-ttu-id="aaa79-475">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-475">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="aaa79-476">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="aaa79-476">AzureRM.LogicApp</span></span>
* <span data-ttu-id="aaa79-477">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-477">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="aaa79-478">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="aaa79-478">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="aaa79-479">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-479">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="aaa79-480">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="aaa79-480">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="aaa79-481">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-481">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="aaa79-482">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="aaa79-482">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="aaa79-483">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-483">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="aaa79-484">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="aaa79-484">AzureRM.Media</span></span>
* <span data-ttu-id="aaa79-485">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-485">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="aaa79-486">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="aaa79-486">AzureRM.Network</span></span>
* <span data-ttu-id="aaa79-487">Set-AzureRmLocalNetworkGateway örneği eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-487">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="aaa79-488">Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey ve New-AzureRmVirtualNetworkGatewayConnection için örnek ve açıklamalar eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-488">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="aaa79-489">Remove-AzureRmVirtualNetworkGatewayIpConfig ve Reset-AzureRmVirtualNetworkGateway örnekleri eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-489">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="aaa79-490">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey örneği eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-490">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="aaa79-491">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey örneği eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-491">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="aaa79-492">Set-AzureRmVirtualNetworkGatewayConnection örneği eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-492">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="aaa79-493">ApplicationSecurityGroup, RouteTable ve Usage için en son kod oluşturucu kullanılarak cmdlet’ler yeniden oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="aaa79-493">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="aaa79-494">Varolmayan bir alt ağ alma girişiminde bulunulduğunda Get-AzureRmVirtualNetworkSubnetConfig cmdlet'inin hata iletisi netleştirildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-494">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="aaa79-495">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="aaa79-495">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="aaa79-496">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-496">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="aaa79-497">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="aaa79-497">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="aaa79-498">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-498">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="aaa79-499">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="aaa79-499">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="aaa79-500">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-500">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="aaa79-501">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="aaa79-501">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="aaa79-502">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-502">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="aaa79-503">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="aaa79-503">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="aaa79-504">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-504">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="aaa79-505">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="aaa79-505">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="aaa79-506">Get-AzureRmRecoveryServicesBackItem cmdlet’ine ilke filtresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-506">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="aaa79-507">Komut, verilen ilke kimliği tarafından korunan yedekleme öğelerinin listesini döndürüyor.</span><span class="sxs-lookup"><span data-stu-id="aaa79-507">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="aaa79-508">Microsoft.Azure.Management.RecoveryServices.Backup, sürüm 3.0.0 önizlemesine güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-508">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="aaa79-509">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-509">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="aaa79-510">Restore-AzureRmRecoveryServicesBackupItem’e TargetResourceGroupName parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-510">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="aaa79-511">Yönetilen disklerin geri yüklendiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="aaa79-511">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="aaa79-512">Yönetilen disklerle yapılan VM yedeklemesi için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="aaa79-512">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="aaa79-513">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="aaa79-513">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="aaa79-514">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-514">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="aaa79-515">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="aaa79-515">AzureRM.RedisCache</span></span>
* <span data-ttu-id="aaa79-516">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-516">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="aaa79-517">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="aaa79-517">AzureRM.Relay</span></span>
* <span data-ttu-id="aaa79-518">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-518">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="aaa79-519">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="aaa79-519">AzureRM.Resources</span></span>
* <span data-ttu-id="aaa79-520">Abonelik kapsamındaki şablon dağıtımı destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="aaa79-520">Support template deployment at subscription scope.</span></span> <span data-ttu-id="aaa79-521">Yeni Cmdlet’ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="aaa79-521">Add new Cmdlets:</span></span>
    - <span data-ttu-id="aaa79-522">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="aaa79-522">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="aaa79-523">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="aaa79-523">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="aaa79-524">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="aaa79-524">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="aaa79-525">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="aaa79-525">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="aaa79-526">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="aaa79-526">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="aaa79-527">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="aaa79-527">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="aaa79-528">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="aaa79-528">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="aaa79-529">Set-AzureRmResource’a bağlam geçirilirken hata oluşmasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-529">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="aaa79-530">New-AzureRmResourceGroupDeployment cmdlet'indeki örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-530">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="aaa79-531">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-531">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="aaa79-532">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="aaa79-532">AzureRM.Scheduler</span></span>
* <span data-ttu-id="aaa79-533">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-533">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="aaa79-534">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="aaa79-534">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="aaa79-535">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-535">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="aaa79-536">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="aaa79-536">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="aaa79-537">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-537">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="aaa79-538">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="aaa79-538">AzureRM.Sql</span></span>
* <span data-ttu-id="aaa79-539">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-539">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="aaa79-540">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="aaa79-540">AzureRM.Storage</span></span>
* <span data-ttu-id="aaa79-541">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-541">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="aaa79-542">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="aaa79-542">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="aaa79-543">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-543">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="aaa79-544">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="aaa79-544">AzureRM.Tags</span></span>
* <span data-ttu-id="aaa79-545">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-545">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="aaa79-546">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="aaa79-546">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="aaa79-547">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-547">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="aaa79-548">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="aaa79-548">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="aaa79-549">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-549">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="aaa79-550">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="aaa79-550">AzureRM.Websites</span></span>
* <span data-ttu-id="aaa79-551">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-551">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="aaa79-552">6.6.0 - Temmuz 2018</span><span class="sxs-lookup"><span data-stu-id="aaa79-552">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="aaa79-553">Genel</span><span class="sxs-lookup"><span data-stu-id="aaa79-553">General</span></span>
* <span data-ttu-id="aaa79-554">Tüm yardım dosyaları tam parametre türleriyle doğru giriş/çıkış türlerini içerecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-554">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="aaa79-555">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="aaa79-555">AzureRM.Profile</span></span>
* <span data-ttu-id="aaa79-556">Kaynağın geçerli yapılandırmasının hedef kaynakla uyumlu olduğunu doğrulayabilmek için Common.Strategy kitaplığı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-556">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="aaa79-557">Common.Storage'a ps1xml türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-557">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="aaa79-558">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="aaa79-558">Azure.Storage</span></span>
* <span data-ttu-id="aaa79-559">DefaultProfile’dan Depolama Bağlamı almak için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-559">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="aaa79-560">Cmdlet'lerin çıkış türü özelliklerine Ps1XmlAttribute eklendi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-560">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="aaa79-561">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="aaa79-561">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="aaa79-562">https://github.com/Azure/azure-powershell/issues/6370 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-562">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="aaa79-563">PsApiManagementApi'yi ApiContract'e çevirmek için Automapper hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-563">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="aaa79-564">https://github.com/Azure/azure-powershell/issues/6515 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-564">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="aaa79-565">Kodlama Türü ile aşırı yüklemeyi önlemek için File.Save hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-565">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="aaa79-566">https://github.com/Azure/azure-powershell/issues/6560 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-566">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="aaa79-567">apiId üzerindeki desen özel durumunu düzelten 4.0.3 Nuget sürümüne yükseltildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-567">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="aaa79-568">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="aaa79-568">AzureRM.Compute</span></span>
* <span data-ttu-id="aaa79-569">PremiumLRS depolama hesap türü yeniden adlandırması nedeniyle New-AzureRmVm'de DiskFileParameterSet kullanılarak sanal makine oluşturmanın başarısız olmasıyla ilgili hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-569">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="aaa79-570">Invoke-AzureRmVMRunCommand cmdlet'i düzeltildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-570">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="aaa79-571">Abonelikteki tüm kullanılabilir kümelerin listelenebilmesi için Get-AzureRmAvailabilitySet güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-571">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="aaa79-572">(ResouceGroupName parametresi artık isteğe bağlı.)</span><span class="sxs-lookup"><span data-stu-id="aaa79-572">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="aaa79-573">Uygun sanal makinelerde Hızlandırılmış Ağı etkinleştirmek için 'New-AzureRmVm' cmdlet'inin SimpleParameterSet öğesi güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-573">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="aaa79-574">Kullanıcının belirttiği LB zaten mevcut olduğunda vmss oluşturmanın başarısız olması için New-AzureRmVmss basit parametre kümesi güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-574">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="aaa79-575">New-AzureRmDisk örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-575">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="aaa79-576">'New-AzureRmVM' için örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-576">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="aaa79-577">Set-AzureRmVMOSDisk açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-577">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="aaa79-578">Yazımı ve ön eki düzeltmek amacıyla Set-AzureRmVMBginfoExtension için Örnek 1 güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-578">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="aaa79-579">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="aaa79-579">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="aaa79-580">ADF .Net SDK sürümü 1.1.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-580">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="aaa79-581">Veri fabrikaları arasında paylaşılan şirket içinde barındırılan tümleştirme çalışma zamanı desteği.</span><span class="sxs-lookup"><span data-stu-id="aaa79-581">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="aaa79-582">Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet'ine yeni -SharedIntegrationRuntimeResourceId parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-582">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="aaa79-583">Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet'ine isteğe bağlı yeni -LinkedDataFactoryName parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-583">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="aaa79-584">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="aaa79-584">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="aaa79-585">DataPlane SDK'sı (Microsoft.Azure.DataLake.Store) sürümü 1.1.9'a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-585">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="aaa79-586">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="aaa79-586">AzureRM.EventHub</span></span>
* <span data-ttu-id="aaa79-587">Kaldırma cmdlet'lerine InputObject ve ResourceId yöneltmesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-587">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="aaa79-588">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="aaa79-588">AzureRM.Insights</span></span>
* <span data-ttu-id="aaa79-589">Yardım dosyalarındaki OutputType biçimlendirmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-589">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="aaa79-590">Microsoft.Azure.Management.Monitor SDK 0.19.1-preview kullanımı</span><span class="sxs-lookup"><span data-stu-id="aaa79-590">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="aaa79-591">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="aaa79-591">AzureRM.KeyVault</span></span>
* <span data-ttu-id="aaa79-592">Set-AzureRmKeyVaultAccessPolicy'de yönlendirme sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-592">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="aaa79-593">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="aaa79-593">AzureRM.Network</span></span>
* <span data-ttu-id="aaa79-594">LoadBalancerInboundNatPoolConfig cmdlet'leri için örnekler eklendi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-594">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="aaa79-595">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="aaa79-595">AzureRM.Resources</span></span>
* <span data-ttu-id="aaa79-596">'Get-AzureRmResource' için hem etiket adı hem de değer sağlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-596">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="aaa79-597">'Set-AzureRmResource' için yönlendirme senaryosu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-597">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="aaa79-598">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="aaa79-598">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="aaa79-599">Kaldırma cmdlet'lerine InputObject ve ResourceId yöneltmesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-599">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="aaa79-600">birkaç sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-600">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="aaa79-601">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="aaa79-601">AzureRM.Sql</span></span>
* <span data-ttu-id="aaa79-602">Aşağıdaki cmdlet'lere Sunucu Gelişmiş Tehdit Koruması desteği ekleniyor:</span><span class="sxs-lookup"><span data-stu-id="aaa79-602">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="aaa79-603">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="aaa79-603">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="aaa79-604">Aşağıdaki cmdlet'lere Güvenlik Açığı Değerlendirme desteği ekleniyor:</span><span class="sxs-lookup"><span data-stu-id="aaa79-604">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="aaa79-605">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="aaa79-605">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="aaa79-606">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="aaa79-606">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="aaa79-607">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="aaa79-607">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="aaa79-608">Remove-AzureRmSqlServerFirewallRulecmdlet'indeki örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-608">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="aaa79-609">Get-AzureSqlSyncGroupLog içinde ABD temelli olmayan kültürde yanlış tarih saat işlemesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-609">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="aaa79-610">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="aaa79-610">AzureRM.Storage</span></span>
* <span data-ttu-id="aaa79-611">Cmdlet'lerin çıkış türü özelliklerine Ps1XmlAttribute eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-611">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="aaa79-612">Tablo görünümünde StorageAccount cmdlet'i çıkışı gösteriliyor</span><span class="sxs-lookup"><span data-stu-id="aaa79-612">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="aaa79-613">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="aaa79-613">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="aaa79-614">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="aaa79-614">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="aaa79-615">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="aaa79-615">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="aaa79-616">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="aaa79-616">AzureRM.Tags</span></span>
* <span data-ttu-id="aaa79-617">Tag cmdlet'inin yardımında hatayı deyim kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="aaa79-617">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="aaa79-618">6.5.0 - Temmuz 2018</span><span class="sxs-lookup"><span data-stu-id="aaa79-618">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="aaa79-619">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="aaa79-619">AzureRM.Profile</span></span>
* <span data-ttu-id="aaa79-620">'Get-AzureRmContextAutosaveSetting' için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-620">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="aaa79-621">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="aaa79-621">Azure.Storage</span></span>
* <span data-ttu-id="aaa79-622">Salt yazılır Sas belirteciyle Karşıya Yükleme Blobu veya Dosyası desteği</span><span class="sxs-lookup"><span data-stu-id="aaa79-622">Support Upload Blob or File with write only Sas token</span></span>
* <span data-ttu-id="aaa79-623">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="aaa79-623">Set-AzureStorageBlobContent</span></span>
* <span data-ttu-id="aaa79-624">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="aaa79-624">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="aaa79-625">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="aaa79-625">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="aaa79-626">AS'ye gerekli ResourceGroupName özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-626">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="aaa79-627">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="aaa79-627">AzureRM.Automation</span></span>
* <span data-ttu-id="aaa79-628">'New-AzureRMAutomationSchedule' için yardım güncelleştirildi ve örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-628">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="aaa79-629">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="aaa79-629">AzureRM.Compute</span></span>
* <span data-ttu-id="aaa79-630">Update/New-AzureRmAvailabilitySet komutlarına -Tag parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-630">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="aaa79-631">'Add-AzureRmVmssExtension' için örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-631">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="aaa79-632">'Remove-AzureRmVmssExtension' için örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-632">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="aaa79-633">'Set-AzureRmVMAccessExtension' için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-633">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="aaa79-634">New-AzureRmVmss için SimpleParameterSet güncelleştirilerek SinglePlacementGroup varsayılan olarak false değerine ayarlandı ve kullanıcının tek yerleşim grubunda VMSS oluşturmasına olanak tanıyan 'SinglePlacementGroup' geçiş parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-634">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="aaa79-635">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="aaa79-635">AzureRM.EventHub</span></span>
* <span data-ttu-id="aaa79-636">PSEventHubDRConfigurationAttributes sınıfına, çoğaltma işlemi devam ederken bekleyen çoğaltma işlemlerinin sayısını veren salt okunur 'PendingReplicationOperationsCount' özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-636">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="aaa79-637">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="aaa79-637">AzureRM.KeyVault</span></span>
* <span data-ttu-id="aaa79-638">Set-AzureRmKeyVaultAccessPolicy için hata iletisi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-638">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="aaa79-639">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="aaa79-639">AzureRM.LogicApp</span></span>
* <span data-ttu-id="aaa79-640">New-AzureRmLogicApp’te "parametre kümesi çözümlenemedi" hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-640">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="aaa79-641">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="aaa79-641">AzureRM.Network</span></span>
* <span data-ttu-id="aaa79-642">Set/Add-AzureRmVirtualNetworkPeering için birden çok Kiracıdaki Sanal Makineler arasında eşleme etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-642">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="aaa79-643">Aşağıdaki cmdlet’ler Application Gateway için güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-643">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="aaa79-644">New-AzureRmApplicationGateway : EnableFIPS bayrağı ve Zones desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-644">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="aaa79-645">New-AzureRmApplicationGatewaySku : Yeni Standard_v2 ve WAF_v2 sku'ları eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-645">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="aaa79-646">Set-AzureRmApplicationGatewaySku : Yeni Standard_v2 ve WAF_v2 sku'ları eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-646">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="aaa79-647">RouteTable cmdlet’leri en son oluşturucu sürümüyle yeniden oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="aaa79-647">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="aaa79-648">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="aaa79-648">AzureRM.Relay</span></span>
* <span data-ttu-id="aaa79-649">Markdown dosyaları güncelleştirildi, örnekteki parametre adı sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="aaa79-649">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="aaa79-650">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="aaa79-650">AzureRM.Resources</span></span>
* <span data-ttu-id="aaa79-651">Roleassignment ve roledefinition cmdlet’leri güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="aaa79-651">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="aaa79-652">Disk belleğinin parçası olarak yapılan ek roledefinition çağrıları kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="aaa79-652">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="aaa79-653">Get-AzureRmRoleAssignment cmdlet’i düzeltildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-653">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="aaa79-654">-ExpandPrincipalGroups komut parametresi işlevselliği düzeltildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-654">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="aaa79-655">'-ResourceType' parametresinin büyük/küçük harfe duyarlı olduğu 'Get-AzureRmResource' sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-655">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="aaa79-656">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="aaa79-656">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="aaa79-657">Liste cmdlet’lerine top ve skip parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-657">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="aaa79-658">Standard'dan Premium NameSpace'e geçiş cmdlet’leri eklendi :</span><span class="sxs-lookup"><span data-stu-id="aaa79-658">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="aaa79-659">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="aaa79-659">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="aaa79-660">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="aaa79-660">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="aaa79-661">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="aaa79-661">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="aaa79-662">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="aaa79-662">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="aaa79-663">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="aaa79-663">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="aaa79-664">PSServiceBusDRConfigurationAttributes sınıfına, çoğaltma işlemi sürerken beklemede olan çoğaltma işlemi sayısını veren salt okunur 'PendingReplicationOperationsCount' özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-664">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="aaa79-665">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="aaa79-665">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="aaa79-666">'New-AzureRmServiceFabricCluster' için örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-666">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="aaa79-667">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="aaa79-667">AzureRM.Sql</span></span>
* <span data-ttu-id="aaa79-668">Müşterilerin Sql Server örneğine veya Yönetilen Örneğe TDE Sertifikası ekleyebilmeleri için yeni Management.Sql Cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-668">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="aaa79-669">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="aaa79-669">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="aaa79-670">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="aaa79-670">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="aaa79-671">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="aaa79-671">AzureRM.Websites</span></span>
* <span data-ttu-id="aaa79-672">Artık `Set-AzureRmWebApp -AssignIdentity` ve `Set-AzureRmWebAppSlot -AssignIdentity` false olarak ayarlandığında site object.Removing önizleme etiketinden Identity özelliğini kaldırıyor.</span><span class="sxs-lookup"><span data-stu-id="aaa79-672">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="aaa79-673">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-673">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="aaa79-674">`Set-AzureRmWebApp -PhpVersion` geçerli bir php sürümü off değerini destekliyor</span><span class="sxs-lookup"><span data-stu-id="aaa79-674">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="aaa79-675">6.4.0 - Temmuz 2018</span><span class="sxs-lookup"><span data-stu-id="aaa79-675">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="aaa79-676">Genel</span><span class="sxs-lookup"><span data-stu-id="aaa79-676">General</span></span>
* <span data-ttu-id="aaa79-677">Modüllerin çoğu için yardım dosyalarındaki OutputType biçimlendirmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-677">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="aaa79-678">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="aaa79-678">AzureRM.Profile</span></span>
* <span data-ttu-id="aaa79-679">Temel çıkış türlerine Ps1Xml özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-679">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="aaa79-680">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="aaa79-680">AzureRM.Compute</span></span>
* <span data-ttu-id="aaa79-681">VMSS için IP Etiketi özelliği</span><span class="sxs-lookup"><span data-stu-id="aaa79-681">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="aaa79-682">'New-AzureRmVmssIpTagConfig' cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-682">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="aaa79-683">New-AzureRmVmssIpConfig cmdlet'ine IpTag parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-683">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="aaa79-684">VMSS için Otomatik İşletim Sistemi Geri Alma özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-684">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="aaa79-685">New-AzureRmVmssConfig ve Update-AzureRmVmss cmdlet'lerine DisableAutoRollback parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-685">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="aaa79-686">VMSS için İşletim Sistemi Yükseltme Geçmişi özelliği</span><span class="sxs-lookup"><span data-stu-id="aaa79-686">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="aaa79-687">Get-AzureRmVmss cmdlet'ine OSUpgradeHistory anahtarı parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-687">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="aaa79-688">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="aaa79-688">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="aaa79-689">Aşağıdaki komutlarla Katalog ACL'si için destek eklendi:</span><span class="sxs-lookup"><span data-stu-id="aaa79-689">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="aaa79-690">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="aaa79-690">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="aaa79-691">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="aaa79-691">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="aaa79-692">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="aaa79-692">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="aaa79-693">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="aaa79-693">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="aaa79-694">Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry ve Set-AzureRmDataLakeStoreItemAcl için iptal desteği ve ilerleme izleme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-694">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="aaa79-695">Export-AzureRmDataLakeStoreChildItemProperties için iptal desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-695">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="aaa79-696">Özyinelemeli işlemler gerçekleştiren cmdlet'ler için hata ayıklama iletilerinin boşaltılması hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-696">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="aaa79-697">DataLake cmdlet'lerinin test konumu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-697">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="aaa79-698">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="aaa79-698">AzureRM.EventHub</span></span>
* <span data-ttu-id="aaa79-699">Get-AzureRmEventHub ve Get-AzureRmEventHubConsumerGroup Listeleme İşlemleri cmdlet'lerine İsteğe Bağlı MaxCount parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-699">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="aaa79-700">New-AzureRmEventHub cmdlet'inde yeni Olay Hub'ı oluşturma sırasında en az bir parametreye ihtiyaç duyma sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-700">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="aaa79-701">Varsayılan Parametre kümesi sağlandı.</span><span class="sxs-lookup"><span data-stu-id="aaa79-701">Provided Default Parameter set.</span></span>
* <span data-ttu-id="aaa79-702">Kullanıcının New-AzureRmEventHubKey cmdlet'ine KeyValue eklemesini sağlayan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-702">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="aaa79-703">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="aaa79-703">AzureRM.KeyVault</span></span>
* <span data-ttu-id="aaa79-704">Get-AzureRmKeyVault -Tag ile tüm kaynakların döndürülmesine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-704">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="aaa79-705">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="aaa79-705">AzureRM.Network</span></span>
* <span data-ttu-id="aaa79-706">Zone-Redundant VirtualNetworkGateways için yeni SKU'lar kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="aaa79-706">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="aaa79-707">ARM aracılığıyla ExpressRoute Partner API'leri özelliği için yeni komutlar eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-707">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="aaa79-708">Get-AzureRmExpressRouteCrossConnection eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-708">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="aaa79-709">Set-AzureRmExpressRouteCrossConnection eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-709">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="aaa79-710">Add-AzureRmExpressRouteCrossConnectionPeering eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-710">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="aaa79-711">Get-AzureRmExpressRouteCrossConnectionPeering eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-711">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="aaa79-712">Remove-AzureRmExpressRouteCrossConnectionPeering eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-712">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="aaa79-713">Get-AzureRMExpressRouteCrossConnectionArpTable eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-713">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="aaa79-714">Get-AzureRMExpressRouteCrossConnectionRouteTable eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-714">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="aaa79-715">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-715">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="aaa79-716">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="aaa79-716">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="aaa79-717">Get-AzureRmRecoveryServicesBackupStatus cmdlet'i eklendi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-717">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="aaa79-718">Bu cmdlet bir sanal makinenin kimliğini alır ve sanal makinenin abonelik içindeki kasaların koruması altında olup olmadığını denetler.</span><span class="sxs-lookup"><span data-stu-id="aaa79-718">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="aaa79-719">Böyle bir kasa varsa cmdlet, bu kasanın ayrıntılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="aaa79-719">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="aaa79-720">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="aaa79-720">AzureRM.Resources</span></span>
* <span data-ttu-id="aaa79-721">Get-AzureRmPolicyAssignment cmdlet'leri güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="aaa79-721">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="aaa79-722">Yönetim grubu düzeyinde -Scope değerlerini listeleme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-722">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="aaa79-723">Yönetim grubu düzeyinde -Scope değerlerine sahip olan tek atamaları alma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-723">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="aaa79-724">control parametresine -Effective ve -All anahtarları eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-724">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="aaa79-725">Get/New/Remove/Set-AzureRmPolicyDefinition cmdlet'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-725">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="aaa79-726">Belirli bir yönetim grubuna işlem uygulamayı sağlayan için -ManagementGroupName parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-726">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="aaa79-727">Belirli bir aboneliğe işlem uygulamayı sağlayan Add -SubscriptionId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-727">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="aaa79-728">Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlet'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-728">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="aaa79-729">Belirli bir yönetim grubuna işlem uygulamayı sağlayan -ManagementGroupName parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-729">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="aaa79-730">Belirli bir aboneliğe işlem uygulamayı sağlayan Add -SubscriptionId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-730">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="aaa79-731">'New-AzureRmResourceGroupDeployment' içinde 'TemplateParameterObject' kullanırken parametrelerde KeyVault gizli dizi başvurusu desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-731">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="aaa79-732">'New-AzureRmADAppCredential' için '-EndDate' parametresinin yoksayılmasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-732">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="aaa79-733">'Add-AzureRmADGroupMember' cmdlet'inin istekte bulunmak için yanlış URL'yi kullandığı sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-733">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="aaa79-734">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="aaa79-734">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="aaa79-735">Kullanıcının New-AzureRmServiceBusKey cmdlet'ine KeyValue eklemesini sağlayan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-735">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="aaa79-736">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="aaa79-736">AzureRM.Sql</span></span>
* <span data-ttu-id="aaa79-737">New-AzureRmSqlDatabaseRestorePoint yardımında Kullanıcı Tanımlı Geri Yükleme Noktaları netleştirildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-737">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="aaa79-738">Birden fazla cmdlet'te -ComputeGeneration parametresinin belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-738">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="aaa79-739">6.3.0 - Haziran 2018</span><span class="sxs-lookup"><span data-stu-id="aaa79-739">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="aaa79-740">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="aaa79-740">AzureRM.Profile</span></span>
* <span data-ttu-id="aaa79-741">Enable-AzureRmContextAutoSave için hata iletileri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-741">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="aaa79-742">'Connect-AzureRmAccount' cmdlet'i eski bir bağlam olmadan çalıştırıldığında her abonelik için bir bağlam oluşturur</span><span class="sxs-lookup"><span data-stu-id="aaa79-742">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="aaa79-743">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="aaa79-743">Azure.Storage</span></span>
* <span data-ttu-id="aaa79-744">Yardım dosyalarına -Permissions parametresi hakkında daha fazla bilgi eklendi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-744">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="aaa79-745">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="aaa79-745">AzureRM.Compute</span></span>
* <span data-ttu-id="aaa79-746">'Get-AzureRmVmDiskEncryptionStatus' için veri diski bulunmayan VM'lerde karşılaşılan bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-746">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="aaa79-747">Aşağıdaki cmdlet'leri düzeltmek için bilgisayar istemci kitaplığı sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-747">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="aaa79-748">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="aaa79-748">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="aaa79-749">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="aaa79-749">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="aaa79-750">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="aaa79-750">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="aaa79-751">Aşağıdaki cmdlet'ler 'operation ID' ve 'operation status' bilgilerini doğru gösterecek şekilde düzeltildi:</span><span class="sxs-lookup"><span data-stu-id="aaa79-751">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="aaa79-752">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="aaa79-752">Start-AzureRmVM</span></span>
    - <span data-ttu-id="aaa79-753">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="aaa79-753">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="aaa79-754">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="aaa79-754">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="aaa79-755">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="aaa79-755">Set-AzureRmVM</span></span>
    - <span data-ttu-id="aaa79-756">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="aaa79-756">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="aaa79-757">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="aaa79-757">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="aaa79-758">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="aaa79-758">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="aaa79-759">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="aaa79-759">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="aaa79-760">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="aaa79-760">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="aaa79-761">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="aaa79-761">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="aaa79-762">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="aaa79-762">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="aaa79-763">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="aaa79-763">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="aaa79-764">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="aaa79-764">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="aaa79-765">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="aaa79-765">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="aaa79-766">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="aaa79-766">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="aaa79-767">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="aaa79-767">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="aaa79-768">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="aaa79-768">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="aaa79-769">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="aaa79-769">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="aaa79-770">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="aaa79-770">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="aaa79-771">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="aaa79-771">AzureRM.EventGrid</span></span>
* <span data-ttu-id="aaa79-772">Gerekli olması halinde parametrelerin boş dizeyle değiştirilmesine izin vermek için Update-AzureRmEventGridSubscription cmdlet'i içindeki SubjectBeginsWith/SubjectEndsWith için ValidateNotNullOrEmpty doğrulama koşulları kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="aaa79-772">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="aaa79-773">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="aaa79-773">AzureRM.KeyVault</span></span>
* <span data-ttu-id="aaa79-774">Get-AzureRmKeyVault -Tag çalıştırıldığında etiket döndürülmeme sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-774">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="aaa79-775">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="aaa79-775">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="aaa79-776">Policy Insights cmdlet'leri genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="aaa79-776">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="aaa79-777">API 2018-04-04 sürümünü kullanın</span><span class="sxs-lookup"><span data-stu-id="aaa79-777">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="aaa79-778">PolicyDefinitionReferenceId, Get-AzureRmPolicyStateSummary sonuçlarına eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-778">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="aaa79-779">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="aaa79-779">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="aaa79-780">RecoveryServices.Backup cmdlet'lerine -Vault parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-780">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="aaa79-781">Bu parametre iletildiğinde Set-AzureRmRecoveryServicesContext cmdlet'ini geçersiz kılar.</span><span class="sxs-lookup"><span data-stu-id="aaa79-781">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="aaa79-782">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="aaa79-782">AzureRM.Sql</span></span>
* <span data-ttu-id="aaa79-783">Yardım dosyasındaki Get-AzureRmSqlDatabaseExpanded örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-783">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="aaa79-784">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="aaa79-784">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="aaa79-785">Yardım dosyasındaki Add-AzureRmTrafficManagerEndpointConfig bölümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-785">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="aaa79-786">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="aaa79-786">AzureRM.Websites</span></span>
* <span data-ttu-id="aaa79-787">'Set-AzureRmWebApp', -AssignIdentity kullanıldığında AppSettings verilerini geçersiz kılmayacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-787">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="aaa79-788">'New-AzureRmWebAppSlot', isteğe bağlı parametre olarak AppServicePlan girişini kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-788">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="aaa79-789">6.2.1 - Haziran 2018</span><span class="sxs-lookup"><span data-stu-id="aaa79-789">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="aaa79-790">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="aaa79-790">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="aaa79-791">PSWorkspace modeli Network için tür parametresini kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-791">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="aaa79-792">6.2.0 - Haziran 2018</span><span class="sxs-lookup"><span data-stu-id="aaa79-792">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="aaa79-793">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="aaa79-793">AzureRM.Profile</span></span>
* <span data-ttu-id="aaa79-794">Modülün içeri aktarılması sırasında Newtonsoft.Json 10.0.3 sürümünün yüklenmemesine ilişkin sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-794">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="aaa79-795">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="aaa79-795">AzureRM.Compute</span></span>
* <span data-ttu-id="aaa79-796">VMSS VM Güncelleştirme özelliği</span><span class="sxs-lookup"><span data-stu-id="aaa79-796">VMSS VM Update feature</span></span>
    - <span data-ttu-id="aaa79-797">'Update-AzureRmVmssVM' ve 'New-AzureRmVMDataDisk' cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-797">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="aaa79-798">VMSS VM’sine veri diski eklemeyi desteklemek için 'Add-AzureRmVMDataDisk' cmdlet’ine VirtualMachineScaleSetVM parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-798">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="aaa79-799">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="aaa79-799">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="aaa79-800">ADF .Net SDK sürümü, aşağıdaki değişiklikleri içeren 0.8.0-preview sürümüne güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="aaa79-800">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="aaa79-801">Fabrika deposunu yapılandırma işlemi eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-801">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="aaa79-802">QuickBooks LinkedService, consumerKey ve consumerSecret özelliklerini kullanıma sunmak üzere güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-802">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="aaa79-803">SecretBase’ten Object’e birkaç model türü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-803">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="aaa79-804">Blob Etkinliklerini tetikleme eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-804">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="aaa79-805">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="aaa79-805">AzureRM.KeyVault</span></span>
* <span data-ttu-id="aaa79-806">Belgeler örnek çıktı ile güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-806">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="aaa79-807">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="aaa79-807">AzureRM.Network</span></span>
* <span data-ttu-id="aaa79-808">Ağ İzleyicisi cmdlet’leri üzerindeki Trafik Analizi parametreleri etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-808">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="aaa79-809">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="aaa79-809">AzureRM.Resources</span></span>
* <span data-ttu-id="aaa79-810">'Get-AzureRmResource' cmdlet’inden döndürülen 'PSResource' nesnesinin 'Properties' özelliğiyle ilgili bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-810">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="aaa79-811">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="aaa79-811">AzureRM.Scheduler</span></span>
* <span data-ttu-id="aaa79-812">Güncelleştirilen ServiceBusQueueJob’ın yeni Kimlik Doğrulaması değerlerini ayarlamamasıyla ilgili bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-812">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="aaa79-813">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="aaa79-813">AzureRM.Sql</span></span>
* <span data-ttu-id="aaa79-814">Şu cmdlet’ler isteğe bağlı LicenseType parametresiyle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="aaa79-814">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="aaa79-815">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="aaa79-815">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="aaa79-816">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="aaa79-816">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="aaa79-817">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="aaa79-817">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="aaa79-818">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="aaa79-818">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="aaa79-819">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="aaa79-819">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="aaa79-820">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="aaa79-820">AzureRM.Websites</span></span>
* <span data-ttu-id="aaa79-821">'New-AzureRMWebApp' Strategy kütüphanesindeki ortak algoritmaları kullanmak üzere güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-821">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="aaa79-822">6.1.0 - Mayıs 2018</span><span class="sxs-lookup"><span data-stu-id="aaa79-822">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="aaa79-823">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="aaa79-823">AzureRM.Profile</span></span>
* <span data-ttu-id="aaa79-824">'Clear-AzureRmContext' komutunun çalıştırılmasının boş bir bağlamı önceki varsayılan bağlamın adıyla tutmasına ve böylece kullanıcının eski ad ile yeni bir bağlam oluşturamadığı bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-824">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="aaa79-825">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="aaa79-825">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="aaa79-826">AS’de Ağ geçidi ilişkilendirme/ilişkilendirme kaldırma işlemlerini etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="aaa79-826">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="aaa79-827">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="aaa79-827">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="aaa79-828">ApiVersions, ApiReleases ve ApiRevisions desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-828">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="aaa79-829">ServiceFabric Arka Ucu desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-829">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="aaa79-830">Application Insights Günlükçüsü desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-830">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="aaa79-831">‘Temel’ sku’yu Api Yönetim hizmetinin geçerli sku’su olarak algılama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-831">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="aaa79-832">Özel CA tarafından Kök veya CA olarak yayınlanan Sertifikaları yükleme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-832">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="aaa79-833">Özel SSL sertifikalarını KeyVault ve Çoklu ara sunucu ana bilgisayar adlarıyla kabul etme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-833">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="aaa79-834">MSI kimliği desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-834">Added support for MSI identity</span></span>
* <span data-ttu-id="aaa79-835">İlkeleri Url ile kabul etme desteği eklendi NOT: Aşağıdaki cmdlet’ler gelecekteki sürümlerde kullanım dışı kalacaktır</span><span class="sxs-lookup"><span data-stu-id="aaa79-835">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="aaa79-836">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="aaa79-836">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="aaa79-837">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="aaa79-837">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="aaa79-838">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="aaa79-838">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="aaa79-839">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="aaa79-839">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="aaa79-840">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="aaa79-840">AzureRM.Batch</span></span>
* <span data-ttu-id="aaa79-841">Yeni Get-AzureBatchPoolNodeCounts cmdlet’ini yayınlama</span><span class="sxs-lookup"><span data-stu-id="aaa79-841">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="aaa79-842">Yeni AzureBatchComputeNodeServiceLogUpload cmdlet’ini yayınlama</span><span class="sxs-lookup"><span data-stu-id="aaa79-842">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="aaa79-843">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="aaa79-843">AzureRM.Consumption</span></span>
* <span data-ttu-id="aaa79-844">Get-AzureRmConsumptionUsageDetail cmdlet’inde yeni Expand, ResourceGroup, InstanceName, InstanceId, Tags ve Top parametrelerini ekleme</span><span class="sxs-lookup"><span data-stu-id="aaa79-844">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="aaa79-845">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="aaa79-845">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="aaa79-846">Export-AzureRmDataLakeStoreChildItemProperties için düzeltme örneği</span><span class="sxs-lookup"><span data-stu-id="aaa79-846">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="aaa79-847">Set-AzureRmDataLakeStoreItemAclEntry komutunda Özyineleme durumu için null parametresi özel durumunu düzeltme</span><span class="sxs-lookup"><span data-stu-id="aaa79-847">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="aaa79-848">Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry’ye yönelik yardım dosyalarını düzeltme</span><span class="sxs-lookup"><span data-stu-id="aaa79-848">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="aaa79-849">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="aaa79-849">AzureRM.Network</span></span>
* <span data-ttu-id="aaa79-850">Ağ SDK sürümünü 18.0.0-önizleme’den 19.0.0-önizlemeye yükseltme</span><span class="sxs-lookup"><span data-stu-id="aaa79-850">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="aaa79-851">Protokol yapılandırması oluşturma cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-851">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="aaa79-852">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="aaa79-852">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="aaa79-853">Varolan express route bağlantı hattına yeni bir bağlantı hattı ekleme cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-853">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="aaa79-854">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="aaa79-854">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="aaa79-855">Varolan express route bağlantı hattındaki bir bağlantı hattı bağlantısını kaldırma cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-855">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="aaa79-856">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="aaa79-856">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="aaa79-857">Bağlantı hattı bağlantısı alma cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="aaa79-857">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="aaa79-858">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="aaa79-858">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="aaa79-859">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="aaa79-859">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="aaa79-860">Oluşturulan sertifikalarla sunucu kimlik doğrulaması kullanımı düzeltildi (Sorun No. 5998)</span><span class="sxs-lookup"><span data-stu-id="aaa79-860">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="aaa79-861">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="aaa79-861">AzureRM.Sql</span></span>
* <span data-ttu-id="aaa79-862">AuditActions veya AuditActionGroups’un kaldırılmasını sağlamak üzere Denetim cmdlet’leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="aaa79-862">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="aaa79-863">Yeni bir esnek saklama ilkesi ayarlarken komutun ‘Azure kurtarma hizmeti kasası ve ilkesiyle uzun süreli saklama ilkesini yapılandırma artık desteklenmiyor. Lütfen yeni esnek saklama ilkesi ile istek gönderin’ hatasını verdiği Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="aaa79-863">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="aaa79-864">komutuna ilişkin sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="aaa79-864">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="aaa79-865">Ölçek ve katman ilişkili özelliklere yönelik Sku özelliğini destekleyen yeni Veritabanı API’sini kullanmak için tüm Azure Sql Database/ElasticPool Creation/Update cmdlet’lerini güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="aaa79-865">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="aaa79-866">Güncelleştirilen cmlet’ler arasında şunlar yer almaktadır:</span><span class="sxs-lookup"><span data-stu-id="aaa79-866">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="aaa79-867">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="aaa79-867">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="aaa79-868">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="aaa79-868">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="aaa79-869">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="aaa79-869">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="aaa79-870">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="aaa79-870">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="aaa79-871">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="aaa79-871">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="aaa79-872">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="aaa79-872">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="aaa79-873">-Name parametresini kullanırken -ResourceGroupName parametresinin gerekli olması için 'Get-AzureRmTrafficManagerProfile'a yönelik parametreleri güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="aaa79-873">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
