---
title: Azure PowerShell sürüm notları
description: Azure PowerShell modüllerine yönelik en son güncelleştirmeler hakkında bilgi edinin.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 27073db862b83c5b95f2364355037c1ebd34a3b5
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/06/2020
ms.locfileid: "93407502"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="50143-103">Azure PowerShell sürüm notları</span><span class="sxs-lookup"><span data-stu-id="50143-103">Azure PowerShell release notes</span></span>

## <a name="500---october-2020"></a><span data-ttu-id="50143-104">5.0.0 - Ekim 2020</span><span class="sxs-lookup"><span data-stu-id="50143-104">5.0.0 - October 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="50143-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="50143-105">Az.Accounts</span></span>
* <span data-ttu-id="50143-106">[Yeni Değişiklik] 'Get-AzProfile' ve 'Select-AzProfile' kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="50143-106">[Breaking Change] Removed 'Get-AzProfile' and 'Select-AzProfile'</span></span>
* <span data-ttu-id="50143-107">Azure Directory Authentication Library, Microsoft Authentication Library (MSAL) ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-107">Replaced Azure Directory Authentication Library with Microsoft Authentication Library(MSAL)</span></span>

#### <a name="azaks"></a><span data-ttu-id="50143-108">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="50143-108">Az.Aks</span></span>
* <span data-ttu-id="50143-109">[Yeni Değişiklik] 'New-AzAksCluster' ve 'Set-AzAksCluster' cmdlet’indeki 'ClientIdAndSecret' parametre diğer adı kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50143-109">[Breaking Change] Removed parameter alias 'ClientIdAndSecret' in 'New-AzAksCluster' and 'Set-AzAksCluster'.</span></span>
* <span data-ttu-id="50143-110">[Yeni Değişiklik] 'New-AzAksCluster' cmdlet’indeki 'NodeVmSetType' parametresinin 'AvailabilitySet' varsayılan değeri 'VirtualMachineScaleSets' olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-110">[Breaking Change] Changed the default value of 'NodeVmSetType' in 'New-AzAksCluster' from 'AvailabilitySet' to 'VirtualMachineScaleSets'.</span></span>
* <span data-ttu-id="50143-111">[Yeni Değişiklik] 'New-AzAksCluster' cmdlet’indeki 'NetworkPlugin' parametresinin 'None' varsayılan değeri 'azure' olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-111">[Breaking Change] Changed the default value of 'NetworkPlugin' in 'New-AzAksCluster' from 'None' to 'azure'.</span></span>
* <span data-ttu-id="50143-112">[Yeni Değişiklik] Linux’ta yalnızca bir değeri desteklediğinden 'New-AzAksCluster' cmdlet’indeki 'NodeOsType' parametresi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50143-112">[Breaking Change] Removed parameter 'NodeOsType' in 'New-AzAksCluster' as it supports only one value Linux.</span></span>

#### <a name="azbilling"></a><span data-ttu-id="50143-113">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="50143-113">Az.Billing</span></span>
* <span data-ttu-id="50143-114">'Get-AzBillingAccount' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-114">Added 'Get-AzBillingAccount' cmdlet</span></span>
* <span data-ttu-id="50143-115">'Get-AzBillingProfile' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-115">Added 'Get-AzBillingProfile' cmdlet</span></span>
* <span data-ttu-id="50143-116">'Get-AzInvoiceSection' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-116">Added 'Get-AzInvoiceSection' cmdlet</span></span>
* <span data-ttu-id="50143-117">'Get-AzBillingInvoice' cmdlet’ine yeni parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-117">Added new parameters in 'Get-AzBillingInvoice' cmdlet</span></span>
* <span data-ttu-id="50143-118">Get-AzBillingInvoice cmdlet’inin yanıtından DownloadUrlExpiry, Type ve BillingPeriodNames özellikleri kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="50143-118">Removed properties DownloadUrlExpiry, Type, BillingPeriodNames from the response of Get-AzBillingInvoice cmdlet</span></span>

#### <a name="azcdn"></a><span data-ttu-id="50143-119">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="50143-119">Az.Cdn</span></span>
* <span data-ttu-id="50143-120">Çoklu kaynak ve özel bağlantı işlevini destekleyecek cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-120">Added cmdlets to support multi-origin and private link functionality</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="50143-121">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="50143-121">Az.CognitiveServices</span></span>
* <span data-ttu-id="50143-122">SDK sürümü 7.4.0-preview olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-122">Updated SDK to 7.4.0-preview.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="50143-123">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="50143-123">Az.Compute</span></span>
* <span data-ttu-id="50143-124">'New-AzVm' cmdlet’ine '-VmssId' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-124">Added '-VmssId' parameter to 'New-AzVm'</span></span>
* <span data-ttu-id="50143-125">'New-AzVmss' cmdlet’ine 'PlatformFaultDomainCount' parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-125">Added 'PlatformFaultDomainCount' parameter to the 'New-AzVmss' cmdlet.</span></span>
* <span data-ttu-id="50143-126">Yeni 'Get-AzDiskEncryptionSetAssociatedResource' cmdlet’i</span><span class="sxs-lookup"><span data-stu-id="50143-126">New cmdlet 'Get-AzDiskEncryptionSetAssociatedResource'</span></span>
* <span data-ttu-id="50143-127">New-AzDiskConfig cmdlet’ine isteğe bağlı 'Tier' ve 'LogicalSectorSize' parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-127">Added 'Tier' and 'LogicalSectorSize' optional parameters to the New-AzDiskConfig cmdlet.</span></span> 
* <span data-ttu-id="50143-128">'New-AzDiskUpdateConfig' cmdlet’ine 'Tier', 'MaxSharesCount', 'DiskIOPSReadOnly' ve 'DiskMBpsReadOnly' eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-128">Added 'Tier', 'MaxSharesCount', 'DiskIOPSReadOnly', and 'DiskMBpsReadOnly' optional parameters to the 'New-AzDiskUpdateConfig' cmdlet.</span></span> 

#### <a name="azcontainerregistry"></a><span data-ttu-id="50143-129">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="50143-129">Az.ContainerRegistry</span></span>
* <span data-ttu-id="50143-130">[Yeni Değişiklik] API sürümü 2019-05-01 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-130">[Breaking Change] Updates API version to 2019-05-01</span></span>
* <span data-ttu-id="50143-131">[Yeni Değişiklik] 'New-AzContainerRegistry' cmdlet’inden 'Classic' SKU’su ve 'StorageAccountName' parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="50143-131">[Breaking Change] Removed SKU 'Classic' and parameter 'StorageAccountName' from 'New-AzContainerRegistry'</span></span>
* <span data-ttu-id="50143-132">Yeni cmdlet’ler eklendi: 'Connect-AzContainerRegistry', 'Import-AzContainerRegistry', 'Get-AzContainerRegistryUsage', 'New-AzContainerRegistryNetworkRule', 'Set-AzContainerRegistryNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="50143-132">Added New cmdlets: 'Connect-AzContainerRegistry', 'Import-AzContainerRegistry', 'Get-AzContainerRegistryUsage', 'New-AzContainerRegistryNetworkRule', 'Set-AzContainerRegistryNetworkRule'</span></span>
* <span data-ttu-id="50143-133">'Update-AzContainerRegistry' cmdlet’ine yeni 'NetworkRuleSet' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-133">Added new parameter 'NetworkRuleSet' to 'Update-AzContainerRegistry'</span></span>

#### <a name="azdatabricks"></a><span data-ttu-id="50143-134">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="50143-134">Az.Databricks</span></span>
* <span data-ttu-id="50143-135">`-EncryptionKeyVersion` başarısız olmadan Databricks çalışma alanını güncelleştirmeye neden olabilecek bir hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-135">Fixed a bug that may cause updating databricks workspace without `-EncryptionKeyVersion` to fail.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="50143-136">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="50143-136">Az.DataFactory</span></span>
* <span data-ttu-id="50143-137">ADF .NET SDK’sı 4.12.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-137">Updated ADF .Net SDK version to 4.12.0</span></span>
* <span data-ttu-id="50143-138">ADF şifrelemesi istemci SDK’sı 4.14.7587.7 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-138">Updated ADF encryption client SDK version to 4.14.7587.7</span></span>
* <span data-ttu-id="50143-139">'Stop-AzDataFactoryV2TriggerRun' ve 'Invoke-AzDataFactoryV2TriggerRun' komutları eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-139">Added 'Stop-AzDataFactoryV2TriggerRun' and 'Invoke-AzDataFactoryV2TriggerRun' commands</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="50143-140">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="50143-140">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="50143-141">Üst düzey ARM nesneleri oluşturmak için Location özelliği gerekli kılındı.</span><span class="sxs-lookup"><span data-stu-id="50143-141">Require Location property for creating top level arm objects.</span></span>
        <span data-ttu-id="50143-142">\* `New-AzWvdApplicationGroup` için `ApplicationGroupType` gerekli kılındı.</span><span class="sxs-lookup"><span data-stu-id="50143-142">\* Made `ApplicationGroupType` required for `New-AzWvdApplicationGroup`.</span></span>
        <span data-ttu-id="50143-143">\* `New-AzWvdApplicationGroup` için `HostPoolArmPath` gerekli kılındı.</span><span class="sxs-lookup"><span data-stu-id="50143-143">\* Made `HostPoolArmPath` required for `New-AzWvdApplicationGroup`.</span></span>
        <span data-ttu-id="50143-144">\* `New-AzWvdHostPool` cmdlet’ine `PreferredAppGroupType` eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-144">\* Added `PreferredAppGroupType` for `New-AzWvdHostPool`.</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="50143-145">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="50143-145">Az.Functions</span></span>
* <span data-ttu-id="50143-146">[Yeni Değişiklik] 'IncludeSlot' anahtar parametresi, 'Get-AzFunctionApp' cmdlet’inin parametre kümelerinden biri hariç tümünden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50143-146">[Breaking Change] Removed 'IncludeSlot' switch parameter from all but one parameter set of 'Get-AzFunctionApp'.</span></span> <span data-ttu-id="50143-147">Cmdlet, şimdi '-IncludeSlot' belirtildiğinde sonuçlarda dağıtım yuvalarının alınmasını destekliyor.</span><span class="sxs-lookup"><span data-stu-id="50143-147">The cmdlet now supports retrieving deployment slots in the results when '-IncludeSlot' is specified.</span></span> 
* <span data-ttu-id="50143-148">'New-AzFunctionApp' güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="50143-148">Updated 'New-AzFunctionApp':</span></span>
  - <span data-ttu-id="50143-149">-DisableApplicationInsights, bu seçenek belirtildiğinde hiçbir Application Insights projesi oluşturulmayacak şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-149">Fixed -DisableApplicationInsights so that no application insights project is created when this option is specified.</span></span> <span data-ttu-id="50143-150">[#12728]</span><span class="sxs-lookup"><span data-stu-id="50143-150">[#12728]</span></span>
  - <span data-ttu-id="50143-151">[Yeni Değişiklik] PowerShell 6.2 işlev uygulamaları oluşturma desteği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50143-151">[Breaking Change] Removed support to create PowerShell 6.2 function apps.</span></span>
  - <span data-ttu-id="50143-152">[Yeni Değişiklik] RuntimeVersion parametresi belirtilmediğinde, PowerShell işlev uygulamaları için Windows üzerinde İşlevler sürüm 3’teki varsayılan çalışma zamanı 6.2 sürümünden 7.0 sürümüne yükseltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-152">[Breaking Change] Changed the default runtime version in Functions version 3 on Windows for PowerShell function apps from 6.2 to 7.0 when the RuntimeVersion parameter is not specified.</span></span>
  - <span data-ttu-id="50143-153">[Yeni Değişiklik] RuntimeVersion parametresi belirtilmediğinde, Node işlev uygulamaları için Windows ve Linux üzerinde sürüm 3’teki varsayılan çalışma zamanı 10 sürümünden 12 sürümüne yükseltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-153">[Breaking Change] Changed the default runtime version in Functions version 3 on Windows and Linux for Node function apps from 10 to 12 when the RuntimeVersion parameter is not specified.</span></span>
  - <span data-ttu-id="50143-154">[Yeni Değişiklik] RuntimeVersion parametresi belirtilmediğinde, Python işlev uygulamaları için Linux üzerinde sürüm 3’teki varsayılan çalışma zamanı 3.7 sürümünden 3.8 sürümüne yükseltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-154">[Breaking Change] Changed the default runtime version in Functions version 3 on Linux for Python function apps from 3.7 to 3.8 when the RuntimeVersion parameter is not specified.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="50143-155">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="50143-155">Az.HDInsight</span></span>
 * <span data-ttu-id="50143-156">New-AzHDInsightCluster cmdlet’inde:</span><span class="sxs-lookup"><span data-stu-id="50143-156">For New-AzHDInsightCluster cmdlet:</span></span>
     - <span data-ttu-id="50143-157">'DefaultStorageAccountName' parametresi 'StorageAccountResourceId' ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-157">Replaced parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
     - <span data-ttu-id="50143-158">'DefaultStorageAccountKey' parametresi 'StorageAccountKey' ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-158">Replaced parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
     - <span data-ttu-id="50143-159">'DefaultStorageAccountType' parametresi 'StorageAccountType' ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-159">Replaced parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
     - <span data-ttu-id="50143-160">'PublicNetworkAccessType' parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="50143-160">Removed parameter 'PublicNetworkAccessType'</span></span>
     - <span data-ttu-id="50143-161">'OutboundPublicNetworkAccessType' parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="50143-161">Removed parameter 'OutboundPublicNetworkAccessType'</span></span>
     - <span data-ttu-id="50143-162">Yeni parametreler eklendi: ADLS 2. Nesil’i desteklemek üzere 'StorageFileSystem' ve 'StorageAccountManagedIdentity' eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-162">Added new parameters: 'StorageFileSystem' and 'StorageAccountManagedIdentity' to support ADLSGen2</span></span>
     - <span data-ttu-id="50143-163">HDInsight Kimlik Aracısını desteklemek üzere yeni 'EnableIDBroker' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-163">Added new parameter 'EnableIDBroker' to Support HDInsight ID Broker</span></span>
     - <span data-ttu-id="50143-164">Yeni parametreler eklendi: Kafka REST Proxy’yi desteklemek üzere 'KafkaClientGroupId', 'KafkaClientGroupName' ve 'KafkaManagementNodeSize' eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-164">Added new parameters: 'KafkaClientGroupId', 'KafkaClientGroupName' and 'KafkaManagementNodeSize' to support Kafka Rest Proxy</span></span>
 * <span data-ttu-id="50143-165">New-AzHDInsightClusterConfig cmdlet’inde:</span><span class="sxs-lookup"><span data-stu-id="50143-165">For New-AzHDInsightClusterConfig cmdlet:</span></span>
     - <span data-ttu-id="50143-166">'DefaultStorageAccountName' parametresi 'StorageAccountResourceId' ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-166">Replaced parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
     - <span data-ttu-id="50143-167">'DefaultStorageAccountKey' parametresi 'StorageAccountKey' ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-167">Replaced parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
     - <span data-ttu-id="50143-168">'DefaultStorageAccountType' parametresi 'StorageAccountType' ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-168">Replaced parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
     - <span data-ttu-id="50143-169">'PublicNetworkAccessType' parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="50143-169">Removed parameter 'PublicNetworkAccessType'</span></span>
     - <span data-ttu-id="50143-170">'OutboundPublicNetworkAccessType' parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="50143-170">Removed parameter 'OutboundPublicNetworkAccessType'</span></span>
* <span data-ttu-id="50143-171">Set-AzHDInsightDefaultStorage cmdlet’inde:</span><span class="sxs-lookup"><span data-stu-id="50143-171">For Set-AzHDInsightDefaultStorage cmdlet:</span></span>
    - <span data-ttu-id="50143-172">'StorageAccountName' parametresi 'StorageAccountResourceId' ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-172">Replaced parameter 'StorageAccountName' with 'StorageAccountResourceId'</span></span>
* <span data-ttu-id="50143-173">Add-AzHDInsightSecurityProfile cmdlet’inde:</span><span class="sxs-lookup"><span data-stu-id="50143-173">For Add-AzHDInsightSecurityProfile cmdlet:</span></span>
    - <span data-ttu-id="50143-174">'Domain' parametresi 'DomainResourceId' ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-174">Replaced parameter 'Domain' with 'DomainResourceId'</span></span>
    - <span data-ttu-id="50143-175">'OrganizationalUnitDN' parametresi için zorunlu gereksinim kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="50143-175">Removed the mandatory requirement for parameter 'OrganizationalUnitDN'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="50143-176">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="50143-176">Az.KeyVault</span></span>
* <span data-ttu-id="50143-177">[Yeni Değişiklik] 'New-AzKeyVault' cmdlet’indeki DisableSoftDelete ve 'Update-AzKeyVault' cmdlet’indeki EnableSoftDelete parametreleri kullanımdan kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="50143-177">[Breaking Change] Deprecated parameter DisableSoftDelete in 'New-AzKeyVault' and EnableSoftDelete in 'Update-AzKeyVault'</span></span>
* <span data-ttu-id="50143-178">[Yeni Değişiklik] Doğrudan SecretValue değerinin görüntülenmesini önlemek amacıyla SecretValueText özniteliği kaldırıldı [#12266]</span><span class="sxs-lookup"><span data-stu-id="50143-178">[Breaking Change] Removed attribute SecretValueText to avoid displaying SecretValue directly [#12266]</span></span>
* <span data-ttu-id="50143-179">Şu yeni kaynak türü için destek eklendi: yönetilen HSM</span><span class="sxs-lookup"><span data-stu-id="50143-179">Supported new resource type: managed HSM</span></span>
    - <span data-ttu-id="50143-180">Yönetilen HSM’deki anahtarları çalıştırmaya yönelik, yönetilen HSM ve cmdlet’lerin CRUD’si</span><span class="sxs-lookup"><span data-stu-id="50143-180">CRUD of managed HSM and cmdlets to operate keys on managed HSM</span></span>
    - <span data-ttu-id="50143-181">Tam HSM yedeklemesi/geri yüklemesi, AES anahtarı oluşturma, güvenlik etki alanı yedeklemesi/geri yüklemesi, RBAC</span><span class="sxs-lookup"><span data-stu-id="50143-181">Full HSM backup/restore, AES key creation, security domain backup/restore, RBAC</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="50143-182">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="50143-182">Az.ManagedServices</span></span>
* <span data-ttu-id="50143-183">[Yeni Değişiklik] Parametrelerin adlandırma kuralları ve ilişkili örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-183">[Breaking Change] Updated parameters naming conventions and associated examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="50143-184">Az.Network</span><span class="sxs-lookup"><span data-stu-id="50143-184">Az.Network</span></span>
* <span data-ttu-id="50143-185">[Yeni Değişiklik] 'HostedSubnet' parametresi kaldırıldı ve yerine 'Subnet' eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-185">[Breaking Change] Removed parameter 'HostedSubnet' and added 'Subnet' instead</span></span>
* <span data-ttu-id="50143-186">Sanal Yönlendirici Eş Düğüm Yolları için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-186">Added new cmdlets for Virtual Router Peer Routes</span></span>
    - <span data-ttu-id="50143-187">'Get-AzVirtualRouterPeerLearnedRoute'</span><span class="sxs-lookup"><span data-stu-id="50143-187">'Get-AzVirtualRouterPeerLearnedRoute'</span></span>
    - <span data-ttu-id="50143-188">'Get-AzVirtualRouterPeerAdvertisedRoute'</span><span class="sxs-lookup"><span data-stu-id="50143-188">'Get-AzVirtualRouterPeerAdvertisedRoute'</span></span>
* <span data-ttu-id="50143-189">New-AzFirewall cmdlet'i güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="50143-189">Updated New-AzFirewall cmdlet:</span></span>
    - <span data-ttu-id="50143-190">'-SkuTier' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-190">Added parameter '-SkuTier'</span></span>
    - <span data-ttu-id="50143-191">'-SkuName' parametresi eklendi ve bu parametreye yönelik SKU, Diğer Ad haline getirildi</span><span class="sxs-lookup"><span data-stu-id="50143-191">Added parameter '-SkuName' and made Sku as Alias for this</span></span>
    - <span data-ttu-id="50143-192">'-Sku' parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="50143-192">Removed parameter '-Sku'</span></span>
* <span data-ttu-id="50143-193">[Yeni Değişiklik] 'Start-AzVpnConnectionPacketCapture' ve 'Stop-AzVpnConnectionPacketCapture' cmdlet’lerinde 'Connectionlink' bağımsız değişkeni zorunlu kılındı</span><span class="sxs-lookup"><span data-stu-id="50143-193">[Breaking Change] Made 'Connectionlink' argument mandatory in 'Start-AzVpnConnectionPacketCapture' and 'Stop-AzVpnConnectionPacketCapture'</span></span>
* <span data-ttu-id="50143-194">[Yeni Değişiklik] 'New-AzNetworkWatcherConnectionMonitorEndPointObject', '-Filter' parametresi kaldırılacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-194">[Breaking Change] Updated 'New-AzNetworkWatcherConnectionMonitorEndPointObject' to remove parameter '-Filter'</span></span>
* <span data-ttu-id="50143-195">[Yeni Değişiklik] 'New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject' cmdlet’i 'New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject' ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-195">[Breaking Change] Replaced 'New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject' cmdlet with 'New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject'</span></span>
* <span data-ttu-id="50143-196">'New-AzNetworkWatcherConnectionMonitorEndPointObject' cmdlet’i güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="50143-196">Updated 'New-AzNetworkWatcherConnectionMonitorEndPointObject' cmdlet:</span></span>
    - <span data-ttu-id="50143-197">'-Type' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-197">Added parameter '-Type'</span></span>
    - <span data-ttu-id="50143-198">'-CoverageLevel' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-198">Added parameter '-CoverageLevel'</span></span>
    - <span data-ttu-id="50143-199">'-Scope' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-199">Added parameter '-Scope'</span></span>
* <span data-ttu-id="50143-200">'New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject' cmdlet’i yeni '-DestinationPortBehavior' parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-200">Updated 'New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject' cmdlet with new parameter '-DestinationPortBehavior'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="50143-201">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="50143-201">Az.RecoveryServices</span></span>
* <span data-ttu-id="50143-202">Katkıda bulunan izinleri için İş Yükü Geri Yüklemesi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-202">Fixing Workload Restore for contributor permissions.</span></span>
* <span data-ttu-id="50143-203">Restore-AzRecoveryServicesBackupItem cmdlet’ine yeni parametre kümeleri ve doğrulamalar eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-203">Added new parameter sets and validations for Restore-AzRecoveryServicesBackupItem cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="50143-204">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="50143-204">Az.Resources</span></span>
* <span data-ttu-id="50143-205">Ayrıştırma hataları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-205">Fixed parsing bug</span></span>
* <span data-ttu-id="50143-206">ARM şablonu What-If cmdlet’leri, sonuçlardan önizleme iletisi kaldırılacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-206">Updated ARM template What-If cmdlets to remove preview message from results</span></span>
* <span data-ttu-id="50143-207">'-WhatIf' cmdlet’i daha yüksek bir kapsama ayarlandığında, şablon dağıtım cmdlet’lerinin kilitlenmesiyle ilgili bir sorun düzeltildi [#13038]</span><span class="sxs-lookup"><span data-stu-id="50143-207">Fixed an issue where template deployment cmdlets crash if '-WhatIf' is set at a higher scope [#13038]</span></span>
* <span data-ttu-id="50143-208">Şablon dağıtım cmdlet’lerinin şablon parametrelerindeki büyük/küçük harfi korumamasıyla ilgili bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-208">Fixed an issue where template deployment cmdlets does not preserve case for template parameters</span></span>
* <span data-ttu-id="50143-209">'Export-AzResourceGroup' cmdlet’inde kullanılmak üzere varsayılan API sürümü eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-209">Added a default API version to be used in 'Export-AzResourceGroup' cmdlet</span></span>
* <span data-ttu-id="50143-210">Şablon Belirtimlerine yönelik cmdlet’ler ('Get-AzTemplateSpec', 'Set-AzTemplateSpec', 'New-AzTemplateSpec', 'Remove-AzTemplateSpec', 'Export-AzTemplateSpec') eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-210">Added cmdlets for Template Specs ('Get-AzTemplateSpec', 'Set-AzTemplateSpec', 'New-AzTemplateSpec', 'Remove-AzTemplateSpec', 'Export-AzTemplateSpec')</span></span>
* <span data-ttu-id="50143-211">Mevcut dağıtım cmdlet’lerini kullanarak (yeni -TemplateSpecId parametresi aracılığıyla) Şablon Belirtimlerini dağıtma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-211">Added support for deploying Template Specs using existing deployment cmdlets (via the new -TemplateSpecId parameter)</span></span> 
* <span data-ttu-id="50143-212">'Get-AzResourceGroupDeploymentOperation', SDK’yı kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-212">Updated 'Get-AzResourceGroupDeploymentOperation' to use the SDK.</span></span>
* <span data-ttu-id="50143-213">'\*-AzDeployment' cmdlet’lerinden '-ApiVersion' parametresi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50143-213">Removed '-ApiVersion' parameter from '\*-AzDeployment' cmdlets.</span></span>

#### <a name="azsql"></a><span data-ttu-id="50143-214">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="50143-214">Az.Sql</span></span>
* <span data-ttu-id="50143-215">networkIsolation belirtilmediğinde New-AzSqlDatabaseExport cmdlet’inin başarısız olmasıyla ilgili sorun düzeltildi [#13097]</span><span class="sxs-lookup"><span data-stu-id="50143-215">Fixed issue where New-AzSqlDatabaseExport fails if networkIsolation not specified [#13097]</span></span>
* <span data-ttu-id="50143-216">New-AzSqlDatabaseExport ve New-AzSqlDatabaseImport cmdlet’lerinin sonuç nesnesinde OperationStatusLink parametresini döndürmemesiyle ilgili sorun düzeltildi [#13097]</span><span class="sxs-lookup"><span data-stu-id="50143-216">Fixed issue where New-AzSqlDatabaseExport and New-AzSqlDatabaseImport were not returning OperationStatusLink in the result object [#13097]</span></span>
* <span data-ttu-id="50143-217">Yedekleme Alanı Yedeklilik Uyarıları’ndaki Azure Eşlenmiş Bölgeler URL’si Güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-217">Update Azure Paired Regions URL in Backup Storage Redundancy Warnings</span></span> 

#### <a name="azstorage"></a><span data-ttu-id="50143-218">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="50143-218">Az.Storage</span></span>
* <span data-ttu-id="50143-219">Eski RestorePolicy.LastEnabledTime özelliği kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="50143-219">Removed obsolete property RestorePolicy.LastEnabledTime</span></span>
    - <span data-ttu-id="50143-220">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="50143-220">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="50143-221">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="50143-221">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="50143-222">'Get-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="50143-222">'Get-AzStorageBlobServiceProperty'</span></span>
    - <span data-ttu-id="50143-223">“Update-AzStorageBlobServiceProperty”</span><span class="sxs-lookup"><span data-stu-id="50143-223">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="50143-224">DaysAfterModificationGreaterThan parametresinin türü int yerine int? olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-224">Change Type of DaysAfterModificationGreaterThan from int to int?</span></span>
    - <span data-ttu-id="50143-225">'Set-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="50143-225">'Set-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="50143-226">'Get-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="50143-226">'Get-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="50143-227">'Add-AzStorageAccountManagementPolicyAction'</span><span class="sxs-lookup"><span data-stu-id="50143-227">'Add-AzStorageAccountManagementPolicyAction'</span></span>
    - <span data-ttu-id="50143-228">'New-AzStorageAccountManagementPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="50143-228">'New-AzStorageAccountManagementPolicyRule'</span></span>
* <span data-ttu-id="50143-229">Erişim katmanına sahip dosya paylaşımı oluşturma/güncelleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-229">Supported create/update file share with access tier</span></span>
    - <span data-ttu-id="50143-230">'New-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="50143-230">'New-AzRmStorageShare'</span></span>
    - <span data-ttu-id="50143-231">'Update-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="50143-231">'Update-AzRmStorageShare'</span></span>
* <span data-ttu-id="50143-232">Data Lake 2. Nesil’deki ACL’yi özyinelemeli olarak ayarlama/güncelleştirme/kaldırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-232">Supported set/update/remove Acl recursively on Datalake Gen2 item</span></span> 
    -  <span data-ttu-id="50143-233">'Set-AzDataLakeGen2AclRecursive'</span><span class="sxs-lookup"><span data-stu-id="50143-233">'Set-AzDataLakeGen2AclRecursive'</span></span> 
    -  <span data-ttu-id="50143-234">'Update-AzDataLakeGen2AclRecursive'</span><span class="sxs-lookup"><span data-stu-id="50143-234">'Update-AzDataLakeGen2AclRecursive'</span></span> 
    -  <span data-ttu-id="50143-235">'Remove-AzDataLakeGen2AclRecursive'</span><span class="sxs-lookup"><span data-stu-id="50143-235">'Remove-AzDataLakeGen2AclRecursive'</span></span>
* <span data-ttu-id="50143-236">Yeni x,t iznine sahip Kapsayıcı erişim ilkesi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-236">Supported Container access policy with new permission x,t</span></span>
    -  <span data-ttu-id="50143-237">'New-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="50143-237">'New-AzStorageContainerStoredAccessPolicy'</span></span>
    -  <span data-ttu-id="50143-238">'Set-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="50143-238">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
* <span data-ttu-id="50143-239">Permission alt özelliğinin türü enum’dan String’e değiştirilerek Kapsayıcı erişim ilkesi cmdlet’ini alma/ayarlama işleminin çıkışı değiştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-239">Changed the output of get/set Container access policy cmdlet, by change the child property Permission type from enum to String</span></span>
    -  <span data-ttu-id="50143-240">'Get-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="50143-240">'Get-AzStorageContainerStoredAccessPolicy'</span></span>
    -  <span data-ttu-id="50143-241">'Set-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="50143-241">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
* <span data-ttu-id="50143-242">JSON ile yönetim ilkesi ayarlamayla ilgili örnek betik sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-242">Fixed a sample script issue of set management policy with json</span></span>
    -  <span data-ttu-id="50143-243">'Set-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="50143-243">'Set-AzStorageAccountManagementPolicy'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="50143-244">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="50143-244">Az.Websites</span></span>
* <span data-ttu-id="50143-245">Premium V3 fiyatlandırma katmanı desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-245">Added support for Premium V3 pricing tier</span></span>
* <span data-ttu-id="50143-246">WebSites SDK 3.1.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-246">Updated the WebSites SDK to 3.1.0</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="50143-247">Topluluğumuzdan katkıda bulunanlara teşekkür ederiz</span><span class="sxs-lookup"><span data-stu-id="50143-247">Thanks to our community contributors</span></span>
* <span data-ttu-id="50143-248">@atul-ram, Get-AzDelegation.md güncelleştirildi (#13176)</span><span class="sxs-lookup"><span data-stu-id="50143-248">@atul-ram, Update Get-AzDelegation.md (#13176)</span></span>
* <span data-ttu-id="50143-249">@dineshreddy007, Stack HCI kaydının WAC belirtecini kullanması durumunda doğru atanan Uygulama Rolleri alınıyor.</span><span class="sxs-lookup"><span data-stu-id="50143-249">@dineshreddy007, Get the App Roles assigned correctly in case of Stack HCI registration using WAC token.</span></span> <span data-ttu-id="50143-250">(#13249)</span><span class="sxs-lookup"><span data-stu-id="50143-250">(#13249)</span></span>
* <span data-ttu-id="50143-251">@kongou-ae, New-AzOffice365PolicyProperty.md güncelleştirildi (#13217)</span><span class="sxs-lookup"><span data-stu-id="50143-251">@kongou-ae, Update New-AzOffice365PolicyProperty.md (#13217)</span></span>
* <span data-ttu-id="50143-252">Lohith Chowdary Chilukuri (@Lochiluk), Set-AzApplicationGateway.md güncelleştirildi (#13150)</span><span class="sxs-lookup"><span data-stu-id="50143-252">Lohith Chowdary Chilukuri (@Lochiluk), Update Set-AzApplicationGateway.md (#13150)</span></span>
* <span data-ttu-id="50143-253">Matthew Burleigh (@mburleigh)</span><span class="sxs-lookup"><span data-stu-id="50143-253">Matthew Burleigh (@mburleigh)</span></span>
  * <span data-ttu-id="50143-254">Belgede başvurulan PowerShell cmdlet’lerine bağlantılar eklendi (#13203)</span><span class="sxs-lookup"><span data-stu-id="50143-254">Add links to PowerShell cmdlets referenced in the document (#13203)</span></span>
  * <span data-ttu-id="50143-255">Belgede başvurulan PowerShell cmdlet’lerine bağlantılar eklendi (#13190)</span><span class="sxs-lookup"><span data-stu-id="50143-255">Add links to PowerShell cmdlets referenced in the document (#13190)</span></span>
  * <span data-ttu-id="50143-256">Belgede başvurulan PowerShell cmdlet’lerine bağlantılar eklendi (#13189)</span><span class="sxs-lookup"><span data-stu-id="50143-256">Add links to PowerShell cmdlets referenced in the document (#13189)</span></span>
  * <span data-ttu-id="50143-257">Başvurulan cmdlet’lere bağlantılar eklendi (#13137)</span><span class="sxs-lookup"><span data-stu-id="50143-257">add links to referenced cmdlets (#13137)</span></span>
  * <span data-ttu-id="50143-258">Belgede başvurulan PowerShell cmdlet’lerine bağlantılar eklendi (#13204)</span><span class="sxs-lookup"><span data-stu-id="50143-258">Add links to PowerShell cmdlets referenced in the document (#13204)</span></span>
  * <span data-ttu-id="50143-259">Belgede başvurulan PowerShell cmdlet’lerine bağlantılar eklendi (#13205)</span><span class="sxs-lookup"><span data-stu-id="50143-259">Add links to PowerShell cmdlets referenced in the document (#13205)</span></span>

## <a name="480---october-2020"></a><span data-ttu-id="50143-260">4.8.0 - Ekim 2020</span><span class="sxs-lookup"><span data-stu-id="50143-260">4.8.0 - October 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="50143-261">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="50143-261">Az.Accounts</span></span>
* <span data-ttu-id="50143-262">Ortak kitaplıklardaki DateTime ayrıştırma sorunu düzeltildi [#13045]</span><span class="sxs-lookup"><span data-stu-id="50143-262">Fixed DateTime parse issue in common libraries [#13045]</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="50143-263">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="50143-263">Az.CognitiveServices</span></span>
* <span data-ttu-id="50143-264">'New-AzCognitiveServicesAccountApiProperty' cmdlet'i eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-264">Added 'New-AzCognitiveServicesAccountApiProperty' cmdlet.</span></span>
* <span data-ttu-id="50143-265">'New-AzCognitiveServicesAccount' ve 'Set-AzCognitiveServicesAccount' için 'ApiProperty' parametresi destekleniyor</span><span class="sxs-lookup"><span data-stu-id="50143-265">Supported 'ApiProperty' parameter for 'New-AzCognitiveServicesAccount' and 'Set-AzCognitiveServicesAccount'</span></span>

#### <a name="azcompute"></a><span data-ttu-id="50143-266">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="50143-266">Az.Compute</span></span>
* <span data-ttu-id="50143-267">'Update-ASRRecoveryPlan' cmdlet'indeki sorun Yük Devretme Türleri doldurularak düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-267">Fixed issue in 'Update-ASRRecoveryPlan' by populating FailoverTypes</span></span>
* <span data-ttu-id="50143-268">'Get-AzVmImage' cmdlet'ine isteğe bağlı '-Top' ve '-OrderBy' parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-268">Added the '-Top' and '-OrderBy' optional parameters to the 'Get-AzVmImage' cmdlet.</span></span> 

#### <a name="azdatabricks"></a><span data-ttu-id="50143-269">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="50143-269">Az.Databricks</span></span>
* <span data-ttu-id="50143-270">'Az.Databricks' modülü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="50143-270">General availability of 'Az.Databricks' module</span></span>
* <span data-ttu-id="50143-271">Sanal ağ eşlemesi için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-271">Added support for virtual network peering</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="50143-272">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="50143-272">Az.DataFactory</span></span>
* <span data-ttu-id="50143-273">Çıkış iletilerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-273">Fixed typo in output messages</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="50143-274">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="50143-274">Az.EventHub</span></span>
* <span data-ttu-id="50143-275">'Set-AzEventHubNetworkRuleSet' cmdlet'ine isteğe bağlı 'TrustedServiceAccessEnabled' anahtar parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-275">Added optional switch parameter 'TrustedServiceAccessEnabled' to 'Set-AzEventHubNetworkRuleSet' cmdlet</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="50143-276">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="50143-276">Az.HDInsight</span></span>
* <span data-ttu-id="50143-277">'PublicNetworkAccessType' ve 'OutboundPublicNetworkAccessType' parametrelerini kullanımdan kaldırma planlaması için uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-277">Added warning message for planning to deprecate the parameters 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType'</span></span>
* <span data-ttu-id="50143-278">'DefaultStorageAccountName' parametresini 'StorageAccountResourceId' ile değiştirme planlaması için uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-278">Added warning message for planning to replace the parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
* <span data-ttu-id="50143-279">'DefaultStorageAccountKey' parametresini 'StorageAccountKey' ile değiştirme planlaması için uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-279">Added warning message for planning to replace the parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
* <span data-ttu-id="50143-280">'DefaultStorageAccountType' parametresini 'StorageAccountType' ile değiştirme planlaması için uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-280">Added warning message for planning to replace the parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
* <span data-ttu-id="50143-281">'DefaultStorageContainer' parametresini 'StorageContainer' ile değiştirme planlaması için uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-281">Added warning message for planning to replace the parameter 'DefaultStorageContainer' with 'StorageContainer'</span></span>
* <span data-ttu-id="50143-282">'DefaultStorageRootPath' parametresini 'StorageRootPath' ile değiştirme planlaması için uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-282">Added warning message for planning to replace the parameter 'DefaultStorageRootPath' with 'StorageRootPath'</span></span>

#### <a name="aziothub"></a><span data-ttu-id="50143-283">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="50143-283">Az.IotHub</span></span>
* <span data-ttu-id="50143-284">Cihazların sdk'sı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-284">Updated devices sdk.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="50143-285">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="50143-285">Az.KeyVault</span></span>
* <span data-ttu-id="50143-286">SecretValueText özelliğinin kaldırılacağı ayrıntılı tarih sağlandı</span><span class="sxs-lookup"><span data-stu-id="50143-286">Provided the detailed date of removing property SecretValueText</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="50143-287">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="50143-287">Az.ManagedServices</span></span>
* <span data-ttu-id="50143-288">Yönetilen hizmet atama ve tanım cmdlet’lerine hataya neden olan değişiklik uyarıları güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-288">Updated breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="50143-289">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="50143-289">Az.Monitor</span></span>
* <span data-ttu-id="50143-290">Uyarı iletisinin gizlenememesi hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-290">Fixed the bug that warning message cannot be suppressed.</span></span> <span data-ttu-id="50143-291">[#12889]</span><span class="sxs-lookup"><span data-stu-id="50143-291">[#12889]</span></span>
* <span data-ttu-id="50143-292">Uyarı kuralı ölçütlerinde 'SkipMetricValidation' parametresi destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="50143-292">Supported 'SkipMetricValidation' parameter in alert rule criteria.</span></span> <span data-ttu-id="50143-293">Ölçüm doğrulamasının atlanmasına neden olarak henüz yayılmamış özel bir ölçümle ilgili uyarı kuralı oluşturmaya olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="50143-293">Allows creating an alert rule on a custom metric that isn't yet emitted, by causing the metric validation to be skipped.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="50143-294">Az.Network</span><span class="sxs-lookup"><span data-stu-id="50143-294">Az.Network</span></span>
* <span data-ttu-id="50143-295">VPNSite Kaynağına Office365 İlkesi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-295">Added Office365 Policy to VPNSite Resource</span></span>
    - <span data-ttu-id="50143-296">'New-AzO365PolicyProperty'</span><span class="sxs-lookup"><span data-stu-id="50143-296">'New-AzO365PolicyProperty'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="50143-297">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="50143-297">Az.RecoveryServices</span></span>
* <span data-ttu-id="50143-298">İş yükü yedeklemesi için kapsayıcı adı doğrulaması eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-298">Added container name validation for workload backup.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="50143-299">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="50143-299">Az.RedisCache</span></span>
* <span data-ttu-id="50143-300">Microsoft.Cache RP kaydıyla ilgili izin sorunundan dolayı 'New-AzRedisCache' ve 'Set-AzRedisCache' cmdlet'lerinin başarısız olmaması sağlandı</span><span class="sxs-lookup"><span data-stu-id="50143-300">Made 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets not fail because of permission issue related to registering Microsoft.Cache RP</span></span>

#### <a name="azsql"></a><span data-ttu-id="50143-301">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="50143-301">Az.Sql</span></span>
* <span data-ttu-id="50143-302">Aşağıdakilere BackupStorageRedundancy eklendi:</span><span class="sxs-lookup"><span data-stu-id="50143-302">Added BackupStorageRedundancy to the following:</span></span> 
    - <span data-ttu-id="50143-303">'Restore-AzureRmSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="50143-303">'Restore-AzureRmSqlDatabase'</span></span>
    - <span data-ttu-id="50143-304">'New-AzSqlDatabaseCopy'</span><span class="sxs-lookup"><span data-stu-id="50143-304">'New-AzSqlDatabaseCopy'</span></span>
    - <span data-ttu-id="50143-305">'New-AzSqlDatabaseSecondary'</span><span class="sxs-lookup"><span data-stu-id="50143-305">'New-AzSqlDatabaseSecondary'</span></span>
* <span data-ttu-id="50143-306">Tüm SQL DB başvurularında BackupStorageRedundancy parametresi için büyük/küçük harf duyarlılığı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="50143-306">Removed case sensitivity for BackupStorageRedundancy parameter for all SQL DB references</span></span> 
* <span data-ttu-id="50143-307">BackupStorageRedundancy uyarı iletisi adları güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-307">Updated BackupStorageRedundancy warning message names</span></span>

#### <a name="azstorage"></a><span data-ttu-id="50143-308">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="50143-308">Az.Storage</span></span>
* <span data-ttu-id="50143-309">Depolama hesabının dosya hizmetinde paylaşımı etkinleştirme/devre dışı bırakma/alma geçici silme özellikleri destekleniyor</span><span class="sxs-lookup"><span data-stu-id="50143-309">Supported enable/disable/get share soft delete properties on file Service of a Storage account</span></span>
    - <span data-ttu-id="50143-310">'Update-AzStorageFileServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="50143-310">'Update-AzStorageFileServiceProperty'</span></span>
    - <span data-ttu-id="50143-311">'Get-AzStorageFileServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="50143-311">'Get-AzStorageFileServiceProperty'</span></span>
* <span data-ttu-id="50143-312">Desteklenen liste dosya paylaşımları Depolama hesabının silinmiş olan dosyalarını içeriyor ve Tek dosya paylaşımı kullanımı alınıyor</span><span class="sxs-lookup"><span data-stu-id="50143-312">Supported list file shares include the deleted ones of a Storage account, and Get single file share usage</span></span>
    - <span data-ttu-id="50143-313">'Get-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="50143-313">'Get-AzRmStorageShare'</span></span>
* <span data-ttu-id="50143-314">Silinmiş dosya paylaşımını geri yükleme destekleniyor</span><span class="sxs-lookup"><span data-stu-id="50143-314">Supported restore a deleted file share</span></span>
    - <span data-ttu-id="50143-315">'Restore-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="50143-315">'Restore-AzRmStorageShare'</span></span>
* <span data-ttu-id="50143-316">Blob hizmeti özelliklerini değiştirmeye yönelik cmdlet'ler değiştirildi. Sunucudan ilk özellikler alınmayacak, yalnızca değiştirilen özellikler sunucuya ayarlanacak.</span><span class="sxs-lookup"><span data-stu-id="50143-316">Changed the cmdlets for modify blob service properties, won't get the original properties from server, but only set the modified properties to server.</span></span>
    - <span data-ttu-id="50143-317">'Enable-AzStorageBlobDeleteRetentionPolicy'</span><span class="sxs-lookup"><span data-stu-id="50143-317">'Enable-AzStorageBlobDeleteRetentionPolicy'</span></span>
    - <span data-ttu-id="50143-318">'Disable-AzStorageBlobDeleteRetentionPolicy'</span><span class="sxs-lookup"><span data-stu-id="50143-318">'Disable-AzStorageBlobDeleteRetentionPolicy'</span></span>  
    - <span data-ttu-id="50143-319">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="50143-319">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="50143-320">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="50143-320">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="50143-321">“Update-AzStorageBlobServiceProperty”</span><span class="sxs-lookup"><span data-stu-id="50143-321">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="50143-322">New-AzStorageAccount parametresi -Kind varsayılan değeri için yardım sorunu düzeltildi [#12189]</span><span class="sxs-lookup"><span data-stu-id="50143-322">Fixed help issue for New-AzStorageAccount parameter -Kind default value [#12189]</span></span>
* <span data-ttu-id="50143-323">Blob karşıya yüklemesinde doğru ContentType ayarlama işlemini göstermek için örnek eklenerek sorun düzeltildi [#12989]</span><span class="sxs-lookup"><span data-stu-id="50143-323">Fixed issue by add example to show how to set correct ContentType in blob upload [#12989]</span></span>

## <a name="470---september-2020"></a><span data-ttu-id="50143-324">4.7.0 - Eylül 2020</span><span class="sxs-lookup"><span data-stu-id="50143-324">4.7.0 - September 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="50143-325">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="50143-325">Az.Accounts</span></span>
* <span data-ttu-id="50143-326">Yaklaşan yeni değişiklik iletileri biçimlendirildi</span><span class="sxs-lookup"><span data-stu-id="50143-326">Formatted the upcoming breaking change messages</span></span>
* <span data-ttu-id="50143-327">Azure.Core 1.4.1 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-327">Updated Azure.Core to 1.4.1</span></span>

#### <a name="azaks"></a><span data-ttu-id="50143-328">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="50143-328">Az.Aks</span></span>
* <span data-ttu-id="50143-329">'New-AzAksCluster', 'Set-AzAksCluster' ve 'New-AzAksNodePool' için istemci tarafı parametre doğrulama mantığı eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-329">Added client side parameter validation logic for 'New-AzAksCluster', 'Set-AzAksCluster' and 'New-AzAksNodePool'.</span></span> <span data-ttu-id="50143-330">[#12372]</span><span class="sxs-lookup"><span data-stu-id="50143-330">[#12372]</span></span>
* <span data-ttu-id="50143-331">'New-AzAksCluster' cmdlet’inde eklentilere yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-331">Added support for add-ons in 'New-AzAksCluster'.</span></span> <span data-ttu-id="50143-332">[#11239]</span><span class="sxs-lookup"><span data-stu-id="50143-332">[#11239]</span></span>
* <span data-ttu-id="50143-333">Eklentiler için 'Enable-AzAksAddOn' ve 'Disable-AzAksAddOn' cmdlet’leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-333">Added cmdlets 'Enable-AzAksAddOn' and 'Disable-AzAksAddOn' for add-ons.</span></span> <span data-ttu-id="50143-334">[#11239]</span><span class="sxs-lookup"><span data-stu-id="50143-334">[#11239]</span></span>
* <span data-ttu-id="50143-335">'New-AzAksCluster' için 'GenerateSshKey' parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-335">Added parameter 'GenerateSshKey' for 'New-AzAksCluster'.</span></span> <span data-ttu-id="50143-336">[#12371]</span><span class="sxs-lookup"><span data-stu-id="50143-336">[#12371]</span></span>
* <span data-ttu-id="50143-337">API sürümü 2020-06-01 olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-337">Updated api version to 2020-06-01.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="50143-338">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="50143-338">Az.CognitiveServices</span></span>
* <span data-ttu-id="50143-339">Belirli API’ler için ek yasal koşullar gösterildi.</span><span class="sxs-lookup"><span data-stu-id="50143-339">Showed additional legal terms for certain APIs.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="50143-340">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="50143-340">Az.Compute</span></span>
* <span data-ttu-id="50143-341">'New-AzVmDiskEncryptionSetConfig' için isteğe bağlı '-EncryptionType' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-341">Added the '-EncryptionType' optional parameter to 'New-AzVmDiskEncryptionSetConfig'</span></span>
* <span data-ttu-id="50143-342">Yeni kaynak türü için yeni cmdlet’ler: DiskAccess 'Get-AzDiskAccess', 'New-AzDiskAccess', 'Get-AzDiskAccess'</span><span class="sxs-lookup"><span data-stu-id="50143-342">New cmdlets for new resource type: DiskAccess 'Get-AzDiskAccess', 'New-AzDiskAccess', 'Get-AzDiskAccess'</span></span>
* <span data-ttu-id="50143-343">'New-AzSnapshotConfig' cmdlet’ine isteğe bağlı '-DiskAccessId' ve '-NetworkAccessPolicy' parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-343">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzSnapshotConfig'</span></span>
* <span data-ttu-id="50143-344">'New-AzDiskConfig' cmdlet’ine isteğe bağlı '-DiskAccessId' ve '-NetworkAccessPolicy' parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-344">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzDiskConfig'</span></span>
* <span data-ttu-id="50143-345">VirtualMachine Örnek Görünümüne 'PatchStatus' özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-345">Added 'PatchStatus' property to VirtualMachine Instance View</span></span>
* <span data-ttu-id="50143-346">'Get-AzVm' cmdlet’i '-Status' ile çağrıldığında döndürülen nesne olan 'VMHealth' özelliği, sanal makinenin örnek görünümüne eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-346">Added 'VMHealth' property to the virtual machine's instance view, which is the returned object when 'Get-AzVm' is invoked with '-Status'</span></span>
* <span data-ttu-id="50143-347">'Get-AzVM' ve 'Get-AzVmss' örnek görünümlerine 'AssignedHost' alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-347">Added 'AssignedHost' field to 'Get-AzVM' and 'Get-AzVmss' instance views.</span></span> <span data-ttu-id="50143-348">Alan, sanal makine örneğinin kaynak kimliğini gösterir</span><span class="sxs-lookup"><span data-stu-id="50143-348">The field shows the resource id of the virtual machine instance</span></span>
* <span data-ttu-id="50143-349">'New-AzHostGroup' cmdlet’ine isteğe bağlı '-SupportAutomaticPlacement' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-349">Added optional parameter '-SupportAutomaticPlacement' to 'New-AzHostGroup'</span></span> 
* <span data-ttu-id="50143-350">'New-AzVm' ve 'New-AzVmss' cmdlet’lerine '-HostGroupId' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-350">Added the '-HostGroupId' parameter to 'New-AzVm' and 'New-AzVmss'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="50143-351">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="50143-351">Az.DataFactory</span></span>
* <span data-ttu-id="50143-352">ADF .NET SDK’sı 4.11.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-352">Updated ADF .Net SDK version to 4.11.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="50143-353">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="50143-353">Az.EventHub</span></span>
* <span data-ttu-id="50143-354">Yeni 'New-AzEventHubCluster', 'Set-AzEventHubCluster', 'Get-AzEventHubCluster', 'Remove-AzEventHubCluster', 'Get-AzEventHubClustersAvailableRegions' Cluster cmdlet’leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-354">Added new Cluster cmdlets - 'New-AzEventHubCluster', 'Set-AzEventHubCluster', 'Get-AzEventHubCluster', 'Remove-AzEventHubCluster', 'Get-AzEventHubClustersAvailableRegions'.</span></span>
* <span data-ttu-id="50143-355">#10722 numaralı soruna yönelik aşağıdaki düzeltmeler yapıldı: AuthorizationRule haklarına yalnızca 'Listen' atanabilecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-355">Fixed for issue #10722 : Fix for assigning only 'Listen' to AuthorizationRule rights.</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="50143-356">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="50143-356">Az.Functions</span></span>
* <span data-ttu-id="50143-357">Desteklemeyen bölgelerde v2 İşlevleri oluşturma özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50143-357">Removed the ability to create v2 Functions in regions that do not support it.</span></span>
* <span data-ttu-id="50143-358">PowerShell 6.2 sürümü kullanımdan kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50143-358">Deprecated PowerShell 6.2.</span></span> <span data-ttu-id="50143-359">Kullanıcı PowerShell 6.2 işlev uygulaması oluşturduğunda, bunun yerine PowerShell 7.0 işlev uygulaması oluşturmasını öneren bir uyarı eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-359">Added a warning for when a user creates a PowerShell 6.2 function app that advises them to create a PowerShell 7.0 function app instead.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="50143-360">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="50143-360">Az.HDInsight</span></span>
* <span data-ttu-id="50143-361">Otomatik ölçeklendirme yapılandırmasıyla küme oluşturma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-361">Supported creating cluster with Autoscale configuration</span></span>
    - <span data-ttu-id="50143-362">'New-AzHDInsightCluster' cmdlet’ine yeni 'AutoscaleConfiguration' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-362">Add new parameter 'AutoscaleConfiguration' to the cmdlet 'New-AzHDInsightCluster'</span></span>
* <span data-ttu-id="50143-363">Kümenin Otomatik ölçeklendirme yapılandırmasını çalıştırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-363">Supported operating cluster's Autoscale configuration</span></span>
    - <span data-ttu-id="50143-364">Yeni 'Get-AzHDInsihgtClusterAutoscaleConfiguration' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-364">Add new cmdlet 'Get-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="50143-365">Yeni 'New-AzHDInsihgtClusterAutoscaleConfiguration' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-365">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="50143-366">Yeni 'Set-AzHDInsihgtClusterAutoscaleConfiguration' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-366">Add new cmdlet 'Set-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="50143-367">Yeni 'Remove-AzHDInsihgtClusterAutoscaleConfiguration' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-367">Add new cmdlet 'Remove-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="50143-368">Yeni 'New-AzHDInsihgtClusterAutoscaleScheduleCondition' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-368">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleScheduleCondition'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="50143-369">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="50143-369">Az.KeyVault</span></span>
* <span data-ttu-id="50143-370">RBAC yetkilendirmesi desteği eklendi [#10557]</span><span class="sxs-lookup"><span data-stu-id="50143-370">Added support for RBAC authorization [#10557]</span></span>
* <span data-ttu-id="50143-371">'Set-AzKeyVaultAccessPolicy' cmdlet’indeki hata işleme özelliği iyileştirildi [#4007]</span><span class="sxs-lookup"><span data-stu-id="50143-371">Enhanced error handling in 'Set-AzKeyVaultAccessPolicy' [#4007]</span></span>

#### <a name="azkusto"></a><span data-ttu-id="50143-372">Az.Kusto</span><span class="sxs-lookup"><span data-stu-id="50143-372">Az.Kusto</span></span>
* <span data-ttu-id="50143-373">'Az.Kusto' modülü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="50143-373">General availability of 'Az.Kusto' module</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="50143-374">Az.Network</span><span class="sxs-lookup"><span data-stu-id="50143-374">Az.Network</span></span>
* <span data-ttu-id="50143-375">[Yeni Değişiklik] Aşağıdaki cmdlet’ler, kaynak sanal yönlendiricisini ve sanal merkezi uyumlu hale getirecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-375">[Breaking Change] Updated below cmdlets to align resource virtual router and virtual hub</span></span>
    - <span data-ttu-id="50143-376">'New-AzVirtualRouter':</span><span class="sxs-lookup"><span data-stu-id="50143-376">'New-AzVirtualRouter':</span></span> 
        - <span data-ttu-id="50143-377">IP yapılandırması alt kaynağını desteklemek için -HostedSubnet parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-377">Added -HostedSubnet parameter to support IP configuration child resource</span></span>
        - <span data-ttu-id="50143-378">-HostedGateway ve -HostedGatewayId parametreleri silindi</span><span class="sxs-lookup"><span data-stu-id="50143-378">deleted -HostedGateway and -HostedGatewayId</span></span>
    - <span data-ttu-id="50143-379">'Get-AzVirtualRouter':</span><span class="sxs-lookup"><span data-stu-id="50143-379">'Get-AzVirtualRouter':</span></span>
        - <span data-ttu-id="50143-380">Abonelik düzeyi parametre kümesi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-380">Added subscription level parameter set</span></span>
    - <span data-ttu-id="50143-381">'Remove-AzVirtualRouter'</span><span class="sxs-lookup"><span data-stu-id="50143-381">'Remove-AzVirtualRouter'</span></span>
    - <span data-ttu-id="50143-382">'Add-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="50143-382">'Add-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="50143-383">'Get-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="50143-383">'Get-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="50143-384">'Remove-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="50143-384">'Remove-AzVirtualRouterPeer'</span></span>
* <span data-ttu-id="50143-385">Azure ExpressRoute Bağlantı Noktası için yeni cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-385">Added new cmdlet for Azure Express Route Port</span></span>
    - <span data-ttu-id="50143-386">'New-AzExpressRoutePortLOA'</span><span class="sxs-lookup"><span data-stu-id="50143-386">'New-AzExpressRoutePortLOA'</span></span>
* <span data-ttu-id="50143-387">VirtualNetwork Eşleme Kaynağına RemoteBgpCommunities özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-387">Added RemoteBgpCommunities property to the VirtualNetwork Peering Resource</span></span>
* <span data-ttu-id="50143-388">'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' ve 'New-AzPublicIpPrefix' uyarı iletisi değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-388">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>
* <span data-ttu-id="50143-389">'Get-AzVpnGateway' çıkışına VpnGatewayIpConfigurations eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-389">Added VpnGatewayIpConfigurations to 'Get-AzVpnGateway' output</span></span>
* <span data-ttu-id="50143-390">'Set-AzApplicationGatewaySslCertificate' ile ilgili hata düzeltildi [#9488]</span><span class="sxs-lookup"><span data-stu-id="50143-390">Fixed bug for 'Set-AzApplicationGatewaySslCertificate' [#9488]</span></span>
* <span data-ttu-id="50143-391">'AzureFirewall' öğesine 'AllowActiveFTP' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-391">Added 'AllowActiveFTP' parameter to 'AzureFirewall'</span></span>
* <span data-ttu-id="50143-392">Özellik için aşağıdaki komutlar güncelleştirildi: VirtualWan P2SVpnGateway üzerinde internet güvenliğini ayarlama/kaldırma özelliği etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-392">Updated below commands for feature: Enable internet security set/remove on VirtualWan P2SVpnGateway.</span></span>
- <span data-ttu-id="50143-393">'New-AzP2sVpnGateway' güncelleştirildi: Müşterilerin P2SVpnGateway üzerinde internet güvenliğini etkinleştirmek için true olarak ayarlayacakları, Noktadan siteye istemcilere uygulanacak olan isteğe bağlı 'EnableInternetSecurityFlag' anahtar parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-393">Updated 'New-AzP2sVpnGateway': Added optional switch parameter 'EnableInternetSecurityFlag' for customers to set true to enable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
- <span data-ttu-id="50143-394">'Update-AzP2sVpnGateway' güncelleştirildi: Müşterilerin P2SVpnGateway üzerinde internet güvenliğini etkinleştirip devre dışı bırakmak için true/false olarak ayarlayacakları, Noktadan siteye istemcilere uygulanacak olan isteğe bağlı 'EnableInternetSecurityFlag' veya 'DisableInternetSecurityFlag' anahtar parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-394">Updated 'Update-AzP2sVpnGateway': Added optional switch parameters 'EnableInternetSecurityFlag' or 'DisableInternetSecurityFlag' for customers to set true/false to enable/disable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
* <span data-ttu-id="50143-395">Müşterilerin sorun giderme amacıyla VirtualWan P2SVpnGateway’lerini sıfırlamalarını/yeniden başlatmalarını sağlayan yeni 'Reset-AzP2sVpnGateway' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-395">Added new cmdlet 'Reset-AzP2sVpnGateway' for customers to reset/reboot their VirtualWan P2SVpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="50143-396">Müşterilerin sorun giderme amacıyla VirtualWan VpnGateway’lerini sıfırlamalarını/yeniden başlatmalarını sağlayan yeni 'Reset-AzVpnGateway' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-396">Added new cmdlet 'Reset-AzVpnGateway' for customers to reset/reboot their VirtualWan VpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="50143-397">'Set-AzVirtualNetworkSubnetConfig' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-397">Updated 'Set-AzVirtualNetworkSubnetConfig'</span></span>
    - <span data-ttu-id="50143-398">Parametrelerde açıkça ayarlanmışsa alt ağın NSG ve Yönlendirme Tablosu özelliklerinin null olarak ayarlanması [#1548][#9718]</span><span class="sxs-lookup"><span data-stu-id="50143-398">Set NSG and Route Table properties of subnet to null if explicitly set in parameters [#1548][#9718]</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="50143-399">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="50143-399">Az.RecoveryServices</span></span>
* <span data-ttu-id="50143-400">İş yükü Yedekleme Öğeleri için Silme Durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-400">Fixed the Delete State for workload Backup Items.</span></span>

#### <a name="azresources"></a><span data-ttu-id="50143-401">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="50143-401">Az.Resources</span></span>
* <span data-ttu-id="50143-402">Eksik olan denetim Set-AzRoleAssignment cmdlet’ine eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-402">Added missing check for Set-AzRoleAssignment</span></span>
* <span data-ttu-id="50143-403">'Get-AzResourceGroupDeploymentOperation' cmdlet’inin 'SubscriptionId' parametresine hataya neden olan değişiklik özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-403">Added breaking change attribute to 'SubscriptionId' parameter of 'Get-AzResourceGroupDeploymentOperation'</span></span>
* <span data-ttu-id="50143-404">ARM şablonu What-If cmdlet’leri 'Ignore' kaynak değişiklikleri son olarak gösterilecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-404">Updated ARM template What-If cmdlets to show 'Ignore' resource changes last</span></span>
* <span data-ttu-id="50143-405">Dağıtım cmdlet’lerindeki güvenlik ve dizi parametresi serileştirme sorunları düzeltildi [#12773]</span><span class="sxs-lookup"><span data-stu-id="50143-405">Fixed secure and array parameter serialization issues for deployment cmdlets [#12773]</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="50143-406">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="50143-406">Az.ServiceFabric</span></span>
* <span data-ttu-id="50143-407">Yönetilen kümeler ve düğüm türleri için yeni cmdlet’ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="50143-407">Added new cmdlets for managed clusters and node types:</span></span>
    - <span data-ttu-id="50143-408">'New-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="50143-408">'New-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="50143-409">'Get-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="50143-409">'Get-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="50143-410">'Set-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="50143-410">'Set-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="50143-411">'Remove-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="50143-411">'Remove-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="50143-412">'Add-AzServiceFabricManagedClusterClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="50143-412">'Add-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="50143-413">'Remove-AzServiceFabricManagedClusterClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="50143-413">'Remove-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="50143-414">'New-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="50143-414">'New-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="50143-415">'Get-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="50143-415">'Get-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="50143-416">'Set-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="50143-416">'Set-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="50143-417">'Remove-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="50143-417">'Remove-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="50143-418">'Add-AzServiceFabricManagedNodeTypeVMExtension'</span><span class="sxs-lookup"><span data-stu-id="50143-418">'Add-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="50143-419">'Add-AzServiceFabricManagedNodeTypeVMSecret'</span><span class="sxs-lookup"><span data-stu-id="50143-419">'Add-AzServiceFabricManagedNodeTypeVMSecret'</span></span>
    - <span data-ttu-id="50143-420">'Remove-AzServiceFabricManagedNodeTypeVMExtension'</span><span class="sxs-lookup"><span data-stu-id="50143-420">'Remove-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="50143-421">'Restart-AzServiceFabricManagedNodeTyp'</span><span class="sxs-lookup"><span data-stu-id="50143-421">'Restart-AzServiceFabricManagedNodeTyp'</span></span>
* <span data-ttu-id="50143-422">Service Fabric SDK’sı, geçerli model için Service Fabric kaynak sağlayıcısı 2020-03-01 API sürümünü kullanan 1.2.0 sürümüne, yönetilen kümeler için 2020-01-01-preview sürümüne yükseltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-422">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2020-03-01 for the current model and 2020-01-01-preview for managed clusters.</span></span>

#### <a name="azsql"></a><span data-ttu-id="50143-423">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="50143-423">Az.Sql</span></span>
* <span data-ttu-id="50143-424">'New-AzSqlInstance' ve 'Get-AzSqlInstance' cmdlet’lerine BackupStorageRedundancy eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-424">Added BackupStorageRedundancy to 'New-AzSqlInstance' and 'Get-AzSqlInstance'</span></span>
* <span data-ttu-id="50143-425">'Get-AzSqlServerActiveDirectoryOnlyAuthentication' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-425">Added cmdlet 'Get-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="50143-426">'Enable-AzSqlServerActiveDirectoryOnlyAuthentication' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-426">Added cmdlet 'Enable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="50143-427">'New-AzSqlInstance' cmdlet’ine Force parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-427">Added Force parameter to 'New-AzSqlInstance'</span></span>
* <span data-ttu-id="50143-428">Yönetilen Veritabanı Günlük Yeniden Oynatma hizmetine cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-428">Added cmdlets for Managed Database Log Replay service</span></span>
    - <span data-ttu-id="50143-429">'Start-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="50143-429">'Start-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="50143-430">'Get-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="50143-430">'Get-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="50143-431">'Complete-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="50143-431">'Complete-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="50143-432">'Stop-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="50143-432">'Stop-AzSqlInstanceDatabaseLogReplay'</span></span>
* <span data-ttu-id="50143-433">'Get-AzSqlInstanceActiveDirectoryOnlyAuthentication' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-433">Added cmdlet 'Get-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="50143-434">'Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-434">Added cmdlet 'Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="50143-435">'Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-435">Added cmdlet 'Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="50143-436">Ağ yalıtım işlevselliğini desteklemek için 'New-AzSqlDatabaseImport' ve 'New-AzSqlDatabaseExport' cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-436">Updated cmdlets 'New-AzSqlDatabaseImport' and 'New-AzSqlDatabaseExport' to support network isolation functionality</span></span>
* <span data-ttu-id="50143-437">'New-AzSqlDatabaseImportExisting' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-437">Added cmdlet 'New-AzSqlDatabaseImportExisting'</span></span>
* <span data-ttu-id="50143-438">Database cmdlet’leri yedekleme alanı tür belirtimini destekleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-438">Updated Databases cmdlets to support backup storage type specification</span></span>
* <span data-ttu-id="50143-439">'New-AzSqlDatabase' cmdlet’ine Force parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-439">Added Force parameter to 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="50143-440">'New-AzSqlDatabase' cmdlet’indeki seçili bölgelerde yer alan BackupStorageRedundancy yapılandırmasına yönelik uyarı eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-440">Added warning for BackupStorageRedundancy configuration in select regions in 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="50143-441">Sunucu ve örneğe yönelik ActiveDirectoryOnlyAuthentication cmdlet’leri, ResourceId ve InputObject’i içerek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-441">Updated ActiveDirectoryOnlyAuthentication cmdlets for server and instance to include ResourceId and InputObject</span></span>

#### <a name="azstorage"></a><span data-ttu-id="50143-442">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="50143-442">Az.Storage</span></span>
* <span data-ttu-id="50143-443">Microsoft.Azure.Storage.DataMovement 2.0.0 sürümüne yükseltme sırasında blob karşıya yüklenirken oluşan hata düzeltildi [#12220]</span><span class="sxs-lookup"><span data-stu-id="50143-443">Fixed upload blob fail by upgrade to Microsoft.Azure.Storage.DataMovement 2.0.0 [#12220]</span></span>
* <span data-ttu-id="50143-444">Belirli Bir Noktaya Geri Yükleme Desteği Eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-444">Supported Point In Time Restore</span></span>
    - <span data-ttu-id="50143-445">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="50143-445">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="50143-446">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="50143-446">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="50143-447">'New-AzStorageBlobRangeToRestore'</span><span class="sxs-lookup"><span data-stu-id="50143-447">'New-AzStorageBlobRangeToRestore'</span></span>
    - <span data-ttu-id="50143-448">'Restore-AzStorageBlobRange'</span><span class="sxs-lookup"><span data-stu-id="50143-448">'Restore-AzStorageBlobRange'</span></span>
* <span data-ttu-id="50143-449">get-AzureRMStorageAccount cmdlet’ini -IncludeBlobRestoreStatus parametresiyle çalıştırarak Depolama hesabının blobu geri yükleme durumunu almaya yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-449">Supported get blob restore status of Storage account by run get-AzureRMStorageAccount with parameter -IncludeBlobRestoreStatus</span></span> 
    - <span data-ttu-id="50143-450">'Get-AzureRMStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="50143-450">'Get-AzureRMStorageAccount'</span></span>
* <span data-ttu-id="50143-451">Yaklaşan cmdlet çıkış değişikliği için hataya neden olan değişiklik uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-451">Added breaking change warning message for upcoming cmdlet output change</span></span>
    - <span data-ttu-id="50143-452">'Get-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="50143-452">'Get-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="50143-453">'Set-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="50143-453">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="50143-454">'Set-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="50143-454">'Set-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="50143-455">'Get-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="50143-455">'Get-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="50143-456">'Add-AzStorageAccountManagementPolicyAction'</span><span class="sxs-lookup"><span data-stu-id="50143-456">'Add-AzStorageAccountManagementPolicyAction'</span></span>
    - <span data-ttu-id="50143-457">'New-AzStorageAccountManagementPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="50143-457">'New-AzStorageAccountManagementPolicyRule'</span></span>
* <span data-ttu-id="50143-458">Microsoft.Azure.Cosmos.Table SDK 1.0.8 sürümüne yükseltildi</span><span class="sxs-lookup"><span data-stu-id="50143-458">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.8</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="50143-459">Topluluğumuzdan katkıda bulunanlara teşekkür ederiz</span><span class="sxs-lookup"><span data-stu-id="50143-459">Thanks to our community contributors</span></span>
* <span data-ttu-id="50143-460">Thomas Van Laere (@ThomVanL), Dockerfile-alpine-3.10’u ekledi (#12911)</span><span class="sxs-lookup"><span data-stu-id="50143-460">Thomas Van Laere (@ThomVanL), Add Dockerfile-alpine-3.10 (#12911)</span></span> 
* <span data-ttu-id="50143-461">Lohith Chowdary Chilukuri (@Lochiluk), Remove-AzNetworkInterfaceIpConfig.md dosyasını güncelleştirdi (#12807)</span><span class="sxs-lookup"><span data-stu-id="50143-461">Lohith Chowdary Chilukuri (@Lochiluk), Update Remove-AzNetworkInterfaceIpConfig.md (#12807)</span></span> 
* <span data-ttu-id="50143-462">Roberth Strand (@roberthstrand), Get-AzResourceGroup-New örneği ve temizleme (#12828)</span><span class="sxs-lookup"><span data-stu-id="50143-462">Roberth Strand (@roberthstrand), Get-AzResourceGroup - New example, and cleanup (#12828)</span></span> 
* <span data-ttu-id="50143-463">Ravi Mishra (@inmishrar), Azure Web App çalışma zamanı yığınını DOTNETCORE’a güncelleştirdi (#12833)</span><span class="sxs-lookup"><span data-stu-id="50143-463">Ravi Mishra (@inmishrar), update Azure Web App runtime stack to DOTNETCORE (#12833)</span></span> 
* <span data-ttu-id="50143-464">@jack-education, Set-AzVirtualNetworkSubnetConfig cmdlet’i NSG ve Rota Tablosunu alt ağdan kaldıracak şekilde güncelleştirdi (#12351)</span><span class="sxs-lookup"><span data-stu-id="50143-464">@jack-education, Updated Set-AzVirtualNetworkSubnetConfig to allow NSG and Route Table to be removed from subnet (#12351)</span></span> 
* <span data-ttu-id="50143-465">@hagop-globanet, Add-AzApplicationGatewayCustomError.md dosyasını güncelleştirdi (#12784)</span><span class="sxs-lookup"><span data-stu-id="50143-465">@hagop-globanet, Update Add-AzApplicationGatewayCustomError.md (#12784)</span></span> 
* <span data-ttu-id="50143-466">Joshua Van Daalen (@greenSacrifice)</span><span class="sxs-lookup"><span data-stu-id="50143-466">Joshua Van Daalen (@greenSacrifice)</span></span>
  * <span data-ttu-id="50143-467">Özellikten Özelliğe yazımını güncelleştirdi (#12821)</span><span class="sxs-lookup"><span data-stu-id="50143-467">Update spelling of Property to Property (#12821)</span></span> 
  * <span data-ttu-id="50143-468">New-AzResourceLock.md örneklerini güncelleştirdi (#12806)</span><span class="sxs-lookup"><span data-stu-id="50143-468">Update New-AzResourceLock.md examples (#12806)</span></span>
* <span data-ttu-id="50143-469">Eragon Riddle (@eragonriddle), örnekteki parametre alanı adını düzeltti (#12825)</span><span class="sxs-lookup"><span data-stu-id="50143-469">Eragon Riddle (@eragonriddle), Corrected parameter field name in the example (#12825)</span></span> 
* <span data-ttu-id="50143-470">@rossifumax, New-AzConfigurationAssignment.md dosyasındaki yazım hatasını düzeltti (#12701)</span><span class="sxs-lookup"><span data-stu-id="50143-470">@rossifumax, Fix typo in New-AzConfigurationAssignment.md (#12701)</span></span>

## <a name="461---august-2020"></a><span data-ttu-id="50143-471">4.6.1 - Ağustos 2020</span><span class="sxs-lookup"><span data-stu-id="50143-471">4.6.1 - August 2020</span></span>
#### <a name="azcompute"></a><span data-ttu-id="50143-472">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="50143-472">Az.Compute</span></span>
* <span data-ttu-id="50143-473">False değerinin varsayılan değerini kaldırmak için 'New-AzVm' içindeki '-EncryptionAtHost' parametresine yama uygulandı [#12776]</span><span class="sxs-lookup"><span data-stu-id="50143-473">Patched '-EncryptionAtHost' parameter in 'New-AzVm' to remove default value of false [#12776]</span></span>

## <a name="460---august-2020"></a><span data-ttu-id="50143-474">4.6.0 - Ağustos 2020</span><span class="sxs-lookup"><span data-stu-id="50143-474">4.6.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="50143-475">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="50143-475">Az.Accounts</span></span>
* <span data-ttu-id="50143-476">Bulma uç noktası varsayılan AzureCloud ortamını veya diğer genel ortamları döndürmediğinden tüm genel bulut ortamları yüklendi (#12633)</span><span class="sxs-lookup"><span data-stu-id="50143-476">Loaded all public cloud environments when discovery endpoint doesn't return default AzureCloud or other public environments [#12633]</span></span>
* <span data-ttu-id="50143-477">SubscriptionPolicies, 'Get-AzSubscription' cmdlet’inde kullanıma sunuldu [#12551]</span><span class="sxs-lookup"><span data-stu-id="50143-477">Exposed SubscriptionPolicies in 'Get-AzSubscription' [#12551]</span></span>

#### <a name="azautomation"></a><span data-ttu-id="50143-478">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="50143-478">Az.Automation</span></span>
* <span data-ttu-id="50143-479">Karma Çalışanı Grubu belirtmek için 'Set-AzAutomationWebhook' cmdlet’ine '-RunOn' parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-479">Added '-RunOn' parameters to 'Set-AzAutomationWebhook' to specify a Hybrid Worker Group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="50143-480">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="50143-480">Az.Compute</span></span>
* <span data-ttu-id="50143-481">'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM' ve 'Update-AzVmss' cmdlet’lerine '-EncryptionAtHost' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-481">Added '-EncryptionAtHost' parameter to 'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM', and 'Update-AzVmss'</span></span>
* <span data-ttu-id="50143-482">'Get-AzVM' ve 'Get-AzVmss' cmdlet’lerinin dönüş nesnesine 'SecurityProfile' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-482">Added 'SecurityProfile' to 'Get-AzVM' and 'Get-AzVmss' return object</span></span>
* <span data-ttu-id="50143-483">'-InstanceView' anahtarı 'Get-AzHostGroup' cmdlet’ine isteğe bağlı parametre olarak eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-483">Added '-InstanceView' switch as optional parameter to 'Get-AzHostGroup'</span></span>
* <span data-ttu-id="50143-484">Yeni 'Invoke-AzVmPatchAssessment' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-484">Added new cmdlet 'Invoke-AzVmPatchAssessment'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="50143-485">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="50143-485">Az.DataFactory</span></span>
* <span data-ttu-id="50143-486">PSPipelineRun sınıfındaki eksik özellikler eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-486">Added missing properties to PSPipelineRun class.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="50143-487">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="50143-487">Az.HDInsight</span></span>
* <span data-ttu-id="50143-488">Konakta şifreleme özelliğiyle küme oluşturma desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-488">Supported creating cluster with encryption at host feature.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="50143-489">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="50143-489">Az.KeyVault</span></span>
* <span data-ttu-id="50143-490">Geçici silmeyi devre dışı bırakma planlaması için uyarı iletileri eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-490">Added warning messages for planning to disable soft delete</span></span>
* <span data-ttu-id="50143-491">SecretValueText özniteliğini kaldırma planlaması için uyarı iletileri eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-491">Added warning messages for planning to remove attribute SecretValueText</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="50143-492">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="50143-492">Az.Maintenance</span></span>
* <span data-ttu-id="50143-493">'New-AzMaintenanceConfiguration' cmdlet’ine isteğe bağlı zamanlamayla ilgili alanlar eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-493">Added optional schedule related fields to 'New-AzMaintenanceConfiguration'</span></span>
* <span data-ttu-id="50143-494">'Get-AzMaintenancePublicConfiguration' için yeni cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-494">Added new cmdlet for 'Get-AzMaintenancePublicConfiguration'</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="50143-495">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="50143-495">Az.ManagedServices</span></span>
* <span data-ttu-id="50143-496">Yönetilen hizmet atama ve tanım cmdlet’lerine hataya neden olan değişiklik uyarıları eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-496">Added breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="50143-497">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="50143-497">Az.Monitor</span></span>
* <span data-ttu-id="50143-498">Günlüklerin ve Ölçümlerin ayrılmasını etkinleştirmek için 'Set-AzDiagnosticSetting' cmdlet’indeki parametre kümesi genişletildi [#12482]</span><span class="sxs-lookup"><span data-stu-id="50143-498">Extended the parameter set in 'Set-AzDiagnosticSetting' for separation of Logs and Metrics enablement [#12482]</span></span>
* <span data-ttu-id="50143-499">'Add-AzMetricAlertRuleV2' cmdlet’inde işlem hattından ölçüm uyarısı alınırken oluşan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-499">Fixed bug for 'Add-AzMetricAlertRuleV2' when getting metric alert from pipeline</span></span>

#### <a name="azresources"></a><span data-ttu-id="50143-500">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="50143-500">Az.Resources</span></span>
* <span data-ttu-id="50143-501">'Get-AzPolicyAlias' cmdlet’i, diğer adın Azure İlkesi tarafından değiştirilebilir olup olmadığını belirten bilgiler içerek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-501">Updated 'Get-AzPolicyAlias' response to include information indicating whether the alias is modifiable by Azure Policy.</span></span>
* <span data-ttu-id="50143-502">Yeni 'Set-AzRoleAssignment' cmdlet’i oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="50143-502">Created new cmdlet 'Set-AzRoleAssignment'</span></span>
* <span data-ttu-id="50143-503">Yönetim grubu kapsamındaki ARM şablonu Durum sonuçlarını almak için 'Get-AzDeploymentManagementGroupWhatIfResult' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-503">Added 'Get-AzDeploymentManagementGroupWhatIfResult' for getting ARM template What-If results at management Group scope</span></span>
* <span data-ttu-id="50143-504">Kiracı kapsamındaki ARM şablonu Durum sonuçlarını almaya yönelik yeni 'Get-AzTenantWhatIfResult' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-504">Added 'Get-AzTenantWhatIfResult' new cmdlet for getting ARM template What-If results at tenant scope</span></span>
* <span data-ttu-id="50143-505">'New-AzManagementGroupDeployment' ve 'New-AzTenantDeployment' için '-WhatIf' ve '-Confirm' parametreleri, ARM şablonu Durum sonuçlarını kullanacak şekilde geçersiz kılındı</span><span class="sxs-lookup"><span data-stu-id="50143-505">Overrode '-WhatIf' and '-Confirm' for 'New-AzManagementGroupDeployment' and 'New-AzTenantDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="50143-506">Yeni dağıtım cmdlet’lerindeki '-WhatIf' ve '-Confirm' parametrelerinin davranışları False ile uyumlu olacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-506">Fixed the behaviors of '-WhatIf' and '-Confirm' for new deployment cmdlets so they comply with False and</span></span> 
* <span data-ttu-id="50143-507">'-TemplateObject' ve 'TemplateParameterObject' için serileştirme hatası düzeltildi [#1528] [#6292]</span><span class="sxs-lookup"><span data-stu-id="50143-507">Fixed serialization error for '-TemplateObject' and 'TemplateParameterObject' [#1528] [#6292]</span></span>
* <span data-ttu-id="50143-508">'Get-AzResourceGroupDeploymentOperation' cmdlet’ine, yaklaşan çıkış türü değişikliğine yönelik hataya neden olan değişiklik özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-508">Added breaking change attribute to 'Get-AzResourceGroupDeploymentOperation' for the upcoming output type change</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="50143-509">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="50143-509">Az.SignalR</span></span>
* <span data-ttu-id="50143-510">'Restart-AzSignalR' ve 'Update-AzSignalR' yardım dosyalarındaki hatalar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-510">Fixed 'Restart-AzSignalR' and 'Update-AzSignalR' help files errors</span></span>
* <span data-ttu-id="50143-511">'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream' cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-511">Added cmdlets 'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="50143-512">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="50143-512">Az.Storage</span></span>
* <span data-ttu-id="50143-513">Blob sorgu hızlandırması desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-513">Supported blob query acceleration</span></span>
    -  <span data-ttu-id="50143-514">'Get-AzStorageBlobQueryResult'</span><span class="sxs-lookup"><span data-stu-id="50143-514">'Get-AzStorageBlobQueryResult'</span></span>
    -  <span data-ttu-id="50143-515">'New-AzStorageBlobQueryConfig'</span><span class="sxs-lookup"><span data-stu-id="50143-515">'New-AzStorageBlobQueryConfig'</span></span>
* <span data-ttu-id="50143-516">Yardım dosyası güncelleştirildi, daha fazla açıklama eklendi ve yazım hataları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-516">Updated help file, added more description, and fixed typo</span></span>
    -  <span data-ttu-id="50143-517">“Start-AzStorageBlobCopy”</span><span class="sxs-lookup"><span data-stu-id="50143-517">'Start-AzStorageBlobCopy'</span></span>
    -  <span data-ttu-id="50143-518">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="50143-518">'Get-AzDataLakeGen2Item'</span></span>
* <span data-ttu-id="50143-519">İlgili alt dizin mevcut olmadığında blobu indirme işleminin başarısız olmasıyla ilgili sorun düzeltildi [#12592]</span><span class="sxs-lookup"><span data-stu-id="50143-519">Fixed download blob fail when related sub directory not exist [#12592]</span></span>
    -  <span data-ttu-id="50143-520">“Get-AzStorageBlobContent”</span><span class="sxs-lookup"><span data-stu-id="50143-520">'Get-AzStorageBlobContent'</span></span>
* <span data-ttu-id="50143-521">Depolama hesaplarında Set/Get/Remove Nesne Çoğaltma İlkesi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-521">Supported Set/Get/Remove Object Replication Policy on Storage accounts</span></span>
    - <span data-ttu-id="50143-522">'New-AzStorageObjectReplicationPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="50143-522">'New-AzStorageObjectReplicationPolicyRule'</span></span>
    - <span data-ttu-id="50143-523">'Set-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="50143-523">'Set-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="50143-524">'Get-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="50143-524">'Get-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="50143-525">'Remove-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="50143-525">'Remove-AzStorageObjectReplicationPolicy'</span></span>
* <span data-ttu-id="50143-526">Bir Depolama hesabının Blob Hizmeti üzerinde ChangeFeed’i etkinleştirmeye/devre dışı bırakmaya yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-526">Supported enable/disable ChangeFeed on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="50143-527">“Update-AzStorageBlobServiceProperty”</span><span class="sxs-lookup"><span data-stu-id="50143-527">'Update-AzStorageBlobServiceProperty'</span></span>

## <a name="450---august-2020"></a><span data-ttu-id="50143-528">4.5.0 - Ağustos 2020</span><span class="sxs-lookup"><span data-stu-id="50143-528">4.5.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="50143-529">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="50143-529">Az.Accounts</span></span>
* <span data-ttu-id="50143-530">'Connect-AzAccount' cmdlet’i 'MaxContextPopulation' parametresini kabul edecek şekilde güncelleştirildi [#9865]</span><span class="sxs-lookup"><span data-stu-id="50143-530">Updated 'Connect-AzAccount' to accept parameter 'MaxContextPopulation' [#9865]</span></span>
* <span data-ttu-id="50143-531">SubscriptionClient sürümü 2019-06-01 olarak ve kiracı etki alanlarını görüntüleyecek şekilde güncelleştirildi [#9838]</span><span class="sxs-lookup"><span data-stu-id="50143-531">Updated SubscriptionClient version to 2019-06-01 and display tenant domains [#9838]</span></span>
* <span data-ttu-id="50143-532">Aboneliğin giriş kiracısı ve yöneten kiracısı bilgilerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-532">Supported home tenant and managedBy tenant information of subscription</span></span>
* <span data-ttu-id="50143-533">Telemetri verilerindeki modül adı ve sürüm bilgileri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-533">Corrected module name, version info in telemetry data</span></span>
* <span data-ttu-id="50143-534">SqlDatabaseDnsSuffix ve ServiceManagementUrl, ortam meta verileri uç noktasının uyumsuz değer döndürdüğü durumlar için ayarlandı</span><span class="sxs-lookup"><span data-stu-id="50143-534">Adjusted SqlDatabaseDnsSuffix and ServiceManagementUrl if environment metadata endpoint returns incompatible value</span></span>

#### <a name="azaks"></a><span data-ttu-id="50143-535">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="50143-535">Az.Aks</span></span>
* <span data-ttu-id="50143-536">'ClientIdAndSecret' kaldırılarak 'ServicePrincipalIdAndSecret' eklendi ve 'ClientIdAndSecret' bir diğer ad olarak ayarlandı [#12381].</span><span class="sxs-lookup"><span data-stu-id="50143-536">Removed 'ClientIdAndSecret' to 'ServicePrincipalIdAndSecret' and set 'ClientIdAndSecret' as an alias [#12381].</span></span>
* <span data-ttu-id="50143-537">'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' cmdlet’leri kaldırılarak 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' eklendi ve özgün olanlar diğer ad olarak ayarlandı [#12373].</span><span class="sxs-lookup"><span data-stu-id="50143-537">Removed 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' to 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' and set the original ones as alias [#12373].</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="50143-538">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="50143-538">Az.ApiManagement</span></span>
* <span data-ttu-id="50143-539">Yeni 'Add-AzApiManagementApiToGateway' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-539">Added new 'Add-AzApiManagementApiToGateway' cmdlet.</span></span>
* <span data-ttu-id="50143-540">Yeni 'Get-AzApiManagementGateway' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-540">Added new 'Get-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="50143-541">Yeni 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-541">Added new 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="50143-542">Yeni 'Get-AzApiManagementGatewayKey' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-542">Added new 'Get-AzApiManagementGatewayKey' cmdlet.</span></span>
* <span data-ttu-id="50143-543">Yeni 'New-AzApiManagementGateway' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-543">Added new 'New-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="50143-544">Yeni 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-544">Added new 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="50143-545">Yeni 'New-AzApiManagementResourceLocationObject' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-545">Added new 'New-AzApiManagementResourceLocationObject' cmdlet.</span></span>
* <span data-ttu-id="50143-546">Yeni 'Remove-AzApiManagementApiFromGateway' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-546">Added new 'Remove-AzApiManagementApiFromGateway' cmdlet.</span></span>
* <span data-ttu-id="50143-547">Yeni 'Remove-AzApiManagementGateway' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-547">Added new 'Remove-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="50143-548">Yeni 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-548">Added new 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="50143-549">Yeni 'Update-AzApiManagementGateway' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-549">Added new 'Update-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="50143-550">'Get-AzApiManagementApi' cmdlet’ine yeni ve isteğe bağlı [-GatewayId] parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-550">Added new optional [-GatewayId] parameter to the 'Get-AzApiManagementApi' cmdlet.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="50143-551">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="50143-551">Az.CognitiveServices</span></span>
* <span data-ttu-id="50143-552">'Deny', özellikle NetworkRules varsayılan eylemi olarak kullanıldı.</span><span class="sxs-lookup"><span data-stu-id="50143-552">Used 'Deny' specifically as NetworkRules default action.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="50143-553">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="50143-553">Az.FrontDoor</span></span>
* <span data-ttu-id="50143-554">Enum.Parse metodu, bir null değeri Enabled veya Disabled sabit listesi değerlerine zorladığında özel durum oluşturulmasıyla ilgili bir sorun düzeltildi [#12344]</span><span class="sxs-lookup"><span data-stu-id="50143-554">Fixed an issue where an exception is being thrown when Enum.Parse tries to coerce a null value to an Enabled or Disabled enum values [#12344]</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="50143-555">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="50143-555">Az.HDInsight</span></span>
* <span data-ttu-id="50143-556">Aktarma özelliğinde şifrelemeye sahip küme oluşturma desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-556">Supported creating cluster with encryption in transit feature.</span></span>
    - <span data-ttu-id="50143-557">'New-AzHDInsightCluster' cmdlet’ine yeni 'EncryptionInTransit' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-557">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="50143-558">'New-AzHDInsightClusterConfig' cmdlet’ine yeni 'EncryptionInTransit' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-558">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="50143-559">Özel bağlantı özelliğine sahip küme oluşturma desteği eklendi:</span><span class="sxs-lookup"><span data-stu-id="50143-559">Supported creating cluster with private link feature:</span></span>
    - <span data-ttu-id="50143-560">'New-AzHDInsightCluster' cmdlet’ine yeni 'PublicNetworkAccessType' ve 'OutboundPublicNetworkAccessType' parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-560">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="50143-561">'New-AzHDInsightClusterConfig' cmdlet’ine yeni 'PublicNetworkAccessType' ve 'OutboundPublicNetworkAccessType' parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-561">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="50143-562">'New-AzHDInsightCluster' veya 'Get-AzHDInsightCluster' çağrıldığında sanal ağ bilgileri döndürüldü</span><span class="sxs-lookup"><span data-stu-id="50143-562">Returned virtual network information when calling 'New-AzHDInsightCluster' or 'Get-AzHDInsightCluster'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="50143-563">Az.Network</span><span class="sxs-lookup"><span data-stu-id="50143-563">Az.Network</span></span>
* <span data-ttu-id="50143-564">'Remove-AzExpressRouteCircuitConnectionConfig' cmdlet’ine yönelik AddressPrefixType parametresi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-564">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="50143-565">Hataya neden olmayan değişiklikler eklendi: 'Remove-AzExpressRouteCircutPeeringConfig' cmdlet’inde Özel Eşleme’ye yönelik PeerAddressType işlevi eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-565">Added non-breaking changes: PeerAddressType functionality for Private Peering in 'Remove-AzExpressRouteCircutPeeringConfig'.</span></span>
* <span data-ttu-id="50143-566">AddressPrefixType ve PeerAddressType parametresindeki kodlar büyük/küçük harfi yoksayacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-566">Code changed to ignore case for AddressPrefixType and PeerAddressType parameter.</span></span>
* <span data-ttu-id="50143-567">'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' ve 'New-AzPublicIpPrefix' uyarı iletisi değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-567">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="50143-568">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="50143-568">Az.OperationalInsights</span></span>
* <span data-ttu-id="50143-569">'Remove-AzOperationalInsightsworkspace' için '-ForceDelete' seçeneği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-569">Added '-ForceDelete' option for 'Remove-AzOperationalInsightsworkspace'</span></span>
* <span data-ttu-id="50143-570">Yeni 'Get-AzOperationalInsightsDeletedWorkspace' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-570">Added new cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span></span>
* <span data-ttu-id="50143-571">Yeni 'Restore-AzOperationalInsightsWorkspace' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-571">Added new cmdlet 'Restore-AzOperationalInsightsWorkspace'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="50143-572">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="50143-572">Az.RecoveryServices</span></span>
* <span data-ttu-id="50143-573">Azure Backup kapsayıcı/öğe keşif deneyimi iyileştirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-573">Improved the Azure Backup container/item discovery experience.</span></span>

#### <a name="azresources"></a><span data-ttu-id="50143-574">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="50143-574">Az.Resources</span></span>
* <span data-ttu-id="50143-575">'New-AzRoleAssignment' cmdlet’ine 'Condition', 'ConditionVersion' ve 'Description' özellikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-575">Added properties 'Condition', 'ConditionVersion' and 'Description' to 'New-AzRoleAssignment'</span></span>
    - <span data-ttu-id="50143-576">Bu, veri modellerinde yapılan tüm ilgili değişiklikleri içerir</span><span class="sxs-lookup"><span data-stu-id="50143-576">This included all the relevant changes to the data models</span></span>

#### <a name="azsql"></a><span data-ttu-id="50143-577">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="50143-577">Az.Sql</span></span>
* <span data-ttu-id="50143-578">'New-AzSqlServer' ve 'Set-AzSqlServer' cmdlet’lerindeki sunucu adının olası büyük/küçük harfe duyarsızlık hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-578">Fixed potential server name case insensitive error in 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="50143-579">'New-AzSqlDatabaseSecondary' cmdlet’indeki mevcut veritabanına yanlış veritabanı adının döndürülmesi hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-579">Fixed wrong database name returned on existing database error in 'New-AzSqlDatabaseSecondary'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="50143-580">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="50143-580">Az.Storage</span></span>
* <span data-ttu-id="50143-581">Yeni x,t izniyle kapsayıcı/blob Sas belirteci oluşturma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-581">Supported create container/blob Sas token with new permission x,t</span></span>
    -  <span data-ttu-id="50143-582">“New-AzStorageBlobSASToken”</span><span class="sxs-lookup"><span data-stu-id="50143-582">'New-AzStorageBlobSASToken'</span></span>
    -  <span data-ttu-id="50143-583">'New-AzStorageContainerSASToken'</span><span class="sxs-lookup"><span data-stu-id="50143-583">'New-AzStorageContainerSASToken'</span></span>
* <span data-ttu-id="50143-584">Yeni x,t,f izniyle hesap Sas belirteci oluşturma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-584">Supported create account Sas token with new permission x,t,f</span></span>
    -  <span data-ttu-id="50143-585">'New-AzStorageAccountSASToken'</span><span class="sxs-lookup"><span data-stu-id="50143-585">'New-AzStorageAccountSASToken'</span></span>
* <span data-ttu-id="50143-586">Tek dosya paylaşımı kullanımını alma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-586">Supported get single file share usage</span></span>
    - <span data-ttu-id="50143-587">'Get-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="50143-587">'Get-AzRmStorageShare'</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="50143-588">4.4.0 - Temmuz 2020</span><span class="sxs-lookup"><span data-stu-id="50143-588">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="50143-589">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="50143-589">Az.Accounts</span></span>
* <span data-ttu-id="50143-590">“Invoke-AzRestMethod” adlı yeni cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-590">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="50143-591">“Start-Job” kullanan birden çok Azure PowerShell cmdlet’inin çalıştığı durumlar gibi çok işlemli senaryolarda kimlik doğrulama hatalarına sebep olabilen bir sorun düzeltildi [#9448]</span><span class="sxs-lookup"><span data-stu-id="50143-591">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="50143-592">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="50143-592">Az.Aks</span></span>
* <span data-ttu-id="50143-593">“Get-AzAks” cmdlet’inin tüm kümeleri almamasına neden olan hata düzeltildi [#12296]</span><span class="sxs-lookup"><span data-stu-id="50143-593">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="50143-594">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="50143-594">Az.AnalysisServices</span></span>
* <span data-ttu-id="50143-595">Kimlik Doğrulamasına yönelik proje başvurusu kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="50143-595">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="50143-596">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="50143-596">Az.Automation</span></span>
* <span data-ttu-id="50143-597">Kaçış karakterleri içeren dizenin bir JSON nesnesine dönüştürülememesiyle ilgili sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-597">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="50143-598">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="50143-598">Az.Compute</span></span>
* <span data-ttu-id="50143-599">“En son” resim sürümü olmadan “New-AzVmss” cmdlet’ini kullanırken görüntülenecek bir uyarı eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-599">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="50143-600">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="50143-600">Az.DataFactory</span></span>
* <span data-ttu-id="50143-601">Data Factory’ye genel parametreler eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-601">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="50143-602">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="50143-602">Az.EventGrid</span></span>
* <span data-ttu-id="50143-603">2020-06-01 API sürümünü kullanacak biçimde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-603">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="50143-604">Yeni özellikler eklendi:</span><span class="sxs-lookup"><span data-stu-id="50143-604">Added new features:</span></span>
    - <span data-ttu-id="50143-605">Giriş eşleme</span><span class="sxs-lookup"><span data-stu-id="50143-605">Input mapping</span></span>
    - <span data-ttu-id="50143-606">Olay Teslim Şeması</span><span class="sxs-lookup"><span data-stu-id="50143-606">Event Delivery Schema</span></span>
    - <span data-ttu-id="50143-607">Özel Bağlantı</span><span class="sxs-lookup"><span data-stu-id="50143-607">Private Link</span></span>
    - <span data-ttu-id="50143-608">Bulut Olayı V10 Şeması</span><span class="sxs-lookup"><span data-stu-id="50143-608">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="50143-609">Hedef Olarak Service Bus Konu Başlığı</span><span class="sxs-lookup"><span data-stu-id="50143-609">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="50143-610">Hedef Olarak Azure İşlevi</span><span class="sxs-lookup"><span data-stu-id="50143-610">Azure Function As Destination</span></span>
    - <span data-ttu-id="50143-611">Web Kancası Toplu İş</span><span class="sxs-lookup"><span data-stu-id="50143-611">WebHook Batching</span></span>
    - <span data-ttu-id="50143-612">Güvenli web kancası (AAD desteği)</span><span class="sxs-lookup"><span data-stu-id="50143-612">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="50143-613">IpFiltering</span><span class="sxs-lookup"><span data-stu-id="50143-613">IpFiltering</span></span>
* <span data-ttu-id="50143-614">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="50143-614">Updated cmdlets:</span></span>
    - <span data-ttu-id="50143-615">“New-AzEventGridSubscription'/'Update-AzEventGridSubscription”:</span><span class="sxs-lookup"><span data-stu-id="50143-615">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="50143-616">Web kancası toplu işlemin destekleyecek yeni, isteğe bağlı parametreler eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-616">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="50143-617">AAD kullanarak güvenli web kancasını desteklemek için yeni, isteğe bağlı parametreler eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-617">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="50143-618">Yeni hedef olarak Azure İşlevi’ni ve Service Bus konu başlığını desteklemek üzere EndpointType parametresi için yeni bir sabit listesi eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-618">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="50143-619">Teslim şeması için yeni, isteğe bağlı parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-619">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="50143-620">“New-AzEventGridTopic'/'Update-AzEventGridTopic” ve “New-AzEventGridDomain'/'Update-AzEventGridDomain”:</span><span class="sxs-lookup"><span data-stu-id="50143-620">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="50143-621">IpFiltering’i destekleyecek yeni, isteğe bağlı parametreler eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-621">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="50143-622">“New-AzEventGridTopic'/'New-AzEventGridDomain”:</span><span class="sxs-lookup"><span data-stu-id="50143-622">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="50143-623">Giriş eşlemeyi destekleyecek yeni, isteğe bağlı parametreler eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-623">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="50143-624">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="50143-624">Az.FrontDoor</span></span>
* <span data-ttu-id="50143-625">Modül, API 2020-05-01 kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-625">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="50143-626">Depolama, Key Vault ve Web App Service kaynakları için Özel bağlantı desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-626">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="50143-627">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="50143-627">Az.HDInsight</span></span>
* <span data-ttu-id="50143-628">Ulusal bulutlarda ADLS 1. veya 2. Nesil depolama ile küme oluşturmaya yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-628">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="50143-629">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="50143-629">Az.Monitor</span></span>
* <span data-ttu-id="50143-630">Ölçümler ve günlükler null olduğunda “Get-AzDiagnosticSetting” cmdlet’inde oluşan hata düzeltildi [#12272]</span><span class="sxs-lookup"><span data-stu-id="50143-630">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="50143-631">Az.Network</span><span class="sxs-lookup"><span data-stu-id="50143-631">Az.Network</span></span>
* <span data-ttu-id="50143-632">VWan HubVnet bağlantısında değişen parametreler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-632">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="50143-633">Azure Ağ Sanal Alet Siteleri’ne yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-633">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="50143-634">“Get-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="50143-634">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="50143-635">“New-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="50143-635">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="50143-636">“Remove-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="50143-636">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="50143-637">“Update-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="50143-637">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="50143-638">“New-AzOffice365PolicyProperty”</span><span class="sxs-lookup"><span data-stu-id="50143-638">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="50143-639">Azure Ağ Sanal Gereçi’ne yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-639">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="50143-640">“Get-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="50143-640">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="50143-641">“New-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="50143-641">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="50143-642">“Remove-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="50143-642">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="50143-643">“Update-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="50143-643">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="50143-644">“Get-AzNetworkVirtualApplianceSku”</span><span class="sxs-lookup"><span data-stu-id="50143-644">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="50143-645">“New-AzVirtualApplianceSkuProperty”</span><span class="sxs-lookup"><span data-stu-id="50143-645">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="50143-646">Özel Bağlantı Ortak Cmdlet’lerine Application Gateway eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-646">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="50143-647">Özel Bağlantı Ortak Cmdlet’lerine StorageSync Eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-647">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="50143-648">Özel Bağlantı Ortak Cmdlet’lerine SignalR Eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-648">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="50143-649">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="50143-649">Az.RecoveryServices</span></span>
* <span data-ttu-id="50143-650">Kimlik Doğrulamasına yönelik proje başvurusu kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="50143-650">Removed project reference to Authentication</span></span>
* <span data-ttu-id="50143-651">Azure Backup, cmdlet’leri metinlerin daha doğru görüneceği şekilde ayarladı</span><span class="sxs-lookup"><span data-stu-id="50143-651">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="50143-652">Azure Backup, “Get-AzRecoveryServicesBackupJob” cmdlet’i kullanılarak MAB aracı işlerinin getirilmesine yönelik destek ekledi.</span><span class="sxs-lookup"><span data-stu-id="50143-652">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="50143-653">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="50143-653">Az.Resources</span></span>
* <span data-ttu-id="50143-654">“Save-AzResourceGroupDeploymentTemplate” cmdlet’i SDK’yı kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-654">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="50143-655">“Unregister-AzResourceProvider” cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-655">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="50143-656">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="50143-656">Az.Sql</span></span>
* <span data-ttu-id="50143-657">“Set-AzSqlInstanceActiveDirectoryAdministrator” cmdlet’indeki Hizmet sorumlusu ve konuk kullanıcılara yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-657">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="50143-658">Veri Sınıflandırma cmdlet’lerindeki bir sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-658">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="50143-659">Azure SQL Yönetilen Örneği yük devretmesine yönelik destek eklendi: “Invoke-AzSqlInstanceFailover”</span><span class="sxs-lookup"><span data-stu-id="50143-659">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="50143-660">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="50143-660">Az.Storage</span></span>
* <span data-ttu-id="50143-661">Bazı veri düzlemi cmdlet’leri için UserAgent’ın eklenmemesiyle ilgili sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-661">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="50143-662">MinimumTlsVersion ve AllowBlobPublicAccess içeren bir Depolama hesabını oluşturmaya/güncelleştirmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-662">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="50143-663">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="50143-663">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="50143-664">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="50143-664">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="50143-665">Bir Depolama hesabının Blob Hizmeti üzerinde sürüm oluşturmayı etkinleştirmeye/devre dışı bırakmaya yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-665">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="50143-666">“Update-AzStorageBlobServiceProperty”</span><span class="sxs-lookup"><span data-stu-id="50143-666">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="50143-667">Blob sürümlerini içeren destek listesi blobları</span><span class="sxs-lookup"><span data-stu-id="50143-667">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="50143-668">“Get-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="50143-668">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="50143-669">Tek bir blob anlık görüntüsünü veya blob sürümünü almaya/kaldırmaya yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-669">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="50143-670">“Get-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="50143-670">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="50143-671">“Remove-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="50143-671">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="50143-672">Azure.Storage.Blobs V12’den oluşturulan blob nesnesindeki işlem hattına yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-672">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="50143-673">“Get-AzStorageBlobContent”</span><span class="sxs-lookup"><span data-stu-id="50143-673">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="50143-674">“New-AzStorageBlobSASToken”</span><span class="sxs-lookup"><span data-stu-id="50143-674">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="50143-675">“Remove-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="50143-675">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="50143-676">“Set-AzStorageBlobContent”</span><span class="sxs-lookup"><span data-stu-id="50143-676">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="50143-677">“Start-AzStorageBlobCopy”</span><span class="sxs-lookup"><span data-stu-id="50143-677">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="50143-678">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="50143-678">Az.StorageSync</span></span>
* <span data-ttu-id="50143-679">ApiVersion 2020-03-01 sürümünü hedefleyen yeni bir StorageSync SDK sürümü eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-679">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="50143-680">“UpdateStorageSyncService” cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-680">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="50143-681">“Set-AzStorageSyncService”</span><span class="sxs-lookup"><span data-stu-id="50143-681">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="50143-682">StorageSyncService cmdlet’ine IncomingTrafficPolicy ve PrivateEndpointConnections eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-682">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="50143-683">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="50143-683">Az.Websites</span></span>
* <span data-ttu-id="50143-684">App Service Planıyla aynı kaynak grubunda bulunmayan Yuvalar için işlem gerçekleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-684">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="50143-685">4.3.0 - Haziran 2020</span><span class="sxs-lookup"><span data-stu-id="50143-685">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="50143-686">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="50143-686">Az.Accounts</span></span>
* <span data-ttu-id="50143-687">Ortam ayarını varsayılan olarak bulma ve 'Add-AzEnvironment' aracılığıyla ortam ekleme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-687">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="50143-688">Önceden yüklenmiş bütünleştirilmiş kodlar güncelleştirildi [#12024], [#11976]</span><span class="sxs-lookup"><span data-stu-id="50143-688">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="50143-689">Azure.Core bütünleştirilmiş kodu güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-689">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="50143-690">'Connect-AzAccount' cmdlet’inin çok iş parçacıklı yürütmede başarısız olmasına neden olabilen bir sorun düzeltildi [#11201]</span><span class="sxs-lookup"><span data-stu-id="50143-690">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="50143-691">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="50143-691">Az.Aks</span></span>
* <span data-ttu-id="50143-692">Eski [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile)’sinin kullanımı [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) ve [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) API’lerine yönelik çağrılarla değiştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-692">Replaced usage of old [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="50143-693">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="50143-693">Az.Batch</span></span>
* <span data-ttu-id="50143-694">Az.Batch, 'Microsoft.Azure.Management.Batch' SDK sürüm 11.0.0 kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-694">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="50143-695">BatchAccount.Identity özelliğini 'New-AzBatchAccount' cmdlet’ine ayarlama özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-695">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="50143-696">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="50143-696">Az.CognitiveServices</span></span>
* <span data-ttu-id="50143-697">Hesap özelliklerini görüntüleme desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-697">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="50143-698">PublicNetworkAccess özelliğinin değiştirilmesi desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-698">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="50143-699">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="50143-699">Az.Compute</span></span>
* <span data-ttu-id="50143-700">Set-AzVM ve Set-AzVmssVM cmdlet’lerine SimulateEviction parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-700">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="50143-701">New-AzGalleryImageVersion cmdlet’i için StorageAccountType parametresinin bağımsız değişken tamamlayıcısına 'Premium_LRS' eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-701">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="50143-702">VMCustomScriptExtension için Alt Durumlar eklendi [#11297]</span><span class="sxs-lookup"><span data-stu-id="50143-702">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="50143-703">New-AzVM ve New-AzVMConfig cmdlet’leri için EvictionPolicy parametresinin bağımsız değişken tamamlayıcısına 'Delete' eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-703">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="50143-704">SAP için yeni VM Uzantısı’nın adı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-704">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="50143-705">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="50143-705">Az.DataFactory</span></span>
* <span data-ttu-id="50143-706">ADF .NET SDK’sı 4.9.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-706">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="50143-707">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="50143-707">Az.EventHub</span></span>
* <span data-ttu-id="50143-708">'New-AzEventHubNamespace' ve 'Set-AzEventHubNamespace' cmdlet’lerine Yönetilen Kimlik parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-708">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="50143-709">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="50143-709">Az.Functions</span></span>
* <span data-ttu-id="50143-710">PowerShell 7.0 ve Java 11 işlev uygulamaları oluşturma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-710">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="50143-711">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="50143-711">Az.HDInsight</span></span>
* <span data-ttu-id="50143-712">HDInsight kümesinin konaklarını listeleme ve belirli konaklarını yeniden başlatma desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-712">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="50143-713">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="50143-713">Az.HealthcareApis</span></span>
* <span data-ttu-id="50143-714">SDK sürümü 1.1.0 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-714">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="50143-715">Dışarı aktarma ayarları ve Yönetilen Kimlik desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-715">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="50143-716">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="50143-716">Az.Monitor</span></span>
* <span data-ttu-id="50143-717">'Set-AzActivityLogAlert' için giriş nesnesi parametresi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-717">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="50143-718">'Set-AzActionGroup' için 'InputObject' parametresi düzeltildi [#10868]</span><span class="sxs-lookup"><span data-stu-id="50143-718">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="50143-719">Az.Network</span><span class="sxs-lookup"><span data-stu-id="50143-719">Az.Network</span></span>
* <span data-ttu-id="50143-720">'Remove-AzExpressRouteCircuitConnectionConfig' cmdlet’ine yönelik AddressPrefixType parametresi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-720">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="50143-721">Azure FirewallPolicy için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-721">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="50143-722">'New-AzFirewallPolicyDnsSetting'</span><span class="sxs-lookup"><span data-stu-id="50143-722">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="50143-723">Güvenlik Duvarı İlkesi için Ağ Kuralları’nda Hedef FQDN Desteği</span><span class="sxs-lookup"><span data-stu-id="50143-723">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="50143-724">Arka uç adres havuzu işlemlerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-724">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="50143-725">'New-AzLoadBalancerBackendAddressConfig'</span><span class="sxs-lookup"><span data-stu-id="50143-725">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="50143-726">'New-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="50143-726">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="50143-727">'Set-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="50143-727">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="50143-728">'Remove-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="50143-728">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="50143-729">'Get-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="50143-729">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="50143-730">'New-AzIpGroup' için ad doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-730">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="50143-731">Azure FirewallPolicy için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-731">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="50143-732">'New-AzFirewallPolicyThreatIntelWhitelist'</span><span class="sxs-lookup"><span data-stu-id="50143-732">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="50143-733">Özellik için aşağıdaki komutlar güncelleştirildi: VirtualWan P2SVpnGateway üzerinde özel DNS sunucuları ayarlama/kaldırma.</span><span class="sxs-lookup"><span data-stu-id="50143-733">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="50143-734">New-AzP2sVpnGateway güncelleştirildi: Müşterilerin DNS sunucularını, Noktadan siteye işlemciler tarafından kullanılabilen P2SVpnGateway üzerinde ayarlanacak şekilde belirtmeleri için '-CustomDnsServer' isteğe bağlı parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-734">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="50143-735">Update-AzP2sVpnGateway güncelleştirildi: Müşterilerin DNS sunucularını, Noktadan siteye işlemciler tarafından kullanılabilen P2SVpnGateway üzerinde ayarlanacak şekilde belirtmeleri için '-CustomDnsServer' isteğe bağlı parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-735">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="50143-736">'Update-AzVpnGateway' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-736">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="50143-737">Müşterilerin özel BGP’lerini VpnGateway üzerinde ayarlanacak şekilde belirtmeleri için '-BgpPeeringAddress' isteğe bağlı parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-737">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="50143-738">Bir VirtualHub kaynağının yönlendirme durumunu sıfırlamayı desteklemek amacıyla yeni cmdlet eklendi:</span><span class="sxs-lookup"><span data-stu-id="50143-738">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="50143-739">'Reset-AzHubRouter'</span><span class="sxs-lookup"><span data-stu-id="50143-739">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="50143-740">Güvenlik Duvarı İlkesi’nde yapılan son Swagger değişikliğine göre aşağıdakiler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-740">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="50143-741">RuleGroup, RuleCollectionGroup ve RuleType adları değiştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-741">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="50143-742">Birden çok NAT Kural Koleksiyonu’nu desteklemek amacıyla Güvenlik Duvarı İlkesi NAT Kural Koleksiyonları’na yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-742">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="50143-743">[Yeni Değişiklik] 'New-AzFirewallPolicyApplicationRule' ve 'New-AzFirewallPolicyNetworkRule' için 'SourceIpGroup' zorunlu parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-743">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="50143-744">[Yeni Değişiklik] 'New-AzFirewallPolicyApplicationRule', 'SourceAddress' parametresi zorunlu olacak şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-744">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="50143-745">[Yeni Değişiklik] 'New-AzFirewallPolicyApplicationRule', 'SourceAddress' parametresi zorunlu olacak şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-745">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="50143-746">[Yeni Değişiklik] Şu zorunu parametreler kaldırıldı: 'New-AzFirewallPolicyNatRuleCollection' için 'TranslatedAddress', 'TranslatedPort'.</span><span class="sxs-lookup"><span data-stu-id="50143-746">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="50143-747">Application Gateway üzerinde PrivateLink’i destekleyecek yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-747">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="50143-748">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="50143-748">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="50143-749">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="50143-749">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="50143-750">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="50143-750">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="50143-751">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="50143-751">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="50143-752">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="50143-752">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="50143-753">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span><span class="sxs-lookup"><span data-stu-id="50143-753">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="50143-754">VirtualHub’ın HubRouteTables alt kaynağı için yeni cmdlet’ler eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-754">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="50143-755">'New-AzVHubRoute'</span><span class="sxs-lookup"><span data-stu-id="50143-755">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="50143-756">'New-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="50143-756">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="50143-757">'Get-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="50143-757">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="50143-758">'Update-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="50143-758">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="50143-759">'Remove-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="50143-759">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="50143-760">Mevcut cmdlet’ler VirtualWan’deki özel yönlendirmede isteğe bağlı RoutingConfiguration giriş parametresini destekleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-760">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="50143-761">'New-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="50143-761">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="50143-762">'Set-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="50143-762">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="50143-763">‘New-AzVirtualHubVnetConnection’</span><span class="sxs-lookup"><span data-stu-id="50143-763">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="50143-764">‘Update-AzVirtualHubVnetConnection’</span><span class="sxs-lookup"><span data-stu-id="50143-764">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="50143-765">'New-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="50143-765">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="50143-766">'Update-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="50143-766">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="50143-767">'New-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="50143-767">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="50143-768">'Update-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="50143-768">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="50143-769">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="50143-769">Az.OperationalInsights</span></span>
* <span data-ttu-id="50143-770">PSWorkspace’in OperationalInsightsWorkspace’i uygulamamasıyla ilgili hata düzeltildi [#12135]</span><span class="sxs-lookup"><span data-stu-id="50143-770">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="50143-771">'Set-AzOperationalInsightsWorkspace' cmdlet’indeki 'Sku' parametresinin geçerli değer kümesine 'pergb2018' eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-771">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="50143-772">'FunctionParameter' parametresi için 'FunctionParameters' diğer adı eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-772">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="50143-773">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="50143-773">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="50143-774">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="50143-774">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="50143-775">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="50143-775">Az.RecoveryServices</span></span>
* <span data-ttu-id="50143-776">Azure Backup’a MAB öğelerini getirme desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-776">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="50143-777">Azure Site Recovery, 'StandardSSD_LRS' disk türünü destekler</span><span class="sxs-lookup"><span data-stu-id="50143-777">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="50143-778">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="50143-778">Az.Resources</span></span>
* <span data-ttu-id="50143-779">'PSADUser' değerine 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname' eklendi [#10526] [#10497]</span><span class="sxs-lookup"><span data-stu-id="50143-779">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="50143-780">'Get-AzADUser' üzerinde '-Mail' değerinin çalışmamasıyla ilgili sorun düzeltildi [#11981]</span><span class="sxs-lookup"><span data-stu-id="50143-780">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="50143-781">'Get-AzDeploymentWhatIfResult' ve 'Get-AzResourceGroupDeploymentWhatIfResult' cmdlet’lerine -ExcludeChangeType' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-781">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="50143-782">'New-AzDeployment' ve 'New-AzResourceGroupDeployment' cmdlet’lerine '-WhatIfExcludeChangeType' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-782">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="50143-783">'Test-Az\*Deployment' cmdlet’leri daha iyi hata iletileri gösterecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-783">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="50143-784">deployment create ve What-If cmdlet’lerinin '-Name' parametresine yönelik yardım iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-784">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="50143-785">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="50143-785">Az.Sql</span></span>
* <span data-ttu-id="50143-786">SQL Server Azure Active Directory Yönetici cmdlet’ine hizmet sorumlusu desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-786">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="50143-787">Veri Sınıflandırma cmdlet’lerindeki eşitleme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-787">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="50143-788">'Set-AzSqlServerActiveDirectoryAdministrator' üzerinde postaya göre kullanıcı arama desteği eklendi [#12192]</span><span class="sxs-lookup"><span data-stu-id="50143-788">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="50143-789">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="50143-789">Az.Storage</span></span>
* <span data-ttu-id="50143-790">RequireInfrastructureEncryption ile Depolama hesabı oluşturma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-790">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="50143-791">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="50143-791">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="50143-792">Azure.Core yükleme mantığı Az.Accounts’a taşındı</span><span class="sxs-lookup"><span data-stu-id="50143-792">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="50143-793">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="50143-793">Az.Websites</span></span>
* <span data-ttu-id="50143-794">'Restore-AzDeletedWebApp' cmdlet’inde geri yüklemenin başarısız olması durumunda, oluşturulan web uygulamasının silinmesine yönelik koruma eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-794">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="50143-795">'New-AzWebApp' ve 'New-AzWebAppSlot' için SourceWebApp.Location' eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-795">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="50143-796">'Set-AzWebApp' ve 'Set-AzWebAppSlot' cmdlet’lerinde Kapsayıcı ayarlarının değiştirilmesini engelleyen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-796">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="50143-797">Get-AzWebApp için -Name verilmediğinde SiteConfig alınmasıyla ilgili hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-797">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="50143-798">Linux Uygulamaları için ASP oluşturmaya yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-798">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="50143-799">Kaynak grupları arasında kopyalama için özel durumlar eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-799">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="50143-800">4.2.0 - Haziran 2020</span><span class="sxs-lookup"><span data-stu-id="50143-800">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="50143-801">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="50143-801">Az.Accounts</span></span>
* <span data-ttu-id="50143-802">Azure Otomasyonu veya PowerShell işlerinde Az’nin günlükleri atlamasına neden olabilecek bir sorun düzeltildi [#11492]</span><span class="sxs-lookup"><span data-stu-id="50143-802">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="50143-803">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="50143-803">Az.AnalysisServices</span></span>
* <span data-ttu-id="50143-804">Veri düzlemi cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-804">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="50143-805">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="50143-805">Az.ApiManagement</span></span>
* <span data-ttu-id="50143-806">Hizmet yönetimi cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-806">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="50143-807">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="50143-807">Az.Billing</span></span>
* <span data-ttu-id="50143-808">Tüketim cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-808">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="50143-809">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="50143-809">Az.CognitiveServices</span></span>
* <span data-ttu-id="50143-810">PrivateEndpoint ve PublicNetworkAccess denetimini destekler.</span><span class="sxs-lookup"><span data-stu-id="50143-810">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="50143-811">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="50143-811">Az.DataFactory</span></span>
* <span data-ttu-id="50143-812">Veri fabrikası V2 cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-812">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="50143-813">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="50143-813">Az.DataShare</span></span>
* <span data-ttu-id="50143-814">''Az.DataShare'' modülü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="50143-814">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="50143-815">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="50143-815">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="50143-816">''Az.DesktopVirtualization'' modülü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="50143-816">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="50143-817">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="50143-817">Az.OperationalInsights</span></span>
* <span data-ttu-id="50143-818">SDK 0.21.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-818">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="50143-819">İsteğe bağlı aşağıdaki parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-819">Added optional parameters to</span></span> 
    - <span data-ttu-id="50143-820">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="50143-820">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="50143-821">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="50143-821">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="50143-822">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="50143-822">Az.PolicyInsights</span></span>
* <span data-ttu-id="50143-823">'Start-AzPolicyComplianceScan' için 3. örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-823">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="50143-824">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="50143-824">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="50143-825">PowerBI cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-825">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="50143-826">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="50143-826">Az.PrivateDns</span></span>
* <span data-ttu-id="50143-827">Remove-AzPrivateDnsRecordSet için ayrıntılı çıkış dizesi biçimlendirmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-827">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="50143-828">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="50143-828">Az.RecoveryServices</span></span>
* <span data-ttu-id="50143-829">XML girişinden bölgeler arasında çoğaltma için kurtarma planı oluşturmaya yönelik Azure Site Recovery desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-829">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="50143-830">SiteRecovery ve Backup cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-830">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="50143-831">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="50143-831">Az.Resources</span></span>
* <span data-ttu-id="50143-832">Get-AzDeploymentScriptLog ve Save-AzDeploymentScriptLog cmdlet’lerine Tail parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-832">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="50143-833">Çıkış özelliği biçimlendirildi ve Get-AzDeploymentScript cmdlet çıkışında gösterildi</span><span class="sxs-lookup"><span data-stu-id="50143-833">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="50143-834">-DeploymentScriptInputObject parametresinin adı -DeploymentScriptObject olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-834">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="50143-835">Cmdlet iletilerinde geçersiz dosya/hedef adı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-835">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="50143-836">Kaynak yöneticisi ve etiketler cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-836">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="50143-837">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="50143-837">Az.Sql</span></span>
* <span data-ttu-id="50143-838">'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' ve 'Update-AzSqlSyncMember' öğelerine UsePrivateLinkConnection eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-838">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="50143-839">'New-AzSqlSyncMember' ve 'Update-AzSqlSyncMember' öğelerine SyncMemberAzureDatabaseResourceId eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-839">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="50143-840">SQL Server Azure Active Directory Yönetici cmdlet’ine Konuk kullanıcı arama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-840">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="50143-841">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="50143-841">Az.Storage</span></span>
* <span data-ttu-id="50143-842">Veri düzlemi cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-842">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="50143-843">4.1.0 - Mayıs 2020</span><span class="sxs-lookup"><span data-stu-id="50143-843">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="50143-844">Son sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="50143-844">Highlights since the last release</span></span>
* <span data-ttu-id="50143-845">Desteklenen PowerShell sürümleri: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="50143-845">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="50143-846">Az.Functions genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="50143-846">General availability of Az.Functions</span></span> 
* <span data-ttu-id="50143-847">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources ve Az.Storage için ana sürüm yayımlandı</span><span class="sxs-lookup"><span data-stu-id="50143-847">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="50143-848">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="50143-848">Az.Accounts</span></span>
* <span data-ttu-id="50143-849">'Add-AzEnvironment' ve 'Set-AzEnvironment', 'AzureSynapseAnalyticsEndpointResourceId' ve 'AzureSynapseAnalyticsEndpointSuffix' parametrelerini kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-849">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="50143-850">Azure.Core ile ilgili bütünleştirilmiş kodlar Az.Accounts’a eklendi, desteklenen PowerShell platformları Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+ sürümlerini içerir</span><span class="sxs-lookup"><span data-stu-id="50143-850">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="50143-851">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="50143-851">Az.Aks</span></span>
* <span data-ttu-id="50143-852">API Sürümü 2019-10-01’e yükseltildi</span><span class="sxs-lookup"><span data-stu-id="50143-852">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="50143-853">Windows kapsayıcısı kullanılarak AKS oluşturma desteği sunuldu</span><span class="sxs-lookup"><span data-stu-id="50143-853">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="50143-854">Yeni cmdlet’ler sağlandı: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span><span class="sxs-lookup"><span data-stu-id="50143-854">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="50143-855">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="50143-855">Az.ApiManagement</span></span>
* <span data-ttu-id="50143-856">'New-AzApiManagement' ve 'Set-AzApiManagement': [-AssignIdentity] parametresi [-SystemAssignedIdentity] olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="50143-856">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="50143-857">'New-AzApiManagement' ve 'Set-AzApiManagement': Yeni parametre eklendi: [-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="50143-857">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="50143-858">'Get-AzApiManagementProperty': 'Get-AzApiManagementNamedValue' olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="50143-858">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="50143-859">PropertyId parametresi NamedValueId olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="50143-859">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="50143-860">'New-AzApiManagementProperty': 'New-AzApiManagementNamedValue' olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="50143-860">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="50143-861">PropertyId parametresi NamedValueId olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="50143-861">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="50143-862">'Set-AzApiManagementProperty': 'Set-AzApiManagementNamedValue' olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="50143-862">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="50143-863">PropertyId parametresi NamedValueId olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="50143-863">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="50143-864">'Remove-AzApiManagementProperty': 'Remove-AzApiManagementNamedValue' olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="50143-864">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="50143-865">PropertyId parametresi NamedValueId olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="50143-865">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="50143-866">Yeni 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet’i eklendi. 'Get-AzApiManagementAuthorizationServer' artık istemci gizli dizisini döndürmez.</span><span class="sxs-lookup"><span data-stu-id="50143-866">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="50143-867">Yeni 'Get-AzApiManagementNamedValueSecretValue' cmdlet’i eklendi. 'Get-AzApiManagementNamedValue' artık gizli dizi değerini döndürmez.</span><span class="sxs-lookup"><span data-stu-id="50143-867">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="50143-868">Yeni 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet’i eklendi. 'Get-AzApiManagementOpenIdConnectProvider' artık istemci gizli dizisini döndürmez.</span><span class="sxs-lookup"><span data-stu-id="50143-868">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="50143-869">Yeni 'Get-AzApiManagementSubscriptionKey' cmdlet’i eklendi. 'Get-AzApiManagementSubscription' artık abonelik anahtarlarını döndürmez.</span><span class="sxs-lookup"><span data-stu-id="50143-869">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="50143-870">Yeni 'Get-AzApiManagementTenantAccessSecret' cmdlet’i eklendi. 'Get-AzApiManagementTenantAccess' artık anahtarları döndürmez.</span><span class="sxs-lookup"><span data-stu-id="50143-870">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="50143-871">Yeni 'Get-AzApiManagementTenantGitAccessSecret' cmdlet’i eklendi. 'Get-AzApiManagementTenantGitAccess' artık anahtarları döndürmez.</span><span class="sxs-lookup"><span data-stu-id="50143-871">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="50143-872">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="50143-872">Az.ApplicationInsights</span></span>
* <span data-ttu-id="50143-873">Parametreler eklendi: 'New-AzApplicationInsights' için 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery'</span><span class="sxs-lookup"><span data-stu-id="50143-873">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="50143-874">'Update-AzApplicationInsights' cmdlet’i oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="50143-874">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="50143-875">Bağlı Depolama Hesapları için cmdlet’ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="50143-875">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="50143-876">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="50143-876">Az.Batch</span></span>
* <span data-ttu-id="50143-877">Az.Batch, 'Microsoft.Azure.Batch' SDK sürüm 13.0.0 ve 'Microsoft.Azure.Management.Batch' SDK sürüm 9.0.0 kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-877">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="50143-878">'New-AzBatchCertificate' için yeni '-CertificateKind' parametresi kullanılarak eklenen sertifika türünü seçme yeteneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-878">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="50143-879">Önceden hep '' olan 'ApplicationPackages' özelliği 'PSApplication' öğesinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50143-879">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="50143-880">Uygulamanın içindeki belirli paketler artık 'Get-AzBatchApplicationPackage' kullanılarak alınabilir.</span><span class="sxs-lookup"><span data-stu-id="50143-880">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="50143-881">Örneğin: 'Get-AzBatchApplication -AccountName hesabım -ResourceGroupName kaynakgrubum -ApplicationId uygulamam'.</span><span class="sxs-lookup"><span data-stu-id="50143-881">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="50143-882">'New-AzBatchPool' kullanılarak havuz oluşturulurken, 'PSImageReference' öğesinin 'VirtualMachineImageId' özelliği artık yalnızca bir Paylaşılan Görüntü Galerisi görüntüsüne başvurabilir.</span><span class="sxs-lookup"><span data-stu-id="50143-882">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="50143-883">'New-AzBatchPool' kullanılarak havuz oluşturulurken, havuz 'PSNetworkConfiguration' öğesinin yeni 'PublicIPAddressConfiguration' özelliği kullanılarak genel IP olmadan sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="50143-883">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="50143-884">'PSNetworkConfiguration' öğesinin 'PublicIPs' özelliği de 'PSPublicIPAddressConfiguration' içine taşındı.</span><span class="sxs-lookup"><span data-stu-id="50143-884">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="50143-885">Bu özellik yalnızca 'IPAddressProvisioningType' değeri 'UserManaged' olduğunda belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="50143-885">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="50143-886">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="50143-886">Az.Compute</span></span>
* <span data-ttu-id="50143-887">'Update-AzVM' cmdlet’ine HostId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-887">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="50143-888">'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' ve 'Set-AzVmssOsProfile' cmdlet’leri için Yardım belgeleri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-888">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="50143-889">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="50143-889">Breaking changes</span></span>
    - <span data-ttu-id="50143-890">FilterExpression parametresi 'Get-AzVMImage' cmdlet’inden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50143-890">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="50143-891">AssignIdentity parametresi 'New-AzVmssConfig', 'New-AzVMConfig' ve 'Update-AzVM' cmdlet’lerinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50143-891">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="50143-892">AutomaticRepairMaxInstanceRepairsPercent, 'New-AzVmssConfig' ve 'Update-AzVmss' cmdlet’lerinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50143-892">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="50143-893">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus ve VirtualMachineScaleSetsColocationStatus özellikleri ProximityPlacementGroup öğesinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50143-893">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="50143-894">MaxInstanceRepairsPercent özelliği AutomaticRepairsPolicy öğesinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50143-894">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="50143-895">AvailabilitySets, VirtualMachines ve VirtualMachineScaleSets türleri IList<SubResource> türünden IList<SubResourceWithColocationStatus> türüne değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-895">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="50143-896">'Get-AzVM' cmdlet’inin açıklaması, cmdlet’i daha iyi açıklayacak biçimde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-896">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="50143-897">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="50143-897">Az.DataFactory</span></span>
* <span data-ttu-id="50143-898">Yönetilen IR içinde veri akışı çalışma zamanı özelliklerinin CRUD’si desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-898">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="50143-899">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="50143-899">Az.FrontDoor</span></span>
* <span data-ttu-id="50143-900">Front Door Kural Altyapısı nesnesini oluşturmak, güncelleştirmek, almak ve silmek için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-900">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="50143-901">Front Door Kural Altyapısı nesnesini oluşturmak için yardımcı cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-901">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="50143-902">Front Door Yönlendirme Kuralı nesnesine Kural Altyapısı başvurusu eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-902">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="50143-903">Front Door Arka Uç nesnesine Özel Bağlantı parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-903">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="50143-904">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="50143-904">Az.Functions</span></span>
* <span data-ttu-id="50143-905">''Az.Functions'' modülü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="50143-905">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="50143-906">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="50143-906">Az.HDInsight</span></span>
* <span data-ttu-id="50143-907">Müşteri tarafından yönetilen anahtar disk şifrelemesi desteği sunuldu.</span><span class="sxs-lookup"><span data-stu-id="50143-907">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="50143-908">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="50143-908">Az.HealthcareApis</span></span>
* <span data-ttu-id="50143-909">Erişim ilkeleri artık varsayılan olarak geçerli sorumluyu kullanmıyor</span><span class="sxs-lookup"><span data-stu-id="50143-909">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="50143-910">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="50143-910">Az.IotHub</span></span>
* <span data-ttu-id="50143-911">SQL benzeri bir dil kullanarak bilgi almak üzere bir IoT hub’ında sorgu çağırmak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-911">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="50143-912">'Add-AzIotHubDevice' cmdlet’inin alt cihaz olmadan Uç Özellikli Cihaz oluşturamaması sorunu düzeltildi [#11597]</span><span class="sxs-lookup"><span data-stu-id="50143-912">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="50143-913">IoT hub’ı, cihaz veya modül için SAS belirteci oluşturmak üzere cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-913">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="50143-914">Yapılandırma ölçümleri sorgusunu çağırmak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-914">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="50143-915">IoT Edge otomatik dağıtımını büyük ölçekte yönetin.</span><span class="sxs-lookup"><span data-stu-id="50143-915">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="50143-916">Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="50143-916">New cmdlets are:</span></span>
    - <span data-ttu-id="50143-917">'Add-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="50143-917">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="50143-918">'Get-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="50143-918">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="50143-919">'Remove-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="50143-919">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="50143-920">'Set-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="50143-920">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="50143-921">IoT Edge dağıtım ölçümleri sorgusunu çağırmak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-921">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="50143-922">Yapılandırma içeriğini belirtilen uç cihaza uygulamak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-922">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="50143-923">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="50143-923">Az.KeyVault</span></span>
* <span data-ttu-id="50143-924">İki diğer ad kaldırıldı: 'New-AzKeyVaultCertificateAdministratorDetails' ve 'New-AzKeyVaultCertificateOrganizationDetails'</span><span class="sxs-lookup"><span data-stu-id="50143-924">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="50143-925">Anahtar kasası oluştururken varsayılan olarak geçici silme etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-925">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="50143-926">Ağ kuralları, bir anahtar kasası oluştururken belirli ağ konumlarından erişilebilirliği yönetecek şekilde ayarlanabilir</span><span class="sxs-lookup"><span data-stu-id="50143-926">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="50143-927">Kendi anahtarını getir (BYOK) desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-927">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="50143-928">'Add-AzKeyVaultKey' anahtar değişim anahtarı oluşturmayı destekler</span><span class="sxs-lookup"><span data-stu-id="50143-928">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="50143-929">'Get-AzKeyVaultKey' genel bir anahtarı PEM biçiminde indirmeyi destekler</span><span class="sxs-lookup"><span data-stu-id="50143-929">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="50143-930">'Add-AzKeyVaultKey' yardım belgesinin 'KeyOps' bölümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-930">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="50143-931">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="50143-931">Az.Monitor</span></span>
* <span data-ttu-id="50143-932">'Set-AzDiagnosticSettings' için saklama ilkesinin tüm kategorilere uygulanmadığı hata düzeltildi [#11589]</span><span class="sxs-lookup"><span data-stu-id="50143-932">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="50143-933">Ölçüm uyarısı V2 için WebTest kullanılabilirlik ölçütleri desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-933">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="50143-934">'New-AzMetricAlertRuleV2Criteria': Web testi kullanılabilirlik ölçütü oluşturma seçeneği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-934">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="50143-935">'Add-AzMetricAlertRuleV2': Yeni web testi kullanılabilirlik ölçütünü destekler</span><span class="sxs-lookup"><span data-stu-id="50143-935">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="50143-936">PSLogProfile içinde RetentionPolicy için gereksiz tanım kaldırıldı [#7608]</span><span class="sxs-lookup"><span data-stu-id="50143-936">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="50143-937">PSEventData içinde tanımlanan gereksiz özellikler kaldırıldı [#11353]</span><span class="sxs-lookup"><span data-stu-id="50143-937">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="50143-938">'Get-AzLog', 'Get-AzActivityLog' olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="50143-938">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="50143-939">Az.Network</span><span class="sxs-lookup"><span data-stu-id="50143-939">Az.Network</span></span>
* <span data-ttu-id="50143-940">Bölge varsayılan davranışının değiştirileceğini bildirmek için hataya neden olan değişiklik özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-940">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="50143-941">'New-AzPublicIpAddress'</span><span class="sxs-lookup"><span data-stu-id="50143-941">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="50143-942">'New-AzPublicIpPrefix'</span><span class="sxs-lookup"><span data-stu-id="50143-942">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="50143-943">'New-AzLoadBalancerFrontendIpConfig'</span><span class="sxs-lookup"><span data-stu-id="50143-943">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="50143-944">Yeni üst düzey SecurityPartnerProvider kaynağı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-944">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="50143-945">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="50143-945">New cmdlets added:</span></span>
        - <span data-ttu-id="50143-946">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="50143-946">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="50143-947">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="50143-947">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="50143-948">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="50143-948">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="50143-949">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="50143-949">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="50143-950">'PSPrivateLinkResource' üzerinde 'RequiredZoneNames' ve 'PSPrivateEndpointConnection' üzerinde 'GroupId' eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-950">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="50143-951">New-AzNetworkWatcherConnectionMonitorTestConfigurationObject için SuccessThresholdRoundTripTimeMs parametresinin hatalı türü düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-951">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="50143-952">VirtualWan cmdlet’leri AllowVnetToVnetTraffic bağımsız değişkeninin varsayılan değerini True olarak ayarlayacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-952">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="50143-953">'New-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="50143-953">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="50143-954">'Update-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="50143-954">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="50143-955">Özel uç nokta için DNS bölgesi grubunu desteklemek amacıyla yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-955">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="50143-956">'New-AzPrivateDnsZoneConfig'</span><span class="sxs-lookup"><span data-stu-id="50143-956">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="50143-957">'Get-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="50143-957">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="50143-958">'New-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="50143-958">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="50143-959">'Set-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="50143-959">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="50143-960">'Remove-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="50143-960">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="50143-961">'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' ve 'DNSServers' parametreleri 'AzureFirewall' öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-961">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="50143-962">'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' ve 'DnsServer' parametreleri 'AzureFirewall' öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-962">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="50143-963">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="50143-963">Updated cmdlet:</span></span>
        - <span data-ttu-id="50143-964">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="50143-964">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="50143-965">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="50143-965">Az.OperationalInsights</span></span>
* <span data-ttu-id="50143-966">Yeni oluşturulan SDK’yı uygulamak için eski kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-966">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="50143-967">Kullanımdan kaldırılan API’ler nedeniyle silinen cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="50143-967">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="50143-968">'Get-AzOperationalInsightsSavedSearchResult' (diğer adı 'Get-AzOperationalInsightsSavedSearchResults')</span><span class="sxs-lookup"><span data-stu-id="50143-968">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="50143-969">'Get-AzOperationalInsightsSearchResult' (diğer adı 'Get-AzOperationalInsightsSearchResults')</span><span class="sxs-lookup"><span data-stu-id="50143-969">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="50143-970">'Get-AzOperationalInsightsLinkTarget' (diğer adı 'Get-AzOperationalInsightsLinkTargets')</span><span class="sxs-lookup"><span data-stu-id="50143-970">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="50143-971">'Set-AzOperationalInsightsWorkspace' ve 'New-AzOperationalInsightsWorkspace' için parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-971">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="50143-972">Bağlı Depolama Hesabı için cmdlet’ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="50143-972">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="50143-973">Kümeler ve Bağlı Hizmet için cmdlet’ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="50143-973">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="50143-974">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="50143-974">Az.RecoveryServices</span></span>
* <span data-ttu-id="50143-975">Azure Site Recovery’de Azure’dan Azure’a sağlayıcı için yakın yerleştirilen grup sanal makinelerini korumak üzere destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-975">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="50143-976">Azure Site Recovery’de bölgeden bölgeye çoğaltma için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-976">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="50143-977">Azure Backup’ta Azure Dosya Paylaşımı Kurtarma Noktaları için uzun süreli saklama desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-977">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="50143-978">Azure Backup’ta 'Get-AzRecoveryServicesBackupItem' cmdlet’inin çıkışına disk hariç tutma özellikleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-978">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="50143-979">Site Recovery hizmeti için Kasa kimlik bilgilerine yönelik özel uç noktalar eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-979">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="50143-980">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="50143-980">Az.Resources</span></span>
* <span data-ttu-id="50143-981">Yeni bir Rol Tanımı oluşturulurken görüntüleme gecikmesi hakkında ileti uyarısı eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-981">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="50143-982">Kesin tür belirtilmiş nesne çıkışı için ilke cmdlet’leri değiştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-982">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="50143-983">'Get-AzResourceLock' cmdlet’i üzerinde kullanılan '-TenantLevel' parametresi kaldırıldı [#11335]</span><span class="sxs-lookup"><span data-stu-id="50143-983">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="50143-984">'Remove-AzResourceGroup -Id ResourceId' düzeltildi [#9882]</span><span class="sxs-lookup"><span data-stu-id="50143-984">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="50143-985">Kaynak grubu kapsamında ARM şablonu Durum çözümlemesi sonuçlarını almak için yeni cmdlet eklendi: 'Get-AzDeploymentResourceGroupWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="50143-985">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="50143-986">Abonelik kapsamında ARM şablonu Durum çözümlemesi sonuçlarını almak için yeni cmdlet eklendi: 'Get-AzDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="50143-986">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="50143-987">Diğer ad: 'Get-AzSubscriptionDeploymentWhatIf'</span><span class="sxs-lookup"><span data-stu-id="50143-987">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="50143-988">'New-AzDeployment' ve 'New-AzResourceGroupDeployment' için '-WhatIf' ve '-Confirm' parametreleri ARM şablonu Durum sonuçlarını kullanmak için geçersiz kılındı</span><span class="sxs-lookup"><span data-stu-id="50143-988">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="50143-989">Dağıtım cmdlet’lerinde 'ApiVersion' parametresi için kullanımdan kaldırma iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-989">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="50143-990">Dağıtım hataları için iyileştirilmiş hata iletilerini gösterme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-990">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="50143-991">Dağıtım hataları için correlationId’yi günlüğe kaydetme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-991">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="50143-992">Dağıtım betiği çıkışına 'error' özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-992">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="50143-993">NuGet Microsoft.Azure.Management.ResourceManager '3.7.1-preview' sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-993">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="50143-994">DeploymentValidateResult içindeki Error özelliği nuget 3.7.1-preview sürümünden itibaren salt okunur olarak değiştirildiğinden belirli test çalışmaları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="50143-994">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="50143-995">SDK ResourceManager 3.7.1-preview sürümünden GenericResourceExpanded öğesi getirildi</span><span class="sxs-lookup"><span data-stu-id="50143-995">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="50143-996">Dağıtım için tüm Get cmdlet’lerine yönelik etiket desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-996">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="50143-997">'New-AzDeployment'</span><span class="sxs-lookup"><span data-stu-id="50143-997">'New-AzDeployment'</span></span>
    - <span data-ttu-id="50143-998">'New-AzManagementGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="50143-998">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="50143-999">'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="50143-999">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="50143-1000">'New-AzTenantDeployment'</span><span class="sxs-lookup"><span data-stu-id="50143-1000">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="50143-1001">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="50143-1001">Az.ServiceFabric</span></span>
* <span data-ttu-id="50143-1002">Yanlış sertifika parmak izini alan --SecretIdentifier parametresini kullanarak sertifika ekleme özelliğindeki hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-1002">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="50143-1003">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="50143-1003">Az.Sql</span></span>
* <span data-ttu-id="50143-1004">Şunların performansı iyileştirildi:</span><span class="sxs-lookup"><span data-stu-id="50143-1004">Enhance performance of:</span></span>
    - <span data-ttu-id="50143-1005">'Set-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="50143-1005">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="50143-1006">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="50143-1006">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="50143-1007">'Remove-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="50143-1007">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="50143-1008">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="50143-1008">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="50143-1009">'Enable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="50143-1009">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="50143-1010">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="50143-1010">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="50143-1011">'Disable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="50143-1011">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="50143-1012">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="50143-1012">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="50143-1013">'Set-AzSqlDatabaseBackupShortTermRetentionPolicy' cmdlet’inden 'RetentionDays' parametresinin istemci tarafı doğrulaması kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="50143-1013">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="50143-1014">Sanal ağ içindeki bir depolama hesabına denetim yapılarak Depolama Blob Verileri Katkıda Bulunan rolünün oluşturulması sırasında karşılaşılan hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-1014">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="50143-1015">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="50143-1015">Az.Storage</span></span>
* <span data-ttu-id="50143-1016">'Get-AzStorageAccount' hesap alma/listeleme cmdlet’ine '-AsJob' eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1016">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="50143-1017">Anahtar otomatik döndürmesini desteklemek için Depolama hesabı KeyvaultEncryption ile güncelleştirilirken KeyVersion isteğe bağlı hale getirildi</span><span class="sxs-lookup"><span data-stu-id="50143-1017">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="50143-1018">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="50143-1018">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="50143-1019">İşlem hattıyla Azure Dosya Dizinini kaldırma hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-1019">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="50143-1020">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="50143-1020">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="50143-1021">Düzeltildi [#9880]: NetWorkRule DefaultAction değer tanımı swagger ile uyumlu olacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-1021">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="50143-1022">'Update-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="50143-1022">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="50143-1023">'Get-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="50143-1023">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="50143-1024">Düzeltildi [#11624]: Sunucu hatasından kaçınmak için NetworkRules eklenirken yinelenen kuralları atla</span><span class="sxs-lookup"><span data-stu-id="50143-1024">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="50143-1025">'Add-AzStorageAccountNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="50143-1025">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="50143-1026">Microsoft.Azure.Cosmos.Table SDK 1.0.7 sürümüne yükseltildi</span><span class="sxs-lookup"><span data-stu-id="50143-1026">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="50143-1027">DataLake 2. Nesil Öğeleri listesinde yalnızca bazı öğeler döndürüldüğünde kullanıcıya ContinuationToken ile yeniden listelemesini anımsatmak için uyarı iletisi eklendi,</span><span class="sxs-lookup"><span data-stu-id="50143-1027">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="50143-1028">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="50143-1028">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="50143-1029">Azure Dosyalar Active Directory Domain Services Kimlik Doğrulaması ile Depolama hesabı oluşturma veya güncelleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1029">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="50143-1030">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="50143-1030">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="50143-1031">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="50143-1031">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="50143-1032">Depolama hesabının Kerberos anahtarlarını yeni oluşturma veya listeleme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1032">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="50143-1033">'New-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="50143-1033">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="50143-1034">'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="50143-1034">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="50143-1035">Yük devretme Depolama hesabı desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1035">Supported failover Storage account</span></span>
    - <span data-ttu-id="50143-1036">'Invoke-AzStorageAccountFailover'</span><span class="sxs-lookup"><span data-stu-id="50143-1036">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="50143-1037">'Get-AzStorageBlobCopyState' yardımı güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-1037">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="50143-1038">'Get-AzStorageFileCopyState' ve 'Start-AzStorageBlobCopy' yardımı güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-1038">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="50143-1039">Depolama istemci kitaplığı v12, Kuyruk ve Dosya cmdlet’leriyle tümleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-1039">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="50143-1040">CloudFile olan çıkış türü AzureStorageFile olarak değiştirildi, özgün çıkış yeni çıkışın bir alt özelliği olacak</span><span class="sxs-lookup"><span data-stu-id="50143-1040">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="50143-1041">'Get-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="50143-1041">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="50143-1042">'Remove-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="50143-1042">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="50143-1043">'Get-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="50143-1043">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="50143-1044">'Set-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="50143-1044">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="50143-1045">'Start-AzStorageFileCopy'</span><span class="sxs-lookup"><span data-stu-id="50143-1045">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="50143-1046">CloudFileDirectory olan çıkış türü AzureStorageFileDirectory olarak değiştirildi, özgün çıkış yeni çıkışın bir alt özelliği olacak</span><span class="sxs-lookup"><span data-stu-id="50143-1046">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="50143-1047">'New-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="50143-1047">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="50143-1048">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="50143-1048">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="50143-1049">CloudFileShare olan çıkış türü AzureStorageFileShare olarak değiştirildi, özgün çıkış yeni çıkışın bir alt özelliği olacak</span><span class="sxs-lookup"><span data-stu-id="50143-1049">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="50143-1050">'Get-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="50143-1050">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="50143-1051">'New-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="50143-1051">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="50143-1052">'Remove-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="50143-1052">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="50143-1053">FileShareProperties olan çıkış türü AzureStorageFileShare olarak değiştirildi, özgün çıkış yeni çıkışın bir alt alt özelliği olacak</span><span class="sxs-lookup"><span data-stu-id="50143-1053">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="50143-1054">'Set-AzStorageShareQuota'</span><span class="sxs-lookup"><span data-stu-id="50143-1054">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="50143-1055">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="50143-1055">Az.TrafficManager</span></span>
* <span data-ttu-id="50143-1056">'DisableAzureTrafficManagerEndpoint' ayrıntılı çıkışındaki hatalı profil adı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-1056">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="50143-1057">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="50143-1057">Az.Websites</span></span>
* <span data-ttu-id="50143-1058">'Update-AzWebAppAccessRestrictionConfig' yardımındaki yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-1058">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="50143-1059">3.8.0 - Nisan 2020</span><span class="sxs-lookup"><span data-stu-id="50143-1059">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="50143-1060">Son sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="50143-1060">Highlights since the last release</span></span>
* <span data-ttu-id="50143-1061">Az.Storage’ın desteklediği PowerShell sürümleri: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="50143-1061">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="50143-1062">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="50143-1062">Az.Accounts</span></span>
* <span data-ttu-id="50143-1063">'Resolve-AzError' içinde Azure PowerShell anket URL’si güncelleştirildi [#11507]</span><span class="sxs-lookup"><span data-stu-id="50143-1063">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="50143-1064">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="50143-1064">Az.ApiManagement</span></span>
* <span data-ttu-id="50143-1065">Sonraki sürümlerde Azure Dosya cmdlet’leri için hataya neden olan değişiklik bildirimi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1065">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="50143-1066">'Set-AzApiManagementGroup' belgeleri GroupId parametresini belirtmek için güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-1066">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="50143-1067">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="50143-1067">Az.Cdn</span></span>
* <span data-ttu-id="50143-1068">ChinaCDN ile ilgili fiyatlandırma SKU’nun görüntüsü düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-1068">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="50143-1069">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="50143-1069">Az.CognitiveServices</span></span>
* <span data-ttu-id="50143-1070">Kimlik, Şifreleme, UserOwnedStorage desteği sağlandı</span><span class="sxs-lookup"><span data-stu-id="50143-1070">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="50143-1071">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="50143-1071">Az.Compute</span></span>
* <span data-ttu-id="50143-1072">'Set-AzVmssOrchestrationServiceState' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-1072">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="50143-1073">-InstanceView ile 'Get-AzVmss', OrchestrationService durumlarını gösteriyor.</span><span class="sxs-lookup"><span data-stu-id="50143-1073">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="50143-1074">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="50143-1074">Az.IotHub</span></span>
* <span data-ttu-id="50143-1075">IoT cihaz ikizi yapılandırmasını yönetme, Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="50143-1075">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="50143-1076">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="50143-1076">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="50143-1077">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="50143-1077">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="50143-1078">IoT Hub’ındaki bir cihazda doğrudan yöntem çağırmak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-1078">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="50143-1079">IoT cihaz modülü ikizi yapılandırmasını yönetme, Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="50143-1079">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="50143-1080">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="50143-1080">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="50143-1081">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="50143-1081">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="50143-1082">Büyük ölçekte IoT otomatik cihaz yönetimi yapılandırmasını yönetin.</span><span class="sxs-lookup"><span data-stu-id="50143-1082">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="50143-1083">Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="50143-1083">New cmdlets are:</span></span>
    - <span data-ttu-id="50143-1084">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="50143-1084">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="50143-1085">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="50143-1085">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="50143-1086">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="50143-1086">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="50143-1087">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="50143-1087">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="50143-1088">Bir IoT Hub’ında kenar modülü yöntemini çağırmak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-1088">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="50143-1089">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="50143-1089">Az.KeyVault</span></span>
* <span data-ttu-id="50143-1090">Bir kasada geçici silme ve temizleme korumasını etkinleştirebilen yeni bir 'Update-AzKeyVault' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1090">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="50143-1091">Microsoft.PowerShell.SecretManagement desteği eklendi [#11178]</span><span class="sxs-lookup"><span data-stu-id="50143-1091">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="50143-1092">'Remove-AzKeyVaultManagedStorageSasDefinition' örneklerindeki hata düzeltildi [#11479]</span><span class="sxs-lookup"><span data-stu-id="50143-1092">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="50143-1093">Özel uç noktaya destek eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1093">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="50143-1094">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="50143-1094">Az.Maintenance</span></span>
* <span data-ttu-id="50143-1095">GA için Bakım cmdlet’lerinin yayın sürümü yayımlanıyor</span><span class="sxs-lookup"><span data-stu-id="50143-1095">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="50143-1096">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="50143-1096">Az.Monitor</span></span>
* <span data-ttu-id="50143-1097">Özel bağlantı kapsamı için cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1097">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="50143-1098">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="50143-1098">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="50143-1099">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="50143-1099">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="50143-1100">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="50143-1100">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="50143-1101">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="50143-1101">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="50143-1102">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="50143-1102">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="50143-1103">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="50143-1103">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="50143-1104">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="50143-1104">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="50143-1105">Az.Network</span><span class="sxs-lookup"><span data-stu-id="50143-1105">Az.Network</span></span>
* <span data-ttu-id="50143-1106">Sanal Ağ Geçidi için özel IP’de bağlantıyı etkinleştirmek üzere cmdlet’ler güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-1106">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="50143-1107">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="50143-1107">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="50143-1108">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="50143-1108">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="50143-1109">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="50143-1109">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="50143-1110">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="50143-1110">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="50143-1111">FQDN tabanlı LocalNetworkGateways ve VpnSites’ı etkinleştirmek için cmdlet’ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-1111">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="50143-1112">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="50143-1112">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="50143-1113">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="50143-1113">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="50143-1114">ExpressRouteCircuitConnectionConfig (Global Reach) içinde IPv6 adres ailesi için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1114">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="50143-1115">'Set-AzExpressRouteCircuitConnectionConfig' eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1115">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="50143-1116">IPv6CircuitConnectionProperties dahil tüm mevcut özelliklerin ayarlanmasına olanak sağlar</span><span class="sxs-lookup"><span data-stu-id="50143-1116">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="50143-1117">'Add-AzExpressRouteCircuitConnectionConfig' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-1117">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="50143-1118">Adres ön ekinin adres ailesini belirtmek için başka bir isteğe bağlı AddressPrefixType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1118">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="50143-1119">Sanal Ağ Geçidi Bağlantılarında DPD Zaman Aşımı ayarlanmasını sağlamak için cmdlet’ler güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-1119">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="50143-1120">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="50143-1120">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="50143-1121">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="50143-1121">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="50143-1122">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="50143-1122">Az.PolicyInsights</span></span>
* <span data-ttu-id="50143-1123">İlke uyumluluğu taramalarını tetiklemek için 'Start-AzPolicyComplianceScan' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1123">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="50143-1124">'Get-AzPolicyState' çıkışına ilke tanımı, küme tanımı ve atama sürümleri eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1124">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="50143-1125">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="50143-1125">Az.ServiceFabric</span></span>
* <span data-ttu-id="50143-1126">'New-AzServiceFabricCluster' örneklerinin kod biçimlendirmesi ve kullanılabilirliği iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-1126">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="50143-1127">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="50143-1127">Az.Sql</span></span>
* <span data-ttu-id="50143-1128">'Get-AzSqlInstanceOperation' ve 'Stop-AzSqlInstanceOperation' cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1128">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="50143-1129">Sanal ağdaki bir depolama hesabının denetlenmesine yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-1129">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="50143-1130">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="50143-1130">Az.Storage</span></span>
* <span data-ttu-id="50143-1131">Sonraki sürümlerde Azure Dosya cmdlet’leri için hataya neden olan değişiklik bildirimi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1131">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="50143-1132">Depolama hesabı oluşturma/güncelleştirme sırasında yeni SkuName StandardGZRS, StandardRAGZRS desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1132">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="50143-1133">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="50143-1133">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="50143-1134">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="50143-1134">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="50143-1135">DataLake Gen2 desteklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1135">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="50143-1136">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="50143-1136">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="50143-1137">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="50143-1137">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="50143-1138">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="50143-1138">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="50143-1139">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="50143-1139">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="50143-1140">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="50143-1140">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="50143-1141">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="50143-1141">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="50143-1142">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="50143-1142">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="50143-1143">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="50143-1143">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="50143-1144">0.10.0-preview - Nisan 2020</span><span class="sxs-lookup"><span data-stu-id="50143-1144">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="50143-1145">Genel</span><span class="sxs-lookup"><span data-stu-id="50143-1145">General</span></span>
* <span data-ttu-id="50143-1146">Az modülleri artık Azure Stack Hub’da önizlemede kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="50143-1146">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="50143-1147">Bu, Linux ve macOs ile platformlar arası uyumluluk sağlar.</span><span class="sxs-lookup"><span data-stu-id="50143-1147">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="50143-1148">Azure Stack Hub artık Az modülleriyle PowerShell Core’u destekliyor, daha fazla bilgiyi [burada](https://aka.ms/az4AzureStack) bulabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="50143-1148">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="50143-1149">Az modülleri profil 2019-03-01-hybrid’i destekliyor:</span><span class="sxs-lookup"><span data-stu-id="50143-1149">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="50143-1150">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="50143-1150">Az.Billing</span></span>
  - <span data-ttu-id="50143-1151">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="50143-1151">Az.Compute</span></span>
  - <span data-ttu-id="50143-1152">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="50143-1152">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="50143-1153">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="50143-1153">Az.EventHub</span></span>
  - <span data-ttu-id="50143-1154">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="50143-1154">Az.IotHub</span></span>
  - <span data-ttu-id="50143-1155">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="50143-1155">Az.KeyVault</span></span>
  - <span data-ttu-id="50143-1156">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="50143-1156">Az.Monitor</span></span>
  - <span data-ttu-id="50143-1157">Az.Network</span><span class="sxs-lookup"><span data-stu-id="50143-1157">Az.Network</span></span>
  - <span data-ttu-id="50143-1158">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="50143-1158">Az.Resources</span></span>
  - <span data-ttu-id="50143-1159">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="50143-1159">Az.Storage</span></span>
  - <span data-ttu-id="50143-1160">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="50143-1160">Az.Websites</span></span>
* <span data-ttu-id="50143-1161">Az için Azure Stack Hub ile çalışan üç yeni PowerShell modülü (Az.Databox, Az.IotHub ve Az.EventHub) kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="50143-1161">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="50143-1162">Komutlar, AzureRM’nin Az olarak değiştirilmesi gibi küçük değişiklikler ile görece aynı kalır</span><span class="sxs-lookup"><span data-stu-id="50143-1162">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="50143-1163">Azure Stack Hub için PowerShell belgelerine güncelleştirilmiş bağlantı [burada](https://aka.ms/InstallASHPowerShell) bulunabilir</span><span class="sxs-lookup"><span data-stu-id="50143-1163">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="50143-1164">3.7.0 - Mart 2020</span><span class="sxs-lookup"><span data-stu-id="50143-1164">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="50143-1165">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="50143-1165">Az.Accounts</span></span>
* <span data-ttu-id="50143-1166">Oturum açılmadığında ‘Get-AzTenant’/’Get-AzDefault’/’Set-AzDefault’ cmdlet’lerinin NullReferenceException hatası oluşturması düzeltildi [#10292]</span><span class="sxs-lookup"><span data-stu-id="50143-1166">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="50143-1167">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="50143-1167">Az.Compute</span></span>
* <span data-ttu-id="50143-1168">‘New-AzDiskConfig’ cmdlet’ine şu parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="50143-1168">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="50143-1169">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="50143-1169">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="50143-1170">Şifreleme özelliğinin ‘New-AzGalleryImageVersion’ cmdlet’inin parametrelerini hedeflemesine izin verildi.</span><span class="sxs-lookup"><span data-stu-id="50143-1170">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="50143-1171">‘Set-AzVmss’ -Reimage ve ‘Invoke-AzVMReimage’ cmdlet’lerine yönelik tempDisk sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-1171">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="50143-1172">[#11354]</span><span class="sxs-lookup"><span data-stu-id="50143-1172">[#11354]</span></span>
* <span data-ttu-id="50143-1173">Aşağıdaki cmdlet’lere yeni SAP uzantısına yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1173">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="50143-1174">‘Set-AzVMAEMExtension’</span><span class="sxs-lookup"><span data-stu-id="50143-1174">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="50143-1175">‘Get-AzVMAEMExtension’</span><span class="sxs-lookup"><span data-stu-id="50143-1175">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="50143-1176">‘Remove-AzVMAEMExtension’</span><span class="sxs-lookup"><span data-stu-id="50143-1176">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="50143-1177">‘Update-AzVMAEMExtension’</span><span class="sxs-lookup"><span data-stu-id="50143-1177">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="50143-1178">Yardım belgelerinde bulunan örneklerdeki hatalar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-1178">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="50143-1179">VM PowerState için tam dize değeri tablo biçiminde gösterildi.</span><span class="sxs-lookup"><span data-stu-id="50143-1179">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="50143-1180">‘New-AzVmssConfig’: SinglePlacementGroup devre dışı bırakıldığında AutomaticRepairs özelliğinin serileştirilmesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-1180">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="50143-1181">[#11257]</span><span class="sxs-lookup"><span data-stu-id="50143-1181">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="50143-1182">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="50143-1182">Az.DataFactory</span></span>
* <span data-ttu-id="50143-1183">ADF .NET SDK’sı 4.8.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-1183">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="50143-1184">Yeniden çalıştırmayı desteklemek için ‘Invoke-AzDataFactoryV2Pipeline’ komutuna isteğe bağlı parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1184">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="50143-1185">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="50143-1185">Az.DataLakeStore</span></span>
* <span data-ttu-id="50143-1186">‘Export-AzDataLakeStoreItem’ ve ‘Import-AzDataLakeStoreItem’ için hataya neden olan değişiklik açıklaması eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1186">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="50143-1187">‘New-AzDataLakeStoreItem’, ‘Add-AzDAtaLakeStoreItemContent’ ve ‘Get-AzDAtaLakeStoreItemContent’ için Bayt kodlaması seçeneği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1187">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="50143-1188">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="50143-1188">Az.HDInsight</span></span>
* <span data-ttu-id="50143-1189">Küme oluştururken TLS sürümünün desteklenen en düşük sürümünün belirtilmesine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1189">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="50143-1190">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="50143-1190">Az.IotHub</span></span>
* <span data-ttu-id="50143-1191">Cihaz başına dağıtılmış ayarları yönetmeye yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-1191">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="50143-1192">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="50143-1192">New Cmdlets are:</span></span>
    - <span data-ttu-id="50143-1193">‘Get-AzIotHubDistributedTracing’</span><span class="sxs-lookup"><span data-stu-id="50143-1193">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="50143-1194">‘Set-AzIotHubDistributedTracing’</span><span class="sxs-lookup"><span data-stu-id="50143-1194">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="50143-1195">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="50143-1195">Az.KeyVault</span></span>
* <span data-ttu-id="50143-1196">‘New-AzKeyVault’ cmdlet’ine hataya neden olan değişiklik öznitelikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1196">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="50143-1197">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="50143-1197">Az.Monitor</span></span>
* <span data-ttu-id="50143-1198">‘New-AzScheduledQueryRuleLogMetricTrigger’ cmdlet’ine yönelik belgeler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-1198">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="50143-1199">Az.Network</span><span class="sxs-lookup"><span data-stu-id="50143-1199">Az.Network</span></span>
* <span data-ttu-id="50143-1200">Kiracılar arası VirtualHubVnetConnections kurulmasına olanak tanımak için cmdlet’ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-1200">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="50143-1201">‘New-AzVirtualHubVnetConnection’</span><span class="sxs-lookup"><span data-stu-id="50143-1201">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="50143-1202">‘Update-AzVirtualHubVnetConnection’</span><span class="sxs-lookup"><span data-stu-id="50143-1202">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="50143-1203">‘New-AzVirtualHub’</span><span class="sxs-lookup"><span data-stu-id="50143-1203">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="50143-1204">‘Update-AzVirtualHub’</span><span class="sxs-lookup"><span data-stu-id="50143-1204">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="50143-1205">SQL Yönetim SDK’sı bağımlılığı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="50143-1205">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="50143-1206">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="50143-1206">Az.PolicyInsights</span></span>
* <span data-ttu-id="50143-1207">Hata iletileri iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-1207">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="50143-1208">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="50143-1208">Az.RecoveryServices</span></span>
* <span data-ttu-id="50143-1209">Azure Site Recovery’de, Azure disk tarafından şifrelenmiş Sanal Makinelere yönelik VM özellikleri güncelleştirildi ve yeniden koruma gerçekleştirmeye yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-1209">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="50143-1210">Azure Site Recovery VmwareToAzure DR izleme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1210">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="50143-1211">Başarısız öğeler için ilke güncelleştirmesini yeniden deneme özelliğine yönelik destek Azure Backup’a eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-1211">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="50143-1212">Yedekleme ve geri yükleme işlemleri sırasında disk dışlaması ayarını kullanmaya yönelik destek Azure Backup’a eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-1212">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="50143-1213">AzureFileShare’den birden fazla dosyayı/klasörü geri yüklemeye yönelik destek Azure Backup’a eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1213">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="50143-1214">IaasVM İlkesini güncelleştirilirken kullanıcı tarafından belirtilen Resourcegroup desteğine yönelik destek Azure Backup’a eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1214">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="50143-1215">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="50143-1215">Az.Resources</span></span>
* <span data-ttu-id="50143-1216">‘Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType’ komutlarındaki bir hata düzeltildi ve bunların varsayılan apiVersion yerine kaynakların asıl apiVersion’unu kullanması sağlandı [#11267]</span><span class="sxs-lookup"><span data-stu-id="50143-1216">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="50143-1217">Hata senaryoları için correlationId’yi günlüğe kaydetme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1217">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="50143-1218">‘Get-AzResourceLock’ cmdlet’inde küçük bir belge değişikliği yapıldı.</span><span class="sxs-lookup"><span data-stu-id="50143-1218">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="50143-1219">Örnek eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-1219">Added example.</span></span>
* <span data-ttu-id="50143-1220">‘Get-AzADUser’ cmdlet’inin parametre değerinde tek tırnak işaretinin atlanması [#11317]</span><span class="sxs-lookup"><span data-stu-id="50143-1220">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="50143-1221">Dağıtım Betikleri için yeni cmdlet’ler eklendi (‘Get-AzDeploymentScript’, ‘Get-AzDeploymentScriptLog’, ‘Save-AzDeploymentScriptLog’ ve ‘Remove-AzDeploymentScript’)</span><span class="sxs-lookup"><span data-stu-id="50143-1221">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="50143-1222">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="50143-1222">Az.Sql</span></span>
* <span data-ttu-id="50143-1223">‘Invoke-AzSqlDatabaseFailover’ cmdlet’ine okunabilir ikincil parametre eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1223">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="50143-1224">‘Disable-AzSqlServerActiveDirectoryOnlyAuthentication’ cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1224">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="50143-1225">Veritabanındaki sütunlar sınıflandırılırken duyarlılık derecesi kaydedildi.</span><span class="sxs-lookup"><span data-stu-id="50143-1225">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="50143-1226">Az.Support</span><span class="sxs-lookup"><span data-stu-id="50143-1226">Az.Support</span></span>
* <span data-ttu-id="50143-1227">‘Az.Support’ modülü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="50143-1227">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="50143-1228">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="50143-1228">Az.Websites</span></span>
* <span data-ttu-id="50143-1229">Aşağıdaki yeni cmdlet’leri kullanarak Trafik Yönlendirme Kurallarıyla çalışmaya yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-1229">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="50143-1230">‘Get-AzWebAppTrafficRouting’</span><span class="sxs-lookup"><span data-stu-id="50143-1230">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="50143-1231">‘Update-AzWebAppTrafficRouting’</span><span class="sxs-lookup"><span data-stu-id="50143-1231">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="50143-1232">‘Add-AzWebAppTrafficRouting’</span><span class="sxs-lookup"><span data-stu-id="50143-1232">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="50143-1233">‘Remove-AzWebAppTrafficRouting’</span><span class="sxs-lookup"><span data-stu-id="50143-1233">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="50143-1234">3.6.1 - Mart 2020</span><span class="sxs-lookup"><span data-stu-id="50143-1234">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="50143-1235">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="50143-1235">Az.Accounts</span></span>
* <span data-ttu-id="50143-1236">'Send-Feedback' içinde Azure PowerShell anket sayfasını açma [#11020]</span><span class="sxs-lookup"><span data-stu-id="50143-1236">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="50143-1237">'Resolve-Error' içinde Azure PowerShell anket URL’sini görüntüleme [#11021]</span><span class="sxs-lookup"><span data-stu-id="50143-1237">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="50143-1238">UserAgent’ta Az sürümü eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1238">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="50143-1239">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="50143-1239">Az.ApiManagement</span></span>
* <span data-ttu-id="50143-1240">DeveloperPortal Uç Noktasında Özel Etki Alanını alma ve yapılandırma desteği eklendi [#11007]</span><span class="sxs-lookup"><span data-stu-id="50143-1240">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="50143-1241">'Export-AzApiManagementApi' içinde Api Tanımını Json biçiminde indirme desteği eklendi [#9987]</span><span class="sxs-lookup"><span data-stu-id="50143-1241">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="50143-1242">'Import-AzApiManagementApi' içinde OpenApi 3.0 tanımını Json belgesinden içeri aktarma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1242">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="50143-1243">'New-AzApiManagementIdentityProvider' ve 'Set-AzApiManagementIdentityProvider' içinde AAD B2C Sağlayıcısı için 'Oturum Açan Kiracı' yapılandırma desteği eklendi [#9784]</span><span class="sxs-lookup"><span data-stu-id="50143-1243">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="50143-1244">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="50143-1244">Az.DataLakeStore</span></span>
* <span data-ttu-id="50143-1245">csproj ve psd1 içinde System.Buffers öğesine açık başvuru eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-1245">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="50143-1246">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="50143-1246">Az.IotHub</span></span>
* <span data-ttu-id="50143-1247">Iot Hub’daki cihazları yönetmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-1247">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="50143-1248">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="50143-1248">New Cmdlets are:</span></span>
    - <span data-ttu-id="50143-1249">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="50143-1249">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="50143-1250">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="50143-1250">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="50143-1251">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="50143-1251">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="50143-1252">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="50143-1252">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="50143-1253">IoT hub’ındaki hedef IoT cihazında modülleri yönetmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-1253">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="50143-1254">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="50143-1254">New Cmdlets are:</span></span>
    - <span data-ttu-id="50143-1255">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="50143-1255">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="50143-1256">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="50143-1256">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="50143-1257">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="50143-1257">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="50143-1258">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="50143-1258">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="50143-1259">Bir IoT hub’ında hedef IoT cihazının bağlantı dizesini almak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-1259">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="50143-1260">Bir IoT hub’ında hedef IoT cihazındaki modülün bağlantı dizesini almak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-1260">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="50143-1261">IoT cihazının üst cihazını almak/ayarlamak için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-1261">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="50143-1262">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="50143-1262">New Cmdlets are:</span></span>
    - <span data-ttu-id="50143-1263">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="50143-1263">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="50143-1264">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="50143-1264">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="50143-1265">Cihaz üst-alt ilişkisinin yönetilmesi için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-1265">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="50143-1266">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="50143-1266">Az.Monitor</span></span>
* <span data-ttu-id="50143-1267">'Get-AzMetricDefinition' için çıkış değeri düzeltildi [#9714]</span><span class="sxs-lookup"><span data-stu-id="50143-1267">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="50143-1268">Az.Network</span><span class="sxs-lookup"><span data-stu-id="50143-1268">Az.Network</span></span>
* <span data-ttu-id="50143-1269">SQL Yönetim SDK’sı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-1269">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="50143-1270">PrivateLinkServiceConnectionState sınıfındaki bir adlandırma farkı sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-1270">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="50143-1271">ActionsRequired alanı ActionRequired alanına eşleniyor.</span><span class="sxs-lookup"><span data-stu-id="50143-1271">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="50143-1272">'New-AzSqlServer' ve 'Set-AzSqlServer' için PublicNetworkAccess eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1272">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="50143-1273">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="50143-1273">Az.Resources</span></span>
* <span data-ttu-id="50143-1274">'Get-AzRoleAssignment' içindeki null başvuru hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-1274">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="50143-1275">'-Force' ve '-PassThru' anahtarı 'Remove-AzADGroup' içinde isteğe bağlı olarak işaretlendi [#10849]</span><span class="sxs-lookup"><span data-stu-id="50143-1275">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="50143-1276">'MailNickname' öğesinin 'Remove-AzADGroup' içinde döndürülmemesi sorunu düzeltildi [#11167]</span><span class="sxs-lookup"><span data-stu-id="50143-1276">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="50143-1277">'Remove-AzADGroup' kanal oluşturma işleminin çalışmaması sorunu düzeltildi [#11171]</span><span class="sxs-lookup"><span data-stu-id="50143-1277">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="50143-1278">GetAzureRoleAssignmentCommand içinde null başvuru hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-1278">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="50143-1279">İlke cmdlet’lerinde yaklaşan değişiklikler için hataya neden olan değişiklik öznitelikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1279">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="50143-1280">'Get-AzResourceGroup' sunucu tarafında kaynak grubu etiket filtreleme gerçekleştirmek için güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-1280">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="50143-1281">Tag cmdlet’leri -ResourceId öğesini kabul edecek şekilde genişletildi</span><span class="sxs-lookup"><span data-stu-id="50143-1281">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="50143-1282">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="50143-1282">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="50143-1283">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="50143-1283">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="50143-1284">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="50143-1284">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="50143-1285">Yeni Tag cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1285">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="50143-1286">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="50143-1286">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="50143-1287">SDK 3.3.0 sürümünden ScopedDeployment getirildi</span><span class="sxs-lookup"><span data-stu-id="50143-1287">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="50143-1288">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="50143-1288">Az.Sql</span></span>
* <span data-ttu-id="50143-1289">'New-AzSqlServer' ve 'Set-AzSqlServer' için PublicNetworkAccess eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1289">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="50143-1290">Yönetilen Veritabanları için Uzun Süreli Saklamalı yedekleme yapılandırması desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1290">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="50143-1291">Yönetilen bir veritabanında LTR ilkesini alma/ayarlama</span><span class="sxs-lookup"><span data-stu-id="50143-1291">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="50143-1292">Yönetilen veritabanı, yönetilen örnek veya konuma göre LTR yedeklemelerini alma</span><span class="sxs-lookup"><span data-stu-id="50143-1292">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="50143-1293">Bir LTR yedeklemesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="50143-1293">Remove an LTR backup</span></span>
    - <span data-ttu-id="50143-1294">Yeni yönetilen veritabanı oluşturmak için LTR yedeklemesini geri yükleme</span><span class="sxs-lookup"><span data-stu-id="50143-1294">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="50143-1295">New-AzSqlServer ve Set-AzSqlServer için MinimalTlsVersion eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1295">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="50143-1296">New-AzSqlInstance ve Set-AzSqlInstance için MinimalTlsVersion eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1296">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="50143-1297">Az.Network için SQL SDK sürümü artırıldı</span><span class="sxs-lookup"><span data-stu-id="50143-1297">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="50143-1298">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="50143-1298">Az.Storage</span></span>
* <span data-ttu-id="50143-1299">ImmutabilityPolicy içinde AllowProtectedAppendWrite desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1299">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="50143-1300">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="50143-1300">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="50143-1301">Gelecekteki bir yayın için AzureStorageTable tür değişikliğine yönelik hataya neden olan değişiklik uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1301">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="50143-1302">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="50143-1302">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="50143-1303">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="50143-1303">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="50143-1304">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="50143-1304">Az.Websites</span></span>
* <span data-ttu-id="50143-1305">'New-AzAppServicePlan' ve 'Set-AzAppServicePlan' için Etiket parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1305">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="50143-1306">Özel etki alanı bir web sitesine eklenirken özel durum oluşturulursa cmdlet’i yürütmeyi durdur</span><span class="sxs-lookup"><span data-stu-id="50143-1306">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="50143-1307">App Service Planıyla aynı kaynak grubunda bulunmayan Uygulama Hizmetleri için işlem gerçekleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1307">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="50143-1308">Farklı kaynak gruplarındaki WebApp/İşlev öğesine erişim kısıtlaması uygulandı</span><span class="sxs-lookup"><span data-stu-id="50143-1308">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="50143-1309">WebAppSlots için özel ana bilgisayar adları ayarlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-1309">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="50143-1310">3.5.0 - Şubat 2020</span><span class="sxs-lookup"><span data-stu-id="50143-1310">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="50143-1311">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="50143-1311">Highlights since the last major release</span></span>
* <span data-ttu-id="50143-1312">İstemci tarafı telemetri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-1312">Updated client side telemetry.</span></span>
* <span data-ttu-id="50143-1313">Cihaz yönetimini desteklemek için Az.IotHub cmdlet’leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-1313">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="50143-1314">Kullanılabilirlik Grubu Dinleyicisi için Az.SqlVirtualMachine cmdlet’leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-1314">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="50143-1315">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="50143-1315">Az.Accounts</span></span>
* <span data-ttu-id="50143-1316">İstemci tarafı telemetri verilerine SubscriptionId, TenantId ve yürütme zamanı eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1316">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="50143-1317">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="50143-1317">Az.Automation</span></span>
* <span data-ttu-id="50143-1318">'New-AzAutomationSoftwareUpdateConfiguration' için başvuru belgelerinde Örnek 1’deki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-1318">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="50143-1319">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="50143-1319">Az.CognitiveServices</span></span>
* <span data-ttu-id="50143-1320">SDK 7.0 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-1320">Updated SDK to 7.0</span></span>
* <span data-ttu-id="50143-1321">Sunucu yanıtları boş gövde olduğunda alınan hata iletisi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-1321">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="50143-1322">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="50143-1322">Az.Compute</span></span>
* <span data-ttu-id="50143-1323">Güncelleştirme sırasında ProximityPlacementGroupId için boş değere izin verildi</span><span class="sxs-lookup"><span data-stu-id="50143-1323">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="50143-1324">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="50143-1324">Az.FrontDoor</span></span>
* <span data-ttu-id="50143-1325">WAF’de kullanılabilen yönetilen kural tanımlarını almak için cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1325">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="50143-1326">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="50143-1326">Az.IotHub</span></span>
* <span data-ttu-id="50143-1327">Iot Hub’daki cihazları yönetmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-1327">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="50143-1328">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="50143-1328">New Cmdlets are:</span></span>
    - <span data-ttu-id="50143-1329">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="50143-1329">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="50143-1330">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="50143-1330">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="50143-1331">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="50143-1331">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="50143-1332">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="50143-1332">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="50143-1333">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="50143-1333">Az.KeyVault</span></span>
* <span data-ttu-id="50143-1334">Add-AzKeyVaultKey.md için yinelenen metin düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-1334">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="50143-1335">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="50143-1335">Az.Monitor</span></span>
* <span data-ttu-id="50143-1336">Get-AzLog cmdlet’inin açıklaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-1336">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="50143-1337">'New-AzMetricAlertRuleV2' komutuna ActionGroupId adlı yeni bir parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-1337">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="50143-1338">Kullanıcı ActionGroupId(string) veya ActionGroup(ActivityLogAlertActionGroup) sağlayabilir.</span><span class="sxs-lookup"><span data-stu-id="50143-1338">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="50143-1339">Az.Network</span><span class="sxs-lookup"><span data-stu-id="50143-1339">Az.Network</span></span>
* <span data-ttu-id="50143-1340">'New-AzPrivateLinkService' cmdlet’inin '-EnableProxyProtocol' parametresi için ek bir parametre notu eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-1340">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="50143-1341">Start-AzVirtualNetworkGatewayConnectionPacketCapture.md ve Start-AzVirtualnetworkGatewayPacketCapture.md içindeki FilterData örneği düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-1341">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="50143-1342">Start-AzVirtualNetworkGatewayConnectionPacketCapture.md ve Start-AzVirtualnetworkGatewayPacketCapture.md içinde tüm iç ve dış paketleri yakalamak için Paket Yakalama örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-1342">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="50143-1343">Sanal Ağ Güvenlik Duvarları üzerinde Azure Güvenlik Duvarı desteği sağlandı</span><span class="sxs-lookup"><span data-stu-id="50143-1343">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="50143-1344">Yeni cmdlet eklenmedi.</span><span class="sxs-lookup"><span data-stu-id="50143-1344">No new cmdlets are added.</span></span> <span data-ttu-id="50143-1345">Sanal ağ güvenlik duvarları üzerinde güvenlik duvarı ilkesi için kısıtlama gevşetiliyor</span><span class="sxs-lookup"><span data-stu-id="50143-1345">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="50143-1346">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="50143-1346">Az.RecoveryServices</span></span>
* <span data-ttu-id="50143-1347">SQL Veritabanları için Dosya olarak geri yükleme desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-1347">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="50143-1348">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="50143-1348">Az.Resources</span></span>
* <span data-ttu-id="50143-1349">Şablon dağıtım cmdlet’leri yeniden düzenlendi</span><span class="sxs-lookup"><span data-stu-id="50143-1349">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="50143-1350">Yönetim grubunda dağıtımları yönetmek için yeni cmdlet’ler eklendi: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="50143-1350">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="50143-1351">Kiracı kapsamında dağıtımları yönetmek için yeni cmdlet’ler eklendi: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="50143-1351">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="50143-1352">\*-AzDeployment cmdlet’leri özel olarak abonelik kapsamında çalışmak için yeniden düzenlendi</span><span class="sxs-lookup"><span data-stu-id="50143-1352">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="50143-1353">\*-AzDeployment cmdlet’leri için \*-AzSubscriptionDeployment diğer adları oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="50143-1353">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="50143-1354">'AvailableToOtherTenants' parametresi ayarlanmadığında 'Update-AzADApplication' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-1354">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="50143-1355">AmbiguousParameterSetException özel durumundan kaçınmak için ApplicationObjectWithoutCredentialParameterSet kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50143-1355">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="50143-1356">Yardım dosyaları yeniden oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="50143-1356">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="50143-1357">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="50143-1357">Az.Sql</span></span>
* <span data-ttu-id="50143-1358">Yönetilen Örneklerde abonelikler arasında zaman noktası geri yüklemesi için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-1358">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="50143-1359">Mevcut SQL Yönetilen Örnek donanım neslini değiştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1359">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="50143-1360">'Update-AzSqlServerVulnerabilityAssessmentSetting' yardım örnekleri düzeltildi: parameter/property output - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="50143-1360">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="50143-1361">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="50143-1361">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="50143-1362">Kullanılabilirlik Grubu Dinleyicisi için cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1362">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="50143-1363">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="50143-1363">Az.StorageSync</span></span>
* <span data-ttu-id="50143-1364">'Invoke-AzStorageSyncCompatibilityCheck' içinde desteklenen karakter kümeleri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-1364">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="50143-1365">3.4.0 - Şubat 2020</span><span class="sxs-lookup"><span data-stu-id="50143-1365">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="50143-1366">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="50143-1366">Highlights since the last major release</span></span>
* <span data-ttu-id="50143-1367">Az.CosmosDB ilk sürüm 0.1.0 yayınlandı</span><span class="sxs-lookup"><span data-stu-id="50143-1367">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="50143-1368">Az.Network ConnectionMonitor V2 desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1368">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="50143-1369">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="50143-1369">Az.Accounts</span></span>
* <span data-ttu-id="50143-1370">AzureRmContext.json kullanılamadığında bağlamı otomatik olarak kaydetmeyi devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="50143-1370">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="50143-1371">Azure PowerShell Common’ın başvurusu 1.3.5-önizleme olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-1371">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="50143-1372">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="50143-1372">Az.ApiManagement</span></span>
* <span data-ttu-id="50143-1373">**Get-AzApiManagementApiSchema** Bir API ile ilişkili Open-Api Şemasını alma düzeltildi https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="50143-1373">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="50143-1374">**New-AzApiManagementProduct** _ ve _ *Set-AzApiManagementProduct*\*</span><span class="sxs-lookup"><span data-stu-id="50143-1374">**New-AzApiManagementProduct** _ and _ *Set-AzApiManagementProduct*\*</span></span>
  - <span data-ttu-id="50143-1375"> https://github.com/Azure/azure-powershell/issues/10472 öğesine ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-1375">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="50143-1376">**Set-AzApiManagementApi** ServiceUrl’nin cmdlet kullanılarak nasıl güncelleştirildiğini göstermek için örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1376">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="50143-1377">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="50143-1377">Az.Compute</span></span>
* <span data-ttu-id="50143-1378">Get-AzVM -Status VM adı olmadan gerçekleştirildiğinde ağ kapasitesinin azaltılmasını engellemek için VM durumu sayısını 100 ile sınırlandırın.</span><span class="sxs-lookup"><span data-stu-id="50143-1378">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="50143-1379">Update-AzDiskEncryptionSet cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1379">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="50143-1380">Aşağıdaki cmdlet’lere EncryptionType ve DiskEncryptionSetId parametreleri eklendi:</span><span class="sxs-lookup"><span data-stu-id="50143-1380">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="50143-1381">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="50143-1381">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="50143-1382">Get-AzProximityPlacementGroup cmdlet’ine ColocationStatus parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-1382">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="50143-1383">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="50143-1383">Az.DataFactory</span></span>
* <span data-ttu-id="50143-1384">ADF .Net SDK sürümü 4.7.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-1384">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="50143-1385">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="50143-1385">Az.DeploymentManager</span></span>
* <span data-ttu-id="50143-1386">Kaynaklara yönelik LIST işlemlerini ekler</span><span class="sxs-lookup"><span data-stu-id="50143-1386">Adds LIST operations for resources</span></span>
* <span data-ttu-id="50143-1387">Durum Denetimi adımlarında işlem gerçekleştirmeye yönelik özellik ekler</span><span class="sxs-lookup"><span data-stu-id="50143-1387">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="50143-1388">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="50143-1388">Az.HDInsight</span></span>
* <span data-ttu-id="50143-1389">New-AzHDInsightCluster’ın belge hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-1389">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="50143-1390">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="50143-1390">Az.KeyVault</span></span>
* <span data-ttu-id="50143-1391">Remove-AzureKeyVault’un New-AzureKeyVault ile tutarlı olmasını sağlamak için VaultName özniteliğine Name diğer adı eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-1391">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="50143-1392">Az.Network</span><span class="sxs-lookup"><span data-stu-id="50143-1392">Az.Network</span></span>
* <span data-ttu-id="50143-1393">Trafik Analizi’nin devre dışı bırakıldığı bir senaryoyu göstermek için Set-AzNetworkWatcherConfigFlowLog.md dosyasına yeni örnek eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-1393">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="50143-1394">Azure Güvenlik Duvarı’na yönetim IP yapılandırması atamaya yönelik destek eklendi. Güvenlik duvarı, yönetim trafiği için ayrılmış alt ağı ve Genel IP’yi kullanacak</span><span class="sxs-lookup"><span data-stu-id="50143-1394">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="50143-1395">New-AzFirewall cmdlet'i güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="50143-1395">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="50143-1396">Genel IP Adresi nesnesi kabul eden -ManagementPublicIpAdress (zorunlu değil) parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1396">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="50143-1397">Güvenlik duvarı nesnesine SetManagementIpConfiguration yöntemi eklendi. Giriş olarak bir alt ağ ve Genel IP adresi gerektirir. Alt ağ adının ‘AzureFirewallManagementSubnet’ olması gerekir</span><span class="sxs-lookup"><span data-stu-id="50143-1397">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="50143-1398">Get-AzNetworkSecurityGroup örnekleri, ağ arabirimlerinin yerine NSG’lere yönelik örnekleri gösterecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-1398">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="50143-1399">Kaynak kimliği tamamlayıcısının bir parametreyi tamamlamasını engelleyen New-AzVpnSite komutundaki yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-1399">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="50143-1400">Application Gateway’de Yeniden Yazma Kuralları Eylem Kümesinde Url Yapılandırması için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1400">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="50143-1401">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="50143-1401">New cmdlets added:</span></span>
        - <span data-ttu-id="50143-1402">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="50143-1402">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="50143-1403">Cmdlet’ler isteğe bağlı -UrlConfiguration parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-1403">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="50143-1404">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="50143-1404">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="50143-1405">NetworkWatcher ConnectionMonitor sürüm 2 kaynakları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1405">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="50143-1406">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="50143-1406">Az.PolicyInsights</span></span>
* <span data-ttu-id="50143-1407">Hangi kaynağın düzeltileceği belirlenmeden önce destek değerlendirmesi uyumluluğu</span><span class="sxs-lookup"><span data-stu-id="50143-1407">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="50143-1408">Start-AzPolicyRemediation cmdlet’ine ‘-ResourceDiscoverMode’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1408">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="50143-1409">İlke meta verilerine ilişkin kaynakları almak için Get-AzPolicyMetadata cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1409">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="50143-1410">API sürümü 2019-10-01 için Get-AzPolicyState ve Get-AzPolicyStateSummary güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-1410">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="50143-1411">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="50143-1411">Az.RecoveryServices</span></span>
* <span data-ttu-id="50143-1412">Çoğaltılan bir diski kaldırılmasına yönelik Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="50143-1412">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="50143-1413">Azure Backup, Kurtarma Hizmetleri Kasası oluştururken etiket eklemeye yönelik destek ekledi.</span><span class="sxs-lookup"><span data-stu-id="50143-1413">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="50143-1414">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="50143-1414">Az.Resources</span></span>
* <span data-ttu-id="50143-1415">Varsayılanı bağlam aboneliği olan \*-AzPolicyAssignment cmdlet’lerinde -Scope isteğe bağlı yapıldı</span><span class="sxs-lookup"><span data-stu-id="50143-1415">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="50143-1416">Parola ve anahtar kimlik bilgileriyle ADServicePrincipal oluşturma örnekleri eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1416">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="50143-1417">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="50143-1417">Az.Sql</span></span>
<span data-ttu-id="50143-1418">DatabaseName’in yerine PartnerDatabaseName’in olup olmadığını denetlemeye yarayan New-AzSqlDatabaseSecondary cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-1418">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="50143-1419">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="50143-1419">Az.Storage</span></span>
* <span data-ttu-id="50143-1420">Depolama Hesabı Oluştur’da Tablo/Sıra Şifreleme Anahtarı’nın ayarlanmasına yönelik destek</span><span class="sxs-lookup"><span data-stu-id="50143-1420">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="50143-1421">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="50143-1421">New-AzStorageAccount</span></span>
* <span data-ttu-id="50143-1422">StorageException’da ExtendedErrorInformation olmadığında RequestId’nin gösterilmesi</span><span class="sxs-lookup"><span data-stu-id="50143-1422">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="50143-1423">Start-AzStorageBlobCopy cmdlet’ine ait olan Örnek 6 düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-1423">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="50143-1424">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="50143-1424">Az.Websites</span></span>
* <span data-ttu-id="50143-1425">Set-AzWebapp ve Set-AzWebappSlot, şu özellikleri destekler: AlwaysOn, MinTls ve FtpsState</span><span class="sxs-lookup"><span data-stu-id="50143-1425">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="50143-1426">Tek Set-AzWebApp Komutunu kullanarak HttpsOnly ayarlanırken aynı anda AppservicePlan değiştirildiğinde HttpsOnly’nin varsayılan değere sıfırlanması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-1426">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="50143-1427">3.3.0 - Ocak 2020</span><span class="sxs-lookup"><span data-stu-id="50143-1427">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="50143-1428">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="50143-1428">Az.Accounts</span></span>
* <span data-ttu-id="50143-1429">Add-AzEnvironment ve Set-AzEnvironment, AzureAttestationServiceEndpointResourceId ve AzureAttestationServiceEndpointSuffix parametrelerini kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-1429">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="50143-1430">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="50143-1430">Az.Cdn</span></span>
* <span data-ttu-id="50143-1431">New-AzCdnEndpoint cmdlet’inde hata yanıtı ayrıntılarını görüntüleme</span><span class="sxs-lookup"><span data-stu-id="50143-1431">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="50143-1432">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="50143-1432">Az.Compute</span></span>
* <span data-ttu-id="50143-1433">İşletim sistemi profili bulunmayan, yönetilen OD diskine sahip bir VM için Set-AzVMCustomScriptExtension cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-1433">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="50143-1434">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="50143-1434">Az.ContainerInstance</span></span>
* <span data-ttu-id="50143-1435">New-AzContainerGroup örneği tarafından kullanılan parametre adları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-1435">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="50143-1436">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="50143-1436">Az.DataBoxEdge</span></span>
* <span data-ttu-id="50143-1437">'Get-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1437">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="50143-1438">Edge Depolama Kapsayıcısını edinme</span><span class="sxs-lookup"><span data-stu-id="50143-1438">Get the Edge Storage Container</span></span>
* <span data-ttu-id="50143-1439">'New-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1439">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="50143-1440">Yeni Edge Depolama Kapsayıcısı oluşturma</span><span class="sxs-lookup"><span data-stu-id="50143-1440">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="50143-1441">'Remove-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1441">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="50143-1442">Edge Depolama Kapsayıcısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="50143-1442">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="50143-1443">'Invoke-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1443">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="50143-1444">Edge Depolama Kapsayıcısındaki verileri yenilemek için eylem çağırma</span><span class="sxs-lookup"><span data-stu-id="50143-1444">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="50143-1445">'Get-AzDataBoxEdgeStorageAccount' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1445">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="50143-1446">Edge Depolama Hesabını edinme</span><span class="sxs-lookup"><span data-stu-id="50143-1446">Get the Edge Storage Account</span></span>
* <span data-ttu-id="50143-1447">'New-AzDataBoxEdgeStorageAccount' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1447">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="50143-1448">Yeni Edge Depolama Hesabını oluşturma</span><span class="sxs-lookup"><span data-stu-id="50143-1448">Create new Edge Storage Account</span></span>
* <span data-ttu-id="50143-1449">'Remove-AzDataBoxEdgeStorageAccount' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1449">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="50143-1450">Edge Depolama Hesabını kaldırma</span><span class="sxs-lookup"><span data-stu-id="50143-1450">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="50143-1451">'Invoke-AzDataBoxEdgeShare' cmdlet’ini çağırma</span><span class="sxs-lookup"><span data-stu-id="50143-1451">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="50143-1452">Paylaşımdaki verileri yenilemek için eylem çağırma</span><span class="sxs-lookup"><span data-stu-id="50143-1452">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="50143-1453">'Set-AzDataBoxEdgeStorageAccountCredential' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1453">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="50143-1454">Az databoxedge depolama hesabı kimlik bilgilerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="50143-1454">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="50143-1455">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="50143-1455">Az.DataFactory</span></span>
* <span data-ttu-id="50143-1456">Get-AzDataFactoryV2IntegrationRuntime cmdlet’i için AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId ve VersionStatus özellikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1456">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="50143-1457">ADF .Net SDK sürümü 4.6.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-1457">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="50143-1458">Statik genel IP adreslerine sahip Azure-SSIS IR’nin oluşturulmasına olanak tanımak için ‘Set-AzureRmDataFactoryV2IntegrationRuntime’ cmdlet’ine yönelik ‘PublicIPs’ parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-1458">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="50143-1459">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="50143-1459">Az.DevTestLabs</span></span>
* <span data-ttu-id="50143-1460">Get-AzDtlAllowedVMSizesPolicy.md’deki bozuk bağlantı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="50143-1460">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="50143-1461">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="50143-1461">Az.EventHub</span></span>
* <span data-ttu-id="50143-1462">Sorun 10634’e yönelik düzeltme: Eventhubnamespace’i kaldırmaya yönelik null Nesne başvurusu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-1462">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="50143-1463">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="50143-1463">Az.HDInsight</span></span>
* <span data-ttu-id="50143-1464">Invoke-AzHDInsightHiveJob.md hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-1464">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="50143-1465">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="50143-1465">Az.MachineLearning</span></span>
* <span data-ttu-id="50143-1466">MachineLearningCompute artık kullanılamadığından, aşağıdaki cmdlet’ler kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="50143-1466">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="50143-1467">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="50143-1467">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="50143-1468">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="50143-1468">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="50143-1469">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="50143-1469">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="50143-1470">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="50143-1470">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="50143-1471">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="50143-1471">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="50143-1472">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="50143-1472">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="50143-1473">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="50143-1473">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="50143-1474">Az.Network</span><span class="sxs-lookup"><span data-stu-id="50143-1474">Az.Network</span></span>
* <span data-ttu-id="50143-1475">1\.36-preview olan Microsoft.Azure.Management.Sql bağımlılığı 1.37-preview’a yükseltildi</span><span class="sxs-lookup"><span data-stu-id="50143-1475">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="50143-1476">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="50143-1476">Az.RecoveryServices</span></span>
* <span data-ttu-id="50143-1477">Azure’dan Azure’a sağlayıcı için müşteri tarafından yönetilen anahtarlar ile bekleyen durumda şifrelenen yönetilen disk VM’lerine yönelik Azure Site Recovery değişim desteği.</span><span class="sxs-lookup"><span data-stu-id="50143-1477">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="50143-1478">Disk şifreleme Kümesi Kimliklerini VMware’den Azure’a aktarımlara yönelik koruma sağlayan isteğe bağlı giriş olarak girmek için Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="50143-1478">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="50143-1479">Disk şifreleme Kümesi Kimliklerini VMware’den Azure’a aktarımlara yönelik koruma sağlayan disk düzeyinde isteğe bağlı giriş olarak girmek için Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="50143-1479">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="50143-1480">HyperV’den Azure’a disk şifrelemesi ayarlama eşlemesi ile çoğaltma korumalı öğeyi güncelleştirmeye yönelik Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="50143-1480">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="50143-1481">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="50143-1481">Az.Resources</span></span>
* <span data-ttu-id="50143-1482">'Remove-AzTag' yardım belgesindeki bir hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-1482">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="50143-1483">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="50143-1483">Az.Sql</span></span>
* <span data-ttu-id="50143-1484">Güvenlik açığı değerlendirmesi tarafından ayarlanan temel cmdlet işlevi, Azure veritabanına yönelik ana veritabanında çalışacak ve yönetilen örnek sistem veritabanlarında sınırlandırılacak şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-1484">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="50143-1485">SQL örneği yük devretme grubu oluşturulurken karşılaşılan bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-1485">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="50143-1486">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="50143-1486">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="50143-1487">Yeni geçerli Lisans türü olarak DR eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1487">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="50143-1488">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="50143-1488">Az.Storage</span></span>
* <span data-ttu-id="50143-1489">Sonraki bir sürümde gerçekleşecek DefaultAction değerinin değişikliğine yönelik hataya neden olan değişiklik uyarısı eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1489">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="50143-1490">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="50143-1490">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="50143-1491">Get-AzureRMStorageAccount cmdlet’i -IncludeGeoReplicationStats parametresiyle çalıştırarak Depolama hesabının en son eşitleme zamanını almaya yönelik destek</span><span class="sxs-lookup"><span data-stu-id="50143-1491">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="50143-1492">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="50143-1492">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="50143-1493">3.2.0 - Aralık 2019</span><span class="sxs-lookup"><span data-stu-id="50143-1493">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="50143-1494">Genel</span><span class="sxs-lookup"><span data-stu-id="50143-1494">General</span></span>
* <span data-ttu-id="50143-1495">.psd1 içindeki başvurular, tüm modüller için göreli yol kullanılacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-1495">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="50143-1496">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="50143-1496">Az.Accounts</span></span>
* <span data-ttu-id="50143-1497">Az 4.0 önizlemesine yönelik istemci tarafı telemetri için doğru UserAgent ayarlandı</span><span class="sxs-lookup"><span data-stu-id="50143-1497">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="50143-1498">Az 4.0 önizlemesinde bağlam null olduğunda kolay hata iletisi görüntüleniyor</span><span class="sxs-lookup"><span data-stu-id="50143-1498">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="50143-1499">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="50143-1499">Az.Batch</span></span>
* <span data-ttu-id="50143-1500">**New-AzBatchPool** cmdlet’inin 'VirtualMachineConfiguration. ContainerConfiguration' veya 'VirtualMachineConfiguration.DataDisks' öğelerini sunucuya doğru bir şekilde göndermediği [10602](https://github.com/Azure/azure-powershell/issues/10602) numaralı sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-1500">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="50143-1501">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="50143-1501">Az.DataFactory</span></span>
* <span data-ttu-id="50143-1502">ADF .Net SDK sürümü 4.5.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-1502">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="50143-1503">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="50143-1503">Az.FrontDoor</span></span>
* <span data-ttu-id="50143-1504">WAF tarafından yönetilen kuralları dışlama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1504">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="50143-1505">Otomatik tamamlamaya SocketAddr eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1505">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="50143-1506">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="50143-1506">Az.HealthcareApis</span></span>
* <span data-ttu-id="50143-1507">Özel Durum İşleme</span><span class="sxs-lookup"><span data-stu-id="50143-1507">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="50143-1508">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="50143-1508">Az.KeyVault</span></span>
* <span data-ttu-id="50143-1509">Ayarlanmamış olabilecek değere erişirken gerçekleşen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-1509">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="50143-1510">Eliptik Eğri Şifrelemesi Sertifika Yönetimi</span><span class="sxs-lookup"><span data-stu-id="50143-1510">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="50143-1511">Sertifika İlkeleri için Eğri belirtme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1511">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="50143-1512">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="50143-1512">Az.Monitor</span></span>
* <span data-ttu-id="50143-1513">Tanılama Ayarları Ekle komutuna isteğe bağlı bağımsız değişken eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-1513">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="50143-1514">Mevcut olduğunda, Log Analytics’e aktarmanın sabit bir şemaya (ayrılmış</span><span class="sxs-lookup"><span data-stu-id="50143-1514">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="50143-1515">veri türü olarak da bilinir) yönelik olması gerektiğini belirten bir anahtar bağımsız değişkeni</span><span class="sxs-lookup"><span data-stu-id="50143-1515">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="50143-1516">Az.Network</span><span class="sxs-lookup"><span data-stu-id="50143-1516">Az.Network</span></span>
* <span data-ttu-id="50143-1517">AzureFirewall Uygulama, NAT ve Ağ Kuralları içinde IpGroups desteği.</span><span class="sxs-lookup"><span data-stu-id="50143-1517">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="50143-1518">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="50143-1518">Az.Resources</span></span>
* <span data-ttu-id="50143-1519">Şablon parametresi adının yerleşik bir parametre adıyla çakışması durumunda şablon dağıtımının, şablon parametresini okuyamamasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-1519">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="50143-1520">İlke cmdlet’leri, ilke kümesi tanımları içinde gruplandırma desteği sunan yeni API sürümü 2019-09-01’i kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-1520">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="50143-1521">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="50143-1521">Az.Sql</span></span>
* <span data-ttu-id="50143-1522">Güvenlik Açığı Değerlendirmesi otomatik etkinleştirmesi, depolamayı StorageV2'de oluşturacak şekilde yükseltildi</span><span class="sxs-lookup"><span data-stu-id="50143-1522">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="50143-1523">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="50143-1523">Az.Storage</span></span>
* <span data-ttu-id="50143-1524">OAuth kimlik doğrulaması tabanlı Depolama Bağlamı ile Blob/Kapsayıcı Kimliği tabanlı SAS belirteci oluşturma desteği</span><span class="sxs-lookup"><span data-stu-id="50143-1524">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="50143-1525">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="50143-1525">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="50143-1526">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="50143-1526">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="50143-1527">Tüm Kimlik SAS belirteçleri iptal edilecek şekilde Depolama Hesabı Kullanıcı Temsilcisi Anahtarlarını iptal etme desteği</span><span class="sxs-lookup"><span data-stu-id="50143-1527">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="50143-1528">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="50143-1528">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="50143-1529">Microsoft.Azure.Management.Storage, yeni API sürümü 2019-06-01 desteklenecek şekilde 14.2.0 sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-1529">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="50143-1530">Dosya Paylaşımı cmdlet’lerinin Yönetim düzlemindeki 5120’den daha büyük değerler için QuotaGiB (Gibibayt temelinde Paylaşım Kotası) desteği sunuldu ve 'QuotaGiB' parametresine yönelik diğer ad olarak 'Quota' parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-1530">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="50143-1531">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="50143-1531">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="50143-1532">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="50143-1532">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="50143-1533">'Quota' parametresine 'QuotaGiB' parametre diğer adı eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1533">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="50143-1534">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="50143-1534">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="50143-1535">Set-AzStorageContainerAcl’nin depolanan Erişim İlkesini temizlemesine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-1535">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="50143-1536">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="50143-1536">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="50143-1537">3.1.0 - Kasım 2019</span><span class="sxs-lookup"><span data-stu-id="50143-1537">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="50143-1538">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="50143-1538">Highlights since the last major release</span></span>
* <span data-ttu-id="50143-1539">Az.DataBoxEdge 1.0.0 yayımlandı</span><span class="sxs-lookup"><span data-stu-id="50143-1539">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="50143-1540">Az.SqlVirtualMachine 1.0.0 yayımlandı</span><span class="sxs-lookup"><span data-stu-id="50143-1540">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="50143-1541">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="50143-1541">Az.Compute</span></span>
* <span data-ttu-id="50143-1542">VM Reapply özelliği</span><span class="sxs-lookup"><span data-stu-id="50143-1542">VM Reapply feature</span></span>
    - <span data-ttu-id="50143-1543">Set-AzVM cmdlet’ine Reapply parametresi ekleme</span><span class="sxs-lookup"><span data-stu-id="50143-1543">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="50143-1544">VM Ölçek Kümesi AutomaticRepairs özelliği:</span><span class="sxs-lookup"><span data-stu-id="50143-1544">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="50143-1545">EnableAutomaticRepair, AutomaticRepairGracePeriod ve AutomaticRepairMaxInstanceRepairsPercent parametreleri şu cmdlet’lere eklendi:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="50143-1545">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="50143-1546">New-AzVM için kiracılar arası galeri görüntüsü desteği</span><span class="sxs-lookup"><span data-stu-id="50143-1546">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="50143-1547">New-AzVM, New-AzVMConfig ve New-AzVmss cmdlet’lerindeki Priority parametresinin bağımsız değişken tamamlayıcısına ‘Spot’ eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-1547">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="50143-1548">Add-AzVmssDataDisk cmdlet’ine DiskIOPSReadWrite ve DiskMBpsReadWrite parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1548">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="50143-1549">New-AzGalleryImageVersion cmdlet’inin SourceImageId parametresi isteğe bağlı olacak şekilde değiştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-1549">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="50143-1550">New-AzGalleryImageVersion cmdlet’ine OSDiskImage ve DataDiskImage parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1550">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="50143-1551">New-AzGalleryImageDefinition cmdlet’ine HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1551">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="50143-1552">New-AzVmss, New-AzVmssConfig ve Update-AzVmss cmdlet’lerine SkipExtensionsOnOverprovisionedVMs parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1552">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="50143-1553">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="50143-1553">Az.DataBoxEdge</span></span>
* <span data-ttu-id="50143-1554">`Get-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1554">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="50143-1555">Sırayı Al</span><span class="sxs-lookup"><span data-stu-id="50143-1555">Get the Order</span></span>
* <span data-ttu-id="50143-1556">`New-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1556">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="50143-1557">Yeni Sıra oluştur</span><span class="sxs-lookup"><span data-stu-id="50143-1557">Create new Order</span></span>
* <span data-ttu-id="50143-1558">`Remove-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1558">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="50143-1559">Sırayı kaldır</span><span class="sxs-lookup"><span data-stu-id="50143-1559">Remove the Order</span></span>
* <span data-ttu-id="50143-1560">`New-AzDataBoxEdgeShare` cmdlet’inde değiştir</span><span class="sxs-lookup"><span data-stu-id="50143-1560">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="50143-1561">Yerel Paylaşım’ı oluşturur</span><span class="sxs-lookup"><span data-stu-id="50143-1561">Now creates Local Share</span></span>
* <span data-ttu-id="50143-1562">`Set-AzDataBoxEdgeRole` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1562">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="50143-1563">IotRole artık Paylaş ile eşlenebilir</span><span class="sxs-lookup"><span data-stu-id="50143-1563">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="50143-1564">`Invoke-AzDataBoxEdgeDevice` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1564">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="50143-1565">Tarama güncelleştirmesi çağırın, güncelleştirmeyi indirin ve bunları cihaza yükleyin</span><span class="sxs-lookup"><span data-stu-id="50143-1565">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="50143-1566">`Get-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1566">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="50143-1567">Tetikleyicilere ilişkin bilgileri alır</span><span class="sxs-lookup"><span data-stu-id="50143-1567">Gets the information about Triggers</span></span>
* <span data-ttu-id="50143-1568">`New-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1568">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="50143-1569">Yeni Tetikleyiciler oluştur</span><span class="sxs-lookup"><span data-stu-id="50143-1569">Create new Triggers</span></span>
* <span data-ttu-id="50143-1570">`Remove-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1570">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="50143-1571">Tetikleyicileri kaldır</span><span class="sxs-lookup"><span data-stu-id="50143-1571">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="50143-1572">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="50143-1572">Az.DataFactory</span></span>
* <span data-ttu-id="50143-1573">ADF .Net SDK sürümü 4.4.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-1573">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="50143-1574">Özel kurulum betiği olmadan kurulum yapılandırmalarını ve 3. taraf bileşenleri etkinleştirmek üzere ‘Set-AzureRmDataFactoryV2IntegrationRuntime’ komutu için ‘ExpressCustomSetup’ parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-1574">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="50143-1575">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="50143-1575">Az.DataLakeStore</span></span>
* <span data-ttu-id="50143-1576">Get-AzDataLakeStoreDeletedItem ve Restore-AzDataLakeStoreDeletedItem parametrelerinin belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-1576">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="50143-1577">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="50143-1577">Az.EventHub</span></span>
* <span data-ttu-id="50143-1578">#10301 numaralı şu sorun düzeltildi: SAS Belirtecinin tarih biçimi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-1578">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="50143-1579">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="50143-1579">Az.FrontDoor</span></span>
* <span data-ttu-id="50143-1580">Enable-AzFrontDoorCustomDomainHttps ve New-AzFrontDoorFrontendEndpointObject öğelerine MinimumTlsVersion parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1580">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="50143-1581">New-AzFrontDoorHealthProbeSettingObject öğesine HealthProbeMethod ve EnabledState parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1581">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="50143-1582">BackendPoolsSettings öğesinin Front Door oluşturmasına/güncelleştirmesine geçmesi için BackendPoolsSettings nesnesi oluşturmaya yönelik yeni cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1582">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="50143-1583">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="50143-1583">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="50143-1584">Az.Network</span><span class="sxs-lookup"><span data-stu-id="50143-1584">Az.Network</span></span>
* <span data-ttu-id="50143-1585">‘Start-AzVirtualNetworkGatewayConnectionPacketCapture.md’ ve 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData seçeneği örnekleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-1585">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="50143-1586">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="50143-1586">Az.PrivateDns</span></span>
* <span data-ttu-id="50143-1587">PrivateDns .Net SDK’sı sürüm 1.0.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-1587">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="50143-1588">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="50143-1588">Az.RecoveryServices</span></span>
* <span data-ttu-id="50143-1589">Koruma etkinleştirilirken disk türünü seçmeye yönelik Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="50143-1589">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="50143-1590">Kurtarma planı eylemi düzenlemesine yönelik Azure Site Recovery hata düzeltmesi.</span><span class="sxs-lookup"><span data-stu-id="50143-1590">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="50143-1591">Dosya akışı Veritabanlarını kabul etmek için Azure Backup SQL Geri yükleme desteği.</span><span class="sxs-lookup"><span data-stu-id="50143-1591">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="50143-1592">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="50143-1592">Az.RedisCache</span></span>
* <span data-ttu-id="50143-1593">‘New-AzRedisCache’ ve ‘Set-AzRedisCache’ cmdletlerine ‘MinimumTlsVersion’ parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-1593">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="50143-1594">‘Get-AzRedisCache’ cmdlet’inin çıkışına ‘MinimumTlsVersion’ eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-1594">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="50143-1595">‘Set-AzRedisCache’ ve ‘New-AzRedisCache’ cmdletlerine yönelik ‘-Size’ parametresine doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-1595">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="50143-1596">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="50143-1596">Az.Resources</span></span>
- <span data-ttu-id="50143-1597">İlke cmdletleri, ilke atamasında EnforcementMode özelliğine sahip yeni 2019-06-01 api sürümünü kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-1597">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="50143-1598">İlke tanımı oluştur yardım örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-1598">Updated create policy definition help example</span></span>
- <span data-ttu-id="50143-1599">Remove-AZADServicePrincipal -ServicePrincipalName’in boş referans adı bulunamadığında boş referans sunması hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-1599">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="50143-1600">Kiracının aboneliği olmadığında New-AZADServicePrincipal’ın boş referans sunmasına ilişkin hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-1600">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="50143-1601">Kimlik bilgilerini yalnızca ilişkili uygulamaya eklemek için New-AzAdServicePrincipal değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-1601">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="50143-1602">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="50143-1602">Az.Sql</span></span>
* <span data-ttu-id="50143-1603">ReadReplicaCount veritabanı için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-1603">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="50143-1604">Alan yedekliliği ayarlı olmadığında Set-AzSqlDatabase düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-1604">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="50143-1605">3.0.0 - Kasım 2019</span><span class="sxs-lookup"><span data-stu-id="50143-1605">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="50143-1606">Genel</span><span class="sxs-lookup"><span data-stu-id="50143-1606">General</span></span>
* <span data-ttu-id="50143-1607">Az.PrivateDns 1.0.0 yayınlandı</span><span class="sxs-lookup"><span data-stu-id="50143-1607">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="50143-1608">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="50143-1608">Az.Accounts</span></span>
* <span data-ttu-id="50143-1609">'Resolve-Error' diğer adı için bir kullanımdan kaldırma iletisi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="50143-1609">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="50143-1610">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="50143-1610">Az.Advisor</span></span>
* <span data-ttu-id="50143-1611">Get-AzAdvisorRecommendation cmdlet'ine yeni 'Operational Excellence' (Operasyonel Mükemmellik) kategorisi eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-1611">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="50143-1612">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="50143-1612">Az.Batch</span></span>
* <span data-ttu-id="50143-1613">`BatchAccountContext` içinde `CoreQuota`, `DedicatedCoreQuota` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="50143-1613">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="50143-1614">Ayrıca yeni bir `LowPriorityCoreQuota` var.</span><span class="sxs-lookup"><span data-stu-id="50143-1614">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="50143-1615">Bu **Get-AzBatchAccount** cmdlet'ini etkiliyor.</span><span class="sxs-lookup"><span data-stu-id="50143-1615">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="50143-1616">**New-AzBatchTask**`-ResourceFile` parametresi şimdi yeni **New-AzBatchResourceFile** cmdlet’i kullanılarak oluşturulabilen bir `PSResourceFile` koleksiyonu alıyor.</span><span class="sxs-lookup"><span data-stu-id="50143-1616">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="50143-1617">`PSResourceFile` nesnelerini oluşturmaya yardımcı olmak için yeni **New-AzBatchResourceFile** cmdlet'i.</span><span class="sxs-lookup"><span data-stu-id="50143-1617">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="50143-1618">Bunlar `-ResourceFile` parametresinde **New-AzBatchTask** cmdlet'ine sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="50143-1618">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="50143-1619">Mevcut `HttpUrl` yolunun yanı sıra iki tür yeni kaynak dosyasını destekliyor:</span><span class="sxs-lookup"><span data-stu-id="50143-1619">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="50143-1620">`AutoStorageContainerName` tabanlı kaynak dosyaları bir otomatik depolama kapsayıcısının tamamını Batch düğümüne indiriyor.</span><span class="sxs-lookup"><span data-stu-id="50143-1620">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="50143-1621">`StorageContainerUrl` tabanlı kaynak dosyaları URL'de belirtilen kapsayıcıyı Batch düğümüne indiriyor.</span><span class="sxs-lookup"><span data-stu-id="50143-1621">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="50143-1622">**Get-AzBatchApplication** tarafından döndürülen `PSApplication` öğesinin `ApplicationPackages` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50143-1622">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="50143-1623">Uygulamanın içindeki belirli paketler artık **Get-AzBatchApplicationPackage** kullanılarak alınabilir.</span><span class="sxs-lookup"><span data-stu-id="50143-1623">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="50143-1624">Örneğin: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="50143-1624">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="50143-1625">**Get-AzBatchApplicationPackage** , **New-AzBatchApplicationPackage** , **Remove-AzBatchApplicationPackage** , **Get-AzBatchApplication** , **New-AzBatchApplication** , **Remove-AzBatchApplication** , ve **Set-AzBatchApplication** cmdlet'lerinde `ApplicationId` parametresi `ApplicationName` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="50143-1625">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage** , **New-AzBatchApplicationPackage** , **Remove-AzBatchApplicationPackage** , **Get-AzBatchApplication** , **New-AzBatchApplication** , **Remove-AzBatchApplication** , and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="50143-1626">`ApplicationId` artık `ApplicationName` parametresinin diğer adıdır.</span><span class="sxs-lookup"><span data-stu-id="50143-1626">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="50143-1627">`PSUserAccount` öğesine yeni `PSWindowsUserConfiguration` özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-1627">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="50143-1628">`PSApplicationPackage` içinde `Version` öğesi `Name` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="50143-1628">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="50143-1629">`PSResourceFile` içinde `BlobSource` öğesi `HttpUrl` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="50143-1629">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="50143-1630">`PSVirtualMachineConfiguration` içinden `OSDisk` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50143-1630">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="50143-1631">**Set-AzBatchPoolOSVersion** kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50143-1631">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="50143-1632">Bu işlem artık desteklenmiyor.</span><span class="sxs-lookup"><span data-stu-id="50143-1632">This operation is no longer supported.</span></span>
* <span data-ttu-id="50143-1633">`PSCloudServiceConfiguration` içinden `TargetOSVersion` kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50143-1633">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="50143-1634">`PSCloudServiceConfiguration` içinde `CurrentOSVersion` öğesi `OSVersion` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="50143-1634">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="50143-1635">`PSPoolUsageMetrics` içinden `DataEgressGiB` ve `DataIngressGiB` kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50143-1635">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="50143-1636">**Get-AzBatchNodeAgentSku** kaldırıldı ve bunun yerini **Get-AzBatchSupportedImage** aldı.</span><span class="sxs-lookup"><span data-stu-id="50143-1636">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="50143-1637">**Get-AzBatchSupportedImage** , **Get-AzBatchNodeAgentSku** ile aynı verileri ama daha kullanımı kolay bir biçimde döndürüyor.</span><span class="sxs-lookup"><span data-stu-id="50143-1637">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="50143-1638">Artık yeni doğrulanmamış resimler de döndürülüyor.</span><span class="sxs-lookup"><span data-stu-id="50143-1638">New non-verified images are also now returned.</span></span> <span data-ttu-id="50143-1639">Her resim için `Capabilities` ve `BatchSupportEndOfLife` hakkında ek bilgiler de ekleniyor.</span><span class="sxs-lookup"><span data-stu-id="50143-1639">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="50143-1640">**New-AzBatchPool** cmdlet'inin `MountConfiguration` parametresiyle havuzun her düğümünde uzak dosya sistemlerini bağlama özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-1640">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="50143-1641">Artık trafiğin kaynak bağlantı noktası temelinde havuza ağ erişimini engelleyen ağ güvenlik kuralları destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="50143-1641">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="50143-1642">Bu destek `PSNetworkSecurityGroupRule` öğesinin `SourcePortRanges` özelliğiyle sağlanıyor.</span><span class="sxs-lookup"><span data-stu-id="50143-1642">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="50143-1643">Kapsayıcıyı çalıştırırken, şimdi Batch görevin kapsayıcı çalışma dizininde veya Batch görevi çalışma dizininde yürütülmesini destekliyor.</span><span class="sxs-lookup"><span data-stu-id="50143-1643">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="50143-1644">Bu, `PSTaskContainerSettings` öğesinin `WorkingDirectory` özelliğiyle denetleniyor.</span><span class="sxs-lookup"><span data-stu-id="50143-1644">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="50143-1645">Yeni `PublicIPs` özelliği aracılığıyla `PSNetworkConfiguration` parametresinde bir genel IP koleksiyonu belirtme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-1645">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="50143-1646">Bu sayede Havuzdaki düğümlerin kullanıcı tarafından sağlanan IP listesinden bir IP alması garanti ediliyor.</span><span class="sxs-lookup"><span data-stu-id="50143-1646">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="50143-1647">Belirtilmediğinde, `PSSTartTask` üzerindeki `WaitForSuccess` öğesinin varsayılan değeri artık `$True` (daha önce `$False` değeriydi).</span><span class="sxs-lookup"><span data-stu-id="50143-1647">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="50143-1648">Belirtilmediğinde, `PSAutoUserSpecification` üzerindeki `Scope` öğesinin varsayılan değeri artık `Pool` (daha önce Windows'da `Task` ve Linux'ta `Pool` değeriydi).</span><span class="sxs-lookup"><span data-stu-id="50143-1648">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="50143-1649">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="50143-1649">Az.Cdn</span></span>
* <span data-ttu-id="50143-1650">RulesEngine'e UrlRewriteAction ve CacheKeyQueryStringAction eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-1650">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="50143-1651">New-AzDeliveryRuleCondition cmdlet'inde eksik 'Selector' Girişi gibi çeşitli hatalar düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-1651">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="50143-1652">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="50143-1652">Az.Compute</span></span>
* <span data-ttu-id="50143-1653">Disk Şifreleme Kümesi özelliği</span><span class="sxs-lookup"><span data-stu-id="50143-1653">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="50143-1654">Yeni cmdlet’ler:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="50143-1654">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="50143-1655">Aşağıdaki cmdlet'lere DiskEncryptionSetId parametresi eklendi:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="50143-1655">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="50143-1656">Aşağıdaki cmdlet'lere DiskEncryptionSetId ve EncryptionType parametreleri eklendi:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="50143-1656">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="50143-1657">New-AzVmssIPConfig cmdlet'ine PublicIPAddressVersion parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1657">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="50143-1658">Özel betik uzantısının FileUris öğesi genel ayardan korumalı ayara taşındı</span><span class="sxs-lookup"><span data-stu-id="50143-1658">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="50143-1659">New-AzVmss, New-AzVmssConfig ve Update-AzVmss cmdlet'lerine ScaleInPolicy eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1659">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="50143-1660">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="50143-1660">Breaking changes</span></span>
    - <span data-ttu-id="50143-1661">CreateOption değeri Upload olduğunda New-AzDiskConfig cmdlet'i için DiskSizeGB yerine UploadSizeInBytes parametresi kullanılıyor</span><span class="sxs-lookup"><span data-stu-id="50143-1661">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="50143-1662">GalleryImageVersion nesnesinde PublishingProfile.Source.ManagedImage.Id yerini StorageProfile.Source.Id'ye bıraktı</span><span class="sxs-lookup"><span data-stu-id="50143-1662">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="50143-1663">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="50143-1663">Az.DataFactory</span></span>
* <span data-ttu-id="50143-1664">ADF .Net SDK sürümü 4.3.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-1664">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="50143-1665">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="50143-1665">Az.DataLakeStore</span></span>
* <span data-ttu-id="50143-1666">ADLS SDK sürümünün güncelleştirilmesi (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) aşağıdaki düzeltmeleri sağlıyor</span><span class="sxs-lookup"><span data-stu-id="50143-1666">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="50143-1667">Geri dönüşüm kutusu veya dizin girdisinin creationtime öğesi seri durumdan çıkarılamadığında özel durum oluşturulmasını önleme.</span><span class="sxs-lookup"><span data-stu-id="50143-1667">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="50143-1668">adlsclient içinde istek başına zaman aşımı ayarını kullanıma sunma</span><span class="sxs-lookup"><span data-stu-id="50143-1668">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="50143-1669">badoffset kurtarması için özgün syncflag değerinin geçirilmesini düzeltme</span><span class="sxs-lookup"><span data-stu-id="50143-1669">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="50143-1670">Yanıt denetlendikten sonra devamlılık belirtecini almak için EnumerateDirectory'yi düzeltme</span><span class="sxs-lookup"><span data-stu-id="50143-1670">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="50143-1671">Birleştirme Hatasını Düzeltme</span><span class="sxs-lookup"><span data-stu-id="50143-1671">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="50143-1672">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="50143-1672">Az.FrontDoor</span></span>
* <span data-ttu-id="50143-1673">Modüllerde çeşitli yazım hataları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-1673">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="50143-1674">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="50143-1674">Az.HDInsight</span></span>
* <span data-ttu-id="50143-1675">ADLSGen1 depolamasıyla kümeyi almak için Get-AzHDInsightCluster cmdlet'ini kullandığında müşterinin 'Geçerli bir Base-64 dizesi değil' hatası almasına yol açan hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-1675">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="50143-1676">Müşterinin Azure Data Lake'e erişirken hizmet sorumlusu uygulama kimliğini sağlayabilmesi için üç cmdlet'e (Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig ve New-AzHDInsightCluster) 'ApplicationId' parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-1676">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="50143-1677">Microsoft.Azure.Management.HDInsight 2.1.0'dan 5.1.0'a geçirildi</span><span class="sxs-lookup"><span data-stu-id="50143-1677">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="50143-1678">Beş cmdlet kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="50143-1678">Removed five cmdlets:</span></span>
    - <span data-ttu-id="50143-1679">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="50143-1679">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="50143-1680">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="50143-1680">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="50143-1681">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="50143-1681">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="50143-1682">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="50143-1682">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="50143-1683">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="50143-1683">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="50143-1684">Üç cmdlet eklendi:</span><span class="sxs-lookup"><span data-stu-id="50143-1684">Added three cmdlets:</span></span>
    - <span data-ttu-id="50143-1685">Get-AzHDInsightMonitoring (Get-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="50143-1685">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="50143-1686">Enable-AzHDInsightMonitoring (Enable-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="50143-1686">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="50143-1687">Disable-AzHDInsightMonitoring (Disable-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="50143-1687">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="50143-1688">Belirli bir konumdan özellik bilgilerinin alınmasını desteklemek için Get-AzHDInsightProperties cmdlet'i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-1688">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="50143-1689">Add-AzHDInsightConfigValue cmdlet'inden parametre kümeleri ('Spark1', 'Spark2') kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50143-1689">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="50143-1690">Add-AzHDInsightSecurityProfile cmdlet'inin yardım belgelerine örnekler eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-1690">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="50143-1691">Aşağıdaki cmdlet'lerin çıkış türü değiştirildi:</span><span class="sxs-lookup"><span data-stu-id="50143-1691">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="50143-1692">Get-AzHDInsightProperties cmdlet'inin CapabilitiesResponse olan çıkış türü AzureHDInsightCapabilities olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-1692">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="50143-1693">Remove-AzHDInsightCluster cmdlet'inin ClusterGetResponse olan çıkış türü bool olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-1693">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="50143-1694">Set-AzHDInsightGatewaySettings cmdlet'inin HttpConnectivitySettings olan çıkış türü GatewaySettings olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-1694">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="50143-1695">Bazı senaryo test çalışmaları eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-1695">Added some scenario test cases.</span></span>
* <span data-ttu-id="50143-1696">Bazı diğer adlar kaldırıldı: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="50143-1696">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="50143-1697">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="50143-1697">Az.IotHub</span></span>
* <span data-ttu-id="50143-1698">Hataya neden olan değişiklikler:</span><span class="sxs-lookup"><span data-stu-id="50143-1698">Breaking changes:</span></span>
    - <span data-ttu-id="50143-1699">'Add-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="50143-1699">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="50143-1700">'Add-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50143-1700">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="50143-1701">'Get-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="50143-1701">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="50143-1702">'Get-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50143-1702">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="50143-1703">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' türündeki 'OperationsMonitoringProperties' özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50143-1703">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="50143-1704">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' türündeki 'OperationsMonitoringProperties' özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50143-1704">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="50143-1705">'New-AzIotHubExportDevice' cmdlet'i artık 'New-AzIotHubExportDevices' diğer adını desteklemiyor.</span><span class="sxs-lookup"><span data-stu-id="50143-1705">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="50143-1706">'New-AzIotHubImportDevice' cmdlet'i artık 'New-AzIotHubImportDevices' diğer adını desteklemiyor.</span><span class="sxs-lookup"><span data-stu-id="50143-1706">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="50143-1707">'Remove-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="50143-1707">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="50143-1708">'Remove-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50143-1708">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="50143-1709">'Set-AzIotHub' cmdet'i artık 'OperationsMonitoringProperties' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="50143-1709">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="50143-1710">'Set-AzIotHub' cmdlet'inden 'UpdateOperationsMonitoringProperties' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50143-1710">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="50143-1711">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="50143-1711">Az.RecoveryServices</span></span>
* <span data-ttu-id="50143-1712">NSG, genel IP ve Azure'dan Azure'a iç yük dengeleyiciler gibi ağ kaynaklarını yapılandırmak için Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="50143-1712">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="50143-1713">Azure'a vMWare için yönetilen diske yazmaya yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="50143-1713">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="50143-1714">Azure'a vMWare için NIC azaltmasına yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="50143-1714">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="50143-1715">Azure'a Azure için hızlandırılmış ağa yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="50143-1715">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="50143-1716">Azure'a Azure için aracı otomatik güncelleştirmesine yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="50143-1716">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="50143-1717">Azure'a Azure için Standart SSD'ye yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="50143-1717">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="50143-1718">Azure'a Azure için Azure Disk Şifrelemesi iki geçişine yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="50143-1718">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="50143-1719">Azure'a Azure için yeni eklenen diski korumaya yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="50143-1719">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="50143-1720">VM için SoftDelete özelliği eklendi ve softdelete için de testler eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1720">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="50143-1721">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="50143-1721">Az.Resources</span></span>
* <span data-ttu-id="50143-1722">Bağımlılık derlemesi Microsoft.Extensions.Caching.Memory 1.1.1'den 2.2'ye güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-1722">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="50143-1723">Az.Network</span><span class="sxs-lookup"><span data-stu-id="50143-1723">Az.Network</span></span>
* <span data-ttu-id="50143-1724">PrivateEndpointConnection için tüm cmdlet'ler genel hizmet sağlayıcısını destekleyecek şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-1724">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="50143-1725">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="50143-1725">Updated cmdlet:</span></span>
        - <span data-ttu-id="50143-1726">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="50143-1726">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="50143-1727">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="50143-1727">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="50143-1728">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="50143-1728">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="50143-1729">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="50143-1729">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="50143-1730">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="50143-1730">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="50143-1731">PrivateLinkResource için yeni cmdlet eklendi ve bu da genel hizmet sağlayıcısını destekliyor.</span><span class="sxs-lookup"><span data-stu-id="50143-1731">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="50143-1732">Yeni cmdlet:</span><span class="sxs-lookup"><span data-stu-id="50143-1732">New cmdlet:</span></span>
        - <span data-ttu-id="50143-1733">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="50143-1733">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="50143-1734">Proxy Protocol V2 özelliği için yeni alanlar ve parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-1734">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="50143-1735">PrivateLinkService'e EnableProxyProtocol özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1735">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="50143-1736">PrivateEndpointConnection'a LinkIdentifier özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1736">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="50143-1737">New-AzPrivateLinkService cmdlet'i yeni isteğe bağlı EnableProxyProtocol parametresi eklenerek güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-1737">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="50143-1738">'New-AzApplicationGatewaySku' başvuru belgelerindeki yanlış parametre açıklaması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-1738">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="50143-1739">Azure güvenlik duvarı ilkesini desteklemek için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1739">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="50143-1740">VirtualHub'ın RouteTables alt kaynağı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1740">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="50143-1741">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="50143-1741">New cmdlets added:</span></span>
        - <span data-ttu-id="50143-1742">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="50143-1742">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="50143-1743">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="50143-1743">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="50143-1744">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="50143-1744">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="50143-1745">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="50143-1745">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="50143-1746">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="50143-1746">Set-AzVirtualHub</span></span>
* <span data-ttu-id="50143-1747">VirtualWan'ın yeni VirtualHub ve VirtualWANType özellikleri Sku'su için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1747">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="50143-1748">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="50143-1748">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="50143-1749">New-AzVirtualHub : Sku parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1749">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="50143-1750">Update-AzVirtualHub : Sku parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1750">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="50143-1751">New-AzVirtualWan : VirtualWANType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1751">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="50143-1752">Update-AzVirtualWan : VirtualWANType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1752">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="50143-1753">HubVnetConnection, VpnConnection ve ExpressRouteConnection için EnableInternetSecurity özelliği desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1753">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="50143-1754">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="50143-1754">New cmdlets added:</span></span>
        - <span data-ttu-id="50143-1755">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="50143-1755">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="50143-1756">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="50143-1756">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="50143-1757">New-AzureRmVirtualHubVnetConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1757">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="50143-1758">New-AzureRmVpnConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1758">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="50143-1759">Update-AzureRmVpnConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1759">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="50143-1760">New-AzureRmExpressRouteConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1760">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="50143-1761">Set-AzureRmExpressRouteConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1761">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="50143-1762">TopLevel WebApplicationFirewall İlkesini Yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1762">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="50143-1763">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="50143-1763">New cmdlets added:</span></span>
        - <span data-ttu-id="50143-1764">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="50143-1764">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="50143-1765">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="50143-1765">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="50143-1766">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="50143-1766">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="50143-1767">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="50143-1767">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="50143-1768">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="50143-1768">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="50143-1769">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="50143-1769">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="50143-1770">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="50143-1770">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="50143-1771">New-AzApplicationGatewayFirewallPolicy : PolicySetting, ManagedRule parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1771">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="50143-1772">CustomRule'da Geo-Match işleci için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1772">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="50143-1773">FirewallCondition'da işlece GeoMatch eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1773">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="50143-1774">perListener ve perSite Güvenlik duvarı ilkesi için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1774">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="50143-1775">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="50143-1775">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="50143-1776">New-AzApplicationGatewayHttpListener : FirewallPolicy, FirewallPolicyId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1776">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="50143-1777">New-AzApplicationGatewayPathRuleConfig : FirewallPolicy, FirewallPolicyId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1777">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="50143-1778">'PSBastion' içinde AzureBastionSubnet adlı gerekli alt ağın büyük/küçük harfe duyarlı olması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-1778">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="50143-1779">Azure Güvenlik Duvarı için Ağ Kurallarında Hedef FQDN'lere ve NAT Kurallarında Çevrilmiş FQDN'ye yönelik destek</span><span class="sxs-lookup"><span data-stu-id="50143-1779">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="50143-1780">IpGroup'un RouteTables üst düzey kaynağı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1780">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="50143-1781">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="50143-1781">New cmdlets added:</span></span>
        - <span data-ttu-id="50143-1782">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="50143-1782">New-AzIpGroup</span></span>
        - <span data-ttu-id="50143-1783">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="50143-1783">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="50143-1784">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="50143-1784">Get-AzIpGroup</span></span>
        - <span data-ttu-id="50143-1785">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="50143-1785">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="50143-1786">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="50143-1786">Az.ServiceFabric</span></span>
* <span data-ttu-id="50143-1787">Bu senaryo artık Add-AzVmssSecret cmdlet'inin kapsamına girdiğinden Add-AzServiceFabricApplicationCertificate cmdlet'i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50143-1787">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="50143-1788">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="50143-1788">Az.Sql</span></span>
* <span data-ttu-id="50143-1789">Yönetilen Örneklerde bırakılan veritabanlarını geri yükleme desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-1789">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="50143-1790">Eski denetim cmdlet'leri kodda kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="50143-1790">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="50143-1791">Kullanım dışı bırakılan diğer adlar kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="50143-1791">Removed deprecated aliases:</span></span>
* <span data-ttu-id="50143-1792">Get-AzSqlDatabaseIndexRecommendations (bunun yerine Get-AzSqlDatabaseIndexRecommendation kullanın)</span><span class="sxs-lookup"><span data-stu-id="50143-1792">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="50143-1793">Get-AzSqlDatabaseRestorePoints (bunun yerine Get-AzSqlDatabaseRestorePoint kullanıldı)</span><span class="sxs-lookup"><span data-stu-id="50143-1793">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="50143-1794">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet'i kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="50143-1794">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="50143-1795">Kullanım dışı bırakılan Güvenlik Açığı Değerlendirmesi Ayarları cmdlet'lerinin diğer adları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="50143-1795">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="50143-1796">Gelişmiş Tehdit Algılama Ayarları cmdlet'leri kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="50143-1796">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="50143-1797">Veritabanındaki sütunlarda duyarlılık önerilerini devre dışı bırakma ve etkinleştirme cmdlet'leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-1797">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="50143-1798">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="50143-1798">Az.Storage</span></span>
* <span data-ttu-id="50143-1799">Depolama hesabı oluşturulur veya güncelleştirilirken Büyük dosya paylaşımını etkinleştirme desteği</span><span class="sxs-lookup"><span data-stu-id="50143-1799">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="50143-1800">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="50143-1800">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="50143-1801">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="50143-1801">Set-AzStorageAccount</span></span>
* <span data-ttu-id="50143-1802">Dosya işleyicisi kapatılırken/alınırken, DeletePending durumundaki nesnesinde hata olmasını önlemek için giriş yolunun Dosya dizini mi yoksa Dosya mı olduğunu denetlemeyi atlayın</span><span class="sxs-lookup"><span data-stu-id="50143-1802">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="50143-1803">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="50143-1803">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="50143-1804">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="50143-1804">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="50143-1805">2.8.0 - Ekim 2019</span><span class="sxs-lookup"><span data-stu-id="50143-1805">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="50143-1806">Genel</span><span class="sxs-lookup"><span data-stu-id="50143-1806">General</span></span>
* <span data-ttu-id="50143-1807">Az.HealthcareApis 1.0.0 sürümü</span><span class="sxs-lookup"><span data-stu-id="50143-1807">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="50143-1808">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="50143-1808">Az.Accounts</span></span>
* <span data-ttu-id="50143-1809">Oluşturulan modüller için telemetri ve URL’yi yeniden yazma özelliği güncelleştirildi, Windows birim testleri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-1809">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="50143-1810">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="50143-1810">Az.ApiManagement</span></span>
* <span data-ttu-id="50143-1811">**Set-AzApiManagementApi** - ApiVersionSet’e Güncelleştirme API’si desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1811">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="50143-1812">[https://github.com/Azure/azure-powershell/issues/10068](https://github.com/Azure/azure-powershell/issues/10068 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-1812">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="50143-1813">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="50143-1813">Az.Automation</span></span>
* <span data-ttu-id="50143-1814">Linux yeniden başlatma ayarı parametresi için New-AzureAutomationSoftwareUpdateConfiguration cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-1814">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="50143-1815">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="50143-1815">Az.Batch</span></span>
* <span data-ttu-id="50143-1816">Kullanımdan kaldırılan **Get-AzBatchNodeAgentSku** yerine 2.0.0 sürümünde **Get-AzBatchSupportImage** kullanıma sunulacak.</span><span class="sxs-lookup"><span data-stu-id="50143-1816">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="50143-1817">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="50143-1817">Az.Compute</span></span>
* <span data-ttu-id="50143-1818">New-AzVM ve New-AzVmss cmdlet’lerine Priority, EvictionPolicy ve MaxPrice parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1818">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="50143-1819">Add-AzVMAdditionalUnattendContent ve Add-AzVMSshPublicKey cmdlet’leri için uyarı iletisi ve yardım belgesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-1819">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="50143-1820">Set-AzVMDiskEncryptionExtension için yönetilen diskleri olan Linux VM’lere yönelik -skipVmBackup özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-1820">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="50143-1821">Set-AzVMDiskEncryptionExtension’daki iki geçişli senaryoda güncelleştirme şifreleme ayarlarındaki hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-1821">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="50143-1822">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="50143-1822">Az.DataFactory</span></span>
* <span data-ttu-id="50143-1823">ADF V2 veri akışı için CRUD komutları eklendi: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, ve Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="50143-1823">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="50143-1824">ADF V2 veri akışı hata ayıklama oturumu için eylem komutları eklendi: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand ve Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="50143-1824">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="50143-1825">ADF .Net SDK sürümü 4.2.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-1825">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="50143-1826">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="50143-1826">Az.DataLakeStore</span></span>
* <span data-ttu-id="50143-1827">‘-’ içeren hesapların etki alanı olmadan geçirilebilmesi için hesap doğrulama düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-1827">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="50143-1828">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="50143-1828">Az.HealthcareApis</span></span>
* <span data-ttu-id="50143-1829">PowerShell sürümü 1.0.0 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-1829">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="50143-1830">SDK sürümü 1.0.2 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-1830">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="50143-1831">Yeni SDK sürümüne başvurmaları için testler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-1831">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="50143-1832">İç içe geçmiş çıkış yapısı, düzleştirilmiş olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-1832">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="50143-1833">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="50143-1833">Az.IotHub</span></span>
* <span data-ttu-id="50143-1834">Yeni yönlendirme kaynağı eklendi: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="50143-1834">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="50143-1835">Küçük hata düzeltmesi: Get-AzIothub SubscriptionId öğesini döndürmüyor</span><span class="sxs-lookup"><span data-stu-id="50143-1835">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="50143-1836">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="50143-1836">Az.Monitor</span></span>
* <span data-ttu-id="50143-1837">Eylem grupları -ItsmReceiver -VoiceReceiver -ArmRoleReceiver -AzureFunctionReceiver -LogicAppReceiver -AutomationRunbookReceiver -AzureAppPushReceiver için yeni eylem grubu alıcıları eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1837">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="50143-1838">Alıcılar için etkinleştirilen ortak uyarı şemasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="50143-1838">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="50143-1839">Bunlar SMS, Azure Uygulaması iletimi, ITSM ve ses alıcıları için geçerli değildir</span><span class="sxs-lookup"><span data-stu-id="50143-1839">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="50143-1840">Web kancaları artık Azure Active Directory kimlik doğrulamasını destekliyor.</span><span class="sxs-lookup"><span data-stu-id="50143-1840">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="50143-1841">Az.Network</span><span class="sxs-lookup"><span data-stu-id="50143-1841">Az.Network</span></span>
* <span data-ttu-id="50143-1842">Hizmet Uç Noktası İlkeleri için kullanılabilen diğer adları almak için çağrılabilen Get-AzAvailableServiceAlias cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-1842">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="50143-1843">Sanal Ağ Geçidi Bağlantılarına trafik seçicileri eklemeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1843">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="50143-1844">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="50143-1844">New cmdlets added:</span></span>
        - <span data-ttu-id="50143-1845">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="50143-1845">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="50143-1846">Cmdlet’ler, şu isteğe bağlı parametreler ile güncelleştirildi: -TrafficSelectorPolicies -New-AzureRmVirtualNetworkGatewayConnection -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="50143-1846">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="50143-1847">Ağ güvenlik kuralı yapılandırmalarında ESP ve AH protokollerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1847">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="50143-1848">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="50143-1848">Updated cmdlets:</span></span>
        - <span data-ttu-id="50143-1849">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="50143-1849">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="50143-1850">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="50143-1850">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="50143-1851">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="50143-1851">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="50143-1852">Cortex cmdlet’lerinde özel durumların işlenmesi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-1852">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="50143-1853">VirtualNetworkGateways için yeni Nesiller ve SKU’lar</span><span class="sxs-lookup"><span data-stu-id="50143-1853">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="50143-1854">VirtualNetworkGateways için yeni Nesiller sunuldu.</span><span class="sxs-lookup"><span data-stu-id="50143-1854">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="50143-1855">VirtualNetworkGateways için yüksek verimliliğe sahip yeni SKU’lar sunuldu.</span><span class="sxs-lookup"><span data-stu-id="50143-1855">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="50143-1856">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="50143-1856">Az.RedisCache</span></span>
* <span data-ttu-id="50143-1857">‘-Size’ parametresine yönelik eksik değerleri eklemek için ‘Set-AzRedisCache’ başvuru belgesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-1857">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="50143-1858">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="50143-1858">Az.Sql</span></span>
* <span data-ttu-id="50143-1859">Yönetilen örnekte Active Directory yöneticisini ayarlama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1859">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="50143-1860">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="50143-1860">Az.Storage</span></span>
* <span data-ttu-id="50143-1861">Depolama İstemcisi Kitaplığı 11.1.0 sürümüne yükseltildi</span><span class="sxs-lookup"><span data-stu-id="50143-1861">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="50143-1862">Yönetim düzlemi API’si olan liste kapsayıcıları NextPageLink ile listelenecek</span><span class="sxs-lookup"><span data-stu-id="50143-1862">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="50143-1863">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="50143-1863">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="50143-1864">Abonelikteki Liste Depolama hesapları NextPageLink ile listelenecek</span><span class="sxs-lookup"><span data-stu-id="50143-1864">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="50143-1865">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="50143-1865">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="50143-1866">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="50143-1866">Az.StorageSync</span></span>
* <span data-ttu-id="50143-1867">Reset-AzStorageSyncServerCertificate öğesinde Sorun 9810 düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-1867">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="50143-1868">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="50143-1868">Az.Websites</span></span>
* <span data-ttu-id="50143-1869">Bir uygulamanın ASP’sini güncelleştiren Set-AzWebApp başarısız oluyor</span><span class="sxs-lookup"><span data-stu-id="50143-1869">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="50143-1870">2.7.0 - Eylül 2019</span><span class="sxs-lookup"><span data-stu-id="50143-1870">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="50143-1871">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="50143-1871">Az.ApiManagement</span></span>
* <span data-ttu-id="50143-1872">'Set-AzApiManagementPolicy' başvuru belgesindeki '-Format' parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-1872">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="50143-1873">Kullanım dışı bırakılan 'Update-AzApiManagementDeployment' cmdlet’ine başvurular, başvuru belgesinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50143-1873">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="50143-1874">Bunun yerine 'Set-AzApiManagement' kullanın.</span><span class="sxs-lookup"><span data-stu-id="50143-1874">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="50143-1875">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="50143-1875">Az.Automation</span></span>
* <span data-ttu-id="50143-1876">'Register-AzAutomationDscNode' için başvuru belgesindeki örnek yazım yanlışı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-1876">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="50143-1877">Register-AzAutomationDSCNode için işletim sistemi kısıtlamasına açıklama eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1877">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="50143-1878">-Wait seçeneği için Start-AzAutomationRunbook cmdlet’i Null başvuru özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-1878">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="50143-1879">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="50143-1879">Az.Compute</span></span>
* <span data-ttu-id="50143-1880">New-AzDiskConfig cmdlet’ine UploadSizeInBytes parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1880">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="50143-1881">New-AzSnapshotConfig cmdlet’ine Incremental parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1881">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="50143-1882">Düşük öncelikli sanal makine özelliği eklendi:</span><span class="sxs-lookup"><span data-stu-id="50143-1882">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="50143-1883">New-AzVMConfig cmdlet’ine MaxPrice, EvictionPolicy ve Priority parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-1883">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="50143-1884">New-AzVmssConfig, Update-AzVM ve Update-AzVmss cmdlet’lerine MaxPrice parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-1884">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="50143-1885">Get-AzAvailabilitySet cmdlet’i abonelikteki tüm kullanılabilirlik kümelerini listelediğinde oluşan VM başvuru sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-1885">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="50143-1886">Get-AzRemoteDesktopFile için null özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-1886">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="50143-1887">Sona göre konum için VHD Seek yöntemi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-1887">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="50143-1888">New-AzVM ve Update-AzVM için UltraSSD sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-1888">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="50143-1889">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="50143-1889">Az.DataFactory</span></span>
* <span data-ttu-id="50143-1890">ADF V2’ye 3 yeni komut eklendi - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription ve Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="50143-1890">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="50143-1891">ADF .Net SDK sürümü 4.1.3’e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-1891">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="50143-1892">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="50143-1892">Az.HDInsight</span></span>
* <span data-ttu-id="50143-1893">Son değişiklikler duyurusu</span><span class="sxs-lookup"><span data-stu-id="50143-1893">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="50143-1894">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="50143-1894">Az.IotHub</span></span>
* <span data-ttu-id="50143-1895">Coğrafi olarak eşleştirilmiş olağanüstü durum kurtarma bölgesine bir IotHub için yük devretme çağırmaya yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-1895">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="50143-1896">IotHub için ileti zenginleştirmelerini yönetmeye yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-1896">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="50143-1897">Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="50143-1897">New cmdlets are:</span></span>
    - <span data-ttu-id="50143-1898">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="50143-1898">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="50143-1899">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="50143-1899">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="50143-1900">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="50143-1900">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="50143-1901">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="50143-1901">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="50143-1902">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="50143-1902">Az.Monitor</span></span>
* <span data-ttu-id="50143-1903">En son İzleme SDK’sını, yani 0.24.1-preview sürümünü işaret eder</span><span class="sxs-lookup"><span data-stu-id="50143-1903">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="50143-1904">Ölçüm cmdlet’lerine hataya neden olmayan değişiklikler ekler, yani Birim sabit listesi birçok yeni değeri destekler.</span><span class="sxs-lookup"><span data-stu-id="50143-1904">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="50143-1905">Bunlar salt okunur cmdlet’ler olduğundan girişlerinde değişiklik olmaz.</span><span class="sxs-lookup"><span data-stu-id="50143-1905">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="50143-1906">**ActionGroups** istekleri için api-version şimdi **2019-06-01** değerine sahiptir. Önceden **2018-03-01** sürümü kullanılıyordu.</span><span class="sxs-lookup"><span data-stu-id="50143-1906">The api-version of the **ActionGroups** requests is now **2019-06-01** , before it was **2018-03-01**.</span></span> <span data-ttu-id="50143-1907">Senaryo testleri bu değişikliğe uyum sağlayacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-1907">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="50143-1908">**EmailReceiver** ve **WebhookReceiver** sınıfları için oluşturuculara yeni bir zorunlu bağımsız değişken ( **useCommonAlertSchema** adlı bir Boole değeri) eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-1908">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="50143-1909">Şu anda, hataya neden olan bu değişikliği cmdlet’lerden gizlemek için değer **false** olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="50143-1909">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="50143-1910">**NOT** : Bu, Uyarılar ekibi tarafından doğrulanması gereken geçici bir değişikliktir.</span><span class="sxs-lookup"><span data-stu-id="50143-1910">**NOTE** : this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="50143-1911">**Kaynak** ( **ScheduledQueryRuleSource** sınıfı ile ilişkili) sınıfının oluşturucusu için bağımsız değişkenlerin sırası önceki SDK’dan değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-1911">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="50143-1912">Bu değişiklik iki birim testinin düzeltilmesini gerektirdi: Bunlar derlenebiliyor ancak testleri geçemiyordu.</span><span class="sxs-lookup"><span data-stu-id="50143-1912">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="50143-1913">**AlertingAction** ( **ScheduledQueryRuleSource** sınıfı ile ilişkili) sınıfının oluşturucusu için bağımsız değişkenlerin sırası önceki SDK’dan değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-1913">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="50143-1914">Bu değişiklik iki birim testinin düzeltilmesini gerektirdi: Bunlar derlenebiliyor ancak testleri geçemiyordu.</span><span class="sxs-lookup"><span data-stu-id="50143-1914">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="50143-1915">Ölçüm uyarısı V2 için Dinamik Eşik ölçütlerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1915">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="50143-1916">New-AzMetricAlertRuleV2Criteria: Şimdi dinamik eşik ölçütleri de oluşturur</span><span class="sxs-lookup"><span data-stu-id="50143-1916">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="50143-1917">Add-AzMetricAlertRuleV2: Şimdi dinamik eşik ölçütlerini de kabul eder</span><span class="sxs-lookup"><span data-stu-id="50143-1917">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="50143-1918">Zamanlanmış Sorgu Kuralı cmdlet’lerinde (SQR) geliştirmeler</span><span class="sxs-lookup"><span data-stu-id="50143-1918">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="50143-1919">Cmdlet’ler 'Location' parametresini hem konum (ör. eastus) hem de konumun görünen adı (ör. Doğu ABD) biçiminde kabul eder</span><span class="sxs-lookup"><span data-stu-id="50143-1919">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="50143-1920">'Enabled' parametresi yardım dosyalarında düzgün şekilde açıklandı</span><span class="sxs-lookup"><span data-stu-id="50143-1920">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="50143-1921">İsteğe bağlı 'ActionGroup' parametresi için örnekler eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1921">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="50143-1922">Yardım dosyaları genel olarak geliştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-1922">Overall improved help files</span></span>
* <span data-ttu-id="50143-1923">'Set-AzActionRule' için kapsam türünü belirlemeyle ilgili bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-1923">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="50143-1924">Az.Network</span><span class="sxs-lookup"><span data-stu-id="50143-1924">Az.Network</span></span>
* <span data-ttu-id="50143-1925">'New-AzApplicationGateway' başvuru belgesindeki yanlış örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-1925">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="50143-1926">'Get-AzNetworkWatcherPacketCapture' başvuru belgesine paket yakalama için tüm özellikleri almayla ilgili not eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1926">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="50143-1927">'Test-AzNetworkWatcherIPFlow' başvuru belgesindeki örnek, NIC’lerin doğru olarak numaralandırılacağı şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-1927">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="50143-1928">Bulut özel durum ayrıştırması, mevcut olması durumunda daha fazla ayrıntı gösterecek şekilde iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-1928">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="50143-1929">Bulut özel durum ayrıştırması, ek SDK özel durum türünü işleyecek şekilde geliştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-1929">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="50143-1930">Güvenlik Kuralı modellerinin yanlış eşlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-1930">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="50143-1931">Özel IP özelliği için ağ arabirimine özellikler eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1931">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="50143-1932">'PrivateEndpoint' özelliği PSResourceId türü olarak PSNetworkInterface öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1932">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="50143-1933">'PrivateLinkConnectionProperties' özelliği PSIpConfigurationConnectivityInformation türü olarak PSNetworkInterfaceIPConfiguration öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1933">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="50143-1934">Yeni PSIpConfigurationConnectivityInformation model sınıfı eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1934">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="50143-1935">Azure Güvenlik Duvarı kaynağı için 'mssql' adlı yeni ApplicationRuleProtocolType eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1935">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="50143-1936">Sanal WAN’da çoklu bağlantı desteği</span><span class="sxs-lookup"><span data-stu-id="50143-1936">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="50143-1937">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="50143-1937">New cmdlets</span></span>
        - <span data-ttu-id="50143-1938">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="50143-1938">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="50143-1939">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="50143-1939">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="50143-1940">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="50143-1940">Updated cmdlet:</span></span>
        - <span data-ttu-id="50143-1941">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="50143-1941">New-VpnSite</span></span>
        - <span data-ttu-id="50143-1942">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="50143-1942">Update-VpnSite</span></span>
        - <span data-ttu-id="50143-1943">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="50143-1943">New-VpnConnection</span></span>
        - <span data-ttu-id="50143-1944">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="50143-1944">Update-VpnConnection</span></span>
* <span data-ttu-id="50143-1945">Belgeler, bazı PowerShell örneklerinde AzureRM cmdlet’leri yerine Az cmdlet’leri kullanılacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-1945">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="50143-1946">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="50143-1946">Az.RecoveryServices</span></span>
* <span data-ttu-id="50143-1947">AzureVMpolicy Nesnesi, ProtectedItemsCount Özniteliği ile güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-1947">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="50143-1948">VM ilkesi ve Özgün Depolama Hesabı Geri Yükleme için Testler eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1948">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="50143-1949">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="50143-1949">Az.Resources</span></span>
* <span data-ttu-id="50143-1950">New-AzRoleAssignment cmdlet’inin Scope parametresi olmadan çağrılamamasına neden olan bir hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-1950">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="50143-1951">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="50143-1951">Az.ServiceFabric</span></span>
* <span data-ttu-id="50143-1952">'Update-AzServiceFabricReliability' başvuru belgesindeki örnekteki yazım yanlışı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-1952">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="50143-1953">Uygulamaları ve hizmetleri yönetmek için yeni cmdlet’ler ekleniyor:</span><span class="sxs-lookup"><span data-stu-id="50143-1953">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="50143-1954">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="50143-1954">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="50143-1955">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="50143-1955">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="50143-1956">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="50143-1956">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="50143-1957">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="50143-1957">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="50143-1958">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="50143-1958">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="50143-1959">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="50143-1959">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="50143-1960">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="50143-1960">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="50143-1961">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="50143-1961">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="50143-1962">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="50143-1962">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="50143-1963">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="50143-1963">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="50143-1964">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="50143-1964">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="50143-1965">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="50143-1965">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="50143-1966">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="50143-1966">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="50143-1967">Service Fabric SDK’sı, Service Fabric kaynak sağlayıcısı api-version 2019-03-01 kullanan 1.2.0 sürümüne yükseltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-1967">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="50143-1968">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="50143-1968">Az.SignalR</span></span>
* <span data-ttu-id="50143-1969">Update, Restart, CheckNameAvailability, GetUsage Cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1969">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="50143-1970">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="50143-1970">Az.Sql</span></span>
* <span data-ttu-id="50143-1971">'Get-AzSqlElasticPool' için başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-1971">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="50143-1972">Elastik havuz oluşturmak (New-AzSqlElasticPool) için sanal çekirdek örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-1972">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="50143-1973">Set-AzSqlServerAdvancedThreatProtectionPolicy ve Set-AzSqlDatabaseAdvancedThreatProtectionPolicy içinde EmailAddresses’in doğrulanması ve EmailAddresses’in boş olması durumunda EmailAdmins’in false olmamasına yönelik denetim kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="50143-1973">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="50143-1974">Denetim kategorisini etkinleştiren birden çok tanılama ayarı olduğunda sunucu/veritabanı denetim ayarlarının kaldırılması etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-1974">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="50143-1975">Birden çok Sql Güvenlik Açığı Değerlendirmesi cmdlet’inde (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting ve Update-AzSqlInstanceVulnerabilityAssessmentSetting) e-posta adresleri doğrulaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-1975">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="50143-1976">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="50143-1976">Az.Storage</span></span>
* <span data-ttu-id="50143-1977">'Get-AzStorageAccountKey' için başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-1977">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="50143-1978">Azure Dosyasını karşıya yüklerken/indirirken, hedef dosyada, dosya SMB özelliklerinin (Dosya Öznitelikleri, Dosya Oluşturma Zamanı, Dosya Son Yazma Zamanı) korunmasına yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1978">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="50143-1979">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="50143-1979">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="50143-1980">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="50143-1980">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="50143-1981">Kapsayıcı tarafından etkinleştirilmiş ImmutabilityPolicy üzerinde özellikler/meta tarih hatası içeren Karşıya yükleme blok blobu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-1981">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="50143-1982">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="50143-1982">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="50143-1983">Yönetim düzlemi API’si ile Azure Dosya paylaşımlarını yönetmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-1983">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="50143-1984">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="50143-1984">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="50143-1985">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="50143-1985">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="50143-1986">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="50143-1986">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="50143-1987">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="50143-1987">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="50143-1988">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="50143-1988">Az.Websites</span></span>
* <span data-ttu-id="50143-1989">Uygulamanın yeni ASP’ye geçirilmesi sırasında webapp Etiketlerinin silinmesine neden olan bir sorun düzeltiliyor</span><span class="sxs-lookup"><span data-stu-id="50143-1989">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="50143-1990">Publish-AzureWebapp cmdlet’i Linux ve Windows üzerinde çalışacak şekilde düzeltiliyor</span><span class="sxs-lookup"><span data-stu-id="50143-1990">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="50143-1991">'Get-AzWebAppPublishingProfile' başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-1991">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="50143-1992">2.6.0 - Ağustos 2019</span><span class="sxs-lookup"><span data-stu-id="50143-1992">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="50143-1993">Genel</span><span class="sxs-lookup"><span data-stu-id="50143-1993">General</span></span>
* <span data-ttu-id="50143-1994">Çok sayıda modülde çeşitli yazım hataları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-1994">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="50143-1995">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="50143-1995">Az.Accounts</span></span>
* <span data-ttu-id="50143-1996">Azure İşlevleri Kimlik Doğrulaması’nda kullanıcı tarafından atanan MSI desteği (#9479)</span><span class="sxs-lookup"><span data-stu-id="50143-1996">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="50143-1997">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="50143-1997">Az.Aks</span></span>
* <span data-ttu-id="50143-1998">‘Get-AzAks’ için çıkışla ilgili bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-1998">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="50143-1999">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="50143-1999">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="50143-2000">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="50143-2000">Az.ApiManagement</span></span>
* <span data-ttu-id="50143-2001">[https://github.com/Azure/azure-powershell/issues/9351](https://github.com/Azure/azure-powershell/issues/9351 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2001">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="50143-2002">ProductID, APIID, GroupID ve UserID için kısıtlamaları zorunlu kılmayan .NET NuGet sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2002">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="50143-2003">**Get-AzApiManagementProduct** - Ürünleri API kullanarak sorgulama desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-2003">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="50143-2004">**New-AzApiManagementApiRevision** - Yeni API düzeltmesi oluşturulurken ApiRevisionDescription parametresinin ayarlanmamasına neden olan sorun düzeltildi https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="50143-2004">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="50143-2005">'PsApiManagementOAuth2AuthrozationServer' modeli 'PsApiManagementOAuth2AuthorizationServer' olarak değiştirilerek yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2005">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="50143-2006">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="50143-2006">Az.Batch</span></span>
* <span data-ttu-id="50143-2007">Windows’un ilk harfi büyütülerek yardım iletisindeki ve belgelerdeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2007">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="50143-2008">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="50143-2008">Az.Cdn</span></span>
* <span data-ttu-id="50143-2009">CDN modülü dönüştürme yardımcısındaki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2009">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="50143-2010">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="50143-2010">Az.Compute</span></span>
* <span data-ttu-id="50143-2011">New-AzVMConfig cmdlet’ine VmssID eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2011">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="50143-2012">New-AzVmssConfig ve Update-AzVmss öğelerine TerminateScheduledEvents ve TerminateScheduledEventNotBeforeTimeoutInMinutes parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2012">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="50143-2013">VM görüntüsü nesnesine HyperVGeneration özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2013">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="50143-2014">Host ve HostGroup özellikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2014">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="50143-2015">Yeni cmdlet’ler:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="50143-2015">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="50143-2016">New-AzVMConfig ve New-AzVM öğelerine HostId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2016">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="50143-2017">Doğru parametre adını kullanmak için ‘Invoke-AzVMRunCommand’ belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2017">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="50143-2018">'Set-AzVMDiskEncryptionExtension' ve 'Set-AzVmssDiskEncryptionExtension' referans belgelerindeki '-VolumeType' açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2018">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="50143-2019">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="50143-2019">Az.DataFactory</span></span>
* <span data-ttu-id="50143-2020">‘Windows’ sözcüğünün baş harfi büyütülerek 'New-AzDataFactoryEncryptValue' belgesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2020">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="50143-2021">ADF .Net SDK sürümü 4.1.2’ye güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2021">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="50143-2022">Şirket İçinde Barındırılan Integration Runtime’ı SSIS Integration Runtime için ara sunucu olarak ayarlamak üzere 'Set-AzureRmDataFactoryV2IntegrationRuntime' komutuna 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' ve 'DataProxyStagingPath' parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2022">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="50143-2023">Tetiklenen işlem hatlarını, iletiyi ve özellikleri göstermesi için PSTriggerRun öğesi, etkinlik türünü göstermesi için de PSActivityRun öğesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2023">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="50143-2024">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="50143-2024">Az.DataLakeStore</span></span>
* <span data-ttu-id="50143-2025">Hata veya uzak özel durumları için Get-DataLakeStoreDeletedItem öğesinin yanıt vermemeye başlaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-2025">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="50143-2026">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="50143-2026">Az.EventHub</span></span>
* <span data-ttu-id="50143-2027">#9658 numaralı şu sorun düzeltildi: Set-AzEventHubNetworkRuleSet öğesinde bulunan VirtualNteworkRule parametresindeki yazım hatası</span><span class="sxs-lookup"><span data-stu-id="50143-2027">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="50143-2028">#9558 numaralı şu sorun düzeltildi: Set-AzEventHubNamespace öğesinin PUT yerine PATCH kullanması</span><span class="sxs-lookup"><span data-stu-id="50143-2028">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="50143-2029">Set-AzEventHubNamespace cmdlet’ine EnableKafka parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2029">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="50143-2030">#9786 numaralı şu sorun düzeltildi: Yalnızca dinleme haklarıyla bir kural oluşturulamaması</span><span class="sxs-lookup"><span data-stu-id="50143-2030">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="50143-2031">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="50143-2031">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="50143-2032">‘Azure’ın’ tamamen küçük harflerle yazılmasıyla belgede oluşan yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2032">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="50143-2033">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="50143-2033">Az.Monitor</span></span>
* <span data-ttu-id="50143-2034">Yardım belgelerindeki yanlış parametre adı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2034">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="50143-2035">Az.Network</span><span class="sxs-lookup"><span data-stu-id="50143-2035">Az.Network</span></span>
* <span data-ttu-id="50143-2036">New-AzPrivateLinkServiceIpConfig güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2036">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="50143-2037">Sunucu tarafında hiç kullanılmadığı için ‘PublicIpAddress’ parametresi kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="50143-2037">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="50143-2038">Mevcut IP yapılandırmasının birincil yapılandırma olup olmadığını belirten bir isteğe bağlı bir parametre (‘Primary’) eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-2038">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="50143-2039">SDK’daki istek hatası özel durumunun işlenmesi geliştirildi. Bu, daha önceden SDK özel durumlarının düzgün şekilde işlenenmemesiyle oluşan ve önemli hata ayrıntılarının görüntülenmemesine neden olan sorunu düzeltir</span><span class="sxs-lookup"><span data-stu-id="50143-2039">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="50143-2040">Doğru IPv6 ön ek uzunluğunu denetlemek amacıyla Ipv6 IP Ön eki için doğrulama mantığı ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="50143-2040">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="50143-2041">Get-AzVirtualNetworkSubnetConfig güncelleştirildi: Alt ağ kaynak kimliği ile almak için parametre kümesi eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-2041">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="50143-2042">AzNetworkServiceTag için Konum parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2042">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="50143-2043">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="50143-2043">Az.OperationalInsights</span></span>
* <span data-ttu-id="50143-2044">'New-AzOperationalInsightsLinuxSyslogDataSource' öğesine yönelik belgeler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2044">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="50143-2045">Örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2045">Added example</span></span>
    - <span data-ttu-id="50143-2046">‘-Name’ parametresi için açıklama güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2046">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="50143-2047">New-AzOperationalInsightsWindowsEventDataSource için bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2047">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="50143-2048">New-AzOperationalInsightsWindowsEventDataSource için -Name parametresinin açıklaması değiştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2048">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="50143-2049">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="50143-2049">Az.RecoveryServices</span></span>
* <span data-ttu-id="50143-2050">'Get-AzRecoveryServicesBackupJobDetail.md' dosyası güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2050">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="50143-2051">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="50143-2051">Az.Resources</span></span>
* <span data-ttu-id="50143-2052">Microsoft.Resource için yeni API sürümüne (2019-05-10) yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2052">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="50143-2053">Değişkenler, kaynaklar ve özellikler için copy.count = 0 parametresine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2053">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="50143-2054">'condition = false' veya 'copy.count = 0' içeren kaynaklar tam modda silinir</span><span class="sxs-lookup"><span data-stu-id="50143-2054">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="50143-2055">Belgelere yardımcı olması için abonelik düzeyinde ilke atama örneği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2055">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="50143-2056">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="50143-2056">Az.ServiceBus</span></span>
* <span data-ttu-id="50143-2057">#9658 numaralı şu sorun düzeltildi: Set-AzServiceBusNetworkRuleSet öğesinde bulunan VirtualNetworkRule parametresindeki yazım hatası</span><span class="sxs-lookup"><span data-stu-id="50143-2057">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="50143-2058">#9786 numaralı şu sorun düzeltildi: Yalnızca dinleme haklarıyla bir kural oluşturulamaması</span><span class="sxs-lookup"><span data-stu-id="50143-2058">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="50143-2059">Sıra ve konu için ad kullanılabilirliğini denetlemeye yönelik yeni komut ('Test-AzServiceBusNameAvailability') eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2059">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="50143-2060">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="50143-2060">Az.ServiceFabric</span></span>
* <span data-ttu-id="50143-2061">Düğüm ekleme türü cmdlet hataları düzeltildi:</span><span class="sxs-lookup"><span data-stu-id="50143-2061">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="50143-2062">Kaynak grubunun Service Fabric kümesiyle ilgili diğer vmss öğesi olduğunda oluşan NullReferenceException hatası.</span><span class="sxs-lookup"><span data-stu-id="50143-2062">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="50143-2063">Şu sorunu düzeltir: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="50143-2063">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="50143-2064">virtualNetwork kümeyle farklı bir kaynak grubunda yer aldığında cmdlet’in başarısız olmasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-2064">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="50143-2065">Şu sorunu düzeltir: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="50143-2065">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="50143-2066">Add-AzServiceFabricApplicationCertificate cmdlet’i kullanımdan kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="50143-2066">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="50143-2067">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="50143-2067">Az.Sql</span></span>
* <span data-ttu-id="50143-2068">Eski denetim cmdlet’lerinin belgeleri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-2068">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="50143-2069">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="50143-2069">Az.Storage</span></span>
* <span data-ttu-id="50143-2070">Cmdlet örneklerine ve güncelleştirme parametresi açıklamalarına daha fazla senaryo eklenerek Get/Close-AzStorageFileHandle öğesi için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2070">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="50143-2071">Karşıya yükleme blobu ve kopyalama blobunda StandardBlobTier için destek</span><span class="sxs-lookup"><span data-stu-id="50143-2071">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="50143-2072">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="50143-2072">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="50143-2073">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="50143-2073">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="50143-2074">Blobu kopyala işleminde Yeniden Doldurma Önceliği Desteği</span><span class="sxs-lookup"><span data-stu-id="50143-2074">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="50143-2075">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="50143-2075">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="50143-2076">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="50143-2076">Az.Websites</span></span>
* <span data-ttu-id="50143-2077">Set-AzWebApp ve Set-AzWebAppSlot öğelerindeki -AppSettings parametresine yönelik açıklama eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2077">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="50143-2078">2.5.0 - Temmuz 2019</span><span class="sxs-lookup"><span data-stu-id="50143-2078">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="50143-2079">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="50143-2079">Az.Accounts</span></span>
* <span data-ttu-id="50143-2080">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2080">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="50143-2081">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="50143-2081">Az.ApplicationInsights</span></span>
* <span data-ttu-id="50143-2082">'Remove-AzApplicationInsightsApiKey' belgesindeki örnek yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2082">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="50143-2083">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="50143-2083">Az.Automation</span></span>
* <span data-ttu-id="50143-2084">Kaynak dizesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2084">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="50143-2085">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="50143-2085">Az.CognitiveServices</span></span>
* <span data-ttu-id="50143-2086">NetworkRuleSet desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-2086">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="50143-2087">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="50143-2087">Az.Compute</span></span>
* <span data-ttu-id="50143-2088">VM örneği görünüm nesnesinin eksik özellikleri (ComputerName, OsName, OsVersion ve HyperVGeneration) eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-2088">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="50143-2089">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="50143-2089">Az.ContainerRegistry</span></span>
* <span data-ttu-id="50143-2090">Çoğaltma parametresi için Remove-AzContainerRegistryReplication içindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2090">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="50143-2091">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="50143-2091">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="50143-2092">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="50143-2092">Az.DataFactory</span></span>
* <span data-ttu-id="50143-2093">ADF .Net SDK’sı 4.1.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2093">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="50143-2094">'Get-AzDataFactoryV2PipelineRun' belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2094">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="50143-2095">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="50143-2095">Az.EventHub</span></span>
* <span data-ttu-id="50143-2096">SAS belirteci oluşturmak için yeni cmdlet eklendi: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="50143-2096">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="50143-2097">yalnızca 'Manage' atanırsa authorizationrules hakları için doğrulama ve hata iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2097">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="50143-2098">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="50143-2098">Az.KeyVault</span></span>
* <span data-ttu-id="50143-2099">Sertifika İlkeleri için KeySize’ı belirtmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2099">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="50143-2100">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="50143-2100">Az.LogicApp</span></span>
* <span data-ttu-id="50143-2101">Get-AzIntegrationAccountMap’in tüm eşleme türlerini listelemesi için düzeltme</span><span class="sxs-lookup"><span data-stu-id="50143-2101">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="50143-2102">Filtreleme için yeni MapType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2102">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="50143-2103">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="50143-2103">Az.ManagedServices</span></span>
* <span data-ttu-id="50143-2104">API 2019-06-01 sürümü için destek eklendi (GA)</span><span class="sxs-lookup"><span data-stu-id="50143-2104">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="50143-2105">Az.Network</span><span class="sxs-lookup"><span data-stu-id="50143-2105">Az.Network</span></span>
* <span data-ttu-id="50143-2106">Özel uç nokta ve özel bağlantı hizmeti için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2106">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="50143-2107">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="50143-2107">New cmdlets</span></span>
        - <span data-ttu-id="50143-2108">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="50143-2108">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="50143-2109">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="50143-2109">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="50143-2110">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="50143-2110">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="50143-2111">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="50143-2111">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="50143-2112">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="50143-2112">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="50143-2113">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="50143-2113">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="50143-2114">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="50143-2114">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="50143-2115">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="50143-2115">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="50143-2116">Özellik için aşağıdaki komutlar güncelleştirildi: Virtualnetwork’te Alt Ağ üzerinde PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies bayrağı</span><span class="sxs-lookup"><span data-stu-id="50143-2116">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="50143-2117">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2117">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="50143-2118">Bu alt ağda özel uç nokta üzerinde ağ ilkelerinin uygulanıp uygulanmayacağını yapılandıran isteğe bağlı -PrivateEndpointNetworkPoliciesFlag parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-2118">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="50143-2119">Bu alt ağda özel bağlantı hizmeti üzerinde ağ ilkelerinin uygulanıp uygulanmayacağını yapılandıran isteğe bağlı -PrivateLinkServiceNetworkPoliciesFlag parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-2119">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="50143-2120">AzPrivateLinkService’in cmdlet 'ServiceName' parametresi, geriye yönelik uyumluluk için 'ServiceName' diğer adıyla 'Name' olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="50143-2120">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="50143-2121">Ağ güvenlik kuralı yapılandırmalarına yönelik ICMP protokolü etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2121">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="50143-2122">Cmdlet'ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2122">Updated cmdlets</span></span>
        - <span data-ttu-id="50143-2123">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="50143-2123">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="50143-2124">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="50143-2124">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="50143-2125">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="50143-2125">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="50143-2126">ConnectionProtocolType (Ikev1/Ikev2), New-AzVirtualNetworkGatewayConnection için yapılandırılabilir bir parametre olarak eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2126">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="50143-2127">LoadBalancerFrontendIpConfiguration içinde PrivateIpAddressVersion eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2127">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="50143-2128">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="50143-2128">Updated cmdlet:</span></span>
        - <span data-ttu-id="50143-2129">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="50143-2129">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="50143-2130">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="50143-2130">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="50143-2131">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="50143-2131">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="50143-2132">Yoklama içinde özek bağlantı noktasını desteklemek için Application Gateway New-AzApplicationGatewayProbeConfig komutu güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2132">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="50143-2133">New-AzApplicationGatewayProbeConfig güncelleştirildi: Arka uç sunucusunu yoklamak için kullanılan isteğe bağlı parametre Bağlantı Noktası eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-2133">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="50143-2134">Bu parametre Standard_V2 ve WAF_V2 SKU için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="50143-2134">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="50143-2135">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="50143-2135">Az.OperationalInsights</span></span>
* <span data-ttu-id="50143-2136">Kayıtlı aramaların varsayılan sürümü 1 olacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-2136">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="50143-2137">Özel günlük null normal ifade işleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2137">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="50143-2138">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="50143-2138">Az.RecoveryServices</span></span>
* <span data-ttu-id="50143-2139">'Get-AzRecoveryServicesBackupJob.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2139">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="50143-2140">'Get-AzRecoveryServicesBackupContainer.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2140">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="50143-2141">'Get-AzRecoveryServicesVault.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2141">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="50143-2142">'Wait-AzRecoveryServicesBackupJob.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2142">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="50143-2143">'Set-AzRecoveryServicesVaultContext.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2143">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="50143-2144">'Get-AzRecoveryServicesBackupItem.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2144">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="50143-2145">'Get-AzRecoveryServicesBackupRecoveryPoint.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2145">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="50143-2146">'Restore-AzRecoveryServicesBackupItem.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2146">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="50143-2147">Azure Dosya Paylaşımı kapsayıcısının Kaydını Silmeye yönelik hizmet çağrısı güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2147">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="50143-2148">'Set-AzRecoveryServicesAsrAlertSetting.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2148">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="50143-2149">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="50143-2149">Az.Resources</span></span>
- <span data-ttu-id="50143-2150">'New-AzResourceGroupDeployment' belgelerinde başvurulan eksik cmdlet kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="50143-2150">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="50143-2151">İlke cmdlet’leri yeni 2019-01-01 api sürümünü kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2151">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="50143-2152">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="50143-2152">Az.ServiceBus</span></span>
* <span data-ttu-id="50143-2153">SAS belirteci oluşturmak için yeni cmdlet eklendi: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="50143-2153">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="50143-2154">yalnızca 'Manage' atanırsa authorizationrules hakları için doğrulama ve hata iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2154">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="50143-2155">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="50143-2155">Az.Sql</span></span>
* <span data-ttu-id="50143-2156">Set-AzSqlDatabaseSecondary cmdlet’i için eksik örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2156">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="50143-2157">E-posta adresi sağlamadan yinelenen Güvenlik Açığı Değerlendirme taramalarının ayarlanması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2157">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="50143-2158">Bir uyarı iletisindeki küçük bir yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-2158">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="50143-2159">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="50143-2159">Az.Storage</span></span>
* <span data-ttu-id="50143-2160">'Get-AzStorageAccount' başvuru belgelerindeki örnek, doğru parametre adını kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2160">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="50143-2161">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="50143-2161">Az.StorageSync</span></span>
* <span data-ttu-id="50143-2162">Invoke-AzStorageSyncChangeDetection cmdlet’i ekleniyor.</span><span class="sxs-lookup"><span data-stu-id="50143-2162">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="50143-2163">TierFilesOlderThanDays’in uygulanmasına yönelik Sorun 9551 düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2163">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="50143-2164">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="50143-2164">Az.Websites</span></span>
* <span data-ttu-id="50143-2165">Bazı SiteConfig özelliklerinin Get-AzWebApp ve Set-AzWebApp tarafından döndürülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2165">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="50143-2166">Get-AzDeletedWebApp ve Restore-AzDeletedWebApp için yeni bir Konum parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2166">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="50143-2167">New-AzWebApp -IncludeSourceWebAppSlots kullanılarak web uygulaması yuvalarının kopyalanmasıyla ilgili bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2167">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="50143-2168">2.4.0 - Temmuz 2019</span><span class="sxs-lookup"><span data-stu-id="50143-2168">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="50143-2169">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="50143-2169">Az.Accounts</span></span>
* <span data-ttu-id="50143-2170">Profil cmdlet’leri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2170">Add support for profile cmdlets</span></span>
* <span data-ttu-id="50143-2171">Oluşturulan cmdlet’lerde ortamlar ve veri düzlemleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2171">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="50143-2172">Windows PowerShell’deki veri düzlemi cmdlet’leri için bazı durumlarda yanlış uç noktası kullanılması hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2172">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="50143-2173">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="50143-2173">Az.Advisor</span></span>
* <span data-ttu-id="50143-2174">Az.Advisor genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="50143-2174">GA release of Az.Advisor</span></span>
* <span data-ttu-id="50143-2175">Bu modül, artık toplama `Az` modülünün bir parçası olarak sunulur</span><span class="sxs-lookup"><span data-stu-id="50143-2175">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="50143-2176">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="50143-2176">Az.ApiManagement</span></span>
* <span data-ttu-id="50143-2177">[https://github.com/Azure/azure-powershell/issues/8671](https://github.com/Azure/azure-powershell/issues/8671 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2177">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="50143-2178">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="50143-2178">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="50143-2179">Abonelikleri Kullanıcı ve Ürüne göre sorgulama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2179">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="50143-2180">Kapsam kullanarak sorgulama desteği eklendi ('/', '/apis', '/apis/echo-api')</span><span class="sxs-lookup"><span data-stu-id="50143-2180">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="50143-2181">[https://github.com/Azure/azure-powershell/issues/9307](https://github.com/Azure/azure-powershell/issues/9307 ) ve https://github.com/Azure/azure-powershell/issues/8432 sorunları için düzeltme</span><span class="sxs-lookup"><span data-stu-id="50143-2181">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="50143-2182">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="50143-2182">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="50143-2183">API’leri içeri aktarırken ‘ApiVersion’ ve ‘ApiVersionSetId’ belirtmek için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2183">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="50143-2184">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="50143-2184">Az.Automation</span></span>
* <span data-ttu-id="50143-2185">Dize değerini işlemek için Set-AzAutomationConnectionFieldValue cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-2185">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="50143-2186">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="50143-2186">Az.Compute</span></span>
* <span data-ttu-id="50143-2187">New-AzImageConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2187">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="50143-2188">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="50143-2188">Az.DataFactory</span></span>
* <span data-ttu-id="50143-2189">Etkinlik çalıştırmalarını alma, işlem hattı çalıştırmalarını alma ve tetikleme çalıştırmalarını alma ADF cmdlet’lerinin çıkışları, Select-Object kanalını destekleyecek şekilde güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="50143-2189">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="50143-2190">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="50143-2190">Az.EventGrid</span></span>
* <span data-ttu-id="50143-2191">‘New-AzEventGridSubscription’ belgesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2191">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="50143-2192">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="50143-2192">Az.IotHub</span></span>
* <span data-ttu-id="50143-2193">Yetkilendirme ilkesi anahtarlarını yeniden oluşturma desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-2193">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="50143-2194">Az.Network</span><span class="sxs-lookup"><span data-stu-id="50143-2194">Az.Network</span></span>
* <span data-ttu-id="50143-2195">Genel IP etiketlerine ‘RoutingPreference’ eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2195">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="50143-2196">‘Get-AzNetworkServiceTag’ başvuru belgesi için örnekler geliştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2196">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="50143-2197">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="50143-2197">Az.PolicyInsights</span></span>
* <span data-ttu-id="50143-2198">Get-AzPolicyState’de boş başvuru sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2198">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="50143-2199">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="50143-2199">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="50143-2200">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="50143-2200">Az.OperationalInsights</span></span>
* <span data-ttu-id="50143-2201">Get-AzOperationalInsightsDataSource’da döndürülen CustomLog veri kaynağı modeli düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2201">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="50143-2202">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="50143-2202">Az.RecoveryServices</span></span>
* <span data-ttu-id="50143-2203">IaaSVM’ler için get-policy komutu düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="50143-2203">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="50143-2204">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="50143-2204">Az.Resources</span></span>
    - <span data-ttu-id="50143-2205">Get-AzPolicyState -Top parametresi için yardım metni düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="50143-2205">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="50143-2206">Get-AzPolicyAlias için istemci tarafı sayfalama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2206">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="50143-2207">Set-AzPolicyAssignment, -PolicyParameters ve -PolicyParametersObject için yeni parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2207">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="50143-2208">İlke cmdlet’leri için bazı belge ve örnekler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2208">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="50143-2209">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="50143-2209">Az.ServiceBus</span></span>
* <span data-ttu-id="50143-2210">4938 numaralı, MaxSizeInMegabytes ayarlanırken New-AzureRmServiceBusQueue’nun BadRequest döndürmesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2210">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="50143-2211">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="50143-2211">Az.Sql</span></span>
* <span data-ttu-id="50143-2212">Önizleme sürümündeki Örnek Yük Devretme Grubu cmdlet’leri genel kullanım sürümüne eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2212">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="50143-2213">Yeni cmdlet’ler ile Azure SQL Server\Veritabanı Denetimi desteği.</span><span class="sxs-lookup"><span data-stu-id="50143-2213">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="50143-2214">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="50143-2214">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="50143-2215">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="50143-2215">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="50143-2216">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="50143-2216">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="50143-2217">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="50143-2217">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="50143-2218">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="50143-2218">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="50143-2219">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="50143-2219">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="50143-2220">Güvenlik Açığı Değerlendirmesi ayarlarından e-posta kısıtlamaları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="50143-2220">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="50143-2221">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="50143-2221">Az.Storage</span></span>
* <span data-ttu-id="50143-2222">Aşağıdaki cmdlet’te 2 parametre (‘-IndexDocument’ ve ‘-ErrorDocument404Path’) gerekliden isteğe bağlı olarak değiştirildi:</span><span class="sxs-lookup"><span data-stu-id="50143-2222">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="50143-2223">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="50143-2223">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="50143-2224">Get-AzStorageBlobContent’in yardımı, örnek eklenerek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2224">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="50143-2225">Cmdlet StorageException ile başarısız olduğunda artık daha ayrıntılı hata bilgisi gösteriliyor</span><span class="sxs-lookup"><span data-stu-id="50143-2225">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="50143-2226">Azure Dosyalar AAD DS Kimlik Doğrulaması ile Depolama hesabı oluşturma veya güncelleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2226">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="50143-2227">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="50143-2227">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="50143-2228">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="50143-2228">Set-AzStorageAccount</span></span>
* <span data-ttu-id="50143-2229">Bir dosya paylaşımının, dosya dizininin veya dosyanın dosya tanıtıcılarını listeleme veya kapatma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2229">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="50143-2230">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="50143-2230">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="50143-2231">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="50143-2231">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="50143-2232">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="50143-2232">Az.StorageSync</span></span>
* <span data-ttu-id="50143-2233">Bu modül, artık toplama `Az` modülünün bir parçası olarak sunulur</span><span class="sxs-lookup"><span data-stu-id="50143-2233">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="50143-2234">2.3.2 - Haziran 2019</span><span class="sxs-lookup"><span data-stu-id="50143-2234">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="50143-2235">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="50143-2235">Az.Accounts</span></span>
* <span data-ttu-id="50143-2236">İşlevler çağrıları için bazı durumlarda yanlış URL’nin kullanılmasına neden olan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2236">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="50143-2237">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="50143-2237">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="50143-2238">AzureRM’den Az cmdlet’lerine yönelik diğer adlarla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2238">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="50143-2239">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="50143-2239">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="50143-2240">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="50143-2240">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="50143-2241">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="50143-2241">Az.Compute</span></span>
* <span data-ttu-id="50143-2242">New-AzVm ve New-AzVmss basit parametre kümeleri artık 'ProximityPlacementGroup' parametresini kabul ediyor.</span><span class="sxs-lookup"><span data-stu-id="50143-2242">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="50143-2243">'New-AzVM' başvuru belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2243">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="50143-2244">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="50143-2244">Az.Dns</span></span>
* <span data-ttu-id="50143-2245">'Set-AzDnsZone' yardım örneklerindeki bir yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-2245">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="50143-2246">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="50143-2246">Az.EventGrid</span></span>
* <span data-ttu-id="50143-2247">2019-06-01 API sürümünü kullanacak biçimde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-2247">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="50143-2248">Yeni cmdlet’ler:</span><span class="sxs-lookup"><span data-stu-id="50143-2248">New cmdlets:</span></span>
    - <span data-ttu-id="50143-2249">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="50143-2249">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="50143-2250">Yeni bir Azure Event Grid etki alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="50143-2250">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="50143-2251">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="50143-2251">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="50143-2252">Event Grid Etki Alanının ayrıntılarını veya mevcut Azure aboneliğindeki tüm Event Grid Etki Alanlarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="50143-2252">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="50143-2253">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="50143-2253">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="50143-2254">Bir Azure Event Grid Etki Alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="50143-2254">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="50143-2255">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="50143-2255">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="50143-2256">Bir Azure Event Grid Etki Alanı için paylaşılan erişim anahtarını yeniden üretir.</span><span class="sxs-lookup"><span data-stu-id="50143-2256">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="50143-2257">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="50143-2257">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="50143-2258">Etkinlikleri bir Event Grid Etki Alanıyla paylaşmak için kullanılan paylaşılan erişim anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="50143-2258">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="50143-2259">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="50143-2259">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="50143-2260">Yeni bir Azure Event Grid Etki Alanı Konu Başlığı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="50143-2260">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="50143-2261">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="50143-2261">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="50143-2262">Bir Event Grid Etki Alanının ayrıntılarını veya mevcut Azure aboneliğindeki belirli Event Grid Etki Alanlarının altında bulunan tüm Event Grid Etki Alanı Konu Başlıklarının listesini alır</span><span class="sxs-lookup"><span data-stu-id="50143-2262">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="50143-2263">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="50143-2263">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="50143-2264">Mevcut bir Azure Event Grid Etki Alanı Konu Başlığını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="50143-2264">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="50143-2265">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="50143-2265">Updated cmdlets:</span></span>
    - <span data-ttu-id="50143-2266">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="50143-2266">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="50143-2267">Bu kaynakların altında yeni olay aboneliklerinin oluşturulmasına olanak tanımak amacıyla yeni Event Grid Etki Alanı ve Event Grid Etki Alanı Konu Başlığına yönelik kanal oluşturmanın desteklemesi için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="50143-2267">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="50143-2268">Bu kaynakların altında yeni olay aboneliklerinin oluşturulmasına olanak tanımak amacıyla yeni Event Grid Etki Alanı adını ve/veya Event Grid Etki Alanı Konu Başlığının adını belirtmek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="50143-2268">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="50143-2269">Mevcut parametrelerin yeniden kullanılmasına olanak tanımak için etki alanları ve etki alanı konu başlıkları için yeni Parametre kümeleri (örneğin, EndPointType, SubjectBeginsWith vb.) ekler.</span><span class="sxs-lookup"><span data-stu-id="50143-2269">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="50143-2270">Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="50143-2270">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="50143-2271">Olay aboneliği bitiş tarihi,</span><span class="sxs-lookup"><span data-stu-id="50143-2271">Event subscription expiration date,</span></span>
            - <span data-ttu-id="50143-2272">Gelişmiş filtreleme parametreleri.</span><span class="sxs-lookup"><span data-stu-id="50143-2272">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="50143-2273">Hedef olarak servicebusqueue için yeni sabit listesi ekler.</span><span class="sxs-lookup"><span data-stu-id="50143-2273">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="50143-2274">-IncludedEventType seçeneğinde ‘All’ kullanılmasını engeller ve bunu şununla değiştirir</span><span class="sxs-lookup"><span data-stu-id="50143-2274">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="50143-2275">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="50143-2275">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="50143-2276">Sayfalandırma ve filtreleme sonuçlarını desteklemek için yeni isteğe bağlı parametreler (Top, ODataQuery and NextLink) ekler.</span><span class="sxs-lookup"><span data-stu-id="50143-2276">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="50143-2277">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="50143-2277">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="50143-2278">Bu kaynakların altında bulunan mevcut olay aboneliklerinin taşınmasına olanak tanımak amacıyla Event Grid Etki Alanı ve Event Grid Etki Alanı Konu Başlığına yönelik kanal oluşturmayı desteklemek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="50143-2278">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="50143-2279">Bu kaynakların altında bulunan mevcut olay aboneliklerinin taşınmasına olanak tanımak amacıyla Event Grid Etki Alanı adının ve/veya Event Grid Etki Alanı Konu Başlığı adını belirtmek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="50143-2279">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="50143-2280">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="50143-2280">Az.FrontDoor</span></span>
* <span data-ttu-id="50143-2281">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="50143-2281">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="50143-2282">Dönüştürmeler desteği ve yeni işleç otomatik tamamlama değeri (RegEx) ekler</span><span class="sxs-lookup"><span data-stu-id="50143-2282">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="50143-2283">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="50143-2283">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="50143-2284">Yeni otomatik tamamlama değerleri ekler</span><span class="sxs-lookup"><span data-stu-id="50143-2284">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="50143-2285">Az.Network</span><span class="sxs-lookup"><span data-stu-id="50143-2285">Az.Network</span></span>
* <span data-ttu-id="50143-2286">Sanal Ağ Geçidi Kaynağı için destek ekler</span><span class="sxs-lookup"><span data-stu-id="50143-2286">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="50143-2287">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="50143-2287">New cmdlets</span></span>
        - <span data-ttu-id="50143-2288">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="50143-2288">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="50143-2289">AvailablePrivateEndpointType ekler</span><span class="sxs-lookup"><span data-stu-id="50143-2289">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="50143-2290">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="50143-2290">New cmdlets</span></span>
        - <span data-ttu-id="50143-2291">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="50143-2291">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="50143-2292">PrivatePrivateLinkService ekler</span><span class="sxs-lookup"><span data-stu-id="50143-2292">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="50143-2293">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="50143-2293">New cmdlets</span></span>
        - <span data-ttu-id="50143-2294">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="50143-2294">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="50143-2295">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="50143-2295">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="50143-2296">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="50143-2296">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="50143-2297">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="50143-2297">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="50143-2298">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="50143-2298">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="50143-2299">PrivateEndpoint ekler</span><span class="sxs-lookup"><span data-stu-id="50143-2299">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="50143-2300">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="50143-2300">New cmdlets</span></span>
        - <span data-ttu-id="50143-2301">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="50143-2301">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="50143-2302">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="50143-2302">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="50143-2303">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="50143-2303">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="50143-2304">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="50143-2304">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="50143-2305">Özellik için aşağıdaki komutlar güncelleştirildi: VpnConnection’da UseLocalAzureIpAddress bayrağı</span><span class="sxs-lookup"><span data-stu-id="50143-2305">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="50143-2306">New-AzVpnConnection güncelleştirildi: Bağlantı başlatılırken yerel Azure IP adresinin kullanılması gerektiğini belirtmek için isteğe bağlı -UseLocalAzureIpAddress parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-2306">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="50143-2307">Set-AzVpnConnection güncelleştirildi: Bağlantı başlatılırken yerel Azure IP adresinin kullanılması gerektiğini belirtmek için isteğe bağlı -UseLocalAzureIpAddress parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-2307">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="50143-2308">ExpressRoute eşlemede PeeredConnections salt okunur alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-2308">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="50143-2309">ExpressRoute’ta GlobalReachEnabled salt okunur alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-2309">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="50143-2310">ExpressRouteCircuit modelindeki AllowGlobalReach alanının kullanımdan kaldırıldığını duyurmak için hataya neden olan değişiklik özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2310">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="50143-2311">AzApplicationGatewayRedirectConfiguration cmdlet’leri ile TargetListenerID’yi kullanırken oluşan 8756 Hatası Sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2311">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="50143-2312">New-AzApplicationGatewayPathRuleConfig’de yeniden yazma kuralının ayarlanmasını engelleyen hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-2312">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="50143-2313">NetworkInterfaceIpConfiguration’da VirtualNetworkTaps’in görüntülenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2313">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="50143-2314">Tümünü listele bölümü için Cortex Get cmdlet’leri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2314">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="50143-2315">ExpressRouteGateways ve VpnGateway için VirtualHub başvurusu oluşturma düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2315">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="50143-2316">AzureFirewall ve NatGateway için Kullanılabilirlik Alanları desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2316">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="50143-2317">Get-AzNetworkServiceTag cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2317">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="50143-2318">Azure Güvenlik Duvarı için birden fazla genel IP adresi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2318">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="50143-2319">New-AzFirewall cmdlet'i güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="50143-2319">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="50143-2320">Bir veya daha fazla Genel IP Adresi nesnesi kabul eden -PublicIpAddress parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2320">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="50143-2321">Bir Sanal Ağ nesnesini kabul eden -VirtualNetwork parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2321">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="50143-2322">Güvenlik duvarı nesnesine AddPublicIpAddress ve RemovePublicIpAddress yöntemleri eklendi - bunlar giriş olarak Genel IP Adresi nesnesini kabul eder</span><span class="sxs-lookup"><span data-stu-id="50143-2322">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="50143-2323">Kullanım dışı parametreler - PublicIpName ve -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="50143-2323">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="50143-2324">Özellik için aşağıdaki komutlar güncelleştirildi: Sanal ağ geçidi kaynağına VpnClient AAD kimlik doğrulaması seçenekleri ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="50143-2324">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="50143-2325">New-AzVirtualNetworkGateway güncelleştirildi: Ağ Geçidinde VpnClient AAD kimlik doğrulamasını ayarlamak için isteğe bağlı AadTenantUri, AadAudienceId, AadIssuerUri parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-2325">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="50143-2326">Set-AzVirtualNetworkGateway güncelleştirildi: Ağ Geçidinde VpnClient AAD kimlik doğrulamasını ayarlamak için isteğe bağlı AadTenantUri, AadAudienceId, AadIssuerUri parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-2326">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="50143-2327">Set-AzVirtualNetworkGateway güncelleştirildi: VpnClient AAD kimlik doğrulaması seçeneklerini Ağ Geçidinden kaldırmak için isteğe bağlı RemoveAadAuthentication anahtar parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-2327">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="50143-2328">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="50143-2328">Az.OperationalInsights</span></span>
* <span data-ttu-id="50143-2329">‘New-Azurermoperationalınsightsworkspace’ komutunda **pergb2018** fiyatlandırma katmanı etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2329">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="50143-2330">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="50143-2330">Az.Resources</span></span>
* <span data-ttu-id="50143-2331">Ek Şablon Dışarı Aktarma seçenekleri için destek</span><span class="sxs-lookup"><span data-stu-id="50143-2331">Support for additional Template Export options</span></span>
    - <span data-ttu-id="50143-2332">Export-AzResourceGroup’a ‘-SkipResourceNameParameterization’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2332">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="50143-2333">Export-AzResourceGroup’a ‘-SkipAllParameterization’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2333">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="50143-2334">Dışarı aktarılan kaynak filtrelemesi için Export-AzResourceGroup’a ‘Resource’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2334">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="50143-2335">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="50143-2335">Az.ServiceFabric</span></span>
* <span data-ttu-id="50143-2336">ByExistingKeyVault sertifika eklemenin bazı durumlarda yanlış parmak izi alması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2336">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="50143-2337">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="50143-2337">Az.Sql</span></span>
* <span data-ttu-id="50143-2338">Gelişmiş Tehdit Koruması depolama uç noktası son eki düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2338">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="50143-2339">Gelişmiş Veri Güvenliği’ni etkinleştirmenin Gelişmiş Tehdit Koruması ilkesini geçersiz kılması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2339">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="50143-2340">Müşterilerin yönetilen örnekler için TDE anahtarları ekleyip TDE koruyucusu ayarlamasına olanak tanımak için Management.Sql’e yönelik yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="50143-2340">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="50143-2341">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="50143-2341">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="50143-2342">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="50143-2342">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="50143-2343">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="50143-2343">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="50143-2344">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="50143-2344">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="50143-2345">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="50143-2345">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="50143-2346">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="50143-2346">Az.Storage</span></span>
* <span data-ttu-id="50143-2347">Depolama hesabı oluştururken FileStorage ve SkuName Premium_ZRS tiplerine yönelik destek</span><span class="sxs-lookup"><span data-stu-id="50143-2347">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="50143-2348">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="50143-2348">New-AzStorageAccount</span></span>
* <span data-ttu-id="50143-2349">Blob değiştirilemezlik cmdlet’inin açıklaması netleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2349">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="50143-2350">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="50143-2350">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="50143-2351">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="50143-2351">Az.Websites</span></span>
* <span data-ttu-id="50143-2352">Kaynak grubu ile filtrelemeyi istemci yerine sunucuda yapmasını sağlayarak Get-AzWebAppCertificate’ı iyileştirir</span><span class="sxs-lookup"><span data-stu-id="50143-2352">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="50143-2353">Get-AzWebAppSnapshot’a -UseDisasterRecovery anahtar parametresi ekler</span><span class="sxs-lookup"><span data-stu-id="50143-2353">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="50143-2354">2.2.0 - Haziran 2019</span><span class="sxs-lookup"><span data-stu-id="50143-2354">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="50143-2355">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="50143-2355">Az.Cdn</span></span>
* <span data-ttu-id="50143-2356">Cmdlet'ler API sürümü 2019-04-15’i temel alan rulesEngine özelliğini destekleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-2356">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="50143-2357">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="50143-2357">Az.Compute</span></span>
* <span data-ttu-id="50143-2358">İşlemi başlatan ve işlem tamamlanmadan önce hemen döndürülen `NoWait` parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-2358">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="50143-2359">Cmdlet'ler güncelleştirildi:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="50143-2359">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="50143-2360">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="50143-2360">Az.EventHub</span></span>
* <span data-ttu-id="50143-2361">#9231 - Get-AzEventHubNamespace etiketleri döndürmüyor hatasının düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="50143-2361">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="50143-2362">#9230 - Get-AzEventHubNamespace ResourceGroupName yerine ResourceGroup döndürüyor hatasının düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="50143-2362">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="50143-2363">Az.Network</span><span class="sxs-lookup"><span data-stu-id="50143-2363">Az.Network</span></span>
* <span data-ttu-id="50143-2364">Nat Gateway için ResourceId ve InputObject değerleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2364">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="50143-2365">ResourceId ve InputObject için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2365">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="50143-2366">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="50143-2366">Az.PolicyInsights</span></span>
* <span data-ttu-id="50143-2367">Get-AzPolicyEvent’de Boş referans sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2367">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="50143-2368">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="50143-2368">Az.RecoveryServices</span></span>
* <span data-ttu-id="50143-2369">IaaSVM ilkesinin gün cinsinden en kısa saklama süresi 1'den 7'ye değiştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2369">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="50143-2370">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="50143-2370">Az.ServiceBus</span></span>
* <span data-ttu-id="50143-2371">#9182 - Get-AzServiceBusNamespace ResourceGroupName yerine ResourceGroup döndürüyor sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="50143-2371">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="50143-2372">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="50143-2372">Az.ServiceFabric</span></span>
* <span data-ttu-id="50143-2373">'Update-AzServiceFabricReliability' hata iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2373">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="50143-2374">Service Fabric komut satırlarındaki eksik karakter düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2374">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="50143-2375">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="50143-2375">Az.Sql</span></span>
* <span data-ttu-id="50143-2376">Yönetilen Örnek için AutoDr’yi desteklemek amacıyla New-AzureSqlInstance cmdlet’ine DnsZonePartner parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-2376">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="50143-2377">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet’i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="50143-2377">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="50143-2378">Gelişmiş Tehdit Koruması için Tehdit Algılama cmdlet’leri yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="50143-2378">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="50143-2379">New-AzSqlInstance - StorageSizeInGB ve -LicenseType parametreleri artık isteğe bağlı.</span><span class="sxs-lookup"><span data-stu-id="50143-2379">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="50143-2380">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="50143-2380">Az.Websites</span></span>
* <span data-ttu-id="50143-2381">Set-AzWebApp ve Set-AzWebAppSlot, WebApp özelliğiyle kullanıldığında etiketlerin kaldırılmasına neden olan sorun giderildi</span><span class="sxs-lookup"><span data-stu-id="50143-2381">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="50143-2382">2.1.0 - Mayıs 2019</span><span class="sxs-lookup"><span data-stu-id="50143-2382">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="50143-2383">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="50143-2383">Az.ApiManagement</span></span>
* <span data-ttu-id="50143-2384">Genel Kapsamda ve API Kapsamında tanılamaları yönetmek için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="50143-2384">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="50143-2385">**Get-AzApiManagementDiagnostic** - Genel kapsam veya API Kapsamında yapılandırılan tanılamaları alır</span><span class="sxs-lookup"><span data-stu-id="50143-2385">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="50143-2386">**New-AzApiManagementDiagnostic** - Genel kapsamda veya API Kapsamında yeni tanılama oluşturur</span><span class="sxs-lookup"><span data-stu-id="50143-2386">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="50143-2387">**New-AzApiManagementHttpMessageDiagnostic** - Üst Bilgileri günlüğe kaydetme ve Gövde Baytları boyutu için tanılama ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="50143-2387">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="50143-2388">**New-AzApiManagementPipelineDiagnosticSetting** - Ağ Geçidinde gelen/giden HTTP iletileri için Tanılama ayarları oluşturur.</span><span class="sxs-lookup"><span data-stu-id="50143-2388">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="50143-2389">**New-AzApiManagementSamplingSetting** - Tanılamaya yönelik istekler/yanıtlar için Örnekleme Ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="50143-2389">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="50143-2390">**Remove-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama varlığını kaldırır</span><span class="sxs-lookup"><span data-stu-id="50143-2390">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="50143-2391">**Set-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama Varlığını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="50143-2391">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="50143-2392">ApiManagement hizmetinde Önbellek yönetimi için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="50143-2392">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="50143-2393">**Get-AzApiManagementCache** - Tanımlayıcı tarafından belirtilen Önbelleğin veya tüm önbelleklerin ayrıntılarını alır</span><span class="sxs-lookup"><span data-stu-id="50143-2393">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="50143-2394">**New-AzApiManagementCache** - Yeni bir 'varsayılan' Önbellek veya belirli bir azure 'bölgesinde' Önbellek oluşturur</span><span class="sxs-lookup"><span data-stu-id="50143-2394">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="50143-2395">**Remove-AzApiManagementCache** - Önbelleği kaldırır</span><span class="sxs-lookup"><span data-stu-id="50143-2395">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="50143-2396">**Update-AzApiManagementCache** - Önbelleği güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="50143-2396">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="50143-2397">API Şemasını yönetmek için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="50143-2397">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="50143-2398">**New-AzApiManagementSchema** - API için yeni Şema oluşturur</span><span class="sxs-lookup"><span data-stu-id="50143-2398">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="50143-2399">**Get-AzApiManagementSchema** - API'de yapılandırılan şemaları alır</span><span class="sxs-lookup"><span data-stu-id="50143-2399">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="50143-2400">**Remove-AzApiManagementSchema** - API'de yapılandırılan şemaları kaldırır</span><span class="sxs-lookup"><span data-stu-id="50143-2400">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="50143-2401">**Set-AzApiManagementSchema** - API'de yapılandırılan şemayı güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="50143-2401">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="50143-2402">Kullanıcı Belirteci oluşturmak için yeni Cmdlet oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="50143-2402">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="50143-2403">**New-AzApiManagementUserToken** - Varsayılan olarak 8 saat geçerli kalan yeni bir Kullanıcı Belirteci oluşturur. 'GIT' kullanıcısı için bu cmdlet kullanılarak Belirteç oluşturulabilir./</span><span class="sxs-lookup"><span data-stu-id="50143-2403">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="50143-2404">Ağ Durumunu almak için yeni cmdlet oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="50143-2404">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="50143-2405">**Get-AzApiManagementNetworkStatus** - API Management hizmetinin bağımlı olduğu kaynakların bağlantısında ağ durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="50143-2405">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="50143-2406">ApiManagement hizmeti Sanal Ağa dağıtılırken ve bağımlılıklardan herhangi birinin bozulup bozulmadığı denetlenirken bu cmdlet yararlı olur.</span><span class="sxs-lookup"><span data-stu-id="50143-2406">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="50143-2407">**New-AzApiManagement** cmdlet'i ApiManagement hizmetini yönetecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2407">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="50143-2408">Yeni 'Consumption' SKU'su için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2408">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="50143-2409">'Consumption' SKU'sunda 'EnableClientCertificate' bayrağını etkinleştirmek için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2409">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="50143-2410">Yeni **New-AzApiManagementSslSetting** cmdlet'i 'Backend' ve 'Frontend'de 'TLS/SSL' ayarını yapılandırmaya olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="50143-2410">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="50143-2411">Bu cmdlet ApiManagement hizmetinin 'Frontend'inde '3DES' gibi 'Ciphers' yapılandırması ve 'Http2' gibi 'ServerProtocols' yapılandırması için de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="50143-2411">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="50143-2412">ApiManagement hizmetinde 'DeveloperPortal' ana bilgisayar adının yapılandırması için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-2412">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="50143-2413">**Get-AzApiManagementSsoToken** cmdlet'leri giriş olarak 'PsApiManagement' nesnesini alacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2413">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="50143-2414">Cmdlet satır içinde Hata İletileri görüntüleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2414">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="50143-2415">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Hata Kodu: ValidationError Hata İletisi: Bir veya birden çok alan yanlış değerler içeriyor: Hata Ayrıntıları:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="50143-2415">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="50143-2416">**Export-AzApiManagementApi** cmdlet'i API'leri 'OpenApi 3.0' biçiminde dışarı aktaracak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2416">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="50143-2417">**Import-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2417">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="50143-2418">'OpenApi 3.0' belge belirtiminden Api'yi içeri aktarmak için</span><span class="sxs-lookup"><span data-stu-id="50143-2418">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="50143-2419">Herhangi bir ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') belgesinde belirtilen 'PsApiManagementSchema' özelliğini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="50143-2419">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="50143-2420">Herhangi bir belgede belirtilen 'ServiceUrl' özelliğini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="50143-2420">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="50143-2421">**Get-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak döndürecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2421">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="50143-2422">**Set-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak ve 'xml' kullanarak Xml kaçışlı kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2422">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="50143-2423">**New-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2423">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="50143-2424">API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="50143-2424">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="50143-2425">'ApiVersionSet' içinde API oluşturmak için</span><span class="sxs-lookup"><span data-stu-id="50143-2425">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="50143-2426">'SourceApiId' ve 'SourceApiRevision' kullanıp API'yi kopyalamak için.</span><span class="sxs-lookup"><span data-stu-id="50143-2426">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="50143-2427">Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği.</span><span class="sxs-lookup"><span data-stu-id="50143-2427">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="50143-2428">**Set-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2428">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="50143-2429">API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="50143-2429">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="50143-2430">API'yi 'ApiVersionSet' olarak güncelleştirmek için</span><span class="sxs-lookup"><span data-stu-id="50143-2430">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="50143-2431">Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği.</span><span class="sxs-lookup"><span data-stu-id="50143-2431">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="50143-2432">**New-AzApiManagementRevision** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2432">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="50143-2433">'SourceApiRevision' kullanarak mevcut düzeltmeyi kopyalamak (etiketleri, ürünleri, işlemleri ve ilkeleri kopyalamak) için.</span><span class="sxs-lookup"><span data-stu-id="50143-2433">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="50143-2434">Yeni Düzeltme üst öğenin 'ApiId' değerini varsayılan olarak alır.</span><span class="sxs-lookup"><span data-stu-id="50143-2434">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="50143-2435">'ApiRevisionDescription' sağlamak için</span><span class="sxs-lookup"><span data-stu-id="50143-2435">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="50143-2436">API kopyalanırken 'ServiceUrl' değerini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="50143-2436">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="50143-2437">**New-AzApiManagementIdentityProvider** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2437">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="50143-2438">'AAD' veya 'AADB2C'yi bir 'Authority' ile yapılandırmak için</span><span class="sxs-lookup"><span data-stu-id="50143-2438">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="50143-2439">'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' ve 'PasswordResetPolicy' ayarlamak için</span><span class="sxs-lookup"><span data-stu-id="50143-2439">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="50143-2440">**New-AzApiManagementSubscription** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2440">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="50143-2441">'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="50143-2441">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="50143-2442">'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="50143-2442">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="50143-2443">Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-2443">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="50143-2444">**Set-AzApiManagementSubscription** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2444">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="50143-2445">'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="50143-2445">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="50143-2446">'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="50143-2446">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="50143-2447">Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-2447">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="50143-2448">Aşağıdaki cmdlet'ler giriş olarak 'ResourceId' kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2448">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="50143-2449">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="50143-2449">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="50143-2450">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="50143-2450">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="50143-2451">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="50143-2451">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="50143-2452">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="50143-2452">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="50143-2453">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="50143-2453">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="50143-2454">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="50143-2454">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="50143-2455">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="50143-2455">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="50143-2456">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="50143-2456">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="50143-2457">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="50143-2457">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="50143-2458">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="50143-2458">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="50143-2459">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="50143-2459">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="50143-2460">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="50143-2460">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="50143-2461">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="50143-2461">Az.Automation</span></span>
* <span data-ttu-id="50143-2462">Get-AzAutomationJobOutputRecord, JSON ve Text kayıt değerlerini işleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-2462">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="50143-2463">[https://github.com/Azure/azure-powershell/issues/8347](https://github.com/Azure/azure-powershell/issues/7977 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2463">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="50143-2464">[https://github.com/Azure/azure-powershell/issues/8347](https://github.com/Azure/azure-powershell/issues/8600 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2464">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="50143-2465">Start-AzAutomationDscCompilationJob cmdlet'inin davranışı tamamlanmasını beklemek yerine yalnızca işi başlatacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-2465">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="50143-2466">[https://github.com/Azure/azure-powershell/issues/8347](https://github.com/Azure/azure-powershell/issues/8347 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2466">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="50143-2467">Get-AzAutomationDscNode için -Name kullanıldığında tüm düğümlerin döndürülmesi sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-2467">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="50143-2468">Artık yalnızca eşleşen düğüm döndürülüyor.</span><span class="sxs-lookup"><span data-stu-id="50143-2468">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="50143-2469">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="50143-2469">Az.Compute</span></span>
* <span data-ttu-id="50143-2470">Update-AzVmssVM cmdlet'ine ProtectFromScaleIn ve ProtectFromScaleSetAction parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-2470">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="50143-2471">New-AzVM basit parametre kümesi artık 'East US' desteklenmiyorsa varsayılan olarak kullanılabilir bir konumu kullanıyor</span><span class="sxs-lookup"><span data-stu-id="50143-2471">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="50143-2472">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="50143-2472">Az.DataLakeStore</span></span>
* <span data-ttu-id="50143-2473">ADLS sdk'si azure çerçevesiyle httpclient, tümleşik veri düzlemi testi kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2473">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="50143-2474">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="50143-2474">Az.Monitor</span></span>
* <span data-ttu-id="50143-2475">Yardım örneklerindeki yanlış parametre adları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2475">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="50143-2476">Az.Network</span><span class="sxs-lookup"><span data-stu-id="50143-2476">Az.Network</span></span>
* <span data-ttu-id="50143-2477">Etkin Yol Tablosu çıkışına DisableBgpRoutePropagation bayrağı eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2477">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="50143-2478">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="50143-2478">Updated cmdlet:</span></span>
        - <span data-ttu-id="50143-2479">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="50143-2479">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="50143-2480">New-AzApplicationGatewayTrustedRootCertificate belgelerindeki çift tire düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2480">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="50143-2481">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="50143-2481">Az.Resources</span></span>
* <span data-ttu-id="50143-2482">Reddetme atamalarını almak için yeni Get-AzureRmDenyAssignment cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2482">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="50143-2483">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="50143-2483">Az.Sql</span></span>
* <span data-ttu-id="50143-2484">Gelişmiş Tehdit Koruması (Advanced Threat Protection) cmdlet'leri Gelişmiş Veri Güvenliği (Advanced Data Security) olarak yeniden adlandırıldı ve varsayılan olarak Güvenlik Açığı Değerlendirmesi etkinleştiriliyor</span><span class="sxs-lookup"><span data-stu-id="50143-2484">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="50143-2485">2.0.0 - Mayıs 2019</span><span class="sxs-lookup"><span data-stu-id="50143-2485">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="50143-2486">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="50143-2486">Az.Accounts</span></span>
* <span data-ttu-id="50143-2487">Kullanıcı adı/parola kimlik doğrulamasıyla ilişkili ADFS sorunlarını düzeltmek için Authentication Library’i güncelleştirin</span><span class="sxs-lookup"><span data-stu-id="50143-2487">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="50143-2488">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="50143-2488">Az.CognitiveServices</span></span>
* <span data-ttu-id="50143-2489">Yalnızca Bing Arama Hizmetleri için Bing bildirimini görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="50143-2489">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="50143-2490">Hesap oluşturma başarısız olduğunda hata iletisini geliştirin.</span><span class="sxs-lookup"><span data-stu-id="50143-2490">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="50143-2491">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="50143-2491">Az.Compute</span></span>
* <span data-ttu-id="50143-2492">Yakınlık yerleştirme grubu özelliği.</span><span class="sxs-lookup"><span data-stu-id="50143-2492">Proximity placement group feature.</span></span>
    - <span data-ttu-id="50143-2493">Aşağıdaki yeni cmdlet’ler eklendi:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="50143-2493">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="50143-2494">Yeni ProximityPlacementGroupId parametresi aşağıdaki cmdlet'lere eklendi:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="50143-2494">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="50143-2495">StorageAccountType parametresi New-AzGalleryImageVersion öğesine eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-2495">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="50143-2496">New-AzGalleryImageVersion komutunun TargetRegion parametresi StorageAccountType içerebilir.</span><span class="sxs-lookup"><span data-stu-id="50143-2496">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="50143-2497">SkipShutdown anahtar parametresi Stop-AzVM ve Stop-AzVmss öğelerine eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2497">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="50143-2498">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="50143-2498">Breaking changes</span></span>
    - <span data-ttu-id="50143-2499">Set-AzVMBootDiagnostics, Set-AzVMBootDiagnostic olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-2499">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="50143-2500">Export-AzLogAnalyticThrottledRequests, Export-AzLogAnalyticThrottledRequests olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-2500">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="50143-2501">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="50143-2501">Az.DeploymentManager</span></span>
* <span data-ttu-id="50143-2502">Azure Deployment Manager cmdlet’lerinin Genel Kullanıma sunulan ilk sürümü</span><span class="sxs-lookup"><span data-stu-id="50143-2502">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="50143-2503">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="50143-2503">Az.Dns</span></span>
* <span data-ttu-id="50143-2504">Otomatik DNS NameServer Temsilcisi</span><span class="sxs-lookup"><span data-stu-id="50143-2504">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="50143-2505">Create DNS zone cmdlet’i üst bölge adını isteğe bağlı bir ek parametre olarak kabul eder.</span><span class="sxs-lookup"><span data-stu-id="50143-2505">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="50143-2506">Yeni oluşturulan alt bölge için NS kayıtlarını üst bölgeye ekler.</span><span class="sxs-lookup"><span data-stu-id="50143-2506">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="50143-2507">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="50143-2507">Az.FrontDoor</span></span>
* <span data-ttu-id="50143-2508">Azure FrontDoor cmdlet’lerinin Genel Kullanıma Sunulan ilk sürümü</span><span class="sxs-lookup"><span data-stu-id="50143-2508">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="50143-2509">WAF cmdlet'lerini 'Waf' içerecek şekilde yeniden adlandırın</span><span class="sxs-lookup"><span data-stu-id="50143-2509">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="50143-2510">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="50143-2510">Az.HDInsight</span></span>
* <span data-ttu-id="50143-2511">İki cmdlet kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="50143-2511">Removed two cmdlets:</span></span>
    - <span data-ttu-id="50143-2512">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="50143-2512">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="50143-2513">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="50143-2513">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="50143-2514">Grant-AzHDInsightHttpServicesAccess, yeni Set-AzHDInsightGatewayCredential cmdlet’i ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2514">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="50143-2515">Okuyucu rolü ile hdinsight işleç rolünü ayırt etmek için Get-AzHDInsightJobOutput cmdlet’ini güncelleştirin:</span><span class="sxs-lookup"><span data-stu-id="50143-2515">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="50143-2516">Okuyucu rolüne sahip kullanıcıların, 'DefaultStorageAccountKey' parametresini açıkça belirtmesi gerekir, aksi takdirde hata oluşur.</span><span class="sxs-lookup"><span data-stu-id="50143-2516">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="50143-2517">hdinsight işleç rolüne sahip kullanıcılar bu durumdan etkilenmez.</span><span class="sxs-lookup"><span data-stu-id="50143-2517">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="50143-2518">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="50143-2518">Az.Monitor</span></span>
* <span data-ttu-id="50143-2519">SQR API (Zamanlanmış Sorgu Kuralı) için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="50143-2519">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="50143-2520">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="50143-2520">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="50143-2521">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="50143-2521">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="50143-2522">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="50143-2522">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="50143-2523">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="50143-2523">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="50143-2524">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="50143-2524">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="50143-2525">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="50143-2525">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="50143-2526">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="50143-2526">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="50143-2527">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="50143-2527">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="50143-2528">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="50143-2528">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="50143-2529">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="50143-2529">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="50143-2530">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="50143-2530">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="50143-2531">SQR API hakkında [daha fazla](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) bilgi</span><span class="sxs-lookup"><span data-stu-id="50143-2531">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="50143-2532">Az.Monitor.md, GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için cmdlet'leri içerecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2532">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="50143-2533">Az.Network</span><span class="sxs-lookup"><span data-stu-id="50143-2533">Az.Network</span></span>
* <span data-ttu-id="50143-2534">Nat Gateway Resource için destek ekleyin</span><span class="sxs-lookup"><span data-stu-id="50143-2534">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="50143-2535">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="50143-2535">New cmdlets</span></span>
        - <span data-ttu-id="50143-2536">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="50143-2536">New-AzNatGateway</span></span>
        - <span data-ttu-id="50143-2537">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="50143-2537">Get-AzNatGateway</span></span>
        - <span data-ttu-id="50143-2538">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="50143-2538">Set-AzNatGateway</span></span>
        - <span data-ttu-id="50143-2539">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="50143-2539">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="50143-2540">Cmdlet'ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2540">Updated cmdlets</span></span>
        - <span data-ttu-id="50143-2541">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="50143-2541">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="50143-2542">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="50143-2542">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="50143-2543">Özellik için aşağıdaki komutlar güncelleştirildi: Brooklyn Gateway üzerinde özel yollar ayarlama/kaldırma.</span><span class="sxs-lookup"><span data-stu-id="50143-2543">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="50143-2544">New-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-2544">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="50143-2545">Set-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-2545">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="50143-2546">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="50143-2546">Az.PolicyInsights</span></span>
* <span data-ttu-id="50143-2547">İlke değerlendirme ayrıntılarını sorgulama desteği.</span><span class="sxs-lookup"><span data-stu-id="50143-2547">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="50143-2548">Get-AzPolicyState komutuna '-Expand' parametresini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="50143-2548">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="50143-2549">'-Expand PolicyEvaluationDetails' öğesini destekleyin.</span><span class="sxs-lookup"><span data-stu-id="50143-2549">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="50143-2550">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="50143-2550">Az.RecoveryServices</span></span>
* <span data-ttu-id="50143-2551">Abonelikler arası Azure'dan Azure’a konum kurtarma desteği.</span><span class="sxs-lookup"><span data-stu-id="50143-2551">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="50143-2552">Azure Site Recovery için yaklaşan hataya neden olan değişiklikleri işaretleme.</span><span class="sxs-lookup"><span data-stu-id="50143-2552">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="50143-2553">Azure Site Recovery kurtarma planı ve eylem planı için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="50143-2553">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="50143-2554">Azure'dan Azure'a Azure Site Recovery Güncelleştirmesi ağ eşlemesi için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="50143-2554">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="50143-2555">Yönetilen diske yönelik Azure'dan Azure'a Azure Site Recovery güncelleştirmesi koruma yönü için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="50143-2555">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="50143-2556">Diğer küçük düzeltmeler.</span><span class="sxs-lookup"><span data-stu-id="50143-2556">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="50143-2557">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="50143-2557">Az.Relay</span></span>
* <span data-ttu-id="50143-2558">Müşteriye dönük iletilerdeki yazım hatalarını düzeltin</span><span class="sxs-lookup"><span data-stu-id="50143-2558">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="50143-2559">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="50143-2559">Az.ServiceBus</span></span>
* <span data-ttu-id="50143-2560">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2560">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="50143-2561">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="50143-2561">Az.Storage</span></span>
* <span data-ttu-id="50143-2562">Storage Client Library 10.0.1 sürümüne güncelleştirin (bu SDK’daki tüm nesnelerin 'Microsoft.WindowsAzure.Storage. *' ad alanı, 'Microsoft.Azure.Storage.* ' olarak değiştirilir)</span><span class="sxs-lookup"><span data-stu-id="50143-2562">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage. *' to 'Microsoft.Azure.Storage.* ')</span></span>
* <span data-ttu-id="50143-2563">Yeni 2019-04-01 API sürümünü desteklemek için Microsoft.Azure.Management.Storage 11.0.0 sürümüne güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="50143-2563">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="50143-2564">Depolama hesabı oluştur komutundaki varsayılan 'Storage' Depolama hesabı Türü 'StorageV2' olarak değişir</span><span class="sxs-lookup"><span data-stu-id="50143-2564">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="50143-2565">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="50143-2565">New-AzStorageAccount</span></span>
* <span data-ttu-id="50143-2566">'StandardLRS' öğesinin 'Standard_LRS' olarak değiştirilmesi gibi, '-' ekleyerek Sku.Name Depolama hesabı cmdlet çıkışını giriş SkuName ile hizalanacak şekilde değiştirin</span><span class="sxs-lookup"><span data-stu-id="50143-2566">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="50143-2567">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="50143-2567">New-AzStorageAccount</span></span>
    - <span data-ttu-id="50143-2568">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="50143-2568">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="50143-2569">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="50143-2569">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="50143-2570">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="50143-2570">Az.Websites</span></span>
* <span data-ttu-id="50143-2571">'Kind' özelliği artık Get-AzWebApp tarafından döndürülen PSSite nesneleri için ayarlanır</span><span class="sxs-lookup"><span data-stu-id="50143-2571">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="50143-2572">Get-AzWebApp\*Metrics ve Get-AzAppServicePlanMetrics, kullanım dışı olarak işaretlendi</span><span class="sxs-lookup"><span data-stu-id="50143-2572">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="50143-2573">1.8.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="50143-2573">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="50143-2574">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="50143-2574">Highlights since the last major release</span></span>
* <span data-ttu-id="50143-2575">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="50143-2575">General availability of `Az` module</span></span>
* <span data-ttu-id="50143-2576">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="50143-2576">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="50143-2577">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="50143-2577">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="50143-2578">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2578">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="50143-2579">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2579">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="50143-2580">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2580">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="50143-2581">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="50143-2581">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="50143-2582">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="50143-2582">Az.Accounts</span></span>
* <span data-ttu-id="50143-2583">Mac’te modülleri doğru bir biçimde silmek için Uninstall-AzureRm güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2583">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="50143-2584">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="50143-2584">Az.Batch</span></span>
* <span data-ttu-id="50143-2585">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="50143-2585">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="50143-2586">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="50143-2586">Az.Cdn</span></span>
* <span data-ttu-id="50143-2587">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="50143-2587">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="50143-2588">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="50143-2588">Az.CognitiveServices</span></span>
* <span data-ttu-id="50143-2589">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="50143-2589">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="50143-2590">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="50143-2590">Az.Compute</span></span>
* <span data-ttu-id="50143-2591">Disklerin kaynak kimlikleri kaynak kimliğinde küçük harfli kaynak grubu içerdiğinde oluşan AEM yüklemesiyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2591">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="50143-2592">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="50143-2592">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="50143-2593">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2593">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="50143-2594">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="50143-2594">Az.DataFactory</span></span>
* <span data-ttu-id="50143-2595">Yönetilen tümleştirme çalışma zamanı için Nodecount’ın null olmadığı durumlar için SsisProperties eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-2595">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="50143-2596">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="50143-2596">Az.DataLakeStore</span></span>
* <span data-ttu-id="50143-2597">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="50143-2597">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="50143-2598">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="50143-2598">Az.EventGrid</span></span>
* <span data-ttu-id="50143-2599">Oluşturma/güncelleştirme etkinliği için abonelik cmdlet’lerini kullanmadan önce kaynakların oluşturulmasının gerektiğini belirten yardım metni güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-2599">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="50143-2600">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="50143-2600">Az.EventHub</span></span>
* <span data-ttu-id="50143-2601">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2601">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="50143-2602">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="50143-2602">Az.HDInsight</span></span>
* <span data-ttu-id="50143-2603">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="50143-2603">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="50143-2604">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="50143-2604">Az.IotHub</span></span>
* <span data-ttu-id="50143-2605">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="50143-2605">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="50143-2606">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="50143-2606">Az.KeyVault</span></span>
* <span data-ttu-id="50143-2607">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="50143-2607">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="50143-2608">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2608">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="50143-2609">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="50143-2609">Az.MachineLearning</span></span>
* <span data-ttu-id="50143-2610">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="50143-2610">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="50143-2611">Az.Media</span><span class="sxs-lookup"><span data-stu-id="50143-2611">Az.Media</span></span>
* <span data-ttu-id="50143-2612">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="50143-2612">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="50143-2613">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="50143-2613">Az.Monitor</span></span>
  * <span data-ttu-id="50143-2614">GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="50143-2614">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="50143-2615">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="50143-2615">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="50143-2616">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="50143-2616">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="50143-2617">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="50143-2617">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="50143-2618">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="50143-2618">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="50143-2619">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="50143-2619">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="50143-2620">İzleyici SDK’sı 0.22.0-önizleme sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2620">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="50143-2621">Az.Network</span><span class="sxs-lookup"><span data-stu-id="50143-2621">Az.Network</span></span>
* <span data-ttu-id="50143-2622">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="50143-2622">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="50143-2623">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2623">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="50143-2624">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="50143-2624">Az.NotificationHubs</span></span>
* <span data-ttu-id="50143-2625">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="50143-2625">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="50143-2626">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="50143-2626">Az.OperationalInsights</span></span>
* <span data-ttu-id="50143-2627">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="50143-2627">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="50143-2628">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="50143-2628">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="50143-2629">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="50143-2629">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="50143-2630">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="50143-2630">Az.RecoveryServices</span></span>
* <span data-ttu-id="50143-2631">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="50143-2631">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="50143-2632">Azure VM'de SQL için güncelleştirilmiş tablo biçimi</span><span class="sxs-lookup"><span data-stu-id="50143-2632">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="50143-2633">AzureFileShare’de konumu getirmeye yönelik alternatif yöntem eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2633">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="50143-2634">SchedulePolicy nesnesindeki ScheduleRunDays saat dilimine göre güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2634">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="50143-2635">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="50143-2635">Az.RedisCache</span></span>
* <span data-ttu-id="50143-2636">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="50143-2636">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="50143-2637">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="50143-2637">Az.Resources</span></span>
* <span data-ttu-id="50143-2638">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2638">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="50143-2639">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="50143-2639">Az.Sql</span></span>
* <span data-ttu-id="50143-2640">İzleyici SDK’sının bağımlılığı ortak kod ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2640">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="50143-2641">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="50143-2641">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="50143-2642">Birden fazla sütun sınıflandırma işlemi geliştirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-2642">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="50143-2643">Get-AzSqlServerServiceObjective’den alınan yanıta SKU özellikleri (SKU adı, ailesi, kapasitesi) dahil edildi ve bunlar varsayılan olarak tablo şeklinde biçimlendirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-2643">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="50143-2644">Bölgede önceden var olan bir sunucuya ihtiyaç duymadan, konuma göre Get-AzSqlServerServiceObjective yapabilme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-2644">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="50143-2645">Yönetilen Örnek oluşturmadaki saat dilimi parametresi desteği.</span><span class="sxs-lookup"><span data-stu-id="50143-2645">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="50143-2646">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2646">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="50143-2647">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="50143-2647">Az.Websites</span></span>
* <span data-ttu-id="50143-2648">Set-AzWebApp ve Set-AzWebAppSlot çalıştırılırken etiketlerin kaldırılmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2648">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="50143-2649">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="50143-2649">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="50143-2650">Web siteleri SDK'sı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-2650">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="50143-2651">PSAppServicePlan’den AdminSiteName özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="50143-2651">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="50143-2652">1.7.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="50143-2652">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="50143-2653">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="50143-2653">Highlights since the last major release</span></span>
* <span data-ttu-id="50143-2654">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="50143-2654">General availability of `Az` module</span></span>
* <span data-ttu-id="50143-2655">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="50143-2655">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="50143-2656">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="50143-2656">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="50143-2657">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2657">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="50143-2658">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2658">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="50143-2659">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2659">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="50143-2660">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="50143-2660">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="50143-2661">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="50143-2661">Az.Accounts</span></span>
* <span data-ttu-id="50143-2662">Add-AzEnvironment ve Set-AzEnvironment, AzureAnalysisServicesEndpointResourceId parametresini kabul edecek biçimde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2662">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="50143-2663">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="50143-2663">Az.AnalysisServices</span></span>
* <span data-ttu-id="50143-2664">Veri düzlemi cmdlet’lerinde ServiceClient kullanma ve orijinal kimlik doğrulaması mantığını kaldırma</span><span class="sxs-lookup"><span data-stu-id="50143-2664">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="50143-2665">Hataya neden olan değişikliklerden kaçınmak için Add-AzureASAccount’ı Connect-AzAccount’ın sarmalayıcısı yapma</span><span class="sxs-lookup"><span data-stu-id="50143-2665">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="50143-2666">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="50143-2666">Az.Automation</span></span>
* <span data-ttu-id="50143-2667">Eklemeler için New-AzAutomationSoftwareUpdateConfiguration cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-2667">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="50143-2668">IncludedKbNumber ve IncludedPackageNameMask parametrelerinin artık çalışması bekleniyor.</span><span class="sxs-lookup"><span data-stu-id="50143-2668">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="50143-2669">Azure otomasyonu güncelleştirmesi yönetim dinamik grubu için hata düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="50143-2669">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="50143-2670">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="50143-2670">Az.Compute</span></span>
* <span data-ttu-id="50143-2671">New-AzDiskConfig ve New-AzSnapshotConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2671">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="50143-2672">Diğer kiracıların karakter görüntüleriyle VM oluşturmaya izin verildi.</span><span class="sxs-lookup"><span data-stu-id="50143-2672">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="50143-2673">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="50143-2673">Az.ContainerInstance</span></span>
* <span data-ttu-id="50143-2674">New-AzContainerGroup’un -command parametresinde bağımsız boş değişken ekleyen sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2674">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="50143-2675">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="50143-2675">Az.DataFactory</span></span>
* <span data-ttu-id="50143-2676">ADF .Net SDK’sı 3.0.2 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2676">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="50143-2677">Set-AzDataFactoryV2 cmdlet’i RepoConfiguration ile ilgili ayarların ek parametreleriyle güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-2677">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="50143-2678">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="50143-2678">Az.Resources</span></span>
* <span data-ttu-id="50143-2679">'-ResourceId' veya '-ResourceGroupName', '-Name' ve '-ResourceType' parametreleri sağlanırken ‘Get-AzResource’ için sağlayıcıların işlenmesi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2679">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="50143-2680">‘Test-AzDeployment’ ve ‘Test-AzResourceGroupDeployment’ için hata işleme geliştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2680">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="50143-2681">İşleme hataları dağıtım doğrulamasının dışında tutuldu ve komut çıkışına dahil edildi</span><span class="sxs-lookup"><span data-stu-id="50143-2681">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="50143-2682">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="50143-2682">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="50143-2683">Betik ve iş senaryolarında istemi atlamak için bir dizi dağıtım cmdlet’lerine ‘-IgnoreDynamicParameters’ anahtar parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2683">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="50143-2684">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="50143-2684">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="50143-2685">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="50143-2685">Az.Sql</span></span>
* <span data-ttu-id="50143-2686">Veritabanı Verileri Sınıflandırması Desteği.</span><span class="sxs-lookup"><span data-stu-id="50143-2686">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="50143-2687">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="50143-2687">Az.Storage</span></span>
* <span data-ttu-id="50143-2688">-UseConnectedAccount parametresi ile depolama bağlamı oluştururken ayrıntı hatası raporlama</span><span class="sxs-lookup"><span data-stu-id="50143-2688">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="50143-2689">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="50143-2689">New-AzStorageContext</span></span>
* <span data-ttu-id="50143-2690">Belirtilen depolama hesabının Yönetim düzlemi API’si ile Blob Hizmeti Özellikleri için Yönetim Desteği</span><span class="sxs-lookup"><span data-stu-id="50143-2690">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="50143-2691">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="50143-2691">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="50143-2692">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="50143-2692">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="50143-2693">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="50143-2693">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="50143-2694">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="50143-2694">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="50143-2695">Blob ve dosya karşıya yükleme ve indirme cmdlet’leri için -Asjob desteği</span><span class="sxs-lookup"><span data-stu-id="50143-2695">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="50143-2696">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="50143-2696">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="50143-2697">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="50143-2697">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="50143-2698">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="50143-2698">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="50143-2699">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="50143-2699">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="50143-2700">1.6.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="50143-2700">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="50143-2701">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="50143-2701">Highlights since the last major release</span></span>
* <span data-ttu-id="50143-2702">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="50143-2702">General availability of `Az` module</span></span>
* <span data-ttu-id="50143-2703">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="50143-2703">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="50143-2704">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="50143-2704">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="50143-2705">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2705">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="50143-2706">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2706">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="50143-2707">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2707">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="50143-2708">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="50143-2708">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="50143-2709">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="50143-2709">Az.Automation</span></span>
* <span data-ttu-id="50143-2710">Aşağıdaki yeni özellikleri desteklemek için Azure otomasyonu güncelleştirme yönetimi değişikliği:</span><span class="sxs-lookup"><span data-stu-id="50143-2710">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="50143-2711">Dinamik gruplandırma</span><span class="sxs-lookup"><span data-stu-id="50143-2711">Dynamic grouping</span></span>
    * <span data-ttu-id="50143-2712">Ön-Son betik</span><span class="sxs-lookup"><span data-stu-id="50143-2712">Pre-Post script</span></span>
    * <span data-ttu-id="50143-2713">Yeniden Başlatma Ayarı</span><span class="sxs-lookup"><span data-stu-id="50143-2713">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="50143-2714">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="50143-2714">Az.Compute</span></span>
* <span data-ttu-id="50143-2715">Get-AzVmBootDiagnosticsData içinde yol çözümleme sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="50143-2715">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="50143-2716">İşlem istemci kitaplığı 25.0.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-2716">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="50143-2717">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="50143-2717">Az.KeyVault</span></span>
* <span data-ttu-id="50143-2718">KeyVault cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2718">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="50143-2719">Az.Network</span><span class="sxs-lookup"><span data-stu-id="50143-2719">Az.Network</span></span>
* <span data-ttu-id="50143-2720">Azure Güvenlik Duvarı için Tehdit Bilgileri desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2720">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="50143-2721">Application Gateway Güvenlik Duvarı İlkesi üst düzey kaynağı ve Özel Kurallar eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2721">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="50143-2722">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="50143-2722">Az.RecoveryServices</span></span>
* <span data-ttu-id="50143-2723">Anında RP desteği için Azure VM ilkesine SnapshotRetentionInDays eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2723">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="50143-2724">Kapsayıcı kaydını kaldırmak için kanal desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2724">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="50143-2725">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="50143-2725">Az.Resources</span></span>
* <span data-ttu-id="50143-2726">Get-AzResource ve Get-AzResourceGroup için joker karakter desteği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2726">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="50143-2727">ARM'ye genel çağrı yapılırken kullanılan kimlik bilgileri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2727">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="50143-2728">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="50143-2728">Az.Sql</span></span>
* <span data-ttu-id="50143-2729">Yeni DetectionType'lar eklendiğinde gelecekte kullanılabilmesini sağlamak ve otomatik tamamlamayı da desteklemek için Tehdit Algılama cmdlet'lerinin DetectionType olan parametresi (ExcludeDetectionType) string[] olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-2729">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="50143-2730">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="50143-2730">Az.Storage</span></span>
* <span data-ttu-id="50143-2731">Depolama hesabında Yönetim İlkesini Alma/Ayarlama/Kaldırma desteği</span><span class="sxs-lookup"><span data-stu-id="50143-2731">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="50143-2732">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="50143-2732">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="50143-2733">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="50143-2733">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="50143-2734">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="50143-2734">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="50143-2735">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="50143-2735">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="50143-2736">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="50143-2736">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="50143-2737">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="50143-2737">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="50143-2738">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="50143-2738">Az.Websites</span></span>
* <span data-ttu-id="50143-2739">'New-AzWebApp -IncludeSourceWebAppSlots' kullanarak tüm yuvaların kopyalanmasını kesintiye uğratan ARM şablon hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2739">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="50143-2740">1.5.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="50143-2740">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="50143-2741">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="50143-2741">Az.Accounts</span></span>
* <span data-ttu-id="50143-2742">AutoRest tarafından oluşturulan cmdlet’leri desteklemek için 'Register-AzModule' komutu eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2742">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="50143-2743">Connect-AzAccount örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2743">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="50143-2744">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="50143-2744">Az.Automation</span></span>
* <span data-ttu-id="50143-2745">Birden fazla Azure Otomasyonu cmdlet’inde belirli aylık zamanlamalar alınırken yaşanan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2745">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="50143-2746">Yalnızca ilk 20 düğümü döndüren Get-AzAutomationDscNode düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-2746">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="50143-2747">Artık tüm düğümleri döndürür</span><span class="sxs-lookup"><span data-stu-id="50143-2747">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="50143-2748">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="50143-2748">Az.Cdn</span></span>
* <span data-ttu-id="50143-2749">Özel Etki Alanı Https Etkinleştirmesi/Devre Dışı Bırakması için yeni PowerShell cmdlet’leri eklendi ve eskiler kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="50143-2749">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="50143-2750">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="50143-2750">Az.Compute</span></span>
* <span data-ttu-id="50143-2751">Get cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2751">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="50143-2752">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="50143-2752">Az.DataFactory</span></span>
* <span data-ttu-id="50143-2753">ADF .Net SDK sürümü 3.0.1'e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2753">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="50143-2754">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="50143-2754">Az.LogicApp</span></span>
* <span data-ttu-id="50143-2755">Yalnızca ilk sonuç sayfasını getiren ListWorkflows için düzeltme</span><span class="sxs-lookup"><span data-stu-id="50143-2755">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="50143-2756">Az.Network</span><span class="sxs-lookup"><span data-stu-id="50143-2756">Az.Network</span></span>
* <span data-ttu-id="50143-2757">Network cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2757">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="50143-2758">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="50143-2758">Az.RecoveryServices</span></span>
* <span data-ttu-id="50143-2759">Azure VM desteğine SQL Server eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2759">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="50143-2760">SDK Güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="50143-2760">SDK Update</span></span>
* <span data-ttu-id="50143-2761">Get-ProtectableItem içindeki Removed VMappContainer denetimi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="50143-2761">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="50143-2762">Get-ProtectableItem için Name ve ServerName parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2762">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="50143-2763">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="50143-2763">Az.Resources</span></span>
* <span data-ttu-id="50143-2764">Dağıtım cmdlet’lerine `-TemplateObject` parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2764">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="50143-2765">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="50143-2765">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="50143-2766">`Get-AzResource` sonucu `Set-AzResource` üzerine aktarılırken oluşan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2766">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="50143-2767">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="50143-2767">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="50143-2768">`Set-AzResource` çalıştırılırken JSON veri türü değişikliğine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2768">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="50143-2769">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="50143-2769">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="50143-2770">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="50143-2770">Az.Sql</span></span>
* <span data-ttu-id="50143-2771">AuditingEndpointsCommunicator güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="50143-2771">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="50143-2772">Yeni tanılama ayarları oluşturulurken kenar durumunun davranışı düzeltiliyor.</span><span class="sxs-lookup"><span data-stu-id="50143-2772">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="50143-2773">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="50143-2773">Az.Storage</span></span>
* <span data-ttu-id="50143-2774">Depolama hesabı oluşturulurken Support Kind BlockBlobStorage desteği sağlandı      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="50143-2774">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="50143-2775">1.4.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="50143-2775">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="50143-2776">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="50143-2776">Az.AnalysisServices</span></span>
* <span data-ttu-id="50143-2777">AddAzureASAccount cmdlet'i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="50143-2777">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="50143-2778">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="50143-2778">Az.Automation</span></span>
* <span data-ttu-id="50143-2779">Import-AzAutomationDscNodeConfiguration için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2779">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="50143-2780">Import-AzAutomationDscConfiguration cmdlet'ine yapılandırma adı doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2780">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="50143-2781">Import-AzAutomationDscConfiguration cmdlet'i için hata işleme iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2781">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="50143-2782">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="50143-2782">Az.CognitiveServices</span></span>
* <span data-ttu-id="50143-2783">Kaynağın alt etki alanını belirtmek amacıyla kullanılan New-AzCognitiveServicesAccount için CustomSubdomainName adlı, isteğe bağlı, yeni bir parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-2783">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="50143-2784">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="50143-2784">Az.Compute</span></span>
* <span data-ttu-id="50143-2785">Kimlik parametresi kümeleriyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2785">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="50143-2786">Get-AzVMExtension, Name parametresi sağlanmadığında yüklü tüm uzantıları listeleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2786">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="50143-2787">Update-AzImage cmdlet’ine Tag ve ResourceId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2787">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="50143-2788">Get-AzVmssVM, örnek kimliği olmadan ve InstanceView ile, örnek görünümüne sahip VMSS VM’lerini listeleyebilir.</span><span class="sxs-lookup"><span data-stu-id="50143-2788">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="50143-2789">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="50143-2789">Az.DataLakeStore</span></span>
* <span data-ttu-id="50143-2790">ADL silinmiş öğe listeleme ve geri yükleme cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2790">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="50143-2791">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="50143-2791">Az.EventHub</span></span>
* <span data-ttu-id="50143-2792">EventHub’ın CaptureDescription sınıfında Boş Arşivleri Atlamak için SkipEmptyArchives adlı yeni Boole özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2792">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="50143-2793">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="50143-2793">Az.KeyVault</span></span>
* <span data-ttu-id="50143-2794">Set-AzKeyVaultSecret’daki etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2794">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="50143-2795">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="50143-2795">Az.LogicApp</span></span>
* <span data-ttu-id="50143-2796">Tümleştirme Hesapları için Temel SKU eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2796">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="50143-2797">XSLT 2.0, XSLT 3.0 ve Liquid Eşleşme Türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2797">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="50143-2798">Tümleştirme Hesabı Bütünleştirilmiş Kodları için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="50143-2798">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="50143-2799">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="50143-2799">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="50143-2800">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="50143-2800">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="50143-2801">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="50143-2801">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="50143-2802">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="50143-2802">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="50143-2803">Tümleştirme Hesabı Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="50143-2803">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="50143-2804">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="50143-2804">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="50143-2805">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="50143-2805">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="50143-2806">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="50143-2806">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="50143-2807">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="50143-2807">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="50143-2808">Logic Apps SDK sürüm 4.1.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2808">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="50143-2809">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="50143-2809">Az.Monitor</span></span>
* <span data-ttu-id="50143-2810">Get-AzMetric için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2810">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="50143-2811">Az.Network</span><span class="sxs-lookup"><span data-stu-id="50143-2811">Az.Network</span></span>
* <span data-ttu-id="50143-2812">Add-AzApplicationGatewayCustomError için yardım örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2812">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="50143-2813">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="50143-2813">Az.OperationalInsights</span></span>
* <span data-ttu-id="50143-2814">New ve Get ApplicationInsights veri kaynağı için ek destek sunuldu.</span><span class="sxs-lookup"><span data-stu-id="50143-2814">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="50143-2815">Belirli bir çalışma alanı için belirli ve tüm Get ApplicationInsights veri kaynaklarını desteklemek için yeni ‘ApplicationInsights’ türü eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-2815">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="50143-2816">Belirli Application-Insights kaynak parametrelerine (abonelik kimliği, resourceGroupName ve ad) göre veri kaynağı oluşturmak için New-AzOperationalInsightsApplicationInsightsDataSource cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-2816">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="50143-2817">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="50143-2817">Az.Resources</span></span>
* <span data-ttu-id="50143-2818">[https://github.com/Azure/azure-powershell/issues/8166](https://github.com/Azure/azure-powershell/issues/8166 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2818">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="50143-2819">[https://github.com/Azure/azure-powershell/issues/8166](https://github.com/Azure/azure-powershell/issues/8235 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2819">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="50143-2820">[https://github.com/Azure/azure-powershell/issues/8235](https://github.com/Azure/azure-powershell/issues/6219 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2820">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="50143-2821">KeyCredentials’ın tekrar oluşturmasını engelleyen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2821">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="50143-2822">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="50143-2822">Az.Sql</span></span>
* <span data-ttu-id="50143-2823">SQL DB Hiper Ölçek katmanı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2823">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="50143-2824">Geri yükleme isteğinde gereksiz özellikler ayarlandığı için geri yüklemenin başarısız olmasına yol açan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2824">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="50143-2825">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="50143-2825">Az.Websites</span></span>
* <span data-ttu-id="50143-2826">Get-AzWebAppSlotMetrics örneği düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2826">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="50143-2827">1.3.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="50143-2827">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="50143-2828">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="50143-2828">Az.Accounts</span></span>
* <span data-ttu-id="50143-2829">En son ClientRuntime sürümüne güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="50143-2829">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="50143-2830">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="50143-2830">Az.AnalysisServices</span></span>
<span data-ttu-id="50143-2831">Az.AnalysisServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="50143-2831">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="50143-2832">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="50143-2832">Az.Compute</span></span>
* <span data-ttu-id="50143-2833">AEM uzantısı: UltraSSD ile P60,P70 ve P80 diskleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2833">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="50143-2834">Set-AzVMBootDiagnostics yardım açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2834">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="50143-2835">Update-AzImage için yardım açıklaması ve örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2835">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="50143-2836">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="50143-2836">Az.RecoveryServices</span></span>
<span data-ttu-id="50143-2837">Az.RecoveryServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="50143-2837">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="50143-2838">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="50143-2838">Az.Resources</span></span>
* <span data-ttu-id="50143-2839">Kaynak grupları için etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2839">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="50143-2840">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="50143-2840">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="50143-2841">`Get-AzureRmRoleAssignment` komutunun -ErrorAction'a uymama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2841">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="50143-2842">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="50143-2842">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="50143-2843">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="50143-2843">Az.Sql</span></span>
* <span data-ttu-id="50143-2844">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="50143-2844">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="50143-2845">Azure hesabında oturum açılmamasının SQL cmdlet'leri yürütülürken nullref özel durumuna yol açması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2845">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="50143-2846">Get-AzSqlCapability'de null başvuru özel durumu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2846">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="50143-2847">1.2.1 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="50143-2847">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="50143-2848">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="50143-2848">Az.Accounts</span></span>
* <span data-ttu-id="50143-2849">Kimlik Doğrulaması'nın doğru yayınını içeren sürümü</span><span class="sxs-lookup"><span data-stu-id="50143-2849">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="50143-2850">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="50143-2850">Az.AnalysisServices</span></span>
* <span data-ttu-id="50143-2851">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="50143-2851">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="50143-2852">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="50143-2852">Az.RecoveryServices</span></span>
* <span data-ttu-id="50143-2853">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="50143-2853">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="50143-2854">1.2.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="50143-2854">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="50143-2855">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="50143-2855">Az.Accounts</span></span>
* <span data-ttu-id="50143-2856">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2856">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="50143-2857">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2857">Update incorrect online help URLs</span></span>
* <span data-ttu-id="50143-2858">Uninstall-AzureRm için PC Çekirdeğine uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2858">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="50143-2859">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="50143-2859">Az.Aks</span></span>
* <span data-ttu-id="50143-2860">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2860">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="50143-2861">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="50143-2861">Az.Automation</span></span>
* <span data-ttu-id="50143-2862">Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2862">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="50143-2863">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2863">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="50143-2864">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="50143-2864">Az.Cdn</span></span>
* <span data-ttu-id="50143-2865">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2865">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="50143-2866">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="50143-2866">Az.Compute</span></span>
* <span data-ttu-id="50143-2867">Invoke-AzVMReimage cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2867">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="50143-2868">Set-AzVmss'ye TempDisk parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2868">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="50143-2869">New-AzVM'nin uyarı iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2869">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="50143-2870">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="50143-2870">Az.ContainerRegistry</span></span>
* <span data-ttu-id="50143-2871">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2871">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="50143-2872">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="50143-2872">Az.DataFactory</span></span>
* <span data-ttu-id="50143-2873">ADF .Net SDK sürümü 3.0.0'a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2873">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="50143-2874">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="50143-2874">Az.DataLakeStore</span></span>
* <span data-ttu-id="50143-2875">MSI kullanırken ADLS uç noktasındaki sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2875">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="50143-2876">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="50143-2876">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="50143-2877">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2877">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="50143-2878">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="50143-2878">Az.IotHub</span></span>
* <span data-ttu-id="50143-2879">Add-IotHubRoutingEndpoint cmdlet'ine Kodlama biçimi eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-2879">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="50143-2880">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="50143-2880">Az.KeyVault</span></span>
* <span data-ttu-id="50143-2881">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2881">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="50143-2882">Az.Network</span><span class="sxs-lookup"><span data-stu-id="50143-2882">Az.Network</span></span>
* <span data-ttu-id="50143-2883">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2883">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="50143-2884">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="50143-2884">Az.Resources</span></span>
* <span data-ttu-id="50143-2885">'New-AzADAppCredential' ve 'New-AzADSpCredential' başvuru belgelerindeki hatalı örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2885">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="50143-2886">Kaynak grubu dağıtım cmdlet'lerini yürütmeden önce '-TemplateFile' parametresi yolunun çözülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2886">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="50143-2887">Az.Resources: Belgede New-AzureRmPolicyDefinition -Mode varsayılan değeri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2887">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="50143-2888">Az.Resources: [https://github.com/Azure/azure-powershell/issues/9351](https://github.com/Azure/azure-powershell/issues/7522 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2888">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="50143-2889">Az.Resources: [https://github.com/Azure/azure-powershell/issues/9351](https://github.com/Azure/azure-powershell/issues/5747 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2889">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="50143-2890">'PSResourceGroupDeployment' nesnesinin biçimlendirme sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2890">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="50143-2891">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="50143-2891">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="50143-2892">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="50143-2892">Az.ServiceFabric</span></span>
* <span data-ttu-id="50143-2893">VMSS modeline sertifika eklendiğinde ama özel durum oluştuğunda geri alma için hata düzeltmesi: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="50143-2893">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="50143-2894">Bazı hata iletileri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-2894">Fix some error messages.</span></span>
* <span data-ttu-id="50143-2895">Az geçişinde çalışmayan New-AzServiceFabriCluster için varsayılan ARM şablonuyla küme oluşturma sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-2895">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="50143-2896">Uzantıda küme kimliği denetlenerek küme/uygulama sertifikasının yalnızca kümeye karşılık gelen VM Ölçek Kümelerine eklenmesi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-2896">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="50143-2897">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="50143-2897">Az.SignalR</span></span>
* <span data-ttu-id="50143-2898">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2898">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="50143-2899">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="50143-2899">Az.Sql</span></span>
* <span data-ttu-id="50143-2900">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2900">Update incorrect online help URLs</span></span>
* <span data-ttu-id="50143-2901">LicenseType parametresinin parametre açıklaması olası değerlerle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2901">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="50143-2902">Yönetilen örnek kimliği güncelleştirmesinin, güncelleştirilen tek özellik bu olduğunda çalışmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2902">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="50143-2903">Yönetilen örnekte özel harmanlama desteği</span><span class="sxs-lookup"><span data-stu-id="50143-2903">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="50143-2904">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="50143-2904">Az.Storage</span></span>
* <span data-ttu-id="50143-2905">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2905">Update incorrect online help URLs</span></span>
* <span data-ttu-id="50143-2906">Premium Depolama Hesabı klasik Günlük/Ölçüm desteği sağlamadığından, Premium Depolama Hesabında klasik Günlük/Ölçüm için get/set komutları kullanıldığında ayrıntılı hata iletisi veriliyor.</span><span class="sxs-lookup"><span data-stu-id="50143-2906">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="50143-2907">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="50143-2907">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="50143-2908">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="50143-2908">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="50143-2909">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="50143-2909">Az.TrafficManager</span></span>
* <span data-ttu-id="50143-2910">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2910">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="50143-2911">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="50143-2911">Az.Websites</span></span>
* <span data-ttu-id="50143-2912">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2912">Update incorrect online help URLs</span></span>
* <span data-ttu-id="50143-2913">Uygulama ASE'de barındırılıyorsa, sertifikayı doğru kaynak grubuna ve konuma yüklemek için 'New-AzWebAppSSLBinding' düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-2913">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="50143-2914">SSL sertifikası bir uygulamaya bağlanırken etiketlerin üzerine yazılmaması için 'New-AzWebAppSSLBinding' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2914">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="50143-2915">1.1.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="50143-2915">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="50143-2916">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="50143-2916">Az.Accounts</span></span>
* <span data-ttu-id="50143-2917">Enable-AzureRmAlias cmdlet'ine 'Local' Kapsamı eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2917">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="50143-2918">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="50143-2918">Az.Compute</span></span>
* <span data-ttu-id="50143-2919">Restart/Start/Stop/Remove/Set-AzVM ve Save-AzVMImage için ayarlanan ID parametresinde ad artık isteğe bağlı</span><span class="sxs-lookup"><span data-stu-id="50143-2919">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="50143-2920">Yardım dosyalarında ID parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2920">Updated the description of ID in help files</span></span>
* <span data-ttu-id="50143-2921">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="50143-2921">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="50143-2922">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="50143-2922">Az.DataLakeStore</span></span>
* <span data-ttu-id="50143-2923">SDK düzeltmeleri için veri düzleminin SDK sürümü 1.1.14 olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-2923">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="50143-2924">getfilestatus ve liststatus için negatif acesstime ve modificationtime değerlerini işleme yöntemi düzeltildi, async iptal belirteci düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2924">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="50143-2925">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="50143-2925">Az.EventGrid</span></span>
* <span data-ttu-id="50143-2926">2019-01-01 API sürümünü kullanmak için güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-2926">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="50143-2927">Aşağıdaki cmdlet'ler 2019-01-01 API sürümünde yeni senaryoyu destekleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2927">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="50143-2928">New-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="50143-2928">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="50143-2929">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="50143-2929">Event Time-To-Live,</span></span>
        - <span data-ttu-id="50143-2930">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="50143-2930">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="50143-2931">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="50143-2931">Dead letter endpoint.</span></span>
    - <span data-ttu-id="50143-2932">Update-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="50143-2932">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="50143-2933">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="50143-2933">Event Time-To-Live,</span></span>
        - <span data-ttu-id="50143-2934">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="50143-2934">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="50143-2935">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="50143-2935">Dead letter endpoint.</span></span>
* <span data-ttu-id="50143-2936">New-AzureRmEventGridSubscription ve Update-AzureRmEventGridSubscription cmdlet'lerinde EndpointType seçeneği için yeni enum değerleri (storageQueue ve hybridConnection) eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-2936">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="50143-2937">Olay aboneliğini oluşturma veya güncelleştirme işleminde kullanıcının el ile bir eylem yapması beklendiğinde uyarı iletisi gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="50143-2937">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="50143-2938">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="50143-2938">Az.IotHub</span></span>
* <span data-ttu-id="50143-2939">IotHub SDK'sı en son sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2939">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="50143-2940">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="50143-2940">Az.LogicApp</span></span>
* <span data-ttu-id="50143-2941">Get-AzLogicApp, Name değeri belirtilmemiş olanların tümünü listeliyor</span><span class="sxs-lookup"><span data-stu-id="50143-2941">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="50143-2942">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="50143-2942">Az.Resources</span></span>
* <span data-ttu-id="50143-2943">'Get-AzResource' için '-ODataQuery' ve '-ResourceId' parametreleri sağlanırken ortaya çıkan parametre ayarlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2943">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="50143-2944">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="50143-2944">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="50143-2945">New/Set-AzPolicyDefinition cmdlet'lerinde -Custom parametresinin işlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2945">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="50143-2946">New-AzDeployment belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2946">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="50143-2947">'New-AzADUser' için '-MailNickname' parametresi zorunlu hale getirildi</span><span class="sxs-lookup"><span data-stu-id="50143-2947">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="50143-2948">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="50143-2948">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="50143-2949">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="50143-2949">Az.SignalR</span></span>
* <span data-ttu-id="50143-2950">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="50143-2950">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="50143-2951">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="50143-2951">Az.Sql</span></span>
* <span data-ttu-id="50143-2952">Depolama yönetimi istemci bağımlılığı ortak SDK uygulamasına dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="50143-2952">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="50143-2953">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="50143-2953">Az.Storage</span></span>
* <span data-ttu-id="50143-2954">Sas Token, OAuth veya Anonymous ile oluşturulduğunda Storage bağlamının StorageAccountName değeri gerçek Depolama Hesabı Adına ayarlanıyor</span><span class="sxs-lookup"><span data-stu-id="50143-2954">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="50143-2955">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="50143-2955">New-AzStorageContext</span></span>
* <span data-ttu-id="50143-2956">Blob Anlık Görüntü Nesnesinin Sas Belirteci '-FullUri' parametresiyle oluşturulduğunda, döndürülen Uri anlık görüntü Uri'si olacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2956">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="50143-2957">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="50143-2957">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="50143-2958">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="50143-2958">Az.Websites</span></span>
* <span data-ttu-id="50143-2959">'Get-AzDeletedWebApp' cmdlet'indeki tarih ayrıştırma hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2959">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="50143-2960">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="50143-2960">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="50143-2961">1.0.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="50143-2961">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="50143-2962">Genel</span><span class="sxs-lookup"><span data-stu-id="50143-2962">General</span></span>

- <span data-ttu-id="50143-2963">Az Modülü Genel Kullanıma Sunuldu</span><span class="sxs-lookup"><span data-stu-id="50143-2963">General Availability of Az Module</span></span>
- <span data-ttu-id="50143-2964">Her modül için çevrimiçi yardım</span><span class="sxs-lookup"><span data-stu-id="50143-2964">Online help for each module</span></span>
- <span data-ttu-id="50143-2965">Diğer ayrıntılar ve yol haritası için bkz. [Az Duyuru Sayfası](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="50143-2965">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="50143-2966">AzureRM’den geçiş hakkında bilgi edinmek için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="50143-2966">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="50143-2967">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="50143-2967">Az.Accounts</span></span>
- <span data-ttu-id="50143-2968">Önceki adı: Az.Profile</span><span class="sxs-lookup"><span data-stu-id="50143-2968">Changed from Az.Profile</span></span>
- <span data-ttu-id="50143-2969">Profil ve bağlam türleri için tablo biçimleri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-2969">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="50143-2970">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="50143-2970">Az.ApiManagement</span></span>
- <span data-ttu-id="50143-2971">#7002 düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="50143-2971">Fixes for #7002</span></span>
- <span data-ttu-id="50143-2972">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="50143-2972">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="50143-2973">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="50143-2973">Az.Batch</span></span>
- <span data-ttu-id="50143-2974">`PSComputeNode` üzerinde yeni `NodeAgentInformation` aracılığıyla bir havuzdaki her bir VM’de Azure Batch Düğüm Aracısı’nın hangi sürümünün çalıştığını görme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-2974">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="50143-2975">`PSDataDisk` için `Caching` varsayılan ayarı artık `None` yerine `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="50143-2975">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="50143-2976">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="50143-2976">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="50143-2977">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="50143-2977">Az.Billing</span></span>
- <span data-ttu-id="50143-2978">Billing, Consumption ve UsageAggregates cmdlet’lerini birleştirir, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="50143-2978">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="50143-2979">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="50143-2979">Az.CognitivServices</span></span>
- <span data-ttu-id="50143-2980">New-AzureRmCognitiveServicesAccount işleminde kullanılabilen SkuName ve Typem için tamamlayıcılar eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2980">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="50143-2981">Get-AzCognitiveServicesAccountSkus cmdlet’inden GetSkusWithAccountParamSetName parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="50143-2981">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="50143-2982">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="50143-2982">Az.ContainerInstance</span></span>
- <span data-ttu-id="50143-2983">ManagedIdentity desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2983">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="50143-2984">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="50143-2984">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="50143-2985">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="50143-2985">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="50143-2986">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="50143-2986">Az.DataLakeStore</span></span>
- <span data-ttu-id="50143-2987">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="50143-2987">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="50143-2988">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="50143-2988">Az.Monitor</span></span>
- <span data-ttu-id="50143-2989">Az.Insights cmdlet’inin adı Az.Monitor olarak değiştirildi ve başka yeni değişiklikler yapıldı, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="50143-2989">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="50143-2990">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="50143-2990">Az.KeyVault</span></span>
- <span data-ttu-id="50143-2991">Çıkış türlerinden kullanım dışı 'PurgeDisabled' özelliği kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="50143-2991">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="50143-2992">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="50143-2992">Az.MachineLearning</span></span>
- <span data-ttu-id="50143-2993">Az.MachineLearningCompute modülünden cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2993">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="50143-2994">Az.Media</span><span class="sxs-lookup"><span data-stu-id="50143-2994">Az.Media</span></span>
- <span data-ttu-id="50143-2995">New-AzMediaService cmdlet’inden kullanım dışı -Tags diğer adı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="50143-2995">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="50143-2996">Az.Network</span><span class="sxs-lookup"><span data-stu-id="50143-2996">Az.Network</span></span>
<span data-ttu-id="50143-2997">Application Gateway’de RewriteRuleSets parametresini yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-2997">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="50143-2998">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="50143-2998">New cmdlets added:</span></span>
        - <span data-ttu-id="50143-2999">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="50143-2999">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="50143-3000">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="50143-3000">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="50143-3001">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="50143-3001">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="50143-3002">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="50143-3002">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="50143-3003">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="50143-3003">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="50143-3004">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="50143-3004">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="50143-3005">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="50143-3005">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="50143-3006">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="50143-3006">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="50143-3007">Cmdlet’ler isteğe bağlı -RewriteRuleSet parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-3007">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="50143-3008">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="50143-3008">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="50143-3009">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="50143-3009">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="50143-3010">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="50143-3010">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="50143-3011">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="50143-3011">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="50143-3012">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="50143-3012">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="50143-3013">New-AzureRmApplicationGatewayUrlPathMapConfig, Kimlik kullanarak Application Gateway’e KeyVault Desteği ekledi.</span><span class="sxs-lookup"><span data-stu-id="50143-3013">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="50143-3014">Cmdlet’ler isteğe bağlı -KeyVaultSecretId, -KeyVaultSecret parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-3014">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="50143-3015">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="50143-3015">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="50143-3016">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="50143-3016">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="50143-3017">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="50143-3017">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="50143-3018">New-AzApplicationGateway cmdlet’i isteğe bağlı -UserAssignedIdentity parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-3018">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="50143-3019">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="50143-3019">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="50143-3020">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="50143-3020">Az.OperationalInsights</span></span>
- <span data-ttu-id="50143-3021">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="50143-3021">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="50143-3022">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="50143-3022">Az.Profile</span></span>
- <span data-ttu-id="50143-3023">Modül adı Az.Accounts olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-3023">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="50143-3024">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="50143-3024">Az.RecoveryServices</span></span>
- <span data-ttu-id="50143-3025">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="50143-3025">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="50143-3026">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="50143-3026">Az.Resources</span></span>
- <span data-ttu-id="50143-3027">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="50143-3027">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="50143-3028">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="50143-3028">Az.ServiceFabric</span></span>
- <span data-ttu-id="50143-3029">Sertifikayı ortak ad ve parmak iziyle belirtme desteği</span><span class="sxs-lookup"><span data-stu-id="50143-3029">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="50143-3030">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="50143-3030">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="50143-3031">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="50143-3031">Az.SIgnalR</span></span>
- <span data-ttu-id="50143-3032">SIgnalR için PowerShell cmdlet'leri Genel Kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="50143-3032">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="50143-3033">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="50143-3033">Az.Sql</span></span>
- <span data-ttu-id="50143-3034">Tehdit Algılama cmdlet’lerine yeni Data_Exfiltration ve Unsafe_Action algılama türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-3034">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="50143-3035">Sql Denetimi cmdlet'leri için belge örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-3035">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="50143-3036">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="50143-3036">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="50143-3037">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="50143-3037">Az.Storage</span></span>
- <span data-ttu-id="50143-3038">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="50143-3038">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="50143-3039">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="50143-3039">Az.Websites</span></span>
- <span data-ttu-id="50143-3040">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="50143-3040">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="50143-3041">0.7.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="50143-3041">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="50143-3042">Genel</span><span class="sxs-lookup"><span data-stu-id="50143-3042">General</span></span>

* <span data-ttu-id="50143-3043">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="50143-3043">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="50143-3044">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="50143-3044">Az.Compute</span></span>

* <span data-ttu-id="50143-3045">`New-AzVm(ss)` cmdlet’leri için basit parametre kümelerinde UltraSSD ve Galeri Görüntüleri desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-3045">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="50143-3046">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="50143-3046">Az.DataLakeStore</span></span>

* <span data-ttu-id="50143-3047">Adls hesabı etki alanının sonundaki eğik çizgi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-3047">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="50143-3048">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="50143-3048">Az.FrontDoor</span></span>

* <span data-ttu-id="50143-3049">Bazı bozuk bağlantılar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-3049">Fixed some broken links</span></span>
    - <span data-ttu-id="50143-3050">New-AzureRmFrontDoor ve Set-AzureRmFrontDoor makalelerinde, New-AzureRmFrontDoorHealthProbeSettingObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-3050">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="50143-3051">New-AzureRmFrontDoorManagedRuleObject makalesinde, New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-3051">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="50143-3052">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="50143-3052">Az.RecoveryServices</span></span>

* <span data-ttu-id="50143-3053">Azure Dosya Paylaşımı geri yükleme işlemleri için istemci tarafı doğrulamalar eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-3053">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="50143-3054">Afs geri yükleme işlemi için storageAccountName ve storageAccountResourceGroupName isteğe bağlı hale getirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-3054">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="50143-3055">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="50143-3055">Az.Resources</span></span>

* <span data-ttu-id="50143-3056"> https://github.com/Azure/azure-powershell/issues/7679 düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="50143-3056">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="50143-3057">Get-AzureRmRoleAssignment, klasik yöneticiler istenirken sağlanmışsa abonelik kapsamını kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-3057">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="50143-3058">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="50143-3058">Az.Sql</span></span>

* <span data-ttu-id="50143-3059">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="50143-3059">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="50143-3060">Get-AzureRmSqlDatabaseVulnerabilityAssessment cmdlet’inin DotNet core ile kullanılması konusundaki bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-3060">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="50143-3061">SQL Denetimi cmdlet’leriyle ilgili yardım iletilerinin belgeleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-3061">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="50143-3062">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="50143-3062">Az.Storage</span></span>

* <span data-ttu-id="50143-3063">New-AzureRmStorageAccount cmdlet’ine -EnableHierarchicalNamespace eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-3063">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="50143-3064">-DestContext girilmediğinde Dosya Kopyalama cmdlet’inin hedefte kaynak bağlamını yeniden kullanamamasına yol açan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-3064">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="50143-3065">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="50143-3065">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="50143-3066">Statik Web Sitesi yapılandırması için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-3066">Support Static Website configuration</span></span>
    - <span data-ttu-id="50143-3067">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="50143-3067">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="50143-3068">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="50143-3068">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="50143-3069">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="50143-3069">Az.Websites</span></span>

* <span data-ttu-id="50143-3070">Set-AzureRmWebApp ve Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="50143-3070">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="50143-3071">Windows ve Linux kapsayıcı uygulamalarında bağlanacak Azure Depolama yollarının belirtilmesi için yeni parametre (-AzureStoragePath) eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-3071">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="50143-3072">Azure Depolama yollarını ayarlamak için yeni New-AzureRmWebAppAzureStoragePath cmdlet’inin çıktısını bir parametre olarak kullanın.</span><span class="sxs-lookup"><span data-stu-id="50143-3072">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="50143-3073">0.6.1 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="50143-3073">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="50143-3074">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="50143-3074">Az.ApiManagement</span></span>
* <span data-ttu-id="50143-3075">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="50143-3075">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="50143-3076">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="50143-3076">Az.Automation</span></span>
* <span data-ttu-id="50143-3077">Swagger tabanlı Azure Otomasyon cmdlet'leri</span><span class="sxs-lookup"><span data-stu-id="50143-3077">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="50143-3078">Güncelleştirme Yönetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-3078">Added Update Management cmdlets</span></span>
* <span data-ttu-id="50143-3079">Kaynak Denetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-3079">Added Source Control cmdlets</span></span>
* <span data-ttu-id="50143-3080">Remove-AzureRmAutomationHybridWorkerGroup cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-3080">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="50143-3081">DSC Kayıt Düğümü komutu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-3081">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="50143-3082">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="50143-3082">Az.Compute</span></span>
* <span data-ttu-id="50143-3083">SystemAssigned kimliği için kimlik sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-3083">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="50143-3084">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="50143-3084">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="50143-3085">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="50143-3085">Az.ContainerInstance</span></span>
* <span data-ttu-id="50143-3086">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="50143-3086">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="50143-3087">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="50143-3087">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="50143-3088">Market cmdlet'leri için örnekler açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-3088">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="50143-3089">Az.Network</span><span class="sxs-lookup"><span data-stu-id="50143-3089">Az.Network</span></span>
* <span data-ttu-id="50143-3090">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-3090">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="50143-3091">Desteklenen AzureFirewall Ağ Protokollerine yeniden ICMP eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-3091">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="50143-3092">Test-AzureRmNetworkWatcherConnectivity cmdlet'i güncelleştirildi; hedef kimlik, adres ve bağlantı noktasında doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-3092">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="50143-3093">VirtualNetwork eşlemesinde bellek kullanımıyla ilgili sorunlar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-3093">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="50143-3094">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="50143-3094">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="50143-3095">Korumalı dosya paylaşımı için ilke değiştirme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-3095">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="50143-3096">İlke saat dilimi büyük harfe dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="50143-3096">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="50143-3097">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="50143-3097">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="50143-3098">New-AzureRmRecoveryServicesAsrProtectableItem cmdlet'indeki örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-3098">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="50143-3099">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="50143-3099">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="50143-3100">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="50143-3100">Az.Relay</span></span>
* <span data-ttu-id="50143-3101">Kullanıcının New-AzureRmRelayKey cmdlet'ine KeyValue sağlamasına olanak tanıyan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-3101">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="50143-3102">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="50143-3102">Az.Resources</span></span>
* <span data-ttu-id="50143-3103">`New-AzureRmPolicyAssignment` ve `Set-AzureRmPolicyAssignment` cmdlet'lerindeki kaynak kimliğiyle ilgili parametrelerin yardım belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-3103">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="50143-3104">New-AzureRmPolicyDefinition cmdlet'ine -Metadata kullanan bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-3104">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="50143-3105">NetStandard'da Tag anahtarında büyük/küçük harf kullanımının korunmasına yönelik düzeltme yapıldı: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="50143-3105">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="50143-3106">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="50143-3106">Az.ServiceFabric</span></span>
* <span data-ttu-id="50143-3107">Hataya neden olan değişiklikler yayınlanacağından kullanımdan kaldırılacak özellikleri belirten iletiler eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-3107">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="50143-3108">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="50143-3108">Az.Sql</span></span>
* <span data-ttu-id="50143-3109">Azure Sql Veritabanı Yönetilen Örneği ve Azure Sql Yönetilen Veritabanı'nındaki CRUD işlemleri için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-3109">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="50143-3110">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="50143-3110">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="50143-3111">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="50143-3111">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="50143-3112">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="50143-3112">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="50143-3113">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="50143-3113">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="50143-3114">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="50143-3114">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="50143-3115">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="50143-3115">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="50143-3116">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="50143-3116">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="50143-3117">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="50143-3117">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="50143-3118">Sunucuda veya veritabanında Genişletilmiş Denetim İlkesi yönetimi etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-3118">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="50143-3119">Denetim günlüklerinde filtrelemeyi etkinleştirmek için yeni parametre (PredicateExpression) eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-3119">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="50143-3120">Cmdlet'ler, SQL istemcileri yerine Eski istemcileri kullanacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-3120">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="50143-3121">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="50143-3121">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="50143-3122">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="50143-3122">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="50143-3123">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="50143-3123">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="50143-3124">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="50143-3124">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="50143-3125">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings cmdlet'inin depolama hesabı ad parametre kümesiyle kullanılmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-3125">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="50143-3126">0.5.0 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="50143-3126">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="50143-3127">Genel</span><span class="sxs-lookup"><span data-stu-id="50143-3127">General</span></span>
* <span data-ttu-id="50143-3128">Birçok temel cmdlet’e Kaynak Tamamlayıcıları eklendi - bunlar cmdlet’leri etkileşimli olarak çağırırken mevcut kaynak adları arasında gezinmenize olanak tanır</span><span class="sxs-lookup"><span data-stu-id="50143-3128">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="50143-3129">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="50143-3129">Az.Profile</span></span>
* <span data-ttu-id="50143-3130">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-3130">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="50143-3131">Connect-AzAccount cmdlet'indeki TenantId parametresi Tenant olarak yeniden adlandırıldı ve TenantId için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-3131">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="50143-3132">Connect-AzAccount için TenantId açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-3132">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="50143-3133">Kiracı etki alanı sağlanırken başarısız oturum açma durumunda gösterilen hata iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-3133">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="50143-3134">Kiracıda abonelikleri olmayan hesaplar için bağlam adı çakışmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-3134">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="50143-3135">MSI kullanırken DataLake uç noktalarıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-3135">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="50143-3136">Bağlantı olmadığında 'Disconnect-AzAccount' oluşturulmasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-3136">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="50143-3137">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="50143-3137">Az.CognitiveServices</span></span>
* <span data-ttu-id="50143-3138">Get-AzCognitiveServicesAccountSkus işlemi eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-3138">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="50143-3139">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="50143-3139">Az.Compute</span></span>
* <span data-ttu-id="50143-3140">Add-AzVmssVMDataDisk ve Remove-AzVmssVMDataDisk cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-3140">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="50143-3141">Get-AzVMImage, AutomaticOSUpgradeProperties gösteriyor</span><span class="sxs-lookup"><span data-stu-id="50143-3141">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="50143-3142">SetAzVMChefExtension -BootstrapOptions ve -JsonAttribute seçeneği değerlerinin Json biçiminde ayarlanmamasıyla ilgili hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-3142">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="50143-3143">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="50143-3143">Az.DataLakeStore</span></span>
* <span data-ttu-id="50143-3144">DataLake paketi 1.1.10'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-3144">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="50143-3145">Çok iş parçacıklı işlemlere varsayılan Concurrency değeri eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-3145">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="50143-3146">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="50143-3146">Az.Insights</span></span>
* <span data-ttu-id="50143-3147">7267 numaralı (Otomatik ölçeklendirme alanı) sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-3147">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="50143-3148">Yeni otomatik ölçeklendirme kuralı oluşturma sırasında numaralandırılmış parametrelerin düzgün ayarlanmamasıyla ilgili sorunlar (bunlar her zaman varsayılan değere ayarlanıyordu).</span><span class="sxs-lookup"><span data-stu-id="50143-3148">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="50143-3149">Set-AzDiagnosticSetting'in ayar oluşturma sırasında kategorilerin açıkça belirtilmesini gerektirmesiyle ilgili 7513 numaralı [Insights] sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-3149">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="50143-3150">Artık cmdlet oluşturma sırasında açık kategori gösteriminin etkinleştirilmesini gerektirmiyor; başka bir deyişle belgelerinde belirtildiği gibi çalışıyor</span><span class="sxs-lookup"><span data-stu-id="50143-3150">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="50143-3151">Az.Network</span><span class="sxs-lookup"><span data-stu-id="50143-3151">Az.Network</span></span>
* <span data-ttu-id="50143-3152">Aşağıdaki parametrelerde PeeringType parametresi zorunlu parametre olarak değiştirildi:-</span><span class="sxs-lookup"><span data-stu-id="50143-3152">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="50143-3153">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="50143-3153">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="50143-3154">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="50143-3154">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="50143-3155">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="50143-3155">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="50143-3156">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="50143-3156">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="50143-3157">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="50143-3157">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="50143-3158">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="50143-3158">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="50143-3159">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="50143-3159">Az.PolicyInsights</span></span>
* <span data-ttu-id="50143-3160">İlke düzeltme cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-3160">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="50143-3161">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="50143-3161">Az.Resources</span></span>
* <span data-ttu-id="50143-3162"> https://github.com/Azure/azure-powershell/issues/7402 düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="50143-3162">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="50143-3163">'Get-AzResource' için '-ResourceId' parametresi kullanılarak kaynakların listelenmesine olanak tanındı</span><span class="sxs-lookup"><span data-stu-id="50143-3163">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="50143-3164">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="50143-3164">Az.ServiceBus</span></span>
* <span data-ttu-id="50143-3165">PSServiceBusMigrationConfigurationAttributes'e Geçiş durumunun bilinmesine yardımcı olacak salt okunur MigrationState özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-3165">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="50143-3166">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="50143-3166">Az.ServiceFabric</span></span>
* <span data-ttu-id="50143-3167">Linux Vmss'ye sertifika ekleme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-3167">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="50143-3168">'Add-AzServiceFabricClusterCertificate' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-3168">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="50143-3169">Yeni sertifikadan doğru parmak izi kullanıyor (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="50143-3169">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="50143-3170">Özel durum doğru görüntüleniyor (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="50143-3170">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="50143-3171">'Update-AzServiceFabricDurability', Vmss CreateOrUpdate işlemini başlatmadan önce küme yapılandırmasını güncelleştirecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-3171">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="50143-3172">0.4.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="50143-3172">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="50143-3173">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="50143-3173">Az.Profile</span></span>
* <span data-ttu-id="50143-3174">CloudShell’de Get-AzSubscription sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="50143-3174">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="50143-3175">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="50143-3175">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="50143-3176">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="50143-3176">Az.Compute</span></span>
* <span data-ttu-id="50143-3177">'New-AzVm' için basit parametre kümesi kullanıldığında hızlandırılmış ağların açılacağı VM boyutları beyaz listesine yeni boyutlar eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-3177">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="50143-3178">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-3178">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="50143-3179">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="50143-3179">Az.DataLakeStore</span></span>
* <span data-ttu-id="50143-3180">Sanal Ağ Kuralları desteği ekleme</span><span class="sxs-lookup"><span data-stu-id="50143-3180">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="50143-3181">Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store sanal ağ kuralını alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="50143-3181">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="50143-3182">Add-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabına sanal ağ kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="50143-3182">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="50143-3183">Set-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabındaki belirtilen sanal ağ kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="50143-3183">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="50143-3184">Remove-AzDataLakeStoreVirtualNetworkRule: Bir Azure Data Lake Store sanal ağ kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="50143-3184">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="50143-3185">Az.Network</span><span class="sxs-lookup"><span data-stu-id="50143-3185">Az.Network</span></span>
* <span data-ttu-id="50143-3186">Test-AzNetworkWatcherConnectivity cmdlet'i güncelleştirildi, arka uca protokol değerini geçiriyor.</span><span class="sxs-lookup"><span data-stu-id="50143-3186">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="50143-3187">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-3187">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="50143-3188">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="50143-3188">Az.Resources</span></span>
* <span data-ttu-id="50143-3189">Get-AzRoleDefinition cmdlet'inin anlaşılmaz bir özel durum oluşturmasına neden olan hata (varsayılan profilin içinde abonelik olmadığında ve hiçbir kapsam belirtilmediğinde), senaryoya anlamlı bir özel durum eklenerek düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="50143-3189">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="50143-3190">Ayrıca varsayılan parametre kümesi 'RoleDefinitionNameParameterSet' olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="50143-3190">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="50143-3191">0.3.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="50143-3191">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="50143-3192">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="50143-3192">Azure.Storage</span></span>
* <span data-ttu-id="50143-3193">Hedefte meta veri sorunu olduğunda Fix Copy Blob/File meta verileri kopyalamayacak</span><span class="sxs-lookup"><span data-stu-id="50143-3193">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="50143-3194">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="50143-3194">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="50143-3195">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="50143-3195">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="50143-3196">Belirli bir konumunun Depolama kaynağı kullanımını alma desteği ve genel Depolama kayrağı kullanımını almak için uyarı iletisi ekleme kullanımdan kalktı.</span><span class="sxs-lookup"><span data-stu-id="50143-3196">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="50143-3197">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="50143-3197">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="50143-3198">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="50143-3198">Az.CognitiveServices</span></span>
* <span data-ttu-id="50143-3199">Mevcut hesap olmadan Get-AzCognitiveServicesAccountSkus desteği.</span><span class="sxs-lookup"><span data-stu-id="50143-3199">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="50143-3200">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="50143-3200">Az.Compute</span></span>
* <span data-ttu-id="50143-3201">Get-AzVM -ResourceGroupName <rg> gerektiğinde 50'den fazla sonuç döndürecek şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-3201">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="50143-3202">New-AzVmss cmdlet'inin yardımına 'SimpleParameterSet' örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-3202">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="50143-3203">Azure Disk Şifrelemesi ilerleme durumu iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-3203">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="50143-3204">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="50143-3204">Az.DataFactoryV2</span></span>
* <span data-ttu-id="50143-3205">ADF .Net SDK sürümü 2.3.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="50143-3205">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="50143-3206">Az.Network</span><span class="sxs-lookup"><span data-stu-id="50143-3206">Az.Network</span></span>
* <span data-ttu-id="50143-3207">NetworkProfile işlevselliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="50143-3207">Added NetworkProfile functionality.</span></span> <span data-ttu-id="50143-3208">yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-3208">new cmdlets added</span></span>
    - <span data-ttu-id="50143-3209">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="50143-3209">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="50143-3210">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="50143-3210">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="50143-3211">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="50143-3211">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="50143-3212">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="50143-3212">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="50143-3213">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="50143-3213">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="50143-3214">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="50143-3214">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="50143-3215">Alt Ağ Modeline hizmet ilişki bağlantısı eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-3215">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="50143-3216">New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-3216">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="50143-3217">Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-3217">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="50143-3218">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="50143-3218">Az.RedisCache</span></span>
* <span data-ttu-id="50143-3219">Bundan sonra Size parametresi olarak her dizeye izin veriliyor.</span><span class="sxs-lookup"><span data-stu-id="50143-3219">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="50143-3220">PSArgumentCompleter açılan listesine P5 eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-3220">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="50143-3221">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="50143-3221">Az.Resources</span></span>
* <span data-ttu-id="50143-3222">Set-AzPolicyDefinition'a eksik -Mode parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="50143-3222">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="50143-3223">Origin öğesi User içeren işlemler için Get-AzProviderOperation commandlet hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-3223">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="50143-3224">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="50143-3224">Az.Sql</span></span>
* <span data-ttu-id="50143-3225">Bazı yedekleme cmdlet'lerinin geçerli Azure aboneliğini tanıyamamasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="50143-3225">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="50143-3226">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="50143-3226">Az.Websites</span></span>
* <span data-ttu-id="50143-3227">Yeni Get-AzWebAppContainerContinuousDeploymentUrl Cmdlet'i - Kapsayıcı Sürekli Dağıtım Web Kancası URL'sini alıyor</span><span class="sxs-lookup"><span data-stu-id="50143-3227">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="50143-3228">Yeni New-AzWebAppContainerPSSession ve Enter-WebAppContainerPSSession Cmdlet'leri - Windows kapsayıcı uygulamasında PowerShell uzak oturumunu başlatıyor</span><span class="sxs-lookup"><span data-stu-id="50143-3228">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="50143-3229">0.2.0 - Eylül 2018</span><span class="sxs-lookup"><span data-stu-id="50143-3229">0.2.0 - September 2018</span></span>
 <span data-ttu-id="50143-3230">İlk Yayın</span><span class="sxs-lookup"><span data-stu-id="50143-3230">Initial Release</span></span>
