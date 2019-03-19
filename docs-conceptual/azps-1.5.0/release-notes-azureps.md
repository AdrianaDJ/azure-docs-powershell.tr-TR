---
ms.openlocfilehash: 9915ff37e59a73c1d226a216213fd9016b55d3d4
ms.sourcegitcommit: 447276d46ffeeb37f0c07a570536665e36c5ddb8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/14/2019
ms.locfileid: "57882650"
---
## <a name="150---march-2019"></a><span data-ttu-id="4b090-101">1.5.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="4b090-101">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4b090-102">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4b090-102">Az.Accounts</span></span>
* <span data-ttu-id="4b090-103">AutoRest tarafından oluşturulan cmdlet’leri desteklemek için 'Register-AzModule' komutu eklendi</span><span class="sxs-lookup"><span data-stu-id="4b090-103">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="4b090-104">Connect-AzAccount örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="4b090-104">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4b090-105">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4b090-105">Az.Automation</span></span>
* <span data-ttu-id="4b090-106">Birden fazla Azure Otomasyonu cmdlet’inde belirli aylık zamanlamalar alınırken yaşanan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="4b090-106">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="4b090-107">Yalnızca ilk 20 düğümü döndüren Get-AzAutomationDscNode düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="4b090-107">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="4b090-108">Artık tüm düğümleri döndürür</span><span class="sxs-lookup"><span data-stu-id="4b090-108">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="4b090-109">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="4b090-109">Az.Cdn</span></span>
* <span data-ttu-id="4b090-110">Özel Etki Alanı Https Etkinleştirmesi/Devre Dışı Bırakması için yeni PowerShell cmdlet’leri eklendi ve eskiler kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="4b090-110">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4b090-111">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4b090-111">Az.Compute</span></span>
* <span data-ttu-id="4b090-112">Get cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="4b090-112">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4b090-113">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4b090-113">Az.DataFactory</span></span>
* <span data-ttu-id="4b090-114">ADF .Net SDK sürümü 3.0.1'e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="4b090-114">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="4b090-115">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="4b090-115">Az.LogicApp</span></span>
* <span data-ttu-id="4b090-116">Yalnızca ilk sonuç sayfasını getiren ListWorkflows için düzeltme</span><span class="sxs-lookup"><span data-stu-id="4b090-116">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4b090-117">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4b090-117">Az.Network</span></span>
* <span data-ttu-id="4b090-118">Network cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="4b090-118">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4b090-119">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4b090-119">Az.RecoveryServices</span></span>
* <span data-ttu-id="4b090-120">Azure VM desteğine SQL Server eklendi</span><span class="sxs-lookup"><span data-stu-id="4b090-120">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="4b090-121">SDK Güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="4b090-121">SDK Update</span></span>
* <span data-ttu-id="4b090-122">Get-ProtectableItem içindeki Removed VMappContainer denetimi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="4b090-122">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="4b090-123">Get-ProtectableItem için Name ve ServerName parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="4b090-123">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="4b090-124">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4b090-124">Az.Resources</span></span>
* <span data-ttu-id="4b090-125">Dağıtım cmdlet’lerine `-TemplateObject` parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="4b090-125">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="4b090-126">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="4b090-126">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="4b090-127">`Get-AzResource` sonucu `Set-AzResource` üzerine aktarılırken oluşan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="4b090-127">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="4b090-128">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="4b090-128">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="4b090-129">`Set-AzResource` çalıştırılırken JSON veri türü değişikliğine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="4b090-129">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="4b090-130">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="4b090-130">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="4b090-131">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4b090-131">Az.Sql</span></span>
* <span data-ttu-id="4b090-132">AuditingEndpointsCommunicator güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="4b090-132">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="4b090-133">Yeni tanılama ayarları oluşturulurken kenar durumunun davranışı düzeltiliyor.</span><span class="sxs-lookup"><span data-stu-id="4b090-133">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4b090-134">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4b090-134">Az.Storage</span></span>
* <span data-ttu-id="4b090-135">Depolama hesabı oluşturulurken Support Kind BlockBlobStorage desteği sağlandı      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4b090-135">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="4b090-136">1.4.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="4b090-136">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="4b090-137">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="4b090-137">Az.AnalysisServices</span></span>
* <span data-ttu-id="4b090-138">AddAzureASAccount cmdlet'i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="4b090-138">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4b090-139">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4b090-139">Az.Automation</span></span>
* <span data-ttu-id="4b090-140">Import-AzAutomationDscNodeConfiguration için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="4b090-140">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="4b090-141">Import-AzAutomationDscConfiguration cmdlet'ine yapılandırma adı doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="4b090-141">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="4b090-142">Import-AzAutomationDscConfiguration cmdlet'i için hata işleme iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="4b090-142">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="4b090-143">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4b090-143">Az.CognitiveServices</span></span>
* <span data-ttu-id="4b090-144">Kaynağın alt etki alanını belirtmek amacıyla kullanılan New-AzCognitiveServicesAccount için CustomSubdomainName adlı, isteğe bağlı, yeni bir parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="4b090-144">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4b090-145">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4b090-145">Az.Compute</span></span>
* <span data-ttu-id="4b090-146">Kimlik parametresi kümeleriyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="4b090-146">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="4b090-147">Get-AzVMExtension, Name parametresi sağlanmadığında yüklü tüm uzantıları listeleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="4b090-147">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="4b090-148">Update-AzImage cmdlet’ine Tag ve ResourceId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="4b090-148">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="4b090-149">Get-AzVmssVM, örnek kimliği olmadan ve InstanceView ile, örnek görünümüne sahip VMSS VM’lerini listeleyebilir.</span><span class="sxs-lookup"><span data-stu-id="4b090-149">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4b090-150">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4b090-150">Az.DataLakeStore</span></span>
* <span data-ttu-id="4b090-151">ADL silinmiş öğe listeleme ve geri yükleme cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="4b090-151">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="4b090-152">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="4b090-152">Az.EventHub</span></span>
* <span data-ttu-id="4b090-153">EventHub’ın CaptureDescription sınıfında Boş Arşivleri Atlamak için SkipEmptyArchives adlı yeni Boole özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="4b090-153">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="4b090-154">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4b090-154">Az.KeyVault</span></span>
* <span data-ttu-id="4b090-155">Set-AzKeyVaultSecret’daki etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="4b090-155">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="4b090-156">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="4b090-156">Az.LogicApp</span></span>
* <span data-ttu-id="4b090-157">Tümleştirme Hesapları için Temel SKU eklendi</span><span class="sxs-lookup"><span data-stu-id="4b090-157">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="4b090-158">XSLT 2.0, XSLT 3.0 ve Liquid Eşleşme Türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="4b090-158">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="4b090-159">Tümleştirme Hesabı Bütünleştirilmiş Kodları için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="4b090-159">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="4b090-160">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="4b090-160">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="4b090-161">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="4b090-161">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="4b090-162">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="4b090-162">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="4b090-163">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="4b090-163">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="4b090-164">Tümleştirme Hesabı Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="4b090-164">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="4b090-165">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="4b090-165">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="4b090-166">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="4b090-166">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="4b090-167">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="4b090-167">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="4b090-168">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="4b090-168">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="4b090-169">Logic Apps SDK sürüm 4.1.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="4b090-169">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4b090-170">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4b090-170">Az.Monitor</span></span>
* <span data-ttu-id="4b090-171">Get-AzMetric için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="4b090-171">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4b090-172">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4b090-172">Az.Network</span></span>
* <span data-ttu-id="4b090-173">Add-AzApplicationGatewayCustomError için yardım örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="4b090-173">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="4b090-174">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4b090-174">Az.OperationalInsights</span></span>
* <span data-ttu-id="4b090-175">New ve Get ApplicationInsights veri kaynağı için ek destek sunuldu.</span><span class="sxs-lookup"><span data-stu-id="4b090-175">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="4b090-176">Belirli bir çalışma alanı için belirli ve tüm Get ApplicationInsights veri kaynaklarını desteklemek için yeni ‘ApplicationInsights’ türü eklendi.</span><span class="sxs-lookup"><span data-stu-id="4b090-176">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="4b090-177">Belirli Application-Insights kaynak parametrelerine (abonelik kimliği, resourceGroupName ve ad) göre veri kaynağı oluşturmak için New-AzOperationalInsightsApplicationInsightsDataSource cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="4b090-177">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="4b090-178">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4b090-178">Az.Resources</span></span>
* <span data-ttu-id="4b090-179">https://github.com/Azure/azure-powershell/issues/8166 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="4b090-179">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="4b090-180">https://github.com/Azure/azure-powershell/issues/8235 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="4b090-180">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="4b090-181">https://github.com/Azure/azure-powershell/issues/6219 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="4b090-181">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="4b090-182">KeyCredentials’ın tekrar oluşturmasını engelleyen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="4b090-182">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="4b090-183">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4b090-183">Az.Sql</span></span>
* <span data-ttu-id="4b090-184">SQL DB Hiper Ölçeklendirme katmanı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="4b090-184">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="4b090-185">Geri yükleme isteğinde gereksiz özellikler ayarlandığı için geri yüklemenin başarısız olmasına yol açan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="4b090-185">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4b090-186">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4b090-186">Az.Websites</span></span>
* <span data-ttu-id="4b090-187">Get-AzWebAppSlotMetrics örneği düzeltildi</span><span class="sxs-lookup"><span data-stu-id="4b090-187">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="4b090-188">1.3.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="4b090-188">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4b090-189">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4b090-189">Az.Accounts</span></span>
* <span data-ttu-id="4b090-190">En son ClientRuntime sürümüne güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="4b090-190">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="4b090-191">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="4b090-191">Az.AnalysisServices</span></span>
<span data-ttu-id="4b090-192">Az.AnalysisServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="4b090-192">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4b090-193">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4b090-193">Az.Compute</span></span>
* <span data-ttu-id="4b090-194">AEM uzantısı: UltraSSD ile P60,P70 ve P80 diskleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="4b090-194">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="4b090-195">Set-AzVMBootDiagnostics yardım açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="4b090-195">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="4b090-196">Update-AzImage için yardım açıklaması ve örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="4b090-196">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4b090-197">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4b090-197">Az.RecoveryServices</span></span>
<span data-ttu-id="4b090-198">Az.RecoveryServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="4b090-198">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4b090-199">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4b090-199">Az.Resources</span></span>
* <span data-ttu-id="4b090-200">Kaynak grupları için etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="4b090-200">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="4b090-201">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="4b090-201">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="4b090-202">`Get-AzureRmRoleAssignment` komutunun -ErrorAction'a uymama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="4b090-202">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="4b090-203">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="4b090-203">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="4b090-204">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4b090-204">Az.Sql</span></span>
* <span data-ttu-id="4b090-205">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="4b090-205">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="4b090-206">Azure hesabında oturum açılmamasının SQL cmdlet'leri yürütülürken nullref özel durumuna yol açması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="4b090-206">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="4b090-207">Get-AzSqlCapability'de null başvuru özel durumu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="4b090-207">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="4b090-208">1.2.1 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="4b090-208">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4b090-209">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4b090-209">Az.Accounts</span></span>
* <span data-ttu-id="4b090-210">Kimlik Doğrulaması'nın doğru yayınını içeren sürümü</span><span class="sxs-lookup"><span data-stu-id="4b090-210">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="4b090-211">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="4b090-211">Az.AnalysisServices</span></span>
* <span data-ttu-id="4b090-212">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="4b090-212">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4b090-213">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4b090-213">Az.RecoveryServices</span></span>
* <span data-ttu-id="4b090-214">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="4b090-214">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="4b090-215">1.2.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="4b090-215">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4b090-216">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4b090-216">Az.Accounts</span></span>
* <span data-ttu-id="4b090-217">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="4b090-217">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="4b090-218">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="4b090-218">Update incorrect online help URLs</span></span>
* <span data-ttu-id="4b090-219">Uninstall-AzureRm için PC Çekirdeğine uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="4b090-219">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="4b090-220">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="4b090-220">Az.Aks</span></span>
* <span data-ttu-id="4b090-221">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="4b090-221">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4b090-222">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4b090-222">Az.Automation</span></span>
* <span data-ttu-id="4b090-223">Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="4b090-223">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="4b090-224">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="4b090-224">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="4b090-225">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="4b090-225">Az.Cdn</span></span>
* <span data-ttu-id="4b090-226">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="4b090-226">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4b090-227">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4b090-227">Az.Compute</span></span>
* <span data-ttu-id="4b090-228">Invoke-AzVMReimage cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="4b090-228">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="4b090-229">Set-AzVmss'ye TempDisk parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="4b090-229">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="4b090-230">New-AzVM'nin uyarı iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="4b090-230">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="4b090-231">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="4b090-231">Az.ContainerRegistry</span></span>
* <span data-ttu-id="4b090-232">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="4b090-232">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4b090-233">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4b090-233">Az.DataFactory</span></span>
* <span data-ttu-id="4b090-234">ADF .Net SDK sürümü 3.0.0'a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="4b090-234">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4b090-235">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4b090-235">Az.DataLakeStore</span></span>
* <span data-ttu-id="4b090-236">MSI kullanırken ADLS uç noktasındaki sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="4b090-236">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="4b090-237">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="4b090-237">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="4b090-238">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="4b090-238">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4b090-239">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4b090-239">Az.IotHub</span></span>
* <span data-ttu-id="4b090-240">Add-IotHubRoutingEndpoint cmdlet'ine Kodlama biçimi eklendi.</span><span class="sxs-lookup"><span data-stu-id="4b090-240">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4b090-241">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4b090-241">Az.KeyVault</span></span>
* <span data-ttu-id="4b090-242">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="4b090-242">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4b090-243">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4b090-243">Az.Network</span></span>
* <span data-ttu-id="4b090-244">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="4b090-244">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="4b090-245">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4b090-245">Az.Resources</span></span>
* <span data-ttu-id="4b090-246">'New-AzADAppCredential' ve 'New-AzADSpCredential' başvuru belgelerindeki hatalı örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="4b090-246">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="4b090-247">Kaynak grubu dağıtım cmdlet'lerini yürütmeden önce '-TemplateFile' parametresi yolunun çözülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="4b090-247">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="4b090-248">Az.Resources: Belgede New-AzureRmPolicyDefinition -Mode varsayılan değeri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="4b090-248">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="4b090-249">Az.Resources: https://github.com/Azure/azure-powershell/issues/7522 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="4b090-249">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="4b090-250">Az.Resources: https://github.com/Azure/azure-powershell/issues/5747 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="4b090-250">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="4b090-251">'PSResourceGroupDeployment' nesnesinin biçimlendirme sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="4b090-251">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="4b090-252">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="4b090-252">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="4b090-253">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4b090-253">Az.ServiceFabric</span></span>
* <span data-ttu-id="4b090-254">VMSS modeline sertifika eklendiğinde ama özel durum oluştuğunda geri alma için hata düzeltmesi: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="4b090-254">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="4b090-255">Bazı hata iletileri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="4b090-255">Fix some error messages.</span></span>
* <span data-ttu-id="4b090-256">Az geçişinde çalışmayan New-AzServiceFabriCluster için varsayılan ARM şablonuyla küme oluşturma sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="4b090-256">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="4b090-257">Uzantıda küme kimliği denetlenerek küme/uygulama sertifikasının yalnızca kümeye karşılık gelen VM Ölçek Kümelerine eklenmesi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="4b090-257">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="4b090-258">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="4b090-258">Az.SignalR</span></span>
* <span data-ttu-id="4b090-259">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="4b090-259">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="4b090-260">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4b090-260">Az.Sql</span></span>
* <span data-ttu-id="4b090-261">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="4b090-261">Update incorrect online help URLs</span></span>
* <span data-ttu-id="4b090-262">LicenseType parametresinin parametre açıklaması olası değerlerle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="4b090-262">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="4b090-263">Yönetilen örnek kimliği güncelleştirmesinin, güncelleştirilen tek özellik bu olduğunda çalışmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="4b090-263">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="4b090-264">Yönetilen örnekte özel harmanlama desteği</span><span class="sxs-lookup"><span data-stu-id="4b090-264">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4b090-265">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4b090-265">Az.Storage</span></span>
* <span data-ttu-id="4b090-266">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="4b090-266">Update incorrect online help URLs</span></span>
* <span data-ttu-id="4b090-267">Premium Depolama Hesabı klasik Günlük/Ölçüm desteği sağlamadığından, Premium Depolama Hesabında klasik Günlük/Ölçüm için get/set komutları kullanıldığında ayrıntılı hata iletisi veriliyor.</span><span class="sxs-lookup"><span data-stu-id="4b090-267">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="4b090-268">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="4b090-268">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="4b090-269">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="4b090-269">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="4b090-270">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="4b090-270">Az.TrafficManager</span></span>
* <span data-ttu-id="4b090-271">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="4b090-271">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4b090-272">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4b090-272">Az.Websites</span></span>
* <span data-ttu-id="4b090-273">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="4b090-273">Update incorrect online help URLs</span></span>
* <span data-ttu-id="4b090-274">Uygulama ASE'de barındırılıyorsa, sertifikayı doğru kaynak grubuna ve konuma yüklemek için 'New-AzWebAppSSLBinding' düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="4b090-274">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="4b090-275">SSL sertifikası bir uygulamaya bağlanırken etiketlerin üzerine yazılmaması için 'New-AzWebAppSSLBinding' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="4b090-275">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="4b090-276">1.1.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="4b090-276">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4b090-277">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4b090-277">Az.Accounts</span></span>
* <span data-ttu-id="4b090-278">Enable-AzureRmAlias cmdlet'ine 'Local' Kapsamı eklendi</span><span class="sxs-lookup"><span data-stu-id="4b090-278">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4b090-279">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4b090-279">Az.Compute</span></span>
* <span data-ttu-id="4b090-280">Restart/Start/Stop/Remove/Set-AzVM ve Save-AzVMImage için ayarlanan ID parametresinde ad artık isteğe bağlı</span><span class="sxs-lookup"><span data-stu-id="4b090-280">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="4b090-281">Yardım dosyalarında ID parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="4b090-281">Updated the description of ID in help files</span></span>
* <span data-ttu-id="4b090-282">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="4b090-282">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4b090-283">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4b090-283">Az.DataLakeStore</span></span>
* <span data-ttu-id="4b090-284">SDK düzeltmeleri için veri düzleminin SDK sürümü 1.1.14 olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="4b090-284">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="4b090-285">getfilestatus ve liststatus için negatif acesstime ve modificationtime değerlerini işleme yöntemi düzeltildi, async iptal belirteci düzeltildi</span><span class="sxs-lookup"><span data-stu-id="4b090-285">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="4b090-286">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="4b090-286">Az.EventGrid</span></span>
* <span data-ttu-id="4b090-287">2019-01-01 API sürümünü kullanmak için güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="4b090-287">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="4b090-288">Aşağıdaki cmdlet'ler 2019-01-01 API sürümünde yeni senaryoyu destekleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="4b090-288">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="4b090-289">New-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="4b090-289">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="4b090-290">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="4b090-290">Event Time-To-Live,</span></span>
        - <span data-ttu-id="4b090-291">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="4b090-291">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="4b090-292">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="4b090-292">Dead letter endpoint.</span></span>
    - <span data-ttu-id="4b090-293">Update-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="4b090-293">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="4b090-294">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="4b090-294">Event Time-To-Live,</span></span>
        - <span data-ttu-id="4b090-295">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="4b090-295">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="4b090-296">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="4b090-296">Dead letter endpoint.</span></span>
* <span data-ttu-id="4b090-297">New-AzureRmEventGridSubscription ve Update-AzureRmEventGridSubscription cmdlet'lerinde EndpointType seçeneği için yeni enum değerleri (storageQueue ve hybridConnection) eklendi.</span><span class="sxs-lookup"><span data-stu-id="4b090-297">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="4b090-298">Olay aboneliğini oluşturma veya güncelleştirme işleminde kullanıcının el ile bir eylem yapması beklendiğinde uyarı iletisi gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="4b090-298">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4b090-299">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4b090-299">Az.IotHub</span></span>
* <span data-ttu-id="4b090-300">IotHub SDK'sı en son sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="4b090-300">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="4b090-301">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="4b090-301">Az.LogicApp</span></span>
* <span data-ttu-id="4b090-302">Get-AzLogicApp, Name değeri belirtilmemiş olanların tümünü listeliyor</span><span class="sxs-lookup"><span data-stu-id="4b090-302">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="4b090-303">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4b090-303">Az.Resources</span></span>
* <span data-ttu-id="4b090-304">'Get-AzResource' için '-ODataQuery' ve '-ResourceId' parametreleri sağlanırken ortaya çıkan parametre ayarlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="4b090-304">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="4b090-305">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="4b090-305">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="4b090-306">New/Set-AzPolicyDefinition cmdlet'lerinde -Custom parametresinin işlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="4b090-306">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="4b090-307">New-AzDeployment belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="4b090-307">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="4b090-308">'New-AzADUser' için '-MailNickname' parametresi zorunlu hale getirildi</span><span class="sxs-lookup"><span data-stu-id="4b090-308">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="4b090-309">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="4b090-309">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="4b090-310">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="4b090-310">Az.SignalR</span></span>
* <span data-ttu-id="4b090-311">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="4b090-311">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="4b090-312">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4b090-312">Az.Sql</span></span>
* <span data-ttu-id="4b090-313">Depolama yönetimi istemci bağımlılığı ortak SDK uygulamasına dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="4b090-313">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4b090-314">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4b090-314">Az.Storage</span></span>
* <span data-ttu-id="4b090-315">Sas Token, OAuth veya Anonymous ile oluşturulduğunda Storage bağlamının StorageAccountName değeri gerçek Depolama Hesabı Adına ayarlanıyor</span><span class="sxs-lookup"><span data-stu-id="4b090-315">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="4b090-316">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="4b090-316">New-AzStorageContext</span></span>
* <span data-ttu-id="4b090-317">Blob Anlık Görüntü Nesnesinin Sas Belirteci '-FullUri' parametresiyle oluşturulduğunda, döndürülen Uri anlık görüntü Uri'si olacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="4b090-317">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="4b090-318">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="4b090-318">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4b090-319">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4b090-319">Az.Websites</span></span>
* <span data-ttu-id="4b090-320">'Get-AzDeletedWebApp' cmdlet'indeki tarih ayrıştırma hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="4b090-320">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="4b090-321">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="4b090-321">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="4b090-322">1.0.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="4b090-322">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="4b090-323">Genel</span><span class="sxs-lookup"><span data-stu-id="4b090-323">General</span></span>

- <span data-ttu-id="4b090-324">Az Modülü Genel Kullanıma Sunuldu</span><span class="sxs-lookup"><span data-stu-id="4b090-324">General Availability of Az Module</span></span>
- <span data-ttu-id="4b090-325">Her modül için çevrimiçi yardım</span><span class="sxs-lookup"><span data-stu-id="4b090-325">Online help for each module</span></span>
- <span data-ttu-id="4b090-326">Diğer ayrıntılar ve yol haritası için bkz. [Az Duyuru Sayfası](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="4b090-326">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="4b090-327">AzureRM’den geçiş hakkında bilgi edinmek için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="4b090-327">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="4b090-328">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4b090-328">Az.Accounts</span></span>
- <span data-ttu-id="4b090-329">Önceki adı: Az.Profile</span><span class="sxs-lookup"><span data-stu-id="4b090-329">Changed from Az.Profile</span></span>
- <span data-ttu-id="4b090-330">Profil ve bağlam türleri için tablo biçimleri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="4b090-330">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="4b090-331">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4b090-331">Az.ApiManagement</span></span>
- <span data-ttu-id="4b090-332">#7002 düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="4b090-332">Fixes for #7002</span></span>
- <span data-ttu-id="4b090-333">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="4b090-333">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="4b090-334">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="4b090-334">Az.Batch</span></span>
- <span data-ttu-id="4b090-335">`PSComputeNode` üzerinde yeni `NodeAgentInformation` aracılığıyla bir havuzdaki her bir VM’de Azure Batch Düğüm Aracısı’nın hangi sürümünün çalıştığını görme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="4b090-335">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="4b090-336">`PSDataDisk` için `Caching` varsayılan ayarı artık `None` yerine `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="4b090-336">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="4b090-337">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="4b090-337">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="4b090-338">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="4b090-338">Az.Billing</span></span>
- <span data-ttu-id="4b090-339">Billing, Consumption ve UsageAggregates cmdlet’lerini birleştirir, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="4b090-339">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="4b090-340">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="4b090-340">Az.CognitivServices</span></span>
- <span data-ttu-id="4b090-341">New-AzureRmCognitiveServicesAccount işleminde kullanılabilen SkuName ve Typem için tamamlayıcılar eklendi</span><span class="sxs-lookup"><span data-stu-id="4b090-341">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="4b090-342">Get-AzCognitiveServicesAccountSkus cmdlet’inden GetSkusWithAccountParamSetName parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="4b090-342">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="4b090-343">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="4b090-343">Az.ContainerInstance</span></span>
- <span data-ttu-id="4b090-344">ManagedIdentity desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="4b090-344">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="4b090-345">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="4b090-345">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="4b090-346">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="4b090-346">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="4b090-347">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4b090-347">Az.DataLakeStore</span></span>
- <span data-ttu-id="4b090-348">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="4b090-348">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="4b090-349">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4b090-349">Az.Monitor</span></span>
- <span data-ttu-id="4b090-350">Az.Insights cmdlet’inin adı Az.Monitor olarak değiştirildi ve başka yeni değişiklikler yapıldı, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="4b090-350">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="4b090-351">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4b090-351">Az.KeyVault</span></span>
- <span data-ttu-id="4b090-352">Çıkış türlerinden kullanım dışı 'PurgeDisabled' özelliği kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="4b090-352">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="4b090-353">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="4b090-353">Az.MachineLearning</span></span>
- <span data-ttu-id="4b090-354">Az.MachineLearningCompute modülünden cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="4b090-354">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="4b090-355">Az.Media</span><span class="sxs-lookup"><span data-stu-id="4b090-355">Az.Media</span></span>
- <span data-ttu-id="4b090-356">New-AzMediaService cmdlet’inden kullanım dışı -Tags diğer adı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="4b090-356">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="4b090-357">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4b090-357">Az.Network</span></span>
<span data-ttu-id="4b090-358">Application Gateway’de RewriteRuleSets parametresini yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="4b090-358">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="4b090-359">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="4b090-359">New cmdlets added:</span></span>
        - <span data-ttu-id="4b090-360">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4b090-360">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="4b090-361">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4b090-361">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="4b090-362">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4b090-362">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="4b090-363">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4b090-363">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="4b090-364">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4b090-364">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="4b090-365">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="4b090-365">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="4b090-366">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="4b090-366">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="4b090-367">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="4b090-367">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="4b090-368">Cmdlet’ler isteğe bağlı -RewriteRuleSet parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="4b090-368">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="4b090-369">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4b090-369">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="4b090-370">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="4b090-370">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="4b090-371">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="4b090-371">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="4b090-372">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4b090-372">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="4b090-373">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4b090-373">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="4b090-374">New-AzureRmApplicationGatewayUrlPathMapConfig, Kimlik kullanarak Application Gateway’e KeyVault Desteği ekledi.</span><span class="sxs-lookup"><span data-stu-id="4b090-374">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="4b090-375">Cmdlet’ler isteğe bağlı -KeyVaultSecretId, -KeyVaultSecret parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="4b090-375">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="4b090-376">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4b090-376">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="4b090-377">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4b090-377">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="4b090-378">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4b090-378">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="4b090-379">New-AzApplicationGateway cmdlet’i isteğe bağlı -UserAssignedIdentity parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="4b090-379">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="4b090-380">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="4b090-380">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="4b090-381">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4b090-381">Az.OperationalInsights</span></span>
- <span data-ttu-id="4b090-382">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="4b090-382">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="4b090-383">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="4b090-383">Az.Profile</span></span>
- <span data-ttu-id="4b090-384">Modül adı Az.Accounts olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="4b090-384">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="4b090-385">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4b090-385">Az.RecoveryServices</span></span>
- <span data-ttu-id="4b090-386">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="4b090-386">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="4b090-387">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4b090-387">Az.Resources</span></span>
- <span data-ttu-id="4b090-388">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="4b090-388">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="4b090-389">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4b090-389">Az.ServiceFabric</span></span>
- <span data-ttu-id="4b090-390">Sertifikayı ortak ad ve parmak iziyle belirtme desteği</span><span class="sxs-lookup"><span data-stu-id="4b090-390">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="4b090-391">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="4b090-391">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="4b090-392">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="4b090-392">Az.SIgnalR</span></span>
- <span data-ttu-id="4b090-393">SIgnalR için PowerShell cmdlet'leri Genel Kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="4b090-393">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="4b090-394">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4b090-394">Az.Sql</span></span>
- <span data-ttu-id="4b090-395">Tehdit Algılama cmdlet’lerine yeni Data_Exfiltration ve Unsafe_Action algılama türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="4b090-395">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="4b090-396">Sql Denetimi cmdlet'leri için belge örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="4b090-396">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="4b090-397">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="4b090-397">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="4b090-398">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4b090-398">Az.Storage</span></span>
- <span data-ttu-id="4b090-399">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="4b090-399">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="4b090-400">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4b090-400">Az.Websites</span></span>
- <span data-ttu-id="4b090-401">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="4b090-401">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="4b090-402">0.7.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="4b090-402">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="4b090-403">Genel</span><span class="sxs-lookup"><span data-stu-id="4b090-403">General</span></span>

* <span data-ttu-id="4b090-404">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="4b090-404">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="4b090-405">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4b090-405">Az.Compute</span></span>

* <span data-ttu-id="4b090-406">`New-AzVm(ss)` cmdlet’leri için basit parametre kümelerinde UltraSSD ve Galeri Görüntüleri desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="4b090-406">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="4b090-407">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4b090-407">Az.DataLakeStore</span></span>

* <span data-ttu-id="4b090-408">Adls hesabı etki alanının sonundaki eğik çizgi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="4b090-408">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="4b090-409">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="4b090-409">Az.FrontDoor</span></span>

* <span data-ttu-id="4b090-410">Bazı bozuk bağlantılar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="4b090-410">Fixed some broken links</span></span>
    - <span data-ttu-id="4b090-411">New-AzureRmFrontDoor ve Set-AzureRmFrontDoor makalelerinde, New-AzureRmFrontDoorHealthProbeSettingObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="4b090-411">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="4b090-412">New-AzureRmFrontDoorManagedRuleObject makalesinde, New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="4b090-412">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="4b090-413">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4b090-413">Az.RecoveryServices</span></span>

* <span data-ttu-id="4b090-414">Azure Dosya Paylaşımı geri yükleme işlemleri için istemci tarafı doğrulamalar eklendi.</span><span class="sxs-lookup"><span data-stu-id="4b090-414">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="4b090-415">Afs geri yükleme işlemi için storageAccountName ve storageAccountResourceGroupName isteğe bağlı hale getirildi.</span><span class="sxs-lookup"><span data-stu-id="4b090-415">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="4b090-416">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4b090-416">Az.Resources</span></span>

* <span data-ttu-id="4b090-417">[https://github.com/Azure/azure-powershell/issues/7402](https://github.com/Azure/azure-powershell/issues/7679) düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="4b090-417">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="4b090-418">Get-AzureRmRoleAssignment, klasik yöneticiler istenirken sağlanmışsa abonelik kapsamını kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="4b090-418">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="4b090-419">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4b090-419">Az.Sql</span></span>

* <span data-ttu-id="4b090-420">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="4b090-420">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="4b090-421">Get-AzureRmSqlDatabaseVulnerabilityAssessment cmdlet’inin DotNet core ile kullanılması konusundaki bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="4b090-421">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="4b090-422">SQL Denetimi cmdlet’leriyle ilgili yardım iletilerinin belgeleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="4b090-422">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="4b090-423">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4b090-423">Az.Storage</span></span>

* <span data-ttu-id="4b090-424">New-AzureRmStorageAccount cmdlet’ine -EnableHierarchicalNamespace eklendi</span><span class="sxs-lookup"><span data-stu-id="4b090-424">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="4b090-425">-DestContext girilmediğinde Dosya Kopyalama cmdlet’inin hedefte kaynak bağlamını yeniden kullanamamasına yol açan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="4b090-425">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="4b090-426">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="4b090-426">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="4b090-427">Statik Web Sitesi yapılandırması için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="4b090-427">Support Static Website configuration</span></span>
    - <span data-ttu-id="4b090-428">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="4b090-428">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="4b090-429">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="4b090-429">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="4b090-430">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4b090-430">Az.Websites</span></span>

* <span data-ttu-id="4b090-431">Set-AzureRmWebApp ve Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4b090-431">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="4b090-432">Windows ve Linux kapsayıcı uygulamalarında bağlanacak Azure Depolama yollarının belirtilmesi için yeni parametre (-AzureStoragePath) eklendi.</span><span class="sxs-lookup"><span data-stu-id="4b090-432">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="4b090-433">Azure Depolama yollarını ayarlamak için yeni New-AzureRmWebAppAzureStoragePath cmdlet’inin çıktısını bir parametre olarak kullanın.</span><span class="sxs-lookup"><span data-stu-id="4b090-433">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="4b090-434">0.6.1 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="4b090-434">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="4b090-435">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4b090-435">Az.ApiManagement</span></span>
* <span data-ttu-id="4b090-436">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="4b090-436">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="4b090-437">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4b090-437">Az.Automation</span></span>
* <span data-ttu-id="4b090-438">Swagger tabanlı Azure Otomasyon cmdlet'leri</span><span class="sxs-lookup"><span data-stu-id="4b090-438">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="4b090-439">Güncelleştirme Yönetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="4b090-439">Added Update Management cmdlets</span></span>
* <span data-ttu-id="4b090-440">Kaynak Denetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="4b090-440">Added Source Control cmdlets</span></span>
* <span data-ttu-id="4b090-441">Remove-AzureRmAutomationHybridWorkerGroup cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="4b090-441">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="4b090-442">DSC Kayıt Düğümü komutu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="4b090-442">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="4b090-443">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4b090-443">Az.Compute</span></span>
* <span data-ttu-id="4b090-444">SystemAssigned kimliği için kimlik sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="4b090-444">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="4b090-445">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="4b090-445">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="4b090-446">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="4b090-446">Az.ContainerInstance</span></span>
* <span data-ttu-id="4b090-447">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="4b090-447">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="4b090-448">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="4b090-448">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="4b090-449">Market cmdlet'leri için örnekler açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="4b090-449">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="4b090-450">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4b090-450">Az.Network</span></span>
* <span data-ttu-id="4b090-451">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="4b090-451">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="4b090-452">Desteklenen AzureFirewall Ağ Protokollerine yeniden ICMP eklendi</span><span class="sxs-lookup"><span data-stu-id="4b090-452">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="4b090-453">Test-AzureRmNetworkWatcherConnectivity cmdlet'i güncelleştirildi; hedef kimlik, adres ve bağlantı noktasında doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="4b090-453">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="4b090-454">VirtualNetwork eşlemesinde bellek kullanımıyla ilgili sorunlar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="4b090-454">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="4b090-455">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="4b090-455">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="4b090-456">Korumalı dosya paylaşımı için ilke değiştirme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="4b090-456">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="4b090-457">İlke saat dilimi büyük harfe dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="4b090-457">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="4b090-458">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="4b090-458">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="4b090-459">New-AzureRmRecoveryServicesAsrProtectableItem cmdlet'indeki örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="4b090-459">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="4b090-460">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="4b090-460">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="4b090-461">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="4b090-461">Az.Relay</span></span>
* <span data-ttu-id="4b090-462">Kullanıcının New-AzureRmRelayKey cmdlet'ine KeyValue sağlamasına olanak tanıyan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="4b090-462">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="4b090-463">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4b090-463">Az.Resources</span></span>
* <span data-ttu-id="4b090-464">`New-AzureRmPolicyAssignment` ve `Set-AzureRmPolicyAssignment` cmdlet'lerindeki kaynak kimliğiyle ilgili parametrelerin yardım belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="4b090-464">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="4b090-465">New-AzureRmPolicyDefinition cmdlet'ine -Metadata kullanan bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="4b090-465">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="4b090-466">NetStandard'da Tag anahtarında büyük/küçük harf kullanımının korunmasına yönelik düzeltme yapıldı: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="4b090-466">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="4b090-467">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4b090-467">Az.ServiceFabric</span></span>
* <span data-ttu-id="4b090-468">Hataya neden olan değişiklikler yayınlanacağından kullanımdan kaldırılacak özellikleri belirten iletiler eklendi</span><span class="sxs-lookup"><span data-stu-id="4b090-468">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="4b090-469">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4b090-469">Az.Sql</span></span>
* <span data-ttu-id="4b090-470">Azure Sql Veritabanı Yönetilen Örneği ve Azure Sql Yönetilen Veritabanı'nındaki CRUD işlemleri için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="4b090-470">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="4b090-471">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="4b090-471">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="4b090-472">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="4b090-472">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="4b090-473">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="4b090-473">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="4b090-474">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="4b090-474">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="4b090-475">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="4b090-475">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="4b090-476">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="4b090-476">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="4b090-477">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="4b090-477">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="4b090-478">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="4b090-478">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="4b090-479">Sunucuda veya veritabanında Genişletilmiş Denetim İlkesi yönetimi etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="4b090-479">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="4b090-480">Denetim günlüklerinde filtrelemeyi etkinleştirmek için yeni parametre (PredicateExpression) eklendi.</span><span class="sxs-lookup"><span data-stu-id="4b090-480">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="4b090-481">Cmdlet'ler, SQL istemcileri yerine Eski istemcileri kullanacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="4b090-481">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="4b090-482">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="4b090-482">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="4b090-483">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="4b090-483">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="4b090-484">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="4b090-484">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="4b090-485">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="4b090-485">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="4b090-486">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings cmdlet'inin depolama hesabı ad parametre kümesiyle kullanılmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="4b090-486">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="4b090-487">0.5.0 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="4b090-487">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="4b090-488">Genel</span><span class="sxs-lookup"><span data-stu-id="4b090-488">General</span></span>
* <span data-ttu-id="4b090-489">Birçok temel cmdlet’e Kaynak Tamamlayıcıları eklendi - bunlar cmdlet’leri etkileşimli olarak çağırırken mevcut kaynak adları arasında gezinmenize olanak tanır</span><span class="sxs-lookup"><span data-stu-id="4b090-489">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="4b090-490">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="4b090-490">Az.Profile</span></span>
* <span data-ttu-id="4b090-491">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="4b090-491">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="4b090-492">Connect-AzAccount cmdlet'indeki TenantId parametresi Tenant olarak yeniden adlandırıldı ve TenantId için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="4b090-492">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="4b090-493">Connect-AzAccount için TenantId açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="4b090-493">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="4b090-494">Kiracı etki alanı sağlanırken başarısız oturum açma durumunda gösterilen hata iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="4b090-494">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="4b090-495">Kiracıda abonelikleri olmayan hesaplar için bağlam adı çakışmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="4b090-495">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="4b090-496">MSI kullanırken DataLake uç noktalarıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="4b090-496">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="4b090-497">Bağlantı olmadığında 'Disconnect-AzAccount' oluşturulmasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="4b090-497">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="4b090-498">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4b090-498">Az.CognitiveServices</span></span>
* <span data-ttu-id="4b090-499">Get-AzCognitiveServicesAccountSkus işlemi eklendi.</span><span class="sxs-lookup"><span data-stu-id="4b090-499">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4b090-500">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4b090-500">Az.Compute</span></span>
* <span data-ttu-id="4b090-501">Add-AzVmssVMDataDisk ve Remove-AzVmssVMDataDisk cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="4b090-501">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="4b090-502">Get-AzVMImage, AutomaticOSUpgradeProperties gösteriyor</span><span class="sxs-lookup"><span data-stu-id="4b090-502">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="4b090-503">SetAzVMChefExtension -BootstrapOptions ve -JsonAttribute seçeneği değerlerinin Json biçiminde ayarlanmamasıyla ilgili hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="4b090-503">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4b090-504">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4b090-504">Az.DataLakeStore</span></span>
* <span data-ttu-id="4b090-505">DataLake paketi 1.1.10'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="4b090-505">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="4b090-506">Çok iş parçacıklı işlemlere varsayılan Concurrency değeri eklendi.</span><span class="sxs-lookup"><span data-stu-id="4b090-506">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="4b090-507">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="4b090-507">Az.Insights</span></span>
* <span data-ttu-id="4b090-508">7267 numaralı (Otomatik ölçeklendirme alanı) sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="4b090-508">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="4b090-509">Yeni otomatik ölçeklendirme kuralı oluşturma sırasında numaralandırılmış parametrelerin düzgün ayarlanmamasıyla ilgili sorunlar (bunlar her zaman varsayılan değere ayarlanıyordu).</span><span class="sxs-lookup"><span data-stu-id="4b090-509">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="4b090-510">Set-AzDiagnosticSetting'in ayar oluşturma sırasında kategorilerin açıkça belirtilmesini gerektirmesiyle ilgili 7513 numaralı [Insights] sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="4b090-510">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="4b090-511">Artık cmdlet oluşturma sırasında açık kategori gösteriminin etkinleştirilmesini gerektirmiyor; başka bir deyişle belgelerinde belirtildiği gibi çalışıyor</span><span class="sxs-lookup"><span data-stu-id="4b090-511">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4b090-512">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4b090-512">Az.Network</span></span>
* <span data-ttu-id="4b090-513">Aşağıdaki parametrelerde PeeringType parametresi zorunlu parametre olarak değiştirildi:-</span><span class="sxs-lookup"><span data-stu-id="4b090-513">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="4b090-514">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="4b090-514">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="4b090-515">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="4b090-515">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="4b090-516">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="4b090-516">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="4b090-517">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="4b090-517">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="4b090-518">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="4b090-518">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="4b090-519">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="4b090-519">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="4b090-520">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="4b090-520">Az.PolicyInsights</span></span>
* <span data-ttu-id="4b090-521">İlke düzeltme cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="4b090-521">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="4b090-522">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4b090-522">Az.Resources</span></span>
* <span data-ttu-id="4b090-523">[https://github.com/Azure/azure-powershell/issues/7402](https://github.com/Azure/azure-powershell/issues/7402) düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="4b090-523">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="4b090-524">'Get-AzResource' için '-ResourceId' parametresi kullanılarak kaynakların listelenmesine olanak tanındı</span><span class="sxs-lookup"><span data-stu-id="4b090-524">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="4b090-525">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="4b090-525">Az.ServiceBus</span></span>
* <span data-ttu-id="4b090-526">PSServiceBusMigrationConfigurationAttributes'e Geçiş durumunun bilinmesine yardımcı olacak salt okunur MigrationState özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="4b090-526">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="4b090-527">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4b090-527">Az.ServiceFabric</span></span>
* <span data-ttu-id="4b090-528">Linux Vmss'ye sertifika ekleme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="4b090-528">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="4b090-529">'Add-AzServiceFabricClusterCertificate' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="4b090-529">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="4b090-530">Yeni sertifikadan doğru parmak izi kullanıyor (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="4b090-530">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="4b090-531">Özel durum doğru görüntüleniyor (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="4b090-531">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="4b090-532">'Update-AzServiceFabricDurability', Vmss CreateOrUpdate işlemini başlatmadan önce küme yapılandırmasını güncelleştirecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="4b090-532">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="4b090-533">0.4.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="4b090-533">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="4b090-534">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="4b090-534">Az.Profile</span></span>
* <span data-ttu-id="4b090-535">CloudShell’de Get-AzSubscription sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="4b090-535">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="4b090-536">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="4b090-536">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4b090-537">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4b090-537">Az.Compute</span></span>
* <span data-ttu-id="4b090-538">'New-AzVm' için basit parametre kümesi kullanıldığında hızlandırılmış ağların açılacağı VM boyutları beyaz listesine yeni boyutlar eklendi</span><span class="sxs-lookup"><span data-stu-id="4b090-538">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="4b090-539">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="4b090-539">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4b090-540">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4b090-540">Az.DataLakeStore</span></span>
* <span data-ttu-id="4b090-541">Sanal Ağ Kuralları desteği ekleme</span><span class="sxs-lookup"><span data-stu-id="4b090-541">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="4b090-542">Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store sanal ağ kuralını alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="4b090-542">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="4b090-543">Add-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabına sanal ağ kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="4b090-543">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="4b090-544">Set-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabındaki belirtilen sanal ağ kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="4b090-544">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="4b090-545">Remove-AzDataLakeStoreVirtualNetworkRule: Bir Azure Data Lake Store sanal ağ kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="4b090-545">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4b090-546">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4b090-546">Az.Network</span></span>
* <span data-ttu-id="4b090-547">Test-AzNetworkWatcherConnectivity cmdlet'i güncelleştirildi, arka uca protokol değerini geçiriyor.</span><span class="sxs-lookup"><span data-stu-id="4b090-547">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="4b090-548">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="4b090-548">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4b090-549">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4b090-549">Az.Resources</span></span>
* <span data-ttu-id="4b090-550">Get-AzRoleDefinition cmdlet'inin anlaşılmaz bir özel durum oluşturmasına neden olan hata (varsayılan profilin içinde abonelik olmadığında ve hiçbir kapsam belirtilmediğinde), senaryoya anlamlı bir özel durum eklenerek düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="4b090-550">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="4b090-551">Ayrıca varsayılan parametre kümesi 'RoleDefinitionNameParameterSet' olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="4b090-551">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="4b090-552">0.3.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="4b090-552">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="4b090-553">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="4b090-553">Azure.Storage</span></span>
* <span data-ttu-id="4b090-554">Hedefte meta veri sorunu olduğunda Fix Copy Blob/File meta verileri kopyalamayacak</span><span class="sxs-lookup"><span data-stu-id="4b090-554">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="4b090-555">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="4b090-555">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="4b090-556">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="4b090-556">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="4b090-557">Belirli bir konumunun Depolama kaynağı kullanımını alma desteği ve genel Depolama kayrağı kullanımını almak için uyarı iletisi ekleme kullanımdan kalktı.</span><span class="sxs-lookup"><span data-stu-id="4b090-557">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="4b090-558">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="4b090-558">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="4b090-559">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4b090-559">Az.CognitiveServices</span></span>
* <span data-ttu-id="4b090-560">Mevcut hesap olmadan Get-AzCognitiveServicesAccountSkus desteği.</span><span class="sxs-lookup"><span data-stu-id="4b090-560">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4b090-561">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4b090-561">Az.Compute</span></span>
* <span data-ttu-id="4b090-562">Get-AzVM -ResourceGroupName <rg> gerektiğinde 50'den fazla sonuç döndürecek şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="4b090-562">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="4b090-563">New-AzVmss cmdlet'inin yardımına 'SimpleParameterSet' örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="4b090-563">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="4b090-564">Azure Disk Şifrelemesi ilerleme durumu iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="4b090-564">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="4b090-565">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="4b090-565">Az.DataFactoryV2</span></span>
* <span data-ttu-id="4b090-566">ADF .Net SDK sürümü 2.3.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="4b090-566">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4b090-567">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4b090-567">Az.Network</span></span>
* <span data-ttu-id="4b090-568">NetworkProfile işlevselliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="4b090-568">Added NetworkProfile functionality.</span></span> <span data-ttu-id="4b090-569">yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="4b090-569">new cmdlets added</span></span>
    - <span data-ttu-id="4b090-570">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4b090-570">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="4b090-571">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4b090-571">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="4b090-572">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4b090-572">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="4b090-573">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4b090-573">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="4b090-574">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="4b090-574">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="4b090-575">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="4b090-575">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="4b090-576">Alt Ağ Modeline hizmet ilişki bağlantısı eklendi</span><span class="sxs-lookup"><span data-stu-id="4b090-576">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="4b090-577">New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="4b090-577">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="4b090-578">Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="4b090-578">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="4b090-579">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="4b090-579">Az.RedisCache</span></span>
* <span data-ttu-id="4b090-580">Bundan sonra Size parametresi olarak her dizeye izin veriliyor.</span><span class="sxs-lookup"><span data-stu-id="4b090-580">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="4b090-581">PSArgumentCompleter açılan listesine P5 eklendi</span><span class="sxs-lookup"><span data-stu-id="4b090-581">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="4b090-582">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4b090-582">Az.Resources</span></span>
* <span data-ttu-id="4b090-583">Set-AzPolicyDefinition'a eksik -Mode parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="4b090-583">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="4b090-584">Origin öğesi User içeren işlemler için Get-AzProviderOperation commandlet hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="4b090-584">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="4b090-585">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4b090-585">Az.Sql</span></span>
* <span data-ttu-id="4b090-586">Bazı yedekleme cmdlet'lerinin geçerli Azure aboneliğini tanıyamamasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="4b090-586">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4b090-587">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4b090-587">Az.Websites</span></span>
* <span data-ttu-id="4b090-588">Yeni Get-AzWebAppContainerContinuousDeploymentUrl Cmdlet'i - Kapsayıcı Sürekli Dağıtım Web Kancası URL'sini alıyor</span><span class="sxs-lookup"><span data-stu-id="4b090-588">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="4b090-589">Yeni New-AzWebAppContainerPSSession ve Enter-WebAppContainerPSSession Cmdlet'leri - Windows kapsayıcı uygulamasında PowerShell uzak oturumunu başlatıyor</span><span class="sxs-lookup"><span data-stu-id="4b090-589">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="4b090-590">0.2.0 - Eylül 2018</span><span class="sxs-lookup"><span data-stu-id="4b090-590">0.2.0 - September 2018</span></span>
 <span data-ttu-id="4b090-591">İlk Yayın</span><span class="sxs-lookup"><span data-stu-id="4b090-591">Initial Release</span></span>