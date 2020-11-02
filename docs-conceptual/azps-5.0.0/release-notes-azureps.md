---
title: Azure PowerShell sürüm notları
description: Azure PowerShell modüllerine yönelik en son güncelleştirmeler hakkında bilgi edinin.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 913532fa5a8937f7ba4cc1ce21c5879f3920fc7f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92753850"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="af695-103">Azure PowerShell sürüm notları</span><span class="sxs-lookup"><span data-stu-id="af695-103">Azure PowerShell release notes</span></span>

## <a name="500---october-2020"></a><span data-ttu-id="af695-104">5.0.0 - Ekim 2020</span><span class="sxs-lookup"><span data-stu-id="af695-104">5.0.0 - October 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="af695-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="af695-105">Az.Accounts</span></span>
* <span data-ttu-id="af695-106">[Yeni Değişiklik] 'Get-AzProfile' ve 'Select-AzProfile' kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="af695-106">[Breaking Change] Removed 'Get-AzProfile' and 'Select-AzProfile'</span></span>
* <span data-ttu-id="af695-107">Azure Directory Authentication Library, Microsoft Authentication Library (MSAL) ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-107">Replaced Azure Directory Authentication Library with Microsoft Authentication Library(MSAL)</span></span>

#### <a name="azaks"></a><span data-ttu-id="af695-108">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="af695-108">Az.Aks</span></span>
* <span data-ttu-id="af695-109">[Yeni Değişiklik] 'New-AzAksCluster' ve 'Set-AzAksCluster' cmdlet’indeki 'ClientIdAndSecret' parametre diğer adı kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="af695-109">[Breaking Change] Removed parameter alias 'ClientIdAndSecret' in 'New-AzAksCluster' and 'Set-AzAksCluster'.</span></span>
* <span data-ttu-id="af695-110">[Yeni Değişiklik] 'New-AzAksCluster' cmdlet’indeki 'NodeVmSetType' parametresinin 'AvailabilitySet' varsayılan değeri 'VirtualMachineScaleSets' olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-110">[Breaking Change] Changed the default value of 'NodeVmSetType' in 'New-AzAksCluster' from 'AvailabilitySet' to 'VirtualMachineScaleSets'.</span></span>
* <span data-ttu-id="af695-111">[Yeni Değişiklik] 'New-AzAksCluster' cmdlet’indeki 'NetworkPlugin' parametresinin 'None' varsayılan değeri 'azure' olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-111">[Breaking Change] Changed the default value of 'NetworkPlugin' in 'New-AzAksCluster' from 'None' to 'azure'.</span></span>
* <span data-ttu-id="af695-112">[Yeni Değişiklik] Linux’ta yalnızca bir değeri desteklediğinden 'New-AzAksCluster' cmdlet’indeki 'NodeOsType' parametresi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="af695-112">[Breaking Change] Removed parameter 'NodeOsType' in 'New-AzAksCluster' as it supports only one value Linux.</span></span>

#### <a name="azbilling"></a><span data-ttu-id="af695-113">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="af695-113">Az.Billing</span></span>
* <span data-ttu-id="af695-114">'Get-AzBillingAccount' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-114">Added 'Get-AzBillingAccount' cmdlet</span></span>
* <span data-ttu-id="af695-115">'Get-AzBillingProfile' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-115">Added 'Get-AzBillingProfile' cmdlet</span></span>
* <span data-ttu-id="af695-116">'Get-AzInvoiceSection' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-116">Added 'Get-AzInvoiceSection' cmdlet</span></span>
* <span data-ttu-id="af695-117">'Get-AzBillingInvoice' cmdlet’ine yeni parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-117">Added new parameters in 'Get-AzBillingInvoice' cmdlet</span></span>
* <span data-ttu-id="af695-118">Get-AzBillingInvoice cmdlet’inin yanıtından DownloadUrlExpiry, Type ve BillingPeriodNames özellikleri kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="af695-118">Removed properties DownloadUrlExpiry, Type, BillingPeriodNames from the response of Get-AzBillingInvoice cmdlet</span></span>

#### <a name="azcdn"></a><span data-ttu-id="af695-119">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="af695-119">Az.Cdn</span></span>
* <span data-ttu-id="af695-120">Çoklu kaynak ve özel bağlantı işlevini destekleyecek cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-120">Added cmdlets to support multi-origin and private link functionality</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="af695-121">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="af695-121">Az.CognitiveServices</span></span>
* <span data-ttu-id="af695-122">SDK sürümü 7.4.0-preview olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-122">Updated SDK to 7.4.0-preview.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="af695-123">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="af695-123">Az.Compute</span></span>
* <span data-ttu-id="af695-124">'New-AzVm' cmdlet’ine '-VmssId' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-124">Added '-VmssId' parameter to 'New-AzVm'</span></span>
* <span data-ttu-id="af695-125">'New-AzVmss' cmdlet’ine 'PlatformFaultDomainCount' parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-125">Added 'PlatformFaultDomainCount' parameter to the 'New-AzVmss' cmdlet.</span></span>
* <span data-ttu-id="af695-126">Yeni 'Get-AzDiskEncryptionSetAssociatedResource' cmdlet’i</span><span class="sxs-lookup"><span data-stu-id="af695-126">New cmdlet 'Get-AzDiskEncryptionSetAssociatedResource'</span></span>
* <span data-ttu-id="af695-127">New-AzDiskConfig cmdlet’ine isteğe bağlı 'Tier' ve 'LogicalSectorSize' parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-127">Added 'Tier' and 'LogicalSectorSize' optional parameters to the New-AzDiskConfig cmdlet.</span></span> 
* <span data-ttu-id="af695-128">'New-AzDiskUpdateConfig' cmdlet’ine 'Tier', 'MaxSharesCount', 'DiskIOPSReadOnly' ve 'DiskMBpsReadOnly' eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-128">Added 'Tier', 'MaxSharesCount', 'DiskIOPSReadOnly', and 'DiskMBpsReadOnly' optional parameters to the 'New-AzDiskUpdateConfig' cmdlet.</span></span> 

#### <a name="azcontainerregistry"></a><span data-ttu-id="af695-129">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="af695-129">Az.ContainerRegistry</span></span>
* <span data-ttu-id="af695-130">[Yeni Değişiklik] API sürümü 2020-05-01 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-130">[Breaking Change] Updates API version to 2020-05-01</span></span>
* <span data-ttu-id="af695-131">[Yeni Değişiklik] 'New-AzContainerRegistry' cmdlet’inden 'Classic' SKU’su ve 'StorageAccountName' parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="af695-131">[Breaking Change] Removed SKU 'Classic' and parameter 'StorageAccountName' from 'New-AzContainerRegistry'</span></span>
* <span data-ttu-id="af695-132">Yeni cmdlet’ler eklendi: 'Connect-AzContainerRegistry', 'Import-AzContainerRegistry', 'Get-AzContainerRegistryUsage', 'New-AzContainerRegistryNetworkRule', 'Set-AzContainerRegistryNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="af695-132">Added New cmdlets: 'Connect-AzContainerRegistry', 'Import-AzContainerRegistry', 'Get-AzContainerRegistryUsage', 'New-AzContainerRegistryNetworkRule', 'Set-AzContainerRegistryNetworkRule'</span></span>
* <span data-ttu-id="af695-133">'Update-AzContainerRegistry' cmdlet’ine yeni 'NetworkRuleSet' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-133">Added new parameter 'NetworkRuleSet' to 'Update-AzContainerRegistry'</span></span>

#### <a name="azdatabricks"></a><span data-ttu-id="af695-134">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="af695-134">Az.Databricks</span></span>
* <span data-ttu-id="af695-135">`-EncryptionKeyVersion` başarısız olmadan Databricks çalışma alanını güncelleştirmeye neden olabilecek bir hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-135">Fixed a bug that may cause updating databricks workspace without `-EncryptionKeyVersion` to fail.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="af695-136">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="af695-136">Az.DataFactory</span></span>
* <span data-ttu-id="af695-137">ADF .NET SDK’sı 4.12.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-137">Updated ADF .Net SDK version to 4.12.0</span></span>
* <span data-ttu-id="af695-138">ADF şifrelemesi istemci SDK’sı 4.14.7587.7 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-138">Updated ADF encryption client SDK version to 4.14.7587.7</span></span>
* <span data-ttu-id="af695-139">'Stop-AzDataFactoryV2TriggerRun' ve 'Invoke-AzDataFactoryV2TriggerRun' komutları eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-139">Added 'Stop-AzDataFactoryV2TriggerRun' and 'Invoke-AzDataFactoryV2TriggerRun' commands</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="af695-140">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="af695-140">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="af695-141">Üst düzey ARM nesneleri oluşturmak için Location özelliği gerekli kılındı.</span><span class="sxs-lookup"><span data-stu-id="af695-141">Require Location property for creating top level arm objects.</span></span>
        <span data-ttu-id="af695-142">\* `New-AzWvdApplicationGroup` için `ApplicationGroupType` gerekli kılındı.</span><span class="sxs-lookup"><span data-stu-id="af695-142">\* Made `ApplicationGroupType` required for `New-AzWvdApplicationGroup`.</span></span>
        <span data-ttu-id="af695-143">\* `New-AzWvdApplicationGroup` için `HostPoolArmPath` gerekli kılındı.</span><span class="sxs-lookup"><span data-stu-id="af695-143">\* Made `HostPoolArmPath` required for `New-AzWvdApplicationGroup`.</span></span>
        <span data-ttu-id="af695-144">\* `New-AzWvdHostPool` cmdlet’ine `PreferredAppGroupType` eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-144">\* Added `PreferredAppGroupType` for `New-AzWvdHostPool`.</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="af695-145">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="af695-145">Az.Functions</span></span>
* <span data-ttu-id="af695-146">[Yeni Değişiklik] 'IncludeSlot' anahtar parametresi, 'Get-AzFunctionApp' cmdlet’inin parametre kümelerinden biri hariç tümünden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="af695-146">[Breaking Change] Removed 'IncludeSlot' switch parameter from all but one parameter set of 'Get-AzFunctionApp'.</span></span> <span data-ttu-id="af695-147">Cmdlet, şimdi '-IncludeSlot' belirtildiğinde sonuçlarda dağıtım yuvalarının alınmasını destekliyor.</span><span class="sxs-lookup"><span data-stu-id="af695-147">The cmdlet now supports retrieving deployment slots in the results when '-IncludeSlot' is specified.</span></span> 
* <span data-ttu-id="af695-148">'New-AzFunctionApp' güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="af695-148">Updated 'New-AzFunctionApp':</span></span>
  - <span data-ttu-id="af695-149">-DisableApplicationInsights, bu seçenek belirtildiğinde hiçbir Application Insights projesi oluşturulmayacak şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-149">Fixed -DisableApplicationInsights so that no application insights project is created when this option is specified.</span></span> <span data-ttu-id="af695-150">[#12728]</span><span class="sxs-lookup"><span data-stu-id="af695-150">[#12728]</span></span>
  - <span data-ttu-id="af695-151">[Yeni Değişiklik] PowerShell 6.2 işlev uygulamaları oluşturma desteği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="af695-151">[Breaking Change] Removed support to create PowerShell 6.2 function apps.</span></span>
  - <span data-ttu-id="af695-152">[Yeni Değişiklik] RuntimeVersion parametresi belirtilmediğinde, PowerShell işlev uygulamaları için Windows üzerinde İşlevler sürüm 3’teki varsayılan çalışma zamanı 6.2 sürümünden 7.0 sürümüne yükseltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-152">[Breaking Change] Changed the default runtime version in Functions version 3 on Windows for PowerShell function apps from 6.2 to 7.0 when the RuntimeVersion parameter is not specified.</span></span>
  - <span data-ttu-id="af695-153">[Yeni Değişiklik] RuntimeVersion parametresi belirtilmediğinde, Node işlev uygulamaları için Windows ve Linux üzerinde sürüm 3’teki varsayılan çalışma zamanı 10 sürümünden 12 sürümüne yükseltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-153">[Breaking Change] Changed the default runtime version in Functions version 3 on Windows and Linux for Node function apps from 10 to 12 when the RuntimeVersion parameter is not specified.</span></span>
  - <span data-ttu-id="af695-154">[Yeni Değişiklik] RuntimeVersion parametresi belirtilmediğinde, Python işlev uygulamaları için Linux üzerinde sürüm 3’teki varsayılan çalışma zamanı 3.7 sürümünden 3.8 sürümüne yükseltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-154">[Breaking Change] Changed the default runtime version in Functions version 3 on Linux for Python function apps from 3.7 to 3.8 when the RuntimeVersion parameter is not specified.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="af695-155">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="af695-155">Az.HDInsight</span></span>
 * <span data-ttu-id="af695-156">New-AzHDInsightCluster cmdlet’inde:</span><span class="sxs-lookup"><span data-stu-id="af695-156">For New-AzHDInsightCluster cmdlet:</span></span>
     - <span data-ttu-id="af695-157">'DefaultStorageAccountName' parametresi 'StorageAccountResourceId' ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-157">Replaced parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
     - <span data-ttu-id="af695-158">'DefaultStorageAccountKey' parametresi 'StorageAccountKey' ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-158">Replaced parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
     - <span data-ttu-id="af695-159">'DefaultStorageAccountType' parametresi 'StorageAccountType' ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-159">Replaced parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
     - <span data-ttu-id="af695-160">'PublicNetworkAccessType' parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="af695-160">Removed parameter 'PublicNetworkAccessType'</span></span>
     - <span data-ttu-id="af695-161">'OutboundPublicNetworkAccessType' parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="af695-161">Removed parameter 'OutboundPublicNetworkAccessType'</span></span>
     - <span data-ttu-id="af695-162">Yeni parametreler eklendi: ADLS 2. Nesil’i desteklemek üzere 'StorageFileSystem' ve 'StorageAccountManagedIdentity' eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-162">Added new parameters: 'StorageFileSystem' and 'StorageAccountManagedIdentity' to support ADLSGen2</span></span>
     - <span data-ttu-id="af695-163">HDInsight Kimlik Aracısını desteklemek üzere yeni 'EnableIDBroker' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-163">Added new parameter 'EnableIDBroker' to Support HDInsight ID Broker</span></span>
     - <span data-ttu-id="af695-164">Yeni parametreler eklendi: Kafka REST Proxy’yi desteklemek üzere 'KafkaClientGroupId', 'KafkaClientGroupName' ve 'KafkaManagementNodeSize' eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-164">Added new parameters: 'KafkaClientGroupId', 'KafkaClientGroupName' and 'KafkaManagementNodeSize' to support Kafka Rest Proxy</span></span>
 * <span data-ttu-id="af695-165">New-AzHDInsightClusterConfig cmdlet’inde:</span><span class="sxs-lookup"><span data-stu-id="af695-165">For New-AzHDInsightClusterConfig cmdlet:</span></span>
     - <span data-ttu-id="af695-166">'DefaultStorageAccountName' parametresi 'StorageAccountResourceId' ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-166">Replaced parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
     - <span data-ttu-id="af695-167">'DefaultStorageAccountKey' parametresi 'StorageAccountKey' ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-167">Replaced parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
     - <span data-ttu-id="af695-168">'DefaultStorageAccountType' parametresi 'StorageAccountType' ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-168">Replaced parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
     - <span data-ttu-id="af695-169">'PublicNetworkAccessType' parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="af695-169">Removed parameter 'PublicNetworkAccessType'</span></span>
     - <span data-ttu-id="af695-170">'OutboundPublicNetworkAccessType' parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="af695-170">Removed parameter 'OutboundPublicNetworkAccessType'</span></span>
* <span data-ttu-id="af695-171">Set-AzHDInsightDefaultStorage cmdlet’inde:</span><span class="sxs-lookup"><span data-stu-id="af695-171">For Set-AzHDInsightDefaultStorage cmdlet:</span></span>
    - <span data-ttu-id="af695-172">'StorageAccountName' parametresi 'StorageAccountResourceId' ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-172">Replaced parameter 'StorageAccountName' with 'StorageAccountResourceId'</span></span>
* <span data-ttu-id="af695-173">Add-AzHDInsightSecurityProfile cmdlet’inde:</span><span class="sxs-lookup"><span data-stu-id="af695-173">For Add-AzHDInsightSecurityProfile cmdlet:</span></span>
    - <span data-ttu-id="af695-174">'Domain' parametresi 'DomainResourceId' ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-174">Replaced parameter 'Domain' with 'DomainResourceId'</span></span>
    - <span data-ttu-id="af695-175">'OrganizationalUnitDN' parametresi için zorunlu gereksinim kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="af695-175">Removed the mandatory requirement for parameter 'OrganizationalUnitDN'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="af695-176">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="af695-176">Az.KeyVault</span></span>
* <span data-ttu-id="af695-177">[Yeni Değişiklik] 'New-AzKeyVault' cmdlet’indeki DisableSoftDelete ve 'Update-AzKeyVault' cmdlet’indeki EnableSoftDelete parametreleri kullanımdan kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="af695-177">[Breaking Change] Deprecated parameter DisableSoftDelete in 'New-AzKeyVault' and EnableSoftDelete in 'Update-AzKeyVault'</span></span>
* <span data-ttu-id="af695-178">[Yeni Değişiklik] Doğrudan SecretValue değerinin görüntülenmesini önlemek amacıyla SecretValueText özniteliği kaldırıldı [#12266]</span><span class="sxs-lookup"><span data-stu-id="af695-178">[Breaking Change] Removed attribute SecretValueText to avoid displaying SecretValue directly [#12266]</span></span>
* <span data-ttu-id="af695-179">Şu yeni kaynak türü için destek eklendi: yönetilen HSM</span><span class="sxs-lookup"><span data-stu-id="af695-179">Supported new resource type: managed HSM</span></span>
    - <span data-ttu-id="af695-180">Yönetilen HSM’deki anahtarları çalıştırmaya yönelik, yönetilen HSM ve cmdlet’lerin CRUD’si</span><span class="sxs-lookup"><span data-stu-id="af695-180">CRUD of managed HSM and cmdlets to operate keys on managed HSM</span></span>
    - <span data-ttu-id="af695-181">Tam HSM yedeklemesi/geri yüklemesi, AES anahtarı oluşturma, güvenlik etki alanı yedeklemesi/geri yüklemesi, RBAC</span><span class="sxs-lookup"><span data-stu-id="af695-181">Full HSM backup/restore, AES key creation, security domain backup/restore, RBAC</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="af695-182">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="af695-182">Az.ManagedServices</span></span>
* <span data-ttu-id="af695-183">[Yeni Değişiklik] Parametrelerin adlandırma kuralları ve ilişkili örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-183">[Breaking Change] Updated parameters naming conventions and associated examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="af695-184">Az.Network</span><span class="sxs-lookup"><span data-stu-id="af695-184">Az.Network</span></span>
* <span data-ttu-id="af695-185">[Yeni Değişiklik] 'HostedSubnet' parametresi kaldırıldı ve yerine 'Subnet' eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-185">[Breaking Change] Removed parameter 'HostedSubnet' and added 'Subnet' instead</span></span>
* <span data-ttu-id="af695-186">Sanal Yönlendirici Eş Düğüm Yolları için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-186">Added new cmdlets for Virtual Router Peer Routes</span></span>
    - <span data-ttu-id="af695-187">'Get-AzVirtualRouterPeerLearnedRoute'</span><span class="sxs-lookup"><span data-stu-id="af695-187">'Get-AzVirtualRouterPeerLearnedRoute'</span></span>
    - <span data-ttu-id="af695-188">'Get-AzVirtualRouterPeerAdvertisedRoute'</span><span class="sxs-lookup"><span data-stu-id="af695-188">'Get-AzVirtualRouterPeerAdvertisedRoute'</span></span>
* <span data-ttu-id="af695-189">New-AzFirewall cmdlet'i güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="af695-189">Updated New-AzFirewall cmdlet:</span></span>
    - <span data-ttu-id="af695-190">'-SkuTier' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-190">Added parameter '-SkuTier'</span></span>
    - <span data-ttu-id="af695-191">'-SkuName' parametresi eklendi ve bu parametreye yönelik SKU, Diğer Ad haline getirildi</span><span class="sxs-lookup"><span data-stu-id="af695-191">Added parameter '-SkuName' and made Sku as Alias for this</span></span>
    - <span data-ttu-id="af695-192">'-Sku' parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="af695-192">Removed parameter '-Sku'</span></span>
* <span data-ttu-id="af695-193">[Yeni Değişiklik] 'Start-AzVpnConnectionPacketCapture' ve 'Stop-AzVpnConnectionPacketCapture' cmdlet’lerinde 'Connectionlink' bağımsız değişkeni zorunlu kılındı</span><span class="sxs-lookup"><span data-stu-id="af695-193">[Breaking Change] Made 'Connectionlink' argument mandatory in 'Start-AzVpnConnectionPacketCapture' and 'Stop-AzVpnConnectionPacketCapture'</span></span>
* <span data-ttu-id="af695-194">[Yeni Değişiklik] 'New-AzNetworkWatcherConnectionMonitorEndPointObject', '-Filter' parametresi kaldırılacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-194">[Breaking Change] Updated 'New-AzNetworkWatcherConnectionMonitorEndPointObject' to remove parameter '-Filter'</span></span>
* <span data-ttu-id="af695-195">[Yeni Değişiklik] 'New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject' cmdlet’i 'New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject' ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-195">[Breaking Change] Replaced 'New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject' cmdlet with 'New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject'</span></span>
* <span data-ttu-id="af695-196">'New-AzNetworkWatcherConnectionMonitorEndPointObject' cmdlet’i güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="af695-196">Updated 'New-AzNetworkWatcherConnectionMonitorEndPointObject' cmdlet:</span></span>
    - <span data-ttu-id="af695-197">'-Type' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-197">Added parameter '-Type'</span></span>
    - <span data-ttu-id="af695-198">'-CoverageLevel' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-198">Added parameter '-CoverageLevel'</span></span>
    - <span data-ttu-id="af695-199">'-Scope' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-199">Added parameter '-Scope'</span></span>
* <span data-ttu-id="af695-200">'New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject' cmdlet’i yeni '-DestinationPortBehavior' parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-200">Updated 'New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject' cmdlet with new parameter '-DestinationPortBehavior'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="af695-201">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="af695-201">Az.RecoveryServices</span></span>
* <span data-ttu-id="af695-202">Katkıda bulunan izinleri için İş Yükü Geri Yüklemesi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-202">Fixing Workload Restore for contributor permissions.</span></span>
* <span data-ttu-id="af695-203">Restore-AzRecoveryServicesBackupItem cmdlet’ine yeni parametre kümeleri ve doğrulamalar eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-203">Added new parameter sets and validations for Restore-AzRecoveryServicesBackupItem cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="af695-204">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="af695-204">Az.Resources</span></span>
* <span data-ttu-id="af695-205">Ayrıştırma hataları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-205">Fixed parsing bug</span></span>
* <span data-ttu-id="af695-206">ARM şablonu What-If cmdlet’leri, sonuçlardan önizleme iletisi kaldırılacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-206">Updated ARM template What-If cmdlets to remove preview message from results</span></span>
* <span data-ttu-id="af695-207">'-WhatIf' cmdlet’i daha yüksek bir kapsama ayarlandığında, şablon dağıtım cmdlet’lerinin kilitlenmesiyle ilgili bir sorun düzeltildi [#13038]</span><span class="sxs-lookup"><span data-stu-id="af695-207">Fixed an issue where template deployment cmdlets crash if '-WhatIf' is set at a higher scope [#13038]</span></span>
* <span data-ttu-id="af695-208">Şablon dağıtım cmdlet’lerinin şablon parametrelerindeki büyük/küçük harfi korumamasıyla ilgili bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-208">Fixed an issue where template deployment cmdlets does not preserve case for template parameters</span></span>
* <span data-ttu-id="af695-209">'Export-AzResourceGroup' cmdlet’inde kullanılmak üzere varsayılan API sürümü eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-209">Added a default API version to be used in 'Export-AzResourceGroup' cmdlet</span></span>
* <span data-ttu-id="af695-210">Şablon Belirtimlerine yönelik cmdlet’ler ('Get-AzTemplateSpec', 'Set-AzTemplateSpec', 'New-AzTemplateSpec', 'Remove-AzTemplateSpec', 'Export-AzTemplateSpec') eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-210">Added cmdlets for Template Specs ('Get-AzTemplateSpec', 'Set-AzTemplateSpec', 'New-AzTemplateSpec', 'Remove-AzTemplateSpec', 'Export-AzTemplateSpec')</span></span>
* <span data-ttu-id="af695-211">Mevcut dağıtım cmdlet’lerini kullanarak (yeni -TemplateSpecId parametresi aracılığıyla) Şablon Belirtimlerini dağıtma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-211">Added support for deploying Template Specs using existing deployment cmdlets (via the new -TemplateSpecId parameter)</span></span> 
* <span data-ttu-id="af695-212">'Get-AzResourceGroupDeploymentOperation', SDK’yı kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-212">Updated 'Get-AzResourceGroupDeploymentOperation' to use the SDK.</span></span>
* <span data-ttu-id="af695-213">'\*-AzDeployment' cmdlet’lerinden '-ApiVersion' parametresi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="af695-213">Removed '-ApiVersion' parameter from '\*-AzDeployment' cmdlets.</span></span>

#### <a name="azsql"></a><span data-ttu-id="af695-214">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="af695-214">Az.Sql</span></span>
* <span data-ttu-id="af695-215">'Set-AzSqlDatabaseBackupShortTermRetentionPolicy' cmdlet’ine DiffBackupIntervalInHours eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-215">Added DiffBackupIntervalInHours to 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span> 
* <span data-ttu-id="af695-216">networkIsolation belirtilmediğinde New-AzSqlDatabaseExport cmdlet’inin başarısız olmasıyla ilgili sorun düzeltildi [#13097]</span><span class="sxs-lookup"><span data-stu-id="af695-216">Fixed issue where New-AzSqlDatabaseExport fails if networkIsolation not specified [#13097]</span></span>
* <span data-ttu-id="af695-217">New-AzSqlDatabaseExport ve New-AzSqlDatabaseImport cmdlet’lerinin sonuç nesnesinde OperationStatusLink parametresini döndürmemesiyle ilgili sorun düzeltildi [#13097]</span><span class="sxs-lookup"><span data-stu-id="af695-217">Fixed issue where New-AzSqlDatabaseExport and New-AzSqlDatabaseImport were not returning OperationStatusLink in the result object [#13097]</span></span>
* <span data-ttu-id="af695-218">Yedekleme Alanı Yedeklilik Uyarıları’ndaki Azure Eşlenmiş Bölgeler URL’si Güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-218">Update Azure Paired Regions URL in Backup Storage Redundancy Warnings</span></span> 

#### <a name="azstorage"></a><span data-ttu-id="af695-219">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="af695-219">Az.Storage</span></span>
* <span data-ttu-id="af695-220">Eski RestorePolicy.LastEnabledTime özelliği kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="af695-220">Removed obsolete property RestorePolicy.LastEnabledTime</span></span>
    - <span data-ttu-id="af695-221">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="af695-221">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="af695-222">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="af695-222">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="af695-223">'Get-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="af695-223">'Get-AzStorageBlobServiceProperty'</span></span>
    - <span data-ttu-id="af695-224">“Update-AzStorageBlobServiceProperty”</span><span class="sxs-lookup"><span data-stu-id="af695-224">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="af695-225">DaysAfterModificationGreaterThan parametresinin türü int yerine int? olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-225">Change Type of DaysAfterModificationGreaterThan from int to int?</span></span>
    - <span data-ttu-id="af695-226">'Set-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="af695-226">'Set-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="af695-227">'Get-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="af695-227">'Get-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="af695-228">'Add-AzStorageAccountManagementPolicyAction'</span><span class="sxs-lookup"><span data-stu-id="af695-228">'Add-AzStorageAccountManagementPolicyAction'</span></span>
    - <span data-ttu-id="af695-229">'New-AzStorageAccountManagementPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="af695-229">'New-AzStorageAccountManagementPolicyRule'</span></span>
* <span data-ttu-id="af695-230">Erişim katmanına sahip dosya paylaşımı oluşturma/güncelleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-230">Supported create/update file share with access tier</span></span>
    - <span data-ttu-id="af695-231">'New-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="af695-231">'New-AzRmStorageShare'</span></span>
    - <span data-ttu-id="af695-232">'Update-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="af695-232">'Update-AzRmStorageShare'</span></span>
* <span data-ttu-id="af695-233">Data Lake 2. Nesil’deki ACL’yi özyinelemeli olarak ayarlama/güncelleştirme/kaldırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-233">Supported set/update/remove Acl recursively on Datalake Gen2 item</span></span> 
    -  <span data-ttu-id="af695-234">'Set-AzDataLakeGen2AclRecursive'</span><span class="sxs-lookup"><span data-stu-id="af695-234">'Set-AzDataLakeGen2AclRecursive'</span></span> 
    -  <span data-ttu-id="af695-235">'Update-AzDataLakeGen2AclRecursive'</span><span class="sxs-lookup"><span data-stu-id="af695-235">'Update-AzDataLakeGen2AclRecursive'</span></span> 
    -  <span data-ttu-id="af695-236">'Remove-AzDataLakeGen2AclRecursive'</span><span class="sxs-lookup"><span data-stu-id="af695-236">'Remove-AzDataLakeGen2AclRecursive'</span></span>
* <span data-ttu-id="af695-237">Yeni x,t iznine sahip Kapsayıcı erişim ilkesi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-237">Supported Container access policy with new permission x,t</span></span>
    -  <span data-ttu-id="af695-238">'New-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="af695-238">'New-AzStorageContainerStoredAccessPolicy'</span></span>
    -  <span data-ttu-id="af695-239">'Set-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="af695-239">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
* <span data-ttu-id="af695-240">Permission alt özelliğinin türü enum’dan String’e değiştirilerek Kapsayıcı erişim ilkesi cmdlet’ini alma/ayarlama işleminin çıkışı değiştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-240">Changed the output of get/set Container access policy cmdlet, by change the child property Permission type from enum to String</span></span>
    -  <span data-ttu-id="af695-241">'Get-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="af695-241">'Get-AzStorageContainerStoredAccessPolicy'</span></span>
    -  <span data-ttu-id="af695-242">'Set-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="af695-242">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
* <span data-ttu-id="af695-243">JSON ile yönetim ilkesi ayarlamayla ilgili örnek betik sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-243">Fixed a sample script issue of set management policy with json</span></span>
    -  <span data-ttu-id="af695-244">'Set-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="af695-244">'Set-AzStorageAccountManagementPolicy'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="af695-245">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="af695-245">Az.Websites</span></span>
* <span data-ttu-id="af695-246">Premium V3 fiyatlandırma katmanı desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-246">Added support for Premium V3 pricing tier</span></span>
* <span data-ttu-id="af695-247">WebSites SDK 3.1.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-247">Updated the WebSites SDK to 3.1.0</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="af695-248">Topluluğumuzdan katkıda bulunanlara teşekkür ederiz</span><span class="sxs-lookup"><span data-stu-id="af695-248">Thanks to our community contributors</span></span>
* <span data-ttu-id="af695-249">@atul-ram, Get-AzDelegation.md güncelleştirildi (#13176)</span><span class="sxs-lookup"><span data-stu-id="af695-249">@atul-ram, Update Get-AzDelegation.md (#13176)</span></span>
* <span data-ttu-id="af695-250">@dineshreddy007, Stack HCI kaydının WAC belirtecini kullanması durumunda doğru atanan Uygulama Rolleri alınıyor.</span><span class="sxs-lookup"><span data-stu-id="af695-250">@dineshreddy007, Get the App Roles assigned correctly in case of Stack HCI registration using WAC token.</span></span> <span data-ttu-id="af695-251">(#13249)</span><span class="sxs-lookup"><span data-stu-id="af695-251">(#13249)</span></span>
* <span data-ttu-id="af695-252">@kongou-ae, New-AzOffice365PolicyProperty.md güncelleştirildi (#13217)</span><span class="sxs-lookup"><span data-stu-id="af695-252">@kongou-ae, Update New-AzOffice365PolicyProperty.md (#13217)</span></span>
* <span data-ttu-id="af695-253">Lohith Chowdary Chilukuri (@Lochiluk), Set-AzApplicationGateway.md güncelleştirildi (#13150)</span><span class="sxs-lookup"><span data-stu-id="af695-253">Lohith Chowdary Chilukuri (@Lochiluk), Update Set-AzApplicationGateway.md (#13150)</span></span>
* <span data-ttu-id="af695-254">Matthew Burleigh (@mburleigh)</span><span class="sxs-lookup"><span data-stu-id="af695-254">Matthew Burleigh (@mburleigh)</span></span>
  * <span data-ttu-id="af695-255">Belgede başvurulan PowerShell cmdlet’lerine bağlantılar eklendi (#13203)</span><span class="sxs-lookup"><span data-stu-id="af695-255">Add links to PowerShell cmdlets referenced in the document (#13203)</span></span>
  * <span data-ttu-id="af695-256">Belgede başvurulan PowerShell cmdlet’lerine bağlantılar eklendi (#13190)</span><span class="sxs-lookup"><span data-stu-id="af695-256">Add links to PowerShell cmdlets referenced in the document (#13190)</span></span>
  * <span data-ttu-id="af695-257">Belgede başvurulan PowerShell cmdlet’lerine bağlantılar eklendi (#13189)</span><span class="sxs-lookup"><span data-stu-id="af695-257">Add links to PowerShell cmdlets referenced in the document (#13189)</span></span>
  * <span data-ttu-id="af695-258">Başvurulan cmdlet’lere bağlantılar eklendi (#13137)</span><span class="sxs-lookup"><span data-stu-id="af695-258">add links to referenced cmdlets (#13137)</span></span>
  * <span data-ttu-id="af695-259">Belgede başvurulan PowerShell cmdlet’lerine bağlantılar eklendi (#13204)</span><span class="sxs-lookup"><span data-stu-id="af695-259">Add links to PowerShell cmdlets referenced in the document (#13204)</span></span>
  * <span data-ttu-id="af695-260">Belgede başvurulan PowerShell cmdlet’lerine bağlantılar eklendi (#13205)</span><span class="sxs-lookup"><span data-stu-id="af695-260">Add links to PowerShell cmdlets referenced in the document (#13205)</span></span>

## <a name="480---october-2020"></a><span data-ttu-id="af695-261">4.8.0 - Ekim 2020</span><span class="sxs-lookup"><span data-stu-id="af695-261">4.8.0 - October 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="af695-262">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="af695-262">Az.Accounts</span></span>
* <span data-ttu-id="af695-263">Ortak kitaplıklardaki DateTime ayrıştırma sorunu düzeltildi [#13045]</span><span class="sxs-lookup"><span data-stu-id="af695-263">Fixed DateTime parse issue in common libraries [#13045]</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="af695-264">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="af695-264">Az.CognitiveServices</span></span>
* <span data-ttu-id="af695-265">'New-AzCognitiveServicesAccountApiProperty' cmdlet'i eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-265">Added 'New-AzCognitiveServicesAccountApiProperty' cmdlet.</span></span>
* <span data-ttu-id="af695-266">'New-AzCognitiveServicesAccount' ve 'Set-AzCognitiveServicesAccount' için 'ApiProperty' parametresi destekleniyor</span><span class="sxs-lookup"><span data-stu-id="af695-266">Supported 'ApiProperty' parameter for 'New-AzCognitiveServicesAccount' and 'Set-AzCognitiveServicesAccount'</span></span>

#### <a name="azcompute"></a><span data-ttu-id="af695-267">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="af695-267">Az.Compute</span></span>
* <span data-ttu-id="af695-268">'Update-ASRRecoveryPlan' cmdlet'indeki sorun Yük Devretme Türleri doldurularak düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-268">Fixed issue in 'Update-ASRRecoveryPlan' by populating FailoverTypes</span></span>
* <span data-ttu-id="af695-269">'Get-AzVmImage' cmdlet'ine isteğe bağlı '-Top' ve '-OrderBy' parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-269">Added the '-Top' and '-OrderBy' optional parameters to the 'Get-AzVmImage' cmdlet.</span></span> 

#### <a name="azdatabricks"></a><span data-ttu-id="af695-270">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="af695-270">Az.Databricks</span></span>
* <span data-ttu-id="af695-271">'Az.Databricks' modülü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="af695-271">General availability of 'Az.Databricks' module</span></span>
* <span data-ttu-id="af695-272">Sanal ağ eşlemesi için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-272">Added support for virtual network peering</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="af695-273">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="af695-273">Az.DataFactory</span></span>
* <span data-ttu-id="af695-274">Çıkış iletilerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-274">Fixed typo in output messages</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="af695-275">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="af695-275">Az.EventHub</span></span>
* <span data-ttu-id="af695-276">'Set-AzEventHubNetworkRuleSet' cmdlet'ine isteğe bağlı 'TrustedServiceAccessEnabled' anahtar parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-276">Added optional switch parameter 'TrustedServiceAccessEnabled' to 'Set-AzEventHubNetworkRuleSet' cmdlet</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="af695-277">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="af695-277">Az.HDInsight</span></span>
* <span data-ttu-id="af695-278">'PublicNetworkAccessType' ve 'OutboundPublicNetworkAccessType' parametrelerini kullanımdan kaldırma planlaması için uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-278">Added warning message for planning to deprecate the parameters 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType'</span></span>
* <span data-ttu-id="af695-279">'DefaultStorageAccountName' parametresini 'StorageAccountResourceId' ile değiştirme planlaması için uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-279">Added warning message for planning to replace the parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
* <span data-ttu-id="af695-280">'DefaultStorageAccountKey' parametresini 'StorageAccountKey' ile değiştirme planlaması için uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-280">Added warning message for planning to replace the parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
* <span data-ttu-id="af695-281">'DefaultStorageAccountType' parametresini 'StorageAccountType' ile değiştirme planlaması için uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-281">Added warning message for planning to replace the parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
* <span data-ttu-id="af695-282">'DefaultStorageContainer' parametresini 'StorageContainer' ile değiştirme planlaması için uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-282">Added warning message for planning to replace the parameter 'DefaultStorageContainer' with 'StorageContainer'</span></span>
* <span data-ttu-id="af695-283">'DefaultStorageRootPath' parametresini 'StorageRootPath' ile değiştirme planlaması için uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-283">Added warning message for planning to replace the parameter 'DefaultStorageRootPath' with 'StorageRootPath'</span></span>

#### <a name="aziothub"></a><span data-ttu-id="af695-284">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="af695-284">Az.IotHub</span></span>
* <span data-ttu-id="af695-285">Cihazların sdk'sı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-285">Updated devices sdk.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="af695-286">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="af695-286">Az.KeyVault</span></span>
* <span data-ttu-id="af695-287">SecretValueText özelliğinin kaldırılacağı ayrıntılı tarih sağlandı</span><span class="sxs-lookup"><span data-stu-id="af695-287">Provided the detailed date of removing property SecretValueText</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="af695-288">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="af695-288">Az.ManagedServices</span></span>
* <span data-ttu-id="af695-289">Yönetilen hizmet atama ve tanım cmdlet’lerine hataya neden olan değişiklik uyarıları güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-289">Updated breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="af695-290">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="af695-290">Az.Monitor</span></span>
* <span data-ttu-id="af695-291">Uyarı iletisinin gizlenememesi hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-291">Fixed the bug that warning message cannot be suppressed.</span></span> <span data-ttu-id="af695-292">[#12889]</span><span class="sxs-lookup"><span data-stu-id="af695-292">[#12889]</span></span>
* <span data-ttu-id="af695-293">Uyarı kuralı ölçütlerinde 'SkipMetricValidation' parametresi destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="af695-293">Supported 'SkipMetricValidation' parameter in alert rule criteria.</span></span> <span data-ttu-id="af695-294">Ölçüm doğrulamasının atlanmasına neden olarak henüz yayılmamış özel bir ölçümle ilgili uyarı kuralı oluşturmaya olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="af695-294">Allows creating an alert rule on a custom metric that isn't yet emitted, by causing the metric validation to be skipped.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="af695-295">Az.Network</span><span class="sxs-lookup"><span data-stu-id="af695-295">Az.Network</span></span>
* <span data-ttu-id="af695-296">VPNSite Kaynağına Office365 İlkesi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-296">Added Office365 Policy to VPNSite Resource</span></span>
    - <span data-ttu-id="af695-297">'New-AzO365PolicyProperty'</span><span class="sxs-lookup"><span data-stu-id="af695-297">'New-AzO365PolicyProperty'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="af695-298">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="af695-298">Az.RecoveryServices</span></span>
* <span data-ttu-id="af695-299">İş yükü yedeklemesi için kapsayıcı adı doğrulaması eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-299">Added container name validation for workload backup.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="af695-300">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="af695-300">Az.RedisCache</span></span>
* <span data-ttu-id="af695-301">Microsoft.Cache RP kaydıyla ilgili izin sorunundan dolayı 'New-AzRedisCache' ve 'Set-AzRedisCache' cmdlet'lerinin başarısız olmaması sağlandı</span><span class="sxs-lookup"><span data-stu-id="af695-301">Made 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets not fail because of permission issue related to registering Microsoft.Cache RP</span></span>

#### <a name="azsql"></a><span data-ttu-id="af695-302">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="af695-302">Az.Sql</span></span>
* <span data-ttu-id="af695-303">Aşağıdakilere BackupStorageRedundancy eklendi:</span><span class="sxs-lookup"><span data-stu-id="af695-303">Added BackupStorageRedundancy to the following:</span></span> 
    - <span data-ttu-id="af695-304">'Restore-AzureRmSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="af695-304">'Restore-AzureRmSqlDatabase'</span></span>
    - <span data-ttu-id="af695-305">'New-AzSqlDatabaseCopy'</span><span class="sxs-lookup"><span data-stu-id="af695-305">'New-AzSqlDatabaseCopy'</span></span>
    - <span data-ttu-id="af695-306">'New-AzSqlDatabaseSecondary'</span><span class="sxs-lookup"><span data-stu-id="af695-306">'New-AzSqlDatabaseSecondary'</span></span>
* <span data-ttu-id="af695-307">Tüm SQL DB başvurularında BackupStorageRedundancy parametresi için büyük/küçük harf duyarlılığı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="af695-307">Removed case sensitivity for BackupStorageRedundancy parameter for all SQL DB references</span></span> 
* <span data-ttu-id="af695-308">BackupStorageRedundancy uyarı iletisi adları güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-308">Updated BackupStorageRedundancy warning message names</span></span>

#### <a name="azstorage"></a><span data-ttu-id="af695-309">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="af695-309">Az.Storage</span></span>
* <span data-ttu-id="af695-310">Depolama hesabının dosya hizmetinde paylaşımı etkinleştirme/devre dışı bırakma/alma geçici silme özellikleri destekleniyor</span><span class="sxs-lookup"><span data-stu-id="af695-310">Supported enable/disable/get share soft delete properties on file Service of a Storage account</span></span>
    - <span data-ttu-id="af695-311">'Update-AzStorageFileServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="af695-311">'Update-AzStorageFileServiceProperty'</span></span>
    - <span data-ttu-id="af695-312">'Get-AzStorageFileServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="af695-312">'Get-AzStorageFileServiceProperty'</span></span>
* <span data-ttu-id="af695-313">Desteklenen liste dosya paylaşımları Depolama hesabının silinmiş olan dosyalarını içeriyor ve Tek dosya paylaşımı kullanımı alınıyor</span><span class="sxs-lookup"><span data-stu-id="af695-313">Supported list file shares include the deleted ones of a Storage account, and Get single file share usage</span></span>
    - <span data-ttu-id="af695-314">'Get-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="af695-314">'Get-AzRmStorageShare'</span></span>
* <span data-ttu-id="af695-315">Silinmiş dosya paylaşımını geri yükleme destekleniyor</span><span class="sxs-lookup"><span data-stu-id="af695-315">Supported restore a deleted file share</span></span>
    - <span data-ttu-id="af695-316">'Restore-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="af695-316">'Restore-AzRmStorageShare'</span></span>
* <span data-ttu-id="af695-317">Blob hizmeti özelliklerini değiştirmeye yönelik cmdlet'ler değiştirildi. Sunucudan ilk özellikler alınmayacak, yalnızca değiştirilen özellikler sunucuya ayarlanacak.</span><span class="sxs-lookup"><span data-stu-id="af695-317">Changed the cmdlets for modify blob service properties, won't get the original properties from server, but only set the modified properties to server.</span></span>
    - <span data-ttu-id="af695-318">'Enable-AzStorageBlobDeleteRetentionPolicy'</span><span class="sxs-lookup"><span data-stu-id="af695-318">'Enable-AzStorageBlobDeleteRetentionPolicy'</span></span>
    - <span data-ttu-id="af695-319">'Disable-AzStorageBlobDeleteRetentionPolicy'</span><span class="sxs-lookup"><span data-stu-id="af695-319">'Disable-AzStorageBlobDeleteRetentionPolicy'</span></span>  
    - <span data-ttu-id="af695-320">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="af695-320">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="af695-321">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="af695-321">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="af695-322">“Update-AzStorageBlobServiceProperty”</span><span class="sxs-lookup"><span data-stu-id="af695-322">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="af695-323">New-AzStorageAccount parametresi -Kind varsayılan değeri için yardım sorunu düzeltildi [#12189]</span><span class="sxs-lookup"><span data-stu-id="af695-323">Fixed help issue for New-AzStorageAccount parameter -Kind default value [#12189]</span></span>
* <span data-ttu-id="af695-324">Blob karşıya yüklemesinde doğru ContentType ayarlama işlemini göstermek için örnek eklenerek sorun düzeltildi [#12989]</span><span class="sxs-lookup"><span data-stu-id="af695-324">Fixed issue by add example to show how to set correct ContentType in blob upload [#12989]</span></span>

## <a name="470---september-2020"></a><span data-ttu-id="af695-325">4.7.0 - Eylül 2020</span><span class="sxs-lookup"><span data-stu-id="af695-325">4.7.0 - September 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="af695-326">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="af695-326">Az.Accounts</span></span>
* <span data-ttu-id="af695-327">Yaklaşan yeni değişiklik iletileri biçimlendirildi</span><span class="sxs-lookup"><span data-stu-id="af695-327">Formatted the upcoming breaking change messages</span></span>
* <span data-ttu-id="af695-328">Azure.Core 1.4.1 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-328">Updated Azure.Core to 1.4.1</span></span>

#### <a name="azaks"></a><span data-ttu-id="af695-329">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="af695-329">Az.Aks</span></span>
* <span data-ttu-id="af695-330">'New-AzAksCluster', 'Set-AzAksCluster' ve 'New-AzAksNodePool' için istemci tarafı parametre doğrulama mantığı eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-330">Added client side parameter validation logic for 'New-AzAksCluster', 'Set-AzAksCluster' and 'New-AzAksNodePool'.</span></span> <span data-ttu-id="af695-331">[#12372]</span><span class="sxs-lookup"><span data-stu-id="af695-331">[#12372]</span></span>
* <span data-ttu-id="af695-332">'New-AzAksCluster' cmdlet’inde eklentilere yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-332">Added support for add-ons in 'New-AzAksCluster'.</span></span> <span data-ttu-id="af695-333">[#11239]</span><span class="sxs-lookup"><span data-stu-id="af695-333">[#11239]</span></span>
* <span data-ttu-id="af695-334">Eklentiler için 'Enable-AzAksAddOn' ve 'Disable-AzAksAddOn' cmdlet’leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-334">Added cmdlets 'Enable-AzAksAddOn' and 'Disable-AzAksAddOn' for add-ons.</span></span> <span data-ttu-id="af695-335">[#11239]</span><span class="sxs-lookup"><span data-stu-id="af695-335">[#11239]</span></span>
* <span data-ttu-id="af695-336">'New-AzAksCluster' için 'GenerateSshKey' parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-336">Added parameter 'GenerateSshKey' for 'New-AzAksCluster'.</span></span> <span data-ttu-id="af695-337">[#12371]</span><span class="sxs-lookup"><span data-stu-id="af695-337">[#12371]</span></span>
* <span data-ttu-id="af695-338">API sürümü 2020-06-01 olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-338">Updated api version to 2020-06-01.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="af695-339">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="af695-339">Az.CognitiveServices</span></span>
* <span data-ttu-id="af695-340">Belirli API’ler için ek yasal koşullar gösterildi.</span><span class="sxs-lookup"><span data-stu-id="af695-340">Showed additional legal terms for certain APIs.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="af695-341">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="af695-341">Az.Compute</span></span>
* <span data-ttu-id="af695-342">'New-AzVmDiskEncryptionSetConfig' için isteğe bağlı '-EncryptionType' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-342">Added the '-EncryptionType' optional parameter to 'New-AzVmDiskEncryptionSetConfig'</span></span>
* <span data-ttu-id="af695-343">Yeni kaynak türü için yeni cmdlet’ler: DiskAccess 'Get-AzDiskAccess', 'New-AzDiskAccess', 'Get-AzDiskAccess'</span><span class="sxs-lookup"><span data-stu-id="af695-343">New cmdlets for new resource type: DiskAccess 'Get-AzDiskAccess', 'New-AzDiskAccess', 'Get-AzDiskAccess'</span></span>
* <span data-ttu-id="af695-344">'New-AzSnapshotConfig' cmdlet’ine isteğe bağlı '-DiskAccessId' ve '-NetworkAccessPolicy' parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-344">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzSnapshotConfig'</span></span>
* <span data-ttu-id="af695-345">'New-AzDiskConfig' cmdlet’ine isteğe bağlı '-DiskAccessId' ve '-NetworkAccessPolicy' parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-345">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzDiskConfig'</span></span>
* <span data-ttu-id="af695-346">VirtualMachine Örnek Görünümüne 'PatchStatus' özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-346">Added 'PatchStatus' property to VirtualMachine Instance View</span></span>
* <span data-ttu-id="af695-347">'Get-AzVm' cmdlet’i '-Status' ile çağrıldığında döndürülen nesne olan 'VMHealth' özelliği, sanal makinenin örnek görünümüne eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-347">Added 'VMHealth' property to the virtual machine's instance view, which is the returned object when 'Get-AzVm' is invoked with '-Status'</span></span>
* <span data-ttu-id="af695-348">'Get-AzVM' ve 'Get-AzVmss' örnek görünümlerine 'AssignedHost' alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-348">Added 'AssignedHost' field to 'Get-AzVM' and 'Get-AzVmss' instance views.</span></span> <span data-ttu-id="af695-349">Alan, sanal makine örneğinin kaynak kimliğini gösterir</span><span class="sxs-lookup"><span data-stu-id="af695-349">The field shows the resource id of the virtual machine instance</span></span>
* <span data-ttu-id="af695-350">'New-AzHostGroup' cmdlet’ine isteğe bağlı '-SupportAutomaticPlacement' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-350">Added optional parameter '-SupportAutomaticPlacement' to 'New-AzHostGroup'</span></span> 
* <span data-ttu-id="af695-351">'New-AzVm' ve 'New-AzVmss' cmdlet’lerine '-HostGroupId' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-351">Added the '-HostGroupId' parameter to 'New-AzVm' and 'New-AzVmss'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="af695-352">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="af695-352">Az.DataFactory</span></span>
* <span data-ttu-id="af695-353">ADF .NET SDK’sı 4.11.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-353">Updated ADF .Net SDK version to 4.11.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="af695-354">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="af695-354">Az.EventHub</span></span>
* <span data-ttu-id="af695-355">Yeni 'New-AzEventHubCluster', 'Set-AzEventHubCluster', 'Get-AzEventHubCluster', 'Remove-AzEventHubCluster', 'Get-AzEventHubClustersAvailableRegions' Cluster cmdlet’leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-355">Added new Cluster cmdlets - 'New-AzEventHubCluster', 'Set-AzEventHubCluster', 'Get-AzEventHubCluster', 'Remove-AzEventHubCluster', 'Get-AzEventHubClustersAvailableRegions'.</span></span>
* <span data-ttu-id="af695-356">#10722 numaralı soruna yönelik aşağıdaki düzeltmeler yapıldı: AuthorizationRule haklarına yalnızca 'Listen' atanabilecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-356">Fixed for issue #10722 : Fix for assigning only 'Listen' to AuthorizationRule rights.</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="af695-357">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="af695-357">Az.Functions</span></span>
* <span data-ttu-id="af695-358">Desteklemeyen bölgelerde v2 İşlevleri oluşturma özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="af695-358">Removed the ability to create v2 Functions in regions that do not support it.</span></span>
* <span data-ttu-id="af695-359">PowerShell 6.2 sürümü kullanımdan kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="af695-359">Deprecated PowerShell 6.2.</span></span> <span data-ttu-id="af695-360">Kullanıcı PowerShell 6.2 işlev uygulaması oluşturduğunda, bunun yerine PowerShell 7.0 işlev uygulaması oluşturmasını öneren bir uyarı eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-360">Added a warning for when a user creates a PowerShell 6.2 function app that advises them to create a PowerShell 7.0 function app instead.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="af695-361">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="af695-361">Az.HDInsight</span></span>
* <span data-ttu-id="af695-362">Otomatik ölçeklendirme yapılandırmasıyla küme oluşturma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-362">Supported creating cluster with Autoscale configuration</span></span>
    - <span data-ttu-id="af695-363">'New-AzHDInsightCluster' cmdlet’ine yeni 'AutoscaleConfiguration' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-363">Add new parameter 'AutoscaleConfiguration' to the cmdlet 'New-AzHDInsightCluster'</span></span>
* <span data-ttu-id="af695-364">Kümenin Otomatik ölçeklendirme yapılandırmasını çalıştırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-364">Supported operating cluster's Autoscale configuration</span></span>
    - <span data-ttu-id="af695-365">Yeni 'Get-AzHDInsihgtClusterAutoscaleConfiguration' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-365">Add new cmdlet 'Get-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="af695-366">Yeni 'New-AzHDInsihgtClusterAutoscaleConfiguration' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-366">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="af695-367">Yeni 'Set-AzHDInsihgtClusterAutoscaleConfiguration' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-367">Add new cmdlet 'Set-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="af695-368">Yeni 'Remove-AzHDInsihgtClusterAutoscaleConfiguration' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-368">Add new cmdlet 'Remove-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="af695-369">Yeni 'New-AzHDInsihgtClusterAutoscaleScheduleCondition' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-369">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleScheduleCondition'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="af695-370">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="af695-370">Az.KeyVault</span></span>
* <span data-ttu-id="af695-371">RBAC yetkilendirmesi desteği eklendi [#10557]</span><span class="sxs-lookup"><span data-stu-id="af695-371">Added support for RBAC authorization [#10557]</span></span>
* <span data-ttu-id="af695-372">'Set-AzKeyVaultAccessPolicy' cmdlet’indeki hata işleme özelliği iyileştirildi [#4007]</span><span class="sxs-lookup"><span data-stu-id="af695-372">Enhanced error handling in 'Set-AzKeyVaultAccessPolicy' [#4007]</span></span>

#### <a name="azkusto"></a><span data-ttu-id="af695-373">Az.Kusto</span><span class="sxs-lookup"><span data-stu-id="af695-373">Az.Kusto</span></span>
* <span data-ttu-id="af695-374">'Az.Kusto' modülü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="af695-374">General availability of 'Az.Kusto' module</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="af695-375">Az.Network</span><span class="sxs-lookup"><span data-stu-id="af695-375">Az.Network</span></span>
* <span data-ttu-id="af695-376">[Yeni Değişiklik] Aşağıdaki cmdlet’ler, kaynak sanal yönlendiricisini ve sanal merkezi uyumlu hale getirecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-376">[Breaking Change] Updated below cmdlets to align resource virtual router and virtual hub</span></span>
    - <span data-ttu-id="af695-377">'New-AzVirtualRouter':</span><span class="sxs-lookup"><span data-stu-id="af695-377">'New-AzVirtualRouter':</span></span> 
        - <span data-ttu-id="af695-378">IP yapılandırması alt kaynağını desteklemek için -HostedSubnet parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-378">Added -HostedSubnet parameter to support IP configuration child resource</span></span>
        - <span data-ttu-id="af695-379">-HostedGateway ve -HostedGatewayId parametreleri silindi</span><span class="sxs-lookup"><span data-stu-id="af695-379">deleted -HostedGateway and -HostedGatewayId</span></span>
    - <span data-ttu-id="af695-380">'Get-AzVirtualRouter':</span><span class="sxs-lookup"><span data-stu-id="af695-380">'Get-AzVirtualRouter':</span></span>
        - <span data-ttu-id="af695-381">Abonelik düzeyi parametre kümesi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-381">Added subscription level parameter set</span></span>
    - <span data-ttu-id="af695-382">'Remove-AzVirtualRouter'</span><span class="sxs-lookup"><span data-stu-id="af695-382">'Remove-AzVirtualRouter'</span></span>
    - <span data-ttu-id="af695-383">'Add-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="af695-383">'Add-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="af695-384">'Get-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="af695-384">'Get-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="af695-385">'Remove-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="af695-385">'Remove-AzVirtualRouterPeer'</span></span>
* <span data-ttu-id="af695-386">Azure ExpressRoute Bağlantı Noktası için yeni cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-386">Added new cmdlet for Azure Express Route Port</span></span>
    - <span data-ttu-id="af695-387">'New-AzExpressRoutePortLOA'</span><span class="sxs-lookup"><span data-stu-id="af695-387">'New-AzExpressRoutePortLOA'</span></span>
* <span data-ttu-id="af695-388">VirtualNetwork Eşleme Kaynağına RemoteBgpCommunities özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-388">Added RemoteBgpCommunities property to the VirtualNetwork Peering Resource</span></span>
* <span data-ttu-id="af695-389">'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' ve 'New-AzPublicIpPrefix' uyarı iletisi değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-389">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>
* <span data-ttu-id="af695-390">'Get-AzVpnGateway' çıkışına VpnGatewayIpConfigurations eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-390">Added VpnGatewayIpConfigurations to 'Get-AzVpnGateway' output</span></span>
* <span data-ttu-id="af695-391">'Set-AzApplicationGatewaySslCertificate' ile ilgili hata düzeltildi [#9488]</span><span class="sxs-lookup"><span data-stu-id="af695-391">Fixed bug for 'Set-AzApplicationGatewaySslCertificate' [#9488]</span></span>
* <span data-ttu-id="af695-392">'AzureFirewall' öğesine 'AllowActiveFTP' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-392">Added 'AllowActiveFTP' parameter to 'AzureFirewall'</span></span>
* <span data-ttu-id="af695-393">Özellik için aşağıdaki komutlar güncelleştirildi: VirtualWan P2SVpnGateway üzerinde internet güvenliğini ayarlama/kaldırma özelliği etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-393">Updated below commands for feature: Enable internet security set/remove on VirtualWan P2SVpnGateway.</span></span>
- <span data-ttu-id="af695-394">'New-AzP2sVpnGateway' güncelleştirildi: Müşterilerin P2SVpnGateway üzerinde internet güvenliğini etkinleştirmek için true olarak ayarlayacakları, Noktadan siteye istemcilere uygulanacak olan isteğe bağlı 'EnableInternetSecurityFlag' anahtar parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-394">Updated 'New-AzP2sVpnGateway': Added optional switch parameter 'EnableInternetSecurityFlag' for customers to set true to enable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
- <span data-ttu-id="af695-395">'Update-AzP2sVpnGateway' güncelleştirildi: Müşterilerin P2SVpnGateway üzerinde internet güvenliğini etkinleştirip devre dışı bırakmak için true/false olarak ayarlayacakları, Noktadan siteye istemcilere uygulanacak olan isteğe bağlı 'EnableInternetSecurityFlag' veya 'DisableInternetSecurityFlag' anahtar parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-395">Updated 'Update-AzP2sVpnGateway': Added optional switch parameters 'EnableInternetSecurityFlag' or 'DisableInternetSecurityFlag' for customers to set true/false to enable/disable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
* <span data-ttu-id="af695-396">Müşterilerin sorun giderme amacıyla VirtualWan P2SVpnGateway’lerini sıfırlamalarını/yeniden başlatmalarını sağlayan yeni 'Reset-AzP2sVpnGateway' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-396">Added new cmdlet 'Reset-AzP2sVpnGateway' for customers to reset/reboot their VirtualWan P2SVpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="af695-397">Müşterilerin sorun giderme amacıyla VirtualWan VpnGateway’lerini sıfırlamalarını/yeniden başlatmalarını sağlayan yeni 'Reset-AzVpnGateway' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-397">Added new cmdlet 'Reset-AzVpnGateway' for customers to reset/reboot their VirtualWan VpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="af695-398">'Set-AzVirtualNetworkSubnetConfig' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-398">Updated 'Set-AzVirtualNetworkSubnetConfig'</span></span>
    - <span data-ttu-id="af695-399">Parametrelerde açıkça ayarlanmışsa alt ağın NSG ve Yönlendirme Tablosu özelliklerinin null olarak ayarlanması [#1548][#9718]</span><span class="sxs-lookup"><span data-stu-id="af695-399">Set NSG and Route Table properties of subnet to null if explicitly set in parameters [#1548][#9718]</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="af695-400">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="af695-400">Az.RecoveryServices</span></span>
* <span data-ttu-id="af695-401">İş yükü Yedekleme Öğeleri için Silme Durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-401">Fixed the Delete State for workload Backup Items.</span></span>

#### <a name="azresources"></a><span data-ttu-id="af695-402">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="af695-402">Az.Resources</span></span>
* <span data-ttu-id="af695-403">Eksik olan denetim Set-AzRoleAssignment cmdlet’ine eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-403">Added missing check for Set-AzRoleAssignment</span></span>
* <span data-ttu-id="af695-404">'Get-AzResourceGroupDeploymentOperation' cmdlet’inin 'SubscriptionId' parametresine hataya neden olan değişiklik özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-404">Added breaking change attribute to 'SubscriptionId' parameter of 'Get-AzResourceGroupDeploymentOperation'</span></span>
* <span data-ttu-id="af695-405">ARM şablonu What-If cmdlet’leri 'Ignore' kaynak değişiklikleri son olarak gösterilecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-405">Updated ARM template What-If cmdlets to show 'Ignore' resource changes last</span></span>
* <span data-ttu-id="af695-406">Dağıtım cmdlet’lerindeki güvenlik ve dizi parametresi serileştirme sorunları düzeltildi [#12773]</span><span class="sxs-lookup"><span data-stu-id="af695-406">Fixed secure and array parameter serialization issues for deployment cmdlets [#12773]</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="af695-407">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="af695-407">Az.ServiceFabric</span></span>
* <span data-ttu-id="af695-408">Yönetilen kümeler ve düğüm türleri için yeni cmdlet’ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="af695-408">Added new cmdlets for managed clusters and node types:</span></span>
    - <span data-ttu-id="af695-409">'New-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="af695-409">'New-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="af695-410">'Get-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="af695-410">'Get-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="af695-411">'Set-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="af695-411">'Set-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="af695-412">'Remove-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="af695-412">'Remove-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="af695-413">'Add-AzServiceFabricManagedClusterClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="af695-413">'Add-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="af695-414">'Remove-AzServiceFabricManagedClusterClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="af695-414">'Remove-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="af695-415">'New-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="af695-415">'New-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="af695-416">'Get-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="af695-416">'Get-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="af695-417">'Set-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="af695-417">'Set-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="af695-418">'Remove-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="af695-418">'Remove-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="af695-419">'Add-AzServiceFabricManagedNodeTypeVMExtension'</span><span class="sxs-lookup"><span data-stu-id="af695-419">'Add-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="af695-420">'Add-AzServiceFabricManagedNodeTypeVMSecret'</span><span class="sxs-lookup"><span data-stu-id="af695-420">'Add-AzServiceFabricManagedNodeTypeVMSecret'</span></span>
    - <span data-ttu-id="af695-421">'Remove-AzServiceFabricManagedNodeTypeVMExtension'</span><span class="sxs-lookup"><span data-stu-id="af695-421">'Remove-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="af695-422">'Restart-AzServiceFabricManagedNodeTyp'</span><span class="sxs-lookup"><span data-stu-id="af695-422">'Restart-AzServiceFabricManagedNodeTyp'</span></span>
* <span data-ttu-id="af695-423">Service Fabric SDK’sı, geçerli model için Service Fabric kaynak sağlayıcısı 2020-03-01 API sürümünü kullanan 1.2.0 sürümüne, yönetilen kümeler için 2020-01-01-preview sürümüne yükseltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-423">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2020-03-01 for the current model and 2020-01-01-preview for managed clusters.</span></span>

#### <a name="azsql"></a><span data-ttu-id="af695-424">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="af695-424">Az.Sql</span></span>
* <span data-ttu-id="af695-425">'New-AzSqlInstance' ve 'Get-AzSqlInstance' cmdlet’lerine BackupStorageRedundancy eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-425">Added BackupStorageRedundancy to 'New-AzSqlInstance' and 'Get-AzSqlInstance'</span></span>
* <span data-ttu-id="af695-426">'Get-AzSqlServerActiveDirectoryOnlyAuthentication' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-426">Added cmdlet 'Get-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="af695-427">'Enable-AzSqlServerActiveDirectoryOnlyAuthentication' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-427">Added cmdlet 'Enable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="af695-428">'New-AzSqlInstance' cmdlet’ine Force parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-428">Added Force parameter to 'New-AzSqlInstance'</span></span>
* <span data-ttu-id="af695-429">Yönetilen Veritabanı Günlük Yeniden Oynatma hizmetine cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-429">Added cmdlets for Managed Database Log Replay service</span></span>
    - <span data-ttu-id="af695-430">'Start-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="af695-430">'Start-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="af695-431">'Get-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="af695-431">'Get-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="af695-432">'Complete-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="af695-432">'Complete-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="af695-433">'Stop-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="af695-433">'Stop-AzSqlInstanceDatabaseLogReplay'</span></span>
* <span data-ttu-id="af695-434">'Get-AzSqlInstanceActiveDirectoryOnlyAuthentication' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-434">Added cmdlet 'Get-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="af695-435">'Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-435">Added cmdlet 'Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="af695-436">'Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-436">Added cmdlet 'Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="af695-437">Ağ yalıtım işlevselliğini desteklemek için 'New-AzSqlDatabaseImport' ve 'New-AzSqlDatabaseExport' cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-437">Updated cmdlets 'New-AzSqlDatabaseImport' and 'New-AzSqlDatabaseExport' to support network isolation functionality</span></span>
* <span data-ttu-id="af695-438">'New-AzSqlDatabaseImportExisting' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-438">Added cmdlet 'New-AzSqlDatabaseImportExisting'</span></span>
* <span data-ttu-id="af695-439">Database cmdlet’leri yedekleme alanı tür belirtimini destekleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-439">Updated Databases cmdlets to support backup storage type specification</span></span>
* <span data-ttu-id="af695-440">'New-AzSqlDatabase' cmdlet’ine Force parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-440">Added Force parameter to 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="af695-441">'New-AzSqlDatabase' cmdlet’indeki seçili bölgelerde yer alan BackupStorageRedundancy yapılandırmasına yönelik uyarı eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-441">Added warning for BackupStorageRedundancy configuration in select regions in 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="af695-442">Sunucu ve örneğe yönelik ActiveDirectoryOnlyAuthentication cmdlet’leri, ResourceId ve InputObject’i içerek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-442">Updated ActiveDirectoryOnlyAuthentication cmdlets for server and instance to include ResourceId and InputObject</span></span>

#### <a name="azstorage"></a><span data-ttu-id="af695-443">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="af695-443">Az.Storage</span></span>
* <span data-ttu-id="af695-444">Microsoft.Azure.Storage.DataMovement 2.0.0 sürümüne yükseltme sırasında blob karşıya yüklenirken oluşan hata düzeltildi [#12220]</span><span class="sxs-lookup"><span data-stu-id="af695-444">Fixed upload blob fail by upgrade to Microsoft.Azure.Storage.DataMovement 2.0.0 [#12220]</span></span>
* <span data-ttu-id="af695-445">Belirli Bir Noktaya Geri Yükleme Desteği Eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-445">Supported Point In Time Restore</span></span>
    - <span data-ttu-id="af695-446">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="af695-446">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="af695-447">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="af695-447">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="af695-448">'New-AzStorageBlobRangeToRestore'</span><span class="sxs-lookup"><span data-stu-id="af695-448">'New-AzStorageBlobRangeToRestore'</span></span>
    - <span data-ttu-id="af695-449">'Restore-AzStorageBlobRange'</span><span class="sxs-lookup"><span data-stu-id="af695-449">'Restore-AzStorageBlobRange'</span></span>
* <span data-ttu-id="af695-450">get-AzureRMStorageAccount cmdlet’ini -IncludeBlobRestoreStatus parametresiyle çalıştırarak Depolama hesabının blobu geri yükleme durumunu almaya yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-450">Supported get blob restore status of Storage account by run get-AzureRMStorageAccount with parameter -IncludeBlobRestoreStatus</span></span> 
    - <span data-ttu-id="af695-451">'Get-AzureRMStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="af695-451">'Get-AzureRMStorageAccount'</span></span>
* <span data-ttu-id="af695-452">Yaklaşan cmdlet çıkış değişikliği için hataya neden olan değişiklik uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-452">Added breaking change warning message for upcoming cmdlet output change</span></span>
    - <span data-ttu-id="af695-453">'Get-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="af695-453">'Get-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="af695-454">'Set-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="af695-454">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="af695-455">'Set-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="af695-455">'Set-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="af695-456">'Get-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="af695-456">'Get-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="af695-457">'Add-AzStorageAccountManagementPolicyAction'</span><span class="sxs-lookup"><span data-stu-id="af695-457">'Add-AzStorageAccountManagementPolicyAction'</span></span>
    - <span data-ttu-id="af695-458">'New-AzStorageAccountManagementPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="af695-458">'New-AzStorageAccountManagementPolicyRule'</span></span>
* <span data-ttu-id="af695-459">Microsoft.Azure.Cosmos.Table SDK 1.0.8 sürümüne yükseltildi</span><span class="sxs-lookup"><span data-stu-id="af695-459">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.8</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="af695-460">Topluluğumuzdan katkıda bulunanlara teşekkür ederiz</span><span class="sxs-lookup"><span data-stu-id="af695-460">Thanks to our community contributors</span></span>
* <span data-ttu-id="af695-461">Thomas Van Laere (@ThomVanL), Dockerfile-alpine-3.10’u ekledi (#12911)</span><span class="sxs-lookup"><span data-stu-id="af695-461">Thomas Van Laere (@ThomVanL), Add Dockerfile-alpine-3.10 (#12911)</span></span> 
* <span data-ttu-id="af695-462">Lohith Chowdary Chilukuri (@Lochiluk), Remove-AzNetworkInterfaceIpConfig.md dosyasını güncelleştirdi (#12807)</span><span class="sxs-lookup"><span data-stu-id="af695-462">Lohith Chowdary Chilukuri (@Lochiluk), Update Remove-AzNetworkInterfaceIpConfig.md (#12807)</span></span> 
* <span data-ttu-id="af695-463">Roberth Strand (@roberthstrand), Get-AzResourceGroup-New örneği ve temizleme (#12828)</span><span class="sxs-lookup"><span data-stu-id="af695-463">Roberth Strand (@roberthstrand), Get-AzResourceGroup - New example, and cleanup (#12828)</span></span> 
* <span data-ttu-id="af695-464">Ravi Mishra (@inmishrar), Azure Web App çalışma zamanı yığınını DOTNETCORE’a güncelleştirdi (#12833)</span><span class="sxs-lookup"><span data-stu-id="af695-464">Ravi Mishra (@inmishrar), update Azure Web App runtime stack to DOTNETCORE (#12833)</span></span> 
* <span data-ttu-id="af695-465">@jack-education, Set-AzVirtualNetworkSubnetConfig cmdlet’i NSG ve Rota Tablosunu alt ağdan kaldıracak şekilde güncelleştirdi (#12351)</span><span class="sxs-lookup"><span data-stu-id="af695-465">@jack-education, Updated Set-AzVirtualNetworkSubnetConfig to allow NSG and Route Table to be removed from subnet (#12351)</span></span> 
* <span data-ttu-id="af695-466">@hagop-globanet, Add-AzApplicationGatewayCustomError.md dosyasını güncelleştirdi (#12784)</span><span class="sxs-lookup"><span data-stu-id="af695-466">@hagop-globanet, Update Add-AzApplicationGatewayCustomError.md (#12784)</span></span> 
* <span data-ttu-id="af695-467">Joshua Van Daalen (@greenSacrifice)</span><span class="sxs-lookup"><span data-stu-id="af695-467">Joshua Van Daalen (@greenSacrifice)</span></span>
  * <span data-ttu-id="af695-468">Özellikten Özelliğe yazımını güncelleştirdi (#12821)</span><span class="sxs-lookup"><span data-stu-id="af695-468">Update spelling of Property to Property (#12821)</span></span> 
  * <span data-ttu-id="af695-469">New-AzResourceLock.md örneklerini güncelleştirdi (#12806)</span><span class="sxs-lookup"><span data-stu-id="af695-469">Update New-AzResourceLock.md examples (#12806)</span></span>
* <span data-ttu-id="af695-470">Eragon Riddle (@eragonriddle), örnekteki parametre alanı adını düzeltti (#12825)</span><span class="sxs-lookup"><span data-stu-id="af695-470">Eragon Riddle (@eragonriddle), Corrected parameter field name in the example (#12825)</span></span> 
* <span data-ttu-id="af695-471">@rossifumax, New-AzConfigurationAssignment.md dosyasındaki yazım hatasını düzeltti (#12701)</span><span class="sxs-lookup"><span data-stu-id="af695-471">@rossifumax, Fix typo in New-AzConfigurationAssignment.md (#12701)</span></span>

## <a name="461---august-2020"></a><span data-ttu-id="af695-472">4.6.1 - Ağustos 2020</span><span class="sxs-lookup"><span data-stu-id="af695-472">4.6.1 - August 2020</span></span>
#### <a name="azcompute"></a><span data-ttu-id="af695-473">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="af695-473">Az.Compute</span></span>
* <span data-ttu-id="af695-474">False değerinin varsayılan değerini kaldırmak için 'New-AzVm' içindeki '-EncryptionAtHost' parametresine yama uygulandı [#12776]</span><span class="sxs-lookup"><span data-stu-id="af695-474">Patched '-EncryptionAtHost' parameter in 'New-AzVm' to remove default value of false [#12776]</span></span>

## <a name="460---august-2020"></a><span data-ttu-id="af695-475">4.6.0 - Ağustos 2020</span><span class="sxs-lookup"><span data-stu-id="af695-475">4.6.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="af695-476">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="af695-476">Az.Accounts</span></span>
* <span data-ttu-id="af695-477">Bulma uç noktası varsayılan AzureCloud ortamını veya diğer genel ortamları döndürmediğinden tüm genel bulut ortamları yüklendi (#12633)</span><span class="sxs-lookup"><span data-stu-id="af695-477">Loaded all public cloud environments when discovery endpoint doesn't return default AzureCloud or other public environments [#12633]</span></span>
* <span data-ttu-id="af695-478">SubscriptionPolicies, 'Get-AzSubscription' cmdlet’inde kullanıma sunuldu [#12551]</span><span class="sxs-lookup"><span data-stu-id="af695-478">Exposed SubscriptionPolicies in 'Get-AzSubscription' [#12551]</span></span>

#### <a name="azautomation"></a><span data-ttu-id="af695-479">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="af695-479">Az.Automation</span></span>
* <span data-ttu-id="af695-480">Karma Çalışanı Grubu belirtmek için 'Set-AzAutomationWebhook' cmdlet’ine '-RunOn' parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-480">Added '-RunOn' parameters to 'Set-AzAutomationWebhook' to specify a Hybrid Worker Group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="af695-481">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="af695-481">Az.Compute</span></span>
* <span data-ttu-id="af695-482">'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM' ve 'Update-AzVmss' cmdlet’lerine '-EncryptionAtHost' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-482">Added '-EncryptionAtHost' parameter to 'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM', and 'Update-AzVmss'</span></span>
* <span data-ttu-id="af695-483">'Get-AzVM' ve 'Get-AzVmss' cmdlet’lerinin dönüş nesnesine 'SecurityProfile' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-483">Added 'SecurityProfile' to 'Get-AzVM' and 'Get-AzVmss' return object</span></span>
* <span data-ttu-id="af695-484">'-InstanceView' anahtarı 'Get-AzHostGroup' cmdlet’ine isteğe bağlı parametre olarak eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-484">Added '-InstanceView' switch as optional parameter to 'Get-AzHostGroup'</span></span>
* <span data-ttu-id="af695-485">Yeni 'Invoke-AzVmPatchAssessment' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-485">Added new cmdlet 'Invoke-AzVmPatchAssessment'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="af695-486">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="af695-486">Az.DataFactory</span></span>
* <span data-ttu-id="af695-487">PSPipelineRun sınıfındaki eksik özellikler eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-487">Added missing properties to PSPipelineRun class.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="af695-488">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="af695-488">Az.HDInsight</span></span>
* <span data-ttu-id="af695-489">Konakta şifreleme özelliğiyle küme oluşturma desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-489">Supported creating cluster with encryption at host feature.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="af695-490">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="af695-490">Az.KeyVault</span></span>
* <span data-ttu-id="af695-491">Geçici silmeyi devre dışı bırakma planlaması için uyarı iletileri eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-491">Added warning messages for planning to disable soft delete</span></span>
* <span data-ttu-id="af695-492">SecretValueText özniteliğini kaldırma planlaması için uyarı iletileri eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-492">Added warning messages for planning to remove attribute SecretValueText</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="af695-493">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="af695-493">Az.Maintenance</span></span>
* <span data-ttu-id="af695-494">'New-AzMaintenanceConfiguration' cmdlet’ine isteğe bağlı zamanlamayla ilgili alanlar eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-494">Added optional schedule related fields to 'New-AzMaintenanceConfiguration'</span></span>
* <span data-ttu-id="af695-495">'Get-AzMaintenancePublicConfiguration' için yeni cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-495">Added new cmdlet for 'Get-AzMaintenancePublicConfiguration'</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="af695-496">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="af695-496">Az.ManagedServices</span></span>
* <span data-ttu-id="af695-497">Yönetilen hizmet atama ve tanım cmdlet’lerine hataya neden olan değişiklik uyarıları eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-497">Added breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="af695-498">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="af695-498">Az.Monitor</span></span>
* <span data-ttu-id="af695-499">Günlüklerin ve Ölçümlerin ayrılmasını etkinleştirmek için 'Set-AzDiagnosticSetting' cmdlet’indeki parametre kümesi genişletildi [#12482]</span><span class="sxs-lookup"><span data-stu-id="af695-499">Extended the parameter set in 'Set-AzDiagnosticSetting' for separation of Logs and Metrics enablement [#12482]</span></span>
* <span data-ttu-id="af695-500">'Add-AzMetricAlertRuleV2' cmdlet’inde işlem hattından ölçüm uyarısı alınırken oluşan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-500">Fixed bug for 'Add-AzMetricAlertRuleV2' when getting metric alert from pipeline</span></span>

#### <a name="azresources"></a><span data-ttu-id="af695-501">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="af695-501">Az.Resources</span></span>
* <span data-ttu-id="af695-502">'Get-AzPolicyAlias' cmdlet’i, diğer adın Azure İlkesi tarafından değiştirilebilir olup olmadığını belirten bilgiler içerek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-502">Updated 'Get-AzPolicyAlias' response to include information indicating whether the alias is modifiable by Azure Policy.</span></span>
* <span data-ttu-id="af695-503">Yeni 'Set-AzRoleAssignment' cmdlet’i oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="af695-503">Created new cmdlet 'Set-AzRoleAssignment'</span></span>
* <span data-ttu-id="af695-504">Yönetim grubu kapsamındaki ARM şablonu Durum sonuçlarını almak için 'Get-AzDeploymentManagementGroupWhatIfResult' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-504">Added 'Get-AzDeploymentManagementGroupWhatIfResult' for getting ARM template What-If results at management Group scope</span></span>
* <span data-ttu-id="af695-505">Kiracı kapsamındaki ARM şablonu Durum sonuçlarını almaya yönelik yeni 'Get-AzTenantWhatIfResult' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-505">Added 'Get-AzTenantWhatIfResult' new cmdlet for getting ARM template What-If results at tenant scope</span></span>
* <span data-ttu-id="af695-506">'New-AzManagementGroupDeployment' ve 'New-AzTenantDeployment' için '-WhatIf' ve '-Confirm' parametreleri, ARM şablonu Durum sonuçlarını kullanacak şekilde geçersiz kılındı</span><span class="sxs-lookup"><span data-stu-id="af695-506">Overrode '-WhatIf' and '-Confirm' for 'New-AzManagementGroupDeployment' and 'New-AzTenantDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="af695-507">Yeni dağıtım cmdlet’lerindeki '-WhatIf' ve '-Confirm' parametrelerinin davranışları False ile uyumlu olacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-507">Fixed the behaviors of '-WhatIf' and '-Confirm' for new deployment cmdlets so they comply with False and</span></span> 
* <span data-ttu-id="af695-508">'-TemplateObject' ve 'TemplateParameterObject' için serileştirme hatası düzeltildi [#1528] [#6292]</span><span class="sxs-lookup"><span data-stu-id="af695-508">Fixed serialization error for '-TemplateObject' and 'TemplateParameterObject' [#1528] [#6292]</span></span>
* <span data-ttu-id="af695-509">'Get-AzResourceGroupDeploymentOperation' cmdlet’ine, yaklaşan çıkış türü değişikliğine yönelik hataya neden olan değişiklik özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-509">Added breaking change attribute to 'Get-AzResourceGroupDeploymentOperation' for the upcoming output type change</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="af695-510">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="af695-510">Az.SignalR</span></span>
* <span data-ttu-id="af695-511">'Restart-AzSignalR' ve 'Update-AzSignalR' yardım dosyalarındaki hatalar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-511">Fixed 'Restart-AzSignalR' and 'Update-AzSignalR' help files errors</span></span>
* <span data-ttu-id="af695-512">'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream' cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-512">Added cmdlets 'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="af695-513">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="af695-513">Az.Storage</span></span>
* <span data-ttu-id="af695-514">Blob sorgu hızlandırması desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-514">Supported blob query acceleration</span></span>
    -  <span data-ttu-id="af695-515">'Get-AzStorageBlobQueryResult'</span><span class="sxs-lookup"><span data-stu-id="af695-515">'Get-AzStorageBlobQueryResult'</span></span>
    -  <span data-ttu-id="af695-516">'New-AzStorageBlobQueryConfig'</span><span class="sxs-lookup"><span data-stu-id="af695-516">'New-AzStorageBlobQueryConfig'</span></span>
* <span data-ttu-id="af695-517">Yardım dosyası güncelleştirildi, daha fazla açıklama eklendi ve yazım hataları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-517">Updated help file, added more description, and fixed typo</span></span>
    -  <span data-ttu-id="af695-518">“Start-AzStorageBlobCopy”</span><span class="sxs-lookup"><span data-stu-id="af695-518">'Start-AzStorageBlobCopy'</span></span>
    -  <span data-ttu-id="af695-519">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="af695-519">'Get-AzDataLakeGen2Item'</span></span>
* <span data-ttu-id="af695-520">İlgili alt dizin mevcut olmadığında blobu indirme işleminin başarısız olmasıyla ilgili sorun düzeltildi [#12592]</span><span class="sxs-lookup"><span data-stu-id="af695-520">Fixed download blob fail when related sub directory not exist [#12592]</span></span>
    -  <span data-ttu-id="af695-521">“Get-AzStorageBlobContent”</span><span class="sxs-lookup"><span data-stu-id="af695-521">'Get-AzStorageBlobContent'</span></span>
* <span data-ttu-id="af695-522">Depolama hesaplarında Set/Get/Remove Nesne Çoğaltma İlkesi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-522">Supported Set/Get/Remove Object Replication Policy on Storage accounts</span></span>
    - <span data-ttu-id="af695-523">'New-AzStorageObjectReplicationPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="af695-523">'New-AzStorageObjectReplicationPolicyRule'</span></span>
    - <span data-ttu-id="af695-524">'Set-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="af695-524">'Set-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="af695-525">'Get-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="af695-525">'Get-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="af695-526">'Remove-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="af695-526">'Remove-AzStorageObjectReplicationPolicy'</span></span>
* <span data-ttu-id="af695-527">Bir Depolama hesabının Blob Hizmeti üzerinde ChangeFeed’i etkinleştirmeye/devre dışı bırakmaya yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-527">Supported enable/disable ChangeFeed on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="af695-528">“Update-AzStorageBlobServiceProperty”</span><span class="sxs-lookup"><span data-stu-id="af695-528">'Update-AzStorageBlobServiceProperty'</span></span>

## <a name="450---august-2020"></a><span data-ttu-id="af695-529">4.5.0 - Ağustos 2020</span><span class="sxs-lookup"><span data-stu-id="af695-529">4.5.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="af695-530">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="af695-530">Az.Accounts</span></span>
* <span data-ttu-id="af695-531">'Connect-AzAccount' cmdlet’i 'MaxContextPopulation' parametresini kabul edecek şekilde güncelleştirildi [#9865]</span><span class="sxs-lookup"><span data-stu-id="af695-531">Updated 'Connect-AzAccount' to accept parameter 'MaxContextPopulation' [#9865]</span></span>
* <span data-ttu-id="af695-532">SubscriptionClient sürümü 2019-06-01 olarak ve kiracı etki alanlarını görüntüleyecek şekilde güncelleştirildi [#9838]</span><span class="sxs-lookup"><span data-stu-id="af695-532">Updated SubscriptionClient version to 2019-06-01 and display tenant domains [#9838]</span></span>
* <span data-ttu-id="af695-533">Aboneliğin giriş kiracısı ve yöneten kiracısı bilgilerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-533">Supported home tenant and managedBy tenant information of subscription</span></span>
* <span data-ttu-id="af695-534">Telemetri verilerindeki modül adı ve sürüm bilgileri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-534">Corrected module name, version info in telemetry data</span></span>
* <span data-ttu-id="af695-535">SqlDatabaseDnsSuffix ve ServiceManagementUrl, ortam meta verileri uç noktasının uyumsuz değer döndürdüğü durumlar için ayarlandı</span><span class="sxs-lookup"><span data-stu-id="af695-535">Adjusted SqlDatabaseDnsSuffix and ServiceManagementUrl if environment metadata endpoint returns incompatible value</span></span>

#### <a name="azaks"></a><span data-ttu-id="af695-536">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="af695-536">Az.Aks</span></span>
* <span data-ttu-id="af695-537">'ClientIdAndSecret' kaldırılarak 'ServicePrincipalIdAndSecret' eklendi ve 'ClientIdAndSecret' bir diğer ad olarak ayarlandı [#12381].</span><span class="sxs-lookup"><span data-stu-id="af695-537">Removed 'ClientIdAndSecret' to 'ServicePrincipalIdAndSecret' and set 'ClientIdAndSecret' as an alias [#12381].</span></span>
* <span data-ttu-id="af695-538">'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' cmdlet’leri kaldırılarak 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' eklendi ve özgün olanlar diğer ad olarak ayarlandı [#12373].</span><span class="sxs-lookup"><span data-stu-id="af695-538">Removed 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' to 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' and set the original ones as alias [#12373].</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="af695-539">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="af695-539">Az.ApiManagement</span></span>
* <span data-ttu-id="af695-540">Yeni 'Add-AzApiManagementApiToGateway' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-540">Added new 'Add-AzApiManagementApiToGateway' cmdlet.</span></span>
* <span data-ttu-id="af695-541">Yeni 'Get-AzApiManagementGateway' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-541">Added new 'Get-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="af695-542">Yeni 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-542">Added new 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="af695-543">Yeni 'Get-AzApiManagementGatewayKey' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-543">Added new 'Get-AzApiManagementGatewayKey' cmdlet.</span></span>
* <span data-ttu-id="af695-544">Yeni 'New-AzApiManagementGateway' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-544">Added new 'New-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="af695-545">Yeni 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-545">Added new 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="af695-546">Yeni 'New-AzApiManagementResourceLocationObject' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-546">Added new 'New-AzApiManagementResourceLocationObject' cmdlet.</span></span>
* <span data-ttu-id="af695-547">Yeni 'Remove-AzApiManagementApiFromGateway' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-547">Added new 'Remove-AzApiManagementApiFromGateway' cmdlet.</span></span>
* <span data-ttu-id="af695-548">Yeni 'Remove-AzApiManagementGateway' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-548">Added new 'Remove-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="af695-549">Yeni 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-549">Added new 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="af695-550">Yeni 'Update-AzApiManagementGateway' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-550">Added new 'Update-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="af695-551">'Get-AzApiManagementApi' cmdlet’ine yeni ve isteğe bağlı [-GatewayId] parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-551">Added new optional [-GatewayId] parameter to the 'Get-AzApiManagementApi' cmdlet.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="af695-552">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="af695-552">Az.CognitiveServices</span></span>
* <span data-ttu-id="af695-553">'Deny', özellikle NetworkRules varsayılan eylemi olarak kullanıldı.</span><span class="sxs-lookup"><span data-stu-id="af695-553">Used 'Deny' specifically as NetworkRules default action.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="af695-554">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="af695-554">Az.FrontDoor</span></span>
* <span data-ttu-id="af695-555">Enum.Parse metodu, bir null değeri Enabled veya Disabled sabit listesi değerlerine zorladığında özel durum oluşturulmasıyla ilgili bir sorun düzeltildi [#12344]</span><span class="sxs-lookup"><span data-stu-id="af695-555">Fixed an issue where an exception is being thrown when Enum.Parse tries to coerce a null value to an Enabled or Disabled enum values [#12344]</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="af695-556">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="af695-556">Az.HDInsight</span></span>
* <span data-ttu-id="af695-557">Aktarma özelliğinde şifrelemeye sahip küme oluşturma desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-557">Supported creating cluster with encryption in transit feature.</span></span>
    - <span data-ttu-id="af695-558">'New-AzHDInsightCluster' cmdlet’ine yeni 'EncryptionInTransit' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-558">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="af695-559">'New-AzHDInsightClusterConfig' cmdlet’ine yeni 'EncryptionInTransit' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-559">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="af695-560">Özel bağlantı özelliğine sahip küme oluşturma desteği eklendi:</span><span class="sxs-lookup"><span data-stu-id="af695-560">Supported creating cluster with private link feature:</span></span>
    - <span data-ttu-id="af695-561">'New-AzHDInsightCluster' cmdlet’ine yeni 'PublicNetworkAccessType' ve 'OutboundPublicNetworkAccessType' parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-561">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="af695-562">'New-AzHDInsightClusterConfig' cmdlet’ine yeni 'PublicNetworkAccessType' ve 'OutboundPublicNetworkAccessType' parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-562">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="af695-563">'New-AzHDInsightCluster' veya 'Get-AzHDInsightCluster' çağrıldığında sanal ağ bilgileri döndürüldü</span><span class="sxs-lookup"><span data-stu-id="af695-563">Returned virtual network information when calling 'New-AzHDInsightCluster' or 'Get-AzHDInsightCluster'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="af695-564">Az.Network</span><span class="sxs-lookup"><span data-stu-id="af695-564">Az.Network</span></span>
* <span data-ttu-id="af695-565">'Remove-AzExpressRouteCircuitConnectionConfig' cmdlet’ine yönelik AddressPrefixType parametresi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-565">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="af695-566">Hataya neden olmayan değişiklikler eklendi: 'Remove-AzExpressRouteCircutPeeringConfig' cmdlet’inde Özel Eşleme’ye yönelik PeerAddressType işlevi eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-566">Added non-breaking changes: PeerAddressType functionality for Private Peering in 'Remove-AzExpressRouteCircutPeeringConfig'.</span></span>
* <span data-ttu-id="af695-567">AddressPrefixType ve PeerAddressType parametresindeki kodlar büyük/küçük harfi yoksayacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-567">Code changed to ignore case for AddressPrefixType and PeerAddressType parameter.</span></span>
* <span data-ttu-id="af695-568">'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' ve 'New-AzPublicIpPrefix' uyarı iletisi değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-568">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="af695-569">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="af695-569">Az.OperationalInsights</span></span>
* <span data-ttu-id="af695-570">'Remove-AzOperationalInsightsworkspace' için '-ForceDelete' seçeneği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-570">Added '-ForceDelete' option for 'Remove-AzOperationalInsightsworkspace'</span></span>
* <span data-ttu-id="af695-571">Yeni 'Get-AzOperationalInsightsDeletedWorkspace' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-571">Added new cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span></span>
* <span data-ttu-id="af695-572">Yeni 'Restore-AzOperationalInsightsWorkspace' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-572">Added new cmdlet 'Restore-AzOperationalInsightsWorkspace'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="af695-573">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="af695-573">Az.RecoveryServices</span></span>
* <span data-ttu-id="af695-574">Azure Backup kapsayıcı/öğe keşif deneyimi iyileştirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-574">Improved the Azure Backup container/item discovery experience.</span></span>

#### <a name="azresources"></a><span data-ttu-id="af695-575">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="af695-575">Az.Resources</span></span>
* <span data-ttu-id="af695-576">'New-AzRoleAssignment' cmdlet’ine 'Condition', 'ConditionVersion' ve 'Description' özellikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-576">Added properties 'Condition', 'ConditionVersion' and 'Description' to 'New-AzRoleAssignment'</span></span>
    - <span data-ttu-id="af695-577">Bu, veri modellerinde yapılan tüm ilgili değişiklikleri içerir</span><span class="sxs-lookup"><span data-stu-id="af695-577">This included all the relevant changes to the data models</span></span>

#### <a name="azsql"></a><span data-ttu-id="af695-578">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="af695-578">Az.Sql</span></span>
* <span data-ttu-id="af695-579">'New-AzSqlServer' ve 'Set-AzSqlServer' cmdlet’lerindeki sunucu adının olası büyük/küçük harfe duyarsızlık hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-579">Fixed potential server name case insensitive error in 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="af695-580">'New-AzSqlDatabaseSecondary' cmdlet’indeki mevcut veritabanına yanlış veritabanı adının döndürülmesi hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-580">Fixed wrong database name returned on existing database error in 'New-AzSqlDatabaseSecondary'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="af695-581">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="af695-581">Az.Storage</span></span>
* <span data-ttu-id="af695-582">Yeni x,t izniyle kapsayıcı/blob Sas belirteci oluşturma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-582">Supported create container/blob Sas token with new permission x,t</span></span>
    -  <span data-ttu-id="af695-583">“New-AzStorageBlobSASToken”</span><span class="sxs-lookup"><span data-stu-id="af695-583">'New-AzStorageBlobSASToken'</span></span>
    -  <span data-ttu-id="af695-584">'New-AzStorageContainerSASToken'</span><span class="sxs-lookup"><span data-stu-id="af695-584">'New-AzStorageContainerSASToken'</span></span>
* <span data-ttu-id="af695-585">Yeni x,t,f izniyle hesap Sas belirteci oluşturma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-585">Supported create account Sas token with new permission x,t,f</span></span>
    -  <span data-ttu-id="af695-586">'New-AzStorageAccountSASToken'</span><span class="sxs-lookup"><span data-stu-id="af695-586">'New-AzStorageAccountSASToken'</span></span>
* <span data-ttu-id="af695-587">Tek dosya paylaşımı kullanımını alma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-587">Supported get single file share usage</span></span>
    - <span data-ttu-id="af695-588">'Get-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="af695-588">'Get-AzRmStorageShare'</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="af695-589">4.4.0 - Temmuz 2020</span><span class="sxs-lookup"><span data-stu-id="af695-589">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="af695-590">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="af695-590">Az.Accounts</span></span>
* <span data-ttu-id="af695-591">“Invoke-AzRestMethod” adlı yeni cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-591">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="af695-592">“Start-Job” kullanan birden çok Azure PowerShell cmdlet’inin çalıştığı durumlar gibi çok işlemli senaryolarda kimlik doğrulama hatalarına sebep olabilen bir sorun düzeltildi [#9448]</span><span class="sxs-lookup"><span data-stu-id="af695-592">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="af695-593">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="af695-593">Az.Aks</span></span>
* <span data-ttu-id="af695-594">“Get-AzAks” cmdlet’inin tüm kümeleri almamasına neden olan hata düzeltildi [#12296]</span><span class="sxs-lookup"><span data-stu-id="af695-594">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="af695-595">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="af695-595">Az.AnalysisServices</span></span>
* <span data-ttu-id="af695-596">Kimlik Doğrulamasına yönelik proje başvurusu kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="af695-596">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="af695-597">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="af695-597">Az.Automation</span></span>
* <span data-ttu-id="af695-598">Kaçış karakterleri içeren dizenin bir JSON nesnesine dönüştürülememesiyle ilgili sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-598">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="af695-599">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="af695-599">Az.Compute</span></span>
* <span data-ttu-id="af695-600">“En son” resim sürümü olmadan “New-AzVmss” cmdlet’ini kullanırken görüntülenecek bir uyarı eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-600">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="af695-601">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="af695-601">Az.DataFactory</span></span>
* <span data-ttu-id="af695-602">Data Factory’ye genel parametreler eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-602">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="af695-603">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="af695-603">Az.EventGrid</span></span>
* <span data-ttu-id="af695-604">2020-06-01 API sürümünü kullanacak biçimde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-604">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="af695-605">Yeni özellikler eklendi:</span><span class="sxs-lookup"><span data-stu-id="af695-605">Added new features:</span></span>
    - <span data-ttu-id="af695-606">Giriş eşleme</span><span class="sxs-lookup"><span data-stu-id="af695-606">Input mapping</span></span>
    - <span data-ttu-id="af695-607">Olay Teslim Şeması</span><span class="sxs-lookup"><span data-stu-id="af695-607">Event Delivery Schema</span></span>
    - <span data-ttu-id="af695-608">Özel Bağlantı</span><span class="sxs-lookup"><span data-stu-id="af695-608">Private Link</span></span>
    - <span data-ttu-id="af695-609">Bulut Olayı V10 Şeması</span><span class="sxs-lookup"><span data-stu-id="af695-609">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="af695-610">Hedef Olarak Service Bus Konu Başlığı</span><span class="sxs-lookup"><span data-stu-id="af695-610">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="af695-611">Hedef Olarak Azure İşlevi</span><span class="sxs-lookup"><span data-stu-id="af695-611">Azure Function As Destination</span></span>
    - <span data-ttu-id="af695-612">Web Kancası Toplu İş</span><span class="sxs-lookup"><span data-stu-id="af695-612">WebHook Batching</span></span>
    - <span data-ttu-id="af695-613">Güvenli web kancası (AAD desteği)</span><span class="sxs-lookup"><span data-stu-id="af695-613">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="af695-614">IpFiltering</span><span class="sxs-lookup"><span data-stu-id="af695-614">IpFiltering</span></span>
* <span data-ttu-id="af695-615">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="af695-615">Updated cmdlets:</span></span>
    - <span data-ttu-id="af695-616">“New-AzEventGridSubscription'/'Update-AzEventGridSubscription”:</span><span class="sxs-lookup"><span data-stu-id="af695-616">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="af695-617">Web kancası toplu işlemin destekleyecek yeni, isteğe bağlı parametreler eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-617">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="af695-618">AAD kullanarak güvenli web kancasını desteklemek için yeni, isteğe bağlı parametreler eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-618">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="af695-619">Yeni hedef olarak Azure İşlevi’ni ve Service Bus konu başlığını desteklemek üzere EndpointType parametresi için yeni bir sabit listesi eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-619">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="af695-620">Teslim şeması için yeni, isteğe bağlı parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-620">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="af695-621">“New-AzEventGridTopic'/'Update-AzEventGridTopic” ve “New-AzEventGridDomain'/'Update-AzEventGridDomain”:</span><span class="sxs-lookup"><span data-stu-id="af695-621">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="af695-622">IpFiltering’i destekleyecek yeni, isteğe bağlı parametreler eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-622">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="af695-623">“New-AzEventGridTopic'/'New-AzEventGridDomain”:</span><span class="sxs-lookup"><span data-stu-id="af695-623">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="af695-624">Giriş eşlemeyi destekleyecek yeni, isteğe bağlı parametreler eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-624">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="af695-625">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="af695-625">Az.FrontDoor</span></span>
* <span data-ttu-id="af695-626">Modül, API 2020-05-01 kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-626">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="af695-627">Depolama, Key Vault ve Web App Service kaynakları için Özel bağlantı desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-627">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="af695-628">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="af695-628">Az.HDInsight</span></span>
* <span data-ttu-id="af695-629">Ulusal bulutlarda ADLS 1. veya 2. Nesil depolama ile küme oluşturmaya yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-629">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="af695-630">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="af695-630">Az.Monitor</span></span>
* <span data-ttu-id="af695-631">Ölçümler ve günlükler null olduğunda “Get-AzDiagnosticSetting” cmdlet’inde oluşan hata düzeltildi [#12272]</span><span class="sxs-lookup"><span data-stu-id="af695-631">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="af695-632">Az.Network</span><span class="sxs-lookup"><span data-stu-id="af695-632">Az.Network</span></span>
* <span data-ttu-id="af695-633">VWan HubVnet bağlantısında değişen parametreler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-633">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="af695-634">Azure Ağ Sanal Alet Siteleri’ne yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-634">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="af695-635">“Get-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="af695-635">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="af695-636">“New-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="af695-636">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="af695-637">“Remove-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="af695-637">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="af695-638">“Update-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="af695-638">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="af695-639">“New-AzOffice365PolicyProperty”</span><span class="sxs-lookup"><span data-stu-id="af695-639">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="af695-640">Azure Ağ Sanal Gereçi’ne yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-640">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="af695-641">“Get-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="af695-641">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="af695-642">“New-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="af695-642">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="af695-643">“Remove-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="af695-643">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="af695-644">“Update-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="af695-644">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="af695-645">“Get-AzNetworkVirtualApplianceSku”</span><span class="sxs-lookup"><span data-stu-id="af695-645">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="af695-646">“New-AzVirtualApplianceSkuProperty”</span><span class="sxs-lookup"><span data-stu-id="af695-646">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="af695-647">Özel Bağlantı Ortak Cmdlet’lerine Application Gateway eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-647">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="af695-648">Özel Bağlantı Ortak Cmdlet’lerine StorageSync Eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-648">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="af695-649">Özel Bağlantı Ortak Cmdlet’lerine SignalR Eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-649">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="af695-650">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="af695-650">Az.RecoveryServices</span></span>
* <span data-ttu-id="af695-651">Kimlik Doğrulamasına yönelik proje başvurusu kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="af695-651">Removed project reference to Authentication</span></span>
* <span data-ttu-id="af695-652">Azure Backup, cmdlet’leri metinlerin daha doğru görüneceği şekilde ayarladı</span><span class="sxs-lookup"><span data-stu-id="af695-652">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="af695-653">Azure Backup, “Get-AzRecoveryServicesBackupJob” cmdlet’i kullanılarak MAB aracı işlerinin getirilmesine yönelik destek ekledi.</span><span class="sxs-lookup"><span data-stu-id="af695-653">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="af695-654">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="af695-654">Az.Resources</span></span>
* <span data-ttu-id="af695-655">“Save-AzResourceGroupDeploymentTemplate” cmdlet’i SDK’yı kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-655">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="af695-656">“Unregister-AzResourceProvider” cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-656">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="af695-657">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="af695-657">Az.Sql</span></span>
* <span data-ttu-id="af695-658">“Set-AzSqlInstanceActiveDirectoryAdministrator” cmdlet’indeki Hizmet sorumlusu ve konuk kullanıcılara yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-658">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="af695-659">Veri Sınıflandırma cmdlet’lerindeki bir sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-659">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="af695-660">Azure SQL Yönetilen Örneği yük devretmesine yönelik destek eklendi: “Invoke-AzSqlInstanceFailover”</span><span class="sxs-lookup"><span data-stu-id="af695-660">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="af695-661">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="af695-661">Az.Storage</span></span>
* <span data-ttu-id="af695-662">Bazı veri düzlemi cmdlet’leri için UserAgent’ın eklenmemesiyle ilgili sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-662">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="af695-663">MinimumTlsVersion ve AllowBlobPublicAccess içeren bir Depolama hesabını oluşturmaya/güncelleştirmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-663">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="af695-664">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="af695-664">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="af695-665">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="af695-665">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="af695-666">Bir Depolama hesabının Blob Hizmeti üzerinde sürüm oluşturmayı etkinleştirmeye/devre dışı bırakmaya yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-666">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="af695-667">“Update-AzStorageBlobServiceProperty”</span><span class="sxs-lookup"><span data-stu-id="af695-667">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="af695-668">Blob sürümlerini içeren destek listesi blobları</span><span class="sxs-lookup"><span data-stu-id="af695-668">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="af695-669">“Get-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="af695-669">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="af695-670">Tek bir blob anlık görüntüsünü veya blob sürümünü almaya/kaldırmaya yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-670">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="af695-671">“Get-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="af695-671">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="af695-672">“Remove-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="af695-672">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="af695-673">Azure.Storage.Blobs V12’den oluşturulan blob nesnesindeki işlem hattına yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-673">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="af695-674">“Get-AzStorageBlobContent”</span><span class="sxs-lookup"><span data-stu-id="af695-674">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="af695-675">“New-AzStorageBlobSASToken”</span><span class="sxs-lookup"><span data-stu-id="af695-675">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="af695-676">“Remove-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="af695-676">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="af695-677">“Set-AzStorageBlobContent”</span><span class="sxs-lookup"><span data-stu-id="af695-677">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="af695-678">“Start-AzStorageBlobCopy”</span><span class="sxs-lookup"><span data-stu-id="af695-678">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="af695-679">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="af695-679">Az.StorageSync</span></span>
* <span data-ttu-id="af695-680">ApiVersion 2020-03-01 sürümünü hedefleyen yeni bir StorageSync SDK sürümü eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-680">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="af695-681">“UpdateStorageSyncService” cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-681">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="af695-682">“Set-AzStorageSyncService”</span><span class="sxs-lookup"><span data-stu-id="af695-682">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="af695-683">StorageSyncService cmdlet’ine IncomingTrafficPolicy ve PrivateEndpointConnections eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-683">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="af695-684">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="af695-684">Az.Websites</span></span>
* <span data-ttu-id="af695-685">App Service Planıyla aynı kaynak grubunda bulunmayan Yuvalar için işlem gerçekleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-685">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="af695-686">4.3.0 - Haziran 2020</span><span class="sxs-lookup"><span data-stu-id="af695-686">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="af695-687">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="af695-687">Az.Accounts</span></span>
* <span data-ttu-id="af695-688">Ortam ayarını varsayılan olarak bulma ve 'Add-AzEnvironment' aracılığıyla ortam ekleme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-688">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="af695-689">Önceden yüklenmiş bütünleştirilmiş kodlar güncelleştirildi [#12024], [#11976]</span><span class="sxs-lookup"><span data-stu-id="af695-689">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="af695-690">Azure.Core bütünleştirilmiş kodu güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-690">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="af695-691">'Connect-AzAccount' cmdlet’inin çok iş parçacıklı yürütmede başarısız olmasına neden olabilen bir sorun düzeltildi [#11201]</span><span class="sxs-lookup"><span data-stu-id="af695-691">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="af695-692">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="af695-692">Az.Aks</span></span>
* <span data-ttu-id="af695-693">Eski [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile)’sinin kullanımı [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) ve [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) API’lerine yönelik çağrılarla değiştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-693">Replaced usage of old [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="af695-694">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="af695-694">Az.Batch</span></span>
* <span data-ttu-id="af695-695">Az.Batch, 'Microsoft.Azure.Management.Batch' SDK sürüm 11.0.0 kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-695">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="af695-696">BatchAccount.Identity özelliğini 'New-AzBatchAccount' cmdlet’ine ayarlama özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-696">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="af695-697">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="af695-697">Az.CognitiveServices</span></span>
* <span data-ttu-id="af695-698">Hesap özelliklerini görüntüleme desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-698">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="af695-699">PublicNetworkAccess özelliğinin değiştirilmesi desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-699">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="af695-700">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="af695-700">Az.Compute</span></span>
* <span data-ttu-id="af695-701">Set-AzVM ve Set-AzVmssVM cmdlet’lerine SimulateEviction parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-701">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="af695-702">New-AzGalleryImageVersion cmdlet’i için StorageAccountType parametresinin bağımsız değişken tamamlayıcısına 'Premium_LRS' eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-702">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="af695-703">VMCustomScriptExtension için Alt Durumlar eklendi [#11297]</span><span class="sxs-lookup"><span data-stu-id="af695-703">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="af695-704">New-AzVM ve New-AzVMConfig cmdlet’leri için EvictionPolicy parametresinin bağımsız değişken tamamlayıcısına 'Delete' eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-704">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="af695-705">SAP için yeni VM Uzantısı’nın adı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-705">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="af695-706">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="af695-706">Az.DataFactory</span></span>
* <span data-ttu-id="af695-707">ADF .NET SDK’sı 4.9.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-707">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="af695-708">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="af695-708">Az.EventHub</span></span>
* <span data-ttu-id="af695-709">'New-AzEventHubNamespace' ve 'Set-AzEventHubNamespace' cmdlet’lerine Yönetilen Kimlik parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-709">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="af695-710">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="af695-710">Az.Functions</span></span>
* <span data-ttu-id="af695-711">PowerShell 7.0 ve Java 11 işlev uygulamaları oluşturma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-711">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="af695-712">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="af695-712">Az.HDInsight</span></span>
* <span data-ttu-id="af695-713">HDInsight kümesinin konaklarını listeleme ve belirli konaklarını yeniden başlatma desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-713">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="af695-714">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="af695-714">Az.HealthcareApis</span></span>
* <span data-ttu-id="af695-715">SDK sürümü 1.1.0 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-715">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="af695-716">Dışarı aktarma ayarları ve Yönetilen Kimlik desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-716">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="af695-717">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="af695-717">Az.Monitor</span></span>
* <span data-ttu-id="af695-718">'Set-AzActivityLogAlert' için giriş nesnesi parametresi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-718">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="af695-719">'Set-AzActionGroup' için 'InputObject' parametresi düzeltildi [#10868]</span><span class="sxs-lookup"><span data-stu-id="af695-719">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="af695-720">Az.Network</span><span class="sxs-lookup"><span data-stu-id="af695-720">Az.Network</span></span>
* <span data-ttu-id="af695-721">'Remove-AzExpressRouteCircuitConnectionConfig' cmdlet’ine yönelik AddressPrefixType parametresi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-721">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="af695-722">Azure FirewallPolicy için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-722">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="af695-723">'New-AzFirewallPolicyDnsSetting'</span><span class="sxs-lookup"><span data-stu-id="af695-723">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="af695-724">Güvenlik Duvarı İlkesi için Ağ Kuralları’nda Hedef FQDN Desteği</span><span class="sxs-lookup"><span data-stu-id="af695-724">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="af695-725">Arka uç adres havuzu işlemlerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-725">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="af695-726">'New-AzLoadBalancerBackendAddressConfig'</span><span class="sxs-lookup"><span data-stu-id="af695-726">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="af695-727">'New-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="af695-727">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="af695-728">'Set-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="af695-728">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="af695-729">'Remove-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="af695-729">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="af695-730">'Get-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="af695-730">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="af695-731">'New-AzIpGroup' için ad doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-731">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="af695-732">Azure FirewallPolicy için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-732">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="af695-733">'New-AzFirewallPolicyThreatIntelWhitelist'</span><span class="sxs-lookup"><span data-stu-id="af695-733">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="af695-734">Özellik için aşağıdaki komutlar güncelleştirildi: VirtualWan P2SVpnGateway üzerinde özel DNS sunucuları ayarlama/kaldırma.</span><span class="sxs-lookup"><span data-stu-id="af695-734">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="af695-735">New-AzP2sVpnGateway güncelleştirildi: Müşterilerin DNS sunucularını, Noktadan siteye işlemciler tarafından kullanılabilen P2SVpnGateway üzerinde ayarlanacak şekilde belirtmeleri için '-CustomDnsServer' isteğe bağlı parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-735">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="af695-736">Update-AzP2sVpnGateway güncelleştirildi: Müşterilerin DNS sunucularını, Noktadan siteye işlemciler tarafından kullanılabilen P2SVpnGateway üzerinde ayarlanacak şekilde belirtmeleri için '-CustomDnsServer' isteğe bağlı parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-736">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="af695-737">'Update-AzVpnGateway' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-737">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="af695-738">Müşterilerin özel BGP’lerini VpnGateway üzerinde ayarlanacak şekilde belirtmeleri için '-BgpPeeringAddress' isteğe bağlı parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-738">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="af695-739">Bir VirtualHub kaynağının yönlendirme durumunu sıfırlamayı desteklemek amacıyla yeni cmdlet eklendi:</span><span class="sxs-lookup"><span data-stu-id="af695-739">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="af695-740">'Reset-AzHubRouter'</span><span class="sxs-lookup"><span data-stu-id="af695-740">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="af695-741">Güvenlik Duvarı İlkesi’nde yapılan son Swagger değişikliğine göre aşağıdakiler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-741">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="af695-742">RuleGroup, RuleCollectionGroup ve RuleType adları değiştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-742">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="af695-743">Birden çok NAT Kural Koleksiyonu’nu desteklemek amacıyla Güvenlik Duvarı İlkesi NAT Kural Koleksiyonları’na yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-743">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="af695-744">[Yeni Değişiklik] 'New-AzFirewallPolicyApplicationRule' ve 'New-AzFirewallPolicyNetworkRule' için 'SourceIpGroup' zorunlu parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-744">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="af695-745">[Yeni Değişiklik] 'New-AzFirewallPolicyApplicationRule', 'SourceAddress' parametresi zorunlu olacak şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-745">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="af695-746">[Yeni Değişiklik] 'New-AzFirewallPolicyApplicationRule', 'SourceAddress' parametresi zorunlu olacak şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-746">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="af695-747">[Yeni Değişiklik] Şu zorunu parametreler kaldırıldı: 'New-AzFirewallPolicyNatRuleCollection' için 'TranslatedAddress', 'TranslatedPort'.</span><span class="sxs-lookup"><span data-stu-id="af695-747">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="af695-748">Application Gateway üzerinde PrivateLink’i destekleyecek yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-748">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="af695-749">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="af695-749">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="af695-750">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="af695-750">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="af695-751">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="af695-751">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="af695-752">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="af695-752">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="af695-753">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="af695-753">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="af695-754">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span><span class="sxs-lookup"><span data-stu-id="af695-754">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="af695-755">VirtualHub’ın HubRouteTables alt kaynağı için yeni cmdlet’ler eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-755">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="af695-756">'New-AzVHubRoute'</span><span class="sxs-lookup"><span data-stu-id="af695-756">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="af695-757">'New-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="af695-757">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="af695-758">'Get-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="af695-758">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="af695-759">'Update-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="af695-759">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="af695-760">'Remove-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="af695-760">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="af695-761">Mevcut cmdlet’ler VirtualWan’deki özel yönlendirmede isteğe bağlı RoutingConfiguration giriş parametresini destekleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-761">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="af695-762">'New-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="af695-762">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="af695-763">'Set-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="af695-763">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="af695-764">‘New-AzVirtualHubVnetConnection’</span><span class="sxs-lookup"><span data-stu-id="af695-764">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="af695-765">‘Update-AzVirtualHubVnetConnection’</span><span class="sxs-lookup"><span data-stu-id="af695-765">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="af695-766">'New-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="af695-766">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="af695-767">'Update-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="af695-767">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="af695-768">'New-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="af695-768">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="af695-769">'Update-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="af695-769">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="af695-770">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="af695-770">Az.OperationalInsights</span></span>
* <span data-ttu-id="af695-771">PSWorkspace’in OperationalInsightsWorkspace’i uygulamamasıyla ilgili hata düzeltildi [#12135]</span><span class="sxs-lookup"><span data-stu-id="af695-771">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="af695-772">'Set-AzOperationalInsightsWorkspace' cmdlet’indeki 'Sku' parametresinin geçerli değer kümesine 'pergb2018' eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-772">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="af695-773">'FunctionParameter' parametresi için 'FunctionParameters' diğer adı eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-773">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="af695-774">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="af695-774">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="af695-775">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="af695-775">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="af695-776">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="af695-776">Az.RecoveryServices</span></span>
* <span data-ttu-id="af695-777">Azure Backup’a MAB öğelerini getirme desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-777">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="af695-778">Azure Site Recovery, 'StandardSSD_LRS' disk türünü destekler</span><span class="sxs-lookup"><span data-stu-id="af695-778">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="af695-779">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="af695-779">Az.Resources</span></span>
* <span data-ttu-id="af695-780">'PSADUser' değerine 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname' eklendi [#10526] [#10497]</span><span class="sxs-lookup"><span data-stu-id="af695-780">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="af695-781">'Get-AzADUser' üzerinde '-Mail' değerinin çalışmamasıyla ilgili sorun düzeltildi [#11981]</span><span class="sxs-lookup"><span data-stu-id="af695-781">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="af695-782">'Get-AzDeploymentWhatIfResult' ve 'Get-AzResourceGroupDeploymentWhatIfResult' cmdlet’lerine -ExcludeChangeType' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-782">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="af695-783">'New-AzDeployment' ve 'New-AzResourceGroupDeployment' cmdlet’lerine '-WhatIfExcludeChangeType' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-783">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="af695-784">'Test-Az\*Deployment' cmdlet’leri daha iyi hata iletileri gösterecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-784">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="af695-785">deployment create ve What-If cmdlet’lerinin '-Name' parametresine yönelik yardım iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-785">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="af695-786">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="af695-786">Az.Sql</span></span>
* <span data-ttu-id="af695-787">SQL Server Azure Active Directory Yönetici cmdlet’ine hizmet sorumlusu desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-787">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="af695-788">Veri Sınıflandırma cmdlet’lerindeki eşitleme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-788">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="af695-789">'Set-AzSqlServerActiveDirectoryAdministrator' üzerinde postaya göre kullanıcı arama desteği eklendi [#12192]</span><span class="sxs-lookup"><span data-stu-id="af695-789">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="af695-790">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="af695-790">Az.Storage</span></span>
* <span data-ttu-id="af695-791">RequireInfrastructureEncryption ile Depolama hesabı oluşturma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-791">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="af695-792">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="af695-792">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="af695-793">Azure.Core yükleme mantığı Az.Accounts’a taşındı</span><span class="sxs-lookup"><span data-stu-id="af695-793">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="af695-794">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="af695-794">Az.Websites</span></span>
* <span data-ttu-id="af695-795">'Restore-AzDeletedWebApp' cmdlet’inde geri yüklemenin başarısız olması durumunda, oluşturulan web uygulamasının silinmesine yönelik koruma eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-795">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="af695-796">'New-AzWebApp' ve 'New-AzWebAppSlot' için SourceWebApp.Location' eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-796">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="af695-797">'Set-AzWebApp' ve 'Set-AzWebAppSlot' cmdlet’lerinde Kapsayıcı ayarlarının değiştirilmesini engelleyen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-797">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="af695-798">Get-AzWebApp için -Name verilmediğinde SiteConfig alınmasıyla ilgili hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-798">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="af695-799">Linux Uygulamaları için ASP oluşturmaya yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-799">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="af695-800">Kaynak grupları arasında kopyalama için özel durumlar eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-800">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="af695-801">4.2.0 - Haziran 2020</span><span class="sxs-lookup"><span data-stu-id="af695-801">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="af695-802">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="af695-802">Az.Accounts</span></span>
* <span data-ttu-id="af695-803">Azure Otomasyonu veya PowerShell işlerinde Az’nin günlükleri atlamasına neden olabilecek bir sorun düzeltildi [#11492]</span><span class="sxs-lookup"><span data-stu-id="af695-803">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="af695-804">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="af695-804">Az.AnalysisServices</span></span>
* <span data-ttu-id="af695-805">Veri düzlemi cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-805">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="af695-806">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="af695-806">Az.ApiManagement</span></span>
* <span data-ttu-id="af695-807">Hizmet yönetimi cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-807">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="af695-808">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="af695-808">Az.Billing</span></span>
* <span data-ttu-id="af695-809">Tüketim cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-809">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="af695-810">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="af695-810">Az.CognitiveServices</span></span>
* <span data-ttu-id="af695-811">PrivateEndpoint ve PublicNetworkAccess denetimini destekler.</span><span class="sxs-lookup"><span data-stu-id="af695-811">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="af695-812">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="af695-812">Az.DataFactory</span></span>
* <span data-ttu-id="af695-813">Veri fabrikası V2 cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-813">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="af695-814">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="af695-814">Az.DataShare</span></span>
* <span data-ttu-id="af695-815">''Az.DataShare'' modülü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="af695-815">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="af695-816">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="af695-816">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="af695-817">''Az.DesktopVirtualization'' modülü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="af695-817">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="af695-818">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="af695-818">Az.OperationalInsights</span></span>
* <span data-ttu-id="af695-819">SDK 0.21.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-819">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="af695-820">İsteğe bağlı aşağıdaki parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-820">Added optional parameters to</span></span> 
    - <span data-ttu-id="af695-821">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="af695-821">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="af695-822">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="af695-822">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="af695-823">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="af695-823">Az.PolicyInsights</span></span>
* <span data-ttu-id="af695-824">'Start-AzPolicyComplianceScan' için 3. örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-824">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="af695-825">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="af695-825">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="af695-826">PowerBI cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-826">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="af695-827">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="af695-827">Az.PrivateDns</span></span>
* <span data-ttu-id="af695-828">Remove-AzPrivateDnsRecordSet için ayrıntılı çıkış dizesi biçimlendirmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-828">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="af695-829">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="af695-829">Az.RecoveryServices</span></span>
* <span data-ttu-id="af695-830">XML girişinden bölgeler arasında çoğaltma için kurtarma planı oluşturmaya yönelik Azure Site Recovery desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-830">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="af695-831">SiteRecovery ve Backup cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-831">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="af695-832">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="af695-832">Az.Resources</span></span>
* <span data-ttu-id="af695-833">Get-AzDeploymentScriptLog ve Save-AzDeploymentScriptLog cmdlet’lerine Tail parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-833">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="af695-834">Çıkış özelliği biçimlendirildi ve Get-AzDeploymentScript cmdlet çıkışında gösterildi</span><span class="sxs-lookup"><span data-stu-id="af695-834">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="af695-835">-DeploymentScriptInputObject parametresinin adı -DeploymentScriptObject olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-835">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="af695-836">Cmdlet iletilerinde geçersiz dosya/hedef adı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-836">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="af695-837">Kaynak yöneticisi ve etiketler cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-837">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="af695-838">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="af695-838">Az.Sql</span></span>
* <span data-ttu-id="af695-839">'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' ve 'Update-AzSqlSyncMember' öğelerine UsePrivateLinkConnection eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-839">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="af695-840">'New-AzSqlSyncMember' ve 'Update-AzSqlSyncMember' öğelerine SyncMemberAzureDatabaseResourceId eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-840">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="af695-841">SQL Server Azure Active Directory Yönetici cmdlet’ine Konuk kullanıcı arama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-841">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="af695-842">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="af695-842">Az.Storage</span></span>
* <span data-ttu-id="af695-843">Veri düzlemi cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-843">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="af695-844">4.1.0 - Mayıs 2020</span><span class="sxs-lookup"><span data-stu-id="af695-844">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="af695-845">Son sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="af695-845">Highlights since the last release</span></span>
* <span data-ttu-id="af695-846">Desteklenen PowerShell sürümleri: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="af695-846">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="af695-847">Az.Functions genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="af695-847">General availability of Az.Functions</span></span> 
* <span data-ttu-id="af695-848">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources ve Az.Storage için ana sürüm yayımlandı</span><span class="sxs-lookup"><span data-stu-id="af695-848">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="af695-849">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="af695-849">Az.Accounts</span></span>
* <span data-ttu-id="af695-850">'Add-AzEnvironment' ve 'Set-AzEnvironment', 'AzureSynapseAnalyticsEndpointResourceId' ve 'AzureSynapseAnalyticsEndpointSuffix' parametrelerini kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-850">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="af695-851">Azure.Core ile ilgili bütünleştirilmiş kodlar Az.Accounts’a eklendi, desteklenen PowerShell platformları Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+ sürümlerini içerir</span><span class="sxs-lookup"><span data-stu-id="af695-851">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="af695-852">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="af695-852">Az.Aks</span></span>
* <span data-ttu-id="af695-853">API Sürümü 2019-10-01’e yükseltildi</span><span class="sxs-lookup"><span data-stu-id="af695-853">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="af695-854">Windows kapsayıcısı kullanılarak AKS oluşturma desteği sunuldu</span><span class="sxs-lookup"><span data-stu-id="af695-854">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="af695-855">Yeni cmdlet’ler sağlandı: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span><span class="sxs-lookup"><span data-stu-id="af695-855">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="af695-856">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="af695-856">Az.ApiManagement</span></span>
* <span data-ttu-id="af695-857">'New-AzApiManagement' ve 'Set-AzApiManagement': [-AssignIdentity] parametresi [-SystemAssignedIdentity] olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="af695-857">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="af695-858">'New-AzApiManagement' ve 'Set-AzApiManagement': Yeni parametre eklendi: [-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="af695-858">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="af695-859">'Get-AzApiManagementProperty': 'Get-AzApiManagementNamedValue' olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="af695-859">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="af695-860">PropertyId parametresi NamedValueId olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="af695-860">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="af695-861">'New-AzApiManagementProperty': 'New-AzApiManagementNamedValue' olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="af695-861">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="af695-862">PropertyId parametresi NamedValueId olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="af695-862">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="af695-863">'Set-AzApiManagementProperty': 'Set-AzApiManagementNamedValue' olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="af695-863">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="af695-864">PropertyId parametresi NamedValueId olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="af695-864">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="af695-865">'Remove-AzApiManagementProperty': 'Remove-AzApiManagementNamedValue' olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="af695-865">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="af695-866">PropertyId parametresi NamedValueId olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="af695-866">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="af695-867">Yeni 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet’i eklendi. 'Get-AzApiManagementAuthorizationServer' artık istemci gizli dizisini döndürmez.</span><span class="sxs-lookup"><span data-stu-id="af695-867">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="af695-868">Yeni 'Get-AzApiManagementNamedValueSecretValue' cmdlet’i eklendi. 'Get-AzApiManagementNamedValue' artık gizli dizi değerini döndürmez.</span><span class="sxs-lookup"><span data-stu-id="af695-868">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="af695-869">Yeni 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet’i eklendi. 'Get-AzApiManagementOpenIdConnectProvider' artık istemci gizli dizisini döndürmez.</span><span class="sxs-lookup"><span data-stu-id="af695-869">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="af695-870">Yeni 'Get-AzApiManagementSubscriptionKey' cmdlet’i eklendi. 'Get-AzApiManagementSubscription' artık abonelik anahtarlarını döndürmez.</span><span class="sxs-lookup"><span data-stu-id="af695-870">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="af695-871">Yeni 'Get-AzApiManagementTenantAccessSecret' cmdlet’i eklendi. 'Get-AzApiManagementTenantAccess' artık anahtarları döndürmez.</span><span class="sxs-lookup"><span data-stu-id="af695-871">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="af695-872">Yeni 'Get-AzApiManagementTenantGitAccessSecret' cmdlet’i eklendi. 'Get-AzApiManagementTenantGitAccess' artık anahtarları döndürmez.</span><span class="sxs-lookup"><span data-stu-id="af695-872">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="af695-873">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="af695-873">Az.ApplicationInsights</span></span>
* <span data-ttu-id="af695-874">Parametreler eklendi: 'New-AzApplicationInsights' için 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery'</span><span class="sxs-lookup"><span data-stu-id="af695-874">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="af695-875">'Update-AzApplicationInsights' cmdlet’i oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="af695-875">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="af695-876">Bağlı Depolama Hesapları için cmdlet’ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="af695-876">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="af695-877">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="af695-877">Az.Batch</span></span>
* <span data-ttu-id="af695-878">Az.Batch, 'Microsoft.Azure.Batch' SDK sürüm 13.0.0 ve 'Microsoft.Azure.Management.Batch' SDK sürüm 9.0.0 kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-878">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="af695-879">'New-AzBatchCertificate' için yeni '-CertificateKind' parametresi kullanılarak eklenen sertifika türünü seçme yeteneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-879">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="af695-880">Önceden hep '' olan 'ApplicationPackages' özelliği 'PSApplication' öğesinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="af695-880">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="af695-881">Uygulamanın içindeki belirli paketler artık 'Get-AzBatchApplicationPackage' kullanılarak alınabilir.</span><span class="sxs-lookup"><span data-stu-id="af695-881">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="af695-882">Örneğin: 'Get-AzBatchApplication -AccountName hesabım -ResourceGroupName kaynakgrubum -ApplicationId uygulamam'.</span><span class="sxs-lookup"><span data-stu-id="af695-882">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="af695-883">'New-AzBatchPool' kullanılarak havuz oluşturulurken, 'PSImageReference' öğesinin 'VirtualMachineImageId' özelliği artık yalnızca bir Paylaşılan Görüntü Galerisi görüntüsüne başvurabilir.</span><span class="sxs-lookup"><span data-stu-id="af695-883">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="af695-884">'New-AzBatchPool' kullanılarak havuz oluşturulurken, havuz 'PSNetworkConfiguration' öğesinin yeni 'PublicIPAddressConfiguration' özelliği kullanılarak genel IP olmadan sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="af695-884">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="af695-885">'PSNetworkConfiguration' öğesinin 'PublicIPs' özelliği de 'PSPublicIPAddressConfiguration' içine taşındı.</span><span class="sxs-lookup"><span data-stu-id="af695-885">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="af695-886">Bu özellik yalnızca 'IPAddressProvisioningType' değeri 'UserManaged' olduğunda belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="af695-886">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="af695-887">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="af695-887">Az.Compute</span></span>
* <span data-ttu-id="af695-888">'Update-AzVM' cmdlet’ine HostId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-888">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="af695-889">'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' ve 'Set-AzVmssOsProfile' cmdlet’leri için Yardım belgeleri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-889">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="af695-890">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="af695-890">Breaking changes</span></span>
    - <span data-ttu-id="af695-891">FilterExpression parametresi 'Get-AzVMImage' cmdlet’inden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="af695-891">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="af695-892">AssignIdentity parametresi 'New-AzVmssConfig', 'New-AzVMConfig' ve 'Update-AzVM' cmdlet’lerinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="af695-892">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="af695-893">AutomaticRepairMaxInstanceRepairsPercent, 'New-AzVmssConfig' ve 'Update-AzVmss' cmdlet’lerinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="af695-893">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="af695-894">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus ve VirtualMachineScaleSetsColocationStatus özellikleri ProximityPlacementGroup öğesinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="af695-894">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="af695-895">MaxInstanceRepairsPercent özelliği AutomaticRepairsPolicy öğesinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="af695-895">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="af695-896">AvailabilitySets, VirtualMachines ve VirtualMachineScaleSets türleri IList<SubResource> türünden IList<SubResourceWithColocationStatus> türüne değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-896">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="af695-897">'Get-AzVM' cmdlet’inin açıklaması, cmdlet’i daha iyi açıklayacak biçimde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-897">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="af695-898">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="af695-898">Az.DataFactory</span></span>
* <span data-ttu-id="af695-899">Yönetilen IR içinde veri akışı çalışma zamanı özelliklerinin CRUD’si desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-899">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="af695-900">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="af695-900">Az.FrontDoor</span></span>
* <span data-ttu-id="af695-901">Front Door Kural Altyapısı nesnesini oluşturmak, güncelleştirmek, almak ve silmek için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-901">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="af695-902">Front Door Kural Altyapısı nesnesini oluşturmak için yardımcı cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-902">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="af695-903">Front Door Yönlendirme Kuralı nesnesine Kural Altyapısı başvurusu eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-903">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="af695-904">Front Door Arka Uç nesnesine Özel Bağlantı parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-904">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="af695-905">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="af695-905">Az.Functions</span></span>
* <span data-ttu-id="af695-906">''Az.Functions'' modülü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="af695-906">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="af695-907">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="af695-907">Az.HDInsight</span></span>
* <span data-ttu-id="af695-908">Müşteri tarafından yönetilen anahtar disk şifrelemesi desteği sunuldu.</span><span class="sxs-lookup"><span data-stu-id="af695-908">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="af695-909">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="af695-909">Az.HealthcareApis</span></span>
* <span data-ttu-id="af695-910">Erişim ilkeleri artık varsayılan olarak geçerli sorumluyu kullanmıyor</span><span class="sxs-lookup"><span data-stu-id="af695-910">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="af695-911">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="af695-911">Az.IotHub</span></span>
* <span data-ttu-id="af695-912">SQL benzeri bir dil kullanarak bilgi almak üzere bir IoT hub’ında sorgu çağırmak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-912">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="af695-913">'Add-AzIotHubDevice' cmdlet’inin alt cihaz olmadan Uç Özellikli Cihaz oluşturamaması sorunu düzeltildi [#11597]</span><span class="sxs-lookup"><span data-stu-id="af695-913">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="af695-914">IoT hub’ı, cihaz veya modül için SAS belirteci oluşturmak üzere cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-914">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="af695-915">Yapılandırma ölçümleri sorgusunu çağırmak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-915">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="af695-916">IoT Edge otomatik dağıtımını büyük ölçekte yönetin.</span><span class="sxs-lookup"><span data-stu-id="af695-916">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="af695-917">Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="af695-917">New cmdlets are:</span></span>
    - <span data-ttu-id="af695-918">'Add-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="af695-918">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="af695-919">'Get-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="af695-919">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="af695-920">'Remove-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="af695-920">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="af695-921">'Set-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="af695-921">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="af695-922">IoT Edge dağıtım ölçümleri sorgusunu çağırmak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-922">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="af695-923">Yapılandırma içeriğini belirtilen uç cihaza uygulamak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-923">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="af695-924">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="af695-924">Az.KeyVault</span></span>
* <span data-ttu-id="af695-925">İki diğer ad kaldırıldı: 'New-AzKeyVaultCertificateAdministratorDetails' ve 'New-AzKeyVaultCertificateOrganizationDetails'</span><span class="sxs-lookup"><span data-stu-id="af695-925">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="af695-926">Anahtar kasası oluştururken varsayılan olarak geçici silme etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-926">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="af695-927">Ağ kuralları, bir anahtar kasası oluştururken belirli ağ konumlarından erişilebilirliği yönetecek şekilde ayarlanabilir</span><span class="sxs-lookup"><span data-stu-id="af695-927">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="af695-928">Kendi anahtarını getir (BYOK) desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-928">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="af695-929">'Add-AzKeyVaultKey' anahtar değişim anahtarı oluşturmayı destekler</span><span class="sxs-lookup"><span data-stu-id="af695-929">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="af695-930">'Get-AzKeyVaultKey' genel bir anahtarı PEM biçiminde indirmeyi destekler</span><span class="sxs-lookup"><span data-stu-id="af695-930">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="af695-931">'Add-AzKeyVaultKey' yardım belgesinin 'KeyOps' bölümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-931">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="af695-932">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="af695-932">Az.Monitor</span></span>
* <span data-ttu-id="af695-933">'Set-AzDiagnosticSettings' için saklama ilkesinin tüm kategorilere uygulanmadığı hata düzeltildi [#11589]</span><span class="sxs-lookup"><span data-stu-id="af695-933">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="af695-934">Ölçüm uyarısı V2 için WebTest kullanılabilirlik ölçütleri desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-934">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="af695-935">'New-AzMetricAlertRuleV2Criteria': Web testi kullanılabilirlik ölçütü oluşturma seçeneği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-935">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="af695-936">'Add-AzMetricAlertRuleV2': Yeni web testi kullanılabilirlik ölçütünü destekler</span><span class="sxs-lookup"><span data-stu-id="af695-936">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="af695-937">PSLogProfile içinde RetentionPolicy için gereksiz tanım kaldırıldı [#7608]</span><span class="sxs-lookup"><span data-stu-id="af695-937">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="af695-938">PSEventData içinde tanımlanan gereksiz özellikler kaldırıldı [#11353]</span><span class="sxs-lookup"><span data-stu-id="af695-938">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="af695-939">'Get-AzLog', 'Get-AzActivityLog' olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="af695-939">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="af695-940">Az.Network</span><span class="sxs-lookup"><span data-stu-id="af695-940">Az.Network</span></span>
* <span data-ttu-id="af695-941">Bölge varsayılan davranışının değiştirileceğini bildirmek için hataya neden olan değişiklik özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-941">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="af695-942">'New-AzPublicIpAddress'</span><span class="sxs-lookup"><span data-stu-id="af695-942">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="af695-943">'New-AzPublicIpPrefix'</span><span class="sxs-lookup"><span data-stu-id="af695-943">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="af695-944">'New-AzLoadBalancerFrontendIpConfig'</span><span class="sxs-lookup"><span data-stu-id="af695-944">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="af695-945">Yeni üst düzey SecurityPartnerProvider kaynağı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-945">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="af695-946">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="af695-946">New cmdlets added:</span></span>
        - <span data-ttu-id="af695-947">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="af695-947">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="af695-948">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="af695-948">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="af695-949">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="af695-949">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="af695-950">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="af695-950">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="af695-951">'PSPrivateLinkResource' üzerinde 'RequiredZoneNames' ve 'PSPrivateEndpointConnection' üzerinde 'GroupId' eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-951">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="af695-952">New-AzNetworkWatcherConnectionMonitorTestConfigurationObject için SuccessThresholdRoundTripTimeMs parametresinin hatalı türü düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-952">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="af695-953">VirtualWan cmdlet’leri AllowVnetToVnetTraffic bağımsız değişkeninin varsayılan değerini True olarak ayarlayacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-953">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="af695-954">'New-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="af695-954">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="af695-955">'Update-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="af695-955">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="af695-956">Özel uç nokta için DNS bölgesi grubunu desteklemek amacıyla yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-956">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="af695-957">'New-AzPrivateDnsZoneConfig'</span><span class="sxs-lookup"><span data-stu-id="af695-957">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="af695-958">'Get-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="af695-958">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="af695-959">'New-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="af695-959">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="af695-960">'Set-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="af695-960">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="af695-961">'Remove-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="af695-961">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="af695-962">'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' ve 'DNSServers' parametreleri 'AzureFirewall' öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-962">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="af695-963">'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' ve 'DnsServer' parametreleri 'AzureFirewall' öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-963">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="af695-964">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="af695-964">Updated cmdlet:</span></span>
        - <span data-ttu-id="af695-965">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="af695-965">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="af695-966">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="af695-966">Az.OperationalInsights</span></span>
* <span data-ttu-id="af695-967">Yeni oluşturulan SDK’yı uygulamak için eski kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-967">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="af695-968">Kullanımdan kaldırılan API’ler nedeniyle silinen cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="af695-968">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="af695-969">'Get-AzOperationalInsightsSavedSearchResult' (diğer adı 'Get-AzOperationalInsightsSavedSearchResults')</span><span class="sxs-lookup"><span data-stu-id="af695-969">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="af695-970">'Get-AzOperationalInsightsSearchResult' (diğer adı 'Get-AzOperationalInsightsSearchResults')</span><span class="sxs-lookup"><span data-stu-id="af695-970">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="af695-971">'Get-AzOperationalInsightsLinkTarget' (diğer adı 'Get-AzOperationalInsightsLinkTargets')</span><span class="sxs-lookup"><span data-stu-id="af695-971">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="af695-972">'Set-AzOperationalInsightsWorkspace' ve 'New-AzOperationalInsightsWorkspace' için parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-972">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="af695-973">Bağlı Depolama Hesabı için cmdlet’ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="af695-973">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="af695-974">Kümeler ve Bağlı Hizmet için cmdlet’ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="af695-974">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="af695-975">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="af695-975">Az.RecoveryServices</span></span>
* <span data-ttu-id="af695-976">Azure Site Recovery’de Azure’dan Azure’a sağlayıcı için yakın yerleştirilen grup sanal makinelerini korumak üzere destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-976">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="af695-977">Azure Site Recovery’de bölgeden bölgeye çoğaltma için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-977">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="af695-978">Azure Backup’ta Azure Dosya Paylaşımı Kurtarma Noktaları için uzun süreli saklama desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-978">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="af695-979">Azure Backup’ta 'Get-AzRecoveryServicesBackupItem' cmdlet’inin çıkışına disk hariç tutma özellikleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-979">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="af695-980">Site Recovery hizmeti için Kasa kimlik bilgilerine yönelik özel uç noktalar eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-980">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="af695-981">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="af695-981">Az.Resources</span></span>
* <span data-ttu-id="af695-982">Yeni bir Rol Tanımı oluşturulurken görüntüleme gecikmesi hakkında ileti uyarısı eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-982">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="af695-983">Kesin tür belirtilmiş nesne çıkışı için ilke cmdlet’leri değiştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-983">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="af695-984">'Get-AzResourceLock' cmdlet’i üzerinde kullanılan '-TenantLevel' parametresi kaldırıldı [#11335]</span><span class="sxs-lookup"><span data-stu-id="af695-984">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="af695-985">'Remove-AzResourceGroup -Id ResourceId' düzeltildi [#9882]</span><span class="sxs-lookup"><span data-stu-id="af695-985">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="af695-986">Kaynak grubu kapsamında ARM şablonu Durum çözümlemesi sonuçlarını almak için yeni cmdlet eklendi: 'Get-AzDeploymentResourceGroupWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="af695-986">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="af695-987">Abonelik kapsamında ARM şablonu Durum çözümlemesi sonuçlarını almak için yeni cmdlet eklendi: 'Get-AzDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="af695-987">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="af695-988">Diğer ad: 'Get-AzSubscriptionDeploymentWhatIf'</span><span class="sxs-lookup"><span data-stu-id="af695-988">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="af695-989">'New-AzDeployment' ve 'New-AzResourceGroupDeployment' için '-WhatIf' ve '-Confirm' parametreleri ARM şablonu Durum sonuçlarını kullanmak için geçersiz kılındı</span><span class="sxs-lookup"><span data-stu-id="af695-989">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="af695-990">Dağıtım cmdlet’lerinde 'ApiVersion' parametresi için kullanımdan kaldırma iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-990">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="af695-991">Dağıtım hataları için iyileştirilmiş hata iletilerini gösterme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-991">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="af695-992">Dağıtım hataları için correlationId’yi günlüğe kaydetme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-992">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="af695-993">Dağıtım betiği çıkışına 'error' özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-993">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="af695-994">NuGet Microsoft.Azure.Management.ResourceManager '3.7.1-preview' sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-994">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="af695-995">DeploymentValidateResult içindeki Error özelliği nuget 3.7.1-preview sürümünden itibaren salt okunur olarak değiştirildiğinden belirli test çalışmaları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="af695-995">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="af695-996">SDK ResourceManager 3.7.1-preview sürümünden GenericResourceExpanded öğesi getirildi</span><span class="sxs-lookup"><span data-stu-id="af695-996">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="af695-997">Dağıtım için tüm Get cmdlet’lerine yönelik etiket desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-997">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="af695-998">'New-AzDeployment'</span><span class="sxs-lookup"><span data-stu-id="af695-998">'New-AzDeployment'</span></span>
    - <span data-ttu-id="af695-999">'New-AzManagementGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="af695-999">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="af695-1000">'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="af695-1000">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="af695-1001">'New-AzTenantDeployment'</span><span class="sxs-lookup"><span data-stu-id="af695-1001">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="af695-1002">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="af695-1002">Az.ServiceFabric</span></span>
* <span data-ttu-id="af695-1003">Yanlış sertifika parmak izini alan --SecretIdentifier parametresini kullanarak sertifika ekleme özelliğindeki hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-1003">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="af695-1004">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="af695-1004">Az.Sql</span></span>
* <span data-ttu-id="af695-1005">Şunların performansı iyileştirildi:</span><span class="sxs-lookup"><span data-stu-id="af695-1005">Enhance performance of:</span></span>
    - <span data-ttu-id="af695-1006">'Set-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="af695-1006">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="af695-1007">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="af695-1007">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="af695-1008">'Remove-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="af695-1008">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="af695-1009">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="af695-1009">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="af695-1010">'Enable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="af695-1010">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="af695-1011">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="af695-1011">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="af695-1012">'Disable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="af695-1012">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="af695-1013">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="af695-1013">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="af695-1014">'Set-AzSqlDatabaseBackupShortTermRetentionPolicy' cmdlet’inden 'RetentionDays' parametresinin istemci tarafı doğrulaması kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="af695-1014">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="af695-1015">Sanal ağ içindeki bir depolama hesabına denetim yapılarak Depolama Blob Verileri Katkıda Bulunan rolünün oluşturulması sırasında karşılaşılan hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-1015">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="af695-1016">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="af695-1016">Az.Storage</span></span>
* <span data-ttu-id="af695-1017">'Get-AzStorageAccount' hesap alma/listeleme cmdlet’ine '-AsJob' eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1017">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="af695-1018">Anahtar otomatik döndürmesini desteklemek için Depolama hesabı KeyvaultEncryption ile güncelleştirilirken KeyVersion isteğe bağlı hale getirildi</span><span class="sxs-lookup"><span data-stu-id="af695-1018">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="af695-1019">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="af695-1019">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="af695-1020">İşlem hattıyla Azure Dosya Dizinini kaldırma hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-1020">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="af695-1021">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="af695-1021">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="af695-1022">Düzeltildi [#9880]: NetWorkRule DefaultAction değer tanımı swagger ile uyumlu olacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-1022">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="af695-1023">'Update-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="af695-1023">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="af695-1024">'Get-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="af695-1024">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="af695-1025">Düzeltildi [#11624]: Sunucu hatasından kaçınmak için NetworkRules eklenirken yinelenen kuralları atla</span><span class="sxs-lookup"><span data-stu-id="af695-1025">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="af695-1026">'Add-AzStorageAccountNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="af695-1026">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="af695-1027">Microsoft.Azure.Cosmos.Table SDK 1.0.7 sürümüne yükseltildi</span><span class="sxs-lookup"><span data-stu-id="af695-1027">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="af695-1028">DataLake 2. Nesil Öğeleri listesinde yalnızca bazı öğeler döndürüldüğünde kullanıcıya ContinuationToken ile yeniden listelemesini anımsatmak için uyarı iletisi eklendi,</span><span class="sxs-lookup"><span data-stu-id="af695-1028">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="af695-1029">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="af695-1029">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="af695-1030">Azure Dosyalar Active Directory Domain Services Kimlik Doğrulaması ile Depolama hesabı oluşturma veya güncelleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1030">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="af695-1031">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="af695-1031">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="af695-1032">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="af695-1032">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="af695-1033">Depolama hesabının Kerberos anahtarlarını yeni oluşturma veya listeleme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1033">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="af695-1034">'New-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="af695-1034">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="af695-1035">'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="af695-1035">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="af695-1036">Yük devretme Depolama hesabı desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1036">Supported failover Storage account</span></span>
    - <span data-ttu-id="af695-1037">'Invoke-AzStorageAccountFailover'</span><span class="sxs-lookup"><span data-stu-id="af695-1037">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="af695-1038">'Get-AzStorageBlobCopyState' yardımı güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-1038">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="af695-1039">'Get-AzStorageFileCopyState' ve 'Start-AzStorageBlobCopy' yardımı güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-1039">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="af695-1040">Depolama istemci kitaplığı v12, Kuyruk ve Dosya cmdlet’leriyle tümleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-1040">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="af695-1041">CloudFile olan çıkış türü AzureStorageFile olarak değiştirildi, özgün çıkış yeni çıkışın bir alt özelliği olacak</span><span class="sxs-lookup"><span data-stu-id="af695-1041">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="af695-1042">'Get-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="af695-1042">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="af695-1043">'Remove-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="af695-1043">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="af695-1044">'Get-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="af695-1044">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="af695-1045">'Set-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="af695-1045">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="af695-1046">'Start-AzStorageFileCopy'</span><span class="sxs-lookup"><span data-stu-id="af695-1046">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="af695-1047">CloudFileDirectory olan çıkış türü AzureStorageFileDirectory olarak değiştirildi, özgün çıkış yeni çıkışın bir alt özelliği olacak</span><span class="sxs-lookup"><span data-stu-id="af695-1047">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="af695-1048">'New-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="af695-1048">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="af695-1049">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="af695-1049">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="af695-1050">CloudFileShare olan çıkış türü AzureStorageFileShare olarak değiştirildi, özgün çıkış yeni çıkışın bir alt özelliği olacak</span><span class="sxs-lookup"><span data-stu-id="af695-1050">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="af695-1051">'Get-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="af695-1051">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="af695-1052">'New-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="af695-1052">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="af695-1053">'Remove-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="af695-1053">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="af695-1054">FileShareProperties olan çıkış türü AzureStorageFileShare olarak değiştirildi, özgün çıkış yeni çıkışın bir alt alt özelliği olacak</span><span class="sxs-lookup"><span data-stu-id="af695-1054">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="af695-1055">'Set-AzStorageShareQuota'</span><span class="sxs-lookup"><span data-stu-id="af695-1055">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="af695-1056">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="af695-1056">Az.TrafficManager</span></span>
* <span data-ttu-id="af695-1057">'DisableAzureTrafficManagerEndpoint' ayrıntılı çıkışındaki hatalı profil adı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-1057">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="af695-1058">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="af695-1058">Az.Websites</span></span>
* <span data-ttu-id="af695-1059">'Update-AzWebAppAccessRestrictionConfig' yardımındaki yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-1059">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="af695-1060">3.8.0 - Nisan 2020</span><span class="sxs-lookup"><span data-stu-id="af695-1060">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="af695-1061">Son sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="af695-1061">Highlights since the last release</span></span>
* <span data-ttu-id="af695-1062">Az.Storage’ın desteklediği PowerShell sürümleri: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="af695-1062">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="af695-1063">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="af695-1063">Az.Accounts</span></span>
* <span data-ttu-id="af695-1064">'Resolve-AzError' içinde Azure PowerShell anket URL’si güncelleştirildi [#11507]</span><span class="sxs-lookup"><span data-stu-id="af695-1064">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="af695-1065">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="af695-1065">Az.ApiManagement</span></span>
* <span data-ttu-id="af695-1066">Sonraki sürümlerde Azure Dosya cmdlet’leri için hataya neden olan değişiklik bildirimi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1066">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="af695-1067">'Set-AzApiManagementGroup' belgeleri GroupId parametresini belirtmek için güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-1067">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="af695-1068">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="af695-1068">Az.Cdn</span></span>
* <span data-ttu-id="af695-1069">ChinaCDN ile ilgili fiyatlandırma SKU’nun görüntüsü düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-1069">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="af695-1070">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="af695-1070">Az.CognitiveServices</span></span>
* <span data-ttu-id="af695-1071">Kimlik, Şifreleme, UserOwnedStorage desteği sağlandı</span><span class="sxs-lookup"><span data-stu-id="af695-1071">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="af695-1072">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="af695-1072">Az.Compute</span></span>
* <span data-ttu-id="af695-1073">'Set-AzVmssOrchestrationServiceState' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-1073">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="af695-1074">-InstanceView ile 'Get-AzVmss', OrchestrationService durumlarını gösteriyor.</span><span class="sxs-lookup"><span data-stu-id="af695-1074">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="af695-1075">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="af695-1075">Az.IotHub</span></span>
* <span data-ttu-id="af695-1076">IoT cihaz ikizi yapılandırmasını yönetme, Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="af695-1076">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="af695-1077">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="af695-1077">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="af695-1078">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="af695-1078">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="af695-1079">IoT Hub’ındaki bir cihazda doğrudan yöntem çağırmak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-1079">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="af695-1080">IoT cihaz modülü ikizi yapılandırmasını yönetme, Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="af695-1080">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="af695-1081">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="af695-1081">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="af695-1082">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="af695-1082">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="af695-1083">Büyük ölçekte IoT otomatik cihaz yönetimi yapılandırmasını yönetin.</span><span class="sxs-lookup"><span data-stu-id="af695-1083">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="af695-1084">Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="af695-1084">New cmdlets are:</span></span>
    - <span data-ttu-id="af695-1085">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="af695-1085">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="af695-1086">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="af695-1086">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="af695-1087">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="af695-1087">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="af695-1088">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="af695-1088">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="af695-1089">Bir IoT Hub’ında kenar modülü yöntemini çağırmak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-1089">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="af695-1090">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="af695-1090">Az.KeyVault</span></span>
* <span data-ttu-id="af695-1091">Bir kasada geçici silme ve temizleme korumasını etkinleştirebilen yeni bir 'Update-AzKeyVault' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1091">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="af695-1092">Microsoft.PowerShell.SecretManagement desteği eklendi [#11178]</span><span class="sxs-lookup"><span data-stu-id="af695-1092">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="af695-1093">'Remove-AzKeyVaultManagedStorageSasDefinition' örneklerindeki hata düzeltildi [#11479]</span><span class="sxs-lookup"><span data-stu-id="af695-1093">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="af695-1094">Özel uç noktaya destek eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1094">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="af695-1095">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="af695-1095">Az.Maintenance</span></span>
* <span data-ttu-id="af695-1096">GA için Bakım cmdlet’lerinin yayın sürümü yayımlanıyor</span><span class="sxs-lookup"><span data-stu-id="af695-1096">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="af695-1097">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="af695-1097">Az.Monitor</span></span>
* <span data-ttu-id="af695-1098">Özel bağlantı kapsamı için cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1098">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="af695-1099">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="af695-1099">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="af695-1100">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="af695-1100">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="af695-1101">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="af695-1101">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="af695-1102">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="af695-1102">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="af695-1103">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="af695-1103">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="af695-1104">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="af695-1104">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="af695-1105">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="af695-1105">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="af695-1106">Az.Network</span><span class="sxs-lookup"><span data-stu-id="af695-1106">Az.Network</span></span>
* <span data-ttu-id="af695-1107">Sanal Ağ Geçidi için özel IP’de bağlantıyı etkinleştirmek üzere cmdlet’ler güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-1107">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="af695-1108">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="af695-1108">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="af695-1109">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="af695-1109">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="af695-1110">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="af695-1110">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="af695-1111">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="af695-1111">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="af695-1112">FQDN tabanlı LocalNetworkGateways ve VpnSites’ı etkinleştirmek için cmdlet’ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-1112">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="af695-1113">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="af695-1113">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="af695-1114">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="af695-1114">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="af695-1115">ExpressRouteCircuitConnectionConfig (Global Reach) içinde IPv6 adres ailesi için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1115">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="af695-1116">'Set-AzExpressRouteCircuitConnectionConfig' eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1116">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="af695-1117">IPv6CircuitConnectionProperties dahil tüm mevcut özelliklerin ayarlanmasına olanak sağlar</span><span class="sxs-lookup"><span data-stu-id="af695-1117">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="af695-1118">'Add-AzExpressRouteCircuitConnectionConfig' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-1118">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="af695-1119">Adres ön ekinin adres ailesini belirtmek için başka bir isteğe bağlı AddressPrefixType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1119">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="af695-1120">Sanal Ağ Geçidi Bağlantılarında DPD Zaman Aşımı ayarlanmasını sağlamak için cmdlet’ler güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-1120">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="af695-1121">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="af695-1121">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="af695-1122">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="af695-1122">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="af695-1123">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="af695-1123">Az.PolicyInsights</span></span>
* <span data-ttu-id="af695-1124">İlke uyumluluğu taramalarını tetiklemek için 'Start-AzPolicyComplianceScan' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1124">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="af695-1125">'Get-AzPolicyState' çıkışına ilke tanımı, küme tanımı ve atama sürümleri eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1125">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="af695-1126">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="af695-1126">Az.ServiceFabric</span></span>
* <span data-ttu-id="af695-1127">'New-AzServiceFabricCluster' örneklerinin kod biçimlendirmesi ve kullanılabilirliği iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-1127">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="af695-1128">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="af695-1128">Az.Sql</span></span>
* <span data-ttu-id="af695-1129">'Get-AzSqlInstanceOperation' ve 'Stop-AzSqlInstanceOperation' cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1129">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="af695-1130">Sanal ağdaki bir depolama hesabının denetlenmesine yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-1130">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="af695-1131">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="af695-1131">Az.Storage</span></span>
* <span data-ttu-id="af695-1132">Sonraki sürümlerde Azure Dosya cmdlet’leri için hataya neden olan değişiklik bildirimi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1132">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="af695-1133">Depolama hesabı oluşturma/güncelleştirme sırasında yeni SkuName StandardGZRS, StandardRAGZRS desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1133">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="af695-1134">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="af695-1134">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="af695-1135">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="af695-1135">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="af695-1136">DataLake Gen2 desteklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1136">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="af695-1137">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="af695-1137">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="af695-1138">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="af695-1138">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="af695-1139">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="af695-1139">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="af695-1140">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="af695-1140">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="af695-1141">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="af695-1141">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="af695-1142">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="af695-1142">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="af695-1143">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="af695-1143">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="af695-1144">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="af695-1144">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="af695-1145">0.10.0-preview - Nisan 2020</span><span class="sxs-lookup"><span data-stu-id="af695-1145">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="af695-1146">Genel</span><span class="sxs-lookup"><span data-stu-id="af695-1146">General</span></span>
* <span data-ttu-id="af695-1147">Az modülleri artık Azure Stack Hub’da önizlemede kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="af695-1147">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="af695-1148">Bu, Linux ve macOs ile platformlar arası uyumluluk sağlar.</span><span class="sxs-lookup"><span data-stu-id="af695-1148">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="af695-1149">Azure Stack Hub artık Az modülleriyle PowerShell Core’u destekliyor, daha fazla bilgiyi [burada](https://aka.ms/az4AzureStack) bulabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="af695-1149">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="af695-1150">Az modülleri profil 2019-03-01-hybrid’i destekliyor:</span><span class="sxs-lookup"><span data-stu-id="af695-1150">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="af695-1151">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="af695-1151">Az.Billing</span></span>
  - <span data-ttu-id="af695-1152">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="af695-1152">Az.Compute</span></span>
  - <span data-ttu-id="af695-1153">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="af695-1153">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="af695-1154">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="af695-1154">Az.EventHub</span></span>
  - <span data-ttu-id="af695-1155">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="af695-1155">Az.IotHub</span></span>
  - <span data-ttu-id="af695-1156">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="af695-1156">Az.KeyVault</span></span>
  - <span data-ttu-id="af695-1157">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="af695-1157">Az.Monitor</span></span>
  - <span data-ttu-id="af695-1158">Az.Network</span><span class="sxs-lookup"><span data-stu-id="af695-1158">Az.Network</span></span>
  - <span data-ttu-id="af695-1159">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="af695-1159">Az.Resources</span></span>
  - <span data-ttu-id="af695-1160">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="af695-1160">Az.Storage</span></span>
  - <span data-ttu-id="af695-1161">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="af695-1161">Az.Websites</span></span>
* <span data-ttu-id="af695-1162">Az için Azure Stack Hub ile çalışan üç yeni PowerShell modülü (Az.Databox, Az.IotHub ve Az.EventHub) kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="af695-1162">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="af695-1163">Komutlar, AzureRM’nin Az olarak değiştirilmesi gibi küçük değişiklikler ile görece aynı kalır</span><span class="sxs-lookup"><span data-stu-id="af695-1163">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="af695-1164">Azure Stack Hub için PowerShell belgelerine güncelleştirilmiş bağlantı [burada](https://aka.ms/InstallASHPowerShell) bulunabilir</span><span class="sxs-lookup"><span data-stu-id="af695-1164">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="af695-1165">3.7.0 - Mart 2020</span><span class="sxs-lookup"><span data-stu-id="af695-1165">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="af695-1166">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="af695-1166">Az.Accounts</span></span>
* <span data-ttu-id="af695-1167">Oturum açılmadığında ‘Get-AzTenant’/’Get-AzDefault’/’Set-AzDefault’ cmdlet’lerinin NullReferenceException hatası oluşturması düzeltildi [#10292]</span><span class="sxs-lookup"><span data-stu-id="af695-1167">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="af695-1168">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="af695-1168">Az.Compute</span></span>
* <span data-ttu-id="af695-1169">‘New-AzDiskConfig’ cmdlet’ine şu parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="af695-1169">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="af695-1170">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="af695-1170">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="af695-1171">Şifreleme özelliğinin ‘New-AzGalleryImageVersion’ cmdlet’inin parametrelerini hedeflemesine izin verildi.</span><span class="sxs-lookup"><span data-stu-id="af695-1171">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="af695-1172">‘Set-AzVmss’ -Reimage ve ‘Invoke-AzVMReimage’ cmdlet’lerine yönelik tempDisk sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-1172">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="af695-1173">[#11354]</span><span class="sxs-lookup"><span data-stu-id="af695-1173">[#11354]</span></span>
* <span data-ttu-id="af695-1174">Aşağıdaki cmdlet’lere yeni SAP uzantısına yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1174">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="af695-1175">‘Set-AzVMAEMExtension’</span><span class="sxs-lookup"><span data-stu-id="af695-1175">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="af695-1176">‘Get-AzVMAEMExtension’</span><span class="sxs-lookup"><span data-stu-id="af695-1176">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="af695-1177">‘Remove-AzVMAEMExtension’</span><span class="sxs-lookup"><span data-stu-id="af695-1177">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="af695-1178">‘Update-AzVMAEMExtension’</span><span class="sxs-lookup"><span data-stu-id="af695-1178">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="af695-1179">Yardım belgelerinde bulunan örneklerdeki hatalar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-1179">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="af695-1180">VM PowerState için tam dize değeri tablo biçiminde gösterildi.</span><span class="sxs-lookup"><span data-stu-id="af695-1180">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="af695-1181">‘New-AzVmssConfig’: SinglePlacementGroup devre dışı bırakıldığında AutomaticRepairs özelliğinin serileştirilmesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-1181">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="af695-1182">[#11257]</span><span class="sxs-lookup"><span data-stu-id="af695-1182">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="af695-1183">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="af695-1183">Az.DataFactory</span></span>
* <span data-ttu-id="af695-1184">ADF .NET SDK’sı 4.8.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-1184">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="af695-1185">Yeniden çalıştırmayı desteklemek için ‘Invoke-AzDataFactoryV2Pipeline’ komutuna isteğe bağlı parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1185">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="af695-1186">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="af695-1186">Az.DataLakeStore</span></span>
* <span data-ttu-id="af695-1187">‘Export-AzDataLakeStoreItem’ ve ‘Import-AzDataLakeStoreItem’ için hataya neden olan değişiklik açıklaması eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1187">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="af695-1188">‘New-AzDataLakeStoreItem’, ‘Add-AzDAtaLakeStoreItemContent’ ve ‘Get-AzDAtaLakeStoreItemContent’ için Bayt kodlaması seçeneği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1188">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="af695-1189">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="af695-1189">Az.HDInsight</span></span>
* <span data-ttu-id="af695-1190">Küme oluştururken TLS sürümünün desteklenen en düşük sürümünün belirtilmesine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1190">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="af695-1191">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="af695-1191">Az.IotHub</span></span>
* <span data-ttu-id="af695-1192">Cihaz başına dağıtılmış ayarları yönetmeye yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-1192">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="af695-1193">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="af695-1193">New Cmdlets are:</span></span>
    - <span data-ttu-id="af695-1194">‘Get-AzIotHubDistributedTracing’</span><span class="sxs-lookup"><span data-stu-id="af695-1194">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="af695-1195">‘Set-AzIotHubDistributedTracing’</span><span class="sxs-lookup"><span data-stu-id="af695-1195">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="af695-1196">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="af695-1196">Az.KeyVault</span></span>
* <span data-ttu-id="af695-1197">‘New-AzKeyVault’ cmdlet’ine hataya neden olan değişiklik öznitelikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1197">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="af695-1198">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="af695-1198">Az.Monitor</span></span>
* <span data-ttu-id="af695-1199">‘New-AzScheduledQueryRuleLogMetricTrigger’ cmdlet’ine yönelik belgeler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-1199">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="af695-1200">Az.Network</span><span class="sxs-lookup"><span data-stu-id="af695-1200">Az.Network</span></span>
* <span data-ttu-id="af695-1201">Kiracılar arası VirtualHubVnetConnections kurulmasına olanak tanımak için cmdlet’ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-1201">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="af695-1202">‘New-AzVirtualHubVnetConnection’</span><span class="sxs-lookup"><span data-stu-id="af695-1202">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="af695-1203">‘Update-AzVirtualHubVnetConnection’</span><span class="sxs-lookup"><span data-stu-id="af695-1203">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="af695-1204">‘New-AzVirtualHub’</span><span class="sxs-lookup"><span data-stu-id="af695-1204">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="af695-1205">‘Update-AzVirtualHub’</span><span class="sxs-lookup"><span data-stu-id="af695-1205">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="af695-1206">SQL Yönetim SDK’sı bağımlılığı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="af695-1206">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="af695-1207">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="af695-1207">Az.PolicyInsights</span></span>
* <span data-ttu-id="af695-1208">Hata iletileri iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-1208">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="af695-1209">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="af695-1209">Az.RecoveryServices</span></span>
* <span data-ttu-id="af695-1210">Azure Site Recovery’de, Azure disk tarafından şifrelenmiş Sanal Makinelere yönelik VM özellikleri güncelleştirildi ve yeniden koruma gerçekleştirmeye yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-1210">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="af695-1211">Azure Site Recovery VmwareToAzure DR izleme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1211">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="af695-1212">Başarısız öğeler için ilke güncelleştirmesini yeniden deneme özelliğine yönelik destek Azure Backup’a eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-1212">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="af695-1213">Yedekleme ve geri yükleme işlemleri sırasında disk dışlaması ayarını kullanmaya yönelik destek Azure Backup’a eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-1213">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="af695-1214">AzureFileShare’den birden fazla dosyayı/klasörü geri yüklemeye yönelik destek Azure Backup’a eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1214">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="af695-1215">IaasVM İlkesini güncelleştirilirken kullanıcı tarafından belirtilen Resourcegroup desteğine yönelik destek Azure Backup’a eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1215">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="af695-1216">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="af695-1216">Az.Resources</span></span>
* <span data-ttu-id="af695-1217">‘Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType’ komutlarındaki bir hata düzeltildi ve bunların varsayılan apiVersion yerine kaynakların asıl apiVersion’unu kullanması sağlandı [#11267]</span><span class="sxs-lookup"><span data-stu-id="af695-1217">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="af695-1218">Hata senaryoları için correlationId’yi günlüğe kaydetme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1218">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="af695-1219">‘Get-AzResourceLock’ cmdlet’inde küçük bir belge değişikliği yapıldı.</span><span class="sxs-lookup"><span data-stu-id="af695-1219">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="af695-1220">Örnek eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-1220">Added example.</span></span>
* <span data-ttu-id="af695-1221">‘Get-AzADUser’ cmdlet’inin parametre değerinde tek tırnak işaretinin atlanması [#11317]</span><span class="sxs-lookup"><span data-stu-id="af695-1221">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="af695-1222">Dağıtım Betikleri için yeni cmdlet’ler eklendi (‘Get-AzDeploymentScript’, ‘Get-AzDeploymentScriptLog’, ‘Save-AzDeploymentScriptLog’ ve ‘Remove-AzDeploymentScript’)</span><span class="sxs-lookup"><span data-stu-id="af695-1222">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="af695-1223">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="af695-1223">Az.Sql</span></span>
* <span data-ttu-id="af695-1224">‘Invoke-AzSqlDatabaseFailover’ cmdlet’ine okunabilir ikincil parametre eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1224">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="af695-1225">‘Disable-AzSqlServerActiveDirectoryOnlyAuthentication’ cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1225">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="af695-1226">Veritabanındaki sütunlar sınıflandırılırken duyarlılık derecesi kaydedildi.</span><span class="sxs-lookup"><span data-stu-id="af695-1226">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="af695-1227">Az.Support</span><span class="sxs-lookup"><span data-stu-id="af695-1227">Az.Support</span></span>
* <span data-ttu-id="af695-1228">‘Az.Support’ modülü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="af695-1228">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="af695-1229">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="af695-1229">Az.Websites</span></span>
* <span data-ttu-id="af695-1230">Aşağıdaki yeni cmdlet’leri kullanarak Trafik Yönlendirme Kurallarıyla çalışmaya yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-1230">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="af695-1231">‘Get-AzWebAppTrafficRouting’</span><span class="sxs-lookup"><span data-stu-id="af695-1231">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="af695-1232">‘Update-AzWebAppTrafficRouting’</span><span class="sxs-lookup"><span data-stu-id="af695-1232">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="af695-1233">‘Add-AzWebAppTrafficRouting’</span><span class="sxs-lookup"><span data-stu-id="af695-1233">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="af695-1234">‘Remove-AzWebAppTrafficRouting’</span><span class="sxs-lookup"><span data-stu-id="af695-1234">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="af695-1235">3.6.1 - Mart 2020</span><span class="sxs-lookup"><span data-stu-id="af695-1235">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="af695-1236">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="af695-1236">Az.Accounts</span></span>
* <span data-ttu-id="af695-1237">'Send-Feedback' içinde Azure PowerShell anket sayfasını açma [#11020]</span><span class="sxs-lookup"><span data-stu-id="af695-1237">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="af695-1238">'Resolve-Error' içinde Azure PowerShell anket URL’sini görüntüleme [#11021]</span><span class="sxs-lookup"><span data-stu-id="af695-1238">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="af695-1239">UserAgent’ta Az sürümü eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1239">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="af695-1240">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="af695-1240">Az.ApiManagement</span></span>
* <span data-ttu-id="af695-1241">DeveloperPortal Uç Noktasında Özel Etki Alanını alma ve yapılandırma desteği eklendi [#11007]</span><span class="sxs-lookup"><span data-stu-id="af695-1241">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="af695-1242">'Export-AzApiManagementApi' içinde Api Tanımını Json biçiminde indirme desteği eklendi [#9987]</span><span class="sxs-lookup"><span data-stu-id="af695-1242">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="af695-1243">'Import-AzApiManagementApi' içinde OpenApi 3.0 tanımını Json belgesinden içeri aktarma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1243">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="af695-1244">'New-AzApiManagementIdentityProvider' ve 'Set-AzApiManagementIdentityProvider' içinde AAD B2C Sağlayıcısı için 'Oturum Açan Kiracı' yapılandırma desteği eklendi [#9784]</span><span class="sxs-lookup"><span data-stu-id="af695-1244">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="af695-1245">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="af695-1245">Az.DataLakeStore</span></span>
* <span data-ttu-id="af695-1246">csproj ve psd1 içinde System.Buffers öğesine açık başvuru eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-1246">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="af695-1247">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="af695-1247">Az.IotHub</span></span>
* <span data-ttu-id="af695-1248">Iot Hub’daki cihazları yönetmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-1248">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="af695-1249">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="af695-1249">New Cmdlets are:</span></span>
    - <span data-ttu-id="af695-1250">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="af695-1250">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="af695-1251">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="af695-1251">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="af695-1252">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="af695-1252">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="af695-1253">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="af695-1253">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="af695-1254">IoT hub’ındaki hedef IoT cihazında modülleri yönetmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-1254">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="af695-1255">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="af695-1255">New Cmdlets are:</span></span>
    - <span data-ttu-id="af695-1256">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="af695-1256">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="af695-1257">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="af695-1257">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="af695-1258">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="af695-1258">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="af695-1259">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="af695-1259">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="af695-1260">Bir IoT hub’ında hedef IoT cihazının bağlantı dizesini almak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-1260">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="af695-1261">Bir IoT hub’ında hedef IoT cihazındaki modülün bağlantı dizesini almak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-1261">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="af695-1262">IoT cihazının üst cihazını almak/ayarlamak için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-1262">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="af695-1263">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="af695-1263">New Cmdlets are:</span></span>
    - <span data-ttu-id="af695-1264">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="af695-1264">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="af695-1265">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="af695-1265">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="af695-1266">Cihaz üst-alt ilişkisinin yönetilmesi için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-1266">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="af695-1267">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="af695-1267">Az.Monitor</span></span>
* <span data-ttu-id="af695-1268">'Get-AzMetricDefinition' için çıkış değeri düzeltildi [#9714]</span><span class="sxs-lookup"><span data-stu-id="af695-1268">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="af695-1269">Az.Network</span><span class="sxs-lookup"><span data-stu-id="af695-1269">Az.Network</span></span>
* <span data-ttu-id="af695-1270">SQL Yönetim SDK’sı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-1270">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="af695-1271">PrivateLinkServiceConnectionState sınıfındaki bir adlandırma farkı sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-1271">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="af695-1272">ActionsRequired alanı ActionRequired alanına eşleniyor.</span><span class="sxs-lookup"><span data-stu-id="af695-1272">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="af695-1273">'New-AzSqlServer' ve 'Set-AzSqlServer' için PublicNetworkAccess eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1273">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="af695-1274">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="af695-1274">Az.Resources</span></span>
* <span data-ttu-id="af695-1275">'Get-AzRoleAssignment' içindeki null başvuru hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-1275">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="af695-1276">'-Force' ve '-PassThru' anahtarı 'Remove-AzADGroup' içinde isteğe bağlı olarak işaretlendi [#10849]</span><span class="sxs-lookup"><span data-stu-id="af695-1276">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="af695-1277">'MailNickname' öğesinin 'Remove-AzADGroup' içinde döndürülmemesi sorunu düzeltildi [#11167]</span><span class="sxs-lookup"><span data-stu-id="af695-1277">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="af695-1278">'Remove-AzADGroup' kanal oluşturma işleminin çalışmaması sorunu düzeltildi [#11171]</span><span class="sxs-lookup"><span data-stu-id="af695-1278">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="af695-1279">GetAzureRoleAssignmentCommand içinde null başvuru hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-1279">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="af695-1280">İlke cmdlet’lerinde yaklaşan değişiklikler için hataya neden olan değişiklik öznitelikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1280">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="af695-1281">'Get-AzResourceGroup' sunucu tarafında kaynak grubu etiket filtreleme gerçekleştirmek için güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-1281">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="af695-1282">Tag cmdlet’leri -ResourceId öğesini kabul edecek şekilde genişletildi</span><span class="sxs-lookup"><span data-stu-id="af695-1282">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="af695-1283">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="af695-1283">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="af695-1284">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="af695-1284">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="af695-1285">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="af695-1285">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="af695-1286">Yeni Tag cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1286">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="af695-1287">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="af695-1287">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="af695-1288">SDK 3.3.0 sürümünden ScopedDeployment getirildi</span><span class="sxs-lookup"><span data-stu-id="af695-1288">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="af695-1289">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="af695-1289">Az.Sql</span></span>
* <span data-ttu-id="af695-1290">'New-AzSqlServer' ve 'Set-AzSqlServer' için PublicNetworkAccess eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1290">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="af695-1291">Yönetilen Veritabanları için Uzun Süreli Saklamalı yedekleme yapılandırması desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1291">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="af695-1292">Yönetilen bir veritabanında LTR ilkesini alma/ayarlama</span><span class="sxs-lookup"><span data-stu-id="af695-1292">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="af695-1293">Yönetilen veritabanı, yönetilen örnek veya konuma göre LTR yedeklemelerini alma</span><span class="sxs-lookup"><span data-stu-id="af695-1293">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="af695-1294">Bir LTR yedeklemesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="af695-1294">Remove an LTR backup</span></span>
    - <span data-ttu-id="af695-1295">Yeni yönetilen veritabanı oluşturmak için LTR yedeklemesini geri yükleme</span><span class="sxs-lookup"><span data-stu-id="af695-1295">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="af695-1296">New-AzSqlServer ve Set-AzSqlServer için MinimalTlsVersion eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1296">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="af695-1297">New-AzSqlInstance ve Set-AzSqlInstance için MinimalTlsVersion eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1297">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="af695-1298">Az.Network için SQL SDK sürümü artırıldı</span><span class="sxs-lookup"><span data-stu-id="af695-1298">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="af695-1299">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="af695-1299">Az.Storage</span></span>
* <span data-ttu-id="af695-1300">ImmutabilityPolicy içinde AllowProtectedAppendWrite desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1300">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="af695-1301">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="af695-1301">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="af695-1302">Gelecekteki bir yayın için AzureStorageTable tür değişikliğine yönelik hataya neden olan değişiklik uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1302">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="af695-1303">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="af695-1303">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="af695-1304">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="af695-1304">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="af695-1305">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="af695-1305">Az.Websites</span></span>
* <span data-ttu-id="af695-1306">'New-AzAppServicePlan' ve 'Set-AzAppServicePlan' için Etiket parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1306">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="af695-1307">Özel etki alanı bir web sitesine eklenirken özel durum oluşturulursa cmdlet’i yürütmeyi durdur</span><span class="sxs-lookup"><span data-stu-id="af695-1307">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="af695-1308">App Service Planıyla aynı kaynak grubunda bulunmayan Uygulama Hizmetleri için işlem gerçekleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1308">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="af695-1309">Farklı kaynak gruplarındaki WebApp/İşlev öğesine erişim kısıtlaması uygulandı</span><span class="sxs-lookup"><span data-stu-id="af695-1309">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="af695-1310">WebAppSlots için özel ana bilgisayar adları ayarlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-1310">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="af695-1311">3.5.0 - Şubat 2020</span><span class="sxs-lookup"><span data-stu-id="af695-1311">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="af695-1312">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="af695-1312">Highlights since the last major release</span></span>
* <span data-ttu-id="af695-1313">İstemci tarafı telemetri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-1313">Updated client side telemetry.</span></span>
* <span data-ttu-id="af695-1314">Cihaz yönetimini desteklemek için Az.IotHub cmdlet’leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-1314">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="af695-1315">Kullanılabilirlik Grubu Dinleyicisi için Az.SqlVirtualMachine cmdlet’leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-1315">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="af695-1316">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="af695-1316">Az.Accounts</span></span>
* <span data-ttu-id="af695-1317">İstemci tarafı telemetri verilerine SubscriptionId, TenantId ve yürütme zamanı eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1317">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="af695-1318">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="af695-1318">Az.Automation</span></span>
* <span data-ttu-id="af695-1319">'New-AzAutomationSoftwareUpdateConfiguration' için başvuru belgelerinde Örnek 1’deki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-1319">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="af695-1320">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="af695-1320">Az.CognitiveServices</span></span>
* <span data-ttu-id="af695-1321">SDK 7.0 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-1321">Updated SDK to 7.0</span></span>
* <span data-ttu-id="af695-1322">Sunucu yanıtları boş gövde olduğunda alınan hata iletisi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-1322">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="af695-1323">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="af695-1323">Az.Compute</span></span>
* <span data-ttu-id="af695-1324">Güncelleştirme sırasında ProximityPlacementGroupId için boş değere izin verildi</span><span class="sxs-lookup"><span data-stu-id="af695-1324">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="af695-1325">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="af695-1325">Az.FrontDoor</span></span>
* <span data-ttu-id="af695-1326">WAF’de kullanılabilen yönetilen kural tanımlarını almak için cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1326">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="af695-1327">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="af695-1327">Az.IotHub</span></span>
* <span data-ttu-id="af695-1328">Iot Hub’daki cihazları yönetmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-1328">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="af695-1329">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="af695-1329">New Cmdlets are:</span></span>
    - <span data-ttu-id="af695-1330">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="af695-1330">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="af695-1331">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="af695-1331">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="af695-1332">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="af695-1332">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="af695-1333">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="af695-1333">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="af695-1334">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="af695-1334">Az.KeyVault</span></span>
* <span data-ttu-id="af695-1335">Add-AzKeyVaultKey.md için yinelenen metin düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-1335">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="af695-1336">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="af695-1336">Az.Monitor</span></span>
* <span data-ttu-id="af695-1337">Get-AzLog cmdlet’inin açıklaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-1337">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="af695-1338">'New-AzMetricAlertRuleV2' komutuna ActionGroupId adlı yeni bir parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-1338">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="af695-1339">Kullanıcı ActionGroupId(string) veya ActionGroup(ActivityLogAlertActionGroup) sağlayabilir.</span><span class="sxs-lookup"><span data-stu-id="af695-1339">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="af695-1340">Az.Network</span><span class="sxs-lookup"><span data-stu-id="af695-1340">Az.Network</span></span>
* <span data-ttu-id="af695-1341">'New-AzPrivateLinkService' cmdlet’inin '-EnableProxyProtocol' parametresi için ek bir parametre notu eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-1341">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="af695-1342">Start-AzVirtualNetworkGatewayConnectionPacketCapture.md ve Start-AzVirtualnetworkGatewayPacketCapture.md içindeki FilterData örneği düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-1342">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="af695-1343">Start-AzVirtualNetworkGatewayConnectionPacketCapture.md ve Start-AzVirtualnetworkGatewayPacketCapture.md içinde tüm iç ve dış paketleri yakalamak için Paket Yakalama örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-1343">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="af695-1344">Sanal Ağ Güvenlik Duvarları üzerinde Azure Güvenlik Duvarı desteği sağlandı</span><span class="sxs-lookup"><span data-stu-id="af695-1344">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="af695-1345">Yeni cmdlet eklenmedi.</span><span class="sxs-lookup"><span data-stu-id="af695-1345">No new cmdlets are added.</span></span> <span data-ttu-id="af695-1346">Sanal ağ güvenlik duvarları üzerinde güvenlik duvarı ilkesi için kısıtlama gevşetiliyor</span><span class="sxs-lookup"><span data-stu-id="af695-1346">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="af695-1347">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="af695-1347">Az.RecoveryServices</span></span>
* <span data-ttu-id="af695-1348">SQL Veritabanları için Dosya olarak geri yükleme desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-1348">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="af695-1349">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="af695-1349">Az.Resources</span></span>
* <span data-ttu-id="af695-1350">Şablon dağıtım cmdlet’leri yeniden düzenlendi</span><span class="sxs-lookup"><span data-stu-id="af695-1350">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="af695-1351">Yönetim grubunda dağıtımları yönetmek için yeni cmdlet’ler eklendi: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="af695-1351">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="af695-1352">Kiracı kapsamında dağıtımları yönetmek için yeni cmdlet’ler eklendi: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="af695-1352">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="af695-1353">\*-AzDeployment cmdlet’leri özel olarak abonelik kapsamında çalışmak için yeniden düzenlendi</span><span class="sxs-lookup"><span data-stu-id="af695-1353">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="af695-1354">\*-AzDeployment cmdlet’leri için \*-AzSubscriptionDeployment diğer adları oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="af695-1354">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="af695-1355">'AvailableToOtherTenants' parametresi ayarlanmadığında 'Update-AzADApplication' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-1355">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="af695-1356">AmbiguousParameterSetException özel durumundan kaçınmak için ApplicationObjectWithoutCredentialParameterSet kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="af695-1356">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="af695-1357">Yardım dosyaları yeniden oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="af695-1357">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="af695-1358">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="af695-1358">Az.Sql</span></span>
* <span data-ttu-id="af695-1359">Yönetilen Örneklerde abonelikler arasında zaman noktası geri yüklemesi için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-1359">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="af695-1360">Mevcut SQL Yönetilen Örnek donanım neslini değiştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1360">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="af695-1361">'Update-AzSqlServerVulnerabilityAssessmentSetting' yardım örnekleri düzeltildi: parameter/property output - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="af695-1361">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="af695-1362">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="af695-1362">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="af695-1363">Kullanılabilirlik Grubu Dinleyicisi için cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1363">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="af695-1364">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="af695-1364">Az.StorageSync</span></span>
* <span data-ttu-id="af695-1365">'Invoke-AzStorageSyncCompatibilityCheck' içinde desteklenen karakter kümeleri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-1365">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="af695-1366">3.4.0 - Şubat 2020</span><span class="sxs-lookup"><span data-stu-id="af695-1366">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="af695-1367">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="af695-1367">Highlights since the last major release</span></span>
* <span data-ttu-id="af695-1368">Az.CosmosDB ilk sürüm 0.1.0 yayınlandı</span><span class="sxs-lookup"><span data-stu-id="af695-1368">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="af695-1369">Az.Network ConnectionMonitor V2 desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1369">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="af695-1370">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="af695-1370">Az.Accounts</span></span>
* <span data-ttu-id="af695-1371">AzureRmContext.json kullanılamadığında bağlamı otomatik olarak kaydetmeyi devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="af695-1371">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="af695-1372">Azure PowerShell Common’ın başvurusu 1.3.5-önizleme olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-1372">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="af695-1373">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="af695-1373">Az.ApiManagement</span></span>
* <span data-ttu-id="af695-1374">**Get-AzApiManagementApiSchema** Bir API ile ilişkili Open-Api Şemasını alma düzeltildi https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="af695-1374">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="af695-1375">**New-AzApiManagementProduct** _ ve _ *Set-AzApiManagementProduct*\*</span><span class="sxs-lookup"><span data-stu-id="af695-1375">**New-AzApiManagementProduct** _ and _ *Set-AzApiManagementProduct*\*</span></span>
  - <span data-ttu-id="af695-1376"> https://github.com/Azure/azure-powershell/issues/10472 öğesine ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-1376">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="af695-1377">**Set-AzApiManagementApi** ServiceUrl’nin cmdlet kullanılarak nasıl güncelleştirildiğini göstermek için örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1377">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="af695-1378">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="af695-1378">Az.Compute</span></span>
* <span data-ttu-id="af695-1379">Get-AzVM -Status VM adı olmadan gerçekleştirildiğinde ağ kapasitesinin azaltılmasını engellemek için VM durumu sayısını 100 ile sınırlandırın.</span><span class="sxs-lookup"><span data-stu-id="af695-1379">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="af695-1380">Update-AzDiskEncryptionSet cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1380">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="af695-1381">Aşağıdaki cmdlet’lere EncryptionType ve DiskEncryptionSetId parametreleri eklendi:</span><span class="sxs-lookup"><span data-stu-id="af695-1381">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="af695-1382">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="af695-1382">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="af695-1383">Get-AzProximityPlacementGroup cmdlet’ine ColocationStatus parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-1383">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="af695-1384">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="af695-1384">Az.DataFactory</span></span>
* <span data-ttu-id="af695-1385">ADF .Net SDK sürümü 4.7.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-1385">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="af695-1386">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="af695-1386">Az.DeploymentManager</span></span>
* <span data-ttu-id="af695-1387">Kaynaklara yönelik LIST işlemlerini ekler</span><span class="sxs-lookup"><span data-stu-id="af695-1387">Adds LIST operations for resources</span></span>
* <span data-ttu-id="af695-1388">Durum Denetimi adımlarında işlem gerçekleştirmeye yönelik özellik ekler</span><span class="sxs-lookup"><span data-stu-id="af695-1388">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="af695-1389">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="af695-1389">Az.HDInsight</span></span>
* <span data-ttu-id="af695-1390">New-AzHDInsightCluster’ın belge hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-1390">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="af695-1391">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="af695-1391">Az.KeyVault</span></span>
* <span data-ttu-id="af695-1392">Remove-AzureKeyVault’un New-AzureKeyVault ile tutarlı olmasını sağlamak için VaultName özniteliğine Name diğer adı eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-1392">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="af695-1393">Az.Network</span><span class="sxs-lookup"><span data-stu-id="af695-1393">Az.Network</span></span>
* <span data-ttu-id="af695-1394">Trafik Analizi’nin devre dışı bırakıldığı bir senaryoyu göstermek için Set-AzNetworkWatcherConfigFlowLog.md dosyasına yeni örnek eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-1394">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="af695-1395">Azure Güvenlik Duvarı’na yönetim IP yapılandırması atamaya yönelik destek eklendi. Güvenlik duvarı, yönetim trafiği için ayrılmış alt ağı ve Genel IP’yi kullanacak</span><span class="sxs-lookup"><span data-stu-id="af695-1395">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="af695-1396">New-AzFirewall cmdlet'i güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="af695-1396">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="af695-1397">Genel IP Adresi nesnesi kabul eden -ManagementPublicIpAdress (zorunlu değil) parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1397">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="af695-1398">Güvenlik duvarı nesnesine SetManagementIpConfiguration yöntemi eklendi. Giriş olarak bir alt ağ ve Genel IP adresi gerektirir. Alt ağ adının ‘AzureFirewallManagementSubnet’ olması gerekir</span><span class="sxs-lookup"><span data-stu-id="af695-1398">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="af695-1399">Get-AzNetworkSecurityGroup örnekleri, ağ arabirimlerinin yerine NSG’lere yönelik örnekleri gösterecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-1399">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="af695-1400">Kaynak kimliği tamamlayıcısının bir parametreyi tamamlamasını engelleyen New-AzVpnSite komutundaki yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-1400">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="af695-1401">Application Gateway’de Yeniden Yazma Kuralları Eylem Kümesinde Url Yapılandırması için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1401">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="af695-1402">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="af695-1402">New cmdlets added:</span></span>
        - <span data-ttu-id="af695-1403">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="af695-1403">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="af695-1404">Cmdlet’ler isteğe bağlı -UrlConfiguration parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-1404">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="af695-1405">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="af695-1405">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="af695-1406">NetworkWatcher ConnectionMonitor sürüm 2 kaynakları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1406">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="af695-1407">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="af695-1407">Az.PolicyInsights</span></span>
* <span data-ttu-id="af695-1408">Hangi kaynağın düzeltileceği belirlenmeden önce destek değerlendirmesi uyumluluğu</span><span class="sxs-lookup"><span data-stu-id="af695-1408">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="af695-1409">Start-AzPolicyRemediation cmdlet’ine ‘-ResourceDiscoverMode’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1409">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="af695-1410">İlke meta verilerine ilişkin kaynakları almak için Get-AzPolicyMetadata cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1410">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="af695-1411">API sürümü 2019-10-01 için Get-AzPolicyState ve Get-AzPolicyStateSummary güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-1411">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="af695-1412">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="af695-1412">Az.RecoveryServices</span></span>
* <span data-ttu-id="af695-1413">Çoğaltılan bir diski kaldırılmasına yönelik Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="af695-1413">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="af695-1414">Azure Backup, Kurtarma Hizmetleri Kasası oluştururken etiket eklemeye yönelik destek ekledi.</span><span class="sxs-lookup"><span data-stu-id="af695-1414">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="af695-1415">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="af695-1415">Az.Resources</span></span>
* <span data-ttu-id="af695-1416">Varsayılanı bağlam aboneliği olan \*-AzPolicyAssignment cmdlet’lerinde -Scope isteğe bağlı yapıldı</span><span class="sxs-lookup"><span data-stu-id="af695-1416">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="af695-1417">Parola ve anahtar kimlik bilgileriyle ADServicePrincipal oluşturma örnekleri eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1417">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="af695-1418">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="af695-1418">Az.Sql</span></span>
<span data-ttu-id="af695-1419">DatabaseName’in yerine PartnerDatabaseName’in olup olmadığını denetlemeye yarayan New-AzSqlDatabaseSecondary cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-1419">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="af695-1420">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="af695-1420">Az.Storage</span></span>
* <span data-ttu-id="af695-1421">Depolama Hesabı Oluştur’da Tablo/Sıra Şifreleme Anahtarı’nın ayarlanmasına yönelik destek</span><span class="sxs-lookup"><span data-stu-id="af695-1421">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="af695-1422">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="af695-1422">New-AzStorageAccount</span></span>
* <span data-ttu-id="af695-1423">StorageException’da ExtendedErrorInformation olmadığında RequestId’nin gösterilmesi</span><span class="sxs-lookup"><span data-stu-id="af695-1423">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="af695-1424">Start-AzStorageBlobCopy cmdlet’ine ait olan Örnek 6 düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-1424">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="af695-1425">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="af695-1425">Az.Websites</span></span>
* <span data-ttu-id="af695-1426">Set-AzWebapp ve Set-AzWebappSlot, şu özellikleri destekler: AlwaysOn, MinTls ve FtpsState</span><span class="sxs-lookup"><span data-stu-id="af695-1426">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="af695-1427">Tek Set-AzWebApp Komutunu kullanarak HttpsOnly ayarlanırken aynı anda AppservicePlan değiştirildiğinde HttpsOnly’nin varsayılan değere sıfırlanması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-1427">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="af695-1428">3.3.0 - Ocak 2020</span><span class="sxs-lookup"><span data-stu-id="af695-1428">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="af695-1429">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="af695-1429">Az.Accounts</span></span>
* <span data-ttu-id="af695-1430">Add-AzEnvironment ve Set-AzEnvironment, AzureAttestationServiceEndpointResourceId ve AzureAttestationServiceEndpointSuffix parametrelerini kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-1430">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="af695-1431">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="af695-1431">Az.Cdn</span></span>
* <span data-ttu-id="af695-1432">New-AzCdnEndpoint cmdlet’inde hata yanıtı ayrıntılarını görüntüleme</span><span class="sxs-lookup"><span data-stu-id="af695-1432">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="af695-1433">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="af695-1433">Az.Compute</span></span>
* <span data-ttu-id="af695-1434">İşletim sistemi profili bulunmayan, yönetilen OD diskine sahip bir VM için Set-AzVMCustomScriptExtension cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-1434">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="af695-1435">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="af695-1435">Az.ContainerInstance</span></span>
* <span data-ttu-id="af695-1436">New-AzContainerGroup örneği tarafından kullanılan parametre adları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-1436">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="af695-1437">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="af695-1437">Az.DataBoxEdge</span></span>
* <span data-ttu-id="af695-1438">'Get-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1438">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="af695-1439">Edge Depolama Kapsayıcısını edinme</span><span class="sxs-lookup"><span data-stu-id="af695-1439">Get the Edge Storage Container</span></span>
* <span data-ttu-id="af695-1440">'New-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1440">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="af695-1441">Yeni Edge Depolama Kapsayıcısı oluşturma</span><span class="sxs-lookup"><span data-stu-id="af695-1441">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="af695-1442">'Remove-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1442">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="af695-1443">Edge Depolama Kapsayıcısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="af695-1443">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="af695-1444">'Invoke-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1444">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="af695-1445">Edge Depolama Kapsayıcısındaki verileri yenilemek için eylem çağırma</span><span class="sxs-lookup"><span data-stu-id="af695-1445">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="af695-1446">'Get-AzDataBoxEdgeStorageAccount' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1446">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="af695-1447">Edge Depolama Hesabını edinme</span><span class="sxs-lookup"><span data-stu-id="af695-1447">Get the Edge Storage Account</span></span>
* <span data-ttu-id="af695-1448">'New-AzDataBoxEdgeStorageAccount' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1448">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="af695-1449">Yeni Edge Depolama Hesabını oluşturma</span><span class="sxs-lookup"><span data-stu-id="af695-1449">Create new Edge Storage Account</span></span>
* <span data-ttu-id="af695-1450">'Remove-AzDataBoxEdgeStorageAccount' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1450">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="af695-1451">Edge Depolama Hesabını kaldırma</span><span class="sxs-lookup"><span data-stu-id="af695-1451">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="af695-1452">'Invoke-AzDataBoxEdgeShare' cmdlet’ini çağırma</span><span class="sxs-lookup"><span data-stu-id="af695-1452">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="af695-1453">Paylaşımdaki verileri yenilemek için eylem çağırma</span><span class="sxs-lookup"><span data-stu-id="af695-1453">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="af695-1454">'Set-AzDataBoxEdgeStorageAccountCredential' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1454">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="af695-1455">Az databoxedge depolama hesabı kimlik bilgilerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="af695-1455">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="af695-1456">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="af695-1456">Az.DataFactory</span></span>
* <span data-ttu-id="af695-1457">Get-AzDataFactoryV2IntegrationRuntime cmdlet’i için AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId ve VersionStatus özellikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1457">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="af695-1458">ADF .Net SDK sürümü 4.6.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-1458">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="af695-1459">Statik genel IP adreslerine sahip Azure-SSIS IR’nin oluşturulmasına olanak tanımak için ‘Set-AzureRmDataFactoryV2IntegrationRuntime’ cmdlet’ine yönelik ‘PublicIPs’ parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-1459">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="af695-1460">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="af695-1460">Az.DevTestLabs</span></span>
* <span data-ttu-id="af695-1461">Get-AzDtlAllowedVMSizesPolicy.md’deki bozuk bağlantı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="af695-1461">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="af695-1462">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="af695-1462">Az.EventHub</span></span>
* <span data-ttu-id="af695-1463">Sorun 10634’e yönelik düzeltme: Eventhubnamespace’i kaldırmaya yönelik null Nesne başvurusu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-1463">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="af695-1464">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="af695-1464">Az.HDInsight</span></span>
* <span data-ttu-id="af695-1465">Invoke-AzHDInsightHiveJob.md hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-1465">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="af695-1466">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="af695-1466">Az.MachineLearning</span></span>
* <span data-ttu-id="af695-1467">MachineLearningCompute artık kullanılamadığından, aşağıdaki cmdlet’ler kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="af695-1467">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="af695-1468">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="af695-1468">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="af695-1469">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="af695-1469">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="af695-1470">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="af695-1470">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="af695-1471">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="af695-1471">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="af695-1472">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="af695-1472">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="af695-1473">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="af695-1473">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="af695-1474">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="af695-1474">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="af695-1475">Az.Network</span><span class="sxs-lookup"><span data-stu-id="af695-1475">Az.Network</span></span>
* <span data-ttu-id="af695-1476">1\.36-preview olan Microsoft.Azure.Management.Sql bağımlılığı 1.37-preview’a yükseltildi</span><span class="sxs-lookup"><span data-stu-id="af695-1476">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="af695-1477">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="af695-1477">Az.RecoveryServices</span></span>
* <span data-ttu-id="af695-1478">Azure’dan Azure’a sağlayıcı için müşteri tarafından yönetilen anahtarlar ile bekleyen durumda şifrelenen yönetilen disk VM’lerine yönelik Azure Site Recovery değişim desteği.</span><span class="sxs-lookup"><span data-stu-id="af695-1478">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="af695-1479">Disk şifreleme Kümesi Kimliklerini VMware’den Azure’a aktarımlara yönelik koruma sağlayan isteğe bağlı giriş olarak girmek için Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="af695-1479">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="af695-1480">Disk şifreleme Kümesi Kimliklerini VMware’den Azure’a aktarımlara yönelik koruma sağlayan disk düzeyinde isteğe bağlı giriş olarak girmek için Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="af695-1480">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="af695-1481">HyperV’den Azure’a disk şifrelemesi ayarlama eşlemesi ile çoğaltma korumalı öğeyi güncelleştirmeye yönelik Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="af695-1481">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="af695-1482">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="af695-1482">Az.Resources</span></span>
* <span data-ttu-id="af695-1483">'Remove-AzTag' yardım belgesindeki bir hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-1483">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="af695-1484">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="af695-1484">Az.Sql</span></span>
* <span data-ttu-id="af695-1485">Güvenlik açığı değerlendirmesi tarafından ayarlanan temel cmdlet işlevi, Azure veritabanına yönelik ana veritabanında çalışacak ve yönetilen örnek sistem veritabanlarında sınırlandırılacak şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-1485">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="af695-1486">SQL örneği yük devretme grubu oluşturulurken karşılaşılan bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-1486">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="af695-1487">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="af695-1487">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="af695-1488">Yeni geçerli Lisans türü olarak DR eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1488">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="af695-1489">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="af695-1489">Az.Storage</span></span>
* <span data-ttu-id="af695-1490">Sonraki bir sürümde gerçekleşecek DefaultAction değerinin değişikliğine yönelik hataya neden olan değişiklik uyarısı eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1490">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="af695-1491">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="af695-1491">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="af695-1492">Get-AzureRMStorageAccount cmdlet’i -IncludeGeoReplicationStats parametresiyle çalıştırarak Depolama hesabının en son eşitleme zamanını almaya yönelik destek</span><span class="sxs-lookup"><span data-stu-id="af695-1492">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="af695-1493">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="af695-1493">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="af695-1494">3.2.0 - Aralık 2019</span><span class="sxs-lookup"><span data-stu-id="af695-1494">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="af695-1495">Genel</span><span class="sxs-lookup"><span data-stu-id="af695-1495">General</span></span>
* <span data-ttu-id="af695-1496">.psd1 içindeki başvurular, tüm modüller için göreli yol kullanılacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-1496">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="af695-1497">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="af695-1497">Az.Accounts</span></span>
* <span data-ttu-id="af695-1498">Az 4.0 önizlemesine yönelik istemci tarafı telemetri için doğru UserAgent ayarlandı</span><span class="sxs-lookup"><span data-stu-id="af695-1498">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="af695-1499">Az 4.0 önizlemesinde bağlam null olduğunda kolay hata iletisi görüntüleniyor</span><span class="sxs-lookup"><span data-stu-id="af695-1499">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="af695-1500">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="af695-1500">Az.Batch</span></span>
* <span data-ttu-id="af695-1501">**New-AzBatchPool** cmdlet’inin 'VirtualMachineConfiguration. ContainerConfiguration' veya 'VirtualMachineConfiguration.DataDisks' öğelerini sunucuya doğru bir şekilde göndermediği [10602](https://github.com/Azure/azure-powershell/issues/10602) numaralı sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-1501">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="af695-1502">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="af695-1502">Az.DataFactory</span></span>
* <span data-ttu-id="af695-1503">ADF .Net SDK sürümü 4.5.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-1503">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="af695-1504">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="af695-1504">Az.FrontDoor</span></span>
* <span data-ttu-id="af695-1505">WAF tarafından yönetilen kuralları dışlama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1505">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="af695-1506">Otomatik tamamlamaya SocketAddr eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1506">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="af695-1507">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="af695-1507">Az.HealthcareApis</span></span>
* <span data-ttu-id="af695-1508">Özel Durum İşleme</span><span class="sxs-lookup"><span data-stu-id="af695-1508">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="af695-1509">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="af695-1509">Az.KeyVault</span></span>
* <span data-ttu-id="af695-1510">Ayarlanmamış olabilecek değere erişirken gerçekleşen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-1510">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="af695-1511">Eliptik Eğri Şifrelemesi Sertifika Yönetimi</span><span class="sxs-lookup"><span data-stu-id="af695-1511">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="af695-1512">Sertifika İlkeleri için Eğri belirtme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1512">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="af695-1513">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="af695-1513">Az.Monitor</span></span>
* <span data-ttu-id="af695-1514">Tanılama Ayarları Ekle komutuna isteğe bağlı bağımsız değişken eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-1514">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="af695-1515">Mevcut olduğunda, Log Analytics’e aktarmanın sabit bir şemaya (ayrılmış</span><span class="sxs-lookup"><span data-stu-id="af695-1515">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="af695-1516">veri türü olarak da bilinir) yönelik olması gerektiğini belirten bir anahtar bağımsız değişkeni</span><span class="sxs-lookup"><span data-stu-id="af695-1516">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="af695-1517">Az.Network</span><span class="sxs-lookup"><span data-stu-id="af695-1517">Az.Network</span></span>
* <span data-ttu-id="af695-1518">AzureFirewall Uygulama, NAT ve Ağ Kuralları içinde IpGroups desteği.</span><span class="sxs-lookup"><span data-stu-id="af695-1518">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="af695-1519">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="af695-1519">Az.Resources</span></span>
* <span data-ttu-id="af695-1520">Şablon parametresi adının yerleşik bir parametre adıyla çakışması durumunda şablon dağıtımının, şablon parametresini okuyamamasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-1520">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="af695-1521">İlke cmdlet’leri, ilke kümesi tanımları içinde gruplandırma desteği sunan yeni API sürümü 2019-09-01’i kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-1521">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="af695-1522">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="af695-1522">Az.Sql</span></span>
* <span data-ttu-id="af695-1523">Güvenlik Açığı Değerlendirmesi otomatik etkinleştirmesi, depolamayı StorageV2'de oluşturacak şekilde yükseltildi</span><span class="sxs-lookup"><span data-stu-id="af695-1523">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="af695-1524">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="af695-1524">Az.Storage</span></span>
* <span data-ttu-id="af695-1525">OAuth kimlik doğrulaması tabanlı Depolama Bağlamı ile Blob/Kapsayıcı Kimliği tabanlı SAS belirteci oluşturma desteği</span><span class="sxs-lookup"><span data-stu-id="af695-1525">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="af695-1526">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="af695-1526">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="af695-1527">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="af695-1527">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="af695-1528">Tüm Kimlik SAS belirteçleri iptal edilecek şekilde Depolama Hesabı Kullanıcı Temsilcisi Anahtarlarını iptal etme desteği</span><span class="sxs-lookup"><span data-stu-id="af695-1528">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="af695-1529">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="af695-1529">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="af695-1530">Microsoft.Azure.Management.Storage, yeni API sürümü 2019-06-01 desteklenecek şekilde 14.2.0 sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-1530">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="af695-1531">Dosya Paylaşımı cmdlet’lerinin Yönetim düzlemindeki 5120’den daha büyük değerler için QuotaGiB (Gibibayt temelinde Paylaşım Kotası) desteği sunuldu ve 'QuotaGiB' parametresine yönelik diğer ad olarak 'Quota' parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-1531">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="af695-1532">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="af695-1532">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="af695-1533">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="af695-1533">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="af695-1534">'Quota' parametresine 'QuotaGiB' parametre diğer adı eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1534">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="af695-1535">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="af695-1535">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="af695-1536">Set-AzStorageContainerAcl’nin depolanan Erişim İlkesini temizlemesine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-1536">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="af695-1537">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="af695-1537">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="af695-1538">3.1.0 - Kasım 2019</span><span class="sxs-lookup"><span data-stu-id="af695-1538">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="af695-1539">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="af695-1539">Highlights since the last major release</span></span>
* <span data-ttu-id="af695-1540">Az.DataBoxEdge 1.0.0 yayımlandı</span><span class="sxs-lookup"><span data-stu-id="af695-1540">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="af695-1541">Az.SqlVirtualMachine 1.0.0 yayımlandı</span><span class="sxs-lookup"><span data-stu-id="af695-1541">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="af695-1542">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="af695-1542">Az.Compute</span></span>
* <span data-ttu-id="af695-1543">VM Reapply özelliği</span><span class="sxs-lookup"><span data-stu-id="af695-1543">VM Reapply feature</span></span>
    - <span data-ttu-id="af695-1544">Set-AzVM cmdlet’ine Reapply parametresi ekleme</span><span class="sxs-lookup"><span data-stu-id="af695-1544">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="af695-1545">VM Ölçek Kümesi AutomaticRepairs özelliği:</span><span class="sxs-lookup"><span data-stu-id="af695-1545">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="af695-1546">EnableAutomaticRepair, AutomaticRepairGracePeriod ve AutomaticRepairMaxInstanceRepairsPercent parametreleri şu cmdlet’lere eklendi:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="af695-1546">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="af695-1547">New-AzVM için kiracılar arası galeri görüntüsü desteği</span><span class="sxs-lookup"><span data-stu-id="af695-1547">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="af695-1548">New-AzVM, New-AzVMConfig ve New-AzVmss cmdlet’lerindeki Priority parametresinin bağımsız değişken tamamlayıcısına ‘Spot’ eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-1548">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="af695-1549">Add-AzVmssDataDisk cmdlet’ine DiskIOPSReadWrite ve DiskMBpsReadWrite parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1549">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="af695-1550">New-AzGalleryImageVersion cmdlet’inin SourceImageId parametresi isteğe bağlı olacak şekilde değiştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-1550">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="af695-1551">New-AzGalleryImageVersion cmdlet’ine OSDiskImage ve DataDiskImage parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1551">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="af695-1552">New-AzGalleryImageDefinition cmdlet’ine HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1552">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="af695-1553">New-AzVmss, New-AzVmssConfig ve Update-AzVmss cmdlet’lerine SkipExtensionsOnOverprovisionedVMs parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1553">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="af695-1554">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="af695-1554">Az.DataBoxEdge</span></span>
* <span data-ttu-id="af695-1555">`Get-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1555">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="af695-1556">Sırayı Al</span><span class="sxs-lookup"><span data-stu-id="af695-1556">Get the Order</span></span>
* <span data-ttu-id="af695-1557">`New-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1557">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="af695-1558">Yeni Sıra oluştur</span><span class="sxs-lookup"><span data-stu-id="af695-1558">Create new Order</span></span>
* <span data-ttu-id="af695-1559">`Remove-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1559">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="af695-1560">Sırayı kaldır</span><span class="sxs-lookup"><span data-stu-id="af695-1560">Remove the Order</span></span>
* <span data-ttu-id="af695-1561">`New-AzDataBoxEdgeShare` cmdlet’inde değiştir</span><span class="sxs-lookup"><span data-stu-id="af695-1561">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="af695-1562">Yerel Paylaşım’ı oluşturur</span><span class="sxs-lookup"><span data-stu-id="af695-1562">Now creates Local Share</span></span>
* <span data-ttu-id="af695-1563">`Set-AzDataBoxEdgeRole` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1563">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="af695-1564">IotRole artık Paylaş ile eşlenebilir</span><span class="sxs-lookup"><span data-stu-id="af695-1564">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="af695-1565">`Invoke-AzDataBoxEdgeDevice` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1565">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="af695-1566">Tarama güncelleştirmesi çağırın, güncelleştirmeyi indirin ve bunları cihaza yükleyin</span><span class="sxs-lookup"><span data-stu-id="af695-1566">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="af695-1567">`Get-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1567">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="af695-1568">Tetikleyicilere ilişkin bilgileri alır</span><span class="sxs-lookup"><span data-stu-id="af695-1568">Gets the information about Triggers</span></span>
* <span data-ttu-id="af695-1569">`New-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1569">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="af695-1570">Yeni Tetikleyiciler oluştur</span><span class="sxs-lookup"><span data-stu-id="af695-1570">Create new Triggers</span></span>
* <span data-ttu-id="af695-1571">`Remove-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1571">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="af695-1572">Tetikleyicileri kaldır</span><span class="sxs-lookup"><span data-stu-id="af695-1572">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="af695-1573">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="af695-1573">Az.DataFactory</span></span>
* <span data-ttu-id="af695-1574">ADF .Net SDK sürümü 4.4.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-1574">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="af695-1575">Özel kurulum betiği olmadan kurulum yapılandırmalarını ve 3. taraf bileşenleri etkinleştirmek üzere ‘Set-AzureRmDataFactoryV2IntegrationRuntime’ komutu için ‘ExpressCustomSetup’ parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-1575">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="af695-1576">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="af695-1576">Az.DataLakeStore</span></span>
* <span data-ttu-id="af695-1577">Get-AzDataLakeStoreDeletedItem ve Restore-AzDataLakeStoreDeletedItem parametrelerinin belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-1577">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="af695-1578">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="af695-1578">Az.EventHub</span></span>
* <span data-ttu-id="af695-1579">#10301 numaralı şu sorun düzeltildi: SAS Belirtecinin tarih biçimi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-1579">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="af695-1580">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="af695-1580">Az.FrontDoor</span></span>
* <span data-ttu-id="af695-1581">Enable-AzFrontDoorCustomDomainHttps ve New-AzFrontDoorFrontendEndpointObject öğelerine MinimumTlsVersion parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1581">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="af695-1582">New-AzFrontDoorHealthProbeSettingObject öğesine HealthProbeMethod ve EnabledState parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1582">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="af695-1583">BackendPoolsSettings öğesinin Front Door oluşturmasına/güncelleştirmesine geçmesi için BackendPoolsSettings nesnesi oluşturmaya yönelik yeni cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1583">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="af695-1584">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="af695-1584">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="af695-1585">Az.Network</span><span class="sxs-lookup"><span data-stu-id="af695-1585">Az.Network</span></span>
* <span data-ttu-id="af695-1586">‘Start-AzVirtualNetworkGatewayConnectionPacketCapture.md’ ve 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData seçeneği örnekleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-1586">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="af695-1587">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="af695-1587">Az.PrivateDns</span></span>
* <span data-ttu-id="af695-1588">PrivateDns .Net SDK’sı sürüm 1.0.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-1588">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="af695-1589">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="af695-1589">Az.RecoveryServices</span></span>
* <span data-ttu-id="af695-1590">Koruma etkinleştirilirken disk türünü seçmeye yönelik Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="af695-1590">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="af695-1591">Kurtarma planı eylemi düzenlemesine yönelik Azure Site Recovery hata düzeltmesi.</span><span class="sxs-lookup"><span data-stu-id="af695-1591">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="af695-1592">Dosya akışı Veritabanlarını kabul etmek için Azure Backup SQL Geri yükleme desteği.</span><span class="sxs-lookup"><span data-stu-id="af695-1592">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="af695-1593">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="af695-1593">Az.RedisCache</span></span>
* <span data-ttu-id="af695-1594">‘New-AzRedisCache’ ve ‘Set-AzRedisCache’ cmdletlerine ‘MinimumTlsVersion’ parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-1594">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="af695-1595">‘Get-AzRedisCache’ cmdlet’inin çıkışına ‘MinimumTlsVersion’ eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-1595">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="af695-1596">‘Set-AzRedisCache’ ve ‘New-AzRedisCache’ cmdletlerine yönelik ‘-Size’ parametresine doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-1596">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="af695-1597">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="af695-1597">Az.Resources</span></span>
- <span data-ttu-id="af695-1598">İlke cmdletleri, ilke atamasında EnforcementMode özelliğine sahip yeni 2019-06-01 api sürümünü kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-1598">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="af695-1599">İlke tanımı oluştur yardım örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-1599">Updated create policy definition help example</span></span>
- <span data-ttu-id="af695-1600">Remove-AZADServicePrincipal -ServicePrincipalName’in boş referans adı bulunamadığında boş referans sunması hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-1600">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="af695-1601">Kiracının aboneliği olmadığında New-AZADServicePrincipal’ın boş referans sunmasına ilişkin hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-1601">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="af695-1602">Kimlik bilgilerini yalnızca ilişkili uygulamaya eklemek için New-AzAdServicePrincipal değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-1602">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="af695-1603">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="af695-1603">Az.Sql</span></span>
* <span data-ttu-id="af695-1604">ReadReplicaCount veritabanı için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-1604">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="af695-1605">Alan yedekliliği ayarlı olmadığında Set-AzSqlDatabase düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-1605">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="af695-1606">3.0.0 - Kasım 2019</span><span class="sxs-lookup"><span data-stu-id="af695-1606">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="af695-1607">Genel</span><span class="sxs-lookup"><span data-stu-id="af695-1607">General</span></span>
* <span data-ttu-id="af695-1608">Az.PrivateDns 1.0.0 yayınlandı</span><span class="sxs-lookup"><span data-stu-id="af695-1608">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="af695-1609">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="af695-1609">Az.Accounts</span></span>
* <span data-ttu-id="af695-1610">'Resolve-Error' diğer adı için bir kullanımdan kaldırma iletisi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="af695-1610">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="af695-1611">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="af695-1611">Az.Advisor</span></span>
* <span data-ttu-id="af695-1612">Get-AzAdvisorRecommendation cmdlet'ine yeni 'Operational Excellence' (Operasyonel Mükemmellik) kategorisi eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-1612">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="af695-1613">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="af695-1613">Az.Batch</span></span>
* <span data-ttu-id="af695-1614">`BatchAccountContext` içinde `CoreQuota`, `DedicatedCoreQuota` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="af695-1614">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="af695-1615">Ayrıca yeni bir `LowPriorityCoreQuota` var.</span><span class="sxs-lookup"><span data-stu-id="af695-1615">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="af695-1616">Bu **Get-AzBatchAccount** cmdlet'ini etkiliyor.</span><span class="sxs-lookup"><span data-stu-id="af695-1616">This impacts **Get-AzBatchAccount** .</span></span>
* <span data-ttu-id="af695-1617">**New-AzBatchTask**`-ResourceFile` parametresi şimdi yeni **New-AzBatchResourceFile** cmdlet’i kullanılarak oluşturulabilen bir `PSResourceFile` koleksiyonu alıyor.</span><span class="sxs-lookup"><span data-stu-id="af695-1617">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="af695-1618">`PSResourceFile` nesnelerini oluşturmaya yardımcı olmak için yeni **New-AzBatchResourceFile** cmdlet'i.</span><span class="sxs-lookup"><span data-stu-id="af695-1618">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="af695-1619">Bunlar `-ResourceFile` parametresinde **New-AzBatchTask** cmdlet'ine sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="af695-1619">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="af695-1620">Mevcut `HttpUrl` yolunun yanı sıra iki tür yeni kaynak dosyasını destekliyor:</span><span class="sxs-lookup"><span data-stu-id="af695-1620">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="af695-1621">`AutoStorageContainerName` tabanlı kaynak dosyaları bir otomatik depolama kapsayıcısının tamamını Batch düğümüne indiriyor.</span><span class="sxs-lookup"><span data-stu-id="af695-1621">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="af695-1622">`StorageContainerUrl` tabanlı kaynak dosyaları URL'de belirtilen kapsayıcıyı Batch düğümüne indiriyor.</span><span class="sxs-lookup"><span data-stu-id="af695-1622">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="af695-1623">**Get-AzBatchApplication** tarafından döndürülen `PSApplication` öğesinin `ApplicationPackages` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="af695-1623">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication** .</span></span>
  - <span data-ttu-id="af695-1624">Uygulamanın içindeki belirli paketler artık **Get-AzBatchApplicationPackage** kullanılarak alınabilir.</span><span class="sxs-lookup"><span data-stu-id="af695-1624">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage** .</span></span> <span data-ttu-id="af695-1625">Örneğin: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="af695-1625">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="af695-1626">**Get-AzBatchApplicationPackage** , **New-AzBatchApplicationPackage** , **Remove-AzBatchApplicationPackage** , **Get-AzBatchApplication** , **New-AzBatchApplication** , **Remove-AzBatchApplication** , ve **Set-AzBatchApplication** cmdlet'lerinde `ApplicationId` parametresi `ApplicationName` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="af695-1626">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage** , **New-AzBatchApplicationPackage** , **Remove-AzBatchApplicationPackage** , **Get-AzBatchApplication** , **New-AzBatchApplication** , **Remove-AzBatchApplication** , and **Set-AzBatchApplication** .</span></span>
  - <span data-ttu-id="af695-1627">`ApplicationId` artık `ApplicationName` parametresinin diğer adıdır.</span><span class="sxs-lookup"><span data-stu-id="af695-1627">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="af695-1628">`PSUserAccount` öğesine yeni `PSWindowsUserConfiguration` özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-1628">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="af695-1629">`PSApplicationPackage` içinde `Version` öğesi `Name` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="af695-1629">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="af695-1630">`PSResourceFile` içinde `BlobSource` öğesi `HttpUrl` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="af695-1630">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="af695-1631">`PSVirtualMachineConfiguration` içinden `OSDisk` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="af695-1631">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="af695-1632">**Set-AzBatchPoolOSVersion** kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="af695-1632">Removed **Set-AzBatchPoolOSVersion** .</span></span> <span data-ttu-id="af695-1633">Bu işlem artık desteklenmiyor.</span><span class="sxs-lookup"><span data-stu-id="af695-1633">This operation is no longer supported.</span></span>
* <span data-ttu-id="af695-1634">`PSCloudServiceConfiguration` içinden `TargetOSVersion` kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="af695-1634">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="af695-1635">`PSCloudServiceConfiguration` içinde `CurrentOSVersion` öğesi `OSVersion` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="af695-1635">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="af695-1636">`PSPoolUsageMetrics` içinden `DataEgressGiB` ve `DataIngressGiB` kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="af695-1636">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="af695-1637">**Get-AzBatchNodeAgentSku** kaldırıldı ve bunun yerini **Get-AzBatchSupportedImage** aldı.</span><span class="sxs-lookup"><span data-stu-id="af695-1637">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage** .</span></span>
  - <span data-ttu-id="af695-1638">**Get-AzBatchSupportedImage** , **Get-AzBatchNodeAgentSku** ile aynı verileri ama daha kullanımı kolay bir biçimde döndürüyor.</span><span class="sxs-lookup"><span data-stu-id="af695-1638">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="af695-1639">Artık yeni doğrulanmamış resimler de döndürülüyor.</span><span class="sxs-lookup"><span data-stu-id="af695-1639">New non-verified images are also now returned.</span></span> <span data-ttu-id="af695-1640">Her resim için `Capabilities` ve `BatchSupportEndOfLife` hakkında ek bilgiler de ekleniyor.</span><span class="sxs-lookup"><span data-stu-id="af695-1640">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="af695-1641">**New-AzBatchPool** cmdlet'inin `MountConfiguration` parametresiyle havuzun her düğümünde uzak dosya sistemlerini bağlama özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-1641">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool** .</span></span>
* <span data-ttu-id="af695-1642">Artık trafiğin kaynak bağlantı noktası temelinde havuza ağ erişimini engelleyen ağ güvenlik kuralları destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="af695-1642">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="af695-1643">Bu destek `PSNetworkSecurityGroupRule` öğesinin `SourcePortRanges` özelliğiyle sağlanıyor.</span><span class="sxs-lookup"><span data-stu-id="af695-1643">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="af695-1644">Kapsayıcıyı çalıştırırken, şimdi Batch görevin kapsayıcı çalışma dizininde veya Batch görevi çalışma dizininde yürütülmesini destekliyor.</span><span class="sxs-lookup"><span data-stu-id="af695-1644">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="af695-1645">Bu, `PSTaskContainerSettings` öğesinin `WorkingDirectory` özelliğiyle denetleniyor.</span><span class="sxs-lookup"><span data-stu-id="af695-1645">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="af695-1646">Yeni `PublicIPs` özelliği aracılığıyla `PSNetworkConfiguration` parametresinde bir genel IP koleksiyonu belirtme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-1646">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="af695-1647">Bu sayede Havuzdaki düğümlerin kullanıcı tarafından sağlanan IP listesinden bir IP alması garanti ediliyor.</span><span class="sxs-lookup"><span data-stu-id="af695-1647">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="af695-1648">Belirtilmediğinde, `PSSTartTask` üzerindeki `WaitForSuccess` öğesinin varsayılan değeri artık `$True` (daha önce `$False` değeriydi).</span><span class="sxs-lookup"><span data-stu-id="af695-1648">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="af695-1649">Belirtilmediğinde, `PSAutoUserSpecification` üzerindeki `Scope` öğesinin varsayılan değeri artık `Pool` (daha önce Windows'da `Task` ve Linux'ta `Pool` değeriydi).</span><span class="sxs-lookup"><span data-stu-id="af695-1649">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="af695-1650">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="af695-1650">Az.Cdn</span></span>
* <span data-ttu-id="af695-1651">RulesEngine'e UrlRewriteAction ve CacheKeyQueryStringAction eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-1651">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="af695-1652">New-AzDeliveryRuleCondition cmdlet'inde eksik 'Selector' Girişi gibi çeşitli hatalar düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-1652">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="af695-1653">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="af695-1653">Az.Compute</span></span>
* <span data-ttu-id="af695-1654">Disk Şifreleme Kümesi özelliği</span><span class="sxs-lookup"><span data-stu-id="af695-1654">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="af695-1655">Yeni cmdlet’ler:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="af695-1655">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="af695-1656">Aşağıdaki cmdlet'lere DiskEncryptionSetId parametresi eklendi:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="af695-1656">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="af695-1657">Aşağıdaki cmdlet'lere DiskEncryptionSetId ve EncryptionType parametreleri eklendi:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="af695-1657">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="af695-1658">New-AzVmssIPConfig cmdlet'ine PublicIPAddressVersion parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1658">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="af695-1659">Özel betik uzantısının FileUris öğesi genel ayardan korumalı ayara taşındı</span><span class="sxs-lookup"><span data-stu-id="af695-1659">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="af695-1660">New-AzVmss, New-AzVmssConfig ve Update-AzVmss cmdlet'lerine ScaleInPolicy eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1660">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="af695-1661">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="af695-1661">Breaking changes</span></span>
    - <span data-ttu-id="af695-1662">CreateOption değeri Upload olduğunda New-AzDiskConfig cmdlet'i için DiskSizeGB yerine UploadSizeInBytes parametresi kullanılıyor</span><span class="sxs-lookup"><span data-stu-id="af695-1662">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="af695-1663">GalleryImageVersion nesnesinde PublishingProfile.Source.ManagedImage.Id yerini StorageProfile.Source.Id'ye bıraktı</span><span class="sxs-lookup"><span data-stu-id="af695-1663">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="af695-1664">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="af695-1664">Az.DataFactory</span></span>
* <span data-ttu-id="af695-1665">ADF .Net SDK sürümü 4.3.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-1665">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="af695-1666">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="af695-1666">Az.DataLakeStore</span></span>
* <span data-ttu-id="af695-1667">ADLS SDK sürümünün güncelleştirilmesi (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) aşağıdaki düzeltmeleri sağlıyor</span><span class="sxs-lookup"><span data-stu-id="af695-1667">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="af695-1668">Geri dönüşüm kutusu veya dizin girdisinin creationtime öğesi seri durumdan çıkarılamadığında özel durum oluşturulmasını önleme.</span><span class="sxs-lookup"><span data-stu-id="af695-1668">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="af695-1669">adlsclient içinde istek başına zaman aşımı ayarını kullanıma sunma</span><span class="sxs-lookup"><span data-stu-id="af695-1669">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="af695-1670">badoffset kurtarması için özgün syncflag değerinin geçirilmesini düzeltme</span><span class="sxs-lookup"><span data-stu-id="af695-1670">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="af695-1671">Yanıt denetlendikten sonra devamlılık belirtecini almak için EnumerateDirectory'yi düzeltme</span><span class="sxs-lookup"><span data-stu-id="af695-1671">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="af695-1672">Birleştirme Hatasını Düzeltme</span><span class="sxs-lookup"><span data-stu-id="af695-1672">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="af695-1673">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="af695-1673">Az.FrontDoor</span></span>
* <span data-ttu-id="af695-1674">Modüllerde çeşitli yazım hataları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-1674">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="af695-1675">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="af695-1675">Az.HDInsight</span></span>
* <span data-ttu-id="af695-1676">ADLSGen1 depolamasıyla kümeyi almak için Get-AzHDInsightCluster cmdlet'ini kullandığında müşterinin 'Geçerli bir Base-64 dizesi değil' hatası almasına yol açan hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-1676">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="af695-1677">Müşterinin Azure Data Lake'e erişirken hizmet sorumlusu uygulama kimliğini sağlayabilmesi için üç cmdlet'e (Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig ve New-AzHDInsightCluster) 'ApplicationId' parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-1677">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="af695-1678">Microsoft.Azure.Management.HDInsight 2.1.0'dan 5.1.0'a geçirildi</span><span class="sxs-lookup"><span data-stu-id="af695-1678">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="af695-1679">Beş cmdlet kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="af695-1679">Removed five cmdlets:</span></span>
    - <span data-ttu-id="af695-1680">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="af695-1680">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="af695-1681">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="af695-1681">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="af695-1682">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="af695-1682">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="af695-1683">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="af695-1683">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="af695-1684">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="af695-1684">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="af695-1685">Üç cmdlet eklendi:</span><span class="sxs-lookup"><span data-stu-id="af695-1685">Added three cmdlets:</span></span>
    - <span data-ttu-id="af695-1686">Get-AzHDInsightMonitoring (Get-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="af695-1686">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="af695-1687">Enable-AzHDInsightMonitoring (Enable-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="af695-1687">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="af695-1688">Disable-AzHDInsightMonitoring (Disable-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="af695-1688">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="af695-1689">Belirli bir konumdan özellik bilgilerinin alınmasını desteklemek için Get-AzHDInsightProperties cmdlet'i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-1689">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="af695-1690">Add-AzHDInsightConfigValue cmdlet'inden parametre kümeleri ('Spark1', 'Spark2') kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="af695-1690">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="af695-1691">Add-AzHDInsightSecurityProfile cmdlet'inin yardım belgelerine örnekler eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-1691">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="af695-1692">Aşağıdaki cmdlet'lerin çıkış türü değiştirildi:</span><span class="sxs-lookup"><span data-stu-id="af695-1692">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="af695-1693">Get-AzHDInsightProperties cmdlet'inin CapabilitiesResponse olan çıkış türü AzureHDInsightCapabilities olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-1693">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="af695-1694">Remove-AzHDInsightCluster cmdlet'inin ClusterGetResponse olan çıkış türü bool olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-1694">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="af695-1695">Set-AzHDInsightGatewaySettings cmdlet'inin HttpConnectivitySettings olan çıkış türü GatewaySettings olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-1695">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="af695-1696">Bazı senaryo test çalışmaları eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-1696">Added some scenario test cases.</span></span>
* <span data-ttu-id="af695-1697">Bazı diğer adlar kaldırıldı: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="af695-1697">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="af695-1698">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="af695-1698">Az.IotHub</span></span>
* <span data-ttu-id="af695-1699">Hataya neden olan değişiklikler:</span><span class="sxs-lookup"><span data-stu-id="af695-1699">Breaking changes:</span></span>
    - <span data-ttu-id="af695-1700">'Add-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="af695-1700">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="af695-1701">'Add-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="af695-1701">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="af695-1702">'Get-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="af695-1702">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="af695-1703">'Get-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="af695-1703">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="af695-1704">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' türündeki 'OperationsMonitoringProperties' özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="af695-1704">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="af695-1705">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' türündeki 'OperationsMonitoringProperties' özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="af695-1705">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="af695-1706">'New-AzIotHubExportDevice' cmdlet'i artık 'New-AzIotHubExportDevices' diğer adını desteklemiyor.</span><span class="sxs-lookup"><span data-stu-id="af695-1706">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="af695-1707">'New-AzIotHubImportDevice' cmdlet'i artık 'New-AzIotHubImportDevices' diğer adını desteklemiyor.</span><span class="sxs-lookup"><span data-stu-id="af695-1707">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="af695-1708">'Remove-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="af695-1708">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="af695-1709">'Remove-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="af695-1709">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="af695-1710">'Set-AzIotHub' cmdet'i artık 'OperationsMonitoringProperties' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="af695-1710">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="af695-1711">'Set-AzIotHub' cmdlet'inden 'UpdateOperationsMonitoringProperties' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="af695-1711">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="af695-1712">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="af695-1712">Az.RecoveryServices</span></span>
* <span data-ttu-id="af695-1713">NSG, genel IP ve Azure'dan Azure'a iç yük dengeleyiciler gibi ağ kaynaklarını yapılandırmak için Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="af695-1713">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="af695-1714">Azure'a vMWare için yönetilen diske yazmaya yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="af695-1714">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="af695-1715">Azure'a vMWare için NIC azaltmasına yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="af695-1715">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="af695-1716">Azure'a Azure için hızlandırılmış ağa yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="af695-1716">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="af695-1717">Azure'a Azure için aracı otomatik güncelleştirmesine yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="af695-1717">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="af695-1718">Azure'a Azure için Standart SSD'ye yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="af695-1718">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="af695-1719">Azure'a Azure için Azure Disk Şifrelemesi iki geçişine yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="af695-1719">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="af695-1720">Azure'a Azure için yeni eklenen diski korumaya yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="af695-1720">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="af695-1721">VM için SoftDelete özelliği eklendi ve softdelete için de testler eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1721">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="af695-1722">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="af695-1722">Az.Resources</span></span>
* <span data-ttu-id="af695-1723">Bağımlılık derlemesi Microsoft.Extensions.Caching.Memory 1.1.1'den 2.2'ye güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-1723">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="af695-1724">Az.Network</span><span class="sxs-lookup"><span data-stu-id="af695-1724">Az.Network</span></span>
* <span data-ttu-id="af695-1725">PrivateEndpointConnection için tüm cmdlet'ler genel hizmet sağlayıcısını destekleyecek şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-1725">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="af695-1726">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="af695-1726">Updated cmdlet:</span></span>
        - <span data-ttu-id="af695-1727">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="af695-1727">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="af695-1728">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="af695-1728">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="af695-1729">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="af695-1729">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="af695-1730">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="af695-1730">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="af695-1731">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="af695-1731">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="af695-1732">PrivateLinkResource için yeni cmdlet eklendi ve bu da genel hizmet sağlayıcısını destekliyor.</span><span class="sxs-lookup"><span data-stu-id="af695-1732">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="af695-1733">Yeni cmdlet:</span><span class="sxs-lookup"><span data-stu-id="af695-1733">New cmdlet:</span></span>
        - <span data-ttu-id="af695-1734">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="af695-1734">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="af695-1735">Proxy Protocol V2 özelliği için yeni alanlar ve parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-1735">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="af695-1736">PrivateLinkService'e EnableProxyProtocol özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1736">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="af695-1737">PrivateEndpointConnection'a LinkIdentifier özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1737">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="af695-1738">New-AzPrivateLinkService cmdlet'i yeni isteğe bağlı EnableProxyProtocol parametresi eklenerek güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-1738">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="af695-1739">'New-AzApplicationGatewaySku' başvuru belgelerindeki yanlış parametre açıklaması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-1739">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="af695-1740">Azure güvenlik duvarı ilkesini desteklemek için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1740">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="af695-1741">VirtualHub'ın RouteTables alt kaynağı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1741">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="af695-1742">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="af695-1742">New cmdlets added:</span></span>
        - <span data-ttu-id="af695-1743">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="af695-1743">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="af695-1744">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="af695-1744">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="af695-1745">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="af695-1745">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="af695-1746">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="af695-1746">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="af695-1747">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="af695-1747">Set-AzVirtualHub</span></span>
* <span data-ttu-id="af695-1748">VirtualWan'ın yeni VirtualHub ve VirtualWANType özellikleri Sku'su için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1748">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="af695-1749">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="af695-1749">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="af695-1750">New-AzVirtualHub : Sku parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1750">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="af695-1751">Update-AzVirtualHub : Sku parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1751">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="af695-1752">New-AzVirtualWan : VirtualWANType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1752">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="af695-1753">Update-AzVirtualWan : VirtualWANType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1753">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="af695-1754">HubVnetConnection, VpnConnection ve ExpressRouteConnection için EnableInternetSecurity özelliği desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1754">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="af695-1755">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="af695-1755">New cmdlets added:</span></span>
        - <span data-ttu-id="af695-1756">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="af695-1756">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="af695-1757">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="af695-1757">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="af695-1758">New-AzureRmVirtualHubVnetConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1758">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="af695-1759">New-AzureRmVpnConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1759">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="af695-1760">Update-AzureRmVpnConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1760">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="af695-1761">New-AzureRmExpressRouteConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1761">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="af695-1762">Set-AzureRmExpressRouteConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1762">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="af695-1763">TopLevel WebApplicationFirewall İlkesini Yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1763">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="af695-1764">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="af695-1764">New cmdlets added:</span></span>
        - <span data-ttu-id="af695-1765">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="af695-1765">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="af695-1766">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="af695-1766">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="af695-1767">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="af695-1767">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="af695-1768">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="af695-1768">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="af695-1769">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="af695-1769">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="af695-1770">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="af695-1770">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="af695-1771">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="af695-1771">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="af695-1772">New-AzApplicationGatewayFirewallPolicy : PolicySetting, ManagedRule parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1772">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="af695-1773">CustomRule'da Geo-Match işleci için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1773">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="af695-1774">FirewallCondition'da işlece GeoMatch eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1774">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="af695-1775">perListener ve perSite Güvenlik duvarı ilkesi için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1775">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="af695-1776">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="af695-1776">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="af695-1777">New-AzApplicationGatewayHttpListener : FirewallPolicy, FirewallPolicyId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1777">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="af695-1778">New-AzApplicationGatewayPathRuleConfig : FirewallPolicy, FirewallPolicyId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1778">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="af695-1779">'PSBastion' içinde AzureBastionSubnet adlı gerekli alt ağın büyük/küçük harfe duyarlı olması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-1779">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="af695-1780">Azure Güvenlik Duvarı için Ağ Kurallarında Hedef FQDN'lere ve NAT Kurallarında Çevrilmiş FQDN'ye yönelik destek</span><span class="sxs-lookup"><span data-stu-id="af695-1780">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="af695-1781">IpGroup'un RouteTables üst düzey kaynağı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1781">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="af695-1782">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="af695-1782">New cmdlets added:</span></span>
        - <span data-ttu-id="af695-1783">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="af695-1783">New-AzIpGroup</span></span>
        - <span data-ttu-id="af695-1784">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="af695-1784">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="af695-1785">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="af695-1785">Get-AzIpGroup</span></span>
        - <span data-ttu-id="af695-1786">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="af695-1786">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="af695-1787">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="af695-1787">Az.ServiceFabric</span></span>
* <span data-ttu-id="af695-1788">Bu senaryo artık Add-AzVmssSecret cmdlet'inin kapsamına girdiğinden Add-AzServiceFabricApplicationCertificate cmdlet'i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="af695-1788">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="af695-1789">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="af695-1789">Az.Sql</span></span>
* <span data-ttu-id="af695-1790">Yönetilen Örneklerde bırakılan veritabanlarını geri yükleme desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-1790">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="af695-1791">Eski denetim cmdlet'leri kodda kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="af695-1791">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="af695-1792">Kullanım dışı bırakılan diğer adlar kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="af695-1792">Removed deprecated aliases:</span></span>
* <span data-ttu-id="af695-1793">Get-AzSqlDatabaseIndexRecommendations (bunun yerine Get-AzSqlDatabaseIndexRecommendation kullanın)</span><span class="sxs-lookup"><span data-stu-id="af695-1793">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="af695-1794">Get-AzSqlDatabaseRestorePoints (bunun yerine Get-AzSqlDatabaseRestorePoint kullanıldı)</span><span class="sxs-lookup"><span data-stu-id="af695-1794">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="af695-1795">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet'i kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="af695-1795">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="af695-1796">Kullanım dışı bırakılan Güvenlik Açığı Değerlendirmesi Ayarları cmdlet'lerinin diğer adları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="af695-1796">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="af695-1797">Gelişmiş Tehdit Algılama Ayarları cmdlet'leri kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="af695-1797">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="af695-1798">Veritabanındaki sütunlarda duyarlılık önerilerini devre dışı bırakma ve etkinleştirme cmdlet'leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-1798">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="af695-1799">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="af695-1799">Az.Storage</span></span>
* <span data-ttu-id="af695-1800">Depolama hesabı oluşturulur veya güncelleştirilirken Büyük dosya paylaşımını etkinleştirme desteği</span><span class="sxs-lookup"><span data-stu-id="af695-1800">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="af695-1801">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="af695-1801">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="af695-1802">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="af695-1802">Set-AzStorageAccount</span></span>
* <span data-ttu-id="af695-1803">Dosya işleyicisi kapatılırken/alınırken, DeletePending durumundaki nesnesinde hata olmasını önlemek için giriş yolunun Dosya dizini mi yoksa Dosya mı olduğunu denetlemeyi atlayın</span><span class="sxs-lookup"><span data-stu-id="af695-1803">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="af695-1804">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="af695-1804">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="af695-1805">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="af695-1805">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="af695-1806">2.8.0 - Ekim 2019</span><span class="sxs-lookup"><span data-stu-id="af695-1806">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="af695-1807">Genel</span><span class="sxs-lookup"><span data-stu-id="af695-1807">General</span></span>
* <span data-ttu-id="af695-1808">Az.HealthcareApis 1.0.0 sürümü</span><span class="sxs-lookup"><span data-stu-id="af695-1808">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="af695-1809">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="af695-1809">Az.Accounts</span></span>
* <span data-ttu-id="af695-1810">Oluşturulan modüller için telemetri ve URL’yi yeniden yazma özelliği güncelleştirildi, Windows birim testleri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-1810">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="af695-1811">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="af695-1811">Az.ApiManagement</span></span>
* <span data-ttu-id="af695-1812">**Set-AzApiManagementApi** - ApiVersionSet’e Güncelleştirme API’si desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1812">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="af695-1813">[https://github.com/Azure/azure-powershell/issues/10068](https://github.com/Azure/azure-powershell/issues/10068 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-1813">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="af695-1814">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="af695-1814">Az.Automation</span></span>
* <span data-ttu-id="af695-1815">Linux yeniden başlatma ayarı parametresi için New-AzureAutomationSoftwareUpdateConfiguration cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-1815">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="af695-1816">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="af695-1816">Az.Batch</span></span>
* <span data-ttu-id="af695-1817">Kullanımdan kaldırılan **Get-AzBatchNodeAgentSku** yerine 2.0.0 sürümünde **Get-AzBatchSupportImage** kullanıma sunulacak.</span><span class="sxs-lookup"><span data-stu-id="af695-1817">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="af695-1818">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="af695-1818">Az.Compute</span></span>
* <span data-ttu-id="af695-1819">New-AzVM ve New-AzVmss cmdlet’lerine Priority, EvictionPolicy ve MaxPrice parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1819">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="af695-1820">Add-AzVMAdditionalUnattendContent ve Add-AzVMSshPublicKey cmdlet’leri için uyarı iletisi ve yardım belgesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-1820">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="af695-1821">Set-AzVMDiskEncryptionExtension için yönetilen diskleri olan Linux VM’lere yönelik -skipVmBackup özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-1821">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="af695-1822">Set-AzVMDiskEncryptionExtension’daki iki geçişli senaryoda güncelleştirme şifreleme ayarlarındaki hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-1822">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="af695-1823">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="af695-1823">Az.DataFactory</span></span>
* <span data-ttu-id="af695-1824">ADF V2 veri akışı için CRUD komutları eklendi: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, ve Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="af695-1824">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="af695-1825">ADF V2 veri akışı hata ayıklama oturumu için eylem komutları eklendi: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand ve Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="af695-1825">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="af695-1826">ADF .Net SDK sürümü 4.2.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-1826">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="af695-1827">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="af695-1827">Az.DataLakeStore</span></span>
* <span data-ttu-id="af695-1828">‘-’ içeren hesapların etki alanı olmadan geçirilebilmesi için hesap doğrulama düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-1828">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="af695-1829">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="af695-1829">Az.HealthcareApis</span></span>
* <span data-ttu-id="af695-1830">PowerShell sürümü 1.0.0 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-1830">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="af695-1831">SDK sürümü 1.0.2 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-1831">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="af695-1832">Yeni SDK sürümüne başvurmaları için testler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-1832">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="af695-1833">İç içe geçmiş çıkış yapısı, düzleştirilmiş olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-1833">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="af695-1834">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="af695-1834">Az.IotHub</span></span>
* <span data-ttu-id="af695-1835">Yeni yönlendirme kaynağı eklendi: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="af695-1835">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="af695-1836">Küçük hata düzeltmesi: Get-AzIothub SubscriptionId öğesini döndürmüyor</span><span class="sxs-lookup"><span data-stu-id="af695-1836">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="af695-1837">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="af695-1837">Az.Monitor</span></span>
* <span data-ttu-id="af695-1838">Eylem grupları -ItsmReceiver -VoiceReceiver -ArmRoleReceiver -AzureFunctionReceiver -LogicAppReceiver -AutomationRunbookReceiver -AzureAppPushReceiver için yeni eylem grubu alıcıları eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1838">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="af695-1839">Alıcılar için etkinleştirilen ortak uyarı şemasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="af695-1839">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="af695-1840">Bunlar SMS, Azure Uygulaması iletimi, ITSM ve ses alıcıları için geçerli değildir</span><span class="sxs-lookup"><span data-stu-id="af695-1840">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="af695-1841">Web kancaları artık Azure Active Directory kimlik doğrulamasını destekliyor.</span><span class="sxs-lookup"><span data-stu-id="af695-1841">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="af695-1842">Az.Network</span><span class="sxs-lookup"><span data-stu-id="af695-1842">Az.Network</span></span>
* <span data-ttu-id="af695-1843">Hizmet Uç Noktası İlkeleri için kullanılabilen diğer adları almak için çağrılabilen Get-AzAvailableServiceAlias cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-1843">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="af695-1844">Sanal Ağ Geçidi Bağlantılarına trafik seçicileri eklemeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1844">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="af695-1845">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="af695-1845">New cmdlets added:</span></span>
        - <span data-ttu-id="af695-1846">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="af695-1846">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="af695-1847">Cmdlet’ler, şu isteğe bağlı parametreler ile güncelleştirildi: -TrafficSelectorPolicies -New-AzureRmVirtualNetworkGatewayConnection -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="af695-1847">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="af695-1848">Ağ güvenlik kuralı yapılandırmalarında ESP ve AH protokollerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1848">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="af695-1849">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="af695-1849">Updated cmdlets:</span></span>
        - <span data-ttu-id="af695-1850">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="af695-1850">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="af695-1851">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="af695-1851">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="af695-1852">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="af695-1852">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="af695-1853">Cortex cmdlet’lerinde özel durumların işlenmesi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-1853">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="af695-1854">VirtualNetworkGateways için yeni Nesiller ve SKU’lar</span><span class="sxs-lookup"><span data-stu-id="af695-1854">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="af695-1855">VirtualNetworkGateways için yeni Nesiller sunuldu.</span><span class="sxs-lookup"><span data-stu-id="af695-1855">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="af695-1856">VirtualNetworkGateways için yüksek verimliliğe sahip yeni SKU’lar sunuldu.</span><span class="sxs-lookup"><span data-stu-id="af695-1856">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="af695-1857">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="af695-1857">Az.RedisCache</span></span>
* <span data-ttu-id="af695-1858">‘-Size’ parametresine yönelik eksik değerleri eklemek için ‘Set-AzRedisCache’ başvuru belgesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-1858">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="af695-1859">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="af695-1859">Az.Sql</span></span>
* <span data-ttu-id="af695-1860">Yönetilen örnekte Active Directory yöneticisini ayarlama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1860">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="af695-1861">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="af695-1861">Az.Storage</span></span>
* <span data-ttu-id="af695-1862">Depolama İstemcisi Kitaplığı 11.1.0 sürümüne yükseltildi</span><span class="sxs-lookup"><span data-stu-id="af695-1862">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="af695-1863">Yönetim düzlemi API’si olan liste kapsayıcıları NextPageLink ile listelenecek</span><span class="sxs-lookup"><span data-stu-id="af695-1863">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="af695-1864">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="af695-1864">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="af695-1865">Abonelikteki Liste Depolama hesapları NextPageLink ile listelenecek</span><span class="sxs-lookup"><span data-stu-id="af695-1865">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="af695-1866">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="af695-1866">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="af695-1867">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="af695-1867">Az.StorageSync</span></span>
* <span data-ttu-id="af695-1868">Reset-AzStorageSyncServerCertificate öğesinde Sorun 9810 düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-1868">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="af695-1869">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="af695-1869">Az.Websites</span></span>
* <span data-ttu-id="af695-1870">Bir uygulamanın ASP’sini güncelleştiren Set-AzWebApp başarısız oluyor</span><span class="sxs-lookup"><span data-stu-id="af695-1870">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="af695-1871">2.7.0 - Eylül 2019</span><span class="sxs-lookup"><span data-stu-id="af695-1871">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="af695-1872">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="af695-1872">Az.ApiManagement</span></span>
* <span data-ttu-id="af695-1873">'Set-AzApiManagementPolicy' başvuru belgesindeki '-Format' parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-1873">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="af695-1874">Kullanım dışı bırakılan 'Update-AzApiManagementDeployment' cmdlet’ine başvurular, başvuru belgesinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="af695-1874">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="af695-1875">Bunun yerine 'Set-AzApiManagement' kullanın.</span><span class="sxs-lookup"><span data-stu-id="af695-1875">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="af695-1876">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="af695-1876">Az.Automation</span></span>
* <span data-ttu-id="af695-1877">'Register-AzAutomationDscNode' için başvuru belgesindeki örnek yazım yanlışı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-1877">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="af695-1878">Register-AzAutomationDSCNode için işletim sistemi kısıtlamasına açıklama eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1878">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="af695-1879">-Wait seçeneği için Start-AzAutomationRunbook cmdlet’i Null başvuru özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-1879">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="af695-1880">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="af695-1880">Az.Compute</span></span>
* <span data-ttu-id="af695-1881">New-AzDiskConfig cmdlet’ine UploadSizeInBytes parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1881">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="af695-1882">New-AzSnapshotConfig cmdlet’ine Incremental parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1882">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="af695-1883">Düşük öncelikli sanal makine özelliği eklendi:</span><span class="sxs-lookup"><span data-stu-id="af695-1883">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="af695-1884">New-AzVMConfig cmdlet’ine MaxPrice, EvictionPolicy ve Priority parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-1884">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="af695-1885">New-AzVmssConfig, Update-AzVM ve Update-AzVmss cmdlet’lerine MaxPrice parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-1885">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="af695-1886">Get-AzAvailabilitySet cmdlet’i abonelikteki tüm kullanılabilirlik kümelerini listelediğinde oluşan VM başvuru sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-1886">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="af695-1887">Get-AzRemoteDesktopFile için null özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-1887">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="af695-1888">Sona göre konum için VHD Seek yöntemi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-1888">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="af695-1889">New-AzVM ve Update-AzVM için UltraSSD sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-1889">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="af695-1890">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="af695-1890">Az.DataFactory</span></span>
* <span data-ttu-id="af695-1891">ADF V2’ye 3 yeni komut eklendi - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription ve Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="af695-1891">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="af695-1892">ADF .Net SDK sürümü 4.1.3’e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-1892">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="af695-1893">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="af695-1893">Az.HDInsight</span></span>
* <span data-ttu-id="af695-1894">Son değişiklikler duyurusu</span><span class="sxs-lookup"><span data-stu-id="af695-1894">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="af695-1895">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="af695-1895">Az.IotHub</span></span>
* <span data-ttu-id="af695-1896">Coğrafi olarak eşleştirilmiş olağanüstü durum kurtarma bölgesine bir IotHub için yük devretme çağırmaya yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-1896">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="af695-1897">IotHub için ileti zenginleştirmelerini yönetmeye yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-1897">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="af695-1898">Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="af695-1898">New cmdlets are:</span></span>
    - <span data-ttu-id="af695-1899">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="af695-1899">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="af695-1900">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="af695-1900">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="af695-1901">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="af695-1901">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="af695-1902">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="af695-1902">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="af695-1903">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="af695-1903">Az.Monitor</span></span>
* <span data-ttu-id="af695-1904">En son İzleme SDK’sını, yani 0.24.1-preview sürümünü işaret eder</span><span class="sxs-lookup"><span data-stu-id="af695-1904">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="af695-1905">Ölçüm cmdlet’lerine hataya neden olmayan değişiklikler ekler, yani Birim sabit listesi birçok yeni değeri destekler.</span><span class="sxs-lookup"><span data-stu-id="af695-1905">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="af695-1906">Bunlar salt okunur cmdlet’ler olduğundan girişlerinde değişiklik olmaz.</span><span class="sxs-lookup"><span data-stu-id="af695-1906">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="af695-1907">**ActionGroups** istekleri için api-version şimdi **2019-06-01** değerine sahiptir. Önceden **2018-03-01** sürümü kullanılıyordu.</span><span class="sxs-lookup"><span data-stu-id="af695-1907">The api-version of the **ActionGroups** requests is now **2019-06-01** , before it was **2018-03-01** .</span></span> <span data-ttu-id="af695-1908">Senaryo testleri bu değişikliğe uyum sağlayacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-1908">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="af695-1909">**EmailReceiver** ve **WebhookReceiver** sınıfları için oluşturuculara yeni bir zorunlu bağımsız değişken ( **useCommonAlertSchema** adlı bir Boole değeri) eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-1909">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema** .</span></span> <span data-ttu-id="af695-1910">Şu anda, hataya neden olan bu değişikliği cmdlet’lerden gizlemek için değer **false** olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="af695-1910">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="af695-1911">**NOT** : Bu, Uyarılar ekibi tarafından doğrulanması gereken geçici bir değişikliktir.</span><span class="sxs-lookup"><span data-stu-id="af695-1911">**NOTE** : this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="af695-1912">**Kaynak** ( **ScheduledQueryRuleSource** sınıfı ile ilişkili) sınıfının oluşturucusu için bağımsız değişkenlerin sırası önceki SDK’dan değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-1912">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="af695-1913">Bu değişiklik iki birim testinin düzeltilmesini gerektirdi: Bunlar derlenebiliyor ancak testleri geçemiyordu.</span><span class="sxs-lookup"><span data-stu-id="af695-1913">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="af695-1914">**AlertingAction** ( **ScheduledQueryRuleSource** sınıfı ile ilişkili) sınıfının oluşturucusu için bağımsız değişkenlerin sırası önceki SDK’dan değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-1914">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="af695-1915">Bu değişiklik iki birim testinin düzeltilmesini gerektirdi: Bunlar derlenebiliyor ancak testleri geçemiyordu.</span><span class="sxs-lookup"><span data-stu-id="af695-1915">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="af695-1916">Ölçüm uyarısı V2 için Dinamik Eşik ölçütlerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1916">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="af695-1917">New-AzMetricAlertRuleV2Criteria: Şimdi dinamik eşik ölçütleri de oluşturur</span><span class="sxs-lookup"><span data-stu-id="af695-1917">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="af695-1918">Add-AzMetricAlertRuleV2: Şimdi dinamik eşik ölçütlerini de kabul eder</span><span class="sxs-lookup"><span data-stu-id="af695-1918">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="af695-1919">Zamanlanmış Sorgu Kuralı cmdlet’lerinde (SQR) geliştirmeler</span><span class="sxs-lookup"><span data-stu-id="af695-1919">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="af695-1920">Cmdlet’ler 'Location' parametresini hem konum (ör. eastus) hem de konumun görünen adı (ör. Doğu ABD) biçiminde kabul eder</span><span class="sxs-lookup"><span data-stu-id="af695-1920">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="af695-1921">'Enabled' parametresi yardım dosyalarında düzgün şekilde açıklandı</span><span class="sxs-lookup"><span data-stu-id="af695-1921">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="af695-1922">İsteğe bağlı 'ActionGroup' parametresi için örnekler eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1922">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="af695-1923">Yardım dosyaları genel olarak geliştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-1923">Overall improved help files</span></span>
* <span data-ttu-id="af695-1924">'Set-AzActionRule' için kapsam türünü belirlemeyle ilgili bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-1924">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="af695-1925">Az.Network</span><span class="sxs-lookup"><span data-stu-id="af695-1925">Az.Network</span></span>
* <span data-ttu-id="af695-1926">'New-AzApplicationGateway' başvuru belgesindeki yanlış örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-1926">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="af695-1927">'Get-AzNetworkWatcherPacketCapture' başvuru belgesine paket yakalama için tüm özellikleri almayla ilgili not eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1927">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="af695-1928">'Test-AzNetworkWatcherIPFlow' başvuru belgesindeki örnek, NIC’lerin doğru olarak numaralandırılacağı şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-1928">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="af695-1929">Bulut özel durum ayrıştırması, mevcut olması durumunda daha fazla ayrıntı gösterecek şekilde iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-1929">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="af695-1930">Bulut özel durum ayrıştırması, ek SDK özel durum türünü işleyecek şekilde geliştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-1930">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="af695-1931">Güvenlik Kuralı modellerinin yanlış eşlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-1931">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="af695-1932">Özel IP özelliği için ağ arabirimine özellikler eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1932">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="af695-1933">'PrivateEndpoint' özelliği PSResourceId türü olarak PSNetworkInterface öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1933">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="af695-1934">'PrivateLinkConnectionProperties' özelliği PSIpConfigurationConnectivityInformation türü olarak PSNetworkInterfaceIPConfiguration öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1934">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="af695-1935">Yeni PSIpConfigurationConnectivityInformation model sınıfı eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1935">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="af695-1936">Azure Güvenlik Duvarı kaynağı için 'mssql' adlı yeni ApplicationRuleProtocolType eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1936">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="af695-1937">Sanal WAN’da çoklu bağlantı desteği</span><span class="sxs-lookup"><span data-stu-id="af695-1937">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="af695-1938">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="af695-1938">New cmdlets</span></span>
        - <span data-ttu-id="af695-1939">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="af695-1939">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="af695-1940">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="af695-1940">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="af695-1941">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="af695-1941">Updated cmdlet:</span></span>
        - <span data-ttu-id="af695-1942">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="af695-1942">New-VpnSite</span></span>
        - <span data-ttu-id="af695-1943">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="af695-1943">Update-VpnSite</span></span>
        - <span data-ttu-id="af695-1944">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="af695-1944">New-VpnConnection</span></span>
        - <span data-ttu-id="af695-1945">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="af695-1945">Update-VpnConnection</span></span>
* <span data-ttu-id="af695-1946">Belgeler, bazı PowerShell örneklerinde AzureRM cmdlet’leri yerine Az cmdlet’leri kullanılacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-1946">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="af695-1947">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="af695-1947">Az.RecoveryServices</span></span>
* <span data-ttu-id="af695-1948">AzureVMpolicy Nesnesi, ProtectedItemsCount Özniteliği ile güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-1948">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="af695-1949">VM ilkesi ve Özgün Depolama Hesabı Geri Yükleme için Testler eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1949">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="af695-1950">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="af695-1950">Az.Resources</span></span>
* <span data-ttu-id="af695-1951">New-AzRoleAssignment cmdlet’inin Scope parametresi olmadan çağrılamamasına neden olan bir hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-1951">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="af695-1952">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="af695-1952">Az.ServiceFabric</span></span>
* <span data-ttu-id="af695-1953">'Update-AzServiceFabricReliability' başvuru belgesindeki örnekteki yazım yanlışı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-1953">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="af695-1954">Uygulamaları ve hizmetleri yönetmek için yeni cmdlet’ler ekleniyor:</span><span class="sxs-lookup"><span data-stu-id="af695-1954">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="af695-1955">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="af695-1955">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="af695-1956">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="af695-1956">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="af695-1957">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="af695-1957">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="af695-1958">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="af695-1958">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="af695-1959">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="af695-1959">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="af695-1960">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="af695-1960">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="af695-1961">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="af695-1961">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="af695-1962">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="af695-1962">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="af695-1963">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="af695-1963">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="af695-1964">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="af695-1964">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="af695-1965">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="af695-1965">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="af695-1966">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="af695-1966">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="af695-1967">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="af695-1967">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="af695-1968">Service Fabric SDK’sı, Service Fabric kaynak sağlayıcısı api-version 2019-03-01 kullanan 1.2.0 sürümüne yükseltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-1968">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="af695-1969">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="af695-1969">Az.SignalR</span></span>
* <span data-ttu-id="af695-1970">Update, Restart, CheckNameAvailability, GetUsage Cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1970">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="af695-1971">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="af695-1971">Az.Sql</span></span>
* <span data-ttu-id="af695-1972">'Get-AzSqlElasticPool' için başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-1972">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="af695-1973">Elastik havuz oluşturmak (New-AzSqlElasticPool) için sanal çekirdek örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-1973">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="af695-1974">Set-AzSqlServerAdvancedThreatProtectionPolicy ve Set-AzSqlDatabaseAdvancedThreatProtectionPolicy içinde EmailAddresses’in doğrulanması ve EmailAddresses’in boş olması durumunda EmailAdmins’in false olmamasına yönelik denetim kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="af695-1974">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="af695-1975">Denetim kategorisini etkinleştiren birden çok tanılama ayarı olduğunda sunucu/veritabanı denetim ayarlarının kaldırılması etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-1975">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="af695-1976">Birden çok Sql Güvenlik Açığı Değerlendirmesi cmdlet’inde (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting ve Update-AzSqlInstanceVulnerabilityAssessmentSetting) e-posta adresleri doğrulaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-1976">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="af695-1977">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="af695-1977">Az.Storage</span></span>
* <span data-ttu-id="af695-1978">'Get-AzStorageAccountKey' için başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-1978">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="af695-1979">Azure Dosyasını karşıya yüklerken/indirirken, hedef dosyada, dosya SMB özelliklerinin (Dosya Öznitelikleri, Dosya Oluşturma Zamanı, Dosya Son Yazma Zamanı) korunmasına yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1979">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="af695-1980">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="af695-1980">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="af695-1981">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="af695-1981">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="af695-1982">Kapsayıcı tarafından etkinleştirilmiş ImmutabilityPolicy üzerinde özellikler/meta tarih hatası içeren Karşıya yükleme blok blobu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-1982">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="af695-1983">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="af695-1983">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="af695-1984">Yönetim düzlemi API’si ile Azure Dosya paylaşımlarını yönetmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-1984">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="af695-1985">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="af695-1985">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="af695-1986">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="af695-1986">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="af695-1987">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="af695-1987">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="af695-1988">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="af695-1988">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="af695-1989">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="af695-1989">Az.Websites</span></span>
* <span data-ttu-id="af695-1990">Uygulamanın yeni ASP’ye geçirilmesi sırasında webapp Etiketlerinin silinmesine neden olan bir sorun düzeltiliyor</span><span class="sxs-lookup"><span data-stu-id="af695-1990">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="af695-1991">Publish-AzureWebapp cmdlet’i Linux ve Windows üzerinde çalışacak şekilde düzeltiliyor</span><span class="sxs-lookup"><span data-stu-id="af695-1991">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="af695-1992">'Get-AzWebAppPublishingProfile' başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-1992">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="af695-1993">2.6.0 - Ağustos 2019</span><span class="sxs-lookup"><span data-stu-id="af695-1993">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="af695-1994">Genel</span><span class="sxs-lookup"><span data-stu-id="af695-1994">General</span></span>
* <span data-ttu-id="af695-1995">Çok sayıda modülde çeşitli yazım hataları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-1995">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="af695-1996">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="af695-1996">Az.Accounts</span></span>
* <span data-ttu-id="af695-1997">Azure İşlevleri Kimlik Doğrulaması’nda kullanıcı tarafından atanan MSI desteği (#9479)</span><span class="sxs-lookup"><span data-stu-id="af695-1997">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="af695-1998">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="af695-1998">Az.Aks</span></span>
* <span data-ttu-id="af695-1999">‘Get-AzAks’ için çıkışla ilgili bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-1999">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="af695-2000">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="af695-2000">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="af695-2001">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="af695-2001">Az.ApiManagement</span></span>
* <span data-ttu-id="af695-2002">[https://github.com/Azure/azure-powershell/issues/9351](https://github.com/Azure/azure-powershell/issues/9351 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2002">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="af695-2003">ProductID, APIID, GroupID ve UserID için kısıtlamaları zorunlu kılmayan .NET NuGet sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2003">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="af695-2004">**Get-AzApiManagementProduct** - Ürünleri API kullanarak sorgulama desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-2004">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="af695-2005">**New-AzApiManagementApiRevision** - Yeni API düzeltmesi oluşturulurken ApiRevisionDescription parametresinin ayarlanmamasına neden olan sorun düzeltildi https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="af695-2005">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="af695-2006">'PsApiManagementOAuth2AuthrozationServer' modeli 'PsApiManagementOAuth2AuthorizationServer' olarak değiştirilerek yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2006">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="af695-2007">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="af695-2007">Az.Batch</span></span>
* <span data-ttu-id="af695-2008">Windows’un ilk harfi büyütülerek yardım iletisindeki ve belgelerdeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2008">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="af695-2009">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="af695-2009">Az.Cdn</span></span>
* <span data-ttu-id="af695-2010">CDN modülü dönüştürme yardımcısındaki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2010">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="af695-2011">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="af695-2011">Az.Compute</span></span>
* <span data-ttu-id="af695-2012">New-AzVMConfig cmdlet’ine VmssID eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2012">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="af695-2013">New-AzVmssConfig ve Update-AzVmss öğelerine TerminateScheduledEvents ve TerminateScheduledEventNotBeforeTimeoutInMinutes parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2013">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="af695-2014">VM görüntüsü nesnesine HyperVGeneration özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2014">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="af695-2015">Host ve HostGroup özellikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2015">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="af695-2016">Yeni cmdlet’ler:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="af695-2016">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="af695-2017">New-AzVMConfig ve New-AzVM öğelerine HostId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2017">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="af695-2018">Doğru parametre adını kullanmak için ‘Invoke-AzVMRunCommand’ belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2018">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="af695-2019">'Set-AzVMDiskEncryptionExtension' ve 'Set-AzVmssDiskEncryptionExtension' referans belgelerindeki '-VolumeType' açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2019">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="af695-2020">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="af695-2020">Az.DataFactory</span></span>
* <span data-ttu-id="af695-2021">‘Windows’ sözcüğünün baş harfi büyütülerek 'New-AzDataFactoryEncryptValue' belgesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2021">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="af695-2022">ADF .Net SDK sürümü 4.1.2’ye güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2022">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="af695-2023">Şirket İçinde Barındırılan Integration Runtime’ı SSIS Integration Runtime için ara sunucu olarak ayarlamak üzere 'Set-AzureRmDataFactoryV2IntegrationRuntime' komutuna 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' ve 'DataProxyStagingPath' parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2023">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="af695-2024">Tetiklenen işlem hatlarını, iletiyi ve özellikleri göstermesi için PSTriggerRun öğesi, etkinlik türünü göstermesi için de PSActivityRun öğesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2024">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="af695-2025">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="af695-2025">Az.DataLakeStore</span></span>
* <span data-ttu-id="af695-2026">Hata veya uzak özel durumları için Get-DataLakeStoreDeletedItem öğesinin yanıt vermemeye başlaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-2026">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="af695-2027">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="af695-2027">Az.EventHub</span></span>
* <span data-ttu-id="af695-2028">#9658 numaralı şu sorun düzeltildi: Set-AzEventHubNetworkRuleSet öğesinde bulunan VirtualNteworkRule parametresindeki yazım hatası</span><span class="sxs-lookup"><span data-stu-id="af695-2028">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="af695-2029">#9558 numaralı şu sorun düzeltildi: Set-AzEventHubNamespace öğesinin PUT yerine PATCH kullanması</span><span class="sxs-lookup"><span data-stu-id="af695-2029">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="af695-2030">Set-AzEventHubNamespace cmdlet’ine EnableKafka parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2030">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="af695-2031">#9786 numaralı şu sorun düzeltildi: Yalnızca dinleme haklarıyla bir kural oluşturulamaması</span><span class="sxs-lookup"><span data-stu-id="af695-2031">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="af695-2032">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="af695-2032">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="af695-2033">‘Azure’ın’ tamamen küçük harflerle yazılmasıyla belgede oluşan yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2033">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="af695-2034">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="af695-2034">Az.Monitor</span></span>
* <span data-ttu-id="af695-2035">Yardım belgelerindeki yanlış parametre adı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2035">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="af695-2036">Az.Network</span><span class="sxs-lookup"><span data-stu-id="af695-2036">Az.Network</span></span>
* <span data-ttu-id="af695-2037">New-AzPrivateLinkServiceIpConfig güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2037">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="af695-2038">Sunucu tarafında hiç kullanılmadığı için ‘PublicIpAddress’ parametresi kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="af695-2038">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="af695-2039">Mevcut IP yapılandırmasının birincil yapılandırma olup olmadığını belirten bir isteğe bağlı bir parametre (‘Primary’) eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-2039">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="af695-2040">SDK’daki istek hatası özel durumunun işlenmesi geliştirildi. Bu, daha önceden SDK özel durumlarının düzgün şekilde işlenenmemesiyle oluşan ve önemli hata ayrıntılarının görüntülenmemesine neden olan sorunu düzeltir</span><span class="sxs-lookup"><span data-stu-id="af695-2040">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="af695-2041">Doğru IPv6 ön ek uzunluğunu denetlemek amacıyla Ipv6 IP Ön eki için doğrulama mantığı ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="af695-2041">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="af695-2042">Get-AzVirtualNetworkSubnetConfig güncelleştirildi: Alt ağ kaynak kimliği ile almak için parametre kümesi eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-2042">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="af695-2043">AzNetworkServiceTag için Konum parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2043">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="af695-2044">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="af695-2044">Az.OperationalInsights</span></span>
* <span data-ttu-id="af695-2045">'New-AzOperationalInsightsLinuxSyslogDataSource' öğesine yönelik belgeler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2045">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="af695-2046">Örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2046">Added example</span></span>
    - <span data-ttu-id="af695-2047">‘-Name’ parametresi için açıklama güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2047">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="af695-2048">New-AzOperationalInsightsWindowsEventDataSource için bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2048">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="af695-2049">New-AzOperationalInsightsWindowsEventDataSource için -Name parametresinin açıklaması değiştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2049">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="af695-2050">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="af695-2050">Az.RecoveryServices</span></span>
* <span data-ttu-id="af695-2051">'Get-AzRecoveryServicesBackupJobDetail.md' dosyası güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2051">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="af695-2052">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="af695-2052">Az.Resources</span></span>
* <span data-ttu-id="af695-2053">Microsoft.Resource için yeni API sürümüne (2019-05-10) yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2053">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="af695-2054">Değişkenler, kaynaklar ve özellikler için copy.count = 0 parametresine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2054">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="af695-2055">'condition = false' veya 'copy.count = 0' içeren kaynaklar tam modda silinir</span><span class="sxs-lookup"><span data-stu-id="af695-2055">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="af695-2056">Belgelere yardımcı olması için abonelik düzeyinde ilke atama örneği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2056">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="af695-2057">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="af695-2057">Az.ServiceBus</span></span>
* <span data-ttu-id="af695-2058">#9658 numaralı şu sorun düzeltildi: Set-AzServiceBusNetworkRuleSet öğesinde bulunan VirtualNetworkRule parametresindeki yazım hatası</span><span class="sxs-lookup"><span data-stu-id="af695-2058">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="af695-2059">#9786 numaralı şu sorun düzeltildi: Yalnızca dinleme haklarıyla bir kural oluşturulamaması</span><span class="sxs-lookup"><span data-stu-id="af695-2059">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="af695-2060">Sıra ve konu için ad kullanılabilirliğini denetlemeye yönelik yeni komut ('Test-AzServiceBusNameAvailability') eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2060">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="af695-2061">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="af695-2061">Az.ServiceFabric</span></span>
* <span data-ttu-id="af695-2062">Düğüm ekleme türü cmdlet hataları düzeltildi:</span><span class="sxs-lookup"><span data-stu-id="af695-2062">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="af695-2063">Kaynak grubunun Service Fabric kümesiyle ilgili diğer vmss öğesi olduğunda oluşan NullReferenceException hatası.</span><span class="sxs-lookup"><span data-stu-id="af695-2063">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="af695-2064">Şu sorunu düzeltir: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="af695-2064">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="af695-2065">virtualNetwork kümeyle farklı bir kaynak grubunda yer aldığında cmdlet’in başarısız olmasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-2065">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="af695-2066">Şu sorunu düzeltir: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="af695-2066">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="af695-2067">Add-AzServiceFabricApplicationCertificate cmdlet’i kullanımdan kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="af695-2067">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="af695-2068">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="af695-2068">Az.Sql</span></span>
* <span data-ttu-id="af695-2069">Eski denetim cmdlet’lerinin belgeleri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-2069">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="af695-2070">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="af695-2070">Az.Storage</span></span>
* <span data-ttu-id="af695-2071">Cmdlet örneklerine ve güncelleştirme parametresi açıklamalarına daha fazla senaryo eklenerek Get/Close-AzStorageFileHandle öğesi için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2071">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="af695-2072">Karşıya yükleme blobu ve kopyalama blobunda StandardBlobTier için destek</span><span class="sxs-lookup"><span data-stu-id="af695-2072">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="af695-2073">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="af695-2073">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="af695-2074">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="af695-2074">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="af695-2075">Blobu kopyala işleminde Yeniden Doldurma Önceliği Desteği</span><span class="sxs-lookup"><span data-stu-id="af695-2075">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="af695-2076">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="af695-2076">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="af695-2077">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="af695-2077">Az.Websites</span></span>
* <span data-ttu-id="af695-2078">Set-AzWebApp ve Set-AzWebAppSlot öğelerindeki -AppSettings parametresine yönelik açıklama eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2078">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="af695-2079">2.5.0 - Temmuz 2019</span><span class="sxs-lookup"><span data-stu-id="af695-2079">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="af695-2080">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="af695-2080">Az.Accounts</span></span>
* <span data-ttu-id="af695-2081">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2081">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="af695-2082">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="af695-2082">Az.ApplicationInsights</span></span>
* <span data-ttu-id="af695-2083">'Remove-AzApplicationInsightsApiKey' belgesindeki örnek yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2083">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="af695-2084">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="af695-2084">Az.Automation</span></span>
* <span data-ttu-id="af695-2085">Kaynak dizesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2085">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="af695-2086">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="af695-2086">Az.CognitiveServices</span></span>
* <span data-ttu-id="af695-2087">NetworkRuleSet desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-2087">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="af695-2088">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="af695-2088">Az.Compute</span></span>
* <span data-ttu-id="af695-2089">VM örneği görünüm nesnesinin eksik özellikleri (ComputerName, OsName, OsVersion ve HyperVGeneration) eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-2089">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="af695-2090">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="af695-2090">Az.ContainerRegistry</span></span>
* <span data-ttu-id="af695-2091">Çoğaltma parametresi için Remove-AzContainerRegistryReplication içindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2091">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="af695-2092">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="af695-2092">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="af695-2093">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="af695-2093">Az.DataFactory</span></span>
* <span data-ttu-id="af695-2094">ADF .Net SDK’sı 4.1.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2094">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="af695-2095">'Get-AzDataFactoryV2PipelineRun' belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2095">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="af695-2096">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="af695-2096">Az.EventHub</span></span>
* <span data-ttu-id="af695-2097">SAS belirteci oluşturmak için yeni cmdlet eklendi: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="af695-2097">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="af695-2098">yalnızca 'Manage' atanırsa authorizationrules hakları için doğrulama ve hata iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2098">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="af695-2099">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="af695-2099">Az.KeyVault</span></span>
* <span data-ttu-id="af695-2100">Sertifika İlkeleri için KeySize’ı belirtmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2100">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="af695-2101">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="af695-2101">Az.LogicApp</span></span>
* <span data-ttu-id="af695-2102">Get-AzIntegrationAccountMap’in tüm eşleme türlerini listelemesi için düzeltme</span><span class="sxs-lookup"><span data-stu-id="af695-2102">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="af695-2103">Filtreleme için yeni MapType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2103">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="af695-2104">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="af695-2104">Az.ManagedServices</span></span>
* <span data-ttu-id="af695-2105">API 2019-06-01 sürümü için destek eklendi (GA)</span><span class="sxs-lookup"><span data-stu-id="af695-2105">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="af695-2106">Az.Network</span><span class="sxs-lookup"><span data-stu-id="af695-2106">Az.Network</span></span>
* <span data-ttu-id="af695-2107">Özel uç nokta ve özel bağlantı hizmeti için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2107">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="af695-2108">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="af695-2108">New cmdlets</span></span>
        - <span data-ttu-id="af695-2109">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="af695-2109">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="af695-2110">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="af695-2110">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="af695-2111">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="af695-2111">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="af695-2112">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="af695-2112">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="af695-2113">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="af695-2113">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="af695-2114">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="af695-2114">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="af695-2115">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="af695-2115">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="af695-2116">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="af695-2116">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="af695-2117">Özellik için aşağıdaki komutlar güncelleştirildi: Virtualnetwork’te Alt Ağ üzerinde PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies bayrağı</span><span class="sxs-lookup"><span data-stu-id="af695-2117">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="af695-2118">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2118">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="af695-2119">Bu alt ağda özel uç nokta üzerinde ağ ilkelerinin uygulanıp uygulanmayacağını yapılandıran isteğe bağlı -PrivateEndpointNetworkPoliciesFlag parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-2119">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="af695-2120">Bu alt ağda özel bağlantı hizmeti üzerinde ağ ilkelerinin uygulanıp uygulanmayacağını yapılandıran isteğe bağlı -PrivateLinkServiceNetworkPoliciesFlag parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-2120">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="af695-2121">AzPrivateLinkService’in cmdlet 'ServiceName' parametresi, geriye yönelik uyumluluk için 'ServiceName' diğer adıyla 'Name' olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="af695-2121">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="af695-2122">Ağ güvenlik kuralı yapılandırmalarına yönelik ICMP protokolü etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2122">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="af695-2123">Cmdlet'ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2123">Updated cmdlets</span></span>
        - <span data-ttu-id="af695-2124">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="af695-2124">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="af695-2125">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="af695-2125">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="af695-2126">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="af695-2126">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="af695-2127">ConnectionProtocolType (Ikev1/Ikev2), New-AzVirtualNetworkGatewayConnection için yapılandırılabilir bir parametre olarak eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2127">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="af695-2128">LoadBalancerFrontendIpConfiguration içinde PrivateIpAddressVersion eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2128">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="af695-2129">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="af695-2129">Updated cmdlet:</span></span>
        - <span data-ttu-id="af695-2130">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="af695-2130">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="af695-2131">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="af695-2131">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="af695-2132">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="af695-2132">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="af695-2133">Yoklama içinde özek bağlantı noktasını desteklemek için Application Gateway New-AzApplicationGatewayProbeConfig komutu güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2133">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="af695-2134">New-AzApplicationGatewayProbeConfig güncelleştirildi: Arka uç sunucusunu yoklamak için kullanılan isteğe bağlı parametre Bağlantı Noktası eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-2134">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="af695-2135">Bu parametre Standard_V2 ve WAF_V2 SKU için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="af695-2135">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="af695-2136">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="af695-2136">Az.OperationalInsights</span></span>
* <span data-ttu-id="af695-2137">Kayıtlı aramaların varsayılan sürümü 1 olacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-2137">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="af695-2138">Özel günlük null normal ifade işleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2138">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="af695-2139">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="af695-2139">Az.RecoveryServices</span></span>
* <span data-ttu-id="af695-2140">'Get-AzRecoveryServicesBackupJob.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2140">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="af695-2141">'Get-AzRecoveryServicesBackupContainer.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2141">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="af695-2142">'Get-AzRecoveryServicesVault.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2142">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="af695-2143">'Wait-AzRecoveryServicesBackupJob.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2143">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="af695-2144">'Set-AzRecoveryServicesVaultContext.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2144">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="af695-2145">'Get-AzRecoveryServicesBackupItem.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2145">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="af695-2146">'Get-AzRecoveryServicesBackupRecoveryPoint.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2146">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="af695-2147">'Restore-AzRecoveryServicesBackupItem.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2147">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="af695-2148">Azure Dosya Paylaşımı kapsayıcısının Kaydını Silmeye yönelik hizmet çağrısı güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2148">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="af695-2149">'Set-AzRecoveryServicesAsrAlertSetting.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2149">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="af695-2150">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="af695-2150">Az.Resources</span></span>
- <span data-ttu-id="af695-2151">'New-AzResourceGroupDeployment' belgelerinde başvurulan eksik cmdlet kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="af695-2151">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="af695-2152">İlke cmdlet’leri yeni 2019-01-01 api sürümünü kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2152">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="af695-2153">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="af695-2153">Az.ServiceBus</span></span>
* <span data-ttu-id="af695-2154">SAS belirteci oluşturmak için yeni cmdlet eklendi: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="af695-2154">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="af695-2155">yalnızca 'Manage' atanırsa authorizationrules hakları için doğrulama ve hata iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2155">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="af695-2156">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="af695-2156">Az.Sql</span></span>
* <span data-ttu-id="af695-2157">Set-AzSqlDatabaseSecondary cmdlet’i için eksik örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2157">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="af695-2158">E-posta adresi sağlamadan yinelenen Güvenlik Açığı Değerlendirme taramalarının ayarlanması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2158">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="af695-2159">Bir uyarı iletisindeki küçük bir yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-2159">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="af695-2160">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="af695-2160">Az.Storage</span></span>
* <span data-ttu-id="af695-2161">'Get-AzStorageAccount' başvuru belgelerindeki örnek, doğru parametre adını kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2161">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="af695-2162">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="af695-2162">Az.StorageSync</span></span>
* <span data-ttu-id="af695-2163">Invoke-AzStorageSyncChangeDetection cmdlet’i ekleniyor.</span><span class="sxs-lookup"><span data-stu-id="af695-2163">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="af695-2164">TierFilesOlderThanDays’in uygulanmasına yönelik Sorun 9551 düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2164">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="af695-2165">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="af695-2165">Az.Websites</span></span>
* <span data-ttu-id="af695-2166">Bazı SiteConfig özelliklerinin Get-AzWebApp ve Set-AzWebApp tarafından döndürülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2166">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="af695-2167">Get-AzDeletedWebApp ve Restore-AzDeletedWebApp için yeni bir Konum parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2167">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="af695-2168">New-AzWebApp -IncludeSourceWebAppSlots kullanılarak web uygulaması yuvalarının kopyalanmasıyla ilgili bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2168">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="af695-2169">2.4.0 - Temmuz 2019</span><span class="sxs-lookup"><span data-stu-id="af695-2169">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="af695-2170">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="af695-2170">Az.Accounts</span></span>
* <span data-ttu-id="af695-2171">Profil cmdlet’leri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2171">Add support for profile cmdlets</span></span>
* <span data-ttu-id="af695-2172">Oluşturulan cmdlet’lerde ortamlar ve veri düzlemleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2172">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="af695-2173">Windows PowerShell’deki veri düzlemi cmdlet’leri için bazı durumlarda yanlış uç noktası kullanılması hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2173">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="af695-2174">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="af695-2174">Az.Advisor</span></span>
* <span data-ttu-id="af695-2175">Az.Advisor genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="af695-2175">GA release of Az.Advisor</span></span>
* <span data-ttu-id="af695-2176">Bu modül, artık toplama `Az` modülünün bir parçası olarak sunulur</span><span class="sxs-lookup"><span data-stu-id="af695-2176">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="af695-2177">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="af695-2177">Az.ApiManagement</span></span>
* <span data-ttu-id="af695-2178">[https://github.com/Azure/azure-powershell/issues/8671](https://github.com/Azure/azure-powershell/issues/8671 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2178">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="af695-2179">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="af695-2179">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="af695-2180">Abonelikleri Kullanıcı ve Ürüne göre sorgulama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2180">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="af695-2181">Kapsam kullanarak sorgulama desteği eklendi ('/', '/apis', '/apis/echo-api')</span><span class="sxs-lookup"><span data-stu-id="af695-2181">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="af695-2182">[https://github.com/Azure/azure-powershell/issues/9307](https://github.com/Azure/azure-powershell/issues/9307 ) ve https://github.com/Azure/azure-powershell/issues/8432 sorunları için düzeltme</span><span class="sxs-lookup"><span data-stu-id="af695-2182">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="af695-2183">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="af695-2183">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="af695-2184">API’leri içeri aktarırken ‘ApiVersion’ ve ‘ApiVersionSetId’ belirtmek için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2184">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="af695-2185">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="af695-2185">Az.Automation</span></span>
* <span data-ttu-id="af695-2186">Dize değerini işlemek için Set-AzAutomationConnectionFieldValue cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-2186">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="af695-2187">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="af695-2187">Az.Compute</span></span>
* <span data-ttu-id="af695-2188">New-AzImageConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2188">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="af695-2189">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="af695-2189">Az.DataFactory</span></span>
* <span data-ttu-id="af695-2190">Etkinlik çalıştırmalarını alma, işlem hattı çalıştırmalarını alma ve tetikleme çalıştırmalarını alma ADF cmdlet’lerinin çıkışları, Select-Object kanalını destekleyecek şekilde güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="af695-2190">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="af695-2191">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="af695-2191">Az.EventGrid</span></span>
* <span data-ttu-id="af695-2192">‘New-AzEventGridSubscription’ belgesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2192">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="af695-2193">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="af695-2193">Az.IotHub</span></span>
* <span data-ttu-id="af695-2194">Yetkilendirme ilkesi anahtarlarını yeniden oluşturma desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-2194">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="af695-2195">Az.Network</span><span class="sxs-lookup"><span data-stu-id="af695-2195">Az.Network</span></span>
* <span data-ttu-id="af695-2196">Genel IP etiketlerine ‘RoutingPreference’ eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2196">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="af695-2197">‘Get-AzNetworkServiceTag’ başvuru belgesi için örnekler geliştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2197">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="af695-2198">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="af695-2198">Az.PolicyInsights</span></span>
* <span data-ttu-id="af695-2199">Get-AzPolicyState’de boş başvuru sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2199">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="af695-2200">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="af695-2200">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="af695-2201">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="af695-2201">Az.OperationalInsights</span></span>
* <span data-ttu-id="af695-2202">Get-AzOperationalInsightsDataSource’da döndürülen CustomLog veri kaynağı modeli düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2202">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="af695-2203">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="af695-2203">Az.RecoveryServices</span></span>
* <span data-ttu-id="af695-2204">IaaSVM’ler için get-policy komutu düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="af695-2204">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="af695-2205">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="af695-2205">Az.Resources</span></span>
    - <span data-ttu-id="af695-2206">Get-AzPolicyState -Top parametresi için yardım metni düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="af695-2206">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="af695-2207">Get-AzPolicyAlias için istemci tarafı sayfalama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2207">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="af695-2208">Set-AzPolicyAssignment, -PolicyParameters ve -PolicyParametersObject için yeni parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2208">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="af695-2209">İlke cmdlet’leri için bazı belge ve örnekler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2209">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="af695-2210">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="af695-2210">Az.ServiceBus</span></span>
* <span data-ttu-id="af695-2211">4938 numaralı, MaxSizeInMegabytes ayarlanırken New-AzureRmServiceBusQueue’nun BadRequest döndürmesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2211">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="af695-2212">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="af695-2212">Az.Sql</span></span>
* <span data-ttu-id="af695-2213">Önizleme sürümündeki Örnek Yük Devretme Grubu cmdlet’leri genel kullanım sürümüne eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2213">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="af695-2214">Yeni cmdlet’ler ile Azure SQL Server\Veritabanı Denetimi desteği.</span><span class="sxs-lookup"><span data-stu-id="af695-2214">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="af695-2215">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="af695-2215">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="af695-2216">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="af695-2216">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="af695-2217">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="af695-2217">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="af695-2218">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="af695-2218">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="af695-2219">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="af695-2219">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="af695-2220">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="af695-2220">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="af695-2221">Güvenlik Açığı Değerlendirmesi ayarlarından e-posta kısıtlamaları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="af695-2221">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="af695-2222">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="af695-2222">Az.Storage</span></span>
* <span data-ttu-id="af695-2223">Aşağıdaki cmdlet’te 2 parametre (‘-IndexDocument’ ve ‘-ErrorDocument404Path’) gerekliden isteğe bağlı olarak değiştirildi:</span><span class="sxs-lookup"><span data-stu-id="af695-2223">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="af695-2224">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="af695-2224">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="af695-2225">Get-AzStorageBlobContent’in yardımı, örnek eklenerek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2225">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="af695-2226">Cmdlet StorageException ile başarısız olduğunda artık daha ayrıntılı hata bilgisi gösteriliyor</span><span class="sxs-lookup"><span data-stu-id="af695-2226">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="af695-2227">Azure Dosyalar AAD DS Kimlik Doğrulaması ile Depolama hesabı oluşturma veya güncelleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2227">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="af695-2228">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="af695-2228">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="af695-2229">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="af695-2229">Set-AzStorageAccount</span></span>
* <span data-ttu-id="af695-2230">Bir dosya paylaşımının, dosya dizininin veya dosyanın dosya tanıtıcılarını listeleme veya kapatma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2230">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="af695-2231">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="af695-2231">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="af695-2232">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="af695-2232">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="af695-2233">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="af695-2233">Az.StorageSync</span></span>
* <span data-ttu-id="af695-2234">Bu modül, artık toplama `Az` modülünün bir parçası olarak sunulur</span><span class="sxs-lookup"><span data-stu-id="af695-2234">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="af695-2235">2.3.2 - Haziran 2019</span><span class="sxs-lookup"><span data-stu-id="af695-2235">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="af695-2236">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="af695-2236">Az.Accounts</span></span>
* <span data-ttu-id="af695-2237">İşlevler çağrıları için bazı durumlarda yanlış URL’nin kullanılmasına neden olan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2237">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="af695-2238">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="af695-2238">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="af695-2239">AzureRM’den Az cmdlet’lerine yönelik diğer adlarla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2239">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="af695-2240">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="af695-2240">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="af695-2241">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="af695-2241">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="af695-2242">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="af695-2242">Az.Compute</span></span>
* <span data-ttu-id="af695-2243">New-AzVm ve New-AzVmss basit parametre kümeleri artık 'ProximityPlacementGroup' parametresini kabul ediyor.</span><span class="sxs-lookup"><span data-stu-id="af695-2243">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="af695-2244">'New-AzVM' başvuru belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2244">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="af695-2245">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="af695-2245">Az.Dns</span></span>
* <span data-ttu-id="af695-2246">'Set-AzDnsZone' yardım örneklerindeki bir yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-2246">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="af695-2247">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="af695-2247">Az.EventGrid</span></span>
* <span data-ttu-id="af695-2248">2019-06-01 API sürümünü kullanacak biçimde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-2248">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="af695-2249">Yeni cmdlet’ler:</span><span class="sxs-lookup"><span data-stu-id="af695-2249">New cmdlets:</span></span>
    - <span data-ttu-id="af695-2250">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="af695-2250">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="af695-2251">Yeni bir Azure Event Grid etki alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="af695-2251">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="af695-2252">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="af695-2252">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="af695-2253">Event Grid Etki Alanının ayrıntılarını veya mevcut Azure aboneliğindeki tüm Event Grid Etki Alanlarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="af695-2253">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="af695-2254">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="af695-2254">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="af695-2255">Bir Azure Event Grid Etki Alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="af695-2255">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="af695-2256">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="af695-2256">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="af695-2257">Bir Azure Event Grid Etki Alanı için paylaşılan erişim anahtarını yeniden üretir.</span><span class="sxs-lookup"><span data-stu-id="af695-2257">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="af695-2258">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="af695-2258">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="af695-2259">Etkinlikleri bir Event Grid Etki Alanıyla paylaşmak için kullanılan paylaşılan erişim anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="af695-2259">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="af695-2260">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="af695-2260">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="af695-2261">Yeni bir Azure Event Grid Etki Alanı Konu Başlığı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="af695-2261">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="af695-2262">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="af695-2262">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="af695-2263">Bir Event Grid Etki Alanının ayrıntılarını veya mevcut Azure aboneliğindeki belirli Event Grid Etki Alanlarının altında bulunan tüm Event Grid Etki Alanı Konu Başlıklarının listesini alır</span><span class="sxs-lookup"><span data-stu-id="af695-2263">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="af695-2264">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="af695-2264">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="af695-2265">Mevcut bir Azure Event Grid Etki Alanı Konu Başlığını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="af695-2265">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="af695-2266">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="af695-2266">Updated cmdlets:</span></span>
    - <span data-ttu-id="af695-2267">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="af695-2267">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="af695-2268">Bu kaynakların altında yeni olay aboneliklerinin oluşturulmasına olanak tanımak amacıyla yeni Event Grid Etki Alanı ve Event Grid Etki Alanı Konu Başlığına yönelik kanal oluşturmanın desteklemesi için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="af695-2268">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="af695-2269">Bu kaynakların altında yeni olay aboneliklerinin oluşturulmasına olanak tanımak amacıyla yeni Event Grid Etki Alanı adını ve/veya Event Grid Etki Alanı Konu Başlığının adını belirtmek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="af695-2269">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="af695-2270">Mevcut parametrelerin yeniden kullanılmasına olanak tanımak için etki alanları ve etki alanı konu başlıkları için yeni Parametre kümeleri (örneğin, EndPointType, SubjectBeginsWith vb.) ekler.</span><span class="sxs-lookup"><span data-stu-id="af695-2270">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="af695-2271">Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="af695-2271">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="af695-2272">Olay aboneliği bitiş tarihi,</span><span class="sxs-lookup"><span data-stu-id="af695-2272">Event subscription expiration date,</span></span>
            - <span data-ttu-id="af695-2273">Gelişmiş filtreleme parametreleri.</span><span class="sxs-lookup"><span data-stu-id="af695-2273">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="af695-2274">Hedef olarak servicebusqueue için yeni sabit listesi ekler.</span><span class="sxs-lookup"><span data-stu-id="af695-2274">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="af695-2275">-IncludedEventType seçeneğinde ‘All’ kullanılmasını engeller ve bunu şununla değiştirir</span><span class="sxs-lookup"><span data-stu-id="af695-2275">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="af695-2276">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="af695-2276">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="af695-2277">Sayfalandırma ve filtreleme sonuçlarını desteklemek için yeni isteğe bağlı parametreler (Top, ODataQuery and NextLink) ekler.</span><span class="sxs-lookup"><span data-stu-id="af695-2277">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="af695-2278">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="af695-2278">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="af695-2279">Bu kaynakların altında bulunan mevcut olay aboneliklerinin taşınmasına olanak tanımak amacıyla Event Grid Etki Alanı ve Event Grid Etki Alanı Konu Başlığına yönelik kanal oluşturmayı desteklemek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="af695-2279">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="af695-2280">Bu kaynakların altında bulunan mevcut olay aboneliklerinin taşınmasına olanak tanımak amacıyla Event Grid Etki Alanı adının ve/veya Event Grid Etki Alanı Konu Başlığı adını belirtmek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="af695-2280">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="af695-2281">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="af695-2281">Az.FrontDoor</span></span>
* <span data-ttu-id="af695-2282">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="af695-2282">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="af695-2283">Dönüştürmeler desteği ve yeni işleç otomatik tamamlama değeri (RegEx) ekler</span><span class="sxs-lookup"><span data-stu-id="af695-2283">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="af695-2284">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="af695-2284">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="af695-2285">Yeni otomatik tamamlama değerleri ekler</span><span class="sxs-lookup"><span data-stu-id="af695-2285">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="af695-2286">Az.Network</span><span class="sxs-lookup"><span data-stu-id="af695-2286">Az.Network</span></span>
* <span data-ttu-id="af695-2287">Sanal Ağ Geçidi Kaynağı için destek ekler</span><span class="sxs-lookup"><span data-stu-id="af695-2287">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="af695-2288">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="af695-2288">New cmdlets</span></span>
        - <span data-ttu-id="af695-2289">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="af695-2289">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="af695-2290">AvailablePrivateEndpointType ekler</span><span class="sxs-lookup"><span data-stu-id="af695-2290">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="af695-2291">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="af695-2291">New cmdlets</span></span>
        - <span data-ttu-id="af695-2292">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="af695-2292">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="af695-2293">PrivatePrivateLinkService ekler</span><span class="sxs-lookup"><span data-stu-id="af695-2293">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="af695-2294">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="af695-2294">New cmdlets</span></span>
        - <span data-ttu-id="af695-2295">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="af695-2295">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="af695-2296">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="af695-2296">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="af695-2297">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="af695-2297">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="af695-2298">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="af695-2298">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="af695-2299">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="af695-2299">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="af695-2300">PrivateEndpoint ekler</span><span class="sxs-lookup"><span data-stu-id="af695-2300">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="af695-2301">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="af695-2301">New cmdlets</span></span>
        - <span data-ttu-id="af695-2302">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="af695-2302">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="af695-2303">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="af695-2303">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="af695-2304">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="af695-2304">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="af695-2305">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="af695-2305">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="af695-2306">Özellik için aşağıdaki komutlar güncelleştirildi: VpnConnection’da UseLocalAzureIpAddress bayrağı</span><span class="sxs-lookup"><span data-stu-id="af695-2306">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="af695-2307">New-AzVpnConnection güncelleştirildi: Bağlantı başlatılırken yerel Azure IP adresinin kullanılması gerektiğini belirtmek için isteğe bağlı -UseLocalAzureIpAddress parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-2307">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="af695-2308">Set-AzVpnConnection güncelleştirildi: Bağlantı başlatılırken yerel Azure IP adresinin kullanılması gerektiğini belirtmek için isteğe bağlı -UseLocalAzureIpAddress parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-2308">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="af695-2309">ExpressRoute eşlemede PeeredConnections salt okunur alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-2309">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="af695-2310">ExpressRoute’ta GlobalReachEnabled salt okunur alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-2310">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="af695-2311">ExpressRouteCircuit modelindeki AllowGlobalReach alanının kullanımdan kaldırıldığını duyurmak için hataya neden olan değişiklik özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2311">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="af695-2312">AzApplicationGatewayRedirectConfiguration cmdlet’leri ile TargetListenerID’yi kullanırken oluşan 8756 Hatası Sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2312">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="af695-2313">New-AzApplicationGatewayPathRuleConfig’de yeniden yazma kuralının ayarlanmasını engelleyen hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-2313">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="af695-2314">NetworkInterfaceIpConfiguration’da VirtualNetworkTaps’in görüntülenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2314">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="af695-2315">Tümünü listele bölümü için Cortex Get cmdlet’leri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2315">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="af695-2316">ExpressRouteGateways ve VpnGateway için VirtualHub başvurusu oluşturma düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2316">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="af695-2317">AzureFirewall ve NatGateway için Kullanılabilirlik Alanları desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2317">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="af695-2318">Get-AzNetworkServiceTag cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2318">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="af695-2319">Azure Güvenlik Duvarı için birden fazla genel IP adresi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2319">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="af695-2320">New-AzFirewall cmdlet'i güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="af695-2320">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="af695-2321">Bir veya daha fazla Genel IP Adresi nesnesi kabul eden -PublicIpAddress parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2321">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="af695-2322">Bir Sanal Ağ nesnesini kabul eden -VirtualNetwork parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2322">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="af695-2323">Güvenlik duvarı nesnesine AddPublicIpAddress ve RemovePublicIpAddress yöntemleri eklendi - bunlar giriş olarak Genel IP Adresi nesnesini kabul eder</span><span class="sxs-lookup"><span data-stu-id="af695-2323">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="af695-2324">Kullanım dışı parametreler - PublicIpName ve -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="af695-2324">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="af695-2325">Özellik için aşağıdaki komutlar güncelleştirildi: Sanal ağ geçidi kaynağına VpnClient AAD kimlik doğrulaması seçenekleri ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="af695-2325">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="af695-2326">New-AzVirtualNetworkGateway güncelleştirildi: Ağ Geçidinde VpnClient AAD kimlik doğrulamasını ayarlamak için isteğe bağlı AadTenantUri, AadAudienceId, AadIssuerUri parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-2326">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="af695-2327">Set-AzVirtualNetworkGateway güncelleştirildi: Ağ Geçidinde VpnClient AAD kimlik doğrulamasını ayarlamak için isteğe bağlı AadTenantUri, AadAudienceId, AadIssuerUri parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-2327">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="af695-2328">Set-AzVirtualNetworkGateway güncelleştirildi: VpnClient AAD kimlik doğrulaması seçeneklerini Ağ Geçidinden kaldırmak için isteğe bağlı RemoveAadAuthentication anahtar parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-2328">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="af695-2329">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="af695-2329">Az.OperationalInsights</span></span>
* <span data-ttu-id="af695-2330">‘New-Azurermoperationalınsightsworkspace’ komutunda **pergb2018** fiyatlandırma katmanı etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2330">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="af695-2331">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="af695-2331">Az.Resources</span></span>
* <span data-ttu-id="af695-2332">Ek Şablon Dışarı Aktarma seçenekleri için destek</span><span class="sxs-lookup"><span data-stu-id="af695-2332">Support for additional Template Export options</span></span>
    - <span data-ttu-id="af695-2333">Export-AzResourceGroup’a ‘-SkipResourceNameParameterization’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2333">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="af695-2334">Export-AzResourceGroup’a ‘-SkipAllParameterization’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2334">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="af695-2335">Dışarı aktarılan kaynak filtrelemesi için Export-AzResourceGroup’a ‘Resource’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2335">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="af695-2336">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="af695-2336">Az.ServiceFabric</span></span>
* <span data-ttu-id="af695-2337">ByExistingKeyVault sertifika eklemenin bazı durumlarda yanlış parmak izi alması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2337">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="af695-2338">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="af695-2338">Az.Sql</span></span>
* <span data-ttu-id="af695-2339">Gelişmiş Tehdit Koruması depolama uç noktası son eki düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2339">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="af695-2340">Gelişmiş Veri Güvenliği’ni etkinleştirmenin Gelişmiş Tehdit Koruması ilkesini geçersiz kılması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2340">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="af695-2341">Müşterilerin yönetilen örnekler için TDE anahtarları ekleyip TDE koruyucusu ayarlamasına olanak tanımak için Management.Sql’e yönelik yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="af695-2341">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="af695-2342">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="af695-2342">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="af695-2343">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="af695-2343">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="af695-2344">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="af695-2344">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="af695-2345">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="af695-2345">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="af695-2346">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="af695-2346">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="af695-2347">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="af695-2347">Az.Storage</span></span>
* <span data-ttu-id="af695-2348">Depolama hesabı oluştururken FileStorage ve SkuName Premium_ZRS tiplerine yönelik destek</span><span class="sxs-lookup"><span data-stu-id="af695-2348">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="af695-2349">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="af695-2349">New-AzStorageAccount</span></span>
* <span data-ttu-id="af695-2350">Blob değiştirilemezlik cmdlet’inin açıklaması netleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2350">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="af695-2351">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="af695-2351">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="af695-2352">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="af695-2352">Az.Websites</span></span>
* <span data-ttu-id="af695-2353">Kaynak grubu ile filtrelemeyi istemci yerine sunucuda yapmasını sağlayarak Get-AzWebAppCertificate’ı iyileştirir</span><span class="sxs-lookup"><span data-stu-id="af695-2353">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="af695-2354">Get-AzWebAppSnapshot’a -UseDisasterRecovery anahtar parametresi ekler</span><span class="sxs-lookup"><span data-stu-id="af695-2354">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="af695-2355">2.2.0 - Haziran 2019</span><span class="sxs-lookup"><span data-stu-id="af695-2355">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="af695-2356">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="af695-2356">Az.Cdn</span></span>
* <span data-ttu-id="af695-2357">Cmdlet'ler API sürümü 2019-04-15’i temel alan rulesEngine özelliğini destekleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-2357">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="af695-2358">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="af695-2358">Az.Compute</span></span>
* <span data-ttu-id="af695-2359">İşlemi başlatan ve işlem tamamlanmadan önce hemen döndürülen `NoWait` parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-2359">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="af695-2360">Cmdlet'ler güncelleştirildi:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="af695-2360">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="af695-2361">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="af695-2361">Az.EventHub</span></span>
* <span data-ttu-id="af695-2362">#9231 - Get-AzEventHubNamespace etiketleri döndürmüyor hatasının düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="af695-2362">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="af695-2363">#9230 - Get-AzEventHubNamespace ResourceGroupName yerine ResourceGroup döndürüyor hatasının düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="af695-2363">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="af695-2364">Az.Network</span><span class="sxs-lookup"><span data-stu-id="af695-2364">Az.Network</span></span>
* <span data-ttu-id="af695-2365">Nat Gateway için ResourceId ve InputObject değerleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2365">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="af695-2366">ResourceId ve InputObject için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2366">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="af695-2367">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="af695-2367">Az.PolicyInsights</span></span>
* <span data-ttu-id="af695-2368">Get-AzPolicyEvent’de Boş referans sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2368">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="af695-2369">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="af695-2369">Az.RecoveryServices</span></span>
* <span data-ttu-id="af695-2370">IaaSVM ilkesinin gün cinsinden en kısa saklama süresi 1'den 7'ye değiştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2370">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="af695-2371">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="af695-2371">Az.ServiceBus</span></span>
* <span data-ttu-id="af695-2372">#9182 - Get-AzServiceBusNamespace ResourceGroupName yerine ResourceGroup döndürüyor sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="af695-2372">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="af695-2373">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="af695-2373">Az.ServiceFabric</span></span>
* <span data-ttu-id="af695-2374">'Update-AzServiceFabricReliability' hata iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2374">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="af695-2375">Service Fabric komut satırlarındaki eksik karakter düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2375">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="af695-2376">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="af695-2376">Az.Sql</span></span>
* <span data-ttu-id="af695-2377">Yönetilen Örnek için AutoDr’yi desteklemek amacıyla New-AzureSqlInstance cmdlet’ine DnsZonePartner parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-2377">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="af695-2378">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet’i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="af695-2378">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="af695-2379">Gelişmiş Tehdit Koruması için Tehdit Algılama cmdlet’leri yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="af695-2379">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="af695-2380">New-AzSqlInstance - StorageSizeInGB ve -LicenseType parametreleri artık isteğe bağlı.</span><span class="sxs-lookup"><span data-stu-id="af695-2380">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="af695-2381">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="af695-2381">Az.Websites</span></span>
* <span data-ttu-id="af695-2382">Set-AzWebApp ve Set-AzWebAppSlot, WebApp özelliğiyle kullanıldığında etiketlerin kaldırılmasına neden olan sorun giderildi</span><span class="sxs-lookup"><span data-stu-id="af695-2382">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="af695-2383">2.1.0 - Mayıs 2019</span><span class="sxs-lookup"><span data-stu-id="af695-2383">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="af695-2384">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="af695-2384">Az.ApiManagement</span></span>
* <span data-ttu-id="af695-2385">Genel Kapsamda ve API Kapsamında tanılamaları yönetmek için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="af695-2385">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="af695-2386">**Get-AzApiManagementDiagnostic** - Genel kapsam veya API Kapsamında yapılandırılan tanılamaları alır</span><span class="sxs-lookup"><span data-stu-id="af695-2386">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="af695-2387">**New-AzApiManagementDiagnostic** - Genel kapsamda veya API Kapsamında yeni tanılama oluşturur</span><span class="sxs-lookup"><span data-stu-id="af695-2387">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="af695-2388">**New-AzApiManagementHttpMessageDiagnostic** - Üst Bilgileri günlüğe kaydetme ve Gövde Baytları boyutu için tanılama ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="af695-2388">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="af695-2389">**New-AzApiManagementPipelineDiagnosticSetting** - Ağ Geçidinde gelen/giden HTTP iletileri için Tanılama ayarları oluşturur.</span><span class="sxs-lookup"><span data-stu-id="af695-2389">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="af695-2390">**New-AzApiManagementSamplingSetting** - Tanılamaya yönelik istekler/yanıtlar için Örnekleme Ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="af695-2390">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="af695-2391">**Remove-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama varlığını kaldırır</span><span class="sxs-lookup"><span data-stu-id="af695-2391">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="af695-2392">**Set-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama Varlığını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="af695-2392">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="af695-2393">ApiManagement hizmetinde Önbellek yönetimi için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="af695-2393">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="af695-2394">**Get-AzApiManagementCache** - Tanımlayıcı tarafından belirtilen Önbelleğin veya tüm önbelleklerin ayrıntılarını alır</span><span class="sxs-lookup"><span data-stu-id="af695-2394">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="af695-2395">**New-AzApiManagementCache** - Yeni bir 'varsayılan' Önbellek veya belirli bir azure 'bölgesinde' Önbellek oluşturur</span><span class="sxs-lookup"><span data-stu-id="af695-2395">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="af695-2396">**Remove-AzApiManagementCache** - Önbelleği kaldırır</span><span class="sxs-lookup"><span data-stu-id="af695-2396">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="af695-2397">**Update-AzApiManagementCache** - Önbelleği güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="af695-2397">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="af695-2398">API Şemasını yönetmek için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="af695-2398">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="af695-2399">**New-AzApiManagementSchema** - API için yeni Şema oluşturur</span><span class="sxs-lookup"><span data-stu-id="af695-2399">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="af695-2400">**Get-AzApiManagementSchema** - API'de yapılandırılan şemaları alır</span><span class="sxs-lookup"><span data-stu-id="af695-2400">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="af695-2401">**Remove-AzApiManagementSchema** - API'de yapılandırılan şemaları kaldırır</span><span class="sxs-lookup"><span data-stu-id="af695-2401">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="af695-2402">**Set-AzApiManagementSchema** - API'de yapılandırılan şemayı güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="af695-2402">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="af695-2403">Kullanıcı Belirteci oluşturmak için yeni Cmdlet oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="af695-2403">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="af695-2404">**New-AzApiManagementUserToken** - Varsayılan olarak 8 saat geçerli kalan yeni bir Kullanıcı Belirteci oluşturur. 'GIT' kullanıcısı için bu cmdlet kullanılarak Belirteç oluşturulabilir./</span><span class="sxs-lookup"><span data-stu-id="af695-2404">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="af695-2405">Ağ Durumunu almak için yeni cmdlet oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="af695-2405">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="af695-2406">**Get-AzApiManagementNetworkStatus** - API Management hizmetinin bağımlı olduğu kaynakların bağlantısında ağ durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="af695-2406">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="af695-2407">ApiManagement hizmeti Sanal Ağa dağıtılırken ve bağımlılıklardan herhangi birinin bozulup bozulmadığı denetlenirken bu cmdlet yararlı olur.</span><span class="sxs-lookup"><span data-stu-id="af695-2407">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="af695-2408">**New-AzApiManagement** cmdlet'i ApiManagement hizmetini yönetecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2408">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="af695-2409">Yeni 'Consumption' SKU'su için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2409">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="af695-2410">'Consumption' SKU'sunda 'EnableClientCertificate' bayrağını etkinleştirmek için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2410">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="af695-2411">Yeni **New-AzApiManagementSslSetting** cmdlet'i 'Backend' ve 'Frontend'de 'TLS/SSL' ayarını yapılandırmaya olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="af695-2411">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="af695-2412">Bu cmdlet ApiManagement hizmetinin 'Frontend'inde '3DES' gibi 'Ciphers' yapılandırması ve 'Http2' gibi 'ServerProtocols' yapılandırması için de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="af695-2412">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="af695-2413">ApiManagement hizmetinde 'DeveloperPortal' ana bilgisayar adının yapılandırması için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-2413">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="af695-2414">**Get-AzApiManagementSsoToken** cmdlet'leri giriş olarak 'PsApiManagement' nesnesini alacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2414">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="af695-2415">Cmdlet satır içinde Hata İletileri görüntüleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2415">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="af695-2416">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Hata Kodu: ValidationError Hata İletisi: Bir veya birden çok alan yanlış değerler içeriyor: Hata Ayrıntıları:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="af695-2416">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="af695-2417">**Export-AzApiManagementApi** cmdlet'i API'leri 'OpenApi 3.0' biçiminde dışarı aktaracak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2417">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="af695-2418">**Import-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2418">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="af695-2419">'OpenApi 3.0' belge belirtiminden Api'yi içeri aktarmak için</span><span class="sxs-lookup"><span data-stu-id="af695-2419">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="af695-2420">Herhangi bir ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') belgesinde belirtilen 'PsApiManagementSchema' özelliğini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="af695-2420">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="af695-2421">Herhangi bir belgede belirtilen 'ServiceUrl' özelliğini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="af695-2421">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="af695-2422">**Get-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak döndürecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2422">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="af695-2423">**Set-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak ve 'xml' kullanarak Xml kaçışlı kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2423">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="af695-2424">**New-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2424">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="af695-2425">API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="af695-2425">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="af695-2426">'ApiVersionSet' içinde API oluşturmak için</span><span class="sxs-lookup"><span data-stu-id="af695-2426">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="af695-2427">'SourceApiId' ve 'SourceApiRevision' kullanıp API'yi kopyalamak için.</span><span class="sxs-lookup"><span data-stu-id="af695-2427">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="af695-2428">Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği.</span><span class="sxs-lookup"><span data-stu-id="af695-2428">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="af695-2429">**Set-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2429">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="af695-2430">API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="af695-2430">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="af695-2431">API'yi 'ApiVersionSet' olarak güncelleştirmek için</span><span class="sxs-lookup"><span data-stu-id="af695-2431">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="af695-2432">Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği.</span><span class="sxs-lookup"><span data-stu-id="af695-2432">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="af695-2433">**New-AzApiManagementRevision** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2433">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="af695-2434">'SourceApiRevision' kullanarak mevcut düzeltmeyi kopyalamak (etiketleri, ürünleri, işlemleri ve ilkeleri kopyalamak) için.</span><span class="sxs-lookup"><span data-stu-id="af695-2434">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="af695-2435">Yeni Düzeltme üst öğenin 'ApiId' değerini varsayılan olarak alır.</span><span class="sxs-lookup"><span data-stu-id="af695-2435">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="af695-2436">'ApiRevisionDescription' sağlamak için</span><span class="sxs-lookup"><span data-stu-id="af695-2436">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="af695-2437">API kopyalanırken 'ServiceUrl' değerini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="af695-2437">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="af695-2438">**New-AzApiManagementIdentityProvider** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2438">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="af695-2439">'AAD' veya 'AADB2C'yi bir 'Authority' ile yapılandırmak için</span><span class="sxs-lookup"><span data-stu-id="af695-2439">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="af695-2440">'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' ve 'PasswordResetPolicy' ayarlamak için</span><span class="sxs-lookup"><span data-stu-id="af695-2440">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="af695-2441">**New-AzApiManagementSubscription** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2441">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="af695-2442">'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="af695-2442">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="af695-2443">'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="af695-2443">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="af695-2444">Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-2444">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="af695-2445">**Set-AzApiManagementSubscription** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2445">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="af695-2446">'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="af695-2446">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="af695-2447">'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="af695-2447">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="af695-2448">Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-2448">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="af695-2449">Aşağıdaki cmdlet'ler giriş olarak 'ResourceId' kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2449">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="af695-2450">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="af695-2450">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="af695-2451">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="af695-2451">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="af695-2452">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="af695-2452">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="af695-2453">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="af695-2453">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="af695-2454">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="af695-2454">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="af695-2455">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="af695-2455">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="af695-2456">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="af695-2456">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="af695-2457">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="af695-2457">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="af695-2458">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="af695-2458">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="af695-2459">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="af695-2459">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="af695-2460">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="af695-2460">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="af695-2461">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="af695-2461">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="af695-2462">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="af695-2462">Az.Automation</span></span>
* <span data-ttu-id="af695-2463">Get-AzAutomationJobOutputRecord, JSON ve Text kayıt değerlerini işleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-2463">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="af695-2464">[https://github.com/Azure/azure-powershell/issues/8347](https://github.com/Azure/azure-powershell/issues/7977 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2464">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="af695-2465">[https://github.com/Azure/azure-powershell/issues/8600](https://github.com/Azure/azure-powershell/issues/8600 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2465">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="af695-2466">Start-AzAutomationDscCompilationJob cmdlet'inin davranışı tamamlanmasını beklemek yerine yalnızca işi başlatacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-2466">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="af695-2467">[https://github.com/Azure/azure-powershell/issues/8347](https://github.com/Azure/azure-powershell/issues/8347 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2467">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="af695-2468">Get-AzAutomationDscNode için -Name kullanıldığında tüm düğümlerin döndürülmesi sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-2468">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="af695-2469">Artık yalnızca eşleşen düğüm döndürülüyor.</span><span class="sxs-lookup"><span data-stu-id="af695-2469">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="af695-2470">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="af695-2470">Az.Compute</span></span>
* <span data-ttu-id="af695-2471">Update-AzVmssVM cmdlet'ine ProtectFromScaleIn ve ProtectFromScaleSetAction parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-2471">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="af695-2472">New-AzVM basit parametre kümesi artık 'East US' desteklenmiyorsa varsayılan olarak kullanılabilir bir konumu kullanıyor</span><span class="sxs-lookup"><span data-stu-id="af695-2472">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="af695-2473">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="af695-2473">Az.DataLakeStore</span></span>
* <span data-ttu-id="af695-2474">ADLS sdk'si azure çerçevesiyle httpclient, tümleşik veri düzlemi testi kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2474">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="af695-2475">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="af695-2475">Az.Monitor</span></span>
* <span data-ttu-id="af695-2476">Yardım örneklerindeki yanlış parametre adları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2476">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="af695-2477">Az.Network</span><span class="sxs-lookup"><span data-stu-id="af695-2477">Az.Network</span></span>
* <span data-ttu-id="af695-2478">Etkin Yol Tablosu çıkışına DisableBgpRoutePropagation bayrağı eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2478">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="af695-2479">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="af695-2479">Updated cmdlet:</span></span>
        - <span data-ttu-id="af695-2480">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="af695-2480">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="af695-2481">New-AzApplicationGatewayTrustedRootCertificate belgelerindeki çift tire düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2481">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="af695-2482">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="af695-2482">Az.Resources</span></span>
* <span data-ttu-id="af695-2483">Reddetme atamalarını almak için yeni Get-AzureRmDenyAssignment cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2483">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="af695-2484">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="af695-2484">Az.Sql</span></span>
* <span data-ttu-id="af695-2485">Gelişmiş Tehdit Koruması (Advanced Threat Protection) cmdlet'leri Gelişmiş Veri Güvenliği (Advanced Data Security) olarak yeniden adlandırıldı ve varsayılan olarak Güvenlik Açığı Değerlendirmesi etkinleştiriliyor</span><span class="sxs-lookup"><span data-stu-id="af695-2485">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="af695-2486">2.0.0 - Mayıs 2019</span><span class="sxs-lookup"><span data-stu-id="af695-2486">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="af695-2487">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="af695-2487">Az.Accounts</span></span>
* <span data-ttu-id="af695-2488">Kullanıcı adı/parola kimlik doğrulamasıyla ilişkili ADFS sorunlarını düzeltmek için Authentication Library’i güncelleştirin</span><span class="sxs-lookup"><span data-stu-id="af695-2488">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="af695-2489">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="af695-2489">Az.CognitiveServices</span></span>
* <span data-ttu-id="af695-2490">Yalnızca Bing Arama Hizmetleri için Bing bildirimini görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="af695-2490">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="af695-2491">Hesap oluşturma başarısız olduğunda hata iletisini geliştirin.</span><span class="sxs-lookup"><span data-stu-id="af695-2491">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="af695-2492">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="af695-2492">Az.Compute</span></span>
* <span data-ttu-id="af695-2493">Yakınlık yerleştirme grubu özelliği.</span><span class="sxs-lookup"><span data-stu-id="af695-2493">Proximity placement group feature.</span></span>
    - <span data-ttu-id="af695-2494">Aşağıdaki yeni cmdlet’ler eklendi:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="af695-2494">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="af695-2495">Yeni ProximityPlacementGroupId parametresi aşağıdaki cmdlet'lere eklendi:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="af695-2495">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="af695-2496">StorageAccountType parametresi New-AzGalleryImageVersion öğesine eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-2496">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="af695-2497">New-AzGalleryImageVersion komutunun TargetRegion parametresi StorageAccountType içerebilir.</span><span class="sxs-lookup"><span data-stu-id="af695-2497">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="af695-2498">SkipShutdown anahtar parametresi Stop-AzVM ve Stop-AzVmss öğelerine eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2498">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="af695-2499">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="af695-2499">Breaking changes</span></span>
    - <span data-ttu-id="af695-2500">Set-AzVMBootDiagnostics, Set-AzVMBootDiagnostic olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-2500">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="af695-2501">Export-AzLogAnalyticThrottledRequests, Export-AzLogAnalyticThrottledRequests olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-2501">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="af695-2502">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="af695-2502">Az.DeploymentManager</span></span>
* <span data-ttu-id="af695-2503">Azure Deployment Manager cmdlet’lerinin Genel Kullanıma sunulan ilk sürümü</span><span class="sxs-lookup"><span data-stu-id="af695-2503">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="af695-2504">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="af695-2504">Az.Dns</span></span>
* <span data-ttu-id="af695-2505">Otomatik DNS NameServer Temsilcisi</span><span class="sxs-lookup"><span data-stu-id="af695-2505">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="af695-2506">Create DNS zone cmdlet’i üst bölge adını isteğe bağlı bir ek parametre olarak kabul eder.</span><span class="sxs-lookup"><span data-stu-id="af695-2506">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="af695-2507">Yeni oluşturulan alt bölge için NS kayıtlarını üst bölgeye ekler.</span><span class="sxs-lookup"><span data-stu-id="af695-2507">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="af695-2508">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="af695-2508">Az.FrontDoor</span></span>
* <span data-ttu-id="af695-2509">Azure FrontDoor cmdlet’lerinin Genel Kullanıma Sunulan ilk sürümü</span><span class="sxs-lookup"><span data-stu-id="af695-2509">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="af695-2510">WAF cmdlet'lerini 'Waf' içerecek şekilde yeniden adlandırın</span><span class="sxs-lookup"><span data-stu-id="af695-2510">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="af695-2511">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="af695-2511">Az.HDInsight</span></span>
* <span data-ttu-id="af695-2512">İki cmdlet kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="af695-2512">Removed two cmdlets:</span></span>
    - <span data-ttu-id="af695-2513">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="af695-2513">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="af695-2514">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="af695-2514">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="af695-2515">Grant-AzHDInsightHttpServicesAccess, yeni Set-AzHDInsightGatewayCredential cmdlet’i ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2515">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="af695-2516">Okuyucu rolü ile hdinsight işleç rolünü ayırt etmek için Get-AzHDInsightJobOutput cmdlet’ini güncelleştirin:</span><span class="sxs-lookup"><span data-stu-id="af695-2516">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="af695-2517">Okuyucu rolüne sahip kullanıcıların, 'DefaultStorageAccountKey' parametresini açıkça belirtmesi gerekir, aksi takdirde hata oluşur.</span><span class="sxs-lookup"><span data-stu-id="af695-2517">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="af695-2518">hdinsight işleç rolüne sahip kullanıcılar bu durumdan etkilenmez.</span><span class="sxs-lookup"><span data-stu-id="af695-2518">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="af695-2519">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="af695-2519">Az.Monitor</span></span>
* <span data-ttu-id="af695-2520">SQR API (Zamanlanmış Sorgu Kuralı) için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="af695-2520">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="af695-2521">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="af695-2521">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="af695-2522">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="af695-2522">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="af695-2523">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="af695-2523">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="af695-2524">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="af695-2524">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="af695-2525">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="af695-2525">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="af695-2526">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="af695-2526">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="af695-2527">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="af695-2527">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="af695-2528">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="af695-2528">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="af695-2529">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="af695-2529">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="af695-2530">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="af695-2530">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="af695-2531">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="af695-2531">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="af695-2532">SQR API hakkında [daha fazla](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) bilgi</span><span class="sxs-lookup"><span data-stu-id="af695-2532">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="af695-2533">Az.Monitor.md, GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için cmdlet'leri içerecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2533">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="af695-2534">Az.Network</span><span class="sxs-lookup"><span data-stu-id="af695-2534">Az.Network</span></span>
* <span data-ttu-id="af695-2535">Nat Gateway Resource için destek ekleyin</span><span class="sxs-lookup"><span data-stu-id="af695-2535">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="af695-2536">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="af695-2536">New cmdlets</span></span>
        - <span data-ttu-id="af695-2537">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="af695-2537">New-AzNatGateway</span></span>
        - <span data-ttu-id="af695-2538">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="af695-2538">Get-AzNatGateway</span></span>
        - <span data-ttu-id="af695-2539">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="af695-2539">Set-AzNatGateway</span></span>
        - <span data-ttu-id="af695-2540">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="af695-2540">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="af695-2541">Cmdlet'ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2541">Updated cmdlets</span></span>
        - <span data-ttu-id="af695-2542">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="af695-2542">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="af695-2543">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="af695-2543">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="af695-2544">Özellik için aşağıdaki komutlar güncelleştirildi: Brooklyn Gateway üzerinde özel yollar ayarlama/kaldırma.</span><span class="sxs-lookup"><span data-stu-id="af695-2544">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="af695-2545">New-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-2545">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="af695-2546">Set-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-2546">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="af695-2547">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="af695-2547">Az.PolicyInsights</span></span>
* <span data-ttu-id="af695-2548">İlke değerlendirme ayrıntılarını sorgulama desteği.</span><span class="sxs-lookup"><span data-stu-id="af695-2548">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="af695-2549">Get-AzPolicyState komutuna '-Expand' parametresini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="af695-2549">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="af695-2550">'-Expand PolicyEvaluationDetails' öğesini destekleyin.</span><span class="sxs-lookup"><span data-stu-id="af695-2550">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="af695-2551">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="af695-2551">Az.RecoveryServices</span></span>
* <span data-ttu-id="af695-2552">Abonelikler arası Azure'dan Azure’a konum kurtarma desteği.</span><span class="sxs-lookup"><span data-stu-id="af695-2552">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="af695-2553">Azure Site Recovery için yaklaşan hataya neden olan değişiklikleri işaretleme.</span><span class="sxs-lookup"><span data-stu-id="af695-2553">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="af695-2554">Azure Site Recovery kurtarma planı ve eylem planı için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="af695-2554">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="af695-2555">Azure'dan Azure'a Azure Site Recovery Güncelleştirmesi ağ eşlemesi için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="af695-2555">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="af695-2556">Yönetilen diske yönelik Azure'dan Azure'a Azure Site Recovery güncelleştirmesi koruma yönü için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="af695-2556">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="af695-2557">Diğer küçük düzeltmeler.</span><span class="sxs-lookup"><span data-stu-id="af695-2557">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="af695-2558">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="af695-2558">Az.Relay</span></span>
* <span data-ttu-id="af695-2559">Müşteriye dönük iletilerdeki yazım hatalarını düzeltin</span><span class="sxs-lookup"><span data-stu-id="af695-2559">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="af695-2560">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="af695-2560">Az.ServiceBus</span></span>
* <span data-ttu-id="af695-2561">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2561">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="af695-2562">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="af695-2562">Az.Storage</span></span>
* <span data-ttu-id="af695-2563">Storage Client Library 10.0.1 sürümüne güncelleştirin (bu SDK’daki tüm nesnelerin 'Microsoft.WindowsAzure.Storage. *' ad alanı, 'Microsoft.Azure.Storage.* ' olarak değiştirilir)</span><span class="sxs-lookup"><span data-stu-id="af695-2563">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage. *' to 'Microsoft.Azure.Storage.* ')</span></span>
* <span data-ttu-id="af695-2564">Yeni 2019-04-01 API sürümünü desteklemek için Microsoft.Azure.Management.Storage 11.0.0 sürümüne güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="af695-2564">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="af695-2565">Depolama hesabı oluştur komutundaki varsayılan 'Storage' Depolama hesabı Türü 'StorageV2' olarak değişir</span><span class="sxs-lookup"><span data-stu-id="af695-2565">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="af695-2566">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="af695-2566">New-AzStorageAccount</span></span>
* <span data-ttu-id="af695-2567">'StandardLRS' öğesinin 'Standard_LRS' olarak değiştirilmesi gibi, '-' ekleyerek Sku.Name Depolama hesabı cmdlet çıkışını giriş SkuName ile hizalanacak şekilde değiştirin</span><span class="sxs-lookup"><span data-stu-id="af695-2567">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="af695-2568">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="af695-2568">New-AzStorageAccount</span></span>
    - <span data-ttu-id="af695-2569">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="af695-2569">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="af695-2570">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="af695-2570">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="af695-2571">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="af695-2571">Az.Websites</span></span>
* <span data-ttu-id="af695-2572">'Kind' özelliği artık Get-AzWebApp tarafından döndürülen PSSite nesneleri için ayarlanır</span><span class="sxs-lookup"><span data-stu-id="af695-2572">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="af695-2573">Get-AzWebApp\*Metrics ve Get-AzAppServicePlanMetrics, kullanım dışı olarak işaretlendi</span><span class="sxs-lookup"><span data-stu-id="af695-2573">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="af695-2574">1.8.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="af695-2574">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="af695-2575">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="af695-2575">Highlights since the last major release</span></span>
* <span data-ttu-id="af695-2576">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="af695-2576">General availability of `Az` module</span></span>
* <span data-ttu-id="af695-2577">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="af695-2577">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="af695-2578">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="af695-2578">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="af695-2579">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2579">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="af695-2580">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2580">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="af695-2581">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2581">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="af695-2582">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="af695-2582">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="af695-2583">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="af695-2583">Az.Accounts</span></span>
* <span data-ttu-id="af695-2584">Mac’te modülleri doğru bir biçimde silmek için Uninstall-AzureRm güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2584">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="af695-2585">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="af695-2585">Az.Batch</span></span>
* <span data-ttu-id="af695-2586">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="af695-2586">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="af695-2587">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="af695-2587">Az.Cdn</span></span>
* <span data-ttu-id="af695-2588">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="af695-2588">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="af695-2589">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="af695-2589">Az.CognitiveServices</span></span>
* <span data-ttu-id="af695-2590">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="af695-2590">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="af695-2591">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="af695-2591">Az.Compute</span></span>
* <span data-ttu-id="af695-2592">Disklerin kaynak kimlikleri kaynak kimliğinde küçük harfli kaynak grubu içerdiğinde oluşan AEM yüklemesiyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2592">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="af695-2593">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="af695-2593">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="af695-2594">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2594">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="af695-2595">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="af695-2595">Az.DataFactory</span></span>
* <span data-ttu-id="af695-2596">Yönetilen tümleştirme çalışma zamanı için Nodecount’ın null olmadığı durumlar için SsisProperties eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-2596">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="af695-2597">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="af695-2597">Az.DataLakeStore</span></span>
* <span data-ttu-id="af695-2598">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="af695-2598">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="af695-2599">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="af695-2599">Az.EventGrid</span></span>
* <span data-ttu-id="af695-2600">Oluşturma/güncelleştirme etkinliği için abonelik cmdlet’lerini kullanmadan önce kaynakların oluşturulmasının gerektiğini belirten yardım metni güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-2600">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="af695-2601">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="af695-2601">Az.EventHub</span></span>
* <span data-ttu-id="af695-2602">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2602">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="af695-2603">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="af695-2603">Az.HDInsight</span></span>
* <span data-ttu-id="af695-2604">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="af695-2604">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="af695-2605">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="af695-2605">Az.IotHub</span></span>
* <span data-ttu-id="af695-2606">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="af695-2606">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="af695-2607">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="af695-2607">Az.KeyVault</span></span>
* <span data-ttu-id="af695-2608">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="af695-2608">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="af695-2609">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2609">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="af695-2610">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="af695-2610">Az.MachineLearning</span></span>
* <span data-ttu-id="af695-2611">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="af695-2611">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="af695-2612">Az.Media</span><span class="sxs-lookup"><span data-stu-id="af695-2612">Az.Media</span></span>
* <span data-ttu-id="af695-2613">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="af695-2613">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="af695-2614">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="af695-2614">Az.Monitor</span></span>
  * <span data-ttu-id="af695-2615">GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="af695-2615">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="af695-2616">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="af695-2616">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="af695-2617">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="af695-2617">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="af695-2618">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="af695-2618">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="af695-2619">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="af695-2619">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="af695-2620">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="af695-2620">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="af695-2621">İzleyici SDK’sı 0.22.0-önizleme sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2621">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="af695-2622">Az.Network</span><span class="sxs-lookup"><span data-stu-id="af695-2622">Az.Network</span></span>
* <span data-ttu-id="af695-2623">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="af695-2623">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="af695-2624">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2624">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="af695-2625">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="af695-2625">Az.NotificationHubs</span></span>
* <span data-ttu-id="af695-2626">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="af695-2626">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="af695-2627">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="af695-2627">Az.OperationalInsights</span></span>
* <span data-ttu-id="af695-2628">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="af695-2628">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="af695-2629">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="af695-2629">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="af695-2630">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="af695-2630">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="af695-2631">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="af695-2631">Az.RecoveryServices</span></span>
* <span data-ttu-id="af695-2632">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="af695-2632">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="af695-2633">Azure VM'de SQL için güncelleştirilmiş tablo biçimi</span><span class="sxs-lookup"><span data-stu-id="af695-2633">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="af695-2634">AzureFileShare’de konumu getirmeye yönelik alternatif yöntem eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2634">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="af695-2635">SchedulePolicy nesnesindeki ScheduleRunDays saat dilimine göre güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2635">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="af695-2636">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="af695-2636">Az.RedisCache</span></span>
* <span data-ttu-id="af695-2637">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="af695-2637">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="af695-2638">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="af695-2638">Az.Resources</span></span>
* <span data-ttu-id="af695-2639">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2639">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="af695-2640">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="af695-2640">Az.Sql</span></span>
* <span data-ttu-id="af695-2641">İzleyici SDK’sının bağımlılığı ortak kod ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2641">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="af695-2642">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="af695-2642">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="af695-2643">Birden fazla sütun sınıflandırma işlemi geliştirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-2643">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="af695-2644">Get-AzSqlServerServiceObjective’den alınan yanıta SKU özellikleri (SKU adı, ailesi, kapasitesi) dahil edildi ve bunlar varsayılan olarak tablo şeklinde biçimlendirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-2644">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="af695-2645">Bölgede önceden var olan bir sunucuya ihtiyaç duymadan, konuma göre Get-AzSqlServerServiceObjective yapabilme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-2645">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="af695-2646">Yönetilen Örnek oluşturmadaki saat dilimi parametresi desteği.</span><span class="sxs-lookup"><span data-stu-id="af695-2646">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="af695-2647">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2647">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="af695-2648">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="af695-2648">Az.Websites</span></span>
* <span data-ttu-id="af695-2649">Set-AzWebApp ve Set-AzWebAppSlot çalıştırılırken etiketlerin kaldırılmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2649">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="af695-2650">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="af695-2650">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="af695-2651">Web siteleri SDK'sı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-2651">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="af695-2652">PSAppServicePlan’den AdminSiteName özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="af695-2652">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="af695-2653">1.7.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="af695-2653">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="af695-2654">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="af695-2654">Highlights since the last major release</span></span>
* <span data-ttu-id="af695-2655">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="af695-2655">General availability of `Az` module</span></span>
* <span data-ttu-id="af695-2656">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="af695-2656">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="af695-2657">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="af695-2657">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="af695-2658">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2658">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="af695-2659">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2659">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="af695-2660">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2660">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="af695-2661">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="af695-2661">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="af695-2662">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="af695-2662">Az.Accounts</span></span>
* <span data-ttu-id="af695-2663">Add-AzEnvironment ve Set-AzEnvironment, AzureAnalysisServicesEndpointResourceId parametresini kabul edecek biçimde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2663">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="af695-2664">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="af695-2664">Az.AnalysisServices</span></span>
* <span data-ttu-id="af695-2665">Veri düzlemi cmdlet’lerinde ServiceClient kullanma ve orijinal kimlik doğrulaması mantığını kaldırma</span><span class="sxs-lookup"><span data-stu-id="af695-2665">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="af695-2666">Hataya neden olan değişikliklerden kaçınmak için Add-AzureASAccount’ı Connect-AzAccount’ın sarmalayıcısı yapma</span><span class="sxs-lookup"><span data-stu-id="af695-2666">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="af695-2667">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="af695-2667">Az.Automation</span></span>
* <span data-ttu-id="af695-2668">Eklemeler için New-AzAutomationSoftwareUpdateConfiguration cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-2668">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="af695-2669">IncludedKbNumber ve IncludedPackageNameMask parametrelerinin artık çalışması bekleniyor.</span><span class="sxs-lookup"><span data-stu-id="af695-2669">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="af695-2670">Azure otomasyonu güncelleştirmesi yönetim dinamik grubu için hata düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="af695-2670">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="af695-2671">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="af695-2671">Az.Compute</span></span>
* <span data-ttu-id="af695-2672">New-AzDiskConfig ve New-AzSnapshotConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2672">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="af695-2673">Diğer kiracıların karakter görüntüleriyle VM oluşturmaya izin verildi.</span><span class="sxs-lookup"><span data-stu-id="af695-2673">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="af695-2674">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="af695-2674">Az.ContainerInstance</span></span>
* <span data-ttu-id="af695-2675">New-AzContainerGroup’un -command parametresinde bağımsız boş değişken ekleyen sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2675">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="af695-2676">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="af695-2676">Az.DataFactory</span></span>
* <span data-ttu-id="af695-2677">ADF .Net SDK’sı 3.0.2 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2677">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="af695-2678">Set-AzDataFactoryV2 cmdlet’i RepoConfiguration ile ilgili ayarların ek parametreleriyle güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-2678">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="af695-2679">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="af695-2679">Az.Resources</span></span>
* <span data-ttu-id="af695-2680">'-ResourceId' veya '-ResourceGroupName', '-Name' ve '-ResourceType' parametreleri sağlanırken ‘Get-AzResource’ için sağlayıcıların işlenmesi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2680">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="af695-2681">‘Test-AzDeployment’ ve ‘Test-AzResourceGroupDeployment’ için hata işleme geliştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2681">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="af695-2682">İşleme hataları dağıtım doğrulamasının dışında tutuldu ve komut çıkışına dahil edildi</span><span class="sxs-lookup"><span data-stu-id="af695-2682">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="af695-2683">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="af695-2683">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="af695-2684">Betik ve iş senaryolarında istemi atlamak için bir dizi dağıtım cmdlet’lerine ‘-IgnoreDynamicParameters’ anahtar parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2684">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="af695-2685">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="af695-2685">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="af695-2686">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="af695-2686">Az.Sql</span></span>
* <span data-ttu-id="af695-2687">Veritabanı Verileri Sınıflandırması Desteği.</span><span class="sxs-lookup"><span data-stu-id="af695-2687">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="af695-2688">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="af695-2688">Az.Storage</span></span>
* <span data-ttu-id="af695-2689">-UseConnectedAccount parametresi ile depolama bağlamı oluştururken ayrıntı hatası raporlama</span><span class="sxs-lookup"><span data-stu-id="af695-2689">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="af695-2690">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="af695-2690">New-AzStorageContext</span></span>
* <span data-ttu-id="af695-2691">Belirtilen depolama hesabının Yönetim düzlemi API’si ile Blob Hizmeti Özellikleri için Yönetim Desteği</span><span class="sxs-lookup"><span data-stu-id="af695-2691">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="af695-2692">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="af695-2692">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="af695-2693">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="af695-2693">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="af695-2694">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="af695-2694">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="af695-2695">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="af695-2695">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="af695-2696">Blob ve dosya karşıya yükleme ve indirme cmdlet’leri için -Asjob desteği</span><span class="sxs-lookup"><span data-stu-id="af695-2696">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="af695-2697">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="af695-2697">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="af695-2698">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="af695-2698">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="af695-2699">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="af695-2699">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="af695-2700">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="af695-2700">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="af695-2701">1.6.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="af695-2701">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="af695-2702">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="af695-2702">Highlights since the last major release</span></span>
* <span data-ttu-id="af695-2703">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="af695-2703">General availability of `Az` module</span></span>
* <span data-ttu-id="af695-2704">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="af695-2704">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="af695-2705">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="af695-2705">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="af695-2706">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2706">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="af695-2707">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2707">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="af695-2708">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2708">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="af695-2709">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="af695-2709">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="af695-2710">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="af695-2710">Az.Automation</span></span>
* <span data-ttu-id="af695-2711">Aşağıdaki yeni özellikleri desteklemek için Azure otomasyonu güncelleştirme yönetimi değişikliği:</span><span class="sxs-lookup"><span data-stu-id="af695-2711">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="af695-2712">Dinamik gruplandırma</span><span class="sxs-lookup"><span data-stu-id="af695-2712">Dynamic grouping</span></span>
    * <span data-ttu-id="af695-2713">Ön-Son betik</span><span class="sxs-lookup"><span data-stu-id="af695-2713">Pre-Post script</span></span>
    * <span data-ttu-id="af695-2714">Yeniden Başlatma Ayarı</span><span class="sxs-lookup"><span data-stu-id="af695-2714">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="af695-2715">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="af695-2715">Az.Compute</span></span>
* <span data-ttu-id="af695-2716">Get-AzVmBootDiagnosticsData içinde yol çözümleme sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="af695-2716">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="af695-2717">İşlem istemci kitaplığı 25.0.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-2717">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="af695-2718">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="af695-2718">Az.KeyVault</span></span>
* <span data-ttu-id="af695-2719">KeyVault cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2719">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="af695-2720">Az.Network</span><span class="sxs-lookup"><span data-stu-id="af695-2720">Az.Network</span></span>
* <span data-ttu-id="af695-2721">Azure Güvenlik Duvarı için Tehdit Bilgileri desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2721">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="af695-2722">Application Gateway Güvenlik Duvarı İlkesi üst düzey kaynağı ve Özel Kurallar eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2722">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="af695-2723">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="af695-2723">Az.RecoveryServices</span></span>
* <span data-ttu-id="af695-2724">Anında RP desteği için Azure VM ilkesine SnapshotRetentionInDays eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2724">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="af695-2725">Kapsayıcı kaydını kaldırmak için kanal desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2725">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="af695-2726">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="af695-2726">Az.Resources</span></span>
* <span data-ttu-id="af695-2727">Get-AzResource ve Get-AzResourceGroup için joker karakter desteği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2727">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="af695-2728">ARM'ye genel çağrı yapılırken kullanılan kimlik bilgileri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2728">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="af695-2729">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="af695-2729">Az.Sql</span></span>
* <span data-ttu-id="af695-2730">Yeni DetectionType'lar eklendiğinde gelecekte kullanılabilmesini sağlamak ve otomatik tamamlamayı da desteklemek için Tehdit Algılama cmdlet'lerinin DetectionType olan parametresi (ExcludeDetectionType) string[] olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-2730">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="af695-2731">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="af695-2731">Az.Storage</span></span>
* <span data-ttu-id="af695-2732">Depolama hesabında Yönetim İlkesini Alma/Ayarlama/Kaldırma desteği</span><span class="sxs-lookup"><span data-stu-id="af695-2732">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="af695-2733">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="af695-2733">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="af695-2734">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="af695-2734">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="af695-2735">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="af695-2735">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="af695-2736">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="af695-2736">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="af695-2737">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="af695-2737">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="af695-2738">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="af695-2738">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="af695-2739">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="af695-2739">Az.Websites</span></span>
* <span data-ttu-id="af695-2740">'New-AzWebApp -IncludeSourceWebAppSlots' kullanarak tüm yuvaların kopyalanmasını kesintiye uğratan ARM şablon hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2740">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="af695-2741">1.5.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="af695-2741">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="af695-2742">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="af695-2742">Az.Accounts</span></span>
* <span data-ttu-id="af695-2743">AutoRest tarafından oluşturulan cmdlet’leri desteklemek için 'Register-AzModule' komutu eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2743">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="af695-2744">Connect-AzAccount örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2744">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="af695-2745">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="af695-2745">Az.Automation</span></span>
* <span data-ttu-id="af695-2746">Birden fazla Azure Otomasyonu cmdlet’inde belirli aylık zamanlamalar alınırken yaşanan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2746">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="af695-2747">Yalnızca ilk 20 düğümü döndüren Get-AzAutomationDscNode düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-2747">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="af695-2748">Artık tüm düğümleri döndürür</span><span class="sxs-lookup"><span data-stu-id="af695-2748">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="af695-2749">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="af695-2749">Az.Cdn</span></span>
* <span data-ttu-id="af695-2750">Özel Etki Alanı Https Etkinleştirmesi/Devre Dışı Bırakması için yeni PowerShell cmdlet’leri eklendi ve eskiler kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="af695-2750">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="af695-2751">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="af695-2751">Az.Compute</span></span>
* <span data-ttu-id="af695-2752">Get cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2752">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="af695-2753">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="af695-2753">Az.DataFactory</span></span>
* <span data-ttu-id="af695-2754">ADF .Net SDK sürümü 3.0.1'e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2754">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="af695-2755">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="af695-2755">Az.LogicApp</span></span>
* <span data-ttu-id="af695-2756">Yalnızca ilk sonuç sayfasını getiren ListWorkflows için düzeltme</span><span class="sxs-lookup"><span data-stu-id="af695-2756">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="af695-2757">Az.Network</span><span class="sxs-lookup"><span data-stu-id="af695-2757">Az.Network</span></span>
* <span data-ttu-id="af695-2758">Network cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2758">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="af695-2759">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="af695-2759">Az.RecoveryServices</span></span>
* <span data-ttu-id="af695-2760">Azure VM desteğine SQL Server eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2760">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="af695-2761">SDK Güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="af695-2761">SDK Update</span></span>
* <span data-ttu-id="af695-2762">Get-ProtectableItem içindeki Removed VMappContainer denetimi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="af695-2762">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="af695-2763">Get-ProtectableItem için Name ve ServerName parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2763">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="af695-2764">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="af695-2764">Az.Resources</span></span>
* <span data-ttu-id="af695-2765">Dağıtım cmdlet’lerine `-TemplateObject` parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2765">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="af695-2766">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="af695-2766">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="af695-2767">`Get-AzResource` sonucu `Set-AzResource` üzerine aktarılırken oluşan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2767">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="af695-2768">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="af695-2768">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="af695-2769">`Set-AzResource` çalıştırılırken JSON veri türü değişikliğine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2769">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="af695-2770">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="af695-2770">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="af695-2771">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="af695-2771">Az.Sql</span></span>
* <span data-ttu-id="af695-2772">AuditingEndpointsCommunicator güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="af695-2772">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="af695-2773">Yeni tanılama ayarları oluşturulurken kenar durumunun davranışı düzeltiliyor.</span><span class="sxs-lookup"><span data-stu-id="af695-2773">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="af695-2774">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="af695-2774">Az.Storage</span></span>
* <span data-ttu-id="af695-2775">Depolama hesabı oluşturulurken Support Kind BlockBlobStorage desteği sağlandı      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="af695-2775">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="af695-2776">1.4.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="af695-2776">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="af695-2777">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="af695-2777">Az.AnalysisServices</span></span>
* <span data-ttu-id="af695-2778">AddAzureASAccount cmdlet'i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="af695-2778">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="af695-2779">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="af695-2779">Az.Automation</span></span>
* <span data-ttu-id="af695-2780">Import-AzAutomationDscNodeConfiguration için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2780">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="af695-2781">Import-AzAutomationDscConfiguration cmdlet'ine yapılandırma adı doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2781">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="af695-2782">Import-AzAutomationDscConfiguration cmdlet'i için hata işleme iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2782">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="af695-2783">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="af695-2783">Az.CognitiveServices</span></span>
* <span data-ttu-id="af695-2784">Kaynağın alt etki alanını belirtmek amacıyla kullanılan New-AzCognitiveServicesAccount için CustomSubdomainName adlı, isteğe bağlı, yeni bir parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-2784">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="af695-2785">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="af695-2785">Az.Compute</span></span>
* <span data-ttu-id="af695-2786">Kimlik parametresi kümeleriyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2786">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="af695-2787">Get-AzVMExtension, Name parametresi sağlanmadığında yüklü tüm uzantıları listeleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2787">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="af695-2788">Update-AzImage cmdlet’ine Tag ve ResourceId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2788">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="af695-2789">Get-AzVmssVM, örnek kimliği olmadan ve InstanceView ile, örnek görünümüne sahip VMSS VM’lerini listeleyebilir.</span><span class="sxs-lookup"><span data-stu-id="af695-2789">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="af695-2790">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="af695-2790">Az.DataLakeStore</span></span>
* <span data-ttu-id="af695-2791">ADL silinmiş öğe listeleme ve geri yükleme cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2791">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="af695-2792">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="af695-2792">Az.EventHub</span></span>
* <span data-ttu-id="af695-2793">EventHub’ın CaptureDescription sınıfında Boş Arşivleri Atlamak için SkipEmptyArchives adlı yeni Boole özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2793">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="af695-2794">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="af695-2794">Az.KeyVault</span></span>
* <span data-ttu-id="af695-2795">Set-AzKeyVaultSecret’daki etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2795">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="af695-2796">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="af695-2796">Az.LogicApp</span></span>
* <span data-ttu-id="af695-2797">Tümleştirme Hesapları için Temel SKU eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2797">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="af695-2798">XSLT 2.0, XSLT 3.0 ve Liquid Eşleşme Türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2798">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="af695-2799">Tümleştirme Hesabı Bütünleştirilmiş Kodları için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="af695-2799">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="af695-2800">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="af695-2800">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="af695-2801">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="af695-2801">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="af695-2802">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="af695-2802">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="af695-2803">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="af695-2803">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="af695-2804">Tümleştirme Hesabı Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="af695-2804">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="af695-2805">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="af695-2805">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="af695-2806">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="af695-2806">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="af695-2807">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="af695-2807">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="af695-2808">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="af695-2808">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="af695-2809">Logic Apps SDK sürüm 4.1.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2809">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="af695-2810">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="af695-2810">Az.Monitor</span></span>
* <span data-ttu-id="af695-2811">Get-AzMetric için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2811">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="af695-2812">Az.Network</span><span class="sxs-lookup"><span data-stu-id="af695-2812">Az.Network</span></span>
* <span data-ttu-id="af695-2813">Add-AzApplicationGatewayCustomError için yardım örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2813">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="af695-2814">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="af695-2814">Az.OperationalInsights</span></span>
* <span data-ttu-id="af695-2815">New ve Get ApplicationInsights veri kaynağı için ek destek sunuldu.</span><span class="sxs-lookup"><span data-stu-id="af695-2815">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="af695-2816">Belirli bir çalışma alanı için belirli ve tüm Get ApplicationInsights veri kaynaklarını desteklemek için yeni ‘ApplicationInsights’ türü eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-2816">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="af695-2817">Belirli Application-Insights kaynak parametrelerine (abonelik kimliği, resourceGroupName ve ad) göre veri kaynağı oluşturmak için New-AzOperationalInsightsApplicationInsightsDataSource cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-2817">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="af695-2818">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="af695-2818">Az.Resources</span></span>
* <span data-ttu-id="af695-2819">[https://github.com/Azure/azure-powershell/issues/8166](https://github.com/Azure/azure-powershell/issues/8166 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2819">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="af695-2820">[https://github.com/Azure/azure-powershell/issues/8235](https://github.com/Azure/azure-powershell/issues/8235 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2820">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="af695-2821">[https://github.com/Azure/azure-powershell/issues/6219](https://github.com/Azure/azure-powershell/issues/6219 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2821">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="af695-2822">KeyCredentials’ın tekrar oluşturmasını engelleyen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2822">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="af695-2823">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="af695-2823">Az.Sql</span></span>
* <span data-ttu-id="af695-2824">SQL DB Hiper Ölçek katmanı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2824">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="af695-2825">Geri yükleme isteğinde gereksiz özellikler ayarlandığı için geri yüklemenin başarısız olmasına yol açan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2825">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="af695-2826">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="af695-2826">Az.Websites</span></span>
* <span data-ttu-id="af695-2827">Get-AzWebAppSlotMetrics örneği düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2827">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="af695-2828">1.3.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="af695-2828">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="af695-2829">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="af695-2829">Az.Accounts</span></span>
* <span data-ttu-id="af695-2830">En son ClientRuntime sürümüne güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="af695-2830">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="af695-2831">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="af695-2831">Az.AnalysisServices</span></span>
<span data-ttu-id="af695-2832">Az.AnalysisServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="af695-2832">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="af695-2833">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="af695-2833">Az.Compute</span></span>
* <span data-ttu-id="af695-2834">AEM uzantısı: UltraSSD ile P60,P70 ve P80 diskleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2834">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="af695-2835">Set-AzVMBootDiagnostics yardım açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2835">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="af695-2836">Update-AzImage için yardım açıklaması ve örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2836">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="af695-2837">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="af695-2837">Az.RecoveryServices</span></span>
<span data-ttu-id="af695-2838">Az.RecoveryServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="af695-2838">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="af695-2839">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="af695-2839">Az.Resources</span></span>
* <span data-ttu-id="af695-2840">Kaynak grupları için etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2840">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="af695-2841">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="af695-2841">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="af695-2842">`Get-AzureRmRoleAssignment` komutunun -ErrorAction'a uymama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2842">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="af695-2843">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="af695-2843">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="af695-2844">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="af695-2844">Az.Sql</span></span>
* <span data-ttu-id="af695-2845">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="af695-2845">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="af695-2846">Azure hesabında oturum açılmamasının SQL cmdlet'leri yürütülürken nullref özel durumuna yol açması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2846">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="af695-2847">Get-AzSqlCapability'de null başvuru özel durumu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2847">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="af695-2848">1.2.1 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="af695-2848">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="af695-2849">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="af695-2849">Az.Accounts</span></span>
* <span data-ttu-id="af695-2850">Kimlik Doğrulaması'nın doğru yayınını içeren sürümü</span><span class="sxs-lookup"><span data-stu-id="af695-2850">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="af695-2851">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="af695-2851">Az.AnalysisServices</span></span>
* <span data-ttu-id="af695-2852">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="af695-2852">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="af695-2853">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="af695-2853">Az.RecoveryServices</span></span>
* <span data-ttu-id="af695-2854">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="af695-2854">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="af695-2855">1.2.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="af695-2855">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="af695-2856">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="af695-2856">Az.Accounts</span></span>
* <span data-ttu-id="af695-2857">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2857">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="af695-2858">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2858">Update incorrect online help URLs</span></span>
* <span data-ttu-id="af695-2859">Uninstall-AzureRm için PC Çekirdeğine uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2859">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="af695-2860">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="af695-2860">Az.Aks</span></span>
* <span data-ttu-id="af695-2861">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2861">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="af695-2862">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="af695-2862">Az.Automation</span></span>
* <span data-ttu-id="af695-2863">Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2863">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="af695-2864">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2864">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="af695-2865">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="af695-2865">Az.Cdn</span></span>
* <span data-ttu-id="af695-2866">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2866">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="af695-2867">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="af695-2867">Az.Compute</span></span>
* <span data-ttu-id="af695-2868">Invoke-AzVMReimage cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2868">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="af695-2869">Set-AzVmss'ye TempDisk parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2869">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="af695-2870">New-AzVM'nin uyarı iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2870">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="af695-2871">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="af695-2871">Az.ContainerRegistry</span></span>
* <span data-ttu-id="af695-2872">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2872">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="af695-2873">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="af695-2873">Az.DataFactory</span></span>
* <span data-ttu-id="af695-2874">ADF .Net SDK sürümü 3.0.0'a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2874">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="af695-2875">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="af695-2875">Az.DataLakeStore</span></span>
* <span data-ttu-id="af695-2876">MSI kullanırken ADLS uç noktasındaki sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2876">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="af695-2877">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="af695-2877">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="af695-2878">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2878">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="af695-2879">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="af695-2879">Az.IotHub</span></span>
* <span data-ttu-id="af695-2880">Add-IotHubRoutingEndpoint cmdlet'ine Kodlama biçimi eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-2880">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="af695-2881">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="af695-2881">Az.KeyVault</span></span>
* <span data-ttu-id="af695-2882">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2882">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="af695-2883">Az.Network</span><span class="sxs-lookup"><span data-stu-id="af695-2883">Az.Network</span></span>
* <span data-ttu-id="af695-2884">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2884">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="af695-2885">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="af695-2885">Az.Resources</span></span>
* <span data-ttu-id="af695-2886">'New-AzADAppCredential' ve 'New-AzADSpCredential' başvuru belgelerindeki hatalı örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2886">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="af695-2887">Kaynak grubu dağıtım cmdlet'lerini yürütmeden önce '-TemplateFile' parametresi yolunun çözülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2887">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="af695-2888">Az.Resources: Belgede New-AzureRmPolicyDefinition -Mode varsayılan değeri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2888">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="af695-2889">Az.Resources: [https://github.com/Azure/azure-powershell/issues/9351](https://github.com/Azure/azure-powershell/issues/7522 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2889">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="af695-2890">Az.Resources: https://github.com/Azure/azure-powershell/issues/5747 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2890">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="af695-2891">'PSResourceGroupDeployment' nesnesinin biçimlendirme sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2891">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="af695-2892">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="af695-2892">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="af695-2893">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="af695-2893">Az.ServiceFabric</span></span>
* <span data-ttu-id="af695-2894">VMSS modeline sertifika eklendiğinde ama özel durum oluştuğunda geri alma için hata düzeltmesi: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="af695-2894">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="af695-2895">Bazı hata iletileri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-2895">Fix some error messages.</span></span>
* <span data-ttu-id="af695-2896">Az geçişinde çalışmayan New-AzServiceFabriCluster için varsayılan ARM şablonuyla küme oluşturma sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-2896">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="af695-2897">Uzantıda küme kimliği denetlenerek küme/uygulama sertifikasının yalnızca kümeye karşılık gelen VM Ölçek Kümelerine eklenmesi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-2897">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="af695-2898">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="af695-2898">Az.SignalR</span></span>
* <span data-ttu-id="af695-2899">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2899">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="af695-2900">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="af695-2900">Az.Sql</span></span>
* <span data-ttu-id="af695-2901">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2901">Update incorrect online help URLs</span></span>
* <span data-ttu-id="af695-2902">LicenseType parametresinin parametre açıklaması olası değerlerle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2902">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="af695-2903">Yönetilen örnek kimliği güncelleştirmesinin, güncelleştirilen tek özellik bu olduğunda çalışmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2903">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="af695-2904">Yönetilen örnekte özel harmanlama desteği</span><span class="sxs-lookup"><span data-stu-id="af695-2904">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="af695-2905">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="af695-2905">Az.Storage</span></span>
* <span data-ttu-id="af695-2906">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2906">Update incorrect online help URLs</span></span>
* <span data-ttu-id="af695-2907">Premium Depolama Hesabı klasik Günlük/Ölçüm desteği sağlamadığından, Premium Depolama Hesabında klasik Günlük/Ölçüm için get/set komutları kullanıldığında ayrıntılı hata iletisi veriliyor.</span><span class="sxs-lookup"><span data-stu-id="af695-2907">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="af695-2908">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="af695-2908">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="af695-2909">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="af695-2909">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="af695-2910">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="af695-2910">Az.TrafficManager</span></span>
* <span data-ttu-id="af695-2911">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2911">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="af695-2912">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="af695-2912">Az.Websites</span></span>
* <span data-ttu-id="af695-2913">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2913">Update incorrect online help URLs</span></span>
* <span data-ttu-id="af695-2914">Uygulama ASE'de barındırılıyorsa, sertifikayı doğru kaynak grubuna ve konuma yüklemek için 'New-AzWebAppSSLBinding' düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-2914">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="af695-2915">SSL sertifikası bir uygulamaya bağlanırken etiketlerin üzerine yazılmaması için 'New-AzWebAppSSLBinding' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2915">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="af695-2916">1.1.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="af695-2916">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="af695-2917">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="af695-2917">Az.Accounts</span></span>
* <span data-ttu-id="af695-2918">Enable-AzureRmAlias cmdlet'ine 'Local' Kapsamı eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2918">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="af695-2919">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="af695-2919">Az.Compute</span></span>
* <span data-ttu-id="af695-2920">Restart/Start/Stop/Remove/Set-AzVM ve Save-AzVMImage için ayarlanan ID parametresinde ad artık isteğe bağlı</span><span class="sxs-lookup"><span data-stu-id="af695-2920">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="af695-2921">Yardım dosyalarında ID parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2921">Updated the description of ID in help files</span></span>
* <span data-ttu-id="af695-2922">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="af695-2922">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="af695-2923">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="af695-2923">Az.DataLakeStore</span></span>
* <span data-ttu-id="af695-2924">SDK düzeltmeleri için veri düzleminin SDK sürümü 1.1.14 olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-2924">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="af695-2925">getfilestatus ve liststatus için negatif acesstime ve modificationtime değerlerini işleme yöntemi düzeltildi, async iptal belirteci düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2925">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="af695-2926">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="af695-2926">Az.EventGrid</span></span>
* <span data-ttu-id="af695-2927">2019-01-01 API sürümünü kullanmak için güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-2927">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="af695-2928">Aşağıdaki cmdlet'ler 2019-01-01 API sürümünde yeni senaryoyu destekleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2928">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="af695-2929">New-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="af695-2929">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="af695-2930">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="af695-2930">Event Time-To-Live,</span></span>
        - <span data-ttu-id="af695-2931">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="af695-2931">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="af695-2932">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="af695-2932">Dead letter endpoint.</span></span>
    - <span data-ttu-id="af695-2933">Update-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="af695-2933">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="af695-2934">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="af695-2934">Event Time-To-Live,</span></span>
        - <span data-ttu-id="af695-2935">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="af695-2935">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="af695-2936">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="af695-2936">Dead letter endpoint.</span></span>
* <span data-ttu-id="af695-2937">New-AzureRmEventGridSubscription ve Update-AzureRmEventGridSubscription cmdlet'lerinde EndpointType seçeneği için yeni enum değerleri (storageQueue ve hybridConnection) eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-2937">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="af695-2938">Olay aboneliğini oluşturma veya güncelleştirme işleminde kullanıcının el ile bir eylem yapması beklendiğinde uyarı iletisi gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="af695-2938">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="af695-2939">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="af695-2939">Az.IotHub</span></span>
* <span data-ttu-id="af695-2940">IotHub SDK'sı en son sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2940">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="af695-2941">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="af695-2941">Az.LogicApp</span></span>
* <span data-ttu-id="af695-2942">Get-AzLogicApp, Name değeri belirtilmemiş olanların tümünü listeliyor</span><span class="sxs-lookup"><span data-stu-id="af695-2942">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="af695-2943">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="af695-2943">Az.Resources</span></span>
* <span data-ttu-id="af695-2944">'Get-AzResource' için '-ODataQuery' ve '-ResourceId' parametreleri sağlanırken ortaya çıkan parametre ayarlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2944">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="af695-2945">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="af695-2945">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="af695-2946">New/Set-AzPolicyDefinition cmdlet'lerinde -Custom parametresinin işlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2946">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="af695-2947">New-AzDeployment belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2947">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="af695-2948">'New-AzADUser' için '-MailNickname' parametresi zorunlu hale getirildi</span><span class="sxs-lookup"><span data-stu-id="af695-2948">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="af695-2949">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="af695-2949">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="af695-2950">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="af695-2950">Az.SignalR</span></span>
* <span data-ttu-id="af695-2951">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="af695-2951">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="af695-2952">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="af695-2952">Az.Sql</span></span>
* <span data-ttu-id="af695-2953">Depolama yönetimi istemci bağımlılığı ortak SDK uygulamasına dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="af695-2953">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="af695-2954">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="af695-2954">Az.Storage</span></span>
* <span data-ttu-id="af695-2955">Sas Token, OAuth veya Anonymous ile oluşturulduğunda Storage bağlamının StorageAccountName değeri gerçek Depolama Hesabı Adına ayarlanıyor</span><span class="sxs-lookup"><span data-stu-id="af695-2955">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="af695-2956">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="af695-2956">New-AzStorageContext</span></span>
* <span data-ttu-id="af695-2957">Blob Anlık Görüntü Nesnesinin Sas Belirteci '-FullUri' parametresiyle oluşturulduğunda, döndürülen Uri anlık görüntü Uri'si olacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2957">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="af695-2958">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="af695-2958">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="af695-2959">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="af695-2959">Az.Websites</span></span>
* <span data-ttu-id="af695-2960">'Get-AzDeletedWebApp' cmdlet'indeki tarih ayrıştırma hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2960">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="af695-2961">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="af695-2961">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="af695-2962">1.0.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="af695-2962">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="af695-2963">Genel</span><span class="sxs-lookup"><span data-stu-id="af695-2963">General</span></span>

- <span data-ttu-id="af695-2964">Az Modülü Genel Kullanıma Sunuldu</span><span class="sxs-lookup"><span data-stu-id="af695-2964">General Availability of Az Module</span></span>
- <span data-ttu-id="af695-2965">Her modül için çevrimiçi yardım</span><span class="sxs-lookup"><span data-stu-id="af695-2965">Online help for each module</span></span>
- <span data-ttu-id="af695-2966">Diğer ayrıntılar ve yol haritası için bkz. [Az Duyuru Sayfası](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="af695-2966">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="af695-2967">AzureRM’den geçiş hakkında bilgi edinmek için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="af695-2967">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="af695-2968">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="af695-2968">Az.Accounts</span></span>
- <span data-ttu-id="af695-2969">Önceki adı: Az.Profile</span><span class="sxs-lookup"><span data-stu-id="af695-2969">Changed from Az.Profile</span></span>
- <span data-ttu-id="af695-2970">Profil ve bağlam türleri için tablo biçimleri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-2970">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="af695-2971">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="af695-2971">Az.ApiManagement</span></span>
- <span data-ttu-id="af695-2972">#7002 düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="af695-2972">Fixes for #7002</span></span>
- <span data-ttu-id="af695-2973">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="af695-2973">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="af695-2974">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="af695-2974">Az.Batch</span></span>
- <span data-ttu-id="af695-2975">`PSComputeNode` üzerinde yeni `NodeAgentInformation` aracılığıyla bir havuzdaki her bir VM’de Azure Batch Düğüm Aracısı’nın hangi sürümünün çalıştığını görme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-2975">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="af695-2976">`PSDataDisk` için `Caching` varsayılan ayarı artık `None` yerine `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="af695-2976">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="af695-2977">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="af695-2977">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="af695-2978">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="af695-2978">Az.Billing</span></span>
- <span data-ttu-id="af695-2979">Billing, Consumption ve UsageAggregates cmdlet’lerini birleştirir, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="af695-2979">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="af695-2980">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="af695-2980">Az.CognitivServices</span></span>
- <span data-ttu-id="af695-2981">New-AzureRmCognitiveServicesAccount işleminde kullanılabilen SkuName ve Typem için tamamlayıcılar eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2981">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="af695-2982">Get-AzCognitiveServicesAccountSkus cmdlet’inden GetSkusWithAccountParamSetName parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="af695-2982">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="af695-2983">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="af695-2983">Az.ContainerInstance</span></span>
- <span data-ttu-id="af695-2984">ManagedIdentity desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2984">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="af695-2985">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="af695-2985">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="af695-2986">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="af695-2986">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="af695-2987">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="af695-2987">Az.DataLakeStore</span></span>
- <span data-ttu-id="af695-2988">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="af695-2988">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="af695-2989">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="af695-2989">Az.Monitor</span></span>
- <span data-ttu-id="af695-2990">Az.Insights cmdlet’inin adı Az.Monitor olarak değiştirildi ve başka yeni değişiklikler yapıldı, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="af695-2990">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="af695-2991">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="af695-2991">Az.KeyVault</span></span>
- <span data-ttu-id="af695-2992">Çıkış türlerinden kullanım dışı 'PurgeDisabled' özelliği kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="af695-2992">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="af695-2993">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="af695-2993">Az.MachineLearning</span></span>
- <span data-ttu-id="af695-2994">Az.MachineLearningCompute modülünden cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2994">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="af695-2995">Az.Media</span><span class="sxs-lookup"><span data-stu-id="af695-2995">Az.Media</span></span>
- <span data-ttu-id="af695-2996">New-AzMediaService cmdlet’inden kullanım dışı -Tags diğer adı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="af695-2996">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="af695-2997">Az.Network</span><span class="sxs-lookup"><span data-stu-id="af695-2997">Az.Network</span></span>
<span data-ttu-id="af695-2998">Application Gateway’de RewriteRuleSets parametresini yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-2998">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="af695-2999">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="af695-2999">New cmdlets added:</span></span>
        - <span data-ttu-id="af695-3000">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="af695-3000">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="af695-3001">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="af695-3001">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="af695-3002">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="af695-3002">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="af695-3003">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="af695-3003">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="af695-3004">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="af695-3004">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="af695-3005">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="af695-3005">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="af695-3006">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="af695-3006">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="af695-3007">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="af695-3007">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="af695-3008">Cmdlet’ler isteğe bağlı -RewriteRuleSet parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-3008">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="af695-3009">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="af695-3009">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="af695-3010">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="af695-3010">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="af695-3011">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="af695-3011">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="af695-3012">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="af695-3012">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="af695-3013">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="af695-3013">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="af695-3014">New-AzureRmApplicationGatewayUrlPathMapConfig, Kimlik kullanarak Application Gateway’e KeyVault Desteği ekledi.</span><span class="sxs-lookup"><span data-stu-id="af695-3014">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="af695-3015">Cmdlet’ler isteğe bağlı -KeyVaultSecretId, -KeyVaultSecret parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-3015">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="af695-3016">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="af695-3016">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="af695-3017">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="af695-3017">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="af695-3018">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="af695-3018">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="af695-3019">New-AzApplicationGateway cmdlet’i isteğe bağlı -UserAssignedIdentity parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-3019">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="af695-3020">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="af695-3020">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="af695-3021">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="af695-3021">Az.OperationalInsights</span></span>
- <span data-ttu-id="af695-3022">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="af695-3022">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="af695-3023">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="af695-3023">Az.Profile</span></span>
- <span data-ttu-id="af695-3024">Modül adı Az.Accounts olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-3024">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="af695-3025">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="af695-3025">Az.RecoveryServices</span></span>
- <span data-ttu-id="af695-3026">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="af695-3026">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="af695-3027">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="af695-3027">Az.Resources</span></span>
- <span data-ttu-id="af695-3028">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="af695-3028">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="af695-3029">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="af695-3029">Az.ServiceFabric</span></span>
- <span data-ttu-id="af695-3030">Sertifikayı ortak ad ve parmak iziyle belirtme desteği</span><span class="sxs-lookup"><span data-stu-id="af695-3030">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="af695-3031">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="af695-3031">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="af695-3032">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="af695-3032">Az.SIgnalR</span></span>
- <span data-ttu-id="af695-3033">SIgnalR için PowerShell cmdlet'leri Genel Kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="af695-3033">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="af695-3034">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="af695-3034">Az.Sql</span></span>
- <span data-ttu-id="af695-3035">Tehdit Algılama cmdlet’lerine yeni Data_Exfiltration ve Unsafe_Action algılama türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-3035">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="af695-3036">Sql Denetimi cmdlet'leri için belge örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-3036">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="af695-3037">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="af695-3037">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="af695-3038">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="af695-3038">Az.Storage</span></span>
- <span data-ttu-id="af695-3039">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="af695-3039">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="af695-3040">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="af695-3040">Az.Websites</span></span>
- <span data-ttu-id="af695-3041">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="af695-3041">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="af695-3042">0.7.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="af695-3042">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="af695-3043">Genel</span><span class="sxs-lookup"><span data-stu-id="af695-3043">General</span></span>

* <span data-ttu-id="af695-3044">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="af695-3044">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="af695-3045">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="af695-3045">Az.Compute</span></span>

* <span data-ttu-id="af695-3046">`New-AzVm(ss)` cmdlet’leri için basit parametre kümelerinde UltraSSD ve Galeri Görüntüleri desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-3046">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="af695-3047">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="af695-3047">Az.DataLakeStore</span></span>

* <span data-ttu-id="af695-3048">Adls hesabı etki alanının sonundaki eğik çizgi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-3048">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="af695-3049">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="af695-3049">Az.FrontDoor</span></span>

* <span data-ttu-id="af695-3050">Bazı bozuk bağlantılar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-3050">Fixed some broken links</span></span>
    - <span data-ttu-id="af695-3051">New-AzureRmFrontDoor ve Set-AzureRmFrontDoor makalelerinde, New-AzureRmFrontDoorHealthProbeSettingObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-3051">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="af695-3052">New-AzureRmFrontDoorManagedRuleObject makalesinde, New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-3052">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="af695-3053">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="af695-3053">Az.RecoveryServices</span></span>

* <span data-ttu-id="af695-3054">Azure Dosya Paylaşımı geri yükleme işlemleri için istemci tarafı doğrulamalar eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-3054">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="af695-3055">Afs geri yükleme işlemi için storageAccountName ve storageAccountResourceGroupName isteğe bağlı hale getirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-3055">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="af695-3056">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="af695-3056">Az.Resources</span></span>

* <span data-ttu-id="af695-3057"> https://github.com/Azure/azure-powershell/issues/7679 düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="af695-3057">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="af695-3058">Get-AzureRmRoleAssignment, klasik yöneticiler istenirken sağlanmışsa abonelik kapsamını kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-3058">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="af695-3059">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="af695-3059">Az.Sql</span></span>

* <span data-ttu-id="af695-3060">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="af695-3060">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="af695-3061">Get-AzureRmSqlDatabaseVulnerabilityAssessment cmdlet’inin DotNet core ile kullanılması konusundaki bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-3061">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="af695-3062">SQL Denetimi cmdlet’leriyle ilgili yardım iletilerinin belgeleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-3062">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="af695-3063">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="af695-3063">Az.Storage</span></span>

* <span data-ttu-id="af695-3064">New-AzureRmStorageAccount cmdlet’ine -EnableHierarchicalNamespace eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-3064">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="af695-3065">-DestContext girilmediğinde Dosya Kopyalama cmdlet’inin hedefte kaynak bağlamını yeniden kullanamamasına yol açan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-3065">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="af695-3066">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="af695-3066">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="af695-3067">Statik Web Sitesi yapılandırması için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-3067">Support Static Website configuration</span></span>
    - <span data-ttu-id="af695-3068">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="af695-3068">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="af695-3069">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="af695-3069">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="af695-3070">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="af695-3070">Az.Websites</span></span>

* <span data-ttu-id="af695-3071">Set-AzureRmWebApp ve Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="af695-3071">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="af695-3072">Windows ve Linux kapsayıcı uygulamalarında bağlanacak Azure Depolama yollarının belirtilmesi için yeni parametre (-AzureStoragePath) eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-3072">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="af695-3073">Azure Depolama yollarını ayarlamak için yeni New-AzureRmWebAppAzureStoragePath cmdlet’inin çıktısını bir parametre olarak kullanın.</span><span class="sxs-lookup"><span data-stu-id="af695-3073">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="af695-3074">0.6.1 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="af695-3074">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="af695-3075">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="af695-3075">Az.ApiManagement</span></span>
* <span data-ttu-id="af695-3076">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="af695-3076">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="af695-3077">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="af695-3077">Az.Automation</span></span>
* <span data-ttu-id="af695-3078">Swagger tabanlı Azure Otomasyon cmdlet'leri</span><span class="sxs-lookup"><span data-stu-id="af695-3078">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="af695-3079">Güncelleştirme Yönetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-3079">Added Update Management cmdlets</span></span>
* <span data-ttu-id="af695-3080">Kaynak Denetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-3080">Added Source Control cmdlets</span></span>
* <span data-ttu-id="af695-3081">Remove-AzureRmAutomationHybridWorkerGroup cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-3081">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="af695-3082">DSC Kayıt Düğümü komutu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-3082">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="af695-3083">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="af695-3083">Az.Compute</span></span>
* <span data-ttu-id="af695-3084">SystemAssigned kimliği için kimlik sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-3084">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="af695-3085">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="af695-3085">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="af695-3086">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="af695-3086">Az.ContainerInstance</span></span>
* <span data-ttu-id="af695-3087">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="af695-3087">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="af695-3088">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="af695-3088">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="af695-3089">Market cmdlet'leri için örnekler açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-3089">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="af695-3090">Az.Network</span><span class="sxs-lookup"><span data-stu-id="af695-3090">Az.Network</span></span>
* <span data-ttu-id="af695-3091">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-3091">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="af695-3092">Desteklenen AzureFirewall Ağ Protokollerine yeniden ICMP eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-3092">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="af695-3093">Test-AzureRmNetworkWatcherConnectivity cmdlet'i güncelleştirildi; hedef kimlik, adres ve bağlantı noktasında doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-3093">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="af695-3094">VirtualNetwork eşlemesinde bellek kullanımıyla ilgili sorunlar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-3094">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="af695-3095">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="af695-3095">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="af695-3096">Korumalı dosya paylaşımı için ilke değiştirme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-3096">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="af695-3097">İlke saat dilimi büyük harfe dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="af695-3097">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="af695-3098">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="af695-3098">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="af695-3099">New-AzureRmRecoveryServicesAsrProtectableItem cmdlet'indeki örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-3099">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="af695-3100">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="af695-3100">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="af695-3101">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="af695-3101">Az.Relay</span></span>
* <span data-ttu-id="af695-3102">Kullanıcının New-AzureRmRelayKey cmdlet'ine KeyValue sağlamasına olanak tanıyan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-3102">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="af695-3103">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="af695-3103">Az.Resources</span></span>
* <span data-ttu-id="af695-3104">`New-AzureRmPolicyAssignment` ve `Set-AzureRmPolicyAssignment` cmdlet'lerindeki kaynak kimliğiyle ilgili parametrelerin yardım belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-3104">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="af695-3105">New-AzureRmPolicyDefinition cmdlet'ine -Metadata kullanan bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-3105">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="af695-3106">NetStandard'da Tag anahtarında büyük/küçük harf kullanımının korunmasına yönelik düzeltme yapıldı: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="af695-3106">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="af695-3107">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="af695-3107">Az.ServiceFabric</span></span>
* <span data-ttu-id="af695-3108">Hataya neden olan değişiklikler yayınlanacağından kullanımdan kaldırılacak özellikleri belirten iletiler eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-3108">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="af695-3109">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="af695-3109">Az.Sql</span></span>
* <span data-ttu-id="af695-3110">Azure Sql Veritabanı Yönetilen Örneği ve Azure Sql Yönetilen Veritabanı'nındaki CRUD işlemleri için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-3110">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="af695-3111">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="af695-3111">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="af695-3112">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="af695-3112">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="af695-3113">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="af695-3113">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="af695-3114">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="af695-3114">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="af695-3115">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="af695-3115">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="af695-3116">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="af695-3116">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="af695-3117">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="af695-3117">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="af695-3118">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="af695-3118">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="af695-3119">Sunucuda veya veritabanında Genişletilmiş Denetim İlkesi yönetimi etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-3119">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="af695-3120">Denetim günlüklerinde filtrelemeyi etkinleştirmek için yeni parametre (PredicateExpression) eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-3120">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="af695-3121">Cmdlet'ler, SQL istemcileri yerine Eski istemcileri kullanacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-3121">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="af695-3122">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="af695-3122">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="af695-3123">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="af695-3123">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="af695-3124">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="af695-3124">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="af695-3125">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="af695-3125">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="af695-3126">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings cmdlet'inin depolama hesabı ad parametre kümesiyle kullanılmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-3126">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="af695-3127">0.5.0 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="af695-3127">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="af695-3128">Genel</span><span class="sxs-lookup"><span data-stu-id="af695-3128">General</span></span>
* <span data-ttu-id="af695-3129">Birçok temel cmdlet’e Kaynak Tamamlayıcıları eklendi - bunlar cmdlet’leri etkileşimli olarak çağırırken mevcut kaynak adları arasında gezinmenize olanak tanır</span><span class="sxs-lookup"><span data-stu-id="af695-3129">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="af695-3130">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="af695-3130">Az.Profile</span></span>
* <span data-ttu-id="af695-3131">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-3131">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="af695-3132">Connect-AzAccount cmdlet'indeki TenantId parametresi Tenant olarak yeniden adlandırıldı ve TenantId için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-3132">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="af695-3133">Connect-AzAccount için TenantId açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-3133">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="af695-3134">Kiracı etki alanı sağlanırken başarısız oturum açma durumunda gösterilen hata iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-3134">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="af695-3135">Kiracıda abonelikleri olmayan hesaplar için bağlam adı çakışmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-3135">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="af695-3136">MSI kullanırken DataLake uç noktalarıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-3136">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="af695-3137">Bağlantı olmadığında 'Disconnect-AzAccount' oluşturulmasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-3137">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="af695-3138">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="af695-3138">Az.CognitiveServices</span></span>
* <span data-ttu-id="af695-3139">Get-AzCognitiveServicesAccountSkus işlemi eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-3139">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="af695-3140">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="af695-3140">Az.Compute</span></span>
* <span data-ttu-id="af695-3141">Add-AzVmssVMDataDisk ve Remove-AzVmssVMDataDisk cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-3141">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="af695-3142">Get-AzVMImage, AutomaticOSUpgradeProperties gösteriyor</span><span class="sxs-lookup"><span data-stu-id="af695-3142">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="af695-3143">SetAzVMChefExtension -BootstrapOptions ve -JsonAttribute seçeneği değerlerinin Json biçiminde ayarlanmamasıyla ilgili hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-3143">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="af695-3144">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="af695-3144">Az.DataLakeStore</span></span>
* <span data-ttu-id="af695-3145">DataLake paketi 1.1.10'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-3145">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="af695-3146">Çok iş parçacıklı işlemlere varsayılan Concurrency değeri eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-3146">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="af695-3147">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="af695-3147">Az.Insights</span></span>
* <span data-ttu-id="af695-3148">7267 numaralı (Otomatik ölçeklendirme alanı) sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-3148">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="af695-3149">Yeni otomatik ölçeklendirme kuralı oluşturma sırasında numaralandırılmış parametrelerin düzgün ayarlanmamasıyla ilgili sorunlar (bunlar her zaman varsayılan değere ayarlanıyordu).</span><span class="sxs-lookup"><span data-stu-id="af695-3149">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="af695-3150">Set-AzDiagnosticSetting'in ayar oluşturma sırasında kategorilerin açıkça belirtilmesini gerektirmesiyle ilgili 7513 numaralı [Insights] sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-3150">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="af695-3151">Artık cmdlet oluşturma sırasında açık kategori gösteriminin etkinleştirilmesini gerektirmiyor; başka bir deyişle belgelerinde belirtildiği gibi çalışıyor</span><span class="sxs-lookup"><span data-stu-id="af695-3151">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="af695-3152">Az.Network</span><span class="sxs-lookup"><span data-stu-id="af695-3152">Az.Network</span></span>
* <span data-ttu-id="af695-3153">Aşağıdaki parametrelerde PeeringType parametresi zorunlu parametre olarak değiştirildi:-</span><span class="sxs-lookup"><span data-stu-id="af695-3153">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="af695-3154">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="af695-3154">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="af695-3155">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="af695-3155">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="af695-3156">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="af695-3156">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="af695-3157">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="af695-3157">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="af695-3158">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="af695-3158">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="af695-3159">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="af695-3159">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="af695-3160">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="af695-3160">Az.PolicyInsights</span></span>
* <span data-ttu-id="af695-3161">İlke düzeltme cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-3161">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="af695-3162">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="af695-3162">Az.Resources</span></span>
* <span data-ttu-id="af695-3163"> https://github.com/Azure/azure-powershell/issues/7402 düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="af695-3163">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="af695-3164">'Get-AzResource' için '-ResourceId' parametresi kullanılarak kaynakların listelenmesine olanak tanındı</span><span class="sxs-lookup"><span data-stu-id="af695-3164">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="af695-3165">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="af695-3165">Az.ServiceBus</span></span>
* <span data-ttu-id="af695-3166">PSServiceBusMigrationConfigurationAttributes'e Geçiş durumunun bilinmesine yardımcı olacak salt okunur MigrationState özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-3166">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="af695-3167">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="af695-3167">Az.ServiceFabric</span></span>
* <span data-ttu-id="af695-3168">Linux Vmss'ye sertifika ekleme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-3168">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="af695-3169">'Add-AzServiceFabricClusterCertificate' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-3169">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="af695-3170">Yeni sertifikadan doğru parmak izi kullanıyor (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="af695-3170">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="af695-3171">Özel durum doğru görüntüleniyor (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="af695-3171">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="af695-3172">'Update-AzServiceFabricDurability', Vmss CreateOrUpdate işlemini başlatmadan önce küme yapılandırmasını güncelleştirecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-3172">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="af695-3173">0.4.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="af695-3173">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="af695-3174">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="af695-3174">Az.Profile</span></span>
* <span data-ttu-id="af695-3175">CloudShell’de Get-AzSubscription sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="af695-3175">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="af695-3176">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="af695-3176">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="af695-3177">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="af695-3177">Az.Compute</span></span>
* <span data-ttu-id="af695-3178">'New-AzVm' için basit parametre kümesi kullanıldığında hızlandırılmış ağların açılacağı VM boyutları beyaz listesine yeni boyutlar eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-3178">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="af695-3179">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-3179">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="af695-3180">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="af695-3180">Az.DataLakeStore</span></span>
* <span data-ttu-id="af695-3181">Sanal Ağ Kuralları desteği ekleme</span><span class="sxs-lookup"><span data-stu-id="af695-3181">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="af695-3182">Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store sanal ağ kuralını alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="af695-3182">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="af695-3183">Add-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabına sanal ağ kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="af695-3183">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="af695-3184">Set-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabındaki belirtilen sanal ağ kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="af695-3184">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="af695-3185">Remove-AzDataLakeStoreVirtualNetworkRule: Bir Azure Data Lake Store sanal ağ kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="af695-3185">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="af695-3186">Az.Network</span><span class="sxs-lookup"><span data-stu-id="af695-3186">Az.Network</span></span>
* <span data-ttu-id="af695-3187">Test-AzNetworkWatcherConnectivity cmdlet'i güncelleştirildi, arka uca protokol değerini geçiriyor.</span><span class="sxs-lookup"><span data-stu-id="af695-3187">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="af695-3188">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-3188">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="af695-3189">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="af695-3189">Az.Resources</span></span>
* <span data-ttu-id="af695-3190">Get-AzRoleDefinition cmdlet'inin anlaşılmaz bir özel durum oluşturmasına neden olan hata (varsayılan profilin içinde abonelik olmadığında ve hiçbir kapsam belirtilmediğinde), senaryoya anlamlı bir özel durum eklenerek düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="af695-3190">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="af695-3191">Ayrıca varsayılan parametre kümesi 'RoleDefinitionNameParameterSet' olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="af695-3191">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="af695-3192">0.3.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="af695-3192">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="af695-3193">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="af695-3193">Azure.Storage</span></span>
* <span data-ttu-id="af695-3194">Hedefte meta veri sorunu olduğunda Fix Copy Blob/File meta verileri kopyalamayacak</span><span class="sxs-lookup"><span data-stu-id="af695-3194">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="af695-3195">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="af695-3195">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="af695-3196">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="af695-3196">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="af695-3197">Belirli bir konumunun Depolama kaynağı kullanımını alma desteği ve genel Depolama kayrağı kullanımını almak için uyarı iletisi ekleme kullanımdan kalktı.</span><span class="sxs-lookup"><span data-stu-id="af695-3197">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="af695-3198">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="af695-3198">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="af695-3199">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="af695-3199">Az.CognitiveServices</span></span>
* <span data-ttu-id="af695-3200">Mevcut hesap olmadan Get-AzCognitiveServicesAccountSkus desteği.</span><span class="sxs-lookup"><span data-stu-id="af695-3200">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="af695-3201">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="af695-3201">Az.Compute</span></span>
* <span data-ttu-id="af695-3202">Get-AzVM -ResourceGroupName <rg> gerektiğinde 50'den fazla sonuç döndürecek şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-3202">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="af695-3203">New-AzVmss cmdlet'inin yardımına 'SimpleParameterSet' örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-3203">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="af695-3204">Azure Disk Şifrelemesi ilerleme durumu iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-3204">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="af695-3205">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="af695-3205">Az.DataFactoryV2</span></span>
* <span data-ttu-id="af695-3206">ADF .Net SDK sürümü 2.3.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="af695-3206">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="af695-3207">Az.Network</span><span class="sxs-lookup"><span data-stu-id="af695-3207">Az.Network</span></span>
* <span data-ttu-id="af695-3208">NetworkProfile işlevselliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="af695-3208">Added NetworkProfile functionality.</span></span> <span data-ttu-id="af695-3209">yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-3209">new cmdlets added</span></span>
    - <span data-ttu-id="af695-3210">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="af695-3210">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="af695-3211">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="af695-3211">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="af695-3212">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="af695-3212">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="af695-3213">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="af695-3213">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="af695-3214">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="af695-3214">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="af695-3215">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="af695-3215">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="af695-3216">Alt Ağ Modeline hizmet ilişki bağlantısı eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-3216">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="af695-3217">New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-3217">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="af695-3218">Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-3218">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="af695-3219">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="af695-3219">Az.RedisCache</span></span>
* <span data-ttu-id="af695-3220">Bundan sonra Size parametresi olarak her dizeye izin veriliyor.</span><span class="sxs-lookup"><span data-stu-id="af695-3220">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="af695-3221">PSArgumentCompleter açılan listesine P5 eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-3221">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="af695-3222">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="af695-3222">Az.Resources</span></span>
* <span data-ttu-id="af695-3223">Set-AzPolicyDefinition'a eksik -Mode parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="af695-3223">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="af695-3224">Origin öğesi User içeren işlemler için Get-AzProviderOperation commandlet hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-3224">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="af695-3225">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="af695-3225">Az.Sql</span></span>
* <span data-ttu-id="af695-3226">Bazı yedekleme cmdlet'lerinin geçerli Azure aboneliğini tanıyamamasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="af695-3226">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="af695-3227">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="af695-3227">Az.Websites</span></span>
* <span data-ttu-id="af695-3228">Yeni Get-AzWebAppContainerContinuousDeploymentUrl Cmdlet'i - Kapsayıcı Sürekli Dağıtım Web Kancası URL'sini alıyor</span><span class="sxs-lookup"><span data-stu-id="af695-3228">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="af695-3229">Yeni New-AzWebAppContainerPSSession ve Enter-WebAppContainerPSSession Cmdlet'leri - Windows kapsayıcı uygulamasında PowerShell uzak oturumunu başlatıyor</span><span class="sxs-lookup"><span data-stu-id="af695-3229">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="af695-3230">0.2.0 - Eylül 2018</span><span class="sxs-lookup"><span data-stu-id="af695-3230">0.2.0 - September 2018</span></span>
 <span data-ttu-id="af695-3231">İlk Yayın</span><span class="sxs-lookup"><span data-stu-id="af695-3231">Initial Release</span></span>
