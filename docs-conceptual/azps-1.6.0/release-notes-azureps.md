---
ms.openlocfilehash: 2db9810e20254373a487013de50d4297d4ec50d5
ms.sourcegitcommit: 8f59e11e5c991543964154d63648aa1e6ae22512
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/26/2019
ms.locfileid: "58475638"
---
## <a name="160---march-2019"></a><span data-ttu-id="6e189-101">1.6.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="6e189-101">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="6e189-102">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="6e189-102">Highlights since the last major release</span></span>
* <span data-ttu-id="6e189-103">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="6e189-103">General availability of `Az` module</span></span>
* <span data-ttu-id="6e189-104">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="6e189-104">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="6e189-105">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="6e189-105">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="6e189-106">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="6e189-106">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="6e189-107">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="6e189-107">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="6e189-108">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="6e189-108">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="6e189-109">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="6e189-109">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6e189-110">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6e189-110">Az.Automation</span></span>
* <span data-ttu-id="6e189-111">Aşağıdaki yeni özellikleri desteklemek için Azure otomasyonu güncelleştirme yönetimi değişikliği:</span><span class="sxs-lookup"><span data-stu-id="6e189-111">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="6e189-112">Dinamik gruplandırma</span><span class="sxs-lookup"><span data-stu-id="6e189-112">Dynamic grouping</span></span>
    * <span data-ttu-id="6e189-113">Ön-Son betik</span><span class="sxs-lookup"><span data-stu-id="6e189-113">Pre-Post script</span></span>
    * <span data-ttu-id="6e189-114">Yeniden Başlatma Ayarı</span><span class="sxs-lookup"><span data-stu-id="6e189-114">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6e189-115">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6e189-115">Az.Compute</span></span>
* <span data-ttu-id="6e189-116">Get-AzVmBootDiagnosticsData içinde yol çözümleme sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="6e189-116">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="6e189-117">İşlem istemci kitaplığı 25.0.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="6e189-117">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6e189-118">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6e189-118">Az.KeyVault</span></span>
* <span data-ttu-id="6e189-119">KeyVault cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="6e189-119">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6e189-120">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6e189-120">Az.Network</span></span>
* <span data-ttu-id="6e189-121">Azure Güvenlik Duvarı için Tehdit Bilgileri desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="6e189-121">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="6e189-122">Application Gateway Güvenlik Duvarı İlkesi üst düzey kaynağı ve Özel Kurallar eklendi</span><span class="sxs-lookup"><span data-stu-id="6e189-122">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6e189-123">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6e189-123">Az.RecoveryServices</span></span>
* <span data-ttu-id="6e189-124">Anında RP desteği için Azure VM ilkesine SnapshotRetentionInDays eklendi</span><span class="sxs-lookup"><span data-stu-id="6e189-124">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="6e189-125">Kapsayıcı kaydını kaldırmak için kanal desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="6e189-125">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="6e189-126">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6e189-126">Az.Resources</span></span>
* <span data-ttu-id="6e189-127">Get-AzResource ve Get-AzResourceGroup için joker karakter desteği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6e189-127">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="6e189-128">ARM'ye genel çağrı yapılırken kullanılan kimlik bilgileri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6e189-128">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="6e189-129">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6e189-129">Az.Sql</span></span>
* <span data-ttu-id="6e189-130">Yeni DetectionType'lar eklendiğinde gelecekte kullanılabilmesini sağlamak ve otomatik tamamlamayı da desteklemek için Tehdit Algılama cmdlet'lerinin DetectionType olan parametresi (ExcludeDetectionType) string[] olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="6e189-130">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6e189-131">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6e189-131">Az.Storage</span></span>
* <span data-ttu-id="6e189-132">Depolama hesabında Yönetim İlkesini Alma/Ayarlama/Kaldırma desteği</span><span class="sxs-lookup"><span data-stu-id="6e189-132">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="6e189-133">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="6e189-133">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="6e189-134">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="6e189-134">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="6e189-135">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="6e189-135">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="6e189-136">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="6e189-136">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="6e189-137">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="6e189-137">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="6e189-138">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="6e189-138">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6e189-139">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6e189-139">Az.Websites</span></span>
* <span data-ttu-id="6e189-140">'New-AzWebApp -IncludeSourceWebAppSlots' kullanarak tüm yuvaların kopyalanmasını kesintiye uğratan ARM şablon hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6e189-140">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="6e189-141">1.5.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="6e189-141">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6e189-142">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6e189-142">Az.Accounts</span></span>
* <span data-ttu-id="6e189-143">AutoRest tarafından oluşturulan cmdlet’leri desteklemek için 'Register-AzModule' komutu eklendi</span><span class="sxs-lookup"><span data-stu-id="6e189-143">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="6e189-144">Connect-AzAccount örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6e189-144">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6e189-145">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6e189-145">Az.Automation</span></span>
* <span data-ttu-id="6e189-146">Birden fazla Azure Otomasyonu cmdlet’inde belirli aylık zamanlamalar alınırken yaşanan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6e189-146">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="6e189-147">Yalnızca ilk 20 düğümü döndüren Get-AzAutomationDscNode düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="6e189-147">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="6e189-148">Artık tüm düğümleri döndürür</span><span class="sxs-lookup"><span data-stu-id="6e189-148">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="6e189-149">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6e189-149">Az.Cdn</span></span>
* <span data-ttu-id="6e189-150">Özel Etki Alanı Https Etkinleştirmesi/Devre Dışı Bırakması için yeni PowerShell cmdlet’leri eklendi ve eskiler kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="6e189-150">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6e189-151">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6e189-151">Az.Compute</span></span>
* <span data-ttu-id="6e189-152">Get cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="6e189-152">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6e189-153">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6e189-153">Az.DataFactory</span></span>
* <span data-ttu-id="6e189-154">ADF .Net SDK sürümü 3.0.1'e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6e189-154">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="6e189-155">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="6e189-155">Az.LogicApp</span></span>
* <span data-ttu-id="6e189-156">Yalnızca ilk sonuç sayfasını getiren ListWorkflows için düzeltme</span><span class="sxs-lookup"><span data-stu-id="6e189-156">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6e189-157">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6e189-157">Az.Network</span></span>
* <span data-ttu-id="6e189-158">Network cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="6e189-158">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6e189-159">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6e189-159">Az.RecoveryServices</span></span>
* <span data-ttu-id="6e189-160">Azure VM desteğine SQL Server eklendi</span><span class="sxs-lookup"><span data-stu-id="6e189-160">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="6e189-161">SDK Güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="6e189-161">SDK Update</span></span>
* <span data-ttu-id="6e189-162">Get-ProtectableItem içindeki Removed VMappContainer denetimi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="6e189-162">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="6e189-163">Get-ProtectableItem için Name ve ServerName parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="6e189-163">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="6e189-164">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6e189-164">Az.Resources</span></span>
* <span data-ttu-id="6e189-165">Dağıtım cmdlet’lerine `-TemplateObject` parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="6e189-165">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="6e189-166">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="6e189-166">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="6e189-167">`Get-AzResource` sonucu `Set-AzResource` üzerine aktarılırken oluşan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6e189-167">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="6e189-168">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="6e189-168">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="6e189-169">`Set-AzResource` çalıştırılırken JSON veri türü değişikliğine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6e189-169">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="6e189-170">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="6e189-170">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="6e189-171">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6e189-171">Az.Sql</span></span>
* <span data-ttu-id="6e189-172">AuditingEndpointsCommunicator güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="6e189-172">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="6e189-173">Yeni tanılama ayarları oluşturulurken kenar durumunun davranışı düzeltiliyor.</span><span class="sxs-lookup"><span data-stu-id="6e189-173">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6e189-174">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6e189-174">Az.Storage</span></span>
* <span data-ttu-id="6e189-175">Depolama hesabı oluşturulurken Support Kind BlockBlobStorage desteği sağlandı      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6e189-175">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="6e189-176">1.4.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="6e189-176">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="6e189-177">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6e189-177">Az.AnalysisServices</span></span>
* <span data-ttu-id="6e189-178">AddAzureASAccount cmdlet'i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="6e189-178">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6e189-179">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6e189-179">Az.Automation</span></span>
* <span data-ttu-id="6e189-180">Import-AzAutomationDscNodeConfiguration için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6e189-180">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="6e189-181">Import-AzAutomationDscConfiguration cmdlet'ine yapılandırma adı doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="6e189-181">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="6e189-182">Import-AzAutomationDscConfiguration cmdlet'i için hata işleme iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="6e189-182">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="6e189-183">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6e189-183">Az.CognitiveServices</span></span>
* <span data-ttu-id="6e189-184">Kaynağın alt etki alanını belirtmek amacıyla kullanılan New-AzCognitiveServicesAccount için CustomSubdomainName adlı, isteğe bağlı, yeni bir parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="6e189-184">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6e189-185">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6e189-185">Az.Compute</span></span>
* <span data-ttu-id="6e189-186">Kimlik parametresi kümeleriyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6e189-186">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="6e189-187">Get-AzVMExtension, Name parametresi sağlanmadığında yüklü tüm uzantıları listeleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6e189-187">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="6e189-188">Update-AzImage cmdlet’ine Tag ve ResourceId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="6e189-188">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="6e189-189">Get-AzVmssVM, örnek kimliği olmadan ve InstanceView ile, örnek görünümüne sahip VMSS VM’lerini listeleyebilir.</span><span class="sxs-lookup"><span data-stu-id="6e189-189">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6e189-190">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6e189-190">Az.DataLakeStore</span></span>
* <span data-ttu-id="6e189-191">ADL silinmiş öğe listeleme ve geri yükleme cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="6e189-191">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6e189-192">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6e189-192">Az.EventHub</span></span>
* <span data-ttu-id="6e189-193">EventHub’ın CaptureDescription sınıfında Boş Arşivleri Atlamak için SkipEmptyArchives adlı yeni Boole özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="6e189-193">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="6e189-194">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6e189-194">Az.KeyVault</span></span>
* <span data-ttu-id="6e189-195">Set-AzKeyVaultSecret’daki etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6e189-195">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="6e189-196">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="6e189-196">Az.LogicApp</span></span>
* <span data-ttu-id="6e189-197">Tümleştirme Hesapları için Temel SKU eklendi</span><span class="sxs-lookup"><span data-stu-id="6e189-197">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="6e189-198">XSLT 2.0, XSLT 3.0 ve Liquid Eşleşme Türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="6e189-198">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="6e189-199">Tümleştirme Hesabı Bütünleştirilmiş Kodları için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="6e189-199">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="6e189-200">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="6e189-200">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="6e189-201">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="6e189-201">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="6e189-202">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="6e189-202">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="6e189-203">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="6e189-203">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="6e189-204">Tümleştirme Hesabı Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="6e189-204">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="6e189-205">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="6e189-205">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="6e189-206">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="6e189-206">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="6e189-207">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="6e189-207">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="6e189-208">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="6e189-208">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="6e189-209">Logic Apps SDK sürüm 4.1.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6e189-209">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6e189-210">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6e189-210">Az.Monitor</span></span>
* <span data-ttu-id="6e189-211">Get-AzMetric için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6e189-211">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6e189-212">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6e189-212">Az.Network</span></span>
* <span data-ttu-id="6e189-213">Add-AzApplicationGatewayCustomError için yardım örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6e189-213">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6e189-214">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6e189-214">Az.OperationalInsights</span></span>
* <span data-ttu-id="6e189-215">New ve Get ApplicationInsights veri kaynağı için ek destek sunuldu.</span><span class="sxs-lookup"><span data-stu-id="6e189-215">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="6e189-216">Belirli bir çalışma alanı için belirli ve tüm Get ApplicationInsights veri kaynaklarını desteklemek için yeni ‘ApplicationInsights’ türü eklendi.</span><span class="sxs-lookup"><span data-stu-id="6e189-216">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="6e189-217">Belirli Application-Insights kaynak parametrelerine (abonelik kimliği, resourceGroupName ve ad) göre veri kaynağı oluşturmak için New-AzOperationalInsightsApplicationInsightsDataSource cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="6e189-217">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="6e189-218">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6e189-218">Az.Resources</span></span>
* <span data-ttu-id="6e189-219">https://github.com/Azure/azure-powershell/issues/8166 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6e189-219">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="6e189-220">https://github.com/Azure/azure-powershell/issues/8235 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6e189-220">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="6e189-221">https://github.com/Azure/azure-powershell/issues/6219 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6e189-221">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="6e189-222">KeyCredentials’ın tekrar oluşturmasını engelleyen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6e189-222">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="6e189-223">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6e189-223">Az.Sql</span></span>
* <span data-ttu-id="6e189-224">SQL DB Hiper Ölçeklendirme katmanı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="6e189-224">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="6e189-225">Geri yükleme isteğinde gereksiz özellikler ayarlandığı için geri yüklemenin başarısız olmasına yol açan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6e189-225">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6e189-226">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6e189-226">Az.Websites</span></span>
* <span data-ttu-id="6e189-227">Get-AzWebAppSlotMetrics örneği düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6e189-227">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="6e189-228">1.3.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="6e189-228">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6e189-229">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6e189-229">Az.Accounts</span></span>
* <span data-ttu-id="6e189-230">En son ClientRuntime sürümüne güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="6e189-230">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="6e189-231">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6e189-231">Az.AnalysisServices</span></span>
<span data-ttu-id="6e189-232">Az.AnalysisServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="6e189-232">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6e189-233">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6e189-233">Az.Compute</span></span>
* <span data-ttu-id="6e189-234">AEM uzantısı: UltraSSD ile P60,P70 ve P80 diskleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="6e189-234">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="6e189-235">Set-AzVMBootDiagnostics yardım açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6e189-235">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="6e189-236">Update-AzImage için yardım açıklaması ve örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6e189-236">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6e189-237">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6e189-237">Az.RecoveryServices</span></span>
<span data-ttu-id="6e189-238">Az.RecoveryServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="6e189-238">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6e189-239">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6e189-239">Az.Resources</span></span>
* <span data-ttu-id="6e189-240">Kaynak grupları için etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6e189-240">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="6e189-241">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="6e189-241">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="6e189-242">`Get-AzureRmRoleAssignment` komutunun -ErrorAction'a uymama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6e189-242">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="6e189-243">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="6e189-243">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="6e189-244">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6e189-244">Az.Sql</span></span>
* <span data-ttu-id="6e189-245">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="6e189-245">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="6e189-246">Azure hesabında oturum açılmamasının SQL cmdlet'leri yürütülürken nullref özel durumuna yol açması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6e189-246">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="6e189-247">Get-AzSqlCapability'de null başvuru özel durumu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6e189-247">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="6e189-248">1.2.1 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="6e189-248">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6e189-249">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6e189-249">Az.Accounts</span></span>
* <span data-ttu-id="6e189-250">Kimlik Doğrulaması'nın doğru yayınını içeren sürümü</span><span class="sxs-lookup"><span data-stu-id="6e189-250">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="6e189-251">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6e189-251">Az.AnalysisServices</span></span>
* <span data-ttu-id="6e189-252">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="6e189-252">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6e189-253">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6e189-253">Az.RecoveryServices</span></span>
* <span data-ttu-id="6e189-254">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="6e189-254">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="6e189-255">1.2.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="6e189-255">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6e189-256">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6e189-256">Az.Accounts</span></span>
* <span data-ttu-id="6e189-257">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="6e189-257">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="6e189-258">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6e189-258">Update incorrect online help URLs</span></span>
* <span data-ttu-id="6e189-259">Uninstall-AzureRm için PC Çekirdeğine uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="6e189-259">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="6e189-260">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="6e189-260">Az.Aks</span></span>
* <span data-ttu-id="6e189-261">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6e189-261">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6e189-262">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6e189-262">Az.Automation</span></span>
* <span data-ttu-id="6e189-263">Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="6e189-263">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="6e189-264">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6e189-264">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="6e189-265">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6e189-265">Az.Cdn</span></span>
* <span data-ttu-id="6e189-266">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6e189-266">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6e189-267">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6e189-267">Az.Compute</span></span>
* <span data-ttu-id="6e189-268">Invoke-AzVMReimage cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="6e189-268">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="6e189-269">Set-AzVmss'ye TempDisk parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="6e189-269">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="6e189-270">New-AzVM'nin uyarı iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6e189-270">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="6e189-271">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="6e189-271">Az.ContainerRegistry</span></span>
* <span data-ttu-id="6e189-272">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6e189-272">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6e189-273">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6e189-273">Az.DataFactory</span></span>
* <span data-ttu-id="6e189-274">ADF .Net SDK sürümü 3.0.0'a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6e189-274">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6e189-275">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6e189-275">Az.DataLakeStore</span></span>
* <span data-ttu-id="6e189-276">MSI kullanırken ADLS uç noktasındaki sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6e189-276">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="6e189-277">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="6e189-277">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="6e189-278">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6e189-278">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6e189-279">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6e189-279">Az.IotHub</span></span>
* <span data-ttu-id="6e189-280">Add-IotHubRoutingEndpoint cmdlet'ine Kodlama biçimi eklendi.</span><span class="sxs-lookup"><span data-stu-id="6e189-280">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6e189-281">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6e189-281">Az.KeyVault</span></span>
* <span data-ttu-id="6e189-282">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6e189-282">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6e189-283">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6e189-283">Az.Network</span></span>
* <span data-ttu-id="6e189-284">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6e189-284">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="6e189-285">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6e189-285">Az.Resources</span></span>
* <span data-ttu-id="6e189-286">'New-AzADAppCredential' ve 'New-AzADSpCredential' başvuru belgelerindeki hatalı örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6e189-286">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="6e189-287">Kaynak grubu dağıtım cmdlet'lerini yürütmeden önce '-TemplateFile' parametresi yolunun çözülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6e189-287">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="6e189-288">Az.Resources: Belgede New-AzureRmPolicyDefinition -Mode varsayılan değeri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6e189-288">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="6e189-289">Az.Resources: https://github.com/Azure/azure-powershell/issues/7522 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6e189-289">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="6e189-290">Az.Resources: https://github.com/Azure/azure-powershell/issues/5747 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6e189-290">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="6e189-291">'PSResourceGroupDeployment' nesnesinin biçimlendirme sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6e189-291">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="6e189-292">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="6e189-292">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6e189-293">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6e189-293">Az.ServiceFabric</span></span>
* <span data-ttu-id="6e189-294">VMSS modeline sertifika eklendiğinde ama özel durum oluştuğunda geri alma için hata düzeltmesi: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="6e189-294">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="6e189-295">Bazı hata iletileri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="6e189-295">Fix some error messages.</span></span>
* <span data-ttu-id="6e189-296">Az geçişinde çalışmayan New-AzServiceFabriCluster için varsayılan ARM şablonuyla küme oluşturma sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="6e189-296">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="6e189-297">Uzantıda küme kimliği denetlenerek küme/uygulama sertifikasının yalnızca kümeye karşılık gelen VM Ölçek Kümelerine eklenmesi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="6e189-297">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="6e189-298">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="6e189-298">Az.SignalR</span></span>
* <span data-ttu-id="6e189-299">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6e189-299">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="6e189-300">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6e189-300">Az.Sql</span></span>
* <span data-ttu-id="6e189-301">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6e189-301">Update incorrect online help URLs</span></span>
* <span data-ttu-id="6e189-302">LicenseType parametresinin parametre açıklaması olası değerlerle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6e189-302">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="6e189-303">Yönetilen örnek kimliği güncelleştirmesinin, güncelleştirilen tek özellik bu olduğunda çalışmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6e189-303">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="6e189-304">Yönetilen örnekte özel harmanlama desteği</span><span class="sxs-lookup"><span data-stu-id="6e189-304">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6e189-305">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6e189-305">Az.Storage</span></span>
* <span data-ttu-id="6e189-306">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6e189-306">Update incorrect online help URLs</span></span>
* <span data-ttu-id="6e189-307">Premium Depolama Hesabı klasik Günlük/Ölçüm desteği sağlamadığından, Premium Depolama Hesabında klasik Günlük/Ölçüm için get/set komutları kullanıldığında ayrıntılı hata iletisi veriliyor.</span><span class="sxs-lookup"><span data-stu-id="6e189-307">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="6e189-308">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="6e189-308">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="6e189-309">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="6e189-309">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="6e189-310">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="6e189-310">Az.TrafficManager</span></span>
* <span data-ttu-id="6e189-311">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6e189-311">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6e189-312">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6e189-312">Az.Websites</span></span>
* <span data-ttu-id="6e189-313">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6e189-313">Update incorrect online help URLs</span></span>
* <span data-ttu-id="6e189-314">Uygulama ASE'de barındırılıyorsa, sertifikayı doğru kaynak grubuna ve konuma yüklemek için 'New-AzWebAppSSLBinding' düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="6e189-314">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="6e189-315">SSL sertifikası bir uygulamaya bağlanırken etiketlerin üzerine yazılmaması için 'New-AzWebAppSSLBinding' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6e189-315">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="6e189-316">1.1.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="6e189-316">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6e189-317">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6e189-317">Az.Accounts</span></span>
* <span data-ttu-id="6e189-318">Enable-AzureRmAlias cmdlet'ine 'Local' Kapsamı eklendi</span><span class="sxs-lookup"><span data-stu-id="6e189-318">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6e189-319">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6e189-319">Az.Compute</span></span>
* <span data-ttu-id="6e189-320">Restart/Start/Stop/Remove/Set-AzVM ve Save-AzVMImage için ayarlanan ID parametresinde ad artık isteğe bağlı</span><span class="sxs-lookup"><span data-stu-id="6e189-320">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="6e189-321">Yardım dosyalarında ID parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6e189-321">Updated the description of ID in help files</span></span>
* <span data-ttu-id="6e189-322">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="6e189-322">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6e189-323">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6e189-323">Az.DataLakeStore</span></span>
* <span data-ttu-id="6e189-324">SDK düzeltmeleri için veri düzleminin SDK sürümü 1.1.14 olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="6e189-324">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="6e189-325">getfilestatus ve liststatus için negatif acesstime ve modificationtime değerlerini işleme yöntemi düzeltildi, async iptal belirteci düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6e189-325">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="6e189-326">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="6e189-326">Az.EventGrid</span></span>
* <span data-ttu-id="6e189-327">2019-01-01 API sürümünü kullanmak için güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="6e189-327">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="6e189-328">Aşağıdaki cmdlet'ler 2019-01-01 API sürümünde yeni senaryoyu destekleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6e189-328">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="6e189-329">New-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="6e189-329">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="6e189-330">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="6e189-330">Event Time-To-Live,</span></span>
        - <span data-ttu-id="6e189-331">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="6e189-331">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="6e189-332">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="6e189-332">Dead letter endpoint.</span></span>
    - <span data-ttu-id="6e189-333">Update-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="6e189-333">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="6e189-334">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="6e189-334">Event Time-To-Live,</span></span>
        - <span data-ttu-id="6e189-335">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="6e189-335">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="6e189-336">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="6e189-336">Dead letter endpoint.</span></span>
* <span data-ttu-id="6e189-337">New-AzureRmEventGridSubscription ve Update-AzureRmEventGridSubscription cmdlet'lerinde EndpointType seçeneği için yeni enum değerleri (storageQueue ve hybridConnection) eklendi.</span><span class="sxs-lookup"><span data-stu-id="6e189-337">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="6e189-338">Olay aboneliğini oluşturma veya güncelleştirme işleminde kullanıcının el ile bir eylem yapması beklendiğinde uyarı iletisi gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="6e189-338">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6e189-339">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6e189-339">Az.IotHub</span></span>
* <span data-ttu-id="6e189-340">IotHub SDK'sı en son sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6e189-340">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="6e189-341">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="6e189-341">Az.LogicApp</span></span>
* <span data-ttu-id="6e189-342">Get-AzLogicApp, Name değeri belirtilmemiş olanların tümünü listeliyor</span><span class="sxs-lookup"><span data-stu-id="6e189-342">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="6e189-343">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6e189-343">Az.Resources</span></span>
* <span data-ttu-id="6e189-344">'Get-AzResource' için '-ODataQuery' ve '-ResourceId' parametreleri sağlanırken ortaya çıkan parametre ayarlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6e189-344">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="6e189-345">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="6e189-345">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="6e189-346">New/Set-AzPolicyDefinition cmdlet'lerinde -Custom parametresinin işlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6e189-346">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="6e189-347">New-AzDeployment belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6e189-347">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="6e189-348">'New-AzADUser' için '-MailNickname' parametresi zorunlu hale getirildi</span><span class="sxs-lookup"><span data-stu-id="6e189-348">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="6e189-349">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="6e189-349">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="6e189-350">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="6e189-350">Az.SignalR</span></span>
* <span data-ttu-id="6e189-351">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="6e189-351">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="6e189-352">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6e189-352">Az.Sql</span></span>
* <span data-ttu-id="6e189-353">Depolama yönetimi istemci bağımlılığı ortak SDK uygulamasına dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="6e189-353">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6e189-354">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6e189-354">Az.Storage</span></span>
* <span data-ttu-id="6e189-355">Sas Token, OAuth veya Anonymous ile oluşturulduğunda Storage bağlamının StorageAccountName değeri gerçek Depolama Hesabı Adına ayarlanıyor</span><span class="sxs-lookup"><span data-stu-id="6e189-355">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="6e189-356">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="6e189-356">New-AzStorageContext</span></span>
* <span data-ttu-id="6e189-357">Blob Anlık Görüntü Nesnesinin Sas Belirteci '-FullUri' parametresiyle oluşturulduğunda, döndürülen Uri anlık görüntü Uri'si olacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6e189-357">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="6e189-358">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="6e189-358">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6e189-359">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6e189-359">Az.Websites</span></span>
* <span data-ttu-id="6e189-360">'Get-AzDeletedWebApp' cmdlet'indeki tarih ayrıştırma hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6e189-360">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="6e189-361">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="6e189-361">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="6e189-362">1.0.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="6e189-362">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="6e189-363">Genel</span><span class="sxs-lookup"><span data-stu-id="6e189-363">General</span></span>

- <span data-ttu-id="6e189-364">Az Modülü Genel Kullanıma Sunuldu</span><span class="sxs-lookup"><span data-stu-id="6e189-364">General Availability of Az Module</span></span>
- <span data-ttu-id="6e189-365">Her modül için çevrimiçi yardım</span><span class="sxs-lookup"><span data-stu-id="6e189-365">Online help for each module</span></span>
- <span data-ttu-id="6e189-366">Diğer ayrıntılar ve yol haritası için bkz. [Az Duyuru Sayfası](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="6e189-366">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="6e189-367">AzureRM’den geçiş hakkında bilgi edinmek için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="6e189-367">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="6e189-368">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6e189-368">Az.Accounts</span></span>
- <span data-ttu-id="6e189-369">Önceki adı: Az.Profile</span><span class="sxs-lookup"><span data-stu-id="6e189-369">Changed from Az.Profile</span></span>
- <span data-ttu-id="6e189-370">Profil ve bağlam türleri için tablo biçimleri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6e189-370">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="6e189-371">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6e189-371">Az.ApiManagement</span></span>
- <span data-ttu-id="6e189-372">#7002 düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="6e189-372">Fixes for #7002</span></span>
- <span data-ttu-id="6e189-373">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="6e189-373">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="6e189-374">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="6e189-374">Az.Batch</span></span>
- <span data-ttu-id="6e189-375">`PSComputeNode` üzerinde yeni `NodeAgentInformation` aracılığıyla bir havuzdaki her bir VM’de Azure Batch Düğüm Aracısı’nın hangi sürümünün çalıştığını görme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="6e189-375">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="6e189-376">`PSDataDisk` için `Caching` varsayılan ayarı artık `None` yerine `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="6e189-376">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="6e189-377">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="6e189-377">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="6e189-378">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="6e189-378">Az.Billing</span></span>
- <span data-ttu-id="6e189-379">Billing, Consumption ve UsageAggregates cmdlet’lerini birleştirir, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="6e189-379">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="6e189-380">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="6e189-380">Az.CognitivServices</span></span>
- <span data-ttu-id="6e189-381">New-AzureRmCognitiveServicesAccount işleminde kullanılabilen SkuName ve Typem için tamamlayıcılar eklendi</span><span class="sxs-lookup"><span data-stu-id="6e189-381">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="6e189-382">Get-AzCognitiveServicesAccountSkus cmdlet’inden GetSkusWithAccountParamSetName parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="6e189-382">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="6e189-383">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="6e189-383">Az.ContainerInstance</span></span>
- <span data-ttu-id="6e189-384">ManagedIdentity desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="6e189-384">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="6e189-385">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="6e189-385">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="6e189-386">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="6e189-386">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="6e189-387">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6e189-387">Az.DataLakeStore</span></span>
- <span data-ttu-id="6e189-388">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="6e189-388">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="6e189-389">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6e189-389">Az.Monitor</span></span>
- <span data-ttu-id="6e189-390">Az.Insights cmdlet’inin adı Az.Monitor olarak değiştirildi ve başka yeni değişiklikler yapıldı, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="6e189-390">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="6e189-391">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6e189-391">Az.KeyVault</span></span>
- <span data-ttu-id="6e189-392">Çıkış türlerinden kullanım dışı 'PurgeDisabled' özelliği kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="6e189-392">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="6e189-393">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="6e189-393">Az.MachineLearning</span></span>
- <span data-ttu-id="6e189-394">Az.MachineLearningCompute modülünden cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="6e189-394">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="6e189-395">Az.Media</span><span class="sxs-lookup"><span data-stu-id="6e189-395">Az.Media</span></span>
- <span data-ttu-id="6e189-396">New-AzMediaService cmdlet’inden kullanım dışı -Tags diğer adı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="6e189-396">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="6e189-397">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6e189-397">Az.Network</span></span>
<span data-ttu-id="6e189-398">Application Gateway’de RewriteRuleSets parametresini yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="6e189-398">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="6e189-399">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="6e189-399">New cmdlets added:</span></span>
        - <span data-ttu-id="6e189-400">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6e189-400">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6e189-401">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6e189-401">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6e189-402">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6e189-402">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6e189-403">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6e189-403">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6e189-404">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6e189-404">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6e189-405">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="6e189-405">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="6e189-406">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="6e189-406">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="6e189-407">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="6e189-407">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="6e189-408">Cmdlet’ler isteğe bağlı -RewriteRuleSet parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6e189-408">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="6e189-409">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6e189-409">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="6e189-410">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6e189-410">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="6e189-411">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6e189-411">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="6e189-412">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6e189-412">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="6e189-413">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="6e189-413">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="6e189-414">New-AzureRmApplicationGatewayUrlPathMapConfig, Kimlik kullanarak Application Gateway’e KeyVault Desteği ekledi.</span><span class="sxs-lookup"><span data-stu-id="6e189-414">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="6e189-415">Cmdlet’ler isteğe bağlı -KeyVaultSecretId, -KeyVaultSecret parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6e189-415">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="6e189-416">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6e189-416">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="6e189-417">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6e189-417">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="6e189-418">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6e189-418">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="6e189-419">New-AzApplicationGateway cmdlet’i isteğe bağlı -UserAssignedIdentity parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6e189-419">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="6e189-420">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="6e189-420">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="6e189-421">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6e189-421">Az.OperationalInsights</span></span>
- <span data-ttu-id="6e189-422">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="6e189-422">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="6e189-423">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="6e189-423">Az.Profile</span></span>
- <span data-ttu-id="6e189-424">Modül adı Az.Accounts olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="6e189-424">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="6e189-425">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6e189-425">Az.RecoveryServices</span></span>
- <span data-ttu-id="6e189-426">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="6e189-426">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="6e189-427">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6e189-427">Az.Resources</span></span>
- <span data-ttu-id="6e189-428">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="6e189-428">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="6e189-429">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6e189-429">Az.ServiceFabric</span></span>
- <span data-ttu-id="6e189-430">Sertifikayı ortak ad ve parmak iziyle belirtme desteği</span><span class="sxs-lookup"><span data-stu-id="6e189-430">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="6e189-431">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="6e189-431">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="6e189-432">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="6e189-432">Az.SIgnalR</span></span>
- <span data-ttu-id="6e189-433">SIgnalR için PowerShell cmdlet'leri Genel Kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="6e189-433">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="6e189-434">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6e189-434">Az.Sql</span></span>
- <span data-ttu-id="6e189-435">Tehdit Algılama cmdlet’lerine yeni Data_Exfiltration ve Unsafe_Action algılama türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="6e189-435">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="6e189-436">Sql Denetimi cmdlet'leri için belge örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6e189-436">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="6e189-437">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="6e189-437">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="6e189-438">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6e189-438">Az.Storage</span></span>
- <span data-ttu-id="6e189-439">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="6e189-439">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="6e189-440">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6e189-440">Az.Websites</span></span>
- <span data-ttu-id="6e189-441">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="6e189-441">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="6e189-442">0.7.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="6e189-442">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="6e189-443">Genel</span><span class="sxs-lookup"><span data-stu-id="6e189-443">General</span></span>

* <span data-ttu-id="6e189-444">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="6e189-444">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="6e189-445">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6e189-445">Az.Compute</span></span>

* <span data-ttu-id="6e189-446">`New-AzVm(ss)` cmdlet’leri için basit parametre kümelerinde UltraSSD ve Galeri Görüntüleri desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="6e189-446">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="6e189-447">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6e189-447">Az.DataLakeStore</span></span>

* <span data-ttu-id="6e189-448">Adls hesabı etki alanının sonundaki eğik çizgi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6e189-448">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="6e189-449">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6e189-449">Az.FrontDoor</span></span>

* <span data-ttu-id="6e189-450">Bazı bozuk bağlantılar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6e189-450">Fixed some broken links</span></span>
    - <span data-ttu-id="6e189-451">New-AzureRmFrontDoor ve Set-AzureRmFrontDoor makalelerinde, New-AzureRmFrontDoorHealthProbeSettingObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="6e189-451">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="6e189-452">New-AzureRmFrontDoorManagedRuleObject makalesinde, New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="6e189-452">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="6e189-453">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6e189-453">Az.RecoveryServices</span></span>

* <span data-ttu-id="6e189-454">Azure Dosya Paylaşımı geri yükleme işlemleri için istemci tarafı doğrulamalar eklendi.</span><span class="sxs-lookup"><span data-stu-id="6e189-454">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="6e189-455">Afs geri yükleme işlemi için storageAccountName ve storageAccountResourceGroupName isteğe bağlı hale getirildi.</span><span class="sxs-lookup"><span data-stu-id="6e189-455">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="6e189-456">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6e189-456">Az.Resources</span></span>

* <span data-ttu-id="6e189-457">[https://github.com/Azure/azure-powershell/issues/7402](https://github.com/Azure/azure-powershell/issues/7679) düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="6e189-457">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="6e189-458">Get-AzureRmRoleAssignment, klasik yöneticiler istenirken sağlanmışsa abonelik kapsamını kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="6e189-458">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="6e189-459">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6e189-459">Az.Sql</span></span>

* <span data-ttu-id="6e189-460">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="6e189-460">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="6e189-461">Get-AzureRmSqlDatabaseVulnerabilityAssessment cmdlet’inin DotNet core ile kullanılması konusundaki bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6e189-461">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="6e189-462">SQL Denetimi cmdlet’leriyle ilgili yardım iletilerinin belgeleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="6e189-462">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="6e189-463">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6e189-463">Az.Storage</span></span>

* <span data-ttu-id="6e189-464">New-AzureRmStorageAccount cmdlet’ine -EnableHierarchicalNamespace eklendi</span><span class="sxs-lookup"><span data-stu-id="6e189-464">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="6e189-465">-DestContext girilmediğinde Dosya Kopyalama cmdlet’inin hedefte kaynak bağlamını yeniden kullanamamasına yol açan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6e189-465">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="6e189-466">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="6e189-466">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="6e189-467">Statik Web Sitesi yapılandırması için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="6e189-467">Support Static Website configuration</span></span>
    - <span data-ttu-id="6e189-468">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="6e189-468">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="6e189-469">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="6e189-469">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="6e189-470">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6e189-470">Az.Websites</span></span>

* <span data-ttu-id="6e189-471">Set-AzureRmWebApp ve Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6e189-471">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="6e189-472">Windows ve Linux kapsayıcı uygulamalarında bağlanacak Azure Depolama yollarının belirtilmesi için yeni parametre (-AzureStoragePath) eklendi.</span><span class="sxs-lookup"><span data-stu-id="6e189-472">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="6e189-473">Azure Depolama yollarını ayarlamak için yeni New-AzureRmWebAppAzureStoragePath cmdlet’inin çıktısını bir parametre olarak kullanın.</span><span class="sxs-lookup"><span data-stu-id="6e189-473">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="6e189-474">0.6.1 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="6e189-474">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="6e189-475">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6e189-475">Az.ApiManagement</span></span>
* <span data-ttu-id="6e189-476">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="6e189-476">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="6e189-477">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6e189-477">Az.Automation</span></span>
* <span data-ttu-id="6e189-478">Swagger tabanlı Azure Otomasyon cmdlet'leri</span><span class="sxs-lookup"><span data-stu-id="6e189-478">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="6e189-479">Güncelleştirme Yönetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="6e189-479">Added Update Management cmdlets</span></span>
* <span data-ttu-id="6e189-480">Kaynak Denetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="6e189-480">Added Source Control cmdlets</span></span>
* <span data-ttu-id="6e189-481">Remove-AzureRmAutomationHybridWorkerGroup cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="6e189-481">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="6e189-482">DSC Kayıt Düğümü komutu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6e189-482">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="6e189-483">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6e189-483">Az.Compute</span></span>
* <span data-ttu-id="6e189-484">SystemAssigned kimliği için kimlik sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6e189-484">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="6e189-485">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="6e189-485">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="6e189-486">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="6e189-486">Az.ContainerInstance</span></span>
* <span data-ttu-id="6e189-487">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="6e189-487">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="6e189-488">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="6e189-488">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="6e189-489">Market cmdlet'leri için örnekler açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6e189-489">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="6e189-490">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6e189-490">Az.Network</span></span>
* <span data-ttu-id="6e189-491">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="6e189-491">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="6e189-492">Desteklenen AzureFirewall Ağ Protokollerine yeniden ICMP eklendi</span><span class="sxs-lookup"><span data-stu-id="6e189-492">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="6e189-493">Test-AzureRmNetworkWatcherConnectivity cmdlet'i güncelleştirildi; hedef kimlik, adres ve bağlantı noktasında doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="6e189-493">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="6e189-494">VirtualNetwork eşlemesinde bellek kullanımıyla ilgili sorunlar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6e189-494">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="6e189-495">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="6e189-495">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="6e189-496">Korumalı dosya paylaşımı için ilke değiştirme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="6e189-496">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="6e189-497">İlke saat dilimi büyük harfe dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="6e189-497">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="6e189-498">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="6e189-498">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="6e189-499">New-AzureRmRecoveryServicesAsrProtectableItem cmdlet'indeki örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6e189-499">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="6e189-500">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="6e189-500">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="6e189-501">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="6e189-501">Az.Relay</span></span>
* <span data-ttu-id="6e189-502">Kullanıcının New-AzureRmRelayKey cmdlet'ine KeyValue sağlamasına olanak tanıyan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="6e189-502">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="6e189-503">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6e189-503">Az.Resources</span></span>
* <span data-ttu-id="6e189-504">`New-AzureRmPolicyAssignment` ve `Set-AzureRmPolicyAssignment` cmdlet'lerindeki kaynak kimliğiyle ilgili parametrelerin yardım belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6e189-504">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="6e189-505">New-AzureRmPolicyDefinition cmdlet'ine -Metadata kullanan bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="6e189-505">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="6e189-506">NetStandard'da Tag anahtarında büyük/küçük harf kullanımının korunmasına yönelik düzeltme yapıldı: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="6e189-506">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="6e189-507">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6e189-507">Az.ServiceFabric</span></span>
* <span data-ttu-id="6e189-508">Hataya neden olan değişiklikler yayınlanacağından kullanımdan kaldırılacak özellikleri belirten iletiler eklendi</span><span class="sxs-lookup"><span data-stu-id="6e189-508">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="6e189-509">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6e189-509">Az.Sql</span></span>
* <span data-ttu-id="6e189-510">Azure Sql Veritabanı Yönetilen Örneği ve Azure Sql Yönetilen Veritabanı'nındaki CRUD işlemleri için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="6e189-510">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="6e189-511">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="6e189-511">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="6e189-512">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="6e189-512">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="6e189-513">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="6e189-513">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="6e189-514">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="6e189-514">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="6e189-515">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="6e189-515">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="6e189-516">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="6e189-516">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="6e189-517">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="6e189-517">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="6e189-518">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="6e189-518">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="6e189-519">Sunucuda veya veritabanında Genişletilmiş Denetim İlkesi yönetimi etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="6e189-519">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="6e189-520">Denetim günlüklerinde filtrelemeyi etkinleştirmek için yeni parametre (PredicateExpression) eklendi.</span><span class="sxs-lookup"><span data-stu-id="6e189-520">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="6e189-521">Cmdlet'ler, SQL istemcileri yerine Eski istemcileri kullanacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="6e189-521">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="6e189-522">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="6e189-522">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="6e189-523">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="6e189-523">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="6e189-524">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="6e189-524">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="6e189-525">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="6e189-525">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="6e189-526">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings cmdlet'inin depolama hesabı ad parametre kümesiyle kullanılmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6e189-526">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="6e189-527">0.5.0 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="6e189-527">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="6e189-528">Genel</span><span class="sxs-lookup"><span data-stu-id="6e189-528">General</span></span>
* <span data-ttu-id="6e189-529">Birçok temel cmdlet’e Kaynak Tamamlayıcıları eklendi - bunlar cmdlet’leri etkileşimli olarak çağırırken mevcut kaynak adları arasında gezinmenize olanak tanır</span><span class="sxs-lookup"><span data-stu-id="6e189-529">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="6e189-530">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="6e189-530">Az.Profile</span></span>
* <span data-ttu-id="6e189-531">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6e189-531">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="6e189-532">Connect-AzAccount cmdlet'indeki TenantId parametresi Tenant olarak yeniden adlandırıldı ve TenantId için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="6e189-532">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="6e189-533">Connect-AzAccount için TenantId açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6e189-533">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="6e189-534">Kiracı etki alanı sağlanırken başarısız oturum açma durumunda gösterilen hata iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6e189-534">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="6e189-535">Kiracıda abonelikleri olmayan hesaplar için bağlam adı çakışmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6e189-535">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="6e189-536">MSI kullanırken DataLake uç noktalarıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6e189-536">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="6e189-537">Bağlantı olmadığında 'Disconnect-AzAccount' oluşturulmasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6e189-537">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="6e189-538">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6e189-538">Az.CognitiveServices</span></span>
* <span data-ttu-id="6e189-539">Get-AzCognitiveServicesAccountSkus işlemi eklendi.</span><span class="sxs-lookup"><span data-stu-id="6e189-539">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6e189-540">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6e189-540">Az.Compute</span></span>
* <span data-ttu-id="6e189-541">Add-AzVmssVMDataDisk ve Remove-AzVmssVMDataDisk cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="6e189-541">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="6e189-542">Get-AzVMImage, AutomaticOSUpgradeProperties gösteriyor</span><span class="sxs-lookup"><span data-stu-id="6e189-542">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="6e189-543">SetAzVMChefExtension -BootstrapOptions ve -JsonAttribute seçeneği değerlerinin Json biçiminde ayarlanmamasıyla ilgili hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="6e189-543">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6e189-544">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6e189-544">Az.DataLakeStore</span></span>
* <span data-ttu-id="6e189-545">DataLake paketi 1.1.10'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="6e189-545">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="6e189-546">Çok iş parçacıklı işlemlere varsayılan Concurrency değeri eklendi.</span><span class="sxs-lookup"><span data-stu-id="6e189-546">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="6e189-547">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="6e189-547">Az.Insights</span></span>
* <span data-ttu-id="6e189-548">7267 numaralı (Otomatik ölçeklendirme alanı) sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6e189-548">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="6e189-549">Yeni otomatik ölçeklendirme kuralı oluşturma sırasında numaralandırılmış parametrelerin düzgün ayarlanmamasıyla ilgili sorunlar (bunlar her zaman varsayılan değere ayarlanıyordu).</span><span class="sxs-lookup"><span data-stu-id="6e189-549">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="6e189-550">Set-AzDiagnosticSetting'in ayar oluşturma sırasında kategorilerin açıkça belirtilmesini gerektirmesiyle ilgili 7513 numaralı [Insights] sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6e189-550">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="6e189-551">Artık cmdlet oluşturma sırasında açık kategori gösteriminin etkinleştirilmesini gerektirmiyor; başka bir deyişle belgelerinde belirtildiği gibi çalışıyor</span><span class="sxs-lookup"><span data-stu-id="6e189-551">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6e189-552">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6e189-552">Az.Network</span></span>
* <span data-ttu-id="6e189-553">Aşağıdaki parametrelerde PeeringType parametresi zorunlu parametre olarak değiştirildi:-</span><span class="sxs-lookup"><span data-stu-id="6e189-553">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="6e189-554">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="6e189-554">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="6e189-555">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="6e189-555">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="6e189-556">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="6e189-556">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="6e189-557">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="6e189-557">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="6e189-558">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="6e189-558">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="6e189-559">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="6e189-559">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="6e189-560">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6e189-560">Az.PolicyInsights</span></span>
* <span data-ttu-id="6e189-561">İlke düzeltme cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="6e189-561">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="6e189-562">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6e189-562">Az.Resources</span></span>
* <span data-ttu-id="6e189-563">[https://github.com/Azure/azure-powershell/issues/7402](https://github.com/Azure/azure-powershell/issues/7402) düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="6e189-563">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="6e189-564">'Get-AzResource' için '-ResourceId' parametresi kullanılarak kaynakların listelenmesine olanak tanındı</span><span class="sxs-lookup"><span data-stu-id="6e189-564">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="6e189-565">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6e189-565">Az.ServiceBus</span></span>
* <span data-ttu-id="6e189-566">PSServiceBusMigrationConfigurationAttributes'e Geçiş durumunun bilinmesine yardımcı olacak salt okunur MigrationState özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="6e189-566">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6e189-567">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6e189-567">Az.ServiceFabric</span></span>
* <span data-ttu-id="6e189-568">Linux Vmss'ye sertifika ekleme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="6e189-568">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="6e189-569">'Add-AzServiceFabricClusterCertificate' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6e189-569">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="6e189-570">Yeni sertifikadan doğru parmak izi kullanıyor (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="6e189-570">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="6e189-571">Özel durum doğru görüntüleniyor (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="6e189-571">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="6e189-572">'Update-AzServiceFabricDurability', Vmss CreateOrUpdate işlemini başlatmadan önce küme yapılandırmasını güncelleştirecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="6e189-572">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="6e189-573">0.4.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="6e189-573">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="6e189-574">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="6e189-574">Az.Profile</span></span>
* <span data-ttu-id="6e189-575">CloudShell’de Get-AzSubscription sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="6e189-575">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="6e189-576">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6e189-576">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6e189-577">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6e189-577">Az.Compute</span></span>
* <span data-ttu-id="6e189-578">'New-AzVm' için basit parametre kümesi kullanıldığında hızlandırılmış ağların açılacağı VM boyutları beyaz listesine yeni boyutlar eklendi</span><span class="sxs-lookup"><span data-stu-id="6e189-578">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="6e189-579">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="6e189-579">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6e189-580">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6e189-580">Az.DataLakeStore</span></span>
* <span data-ttu-id="6e189-581">Sanal Ağ Kuralları desteği ekleme</span><span class="sxs-lookup"><span data-stu-id="6e189-581">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="6e189-582">Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store sanal ağ kuralını alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="6e189-582">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="6e189-583">Add-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabına sanal ağ kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="6e189-583">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="6e189-584">Set-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabındaki belirtilen sanal ağ kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="6e189-584">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="6e189-585">Remove-AzDataLakeStoreVirtualNetworkRule: Bir Azure Data Lake Store sanal ağ kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="6e189-585">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6e189-586">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6e189-586">Az.Network</span></span>
* <span data-ttu-id="6e189-587">Test-AzNetworkWatcherConnectivity cmdlet'i güncelleştirildi, arka uca protokol değerini geçiriyor.</span><span class="sxs-lookup"><span data-stu-id="6e189-587">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="6e189-588">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="6e189-588">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6e189-589">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6e189-589">Az.Resources</span></span>
* <span data-ttu-id="6e189-590">Get-AzRoleDefinition cmdlet'inin anlaşılmaz bir özel durum oluşturmasına neden olan hata (varsayılan profilin içinde abonelik olmadığında ve hiçbir kapsam belirtilmediğinde), senaryoya anlamlı bir özel durum eklenerek düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="6e189-590">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="6e189-591">Ayrıca varsayılan parametre kümesi 'RoleDefinitionNameParameterSet' olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="6e189-591">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="6e189-592">0.3.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="6e189-592">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="6e189-593">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="6e189-593">Azure.Storage</span></span>
* <span data-ttu-id="6e189-594">Hedefte meta veri sorunu olduğunda Fix Copy Blob/File meta verileri kopyalamayacak</span><span class="sxs-lookup"><span data-stu-id="6e189-594">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="6e189-595">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="6e189-595">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="6e189-596">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="6e189-596">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="6e189-597">Belirli bir konumunun Depolama kaynağı kullanımını alma desteği ve genel Depolama kayrağı kullanımını almak için uyarı iletisi ekleme kullanımdan kalktı.</span><span class="sxs-lookup"><span data-stu-id="6e189-597">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="6e189-598">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="6e189-598">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="6e189-599">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6e189-599">Az.CognitiveServices</span></span>
* <span data-ttu-id="6e189-600">Mevcut hesap olmadan Get-AzCognitiveServicesAccountSkus desteği.</span><span class="sxs-lookup"><span data-stu-id="6e189-600">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6e189-601">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6e189-601">Az.Compute</span></span>
* <span data-ttu-id="6e189-602">Get-AzVM -ResourceGroupName <rg> gerektiğinde 50'den fazla sonuç döndürecek şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6e189-602">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="6e189-603">New-AzVmss cmdlet'inin yardımına 'SimpleParameterSet' örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="6e189-603">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="6e189-604">Azure Disk Şifrelemesi ilerleme durumu iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6e189-604">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="6e189-605">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="6e189-605">Az.DataFactoryV2</span></span>
* <span data-ttu-id="6e189-606">ADF .Net SDK sürümü 2.3.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="6e189-606">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6e189-607">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6e189-607">Az.Network</span></span>
* <span data-ttu-id="6e189-608">NetworkProfile işlevselliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="6e189-608">Added NetworkProfile functionality.</span></span> <span data-ttu-id="6e189-609">yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="6e189-609">new cmdlets added</span></span>
    - <span data-ttu-id="6e189-610">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6e189-610">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="6e189-611">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6e189-611">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="6e189-612">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6e189-612">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="6e189-613">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6e189-613">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="6e189-614">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="6e189-614">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="6e189-615">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="6e189-615">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="6e189-616">Alt Ağ Modeline hizmet ilişki bağlantısı eklendi</span><span class="sxs-lookup"><span data-stu-id="6e189-616">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="6e189-617">New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="6e189-617">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="6e189-618">Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="6e189-618">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="6e189-619">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="6e189-619">Az.RedisCache</span></span>
* <span data-ttu-id="6e189-620">Bundan sonra Size parametresi olarak her dizeye izin veriliyor.</span><span class="sxs-lookup"><span data-stu-id="6e189-620">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="6e189-621">PSArgumentCompleter açılan listesine P5 eklendi</span><span class="sxs-lookup"><span data-stu-id="6e189-621">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="6e189-622">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6e189-622">Az.Resources</span></span>
* <span data-ttu-id="6e189-623">Set-AzPolicyDefinition'a eksik -Mode parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="6e189-623">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="6e189-624">Origin öğesi User içeren işlemler için Get-AzProviderOperation commandlet hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6e189-624">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="6e189-625">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6e189-625">Az.Sql</span></span>
* <span data-ttu-id="6e189-626">Bazı yedekleme cmdlet'lerinin geçerli Azure aboneliğini tanıyamamasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6e189-626">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6e189-627">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6e189-627">Az.Websites</span></span>
* <span data-ttu-id="6e189-628">Yeni Get-AzWebAppContainerContinuousDeploymentUrl Cmdlet'i - Kapsayıcı Sürekli Dağıtım Web Kancası URL'sini alıyor</span><span class="sxs-lookup"><span data-stu-id="6e189-628">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="6e189-629">Yeni New-AzWebAppContainerPSSession ve Enter-WebAppContainerPSSession Cmdlet'leri - Windows kapsayıcı uygulamasında PowerShell uzak oturumunu başlatıyor</span><span class="sxs-lookup"><span data-stu-id="6e189-629">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="6e189-630">0.2.0 - Eylül 2018</span><span class="sxs-lookup"><span data-stu-id="6e189-630">0.2.0 - September 2018</span></span>
 <span data-ttu-id="6e189-631">İlk Yayın</span><span class="sxs-lookup"><span data-stu-id="6e189-631">Initial Release</span></span>