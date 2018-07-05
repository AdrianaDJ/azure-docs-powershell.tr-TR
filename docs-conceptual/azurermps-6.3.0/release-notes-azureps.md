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
ms.openlocfilehash: 3811e28dda69d194d23934943fb47d562f869fc4
ms.sourcegitcommit: 5a5b6dd216d5f805204244146cf6f88ad2f34fb4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/19/2018
ms.locfileid: "36238071"
---
# <a name="release-notes"></a><span data-ttu-id="7a2bf-103">Sürüm notları</span><span class="sxs-lookup"><span data-stu-id="7a2bf-103">Release notes</span></span>

<span data-ttu-id="7a2bf-104">Azure PowerShell'in bu sürümünde yapılan değişikliklerin listesi aşağıda verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="7a2bf-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="630---june-2018"></a><span data-ttu-id="7a2bf-105">6.3.0 - Haziran 2018</span><span class="sxs-lookup"><span data-stu-id="7a2bf-105">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="7a2bf-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="7a2bf-106">AzureRM.Profile</span></span>
* <span data-ttu-id="7a2bf-107">Enable-AzureRmContextAutoSave için hata iletileri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7a2bf-107">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="7a2bf-108">'Connect-AzureRmAccount' cmdlet'i eski bir bağlam olmadan çalıştırıldığında her abonelik için bir bağlam oluşturur</span><span class="sxs-lookup"><span data-stu-id="7a2bf-108">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="7a2bf-109">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="7a2bf-109">Azure.Storage</span></span>
* <span data-ttu-id="7a2bf-110">Yardım dosyalarına -Permissions parametresi hakkında daha fazla bilgi eklendi.</span><span class="sxs-lookup"><span data-stu-id="7a2bf-110">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="7a2bf-111">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="7a2bf-111">AzureRM.Compute</span></span>
* <span data-ttu-id="7a2bf-112">'Get-AzureRmVmDiskEncryptionStatus' için veri diski bulunmayan VM'lerde karşılaşılan bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7a2bf-112">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="7a2bf-113">Aşağıdaki cmdlet'leri düzeltmek için bilgisayar istemci kitaplığı sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7a2bf-113">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="7a2bf-114">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="7a2bf-114">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="7a2bf-115">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="7a2bf-115">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="7a2bf-116">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="7a2bf-116">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="7a2bf-117">Aşağıdaki cmdlet'ler 'operation ID' ve 'operation status' bilgilerini doğru gösterecek şekilde düzeltildi:</span><span class="sxs-lookup"><span data-stu-id="7a2bf-117">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="7a2bf-118">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="7a2bf-118">Start-AzureRmVM</span></span>
    - <span data-ttu-id="7a2bf-119">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="7a2bf-119">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="7a2bf-120">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="7a2bf-120">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="7a2bf-121">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="7a2bf-121">Set-AzureRmVM</span></span>
    - <span data-ttu-id="7a2bf-122">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="7a2bf-122">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="7a2bf-123">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="7a2bf-123">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="7a2bf-124">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="7a2bf-124">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="7a2bf-125">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="7a2bf-125">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="7a2bf-126">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="7a2bf-126">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="7a2bf-127">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="7a2bf-127">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="7a2bf-128">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="7a2bf-128">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="7a2bf-129">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="7a2bf-129">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="7a2bf-130">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="7a2bf-130">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="7a2bf-131">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="7a2bf-131">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="7a2bf-132">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="7a2bf-132">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="7a2bf-133">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="7a2bf-133">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="7a2bf-134">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="7a2bf-134">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="7a2bf-135">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="7a2bf-135">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="7a2bf-136">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="7a2bf-136">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="7a2bf-137">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="7a2bf-137">AzureRM.EventGrid</span></span>
* <span data-ttu-id="7a2bf-138">Gerekli olması halinde parametrelerin boş dizeyle değiştirilmesine izin vermek için Update-AzureRmEventGridSubscription cmdlet'i içindeki SubjectBeginsWith/SubjectEndsWith için ValidateNotNullOrEmpty doğrulama koşulları kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="7a2bf-138">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="7a2bf-139">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7a2bf-139">AzureRM.KeyVault</span></span>
* <span data-ttu-id="7a2bf-140">Get-AzureRmKeyVault -Tag çalıştırıldığında etiket döndürülmeme sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7a2bf-140">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="7a2bf-141">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="7a2bf-141">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="7a2bf-142">Policy Insights cmdlet'leri genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="7a2bf-142">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="7a2bf-143">API 2018-04-04 sürümünü kullanın</span><span class="sxs-lookup"><span data-stu-id="7a2bf-143">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="7a2bf-144">PolicyDefinitionReferenceId, Get-AzureRmPolicyStateSummary sonuçlarına eklendi</span><span class="sxs-lookup"><span data-stu-id="7a2bf-144">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="7a2bf-145">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="7a2bf-145">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="7a2bf-146">RecoveryServices.Backup cmdlet'lerine -Vault parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="7a2bf-146">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="7a2bf-147">Bu parametre iletildiğinde Set-AzureRmRecoveryServicesContext cmdlet'ini geçersiz kılar.</span><span class="sxs-lookup"><span data-stu-id="7a2bf-147">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="7a2bf-148">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="7a2bf-148">AzureRM.Sql</span></span>
* <span data-ttu-id="7a2bf-149">Yardım dosyasındaki Get-AzureRmSqlDatabaseExpanded örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7a2bf-149">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="7a2bf-150">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="7a2bf-150">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="7a2bf-151">Yardım dosyasındaki Add-AzureRmTrafficManagerEndpointConfig bölümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7a2bf-151">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="7a2bf-152">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="7a2bf-152">AzureRM.Websites</span></span>
* <span data-ttu-id="7a2bf-153">'Set-AzureRmWebApp', -AssignIdentity kullanıldığında AppSettings verilerini geçersiz kılmayacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7a2bf-153">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="7a2bf-154">'New-AzureRmWebAppSlot', isteğe bağlı parametre olarak AppServicePlan girişini kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7a2bf-154">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="7a2bf-155">6.2.1 - Haziran 2018</span><span class="sxs-lookup"><span data-stu-id="7a2bf-155">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="7a2bf-156">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7a2bf-156">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="7a2bf-157">PSWorkspace modeli Network için tür parametresini kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7a2bf-157">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="7a2bf-158">6.2.0 - Haziran 2018</span><span class="sxs-lookup"><span data-stu-id="7a2bf-158">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="7a2bf-159">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="7a2bf-159">AzureRM.Profile</span></span>
* <span data-ttu-id="7a2bf-160">Modülün içeri aktarılması sırasında Newtonsoft.Json 10.0.3 sürümünün yüklenmemesine ilişkin sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7a2bf-160">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="7a2bf-161">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="7a2bf-161">AzureRM.Compute</span></span>
* <span data-ttu-id="7a2bf-162">VMSS VM Güncelleştirme özelliği</span><span class="sxs-lookup"><span data-stu-id="7a2bf-162">VMSS VM Update feature</span></span>
    - <span data-ttu-id="7a2bf-163">'Update-AzureRmVmssVM' ve 'New-AzureRmVMDataDisk' cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="7a2bf-163">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="7a2bf-164">VMSS VM’sine veri diski eklemeyi desteklemek için 'Add-AzureRmVMDataDisk' cmdlet’ine VirtualMachineScaleSetVM parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="7a2bf-164">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="7a2bf-165">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="7a2bf-165">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="7a2bf-166">ADF .Net SDK sürümü, aşağıdaki değişiklikleri içeren 0.8.0-preview sürümüne güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="7a2bf-166">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="7a2bf-167">Fabrika deposunu yapılandırma işlemi eklendi</span><span class="sxs-lookup"><span data-stu-id="7a2bf-167">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="7a2bf-168">QuickBooks LinkedService, consumerKey ve consumerSecret özelliklerini kullanıma sunmak üzere güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7a2bf-168">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="7a2bf-169">SecretBase’ten Object’e birkaç model türü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7a2bf-169">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="7a2bf-170">Blob Etkinliklerini tetikleme eklendi</span><span class="sxs-lookup"><span data-stu-id="7a2bf-170">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="7a2bf-171">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7a2bf-171">AzureRM.KeyVault</span></span>
* <span data-ttu-id="7a2bf-172">Belgeler örnek çıktı ile güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7a2bf-172">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="7a2bf-173">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="7a2bf-173">AzureRM.Network</span></span>
* <span data-ttu-id="7a2bf-174">Ağ İzleyicisi cmdlet’leri üzerindeki Trafik Analizi parametreleri etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="7a2bf-174">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="7a2bf-175">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="7a2bf-175">AzureRM.Resources</span></span>
* <span data-ttu-id="7a2bf-176">'Get-AzureRmResource' cmdlet’inden döndürülen 'PSResource' nesnesinin 'Properties' özelliğiyle ilgili bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7a2bf-176">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="7a2bf-177">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="7a2bf-177">AzureRM.Scheduler</span></span>
* <span data-ttu-id="7a2bf-178">Güncelleştirilen ServiceBusQueueJob’ın yeni Kimlik Doğrulaması değerlerini ayarlamamasıyla ilgili bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7a2bf-178">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="7a2bf-179">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="7a2bf-179">AzureRM.Sql</span></span>
* <span data-ttu-id="7a2bf-180">Şu cmdlet’ler isteğe bağlı LicenseType parametresiyle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="7a2bf-180">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="7a2bf-181">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="7a2bf-181">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="7a2bf-182">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="7a2bf-182">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="7a2bf-183">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="7a2bf-183">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="7a2bf-184">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="7a2bf-184">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="7a2bf-185">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="7a2bf-185">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="7a2bf-186">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="7a2bf-186">AzureRM.Websites</span></span>
* <span data-ttu-id="7a2bf-187">'New-AzureRMWebApp' Strategy kütüphanesindeki ortak algoritmaları kullanmak üzere güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="7a2bf-187">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="7a2bf-188">6.1.0 - Mayıs 2018</span><span class="sxs-lookup"><span data-stu-id="7a2bf-188">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="7a2bf-189">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="7a2bf-189">AzureRM.Profile</span></span>
* <span data-ttu-id="7a2bf-190">'Clear-AzureRmContext' komutunun çalıştırılmasının boş bir bağlamı önceki varsayılan bağlamın adıyla tutmasına ve böylece kullanıcının eski ad ile yeni bir bağlam oluşturamadığı bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7a2bf-190">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="7a2bf-191">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7a2bf-191">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="7a2bf-192">AS’de Ağ geçidi ilişkilendirme/ilişkilendirme kaldırma işlemlerini etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="7a2bf-192">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="7a2bf-193">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7a2bf-193">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="7a2bf-194">ApiVersions, ApiReleases ve ApiRevisions desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7a2bf-194">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="7a2bf-195">ServiceFabric Arka Ucu desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7a2bf-195">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="7a2bf-196">Application Insights Günlükçüsü desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7a2bf-196">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="7a2bf-197">‘Temel’ sku’yu Api Yönetim hizmetinin geçerli sku’su olarak algılama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7a2bf-197">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="7a2bf-198">Özel CA tarafından Kök veya CA olarak yayınlanan Sertifikaları yükleme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7a2bf-198">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="7a2bf-199">Özel SSL sertifikalarını KeyVault ve Çoklu ara sunucu ana bilgisayar adlarıyla kabul etme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7a2bf-199">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="7a2bf-200">MSI kimliği desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7a2bf-200">Added support for MSI identity</span></span>
* <span data-ttu-id="7a2bf-201">İlkeleri Url ile kabul etme desteği eklendi NOT: Aşağıdaki cmdlet’ler gelecekteki sürümlerde kullanım dışı kalacaktır</span><span class="sxs-lookup"><span data-stu-id="7a2bf-201">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="7a2bf-202">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="7a2bf-202">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="7a2bf-203">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="7a2bf-203">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="7a2bf-204">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="7a2bf-204">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="7a2bf-205">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="7a2bf-205">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="7a2bf-206">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="7a2bf-206">AzureRM.Batch</span></span>
* <span data-ttu-id="7a2bf-207">Yeni Get-AzureBatchPoolNodeCounts cmdlet’ini yayınlama</span><span class="sxs-lookup"><span data-stu-id="7a2bf-207">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="7a2bf-208">Yeni AzureBatchComputeNodeServiceLogUpload cmdlet’ini yayınlama</span><span class="sxs-lookup"><span data-stu-id="7a2bf-208">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="7a2bf-209">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="7a2bf-209">AzureRM.Consumption</span></span>
* <span data-ttu-id="7a2bf-210">Get-AzureRmConsumptionUsageDetail cmdlet’inde yeni Expand, ResourceGroup, InstanceName, InstanceId, Tags ve Top parametrelerini ekleme</span><span class="sxs-lookup"><span data-stu-id="7a2bf-210">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="7a2bf-211">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7a2bf-211">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="7a2bf-212">Export-AzureRmDataLakeStoreChildItemProperties için düzeltme örneği</span><span class="sxs-lookup"><span data-stu-id="7a2bf-212">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="7a2bf-213">Set-AzureRmDataLakeStoreItemAclEntry komutunda Özyineleme durumu için null parametresi özel durumunu düzeltme</span><span class="sxs-lookup"><span data-stu-id="7a2bf-213">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="7a2bf-214">Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry’ye yönelik yardım dosyalarını düzeltme</span><span class="sxs-lookup"><span data-stu-id="7a2bf-214">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="7a2bf-215">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="7a2bf-215">AzureRM.Network</span></span>
* <span data-ttu-id="7a2bf-216">Ağ SDK sürümünü 18.0.0-önizleme’den 19.0.0-önizlemeye yükseltme</span><span class="sxs-lookup"><span data-stu-id="7a2bf-216">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="7a2bf-217">Protokol yapılandırması oluşturma cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="7a2bf-217">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="7a2bf-218">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="7a2bf-218">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="7a2bf-219">Varolan express route bağlantı hattına yeni bir bağlantı hattı ekleme cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="7a2bf-219">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="7a2bf-220">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="7a2bf-220">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="7a2bf-221">Varolan express route bağlantı hattındaki bir bağlantı hattı bağlantısını kaldırma cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="7a2bf-221">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="7a2bf-222">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="7a2bf-222">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="7a2bf-223">Bağlantı hattı bağlantısı alma cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="7a2bf-223">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="7a2bf-224">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="7a2bf-224">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="7a2bf-225">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7a2bf-225">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="7a2bf-226">Oluşturulan sertifikalarla sunucu kimlik doğrulaması kullanımı düzeltildi (Sorun No. 5998)</span><span class="sxs-lookup"><span data-stu-id="7a2bf-226">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="7a2bf-227">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="7a2bf-227">AzureRM.Sql</span></span>
* <span data-ttu-id="7a2bf-228">AuditActions veya AuditActionGroups’un kaldırılmasını sağlamak üzere Denetim cmdlet’leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7a2bf-228">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="7a2bf-229">Yeni bir esnek saklama ilkesi ayarlarken komutun ‘Azure kurtarma hizmeti kasası ve ilkesiyle uzun süreli saklama ilkesini yapılandırma artık desteklenmiyor. Lütfen yeni esnek saklama ilkesi ile istek gönderin’ hatasını verdiği Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="7a2bf-229">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="7a2bf-230">komutuna ilişkin sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7a2bf-230">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="7a2bf-231">Ölçek ve katman ilişkili özelliklere yönelik Sku özelliğini destekleyen yeni Veritabanı API’sini kullanmak için tüm Azure Sql Database/ElasticPool Creation/Update cmdlet’lerini güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="7a2bf-231">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="7a2bf-232">Güncelleştirilen cmlet’ler arasında şunlar yer almaktadır:</span><span class="sxs-lookup"><span data-stu-id="7a2bf-232">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="7a2bf-233">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="7a2bf-233">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="7a2bf-234">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="7a2bf-234">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="7a2bf-235">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="7a2bf-235">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="7a2bf-236">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="7a2bf-236">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="7a2bf-237">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="7a2bf-237">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="7a2bf-238">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="7a2bf-238">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="7a2bf-239">-Name parametresini kullanırken -ResourceGroupName parametresinin gerekli olması için 'Get-AzureRmTrafficManagerProfile'a yönelik parametreleri güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="7a2bf-239">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>