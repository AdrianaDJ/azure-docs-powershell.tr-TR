## <a name="140---february-2019"></a><span data-ttu-id="8c612-101">1.4.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="8c612-101">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="8c612-102">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8c612-102">Az.AnalysisServices</span></span>
* <span data-ttu-id="8c612-103">AddAzureASAccount cmdlet'i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="8c612-103">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8c612-104">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8c612-104">Az.Automation</span></span>
* <span data-ttu-id="8c612-105">Import-AzAutomationDscNodeConfiguration için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8c612-105">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="8c612-106">Import-AzAutomationDscConfiguration cmdlet'ine yapılandırma adı doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="8c612-106">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="8c612-107">Import-AzAutomationDscConfiguration cmdlet'i için hata işleme iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="8c612-107">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="8c612-108">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8c612-108">Az.CognitiveServices</span></span>
* <span data-ttu-id="8c612-109">Kaynağın alt etki alanını belirtmek amacıyla kullanılan New-AzCognitiveServicesAccount için CustomSubdomainName adlı, isteğe bağlı, yeni bir parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="8c612-109">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8c612-110">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8c612-110">Az.Compute</span></span>
* <span data-ttu-id="8c612-111">Kimlik parametresi kümeleriyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8c612-111">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="8c612-112">Get-AzVMExtension, Name parametresi sağlanmadığında yüklü tüm uzantıları listeleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8c612-112">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="8c612-113">Update-AzImage cmdlet’ine Tag ve ResourceId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="8c612-113">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="8c612-114">Get-AzVmssVM, örnek kimliği olmadan ve InstanceView ile, örnek görünümüne sahip VMSS VM’lerini listeleyebilir.</span><span class="sxs-lookup"><span data-stu-id="8c612-114">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8c612-115">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8c612-115">Az.DataLakeStore</span></span>
* <span data-ttu-id="8c612-116">ADL silinmiş öğe listeleme ve geri yükleme cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="8c612-116">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8c612-117">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8c612-117">Az.EventHub</span></span>
* <span data-ttu-id="8c612-118">EventHub’ın CaptureDescription sınıfında Boş Arşivleri Atlamak için SkipEmptyArchives adlı yeni Boole özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="8c612-118">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="8c612-119">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8c612-119">Az.KeyVault</span></span>
* <span data-ttu-id="8c612-120">Set-AzKeyVaultSecret’daki etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8c612-120">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="8c612-121">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="8c612-121">Az.LogicApp</span></span>
* <span data-ttu-id="8c612-122">Tümleştirme Hesapları için Temel SKU eklendi</span><span class="sxs-lookup"><span data-stu-id="8c612-122">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="8c612-123">XSLT 2.0, XSLT 3.0 ve Liquid Eşleşme Türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="8c612-123">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="8c612-124">Tümleştirme Hesabı Bütünleştirilmiş Kodları için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="8c612-124">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="8c612-125">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="8c612-125">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="8c612-126">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="8c612-126">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="8c612-127">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="8c612-127">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="8c612-128">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="8c612-128">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="8c612-129">Tümleştirme Hesabı Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="8c612-129">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="8c612-130">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="8c612-130">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="8c612-131">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="8c612-131">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="8c612-132">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="8c612-132">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="8c612-133">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="8c612-133">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="8c612-134">Logic Apps SDK sürüm 4.1.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8c612-134">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8c612-135">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8c612-135">Az.Monitor</span></span>
* <span data-ttu-id="8c612-136">Get-AzMetric için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8c612-136">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8c612-137">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8c612-137">Az.Network</span></span>
* <span data-ttu-id="8c612-138">Add-AzApplicationGatewayCustomError için yardım örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8c612-138">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8c612-139">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8c612-139">Az.OperationalInsights</span></span>
* <span data-ttu-id="8c612-140">New ve Get ApplicationInsights veri kaynağı için ek destek sunuldu.</span><span class="sxs-lookup"><span data-stu-id="8c612-140">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="8c612-141">Belirli bir çalışma alanı için belirli ve tüm Get ApplicationInsights veri kaynaklarını desteklemek için yeni ‘ApplicationInsights’ türü eklendi.</span><span class="sxs-lookup"><span data-stu-id="8c612-141">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="8c612-142">Belirli Application-Insights kaynak parametrelerine (abonelik kimliği, resourceGroupName ve ad) göre veri kaynağı oluşturmak için New-AzOperationalInsightsApplicationInsightsDataSource cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="8c612-142">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="8c612-143">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8c612-143">Az.Resources</span></span>
* <span data-ttu-id="8c612-144">https://github.com/Azure/azure-powershell/issues/8166 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8c612-144">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="8c612-145">https://github.com/Azure/azure-powershell/issues/8235 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8c612-145">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="8c612-146">https://github.com/Azure/azure-powershell/issues/6219 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8c612-146">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="8c612-147">KeyCredentials’ın tekrar oluşturmasını engelleyen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8c612-147">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="8c612-148">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8c612-148">Az.Sql</span></span>
* <span data-ttu-id="8c612-149">SQL DB Hiper Ölçeklendirme katmanı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="8c612-149">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="8c612-150">Geri yükleme isteğinde gereksiz özellikler ayarlandığı için geri yüklemenin başarısız olmasına yol açan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8c612-150">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8c612-151">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8c612-151">Az.Websites</span></span>
* <span data-ttu-id="8c612-152">Get-AzWebAppSlotMetrics örneği düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8c612-152">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="8c612-153">1.3.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="8c612-153">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8c612-154">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8c612-154">Az.Accounts</span></span>
* <span data-ttu-id="8c612-155">En son ClientRuntime sürümüne güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="8c612-155">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="8c612-156">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8c612-156">Az.AnalysisServices</span></span>
<span data-ttu-id="8c612-157">Az.AnalysisServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="8c612-157">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8c612-158">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8c612-158">Az.Compute</span></span>
* <span data-ttu-id="8c612-159">AEM uzantısı: UltraSSD ile P60,P70 ve P80 diskleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="8c612-159">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="8c612-160">Set-AzVMBootDiagnostics yardım açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8c612-160">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="8c612-161">Update-AzImage için yardım açıklaması ve örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8c612-161">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8c612-162">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8c612-162">Az.RecoveryServices</span></span>
<span data-ttu-id="8c612-163">Az.RecoveryServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="8c612-163">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8c612-164">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8c612-164">Az.Resources</span></span>
* <span data-ttu-id="8c612-165">Kaynak grupları için etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8c612-165">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="8c612-166">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="8c612-166">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="8c612-167">`Get-AzureRmRoleAssignment` komutunun -ErrorAction'a uymama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8c612-167">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="8c612-168">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="8c612-168">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="8c612-169">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8c612-169">Az.Sql</span></span>
* <span data-ttu-id="8c612-170">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8c612-170">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="8c612-171">Azure hesabında oturum açılmamasının SQL cmdlet'leri yürütülürken nullref özel durumuna yol açması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8c612-171">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="8c612-172">Get-AzSqlCapability'de null başvuru özel durumu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8c612-172">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="8c612-173">1.2.1 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="8c612-173">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8c612-174">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8c612-174">Az.Accounts</span></span>
* <span data-ttu-id="8c612-175">Kimlik Doğrulaması'nın doğru yayınını içeren sürümü</span><span class="sxs-lookup"><span data-stu-id="8c612-175">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="8c612-176">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8c612-176">Az.AnalysisServices</span></span>
* <span data-ttu-id="8c612-177">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="8c612-177">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8c612-178">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8c612-178">Az.RecoveryServices</span></span>
* <span data-ttu-id="8c612-179">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="8c612-179">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="8c612-180">1.2.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="8c612-180">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8c612-181">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8c612-181">Az.Accounts</span></span>
* <span data-ttu-id="8c612-182">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="8c612-182">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="8c612-183">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8c612-183">Update incorrect online help URLs</span></span>
* <span data-ttu-id="8c612-184">Uninstall-AzureRm için PC Çekirdeğine uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="8c612-184">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="8c612-185">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="8c612-185">Az.Aks</span></span>
* <span data-ttu-id="8c612-186">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8c612-186">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8c612-187">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8c612-187">Az.Automation</span></span>
* <span data-ttu-id="8c612-188">Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="8c612-188">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="8c612-189">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8c612-189">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="8c612-190">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8c612-190">Az.Cdn</span></span>
* <span data-ttu-id="8c612-191">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8c612-191">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8c612-192">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8c612-192">Az.Compute</span></span>
* <span data-ttu-id="8c612-193">Invoke-AzVMReimage cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="8c612-193">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="8c612-194">Set-AzVmss'ye TempDisk parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="8c612-194">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="8c612-195">New-AzVM'nin uyarı iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8c612-195">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="8c612-196">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8c612-196">Az.ContainerRegistry</span></span>
* <span data-ttu-id="8c612-197">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8c612-197">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8c612-198">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8c612-198">Az.DataFactory</span></span>
* <span data-ttu-id="8c612-199">ADF .Net SDK sürümü 3.0.0'a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8c612-199">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8c612-200">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8c612-200">Az.DataLakeStore</span></span>
* <span data-ttu-id="8c612-201">MSI kullanırken ADLS uç noktasındaki sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8c612-201">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="8c612-202">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="8c612-202">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="8c612-203">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8c612-203">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8c612-204">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8c612-204">Az.IotHub</span></span>
* <span data-ttu-id="8c612-205">Add-IotHubRoutingEndpoint cmdlet'ine Kodlama biçimi eklendi.</span><span class="sxs-lookup"><span data-stu-id="8c612-205">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8c612-206">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8c612-206">Az.KeyVault</span></span>
* <span data-ttu-id="8c612-207">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8c612-207">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8c612-208">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8c612-208">Az.Network</span></span>
* <span data-ttu-id="8c612-209">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8c612-209">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="8c612-210">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8c612-210">Az.Resources</span></span>
* <span data-ttu-id="8c612-211">'New-AzADAppCredential' ve 'New-AzADSpCredential' başvuru belgelerindeki hatalı örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8c612-211">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="8c612-212">Kaynak grubu dağıtım cmdlet'lerini yürütmeden önce '-TemplateFile' parametresi yolunun çözülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8c612-212">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="8c612-213">Az.Resources: Belgede New-AzureRmPolicyDefinition -Mode varsayılan değeri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8c612-213">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="8c612-214">Az.Resources: https://github.com/Azure/azure-powershell/issues/7522 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8c612-214">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="8c612-215">Az.Resources: https://github.com/Azure/azure-powershell/issues/5747 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8c612-215">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="8c612-216">'PSResourceGroupDeployment' nesnesinin biçimlendirme sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8c612-216">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="8c612-217">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="8c612-217">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8c612-218">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8c612-218">Az.ServiceFabric</span></span>
* <span data-ttu-id="8c612-219">VMSS modeline sertifika eklendiğinde ama özel durum oluştuğunda geri alma için hata düzeltmesi: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="8c612-219">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="8c612-220">Bazı hata iletileri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="8c612-220">Fix some error messages.</span></span>
* <span data-ttu-id="8c612-221">Az geçişinde çalışmayan New-AzServiceFabriCluster için varsayılan ARM şablonuyla küme oluşturma sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="8c612-221">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="8c612-222">Uzantıda küme kimliği denetlenerek küme/uygulama sertifikasının yalnızca kümeye karşılık gelen VM Ölçek Kümelerine eklenmesi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="8c612-222">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="8c612-223">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="8c612-223">Az.SignalR</span></span>
* <span data-ttu-id="8c612-224">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8c612-224">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="8c612-225">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8c612-225">Az.Sql</span></span>
* <span data-ttu-id="8c612-226">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8c612-226">Update incorrect online help URLs</span></span>
* <span data-ttu-id="8c612-227">LicenseType parametresinin parametre açıklaması olası değerlerle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8c612-227">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="8c612-228">Yönetilen örnek kimliği güncelleştirmesinin, güncelleştirilen tek özellik bu olduğunda çalışmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8c612-228">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="8c612-229">Yönetilen örnekte özel harmanlama desteği</span><span class="sxs-lookup"><span data-stu-id="8c612-229">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8c612-230">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8c612-230">Az.Storage</span></span>
* <span data-ttu-id="8c612-231">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8c612-231">Update incorrect online help URLs</span></span>
* <span data-ttu-id="8c612-232">Premium Depolama Hesabı klasik Günlük/Ölçüm desteği sağlamadığından, Premium Depolama Hesabında klasik Günlük/Ölçüm için get/set komutları kullanıldığında ayrıntılı hata iletisi veriliyor.</span><span class="sxs-lookup"><span data-stu-id="8c612-232">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="8c612-233">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="8c612-233">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="8c612-234">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="8c612-234">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="8c612-235">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="8c612-235">Az.TrafficManager</span></span>
* <span data-ttu-id="8c612-236">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8c612-236">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8c612-237">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8c612-237">Az.Websites</span></span>
* <span data-ttu-id="8c612-238">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8c612-238">Update incorrect online help URLs</span></span>
* <span data-ttu-id="8c612-239">Uygulama ASE'de barındırılıyorsa, sertifikayı doğru kaynak grubuna ve konuma yüklemek için 'New-AzWebAppSSLBinding' düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="8c612-239">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="8c612-240">SSL sertifikası bir uygulamaya bağlanırken etiketlerin üzerine yazılmaması için 'New-AzWebAppSSLBinding' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8c612-240">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="8c612-241">1.1.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="8c612-241">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8c612-242">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8c612-242">Az.Accounts</span></span>
* <span data-ttu-id="8c612-243">Enable-AzureRmAlias cmdlet'ine 'Local' Kapsamı eklendi</span><span class="sxs-lookup"><span data-stu-id="8c612-243">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8c612-244">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8c612-244">Az.Compute</span></span>
* <span data-ttu-id="8c612-245">Restart/Start/Stop/Remove/Set-AzVM ve Save-AzVMImage için ayarlanan ID parametresinde ad artık isteğe bağlı</span><span class="sxs-lookup"><span data-stu-id="8c612-245">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="8c612-246">Yardım dosyalarında ID parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8c612-246">Updated the description of ID in help files</span></span>
* <span data-ttu-id="8c612-247">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="8c612-247">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8c612-248">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8c612-248">Az.DataLakeStore</span></span>
* <span data-ttu-id="8c612-249">SDK düzeltmeleri için veri düzleminin SDK sürümü 1.1.14 olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8c612-249">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="8c612-250">getfilestatus ve liststatus için negatif acesstime ve modificationtime değerlerini işleme yöntemi düzeltildi, async iptal belirteci düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8c612-250">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="8c612-251">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="8c612-251">Az.EventGrid</span></span>
* <span data-ttu-id="8c612-252">2019-01-01 API sürümünü kullanmak için güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8c612-252">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="8c612-253">Aşağıdaki cmdlet'ler 2019-01-01 API sürümünde yeni senaryoyu destekleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8c612-253">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="8c612-254">New-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="8c612-254">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="8c612-255">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="8c612-255">Event Time-To-Live,</span></span>
        - <span data-ttu-id="8c612-256">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="8c612-256">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="8c612-257">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="8c612-257">Dead letter endpoint.</span></span>
    - <span data-ttu-id="8c612-258">Update-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="8c612-258">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="8c612-259">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="8c612-259">Event Time-To-Live,</span></span>
        - <span data-ttu-id="8c612-260">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="8c612-260">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="8c612-261">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="8c612-261">Dead letter endpoint.</span></span>
* <span data-ttu-id="8c612-262">New-AzureRmEventGridSubscription ve Update-AzureRmEventGridSubscription cmdlet'lerinde EndpointType seçeneği için yeni enum değerleri (storageQueue ve hybridConnection) eklendi.</span><span class="sxs-lookup"><span data-stu-id="8c612-262">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="8c612-263">Olay aboneliğini oluşturma veya güncelleştirme işleminde kullanıcının el ile bir eylem yapması beklendiğinde uyarı iletisi gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="8c612-263">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8c612-264">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8c612-264">Az.IotHub</span></span>
* <span data-ttu-id="8c612-265">IotHub SDK'sı en son sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8c612-265">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="8c612-266">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="8c612-266">Az.LogicApp</span></span>
* <span data-ttu-id="8c612-267">Get-AzLogicApp, Name değeri belirtilmemiş olanların tümünü listeliyor</span><span class="sxs-lookup"><span data-stu-id="8c612-267">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="8c612-268">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8c612-268">Az.Resources</span></span>
* <span data-ttu-id="8c612-269">'Get-AzResource' için '-ODataQuery' ve '-ResourceId' parametreleri sağlanırken ortaya çıkan parametre ayarlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8c612-269">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="8c612-270">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="8c612-270">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="8c612-271">New/Set-AzPolicyDefinition cmdlet'lerinde -Custom parametresinin işlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8c612-271">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="8c612-272">New-AzDeployment belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8c612-272">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="8c612-273">'New-AzADUser' için '-MailNickname' parametresi zorunlu hale getirildi</span><span class="sxs-lookup"><span data-stu-id="8c612-273">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="8c612-274">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="8c612-274">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="8c612-275">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="8c612-275">Az.SignalR</span></span>
* <span data-ttu-id="8c612-276">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="8c612-276">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="8c612-277">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8c612-277">Az.Sql</span></span>
* <span data-ttu-id="8c612-278">Depolama yönetimi istemci bağımlılığı ortak SDK uygulamasına dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="8c612-278">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8c612-279">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8c612-279">Az.Storage</span></span>
* <span data-ttu-id="8c612-280">Sas Token, OAuth veya Anonymous ile oluşturulduğunda Storage bağlamının StorageAccountName değeri gerçek Depolama Hesabı Adına ayarlanıyor</span><span class="sxs-lookup"><span data-stu-id="8c612-280">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="8c612-281">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="8c612-281">New-AzStorageContext</span></span>
* <span data-ttu-id="8c612-282">Blob Anlık Görüntü Nesnesinin Sas Belirteci '-FullUri' parametresiyle oluşturulduğunda, döndürülen Uri anlık görüntü Uri'si olacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8c612-282">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="8c612-283">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="8c612-283">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8c612-284">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8c612-284">Az.Websites</span></span>
* <span data-ttu-id="8c612-285">'Get-AzDeletedWebApp' cmdlet'indeki tarih ayrıştırma hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8c612-285">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="8c612-286">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="8c612-286">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="8c612-287">1.0.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="8c612-287">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="8c612-288">Genel</span><span class="sxs-lookup"><span data-stu-id="8c612-288">General</span></span>

- <span data-ttu-id="8c612-289">Az Modülü Genel Kullanıma Sunuldu</span><span class="sxs-lookup"><span data-stu-id="8c612-289">General Availability of Az Module</span></span>
- <span data-ttu-id="8c612-290">Her modül için çevrimiçi yardım</span><span class="sxs-lookup"><span data-stu-id="8c612-290">Online help for each module</span></span>
- <span data-ttu-id="8c612-291">Diğer ayrıntılar ve yol haritası için bkz. [Az Duyuru Sayfası](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="8c612-291">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="8c612-292">AzureRM’den geçiş hakkında bilgi edinmek için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8c612-292">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="8c612-293">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8c612-293">Az.Accounts</span></span>
- <span data-ttu-id="8c612-294">Önceki adı: Az.Profile</span><span class="sxs-lookup"><span data-stu-id="8c612-294">Changed from Az.Profile</span></span>
- <span data-ttu-id="8c612-295">Profil ve bağlam türleri için tablo biçimleri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8c612-295">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="8c612-296">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8c612-296">Az.ApiManagement</span></span>
- <span data-ttu-id="8c612-297">#7002 düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="8c612-297">Fixes for #7002</span></span>
- <span data-ttu-id="8c612-298">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8c612-298">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="8c612-299">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="8c612-299">Az.Batch</span></span>
- <span data-ttu-id="8c612-300">`PSComputeNode` üzerinde yeni `NodeAgentInformation` aracılığıyla bir havuzdaki her bir VM’de Azure Batch Düğüm Aracısı’nın hangi sürümünün çalıştığını görme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="8c612-300">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="8c612-301">`PSDataDisk` için `Caching` varsayılan ayarı artık `None` yerine `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="8c612-301">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="8c612-302">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8c612-302">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="8c612-303">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="8c612-303">Az.Billing</span></span>
- <span data-ttu-id="8c612-304">Billing, Consumption ve UsageAggregates cmdlet’lerini birleştirir, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8c612-304">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="8c612-305">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="8c612-305">Az.CognitivServices</span></span>
- <span data-ttu-id="8c612-306">New-AzureRmCognitiveServicesAccount işleminde kullanılabilen SkuName ve Typem için tamamlayıcılar eklendi</span><span class="sxs-lookup"><span data-stu-id="8c612-306">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="8c612-307">Get-AzCognitiveServicesAccountSkus cmdlet’inden GetSkusWithAccountParamSetName parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="8c612-307">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="8c612-308">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="8c612-308">Az.ContainerInstance</span></span>
- <span data-ttu-id="8c612-309">ManagedIdentity desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="8c612-309">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="8c612-310">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="8c612-310">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="8c612-311">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8c612-311">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="8c612-312">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8c612-312">Az.DataLakeStore</span></span>
- <span data-ttu-id="8c612-313">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8c612-313">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="8c612-314">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8c612-314">Az.Monitor</span></span>
- <span data-ttu-id="8c612-315">Az.Insights cmdlet’inin adı Az.Monitor olarak değiştirildi ve başka yeni değişiklikler yapıldı, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8c612-315">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="8c612-316">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8c612-316">Az.KeyVault</span></span>
- <span data-ttu-id="8c612-317">Çıkış türlerinden kullanım dışı 'PurgeDisabled' özelliği kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="8c612-317">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="8c612-318">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="8c612-318">Az.MachineLearning</span></span>
- <span data-ttu-id="8c612-319">Az.MachineLearningCompute modülünden cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="8c612-319">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="8c612-320">Az.Media</span><span class="sxs-lookup"><span data-stu-id="8c612-320">Az.Media</span></span>
- <span data-ttu-id="8c612-321">New-AzMediaService cmdlet’inden kullanım dışı -Tags diğer adı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="8c612-321">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="8c612-322">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8c612-322">Az.Network</span></span>
<span data-ttu-id="8c612-323">Application Gateway’de RewriteRuleSets parametresini yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="8c612-323">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="8c612-324">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="8c612-324">New cmdlets added:</span></span>
        - <span data-ttu-id="8c612-325">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8c612-325">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8c612-326">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8c612-326">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8c612-327">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8c612-327">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8c612-328">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8c612-328">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8c612-329">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8c612-329">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8c612-330">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="8c612-330">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="8c612-331">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="8c612-331">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="8c612-332">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="8c612-332">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="8c612-333">Cmdlet’ler isteğe bağlı -RewriteRuleSet parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8c612-333">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="8c612-334">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8c612-334">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="8c612-335">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="8c612-335">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="8c612-336">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="8c612-336">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="8c612-337">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8c612-337">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="8c612-338">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="8c612-338">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="8c612-339">New-AzureRmApplicationGatewayUrlPathMapConfig, Kimlik kullanarak Application Gateway’e KeyVault Desteği ekledi.</span><span class="sxs-lookup"><span data-stu-id="8c612-339">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="8c612-340">Cmdlet’ler isteğe bağlı -KeyVaultSecretId, -KeyVaultSecret parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8c612-340">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="8c612-341">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8c612-341">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="8c612-342">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8c612-342">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="8c612-343">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8c612-343">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="8c612-344">New-AzApplicationGateway cmdlet’i isteğe bağlı -UserAssignedIdentity parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8c612-344">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="8c612-345">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8c612-345">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="8c612-346">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8c612-346">Az.OperationalInsights</span></span>
- <span data-ttu-id="8c612-347">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8c612-347">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="8c612-348">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="8c612-348">Az.Profile</span></span>
- <span data-ttu-id="8c612-349">Modül adı Az.Accounts olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="8c612-349">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="8c612-350">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8c612-350">Az.RecoveryServices</span></span>
- <span data-ttu-id="8c612-351">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8c612-351">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="8c612-352">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8c612-352">Az.Resources</span></span>
- <span data-ttu-id="8c612-353">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8c612-353">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="8c612-354">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8c612-354">Az.ServiceFabric</span></span>
- <span data-ttu-id="8c612-355">Sertifikayı ortak ad ve parmak iziyle belirtme desteği</span><span class="sxs-lookup"><span data-stu-id="8c612-355">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="8c612-356">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8c612-356">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="8c612-357">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="8c612-357">Az.SIgnalR</span></span>
- <span data-ttu-id="8c612-358">SIgnalR için PowerShell cmdlet'leri Genel Kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="8c612-358">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="8c612-359">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8c612-359">Az.Sql</span></span>
- <span data-ttu-id="8c612-360">Tehdit Algılama cmdlet’lerine yeni Data_Exfiltration ve Unsafe_Action algılama türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="8c612-360">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="8c612-361">Sql Denetimi cmdlet'leri için belge örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8c612-361">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="8c612-362">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8c612-362">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="8c612-363">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8c612-363">Az.Storage</span></span>
- <span data-ttu-id="8c612-364">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8c612-364">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="8c612-365">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8c612-365">Az.Websites</span></span>
- <span data-ttu-id="8c612-366">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8c612-366">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="8c612-367">0.7.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="8c612-367">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="8c612-368">Genel</span><span class="sxs-lookup"><span data-stu-id="8c612-368">General</span></span>

* <span data-ttu-id="8c612-369">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="8c612-369">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="8c612-370">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8c612-370">Az.Compute</span></span>

* <span data-ttu-id="8c612-371">`New-AzVm(ss)` cmdlet’leri için basit parametre kümelerinde UltraSSD ve Galeri Görüntüleri desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="8c612-371">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="8c612-372">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8c612-372">Az.DataLakeStore</span></span>

* <span data-ttu-id="8c612-373">Adls hesabı etki alanının sonundaki eğik çizgi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8c612-373">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="8c612-374">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="8c612-374">Az.FrontDoor</span></span>

* <span data-ttu-id="8c612-375">Bazı bozuk bağlantılar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8c612-375">Fixed some broken links</span></span>
    - <span data-ttu-id="8c612-376">New-AzureRmFrontDoor ve Set-AzureRmFrontDoor makalelerinde, New-AzureRmFrontDoorHealthProbeSettingObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="8c612-376">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="8c612-377">New-AzureRmFrontDoorManagedRuleObject makalesinde, New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="8c612-377">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="8c612-378">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8c612-378">Az.RecoveryServices</span></span>

* <span data-ttu-id="8c612-379">Azure Dosya Paylaşımı geri yükleme işlemleri için istemci tarafı doğrulamalar eklendi.</span><span class="sxs-lookup"><span data-stu-id="8c612-379">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="8c612-380">Afs geri yükleme işlemi için storageAccountName ve storageAccountResourceGroupName isteğe bağlı hale getirildi.</span><span class="sxs-lookup"><span data-stu-id="8c612-380">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="8c612-381">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8c612-381">Az.Resources</span></span>

* <span data-ttu-id="8c612-382">[https://github.com/Azure/azure-powershell/issues/7402](https://github.com/Azure/azure-powershell/issues/7679) düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="8c612-382">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="8c612-383">Get-AzureRmRoleAssignment, klasik yöneticiler istenirken sağlanmışsa abonelik kapsamını kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8c612-383">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="8c612-384">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8c612-384">Az.Sql</span></span>

* <span data-ttu-id="8c612-385">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="8c612-385">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="8c612-386">Get-AzureRmSqlDatabaseVulnerabilityAssessment cmdlet’inin DotNet core ile kullanılması konusundaki bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8c612-386">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="8c612-387">SQL Denetimi cmdlet’leriyle ilgili yardım iletilerinin belgeleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="8c612-387">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="8c612-388">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8c612-388">Az.Storage</span></span>

* <span data-ttu-id="8c612-389">New-AzureRmStorageAccount cmdlet’ine -EnableHierarchicalNamespace eklendi</span><span class="sxs-lookup"><span data-stu-id="8c612-389">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="8c612-390">-DestContext girilmediğinde Dosya Kopyalama cmdlet’inin hedefte kaynak bağlamını yeniden kullanamamasına yol açan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8c612-390">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="8c612-391">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="8c612-391">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="8c612-392">Statik Web Sitesi yapılandırması için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="8c612-392">Support Static Website configuration</span></span>
    - <span data-ttu-id="8c612-393">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="8c612-393">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="8c612-394">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="8c612-394">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="8c612-395">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8c612-395">Az.Websites</span></span>

* <span data-ttu-id="8c612-396">Set-AzureRmWebApp ve Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8c612-396">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="8c612-397">Windows ve Linux kapsayıcı uygulamalarında bağlanacak Azure Depolama yollarının belirtilmesi için yeni parametre (-AzureStoragePath) eklendi.</span><span class="sxs-lookup"><span data-stu-id="8c612-397">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="8c612-398">Azure Depolama yollarını ayarlamak için yeni New-AzureRmWebAppAzureStoragePath cmdlet’inin çıktısını bir parametre olarak kullanın.</span><span class="sxs-lookup"><span data-stu-id="8c612-398">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="8c612-399">0.6.1 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="8c612-399">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="8c612-400">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8c612-400">Az.ApiManagement</span></span>
* <span data-ttu-id="8c612-401">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="8c612-401">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="8c612-402">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8c612-402">Az.Automation</span></span>
* <span data-ttu-id="8c612-403">Swagger tabanlı Azure Otomasyon cmdlet'leri</span><span class="sxs-lookup"><span data-stu-id="8c612-403">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="8c612-404">Güncelleştirme Yönetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="8c612-404">Added Update Management cmdlets</span></span>
* <span data-ttu-id="8c612-405">Kaynak Denetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="8c612-405">Added Source Control cmdlets</span></span>
* <span data-ttu-id="8c612-406">Remove-AzureRmAutomationHybridWorkerGroup cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="8c612-406">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="8c612-407">DSC Kayıt Düğümü komutu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8c612-407">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="8c612-408">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8c612-408">Az.Compute</span></span>
* <span data-ttu-id="8c612-409">SystemAssigned kimliği için kimlik sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8c612-409">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="8c612-410">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="8c612-410">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="8c612-411">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="8c612-411">Az.ContainerInstance</span></span>
* <span data-ttu-id="8c612-412">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="8c612-412">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="8c612-413">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="8c612-413">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="8c612-414">Market cmdlet'leri için örnekler açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8c612-414">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="8c612-415">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8c612-415">Az.Network</span></span>
* <span data-ttu-id="8c612-416">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="8c612-416">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="8c612-417">Desteklenen AzureFirewall Ağ Protokollerine yeniden ICMP eklendi</span><span class="sxs-lookup"><span data-stu-id="8c612-417">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="8c612-418">Test-AzureRmNetworkWatcherConnectivity cmdlet'i güncelleştirildi; hedef kimlik, adres ve bağlantı noktasında doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="8c612-418">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="8c612-419">VirtualNetwork eşlemesinde bellek kullanımıyla ilgili sorunlar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8c612-419">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="8c612-420">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="8c612-420">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="8c612-421">Korumalı dosya paylaşımı için ilke değiştirme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="8c612-421">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="8c612-422">İlke saat dilimi büyük harfe dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="8c612-422">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="8c612-423">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="8c612-423">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="8c612-424">New-AzureRmRecoveryServicesAsrProtectableItem cmdlet'indeki örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8c612-424">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="8c612-425">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="8c612-425">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="8c612-426">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="8c612-426">Az.Relay</span></span>
* <span data-ttu-id="8c612-427">Kullanıcının New-AzureRmRelayKey cmdlet'ine KeyValue sağlamasına olanak tanıyan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="8c612-427">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="8c612-428">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8c612-428">Az.Resources</span></span>
* <span data-ttu-id="8c612-429">`New-AzureRmPolicyAssignment` ve `Set-AzureRmPolicyAssignment` cmdlet'lerindeki kaynak kimliğiyle ilgili parametrelerin yardım belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8c612-429">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="8c612-430">New-AzureRmPolicyDefinition cmdlet'ine -Metadata kullanan bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="8c612-430">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="8c612-431">NetStandard'da Tag anahtarında büyük/küçük harf kullanımının korunmasına yönelik düzeltme yapıldı: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="8c612-431">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="8c612-432">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8c612-432">Az.ServiceFabric</span></span>
* <span data-ttu-id="8c612-433">Hataya neden olan değişiklikler yayınlanacağından kullanımdan kaldırılacak özellikleri belirten iletiler eklendi</span><span class="sxs-lookup"><span data-stu-id="8c612-433">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="8c612-434">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8c612-434">Az.Sql</span></span>
* <span data-ttu-id="8c612-435">Azure Sql Veritabanı Yönetilen Örneği ve Azure Sql Yönetilen Veritabanı'nındaki CRUD işlemleri için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="8c612-435">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="8c612-436">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="8c612-436">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="8c612-437">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="8c612-437">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="8c612-438">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="8c612-438">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="8c612-439">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="8c612-439">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="8c612-440">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="8c612-440">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="8c612-441">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="8c612-441">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="8c612-442">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="8c612-442">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="8c612-443">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="8c612-443">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="8c612-444">Sunucuda veya veritabanında Genişletilmiş Denetim İlkesi yönetimi etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8c612-444">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="8c612-445">Denetim günlüklerinde filtrelemeyi etkinleştirmek için yeni parametre (PredicateExpression) eklendi.</span><span class="sxs-lookup"><span data-stu-id="8c612-445">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="8c612-446">Cmdlet'ler, SQL istemcileri yerine Eski istemcileri kullanacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="8c612-446">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="8c612-447">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="8c612-447">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="8c612-448">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="8c612-448">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="8c612-449">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="8c612-449">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="8c612-450">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="8c612-450">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="8c612-451">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings cmdlet'inin depolama hesabı ad parametre kümesiyle kullanılmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8c612-451">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="8c612-452">0.5.0 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="8c612-452">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="8c612-453">Genel</span><span class="sxs-lookup"><span data-stu-id="8c612-453">General</span></span>
* <span data-ttu-id="8c612-454">Birçok temel cmdlet’e Kaynak Tamamlayıcıları eklendi - bunlar cmdlet’leri etkileşimli olarak çağırırken mevcut kaynak adları arasında gezinmenize olanak tanır</span><span class="sxs-lookup"><span data-stu-id="8c612-454">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="8c612-455">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="8c612-455">Az.Profile</span></span>
* <span data-ttu-id="8c612-456">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8c612-456">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="8c612-457">Connect-AzAccount cmdlet'indeki TenantId parametresi Tenant olarak yeniden adlandırıldı ve TenantId için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="8c612-457">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="8c612-458">Connect-AzAccount için TenantId açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8c612-458">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="8c612-459">Kiracı etki alanı sağlanırken başarısız oturum açma durumunda gösterilen hata iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8c612-459">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="8c612-460">Kiracıda abonelikleri olmayan hesaplar için bağlam adı çakışmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8c612-460">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="8c612-461">MSI kullanırken DataLake uç noktalarıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8c612-461">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="8c612-462">Bağlantı olmadığında 'Disconnect-AzAccount' oluşturulmasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8c612-462">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="8c612-463">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8c612-463">Az.CognitiveServices</span></span>
* <span data-ttu-id="8c612-464">Get-AzCognitiveServicesAccountSkus işlemi eklendi.</span><span class="sxs-lookup"><span data-stu-id="8c612-464">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8c612-465">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8c612-465">Az.Compute</span></span>
* <span data-ttu-id="8c612-466">Add-AzVmssVMDataDisk ve Remove-AzVmssVMDataDisk cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="8c612-466">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="8c612-467">Get-AzVMImage, AutomaticOSUpgradeProperties gösteriyor</span><span class="sxs-lookup"><span data-stu-id="8c612-467">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="8c612-468">SetAzVMChefExtension -BootstrapOptions ve -JsonAttribute seçeneği değerlerinin Json biçiminde ayarlanmamasıyla ilgili hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="8c612-468">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8c612-469">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8c612-469">Az.DataLakeStore</span></span>
* <span data-ttu-id="8c612-470">DataLake paketi 1.1.10'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8c612-470">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="8c612-471">Çok iş parçacıklı işlemlere varsayılan Concurrency değeri eklendi.</span><span class="sxs-lookup"><span data-stu-id="8c612-471">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="8c612-472">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="8c612-472">Az.Insights</span></span>
* <span data-ttu-id="8c612-473">7267 numaralı (Otomatik ölçeklendirme alanı) sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8c612-473">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="8c612-474">Yeni otomatik ölçeklendirme kuralı oluşturma sırasında numaralandırılmış parametrelerin düzgün ayarlanmamasıyla ilgili sorunlar (bunlar her zaman varsayılan değere ayarlanıyordu).</span><span class="sxs-lookup"><span data-stu-id="8c612-474">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="8c612-475">Set-AzDiagnosticSetting'in ayar oluşturma sırasında kategorilerin açıkça belirtilmesini gerektirmesiyle ilgili 7513 numaralı [Insights] sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8c612-475">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="8c612-476">Artık cmdlet oluşturma sırasında açık kategori gösteriminin etkinleştirilmesini gerektirmiyor; başka bir deyişle belgelerinde belirtildiği gibi çalışıyor</span><span class="sxs-lookup"><span data-stu-id="8c612-476">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8c612-477">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8c612-477">Az.Network</span></span>
* <span data-ttu-id="8c612-478">Aşağıdaki parametrelerde PeeringType parametresi zorunlu parametre olarak değiştirildi:-</span><span class="sxs-lookup"><span data-stu-id="8c612-478">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="8c612-479">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="8c612-479">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="8c612-480">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="8c612-480">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="8c612-481">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="8c612-481">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="8c612-482">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="8c612-482">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="8c612-483">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="8c612-483">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="8c612-484">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="8c612-484">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="8c612-485">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="8c612-485">Az.PolicyInsights</span></span>
* <span data-ttu-id="8c612-486">İlke düzeltme cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="8c612-486">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="8c612-487">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8c612-487">Az.Resources</span></span>
* <span data-ttu-id="8c612-488">[https://github.com/Azure/azure-powershell/issues/7402](https://github.com/Azure/azure-powershell/issues/7402) düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="8c612-488">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="8c612-489">'Get-AzResource' için '-ResourceId' parametresi kullanılarak kaynakların listelenmesine olanak tanındı</span><span class="sxs-lookup"><span data-stu-id="8c612-489">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="8c612-490">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8c612-490">Az.ServiceBus</span></span>
* <span data-ttu-id="8c612-491">PSServiceBusMigrationConfigurationAttributes'e Geçiş durumunun bilinmesine yardımcı olacak salt okunur MigrationState özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="8c612-491">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8c612-492">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8c612-492">Az.ServiceFabric</span></span>
* <span data-ttu-id="8c612-493">Linux Vmss'ye sertifika ekleme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="8c612-493">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="8c612-494">'Add-AzServiceFabricClusterCertificate' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8c612-494">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="8c612-495">Yeni sertifikadan doğru parmak izi kullanıyor (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="8c612-495">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="8c612-496">Özel durum doğru görüntüleniyor (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="8c612-496">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="8c612-497">'Update-AzServiceFabricDurability', Vmss CreateOrUpdate işlemini başlatmadan önce küme yapılandırmasını güncelleştirecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="8c612-497">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="8c612-498">0.4.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="8c612-498">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="8c612-499">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="8c612-499">Az.Profile</span></span>
* <span data-ttu-id="8c612-500">CloudShell’de Get-AzSubscription sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="8c612-500">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="8c612-501">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="8c612-501">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8c612-502">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8c612-502">Az.Compute</span></span>
* <span data-ttu-id="8c612-503">'New-AzVm' için basit parametre kümesi kullanıldığında hızlandırılmış ağların açılacağı VM boyutları beyaz listesine yeni boyutlar eklendi</span><span class="sxs-lookup"><span data-stu-id="8c612-503">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="8c612-504">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="8c612-504">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8c612-505">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8c612-505">Az.DataLakeStore</span></span>
* <span data-ttu-id="8c612-506">Sanal Ağ Kuralları desteği ekleme</span><span class="sxs-lookup"><span data-stu-id="8c612-506">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="8c612-507">Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store sanal ağ kuralını alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="8c612-507">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="8c612-508">Add-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabına sanal ağ kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="8c612-508">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="8c612-509">Set-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabındaki belirtilen sanal ağ kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="8c612-509">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="8c612-510">Remove-AzDataLakeStoreVirtualNetworkRule: Bir Azure Data Lake Store sanal ağ kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="8c612-510">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8c612-511">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8c612-511">Az.Network</span></span>
* <span data-ttu-id="8c612-512">Test-AzNetworkWatcherConnectivity cmdlet'i güncelleştirildi, arka uca protokol değerini geçiriyor.</span><span class="sxs-lookup"><span data-stu-id="8c612-512">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="8c612-513">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="8c612-513">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8c612-514">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8c612-514">Az.Resources</span></span>
* <span data-ttu-id="8c612-515">Get-AzRoleDefinition cmdlet'inin anlaşılmaz bir özel durum oluşturmasına neden olan hata (varsayılan profilin içinde abonelik olmadığında ve hiçbir kapsam belirtilmediğinde), senaryoya anlamlı bir özel durum eklenerek düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="8c612-515">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="8c612-516">Ayrıca varsayılan parametre kümesi 'RoleDefinitionNameParameterSet' olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="8c612-516">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="8c612-517">0.3.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="8c612-517">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="8c612-518">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="8c612-518">Azure.Storage</span></span>
* <span data-ttu-id="8c612-519">Hedefte meta veri sorunu olduğunda Fix Copy Blob/File meta verileri kopyalamayacak</span><span class="sxs-lookup"><span data-stu-id="8c612-519">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="8c612-520">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="8c612-520">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="8c612-521">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="8c612-521">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="8c612-522">Belirli bir konumunun Depolama kaynağı kullanımını alma desteği ve genel Depolama kayrağı kullanımını almak için uyarı iletisi ekleme kullanımdan kalktı.</span><span class="sxs-lookup"><span data-stu-id="8c612-522">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="8c612-523">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="8c612-523">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="8c612-524">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8c612-524">Az.CognitiveServices</span></span>
* <span data-ttu-id="8c612-525">Mevcut hesap olmadan Get-AzCognitiveServicesAccountSkus desteği.</span><span class="sxs-lookup"><span data-stu-id="8c612-525">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8c612-526">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8c612-526">Az.Compute</span></span>
* <span data-ttu-id="8c612-527">Get-AzVM -ResourceGroupName <rg> gerektiğinde 50'den fazla sonuç döndürecek şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8c612-527">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="8c612-528">New-AzVmss cmdlet'inin yardımına 'SimpleParameterSet' örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="8c612-528">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="8c612-529">Azure Disk Şifrelemesi ilerleme durumu iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8c612-529">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="8c612-530">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="8c612-530">Az.DataFactoryV2</span></span>
* <span data-ttu-id="8c612-531">ADF .Net SDK sürümü 2.3.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="8c612-531">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8c612-532">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8c612-532">Az.Network</span></span>
* <span data-ttu-id="8c612-533">NetworkProfile işlevselliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="8c612-533">Added NetworkProfile functionality.</span></span> <span data-ttu-id="8c612-534">yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="8c612-534">new cmdlets added</span></span>
    - <span data-ttu-id="8c612-535">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8c612-535">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="8c612-536">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8c612-536">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="8c612-537">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8c612-537">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="8c612-538">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8c612-538">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="8c612-539">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="8c612-539">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="8c612-540">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="8c612-540">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="8c612-541">Alt Ağ Modeline hizmet ilişki bağlantısı eklendi</span><span class="sxs-lookup"><span data-stu-id="8c612-541">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="8c612-542">New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="8c612-542">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="8c612-543">Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="8c612-543">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="8c612-544">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="8c612-544">Az.RedisCache</span></span>
* <span data-ttu-id="8c612-545">Bundan sonra Size parametresi olarak her dizeye izin veriliyor.</span><span class="sxs-lookup"><span data-stu-id="8c612-545">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="8c612-546">PSArgumentCompleter açılan listesine P5 eklendi</span><span class="sxs-lookup"><span data-stu-id="8c612-546">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="8c612-547">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8c612-547">Az.Resources</span></span>
* <span data-ttu-id="8c612-548">Set-AzPolicyDefinition'a eksik -Mode parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="8c612-548">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="8c612-549">Origin öğesi User içeren işlemler için Get-AzProviderOperation commandlet hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8c612-549">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="8c612-550">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8c612-550">Az.Sql</span></span>
* <span data-ttu-id="8c612-551">Bazı yedekleme cmdlet'lerinin geçerli Azure aboneliğini tanıyamamasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="8c612-551">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8c612-552">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8c612-552">Az.Websites</span></span>
* <span data-ttu-id="8c612-553">Yeni Get-AzWebAppContainerContinuousDeploymentUrl Cmdlet'i - Kapsayıcı Sürekli Dağıtım Web Kancası URL'sini alıyor</span><span class="sxs-lookup"><span data-stu-id="8c612-553">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="8c612-554">Yeni New-AzWebAppContainerPSSession ve Enter-WebAppContainerPSSession Cmdlet'leri - Windows kapsayıcı uygulamasında PowerShell uzak oturumunu başlatıyor</span><span class="sxs-lookup"><span data-stu-id="8c612-554">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="8c612-555">0.2.0 - Eylül 2018</span><span class="sxs-lookup"><span data-stu-id="8c612-555">0.2.0 - September 2018</span></span>
 <span data-ttu-id="8c612-556">İlk Yayın</span><span class="sxs-lookup"><span data-stu-id="8c612-556">Initial Release</span></span>