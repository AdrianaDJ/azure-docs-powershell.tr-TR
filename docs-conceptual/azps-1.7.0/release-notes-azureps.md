---
ms.openlocfilehash: 54d7a9da878e085e90479fb229876c9be6dafd74
ms.sourcegitcommit: 89066b7c4b527357bb2024e1ad708df84c131804
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59364241"
---
## <a name="170---april-2019"></a><span data-ttu-id="a7d1d-101">1.7.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="a7d1d-101">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="a7d1d-102">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="a7d1d-102">Highlights since the last major release</span></span>
* <span data-ttu-id="a7d1d-103">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="a7d1d-103">General availability of `Az` module</span></span>
* <span data-ttu-id="a7d1d-104">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="a7d1d-104">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="a7d1d-105">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="a7d1d-105">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="a7d1d-106">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-106">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="a7d1d-107">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-107">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="a7d1d-108">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-108">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="a7d1d-109">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="a7d1d-109">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a7d1d-110">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a7d1d-110">Az.Accounts</span></span>
* <span data-ttu-id="a7d1d-111">Add-AzEnvironment ve Set-AzEnvironment, AzureAnalysisServicesEndpointResourceId parametresini kabul edecek biçimde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-111">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="a7d1d-112">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a7d1d-112">Az.AnalysisServices</span></span>
* <span data-ttu-id="a7d1d-113">Veri düzlemi cmdlet’lerinde ServiceClient kullanma ve orijinal kimlik doğrulaması mantığını kaldırma</span><span class="sxs-lookup"><span data-stu-id="a7d1d-113">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="a7d1d-114">Hataya neden olan değişikliklerden kaçınmak için Add-AzureASAccount’ı Connect-AzAccount’ın sarmalayıcısı yapma</span><span class="sxs-lookup"><span data-stu-id="a7d1d-114">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a7d1d-115">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a7d1d-115">Az.Automation</span></span>
* <span data-ttu-id="a7d1d-116">Eklemeler için New-AzAutomationSoftwareUpdateConfiguration cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-116">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="a7d1d-117">IncludedKbNumber ve IncludedPackageNameMask parametrelerinin artık çalışması bekleniyor.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-117">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="a7d1d-118">Azure otomasyonu güncelleştirmesi yönetim dinamik grubu için hata düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-118">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a7d1d-119">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a7d1d-119">Az.Compute</span></span>
* <span data-ttu-id="a7d1d-120">New-AzDiskConfig ve New-AzSnapshotConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-120">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="a7d1d-121">Diğer kiracıların karakter görüntüleriyle VM oluşturmaya izin verildi.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-121">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="a7d1d-122">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="a7d1d-122">Az.ContainerInstance</span></span>
* <span data-ttu-id="a7d1d-123">New-AzContainerGroup’un -command parametresinde bağımsız boş değişken ekleyen sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-123">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a7d1d-124">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a7d1d-124">Az.DataFactory</span></span>
* <span data-ttu-id="a7d1d-125">ADF .Net SDK’sı 3.0.2 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-125">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="a7d1d-126">Set-AzDataFactoryV2 cmdlet’i RepoConfiguration ile ilgili ayarların ek parametreleriyle güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-126">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a7d1d-127">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a7d1d-127">Az.Resources</span></span>
* <span data-ttu-id="a7d1d-128">'-ResourceId' veya '-ResourceGroupName', '-Name' ve '-ResourceType' parametreleri sağlanırken ‘Get-AzResource’ için sağlayıcıların işlenmesi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-128">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="a7d1d-129">‘Test-AzDeployment’ ve ‘Test-AzResourceGroupDeployment’ için hata işleme geliştirildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-129">Improve error handling for for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="a7d1d-130">İşleme hataları dağıtım doğrulamasının dışında tutuldu ve komut çıkışına dahil edildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-130">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="a7d1d-131">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="a7d1d-131">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="a7d1d-132">Betik ve iş senaryolarında istemi atlamak için bir dizi dağıtım cmdlet’lerine ‘-IgnoreDynamicParameters’ anahtar parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-132">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="a7d1d-133">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="a7d1d-133">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="a7d1d-134">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a7d1d-134">Az.Sql</span></span>
* <span data-ttu-id="a7d1d-135">Veritabanı Verileri Sınıflandırması Desteği.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-135">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a7d1d-136">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a7d1d-136">Az.Storage</span></span>
* <span data-ttu-id="a7d1d-137">-UseConnectedAccount parametresi ile depolama bağlamı oluştururken ayrıntı hatası raporlama</span><span class="sxs-lookup"><span data-stu-id="a7d1d-137">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="a7d1d-138">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="a7d1d-138">New-AzStorageContext</span></span>
* <span data-ttu-id="a7d1d-139">Belirtilen depolama hesabının Yönetim düzlemi API’si ile Blob Hizmeti Özellikleri için Yönetim Desteği</span><span class="sxs-lookup"><span data-stu-id="a7d1d-139">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="a7d1d-140">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="a7d1d-140">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="a7d1d-141">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="a7d1d-141">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="a7d1d-142">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="a7d1d-142">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="a7d1d-143">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="a7d1d-143">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="a7d1d-144">Blob ve dosya karşıya yükleme ve indirme cmdlet’leri için -Asjob desteği</span><span class="sxs-lookup"><span data-stu-id="a7d1d-144">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="a7d1d-145">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a7d1d-145">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="a7d1d-146">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a7d1d-146">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="a7d1d-147">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="a7d1d-147">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="a7d1d-148">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="a7d1d-148">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="a7d1d-149">1.6.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="a7d1d-149">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="a7d1d-150">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="a7d1d-150">Highlights since the last major release</span></span>
* <span data-ttu-id="a7d1d-151">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="a7d1d-151">General availability of `Az` module</span></span>
* <span data-ttu-id="a7d1d-152">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="a7d1d-152">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="a7d1d-153">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="a7d1d-153">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="a7d1d-154">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-154">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="a7d1d-155">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-155">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="a7d1d-156">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-156">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="a7d1d-157">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="a7d1d-157">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a7d1d-158">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a7d1d-158">Az.Automation</span></span>
* <span data-ttu-id="a7d1d-159">Aşağıdaki yeni özellikleri desteklemek için Azure otomasyonu güncelleştirme yönetimi değişikliği:</span><span class="sxs-lookup"><span data-stu-id="a7d1d-159">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="a7d1d-160">Dinamik gruplandırma</span><span class="sxs-lookup"><span data-stu-id="a7d1d-160">Dynamic grouping</span></span>
    * <span data-ttu-id="a7d1d-161">Ön-Son betik</span><span class="sxs-lookup"><span data-stu-id="a7d1d-161">Pre-Post script</span></span>
    * <span data-ttu-id="a7d1d-162">Yeniden Başlatma Ayarı</span><span class="sxs-lookup"><span data-stu-id="a7d1d-162">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a7d1d-163">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a7d1d-163">Az.Compute</span></span>
* <span data-ttu-id="a7d1d-164">Get-AzVmBootDiagnosticsData içinde yol çözümleme sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="a7d1d-164">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="a7d1d-165">İşlem istemci kitaplığı 25.0.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-165">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a7d1d-166">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a7d1d-166">Az.KeyVault</span></span>
* <span data-ttu-id="a7d1d-167">KeyVault cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-167">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a7d1d-168">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a7d1d-168">Az.Network</span></span>
* <span data-ttu-id="a7d1d-169">Azure Güvenlik Duvarı için Tehdit Bilgileri desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-169">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="a7d1d-170">Application Gateway Güvenlik Duvarı İlkesi üst düzey kaynağı ve Özel Kurallar eklendi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-170">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a7d1d-171">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a7d1d-171">Az.RecoveryServices</span></span>
* <span data-ttu-id="a7d1d-172">Anında RP desteği için Azure VM ilkesine SnapshotRetentionInDays eklendi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-172">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="a7d1d-173">Kapsayıcı kaydını kaldırmak için kanal desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-173">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="a7d1d-174">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a7d1d-174">Az.Resources</span></span>
* <span data-ttu-id="a7d1d-175">Get-AzResource ve Get-AzResourceGroup için joker karakter desteği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-175">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="a7d1d-176">ARM'ye genel çağrı yapılırken kullanılan kimlik bilgileri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-176">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="a7d1d-177">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a7d1d-177">Az.Sql</span></span>
* <span data-ttu-id="a7d1d-178">Yeni DetectionType'lar eklendiğinde gelecekte kullanılabilmesini sağlamak ve otomatik tamamlamayı da desteklemek için Tehdit Algılama cmdlet'lerinin DetectionType olan parametresi (ExcludeDetectionType) string[] olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-178">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a7d1d-179">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a7d1d-179">Az.Storage</span></span>
* <span data-ttu-id="a7d1d-180">Depolama hesabında Yönetim İlkesini Alma/Ayarlama/Kaldırma desteği</span><span class="sxs-lookup"><span data-stu-id="a7d1d-180">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="a7d1d-181">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="a7d1d-181">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="a7d1d-182">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="a7d1d-182">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="a7d1d-183">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="a7d1d-183">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="a7d1d-184">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="a7d1d-184">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="a7d1d-185">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="a7d1d-185">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="a7d1d-186">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="a7d1d-186">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a7d1d-187">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a7d1d-187">Az.Websites</span></span>
* <span data-ttu-id="a7d1d-188">'New-AzWebApp -IncludeSourceWebAppSlots' kullanarak tüm yuvaların kopyalanmasını kesintiye uğratan ARM şablon hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-188">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="a7d1d-189">1.5.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="a7d1d-189">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a7d1d-190">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a7d1d-190">Az.Accounts</span></span>
* <span data-ttu-id="a7d1d-191">AutoRest tarafından oluşturulan cmdlet’leri desteklemek için 'Register-AzModule' komutu eklendi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-191">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="a7d1d-192">Connect-AzAccount örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-192">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a7d1d-193">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a7d1d-193">Az.Automation</span></span>
* <span data-ttu-id="a7d1d-194">Birden fazla Azure Otomasyonu cmdlet’inde belirli aylık zamanlamalar alınırken yaşanan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-194">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="a7d1d-195">Yalnızca ilk 20 düğümü döndüren Get-AzAutomationDscNode düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-195">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="a7d1d-196">Artık tüm düğümleri döndürür</span><span class="sxs-lookup"><span data-stu-id="a7d1d-196">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a7d1d-197">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a7d1d-197">Az.Cdn</span></span>
* <span data-ttu-id="a7d1d-198">Özel Etki Alanı Https Etkinleştirmesi/Devre Dışı Bırakması için yeni PowerShell cmdlet’leri eklendi ve eskiler kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="a7d1d-198">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a7d1d-199">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a7d1d-199">Az.Compute</span></span>
* <span data-ttu-id="a7d1d-200">Get cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-200">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a7d1d-201">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a7d1d-201">Az.DataFactory</span></span>
* <span data-ttu-id="a7d1d-202">ADF .Net SDK sürümü 3.0.1'e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-202">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="a7d1d-203">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a7d1d-203">Az.LogicApp</span></span>
* <span data-ttu-id="a7d1d-204">Yalnızca ilk sonuç sayfasını getiren ListWorkflows için düzeltme</span><span class="sxs-lookup"><span data-stu-id="a7d1d-204">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a7d1d-205">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a7d1d-205">Az.Network</span></span>
* <span data-ttu-id="a7d1d-206">Network cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-206">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a7d1d-207">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a7d1d-207">Az.RecoveryServices</span></span>
* <span data-ttu-id="a7d1d-208">Azure VM desteğine SQL Server eklendi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-208">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="a7d1d-209">SDK Güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-209">SDK Update</span></span>
* <span data-ttu-id="a7d1d-210">Get-ProtectableItem içindeki Removed VMappContainer denetimi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="a7d1d-210">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="a7d1d-211">Get-ProtectableItem için Name ve ServerName parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-211">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="a7d1d-212">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a7d1d-212">Az.Resources</span></span>
* <span data-ttu-id="a7d1d-213">Dağıtım cmdlet’lerine `-TemplateObject` parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-213">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="a7d1d-214">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="a7d1d-214">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="a7d1d-215">`Get-AzResource` sonucu şuna aktarılırken oluşan sorun düzeltildi:</span><span class="sxs-lookup"><span data-stu-id="a7d1d-215">Fix issue when piping the result of `Get-AzResource` to</span></span> `Set-AzResource`
    - <span data-ttu-id="a7d1d-216">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="a7d1d-216">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="a7d1d-217">Şu çalıştırılırken JSON veri türü değişikliğine neden olan sorun düzeltildi:</span><span class="sxs-lookup"><span data-stu-id="a7d1d-217">Fix issue with JSON data type change when running</span></span> `Set-AzResource`
    - <span data-ttu-id="a7d1d-218">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="a7d1d-218">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="a7d1d-219">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a7d1d-219">Az.Sql</span></span>
* <span data-ttu-id="a7d1d-220">AuditingEndpointsCommunicator güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-220">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="a7d1d-221">Yeni tanılama ayarları oluşturulurken kenar durumunun davranışı düzeltiliyor.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-221">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a7d1d-222">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a7d1d-222">Az.Storage</span></span>
* <span data-ttu-id="a7d1d-223">Depolama hesabı oluşturulurken Support Kind BlockBlobStorage desteği sağlandı      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a7d1d-223">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="a7d1d-224">1.4.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="a7d1d-224">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="a7d1d-225">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a7d1d-225">Az.AnalysisServices</span></span>
* <span data-ttu-id="a7d1d-226">AddAzureASAccount cmdlet'i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="a7d1d-226">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a7d1d-227">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a7d1d-227">Az.Automation</span></span>
* <span data-ttu-id="a7d1d-228">Import-AzAutomationDscNodeConfiguration için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-228">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="a7d1d-229">Import-AzAutomationDscConfiguration cmdlet'ine yapılandırma adı doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-229">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="a7d1d-230">Import-AzAutomationDscConfiguration cmdlet'i için hata işleme iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-230">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a7d1d-231">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a7d1d-231">Az.CognitiveServices</span></span>
* <span data-ttu-id="a7d1d-232">Kaynağın alt etki alanını belirtmek amacıyla kullanılan New-AzCognitiveServicesAccount için CustomSubdomainName adlı, isteğe bağlı, yeni bir parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-232">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a7d1d-233">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a7d1d-233">Az.Compute</span></span>
* <span data-ttu-id="a7d1d-234">Kimlik parametresi kümeleriyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-234">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="a7d1d-235">Get-AzVMExtension, Name parametresi sağlanmadığında yüklü tüm uzantıları listeleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-235">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="a7d1d-236">Update-AzImage cmdlet’ine Tag ve ResourceId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-236">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="a7d1d-237">Get-AzVmssVM, örnek kimliği olmadan ve InstanceView ile, örnek görünümüne sahip VMSS VM’lerini listeleyebilir.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-237">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a7d1d-238">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a7d1d-238">Az.DataLakeStore</span></span>
* <span data-ttu-id="a7d1d-239">ADL silinmiş öğe listeleme ve geri yükleme cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-239">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a7d1d-240">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a7d1d-240">Az.EventHub</span></span>
* <span data-ttu-id="a7d1d-241">EventHub’ın CaptureDescription sınıfında Boş Arşivleri Atlamak için SkipEmptyArchives adlı yeni Boole özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-241">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="a7d1d-242">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a7d1d-242">Az.KeyVault</span></span>
* <span data-ttu-id="a7d1d-243">Set-AzKeyVaultSecret’daki etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-243">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="a7d1d-244">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a7d1d-244">Az.LogicApp</span></span>
* <span data-ttu-id="a7d1d-245">Tümleştirme Hesapları için Temel SKU eklendi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-245">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="a7d1d-246">XSLT 2.0, XSLT 3.0 ve Liquid Eşleşme Türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-246">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="a7d1d-247">Tümleştirme Hesabı Bütünleştirilmiş Kodları için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="a7d1d-247">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="a7d1d-248">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a7d1d-248">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="a7d1d-249">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a7d1d-249">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="a7d1d-250">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a7d1d-250">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="a7d1d-251">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a7d1d-251">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="a7d1d-252">Tümleştirme Hesabı Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="a7d1d-252">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="a7d1d-253">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a7d1d-253">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="a7d1d-254">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a7d1d-254">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="a7d1d-255">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a7d1d-255">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="a7d1d-256">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a7d1d-256">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="a7d1d-257">Logic Apps SDK sürüm 4.1.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-257">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a7d1d-258">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a7d1d-258">Az.Monitor</span></span>
* <span data-ttu-id="a7d1d-259">Get-AzMetric için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-259">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a7d1d-260">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a7d1d-260">Az.Network</span></span>
* <span data-ttu-id="a7d1d-261">Add-AzApplicationGatewayCustomError için yardım örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-261">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a7d1d-262">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a7d1d-262">Az.OperationalInsights</span></span>
* <span data-ttu-id="a7d1d-263">New ve Get ApplicationInsights veri kaynağı için ek destek sunuldu.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-263">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="a7d1d-264">Belirli bir çalışma alanı için belirli ve tüm Get ApplicationInsights veri kaynaklarını desteklemek için yeni ‘ApplicationInsights’ türü eklendi.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-264">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="a7d1d-265">Belirli Application-Insights kaynak parametrelerine (abonelik kimliği, resourceGroupName ve ad) göre veri kaynağı oluşturmak için New-AzOperationalInsightsApplicationInsightsDataSource cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-265">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="a7d1d-266">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a7d1d-266">Az.Resources</span></span>
* <span data-ttu-id="a7d1d-267">https://github.com/Azure/azure-powershell/issues/8166 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-267">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="a7d1d-268">https://github.com/Azure/azure-powershell/issues/8235 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-268">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="a7d1d-269">https://github.com/Azure/azure-powershell/issues/6219 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-269">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="a7d1d-270">KeyCredentials’ın tekrar oluşturmasını engelleyen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-270">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="a7d1d-271">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a7d1d-271">Az.Sql</span></span>
* <span data-ttu-id="a7d1d-272">SQL DB Hiper Ölçeklendirme katmanı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-272">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="a7d1d-273">Geri yükleme isteğinde gereksiz özellikler ayarlandığı için geri yüklemenin başarısız olmasına yol açan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-273">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a7d1d-274">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a7d1d-274">Az.Websites</span></span>
* <span data-ttu-id="a7d1d-275">Get-AzWebAppSlotMetrics örneği düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-275">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="a7d1d-276">1.3.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="a7d1d-276">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a7d1d-277">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a7d1d-277">Az.Accounts</span></span>
* <span data-ttu-id="a7d1d-278">En son ClientRuntime sürümüne güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="a7d1d-278">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="a7d1d-279">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a7d1d-279">Az.AnalysisServices</span></span>
<span data-ttu-id="a7d1d-280">Az.AnalysisServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-280">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a7d1d-281">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a7d1d-281">Az.Compute</span></span>
* <span data-ttu-id="a7d1d-282">AEM uzantısı: UltraSSD ile P60,P70 ve P80 diskleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-282">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="a7d1d-283">Set-AzVMBootDiagnostics yardım açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-283">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="a7d1d-284">Update-AzImage için yardım açıklaması ve örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-284">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a7d1d-285">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a7d1d-285">Az.RecoveryServices</span></span>
<span data-ttu-id="a7d1d-286">Az.RecoveryServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-286">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a7d1d-287">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a7d1d-287">Az.Resources</span></span>
* <span data-ttu-id="a7d1d-288">Kaynak grupları için etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-288">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="a7d1d-289">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="a7d1d-289">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="a7d1d-290">`Get-AzureRmRoleAssignment` komutunun -ErrorAction'a uymama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-290">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="a7d1d-291">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="a7d1d-291">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="a7d1d-292">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a7d1d-292">Az.Sql</span></span>
* <span data-ttu-id="a7d1d-293">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="a7d1d-293">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="a7d1d-294">Azure hesabında oturum açılmamasının SQL cmdlet'leri yürütülürken nullref özel durumuna yol açması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-294">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="a7d1d-295">Get-AzSqlCapability'de null başvuru özel durumu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-295">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="a7d1d-296">1.2.1 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="a7d1d-296">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a7d1d-297">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a7d1d-297">Az.Accounts</span></span>
* <span data-ttu-id="a7d1d-298">Kimlik Doğrulaması'nın doğru yayınını içeren sürümü</span><span class="sxs-lookup"><span data-stu-id="a7d1d-298">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="a7d1d-299">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a7d1d-299">Az.AnalysisServices</span></span>
* <span data-ttu-id="a7d1d-300">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="a7d1d-300">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a7d1d-301">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a7d1d-301">Az.RecoveryServices</span></span>
* <span data-ttu-id="a7d1d-302">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="a7d1d-302">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="a7d1d-303">1.2.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="a7d1d-303">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a7d1d-304">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a7d1d-304">Az.Accounts</span></span>
* <span data-ttu-id="a7d1d-305">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-305">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="a7d1d-306">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-306">Update incorrect online help URLs</span></span>
* <span data-ttu-id="a7d1d-307">Uninstall-AzureRm için PC Çekirdeğine uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-307">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="a7d1d-308">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="a7d1d-308">Az.Aks</span></span>
* <span data-ttu-id="a7d1d-309">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-309">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a7d1d-310">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a7d1d-310">Az.Automation</span></span>
* <span data-ttu-id="a7d1d-311">Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-311">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="a7d1d-312">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-312">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a7d1d-313">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a7d1d-313">Az.Cdn</span></span>
* <span data-ttu-id="a7d1d-314">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-314">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a7d1d-315">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a7d1d-315">Az.Compute</span></span>
* <span data-ttu-id="a7d1d-316">Invoke-AzVMReimage cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-316">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="a7d1d-317">Set-AzVmss'ye TempDisk parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-317">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="a7d1d-318">New-AzVM'nin uyarı iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-318">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="a7d1d-319">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a7d1d-319">Az.ContainerRegistry</span></span>
* <span data-ttu-id="a7d1d-320">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-320">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a7d1d-321">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a7d1d-321">Az.DataFactory</span></span>
* <span data-ttu-id="a7d1d-322">ADF .Net SDK sürümü 3.0.0'a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-322">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a7d1d-323">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a7d1d-323">Az.DataLakeStore</span></span>
* <span data-ttu-id="a7d1d-324">MSI kullanırken ADLS uç noktasındaki sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-324">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="a7d1d-325">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="a7d1d-325">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="a7d1d-326">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-326">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a7d1d-327">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a7d1d-327">Az.IotHub</span></span>
* <span data-ttu-id="a7d1d-328">Add-IotHubRoutingEndpoint cmdlet'ine Kodlama biçimi eklendi.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-328">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a7d1d-329">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a7d1d-329">Az.KeyVault</span></span>
* <span data-ttu-id="a7d1d-330">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-330">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a7d1d-331">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a7d1d-331">Az.Network</span></span>
* <span data-ttu-id="a7d1d-332">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-332">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="a7d1d-333">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a7d1d-333">Az.Resources</span></span>
* <span data-ttu-id="a7d1d-334">'New-AzADAppCredential' ve 'New-AzADSpCredential' başvuru belgelerindeki hatalı örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-334">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="a7d1d-335">Kaynak grubu dağıtım cmdlet'lerini yürütmeden önce '-TemplateFile' parametresi yolunun çözülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-335">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="a7d1d-336">Az.Resources: Belgede New-AzureRmPolicyDefinition -Mode varsayılan değeri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-336">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="a7d1d-337">Az.Resources: https://github.com/Azure/azure-powershell/issues/7522 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-337">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="a7d1d-338">Az.Resources: https://github.com/Azure/azure-powershell/issues/5747 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-338">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="a7d1d-339">'PSResourceGroupDeployment' nesnesinin biçimlendirme sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-339">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="a7d1d-340">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="a7d1d-340">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a7d1d-341">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a7d1d-341">Az.ServiceFabric</span></span>
* <span data-ttu-id="a7d1d-342">VMSS modeline sertifika eklendiğinde ama özel durum oluştuğunda geri alma için hata düzeltmesi: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="a7d1d-342">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="a7d1d-343">Bazı hata iletileri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-343">Fix some error messages.</span></span>
* <span data-ttu-id="a7d1d-344">Az geçişinde çalışmayan New-AzServiceFabriCluster için varsayılan ARM şablonuyla küme oluşturma sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-344">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="a7d1d-345">Uzantıda küme kimliği denetlenerek küme/uygulama sertifikasının yalnızca kümeye karşılık gelen VM Ölçek Kümelerine eklenmesi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-345">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="a7d1d-346">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="a7d1d-346">Az.SignalR</span></span>
* <span data-ttu-id="a7d1d-347">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-347">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="a7d1d-348">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a7d1d-348">Az.Sql</span></span>
* <span data-ttu-id="a7d1d-349">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-349">Update incorrect online help URLs</span></span>
* <span data-ttu-id="a7d1d-350">LicenseType parametresinin parametre açıklaması olası değerlerle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-350">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="a7d1d-351">Yönetilen örnek kimliği güncelleştirmesinin, güncelleştirilen tek özellik bu olduğunda çalışmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-351">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="a7d1d-352">Yönetilen örnekte özel harmanlama desteği</span><span class="sxs-lookup"><span data-stu-id="a7d1d-352">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a7d1d-353">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a7d1d-353">Az.Storage</span></span>
* <span data-ttu-id="a7d1d-354">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-354">Update incorrect online help URLs</span></span>
* <span data-ttu-id="a7d1d-355">Premium Depolama Hesabı klasik Günlük/Ölçüm desteği sağlamadığından, Premium Depolama Hesabında klasik Günlük/Ölçüm için get/set komutları kullanıldığında ayrıntılı hata iletisi veriliyor.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-355">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="a7d1d-356">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="a7d1d-356">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="a7d1d-357">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="a7d1d-357">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="a7d1d-358">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="a7d1d-358">Az.TrafficManager</span></span>
* <span data-ttu-id="a7d1d-359">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-359">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a7d1d-360">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a7d1d-360">Az.Websites</span></span>
* <span data-ttu-id="a7d1d-361">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-361">Update incorrect online help URLs</span></span>
* <span data-ttu-id="a7d1d-362">Uygulama ASE'de barındırılıyorsa, sertifikayı doğru kaynak grubuna ve konuma yüklemek için 'New-AzWebAppSSLBinding' düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-362">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="a7d1d-363">SSL sertifikası bir uygulamaya bağlanırken etiketlerin üzerine yazılmaması için 'New-AzWebAppSSLBinding' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-363">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="a7d1d-364">1.1.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="a7d1d-364">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a7d1d-365">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a7d1d-365">Az.Accounts</span></span>
* <span data-ttu-id="a7d1d-366">Enable-AzureRmAlias cmdlet'ine 'Local' Kapsamı eklendi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-366">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a7d1d-367">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a7d1d-367">Az.Compute</span></span>
* <span data-ttu-id="a7d1d-368">Restart/Start/Stop/Remove/Set-AzVM ve Save-AzVMImage için ayarlanan ID parametresinde ad artık isteğe bağlı</span><span class="sxs-lookup"><span data-stu-id="a7d1d-368">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="a7d1d-369">Yardım dosyalarında ID parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-369">Updated the description of ID in help files</span></span>
* <span data-ttu-id="a7d1d-370">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="a7d1d-370">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a7d1d-371">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a7d1d-371">Az.DataLakeStore</span></span>
* <span data-ttu-id="a7d1d-372">SDK düzeltmeleri için veri düzleminin SDK sürümü 1.1.14 olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-372">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="a7d1d-373">getfilestatus ve liststatus için negatif acesstime ve modificationtime değerlerini işleme yöntemi düzeltildi, async iptal belirteci düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-373">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="a7d1d-374">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a7d1d-374">Az.EventGrid</span></span>
* <span data-ttu-id="a7d1d-375">2019-01-01 API sürümünü kullanmak için güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-375">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="a7d1d-376">Aşağıdaki cmdlet'ler 2019-01-01 API sürümünde yeni senaryoyu destekleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-376">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="a7d1d-377">New-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="a7d1d-377">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="a7d1d-378">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="a7d1d-378">Event Time-To-Live,</span></span>
        - <span data-ttu-id="a7d1d-379">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="a7d1d-379">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="a7d1d-380">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-380">Dead letter endpoint.</span></span>
    - <span data-ttu-id="a7d1d-381">Update-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="a7d1d-381">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="a7d1d-382">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="a7d1d-382">Event Time-To-Live,</span></span>
        - <span data-ttu-id="a7d1d-383">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="a7d1d-383">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="a7d1d-384">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-384">Dead letter endpoint.</span></span>
* <span data-ttu-id="a7d1d-385">New-AzureRmEventGridSubscription ve Update-AzureRmEventGridSubscription cmdlet'lerinde EndpointType seçeneği için yeni enum değerleri (storageQueue ve hybridConnection) eklendi.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-385">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="a7d1d-386">Olay aboneliğini oluşturma veya güncelleştirme işleminde kullanıcının el ile bir eylem yapması beklendiğinde uyarı iletisi gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-386">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a7d1d-387">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a7d1d-387">Az.IotHub</span></span>
* <span data-ttu-id="a7d1d-388">IotHub SDK'sı en son sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-388">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="a7d1d-389">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a7d1d-389">Az.LogicApp</span></span>
* <span data-ttu-id="a7d1d-390">Get-AzLogicApp, Name değeri belirtilmemiş olanların tümünü listeliyor</span><span class="sxs-lookup"><span data-stu-id="a7d1d-390">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="a7d1d-391">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a7d1d-391">Az.Resources</span></span>
* <span data-ttu-id="a7d1d-392">'Get-AzResource' için '-ODataQuery' ve '-ResourceId' parametreleri sağlanırken ortaya çıkan parametre ayarlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-392">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="a7d1d-393">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="a7d1d-393">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="a7d1d-394">New/Set-AzPolicyDefinition cmdlet'lerinde -Custom parametresinin işlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-394">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="a7d1d-395">New-AzDeployment belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-395">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="a7d1d-396">'New-AzADUser' için '-MailNickname' parametresi zorunlu hale getirildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-396">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="a7d1d-397">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="a7d1d-397">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="a7d1d-398">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="a7d1d-398">Az.SignalR</span></span>
* <span data-ttu-id="a7d1d-399">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="a7d1d-399">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="a7d1d-400">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a7d1d-400">Az.Sql</span></span>
* <span data-ttu-id="a7d1d-401">Depolama yönetimi istemci bağımlılığı ortak SDK uygulamasına dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-401">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a7d1d-402">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a7d1d-402">Az.Storage</span></span>
* <span data-ttu-id="a7d1d-403">Sas Token, OAuth veya Anonymous ile oluşturulduğunda Storage bağlamının StorageAccountName değeri gerçek Depolama Hesabı Adına ayarlanıyor</span><span class="sxs-lookup"><span data-stu-id="a7d1d-403">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="a7d1d-404">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="a7d1d-404">New-AzStorageContext</span></span>
* <span data-ttu-id="a7d1d-405">Blob Anlık Görüntü Nesnesinin Sas Belirteci '-FullUri' parametresiyle oluşturulduğunda, döndürülen Uri anlık görüntü Uri'si olacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-405">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="a7d1d-406">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="a7d1d-406">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a7d1d-407">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a7d1d-407">Az.Websites</span></span>
* <span data-ttu-id="a7d1d-408">'Get-AzDeletedWebApp' cmdlet'indeki tarih ayrıştırma hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-408">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="a7d1d-409">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="a7d1d-409">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="a7d1d-410">1.0.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="a7d1d-410">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="a7d1d-411">Genel</span><span class="sxs-lookup"><span data-stu-id="a7d1d-411">General</span></span>

- <span data-ttu-id="a7d1d-412">Az Modülü Genel Kullanıma Sunuldu</span><span class="sxs-lookup"><span data-stu-id="a7d1d-412">General Availability of Az Module</span></span>
- <span data-ttu-id="a7d1d-413">Her modül için çevrimiçi yardım</span><span class="sxs-lookup"><span data-stu-id="a7d1d-413">Online help for each module</span></span>
- <span data-ttu-id="a7d1d-414">Diğer ayrıntılar ve yol haritası için bkz. [Az Duyuru Sayfası](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="a7d1d-414">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="a7d1d-415">AzureRM’den geçiş hakkında bilgi edinmek için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a7d1d-415">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="a7d1d-416">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a7d1d-416">Az.Accounts</span></span>
- <span data-ttu-id="a7d1d-417">Önceki adı: Az.Profile</span><span class="sxs-lookup"><span data-stu-id="a7d1d-417">Changed from Az.Profile</span></span>
- <span data-ttu-id="a7d1d-418">Profil ve bağlam türleri için tablo biçimleri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-418">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="a7d1d-419">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a7d1d-419">Az.ApiManagement</span></span>
- <span data-ttu-id="a7d1d-420">#7002 düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="a7d1d-420">Fixes for #7002</span></span>
- <span data-ttu-id="a7d1d-421">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a7d1d-421">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="a7d1d-422">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="a7d1d-422">Az.Batch</span></span>
- <span data-ttu-id="a7d1d-423">`PSComputeNode` üzerinde yeni `NodeAgentInformation` aracılığıyla bir havuzdaki her bir VM’de Azure Batch Düğüm Aracısı’nın hangi sürümünün çalıştığını görme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-423">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="a7d1d-424">`PSDataDisk` için `Caching` varsayılan ayarı artık `None` yerine `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-424">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="a7d1d-425">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a7d1d-425">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="a7d1d-426">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="a7d1d-426">Az.Billing</span></span>
- <span data-ttu-id="a7d1d-427">Billing, Consumption ve UsageAggregates cmdlet’lerini birleştirir, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a7d1d-427">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="a7d1d-428">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="a7d1d-428">Az.CognitivServices</span></span>
- <span data-ttu-id="a7d1d-429">New-AzureRmCognitiveServicesAccount işleminde kullanılabilen SkuName ve Typem için tamamlayıcılar eklendi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-429">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="a7d1d-430">Get-AzCognitiveServicesAccountSkus cmdlet’inden GetSkusWithAccountParamSetName parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="a7d1d-430">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="a7d1d-431">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="a7d1d-431">Az.ContainerInstance</span></span>
- <span data-ttu-id="a7d1d-432">ManagedIdentity desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-432">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="a7d1d-433">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="a7d1d-433">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="a7d1d-434">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a7d1d-434">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="a7d1d-435">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a7d1d-435">Az.DataLakeStore</span></span>
- <span data-ttu-id="a7d1d-436">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a7d1d-436">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="a7d1d-437">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a7d1d-437">Az.Monitor</span></span>
- <span data-ttu-id="a7d1d-438">Az.Insights cmdlet’inin adı Az.Monitor olarak değiştirildi ve başka yeni değişiklikler yapıldı, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a7d1d-438">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="a7d1d-439">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a7d1d-439">Az.KeyVault</span></span>
- <span data-ttu-id="a7d1d-440">Çıkış türlerinden kullanım dışı 'PurgeDisabled' özelliği kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="a7d1d-440">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="a7d1d-441">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="a7d1d-441">Az.MachineLearning</span></span>
- <span data-ttu-id="a7d1d-442">Az.MachineLearningCompute modülünden cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-442">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="a7d1d-443">Az.Media</span><span class="sxs-lookup"><span data-stu-id="a7d1d-443">Az.Media</span></span>
- <span data-ttu-id="a7d1d-444">New-AzMediaService cmdlet’inden kullanım dışı -Tags diğer adı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="a7d1d-444">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="a7d1d-445">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a7d1d-445">Az.Network</span></span>
<span data-ttu-id="a7d1d-446">Application Gateway’de RewriteRuleSets parametresini yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-446">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="a7d1d-447">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="a7d1d-447">New cmdlets added:</span></span>
        - <span data-ttu-id="a7d1d-448">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a7d1d-448">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a7d1d-449">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a7d1d-449">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a7d1d-450">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a7d1d-450">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a7d1d-451">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a7d1d-451">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a7d1d-452">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a7d1d-452">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a7d1d-453">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="a7d1d-453">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="a7d1d-454">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="a7d1d-454">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="a7d1d-455">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="a7d1d-455">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="a7d1d-456">Cmdlet’ler isteğe bağlı -RewriteRuleSet parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-456">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="a7d1d-457">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a7d1d-457">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="a7d1d-458">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="a7d1d-458">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="a7d1d-459">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="a7d1d-459">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="a7d1d-460">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a7d1d-460">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="a7d1d-461">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a7d1d-461">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="a7d1d-462">New-AzureRmApplicationGatewayUrlPathMapConfig, Kimlik kullanarak Application Gateway’e KeyVault Desteği ekledi.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-462">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="a7d1d-463">Cmdlet’ler isteğe bağlı -KeyVaultSecretId, -KeyVaultSecret parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-463">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="a7d1d-464">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a7d1d-464">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="a7d1d-465">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a7d1d-465">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="a7d1d-466">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a7d1d-466">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="a7d1d-467">New-AzApplicationGateway cmdlet’i isteğe bağlı -UserAssignedIdentity parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-467">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="a7d1d-468">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a7d1d-468">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="a7d1d-469">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a7d1d-469">Az.OperationalInsights</span></span>
- <span data-ttu-id="a7d1d-470">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a7d1d-470">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="a7d1d-471">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="a7d1d-471">Az.Profile</span></span>
- <span data-ttu-id="a7d1d-472">Modül adı Az.Accounts olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-472">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="a7d1d-473">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a7d1d-473">Az.RecoveryServices</span></span>
- <span data-ttu-id="a7d1d-474">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a7d1d-474">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="a7d1d-475">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a7d1d-475">Az.Resources</span></span>
- <span data-ttu-id="a7d1d-476">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a7d1d-476">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="a7d1d-477">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a7d1d-477">Az.ServiceFabric</span></span>
- <span data-ttu-id="a7d1d-478">Sertifikayı ortak ad ve parmak iziyle belirtme desteği</span><span class="sxs-lookup"><span data-stu-id="a7d1d-478">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="a7d1d-479">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a7d1d-479">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="a7d1d-480">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="a7d1d-480">Az.SIgnalR</span></span>
- <span data-ttu-id="a7d1d-481">SIgnalR için PowerShell cmdlet'leri Genel Kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="a7d1d-481">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="a7d1d-482">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a7d1d-482">Az.Sql</span></span>
- <span data-ttu-id="a7d1d-483">Tehdit Algılama cmdlet’lerine yeni Data_Exfiltration ve Unsafe_Action algılama türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-483">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="a7d1d-484">Sql Denetimi cmdlet'leri için belge örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-484">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="a7d1d-485">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a7d1d-485">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="a7d1d-486">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a7d1d-486">Az.Storage</span></span>
- <span data-ttu-id="a7d1d-487">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a7d1d-487">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="a7d1d-488">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a7d1d-488">Az.Websites</span></span>
- <span data-ttu-id="a7d1d-489">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a7d1d-489">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="a7d1d-490">0.7.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="a7d1d-490">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="a7d1d-491">Genel</span><span class="sxs-lookup"><span data-stu-id="a7d1d-491">General</span></span>

* <span data-ttu-id="a7d1d-492">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="a7d1d-492">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="a7d1d-493">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a7d1d-493">Az.Compute</span></span>

* <span data-ttu-id="a7d1d-494">`New-AzVm(ss)` cmdlet’leri için basit parametre kümelerinde UltraSSD ve Galeri Görüntüleri desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-494">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="a7d1d-495">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a7d1d-495">Az.DataLakeStore</span></span>

* <span data-ttu-id="a7d1d-496">Adls hesabı etki alanının sonundaki eğik çizgi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-496">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="a7d1d-497">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a7d1d-497">Az.FrontDoor</span></span>

* <span data-ttu-id="a7d1d-498">Bazı bozuk bağlantılar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-498">Fixed some broken links</span></span>
    - <span data-ttu-id="a7d1d-499">New-AzureRmFrontDoor ve Set-AzureRmFrontDoor makalelerinde, New-AzureRmFrontDoorHealthProbeSettingObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-499">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="a7d1d-500">New-AzureRmFrontDoorManagedRuleObject makalesinde, New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-500">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="a7d1d-501">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a7d1d-501">Az.RecoveryServices</span></span>

* <span data-ttu-id="a7d1d-502">Azure Dosya Paylaşımı geri yükleme işlemleri için istemci tarafı doğrulamalar eklendi.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-502">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="a7d1d-503">Afs geri yükleme işlemi için storageAccountName ve storageAccountResourceGroupName isteğe bağlı hale getirildi.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-503">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="a7d1d-504">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a7d1d-504">Az.Resources</span></span>

* <span data-ttu-id="a7d1d-505">[https://github.com/Azure/azure-powershell/issues/7402](https://github.com/Azure/azure-powershell/issues/7679) düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-505">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="a7d1d-506">Get-AzureRmRoleAssignment, klasik yöneticiler istenirken sağlanmışsa abonelik kapsamını kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-506">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="a7d1d-507">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a7d1d-507">Az.Sql</span></span>

* <span data-ttu-id="a7d1d-508">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="a7d1d-508">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="a7d1d-509">Get-AzureRmSqlDatabaseVulnerabilityAssessment cmdlet’inin DotNet core ile kullanılması konusundaki bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-509">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="a7d1d-510">SQL Denetimi cmdlet’leriyle ilgili yardım iletilerinin belgeleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-510">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="a7d1d-511">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a7d1d-511">Az.Storage</span></span>

* <span data-ttu-id="a7d1d-512">New-AzureRmStorageAccount cmdlet’ine -EnableHierarchicalNamespace eklendi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-512">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="a7d1d-513">-DestContext girilmediğinde Dosya Kopyalama cmdlet’inin hedefte kaynak bağlamını yeniden kullanamamasına yol açan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-513">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="a7d1d-514">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="a7d1d-514">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="a7d1d-515">Statik Web Sitesi yapılandırması için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-515">Support Static Website configuration</span></span>
    - <span data-ttu-id="a7d1d-516">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="a7d1d-516">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="a7d1d-517">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="a7d1d-517">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="a7d1d-518">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a7d1d-518">Az.Websites</span></span>

* <span data-ttu-id="a7d1d-519">Set-AzureRmWebApp ve Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a7d1d-519">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="a7d1d-520">Windows ve Linux kapsayıcı uygulamalarında bağlanacak Azure Depolama yollarının belirtilmesi için yeni parametre (-AzureStoragePath) eklendi.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-520">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="a7d1d-521">Azure Depolama yollarını ayarlamak için yeni New-AzureRmWebAppAzureStoragePath cmdlet’inin çıktısını bir parametre olarak kullanın.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-521">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="a7d1d-522">0.6.1 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="a7d1d-522">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="a7d1d-523">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a7d1d-523">Az.ApiManagement</span></span>
* <span data-ttu-id="a7d1d-524">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="a7d1d-524">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="a7d1d-525">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a7d1d-525">Az.Automation</span></span>
* <span data-ttu-id="a7d1d-526">Swagger tabanlı Azure Otomasyon cmdlet'leri</span><span class="sxs-lookup"><span data-stu-id="a7d1d-526">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="a7d1d-527">Güncelleştirme Yönetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-527">Added Update Management cmdlets</span></span>
* <span data-ttu-id="a7d1d-528">Kaynak Denetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-528">Added Source Control cmdlets</span></span>
* <span data-ttu-id="a7d1d-529">Remove-AzureRmAutomationHybridWorkerGroup cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-529">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="a7d1d-530">DSC Kayıt Düğümü komutu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-530">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="a7d1d-531">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a7d1d-531">Az.Compute</span></span>
* <span data-ttu-id="a7d1d-532">SystemAssigned kimliği için kimlik sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-532">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="a7d1d-533">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="a7d1d-533">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="a7d1d-534">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="a7d1d-534">Az.ContainerInstance</span></span>
* <span data-ttu-id="a7d1d-535">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="a7d1d-535">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="a7d1d-536">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="a7d1d-536">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="a7d1d-537">Market cmdlet'leri için örnekler açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-537">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="a7d1d-538">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a7d1d-538">Az.Network</span></span>
* <span data-ttu-id="a7d1d-539">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-539">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="a7d1d-540">Desteklenen AzureFirewall Ağ Protokollerine yeniden ICMP eklendi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-540">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="a7d1d-541">Test-AzureRmNetworkWatcherConnectivity cmdlet'i güncelleştirildi; hedef kimlik, adres ve bağlantı noktasında doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-541">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="a7d1d-542">VirtualNetwork eşlemesinde bellek kullanımıyla ilgili sorunlar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-542">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="a7d1d-543">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="a7d1d-543">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="a7d1d-544">Korumalı dosya paylaşımı için ilke değiştirme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-544">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="a7d1d-545">İlke saat dilimi büyük harfe dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-545">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="a7d1d-546">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="a7d1d-546">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="a7d1d-547">New-AzureRmRecoveryServicesAsrProtectableItem cmdlet'indeki örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-547">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="a7d1d-548">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="a7d1d-548">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="a7d1d-549">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="a7d1d-549">Az.Relay</span></span>
* <span data-ttu-id="a7d1d-550">Kullanıcının New-AzureRmRelayKey cmdlet'ine KeyValue sağlamasına olanak tanıyan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-550">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="a7d1d-551">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a7d1d-551">Az.Resources</span></span>
* <span data-ttu-id="a7d1d-552">Şu cmdlet'lerdeki kaynak kimliğiyle ilgili parametrelerin yardım belgeleri güncelleştirildi: `New-AzureRmPolicyAssignment` ve</span><span class="sxs-lookup"><span data-stu-id="a7d1d-552">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and</span></span> `Set-AzureRmPolicyAssignment`
* <span data-ttu-id="a7d1d-553">New-AzureRmPolicyDefinition cmdlet'ine -Metadata kullanan bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-553">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="a7d1d-554">NetStandard'da Tag anahtarında büyük/küçük harf kullanımının korunmasına yönelik düzeltme yapıldı: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="a7d1d-554">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="a7d1d-555">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a7d1d-555">Az.ServiceFabric</span></span>
* <span data-ttu-id="a7d1d-556">Hataya neden olan değişiklikler yayınlanacağından kullanımdan kaldırılacak özellikleri belirten iletiler eklendi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-556">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="a7d1d-557">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a7d1d-557">Az.Sql</span></span>
* <span data-ttu-id="a7d1d-558">Azure Sql Veritabanı Yönetilen Örneği ve Azure Sql Yönetilen Veritabanı'nındaki CRUD işlemleri için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-558">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="a7d1d-559">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a7d1d-559">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="a7d1d-560">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a7d1d-560">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="a7d1d-561">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a7d1d-561">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="a7d1d-562">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a7d1d-562">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="a7d1d-563">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="a7d1d-563">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="a7d1d-564">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="a7d1d-564">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="a7d1d-565">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="a7d1d-565">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="a7d1d-566">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="a7d1d-566">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="a7d1d-567">Sunucuda veya veritabanında Genişletilmiş Denetim İlkesi yönetimi etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-567">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="a7d1d-568">Denetim günlüklerinde filtrelemeyi etkinleştirmek için yeni parametre (PredicateExpression) eklendi.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-568">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="a7d1d-569">Cmdlet'ler, SQL istemcileri yerine Eski istemcileri kullanacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-569">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="a7d1d-570">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-570">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="a7d1d-571">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-571">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="a7d1d-572">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-572">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="a7d1d-573">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-573">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="a7d1d-574">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings cmdlet'inin depolama hesabı ad parametre kümesiyle kullanılmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-574">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="a7d1d-575">0.5.0 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="a7d1d-575">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="a7d1d-576">Genel</span><span class="sxs-lookup"><span data-stu-id="a7d1d-576">General</span></span>
* <span data-ttu-id="a7d1d-577">Birçok temel cmdlet’e Kaynak Tamamlayıcıları eklendi - bunlar cmdlet’leri etkileşimli olarak çağırırken mevcut kaynak adları arasında gezinmenize olanak tanır</span><span class="sxs-lookup"><span data-stu-id="a7d1d-577">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="a7d1d-578">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="a7d1d-578">Az.Profile</span></span>
* <span data-ttu-id="a7d1d-579">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-579">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="a7d1d-580">Connect-AzAccount cmdlet'indeki TenantId parametresi Tenant olarak yeniden adlandırıldı ve TenantId için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-580">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="a7d1d-581">Connect-AzAccount için TenantId açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-581">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="a7d1d-582">Kiracı etki alanı sağlanırken başarısız oturum açma durumunda gösterilen hata iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-582">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="a7d1d-583">Kiracıda abonelikleri olmayan hesaplar için bağlam adı çakışmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-583">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="a7d1d-584">MSI kullanırken DataLake uç noktalarıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-584">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="a7d1d-585">Bağlantı olmadığında 'Disconnect-AzAccount' oluşturulmasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-585">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="a7d1d-586">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a7d1d-586">Az.CognitiveServices</span></span>
* <span data-ttu-id="a7d1d-587">Get-AzCognitiveServicesAccountSkus işlemi eklendi.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-587">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a7d1d-588">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a7d1d-588">Az.Compute</span></span>
* <span data-ttu-id="a7d1d-589">Add-AzVmssVMDataDisk ve Remove-AzVmssVMDataDisk cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-589">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="a7d1d-590">Get-AzVMImage, AutomaticOSUpgradeProperties gösteriyor</span><span class="sxs-lookup"><span data-stu-id="a7d1d-590">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="a7d1d-591">SetAzVMChefExtension -BootstrapOptions ve -JsonAttribute seçeneği değerlerinin Json biçiminde ayarlanmamasıyla ilgili hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-591">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a7d1d-592">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a7d1d-592">Az.DataLakeStore</span></span>
* <span data-ttu-id="a7d1d-593">DataLake paketi 1.1.10'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-593">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="a7d1d-594">Çok iş parçacıklı işlemlere varsayılan Concurrency değeri eklendi.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-594">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="a7d1d-595">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="a7d1d-595">Az.Insights</span></span>
* <span data-ttu-id="a7d1d-596">7267 numaralı (Otomatik ölçeklendirme alanı) sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-596">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="a7d1d-597">Yeni otomatik ölçeklendirme kuralı oluşturma sırasında numaralandırılmış parametrelerin düzgün ayarlanmamasıyla ilgili sorunlar (bunlar her zaman varsayılan değere ayarlanıyordu).</span><span class="sxs-lookup"><span data-stu-id="a7d1d-597">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="a7d1d-598">Set-AzDiagnosticSetting'in ayar oluşturma sırasında kategorilerin açıkça belirtilmesini gerektirmesiyle ilgili 7513 numaralı [Insights] sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-598">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="a7d1d-599">Artık cmdlet oluşturma sırasında açık kategori gösteriminin etkinleştirilmesini gerektirmiyor; başka bir deyişle belgelerinde belirtildiği gibi çalışıyor</span><span class="sxs-lookup"><span data-stu-id="a7d1d-599">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a7d1d-600">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a7d1d-600">Az.Network</span></span>
* <span data-ttu-id="a7d1d-601">Aşağıdaki parametrelerde PeeringType parametresi zorunlu parametre olarak değiştirildi:-</span><span class="sxs-lookup"><span data-stu-id="a7d1d-601">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="a7d1d-602">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="a7d1d-602">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="a7d1d-603">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="a7d1d-603">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="a7d1d-604">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="a7d1d-604">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="a7d1d-605">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="a7d1d-605">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="a7d1d-606">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="a7d1d-606">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="a7d1d-607">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="a7d1d-607">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a7d1d-608">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a7d1d-608">Az.PolicyInsights</span></span>
* <span data-ttu-id="a7d1d-609">İlke düzeltme cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-609">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="a7d1d-610">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a7d1d-610">Az.Resources</span></span>
* <span data-ttu-id="a7d1d-611">[https://github.com/Azure/azure-powershell/issues/7402](https://github.com/Azure/azure-powershell/issues/7402) düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-611">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="a7d1d-612">'Get-AzResource' için '-ResourceId' parametresi kullanılarak kaynakların listelenmesine olanak tanındı</span><span class="sxs-lookup"><span data-stu-id="a7d1d-612">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="a7d1d-613">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a7d1d-613">Az.ServiceBus</span></span>
* <span data-ttu-id="a7d1d-614">PSServiceBusMigrationConfigurationAttributes'e Geçiş durumunun bilinmesine yardımcı olacak salt okunur MigrationState özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-614">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a7d1d-615">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a7d1d-615">Az.ServiceFabric</span></span>
* <span data-ttu-id="a7d1d-616">Linux Vmss'ye sertifika ekleme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-616">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="a7d1d-617">'Add-AzServiceFabricClusterCertificate' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-617">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="a7d1d-618">Yeni sertifikadan doğru parmak izi kullanıyor (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="a7d1d-618">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="a7d1d-619">Özel durum doğru görüntüleniyor (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="a7d1d-619">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="a7d1d-620">'Update-AzServiceFabricDurability', Vmss CreateOrUpdate işlemini başlatmadan önce küme yapılandırmasını güncelleştirecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-620">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="a7d1d-621">0.4.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="a7d1d-621">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="a7d1d-622">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="a7d1d-622">Az.Profile</span></span>
* <span data-ttu-id="a7d1d-623">CloudShell’de Get-AzSubscription sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="a7d1d-623">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="a7d1d-624">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-624">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a7d1d-625">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a7d1d-625">Az.Compute</span></span>
* <span data-ttu-id="a7d1d-626">'New-AzVm' için basit parametre kümesi kullanıldığında hızlandırılmış ağların açılacağı VM boyutları beyaz listesine yeni boyutlar eklendi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-626">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="a7d1d-627">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-627">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a7d1d-628">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a7d1d-628">Az.DataLakeStore</span></span>
* <span data-ttu-id="a7d1d-629">Sanal Ağ Kuralları desteği ekleme</span><span class="sxs-lookup"><span data-stu-id="a7d1d-629">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="a7d1d-630">Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store sanal ağ kuralını alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-630">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="a7d1d-631">Add-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabına sanal ağ kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-631">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="a7d1d-632">Set-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabındaki belirtilen sanal ağ kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-632">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="a7d1d-633">Remove-AzDataLakeStoreVirtualNetworkRule: Bir Azure Data Lake Store sanal ağ kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-633">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a7d1d-634">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a7d1d-634">Az.Network</span></span>
* <span data-ttu-id="a7d1d-635">Test-AzNetworkWatcherConnectivity cmdlet'i güncelleştirildi, arka uca protokol değerini geçiriyor.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-635">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="a7d1d-636">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-636">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a7d1d-637">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a7d1d-637">Az.Resources</span></span>
* <span data-ttu-id="a7d1d-638">Get-AzRoleDefinition cmdlet'inin anlaşılmaz bir özel durum oluşturmasına neden olan hata (varsayılan profilin içinde abonelik olmadığında ve hiçbir kapsam belirtilmediğinde), senaryoya anlamlı bir özel durum eklenerek düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-638">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="a7d1d-639">Ayrıca varsayılan parametre kümesi 'RoleDefinitionNameParameterSet' olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-639">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="a7d1d-640">0.3.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="a7d1d-640">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="a7d1d-641">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="a7d1d-641">Azure.Storage</span></span>
* <span data-ttu-id="a7d1d-642">Hedefte meta veri sorunu olduğunda Fix Copy Blob/File meta verileri kopyalamayacak</span><span class="sxs-lookup"><span data-stu-id="a7d1d-642">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="a7d1d-643">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="a7d1d-643">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="a7d1d-644">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="a7d1d-644">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="a7d1d-645">Belirli bir konumunun Depolama kaynağı kullanımını alma desteği ve genel Depolama kayrağı kullanımını almak için uyarı iletisi ekleme kullanımdan kalktı.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-645">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="a7d1d-646">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="a7d1d-646">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="a7d1d-647">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a7d1d-647">Az.CognitiveServices</span></span>
* <span data-ttu-id="a7d1d-648">Mevcut hesap olmadan Get-AzCognitiveServicesAccountSkus desteği.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-648">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a7d1d-649">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a7d1d-649">Az.Compute</span></span>
* <span data-ttu-id="a7d1d-650">Get-AzVM -ResourceGroupName <rg> gerektiğinde 50'den fazla sonuç döndürecek şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-650">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="a7d1d-651">New-AzVmss cmdlet'inin yardımına 'SimpleParameterSet' örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-651">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="a7d1d-652">Azure Disk Şifrelemesi ilerleme durumu iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-652">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="a7d1d-653">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="a7d1d-653">Az.DataFactoryV2</span></span>
* <span data-ttu-id="a7d1d-654">ADF .Net SDK sürümü 2.3.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-654">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a7d1d-655">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a7d1d-655">Az.Network</span></span>
* <span data-ttu-id="a7d1d-656">NetworkProfile işlevselliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-656">Added NetworkProfile functionality.</span></span> <span data-ttu-id="a7d1d-657">yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-657">new cmdlets added</span></span>
    - <span data-ttu-id="a7d1d-658">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a7d1d-658">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="a7d1d-659">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a7d1d-659">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="a7d1d-660">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a7d1d-660">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="a7d1d-661">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a7d1d-661">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="a7d1d-662">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="a7d1d-662">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="a7d1d-663">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="a7d1d-663">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="a7d1d-664">Alt Ağ Modeline hizmet ilişki bağlantısı eklendi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-664">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="a7d1d-665">New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-665">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="a7d1d-666">Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-666">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="a7d1d-667">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="a7d1d-667">Az.RedisCache</span></span>
* <span data-ttu-id="a7d1d-668">Bundan sonra Size parametresi olarak her dizeye izin veriliyor.</span><span class="sxs-lookup"><span data-stu-id="a7d1d-668">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="a7d1d-669">PSArgumentCompleter açılan listesine P5 eklendi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-669">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="a7d1d-670">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a7d1d-670">Az.Resources</span></span>
* <span data-ttu-id="a7d1d-671">Set-AzPolicyDefinition'a eksik -Mode parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-671">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="a7d1d-672">Origin öğesi User içeren işlemler için Get-AzProviderOperation commandlet hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-672">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="a7d1d-673">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a7d1d-673">Az.Sql</span></span>
* <span data-ttu-id="a7d1d-674">Bazı yedekleme cmdlet'lerinin geçerli Azure aboneliğini tanıyamamasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a7d1d-674">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a7d1d-675">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a7d1d-675">Az.Websites</span></span>
* <span data-ttu-id="a7d1d-676">Yeni Get-AzWebAppContainerContinuousDeploymentUrl Cmdlet'i - Kapsayıcı Sürekli Dağıtım Web Kancası URL'sini alıyor</span><span class="sxs-lookup"><span data-stu-id="a7d1d-676">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="a7d1d-677">Yeni New-AzWebAppContainerPSSession ve Enter-WebAppContainerPSSession Cmdlet'leri - Windows kapsayıcı uygulamasında PowerShell uzak oturumunu başlatıyor</span><span class="sxs-lookup"><span data-stu-id="a7d1d-677">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="a7d1d-678">0.2.0 - Eylül 2018</span><span class="sxs-lookup"><span data-stu-id="a7d1d-678">0.2.0 - September 2018</span></span>
 <span data-ttu-id="a7d1d-679">İlk Yayın</span><span class="sxs-lookup"><span data-stu-id="a7d1d-679">Initial Release</span></span>