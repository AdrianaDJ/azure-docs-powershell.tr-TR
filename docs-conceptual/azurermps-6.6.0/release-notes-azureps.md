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
ms.openlocfilehash: 340c1d2d28e1b97cdd2ec98033361eb00b4302da
ms.sourcegitcommit: 72086f8d368ec84bd403e802305acfc336c08978
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/14/2018
ms.locfileid: "43018595"
---
# <a name="release-notes"></a><span data-ttu-id="2b32a-103">Sürüm notları</span><span class="sxs-lookup"><span data-stu-id="2b32a-103">Release notes</span></span>

<span data-ttu-id="2b32a-104">Azure PowerShell'in bu sürümünde yapılan değişikliklerin listesi aşağıda verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="2b32a-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="660---july-2018"></a><span data-ttu-id="2b32a-105">6.6.0 - Temmuz 2018</span><span class="sxs-lookup"><span data-stu-id="2b32a-105">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="2b32a-106">Genel</span><span class="sxs-lookup"><span data-stu-id="2b32a-106">General</span></span>
* <span data-ttu-id="2b32a-107">Tüm yardım dosyaları tam parametre türleriyle doğru giriş/çıkış türlerini içerecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="2b32a-107">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="2b32a-108">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="2b32a-108">AzureRM.Profile</span></span>
* <span data-ttu-id="2b32a-109">Kaynağın geçerli yapılandırmasının hedef kaynakla uyumlu olduğunu doğrulayabilmek için Common.Strategy kitaplığı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="2b32a-109">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="2b32a-110">Common.Storage'a ps1xml türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="2b32a-110">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="2b32a-111">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="2b32a-111">Azure.Storage</span></span>
* <span data-ttu-id="2b32a-112">DefaultProfile’dan Depolama Bağlamı almak için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="2b32a-112">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="2b32a-113">Cmdlet'lerin çıkış türü özelliklerine Ps1XmlAttribute eklendi.</span><span class="sxs-lookup"><span data-stu-id="2b32a-113">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="2b32a-114">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2b32a-114">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="2b32a-115">https://github.com/Azure/azure-powershell/issues/6370 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="2b32a-115">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="2b32a-116">PsApiManagementApi'yi ApiContract'e çevirmek için Automapper hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="2b32a-116">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="2b32a-117">https://github.com/Azure/azure-powershell/issues/6515 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="2b32a-117">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="2b32a-118">Kodlama Türü ile aşırı yüklemeyi önlemek için File.Save hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="2b32a-118">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="2b32a-119">https://github.com/Azure/azure-powershell/issues/6560 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="2b32a-119">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="2b32a-120">apiId üzerindeki desen özel durumunu düzelten 4.0.3 Nuget sürümüne yükseltildi</span><span class="sxs-lookup"><span data-stu-id="2b32a-120">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="2b32a-121">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="2b32a-121">AzureRM.Compute</span></span>
* <span data-ttu-id="2b32a-122">PremiumLRS depolama hesap türü yeniden adlandırması nedeniyle New-AzureRmVm'de DiskFileParameterSet kullanılarak sanal makine oluşturmanın başarısız olmasıyla ilgili hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="2b32a-122">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="2b32a-123">Invoke-AzureRmVMRunCommand cmdlet'i düzeltildi</span><span class="sxs-lookup"><span data-stu-id="2b32a-123">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="2b32a-124">Abonelikteki tüm kullanılabilir kümelerin listelenebilmesi için Get-AzureRmAvailabilitySet güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="2b32a-124">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="2b32a-125">(ResouceGroupName parametresi artık isteğe bağlı.)</span><span class="sxs-lookup"><span data-stu-id="2b32a-125">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="2b32a-126">Uygun sanal makinelerde Hızlandırılmış Ağı etkinleştirmek için 'New-AzureRmVm' cmdlet'inin SimpleParameterSet öğesi güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="2b32a-126">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="2b32a-127">Kullanıcının belirttiği LB zaten mevcut olduğunda vmss oluşturmanın başarısız olması için New-AzureRmVmss basit parametre kümesi güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="2b32a-127">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="2b32a-128">New-AzureRmDisk örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="2b32a-128">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="2b32a-129">'New-AzureRmVM' için örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="2b32a-129">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="2b32a-130">Set-AzureRmVMOSDisk açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="2b32a-130">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="2b32a-131">Yazımı ve ön eki düzeltmek amacıyla Set-AzureRmVMBginfoExtension için Örnek 1 güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="2b32a-131">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="2b32a-132">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="2b32a-132">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="2b32a-133">ADF .Net SDK sürümü 1.1.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="2b32a-133">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="2b32a-134">Veri fabrikaları arasında paylaşılan şirket içinde barındırılan tümleştirme çalışma zamanı desteği.</span><span class="sxs-lookup"><span data-stu-id="2b32a-134">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="2b32a-135">Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet'ine yeni -SharedIntegrationRuntimeResourceId parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="2b32a-135">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="2b32a-136">Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet'ine isteğe bağlı yeni -LinkedDataFactoryName parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="2b32a-136">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="2b32a-137">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2b32a-137">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="2b32a-138">DataPlane SDK'sı (Microsoft.Azure.DataLake.Store) sürümü 1.1.9'a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="2b32a-138">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="2b32a-139">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="2b32a-139">AzureRM.EventHub</span></span>
* <span data-ttu-id="2b32a-140">Kaldırma cmdlet'lerine InputObject ve ResourceId yöneltmesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="2b32a-140">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="2b32a-141">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="2b32a-141">AzureRM.Insights</span></span>
* <span data-ttu-id="2b32a-142">Yardım dosyalarındaki OutputType biçimlendirmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="2b32a-142">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="2b32a-143">Microsoft.Azure.Management.Monitor SDK 0.19.1-preview kullanımı</span><span class="sxs-lookup"><span data-stu-id="2b32a-143">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="2b32a-144">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2b32a-144">AzureRM.KeyVault</span></span>
* <span data-ttu-id="2b32a-145">Set-AzureRmKeyVaultAccessPolicy'de yönlendirme sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="2b32a-145">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="2b32a-146">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="2b32a-146">AzureRM.Network</span></span>
* <span data-ttu-id="2b32a-147">LoadBalancerInboundNatPoolConfig cmdlet'leri için örnekler eklendi.</span><span class="sxs-lookup"><span data-stu-id="2b32a-147">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="2b32a-148">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="2b32a-148">AzureRM.Resources</span></span>
* <span data-ttu-id="2b32a-149">'Get-AzureRmResource' için hem etiket adı hem de değer sağlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="2b32a-149">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="2b32a-150">'Set-AzureRmResource' için yönlendirme senaryosu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="2b32a-150">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="2b32a-151">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2b32a-151">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="2b32a-152">Kaldırma cmdlet'lerine InputObject ve ResourceId yöneltmesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="2b32a-152">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="2b32a-153">birkaç sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="2b32a-153">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="2b32a-154">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="2b32a-154">AzureRM.Sql</span></span>
* <span data-ttu-id="2b32a-155">Aşağıdaki cmdlet'lere Sunucu Gelişmiş Tehdit Koruması desteği ekleniyor:</span><span class="sxs-lookup"><span data-stu-id="2b32a-155">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="2b32a-156">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="2b32a-156">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="2b32a-157">Aşağıdaki cmdlet'lere Güvenlik Açığı Değerlendirme desteği ekleniyor:</span><span class="sxs-lookup"><span data-stu-id="2b32a-157">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="2b32a-158">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="2b32a-158">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="2b32a-159">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="2b32a-159">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="2b32a-160">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="2b32a-160">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="2b32a-161">Remove-AzureRmSqlServerFirewallRulecmdlet'indeki örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="2b32a-161">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="2b32a-162">Get-AzureSqlSyncGroupLog içinde ABD temelli olmayan kültürde yanlış tarih saat işlemesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="2b32a-162">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="2b32a-163">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="2b32a-163">AzureRM.Storage</span></span>
* <span data-ttu-id="2b32a-164">Cmdlet'lerin çıkış türü özelliklerine Ps1XmlAttribute eklendi</span><span class="sxs-lookup"><span data-stu-id="2b32a-164">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="2b32a-165">Tablo görünümünde StorageAccount cmdlet'i çıkışı gösteriliyor</span><span class="sxs-lookup"><span data-stu-id="2b32a-165">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="2b32a-166">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2b32a-166">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="2b32a-167">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2b32a-167">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="2b32a-168">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2b32a-168">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="2b32a-169">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="2b32a-169">AzureRM.Tags</span></span>
* <span data-ttu-id="2b32a-170">Tag cmdlet'inin yardımında hatayı deyim kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="2b32a-170">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="2b32a-171">6.5.0 - Temmuz 2018</span><span class="sxs-lookup"><span data-stu-id="2b32a-171">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="2b32a-172">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="2b32a-172">AzureRM.Profile</span></span>
* <span data-ttu-id="2b32a-173">'Get-AzureRmContextAutosaveSetting' için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="2b32a-173">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="2b32a-174">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="2b32a-174">Azure.Storage</span></span>
* <span data-ttu-id="2b32a-175">Salt yazılır Sas belirteciyle Karşıya Yükleme Blobu veya Dosyası desteği</span><span class="sxs-lookup"><span data-stu-id="2b32a-175">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="2b32a-176">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="2b32a-176">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="2b32a-177">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="2b32a-177">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="2b32a-178">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2b32a-178">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="2b32a-179">AS'ye gerekli ResourceGroupName özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="2b32a-179">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="2b32a-180">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="2b32a-180">AzureRM.Automation</span></span>
* <span data-ttu-id="2b32a-181">'New-AzureRMAutomationSchedule' için yardım güncelleştirildi ve örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="2b32a-181">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="2b32a-182">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="2b32a-182">AzureRM.Compute</span></span>
* <span data-ttu-id="2b32a-183">Update/New-AzureRmAvailabilitySet komutlarına -Tag parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="2b32a-183">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="2b32a-184">'Add-AzureRmVmssExtension' için örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="2b32a-184">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="2b32a-185">'Remove-AzureRmVmssExtension' için örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="2b32a-185">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="2b32a-186">'Set-AzureRmVMAccessExtension' için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="2b32a-186">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="2b32a-187">New-AzureRmVmss için SimpleParameterSet güncelleştirilerek SinglePlacementGroup varsayılan olarak false değerine ayarlandı ve kullanıcının tek yerleşim grubunda VMSS oluşturmasına olanak tanıyan 'SinglePlacementGroup' geçiş parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="2b32a-187">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="2b32a-188">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="2b32a-188">AzureRM.EventHub</span></span>
* <span data-ttu-id="2b32a-189">PSEventHubDRConfigurationAttributes sınıfına, çoğaltma işlemi devam ederken bekleyen çoğaltma işlemlerinin sayısını veren salt okunur 'PendingReplicationOperationsCount' özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="2b32a-189">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="2b32a-190">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2b32a-190">AzureRM.KeyVault</span></span>
* <span data-ttu-id="2b32a-191">Set-AzureRmKeyVaultAccessPolicy için hata iletisi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="2b32a-191">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="2b32a-192">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="2b32a-192">AzureRM.LogicApp</span></span>
* <span data-ttu-id="2b32a-193">New-AzureRmLogicApp’te "parametre kümesi çözümlenemedi" hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="2b32a-193">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="2b32a-194">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="2b32a-194">AzureRM.Network</span></span>
* <span data-ttu-id="2b32a-195">Set/Add-AzureRmVirtualNetworkPeering için birden çok Kiracıdaki Sanal Makineler arasında eşleme etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="2b32a-195">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="2b32a-196">Aşağıdaki cmdlet’ler Application Gateway için güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="2b32a-196">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="2b32a-197">New-AzureRmApplicationGateway : EnableFIPS bayrağı ve Zones desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="2b32a-197">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="2b32a-198">New-AzureRmApplicationGatewaySku : Yeni Standard_v2 ve WAF_v2 sku'ları eklendi</span><span class="sxs-lookup"><span data-stu-id="2b32a-198">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="2b32a-199">Set-AzureRmApplicationGatewaySku : Yeni Standard_v2 ve WAF_v2 sku'ları eklendi</span><span class="sxs-lookup"><span data-stu-id="2b32a-199">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="2b32a-200">RouteTable cmdlet’leri en son oluşturucu sürümüyle yeniden oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="2b32a-200">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="2b32a-201">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="2b32a-201">AzureRM.Relay</span></span>
* <span data-ttu-id="2b32a-202">Markdown dosyaları güncelleştirildi, örnekteki parametre adı sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="2b32a-202">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="2b32a-203">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="2b32a-203">AzureRM.Resources</span></span>
* <span data-ttu-id="2b32a-204">Roleassignment ve roledefinition cmdlet’leri güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="2b32a-204">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="2b32a-205">Disk belleğinin parçası olarak yapılan ek roledefinition çağrıları kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="2b32a-205">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="2b32a-206">Get-AzureRmRoleAssignment cmdlet’i düzeltildi</span><span class="sxs-lookup"><span data-stu-id="2b32a-206">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="2b32a-207">-ExpandPrincipalGroups komut parametresi işlevselliği düzeltildi</span><span class="sxs-lookup"><span data-stu-id="2b32a-207">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="2b32a-208">'-ResourceType' parametresinin büyük/küçük harfe duyarlı olduğu 'Get-AzureRmResource' sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="2b32a-208">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="2b32a-209">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2b32a-209">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="2b32a-210">Liste cmdlet’lerine top ve skip parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="2b32a-210">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="2b32a-211">Standard'dan Premium NameSpace'e geçiş cmdlet’leri eklendi :</span><span class="sxs-lookup"><span data-stu-id="2b32a-211">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="2b32a-212">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="2b32a-212">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="2b32a-213">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="2b32a-213">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="2b32a-214">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="2b32a-214">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="2b32a-215">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="2b32a-215">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="2b32a-216">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="2b32a-216">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="2b32a-217">PSServiceBusDRConfigurationAttributes sınıfına, çoğaltma işlemi sürerken beklemede olan çoğaltma işlemi sayısını veren salt okunur 'PendingReplicationOperationsCount' özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="2b32a-217">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="2b32a-218">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2b32a-218">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="2b32a-219">'New-AzureRmServiceFabricCluster' için örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="2b32a-219">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="2b32a-220">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="2b32a-220">AzureRM.Sql</span></span>
* <span data-ttu-id="2b32a-221">Müşterilerin Sql Server örneğine veya Yönetilen Örneğe TDE Sertifikası ekleyebilmeleri için yeni Management.Sql Cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="2b32a-221">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="2b32a-222">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="2b32a-222">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="2b32a-223">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="2b32a-223">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="2b32a-224">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="2b32a-224">AzureRM.Websites</span></span>
* <span data-ttu-id="2b32a-225">Artık `Set-AzureRmWebApp -AssignIdentity` ve `Set-AzureRmWebAppSlot -AssignIdentity` false olarak ayarlandığında site object.Removing önizleme etiketinden Identity özelliğini kaldırıyor.</span><span class="sxs-lookup"><span data-stu-id="2b32a-225">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="2b32a-226">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="2b32a-226">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="2b32a-227">`Set-AzureRmWebApp -PhpVersion` geçerli bir php sürümü off değerini destekliyor</span><span class="sxs-lookup"><span data-stu-id="2b32a-227">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="2b32a-228">6.4.0 - Temmuz 2018</span><span class="sxs-lookup"><span data-stu-id="2b32a-228">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="2b32a-229">Genel</span><span class="sxs-lookup"><span data-stu-id="2b32a-229">General</span></span>
* <span data-ttu-id="2b32a-230">Modüllerin çoğu için yardım dosyalarındaki OutputType biçimlendirmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="2b32a-230">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="2b32a-231">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="2b32a-231">AzureRM.Profile</span></span>
* <span data-ttu-id="2b32a-232">Temel çıkış türlerine Ps1Xml özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="2b32a-232">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="2b32a-233">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="2b32a-233">AzureRM.Compute</span></span>
* <span data-ttu-id="2b32a-234">VMSS için IP Etiketi özelliği</span><span class="sxs-lookup"><span data-stu-id="2b32a-234">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="2b32a-235">'New-AzureRmVmssIpTagConfig' cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="2b32a-235">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="2b32a-236">New-AzureRmVmssIpConfig cmdlet'ine IpTag parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="2b32a-236">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="2b32a-237">VMSS için Otomatik İşletim Sistemi Geri Alma özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="2b32a-237">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="2b32a-238">New-AzureRmVmssConfig ve Update-AzureRmVmss cmdlet'lerine DisableAutoRollback parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="2b32a-238">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="2b32a-239">VMSS için İşletim Sistemi Yükseltme Geçmişi özelliği</span><span class="sxs-lookup"><span data-stu-id="2b32a-239">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="2b32a-240">Get-AzureRmVmss cmdlet'ine OSUpgradeHistory anahtarı parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="2b32a-240">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="2b32a-241">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="2b32a-241">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="2b32a-242">Aşağıdaki komutlarla Katalog ACL'si için destek eklendi:</span><span class="sxs-lookup"><span data-stu-id="2b32a-242">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="2b32a-243">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="2b32a-243">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="2b32a-244">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="2b32a-244">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="2b32a-245">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="2b32a-245">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="2b32a-246">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2b32a-246">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="2b32a-247">Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry ve Set-AzureRmDataLakeStoreItemAcl için iptal desteği ve ilerleme izleme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="2b32a-247">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="2b32a-248">Export-AzureRmDataLakeStoreChildItemProperties için iptal desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="2b32a-248">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="2b32a-249">Özyinelemeli işlemler gerçekleştiren cmdlet'ler için hata ayıklama iletilerinin boşaltılması hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="2b32a-249">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="2b32a-250">DataLake cmdlet'lerinin test konumu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="2b32a-250">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="2b32a-251">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="2b32a-251">AzureRM.EventHub</span></span>
* <span data-ttu-id="2b32a-252">Get-AzureRmEventHub ve Get-AzureRmEventHubConsumerGroup Listeleme İşlemleri cmdlet'lerine İsteğe Bağlı MaxCount parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="2b32a-252">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="2b32a-253">New-AzureRmEventHub cmdlet'inde yeni Olay Hub'ı oluşturma sırasında en az bir parametreye ihtiyaç duyma sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="2b32a-253">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="2b32a-254">Varsayılan Parametre kümesi sağlandı.</span><span class="sxs-lookup"><span data-stu-id="2b32a-254">Provided Default Parameter set.</span></span>
* <span data-ttu-id="2b32a-255">Kullanıcının New-AzureRmEventHubKey cmdlet'ine KeyValue eklemesini sağlayan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="2b32a-255">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="2b32a-256">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2b32a-256">AzureRM.KeyVault</span></span>
* <span data-ttu-id="2b32a-257">Get-AzureRmKeyVault -Tag ile tüm kaynakların döndürülmesine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="2b32a-257">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="2b32a-258">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="2b32a-258">AzureRM.Network</span></span>
* <span data-ttu-id="2b32a-259">Zone-Redundant VirtualNetworkGateways için yeni SKU'lar kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="2b32a-259">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="2b32a-260">ARM aracılığıyla ExpressRoute Partner API'leri özelliği için yeni komutlar eklendi</span><span class="sxs-lookup"><span data-stu-id="2b32a-260">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="2b32a-261">Get-AzureRmExpressRouteCrossConnection eklendi</span><span class="sxs-lookup"><span data-stu-id="2b32a-261">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="2b32a-262">Set-AzureRmExpressRouteCrossConnection eklendi</span><span class="sxs-lookup"><span data-stu-id="2b32a-262">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="2b32a-263">Add-AzureRmExpressRouteCrossConnectionPeering eklendi</span><span class="sxs-lookup"><span data-stu-id="2b32a-263">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="2b32a-264">Get-AzureRmExpressRouteCrossConnectionPeering eklendi</span><span class="sxs-lookup"><span data-stu-id="2b32a-264">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="2b32a-265">Remove-AzureRmExpressRouteCrossConnectionPeering eklendi</span><span class="sxs-lookup"><span data-stu-id="2b32a-265">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="2b32a-266">Get-AzureRMExpressRouteCrossConnectionArpTable eklendi</span><span class="sxs-lookup"><span data-stu-id="2b32a-266">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="2b32a-267">Get-AzureRMExpressRouteCrossConnectionRouteTable eklendi</span><span class="sxs-lookup"><span data-stu-id="2b32a-267">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="2b32a-268">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary eklendi</span><span class="sxs-lookup"><span data-stu-id="2b32a-268">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="2b32a-269">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="2b32a-269">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="2b32a-270">Get-AzureRmRecoveryServicesBackupStatus cmdlet'i eklendi.</span><span class="sxs-lookup"><span data-stu-id="2b32a-270">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="2b32a-271">Bu cmdlet bir sanal makinenin kimliğini alır ve sanal makinenin abonelik içindeki kasaların koruması altında olup olmadığını denetler.</span><span class="sxs-lookup"><span data-stu-id="2b32a-271">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="2b32a-272">Böyle bir kasa varsa cmdlet, bu kasanın ayrıntılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b32a-272">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="2b32a-273">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="2b32a-273">AzureRM.Resources</span></span>
* <span data-ttu-id="2b32a-274">Get-AzureRmPolicyAssignment cmdlet'leri güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="2b32a-274">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="2b32a-275">Yönetim grubu düzeyinde -Scope değerlerini listeleme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="2b32a-275">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="2b32a-276">Yönetim grubu düzeyinde -Scope değerlerine sahip olan tek atamaları alma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="2b32a-276">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="2b32a-277">control parametresine -Effective ve -All anahtarları eklendi</span><span class="sxs-lookup"><span data-stu-id="2b32a-277">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="2b32a-278">Get/New/Remove/Set-AzureRmPolicyDefinition cmdlet'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="2b32a-278">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="2b32a-279">Belirli bir yönetim grubuna işlem uygulamayı sağlayan için -ManagementGroupName parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="2b32a-279">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="2b32a-280">Belirli bir aboneliğe işlem uygulamayı sağlayan Add -SubscriptionId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="2b32a-280">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="2b32a-281">Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlet'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="2b32a-281">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="2b32a-282">Belirli bir yönetim grubuna işlem uygulamayı sağlayan -ManagementGroupName parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="2b32a-282">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="2b32a-283">Belirli bir aboneliğe işlem uygulamayı sağlayan Add -SubscriptionId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="2b32a-283">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="2b32a-284">'New-AzureRmResourceGroupDeployment' içinde 'TemplateParameterObject' kullanırken parametrelerde KeyVault gizli dizi başvurusu desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="2b32a-284">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="2b32a-285">'New-AzureRmADAppCredential' için '-EndDate' parametresinin yoksayılmasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="2b32a-285">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="2b32a-286">'Add-AzureRmADGroupMember' cmdlet'inin istekte bulunmak için yanlış URL'yi kullandığı sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="2b32a-286">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="2b32a-287">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2b32a-287">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="2b32a-288">Kullanıcının New-AzureRmServiceBusKey cmdlet'ine KeyValue eklemesini sağlayan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="2b32a-288">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="2b32a-289">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="2b32a-289">AzureRM.Sql</span></span>
* <span data-ttu-id="2b32a-290">New-AzureRmSqlDatabaseRestorePoint yardımında Kullanıcı Tanımlı Geri Yükleme Noktaları netleştirildi</span><span class="sxs-lookup"><span data-stu-id="2b32a-290">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="2b32a-291">Birden fazla cmdlet'te -ComputeGeneration parametresinin belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="2b32a-291">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="2b32a-292">6.3.0 - Haziran 2018</span><span class="sxs-lookup"><span data-stu-id="2b32a-292">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="2b32a-293">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="2b32a-293">AzureRM.Profile</span></span>
* <span data-ttu-id="2b32a-294">Enable-AzureRmContextAutoSave için hata iletileri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="2b32a-294">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="2b32a-295">'Connect-AzureRmAccount' cmdlet'i eski bir bağlam olmadan çalıştırıldığında her abonelik için bir bağlam oluşturur</span><span class="sxs-lookup"><span data-stu-id="2b32a-295">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="2b32a-296">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="2b32a-296">Azure.Storage</span></span>
* <span data-ttu-id="2b32a-297">Yardım dosyalarına -Permissions parametresi hakkında daha fazla bilgi eklendi.</span><span class="sxs-lookup"><span data-stu-id="2b32a-297">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="2b32a-298">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="2b32a-298">AzureRM.Compute</span></span>
* <span data-ttu-id="2b32a-299">'Get-AzureRmVmDiskEncryptionStatus' için veri diski bulunmayan VM'lerde karşılaşılan bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="2b32a-299">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="2b32a-300">Aşağıdaki cmdlet'leri düzeltmek için bilgisayar istemci kitaplığı sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="2b32a-300">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="2b32a-301">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="2b32a-301">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="2b32a-302">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="2b32a-302">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="2b32a-303">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="2b32a-303">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="2b32a-304">Aşağıdaki cmdlet'ler 'operation ID' ve 'operation status' bilgilerini doğru gösterecek şekilde düzeltildi:</span><span class="sxs-lookup"><span data-stu-id="2b32a-304">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="2b32a-305">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="2b32a-305">Start-AzureRmVM</span></span>
    - <span data-ttu-id="2b32a-306">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="2b32a-306">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="2b32a-307">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="2b32a-307">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="2b32a-308">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="2b32a-308">Set-AzureRmVM</span></span>
    - <span data-ttu-id="2b32a-309">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="2b32a-309">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="2b32a-310">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2b32a-310">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="2b32a-311">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="2b32a-311">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="2b32a-312">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="2b32a-312">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="2b32a-313">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2b32a-313">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="2b32a-314">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2b32a-314">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="2b32a-315">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2b32a-315">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="2b32a-316">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2b32a-316">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="2b32a-317">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="2b32a-317">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="2b32a-318">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="2b32a-318">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="2b32a-319">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="2b32a-319">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="2b32a-320">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="2b32a-320">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="2b32a-321">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="2b32a-321">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="2b32a-322">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="2b32a-322">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="2b32a-323">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="2b32a-323">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="2b32a-324">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="2b32a-324">AzureRM.EventGrid</span></span>
* <span data-ttu-id="2b32a-325">Gerekli olması halinde parametrelerin boş dizeyle değiştirilmesine izin vermek için Update-AzureRmEventGridSubscription cmdlet'i içindeki SubjectBeginsWith/SubjectEndsWith için ValidateNotNullOrEmpty doğrulama koşulları kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="2b32a-325">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="2b32a-326">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2b32a-326">AzureRM.KeyVault</span></span>
* <span data-ttu-id="2b32a-327">Get-AzureRmKeyVault -Tag çalıştırıldığında etiket döndürülmeme sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="2b32a-327">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="2b32a-328">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="2b32a-328">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="2b32a-329">Policy Insights cmdlet'leri genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="2b32a-329">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="2b32a-330">API 2018-04-04 sürümünü kullanın</span><span class="sxs-lookup"><span data-stu-id="2b32a-330">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="2b32a-331">PolicyDefinitionReferenceId, Get-AzureRmPolicyStateSummary sonuçlarına eklendi</span><span class="sxs-lookup"><span data-stu-id="2b32a-331">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="2b32a-332">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="2b32a-332">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="2b32a-333">RecoveryServices.Backup cmdlet'lerine -Vault parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="2b32a-333">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="2b32a-334">Bu parametre iletildiğinde Set-AzureRmRecoveryServicesContext cmdlet'ini geçersiz kılar.</span><span class="sxs-lookup"><span data-stu-id="2b32a-334">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="2b32a-335">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="2b32a-335">AzureRM.Sql</span></span>
* <span data-ttu-id="2b32a-336">Yardım dosyasındaki Get-AzureRmSqlDatabaseExpanded örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="2b32a-336">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="2b32a-337">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="2b32a-337">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="2b32a-338">Yardım dosyasındaki Add-AzureRmTrafficManagerEndpointConfig bölümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="2b32a-338">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="2b32a-339">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="2b32a-339">AzureRM.Websites</span></span>
* <span data-ttu-id="2b32a-340">'Set-AzureRmWebApp', -AssignIdentity kullanıldığında AppSettings verilerini geçersiz kılmayacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="2b32a-340">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="2b32a-341">'New-AzureRmWebAppSlot', isteğe bağlı parametre olarak AppServicePlan girişini kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="2b32a-341">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="2b32a-342">6.2.1 - Haziran 2018</span><span class="sxs-lookup"><span data-stu-id="2b32a-342">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="2b32a-343">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2b32a-343">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="2b32a-344">PSWorkspace modeli Network için tür parametresini kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="2b32a-344">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="2b32a-345">6.2.0 - Haziran 2018</span><span class="sxs-lookup"><span data-stu-id="2b32a-345">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="2b32a-346">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="2b32a-346">AzureRM.Profile</span></span>
* <span data-ttu-id="2b32a-347">Modülün içeri aktarılması sırasında Newtonsoft.Json 10.0.3 sürümünün yüklenmemesine ilişkin sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="2b32a-347">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="2b32a-348">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="2b32a-348">AzureRM.Compute</span></span>
* <span data-ttu-id="2b32a-349">VMSS VM Güncelleştirme özelliği</span><span class="sxs-lookup"><span data-stu-id="2b32a-349">VMSS VM Update feature</span></span>
    - <span data-ttu-id="2b32a-350">'Update-AzureRmVmssVM' ve 'New-AzureRmVMDataDisk' cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="2b32a-350">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="2b32a-351">VMSS VM’sine veri diski eklemeyi desteklemek için 'Add-AzureRmVMDataDisk' cmdlet’ine VirtualMachineScaleSetVM parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="2b32a-351">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="2b32a-352">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="2b32a-352">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="2b32a-353">ADF .Net SDK sürümü, aşağıdaki değişiklikleri içeren 0.8.0-preview sürümüne güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="2b32a-353">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="2b32a-354">Fabrika deposunu yapılandırma işlemi eklendi</span><span class="sxs-lookup"><span data-stu-id="2b32a-354">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="2b32a-355">QuickBooks LinkedService, consumerKey ve consumerSecret özelliklerini kullanıma sunmak üzere güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="2b32a-355">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="2b32a-356">SecretBase’ten Object’e birkaç model türü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="2b32a-356">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="2b32a-357">Blob Etkinliklerini tetikleme eklendi</span><span class="sxs-lookup"><span data-stu-id="2b32a-357">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="2b32a-358">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2b32a-358">AzureRM.KeyVault</span></span>
* <span data-ttu-id="2b32a-359">Belgeler örnek çıktı ile güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="2b32a-359">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="2b32a-360">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="2b32a-360">AzureRM.Network</span></span>
* <span data-ttu-id="2b32a-361">Ağ İzleyicisi cmdlet’leri üzerindeki Trafik Analizi parametreleri etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="2b32a-361">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="2b32a-362">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="2b32a-362">AzureRM.Resources</span></span>
* <span data-ttu-id="2b32a-363">'Get-AzureRmResource' cmdlet’inden döndürülen 'PSResource' nesnesinin 'Properties' özelliğiyle ilgili bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="2b32a-363">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="2b32a-364">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="2b32a-364">AzureRM.Scheduler</span></span>
* <span data-ttu-id="2b32a-365">Güncelleştirilen ServiceBusQueueJob’ın yeni Kimlik Doğrulaması değerlerini ayarlamamasıyla ilgili bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="2b32a-365">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="2b32a-366">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="2b32a-366">AzureRM.Sql</span></span>
* <span data-ttu-id="2b32a-367">Şu cmdlet’ler isteğe bağlı LicenseType parametresiyle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="2b32a-367">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="2b32a-368">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2b32a-368">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="2b32a-369">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="2b32a-369">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="2b32a-370">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="2b32a-370">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="2b32a-371">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="2b32a-371">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="2b32a-372">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2b32a-372">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="2b32a-373">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="2b32a-373">AzureRM.Websites</span></span>
* <span data-ttu-id="2b32a-374">'New-AzureRMWebApp' Strategy kütüphanesindeki ortak algoritmaları kullanmak üzere güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="2b32a-374">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="2b32a-375">6.1.0 - Mayıs 2018</span><span class="sxs-lookup"><span data-stu-id="2b32a-375">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="2b32a-376">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="2b32a-376">AzureRM.Profile</span></span>
* <span data-ttu-id="2b32a-377">'Clear-AzureRmContext' komutunun çalıştırılmasının boş bir bağlamı önceki varsayılan bağlamın adıyla tutmasına ve böylece kullanıcının eski ad ile yeni bir bağlam oluşturamadığı bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="2b32a-377">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="2b32a-378">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2b32a-378">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="2b32a-379">AS’de Ağ geçidi ilişkilendirme/ilişkilendirme kaldırma işlemlerini etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="2b32a-379">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="2b32a-380">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2b32a-380">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="2b32a-381">ApiVersions, ApiReleases ve ApiRevisions desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="2b32a-381">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="2b32a-382">ServiceFabric Arka Ucu desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="2b32a-382">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="2b32a-383">Application Insights Günlükçüsü desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="2b32a-383">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="2b32a-384">‘Temel’ sku’yu Api Yönetim hizmetinin geçerli sku’su olarak algılama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="2b32a-384">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="2b32a-385">Özel CA tarafından Kök veya CA olarak yayınlanan Sertifikaları yükleme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="2b32a-385">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="2b32a-386">Özel SSL sertifikalarını KeyVault ve Çoklu ara sunucu ana bilgisayar adlarıyla kabul etme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="2b32a-386">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="2b32a-387">MSI kimliği desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="2b32a-387">Added support for MSI identity</span></span>
* <span data-ttu-id="2b32a-388">İlkeleri Url ile kabul etme desteği eklendi NOT: Aşağıdaki cmdlet’ler gelecekteki sürümlerde kullanım dışı kalacaktır</span><span class="sxs-lookup"><span data-stu-id="2b32a-388">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="2b32a-389">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="2b32a-389">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="2b32a-390">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="2b32a-390">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="2b32a-391">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="2b32a-391">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="2b32a-392">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="2b32a-392">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="2b32a-393">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="2b32a-393">AzureRM.Batch</span></span>
* <span data-ttu-id="2b32a-394">Yeni Get-AzureBatchPoolNodeCounts cmdlet’ini yayınlama</span><span class="sxs-lookup"><span data-stu-id="2b32a-394">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="2b32a-395">Yeni AzureBatchComputeNodeServiceLogUpload cmdlet’ini yayınlama</span><span class="sxs-lookup"><span data-stu-id="2b32a-395">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="2b32a-396">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="2b32a-396">AzureRM.Consumption</span></span>
* <span data-ttu-id="2b32a-397">Get-AzureRmConsumptionUsageDetail cmdlet’inde yeni Expand, ResourceGroup, InstanceName, InstanceId, Tags ve Top parametrelerini ekleme</span><span class="sxs-lookup"><span data-stu-id="2b32a-397">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="2b32a-398">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2b32a-398">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="2b32a-399">Export-AzureRmDataLakeStoreChildItemProperties için düzeltme örneği</span><span class="sxs-lookup"><span data-stu-id="2b32a-399">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="2b32a-400">Set-AzureRmDataLakeStoreItemAclEntry komutunda Özyineleme durumu için null parametresi özel durumunu düzeltme</span><span class="sxs-lookup"><span data-stu-id="2b32a-400">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="2b32a-401">Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry’ye yönelik yardım dosyalarını düzeltme</span><span class="sxs-lookup"><span data-stu-id="2b32a-401">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="2b32a-402">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="2b32a-402">AzureRM.Network</span></span>
* <span data-ttu-id="2b32a-403">Ağ SDK sürümünü 18.0.0-önizleme’den 19.0.0-önizlemeye yükseltme</span><span class="sxs-lookup"><span data-stu-id="2b32a-403">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="2b32a-404">Protokol yapılandırması oluşturma cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="2b32a-404">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="2b32a-405">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="2b32a-405">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="2b32a-406">Varolan express route bağlantı hattına yeni bir bağlantı hattı ekleme cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="2b32a-406">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="2b32a-407">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="2b32a-407">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="2b32a-408">Varolan express route bağlantı hattındaki bir bağlantı hattı bağlantısını kaldırma cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="2b32a-408">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="2b32a-409">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="2b32a-409">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="2b32a-410">Bağlantı hattı bağlantısı alma cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="2b32a-410">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="2b32a-411">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="2b32a-411">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="2b32a-412">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2b32a-412">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="2b32a-413">Oluşturulan sertifikalarla sunucu kimlik doğrulaması kullanımı düzeltildi (Sorun No. 5998)</span><span class="sxs-lookup"><span data-stu-id="2b32a-413">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="2b32a-414">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="2b32a-414">AzureRM.Sql</span></span>
* <span data-ttu-id="2b32a-415">AuditActions veya AuditActionGroups’un kaldırılmasını sağlamak üzere Denetim cmdlet’leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="2b32a-415">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="2b32a-416">Yeni bir esnek saklama ilkesi ayarlarken komutun ‘Azure kurtarma hizmeti kasası ve ilkesiyle uzun süreli saklama ilkesini yapılandırma artık desteklenmiyor. Lütfen yeni esnek saklama ilkesi ile istek gönderin’ hatasını verdiği Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="2b32a-416">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="2b32a-417">komutuna ilişkin sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="2b32a-417">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="2b32a-418">Ölçek ve katman ilişkili özelliklere yönelik Sku özelliğini destekleyen yeni Veritabanı API’sini kullanmak için tüm Azure Sql Database/ElasticPool Creation/Update cmdlet’lerini güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="2b32a-418">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="2b32a-419">Güncelleştirilen cmlet’ler arasında şunlar yer almaktadır:</span><span class="sxs-lookup"><span data-stu-id="2b32a-419">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="2b32a-420">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2b32a-420">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="2b32a-421">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="2b32a-421">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="2b32a-422">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="2b32a-422">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="2b32a-423">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="2b32a-423">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="2b32a-424">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2b32a-424">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="2b32a-425">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="2b32a-425">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="2b32a-426">-Name parametresini kullanırken -ResourceGroupName parametresinin gerekli olması için 'Get-AzureRmTrafficManagerProfile'a yönelik parametreleri güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="2b32a-426">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
