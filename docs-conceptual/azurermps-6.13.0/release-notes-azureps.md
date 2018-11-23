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
ms.openlocfilehash: 7f517f0b3768a2075557b131158ee1264ea9ab3f
ms.sourcegitcommit: 80a3da199954d0ab78765715fb49793e89a30f12
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/22/2018
ms.locfileid: "52260002"
---
# <a name="release-notes"></a><span data-ttu-id="bdd48-103">Sürüm notları</span><span class="sxs-lookup"><span data-stu-id="bdd48-103">Release notes</span></span>

<span data-ttu-id="bdd48-104">Azure PowerShell'in bu sürümünde yapılan değişikliklerin listesi aşağıda verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="bdd48-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="6130---november-2018"></a><span data-ttu-id="bdd48-105">6.13.0 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="bdd48-105">6.13.0 - November 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="bdd48-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="bdd48-106">AzureRM.Profile</span></span>
* <span data-ttu-id="bdd48-107">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-107">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="bdd48-108">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="bdd48-108">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="bdd48-109">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="bdd48-109">Update dependencies for type mapping issue</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="bdd48-110">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="bdd48-110">AzureRM.Automation</span></span>
* <span data-ttu-id="bdd48-111">Swagger tabanlı Azure Otomasyon cmdlet'leri</span><span class="sxs-lookup"><span data-stu-id="bdd48-111">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="bdd48-112">Güncelleştirme Yönetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-112">Added Update Management cmdlets</span></span>
* <span data-ttu-id="bdd48-113">Kaynak Denetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-113">Added Source Control cmdlets</span></span>
* <span data-ttu-id="bdd48-114">Remove-AzureRmAutomationHybridWorkerGroup cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-114">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="bdd48-115">DSC Kayıt Düğümü komutu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-115">Fixed the DSC Register Node command</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="bdd48-116">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="bdd48-116">AzureRM.Compute</span></span>
* <span data-ttu-id="bdd48-117">SystemAssigned kimliği için kimlik sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-117">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="bdd48-118">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="bdd48-118">Update dependencies for type mapping issue</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="bdd48-119">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="bdd48-119">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="bdd48-120">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="bdd48-120">Update dependencies for type mapping issue</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="bdd48-121">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="bdd48-121">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="bdd48-122">Market cmdlet'leri için örnekler açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-122">update the examples description for marketplace cmdlets</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="bdd48-123">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="bdd48-123">AzureRM.Network</span></span>
* <span data-ttu-id="bdd48-124">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-124">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="bdd48-125">Desteklenen AzureFirewall Ağ Protokollerine yeniden ICMP eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-125">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="bdd48-126">Test-AzureRmNetworkWatcherConnectivity cmdlet'i güncelleştirildi; hedef kimlik, adres ve bağlantı noktasında doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-126">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="bdd48-127">VirtualNetwork eşlemesinde bellek kullanımıyla ilgili sorunlar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-127">Fix issues with memory usage in VirtualNetwork map</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="bdd48-128">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="bdd48-128">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="bdd48-129">Korumalı dosya paylaşımı için ilke değiştirme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-129">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="bdd48-130">İlke saat dilimi büyük harfe dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="bdd48-130">Converted policy timezone to uppercase.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="bdd48-131">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="bdd48-131">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="bdd48-132">New-AzureRmRecoveryServicesAsrProtectableItem cmdlet'indeki örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-132">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="bdd48-133">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="bdd48-133">Update dependencies for type mapping issue</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="bdd48-134">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="bdd48-134">AzureRM.Relay</span></span>
* <span data-ttu-id="bdd48-135">Kullanıcının New-AzureRmRelayKey cmdlet'ine KeyValue sağlamasına olanak tanıyan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-135">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="bdd48-136">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="bdd48-136">AzureRM.Resources</span></span>
* <span data-ttu-id="bdd48-137">`New-AzureRmPolicyAssignment` ve `Set-AzureRmPolicyAssignment` cmdlet'lerindeki kaynak kimliğiyle ilgili parametrelerin yardım belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-137">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="bdd48-138">New-AzureRmPolicyDefinition cmdlet'ine -Metadata kullanan bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-138">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="bdd48-139">NetStandard'da Tag anahtarında büyük/küçük harf kullanımının korunmasına yönelik düzeltme yapıldı: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="bdd48-139">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="bdd48-140">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="bdd48-140">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="bdd48-141">Hataya neden olan değişiklikler yayınlanacağından kullanımdan kaldırılacak özellikleri belirten iletiler eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-141">Add deprecation messages for upcoming breaking changes</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="bdd48-142">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="bdd48-142">AzureRM.Sql</span></span>
* <span data-ttu-id="bdd48-143">Azure Sql Veritabanı Yönetilen Örneği ve Azure Sql Yönetilen Veritabanı'nındaki CRUD işlemleri için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-143">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="bdd48-144">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="bdd48-144">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="bdd48-145">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="bdd48-145">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="bdd48-146">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="bdd48-146">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="bdd48-147">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="bdd48-147">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="bdd48-148">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="bdd48-148">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="bdd48-149">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="bdd48-149">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="bdd48-150">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="bdd48-150">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="bdd48-151">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="bdd48-151">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="bdd48-152">Sunucuda veya veritabanında Genişletilmiş Denetim İlkesi yönetimi etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-152">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="bdd48-153">Denetim günlüklerinde filtrelemeyi etkinleştirmek için yeni parametre (PredicateExpression) eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-153">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="bdd48-154">Cmdlet'ler, SQL istemcileri yerine Eski istemcileri kullanacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-154">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="bdd48-155">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="bdd48-155">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="bdd48-156">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="bdd48-156">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="bdd48-157">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="bdd48-157">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="bdd48-158">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="bdd48-158">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="bdd48-159">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings cmdlet'inin depolama hesabı ad parametre kümesiyle kullanılmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-159">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="6120---november-2018"></a><span data-ttu-id="bdd48-160">6.12.0 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="bdd48-160">6.12.0 - November 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="bdd48-161">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="bdd48-161">AzureRM.Profile</span></span>
* <span data-ttu-id="bdd48-162">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-162">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="bdd48-163">Connect-AzureRmAccount cmdlet'indeki TenantId parametresi Tenant olarak yeniden adlandırıldı ve TenantId için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-163">Rename param TenantId in cmdlet Connect-AzureRmAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="bdd48-164">Connect-AzureRmAccount için TenantId açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-164">Updated TenantId description for Connect-AzureRmAccount</span></span>
* <span data-ttu-id="bdd48-165">Kiracı etki alanı sağlanırken başarısız oturum açma durumunda gösterilen hata iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-165">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="bdd48-166">Kiracıda abonelikleri olmayan hesaplar için bağlam adı çakışmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-166">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="bdd48-167">MSI kullanırken DataLake uç noktalarıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-167">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="bdd48-168">Bağlantı olmadığında 'Disconnect-AzureRmAccount' oluşturulmasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-168">Fix issue where 'Disconnect-AzureRmAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azurermautomation"></a><span data-ttu-id="bdd48-169">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="bdd48-169">AzureRM.Automation</span></span>
* <span data-ttu-id="bdd48-170">Cmdlet DLL dosya adı Microsoft.Azure.Commands.Automation.dll olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-170">Renamed cmdlet DLL filename to Microsoft.Azure.Commands.Automation.dll</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="bdd48-171">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="bdd48-171">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="bdd48-172">Get-AzureRmCognitiveServicesAccountSkus işlemi eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-172">Add Get-AzureRmCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="bdd48-173">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="bdd48-173">AzureRM.Compute</span></span>
* <span data-ttu-id="bdd48-174">Add-AzureRmVmssVMDataDisk ve Remove-AzureRmVmssVMDataDisk cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-174">Add Add-AzureRmVmssVMDataDisk and Remove-AzureRmVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="bdd48-175">Get-AzureRmVMImage, AutomaticOSUpgradeProperties gösteriyor</span><span class="sxs-lookup"><span data-stu-id="bdd48-175">Get-AzureRmVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="bdd48-176">Json biçiminde SetAzureRmVMChefExtension -BootstrapOptions ve -JsonAttribute seçeneği değerlerinin ayarlanmamasıyla ilgili hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-176">Fixed SetAzureRmVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="bdd48-177">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="bdd48-177">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="bdd48-178">DataLake paketi 1.1.10'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-178">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="bdd48-179">Çok iş parçacıklı işlemlere varsayılan Concurrency değeri eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-179">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="bdd48-180">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="bdd48-180">AzureRM.Insights</span></span>
* <span data-ttu-id="bdd48-181">7267 numaralı (Otomatik ölçeklendirme alanı) sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-181">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="bdd48-182">Yeni otomatik ölçeklendirme kuralı oluşturma sırasında numaralandırılmış parametrelerin düzgün ayarlanmamasıyla ilgili sorunlar (bunlar her zaman varsayılan değere ayarlanıyordu).</span><span class="sxs-lookup"><span data-stu-id="bdd48-182">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="bdd48-183">Set-AzureRMDiagnosticSetting'in ayar oluşturma sırasında kategorilerin açıkça belirtilmesini gerektirmesiyle ilgili 7513 numaralı [Insights] sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-183">Fixed issue #7513 [Insights] Set-AzureRMDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="bdd48-184">Artık cmdlet oluşturma sırasında açık kategori gösteriminin etkinleştirilmesini gerektirmiyor; başka bir deyişle belgelerinde belirtildiği gibi çalışıyor</span><span class="sxs-lookup"><span data-stu-id="bdd48-184">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="bdd48-185">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="bdd48-185">AzureRM.Network</span></span>
* <span data-ttu-id="bdd48-186">Aşağıdaki parametrelerde PeeringType parametresi zorunlu parametre olarak değiştirildi:-</span><span class="sxs-lookup"><span data-stu-id="bdd48-186">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="bdd48-187">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="bdd48-187">Get-AzureRmExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="bdd48-188">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="bdd48-188">Get-AzureRmExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="bdd48-189">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="bdd48-189">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="bdd48-190">Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="bdd48-190">Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="bdd48-191">Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="bdd48-191">Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="bdd48-192">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="bdd48-192">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="bdd48-193">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="bdd48-193">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="bdd48-194">İlke düzeltme cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-194">Added policy remediation cmdlets</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="bdd48-195">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="bdd48-195">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="bdd48-196">Kurtarma hizmetlerinde Azure dosya paylaşımları için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-196">Added support for azure file shares in recovery services.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="bdd48-197">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="bdd48-197">AzureRM.Resources</span></span>
* <span data-ttu-id="bdd48-198">https://github.com/Azure/azure-powershell/issues/7402 düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="bdd48-198">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="bdd48-199">'Get-AzureRmResource' için '-ResourceId' parametresi kullanılarak kaynakların listelenmesine olanak tanındı</span><span class="sxs-lookup"><span data-stu-id="bdd48-199">Allow listing resources using the '-ResourceId' parameter for 'Get-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="bdd48-200">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="bdd48-200">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="bdd48-201">PSServiceBusMigrationConfigurationAttributes'e Geçiş durumunun bilinmesine yardımcı olacak salt okunur MigrationState özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-201">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="bdd48-202">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="bdd48-202">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="bdd48-203">Linux Vmss'ye sertifika ekleme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-203">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="bdd48-204">'Add-AzureRmServiceFabricClusterCertificate' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-204">Fix 'Add-AzureRmServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="bdd48-205">Yeni sertifikadan doğru parmak izi kullanıyor (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="bdd48-205">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="bdd48-206">Özel durum doğru görüntüleniyor (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="bdd48-206">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="bdd48-207">'Update-AzureRmServiceFabricDurability', Vmss CreateOrUpdate işlemini başlatmadan önce küme yapılandırmasını güncelleştirecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-207">Fix 'Update-AzureRmServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="6110---october-2018"></a><span data-ttu-id="bdd48-208">6.11.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="bdd48-208">6.11.0 - October 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="bdd48-209">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="bdd48-209">AzureRM.Profile</span></span>
* <span data-ttu-id="bdd48-210">CloudShell’de Get-AzureRmSubscription sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="bdd48-210">Fix issue with Get-AzureRmSubscription in CloudShell</span></span>
* <span data-ttu-id="bdd48-211">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-211">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="bdd48-212">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="bdd48-212">AzureRM.Backup</span></span>
* <span data-ttu-id="bdd48-213">Azure Backup cmdlet’leri kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="bdd48-213">Deprecated Azure Backup cmdlets.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="bdd48-214">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="bdd48-214">AzureRM.Compute</span></span>
* <span data-ttu-id="bdd48-215">'New-AzureRmVm' için basit parametre kümesi kullanıldığında hızlandırılmış ağların açılacağı VM boyutları beyaz listesine yeni boyutlar eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-215">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzureRmVm'</span></span>
* <span data-ttu-id="bdd48-216">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-216">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="bdd48-217">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="bdd48-217">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="bdd48-218">Sanal Ağ Kuralları desteği ekleme</span><span class="sxs-lookup"><span data-stu-id="bdd48-218">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="bdd48-219">Get-AzureRmDataLakeStoreVirtualNetworkRule: Azure Data Lake Store sanal ağ kuralını alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="bdd48-219">Get-AzureRmDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="bdd48-220">Add-AzureRmDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabına sanal ağ kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="bdd48-220">Add-AzureRmDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="bdd48-221">Set-AzureRmDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabında belirtilen sanal ağ kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="bdd48-221">Set-AzureRmDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="bdd48-222">Remove-AzureRmDataLakeStoreVirtualNetworkRule: Azure Data Lake Store sanal ağ kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="bdd48-222">Remove-AzureRmDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="bdd48-223">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="bdd48-223">AzureRM.Network</span></span>
* <span data-ttu-id="bdd48-224">Test-AzureRmNetworkWatcherConnectivity cmdlet'i güncelleştirildi, arka uca protokol değerini geçiriyor.</span><span class="sxs-lookup"><span data-stu-id="bdd48-224">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="bdd48-225">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-225">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="bdd48-226">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="bdd48-226">AzureRM.Resources</span></span>
* <span data-ttu-id="bdd48-227">Get-AzureRMRoleDefinition cmdlet'inin anlaşılmaz bir özel durum oluşturmasına neden olan hata (varsayılan profilin içinde abonelik olmadığında ve hiçbir kapsam belirtilmediğinde), senaryoya anlamlı bir özel durum eklenerek düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-227">Fix isssue where Get-AzureRMRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="bdd48-228">Ayrıca varsayılan parametre kümesi 'RoleDefinitionNameParameterSet' olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="bdd48-228">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="6100---october-2018"></a><span data-ttu-id="bdd48-229">6.10.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="bdd48-229">6.10.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="bdd48-230">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="bdd48-230">Azure.Storage</span></span>
* <span data-ttu-id="bdd48-231">Hedefte meta veri sorunu olduğunda Fix Copy Blob/File meta verileri kopyalamayacak</span><span class="sxs-lookup"><span data-stu-id="bdd48-231">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="bdd48-232">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="bdd48-232">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="bdd48-233">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="bdd48-233">Start-AzureStorageFileCopy</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="bdd48-234">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="bdd48-234">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="bdd48-235">Mevcut hesap olmadan Get-AzureRmCognitiveServicesAccountSkus desteği.</span><span class="sxs-lookup"><span data-stu-id="bdd48-235">Support Get-AzureRmCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="bdd48-236">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="bdd48-236">AzureRM.Compute</span></span>
* <span data-ttu-id="bdd48-237">Get-AzureRmVM -ResourceGroupName <rg> gerektiğinde 50'den fazla sonuç döndürecek şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-237">Fix Get-AzureRmVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="bdd48-238">New-AzureRmVmss cmdlet'inin yardımına 'SimpleParameterSet' örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-238">Added an example of the 'SimpleParameterSet' to New-AzureRmVmss cmdlet help.</span></span>
* <span data-ttu-id="bdd48-239">Azure Disk Şifrelemesi ilerleme durumu iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-239">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="bdd48-240">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="bdd48-240">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="bdd48-241">ADF .Net SDK sürümü 2.3.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-241">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="bdd48-242">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="bdd48-242">AzureRM.Network</span></span>
* <span data-ttu-id="bdd48-243">NetworkProfile işlevselliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-243">Added NetworkProfile functionality.</span></span> <span data-ttu-id="bdd48-244">yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-244">new cmdlets added</span></span>
    - <span data-ttu-id="bdd48-245">Get-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="bdd48-245">Get-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="bdd48-246">New-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="bdd48-246">New-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="bdd48-247">Remove-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="bdd48-247">Remove-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="bdd48-248">Set-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="bdd48-248">Set-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="bdd48-249">New-AzureRMContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="bdd48-249">New-AzureRMContainerNicConfig</span></span>
    - <span data-ttu-id="bdd48-250">New-AzureRmContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="bdd48-250">New-AzureRmContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="bdd48-251">Alt Ağ Modeline hizmet ilişki bağlantısı eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-251">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="bdd48-252">New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-252">Added cmdlet New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap</span></span>
* <span data-ttu-id="bdd48-253">Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-253">Added cmdlet Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="bdd48-254">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="bdd48-254">AzureRM.RedisCache</span></span>
* <span data-ttu-id="bdd48-255">Bundan sonra Size parametresi olarak her dizeye izin veriliyor.</span><span class="sxs-lookup"><span data-stu-id="bdd48-255">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="bdd48-256">PSArgumentCompleter açılan listesine P5 eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-256">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="bdd48-257">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="bdd48-257">AzureRM.Resources</span></span>
* <span data-ttu-id="bdd48-258">Set-AzureRmPolicyDefinition'a eksik -Mode parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-258">Add missing -Mode parameter to Set-AzureRmPolicyDefinition</span></span>
* <span data-ttu-id="bdd48-259">Origin öğesi User içeren işlemler için Get-AzureRmProviderOperation commandlet hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-259">Fix Get-AzureRmProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="bdd48-260">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="bdd48-260">AzureRM.Sql</span></span>
* <span data-ttu-id="bdd48-261">Bazı yedekleme cmdlet'lerinin geçerli Azure aboneliğini tanıyamamasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-261">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="bdd48-262">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="bdd48-262">AzureRM.Storage</span></span>
* <span data-ttu-id="bdd48-263">Belirli bir konumunun Depolama kaynağı kullanımını alma desteği ve genel Depolama kayrağı kullanımını almak için uyarı iletisi ekleme kullanımdan kalktı.</span><span class="sxs-lookup"><span data-stu-id="bdd48-263">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="bdd48-264">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="bdd48-264">Get-AzureRmStorageUsage</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="bdd48-265">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="bdd48-265">AzureRM.Websites</span></span>
* <span data-ttu-id="bdd48-266">Yeni Get-AzureRMWebAppContainerContinuousDeploymentUrl Cmdlet'i - Kapsayıcı Sürekli Dağıtım Web Kancası URL'sini alıyor</span><span class="sxs-lookup"><span data-stu-id="bdd48-266">New Cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="bdd48-267">Yeni New-AzureRMWebAppContainerPSSession ve Enter-WebAppContainerPSSession Cmdlet'leri - Windows kapsayıcı uygulamasında PowerShell uzak oturumunu başlatıyor</span><span class="sxs-lookup"><span data-stu-id="bdd48-267">New Cmdlets New-AzureRMWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="690---september-2018"></a><span data-ttu-id="bdd48-268">6.9.0 - Eylül 2018</span><span class="sxs-lookup"><span data-stu-id="bdd48-268">6.9.0 - September 2018</span></span>
#### <a name="general"></a><span data-ttu-id="bdd48-269">Genel</span><span class="sxs-lookup"><span data-stu-id="bdd48-269">General</span></span>
* <span data-ttu-id="bdd48-270">AzureRM.SignalR, AzureRM toplu modülüne eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-270">AzureRM.SignalR was added to the AzureRM rollup module</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="bdd48-271">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="bdd48-271">AzureRM.Profile</span></span>
* <span data-ttu-id="bdd48-272">Depolama ortak kodunda küçük değişiklikler yapıldı</span><span class="sxs-lookup"><span data-stu-id="bdd48-272">Minor changes to the storage common code</span></span>
* <span data-ttu-id="bdd48-273">Yardım dosyaları tüm parametre türlerini içerecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-273">Updated help files to include full parameter types.</span></span>
* <span data-ttu-id="bdd48-274">ServicePrincipalCertificateWithSubscriptionId parametre kümesindeki -ServicePrincipal parametresi zorunlu olmaktan çıkarıldı</span><span class="sxs-lookup"><span data-stu-id="bdd48-274">Changed -ServicePrincipal to non-mandatory in the ServicePrincipalCertificateWithSubscriptionId parameter set</span></span> 

#### <a name="azurestorage"></a><span data-ttu-id="bdd48-275">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="bdd48-275">Azure.Storage</span></span>
* <span data-ttu-id="bdd48-276">OAuth ile Depolama Bağlamı oluşturma desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-276">Support create Storage Context with OAuth.</span></span> 
    - <span data-ttu-id="bdd48-277">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="bdd48-277">New-AzureStorageContext</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="bdd48-278">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="bdd48-278">AzureRM.Cdn</span></span>
* <span data-ttu-id="bdd48-279">CDN fiyatlandırma SKU'suna Standard_Microsoft eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-279">Added Standard_Microsoft in Cdn pricing sku.</span></span> 

#### <a name="azurermcompute"></a><span data-ttu-id="bdd48-280">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="bdd48-280">AzureRM.Compute</span></span>
* <span data-ttu-id="bdd48-281">Keyvault ve Storage bağımlılıkları ortak bağımlılıklara taşındı</span><span class="sxs-lookup"><span data-stu-id="bdd48-281">Move dependencies on Keyvault and Storage to the common dependencies</span></span>
* <span data-ttu-id="bdd48-282">AEM cmdlet'lerine daha fazla sanal makine boyutu için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-282">Add support for more virutal machine sizes to AEM cmdlets</span></span>
* <span data-ttu-id="bdd48-283">New-AzureRmVmssIpConfig cmdlet'ine Add PublicIPPrefix parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-283">Add PublicIPPrefix parameter to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="bdd48-284">Invoke-AzureRmVMRunCommand cmdlet'ine ResourceId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-284">Add ResourceId parameter to Invoke-AzureRmVMRunCommand cmdelt</span></span>
* <span data-ttu-id="bdd48-285">Invoke-AzureRmVmssVMRunCommand cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-285">Add Invoke-AzureRmVmssVMRunCommand cmdlet</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="bdd48-286">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="bdd48-286">AzureRM.Dns</span></span>
* <span data-ttu-id="bdd48-287">DNS kaydı oluşturma işlemi sırasında diğer ad kaydı desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-287">Added support for alias record during dns record creation</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="bdd48-288">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="bdd48-288">AzureRM.Insights</span></span>
* <span data-ttu-id="bdd48-289">6833 ve 7102 numaralı sorunlar giderildi (Tanılama Ayarları bölümü)</span><span class="sxs-lookup"><span data-stu-id="bdd48-289">Fixed issues #6833 and #7102 (Diagnostic Settings area)</span></span>
    - <span data-ttu-id="bdd48-290">Tanılama ayarlarını oluşturma ve listeleme/alma sırasında karşılaşılan varsayılan ad 'service' sorunları</span><span class="sxs-lookup"><span data-stu-id="bdd48-290">Issues with the default name, i.e. 'service', during creation and listing/getting of diagnostic settings</span></span>
    - <span data-ttu-id="bdd48-291">Kategoriye sahip tanılama ayarı oluşturma sorunları</span><span class="sxs-lookup"><span data-stu-id="bdd48-291">Issues creating diagnostic settings with categories</span></span>
* <span data-ttu-id="bdd48-292">Ölçümler zaman dilimi parametreleri için kullanımdan kaldırma iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-292">Added deprecation message for metrics time grains parameters</span></span>
    - <span data-ttu-id="bdd48-293">Zaman dilimi parametreleri yine kabul ediliyor (bu bir hataya neden olan değişiklik değil) ancak yalnızca PT1M geçerli olduğu için bu parametreler arka uçta yoksayılıyor</span><span class="sxs-lookup"><span data-stu-id="bdd48-293">Timegrains parameters are still being accepted (this is a non-breaking change,) but they are ignored in the backend since only PT1M is valid</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="bdd48-294">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="bdd48-294">AzureRM.Network</span></span>
* <span data-ttu-id="bdd48-295">LoadBalancer cmdlet'lerinde değişiklikler yapıldı</span><span class="sxs-lookup"><span data-stu-id="bdd48-295">Changes to LoadBalancer cmdlets</span></span>
  - <span data-ttu-id="bdd48-296">LoadBalancerInboundNatPoolConfig: IdleTimeoutInMinutes, EnableFloatingIp ve EnableTcpReset parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-296">LoadBalancerInboundNatPoolConfig: added parameters IdleTimeoutInMinutes, EnableFloatingIp and EnableTcpReset</span></span>
  - <span data-ttu-id="bdd48-297">LoadBalancerInboundNatRuleConfig: EnableTcpReset parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-297">LoadBalancerInboundNatRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="bdd48-298">LoadBalancerRuleConfig: EnableTcpReset parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-298">LoadBalancerRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="bdd48-299">LoadBalancerProbeConfig: Protocol parametresi için "Https" değeri desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-299">LoadBalancerProbeConfig: added support for value "Https" for parameter Protocol</span></span>
* <span data-ttu-id="bdd48-300">Yeni LoadBalancer alt kaynağı OutboundRule için yeni komutlar eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-300">Added new commands for new LoadBalancer's subresource OutboundRule</span></span>
  - <span data-ttu-id="bdd48-301">Add-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bdd48-301">Add-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="bdd48-302">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bdd48-302">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="bdd48-303">New-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bdd48-303">New-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="bdd48-304">Set-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bdd48-304">Set-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="bdd48-305">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bdd48-305">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>
* <span data-ttu-id="bdd48-306">PSNetworkInterface için yeni HostedWorkloads özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-306">Added new HostedWorkloads property for PSNetworkInterface</span></span>
* <span data-ttu-id="bdd48-307">ARM aracılığıyla Azure Güvenlik Duvarı özelliği için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-307">Added new cmdlets for feature: Azure Firewall via ARM</span></span>
  - <span data-ttu-id="bdd48-308">Get-AzureRmFirewall eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-308">Added Get-AzureRmFirewall</span></span>
  - <span data-ttu-id="bdd48-309">Set-AzureRmFirewall eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-309">Added Set-AzureRmFirewall</span></span>
  - <span data-ttu-id="bdd48-310">New-AzureRmFirewall eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-310">Added New-AzureRmFirewall</span></span>
  - <span data-ttu-id="bdd48-311">Remove-AzureRmFirewall eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-311">Added Remove-AzureRmFirewall</span></span>
  - <span data-ttu-id="bdd48-312">New-AzureRmFirewallApplicationRuleCollection eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-312">Added New-AzureRmFirewallApplicationRuleCollection</span></span>
  - <span data-ttu-id="bdd48-313">New-AzureRmFirewallApplicationRule eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-313">Added New-AzureRmFirewallApplicationRule</span></span>
  - <span data-ttu-id="bdd48-314">New-AzureRmFirewallNatRuleCollection eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-314">Added New-AzureRmFirewallNatRuleCollection</span></span>
  - <span data-ttu-id="bdd48-315">New-AzureRmFirewallNatRule eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-315">Added New-AzureRmFirewallNatRule</span></span>
  - <span data-ttu-id="bdd48-316">New-AzureRmFirewallNetworkRuleCollection eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-316">Added New-AzureRmFirewallNetworkRuleCollection</span></span>
  - <span data-ttu-id="bdd48-317">New-AzureRmFirewallNetworkRule eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-317">Added New-AzureRmFirewallNetworkRule</span></span>
* <span data-ttu-id="bdd48-318">Application Gateway'de Güvenilen Kök sertifika ve Otomatik ölçeklendirme yapılandırması desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-318">Added support for Trusted Root certificate and Autoscale configuration in Application Gateway</span></span>
  - <span data-ttu-id="bdd48-319">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="bdd48-319">New Cmdlets added:</span></span>
      - <span data-ttu-id="bdd48-320">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="bdd48-320">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="bdd48-321">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="bdd48-321">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="bdd48-322">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="bdd48-322">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="bdd48-323">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="bdd48-323">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="bdd48-324">Set-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="bdd48-324">Set-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="bdd48-325">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="bdd48-325">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="bdd48-326">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="bdd48-326">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="bdd48-327">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="bdd48-327">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="bdd48-328">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="bdd48-328">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
  - <span data-ttu-id="bdd48-329">Cmdlet'ler isteğe bağlı -TrustedRootCertificate parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-329">Cmdlets updated with optonal parameter -TrustedRootCertificate</span></span>
      - <span data-ttu-id="bdd48-330">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bdd48-330">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="bdd48-331">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bdd48-331">Set-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="bdd48-332">New-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="bdd48-332">New-AzureRmApplicationGatewayBackendHttpSetting</span></span>
      - <span data-ttu-id="bdd48-333">Set-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="bdd48-333">Set-AzureRmApplicationGatewayBackendHttpSetting</span></span>
  - <span data-ttu-id="bdd48-334">Cmdlet'ler isteğe bağlı -AutoscaleConfiguration parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-334">Cmdlets updated with optonal parameter -AutoscaleConfiguration</span></span>
      - <span data-ttu-id="bdd48-335">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bdd48-335">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="bdd48-336">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bdd48-336">Set-AzureRmApplicationGateway</span></span>
* <span data-ttu-id="bdd48-337">Arabirim Uç Noktası için Get-AzureInterfaceEndpoint cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-337">Add cmdlet for Interface Endpoint Get-AzureInterfaceEndpoint</span></span>
* <span data-ttu-id="bdd48-338">Bir alt ağda birden fazla adres ön eki için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-338">Added support for multiple address prefixes in a subnet.</span></span> <span data-ttu-id="bdd48-339">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="bdd48-339">Updated cmdlets:</span></span>
  - <span data-ttu-id="bdd48-340">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="bdd48-340">New-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="bdd48-341">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="bdd48-341">Set-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="bdd48-342">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="bdd48-342">Add-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="bdd48-343">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="bdd48-343">Get-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="bdd48-344">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="bdd48-344">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>
  - <span data-ttu-id="bdd48-345">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="bdd48-345">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="bdd48-346">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="bdd48-346">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="bdd48-347">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="bdd48-347">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="bdd48-348">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="bdd48-348">Add-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="bdd48-349">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="bdd48-349">New-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="bdd48-350">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="bdd48-350">Set-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="bdd48-351">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="bdd48-351">Add-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="bdd48-352">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="bdd48-352">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="bdd48-353">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="bdd48-353">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="bdd48-354">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="bdd48-354">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="bdd48-355">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="bdd48-355">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="bdd48-356">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="bdd48-356">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="bdd48-357">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="bdd48-357">New-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="bdd48-358">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="bdd48-358">New-AzureRmNetworkInterface</span></span>
* <span data-ttu-id="bdd48-359">Alt ağ temsilcisi seçme cmdlet'leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-359">Adding cmdlets for subnet delegation.</span></span>
  - <span data-ttu-id="bdd48-360">New-AzureRmDelegation: Bir alt ağa eklenebilecek yeni bir temsilci oluşturur</span><span class="sxs-lookup"><span data-stu-id="bdd48-360">New-AzureRmDelegation: Creates a new delegation, which can be added to a subnet</span></span>
  - <span data-ttu-id="bdd48-361">Remove-AzureRmDelegation: Bir alt ağı alır ve belirtilen temsilci adını o alt ağdan kaldırır</span><span class="sxs-lookup"><span data-stu-id="bdd48-361">Remove-AzureRmDelegation: Takes in a subnet and removes the provided delegation name from that subnet</span></span>
  - <span data-ttu-id="bdd48-362">Add-AzureRmDelegation: Bir alt ağı alır ve belirtilen hizmet adını o alt ağa temsilci olarak ekler</span><span class="sxs-lookup"><span data-stu-id="bdd48-362">Add-AzureRmDelegation: Takes in a subnet and adds the provided service name as a delegation to that subnet</span></span>
  - <span data-ttu-id="bdd48-363">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="bdd48-363">Get-AzureRmDelegation</span></span>
  - <span data-ttu-id="bdd48-364">Get-AzureRmAvailableServiceDelegations</span><span class="sxs-lookup"><span data-stu-id="bdd48-364">Get-AzureRmAvailableServiceDelegations</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="bdd48-365">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="bdd48-365">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="bdd48-366">Yönetilen disk desteği</span><span class="sxs-lookup"><span data-stu-id="bdd48-366">Support for managed Managed disk</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="bdd48-367">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="bdd48-367">AzureRM.RedisCache</span></span>
* <span data-ttu-id="bdd48-368">Insights bağımlılığı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-368">Updated Insights dependency.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="bdd48-369">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="bdd48-369">AzureRM.Resources</span></span>
* <span data-ttu-id="bdd48-370">New-AzureRmResourceGroupDeployment cmdlet'i yeni RollbackAction parametresi eklenerek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-370">Update New-AzureRmResourceGroupDeployment with new parameter RollbackAction</span></span>
    - <span data-ttu-id="bdd48-371">Yeni parametreyle OnErrorDeployment desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-371">Add support for OnErrorDeployment with the new parameter.</span></span>
* <span data-ttu-id="bdd48-372">İlke atamalarında yönetilen kimlik desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-372">Support managed identity on policy assignments.</span></span>
* <span data-ttu-id="bdd48-373">Varsayılan değerlere sahip parametrelerin artık 'New-AzureRmPolicyAssignment' ile ilke atama işlemi sırasında belirtilmesi zorunlu değil</span><span class="sxs-lookup"><span data-stu-id="bdd48-373">Parameters with default values are no longer requred when assigning a policy with 'New-AzureRmPolicyAssignment'</span></span>
* <span data-ttu-id="bdd48-374">İlke diğer adlarını almak için yeni Get-AzureRmPolicyAlias cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-374">Add new cmdlet Get-AzureRmPolicyAlias for retrieving policy aliases</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="bdd48-375">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="bdd48-375">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="bdd48-376">7161 numaralı sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-376">Fixed issue #7161</span></span>

#### <a name="azurermsignalr"></a><span data-ttu-id="bdd48-377">AzureRM.SignalR</span><span class="sxs-lookup"><span data-stu-id="bdd48-377">AzureRM.SignalR</span></span>
* <span data-ttu-id="bdd48-378">SKU adları Free_F1 ve Standard_S1 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-378">Update SKU names to Free_F1 and Standard_S1</span></span>
* <span data-ttu-id="bdd48-379">PSSignalRResource nesnesine sürüm alanı, PSSignalRKeys nesnesine de bağlantı dizesi eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-379">Add version field to the PSSignalRResource object and connection string to the PSSignalRKeys object.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="bdd48-380">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="bdd48-380">AzureRM.Storage</span></span>
* <span data-ttu-id="bdd48-381">AzureRm.Storage için Değiştirilemezlik İlkesi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-381">Support Immutability Policy in AzureRm.Storage</span></span> 
    - <span data-ttu-id="bdd48-382">Remove-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="bdd48-382">Remove-AzureRmStorageAccountNetworkRule</span></span>
    - <span data-ttu-id="bdd48-383">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="bdd48-383">Get-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="bdd48-384">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="bdd48-384">Update-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="bdd48-385">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="bdd48-385">New-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="bdd48-386">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="bdd48-386">Remove-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="bdd48-387">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="bdd48-387">Add-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="bdd48-388">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="bdd48-388">Remove-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="bdd48-389">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="bdd48-389">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="bdd48-390">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="bdd48-390">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="bdd48-391">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="bdd48-391">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="bdd48-392">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="bdd48-392">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="bdd48-393">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="bdd48-393">AzureRM.Websites</span></span>
* <span data-ttu-id="bdd48-394">İki yeni cmdlet eklendi: Get-AzureRmDeletedWebApp ve Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="bdd48-394">Added two new cmdlets: Get-AzureRmDeletedWebApp and Restore-AzureRmDeletedWebApp</span></span>
* <span data-ttu-id="bdd48-395">Windows kapsayıcısı ile App Service planı oluşturmak için New-AzureRmAppServicePlan -HyperV anahtarı eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-395">New-AzureRmAppServicePlan -HyperV switch is added for create app service plan with windows container</span></span>
* <span data-ttu-id="bdd48-396">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - Windows kapsayıcı uygulaması oluşturmak ve yönetmek için yeni parametreler (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-396">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - New parameters (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) added for creating and managing windows container app</span></span>

## <a name="681---august-2018"></a><span data-ttu-id="bdd48-397">6.8.1 - Ağustos 2018</span><span class="sxs-lookup"><span data-stu-id="bdd48-397">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="bdd48-398">Genel</span><span class="sxs-lookup"><span data-stu-id="bdd48-398">General</span></span>
* <span data-ttu-id="bdd48-399">Varsayılan kaynak gruplarının ayarlanmamasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-399">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="bdd48-400">Ortak çalışma zamanı bütünleştirilmiş kodları güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-400">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="bdd48-401">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="bdd48-401">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="bdd48-402">Varsayılan kaynak gruplarının ayarlanmamasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-402">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="bdd48-403">https://github.com/Azure/azure-powershell/issues/6603 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-403">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="bdd48-404">Import-AzureRmApiManagementApi ve \*-AzureRmApiManagementCertificate cmdlet’leri artık göreli yolları işleyebiliyor</span><span class="sxs-lookup"><span data-stu-id="bdd48-404">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="bdd48-405">https://github.com/Azure/azure-powershell/issues/6879 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-405">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="bdd48-406">CertificateInformation, Set-AzureRmApiManagement cmdlet’inin düzgün çalışmasını sağlayan, ayarlanabilir bir özelliktir.</span><span class="sxs-lookup"><span data-stu-id="bdd48-406">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="bdd48-407">4.0.4-preview nuget’e yükselterek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-407">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="bdd48-408">https://github.com/Azure/azure-powershell/issues/6853 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-408">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="bdd48-409">Odata filtresi Ürün üzerinde Ada Göre Arama için düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-409">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="bdd48-410">https://github.com/Azure/azure-powershell/issues/6814 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-410">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="bdd48-411">Odata filtresi API üzerinde Ada Göre Arama için düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-411">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="bdd48-412">Azure İzleyici günlükçüsüne yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-412">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="bdd48-413">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="bdd48-413">AzureRM.Compute</span></span>
* <span data-ttu-id="bdd48-414">Hata çıktısında hedefin eksik olmasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-414">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="bdd48-415">Yönetilen diske sahip VM için depolama hesabı türüyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-415">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="bdd48-416">Varsayılan kaynak gruplarının ayarlanmamasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-416">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="bdd48-417">Azure Çin gibi diğer ortamlar için AEM Uzantı cmdlet'leri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-417">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="bdd48-418">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="bdd48-418">AzureRM.Network</span></span>
* <span data-ttu-id="bdd48-419">Varsayılan cmdlet çıkış gösterimi, tablo görünümü olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-419">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="bdd48-420">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="bdd48-420">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="bdd48-421">Duraklatılmış kapasite ölçeklendirilmeye çalışılırken Update-AzureRmPowerBIEmbeddedCapacity üzerindeki hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-421">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="bdd48-422">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="bdd48-422">AzureRM.Resources</span></span>
* <span data-ttu-id="bdd48-423">Market’ten yönetilen uygulama oluşturmayla ilgili sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-423">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="bdd48-424">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="bdd48-424">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="bdd48-425">Düzeltilen sorunlar</span><span class="sxs-lookup"><span data-stu-id="bdd48-425">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="bdd48-426">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="bdd48-426">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="bdd48-427">Çoklu değer yönlendirme yöntemi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-427">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="bdd48-428">Çoklu değer yönlendirme için yeni 'MaxReturn' parametresi</span><span class="sxs-lookup"><span data-stu-id="bdd48-428">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="bdd48-429">Alt ağ yönlendirme yöntemi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-429">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="bdd48-430">Uç noktalarda IP adresi aralıkları (alt ağları) desteği</span><span class="sxs-lookup"><span data-stu-id="bdd48-430">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="bdd48-431">Profillerde Özel Üst Bilgi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-431">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="bdd48-432">Profillerde Beklenen durum kodu aralığı desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-432">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="bdd48-433">Uç noktalarda Özel Üst Bilgi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-433">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="bdd48-434">6.8.0 - Ağustos 2018</span><span class="sxs-lookup"><span data-stu-id="bdd48-434">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="bdd48-435">Genel</span><span class="sxs-lookup"><span data-stu-id="bdd48-435">General</span></span>
* <span data-ttu-id="bdd48-436">Varsayılan kaynak gruplarının ayarlanmamasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-436">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="bdd48-437">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="bdd48-437">AzureRM.Profile</span></span>
* <span data-ttu-id="bdd48-438">Connect-AzureRmAccount sırasında döndürülen belirteçlere sona erme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-438">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="bdd48-439">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="bdd48-439">AzureRM.Compute</span></span>
* <span data-ttu-id="bdd48-440">Hata çıktısında hedefin eksik olmasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-440">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="bdd48-441">Yönetilen diske sahip VM için depolama hesabı türüyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-441">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="bdd48-442">Azure Çin gibi diğer ortamlar için AEM Uzantı cmdlet'leri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-442">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="bdd48-443">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="bdd48-443">AzureRM.IotHub</span></span>
* <span data-ttu-id="bdd48-444">New-AzureRmIotHubExportDevices ve New-AzureRmIotHubImportDevices için düzeltme örnekleri</span><span class="sxs-lookup"><span data-stu-id="bdd48-444">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="bdd48-445">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="bdd48-445">AzureRM.Network</span></span>
* <span data-ttu-id="bdd48-446">Varsayılan model gösterimi tablo görünümü olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-446">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="bdd48-447">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="bdd48-447">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="bdd48-448">Duraklatılmış kapasite ölçeklendirilmeye çalışılırken Update-AzureRmPowerBIEmbeddedCapacity üzerindeki hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-448">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="bdd48-449">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="bdd48-449">AzureRM.Resources</span></span>
* <span data-ttu-id="bdd48-450">Marketten yönetilen uygulamayla ilgili sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-450">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="bdd48-451">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="bdd48-451">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="bdd48-452">Sorunlar için düzeltme</span><span class="sxs-lookup"><span data-stu-id="bdd48-452">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="bdd48-453">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="bdd48-453">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="bdd48-454">Çoklu değer yönlendirme yöntemi desteği</span><span class="sxs-lookup"><span data-stu-id="bdd48-454">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="bdd48-455">Çoklu değer yönlendirme için yeni 'MaxReturn' parametresi</span><span class="sxs-lookup"><span data-stu-id="bdd48-455">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="bdd48-456">Alt ağ yönlendirme yöntemi desteği</span><span class="sxs-lookup"><span data-stu-id="bdd48-456">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="bdd48-457">Uç noktalarda IP adresi aralıkları (alt ağları) desteği</span><span class="sxs-lookup"><span data-stu-id="bdd48-457">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="bdd48-458">Profillerde Özel Üst Bilgi desteği</span><span class="sxs-lookup"><span data-stu-id="bdd48-458">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="bdd48-459">Profillerde Beklenen durum kodu aralığı desteği</span><span class="sxs-lookup"><span data-stu-id="bdd48-459">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="bdd48-460">Uç noktalarda Özel Üst Bilgi desteği</span><span class="sxs-lookup"><span data-stu-id="bdd48-460">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="bdd48-461">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="bdd48-461">AzureRM.Websites</span></span>
* <span data-ttu-id="bdd48-462">Varsayılan kaynak gruplarının yanlış ayarlanmasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-462">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="bdd48-463">6.7.0 - Ağustos 2018</span><span class="sxs-lookup"><span data-stu-id="bdd48-463">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="bdd48-464">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="bdd48-464">AzureRM.Profile</span></span>
* <span data-ttu-id="bdd48-465">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-465">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="bdd48-466">Bağlam çakışmasını önlemek için varsayılan bağlam adına kullanıcı kimliği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-466">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="bdd48-467">Bağlam #6398 seçerken sorunlara neden olan Clear-AzureRmContext ile ilgili sorunlar giderildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-467">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="bdd48-468">'Connect-AzureRmAccount' için kiracı etki alanının '-TenantId' parametresine geçirilmesi etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-468">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="bdd48-469">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="bdd48-469">Azure.Storage</span></span>
* <span data-ttu-id="bdd48-470">Azure Dosya Paylaşımı kotasındaki 5 TB'lık sınır kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="bdd48-470">Remove the 5TB limitation for Azure File Share quota</span></span>
* <span data-ttu-id="bdd48-471">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="bdd48-471">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="bdd48-472">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="bdd48-472">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="bdd48-473">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-473">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="bdd48-474">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="bdd48-474">Azure.AnalysisServices</span></span>
* <span data-ttu-id="bdd48-475">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-475">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="bdd48-476">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="bdd48-476">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="bdd48-477">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-477">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="bdd48-478">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="bdd48-478">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="bdd48-479">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-479">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="bdd48-480">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="bdd48-480">AzureRM.Automation</span></span>
* <span data-ttu-id="bdd48-481">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-481">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="bdd48-482">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="bdd48-482">AzureRM.Backup</span></span>
* <span data-ttu-id="bdd48-483">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-483">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="bdd48-484">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="bdd48-484">AzureRM.Batch</span></span>
* <span data-ttu-id="bdd48-485">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-485">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="bdd48-486">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="bdd48-486">AzureRM.Billing</span></span>
* <span data-ttu-id="bdd48-487">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-487">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="bdd48-488">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="bdd48-488">AzureRM.Cdn</span></span>
* <span data-ttu-id="bdd48-489">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-489">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="bdd48-490">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="bdd48-490">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="bdd48-491">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-491">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="bdd48-492">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="bdd48-492">AzureRM.Compute</span></span>
* <span data-ttu-id="bdd48-493">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-493">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="bdd48-494">New-AzureRmVmssConfig’e EvictionPolicy parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-494">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="bdd48-495">Hiçbir konum belirtilmediyse New-AzureRmVm’nin DiskFileParameterSet parametresinde varsayılan konum kullanılıyor.</span><span class="sxs-lookup"><span data-stu-id="bdd48-495">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="bdd48-496">Save-AzureRmVMImage cmdlet'inde parametre açıklaması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-496">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="bdd48-497">Singlepass ile ilgili bazı senaryolarda Get-AzureRmVMDiskEncryptionStatus cmdlet’i düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-497">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="bdd48-498">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="bdd48-498">AzureRM.Consumption</span></span>
* <span data-ttu-id="bdd48-499">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-499">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="bdd48-500">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="bdd48-500">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="bdd48-501">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-501">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="bdd48-502">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="bdd48-502">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="bdd48-503">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-503">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="bdd48-504">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="bdd48-504">AzureRM.DataFactories</span></span>
* <span data-ttu-id="bdd48-505">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-505">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="bdd48-506">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="bdd48-506">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="bdd48-507">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-507">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="bdd48-508">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="bdd48-508">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="bdd48-509">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-509">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="bdd48-510">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="bdd48-510">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="bdd48-511">DebugPreference Powershell komut satırından ayarlandığında hata ayıklama düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-511">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="bdd48-512">Set-AzureRmDataLakeStoreItemAcl örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-512">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="bdd48-513">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-513">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="bdd48-514">Set-AzureRmDataLakeStoreItemAclEntry örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-514">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="bdd48-515">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="bdd48-515">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="bdd48-516">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-516">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="bdd48-517">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="bdd48-517">AzureRM.Dns</span></span>
* <span data-ttu-id="bdd48-518">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-518">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="bdd48-519">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="bdd48-519">AzureRM.EventGrid</span></span>
* <span data-ttu-id="bdd48-520">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-520">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="bdd48-521">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="bdd48-521">AzureRM.EventHub</span></span>
* <span data-ttu-id="bdd48-522">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-522">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="bdd48-523">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="bdd48-523">AzureRM.HDInsight</span></span>
* <span data-ttu-id="bdd48-524">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-524">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="bdd48-525">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="bdd48-525">AzureRM.Insights</span></span>
* <span data-ttu-id="bdd48-526">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-526">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="bdd48-527">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="bdd48-527">AzureRM.IotHub</span></span>
* <span data-ttu-id="bdd48-528">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-528">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="bdd48-529">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="bdd48-529">AzureRM.KeyVault</span></span>
* <span data-ttu-id="bdd48-530">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-530">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="bdd48-531">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="bdd48-531">AzureRM.LogicApp</span></span>
* <span data-ttu-id="bdd48-532">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-532">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="bdd48-533">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="bdd48-533">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="bdd48-534">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-534">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="bdd48-535">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="bdd48-535">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="bdd48-536">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-536">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="bdd48-537">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="bdd48-537">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="bdd48-538">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-538">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="bdd48-539">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="bdd48-539">AzureRM.Media</span></span>
* <span data-ttu-id="bdd48-540">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-540">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="bdd48-541">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="bdd48-541">AzureRM.Network</span></span>
* <span data-ttu-id="bdd48-542">Set-AzureRmLocalNetworkGateway örneği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-542">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="bdd48-543">Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey ve New-AzureRmVirtualNetworkGatewayConnection için örnek ve açıklamalar eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-543">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="bdd48-544">Remove-AzureRmVirtualNetworkGatewayIpConfig ve Reset-AzureRmVirtualNetworkGateway örnekleri eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-544">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="bdd48-545">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey örneği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-545">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="bdd48-546">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey örneği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-546">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="bdd48-547">Set-AzureRmVirtualNetworkGatewayConnection örneği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-547">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="bdd48-548">ApplicationSecurityGroup, RouteTable ve Usage için en son kod oluşturucu kullanılarak cmdlet’ler yeniden oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="bdd48-548">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="bdd48-549">Varolmayan bir alt ağ alma girişiminde bulunulduğunda Get-AzureRmVirtualNetworkSubnetConfig cmdlet'inin hata iletisi netleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-549">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="bdd48-550">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="bdd48-550">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="bdd48-551">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-551">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="bdd48-552">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="bdd48-552">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="bdd48-553">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-553">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="bdd48-554">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="bdd48-554">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="bdd48-555">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-555">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="bdd48-556">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="bdd48-556">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="bdd48-557">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-557">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="bdd48-558">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bdd48-558">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="bdd48-559">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-559">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="bdd48-560">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="bdd48-560">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="bdd48-561">Get-AzureRmRecoveryServicesBackItem cmdlet’ine ilke filtresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-561">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="bdd48-562">Komut, verilen ilke kimliği tarafından korunan yedekleme öğelerinin listesini döndürüyor.</span><span class="sxs-lookup"><span data-stu-id="bdd48-562">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="bdd48-563">Microsoft.Azure.Management.RecoveryServices.Backup, sürüm 3.0.0 önizlemesine güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-563">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="bdd48-564">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-564">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="bdd48-565">Restore-AzureRmRecoveryServicesBackupItem’e TargetResourceGroupName parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-565">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="bdd48-566">Yönetilen disklerin geri yüklendiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="bdd48-566">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="bdd48-567">Yönetilen disklerle yapılan VM yedeklemesi için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="bdd48-567">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="bdd48-568">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="bdd48-568">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="bdd48-569">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-569">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="bdd48-570">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="bdd48-570">AzureRM.RedisCache</span></span>
* <span data-ttu-id="bdd48-571">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-571">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="bdd48-572">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="bdd48-572">AzureRM.Relay</span></span>
* <span data-ttu-id="bdd48-573">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-573">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="bdd48-574">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="bdd48-574">AzureRM.Resources</span></span>
* <span data-ttu-id="bdd48-575">Abonelik kapsamındaki şablon dağıtımı destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="bdd48-575">Support template deployment at subscription scope.</span></span> <span data-ttu-id="bdd48-576">Yeni Cmdlet’ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="bdd48-576">Add new Cmdlets:</span></span>
    - <span data-ttu-id="bdd48-577">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="bdd48-577">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="bdd48-578">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="bdd48-578">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="bdd48-579">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="bdd48-579">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="bdd48-580">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="bdd48-580">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="bdd48-581">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="bdd48-581">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="bdd48-582">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="bdd48-582">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="bdd48-583">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="bdd48-583">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="bdd48-584">Set-AzureRmResource’a bağlam geçirilirken hata oluşmasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-584">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="bdd48-585">New-AzureRmResourceGroupDeployment cmdlet'indeki örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-585">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="bdd48-586">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-586">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="bdd48-587">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="bdd48-587">AzureRM.Scheduler</span></span>
* <span data-ttu-id="bdd48-588">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-588">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="bdd48-589">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="bdd48-589">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="bdd48-590">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-590">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="bdd48-591">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="bdd48-591">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="bdd48-592">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-592">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="bdd48-593">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="bdd48-593">AzureRM.Sql</span></span>
* <span data-ttu-id="bdd48-594">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-594">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="bdd48-595">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="bdd48-595">AzureRM.Storage</span></span>
* <span data-ttu-id="bdd48-596">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-596">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="bdd48-597">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="bdd48-597">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="bdd48-598">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-598">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="bdd48-599">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="bdd48-599">AzureRM.Tags</span></span>
* <span data-ttu-id="bdd48-600">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-600">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="bdd48-601">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="bdd48-601">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="bdd48-602">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-602">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="bdd48-603">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="bdd48-603">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="bdd48-604">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-604">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="bdd48-605">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="bdd48-605">AzureRM.Websites</span></span>
* <span data-ttu-id="bdd48-606">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-606">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="bdd48-607">6.6.0 - Temmuz 2018</span><span class="sxs-lookup"><span data-stu-id="bdd48-607">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="bdd48-608">Genel</span><span class="sxs-lookup"><span data-stu-id="bdd48-608">General</span></span>
* <span data-ttu-id="bdd48-609">Tüm yardım dosyaları tam parametre türleriyle doğru giriş/çıkış türlerini içerecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-609">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="bdd48-610">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="bdd48-610">AzureRM.Profile</span></span>
* <span data-ttu-id="bdd48-611">Kaynağın geçerli yapılandırmasının hedef kaynakla uyumlu olduğunu doğrulayabilmek için Common.Strategy kitaplığı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-611">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="bdd48-612">Common.Storage'a ps1xml türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-612">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="bdd48-613">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="bdd48-613">Azure.Storage</span></span>
* <span data-ttu-id="bdd48-614">DefaultProfile’dan Depolama Bağlamı almak için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-614">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="bdd48-615">Cmdlet'lerin çıkış türü özelliklerine Ps1XmlAttribute eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-615">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="bdd48-616">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="bdd48-616">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="bdd48-617">https://github.com/Azure/azure-powershell/issues/6370 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-617">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="bdd48-618">PsApiManagementApi'yi ApiContract'e çevirmek için Automapper hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-618">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="bdd48-619">https://github.com/Azure/azure-powershell/issues/6515 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-619">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="bdd48-620">Kodlama Türü ile aşırı yüklemeyi önlemek için File.Save hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-620">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="bdd48-621">https://github.com/Azure/azure-powershell/issues/6560 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-621">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="bdd48-622">apiId üzerindeki desen özel durumunu düzelten 4.0.3 Nuget sürümüne yükseltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-622">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="bdd48-623">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="bdd48-623">AzureRM.Compute</span></span>
* <span data-ttu-id="bdd48-624">PremiumLRS depolama hesap türü yeniden adlandırması nedeniyle New-AzureRmVm'de DiskFileParameterSet kullanılarak sanal makine oluşturmanın başarısız olmasıyla ilgili hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-624">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="bdd48-625">Invoke-AzureRmVMRunCommand cmdlet'i düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-625">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="bdd48-626">Abonelikteki tüm kullanılabilir kümelerin listelenebilmesi için Get-AzureRmAvailabilitySet güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-626">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="bdd48-627">(ResouceGroupName parametresi artık isteğe bağlı.)</span><span class="sxs-lookup"><span data-stu-id="bdd48-627">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="bdd48-628">Uygun sanal makinelerde Hızlandırılmış Ağı etkinleştirmek için 'New-AzureRmVm' cmdlet'inin SimpleParameterSet öğesi güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-628">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="bdd48-629">Kullanıcının belirttiği LB zaten mevcut olduğunda vmss oluşturmanın başarısız olması için New-AzureRmVmss basit parametre kümesi güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-629">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="bdd48-630">New-AzureRmDisk örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-630">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="bdd48-631">'New-AzureRmVM' için örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-631">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="bdd48-632">Set-AzureRmVMOSDisk açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-632">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="bdd48-633">Yazımı ve ön eki düzeltmek amacıyla Set-AzureRmVMBginfoExtension için Örnek 1 güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-633">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="bdd48-634">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="bdd48-634">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="bdd48-635">ADF .Net SDK sürümü 1.1.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-635">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="bdd48-636">Veri fabrikaları arasında paylaşılan şirket içinde barındırılan tümleştirme çalışma zamanı desteği.</span><span class="sxs-lookup"><span data-stu-id="bdd48-636">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="bdd48-637">Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet'ine yeni -SharedIntegrationRuntimeResourceId parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-637">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="bdd48-638">Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet'ine isteğe bağlı yeni -LinkedDataFactoryName parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-638">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="bdd48-639">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="bdd48-639">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="bdd48-640">DataPlane SDK'sı (Microsoft.Azure.DataLake.Store) sürümü 1.1.9'a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-640">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="bdd48-641">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="bdd48-641">AzureRM.EventHub</span></span>
* <span data-ttu-id="bdd48-642">Kaldırma cmdlet'lerine InputObject ve ResourceId yöneltmesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-642">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="bdd48-643">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="bdd48-643">AzureRM.Insights</span></span>
* <span data-ttu-id="bdd48-644">Yardım dosyalarındaki OutputType biçimlendirmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-644">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="bdd48-645">Microsoft.Azure.Management.Monitor SDK 0.19.1-preview kullanımı</span><span class="sxs-lookup"><span data-stu-id="bdd48-645">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="bdd48-646">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="bdd48-646">AzureRM.KeyVault</span></span>
* <span data-ttu-id="bdd48-647">Set-AzureRmKeyVaultAccessPolicy'de yönlendirme sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-647">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="bdd48-648">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="bdd48-648">AzureRM.Network</span></span>
* <span data-ttu-id="bdd48-649">LoadBalancerInboundNatPoolConfig cmdlet'leri için örnekler eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-649">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="bdd48-650">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="bdd48-650">AzureRM.Resources</span></span>
* <span data-ttu-id="bdd48-651">'Get-AzureRmResource' için hem etiket adı hem de değer sağlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-651">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="bdd48-652">'Set-AzureRmResource' için yönlendirme senaryosu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-652">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="bdd48-653">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="bdd48-653">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="bdd48-654">Kaldırma cmdlet'lerine InputObject ve ResourceId yöneltmesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-654">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="bdd48-655">birkaç sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-655">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="bdd48-656">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="bdd48-656">AzureRM.Sql</span></span>
* <span data-ttu-id="bdd48-657">Aşağıdaki cmdlet'lere Sunucu Gelişmiş Tehdit Koruması desteği ekleniyor:</span><span class="sxs-lookup"><span data-stu-id="bdd48-657">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="bdd48-658">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="bdd48-658">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="bdd48-659">Aşağıdaki cmdlet'lere Güvenlik Açığı Değerlendirme desteği ekleniyor:</span><span class="sxs-lookup"><span data-stu-id="bdd48-659">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="bdd48-660">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="bdd48-660">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="bdd48-661">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="bdd48-661">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="bdd48-662">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="bdd48-662">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="bdd48-663">Remove-AzureRmSqlServerFirewallRulecmdlet'indeki örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-663">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="bdd48-664">Get-AzureSqlSyncGroupLog içinde ABD temelli olmayan kültürde yanlış tarih saat işlemesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-664">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="bdd48-665">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="bdd48-665">AzureRM.Storage</span></span>
* <span data-ttu-id="bdd48-666">Cmdlet'lerin çıkış türü özelliklerine Ps1XmlAttribute eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-666">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="bdd48-667">Tablo görünümünde StorageAccount cmdlet'i çıkışı gösteriliyor</span><span class="sxs-lookup"><span data-stu-id="bdd48-667">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="bdd48-668">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bdd48-668">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="bdd48-669">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bdd48-669">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="bdd48-670">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bdd48-670">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="bdd48-671">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="bdd48-671">AzureRM.Tags</span></span>
* <span data-ttu-id="bdd48-672">Tag cmdlet'inin yardımında hatayı deyim kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="bdd48-672">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="bdd48-673">6.5.0 - Temmuz 2018</span><span class="sxs-lookup"><span data-stu-id="bdd48-673">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="bdd48-674">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="bdd48-674">AzureRM.Profile</span></span>
* <span data-ttu-id="bdd48-675">'Get-AzureRmContextAutosaveSetting' için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-675">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="bdd48-676">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="bdd48-676">Azure.Storage</span></span>
* <span data-ttu-id="bdd48-677">Salt yazılır Sas belirteciyle Karşıya Yükleme Blobu veya Dosyası desteği</span><span class="sxs-lookup"><span data-stu-id="bdd48-677">Support Upload Blob or File with write only Sas token</span></span>
* <span data-ttu-id="bdd48-678">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="bdd48-678">Set-AzureStorageBlobContent</span></span>
* <span data-ttu-id="bdd48-679">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="bdd48-679">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="bdd48-680">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="bdd48-680">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="bdd48-681">AS'ye gerekli ResourceGroupName özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-681">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="bdd48-682">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="bdd48-682">AzureRM.Automation</span></span>
* <span data-ttu-id="bdd48-683">'New-AzureRMAutomationSchedule' için yardım güncelleştirildi ve örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-683">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="bdd48-684">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="bdd48-684">AzureRM.Compute</span></span>
* <span data-ttu-id="bdd48-685">Update/New-AzureRmAvailabilitySet komutlarına -Tag parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-685">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="bdd48-686">'Add-AzureRmVmssExtension' için örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-686">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="bdd48-687">'Remove-AzureRmVmssExtension' için örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-687">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="bdd48-688">'Set-AzureRmVMAccessExtension' için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-688">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="bdd48-689">New-AzureRmVmss için SimpleParameterSet güncelleştirilerek SinglePlacementGroup varsayılan olarak false değerine ayarlandı ve kullanıcının tek yerleşim grubunda VMSS oluşturmasına olanak tanıyan 'SinglePlacementGroup' geçiş parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-689">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="bdd48-690">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="bdd48-690">AzureRM.EventHub</span></span>
* <span data-ttu-id="bdd48-691">PSEventHubDRConfigurationAttributes sınıfına, çoğaltma işlemi devam ederken bekleyen çoğaltma işlemlerinin sayısını veren salt okunur 'PendingReplicationOperationsCount' özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-691">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="bdd48-692">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="bdd48-692">AzureRM.KeyVault</span></span>
* <span data-ttu-id="bdd48-693">Set-AzureRmKeyVaultAccessPolicy için hata iletisi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-693">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="bdd48-694">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="bdd48-694">AzureRM.LogicApp</span></span>
* <span data-ttu-id="bdd48-695">New-AzureRmLogicApp’te "parametre kümesi çözümlenemedi" hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-695">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="bdd48-696">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="bdd48-696">AzureRM.Network</span></span>
* <span data-ttu-id="bdd48-697">Set/Add-AzureRmVirtualNetworkPeering için birden çok Kiracıdaki Sanal Makineler arasında eşleme etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-697">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="bdd48-698">Aşağıdaki cmdlet’ler Application Gateway için güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-698">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="bdd48-699">New-AzureRmApplicationGateway : EnableFIPS bayrağı ve Zones desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-699">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="bdd48-700">New-AzureRmApplicationGatewaySku : Yeni Standard_v2 ve WAF_v2 sku'ları eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-700">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="bdd48-701">Set-AzureRmApplicationGatewaySku : Yeni Standard_v2 ve WAF_v2 sku'ları eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-701">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="bdd48-702">RouteTable cmdlet’leri en son oluşturucu sürümüyle yeniden oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="bdd48-702">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="bdd48-703">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="bdd48-703">AzureRM.Relay</span></span>
* <span data-ttu-id="bdd48-704">Markdown dosyaları güncelleştirildi, örnekteki parametre adı sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="bdd48-704">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="bdd48-705">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="bdd48-705">AzureRM.Resources</span></span>
* <span data-ttu-id="bdd48-706">Roleassignment ve roledefinition cmdlet’leri güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="bdd48-706">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="bdd48-707">Disk belleğinin parçası olarak yapılan ek roledefinition çağrıları kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="bdd48-707">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="bdd48-708">Get-AzureRmRoleAssignment cmdlet’i düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-708">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="bdd48-709">-ExpandPrincipalGroups komut parametresi işlevselliği düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-709">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="bdd48-710">'-ResourceType' parametresinin büyük/küçük harfe duyarlı olduğu 'Get-AzureRmResource' sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-710">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="bdd48-711">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="bdd48-711">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="bdd48-712">Liste cmdlet’lerine top ve skip parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-712">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="bdd48-713">Standard'dan Premium NameSpace'e geçiş cmdlet’leri eklendi :</span><span class="sxs-lookup"><span data-stu-id="bdd48-713">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="bdd48-714">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="bdd48-714">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="bdd48-715">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="bdd48-715">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="bdd48-716">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="bdd48-716">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="bdd48-717">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="bdd48-717">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="bdd48-718">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="bdd48-718">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="bdd48-719">PSServiceBusDRConfigurationAttributes sınıfına, çoğaltma işlemi sürerken beklemede olan çoğaltma işlemi sayısını veren salt okunur 'PendingReplicationOperationsCount' özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-719">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="bdd48-720">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="bdd48-720">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="bdd48-721">'New-AzureRmServiceFabricCluster' için örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-721">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="bdd48-722">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="bdd48-722">AzureRM.Sql</span></span>
* <span data-ttu-id="bdd48-723">Müşterilerin Sql Server örneğine veya Yönetilen Örneğe TDE Sertifikası ekleyebilmeleri için yeni Management.Sql Cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-723">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="bdd48-724">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="bdd48-724">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="bdd48-725">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="bdd48-725">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="bdd48-726">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="bdd48-726">AzureRM.Websites</span></span>
* <span data-ttu-id="bdd48-727">Artık `Set-AzureRmWebApp -AssignIdentity` ve `Set-AzureRmWebAppSlot -AssignIdentity` false olarak ayarlandığında site object.Removing önizleme etiketinden Identity özelliğini kaldırıyor.</span><span class="sxs-lookup"><span data-stu-id="bdd48-727">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="bdd48-728">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-728">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="bdd48-729">`Set-AzureRmWebApp -PhpVersion` geçerli bir php sürümü off değerini destekliyor</span><span class="sxs-lookup"><span data-stu-id="bdd48-729">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="bdd48-730">6.4.0 - Temmuz 2018</span><span class="sxs-lookup"><span data-stu-id="bdd48-730">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="bdd48-731">Genel</span><span class="sxs-lookup"><span data-stu-id="bdd48-731">General</span></span>
* <span data-ttu-id="bdd48-732">Modüllerin çoğu için yardım dosyalarındaki OutputType biçimlendirmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-732">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="bdd48-733">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="bdd48-733">AzureRM.Profile</span></span>
* <span data-ttu-id="bdd48-734">Temel çıkış türlerine Ps1Xml özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-734">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="bdd48-735">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="bdd48-735">AzureRM.Compute</span></span>
* <span data-ttu-id="bdd48-736">VMSS için IP Etiketi özelliği</span><span class="sxs-lookup"><span data-stu-id="bdd48-736">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="bdd48-737">'New-AzureRmVmssIpTagConfig' cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-737">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="bdd48-738">New-AzureRmVmssIpConfig cmdlet'ine IpTag parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-738">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="bdd48-739">VMSS için Otomatik İşletim Sistemi Geri Alma özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-739">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="bdd48-740">New-AzureRmVmssConfig ve Update-AzureRmVmss cmdlet'lerine DisableAutoRollback parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-740">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="bdd48-741">VMSS için İşletim Sistemi Yükseltme Geçmişi özelliği</span><span class="sxs-lookup"><span data-stu-id="bdd48-741">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="bdd48-742">Get-AzureRmVmss cmdlet'ine OSUpgradeHistory anahtarı parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-742">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="bdd48-743">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="bdd48-743">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="bdd48-744">Aşağıdaki komutlarla Katalog ACL'si için destek eklendi:</span><span class="sxs-lookup"><span data-stu-id="bdd48-744">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="bdd48-745">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="bdd48-745">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="bdd48-746">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="bdd48-746">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="bdd48-747">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="bdd48-747">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="bdd48-748">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="bdd48-748">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="bdd48-749">Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry ve Set-AzureRmDataLakeStoreItemAcl için iptal desteği ve ilerleme izleme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-749">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="bdd48-750">Export-AzureRmDataLakeStoreChildItemProperties için iptal desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-750">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="bdd48-751">Özyinelemeli işlemler gerçekleştiren cmdlet'ler için hata ayıklama iletilerinin boşaltılması hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-751">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="bdd48-752">DataLake cmdlet'lerinin test konumu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-752">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="bdd48-753">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="bdd48-753">AzureRM.EventHub</span></span>
* <span data-ttu-id="bdd48-754">Get-AzureRmEventHub ve Get-AzureRmEventHubConsumerGroup Listeleme İşlemleri cmdlet'lerine İsteğe Bağlı MaxCount parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-754">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="bdd48-755">New-AzureRmEventHub cmdlet'inde yeni Olay Hub'ı oluşturma sırasında en az bir parametreye ihtiyaç duyma sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-755">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="bdd48-756">Varsayılan Parametre kümesi sağlandı.</span><span class="sxs-lookup"><span data-stu-id="bdd48-756">Provided Default Parameter set.</span></span>
* <span data-ttu-id="bdd48-757">Kullanıcının New-AzureRmEventHubKey cmdlet'ine KeyValue eklemesini sağlayan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-757">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="bdd48-758">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="bdd48-758">AzureRM.KeyVault</span></span>
* <span data-ttu-id="bdd48-759">Get-AzureRmKeyVault -Tag ile tüm kaynakların döndürülmesine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-759">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="bdd48-760">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="bdd48-760">AzureRM.Network</span></span>
* <span data-ttu-id="bdd48-761">Zone-Redundant VirtualNetworkGateways için yeni SKU'lar kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="bdd48-761">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="bdd48-762">ARM aracılığıyla ExpressRoute Partner API'leri özelliği için yeni komutlar eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-762">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="bdd48-763">Get-AzureRmExpressRouteCrossConnection eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-763">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="bdd48-764">Set-AzureRmExpressRouteCrossConnection eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-764">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="bdd48-765">Add-AzureRmExpressRouteCrossConnectionPeering eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-765">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="bdd48-766">Get-AzureRmExpressRouteCrossConnectionPeering eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-766">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="bdd48-767">Remove-AzureRmExpressRouteCrossConnectionPeering eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-767">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="bdd48-768">Get-AzureRMExpressRouteCrossConnectionArpTable eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-768">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="bdd48-769">Get-AzureRMExpressRouteCrossConnectionRouteTable eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-769">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="bdd48-770">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-770">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="bdd48-771">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="bdd48-771">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="bdd48-772">Get-AzureRmRecoveryServicesBackupStatus cmdlet'i eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-772">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="bdd48-773">Bu cmdlet bir sanal makinenin kimliğini alır ve sanal makinenin abonelik içindeki kasaların koruması altında olup olmadığını denetler.</span><span class="sxs-lookup"><span data-stu-id="bdd48-773">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="bdd48-774">Böyle bir kasa varsa cmdlet, bu kasanın ayrıntılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bdd48-774">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="bdd48-775">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="bdd48-775">AzureRM.Resources</span></span>
* <span data-ttu-id="bdd48-776">Get-AzureRmPolicyAssignment cmdlet'leri güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="bdd48-776">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="bdd48-777">Yönetim grubu düzeyinde -Scope değerlerini listeleme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-777">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="bdd48-778">Yönetim grubu düzeyinde -Scope değerlerine sahip olan tek atamaları alma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-778">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="bdd48-779">control parametresine -Effective ve -All anahtarları eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-779">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="bdd48-780">Get/New/Remove/Set-AzureRmPolicyDefinition cmdlet'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-780">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="bdd48-781">Belirli bir yönetim grubuna işlem uygulamayı sağlayan için -ManagementGroupName parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-781">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="bdd48-782">Belirli bir aboneliğe işlem uygulamayı sağlayan Add -SubscriptionId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-782">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="bdd48-783">Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlet'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-783">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="bdd48-784">Belirli bir yönetim grubuna işlem uygulamayı sağlayan -ManagementGroupName parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-784">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="bdd48-785">Belirli bir aboneliğe işlem uygulamayı sağlayan Add -SubscriptionId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-785">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="bdd48-786">'New-AzureRmResourceGroupDeployment' içinde 'TemplateParameterObject' kullanırken parametrelerde KeyVault gizli dizi başvurusu desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-786">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="bdd48-787">'New-AzureRmADAppCredential' için '-EndDate' parametresinin yoksayılmasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-787">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="bdd48-788">'Add-AzureRmADGroupMember' cmdlet'inin istekte bulunmak için yanlış URL'yi kullandığı sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-788">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="bdd48-789">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="bdd48-789">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="bdd48-790">Kullanıcının New-AzureRmServiceBusKey cmdlet'ine KeyValue eklemesini sağlayan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-790">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="bdd48-791">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="bdd48-791">AzureRM.Sql</span></span>
* <span data-ttu-id="bdd48-792">New-AzureRmSqlDatabaseRestorePoint yardımında Kullanıcı Tanımlı Geri Yükleme Noktaları netleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-792">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="bdd48-793">Birden fazla cmdlet'te -ComputeGeneration parametresinin belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-793">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="bdd48-794">6.3.0 - Haziran 2018</span><span class="sxs-lookup"><span data-stu-id="bdd48-794">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="bdd48-795">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="bdd48-795">AzureRM.Profile</span></span>
* <span data-ttu-id="bdd48-796">Enable-AzureRmContextAutoSave için hata iletileri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-796">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="bdd48-797">'Connect-AzureRmAccount' cmdlet'i eski bir bağlam olmadan çalıştırıldığında her abonelik için bir bağlam oluşturur</span><span class="sxs-lookup"><span data-stu-id="bdd48-797">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="bdd48-798">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="bdd48-798">Azure.Storage</span></span>
* <span data-ttu-id="bdd48-799">Yardım dosyalarına -Permissions parametresi hakkında daha fazla bilgi eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-799">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="bdd48-800">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="bdd48-800">AzureRM.Compute</span></span>
* <span data-ttu-id="bdd48-801">'Get-AzureRmVmDiskEncryptionStatus' için veri diski bulunmayan VM'lerde karşılaşılan bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-801">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="bdd48-802">Aşağıdaki cmdlet'leri düzeltmek için bilgisayar istemci kitaplığı sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-802">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="bdd48-803">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="bdd48-803">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="bdd48-804">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="bdd48-804">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="bdd48-805">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="bdd48-805">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="bdd48-806">Aşağıdaki cmdlet'ler 'operation ID' ve 'operation status' bilgilerini doğru gösterecek şekilde düzeltildi:</span><span class="sxs-lookup"><span data-stu-id="bdd48-806">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="bdd48-807">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="bdd48-807">Start-AzureRmVM</span></span>
    - <span data-ttu-id="bdd48-808">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="bdd48-808">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="bdd48-809">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="bdd48-809">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="bdd48-810">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="bdd48-810">Set-AzureRmVM</span></span>
    - <span data-ttu-id="bdd48-811">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="bdd48-811">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="bdd48-812">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="bdd48-812">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="bdd48-813">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="bdd48-813">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="bdd48-814">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="bdd48-814">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="bdd48-815">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="bdd48-815">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="bdd48-816">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="bdd48-816">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="bdd48-817">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="bdd48-817">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="bdd48-818">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="bdd48-818">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="bdd48-819">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="bdd48-819">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="bdd48-820">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="bdd48-820">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="bdd48-821">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="bdd48-821">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="bdd48-822">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="bdd48-822">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="bdd48-823">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="bdd48-823">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="bdd48-824">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="bdd48-824">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="bdd48-825">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="bdd48-825">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="bdd48-826">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="bdd48-826">AzureRM.EventGrid</span></span>
* <span data-ttu-id="bdd48-827">Gerekli olması halinde parametrelerin boş dizeyle değiştirilmesine izin vermek için Update-AzureRmEventGridSubscription cmdlet'i içindeki SubjectBeginsWith/SubjectEndsWith için ValidateNotNullOrEmpty doğrulama koşulları kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="bdd48-827">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="bdd48-828">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="bdd48-828">AzureRM.KeyVault</span></span>
* <span data-ttu-id="bdd48-829">Get-AzureRmKeyVault -Tag çalıştırıldığında etiket döndürülmeme sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-829">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="bdd48-830">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="bdd48-830">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="bdd48-831">Policy Insights cmdlet'leri genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="bdd48-831">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="bdd48-832">API 2018-04-04 sürümünü kullanın</span><span class="sxs-lookup"><span data-stu-id="bdd48-832">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="bdd48-833">PolicyDefinitionReferenceId, Get-AzureRmPolicyStateSummary sonuçlarına eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-833">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="bdd48-834">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="bdd48-834">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="bdd48-835">RecoveryServices.Backup cmdlet'lerine -Vault parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-835">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="bdd48-836">Bu parametre iletildiğinde Set-AzureRmRecoveryServicesContext cmdlet'ini geçersiz kılar.</span><span class="sxs-lookup"><span data-stu-id="bdd48-836">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="bdd48-837">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="bdd48-837">AzureRM.Sql</span></span>
* <span data-ttu-id="bdd48-838">Yardım dosyasındaki Get-AzureRmSqlDatabaseExpanded örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-838">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="bdd48-839">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="bdd48-839">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="bdd48-840">Yardım dosyasındaki Add-AzureRmTrafficManagerEndpointConfig bölümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-840">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="bdd48-841">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="bdd48-841">AzureRM.Websites</span></span>
* <span data-ttu-id="bdd48-842">'Set-AzureRmWebApp', -AssignIdentity kullanıldığında AppSettings verilerini geçersiz kılmayacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-842">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="bdd48-843">'New-AzureRmWebAppSlot', isteğe bağlı parametre olarak AppServicePlan girişini kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-843">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="bdd48-844">6.2.1 - Haziran 2018</span><span class="sxs-lookup"><span data-stu-id="bdd48-844">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="bdd48-845">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="bdd48-845">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="bdd48-846">PSWorkspace modeli Network için tür parametresini kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-846">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="bdd48-847">6.2.0 - Haziran 2018</span><span class="sxs-lookup"><span data-stu-id="bdd48-847">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="bdd48-848">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="bdd48-848">AzureRM.Profile</span></span>
* <span data-ttu-id="bdd48-849">Modülün içeri aktarılması sırasında Newtonsoft.Json 10.0.3 sürümünün yüklenmemesine ilişkin sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-849">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="bdd48-850">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="bdd48-850">AzureRM.Compute</span></span>
* <span data-ttu-id="bdd48-851">VMSS VM Güncelleştirme özelliği</span><span class="sxs-lookup"><span data-stu-id="bdd48-851">VMSS VM Update feature</span></span>
    - <span data-ttu-id="bdd48-852">'Update-AzureRmVmssVM' ve 'New-AzureRmVMDataDisk' cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-852">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="bdd48-853">VMSS VM’sine veri diski eklemeyi desteklemek için 'Add-AzureRmVMDataDisk' cmdlet’ine VirtualMachineScaleSetVM parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-853">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="bdd48-854">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="bdd48-854">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="bdd48-855">ADF .Net SDK sürümü, aşağıdaki değişiklikleri içeren 0.8.0-preview sürümüne güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="bdd48-855">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="bdd48-856">Fabrika deposunu yapılandırma işlemi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-856">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="bdd48-857">QuickBooks LinkedService, consumerKey ve consumerSecret özelliklerini kullanıma sunmak üzere güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-857">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="bdd48-858">SecretBase’ten Object’e birkaç model türü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-858">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="bdd48-859">Blob Etkinliklerini tetikleme eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-859">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="bdd48-860">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="bdd48-860">AzureRM.KeyVault</span></span>
* <span data-ttu-id="bdd48-861">Belgeler örnek çıktı ile güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-861">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="bdd48-862">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="bdd48-862">AzureRM.Network</span></span>
* <span data-ttu-id="bdd48-863">Ağ İzleyicisi cmdlet’leri üzerindeki Trafik Analizi parametreleri etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-863">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="bdd48-864">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="bdd48-864">AzureRM.Resources</span></span>
* <span data-ttu-id="bdd48-865">'Get-AzureRmResource' cmdlet’inden döndürülen 'PSResource' nesnesinin 'Properties' özelliğiyle ilgili bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-865">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="bdd48-866">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="bdd48-866">AzureRM.Scheduler</span></span>
* <span data-ttu-id="bdd48-867">Güncelleştirilen ServiceBusQueueJob’ın yeni Kimlik Doğrulaması değerlerini ayarlamamasıyla ilgili bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-867">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="bdd48-868">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="bdd48-868">AzureRM.Sql</span></span>
* <span data-ttu-id="bdd48-869">Şu cmdlet’ler isteğe bağlı LicenseType parametresiyle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="bdd48-869">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="bdd48-870">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="bdd48-870">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="bdd48-871">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="bdd48-871">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="bdd48-872">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="bdd48-872">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="bdd48-873">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="bdd48-873">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="bdd48-874">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="bdd48-874">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="bdd48-875">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="bdd48-875">AzureRM.Websites</span></span>
* <span data-ttu-id="bdd48-876">'New-AzureRMWebApp' Strategy kütüphanesindeki ortak algoritmaları kullanmak üzere güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-876">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="bdd48-877">6.1.0 - Mayıs 2018</span><span class="sxs-lookup"><span data-stu-id="bdd48-877">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="bdd48-878">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="bdd48-878">AzureRM.Profile</span></span>
* <span data-ttu-id="bdd48-879">'Clear-AzureRmContext' komutunun çalıştırılmasının boş bir bağlamı önceki varsayılan bağlamın adıyla tutmasına ve böylece kullanıcının eski ad ile yeni bir bağlam oluşturamadığı bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-879">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="bdd48-880">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="bdd48-880">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="bdd48-881">AS’de Ağ geçidi ilişkilendirme/ilişkilendirme kaldırma işlemlerini etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="bdd48-881">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="bdd48-882">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="bdd48-882">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="bdd48-883">ApiVersions, ApiReleases ve ApiRevisions desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-883">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="bdd48-884">ServiceFabric Arka Ucu desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-884">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="bdd48-885">Application Insights Günlükçüsü desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-885">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="bdd48-886">‘Temel’ sku’yu Api Yönetim hizmetinin geçerli sku’su olarak algılama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-886">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="bdd48-887">Özel CA tarafından Kök veya CA olarak yayınlanan Sertifikaları yükleme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-887">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="bdd48-888">Özel SSL sertifikalarını KeyVault ve Çoklu ara sunucu ana bilgisayar adlarıyla kabul etme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-888">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="bdd48-889">MSI kimliği desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-889">Added support for MSI identity</span></span>
* <span data-ttu-id="bdd48-890">İlkeleri Url ile kabul etme desteği eklendi NOT: Aşağıdaki cmdlet’ler gelecekteki sürümlerde kullanım dışı kalacaktır</span><span class="sxs-lookup"><span data-stu-id="bdd48-890">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="bdd48-891">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="bdd48-891">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="bdd48-892">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="bdd48-892">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="bdd48-893">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="bdd48-893">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="bdd48-894">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="bdd48-894">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="bdd48-895">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="bdd48-895">AzureRM.Batch</span></span>
* <span data-ttu-id="bdd48-896">Yeni Get-AzureBatchPoolNodeCounts cmdlet’ini yayınlama</span><span class="sxs-lookup"><span data-stu-id="bdd48-896">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="bdd48-897">Yeni AzureBatchComputeNodeServiceLogUpload cmdlet’ini yayınlama</span><span class="sxs-lookup"><span data-stu-id="bdd48-897">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="bdd48-898">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="bdd48-898">AzureRM.Consumption</span></span>
* <span data-ttu-id="bdd48-899">Get-AzureRmConsumptionUsageDetail cmdlet’inde yeni Expand, ResourceGroup, InstanceName, InstanceId, Tags ve Top parametrelerini ekleme</span><span class="sxs-lookup"><span data-stu-id="bdd48-899">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="bdd48-900">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="bdd48-900">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="bdd48-901">Export-AzureRmDataLakeStoreChildItemProperties için düzeltme örneği</span><span class="sxs-lookup"><span data-stu-id="bdd48-901">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="bdd48-902">Set-AzureRmDataLakeStoreItemAclEntry komutunda Özyineleme durumu için null parametresi özel durumunu düzeltme</span><span class="sxs-lookup"><span data-stu-id="bdd48-902">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="bdd48-903">Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry’ye yönelik yardım dosyalarını düzeltme</span><span class="sxs-lookup"><span data-stu-id="bdd48-903">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="bdd48-904">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="bdd48-904">AzureRM.Network</span></span>
* <span data-ttu-id="bdd48-905">Ağ SDK sürümünü 18.0.0-önizleme’den 19.0.0-önizlemeye yükseltme</span><span class="sxs-lookup"><span data-stu-id="bdd48-905">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="bdd48-906">Protokol yapılandırması oluşturma cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-906">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="bdd48-907">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="bdd48-907">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="bdd48-908">Varolan express route bağlantı hattına yeni bir bağlantı hattı ekleme cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-908">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="bdd48-909">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="bdd48-909">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="bdd48-910">Varolan express route bağlantı hattındaki bir bağlantı hattı bağlantısını kaldırma cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-910">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="bdd48-911">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="bdd48-911">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="bdd48-912">Bağlantı hattı bağlantısı alma cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="bdd48-912">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="bdd48-913">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="bdd48-913">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="bdd48-914">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="bdd48-914">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="bdd48-915">Oluşturulan sertifikalarla sunucu kimlik doğrulaması kullanımı düzeltildi (Sorun No. 5998)</span><span class="sxs-lookup"><span data-stu-id="bdd48-915">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="bdd48-916">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="bdd48-916">AzureRM.Sql</span></span>
* <span data-ttu-id="bdd48-917">AuditActions veya AuditActionGroups’un kaldırılmasını sağlamak üzere Denetim cmdlet’leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdd48-917">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="bdd48-918">Yeni bir esnek saklama ilkesi ayarlarken komutun ‘Azure kurtarma hizmeti kasası ve ilkesiyle uzun süreli saklama ilkesini yapılandırma artık desteklenmiyor. Lütfen yeni esnek saklama ilkesi ile istek gönderin’ hatasını verdiği Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="bdd48-918">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="bdd48-919">komutuna ilişkin sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdd48-919">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="bdd48-920">Ölçek ve katman ilişkili özelliklere yönelik Sku özelliğini destekleyen yeni Veritabanı API’sini kullanmak için tüm Azure Sql Database/ElasticPool Creation/Update cmdlet’lerini güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="bdd48-920">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="bdd48-921">Güncelleştirilen cmlet’ler arasında şunlar yer almaktadır:</span><span class="sxs-lookup"><span data-stu-id="bdd48-921">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="bdd48-922">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="bdd48-922">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="bdd48-923">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="bdd48-923">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="bdd48-924">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="bdd48-924">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="bdd48-925">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="bdd48-925">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="bdd48-926">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="bdd48-926">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="bdd48-927">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="bdd48-927">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="bdd48-928">-Name parametresini kullanırken -ResourceGroupName parametresinin gerekli olması için 'Get-AzureRmTrafficManagerProfile'a yönelik parametreleri güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="bdd48-928">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
