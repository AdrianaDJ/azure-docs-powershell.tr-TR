---
title: Azure PowerShell Değişiklik Günlüğü | Microsoft Docs
description: Azure PowerShell'in en son sürümünde yapılan değişikliklerin geçmişi aşağıda verilmiştir.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: 3961f5c37869d0dc877b85bad535f399181040db
ms.sourcegitcommit: afae9f2f091b21ed07d5aec1c249cf859a8b89a4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2018
ms.locfileid: "39653500"
---
# <a name="release-notes"></a><span data-ttu-id="6d55c-103">Sürüm notları</span><span class="sxs-lookup"><span data-stu-id="6d55c-103">Release notes</span></span>

<span data-ttu-id="6d55c-104">Azure PowerShell'in bu sürümünde yapılan değişikliklerin listesi aşağıda verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="6d55c-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="660---july-2018"></a><span data-ttu-id="6d55c-105">6.6.0 - Temmuz 2018</span><span class="sxs-lookup"><span data-stu-id="6d55c-105">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="6d55c-106">Genel</span><span class="sxs-lookup"><span data-stu-id="6d55c-106">General</span></span>
* <span data-ttu-id="6d55c-107">Tüm yardım dosyaları tam parametre türleriyle doğru giriş/çıkış türlerini içerecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="6d55c-107">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="6d55c-108">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="6d55c-108">AzureRM.Profile</span></span>
* <span data-ttu-id="6d55c-109">Kaynağın geçerli yapılandırmasının hedef kaynakla uyumlu olduğunu doğrulayabilmek için Common.Strategy kitaplığı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="6d55c-109">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span> <span data-ttu-id="6d55c-110">Varsayılan her zaman doğru olmasıdır; tek tek kaynaklarda varsayılan geçersiz kılınabilir.</span><span class="sxs-lookup"><span data-stu-id="6d55c-110">Default is always true, individual resources and overridet the default.</span></span>
* <span data-ttu-id="6d55c-111">Common.Storage'a ps1xml türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="6d55c-111">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="6d55c-112">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="6d55c-112">Azure.Storage</span></span>
* <span data-ttu-id="6d55c-113">Destek DefaulfProfile'dan Depolama Bağlamı'nı alıyor</span><span class="sxs-lookup"><span data-stu-id="6d55c-113">Support get Storage Context from DefaulfProfile</span></span>
* <span data-ttu-id="6d55c-114">Cmdlet'lerin çıkış türü özelliklerine Ps1XmlAttribute eklendi.</span><span class="sxs-lookup"><span data-stu-id="6d55c-114">Add Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="6d55c-115">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6d55c-115">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="6d55c-116">https://github.com/Azure/azure-powershell/issues/6370 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6d55c-116">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="6d55c-117">PsApiManagementApi'yi ApiContract'e çevirmek için Automapper hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6d55c-117">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="6d55c-118">https://github.com/Azure/azure-powershell/issues/6515 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6d55c-118">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="6d55c-119">Kodlama Türü ile aşırı yüklemeyi önlemek için File.Save hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6d55c-119">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="6d55c-120">https://github.com/Azure/azure-powershell/issues/6560 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6d55c-120">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="6d55c-121">apiId üzerindeki desen özel durumunu düzelten 4.0.3 Nuget sürümüne yükseltildi</span><span class="sxs-lookup"><span data-stu-id="6d55c-121">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="6d55c-122">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="6d55c-122">AzureRM.Compute</span></span>
* <span data-ttu-id="6d55c-123">PremiumLRS depolama hesap türü yeniden adlandırması nedeniyle New-AzureRmVm'de DiskFileParameterSet kullanılarak sanal makine oluşturmanın başarısız olmasıyla ilgili hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="6d55c-123">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="6d55c-124">Invoke-AzureRmVMRunCommand cmdlet'i düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6d55c-124">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="6d55c-125">Abonelikteki tüm kullanılabilir kümelerin listelenebilmesi için Get-AzureRmAvailabilitySet güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="6d55c-125">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="6d55c-126">(ResouceGroupName parametresi artık isteğe bağlı.)</span><span class="sxs-lookup"><span data-stu-id="6d55c-126">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="6d55c-127">Uygun sanal makinelerde Hızlandırılmış Ağı etkinleştirmek için 'New-AzureRmVm' cmdlet'inin SimpleParameterSet öğesi güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="6d55c-127">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="6d55c-128">Kullanıcının belirttiği LB zaten mevcut olduğunda vmss oluşturmanın başarısız olması için New-AzureRmVmss basit parametre kümesi güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="6d55c-128">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="6d55c-129">New-AzureRmDisk örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6d55c-129">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="6d55c-130">'New-AzureRmVM' için örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="6d55c-130">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="6d55c-131">Set-AzureRmVMOSDisk açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6d55c-131">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="6d55c-132">Yazımı ve ön eki düzeltmek amacıyla Set-AzureRmVMBginfoExtension için Örnek 1 güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="6d55c-132">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="6d55c-133">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="6d55c-133">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="6d55c-134">ADF .Net SDK sürümü 1.1.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="6d55c-134">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="6d55c-135">Veri fabrikaları arasında paylaşılan şirket içinde barındırılan tümleştirme çalışma zamanı desteği.</span><span class="sxs-lookup"><span data-stu-id="6d55c-135">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="6d55c-136">Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet'ine yeni -SharedIntegrationRuntimeResourceId parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="6d55c-136">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="6d55c-137">Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet'ine isteğe bağlı yeni -LinkedDataFactoryName parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="6d55c-137">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="6d55c-138">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6d55c-138">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="6d55c-139">DataPlane SDK'sı (Microsoft.Azure.DataLake.Store) sürümü 1.1.9'a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6d55c-139">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="6d55c-140">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="6d55c-140">AzureRM.EventHub</span></span>
* <span data-ttu-id="6d55c-141">Kaldırma cmdlet'lerine InputObject ve ResourceId yöneltmesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6d55c-141">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="6d55c-142">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="6d55c-142">AzureRM.Insights</span></span>
* <span data-ttu-id="6d55c-143">Yardım dosyalarındaki OutputType biçimlendirmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6d55c-143">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="6d55c-144">Microsoft.Azure.Management.Monitor SDK 0.19.1-preview kullanımı</span><span class="sxs-lookup"><span data-stu-id="6d55c-144">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="6d55c-145">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6d55c-145">AzureRM.KeyVault</span></span>
* <span data-ttu-id="6d55c-146">Set-AzureRmKeyVaultAccessPolicy'de yönlendirme sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6d55c-146">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="6d55c-147">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="6d55c-147">AzureRM.Network</span></span>
* <span data-ttu-id="6d55c-148">LoadBalancerInboundNatPoolConfig cmdlet'leri için örnekler eklendi.</span><span class="sxs-lookup"><span data-stu-id="6d55c-148">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="6d55c-149">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="6d55c-149">AzureRM.Resources</span></span>
* <span data-ttu-id="6d55c-150">'Get-AzureRmResource' için hem etiket adı hem de değer sağlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6d55c-150">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="6d55c-151">'Set-AzureRmResource' için yönlendirme senaryosu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6d55c-151">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="6d55c-152">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6d55c-152">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="6d55c-153">Kaldırma cmdlet'lerine InputObject ve ResourceId yöneltmesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6d55c-153">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="6d55c-154">birkaç sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6d55c-154">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="6d55c-155">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="6d55c-155">AzureRM.Sql</span></span>
* <span data-ttu-id="6d55c-156">Aşağıdaki cmdlet'lere Sunucu Gelişmiş Tehdit Koruması desteği ekleniyor:</span><span class="sxs-lookup"><span data-stu-id="6d55c-156">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="6d55c-157">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6d55c-157">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="6d55c-158">Aşağıdaki cmdlet'lere Güvenlik Açığı Değerlendirme desteği ekleniyor:</span><span class="sxs-lookup"><span data-stu-id="6d55c-158">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="6d55c-159">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="6d55c-159">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="6d55c-160">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="6d55c-160">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="6d55c-161">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="6d55c-161">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="6d55c-162">Remove-AzureRmSqlServerFirewallRulecmdlet'indeki örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6d55c-162">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="6d55c-163">Get-AzureSqlSyncGroupLog içinde ABD temelli olmayan kültürde yanlış tarih saat işlemesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6d55c-163">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="6d55c-164">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="6d55c-164">AzureRM.Storage</span></span>
* <span data-ttu-id="6d55c-165">Cmdlet'lerin çıkış türü özelliklerine Ps1XmlAttribute eklendi</span><span class="sxs-lookup"><span data-stu-id="6d55c-165">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="6d55c-166">Tablo görünümünde StorageAccount cmdlet'i çıkışı gösteriliyor</span><span class="sxs-lookup"><span data-stu-id="6d55c-166">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="6d55c-167">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6d55c-167">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="6d55c-168">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6d55c-168">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="6d55c-169">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6d55c-169">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="6d55c-170">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="6d55c-170">AzureRM.Tags</span></span>
* <span data-ttu-id="6d55c-171">Tag cmdlet'inin yardımında hatayı deyim kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="6d55c-171">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="6d55c-172">6.5.0 - Temmuz 2018</span><span class="sxs-lookup"><span data-stu-id="6d55c-172">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="6d55c-173">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="6d55c-173">AzureRM.Profile</span></span>
* <span data-ttu-id="6d55c-174">'Get-AzureRmContextAutosaveSetting' için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6d55c-174">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="6d55c-175">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="6d55c-175">Azure.Storage</span></span>
* <span data-ttu-id="6d55c-176">Salt yazılır Sas belirteciyle Karşıya Yükleme Blobu veya Dosyası desteği</span><span class="sxs-lookup"><span data-stu-id="6d55c-176">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="6d55c-177">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="6d55c-177">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="6d55c-178">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="6d55c-178">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="6d55c-179">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6d55c-179">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="6d55c-180">AS'ye gerekli ResourceGroupName özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="6d55c-180">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="6d55c-181">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="6d55c-181">AzureRM.Automation</span></span>
* <span data-ttu-id="6d55c-182">'New-AzureRMAutomationSchedule' için yardım güncelleştirildi ve örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="6d55c-182">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="6d55c-183">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="6d55c-183">AzureRM.Compute</span></span>
* <span data-ttu-id="6d55c-184">Update/New-AzureRmAvailabilitySet komutlarına -Tag parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="6d55c-184">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="6d55c-185">'Add-AzureRmVmssExtension' için örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="6d55c-185">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="6d55c-186">'Remove-AzureRmVmssExtension' için örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="6d55c-186">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="6d55c-187">'Set-AzureRmVMAccessExtension' için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6d55c-187">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="6d55c-188">New-AzureRmVmss için SimpleParameterSet güncelleştirilerek SinglePlacementGroup varsayılan olarak false değerine ayarlandı ve kullanıcının tek yerleşim grubunda VMSS oluşturmasına olanak tanıyan 'SinglePlacementGroup' geçiş parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="6d55c-188">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="6d55c-189">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="6d55c-189">AzureRM.EventHub</span></span>
* <span data-ttu-id="6d55c-190">PSEventHubDRConfigurationAttributes sınıfına, çoğaltma işlemi devam ederken bekleyen çoğaltma işlemlerinin sayısını veren salt okunur 'PendingReplicationOperationsCount' özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="6d55c-190">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="6d55c-191">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6d55c-191">AzureRM.KeyVault</span></span>
* <span data-ttu-id="6d55c-192">Set-AzureRmKeyVaultAccessPolicy için hata iletisi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6d55c-192">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="6d55c-193">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="6d55c-193">AzureRM.LogicApp</span></span>
* <span data-ttu-id="6d55c-194">New-AzureRmLogicApp’te "parametre kümesi çözümlenemedi" hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6d55c-194">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="6d55c-195">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="6d55c-195">AzureRM.Network</span></span>
* <span data-ttu-id="6d55c-196">Set/Add-AzureRmVirtualNetworkPeering için birden çok Kiracıdaki Sanal Makineler arasında eşleme etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="6d55c-196">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="6d55c-197">Aşağıdaki cmdlet’ler Application Gateway için güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6d55c-197">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="6d55c-198">New-AzureRmApplicationGateway : EnableFIPS bayrağı ve Zones desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="6d55c-198">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="6d55c-199">New-AzureRmApplicationGatewaySku : Yeni Standard_v2 ve WAF_v2 sku'ları eklendi</span><span class="sxs-lookup"><span data-stu-id="6d55c-199">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="6d55c-200">Set-AzureRmApplicationGatewaySku : Yeni Standard_v2 ve WAF_v2 sku'ları eklendi</span><span class="sxs-lookup"><span data-stu-id="6d55c-200">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="6d55c-201">RouteTable cmdlet’leri en son oluşturucu sürümüyle yeniden oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="6d55c-201">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="6d55c-202">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="6d55c-202">AzureRM.Relay</span></span>
* <span data-ttu-id="6d55c-203">Markdown dosyaları güncelleştirildi, örnekteki parametre adı sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="6d55c-203">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="6d55c-204">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="6d55c-204">AzureRM.Resources</span></span>
* <span data-ttu-id="6d55c-205">Roleassignment ve roledefinition cmdlet’leri güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="6d55c-205">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="6d55c-206">Disk belleğinin parçası olarak yapılan ek roledefinition çağrıları kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="6d55c-206">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="6d55c-207">Get-AzureRmRoleAssignment cmdlet’i düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6d55c-207">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="6d55c-208">-ExpandPrincipalGroups komut parametresi işlevselliği düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6d55c-208">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="6d55c-209">'-ResourceType' parametresinin büyük/küçük harfe duyarlı olduğu 'Get-AzureRmResource' sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6d55c-209">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="6d55c-210">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6d55c-210">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="6d55c-211">Liste cmdlet’lerine top ve skip parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="6d55c-211">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="6d55c-212">Standard'dan Premium NameSpace'e geçiş cmdlet’leri eklendi :</span><span class="sxs-lookup"><span data-stu-id="6d55c-212">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="6d55c-213">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="6d55c-213">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="6d55c-214">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="6d55c-214">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="6d55c-215">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="6d55c-215">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="6d55c-216">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="6d55c-216">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="6d55c-217">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="6d55c-217">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="6d55c-218">PSServiceBusDRConfigurationAttributes sınıfına, çoğaltma işlemi sürerken beklemede olan çoğaltma işlemi sayısını veren salt okunur 'PendingReplicationOperationsCount' özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="6d55c-218">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="6d55c-219">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6d55c-219">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="6d55c-220">'New-AzureRmServiceFabricCluster' için örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6d55c-220">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="6d55c-221">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="6d55c-221">AzureRM.Sql</span></span>
* <span data-ttu-id="6d55c-222">Müşterilerin Sql Server örneğine veya Yönetilen Örneğe TDE Sertifikası ekleyebilmeleri için yeni Management.Sql Cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="6d55c-222">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="6d55c-223">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="6d55c-223">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="6d55c-224">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="6d55c-224">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="6d55c-225">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="6d55c-225">AzureRM.Websites</span></span>
* <span data-ttu-id="6d55c-226">Artık `Set-AzureRmWebApp -AssignIdentity` ve `Set-AzureRmWebAppSlot -AssignIdentity` false olarak ayarlandığında site object.Removing önizleme etiketinden Identity özelliğini kaldırıyor.</span><span class="sxs-lookup"><span data-stu-id="6d55c-226">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="6d55c-227">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6d55c-227">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="6d55c-228">`Set-AzureRmWebApp -PhpVersion` geçerli bir php sürümü off değerini destekliyor</span><span class="sxs-lookup"><span data-stu-id="6d55c-228">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="6d55c-229">6.4.0 - Temmuz 2018</span><span class="sxs-lookup"><span data-stu-id="6d55c-229">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="6d55c-230">Genel</span><span class="sxs-lookup"><span data-stu-id="6d55c-230">General</span></span>
* <span data-ttu-id="6d55c-231">Modüllerin çoğu için yardım dosyalarındaki OutputType biçimlendirmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6d55c-231">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="6d55c-232">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="6d55c-232">AzureRM.Profile</span></span>
* <span data-ttu-id="6d55c-233">Temel çıkış türlerine Ps1Xml özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="6d55c-233">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="6d55c-234">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="6d55c-234">AzureRM.Compute</span></span>
* <span data-ttu-id="6d55c-235">VMSS için IP Etiketi özelliği</span><span class="sxs-lookup"><span data-stu-id="6d55c-235">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="6d55c-236">'New-AzureRmVmssIpTagConfig' cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="6d55c-236">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="6d55c-237">New-AzureRmVmssIpConfig cmdlet'ine IpTag parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="6d55c-237">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="6d55c-238">VMSS için Otomatik İşletim Sistemi Geri Alma özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="6d55c-238">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="6d55c-239">New-AzureRmVmssConfig ve Update-AzureRmVmss cmdlet'lerine DisableAutoRollback parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="6d55c-239">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="6d55c-240">VMSS için İşletim Sistemi Yükseltme Geçmişi özelliği</span><span class="sxs-lookup"><span data-stu-id="6d55c-240">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="6d55c-241">Get-AzureRmVmss cmdlet'ine OSUpgradeHistory anahtarı parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="6d55c-241">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="6d55c-242">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="6d55c-242">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="6d55c-243">Aşağıdaki komutlarla Katalog ACL'si için destek eklendi:</span><span class="sxs-lookup"><span data-stu-id="6d55c-243">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="6d55c-244">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="6d55c-244">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="6d55c-245">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="6d55c-245">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="6d55c-246">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="6d55c-246">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="6d55c-247">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6d55c-247">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="6d55c-248">Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry ve Set-AzureRmDataLakeStoreItemAcl için iptal desteği ve ilerleme izleme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="6d55c-248">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="6d55c-249">Export-AzureRmDataLakeStoreChildItemProperties için iptal desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="6d55c-249">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="6d55c-250">Özyinelemeli işlemler gerçekleştiren cmdlet'ler için hata ayıklama iletilerinin boşaltılması hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6d55c-250">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="6d55c-251">DataLake cmdlet'lerinin test konumu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6d55c-251">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="6d55c-252">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="6d55c-252">AzureRM.EventHub</span></span>
* <span data-ttu-id="6d55c-253">Get-AzureRmEventHub ve Get-AzureRmEventHubConsumerGroup Listeleme İşlemleri cmdlet'lerine İsteğe Bağlı MaxCount parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="6d55c-253">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="6d55c-254">New-AzureRmEventHub cmdlet'inde yeni Olay Hub'ı oluşturma sırasında en az bir parametreye ihtiyaç duyma sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="6d55c-254">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="6d55c-255">Varsayılan Parametre kümesi sağlandı.</span><span class="sxs-lookup"><span data-stu-id="6d55c-255">Provided Default Parameter set.</span></span>
* <span data-ttu-id="6d55c-256">Kullanıcının New-AzureRmEventHubKey cmdlet'ine KeyValue eklemesini sağlayan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="6d55c-256">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="6d55c-257">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6d55c-257">AzureRM.KeyVault</span></span>
* <span data-ttu-id="6d55c-258">Get-AzureRmKeyVault -Tag ile tüm kaynakların döndürülmesine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6d55c-258">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="6d55c-259">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="6d55c-259">AzureRM.Network</span></span>
* <span data-ttu-id="6d55c-260">Zone-Redundant VirtualNetworkGateways için yeni SKU'lar kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="6d55c-260">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="6d55c-261">ARM aracılığıyla ExpressRoute Partner API'leri özelliği için yeni komutlar eklendi</span><span class="sxs-lookup"><span data-stu-id="6d55c-261">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="6d55c-262">Get-AzureRmExpressRouteCrossConnection eklendi</span><span class="sxs-lookup"><span data-stu-id="6d55c-262">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="6d55c-263">Set-AzureRmExpressRouteCrossConnection eklendi</span><span class="sxs-lookup"><span data-stu-id="6d55c-263">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="6d55c-264">Add-AzureRmExpressRouteCrossConnectionPeering eklendi</span><span class="sxs-lookup"><span data-stu-id="6d55c-264">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="6d55c-265">Get-AzureRmExpressRouteCrossConnectionPeering eklendi</span><span class="sxs-lookup"><span data-stu-id="6d55c-265">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="6d55c-266">Remove-AzureRmExpressRouteCrossConnectionPeering eklendi</span><span class="sxs-lookup"><span data-stu-id="6d55c-266">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="6d55c-267">Get-AzureRMExpressRouteCrossConnectionArpTable eklendi</span><span class="sxs-lookup"><span data-stu-id="6d55c-267">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="6d55c-268">Get-AzureRMExpressRouteCrossConnectionRouteTable eklendi</span><span class="sxs-lookup"><span data-stu-id="6d55c-268">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="6d55c-269">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary eklendi</span><span class="sxs-lookup"><span data-stu-id="6d55c-269">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="6d55c-270">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="6d55c-270">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="6d55c-271">Get-AzureRmRecoveryServicesBackupStatus cmdlet'i eklendi.</span><span class="sxs-lookup"><span data-stu-id="6d55c-271">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="6d55c-272">Bu cmdlet bir sanal makinenin kimliğini alır ve sanal makinenin abonelik içindeki kasaların koruması altında olup olmadığını denetler.</span><span class="sxs-lookup"><span data-stu-id="6d55c-272">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="6d55c-273">Böyle bir kasa varsa cmdlet, bu kasanın ayrıntılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d55c-273">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="6d55c-274">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="6d55c-274">AzureRM.Resources</span></span>
* <span data-ttu-id="6d55c-275">Get-AzureRmPolicyAssignment cmdlet'leri güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="6d55c-275">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="6d55c-276">Yönetim grubu düzeyinde -Scope değerlerini listeleme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="6d55c-276">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="6d55c-277">Yönetim grubu düzeyinde -Scope değerlerine sahip olan tek atamaları alma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="6d55c-277">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="6d55c-278">control parametresine -Effective ve -All anahtarları eklendi</span><span class="sxs-lookup"><span data-stu-id="6d55c-278">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="6d55c-279">Get/New/Remove/Set-AzureRmPolicyDefinition cmdlet'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6d55c-279">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="6d55c-280">Belirli bir yönetim grubuna işlem uygulamayı sağlayan için -ManagementGroupName parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="6d55c-280">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="6d55c-281">Belirli bir aboneliğe işlem uygulamayı sağlayan Add -SubscriptionId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="6d55c-281">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="6d55c-282">Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlet'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6d55c-282">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="6d55c-283">Belirli bir yönetim grubuna işlem uygulamayı sağlayan -ManagementGroupName parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="6d55c-283">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="6d55c-284">Belirli bir aboneliğe işlem uygulamayı sağlayan Add -SubscriptionId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="6d55c-284">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="6d55c-285">'New-AzureRmResourceGroupDeployment' içinde 'TemplateParameterObject' kullanırken parametrelerde KeyVault gizli dizi başvurusu desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="6d55c-285">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="6d55c-286">'New-AzureRmADAppCredential' için '-EndDate' parametresinin yoksayılmasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6d55c-286">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="6d55c-287">'Add-AzureRmADGroupMember' cmdlet'inin istekte bulunmak için yanlış URL'yi kullandığı sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6d55c-287">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="6d55c-288">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6d55c-288">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="6d55c-289">Kullanıcının New-AzureRmServiceBusKey cmdlet'ine KeyValue eklemesini sağlayan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="6d55c-289">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="6d55c-290">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="6d55c-290">AzureRM.Sql</span></span>
* <span data-ttu-id="6d55c-291">New-AzureRmSqlDatabaseRestorePoint yardımında Kullanıcı Tanımlı Geri Yükleme Noktaları netleştirildi</span><span class="sxs-lookup"><span data-stu-id="6d55c-291">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="6d55c-292">Birden fazla cmdlet'te -ComputeGeneration parametresinin belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6d55c-292">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="6d55c-293">6.3.0 - Haziran 2018</span><span class="sxs-lookup"><span data-stu-id="6d55c-293">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="6d55c-294">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="6d55c-294">AzureRM.Profile</span></span>
* <span data-ttu-id="6d55c-295">Enable-AzureRmContextAutoSave için hata iletileri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6d55c-295">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="6d55c-296">'Connect-AzureRmAccount' cmdlet'i eski bir bağlam olmadan çalıştırıldığında her abonelik için bir bağlam oluşturur</span><span class="sxs-lookup"><span data-stu-id="6d55c-296">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="6d55c-297">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="6d55c-297">Azure.Storage</span></span>
* <span data-ttu-id="6d55c-298">Yardım dosyalarına -Permissions parametresi hakkında daha fazla bilgi eklendi.</span><span class="sxs-lookup"><span data-stu-id="6d55c-298">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="6d55c-299">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="6d55c-299">AzureRM.Compute</span></span>
* <span data-ttu-id="6d55c-300">'Get-AzureRmVmDiskEncryptionStatus' için veri diski bulunmayan VM'lerde karşılaşılan bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6d55c-300">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="6d55c-301">Aşağıdaki cmdlet'leri düzeltmek için bilgisayar istemci kitaplığı sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6d55c-301">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="6d55c-302">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="6d55c-302">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="6d55c-303">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="6d55c-303">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="6d55c-304">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="6d55c-304">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="6d55c-305">Aşağıdaki cmdlet'ler 'operation ID' ve 'operation status' bilgilerini doğru gösterecek şekilde düzeltildi:</span><span class="sxs-lookup"><span data-stu-id="6d55c-305">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="6d55c-306">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6d55c-306">Start-AzureRmVM</span></span>
    - <span data-ttu-id="6d55c-307">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6d55c-307">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="6d55c-308">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6d55c-308">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="6d55c-309">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6d55c-309">Set-AzureRmVM</span></span>
    - <span data-ttu-id="6d55c-310">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6d55c-310">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="6d55c-311">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6d55c-311">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="6d55c-312">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="6d55c-312">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="6d55c-313">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="6d55c-313">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="6d55c-314">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6d55c-314">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="6d55c-315">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6d55c-315">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="6d55c-316">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6d55c-316">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="6d55c-317">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6d55c-317">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="6d55c-318">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="6d55c-318">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="6d55c-319">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="6d55c-319">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="6d55c-320">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="6d55c-320">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="6d55c-321">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="6d55c-321">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="6d55c-322">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="6d55c-322">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="6d55c-323">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="6d55c-323">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="6d55c-324">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="6d55c-324">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="6d55c-325">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="6d55c-325">AzureRM.EventGrid</span></span>
* <span data-ttu-id="6d55c-326">Gerekli olması halinde parametrelerin boş dizeyle değiştirilmesine izin vermek için Update-AzureRmEventGridSubscription cmdlet'i içindeki SubjectBeginsWith/SubjectEndsWith için ValidateNotNullOrEmpty doğrulama koşulları kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="6d55c-326">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="6d55c-327">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6d55c-327">AzureRM.KeyVault</span></span>
* <span data-ttu-id="6d55c-328">Get-AzureRmKeyVault -Tag çalıştırıldığında etiket döndürülmeme sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6d55c-328">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="6d55c-329">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6d55c-329">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="6d55c-330">Policy Insights cmdlet'leri genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="6d55c-330">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="6d55c-331">API 2018-04-04 sürümünü kullanın</span><span class="sxs-lookup"><span data-stu-id="6d55c-331">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="6d55c-332">PolicyDefinitionReferenceId, Get-AzureRmPolicyStateSummary sonuçlarına eklendi</span><span class="sxs-lookup"><span data-stu-id="6d55c-332">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="6d55c-333">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="6d55c-333">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="6d55c-334">RecoveryServices.Backup cmdlet'lerine -Vault parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="6d55c-334">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="6d55c-335">Bu parametre iletildiğinde Set-AzureRmRecoveryServicesContext cmdlet'ini geçersiz kılar.</span><span class="sxs-lookup"><span data-stu-id="6d55c-335">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="6d55c-336">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="6d55c-336">AzureRM.Sql</span></span>
* <span data-ttu-id="6d55c-337">Yardım dosyasındaki Get-AzureRmSqlDatabaseExpanded örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6d55c-337">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="6d55c-338">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="6d55c-338">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="6d55c-339">Yardım dosyasındaki Add-AzureRmTrafficManagerEndpointConfig bölümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6d55c-339">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="6d55c-340">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="6d55c-340">AzureRM.Websites</span></span>
* <span data-ttu-id="6d55c-341">'Set-AzureRmWebApp', -AssignIdentity kullanıldığında AppSettings verilerini geçersiz kılmayacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6d55c-341">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="6d55c-342">'New-AzureRmWebAppSlot', isteğe bağlı parametre olarak AppServicePlan girişini kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6d55c-342">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="6d55c-343">6.2.1 - Haziran 2018</span><span class="sxs-lookup"><span data-stu-id="6d55c-343">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="6d55c-344">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6d55c-344">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="6d55c-345">PSWorkspace modeli Network için tür parametresini kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6d55c-345">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="6d55c-346">6.2.0 - Haziran 2018</span><span class="sxs-lookup"><span data-stu-id="6d55c-346">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="6d55c-347">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="6d55c-347">AzureRM.Profile</span></span>
* <span data-ttu-id="6d55c-348">Modülün içeri aktarılması sırasında Newtonsoft.Json 10.0.3 sürümünün yüklenmemesine ilişkin sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6d55c-348">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="6d55c-349">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="6d55c-349">AzureRM.Compute</span></span>
* <span data-ttu-id="6d55c-350">VMSS VM Güncelleştirme özelliği</span><span class="sxs-lookup"><span data-stu-id="6d55c-350">VMSS VM Update feature</span></span>
    - <span data-ttu-id="6d55c-351">'Update-AzureRmVmssVM' ve 'New-AzureRmVMDataDisk' cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="6d55c-351">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="6d55c-352">VMSS VM’sine veri diski eklemeyi desteklemek için 'Add-AzureRmVMDataDisk' cmdlet’ine VirtualMachineScaleSetVM parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="6d55c-352">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="6d55c-353">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="6d55c-353">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="6d55c-354">ADF .Net SDK sürümü, aşağıdaki değişiklikleri içeren 0.8.0-preview sürümüne güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="6d55c-354">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="6d55c-355">Fabrika deposunu yapılandırma işlemi eklendi</span><span class="sxs-lookup"><span data-stu-id="6d55c-355">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="6d55c-356">QuickBooks LinkedService, consumerKey ve consumerSecret özelliklerini kullanıma sunmak üzere güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6d55c-356">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="6d55c-357">SecretBase’ten Object’e birkaç model türü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6d55c-357">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="6d55c-358">Blob Etkinliklerini tetikleme eklendi</span><span class="sxs-lookup"><span data-stu-id="6d55c-358">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="6d55c-359">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6d55c-359">AzureRM.KeyVault</span></span>
* <span data-ttu-id="6d55c-360">Belgeler örnek çıktı ile güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6d55c-360">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="6d55c-361">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="6d55c-361">AzureRM.Network</span></span>
* <span data-ttu-id="6d55c-362">Ağ İzleyicisi cmdlet’leri üzerindeki Trafik Analizi parametreleri etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="6d55c-362">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="6d55c-363">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="6d55c-363">AzureRM.Resources</span></span>
* <span data-ttu-id="6d55c-364">'Get-AzureRmResource' cmdlet’inden döndürülen 'PSResource' nesnesinin 'Properties' özelliğiyle ilgili bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6d55c-364">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="6d55c-365">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="6d55c-365">AzureRM.Scheduler</span></span>
* <span data-ttu-id="6d55c-366">Güncelleştirilen ServiceBusQueueJob’ın yeni Kimlik Doğrulaması değerlerini ayarlamamasıyla ilgili bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6d55c-366">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="6d55c-367">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="6d55c-367">AzureRM.Sql</span></span>
* <span data-ttu-id="6d55c-368">Şu cmdlet’ler isteğe bağlı LicenseType parametresiyle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="6d55c-368">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="6d55c-369">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6d55c-369">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="6d55c-370">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="6d55c-370">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="6d55c-371">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="6d55c-371">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="6d55c-372">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="6d55c-372">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="6d55c-373">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6d55c-373">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="6d55c-374">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="6d55c-374">AzureRM.Websites</span></span>
* <span data-ttu-id="6d55c-375">'New-AzureRMWebApp' Strategy kütüphanesindeki ortak algoritmaları kullanmak üzere güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="6d55c-375">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="6d55c-376">6.1.0 - Mayıs 2018</span><span class="sxs-lookup"><span data-stu-id="6d55c-376">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="6d55c-377">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="6d55c-377">AzureRM.Profile</span></span>
* <span data-ttu-id="6d55c-378">'Clear-AzureRmContext' komutunun çalıştırılmasının boş bir bağlamı önceki varsayılan bağlamın adıyla tutmasına ve böylece kullanıcının eski ad ile yeni bir bağlam oluşturamadığı bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6d55c-378">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="6d55c-379">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6d55c-379">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="6d55c-380">AS’de Ağ geçidi ilişkilendirme/ilişkilendirme kaldırma işlemlerini etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="6d55c-380">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="6d55c-381">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6d55c-381">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="6d55c-382">ApiVersions, ApiReleases ve ApiRevisions desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="6d55c-382">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="6d55c-383">ServiceFabric Arka Ucu desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="6d55c-383">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="6d55c-384">Application Insights Günlükçüsü desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="6d55c-384">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="6d55c-385">‘Temel’ sku’yu Api Yönetim hizmetinin geçerli sku’su olarak algılama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="6d55c-385">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="6d55c-386">Özel CA tarafından Kök veya CA olarak yayınlanan Sertifikaları yükleme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="6d55c-386">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="6d55c-387">Özel SSL sertifikalarını KeyVault ve Çoklu ara sunucu ana bilgisayar adlarıyla kabul etme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="6d55c-387">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="6d55c-388">MSI kimliği desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="6d55c-388">Added support for MSI identity</span></span>
* <span data-ttu-id="6d55c-389">İlkeleri Url ile kabul etme desteği eklendi NOT: Aşağıdaki cmdlet’ler gelecekteki sürümlerde kullanım dışı kalacaktır</span><span class="sxs-lookup"><span data-stu-id="6d55c-389">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="6d55c-390">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="6d55c-390">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="6d55c-391">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="6d55c-391">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="6d55c-392">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="6d55c-392">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="6d55c-393">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="6d55c-393">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="6d55c-394">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="6d55c-394">AzureRM.Batch</span></span>
* <span data-ttu-id="6d55c-395">Yeni Get-AzureBatchPoolNodeCounts cmdlet’ini yayınlama</span><span class="sxs-lookup"><span data-stu-id="6d55c-395">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="6d55c-396">Yeni AzureBatchComputeNodeServiceLogUpload cmdlet’ini yayınlama</span><span class="sxs-lookup"><span data-stu-id="6d55c-396">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="6d55c-397">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="6d55c-397">AzureRM.Consumption</span></span>
* <span data-ttu-id="6d55c-398">Get-AzureRmConsumptionUsageDetail cmdlet’inde yeni Expand, ResourceGroup, InstanceName, InstanceId, Tags ve Top parametrelerini ekleme</span><span class="sxs-lookup"><span data-stu-id="6d55c-398">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="6d55c-399">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6d55c-399">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="6d55c-400">Export-AzureRmDataLakeStoreChildItemProperties için düzeltme örneği</span><span class="sxs-lookup"><span data-stu-id="6d55c-400">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="6d55c-401">Set-AzureRmDataLakeStoreItemAclEntry komutunda Özyineleme durumu için null parametresi özel durumunu düzeltme</span><span class="sxs-lookup"><span data-stu-id="6d55c-401">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="6d55c-402">Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry’ye yönelik yardım dosyalarını düzeltme</span><span class="sxs-lookup"><span data-stu-id="6d55c-402">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="6d55c-403">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="6d55c-403">AzureRM.Network</span></span>
* <span data-ttu-id="6d55c-404">Ağ SDK sürümünü 18.0.0-önizleme’den 19.0.0-önizlemeye yükseltme</span><span class="sxs-lookup"><span data-stu-id="6d55c-404">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="6d55c-405">Protokol yapılandırması oluşturma cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="6d55c-405">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="6d55c-406">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="6d55c-406">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="6d55c-407">Varolan express route bağlantı hattına yeni bir bağlantı hattı ekleme cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="6d55c-407">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="6d55c-408">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="6d55c-408">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="6d55c-409">Varolan express route bağlantı hattındaki bir bağlantı hattı bağlantısını kaldırma cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="6d55c-409">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="6d55c-410">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="6d55c-410">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="6d55c-411">Bağlantı hattı bağlantısı alma cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="6d55c-411">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="6d55c-412">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="6d55c-412">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="6d55c-413">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6d55c-413">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="6d55c-414">Oluşturulan sertifikalarla sunucu kimlik doğrulaması kullanımı düzeltildi (Sorun No. 5998)</span><span class="sxs-lookup"><span data-stu-id="6d55c-414">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="6d55c-415">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="6d55c-415">AzureRM.Sql</span></span>
* <span data-ttu-id="6d55c-416">AuditActions veya AuditActionGroups’un kaldırılmasını sağlamak üzere Denetim cmdlet’leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6d55c-416">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="6d55c-417">Yeni bir esnek saklama ilkesi ayarlarken komutun ‘Azure kurtarma hizmeti kasası ve ilkesiyle uzun süreli saklama ilkesini yapılandırma artık desteklenmiyor. Lütfen yeni esnek saklama ilkesi ile istek gönderin’ hatasını verdiği Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="6d55c-417">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="6d55c-418">komutuna ilişkin sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="6d55c-418">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="6d55c-419">Ölçek ve katman ilişkili özelliklere yönelik Sku özelliğini destekleyen yeni Veritabanı API’sini kullanmak için tüm Azure Sql Database/ElasticPool Creation/Update cmdlet’lerini güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="6d55c-419">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="6d55c-420">Güncelleştirilen cmlet’ler arasında şunlar yer almaktadır:</span><span class="sxs-lookup"><span data-stu-id="6d55c-420">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="6d55c-421">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6d55c-421">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="6d55c-422">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="6d55c-422">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="6d55c-423">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="6d55c-423">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="6d55c-424">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="6d55c-424">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="6d55c-425">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6d55c-425">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="6d55c-426">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="6d55c-426">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="6d55c-427">-Name parametresini kullanırken -ResourceGroupName parametresinin gerekli olması için 'Get-AzureRmTrafficManagerProfile'a yönelik parametreleri güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="6d55c-427">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>