---
title: Azure PowerShell Değişiklik Günlüğü | Microsoft Docs
description: Azure PowerShell'in en son sürümünde yapılan değişikliklerin geçmişi aşağıda verilmiştir.
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: 8515a267e80e5d1f7bb97557efa72b9e86b7b45d
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/08/2018
---
# <a name="release-notes"></a><span data-ttu-id="5e9d0-103">Sürüm notları</span><span class="sxs-lookup"><span data-stu-id="5e9d0-103">Release notes</span></span>

<span data-ttu-id="5e9d0-104">Azure PowerShell'in bu sürümünde yapılan değişikliklerin listesi aşağıda verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="5e9d0-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---

## <a name="600---may-2018"></a><span data-ttu-id="5e9d0-105">6.0.0 - Mayıs 2018</span><span class="sxs-lookup"><span data-stu-id="5e9d0-105">6.0.0 - May 2018</span></span>

### <a name="general"></a><span data-ttu-id="5e9d0-106">Genel</span><span class="sxs-lookup"><span data-stu-id="5e9d0-106">General</span></span>
* <span data-ttu-id="5e9d0-107">Modüllerin PowerShell 5.0’a en düşük bağımlılığını ayarlama</span><span class="sxs-lookup"><span data-stu-id="5e9d0-107">Set minimum dependency of modules to PowerShell 5.0</span></span>

### <a name="azurestorage"></a><span data-ttu-id="5e9d0-108">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="5e9d0-108">Azure.Storage</span></span>
* <span data-ttu-id="5e9d0-109">Depolama blob kapsayıcı adı olarak destek</span><span class="sxs-lookup"><span data-stu-id="5e9d0-109">Support  as Storage blob container name</span></span>
    - <span data-ttu-id="5e9d0-110">New-AzureStorageBlobContainer</span><span class="sxs-lookup"><span data-stu-id="5e9d0-110">New-AzureStorageBlobContainer</span></span>
    - <span data-ttu-id="5e9d0-111">Remove-AzureStorageBlobContainer</span><span class="sxs-lookup"><span data-stu-id="5e9d0-111">Remove-AzureStorageBlobContainer</span></span>
    - <span data-ttu-id="5e9d0-112">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="5e9d0-112">Set-AzureStorageBlobContent</span></span>
    - <span data-ttu-id="5e9d0-113">Get-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="5e9d0-113">Get-AzureStorageBlobContent</span></span>
* <span data-ttu-id="5e9d0-114">Bazı Depolama cmdlet’lerinin hata çıktısının ayrıntılı hata bilgilerini içermediği sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="5e9d0-114">Fix the issue that some Storage cmdlets failure output not contain detail failure information</span></span>

### <a name="azurermapimanagement"></a><span data-ttu-id="5e9d0-115">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5e9d0-115">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="5e9d0-116">Birden çok hataya neden olan değişiklik eklendi</span><span class="sxs-lookup"><span data-stu-id="5e9d0-116">Introduce multiple breaking changes</span></span>
    - <span data-ttu-id="5e9d0-117">Daha fazla bilgi için lütfen geçiş kılavuzuna bakın</span><span class="sxs-lookup"><span data-stu-id="5e9d0-117">Please refer to the migration guide for more information</span></span>

### <a name="azurermautomation"></a><span data-ttu-id="5e9d0-118">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="5e9d0-118">AzureRM.Automation</span></span>
* <span data-ttu-id="5e9d0-119">Kullanım dışı 'Tags' diğer adı cmdlet’lerden kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="5e9d0-119">Remove deprecated 'Tags' alias from cmdlets</span></span>
    - <span data-ttu-id="5e9d0-120">'Set-AzureRmAutomationRunbook'</span><span class="sxs-lookup"><span data-stu-id="5e9d0-120">'Set-AzureRmAutomationRunbook'</span></span>

### <a name="azurermbatch"></a><span data-ttu-id="5e9d0-121">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="5e9d0-121">AzureRM.Batch</span></span>
* <span data-ttu-id="5e9d0-122">New-AzureBatchPool belgeleri kullanım dışı örneği kaldırmak üzere güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="5e9d0-122">Updated New-AzureBatchPool documentation to remove deprecated example</span></span>

### <a name="azurermcdn"></a><span data-ttu-id="5e9d0-123">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="5e9d0-123">AzureRM.Cdn</span></span>
* <span data-ttu-id="5e9d0-124">Birden çok hataya neden olan değişiklik eklendi</span><span class="sxs-lookup"><span data-stu-id="5e9d0-124">Introduce multiple breaking changes</span></span>
    - <span data-ttu-id="5e9d0-125">Daha fazla bilgi için lütfen geçiş kılavuzuna bakın</span><span class="sxs-lookup"><span data-stu-id="5e9d0-125">Please refer to the migration guide for more information</span></span>

### <a name="azurermcompute"></a><span data-ttu-id="5e9d0-126">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="5e9d0-126">AzureRM.Compute</span></span>
* <span data-ttu-id="5e9d0-127">'New-AzureRmVm' ve 'New-AzureRmVmss', parametrelerin ayrıntılı çıktısını destekler</span><span class="sxs-lookup"><span data-stu-id="5e9d0-127">'New-AzureRmVm' and 'New-AzureRmVmss' support verbose output of parameters</span></span>
* <span data-ttu-id="5e9d0-128">'New-AzureRmVm' ve 'New-AzureRmVmss' (tek parametre kümesi), sanal makinelere kullanıcı tanımlı ve(veya) sistem tanımlı kimlikler atamayı destekler.</span><span class="sxs-lookup"><span data-stu-id="5e9d0-128">'New-AzureRmVm' and 'New-AzureRmVmss' (simple parameter set) support assigning user defined and(or) system defined identities to the VM(s).</span></span>
* <span data-ttu-id="5e9d0-129">VMSS Redeploy ve PerformMaintenance özelliği</span><span class="sxs-lookup"><span data-stu-id="5e9d0-129">VMSS Redeploy and PerformMaintenance feature</span></span>
    -  <span data-ttu-id="5e9d0-130">Yeni -Redeploy ve -PerformMaintenance anahtar parametresi 'Set-AzureRmVmss' ve 'Set-AzureRmVmssVM' içine eklendi</span><span class="sxs-lookup"><span data-stu-id="5e9d0-130">Add new switch parameter -Redeploy and -PerformMaintenance to 'Set-AzureRmVmss' and 'Set-AzureRmVmssVM'</span></span>
* <span data-ttu-id="5e9d0-131">DisableVMAgent anahtar parametresi 'Set-AzureRmVMOperatingSystem' cmdlet’ine eklendi</span><span class="sxs-lookup"><span data-stu-id="5e9d0-131">Add DisableVMAgent switch parameter to 'Set-AzureRmVMOperatingSystem' cmdlet</span></span>
* <span data-ttu-id="5e9d0-132">'New-AzureRmVm' ve 'New-AzureRmVmss' (basit parametre kümesi) bir 'Win10' görüntüsünü destekler.</span><span class="sxs-lookup"><span data-stu-id="5e9d0-132">'New-AzureRmVm' and 'New-AzureRmVmss' (simple parameter set) support a 'Win10' image.</span></span>
* <span data-ttu-id="5e9d0-133">'Repair-AzureRmVmssServiceFabricUpdateDomain' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="5e9d0-133">'Repair-AzureRmVmssServiceFabricUpdateDomain' cmdlet is added.</span></span>
* <span data-ttu-id="5e9d0-134">Birden çok hataya neden olan değişiklik eklendi</span><span class="sxs-lookup"><span data-stu-id="5e9d0-134">Introduce multiple breaking changes</span></span>
    - <span data-ttu-id="5e9d0-135">Daha ayrıntılı bilgi için lütfen geçiş kılavuzuna bakın</span><span class="sxs-lookup"><span data-stu-id="5e9d0-135">Please refer to the migration guide for more details</span></span>
* <span data-ttu-id="5e9d0-136">'Set-AzureRmVmDiskEncryptionExtension', AAD parametrelerini isteğe bağlı yapar</span><span class="sxs-lookup"><span data-stu-id="5e9d0-136">'Set-AzureRmVmDiskEncryptionExtension' makes AAD parameters optional</span></span>

### <a name="azurermdatafactories"></a><span data-ttu-id="5e9d0-137">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="5e9d0-137">AzureRM.DataFactories</span></span>
* <span data-ttu-id="5e9d0-138">Kullanım dışı 'Tags' diğer adı cmdlet’lerden kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="5e9d0-138">Remove deprecated 'Tags' alias from cmdlets</span></span>
    - <span data-ttu-id="5e9d0-139">New-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="5e9d0-139">New-AzureRmDataFactory</span></span>

### <a name="azurermdatafactoryv2"></a><span data-ttu-id="5e9d0-140">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="5e9d0-140">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="5e9d0-141">ADF .Net SDK sürümü, aşağıdaki değişiklikleri içeren 0.7.0-preview sürümüne güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="5e9d0-141">Updated the ADF .Net SDK version to 0.7.0-preview containing following changes:</span></span>
    - <span data-ttu-id="5e9d0-142">ExecuteSSISPackage Etkinliğine yürütme parametreleri ve connection managers özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="5e9d0-142">Added execution parameters and connection managers property on ExecuteSSISPackage Activity</span></span>
    - <span data-ttu-id="5e9d0-143">PostgreSql, MySql bağlı hizmeti, sunucu, veritabanı, şema, kullanıcı ve parola yerine tam bağlantı dizesini kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="5e9d0-143">Updated PostgreSql, MySql llinked service to use full connection string instead of server, database, schema, username and password</span></span>
    - <span data-ttu-id="5e9d0-144">Şemaya DB2 bağlı hizmetinden kaldırdı</span><span class="sxs-lookup"><span data-stu-id="5e9d0-144">Removed the schema from DB2 linked service</span></span>
    - <span data-ttu-id="5e9d0-145">Schema özelliği Teradata bağlı hizmetinden kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="5e9d0-145">Removed schema property from Teradata linked service</span></span>
    - <span data-ttu-id="5e9d0-146">Responsys için LinkedService, Dataset, CopySource eklendi</span><span class="sxs-lookup"><span data-stu-id="5e9d0-146">Added LinkedService, Dataset, CopySource for Responsys</span></span>

### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="5e9d0-147">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="5e9d0-147">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="5e9d0-148">Kullanım dışı 'Tags' diğer adı cmdlet’lerden kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="5e9d0-148">Remove deprecated 'Tags' alias from cmdlets</span></span>
    - <span data-ttu-id="5e9d0-149">'New-AzureRmDataLakeAnalyticsAccount'</span><span class="sxs-lookup"><span data-stu-id="5e9d0-149">'New-AzureRmDataLakeAnalyticsAccount'</span></span>
    - <span data-ttu-id="5e9d0-150">'Set-AzureRmDataLakeAnalyticsAccount'</span><span class="sxs-lookup"><span data-stu-id="5e9d0-150">'Set-AzureRmDataLakeAnalyticsAccount'</span></span>

### <a name="azurermdatalakestore"></a><span data-ttu-id="5e9d0-151">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5e9d0-151">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="5e9d0-152">Özyinelemeli yeni Acl Değişikliği özelliği Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl cmdlet’lerine eklendi</span><span class="sxs-lookup"><span data-stu-id="5e9d0-152">Add new feature of recursive Acl Change to Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="5e9d0-153">Bir dizin altındaki içerik özetini almak için yeni cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="5e9d0-153">Add new cmdlet for retrieving the content summary under a directory</span></span>
* <span data-ttu-id="5e9d0-154">Disk kullanımı ve Acl yedek kopyasını almak için yeni cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="5e9d0-154">Add new cmdlet for retrieving the disk usage and Acl dump</span></span>
* <span data-ttu-id="5e9d0-155">Set-AzureRmDataLakeStoreItemAcl bool değerinin dönüş türü IEnumerable<DataLakeStoreItemAce> olarak düzeltildi</span><span class="sxs-lookup"><span data-stu-id="5e9d0-155">Correct return type of Set-AzureRmDataLakeStoreItemAcl bool to IEnumerable<DataLakeStoreItemAce></span></span>
* <span data-ttu-id="5e9d0-156">Set-AzureRmDataLakeStoreItemAclEntry bool değerinin dönüş türü IEnumerable<DataLakeStoreItemAce> olarak düzeltildi</span><span class="sxs-lookup"><span data-stu-id="5e9d0-156">Correct return type of Set-AzureRmDataLakeStoreItemAclEntry bool to IEnumerable<DataLakeStoreItemAce></span></span>
* <span data-ttu-id="5e9d0-157">Export-AzureRmDataLakeStoreItem, Import-AzureRmDataLakeStoreItem, Remove-AzureRmDataLakeStoreItem cmdlet’lerinde hataya neden olan değişiklikler</span><span class="sxs-lookup"><span data-stu-id="5e9d0-157">Breaking changes in Export-AzureRmDataLakeStoreItem, Import-AzureRmDataLakeStoreItem, Remove-AzureRmDataLakeStoreItem</span></span>

### <a name="azurermdns"></a><span data-ttu-id="5e9d0-158">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="5e9d0-158">AzureRM.Dns</span></span>
* <span data-ttu-id="5e9d0-159">Birden çok hataya neden olan değişiklik eklendi</span><span class="sxs-lookup"><span data-stu-id="5e9d0-159">Introduce multiple breaking changes</span></span>
    - <span data-ttu-id="5e9d0-160">Daha fazla bilgi için lütfen geçiş kılavuzuna bakın</span><span class="sxs-lookup"><span data-stu-id="5e9d0-160">Please refer to the migration guide for more information</span></span>

### <a name="azurermeventhub"></a><span data-ttu-id="5e9d0-161">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="5e9d0-161">AzureRM.EventHub</span></span>
* <span data-ttu-id="5e9d0-162">Cmdlet Yardımı, eksik örneklerle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="5e9d0-162">Updated Help for cmdlets with missing examples</span></span>

### <a name="azurerminsights"></a><span data-ttu-id="5e9d0-163">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="5e9d0-163">AzureRM.Insights</span></span>
* <span data-ttu-id="5e9d0-164">Birden çok hataya neden olan değişiklik eklendi</span><span class="sxs-lookup"><span data-stu-id="5e9d0-164">Introduced multiple breaking changes</span></span>
    - <span data-ttu-id="5e9d0-165">Daha fazla bilgi için lütfen geçiş kılavuzuna bakın</span><span class="sxs-lookup"><span data-stu-id="5e9d0-165">Please refer to the migration guide for more information</span></span>

### <a name="azurermiothub"></a><span data-ttu-id="5e9d0-166">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="5e9d0-166">AzureRM.IotHub</span></span>
* <span data-ttu-id="5e9d0-167">IotHub’da etiketler ve Temel Sku etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="5e9d0-167">Enable tags and Basic Sku to the IotHub</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="5e9d0-168">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5e9d0-168">AzureRM.KeyVault</span></span>
* <span data-ttu-id="5e9d0-169">Kanal oluşturma senaryolarını desteklemek amacıyla hataya neden olan değişiklikler</span><span class="sxs-lookup"><span data-stu-id="5e9d0-169">Breaking changes to support piping scenarios</span></span>
* <span data-ttu-id="5e9d0-170">Yeni cmdlet’ler eklendi: Backup/Restore-AzureKeyVaultManagedStorageAccount, Backup/Restore-AzureKeyVaultCertificate, Undo-AzureKeyVaultManagedStorageSasDefinitionRemoval ve Undo-AzureKeyVaultManagedStorageAccountRemoval</span><span class="sxs-lookup"><span data-stu-id="5e9d0-170">Added new cmdlets: Backup/Restore-AzureKeyVaultManagedStorageAccount, Backup/Restore-AzureKeyVaultCertificate, Undo-AzureKeyVaultManagedStorageSasDefinitionRemoval, and Undo-AzureKeyVaultManagedStorageAccountRemoval</span></span>

### <a name="azurermmachinelearning"></a><span data-ttu-id="5e9d0-171">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="5e9d0-171">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="5e9d0-172">Kullanım dışı 'Tags' diğer adı cmdlet’lerden kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="5e9d0-172">Remove deprecated 'Tags' alias from cmdlets</span></span>
    - <span data-ttu-id="5e9d0-173">Update-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="5e9d0-173">Update-AzureRmMlCommitmentPlan</span></span>

### <a name="azurermmedia"></a><span data-ttu-id="5e9d0-174">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="5e9d0-174">AzureRM.Media</span></span>
* <span data-ttu-id="5e9d0-175">Kullanım dışı 'Tags' diğer adı cmdlet’lerden kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="5e9d0-175">Remove deprecated 'Tags' alias from cmdlets</span></span>
    - <span data-ttu-id="5e9d0-176">'Set-AzureRmMediaService'</span><span class="sxs-lookup"><span data-stu-id="5e9d0-176">'Set-AzureRmMediaService'</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="5e9d0-177">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="5e9d0-177">AzureRM.Network</span></span>
* <span data-ttu-id="5e9d0-178">DDoS koruması plan kaynağı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="5e9d0-178">Add support for DDoS protection plan resource</span></span>
* <span data-ttu-id="5e9d0-179">Birden çok hataya neden olan değişiklik eklendi</span><span class="sxs-lookup"><span data-stu-id="5e9d0-179">Introduced multiple breaking changes</span></span>
    - <span data-ttu-id="5e9d0-180">Daha fazla bilgi için lütfen geçiş kılavuzuna bakın</span><span class="sxs-lookup"><span data-stu-id="5e9d0-180">Please refer to the migration guide for more information</span></span>

### <a name="azurermnotificationhubs"></a><span data-ttu-id="5e9d0-181">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="5e9d0-181">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="5e9d0-182">Birden çok hataya neden olan değişiklik eklendi</span><span class="sxs-lookup"><span data-stu-id="5e9d0-182">Introduce multiple breaking changes</span></span>
    - <span data-ttu-id="5e9d0-183">Daha fazla bilgi için lütfen geçiş kılavuzuna bakın</span><span class="sxs-lookup"><span data-stu-id="5e9d0-183">Please refer to the migration guide for more information</span></span>

### <a name="azurermoperationalinsights"></a><span data-ttu-id="5e9d0-184">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="5e9d0-184">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="5e9d0-185">Birden çok hataya neden olan değişiklik eklendi</span><span class="sxs-lookup"><span data-stu-id="5e9d0-185">Introduce multiple breaking changes</span></span>
    - <span data-ttu-id="5e9d0-186">Daha fazla bilgi için lütfen geçiş kılavuzuna bakın</span><span class="sxs-lookup"><span data-stu-id="5e9d0-186">Please refer to the migration guide for more information</span></span>

### <a name="azurermprofile"></a><span data-ttu-id="5e9d0-187">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="5e9d0-187">AzureRM.Profile</span></span>
* <span data-ttu-id="5e9d0-188">Bağlam otomatik kaydı varsayılan olarak etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="5e9d0-188">Enable context autosave by default</span></span>
* <span data-ttu-id="5e9d0-189">Azure US Gov ortamına USGovernmentOperationalInsightsEndpoint ve USGovernmentOperationalInsightsEndpointResourceId özellikleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="5e9d0-189">Add USGovernmentOperationalInsightsEndpoint and USGovernmentOperationalInsightsEndpointResourceId properties to Azure environment for US Gov.</span></span>

### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="5e9d0-190">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="5e9d0-190">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="5e9d0-191">SiteRecovery senaryolarında Kimlik Doğrulama Üst Bilgisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="5e9d0-191">Fixed Authentication Header in SiteRecovery scenarios</span></span>

### <a name="azurermrediscache"></a><span data-ttu-id="5e9d0-192">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="5e9d0-192">AzureRM.RedisCache</span></span>
* <span data-ttu-id="5e9d0-193">Birden çok hataya neden olan değişiklik eklendi</span><span class="sxs-lookup"><span data-stu-id="5e9d0-193">Introduced multiple breaking changes</span></span>
    - <span data-ttu-id="5e9d0-194">Daha fazla bilgi için lütfen geçiş kılavuzuna bakın</span><span class="sxs-lookup"><span data-stu-id="5e9d0-194">Please refer to the migration guide for more information</span></span>

### <a name="azurermresources"></a><span data-ttu-id="5e9d0-195">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="5e9d0-195">AzureRM.Resources</span></span>
* <span data-ttu-id="5e9d0-196">Geçersiz -AtScopeAndBelow parametresi Get-AzureRmRoledefinition çağrısından kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="5e9d0-196">Remove obsolete parameter -AtScopeAndBelow from Get-AzureRmRoledefinition call</span></span>
* <span data-ttu-id="5e9d0-197">Silinen USers/Groups/ServicePrincipals atamaları Get-AzureRmRoleAssignment sonucuna eklendi</span><span class="sxs-lookup"><span data-stu-id="5e9d0-197">Include assignments to deleted USers/Groups/ServicePrincipals in Get-AzureRmRoleAssignment result</span></span>
* <span data-ttu-id="5e9d0-198">Scope ve ResourceType için Tab tamamlayıcıları eklendi</span><span class="sxs-lookup"><span data-stu-id="5e9d0-198">Add Tab completers for Scope and ResourceType</span></span>
* <span data-ttu-id="5e9d0-199">ServicePrincipals oluşturmak için kolaylık cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="5e9d0-199">Add convenience cmdlet for creating ServicePrincipals</span></span>
* <span data-ttu-id="5e9d0-200">Get- ve Find- işlevselliği Get-AzureRmResource içinde birleştirildi</span><span class="sxs-lookup"><span data-stu-id="5e9d0-200">Merge Get- and Find- functionality in Get-AzureRmResource</span></span>
* <span data-ttu-id="5e9d0-201">AD Cmdlet’leri eklendi:</span><span class="sxs-lookup"><span data-stu-id="5e9d0-201">Add AD Cmdlets:</span></span>
  - <span data-ttu-id="5e9d0-202">Remove-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="5e9d0-202">Remove-AzureRmADGroupMember</span></span>
  - <span data-ttu-id="5e9d0-203">Get-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="5e9d0-203">Get-AzureRmADGroup</span></span>
  - <span data-ttu-id="5e9d0-204">New-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="5e9d0-204">New-AzureRmADGroup</span></span>
  - <span data-ttu-id="5e9d0-205">Remove-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="5e9d0-205">Remove-AzureRmADGroup</span></span>
  - <span data-ttu-id="5e9d0-206">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="5e9d0-206">Remove-AzureRmADUser</span></span>
  - <span data-ttu-id="5e9d0-207">Update-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="5e9d0-207">Update-AzureRmADApplication</span></span>
  - <span data-ttu-id="5e9d0-208">Update-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="5e9d0-208">Update-AzureRmADServicePrincipal</span></span>
  - <span data-ttu-id="5e9d0-209">Update-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="5e9d0-209">Update-AzureRmADUser</span></span>

### <a name="azurermservicefabric"></a><span data-ttu-id="5e9d0-210">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5e9d0-210">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="5e9d0-211">Varsayılan Linux görüntü sürümü sku’su güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="5e9d0-211">Update default Linux image version sku</span></span>
  - <span data-ttu-id="5e9d0-212">NewAzureServiceFabricCluster.cs default UbuntuServer1604 Sku güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="5e9d0-212">NewAzureServiceFabricCluster.cs default UbuntuServer1604 Sku update</span></span>

### <a name="azurermstorage"></a><span data-ttu-id="5e9d0-213">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="5e9d0-213">AzureRM.Storage</span></span>
* <span data-ttu-id="5e9d0-214">Birden çok hataya neden olan değişiklik eklendi</span><span class="sxs-lookup"><span data-stu-id="5e9d0-214">Introduced multiple breaking changes</span></span>
    - <span data-ttu-id="5e9d0-215">Daha fazla bilgi için lütfen geçiş kılavuzuna bakın</span><span class="sxs-lookup"><span data-stu-id="5e9d0-215">Please refer to the migration guide for more information</span></span>

### <a name="azurermwebsites"></a><span data-ttu-id="5e9d0-216">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="5e9d0-216">AzureRM.Websites</span></span>
* <span data-ttu-id="5e9d0-217">Web Siteleri SDK'sının en son sürümüne yükseltildi</span><span class="sxs-lookup"><span data-stu-id="5e9d0-217">Upgrade to latest version of the Websites SDK</span></span>
* <span data-ttu-id="5e9d0-218">Set-AzureRmWebApp ve Set-AzureRmWebAppSlot için -AssignIdentity ve -Httpsonly özellikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="5e9d0-218">Added -AssignIdentity & -Httpsonly properties for Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
* <span data-ttu-id="5e9d0-219">İki yeni cmdlet eklendi: Get-AzureRmWebAppSnapshots ve Restore-AzureRmWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="5e9d0-219">Added two new cmdlets: Get-AzureRmWebAppSnapshots and Restore-AzureRmWebAppSnapshot</span></span>
