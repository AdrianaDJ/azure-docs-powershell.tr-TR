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
ms.openlocfilehash: 255e26aea5ea3cea866faa0d095cdf643c8ef0a8
ms.sourcegitcommit: de0e60800df1add9f3400166faacca202ef567d9
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/03/2018
ms.locfileid: "37406673"
---
# <a name="release-notes"></a><span data-ttu-id="5c59e-103">Sürüm notları</span><span class="sxs-lookup"><span data-stu-id="5c59e-103">Release notes</span></span>

<span data-ttu-id="5c59e-104">Azure PowerShell'in bu sürümünde yapılan değişikliklerin listesi aşağıda verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="5c59e-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="640---july-2018"></a><span data-ttu-id="5c59e-105">6.4.0 - Temmuz 2018</span><span class="sxs-lookup"><span data-stu-id="5c59e-105">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="5c59e-106">Genel</span><span class="sxs-lookup"><span data-stu-id="5c59e-106">General</span></span>
* <span data-ttu-id="5c59e-107">Modüllerin çoğu için yardım dosyalarındaki OutputType biçimlendirmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="5c59e-107">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="5c59e-108">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="5c59e-108">AzureRM.Profile</span></span>
* <span data-ttu-id="5c59e-109">Temel çıkış türlerine Ps1Xml özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="5c59e-109">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="5c59e-110">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="5c59e-110">AzureRM.Compute</span></span>
* <span data-ttu-id="5c59e-111">VMSS için IP Etiketi özelliği</span><span class="sxs-lookup"><span data-stu-id="5c59e-111">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="5c59e-112">'New-AzureRmVmssIpTagConfig' cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="5c59e-112">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="5c59e-113">New-AzureRmVmssIpConfig cmdlet'ine IpTag parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="5c59e-113">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="5c59e-114">VMSS için Otomatik İşletim Sistemi Geri Alma özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="5c59e-114">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="5c59e-115">New-AzureRmVmssConfig ve Update-AzureRmVmss cmdlet'lerine DisableAutoRollback parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="5c59e-115">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="5c59e-116">VMSS için İşletim Sistemi Yükseltme Geçmişi özelliği</span><span class="sxs-lookup"><span data-stu-id="5c59e-116">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="5c59e-117">Get-AzureRmVmss cmdlet'ine OSUpgradeHistory anahtarı parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="5c59e-117">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="5c59e-118">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="5c59e-118">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="5c59e-119">Aşağıdaki komutlarla Katalog ACL'si için destek eklendi:</span><span class="sxs-lookup"><span data-stu-id="5c59e-119">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="5c59e-120">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="5c59e-120">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="5c59e-121">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="5c59e-121">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="5c59e-122">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="5c59e-122">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="5c59e-123">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5c59e-123">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="5c59e-124">Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry ve Set-AzureRmDataLakeStoreItemAcl için iptal desteği ve ilerleme izleme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="5c59e-124">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="5c59e-125">Export-AzureRmDataLakeStoreChildItemProperties için iptal desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="5c59e-125">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="5c59e-126">Özyinelemeli işlemler gerçekleştiren cmdlet'ler için hata ayıklama iletilerinin boşaltılması hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="5c59e-126">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="5c59e-127">DataLake cmdlet'lerinin test konumu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="5c59e-127">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="5c59e-128">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="5c59e-128">AzureRM.EventHub</span></span>
* <span data-ttu-id="5c59e-129">Get-AzureRmEventHub ve Get-AzureRmEventHubConsumerGroup Listeleme İşlemleri cmdlet'lerine İsteğe Bağlı MaxCount parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="5c59e-129">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="5c59e-130">New-AzureRmEventHub cmdlet'inde yeni Olay Hub'ı oluşturma sırasında en az bir parametreye ihtiyaç duyma sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="5c59e-130">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="5c59e-131">Varsayılan Parametre kümesi sağlandı.</span><span class="sxs-lookup"><span data-stu-id="5c59e-131">Provided Default Parameter set.</span></span>
* <span data-ttu-id="5c59e-132">Kullanıcının New-AzureRmEventHubKey cmdlet'ine KeyValue eklemesini sağlayan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="5c59e-132">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="5c59e-133">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5c59e-133">AzureRM.KeyVault</span></span>
* <span data-ttu-id="5c59e-134">Get-AzureRmKeyVault -Tag ile tüm kaynakların döndürülmesine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="5c59e-134">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="5c59e-135">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="5c59e-135">AzureRM.Network</span></span>
* <span data-ttu-id="5c59e-136">Zone-Redundant VirtualNetworkGateways için yeni SKU'lar kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="5c59e-136">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="5c59e-137">ARM aracılığıyla ExpressRoute Partner API'leri özelliği için yeni komutlar eklendi</span><span class="sxs-lookup"><span data-stu-id="5c59e-137">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="5c59e-138">Get-AzureRmExpressRouteCrossConnection eklendi</span><span class="sxs-lookup"><span data-stu-id="5c59e-138">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="5c59e-139">Set-AzureRmExpressRouteCrossConnection eklendi</span><span class="sxs-lookup"><span data-stu-id="5c59e-139">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="5c59e-140">Add-AzureRmExpressRouteCrossConnectionPeering eklendi</span><span class="sxs-lookup"><span data-stu-id="5c59e-140">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="5c59e-141">Get-AzureRmExpressRouteCrossConnectionPeering eklendi</span><span class="sxs-lookup"><span data-stu-id="5c59e-141">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="5c59e-142">Remove-AzureRmExpressRouteCrossConnectionPeering eklendi</span><span class="sxs-lookup"><span data-stu-id="5c59e-142">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="5c59e-143">Get-AzureRMExpressRouteCrossConnectionArpTable eklendi</span><span class="sxs-lookup"><span data-stu-id="5c59e-143">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="5c59e-144">Get-AzureRMExpressRouteCrossConnectionRouteTable eklendi</span><span class="sxs-lookup"><span data-stu-id="5c59e-144">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="5c59e-145">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary eklendi</span><span class="sxs-lookup"><span data-stu-id="5c59e-145">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="5c59e-146">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="5c59e-146">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="5c59e-147">Get-AzureRmRecoveryServicesBackupStatus cmdlet'i eklendi.</span><span class="sxs-lookup"><span data-stu-id="5c59e-147">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="5c59e-148">Bu cmdlet bir sanal makinenin kimliğini alır ve sanal makinenin abonelik içindeki kasaların koruması altında olup olmadığını denetler.</span><span class="sxs-lookup"><span data-stu-id="5c59e-148">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="5c59e-149">Böyle bir kasa varsa cmdlet, bu kasanın ayrıntılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5c59e-149">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="5c59e-150">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="5c59e-150">AzureRM.Resources</span></span>
* <span data-ttu-id="5c59e-151">Get-AzureRmPolicyAssignment cmdlet'leri güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="5c59e-151">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="5c59e-152">Yönetim grubu düzeyinde -Scope değerlerini listeleme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="5c59e-152">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="5c59e-153">Yönetim grubu düzeyinde -Scope değerlerine sahip olan tek atamaları alma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="5c59e-153">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="5c59e-154">control parametresine -Effective ve -All anahtarları eklendi</span><span class="sxs-lookup"><span data-stu-id="5c59e-154">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="5c59e-155">Get/New/Remove/Set-AzureRmPolicyDefinition cmdlet'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="5c59e-155">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="5c59e-156">Belirli bir yönetim grubuna işlem uygulamayı sağlayan için -ManagementGroupName parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="5c59e-156">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="5c59e-157">Belirli bir aboneliğe işlem uygulamayı sağlayan Add -SubscriptionId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="5c59e-157">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="5c59e-158">Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlet'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="5c59e-158">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="5c59e-159">Belirli bir yönetim grubuna işlem uygulamayı sağlayan -ManagementGroupName parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="5c59e-159">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="5c59e-160">Belirli bir aboneliğe işlem uygulamayı sağlayan Add -SubscriptionId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="5c59e-160">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="5c59e-161">'New-AzureRmResourceGroupDeployment' içinde 'TemplateParameterObject' kullanırken parametrelerde KeyVault gizli dizi başvurusu desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="5c59e-161">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="5c59e-162">'New-AzureRmADAppCredential' için '-EndDate' parametresinin yoksayılmasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="5c59e-162">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="5c59e-163">'Add-AzureRmADGroupMember' cmdlet'inin istekte bulunmak için yanlış URL'yi kullandığı sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="5c59e-163">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="5c59e-164">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="5c59e-164">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="5c59e-165">Kullanıcının New-AzureRmServiceBusKey cmdlet'ine KeyValue eklemesini sağlayan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="5c59e-165">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="5c59e-166">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="5c59e-166">AzureRM.Sql</span></span>
* <span data-ttu-id="5c59e-167">New-AzureRmSqlDatabaseRestorePoint yardımında Kullanıcı Tanımlı Geri Yükleme Noktaları netleştirildi</span><span class="sxs-lookup"><span data-stu-id="5c59e-167">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="5c59e-168">Birden fazla cmdlet'te -ComputeGeneration parametresinin belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="5c59e-168">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="5c59e-169">6.3.0 - Haziran 2018</span><span class="sxs-lookup"><span data-stu-id="5c59e-169">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="5c59e-170">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="5c59e-170">AzureRM.Profile</span></span>
* <span data-ttu-id="5c59e-171">Enable-AzureRmContextAutoSave için hata iletileri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="5c59e-171">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="5c59e-172">'Connect-AzureRmAccount' cmdlet'i eski bir bağlam olmadan çalıştırıldığında her abonelik için bir bağlam oluşturur</span><span class="sxs-lookup"><span data-stu-id="5c59e-172">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="5c59e-173">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="5c59e-173">Azure.Storage</span></span>
* <span data-ttu-id="5c59e-174">Yardım dosyalarına -Permissions parametresi hakkında daha fazla bilgi eklendi.</span><span class="sxs-lookup"><span data-stu-id="5c59e-174">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="5c59e-175">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="5c59e-175">AzureRM.Compute</span></span>
* <span data-ttu-id="5c59e-176">'Get-AzureRmVmDiskEncryptionStatus' için veri diski bulunmayan VM'lerde karşılaşılan bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="5c59e-176">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="5c59e-177">Aşağıdaki cmdlet'leri düzeltmek için bilgisayar istemci kitaplığı sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="5c59e-177">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="5c59e-178">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="5c59e-178">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="5c59e-179">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="5c59e-179">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="5c59e-180">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="5c59e-180">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="5c59e-181">Aşağıdaki cmdlet'ler 'operation ID' ve 'operation status' bilgilerini doğru gösterecek şekilde düzeltildi:</span><span class="sxs-lookup"><span data-stu-id="5c59e-181">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="5c59e-182">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5c59e-182">Start-AzureRmVM</span></span>
    - <span data-ttu-id="5c59e-183">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5c59e-183">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="5c59e-184">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5c59e-184">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="5c59e-185">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5c59e-185">Set-AzureRmVM</span></span>
    - <span data-ttu-id="5c59e-186">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5c59e-186">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="5c59e-187">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="5c59e-187">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="5c59e-188">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="5c59e-188">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="5c59e-189">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="5c59e-189">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="5c59e-190">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="5c59e-190">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="5c59e-191">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="5c59e-191">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="5c59e-192">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="5c59e-192">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="5c59e-193">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="5c59e-193">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="5c59e-194">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="5c59e-194">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="5c59e-195">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="5c59e-195">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="5c59e-196">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="5c59e-196">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="5c59e-197">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="5c59e-197">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="5c59e-198">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="5c59e-198">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="5c59e-199">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="5c59e-199">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="5c59e-200">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="5c59e-200">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="5c59e-201">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="5c59e-201">AzureRM.EventGrid</span></span>
* <span data-ttu-id="5c59e-202">Gerekli olması halinde parametrelerin boş dizeyle değiştirilmesine izin vermek için Update-AzureRmEventGridSubscription cmdlet'i içindeki SubjectBeginsWith/SubjectEndsWith için ValidateNotNullOrEmpty doğrulama koşulları kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="5c59e-202">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="5c59e-203">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5c59e-203">AzureRM.KeyVault</span></span>
* <span data-ttu-id="5c59e-204">Get-AzureRmKeyVault -Tag çalıştırıldığında etiket döndürülmeme sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="5c59e-204">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="5c59e-205">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="5c59e-205">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="5c59e-206">Policy Insights cmdlet'leri genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="5c59e-206">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="5c59e-207">API 2018-04-04 sürümünü kullanın</span><span class="sxs-lookup"><span data-stu-id="5c59e-207">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="5c59e-208">PolicyDefinitionReferenceId, Get-AzureRmPolicyStateSummary sonuçlarına eklendi</span><span class="sxs-lookup"><span data-stu-id="5c59e-208">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="5c59e-209">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="5c59e-209">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="5c59e-210">RecoveryServices.Backup cmdlet'lerine -Vault parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="5c59e-210">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="5c59e-211">Bu parametre iletildiğinde Set-AzureRmRecoveryServicesContext cmdlet'ini geçersiz kılar.</span><span class="sxs-lookup"><span data-stu-id="5c59e-211">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="5c59e-212">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="5c59e-212">AzureRM.Sql</span></span>
* <span data-ttu-id="5c59e-213">Yardım dosyasındaki Get-AzureRmSqlDatabaseExpanded örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="5c59e-213">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="5c59e-214">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="5c59e-214">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="5c59e-215">Yardım dosyasındaki Add-AzureRmTrafficManagerEndpointConfig bölümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="5c59e-215">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="5c59e-216">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="5c59e-216">AzureRM.Websites</span></span>
* <span data-ttu-id="5c59e-217">'Set-AzureRmWebApp', -AssignIdentity kullanıldığında AppSettings verilerini geçersiz kılmayacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="5c59e-217">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="5c59e-218">'New-AzureRmWebAppSlot', isteğe bağlı parametre olarak AppServicePlan girişini kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="5c59e-218">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="5c59e-219">6.2.1 - Haziran 2018</span><span class="sxs-lookup"><span data-stu-id="5c59e-219">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="5c59e-220">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="5c59e-220">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="5c59e-221">PSWorkspace modeli Network için tür parametresini kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="5c59e-221">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="5c59e-222">6.2.0 - Haziran 2018</span><span class="sxs-lookup"><span data-stu-id="5c59e-222">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="5c59e-223">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="5c59e-223">AzureRM.Profile</span></span>
* <span data-ttu-id="5c59e-224">Modülün içeri aktarılması sırasında Newtonsoft.Json 10.0.3 sürümünün yüklenmemesine ilişkin sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="5c59e-224">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="5c59e-225">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="5c59e-225">AzureRM.Compute</span></span>
* <span data-ttu-id="5c59e-226">VMSS VM Güncelleştirme özelliği</span><span class="sxs-lookup"><span data-stu-id="5c59e-226">VMSS VM Update feature</span></span>
    - <span data-ttu-id="5c59e-227">'Update-AzureRmVmssVM' ve 'New-AzureRmVMDataDisk' cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="5c59e-227">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="5c59e-228">VMSS VM’sine veri diski eklemeyi desteklemek için 'Add-AzureRmVMDataDisk' cmdlet’ine VirtualMachineScaleSetVM parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="5c59e-228">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="5c59e-229">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="5c59e-229">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="5c59e-230">ADF .Net SDK sürümü, aşağıdaki değişiklikleri içeren 0.8.0-preview sürümüne güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="5c59e-230">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="5c59e-231">Fabrika deposunu yapılandırma işlemi eklendi</span><span class="sxs-lookup"><span data-stu-id="5c59e-231">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="5c59e-232">QuickBooks LinkedService, consumerKey ve consumerSecret özelliklerini kullanıma sunmak üzere güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="5c59e-232">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="5c59e-233">SecretBase’ten Object’e birkaç model türü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="5c59e-233">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="5c59e-234">Blob Etkinliklerini tetikleme eklendi</span><span class="sxs-lookup"><span data-stu-id="5c59e-234">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="5c59e-235">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5c59e-235">AzureRM.KeyVault</span></span>
* <span data-ttu-id="5c59e-236">Belgeler örnek çıktı ile güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="5c59e-236">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="5c59e-237">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="5c59e-237">AzureRM.Network</span></span>
* <span data-ttu-id="5c59e-238">Ağ İzleyicisi cmdlet’leri üzerindeki Trafik Analizi parametreleri etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="5c59e-238">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="5c59e-239">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="5c59e-239">AzureRM.Resources</span></span>
* <span data-ttu-id="5c59e-240">'Get-AzureRmResource' cmdlet’inden döndürülen 'PSResource' nesnesinin 'Properties' özelliğiyle ilgili bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="5c59e-240">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="5c59e-241">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="5c59e-241">AzureRM.Scheduler</span></span>
* <span data-ttu-id="5c59e-242">Güncelleştirilen ServiceBusQueueJob’ın yeni Kimlik Doğrulaması değerlerini ayarlamamasıyla ilgili bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="5c59e-242">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="5c59e-243">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="5c59e-243">AzureRM.Sql</span></span>
* <span data-ttu-id="5c59e-244">Şu cmdlet’ler isteğe bağlı LicenseType parametresiyle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="5c59e-244">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="5c59e-245">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5c59e-245">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="5c59e-246">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="5c59e-246">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="5c59e-247">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="5c59e-247">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="5c59e-248">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="5c59e-248">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="5c59e-249">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5c59e-249">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="5c59e-250">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="5c59e-250">AzureRM.Websites</span></span>
* <span data-ttu-id="5c59e-251">'New-AzureRMWebApp' Strategy kütüphanesindeki ortak algoritmaları kullanmak üzere güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="5c59e-251">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="5c59e-252">6.1.0 - Mayıs 2018</span><span class="sxs-lookup"><span data-stu-id="5c59e-252">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="5c59e-253">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="5c59e-253">AzureRM.Profile</span></span>
* <span data-ttu-id="5c59e-254">'Clear-AzureRmContext' komutunun çalıştırılmasının boş bir bağlamı önceki varsayılan bağlamın adıyla tutmasına ve böylece kullanıcının eski ad ile yeni bir bağlam oluşturamadığı bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="5c59e-254">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="5c59e-255">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="5c59e-255">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="5c59e-256">AS’de Ağ geçidi ilişkilendirme/ilişkilendirme kaldırma işlemlerini etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="5c59e-256">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="5c59e-257">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5c59e-257">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="5c59e-258">ApiVersions, ApiReleases ve ApiRevisions desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="5c59e-258">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="5c59e-259">ServiceFabric Arka Ucu desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="5c59e-259">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="5c59e-260">Application Insights Günlükçüsü desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="5c59e-260">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="5c59e-261">‘Temel’ sku’yu Api Yönetim hizmetinin geçerli sku’su olarak algılama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="5c59e-261">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="5c59e-262">Özel CA tarafından Kök veya CA olarak yayınlanan Sertifikaları yükleme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="5c59e-262">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="5c59e-263">Özel SSL sertifikalarını KeyVault ve Çoklu ara sunucu ana bilgisayar adlarıyla kabul etme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="5c59e-263">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="5c59e-264">MSI kimliği desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="5c59e-264">Added support for MSI identity</span></span>
* <span data-ttu-id="5c59e-265">İlkeleri Url ile kabul etme desteği eklendi NOT: Aşağıdaki cmdlet’ler gelecekteki sürümlerde kullanım dışı kalacaktır</span><span class="sxs-lookup"><span data-stu-id="5c59e-265">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="5c59e-266">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="5c59e-266">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="5c59e-267">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c59e-267">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="5c59e-268">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="5c59e-268">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="5c59e-269">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="5c59e-269">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="5c59e-270">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="5c59e-270">AzureRM.Batch</span></span>
* <span data-ttu-id="5c59e-271">Yeni Get-AzureBatchPoolNodeCounts cmdlet’ini yayınlama</span><span class="sxs-lookup"><span data-stu-id="5c59e-271">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="5c59e-272">Yeni AzureBatchComputeNodeServiceLogUpload cmdlet’ini yayınlama</span><span class="sxs-lookup"><span data-stu-id="5c59e-272">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="5c59e-273">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="5c59e-273">AzureRM.Consumption</span></span>
* <span data-ttu-id="5c59e-274">Get-AzureRmConsumptionUsageDetail cmdlet’inde yeni Expand, ResourceGroup, InstanceName, InstanceId, Tags ve Top parametrelerini ekleme</span><span class="sxs-lookup"><span data-stu-id="5c59e-274">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="5c59e-275">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5c59e-275">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="5c59e-276">Export-AzureRmDataLakeStoreChildItemProperties için düzeltme örneği</span><span class="sxs-lookup"><span data-stu-id="5c59e-276">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="5c59e-277">Set-AzureRmDataLakeStoreItemAclEntry komutunda Özyineleme durumu için null parametresi özel durumunu düzeltme</span><span class="sxs-lookup"><span data-stu-id="5c59e-277">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="5c59e-278">Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry’ye yönelik yardım dosyalarını düzeltme</span><span class="sxs-lookup"><span data-stu-id="5c59e-278">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="5c59e-279">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="5c59e-279">AzureRM.Network</span></span>
* <span data-ttu-id="5c59e-280">Ağ SDK sürümünü 18.0.0-önizleme’den 19.0.0-önizlemeye yükseltme</span><span class="sxs-lookup"><span data-stu-id="5c59e-280">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="5c59e-281">Protokol yapılandırması oluşturma cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="5c59e-281">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="5c59e-282">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c59e-282">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="5c59e-283">Varolan express route bağlantı hattına yeni bir bağlantı hattı ekleme cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="5c59e-283">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="5c59e-284">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="5c59e-284">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="5c59e-285">Varolan express route bağlantı hattındaki bir bağlantı hattı bağlantısını kaldırma cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="5c59e-285">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="5c59e-286">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="5c59e-286">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="5c59e-287">Bağlantı hattı bağlantısı alma cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="5c59e-287">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="5c59e-288">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="5c59e-288">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="5c59e-289">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5c59e-289">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="5c59e-290">Oluşturulan sertifikalarla sunucu kimlik doğrulaması kullanımı düzeltildi (Sorun No. 5998)</span><span class="sxs-lookup"><span data-stu-id="5c59e-290">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="5c59e-291">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="5c59e-291">AzureRM.Sql</span></span>
* <span data-ttu-id="5c59e-292">AuditActions veya AuditActionGroups’un kaldırılmasını sağlamak üzere Denetim cmdlet’leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="5c59e-292">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="5c59e-293">Yeni bir esnek saklama ilkesi ayarlarken komutun ‘Azure kurtarma hizmeti kasası ve ilkesiyle uzun süreli saklama ilkesini yapılandırma artık desteklenmiyor. Lütfen yeni esnek saklama ilkesi ile istek gönderin’ hatasını verdiği Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="5c59e-293">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="5c59e-294">komutuna ilişkin sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="5c59e-294">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="5c59e-295">Ölçek ve katman ilişkili özelliklere yönelik Sku özelliğini destekleyen yeni Veritabanı API’sini kullanmak için tüm Azure Sql Database/ElasticPool Creation/Update cmdlet’lerini güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="5c59e-295">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="5c59e-296">Güncelleştirilen cmlet’ler arasında şunlar yer almaktadır:</span><span class="sxs-lookup"><span data-stu-id="5c59e-296">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="5c59e-297">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5c59e-297">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="5c59e-298">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="5c59e-298">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="5c59e-299">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="5c59e-299">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="5c59e-300">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="5c59e-300">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="5c59e-301">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5c59e-301">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="5c59e-302">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="5c59e-302">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="5c59e-303">-Name parametresini kullanırken -ResourceGroupName parametresinin gerekli olması için 'Get-AzureRmTrafficManagerProfile'a yönelik parametreleri güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="5c59e-303">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>